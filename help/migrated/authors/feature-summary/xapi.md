---
jcr-language: en_us
title: xAPI no Learning Manager
description: A Experience API (xAPI) é uma especificação de software de e-learning que permite que o conteúdo de aprendizado e os sistemas de aprendizado se comuniquem entre si de maneira que registrem e rastreiem todos os tipos de experiências de aprendizado.
exl-id: 8e36b538-a451-448e-a65d-08d286adcfdb
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 49%

---

# xAPI no Learning Manager

## O que é xAPI? {#whatisxapi}

A Experience API (xAPI) é uma especificação de software de e-learning que permite que o conteúdo de aprendizado e os sistemas de aprendizado se comuniquem entre si de maneira que registrem e rastreiem todos os tipos de experiências de aprendizado. As experiências de aprendizado são gravadas em um LRS (Armazenamento de Registros de Aprendizagem). Os LRSs podem existir em sistemas tradicionais de gerenciamento de aprendizagem (LMSs) ou por conta própria.

Para obter mais informações sobre a xAPI, consulte: [https://github.com/adlnet/xAPI-Spec](https://github.com/adlnet/xAPI-Spec).

## Como o Learning Manager oferece suporte à xAPI? {#howdoescaptivateprimesupportxapi}

O Learning Manager tem um Armazenamento de Registros de Aprendizagem incorparado. Esse LRS tem a capacidade total de aceitar instruções xAPI do conteúdo hospedado no Learning Manager. Ele até aceita instruções xAPI que terceiros geram. Essas instruções xAPI são armazenadas no Learning Manager e podem ser exportadas para fora do Learning Manager para serem visualizadas em qualquer sistema de data warehouse de terceiros.

## Quando usar a xAPI? {#whendoyouusexapi}

Cada vez mais, é necessário capturar experiências de aprendizado do usuário final que se estendem por vários sistemas.  Também é necessário rastrear o envolvimento exato do aluno com o conteúdo de treinamento. Ele vai além de Início, Em andamento e Conclusão (que são os únicos atributos capturados pelo SCORM).

## Uso da xAPI no Learning Manager {#usingxapiinprime}

## Configure o seu aplicativo {#setupyourapplication}

1. Faça logon como administrador de integração. Selecione **[!UICONTROL Aplicativos]** > **[!UICONTROL Registrar]**.

   ![](assets/appregistration.png)

1. Registre um novo aplicativo.

   ![](assets/appregistration.png)

1. Defina o escopo do aplicativo.

   * Se **[!UICONTROL Acesso de leitura e gravação xAPI da função de administrador]** estiver ativado, o administrador poderá publicar e obter instruções e documentos xAPI.
   * Se **[!UICONTROL Acesso de leitura e gravação xAPI da função do aluno]** estiver ativado, o administrador poderá publicar e obter instruções e documentos xAPI.

1. Salve a alterações. Você recebe sua ID de desenvolvedor e seu segredo.

**Pontos de extremidade**:

Clique no link abaixo para exibir o documento swagger xAPI:

[https://learningmanagereu.adobe.com/docs/primeapi/xapi/](https://learningmanagereu.adobe.com/docs/primeapi/xapi/)

Observação: a versão da xAPI compatível com o Learning Manager é 1.0.3.

## Autenticação da API {#apiauthentication}

A xAPI do Learning Manager usa a estrutura OAuth 2.0 para autenticar e autorizar os seus aplicativos cliente. Depois de registrar o aplicativo, você pode obter a clientId e o clientSecret. Obter URL é usado no navegador ao autenticar os usuários do Learning Manager usando suas contas pré-configuradas, como SSO e Adobe ID.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<admin:xapi or learner:xapi>&response_type=CODE.
```

## Rastreamento de instruções xAPI como OA do Learning Manager {#trackingxapistatementsasprimelo}

Como autor, agora você pode escolher o módulo xAPI ao criar cursos para monitorar a experiência do usuário fora do Learning Manager. Por exemplo, você pode usar esse recurso para avaliar as atividades dos usuários em uma plataforma de terceiros usada para a realização do curso.

1. Ao criar um **[!UICONTROL Módulo de Atividade]**, na opção **[!UICONTROL Tipo]**&#x200B;use o menu pop-up para selecionar o **[!UICONTROL Módulo baseado em xAPI.]**

   ![](assets/xapimodulecreation.png)

1. Você deve fornecer um IRI. Se não for fornecido, o Learning Manager gera um automaticamente.

   O IRI de uma atividade é exclusivo em uma conta. Ou seja, dois módulos no Learning Manager não podem ter o mesmo IRI. Um novo IRI é gerado nos seguintes casos:

   * Quando um curso com o módulo xAPI é compartilhado entre contas.
   * Quando uma certificação com o módulo xAPI for repetida



   Qualquer instrução xAPI com o IRI mencionado é rastreada no módulo acima e é refletida nos relatórios do Learning Manager.

1. Para copiar o IRI gerado automaticamente, veja novamente a página Módulo de atividade.
1. Publique o módulo.

**Pontos a observar:**

* No momento, o Learning Manager oferece suporte somente ao mbox como um identificador. Outros identificadores, incluindo mboz_sha1, openid, account, não são suportados.

* A stateId e a profileId são UUID quando usadas com o Learning Manager.
* A solicitação de PUT não substitui o documento para agentes/perfil xAPIs, atividade/perfil e atividade/estado
* O grupo não identificado não tem suporte no Ator.
* O parâmetro “related_activities” não tem suporte na instrução GET.
* Os parâmetros &#39;format=ids&#39; e &#39;format=canonical&#39; não são suportados em instruções GET.
* A anulação da instrução xAPI não desfaz as ações que ocorreram no Learning Manager quando a instrução foi publicada.

## Gerar relatórios {#generatereports}

Os relatórios xAPI podem ser gerados como relatórios do Excel. Como administrador, abra **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Relatório de atividades da xAPI]**.

O relatório baixado busca todas as informações publicadas pelo aluno e administrador para qualquer instrução.

Os mesmos relatórios podem ser gerados/agendados usando conectores FTP e Box para qualquer integração de terceiros. Siga estas etapas:

Faça logon como Administrador de integração > Abra o conector FTP/Box > Selecione o relatório de atividades da xAPI no painel esquerdo > Opte por agendar/gerar um relatório.

![](assets/xapischedule.png)

* Quando apenas a pontuação bruta é enviada na instrução xAPI sem pontuação máxima, a pontuação do quiz não é exibida no LT.

* Para obter a pontuação percentual no Learning Manager, as pontuações dimensionadas são enviadas por meio da xAPI.

## Relatório de exemplo {#samplereport}

[Relatório de xAPI de exemplo.](assets/xapireport8842560559890766717csv.zip)
