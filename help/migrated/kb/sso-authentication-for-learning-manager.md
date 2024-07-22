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
1. Clique na lista suspensa ao lado da opção **[!UICONTROL logon]** e selecione **[!UICONTROL Logon único]**.

   ![](assets/single-sign-on.png)

1. Para ajustar as configurações de logon único (SSO), clique em **[!UICONTROL Alterar.]**

   ![](assets/change.png)

1. Insira a **[!UICONTROL URL de Autenticação iniciada por IDP]** fornecida pelo provedor de serviços e carregue o arquivo XML clicando em **[!UICONTROL Arquivo XML de Metadados IDP.]**

   ![](assets/sso-configuration.png)

   O SSO que você configura no Learning Manager deve ser suportado por SAML 2.0.

   Você agora pode efetuar o login no Learning Manager usando sua autenticação SSO.

