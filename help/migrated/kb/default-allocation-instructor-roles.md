---
jcr-language: en_us
title: Alocação padrão de funções de professor para grupos de usuários no Learning Manager
description: Alocação padrão de funções de professor para grupos de usuários no Learning Manager
contentowner: nluke
preview: true
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 48%

---



# Alocação padrão de funções de professor para grupos de usuários no Learning Manager

## Problema

Todos os usuários alocados a uma sessão recebem a função de professor.

## Descrição

Há cenários em que uma sessão pode exigir vários professores ou um administrador/autor atribui um grupo de usuários a uma sessão. Isso resulta na atribuição da função de professor a todos os usuários no grupo de usuários.

## Causa

Como as funções não podem ser ramificadas durante a atribuição em massa de usuários em um grupo de usuários, a função de professor é atribuída a todos os usuários.

## Solução

Crie grupos de usuários personalizados para filtrar as funções de usuário atribuídas a uma sessão. Para remover as funções de professor atribuídas em um grupo de usuários, execute as seguintes etapas:

1. Faça logon como administrador. No painel esquerdo, clique em **[!UICONTROL Modelos de e-mail]**.
1. Para evitar acionadores de e-mail para as alterações a serem feitas, clique em **[!UICONTROL Desativar tudo]**.

   ![](assets/instructor-disable-all.png)

1. Navegue até **Usuários** > **Grupo de usuários**. Clique em **[!UICONTROL Adicionar]**.

   ![](assets/instructor-usergroups.png)

1. Crie um grupo de usuários personalizado na janela Adicionar grupo de usuários da seguinte maneira:

   * Insira um nome para o grupo personalizado na caixa **[!UICONTROL Nome]** campo.
   * Em **[!UICONTROL Incluir alunos]** adicione o grupo de usuários para o qual deseja filtrar os professores.
   * Em **[!UICONTROL Excluir alunos]** adicione os usuários para os quais deseja manter a função de professor.

   ![](assets/instructor-add-ug.png)

   As etapas acima criam uma lista de usuários a serem adicionados ao conjunto de inclusão e removem usuários específicos (professores) mencionados no conjunto de exclusão.

1. Clique em **[!UICONTROL Salvar]** as alterações feitas.
1. Procure o grupo de usuários personalizado criado acessando **[!UICONTROL Usuários]** > **[!UICONTROL Interno]**.

   ![](assets/instructor-custom-ug.png)

1. Clique na caixa de seleção para selecionar todos os usuários no grupo.

   ![](assets/instructor-bulk-ug.png)

1. Clique em **[!UICONTROL Ações]** > **[!UICONTROL Remover Função]** > **[!UICONTROL Remover professor]**.

Certifique-se de que todos os acionadores de e-mail que foram desativados na etapa 2 sejam reativados depois de concluído.
