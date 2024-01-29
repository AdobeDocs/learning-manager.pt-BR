---
jcr-language: en_us
title: Integração do Learning Manager com o Slack
description: Integração do Learning Manager com o Slack
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---



# Integração do Learning Manager com o Slack

Nós temos **removido** **Slack** como um conector no Learning Manager. Você não terá mais acesso ao conector Slack.

Como usuário de Slack, você pode instalar o aplicativo Adobe Learning Manager do diretório de aplicativos Slack nas suas equipes de Slack e explorar o conteúdo do Learning Manager diretamente no Slack. Você pode interagir com o Primebot para pesquisar novos cursos, visualizar recomendações e obter notificações sobre futuros prazos de conclusão no Learning Manager. Você também pode se inscrever e ir diretamente para o seu aprendizado no Slack.

O aplicativo Learning Manager para Slack não tem suporte em uma instância do Azure no Learning Manager.

## Instalando o aplicativo Adobe Learning Manager {#installingadobecaptivateprimeapp}

Como aluno, você pode instalar o aplicativo CP Prime na sua conta Slack. Para instalar o aplicativo, na sua conta de Slack, abra o diretório do aplicativo e procure por Learning Manager. Baixe e instale o aplicativo Se o aplicativo não for aprovado em sua conta, entre em contato com o administrador de integração para obter aprovação. Se já estiver aprovado, você poderá fazer logon.

## Aprovando o logon do aluno como administrador de integração {#approvinglearnersigninasanintegrationadmin}

Como administrador de integração, para aprovar a permissão de um aluno para usar o aplicativo Prime no Slack, siga estas etapas.

1. Selecionar **[!UICONTROL Aplicativos]** no painel esquerdo e clique no botão **[!UICONTROL Aplicativos em destaque]** guia.

   ![](assets/featuredapps.jpg)

1. Clique no botão **[!UICONTROL Slack]** bloco > a página integração do slack é aberta. Clique em **[!UICONTROL Aprovar]** no canto superior direito para aprovar o aplicativo.

   ![](assets/approval.png)

1. Voltar para a página **[!UICONTROL Aplicativos]** página. Uma vez aprovado, o Slack deve aparecer na caixa **[!UICONTROL Aplicativos Externos]** guia.
1. Os alunos agora podem fazer logon na conta do Prime usando o Slack.

## Funcionalidades do Primebot {#primebotfunctionalities}

Agora você pode começar a interagir com o Primebot. Estas são as funcionalidades do bot.

1 - Comando

&#42;/prime&#42; pode ser usado para consultas pontuais relacionadas à sua conta do Adobe Learning Manager.

Os subcomandos disponíveis são:

/prime find `<query>` - pesquise cursos, certificações etc.

/prime recommend - mostra recomendações

/prime deadlines - mostra prazos vencidos e futuros

/prime enrollments - mostra inscrições

/prime skills - mostra habilidades

/prime notifications - mostra notificações

/prime catalogs - mostra catálogos

/prime invite - [Somente administrador] convide os usuários do Slack na equipe atual para experimentar o primebot

/prime profile- mostrar perfil

/prime logout - faça logoff da sua conta Prime nesta equipe Slack

/prime help - mostra mensagem de ajuda

2 - Recomendação

Você pode tentar uma frase como `show my recommendations` para obter uma lista personalizada de cursos recomendados, certificações e programas de aprendizado da sua conta do Adobe Learning Manager.

3 - Pesquisa

Você pode experimentar frases como `search for machine learning` ou `search for artificial intelligence`. É possível especificar o tipo de objeto de aprendizado usando frases como `search for machine learning certifications`, `search for artificial intelligence courses` ou `search for adobe photoshop job aids`. Você também pode pesquisar em um catálogo usando frases como `search for machine learning in Lynda catalog`.

4 - Prazos

Usar frase como `show my deadlines` para obter uma lista de prazos vencidos e futuros da sua conta do Adobe Learning Manager. Você pode filtrar prazos atrasados ou futuros com frases como `show my overdue deadlines` ou `show my upcoming deadlines`.
