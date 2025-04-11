---
description: Saiba como gerenciar etiquetas no Learning Manager.
jcr-language: en_us
title: Tags
contentowner: dvenkate
exl-id: ea39d2a2-3d2b-43ae-8f8d-b97420b9d008
source-git-commit: a28ac8f57710c118ca4ad02872fd100c6f24beac
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 63%

---

# Tags

Agora, os administradores podem gerenciar etiquetas no Learning Manager. Use bancos de dados melhor etiquetados e gerenciáveis para ajudar os alunos a pesquisar melhor e obter resultados de pesquisa apropriados rapidamente. Você pode gerenciar etiquetas redundantes, com erros de ortografia e irrelevantes usando esse recurso. Você também podem adicionar, editar, excluir, acrescentar ou substituir tags.

A lista de objetos de aprendizado associados à tag pode ser exibida clicando na contagem fornecida ao lado de cada tag. A lista mostra o número de cursos, programas de aprendizado, certificados, ajudas de tarefa e grupos de conteúdo. Clique em qualquer uma dessas opções para exibir a lista.

Você pode classificar as tags com base no uso ou na ordem alfabética usando a opção **[!UICONTROL Classificar por]**.

## Introdução às tags

Esse treinamento ensinará como adicionar, editar, substituir, adicionar e excluir tags. Você também aprenderá como alterar as configurações de permissão e usar filtros de tags.

[![botão](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318920)

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

## Adicionar/ excluir/ editar tags {#adddeleteedittags}

1. Como administrador, no painel de navegação esquerdo, clique em **[!UICONTROL Tags]**. A página **[!UICONTROL Gerenciamento de tags]** é aberta.
1. Para adicionar uma nova tag, clique em **[!UICONTROL Adicionar]**. O botão Adicionar está disponível no canto superior direito da página. Se não houver tags existentes, o botão **[!UICONTROL Adicionar]** também estará disponível no meio da página **[!UICONTROL Gerenciamento de tags]**.

   Ao adicionar várias tags, separe-as usando (,) ou (;). O nome de uma tag pode conter no máximo 50 caracteres.

1. Para excluir uma tag existente, selecione a tag clicando na caixa de seleção. Você pode selecionar várias tags de até 50% em número para excluir de uma vez. Para excluir, siga esta etapa:

   * Selecione as tags a serem excluídas > abra o menu suspenso **[!UICONTROL Ação]** > selecione **[!UICONTROL Excluir]**.

1. Você só pode editar uma única tag por vez. Para editar uma tag, siga esta etapa:

   * Selecione a tag que deseja editar > abra o menu suspenso **[!UICONTROL Ações]**> clique em **[!UICONTROL Editar]**.

   A caixa de diálogo **[!UICONTROL Editar tag]** é exibida. Insira o novo nome para a tag e clique em **[!UICONTROL Salvar]**.

   Se o nome da tag já existente, o Adobe Learning Manager exibirá uma mensagem de aviso. Não podem existir duas tags com o mesmo nome.

## Substituir tags {#replacetags}

1. Selecione as tags que você deseja substituir. Você pode selecionar até 50 marcas de uma só vez. Abra o **[!UICONTROL menu suspenso Ações]** e selecione **[!UICONTROL Substituir]**.
1. A **[!UICONTROL caixa de diálogo Substituir tags]** é exibida, mostrando as marcas selecionadas.

1. Na opção **[!UICONTROL Nome das tags substituídas]**, digite o nome da nova tag pela qual você deseja substituir as tags selecionadas. Você pode substituí-las por uma tag existente na lista suspensa ou adicionar uma nova tag.

   Ponto e vírgula não pode fazer parte do nome da tag.  Observe que as tags sem ponto-e-vírgula e a exibição de mensagens de erro ao usar essas tags como parte de um LO não serão tratadas em cenários de migração.

1. Clique em **[!UICONTROL Substituir]**.

## Acrescentar tags {#appendtags}

No caso da operação de anexação de tags, a tag nova/existente será anexada a toda a lista de LOs e grupos de conteúdo associados às tags selecionadas.

1. Selecione as tags que deseja acrescentar. Você pode selecionar até 50 marcas de uma só vez. Abra o menu suspenso Ações e selecione **[!UICONTROL Acrescentar]**.
1. A  **[!UICONTROL caixa de diálogo Acrescentar tags]** é exibida, mostrando as marcas selecionadas.
1. É possível acrescentar uma tag adicional a todo o aprendizado com as tags selecionadas, inserindo o nome da **[!UICONTROL Nova tag]** ou na lista suspensa das tags existentes. A nova tag será acrescentada a todo o aprendizado associado no Learning Manager.

   Ponto-e-vírgula ou vírgula não podem fazer parte do nome da tag. Se usado, o Prime mostrará uma mensagem de erro. Observe que as tags sem ponto-e-vírgula e a exibição de mensagens de erro ao usar essas tags como parte de um LO não serão tratadas em cenários de migração.

1. Clique em **[!UICONTROL Acrescentar]**.

## Configurações {#settings}

Como administrador, você pode conceder permissão ao autor para criar tags clicando na opção de configurações.

![](assets/unknown-1.jpeg)

*Página de configurações para a criação de uma tag*

* Quando um usuário tem permissão para criar tags e seleciona tags existentes que são inválidas no momento,

  Uma mensagem de erro é exibida sugerindo que a tag selecionada não é mais válida. Novas tags serão criadas removendo caracteres sem suporte. Nesse caso, o autor deve poder ver as tags antigas sendo transformadas em novas antes de salvar.

* Se o usuário não tiver as permissões para criar novas tags, uma mensagem de erro será exibida indicando que a marca selecionada não é mais válida. Os autores podem entrar em contato com os administradores para modificar tags inválidas.

  Os autores não podem criar ou salvar tags inválidas. Eles podem remover tags inválidas e adicionar qualquer outra tag válida existente e continuar.
