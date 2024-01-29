---
jcr-language: en_us
title: Integração do Okta Ative Diretory com o Adobe Learning Manager
description: Integração do Okta Ative Diretory com o Adobe Learning Manager
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---



# Integração do Okta Ative Diretory com o Adobe Learning Manager {#okta-active-directory-integration-with-adobe-learning-manager}

Neste documento, você aprenderá como integrar o Adobe Learning Manager com o Okta Ative Diretory (AD). Ao integrar o Adobe Learning Manager com o Okta AD, você pode:

* Verifique e controle o acesso do usuário do Learning Manager no Okta AD.
* Permita que os usuários façam logon automaticamente no Adobe Learning Manager com suas contas do Okta AD.
* Gerencie suas contas em um local central: o portal do Okta.

O Adobe Learning Manager oferece suporte ao provedor de identidade (IdP) e ao provedor de serviços (SP) iniciado SSO.

## Criar um aplicativo no OKTA

1. Faça logon como administrador no Okta AD.
1. Clique em **[!UICONTROL Aplicativos]**. Isso abre a App Store no Okta.

   ![](assets/cp-application-store.png)

   *Exibir loja de aplicativos na Okta*

1. Clique em **[!UICONTROL Criar integração de aplicativos]**.

   ![](assets/cp-app-integrations.png)

   *Selecione Criar integração de aplicativos*

1. Selecionar **[!UICONTROL SAML 2.0]** na janela de integração do novo aplicativo.

   ![](assets/cp-saml2.0.png)

   *Selecione a opção SAML2.0*

1. Selecionar **[!UICONTROL Criar integração SAML]** > **[!UICONTROL Página Configurações gerais]**. Insira um Nome de Aplicativo.

   Observe que esse pode ser qualquer nome para identificar exclusivamente o seu aplicativo. Uma vez concluído, clique em **[!UICONTROL Próxima]**.

   ![](assets/cp-saml-integration.png)

   *Insira o nome do aplicativo*

1. Execute as seguintes etapas na página Configurar definições do SAML:

   **Para configuração de IDP:**

   1. No campo do URL de logon único, digite o URL: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. No campo do URL do público-alvo, digite o URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. No menu **Formato de ID de Nome** , selecione **Endereço de e-mail**.
   1. No menu **Nome de usuário do aplicativo** , selecione o nome de usuário do Okta.
   1. Caso queira passar atributos adicionais, você pode adicionar os atributos na seção **Instrução de Atributos** (Opcional)

   ![](assets/cp-saml-integration-step1.png)

   *Adicionar atributos SAML*

   **Para configuração de SP:**

   1. No campo do URL de logon único, digite o URL: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. No campo do URL do público-alvo, digite o URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. Na caixa suspensa Name ID Format, selecione **Endereço de e-mail**.
   1. Na lista suspensa Nome de usuário no aplicativo, selecione o nome de usuário do Okta.
   1. Clique em **Mostrar configurações avançadas**.
   1. Em **Algoritmo de assinatura**, selecione RSA-SHA256
   1. No menu **Algoritmo de asserção**, selecione SHA256
   1. No menu **Criptografia de asserção** dropbox, selecione **Criptografado**.

   1. No menu **Certificado de Criptografia** , carregue o arquivo de certificado compartilhado pelo Adobe.
   1. Caso queira passar atributos adicionais, você pode adicionar os atributos na seção **Instrução de Atributos** (Opcional).

   ![](assets/cp-saml-integration-step2.png)

   *Adicionar atributos adicionais*

   Uma vez concluído, clique em **[!UICONTROL Próxima]**.

1. O **Feedback**  é opcional. Depois de selecionar as opções e receber seu feedback, clique em **[!UICONTROL Concluir]**.

   ![](assets/cp-saml-integration-step3.png)

   *Concluir configuração do SAML*

## Extrair URL iniciado pelo IDP e arquivos de metadados

Para exibir o URL iniciado pelo IdP/SP e o arquivo de metadados, execute as seguintes etapas:

1. Abra o aplicativo criado.
1. Sob a **Logon único** clique em **[!UICONTROL Exibir instruções]**.

   ![](assets/cp-prime-sso.png)

   *Selecionar guia SSO*

   **Para IDP:**

   1. O URL de logon único do provedor de identidade é o URL iniciado pelo IdP.
   1. Copie todo o texto que está presente na **Opcional** campo.
   1. Abra um novo documento do bloco de notas e cole o texto copiado.
   1. Clique em **[!UICONTROL Arquivo]** > **[!UICONTROL Salvar como]** > “filename.xml”. Esse será o arquivo de metadados.

   **Para SP:**

   1. O URL de logon único do provedor de identidade é o URL iniciado pelo IdP.
   1. O emissor do provedor de identidade é a ID da entidade.
   1. Copie todo o texto que está presente na **Opcional** campo.
   1. Abra um novo documento do bloco de notas e cole o texto copiado.
   1. Clique em **[!UICONTROL Arquivo]** > **[!UICONTROL Salvar como]** > **[!UICONTROL filename.xml]**. Esse será o arquivo de metadados.

   ![](assets/cp-saml-integration-step4.png)

   *Salvar arquivo XML da controladora de armazenamento*

   Você precisa salvar este arquivo em um formato XML.

## Configurando o SSO do Adobe Learning Manager

Para configurar o logon único do Adobe Learning Manager, execute as etapas mencionadas no artigo abaixo.

<!--

article not in TOC

[SSO Authentication](/help/migrated/kb/sso-authentication-for-learning-manager.md)
-->