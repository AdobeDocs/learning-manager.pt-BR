---
description: Obtenha eventos de webhook no Adobe Learning Manager quando os professores editarem detalhes da sessão e mantiverem as notificações do aluno e os sistemas conectados atualizados.
jcr-language: en_us
title: Receber eventos de webhook para edições de sessão de professor
exl-id: 6fa4b71b-a8f4-40a2-ab57-bb7f3016542c
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%
---

# Eventos do Webhook para edições de instância do LO por professores

O Adobe Learning Manager fornece eventos de webhook que notificam sistemas externos quando uma instância do objeto de aprendizado (LO), como uma sessão de um curso ministrado pelo professor, é modificada. Anteriormente, esses eventos eram acionados somente quando um administrador ou autor modificava uma instância do LO. Os eventos do webhook agora também são acionados quando um professor edita os detalhes de uma sessão.

Você pode usar esses eventos para manter sistemas externos, como serviços de email, calendários, ferramentas de relatório ou plataformas de análise atualizados com as alterações do professor. Por exemplo, você pode notificar os alunos quando o tempo de uma sessão mudar.

As edições do professor usam o evento de modificação de instância de objeto de aprendizado existente, portanto nenhum novo tipo de evento é introduzido.

>[!NOTE]
>
>As edições do professor acionam um webhook somente se um webhook ativo se inscrever no evento de modificação de instância do objeto de aprendizado. Saiba como [criar e gerenciar webhooks como Administrador de Integração](/help/migrated/integration-admin/feature-summary/webhooks.md#create-manage-webhooks).

## Edições de professor compatíveis

O evento do webhook é acionado quando um professor edita qualquer um dos seguintes detalhes da sessão:

* Horários da sessão

* Créditos

* Fuso horário

* Ponto de Encontro

* Limite de inscrição

* Limite da lista de espera

* Permitir envios

## Estrutura de carga do webhook

Cada solicitação de webhook contém a seguinte estrutura de nível superior:

```json
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "121da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

A mesma estrutura é usada independentemente de quem modifica a instância do LO. A carga não indica se um professor, um administrador ou um autor fez a alteração.

Quando um professor altera um detalhe de sessão, como o fuso horário, o limite de inscrição ou o limite da lista de espera, o webhook envia esse evento para o URL do ouvinte. Use o evento para recuperar os detalhes da sessão mais recente e notificar os alunos ou atualizar seus sistemas externos.

## Recuperar os detalhes da sessão atualizada

O evento do webhook identifica a instância do LO que foi modificada. Para obter os detalhes da sessão atualizada, chame a API pública do Learning Manager (API Prime) usando o `loId` do evento:

```http
GET /primeapi/v2/learningObjects/{loId}
```

Localize a instância que corresponde a `loInstanceId` na resposta e compare-a com os dados armazenados no sistema.

## Criar integrações com eventos do webhook

Você pode usar esses eventos de webhook para:

* Envie notificações ao aluno por meio de um e-mail externo ou serviço de mensagens quando os detalhes da sessão, como data, hora, fuso horário ou alteração do local, forem alterados.

* Sincronizar dados de sessão com calendários, relatórios ou sistemas de análise externos.

* Rastreie as alterações de capacidade quando o limite de inscrição ou de lista de espera de uma sessão for modificado.

* Mantenha as trilhas de auditoria registrando `eventId`, `timestamp` e `eventInfo` junto com o LO e os identificadores de instância.

No mínimo, o manipulador de webhook deve:

* Validar a carga e analisar `events[]`.

* Use `eventName` para identificar o evento de modificação de instância do objeto de aprendizado.

* Use `loId` e `loInstanceId` para localizar o registro correspondente em seu sistema e chame a API pública para recuperar os detalhes da sessão atual.

* Use `eventId` para evitar processamento duplicado se o mesmo evento for entregue mais de uma vez.

O mesmo evento é enviado para edições feitas por professores, administradores e autores, para que sua integração possa recebê-lo com mais frequência do que antes. Compare os detalhes da sessão recuperada com os dados do sistema antes de enviar uma notificação. Os alunos são notificados somente quando os detalhes relevantes são alterados.
