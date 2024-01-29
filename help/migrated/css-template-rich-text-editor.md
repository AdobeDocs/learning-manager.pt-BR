---
jcr-language: en_us
title: Modelo CSS para o Editor de Rich Text
description: Modelo CSS para o Editor de Rich Text
contentowner: saghosh
preview: true
source-git-commit: 9325abb9cda8c8a019c9d72c1944a8284f38f83e
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---



# Modelo CSS para o Editor de Rich Text

## Por que a CSS é necessária?

O rich text é composto de marcação HTML. A renderização da marcação como está resultaria no estilo padrão aplicado pelo navegador. Isso geralmente não dá certo com as diretrizes de estilo da empresa. Uma CSS é necessária para atender às diretrizes.

## Estilo padrão

A folha de estilos de CSS anexada contém o estilo aplicado pelo Learning Manager. O estilo é ajustado considerando a maioria dos casos de uso. Baixe o arquivo CSS anexado e importe-o para o seu aplicativo da Web de acordo com as suas convenções e sistema de compilação. As classes CSS definidas contêm espaços para nome na classe ql-editor e não interferem nos estilos existentes.

## Personalizar estilos

O estilo padrão pode não atender às necessidades de todos. As personalizações podem ser feitas ao substituir a CSS fornecida. Todo o estilo é delimitado sob o ql-editor como seletores descendentes. São usadas as seguintes classes:

* **Recuo**: li.ql-indents-$number. $number varia de 1 a 9
* **tamanho**: ql-size-small, ql-size-large, ql-size-huge
* **alinhamento**: ql-align-center, ql-align-reasons, ql-align-right
* **cor**: ql-color-$color. $color = branco, vermelho, laranja, amarelo, verde, azul, roxo
* **fundo**: ql-bg-$color. $color = preto, vermelho, laranja, amarelo, verde, azul, roxo
* **tags html**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Arquivo CSS a ser usado para personalização.](assets/ql-headless.css)
