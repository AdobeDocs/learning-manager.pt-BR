---
jcr-language: en_us
title: Não é possível exibir envios de arquivos no Adobe Learning Manager
description: Os professores não podem exibir os arquivos que os alunos carregaram no Módulo de Atividade de Envio.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---



# Não é possível exibir envios de arquivos no Adobe Learning Manager

## Problema

Um professor não pode exibir os envios de arquivo que um aluno carregou.

## Descrição

Os professores não podem exibir os arquivos que os alunos carregaram no **Módulo de Atividade de Envio**.

Por exemplo, um aluno se inscreveu em uma instância chamada **Instância de teste** de um curso, conforme mostrado abaixo:

![](assets/test-instance.png)

*Exibir instância*

O aluno abre o curso e carrega um arquivo no módulo Atividade.

Quando o professor tenta aprovar o envio, ele não consegue fazer isso.

![](assets/activity.png)

*Fazer upload de um arquivo no módulo Atividade*

## Causa

Se não houver professor na instância do curso na qual o aluno está inscrito, o problema será exibido.

## Resolução

Para verificar se um professor foi adicionado à instância do curso, execute as etapas abaixo:

1. Navegue até as configurações do curso.
1. No menu **Gerenciar** clique em **[!UICONTROL Instâncias].**
1. Na instância em que o aluno está inscrito, clique em **[!UICONTROL Sessões]**.

   ![](assets/check-instructor.png)

   *Selecione Sessões na instância*

   Não há professor atribuído a esta sessão.

1. Clique em **[!UICONTROL Editar]**. Adicione o professor que aprova o envio do arquivo.

   ![](assets/assign-instructor.png)

   *Adicionar o professor*
1. Salve as alterações.

