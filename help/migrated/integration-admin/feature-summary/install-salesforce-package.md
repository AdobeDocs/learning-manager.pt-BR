---
jcr-language: en_us
title: Instalar pacote do Salesforce
description: O Gerenciador de aprendizado oferece um pacote do aplicativo Salesforce. Depois de instalados e configurados no SFDC, os funcionários de vendas podem executar suas atividades de treinamento no portal do SFDC. Este aplicativo permite que os usuários do SFDC explorem novos treinamentos, visualizem recomendações e as consumam diretamente no portal do SFDC. Os usuários também recebem os comunicados enviados pelos administradores na forma de mastros diretamente dentro do aplicativo no portal do SFDC.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: dffa765061b35d4559388e4120e51943768c8db8
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 47%

---

# Instalar pacote do Salesforce

## Visão geral

O Gerenciador de aprendizado oferece um pacote do aplicativo Salesforce. Depois de instalados e configurados no SFDC, os funcionários de vendas podem executar suas atividades de treinamento no portal do SFDC. Este aplicativo permite que os usuários do SFDC explorem novos treinamentos, visualizem recomendações e as consumam diretamente no portal do SFDC. Os usuários também recebem os comunicados enviados pelos administradores na forma de mastros diretamente dentro do aplicativo no portal do SFDC.

### Configurar no aplicativo Learning Manager

1. Faça logon na sua conta de administrador do Learning Manager como administrador de integração.
1. Clique **[!UICONTROL em Aplicativos]** > **[!UICONTROL aplicativos]** em destaque.
1. Clique **[!UICONTROL em Salesforce]**.
1. Na página do aplicativo Salesforce, observe a ID do aplicativo (também conhecida como id do cliente) e o segredo do cliente mencionados na descrição.
1. Clique **[!UICONTROL em Aprovar]** e seu aplicativo precisa ser aprovado com sucesso.
1. Clique **[!UICONTROL em Recursos]** de desenvolvedor > **[!UICONTROL Tokens de acesso para teste e desenvolvimento]**.
1. Na seção Obter código OAuth, a ID do cliente e o escopo devem ser definidos para - administrador:read,admin:write. Clique em **[!UICONTROL Enviar]**.
1. Em Obter token de atualização, insira a ID do cliente e o segredo do cliente. Clique **[!UICONTROL em Enviar]** e observe o token de atualização.

### Criar conta no aplicativo Salesforce

1. Crie uma conta na página de inscrição do Salesforce. Você deve criar uma conta do Salesforce no enterprise edition ou desenvolvedor.  [URL](https://developer.salesforce.com/signup) de assinatura do desenvolvedor. Certifique-se de usar a ID de e-mail para se inscrever no Salesforce que tinha usado para o Gerenciador de aprendizagem.
1. Verifique a sua conta por meio do e-mail de verificação.
1. Crie uma senha e faça logon no Salesforce.
1. Observe o URL do Salesforce após o logon (por exemplo, site.lightning.force.com)

### Instalar pacote do Learning Manager

Se quiser instalar o pacote, primeiro exclua o pacote existente no Salesforce. Antes de desinstalar, você deve ativar as configurações, conforme mostrado abaixo. A aplicação dessas configurações é obrigatória, caso contrário, não será possível instalar o pacote.

![](assets/uninstall-package.png)

*Instalar o pacote do Gerenciador de aprendizado*

>[!NOTE]
>
>O aplicativo Adobe Learning Manager é compatível somente com o Salesforce Lightning.

1. Inicie o URL do pacote do  [Gerenciador de aprendizado](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP).
1. Na página de **logon**, clique **[!UICONTROL em Usar domínio]** personalizado.

1. Insira o URL do pacote e clique **[!UICONTROL em Continuar]**. A página de instalação deve ter a opção Instalar apenas para administradores selecionada. Não altere essa opção.
1. Clique **em &#39;Entradas&#39;em altura**. Quando o pacote estiver instalado, clique **[!UICONTROL em Concluído]**. Você é guiado até a página Pacotes instalados e poderá ver o pacote instalado do Adobe Learning Manager.

1. Acesse o Inicializador de aplicativos (ao lado de Configuração) e procure o Adobe Learning Manager.
1. Para configurar o aplicativo, clique **[!UICONTROL em Configurar]**.
1. Clique **[!UICONTROL em Novo]** e adicione os seguintes detalhes:

   * **Config:** insira um nome de sua escolha.
   * **ClientID**: insira o valor obtido na primeira seção.
   * **ClientSecret:** insira o valor obtido na primeira seção.
   * **RefreshToken:** insira o valor obtido na primeira seção.
   * **LearningManagerBaseURL:** o URL do site onde o Gerenciador de aprendizado está hospedado.
   * **Desativar redirecionamento:** desative o redirecionamento para a página inicial do aluno no Learning Manager.

>[!NOTE]
>
>Você só pode criar uma única configuração. Se tentar adicionar outra configuração, você verá uma mensagem de erro. A configuração mapeia a conta do Salesforce com a conta do aluno.

### Adicionar configurações de site remoto

1. No canto superior direito da página, clique **[!UICONTROL em Configurar]**.
1. Em **Pesquisa** rápida, pesquise por Configurações de site remoto.
1. Clique **[!UICONTROL em Novo site]** remoto.
1. Insira os detalhes:

   1. **Nome do site remoto:** insira um nome de sua escolha.
   1. **URL do site remoto:** o URL do site onde o Learning Manager está hospedado.

1. Inicie o Learning Manager.

### Adicionar o domínio da Adobe às URLs confiáveis do Salesforce

Para adicionar o domínio da Adobe a URLs confiáveis, siga estas etapas:

1. No console do Salesforce, vá para **[!UICONTROL Configuração]** > **[!UICONTROL Quick Find]**.
1. Pesquise por **[!UICONTROL URLs confiáveis]** e selecione **[!UICONTROL Novo URL]** confiável.
1. Digite um nome no campo Nome ]**da**[!UICONTROL  API.
1. Adicione o URL como `{}.adobe.com{*}`
1. Selecione todas as caixas de seleção nas **Diretivas** de CSP e salve as alterações.
1. Edite o token de atualização do aplicativo Salesforce e salve-o.
1. Reinicie o aplicativo Salesforce.

### Ativar notificações para o aplicativo Learning Manager

1. No canto superior direito, clique **em Configurar**.
1. Procure Notificações personalizadas.
1. Clique **[!UICONTROL em Novo]**.
1. Insira os seguintes detalhes:

   1. **Nome de notificação personalizada:** LearningManagerNotification
   1. **Nome da API:** LearningManagerNotification

1. **Selecione desktop** e **dispositivos móveis** como canais compatíveis.

1. Clique em **[!UICONTROL Salvar]**.
1. Para ativar as notificações push para dispositivos móveis, siga as etapas abaixo:

   1. Instale o aplicativo Salesforce para dispositivos móveis em seu celular.
   1. Faça logon no aplicativo usando suas credenciais.
   1. Vá para **Configuração** > **Configurações** de entrega de notificação.
   1. Adicione o Salesforce para iOS e Android.

### Desinstalar o Learning Manager do Salesforce

1. No aplicativo Salesforce, vá para Pacotes instalados.
1. Clique **[!UICONTROL em Desinstalar]**.

## Configurar o Learning Manager para usuários do Salesforce

O aplicativo Learning Manager também está disponível para usuários que estão presentes em qualquer conta do Salesforce. O administrador do Salesforce pode adicionar usuários com base nos perfis. Os perfis do Salesforce são semelhantes aos perfis no Learning Manager. Por exemplo, administrador, administrador de integração, professor e assim por diante. O administrador do Salesforce também pode criar um perfil personalizado.

### Perfil

Como administrador do Salesforce, você pode atribuir os perfis aos usuários ou criar um perfil personalizado.

>[!NOTE]
>
>Os usuários devem estar presentes no Salesforce e no Learning Manager.

![](assets/create-profile.png)

*Atribuir um perfil a um aluno*

Ao adicionar um aluno, você deve atribuir um perfil específico ao aluno. Em seguida, vá até esse perfil e conceda o acesso necessário.

Para que os alunos visualizem o aplicativo do Gerenciador de aprendizagem, você deve ativar o aplicativo para todos os alunos.

A próxima etapa é conceder permissão para acessar o aplicativo Learning Manager.

![](assets/permission-set.png)

*Adicionar permissões para acessar o aplicativo do Gerenciador de aprendizagem*

Quando você instala o pacote, um novo conjunto de permissões é criado, **Usuário do Gerenciador** de Aprendizagem da Adobe. Vá para o conjunto de permissões e adicione os usuários.

Selecione os usuários e atribua as permissões adequadamente. Os alunos agora podem acessar o aplicativo Learning Manager.

Agora, selecione um perfil, por exemplo, Perfil padrão de um usuário e clique no perfil. Clique **[!UICONTROL em Editar]** e, na **seção Configurações** de aplicativo personalizado, ative a caixa de seleção **do Adobe Learning Manager**. Isso torna o aplicativo acessível ao usuário.

Na seção **Configurações da guia personalizada**, na lista suspensa **Página inicial do aluno**, selecione a opção **[!UICONTROL Padrão ativado]**.

Você deve tornar o aplicativo visível para todos os perfis.

Clique **[!UICONTROL em Salvar]** e os alunos que pertencem a todos os perfis acessarão o aplicativo do Gerenciador de aprendizagem.
