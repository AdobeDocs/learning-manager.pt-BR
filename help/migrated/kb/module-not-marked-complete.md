---
jcr-language: en_us
title: O módulo é marcado como incompleto na conclusão do curso no Adobe Learning Manager
description: Mesmo depois que um aluno conclui um curso no Adobe Learning Manager, o módulo é marcado como incompleto.
contentowner: nluke
exl-id: c0f14f2e-733a-4b4f-a2c2-4c0b33a15fa1
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 65%
---
# O módulo é marcado como incompleto na conclusão do curso no Adobe Learning Manager

## Problema

Mesmo depois que um aluno conclui um curso no Adobe Learning Manager, o módulo é marcado como incompleto.

## Causa

O SCORM 2004 define os critérios de sucesso e conclusão e envia as instruções para ambos separadamente.

Por exemplo, deixe que haja um conjunto de conteúdo com **Critérios de conclusão** de 100% de exibições de slide e **Critérios de sucesso** definido como “Aprovado no questionário”.

Um aluno conclui o curso, mas reprova no questionário. Nesse caso, o progresso é 100%, mas o módulo é marcado como incompleto, pois o aluno não atende aos **Critérios de sucesso**.

## Solução

O problema está relacionado a **Preferências** de relatório definido para o projeto. O autor deve verificar os critérios definidos para a conclusão e o sucesso do curso.

Se houver alterações necessárias, o autor pode fazer isso usando uma ferramenta de criação de conteúdo, como o Adobe Captivate Classic. O autor pode atualizar o módulo adequadamente.

![](assets/scorm.png)

*Exibir Preferências de Relatório Clássico do Captivate*
