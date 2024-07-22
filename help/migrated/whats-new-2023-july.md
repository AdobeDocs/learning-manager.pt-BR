---
title: Novidades desta versão (julho de 2023)
description: Saiba mais sobre os novos recursos e as melhorias no Adobe Learning Manager
hidefromtoc: true
exl-id: c6f192b6-f377-47b2-9151-516ac8179543
source-git-commit: ebf4ea065ba799b957b8ce275fd1690f18b26556
workflow-type: tm+mt
source-wordcount: '2059'
ht-degree: 67%

---

# Novidades desta versão (julho de 2023)

## Recomendações aprimoradas

O Adobe Learning Manager introduziu um sistema de recomendação novo e aprimorado para os cursos. Esse recurso de recomendações usa algoritmos de IA e interesses de usuários, como produtos, funções e níveis, para fornecer recomendações de conteúdo personalizadas.

Para mais informações, consulte [Recomendações no Adobe Learning Manager](recommendations-adobe-learning-manager.md).

## Várias inscrições

Nesta versão do Adobe Learning Manager, estamos introduzindo o recurso de várias inscrições para alunos que permite que eles se inscrevam em mais de uma instância de um curso em um período ou em diferentes períodos de tempo.

Para obter mais informações, consulte [Várias inscrições](/help/migrated/authors/feature-summary/courses.md).

### Várias inscrições em aplicativos móveis ou imersivos

Os alunos não podem se inscrever em várias instâncias a partir de um aplicativo móvel ou imersivo. Não há suporte para várias inscrições no aplicativo móvel e na Web móvel imersiva.

>[!NOTE]
>
>Habilitar o recurso de Várias inscrições resulta na adição de várias linhas ao Relatório de transcrição do aluno para cada curso (uma linha para cada instância).
>
>Se você tiver uma configuração de automação de relatórios que prevê apenas uma linha por curso, deverá fazer os ajustes necessários na automação de relatórios antes de ativar o recurso de Várias Inscrições.

### Formato de medalhas em uma instância com vários inscritos

Para oferecer suporte a medalhas em uma instância com vários registros, o formato da medalha é alterado para `userId_badgeId_COURSE_courseId_courseInstanceId`.

### Iniciar o reprodutor em várias inscrições usando um modo sem periféricos

Nesta versão, alteramos a biblioteca usada para comunicação com o reprodutor sem periféricos.

Em várias inscrições, você deve passar os argumentos quebrados dentro de um objeto.

```
{{startplayer(argument_object) ,
where
argument_object=
{ loId = <loId>, accountId = <accountId>, userId =<userId>, accessToken = <accessToken>, domId = <elementId>, onModuleLoaded = fn(), isMultiEnrolled=<boolean>, instanceId=<instanceId> }
}}
```

## Descontinuação do conector exavault

Esta versão do Adobe Learning Manager incluirá um novo conector, que usará o protocolo SFTP da família AWS Transfer.

Esta alteração também substituirá o conector ExaVault, que não estará mais disponível para novos usuários. Você pode usar qualquer cliente FTP de código aberto como substituto do ExaVault. Para obter mais informações, consulte [Transição do Adobe FTP Manager](transition-from-ftp-manager.md).

## Lembretes no Outlook para sessões de sala de aula e virtuais

As sessões de sala de aula e sala de aula virtual criadas no Adobe Learning Manager que foram adicionadas ao calendário do Outlook do aluno agora suportarão lembretes do Outlook de forma consistente (semelhante aos lembretes de reunião no Outlook).

## Aprimoramentos na atribuição de habilidades a cursos

Fizemos melhorias no fluxo de trabalho de atribuição de habilidades para autores. A lista de sugestões de habilidades na página Configurações do curso agora inclui um recurso de pesquisa com digitação antecipada. Os autores agora podem pesquisar por Habilidades, digitando os primeiros caracteres, e as sugestões serão exibidas na lista suspensa Habilidade com base na entrada. Com esta melhoria, os autores não precisam percorrer a lista completa para localizar e atribuir habilidades aos cursos.

## Melhorias no fluxo de trabalho do curso aprovado pelo gerente

Os cursos aprovados pelo gerente agora fornecem informações de erro apropriadas para gerentes e alunos.

![mensagens de erro](assets/error-messages.png)

Os gerentes agora podem exibir mensagens de erro relevantes com informações (por exemplo, “o prazo final de inscrição já passou”) quando não conseguem aprovar uma solicitação de inscrição no curso. Os alunos recebem a mensagem de erro e a ação corretiva.

## Relatório do novo plano de aprendizado

Os administradores ou administradores personalizados agora podem exportar uma lista de todos os planos de aprendizado na conta e metadados como status, grupos de usuários aplicáveis, informações de acionador, cursos ou planos de aprendizado incluídos no plano de aprendizado e informações de lembrete.

## Relatório para rastrear próximas instâncias desativadas

O Relatório de treinamentos inclui uma coluna adicional para exibir o Prazo de conclusão das instâncias presentes nos cursos ou Planos de aprendizado para que os administradores e autores saibam quais instâncias serão retiradas e possam tomar as medidas necessárias.

## Aprimoramentos para capturar as classificações do curso dos alunos

Uma janela pop-up para capturar a classificação por estrelas de um curso é exibida assim que o usuário conclui o último módulo do curso.

![classificações](assets/ratings.png)

## Personalizar modelos de email

Os modelos de e-mail no Learning Manager agora incluem seções totalmente editáveis, fornecendo uma maior flexibilidade para personalizar as comunicações por e-mail com base nas preferências de mensagens e marcas.

Para obter mais informações, consulte [Personalizar modelo de e-mail](/help/migrated/administrators/feature-summary/email-templates.md#flexibility-in-customizing-the-templates).

## Aprimoramentos no assistente de agendamento

Ajuste o processo de seleção de um professor para sessões virtuais ou em sala de aula. Um filtro Grupo de usuários foi adicionado ao campo Professor no Assistente de agendamento. Os autores agora podem filtrar professores com base em “Habilidades do professor” e qualquer parâmetro adicional, como local, idioma, designação e assim por diante.

Para obter mais informações, consulte o [filtro Grupo de Usuários no Assistente de agendamento](/help/migrated/authors/feature-summary/courses.md#user-group-filter).

## Aprimoramentos no fluxo de trabalho de retirada do objeto de aprendizado

Os autores agora podem fornecer uma data de **Retirada automática** data de um curso. Isso ajuda a evitar a inflação do catálogo com o tempo e a necessidade de voltar e retirar manualmente os cursos.

Os administradores também podem decidir, no nível da conta, a natureza do acesso aos objetos de aprendizado “retirados”.

O Relatório de treinamento inclui uma nova coluna, **Data da retirada automática**, para exibir a data de retirada de cada objeto de aprendizado (se definida).

## Valores de etiqueta de catálogo por autores

Os autores agora podem adicionar seus valores para rótulos de catálogo ao criar ou editar um curso. Os administradores podem habilitar esse recurso no nível da conta. Depois que um autor adiciona um novo valor de rótulo de catálogo, ele se torna parte da pesquisa com digitação antecipada.

![selecionar catálogo](assets/select-catalog.png)

## Aprimoramentos na pesquisa de curso para funções de administrador, autor e gerente

Foram feitas melhorias de pesquisa nas funções de administrador, autor e gerente. Eles agora poderão pesquisar os títulos com palavras-chave. Isso se aplica a cursos, planos de aprendizado e certificações.

## Notificações de falhas de migração

Os administradores de integração são notificados por e-mail se qualquer operação de importação ou exportação falhar durante a migração ou ao usar conectores de dados como PowerBI, FTP, Box etc.

## Configuração de vários gerenciadores por meio de APIs

Uma nova API foi adicionada ao conjunto de APIs do Managed Office para ser compatível com a configuração com vários gerentes.

## Aprimoramentos na API de inscrição

Foram feitas melhorias na API de inscrição para a compatibilidade e otimização de inscrições em massa em grande escala.

## Aplicativo móvel - Exibição de conteúdo offline

Os alunos podem baixar e consumir conteúdo no modo offline. Os Caminhos de Aprendizado aninhados e flexíveis não são compatíveis com a exibição offline.

*Nesta versão, a exibição de conteúdo offline é suportada apenas para conteúdo em inglês.*

## Acessibilidade

Várias melhorias foram implementadas para melhorar a acessibilidade, incluindo melhorias para otimizar a legibilidade pelos leitores de tela.

## Suporte ao aplicativo móvel

Na próxima versão principal, o aplicativo Adobe Learning Manager para dispositivos móveis oferecerá suporte apenas às três versões mais recentes de sistemas operacionais móveis.

## Conteúdo no LinkedIn

O conteúdo do linkedIn não é carregado como esperado no aplicativo Imersivo no navegador Safari. Como solução alternativa, faça o seguinte:

1. No dispositivo, selecione **[!UICONTROL Configurações]** > **[!UICONTROL Safari]**.
1. Desative **Impedir rastreamento entre sites**.
1. Desative **Bloquear todos os cookies**.
1. Faça logon no aplicativo Imersivo.
1. Reproduza o conteúdo.
1. Permita os pop-ups.

## Outras melhorias

### Alternar instâncias no MS Teams

Um aluno pode alternar para uma instância diferente do curso até sua conclusão e manter o andamento do curso.

### Suporte a várias inscrições no MS Teams

Um aluno pode se inscrever em outra instância do curso, independentemente do status de conclusão em qualquer instância anterior. Isso fará com que o aluno se inscreva em várias instâncias do mesmo curso.

### As notas do curso são compatíveis com o recurso de várias inscrições no MS Teams

As notas do curso estão disponíveis no nível da instância do curso para ser compatível com o recurso de várias inscrições.

## Alterações de API

Para obter mais informações sobre as alterações de API, consulte a [Referência de API do Adobe Learning Manager](https://captivateprime.adobe.com/docs/primeapi/v2/).

### Suporte de API para novas recomendações

**GET /conta**

Retorna se prlRecommendation estiver habilitada.

**Solicitação**

`https://learningmanagerstage1.adobe.com/primeapi/v2/account`

**GET /data?filter.recommendationCriteria=product**

Retorna a lista de produtos ou tópicos. Os resultados dependem das configurações da conta que confirmam se todos os produtos estarão visíveis para o aluno ou catálogo visível para produtos ou tópicos.

**Solicitação**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=product&filter.showAllRecommenda`

**`GET /data?filter.recommendationCriteria=role`**

Retorna a lista de Funções recomendadas.

**Solicitação**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=role&filter.showAllRecommendationCriteria=false`

**`GET /data?filter.recommendationCriteria=level`**

Retorna a lista de Funções recomendadas.

**Solicitação**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=level&filter.showAllRecommendationCriteria=false`

**POST /pesquisa/consulta**

A pesquisa também inclui produtos e parâmetros de função na consulta. Não há alterações no corpo e na consulta. Adicionaremos novas opções de classificação

**Solicitação**

`https://learningmanagerstage1.adobe.com/primeapi/v2/search/query?...`

**GET /learningObjects**

O modelo do Objeto de aprendizado retorna recomendações marcadas como autor se a recomendação PRL estiver ativa.

**Solicitar URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects?sort=recommendationScore&filter.recommendationProducts=...&filter.recommendationRoles=...&filter.excludeIgnoredRecommendations=true`

POST /learningObjects/query

Os seguintes atributos são suportados no corpo da chamada de consulta:

```javascript {line-numbers="true"}
{
  "filter.announcedGroups": [
    "string"
  ],
  "filter.bookmarks": true,
  "filter.catalogIds": [
    "string"
  ],
  "filter.cityName": [
    "string"
  ],
  "filter.duration.range": [
    "string"
  ],
  "filter.effectiveModifiedDate.fromDate": "string",
  "filter.effectiveModifiedDate.toDate": "string",
  "filter.excludeIgnoredRecommendations": true,
  "filter.ignoreEnhancedLP": true,
  "filter.ignoreHigherOrderLOEnrollment": true,
  "filter.lang.subLOs": true,
  "filter.lang.twoLetterCode": true,
  "filter.learnerState": [
    "string"
  ],
  "filter.loFormat": [
    "string"
  ],
  "filter.loTypes": [
    "string"
  ],
  "filter.price": "string",
  "filter.priceRange": [
    "string"
  ],
  "filter.recommendationLevels": [
    "string"
  ],
  "filter.skill.level": [
    "string"
  ],
  "filter.skillName": [
    "string"
  ],
  "filter.tagName": [
    "string"
  ],
  "language": [
    "string"
  ],
  "preferredSortPartitionOrder": [
    "string"
  ],
  "showLoContentSource": true,
  "useCache": true,
  "filter.recommendationProducts": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ],
  "filter.recommendationRoles": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ]
}
```

**GET /recommendationProducts**

Recupera o produto PRL por ID de recommendationProduct.

**Solicitar URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationProducts`

GET /recommendationRoles

Recupera o produto PRL por ID de recommendationProduct. Somente as funções visíveis de (Objetos de aprendizado) serão retornadas.

**Solicitar URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/prlRecommendations/roles`

`POST /users/{id}/recommendationPreferences`

Cria ou recria (substitui) as preferências de recomendação PRL. Carga útil de amostra:

```javascript {line-numbers="true"}
{
    "data": {
        "id": "userRecommendationPreferences:14755328",
        "type": "userRecommendationPreferences",
        "attributes": {
            "products": [
                {
                    "id": "recommendationProduct:1",
                    "dateCreated": "2023-05-07T20:00:00.000Z"
                },
                {
                    "id": "recommendationProduct:37",
                    "dateCreated": "2023-05-07T21:00:00.000Z"
                }
            ],
            "roles": [
                {
                    "id": "recommendationRole:23",
                    "dateCreated": "2023-05-07'T'21:00:00.000'Z'"
                },
                {
                    "id": "recommendationRole:1",
                    "dateCreated": "2023-05-07'T'20:01:00.000'Z'"
                },
                {
                    "id": "recommendationRole:2",
                    "dateCreated": "2023-05-07'T'19:02:00.000'Z'"
                },
                 {
                    "id": "recommendationRole:3",
                    "dateCreated": "2023-05-07'T'18:02:00.000'Z'"
                },
                {
                    "id": "recommendationRole:20",
                    "dateCreated": "2023-05-07'T'17:02:00.000'Z'",
                    "levels": [
                        "INTERMEDIATE"
                    ]
                }
            ]
        }
    }
}
```

**`GET /users/{id}/recommendationPreferences`**

**Solicitar URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2//users/123/recommendationPreferences`

**`DELETE /users/{id}/recommendationPreferences`**

Exclui as preferências de usuário de recomendação PRL para um produto ou função.

**Solicitar URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/users/123/recommendationPreferences?ids=recommendationRole:123,recommendationRole:234`

Parâmetros:

Ids = lista de ids a serem excluídas

**PATCH /users/{id}/recommendationPreferences**

Adição ou atualização parcial. Carga útil de amostra:

```javascript {line-numbers="true"}
{
  "data": {
    "id": "userRecommendationPreferences:<USER_ID>",
    "type": "userRecommendationPreferences",
    "attributes": {
      "roles": [
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "INTERMEDIATE"
            ]
          }
        },
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "ADVANCED"
            ]
          }
        }
      ]
    }
  }
}
```

**POST /recommendationPreferences/learningObjects/{id}/ignore**

Adicione o OA às recomendações bloqueadas.

**Solicitar URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`DELETE /recommendationPreferences/learningObjects/{id}/ignore`**

Exclui o OA das recomendações bloqueadas.

**Solicitar URL**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`GET /users/{id}/recommendationStrips`**

Recupera todas as faixas a serem usadas para mostrar recomendações PRL

### Suporte a várias inscrições para API

**GET /primeapi/v2/account**

Dois novos atributos são adicionados:

* instanceSwitchEnabled
* multiEnrollmentEnabled

**GET /users/{userId}/userNotifications**

Adicionada a ID da instância do curso nas notificações no novo atributo de metadados.

**GET /learningObjects**

O relacionamento de inscrição exibe apenas a inscrição principal, ou seja, inscrita primeiro ou concluída primeiro.

**`GET /learningObjects/{id}`**

O relacionamento de inscrição exibe apenas a inscrição principal, ou seja, inscrita primeiro ou concluída primeiro.

**`GET /learningObjects/{loId}/instances/{loInstanceId}`**

Um novo relacionamento é adicionado ao modelo de instância do OA.

**`GET /enrollments/{id}`**

Recupere a inscrição de cursos com várias inscrições.

**`DELETE /enrollments/{id}`**

Cancela a inscrição em uma instância específica do objeto de aprendizado.

**POST /inscrições**

É compatível com inscrições em instâncias diferentes.

**GET/inscrições**

Obtém inscrições somente para inscrições primárias do Objeto de aprendizado.

**`GET /learningObjects/{id}/note`**

Recupera uma lista de notas de um curso.

**`GET /learningObjects/{lo_id}/instances/{loi_id}/note`**

Recupera uma lista de notas de um curso e a instância.

**`GET /learningObjects/{id}/resources/{loResourceId}/note`**

Recupera uma lista de notas de um recurso em um curso.

**`POST /learningObjects/{id}/resources/{loResourceId}/note`**

Adiciona uma nota em um módulo de um curso para um curso específico.

**`DELETE /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Exclui observações específicas de um determinado módulo em relação a uma instância específica (parte de loResourceId).

**`GET /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Recupera uma observação específica em um módulo em um curso para uma determinada instância (parte de loResourceId).

**`PATCH /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Atualiza observações específicas de um determinado módulo em relação a uma instância específica (parte de loResourceId).

**Alterações na API do administrador**

* GET /users/{id}/enrollments
* POST /users/{id}/enrollments
* DELETE /users/{id}/enrollments/{enrollmentId}
* PATCH /users/{id}/enrollments/{enrollmentId}

### Campos aplicados para pontos de extremidade

Os produtos e as funções são carregados somente quando aplicados.

Solicitação de exemplo

* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course%3A7418798?enforcedFields[learningObject]=products`
* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/users/11255638/userBadges?include=model&page[offset]=0&page[limit]=10&sort=dateAchieved&enforcedFields[learningObject]=products,roles`

### Implementação da base de alterações da API de pesquisa (localidade inglesa)

O truncamento é o processo de reduzir uma palavra à sua forma raiz. Isso garante que as variantes de uma palavra correspondam durante uma pesquisa. Por exemplo, andar e andar podem ter a mesma raiz: caminhar. Uma vez feita a raiz, uma ocorrência de uma palavra corresponderia à outra em uma pesquisa.

Nesta versão, adicionamos a raiz para localidades em inglês, que inclui as seguintes variantes: en_US, en_AU, en_GB.

O atributo “stemmed” menciona se o stemming é necessário nos resultados da pesquisa. Por padrão, esta opção está definida como False.

Parâmetros de Consulta de API:

* matchType=phrase_and_match
* stemmed=true

### Remoção de pontos finais V1

As APIs V1 deixarão de funcionar nesta versão. Para obter mais informações, consulte o [Manual do desenvolvedor](/help/migrated/integration-admin/feature-summary/developer-manual.md).

### Notificações de inscrição ou cancelamento de inscrição no curso

Esta versão apresenta compatibilidade com a ID da instância do curso com notificações no novo atributo de metadados.

### Suporte a feedback L1

Permite que o aluno forneça feedback em cada nível de instância do recurso de Várias inscrições.

**API:** `POST /enrollments/{id}/l1Feedback`

### Lista de campos obrigatórios do LO

Nesta versão, você deve enviar seções, prequisiteConstraints, prerequisiteLOs, subLOs, additionalResources, additionalLOs, instâncias, catalogLabels para o learningObject explicitamente.

Por exemplo,

`enforcedFields[learningObject]=prerequisiteLOs,instances`

### Aviso de descontinuação para a próxima versão

* Sinalizador de substituição para APIs do aluno.
* Vamos alterar o padrão para highlightResults=false. Além disso, alteraremos o padrão de snippetType=courseName.
* Descontinuaremos matchType=bool no ponto de extremidade de pesquisa.
* autoCompleteMode tem a marca [Deprecated] e para fornecer a mesma funcionalidade de autoCompleteMode =false, temos um matchType adicionado chamado Match.

### Formato de ID de medalha com várias inscrições

Para oferecer suporte a medalhas de instância com várias inscrições, estamos alterando o formato das medalhas do curso de `userId_badgeId_COURSE_courseId to userId_badgeId_COURSE_courseId_courseInstanceId` para identificar exclusivamente medalhas.

## Notas de versão

Para obter informações sobre as versões atuais e anteriores do aplicativo Web e do aplicativo de dispositivo do Learning Manager, consulte as [Notas da versão](/help/migrated/release-note/release-notes.md).

## Problemas conhecidos ou limitações nesta versão

Estas são as limitações desta versão:

### Exibir conteúdo offline no aplicativo para dispositivos móveis

Os itens a seguir não são compatíveis ao exibir conteúdo offline no aplicativo:

* Cursos, Planos de Aprendizado ou Certificações flexíveis.
* Cursos aprimorados, planos de aprendizado ou certificações.
* Cursos habilitados para vários quizzes, Planos de Aprendizado ou Certificações.
* Harvard Manage Mentor, Marketplace de Conteúdo, GetAbstract ou Cursos, Planos de Aprendizado ou Certificações do LinkedIn.
* Planos de Aprendizado e Certificados com pré-requisitos ativados.
* Cursos, Planos de Aprendizado ou Certificações desativados.
* Cursos, planos de aprendizado ou certificações com prazo expirado.
* Certificados Externos.
* Cursos, planos de aprendizado ou certificações habilitados para eCommerce.

Os seguintes Caminhos de Aprendizado, Cursos ou Certificações têm alguns problemas com a sincronização offline:

* Todos os Caminhos de Aprendizado.
* Todos os certificados internos.
* Conteúdo com chamadas de POST.

### Recomendações

Os itens a seguir não têm suporte para Produto/Função/Nível no novo sistema de recomendação:

* Adobe Experience Manager, Teams, SFDC e Não Conectado.
* O aplicativo para dispositivos móveis não oferece suporte à edição de produtos e funções na página de recomendação.
* O mapeamento não é possível durante a migração.
* Marcação automática de LinkedIn, Marketplace de conteúdo e outros cursos externos, planos de aprendizado ou certificações.
* Revertendo para Baseado em habilidade ou Clássico depois de colocar no ar.
* O menu de pesquisa de Produtos e Funções no aplicativo do aluno.
* Mapeamento em massa de cursos, planos de aprendizado ou certificações e usuários no aplicativo do administrador.

## Requisitos do sistema

[Requisitos de sistema do Learning Manager](/help/migrated/system-requirements.md)
