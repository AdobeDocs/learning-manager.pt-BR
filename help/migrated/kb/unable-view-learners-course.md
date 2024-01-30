---
jcr-language: en_us
title: Não é possível visualizar alunos em um curso
description: A guia Alunos de um curso não exibe nenhum aluno inscrito no Adobe Learning Manager. No entanto, se você gerar um relatório, poderá visualizar os alunos inscritos no relatório.
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 58%

---



# Não é possível visualizar alunos em um curso

## Problema

Não é possível visualizar os alunos inscritos em um curso.

## Descrição

A guia Alunos de um curso não exibe nenhum aluno inscrito. No entanto, se você gerar um relatório, poderá visualizar os alunos inscritos no relatório.

![](assets/no-learners.png)

*Nenhum aluno exibido*

## Causa

Se um aluno estiver inscrito em um Objeto de aprendizado superior (Programa de aprendizado ou Certificação), o aluno ficará visível na guia Aluno do Objeto de aprendizado superior. O aluno não será pesquisável na guia Alunos do curso.

**Como visualizar em qual objeto de aprendizado superior o aluno está inscrito?**

Você pode verificar essas informações no relatório Transcrição de aprendizado. Para gerar uma transcrição do aluno, siga as etapas abaixo:

1. Faça logon como administrador.
1. Clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Transcrição do aluno]**.

1. Insira o nome do **[!UICONTROL Aluno]** e especificar a **[!UICONTROL Data]** intervalo.
1. Expanda a seção **[!UICONTROL Opções avançadas]** e selecione a opção **[!UICONTROL Ativar informações de nível do módulo]**.
1. Clique em **[!UICONTROL Gerar]**.

   Na transcrição do aluno, você pode ver qual objeto de aprendizado superior o aluno está inscrito.
