---
jcr-language: en_us
title: Problemas em desativar um programa de aprendizado
description: Problemas em desativar um programa de aprendizado no Adobe Learning Manager
contentowner: nluke
exl-id: 706cafe3-2650-4837-9dee-e381a4a711f9
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 55%

---

# Problemas em desativar um programa de aprendizado

## Problema

Um programa de aprendizado é automaticamente desativado.

## Causa

Há situações em que um programa de aprendizad é desativado sem um administrador/autor desativar o LP explicitamente.

Esse problema ocorre porque um programa de aprendizado é uma coleção de cursos. Os treinamentos de ordem superior são desativados se algum dos cursos dentro deles contiver uma instância desativada ou a instância do curso for desativada.

## Resolução

Para verificar o curso que contém uma instância desativada, siga as etapas abaixo:

1. Faça logon como administrador e inicie o programa de aprendizado relevante.

1. Clique em **[!UICONTROL Instâncias]** > **CCursos**. A página lista todos os cursos que fazem parte deste programa de aprendizado. Você poderá ver o curso que contém uma instância desativada.

   ![](assets/retired-instance.png)

   *Exibir lista de todos os cursos*

1. Depois de descobrir a instância do curso que foi desativada, clique em **[!UICONTROL Cursos]** > **[!UICONTROL Abrir o curso]**.

1. Clique em **[!UICONTROL Instâncias]**. Na instância desativada, clique em **[!UICONTROL Editar]** e edite a data de conclusão para uma data futura na qual você deseja que a instância seja desativada.

   ![](assets/completion-date.png)

   *Editar a data de conclusão de um curso*

1. Depois de concluído, clique na lista suspensa conforme mostrado na imagem abaixo. Em seguida, clique em **[!UICONTROL Reabrir instância]**.

   ![](assets/re-open-instance.png)

   *Reabrir a instância de um curso*

1. Visite o Programa de aprendizado relevante. Clique em **[!UICONTROL Instâncias]** e execute a etapa anterior para reabrir a instância do Programa de Aprendizado.
