---
description: Leia sobre como gerar arquivos HAR files no Google Chrome.
jcr-language: en_us
title: Gerar um arquivo HAR
contentowner: dvenkate
exl-id: 99fe78e8-b5e7-40a7-b9a5-efc2382de993
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 65%
---
# Gerar um arquivo HAR

Leia sobre como gerar arquivos HAR files no Google Chrome.

Para gerar um arquivo HAR, siga estas etapas:

1. Abra uma janela do Google Chrome e abra uma nova aba.
1. Abra as ferramentas do desenvolvedor para a página, clique com o botão direito do mouse > Inspecionar.
1. Abra a guia **[!UICONTROL Rede]**. Assegure-se de que o botão de gravação em vermelho esteja ativo. Ative a caixa de seleção **[!UICONTROL Preservar o registro]**.

   ![](assets/preserve-log-checkbox.png)

   *Marque a caixa de seleção Preservar Log na guia Rede*

1. Faça login no [Learning Manager](https://learningmanager.adobe.com/acapindex.html) usando suas credenciais e participe do curso. Faça todas as operações que irão resultar no problema.
1. Nas ferramentas de desenvolvedor, clique com o botão direito do mouse e selecione **Salvar tudo como HAR com conteúdo**.

   Em algumas versões do Google Chrome, você poderá ter que selecionar **[!UICONTROL Copiar]** > **[!UICONTROL Copiar tudo como HAR]**.

   ![](assets/copy-hra.png)

   *Copiar todos os arquivos HAR*

1. Cole o conteúdo copiado em um arquivo do bloco de notas. Salve-o na área de trabalho como **logs.har** e envie-o por email para Adobe.
