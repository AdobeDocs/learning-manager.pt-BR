---
jcr-language: en_us
title: Webhooks
description: Saiba mais sobre os webhooks para enviar informações em tempo real, como inscrições no curso, criação do curso e outras informações, para um URL específico
contentowner: chandrum
exl-id: 472aaf2b-9c2f-4f43-a791-2b2d81e69471
source-git-commit: e4c3489db8207ead0416656161b918eba42f4582
workflow-type: tm+mt
source-wordcount: '765'
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
