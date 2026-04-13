---
jcr-language: en_us
title: Webhooks
description: Saiba mais sobre os webhooks para enviar informações em tempo real, como inscrições no curso, criação do curso e outras informações, para um URL específico
contentowner: chandrum
exl-id: 472aaf2b-9c2f-4f43-a791-2b2d81e69471
source-git-commit: 3b35c16d74c83329cee24ee9ad007a53ccbd8cf3
workflow-type: tm+mt
source-wordcount: '1633'
ht-degree: 0%

---

# Webhooks

Um webhook permite que uma entidade envie automaticamente dados ou notificações em tempo real para outra entidade quando ocorre um evento específico. Isso permitirá que um aplicativo forneça informações a outros aplicativos sem solicitar constantemente. Por exemplo, se um usuário concluir um curso do Sistema de Gerenciamento de Aprendizado (LMS), um webhook poderá enviar automaticamente essas informações para outra plataforma, como um CRM ou uma ferramenta de relatório. Os webhooks são frequentemente usados em integrações para automatizar processos e reduzir a necessidade de atualizações manuais entre sistemas. Configure webhooks fornecendo um URL de retorno de chamada para o qual você enviaria os dados.

## Webhooks vs APIs

Os webhooks e as APIs ajudam os sistemas a se comunicarem entre si, mas funcionam de maneiras diferentes. Com as APIs, as informações são compartilhadas somente quando o usuário as solicita. Por exemplo, se um aluno requer dados de progresso do curso, ele envia uma solicitação à API, que fornece as informações. Por outro lado, os webhooks enviam dados automaticamente imediatamente quando um evento acontece. Por exemplo, se um aluno concluir um curso, ele enviará os dados imediatamente para o URL do ouvinte sem nenhuma solicitação manual.

## O que são APIs em tempo real?

As APIs em tempo real permitem que os aplicativos troquem dados instantaneamente quando um evento acontece. Diferentemente das APIs tradicionais, que aguardam um usuário solicitar informações, as APIs em tempo real compartilham dados no momento em que ocorrem. Os webhooks atuam como uma API em tempo real e ajudam a compartilhar os dados imediatamente sempre que o evento especificado ocorre. A API em tempo real garante que essa transferência de dados ocorra imediatamente, sem a necessidade de qualquer solicitação manual, o que permite que os sistemas permaneçam atualizados instantaneamente.

## Eventos do Webhook

Eventos de webhook são ações específicas que ocorrem em um sistema que envia dados automaticamente para um URL de ouvinte. Por exemplo, quando um aluno se inscreve em um curso, um evento de webhook é acionado e envia os detalhes de inscrição para o URL do ouvinte.

Os eventos do webhook são classificados em duas categorias:

* **Eventos em tempo real**: os eventos são processados e enviados em tempo real para uma URL de destino
* **Eventos que não são em tempo real**: os eventos são processados em lotes e enviados em horários especificados em vez de em tempo real

## URL do Listener

Um URL de Listener é um ponto final ou destino que recebe informações de dados quando ocorre um evento. Sempre que um evento específico acontece, como a inscrição de um usuário em um curso, o sistema envia automaticamente os detalhes para esse URL sem qualquer solicitação manual. O URL do listener é o endereço onde todas essas atualizações são fornecidas.
O webhook envia as informações relevantes em um formato JSON. Veja um exemplo de carga de um evento acionado no Adobe Learning Manager:

```
{
  "accountId": 1010,
  "events": [
    {
      "eventId": "d5fb7071-10a9-46b2-9f9e-79dde346c052",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1727414643000,
      "eventInfo": "1727414643000-047210-84242-0",
      "data": {
        "userId": 4279332,
        "loId": "course:7374992",
        "loInstanceId": "course:7376092_10250977",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1727414643
      }
    }
  ]
}
```

## Criar e gerenciar Webhooks - Administrador de integração

Siga as etapas abaixo para criar a integração de webhooks no Adobe Learning Manager:

1. Faça logon como **[!UICONTROL Administrador de Integração]**.
2. Na página inicial, selecione **[!UICONTROL Webhooks]** > **[!UICONTROL Adicionar Webhook]**.

   ![](assets/create-webhook.png)
   _Adicionar um webhook_

3. Digite o **[!UICONTROL Nome]** e a **[!UICONTROL Descrição]** do Webhook.
4. Digite a URL do ouvinte como uma **[!UICONTROL URL de Destino]** para a qual você deseja passar os dados do evento.
5. Selecione qualquer um dos métodos de autenticação:
A autenticação em Webhooks é um método de segurança para garantir que os dados enviados para um URL de listener venham de uma origem confiável.
   * **[!UICONTROL Nenhum]**: nenhuma autenticação necessária.
   * **[!UICONTROL Básico]**: esta é uma autenticação baseada em credencial. Insira o nome de usuário e a senha.
   * **[!UICONTROL Assinatura]**: o sistema cria uma assinatura especial e a adiciona aos dados do webhook. O servidor de recebimento verifica esse código para certificar-se de que os dados são reais e não foram alterados. Gere uma assinatura e use-a para autenticação. Baixe a assinatura como JSON.
6. Selecione os eventos do Webhook no menu suspenso **[!UICONTROL Acionar eventos]**.

   >[!NOTE]
   >
   >Você também pode testar os webhooks selecionando a opção Testar Webhooks na página Adicionar Webhook.

7. Selecione o alternador **[!UICONTROL Status de ativação]** para habilitar o webhook. Uma vez ativado, os dados serão transmitidos sempre que os eventos selecionados ocorrerem.

>[!NOTE]
>
>Você pode criar e gerenciar até 5 webhooks.

### Editar Webhooks - Administrador de Integração

Siga estas etapas para editar webhooks do Adobe Learning Manager:

1. Faça logon como **[!UICONTROL Administrador de Integração.]**
2. Selecione **[!UICONTROL Webhooks]** na página inicial.
3. Selecione o webhook que deseja editar.

   ![](assets/edit-webhook.png)
   _Editar o webhook_
4. Selecione **[!UICONTROL Editar]** para modificar os detalhes do webhook e selecione **[!UICONTROL Salvar]**.

### Remover Webhooks - Administrador de Integração

Siga estas etapas para editar webhooks do Adobe Learning Manager:

1. Faça logon como **[!UICONTROL Administrador de Integração]**.
2. Selecione **[!UICONTROL Webhooks]** na página inicial.
3. Selecione o webhook que deseja excluir.
4. Selecione **[!UICONTROL Excluir]** para remover os webhooks.

![](assets/delete-webhooks.png)
_Remover o webhook_

### Baixar Webhooks - Administrador de Integração

Siga estas etapas para desativar os webhooks:

1. Faça logon como **[!UICONTROL Administrador de Integração]**.
2. Selecione **[!UICONTROL Webhooks]** na página inicial.
3. Selecione o webhook que deseja editar.
4. Selecione **[!UICONTROL Editar]** e desabilite o **[!UICONTROL Status de Ativação]** para desativar o webhook.

![](assets/retire-webhook.png)
_Desativar o webhook_

## Webhooks para alternativas {#webhooks-for-alternates}

O ALM fornece eventos de webhook dedicados para conclusões alternativas a fim de oferecer suporte à automação, integrações e sincronização com sistemas externos.

Esses eventos permitem que os consumidores externos façam uma distinção confiável entre términos diretos e términos concedidos por meio de relacionamentos alternativos.

### Visão geral

Quando um aluno conclui um curso por meio de uma alternativa ou relação, o ALM aciona um evento de webhook separado do webhook de conclusão de curso padrão. Isso garante que as integrações possam responder de forma diferente a conclusões alternativas, quando necessário.

Os eventos do webhook também são acionados quando ocorre conclusão retroativa ou inconclusão retroativa, abrangendo atualizações históricas, bem como alterações de relacionamento.

### Comportamento do evento do Webhook

* Um evento distinto de webhook é acionado quando um aluno recebe Concluído por meio do status Alternativo de um curso de destino.
* O evento é gerado quando o aluno conclui um curso de origem configurado que satisfaz o destino por meio de um relacionamento alternativo.
* Este webhook não é acionado para conclusões diretas de curso.
* Quando a conclusão retroativa ou a inconclusão retroativa estão ativadas, os eventos do webhook são emitidos para cada aluno e curso de destino afetados.

### Detalhes da carga do Webhook

A carga do webhook de conclusão alternativa inclui os seguintes atributos de chave:

* **ID do aluno**
Identifica o aluno que recebeu a conclusão alternativa.
* **Curso de origem**
O curso ou caminho de aprendizado que o aluno concluiu diretamente.
* **Curso de destino**
O curso marcado como concluído por meio do relacionamento alternativo.
* **Método de conclusão**
Indica que o método de conclusão é alternativo.
* **Data de conclusão**
Derivado da data de conclusão do curso de origem.
* **Tipo de relação**
Especifica se a relação é alternativa.

Para cenários de inconclusão retroativa, os eventos do webhook indicam que uma conclusão alternativa existente foi revogada.

### Considerações de integração

Os sistemas externos podem usar esses eventos de webhook para:

* Atualizar registros do aluno
* Sincronizar status de conclusão
* Acionar notificações ou fluxos de trabalho downstream
* Manter trilhas de auditoria para fins de conformidade

Os consumidores de webhook devem diferenciar explicitamente entre conclusões diretas e alternativas.

Conclusões alternativas não concedem recompensas de habilidades, medalhas e gamificação. O feedback deve ser tratado de acordo nos sistemas downstream.

## Webhooks para Caminhos de aprendizado adaptáveis

### Introdução

O Adobe Learning Manager fornece **eventos de webhook** que notificam sistemas externos sempre que o status de conclusão de um **caminho de aprendizado (programa de aprendizado)** é atualizado. Isso permite sincronizar sistemas downstream (como plataformas de RH, de relatórios ou de análise) sempre que o registro de conclusão de um aluno é revertido ou recalculado.

Dois novos tipos de evento de webhook estão disponíveis:

**LEARNING_PATH_COMPLETION_ROLLBACK** - Acionado quando um **aluno** atualiza o status de conclusão de um caminho de aprendizado para si mesmo.

**LEARNING_PATH_COMPLETION_ROLLBACK_BATCH** - Acionado quando um **administrador** atualiza o status de conclusão de um caminho de aprendizado para **um ou mais alunos** (por exemplo, via operações em massa).

Esses eventos usam uma **estrutura de carga comum** e podem ser consumidos pelo ponto de extremidade do webhook para atualizar ou reprocessar dados de conclusão do seu lado.

### Estrutura de carga comum

Cada solicitação do webhook contém a seguinte estrutura de nível superior:

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "757b9d58-048c-4ae2-9fff-35f9def7ef29",
      "eventName": "LEARNING_PATH_COMPLETION_ROLLBACK",
      "timestamp": "2026-01-20T05:48:10.000Z",
      "eventInfo": "1768888090000-197513-137581-0",
      "data": {
        "userId": 13446697,
        "loId": "learningProgram:157165",
        "loInstanceId": "learningProgram:157165_148769",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2026-01-20T05:44:05.000Z"
      }
    }
  ]
}
```

A **mesma estrutura** é usada para os dois tipos de evento; somente o eventName e os valores dentro dos dados (por exemplo, userId, loId, enrollmentSource) diferem.

#### Exemplo: atualização iniciada pelo aluno

Quando um aluno atualiza o status de conclusão de seu próprio caminho de aprendizado, o webhook envia um evento LEARNING_PATH_COMPLETION_ROLLBACK:

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "757b9d58-048c-4ae2-9fff-35f9def7ef29",
      "eventName": "LEARNING_PATH_COMPLETION_ROLLBACK",
      "timestamp": "2026-01-20T05:48:10.000Z",
      "eventInfo": "1768888090000-197513-137581-0",
      "data": {
        "userId": 13446697,
        "loId": "learningProgram:157165",
        "loInstanceId": "learningProgram:157165_148769",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2026-01-20T05:44:05.000Z"
      }
    }
  ]
}
```

Use este evento para **recalcular ou redefinir os dados de conclusão do aluno** nos sistemas externos quando o aluno solicitar explicitamente uma atualização.

#### Exemplo: atualização em lote iniciada pelo administrador

Quando um administrador executa uma atualização de conclusão para um ou mais alunos (por exemplo, corrigindo conclusões históricas para um grupo), o webhook emite um evento LEARNING_PATH_COMPLETION_ROLLBACK_BATCH:

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "757b9d58-048c-4ae2-9fff-35f9def7ef29",
      "eventName": "LEARNING_PATH_COMPLETION_ROLLBACK_BATCH",
      "timestamp": "2026-01-20T05:48:10.000Z",
      "eventInfo": "1768888090000-197513-137581-0",
      "data": {
        "userId": 13446698,
        "loId": "learningProgram:157166",
        "loInstanceId": "learningProgram:157166_148770",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2026-01-21T05:44:05.000Z"
      }
    }
  ]
}
```

Em operações em lote, o ponto de extremidade do webhook pode receber **vários objetos de evento em uma única solicitação**, um por aluno cuja conclusão foi atualizada. Sua integração deve iterar sobre a matriz de eventos e processar cada evento independentemente.

### Como usar esses eventos em integrações

Você pode usar esses eventos de webhook para:

**Sincronizar registros de conclusão** com LMS/LRS, RH ou sistemas de relatórios externos quando uma conclusão é revertida ou recalculada.

**Acionar fluxos de trabalho downstream**, como reatribuições, notificações ou recálculo de certificações e medalhas.

**Manter trilhas de auditoria** registrando eventId, timestamp e eventInfo junto com os identificadores do aluno e do caminho de aprendizado.

No mínimo, o manipulador de webhook deve:

Valide a carga e analise os eventos[].
Use eventName para determinar se a alteração foi **iniciada pelo aluno** ou **iniciada pelo administrador/lote**.

Use userId, loId e loInstanceId para localizar e atualizar o registro correspondente no sistema.
Aproveite a eventId para evitar processamento duplicado se o mesmo evento for entregue mais de uma vez.

## Webhooks para adicionar e remover associação a grupo de usuários

Dois novos tipos de evento de webhook apresentam os status finais:

* RESPOSTA:ASYNCAPI_USERGROUP_USER_ADDED
* RESPOSTA:ASYNCAPI_USERGROUP_USER_REMOVED

### Carga de exemplo

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5",
      "eventName": "RESPONSE:ASYNCAPI_USERGROUP_USER_REMOVED",
      "timestamp": "2026-03-18T13:38:12.000Z",
      "eventInfo": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5",
      "data": {
        "status": "SUCCESS",
        "request": {
          "metadata": { "event_id": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5" },
          "data": [ { "type": "user", "id": "13446641" } ]
        }
      }
    }
  ]
}
```

### Elementos principais

* `accountId` identifica a conta do ALM.
* `events` é uma matriz de objetos de evento.
* `eventId` corresponde ao identificador de solicitação assíncrona original.
* `eventName` indica operação de adição ou remoção.
* `timestamp` mostra o tempo de conclusão.
* `data.status` atualmente relata “ÊXITO” para lotes bem-sucedidos.
* `data.request` contém a solicitação exata enviada.

Sua integração deve principalmente definir a chave de `eventId` (ou `metadata.event_id`) e `status`.

### Exemplos

#### Adicionando usuários de forma assíncrona

**Etapa 1. Fazer a chamada assíncrona**

POST /primeapi/v2/async/userGroups/12345/users

```
{
  "metadata": {
    "event_id": "sync-2026-03-30T10:15:00Z-ug-12345",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0001"
  },
  "data": [
    { "type": "user", "id": "11101219" },
    { "type": "user", "id": "11101220" }
  ]
}
```

**Etapa 2. Ler a resposta imediata**

```
{ "event_id": "sync-2026-03-30T10:15:00Z-ug-12345" }
```

Agora você pode marcar esta tarefa como enviada em seu sistema.

**Etapa 3. Manipular o webhook**

Exemplo de retorno de chamada do Webhook:

```
{
  "accountId": 69735,
  "events": [
    {
      "eventId": "sync-2026-03-30T10:15:00Z-ug-12345",
      "eventName": "RESPONSE:ASYNCAPI_USERGROUP_USER_ADDED",
      "timestamp": "2026-03-30T10:15:43.000Z",
      "data": {
        "status": "SUCCESS",
        "request": {
          "metadata": {
            "event_id": "sync-2026-03-30T10:15:00Z-ug-12345",
            "sourceSystem": "HRIS",
            "batchId": "hr_2026_03_30_0001"
          },
          "data": [
            { "type": "user", "id": "11101219" },
            { "type": "user", "id": "11101220" }
          ]
        }
      }
    }
  ]
}
```

Um consumidor típico irá:

* Localize o job interno.
* Opcionalmente, verifique a associação usando GET /userGroups/{id}/users.
* Marcar o trabalho como concluído.

#### Removendo usuários de forma assíncrona

A remoção é simétrica, usando DELETE com a mesma estrutura corporal.

```
{
  "metadata": {
    "event_id": "sync-2026-03-30T11:00:00Z-ug-12345",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0002"
  },
  "data": [ { "type": "user", "id": "11101219" } ]
}
```

Resposta imediata:

```
{ "event_id": "sync-2026-03-30T11:00:00Z-ug-12345" }
```

Posteriormente, um webhook RESPONSE:ASYNCAPI_USERGROUP_USER_REMOVED chega com a mesma eventId.

Exiba [API pública assíncrona para associação de grupo de usuários](/help/migrated/api-changes-alm.md#asynchronous-public-apis-for-user-group-membership) para obter mais informações.
