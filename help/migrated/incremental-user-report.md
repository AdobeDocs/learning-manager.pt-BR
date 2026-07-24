---
description: A API de trabalho de relatório de usuário incremental permite que os administradores exportem apenas usuários cujos dados foram alterados em um intervalo de datas especificado. Isso elimina a necessidade de exportações completas de usuários e permite uma sincronização mais eficiente de registros novos ou atualizados de usuários.
jcr-language: en_us
title: Relatório de Usuário Incremental (API de Trabalho)
source-git-commit: d61e81b0df6a6043b938c65adaabecb5699c2ce9
workflow-type: tm+mt
source-wordcount: '1602'
ht-degree: 1%

---


# Relatório de Usuário Incremental (API de Trabalho)

## Visão geral

O Relatório de usuário incremental do Adobe Learning Manager é um novo recurso de API de trabalho que permite que os administradores e desenvolvedores de integração exportem apenas os usuários cujos dados foram alterados em uma janela de data e hora especificada. Em vez de obter a lista de usuários completa sempre, você pode solicitar uma fatia direcionada que abranja apenas usuários novos ou modificados.

Este documento abrange:

- Por que existem relatórios incrementais e quando usá-los
- Como o recurso funciona - incluindo o modelo de controle de alterações
- A nova API de trabalho para relatórios incrementais de usuários (carga, parâmetros, paginação)
- Como lidar com contas grandes (mais de 5 milhões de usuários)
- Campos rastreados vs. não rastreados
- Limitações e não-metas

## Por que usar Relatórios Incrementais

Esta seção explica a motivação para o recurso e deve ajudar você a decidir se as exportações incrementais ou completas atendem melhor à sua integração.

## O problema com exportações completas de usuários

A exportação de usuário completa atual (tipo de trabalho generateUsers) retorna cada usuário em uma conta com cada execução. Para contas de grandes empresas, isso cria dois problemas significativos:

| Cliente | Volume do usuário |
|----------|-------------|
| Cliente A | 2,1 milhões de usuários |
| Cliente B | 7 milhões de usuários |
| Cliente C | Mais de 1 milhão de usuários |
| Cliente D | 7,7 milhões de usuários (migração) |


&#x200B;* Nessas escalas, o pipeline de exportação é executado em aproximadamente 90% de utilização da CPU ao buscar, processar e armazenar dados.
&#x200B;* Os painéis de controle downstream (PowerBI, Salesforce, integrações personalizadas) assimilam novamente os registros de usuário inalterados em cada execução, desperdiçando largura de banda e tempo de processamento.
&#x200B;* Não há como perguntar “quais usuários mudaram desde a última exportação?” usando a API atual.

## Quando usar o Relatório Incremental

Use a exportação incremental quando precisar manter um sistema externo sincronizado com os dados do usuário do Adobe Learning Manager. Casos de uso típicos:

&#x200B;* Manter um painel corporativo (PowerBI, Tableau, SFDC) atualizado com as alterações do perfil do usuário.
&#x200B;* Alimentando sistemas de gerenciamento de identidade downstream com alterações de função, estado ou metadados.
&#x200B;* Execução de pipelines delta-sync noturnos ou por hora em vez de recarregamentos completos.
&#x200B;* Redução da carga de API e dos custos de transferência de dados para contas com milhões de usuários.

Use a exportação completa (generateUsers) quando precisar de uma linha de base autoritativa, por exemplo, na primeira configuração ou após um longo intervalo entre as sincronizações.

| Modo de exportação | Usar quando... |
|-------------|-----------|
| Exportação completa (generateUsers) | Inicialização inicial; contas com menos de 50 mil usuários; recuperação após uma janela de sincronização perdida. |
| Exportação incremental (generateUserIncrementalReport) | Sincronização delta normal; contas grandes; pipelines que precisam apenas de registros alterados |

## Relatório de usuário completo atual

(generateUsers) Esta seção documenta o relatório de usuário da API de trabalho existente para referência. Se já estiver familiarizado com ele, pule para a próxima seção.

## Como funciona

O relatório CSV do usuário atual é enviado como um trabalho por meio da API de trabalhos. Um pipeline do Snaplogic seleciona a tarefa, executa uma consulta MySQL no banco de dados CAPTIVATE (tabelas user, usergroup, usergroup_user) e gera um arquivo CSV.

## Filtros disponíveis

A carga suporta três filtros opcionais:

&#x200B;* `expandMetadata` - Passar true para exportar metadados como uma coluna separada.
&#x200B;* `fetchActiveUsers` - Passagem true para exportar somente usuários ativos.
&#x200B;* `peerAccountId` - Para gerar o relatório de usuário para uma conta entre parceiros.

## Colunas CSV

O CSV exportado contém as seguintes colunas:

```
internalUserID, userEmail, customerDefinedUniqueUserId, name, managerEmail,

userType, state, excludedFromGamification, pointsEarned, profile, roles,

dateCreated, lastLoginDate, dateDeleted, uiLocale, contentLocale,

timeZoneCode, userSource, group, AF_location, AF_login, AF_externalaf,

lastSocialActivityDate
```

## Carga da Solicitação

Tipo de trabalho: generateUsers. Somente função de administrador.

```
{

  "data": {

    "type": "job",

    "attributes": {

      "description": "<description of your choice>",

      "jobType": "generateUsers",

      "payload": {

        "expandMetadata": "<true to export metadata as separate column>",

        "fetchActiveUsers": "<true to export ACTIVE users only>",

        "peerAccountId": "<peerAccountId for peer account report>"

      }

    }

  }

}
```

## Limitações

&#x200B;* Sem filtragem com base em data - cada execução exporta todos os usuários.
&#x200B;* Inviável para contas grandes - esgotamento de recursos do pipeline acima de ~1 milhão de usuários.
&#x200B;* Sem capacidade incremental ou delta.

## Relatório de Usuário Incremental (generateUserIncrementalReport)

Esta seção documenta o novo recurso de relatório incremental de usuário introduzido no M46. Este é o assunto principal deste documento.

## O que é uma exportação incremental?

Uma exportação incremental retorna somente usuários cujos dados controlados tenham sido alterados dentro de uma janela de data e hora de início e término especificadas. O back-end armazena um carimbo de data/hora da última modificação para os campos controlados de cada usuário. Quando você solicita um relatório para uma determinada janela, somente os usuários cuja alteração mais recente esteja nessa janela são incluídos.

## Como funciona o modelo de controle de alterações

O Adobe Learning Manager mantém um carimbo de data e hora da última modificação que é atualizado sempre que qualquer campo controlado de um usuário é alterado.

Quando você solicita um relatório incremental com start_date_time e end_date_time, o sistema retorna os usuários cujo carimbo de data/hora da última modificação esteja entre [start_date_time, end_date_time]. Se um usuário foi modificado dentro e depois da janela (ou seja, ele foi alterado novamente após end_date_time), esse usuário não é incluído no relatório - porque seu carimbo de data/hora modificado por último agora está fora da janela.

>[!NOTE]
>
>Isso significa que uma exportação incremental captura os usuários cuja alteração mais recente esteja na janela especificada, e não todos os usuários que foram tocados em qualquer ponto durante a janela.

## Campos monitorados para alterações

Um usuário será incluído em um relatório incremental se qualquer um dos seguintes campos for alterado:

| Campo | Notas |
|---|---|
| userEmail | Endereço de email do usuário |
| nome | Nome do usuário |
| managerId | A tabela Usuário armazena managerId. Se managerId for alterado, o campo será sinalizado como alterado. Se apenas o e-mail do gerente for alterado (mesma ID do gerente), esse campo NÃO será considerado alterado. |
| type | Classificação de usuário interno ou externo |
| estado | Ativo ou excluído |
| perfil | Atribuição de perfil de usuário |
| funções | Adições ou exclusões de funções |
| uiLocale | Localidade da interface do usuário |
| contentLocale | Localidade do conteúdo |
| timeZoneCode | Fuso horário do usuário |
| Campos ativos (AF_*) | Todos os campos ativos configurados, por exemplo AF_location, AF_login |
| metadados | Todos os campos de metadados configurados |

## Campos NÃO rastreados para alterações

Os campos a seguir aparecem na saída CSV, mas não acionam a inclusão em uma exportação incremental quando são alterados:

&#x200B;* deletedFromGamification
&#x200B;* pointsEarned
&#x200B;* lastLoginDate
&#x200B;* dateDeleted
&#x200B;* dateCreated
&#x200B;* userSource
&#x200B;* lastSocialActivityDate

## Formato de saída

O relatório CSV incremental tem as mesmas colunas e formato do relatório CSV completo do usuário. Todas as colunas são exibidas na mesma ordem, incluindo todas as colunas de campo e metadados ativas - independentemente dos campos alterados para os usuários exportados.

>[!NOTE]
>
>Se um novo campo ativo for adicionado ou um existente for removido, todos os usuários afetados por essa alteração aparecerão na próxima exportação incremental. As novas colunas dos novos campos ativos são anexadas ao final do relatório para que as integrações existentes chaveadas na posição da coluna não sejam quebradas.

## Relatório de Nova API de Trabalho para Usuário Incremental

O relatório de usuário incremental usa a API de trabalho para gerar um arquivo CSV que contém usuários cujos dados rastreados foram alterados na janela de data e hora especificada. Para conjuntos de resultados grandes, use o mesmo modelo de paginação descrito posteriormente neste documento: envie a mesma janela de data em cada solicitação e transmita a última userId recebida na resposta anterior como fromUserId para recuperar a próxima parte.

## Tipo de Trabalho

Tipo de trabalho: generateUserIncrementalReport

## Carga da Solicitação

```
{

    "data": {

        "type": "job",

        "attributes": {

            "description": "description of your choice",

            "jobType": "generateUserIncrementalReport",

            "payload":{

                 "fullExport": <Pass true to export all users. If fullExport is true, fromDate and toDate are ignored>,

                 "expandMetadata": <Pass true to export metadata as separate columns>,

                 "fromDate": <Start of the change window in ISO format, for example 2020-01-01T18:30:00.000Z>,

                 "toDate": <End of the change window in ISO format, for example 2020-01-31T18:30:00.000Z>,

                 "fromUserId": <For paginated requests, pass the last userId received in the previous response>

            }

        }

   }

}
```

## Parâmetros de Carga

| Parâmetro | Tipo | Descrição |
|---|---|---|
| fromDate | String (ISO 8601) | Necessário para exportação incremental. Início da janela de alteração. Use o formato ISO 8601. |
| toDate | String (ISO 8601) | Necessário para exportação incremental. Fim da janela de alteração. Use o formato ISO 8601. |
| fromUserId | String | Opcional. Para solicitações paginadas, passe a última userId recebida na resposta anterior como fromUserId. Omita esse parâmetro para a primeira solicitação. |
| expandMetadata | Booleano | Opcional. Se verdadeiro, exporta metadados como colunas separadas. |

Para exportação incremental, passe `fromDate` e `toDate` para definir a janela de alteração. Se o conjunto de resultados for maior do que uma parte, continue a paginação enviando os mesmos `fromDate` e `toDate` e passando os últimos `userId` da resposta anterior como `fromUserId`. Se fullExport for true, a janela de data será ignorada e a API gerará uma exportação de usuário completa.

## Lidando com contas grandes (mais de 500 mil usuários)

Os relatórios de usuário são gerados usando um pipeline de plataforma de dados, e a saída é retornada em blocos para suportar contas grandes. Se uma exportação incremental abranger mais de 500.000 usuários, o relatório será paginado.

## Modelo de paginação

Para recuperar todas as páginas de uma grande exportação incremental, passe o mesmo startDateTime e endDateTime em cada solicitação e, além disso, passe o userId do último usuário recebido na parte anterior como fromUserId. A API retornará o próximo conjunto de até 500.000 usuários com userId maior que o passado deUserId.

## Fluxo de trabalho de paginação

Etapa 1: envie a primeira solicitação sem fromUserId.

```
// First request – no fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z"

  }

}
```

Etapa 2: Receba a primeira parte (até 500.000 usuários). Anote a última userId na resposta.

Etapa 3: Submeta a próxima solicitação, passando a mesma janela de data e a última userId da resposta anterior como fromUserId.

```
// Subsequent request – pass last userId from previous response as fromUserId

{

  "payload": {

    "startDateTime": "2026-05-01T00:00:00Z",

    "endDateTime": "2026-05-31T23:59:59Z",

    "fromUserId": "<last userId from previous response>"

  }

}
```

Etapa 4: Repita até que uma resposta retorne menos de 500.000 registros, indicando que você chegou à última página.

| Solicitação | Parâmetro fromUserId |
|---|---|
| Primeira página | Omitir de UserId |
| Segunda página | Passar a última userId da primeira página como fromUserId |
| Terceira página | Passar a última userId da segunda página como fromUserId |
| ... (continuar) | ... |
| Última página | A resposta contém menos de 500.000 registros |

>[!NOTE]
>
>Certifique-se de que o `startDateTime` e o `endDateTime` permaneçam idênticos em todas as solicitações paginadas para uma única execução de exportação. Alterar a paginação intermediária da janela de data produzirá resultados inconsistentes.

## Limitações

O relatório de usuário incremental tem escopo intencional. Os seguintes recursos estão fora do escopo:

&#x200B;* Não é um relatório de auditoria do usuário - ele não lista quais campos específicos foram alterados.
&#x200B;* Nenhuma comparação de valores antiga/nova - o relatório mostra apenas os valores do campo atual.
&#x200B;* Sem carimbos de data e hora por alteração - o tempo de modificações individuais de campos não é revelado.
&#x200B;* Nenhuma indicação do número de alterações - um usuário modificado uma vez e um usuário modificado dez vezes aparecem de maneira idêntica na exportação.
&#x200B;* O formato do relatório existente não foi alterado — a estrutura da coluna CSV é a mesma do relatório de usuário completo.

## Integração do conector

O relatório de usuário incremental foi projetado para ser usado em conectores do Adobe Learning Manager (PowerBI, Salesforce e outros) como uma substituição drop-in para o relatório de usuário completo em pipelines de sincronização regular. Isso permite que os conectores que hoje usam generateUsers migrem para o modelo incremental sem alterações no esquema de dados de downstream.

&#x200B;* O CSV de saída é compatível com a coluna do relatório de usuário completo.
&#x200B;* Os conectores podem usar o relatório incremental para sincronização delta e voltar ao relatório completo para inicialização ou recuperação.
&#x200B;* Suporte para integração de conector (PowerBI, SFDC)
