---
jcr-language: en_us
title: Adicionar usuários em massa
description: Saiba como adicionar vários usuários de uma vez.
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 31%

---



# Adicionar usuários em massa

Sim, você pode adicionar vários usuários de uma vez seguindo as etapas abaixo:

1. Clique em **[!UICONTROL Usuários]** no painel esquerdo de login do administrador e, em seguida, clique em **[!UICONTROL Adicionar]** > **[!UICONTROL Fazer upload de um csv]**. Uma caixa de diálogo pop-up é exibida.

1. Você pode adicionar vários usuários usando um arquivo .CSV. Clique em **[!UICONTROL Importar]** e selecione/abra o arquivo .csv no computador.

1. Após importar o arquivo, mapeie o conteúdo do arquivo .csv com os rótulos do aplicativo ao fazer upload do arquivo .csv pela primeira vez.

   Para todos os uploads subsequentes, as configurações anteriores para rótulos são consideradas. Clique em **[!UICONTROL Salvar]** depois de concluir o mapeamento de dados e clique em **[!UICONTROL Adicionar]** para carregar o arquivo .csv mapeado.

1. Clique em **[!UICONTROL Salvar]** depois de concluir o mapeamento de dados e clique em **[!UICONTROL Adicionar]** para carregar o arquivo .csv mapeado.

## Upload de CSV com campos obrigatórios {#csvuploadwithmandatoryfields}

Não é obrigatório adicionar o perfil do usuário e a ID de e-mail do gerente no CSV. O nome de usuário e a ID de e-mail do usuário são os únicos campos obrigatórios.

Nesse caso, por padrão, o administrador da sua empresa é tratado como o gerente dos usuários. Por padrão, o funcionário é considerado como o perfil do usuário.

**CSV de amostra**

O CSV de amostra do Learning Manager está disponível abaixo com campos obrigatórios.
[Sample-CSV-name-email.zip](assets/sample-csv-name-email.zip)

## Upload de CSV com todos os campos {#csvuploadwithallthefields}

Antes de incluir a ID de e-mail do gerente para qualquer funcionário, verifique se o gerente foi adicionado primeiro como um funcionário no CSV. Por exemplo, consulte o nome do funcionário Howard Walters na captura de tela abaixo:

![](assets/csv-example.png)

*Modelo CSV para upload*

Além disso, os administradores de uma organização podem adicionar a si mesmos como funcionários e mencionar a ID de e-mail do gerente como raiz.

**CSV de amostra**

O CSV de amostra do Learning Manager está disponível abaixo com todos os campos.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Consulte  [Usar o upload de CSV](/help/migrated/administrators/feature-summary/add-users-user-groups.md) conteúdo de ajuda do recurso para obter mais informações.
