---
description: Saiba como a Adobe Learning Manager usa o NRPS para sincronizar atributos personalizados do aluno de uma plataforma de LTI 1.3 nos perfis do aluno como campos ativos
jcr-language: en_us
title: Suporte de LTI para NRPS
exl-id: 4c972319-b8ce-4f2d-9ccb-1b93c6cc6ac0
source-git-commit: 92be9eb8ece6d083efe595894a492540cd96eead
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%
---

# Suporte de LTI para NRPS

## Visão geral

A Adobe Learning Manager oferece suporte à especificação Names and Role Provisioning Services (NRPS) quando atua como uma ferramenta Learning Tools Interoperability (LTI) 1.3. Quando um aluno inicia o Learning Manager em um sistema de gerenciamento de aprendizado externo (a plataforma), o Learning Manager recupera o registro de associação do aluno na plataforma. Em seguida, ele copia os atributos personalizados nesse registro, como departamento ou ID de funcionário, no perfil do aluno como campos ativos.

## Casos de uso

* **Aprimorar perfis de aluno automaticamente.** Traga atributos como departamento, ID de funcionário ou metadados personalizados da sua plataforma para o Learning Manager sem entrada manual de dados ou importações separadas.
* **Analise de onde vêm seus alunos.** Capture atributos de local, como país e cidade, para criar uma imagem da região de onde vêm os alunos. Use os campos de perfil resultantes para análise no Learning Manager.
* **Manter dados de perfil alinhados com a plataforma de origem.** A plataforma continua a ser a fonte da verdade. O Learning Manager atualiza os valores sempre que um aluno é iniciado.
* **Suporte a várias plataformas em uma conta.** Os prefixos de namespace mantêm os atributos de diferentes plataformas separados, mesmo quando as plataformas usam o mesmo nome de atributo.

Com a sincronização de campo personalizada NRPS, o Learning Manager faz o seguinte na inicialização:

1. Detecta que a plataforma suporta NRPS.
2. Solicita a inicialização do registro de associação do aluno na plataforma.
3. Extrai os atributos personalizados desse registro.
4. Grava os atributos no perfil do aluno como campos ativos. Cada nome de campo carrega um prefixo `<namespace>`, portanto, os atributos de plataformas diferentes não colidem.
5. O Learning Manager reutiliza o token de credenciais do cliente OAuth 2.0 que já usa para os Serviços de Atribuição e Grades (AGS). Você não precisa configurar um novo ponto de extremidade de token.

>[!NOTE]
>
>NRPS é uma especificação opcional em LTI Advantage. O suporte para NRPS e para atributos personalizados varia de acordo com a plataforma. Certifique-se de que sua plataforma expõe o NRPS 2.0 antes de planejar usar esse recurso.

## Principais recursos

* **Suporte para declarações NRPS:** o Learning Manager verifica cada inicialização de LTI 1.3 para a declaração NRPS. Se a reivindicação estiver ausente, a inicialização continua normalmente sem erros e sem impacto no aluno.
  * Esta alegação fornece as seguintes informações:
    * **Ponto de extremidade de associação:** `context_memberships_url `identifica a URL de serviço do curso ou do contexto de aprendizado a partir do qual o aluno iniciou o ALM.
    * **Versões com suporte:** `service_versions` lista as versões de NRPS disponíveis nesse ponto de extremidade.
      Este recurso oferece suporte ao NRPS 2.0.
  * **Infraestrutura de token compartilhada:** o Learning Manager adiciona o escopo NRPS à sua solicitação de token AGS existente e reutiliza o cache de token existente por registro.
* **Sincronizar parâmetros personalizados com perfis do aluno**
  * **Campos ativos prefixados por namespace:** cada atributo personalizado mapeia para um campo ativo denominado `<namespace>_<field_name>`.
  * **Criação automática de campos:** se não existir nenhum campo ativo correspondente, o Learning Manager criará um com o tipo **Texto** e o status **Ativo**.
  * **Plataforma como fonte de verdade:** o Learning Manager substitui os valores de perfil existentes pelos valores mais recentes da plataforma. Alunos e administradores não podem editar esses campos.
  * **Comportamento não bloqueado:** erros de NRPS não impedem que os alunos iniciem conteúdo de aprendizado.
  * **Várias fontes para atributos personalizados:** o Learning Manager pode ler atributos personalizados do ponto de extremidade NRPS e de parâmetros personalizados no token de inicialização de LTI. Saiba mais sobre [atributos personalizados no token de inicialização](#custom-attributes-in-the-launch-token).

## Configurações compatíveis

| Item | Suporte |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| Função do Learning Manager | Ferramenta LTI 1.3 |
| Versão de LTI | LTI 1.3 |
| Versão do serviço NRPS | 2.0 |
| Plataformas (formato de campo personalizado compatível com as especificações) | Moodle, D2L Brightspace, Blackboard (Antologia), Sakai |
| Tipo de campo personalizado | Texto |
| Acionador | Cada inicialização de LTI 1.3 |

O suporte da plataforma depende do padrão de serialização de campo personalizado usado no registro de membro do NRPS. Vários padrões podem coexistir, mas o Learning Manager processa apenas os padrões suportados na versão ativa.

## Como funciona

### Fluxo de lançamento

1. Um aluno inicia o Learning Manager na plataforma.
2. O Learning Manager lê a declaração NRPS no token de inicialização de LTI 1.3. Se a declaração listar o serviço NRPS versão 2.0, o Learning Manager armazenará os `context_memberships_url` da sessão e do contexto de LTI (curso).
3. O Learning Manager solicita um token de acesso que inclui o escopo NRPS `https://purl.imsglobal.org/spec/lti-nrps/scope/contextmembership.readonly`.
4. O Learning Manager chama `context_memberships_url?rlid=<lti_user_id>` com o token do portador para recuperar o registro do aluno que está iniciando. Se a plataforma ignorar o filtro `rlid` e retornar a lista completa, o Learning Manager encontrará o aluno por `user_id`.
5. O Learning Manager extrai os campos personalizados do registro.
6. O Learning Manager mapeia cada campo personalizado para um campo ativo e grava os valores no perfil do aluno.
7. Como alternativa, o ALM também oferece suporte à extração de parâmetros personalizados a serem sincronizados com o perfil do aluno durante a inicialização da ferramenta, se os parâmetros personalizados forem pré-fixados com o campo identificável do ALM `ALMfield`.

### Formato de campo personalizado

A especificação NRPS 2.0 define dados personalizados como uma matriz `message` no registro do membro. O Learning Manager lê os dados personalizados da declaração personalizada de LTI dentro dessa matriz. Nesta versão, o Learning Manager oferece suporte à representação de padrão S compatível com as especificações.

```json
{
  "user_id": "abc123",
  "message": [
    {
      "https://purl.imsglobal.org/spec/lti/claim/custom": {
        "department": "Engineering",
        "employee_id": "E4567"
      }
    }
  ]
}
```

### Atributos personalizados no token de inicialização

As plataformas também podem enviar atributos personalizados como parâmetros personalizados no token de inicialização de LTI. O Learning Manager coleta atributos do token de inicialização e do ponto de extremidade NRPS e os armazena no perfil do aluno.

Para atributos no token de inicialização, o nome do parâmetro deve começar com o prefixo `almfield-` que o Learning Manager exige. Sem o prefixo, o Learning Manager não consegue distinguir esses parâmetros de outros parâmetros personalizados e não os importa. Os atributos recuperados do ponto de extremidade NRPS não precisam desse prefixo. Esse prefixo só é necessário se os parâmetros personalizados forem importados no token de inicialização do ALM para identificar o campo que deve ser sincronizado com os campos ativos do aluno.

>[!NOTE]
>
>Confirme o prefixo obrigatório exato com o seu representante do Learning Manager antes de configurar parâmetros personalizados na plataforma.

### Nomeação e mapeamento de campos ativos

O Learning Manager compila o nome do campo ativo como `<namespace>_<field_name>`. Por exemplo, o campo `department` no namespace `https://purl.imsglobal.org/spec/lti/claim/custom` torna-se `https://purl.imsglobal.org/spec/lti/claim/custom_department`.

O Learning Manager aplica as seguintes regras:

* **Comprimento do nome:** se o nome exceder o limite de caracteres do nome do campo ativo, o Learning Manager encurta primeiro a parte do namespace e mantém o nome do campo.
* **Conflitos de nome:** após encurtar, o Learning Manager verifica se há conflitos com campos ativos existentes de uma origem diferente. Se houver um conflito, ele ajustará o comprimento do encurtamento até encontrar um nome exclusivo. Se não conseguir encontrar um nome exclusivo, o campo será ignorado e um erro será registrado.
* **Correspondência:** a correspondência de nomes de campo não diferencia maiúsculas de minúsculas.
* **Campo existente e habilitado:** o Learning Manager grava o valor no perfil do aluno.
* **Campo existente e desabilitado:** o Learning Manager ignora o campo sem registrar um erro.
* **Nenhum campo existente:** o Learning Manager cria um campo de **Texto** com o status **Ativo**.

### Gravação de valores no perfil

* Em cada inicialização em que o Learning Manager recupera dados NRPS, ele grava todos os valores de campo personalizado resolvidos no perfil do aluno de inicialização. Nenhum outro perfil de aluno é alterado.
* Se um campo já tiver um valor, o Learning Manager o sobrescreverá com o valor mais recente da plataforma.
* Se o valor da plataforma estiver vazio ou for nulo, o Learning Manager manterá o valor do perfil existente.
* Uma falha ao gravar um campo não bloqueia a inicialização nem as gravações de outros campos.
* O Learning Manager aplica as atualizações de campo na mesma transação de inicialização sempre que possível.
* Os alunos não podem editar campos de origem NRPS na página de perfil e os administradores não podem editar esses valores em nome de um aluno.

## Configurar sincronização de campo personalizado NRPS

### Pré-requisitos

* Sua plataforma está registrada no Learning Manager como uma ferramenta de LTI 1.3. Este recurso não oferece suporte a LTI 1.1 ou LTI 1.2.
* Sua plataforma oferece suporte ao serviço NRPS versão 2.0 e expõe atributos personalizados no formato `message` compatível com as especificações.
* O token de inicialização de LTI contém a declaração `namesroleservice`.
* A declaração fornece `context_memberships_url`, que identifica o ponto de extremidade NRPS específico do curso.
* O valor `service_versions` na declaração inclui `2.0`.
* Você tem acesso de administrador ao registro de ferramenta da plataforma.

### Conceder o escopo NRPS ao Learning Manager

Novos registros que incluem o escopo NRPS não exigem configuração adicional no Learning Manager.

Novos registros que incluem o escopo NRPS funcionam sem alterações no Learning Manager. Para um registro existente, o administrador da plataforma deve atualizar o registro da ferramenta no lado da plataforma.

>[!NOTE]
>
>Não é necessário alterar o ponto de extremidade do token, a ID do cliente ou a chave privada no Learning Manager. A configuração AGS existente é reutilizada. Se a plataforma não conceder o escopo NRPS, o Learning Manager ignorará o NRPS sem afetar o AGS ou a inicialização.

### Expor os atributos do aluno na plataforma

A plataforma controla quais atributos do aluno compartilha. As etapas exatas dependem da plataforma. Por exemplo, no Moodle:

1. Adicione o Learning Manager como uma ferramenta externa usando LTI 1.3.
2. Ative as configurações de privacidade que permitem que a plataforma compartilhe informações do aluno com a ferramenta.
3. Defina os atributos personalizados que deseja enviar. Você pode usar variáveis de plataforma ou valores predefinidos.
4. Se você também enviar atributos como parâmetros personalizados no token de inicialização, adicione o prefixo que o Learning Manager requer a cada nome de parâmetro.

>[!NOTE]
>
>Exponha apenas os atributos necessários para o caso de uso de aprendizado. O Learning Manager trata a plataforma como a fonte da verdade e não oferece consentimento separado ou controles de privacidade nesta versão.

### Verificar a sincronização

1. Inicie o Learning Manager na plataforma como um aluno de teste.
2. Confirme se a inicialização é concluída normalmente.
3. No aplicativo de administração do Learning Manager, abra a página de campos ativos.
4. Confirme se os campos aparecem com o prefixo de namespace, com o tipo **Texto** e o status **Ativo**.
5. Abra o perfil do aluno de teste e confirme se os valores correspondem à plataforma.
6. Confirme se os campos de origem NRPS são somente leitura. Nem o aluno nem um administrador podem editar manualmente os valores sincronizados.
7. Reinicie após alterar um valor de origem não vazio e verifique se o Learning Manager substitui o valor do perfil existente pelo valor NRPS mais recente.

>[!TIP]
>
>Se um campo existir mas estiver desativado, o Learning Manager não o gravará. Ative o campo se desejar preenchê-lo.

## Manipulação e registro de erros

O Learning Manager nunca bloqueia um aluno devido a um problema de NRPS. Ele não tenta novamente. Ele registra a falha e ignora a sincronização de NRPS para essa inicialização. A próxima inicialização é tentada novamente.

| Condição | Resultado |
|------------------------------------------------------------------|-------------------------------------------------------|
| A declaração NRPS está ausente do token de inicialização | NRPS ignorado. O lançamento continua. |
| Somente o serviço NRPS versão 1.0 está presente | NRPS ignorado. O lançamento continua. |
| A solicitação de token falha ou a plataforma não concede o escopo NRPS | NRPS ignorado. O AAC e o lançamento não são afetados. |
| Falha na chamada NRPS (tempo limite, 4xx ou 5xx) | O erro é registrado. O lançamento continua. |
| Aluno não encontrado na resposta NRPS | A sincronização de campo foi ignorada. O lançamento continua. |
| Nenhum campo personalizado na resposta NRPS | A sincronização de campos é ignorada sem um erro. |
| Um conflito de nome de campo não pode ser resolvido | O campo é ignorado e um erro é registrado. |
| Uma única gravação de campo falha | Outros campos ainda estão escritos. O lançamento continua. |

Cada entrada de registro inclui o carimbo de data e hora, a ID de registro da plataforma, a ID do aluno e o motivo da falha. Os administradores do sistema do Learning Manager podem acessar os registros.

## Notas

* Somente o registro do aluno que está iniciando é sincronizado. O Learning Manager não sincroniza a lista completa do curso.
* Somente há suporte para o serviço NRPS versão 2.0.
* Todos os campos sincronizados têm o tipo **Texto**. O Learning Manager não infere tipos a partir de valores. Não há suporte para tipos de campo Número, Data e Booleano.
* O Learning Manager atua como a ferramenta de LTI. Ele não atua como uma plataforma NRPS e não fornece um ponto de extremidade de lista para outras ferramentas.
* A sincronização de campo personalizado ocorre durante a inicialização da LTI.
