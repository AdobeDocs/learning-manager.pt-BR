---
jcr-language: en_us
title: Não é possível pesquisar um curso no Learning Manager
description: Um aluno está impossibilitado de pesquisar um curso no Learning Manager.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 55%

---



# Não é possível pesquisar um curso no Learning Manager

## Problema

Um aluno está impossibilitado de pesquisar um curso no Learning Manager.

## Cenário 1: A inscrição é feita por meio de um objeto de aprendizado superior

### Resumo

Há cenários onde um aluno pesquisa um curso e o curso não é listado. Mas se o aluno se inscreveu em um Programa de aprendizado/Certificação, ele poderá ver o curso dentro do Objeto de aprendizado.

### Por que isso ocorre?

No Learning Manager, quando um aluno é inscrito por meio de um Programa de aprendizado/Certificação, a inscrição para esse curso é feita por meio do Programa de aprendizado/Certificação.

Portanto, o aluno não pode procurar os cursos independentes em **Meu aprendizado**.

No entanto, o aluno não pode visualizar os cursos dentro do Programa de aprendizado/Certificação.

## Cenário 2: O aluno não tem acesso ao catálogo que contém o curso.

### Resumo

Um aluno não pode pesquisar cursos no Catálogo ou no Painel de aprendizado.

### Por que isso ocorre?

Esse problema ocorre se:

* O aluno não faz parte do catálogo que contém o curso **OU**
* O curso não faz parte do catálogo ao qual o aluno tem acesso.

### Resolução

1. Faça logon como administrador.

1. Clique em **[!UICONTROL Catálogo]** e navegue até o catálogo que contém o curso.
1. Clique em **[!UICONTROL Compartilhar internamente]** ou **[!UICONTROL Conteúdo]** (dependendo do cenário mencionado acima).

   ![](assets/cp-share-internally.png)

   *Compartilhar o catálogo internamente*

1. Analise os cenários abaixo:

   * O aluno não faz parte do catálogo

     Para compartilhar o catálogo, clique em **[!UICONTROL Adicionar]** e adicione o grupo de usuários do qual o usuário faz parte. Clique em **[!UICONTROL Salvar]**.

     ![](assets/cp-add-user-group.png)

     *Adicionar o grupo de usuários*

   * O curso não faz parte do catálogo

     Na seção Conteúdo, clique em **[!UICONTROL Adicionar conteúdo]** e selecione o curso que você precisa adicionar ao catálogo.

     ![](assets/cp-add-content.png)

     *Adicionar conteúdo ao curso*
