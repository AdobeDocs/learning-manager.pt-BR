---
jcr-language: en_us
title: O usuário é excluído automaticamente no Learning Manager
description: Um usuário é excluído do Learning Manager, no entanto, o administrador nunca executou tal ação.
contentowner: nluke
exl-id: 9e293da3-bcbf-4798-b391-aef53ef8d946
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 61%

---

# O usuário é excluído automaticamente no Learning Manager {#user-gets-auto-deleted-in-learning-manager}

## Problema

Um usuário é excluído do Learning Manager, no entanto, o administrador nunca executou tal ação.

## Causa

No Adobe Learning Manager, há uma opção que permite excluir um usuário se ele não tiver feito logon no sistema por um certo tempo.

## Como alterar/aplicar a configuração?

### Para alunos internos

1. Faça logon como **Administrador**.
1. Em **Configurar**, clique em **Configurações** > **Geral**.
1. Na página Configurações gerais, consulte a opção **Excluir automaticamente usuários internos**.
1. Clique em **[!UICONTROL Editar]** para inserir o número de dias no campo e excluir automaticamente um aluno caso ele não tenha acessado o sistema.

   ![](assets/cp-autodelete-internal.png)

   *Editar o número de dias*

>[!NOTE]
>
>   Deixe o campo em branco caso não queira excluir usuários automaticamente.


1. Clique em **[!UICONTROL Salvar]** para manter as configurações feitas.

### Para alunos externos:

1. Faça logon como **Administrador**.
1. Em **Gerenciar**, clique em **[!UICONTROL Usuários]** > **[!UICONTROL Externos]**.
1. Clique no nome de um usuário externo para o qual a configuração precisa ser aplicada.

   Isso abre a janela **Editar perfil de registro externo**.

1. Clique em **[!UICONTROL Configurações Avançadas]** no canto inferior esquerdo.

   ![](assets/cp-autodelete-external.png)

   *Selecione a opção Configurações Avançadas*

1. No campo **Requisito de logon**, insira o número de dias para excluir automaticamente um aluno caso ele não tenha acessado o sistema.
1. Clique em **[!UICONTROL Salvar]** para manter as configurações feitas.
