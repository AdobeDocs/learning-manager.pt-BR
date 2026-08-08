---
description: Uma referência completa para cada propriedade no esquema JSON do tema do Compositor de conteúdo — incluindo tokens de paleta, pilhas de fontes, tokens de raio e espaçamento, valores de função de texto, propriedades de componente e estilo de avaliação.
jcr-language: en_us
title: Referência de propriedade JSON do tema do Adobe Learning Manager Content Composer
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '1899'
ht-degree: 5%

---


# Referência de propriedade JSON do tema do Adobe Learning Manager Content Composer

Uma referência completa para cada propriedade em um arquivo JSON de tema do Compositor de conteúdo, com descrições e valores de exemplo.

Campos de nível superior que identificam e descrevem o tema.

## **Metadados**

| **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|--------------|----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| id de catálogo padrão | cadeia de caracteres | Identificador de tema exclusivo. Minúsculas, somente hifens, sem espaços ou caracteres especiais. Usado internamente para referenciar o tema. | “ardósia” |
| nome | cadeia de caracteres | Nome de exibição mostrado no painel Temas do curso. | “Ardósia” |
| version | cadeia de caracteres | Número da versão semântica. Use “1.0.0” para novos temas. | &quot;1.0.0&quot; |
| descrição | cadeia de caracteres | Breve descrição do caráter visual do tema. | “Um tema caloroso e confiável com fundo creme, detalhes Adobe vermelho e o sistema tipográfico Roboto Slab + Roboto” |
| autor | cadeia de caracteres | Nome do criador ou da equipe do tema. | “Compositor de conteúdo” |
| source | cadeia de caracteres | Origem do tema. “enviados” para temas incorporados. “personalizado” para temas criados pelo usuário. | “personalizado” |
| isDefault | booleano | Se este tema é aplicado automaticamente a novos cursos. Definido como falso na maioria dos casos. | falso |

## **foundation.palette**

Os sete tokens de cor principais que formam a base de cores do tema. Todos os valores de elemento fazem referência a esses tokens usando var(—tokenName) em vez de valores hexadecimais codificados.

| **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|------------------|------------|---------------------------------------------------------------------------------------------------------------------------|-----------------|
| primeiro plano | cor hexadecimal | Cor principal do primeiro plano para texto, ícones e elementos da interface colocados no plano de fundo. | #1A1A1A |
| fundo | cor hexadecimal | Tela de pintura do curso principal e cor de fundo do slide. | #FAF7F2 |
| acento | cor hexadecimal | Cor de ênfase da marca aplicada a botões, estados selecionados, indicadores de progresso, cabeçalhos de lição e destaques interativos. | #E8001C |
| backgroundSubtle | cor hexadecimal | Cor de fundo secundária para cartões, painéis, navegação e preenchimentos de componentes. | #F0EBE1 |
| secundário | cor hexadecimal | Cor da borda, do divisor e do elemento de interface do usuário inativo. | #D9D3C9 |
| textPrimary | cor hexadecimal | Cor do texto principal de todo o conteúdo do título e do corpo. | #1A1A1A |
| textInverse | cor hexadecimal | Cor do texto para conteúdo colocado em planos de fundo escuros ou coloridos de ênfase, como rótulos de botões na cor de ênfase. | #FFFFFF |

## **foundation.fonts**

Duas pilhas de fontes aplicadas a todas as funções de texto no tema. Fazer referência em valores de elemento usando var(—font-heading) ou var(—font-body).

| **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|--------------|-------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| título | string de pilha de fontes | Família de fontes para títulos de lição, títulos de tópico e títulos de exibição. Inclua fallbacks seguros para a Web. | “Roboto Slab, Geórgia, &#39;Times New Roman&#39;, serifa” |
| body | string de pilha de fontes | Família de fontes para texto de parágrafo, legendas, perguntas do quiz e rótulos de interface. Inclua fallbacks seguros para a Web. | “Roboto, -apple-system, BlinkMacSystemFont, &#39;Segoe UI&#39;, sans-serif” |

## **fundação.espaçamento**

Tokens de espaçamento horizontal e vertical usados como linha de base. Os componentes são dimensionados a partir destes usando os multiplicadores horizontalSpacingScale e verticalSpacingScale.

| **Caminho** | **Tipo** | **Descrição** | **Valor do Tablet** |
|---------------|----------|-------------------------------------|-----------------|
| horizontal.xs | valor px | Menor unidade de espaçamento horizontal | 4px |
| horizontal.s | valor px | Pequena unidade de espaçamento horizontal | 8px |
| horizontal.m | valor px | Unidade de espaçamento horizontal média | 12px |
| horizontal.l | valor px | Grande unidade de espaçamento horizontal | 16px |
| horizontal.xl | valor px | Unidade de espaçamento horizontal extragrande | 24px |
| vertical.xs | valor px | Menor unidade de espaçamento vertical | 4px |
| vertical.s | valor px | Unidade pequena de espaçamento vertical | 8px |
| vertical.m | valor px | Unidade de espaçamento vertical médio | 16px |
| vertical.l | valor px | Unidade grande de espaçamento vertical | 24px |
| vertical.xl | valor px | Unidade de espaçamento vertical extragrande | 32px |

## **fundação.raio**

Tokens de raio de borda que controlam o arredondamento de canto de componentes e placas.

| **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|--------------|----------|---------------------------------------------------------|-----------------|
| nenhum | valor px | Sem arredondamento - cantos acentuados. Sempre “0px”. | 0px |
| s | valor px | Raio pequeno para arredondamento sutil do canto. | 4px |
| m | valor px | Raio médio da placa padrão e do arredondamento de componentes. | 8px |
| l | valor px | Raio grande para arredondamento proeminente. | 16px |
| completo | valor px | Forma completa de pílula ou círculo. Sempre “9999px”. | 9999px |

## **foundation.logo**

| **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|--------------|----------------|----------------------------------------------------------------------------------------------|-----------------|
| logotipo | cadeia de caracteres ou nulo | URL ou caminho do arquivo para a imagem do logotipo exibida no cabeçalho do curso. Defina como nulo para nenhum logotipo. | null |

## **elements.text**

Propriedades de tipografia para cada função de texto nomeada no curso. Todas as funções compartilham o mesmo conjunto de propriedades.

### **Funções de texto**

| **Função** | **Aplicado a** |
|--------------|------------------------------------------------------------------------------|
| títuloDalição | Título principal em um slide de abertura de lição |
| topicTitle | Título na parte superior de cada slide de tópico |
| blockHeading | Títulos dentro de componentes de conteúdo, como cabeçalhos acordeão e títulos de cartão |
| subtítulo | Títulos secundários em um slide de tópico |
| pergunta | Texto de pergunta do quiz e da verificação de conhecimento |
| legenda | Legendas abaixo de imagens e blocos de mídia |
| parágrafo | Corpo de texto em slides de conteúdo |
| buttonLabel | Texto dos botões e elementos de Call-to-action |

### **Propriedades de texto compartilhadas**

As propriedades a seguir aplicam-se a todas as funções de texto listadas acima.

| **Propriedade** | **Tipo** | **Valores aceitos** | **Descrição** |
|--------------------|-----------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| fontFamily | Variável de CSS ou pilha de fontes | var(—font-heading), var(—font-body) ou uma string de pilha de fontes completa | Família de fontes para esta função de texto. |
| fontSize | valor px | Qualquer valor de pixel | Tamanho da fonte. |
| fontWeight | cadeia de caracteres | Somente “bold” ou “normal” - valores numéricos não são suportados | Peso da fonte. |
| fontStyle | cadeia de caracteres | “normal” ou “itálico” | Estilo da fonte. |
| cor | Variável ou hexadecimal do CSS | Qualquer token de paleta via var(—tokenName) ou um valor hexadecimal direto | Cor do texto. |
| textAlign | cadeia de caracteres | “left”, “center” ou “right” | Alinhamento horizontal do texto. |
| letterSpacing | cadeia de caracteres | “normal”, um valor px ou um valor em | Espaço entre caracteres. |
| lineHeight | cadeia de caracteres | Um valor percentual ou unitário | Height de linha. |
| textDecoration | cadeia de caracteres | “none”, “underline” ou “line-through” | Decoração de texto. |
| textTransform | cadeia de caracteres | “none”, “uppercase”, “lowercase” ou “capitalize” | Transformação de caixa de texto. |
| paddingInlineStart | valor px | Qualquer valor de pixel | Preenchimento esquerdo aplicado ao bloco de texto. |
| paragraphSpacing | valor px | Qualquer valor de pixel | Espaço adicionado abaixo de cada parágrafo no bloco de texto. |

### **Valores de função de texto - Tema do Tablet**

| **Função** | **fontFamily** | **fontSize** | **fontWeight** | **fontStyle** | **cor** | **textAlign** | **espaçamentoEntreLetras** | **AlturaDaLinha** | **textTransform** |
|--------------|---------------------|--------------|----------------|---------------|--------------------|---------------|-------------------|----------------|-------------------|
| títuloDalição | var(—font-heading) | 48px | negrito | normal | var(—textPrimary) | centro | -0,01em | 130% | nenhum |
| topicTitle | var(—font-heading) | 40px | normal | normal | var(—textPrimary) | lado | 0 | 135% | nenhum |
| blockHeading | var(—font-heading) | 24px | negrito | normal | var(—textPrimary) | lado | 0 | 140% | nenhum |
| subtítulo | var(—font-body) | 20px | negrito | normal | var(—textPrimary) | lado | 0,01em | 150% | nenhum |
| pergunta | var(—font-heading) | 24px | normal | normal | var(—textPrimary) | lado | 0 | 150% | nenhum |
| legenda | var(—font-body) | 13px | normal | normal | var(—textPrimary) | lado | 0,02em | 170% | nenhum |
| parágrafo | var(—font-body) | 16px | normal | normal | var(—textPrimary) | lado | 0,01em | 190% | nenhum |
| buttonLabel | var(—font-body) | 14px | negrito | normal | var(—textInverse) | centro | 0,06em | 125% | maiúscula |

## **elementos - superfícies estruturais**

Propriedades que controlam o plano de fundo e a borda das superfícies de layout fixo do curso.

| **Elemento** | **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|--------------|--------------|-------------------|---------------------------------------------------|----------------------------|
| tela | fundo | CSS var | Cor de fundo da tela de pintura do curso principal | var(—background) |
| cabeçalho | fundo | CSS var | Cor de fundo da barra de cabeçalho do curso | var(—background) |
| cabeçalho | borda | Cadeia de caracteres de borda CSS | Borda inferior da barra de cabeçalho do curso | var(—secondary) sólido de 1 px |
| rodapé | fundo | CSS var | Cor de fundo da barra do rodapé do curso | var(—background) |
| rodapé | borda | Cadeia de caracteres de borda CSS | Borda superior da barra de rodapé do curso | var(—secondary) sólido de 1 px |
| cabeçalhoLição | fundo | CSS var | Cor de fundo da área de cabeçalho do título do tutorial | var(—accent) |
| tópico | fundo | CSS var | Cor de fundo de cada slide do tópico | var(—background) |
| tópico | borda | Cadeia de caracteres de borda CSS | Borda ao redor do contêiner do slide de tópico | var(—secondary) sólido de 1 px |
| navegação | fundo | CSS var | Cor de fundo do painel de navegação de lição | var(—backgroundSubtle) |
| navegação | borda | Cadeia de caracteres de borda CSS | Borda no painel de navegação de lição | var(—secondary) sólido de 1 px |
| botão | fundo | CSS var | Cor de fundo dos botões de ação principal | var(—accent) |
| paginação | fundo | CSS var | Cor de fundo do controle de paginação | var(—backgroundSubtle) |

## **elementos - propriedades de componente compartilhado**

Essas propriedades aparecem em todos os componentes do bloco de conteúdo: paragraphBlock, videoBlock, imageGrid, acordeão, carrossel, flipCard e linha do tempo.

| **Propriedade** | **Tipo** | **Descrição** |
|------------------------|-------------------|---------------------------------------------------------------------------------------------------|
| fundo | Variável ou cor do CSS | Plano de fundo externo do bloco de componentes. Normalmente “transparente”. |
| cardBackgroundColor | Variável ou cor do CSS | Preenchimento em segundo plano de cartões individuais dentro do componente. |
| cardBorder | Cadeia de caracteres de borda CSS | Borda aplicada a cada cartão. Abreviação completa de CSS, por exemplo “1px solid var(—secondary)”. |
| cardShadowOffset | cadeia de caracteres | Deslocamento X e Y da sombra projetada da placa, por exemplo “0px 2px 6px”. |
| cardShadowColor | Variável ou cor do CSS | Cor da sombra projetada do cartão. |
| cardShadowOpacity | sequência de porcentagem | Opacidade da sombra projetada do cartão. Defina como “0%” para remover a sombra. |
| horizontalSpacingScale | sequência numérica | Multiplicador aplicado a tokens de espaçamento horizontal para este componente. “1” usa o espaçamento padrão. |
| escalaDeEspaçamentoVertical | sequência numérica | Multiplicador aplicado a tokens de espaçamento vertical para este componente. “1” usa o espaçamento padrão. |
| radiusScale | sequência numérica | Multiplicador aplicado aos tokens de raio deste componente. “1” usa o raio padrão. |
| nestedAccentColor | Variável ou cor do CSS | Cor de destaque para elementos aninhados dentro do componente. Aplica-se somente a paragraphBlock. |

### **Valores de componente compartilhados - Tema do Tablet**

| **Componente** | **cardBackgroundColor** | **bordaDoCartão** | **cardShadowOpacity** |
|----------------|-----------------------------|----------------------------|---------------------------|
| paragraphBlock | var(—backgroundSubtle) | var(—secondary) sólido de 1 px | 8% |
| videoBlock | var(—backgroundSubtle) | var(—secondary) sólido de 1 px | 8% |
| imageGrid | var(—backgroundSubtle) | var(—accent) sólido de 1 px | 8% |
| acordeão | var(—backgroundSubtle) | var(—secondary) sólido de 1 px | 8% |
| carrossel | var(—backgroundSubtle) | var(—secondary) sólido de 1 px | 8% |
| flipCard | var(—backgroundSubtle) | var(—secondary) sólido de 1 px | 8% |
| linha do tempo | var(—backgroundSubtle) | var(—secondary) sólido de 1 px | 8% |

## **elementos - propriedades específicas do componente**

Propriedades exclusivas dos tipos de componentes individuais.

| **Componente** | **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|----------------|--------------------------|----------|------------------------------------------------------------------|-------------------------|
| paragraphBlock | nestedAccentColor | CSS var | Cor de destaque para elementos aninhados no bloco de parágrafo | var(—accent) |
| flipCard | cardFrontBackgroundColor | CSS var | Cor de fundo da face frontal da carta de inversão | var(—backgroundSubtle) |
| flipCard | cardBackBackgroundColor | CSS var | Cor de fundo da face traseira da placa - a cor de revelação | var(—accent) |
| flipCard | arrowColor | CSS var | Cor do ícone da seta do indicador de giro | var(—textInverse) |
| tabulações | ativeBg | CSS var | Cor do plano de fundo da aba atualmente selecionada | var(—accent) |
| tabulações | inativeBg | CSS var | Cor do plano de fundo das abas não selecionadas | var(—backgroundSubtle) |
| tabulações | containerBg | CSS var | Cor de fundo do contêiner da barra de abas | var(—backgroundSubtle) |
| linha do tempo | trackColor | CSS var | Cor da linha de conexão entre os nós da linha do tempo | var(—secondary) |
| linha do tempo | progressCompletedBg | CSS var | Cor de preenchimento dos marcadores de progresso da linha do tempo concluída | var(—accent) |
| linha do tempo | progressCurrentBorder | CSS var | Cor da borda do marcador de progresso da linha do tempo atual | var(—accent) |
| linha do tempo | progressUnachedBg | CSS var | A cor de preenchimento dos marcadores da linha do tempo ainda não foi atingida | var(—secondary) |
| linha do tempo | progressUnachedBorder | CSS var | A cor da borda dos marcadores da linha do tempo ainda não foi atingida | var(—backgroundSubtle) |

## **elementos.avaliação**

Propriedades dos componentes quiz e verificação de conhecimento.

| **Propriedade** | **Tipo** | **Descrição** | **Valor do Tablet** |
|----------------------------|----------------|------------------------------------------------------------------------------|-------------------------|
| fundo | CSS var | Plano de fundo externo do bloco de avaliação | transparente |
| optionTextColor | CSS var | Cor do texto dos rótulos de opção de resposta | var(—textPrimary) |
| optionIndicatorColor | CSS var | Cor do botão de opção ou do indicador de caixa de seleção | var(—accent) |
| optionSelectedColor | CSS var | Cor aplicada ao indicador de opção selecionado | var(—accent) |
| optionCheckmarkColor | CSS var | Cor do ícone de marca de seleção mostrado em uma opção selecionada | var(—textInverse) |
| optionBackgroundColor | CSS var | Cor de fundo de cada opção de resposta | var(—background) |
| optionHoverBackgroundColor | CSS var | Cor de fundo de uma opção de resposta ao passar o mouse | var(—backgroundSubtle) |
| buttonBackgroundColor | CSS var | Cor de fundo do botão Enviar ou Verificar resposta | var(—accent) |
| buttonTextColor | CSS var | Cor do texto do rótulo do botão de resposta Enviar ou Verificar | var(—textInverse) |
| buttonHoverBackgroundColor | CSS var | Cor do plano de fundo do botão ao passar o mouse | var(—accent) |
| corCorretaFeedback | cor hexadecimal | Cor de fundo do painel de feedback da resposta correta | #D7F7E1 |
| corIncorretaFeedback | cor hexadecimal | Cor de fundo do painel de comentários da resposta incorreta | #FFEBE8 |
| corDoTextoDeFeedback | cor hexadecimal | Cor do texto dentro do painel de feedback | #111111 |
| optionBorderCorrectColor | cor hexadecimal | Cor da borda na opção de resposta correta após a revelação da resposta | #079355 |
| optionBorderIncorrectColor | cor hexadecimal | Cor da borda em uma opção selecionada incorretamente após revelar a resposta | #D73220 |
| horizontalSpacingScale | sequência numérica | Multiplicador para espaçamento horizontal no componente de avaliação | &quot;1&quot; |
| escalaDeEspaçamentoVertical | sequência numérica | Multiplicador para espaçamento vertical no componente de avaliação | &quot;1&quot; |
| radiusScale | sequência numérica | Multiplicador do raio da borda no componente de avaliação | &quot;1&quot; |

## **Referência de var() do token da paleta**

Use essas expressões var() em valores de elemento para referenciar tokens de paleta. A atualização de um token de paleta atualiza automaticamente cada elemento que o usa.

| **Expressão** | **Referências** |
|-------------------------|-------------------------------------|
| var(—foreground) | foundation.palette.foreground |
| var(—background) | foundation.palette.background |
| var(—accent) | foundation.palette.accent |
| var(—backgroundSubtle) | foundation.palette.backgroundSubtle |
| var(—secondary) | foundation.palette.secondary |
| var(—textPrimary) | foundation.palette.textPrimary |
| var(—textInverse) | foundation.palette.textInverse |
| var(—font-heading) | foundation.fonts.heading |
| var(—font-body) | foundation.fonts.body |

## Exemplo de um tema json

```
{
  "id": "slate",
  "name": "Slate",
  "version": "1.0.0",
  "description": "A warm, authoritative theme with cream background, Adobe red accents, and the Roboto Slab + Roboto type system",
  "author": "Content Composer",
  "source": "custom",
  "isDefault": false,
  "foundation": {
    "palette": {
      "foreground": "#1A1A1A",
      "background": "#FAF7F2",
      "accent": "#E8001C",
      "backgroundSubtle": "#F0EBE1",
      "secondary": "#D9D3C9",
      "textPrimary": "#1A1A1A",
      "textInverse": "#FFFFFF"
    },
    "fonts": {
      "heading": "Roboto Slab, Georgia, 'Times New Roman', serif",
      "body": "Roboto, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif"
    },
    "spacing": {
      "horizontal": {
        "xs": "4px",
        "s": "8px",
        "m": "12px",
        "l": "16px",
        "xl": "24px"
      },
      "vertical": {
        "xs": "4px",
        "s": "8px",
        "m": "16px",
        "l": "24px",
        "xl": "32px"
      }
    },
    "radius": {
      "none": "0px",
      "s": "4px",
      "m": "8px",
      "l": "16px",
      "full": "9999px"
    },
    "logo": null
  },
  "elements": {
    "text": {
      "lessonTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "48px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "center",
        "letterSpacing": "-0.01em",
        "lineHeight": "130%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "topicTitle": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "40px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "135%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "blockHeading": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "140%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "subheading": {
        "fontFamily": "var(--font-body)",
        "fontSize": "20px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "question": {
        "fontFamily": "var(--font-heading)",
        "fontSize": "24px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0",
        "lineHeight": "150%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "caption": {
        "fontFamily": "var(--font-body)",
        "fontSize": "13px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.02em",
        "lineHeight": "170%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "paragraph": {
        "fontFamily": "var(--font-body)",
        "fontSize": "16px",
        "fontWeight": "normal",
        "fontStyle": "normal",
        "color": "var(--textPrimary)",
        "textAlign": "left",
        "letterSpacing": "0.01em",
        "lineHeight": "190%",
        "textDecoration": "none",
        "textTransform": "none",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      },
      "buttonLabel": {
        "fontFamily": "var(--font-body)",
        "fontSize": "14px",
        "fontWeight": "bold",
        "fontStyle": "normal",
        "color": "var(--textInverse)",
        "textAlign": "center",
        "letterSpacing": "0.06em",
        "lineHeight": "125%",
        "textDecoration": "none",
        "textTransform": "uppercase",
        "paddingInlineStart": "0px",
        "paragraphSpacing": "0px"
      }
    },
    "canvas": {
      "background": "var(--background)"
    },
    "header": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "footer": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "lessonHeader": {
      "background": "var(--accent)"
    },
    "topic": {
      "background": "var(--background)",
      "border": "1px solid var(--secondary)"
    },
    "navigation": {
      "background": "var(--backgroundSubtle)",
      "border": "1px solid var(--secondary)"
    },
    "button": {
      "background": "var(--accent)"
    },
    "pagination": {
      "background": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "paragraphBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "nestedAccentColor": "var(--accent)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageBlock": {
      "background": "transparent",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "videoBlock": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "imageGrid": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--accent)",
      "cardShadowOffset": "0px 2px 8px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "accordion": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "carousel": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "flipCard": {
      "background": "transparent",
      "cardFrontBackgroundColor": "var(--backgroundSubtle)",
      "cardBackBackgroundColor": "var(--accent)",
      "arrowColor": "var(--textInverse)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "tabs": {
      "background": "transparent",
      "activeBg": "var(--accent)",
      "inactiveBg": "var(--backgroundSubtle)",
      "containerBg": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "timeline": {
      "background": "transparent",
      "cardBackgroundColor": "var(--backgroundSubtle)",
      "cardBorder": "1px solid var(--secondary)",
      "cardShadowOffset": "0px 2px 6px",
      "cardShadowColor": "var(--foreground)",
      "cardShadowOpacity": "8%",
      "trackColor": "var(--secondary)",
      "progressCompletedBg": "var(--accent)",
      "progressCurrentBorder": "var(--accent)",
      "progressUnreachedBg": "var(--secondary)",
      "progressUnreachedBorder": "var(--backgroundSubtle)",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    },
    "assessment": {
      "background": "transparent",
      "optionTextColor": "var(--textPrimary)",
      "optionIndicatorColor": "var(--accent)",
      "optionSelectedColor": "var(--accent)",
      "optionCheckmarkColor": "var(--textInverse)",
      "optionBackgroundColor": "var(--background)",
      "optionHoverBackgroundColor": "var(--backgroundSubtle)",
      "buttonBackgroundColor": "var(--accent)",
      "buttonTextColor": "var(--textInverse)",
      "buttonHoverBackgroundColor": "var(--accent)",
      "feedbackCorrectColor": "#D7F7E1",
      "feedbackIncorrectColor": "#FFEBE8",
      "feedbackTextColor": "#111111",
      "optionBorderCorrectColor": "#079355",
      "optionBorderIncorrectColor": "#D73220",
      "horizontalSpacingScale": "1",
      "verticalSpacingScale": "1",
      "radiusScale": "1"
    }
  }
}
```
