---
description: Continue lendo para saber como gerar arquivos HAR no Google Chrome.
jcr-language: en_us
title: Gerar um arquivo HAR
contentowner: dvenkate
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---



# Gerar um arquivo HAR

Continue lendo para saber como gerar arquivos HAR no Google Chrome.

Para gerar um arquivo HAR, siga estas etapas:

1. Abra uma janela do Google Chrome e abra uma nova guia.
1. Abra as ferramentas do desenvolvedor para a página, clique com o botão direito > Inspect.
1. Abra o **[!UICONTROL Rede]** guia. Verifique se o botão de gravação em vermelho está ativo. Ative o **[!UICONTROL Preservar log]** caixa de seleção.

   ![](assets/preserve-log-checkbox.png)

   *Marque a caixa de seleção Preservar o registro na guia Rede*

1. Fazer logon em [Learning Manager](https://learningmanager.adobe.com/acapindex.html) usando suas credenciais e participe do curso. Execute todas as operações que resultarão no problema.
1. Nas ferramentas de desenvolvedor, clique com o botão direito e selecione **Salvar tudo como HAR com conteúdo**.

   Em algumas versões do Google Chrome, talvez seja necessário selecionar **[!UICONTROL Copiar]** > **[!UICONTROL Copiar tudo como HAR]**.

   ![](assets/copy-hra.png)

   *Copiar todos os arquivos HAR*

1. Cole o conteúdo copiado em um arquivo do bloco de notas. Salvar na área de trabalho como **logs.har** e envie-o por email para Adobe.
