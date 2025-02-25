---
description: Saiba mais sobre os novos recursos e aprimoramentos na versão de novembro de 2024 do Adobe Learning Manager
jcr-language: en_us
title: Resumo dos novos recursos
exl-id: 4dfe0e31-d202-4a6e-8c4f-43851218699f
source-git-commit: 537d324d6e266552fdfdd9ba16557fd3228870b7
workflow-type: tm+mt
source-wordcount: '3260'
ht-degree: 2%

---

# Resumo dos novos recursos {#new-features-summary}

Saiba mais sobre os novos recursos e aprimoramentos na versão de novembro de 2024 do Adobe Learning Manager.

* **Pesquisa baseada em IA:** combina a pesquisa lexical e semântica para obter resultados mais inteligentes e sensíveis ao contexto.
* **Webhooks**: integre com Webhooks para enviar informações em tempo real para URLs específicas.
* **LTI (Interoperabilidade das Ferramentas de Aprendizagem)**: oferece suporte à LTI para interoperabilidade com outras plataformas LMS.
* **Integração de créditos**: gerenciar e compartilhar medalhas externas por meio da Credly.
* **Aprimoramentos no painel de conformidade**: compartilhe painéis com outros administradores e defina widgets de conformidade padrão nas páginas iniciais do aluno.
* **Suporte a vários idiomas**: crie instâncias específicas de idioma para os módulos Sala de aula e Sala de aula virtual.
* **Funções personalizadas**: controle aprimorado sobre funções e permissões de usuário.
* **Comentários de conclusão**: adicione comentários ao marcar alunos como concluídos.
* **Relatório de grupo de usuários**: gerenciar grupos de usuários com relatórios detalhados.
* **Relatório da lista de espera**: baixe a lista de alunos na lista de espera para instâncias do curso.
* **Aprimoramentos de acessibilidade**: suporte para texto alternativo em manchetes e logotipos de empresas.
* **Suporte para hindi**: suporte de idioma de interface para hindi.
* **Verificação de profanação**: bloquear postagens de redes sociais contendo palavras proibidas.
* **Otimização do modelo de email**: modelos de email combinados e otimizados para atribuições de professor e cancelamentos de sessão.
* **Critérios de conclusão do MS Teams**: defina o tempo mínimo de participação para sessões VILT.
* **Novos fluxos de trabalho de migração**: as alterações de migração incluem critérios de conclusão para cursos e módulos e migração de módulos para pastas.

>[!NOTE]
>
>Confira este [webinar](https://cdn.content.adobelearningmanageracademy.com/public/newlearner/newlearner_0dc0f1e8.html#/overviewPage?instanceId=11932477&amp;loId=11231360&amp;loType=course) para saber mais sobre os novos recursos nesta versão.

## Pesquisa viabilizada por IA no Adobe Learning Manager

O Adobe Learning Manager está aprimorando a forma como os alunos pesquisam cursos ou treinamento. Ele introduz um recurso de pesquisa viabilizado por IA que combina pesquisa lexical e semântica. A busca agora é mais inteligente, pois busca termos específicos e entende o contexto e a intenção por trás deles. A pesquisa avançada entende o significado da consulta e fornece resultados relevantes. Ele identifica o foco principal da pesquisa para fornecer o conjunto mais completo de resultados.

>[!NOTE]
>
>A pesquisa viabilizada por IA só está disponível para os alunos.

Consulte este artigo [Pesquisa Avançada](/help/migrated/learners/feature-summary/advanced-search.md) para obter mais informações.

## Webhooks

O Adobe Learning Manager permite a integração com Webhooks para enviar informações em tempo real, como inscrições no curso, criação do curso e outras informações, para um URL específico.

Um webhook no ALM permite que uma entidade envie dados automaticamente para outro aplicativo por HTTP. Isso permitirá que um aplicativo forneça informações a outros aplicativos sem solicitar constantemente. Por exemplo, se um usuário concluir um curso de sistema de gerenciamento de aprendizagem (LMS), um webhook poderá enviar automaticamente essas informações para outra plataforma, como um CRM ou uma ferramenta de relatório. Os webhooks são frequentemente usados em integrações para automatizar processos e reduzir a necessidade de atualizações manuais entre sistemas. Configure webhooks fornecendo um URL de retorno de chamada para o qual você enviaria os dados.

Consulte este artigo [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md) para obter mais informações.

## Interoperabilidade do Learning Tools

O Adobe Learning Manager agora oferece suporte à LTI para aprimorar a interoperabilidade entre o Adobe Learning Manager e outros sistemas de gerenciamento de aprendizagem (LMS).

### O que é LTI?

A LTI (Interoperabilidade das ferramentas de aprendizado) é um padrão que permite que ferramentas e provedores de conteúdo de terceiros se conectem com um Sistema de Gerenciamento de Aprendizado (LMS). Os usuários podem acessar conteúdo de aprendizado externo de provedores de conteúdo externo diretamente em seu LMS sem fazer logon ou navegar para um LMS diferente.

**LTI como provedor de ferramentas**: o LTI como provedor de ferramentas permite que sistemas externos se integrem com um LMS. O Adobe Learning Manager atua como um provedor de ferramentas de LTI, permitindo que outras plataformas LMS acessem cursos, certificados ou programações de aprendizado do Adobe Learning Manager diretamente no LMS.

**LTI como consumidor de ferramentas**: a LTI como consumidor de ferramentas permite que o LMS integre ferramentas externas por meio da Interoperabilidade das Ferramentas de Aprendizado (LTI). Nesse cenário, o LMS é um consumidor de serviços fornecidos por ferramentas externas. O Adobe Learning Manager atua como um consumidor de ferramenta de LTI, permitindo que ele integre ferramentas de aprendizado de terceiros. Isso permite que os alunos do Adobe Learning Manager realizem cursos, certificados ou programações de aprendizado das ferramentas de terceiros no Adobe Learning Manager.

Consulte este artigo [Interoperabilidade da Learning Tool](/help/migrated/integration-admin/feature-summary/learning-tools-interoperability.md) para obter mais informações.

## Credly

Ao usar a Credly, um administrador no ALM permite que os alunos gerenciem e compartilhem medalhas externas da plataforma em vários canais de redes sociais.

### O que é a Credly?

Credly é uma plataforma de credencial digital que permite que alunos e organizações ganhem, compartilhem e verifiquem conquistas profissionais, como medalhas ou certificações. Os alunos podem gerenciar e compartilhar medalhas por meio de seu perfil de credencial nas redes sociais e em outros lugares.

### Integrar o Credly ao Adobe Learning Manager

Primeiro, adicione o conector Credly no Adobe Learning Manager (ALM). Em seguida, migre as medalhas existentes da Credly para garantir a continuidade das conquistas do aluno. Por fim, crie uma habilidade no Adobe Learning Manager para o caminho de aprendizado apropriado para aprimorar o desenvolvimento e o reconhecimento do aluno.

Consulte este artigo [Credencialmente](/help/migrated/integration-admin/feature-summary/credly-integration.md) para obter mais informações

## Painel de conformidade

Nesta versão, os administradores agora podem compartilhar o painel com outros administradores, administradores personalizados e gerentes de loja, dando a eles acesso instantâneo aos painéis de conformidade. Eles agora podem definir o widget de conformidade padrão na página inicial do aluno, permitindo que os alunos controlem seus requisitos de conformidade. Consulte este artigo [Painel de conformidade](/help/migrated/administrators/feature-summary/reports.md#share-compliance-dashboard-with-admins-and-custom-admins) para obter mais informações.

## Suporte a vários idiomas

O Adobe Learning Manager (ALM) agora permite que os autores criem instâncias específicas do idioma usando a marcação de idioma nos módulos Sala de aula e Sala de aula virtual. Os alunos podem acessar os módulos CR/VC em seu idioma preferido. Por exemplo, um autor pode criar um módulo CR/VC com duas instâncias: uma em inglês e outra em francês. Os alunos podem selecionar as instâncias em seu idioma preferido.

Consulte este artigo [Adicionar objetos de aprendizado em locais diferentes](/help/migrated/authors/feature-summary/add-new-language-learning-objects.md#multi-language-support-for-crvc-instances-with-language-tagging) para obter mais informações.

## Funções personalizadas

As funções personalizadas permitem que os administradores definam funções e responsabilidades específicas para diferentes grupos de usuários, garantindo melhor gerenciamento e controle. Com esta versão, o ALM aprimora as funções personalizadas, fornecendo controle mais detalhado sobre as seções a seguir.

* Usuários
* Cursos
* Caminhos de aprendizado
* Certificações
* Ajudas de tarefa
* Catálogos

Os administradores podem atribuir permissões precisas com base nas responsabilidades do usuário, garantindo que cada grupo tenha acesso apenas aos recursos e ao conteúdo relevantes. Esses controles aprimorados permitem um gerenciamento mais granular das seções principais.

Faça logon como administrador e navegue até **[!UICONTROL Usuários]** > **[!UICONTROL Funções personalizadas]** para criar e gerenciar as Funções Personalizadas.

Consulte este artigo [Funções personalizadas](/help/migrated/administrators/feature-summary/custom-role.md) para obter mais informações.

## Comentários de conclusão

Os administradores agora podem adicionar comentários ao marcar os alunos como concluídos em cursos, programações de aprendizado ou certificações. Os administradores podem adicionar comentários para um ou vários alunos ao mesmo tempo, e os comentários aparecem no relatório [Transcrições do aluno](/help/migrated/administrators/feature-summary/reports.md#learner-transcripts).

Consulte este artigo [Comentários de conclusão](/help/migrated/administrators/feature-summary/courses.md#completion-comments) para obter mais informações.

## Relatório de grupo de usuários

O novo **[!UICONTROL Relatório de grupo de usuários]** do Adobe Learning Manager ajuda a gerenciar grupos de usuários, fornecendo visibilidade sobre grupos deixados sem gerenciamento quando os administradores saíram. Os administradores podem acessar os relatórios na seção **[!UICONTROL Usuários]** > **[!UICONTROL Grupo de Usuários]**. Ele fornece informações detalhadas sobre cada grupo, incluindo:

* Tipo de grupo de usuários
* Nome do grupo
* Descrição
* Criado por (Nome)
* Criado por (Email)
* Criado em (Fuso horário UTC)
* Número de usuários

Consulte este artigo [Relatório de grupo de usuários](/help/migrated/administrators/feature-summary/add-users-user-groups.md#user-group-report) para obter mais informações.

## Relatório de lista de espera

O novo **[!UICONTROL Relatório de lista de espera]** do Adobe Learning Manager permite que os administradores baixem a lista de alunos na lista de espera de todas as instâncias de um curso. Administradores e professores podem acessar este relatório da seção **[!UICONTROL Lista de espera]** no **[!UICONTROL Curso]** ou na página **[!UICONTROL Visão geral da sessão]**. O relatório de lista de espera pode ser baixado das seções Administrador e Professor.

Seguindo as colunas disponíveis no relatório Lista de espera:

* Nome do curso
* Nome da instância
* ID da instância
* Status da instância
* Nome do usuário
* Email
* ID exclusiva do usuário
* Data da inscrição (fuso horário central da Europa)
* Status
* Número na lista de espera
* Limite de listas de espera
* Limite de vaga

Consulte estes artigos [Relatório de lista de espera (Admin)](/help/migrated/administrators/feature-summary/courses.md#waitlist-report) e [Relatório de lista de espera (Professores)](/help/migrated/instructors/feature-summary/learners.md#waitlist-report) para baixar o relatório da seção Administrador e Professor.

## Acessibilidade na página inicial do aluno

O Adobe Learning Manager agora oferece suporte a texto alternativo para todas as manchetes a fim de melhorar a acessibilidade para os alunos. Isso permite que alunos com necessidades especiais usem leitores de tela para ler o texto alternativo e entender a imagem. Você pode selecionar vários idiomas e fornecer texto alternativo para cada idioma. Certifique-se de adicionar o texto alternativo nos respectivos idiomas. Verifique se o logotipo da empresa em sua conta também inclui texto alternativo com o nome da empresa.
Consulte este artigo [Anúncio](/help/migrated/administrators/feature-summary/announcements.md#masthead) para obter mais informações.

## Suporte para hindi

O Adobe Learning Manager agora apresenta o hindi como uma das linguagens de interface da plataforma e suporta o crescimento da plataforma na Índia. O suporte para falantes nativos de híndi garante que todos os recursos, relatórios e a experiência geral do usuário estejam totalmente acessíveis aos usuários.

>[!NOTE]
>
>Os certificados de emblema gerados pelo sistema no formato PDF não suportarão híndi.

Para alterar o idioma da interface, siga estas etapas:

1. Faça logon como **[!UICONTROL Administrador]**.
2. Vá para **[!UICONTROL Configurações de Perfil]** > **[!UICONTROL Idioma da Interface]**.
3. Selecione **[!UICONTROL Hindi]** como uma linguagem de interface.


## Checagem de profanação para publicações em redes sociais

O Adobe Learning Manager agora bloqueia publicações em redes sociais no aplicativo dos alunos que contêm palavras proibidas. Isso ajuda a manter as coisas profissionais e em conformidade, especialmente em áreas sensíveis como a saúde.

## Otimização do modelo de email

### Enviar e-mail aos alunos quando um professor for atribuído

Os emails existentes **[!UICONTROL Você foi adicionado como professor]** e os **[!UICONTROL Detalhes da Sessão do VCProvider]** foram combinados em um email **[!UICONTROL Você foi adicionado como UserType]**. O **[!UICONTROL UserType]** será **[!UICONTROL Professor]** ou **[!UICONTROL Organizador]**, com base na função do usuário. Esses emails não estavam disponíveis na interface antes. Eles agora foram combinados em um único email e adicionados à interface do usuário. Os administradores podem acessar este modelo na seção **[!UICONTROL Modelo de Email]**. Ela será ativada por padrão para todas as contas novas e existentes, mas os administradores podem desativá-la ou ativá-la na mesma seção. Este e-mail será enviado sempre que uma sessão for criada e um professor for atribuído, seja para sessões como Zoom, Equipes, Connect ou outros serviços.

### Enviar e-mail aos alunos quando uma sessão for cancelada

Os professores removidos de uma sessão agora receberão apenas um email de cancelamento de sessão. Anteriormente, eles receberam um e-mail de cancelamento e atualização. Os professores que permanecem em uma sessão receberão um email de atualização da sessão junto com um novo convite para a sessão.

## Critérios de conclusão do MS Teams

Atualmente, os alunos são marcados como frequentados, mesmo se ingressarem em uma sessão de VILT (Virtual Instructor-Led Training, treinamento virtual ministrado por instrutor) por apenas alguns segundos. Com esta versão, introduzimos critérios de conclusão para módulos de equipes para garantir uma participação mais precisa. Os autores agora podem definir um tempo mínimo que os alunos devem passar em uma sessão VILT para que sua participação seja contada.

Esse é um recurso de back-end que está desativado por padrão. Entre em contato com o CSM para ativá-lo.

## Atualizando novos endereços IP para entrega de email

Para aprimorar a confiabilidade de entrega de e-mails, estamos adicionando novos endereços IP ao nosso pool existente. Para garantir uma comunicação de email ininterrupta, atualize as configurações de email da sua organização conforme necessário.

Atualmente, usamos os seguintes endereços IP para a entrega de email:

* 149.72.162.66
* 167.89.5.155

Os seguintes endereços IP serão adicionados ao nosso pool de entrega de email:

* 159.183.228.93
* 159.183.225.26
* 159.183.218.22
* 168.245.57.144

>[!NOTE]
>
>Se necessário, sugerimos colaborar com sua equipe de TI para adicionar os endereços IP à lista de urls permitidos.

## Alterações na migração

As seguintes alterações são feitas no fluxo de trabalho de migração:

* Migrar módulos para pastas específicas.
* Adição de critérios de conclusão para módulos.
* Adição de critérios de conclusão para cursos

### Alterações na migração de módulos

Ao migrar módulos para o ALM, eles serão salvos na pasta pública por padrão. Nesta versão, adicionamos uma nova coluna chamada `folder` no arquivo [module_version.csv](assets/module_version.csv). Os administradores podem usar essa coluna para especificar o nome da pasta para onde os módulos devem ir após a migração. Os administradores também podem colocar um único módulo em várias pastas listando os nomes das pastas separados por vírgulas.

A coluna de pasta usa o tipo de dados string e é uma coluna opcional. Estas são as condições para a coluna de pasta:

* O nome da pasta que você adiciona deve ser uma pasta de conteúdo existente na conta do ALM.
* Os valores devem ser uma cadeia de caracteres separada por vírgulas.
* Se você adicionar um novo nome de pasta para um módulo já presente em uma pasta diferente, o novo valor não substituirá nem substituirá a pasta atribuída. O módulo será adicionado à nova pasta e também permanecerá disponível na pasta existente.
* Se o valor estiver em branco, a pasta assumirá **[!UICONTROL Pública]** como padrão.

Consulte o arquivo de especificação csv [module_version](assets/4-module_version.xlsx) para obter mais informações.

### Alterações na migração de módulos — critérios de conclusão

Os administradores podem especificar os critérios de conclusão dos módulos durante a migração do módulo. Nesta versão, adicionamos novas colunas `completionCriteria`, `viewPercent` e `quizData` no [module_version.csv](assets/module_version.csv).

Estas são as condições para as novas colunas:

1. `completionCriteria`:

   * O tipo de dados deve ser uma cadeia de caracteres e os valores compatíveis são:
      * `LAUNCH_CONTENT`
      * `VIEW_PERCENT`
      * `QUIZ`
      * `MARK_COMPLETE`
   * Adicione critérios de conclusão no nível do módulo somente para tipos de módulo em ritmo individualizado.
   * Os valores com suporte para conteúdo estático são `LAUNCH_CONTENT` e `VIEW_PERCENT`.
   * Os valores com suporte para conteúdo interativo são `LAUNCH_CONTENT`, `VIEW_PERCENT` e `QUIZ`.
   * Os valores com suporte para o conteúdo HTML5 são `LAUNCH_CONTENT` e `MARK_COMPLETE`.

2. `viewPercent`:

   * O tipo de dados desta coluna deve ser um inteiro e o valor deve estar entre 0 e 100.
   * Quando completedCriteria estiver definido como `VIEW_PERCENT`, insira a porcentagem de exibição necessária nesta coluna ou deixe-a em branco.

3. `quizData`:

   * O tipo de dados deve ser uma cadeia de caracteres e os valores com suporte são `QUIZ_ATTEMPTED`, `QUIZ_PASSED` e `QUIZPASSED_OR_LIMITREACHED`.
   * Quando `completionCriteria` estiver definido como `QUIZ`, insira o valor apropriado para o questionário na coluna `quizData`.

Consulte o arquivo de especificação csv [module_version](assets/4-module_version.xlsx) para obter mais informações.

### Alterações na migração do curso — Critérios de conclusão

Os administradores podem especificar os critérios de conclusão dos cursos durante a migração do curso. Nesta versão, adicionamos uma nova coluna chamada `completionCriteria` no [course.csv](assets/course.csv).

Estas são as condições para a coluna `completionCriteria`:

* O tipo de dados deve ser string ou número, e é um campo opcional.
* Os valores devem ser `ALL`, `X` e `SELECTEDMODULES`.
* X é um valor inteiro que deve ser maior que 0 e menor que o número total de módulos.
* Se você definir `completionCriteria` como `SELECTEDMODULES`, precisará marcar os módulos obrigatórios no arquivo [course_module.csv](assets/course_module.csv).
* Na coluna `optionalCriteria`, insira `TRUE` ou `FALSE`. Se você definir o valor como `TRUE`, tornará o módulo obrigatório.

Consulte o arquivo de [especificação csv do curso](assets/3-course.xlsx) e o arquivo de especificação csv do [course_module](assets/6-course_module.xlsx) para obter mais informações.

## Alterações de API

Estas são as alterações da API:

* **API de pesquisa**:
   * Novo filtro de modo com opções: classicSearch e advanceSearch.
   * Nova opção loMetadata para snippetTypes.
* **API de Comunicado**:
   * Inclui o atributo altText para descrições de manchete.
* **APIs de instância**:
   * Novo atributo de localidade para recuperar detalhes de localidade.
* **Verificação de profanação**:
   * APIs atualizadas para verificar palavras proibidas em comentários e respostas em publicações em redes sociais:
* **Limitação de RPM e intermitência**:
   * Limites de RPM (Solicitações por minuto) e intermitência adicionados para todas as APIs.
* **APIs de medalha**:
   * Novo atributo externalProvider para recuperar informações sobre emblemas externos.
* **API de Trabalho**:
   * Baixe o Relatório de grupo de usuários e o Relatório de auditoria de função personalizada usando a API de trabalho.

### Alterações na API de pesquisa

A API de pesquisa agora tem um novo filtro de modo com duas opções: `classicSearch` e `advanceSearch`. Há também uma nova opção `loMetadata` para `snippetTypes`. Para obter os melhores resultados, inclua `loMetadata` em `snippetTypes` ao usar o modo `advanceSearch`.

### Alterações na API de comunicado

O `GET /announcements API` agora inclui o atributo `altText` para fornecer a descrição da manchete.

#### Exemplo de solicitação usando cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' 'https://abcd.adobe.com/primeapi/v2/announcements/123456'
```

#### Exemplo de resposta:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/announcements/123456"
  },
  "data": {
    "id": "12345",
    "type": "adminAnnouncement",
    "attributes": {
      "actionUrl": "google.com",
      "announcementType": "MASTHEAD",
      "expiryDate": "2038-01-19T03:14:07.000Z",
      "liveDate": "2024-07-31T11:11:30.000Z",
      "contentMetaData": [
        {
          "contentType": "IMAGE",
          "contentUrl": "https://abcd.adobe.com",
          "locale": "en-US",
          "altText": "Moonlight - english changed new",
          "thumbnailUrl": "https://abcd.adobe.com/"
        },      ]
    }
  }
}
```

### Alterações nas APIs de instância

O novo atributo `locale` foi adicionado às seguintes APIs para recuperar detalhes de localidade.

* `GET /learningObjects/{loId}/instances/{loInstanceId}`
* `GET /learningObjects/{id}?include=instances,enrollment.loInstance`
* `GET /learningObjects?include=instances,enrollment.loInstance`
* `GET /learningObjects/{id}/relatedLOs?include=instances,enrollment.loInstance`
* `POST /learningObjects/query?include=instances,enrollment.loInstance`
* `POST /search/query?include=model.instances`
* `GET /search?include=model.instances`

#### Exemplo de solicitação usando cURL:

```
curl --location 'http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567' \
```

#### Exemplo de solicitação:

```
{
    "links": {
        "self": "http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567"
    },
    "data": {
        "id": "course:1234567_1234567",
        "type": "learningObjectInstance",
        "attributes": {
            "dateCreated": "2024-02-27T09:21:25.000Z",
            "isAET": false,
            "isDefault": true,
            "isFlexible": false,
            "locale": "en-US",
            "state": "Active",
            "localizedMetadata": [
                {
                    "locale": "en-US",
                    "name": "Default instance"
                }
            ]
        },
        "relationships": {
            "learningObject": {
                "data": {
                    "id": "course:1234567",
                    "type": "learningObject"
                }
            },
            "loResources": {
                "data": [
                    {
                        "id": "course:123456_1234567_1234567_1",
                        "type": "learningObjectResource"
                    }
                ]
            }
        }
    }
}
```

### Alterações na API pública para verificação de profanação

As APIs a seguir foram atualizadas para executar verificações de conteúdo profano para comentários e respostas em publicações em redes sociais.

* `POST /boards/{id}/posts `
* `PATCH /posts/{id}`
* `POST /posts/{id}/comments`
* `PATCH /comments/{id}`
* `POST /comments/{id}/replies`
* `PATCH /replies/{id}`

Se uma palavra restrita for encontrada na postagem, a seguinte resposta será enviada.

#### Exemplo de resposta:

```
{
  "status": "FORBIDDEN",
  "title": "BAD_WORD_FOUND",
  "source": {
    "info": "Unacceptable word found in post"
  }
}
```

### Alterações na limitação de RPM e intermitência

Nesta versão, os limites de RPM (Solicitações por minuto) e intermitência foram adicionados para todas as APIs. O RPM máximo para cada API pode ser verificado na página Swagger.

RPM é o número de solicitações que você pode enviar ao servidor da API em um minuto. O limite de intermitência permite um número maior de solicitações por um curto período, indo além do limite de taxa normal. Por exemplo, a API `learningObject` permite um máximo de 15 solicitações por minuto. Se esse limite for excedido, a API retornará uma mensagem de erro.

### Alterações nas APIs de medalha

O novo atributo `externalProvider` foi adicionado às seguintes APIs para recuperar informações sobre emblemas externos, incluindo a ID da medalha e o nome do provedor.

* `GET /badges `
* `GET /badges/{id}`
* `GET /skills?include=levels.badge`
* `GET /skills/{id}?include=levels.badge`
* `GET /learningObjects/{loId}/instances/{loInstanceId}?include=badge`
* `GET /users/{userId}/userBadges`
* `GET /users/{userId}/userBadges/{id}`

#### Exemplo de solicitação usando cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 123456789' 'https://abcd.adobe.com/primeapi/v2/badges/44'
```

#### Exemplo de resposta:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/badges/44"
  },
  "data": {
    "id": "44",
    "type": "badge",
    "attributes": {
      "imageUrl": "https://abcd.com/accountassets/1/badges/download.png",
      "name": "external badge",
      "state": "Active",
      "externalProvider": {
        "id": "1234sjd-b272-4de1-9b60-1234567",
        "provider": "credly"
      }
    }
  }
}
```

### Baixar relatórios de auditoria de grupo de usuários e função personalizada por meio da API de trabalho

O usuário pode baixar o **[!UICONTROL Relatório de Grupo de Usuários]** e o **[!UICONTROL Relatório de Auditoria de Função Personalizada]** usando o `Job API`.

#### Exemplo de solicitação para download do Relatório de grupo de usuários:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' -d '{ \ 
     "data": { \ 
         "type": "job", \ 
         "attributes": { \ 
             "jobType": "generateUserGroupReport" \ 
         } \ 
    } \ 
 }' 'https://abcd.adobe.com/primeapi/v2/jobs'
```

#### Exemplo de solicitação para download do Relatório de auditoria da função personalizada:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 1234567' -d '{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateCustomRoleAuditReport",
            "payload":{
                 "fromDate": "2020-01-01T18:30:00.000Z",
                 "toDate": "2024-09-31T18:30:00.000Z",
                 "locale":  "en-US"
            }
        }
   }
}
```

### Mensagem de erro para nenhum corpo de solicitação

Introduzimos mensagens de erro específicas para os casos em que o corpo da solicitação é obrigatório, mas não fornecido na API.

#### Amostra de mensagem de erro:

```
{
    "status": "BAD_REQUEST",
    "title": "Generic Error"
}
```

## Melhorias nos relatórios

Os administradores podem localizar essas alterações de relatório na seção **Administrador** > **Relatórios**.

### Relatório de transcrições de aprendizado

O relatório **[!UICONTROL Transcrições de Aprendizado]** conterá duas novas colunas:

* **[!UICONTROL ID do módulo]**: exibe o identificador exclusivo de cada módulo. Esta nova coluna foi adicionada após a coluna **[!UICONTROL Módulo]** existente.
* **[!UICONTROL ID da instância do curso]**: exibe o identificador exclusivo de cada instância do curso. Esta nova coluna foi adicionada após a coluna **[!UICONTROL Instância]** existente.
* **[!UICONTROL Comentário de conclusão]**: esta coluna captura os comentários inseridos pelo administrador ao marcar a conclusão do usuário. Esta nova coluna foi adicionada ao final do relatório.


### Relatório de resumo da sessão

O relatório **[!UICONTROL Resumo da Sessão]** conterá três novas colunas:

* A coluna **[!UICONTROL ID do Módulo]** foi adicionada antes da coluna **[!UICONTROL Nome da Sessão]**.
* A coluna **[!UICONTROL ID da Sessão]** foi adicionada antes da coluna **[!UICONTROL Nome da Sessão]**.
* A coluna **[!UICONTROL ID da instância do curso]** foi adicionada após a coluna **[!UICONTROL Nome da instância]**.
* A coluna **[!UICONTROL Contagem de conclusão]** foi adicionada após a coluna **[!UICONTROL Contagem de Inscrições]**.

## Erros corrigidos nesta atualização

* Correção de um erro que ocorria ao carregar vídeos do módulo de atividade durante o envio de arquivos em dispositivos Android e iOS.
* Correção do problema ao abrir cursos no aplicativo móvel; a versão da Web está funcionando corretamente.
* Correção do problema com a exibição de ajudas de tarefa e outros recursos no Safari.
* Correção de um problema que impedia os usuários de baixar ajudas de tarefa no aplicativo móvel.
* Correção do erro na documentação da API de usuário de patch.
* Correção de um problema em que os organizadores não recebiam notificações por e-mail quando uma sessão era excluída do curso.
* Correção de um problema em que os organizadores não recebiam e-mails de cancelamento de sessão quando um módulo era removido do curso e republicado.
* Foi adicionado suporte para inclusão de caracteres especiais “+” e “-” em endereços de email durante a criação de usuários externos.
* Correção de um problema em que a sincronização do relatório unificado do conector do Marketo falhava, se o relatório de habilidades do usuário contivesse aspas duplas no valor do registro CSV
* Correção de um problema em que o ponto de extremidade `/skills` retornava o estado correto para a API do administrador, mas a API do aluno mostrava consistentemente dados incorretos ou armazenados em cache.
* Correção do problema com a integração do Go1 para cursos freemium que falhava quando a conta não tinha o conector Go1 configurado.
* Correção de um problema em que os cursos no Caminho de aprendizado (LP) não eram acessíveis por migração se o aluno já tivesse concluído a LP.
* Correção de um problema em que o CSV de usuário incremental falhava quando o gerente do usuário e o gerente de nível ignorado eram definidos como SU (Super Usuário) em vez de administrador e não estavam incluídos no CSV.
* Correção de problemas de escopo para gerentes de loja em relatórios do painel.
* Correção de um problema em que xapi_iri não era removido quando um curso de rascunho era excluído.
* Correção de um problema que impedia a adição de uma ID de OA exclusiva em determinados cenários.
* Correção de um problema em que a propriedade IsEmbeddable no plano de aprendizado não era atualizada corretamente em planos de aprendizado compartilhados.
* Correção de um problema que afetava a exibição da duração total de caminhos de aprendizado na exibição do aluno.
* Correção de um problema que permitia aos alunos se registrarem ou se inscreverem por meio de links de autorregistro mesmo após suas contas terem sido excluídas.
* Correção de um problema em que `www` era removido ao adicionar links na descrição do curso durante a criação do curso.
* Correção de um problema em que as informações ocultas e as ajudas de tarefa de download não funcionavam corretamente.
* Correção de um problema em que o logon único (SSO) não funcionava para novos usuários adicionados por meio do link de autorregistro com uma ID de IP.
* Correção de um problema em que os dados da mensagem de notificação não eram buscados após a exclusão de um comunicado.
* Correção do problema de resultados insuficientes na pesquisa de usuários por email.

## Requisitos do sistema

Exibir [requisitos de sistema do Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notas de versão

Confira as [notas de versão](/help/migrated/release-note/release-notes.md) para obter as atualizações de versão mais recentes.

## Versões anteriores do Adobe Learning Manager

* [Versão de julho de 2024](/help/migrated/whats-new-july-2024.md)
* [Versão de março de 2024](/help/migrated/whats-new-march-2024.md)
