---
description: Pontos de extremidade de API públicos e voltados para o aluno para listagem, recuperação, inscrição e exclusão de Caminhos de aprendizado personalizados no Adobe Learning Manager e pontos de extremidade de API para verificar se um ou mais objetos de aprendizado estão diretamente acessíveis a um determinado aluno por meio de um catálogo atribuído a ele.
jcr-language: en_us
title: Alterações na API em setembro de 2026
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1374'
ht-degree: 3%
---

# Alterações na API na versão de setembro de 2026 do Adobe Learning Manager

## API para verificar o acesso ao catálogo dos objetos de aprendizado

Determine se o aluno atual tem acesso direto ao catálogo de um ou mais objetos de aprendizado, independentemente de o aluno ter alcançado esse conteúdo por meio de um caminho de aprendizado ou certificação.

### Finalidade da API

Quando um aluno abre um caminho de aprendizado ou uma certificação, ele pode navegar nos cursos individuais dentro dele, mesmo se um curso específico não for atribuído diretamente a ele por meio de um catálogo. Isso suporta a descoberta de conteúdo: os alunos podem explorar o que um caminho de aprendizado contém antes de decidir se o perseguirão.

No entanto, poder ver um curso dessa maneira não deve significar automaticamente que o aluno possa se inscrever nele. A inscrição deve depender de o aluno ter acesso direto ao catálogo desse curso específico, não apenas acesso indireto por meio de um caminho de aprendizado contendo.

Essa API permite verificar, para um determinado aluno, se um ou mais objetos de aprendizado podem ser acessados diretamente por meio de um catálogo atribuído a ele. Use o resultado para controlar a interface de usuário relacionada à inscrição, por exemplo, mostrando uma opção de Inscrição somente quando o acesso direto ao catálogo for confirmado, mantendo a própria página do curso visível em ambos os casos.

### Ponto de extremidade

`GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs`

| Propriedade | Valor |
|---|---|
| **Escopo** | Acesso de leitura do aluno |
| **Formato de resposta** | application/vnd.api+json |

### Parâmetros de consulta

| Parâmetro | Obrigatório | Tipo | Descrição |
|---|---|---|---|
| ids | Sim | sequência de caracteres ou matriz | Uma ou mais IDs de objetos de aprendizado a serem verificadas. Aceita uma única ID ou uma lista separada por vírgulas. Máximo de 10 IDs por solicitação. |

### Solicitação de exemplo

```
GET /primeapi/v2/learningObjects/isMemberOfVisibleCatalogs?ids=course%3A2400159%2Ccourse%3A2400160%2Ccourse%3A2400161%2Ccourse%3A2400162
Accept: application/vnd.api+json
Authorization: oauth <access-token>
```

>[!NOTE]
>
>As IDs do objeto de aprendizado devem ser codificadas por URL. Os dois pontos em uma ID, como course:2400159, estão codificados como %3A, e a vírgula separando várias IDs está codificada como %2C.

### Exemplo de resposta - 200 OK

```json
{
  "course:2400162": false,
  "course:2400161": false,
  "course:2400160": true,
  "course:2400159": true
}
```

| Valor | Significado |
|---|---|
| verdadeiro | O aluno que está chamando tem acesso direto ao catálogo para esse objeto de aprendizado. |
| falso | O objeto de aprendizado não está diretamente disponível para o aluno que está chamando por meio de um catálogo. O aluno ainda poderá visualizá-la se estiver acessível por meio de um caminho de aprendizado ou certificação à qual tenha acesso. |

### Códigos de resposta

| Status | Significado |
|---|---|
| 200 | A solicitação foi bem-sucedida. A resposta contém um resultado para cada ID solicitada. |
| 400 | Um erro genérico de solicitação incorreta. Por exemplo, mais de 10 IDs foram fornecidas ou uma ID estava malformada. |
| 401 | A solicitação não tem credenciais de aluno válidas ou o acesso foi negado devido a credenciais inválidas. |

### Exemplo de resposta de erro

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "Either LO id is blank or not as per public api specification"
  }
}
```

### Usar esta API na integração

Um caso de uso comum é uma página do curso que um aluno acessa navegando de um caminho de aprendizado. Você deseja que a própria página do curso permaneça acessível para descoberta, ao mesmo tempo em que mostra a ação de **Inscrição** somente se o aluno tiver acesso direto ao catálogo desse curso.

1. Quando a página do curso carregar, chame este ponto de extremidade com a ID do objeto de aprendizado do curso.
2. Se a resposta retornar true para essa ID, mostre a opção **Inscrever**.
3. Se a resposta retornar falso, mantenha a página do curso visível, o título, a descrição e os detalhes do curso, mas oculte a opção **Inscrever-se**.

## API de trabalho para relatório de registro de auditoria do administrador {#apiaudittrailreport}

### Finalidade da API

O Relatório de registro de auditoria do administrador lista as alterações de configuração feitas em um
Conta da Adobe Learning Manager. Por exemplo, alterações em Noções básicas, Integrações ou
Configurações avançadas da conta em um determinado intervalo de datas. A geração do relatório de Trilha de Auditoria requer a consulta e a agregação de registros de alteração de configuração no intervalo de datas solicitado e nos tipos de configuração. Dependendo do tamanho do intervalo e do volume de alterações, isso pode exceder os limites de tempo de uma solicitação HTTP síncrona, o que coloca em risco os timeouts do cliente ou gateway.

Para evitar isso, o relatório é gerado de forma assíncrona por meio da API de Trabalho genérica:

1. **Criar um trabalho.** O administrador envia uma solicitação especificando o tipo de relatório, o intervalo de datas e os tipos de configuração. A API retorna uma ID de trabalho imediatamente, sem esperar que o relatório seja compilado.

2. **Sondar o trabalho.** O administrador recupera periodicamente o trabalho por sua ID para verificar seu status. Quando o trabalho é concluído, a resposta contém o resultado ou uma referência a ele.

### URL base e convenções

| Item | Valor |
|---|---|
| Caminho base | `/primeapi/v2` |
| Tipo de conteúdo | `application/vnd.api+json;charset=UTF-8` (JSON:API) |
| Autenticação | Token OAuth do portador, com escopo para um administrador de conta |
| Contexto da conta | Cabeçalho `x-acap-account` identificando a conta do administrador de chamada |
| Sondagem | Nenhum intervalo fixo está imposto; sonde o ponto de extremidade de Obter Status do Trabalho até `status` não for mais `QUEUED` ou `IN_PROGRESS` |

### IDs

O trabalho `id` retornado quando um trabalho é criado é uma cadeia de caracteres opaca (por exemplo,
`4593`). Sempre passar para trás o valor exato de `id` recebido da criação
resposta ao pesquisar status. Nunca o construa ou analise.

### Escopos de autenticação

Cada ponto de extremidade requer um token OAuth com o seguinte escopo e a
o usuário chamador deve ter a função de administrador de conta:

- `admin:write` cria um trabalho de relatório (`ROLE_ADMIN` necessários)
- `admin:read` leu o status e o resultado de um trabalho (`ROLE_ADMIN` necessários)

As solicitações feitas por um chamador que não mantém `ROLE_ADMIN` na conta são
rejeitado; consulte [Manipulação de erros](/help/migrated/api-changes-sep-2026.md#error-handling)

### Pontos finais

#### Criar um trabalho de Relatório de registro de auditoria

`POST /primeapi/v2/jobs`

Cria um trabalho assíncrono que gera um relatório de Registro de Auditoria de Alteração de Configuração
para o intervalo de datas e tipos de configuração especificados. A resposta retorna imediatamente
com um recurso de trabalho no estado `QUEUED`; o próprio relatório é produzido no estado
fundo.

Escopo: `admin:write`

| Parâmetro | Em | Obrigatório | Descrição |
|---|---|---|---|
| `jobType` | body | Sim | Deve ser `generateConfigChangeAuditReport` para este relatório |
| `payload.fromDate` | body | Sim | Início da janela de relatório, ISO-8601 com deslocamento, por exemplo `2026-09-15T00:00:00.000+05:30` |
| `payload.toDate` | body | Sim | Fim da janela de relatório, ISO-8601 com deslocamento, por exemplo `2026-09-23T23:59:59.000+05:30` |
| `payload.settingTypes` | body | Sim | Matriz de uma ou mais categorias de configuração a serem incluídas; os valores com suporte são `Basics`, `Integrations` e `Advanced` |

Amostra do corpo da solicitação

```json
{
  "data": {
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "payload": {
        "fromDate": "2026-09-15T00:00:00.000+05:30",
        "toDate": "2026-09-23T23:59:59.000+05:30",
        "settingTypes": ["Basics", "Integrations", "Advanced"]
      }
    }
  }
}
```

Resposta: `202 Created`. O corpo da resposta é o recurso de trabalho em sua
Estado `QUEUED`.

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "QUEUED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

>[!NOTE]
>
>Uma janela `fromDate`/`toDate` que abrange um intervalo de datas muito grande ou que
>solicita todos os tipos de configuração para uma conta com um longo histórico de alterações, pode
>demora mais para processar. Sondar o ponto de extremidade Obter Status do Trabalho em vez de
>presumindo que o relatório está pronto após um atraso fixo.

#### Obter o status de um trabalho de Relatório de registro de auditoria

`GET /primeapi/v2/jobs/{id}`

Retorna o status atual de um job criado anteriormente. Enquanto o trabalho for
ainda em execução, `attributes.status` é `QUEUED` ou `IN_PROGRESS` e
`attributes.result` está ausente. Quando o trabalho for concluído, `attributes.status` é
`COMPLETED`, com o local do relatório em `attributes.result`, ou
`FAILED`, com detalhes da falha em `attributes.error`.

Escopo: `admin:read`

| Parâmetro | Em | Obrigatório | Descrição |
|---|---|---|---|
| `id` | caminho | Sim | ID do trabalho retornada quando o trabalho foi criado |

Exemplo de resposta enquanto o job ainda está em execução

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "IN_PROGRESS",
      "dateCreated": "2026-09-23T18:12:04.000+05:30"
    }
  }
}
```

Exemplo de resposta depois que o trabalho for concluído

```json
{
  "data": {
    "id": "4593",
    "type": "job",
    "attributes": {
      "jobType": "generateConfigChangeAuditReport",
      "status": "COMPLETED",
      "dateCreated": "2026-09-23T18:12:04.000+05:30",
      "dateCompleted": "2026-09-23T18:12:41.000+05:30",
      "result": {
        "downloadUrl": "https://learningmanager.adobe.com/primeapi/v2/jobs/4593/download",
        "expiresAt": "2026-09-24T18:12:41.000+05:30"
      }
    }
  }
}
```

### Esquema de recurso

#### Atributos do trabalho

| Campo | Tipo | Descrição |
|---|---|---|
| `id` | cadeia de caracteres | ID de trabalho opaco |
| `jobType` | cadeia de caracteres | `generateConfigChangeAuditReport` para este relatório |
| `status` | cadeia de caracteres | `QUEUED`, `IN_PROGRESS`, `COMPLETED` ou `FAILED` |
| `dateCreated` | string (ISO-8601) | Quando o trabalho foi criado |
| `dateCompleted` | string (ISO-8601) | Quando o trabalho for concluído; presente quando `status` for `COMPLETED` ou `FAILED` |
| `payload` | objeto | Os parâmetros de solicitação com os quais o trabalho foi criado (incorporado - veja abaixo) |
| `result` | objeto | Onde baixar o relatório concluído; presente somente quando `status` for `COMPLETED` (inserido - veja abaixo) |
| `error` | objeto | Detalhes da falha; presente somente quando `status` é `FAILED` |

#### Carga (incorporada, dentro da solicitação de criação)

| Campo | Descrição |
|---|---|
| `fromDate` | Início da janela de geração de relatórios |
| `toDate` | Fim da janela de relatório |
| `settingTypes` | Definindo categorias incluídas no relatório: `Basics`, `Integrations`, `Advanced` |

#### Resultado (incorporado, dentro de um trabalho concluído)

| Campo | Descrição |
|---|---|
| `downloadUrl` | URL assinada da qual o relatório gerado pode ser baixado |
| `expiresAt` | Quando `downloadUrl` deixa de ser válido; solicite uma nova verificação de status para obter um novo link depois desse período |

### Manipulação de erros {#audit-trail-report-error-handling}

Os códigos a seguir se aplicam a esses parâmetros:

| Status do HTTP | Código de erro | Quando ocorre |
|---|---|---|
| 400 | `BAD_REQUEST` | `toDate` é anterior a `fromDate`, `settingTypes` está vazio ou contém um valor sem suporte ou uma data não é válida ISO-8601 - criar somente ponto de extremidade |
| 401 | `UNAUTHORIZED_ACCESS` | O token está ausente, inválido ou expirado |
| 403 | `FORBIDDEN` | O chamador não mantém `ROLE_ADMIN` na conta |
| 400 | `OBJECT_DOESNT_EXIST` | Obter por ID: o trabalho não existe ou a ID está malformada - ambos os casos são recolhidos nesta mesma resposta |

Exemplo de resposta de erro

```json
{
  "status": "BAD_REQUEST",
  "title": "Bad request. Check url, params and headers",
  "source": {
    "info": "toDate must be on or after fromDate"
  }
}
```

### Usar esta API na integração

Um caso de uso comum é uma ação “Baixar trilha de auditoria” voltada para o administrador na
tela configurações da conta.

1. Quando o administrador seleciona um intervalo de datas e um ou mais tipos de configuração e
confirma, chame o ponto final create-job com esses valores.
2. Armazene o trabalho retornado `id` e sonde o ponto de extremidade Obter Status do Trabalho em um
razoável (por exemplo, a cada poucos segundos).
3. Enquanto `status` for `QUEUED` ou `IN_PROGRESS`, continue mostrando um estado de progresso
na interface.
4. Quando `status` se tornar `COMPLETED`, use `result.downloadUrl` para permitir que o
o administrador baixou o relatório antes de `expiresAt` passar.
5. Quando `status` se tornar `FAILED`, surgir como `error` para o administrador e deixá-lo
tente novamente.
