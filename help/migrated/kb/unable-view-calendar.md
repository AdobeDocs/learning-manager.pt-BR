---
jcr-language: en_us
title: Não é possível exibir o calendário
description: Quando um administrador tenta editar a data de expiração de um perfil de inscrição externo e clica no calendário para editar a data de expiração, o calendário não é exibido.
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 88%

---



# Não é possível exibir o calendário

## Problema

Não é possível exibir o calendário ao editar a data de expiração de um perfil externo.

## Descrição

Quando um administrador tenta editar a data de expiração de um perfil de inscrição externo e clica no calendário para editar a data de expiração, o calendário não é exibido.

## Causa

O problema ocorre devido ao seguinte:

* O nível de zoom do navegador é superior a 100%.
* A escala e o layout nas configurações de exibição são mais de 100%.

## Resolução

### Navegador

1. Inicie o navegador.
1. Faça logon no Adobe Learning Manager.
1. Na barra de endereços, clique no ícone de zoom.
1. Clique em **[!UICONTROL Redefinir]**.
1. Altere a data de expiração do perfil de inscrição.

### Configurações de exibição

1. Clique em **[!UICONTROL Início]** > **[!UICONTROL Configurações]** > **[!UICONTROL Sistema]**.
1. Clique em **[!UICONTROL Exibir]**.
1. Na seção **[!UICONTROL Escala e layout]**, use a lista suspensa. Altere as configurações para 100%.

   ![](assets/scale-layout.png)

   *Alterar configurações de exibição*

1. Reinicie o computador.
