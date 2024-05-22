---
jcr-language: en_us
title: Descontinuações de API no Adobe Learning Manager
description: À medida que as APIs no Adobe Learning Manager evoluem, elas são periodicamente reorganizadas ou atualizadas. Quando as APIs evoluem, a API antiga é descontinuada e eventualmente removida. Esta página contém informações que você precisa saber ao migrar de versões de API obsoletas para versões de API mais novas e estáveis.
contentowner: saghosh
exl-id: 0fe9a3cb-9114-42d6-81ae-1a4f28c984fa
source-git-commit: 670d0477b246af2a0257e41eca799817e391b348
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 32%

---

# Descontinuações e alterações de API no Adobe Learning Manager

## Descontinuações de API na versão de março de 2024 do Adobe Learning Manager

<!-- ### Changes in Rate Limits

With the next release of Adobe Learning Manager, we're restructuring API rate limits for new accounts. For existing accounts, only the Admin APIs will be rate-limited. After 90 days (about 3 months), we will restructure rate limits for all APIs, but existing accounts will be whitelisted according to current usage. Existing accounts need to revisit their learner API usage. 

For new accounts, if they want to increase the rate limits, they must contact the Customer Success team of ALM. 

#### Which APIs will be rate limited 

For new accounts, all Admin, Learner, and Search APIs will have rate limits and burst enforced.  

The API burst rate or burst limit refers to the maximum number of requests allowed to be made to an API in a short burst within a limited timeframe. 

The following table lists the rate and burst limits for the APIs.

<table>
    <tr>
        <th>API</th>
        <th>Number of requests-RPM</th>
        <th>Number of requests-Burst</th>
    </tr>
    <tr>
        <td>Admin</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Learner</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Search</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>
-->

### Alterações nos limites de deslocamento

Devido ao alto número de registros recuperados pelo valor de deslocamento e à redução do desempenho geral, estamos aplicando um limite de **500** registros. Na próxima versão, para Administrador e Aluno, o **Usuários do GET** A API retornará um máximo de **500** registros.

Se precisar buscar mais registros, use o **GET** API.

<!--### Exclude paths 

At present, Learning Manager APIs follow a graph data structure, which allows you to fetch data by traversing the API model through includes. Even though you could traverse an API up to seven levels, fetching the data using a single API call is computationally expensive. 

We recommend that all existing and new customers make small calls multiple times instead of one large call. This approach will prevent unwanted data from being loaded in the call. 

We want to enforce these restrictions on new accounts and maintain a whitelist of existing accounts.-->

#### Quais caminhos estão obsoletos

Os caminhos a seguir estão obsoletos:

* /learningObjects
   * Caminhos obsoletos:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Novos caminhos:
      * enrollment.loInstance.loResources
      * instances.loResources

* /learningObjects/{id}
   * Caminho preterido:
      * enrollment.instances.subLoInstances.learningObject
   * Novo caminho:
      * enrollment.instances.subLoInstances

* /enrollments
   * Caminho preterido:
      * loInstance.learningObject.enrollment
   * Novo caminho:
      * loInstance.learningObject

* /learningObjects/{id}
   * Caminho preterido:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Novo caminho:
      * instance.subLoInstances

<!--### Instance summary count changes 

Currently, in the LO summary endpoint, you fetch the number of all possible instances. For example, for a course, you can view the number of enrollments and waitlists in the response for **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. You can then view the completionCount and enrollmentCount in the response. If the course is a VC or classroom, you can also view its seat limit and waitlist limit. 

The process of retrieving the completion and enrollment counts is computationally expensive, therefore the calculation is done on a request basis. If the data is not present in the cache, the data is reloaded, which is computationally intensive. If there are many users enrolling in a course, the counts will be large, and effectively impacts CPU performance. 

In the next release of Adobe Learning Manager, in the LO Instance summary endpoint, the completionCount, enrollmentCount, seatLimit, and waitlistCount are cached. The cached information persists till there are changes in enrollments or unenrollments. For counts exceeding 1000 enrollments, we'll assume the estimated counts, and invalidate the results for all existing and new accounts.

>[!NOTE]
>
>For counts, such as, completionCount, enrollmentCount, seatLimit, and waitlistCount exceeding1000, it's advisable to interpret them as estimates rather than precise figures, as these will be retrieved from cache.-->

### Classificar por nome

Na próxima versão do Adobe Learning Manager, name e -name são descontinuados no campo de classificação das seguintes APIs:

* GET /userGroups/{userGroupId}/users
* GET /users

>[!NOTE]
>
>Para todas as contas novas e existentes, a classificação por nome e -name será descontinuada.


## Descontinuações de API na versão de novembro de 2023 do Adobe Learning Manager

### Sinalizador de substituição

Na versão de novembro de 2023 do Adobe Learning Manager, descontinuamos o sinalizador de substituição das APIs. O sinalizador de substituição não faz parte da especificação da API pública e destina-se a testes de back-end. O sinalizador foi descontinuado para APIs do aluno. No entanto, o sinalizador ainda é válido para APIs de administrador.

O motivo pelo qual estamos descontinuando o sinalizador para as APIs do aluno é porque o sinalizador de substituição estava buscando uma grande quantidade de dados por meio das APIs do aluno.

No futuro, a seguinte API do aluno deixará de funcionar porque tem o sinalizador de substituição.

_/primeapi/v2/users?page[offset]=0&amp;página[limite]=10&amp;sort=id&amp;override=TRUE_

### Alterações de API para novas recomendações baseadas em habilidade

O Adobe Learning Manager aprimora as recomendações para contas habilitadas para clientes e parceiros. Essa melhoria no algoritmo de recomendação com a alteração no algoritmo de classificação para curso, caminho de aprendizado e certificação fornece uma melhor experiência do usuário na detecção de conteúdo.

O algoritmo não permitirá mais recomendações baseadas em pares. A alteração não afetará os usuários existentes, mas a opção Alinhado ao setor continuará existindo. Para a opção Personalizada, o Adobe Learning Manager não permitirá mais a seleção personalizada baseada em pares.

O grupo de colegas agora se torna uma conta e os alunos verão uma sequência de caracteres que mostra os tópicos em tendência no grupo. Todas as recomendações são explicáveis. Por exemplo, se você estiver visualizando algo em um assunto, o cartão na faixa exibirá o motivo do curso.

### Alterações No Relatório De Anúncio De Notificações

Em versões anteriores do Adobe Learning Manager, o relatório de Aviso de Notificação não tinha nenhum filtro. O Adobe Learning Manager baixou todas as notificações na conta.

Na versão de novembro de 2023, adicionamos um filtro de data, com o qual você pode baixar as notificações dentro de um período especificado.  No entanto, você só pode baixar o relatório nos últimos seis meses.

### Descontinuação de valores altos de deslocamento no ponto de extremidade GET /users

Para melhorar o desempenho do sistema e gerenciar a utilização de recursos de maneira mais eficiente, a Adobe reduziu os valores altos de deslocamento no endpoint GET /users para ambos **ADMIN** e **ALUNO** escopos. Recomendamos o uso da **API de trabalhos** para recuperar os registros com um valor de deslocamento.

