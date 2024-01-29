---
jcr-language: en_us
title: Instalar pacote do Salesforce
description: O Learning Manager oferece um pacote do aplicativo Salesforce. Depois de instalados e configurados no SFDC, os funcionários de vendas podem executar suas atividades de treinamento no portal do SFDC. Este aplicativo permite que os usuários do SFDC explorem novos treinamentos, visualizem recomendações e as consumam diretamente no portal do SFDC. Os usuários também recebem os comunicados enviados pelos administradores na forma de cabeçalhos diretamente no aplicativo no portal do SFDC.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---



# Instalar pacote do Salesforce

## Visão geral

O Learning Manager oferece um pacote do aplicativo Salesforce. Depois de instalados e configurados no SFDC, os funcionários de vendas podem executar suas atividades de treinamento no portal do SFDC. Este aplicativo permite que os usuários do SFDC explorem novos treinamentos, visualizem recomendações e as consumam diretamente no portal do SFDC. Os usuários também recebem os comunicados enviados pelos administradores na forma de cabeçalhos diretamente no aplicativo no portal do SFDC.

### Configurar no aplicativo Learning Manager

1. Faça logon na sua conta de administrador do Learning Manager como administrador de integração.
1. Clique em **[!UICONTROL Aplicativos]** > **[!UICONTROL Aplicativos em destaque]**.
1. Clique em **[!UICONTROL Salesforce]**.
1. Na página do aplicativo Salesforce, observe a ID do aplicativo (também conhecida como ID do cliente) e o segredo do cliente mencionado na descrição.
1. Clique em **[!UICONTROL Aprovar]** e seu aplicativo deve ser aprovado com sucesso.
1. Clique em **[!UICONTROL Recursos do desenvolvedor]** > **[!UICONTROL Tokens de acesso para teste e desenvolvimento]**.
1. Na seção Obter código OAuth, a ID do cliente e o escopo devem ser definidos como - admin:read,admin:write. Clique em **[!UICONTROL Enviar]**.
1. Em Obter token de atualização, insira a ID do cliente e o segredo do cliente. Clique em **[!UICONTROL Enviar]** e anote o token de atualização.

### Criar conta no aplicativo Salesforce

1. Crie uma conta na página de inscrição do Salesforce. Você deve criar uma conta do Salesforce na edição para desenvolvedores ou corporativa.  [URL de inscrição do desenvolvedor](https://developer.salesforce.com/signup). Certifique-se de usar a ID de e-mail para se inscrever no Salesforce que você usou para o Learning Manager.
1. Verifique sua conta por meio do e-mail de verificação.
1. Crie uma senha e faça logon no Salesforce.
1. Anote o URL do Salesforce após o logon (por exemplo, site.lightning.force.com)

### Instalar pacote do Learning Manager

Se quiser instalar o pacote, primeiro exclua o pacote existente no Salesforce. Antes de desinstalar, você deve ativar as configurações, conforme mostrado abaixo. A aplicação dessas configurações é obrigatória, caso contrário, não será possível instalar o pacote.

![](assets/uninstall-package.png)

*Instalar o pacote do Learning Manager*

>[!NOTE]
>
>O aplicativo Adobe Learning Manager só é compatível com a exibição Lightning do Salesforce.

1. Inicie o  [URL do pacote do Learning Manager](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftest.salesforce.com%2Fpackaging%2FinstallPackage.apexp%3Fp0%3D04t1k0000008YWn&amp;data=04%7C01%7Ckillamse%40adobe.com%7Cf588f553fc694d2edee108d9a5c74711%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C637723097572585825%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=mhYKVdwvS4F7WPruy0Kvw%2FsqgWxzTQpaZJyEACu8CNw%3D&amp;reserved=0).
1. No menu **Logon** , clique em **[!UICONTROL Usar domínio personalizado]**.

1. Insira o URL do pacote e clique em **[!UICONTROL Continuar]**. A página de instalação deve ter a opção Instalar somente para administradores selecionada. Não altere essa opção.
1. Clique em **Insalto**. Depois que o pacote for instalado, clique em **[!UICONTROL Concluído]**. Você é guiado até a página Pacotes instalados e poderá ver o pacote instalado do Adobe Learning Manager.

1. Acesse o Inicializador de aplicativos (ao lado de Configuração) e procure o Adobe Learning Manager.
1. Para configurar o aplicativo, clique em **[!UICONTROL Configurar]**.
1. Clique em **[!UICONTROL Novo]** e adicione os seguintes detalhes:

   * **Configuração:** Insira um nome de sua escolha.
   * **ClientID**: insira o valor obtido na primeira seção.
   * **ClientSecret:** Insira o valor obtido na primeira seção.
   * **RefreshToken:** Insira o valor obtido na primeira seção.
   * **URL de base do LearningManager:** O URL do site onde o Learning Manager está hospedado.
   * **Desativar redirecionamento:** Desative o redirecionamento para a página inicial do aluno no Learning Manager.

>[!NOTE]
>
>Você só pode criar uma configuração única. Se tentar adicionar outra configuração, você verá uma mensagem de erro. A configuração mapeia a conta do Salesforce com a conta do aluno.

### Adicionar configurações de site remoto

1. No canto superior direito da página, clique em **[!UICONTROL Configuração]**.
1. Entrada **Localização Rápida**, procure Configurações de site remoto.
1. Clique em **[!UICONTROL Novo site remoto]**.
1. Insira os detalhes:

   1. **Nome do site remoto:** Insira um nome de sua escolha.
   1. **URL do site remoto:** O URL do site onde o Learning Manager está hospedado.

1. Inicie o Learning Manager.

### Ativar notificações para o aplicativo Learning Manager

1. No canto superior direito, clique em **Configuração**.
1. Procure Notificações personalizadas.
1. Clique em **[!UICONTROL Novo]**.
1. Insira os seguintes detalhes:

   1. **Nome da notificação personalizada:** NotificaçãoDoLearningManager
   1. **Nome da API:** NotificaçãoDoLearningManager

1. Selecionar ambos **Desktop** e **Celular** como Canais compatíveis.

1. Clique em **[!UICONTROL Salvar]**.
1. Para ativar as notificações push para dispositivos móveis, siga as etapas abaixo:

   1. Instale o aplicativo Salesforce para dispositivos móveis em seu celular.
   1. Faça logon no aplicativo usando suas credenciais.
   1. Ir para **Configuração** > **Configurações de Entrega de Notificação**.
   1. Adicione o Salesforce para iOS e Android.

### Desinstalar o Learning Manager do Salesforce

1. No aplicativo Salesforce, acesse Pacotes instalados.
1. Clique em **[!UICONTROL Desinstalar]**.

## Configurar o Learning Manager para usuários do Salesforce

O aplicativo Learning Manager também está disponível para usuários que estão presentes em qualquer conta do Salesforce. O administrador do Salesforce pode adicionar usuários com base nos perfis. Os perfis do Salesforce são semelhantes aos perfis no Learning Manager. Por exemplo, administrador, administrador de integração, professor e assim por diante. O administrador do Salesforce também pode criar um perfil personalizado.

### Perfil

Como administrador do Salesforce, você pode atribuir os perfis aos usuários ou criar um perfil personalizado.

>[!NOTE]
>
>Os usuários devem estar presentes no Salesforce e no Learning Manager.

![](assets/create-profile.png)

*Atribuir um perfil a um aluno*

Ao adicionar um aluno, você deve atribuir um perfil específico ao aluno. Em seguida, acesse esse perfil e conceda o acesso necessário.

Para que os alunos vejam o aplicativo Learning Manager, você deve ativar o aplicativo para todos os alunos.

A próxima etapa é conceder permissão para acessar o aplicativo Learning Manager.

![](assets/permission-set.png)

*Adicionar permissões para acessar o aplicativo Learning Manager*

Quando você instala o pacote, um novo conjunto de permissões é criado, **Usuário do Adobe Learning Manager**. Vá para o conjunto de permissões e adicione os usuários.

Selecione os usuários e atribua as permissões adequadamente. Os alunos agora podem acessar o aplicativo Learning Manager.

Agora, selecione um perfil, por exemplo, Perfil padrão de um usuário e clique no perfil. Clique em **[!UICONTROL Editar]** e no **Configurações do aplicativo personalizado** , ative a caixa de seleção **Adobe Learning Manager**. Isso torna o aplicativo acessível ao usuário.

No menu **Configurações da guia personalizada** , na seção **Página inicial do aluno** , selecione a opção **[!UICONTROL Padrão Ativado]**.

Você deve tornar o aplicativo visível para todos os perfis.

Clique em **[!UICONTROL Salvar]** e os alunos pertencentes a todos os perfis acessarão o aplicativo Learning Manager.
