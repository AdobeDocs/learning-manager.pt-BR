---
description: Saiba como integrar o Salesforce com o Learning Manager usando conectores, como integrar FTP com o Learning Manager e carregar CSV automaticamente usando o conector FTP.
jcr-language: en_us
title: Conectores do Learning Manager
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '6293'
ht-degree: 0%

---



# Conectores do Learning Manager

Saiba como integrar o Salesforce com o Learning Manager usando conectores, como integrar FTP com o Learning Manager e carregar CSV automaticamente usando o conector FTP.

As empresas têm outros aplicativos e sistemas que talvez precisem ser integrados ao Learning Manager. Os conectores são utilitários que ajudam a executar integrações baseadas em dados, como importar dados para o Learning Manager de sistemas externos ou exportar dados para sistemas externos do Learning Manager. Na versão de julho de 2016, os conectores têm apenas a capacidade de importar usuários em massa para o Learning Manager de sistemas externos.

O Learning Manager fornece conectores do Salesforce e FTP. Usando o conector do Salesforce, os administradores de integração de uma empresa podem integrar o aplicativo Salesforce com o Learning Manager. Como integrador, você também pode usar o conector FTP para importar automaticamente um conjunto de usuários para o seu aplicativo corporativo.

O Learning Manager também fornece os conectores Lynda, getAbstract e Harvard Management System, que permitem que os alunos acessem e realizem cursos de Lynda.com, getAbstract e Harvard ManageMentor.

Leia para saber como configurar e usar cada um desses conectores no Learning Manager.

![](assets/connectorslist.jpg)

## Conector do Salesforce {#sfconnector}

O conector do Salesforce conecta contas do Salesforce e do Learning Manager para automatizar a sincronização de dados. Os recursos do conector do Salesforce são os seguintes:

### Mapear atributos

O administrador de integração pode escolher colunas do Salesforce e mapeá-las para os atributos agrupáveis correspondentes do Learning Manager. Este é um esforço único. Uma vez que o mapeamento é concluído, o mesmo mapeamento é usado em importações subsequentes do usuário. Ele pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

### Importação automatizada de usuários

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no Salesforce e importe-os automaticamente para o Learning Manager. Essa automação evita o esforço manual de criar e carregar um CSV no Learning Manager.

### Programação Automática

O uso do recurso de agendamento automático junto com o recurso de importação automatizada de usuários pode ser eficaz. O administrador do Learning Manager pode configurar o agendamento de acordo com as necessidades da organização. Os usuários podem ser atualizados no aplicativo Learning Manager conforme o agendamento. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

### Filtrar usuários

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

## Configurar o conector do Salesforce {#configuresalesforceconnector}

Conheça o processo para integrar o Learning Manager com o Salesforce.

### Pré-requisitos {#prerequisites}

Certifique-se de que sua organização do Salesforce esteja presente. Por exemplo, se o nome da sua organização for **myorg**, o URL do Salesforce pode ser [https://myorg.salesforce.com](https://myorg.salesforce.com/). Esta é a única entrada necessária para conectar a conta do Salesforce ao Learning Manager.

Verifique também se você tem as credenciais apropriadas para fazer logon na conta.

## Criar uma conexão {#createaconnection}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do Salesforce. Um menu é exibido. Clique em **[!UICONTROL Conectar]** item no menu.

   ![](assets/mouserover-salesforce.png)

1. Uma caixa de diálogo é exibida, solicitando que você insira o org-url. Clique em **[!UICONTROL Conectar]** depois de fornecer o URL.
1. Após a conexão bem-sucedida, a página de visão geral é exibida.

## Mapear atributos {#mapattributes}

Uma vez que a conexão é estabelecida com sucesso, você pode mapear as colunas do Salesforce para os atributos correspondentes do Learning Manager. Esta etapa é obrigatória.

1. No lado esquerdo da página de mapeamento você pode ver as colunas do Learning Manager e, no lado direito, as colunas do Salesforce. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   ![](assets/sfdc-map-columns.png)

   Os dados da coluna do Learning Manager mostrados no lado esquerdo são coletados dos campos ativos. O **gerente** o campo deve necessariamente ser mapeado para um campo do tipo endereço de email. Antes de usar o conector, é necessário mapear todas as colunas.

1. Clique em **[!UICONTROL Salvar]** após concluir o mapeamento.
1. O conector está pronto para uso. A conta que foi configurada agora aparece como uma fonte de dados no aplicativo do administrador, para que o administrador agende a importação ou para sincronização por demanda.

## Uso do conector do Salesforce {#usingsalesforceconnector}

O conector do Salesforce se conecta a Salesforce.com para buscar os usuários, conforme configurado, e adicioná-los ao Learning Manager.

## Conector FTP do Learning Manager {#ftpconnector}

Com o conector FTP, é possível integrar o Learning Manager com sistemas externos arbitrários para automatizar a sincronização dos dados. A expectativa é de que os sistemas externos possam exportar os dados em um formato CSV e colocá-los na pasta apropriada da conta FTP do Learning Manager. Os recursos do conector FTP são os seguintes:

Você também pode usar o conector do Box para migração de dados, importação de usuários e exportação de dados. Para obter mais informações, consulte [Conector Box.](third-party-connectors.md#main-pars_header_302653946)

## Importação de dados {#dataimport}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no serviço FTP do Learning Manager e importe-os automaticamente para o Learning Manager. Com esse recurso, você pode integrar vários sistemas colocando o CSV gerado por eles nas pastas apropriadas das contas FTP. O Learning Manager pega os arquivos CSV, combina os arquivos e importa os dados conforme o agendamento. Consulte o recurso Agendamento para obter mais informações.

**Mapear atributos**

O administrador de integração pode escolher colunas de CSV e mapeá-las para os atributos agrupáveis do Learning Manager. Este mapeamento é uma tarefa única. Depois que o mapeamento é concluído, o mesmo mapeamento é usado em importações subsequentes do usuário. O mapeamento pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

## Exportar dados {#exportdata}

A exportação de dados permite que os usuários exportem suas habilidades para um local de FTP para integração com qualquer sistema de terceiros.

## Programação {#scheduling}

O administrador pode configurar tarefas de agendamento de acordo com os requisitos da organização, e os usuários no aplicativo Learning Manager são atualizados de acordo com o agendamento. Da mesma forma, o administrador de integração pode agendar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

## Configurar o conector FTP do Learning Manager {#configurecaptivateprimeftpconnector}

Conheça o processo de integração do Learning Manager com o conector FTP.

### Criar uma conexão {#Createaconnection-1}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do FTP. Um menu é exibido. Clique em **[!UICONTROL Conectar]** item no menu.

   ![](assets/mouseover-ftpconnector.png)

1. Uma caixa de diálogo é exibida solicitando que você insira a ID de e-mail. Forneça a ID de e-mail da pessoa responsável por gerenciar a conta FTP do Learning Manager da organização. Clique em **[!UICONTROL Conectar]** depois de fornecer a id de email.
1. O Learning Manager envia um e-mail solicitando que o usuário redefina a senha antes de acessar o FTP pela primeira vez. O usuário deve redefinir a senha e usá-la para acessar a conta FTP do Learning Manager.

   Somente uma conta FTP do Learning Manager pode ser criada para uma determinada conta do Learning Manager.

   Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha a ação que deseja executar a partir das seguintes opções:

   * Importar usuários internos
   * Exportar habilidades de usuário - Configurar um agendamento
   * Exportar habilidades do usuário - OnDemand

   ![](assets/connectors-overview.png)

## Importar

+++Usuário interno

A opção de importar usuário interno permite agendar a geração do relatório de importação do usuário automaticamente. Os relatórios gerados são enviados a você como arquivos .CSV.

+++

+++Mapear atributos

Uma vez que a conexão é estabelecida com sucesso, você pode mapear as colunas dos arquivos CSV que serão colocados na pasta FTP para os atributos correspondentes do Learning Manager. Esta etapa é obrigatória.

1. No lado esquerdo da página Mapear atributos você pode ver as colunas esperadas do Learning Manager e, no lado direito, os nomes das colunas CSV. Inicialmente, no lado direito, você verá uma caixa de seleção vazia. Importe qualquer modelo CSV clicando em **Escolher arquivo**.
1. A etapa acima preenche a lista suspensa de seleção do lado direito com todos os nomes de colunas CSV. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   *O campo Gerente deve necessariamente ser mapeado para um campo do tipo endereço de e-mail. Antes de usar o conector, é necessário mapear todas as colunas.*

1. Clique em **[!UICONTROL Salvar]** após concluir o mapeamento.

   O conector está pronto para uso. A conta recém-configurada agora aparecerá como uma fonte de dados no aplicativo do administrador para que o administrador agende a importação ou a sincronização por demanda.



+++

+++Utilização do conector FTP do Learning Manager

1. Os arquivos CSV de sistemas externos devem ser colocados no seguinte caminho:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Observação:** Na versão de julho de 2016, é permitido importar somente usuários. Portanto, para usar o conector FTP, você deve garantir que os arquivos CSV sejam colocados na seguinte pasta:

   `code Home/import/user/internal/*.csv`

1. O conector FTP ocupa todas as linhas dos arquivos CSV, por isso é importante que a linha correspondente a um usuário em um CSV não apareça em nenhum outro CSV.
1. Todos os CSVs devem conter as colunas especificadas no mapeamento.
1. Todos os CSVs necessários devem estar presentes na pasta antes do início do processo.

Ao importar usuários para o Learning Manager, o administrador também precisa saber como os usuários são gerenciados no Learning Manager. Consulte [Ajuda do Gerenciamento de Usuários](../integration-admin/feature-summary/migration-manual.md#usermanagement) para saber mais informações.

+++

## Exportar

+++Habilidades

Há duas opções para exportar relatórios de habilidades do usuário.

**[!UICONTROL Habilidades do usuário - Sob demanda]**: Você pode especificar a data de início e exportar o relatório usando a opção .O relatório será extraído da data inserida até a presente.

![](assets/user-skills-on-demand.png)

**[!UICONTROL Habilidades do usuário - Configurar]**: Essa opção permite agendar a extração do relatório. Marque a caixa de seleção Ativar programação e especifique a data e a hora de início. Você também pode especificar o intervalo no qual deseja que o relatório seja gerado e enviado.

![](assets/user-skills-configure.png)

+++

Para abrir a pasta Exportar em que os arquivos exportados serão colocados no local FTP, abra o link para Pasta FTP fornecido na página Habilidades do usuário, conforme mostrado abaixo.

![](assets/ftp-folder.png)

Os arquivos exportados automaticamente estarão presentes no local **Home/export/&#42;FTP_location&#42;**

Os arquivos exportados automaticamente estarão disponíveis com o título, **skill_veries_&#42;data de &#42;_até_&#42;data - até&#42;.csv**

![](assets/exported-csvs.png)

## Conector do Lynda {#lyndaconnector}

O conector do Lynda pode ser usado por clientes empresariais do Lynda.com que querem que os alunos descubram e realizem os cursos do Lynda no Learning Manager. O conector pode ser configurado para obter periodicamente cursos do site Lynda.com com sua chave de API. Depois que um curso é criado no Learning Manager, os usuários podem pesquisá-lo e consumi-lo. O progresso do aluno pode ser acompanhado no Learning Manager.

### Configurar o conector do Lynda {#configurethelyndaconnector}

1. No painel do administrador integrado, clique em Lynda.

   Você verá o bloco com três opções: Introdução, Conectar e Gerenciar Conexões.

1. Se estiver configurando o conector do Lynda pela primeira vez, clique em Conectar.

   Configure a conta FTP do Exavault antes de configurar este conector.

1. Na página de conexão, especifique um nome para o conector. Insira a chave de aplicativo e a chave secreta da sua conexão.

   Entre em contato com o fornecedor para obter a chave de aplicativo e a chave secreta.

1. Clique em Salvar.

   A configuração será salva e a conexão do Lynda da sua conta será adicionada. Agora você pode clicar em Gerenciar conexões na página Início e editar sua configuração a qualquer momento.

1. Se você já tiver uma conexão estabelecida, clique em Gerenciar conexões para exibir todas as conexões.

   O recurso de migração deve ser habilitado para sua conta antes de você configurar esse conector.

1. Clique na conexão que deseja editar.
1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes da sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar essa conta.
   * Clique em Editar e edite suas credenciais. Clique em Redefinir para desfazer as atualizações neste campo.
   * Clique em Ativar Programação para programar sua sincronização. Você pode inserir a data e a hora de início e, em seguida, inserir a frequência da programação da sincronização em dias. Por exemplo, habilitar a sincronização a cada 3 dias.

   Clique em Salvar para salvar as alterações.

   ![](assets/lynda.png)

1. No painel esquerdo, clique em Execução sob demanda. Esta opção permite importar feeds do usuário e outros dados relevantes do Lynda. Informe a Data de Início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados desde a data de início até a data presente são importados.

   * Você pode clicar em Desativar acesso ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se você clicar em Ativar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

   ![](assets/lynda-ondemand.png)

1. Você também pode clicar em Status de execução no painel esquerdo a qualquer momento para exibir o resumo de todas as execuções deste conector, em ordem cronológica. Você pode exibir a data de início e a duração da sincronização, o tipo de sincronização (seja por demanda) e o status da sincronização (seja em andamento ou concluída).

   Quando você exclui e recria uma conexão, as execuções anteriores do conector aparecem novamente. Você pode exibir todas as execuções antes de excluir a conexão.

   Você pode executar uma nova execução somente para a sincronização mais recente.

   ![](assets/lynda-executionstatus.png)

## conector getAbstract {#getabstractconnector}

O conector getAbstract pode ser usado por clientes empresariais de getAbstract.com, que querem que seus alunos descubram e consumam resumos getAbstract. O conector pode ser configurado para obter periodicamente dados de uso, com base nos registros de conclusão do aluno criados no Learning Manager. Leia para saber como configurar este conector no Learning Manager.

### Configurar o conector getAbstract {#configurethegetabstractconnector}

1. No painel do administrador integrado, clique em getAbstract.

   No bloco, você verá três opções: Introdução, Conectar e Gerenciar Conexões.

1. Se você estiver configurando o conector getAbstract pela primeira vez, clique em Conectar.

   Configure a conta FTP do Exavault antes de configurar este conector.

   Compartilhe as credenciais de FTP com o provedor de conteúdo para acessar os feeds.

1. Digite um nome para a conexão no campo Nome da conexão.

   Insira as chaves apropriadas nos campos ID do cliente e Segredo do cliente. Talvez seja necessário entrar em contato com o fornecedor para obter as chaves apropriadas para esse conector.

   As chaves são necessárias para obter os metadados dos cursos consumidos pelo cliente.

1. Se você já tiver uma conexão estabelecida, na página Início, clique em getAbstract > Gerenciar conexões para exibir e editar a configuração existente.

   O recurso de migração deve ser habilitado para sua conta antes de você configurar esse conector.

1. Clique na conexão cuja configuração você deseja exibir ou editar.

   ![](assets/getabstractschedulepage.png)

1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes da sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar essa conta.
   * Clique em Editar e edite suas credenciais. Clique em Redefinir para desfazer as atualizações neste campo.
   * Clique em Ativar Programação para programar sua sincronização. Você pode inserir a data e a hora de início e, em seguida, inserir a frequência da programação da sincronização em dias. Por exemplo, habilitar a sincronização a cada 3 dias.

1. Clique em Salvar.

   A configuração é salva e a conexão getAbstract da sua conta é adicionada.

1. No painel esquerdo, clique em Execução sob demanda. Esta opção permite importar feeds do usuário e outros dados relevantes de getAbstract. Informe a Data de Início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados desde a data de início até a data presente são importados.

   * Você pode clicar em Desativar acesso ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se você clicar em Ativar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

1. Você também pode clicar em Status de execução no painel esquerdo a qualquer momento para exibir o resumo de todas as execuções deste conector, em ordem cronológica. Você pode exibir a data de início e a duração da sincronização, o tipo de sincronização (seja por demanda) e o status da sincronização (seja em andamento ou concluída).

   Quando você exclui e recria uma conexão, as execuções anteriores do conector aparecem novamente. Você pode exibir todas as execuções antes de excluir a conexão.

   Você pode executar uma nova execução somente para a sincronização mais recente.

   Para que qualquer tipo de sincronização funcione, você deve garantir que o feed de usuário esteja presente na pasta FTP getAbstract para as datas especificadas na sincronização.

   Consulte a seguinte planilha do Excel, que é um exemplo de arquivo de feed do usuário de getAbstract. O nome do arquivo deve seguir o formato:** report_export_yyyy_MM_dd_HHmmss.xlsx** ou **report_export_yyyy_MM_dd.xlsx**.
   [folha do excel de amostra do feed do usuário getAbstract](assets/report-export-20170401175342.xlsx)

## Conector do Harvard ManageMentor {#hmmconnector}

O conector Harvard ManageMentor pode ser usado por clientes empresariais do Harvard ManageMentor, que querem que seus alunos descubram e consumam cursos do Harvard ManageMentor. O conector ajuda a criar cursos no Learning Manager e pode ser configurado para obter periodicamente dados de progresso do aluno. Para configurar esse conector, execute o seguinte procedimento:

### Configurar o conector do Harvard ManagerMentor {#configuretheharvardmanagermentorconnector}

1. No painel do administrador integrado, clique em Harvard ManageMentor.

   No bloco, você verá três opções: Introdução, Conectar e Gerenciar Conexões.

1. Se estiver configurando o conector do Harvard ManageMentor pela primeira vez, clique em Conectar.

   Você também deve configurar a conta FTP do Exavault antes de configurar esse conector.

   Compartilhe as credenciais de FTP com o provedor de conteúdo para acessar os feeds.

1. No campo Nome da conexão, insira um nome para a conexão. Clique em Conectar para salvar esta conexão.
1. Se já tiver uma conexão estabelecida, na página Início, clique em Harvard ManageMentor > Gerenciar conexões. Clique na conexão que deseja editar para editar a configuração existente.

   O recurso de migração deve ser habilitado para sua conta antes de você configurar esse conector.

   ![](assets/hmm.png)

1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes da sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar essa conta.
   * Clique em Ativar Programação para programar sua sincronização. Você pode inserir a data e a hora de início e, em seguida, inserir a frequência da programação da sincronização em dias. Por exemplo, habilitar a sincronização a cada 3 dias.

1. No painel esquerdo, clique em Execução sob demanda. Essa opção permite importar feeds do usuário e outros dados relevantes do Harvard ManageMentor. Informe a Data de Início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados desde a data de início até a data presente são importados para esta conexão.

   * Você pode clicar em Desativar acesso ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se você clicar em Ativar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

   Se você quiser automatizar a sincronização a cada poucos dias, especifique o número de dias no campo Repetir Número de Dias. A sincronização garante que a sua conta seja atualizada com a versão mais recente dos resumos e resumos do Harvard ManageMentor.

1. Você também pode clicar em Status de execução no painel esquerdo a qualquer momento para exibir o resumo de todas as execuções deste conector, em ordem cronológica. Você pode exibir a data de início e a duração da sincronização, o tipo de sincronização (seja por demanda) e o status da sincronização (seja em andamento ou concluída).

   Quando você exclui e recria uma conexão, as execuções anteriores do conector aparecem novamente. Você pode exibir todas as execuções antes de excluir a conexão.

   Você pode executar uma nova execução somente para a sincronização mais recente.

   Para que a sincronização seja bem-sucedida, você deve garantir que pelo menos um dos seguintes arquivos esteja presente na pasta Harvard ManageMentor FTP:

   hmm12_metadata.xlsx: Esse arquivo fornece os metadados do curso para o conector Harvard ManageMentor. Certifique-se de seguir a convenção de nomenclatura ao fazer upload do arquivo.

   client_hmm12_20150125.xlsx: este é o feed de usuário para o conector Harvard ManageMentor. A convenção de nomeação de arquivo que você deve seguir é **client_hmm12_yyyyMMdd.xlsx.**

   Consulte os dois arquivos de amostra de feed do usuário e de feed do curso a seguir para este conector:
   [Arquivo de metadados do curso para o conector Harvard ManageMentor](assets/hmm12-metadata.xlsx) [Feed do usuário para o conector do Harvard ManageMentor](assets/client-hmm12-20170304.xlsx)

## Conector do Workday {#workdayconnector}

Usando o conector do Workday, você pode integrar o Learning Manager com o locatário da Workday para automatizar a sincronização de dados.

### Importar

#### Mapear atributos

O administrador de integração pode escolher colunas do Workday e mapeá-las para os atributos agrupáveis correspondentes do Learning Manager. Este é um esforço único. Uma vez que o mapeamento é concluído, o mesmo mapeamento é usado em importações subsequentes do usuário. Ele pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

#### Importação automatizada de usuários

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no Workday e importe-os automaticamente para o Learning Manager.

#### Filtrar usuários

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

## Exportar

A exportação de habilidades do usuário permite que os usuários exportem habilidades do usuário automaticamente para o Workday.

Não é possível exportar habilidades de várias contas do Learning Manager simultaneamente usando a mesma conta da Workday.

## Programação {#Scheduling-1}

O administrador pode configurar tarefas de agendamento de acordo com os requisitos da organização, e os usuários no aplicativo Learning Manager são atualizados de acordo com o agendamento. Da mesma forma, o administrador de integração pode agendar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

## Configurar o conector do Workday {#configureworkdayconnector}

**Pré-requisito**: solicite ao administrador do Workday de sua organização que crie um usuário do sistema de integração (ISU) com as permissões conforme definido no documento ISU_Permissions. Baixe uma cópia do link abaixo.
[Baixe uma cópia da segurança do ISU (Integration System User).](assets/isu-permissions-v1.pdf) Conheça o processo de integração do Learning Manager com o conector do Workday.

1. Na página inicial do Learning Manager, passe o mouse sobre o bloco do Workday. Um menu é exibido. Clique em **[!UICONTROL Conectar]** item no menu.

   ![](assets/workday-tile.png)

1. É exibida uma caixa de diálogo solicitando que você insira as credenciais da nova conexão. Veja a seguir os campos que você precisa inserir antes de estabelecer a conexão.

   * Nome da conexão: forneça um nome de conexão de acordo com sua preferência.
   * URL do host: o administrador de integração pode obter os detalhes do URL do host do administrador correspondente do Workday.
   * Locatário: o locatário é interno à sua empresa. O administrador do Workday fornecerá os detalhes do locatário.
   * Nome de usuário e senha: o administrador do Workday cria um usuário de sistema integrado (ISU) com os privilégios de segurança necessários e o compartilha com o administrador de integração.

   Observação: o Learning Manager usa a versão 28.1 da API do Workday.

   ![](assets/configure-connector.png)

1. Clique em conectar depois de inserir informações em todos os campos relevantes.

   Também é possível ter várias conexões Workday sincronizadas com sua conta do Learning Manager.

Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha a ação que deseja executar a partir das seguintes opções:

* Importar usuários internos
* Exportar habilidades de usuário - Configurar um agendamento
* Exportar habilidades do usuário - OnDemand

![](assets/overview.png)

## Importar

### Mapear atributos {#MapAttributes-1}

Você pode usar o conector do Workday para integrar o Learning Manager e o Workday e automatizar a sincronização de dados. Você pode importar todos os usuários ativos do Workday para o Learning Manager. Os usuários podem ser importados de várias fontes de dados, incluindo FTP e Salesforce.

Os atributos do usuário do Learning Manager e do Workday precisam ser mapeados antes de importar usuários. Na página Visão geral, use a opção Usuários internos, em Importar, para fornecer os atributos do mapa.

Insira as credenciais do Adobe do Learning Manager abaixo da coluna Adobe do Learning Manager. Use os menus suspensos para selecionar as credenciais corretas para as colunas no Workday.

Atualmente, o Learning Manager suporta a importação de 44 atributos de usuário do Workday. Adicione atributos adicionais usando os Campos ativos no Learning Manager.

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

Você pode exportar todas as habilidades obtidas por um usuário do Learning Manager para o Workday. Observe que apenas todas as habilidades ativas do usuário são exportadas e o Learning Manager não exporta habilidades retiradas. Também é possível conectar várias contas do Learning Manager ao mesmo conector do Workday. Caso os nomes de habilidades sejam os mesmos em duas contas do Learning Manager, eles serão mapeados para a mesma habilidade no Workday. É recomendável atualizar os nomes das habilidades em todas as contas do Learning Manager antes de atualizar a habilidade no Workday, caso duas contas do Learning Manager estejam usando a mesma conta do Workday.

+++Habilidades de usuário - Configurar

Essa opção permite programar a extração do relatório. Verifique se a caixa de seleção Habilitar exportação de habilidades do usuário usando esta conexão está ativada. Marque a caixa de seleção Ativar programação e especifique a data e a hora de início. Você também pode especificar o intervalo no qual deseja que o relatório seja gerado e enviado. Marque a caixa de seleção Ativar programação e informe a Data inicial, a Hora e a Repetição após o número &#39;n&#39; de dias. Uma vez concluído, clique em Salvar.

![](assets/configure-schedule.png)

+++

+++Habilidades do usuário - Sob demanda

Você pode especificar a data de início e exportar o relatório usando a opção. O relatório será extraído da data inserida até a presente. Informe a data a partir da qual deseja começar a gerar o relatório e clique em Executar.

![](assets/on-demand-report.png)

+++

+++Habilidades do usuário - Status da execução

Aqui, você pode exibir o resumo de todas as Tarefas e obter seus relatórios de status. você pode baixar relatórios de erros clicando no link relatório de erros.

![](assets/execution-status.png)

+++

## conector miniOrange {#miniorangeconnector}

Usando o conector do miniOrange, você pode integrar o Learning Manager com o inquilino do miniOrange para automatizar a sincronização de dados.

### Importar

#### Mapear atributos

O administrador de integração pode escolher atributos do miniOrange e mapeá-los para os atributos agrupáveis correspondentes do Learning Manager. Este é um esforço único. Uma vez que o mapeamento é concluído, o mesmo mapeamento é usado em importações subsequentes do usuário. Ele pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

#### Importação automatizada de usuários

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no miniOrange e importe-os automaticamente para o Learning Manager.

#### Filtrar usuários

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

Para configurar o conector do miniOrange, entre em contato com a equipe de CSM do Learning Manager.

## Configurar o conector do miniOrange {#configureminiorangeconnector}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão laranja. Um menu é exibido. Clique em  **[!UICONTROL Conectar]** no menu.

   ![](assets/miniorange-tile.png)

1. Clique em Conectar para estabelecer uma nova conexão. A página do conector do miniOrange é exibida. Insira os detalhes da conta que você deseja mapear.

   ![](assets/establish-connection.png)

1. Se desejar importar o usuário do miniOrange diretamente como um usuário interno do Learning Manager, use o **[!UICONTROL Importar usuários internos]** opção.

   ![](assets/import-users.png)

1. No lado esquerdo da página de mapeamento você pode ver as colunas do Learning Manager e, no lado direito, as colunas do miniOrange. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   ![](assets/map-attributes.png)

1. Para exibir e editar a origem de dados, como administrador, clique em **[!UICONTROL Configurações > Origem de Dados]**.

   A fonte estabelecida do miniOrange seria listada. Se for necessário editar o filtro, clique em **[!UICONTROL Editar]**.

   ![](assets/data-source.png)

1. Você receberá uma notificação após a conclusão da importação. Para exibir ou editar o registro de importação, clique em **[!UICONTROL Usuários > Log de importação.]**

### Excluir uma conexão {#deleteaconnection}

Siga estas etapas para excluir uma conexão miniOrange estabelecida.

## Conector do BlueJeans {#bluejeansconnector}

Agora você pode integrar o Learning Manager com o conector do BlueJeans e usar o BlueJeans para hospedar classes. O BlueJeans permite iniciar chamadas de conferência de áudio e vídeo, bate-papos com vídeo e webinars.

Siga estas etapas para configurar e usar o conector.

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão BlueJeans. Um menu é exibido. Clique em  **[!UICONTROL Conectar]** no menu.

   ![](assets/miniorange.png)

1. A página do conector do BlueJeans é aberta. Insira os detalhes da sua conta nos respectivos campos para integrar o Learning Manager e o BlueJeans para sincronização do feed do usuário. Você pode obter os detalhes do administrador da sua conta do BlueJeans.

   ![](assets/bluejeans-connecotrpage.png)

   Como aluno, ao ativar o conector, use a mesma ID de e-mail usada em sua conta do Learning Manager para ativar feeds do usuário no Learning Manager.

1. Depois que a conexão for estabelecida, como autor, crie um curso de sala de aula virtual com o BlueJeans como o sistema de conferência.

   ![](assets/conferencing-systems.png)

1. Administradores, gerentes e alunos podem inscrever alunos no curso criado. Ao ser inscrito, o aluno receberá um e-mail. O aluno pode fazer logon na sua conta do Learning Manager para visualizar os detalhes do programa e realizar o curso.
1. Quando o curso é concluído, o relatório de conclusão é enviado para o Learning Manager. O administrador pode ver o relatório de conclusão para verificar a participação e a pontuação dos alunos.

   ![](assets/-attendence-and-scoringreport.png)

## Conector da caixa {#boxconnector}

Com o conector do BOX, é possível integrar o Learning Manager com sistemas externos arbitrários para automatizar a sincronização dos dados. A expectativa é de que os sistemas externos possam exportar os dados em um formato CSV e colocá-los na pasta apropriada da conta do Box do Learning Manager. Os recursos do conector Box são os seguintes:

Você também pode usar o conector FTP para migração de dados, importação de usuários e exportação de dados. Para obter mais informações, [Conector FTP do Learning Manager.](third-party-connectors.md#main-pars_header_1427405935)

## Importação de dados {#DataImport-1}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no serviço do Box do Learning Manager e importe-os automaticamente para o Learning Manager. Com esse recurso, você pode integrar vários sistemas colocando o CSV gerado por eles nas pastas apropriadas das contas do Box. O Learning Manager pega os arquivos CSV, combina os arquivos e importa os dados conforme o agendamento. Consulte o recurso Agendamento para obter mais informações.

**Mapear atributos**

O administrador de integração pode escolher colunas de CSV e mapeá-las para os atributos agrupáveis do Learning Manager. Este mapeamento é uma tarefa única. Depois que o mapeamento é concluído, o mesmo mapeamento é usado em importações subsequentes do usuário. O mapeamento pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

## Exportação de dados {#dataexport}

A exportação de dados permite que os usuários exportem suas habilidades para um local do Box para integração com qualquer sistema de terceiros.

## Agendar relatórios {#schedulereports}

O administrador pode configurar tarefas de agendamento de acordo com os requisitos da organização, e os usuários no aplicativo Learning Manager são atualizados de acordo com o agendamento. Da mesma forma, o administrador de integração pode agendar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

## Configurar o conector do Box {#configureboxconnector}

Conheça o processo de integração do Learning Manager com o conector do Box.

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do Box. Um menu é exibido. Clique no item Conectar no menu.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

1. Uma caixa de diálogo é exibida solicitando que você insira a ID de e-mail. Forneça a ID de e-mail da pessoa responsável por gerenciar a conta do Box do Learning Manager da organização. Após fornecer a ID de e-mail, clique em Conectar.

1. O Learning Manager envia um e-mail solicitando que o usuário redefina a senha antes de acessar o Box pela primeira vez. O usuário deve redefinir a senha e usá-la para acessar a conta do Box do Learning Manager.

   Somente uma conta do Box do Learning Manager pode ser criada para uma determinada conta do Learning Manager.

   Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha a ação que deseja executar a partir das seguintes opções:

   * Importar usuários internos
   * Exportar habilidades de usuário - Configurar um agendamento
   * Exportar habilidades do usuário - OnDemand

## Importar

+++Usuário interno

A opção de importar usuário interno permite agendar a geração do relatório de importação do usuário automaticamente. Os relatórios gerados são enviados a você como arquivos .CSV.

+++

+++Mapear atributos

Depois que uma conexão é estabelecida com sucesso, você pode mapear as colunas dos arquivos CSV que serão colocados na pasta do Box para os atributos correspondentes do Learning Manager. Esta etapa é obrigatória.

1. No lado esquerdo da página Mapear atributos você pode ver as colunas esperadas do Learning Manager e, no lado direito, os nomes das colunas CSV. Inicialmente, no lado direito, você verá uma caixa de seleção vazia. Importe qualquer modelo CSV clicando em Escolher arquivo.

1. A etapa acima preenche a lista suspensa de seleção do lado direito com todos os nomes de colunas CSV. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   *O campo Gerente deve necessariamente ser mapeado para um campo do tipo endereço de e-mail. Antes de usar o conector, é necessário mapear todas as colunas.*

1. Clique em Salvar após concluir o mapeamento.

   O conector está pronto para uso. A conta recém-configurada agora aparecerá como uma fonte de dados no aplicativo do administrador para que o administrador agende a importação ou a sincronização por demanda.

+++

+++Utilização do conector do Box do Learning Manager

1. Os arquivos CSV de sistemas externos devem ser colocados no seguinte caminho:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Observação:** Na versão de julho de 2016, é permitido importar somente usuários. Portanto, para usar o conector do Box, você deve garantir que os arquivos CSV sejam colocados na seguinte pasta:\
   `code Home/import/user/internal/*.csv`

1. O conector do Box ocupa todas as linhas dos arquivos CSV, por isso é importante que a linha correspondente a um usuário em um CSV não apareça em nenhum outro CSV.
1. Todos os CSVs devem conter as colunas especificadas no mapeamento.
1. Todos os CSVs necessários devem estar presentes na pasta antes do início do processo.

Ao importar usuários para o Learning Manager, o administrador também precisa saber como os usuários são gerenciados no Learning Manager. Consulte [Ajuda do Gerenciamento de Usuários](../integration-admin/feature-summary/migration-manual.md#usermanagement) para saber mais informações.

+++

## Exportar

+++Habilidades

Há duas opções para exportar relatórios de habilidades do usuário.

Habilidades do Usuário - Sob Demanda: Você pode especificar a data de início e exportar o relatório usando a opção. O relatório será extraído da data informada até a presente

**[!UICONTROL Habilidades do usuário - Configurar]**: Essa opção permite agendar a extração do relatório. Marque a caixa de seleção Ativar programação e especifique a data e a hora de início. Você também pode especificar o intervalo no qual deseja que o relatório seja gerado e enviado.

+++

Para abrir a pasta Exportar em que os arquivos exportados serão colocados no local do Box, abra o link para a Pasta do Box fornecida na página Habilidades do usuário, conforme mostrado abaixo.

Os arquivos exportados automaticamente estarão presentes no local **Home/export/&#42;Box_location&#42;**

Os arquivos exportados automaticamente estarão disponíveis com o título, **skill_veries_&#42;data de &#42;_até_&#42;data - até&#42;.csv**

As permissões de acesso e o conteúdo na pasta do Box compartilhada pela equipe do Learning Manager devem ser gerenciados pelo cliente.  Observe também que o conteúdo da pasta seria armazenado fisicamente na região de Frankfurt.

## Conector do LinkedInLearning {#linkedinlearningconnector}

O conector do LinkedInLearning pode ser usado por clientes empresariais do LinkedIn.com que querem que os alunos descubram e realizem cursos do Learning Manager. O conector pode ser configurado para buscar cursos periodicamente com sua chave de API. Depois que um curso é criado no Learning Manager, os usuários podem pesquisá-lo e consumi-lo. O progresso do aluno pode ser acompanhado no Learning Manager.

### Configurar o conector do LinkedIn {#configurelinkedinconnector}

1. No painel do administrador integrado, clique em LinkedInLearning.

   Você verá o bloco com três opções: Introdução, Conectar e Gerenciar Conexões.

1. Se estiver configurando o conector do LinkedInLearning pela primeira vez, clique em Conectar.

   Configure a conta FTP do Exavault antes de configurar este conector.

1. Na página de conexão, especifique um nome para o conector. Insira a chave de aplicativo e a chave secreta da sua conexão.

   Entre em contato com o fornecedor para obter a chave do aplicativo e a chave secreta.

1. Clique em Salvar.

   A configuração é salva e a conexão do LinkedInLearning para sua conta é adicionada. Agora você pode clicar em Gerenciar conexões na página Início e editar sua configuração a qualquer momento.

1. Se você já tiver uma conexão estabelecida, clique em Gerenciar conexões para exibir todas as conexões.

   O recurso de migração deve ser habilitado para sua conta antes de você configurar esse conector.

1. Clique na conexão que deseja editar.
1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes da sua conta e o agendamento de sincronização nesta janela. Você deve marcar a caixa de seleção Ativar conexão se quiser ativar essa conta.
   * Clique em Editar e edite suas credenciais. Clique em Redefinir para desfazer as atualizações neste campo.
   * Clique em Ativar Programação para programar sua sincronização. Você pode inserir a data e a hora de início e, em seguida, inserir a frequência da programação da sincronização em dias. Por exemplo, habilitar a sincronização a cada 3 dias.

   Clique em Salvar para salvar as alterações.

1. No painel esquerdo, clique em Execução sob demanda. Esta opção permite importar feeds do usuário e outros dados relevantes do LinkedIn. Informe a Data de Início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados desde a data de início até a data presente são importados.

   * Você pode clicar em Desativar acesso ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se você clicar em Ativar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

1. Você também pode clicar em Status de execução no painel esquerdo a qualquer momento para exibir o resumo de todas as execuções deste conector, em ordem cronológica. Você pode exibir a data de início e a duração da sincronização, o tipo de sincronização (seja por demanda) e o status da sincronização (seja em andamento ou concluída).

   Quando você exclui e recria uma conexão, as execuções anteriores do conector aparecem novamente. Você pode exibir todas as execuções antes de excluir a conexão.

   Você pode executar uma nova execução somente para a sincronização mais recente.

