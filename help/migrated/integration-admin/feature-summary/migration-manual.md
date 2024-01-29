---
description: Consulte o manual para administradores de integração que desejam migrar um LMS existente para o LMS do Learning Manager
jcr-language: en_us
title: Manual de migração
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '3705'
ht-degree: 0%

---



# Manual de migração

Consulte o manual para administradores de integração que desejam migrar um LMS existente para o LMS do Learning Manager

## Visão geral {#overview}

<table>
 <tbody>
  <tr>
   <td><img src="assets/migration.jpg"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> é uma solução de gerenciamento de aprendizagem de autosserviço centrada no aluno e hospedada na nuvem. O Adobe permite que empresas com os atuais sistemas de gerenciamento de aprendizagem (LMS) migrem os dados de treinamento e o conteúdo do treinamento da sua organização para o aplicativo de LMS do Learning Manager. </p></td>
  </tr>
 </tbody>
</table>

### Cenário de uso {#usagescenario}

Em geral, as grandes empresas têm seu LMS interno ou sistemas de gerenciamento de aprendizagem herdados fornecidos por qualquer fornecedor. O LMS consiste no conteúdo de treinamento corporativo e nos dados de treinamento. Quando você compra o Learning Manager, pode querer mover o conteúdo e os dados existentes do LMS para o Learning Manager, para que possa aproveitar os benefícios do moderno e intuitivo LMS sem perder os dados herdados da sua organização.

O Learning Manager fornece as ferramentas e especificações necessárias para que o administrador de integração da sua organização possa configurar e executar as tarefas de migração.

A partir de hoje, o recurso de migração do Learning Manager pode ser acessado pelos administradores de uma empresa entrando em contato com a equipe de suporte da Adobe. Para ativar o recurso Migração em sua conta, entre em contato com a equipe de suporte do Adobe Learning Manager.

## Processo de migração {#apidescription}

Os pré-requisitos para migração, as principais etapas envolvidas no processo de migração, os sprints de migração, as especificações, os dados e as etapas de migração de conteúdo são explicados nesta seção da seguinte forma:

### Pré-requisitos {#prerequisites}

A equipe do Learning Manager espera que as tarefas a seguir sejam executadas pelos administradores de integração da sua empresa antes de iniciar o processo de migração:

* O administrador de integração extrai dados e conteúdo do LMS vigente e transforma os dados em formatos de arquivo, conforme definido pelo Learning Manager.
* O Learning Manager não oferece suporte à importação de usuários como parte do processo de migração e espera que a empresa importe os usuários utilizando conectores. A Adobe Systems espera que esses conectores sejam configurados antes do processo de migração. Consulte [Ajuda dos conectores do Learning Manager](connectors.md) para obter mais informações.

O Learning Manager recomenda que os administradores testem o processo de migração em uma conta de teste antes de migrar os dados e o conteúdo para o ambiente de produção do Learning Manager.

### Etapas principais do processo de migração {#keystepsofmigrationprocess}

As principais etapas envolvidas na migração de conteúdo e dados de um LMS existente para o Learning Manager são as seguintes:

1. O administrador ou parceiro de integração avalia os dados e o conteúdo existentes do LMS que precisam ser migrados.
1. O administrador de integração avalia as ferramentas e as especificações que o Learning Manager fornece para inclusão de dados e conteúdo.
1. O administrador de integração grava código ou realiza trabalho manual para exportar os dados e o conteúdo do treinamento do LMS mais antigo com base na funcionalidade fornecida pelo LMS mais antigo.
1. Quando os dados e o conteúdo do treinamento estiverem disponíveis, o administrador de integração analisa e mapeia os dados e o conteúdo para que correspondam às especificações de migração do Learning Manager.
1. O administrador de integração usa as ferramentas fornecidas pelo Learning Manager para migrar na seguinte ordem:

   1. Transferir os alunos para o Learning Manager
   1. Transferir o conteúdo de treinamento para o Learning Manager e
   1. Por fim, transfira os dados de treinamento para o Learning Manager.

A empresa pode começar a usar o LMS do Learning Manager junto com o conteúdo herdado.

### Escopo dos objetos de migração {#scopeofmigrationobjects}

Você pode migrar conteúdo apenas para os seguintes objetos de aprendizado:

* Módulo
* Medalhas
* Curso
* Versão do módulo
* Instância do curso
* Módulo do curso
* Habilidades
* Nível de habilidade
* Curso de habilidade
* Certificação
* Curso de certificação
* Confirmação de certificação
* Programa de aprendizado
* Curso do programa de aprendizado
* Instância do programa de aprendizado
* Instância do curso do programa de aprendizado
* Ajuda de tarefa
* Versão de ajuda de tarefa
* Curso de ajuda de tarefa
* Habilidades de ajuda de tarefa
* Inscrição
* Inscrição de certificação
* Inscrição no programa de aprendizado
* Inscrição em ajuda de tarefa
* Notas do curso do usuário



### Principais conceitos de migração {#keyconceptsofmigration}

Alguns dos principais conceitos do processo de migração do Learning Manager são explicados brevemente para rápida referência da seguinte forma:

**Projeto de migração**

No Learning Manager, um projeto de migração consiste em um ou mais sprints. Você também pode ter vários projetos de migração na sua conta. O processo de migração no Learning Manager começa com a criação de um projeto de migração.

**Sprint**

Um sprint, no processo de migração do Learning Manager, define um conjunto de itens de migração escolhido para ser migrado do LMS existente. Um item de migração pode ser um módulo de curso, registros do aluno ou um conjunto de cursos. É possível ter vários itens de dados de aprendizado em um sprint. Você pode executar tarefas de migração em cada sprint.

**Execuções de sprint**

Execução do sprint é o processo de início de um trabalho de migração do sprint. Você pode parar a execução do sprint a qualquer momento de uma Execução.

**Re-execuções de sprint**

É possível executar novamente um sprint de migração após sua conclusão a qualquer momento. Essa situação de reexecução ou reexecução de um sprint ocorre quando você deseja acrescentar os dados em um item de sprint e migrá-lo para o aplicativo novamente ou corrigir os erros em CSVs.

**Especificação do CSV**

O Learning Manager fornece um conjunto de [especificações CSV padrão](migration-manual.md#main-pars_header_140933605). A prática recomendada é analisar essas especificações CSV antes de iniciar o processo de migração. O administrador de integração da sua empresa pode analisar os formatos de dados existentes e mapeá-los para que correspondam aos itens de modelo CSV fornecidos do Learning Manager.

**Etiquetas do projeto de migração**

A Adobe Systems recomenda usar um conjunto de palavras-chave como etiquetas para identificar facilmente os projetos de migração no aplicativo Learning Manager. Essas etiquetas permitem identificar os projetos internamente no aplicativo Learning Manager em qualquer momento específico.

**Módulo sem conteúdo**

O Learning Manager permite carregar um módulo sem conteúdo. O Adobe Systems o considera um módulo sem conteúdo no Learning Manager. Em um cenário em que você deseja migrar alguns dos dados herdados do LMS existente sem a necessidade de qualquer conteúdo, é possível fazer upload do arquivo module_version.csv sem referência de URL.

## Especificações do CSV e CSVs de amostra {#csv}

Encontre abaixo as especificações CSV padrão que você pode usar para mapear com os dados de migração do LMS existentes. Clique em csv-specifications e sample-csvs para baixar os arquivos zip. O arquivo csv-specifications.zip baixado contém sete arquivos de planilha do Excel. Esses arquivos de planilha do Excel são especificações com descrições para que você entenda como preencher os arquivos .csv. Os arquivos .csv correspondentes devem conter os dados de cada campo no formato prescrito conforme explicado nestes arquivos .xlsx.

<table border="1" cellspacing="0" cellpadding="0" width="100%">
 <tbody>
  <tr>
   <th>
    <p><b>Sl.no</b></p></th>
   <th>
    <p><b>Nome do arquivo</b></p></th>
   <th>
    <p><b>Descrição do conteúdo</b></p></th>
   <th>
    <p>Observações</p></th>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>module.xlsx</p></td>
   <td>
    <p>Metadados para module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>badge.xlsx</p></td>
   <td>
    <p>Metadados para emblema.xlsx</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>course.xlsx</p></td>
   <td>
    <p>Metadados para course.csv</p></td>
   <td>
    <p>Indique um nome de autor de um curso específico porque, às vezes, vários nomes de autor não são exibidos corretamente no aplicativo após a migração. </p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>module_version.xlsx </p></td>
   <td>
    <p>Metadados para module_version.csv</p></td>
   <td>
    <p>Certifique-se de fornecer o caminho do URL da pasta da conta do Box na qual o conteúdo foi carregado. </p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>course_instance.xlsx</p></td>
   <td>
    <p>Metadados para course_instance.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>session.xlsx</p></td>
   <td>
    <p>Metadados para session.csv</p></td>
   <td>
    <p>Verifique se cada entrada no csv da sessão está associada a pelo menos um módulo Sala de aula/Sala de aula virtual</p></td>
  </tr>
  <tr>
   <td>
    <p>7</p></td>
   <td>
    <p>course_module.xlsx</p></td>
   <td>
    <p>Metadados para course_module.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>8</p></td>
   <td>
    <p>skill.xlsx</p></td>
   <td>
    <p>Metadados para skill.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>9</p></td>
   <td>
    <p>skill_level.xlsx</p></td>
   <td>
    <p>Metadados para skill_level.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>10</p></td>
   <td>
    <p>skill_course.xlsx</p></td>
   <td>
    <p>Metadados para skill_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>11</p></td>
   <td>
    <p>certification.xlsx</p></td>
   <td>
    <p>Metadados para Certification.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>12</p></td>
   <td>
    <p>certification_course.xlsx</p></td>
   <td>
    <p>Metadados para certification_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>13</p></td>
   <td>
    <p>certification_commit.xlsx</p></td>
   <td>
    <p>Metadados para certification_commit.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>14</p></td>
   <td>
    <p>learning_program.xlsx</p></td>
   <td>
    <p>Metadados para learning_program.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>15</p></td>
   <td>
    <p>learning_program_course.xls </p></td>
   <td>
    <p>Metadados para learning_program_course.csv </p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>16</p></td>
   <td>
    <p>learning_program_instance.xlsx </p></td>
   <td>
    <p>Metadados para learning_program_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>17</p></td>
   <td>
    <p>learning_program_instance_course_instance.xlsx </p></td>
   <td>
    <p>Metadados para learning_program_instance_course_instance.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>18</p></td>
   <td>
    <p>job_aid.xlsx</p></td>
   <td>
    <p>Metadados para job_aid.csv</p></td>
   <td>
    <p>Cada job_aid migrado requer uma ou mais versões de job_aid.</p></td>
  </tr>
  <tr>
   <td>
    <p>19</p></td>
   <td>
    <p>Job_aid_version.xlsx</p></td>
   <td>
    <p>Metadados para job_aid_version.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>20</p></td>
   <td>
    <p>job_aid_course.xlsx</p></td>
   <td>
    <p>Metadados para job_aid_course.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>21</p></td>
   <td>
    <p>job_aid_skills.xlsx</p></td>
   <td>
    <p>Metadados para job_aid_skills.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>22</p></td>
   <td>
    <p>enrollments.xlsx</p></td>
   <td>
    <p>Metadados para enrollments.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>23</p></td>
   <td>
    <p>certification_enrollement.xlsx</p></td>
   <td>
    <p>Metadados para certification_enrollement.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>24</p></td>
   <td>
    <p>learning_program_enrollment.xlsx</p></td>
   <td>
    <p>Metadados para learning_program_enrollment.csv<br><br></p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>25</p></td>
   <td>
    <p>job_aid_enrollment.xlsx</p></td>
   <td>
    <p>Metadados para job_aid_enrollment.csv</p></td>
   <td> </td>
  </tr>
  <tr>
   <td>
    <p>26</p></td>
   <td>
    <p>user_course_grade.xlsx</p></td>
   <td>
    <p><br>
      Metadados para user_course_grade.csv</p></td>
   <td>
    <p>Forneça os dados necessários de registros do aluno no arquivo .csv mesmo que não sejam obrigatórios. Sem essas informações, mesmo que o .csv seja processado para migração, o aplicativo Learning Manager pode não refletir nenhum dado. O arquivo sample-csvs.zip contém sete arquivos .csv com a convenção de nomenclatura conforme indicado acima.</p></td>
  </tr>
 </tbody>
</table>

O Learning Manager oferece suporte a valores de data e hora somente no formato UTF 8 e 32 bits. Você pode obter erros durante a migração se mencionar a data em arquivos CSV com uma data fora do intervalo como 2038-07-17T08:53:21.000Z ou 1980-04-17T08:13:25,322Z
[sample-csvs.zip](assets/sample-csvs.zip) [csv_specifications.zip](assets/csv-specifications.zip)Você precisa estar ciente das seguintes dependências em arquivos CSV durante a importação:

* module_version.csv depende de module.csv
* course_instance.csv depende de course.csv
* course_module.csv depende de course.csv, module.csv e module_version.csv
* course_instance.csv depende de course.csv
* O session.csv depende do course.csv e do module.csv
* enrollment.csv depende de course.csv
* user_course_grade.csv depende de course.csv e module.csv
* skill_course.csv depende de course.csv
* skill_level.csv depende de skill.csv
* learning_program_instance.csv depende de learning_program e learning_program_course.csv
* learning_program_course.csv depende de learning_program.csv
* learning_program_enrollment.csv depende de learning_program e learning_program_instance.csv
* learning_program_instance_course_instance.csv depende de learning_program.csv, learning_program_instance.csv e course_instance.csv
* certification_course.csv depende de certification.csv e course.csv
* certification_commit.csv depende de certification.csv e certification_course.csv
* certification_enrollment.csv depende de certification.csv, certification_course.csv e certification_enrollment.csv

## Procedimento de migração {#migrationprocedure}

Antes de começar o procedimento de migração, é importante observar os seguintes pontos:

* Somente um projeto de migração pode estar ativo em uma conta em qualquer momento específico. Em um projeto, somente um sprint pode estar ativo em um determinado momento no tempo.
* Não é possível desfazer uma execução que já está no processo de migração. No entanto, você pode usar a opção de exclusão existente em cada recurso do Learning Manager para desfazer qualquer migração de dados ou conteúdo.
* Assim que o projeto de migração é iniciado, ele passa para o estado de &#39;Em migração&#39;. Durante a migração, nenhuma outra função além da função de administrador de integração pode fazer logon no Learning Manager.

### Criar contas FTP e Box {#creatingftpandboxaccounts}

Planejar seu projeto de migração é muito importante. É recomendável dividir os projetos em vários sprints e identificar claramente o que deseja migrar em cada sprint. Pode até ser uma boa ideia fazer alguma validação após cada sprint para ter certeza sobre os dados migrados nesse sprint, em vez de uma grande fase de validação no final do projeto. Antes de iniciar o sprint como parte do projeto de migração, é necessário fazer upload dos arquivos CSV de dados e conteúdo nos servidores FTP e Box, respectivamente. Se você não tiver contas para FTP e Box personalizados, é possível criá-las.

**Criar conta FTP**

Clique em **[!UICONTROL Solicitação de pasta FTP CSV]**. Uma caixa de diálogo suspensa será exibida, solicitando que você insira sua ID de e-mail. Siga as instruções online e crie uma conta FTP. Assim que criar sua conta, você poderá visualizar seu projeto de migração e as pastas do projeto de sprint no FTP.

Um instantâneo de amostra de arquivos de projeto e pasta de FTP é mostrado abaixo para sua referência.

<!--![](assets/exavault-migration-upload-folders.png)-->

**Criar conta do Box**

Crie uma pasta de upload de conteúdo em um processo semelhante ao seguido para a criação da pasta FTP. Clique em Migração no painel esquerdo e clique em Solicitar para uma pasta de upload de conteúdo na parte inferior da página exibida.

Você receberá um email do Box com um link para a pasta compartilhada. Se você não tiver uma conta do Box, clique em Inscrever-se e crie uma conta. As instruções de logon são enviadas à ID de e-mail do administrador de integração.

**Carregamento de dados (arquivos .csv) em pastas FTP ou pastas do Box**

Criar uma conta FTP ou Box é um pré-requisito antes de criar um projeto de migração. Portanto, nesta etapa, você pode criar um projeto e um sprint de migração no aplicativo Learning Manager.  Consulte **Procedimento de migração de dados e conteúdo** nesta página para criar o projeto de migração.

Na conta FTP ou Box, clique no nome da pasta do seu projeto e clique no nome do sprint. Dentro da pasta do sprint, você pode fazer upload dos arquivos de dados .csv que pretende migrar. Para fazer upload, clique no botão Fazer upload de arquivos na parte superior do servidor FTP ou Box e solte os arquivos .csv. Um instantâneo de exemplo após fazer upload para o FTP é mostrado abaixo para sua referência.

<!--![](assets/exavault-upload.png)-->

Você pode voltar ao projeto de migração do Learning Manager, clique em **[!UICONTROL Atualizar]** e visualize todos os tipos de dados .csv listados no sprint de migração.

**Carregar conteúdo de treinamento nas pastas de conteúdo**

Carregue o conteúdo de treinamento do LMS existente na sua conta do Box. Se você já tiver criado o projeto de migração e o sprint, a conta do Box preencherá o projeto de migração e o nome do sprint. Você pode carregar o conteúdo no mesmo caminho. Consulte **Procedimento de migração de dados e conteúdo** nesta página para criar o projeto de migração.

Arraste e solte os arquivos de conteúdo ou clique em **[!UICONTROL Carregar]** e selecione os arquivos da área de trabalho. Se o tamanho do arquivo de seu conteúdo for muito grande, pode haver algum atraso no upload dos arquivos. Dependendo do tamanho do arquivo, o tempo necessário para carregar os arquivos em sua conta do Box varia.

Um exemplo de captura de tela da conta do Box após o upload do conteúdo para ela é mostrado abaixo para sua referência:

![](assets/box-account.png)

*Arquivos na conta do Box*

Após o upload dos arquivos na sua conta do Box, lembre-se de mencionar o caminho relativo do arquivo de conteúdo do Box em module_version.csv. Esta é uma etapa obrigatória para você indicar o caminho do conteúdo do módulo.

Depois de fazer logon nos servidores FTP e Box e carregar o conteúdo, os locais do CSV aparecem conforme ilustrado na captura de tela abaixo no Learning Manager.

![](assets/after-setup.jpg)

*Locais do CSV na conta do Box*

## Procedimento de migração de dados e conteúdo {#dataandcontentmigrationprocedure}

O procedimento para migrar os dados e o conteúdo do LMS corporativo para o Learning Manager é explicado da seguinte forma:

Analise os pré-requisitos do processo de migração antes de começar a migração. Consulte [Especificações do CSV e CSVs de amostra](migration-manual.md#main-pars_header_140933605) nesta página e prepare os CSVs para migração de dados e conteúdo.

1. Faça logon no aplicativo Learning Manager como administrador de integração e clique em **[!UICONTROL Migração]** no painel esquerdo.

   A página inicial dos Projetos de migração é exibida. Se sua organização já criou projetos de migração, você pode exibir a lista de todos os projetos de migração nesta página.

1. Clique em **[!UICONTROL Novo]** no canto superior direito da página para criar um projeto de migração. Como alternativa, você pode clicar em **[!UICONTROL Criar um projeto de migração]** na página para criar um projeto de migração. A página Criar um projeto de migração é exibida.

   Se você já não tiver criado uma pasta FTP, será solicitado que você crie uma pasta FTP na conta. Essa etapa é obrigatória antes de começar a criar um projeto de migração.

   ![](assets/create-project.png)
   *Criar pasta FTP*

   Forneça o nome do projeto, a tag do projeto, o catálogo do curso e a descrição do seu projeto de migração. Clique em **[!UICONTROL Criar]**.

   Os itens de dados de migração são identificados usando esta etiqueta de projeto de migração. Se você não tiver um catálogo específico do curso, escolha o catálogo padrão na lista suspensa. Todos os cursos que você migrar usando um projeto de migração serão incluídos no catálogo escolhido nessa etapa. Se nenhum catálogo for escolhido, todos os cursos migrados farão parte do catálogo padrão.

1. A página de configuração do sprint é exibida conforme mostrado no instantâneo a seguir. Você precisa criar um sprint como parte do projeto de migração. Escolha Nome do sprint e forneça uma breve descrição do sprint. Você pode escolher Sim se quiser migrar conteúdo como parte desse sprint. Clique em **[!UICONTROL Próxima]**.

   ![](assets/users-modified-sprint.png)
   *Migração do sprint*

   Marque a caixa de seleção com o título **Os usuários foram adicionados ou modificados desde a última execução**, para sincronizar a lista de usuários com o aplicativo Learning Manager. Se estiver migrando dados e conteúdo para o aplicativo Learning Manager, talvez isso não seja obrigatório. Mas, se houver um lapso de tempo entre a migração anterior do sprint para a migração mais recente, a prática recomendada é optar por sincronizar a lista de usuários. Essa etapa permite que o banco de dados do Learning Manager esteja em sincronia com os usuários do LMS.

   Essa etapa de sincronização é recomendada quando enrollment.csv e user_course_grade.csv são migrados. Essa etapa permite que o banco de dados do Learning Manager esteja em sincronia com o banco de dados de migração e garante que todos os usuários cujos registros a serem migrados no sprint estejam disponíveis no banco de dados de migração.

1. Você pode iniciar a migração do sprint com os dados e o conteúdo carregados. Clique em **[!UICONTROL Atualizar]** antes de iniciar a Execução do sprint para sincronizar as pastas FTP e Conteúdo com o aplicativo Learning Manager.

   ![](assets/sprint1-filesupload.png)
   *Iniciar migração do sprint*

   Clique em **[!UICONTROL Início]** no canto superior direito da página. Você pode clicar em **[!UICONTROL Parar]** a qualquer momento durante o processo de migração do sprint para abortar a migração do sprint.

   O status da migração é exibido em cada um dos itens de dados e conteúdo do sprint. Verifique o número de itens falhos e bem-sucedidos como parte da execução do sprint de migração.

   Se estiver carregando o conteúdo do módulo, certifique-se de que o caminho da pasta de conteúdo seja fornecido em module_version.csv. Se não realizar essa etapa, podem ocorrer erros durante a migração. Por exemplo, se estiver carregando o conteúdo de um módulo de ritmo individualizado como vídeos, você precisa especificar o caminho relativo do URL do Box em module_version.csv. Para o conteúdo do módulo Atividade, você pode especificar o nome do URL.

   Uma captura de tela de exemplo da caixa de diálogo de progresso é fornecida abaixo para sua referência. Conforme mostrado na captura de tela, você pode exibir o número de registros processados para cada item de dados de migração juntamente com o status de itens com êxito e com falha. Clique em Baixar registros de erros em relação aos itens com falha para baixar e exibir os registros de erros. Você pode corrigir os problemas no CSV e fazer upload novamente no FTP.

   ![](assets/sample-sprint-progress-status.png)
   *Exibir progresso do sprint*

   Clique na lista Sprint no painel esquerdo se quiser exibir a lista de todos os sprints de um projeto de migração. Você pode exibir uma lista de todos os sprints, o número de execuções de cada sprint, a data de início, a duração e o status de conclusão, conforme mostrado na captura de tela abaixo.

   ![](assets/sprint-list.png)
   *Exibir lista de sprints*

1. Depois de fazer upload dos CSVs atualizados mais recentes, você pode clicar em Reexecutar no canto superior direito da página. A nova execução processa todos os itens de dados mais uma vez, ignorando os itens que não têm nenhuma alteração. Quando estiver satisfeito com a migração de itens de dados em um sprint, marque a migração de mola como concluída clicando no botão na parte superior da página. Você pode iniciar um novo sprint com mais itens de dados posteriormente. Quando um sprint é marcado como concluído, não é possível Executá-lo novamente. Da mesma forma, em um projeto de migração, você pode ter qualquer número de sprints. Quando estiver satisfeito com o status de migração de todos os Sprints, marque o projeto de migração como Concluído clicando em **Marcar Projeto como Concluído** na página Lista de sprint.

   Antes de marcar o projeto de migração como concluído, você deve garantir que todos os sprints do projeto estejam concluídos. Depois de marcar o projeto de migração como concluído, você não poderá voltar e criar sprints nesse projeto ou fazer modificações nesse projeto. Você precisa criar outro projeto de migração e adicionar sprints a ele.

## Verificação de migração {#registration}

Depois de migrar os dados e o conteúdo de aprendizado do LMS herdado da sua organização, você pode verificar os dados e o conteúdo importados usando vários recursos de objetos de aprendizado. Por exemplo, você pode fazer logon no aplicativo Learning Manager como administrador e verificar a disponibilidade dos dados e do conteúdo dos módulos e cursos importados.

## Adaptação na migração {#retrofittinginmigration}

Esse recurso de integração permite que você renove dados históricos de um objeto de aprendizado de um sistema de gerenciamento de aprendizado herdado em um curso ativo criado no Learning Manager.

Encontre abaixo as especificações CSV padrão que você pode usar para mapear com os dados de migração do LMS existentes. Clique em csv-specifications e sample-csvs para baixar os arquivos zip. O arquivo csv-specifications.zip baixado contém quatro arquivos de planilha do Excel. Esses arquivos de planilha do Excel são especificações com descrições para que você entenda como preencher os arquivos .csv. Os arquivos .csv correspondentes devem conter os dados de cada campo no formato prescrito conforme explicado nestes arquivos .xlsx.

1-enrollment.xlsx-contém descrições de metadados necessários para o arquivo retrofit_enrollment.csv.

2-certification_enrollment.xlsx-contém descrições de metadados necessários para o arquivo retrofit_certification_enrollment.csv.

3-learning_program_enrollment.xlsx-contém descrições de metadados necessários para o arquivo retrofit_learning_program_enrollment.csv.

4-user_course_grades.xlsx-contém descrições de metadados necessários para o arquivo retrofit_user_course_grades.csv.
[csv-specifications.zip](assets/csv-specifications.zip)

## Solução de problemas de migração {#troubleshootingmigrationissues}

[Clique aqui](../../kb/troubleshooting-migration.md) para saber mais sobre a solução dos problemas enfrentados pelos administradores de integração ao migrar dados e conteúdo do LMS existente para o Learning Manager.

## Dicas para gerenciamento de usuários {#usermanagement}

Neste tópico, encontram-se algumas dicas para compreender como os usuários são analisados e gerenciados no Learning Manager. Esses conceitos poderiam ajudar você a gerenciar melhor os usuários ao usar a importação de CSV, os conectores e os recursos de migração do Learning Manager.

## IDs do Learning Manager {#captivateprimeids}

O Learning Manager fornece dois tipos de IDs exclusivas para usuários:

* ID de e-mail
* UUID (ID exclusiva universal)

O Learning Manager oferece suporte à UUID para proporcionar flexibilidade às organizações no controle de contas de usuários. Como administrador, se você tiver a UUID de usuários em uma conta, poderá modificar as IDs de e-mail dos usuários dessa conta.

**Cenário de uso da UUID em uma organização**

Considere um cenário em que um funcionário A entra em uma empresa chamada Learning Manager, como contratado. Durante o período do contrato, a empresa do Learning Manager não pode fornecer a ID de e-mail da empresa como A@example.com; em vez disso, a empresa pode considerar apenas a conta de e-mail pessoal do funcionário, por exemplo, A@gmail.com. Após completar 6 meses do período do contrato, se o mesmo funcionário A ingressar no Learning Manager como funcionário em tempo integral, o Learning Manager poderá alterar sua ID de e-mail para a ID de e-mail de sua empresa: A@example.com.

Ter acesso da UUID à conta do usuário beneficiará o Learning Manager da empresa no cenário mencionado acima. A empresa do Learning Manager pode substituir facilmente a ID de e-mail pessoal do funcionário A por uma ID de e-mail oficial. Os registros do funcionário relevantes para essa conta não são afetados por essa alteração.

## Identificação de usuário único {#singleuseridentification}

O Learning Manager identifica e lembra como um único usuário é adicionado a ele, por exemplo, usando o autorregistro, o upload de CSV, ou um único usuário adicionado usando a interface do usuário ou por meio da API.

* Se um único usuário for adicionado usando a interface do usuário (UI) ou por meio da API, você poderá excluir esse tipo de usuários únicos usando a UI ou a API.
* Você pode atualizar usuários únicos usando o processo de upload de CSV, mas é necessário lembrar que esses usuários únicos são tratados como usuários CSV e os fluxos de trabalho CSV são aplicáveis a esses usuários.

## Atribuindo função de gerente {#assigningmanagerrole}

Não é possível atribuir diretamente a função de gerente a nenhum usuário no Learning Manager. Um usuário X pode se tornar um gerente do Learning Manager somente quando você definir o atributo Gerente de qualquer usuário (digamos, Y) nessa conta como X.

Em um cenário em que X é o gerente de usuários, por exemplo, A, B e C, se X deixar a organização, será necessário garantir que o atributo Gerente de A, B e C seja definido como o novo gerente. Como alternativa, você também pode definir o atributo Manager desses usuários como ROOT temporariamente e atribuir com o novo nome Manager posteriormente.

Para obter mais informações sobre este tópico, consulte o seguinte conteúdo de Ajuda:

* [Perguntas frequentes sobre carregamento de CSVs](/help/migrated/administrators/add-users-in-bulk.md)
* [Ajuda do recurso sobre adição de usuários](/help/migrated/administrators/feature-summary/add-users-user-groups.md)

