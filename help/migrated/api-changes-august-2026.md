---
description: Alterações de API no ALM
jcr-language: en_us
title: Alterações na API na versão de agosto de 2026 do Adobe Learning Manager
source-git-commit: 857c94b5e9a7460d63a6dacc0beeddd41f362bf9
workflow-type: tm+mt
source-wordcount: '3354'
ht-degree: 3%

---


# Alterações na API na versão de agosto de 2026 do Adobe Learning Manager

## API do administrador de grupos de usuários no Adobe Learning Manager

Esta versão adiciona três novos endpoints de API públicos com escopo de administrador para gerenciar grupos de usuários personalizados de forma programática. Você pode criar, renomear e excluir grupos de usuários personalizados sem usar o aplicativo Admin, permitindo automatizar o gerenciamento de grupos como parte de sua identidade ou fluxos de trabalho de provisionamento.

Esses endpoints funcionam apenas com grupos de usuários personalizados. Os grupos gerenciados pelo sistema, como o grupo Todos os usuários e os grupos de usuários gerados automaticamente, têm somente leitura: true na resposta da API e não pode ser modificado nem excluído por meio desses endpoints.

Para obter os requisitos de autenticação da API, consulte [Autenticação da API do Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### Pontos finais de API de grupos de usuários

Todos os três pontos de extremidade exigem um token de acesso de administrador com permissões de gravação (ROLE_ADMIN).

| **Método** | **Caminho** | **Operação** | **Código de êxito** |
|---|---|---|---|
| POST | /primeapi/v2/userGroups | Criar um grupo de usuários personalizado | 201 Criado |
| PUT | /primeapi/v2/userGroups/{id} | Atualizar o nome ou a descrição de um grupo | 200 OK |
| DELETE | /primeapi/v2/userGroups/{id} | Excluir um grupo de usuários personalizado | 204 Sem conteúdo |

## **Cabeçalhos de solicitação comuns**

Todos os três pontos de extremidade exigem os seguintes cabeçalhos.

```
Authorization: Bearer \<access-token\>
X-acap-user: \<user-id\>
X-acap-account: \<account-id\>
X-acap-caller-role: ROLE_ADMIN
Content-Type: application/vnd.api+json
Accept: application/vnd.api+json
```

### **Criar um grupo de usuários**

```
POST /primeapi/v2/userGroups
```

Cria um novo grupo de usuários personalizado com uma lista inicial de membros. O grupo fica imediatamente disponível para uso no aplicativo do administrador.

#### **Corpo da solicitação**

```
{
  "name": "Marketing Team",
  "description": "Custom user group for marketing onboarding",
  "data": [
    { "type": "user", "id": "11282373" },
    { "type": "user", "id": "11282374" }
  ]
}
```

#### **Parâmetros de solicitação**

| **Parâmetro** | **Obrigatório** | **Tipo** | **Descrição** |
|---------------|--------------|----------|-------------------------------------------------------------------------------------|
| nome | Sim | cadeia de caracteres | Nome de exibição do grupo. Não pode estar em branco ou conter apenas espaços em branco. |
| descrição | Não | cadeia de caracteres | Descrição opcional da finalidade do grupo. |
| dados | Sim | matriz | Lista inicial de membros. Mínimo de 1 item, máximo de 100 itens. |
| data[].type | Sim | cadeia de caracteres | Deve ser “user”. Nenhum outro tipo de recurso é aceito. |
| data[].id | Sim | cadeia de caracteres | Cadeia de caracteres numérica de ID de usuário. O usuário deve pertencer à conta e ter o status ATIVO. |

> **Observação:** a matriz de dados é usada apenas na criação para definir a lista de membros inicial. Para adicionar ou remover membros após a criação, use os endpoints de associação ao grupo de usuários existente.

#### **Resposta 201 Criada**

```
{
  "links": {
    "self": "https://<host>/primeapi/v2/userGroups"
  },
  "data": {
    "id": "2769204",
    "type": "userGroup",
    "attributes": {
      "dateCreated": "2026-06-04T14:19:53.000Z",
      "description": "Custom user group for marketing onboarding",
      "name": "Marketing Team",
      "readOnly": false,
      "userCount": 2
    }
  }
}
```

#### **POST de regras de validação**

| **#** | **Validação** | **Código de erro** | **Acionador** |
|-------|-------------------------------------------------------|----------------------------------------------------------|------------------------------------------------|
| 1 | o nome está presente e não está em branco | USERGROUP_CREATE_NAME_REQUIRED | Nome omitido ou somente espaço em branco |
| 2 | os dados contêm pelo menos um usuário | USERGROUP_CREATE_USERS_REQUIRED | dados ausentes ou matriz vazia |
| 3 | os dados contêm 100 usuários ou menos | USERGROUP_USERS_MAX_LIMIT_EXCEEDED | Mais de 100 entradas nos dados[] |
| 4 | Todas as IDs de usuário são sequências numéricas | INVALID_USER_IDS | Cadeia de caracteres não numérica encontrada em data[].id |
| 5 | Todos os usuários existem na conta e têm o status ATIVO | INVALID_USER_IDS / USERGROUP_CREATE_USERS_NOT_IN_ACCOUNT | Usuário não encontrado ou não ativo |
| 6 | A conta não atingiu o limite de grupos personalizados | 400 | Limite em nível de conta para grupos personalizados excedido |

### **Atualizar um grupo de usuários**

```
PUT /primeapi/v2/userGroups/{id}
```

Atualiza o nome e/ou a descrição de um grupo de usuários personalizado existente. Este ponto de extremidade não pode adicionar ou remover membros do grupo.

Qualquer um dos campos pode ser omitido; a omissão de um campo deixa seu valor atual inalterado. Passar nulo para descrição limpa-o. A transmissão de uma sequência em branco para o nome foi rejeitada.

#### **Corpo da solicitação**

```json
{
  "name": "Updated Group Name",
  "description": "Updated description text"
}
```

#### **Parâmetros de solicitação**

| **Parâmetro** | **Obrigatório** | **Tipo** | **Descrição** |
|---------------|--------------|----------|---------------------------------------------------------------------------|
| nome | Sim | cadeia de caracteres | Novo nome para exibição. Não deve ficar em branco se fornecido. Omita para deixar inalterado. |
| descrição | Não | cadeia de caracteres | Nova descrição. Passar nulo para limpar. Omita para deixar inalterado. |

#### **Resposta 200 OK**

```
{
  "data": {
    "type": "userGroup",
    "id": "2767870",
    "attributes": {
      "name": "Updated Group Name",
      "description": "Updated description text",
      "readOnly": false,
      "state": "Active",
      "userCount": 3
    }
  }
}
```

#### **PUT de regras de validação**

| **#** | **Validação** | **Código de erro** | **Acionador** |
|-------|-------------------------------------|----------------------------------------|----------------------------------------------------------|
| 1 | dados nulos ou ausentes | USERGROUP_UPDATE_USERS_NOT_ALLOWED | O chamador passou dados não nulos tentando alterar a associação |
| 2 | o nome, se fornecido, não está em branco | USERGROUP_UPDATE_NAME_BLANK | nome enviado como cadeia de caracteres somente de espaço em branco |
| 3 | O grupo existe nesta conta | INVALID_USER_GROUP_ID | Parâmetro de caminho {id} desconhecido |
| 4 | O grupo ainda não foi excluído | DELETED_USERGROUP | O grupo foi excluído anteriormente |
| 5 | O grupo readOnly é falso | READ_ONLY_USERGROUP | Grupo gerenciado pelo sistema |
| 6 | Grupo é um tipo personalizado (não sistema) | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Tipo de grupo interno do sistema |

### **Excluir um grupo de usuários**

```
DELETE /primeapi/v2/userGroups/{id}
```

Marca o grupo de usuários personalizado especificado como excluído. O registro do grupo não é removido permanentemente; seu estado é definido como EXCLUÍDO, o que o torna invisível no aplicativo do administrador e inelegível para uso em novas configurações. A ID do grupo não pode ser reutilizada.

#### **Exemplo de solicitação**

```
DELETE /primeapi/v2/userGroups/2767870
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_ADMIN
```

#### **Resposta 204 Sem Conteúdo**

O corpo da resposta está vazio.

> **Observação:** DELETE não é idempotente. O envio de uma segunda solicitação de DELETE para o mesmo ID de grupo retorna um erro 400 com o código DELETED_USERGROUP — não 204. Tratar uma resposta 400 DELETED_USERGROUP como confirmação de que o grupo já foi excluído. Não há suporte para exclusão em massa; cada grupo requer uma solicitação DELETE separada.

#### **DELETE de regras de validação**

| **#** | **Validação** | **Código de erro** | **Acionador** |
|-------|-------------------------------------|----------------------------------------|---------------------------------------------------|
| 1 | O grupo existe nesta conta | INVALID_USER_GROUP_ID | Parâmetro de caminho {id} desconhecido |
| 2 | O grupo ainda não foi excluído | DELETED_USERGROUP | Repita o DELETE em um grupo que já esteja no estado DELETED |
| 3 | O grupo readOnly é falso | READ_ONLY_USERGROUP | Grupo gerenciado pelo sistema |
| 4 | Grupo é um tipo personalizado (não sistema) | USERGROUP_UPDATE_OPERATION_NOT_ALLOWED | Tipo de grupo interno do sistema |

## API de aprendizado externa no Adobe Learning Manager

Esta versão adiciona cinco novos endpoints de API com escopo de aluno para o recurso de aprendizado externo. Esses endpoints permitem que os alunos criem, recuperem e atualizem envios de aprendizado externos de forma programática, por exemplo, a partir de um aplicativo móvel, um sistema de RH integrado ou um portal de aprendizado personalizado.

O fluxo de trabalho de aprendizado externo por meio da API espelha o fluxo de trabalho no aplicativo do aluno: um aluno envia detalhes de treinamento e um documento de prova opcional, seu gerente direto recebe uma notificação para revisar o envio e, na aprovação, o registro aparece na transcrição do aluno.

Todos os cinco pontos de extremidade têm escopo do aluno. Um aluno só pode acessar seus próprios envios — a API retorna um erro se um aluno tentar acessar os dados de outro aluno.

Para obter os requisitos de autenticação da API, consulte [Autenticação da API do Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual#authentication-using-oauth-20).

### Pontos de extremidade da API de aprendizado externos

Todos os pontos de extremidade exigem um token de acesso do aluno (ROLE_LEARNER).

| **Método** | **Caminho** | **Operação** | **Código de êxito** |
|------------|---------------------------------------|----------------------------------|------------------|
| GET | /primeapi/v2/externalLearningSettings | Buscar configuração do formulário da conta | 200 OK |
| GET | /primeapi/v2/externalLearnings | Listar os envios do chamador | 200 OK |
| GET | /primeapi/v2/externalLearnings/{id} | Buscar um único envio | 200 OK |
| POST | /primeapi/v2/externalLearnings | Criar um novo envio | 201 Criado |
| PUT | /primeapi/v2/externalLearnings/{id} | Atualizar um envio pendente | 200 OK |

### Cabeçalhos de solicitação comuns

```
Authorization: Bearer <access-token>
X-acap-user: <user-id>
X-acap-account: <account-id>
X-acap-caller-role: ROLE_LEARNER
Accept: application/vnd.api+json
Content-Type: application/vnd.api+json (POST and PUT only)
```

### Ciclo de vida do status do envio

| **Status** | **Definido por** | **Significado** | **O aluno pode atualizar?** |
|------------|------------------|-----------------------------------------|-----------------------------|
| PENDENTE | Sistema ao criar | Aguardando revisão do gerente | Sim- via PUT |
| APROVADO | Gerente | Aceito; aparece na transcrição do aluno | No- PUT retorna 409 |
| REJEITADO | Gerente | Recusado; comentário de revisão anexado | Não - criar um novo envio |

APROVADO e REJEITADO são estados terminais. Um envio rejeitado não pode ser reaberto; o aluno deve criar um novo envio.

### Buscar configuração do formulário da conta

```
GET /primeapi/v2/externalLearningSettings
```

Retorna a configuração do formulário no nível da conta. Chame esse ponto de extremidade antes de renderizar um formulário de envio. A resposta define quais campos exibir, quais são obrigatórios, seus tipos de dados e quaisquer campos personalizados configurados pelo administrador.

Verifique o atributo de nível superior ativado antes de continuar, se falso, o recurso Aprendizado externo não está ativo para esta conta e os pontos de extremidade de envio retornarão erros.

#### Resposta 200 OK

```
{
  "data": {
    "id": "8627",
    "type": "externalLearningSettings",
    "attributes": {
      "enabled": true,
      "updatedAt": "2026-06-05T06:51:20.000Z",
      "coreFields": [
        { "id": "title", "type": "TEXT", "mandatory": true, "editable": false, "order": 0 },
        { "id": "description_notes", "type": "TEXT", "mandatory": false, "editable": true, "order": 1 },
        { "id": "date", "type": "TIMESTAMP", "mandatory": false, "editable": true, "order": 2 },
        { "id": "score", "type": "NUMBER", "mandatory": true, "editable": true, "order": 3 },
        { "id": "duration", "type": "TEXT", "mandatory": false, "editable": true, "order": 4 },
        { "id": "attachments", "type": "FILE_UPLOAD", "mandatory": true, "editable": true, "order": 5 }
      ],
      "customFields": [
        {
          "id": "960369b2-...",
          "type": "NUMBER",
          "mandatory": true,
          "order": 0,
          "label": { "en_US": "Employee Code" }
        },
        {
          "id": "3c6cc6d9-...",
          "type": "DROPDOWN",
          "mandatory": true,
          "order": 1,
          "label": { "en_US": "Department" },
          "options": [
            { "option_id": "opt_1", "label": { "en_US": "IT" } },
            { "option_id": "opt_2", "label": { "en_US": "HR" } },
            { "option_id": "opt_3", "label": { "en_US": "FIN" } }
          ]
        }
      ]
    }
  }
}
```

#### Referência de campo principal

| **ID do campo** | **Tipo** | **Padrão obrigatório** | **Notas** |
|-------------------|-------------|-----------------------|----------------------------------------------------------------------------------------------------------|
| título | TEXTO | Sim | Nome do treinamento. Sempre presente. Não pode ser desabilitado pelo administrador. |
| description_notes | TEXTO | Não | Descrição ou observações de texto livre. |
| data | CARIMBO DE DATA/HORA | Não | Intervalo de datas. Forma de valor: { “start_date”: &quot;<ISO-Z>“, “end_date”: &quot;<ISO-Z>&quot; }. Qualquer valor pode ser nulo. |
| pontuação | NÚMERO | Sim | Forma de valor: { “completed_score”: <number>, “max_score”: <number> }. Ambos os valores devem ser numéricos. |
| duração | TEXTO | Não | String de forma livre, por exemplo “40 horas”. |
| anexos | FILE_UPLOAD | Sim | Prova de conclusão. **Não** passado dentro de campos[] — use o atributo submissionUrl de nível superior. |

Os campos personalizados são definidos pelo administrador e retornados em customFields[]. Suas IDs, tipos, sinalizadores obrigatórios, etiquetas e opções suspensas variam de acordo com a configuração da conta.

### Listar envios

```
GET /primeapi/v2/externalLearnings
```

Retorna uma lista paginada dos próprios envios do aluno autenticado, classificada por modifiedAt decrescente (modificado mais recentemente primeiro).

#### **Parâmetros de consulta**

| **Parâmetro** | **Padrão** | **Máximo** | **Descrição** |
|---------------|-------------|-------------|-------------------------------------------------------------------------------------------------------|
| página[deslocamento] | 0 | 5000 | Deslocamento de registro com base em zero. |
| página[limite] | 10 | 100 | Registros por página. Valores acima de 100 são silenciosamente fixados em 100. |
| ls_qp_status | — | — | Filtrar por status. Omitir para todos os resultados. Valores válidos: PENDING, APPROVED, REJECTED (não diferencia maiúsculas de minúsculas). |

#### **Resposta 200 OK**

```
{
  "links": {
    "next": "/primeapi/v2/externalLearnings?page[offset]=10&page[limit]=10"
  },
  "data": [
    { "id": "1001", "type": "externalLearning", "attributes": { "status": "PENDING", ... } },
    { "id": "1002", "type": "externalLearning", "attributes": { "status": "APPROVED", ... } }
  ]
}
```

### Buscar um envio

```
GET /primeapi/v2/externalLearnings/{id}
```

Retorna o registro completo de um único envio pertencente ao aluno autenticado.

#### **Resposta 200 OK

```
{
  "data": {
    "id": "1001",
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "https://<cdn-url>/cert.pdf",
      "title": "Java Fundamentals Certification",
      "status": "PENDING",
      "creationSource": "LEARNER",
      "createdAt": "2026-04-14T08:30:00.000Z",
      "modifiedAt": "2026-04-16T11:45:00.000Z",
      "fields": [ "...resolved against live settings..." ]
    },
    "relationships": {
      "reviewerUser": { "data": null }
    }
  }
}
```

### Criar um envio

```
POST /primeapi/v2/externalLearnings
```

Cria um novo envio de aprendizado externo no estado PENDENTE. Todos os campos obrigatórios definidos nas configurações da conta devem ser incluídos. Após um POST bem-sucedido, o gerente do aluno recebe uma notificação na plataforma para revisar o envio.

### **Carregamento de arquivo**

O campo de anexos é tratado separadamente dos outros campos. Não o inclua dentro de campos[]. Em vez disso:

&#x200B;1. Obtenha um URL de upload S3 pré-assinado no ponto de extremidade de upload de arquivos do ALM.

&#x200B;2. Faça upload do arquivo nesse URL.

&#x200B;3. Transmita o URL resultante como o atributo submissionUrl de nível superior em sua solicitação POST.

#### **Corpo da solicitação**

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<pre-signed-upload-url>",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals Certification" },
        { "id": "description_notes", "type": "TEXT", "value": "Completed via online course platform." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": "2026-05-01T00:00:00.000Z", "end_date": "2026-05-15T00:00:00.000Z" } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 88, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "40 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1225" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_3" }
      ]
    }
  }
}
```

#### Formas de valor do campo

| **Tipo de campo** | **Forma de valor** | **Exemplo** |
|----------------|---------------------------------------------------------|----------------------------------------------------------------|
| TEXTO | String | “Fundamentos do Java” |
| NÚMERO | Objeto com reach_score e max_score | { “completed_score”: 88, “max_score”: 100 } |
| CARIMBO DE DATA/HORA | Objeto com start_date e end_date (ISO 8601 ou null) | { “start_date”: “2026-05-01T00:00:00.000Z”, “end_date”: null } |
| MENU SUSPENSO | sequência de caracteres option_id das configurações da conta | “opt_3” |
| FILE_UPLOAD | Não permitido dentro de campos[] — use submissionUrl | — |

#### POST de regras de validação

| **#** | **Validação** | **Acionador** |
|-------|-----------------------------------------------------------------|----------------------------------------------------------|
| 1 | O aprendizado externo está ativado para a conta | Sinalizador de recurso desabilitado |
| 2 | Todos os campos obrigatórios estão presentes nos campos[] | Campo obrigatório omitido |
| 3 | Cada ID de campo, tipo e forma de valor correspondem às configurações da conta | Tipo incorreto ou objeto de valor malformado |
| 4 | O tipo FILE_UPLOAD não está presente nos campos[] | Anexo enviado dentro de campos[] em vez de submissionUrl |
| 5 | submissionUrl é um URL pré-assinado S3 válido | URLs CDN e URLs não S3 rejeitadas no momento da criação |
| 6 | submissionUrl presente quando attachments.mandatory é true | Anexos são necessários, mas submissionUrl está ausente |

### Atualizar um envio

```
PUT /primeapi/v2/externalLearnings/{id}
```

Atualiza um envio PENDENTE existente. Somente envios PENDING podem ser atualizados. A tentativa de PUT de um envio APPROVED ou REJECTED retorna um erro 409.

**Este ponto de extremidade usa semântica de substituição completa.** Forneça a matriz completa fields[] em cada solicitação PUT, não apenas os campos que você está alterando. Os campos omitidos da matriz são apagados.

#### Campos que o aluno pode atualizar

| **Campo/atributo** | **O aluno pode atualizar** | **Notas** |
|-----------------------|------------------------|----------------------------------------------------------------------------|
| campos[] | Sim | Substituição completa — inclua todos os campos, não apenas os alterados |
| submissionUrl | Sim | URLs CDN são aceitas no PUT; URLs pré-assinadas S3 são necessárias somente no POST |
| reviewerUserId | Não | Definir por ação do gerente; somente leitura para o aluno |
| reviewedAt | Não | Definir por ação do gerente; somente leitura para o aluno |
| reviewerComment | Não | Definir por ação do gerente; somente leitura para o aluno |
| status | Não | Controlado pelo gerente: PENDENTE → APROVADO ou REJEITADO |
| creationSource | Não | Sempre aluno para envios criados por API |
| createdAt | Não | Definir no momento da criação; imutável |

#### Corpo da solicitação

```
{
  "data": {
    "type": "externalLearning",
    "attributes": {
      "submissionUrl": "<cdn-url>/cert-v2.pdf",
      "fields": [
        { "id": "title", "type": "TEXT", "value": "Java Fundamentals — Updated" },
        { "id": "description_notes", "type": "TEXT", "value": "Updated notes." },
        { "id": "date", "type": "TIMESTAMP", "value": { "start_date": null, "end_date": null } },
        { "id": "score", "type": "NUMBER", "value": { "achieved_score": 92, "max_score": 100 } },
        { "id": "duration", "type": "TEXT", "value": "42 hours" },
        { "id": "960369b2-...", "type": "NUMBER", "value": "1227" },
        { "id": "3c6cc6d9-...", "type": "DROPDOWN", "value": "opt_2" }
      ]
    }
  }
}
```

## API para ID de certificação relevante para o aluno e ID de certificação raiz no LT

Quando uma certificação recorrente é renovada, o Adobe Learning Manager cria uma nova versão da certificação e inscreve automaticamente os alunos ativos nela. Se a integração consultar dados de certificação diretamente em vez de depender da experiência do aluno do Adobe Learning Manager, você pode usar essa API para determinar exatamente qual versão de uma certificação recorrente é relevante para um aluno específico a qualquer momento.

### Finalidade da API

As certificações recorrentes geram uma nova ID de certificação toda vez que são renovadas. Na experiência nativa do aluno do Adobe Learning Manager, somente a versão relevante para cada aluno é exibida. As versões mais antigas são ocultadas automaticamente assim que um aluno passa para uma mais recente.

Se a sua integração recuperar dados de certificação independentemente, por exemplo, para exibir informações de certificação em um portal externo, ela pode não aplicar automaticamente essa filtragem. Sem ela, um aluno podia ver cada versão histórica de uma certificação recorrente, incluindo aquelas que não eram mais relevantes para ele, sem nenhuma indicação sobre a qual agir.

Essa API resolveu essa lacuna. Dado o ID de certificação raiz, ele retorna a versão de certificação específica que se aplica a um determinado aluno, contabilizando seu histórico de inscrição e quaisquer recorrências.

### Entender a recorrência da certificação

Quando uma certificação é configurada para recorrência, cada renovação cria uma nova versão de certificação com sua própria ID exclusiva. Todas as versões retornam a uma única **ID de certificação raiz**, a ID da certificação original quando ela foi criada pela primeira vez.

Por exemplo, uma certificação que se repete todos os meses pode produzir uma sequência de versões ao longo do tempo, onde cada nova versão é gerada automaticamente quando o intervalo de recorrência é atingido. Os alunos que estão inscritos ativamente quando ocorre uma recorrência são inscritos automaticamente na nova versão.

Como cada versão tem uma ID distinta, a versão relevante de um aluno depende de sua linha do tempo de inscrição individual:

- Um aluno que se inscreveu antes de uma recorrência e concluiu a certificação antes da próxima recorrência terá percorrido várias versões ao longo do tempo.

- Um aluno que se inscreve parcialmente em um ciclo de recorrência é inscrito diretamente na versão atual no momento da inscrição.

### Determinar a versão de certificação relevante

Use a API da versão de certificação para identificar qual versão de uma certificação recorrente é relevante para um aluno específico.

Forneça a **ID de certificação raiz** como entrada. A API avalia o histórico de inscrição do aluno e retorna a versão apropriada com base nas seguintes regras:

| **Estado do aluno** | **O que a API retorna** |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| O aluno ainda não está inscrito na certificação | A versão mais recente disponível da certificação |
| O aluno está inscrito no momento | A versão específica na qual o aluno está inscrito no momento, contabilizando todas as recorrências que ocorreram desde a sua inscrição original |

Isso significa que dois alunos que consultam a mesma ID de certificação raiz ao mesmo tempo podem receber resultados diferentes, dependendo do histórico de inscrição individual de cada aluno.

**Observação**: pode haver uma breve janela durante uma recorrência, enquanto a nova versão está sendo criada e as inscrições estão sendo migradas, na qual a API pode retornar a versão que está prestes a ser substituída, em vez da versão recém-criada.

**Exemplo**

Considere uma certificação que se repete mensalmente, onde quatro versões foram criadas ao longo do tempo devido a recorrências sucessivas:

- Um aluno que se inscreveu na primeira versão e progrediu em cada recorrência à medida que ocorreu será retornado para a versão, ele está atualmente ativo em, o que reflete seu próprio histórico de conclusão e recorrência, não necessariamente a versão mais recente que existe.

- Um aluno que ainda não se inscreveu será retornado para a versão criada mais recentemente, pois essa é a versão na qual novas inscrições devem ingressar.

Isso permite que a integração sempre direcione um aluno para a versão de certificação que é relevante para ele, em vez de mostrar cada versão histórica ou adivinhar qual se aplica.

### Referência da API

**Obter a certificação aplicável para uma certificação raiz**

```
GET /primeapi/v2/learningObjects/{loId}/applicableCertification
```

Resolve a versão de certificação que se aplica ao aluno atual, dada a ID de uma certificação raiz. Para alunos inscritos, isso retorna a versão na qual eles estão inscritos no momento. Para alunos não inscritos, isso retorna a versão ativa mais recente.

| **Propriedade** | Valor **1&rbrace;** |
|----------------------------------------------------------|--------------------------|
| **Escopo** | Acesso de leitura do aluno |
| **Limite de taxa (chamadas padrão de aluno)** | 70 solicitações por minuto |
| **Limite de taxa (credenciais de API elevadas ou de nível de administrador)** | 500 solicitações por hora |
| **Formato de resposta** | application/vnd.api+json |

**Observação**: esta API retorna informações de versão para um único aluno por vez. Ela não retorna uma lista de todas as versões de uma certificação.

**Parâmetros de caminho**

| **Parâmetro** | **Obrigatório** | **Tipo** | **Descrição** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| loID | Sim | cadeia de caracteres | A ID do objeto de aprendizado, especificamente, a certificação raiz, para a qual a versão aplicável está sendo solicitada. Isso está sujeito às permissões de acesso padrão. |

**Parâmetros de consulta**

| **Parâmetro** | **Obrigatório** | **Tipo** | **Descrição** |
|---------------|--------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| incluir | Não | cadeia de caracteres | Uma lista separada por vírgulas de modelos relacionados a serem incluídos na resposta junto com a certificação resolvida, como subLOs ou inscrição. Usa a mesma sintaxe de inclusão de outros pontos de extremidade de objeto de aprendizado do Adobe Learning Manager. |

**Exemplo de solicitação**

```
GET /primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

```
curl -X GET --header 'Accept: application/vnd.api+json' \
--header 'Authorization: oauth <access-token>' \
'https://<host>/primeapi/v2/learningObjects/certification%3A167658/applicableCertification?include=subLOs'
```

**Observação**: o valor loId deve ser codificado por URL. Dois-pontos em uma ID de certificação, como certification:167658, está codificado como %3A.

**Exemplo de resposta 200 OK**

A resposta usa a mesma estrutura de uma resposta de Objeto de aprendizado padrão, retornando a certificação resolvida.

**Importante:** o campo de ID na resposta é a ID da certificação **resolvida**, a versão específica aplicável a este aluno. Normalmente, ela será diferente da ID de certificação raiz transmitida como loId, uma vez que o objetivo dessa API é traduzir uma ID raiz para a versão atual correta.

```
{
  "data": {
    "id": "string",
    "type": "string",
    "attributes": {
      "authorNames": [
        "string"
      ],
      "bannerUrl": "string",
      "catalogs": [
        ...
      ]
    }
  }
}
```

**Códigos de resposta**

| **Status** | **Significado** |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 200 | A certificação aplicável foi resolvida com êxito e é retornada em resposta. |
| 400 | A loId fornecida não é uma certificação ou não é uma certificação raiz. Passe a ID da certificação original, não uma versão de recorrência, como o loId. |
| 401 / 403 | A solicitação não tem credenciais de aluno válidas ou as credenciais não têm o acesso necessário. |
| 404 | Nenhuma certificação ativa pôde ser resolvida para esta certificação raiz. Por exemplo, porque cada versão na cadeia foi desativada ou excluída ou porque a certificação não tem nenhuma referência de certificação raiz registrada. Uma 404 também pode ocorrer se uma versão for resolvida com êxito, mas o aluno que está chamando não tiver acesso ao catálogo para ela. |
| 500 | Erro inesperado do servidor ao resolver a certificação. Repita a solicitação. Se o erro persistir, entre em contato com o suporte. |

**Exemplo de resposta de erro**

```
{
  "meta": {
    "error": "string",
    "detail": "string"
  }
}
```

**Observação:** esta API resolve a versão para um aluno por chamada. Ele não retorna uma lista de todas as versões existentes para uma certificação raiz.

**Pontos importantes**

- **Certificações não recorrentes: I** se o loId passado for uma certificação que não está configurada para recorrência, a API retornará a própria certificação.

- **Versões intermediárias ignoradas: se a inscrição ativa de um aluno for movida diretamente de uma versão anterior para uma posterior sem uma inscrição ativa entre, a API ainda será resolvida corretamente para a versão atual do aluno.** A presença de versões intermediárias com as quais o aluno não interagiu ativamente não afeta a resolução.

- **Certificações excluídas versus retiradas:** uma versão de certificação que foi excluída foi totalmente excluída da resolução. Uma certificação desativada ainda pode ser considerada dependendo de seu estado; se você estiver confiando em uma versão específica que permaneça resolvível, confirme seu estado atual em vez de assumir que a desativação sozinha a remove de consideração.

- **A resolução é determinística:** se os dados de inscrição de um aluno estiverem em um estado inconsistente (por exemplo, mais de uma inscrição estiver marcada como atual), a API será resolvida para a versão criada mais recentemente em vez de retornar um resultado imprevisível ou um erro.

**Observação**: um equivalente no escopo do administrador desta API não está disponível no momento e está sendo avaliado para uma versão futura.

### Usar esta API na integração

Um caso de uso comum é uma página ou portal externo que lista certificações que um aluno pode acessar. Em vez de vincular diretamente a uma ID de certificação específica, que pode ficar desatualizada após uma recorrência. Vincule usando a ID de certificação raiz e resolva a versão correta no momento em que o aluno a selecionar.

1.Armazene ou referencie certificações em sua integração usando a **ID de certificação raiz**, a ID da certificação como ela foi criada pela primeira vez, antes de qualquer recorrência.

&#x200B;2. Quando um aluno seleciona uma certificação para exibir ou agir, chame GET /primeapi/v2/learningObjects/{loId}/appliedCertification, transmitindo a ID de certificação raiz como loId.

&#x200B;3. Use a versão de certificação retornada na resposta para direcionar o aluno para o destino correto, seja uma ação de inscrição ou uma exibição de seu progresso atual.

Isso garante que os alunos sempre tenham acesso à versão da certificação que corresponde à sua inscrição real e ao progresso, mesmo que a certificação ocorra novamente com o tempo e gere novas versões.

## Relatório: ID de treinamento raiz na transcrição do aluno

A coluna **ID de treinamento raiz** está disponível por padrão na transcrição do aluno para todas as contas.

| **Tipo de linha** | **Valor de ID de treinamento raiz** |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| Certificação configurada para recorrência | A ID de certificação raiz que esta versão rastreia |
| Certificação não configurada para recorrência | O mesmo valor da ID de treinamento para essa linha |
| Um curso incorporado em uma certificação | A ID da certificação raiz da certificação pai, não a própria ID do curso |
| Um curso ou caminho de aprendizado que não faz parte de nenhuma certificação | O mesmo valor da ID do treinamento ou da ID do curso incorporado para essa linha |

**Observação**: para contas muito grandes com um alto volume de certificações, os valores de ID de treinamento raiz na transcrição do aluno são resolvidos em lotes. Isso não altera a precisão dos dados, mas transcrições muito grandes podem demorar mais para serem geradas.

Essa coluna permite agrupar e relatar o histórico completo de um aluno em todas as versões de uma certificação recorrente, em vez de tratar cada recorrência como um registro independente e não relacionado. Cada recorrência ainda aparece como sua própria linha na transcrição do aluno. A coluna ID do treinamento raiz simplesmente identifica quais linhas pertencem à mesma certificação subjacente.

**Observação:** use a coluna de ID de treinamento raiz quando precisar rastrear o histórico completo de participação de um aluno em uma certificação recorrente.

