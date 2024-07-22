---
description: Leia sobre como gerar arquivos HAR files no Google Chrome.
jcr-language: en_us
title: Gerar um arquivo HAR
contentowner: dvenkate
exl-id: 99fe78e8-b5e7-40a7-b9a5-efc2382de993
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 57%

---

# Gerar um arquivo HAR

Leia sobre como gerar arquivos HAR files no Google Chrome.

Para gerar um arquivo HAR, siga estas etapas:

1. Abra uma janela do Google Chrome e abra uma nova aba.
1. Abra as ferramentas do desenvolvedor para a página, clique com o botão direito do mouse > Inspecionar.
1. Abra a guia **[!UICONTROL Rede]**. Verifique se o botão de gravação em vermelho está ativo. Habilite a caixa de seleção **[!UICONTROL Preservar Log]**.

   ![](assets/preserve-log-checkbox.png)

   *Marque a caixa de seleção Preservar Log na guia Rede*

1. Faça login no [Learning Manager](https://learningmanager.adobe.com/acapindex.html) usando suas credenciais e participe do curso. Faça todas as operações que irão resultar no problema.
1. Nas ferramentas de desenvolvedor, clique com o botão direito do mouse e selecione **Salvar tudo como HAR com conteúdo**.

   Em algumas versões do Google Chrome, você poderá ter que selecionar **[!UICONTROL Copiar]** > **[!UICONTROL Copiar tudo como HAR]**.

   ![](assets/copy-hra.png)

   *Copiar todos os arquivos HAR*

1. Cole o conteúdo copiado em um arquivo do bloco de notas. Salve-o na área de trabalho como **logs.har** e envie-o por email para Adobe.
