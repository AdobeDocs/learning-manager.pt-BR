---
jcr-language: en_us
title: Guia de Implantação do Learning Manager - Seção 2
contentowner: sanm
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2232'
ht-degree: 0%

---



# Guia de Implantação do Learning Manager - Seção 2

## Configuração técnica {#technicalsetup}

A configuração técnica para sua conta do Learning Manager é necessária principalmente para usuários corporativos. Este documento fala sobre como configurar o Single Sign-On (logon único) para sua organização e integrar o Learning Manager com conectores de terceiros.

### Configurar o Single Sign-On {#configuresinglesignon}

Como administrador de sistema no Admin Console, uma das primeiras tarefas é definir e configurar um sistema de identidade com o qual os usuários finais serão autenticados. À medida que sua organização compra licenças para o Learning Manager, você precisará provisioná-las para seus usuários finais. E para isso, você precisará de uma maneira de autenticar esses usuários. Execute o procedimento a seguir para configurar o SSO para seus usuários.

1. Na página inicial do Learning Manager, clique em **[!UICONTROL ** Configurações **>** Métodos de logon **.]**

   ![](assets/configure-sso-step1.png)

1. Dependendo do tipo de usuário, selecione **[!UICONTROL ** Usuários internos **ou** Usuários Externos **.]**



1. No menu **[!UICONTROL **Logon**]**campo suspenso, selecione **[!UICONTROL ** Logon único **.]**

   ![](assets/configure-sso-step3.png)

1. Para definir as configurações de Single Sign-On, clique em **[!UICONTROL ** Alterar **.]**

   ![](assets/configure-sso-step4.png)

1. No menu ****[!UICONTROL URL de autenticação iniciada pelo IDP]**** digite o URL de autenticação fornecido pelo provedor de serviços.



   ![](assets/configure-sso-step5.png)

1. Clique em **[!UICONTROL **Carregar **]**ao lado do**[!UICONTROL  **Arquivo XML de Metadados do IDP **]******e faça upload do arquivo XML.
1. Clique em **[!UICONTROL ** Salvar **.]**
1. A autenticação SSO foi configurada com sucesso para sua conta. Você poderá fazer logon na sua conta do Learning Manager usando a autenticação SSO.

   ***O SSO que você configura no Learning Manager deve ser compatível com SAML 2.0.***

## Migração de dados do usuário {#migrationofuserdata}

Como administrador, quando sua empresa compra o Learning Manager, uma das etapas cruciais que você precisa executar é a migração. É essencial que você mova o conteúdo de treinamento e os dados do usuário existentes para o Learning Manager. O fluxo de trabalho de migração a seguir ajuda a aproveitar os benefícios do LMS moderno e intuitivo sem perder os dados herdados da sua organização.

O Learning Manager permite migrar do LMS existente por meio de um assistente passo a passo, em sprints iterativos. Você obtém uma visibilidade completa do status de cada sprint para garantir que os alunos não tenham nenhum tempo de inatividade ao migrar os dados herdados para o Adobe Learning Manager.

Para executar o fluxo de trabalho de migração, você precisa dos privilégios do administrador de integração. Como administrador, você pode assumir a função de administrador de integração ou atribuir essa função a outro usuário.

**Podemos pegar a ajuda do Shaleen para criar um visual.**

1. Pré-requisito
1. Avaliação do conteúdo existente e dos dados do usuário
1. Exportar e mapear os dados do LMS existente
1. Configurar pastas FTP e BOX para migração
1. Transferir os alunos para o Learning Manager
1. Transferir conteúdo de aprendizado para o Learning Manager
1. Transferir dados restantes para o Learning Manager



### Pré-requisito {#prerequisite}

Antes de iniciar o processo de migração, você deve executar o seguinte pré-requisito:

* Extração de dados e conteúdo do LMS vigente e transformação dos dados em formatos de arquivo, conforme definido pelo Learning Manager.
* Importação de usuários usando conectores FTP e BOX. O administrador de integração deve garantir que os conectores sejam configurados antes do processo de migração.



***É recomendável que os administradores testem o processo de migração em uma conta de teste antes de migrar os dados e o conteúdo para o ambiente de produção do Learning Manager. ***

### Avaliação e exportação de dados {#evaluatingandexportingdata}

O administrador de integração deve primeiro examinar os dados disponíveis no LMS atual. Como administrador de integração, você pode migrar apenas os seguintes objetos de aprendizado:

* Módulo
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
* Inscrições
* Inscrição de certificação
* Inscrição no programa de aprendizado
* Notas do curso do usuário



Depois de avaliar os dados existentes, você deve mapear esses dados com as especificações do CSV padrão no Learning Manager. Baixe o seguinte exemplo ***csv-specifications.zip*** arquivo que contém sete planilhas do excel necessárias para essa migração. Essas planilhas do Excel contêm especificações com descrições para entender como mapear os dados existentes com os campos nos arquivos .csv.

<!--
<Download link to the zip file>
-->

Verifique se cada arquivo .csv contém os dados de cada campo no formato prescrito:

<table> 
 <tbody> 
  <tr> 
   <th width="7%" valign="top"><p><strong>Não.</strong></p></th> 
   <th width="29%" valign="top"><p><strong>Nome da planilha do Excel</strong></p></th> 
   <th width="31%" valign="top"><p><strong>Descrição do conteúdo</strong></p></th> 
   <th width="31%" valign="top"><p><strong>Observações</strong></p></th> 
  </tr> 
  <tr> 
   <td><p>1</p></td> 
   <td><p>module.xlsx</p></td> 
   <td><p>Metadados para module.csv</p></td> 
   <td><p> </p></td> 
  </tr> 
  <tr> 
   <td><p>2</p></td> 
   <td><p>course.xlsx</p></td> 
   <td><p>Metadados para course.csv</p></td> 
   <td><p>Indique um nome de autor de um curso específico porque, às vezes, vários nomes de autor não são exibidos corretamente no aplicativo após a migração. </p></td> 
  </tr> 
  <tr> 
   <td><p>3</p></td> 
   <td><p>module_version.xlsx </p></td> 
   <td><p>Metadados para module_version.csv</p></td> 
   <td><p>Certifique-se de fornecer o caminho do URL da pasta da conta do Box na qual o conteúdo foi carregado. </p></td> 
  </tr> 
  <tr> 
   <td><p>4</p></td> 
   <td><p>course_instance.xlsx</p></td> 
   <td><p>Metadados para course_instance.csv </p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>5</p></td> 
   <td><p>course_module.xlsx</p></td> 
   <td><p>Metadados para course_module.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>6</p></td> 
   <td><p>skill.xlsx</p></td> 
   <td><p>Metadados para skill.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>7</p></td> 
   <td><p>skill_level.xlsx</p></td> 
   <td><p>Metadados para skill_level.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>8</p></td> 
   <td><p>skill_course.xlsx</p></td> 
   <td><p>Metadados para skill_course.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>9</p></td> 
   <td><p>Certification.xlsx</p></td> 
   <td><p>Metadados para Certification.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>10</p></td> 
   <td><p>certification_course.xlsx</p></td> 
   <td><p>Metadados para certification_course.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>11</p></td> 
   <td><p>certification_commit.xlsx</p></td> 
   <td><p>Metadados para certification_commit.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>12</p></td> 
   <td><p>learning_program.xlsx</p></td> 
   <td><p>Metadados para learning_program.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>13</p></td> 
   <td><p>learning_program_course.xls </p></td> 
   <td><p>Metadados para learning_program_course.csv </p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>14</p></td> 
   <td><p>learning_program_instance.xlsx </p></td> 
   <td><p>Metadados para learning_program_instance.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>15</p></td> 
   <td><p>learning_program_instance_course_instance.xlsx </p></td> 
   <td><p>Metadados para learning_program_instance_course_instance.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>16</p></td> 
   <td><p>enrollments.xlsx</p></td> 
   <td><p>Metadados para enrollments.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>17</p></td> 
   <td><p>certification_enrollment.xlsx</p></td> 
   <td><p>Metadados para certification_enrollment.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>18</p></td> 
   <td><p>learning_program_enrollment.xlsx</p></td> 
   <td><p>Metadados para learning_program_enrollment.csv</p></td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td><p>19</p></td> 
   <td><p>User_course_grade.xlsx</p></td> 
   <td><p>Metadados para User_course_grade.csv</p></td> 
   <td><p>Forneça os dados necessários de registros do aluno no arquivo .csv mesmo que não sejam obrigatórios. Sem essas informações, mesmo que o .csv seja processado para migração, o aplicativo Learning Manager pode não refletir nenhum dado. </p></td> 
  </tr> 
 </tbody> 
</table>

***O Learning Manager oferece suporte a valores de data e hora somente no formato UTF 8 e 32 bits. Você pode obter erros durante a migração se especificar a data em arquivos CSV com uma data fora do intervalo, como 2038-07-17T08:53:21.000Z ou 1980-04-17T08:13:25,322Z***

### Dependências ao importar dados para arquivos csv {#dependencieswhileimportingdatatocsvfiles}

Ao importar os dados existentes para o formato csv padrão, esteja ciente das seguintes dependências:

* module_version.csv depende de module.csv
* course_instance.csv depende de course.csv
* course_module.csv depende de course.csv, module.csv e module_version.csv
* course_instance.csv depende de course.csv
* enrollment.csv depende de course.csv
* user_course_grade.csv depende de course.csv e module.csv
* skill_course.csv depende de course.csv
* skill_level.csv depende de skill.csv
* learning_program_instance.csv depende do programa de aprendizado e learning_program_course.csv
* learning_program_course.csv depende de learning_program.csv
* learning_program_enrollment.csv depende do programa de aprendizado e learning_program_instance.csv
* learning_program_instance_course_instance.csv depende de learning_program.csv, learning_program_instance.csv e course_instance.csv
* certification_course.csv depende de certification.csv e course.csv
* certification_commit.csv depende de certification.csv e certification_course.csv
* certification_enrollment.csv depende de certification.csv, certification_course.csv e certification_enrollment.csv



Depois de exportar os dados, salve os arquivos .csv no computador local. Os arquivos agora estão prontos para serem removidos nas pastas FTP ou BOX.

## Configurar pastas FTP e BOX para a migração {#setupftpandboxfoldersforthemigration}

Antes de planejar e iniciar a migração real de todo o conteúdo, você deve configurar primeiro as pastas FTP e BOX. Você precisa dessas pastas para soltar os arquivos .csv nessas pastas. Quando o conteúdo herdado, na forma de arquivos .csv, estiver disponível nas pastas FTP e BOX, o Learning Manager poderá consumir os dados.

### Configurar uma conta FTP {#setupanftpaccount}

Na página inicial do administrador de integração, clique em **[!UICONTROL ** Solicitação de pasta FTP CSV **.]** Na caixa de diálogo pop-up exibida, insira sua ID de e-mail. Navegue pelo assistente online para criar a conta FTP do Exavault. Assim que criar sua conta, você poderá visualizar seu projeto de migração e as pastas do projeto de sprint no Exavault FTP.

Veja um instantâneo de amostra dos arquivos de projeto e da pasta do ExaVault conforme mostrado aqui:

![](assets/set-up-an-ftp-account.png)

Quando você configura a pasta FTP com sucesso, o sistema exibe a mensagem “A configuração da pasta FTP está concluída”.

## Configurar uma conta do BOX {#setupaboxaccount}

Para criar uma conta BOX e configurar uma pasta do BOX, execute as seguintes etapas:

Na página inicial do administrador de integração, selecione Migração.

Na seção Configuração, clique em Solicitar uma pasta do Box.

![](assets/set-up-a-box-account.png)

No menu ****[!UICONTROL Insira o e-mail]**** , insira a ID do e-mail onde você gostaria de receber as instruções de logon para se conectar ao Box.

Clique em **[!UICONTROL ** Conectar **.]**

Você receberá um email do Box com um link para a pasta compartilhada. Se você não tiver uma conta do Box, clique em Inscrever-se e crie uma conta. As instruções de logon são então enviadas à ID de e-mail do administrador de integração.

Depois de salvar a conexão, a página de migração exibirá a mensagem: “A configuração da pasta do Box está concluída”.

## Migração do conteúdo para o Learning Manager {#migratingthecontenttocaptivateprime}

Antes de iniciar a migração, é importante observar o seguinte:

* Somente um projeto de migração pode estar ativo em uma conta em qualquer momento específico. Em um projeto, somente um sprint pode estar ativo em um determinado momento no tempo.
* Não é possível desfazer uma execução que já está em andamento. No entanto, você pode usar a opção de exclusão existente em cada recurso do Learning Manager para desfazer qualquer migração de dados ou conteúdo.

Assim que o projeto de migração é iniciado, o projeto passa para o estado de &#39;Em migração&#39;. Nesse estado, nenhum outro usuário além do administrador de integração pode fazer logon no Learning Manager.

Carregar conteúdo de treinamento nas pastas de conteúdo:

Na página inicial do administrador de integração, clique em **[!UICONTROL Migração.]**

Na página inicial de migração, o sistema exibe os projetos de migração já criados em sua organização.

Clique em **[!UICONTROL **Novo**]**no canto superior direito da página, para criar um projeto de migração.

***Se você ainda não tiver criado uma pasta FTP, será solicitado que você crie uma conta do Exavault para a pasta FTP. Essa etapa é obrigatória antes de começar a criar um projeto de migração. ***

No menu ****[!UICONTROL Criar um novo projeto de migração]**** especifique o nome do seu projeto.

![](assets/migrating-the-content-1.png)

Especifique uma tag para seu projeto, o catálogo do curso e forneça uma descrição para o projeto de migração. Os itens de dados de migração são identificados usando a etiqueta de projeto de migração. Se você não tiver um catálogo específico do curso, escolha o catálogo padrão na lista suspensa. Todos os cursos que você migrar usando um projeto de migração serão incluídos no catálogo escolhido nessa etapa. Se nenhum catálogo for escolhido, todos os cursos migrados farão parte do catálogo padrão.

Clique em **[!UICONTROL Criar.]**

Na página Configuração do sprint, crie um sprint para seu projeto de migração. Um sprint, no processo de migração do Learning Manager, define um conjunto de itens de migração escolhido para ser migrado do LMS existente.

![](assets/migrating-the-content-2.png)

Especifique um nome para o sprint e forneça uma descrição para o sprint.

Selecione o ****[!UICONTROL Os usuários foram adicionados ou modificados desde a última caixa de seleção de execução]****, para sincronizar a lista de usuários com o aplicativo Learning Manager. Se estiver migrando dados e conteúdo para o aplicativo Learning Manager, talvez isso não seja necessário. Mas, se houver um lapso de tempo entre a migração anterior do sprint para a migração mais recente, é recomendável optar por sincronizar a lista de usuários. Essa etapa permite que o banco de dados do Learning Manager esteja em sincronia com os usuários do LMS.

***A etapa de sincronização é recomendada quando enrollment.csv e user_course_grade.csv são migrados. Essa etapa permite que o banco de dados do Learning Manager esteja em sincronia com o banco de dados de migração e garante que todos os usuários cujos registros a serem migrados no sprint estejam disponíveis no banco de dados de migração.***

Clique em **[!UICONTROL ** Próxima **.]**

Clique em **[!UICONTROL **Início**]**para iniciar a migração do sprint com os dados e o conteúdo carregados. Clique em ****[!UICONTROL Atualizar]**** antes de iniciar a Execução do sprint para sincronizar as pastas FTP e Conteúdo com o Learning Manager.

![](assets/migrating-the-content-3.png)

Clique em ****[!UICONTROL Parar]****a qualquer momento durante o processo de migração do sprint para abortar a migração do sprint.

O sistema exibe o status de migração em relação a cada um dos itens de dados e conteúdo do sprint. Verifique o número de itens falhos e bem-sucedidos como parte da execução do sprint de migração.

Se estiver carregando o conteúdo do módulo, certifique-se de que o caminho da pasta de conteúdo seja fornecido no arquivo *module_version.csv *file. Se não realizar essa etapa, podem ocorrer erros durante a migração. Por exemplo, se estiver carregando o conteúdo de um módulo de ritmo individualizado como vídeos, você precisa especificar o caminho relativo do URL do Box em *module_version.csv *file.

É fornecida abaixo para referência a captura de tela do andamento da migração. Conforme mostrado na captura de tela, você pode exibir o número de registros processados para cada item de dados de migração juntamente com o status de itens com êxito e com falha. Clique em Baixar registros de erros em relação aos itens com falha para baixar e exibir os registros de erros. Você pode corrigir os problemas no CSV e fazer upload novamente no FTP.

![](assets/migrating-the-content-4.png)

Para exibir a lista de todos os sprints de um projeto de migração, clique em **[!UICONTROL **Sprint**]**no painel de navegação à esquerda. Você pode exibir uma lista de todos os sprints, o número de execuções de cada sprint, a data de início, a duração e o status de conclusão, conforme mostrado na captura de tela abaixo.

![](assets/migrating-the-content-5.png)

Para exibir a lista de todos os sprints de um projeto de migração, clique em **[!UICONTROL **Sprint**]**no painel de navegação à esquerda. Você pode exibir uma lista de todos os sprints, o número de execuções de cada sprint, a data de início, a duração e o status de conclusão, conforme mostrado na captura de tela abaixo.

Para exibir a lista de todos os sprints de um projeto de migração, clique em **[!UICONTROL **Sprint**]**no painel de navegação à esquerda. Você pode exibir uma lista de todos os sprints, o número de execuções de cada sprint, a data de início, a duração e o status de conclusão, conforme mostrado na captura de tela abaixo.

***Antes de marcar o projeto de migração como concluído, certifique-se de que todos os sprints do projeto estejam concluídos. Depois de marcar o projeto de migração como concluído, você não poderá voltar e criar sprints nesse projeto. Não é possível fazer modificações nesse projeto. Você só pode criar outro projeto de migração e adicionar sprints a ele.***

Depois de migrar os dados e o conteúdo de aprendizado do LMS herdado da sua organização, verifique se os dados e o conteúdo foram importados corretamente. Você pode verificar fazendo logon como administrador e verificando a disponibilidade de módulos importados e dados e conteúdo de cursos

Para obter recursos úteis na migração, consulte:

* Solução de problemas de migração
* Perguntas frequentes sobre carregamento de CSVs

