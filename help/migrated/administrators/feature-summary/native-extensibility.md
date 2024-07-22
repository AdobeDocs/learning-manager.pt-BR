---
title: Extensibilidade nativa
description: Configure experiências personalizadas na versão nativa do Adobe Learning Manager, permitindo que você não use headless para casos menos complicados.
exl-id: 510bd00f-4f52-4705-817e-4ee73380ca90
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 48%

---

# Extensibilidade nativa

Você pode configurar experiências personalizadas dentro da versão nativa do Adobe Learning Manager, permitindo que você não use headless para casos menos complicados. Você também pode criar aplicativos personalizados e colocá-los em vários pontos na versão nativa dos fluxos de trabalho do aluno, gerente, administrador, autor ou professor.

O Adobe Learning Manager oferece suporte a 15 pontos de chamada no aplicativo do administrador, autor, aluno, gerente e professor.

## Criar uma extensão

1. Como administrador, no painel esquerdo, selecione **[!UICONTROL Extensões nativas]**.
1. Selecione Adicionar uma extensão.
1. Digite o nome da extensão no campo **[!UICONTROL Nome]**.
1. Digite a descrição da extensão no campo **[!UICONTROL Descrição]**.
1. Selecione um ponto de chamada. Um ponto de chamada é qualquer local no Adobe Learning Manager em que um link ou botão pode ser inserido em um aplicativo personalizado. Os seguintes pontos de chamada estão disponíveis:

   Para este exemplo, selecione **[!UICONTROL Administrador]**, **[!UICONTROL Autor: Curso]**, **[!UICONTROL Caminho de Aprendizado]** - **[!UICONTROL Instâncias]** - **[!UICONTROL Linha de instância]**.

   ![imagem de extensão](assets/list-native-extensions.png)
   *Selecionar ponto de invocação*

1. Digite o rótulo da extensão que aparecerá na interface do usuário no campo **[!UICONTROL Rótulo da extensão]**.
1. Digite a URL onde deseja hospedar a extensão no campo **[!UICONTROL URL]**.
1. No menu suspenso Abrir em, selecione se deseja iniciar a extensão em uma janela modal ou em uma nova guia.
1. Selecione o tamanho do modal. As opções estão disponíveis se você selecionou o modal *no aplicativo* na etapa anterior.

   Para manter a acessibilidade dentro do pop-up, o aplicativo de extensão deve ser enviado ao evento assim que estiver no último elemento focalizável em seu site e, em seguida, o usuário seleciona a tecla TAB. Isso é necessário para manter o foco dentro do pop-up para oferecer suporte à acessibilidade.

   ```
   window.parent.postMessage({*}
   
   { type: 'ALM_EXTENSION_APP', eventType: 'trapFocusInModal' }
   
   ,{}'');
   ```

1. Defina o escopo da extensão. Estão disponíveis os seguintes escopos:

   * **[!UICONTROL Todos os cursos, caminhos de aprendizado e certificações]**: esta extensão está habilitada para todos os cursos, caminhos de aprendizado e certificações. Junto com os administradores, os autores podem desativá-la para alguns cursos, caminhos de aprendizado e certificações.
   * **[!UICONTROL Cursos selecionados, caminhos de aprendizado e certificações]**: esta extensão está desabilitada para todos os cursos, caminhos de aprendizado e certificações. Junto com os administradores, os autores podem ativá-la para alguns cursos, caminhos de aprendizado e certificações.

1. Selecione a opção **[!UICONTROL Ativar]** para tornar a extensão ativa. Uma vez ativa, a extensão aparece no ponto de chamada especificado de acordo com o escopo.
1. Selecione **[!UICONTROL Salvar]** no canto superior direito da página para criar a extensão.

## Acessar a extensão como administrador

1. Como administrador, selecione **[!UICONTROL Caminhos de Aprendizado]** na barra de ferramentas esquerda.
1. Selecione um curso > **[!UICONTROL Exibir Caminho de Aprendizado]**.
1. Selecione **[!UICONTROL Instâncias]** no painel esquerdo.
1. Selecione **[!UICONTROL Mais]** na seção Instâncias. A extensão aparece na seção Instâncias.

   ![imagem de instâncias](assets/instances-extension.png)
   *Selecione a extensão*

   Quando você seleciona a extensão, a extensão aparece na janela modal.

## Acessar a extensão como autor

1. Como administrador, selecione **[!UICONTROL Caminhos de Aprendizado]** na barra de ferramentas esquerda.
1. Selecione um curso > **[!UICONTROL Exibir Caminho de Aprendizado]**.
1. Selecione **[!UICONTROL Instâncias]** no painel esquerdo.
1. Selecione **[!UICONTROL Mais]** na seção Instâncias. A extensão aparece na seção Instâncias.

   ![imagem de instâncias](assets/instances-extension.png)
   *Acessar extensão como autor*

   Quando você seleciona a extensão, a extensão aparece na janela modal.

## Exibir todas as extensões

Como administrador, você pode exibir todas as extensões na página Extensões nativas. Para ver a lista, selecione Extensões nativas no painel esquerdo do aplicativo.

![exibir imagem de extensões](assets/view-extensions.png)
*Exibir todas as extensões*

## Ativar ou desativar uma extensão

Como autor, na página Configurações de um curso, você pode ativar ou desativar uma extensão para um Curso, Certificação ou Caminho de Aprendizado.

![ativar imagem de extensão](assets/activate-extension.png)
*Ativar uma extensão*

## Compartilhar uma Chave de acesso

Você deve compartilhar a Chave de acesso se estiver configurando uma extensão de inscrição.

Isso é importante porque, se essa chave não for gerada e compartilhada, a autenticação da inscrição falhará e os alunos não poderão se inscrever nos cursos.

A chave de acesso deve ser compartilhada para inscrição no curso ou no Caminho de aprendizado e nos certificados.

Na guia Configurações, gere a tecla.

![compartilhar imagem da chave](assets/share-extension.png)
*Compartilhar a chave de acesso*

## Baixar relatório de extensão

Há duas maneiras de baixar este relatório.

**Relatório de configuração de extensão**

1. Na página Extensões nativas, selecione **[!UICONTROL Relatório de configuração de extensão]**.

   ![imagem do relatório](assets/extension-config-report.png)
   *Baixar relatório de extensão*

   O relatório é gerado.

1. Selecione OK.

   ![gerando imagem de relatório](assets/generating-report.png)
   *Gerando o relatório*

   O relatório contém os seguintes campos:

   * Nome da Extensão
   * Ponto de Invocação
   * Rótulo
   * Abrir no URL
   * Escopo
   * Ativar
   * ID exclusiva do OA
   * Id do treinamento
   * Tipo de Treinamento
   * Nome do Treinamento

**Página Relatórios**

1. Em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]**, selecione **[!UICONTROL Relatório de Configuração de Extensão]**.

   ![imagem da página de relatórios](assets/extension-report-page.png)
   *Baixar o relatório da página Relatórios*

O estado deve estar no intervalo **0 - 4294967295**, ao configurar o estado de inscrição.
