---
jcr-language: en_us
title: Notificações
description: O recurso Notificações é aplicável a todos os usuários do Adobe Learning Manager. Mas cada usuário com base em sua função recebe diferentes tipos de notificações em vários cenários.
contentowner: manochan
source-git-commit: 147e9edfe323f3d0851880cd401067daa1cee84f
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---



# Notificações

O recurso Notificações é aplicável a todos os usuários do Adobe Learning Manager. Mas cada usuário com base em sua função recebe diferentes tipos de notificações em vários cenários. Todos os alertas e notificações aos usuários são exibidos por meio da caixa de diálogo pop-up de notificações.

## Acessar notificações {#accessnotifications}

Os usuários podem ver as notificações clicando no ícone de notificações no canto superior direito da janela. Esta caixa de diálogo suspensa exibe os destaques de todas as notificações junto com a hora da ocorrência e uma barra de rolagem. Para exibir mais informações sobre todas as notificações, clique em Mostrar todas as notificações na parte inferior da caixa de diálogo pop-up. A página Notificações é exibida.

É possível saber o número de notificações mais recentes com base no número destacado acima do ícone de notificações. Por exemplo, se houver cinco notificações mais recentes após seu logon anterior, você poderá ver o número 5 exibido sobre o ícone de notificações. Esses números desaparecem assim que você lê todas as notificações mais recentes.

## Tipos de notificações para administradores {#typesofnotificationsforadministrators}

Os administradores recebem notificações nas seguintes instâncias:

* Sempre que uma lista csv de usuários é carregada com êxito.
* Sempre que o upload de uma lista csv de usuários não for bem-sucedido. O administrador recebe uma mensagem com o motivo da falha.
* O administrador também pode configurar alertas de notificação em nível de instância para cursos e programas de aprendizado. Nesse caso, o administrador recebe as notificações com base na frequência selecionada no nível da instância.

>[!NOTE]
>
>Se um administrador tiver privilégios de autor ou gerente além de sua função, ele receberá notificações referentes a cada função.

Uma janela de notificação de amostra da função de administrador é mostrada na seguinte captura de tela:

![](assets/admin-notification.png)

*Exibir notificações de administrador*

Essa janela pop-up exibe realces de todas as notificações junto com a hora da ocorrência e uma barra de rolagem. Você pode saber o número de notificações mais recentes com base no número destacado acima do ícone de notificações. Por exemplo, se houver cinco notificações mais recentes após seu logon anterior, você poderá ver o número 5 exibido sobre o ícone de notificações. Esses números desaparecem assim que você lê todas as notificações mais recentes.

Clique em **[!UICONTROL Mostrar todas as notificações]** na parte inferior da janela pop-up de notificações para exibir todas as notificações em uma página separada.

## Configurar notificações de escalonamento de vários níveis {#setupmultilevelescalationnotifications}

Os e-mails de escalonamento, quando os alunos não cumprirem os prazos, podem ser enviados para o gerente e para um gerente ignorado. Você pode configurar notificações de escalonamento de vários níveis para a não conclusão do curso durante o processo de criação de um curso ou mesmo depois de ele ter sido criado. As notificações de escalonamento podem ser configuradas para serem enviadas com uma frequência definida para serem enviadas a um gerente ou um gerente ignorado.

1. Faça logon como administrador ou autor e clique em Cursos.
1. Selecione o curso para o qual deseja modificar as notificações de escalonamento e clique em **[!UICONTROL Exibir curso]**.

   ![](assets/view-courses.png)

   *Selecione a opção Exibir curso*

1. Clique em **[!UICONTROL Instâncias]** > **[!UICONTROL Alertas de Notificação]**.

   ![](assets/notification-alert.png)

   *Selecione a opção Alertas de notificação*

1. Um calendário é aberto indicando o prazo definido para o curso destacado em vermelho. Clique na data destacada para ver os lembretes definidos para o aluno.

   ![](assets/deadline-calender.png)

   *Exibir lembretes de prazo*

1. Defina lembretes selecionando datas anteriores ao prazo. Isso permite configurar lembretes para o aluno sobre o prazo que se aproxima.

   ![](assets/deadline-reminder.png)

   *Definir uma data de lembrete de prazo*

1. Selecione uma data após o prazo para configurar um cronograma de lembretes para as notificações do aluno e de escalonamento para o gerente.

   ![](assets/set-reminders-andescalation.png)

   *Definir lembretes e datas de escalonamento*

1. Se o aluno ainda não conseguir concluir o curso mesmo após o escalonamento para o gerente, as configurações permitem que você transfira para o gerente ignorado do aluno. Clique em uma data após o prazo estendido, selecione a recorrência de lembretes, o número de dias para o agendamento e selecione **Gerente e Ignorar Gerente de Nível** na caixa **Escalonamento** menu suspenso. Clique na marca de seleção azul para salvar as configurações de notificação.

   ![](assets/reminder-to-managerandskipmanager.png)

   *Salvar as configurações de notificação*

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como configurar notificações de lembrete na instância?

Em uma instância, clique em Alertas de notificação. Um calendário é aberto indicando o prazo definido para o curso destacado em vermelho. Clique na data destacada para ver os lembretes definidos para o aluno. Defina os lembretes, conforme explicado neste [seção](user-notifications.md#Setupmultilevelescalationnotifications).
+++
