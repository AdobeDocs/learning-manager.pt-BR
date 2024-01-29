---
jcr-language: en_us
title: Os links de e-mail acionados a partir de modelos modificados geram um erro no Learning Manager
description: Os links de e-mail acionados a partir de modelos modificados geram um erro no Adobe Learning Manager
contentowner: nluke
preview: true
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---



# Os links de e-mail acionados a partir de modelos modificados geram um erro no Learning Manager

## Problema

Ocorre um erro depois de clicar em um link para um e-mail/e-mail de boas-vindas/e-mail de inscrição automatizado.

**Erro**

Status do HTTP 400 - Solicitação incorreta

![](assets/email-404.png)

## Causa

Isso geralmente acontece quando os modelos de e-mail são personalizados incorretamente.

**Solução**

Para evitar erros relacionados a links quebrados, que podem aparecer devido à personalização, siga as etapas abaixo:

1. Faça logon como administrador.
1. No painel esquerdo, clique em **[!UICONTROL Modelos de e-mail]**.

1. Navegue até o modelo necessário e clique para modificá-lo.

   Isso abre a janela **Visualização do modelo** janela.

   ![](assets/email-template.png)

   Observe os pontos ao editar um modelo de e-mail:

   * Recomendamos que você modifique um modelo de e-mail na interface do Learning Manager.
   * Copie e cole o modelo modificado em um arquivo do Bloco de Notas/Word para armazenar uma cópia das alterações feitas.
   * Evite substituir qualquer texto dinâmico no modelo destacado em azul. Por exemplo, &quot;**OrganizationName**“, &quot;**Aluno**“, &quot;**clique aqui**“, &quot;**CertificateName**&quot; e assim por diante.

1. Clique em **[!UICONTROL Salvar]** para confirmar as alterações aplicadas ao modelo.
1. Acione o e-mail para verificar se os links funcionam conforme o esperado.
1. Reverta as configurações para o original clicando na opção **Reverter para original** para o modelo modificado.
