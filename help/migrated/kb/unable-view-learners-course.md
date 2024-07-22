---
jcr-language: en_us
title: Não é possível visualizar alunos em um curso
description: A guia Alunos de um curso não exibe nenhum aluno inscrito no Adobe Learning Manager. No entanto, se você gerar um relatório, poderá visualizar os alunos inscritos no relatório.
contentowner: saghosh
exl-id: 2ea54347-fa6b-493e-b73c-d350efb2aaaf
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
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
1. Clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios personalizados]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Transcrição do aluno]**.

1. Insira o nome do **[!UICONTROL Aluno]** e especifique o intervalo de **[!UICONTROL Datas]**.
1. Expanda a seção **[!UICONTROL Opções avançadas]** e selecione a opção **[!UICONTROL Ativar informações de nível do módulo]**.
1. Clique em **[!UICONTROL Gerar]**.

   Na transcrição do aluno, você pode ver qual objeto de aprendizado superior o aluno está inscrito.
