---
description: Alterações de API no ALM
jcr-language: en_us
title: Alterações na API na versão de correção de maio de 2026
source-git-commit: 24f54599749bce60916a57634144b0ca7f6a6d10
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Alterações na API na versão de correção de maio de 2026

## Aprimoramento da API GET /learningObjects

A API GET /learningObjects agora inclui um novo atributo startDate no recurso learningObjectInstance quando o relacionamento de instâncias é incluído.

**Ponto de Extremidade**
GET /learningObjects/{id}?include=instâncias

**Alterar**
Um novo campo, startDate, foi adicionado em:
incluído[].attributes.startDate

**Descrição**
startDate representa a data e a hora de início programadas de uma instância do objeto de aprendizado.

**Exemplo**
https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course:13209797?include=instâncias
Resposta de amostra (truncada)

```
{
  "id": "course:13209797_16226533",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2026-05-20T04:35:46.000Z",
    "isAET": false,
    "isDefault": true,
    "isFlexible": false,
    "startDate": "2026-10-06T18:29:59.000Z",
    "state": "Active",
    "timeZoneCode": "IST"
  }
}
```

**Notas**

* O campo é retornado somente para instâncias aplicáveis do objeto de aprendizado.
* O valor é retornado no formato de data e hora UTC ISO 8601.
* As integrações existentes permanecem compatíveis com versões anteriores.
