---
description: Saiba como importar um arquivo JSON de tema personalizado para o Compositor de conteúdo e como salvá-lo como um novo tema personalizado disponível no painel Temas do curso.
jcr-language: en_us
title: Importar um tema
source-git-commit: f8687710f5b73e8b7cf8d56057cac25483f38cdc
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Importar um tema

Importe um arquivo JSON personalizado para aplicar suas alterações como um novo tema no Compositor de conteúdo.

1. Selecione **Temas** na barra de ferramentas.

2. Selecione **Importar** das opções de **Tema do curso**.
   ![](../assets/48_course_themes_import_button_updated.png)

3. Escolha o arquivo JSON personalizado no seu computador.

4. Selecione **Salvar como novo** para criar um novo tema personalizado.

## Visão geral da estrutura JSON do tema

Um arquivo JSON de tema tem cinco áreas principais:

| Seção | Controles |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Metadados (id, nome, versão, descrição, autor, origem, isDefault) | Identidade do tema e informações de exibição |
| foundation.palette | Os 7 tokens de cores principais (primeiro plano, plano de fundo, acento, plano de fundo Sutil, secundário, textPrimary, textInverse) referenciados em todo o tema por meio de var(—tokenName) |
| foundation.fonts | Pilhas de fontes de título e corpo |
| foundation.spacing e foundation.radius | Escala de espaçamento horizontal/vertical e tokens de raio de canto |
| elementos | Tipografia e estilo estrutural para cada função de texto (título da lição, título do tópico, título do bloco, subtítulo, pergunta, legenda, parágrafo, rótulo do botão) e para cada componente (bloco do parágrafo, bloco da imagem, bloco do vídeo, grade da imagem, acordeão, carrossel, flipCard, guias, linha do tempo, avaliação) |

Como a maioria dos valores fazem referência a tokens de paleta usando var(—tokenName), a atualização de um único token, como acento, ocorre automaticamente em cascata que muda em todos os elementos que fazem referência a ele. Não é necessário pesquisar valores de cores individuais.

