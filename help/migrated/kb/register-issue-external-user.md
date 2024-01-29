---
jcr-language: en_us
title: Não é possível registrar-se como Usuário externo
description: Os alunos externos não podem se registrar em um perfil no Adobe Learning Manager.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---



# Não é possível registrar-se como Usuário externo

## Problema

Os alunos externos não podem se registrar em um perfil.

## Erro

A ID de e-mail já está registrada. Use um email diferente.

![](assets/cp-register-profile.png)

*Mensagem de erro de um email já registrado*

## Descrição

Há cenários em que um usuário não pode se registrar em um perfil externo. O usuário recebe o erro acima ao se inscrever.

## Causa

Esse problema ocorre em um dos seguintes cenários:

* O usuário já está registrado em outro perfil externo.
* O usuário já é um aluno interno.
* O usuário está em um estado excluído.

## Resolução:

**Cenário 1:** O usuário já está registrado em outro perfil externo.

1. Faça logon como administrador.
1. Em **Gerenciar**, clique em **[!UICONTROL Usuários]** > **[!UICONTROL Externo]**.
1. Abra o Perfil do qual o usuário já faz parte clicando em Vagas utilizadas

   ![](assets/cp-seats-used.png)

   *Abrir perfil do usuário*

1. Selecione o usuário, clique em **[!UICONTROL Ações]** > **[!UICONTROL Alterar perfil]**.

   ![](assets/cp-change-profile.png)

   *Alterar perfil do usuário*

   Isso abre uma janela para selecionar um novo perfil como abaixo.

   ![](assets/cp-select-profiles.png)

   *Selecionar perfil de usuário*

1. Depois de selecionado, clique em **[!UICONTROL Alterar]**.

**Cenário 2:** O usuário está presente como aluno interno.

1. Faça logon como administrador.
1. Em **Gerenciar**, clique em **[!UICONTROL Usuários]** > **[!UICONTROL Interno]**.
1. Clique para abrir um perfil do aluno e clique no ícone Editar.

   ![](assets/cp-internal-learner.png)

   *Abrir um perfil interno do aluno*

1. Altere o endereço de e-mail do aluno ou adicione *_old* para o endereço de email existente. Isso liberará o endereço de email.

   Por exemplo, se o endereço de e-mail do aluno for *<abc@adobe.com>,* altere-o para *<abc_old@adobe.com>*

1. Clique em **Salvar** para manter as alterações feitas.

**Cenário 3**: o usuário está em um estado excluído.

1. Faça logon como administrador.
1. Em **Gerenciar**, clique em **[!UICONTROL Usuários]** > **[!UICONTROL Limpeza do Usuário]**.
1. Selecione o aluno e clique no ícone Editar.

   ![](assets/cp-deleted-learner.png)

   *Editar endereço de email do usuário*

1. Altere o endereço de e-mail do aluno ou adicione *_old* para o endereço de email existente. Isso liberará o endereço de email.

   Por exemplo, se o endereço de e-mail do aluno for **<abc@adobe.com>**, altere-o para **<abc_old@adobe.com>**.
