---
jcr-language: en_us
title: Modelo CSS para o Editor de Rich Text
description: Modelo CSS para o Editor de Rich Text
contentowner: saghosh
preview: true
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 72%
---


# Modelo CSS para o Editor de Rich Text

## Por que a CSS é necessária?

O Rick Text é composto de marcação HTML. A renderização da marcação como está resultaria no estilo padrão aplicado pelo navegador. Isso geralmente não dá certo com as diretrizes de estilo da empresa. É necessária uma CSS para atender às diretrizes.

## Estilo padrão

A folha de estilos de CSS anexada contém o estilo aplicado pelo Learning Manager. O estilo é ajustado considerando a maioria dos casos de uso. Baixe o arquivo CSS anexado e importe-o para o seu aplicativo da Web de acordo com as suas convenções e sistema de compilação. As classes CSS definidas contêm espaços para nome na classe ql-editor e não interferem nos estilos existentes.

## Personalizar estilos

O estilo padrão pode não atender às necessidades de todos. As personalizações podem ser feitas ao substituir a CSS fornecida. Todo o estilo é delimitado sob o ql-editor como seletores descendentes. São usadas as seguintes classes:

* **Recuo**: li.ql-indents-$number. $number varia de 1 a 9
* **tamanho**: ql-size-small, ql-size-large, ql-size-huge
* **alinhamento**: ql-align-center, ql-align-reasons, ql-align-right
* **cor**: ql-color-$color. $color = branco, vermelho, laranja, amarelo, verde, azul, roxo
* **plano de fundo**: ql-bg-$color. $color = preto, vermelho, laranja, amarelo, verde, azul, roxo
* **marcas html**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Arquivo CSS a ser usado para personalização.](assets/ql-headless.css)
