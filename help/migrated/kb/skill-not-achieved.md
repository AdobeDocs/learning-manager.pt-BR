---
jcr-language: en_us
title: Não é possível obter uma habilidade após concluir um curso
description: Um aluno, mesmo após concluir um curso, não obtém uma habilidade. As habilidades atribuídas a esse curso permanecem como Em andamento para o aluno.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---



# Não é possível obter uma habilidade após concluir um curso

## Problema

Um aluno, mesmo após concluir um curso, não obtém uma habilidade. As habilidades atribuídas a esse curso permanecem como **Em andamento** para o aluno.

## Causa

Esse problema ocorre se o **Créditos necessários** para obter essa habilidade é maior que o **Créditos obtidos** pelo aluno após concluir o curso.

## Solução

Verificar o atual **Créditos de habilidade** e **Ponto** informações necessárias para obter a habilidade. Siga as etapas abaixo:

1. Para o aluno, gere um **Transcrição do aluno** relatório.
1. Ao gerar a transcrição do aluno, clique em **[!UICONTROL Opções avançadas]** e marque a opção **[!UICONTROL Incluir dados de habilidades e folhas de resumo]**.

   ![](assets/advanced-options.png)

   *Selecione a opção Incluir dados de habilidades e folhas de resumo*

1. Abra o relatório de transcrição do aluno baixado.
1. Navegue até a guia **[!UICONTROL Transcrição de habilidades]** planilha. Aqui, você pode ver o **[!UICONTROL Créditos necessários]** e **[!UICONTROL Créditos obtidos]** pelo aluno.

   Por exemplo, no exemplo abaixo, os créditos necessários para obter a habilidade para um curso são 50. Mas o aluno obteve apenas um crédito.

   ![](assets/skill-transcript.png)

   *Exibir créditos necessários*

1. Para verificar os créditos atribuídos a uma habilidade específica, faça logon como administrador e navegue até **Habilidades** como mostrado abaixo:

   ![](assets/skill.png)

   *Guia Ativar habilidades*

1. Para verificar o número de créditos atribuídos a um curso, faça logon como autor e abra o curso. Clique em **[!UICONTROL Configurações]** > **Habilidades do curso** conforme mostrado abaixo:

   ![](assets/course-skills.png)

   *Exibir habilidades do curso*
