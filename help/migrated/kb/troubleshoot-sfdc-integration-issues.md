---
jcr-language: en_us
title: Solução de problemas de integração do Salesforce (SFDC) com o Adobe Learning Manager
description: solucionar problemas comuns de integração do Salesforce (SFDC) com o Adobe Learning Manager (ALM), incluindo exportações com falha, problemas de permissão de campo em objetos personalizados do SFDC e notas importantes de compatibilidade do SFDC-ALM.
contentowner: saghosh
source-git-commit: c57896abd8f00ca4a7b26c981eb490cd53ce437b
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---


## Solucionar problemas de falhas de exportação de SFDC (sem exportação por mais de 2 ou 3 horas)

Se a exportação de SFDC não for concluída com êxito por mais de **2-3 horas**, use as etapas abaixo para identificar e entender o problema.

1. Vá para a página **Início do Salesforce**.
2. Na caixa de pesquisa **Localização Rápida**, digite **`Bulk Data Load Jobs`** e abra-a.
3. A página exibe trabalhos de carregamento de dados em massa nos **últimos 7 dias**.
4. Procure trabalhos relacionados a **objetos do Adobe Learning Manager (ALM)**.
5. Clique no cargo específico que deseja investigar.
6. Role até a **parte inferior** da página de detalhes do trabalho para ver a **mensagem de erro** e detalhes adicionais.

Em muitos casos, a causa raiz são **permissões insuficientes no nível de campo no SFDC**. O nome do campo com falha pode se parecer com:

- `cp_Module_ID`
- ou outros campos `cp_...` relacionados a objetos personalizados do ALM.

Se esses campos aparecerem no erro, vá para a próxima seção.

## Conceder permissões de campo em campos de objeto personalizados do ALM no SFDC

Use o recurso **Acessibilidade de Campo** para corrigir problemas de permissão em campos específicos (por exemplo, `cp_Module_ID`).

### Etapas

1. Vá para a página **Início do Salesforce**.
2. Na caixa de pesquisa **Localização Rápida**, digite **`Field Accessibility`** e abra-a.
3. Na lista de objetos, selecione o **tipo de relatório/objeto** relevante.
   - Exemplo: `cp_LearnerTranscript_xxxx_xxxx` para o relatório de transcrição do aluno (LT).
4. Na próxima página, escolha **”Exibir por campos”**.
5. Na lista suspensa **campo**, selecione o campo que apareceu no erro de exportação
   - Exemplo: `cp_Module_ID`.
6. Na matriz de acesso, clique na entrada **”Oculto”** do perfil do **Administrador do Sistema** (e outros perfis relevantes, se necessário).
7. Na próxima página:
   - Habilite **”Visível”** onde for apropriado.
   - Clique em **Salvar** na parte inferior da página.
8. Depois de salvar, você retorna à exibição de acessibilidade do campo. O campo agora deve ser exibido como **”Editável”** para **Administrador do Sistema** (e qualquer outro perfil que você tenha atualizado).

## Repita o processo para todos os campos afetados e repita a exportação

1. **Repita** as etapas de acessibilidade de campo na seção 2 para **cada campo** relatado como tendo problemas de permissão em **Trabalhos de Carregamento de Dados em Massa**.
2. Depois que todos os campos problemáticos tiverem a visibilidade adequada e permissões de edição:
   - Volte para o **Adobe Learning Manager**.
   - Na configuração do **conector do SFDC**, **repita a exportação**.


## Observações importantes e limitações

Lembre-se destas especificações do SFDC-ALM ao projetar ou solucionar problemas de integrações.

### Nenhuma criação automática de objeto/campo no SFDC

- O **conector do SFDC não cria novos objetos ou campos no Salesforce**.
- Se um **novo campo for adicionado ao ALM** e você desejar que ele apareça no SFDC:
   - **crie manualmente o campo personalizado correspondente** no SFDC.
   - **Mapeie** o campo personalizado do SFDC para o **campo ALM apropriado** na configuração do conector.
   - Verifique se o novo campo tem **permissões adequadas no nível de campo** (use a seção 2).

### URL de retorno de chamada para contas do ALM com domínios personalizados

- Se a conta do ALM usar um **domínio personalizado**, a equipe de engenharia deverá **adicionar esse domínio personalizado** à **lista de permissões de URL de retorno de chamada** do aplicativo de produção OAuth do conector do SFDC.
- Isso é feito por meio de uma **solicitação Jira** para a engenharia.
- Sem isso, o fluxo de OAuth para o conector pode falhar.

### Limitação de fuso horário (UTC apenas)

- Se a organização do SFDC usar um **fuso horário diferente do UTC**, os **dados de conclusão e inscrição poderão ser perdidos** durante a sincronização.
- Motivo: no momento, o ALM **oferece suporte apenas ao fuso horário UTC** para integração ao SFDC.
- Referência interna: PAPI-24525 é elevado para suportar fusos horários adicionais.

### Limitação do tipo de dados do filtro (lista de seleção vs. lista de verificação)

- O ALM oferece suporte à importação de **filtros SFDC criados com campos de lista de seleção**.
- O ALM **não oferece suporte** a filtros baseados em campos de lista de verificação/caixa de seleção múltipla.
- Motivo: o ALM **só oferece suporte a tipos de dados de cadeia de caracteres** para filtros SFDC.
