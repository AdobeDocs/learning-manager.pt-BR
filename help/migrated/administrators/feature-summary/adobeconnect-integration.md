---
jcr-language: en_us
title: Integração do Adobe Connect
description: Os autores podem criar cursos em sala de aula virtual com o Adobe Connect durante o processo de criação do curso. Para ativar o Adobe Connect na sua conta do Learning Manager, você precisa entrar em contato com o administrador da sua organização.
contentowner: jayakarr
exl-id: 13458f93-9ea7-4aab-8b33-3c4f4dd5886d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 70%

---

# Integração do Adobe Connect

Os administradores de uma empresa podem definir as configurações da conta do Learning Manager para habilitar a integração do Adobe Connect.

## Configurar o Adobe Connect {#configureadobeconnect}

1. No logon do administrador, clique em **[!UICONTROL Configurações]** no painel esquerdo para exibir as informações básicas sobre sua empresa. Clique em **[!UICONTROL Adobe Connect]** no painel esquerdo.

   ![](assets/left-pane.png)

   *Selecione o Adobe Connect no painel esquerdo*

1. Clique no link **[!UICONTROL Configurar Agora]** na seção **[!UICONTROL Configuração do Adobe Connect]**.

   <!--![](assets/configure-now-connect.png)-->

1. Forneça o nome de domínio do Adobe Connect da sua empresa e as credenciais de logon.

   ![](assets/adobeconnect-config.png)

   *Adicionar nome de domínio e credenciais*

   Um exemplo de URL do Adobe Connect: mycompany.adobeconnect.com\
   Você precisa fornecer a ID de e-mail do administrador da conta do Adobe Connect.

   Somente contas do Connect hospedadas pela Adobe são compatíveis com o Learning Manager. Exemplo; &#39;.adobeconnect.com&#39;.

1. Clique em **[!UICONTROL Integrar].**

   Após autenticar a ID de e-mail, o Learning Manager exibe a mensagem enquanto o Connect é integrado com êxito. Você pode começar a visualizar seus cursos em sala de aula virtual usando o Adobe Connect automaticamente.

   O administrador da conta do Adobe Connect deve aceitar os Termos e condições de uso do Adobe Connect. Se não for aceito, a autenticação do logon pode falhar. Após criar a conta do Adobe Connect, faça logon na conta uma vez. Durante o primeiro logon, uma página de termos e condições é exibida.

   <!--![](assets/mail-confirmation.png)-->

## Adicionar informações da sessão da sala de aula virtual {#addvirtualclassroomsessioninformation}

Se o autor de um curso em sala de aula virtual não tiver fornecido as informações da sessão, o administrador poderá incluir os detalhes da sessão.

No logon do administrador, clique no nome do curso de sala de aula virtual. Clique em **[!UICONTROL Instâncias]** no painel esquerdo e clique em **[!UICONTROL Detalhes da Sessão]**.  Clique no ícone Editar no canto direito da página Detalhes da sessão para adicionar as informações da sessão.

![](assets/session-creation-admin.png)

*Adicionar informações de sessão de sala de aula virtual*

Com a integração do Adobe Learning Manager e Adobe Connect para a criação de módulos ou sessões de sala de aula virtual, sua conta do Connect deve ser compatível com salas de reunião com número adequado de salas e usuários simultâneos para o seu caso de uso. Essas salas de reunião são usadas para hospedar os módulos de sala de aula virtual do Learning Manager. Uma nova sala de reunião do Connect é criada dinamicamente pelo Learning Manager para cada módulo ou sessão de sala de aula virtual no Learning Manager.

Você deve adquirir o Adobe Connect separadamente, além do Adobe Learning Manager.

## Presença dos alunos {#learnersattendance}

Se o host do curso de sala de aula virtual não comparecer à sessão, a participação não será registrada automaticamente para os alunos que participaram da sessão. Nesses cenários, o administrador pode registrar a participação manualmente.

Clique no curso de sala de aula virtual, clique em Participação no painel esquerdo da página seguinte e registre a participação.
