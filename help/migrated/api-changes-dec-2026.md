---
description: Saiba como usar as configurações de assinatura do painel e as APIs de assinantes para configurar e-mails de resumo e gerenciar os assinantes do painel
jcr-language: en_us
title: Alterações na API em novembro de 2026
exl-id: 9b2d3856-810c-4352-bf18-667f698d4d70
source-git-commit: d1399781294a58f6ede8461878c979bd8b5edb34
workflow-type: tm+mt
source-wordcount: '5724'
ht-degree: 4%
---

# Alterações na API em dezembro de 2026

## APIs para notificações do professor do quadro de discussão

Este artigo descreve as novas APIs que oferecem suporte às notificações do professor do quadro de discussão. Use-os para inscrever professores e gerentes de coorte em painéis de discussão e controlar qual atividade aparece em seus emails de resumo.

### Sequência da API {#api-sequence}

As APIs se dividem em dois grupos. A API `boardSubscriptionSettings` funciona no nível da conta. A API de assinantes funciona no nível do quadro. Usar as APIs nesta sequência:

| Etapa | API | Finalidade | Escopo |
|---|---|---|---|
| 1 | [`POST /boardSubscriptionSettings`](#api-create-settings) | Defina as configurações no nível da conta. | `admin:write` |
| 2 | [`PATCH /boardSubscriptionSettings`](#api-update-settings) | Atualize as configurações no nível da conta. | `admin:write` |
| 3 | [`GET /boardSubscriptionSettings`](#api-get-settings) | Recupere as configurações no nível da conta. | `admin:read` |
| 4 | [`GET /boards/{id}/subscribers`](#api-get-subscribers) | Obtenha a lista de usuários inscritos em um painel. | `admin:read` |
| 5 | [`POST /boards/{id}/subscribers`](#api-subscribe-users) | Inscreva usuários em um painel. | `admin:write` |
| 6 | [`DELETE /boards/{id}/subscribers/{userId}`](#api-unsubscribe-user) | Cancelar a inscrição de um usuário em um painel. | `admin:write` |

### Autenticação e permissões

Qualquer pessoa que se autentique com o OAuth e tenha os escopos `admin:read` e `admin:write` pode chamar essas APIs. As APIs usam os seguintes escopos OAuth:

* `admin:read`: Listar assinantes e ler configurações de notificação (`GET` solicitações).
* `admin:write`: crie ou altere configurações de notificação e adicione ou remova assinantes (`POST`, `PATCH` e `DELETE` solicitações).

>[!NOTE]
>
>O acesso ao painel é verificado novamente quando uma notificação é enviada. Se um assinante perder o acesso a um painel, a entrega desse painel será ignorada, mas a assinatura será mantida. A entrega será retomada se o acesso retornar.

### Limites e considerações

* O número de assinantes que podem ser adicionados é limitado.
* O resumo é enviado como um único e-mail sem paginação e o corpo do e-mail tem um limite de tamanho. Para placas com atividade intensa, escolha uma frequência de resumo que mantenha cada e-mail gerenciável, como a cada 6 horas.
* Os links de resumo abrem a publicação, o comentário ou a resposta somente para os usuários que estão conectados.

## API para criar configurações no nível da conta {#api-create-settings}

### Finalidade da API {#purpose-create-settings}

Use esta API para definir as configurações no nível da conta para notificações de assinatura do painel pela primeira vez. As configurações controlam como os resumos de notificação são gerados na conta:

* Quais eventos do quadro de discussão geram notificações.
* Com que frequência os e-mails de resumo são enviados.
* Se posts, comentários, respostas e votos estão incluídos.

Para alterar as configurações depois, use [`PATCH /boardSubscriptionSettings`](#api-update-settings).

### Ponto de extremidade {#endpoint-create-settings}

```http
POST /primeapi/v2/boardSubscriptionSettings
```

| Propriedade | Valor |
|---|---|
| Escopo | `admin:write` |
| Formato de solicitação | `application/vnd.api+json;charset=UTF-8` |
| Formato da resposta | `application/vnd.api+json;charset=UTF-8` |

### Corpo da solicitação {#request-body-create-settings}

Enviar as configurações como atributos de um recurso `boardSubscriptionSettings`.

| Campo | Tipo | Descrição |
|---|---|---|
| `notifyNewPost` | booleano | Se os assinantes são notificados quando uma nova publicação é adicionada a um painel. |
| `notifyComment` | booleano | Se os assinantes são notificados quando um comentário é adicionado a uma postagem. |
| `notifyReply` | booleano | Se os assinantes são notificados quando uma resposta é adicionada a um comentário. |
| `digestFrequencyHours` | número inteiro | Frequência, em horas, em que o email de resumo é enviado. Os valores válidos variam de 1 a 168 (uma semana). Por exemplo, 24 envia uma compilação diária e 168 envia uma compilação semanal. |

### Solicitação de exemplo {#example-request-create-settings}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyNewPost": true,
      "notifyComment": true,
      "notifyReply": true,
      "digestFrequencyHours": 24
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Exemplo de resposta - 201 criado {#example-response-create-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Códigos de resposta {#response-codes-create-settings}

| Status | Significado |
|---|---|
| 201 | A solicitação foi bem-sucedida. As configurações no nível da conta foram criadas. |
| 400 | Um erro genérico de solicitação incorreta. |
| 401 | A solicitação não tem credenciais válidas ou o acesso foi negado devido a credenciais inválidas. |

## API para atualizar as configurações no nível de conta {#api-update-settings}

### Finalidade da API {#purpose-update-settings}

Use esta API para atualizar as configurações no nível de conta criadas com [`POST /boardSubscriptionSettings`](#api-create-settings). Por exemplo, altere a frequência de compilação ou ative ou desative um tipo de evento.

### Ponto de extremidade {#endpoint-update-settings}

```http
PATCH /primeapi/v2/boardSubscriptionSettings
```

| Propriedade | Valor |
|---|---|
| Escopo | `admin:write` |
| Formato de solicitação | `application/vnd.api+json;charset=UTF-8` |
| Formato da resposta | `application/vnd.api+json;charset=UTF-8` |

### Corpo da solicitação {#request-body-update-settings}

Envie os atributos que deseja alterar, no mesmo formato da API de criação: `notifyNewPost`, `notifyComment`, `notifyReply` e `digestFrequencyHours`. Os atributos que você não envia mantêm seus valores atuais. Para obter a descrição de cada atributo, consulte [API para criar configurações no nível de conta](#api-create-settings).

### Solicitação de exemplo {#example-request-update-settings}

```bash
curl -X PATCH \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriptionSettings",
    "attributes": {
      "notifyReply": true,
      "digestFrequencyHours": 12
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Exemplo de resposta - 200 OK {#example-response-update-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 12,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Códigos de resposta {#response-codes-update-settings}

| Status | Significado |
|---|---|
| 200 | A solicitação foi bem-sucedida. As configurações no nível da conta foram atualizadas e a resposta contém as configurações atuais. |
| 400 | Um erro genérico de solicitação incorreta. |
| 401 | A solicitação não tem credenciais válidas ou o acesso foi negado devido a credenciais inválidas. |

## API para recuperar configurações no nível da conta {#api-get-settings}

### Finalidade da API {#purpose-get-settings}

Quando os usuários assinam um painel, o Adobe Learning Manager pode notificá-los sobre a atividade nesse painel por meio de e-mails de resumo. As configurações no nível da conta determinam quais tipos de atividade acionam uma notificação e com que frequência o resumo é enviado.

Essa API permite recuperar essas configurações. Use-o para exibir a configuração de notificação atual em seu aplicativo ou para verificar as configurações antes de criar recursos que dependem delas.

### Ponto de extremidade {#endpoint-get-settings}

```http
GET /primeapi/v2/boardSubscriptionSettings
```

| Propriedade | Valor |
|---|---|
| Escopo | `admin:read` |
| Formato da resposta | `application/vnd.api+json;charset=UTF-8` |

### Solicitação de exemplo {#example-request-get-settings}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings'
```

### Exemplo de resposta - 200 OK {#example-response-get-settings}

```json
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/boardSubscriptionSettings"
  },
  "data": {
    "id": "1010",
    "type": "boardSubscriptionSettings",
    "attributes": {
      "digestFrequencyHours": 24,
      "notifyComment": true,
      "notifyNewPost": true,
      "notifyReply": true
    }
  }
}
```

### Esquema de recurso {#resource-schema-get-settings}

**`boardSubscriptionSettings`atributos**

| Campo | Tipo | Descrição |
|---|---|---|
| `notifyNewPost` | booleano | Se os assinantes são notificados quando uma nova publicação é adicionada a um painel. |
| `notifyComment` | booleano | Se os assinantes são notificados quando um comentário é adicionado a uma postagem. |
| `notifyReply` | booleano | Se os assinantes são notificados quando uma resposta é adicionada a um comentário. |
| `digestFrequencyHours` | número inteiro | Frequência, em horas, em que o email de resumo é enviado. Os valores válidos variam de 1 a 168 (uma semana). Use esse valor para informar aos usuários com que frequência esperar o e-mail de resumo. Por exemplo, mostre “Daily” quando o valor for 24 e “Weekly” quando o valor for 168. |

### Códigos de resposta {#response-codes-get-settings}

| Status | Significado |
|---|---|
| 200 | A solicitação foi bem-sucedida. A resposta contém as configurações de assinatura do quadro no nível da conta. |
| 400 | Um erro genérico de solicitação incorreta. |
| 401 | A solicitação não tem credenciais válidas ou o acesso foi negado devido a credenciais inválidas. |

### Usar esta API na integração {#integration-get-settings}

Um caso de uso comum é uma tela de preferências de notificação que mostra como os emails de assinatura do painel são configurados para a conta.

1. Quando a tela de preferências de notificação do seu aplicativo carregar, ligue para `GET /boardSubscriptionSettings`.
1. Mostrar quais tipos de atividade acionam uma notificação e com que frequência o email de resumo é enviado, usando os valores na resposta.

## API para recuperar assinantes do painel {#api-get-subscribers}

### Finalidade da API {#purpose-get-subscribers}

Recupera a lista de usuários inscritos em um painel específico. Os usuários inscritos em um painel são notificados sobre novas atividades nesse painel. Essa API retorna os usuários que estão atualmente inscritos em determinado painel, juntamente com detalhes sobre quando e por quem cada assinatura foi criada.

Use essa API para exibir uma lista de assinantes em seu aplicativo, para auditar quem recebe atualizações de um painel ou para sincronizar dados de assinatura do painel com um sistema externo.

A resposta é paginada. Use os parâmetros de consulta `page[offset]` e `page[limit]` para se mover por listas grandes de assinantes. Os dados retornados estão sujeitos às permissões do usuário chamador no quadro solicitado.

### Ponto de extremidade {#endpoint-get-subscribers}

```http
GET /primeapi/v2/boards/{id}/subscribers
```

| Propriedade | Valor |
|---|---|
| Escopo | `admin:read` |
| Formato da resposta | `application/vnd.api+json;charset=UTF-8` |

### Parâmetros {#parameters-get-subscribers}

| Parâmetro | Em | Obrigatório | Padrão | Descrição |
|---|---|---|---|---|
| `id` | caminho | Sim | N/A | A ID do painel cujos assinantes você deseja recuperar. O acesso está sujeito às permissões do chamador no quadro. |
| `page[offset]` | consulta | Não | 0 | A posição inicial dos registros a serem retornados. |
| `page[limit]` | consulta | Não | 10 | O número de assinantes a retornar por página. O valor máximo permitido é 200. |

### Solicitação de exemplo {#example-request-get-subscribers}

```bash
curl -X GET \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers?page[offset]=0&page[limit]=50'
```

### Exemplo de resposta - 200 OK {#example-response-get-subscribers}

```json
{
  "data": [
    {
      "id": "1234:5678",
      "type": "boardSubscriber",
      "attributes": {
        "boardId": 1234,
        "dateSubscribed": 1757000000000,
        "subscribedByUserId": 5678,
        "user": {
          "id": "5678",
          "name": "Jane Doe",
          "email": "jane.doe@example.com",
          "avatarUrl": "https://example.com/avatars/5678.png",
          "bio": "Learning enthusiast",
          "contentLocale": "en-US",
          "uiLocale": "en-US",
          "timeZoneCode": "PST",
          "userType": "INTERNAL",
          "state": "ACTIVE",
          "profile": "Learner",
          "roles": ["Learner"],
          "gamificationEnabled": true,
          "pointsEarned": 120,
          "pointsRedeemed": 20,
          "enrollOnClick": true,
          "preferredResolution": "720p",
          "lastLoginDate": "2026-09-23T18:12:04.000Z"
        }
      }
    }
  ]
}
```

### Esquema de recurso {#resource-schema-get-subscribers}

A resposta inclui um novo recurso, `boardSubscriber`. Seus atributos incluem `boardId`, `dateSubscribed`, `subscribedByUserId` e `user`. O objeto de usuário incorporado tem informações de assinante, como ID de usuário, nome, email, perfil e funções, além de outros metadados de usuário.

**`boardSubscriber`atributos**

| Campo | Tipo | Descrição |
|---|---|---|
| `id` | cadeia de caracteres | ID de assinatura opaca. |
| `type` | cadeia de caracteres | O tipo de recurso. |
| `boardId` | número | ID do painel ao qual o usuário está inscrito. |
| `dateSubscribed` | número | Carimbo de data e hora de quando o usuário se inscreveu no painel. |
| `subscribedByUserId` | número | ID do usuário que criou a assinatura. |
| `user` | objeto | Detalhes do usuário inscrito (incorporado, veja abaixo). |

**`user`(inserido, dentro de um assinante)**

| Campo | Tipo | Descrição |
|---|---|---|
| `id` | cadeia de caracteres | ID de usuário opaca. |
| `name` | cadeia de caracteres | Nome de exibição do usuário. |
| `email` | cadeia de caracteres | Endereço de email do usuário. |
| `avatarUrl` | cadeia de caracteres | URL da imagem do perfil do usuário. |
| `bio` | cadeia de caracteres | Breve biografia do usuário. |
| `binUserId` | cadeia de caracteres | Identificador interno do usuário. |
| `userUniqueId` | cadeia de caracteres | Identificador exclusivo do usuário na conta. |
| `userType` | cadeia de caracteres | Tipo de usuário, por exemplo, interno ou externo. |
| `state` | cadeia de caracteres | Estado atual da conta de usuário. |
| `profile` | cadeia de caracteres | Perfil atribuído ao usuário. |
| `roles` | matriz de strings | Funções mantidas pelo usuário. |
| `contentLocale` | cadeia de caracteres | Local no qual o usuário prefere exibir o conteúdo. |
| `uiLocale` | cadeia de caracteres | Localidade usada para a interface do usuário. |
| `timeZoneCode` | cadeia de caracteres | Fuso horário configurado para o usuário. |
| `preferredResolution` | cadeia de caracteres | Resolução de vídeo preferencial do usuário. |
| `enrollOnClick` | booleano | Se o usuário é automaticamente inscrito ao selecionar um objeto de aprendizado. |
| `gamificationEnabled` | booleano | Se a gamificação está habilitada para o usuário. |
| `pointsEarned` | número | Total de pontos de gamificação obtidos pelo usuário. |
| `pointsRedeemed` | número | Total de pontos de gamificação resgatados pelo usuário. |
| `lastLoginDate` | cadeia de caracteres | Data e hora do logon mais recente do usuário. |
| `fields` | objeto | Campos de usuário personalizados e seus valores. |
| `metadata` | objeto | Metadados adicionais associados ao usuário. |

### Códigos de resposta {#response-codes-get-subscribers}

| Status | Significado |
|---|---|
| 200 | A solicitação foi bem-sucedida. A resposta contém os assinantes do painel. |
| 400 | Um erro genérico de solicitação incorreta. Por exemplo, o ID do painel ou um valor de paginação está malformado. |
| 401 | A solicitação não tem credenciais válidas ou o acesso foi negado devido a credenciais inválidas. |

### Usar esta API na integração {#integration-get-subscribers}

Um caso de uso comum é uma exibição de administrador ou moderador que mostra todos que recebem atualizações de um painel.

1. Quando a exibição carregar, chame este ponto de extremidade com a ID da placa e um valor `page[limit]` adequado ao seu layout (até 200).
1. Exiba os valores `user.name`, `user.email` e `dateSubscribed` para cada assinante.
1. Se o número de registros retornados for igual a `page[limit]`, talvez haja mais assinantes. Chame o ponto de extremidade novamente, aumentando `page[offset]` pelo tamanho da página, até que uma página retorne menos registros do que o solicitado.

## API para inscrever usuários em um painel {#api-subscribe-users}

### Finalidade da API {#purpose-subscribe-users}

Inscreva um ou mais usuários em um quadro de discussão para que eles recebam e-mails de resumo sobre isso. Identifique os usuários por ID de usuário, endereço de email (resolvido para IDs de usuário na conta) ou ambos. Você pode adicionar vários usuários em uma única solicitação. Consulte [Assinaturas em massa](#bulk-subscriptions).

### Ponto de extremidade {#endpoint-subscribe-users}

```http
POST /primeapi/v2/boards/{id}/subscribers
```

| Propriedade | Valor |
|---|---|
| Escopo | `admin:write` |
| Formato de solicitação | `application/vnd.api+json;charset=UTF-8` |
| Formato da resposta | `application/vnd.api+json;charset=UTF-8` |

### Parâmetros {#parameters-subscribe-users}

| Parâmetro | Em | Obrigatório | Descrição |
|---|---|---|---|
| `id` | caminho | Sim | A ID do painel no qual inscrever usuários. |

### Corpo da solicitação {#request-body-subscribe-users}

Enviar os usuários como atributos de um recurso `boardSubscriberBulkRequest`. Pelo menos um de `userIds` ou `emails` é necessário.

| Campo | Tipo | Descrição |
|---|---|---|
| `data.attributes.userIds` | matriz de números | As IDs dos usuários a serem inscritos. |
| `data.attributes.emails` | matriz de strings | Os endereços de email dos usuários a serem inscritos. Cada endereço é resolvido para uma ID de usuário na conta. |

### Solicitação de exemplo {#example-request-subscribe-users}

```bash
curl -X POST \
--header 'Content-Type: application/vnd.api+json;charset=UTF-8' \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
-d '{
  "data": {
    "type": "boardSubscriberBulkRequest",
    "attributes": {
      "userIds": [
        1234,
        5678
      ],
      "emails": [
        "abc@xyz.com"
      ]
    }
  }
}' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1010/subscribers'
```

### Exemplo de resposta - 207 Status Múltiplo {#example-response-subscribe-users}

```json
{
  "added": [
    {
      "userId": "12345",
      "status": "SUCCESS"
    }
  ],
  "failed": [
    {
      "userId": "78910",
      "errorCode": "NO_BOARD_ACCESS"
    }
  ]
}
```

**Atributos de resposta**

| Campo | Tipo | Descrição |
|---|---|---|
| `added` | matriz | Os usuários que foram inscritos. Cada entrada tem um `userId` e um `status`. Os usuários que já foram inscritos também são informados aqui como bem-sucedidos. |
| `failed` | matriz | Os usuários que não puderam ser inscritos. Cada entrada tem um `userId` e um `errorCode`, por exemplo `NO_BOARD_ACCESS`. |

### Códigos de resposta {#response-codes-subscribe-users}

| Status | Significado |
|---|---|
| 207 | Status Múltiplo. A solicitação foi processada e a resposta lista o resultado de cada usuário em `added` e `failed`. |
| 400 | Um erro genérico de solicitação incorreta. |
| 401 | A solicitação não tem credenciais válidas ou o acesso foi negado devido a credenciais inválidas. |
| 404 | O recurso solicitado, como o painel, não foi encontrado. |
| 409 | O painel está inativo, excluído ou desativado; portanto, a solicitação inteira será rejeitada. |

### Assinaturas em massa {#bulk-subscriptions}

Use a assinatura em massa para adicionar vários usuários a um quadro de discussão em uma única solicitação. A assinatura em massa ajuda a reduzir o número de chamadas de API necessárias para gerenciar assinantes. É útil quando:

* Um professor gerencia várias coortes.
* Um gerente de coorte precisa ter acesso a muitos painéis de discussão.
* Um sistema externo sincroniza as assinaturas da placa em lote.
* Vários professores precisam ser inscritos durante a criação da coorte.

#### Comportamento de adição em massa

Uma solicitação em massa pode conter IDs de usuário, endereços de email ou uma combinação de ambos. Cada usuário é processado de forma independente.

#### Comportamento idempotente

A adição em massa é impotente. Se um usuário já estiver inscrito no painel, a solicitação será bem-sucedida, nenhuma assinatura duplicada será criada e a assinatura existente permanecerá inalterada. Isso permite que os clientes repitam as solicitações com segurança.

#### Êxito parcial

Alguns usuários podem ser inscritos enquanto outros falham na validação. A operação não falha porque um ou mais usuários são inválidos.

| Caixa | Resultado |
|---|---|
| O usuário existe e tem acesso ao painel | Êxito |
| O usuário já está inscrito | Êxito |
| O usuário não tem acesso ao painel | Falha (`NO_BOARD_ACCESS`) |
| O usuário não existe | Falha |
| O usuário está inativo | Falha |
| O usuário foi excluído | Falha |

#### Formato da resposta

A assinatura em massa retorna o Status Múltiplo HTTP 207 com um resultado `added` e um resultado `failed` para cada usuário, como no [exemplo de resposta](#example-response-subscribe-users).

#### Falhas comuns de validação

* **O usuário não tem acesso ao painel.** Se um usuário não tiver visibilidade do painel, `NO_BOARD_ACCESS` será retornado para esse usuário. Os usuários restantes continuam a ser processados normalmente.
* **O painel está inativo, excluído ou desativado.** Se o painel não estiver qualificado para assinaturas, a solicitação será rejeitada com Conflito HTTP 409.
* **O usuário é inválido.** Se uma conta de usuário não existir, estiver inativa ou tiver sido excluída, a operação retornará uma entrada com falha para esse usuário.

## API para cancelar a inscrição de um usuário em um painel {#api-unsubscribe-user}

### Finalidade da API {#purpose-unsubscribe-user}

Cancelar a inscrição de um usuário em um quadro de discussão. Depois que a assinatura é removida, o usuário não recebe mais notificações e e-mails de resumo para esse painel.

### Ponto de extremidade {#endpoint-unsubscribe-user}

```http
DELETE /primeapi/v2/boards/{id}/subscribers/{userId}
```

| Propriedade | Valor |
|---|---|
| Escopo | `admin:write` |
| Formato da resposta | `application/vnd.api+json;charset=UTF-8` |

### Parâmetros {#parameters-unsubscribe-user}

| Parâmetro | Em | Obrigatório | Descrição |
|---|---|---|---|
| `id` | caminho | Sim | A ID do painel. |
| `userId` | caminho | Sim | A ID do usuário cuja assinatura será cancelada. |

### Solicitação de exemplo {#example-request-unsubscribe-user}

```bash
curl -X DELETE \
--header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://learningmanager.adobe.com/primeapi/v2/boards/1234/subscribers/5678'
```

### Exemplo de resposta - 204 Sem conteúdo {#example-response-unsubscribe-user}

A resposta não tem corpo.

### Códigos de resposta {#response-codes-unsubscribe-user}

| Status | Significado |
|---|---|
| 204 | A solicitação foi bem-sucedida. A inscrição do usuário foi cancelada no painel. |
| 400 | Um erro genérico de solicitação incorreta. |
| 401 | A solicitação não tem credenciais válidas ou o acesso foi negado devido a credenciais inválidas. |
| 404 | O recurso solicitado, como o painel ou a assinatura, não foi encontrado. |

## Pedidos de API de marcador e manipulação de conteúdo desativado

### Finalidade da API

Os alunos marcam os treinamentos que desejam revisitar. Antes dessa alteração, as APIs de marcadores não retornavam marcadores em uma ordem específica. As integrações, especialmente as implementações sem periféricos, não puderam mostrar primeiro os marcadores salvos mais recentemente. Os alunos com muitos marcadores tinham de percorrer itens mais antigos para encontrar itens recentes.

Os marcadores dos objetos de aprendizado retirados também permaneciam na lista. Selecionar um levou a um erro de “Página não encontrada”.

Essa alteração melhora as APIs dos marcadores de duas maneiras:

* Os marcadores são retornados em ordem cronológica, os mais recentes primeiro.
* Os marcadores dos objetos de aprendizado retirados não são mais retornados.

Nenhum novo ponto final, parâmetro ou atributo de resposta foi introduzido. As integrações existentes continuam a funcionar sem alterações.

### URL base e convenções

As APIs de marcadores usam o seguinte caminho base e convenções:

| Item | Valor |
|---|---|
| Caminho base | `/primeapi/v2` |
| Tipo de conteúdo | `application/vnd.api+json` |
| Autenticação | Token OAuth com acesso de leitura do aluno |
| Ordem padrão | Indicador mais recente primeiro |
| Novos parâmetros | Nenhum |
| Estrutura de resposta | Inalterado |

### Pontos de extremidade

#### Pontos de extremidade que retornam marcadores

Os pontos de extremidade a seguir retornam marcadores na nova ordem:

| Ponto de extremidade | Devoluções |
|---|---|
| `GET /primeapi/v2/learningObjects?filter.bookmarks=true` | Objetos de aprendizado marcados pelo aluno |
| `GET /primeapi/v2/bookmarks` | Os marcadores do aluno |

#### Obter objetos de aprendizado marcados em ordem

`GET /primeapi/v2/learningObjects?filter.bookmarks=true`

<!-- Content Review by Claude: Please confirm the endpoint list. The dev-to-QE hand-off confirms ordering for GET /learningObjects?filter.bookmarks=true. The PRD (ALMER-442) also lists GET /primeapi/v2/bookmarks. Please also confirm the OAuth scope. -->

Retorna os objetos de aprendizado marcados pelo aluno chamador. O item marcado mais recentemente é o primeiro item e o mais antigo é o último.

**Escopo:** acesso de leitura do aluno

O ponto de extremidade aceita o seguinte parâmetro de consulta:

| Parâmetro | Em | Obrigatório | Descrição |
|---|---|---|---|
| `filter.bookmarks` | consulta | Sim | Defina como `true` para retornar apenas os objetos de aprendizado marcados pelo aluno |

**Solicitação de exemplo**

```http
GET /primeapi/v2/learningObjects?filter.bookmarks=true
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

**Resposta OK de exemplo 200**

O aluno marcou Introdução ao Adobe Analytics primeiro, Criação de projetos do espaço de trabalho em segundo lugar e Segmentação avançada no Adobe Analytics por último. A resposta os lista do mais recente para o mais antigo. Outros atributos são omitidos por serem breves.

```json
{
  "data": [
    {
      "id": "course:2400162",
      "type": "learningObject",
      "attributes": {
        "name": "Advanced Segmentation in Adobe Analytics"
      }
    },
    {
      "id": "course:2400160",
      "type": "learningObject",
      "attributes": {
        "name": "Building Workspace Projects"
      }
    },
    {
      "id": "course:2400159",
      "type": "learningObject",
      "attributes": {
        "name": "Getting Started with Adobe Analytics"
      }
    }
  ]
}
```

>[!NOTE]
>
>A nova ordem é o comportamento padrão e se aplica a todas as contas.

### Ordenação dos favoritos

#### Como os marcadores são ordenados

Os marcadores são classificados pela data em que foram salvos pelo aluno, do mais recente para o mais antigo. Por exemplo, se um aluno marcar o curso A, depois o curso B e, em seguida, o curso C, a resposta listará o curso C primeiro, o curso B segundo e o curso A último.

Se um OA marcado aparecendo na 10ª posição, por exemplo, for “não salvo” e depois marcado novamente, ele aparecerá como marcado recentemente e no início da lista.

As integrações que classificaram marcadores anteriormente no cliente podem remover essa lógica e exibir os resultados na ordem retornada.

### Manipulação de conteúdo desativada

#### Como os objetos de aprendizado retirados são tratados

Os marcadores dos objetos de aprendizado retirados não são retornados na resposta, independentemente de o aluno estar ou não inscrito no objeto de aprendizado.

Os objetos de aprendizado retirados marcados não aparecerão, a menos que o aluno esteja inscrito neles.

Os alunos não veem mais os marcadores que levam ao erro “Página não encontrada”. O marcador fica oculto dos resultados, e não excluído.

### Compatibilidade

Essa alteração não interrompe os consumidores existentes de API:

* Os pontos finais e seus parâmetros permanecem inalterados.
* A estrutura da resposta permanece inalterada e nenhum atributo é adicionado ou removido.
* Apenas a ordem dos resultados e a exclusão dos objetos de aprendizado retirados diferem do comportamento anterior.

### Usar esta API na integração

Um caso de uso comum é uma lista “Salvo para mais tarde” em uma experiência de aluno sem periféricos. Você quer que os alunos vejam seus marcadores mais recentes primeiro, sem links para o conteúdo retirado.

1. Ligue para `GET /primeapi/v2/learningObjects?filter.bookmarks=true` quando o aluno abrir a lista.
2. Exiba os objetos de aprendizado na ordem retornada. O primeiro item é o marcador mais recente.
3. Remova qualquer classificação do lado do cliente ou filtragem de conteúdo desativado que você adicionou como solução alternativa.
4. Mostrar uma contagem de marcadores usando o número de itens na resposta. Os marcadores dos objetos de aprendizado retirados não estão mais incluídos.

### Suporte de API para instâncias com várias inscrições no widget de conformidade do aluno no aplicativo do aluno

A API pública suporta esse comportamento por meio de um parâmetro de consulta opcional no endpoint de inscrições existente. Se você omitir o parâmetro, a API retornará os mesmos resultados de antes, portanto as integrações existentes, incluindo implementações sem periféricos, continuarão funcionando inalteradas.

**Objetivo final**

GET /primeapi/v2/enrollments

**Parâmetro de consulta**

includeMultiInstanceEnrollments (opcional)

**Consulta**

https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&filter.loTypes=course&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&sort=dateEnrollments

Valor **1&rbrace;**

verdadeiro. Falso por padrão.

**Corpo da resposta**

&lbrace;

“links”: &lbrace;

“self”: “[https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnroll&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true)”,

“next”: “[https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page\[limit\]=10&amp;filter.loTypes=course&amp;sort=dateEnroll&amp;includeHierarchicalEnrollments=false&amp;includeMultiInstanceEnrollments=true&amp;page\[cursor\]=eyJb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjEwLCJsZWFybmb1luZ](https://learningmanagerstage1.adobe.com/primeapi/v2/enrollments?page%5blimit%5d=10&filter.loTypes=course&sort=dateEnrolled&includeHierarchicalEnrollments=false&includeMultiInstanceEnrollments=true&page%5bcursor%5d=eyJjb3Vyc2VNdWx0aSI6MCwiam9iQWlkIjowLCJjb3Vyc2UiOjEwLCJsZWFybmluZ1Byb2dyYW0iOjAsImNlcnRpZmljYXRpb24iOjB9)

&rbrace;,

“data”: \&lbrack;

&lbrace;

“id”: “course:15067_30122_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“completionDeadline”: “2026-02-24T10:50:45.000Z”,

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:15067”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:15067_30122”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:15067_30122_41715_1_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:1108800_1997400_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“enrollmentSource”: “SELF_ENROLL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:1108800”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:1108800_1997400”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:1108800_1997400_2174574_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:2027668_3707328_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:2027668”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:2027668_3707328”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:2027668_3707328_2665897_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:2030067_3709862_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:2030067”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:2030067_3709862”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:2030067_3709862_2668467_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:3081896_5749155_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:3081896”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:3081896_5749155”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:3081896_5749155_3737554_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;,

&lbrace;

“id”: “course:3081896_5749155_3737555_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:2037893_3717940_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:2037893”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:2037893_3717940”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:2037893_3717940_3676856_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:3049434_5713130_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“completedDeadline”: “2020-05-05T18:29:59.000Z”,

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:3049434”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:3049434_5713130”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:3049434_5713130_3693595_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:2001397_3679403_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:2001397”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:2001397_3679403”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:2001397_3679403_2635974_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:2037862_3717900_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“enrollmentSource”: “MGR_APPROVAL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “PENDING_APPROVAL”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:2037862”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:2037862_3717900”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:2037862_3717900_3676816_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;,

&lbrace;

“id”: “course:2037837_3717863_3400468”,

“type”: “learningObjectInstanceEnrollment”,

“attributes”: &lbrace;

“completionDeadline”: “2020-02-29T18:29:59.000Z”,

“enrollmentSource”: “SELF_ENROLL”,

“hasPassed”: false,

“progressPercent”: 0,

“score”: 0,

“state”: “OTHER”

&rbrace;,

“relationship”: &lbrace;

“learner”: &lbrace;

“data”: &lbrace;

“id”: “3400468”,

“type”: “user”

&rbrace;

&rbrace;,

“learningObject”: &lbrace;

“data”: &lbrace;

“id”: “course:2037837”,

“type”: “learningObject”

&rbrace;

&rbrace;,

“loInstance”: &lbrace;

“data”: &lbrace;

“id”: “course:2037837_3717863”,

“type”: “learningObjectInstance”

&rbrace;

&rbrace;,

“loResourceGrades”: &lbrace;

“data”: \&lbrack;

&lbrace;

“id”: “course:2037837_3717863_3597363_0_3400468”,

“type”: “learningObjectResourceGrade”

&rbrace;

\&rbrack;

&rbrace;

&rbrace;

&rbrace;

\&rbrack;

&rbrace;

## Data do último acesso para inscrição no caminho de aprendizado {#last-access-date-lp-enrollment}

O Adobe Learning Manager permite armazenar metadados personalizados, como uma data de último acesso, em uma inscrição no caminho de aprendizado. Você define e lê os metadados por meio da API. Isso ajuda a rastrear o acesso limitado no tempo aos caminhos de aprendizado atribuídos.

## Sobre os metadados de inscrição do caminho de aprendizado

Você já pode definir uma data de último acesso em uma inscrição do curso por meio da API. Essa data controla por quanto tempo um aluno pode acessar o curso. As inscrições no caminho de aprendizado agora suportam um campo de metadados genérico, portanto, você pode armazenar uma data de último acesso ou qualquer outro valor que queira rastrear.

Não é necessário ativar o campo ou enviar um cabeçalho especial. O campo ficará vazio até você defini-lo.

>[!NOTE]
>
>Os metadados são para seu próprio rastreamento. O Adobe Learning Manager não o atualiza quando os alunos abrem uma programação de aprendizado ou seus cursos e não controla o acesso à programação. Também não é propagado para os cursos no caminho. Cada curso mantém sua própria data de último acesso, portanto, os cursos no mesmo caminho podem ter datas diferentes. Continue gerenciando a expiração do acesso em nível de curso separadamente.

### Regras de metadados {#metadata-rules}

* O valor deve ser um objeto JSON. Uma cadeia de caracteres, número, Booleano ou matriz retorna um erro 400 com a mensagem `metadata must be a JSON object`.
* Você pode usar qualquer tecla. O Adobe Learning Manager não valida chaves ou valores e não impõe um formato de data. Os exemplos neste artigo usam milissegundos de época, o mesmo formato das datas do curso.
* Uma solicitação PATCH substitui todo o objeto de metadados. Ele não é mesclado com os valores existentes, de modo que as teclas que você deixar de fora são removidas.
* A configuração `"metadata": null` limpa todos os metadados e retorna 200.
* Uma solicitação com um objeto `attributes` vazio, ou sem uma chave `metadata`, deixa os metadados armazenados inalterados.
* Quando nenhum metadado estiver definido, ou depois de limpá-lo, a chave `metadata` não estará na resposta.

## Definir metadados em uma inscrição existente

Use um token de administrador.

Envie uma solicitação PATCH para o seguinte ponto de extremidade, onde `{enrollmentId}` é a ID de inscrição do caminho de aprendizado no formato `learningProgram:<lpId><instanceId><userId>`:

```
PATCH /primeapi/v2/users/{userId}/enrollments/{enrollmentId}
```

Usar este corpo de solicitação:

```json
{
  "data": {
    "id": "<enrollmentId>",
    "type": "learningObjectInstanceEnrollment",
    "attributes": {
      "metadata": {
        "lastAccessDate": 1745337600000
      }
    }
  }
}
```

### Definir metadados ao inscrever um aluno

Use um token de administrador.

Envie uma solicitação de POST com o caminho de aprendizado e as IDs de instância. Inclua um objeto `metadata` opcional no corpo da solicitação.

```
POST /primeapi/v2/users/{userId}/enrollments?loId=<lpId>&loInstanceId=<instanceId>
```

* Se `metadata` não for um objeto JSON, a solicitação retornará 400 e o usuário não será inscrito.
* Se o usuário já estiver inscrito, a solicitação retornará 200 e não alterará nada. Para alterar os metadados de uma inscrição existente, use a solicitação PATCH.
* A resposta não inclui os metadados. Envie uma solicitação GET para lê-la.

### Recuperar metadados

Você pode recuperar metadados com um administrador ou um token do aluno. As solicitações diferem por tipo de token.

| Token | Obter uma inscrição | Listar inscrições no caminho de aprendizado |
|---|---|---|
| Administrador | `GET /primeapi/v2/users/{userId}/enrollments/{enrollmentId}` | `GET /primeapi/v2/users/{userId}/enrollments?filter.loTypes=learningProgram` |
| Aluno | `GET /primeapi/v2/enrollments/{enrollmentId}`<br>`GET /primeapi/v2/learningObjects/{id}?include=enrollment` | `GET /primeapi/v2/enrollments?filter.loTypes=learningProgram` |

>[!NOTE]
>
>O parâmetro `include=enrollment` funciona apenas com um token de aluno. Não há suporte para ela na função de administrador.

A resposta retorna o objeto `metadata` com a inscrição no caminho de aprendizado.

### Usar metadados em portais externos e sem periféricos

Portais e integrações externos usam as mesmas chamadas de API. Use a solicitação correspondente ao token usado por seu portal.

* **Mostrar o valor em seu portal:** envie a solicitação GET para o seu tipo de token da tabela acima e leia o objeto `metadata` da resposta.
* **Atualize o valor de um sistema externo, como uma plataforma de comércio:** envie a solicitação de PATCH com um token de administrador.

## API de trabalho: exportar relatórios de Report Builder com generateCustomReport

A versão de dezembro de 2026 do Adobe Learning Manager adiciona um novo tipo de trabalho, `generateCustomReport`, à API de trabalho. Use-o para exportar qualquer relatório criado no Report Builder, de forma automatizada, passando a ID do relatório.

Combinado com o novo conjunto de dados do questionário L2 em Report Builder, agora você pode:

* Exporte dados do questionário em nível de pergunta (N2) em vários cursos e módulos em um único relatório, em vez de executar `generateQuizReport` uma vez para cada curso.
* Automatize as exportações recorrentes, por exemplo, uma exportação incremental diária para o data warehouse ou a ferramenta de BI.

Os tipos de trabalho existentes, incluindo `generateQuizReport`, não foram alterados.

### Antes de começar

* Você deve ser um administrador. O tipo de trabalho `generateCustomReport` não está disponível para outras funções.
* Crie e salve o relatório no Report Builder primeiro. Para dados do quiz L2, crie o relatório a partir do conjunto de dados do quiz L2 e inclua os campos de nível de pergunta necessários, como texto da pergunta, resposta do aluno, pontuação, número da tentativa e data da resposta.
* Anote a ID do relatório. Você o transmitiu na solicitação como `reportId`.

### Criar um trabalho

**Objetivo final**

```
POST /primeapi/v2/jobs
```

**Corpo da solicitação**

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "description": "Daily L2 quiz export",
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      }
    }
  }
}
```

**Atributos**

| Atributo | Obrigatório | Descrição |
|---|---|---|
| `jobType` | Sim | Deve ser `generateCustomReport`. |
| `payload.reportId` | Sim | A ID do relatório de Report Builder salvo, como uma cadeia de caracteres. Deve ser um inteiro positivo, passado como uma cadeia de caracteres, por exemplo `"1478"`. O envio de um número, 0, um valor negativo, um valor decimal ou um valor vazio retorna um erro. |
| `description` | Não | Uma descrição da sua escolha para o job. |
| `callbackUrl` | Não | Um URL a ser chamado quando o trabalho for concluído. Funciona da mesma maneira que para outros tipos de trabalho. |
| `payload.filters` | Não | Consulte a seção abaixo. |

### Substituir o filtro de data (opcional) {#override-date-filter}

```json
"payload": {
  "reportId": "1478",
  "filters": [
    { "columnName": "L2 Quiz - Response - Timestamp", "operator": "gte", "val": "2026-11-15T00:00:00.000Z" }
  ]
}
```

* Substitui o filtro de data salva do relatório somente para esta execução. A exportação abrange `val` (inclusive) até o momento em que o trabalho é executado.
* `columnName` usa o formato `<Dataset name> - <Field name>`. Ele deve corresponder a um filtro de data que já existe no relatório. Não diferencia maiúsculas de minúsculas, mas o espaçamento e os hifens devem corresponder exatamente.
* `operator` é opcional e apenas `gte` é permitido.
* `val` é uma hora UTC ISO 8601 nos últimos 7 dias. Os tempos são truncados no segundo.
* Você pode substituir várias colunas. Uma lista vazia significa que os filtros salvos são usados.
* Caso de uso: uma exportação incremental diária que começa onde a anterior terminou.

### Erros retornados ao criar um job

| Causa | Mensagem |
|---|---|
| `reportId` ausente | `reportId is required` |
| `reportId` não é uma cadeia de caracteres inteira positiva | `reportId must be a positive integer string` |
| A data não está no formato ISO | `filters.val must be in ISO format, e.g. 2020-01-01T18:30:00.000Z` |
| Data anterior a 7 dias ou no futuro | `filters.val must be within the last 7 days` |
| Operador diferente de `gte` | `filters.operator must be gte` |
| Mesma coluna dada duas vezes | `Duplicate filter column: <column>` |
| A coluna não é um filtro no relatório | `Unsupported custom report filter column: <column>` |
| Um trabalho para o mesmo relatório ainda está em execução | `There exists an similar job with id = <jobId> which has not finished yet` |

Somente problemas com a definição de relatório salva são detectados quando o trabalho é executado. Nesse caso, o status do trabalho se torna `Failed` e nenhum motivo é retornado.

### Requisitos de relatório

O trabalho falhará com uma mensagem de erro se o relatório não atender a estas condições:

* A definição de relatório inclui um filtro de data relativa, por exemplo, os últimos 7 dias.
* Cada filtro de data no relatório deve cobrir 7 dias ou menos, não apenas um.
* Intervalos de datas fixos, com datas de início e término definidas, não são compatíveis e o trabalho falha.
* Um relatório sem filtro de data falha. Isso inclui relatórios criados em conjuntos de dados que não têm campo de data.

>[!NOTE]
>
>A solicitação de POST é validada imediatamente. Uma solicitação inválida foi rejeitada com HTTP 400 e o motivo está em `source.info`.

### Verificar o status do trabalho e baixar o relatório

**Objetivo final**

```
GET /primeapi/v2/jobs/{jobId}
```

A resposta usa a mesma estrutura de outros tipos de job. Quando o trabalho for concluído, `status.code` será `Completed` e `status.data.s3Url` conterá o link de download.

```json
{
  "data": {
    "type": "job",
    "id": "12345",
    "attributes": {
      "jobType": "generateCustomReport",
      "payload": {
        "reportId": "1478"
      },
      "status": {
        "code": "Completed",
        "data": {
          "s3Url": "valid for 7 days"
        }
      }
    }
  }
}
```

A API retorna `Submitted`, `Completed` e `Failed`. O arquivo é um único CSV chamado `report.csv`.

>[!NOTE]
>
>O URL de download é válido por sete dias. Baixe o arquivo assim que o trabalho for concluído.

>[!IMPORTANT]
>
>Qualquer pessoa com o link pode baixar o arquivo sem fazer logon. Manipule o link da mesma forma que trataria os dados que ele contém.

**Amostra de trabalho com falha**

```json
"status": { "code": "Failed" }
```

### Limites

Somente um trabalho do `generateCustomReport` para um relatório pode ser executado por vez. Uma segunda solicitação é rejeitada até que a primeira seja concluída.

### Saída do relatório do quiz L2

Quando você compila um relatório do conjunto de dados do quiz L2 em Report Builder e o exporta com `generateCustomReport`, a saída tem as seguintes características:

* A saída é um único arquivo CSV chamado `report.csv`. O módulo é uma coluna no arquivo. Se você selecionar um curso, o relatório retornará apenas seus módulos de questionário.
* Cada linha representa a resposta de um aluno a uma pergunta em uma tentativa.
* Os dados são atualizados no intervalo de Report Builder padrão (aproximadamente a cada 15 minutos).
* Os valores de data e hora estão no fuso horário da sua conta. O cabeçalho da coluna mostra o fuso horário, por exemplo, `L2 Quiz - Response - Timestamp (America/Argentina/Salta)`.

### Campos no conjunto de dados do questionário L2

| Categoria | Campos |
|---|---|
| Aluno | ID do usuário |
| Curso | ID do curso, ID da instância do curso, Nome do curso |
| Módulo | ID do módulo, Nome do módulo, Versão do módulo |
| Pergunta | ID da pergunta, Texto da pergunta, Resposta correta, Tipo de interação |
| Resposta | Resposta De Resposta, Pontuação Obtida, Pontuação Máxima Possível, Está Correto, Carimbo De Data/Hora Da Resposta |
| Tentativa | Número da tentativa |

>[!NOTE]
>
>O conjunto de dados do questionário L2 não está vinculado a outros conjuntos de dados de Report Builder. O nome do aluno, e-mail, gerente e atributos personalizados não estão disponíveis neste relatório. Para corresponder uma linha a um aluno, use a ID do usuário.

Você também pode exportar relatórios compilados em outros conjuntos de dados Report Builder com `generateCustomReport`. Os campos disponíveis na saída dependem do conjunto de dados.

## APIs para criar e gerenciar o conector do Zoom

Use essas APIs para gerenciar conexões do Zoom no Adobe Learning Manager. Você pode recuperar conexões existentes, salvar credenciais do Zoom, criar ou atualizar conexões, configurar permissões de acesso para grupos de usuários e funções personalizadas e habilitar ou desabilitar uma conexão.

### Configurar APIs do conector do Zoom

A configuração e o gerenciamento de um conector do Zoom exigem quatro chamadas de API. Crie-os nesta ordem:

| Etapa | API | O que ela faz |
|---|---|---|
| 1 | `POST /ctr/authcred/uuid/20012` | Salva as credenciais do Zoom. |
| 2 | `POST /ctr/app/esconnect` | Cria a conexão do Zoom ou atualiza uma existente. |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Define os grupos de usuários e funções personalizadas que podem usar a conexão. |
| 4 | `POST /ctr/xtsas/{connectionId}/enable` | Ativa ou desativa a conexão. |

>[!NOTE]
>
>Essas APIs usam a sessão do administrador de integração conectado. Eles não usam uma chave de API ou um token OAuth.

### URL base e convenções

As APIs do conector do Zoom usam as seguintes convenções:

| Item | Valor |
|---|---|
| URL base | `https://learningmanagerstage1.adobe.com` |
| Tipo de conteúdo | `application/json` |
| Autenticação | Sessão de um administrador de integração conectado |
| Cabeçalhos obrigatórios | `content-type`, `accept`, `x-acap-caller-role: ROLE_INTEGRATIONADMIN`, `x-csrf-token` e `Cookie` |
| UUID do catálogo de integração para o Zoom | `20012` |
| Limite de conexão | 50 conexões de zoom |

O valor `x-csrf-token` está incorporado no HTML da página do Administrador de Integração como `csrfToken`. O cabeçalho `Cookie` carrega os cookies de sessão do administrador conectado.

### Antes de começar

- Faça logon como administrador de integração.
- Crie um aplicativo OAuth de servidor para servidor do Zoom. Anote a ID do cliente, o segredo do cliente e a ID da conta. Você também precisa do endereço de email do superadministrador do Zoom.
- Ligue para `GET /ctr/xtsas/canCreateAccount/25`. Retorna `true` se você puder criar outra conexão do Zoom.

### Etapa 1: salvar as credenciais do Zoom {#save-credentials}

Chame essa API antes de criar ou atualizar uma conexão. Ele armazena as credenciais que o conector usa para se conectar ao Zoom.

```
POST /ctr/authcred/uuid/20012
```

Para atualizar uma conexão existente, adicione o parâmetro de consulta `connectionId`:

```
POST /ctr/authcred/uuid/20012?connectionId={connectionId}
```

O corpo da solicitação são as credenciais como texto JSON. É uma string JSON que contém JSON, não um objeto aninhado. Inclua as aspas externas.

| Chave | Descrição |
|---|---|
| `clientId` | A ID do cliente do aplicativo Zoom. |
| `clientSecret` | O segredo do cliente do aplicativo Zoom. Este valor é sensível. |
| `accountId` | A ID da conta do Zoom. |
| `superAdmin` | O endereço de email do superadministrador do Zoom. |

Amostra do corpo da solicitação:

```
"{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}"
```

Exemplo de resposta `200 OK`:

```json
{
  "code": 0,
  "description": "Success"
}
```

`code: 0` significa que as credenciais foram salvas.

### Etapa 2: criar ou atualizar a conexão do Zoom {#create-connection}

Esta API cria uma conexão com o Zoom. O mesmo ponto de extremidade também atualiza uma conexão existente.

```
POST /ctr/app/esconnect
```

O corpo da solicitação tem os seguintes campos:

| Campo | Obrigatório | Descrição |
|---|---|---|
| `UUID` | Sim | A UUID do catálogo de integração. Use `20012` para o Zoom. |
| `listOfConnections` | Sim | As conexões a serem criadas. Enviar um item. |
| `listOfConnections[].name` | Sim | O nome de exibição do conector, por exemplo `Zoom_Partner_X`. |
| `listOfConnections[].tag` | Sim | Enviar uma cadeia de caracteres vazia (`""`) ao criar um conector. Omita-o ao atualizar um. |
| `listOfConnections[].credentialsJson` | Sim | As credenciais são texto JSON. Use a mesma string enviada na etapa 1. |
| `listOfConnections[].schedules` | Sim | O agendamento da sincronização. Enviar `objectUUID` 10002, `priority` 1 e `type` 1. |
| `listOfConnections[].id` | Atualizar apenas | A ID da conexão a ser atualizada, por exemplo `3474737`. |

Amostra do corpo da solicitação:

```json
{
  "UUID": 20012,
  "listOfConnections": [
    {
      "name": "Zoom_Example",
      "tag": "",
      "credentialsJson": "{\"clientId\":\"<ZOOM_CLIENT_ID>\", \"clientSecret\":\"<ZOOM_CLIENT_SECRET>\", \"accountId\":\"<ZOOM_ACCOUNT_ID>\", \"superAdmin\":\"<ADMIN_EMAIL>\"}",
      "schedules": [
        { "objectUUID": 10002, "priority": 1, "type": 1 }
      ]
    }
  ]
}
```

Exemplo de resposta `200 OK`:

```json
[3474737]
```

A resposta é uma matriz JSON que contém a ID da nova conexão. Use esse ID nas etapas 3 e 4 e em qualquer chamada de acompanhamento.

### Criar e atualizar comparados

| Diferença | Criar | Atualização |
|---|---|---|
| `listOfConnections[].id` | Não enviado | A ID da conexão |
| `listOfConnections[].tag` | `""` | Não enviado |
| Chamada de credenciais na etapa 1 | `POST /ctr/authcred/uuid/20012` | `POST /ctr/authcred/uuid/20012?connectionId={id}` |

### Etapa 3: Definir quem pode usar a conexão {#set-access}

Essa API define quais grupos de usuários e funções personalizadas podem usar a conexão.

```
PUT /ctr/xtsa/{connectionId}/access
```

O caminho usa o singular `xtsa` para uma conexão. O plural `xtsas` é a coleção de conexões.

O corpo da solicitação é uma matriz JSON. Cada item concede acesso a um grupo de usuários ou função personalizada.

| Campo | Obrigatório | Descrição |
|---|---|---|
| `accessType` | Sim | `USER_GROUP` ou `CUSTOM_ROLE`. |
| `accessId` | Sim | A ID do grupo de usuários ou função personalizada como uma cadeia de caracteres. |

Amostra do corpo da solicitação:

```json
[
  { "accessType": "USER_GROUP", "accessId": "<groupId>" },
  { "accessType": "CUSTOM_ROLE", "accessId": "<roleId>" }
]
```

A API retorna `204 No Content` sem corpo quando a lista de acesso é salva.

>[!NOTE]
>
>A solicitação substitui toda a lista de acesso. Ele não acrescenta a ele. Qualquer coisa que não esteja no corpo perde o acesso. Para remover todo o acesso, envie uma matriz vazia (`[]`).

### Etapa 4: ativar ou desativar a conexão {#enable-disable}

Essa API ativa ou desativa uma conexão. Use-a depois de criar a conexão sempre que precisar alterar seu estado.

```
POST /ctr/xtsas/{connectionId}/enable
```

O caminho usa o plural `xtsas`, como a lista e as chamadas de exclusão. A chamada de acesso na etapa 3 usa o singular `xtsa`.

| Parâmetro Path | Tipo | Descrição |
|---|---|---|
| `connectionId` | Número | A ID da conexão. É o `id` retornado por `GET /ctr/xtsas`, e o ID retornado na etapa 2. |

O corpo da solicitação tem os seguintes campos:

| Campo | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `objectUUID` | Número | Sim | O objeto de sincronização da conexão. Use `10002`, o mesmo valor enviado em `schedules[].objectUUID` na etapa 2. |
| `operation` | Número | Sim | Enviar `1`. |
| `val` | Booleano | Sim | O novo estado da conexão. Envie `false` para desabilitar a conexão. Envie `true` para habilitá-lo. |

Amostra do corpo da solicitação para desativar uma conexão:

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": false
}
```

Exemplo de corpo de solicitação para ativar uma conexão:

```json
{
  "objectUUID": 10002,
  "operation": 1,
  "val": true
}
```

Exemplo de solicitação para desativar uma conexão:

```bash
curl -X POST 'https://learningmanagerstage1.adobe.com/ctr/xtsas/<connectionId>/enable' \
  -H 'accept: application/json' \
  -H 'content-type: application/json' \
  -H 'x-acap-caller-role: ROLE_INTEGRATIONADMIN' \
  -H 'x-csrf-token: <CSRF_TOKEN>' \
  -H 'Cookie: <SESSION_COOKIES>' \
  --data '{"objectUUID":10002,"operation":1,"val":false}'
```

Para confirmar o novo estado, ligue para `GET /ctr/xtsas`, localize a conexão por `id` e verifique seu sinalizador `enabled`.

>[!NOTE]
>
>O cabeçalho `x-acap-caller-role` deve corresponder à função do perfil ativo. Para essas APIs, use `ROLE_INTEGRATIONADMIN`.

### Gerenciar a conexão depois de criá-la

Você pode usar as seguintes chamadas com o ID de conexão:

| Finalidade | Chamada |
|---|---|
| Ativar ou desativar uma conexão | `POST /ctr/xtsas/{connectionId}/enable` |
| Ler a lista de acesso de uma conexão | `GET /ctr/xtsa/{connectionId}/access` |
| Acesso de leitura para todas as conexões do Zoom | `GET /ctr/xtsas/access?UUID=20012` |
| Listar todas as conexões. As conexões de zoom têm `extsysRefId` 25. | `GET /ctr/xtsas` |
| Exibir uma conexão | `GET /ctr/app/connection/{id}/object/10002` |
| Excluir uma conexão permanentemente | `DELETE /ctr/xtsas/{id}` |

>[!NOTE]
>
>A chamada de exibição retorna o segredo do cliente em texto não criptografado. Trate o segredo do cliente como confidencial e gire-o se exposto. Não confirme ou compartilhe cookies de sessão, tokens CSRF ou credenciais, inclusive em arquivos HAR e comandos cURL copiados.

### Usar essas APIs na integração

Um caso de uso comum é uma configuração automatizada de um conector do Zoom para uma nova conta ou parceiro.

1. Ligue para `GET /ctr/xtsas/canCreateAccount/25` para confirmar se você pode criar outra conexão.
2. Chamar `POST /ctr/authcred/uuid/20012` com as credenciais de Zoom.
3. Chame `POST /ctr/app/esconnect` com o nome do conector, a mesma cadeia de caracteres de credenciais e o agendamento de sincronização. Leia a ID de conexão da resposta.
4. Chame `PUT /ctr/xtsa/{connectionId}/access` com os grupos de usuários e funções personalizadas que podem usar a conexão.
5. Chame `POST /ctr/xtsas/{connectionId}/enable` com `val` definido como `true` ou `false` para habilitar ou desabilitar a conexão. Em seguida, ligue para `GET /ctr/xtsas` e verifique o sinalizador `enabled` para confirmar o estado.
6. Para alterar as credenciais mais tarde, repita as etapas 2 e 3 com a ID de conexão.


