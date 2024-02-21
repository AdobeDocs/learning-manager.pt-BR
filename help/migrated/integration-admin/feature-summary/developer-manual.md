---
jcr-language: en_us
title: Manual do desenvolvedor de aplicativos
description: A API V1 do Learning Manager foi descontinuada. As APIs V1 deixarão de funcionar a partir de 28 fevereiro de 2021. Recomendamos usar as APIs V2 para interagir com o Learning Manager.
contentowner: jayakarr
source-git-commit: 956c119a5650b535a906157dc4d36f2ff075cf01
workflow-type: tm+mt
source-wordcount: '3385'
ht-degree: 62%

---



# Manual do desenvolvedor de aplicativos

>[!NOTE]
>
>A API V1 do Learning Manager foi descontinuada. Recomendamos usar as APIs V2 para interagir com o Learning Manager.


## Visão geral {#overview}

O [Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) é uma solução de gerenciamento de aprendizagem de autosserviço centrada no aluno e hospedada na nuvem. Os clientes podem acessar os recursos do Learning Manager de forma programáda usando a API do Learning Manager para integrá-los a outros aplicativos corporativos. A API também pode ser usada por parceiros da Adobe para aprimorar a proposta de valor do Learning Manager, estendendo a sua funcionalidade ou integrando-a a outros aplicativos ou serviços.

### Cenário de uso {#usagescenario}

Usando a API do Learning Manager, os desenvolvedores podem criar aplicativos independentes que ampliam sua funcionalidade ou o integram a outros fluxos de trabalho de aplicativos corporativos. Você pode desenvolver um aplicativo da Web, um cliente de desktop ou um aplicativo móvel usando qualquer tecnologia de sua escolha. Como desenvolvedor, você pode acessar os dados do aplicativo no Learning Manager. A implantação do aplicativo que você desenvolve é externa à plataforma do Learning Manager e você tem controle total sobre o ciclo de vida do desenvolvimento de software à medida que o aplicativo evolui. Geralmente, os aplicativos são desenvolvidos por uma organização do cliente para usar com a conta do Learning Manager, e esses aplicativos são privados para essa organização do cliente específica. Além disso, os parceiros da Adobe podem criar aplicativos genéricos com a API do Learning Manager, que podem ser usados por um grande conjunto de clientes do Learning Manager.

## API do Learning Manager {#apidescription}

A API do Learning Manager é baseada nos princípios de REST e expõe os elementos-chave do Modelo de objeto do Learning Manager aos desenvolvedores de aplicativos por meio de HTTP. Antes de conhecer os detalhes dos pontos de extremidade da API e dos métodos HTTP, os desenvolvedores podem se familiarizar com os vários objetos do Learning Manager, os seus atributos e inter-relacionamentos. Uma vez que os modelos são entendidos, será útil obter um entendimento básico da estrutura de solicitações e respostas da API, e alguns termos comuns de programação que usamos genericamente em toda a API.

Para obter detalhes sobre os diversos métodos e pontos de extremidade da API, consulte  [Documentação da API do Learning Manager](https://learningmanager.adobe.com/docs/primeapi/v2/).

## APIs do aluno

Adobe Learning Manager - as APIs do aluno permitem que você crie uma experiência de aprendizado personalizada para seus usuários. O uso dessas APIs precisa de um token de usuário válido e deve ser usado apenas para fins de fluxos de trabalho em que haja um aluno totalmente licenciado/registrado.

>[!IMPORTANT]
>
>Eles não devem ser usados, como estão, para qualquer tipo de recuperação de dados para suportar usuários não conectados/compartilhados ou quaisquer outros casos.

Os casos de uso não conectados exigem tratamento especial.

**Entre em contato com a equipe de Arquitetura de solução, caso você tenha dúvidas sobre o uso apropriado dessas APIs, e certifique-se de que um arquiteto de solução tenha verificado uma solução antes de implantá-la**.

## Autenticação da API {#apiauthentication}

Ao gravar um aplicativo que faz chamadas de API para o Learning Manager, você precisa registrar o aplicativo usando o aplicativo do administrador de integração.

As APIs do Learning Manager usam a estrutura OAuth 2.0 para autenticar e autorizar os seus aplicativos cliente.

**Procedimento**

**1. Configurar o aplicativo**

Você pode configurar o aplicativo com a ID do cliente e o segredo do cliente para usar os pontos de extremidade apropriados. Depois de registrar o aplicativo, você pode obter a clientId e o clientSecret. Obter URL deve ser usado no navegador, pois ele autentica os usuários do Learning Manager usando as suas contas pré-configuradas, como SSO, Adobe ID e assim por diante.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Após a autenticação bem-sucedida, o navegador redireciona para o redirect_uri mencionado no URL acima. Um **código** de parâmetro é anexado junto com o uri de redirecionamento.

**2. Obtenha o token de atualização do código**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

Corpo da solicitação post:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  code: 
  <code from step 1></code>
 </enter>
</enter>
```

**3.** **Obter um token de acesso do token de atualização**

URL para obter o token de acesso:

POST [https://learningmanager.adobe.com/oauth/token/refresh](https://learningmanager.adobe.com/oauth/token/refresh) Content-Type: application/x-www-form-urlencoded

Corpo da solicitação post:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  refresh_token: 
  <refresh token>
   
  </refresh>
 </enter>
</enter>
```

**URL para verificar os detalhes do token de acesso**

`GET https://learningmanager.adobe.com/oauth/token/check?access_token=<access_token>`

**Limitação de uso**

Um token de acesso é válido por sete dias. Depois de um dia, você tem que gerar um novo token de acesso usando o token de atualização. Se você gerar um novo token de acesso a partir do token de atualização enquanto um token de acesso existente ainda for válido, o token existente será retornado.

Alguns dos termos usados com frequência na API do Learning Manager são explicados abaixo para a sua referência.

**Inclui**

Os desenvolvedores podem acessar um único modelo de objeto de API e também vários modelos associados a esse modelo. Para acessar os modelos relacionados subsequentes, você precisa entender a relação de cada modelo com outros modelos. **Inclui** permite que os desenvolvedores acessem os modelos dependentes. É possível usar um separador de vírgulas para acessar vários modelos. Para obter exemplos de uso e mais detalhes sobre **inclui**, consulte a seção modelo de API de amostra nesta página.

**Solicitação de API**

As solicitações de API podem ser feitas através de uma solicitação HTTP. Dependendo do ponto de extremidade e do desenvolvedor de métodos, você pode ter a opção de vários verbos HTTP, como GET, PUT, POST, DELETE, PATCH etc. Para algumas solicitações, os parâmetros de consulta podem ser transmitidos. Ao fazer uma solicitação para um modelo de dados específico, o usuário também pode solicitar modelos relacionados conforme descrito nas especificações da API JSON. A estrutura de uma Solicitação de API típica é descrita no [exemplo de uso do modelo](#main-pars_header_1415780624).

**Resposta da API**

Quando uma solicitação de API é feita por um cliente, um documento SON é obtido de acordo com a especificação da API JSON. A resposta também contém o código Status HTTP, que o desenvolvedor pode verificar para executar as próximas etapas apropriadas na lógica do aplicativo. A estrutura de uma Resposta de API típica é descrita em  [exemplo de uso do modelo](#main-pars_header_1415780624).

**Erros**

Quando uma solicitação de API falha, uma resposta de erro é obtida. O código de status HTTP retornado na resposta indica a natureza do erro. Os códigos de erro são representados com números para cada modelo na referência da API. 200, 204, 400 e 404 são alguns dos erros comuns representados em APIs que indicam problemas de acesso HTTP.

**Campos**

Os atributos do objeto de API e suas relações são coletivamente chamados de Campos. Consulte a [API JSON para obter mais informações.](http://jsonapi.org/format/#document-resource-object-fields) Você pode usar Campos como um parâmetro enquanto faz chamadas de API para buscar um ou mais atributos específicos do modelo. Na ausência do parâmetro Campos, a chamada da API busca todos os atributos disponíveis do modelo. Por exemplo, na seguinte chamada de API, os campos[habilidade]=name busca somente o atributo name do modelo de habilidade.

https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&amp;fields[skill]=name

**Paginação**

Às vezes, uma solicitação de API resulta em uma longa lista de objetos a serem retornados na resposta. Nesses casos, o atributo de paginação permite que o desenvolvedor busque os resultados sequencialmente em termos de várias páginas, onde cada página contém um intervalo de registros. Por exemplo, o atributo de paginação no Learning Manager permite definir o número máximo de registros a serem exibidos em uma página. Além disso, você pode definir o valor do intervalo dos registros a serem exibidos na página.

**Classificação**

A classificação é permitida em modelos de API. Com base no modelo, escolha o tipo de classificação a ser aplicado para os resultados. A classificação pode ser aplicada em ordem crescente ou decrescente. Por exemplo, se você especificar `code sort=name`, em seguida, é uma classificação ascendente por nome. Se você especificar `code sort=-name`, é uma classificação descendente por nome. Consulte [Especificação da API JSON para obter mais informações](http://jsonapi.org/format/#fetching-sorting).

## Ilustração de uso da API {#samplemodel}

Vamos considerar um cenário em que um desenvolvedor deseja obter o nome da habilidade, os pontos máximos atribuídos ao nível de habilidade e os pontos obtidos pelo aluno para essa habilidade.

Um modelo userSkill nas APIs do Learning Manager consiste em id, type, dateAchieve, dateCreated, pointsEarned como atributos padrão. Portanto, quando um desenvolvedor usa o método GET para adquirir detalhes do modelo userSkill, os dados atuais pertencentes aos atributos padrão são mostrados na saída de resposta.

Mas, nesse cenário, o desenvolvedor quer obter o nome da habilidade e os pontos de nível de habilidade para o usuário. A API do Learning Manager permite que você acesse essas informações relacionadas usando os campos de relacionamento e inclua o parâmetro. Os modelos associados para userSkill são obtidos na tag de relacionamentos. Você pode obter os detalhes de cada modelo associado chamando esses modelos junto com o userSkill. Para obter essas informações, use **`code include`** parâmetro com valores separados por ponto (ponto) para cada um dos modelos associados. Você pode usar vírgula como separador para solicitar outro modelo, como user include=skillLevel.skill,course

**Chamada de API**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

Por exemplo, userId pode ser 746783 e userSkills id: 746783_4426_1.

**Resposta da chamada de API**

```
\{ 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1?include=skillLevel.skill&fields[userSkill]=pointsEarned&fields[skillLevel]=maxCredits&fields[skill]=name"}, 
 "data": { 
 "id": "746783_4426_1", 
 "type": "userSkill", 
 "attributes": {"pointsEarned": 5}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1"} 
 }, 
 "included": [ 
 { 
 "id": "4426", 
 "type": "skill", 
 "attributes": {"name": "Java"}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/skills/4426"} 
 }, 
 { 
 "id": "4426_1", 
 "type": "skillLevel", 
 "attributes": {"maxCredits": 10} 
 } 
 ] 
} 
```

## Modelos do Learning Manager {#models}

A API do Learning Manager permite que os desenvolvedores acessem objetos do Learning Manager como recursos RESTful. Cada ponto de extremidade da API representa um recurso, geralmente uma instância de objeto, como Medalha ou uma coleção desses objetos. Os desenvolvedores usam os verbos HTTP como PUT, GET, POST e DELETE para executar as operações CRUD nesses objetos (coleções).

API +++V1

O diagrama a seguir representa os vários elementos do Modelo de objeto do Learning Manager na API V1.

![](assets/er-diag-primemodels.png)

A tabela a seguir descreve vários elementos do modelo de objeto do Learning Manager V1:

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>Nº de série</strong></p></td>
   <td>
    <p><strong>Objeto do Learning Manager</strong></p></td>
   <td>
    <p><strong>Descrição</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>usuário</p></td>
   <td>
    <p>O usuário é o modelo principal no Learning Manager. Geralmente, os usuários são os alunos internos ou externos de uma organização que consomem objetos de aprendizado. No entanto, eles podem desempenhar algumas outras funções, como autor e gerente, juntamente com a função do aluno. ID do usuário, tipo, e-mail são alguns dos atributos embutidos. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>curso</p></td>
   <td>
    <p>O curso é um dos objetos de aprendizado compatíveis com o Learning Manager, que consiste em um ou mais módulos. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>módulo</p></td>
   <td>
    <p>O módulo é um bloco de construção para criar objetos de aprendizado no Learning Manager. Os módulos podem ser de quatro tipos diferentes; sala de aula, sala de aula virtual, atividade e ritmo individualizado. Use este modelo de módulo para obter os detalhes de todos os módulos em uma conta. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>certificação</p></td>
   <td>
    <p>A certificação é concedida aos alunos com base na conclusão bem-sucedida dos cursos. Os cursos são necessários no aplicativo antes de usar as certificações. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>programa de aprendizado</p></td>
   <td>
    <p>Os programas de aprendizado são cursos exclusivamente criados que atendem aos requisitos específicos de aprendizado dos usuários. Geralmente, os programas de aprendizado são usados para orientar os objetivos de aprendizado em cursos individuais. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>medalha</p></td>
   <td>
    <p>A medalha é um sinal de conquista que os alunos obtêm quando atingem etapas específicas enquanto avançam em um curso. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>habilidade</p></td>
   <td>
    <p>O modelo de habilidades consiste em níveis e créditos. As habilidades podem ser adquiridas pelos alunos após a conclusão relevante do curso. </p></td>
  </tr>
  <tr>
   <td>
    <p>8.      </p></td>
   <td>
    <p>certificationEnrollment</p></td>
   <td>
    <p>Este modelo fornece detalhes de uma inscrição de um usuário em uma única certificação.</p></td>
  </tr>
  <tr>
   <td>
    <p>9.  </p></td>
   <td>
    <p>courseEnrollment</p></td>
   <td>
    <p>Este modelo fornece detalhes de uma inscrição de um usuário em um único curso. </p></td>
  </tr>
  <tr>
   <td>
    <p>10.  </p></td>
   <td>
    <p>courseInstance</p></td>
   <td>
    <p>Um curso pode ter uma ou várias instâncias associadas a ele. Você pode obter a instância do curso </p></td>
  </tr>
  <tr>
   <td>
    <p>11.  </p></td>
   <td>
    <p>courseSkill</p></td>
   <td>
    <p>Um modelo courseSkill especifica o progresso de uma única habilidade, que é obtida ao concluir um curso.</p></td>
  </tr>
  <tr>
   <td>
    <p>12.  </p></td>
   <td>
    <p>courseModule</p></td>
   <td>Um modelo courseModule especifica como um módulo é incluído em um curso. Por exemplo, se o módulo é usado para pré-teste ou para conteúdo.</td>
  </tr>
  <tr>
   <td>
    <p>13.  </p></td>
   <td>learningProgramInstance</td>
   <td>
    <p>Um programa de aprendizado pode consistir em várias instâncias absorvendo propriedades semelhantes de um programa de aprendizado ou instâncias personalizadas. </p></td>
  </tr>
  <tr>
   <td>
    <p>14.  </p></td>
   <td>
    <p>ajuda de tarefa</p></td>
   <td>
    <p>Ajuda de tarefa é um conteúdo de aprendizado acessível aos alunos sem critérios de inscrição ou conclusão. Você pode obter, atualizar a data, o estado, as informações de ID juntamente com seus modelos relacionados, como a versão de ajuda de tarefa, os autores e o nível de habilidade. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>A ajuda de tarefa pode ter uma ou várias versões associadas a ela, com base em revisões de número no conteúdo e no número de uploads. Este modelo fornece detalhes de uma única versão de ajuda de tarefa. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnrollment</p></td>
   <td>
    <p>O programa de aprendizado consiste em uma ou várias instâncias. Os alunos podem se inscrever em uma instância do programa de aprendizado sozinhos ou atribuídos pelo administrador. Esse modelo fornece detalhes de uma inscrição de um usuário em uma única instância do programa de aprendizado. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Um módulo pode ter uma ou várias versões com base nos uploads de conteúdo revisado. Use este modelo para obter informações específicas sobre qualquer versão do módulo. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Um nível de habilidade compreende um ou vários cursos a serem consumidos para adquirir um nível junto com seus créditos associados. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>UserBadge relaciona uma única medalha com um único usuário. Contém detalhes de quando foi obtida, assertionUrl e assim por diante. </p></td>
  </tr>
  <tr>
   <td>
    <p>20.  </p></td>
   <td>
    <p>userSkill</p></td>
   <td>
    <p>UserSkill indica o quanto de um único nível de habilidade é alcançado por um único usuário.</p></td>
  </tr>
 </tbody>
</table>

+++

API +++V2

Veja a seguir os vários elementos do diagrama de classe do Learning Manager na API V2.

![](assets/v2api-class-diagram.jpg)

<table>
 <tbody>
  <tr>
   <th><b>Objeto do Learning Manager</b></th>
   <th><b>Descrição</b></th>
  </tr>
  <tr>
   <td>conta</td>
   <td>Encapsula os detalhes de um cliente do Learning Manager.</td>
  </tr>
  <tr>
   <td><code>
     badge
    </code></td>
   <td>A medalha é um sinal de conquista que os alunos obtêm quando atingem etapas específicas enquanto avançam em um curso. <br></td>
  </tr>
  <tr>
   <td><code>
     catalog
    </code></td>
   <td>O catálogo é uma coleção de objetos de aprendizado.</td>
  </tr>
  <tr>
   <td><code>
     user
    </code></td>
   <td>O usuário é o modelo principal no Learning Manager. Geralmente, os usuários são os alunos internos ou externos de uma organização que consomem objetos de aprendizado. No entanto, eles podem desempenhar algumas outras funções, como autor e gerente, juntamente com a função do aluno. ID do usuário, tipo, e-mail são alguns dos atributos embutidos. </td>
  </tr>
  <tr>
   <td>recurso</td>
   <td>Isso é usado para modelar cada recurso de conteúdo que um módulo procura encapsular. Todos os recursos encapsulados em <code>
     an
    </code> <code>
     loResource
    </code> são equivalentes em termos do objetivo de aprendizado, mas diferem entre si em termos do tipo de entrega ou do local do conteúdo.<br></td>
  </tr>
  <tr>
   <td>userNotification</td>
   <td>Este modelo contém informações de notificação relativas a um aluno.<br></td>
  </tr>
  <tr>
   <td>userSkill</td>
   <td>UserSkill indica o quanto de um único nível de habilidade é alcançado por um único usuário.<br></td>
  </tr>
  <tr>
   <td>userBadge</td>
   <td>UserBadge relaciona um único emblema <code>
     with
    </code> um único usuário. Contém pormenores como, por exemplo, quando foi alcançado, <code>
     assertionUrl
    </code> e assim por diante. <br></td>
  </tr>
  <tr>
   <td>habilidade</td>
   <td>O modelo de habilidades consiste em níveis e créditos. As habilidades podem ser adquiridas pelos alunos após a conclusão relevante do curso. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Um nível de habilidade compreende um ou vários cursos a serem consumidos para adquirir um nível junto com seus créditos associados. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Um objeto de aprendizado é uma abstração para vários tipos de objetos nos quais os usuários podem se inscrever e aprender. Atualmente, o Learning Manager tem os quatro tipos de objetos de aprendizado: curso, certificação e programa de aprendizado <code>
     and
    </code> Ajuda de tarefa.<br></td>
  </tr>
  <tr>
   <td>learningObjectInstance<br></td>
   <td>Uma instância específica de um objeto de aprendizado.<br></td>
  </tr>
  <tr>
   <td>learningObjectResource</td>
   <td>Isto equivale ao conceito de <code>
     module
    </code>. Um curso é composto por um curso <code>
     of
    </code> mais módulos. No Learning Manager, um módulo pode ser fornecido de várias maneiras equivalentes. Por conseguinte, a <code>
     loResource
    </code> essencialmente todos esses recursos equivalentes.<br></td>
  </tr>
  <tr>
   <td>loResourceGrade<br></td>
   <td>Isso encapsula o resultado do usuário que está consumindo um recurso específico no contexto de um objeto de aprendizado no qual ele está inscrito. Possui informações como a duração gasta pelos <code>
     user
    </code> no recurso, percentual do progresso feito pelo usuário, status de aprovação/reprovação e a pontuação obtida pelo usuário em qualquer quiz associado.<br></td>
  </tr>
  <tr>
   <td>calendário<br></td>
   <td>Um objeto de calendário é uma lista de <code>
     upcoming classroom
    </code> ou cursos em sala de aula virtual nos quais o usuário pode se inscrever.<br></td>
  </tr>
  <tr>
   <td>l1FeedbackInfo<br></td>
   <td>O Feedback L1 encapsula as respostas fornecidas por um aluno para as perguntas de feedback associadas aos Objetos de aprendizado. Normalmente, isso é coletado depois que o usuário conclui um Objeto de aprendizado, se configurado para coletar esse feedback dos alunos.<br></td>
  </tr>
  <tr>
   <td>inscrição<br></td>
   <td>Essa abstração encapsula os detalhes relativos à transação que representa a atribuição de um usuário específico a uma instância específica do objeto de aprendizado.<br></td>
  </tr>
 </tbody>
</table>

+++

Lista de atributos e relacionamentos de objetos.

+++conta

**Atributos**
dateCreated\
gamificaçãoAtivada\
id de catálogo padrão \
localidade\
loginUrl\
logoUrl\
name\
subdomínio\
themeData\
timeZoneCode

**Relações**
contentLocales(localizationMetadata)\
gamificationLevels(gamificationLevel)\
timeZones(timeZone)\
uiLocales(localizationMetadata)

+++

+++medalha

**Atributos**
id\
imageUrl\
name\
estado

+++

+++catálogo

**Atributos**
dateCreated\
dateUpdated\
descrição\
id de catálogo padrão \
isDefault\
isInternallySearchable\
isListable\
name\
estado

+++

+++dados

**Atributos**
id\
nomes

+++

+++gamificação

**Atributos**
cor\
name\
pontos

+++

+++learningObject

**Atributos**
authorNames\
dateCreated\
datePublished\
dateUpdated\
effectivenessIndex\
enrollmentType\
id de catálogo padrão \
imageUrl\
isExternal\
isSubLoOrderEnforced\
loType\
estado\
tags

**Relações**
authors(user)\
inscrição(learningObjectInstanceEnrollment)\
instâncias(learningObjectInstance)\
prerequisiteLOs(learningObject)\
skills(learningObjectSkill)\
subLOs(learningObject)\
complementarLOs(learningObject)\
additionalResources(recurso)

+++

+++learningObjectInstance

**Atributos**
completionDeadline\
dateCreated\
enrollmentCount\
id de catálogo padrão \
isDefault\
limite de vagas\
estado\
validade

**Relações**
medalha(medalha)\
l1FeedbackInfo(feedbackInfo)\
learningObject(learningObject)\
loResources(learningObjectResource)\
localizedMetadata(localizationMetadata)\
subLoInstances(learningObjectInstance)

+++

+++learningObjectInstanceEnrollment

**Atributos**
dateCompleted\
dateEnroll\
dateStarted\
hasPassed\
id de catálogo padrão \
porcentagemProgresso\
pontuação\
estado

**Relações**
learner(user)\
learnerBadge(userBadge)\
learningObject(learningObject)\
loInstance(learningObjectInstance)\
loResourceGrades(learningObjectResourceGrade)

+++

+++learningObjectResource

**Atributos**
externalReporting\
id de catálogo padrão \
loResourceType\
resourceType\
versão

**Relações**
learningObject(learningObject)\
loInstance(learningObjectInstance)\
localizedMetadata(localizationMetadata)\
resources(recurso)

+++

+++learningObjectResourceGrade

**Atributos**
dateCompleted\
dateStarted\
dateSuccess\
duração\
hasPassed\
id de catálogo padrão \
porcentagemProgresso\
pontuação

**Relações**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Atributos**
créditos\
id de catálogo padrão \
**Relações**
learningObject(learningObject)\
skillLevel(skillLevel)

+++

+++recomendação

**Atributos**
id\
motivo

**Relações**
learningObject(learningObject)

+++

+++recurso

**Atributos**
authorDesiredDuration\
completionDeadline\
contentStructureInfoUrl\
contentType\
contentZipSize\
contentZipUrl\
dateCreated\
dateStart\
wantedDuration\
downloadUrl\
extraData\
hasQuiz\
hasToc\
id de catálogo padrão \
instrutorNames\
isDefault\
localidade\
localização\
name\
onlyQuiz\
reportingInfo\
reportingType\
limite de vagas

+++

+++habilidade

**Atributos**
descrição\
id de catálogo padrão \
name\
estado

**Relações**
levels(skillLevel)

+++

+++skillLevel

**Atributos**
id\
nível\
maxCredits\
name\
**Relações**
medalha(medalha)\
skill( habilidade)

+++

+++usuário

**Atributos**
avatarUrl\
bio\
contentLocale\
e-mail\
campos\
id de catálogo padrão \
name\
pointsEarned\
perfil\
funções\
estado\
timeZoneCode\
uiLocale

**Relações**
account( conta)\
manager(user)

+++

+++userBadge

**Atributos**
assertionUrl\
dateAchieve\
id de catálogo padrão \
modelType

**Relações**
medalha(medalha)\
learner(user)\
model(learningObject)

+++

+++userCalendar

**Atributos**
curso\
courseType\
dateStart\
inscrito\
id de catálogo padrão \
mês\
trimestre

**Relações**
containerLO(learningObject)\
course(learningObject)

+++

+++userNotification

**Atributos**
actionTaken\
canal\
dateCreated\
id de catálogo padrão \
mensagem\
modelIds\
modelNames\
modelTypes\
leitura\
função

+++

+++userSkill

**Atributos**
dateAchieve\
dateCreated\
id de catálogo padrão \
pointsEarned

**Relações**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
user(usuário)

+++

## Processo de desenvolvimento de aplicativos {#registration}

## Pré-requisitos {#prerequisites}

Como desenvolvedor, você precisa criar uma conta de avaliação no Learning Manager para poder ter acesso total a todas as funções nessa conta. Para poder gravar um aplicativo, um desenvolvedor precisa criar alguns usuários e cursos e levar a conta a um estado razoável para que o aplicativo que está sendo desenvolvido possa ter acesso a alguns dados de amostra.

## Criar ID de cliente e segredo {#createclientidandsecret}

1. Entrada **Administrador de integração** faça login, clique em **[!UICONTROL Aplicativos]** no painel esquerdo.

   ![](assets/application-development-menu.png)

   *Selecionar Aplicativos no Administrador de Integração*

1. Clique em **[!UICONTROL Registrar]** no canto superior direito da página para registrar os detalhes do seu aplicativo. A página Registro é exibida.

   ![](assets/register-application.png)

   *Registrar o aplicativo*

   É obrigatório preencher todos os campos desta página.

   **Nome do aplicativo**: insira o nome do aplicativo. Não é obrigatório usar o mesmo nome de aplicativo; ele pode ser qualquer nome válido.

   **URL**: se souber o URL exato onde o aplicativo está hospedado, você poderá mencioná-lo. Se não estiver ciente, você poderá mencionar o URL da sua empresa. O nome de URL válido é obrigatório neste campo.

   **Domínios de redirecionamento**: insira o nome de domínio do aplicativo no qual você deseja que o aplicativo Learning Manager seja redirecionado após a autenticação OAuth. Você pode mencionar vários URLs aqui, mas deve usar os URLs válidos, como `http://google.com`, `http://yahoo.com` e assim por diante.

   **Descrição:** Insira a breve descrição do seu aplicativo.

   **Escopos:** Escolha uma das quatro opções disponíveis para definir o escopo do seu aplicativo. Com base na sua escolha mencionada aqui, o ponto de extremidade da API do Learning Manager está acessível para o seu aplicativo. Por exemplo, se você escolher **Acesso de leitura à função do aluno**, todos os pontos de extremidade da API do aluno do Learning Manager são somente leitura acessíveis ao seu aplicativo.

   **Apenas para esta conta?**\
   **Sim** - se você escolher Sim, o aplicativo não estará visível para outros administradores de conta.\
   **Não** - se você escolher Não, outros administradores de conta também poderão acessar este aplicativo, mas precisarão usar a ID do aplicativo para acessar esse aplicativo. A ID do aplicativo é gerada e exibida no modo Edição do aplicativo Learning Manager.

   Se você escolher **Acesso de leitura e gravação da função de administrador** como escopo durante o registro do aplicativo e escolha **Acesso de leitura da função de administrador** ao criar as APIs, você ainda pode ter acesso de gravação ao aplicativo, pois o escopo de registro do aplicativo substitui o fluxo de trabalho de autorização.

1. Clique em **[!UICONTROL Registrar]** no canto superior direito após preencher os detalhes na página de registro.

## Desenvolvimento e teste de aplicativos {#applicationdevelopmentandtesting}

A API do Learning Manager pode ser usada pelos desenvolvedores para criar qualquer aplicativo. Os desenvolvedores devem garantir que as suas contas sejam compostas por alguns usuários e cursos válidos. Eles podem criar alguns usuários simulados e cursos e simular a atividade na conta de avaliação para que possam testar a funcionalidade do aplicativo.

## Implantação de aplicativos {#applicationdeployment}

Recomendamos que o administrador do Learning Manager ou um administrador de integração da conta de produção assuma a propriedade de disponibilizar o aplicativo para os usuários em sua organização. Depois que o aplicativo for testado e considerado pronto para produção, informe o administrador da conta de produção. Preferencialmente, os administradores desejam gerar uma nova ID de cliente e segredo de cliente para o aplicativo na conta de produção e executar as etapas necessárias para incorporá-los no aplicativo de maneira segura. O procedimento real de implantação de aplicativos varia de empresa para empresa, e o administrador do Learning Manager da sua organização precisa receber suporte do departamento de TI/IS da organização para concluir a implantação.

## Aprovação de aplicativo externo {#externalapplicationapproval}

É possível adicionar aplicativos externos clicando em **Aprovar** no canto superior direito da **Aplicativos** página. Forneça a ID do aplicativo externo e clique em **Salvar.**

![](assets/add-external-application.png)

*Adicionar e aprovar um aplicativo externo*

## Perguntas frequentes

+++O Learning Manager tem uma integração de comércio eletrônico?

O Learning Manager não tem uma integração de comércio eletrônico. No entanto, fornecemos APIs para que você possa criar seu próprio LMS independente e implementar recursos de comércio eletrônico.
+++
