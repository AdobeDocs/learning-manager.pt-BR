---
jcr-language: en_us
title: Não é possível exibir o calendário
description: Quando um administrador tenta editar a data de expiração de um perfil de inscrição externo e clica no calendário para editar a data de expiração, o calendário não é exibido.
contentowner: saghosh
exl-id: 1b7e5594-714a-4a1d-9b8f-d481c1b48cb5
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 95%
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

## Solução

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
