---
jcr-language: en_us
title: O pop-up automático de feedback L1 não é exibido
description: Como resolver o erro “O pop-up automático de feedback L1 não aparece”
contentowner: saghosh
exl-id: 47edcd7f-e332-4a75-a025-fd07737d0b70
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 76%

---

# O pop-up automático de feedback L1 não é exibido

## Problema

O pop-up de feedback L1 não aparece para um aluno após concluir o curso.

## Causa

Às vezes, pode acontecer que um aluno não receba o feedback L1 após concluir um curso específico ou receba uma mensagem como mostrado abaixo:

![](assets/l1-feedback.png)

*Não é possível receber feedback L1*

Isso pode acontecer pelos seguintes motivos:

1. O feedback não é definido para aparecer após a conclusão do curso.
1. Os lembretes estão desativados.
1. Um lembrete está programado para aparecer após um determinado período de tempo.

## Resolução

1. Verifique se a opção “Mostrar questionário imediatamente após a conclusão do curso” está habilitada em **Curso** > **Instâncias** > **Feedback L1**.
   <!--![](assets/l1-feedback.png)-->
1. Como administrador, acesse **Configurações > Feedback**. Verifique quando o lembrete está programado. Caso esteja programado para **Após a conclusão do curso**, altere a opção para **Na conclusão do curso**.
1. Habilite os seguintes modelos de email: **Modelos de email > Lembretes e atualizações > Solicitar feedback do aluno para o curso**. Caso a opção esteja desativada, ative-a e teste.
1. Se as etapas acima não funcionarem, exclua o lembrete presente em **Administrador > Configurações > Feedback**. Crie uma para &quot;Conclusão do curso&quot; e defina a recorrência de acordo com o requisito.
