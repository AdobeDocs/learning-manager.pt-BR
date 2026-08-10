---
description: Gerencie o faturamento do Learning Manager, faça pedidos com cartão de crédito, assine usando um Pedido de compra ou através do plano Usuários ativos mensais.
jcr-language: en_us
title: Gerenciar pedidos e faturamento do Learning Manager
contentowner: manochan
exl-id: 91635ef7-dbb9-4bb1-98f9-129f6fd5b6b4
source-git-commit: 659829ef14fb3aea67f6bd5f191c1051f1b93a66
workflow-type: tm+mt
source-wordcount: '2660'
ht-degree: 48%

---


# Gerenciar pedidos e faturamento do Learning Manager

Compra com cartão de crédito só está disponível na [região dos EUA](http://learningmanager.adobe.com/).

Gerencie o faturamento do Learning Manager, faça pedidos com cartão de crédito, assine usando um Pedido de compra ou através do plano Usuários ativos mensais.

O Adobe Learning Manager possui um modelo de preços flexível e vantajoso para os clientes, considerado um dos melhores modelos para satisfazer as necessidades da sua empresa. Para mais informações, consulte a página [Learning Manager](https://www.adobe.com/products/learningmanager.html).

Somente os administradores da sua empresa podem gerenciar o faturamento.

Se quiser entrar em contato com a Adobe para obter mais informações sobre a assinatura e o faturamento do Learning Manager, escreva para [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

## A página Faturamento

Para acessar a página Faturamento, faça logon no Adobe Learning Manager como administrador e selecione **[!UICONTROL Faturamento]** no painel de navegação esquerdo.

A página Faturamento contém as seguintes guias:

| Guia | Finalidade |
|---|---|
| **Assinatura** | Exiba detalhes da conta, direitos de licença e consumo de licenças. Gerenciar ativação de plano. |
| **Histórico de pedidos** | Revisar pedidos anteriores feitos na conta. |

### Guia Assinatura

**Detalhes da conta**

O cartão **Detalhes da conta** na parte superior da guia **Assinatura** exibe quatro identificadores somente leitura para sua conta.

| Campo | Descrição |
|---|---|
| **ECCID** | número de referência da Adobe para sua conta. Faça uma citação ao entrar em contato com o suporte de Adobe. |
| **ID da conta** | O identificador exclusivo da sua conta da Adobe Learning Manager. |
| **Nome da conta** | O nome para exibição da sua conta da Adobe Learning Manager. |
| **ID da Organização IMS** | A organização do Adobe Admin Console vinculada a esta conta. Em branco, se ainda não estiver vinculado. |

**Licenças**

A seção **Licenças** lista todas as licenças ou direitos ativos na conta. Cada bloco mostra o nome da licença, uma descrição do plano, quando aplicável, e uma linha de status mostrando os valores de consumo do período do contrato atual.

As colunas da linha de estatísticas variam de acordo com o tipo de licença:

| Tipo de licença | Colunas exibidas |
|---|---|
| Licença paga (por exemplo, Adobe Learning Manager Ultimate) | Comprado/Usado/Usado por contas entre parceiros/Restante |
| Licença de avaliação (por exemplo, Virtual Coach) | Disponível/Usado/Restante |

Selecione **[!UICONTROL Exibir Detalhes de Uso]** abaixo da linha de estatísticas para expandir um detalhamento embutido. A seção expandida mostra:

- Uma lista suspensa **Selecionar período** para filtrar por período de contrato, incluindo períodos históricos
- Uma tabela **Uso Geral** com colunas: Comprado/Usado por esta Conta/Usado por Contas entre Parceiros/Restante
- Um link **Exibir divisão de conta** para ver o uso distribuído entre contas entre parceiros individuais
- Um link para **Baixar Relatório Detalhado** para exportar dados de uso como um arquivo

**Bloco de licença do Agent Orchestrator**

Quando uma licença do Agent Orchestrator é vinculada, a linha de estatísticas mostra:

| Coluna | Descrição |
|---|---|
| **Comprado** | Total de créditos Gen AI adquiridos para o período do contrato. |
| **Usado** | Créditos consumidos em todos os serviços usando esta licença. |
| **Usado pelo ALM** | Créditos consumidos especificamente pelo Adobe Learning Manager. |
| **Restante** | Créditos ainda disponíveis. |

Se a sua organização usa contas de pai e filho, a seção **Licenças** da conta de pai mostra uma coluna **Usado por contas entre parceiros** que reflete o consumo de crédito em todas as contas filho vinculadas. As contas filho exibem sua alocação como **Vagas Sancionadas** em vez de Compradas.

## Vincule sua conta da Adobe Learning Manager ao Adobe Admin Console

Para que os recursos de IA de geração possam ser ativados, sua conta da Adobe Learning Manager deve estar conectada a uma organização da Adobe Admin Console. Depois de vinculado, o Adobe Learning Manager detecta a licença do Agent Orchestrator e disponibiliza a guia **Créditos**.

A vinculação é estabelecida automaticamente quando sua conta foi comprada por meio do processo de pedido padrão do Adobe ou quando você ativou sua conta usando uma chave de ativação. Você pode verificar o link na guia **Assinatura** — se o campo **ID da organização IMS** em **Detalhes da conta** estiver preenchido, a conta já estará vinculada.

### Vincule sua conta manualmente

Se sua conta foi configurada independentemente e o campo **ID da organização IMS** está em branco, vincule manualmente.

**Pré-requisitos:**
- Você deve ser um administrador da conta da Adobe Learning Manager.
- Você deve manter a função de administrador do sistema na organização do Adobe Admin Console que deseja vincular.
- A organização do Adobe Admin Console deve ter uma licença ativa do Agent Orchestrator.

1. Selecione **[!UICONTROL Faturamento]** e selecione a guia **[!UICONTROL Assinatura]**.
2. No cartão **Detalhes da conta**, selecione **[!UICONTROL Vincular Organização IMS]**.
3. Uma janela de logon é aberta. Insira as credenciais da sua conta de Adobe e selecione sua organização na lista. A Adobe Learning Manager confirma que o logon na conta tem a função de administrador do sistema na organização do Adobe Admin Console e que a mesma conta tem a função de administrador no Adobe Learning Manager.
4. Se ambas as verificações forem aprovadas, o link será estabelecido. O campo **ID da organização IMS** é atualizado com o identificador da sua organização, e o saldo de crédito aparece na seção **Licenças**.
5. Se uma verificação falhar, uma mensagem de erro será exibida. Confirme os pré-requisitos acima e tente novamente.

### Desvincular sua conta

Após a desvinculação, os recursos do Gen AI são desabilitados para todos os alunos e a guia **Créditos** fica indisponível até que a conta seja vinculada novamente.

1. Selecione **[!UICONTROL Faturamento]** e selecione a guia **[!UICONTROL Assinatura]**.
2. No cartão **Detalhes da conta**, selecione **[!UICONTROL Desvincular Organização IMS]**.
3. Faça logon novamente para confirmar sua função de administrador na organização.
4. O link é removido. O campo **ID da Organização do IMS** retorna para branco e a guia **Créditos** está oculta.

Para restaurar o acesso, repita as etapas de vinculação manual acima.

## Fazer pedidos com cartões de crédito {#placeordersusingcreditcards}

É possível comprar uma assinatura para um máximo de 3.500 alunos através de um único pedido de pagamento com cartão de crédito. O primeiro pedido da conta deve ter no mínimo 10 alunos.

1. No aplicativo do administrador, clique em **[!UICONTROL Faturamento]** no painel de navegação esquerdo.

   ![](assets/billing.png)

   *Iniciar faturamento do Adobe Learning Manager*

1. Na página **[!UICONTROL Informações de cobrança]**, adicione o número de usuários no campo **[!UICONTROL Adicionar usuários]**. Ao usar um cartão de crédito para assinaturas pré-pagas, é possível ver o número de usuários que podem ser adicionados na assinatura. O número de usuários que podem ser adicionados não deve exceder o número mencionado na seção Restante.

   ![](assets/billing-page-to-manageyoursubscriptionandorders.png)

   *Adicionar número de usuários*

1. Depois de especificar o número de usuários que serão adicionados, clique em Fazer pedido no canto superior direito da página.

   ![](assets/billing2.png)

1. Revise a estimativa que aparece na tela.

   ![](assets/pricing-estimate.png)

   *Fazer um pedido*

   A taxa de assinatura anual é calculada com base no número de usuários adicionados na assinatura. Por exemplo, se forem adicionados quatro usuários, a taxa anual será calculada usando a expressão 4 usuários X $ 4 X $ 12, cujo resultado é $ 192.

   Clique em **[!UICONTROL Continuar]**.

   *Revise a estimativa*

1. Na página Detalhes de pagamento, você pode exibir os preços estimados do pedido. A moeda aparece com base na localidade atual.

   ![](assets/payment-details.png)

   *Exibir detalhes do pagamento*

   Você também pode alterar o local escolhendo o país na lista suspensa.

   ![](assets/change-locale.png)

   *Selecione o país de cobrança*

1. Insira as informações de contato, escolha o tipo de cartão de crédito e forneça os detalhes do cartão de crédito. Depois de inserir os detalhes necessários, clique em **[!UICONTROL Concluir Pedido]**.
1. Depois de fazer o pedido, para ver os pacotes encomendados recentemente, clique na guia **[!UICONTROL Histórico de pedidos]** na página **[!UICONTROL Faturamento]**.

   ![](assets/order-history.png)

   *Exibir histórico de pedidos*

## Verificar status do pedido {#checkorderstatus}

Todos os pedidos podem ter um dos quatro estados:

**Ativo:** há um pedido ativo e os usuários estão registrados com êxito.

**Suspenso:** um pedido passa para o estado suspenso nos seguintes cenários:

- Atraso no recebimento do pagamento do cartão de crédito.
- Expiração do cartão de crédito.
- O pagamento é recusado em qualquer ciclo de pagamento periódico.

**Cancelamento iniciado:** um pedido passa para esse estado quando o administrador do Learning Manager desativa a conta. O pedido passa para o estado cancelado depois de receber a confirmação de cancelamento do pedido.

## Atualizar detalhes da assinatura {#updatesubscriptiondetails}

1. Na lista de pedidos, clique em **[!UICONTROL Editar]**.

   ![](assets/update-subsciptiondetailsclickedit.png)

   *Atualizar detalhes da assinatura*

1. Na página Detalhes da assinatura, clique em **[!UICONTROL Editar assinatura]**.
1. Escolha o item que deseja editar:

   - Método de pagamento: use essa opção para atualizar os detalhes de pagamento, como o cartão de crédito.
   - Endereço: use essa opção para atualizar os detalhes do endereço.

## Cancelar uma assinatura {#cancelasubscription}

Para cancelar um pedido:

1. No painel esquerdo da página Administrador, clique em Faturamento.
1. Na página Faturamento, no canto superior direito, escolha **[!UICONTROL Ações]** > **[!UICONTROL Desativar conta]**.
1. Depois que o administrador desativa a conta, todos os pedidos existentes na conta são cancelados no próximo ciclo de faturamento.

Quando uma conta é desativada pelo cliente, ela entra em um estado de avaliação pelos próximos 30 dias. O proprietário da conta recebe três e-mails de lembrete para reativar a conta. Se o proprietário não reativar a conta, nenhum dos usuários poderá acessar o Learning Manager além do proprietário.

## Fazer pedidos usando o Pedido de compra {#placeordersusingpurchaseorder}

Você pode escolher o processo de pedido de compra (PO) como forma alternativa de pagamento. Como pré-requisito, a conta da sua organização deve ser registrada no Adobe. A conta da empresa é cobrada por esse processo. A conta é cobrada com base nas atividades de um aluno. São cobradas apenas as atividades no nível do objeto de aprendizado. Para fazer um pedido usando o PO:

1. Envie um e-mail para [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com) e mencione o número de alunos necessários.
1. A equipe do Learning Manager envia uma chave de ativação.
1. Na página Faturamento do aplicativo Administrador, insira a chave de ativação.
1. Clique em Ativar no canto superior direito da página.

## Verificar o status da conta {#checkaccountstatus}

Depois que uma conta é ativada, ela pode estar em qualquer um dos seguintes estados:

- **Avaliação** - Você pode criar uma conta da Adobe Learning Manager e usá-la gratuitamente por um período de 30 dias. Não há limite no número de alunos registrados durante o período de avaliação.
- **Ativo** - Neste estado, a conta tem assinaturas de aluno ativas com pagamento mensal recorrente de acordo com o pedido de assinatura.
- **Inativo** - Uma conta passa para o estado inativo nos seguintes cenários:

  - Após o período de avaliação, se não houver pedidos de assinatura ativos na conta.
  - O administrador desativa a conta, o que resulta no cancelamento de todos os pedidos existentes em uma conta a partir do próximo ciclo de faturamento da assinatura.
  - O pagamento é recusado para pedidos ativos em uma conta, mesmo após os lembretes.

Um estado inativo não cancela a conta com efeito imediato. Você recebe pelo menos alguns lembretes da equipe do Learning Manager solicitando que você forneça as informações mais recentes sobre seu cartão de crédito se ele estiver expirado. Em um estado inativo, somente um administrador pode fazer logon na conta da Adobe Learning Manager. Nenhum dos outros usuários pode acessar a conta.

- **Ativação necessária** - A conta passa para esse estado quando o administrador do Learning Manager opta por desativar a conta. Todos os pedidos dessa conta são cancelados. A cobrança do pagamento desses pedidos não é realizada no próximo ciclo de faturamento. O status da conta permanece nesse estado até o dia do último ciclo de faturamento. Nesse estado, todos os usuários podem continuar usando o aplicativo sem impacto algum até o final da última data de pagamento periódico.

## Cancelar uma assinatura {#Cancelasubscription-1}

Para cancelar uma assinatura ativa, entre em contato com a equipe de suporte do Learning Manager.

## Taxa de rescisão de conta {#accountterminationfee}

Se você quiser cancelar a assinatura antes do término do prazo anual, será cobrada uma taxa de rescisão antecipada. A taxa de rescisão equivale a 50% do preço da assinatura correspondente ao período de compromisso remanescente.

## Plano de usuários ativos mensais (MAU) {#monthlyactiveusersmauplan}

Você pode optar pelo plano MAU como forma de faturamento. Essa opção gera a cobrança de acordo com o número de usuários ativos únicos mensais. Os usuários ativos únicos mensais são adicionados cumulativamente por um período de 12 meses, a partir do mês da ativação do plano. Esse número é usado para fazer a cobrança do período.

Use o exemplo a seguir para entender como o plano MAU é calculado.

Supondo que o número de usuários por mês seja o seguinte:

- Mês 1 = 50
- Mês 2 = 500
- Mês 3 = 5.000
- Mês 4 a 12 = 10

Total de usuários ativos mensais faturados = Mês 1 + Mês 2 + Mês 3 + Mês 4 a 12 = 50 + 500 + 5.000 + 90 = 5640.

O faturamento do período seria de 5.640 usuários.

No final do período de 12 meses, a cômputo de uso é redefinido de volta a zero e um novo período do plano MAU é iniciado. Você pode adicionar várias chaves de ativação para aumentar o número de licenças adquiridas.

Qualquer usuário que executar as seguintes ações ou obter as conclusões devido às ações executadas por outro é considerado como um usuário ativo original mensal no mês em questão.

- Ao realizar um curso, programa de aprendizagem ou certificação.
- Ao realizar, baixar uma ajuda de tarefa ou anexos do curso.
- Ao realizar, baixar ou criar notas pessoais.
- Ao participar na aprendizagem social criando painéis, publicações ou comentários.
- Como obter as conclusões devido a aprovações de envio de certificado externo ou participação em uma sala de aula/sessões da sala de aula virtual.

## Exibir detalhes de uso {#viewusagedetails}

1. Para exibir o número de usuários ativos por mês, clique em **[!UICONTROL Exibir detalhes de uso]**.

   ![](assets/report-request-usage.png)

   *Exibir usuários ativos por mês*

1. Na página exibida, você pode ver o seguinte:

   - **Uso geral:** é possível verificar o número total de usuários ativos, usuários que usam o Learning Manager em um mês e o número de usuários que ainda não se inscreveram em nenhum curso.
   - **Uso mensal:** você pode ver uma tabela de usuários ativos exclusivos por mês.

## Baixar relatório de uso {#downloadusagereport}

Você também pode baixar os dados do número de usuários ativos por mês e ano. Para baixar, clique em **[!UICONTROL Baixar relatório detalhado]**.

Na caixa de diálogo **Gerar solicitação de relatório**, insira os meses e o ano necessários e clique em **[!UICONTROL Gerar]**.

![](assets/generate-report-request.png)

*Baixar relatório de uso ativo*

Se você fechar a janela do navegador, o download se iniciará da próxima vez que visitar o Learning Manager.

Os relatórios são salvos na pasta de downloads do seu navegador.

## Cancelar uma assinatura

Para cancelar uma assinatura ativa, entre em contato com a equipe de suporte do Learning Manager.

<!--
## Gen AI credits {#genaicredits}

### How Gen AI credits work

Gen AI credits are consumed each time a learner interacts with an AI-powered feature — for example, when asking a question through the AI Assistant or generating a personalized learning recommendation. Before each interaction begins, Adobe Learning Manager checks that credits are available. If credits are available, the interaction proceeds. If the balance has been exhausted, the learner sees a message that the feature is temporarily unavailable.

Credits are purchased as part of an Adobe Experience Platform Agent Orchestrator license. That license is managed in your Adobe Admin Console, and Adobe Learning Manager connects to it automatically to detect available credits.

**Credit priority rule:** If your Adobe Learning Manager plan includes bundled Gen AI credits and you also have an Agent Orchestrator license, the bundled credits are consumed first. Agent Orchestrator credits are used only after the bundled credits are exhausted.

**Shared credit pools:** If your organization has multiple Adobe Learning Manager accounts all linked to the same Adobe Admin Console organization, all accounts draw from a single shared credit pool.

>[!IMPORTANT]
>
>All Gen AI features are turned off by default. You must enable each feature and set a credit usage limit before learners can access it.

### Access the Gen AI Credits tab

1. Select **[!UICONTROL Admin]** > **[!UICONTROL Billing]**.
2. Select the **[!UICONTROL Credits]** tab.

The **Credits** tab is visible only when Gen AI credits have been purchased or were historically active on the account. If the tab is not visible, verify that your account is linked to an Adobe Admin Console organization that has an active Agent Orchestrator license.

### Gen AI Features table

The **Gen AI Features** table lists every AI feature available on the account.

| Column | Description |
|---|---|
| **Feature Name** | Name of the AI feature. Select the name to go to that feature's settings page. |
| **Status** | Whether the feature is on or off. Toggle the feature from its settings page. |
| **Max Credits Usage Limit** | Maximum credits this feature can consume during the contract period. Must be set before the feature can be enabled. Applies to learner-facing features only. |
| **Credits Used** | Total credits consumed by this feature since the contract start date, updated in real time. |

### Enable a Gen AI feature

1. On the **[!UICONTROL Credits]** tab, locate the feature in the **Gen AI Features** table.
2. In the **Max Credits Usage Limit** column, enter the maximum number of credits this feature can consume during the contract period.
3. Select the feature name to go to its **Feature Settings** page.
4. On the **Feature Settings** page, toggle the feature on.
5. Complete any additional configuration, such as assigning learners and catalogs to the AI Assistant.

### What happens when credits run out

- If a feature reaches its **Max Credits Usage Limit**, learners see a message that the feature is temporarily unavailable. Raise the limit at any time from the **Credits** tab.
- If overall account credits are exhausted, all Gen AI features stop working for learners until additional credits are purchased. Usage reports and credit metrics remain accessible to admins.
- If a learner is mid-interaction when credits are exhausted, that interaction completes. All subsequent interactions are blocked.
- Admins can set a credit limit higher than the number of purchased credits. Over-allocation is permitted, and a true-up can happen at renewal.

### Monthly Credits Usage chart

Below the Gen AI Features table, a **Monthly Credits Usage** chart shows credits consumed per feature per month. By default, the chart shows the current contract year period based on the Agent Orchestrator contract start date. Select **[!UICONTROL Download]** to export the monthly report for the selected period. Report generation is asynchronous — you receive an in-app notification and email when the file is ready.

### Gen AI usage reports

Adobe Learning Manager provides two Gen AI usage reports under **[!UICONTROL Reports]** > **[!UICONTROL AI Reports]**.

**Monthly credits usage report**

Shows credits consumed per feature per month. Useful for budget planning and contract renewal.

- **Columns:** Month | Feature | Credits Used
- **Filter:** Select a date range spanning one or more contract periods
- **Download:** Asynchronous — you receive an in-app notification and email when the file is ready

**Learner Gen AI credits usage report**

An audit trail showing which learners used which features and how many credits each interaction consumed.

- **Columns:** Date | Learner Name | Learner Email | Feature | Credits Used
- **Filter:** Select the date range you want to audit
- **Download:** Asynchronous — you receive an in-app notification and email when the file is ready

### Credit usage alerts

Adobe Learning Manager automatically notifies you when credit consumption crosses key thresholds. Notifications are delivered both in-app and by email.

| Trigger | Notification |
|---|---|
| Account credits reach 90% of total purchased | Warning — credits are nearly exhausted at the account level |
| Account credits reach 100% of total purchased | Alert — all credits are consumed and Gen AI features stop for learners |
| A feature reaches its individual Max Credits Usage Limit | Alert — names the specific feature; that feature stops for learners |

When you receive a 90% warning, contact your Adobe account team to purchase additional credits before the 100% threshold is reached.
-->

## Perguntas frequentes {#frequentlyaskedquestions}

**Como adicionar/remover assinaturas de uma conta?**

Para adicionar assinaturas em uma conta, adicione o número de usuários para quem você deseja comprar assinaturas. Em seguida, no canto superior direito, clique em **[!UICONTROL Fazer pedido]**. Revise a estimativa e clique em **[!UICONTROL Continuar]**. Insira os detalhes da conta e do cartão de crédito. Em seguida, para comprar as assinaturas, clique em **[!UICONTROL Concluir pedido]**.

Para remover uma assinatura ativa, entre em contato com a equipe de suporte do Learning Manager.


**Como alterar um cartão de crédito para assinaturas?**

Na guia **[!UICONTROL Histórico de pedidos]**, para uma conta ativa, clique em **[!UICONTROL Editar]**. Em seguida, na página Detalhes da assinatura, clique em **[!UICONTROL Editar assinatura]**. Insira os detalhes do novo cartão de crédito e clique em **[!UICONTROL Atualizar método de pagamento]**.

![](assets/credit-card-details.png)

*Exibir detalhes do cartão de crédito*


**Como atualizar as informações de faturamento no Learning Manager?**

Para atualizar as informações de faturamento, siga as etapas abaixo:

1. Faça logon como **Administrador** e clique em **[!UICONTROL Faturamento]**.
1. Na lista de pedidos, clique em **[!UICONTROL Editar]**.
1. Na página Detalhes da assinatura, clique em **[!UICONTROL Editar assinatura]**.

Escolha o item que deseja editar:

1. **[!UICONTROL Método de pagamento]:** use esta opção para atualizar os detalhes de pagamento, como o cartão de crédito.
1. **[!UICONTROL Endereço]:** use esta opção para atualizar os detalhes do endereço.


**Posso cancelar parcialmente uma assinatura?**

Não, você não pode cancelar uma assinatura parcialmente. Se precisar reduzir o número de licenças adquiridas, você pode cancelar a assinatura no final do ciclo de faturamento e, em seguida, comprar o número necessário de licenças.


**Como obter uma nota fiscal dos meus pagamentos com cartão de crédito?**

Entre em contato com a [FastSpring](https://fastspring.com/) para obter uma nota fiscal dos seus pagamentos atravès de uma das seguintes formas:

- Crie uma solicitação de serviço com a FastSpring usando o link `https://questionacharge.com`.
- Envie um email para a FastSpring em `orders@fastspring.com` solicitando a nota fiscal.


## Solução de problemas de crédito de IA de geração

| Problema | Solução |
|---|---|
| **A guia Créditos não está visível** | Créditos de IA gerais não foram comprados nem aplicados a esta conta. Verifique sua licença do Agent Orchestrator em seu Adobe Admin Console e confirme se uma organização está vinculada em **[!UICONTROL Faturamento]** > **[!UICONTROL Assinatura]** > **Detalhes da conta**. |
| **O campo ID da Organização IMS está em branco** | Sua conta ainda não está vinculada. Selecione **[!UICONTROL Vincular Organização IMS]** no cartão **Detalhes da conta** e siga as etapas de vinculação acima. |
| **Falha ao vincular com um erro** | Confirme se você tem a função de administrador no Adobe Learning Manager e na organização da Adobe Admin Console que você está tentando vincular. Ambas as verificações devem ser aprovadas para que o link seja estabelecido. |
| **O campo ID da Organização IMS fica em branco após a aplicação de uma chave de ativação** | A vinculação automática ocorre apenas para contas ativadas por meio do fluxo de ordenação padrão do Adobe. Para contas configuradas de forma independente, conclua as etapas de vinculação manual acima após ativar a tecla. |
| **Após a desvinculação, os recursos do Gen AI ficam indisponíveis** | A desvinculação remove o acesso a todos os recursos do Gen AI e oculta a guia Créditos. Vincule novamente sua conta a uma organização do Adobe Admin Console com uma licença ativa do Agent Orchestrator para restaurar o acesso. |

<!-- 
# Manage Learning Manager orders and billing

Credit card-based purchase is only available in the [US region](http://learningmanager.adobe.com/).

Manage Learning Manager billing, place orders by using a credit card, subscribe using a Purchase Order, or via a Monthly Active Users plan.

Adobe Learning Manager has a flexible, customer-friendly, and one of the best pricing models to cater to your organization needs. For more information, see the [Learning Manager](https://www.adobe.com/products/learningmanager.html) page.

Only the Administrators of your organization can manage billing.

If you want to contact Adobe for more information about Learning Manager subscription and billing, write to us at [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

## Place orders using credit cards {#placeordersusingcreditcards}

You can buy a subscription for a maximum of 3500 learners through any single credit card payment order. The first order in the account must be for a minimum of 10 learners.

1. On the Administrator app, click **[!UICONTROL Billing]** on the left navigation pane.

   ![](assets/billing.png)

   *Launch Adobe Learning Manager billing*

1. On the **[!UICONTROL Billing Information]** page, add the number of users in the **[!UICONTROL Add Users]** field. When using a credit card for pre-paid subscriptions, you can see the number of users that you can add for the subscription. The number of users you can add must not exceed the number mentioned in the section Remaining.1. 

   ![](assets/billing-page-to-manageyoursubscriptionandorders.png)

   *Add number of users*

1. After specifying the number of users to add, click Place Order in the upper-right corner of the page.

   ![](assets/billing2.png)

1. Review the estimate that appears on the screen.

   ![](assets/pricing-estimate.png)

   *Place an order*

   The annual subscription fee is calculated based on the number of users who are added for the subscription. For example, if four users are being added, the annual fee is calculated using the expression 4 usersX$4X$12, which returns $192.

   Click **[!UICONTROL Proceed]**.

   *Review the estimate*

1. On the Payment Details page, you can view the estimated price of the order. The currency appears based on the current locale.

   ![](assets/payment-details.png)

   *View payment details*

   You can also change the locale by choosing the country from the drop-down list.

   ![](assets/change-locale.png)

   *Select the country of billing*

1. Enter your contact information, choose the credit card type, and provide the details of the credit card. After you've entered the required details, click **[!UICONTROL Complete Order]**.
1. After you've placed the order, to see the recently ordered packages, click the **[!UICONTROL Order History]** tab on the **[!UICONTROL Billing]** page.

   ![](assets/order-history.png)

   *View order history*

## Check order status {#checkorderstatus}

All orders can have one of the four statuses:

**Active:** An order is active, and users are registered successfully.

**Suspended:** An order moves into suspended state in the following scenarios:

* Delay in receipt of payment from the credit card
* Expiry of the credit card.
* Payment is declined for any recurring payment cycle.

**Canceled initiated:** An order moves into this state when the Learning Manager Administrator deactivates the account. The order then moves into a canceled state after receiving the cancellation confirmation of the order.

## Update subscription details {#updatesubscriptiondetails}

1. In the list of orders, click **[!UICONTROL Edit]**.

   ![](assets/update-subsciptiondetailsclickedit.png)

   *Update subscription details*

1. In the Subscription details page, click **[!UICONTROL Edit Subscription]**.
1. Choose the item that you want to edit:

   * Payment method: Use this option to update payment details, such as, credit card.
   * Address: Use this option to update address details.

## Cancel a subscription {#cancelasubscription}

To cancel an order:

1. In the left pane of the Administrator page, click Billing.
1. In the Billing page, on the upper-right corner, choose **[!UICONTROL Actions]** > **[!UICONTROL Deactivate Account]**.
1. Once the Administrator deactivates the account, all existing orders in the account are canceled from the next billing cycle.

When an account is deactivated by the customer, it enters a trial state for the next 30 days. The account owner receives three reminder emails to revive the account. If the owner does not reactivate the account, none of the users are able to access Learning Manager apart from the owner.

## Place orders using Purchase Order {#placeordersusingpurchaseorder}

You can choose purchase order process as an alternative mode of payment. As a pre-requisite, your organization's account must be registered with Adobe. Your organization account is charged for this process. The account is charged based on a learner's activities. Only Learning Object-level activities are charged. To place an order using PO:

1. Send an email to [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com) and mention the number of required learners.
1. The Learning Manager team sends you an activation key.
1. In the Billing page of the Administrator app, enter the activation key.
1. Click Activate in the upper-right corner of the page.

## Check account status {#checkaccountstatus}

After an account gets activated, the account can be in any of the following states:

* **Trial** - You can create an Adobe Learning Manager account and use it without any payment for a period of 30 days. There is no limit on the number of learners registered during the trial period.
* **Active** - In this state, the account has active learner subscriptions with recurring monthly payment as per the subscription order.
* **Inactive** - An account moves into inactive state in the following scenarios:

  * After the trial period if there are no active subscription orders in the account.
  * Administrator deactivates the account, which results in canceling all the existing orders in an account from the next billing cycle of subscription.
  * Payment is declined for active orders in an account even after reminders.

An inactive state does not cancel your account with immediate effect. You receive at least a couple of reminders from the Learning Manager team asking you to provide the latest information about

your credit card if it has expired. In an inactive state, only an administrator can log in to the Captivate

Learning Manager account. All other users cannot access the account.

* **Activation required** - Your account moves into this state when the Learning Manager administrator chooses to deactivate the account. All the orders of this account get canceled. The collection of payment for these orders does not happen from the next billing cycle. The status of the account remains in this state until the day of the last billing cycle. In this state, all users can continue to use the application without any impact until the end of the last recurring payment date.

## Cancel a subscription {#Cancelasubscription-1}

To cancel an active subscription, contact the Learning Manager support team.

## Account termination fee {#accountterminationfee}

If you want to cancel the subscription before the completion of the annual term, an early termination fee is charged. The termination fee is equivalent to 50% of the subscription price of the remaining commitment period.

## Monthly Active Users (MAU) plan {#monthlyactiveusersmauplan}

You can choose a MAU plan as your preferred way of billing. This option generates billing based on the number of monthly unique active users. The monthly unique active users are added cumulatively for a period of 12 months starting from the month of plan activation. This number is used for billing for the period.

Use the following example to understand how MAU is calculated.

Let there be a case where the number of users per month are as follows:

* Month 1 = 50
* Month 2 = 500
* Month 3 = 5000
* Month 4 to 12 = 10

Total Monthly Active Users that are billed = Month 1 + Month 2 + Month 3 + Month 4 to 12 = 50 + 500 + 5000 + 90 = 5640.

The billing for the period would be for 5640 users.

At the end of the 12-month period, the usage count is reset back to zero and a new period for MAU plan starts. You can add multiple activation keys to increase the purchased number of seats.

Any user who performs the following actions or achieves completions due to actions taken by others is considered as a monthly unique active user for that calendar month.

* Consuming a course, learning program or certification.
* Consuming, downloading a Job Aid or course attachments.
* Consuming, downloading or creating personal notes.
* Participating in Social Learning by creating Boards, posts or comments.
* Achieving completions due to External Certificate submission approvals or attendance for a classroom/virtual classroom sessions.

## View usage details {#viewusagedetails}

1. To view the number of active users by month, click **[!UICONTROL View Usage Details]**.

   ![](assets/report-request-usage.png)

   *View active users by month*

1. On the page that displays, you can view the following:

   * **Overall usage:** You can check the total number of active users, users who are consuming Learning Manager in a month, and the number of users who have not yet signed up for any course.

   * **Monthly usage:** You can see a table of unique active users per month.

## Download usage report {#downloadusagereport}

You can also download the data of the number of active users by month and year. To download, click **[!UICONTROL Download Detailed Report]**.

On the **Generate Report Request** dialog, enter the required months and year, and click **[!UICONTROL Generate]**.

![](assets/generate-report-request.png)

*Download active usage report*

If you close the browser window, the download starts the next time you visit Learning Manager.

The reports are saved in the Downloads folder of your browser.

## Cancel a subscription

To cancel an active subscription, contact the Learning Manager support team.

## Frequently Asked Questions {#frequentlyaskedquestions}

+++How to add/remove subscriptions from an account?

To add subscriptions in an account, add the number of users for who you'd like to purchase subscriptions. Then on the upper-right corner, click **[!UICONTROL Place Order]**. Review the estimate and click **[!UICONTROL Proceed]**. Enter your account details and also your credit card details. Then to purchase the subscriptions, click **[!UICONTROL Complete Order]**.

To remove an active subscription, contact the Learning Manager support team.
+++

+++How to change a credit card for subscriptions?

In the **[!UICONTROL Order History]** tab, for an active account, click **[!UICONTROL Edit]**. Then on the Subscription Details page, click **[!UICONTROL Edit Subscription]**. Enter your new credit card details and click **[!UICONTROL Update Payment Method]**.

![](assets/credit-card-details.png)

*View credit card details*
+++

+++How to update the Billing information on Learning Manager?

To update the billing information, follow the steps below:

1. Log in as **Admin** and click **[!UICONTROL Billing]**.
1. In the list of orders, click **[!UICONTROL Edit]**.
1. In the Subscription details page, click **[!UICONTROL Edit Subscription]**.

Choose the item that you want to edit:

1. **[!UICONTROL Payment method]:** Use this option to update payment details, such as, credit card.
1. **[!UICONTROL Address]:** Use this option to update address details.
+++

+++Can I partially cancel a subscription?

No, you cannot cancel a subscription partially. If you need to reduce the number of seats that you have purchased, you can cancel the subscription at the end of the billing cycle and then purchase the number of seats required.
+++

+++How do I get an Invoice for my Credit card payments?

Contact [FastSpring](https://fastspring.com/) to get an invoice for your payments, using one of the following ways:

* Create a service request with FastSpring using the link `https://questionacharge.com`.
* Send an email to FastSpring on `orders@fastspring.com` requesting for the invoice.
-->
