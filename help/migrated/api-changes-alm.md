---
description: Alterações de API no ALM
jcr-language: en_us
title: Alterações na API na versão de abril
source-git-commit: 3b35c16d74c83329cee24ee9ad007a53ccbd8cf3
workflow-type: tm+mt
source-wordcount: '4093'
ht-degree: 0%

---


# Alterações na API na versão de abril de 2026

A versão de abril de 2026 do Adobe Learning Manager apresenta aprimoramentos focados na API pública em torno de alternativas e equivalentes, acesso em janela de tempo ao conteúdo, tentativas de questionário orientadas por conteúdo, experiências não conectadas e manipulação de ajuda de tarefa. As alterações são projetadas para serem amplamente compatíveis com versões anteriores, permitindo integrações mais precisas.

## Aprendizado adaptável para caminhos de aprendizado

Esta versão adiciona suporte total à API pública para caminhos de aprendizado adaptáveis. Os Caminhos de aprendizado (LPs) agora podem definir regras adaptáveis que controlam quais seções e objetos de subaprendizado (sub LOs) estão visíveis para diferentes grupos de alunos, e a API pública reflete esse comportamento.

Os seguintes endpoints são afetados:

- GET /primeapi/v2/learningObjects?filter.loTypes=caminho de aprendizado
- GET /primeapi/v2/learningObjects/{loId}

Um novo atributo booleano, attributes.isAdaptive, indica que um programa de aprendizado usa regras adaptáveis. Quando esse sinalizador é true, o atributo sections é interpretado de forma adaptativa.

Para chamadas do aluno, apenas as seções visíveis para o aluno atual são retornadas. Cada seção inclui a lista de IDs de objetos de aprendizado (loIds), um sinalizador obrigatório e um mandatoryLOCount que são calculados com base na configuração adaptável para esse aluno, bem como o sectionId. A relação relationship.subLOs agora também é filtrada, portanto contém somente os objetos de sub-aprendizado visíveis para esse aluno.

Para chamadas de administrador, as seções também podem expor uma matriz adaptiveConfig. Isso descreve as regras adaptáveis por grupo de usuários, incluindo userGroupId, userGroupName e se a seção é obrigatória para esse grupo. As ferramentas voltadas para o administrador podem usar isso para visualizar e gerenciar regras adaptativas.

Redefinir conclusão de programas de aprendizado

A versão apresenta uma API para __atualizar (redefinir) a conclusão__ de objetos de aprendizado, incluindo programas de aprendizado adaptáveis. Isso suporta cenários como novo treinamento, atualizações periódicas de conformidade ou reinicializações de programas.

Um novo ponto de extremidade está disponível:

```
POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion
```

Essa operação requer permissões de gravação apropriadas e redefine o estado de conclusão para a instância do objeto de aprendizado especificada no contexto de usuário especificado. Ele deve ser usado por automações do lado do administrador ou ferramentas do aluno com escopo cuidadoso.

Uma versão em massa desse recurso é planejada por meio de uma API de trabalhos. A forma de solicitação é projetada para direcionar usuários por email, ID de usuário ou ID de grupo de usuários, por exemplo:

```
{  
  "emails": ["[user1@example.com](mailto:user1@example.com)", "[user2@example.com](mailto:user2@example.com)"],  
  "userIds": ["12345", "67890"],  
  "userGroupIds": ["ug1", "ug2"]  
}  
```

As integrações devem usar essa API quando precisarem reiniciar os alunos em cada programa ou curso. Os clientes devem tratar as respostas de erro normalmente: a API pode rejeitar solicitações de atualização, quando uma redefinição não é aplicável (por exemplo, quando não existe conclusão ou tipos de objeto de aprendizado sem suporte).

## Equivalentes e conclusões alternativas

Para suportar implementações em que vários objetos de aprendizado podem atender ao mesmo requisito, a versão introduz conclusões de equivalentes e alternativas como APIs públicas.

Os pontos de extremidade do Objeto de aprendizado agora contêm estas informações:

```
- GET /primeapi/v2/learningObjects
- GET /primeapi/v2/learningObjects/{loId}
```

Um novo atributo booleano attributes.isAlternateComplete indica se a conclusão do aluno para um determinado objeto de aprendizado é o resultado de um objeto de aprendizado alternativo ou equivalente em vez do próprio objeto. Quando isso é verdadeiro, a relação relationship.alternateCompletions lista os objetos de aprendizado que agiam como alternativas. Isso permite que relatórios e painéis de controle de downstream diferenciem conclusões diretas e alternativas e mostrem qual alternativa atendeu ao requisito.

Além disso, uma exibição de objetos de aprendizado relacionados permite a descoberta de alternativas potenciais que podem satisfazer um objeto de aprendizado. Isso é exposto por meio de:

```
GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}
```

A resposta retorna objetos de aprendizado que podem atuar como alternativas e inclui um campo meta.count que indica o número total dessas alternativas, independentemente do limite atual. As integrações podem usar isso para apresentar equivalentes recomendados ou para criar exibições administrativas de mapeamentos alternativos.

## Casos de uso do Reporting and analytics

Os usuários que geram relatórios ou análises devem atualizar sua lógica para adicionar isAlternateComplete e alternateCompletions em seus fluxos de trabalho de relatórios.

As integrações de relatórios que consomem dados de conclusão (por exemplo, exportação de LT, feeds de data warehouse personalizados ou painéis de BI) devem estender sua lógica para ler e persistir os atributos. isAlternateComplete e relationship.alternateCompletions das APIs do LO:

- Quando isAlternateComplete == false:\
  Trate o registro como uma __conclusão direta__ do OA, como hoje.
- Quando isAlternateComplete == true:
   - Sinalize o registro como uma __conclusão alternativa__ em seu relatório (por exemplo, uma coluna “Método de Conclusão” com valores DIRECT vs ALTERNATE).
   - Use relationship.alternateCompletions.data[*].id para capturar __qual(is) OA de origem__ concedeu essa conclusão (por exemplo, “Curso B concluído por meio do Curso A alternativo”).

Casos de uso típicos:

- _Relatórios de conformidade_ - mostram que um curso de conformidade foi concluído por meio de um equivalente aprovado e listam o curso de origem que atendeu ao requisito.
- _Painéis de progresso do programa_ - diferencie os alunos que concluíram um caminho _diretamente_ daqueles que o satisfizeram por meio de alternativas, para exibições mais precisas de progresso e correção.
- _Trilhas de auditoria_ - para qualquer LO marcado como isAlternateComplete=true, os auditores podem ver exatamente quais treinamentos alternativos foram usados para conceder essa conclusão.

Sem incorporar esses dois campos, os relatórios de downstream tratarão as conclusões alternativas como conclusões regulares e _não poderão explicar_ *por que* um aluno mostra como concluído um treinamento que nunca fez diretamente.

## Comportamento do aluno vs. da API do OA do administrador

A estrutura de ajuda de tarefa multilíngue é idêntica nas APIs do aluno e do administrador. O escopo do aluno retorna apenas as ajudas de tarefa visíveis para o aluno, mas para cada ajuda de tarefa visível ele expõe todas as localidades configuradas por meio de várias entidades de recurso (uma por localidade) e vários localidades localizedMetadata. O escopo do administrador retorna todas as ajudas de tarefa que o administrador pode gerenciar, com o mesmo modelo de OA e IDs de recurso específicas da localidade. Os clientes com escopo do aluno devem escolher o recurso cujos attributes.locale melhor correspondam ao idioma do conteúdo do aluno, enquanto as ferramentas de administrador podem enumerar todas as localidades para relatório e gerenciamento.

## Lista de verificação com recurso de comentários

Para oferecer suporte a fluxos de trabalho em que os revisores podem compartilhar feedback estruturado em atividades baseadas em listas de verificação, esta versão mostra *comentários de listas de verificação* e controles de visibilidade do revisor por meio da API de recurso do objeto de aprendizado.

Os metadados relacionados à lista de verificação são expostos nas entidades learningObjectResource (JApiLOResource, “type”: “learningObjectResource”) que representam recursos da lista de verificação em um curso ou outro objeto de aprendizado.

As informações estão disponíveis através de:

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

Quando a instância do objeto de aprendizado contém recursos do tipo lista de verificação, as entradas learningObjectResource correspondentes na matriz incluída expõem os atributos comment e reviewer-visibility em atributos em atributos e a identidade do revisor em relacionamentos.

### Novos atributos de comentário na lista de verificação

Para recursos de lista de verificação, os seguintes atributos podem estar presentes em learningObjectResource:

- attributes.checklistComment\
  Um comentário de texto livre deixado pelo revisor para o aluno, por exemplo:\
  “checklistComment”: “Excelente desempenho! Todos os protocolos de segurança foram seguidos corretamente.”\
  Este atributo foi populado _somente se_:
   - showChecklistComment é verdadeiro e
   - a configuração da lista de verificação tem enable_reviewer_remarks ativado.
- attributes.showChecklistComment\
  Um sinalizador Booleano que indica se as observações do revisor devem ser mostradas ao aluno:\
  “showChecklistComment”: true\
  Este atributo está presente _somente quando_ enable_reviewer_remarks está habilitado na configuração de lista de verificação.\
  Os clientes devem usar esse sinalizador para decidir se devem renderizar checklistComment nas experiências do aluno.
- attributes.showReviewerNameToLearner\
  Um sinalizador Booleano que controla se o aluno deve ver a identidade do revisor:\
  “showReviewerNameToLearner”: true\
  Quando verdadeiro, os clientes podem usar o relacionamento checklistReviewedBy (veja abaixo) para resolver e exibir o nome do revisor (por exemplo, por meio de uma API de pesquisa de usuário).

Outro contexto específico da lista de verificação, como checklistEvaluationStatus, isChecklistMandatory, resourceSubType: “CHECKLIST” e submissionDate também estão disponíveis no mesmo learningObjectResource para oferecer suporte a interfaces de usuário e relatórios de lista de verificação mais avançados.

### Relacionamento de identidade do revisor

Quando os nomes dos revisores devem ser visíveis, o learningObjectResource inclui um relacionamento que aponta para o usuário do revisor:

```
"relationships": {
  "checklistReviewedBy": {
    "data": {
      "id": "user_id",
      "type": "user"
    }
  }
}
```

Esta relação é populada _somente se_:

- showReviewerNameToLearner é verdadeiro e
- checklistReviewedBy não é nulo (por exemplo, a lista de verificação foi revisada).

Os aplicativos cliente devem:

1. Verifique attributes.showReviewerNameToLearner.
2. Se true e relationship.checklistReviewedBy.data estiverem presentes, chame a API de usuário apropriada para resolver “id”: “user_id” em um nome de exibição.
3. Processe o nome do revisor ao lado do comentário ou status da lista de verificação, conforme apropriado.

### Acessando recursos e comentários da lista de verificação

Para recuperar recursos de lista de verificação e seus comentários para um determinado objeto de aprendizado, os clientes devem:

- Chamada

```
GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources
```

- Na resposta:
   - Use relationship.instance do learningObject principal para localizar as entradas learningObjectInstance relevantes no incluído.
   - Em cada learningObjectInstance, siga relationship.loResources para localizar entradas de learningObjectResource.
   - Filtrar entradas learningObjectResource onde:
      - attributes.resourceSubType == “LISTA DE VERIFICAÇÃO” (para recursos de lista de verificação) e
      - opcionalmente attributes.showChecklistComment == true para localizar listas de verificação com comentários visíveis ao aluno.

- Para cada learningObjectResource da lista de verificação, consuma:
   - attributes.checklistComment (se presente e showChecklistComment for verdadeiro)
   - attributes.checklistEvaluationStatus (por exemplo, “APROVADO”)
   - attributes.showReviewerNameToLearner
   - relationship.checklistReviewedBy (quando presente) para identificar o revisor.

Esse padrão permite que clientes sem periféricos ou personalizados renderizem uma experiência abrangente de lista de verificação, incluindo status, sinalizadores obrigatórios/opcionais e feedback do revisor, diretamente das APIs do Prime.

### Considerações sobre emissão de relatórios e UX

- _Relatórios e análises_
As integrações que controlam o desempenho do aluno nas listas de verificação podem incorporar:
   - checklistEvaluationStatus para indicadores de aprovação/reprovação ou outros indicadores de status.
   - isChecklistMandatory para diferenciar as atividades de lista de verificação obrigatórias vs. opcionais.
   - Presença ou ausência de checklistComment e showChecklistComment para auditorias da cobertura de feedback.
- _Experiências do aluno_
As implementações de UI devem:
   - Respeite showChecklistComment antes de exibir comentários.
   - Use showReviewerNameToLearner e checklistReviewedBy para decidir se deseja exibir o nome do revisor ou manter a revisão anônima.
   - Volte normalmente quando os comentários estiverem desativados ou não estiverem presentes e ainda mostrem o status da avaliação e as informações de envio.

## Suporte multilíngue para ajuda de tarefa

Para oferecer suporte a implementações em que as ajudas de tarefa devem ser entregues em vários idiomas para alunos e administradores, esta versão estende a manipulação da ajuda de tarefa para retornar *um recurso por localidade* em vez de um único recurso en-US codificado.

As ajudas de tarefa em vários idiomas continuam a usar a hierarquia existente:

_Objeto de aprendizado_ (lo) → _learningObjectResource_ (loResource) → _recurso_

Nenhuma alteração é necessária no contrato de API. Qualquer ajuda de tarefa localizada se encaixa naturalmente nessa estrutura, com entidades de recurso separadas por localidade e metadados localizados compartilhados nos níveis learningObject/learningObjectResource.

Os dados de ajuda de tarefa são expostos por meio de:

```
GET /primeapi/v2/learningObjects/jobAid:{jobAidId}?include=instances.loResources.resources
```

Quando uma ajuda de tarefa tem várias variantes de idioma, a matriz incluída contém várias entradas “type”: “resource” — uma para cada localidade (por exemplo, en-US, fr-FR, es-ES), todas vinculadas a partir de um único learningObjectResource.

### Estrutura de ajuda de tarefa em vários idiomas

Uso de ajudas de tarefa em vários idiomas:

- _learningObject (type: learningObject)_
   - Contém metadados localizados com várias entradas (por exemplo, en-US, fr-FR) para que os clientes possam apresentar o título/descrição da ajuda de tarefa no idioma apropriado.
- _learningObjectInstance (tipo: learningObjectInstance)_
   - Refere-se a uma ou mais entradas learningObjectResource por meio de relationship.loResources.
- _learningObjectResource (tipo: learningObjectResource)_
   - Contém a configuração comum (tipo de conteúdo, versão etc.) e vários locais localizedMetadata.
   - Links para uma ou mais entidades de recurso via relationship.resources.
- _recurso (tipo: recurso)_
   - *Um por localidade*, cada uma com sua própria id, localidade, nome e URL (location/downloadUrl).

Para uma ajuda de tarefa em vários idiomas, um padrão típico é:

- learningObjectResource com localizedMetadata para en-US e fr-FR
- relationship.resources.data apontando para:
   - recurso com localidade: “en-US”
   - recurso com localidade: “fr-FR”

Os clientes podem selecionar o recurso apropriado fazendo a correspondência da localidade do aluno com o campo resource.attributes.locale.

### Novo formato de ID de recurso para ajudas de tarefa

Para diferenciar corretamente várias variantes localizadas de um recurso de ajuda de tarefa, o _formato da ID de recurso foi alterado_.

_Formato de ID de recurso antigo (herdado)_

Anteriormente, os recursos de ajuda de tarefa usavam um formato de ID opaco, como:

jobAid:131032_-1_-1_2_resource

Esse formato não codificava a localidade, e as APIs apresentavam efetivamente apenas um único recurso (geralmente en-US).

_Novo formato de ID de recurso (com reconhecimento de vários idiomas)_

O novo formato é:

```
jobAid:<jobAidId>_<version>_<localeCode>
```

Exemplos:

- jobAid:131032_2_en-US
- jobAid:131032_2_fr_FR
- jobAid:131032_2_es_ES

Discriminação visual:

```
jobAid:131032_2_fr_FR

        │      │ │ │

        │      │ │ └──► Locale Code (fr_FR, en_US, es_ES, etc.)

        │      │ └────► Version (2)

        │      └──────► JobAid ID (131032)

        └─────────────► Resource Type Prefix ("jobAid:")
```

Essa estrutura permite aos clientes:

- Identifique rapidamente a qual ajuda de tarefa e versão um recurso pertence.
- Inferir diretamente a localidade a partir da ID do recurso quando necessário.

### Compatibilidade com versões anteriores: 

```/resources/{resourceId}```

O ponto de extremidade do recurso herdado permanece disponível:

```GET /primeapi/v2/resources/{resourceId}

```

Agora, ele é _compatível com versões anteriores_ com os formatos de ID antigo e novo:

- _Formato de ID antiga_ (por exemplo, jobAid:131032_-1_-1_2_resource)
   - Continua a trabalhar.
   - Retorna o _primeiro recurso criado_ associado a esse identificador herdado (geralmente o recurso en-US original).
- _Novo formato de ID_ (por exemplo, jobAid:131032_2_fr_FR)
   - Retorna o _recurso específico de localidade exato_ correspondente a essa ID.
   - Isso permite a recuperação e a manipulação precisas de variantes localizadas de ajuda de tarefa.

Integrações que atualmente armazenam ou fazem referência às IDs de recurso antigas podem continuar a funcionar sem alteração, enquanto implementações mais recentes são incentivadas a adotar o novo formato de ID para operações específicas da localidade.

### Considerações sobre integração e UX

- _Interface do usuário do aluno/administrador_
   - Use learningObject.localizedMetadata e learningObjectResource.localizedMetadata para apresentar títulos e descrições no idioma apropriado.
   - Use resource.attributes.locale para selecionar o URL correto (local / downloadUrl) para a localidade do aluno.
   - Implementar comportamento de fallback (por exemplo, fallback para pt-BR) se o local exato de um aluno não estiver disponível.
- _APIs e armazenamento_
   - Para novas integrações, armazene as _IDs de recurso de novo formato_ (```jobAid:<jobAidId>_<version>_<localeCode>```) para habilitar a recuperação específica de localidade sem ambiguidade.
   - As IDs herdadas ainda podem ser usadas com /resources/{resourceId}, mas elas não farão distinção entre localidades.

## Restrições de timeslot para iniciar módulos

Algumas experiências de aprendizado devem estar disponíveis somente dentro de uma janela de tempo definida. A versão exibe informações de intervalo de tempo nos recursos do objeto de aprendizado e introduz um ponto de extremidade de validação que verifica se um aluno pode iniciar um recurso no tempo atual.

Os metadados de intervalo de tempo estão disponíveis no endpoint:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

No nível de recurso do objeto de aprendizado, um objeto timeSlot agora pode estar presente nos atributos, com valores startTime e endTime em UTC. Especifica a janela durante a qual o recurso pode ser iniciado.

Antes de iniciar um módulo, as integrações podem chamar um novo ponto de extremidade de validação:

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

Esse ponto de extremidade, destinado a cenários lidos pelo aluno, retorna se o aluno tem permissão atualmente para iniciar o recurso, considerando o intervalo de tempo configurado, o tipo de entrega e outras regras de back-end.

Os players personalizados e aplicativos clientes devem usar canStart para impor o acesso baseado em tempo e usar os metadados timeSlot para exibir mensagens claras sobre quando o conteúdo se torna disponível ou expira. As respostas negativas de canStart devem ser tratadas explicitamente para informar aos alunos por que o conteúdo não pode ser iniciado ainda ou mais.

## Quizzes de várias tentativas orientados por conteúdo

Alguns pacotes de conteúdo implementam seu próprio rastreamento de tentativas em vez de depender exclusivamente da Adobe Learning Manager. A versão introduz um sinalizador que indica quando as tentativas são orientadas pelo próprio conteúdo.

Até:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```

os recursos do objeto de aprendizado agora podem expor um atributo booleano hasContentDrivenAttemptTracking. Quando isso é verdadeiro, o quiz ou o módulo gerencia as tentativas internamente (por exemplo, por meio do SCORM ou da lógica da xAPI), e os contadores de tentativas padrão da plataforma podem não refletir totalmente a experiência do aluno.

As integrações que exibem contagens de tentativas ou controlam o comportamento da repetição devem marcar esse sinalizador. Quando ativada, elas não devem inferir os limites de tentativa apenas a partir dos metadados da plataforma e devem estar preparadas para confiar nos relatórios do lado do conteúdo (por exemplo, por meio de instruções da xAPI) ou em regras específicas dos negócios.

## Alteração de comportamento no formato da ID de recurso da ajuda de tarefa

Esta versão apresenta uma importante __alteração comportamental__ no formato de IDs de recursos de Ajuda de tarefa. Embora nenhum novo ponto de extremidade esteja envolvido, isso tem um impacto direto nos sistemas que armazenam ou analisam essas IDs.

Anteriormente, as IDs de recurso de ajuda de tarefa usavam um formato como:

```jobAid:<jobAidId>_-1_-1_2_resource```

Na versão de abril de 2026, esse texto foi substituído por um formato simplificado e mais explícito:

```jobAid:<jobAidId>_<version>_<localeCode>```

Por exemplo:

jobAid:131032_2_fr_FR

Os componentes são:

- ```<jobAidId>```: a ID numérica da Ajuda de Trabalho (por exemplo, 131032),
- ```<version>```: o número de versão da Ajuda de Trabalho (por exemplo, 2),
- ```<localeCode>```: o código de localidade (por exemplo, en_US, fr_FR, es_ES).

Qualquer integração que indexe recursos ou persista em IDs de recurso de ajuda de tarefa deve atualizar sua lógica de análise e armazenamento para reconhecer o novo formato. Como os próprios identificadores são alterados, é altamente recomendável reconstruir todos os índices locais chaveados por IDs de recurso de ajuda de tarefa após atualizar para a versão de abril de 2026.

## Definir imagens de banner do curso por migração

Agora você pode definir ou atualizar imagens de banner do curso no Adobe Learning Manager como parte do fluxo de trabalho de migração padrão. Isso ajuda a iniciar ou limpar grandes catálogos, mantendo as páginas do curso visualmente consistentes, sem editar manualmente

### Onde as imagens do banner são definidas

As imagens de banner são configuradas no arquivo de migração do _course.csv_, que você já usa para fornecer metadados do curso, como:

- id de catálogo padrão
- courseName
- courseCreationDate
- estado
- autor
- thumbnailUrl

Com esse aprimoramento, a especificação course.csv inclui uma _coluna opcional_ adicional para a imagem de banner do curso. O nome exato do cabeçalho é definido na especificação do CSV baixada da sua conta do Learning Manager (por exemplo, ele pode aparecer como bannerUrl ou bannerImageUrl).

A coluna do banner:

- Aponta para o arquivo de imagem que você deseja usar como _banner do curso_.
- Funciona da mesma forma que o thumbnailUrl, usando imagens disponíveis no repositório de conteúdo configurado (Box/FTP).

### Preparação de imagens de banner para migração

1. Carregar imagens de banner: coloque os arquivos de imagem do banner no mesmo local do Box ou do FTP que você usa para outros ativos de migração, seguindo a estrutura de diretório existente.
2. Verificar formato do arquivo:
Use um dos formatos de imagem compatíveis (por exemplo, png, jpg, jpeg, gif), conforme descrito nos requisitos de sistema:
   1. [*Requisitos do sistema*](/help/migrated/system-requirements.md)
3. Atualizar course.csv: na nova coluna do banner, faça referência ao caminho relativo ou identificador da imagem do banner. Um exemplo conceitual:

```
id,courseName,courseCreationDate,state,author,thumbnailUrl,bannerUrl  
12345,DEMO1,2018-05-05T08:56:21.000Z,Published,Sudheer,pic1.png,banners/banner1.png  
45678,DEMO2,2018-05-05T08:56:21.000Z,Published,Sudheer,pic2.png,banners/banner2.png  
```

### Aplicar banners durante a execução da migração

Depois que seu course.csv é atualizado, o fluxo é o mesmo de qualquer outra migração:

1. _Carregar CSVs_
Carregue o course.csv atualizado (e outros arquivos relevantes) na pasta do Box/FTP configurada para migração. Os nomes de arquivos devem corresponder exatamente aos nomes especificados em csv_specifications.zip (eles diferenciam maiúsculas de minúsculas).
2. _Iniciar uma execução de sprint_
No Adobe Learning Manager, como administrador de integração, inicie uma migração _execução do sprint_ que inclui course.csv.\
   O mecanismo de migração lê a coluna do banner e aplica a imagem do banner a cada curso.
3. _Examinar resultados e logs de erro_
Depois do sprint:
   1. Verifique os banners nos aplicativos _Autor_ e _Aluno_.
   2. Se algumas linhas falharem (por exemplo, devido a um caminho de arquivo inválido ou um formato não compatível), baixe o CSV de erro na execução da migração e corrija os dados.

### Novos cursos vs. cursos existentes

O campo do banner funciona em ambos os cenários:

- _Novos cursos criados por migração_
Quando um curso é criado pela primeira vez em course.csv e a coluna de banner é preenchida, esse banner é definido imediatamente.
- _Cursos existentes (aprimoramento/correções)_
Se você executar novamente a migração com a mesma ID do curso e um novo valor de banner:
   - O Learning Manager localiza o curso existente.
   - A imagem do banner está _atualizada_ para a nova imagem especificada no CSV.

Os nomes e caminhos das colunas reais devem corresponder à _especificação de CSV baixada_ e ao layout do repositório de conteúdo.

## Remover coluna de ordem em LearningProgramCourse

O Adobe Learning Manager agora oferece suporte a um modelo simplificado de _solicitação de cursos nos Caminhos de Aprendizado (Programas de Aprendizado)_ durante a migração. Como parte dessa alteração, a _coluna de ordem é removida_ do arquivo de migração learning_program_course.csv.

Anteriormente, o arquivo learning_program_course.csv incluía uma coluna (geralmente chamada de ordem ou semelhante) usada para:

- Defina explicitamente a _posição_ de cada curso dentro de um Programa de Aprendizado, com base no valor numérico dessa coluna.
- Exigir que administradores ou scripts mantenham essa sequência numérica manualmente, especialmente ao inserir ou reordenar cursos.

Agora, o Adobe Learning Manager não usa mais a coluna de ordem em learning_program_course.csv para determinar a ordem dos cursos. Em vez disso, o CSV de migração se concentra em _quais cursos pertencem a qual programa de aprendizado_, em vez de como eles são ordenados numericamente.

## Impacto nos CSVs de migração

### learning_program_course.csv

Você deve tratar a coluna de ordem herdada como removida ou ignorada:

- Não confie na ordem para controlar a sequência de cursos em um Programa de aprendizado durante a migração.
- Se você ainda tiver uma coluna de ordem de modelos mais antigos:
   - O Learning Manager o ignorará para pedidos.
   - É possível removê-lo com segurança do CSV ao longo do tempo para simplificar os arquivos de migração.
- O mapeamento necessário do núcleo permanece:
   - ID do programa de aprendizado ↔ ID do curso (e quaisquer outras colunas ainda documentadas, como ID, learningProgramId, courseId e datas).

Sempre consulte as [_especificações do CSV_](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual) mais recentes da sua conta do Learning Manager (via csv_specifications.zip) para confirmar o conjunto de cabeçalhos e os requisitos atuais.

## timeZoneCode em instâncias de curso

A partir desta versão, o modelo Instância do curso (learningObjectInstance) expõe um novo atributo:

timeZoneCode — um campo de string que vincula explicitamente uma instância do curso a um dos fusos horários configurados da conta.

Isso permite que os clientes:

- Resolva o fuso horário de uma instância do curso de maneira consistente e orientada por API.
- Interprete e exiba todas as datas/horas no nível da instância corretamente para essa instância, independentemente do fuso horário do próprio usuário.

### Onde timeZoneCode aparece

O campo é adicionado aos atributos do modelo learningObjectInstance
somente para instâncias do curso.

Exemplo:

```
{
  "id": "course:1262748_1359228",
  "type": "learningObjectInstance",
  "attributes": {
    "dateCreated": "2019-08-06T13:50:39.000Z",
    "isAET": false,
    "isDefault": true,
    "timeZoneCode": "356",
    "isFlexible": false,
    "state": "Active",
    "localizedMetadata": [
      {
        "locale": "en-US",
        "name": "Default instance"
      }
    ]
  }
}
```

### Como resolver timeZoneCode

O timeZoneCode numérico é uma chave de pesquisa no catálogo de fuso horário da conta, que é exposta pela API Account:

```http
GET /primeapi/v2/account
Authorization: Bearer <access_token>
```

Na resposta, os fusos horários estão listados em:

```
"data": {
  "attributes": {
    "timeZones": [
      {
        "name": "Etc/GMT+12",
        "timeZoneCode": "356",
        "utcOffset": -720,
        "utcOffsetCode": "UTC-12:00(Etc/GMT+12)",
        "zoneId": "Etc/GMT+12"
      },
      "..."
    ]
  }
}
```

### Fluxo de cliente recomendado:

1. Chame GET /account uma vez, cache attributes.timeZones para o locatário.
2. Para cada instância do curso:
   - Leia attributes.timeZoneCode.
   - Localize a entrada correspondente em timeZones onde timeZoneCode corresponde.
   - Use zoneId, utcOffset e utcOffsetCode da entrada para exibição e lógica de agendamento.

## APIs públicas assíncronas para associação a grupo de usuários

### Introdução

O Adobe Learning Manager expõe duas _APIs assíncronas de administrador_ para gerenciar a associação de grupo de usuários (UG):

- POST /async/userGroups/{userGroupId}/users - adicionar usuários a um UG de forma assíncrona
- DELETE /async/userGroups/{userGroupId}/users - remove usuários de um UG de forma assíncrona

Em vez de atualizar a associação na mesma solicitação, essas APIs aceitam seu lote e retornam uma _ID de evento_. O resultado real é fornecido posteriormente por meio de webhooks.

Use-os quando:

- Você está gerenciando grupos grandes ou atualizações em lote frequentes.
- A latência é menos importante do que a confiabilidade e o throughput.
- Você está criando integrações (HR, CRM, LXP) em vez de cliques na interface do usuário.

Para ações administrativas pequenas e interativas, você pode continuar usando as APIs síncronas `/userGroups/{id}/users`.

### Autenticação e URL base

Estas APIs fazem parte da superfície padrão __API de Administração v2__.

- [URL base (prod)](https://learningmanager.adobe.com/docs/primeapi/v2/)
- Autenticação: Token de acesso OAuth 2.0 com escopo `admin:write`
- Cabeçalhos obrigatórios:
   - Autorização: Portador &lt;access_token>
   - Content-Type: application/json
   - Aceitar: application/json

Para o comportamento e os escopos gerais da API de administração, consulte:

- [Manual do desenvolvedor](/help/migrated/integration-admin/feature-summary/developer-manual.md)
- [Guia de referência da API](https://learningmanager.adobe.com/docs/primeapi/v2/)

### Formato de solicitação

__adicionar__ e __remover__ usam exatamente a mesma forma de corpo.

#### Corpo

```
{
  "metadata": {
    "event_id": "my-optional-correlation-id",
    "sourceSystem": "HRIS",
    "batchId": "hr_2026_03_30_0001"
  },
  "data": [
    { "type": "user", "id": "11101219" },
    { "type": "user", "id": "11101220" }
  ]
}
```

#### dados (obrigatório)

dados é a lista de identificadores de recursos do usuário para este lote.

- `type` deve ser “user”.
- `id` é a _ID numérica do usuário_ no ALM (não email, não UUID).

#### Restrições

- `data` deve estar presente e não vazio.
- Pelo menos um usuário é necessário.
- O tamanho máximo da carga é de 20 usuários por solicitação.
- Todas as IDs devem ser numéricas e fazer referência a usuários válidos.

Se qualquer uma dessas condições falhar, a API retornará um erro e nada será colocado em fila.

#### metadados (opcional)

`metadata` é qualquer dado de correlação adicional que você deseja que seja repetido no Webhook.

Uso típico:

- `event_id` - ID de correlação gerada.
- `sourceSystem` - nome do sistema upstream.
- `batchId` - identificadores de lote ou trabalho.

O serviço retorna este objeto inalterado na resposta do Webhook, para que você possa corresponder o retorno de chamada ao seu trabalho interno.

Restrições:

- Opcional; pode ser omitida totalmente.
- O comprimento combinado de todas as chaves e valores não deve exceder 1.000 caracteres.

### Formato da resposta

Os dois pontos de extremidade respondem de forma síncrona com uma ID de evento:

```
{ "event_id": "cd2972c8-cb15-47a0-a23f-e4a16cb720f5" }
```

Comportamento:

- Se `metadata.event_id` for passado, esse valor será usado.
- Caso contrário, o serviço gera um UUID.

Você deve sempre:

- Armazene `event_id` como o identificador primário do lote.
- Espera-se receber o mesmo valor no retorno de chamada do Webhook.

Exiba [Webhooks para adicionar e remover a associação de grupo de usuários](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-adding-and-removing-user-group-membership) para obter mais informações.

## Perguntas frequentes

_Como a versão de abril de 2026 altera a API learningObjects para programas de aprendizado adaptáveis?_

Esta versão adiciona um sinalizador isAdaptive nos programas de aprendizado e torna as seções e sub-LOs sensíveis ao aluno. Nos programas adaptáveis, os alunos veem apenas as seções e os objetos de subaprendizado que estão visíveis a eles com base em regras adaptáveis, enquanto os administradores podem ver a configuração adaptável subjacente de um grupo de usuários.

_Preciso atualizar minha integração se ela considerar que todas as seções e sub-LOs sempre são retornados?_

Sim Para programas de aprendizado adaptáveis, a API agora retorna apenas as seções e sub LOs que estão visíveis para o aluno atual. O código do cliente deve tratar a resposta como a exibição autoritativa e possivelmente filtrada, em vez de assumir uma lista completa.

_Como redefinir programaticamente a conclusão de um aluno para um curso ou programa de aprendizado?_

Usar o novo ponto de extremidade:

```POST /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/refreshCompletion```
Isso redefine a conclusão da instância de destino quando as permissões e o estado permitirem.

_Como saber se um aluno concluiu algo por meio de um objeto de aprendizado alternativo ou equivalente?_

Verifique o atributo isAlternateComplete no objeto de aprendizado. Se for verdadeiro, o relacionamento alternateCompletions lista os objetos de aprendizado que agiam como alternativas para a conclusão desse aluno.

_Como posso encontrar todas as alternativas que podem satisfazer um determinado objeto de aprendizado?_

Use o seguinte ponto de extremidade:

```GET /primeapi/v2/learningObjects/{loId}/relatedLOs?type=sourceAlternateLOs&limit={n}```

e use a matriz de dados (para as alternativas) e meta.count (para o número total de alternativas).

_Como saber se um aluno tem permissão para iniciar um módulo neste momento?_

Primeiro, busque o timeSlot do recurso de:

```GET /primeapi/v2/learningObjects/{loId}?include=instances.loResources```
e use:

```GET /primeapi/v2/learningObjects/{loId}/instances/{loInstanceId}/loResources/{loResourceId}/canStart```

_O que significa ContentDrivenAttemptTracking em um recurso?_

Indica que o controle de tentativas é controlado pelo próprio conteúdo (por exemplo, por meio da lógica SCORM/xAPI) e não apenas por contadores de plataforma. Quando for verdade, não confie apenas nas contagens ou limites de tentativas de plataforma para sua UX e relatórios.

_Como obter menus apropriados para usuários não conectados (experiências públicas)?_

Usar:

```GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true```

Isso retorna estruturas de menu e página filtradas para usuários anônimos, adequadas para o Experience Builder ou outros sites sem periféricos.

_O que mudou na filtragem da Ajuda de tarefa com effectiveModifiedDate?_

As solicitações que combinam filter.effectiveModifiedDate com filter.loTypes=jobAid agora retornam corretamente apenas ajudas de tarefa na janela de data especificada.

_O que mudou no formato de ID de recurso de Ajuda de Trabalho e como devo lidar com isso?_

O formato da ID mudou de valores como:

```jobAid:<jobAidId>_-1_-1_2_resource```

até:

```jobAid:<jobAidId>_<version>_<localeCode>```

por exemplo jobAid:131032_2_fr_FR. Qualquer sistema que armazena ou analisa IDs de recursos de ajuda de tarefa deve ser atualizado, e você deve planejar recriar índices locais chaveados por esses IDs após atualizar para a versão de abril de 2026.
