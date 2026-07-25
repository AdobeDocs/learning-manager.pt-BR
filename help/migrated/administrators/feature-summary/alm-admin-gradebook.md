---
description: Tudo sobre ativar o Gradebook e torná-lo visível para autores e alunos
jcr-language: en_us
title: Gradebook para administrador
source-git-commit: 971576b95ab0f75b9d28a7f3d1d62440927925f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---


# Ativar a visibilidade do livro de notas para sua conta

## Visão geral

Antes que os autores possam mostrar o livro de notas aos alunos em um curso, um administrador deve ativar a configuração de visibilidade do livro de notas no nível da conta. Essa configuração atua como uma opção mestre: quando desativada, os alunos não podem ver o livro de notas em nenhum curso, independentemente de como os cursos individuais estão configurados.

## O que esta configuração controla

A configuração **Visibilidade do gradiente** em **Configurações** > **Geral** determina se os autores têm permissão para expor o gradiente aos alunos no nível do curso.

| Estado da configuração | Efeito |
| --- | --- |
| Ativado | Os autores podem controlar a visibilidade do livro de notas por curso usando a opção **Mostrar livro de notas aos alunos** no editor de curso. Os alunos veem a guia **Gradebook** nos cursos em que o autor a habilitou. |
| Desativado | Os alunos não podem ver o livro de notas em nenhum curso. Se estiver desativada, a configuração do curso não terá a configuração para mostrar o livro de notas aos alunos. |


Isso significa que as configurações no nível da conta e no nível do curso funcionam juntas. Ambos devem estar ativados para que um aluno veja o catálogo de notas.

## Ativar a visibilidade do livro de notas

1. Faça logon no Adobe Learning Manager como administrador.
2. Na navegação à esquerda, selecione **Configurações**.
3. Selecione **Geral**.
4. Role até a seção **Visibilidade do gradebook**.
5. Marque a caixa de seleção **Habilitar exibição de Gradebook para alunos**.

   ![](assets/gradebook-admin-1.png)

Os autores agora podem configurar a visibilidade do livro de notas por curso.

## Impacto nos fluxos de trabalho do autor

Quando essa configuração no nível da conta está habilitada, a opção **Mostrar gradiente para alunos** fica disponível no editor de cursos. Os autores usam essa alternância para decidir, por curso, se os alunos podem ver a guia **Gradebook**.

Quando esta configuração no nível da conta está desativada:

* A opção **Mostrar gradiente para alunos** no editor de curso ainda pode aparecer, mas qualquer configuração de nível de curso é substituída. Os alunos não verão o livro de notas.
* Pontuações graduais e cálculos ponderados continuam a ser executados em segundo plano para fins de emissão de relatórios do administrador.
* Os administradores e os administradores personalizados ainda podem baixar transcrições do aluno com dados do catálogo de notas.

>[!NOTE]
>
>Desativar essa configuração no nível da conta não exclui nenhuma configuração ou pontuação do catálogo de notas. Se você reativá-lo, todas as configurações de livro de notas de nível de curso configuradas anteriormente serão restauradas imediatamente.

## Como as duas configurações interagem

| Configuração no nível da conta | Configuração no nível do curso | O que o aluno vê |
| --- | --- | --- |
| Ativado | Mostrar catálogo de notas para os alunos: **Ativado** | Guia **Gradebook** visível no reprodutor do curso |
| Ativado | Mostrar catálogo de notas para os alunos: **Desativado** | Nenhuma guia Gradebook; pontuações calculadas apenas internamente |
