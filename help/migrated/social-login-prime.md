---
jcr-language: en_us
title: Logon por rede social no Learning Manager
description: Logon por rede social no Learning Manager
contentowner: saghosh
preview: true
source-git-commit: ccdb222228f76fdae63ebb0a808824ad6ac1db7f
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---



# Logon por rede social no Learning Manager

Você pode usar suas credenciais do Facebook, LinkedIn ou do Twitter para fazer logon no Learning Manager.

## Configurar Logon Social {#setupsociallogin}

1. Entre em contato com seu gerente de sucesso do cliente se desejar que ele configure a conta.

   Caso contrário, siga as etapas abaixo.

1. Procure a conta na qual você deseja configurar o logon por rede social.
1. Altere o logon para SSO.
1. Clique em Avançado. Especifique o seguinte JSON.

   ```
   \{"linkedIn":true,"microsoft":true,"twitter":true,"facebook":true,"editingAllowed":true
   ```

   Se for um JSON incorreto, haverá uma exceção.

   Esse recurso de logon em redes sociais é usado apenas para usuários INTERNOS.

