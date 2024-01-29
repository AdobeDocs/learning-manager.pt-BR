---
description: Saiba como gerenciar etiquetas no Learning Manager.
jcr-language: en_us
title: Tags
contentowner: dvenkate
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---



# Tags

Agora, os administradores podem gerenciar etiquetas no Learning Manager. Use marcações melhores e um banco de dados gerenciável para ajudar os alunos a pesquisar melhor e a obter resultados de pesquisa apropriados rapidamente. Você pode gerenciar tags redundantes, com ortografia incorreta e irrelevantes usando esse recurso. Você também pode adicionar, editar, excluir, acrescentar ou substituir tags.

A lista de objetos de aprendizado associados à tag pode ser exibida clicando na contagem fornecida ao lado de cada tag. A lista mostra o número de cursos, programas de aprendizado, certificados, ajudas de tarefa e grupos de conteúdo. Clique em qualquer uma dessas opções para exibir a lista.

Você pode classificar as tags com base no uso ou na ordem alfabética usando o **[!UICONTROL Classificar por]** opção.

## Adicionar/ excluir/ editar tags {#adddeleteedittags}

1. Como administrador, no painel de navegação esquerdo, clique em **[!UICONTROL Tags]**. O **[!UICONTROL Tag Management]** é aberta.
1. Para adicionar uma nova tag, clique em **[!UICONTROL Adicionar]**. O botão Adicionar está disponível no canto superior direito da página. Se não houver tags existentes, o **[!UICONTROL Adicionar]** também estará disponível no meio do **[!UICONTROL Tag Management]** página.

   Ao adicionar várias tags, separe-as usando (,) ou (;). O nome de uma tag pode conter no máximo 50 caracteres.

1. Para excluir uma tag existente, selecione a tag clicando na caixa de seleção. Você pode selecionar várias tags de até cinquenta caracteres para excluir de uma só vez. Para excluir, siga esta etapa:

   * Selecione as tags a serem excluídas > abra o **[!UICONTROL Ação]** menu suspenso > selecionar **[!UICONTROL Excluir]**.

1. Você só pode editar uma única tag por vez. Para editar uma tag, siga esta etapa:

   * Selecione a tag para editar > abra o **[!UICONTROL Ações]**menu suspenso > clique em **[!UICONTROL Editar]**.

   O **[!UICONTROL Editar tag]** é exibida. Insira o novo nome para a tag e clique em **[!UICONTROL Salvar]**.

   Se o nome da tag inserido já existir, o Adobe Learning Manager exibirá uma mensagem de aviso. Não podem existir duas tags com o mesmo nome.

## Substituir tags {#replacetags}

1. Selecione as tags que você deseja substituir. Você pode selecionar até 50 tags de uma vez. Abra o **[!UICONTROL Ações]** menu suspenso e selecione **[!UICONTROL Substituir]**.
1. O **[!UICONTROL Substituir tags]** é exibida mostrando as tags selecionadas.

1. No menu **[!UICONTROL Nome das tags substituídas]** , digite o nome da nova tag pela qual você deseja substituir as tags selecionadas. Você pode substituí-las por uma tag existente na lista suspensa ou adicionar uma nova tag.

   Ponto-e-vírgula ou vírgula não podem fazer parte do nome da marca.  Observe que as tags sem ponto-e-vírgula e a exibição de mensagens de erro ao usar essas tags como parte de um LO não serão tratadas em cenários de migração.

1. Clique em **[!UICONTROL Substituir]**.

## Acrescentar tags {#appendtags}

No caso da operação Acrescentar para tags, a tag nova/existente será anexada a toda a lista de LOs e grupos de conteúdo associados às tags selecionadas.

1. Selecione as tags que deseja acrescentar. Você pode selecionar até 50 tags de uma vez. Abra o menu suspenso Ações e selecione **[!UICONTROL Acrescentar]**.
1. O  **[!UICONTROL Acrescentar tags]** é exibida mostrando as tags selecionadas.
1. É possível acrescentar uma tag adicional a todo o aprendizado com as tags selecionadas, inserindo o nome da **[!UICONTROL Nova etiqueta]** ou na lista suspensa das tags existentes. A nova tag será acrescentada a todo o aprendizado associado no Learning Manager.

   Ponto-e-vírgula ou vírgula não podem fazer parte do nome da marca. Se usado, o Prime mostrará uma mensagem de erro. Observe que as tags sem ponto-e-vírgula e a exibição de mensagens de erro ao usar essas tags como parte de um LO não serão tratadas em cenários de migração.

1. Clique em **[!UICONTROL Acrescentar]**.

## Configurações {#settings}

Como administrador, você pode fornecer permissão ao autor para criar tags clicando na opção configurações.

![](assets/unknown-1.jpeg)

*Página de configurações para criar uma tag*

* Quando um usuário tem permissão para criar tags e seleciona tags existentes que são inválidas no momento,

  Uma mensagem de erro é exibida, sugerindo que a tag selecionada não é mais válida. Novas tags serão criadas removendo caracteres sem suporte. Nesse caso, o autor deve poder ver as tags antigas sendo transformadas em novas antes de salvar.

* Se o usuário não tiver permissões para criar novas tags, uma mensagem de erro será exibida informando que a tag selecionada não é mais válida. Os autores podem entrar em contato com os administradores para modificar tags inválidas.

  Os autores não podem criar ou salvar tags inválidas. Eles podem remover tags inválidas, adicionar qualquer outra tag válida existente e continuar.
