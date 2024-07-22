---
description: Saiba como integrar o Salesforce com o Learning Manager usando conectores, como integrar um FTP com o Learning Manager e fazer upload de CSV automaticamente usando um conector FTP.
jcr-language: en_us
title: Conectores do Learning Manager
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '6293'
ht-degree: 71%

---



# Conectores do Learning Manager

Saiba como integrar o Salesforce com o Learning Manager usando conectores, como integrar um FTP com o Learning Manager e fazer upload de CSV automaticamente usando um conector FTP.

As empresas usam outros aplicativos e sistemas que precisam ser integrados com o Learning Manager. Os conectores são utilitários que ajudam a executar integrações baseadas em dados, como importar dados para o Learning Manager de sistemas externos ou exportar dados para sistemas externos do Learning Manager. Na versão de julho de 2016, os conectores tinham apenas a capacidade de importação em massa de usuários para o Learning Manager a partir de sistemas externos.

O Learning Manager fornece conectores do Salesforce e FTP. Usando o conector do Salesforce, os administradores de integração de uma empresa podem integrar o aplicativo Salesforce com o Learning Manager. Como integrador, você também pode usar o conector FTP para importar automaticamente um conjunto de usuários para o seu aplicativo corporativo.

O Learning Manager também fornece os conectores Lynda, getAbstract e Harvard Management System, que permitem que os alunos acessem e realizem cursos do Lynda.com, getAbstract e Harvard ManageMentor.

Continue lendo para saber como configurar e usar cada um desses conectores no Learning Manager.

![](assets/connectorslist.jpg)

## Conector do Salesforce {#sfconnector}

O conector do Salesforce conecta contas do Salesforce e do Learning Manager para automatizar a sincronização de dados. Os recursos do conector do Salesforce são os seguintes:

### Mapear atributos

O administrador de integração pode escolher colunas do Salesforce e mapeá-las para os atributos agrupáveis correspondentes do Learning Manager. Este é um esforço único. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário. Ele poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

### Importação automatizada de usuário

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no Salesforce e importe-os automaticamente para o Learning Manager. Esta automação evita o esforço manual de criar e carregar um CSV no Learning Manager.

### Agendamento automático

Usar os recursos automáticos de agendamento e importação de usuário em conjunto pode ser eficaz. O administrador do Learning Manager pode configurar o agendamento conforme as necessidades da organização. Os usuários podem ser atualizados no aplicativo Learning Manager conforme o agendamento. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

### Como filtrar usuários

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

## Configurar o conector do Salesforce {#configuresalesforceconnector}

Saiba mais sobre o processo de integração do Learning Manager com o Salesforce.

### Pré-requisitos {#prerequisites}

Certifique-se de que sua organização do Salesforce compartilhe um URL com você. Por exemplo, se o nome da organização é **myorg**, o URL do Salesforce pode ser [ https://myorg.salesforce.com](https://myorg.salesforce.com/). Esta é a única entrada necessária para conectar a conta do Salesforce ao Learning Manager.

Certifique-se também de possuir as credenciais apropriadas para fazer logon na conta.

## Criar uma conexão {#createaconnection}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do Salesforce. Será exibido um menu. Clique no item **[!UICONTROL Conectar]** no menu.

   ![](assets/mouserover-salesforce.png)

1. É exibida uma caixa de diálogo solicitando que você insira o URL da organização. Clique em **[!UICONTROL Conectar]** após fornecer a URL.
1. Após uma conexão bem-sucedida, a página de visão geral é exibida.

## Mapear atributos {#mapattributes}

Uma vez que a conexão é estabelecida com sucesso, você pode mapear as colunas do Salesforce para os atributos correspondentes do Learning Manager. Essa etapa é obrigatória.

1. No lado esquerdo da página de mapeamento você pode ver as colunas do Learning Manager e, no lado direito, as colunas do Salesforce. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   ![](assets/sfdc-map-columns.png)

   Os dados da coluna do Learning Manager mostrados no lado esquerdo são coletados dos campos ativos. O campo **gerente** deve necessariamente ser mapeado para um campo do tipo endereço de email. Antes de usar o conector, é necessário mapear todas as colunas.

1. Clique em **[!UICONTROL Salvar]** após concluir o mapeamento.
1. O conector está pronto para uso. A conta que foi configurada agora aparece como uma fonte de dados no aplicativo do administrador para que o administrador agende a importação ou sincronização sob demanda.

## Como usar o conector do Salesforce {#usingsalesforceconnector}

O conector do Salesforce se conecta ao Salesforce.com para buscar os usuários, como configurado, e adicioná-los ao Learning Manager.

## Conector FTP do Learning Manager {#ftpconnector}

Com o conector FTP, é possível integrar o Learning Manager com sistemas externos arbitrários para automatizar a sincronização dos dados. A expectativa é de que os sistemas externos possam exportar os dados em um formato CSV e colocá-los na pasta apropriada da conta FTP do Learning Manager. Os recursos do conector FTP são os seguintes:

Você também pode usar o conector do Box para migração de dados, importação de usuários e exportação de dados. Para mais informações, consulte o [conector do Box.](third-party-connectors.md#main-pars_header_302653946)

## Importação de dados {#dataimport}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no serviço FTP do Learning Manager e importe-os automaticamente para o Learning Manager. Com esse recurso, você pode integrar vários sistemas colocando o CSV gerado por eles nas pastas apropriadas das contas FTP. O Learning Manager pega os arquivos CSV, combina os arquivos e importa os dados conforme o agendamento. Consulte o recurso Agendamento para obter mais informações.

**Mapear atributos**

O administrador de integração pode escolher colunas de CSV e mapeá-las para os atributos agrupáveis do Learning Manager. Este mapeamento é uma tarefa única. Uma vez concluído o mapeamento, o mesmo mapeamento é usado em importações subsequentes do usuário. O mapeamento pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

## Exportar dados {#exportdata}

A Exportação de Dados permite que os usuários exportem as habilidades do usuário para um local do FTP para integrar com qualquer sistema de terceiros.

## Agendamento {#scheduling}

O administrador pode configurar tarefas de agendamento conforme os requisitos da organização, enquanto os usuários no aplicativo Learning Manager são atualizados conforme a agenda. Da mesma forma, o administrador de integração pode programar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

## Configurar o conector FTP do Learning Manager {#configurecaptivateprimeftpconnector}

Saiba mais sobre o processo de integração do Learning Manager com o conector FTP.

### Criar uma conexão {#Createaconnection-1}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do FTP. Será exibido um menu. Clique no item **[!UICONTROL Conectar]** no menu.

   ![](assets/mouseover-ftpconnector.png)

1. É exibida uma caixa de diálogo solicitando que você insira a ID de e-mail. Forneça a ID de e-mail da pessoa responsável por gerenciar a conta FTP do Learning Manager da organização. Clique em **[!UICONTROL Conectar]** após fornecer a ID de email.
1. O Learning Manager envia um e-mail solicitando que o usuário redefina a senha antes de acessar o FTP pela primeira vez. O usuário deve redefinir a senha e usá-la para acessar a conta FTP do Learning Manager.

   Somente uma conta FTP do Learning Manager pode ser criada para uma determinada conta do Learning Manager.

   Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha que ação você quer executar entre as seguintes opções:

   * Importar usuários internos
   * Exportar habilidades de usuário - Configurar um agendamento
   * Exportar habilidades de usuário - Sob demanda

   ![](assets/connectors-overview.png)

## Importar

+++Usuário interno

A opção importar usuário interno permite que você agende a geração de relatórios de importação de usuário automaticamente. Os relatórios gerados são enviados como arquivos .CSV.

+++

+++Mapear atributos

Depois que uma conexão é estabelecida com êxito, você pode mapear as colunas dos arquivos CSV que serão colocados na pasta do FTP para os atributos correspondentes do Learning Manager. Essa etapa é obrigatória.

1. No lado esquerdo da página Mapear atributos você pode ver as colunas esperadas do Learning Manager e, no lado direito, os nomes das colunas CSV. Inicialmente, no lado direito, você verá uma caixa de seleção em branco. Importe qualquer modelo CSV clicando em **Escolher Arquivo**.
1. A etapa acima preenche a lista suspensa de seleção do lado direito com todos os nomes de colunas CSV. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   *O campo Gerente deve necessariamente ser mapeado para um campo do tipo endereço de email. Antes de usar o conector, é necessário mapear todas as colunas.*

1. Clique em **[!UICONTROL Salvar]** após concluir o mapeamento.

   O conector está pronto para uso. A conta recém-configurada aparecerá agora como uma fonte de dados no aplicativo do administrador para que o administrador agende a importação ou sincronização sob demanda.



+++

+++Utilização do conector FTP do Learning Manager

1. Os arquivos CSV de sistemas externos devem ser colocados no seguinte caminho:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Observação:** na versão de julho de 2016, é permitido importar somente usuários. Portanto, para usar o conector FTP, você deve garantir que os arquivos CSV sejam colocados na seguinte pasta:

   `code Home/import/user/internal/*.csv`

1. O conector FTP ocupa todas as linhas dos arquivos CSV, por isso é importante que a linha correspondente a um usuário em um CSV não apareça em nenhum outro CSV.
1. Todos os CSVs devem conter as colunas especificadas no mapeamento.
1. Todos os CSVs necessários devem estar presentes na pasta antes do início do processo.

Ao importar usuários para o Learning Manager, o administrador também precisa saber como os usuários são gerenciados no Learning Manager. Consulte a [Ajuda do Gerenciamento de Usuários](../integration-admin/feature-summary/migration-manual.md#usermanagement) para obter mais informações.

+++

## Exportar

+++Habilidades

Há duas opções para exportar relatórios de habilidades do usuário.

**[!UICONTROL Habilidades do usuário - Sob demanda]**: você pode especificar a data de início e exportar o relatório usando a opção .O relatório será extraído da data inserida até a presente.

![](assets/user-skills-on-demand.png)

**[!UICONTROL Habilidades do usuário - Configurar]**: esta opção permite que você agende a extração do relatório. Selecione a caixa de seleção Ativar agendamento e especifique a data e a hora de início. Também é possível especificar o intervalo no qual deseja que o relatório seja gerado e enviado.

![](assets/user-skills-configure.png)

+++

Para abrir a pasta Exportar em que os arquivos exportados serão colocados no local FTP, abra o link para Pasta FTP fornecido na página Habilidades do usuário, conforme mostrado abaixo.

![](assets/ftp-folder.png)

Os arquivos exportados automaticamente estarão presentes no local **Início/exportação/&#42;FTP_location&#42;**

Os arquivos exportados automaticamente estarão disponíveis com o título **skill_conquistas_&#42;data &#42;_a_&#42;data&#42;.csv**

![](assets/exported-csvs.png)

## Conector do Lynda {#lyndaconnector}

O conector do Lynda pode ser usado por clientes empresariais do lynda.com que querem que seus alunos descubram e realizem os cursos do Lynda dentro do Learning Manager. O conector pode ser configurado para obter periodicamente cursos do site Lynda.com com sua chave de API. Depois que um curso é criado no Learning Manager, ele pode ser pesquisado e realizado pelos usuários. O progresso do aluno pode ser acompanhado no Learning Manager.

### Configurar o conector do Lynda {#configurethelyndaconnector}

1. No painel integrado do administrador, clique em Lynda.

   Você verá o quadro com três opções: Introdução, Conexão e Gerenciar conexões.

1. Se você estiver configurando o conector do Lynda pela primeira vez, clique em Conexão.

   Você deve configurar a conta do Exavault FTP antes de configurar este conector.

1. Na página de conexão, especifique um nome para o conector. Insira a chave do aplicativo e a chave secreta da sua conexão.

   Você deve entrar em contato com o seu fornecedor para obter a chave do aplicativo e a chave secreta.

1. Clique em Salvar.

   A configuração é salva e a conexão do Lynda à sua conta é adicionada. Agora você pode clicar em Gerenciar conexões na página Início e editar sua configuração a qualquer momento.

1. Se já tiver uma conexão estabelecida, clique em Gerenciar conexões para ver todas as conexões.

   O recurso de migração da sua conta deve ser habilitado antes de configurar este conector.

1. Clique na conexão que quer editar.
1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar esta conta.
   * Clique em Editar e edite suas credenciais. Clique em Redefinir para desfazer as atualizações neste campo.
   * Clique em Habilitar agendamento para agendar a sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, ativar a sincronização a cada 3 dias.

   Clique em Salvar para salvar as alterações.

   ![](assets/lynda.png)

1. No painel esquerdo, clique em Execução sob demanda. Essa opção permite que você importe feeds do usuário e outros dados relevantes do Lynda. Insira a data de início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados a partir da data de início até o presente serão importados.

   * Você pode clicar em Desabilitar acesso ao Learning Manager durante a execução, quando o aplicativo terá um tempo de inatividade durante a sincronização.
   * Se clicar em Habilitar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

   ![](assets/lynda-ondemand.png)

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

   ![](assets/lynda-executionstatus.png)

## Conector do getAbstract {#getabstractconnector}

O conector getAbstract pode ser usado pelos clientes empresariais do site getAbstract.com que desejam que os alunos descubram e façam os resumos do getAbstract. Este conector pode ser configurado para obter periodicamente dados de uso, com base nos registros de conclusão do aluno criados no Learning Manager. Continue lendo para saber como configurar este conector no Learning Manager.

### Configurar o conector do getAbstract {#configurethegetabstractconnector}

1. No painel integrado do administrador, clique em getAbstract.

   No quadro, você verá três opções: Introdução, Conexão e Gerenciar conexões.

1. Se estiver configurando o conector do getAbstract pela primeira vez, clique em Conectar.

   Você deve configurar a conta do Exavault FTP antes de configurar este conector.

   Certifique-se de compartilhar estas credenciais de FTP com seu provedor de conteúdo para acessar os feeds.

1. Insira um nome para a conexão no campo Nome da conexão.

   Insira as chaves apropriadas nos campos ID do cliente e Segredo do cliente. Talvez você terá que entrar em contato com o fornecedor para obter as chaves apropriadas para esse conector.

   As chaves são necessárias para obter os metadados dos cursos realizados pelo cliente.

1. Se já tiver uma conexão estabelecida, na página inicial, clique em getAbstract > Gerenciar conexões para visualizar e editar a configuração atual.

   O recurso de migração da sua conta deve ser habilitado antes de configurar este conector.

1. Clique na conexão cuja configuração que você deseja exibir ou editar.

   ![](assets/getabstractschedulepage.png)

1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar esta conta.
   * Clique em Editar e edite suas credenciais. Clique em Redefinir para desfazer as atualizações neste campo.
   * Clique em Habilitar agendamento para agendar a sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, ativar a sincronização a cada 3 dias.

1. Clique em Salvar.

   A configuração é salva e a conexão getAbstract para sua conta é adicionada.

1. No painel esquerdo, clique em Execução sob demanda. Essa opção permite que você importe feeds do usuário e outros dados relevantes do getAbstract. Insira a data de início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados a partir da data de início até o presente serão importados.

   * Você pode clicar em Desabilitar acesso ao Learning Manager durante a execução, quando o aplicativo terá um tempo de inatividade durante a sincronização.
   * Se clicar em Habilitar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

   Para que qualquer tipo de sincronização funcione, você deve certificar-se de que o feed do usuário esteja presente na pasta FTP do getAbstract para as datas especificadas na sincronização.

   Veja a planilha Excel a seguir, que é um arquivo de feed do usuário de amostra do getAbstract. O nome do arquivo deve seguir o formato:** report_export_yyyy_MM_dd_HHmmss.xlsx** ou **report_export_yyyy_MM_dd.xlsx**.
   [folha do Excel de exemplo de feed de usuário getAbstract](assets/report-export-20170401175342.xlsx)

## Conector do Harvard ManageMentor {#hmmconnector}

O conector Harvard ManageMentor pode ser usado pelos clientes empresariais do site Harvard ManageMentor que desejam que os alunos descubram e façam os cursos do Harvard ManageMentor. O conector ajuda a criar cursos no Learning Manager e pode ser configurado para obter periodicamente dados de progresso do aluno. Para configurar esse conector, execute o seguinte procedimento:

### Configurar o conector do Harvard ManageMentor {#configuretheharvardmanagermentorconnector}

1. No painel integrado do administrador, clique em Harvard ManageMentor.

   No quadro, você verá três opções: Introdução, Conexão e Gerenciar conexões.

1. Se estiver configurando o conector do Harvard ManageMentor pela primeira vez, clique em Conectar.

   Você também deve configurar a conta do Exavault FTP antes de configurar este conector.

   Certifique-se de compartilhar estas credenciais de FTP com seu provedor de conteúdo para acessar os feeds.

1. No campo Nome da conexão, insira um nome para a conexão. Clique em Conectar para salvar esta conexão.
1. Se já tiver uma conexão estabelecida, na página inicial, clique em Harvard ManageMentor > Gerenciar conexões. Clique na conexão que deseja editar para editar sua configuração existente.

   O recurso de migração da sua conta deve ser ativado antes de configurar este conector.

   ![](assets/hmm.png)

1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar esta conta.
   * Clique em Habilitar agendamento para agendar a sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, ativar a sincronização a cada 3 dias.

1. No painel esquerdo, clique em Execução sob demanda. Essa opção permite que você importe feeds do usuário e outros dados relevantes do Harvard ManageMentor. Insira a data de início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados a partir da data de início até o presente serão importados para esta conexão.

   * Você pode clicar em Desabilitar acesso ao Learning Manager durante a execução, quando o aplicativo terá um tempo de inatividade durante a sincronização.
   * Se clicar em Habilitar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

   Se quiser automatizar a sincronização para que ocorra a cada poucos dias, especifique o número de dias no campo Não número de dias. A sincronização garante que sua conta seja atualizada com a versão mais recente dos sumários e resumos do Harvard ManageMentor.

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

   Para que a sincronização seja bem sucedida, você deve certificar-se de que pelo menos um dos seguintes arquivos estão presentes na pasta FTP do Harvard ManageMentor:

   hmm12_metadata.xlsx: este arquivo fornece os metadados do curso para o conector do Harvard ManageMentor. Certifique-se de ter seguido a convenção de nomenclatura ao carregar o arquivo.

   client_hmm12_20150125.xlsx: este o feed do usuário do conector do Harvard ManageMentor. A convenção de nomenclatura do arquivo que você deve seguir é **client_hmm12_yyyyMMdd.xlsx.**

   Veja os dois seguintes arquivos de amostra a seguir do feed do usuário e do feed do curso deste conector:
   [Arquivo de metadados do curso para o conector Harvard ManageMentor](assets/hmm12-metadata.xlsx) [Feed do usuário para o conector Harvard ManageMentor](assets/client-hmm12-20170304.xlsx)

## Conector do Workday {#workdayconnector}

Com o conector do Workday, você pode integrar o Learning Manager com o inquilino do Workday para automatizar a sincronização dos dados.

### Importar

#### Mapear atributos

O administrador de integração pode escolher colunas do Workday e mapeá-las para os atributos agrupáveis correspondentes do Learning Manager. Este é um esforço único. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário. Ele poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

#### Importação automatizada de usuário

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no Workday e importe-os automaticamente para o Learning Manager.

#### Como filtrar usuários

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

## Exportar

A exportação das habilidades do usuário permite que os usuários exportem habilidades para o Workday automaticamente.

Não é possível exportar habilidades de várias contas do Learning Manager simultaneamente usando a mesma conta do Workday.

## Agendamento {#Scheduling-1}

O administrador pode configurar tarefas de agendamento conforme os requisitos da organização, enquanto os usuários no aplicativo Learning Manager são atualizados conforme a agenda. Da mesma forma, o administrador de integração pode programar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

## Configurar o conector do Workday {#configureworkdayconnector}

**Pré-requisitos**: solicite ao administrador do Workday da sua organização que crie um usuário do sistema de integração (ISU, na sigla em inglês) com as permissões, conforme definido no documento ISU_Permissions. Baixe uma cópia do link abaixo.
[Baixe uma cópia da segurança do usuário do sistema de integração (ISU).](assets/isu-permissions-v1.pdf) Saiba mais sobre o processo de integração do Learning Manager com o conector do Workday.

1. Na página inicial do Learning Manager, passe o mouse sobre o bloco do Workday. Será exibido um menu. Clique no item **[!UICONTROL Conectar]** no menu.

   ![](assets/workday-tile.png)

1. Uma caixa de diálogo é exibida, solicitando que você insira as credenciais da nova conexão. Veja a seguir os campos que você precisa inserir antes de estabelecer a conexão.

   * Nome da conexão: forneça um nome de conexão de sua preferência.
   * URL do host: o administrador de integração pode obter os detalhes do URL do host do administrador do Workday correspondente.
   * Locatário: o locatário é interno à sua empresa. O administrador do Workday fornecerá os detalhes de inquilino.
   * Nome de usuário e senha: o administrador do Workday cria um usuário de sistema integrado (ISU) com os privilégios de segurança necessários e o compartilha com o administrador de integração.

   Aviso: o Learning Manager usa a versão 28.1 da API do Workday.

   ![](assets/configure-connector.png)

1. Clique em conectar após digitar as informações em todos os campos relevantes.

   Também é possível ter várias conexões do Workday sincronizadas com sua conta do Learning Manager.

Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha que ação você quer executar entre as seguintes opções:

* Importar usuários internos
* Exportar habilidades de usuário - Configurar um agendamento
* Exportar habilidades de usuário - Sob demanda

![](assets/overview.png)

## Importar

### Mapear atributos {#MapAttributes-1}

Você pode usar o conector do Workday para integrar o Learning Manager e o Workday à sincronização automática de dados. É possível importar todos os usuários ativos do Workday para o Learning Manager. Os usuários podem ser importados de várias fontes de dados, incluindo FTP e Salesforce.

Os atributos do usuário do Learning Manager e do Workday precisam ser mapeados antes de importar usuários. Na página de visão geral, use a opção Usuários internos, em Importar, para fornecer os atributos do mapa.

Insira as credenciais do Adobe Learning Manager abaixo da coluna Adobe Learning Manager. Use os menus suspensos para selecionar as credenciais corretas para as colunas abaixo do Workday.

Atualmente, o Learning Manager é compatível com a importação de 44 atributos de usuário do Workday. Adicione atributos adicionais usando os Campos ativos no Learning Manager.

![](assets/map-attributes.png)

O Workday tem quatro níveis de hierarquia, enquanto o Learning Manager tem dois níveis. Os quatro níveis no Workday são categoria de perfil de habilidade, perfil de habilidade, categoria de item de habilidade e item de habilidade. Seu nome de habilidade e nível do Learning Manager juntos serão mapeados no Workday sob o item de habilidade.

+++Lista de atributos Workday compatíveis

wd:User_ID\
wd:Worker_ID\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Nome_Formatado\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Nome_Formatado\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.@wd:Endereço_Formatado\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Postal_Code\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Country_Region_Descriptor\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Telefone_Formatado\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Country_ISO_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:International_Phone_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Phone_Number\
wd:Personal_Data.wd:Primary_Nationality_Reference.wd:ID.1.$\
wd:Personal_Data.wd:Gender_Reference.wd:ID.1$\
wd:Personal_Data.wd:Identification_Data.wd:National_ID.0.wd:National_ID_Data.wd:ID\
wd:Personal_Data.wd:Identification_Data.wd:Custom_ID.0.wd:Custom_ID_Data.wd:ID\
wd:User_Account_Data.wd:Default_Display_Language_Reference.wd:ID.1.$\
wd:Role_Data.wd:Organization_Role_Data.wd:Organization_Role.0.wd:Organization_Role_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Position_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Name\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.@wd:Endereço_Formatado\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Classification_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Group_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Work_Space__Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Status_Data.wd:Ative\
wd:Employment_Data.wd:Worker_Status_Data.wd:Ative_Status_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Original_Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirado\
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Terminado\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$\
wd:Qualification_Data.wd:Education.0.wd:School_Name\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Company\
wd:Management_Chain_Data.wd:Worker_Supervisors_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID

+++

## Exportar

Você pode exportar todas as habilidades obtidas por um usuário do Learning Manager para o Workday. Observe que apenas habilidades ativas do usuário são exportadas. O Learning Manager não exporta habilidades retiradas. Também é possível conectar várias contas do Learning Manager ao mesmo conector do Workday. Caso os nomes de habilidades sejam os mesmos em duas contas do Learning Manager, eles serão mapeados para a mesma habilidade no Workday. É recomendável atualizar os nomes das habilidades em todas as contas do Learning Manager antes de atualizar a habilidade no Workday, caso duas contas do Learning Manager estejam usando a mesma conta do Workday.

+++Habilidades de usuário - Configurar

Essa opção permite que você agende a extração do relatório. Certifique-se de que a caixa de seleção Ativar exportação de habilidade do usuário usando esta caixa de seleção de conexão esteja ativada. Selecione a caixa de seleção Ativar agendamento e especifique a data e a hora de início. Também é possível especificar o intervalo no qual deseja que o relatório seja gerado e enviado. Selecione a caixa de seleção Ativar agendamento e digite a Data de início, Hora e Repetir após “n” número de dias. Uma vez concluído, clique em Salvar.

![](assets/configure-schedule.png)

+++

+++Habilidades do usuário - Sob demanda

Você pode especificar a data de início e exportar o relatório usando a opção. O relatório será extraído da data inserida até o presente. Insira a data a partir da qual você quer gerar o relatório e clique em Executar.

![](assets/on-demand-report.png)

+++

+++Habilidades do usuário - Status da execução

Aqui, você pode ver o resumo de todas as tarefas e obter o relatório de status delas. você pode baixar relatórios de erro clicando no link do relatório de erro.

![](assets/execution-status.png)

+++

## Conector do miniOrange {#miniorangeconnector}

Com o conector do miniOrange, você pode integrar o Learning Manager com o inquilino do miniOrange para automatizar a sincronização de dados.

### Importar

#### Mapear atributos

O administrador de integração pode escolher atributos do miniOrange e mapeá-los para os atributos agrupáveis correspondentes do Learning Manager. Este é um esforço único. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário. Ele poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

#### Importação automatizada de usuário

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no miniOrange e importe-os automaticamente para o Learning Manager.

#### Como filtrar usuários

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

Para configurar   miniOrange   entre em contato com a equipe de CSM do Learning Manager.

## Configurar o conector do miniOrange {#configureminiorangeconnector}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão laranja. Será exibido um menu. Clique na opção **[!UICONTROL Conectar]** no menu.

   ![](assets/miniorange-tile.png)

1. Clique em Conectar para configurar uma nova conexão. A página do conector do miniOrange é exibida. Insira os detalhes da conta que você deseja mapear.

   ![](assets/establish-connection.png)

1. Se desejar importar o usuário do miniOrange diretamente como um usuário interno do Learning Manager, use a opção **[!UICONTROL Importar usuários internos]**.

   ![](assets/import-users.png)

1. Na página de mapeamento, à esquerda   lado, você pode ver as colunas do Learning Manager e, à direita,   lado você pode ver as colunas do miniOrange. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   ![](assets/map-attributes.png)

1. Para ver e editar a Fonte de dados, como um administrador, clique em **[!UICONTROL Configurações > Fonte de dados]**.

   A fonte estabelecida do miniOrange seria listada. Se você precisar editar o filtro, clique em **[!UICONTROL Editar]**.

   ![](assets/data-source.png)

1. Você receberá uma notificação após a conclusão da importação. Para ver ou editar o registro de importação, clique em **[!UICONTROL Usuários > Importar registro.]**

### Excluir uma conexão {#deleteaconnection}

Siga estas etapas para excluir uma conexão miniOrange estabelecida.

## Conector do BlueJeans {#bluejeansconnector}

Agora você pode integrar o Learning Manager com o conector do BlueJeans e usar o BlueJeans para hospedar classes. O BlueJeans permite iniciar chamadas de áudio e videoconferência, bate-papos por vídeo e webinars.

Siga estas etapas para configurar e usar o conector.

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão BlueJeans. Será exibido um menu. Clique na opção **[!UICONTROL Conectar]** no menu.

   ![](assets/miniorange.png)

1. A página do conector do BlueJeans é aberta. Insira os detalhes da sua conta nos respectivos campos para integrar o Learning Manager e o BlueJeans para sincronização do feed do usuário. Você pode obter os detalhes com o administrador da sua conta do BlueJeans.

   ![](assets/bluejeans-connecotrpage.png)

   Como aluno, ao ativar o conector, use a mesma ID de e-mail usada em sua conta do Learning Manager para ativar feeds do usuário no Learning Manager.

1. Depois que a conexão é estabelecida, como autor, crie um curso de sala de aula virtual usando o BlueJeans como sistema de conferência.

   ![](assets/conferencing-systems.png)

1. Administradores, gerentes e alunos podem inscrever alunos no curso criado. Ao ser inscrito, o aluno receberá um e-mail. O aluno pode fazer logon na sua conta do Learning Manager para visualizar os detalhes do programa e realizar o curso.
1. Quando o curso é concluído, o relatório de conclusão é enviado para o Learning Manager. O administrador pode visualizar o relatório de conclusão para verificar a participação e pontuação dos alunos.

   ![](assets/-attendence-and-scoringreport.png)

## Conector do Box {#boxconnector}

Com o conector do BOX, é possível integrar o Learning Manager com sistemas externos arbitrários para automatizar a sincronização dos dados. A expectativa é de que os sistemas externos possam exportar os dados em um formato CSV e colocá-los na pasta apropriada da conta do Box do Learning Manager. Os recursos do conector Box são os seguintes:

Você também pode usar o conector FTP para migração de dados, importação de usuários e exportação de dados. Para mais informações, consulte [Conector FTP do Learning Manager.](third-party-connectors.md#main-pars_header_1427405935)

## Importação de dados {#DataImport-1}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no serviço do Box do Learning Manager e importe-os automaticamente para o Learning Manager. Com esse recurso, você pode integrar vários sistemas colocando o CSV gerado por eles nas pastas apropriadas das contas do Box. O Learning Manager pega os arquivos CSV, combina os arquivos e importa os dados conforme o agendamento. Consulte o recurso Agendamento para obter mais informações.

**Mapear atributos**

O administrador de integração pode escolher colunas de CSV e mapeá-las para os atributos agrupáveis do Learning Manager. Este mapeamento é uma tarefa única. Uma vez concluído o mapeamento, o mesmo mapeamento é usado em importações subsequentes do usuário. O mapeamento pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

## Exportação de dados {#dataexport}

A exportação de dados permite que os usuários exportem habilidades do usuário para um local do Box para serem integrados a qualquer sistema de terceiros.

## Agendar relatórios {#schedulereports}

O administrador pode configurar tarefas de agendamento conforme os requisitos da organização, enquanto os usuários no aplicativo Learning Manager são atualizados conforme a agenda. Da mesma forma, o administrador de integração pode programar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

## Configurar o conector do Box {#configureboxconnector}

Conheça o processo de integração do Learning Manager com o conector do Box.

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do Box. Será exibido um menu. Clique no item Conectar no menu.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

1. É exibida uma caixa de diálogo solicitando que você insira a ID de e-mail. Forneça a ID de e-mail da pessoa responsável por gerenciar a conta do Box do Learning Manager da organização. Após fornecer a ID de e-mail, clique em Conectar.

1. O Learning Manager envia um e-mail solicitando que o usuário redefina a senha antes de acessar o Box pela primeira vez. O usuário deve redefinir a senha e usá-la para acessar a conta do Box do Learning Manager.

   Somente uma conta do Box do Learning Manager pode ser criada para uma determinada conta do Learning Manager.

   Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha que ação você quer executar entre as seguintes opções:

   * Importar usuários internos
   * Exportar habilidades de usuário - Configurar um agendamento
   * Exportar habilidades de usuário - Sob demanda

## Importar

+++Usuário interno

A opção importar usuário interno permite que você agende a geração de relatórios de importação de usuário automaticamente. Os relatórios gerados são enviados como arquivos .CSV.

+++

+++Mapear atributos

Depois que uma conexão é estabelecida com sucesso, você pode mapear as colunas dos arquivos CSV que serão colocados na pasta do Box para os atributos correspondentes do Learning Manager. Essa etapa é obrigatória.

1. Na página Mapear atributos, à esquerda   lado, você pode ver as colunas esperadas do Learning Manager e, à direita,   Ao lado, você pode ver os nomes das colunas CSV. Inicialmente, no lado direito, você verá uma caixa de seleção em branco. Importe qualquer modelo CSV clicando em Escolher arquivo.

1. A etapa acima preenche a lista suspensa de seleção do lado direito com todos os nomes de colunas CSV. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   *O campo Gerente deve necessariamente ser mapeado para um campo do tipo endereço de email. Antes de usar o conector, é necessário mapear todas as colunas.*

1. Clique em Salvar após concluir o mapeamento.

   O conector está pronto para uso. A conta recém-configurada aparecerá agora como uma fonte de dados no aplicativo do administrador para que o administrador agende a importação ou sincronização sob demanda.

+++

+++Utilização do conector do Box do Learning Manager

1. Os arquivos CSV de sistemas externos devem ser colocados no seguinte caminho:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Observação:** na versão de julho de 2016, é permitido importar somente usuários. Portanto, para usar o conector do Box, você deve garantir que os arquivos CSV sejam colocados na seguinte pasta:\
   `code Home/import/user/internal/*.csv`

1. O conector do Box ocupa todas as linhas dos arquivos CSV, por isso é importante que a linha correspondente a um usuário em um CSV não apareça em nenhum outro CSV.
1. Todos os CSVs devem conter as colunas especificadas no mapeamento.
1. Todos os CSVs necessários devem estar presentes na pasta antes do início do processo.

Ao importar usuários para o Learning Manager, o administrador também precisa saber como os usuários são gerenciados no Learning Manager. Consulte a [Ajuda do Gerenciamento de Usuários](../integration-admin/feature-summary/migration-manual.md#usermanagement) para obter mais informações.

+++

## Exportar

+++Habilidades

Há duas opções para exportar relatórios de habilidades do usuário.

Habilidades do Usuário - Sob Demanda: Você pode especificar a data de início e exportar o relatório usando a opção. O relatório será extraído da data informada até a presente

**[!UICONTROL Habilidades do usuário - Configurar]**: esta opção permite que você agende a extração do relatório. Selecione a caixa de seleção Ativar agendamento e especifique a data e a hora de início. Também é possível especificar o intervalo no qual deseja que o relatório seja gerado e enviado.

+++

Para abrir a pasta Exportar em que os arquivos exportados serão colocados no local do Box, abra o link para a Pasta do Box fornecida na página Habilidades do usuário, conforme mostrado abaixo.

Os arquivos exportados automaticamente estarão presentes no local **Home/export/&#42;Box_location&#42;**

Os arquivos exportados automaticamente estarão disponíveis com o título **skill_conquistas_&#42;data &#42;_a_&#42;data&#42;.csv**

As permissões de acesso e o conteúdo na pasta do Box compartilhada pela equipe do Learning Manager devem ser gerenciados pelo cliente.  Observe também que o conteúdo da pasta seria armazenado fisicamente na região de Frankfurt.

## Conector do LinkedInLearning {#linkedinlearningconnector}

O conector do LinkedInLearning pode ser usado por clientes empresariais do LinkedIn.com que querem que os alunos descubram e realizem cursos do Learning Manager. O conector pode ser configurado para buscar cursos periodicamente com sua chave de API. Depois que um curso é criado no Learning Manager, ele pode ser pesquisado e realizado pelos usuários. O progresso do aluno pode ser acompanhado no Learning Manager.

### Configurar o conector do LinkedIn {#configurelinkedinconnector}

1. No painel integrado do administrador, clique em LinkedInLearning.

   Você verá o quadro com três opções: Introdução, Conexão e Gerenciar conexões.

1. Se estiver configurando o conector do LinkedInLearning pela primeira vez, clique em Conectar.

   Você deve configurar a conta do Exavault FTP antes de configurar este conector.

1. Na página de conexão, especifique um nome para o conector. Insira a chave do aplicativo e a chave secreta da sua conexão.

   Entre em contato com o fornecedor para obter a chave do aplicativo e a chave secreta.

1. Clique em Salvar.

   A configuração é salva e a conexão do LinkedinLearning para sua conta é adicionada. Agora você pode clicar em Gerenciar conexões na página Início e editar sua configuração a qualquer momento.

1. Se já tiver uma conexão estabelecida, clique em Gerenciar conexões para ver todas as conexões.

   O recurso de migração da sua conta deve ser habilitado antes de configurar este conector.

1. Clique na conexão que quer editar.
1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar esta conta.
   * Clique em Editar e edite suas credenciais. Clique em Redefinir para desfazer as atualizações neste campo.
   * Clique em Habilitar agendamento para agendar a sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, ativar a sincronização a cada 3 dias.

   Clique em Salvar para salvar as alterações.

1. No painel esquerdo, clique em Execução sob demanda. Essa opção permite importar feeds do usuário e outros dados relevantes do LinkedIn. Informe a Data de Início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados a partir da data de início até o presente serão importados.

   * Você pode clicar em Desabilitar acesso ao Learning Manager durante a execução, quando o aplicativo terá um tempo de inatividade durante a sincronização.
   * Se clicar em Habilitar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

