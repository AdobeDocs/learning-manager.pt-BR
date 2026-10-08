---
description: Saiba como os administradores do Learning Manager ativam o Virtual Coach, monitoram o uso do crédito MAU e baixam relatórios de desempenho do aluno
jcr-language: en_us
title: Gerenciar uso e faturamento de Virtual Coach
exl-id: 1f8f6465-51c3-4670-a1c7-9a7dfb091452
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%
---

# Gerenciar uso e faturamento de Virtual Coach

Ative o Virtual Coach, monitore o consumo de crédito do MAU (Monthly Ative User, usuário ativo mensal) e baixe relatórios de desempenho do aluno como administrador do Adobe Learning Manager.

## Ative o Virtual Coach para sua conta {#activatevirtualcoach}

O Virtual Coach está disponível como um complemento do Adobe Learning Manager. Após a compra, o provisionamento gera uma chave de ativação que é enviada por email ao administrador da conta.

1. Faça logon no Adobe Learning Manager como administrador.
2. Navegue até a página **Faturamento** no painel de navegação esquerdo.
3. Na seção **Treinador virtual**, insira a chave de ativação recebida por email.

   ![](/help/migrated/administrators/feature-summary/assets/virtual_coach12.png)
   *Insira a chave de ativação na seção Treinador Virtual da página Faturamento para ativar o recurso.*

4. Selecione **Aplicar**. O Virtual Coach está habilitado para sua conta.

Depois de ativado, você recebe uma notificação no aplicativo confirmando que o recurso está ativo. Quatro exemplos de cenários de interpretação de funções são adicionados automaticamente à **Biblioteca de conteúdo** para que os autores possam começar imediatamente.

>[!NOTE]
>
>A chave de ativação é gerada automaticamente durante o provisionamento e compartilhada por e-mail. Se você não tiver a chave de ativação, entre em contato com o Gerente de sucesso do cliente da Adobe Learning Manager.

## Exibir saldo de crédito MAU

Créditos do Usuário Ativo Mensal (MAU) contam o número de alunos exclusivos que usam o Treinador Virtual a cada mês.

1. Navegue até a página **Faturamento**.
2. Na seção **Treinador virtual**, selecione **Exibir detalhes de uso**.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach22.png)

3. Use o menu suspenso **Selecionar período** para escolher o intervalo de datas que deseja revisar.

   A tabela **Uso Geral** mostra:

   - **Disponível**: total de créditos MAU comprados.
   - **Usados**: créditos consumidos até a data.
   - **Restante**: créditos disponíveis para o restante do período do contrato.

   A tabela **Uso Mensal** mostra o número de alunos ativos exclusivos por mês do calendário.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach23.png)

4. Selecione **Baixar Relatório Detalhado** para exportar os dados de uso completo.

   ![](/help/migrated/administrators/feature-summary/assets/virtual-coach-report-mau-billing-5.png)

## Como os créditos MAU são consumidos

Um crédito MAU é consumido quando um aluno inicia uma sessão de orientação virtual em um mês do calendário. As sessões adicionais do mesmo aluno no mesmo mês não consomem créditos adicionais. Os créditos não utilizados no final do período do contrato vencem e não são acumulados.

| Cenário | MAUs consumidos |
|---|---|
| Um aluno conclui 5 sessões em janeiro | 1 |
| O mesmo aluno usa o Virtual Coach em janeiro e fevereiro | 2 (1 por mês) |
| 100 alunos concluíram cada uma 1 sessão em janeiro | 100 |

*Os créditos do MAU são contados por aluno único por mês do calendário, independentemente de quantas sessões cada aluno inicia.*

**Exemplo: aluno único, várias sessões.** Sarah lança cinco sessões de Virtual Coach em janeiro. Ela conta como um único usuário único para o mês, então 1 MAU é consumido independentemente de quantas vezes ela pratica.

**Exemplo: mesmo aluno, vários meses.** Sarah usa Virtual Coach em janeiro (3 sessões) e fevereiro (2 sessões). Cada mês do calendário conta separadamente, portanto, 2 MAUs são consumidos — 1 para janeiro e 1 para fevereiro.

**Exemplo: vários alunos, mesmo mês.** 100 representantes de vendas lançam uma sessão de orientação virtual em janeiro. Cada aluno único conta como um MAU para esse mês, portanto, 100 MAUs são consumidos.

**Exemplo: prática em equipe ao longo do tempo.** Sua equipe de 50 pessoas usa o Virtual Coach durante todo o ano. Num mês em que apenas cinco dos 50 treinos, cinco MAUs são consumidos nesse mês; num mês em que todos os 50 treinos novamente, 0 MAUs adicionais vão além do que já foi consumido para devolver os alunos nesse mês, uma vez que cada aluno é contado apenas uma vez por mês do calendário, independentemente do número de vezes que pratica dentro dele.

Para saber mais sobre os relatórios de Instrução Virtual, navegue até [Relatórios de Instrução Virtual](/help/migrated/administrators/feature-summary/virtual-coach/virtual-coach-reports.md).
