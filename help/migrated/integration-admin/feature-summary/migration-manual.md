---
description: Consulte o manual para administradores de integração que desejam migrar um LMS existente para o Adobe Learning Manager LMS.
jcr-language: en_us
title: Manual de migração
exl-id: bfdd5cd8-dc5c-4de3-8970-6524fed042a8
source-git-commit: acef8666ce207fdb81011265814b4d4278da7406
workflow-type: tm+mt
source-wordcount: '4438'
ht-degree: 59%

---

# Manual de migração

Consulte o manual para administradores de integração que desejam migrar um LMS existente para o LMS do Learning Manager

<!-- ## Overview {#overview} -->

## Cenário de uso {#usagescenario}

Em geral, as grandes empresas têm seu LMS interno ou qualquer sistema de gerenciamento de aprendizagem legado fornecido pelo fornecedor. O LMS consiste no conteúdo de treinamento corporativo e nos dados de treinamento. Quando você compra o Learning Manager, pode querer mover o conteúdo e os dados existentes do LMS para o Learning Manager, para que possa aproveitar os benefícios do moderno e intuitivo LMS sem perder os dados herdados da sua organização.

O Learning Manager fornece as ferramentas e especificações necessárias para que o administrador de integração da sua organização possa configurar e executar as tarefas de migração.

A partir de hoje, o recurso de migração do Learning Manager pode ser acessado pelos administradores de uma empresa entrando em contato com a equipe de suporte da Adobe. Para ativar o recurso Migração em sua conta, você pode entrar em contato com a equipe de suporte do Adobe Learning Manager.

## Processo de migração {#apidescription}

Os pré-requisitos para migração, as principais etapas envolvidas no processo de migração, os sprints de migração, as especificações, os dados e as etapas de migração de conteúdo são explicados nesta seção da seguinte forma:

### Pré-requisitos {#prerequisites}

A equipe do Learning Manager espera que as tarefas a seguir sejam executadas pelos administradores de integração da sua empresa antes de iniciar o processo de migração:

* O administrador de integração extrai os dados e o conteúdo do LMS vigente e transforma os dados em formatos de arquivo, conforme definido pelo Learning Manager.
* O Learning Manager não oferece suporte à importação de usuários como parte do processo de migração e espera que a empresa importe os usuários utilizando conectores. A Adobe Systems espera que esses conectores sejam configurados antes do processo de migração. Consulte [Ajuda dos conectores do Learning Manager](connectors.md) para mais informações.

O Learning Manager recomenda que os administradores testem o processo de migração em uma conta de teste antes de migrar os dados e o conteúdo para o ambiente de produção do Learning Manager.

### Principais etapas do processo de migração {#keystepsofmigrationprocess}

As principais etapas envolvidas na migração de conteúdo e dados de um LMS existente para o Learning Manager são as seguintes:

1. O administrador ou parceiro de integração avalia os dados e o conteúdo existentes do LMS que precisam ser migrados.
1. O administrador de integração avalia as ferramentas e as especificações que o Learning Manager proporciona para inclusão dos dados e do conteúdo.
1. O administrador de integração grava o código ou realiza trabalho manual para exportar os dados e o conteúdo de treinamento do LMS mais antigo, com base na funcionalidade fornecida pelo LMS mais antigo.
1. Quando os dados e o conteúdo do treinamento estiverem disponíveis, o administrador de integração analisa e mapeia os dados e o conteúdo para que correspondam às especificações de migração do Learning Manager.
1. O administrador de integração usa as ferramentas fornecidas pelo Learning Manager para migrar na seguinte ordem:

   1. Transferir os alunos para o Learning Manager
   1. Transferir o conteúdo de treinamento para o Learning Manager e
   1. Por fim, transfira os dados de treinamento para o Learning Manager.

A empresa pode começar a usar o LMS do Learning Manager juntamente com o conteúdo existente.

### Escopo dos objetos de migração {#scopeofmigrationobjects}

Você pode migrar conteúdo apenas para os seguintes objetos de aprendizado:

* Módulo
* Medalhas
* Curso
* Versão do módulo
* Instância do curso
* Módulo do curso
* Habilidades
* Nível da habilidade
* Habilidade do curso
* Certificação
* Curso de certificação
* Participação na certificação
* Programa de aprendizado
* Curso do programa de aprendizado
* Instância do programa de aprendizado
* Instância do curso do programa de aprendizado
* Material de ajuda
* Versão do material de ajuda
* Curso do material de ajuda
* Habilidades do material de ajuda
* Inscrição
* Inscrição na certificação
* Inscrição no programa de aprendizado
* Inscrição no material de ajuda
* Notas do curso do usuário

### Principais conceitos da migração {#keyconceptsofmigration}

Alguns dos principais conceitos do processo de migração do Learning Manager são explicados brevemente para rápida referência da seguinte forma:

**Projeto de migração**

No Learning Manager, um projeto de migração está formado por um ou mais sprints. Você também pode ter vários projetos de migração na sua conta. O processo de migração do Learning Manager começa com a criação de um projeto de migração.

**Sprint**

Um sprint, no processo de migração do Learning Manager, define um conjunto de itens de migração escolhido para ser migrado do LMS existente. Um item de migração pode ser um módulo do curso, registros do aluno ou um conjunto de cursos. É possível ter vários itens de dados de aprendizado em um sprint. É possível executar tarefas de migração em cada sprint.

**Execuções de sprint**

Execução de sprint é o processo de iniciar uma tarefa de migração do sprint. É possível interromper a execução do sprint em qualquer ponto de uma execução.

**Re-execuções de sprint**

É possível executar um sprint de migração novamente a qualquer momento após a conclusão. Essa situação de re-execução de um sprint ocorre quando você quer acrescentar os dados em um item de sprint e migrá-los novamente no aplicativo ou corrigir os erros nos CSVs.

**Especificação do CSV**

O Learning Manager fornece um conjunto de [especificações CSV padrão](migration-manual.md#main-pars_header_140933605). A prática recomendada é analisar essas especificações CSV antes de iniciar o processo de migração. O administrador de integração da sua empresa pode analisar os formatos de dados existentes e mapeá-los para que correspondam aos itens de modelo CSV fornecidos do Learning Manager.

**Etiquetas do projeto de migração**

A Adobe Systems recomenda usar um conjunto de palavras-chave como etiquetas para identificar facilmente os projetos de migração dentro do aplicativo Learning Manager. Essas etiquetas permitem identificar os projetos internamente no aplicativo Learning Manager em qualquer momento específico.

**Módulo sem conteúdo**

O Learning Manager permite carregar um módulo sem conteúdo. Adobe Systems se considera um módulo sem conteúdo no Learning Manager. Em casos nos quais se deseja migrar alguns dados legados do LMS existente sem a necessidade de conteúdo, é possível carregar o arquivo module_version.csv sem referência de URL.

## Especificações do CSV e CSVs de amostra {#csv}

Abaixo encontram-se as especificações CSV padrão que podem ser usadas para mapear os dados de migração do LMS existente. Clique em csv-specifications e sample-csvs para baixar os arquivos zip. O arquivo csv-specifications.zip baixado contém sete arquivos de planilha do Excel. Esses arquivos de planilha do Excel são especificações com descrições para que você entenda como preencher os arquivos .csv. Os arquivos .csv correspondentes devem conter os dados de cada campo no formato prescrito, conforme explicado nesses arquivos .xlsx.

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
    <p>Notas</p></th>
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
    <p>Metadados para course.csv</p></td>
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
    <p>Verifique se todas as entradas no CSV da sessão foram associadas a pelo menos um módulo de sala de aula/sala de aula virtual</p></td>
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
    <p>Cada job_aid migrado precisa ter uma ou mais versões de job_aid.</p></td>
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
  <tr>
   <td>
    <p>27</p></td>
   <td>
    <p>user_skill.xlsx</p></td>
   <td>
    <p><br>
      Metadados para user_skill.csv</p></td>
   <td>
    <p> </p></td>
  </tr>
 </tbody>
</table>

O Learning Manager oferece suporte a valores de data e hora somente no formato UTF 8 e 32 bits. Você pode obter erros durante a migração se mencionar a data em arquivos CSV com uma data fora do intervalo como 2038-07-17T08:53:21.000Z ou 1980-04-17T08:13:25.322Z.

* [sample-csvs.zip](assets/sample-csvs.zip)
* [csv_specifications.zip](assets/csv-specifications.zip)

Você deve estar ciente das seguintes dependências dos arquivos CSV durante a importação:

* module_version.csv depende de module.csv
* course_instance.csv depende de course.csv
* course_module.csv depende de course.csv, module.csv e module_version.csv
* course_instance.csv depende de course.csv
* session.csv depende de course.csv e module.csv
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

* Somente um projeto de migração pode estar ativo em uma conta em um dado momento. Dentro de um projeto, somente um sprint pode estar ativo em um dado momento.
* Não é possível desfazer uma execução que já está em processo de migração. No entanto, é possível usar a opção de exclusão existente em cada recurso do Learning Manager para desfazer qualquer migração de dados ou conteúdo.
* Assim que o projeto de migração é iniciado, ele passa para o estado de &#39;Em migração&#39;. Durante a migração, nenhuma outra função além da função de administrador de integração pode fazer login no Learning Manager.

### Criação de contas FTP e Box {#creatingftpandboxaccounts}

É muito importante planejar o projeto de migração. Recomenda-se dividir os projetos em vários sprints e identificar com clareza o que se quer migrar em cada sprint. Pode ser uma boa ideia fazer validações após cada sprint para estar seguro dos dados migrados nesse sprint, em vez de fazer uma grande fase de validação no fim do projeto. Antes de começar o sprint como parte do projeto de migração, é necessário carregar arquivos CSV de dados e conteúdo no FTP e nos servidores do Box respectivamente. Se você não tiver contas para FTP e Box personalizados, é possível criá-las.

<!--**Create FTP account**-->

<!--Click **[!UICONTROL Request for CSV FTP folder]**. A pop-up dialog appears prompting you to enter your e-mail id. Go through online instructions and create an FTP account. As soon as you create your account, you can view your migration project and sprint project folders in FTP. 

A sample snapshot of project files and folder of FTP is shown below for your reference. -->

<!--![](assets/exavault-migration-upload-folders.png)-->

**Criar conta do Box**

Crie a pasta para carregamento de conteúdo de forma semelhante à criação da pasta FTP. Clique em Migração no painel esquerdo e clique em Solicitar uma pasta para carregamento de conteúdo na parte inferior da página exibida.

Você receberá um e-mail do Box com um link para a pasta compartilhada. Se não tiver uma conta do Box, clique em Inscreva-se e crie uma conta. As instruções de login são enviadas à ID de e-mail do administrador de integração.

**Carregamento de dados (arquivos .csv) em pastas FTP ou pastas do Box**

A criação de contas FTP ou Box é um pré-requisito para criar projetos de migração. Portanto, nesta etapa, você pode criar um projeto e um sprint de migração no aplicativo Learning Manager.  Consulte a seção **Procedimento de migração de dados e conteúdo** nesta página para criar o projeto de migração.

Nas contas FTP ou Box, clique no nome da pasta do projeto e clique no nome do sprint. Dentro da pasta de sprint, você pode carregar os arquivos de dados .csv que pretende migrar. Para fazer upload, clique no botão Fazer upload de arquivos na parte superior do servidor FTP ou Box e solte os arquivos .csv. Um instantâneo de exemplo após fazer upload para o FTP é mostrado abaixo para sua referência.

<!--![](assets/exavault-upload.png)-->

Você pode voltar ao projeto de migração do Learning Manager, clicar em **[!UICONTROL Atualizar]** e visualizar todos os tipos de dados .csv listados no sprint de migração.

**Carregar conteúdo de treinamento nas pastas de conteúdo**

Carregue o conteúdo de treinamento do LMS existente na sua conta do Box. Se já tiver cirado o sprint e o projeto de migração, a conta do Box preencherá o nome do sprint e do projeto de migração. Você pode carregar o conteúdo no mesmo caminho. Consulte a seção **Procedimento de migração de dados e conteúdo** nesta página para criar o projeto de migração.

Você pode arrastar e soltar os arquivos de conteúdo ou clicar em **[!UICONTROL Carregar]** e selecionar os arquivos na área de trabalho. Se o tamanho do arquivo de conteúdo for muito grande, pode ocorrer um atraso ao carregar os arquivos. Dependendo do tamanho do arquivo, o tempo necessário para carregar os arquivos em sua conta do Box varia.

Um exemplo de captura de tela da conta do Box após o upload do conteúdo para ela é mostrado abaixo para sua referência:

![](assets/box-account.png)

*Conta de arquivos no Box*

Depois que os arquivos são carregados na conta do Box, certifique-se de indicar o caminho relativo deste arquivo de conteúdo do Box no arquivo module_version.csv. É obrigatória a etapa de indicar o caminho do conteúdo do módulo.

Após fazer login nos servidores FTP e Box, e carregar o conteúdo, as localizações do CSV aparecem conforme ilustrado na captura de tela abaixo no Learning Manager.

![](assets/after-setup.jpg)

*Locais CSV na conta do Box*

## Procedimento de migração de dados e conteúdo {#dataandcontentmigrationprocedure}

O procedimento para migrar os dados e o conteúdo do LMS corporativo para o Learning Manager é explicado da seguinte forma:

Analise os pré-requisitos do processo de migração antes de começar a migração. Consulte a seção [Especificações do CSV e CSVs de amostra](migration-manual.md#main-pars_header_140933605) nesta página e prepare os CSVs para migração de dados e conteúdo.

1. Faça logon no aplicativo Learning Manager como administrador de integração e clique em **[!UICONTROL Migração]** no painel esquerdo.

   A página inicial Projetos de migração é exibida. Se sua empresa tiver criado projetos de migração, você pode visualizar a lista de todos os projetos de migração nesta página.

1. Clique em **[!UICONTROL Novo]** no canto superior direito da página para criar um projeto de migração. Como alternativa, você pode clicar no link **[!UICONTROL Criar um projeto de migração]** da página para criar um projeto de migração. A página Criar um projeto de migração é exibida.

   Se você já não tiver criado uma pasta FTP, será solicitado que você crie uma pasta FTP na conta. Essa etapa é obrigatória para começar a criar um projeto de migração.

   ![](assets/create-project.png)
   *Criar pasta FTP*

   Forneça o nome do projeto, a etiqueta do projeto, o catálogo do curso e a descrição do seu projeto de migração. Clique em **[!UICONTROL Criar]**.

   Os itens de dados de migração são identificados usando essa etiqueta de projeto de migração. Se não tiver nenhum catálogo específico do curso, escolha o catálogo padrão na lista suspensa. Todos os cursos migrados usando um projeto de migração serão incluídos no catálogo escolhido nesse estágio. Se nenhum catálogo for escolhido, todos os cursos migrados farão parte do catálogo padrão.

1. A página de configuração do sprint é exibida conforme mostrada na seguinte captura de tela. Você deve criar um sprint como parte do projeto de migração. Escolha o nome do sprint e forneça uma breve descrição do sprint. Você pode escolher Sim se desejar migrar o conteúdo como parte desse sprint. Clique em **[!UICONTROL Avançar]**.

   ![](assets/users-modified-sprint.png)
   *Migração de sprint*

   Marque a caixa de seleção com o título **Os usuários foram adicionados ou modificados desde a última execução** para sincronizar a lista de usuários com o aplicativo Learning Manager. Se estiver migrando dados e conteúdo para o aplicativo Learning Manager, talvez isso não seja obrigatório. Mas, se houver um lapso de tempo entre a migração anterior do sprint em relação à migração mais recente, a prática recomendada é optar por sincronizar a lista de usuários. Essa etapa permite que o banco de dados do Learning Manager esteja em sincronia com os usuários do LMS.

   Essa etapa de sincronização é recomendada quando enrollment.csv e user_course_grade.csv são migrados. Essa etapa permite que o banco de dados do Learning Manager esteja em sincronia com o banco de dados de migração e garante que todos os usuários cujos registros a serem migrados no sprint estejam disponíveis no banco de dados de migração.

1. Você pode iniciar a migração do sprint com os dados e conteúdo carregados. Clique no link **[!UICONTROL Atualizar]** antes de iniciar a Execução do sprint para sincronizar as pastas FTP e Conteúdo com o aplicativo Learning Manager.

   ![](assets/sprint1-filesupload.png)
   *Iniciar migração do sprint*

   Clique em **[!UICONTROL Iniciar]** no canto superior direito da página. Você pode clicar em **[!UICONTROL Parar]** a qualquer momento durante o processo de migração do sprint para anular a migração do sprint.

   O status de migração é exibido em cada um dos itens de dados e conteúdo do sprint. Verifique o número de itens falhos e bem-sucedidos como parte da execução do sprint de migração.

   Se estiver carregando o conteúdo do módulo, certifique-se de que o caminho da pasta de conteúdo seja fornecido no module_version.csv. Se não realizar essa etapa, podem ocorrer erros durante a migração. Por exemplo, se estiver carregando o conteúdo de um módulo de ritmo individualizado como vídeos, você precisa especificar o caminho relativo do URL do Box no module_version.csv. Para o conteúdo do módulo de atividade, você pode especificar o nome do URL.

   É fornecida abaixo para referência a captura de tela da caixa de diálogo de andamento. Conforme mostrado na captura de tela, é possível ver o número de registros processados de cada item de dados de migração juntamente com o status de falha e êxito dos itens. Clique em Baixar registros de erro nos itens falhos para baixar e visualizar os registros de erro. É possível corrigir os problemas no CSV e carregá-lo novamente no FTP.

   ![](assets/sample-sprint-progress-status.png)
   *Exibir progresso do sprint*

   Clique na lista de sprints no painel esquerdo se quiser ver a lista de todos os sprints de um projeto de migração. Você pode exibir uma lista de todos os sprints, o número de execuções de cada sprint, a data de início, a duração e o status de conclusão, conforme mostrado na captura de tela abaixo.

   ![](assets/sprint-list.png)
   *Exibir lista de sprints*

1. Após carregar os CSVs atualizados mais recentes, você pode clicar em Re-executar no canto superior direito da página. A opção Re-executar processa novamente todos os itens de dados, ignorando os itens que não possuem alterações. Quando estiver satisfeito com a migração dos itens de dados em um sprint, você pode marcar a migração do sprint como concluída clicando no botão na parte superior da página. Você pode iniciar um novo sprint com mais itens de dados mais tarde. Quando um sprint está marcado como concluído, você não pode executá-lo novamente. Da mesma forma, em um projeto de migração, é possível ter qualquer número de sprints. Quando estiver satisfeito com o status de migração de todos os Sprints, você poderá marcar o projeto de migração como Concluído clicando no link **Marcar projeto como Concluído** na página Lista de Sprints.

   Antes de marcar o projeto de migração como concluído, você deve garantir que todos os sprints do projeto estejam completos. Depois de marcar o projeto de migração como concluído, você não poderá voltar atrás e nem criar sprints nem fazer qualquer modificação nesse projeto. Você precisa criar outro projeto de migração e adicionar sprints a ele.

## Verificação da migração {#registration}

Depois de migrar os dados e o conteúdo de aprendizado do LMS legado da sua empresa, você pode verificar os dados e o conteúdo importados usando vários recursos do objeto de aprendizado. Por exemplo, você pode fazer login no aplicativo Learning Manager como administrador e verificar a disponibilidade dos dados e do conteúdo dos módulos e cursos importados.

## Migração usando APIs

O Adobe Learning Manager (ALM) fornece um recurso de migração para assimilar dados ou conteúdo de sistemas externos, usado principalmente para migrar de plataformas LMS legadas.

No entanto, algumas organizações podem exigir que esse processo seja executado regularmente (por exemplo, durante a noite ou semanalmente), em vez de como uma importação única.

Como exemplo, você verá como um cliente fictício (NovaFX) se integra a um provedor externo fictício (SquareCorp) e automatiza migrações agendadas. A integração permite:

* Os cursos da SquareCorp aparecem como objetos de aprendizado no ALM para alunos da NovaFX.
* O NovaFX acompanha o progresso do aluno nos cursos hospedados pela SquareCorp diretamente no ALM.

### Requisitos de integração

A SquareCorp deve fornecer:

* Informações de metadados do curso: uma API para compartilhar metadados do curso à qual a NovaFX tem acesso.
* Informações de dados de progresso: uma API para compartilhar informações periódicas sobre o progresso e a conclusão do aluno.

### Definições de chave

* **Projeto ativo:** um projeto estará ativo se estiver “Em andamento” ou “Inicializado”.
* **Sprint ativo:** um sprint estará ativo se estiver “Em andamento” ou “Inicializado”.

### Automatizar a execução do sprint

Crie um aplicativo ou script que execute o seguinte em um cronograma:

1. Buscar metadados do curso, inscrições do usuário e notas do aluno na SquareCorp.
2. Gere os arquivos CSV.
3. Carregue os arquivos no Box ou FTP.
4. Acione o sprint usando as APIs de migração.

### Detalhes da API

#### Iniciar uma execução de migração

**Ponto de extremidade:** POST /primeapi/v2/bulkimport/startrun

Parâmetros:

* **lockaccount (booleano):** o parâmetro determina se a conta deve ser bloqueada no início da execução. Por padrão, é definido como falso. Recomenda-se que os usuários evitem usar esse parâmetro, a menos que haja um motivo válido para bloquear a conta.
* **catalogid (Inteiro):** Esse parâmetro permite selecionar o catálogo de destino durante a migração. Normalmente, é definido ao criar o projeto de migração, mas pode ser ajustado para execuções individuais. Quando a identificação do catálogo é alterada, os objetos de aprendizado adicionados em execuções futuras serão colocados no catálogo escolhido mais recentemente. Se for necessário voltar ao catálogo selecionado durante a criação do projeto de migração, isso também deverá ser especificado explicitamente.
* **migrationProjectId (Inteiro):** O parâmetro é necessário para disparar um projeto de migração específico quando várias execuções habilitadas por API estiverem habilitadas na conta.

#### Verificar se a sincronização pode começar

Verifique se o conteúdo pode ser sincronizado com a pasta do sprint. Não copie conteúdo ou arquivos de metadados para a pasta FTP, a menos que essa API retorne um objeto de resposta bem-sucedido.

**Ponto de extremidade:** GET /primeapi/v2/bulkimport/cansync

Parâmetros:

* **migrationProjectId (Inteiro)** O parâmetro é necessário para disparar um projeto de migração específico quando várias execuções habilitadas por API estiverem habilitadas na conta.

<b>Êxito na resposta</b>

```
{  
    "status": "OK",  
    "title": "BULKIMPORT_CAN_SYNC_NOW",  
    "source": {  
        "info": "Yes"  
    }  
} 
```

<b>Êxito na resposta</b>

```
{ 
    "status": "BAD_REQUEST", 
    "title": "BULKIMPORT_ERROR_CANNOT_SYNC", 
    "source": { 
        "info": "Error, No active projects" 
    } 
} 
```

<b>Possíveis respostas de API</b>

| Ação | Tipo | Mensagem |
| ------------------------------------- | ------- | ------------------------------------------------------------------------------------- |
| BULKIMPORT_RUN_INITIATED_SUCCESSFULLY | Êxito | Execução iniciada com êxito |
| BULKIMPORT_ERROR_CANNOT_INITATE_RUN | Erro | Uma execução está em andamento |
| BULKIMPORT_ERROR_CANNOT_INITATE_RUN | Erro | Há mais de um projeto ativo |
| BULKIMPORT_ERROR_CANNOT_INITATE_RUN | Erro | Há mais de um sprints |
| BULKIMPORT_ERROR_CANNOT_INITATE_RUN | Erro | Nenhum projeto ativo |
| BULKIMPORT_ERROR_CANNOT_INITATE_RUN | Erro | Nenhum sprints ativo |
| BULKIMPORT_ERROR_CANNOT_INITATE_RUN | Erro | O catálogo fornecido não é uma ID válida ou não pertence à conta principal |
| BULKIMPORT_CAN_SYNC_NOW | Informações | Sincronizar agora |
| BULKIMPORT_ERROR_CANNOT_SYNC | Erro | Uma execução está em andamento |
| BULKIMPORT_ERROR_CANNOT_SYNC | Erro | Há mais de um projeto ativo |
| BULKIMPORT_ERROR_CANNOT_SYNC | Erro | Há mais de um sprints |
| BULKIMPORT_ERROR_CANNOT_SYNC | Erro | Nenhum projeto ativo |
| BULKIMPORT_ERROR_CANNOT_SYNC | Erro | Nenhum sprints ativo |
| BULKIMPORT_ERROR_CANNOT_SYNC | Erro | Nenhum arquivo válido presente na pasta |

### Exemplo de fluxo de integração

1. Verifique a API cansync.
2. Gere e faça upload de arquivos CSV.
3. Acione o sprint usando a API startrun.
4. Monitore a resposta e manipule erros.

### Limitações

As APIs de migração não oferecem funcionalidade para verificar erros relacionados à migração diretamente no arquivo CSV de saída após a execução do sprint. No entanto, esses erros podem ser revisados como linhas no arquivo CSV ao acessar a interface do usuário do administrador de integração após uma execução de sprint.

### Verificação de migração por meio de APIs

A API de migração, `runStatus`, permite que os administradores de integração controlem o progresso das execuções de migração acionadas por meio da API.

A API `runStatus` também fornece um link direto para baixar logs de erros no formato CSV para execuções concluídas. O link de download permanece ativo por sete dias e os logs são mantidos por um mês.

**Exemplo de curva**

**Objetivo final**

```
GET /bulkimport/runStatus
```

**Parâmetros**

* **migrationProjectId**: (Obrigatório). Um identificador exclusivo para um projeto de migração. Um projeto de migração é usado para transferir dados e conteúdo de um sistema de gerenciamento de aprendizagem (LMS) existente para o Adobe Learning Manager. Cada projeto de migração pode consistir em vários sprints, que são unidades menores de tarefas de migração.

* **sprintId**: (obrigatório). Um identificador exclusivo de um sprint em um projeto de migração. Um sprint é um subconjunto de tarefas de migração que inclui itens de aprendizado específicos (por exemplo, cursos, módulos, registros do aluno) a serem migrados de um LMS existente para o Adobe Learning Manager. Cada sprint pode ser executado de forma independente, permitindo a migração em fases.

* **sprintRunId**: (Obrigatório). Um identificador exclusivo usado para rastrear a execução de um sprint específico em um projeto de migração. Está associado ao processo de migração real dos itens definidos em um sprint. O sprintRunId ajuda a monitorar, solucionar problemas e gerenciar o trabalho de migração.

**Resposta**

```
{
  "sprintId": 2510080,
  "sprintRunId": 2740845,
  "migrationProjectId": 2509173,
  "startTime": 1746524711052,
  "endTime": 1746524711052,
  [
    {
      "id": 2609923,
      "lastHeartbeatTime": 1746524711052,
      "objectName": "content",
      "jobState": "COMPLETED",
      "errorCsvLink": "",
      "errorLogLink": "migration/5830/2509173/2510080/2740845/content_err.csv",
      "sequenceNumber": 1
    },
    {
      "id": 2609922,
      "lastHeartbeatTime": 1746524713577,
      "objectName": "course",
      "jobState": "WAITING_IN_QUEUE",
      "errorCsvLink": "",
      "errorLogLink": null,
      "sequenceNumber": 2
    }
  ]
}
```

Além disso, a resposta da API `startRun` agora inclui a ID do projeto de migração, a ID do sprint e a ID de execução do sprint, que são necessárias para consultar o novo ponto de extremidade de status.

```
curl -X GET --header 'Accept: text/html' 'https://learningmanager.adobe.com/primeapi/v2/bulkimport/runStatus?migrationProjectId=001&sprintId=10001&sprintRunId=7'
```

Produz a seguinte resposta. A resposta contém:

* `migrationId`
* `sprintId`
* `sprintRunId`

**Resposta**

```
{
  "status": "OK",
  "title": "BULKIMPORT_RUN_INITIATED_SUCCESSFULLY",
  "source": {
    "info": "Success",
    "migrationInfo": {
      "migrationProjectId": "001",
      "sprintId": "10001",
      "sprintRunId": "7"
    }
  }
}
```

## Renovação na migração {#retrofittinginmigration}

Esse recurso de integração permite que você renove dados de um objeto de aprendizado originados em um sistema de gerenciamento de aprendizagem herdado em um curso ativo criado no Learning Manager.

Abaixo encontram-se as especificações CSV padrão que podem ser usadas para mapear os dados de migração do LMS existente. Clique em csv-specifications e sample-csvs para baixar os arquivos zip. O arquivo csv-specifications.zip baixado contém quatro arquivos de planilhas do Excel. Esses arquivos de planilha do Excel são especificações com descrições para que você entenda como preencher os arquivos .csv. Os arquivos .csv correspondentes devem conter os dados de cada campo no formato prescrito, conforme explicado nesses arquivos .xlsx.

1-enrollment.xlsx contém descrições dos metadados necessários do arquivo retrofit_enrollment.csv.

2-certification_enrollment.xlsx contém descrições dos metadados necessários do arquivo retrofit_certification_enrollment.csv.

3-learning_program_enrollment.xlsx contém descrições dos metadados necessários do arquivo retrofit_learning_program_enrollment.csv.

4-user_course_grades.xlsx-contém descrições de metadados necessários para o arquivo retrofit_user_course_grades.csv.
[csv-specifications.zip](assets/csv-specifications.zip)

>[!NOTE]
>
>UUID (Universally Unique Id) também é uma coluna no csv de migração.


## Solução de problemas de migração {#troubleshootingmigrationissues}

Consulte este [artigo](../../kb/troubleshooting-migration.md) para saber mais sobre a solução dos problemas enfrentados pelos administradores de integração ao migrar dados e conteúdo do LMS existente para o Learning Manager.

## Dicas para gerenciamento de usuários {#usermanagement}

Neste tópico, encontram-se algumas dicas para compreender como os usuários são analisados e gerenciados no Learning Manager. Esses conceitos poderiam ajudar você a gerenciar melhor os usuários ao usar a importação de CSV, os conectores e os recursos de migração do Learning Manager.

## IDs do Learning Manager {#captivateprimeids}

O Learning Manager fornece dois tipos de IDs exclusivas para usuários:

* ID de e-mail
* UUID (ID universalmente exclusiva)

O Learning Manager oferece suporte à UUID para proporcionar flexibilidade às empresas no controle de contas de usuários. Como administrador, se você tiver a UUID de usuários em uma conta, poderá modificar as IDs de e-mail dos usuários dessa conta.

**Contexto de uso da UUID em uma empresa**

Considere um cenário em que um funcionário A entra em uma empresa chamada Learning Manager, como contratado. Durante o período do contrato, a empresa do Learning Manager não pode fornecer a ID de e-mail da empresa como ```A@example.com```. Em vez disso, a empresa pode considerar apenas a conta de e-mail pessoal do funcionário, por exemplo, ```A@gmail.com```. Após concluir 6 meses do período do contrato, se o mesmo funcionário A ingressar no Learning Manager como funcionário em tempo integral, o Learning Manager poderá alterar a ID de e-mail para a ID de e-mail da empresa: ```A@example.com```.

Ter acesso da UUID à conta do usuário beneficiará o Learning Manager da empresa no cenário mencionado acima. A empresa do Learning Manager pode substituir facilmente a ID de e-mail pessoal do funcionário A por uma ID de e-mail oficial. Os registros de funcionário relevantes a essa conta não são afetados por essa alteração.

## ID de usuário único {#singleuseridentification}

O Learning Manager identifica e lembra como um único usuário é adicionado a ele, por exemplo, usando o autorregistro, o carregamento de CSV, ou um único usuário adicionado usando a interface do usuário ou por meio da API.

* Se um usuário único é adicionado usando a interface do usuário (IU) ou através da API, você pode excluir esse tipo de usuários únicos usando a IU ou através da API.
* Você pode atualizar os usuários únicos que usam o processo de carregamento de CSV, mas deve se lembrar de que esses usuários únicos são tratados como usuários do CSV e que os fluxos de trabalho do CSV são aplicáveis a esses usuários.

## Atribuindo a função de gerente {#assigningmanagerrole}

Não é possível atribuir diretamente a função de gerente a nenhum usuário no Learning Manager. Um usuário X pode se tornar um gerente do Learning Manager somente quando você definir o atributo Gerente de qualquer usuário (digamos, Y) nessa conta como X.

Em um contexto no qual X é o gerente dos usuários, por exemplo, A, B e C, se X sair da empresa, será necessário garantir que o atributo Gerente de A, B e C esteja definido para o novo gerente. Como alternativa, você também pode definir o atributo Gerente desses usuários como RAIZ temporariamente e atribuir o novo nome de gerente mais tarde.

Para obter mais informações sobre este tópico, consulte o seguinte conteúdo de Ajuda:

* [Perguntas frequentes sobre carregamento de CSVs](/help/migrated/administrators/feature-summary/add-users-user-groups.md#bulk-upload-internal-users/)
* [Ajuda do recurso sobre adição de usuários](/help/migrated/administrators/feature-summary/add-users-user-groups.md)
