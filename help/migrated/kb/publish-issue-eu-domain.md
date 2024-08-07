---
jcr-language: en_us
title: Não é possível publicar no domínio da UE do Learning Manager
description: Não é possível publicar do Adobe Captivate para o domínio da UE do Adobe Learning Manager no Adobe Learning Manager.
contentowner: nluke
exl-id: fb8ae1af-9902-4901-8263-fb3ebff98fbc
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 83%

---

# Não é possível publicar no domínio da UE do Learning Manager {#unable-to-publish-to-learning-manager-eu-domain}

## Problema

Não é possível publicar do Adobe Captivate para o domínio da UE do Adobe Learning Manager.

## Erro

Nenhuma conta encontrada

## Descrição

Há cenários em que os autores tentam publicar um curso do Adobe Captivate para o Adobe Learning Manager. No entanto, eles não podem fazer isso, pois veem a mensagem de erro &quot;Nenhuma conta encontrada&quot;.

## Causa

Esse problema ocorre porque o Adobe Captivate está configurado por padrão para publicar conteúdo no domínio dos EUA do Adobe Learning Manager.

## Solução:

Observações:

* Se estiver aberto, feche o aplicativo Adobe Captivate.
* Você precisaria de acesso de administrador em sua máquina para executar as etapas abaixo. Caso você não tenha acesso de administrador, entre em contato com a equipe de TI para obter assistência.

Execute as etapas abaixo:

1. Vá para o diretório de instalação do Adobe Captivate.

   Por exemplo, `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019) é a versão do Captivate. Difere se você estiver usando uma versão diferente do Adobe Captivate).

1. Copie o arquivo de configuração **AdobeCaptivate.ini** para a área de trabalho.

   ![](assets/cp-captivate.ini.png)
   *Exibir o arquivo de configuração*

1. Abra o arquivo copiado da área de trabalho em um Bloco de notas.
1. Altere o valor de LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` para LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *Exibir PrimeBaseURL*

1. Salve as alterações feitas no Bloco de notas.
1. Copie o arquivo salvo que você editou e cole-o de volta no caminho do arquivo. Substituir o arquivo original em `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. Uma vez concluído, inicie o Adobe Captivate e tente publicar no Adobe Learning Manager.
