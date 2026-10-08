---
jcr-language: en_us
title: Não é possível obter uma habilidade após concluir um curso
description: Um aluno, mesmo após concluir um curso, não obtém uma habilidade. As habilidades atribuídas a esse curso permanecem como Em andamento para o aluno.
contentowner: nluke
exl-id: d9c1e2a2-351d-4d6f-b2e6-f9e9278e6523
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 72%
---
# Não é possível obter uma habilidade após concluir um curso

## Problema

Um aluno, mesmo após concluir um curso, não obtém uma habilidade. As habilidades atribuídas a esse curso permanecem como **Em andamento** para o aluno.

## Causa

Esse problema ocorre se os **Créditos necessários** para obter essa habilidade é maior que os **Créditos obtidos** pelo aluno após concluir o curso.

## Solução

Verifique os **Créditos de habilidade** e o **Ponto** atuais necessários para obter a habilidade. Siga as etapas abaixo:

1. Para o aluno, gere um relatório de **Transcrição do aluno**.
1. Ao gerar a transcrição do aluno, clique em **[!UICONTROL Opções Avançadas]** e marque a opção **[!UICONTROL Incluir dados de habilidades e folhas de resumo]**.

   ![](assets/advanced-options.png)

   *Selecione a opção Incluir dados de habilidades e folhas de resumo*

1. Abra o relatório de transcrição do aluno baixado.
1. Navegue até a folha de **[!UICONTROL Transcrição de habilidades]**. Aqui, você pode ver os **[!UICONTROL Créditos necessários]** e **[!UICONTROL Créditos obtidos]** pelo aluno.

   Por exemplo, no exemplo abaixo, os créditos necessários para obter a habilidade para um curso são 50. Mas o aluno obteve apenas um crédito.

   ![](assets/skill-transcript.png)

   *Exibir créditos necessários*

1. Para verificar os créditos atribuídos a uma habilidade específica, faça logon como administrador e navegue até a guia **Habilidades**, conforme mostrado abaixo:

   ![](assets/skill.png)

   *Iniciar a guia Habilidades*

1. Para verificar o número de créditos atribuídos a um curso, faça logon como autor e abra o curso. Clique em **[!UICONTROL Configurações]** > **Habilidades do curso** conforme mostrado abaixo:

   ![](assets/course-skills.png)

   *Exibir Habilidades Do Curso*
