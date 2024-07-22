---
jcr-language: en_us
title: Não é possível exibir o calendário
description: Quando um administrador tenta editar a data de expiração de um perfil de inscrição externo e clica no calendário para editar a data de expiração, o calendário não é exibido.
contentowner: saghosh
exl-id: 1b7e5594-714a-4a1d-9b8f-d481c1b48cb5
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
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

1. Clique em **[!UICONTROL Iniciar]** > **[!UICONTROL Configurações]** > **[!UICONTROL Sistema]**.
1. Clique em **[!UICONTROL Exibir]**.
1. Na seção **[!UICONTROL Escala e layout]**, use a lista suspensa. Altere as configurações para 100%.

   ![](assets/scale-layout.png)

   *Alterar configurações de Exibição*

1. Reinicie o computador.
