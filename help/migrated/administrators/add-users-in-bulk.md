---
jcr-language: en_us
title: Adicionar usuários em massa
description: Saiba como adicionar vários usuários de uma vez.
contentowner: saghosh
exl-id: c3309ce5-8764-452e-82d5-5637c23c661b
source-git-commit: f964dd3f1adeadb76f4843c9af229ce5f09afde1
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 22%

---

# Adicionar usuários em massa

Neste treinamento, você aprenderá como adicionar usuários em massa por meio de um CSV.

[![botão](feature-summary/assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=51TC8QS1&amp;mv=display&amp;mv2=display#/course/7555555)

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

## Como adicionar vários usuários

Você pode adicionar vários usuários de uma vez seguindo as etapas abaixo:

1. Clique em **[!UICONTROL Usuários]** no painel esquerdo de logon do administrador e em **[!UICONTROL Adicionar]** > **[!UICONTROL Carregar um csv]**. Uma caixa de diálogo pop-up é exibida.

1. Você pode adicionar vários usuários usando um arquivo .CSV. Clique em **[!UICONTROL Importar]** e selecione/abra o arquivo .csv no computador.

1. Após importar o arquivo, mapeie o conteúdo do arquivo .csv com os rótulos do aplicativo ao fazer upload do arquivo .csv pela primeira vez.

   Para todos os uploads subsequentes, as configurações anteriores para rótulos são consideradas. Clique em **[!UICONTROL Salvar]** após concluir o mapeamento de dados e clique em **[!UICONTROL Adicionar]** para carregar o arquivo .csv mapeado.

1. Clique em **[!UICONTROL Salvar]** após concluir o mapeamento de dados e clique em **[!UICONTROL Adicionar]** para carregar o arquivo .csv mapeado.

## Upload de CSV com campos obrigatórios {#csvuploadwithmandatoryfields}

Não é obrigatório adicionar o perfil do usuário e a ID de e-mail do gerente no CSV. O nome de usuário e a ID de e-mail do usuário são os únicos campos obrigatórios.

Nesse caso, por padrão, o administrador da sua empresa é tratado como o gerente dos usuários. Por padrão, o funcionário é considerado como o perfil do usuário.

>[!NOTE]
>
>Para adicionar novos usuários, crie um novo arquivo CSV com seus detalhes e faça upload. Não é possível atualizar e reenviar um arquivo CSV existente.

**CSV de exemplo**

O CSV de amostra do Learning Manager está disponível abaixo com campos obrigatórios.
[Amostra-CSV-nome-email.zip](assets/sample-csv-name-email.zip)

## Upload de CSV com todos os campos {#csvuploadwithallthefields}

Antes de incluir a ID de e-mail do gerente para qualquer funcionário, verifique se o gerente foi adicionado primeiro como um funcionário no CSV. Por exemplo, consulte o nome do funcionário Howard Walters na captura de tela abaixo:

![](assets/csv-example.png)

*Modelo CSV para carregamento*

Além disso, os administradores de uma organização podem adicionar a si mesmos como funcionários e mencionar a ID de e-mail do gerente como raiz.

**CSV de exemplo**

O CSV de amostra do Learning Manager está disponível abaixo com todos os campos.
[learning-manager-sample-csv.zip](assets/learning-manager-sample-csv.zip).

Consulte o conteúdo de ajuda do recurso [Usando carregamento de CSV](/help/migrated/administrators/feature-summary/add-users-user-groups.md) para obter mais informações.
