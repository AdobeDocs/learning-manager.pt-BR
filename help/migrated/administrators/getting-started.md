---
description: Este documento fornece uma abordagem recomendada para as organizações instalarem e configurarem o Adobe Learning Manager. A equipe do Learning Manager sugere uma abordagem em fases para começar a usar o aplicativo. Não é obrigatório que você siga todas as fases em uma sequência específica.
jcr-language: en_us
title: Guia de práticas recomendadas para configurar o Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3387'
ht-degree: 0%

---



# Guia de práticas recomendadas para configurar o Learning Manager

Este documento fornece uma abordagem recomendada para as organizações instalarem e configurarem o Adobe Learning Manager. A equipe do Learning Manager sugere uma abordagem em fases para começar a usar o aplicativo. Não é obrigatório que você siga todas as fases em uma sequência específica.

Essas fases podem ser executadas por três funções diferentes e por um ou mais indivíduos com base na configuração da sua organização. As três funções são as seguintes:

1. **Administrador de TI** - O administrador de TI executa atividades relacionadas à ativação ou integração associadas ao aplicativo Learning Manager em uma organização. O administrador de TI também pode adicionar um ou vários usuários e desempenhar uma função de administrador de integração.
1. **Autor** - O autor cria conteúdo de aprendizado necessário para os requisitos de aprendizado da organização. O autor de conteúdo de treinamento ou aprendizado da sua organização pode começar a criar o conteúdo básico necessário para o aplicativo Learning Manager.
1. **Administrador do Learning Manager** - O administrador do aplicativo Learning Manager realiza atividades de instalação e configuração. Em algumas empresas, o administrador de TI também pode desempenhar o papel de administrador do aplicativo Learning Manager.

Você pode percorrer o infográfico fornecido abaixo para obter uma visão geral das fases e tarefas correspondentes.

![](assets/learning-manager-getting-started.jpg)

Nesta etapa, presumimos que sua organização já recebeu a chave de licença e você ativou a conta do Learning Manager. Como mencionado no infográfico, as três faixas são explicadas da seguinte forma:

## Fase 1 - Configuração técnica (administrador de TI) {#phase1technicalsetupitadministrator}

Na faixa 1, o administrador de TI da sua empresa pode mudar para a função de administrador de integração no aplicativo Learning Manager e executar algumas ativações e integrações da seguinte maneira:

### Ativar/Adicionar campos ativos (Administrador do Learning Manager) {#enableaddactivefieldscaptivateprimeadministrator}

Além dos campos ativos fornecidos pelos usuários durante o registro, o administrador pode adicionar mais campos ativos. O administrador também pode ativar/desativar os campos do usuário. Os valores desses campos ativos são gerados a partir dos metadados de várias fontes de dados associadas às contas de usuário. Consulte [Ajuda de Campos Ativos](feature-summary/add-users-user-groups.md#active-fields) para obter mais informações.

### Logon único (SSO) {#singlesignonsso}

Você pode acessar o aplicativo Learning Manager usando a Adobe ID ou usando o logon único. O Single Sign-On é um mecanismo que permite que um usuário autentique uma vez e obtenha acesso a vários aplicativos várias vezes. Essa configuração não é obrigatória para a organização. Se sua organização tiver um provedor de SSO com base no SAML 2.0, você pode usá-lo para configurar o aplicativo Learning Manager. A configuração é necessária na empresa e no aplicativo Learning Manager. Se você optar por usar o SSO, entre em contato com o suporte de Adobe para receber as instruções de configuração. Consulte [Ajuda de configurações](feature-summary/settings.md) para obter mais informações.

### Importação em massa de usuários {#bulkimportofusers}

Quando você tem um grande volume de usuários em sua organização, pode importar todos os usuários em massa para o aplicativo Learning Manager usando um arquivo .CSV. Antes de realizar essa tarefa, sugerimos que você exporte a lista de usuários do aplicativo de RH da sua organização em um formato CSV. Mesmo que você não importe os usuários em massa nesse estágio, você pode se familiarizar com o formato CSV. Para começar com o processo de importação no Learning Manager, carregue o arquivo .CSV e mapeie os campos de dados do aplicativo com as colunas CSV da sua organização. Consulte [Ajuda para importação em massa](add-users-in-bulk.md) para obter mais informações.

### Integração do conector FTP {#ftpconnectorintegration}

Se você enfrentar a adição ou remoção contínua de funcionários em sua organização, poderá optar por automatizar a importação em massa de usuários usando o conector FTP. Primeiro, é necessário estabelecer uma conexão, depois carregar um CSV e mapear os atributos do CSV com os campos correspondentes do Learning Manager. Você pode agendar o processo de importação automática e também sincronizá-lo como e quando necessário. Consulte [Ajuda do conector FTP](../integration-admin/feature-summary/connectors.md#ftpconnector) para obter mais informações.

### Integração do conector do Salesforce {#salesforceconnectorintegration}

Se você tiver uma conta do Salesforce em sua organização, poderá automatizar o processo de importação de todos os usuários do Salesforce para o aplicativo Learning Manager. Se quiser usar esse recurso, você pode usar o conector do Salesforce para integrar o Learning Manager com a conta do Salesforce e automatizar a sincronização de dados. Use o recurso de agendamento automático para executar a importação automatizada de usuários regularmente. Você também pode executar a sincronização diariamente. Consulte [Ajuda do conector do Salesforce](../integration-admin/feature-summary/connectors.md#sfconnector) para obter mais informações.

### Integração com o Adobe Connect {#adobeconnectintegration}

Se estiver usando o Adobe Connect em sua organização, poderá integrá-lo ao aplicativo Adobe Learning Manager para fornecer uma experiência de usuário perfeita aos alunos. A integração permite que os alunos acessem salas de aula virtuais diretamente no aplicativo Learning Manager com um único clique, sem precisar fazer logon no Adobe Connect novamente. Com esse recurso, os alunos também podem consumir as sessões gravadas da sala de aula virtual no aplicativo Learning Manager. Para integrar, integre as configurações primeiro. Uso **Configurações > Adobe Connect > Configurar agora** para fornecer o URL do Connect e as credenciais de logon e integrar. Consulte [Ajuda de integração do Adobe Connect](feature-summary/adobeconnect-integration.md) para obter mais informações.

### Registro do aplicativo Salesforce {#salesforceappregistration}

Os alunos corporativos podem ter uma experiência perfeita de acesso ao aplicativo Learning Manager diretamente em suas contas do Salesforce. Os alunos podem acessar o conteúdo de aprendizado atribuído, como cursos, programas de aprendizado e ajudas de tarefa no aplicativo Salesforce. Os usuários também podem acessar notificações e comunicados do aplicativo Learning Manager no Salesforce. Para usar essa funcionalidade, você deve registrar o aplicativo em destaque do Salesforce no aplicativo Learning Manager. Consulte [Ajuda do aplicativo Salesforce](../integration-admin/feature-summary/sfdc-app.md) para saber mais sobre as instruções de instalação e uso.

## Fase 2 - Configuração do site (Administrador do Learning Manager) {#phase2siteconfigurationcaptivateprimeadministrator}

O administrador do aplicativo Learning Manager em sua organização precisa configurar ou configurar alguns dos recursos antes de começar a implementá-los para seus alunos.

### Marca {#branding}

Uma organização pode desejar exibir o logotipo da empresa no aplicativo Learning Manager, ter seu próprio domínio no URL, exibir o nome da organização e exibir esquemas de cores que correspondam à marca de uma organização. O Learning Manager permite que as organizações usem todos esses recursos. Se quiser personalizar as configurações e usar sua própria marca, clique na seção Marcas no painel esquerdo. Clique em Editar ao lado de todas essas opções e personalize de acordo com suas necessidades. Consulte [Ajuda sobre temas e marcas](feature-summary/themes.md) para obter mais informações.

### Adicionar usuários/grupos de usuários {#addusersusergroups}

Como os alunos são os principais usuários do conteúdo de aprendizado, a adição de usuários no sistema de gerenciamento de aprendizado é a etapa principal. Adicione usuários ao aplicativo Learning Manager e atribua funções a eles. É possível adicionar usuários das seguintes maneiras:

#### Adicionar usuários (internos) {#addusersinternal}

* **Como usuário único** - Adicionar usuários únicos ao aplicativo Learning Manager permite que você experimente com alguns dos usuários antes de adicioná-los em massa. Além disso, essa opção é útil quando você deseja adicionar mais usuários únicos com base na necessidade, após a importação em massa de usuários.
* **Autorregistro** - Essa opção permite que os administradores registrem seus funcionários no Learning Manager.
* **Importação em massa** (usando carregamento de CSV) - usando essa opção, você pode importar usuários em massa para o aplicativo Learning Manager. Como pré-requisito, você deve manter a lista de usuários pronta no formato CSV antes de usar esse recurso.

#### Adicionar usuários (perfis externos) {#addusersexternalprofiles}

* Por meio de inscrição externa - usando essa opção, você pode inscrever membros de departamentos externos ou funcionários externos da sua organização no aplicativo.

#### Adicionar grupos de usuários {#addusergroups}

O aplicativo Learning Manager gera grupos de usuários padrão com base em atributos semelhantes. Além dos grupos padrão, você pode gerar grupos de usuários personalizados com base em parâmetros, como designação e local, para que você possa utilizar esses grupos na gamificação e relatórios entre outros. Consulte [Ajuda para adicionar usuários](feature-summary/add-users-user-groups.md) para obter mais informações.

### Atribuir funções {#assignroles}

Depois que os usuários são adicionados ao Learning Manager, o administrador pode começar a atribuir funções de autor, administrador ou administrador de integração aos usuários de acordo com os requisitos da organização. Para atribuir funções a usuários, no logon do administrador, você pode clicar em **[!UICONTROL Usuários]**  no painel esquerdo, marque a caixa de seleção em relação a cada nome de usuário e clique em **[!UICONTROL Ações]** para escolher a função que deseja atribuir. As funções de gerente são atribuídas aos usuários pelo Adobe Learning Manager com base nas funções/privilégios mencionados pela sua organização no arquivo CSV. Você também pode alterar as funções dos usuários como Gerentes usando o fluxo de trabalho Editar usuários. Consulte [Ajuda para adicionar usuários](feature-summary/add-users-user-groups.md) para obter mais informações.

### Modelos de notificação {#notificationtemplates}

As notificações podem ser úteis para que os usuários em um sistema de gerenciamento de aprendizado saibam seu status ou sejam informados sobre os eventos/atividades. Ao criar cursos, configurar os recursos ou ao realizar cursos, os usuários passam por vários eventos que acionam notificações para os alunos, seus gerentes, administradores ou autores. O Learning Manager fornece vários modelos de notificação por e-mail no aplicativo. Como administrador, você pode personalizá-los de acordo com os requisitos da sua organização. Para criar notificações por e-mail, escolha **Modelos de e-mail** no painel esquerdo e clique no nome do modelo. Consulte [Ajuda de modelos de e-mail](feature-summary/email-templates.md) para obter mais informações

**Desativar notificações por email (recomendado)**

Por padrão, as notificações estão ativadas no aplicativo Learning Manager. Você pode desativar as notificações neste estágio se não quiser notificar os funcionários da sua organização.

### Medalhas {#badges}

As medalhas são um medidor de desempenho que o funcionário pode ganhar ao concluir um curso. Profissionais no mundo inteiro usam essas medalhas como representação de uma habilidade em particular ou do resultado do aprendizado. Você pode criar uma coleção de medalhas para que possa atribuí-las aos alunos após a conclusão do conteúdo de aprendizado. Para começar a criar medalhas, clique em **[!UICONTROL Medalhas]** no painel esquerdo. Consulte  [Ajuda de medalhas](feature-summary/badges.md) para obter mais informações.

### Feedback {#feedback}

O feedback é um dos fatores importantes de um LMS para medir o progresso da aprendizagem dos alunos e garantir a qualidade do conteúdo de aprendizagem. O Learning Manager fornece dois tipos de opções de feedback aos usuários.

* O feedback N1 é o feedback dado pelos alunos após concluírem o curso.
* O feedback N3 é o feedback dado pelos gerentes aos alunos com base no impacto do curso no comportamento dos alunos e nas atividades diárias.

É opcional as organizações usarem esse recurso. Os administradores podem personalizar os modelos de feedback de acordo com os requisitos da sua organização. Para usar esse recurso, o administrador precisa ativar as opções de feedback N1 e N3 no nível da instância do curso. Para configurar o feedback, escolha qualquer curso, clique em Padrões de instância no painel esquerdo e ative a opção de feedback. Consulte [Ajuda de feedback](feature-summary/courses.md) para obter mais informações.

### Gamificação {#gamification}

Manter os alunos envolvidos enquanto eles consomem o conteúdo é um dos desafios enfrentados pelas organizações. A gamificação aumenta a taxa de conclusão do curso ao envolver e motivar os alunos a atingir seus objetivos, com técnicas de jogos. Os alunos podem competir com seus colegas para marcar pontos em várias atividades de aprendizado e obter os níveis bronze, prata, ouro e platina. Os administradores podem ativar/desativar cada tarefa de gamificação e modificar a alocação de pontos para tarefas. O Learning Manager fornece o recurso Gamificação com algumas configurações padrão. Você pode começar a usar o recurso com as configurações padrão por algum tempo e optar por personalizar. É opcional configurar/alterar as configurações desse recurso. Se você tiver um especialista no assunto em sua organização, recomendamos que você defina as configurações antes de usá-las. Consulte [Ajuda de gamificação](feature-summary/gamification.md) para obter mais informações.

### Criar objetos de aprendizado {#createlearningobjects}

Esse é o estágio lógico em que todas as três faixas (faixa 1, faixa 2 e faixa 3) convergem para que você realize o próximo curso de ação.

Nesse ponto, depois de criar módulos e cursos, você pode começar a criar objetos de aprendizado de nível superior, como certificações, programas de aprendizado ou ajudas de tarefa para continuar. Antes de começar a criar objetos de aprendizado, verifique se você já adicionou alguns usuários no aplicativo Learning Manager e criou alguns módulos e cursos.

#### Criar certificações {#createcertifications}

A certificação é uma prova da conclusão de um conteúdo de aprendizado ou uma prova de realização para os alunos de uma só vez ou em um intervalo de tempo recorrente. A inscrição de alunos no conteúdo de aprendizado pode ser aumentada, fornecendo certificação aos alunos após a conclusão do curso. Como administrador, você pode criar um programa de certificação hospedado internamente ou conduzido por terceiros. Na certificação interna, defina os cursos que um aluno deve concluir para obter a certificação. Antes de criar a certificação, certifique-se de que você tenha alguns cursos disponíveis na conta. Consulte  [Ajuda para certificação](feature-summary/certifications.md) para obter mais informações sobre como criar certificações.

#### Criar ajudas de tarefa {#createjobaids}

As ajudas de tarefa são um repositório de conteúdo de treinamento acessível aos alunos sem critérios de inscrição ou conclusão. Os alunos podem consultar essas ajudas de tarefa para obter assistência na execução de qualquer atividade ou tarefa em uma organização. Embora não seja obrigatório usar ajudas de tarefa como parte da criação do curso, a equipe do Learning Manager recomenda que você crie ajudas de tarefa como uma prática recomendada para sua organização. Consulte o  [Ajuda de ajudas de tarefa](../authors/feature-summary/job-aids.md) para obter informações sobre como criar ajudas de tarefa.

#### Criar programas de aprendizado {#createlearningprograms}

Os programas de aprendizado são um conjunto de cursos exclusivamente projetados que atende aos objetivos específicos do aluno. Antes de criar programas de aprendizado, verifique se você já criou alguns cursos ou se há cursos disponíveis na sua conta.  Embora seja opcional para uma organização usar esse recurso, a equipe do Learning Manager recomenda que você o use para incluir aprendizado direcionado para seus funcionários. Para começar a usar os programas de aprendizado, clique em Programas de aprendizado no painel esquerdo, escolha um conjunto de cursos no catálogo e publique. Consulte o [Ajuda dos programas de aprendizado](feature-summary/learning-programs.md) instruções específicas.

### Criar catálogos {#createcatalogs}

Você pode usar catálogos em uma organização para criar um conteúdo direcionado ou para classificar o conteúdo em um conjunto definido de alunos. No Learning Manager, um catálogo é uma coleção de objetos de aprendizado, como cursos, certificações ou programas de aprendizado. Você pode escolher os objetos de aprendizado de sua escolha ao criar catálogos. Certifique-se de já ter criado um conjunto de cursos, certificações ou programas de aprendizado antes de criar os catálogos. Você pode personalizar a criação de catálogos com um conjunto de objetos de aprendizado se quiser atribuí-los a qualquer grupo de usuários interno ou externo. Consulte o  [Ajuda de catálogos](feature-summary/catalogs.md) para obter mais informações sobre catálogos.

### Ativar notificações por email/acesso de usuário {#turnonemailnotificationsuseraccess}

Nesta etapa, você pode ativar as notificações por e-mail para os usuários de seus aplicativos e também ativar o acesso do usuário.

## Fase 3 - Criação de cursos (autor) {#phase3authoringcoursesauthor}

Os desenvolvedores de conteúdo ou autores em sua organização podem começar a criar o conteúdo de aprendizado. É obrigatório criar módulos e cursos à medida que eles formam a base de todo o seu conteúdo de aprendizado no aplicativo Learning Manager.

### Criar módulos {#createmodules}

Os módulos são os componentes básicos do aplicativo Learning Manager. Para organizar seu conteúdo de aprendizado, comece a criar módulos como autor. O Learning Manager permite escolher qualquer um dos quatro tipos de módulos de curso, como sala de aula, ritmo individualizado, atividade e módulos de sala de aula virtual. Consulte  [Ajuda de Módulos](../authors/how-to-choose-modules.md) para saber qual tipo de módulo de curso é mais adequado para as necessidades da sua organização.

### Criar cursos {#createcourses}

Os administradores podem assumir uma função de autor no aplicativo Learning Manager e criar cursos. No aplicativo Learning Manager, um curso é uma unidade básica com um conjunto de módulos, que pode ser atribuída ao aluno. Os alunos consomem cursos. Você pode começar a criar cursos escolhendo os módulos criados anteriormente, associar as habilidades que deseja que os alunos obtenham do curso, associar níveis, créditos e medalhas a um curso, selecionar ajudas de tarefa, pré-requisitos e recursos com base na sua escolha e publicar o curso. Você também pode criar várias instâncias de um curso para que possa atribuir as instâncias do curso a vários alunos em fusos horários diferentes, programação e assim por diante. Consulte o  [Ajuda dos cursos](../authors/feature-summary/courses.md)para obter mais informações sobre como criar um curso.

### Criar objetos de aprendizado {#Createlearningobjects-1}

Esse é o estágio lógico em que todas as três faixas (faixa 1, faixa 2 e faixa 3) convergem para que você realize o próximo curso de ação.

Nesse ponto, depois de criar módulos e cursos, você pode começar a criar objetos de aprendizado de nível superior, como certificações, programas de aprendizado ou ajudas de tarefa para continuar. Antes de começar a criar objetos de aprendizado, verifique se você já adicionou alguns usuários no aplicativo Learning Manager e criou alguns módulos e cursos.

#### Criar certificações {#Createcertifications-1}

A certificação é uma prova da conclusão de um conteúdo de aprendizado ou uma prova de realização para os alunos de uma só vez ou em um intervalo de tempo recorrente. A inscrição de alunos no conteúdo de aprendizado pode ser aumentada, fornecendo certificação aos alunos após a conclusão do curso. Como administrador, você pode criar um programa de certificação hospedado internamente ou conduzido por terceiros. Na certificação interna, defina os cursos que um aluno deve concluir para obter a certificação. Antes de criar a certificação, certifique-se de que você tenha alguns cursos disponíveis na conta. Consulte  [Ajuda para certificação](feature-summary/certifications.md) para obter mais informações sobre como criar certificações.

#### Criar ajudas de tarefa {#CreateJobaids-1}

As ajudas de tarefa são um repositório de conteúdo de treinamento acessível aos alunos sem critérios de inscrição ou conclusão. Os alunos podem consultar essas ajudas de tarefa para obter assistência na execução de qualquer atividade ou tarefa em uma organização. Embora não seja obrigatório usar ajudas de tarefa como parte da criação do curso, a equipe do Learning Manager recomenda que você crie ajudas de tarefa como uma prática recomendada para sua organização. Consulte o  [Ajuda de ajudas de tarefa](../authors/feature-summary/job-aids.md) para obter informações sobre como criar ajudas de tarefa.

#### Criar programas de aprendizado {#Createlearningprograms-1}

Os programas de aprendizado são um conjunto de cursos exclusivamente projetados que atende aos objetivos específicos do aluno. Antes de criar programas de aprendizado, verifique se você já criou alguns cursos ou se há cursos disponíveis na sua conta.  Embora seja opcional para uma organização usar esse recurso, a equipe do Learning Manager recomenda que você o use para incluir aprendizado direcionado para seus funcionários. Para começar a usar os programas de aprendizado, clique em Programas de aprendizado no painel esquerdo, escolha um conjunto de cursos no catálogo e publique. Consulte o [Ajuda dos programas de aprendizado](feature-summary/learning-programs.md) instruções específicas.

## Fase 4 - Gerenciamento do seu LMS (Administrador do Learning Manager) {#phase4managingyourlmscaptivateprimeadministrator}

### Comunicados {#announcements}

Os comunicados são úteis à organização para dissipar todas as informações importantes para todos os alunos de uma conta de uma só vez. No aplicativo Learning Manager, um comunicado é uma mensagem multimídia (texto, imagem ou vídeo) que um administrador pode criar e transmitir para um conjunto definido de grupos de usuários e objetos de aprendizado. Você pode enviar comunicados instantaneamente ou agendar para acioná-los automaticamente em uma data específica. Se quiser usar esse recurso no aplicativo Learning Manager, escolha Comunicados no painel esquerdo e clique em Adicionar para criar comunicados. Consulte [Ajuda de Comunicados](feature-summary/announcements.md) para obter mais informações.

### Registro de usuário {#userenrollment}

A inscrição de usuários é uma etapa importante para um aplicativo LMS. Nesta etapa, você pode começar a inscrever os alunos em vários objetos de aprendizado do aplicativo Learning Manager. Você pode inscrever os alunos manualmente ou de forma automatizada usando planos de aprendizado.

#### Inscrição manual {#manualenrollment}

* **Autoinscrição -** Se você ativar essa opção ao criar um objeto de aprendizado, os alunos poderão se inscrever nos objetos de aprendizado.
* **Aprovação do gerente** - Se você escolher essa opção no tipo de inscrição ao criar um curso, os gerentes precisarão aprovar a inscrição dos alunos.
* **Nomeação do Gerente** - Se você escolher esse tipo de inscrição durante a criação do curso, esses cursos deverão ser indicados pelos gerentes.
* **Inscrição do administrador** - Nesse caso, o administrador pode inscrever alguns dos alunos com base nos requisitos da organização.

Consulte [Ajuda para inscrição de usuários](feature-summary/courses.md)para obter mais informações.

Inscreva os alunos nos objetos de aprendizado manualmente usando as quatro maneiras a seguir:

### Inscrição automática {#automatedenrollment}

Automatize a inscrição dos alunos em objetos de aprendizado usando planos de aprendizado.

#### Planos de aprendizado (com base em acionadores) {#learningplansbasedontriggers}

Você pode usar planos de aprendizado para atribuir automaticamente cursos, programas de aprendizado ou certificações aos alunos, com base na ocorrência de determinados eventos. Por exemplo,

* Novo usuário é adicionado
* O usuário altera o grupo de usuários
* O aluno conclui um objeto de aprendizado
* Usuário completa uma habilidade

Consulte [Ajuda dos planos de aprendizado](feature-summary/learning-plans.md)  para obter mais informações.

### Criar relatórios {#createreports}

Nesse estágio, você pode começar a criar e gerenciar vários tipos de relatórios.

O Adobe Learning Manager permite que você crie vários relatórios para rastrear, monitorar e controlar as atividades do aluno. Você pode usar os três tipos de recursos de relatório a seguir para gerar relatórios:

* **Painel de relatórios** - Crie relatórios de somatório para obter insights acionáveis sobre o consumo de conteúdo de aprendizado dos alunos, com base em várias categorias, como grupos de usuários, eficácia, tempo dos alunos nos cursos e assim por diante.
* **Transcrições do aluno** - Crie relatórios centrados no aluno com o histórico completo dos alunos desde o dia de registro até a data.
* **Relatórios do curso** - Criar estatísticas de consumo do curso dos alunos de cursos individuais. Você também pode criar relatórios do quiz no nível do curso.

Consulte  [Ajuda de Relatórios](feature-summary/reports.md) para obter mais informações sobre o processo de geração de relatórios.

Para obter outras informações relacionadas ao uso dos recursos do aplicativo Learning Manager, consulte [Ajuda do Learning Manager](../topics.md) com base em cada função.
