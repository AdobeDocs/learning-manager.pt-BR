---
description: Este documento ajuda a configurar a autenticação SSO para fazer logon na sua conta do Learning Manager.
jcr-language: en_us
title: Fazer logon no Learning Manager usando autenticação SSO
contentowner: dvenkate
source-git-commit: a186a600e632e9a564c4ff30d1897c2cdf0d5aac
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 70%

---



# Fazer logon no Learning Manager usando autenticação SSO

Este documento ajuda a configurar a autenticação SSO para fazer logon na sua conta do Learning Manager.

Para configurar a autenticação SSO, execute as seguintes etapas:

1. Abra **[!UICONTROL Configurações]** > **[!UICONTROL Métodos de login.]**

   ![](assets/login-methods.png)

1. Escolha **[!UICONTROL Usuários internos]** ou **[!UICONTROL Usuários externos,]** dependendo de sua necessidade.
1. Clique na lista suspensa ao lado de  **[!UICONTROL fazer logon]** e selecione **[!UICONTROL Logon único]**.

   ![](assets/single-sign-on.png)

1. Para ajustar as configurações de Single Sign-On (SSO), clique em  **[!UICONTROL Alterar.]**

   ![](assets/change.png)

1. Enter  **[!UICONTROL URL de autenticação iniciada pelo IDP]** fornecido pelo provedor de serviços e faça upload do arquivo XML clicando em **[!UICONTROL Arquivo XML de Metadados do IDP.]**

   ![](assets/sso-configuration.png)

   O SSO que você configura no Learning Manager deve ser suportado por SAML 2.0.

   Você agora pode efetuar o login no Learning Manager usando sua autenticação SSO.

