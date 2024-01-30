---
jcr-language: en_us
title: O pop-up automático de feedback L1 não é exibido
description: Como resolver o erro “O pop-up automático de feedback L1 não aparece”
contentowner: saghosh
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
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

1. Certifique-se de que a opção “Mostrar questionário imediatamente após a conclusão do curso” esteja ativada em **Curso** > **Instâncias** > **Feedback N1**.
   <!--![](assets/l1-feedback.png)-->
1. Como administrador, acesse **Configurações > Feedback**. Verifique quando o lembrete está programado. Caso esteja programado para **Após a conclusão do curso**, altere a opção para **Na conclusão do curso**.
1. Ative os seguintes modelos de e-mail: **Modelos de e-mail > Lembretes e atualizações > Solicitar feedback do aluno para o curso**. Caso a opção esteja desativada, ative-a e teste.
1. Se as etapas acima não funcionarem, exclua o lembrete presente em **Administrador > Configurações > Feedback**. Crie uma para &quot;Conclusão do curso&quot; e defina a recorrência de acordo com o requisito.
