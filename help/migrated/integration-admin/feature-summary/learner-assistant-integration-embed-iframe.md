---
description: Saiba como incorporar o Assistente do aluno em seu aplicativo usando um iframe, incluindo configuração e manipulação de eventos
jcr-language: en_us
title: Integrar o Learner Assistant incorporando o iFrame
source-git-commit: 1549a4592b7a930631dcff6b2e75ec3a3d4f5592
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 1%

---


# Incorporação do Assistente do aluno usando um iframe

## Visão geral

Os usuários do Adobe Learning Manager (ALM) podem incorporar o **Assistente de aluno** diretamente em seus próprios aplicativos voltados para o aluno (por exemplo, portais personalizados, front-ends LMS, hubs de aprendizado etc.) usando um HTML padrão `<iframe>`.

Quando incorporado pelo iFrame, o Assistente do aluno fornece acesso a todos os recursos do Assistente do aluno, incluindo:

* Orchestrator
* Agente de resposta
* Agente de conhecimento
* Agente de caminhos de aprendizado

>[!IMPORTANT]
>
>A incorporação do iFrame dá ao seu aplicativo acesso total aos agentes subjacentes do Assistente do aluno. No entanto, seu aplicativo (o “aplicativo pai”) é responsável por lidar com quaisquer eventos que o assistente emita. Por exemplo, quando um aluno clica em uma citação ou em um link de curso dentro da resposta do assistente, ele emite um evento, e o aplicativo pai deve manipular esse evento e executar a navegação real. O Assistente do aluno não navega em nome do seu aplicativo.

## Pré-requisitos

Antes de começar, verifique se você tem:

* Um locatário do ALM com o Assistente do aluno ativado. Configure o(s) catálogo(s) necessário(s) na página de configurações do administrador.
* Um accessToken válido para autenticar a sessão do aluno (ou administrador). Para gerar um token de acesso, siga as instruções na página [Autenticação usando OAuth 2.0](https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20). A página inclui as etapas necessárias para autenticar e gerar o token de acesso necessário para continuar.
* A capacidade de incorporar um `<iframe>` em seu aplicativo e se comunicar com ele por meio da API postMessage do navegador.
* Propriedade de código front-end do aplicativo pai, pois o aplicativo deve ouvir e responder a mensagens do iFrame incorporado.

## Parâmetros de configuração do Learning Assistant

| Nome do Parâmetro | Valor | Descrição |
|---|---|---|
| hostName | learningmanager.adobe.com | Especifica o domínio do host para o aplicativo. |
| accessToken | token123 (token de acesso real) | Token usado para autenticar e autorizar a sessão do usuário. |

## Inicializar iFrame

Passe a configuração para o Assistente do aluno por meio da API postMessage, usando um handshake de configuração de iFrame incorporado.

1. O aplicativo pai incorpora o Assistente de Aprendizado como `<iframe>`.
2. Se nenhuma configuração baseada em URL for encontrada, o Learning Assistant enviará um evento ALM_CHAT_REQUEST_CONFIG ao aplicativo pai.
3. O aplicativo pai responde com um evento ALM_CHAT_CONFIG contendo a carga de configuração. Por exemplo:

   ```json
   {
     "hostName": "learningmanager.adobe.com",
     "accessToken": "token123",
     "openByDefault": false,
     "isAdmin": false
   }
   ```

4. Após a inicialização bem-sucedida, o Assistente do aluno renderiza e está pronto para uso.

## Resumo de eventos do iFrame

O Assistente do aluno e o aplicativo pai se comunicam por meio de eventos postMessage em ambas as direções.

### Eventos de saída (iFrame do Assistente do aluno para aplicativo principal)

| Nome do evento | Descrição | Parâmetros Aprovados |
|---|---|---|
| ALM_CHAT_OPENED | Acionado quando o chat é aberto. | -- |
| ALM_CHAT_CLOSED | Acionado quando o bate-papo é fechado. | -- |
| ALM_CHAT_LO_REDIRECT | Navegue até a página de visão geral do Caminho de aprendizado personalizado. | loId, loType, instanceId |
| ALM_CHAT_URL_REDIRECT | Acionado quando um link externo é clicado na mensagem do bate-papo. | url |
| ALM_CHAT_REQUEST_CONFIG | Solicita a configuração do aplicativo pai. | -- |
| ALM_CHAT_WAITING_FOR_REPLY | Indica que o assistente está processando uma solicitação ou aguardando uma resposta. | isWaitingForReply |
| ALM_CHAT_PERSONALIZED_PATH_CREATED | Acionado quando um caminho de aprendizado é salvo. | -- |

### Eventos de entrada (aplicativo pai para o Assistente do aluno)

| Nome do evento | Descrição | Carga |
|---|---|---|
| ALM_CHAT_CONFIG | Envia a carga de configuração necessária para inicializar o assistente. | Objeto de configuração |
| ALM_CHAT_OPEN | Abre o Assistente do aluno. | Nenhum |
| ALM_CHAT_CLOSE | Fecha o Assistente do aluno. | Nenhum |
| ASK_AI_ASSISTANT_QUERY | Abre a janela de bate-papo e envia uma consulta ao assistente. | { query: “Texto da pergunta” } |

## Requisitos de manipulação de eventos no aplicativo pai

A incorporação do Assistente do aluno por meio do iFrame não o torna um widget totalmente independente. Seu aplicativo pai deve ouvir ativamente eventos de saída e tomar a ação apropriada. No mínimo, seu aplicativo deve:

* Ouça ALM_CHAT_REQUEST_CONFIG e responda com ALM_CHAT_CONFIG para que o assistente possa inicializar.
* Manipular ALM_CHAT_LO_REDIRECT: quando um aluno clica em uma citação ou origem na resposta do assistente, seu aplicativo recebe o loId, o loType e o instanceId e é responsável por navegar pelo aluno para o curso ou objeto de aprendizado correto.
* Manipular ALM_CHAT_URL_REDIRECT: quando um aluno clica em um link externo em uma mensagem de bate-papo, seu aplicativo recebe o url e é responsável por abri-lo ou navegar até ele (por exemplo, em uma nova guia).
* Opcionalmente, rastreie ALM_CHAT_OPENED / ALM_CHAT_CLOSED / ALM_CHAT_WAITING_FOR_REPLY para refletir o estado do assistente em sua própria interface do usuário (por exemplo, mostrar um indicador de carregamento enquanto isWaitingForReply é verdadeiro).
* Opcionalmente, use ALM_CHAT_OPEN / ALM_CHAT_CLOSE / ASK_AI_ASSISTANT_QUERY para controlar o assistente programaticamente. Por exemplo, abrir o assistente e pré-preencher uma consulta de um botão da **Ajuda** em outro local do aplicativo.

## Precisa de ajuda?

Entre em contato com seu gerente de sucesso de clientes da Adobe para configurar um guia técnico.
