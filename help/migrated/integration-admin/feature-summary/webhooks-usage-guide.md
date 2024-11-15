---
jcr-language: en_us
title: Guia de uso de webhooks
description: Saiba mais sobre o uso de webhooks, práticas recomendadas e limitações
contentowner: chandrum
exl-id: e6a63ffb-7fdd-46e4-b5e6-20ce36861cef
source-git-commit: 4b26eddf1285651a13ee9c71fdf677e8b92e6dc3
workflow-type: tm+mt
source-wordcount: '3369'
ht-degree: 1%

---

# Guia de uso de webhooks

Os webhooks são uma maneira de os aplicativos da Web se comunicarem entre si automaticamente e em tempo real.

Diferentemente das APIs tradicionais, que aguardam um usuário solicitar informações, as APIs em tempo real compartilham dados no momento em que ocorrem. Os webhooks atuam como uma API em tempo real e ajudam a compartilhar os dados imediatamente sempre que o evento especificado ocorre.

## Entidades

Para entender os eventos de webhooks, primeiro precisamos estar cientes das entidades envolvidas e das condições de acionamento desses eventos.

### Objetos de aprendizado

Estes são os eventos compatíveis com objetos de aprendizado (curso, caminho de aprendizado ou certificações).

#### Rascunho

Sempre que um objeto de aprendizado é criado a partir da interface do usuário, ele começa no modo **Rascunho**. Isso significa que o objeto de aprendizado ainda não foi publicado e não está disponível para os alunos. O evento **LEARNING_OBJECT_DRAFT** é acionado desde que o objeto de aprendizado permaneça um rascunho. Todas as atualizações sucessivas ao rascunho também acionarão esse evento.

#### Atualização

Depois que o objeto de aprendizado é publicado, seu estado muda de **Rascunho** para **Publicado**. Durante esta transição, o Webhook gera o evento **LEARNING_OBJECT_MODIFICATION** porque o objeto de aprendizado está sendo modificado de **Rascunho** para **Publicado**. Todas as modificações e atualizações subsequentes no OA também acionarão um evento **LEARNING_OBJECT_MODIFICATION**.

O evento **LEARNING_OBJECT_MODIFICATION** também é acionado quando o objeto de aprendizado é desativado. Essa operação desativada marca as instâncias subjacentes como atualizadas, pois essas instâncias são desativadas quando o objeto de aprendizado pai está no estado desativado.

#### Excluir

Após a exclusão de um objeto de aprendizado, o evento **LEARNING_OBJECT_DELETION** é gerado. Esse evento indica que o objeto de aprendizado foi excluído e não está mais disponível para acesso dos alunos.

Além dos eventos em tempo real, os eventos do objeto de aprendizado também têm um equivalente em lote (não em tempo real), que é acionado como parte do evento **LEARNING_OBJECT_MODIFICATION_BATCH**. Esse evento ocorre durante a criação ou a modificação de um objeto de aprendizado por meio do fluxo de trabalho de migração. Como as operações de rascunho e exclusão do objeto de aprendizado não são suportadas por meio da migração, não há eventos de rascunho ou exclusão correspondentes para essas ações.

### Instâncias do objeto de aprendizado

Veja a seguir os eventos compatíveis com instâncias de objetos de aprendizado.

#### Atualização

Depois que uma instância é criada, o evento **LEARNING_OBJECT_INSTANCE_MODIFICATION** é gerado. As instâncias do objeto de aprendizado no Adobe Learning Manager não têm um estado **Rascunho**; portanto, o Adobe Learning Manager não oferece suporte a um evento **LEARNING_OBJECT_INSTANCE_DRAFT**. Este evento é gerado sempre que uma instância é criada, modificada ou desativada.

Além de ser gerado quando uma instância é criada, atualizada ou desativada, este evento também é gerado automaticamente quando seu objeto de aprendizado pai está marcado como **Desativado**. Isso ocorre porque, quando um objeto de aprendizado é desativado, as instâncias subjacentes também precisam ser marcadas como **Desativadas**.

#### Excluir

Quando uma instância é excluída, o evento **LEARNING_OBJECT_INSTANCE_DELETION** é gerado. Esse evento se aplica somente a instâncias do curso que contêm módulos de ritmo individualizado, pois o Adobe Learning Manager permite que apenas administradores excluam instâncias do curso em que o tipo de módulo é de ritmo individualizado. O Adobe Learning Manager não oferece suporte a exclusões explícitas para outros tipos de módulos de curso, não para instâncias de caminho de aprendizado ou instâncias de certificação.

A instância do objeto de aprendizado também tem um equivalente que não é em tempo real, exposto como parte do evento **LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH**. Esse evento é acionado durante a criação ou modificação de uma instância do objeto de aprendizado por meio do fluxo de trabalho de migração. Como as operações de rascunho ou exclusão para instâncias de objetos de aprendizado não são suportadas na migração, os eventos de rascunho ou exclusão correspondentes não estão disponíveis.

### Inscrição

Depois que um aluno executa uma ação de inscrição, um evento de inscrição em tempo real é acionado. Dependendo do tipo de objeto de aprendizado, o evento de inscrição em tempo real pode se enquadrar em uma das seguintes categorias:

* COURSE_ENROLLMENT
* LEARNING_PATH_ENROLLMENT
* CERTIFICATION_ENROLLMENT

Os eventos de inscrição têm contrapartes em lote além desses eventos em tempo real. Sempre que uma inscrição é acionada por um administrador, gerente ou plataforma, eventos de inscrição em tempo não real são acionados. Com base no tipo de objeto de aprendizado, o evento de inscrição em lote pode ser um dos seguintes:

* COURSE_ENROLLMENT_BATCH
* LEARNING_PATH_ENROLLMENT_BATCH
* CERTIFICATION_ENROLLMENT_BATCH

### Cancelamento da inscrição

Quando um aluno executa uma ação de cancelamento de inscrição, um evento de cancelamento de inscrição em tempo real é acionado. Dependendo do tipo de objeto de aprendizado, o evento de cancelamento de inscrição em tempo real pode se enquadrar em uma das seguintes categorias:

* COURSE_UNENROLLMENT
* LEARNING_PATH_UNENROLLMENT
* CERTIFICATION_UNENROLLMENT

Além desses eventos, também há eventos de cancelamento de inscrição em lote. Sempre que um cancelamento de inscrição é marcado por um administrador, gerente ou plataforma, eventos de cancelamento de inscrição em tempo não real são acionados. Com base no tipo de objeto de aprendizado, o evento de cancelamento de inscrição em lote pode ser um dos seguintes:

* COURSE_UNENROLLMENT_BATCH
* LEARNING_PATH_UNENROLLMENT_BATCH
* CERTIFICATION_UNENROLLMENT_BATCH

### Conclusão

O evento de conclusão em tempo real é acionado sempre que um aluno conclui um objeto de aprendizado. Com base no tipo de objeto de aprendizado, o evento de conclusão em tempo real pode se enquadrar em uma das seguintes categorias:

* COURSE_COMPLETED
* LEARNING_PATH_COMPLETED
* CERTIFICATION_COMPLETED

Além desses eventos em tempo real, também há eventos de conclusão de lote. Por exemplo, quando um administrador, gerente ou plataforma marca um objeto de aprendizado como concluído, os eventos de conclusão em tempo não real são acionados. Com base no tipo de objeto de aprendizado, o evento de conclusão de lote pode se enquadrar em uma das seguintes categorias:

* COURSE_COMPLETED_BATCH
* LEARNING_PATH_COMPLETED_BATCH
* CERTIFICATION_COMPLETED_BATCH

### Progresso do aluno

Sempre que um aluno se inscreve em um objeto de aprendizado e inicia o módulo, seu progresso é monitorado. Estes dados estão incluídos no evento **LEARNER_PROGRESS**. O evento pode ser atrasado em até 15 minutos, já que o rastreamento do progresso depende de uma complexa lógica de agregação, que não é em tempo real.

### Estatísticas de CI

O evento em tempo real **CI_STATS** é disparado sempre que há uma alteração na disponibilidade de vaga ou lista de espera para uma instância do curso. Esses dados são capturados somente no nível da instância. Além disso, esse evento é acionado para cursos e não para outros caminhos de aprendizado ou certificações, pois a disponibilidade de vaga e lista de espera são atributos específicos de um curso e sua instância.

## Ordenação de eventos

O Adobe Learning Manager garante que os eventos sejam solicitados para cada conta. No entanto, pode haver discrepâncias ao correlacionar mensagens entre eventos de inscrição ou conclusão e andamento. Isso acontece porque o evento de progresso do aluno pode ser atrasado em até 15 minutos, pois o rastreamento do progresso depende de uma lógica de agregação complexa, que não é em tempo real. Além disso, os eventos de andamento vêm de diferentes fontes de dados, portanto, sua ordem não pode ser garantida em relação aos eventos de inscrição e conclusão. Portanto, a Adobe Learning Manager fornece práticas recomendadas para clientes ao ouvir esses eventos.

Se o evento de conclusão ocorrer antes do evento de progresso do aluno, o cliente poderá ignorar o evento de progresso do aluno. Isso ocorre porque o evento de progresso do aluno pode ser atrasado em até 15 minutos, enquanto o evento de conclusão pode ser acionado antes do evento de progresso ser recebido. Como o recebimento de um evento de conclusão indica que o objeto de aprendizado foi concluído, isso significa que o progresso atingiu 100%.

No caso raro em que o evento de inscrição ocorre após o evento de progresso do aluno, o cliente pode ignorar o evento de inscrição. Isso ocorre porque o progresso só pode ser acompanhado depois que o aluno se inscreve no objeto de aprendizado. Em outras palavras, receber um evento de progresso indica que o objeto de aprendizado foi iniciado, o que só acontece após uma inscrição bem-sucedida.

## Eventos em tempo real vs. eventos em lote

Certos eventos têm equivalentes em tempo real e não em tempo real, conforme mencionado acima. Pode haver perguntas sobre quando inscrever-se em eventos em tempo real e quando inscrever-se em eventos que não são em tempo real. Veja a seguir as diretrizes que podem ser seguidas com base nas entidades descritas acima.

### Eventos em tempo real

| S.No | Eventos do Webhook | Descrição |
|---|---|---|
| 1 | CI_STATS | Acionado quando há uma alteração na disponibilidade de vagas ou listas de espera para uma instância do curso. |
| 2 | COURSE_ENROLLMENT | Acionado quando um aluno se inscreve em um curso. |
| 3 | COURSE_COMPLETED | Acionado quando um aluno conclui um curso. |
| 4 | LEARNING_PATH_ENROLLMENT | Acionado quando um aluno se inscreve em um caminho de aprendizado. |
| 5 | LEARNING_PATH_COMPLETED | Acionado quando um aluno conclui um caminho de aprendizado. |
| 6 | CERTIFICATION_ENROLLMENT | Acionado quando um aluno se inscreve em uma certificação. |
| 7 | CERTIFICATION_COMPLETED | Acionado quando um aluno conclui uma certificação. |
| 8 | COURSE_UNENROLLMENT | Acionado quando um aluno cancela a inscrição em um curso. |
| 9 | LEARNING_PATH_UNENROLLMENT | Acionado quando um aluno cancela a inscrição em um caminho de aprendizado. |
| 10 | CERTIFICATION_UNENROLLMENT | Acionado quando um aluno cancela a inscrição de uma certificação. |
| 11 | LEARNING_OBJECT_DRAFT | Acionado durante a criação de um objeto de aprendizado no estado de rascunho. |
| 12 | LEARNING_OBJECT_DELETION | Acionado durante a exclusão de um objeto de aprendizado. |
| 13 | LEARNING_OBJECT_MODIFICATION | Acionado durante a modificação de um objeto de aprendizado. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Acionado durante a criação ou modificação de uma instância do objeto de aprendizado.<div><b>Observação:</b> é recomendável usar as instâncias do curso somente depois que o curso for publicado.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Acionado durante a exclusão de uma instância do objeto de aprendizado. |

### Eventos que não são de tempo real

| S.No | Eventos do Webhook | Descrição |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Acionado quando um administrador/gerente/plataforma inscreve alunos em um curso. |
| 2 | COURSE_COMPLETED_BATCH | Acionado quando um administrador/gerente/plataforma marca um curso como concluído. |
| 3 | LEARNING_PATH_ENROLLMENT_BATCH | Acionado quando um administrador/gerente/plataforma inscreve alunos em um caminho de aprendizado. |
| 4 | LEARNING_PATH_COMPLETED_BATCH | Acionado quando um administrador/gerente marca um caminho de aprendizado como concluído. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Acionado quando um administrador/gerente/plataforma inscreve alunos em uma certificação. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Acionado quando um administrador/gerente/plataforma marca uma certificação como concluída. |
| 7 | LEARNER_PROGRESS | Controla o progresso de um aluno quando um módulo é concluído. |
| 8 | COURSE_UNENROLLMENT_BATCH | Acionado quando um administrador/gerente/plataforma cancela a inscrição dos alunos em um curso. |
| 9 | LEARNING_PATH_UNENROLLMENT_BATCH | Acionado quando um administrador/gerente/plataforma cancela a inscrição dos alunos em um caminho de aprendizado. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Acionado quando um administrador/gerente/plataforma cancela a inscrição dos alunos de uma certificação. |
| 11 | LEARNING_OBJECT_MODIFICATION_BATCH | Acionado durante a modificação de um objeto de aprendizado por meio do fluxo de trabalho de migração. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Acionado durante a criação ou modificação de uma instância do objeto de aprendizado por meio do fluxo de trabalho de migração. |

### Objetos de aprendizado e suas instâncias

* Assine eventos em tempo real sempre que quiser ouvir alterações em objetos de aprendizado feitas por meio de ações de interface do usuário por funções como administrador, autor etc.
* Inscreva-se em eventos em lote ou em tempo não real sempre que quiser ouvir as alterações feitas em objetos de aprendizado por meio de fluxos de trabalho de migração.

### Inscrição, cancelamento de inscrição e conclusão

* Inscreva-se em eventos em tempo real sempre que desejar ouvir inscrições, cancelar inscrições ou conclusões executadas pelos alunos.
* Inscreva-se em eventos em lote ou que não sejam em tempo real sempre que desejar ouvir inscrições, cancelar inscrições ou conclusões marcadas por Administrador, Gerente, Plataforma etc.

### Progresso do aluno

* Inscreva-se no evento sempre que quiser ouvir as alterações de progresso de um aluno.

>[!NOTE]
>
>Nos cenários acima (inscrição, cancelamento de inscrição, conclusão e progresso), as composições de atributo que consistem em userId e loInstanceId podem identificar exclusivamente um registro.

### Estatísticas da instância do curso

* Assine o evento **CI_STATS** em tempo real sempre que desejar ouvir alterações na disponibilidade de estação ou lista de espera.

## Carga de evento do Webhook

Como parte da carga de resposta dos webhooks, o Adobe Learning Manager emitirá os atributos necessários para identificar exclusivamente uma entidade. Eles serão emitidos no mesmo formato e de acordo com os padrões usados pela API pública, garantindo que os dados do webhook estejam sincronizados com os dados da API pública. Exiba [cargas de exemplo](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#sample-payloads-for-the-events) para ver cargas para os vários eventos.

## Usar webhooks para criar um banco de dados externo ou serviço de notificação

Um dos casos de uso que ouvimos sobre a utilidade dos webhooks é a criação de um banco de dados do lado do cliente. O Adobe Learning Manager tem seu próprio banco de dados e esquema, mas os clientes não têm acesso a eles.

A pergunta é: como os clientes podem criar um banco de dados usando eventos de webhooks?

Como o Adobe Learning Manager não exibirá diretamente os registros de tabela e o esquema, os clientes podem confiar na solução Webhooks para criar um banco de dados externo utilizando os eventos para preenchê-lo. Nesta versão, estamos fornecendo eventos para objetos de aprendizado, instâncias de objeto de aprendizado, inscrição, cancelamento de inscrição, conclusão, progresso e estatísticas de instância do curso.

### Criar um banco de dados a partir de eventos do objeto de aprendizado

Os eventos do objeto de aprendizado expõem `loId` e `loType` para identificar uma entidade. No entanto, esses atributos por si só não são suficientes para criar um banco de dados de objetos de aprendizado externo. Os clientes precisarão de campos adicionais para descrever melhor o objeto de aprendizado.
Há duas abordagens para obter os dados adicionais:

#### Gerar um relatório de dados de treinamento para buscar todos os dados

Essa abordagem deve ser usada quando os objetos de aprendizado são criados em massa por meio de fluxos de trabalho como a migração. A meta aqui é gerar o relatório de **[!UICONTROL Dados de Treinamento]** com todos os objetos de aprendizado assimilados como parte do fluxo de trabalho de migração. Para otimizar o processo de importação, é recomendável definir a hora de início da exportação para a hora em que a migração foi acionada. Isso garantirá que apenas os objetos de aprendizado trazidos por meio da migração sejam exportados no relatório, pois os dados históricos já estarão disponíveis no banco de dados do cliente.

#### Consulte as informações da API pública GET /learningObjects - Admin scope

Essa abordagem deve ser usada quando os objetos de aprendizado são criados por meio de fluxos de trabalho em tempo real. O cliente deve ter sua própria camada de cache para colocar em lote os objetos de aprendizado emitidos por meio dos eventos e, em seguida, consultar a API `GET /learningObjects` passando essas IDs de objetos de aprendizado. O motivo para ter uma camada de cache é garantir que os limites de taxa da API pública não sejam excedidos. Atualmente, temos limites de taxa de administração definidos para 500 solicitações por hora para ` GET /learningObject` APIs. Se esse limite for excedido, o serviço público da API responderá com uma mensagem **HTTP 429 Muitas Solicitações**.

### Criação de banco de dados a partir da instância do objeto de aprendizado e eventos CI_STATS

O evento Instância do objeto de aprendizado emite os atributos `loInstanceId`, `loId` e `loType` para cursos e caminhos de aprendizado. Da mesma forma, o evento **CI_STATS** só é aplicável aos cursos, pois `seatLimit`, `seatAvailability`, `waitListLimit`, `waitlistAvailability` etc., só são aplicáveis aos cursos.

Em certos casos de uso, são necessários dados de instância adicionais, como nome de instância, estado etc. Para buscar dados de instância adicionais, deve-se seguir a seguinte abordagem:

#### Consulte as informações de public-api GET /learningobjects - Admin scope

Os clientes podem consumir a API `GET /learningObjects` conforme mencionado acima, juntamente com instâncias incluídas para buscar as informações sobre instâncias. Eles ainda devem seguir a abordagem mencionada na [seção](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#query-the-information-from-the-public-api-get-learningobjects-admin-scope) para garantir que os limites de taxa não sejam violados.


>[!NOTE]
>
>1. As certificações não têm o conceito de instâncias no ALM.
>2. Não há necessidade de buscar dados adicionais para CI_STATS, pois as mesmas informações já teriam sido buscadas como parte dos eventos de Instância do objeto de aprendizado.

### Criar banco de dados a partir de eventos de inscrição, cancelamento de inscrição, conclusão e progresso

A inscrição do aluno, o cancelamento de inscrição, a conclusão e o progresso são emitidos como eventos separados no Adobe Learning Manager. O aluno é identificado pelo atributo `userId`. No entanto, pode haver alguns cenários em que informações adicionais do aluno, como nome, e-mail etc., são necessárias para workflows downstream no lado do cliente. Para buscar esses dados, os clientes podem seguir a abordagem descrita abaixo:

#### Exportar o relatório de usuário do administrador ou conectores

Essa abordagem deve ser seguida sempre que houver fluxos de trabalho em massa envolvidos, como inscrição em massa, cancelamento de inscrição em massa etc. O Relatório de usuário do Adobe Learning Manager contém todas as informações relacionadas a um usuário. Ao correlacionar a `userId` obtida do evento do webhook, os clientes podem pesquisar este relatório (que pode ser exposto no lado do cliente como um banco de dados, cache ou ponto de extremidade de API) para buscar detalhes adicionais, como Nome, Email, UUID etc. Essa abordagem pode ser usada para sincronizar usuários semanalmente ou diariamente.

#### Consultar informações da API pública GET /users - Escopo do administrador

Essa abordagem pode ser seguida quando os usuários não estão disponíveis no relatório acima. A combinação das abordagens 1 e 2 garante que todos os usuários existentes que foram criados no passado possam ser cobertos pelo **[!UICONTROL Relatório de usuários]**, enquanto os usuários recém-criados ainda podem ser buscados na API. Se o **[!UICONTROL Relatório do Usuário]** não tiver os dados, o cliente poderá enviar as userIds como argumentos de entrada para a API `GET /users` para buscar informações do usuário. Essas informações devem ser armazenadas em cache no lado do cliente para evitar invocações repetidas da API pública para o mesmo conjunto de usuários. Observe que atualmente temos limites de taxa de administração definidos para 500 solicitações por hora para APIs GET /users. Qualquer solicitação além desse limite resultará em uma resposta **HTTP 429 Muitas Solicitações**.

## Tolerância a falhas

O sistema de webhook ALM tolerante a falhas fornece recomendações para que os assinantes tratem de possíveis problemas, como perda de evento, eventos duplicados e entrega fora de ordem.

O ALM tem o tempo limite de conexão configurado para 10 segundos e o tempo limite do soquete configurado para 5 segundos. A expectativa é que o cliente confirme a mensagem assim que recebê-la. Isso garante que o cliente não fique atrasado ao processar mensagens. Caso haja algum processamento downstream que consuma muito tempo, o cliente ainda deve confirmar o evento instantaneamente e, em seguida, lidar com o processamento downstream no final.

### Retenção de dados

Os eventos são mantidos por 7 dias. Se não forem processados dentro desse prazo, serão perdidos permanentemente. Se a recuperação ocorrer no último dia e mais tempo for necessário, o sistema não estenderá o período de retenção.
Se os eventos forem produzidos mais rapidamente do que são consumidos, alguns eventos podem ser perdidos. Embora isso seja incomum, os assinantes devem monitorar para evitar que se torne um problema de longo prazo.

### Desativação de webhooks

Quando um assinante não responde a eventos de webhook, o sistema ALM tenta executar novamente os webhooks usando o backoff exponencial para evitar sobrecarregar o assinante.

O processo de repetição começa com um intervalo inicial de 5 segundos. Se o assinante não responder, o tempo de espera dobrará para 10, 20, 40 e 80 segundos, eventualmente aumentando para um máximo de 5 minutos. Quando atingir 5 minutos, o sistema continuará tentando a cada 5 minutos até que o período de retenção de 7 dias termine. Se o assinante ainda não responder durante esse período inteiro, o webhook será desativado automaticamente. Um e-mail de lembrete será enviado ao assinante em intervalos regulares.

### Duplicar eventos

Se um assinante demorar mais de 5 segundos para responder após o processamento de um evento, o sistema poderá tentar processar o mesmo evento novamente. É recomendável usar IDs de eventos para controlar quais eventos já foram processados. Além disso, se o webhook falhar após enviar o evento, mas antes de salvar que ele tenha sido processado, o mesmo grupo de eventos poderá ser repetido. É recomendável usar IDs de lote ou IDs de evento individuais para reconhecer e ignorar duplicatas.

### Recomendação para tolerância a falhas

Para evitar essas falhas, os assinantes devem monitorar ativamente os eventos do webhook e configurar alertas para problemas como eventos perdidos, entregas duplicadas ou sequências fora de ordem.

## Diretrizes específicas para eventos de webhook

1. Se você receber um evento LEARNER_PROGRESS primeiro, ignore os eventos listados abaixo:

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEARNING_PATH_ENROLLMENT
   * LEARNING_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Ignore o evento LEARNER_PROGRESS se ele vier após os seguintes eventos:

   * COURSE_COMPLETED
   * COURSE_COMPLETED_BATCH
   * LEARNING_PATH_COMPLETED
   * LEARNING_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Use o campo de data/hora para determinar se o evento deve ser ignorado ou processado, exceto para o evento LEARNER_PROGRESS.

## Práticas recomendadas de consumo de eventos de webhooks

* A solução de webhook é usada para lidar com sistemas de alto throughput em que a velocidade e a baixa latência são essenciais. Portanto, o cliente deve garantir que o evento seja confirmado assim que for recebido. Mesmo se for necessário um processamento adicional por parte do cliente (como a busca de dados de relatórios, API ou a execução de outras ações), a confirmação deve ser enviada assim que o evento for recebido e cabe ao cliente processar o evento posteriormente.
* Não reconhecer o evento o mais rápido possível pode afetar a natureza em tempo real dos eventos, já que os eventos subsequentes só serão emitidos depois que a confirmação anterior for recebida.
* Os clientes podem responder com um código de status HTTP 202 Aceito para confirmar que o evento foi aceito.

## Limitações

* As ajudas de tarefa não são consideradas para eventos do Webhook na categoria de OAs porque geralmente são usadas para ajudar os alunos a concluir outros objetos de aprendizado.
* Uma desativação da instância do objeto de aprendizado seria considerada um evento de atualização. Não haveria um evento de exclusão para uma instância, pois ela só pode ser desativada, e não excluída.
* As alterações de sessão seriam capturadas como parte do evento de atualização da instância. Isso se aplica apenas aos cursos. Não haverá propagação ascendente de entidades de nível inferior para instâncias do caminho de aprendizado ou instâncias de certificação.
* Se um caminho de aprendizado contiver um curso e um aluno concluir o curso por meio do caminho de aprendizado, dois eventos **LearnerProgress** serão gerados: um para o curso e outro para o caminho de aprendizado.
* Determinados fluxos de trabalho calculam atributos de objetos de aprendizado, como duração e tipo de entrega, de forma assíncrona. Portanto, os eventos para esses objetos de aprendizado serão gerados assim que o trabalho cron terminar o processamento.
* Se um curso for inscrito por meio de um programa de aprendizado ou certificação pai, os eventos de inscrição, cancelamento de inscrição e conclusão serão acionados apenas para o programa de aprendizado ou certificação pai. Esses eventos não serão acionados para o curso secundário, pois a inscrição ocorreu indiretamente.
* Os webhooks só têm suporte para contas com status **[!UICONTROL ATIVO]**. Eles não estão disponíveis para contas **[!UICONTROL DE AVALIAÇÃO]** ou **[!UICONTROL INATIVAS]**.

## Cargas de exemplo para os eventos

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345-0458-4450-b5dd-6bc1ef4f8b50",
      "eventName": "CI_STATS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456785-LoSt",
      "data": {
        "loInstanceId": "course:12345678_14448475",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345c1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c2345c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12345823000-040363-12018-0",
      "data": {
        "userId": 11080928,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c23458c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
    ]
}
```

+++

+++CAMINHO_DE_APRENDIZADO_INSCRIÇÃO

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234567",
        "loInstanceId": "learningProgram:1234567_109139",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CAMINHO_DE_APRENDIZADO_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12340791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234557",
        "loInstanceId": "learningProgram:1234557_109139",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CAMINHO_DE_APRENDIZADO_CONCLUÍDO

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123404e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++CAMINHO_DE_APRENDIZADO_LOTE_CONCLUÍDO

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12344e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234e776-148e-4128-80e9-b896a460b655",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12344672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123472ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234524713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:123456798",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123454768000-040654-756257-0",
      "data": {
        "userId": 123456728,
        "loId": "certification:123418",
        "loInstanceId": "certification:134518_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123453bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNER_PROGRESS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "d1234d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12380928,
        "loInstanceId": "course:7232090_10423047",
        "dateStarted": "2024-11-08T03:49:52.000Z",
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3237817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1345506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f2317817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "17235506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++CAMINHO_DE_APRENDIZADO_CANCELAR INSCRIÇÃO

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "823df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
      }
    }
]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e23f878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7232766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235507900000-040304-1065-0",
      "data": {
        "userId": 12311591,
        "loId": "certification:123199",
        "loInstanceId": "certification:123199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7202766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1735507900000-040304-1065-0",
      "data": {
        "userId": 12511591,
        "loId": "certification:139199",
        "loInstanceId": "certification:139199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345da9f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234519188000-040344-48604-0",
      "data": {
        "loId": "course:1234091",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234a690-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605296000-040656-662792-0",
      "data": {
        "loId": "course:12319716",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "223e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "1234e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
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

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1231da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12d16e90-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605491000-040657-236307-0",
      "data": {
        "loInstanceId": "course:12319674_14453849",
        "loId": "course:12319674",
        "loType": "course"
      }
    }
  ]
}
```

+++
