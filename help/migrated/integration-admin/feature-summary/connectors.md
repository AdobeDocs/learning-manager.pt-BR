---
description: Saiba como integrar vários conectores no Learning Manager
jcr-language: en_us
title: Conectores do Learning Manager
contentowner: jayakarr
exl-id: 1f44934b-6a2b-484d-bc7f-d0f23e3008ca
source-git-commit: aecc98cff7a46193627c961222f7e64f858dfa2c
workflow-type: tm+mt
source-wordcount: '15862'
ht-degree: 59%

---

# Conectores do Learning Manager

As empresas usam outros aplicativos e sistemas que precisam ser integrados com o Learning Manager. Os conectores são utilitários que ajudam a executar integrações baseadas em dados, como importar dados para o Learning Manager de sistemas externos.  Ele também executa a exportação de dados para sistemas externos a partir do Learning Manager.

O Learning Manager fornece conectores do Salesforce e FTP. Usando o conector do Salesforce, os administradores de integração de uma empresa podem integrar o aplicativo Salesforce com o Learning Manager. Como integrador, você também pode usar o conector FTP para importar automaticamente um conjunto de usuários para o seu aplicativo corporativo.

O Learning Manager também fornece os conectores para o Lynda, getAbstract e Harvard Management System. Estes conectores permitem que os alunos acessem e realizem cursos do Lynda.com, getAbstract e Harvard ManageMentor.

Continue lendo para saber como configurar e usar cada um desses conectores no Learning Manager.

<!--
>[!NOTE]
>
>**Update:** December 2020 update of Learning Manager
>
>For **FTP**, **Box**, and **Custom FTP** connectors, while exporting Learner Transcript or xAPI, you can also export the data as a **zip** file, for:
>
>* Learner Transcripts
>* xAPI
-->

>[!NOTE]
>
>Com a versão de novembro de 2022 do Adobe Learning Manager, o Zoom descontinuou a autenticação [JWT até junho de 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). Da mesma forma, o conector do Zoom com JWT continuará funcionando até a data mencionada, mas recomendamos que os usuários criem um aplicativo OAuth de servidor para servidor para substituir a funcionalidade na conta dele. Toda nova conexão terá a autenticação OAuth do Zoom por padrão.

## Conector do Salesforce {#sfconnector}

O conector do Salesforce conecta contas do Salesforce e do Learning Manager para automatizar a sincronização de dados. Os recursos do conector do Salesforce são os seguintes:

### Mapear atributos {#map-attributes}

O administrador de integração pode escolher colunas do Salesforce e mapeá-las para os atributos agrupáveis correspondentes do Learning Manager. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário. Ele poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

### Importação automatizada de usuário {#automated-user-import}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no Salesforce e importe-os automaticamente para o Learning Manager. Esta automação evita o esforço manual de criar e carregar um CSV no Learning Manager.

### Agendamento automático {#auto-schedule}

Usar os recursos automáticos de agendamento e importação de usuário em conjunto pode ser eficaz. O administrador do Learning Manager pode configurar o agendamento conforme as necessidades da organização. Os usuários podem ser atualizados no aplicativo Learning Manager conforme o agendamento. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

### Como filtrar usuários {#filtering-user}

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

### Configurar o conector do Salesforce {#configuresalesforceconnector}

Veja o processo para integrar o Salesforce com o Learning Manager

#### Pré-requisitos {#prerequisites}

Certifique-se de que sua organização do Salesforce compartilhe um URL com você. Por exemplo, se o nome da organização é **myorg**, a URL do Salesforce pode ser `https://myorg.salesforce.com`. Esta é a única entrada necessária para conectar a conta do Salesforce ao Learning Manager.

Certifique-se também de possuir as credenciais apropriadas para fazer logon na conta.

#### Criar uma conexão {#createaconnection}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do Salesforce. Será exibido um menu. Clique no item **[!UICONTROL Conectar]** no menu.

   ![](assets/mouserover-salesforce.png)

   *Opção Conectar*

1. É exibida uma caixa de diálogo solicitando que você insira o URL da organização. Clique em **[!UICONTROL Conectar]** após fornecer a URL.
1. Após uma conexão bem-sucedida, a página de visão geral é exibida.

### Mapear atributos {#mapattributes}

Uma vez que a conexão é estabelecida com sucesso, você pode mapear as colunas do Salesforce para os atributos correspondentes do Learning Manager. Essa etapa é obrigatória.

1. No lado esquerdo da página de mapeamento você pode ver as colunas do Learning Manager e, no lado direito, as colunas do Salesforce. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   ![](assets/sfdc-map-columns.png)
   *Mapear atributos*

   >[!NOTE]
   >
   >Os dados da coluna do Learning Manager mostrados no lado esquerdo são coletados dos campos ativos. O campo **gerente** deve ser mapeado para um campo do tipo endereço de email. Antes de usar o conector, é necessário mapear todas as colunas.

1. Clique em **[!UICONTROL Salvar]** após concluir o mapeamento.
1. O conector está pronto para uso. A conta que foi configurada e aparece como uma fonte de dados no aplicativo do administrador. O administrador pode agendar a importação ou a sincronização sob demanda.

## Como usar o conector do Salesforce {#usingsalesforceconnector}

O conector do Salesforce se conecta ao Salesforce.com para buscar os usuários, como configurado, e adicioná-los ao Learning Manager.

### Importar usuários dos contatos do Salesforce {#import-salesforce-contacts}

O Learning Manager aprimora o conector do Salesforce para buscar contatos, bem como usuários do Salesforce e importá-los automaticamente para o Learning Manager.

Na página do conector do Salesforce, insira o URL do Salesforce e conclua a autenticação. Depois de autenticar, você pode continuar a importar usuários ou contatos. Se você escolher a opção Contatos, especifique o subconjunto de contatos a serem importados.

Escolha as colunas do Salesforce e mapeie-as para os atributos agrupáveis correspondentes do Learning Manager. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário.

1. Faça logon no Salesforce.
1. Na página de conexão, clique em **[!UICONTROL Importar usuários internos]**.

   ![](assets/image048.png)
   *Importar usuários internos*

1. Na página **Importar Usuários**, há uma nova opção: Contatos. Clique no botão de opção **Contatos** e você verá as seguintes opções.

   ![](assets/image050.png)
   *Mapear os atributos do contato*

1. Se você clicar em **[!UICONTROL Sim]**, poderá executar o seguinte:

   * **Escolha a coluna Contatos:** selecione o campo que deseja importar para o Learning Manager.
   * **Especificar valores:** escolha os valores que representam o campo selecionado.

   ![](assets/image053.png)
   *Especifique os valores*

   * Mapeie as colunas do Salesforce com as do Learning Manager.
   * Para iniciar a importação, clique em **[!UICONTROL Salvar]**.

1. Se você clicar em **[!UICONTROL Não. Importe todos os Contatos]**. Você pode mapear os campos diretamente sem filtrar os contatos. Aqui, você importaria todos os contatos do Salesforce.
1. Para iniciar a importação, clique em **[!UICONTROL Salvar]**.

## Exportar registros de aprendizado {#export-learning-records}

O Learning Manager oferece a capacidade de exportar registros de aprendizado, como transcrição, relatório do usuário e relatório de habilidades, para o Salesforce. Você pode determinar se os dados exportados devem ser vinculados à tabela “Usuário” ou à tabela “Contatos” no Salesforce.

![](assets/export-events-new.png)
*Exportando registros de aprendizado*

### Objetos personalizados no Salesforce {#custom-objects-in-salesforce}

Antes de exportar registros de aprendizado do Learning Manager, você deve criar objetos personalizados no Salesforce. Objetos personalizados são objetos que você cria para armazenar informações específicas à sua empresa ou setor. Para obter mais informações, consulte [Objetos personalizados do Salesforce](https://trailhead.salesforce.com/en/content/learn/modules/data_modeling/objects_intro).

Veja como você criará os objetos:

1. Baixe e instale os pacotes para criar os objetos personalizados.

   * [Pacote 1](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPJ)
   * [Pacote 2](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPT)
   * [Pacote 3](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPi)

1. Renomeie os nomes dos objetos personalizados no Salesforce.
1. Selecione os eventos e clique em **[!UICONTROL Salvar]**.

>[!NOTE]
>
>Verifique se o acesso do administrador do sistema foi concedido a todos os campos ativos adicionados após a instalação do pacote.

**Vincule eventos com:** escolha a seção que deseja exportar - Usuário ou Contato. Se você escolher o objeto Contato, os usuários presentes no Learning Manager, mas não no Salesforce, serão criados no Salesforce.

![](assets/link-events.png)
*Opção Vincular eventos*

>[!NOTE]
>
>Você pode criar várias conexões em uma conta. Uma única conexão pode atender até três objetos personalizados no Salesforce. Se você deseja criar várias conexões para a mesma conta do Salesforce, instale os três pacotes. Oferecemos compatibilidade com até três pacotes.
>
>Quanto mais conexões você deseja criar, mais pacotes você deve instalar.

>[!NOTE]
>
>Na página Status de execução do Salesforce, o número de registros processados só pode ser verificado no Salesforce. O Learning Manager exibe o status como concluído mesmo quando há uma exportação parcial ou falha em todos os registros que foram processados.

## Instalar pacote do Salesforce {#install-salesforce-package}

O Learning Manager oferece um pacote do aplicativo Salesforce. Depois de instalados e configurados no SFDC, os funcionários de vendas podem executar suas atividades de treinamento no portal do SFDC. Este aplicativo permite que os usuários do SFDC explorem novos treinamentos, visualizem recomendações e as consumam diretamente no portal do SFDC. Os usuários também recebem os comunicados enviados pelos administradores na forma de cabeçalhos diretamente no aplicativo no portal do SFDC.

### Configurar no aplicativo Learning Manager {#setup-in-learning-manager-app}

1. Faça logon na sua conta de administrador do Learning Manager como administrador de integração.
1. Clique em **[!UICONTROL Aplicativos]** > **[!UICONTROL Aplicativos em destaque]**.
1. Clique em **[!UICONTROL Salesforce]**.
1. Na página do aplicativo Salesforce, observe a ID do aplicativo (também conhecida como ID do cliente) e o segredo do cliente mencionado na descrição.
1. Clique em **[!UICONTROL Aprovar]** e o aplicativo deve ser aprovado com êxito.
1. Clique em **[!UICONTROL Recursos do desenvolvedor]** > **[!UICONTROL Tokens de acesso para teste e desenvolvimento]**.
1. Na seção Obter código OAuth, a ID do cliente e o escopo devem ser definidos como - admin:read,admin:write. Clique em **[!UICONTROL Enviar]**.
1. Em Obter token de atualização, insira a ID do cliente e o segredo do cliente. Clique em **[!UICONTROL Enviar]** e anote o token de atualização.

### Criar conta no aplicativo Salesforce {#create-account-in-salesforce-app}

1. Crie uma conta na página de inscrição do Salesforce. Você deve criar uma conta do Salesforce na edição para desenvolvedores ou corporativa.  [URL de inscrição do desenvolvedor](https://developer.salesforce.com/signup). Certifique-se de usar a ID de e-mail para se inscrever no Salesforce que você usou para o Learning Manager.
1. Verifique a sua conta por meio do e-mail de verificação.
1. Crie uma senha e faça logon no Salesforce.
1. Anote o URL do Salesforce após o logon (por exemplo, site.lightning.force.com)

### Instalar pacote do Learning Manager {#install-learning-manager-package}

Se quiser instalar o pacote, primeiro exclua o pacote existente no Salesforce. Antes de desinstalar, você deve ativar as configurações, conforme mostrado abaixo. A aplicação dessas configurações é obrigatória, caso contrário, não será possível instalar o pacote.

>[!NOTE]
>
>O aplicativo Adobe Learning Manager só é compatível com a exibição Lightning do Salesforce.

1. Inicie a [url do pacote do Learning Manager](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WOQ).
1. Na página **Logon**, clique em **[!UICONTROL Usar domínio personalizado]**.
1. Insira a URL do pacote e clique em **[!UICONTROL Continuar]**. A página de instalação deve ter a opção Instalar somente para administradores selecionada. Não altere essa opção.
1. Clique em **[!UICONTROL Instalar]**. Após a instalação do pacote, clique em **[!UICONTROL Concluído]**. Você é guiado até a página Pacotes instalados e poderá ver o pacote instalado do Adobe Learning Manager.
1. Acesse o Inicializador de aplicativos (ao lado de Configuração) e procure o Adobe Learning Manager.
1. Para configurar o aplicativo, clique em **[!UICONTROL Configurar]**.
1. Clique em **[!UICONTROL Novo]** e adicione os seguintes detalhes:

   * **Config:** insira um nome de sua escolha.
   * **ClientID**: insira o valor obtido na primeira seção.
   * **ClientSecret:** insira o valor obtido na primeira seção.
   * **RefreshToken:** insira o valor obtido na primeira seção.
   * **LearningManagerBaseURL:** a URL do site onde o Learning Manager está hospedado.

### Adicionar configurações de site remoto {#add-remote-site-settings}

1. No canto superior direito da página, clique em **[!UICONTROL Instalação]**.
1. Em **[!UICONTROL Localização Rápida]**, procure Configurações de Site Remoto.
1. Clique em **[!UICONTROL Novo Site Remoto]**.
1. Insira os detalhes:

   * **Nome do site remoto:** insira um nome de sua escolha.
   * **URL do site remoto:** o URL do site onde o Learning Manager está hospedado.

1. Inicie o Learning Manager.

### Ativar notificações para o aplicativo Learning Manager {#enable-notifications-for-learning-manager-app}

1. No canto superior direito, clique em **[!UICONTROL Instalação]**.
1. Procure Notificações personalizadas.
1. Clique em **[!UICONTROL Novo]**.
1. Insira os seguintes detalhes:

   1. **Nome da Notificação Personalizada:** LearningManagerNotification
   1. **Nome da API:** LearningManagerNotification

1. Selecione **Desktop** e **Dispositivo móvel** como canais suportados.

1. Clique em **[!UICONTROL Salvar]**.
1. Para ativar as notificações push para dispositivos móveis, siga as etapas abaixo:

   1. Instale o aplicativo Salesforce para dispositivos móveis em seu celular.
   1. Faça logon no aplicativo usando suas credenciais.
   1. Vá para **Configuração** > **Configurações de Entrega de Notificação**.
   1. Adicione o Salesforce para iOS e Android.

### Desinstalar o Learning Manager do Salesforce

1. No aplicativo Salesforce, acesse Pacotes instalados.
1. Clique em **[!UICONTROL Desinstalar]**.

## Configurar o Learning Manager para usuários do Salesforce {#configure-learning-manager-for-salesforce-users}

O aplicativo Learning Manager também está disponível para usuários que estão presentes em qualquer conta do Salesforce. O administrador do Salesforce pode adicionar usuários com base nos perfis. Os perfis do Salesforce são semelhantes aos perfis no Learning Manager. Por exemplo, administrador, administrador de integração, professor e assim por diante. O administrador do Salesforce também pode criar um perfil personalizado.

Como administrador do Salesforce, você pode atribuir os perfis aos usuários ou criar um perfil personalizado.

![](assets/create-profile.png)

Ao instalar o pacote, você pode atribuir o perfil do Salesforce aos alunos.

Depois de instalar o pacote, você deve configurar o perfil.

Clique em **[!UICONTROL Configurar]** > **[!UICONTROL Novo]** e adicione o seguinte:

* Nome de configuração
* ClientID
* ClientSecret
* URLdeBaseDoLearningManager
* Desativar redirecionamento

>[!NOTE]
>
>Para que os alunos vejam o aplicativo Learning Manager, você deve ativar o aplicativo para todos os alunos.

A próxima etapa é conceder permissão para acessar o aplicativo Learning Manager.

![](assets/permission-set.png)

*Definir permissões para acessar o aplicativo Learning Manager*

Selecione os usuários e atribua as permissões adequadamente. Os alunos agora podem acessar o aplicativo Learning Manager.

Agora, selecione um perfil, por exemplo, Perfil padrão de um usuário e clique no perfil. Clique em **[!UICONTROL Editar]** e, na seção **Configurações do aplicativo personalizado**, habilite a caixa de seleção **Adobe Learning Manager**. Isso torna o aplicativo acessível ao usuário.

Na seção **Configurações da guia personalizada**, na lista suspensa **Página inicial do aluno**, selecione a opção **Padrão ativado**.

Você deve tornar o aplicativo visível para todos os perfis.

Clique em **[!UICONTROL Salvar]** e os alunos pertencentes a todos os perfis acessarão o aplicativo Learning Manager.

### Alterações relacionadas ao Caminho de aprendizado {#learning-path-changes}

#### Conexões existentes {#existing-connections}

Se a opção Caminho de aprendizado estiver desativada na conta do administrador, nenhuma linha e coluna será adicionada no relatório.

Se a opção Caminho de aprendizado estiver ativada na conta do administrador, a coluna “Tipo” será preenchida com o Caminho de aprendizado, caso os alunos estejam inscritos nele.

>[!NOTE]
>
>Se o sinalizador estiver ativado e você usar uma conexão existente, alguns registros podem ser perdidos.

#### Novas conexões {#new-connections}

Se a opção Caminho de aprendizado estiver desativada na conta do administrador, o relatório de treinamento consistirá das seguintes colunas, mas não conterá dados.

* **Caminho incorporado:** exibe o nome do programa de aprendizado
* **ID do caminho incorporado:** exibe as IDs do programa de aprendizado.
* **ID do curso incorporado:** exibe as IDs dos cursos que estão dentro de um caminho de aprendizado.

Além disso, para novas conexões em contas nas quais o Caminho de aprendizado está habilitado, as três novas colunas serão exibidas e todos os dados fluirão.

Além disso, o relatório conterá o tipo de coluna Caminho de aprendizado (Nível superior) para todos os alunos inscritos em um caminho de aprendizado.

Na coluna Tipo, o Programa de aprendizado será renomeado como Caminho de aprendizado. Para conexões existentes, não haverá alterações.

## Conector FTP do Learning Manager {#ftpconnector}

Com o conector FTP, é possível integrar o Learning Manager com sistemas externos arbitrários para automatizar a sincronização dos dados. A expectativa é de que os sistemas externos possam exportar os dados em um formato CSV e colocá-los na pasta apropriada da conta FTP do Learning Manager. Os recursos do conector FTP são os seguintes:

Você também pode usar o conector do Box para migração de dados, importação de usuários e exportação de dados. Para mais informações, consulte Conector Box.

### Importação de dados {#data-import}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no serviço FTP do Learning Manager e importe-os automaticamente para o Learning Manager. Com esse recurso, você pode integrar vários sistemas colocando o CSV gerado por eles nas pastas apropriadas das contas FTP. O Learning Manager pega os arquivos CSV, combina os arquivos e importa os dados conforme o agendamento. Consulte o recurso Agendamento para obter mais informações.

**Mapear atributos**

O administrador de integração pode escolher colunas de CSV e mapeá-las para os atributos agrupáveis do Learning Manager. Esse mapeamento é um esforço de tempo. Uma vez que o mapeamento está feito, este mesmo mapeamento é usado em importações subsequentes do usuário. O mapeamento poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.


#### Exportar dados {#export-data}

A exportação de dados permite que os usuários exportem habilidades de usuário e transcrições de alunos para um local FTP para serem integrados com um sistema de terceiros.

#### Agendamento {#scheduling}

Os administradores podem configurar tarefas de agendamento de acordo com os requisitos da organização, e os usuários no aplicativo Learning Manager são atualizados de acordo com o agendamento. Da mesma forma, o administrador de integração pode agendar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

### Configurar o conector FTP do Learning Manager {#configure-captivate-prime-ftp-connector}

Veja o processo para integrar o conector FTP com o Learning Manager.

#### Criar uma conexão {#Create-a-connection-1}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do FTP. Será exibido um menu. Selecione o item Conectar no menu.

   ![](assets/mouseover-ftpconnector.png)

   *Opção Conectar*

Para conectar-se a qualquer servidor FTP usando o cliente FTP, você precisará das seguintes informações:

* **Domínio FTP**: este é o endereço do servidor FTP ao qual você deseja se conectar. Por exemplo, ftp.example.com
* **Porta**: a porta FTP padrão é 21, mas alguns servidores podem usar portas diferentes por motivos de segurança. Para Adobe Learning Manager - Porta 22
* **Nome de Usuário do FTP**: o nome de usuário necessário para acessar o servidor FTP.
* **Senha de FTP**: a senha associada ao nome de usuário.

**FileZilla (Windows, macOS e Linux)**

**Etapa 1: baixar e instalar o FileZilla**

Se você ainda não instalou o FileZilla, baixe-o do site oficial: [Baixe](https://filezilla-project.org/) e instale-o em seu computador.

**Etapa 2: Abrir FileZilla**

Após a instalação, inicie o FileZilla no computador.

**Etapa 3: Coletar informações do servidor FTP**

**Etapa 4: inserir informações do servidor FTP no FileZilla**

No menu superior, selecione **[!UICONTROL Arquivo]** e selecione **[!UICONTROL Gerenciador de Sites]** (ou use o atalho Ctrl+S).

**Etapa 5: adicionar novo site FTP**

No Gerenciador de Sites, selecione **Novo Site** e digite um nome (por exemplo, Meu Servidor FTP).

**Etapa 6: inserir detalhes do FTP**

Digite as seguintes informações:

* **Host**: digite o endereço do servidor FTP.
* **Porta**: se o servidor usar uma porta maior que 21, insira o número de porta correto.
* **Protocolo**: escolha **[!UICONTROL SFTP - Protocolo de Transferência de Arquivo SSH]**.
* **Tipo De Logon**: Selecione **[!UICONTROL Normal]**.
* **Usuário**: digite seu nome de usuário do FTP.
* **Senha**: digite a senha do FTP.

**Etapa 7: conectar-se ao servidor FTP**

Selecione o botão **[!UICONTROL Conectar]** no Gerenciador de Sites. O FileZilla se conectará ao servidor FTP se todas as informações estiverem corretas.

**Etapa 8: navegar e transferir arquivos**

Depois de conectado, você verá os arquivos remotos no lado direito e os arquivos locais no lado esquerdo. É possível navegar nos diretórios e transferir arquivos arrastando-os e soltando-os entre os painéis.

>[!CAUTION]
>
>Ao transferir arquivos, evite alterar arquivos importantes no servidor.

<!--1. A dialog appears prompting you to enter the email id. Provide the email id of the person responsible for managing the Learning Manager FTP account for the organization. Click **[!UICONTROL Connect]** after providing the email id. 
1. Learning Manager sends you an email prompting the user to reset the password before accessing the FTP for the first time. The user must reset the password and use it for accessing the Learning Manager FTP account.

   >[!NOTE]
   >
   >Only one Learning Manager FTP account can be created for a given Learning Manager account.

   In the overview page, you can specify the Connection Name for your integration. Choose what action you want to take  from  the following options:

   * Import Internal Users  
   * Import xAPI
   * Export User Skills - Configure a Schedule  
   * Export User Skills - OnDemand  
   * Export Learner Transcripts - Configure a Schedule
   * Export Learner Transcripts - OnDemand

   ![](assets/ftp-connector-dashboard.png)
   *Export options*-->

### Importar {#import}

+++Usuário interno

A opção de importar usuário interno permite importar os usuários de um csv para um Learning Manager sob demanda ou agendamento.

+++

+++Mapear atributos

Uma vez que a conexão é estabelecida com sucesso, você pode mapear as colunas dos arquivos CSV. São colocados na pasta FTP dos atributos correspondentes no Learning Manager. Essa etapa é obrigatória.

1. No lado esquerdo da página Mapear atributos você pode ver as colunas esperadas do Learning Manager e, no lado direito, os nomes das colunas CSV. Inicialmente, no lado direito, você verá uma caixa de seleção em branco. Importe qualquer modelo CSV clicando em **Escolher Arquivo**.
1. A etapa acima preenche a lista suspensa de seleção do lado direito com todos os nomes de colunas CSV. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   >[!NOTE]
   >
   >O campo Gerente deve ser mapeado para um campo do tipo endereço de e-mail. Antes de usar o conector, é necessário mapear todas as colunas.

1. Selecione **[!UICONTROL Salvar]** após concluir o mapeamento.

   O conector está pronto para uso. A conta configurada aparece como uma fonte de dados no aplicativo do administrador para que o administrador agende a importação ou sincronização sob demanda.

+++

+++Utilização do conector FTP do Learning Manager

1. Os arquivos CSV de sistemas externos devem ser colocados no seguinte caminho:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   >[!NOTE]
   >
   >Na versão de julho de 2016, é permitido importar somente usuários. Portanto, para usar o conector FTP, certifique-se de que os arquivos CSV estejam colocados na seguinte pasta:

   `code Home/import/user/internal/*.csv`

1. O conector FTP ocupa todas as linhas dos arquivos CSV. É importante que a linha que corresponde a um usuário em um CSV não apareça em nenhum outro CSV.
1. Todos os CSVs devem conter as colunas especificadas no mapeamento.
1. Todos os CSVs necessários devem estar presentes na pasta antes do início do processo.

>[!NOTE]
>
>Ao importar usuários para o Learning Manager, o administrador também deve saber como os usuários são gerenciados no Learning Manager. Consulte a [Ajuda do Gerenciamento de Usuários](migration-manual.md#usermanagement) para obter mais informações.

+++

+++Importar xAPI

As opções de importação da xAPI permitem agendar a importação das instruções da xAPI dos serviços de terceiros para o Learning Manager sob demanda.

+++

+++Configurações necessárias para importar xAPI

1. Na página de configuração, selecione uma configuração existente que esteja disponível na lista de configurações para importar instruções xAPI do CSV. Clique em Editar ou **adicione um novo link Configuração** para navegar até a página Configurar Import-Sources.

   **Configuração**

   * Na página Configurar importação-Origens, preencha os dois campos, isto é, Nome e Nome do arquivo de origem. O nome do arquivo de origem deve corresponder ao nome do arquivo que é fornecido no local da pasta FTP.
   * Clique em **[!UICONTROL Salvar]** para salvar as alterações.

   ![](assets/configurations.png)
   *Configurar*

   **Filtro**

   * No painel esquerdo, clique em **[!UICONTROL Filtro]**.
   * Na página Configurar importação-Filtro, preencha os campos Nome e Condições para filtrar os registros. Clique em **[!UICONTROL Adicionar novo filtro]** para adicionar outro filtro. É possível salvar ou excluir um filtro clicando na opção **Salvar** ou **Excluir** na coluna Ações.

   ![](assets/filter.png)
   *Filtro*

   **Mapeamento**

   * No painel esquerdo, clique em **[!UICONTROL Mapeamento]**.
   * Na página Importar instruções da xAPI-Configuração-Mapeamento, à esquerda, você pode ver os nomes de caminho do campo JSON da xAPI que precisam ser mapeados com os nomes da coluna do CSV.
   * Por padrão, os três nomes de campo do caminho JSON que precisam ser mapeados com os nomes da coluna do CSV são **actor.mbox**, **verb.id** e **object.id**. É possível adicionar outros campos a serem mapeados clicando em **Adicionar novo mapeamento**.

   * Selecione o tipo de nome de coluna que está mapeando com o nome de caminho do campo JSON (seja string, número, booleano ou tipo de dados).
   * Clique em Salvar após concluir o mapeamento. A importação de xAPI agora pode ser realizada por agendamento ou sob demanda.

   ![](assets/mapping.png)
   *Mapeamento*

1. No painel esquerdo, clique em **[!UICONTROL Configurar agenda]**. Clique em **[!UICONTROL Habilitar agendamento]** para programar a importação de instruções da xAPI.

   Insira a hora e data de início e, em seguida, insira a frequência do agendamento de importação da xAPI em dias. Por exemplo, habilitando a importação da xAPI a cada três dias.

   ![](assets/configure-schedule2x.png)
   *Importar instruções xAPI - Configurar Agendamento*

1. No painel esquerdo, clique em **[!UICONTROL Execução sob Demanda]**.

   ![](assets/on-demand.png)
   *Importar instruções xAPI- Sob demanda*

1. No painel esquerdo, clique em **[!UICONTROL Status da execução]** para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. É possível ver a data de início e o tempo que leva a importação da xAPI, o tipo de importação (se for sob demanda ou agendada) e o status da importação (se a importação da xAPI está em andamento, foi concluída ou falhou).

   ![](assets/execution-status2x.png)
   *Importar instruções xAPI - Status de execução*

+++

<!--### Export

+++Skills

There are two options to export User skill reports.

**[!UICONTROL User Skills - On Demand]**: You can specify the  start date and export the report using the option. The report is extracted from the date entered until present.

![](assets/export-on-demand2x.png)
*On demand export option*

**[!UICONTROL User Skills - Configure]**: This option let's you schedule the extraction of the report. Select the Enable Schedule check box and specify the start date and time. You can also specify the interval at which you want the report to be generated and sent.

![](assets/user-skills-configure.png)
*Configure export of report*

+++

To open the Export folder where the exported files are placed, open the link to FTP Folder provided in the User Skills page as shown below.

![](assets/ftp-folder.png)
*FTP folder to view files*

The auto-exported files are present in the location **Home/export/&#42;FTP_location&#42;**

The auto-exported files are available with the title, **skill_achievements_&#42;date from&#42;_to_&#42;date to&#42;.csv**

![](assets/exported-csvs.png)
*Exported .csv file*

+++Learner Transcript

![](assets/on-demand-report.png)

**Configure**: This option  let's  you schedule the extraction of the report. Select the Enable Schedule check box and specify the start date and time. You can also specify the interval at which you want the report to be generated and sent.

![](assets/configure-report.png)

+++

To open the Export folder where the exported files are placed in your FTP location, open the link to FTP Folder provided on the Learner Transcript page as shown below

The auto-exported files are present in the location **Home/export/&#42;FTP_location&#42;**

The auto-exported files are available with the title, **learner_transcript_&#42;date from&#42;_to_&#42;date to&#42;.csv**-->

### Compatibilidade com campos CSV manuais {#support-for-manual-csv-fields}

Ao importar dados do usuário via FTP, um administrador precisará mapear todos os campos ativos presentes no sistema para o campo correspondente no csv.

Isso é obrigatório para todos os campos ativos do csv. Para campos ativos manuais, o administrador de integração pode selecionar a opção **NãoimportarDaOrigem**.

Ao selecionar essa opção, os valores manuais do campo ativo não serão preenchidos usando a importação csv. Os valores fornecidos pelo aluno permanecem intactos.

>[!NOTE]
>
>Durante o mapeamento, se a opção **DontImportFromSource** for selecionada para o campo ativo csv, esse campo será excluído do sistema.

![](assets/ftp-conector-foractivefields.png)
*Conector FTP para campos Ativos*

## Conector do Lynda {#lynda-connector}

O conector do Lynda é usado por clientes empresariais do lynda.com que querem que seus alunos descubram e realizem os cursos do Lynda dentro do Learning Manager. O conector pode ser configurado para obter periodicamente cursos do site Lynda.com com sua chave de API. Depois que um curso é criado no Learning Manager, ele pode ser pesquisado e realizado pelos usuários. O progresso do aluno pode ser acompanhado no Learning Manager.

### Configurar o conector do Lynda {#configure-the-lynda-connector}

1. No painel integrado do administrador, clique em Lynda.

   Você verá o quadro com três opções: Introdução, Conexão e Gerenciar conexões.

1. Se você estiver configurando o conector do Lynda pela primeira vez, clique em Conexão.

   <!--Configure the Exavault FTP account before you configure this connector.-->

1. Na página de conexão, especifique um nome para o conector. Insira a chave do aplicativo e a chave secreta da sua conexão.

   >[!NOTE]
   >
   >Entre em contato com o fornecedor para obter a chave do aplicativo e a chave secreta.

1. Clique em Salvar.

   A configuração é salva e a conexão do Lynda à sua conta é adicionada. Agora você pode clicar em Gerenciar conexões na página inicial e editar sua configuração a qualquer momento.

1. Se já tiver uma conexão estabelecida, clique em Gerenciar conexões para ver todas as conexões.

   >[!NOTE]
   >
   >O recurso de migração da sua conta deve ser habilitado antes de configurar este conector.

1. Clique na conexão que quer editar.
1. No painel esquerdo, clique em **[!UICONTROL Configurar]**. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Selecione a caixa de seleção Habilitar conexão se deseja habilitar esta conta.
   * Clique em Editar e edite suas credenciais. Para desfazer suas atualizações neste campo, clique em Redefinir.
   * Clique em Habilitar agendamento para agendar a sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, habilitar a sincronização a cada três dias.

   Clique em **[!UICONTROL Salvar]** para salvar as alterações.

   ![](assets/lynda.png)

   *Configurar o conector do Lynda para o Learning Manager*

1. No painel esquerdo, clique em Execução por demanda. Essa opção permite que você importe feeds do usuário e outros dados relevantes do Lynda. Insira a data de início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados a partir da data de início até o presente serão importados.

   * Você pode clicar em Desabilitar acesso ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se clicar em Habilitar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

   ![](assets/lynda-ondemand.png)

   *Executar execução sob demanda para o conector do Lynda*

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   >[!NOTE]
   >
   >Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

   ![](assets/lynda-ondemand.png)

   *Exibir o resumo de todas as execuções e clicar em Status de Execução*

## Conector do getAbstract {#getabstractconnector}

O conector do getAbstract é usado por clientes empresariais do site getAbstract.com que querem que os alunos descubram e usem os resumos do getAbstract. Este conector pode ser configurado para obter periodicamente dados de uso, com base nos registros de conclusão do aluno criados no Learning Manager. Continue lendo para saber como configurar este conector no Learning Manager.

### Configurar o conector do getAbstract {#configure-the-get-abstract-connector}

1. No painel integrado do administrador, clique em getAbstract.

   No quadro, você verá três opções: Introdução, Conexão e Gerenciar conexões.

1. Se estiver configurando o conector do getAbstract pela primeira vez, clique em Conectar.

   <!--Configure the Exavault FTP account before you configure this connector.

   Ensure that you share this FTP credentials with your content provider to access the feeds.-->

1. Insira um nome para a conexão no campo Nome da conexão.

   Insira as chaves apropriadas nos campos ID do cliente e Segredo do cliente. Entre em contato com o fornecedor para obter as chaves apropriadas para este conector.

   As chaves são necessárias para obter os metadados dos cursos realizados pelo cliente.

1. Se já tiver uma conexão estabelecida, na página inicial, clique em getAbstract > Gerenciar conexões para visualizar e editar a configuração atual.

   >[!NOTE]
   >
   >O recurso de migração da sua conta deve ser habilitado antes de configurar este conector.

1. Clique na conexão cuja configuração que você deseja exibir ou editar.

   ![](assets/getabstractschedulepage.png)

   *Configurar o conector getAbstract para o Learning Manager*

1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Selecione a caixa de seleção Habilitar conexão se deseja habilitar esta conta.
   * Clique em Editar e edite suas credenciais. Para desfazer suas atualizações neste campo, clique em Redefinir.
   * Clique em Habilitar agendamento para agendar a sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, habilitar a sincronização a cada três dias.

1. Clique em **[!UICONTROL Salvar]**.

   A configuração é salva e a conexão getAbstract para sua conta é adicionada.

1. No painel esquerdo, clique em Execução por demanda. Essa opção permite que você importe feeds do usuário e outros dados relevantes do getAbstract. Insira a data de início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados a partir da data de início até o presente serão importados.

   * Você pode clicar em Desabilitar acesso ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se clicar em Habilitar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   >[!NOTE]
   >
   >Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

   Para que qualquer tipo de sincronização funcione, assegure-se de que o feed do usuário esteja presente na pasta FTP do getAbstract para as datas especificadas na sincronização.

   Veja a planilha Excel a seguir, que é um arquivo de feed do usuário de amostra do getAbstract. O nome do arquivo deve seguir o formato: **report_export_yyyy_MM_dd_HHmmss.xlsx** ou **report_export_yyyy_MM_dd.xlsx**.
   [folha do Excel de exemplo de feed de usuário getAbstract](assets/report-export-20170401175342.xlsx)

## Conector do Harvard ManageMentor {#hmmconnector}

O conector do Harvard ManageMentor é usado por clientes empresariais do site Harvard ManageMentor que querem que os alunos encontrem e realizem cursos do Harvard ManageMentor. O conector ajuda a criar cursos no Learning Manager e pode ser configurado para obter periodicamente dados de progresso do aluno. Para configurar esse conector, execute o seguinte procedimento:

### Configurar o conector do Harvard ManageMentor {#configure-the-harvard-managermentor-connector}

1. No painel integrado do administrador, clique em Harvard ManageMentor.

   No quadro, você verá três opções: Introdução, Conexão e Gerenciar conexões.

1. Se estiver configurando o conector do Harvard ManageMentor pela primeira vez, clique em Conectar.

   <!--Configure the Exavault FTP account before you configure this connector.

   Ensure that you share this FTP credentials with your content provider to access the feeds.-->

1. No campo Nome da conexão, insira um nome para a conexão. Clique em Conectar para salvar esta conexão.
1. Se já tiver uma conexão estabelecida, na página inicial, clique em Harvard ManageMentor > Gerenciar conexões. Clique na conexão cuja configuração existente você quer editar.

   >[!NOTE]
   >
   >O recurso de migração da sua conta deve ser habilitado antes de configurar este conector.

   ![](assets/hmm.png)

   *Configurar o conector do HarvardManage Mentor para o Learning Manager*

1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Selecione a caixa de seleção Habilitar conexão se deseja habilitar esta conta.
   * Clique em Habilitar agendamento para agendar a sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, habilitar a sincronização a cada três dias.

1. No painel esquerdo, clique em Execução por demanda. Essa opção permite que você importe feeds do usuário e outros dados relevantes do Harvard ManageMentor. Insira a data de início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados desta conexão, a partir da data de início até o presente, serão importados.

   * Você pode clicar em Desabilitar acesso ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se clicar em Habilitar acesso ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

   Se quiser automatizar a sincronização para que ocorra a cada poucos dias, especifique o número de dias no campo Não número de dias. A sincronização garante que sua conta seja atualizada com a versão mais recente dos sumários e resumos do Harvard ManageMentor.

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   >[!NOTE]
   >
   >Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

   Para que a sincronização seja bem sucedida, certifique-se de que pelo menos um dos seguintes arquivos estão presentes na pasta FTP do Harvard ManageMentor:

   hmm12_metadata.csv: Esse arquivo fornece os metadados do curso para o conector Harvard ManageMentor. Certifique-se de ter seguido a convenção de nomenclatura ao carregar o arquivo.

   client_hmm12_20150125.csv: é o feed de usuário do conector Harvard ManageMentor. A seguinte convenção de nomenclatura de arquivo é **client_hmm12_yyyyMMdd.csv.**

   Veja os dois seguintes arquivos de amostra a seguir do feed do usuário e do feed do curso deste conector:

   * [Arquivo de metadados do curso para o conector Harvard ManageMentor](assets/hmm12-metadata.csv)
   * [Feed do usuário do conector do Harvard ManageMentor](assets/client-hmm12-20170304.csv)

## Conector do Workday {#workdayconnector}

Com o conector do Workday, você pode integrar o Learning Manager com o inquilino do Workday para automatizar a sincronização dos dados.

### Importar {#import-1}

#### Mapear atributos {#map-attributes-1}

O administrador de integração pode escolher colunas do Workday e mapeá-las para os atributos agrupáveis correspondentes do Learning Manager. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário. Ele poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

#### Importação automatizada de usuário {#automated-user-import-1}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no Workday e importe-os automaticamente para o Learning Manager.

#### Como filtrar usuários {#filtering-users}

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

### Exportar {#export}

A exportação das habilidades do usuário permite que os usuários exportem habilidades para o Workday automaticamente.

>[!NOTE]
>
>Não é possível exportar habilidades de várias contas do Learning Manager simultaneamente usando a mesma conta do Workday.

#### Apontar para a observação {#points-to-note}

* Garantir que a UUID, o endereço de e-mail e o nome do funcionário sejam exclusivos em várias integrações da Workday. Valores incorretos resultarão em uma falha de conexão.
* O campo UUID preenchido via Workday em não pode ser excluído por nenhum administrador do LMS voltado para o cliente. Se quiser alterar o valor, entre em contato com a equipe de integração ou suporte do Adobe Learning Manager.
* A opção Limpeza do Usuário também pode não funcionar, pois a Limpeza do Usuário oferece suporte apenas a 50 usuários a serem removidos por execução. Tenha muito cuidado ao fazer upload dos usuários pelos UUIDs.

### Agendamento {#Scheduling-1}

O administrador pode configurar tarefas de agendamento conforme os requisitos da organização, enquanto os usuários no aplicativo Learning Manager são atualizados conforme a agenda. Da mesma forma, o administrador de integração pode programar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

### Configurar o conector do Workday {#configure-workday-connector}

>[!PREREQUISITES]
>
>Solicite ao administrador do Workday de sua organização que crie um usuário do sistema de integração (ISU) com as permissões conforme definido no documento ISU_Permissions. Faça download de uma cópia do link abaixo.

[Baixe uma cópia da segurança do usuário do sistema de integração (ISU).](assets/isu-permissions-v1.pdf) Veja o processo para integrar o conector do Workday com o Learning Manager.

1. Na página inicial do Learning Manager, passe o mouse sobre o bloco do Workday. Será exibido um menu. Clique no item **[!UICONTROL Conectar]** no menu.

   ![](assets/workday-tile.png)

   *Bloco do Workday*

1. Uma caixa de diálogo é exibida, solicitando que você insira as credenciais da nova conexão. Antes de fazer a conexão, insira os seguintes campos.

   * Nome da conexão: forneça um nome de conexão de sua preferência.
   * URL do host: o administrador de integração pode obter os detalhes do URL do host do administrador do Workday correspondente.
   * Locatário: o locatário é interno à sua empresa. O administrador do Workday fornecerá os detalhes de inquilino.
   * Nome de usuário e senha: o administrador do Workday cria um usuário de sistema integrado (ISU) com os privilégios de segurança necessários e o compartilha com o administrador de integração.

>[!NOTE]
>
>   O Learning Manager usa a versão 40.1 da API do Workday.


![](assets/configure-connector.png)
*Configurar o conector do Workday*

1. Clique em conectar após digitar as informações em todos os campos relevantes.

   >[!NOTE]
   >
   >Também é possível ter várias conexões do Workday sincronizadas com sua conta do Learning Manager.

Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha que ação você quer executar entre as seguintes opções:

* Importar usuários internos
* Exportar habilidades de usuário - Configurar um agendamento
* Exportar habilidades de usuário - Sob demanda

![](assets/overview.png)
*Visão geral do Workday*

### Importar {#import-5}

#### Mapear atributos {#map-attributes-4}

Você pode usar o conector do Workday para integrar o Learning Manager e o Workday à sincronização automática de dados. É possível importar todos os usuários ativos do Workday para o Learning Manager. Os usuários podem ser importados de várias fontes de dados, incluindo FTP e Salesforce.

Antes de importar usuários, os atributos do usuário do Learning Manager e do Workday devem ser mapeados. Na página de visão geral, use a opção Usuários internos, em Importar, para fornecer os atributos do mapa.

Insira as credenciais do Adobe Learning Manager abaixo da coluna Adobe Learning Manager. Use os menus suspensos para selecionar as credenciais corretas para as colunas abaixo do Workday.

>[!NOTE]
>
>Atualmente, o Learning Manager é compatível com a importação de 69 atributos de usuário do Workday. Adicione mais atributos usando os Campos ativos no Learning Manager.

![](assets/workday.png)
*Mapear atributos*

Marque a caixa de seleção **Excluir trabalhadores temporários** para impedir que os trabalhadores temporários disponíveis sob um gerente sejam importados.

O Workday tem quatro níveis de hierarquia, enquanto o Learning Manager tem dois níveis. Os quatro níveis no Workday são categoria de perfil de habilidade, perfil de habilidade, categoria de item de habilidade e item de habilidade. Seu nome de habilidade e o nível do Learning Manager juntos são mapeados no Workday sob o item de habilidade.

>[!NOTE]
>
>Você pode adicionar outros atributos do Workday. Entre em contato com seu CSAM para obter os atributos adicionados.

+++Lista de atributos Workday compatíveis

wd:User_ID
wd:Worker_ID
gerente
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Nome_Formatado
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Nome_Formatado
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:First_Name
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Last_Name
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:First_Name
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Last_Name
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.@wd:Endereço_Formatado
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Postal_Code
wd:Personal_Data.wd:Contact_Data.wd:Email_Address_Data.0.wd:Email_Address
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Country_Region_Descriptor
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Telefone_Formatado
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Country_ISO_Code
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:International_Phone_Code
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Phone_Number
wd:Personal_Data.wd:Primary_Nationality_Reference.wd:ID.1.$
wd:Personal_Data.wd:Gender_Reference.wd:ID.1$
wd:Personal_Data.wd:Identification_Data.wd:National_ID.0.wd:National_ID_Data.wd:ID
wd:Personal_Data.wd:Identification_Data.wd:Custom_ID.0.wd:Custom_ID_Data.wd:ID
wd:User_Account_Data.wd:Default_Display_Language_Reference.wd:ID.1.$
wd:Role_Data.wd:Organization_Role_Data.wd:Organization_Role.0.wd:Organization_Role_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Position_Title
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Title
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Name
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.@wd:Endereço_Formatado
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Classification_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Group_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Work_Space__Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Family_Reference.0.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Profile_Name
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Profile_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Reference.wd:ID.2.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Worker_Type_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.@wd:Endereço_Formatado
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Management_Level_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Status_Data.wd:Ative
wd:Employment_Data.wd:Worker_Status_Data.wd:Ative_Status_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Hire_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Original_Hire_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirado
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Terminado
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$
wd:Qualification_Data.wd:Education.0.wd:School_Name
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Company
wd:Management_Chain_Data.wd:Worker_Supervisors_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID
Email de Trabalho Principal
wd:Organization_Type_Reference_Cost_Center_ID
wd:Organization_Type_Reference_Cost_Center_Name
wd:Organization_Type_Reference_Company
wd:Organization_Subtype_Reference_Department
wd:Organization_Subtype_Reference_Division
wd:Universal_ID
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Descriptor
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Reference.wd:ID.2.$
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Municipality

+++

### Exportar {#export-1}

Você pode exportar todas as habilidades obtidas por um usuário do Learning Manager para o Workday. Apenas habilidades ativas do usuário são exportadas. O Learning Manager não exporta habilidades retiradas. Também é possível conectar vários Learning Manager\
contas para o mesmo conector do Workday. Caso os nomes de habilidades sejam os mesmos em duas contas do Learning Manager, eles serão mapeados para a mesma habilidade no Workday. Antes de atualizar a habilidade no Workday, se duas contas do Learning Manager estiverem usando a mesma conta do Workday, é recomendável atualizar os nomes das habilidades em todas as contas do Learning Manager.

+++Habilidades de usuário - Configurar

Essa opção permite que você agende a extração do relatório. Certifique-se que a caixa de seleção Habilitar exportação de habilidade do usuário usando esta conexão está habilitada. Selecione a caixa de seleção Habilitar agendamento e especifique a data e hora de início. Também é possível especificar o intervalo no qual deseja que o relatório seja gerado e enviado. Selecione a caixa de seleção Habilitar agendamento e digite a data e hora de início e o número de dias “n” após os quais repetir. Uma vez concluído, clique em Salvar.

![](assets/configure-schedule.png)
*Configurar relatório de habilidades do usuário*

+++

+++Habilidades do usuário - Sob demanda

Você pode especificar a data de início e exportar o relatório usando a opção. O relatório é extraído da data inserida até o presente. Insira a data a partir da qual você quer gerar o relatório e clique em Executar.

![](assets/on-demand-report.png)
*Relatório de habilidades do usuário por demanda*

+++

+++Habilidades do usuário - Status da execução

Aqui, você pode ver o resumo de todas as tarefas e obter o relatório de status delas. É possível baixar relatórios de erro clicando no link do relatório de erro.

![](assets/execution-status.png)
*Relatório de execução de habilidades do usuário*

+++

## Conector do miniOrange {#mini-orange-connector}

Com o conector do miniOrange, você pode integrar o Learning Manager com o inquilino do miniOrange para automatizar a sincronização de dados.

### Importar {#import-6}

#### Mapear atributos {#map-attributes-5}

O administrador de integração pode escolher atributos do miniOrange e mapeá-los para os atributos agrupáveis correspondentes do Learning Manager. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário. Ele poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

#### Importação automatizada de usuário {#automated-user-import-3}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no miniOrange e importe-os automaticamente para o Learning Manager.

#### Como filtrar usuários {#filtering-users-3}

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

Para configurar   miniOrange   entre em contato com a equipe de CSM do Learning Manager.

### Configurar o conector do miniOrange {#configure-mini-orange-connector}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão laranja. Será exibido um menu. Clique na opção **[!UICONTROL Conectar]** no menu.

   ![](assets/miniorange-tile.png)

   *Bloco do conector miniOrange*

1. Clique em **[!UICONTROL Conectar]** para estabelecer uma nova conexão. A página do conector do miniOrange é exibida. Insira os detalhes da conta que quer mapear.

   ![](assets/establish-connection.png)

   *Criar uma conexão*

1. Se quiser importar o usuário do miniOrange diretamente como um usuário interno do Learning Manager, use a opção **[!UICONTROL Importar usuários internos]**.

   ![](assets/import-users.png)

   *Importar usuários internos*

1. Na página de mapeamento, à esquerda   lado, você pode ver as colunas do Learning Manager e, à direita,   lado você pode ver as colunas do miniOrange. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   ![](assets/map-attributes.png)

   *Mapear atributos*

1. Para ver e editar a fonte de dados, como um administrador, clique em **[!UICONTROL Configurações > Fonte de dados]**.

   A fonte estabelecida do miniOrange seria listada. Se você precisar editar o filtro, clique em **[!UICONTROL Editar]**.

   ![](assets/data-source.png)

   *Exibir e editar uma fonte de dados*

1. Você receberá uma notificação após a conclusão da importação. Para ver ou editar o registro de importação, clique em **[!UICONTROL Usuários > Importar registro.]**

<!-- #### Delete a connection {#deleteaconnection}

To delete an established  miniOrange  connection, follow these steps. -->

## Conector do Zoom {#zoom-connector}

Você pode integrar o Learning Manager com conectores do Zoom e usá-los para hospedar classes.  O conector permite que você configure reuniões/aulas de videoconferência com os alunos.

Para configurar e usar o conector, siga estas etapas.

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura do Zoom. Será exibido um menu. Clique na opção **[!UICONTROL Conectar]** no menu.

   <!-- ![](assets/connectors.png)

   *Zoom connector tile* -->

1. A página do conector do Zoom é aberta. Insira os detalhes da sua conta nos respectivos campos para integrar e sincronizar o feed do usuário. Você pode obter os detalhes com o administrador da sua conta do conector.

   <!-- ![](assets/bluejeans-connecotrpage.png)
   *Connect to BlueJeans/ Zoom* -->

   >[!NOTE]
   >
   >Como aluno, ao habilitar o conector, use a mesma ID de e-mail usada em sua conta do Learning Manager para ativar feeds do usuário no Learning Manager.

1. Depois que a conexão for estabelecida, como autor, crie um curso de sala de aula virtual com o Zoom como o sistema de conferência.

   <!-- ![](assets/vc.jpg)
   
   *Create a VC course* -->

1. Administradores, gerentes e alunos podem inscrever alunos no curso criado. Ao ser inscrito, o aluno receberá um e-mail. O aluno pode fazer logon na sua conta do Learning Manager para visualizar os detalhes do programa e realizar o curso.
1. Quando o curso é concluído, o relatório de conclusão é enviado para o Learning Manager. O administrador pode visualizar o relatório de conclusão para verificar a participação e pontuação dos alunos.

   ![](assets/attendence-and-scoringreport.png)
   *Relatório de participação e pontuação*

### Criar um aplicativo OAuth de zoom servidor para servidor {#create-a-zoom-server-to-server-oauth-app}

Ao criar um aplicativo OAuth de servidor para servidor do Zoom para ser usado no Adobe Learning Manager, você deve adicionar escopos exigidos pelo Adobe Learning Manager ao criar a conexão.

O Adobe Learning Manager requer os escopos abaixo e eles devem ser selecionados no aplicativo OAuth.

* Exibir todas as reuniões de usuário `/meeting:read:admin`
* Exibir e gerenciar todas as reuniões de usuário `/meeting:write:admin`
* Exibir dados do relatório `/report:read:admin`
* Exibir todas as informações do usuário `/user:read:admin`
* Exibir informações dos usuários e gerenciar usuários `/user:write:admin`
* Adicionar um inscrito de reunião `/meeting:write:registrant:admin`
* Listar todos os inscritos na reunião `/meeting:read:list_registrants:admin`
* Exibir e gerenciar reuniões de usuário da subconta `/meeting:write:meeting:master`
* Exibir dados do relatório `/report:read:list_meeting_participants:admin`

## Conector do Box {#box_connector}

Com o conector do Box, é possível integrar o Learning Manager com sistemas externos arbitrários para automatizar a sincronização dos dados. A expectativa é de que os sistemas externos possam exportar os dados em um formato CSV e colocá-los na pasta apropriada da conta do Box do Learning Manager. Os recursos do conector Box são os seguintes:

Você também pode usar o conector FTP para migração de dados, importação de usuários e exportação de dados. Para mais informações, consulte [Conector FTP do Learning Manager.](connectors.md#main-pars_header_1427405935)

### Importação de dados {#data-import-1}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no serviço do Box do Learning Manager e importe-os automaticamente para o Learning Manager. Com esse recurso, você pode integrar vários sistemas colocando o CSV gerado por eles nas pastas apropriadas das contas do Box. O Learning Manager pega os arquivos CSV, combina os arquivos e importa os dados conforme o agendamento. Consulte o recurso Agendamento para obter mais informações.

**Mapear atributos**

O administrador de integração pode escolher colunas de CSV e mapeá-las para os atributos agrupáveis do Learning Manager. Este mapeamento é uma tarefa única. Uma vez que o mapeamento está feito, este mesmo mapeamento é usado em importações subsequentes do usuário. O mapeamento poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

## Exportação de dados {#data-export}

A exportação de dados permite que os usuários exportem habilidades do usuário e transcrições dos alunos para um local do Box para serem integrados com um sistema de terceiros.

## Agendar relatórios {#schedule-reports}

O administrador pode configurar tarefas de agendamento conforme os requisitos da organização, enquanto os usuários no aplicativo Learning Manager são atualizados conforme a agenda. Da mesma forma, o administrador de integração pode programar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

## Configurar o conector do Box {#boxconnector}

Veja o processo para integrar o conector do Box com o Learning Manager.

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do Box. Será exibido um menu. Clique no item Conectar no menu.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

   *Conectar à Caixa*

1. É exibida uma caixa de diálogo solicitando que você insira a ID de e-mail. Forneça a ID de e-mail da pessoa responsável por gerenciar a conta do Box do Learning Manager da organização. Após fornecer a ID de e-mail, clique em Conectar.
1. O Learning Manager envia um e-mail solicitando que o usuário redefina a senha antes de acessar o Box pela primeira vez. O usuário deve redefinir a senha e usá-la para acessar a conta do Box do Learning Manager.

   >[!NOTE]
   >
   >Somente uma conta do Box do Learning Manager pode ser criada para uma determinada conta do Learning Manager.

   Na página de visão geral, você pode especificar o Nome da conexão para sua integração. Escolha a ação que deseja executar a partir das seguintes opções:

   * Importar usuários internos
   * Importar relatórios de atividades da xAPI
   * Exportar habilidades de usuário - Configurar um agendamento
   * Exportar habilidades de usuário - Sob demanda
   * Exportar transcrição do aluno - Configurar um agendamento
   * Exportar transcrição do aluno - OnDemand

## Importar {#import-7}

+++Usuário interno

A opção importar usuário interno permite que você agende a geração de relatórios de importação de usuário automaticamente. Os relatórios gerados são enviados como arquivos .CSV.

+++

+++Mapear atributos

Depois que uma conexão é estabelecida com sucesso, você pode mapear as colunas dos arquivos CSV colocados na pasta do Box para os atributos correspondentes do Learning Manager. Essa etapa é obrigatória.

1. Na página Mapear atributos, à esquerda   lado, você pode ver as colunas esperadas do Learning Manager e, à direita,   Ao lado, você pode ver os nomes das colunas CSV. Inicialmente, no lado direito, você verá uma caixa de seleção em branco. Importe qualquer modelo CSV clicando em Escolher arquivo.
1. A etapa acima preenche a lista suspensa de seleção do lado direito com todos os nomes de colunas CSV. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   *O campo Gerente deve ser mapeado para um campo do tipo endereço de email. Antes de usar o conector, é necessário mapear todas as colunas.*

1. Clique em Salvar após concluir o mapeamento.

   O conector está pronto para uso. A conta configurada aparece como uma fonte de dados no aplicativo do administrador para que o administrador agende a importação ou sincronização sob demanda.

+++

+++Relatório de atividades da xAPI

A opção Relatório de atividades da xAPI permite gerar a importação das instruções da xAPI a partir dos serviços de terceiros. Os arquivos são salvos como arquivos .CSV e são, então, convertidos em instruções da xAPI durante a importação para o Learning Manager.

+++

+++Configurações necessárias para importar xAPI

1. Na página de configuração, selecione uma configuração existente que esteja disponível na lista de configurações para importar instruções xAPI do CSV. Clique em Editar ou no link A **Adicionar uma nova Configuração** para navegar até a página Importar Arquivo de Origem de Configuração de Instruções da xAPI.

   ![](assets/artboard-11-2x.png)

   *Editar ou adicionar uma nova configuração*

   **Configuração**

   * Na página Configurar importação-Origens, preencha os dois campos, isto é, Nome e Nome do arquivo de origem. O nome do arquivo de origem deve corresponder ao nome do arquivo que é fornecido no local da pasta FTP.
   * Clique em **[!UICONTROL Salvar]** para salvar as alterações.

   ![](assets/configurations-main2x.png)

   *Configurar*

   **Filtro**

   * No painel esquerdo, clique em Filtro.
   * Na página Configurar importação-Filtro, preencha os campos Nome e Condições para filtrar os registros. Clique em Adicionar novo filtro para adicionar outro filtro. É possível salvar ou excluir um filtro clicando na opção Salvar ou Excluir na coluna Ações.

   ![](assets/box-filter-2x.png)

   *Filtro*

   **Mapeamento**

   * No painel esquerdo, clique em Mapeamento.
   * Na página Configurar importações-Mapeamento, à esquerda, você pode ver os nomes de caminho do campo JSON da xAPI que precisam ser mapeados com os nomes da coluna do CSV.
   * Por padrão, os três nomes de campo do caminho JSON que precisam ser mapeados com os nomes da coluna do CSV são **actor.mbox**, **verb.id** e **object.id**. É possível adicionar outros campos a serem mapeados clicando em Adicionar novo mapeamento.
   * Selecione o tipo de nome de coluna que está mapeando com o nome de caminho do campo JSON (seja string, número, booleano ou tipo de dados).
   * Clique em Salvar após concluir o mapeamento. A importação de xAPI agora pode ser realizada por agendamento ou sob demanda.

   ![](assets/box-mapping-2x.png)
   *Mapeamento*

1. No painel esquerdo, clique em **[!UICONTROL Configurar agenda]**. Clique em Habilitar agendamento para programar a importação de instruções da xAPI. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de importação da xAPI em dias. Por exemplo, habilitando a importação da xAPI a cada três dias.

   ![](assets/configure-schedulebox2x.png)
   *Importar instruções xAPI - Configurar Agendamento*

1. No painel esquerdo, clique em **[!UICONTROL Execução sob Demanda]**.

   ![](assets/box-on-demand-2x.png)
   *Importar instruções xAPI - Sob demanda*

1. No painel esquerdo, clique em **[!UICONTROL Status da execução]** para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. É possível ver a data de início e o tempo que leva a importação da xAPI, o tipo de importação (se for sob demanda ou agendada) e o status da importação (se a importação da xAPI está em andamento, foi concluída ou falhou).

   ![](assets/box-execution-status2x.png)
   *Importar instruções xAPI - Status de execução*

+++

+++Utilização do conector do Box do Learning Manager

1. Os arquivos CSV de sistemas externos devem ser colocados no seguinte caminho:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   >[!NOTE]
   >
   >Na versão de julho de 2016, é permitido importar somente usuários. Portanto, para usar o conector do Box, certifique-se de que os arquivos CSV estejam colocados na seguinte pasta:

   `code Home/import/user/internal/*.csv`

1. O conector do Box ocupa todas as linhas dos arquivos CSV. É importante que a linha que corresponde a um usuário em um CSV não apareça em nenhum outro CSV.
1. Todos os CSVs devem conter as colunas especificadas no mapeamento.
1. Todos os CSVs necessários devem estar presentes na pasta antes do início do processo.

Ao importar usuários para o Learning Manager, o administrador também deve saber como os usuários são gerenciados no Learning Manager. Consulte a [Ajuda do Gerenciamento de Usuários](migration-manual.md#usermanagement) para obter mais informações.

+++

## Exportar {#export-2}

+++Habilidades

Há duas opções para exportar relatórios de habilidades do usuário.

Habilidades do usuário - Sob demanda: especifique a data de início e exporte o relatório usando a opção. O relatório é extraído da data inserida até a presente

**[!UICONTROL Habilidades do usuário - Configurar]**: esta opção permite que você agende a extração do relatório. Selecione a caixa de seleção Habilitar agendamento e especifique a data e hora de início. Também é possível especificar o intervalo no qual deseja que o relatório seja gerado e enviado.

+++

Para abrir a pasta Exportar onde os arquivos exportados são colocados no Box, abra o link para a Pasta do Box fornecida na página Habilidades do usuário, conforme mostrado abaixo.

Os arquivos exportados automaticamente estão presentes no local **Home/export/&#42;Box_location&#42;**

Os arquivos exportados automaticamente estão disponíveis com o título **skill_conquistas_&#42;data de &#42;_a_&#42;data para&#42;.csv**

>[!NOTE]
>
>O cliente gerencia as permissões de acesso e o conteúdo na pasta do Box compartilhada pela equipe do Learning Manager.  Além disso, o conteúdo da pasta seria armazenado fisicamente na região de Frankfurt.

### Compatibilidade com campos CSV manuais {#support-for-manual-csv-fields-1}

Ao importar dados do usuário pelo Box, um administrador precisa mapear todos os campos ativos presentes no sistema para o campo correspondente no csv.

Isso é obrigatório para todos os campos ativos do csv. Para campos ativos manuais, o administrador de integração pode selecionar a opção **NãoimportarDaOrigem**.

Ao selecionar essa opção, os valores manuais do campo ativo não serão preenchidos usando a importação csv. Os valores fornecidos pelo aluno permanecem intactos.

>[!NOTE]
>
>Durante o mapeamento, se a opção **DontImportFromSource** for selecionada para o campo ativo csv, esse campo será excluído do sistema.

![](assets/box-connector-foractivefields.png)
*Conector de caixa para campos Ativos*

>[!NOTE]
>
>Qualquer conector ou migração que use FTP/Box como fonte de dados, todos os arquivos CSV processados serão excluídos.
>
>O CSV para os conectores de conteúdo, por exemplo, o LinkedIn, será excluído após sete dias; já o CSV para usuários de importação será excluído imediatamente.

## Conector do LinkedIn Learning {#linkedinlearningconnector}

O conector do LinkedIn é usado por clientes empresariais do LinkedIn.com que querem que os alunos descubram e realizem cursos do Learning Manager. O conector pode ser configurado para buscar cursos periodicamente com sua chave de API. Depois que um curso é criado no Learning Manager, ele pode ser pesquisado e realizado pelos usuários. O progresso do aluno pode ser acompanhado no Learning Manager.

>[!NOTE]
>
>Você receberá as IDs exclusivas do OA para todos os cursos importados do conector do LinkedIn Learning para o Adobe Learning Manager.

>[!NOTE]
>
>O tempo de aprendizado gasto nos cursos do LinkedIn Learning é comunicado pelo conteúdo do LinkedIn/plataforma do LinkedIn para a plataforma de aprendizado do Learning Manager. Se o LinkedIn Learning não enviar o tempo de aprendizado, ele não poderá ser gravado pela nossa plataforma de aprendizado. Nesse caso, o tempo de aprendizado gasto exibido pelo Learning Manager é zero.

### Defina as configurações no portal do Linkedln Learning {#configure-settings-in-linkedln-learning-portal}

1. Faça logon no Linkedln Learning LMS como administrador.
1. Clique em **[!UICONTROL admin]** no painel de navegação superior.
1. Clique na guia **[!UICONTROL Configurações]** na tela seguinte.
1. Selecione **[!UICONTROL Integração de Reprodução]** no painel de navegação esquerdo e clique na guia **Integração**.
1. Clique em **[!UICONTROL Configurações de Inicialização de Conteúdo do LMS]** para expandir suas configurações.
1. Adicione os seguintes três nomes de host: **learningmanager.adobe.com**, **learningmanagerlrs.adobe.com**, **cpcontents.adobe.com**
1. Selecione **[!UICONTROL Habilitar integração AICC]**.

   ![](assets/linkedin-learning.png)

   *Configuração do LinkedIn Learning*

### Configurar o conector do LinkedIn Learning {#configure-linkedin-learning-connector}

1. No painel Administrador de Integração, clique em [!UICONTROL LinkedIn Learning]. As opções Introdução, Conectar e Gerenciar conexões serão exibidas.
1. Se você estiver configurando o conector do LinkedIn Learning pela primeira vez, clique em [!UICONTROL Conectar].

   <!--Configure the Exavault FTP account before you configure this connector.

   ![](assets/configure.jpg)
   *Configure connection*-->

1. Na página de conexão, especifique um nome para o conector. Insira a chave do aplicativo e a chave secreta da sua conexão.

   >[!NOTE]
   >
   >O administrador corporativo pode gerar um novo aplicativo a partir do portal de administração do LinkedIn Learning para obter a chave de aplicativo e a chave secreta.

1. Clique em **[!UICONTROL Salvar]**.

   A configuração é salva e a conexão do LinkedIn Learning à sua conta é adicionada. Agora você pode clicar em **[!UICONTROL Gerenciar Conexões]** na home page e editar sua configuração a qualquer momento.

1. Se você já tiver uma conexão estabelecida, clique em **[!UICONTROL Gerenciar Conexões]** para exibir todas as conexões.

   >[!NOTE]
   >
   >O recurso de migração da sua conta deve ser habilitado antes de configurar este conector.

1. Clique na conexão que quer editar.
1. No painel esquerdo, clique em Configurar. Siga um destes procedimentos:

   * Exiba ou edite os detalhes de sua conta e o agendamento de sincronização nesta janela. Marque a caixa de seleção **[!UICONTROL Habilitar Conexão]** se quiser habilitar esta conta.
   * Clique em **[!UICONTROL Editar]** e edite suas credenciais. Para desfazer suas atualizações neste campo clique em Redefinir.
   * Clique em **[!UICONTROL Habilitar Agendamento]** para agendar sua sincronização. Insira a hora e data de início e, em seguida, insira a frequência do agendamento de sincronização em dias. Por exemplo, habilitar a sincronização a cada três dias.

   Clique em **[!UICONTROL Salvar]** para salvar as alterações.

1. No painel esquerdo, clique em **[!UICONTROL Execução sob demanda]**. Essa opção permite importar feeds do usuário e outros dados relevantes do LinkedIn. Informe a Data de Início para a execução sob demanda e clique em Executar para executar a sincronização. Todos os dados a partir da data de início até o presente serão importados.

   * Você pode clicar em **[!UICONTROL Desabilitar acesso]** ao Learning Manager durante a execução quando o aplicativo tiver um tempo de inatividade durante a sincronização.
   * Se você clicar em **[!UICONTROL Habilitar acesso]** ao Learning Manager durante a execução, não haverá interrupção no serviço durante a sincronização.

   ![](assets/ondemandexecution.jpg)

   *Execução sob demanda do relatório*

1. Também é possível clicar no Status da execução no painel esquerdo, a qualquer momento, para visualizar o resumo de todas as execuções deste conector, em ordem cronológica. Você pode ver a data de início e a duração da sincronização, o tipo da sincronização (se é ou não uma sincronização sob demanda) e o status da sincronização (se está em andamento ou concluída).

   ![](assets/executionstatus.jpg)

   *Status de execução do relatório*

   >[!NOTE]
   >
   >Ao excluir e recriar uma conexão, as execuções anteriores do conector retornam. É possível ver todas as execuções anteriores à exclusão da conexão.

   É possível executar outra vez somente a sincronização mais recente.

### Filtrar conteúdo do LinkedIn Learning {#filter-linkedin}

Há filtros nos conectores do LinkedIn para segregar conteúdo com base nas bibliotecas do LinkedIn Learning. Além disso, você também pode filtrar o conteúdo com base no idioma e na biblioteca e importar apenas os cursos nos idiomas necessários. Depois de importado, o conteúdo é segregado em vários catálogos com base na configuração de importação.

Os filtros são os seguintes:

**Filtrar treinamento usando:** Filtra um subconjunto de cursos do LinkedIn no Learning Manager.

* **Com base no idioma**

![](assets/filter-language.png)

*Filtrar por idioma*

* **Com base na biblioteca do LinkedIn Learning**

![](assets/filter-catalog.png)

*Filtrar por catálogo*

**Importar treinamentos para**

![](assets/iport-training.png)
*Importar treinamento para catálogos*

**Importar tags**

Há um tipo de tag, **Tag personalizada**, que você pode usar para adicionar tags personalizadas aos cursos do LinkedIn Learning. Você pode adicionar quantas tags desejar, separadas por vírgulas.

![](assets/add-custom-tags.png)

*Adicionar marcas personalizadas*

O conteúdo é salvo somente após a migração. O conteúdo será salvo nos respectivos catálogos.

## Conector do Power BI {#powerbiconnector}

>[!NOTE]
>
>O Learning Manager é compatível com a integração somente com uma licença comercial do Microsoft Power BI. Ele não se integra ao Microsoft Power BI na nuvem do Governo.

É possível usar a integração com este conector para aproveitar as contas existentes do Power BI para analisar e visualizar os dados de aprendizado do Learning Manager no Power BI. Durante a configuração, o administrador de integração pode configurar a área de trabalho do Power BI para que seja preenchida gradualmente com dois conjuntos de dados ao vivo: relatórios de transcrição do aluno e de habilidade do usuário. Você pode usar todos os recursos e o poder do Power BI para desenvolver, implantar e distribuir painéis personalizados como preferirem em suas empresas.

### Como configurar o conector {#configuring-the-connector}

Para configurar o conector, na página **[!UICONTROL Conectores]**, passe o mouse sobre o bloco **[!UICONTROL Power BI]** e clique em **[!UICONTROL Conectar]**. A página Power BI é aberta. Para estabelecer uma conexão, forneça a ID do cliente do aplicativo, o segredo do cliente do aplicativo, o nome do inquilino e a ID da área de trabalho (opcional). Para obter essas credenciais, siga estas etapas.

![](assets/power-bi-configurepage.png)

*Configurar o conector do Power BI*

1. Iniciar <https://app.powerbi.com/embedsetup>.
1. Clique em **[!UICONTROL Incorporar à sua organização]** e faça logon na sua conta da Microsoft.
1. Insira o nome do aplicativo.
1. Na seção Tipo de aplicativo, selecione a opção Aplicativo Web do servidor.
1. Na seção **[!UICONTROL Redirecionar URL]**, selecione a opção **Usar uma URL personalizada** (Escolha esta opção se souber a URL do aplicativo de destino). Insira o seguinte URL:

   `https://learningmanager.adobe.com/ctr/app/azure/_callback` (atualizar o domínio com base no ambiente)

1. No campo URL Inicial, insira a seguinte URL: `https://learningmanager.adobe.com/`
1. Na seção de permissões, selecione **Ler todos os conjuntos de dados** e **Ler e gravar todos os conjuntos de dados**.

   Obtenção do inquilino: entre em contato com seu administrador do Power BI para fornecer o nome do inquilino.

   Como obter a ID do local de trabalho: a criação do local de trabalho só é possível para usuários do Power BI Pro. Você pode criar um local de trabalho no Power BI e obter a ID do URL.

1. Clique em **[!UICONTROL Registrar aplicativo]** e armazene a ID do cliente e o Segredo do cliente.

>[!NOTE]
>
>Se quiser autorizar a conexão novamente, você deve criar outro Power App e especificar o URL de redirecionamento com a nova marca.

Você pode exportar as transcrições do aluno, as habilidades do usuário e o relatório de atividades da xAPI usando o mesmo método. Escolha Transcrições do aluno/Habilidades do usuário no painel esquerdo. A página Exportar será aberta.

Habilite a **[!UICONTROL caixa de seleção Ativar exportação de habilidade do usuário/Transcrição do aluno usando esta conexão]**. Salve a alterações.

**Configuração de exportação**: se quiser agendar a extração do relatório. Marque a caixa de seleção **[!UICONTROL Habilitar Agendamento]** e especifique a data e a hora de início. Também é possível especificar o intervalo no qual deseja que o relatório seja gerado e enviado.

![](assets/power-bi-configureuserskillpage.png)

*Exportar a configuração para agendar o relatório*

**Exportar por demanda:** você pode especificar a data de início e exportar o relatório usando a opção . O relatório é extraído da data inserida até a presente.

![](assets/power-bi-userskillondemandpage.png)

*Exportar por demanda*

Os dados exportados podem ser exibidos acessando sua conta do Power BI. Os dados exportados são listados na opção de conjuntos de dados.

### Exportar relatórios de atividades da xAPI no Learning Manager {#export-xapi-activity-reports-in-captivate-prime}

Na página Recursos PowerBI-xAPI, clique em **[!UICONTROL Exportar relatório de atividades da xAPI]**.

![](assets/powerbi-dashboard.png)
*PowerBI - Exportar Relatório de Atividades da xAPI*

No painel esquerdo, selecione **Configuração** e siga as etapas abaixo:

* Preencha o campo do caminho JSON que corresponde ao nome da coluna e o tipo de string.
* Para adicionar mais caminhos JSON, clique em **[!UICONTROL Adicionar]**.
* Você pode editar as entradas nos campos de caminho JSON clicando em **[!UICONTROL Editar]**.
* Clique em **[!UICONTROL Salvar]** para salvar as alterações.

**Configurar agendamento**

No painel esquerdo, clique em **[!UICONTROL Configurar agendamento]** e faça o seguinte:

* Clique em Habilitar exportação das instruções da xAPI usando esta conexão.
* Selecione a caixa de seleção **[!UICONTROL Habilitar agendamento]** e especifique a data e a hora de início. Também é possível especificar o intervalo de dias em que deseja que a exportação se repita e seja enviada.
* Clique no botão **[!UICONTROL Salvar]** para salvar as definições em Configurar agendamento.

![](assets/configure-schedule.png)
*Agenda de Configuração de Exportação xAPI*

**Sob demanda**

No painel esquerdo, clique em **[!UICONTROL Sob demanda]** e especifique a data de início na página Exportar instruções da xAPI-Sob demanda.

![](assets/on-demand-2.png)
*Exportação xAPI sob demanda*

Todos os dados exportados serão exibidos em um conjunto de dados criado pela Adobe em sua conta do PowerBI.

A exportação da xAPI no PowerBI falha se algumas instruções da xAPI em LRS não tiverem um caminho JSON configurado para exportação. Para obter as instruções da xAPI quando o caminho JSON não estiver disponível, o valor constante N/D deve ser adicionado e exibido no PowerBI.

**Status da execução**

Selecione **Status da execução** para ver o resumo de todas as tarefas em ordem cronológica. O sinal de aviso indica falhas durante a execução. Você pode baixar relatórios de erros como **CSV** clicando no link do relatório de erros.

![](assets/execution-status.png)
*Status de execução de exportação da xAPI*

### Relatórios unificados {#unified-reports}

O Learning Manager fornece uma maneira de exportar com uma combinação de relatórios como dados do usuário, transcrição do aluno, gamificação, relatórios de feedback e muito mais, como um conjunto de dados único para o Power BI.

Isso permite que os usuários do Power BI mesclem os dados de vários relatórios para apresentar análises e visualizações muito poderosas no Power BI.

![](assets/unified-power-bireports.png)
*Relatórios de Power BI unificados*

**Exportação sob demanda**

Especifique a data de início e a data de término e exporte o relatório usando a opção. O relatório é extraído para o período especificado.

![](assets/on-demand-export.png)
*Exportação sob demanda*

**Exportação agendada**

Se você deseja agendar a extração do relatório. Selecione a caixa de seleção **Habilitar agendamento** e especifique a data e hora de início. Também é possível especificar o intervalo no qual deseja que o relatório seja gerado e enviado.

![](assets/configure-schedule.png)
*Configurar agendamento*

Você também pode exportar Relatórios de treinamento para o Power BI.

Os Relatórios de treinamento podem ser exportados para o Power BI como parte do recurso Relatórios unificados.

O Relatório de treinamento tem dois campos adicionais:

* Número de usuários que compartilharam feedback em um curso
* Classificação de estrelas média para um curso

### Status do filtro de transcrições do aluno {#lt-status}

Na seção Relatórios unificados de uma conexão do Power BI, há uma opção para exportar transcrições do aluno com base no status dos Objetos de aprendizado.

* **Selecionar tudo:** Exporte todos os registros ou atividades no nível do módulo no intervalo de datas especificado.
* **Concluído:** Exporte todos os registros concluídos no intervalo de datas.
* **Em andamento:** exporte todos os registros que têm o status- Em andamento.
* **Não iniciado:** exclua os registros que estão inscritos no intervalo de datas especificado, mas não foram iniciados ao gerar o relatório.

* **Não inscrito:** Inclua todos os registros não inscritos no intervalo de datas.

![](assets/lt-filters.png)
*Status do filtro de transcrições de aprendizado*

Você pode exportar a lista obrigatória e usar o Power BI para analisar o relatório mais tarde.

### Baixar modelos de Power BI {#template}

O Learning Manager também fornece modelos de Power BI prontos. Esses modelos oferecem melhor capacidade de análise aos administradores de conta da Adobe Learning Manager.

Você pode baixar os modelos, exportar relatórios relevantes e criar relatórios de plotagem usando esses modelos disponíveis facilmente.

![](assets/download-power-bi-template.png)
*Baixar modelos do Power BI*

Isso permite que os usuários baixem esses modelos e os usem no aplicativo Power BI e os personalizem ainda mais, e faz com que seus relatórios contem uma história convincente.

[**Baixar os modelos**](https://documentcloud.adobe.com/link/track?uri=urn:aaid:scds:US:842bb6a2-cd7d-4c3d-b968-da38bc1cc18a)

<!--<table> 
 <tbody>
  <tr> 
   <td><img src="assets/download.png"></td> 
   <td><p> </p> <p><a disablelinktracking="false" href="https://documentcloud.adobe.com/link/track?uri=urn:aaid:scds:US:842bb6a2-cd7d-4c3d-b968-da38bc1cc18a"><strong><em>Download the templates</em></strong></a></p></td> 
  </tr> 
 </tbody>
</table>-->

Também pode baixar os modelos manualmente através do link acima. Use os modelos e personalize seus relatórios adequadamente.

### Exportar relatório de treinamento {#export-training-report}

Os relatórios de treinamento podem ser exportados para o Power BI como parte do recurso Relatórios unificados.

O Relatório de treinamento tem estes campos adicionais:

* Número de usuários que compartilharam feedback em um curso
* Classificação de estrelas média para um curso

![](assets/export-training-report.png)
*Exportar relatório de treinamento*

### Alterações relacionadas ao Caminho de aprendizado {#learning-path-related-changes}

#### Administrador: Transcrições de aprendizado e Relatório unificado {#learning-transcripts-and-unified-reports}

**Conexões existentes**

Se a opção Caminho de aprendizado estiver desativada na conta do administrador, nenhuma linha e coluna será adicionada nos relatórios.

Se a opção Caminho de aprendizado estiver ativada na conta do administrador, o relatório conterá o tipo de coluna Caminho de aprendizado (Nível superior) para todos os alunos inscritos em um caminho de aprendizado.

**Novas conexões**

Se a opção Caminho de aprendizado estiver desativada na conta do administrador, o relatório de treinamento consistirá das seguintes colunas:

* Caminho incorporado: exibe o nome do programa de aprendizado
* ID do caminho incorporado: exibe as IDs do programa de aprendizado.
* ID do curso incorporado: exibe as IDs dos cursos que estão dentro de um caminho de aprendizado.

Além disso, o relatório conterá o tipo de coluna Caminho de aprendizado (Nível superior) para todos os alunos inscritos em um caminho de aprendizado.

Na coluna Tipo, Programa de aprendizado será renomeado como Caminho de aprendizado. Para conexões existentes, não haverá alterações. No entanto, para novas conexões, as alterações serão refletidas após 30 dias.

#### Relatório de treinamento: Relatório unificado {#training-report}

**Conexões existentes**

Se a opção Caminho de aprendizado estiver desativada na conta do administrador, nenhuma linha e coluna será adicionada nos relatórios.

Se a opção Caminho de aprendizado estiver ativada na conta do administrador, o relatório conterá a coluna “Tipo”. A coluna contém o novo valor “Caminho de aprendizado (nível superior), onde aplicável”.

**Novas conexões**

Se a opção Caminho de aprendizado estiver desativada na conta do administrador, o relatório de treinamento consistirá das seguintes colunas:

* **Caminho incorporado:** exibe o nome do programa de aprendizado
* **ID do caminho incorporado:** exibe as IDs do programa de aprendizado.
* **ID do curso incorporado:** exibe as IDs dos cursos que estão dentro de um caminho de aprendizado.

Além disso, o relatório conterá o tipo de coluna Caminho de aprendizado (Nível superior) para todos os alunos inscritos em um caminho de aprendizado.

Na coluna Tipo, Programa de aprendizado será renomeado como Caminho de aprendizado. Para conexões existentes, não haverá alterações. No entanto, para novas conexões, as alterações serão refletidas após 30 dias.

## FTP personalizado {#custom-ftp}

**Pré-requisitos**

>[!NOTE]
>
>Para configurar seu FTP personalizado, entre em contato com seu CSM. O CSM fornecerá os detalhes necessários para a configuração do FTP.
>
>Configurar o FTP envolve um tempo de execução e requer suporte de TI para permitir a lista de IPs e portas, além de criar determinadas pastas com permissões específicas no servidor FTP.

O Learning Manager fornece a capacidade de se conectar ao seu local de FTP personalizado.

Seu FTP será compatível com:

### Importação de dados {#data-import-2}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no serviço FTP do Learning Manager e importe-os automaticamente para o Learning Manager. Com esse recurso, você pode integrar vários sistemas colocando o CSV gerado por eles nas pastas apropriadas das contas FTP. O Learning Manager pega os arquivos CSV, combina os arquivos e importa os dados conforme o agendamento. Consulte o recurso Agendamento para obter mais informações.

**Mapear atributos**

O administrador de integração pode escolher colunas de CSV e mapeá-las para os atributos agrupáveis do Learning Manager. Este mapeamento é uma tarefa única. Uma vez que o mapeamento está feito, este mesmo mapeamento é usado em importações subsequentes do usuário. O mapeamento poderá ser reconfigurado se o administrador quiser um mapeamento diferente para importar usuários.

### Exportação de dados {#data-export-3}

A exportação de dados permite que os usuários exportem habilidades do usuário e transcrições dos alunos para o FTP para serem integrados a um sistema de terceiros.

### Agendar relatórios {#schedule-reports-2}

O administrador pode configurar tarefas de agendamento conforme os requisitos da organização, enquanto os usuários no aplicativo Learning Manager são atualizados conforme a agenda. Da mesma forma, o administrador de integração pode programar a exportação de habilidades em tempo hábil para integração com um sistema externo. A sincronização pode ser realizada diariamente no aplicativo Learning Manager.

Para configurar seu próprio FTP, faça logon como um administrador de integração e clique em **[!UICONTROL FTP personalizado]** > **[!UICONTROL Conectar]**.

Há dois tipos de autenticação:

![](assets/custom-ftp-authenticationoptions.png)
*Opções de autenticação por FTP personalizado*

* **Básico:** na autenticação básica, você só precisará fornecer a url, o nome de usuário e a senha do domínio FTP. Depois de fornecer os detalhes, clique em Conectar.
* **Certificação:** se o FTP do cliente oferecer suporte à autenticação de certificado, ele poderá escolher esta opção. Depois de clicar em Gerar chave SSH, a chave SSH é baixada para a máquina local. Ao abrir o arquivo, a chave aparece como,

![](assets/ssh-public-key.png)
*Chave pública SSH*

Você deve colocar essa chave pública no servidor FTP antes de adicionar os detalhes abaixo. Depois de definir a chave fornecida como a chave pública do FTP, forneça o URL do domínio FTP e o nome de usuário e clique no botão **Conectar** para configurar a conexão.

Após a configuração da conexão, as pastas de importação e exportação são criadas automaticamente no local de ftp. Depois que a funcionalidade de importação/exportação é fornecida pelo FTP personalizado.

>[!NOTE]
>
>Um conector FTP personalizado pode ser configurado somente com servidores SFTP.

## Conector do ADFS {#adfsconnector}

Pré-requisitos para configurar uma conexão ADFS:

* Faça logon no Portal do Azure usando esta URL: [https://portal.azure.com/](https://portal.azure.com/) antes de registrar o aplicativo.
* Abra o Azure Ative Diretory.

## Etapas para registrar seu aplicativo {#steps-to-register-your-application}

* Clique em Azure Active Directory. Clique em **[!UICONTROL Adicionar]** > **[!UICONTROL Registro de aplicativo]**.

  <!--![](assets/add-app-registration.png)-->
  <!-- *Add app registration*-->

* Insira o nome do aplicativo.

  <!--![](assets/register-app.png)-->
  <!--*Enter the name of the application*-->

  Clique em **[!UICONTROL Registrar]**.

* No painel direito, selecione **[!UICONTROL Certificados e Segredos]**.

  <!--![](assets/add-client-secret.png)-->

  <!--*Select Certificates and Secrets*-->

* Adicione um segredo do cliente.

  <!--![](assets/add-description.png)-->

  <!--*Add a client secret*-->

* Adicione uma descrição ao segredo e defina seu prazo de validade para 24 meses.

  <!-- ![](assets/copy-values.png)-->

  <!--*Add description*-->

* Copie o valor e o segredo para, por exemplo, o bloco de notas.

  <!-- ![](assets/copy-secret.png)-->

  <!--*Copy value and secret key*-->

* Selecione **Permissões de API**.

  <!--![](assets/click-api-permission.png)-->

  <!-- *Left pane containing API Permissions*-->

* Selecione **Adicionar permissões**. Além disso, habilite a opção **Conceder consentimento do administrador**.

  ![](assets/add-permission.png)

  *Adicionar permissões*

* Selecione **Microsoft Graph**.

  <!--![](assets/ms-graph.png)-->

  <!--*Select Microsoft Graph*-->

* Selecione **Permissões do aplicativo**.

  ![](assets/request-api-permission.png)

  *Selecionar permissões do aplicativo*

* Procure *diretório* e selecione **Ler dados do diretório**.

  ![](assets/read-directory-data.png)

  *Selecionar Ler dados do diretório*

* Digite *usuário* como o termo de pesquisa.

  ![](assets/search-user.png)

  *Insira o termo de pesquisa*

* Selecione **Ler os perfis completos de todos os usuários**.

  ![](assets/select-read-all.png)

  *Selecione Ler os perfis completos de todos os usuários*

* Selecione **Adicionar permissões**.

  <!--![](assets/select-add-permission.png)-->

  <!-- *Select Add Permissions*-->

### Página Configuração do ADFS {#adfs-configuration-page}

1. Na página de configuração do ADFS no Adobe Learning Manager, insira a ID do cliente e o Segredo do cliente obtidos anteriormente.

   Clique em **[!UICONTROL Conectar]**.

1. Faça logon no **portal.azure.com**. Os valores serão preenchidos nos campos ID do locatário e Domínio primário.

### Importar {#import-8}

#### Mapear atributos {#map-attributes-6}

O administrador de integração pode escolher atributos do ADFS e mapeá-los para os atributos agrupáveis correspondentes do Learning Manager. Uma vez que o mapeamento é concluído, este mesmo mapeamento é usado em importações subsequentes do usuário. Ele pode ser reconfigurado se o administrador quiser ter um mapeamento diferente para importar usuários.

#### Importação automatizada de usuário {#automated-user-import-4}

O processo de importação de usuário permite que o administrador do Learning Manager busque detalhes dos funcionários no ADFS e importe-os automaticamente para o Learning Manager.

#### Como filtrar usuários {#filtering-users-4}

O administrador do Learning Manager pode aplicar filtros aos usuários antes de importá-los. Por exemplo, o administrador do Learning Manager pode importar todos os usuários da hierarquia sob um ou mais gerentes específicos.

Para configurar o conector do ADFS, entre em contato com a equipe de CSM do Learning Manager.

## Configurar o conector do ADFS {#configure-adfs-connector}

1. Na página inicial do Learning Manager, passe o mouse sobre a miniatura/cartão do ADFS. Será exibido um menu. Clique na opção Conectar no menu.

   ![](assets/adfs1.jpg)

   *Miniatura do AD FS*

1. Clique em Conectar para configurar uma nova conexão. A página do conector do ADFS é exibida. Insira os detalhes da conta que quer mapear.

   ![](assets/adfs2.jpg)

   *Estabelecer conexão*

1. Se quiser importar o usuário do ADFS diretamente como um usuário interno do Learning Manager, use a opção Importar usuários internos.

   ![](assets/adfs3.jpg)

   *Importar usuário para o Learning Manager*

1. Na página de mapeamento, à esquerda   lado, você pode ver as colunas do Learning Manager e, à direita,   lado você pode ver as colunas do ADFS. Selecione o nome da coluna apropriada que faz mapeamento para o nome da coluna do Learning Manager.

   ![](assets/adfs4.jpg)

   *Mapear atributos*

1. Para exibir e editar a fonte de dados, como administrador, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Fonte de Dados]**.

   A origem do AD FS estabelecida será listada. Se você precisar editar o filtro, clique em **[!UICONTROL Editar]**.

   ![](assets/datasource.jpg)
   *Configuração da fonte de dados*

1. Você receberá uma notificação após a conclusão da importação. Para exibir ou editar o log de importação, clique em **[!UICONTROL Usuários]** > **[!UICONTROL Log de importação]**.

### Excluir uma conexão {#delete-a-connection-1}

Para excluir uma conexão miniOrange estabelecida, siga estas etapas.

## Adobe Connect {#connect}

1. No Adobe Connect, clique nos três pontos do cartão e escolha **Conectar**.
1. Clique no link **Configurar Agora** na seção Configuração do Adobe Connect.
1. Forneça o nome de domínio do Adobe Connect da sua empresa e as credenciais de logon.

   Um exemplo de URL do Adobe Connect é: ***minhaempresa.adobeconnect.com***

   Você deve fornecer a ID do e-mail do administrador da conta do Adobe Connect.

   >[!NOTE]
   >
   >Somente contas do Connect hospedadas pela Adobe são compatíveis com o Learning Manager. Exemplo; &#39;.adobeconnect.com&#39;.

1. Clique em **[!UICONTROL Integrar]**.

   Após autenticar a ID de e-mail, o Learning Manager exibe a mensagem enquanto o Connect é integrado com êxito. Você pode começar a visualizar seus cursos em sala de aula virtual usando o Adobe Connect automaticamente.

   **Depois que o administrador da conta do Connect autenticar a sua ID de e-mail, a solicitação será aprovada pela equipe de back-end do Adobe Connect. Geralmente leva um ou dois dias para a integração ser aprovada e configurada.**

   >[!NOTE]
   >
   >O administrador da conta do Adobe Connect deve aceitar os Termos e condições de uso do Adobe Connect. Se não for aceito, a autenticação do logon pode falhar. Após criar a conta do Adobe Connect, faça logon na conta uma vez. Durante o primeiro logon, uma página de termos e condições é exibida.

### Adicionar informações da sessão da sala de aula virtual {#add-virtual-classroom-session-information}

Se o autor de um curso em sala de aula virtual não tiver fornecido as informações da sessão, o administrador poderá incluir os detalhes da sessão.

No logon do administrador, clique no nome do curso de sala de aula virtual. Clique em Instâncias no painel esquerdo e em Detalhes da sessão.  Clique no ícone Editar no canto direito da página Detalhes da sessão para adicionar as informações da sessão.

Com a integração do Adobe Learning Manager e Adobe Connect para a criação de módulos ou sessões de sala de aula virtual, sua conta do Connect deve ser compatível com salas de reunião com número adequado de salas e usuários simultâneos para o seu caso de uso. Essas salas de reunião são usadas para hospedar os módulos de sala de aula virtual do Learning Manager. Uma nova sala de reunião do Connect é criada dinamicamente pelo Learning Manager para cada módulo ou sessão de sala de aula virtual no Learning Manager.

>[!NOTE]
>
>Você deve adquirir o Adobe Connect separadamente, além do Adobe Learning Manager.

### Sala de reunião permanente do Adobe Connect {#persistent}

No Adobe Connect, os clientes usam as salas de reuniões existentes que já foram criadas no Connect. Todas as salas de reunião do Connect são permanentes e os modelos de sala de reuniões são configurados com cuidado para fornecer uma experiência unificada para cada sala permanente.

Você pode criar uma sessão de sala de aula virtual usando uma sala já criada no Adobe Connect.

O Learning Manager também permite que os alunos entrem na sala do Connect para suas sessões virtuais usando um método de autenticação.

![](assets/adobe-connect-authentication.png)
*Autenticação do Adobe Connect*

Ao criar um módulo de sala de aula virtual usando o Adobe Connect, você pode selecionar uma sala permanente. Se a opção **Não** for selecionada, será criada uma sala de reuniões dinâmica como antes.

![](assets/persistent-room-selection.png)
*Seleção de sala persistente*

Quando um aluno faz um curso pelo Adobe Connect e termina, depois de algum tempo, a gravação da sessão junto com a senha é exibida no aplicativo do aluno.

![](assets/connect-recording.png)
*Conectar gravação*

### Importar pontuações do questionário do Adobe Connect {#quiz-adobe-connect}

Importe os dados do questionário do Connect para o Learning Manager e integre-os com o fluxo de trabalho de relatórios existente para que os usuários do Learning Manager possam obter dados do questionário, respostas do usuário e pontuações das sessões do Adobe Connect dentro do relatório, como a maneira como eles estão disponíveis para os módulos individuais com questionários.

Na seção do Connect, se qualquer aluno fizer um curso de questionário ou qualquer interação que seja compatível com relatórios de questionário, todas as interações dos alunos serão rastreadas, além da conclusão. O curso deve ser um treinamento VC do Connect.

Aqui está um breve fluxo de trabalho do processo.

**Adobe Connect - Host**

* O host no Connect cria um curso e carrega conteúdo que contém um questionário interativo.
* O host cria um treinamento de **sala de aula virtual** e salva-o. O host tem a opção de vincular o curso criado acima ao VC ou pode usar a opção **Compartilhar curso** no aplicativo Connect durante a sessão para compartilhar o curso.

**Learning Manager - Autor**

* O autor cria um curso no Learning Manager com o tipo de módulo como **Sala de aula virtual.**
* Na lista suspensa **Sistema de Conferência**, escolha Conectar como provedor VC.
* Escolha o curso Reunião persistente e selecione a sala de aula VC criada pelo host no Connect. Escolha o professor. Salve e publique o curso.

**Learning Manager - Aluno**

* Depois que o curso é publicado, o aluno se inscreve no curso.
* O aluno é redirecionado para a sessão VC do Connect, na qual ele/ela tem acesso à sessão VC pelo host do Connect.

**Adobe Connect - Host**

* Na sessão VC, o host do Connect compartilha o questionário que foi compartilhado anteriormente.

**Adobe Connect - Aluno**

* O aluno faz o questionário e fecha a sessão após a sua conclusão.

**Learning Manager - Aluno**

* O aluno fecha a sessão e ela é sincronizada automaticamente.

**Learning Manager - Administrador**

* Depois que a sessão expirar, o fluxo de trabalho de importação do questionário será acionado após a duração programada.
* Aguarde até que a programação seja acionada e o processamento seja concluído. Para verificar o status do processamento no lado do administrador de integração, você pode ver o **status de execução** no conector do Adobe Connect para observar o progresso. Assim que a execução for bem-sucedida, o status será alterado para **Concluído**.

* Em seguida, o administrador escolhe o curso do Learning Manager criado anteriormente. O administrador vê o seguinte:

   * **Participação e pontuação** - Exibe a pontuação final do questionário e o status da participação.
   * **Pontuação do questionário L2**

      * **Por usuário** - Exibe a pontuação final do quiz exibida como **Pontos** e **Porcentagem**.
      * **Por pergunta** - Exibe as informações do questionário como um gráfico de relatório.

## Conector do Marketo Engage {#marketo}

O Learning Manager integra-se ao Marketo Engage, um software de automação de marketing que ajuda a executar campanhas de marketing.

O conector do Marketo Engage foi projetado para adicionar (ou atualizar) leads no banco de dados do Marketo Engage quando um novo usuário é adicionado à conta do Learning Manager. Ele também associa os comportamentos de aprendizado do usuário no Learning Manager (inscrição no curso, conclusão do curso, atribuição de habilidades e realização de habilidades) como objetos personalizados com os leads correspondentes no Marketo Engage. Isso permite que um comerciante use essas informações para segmentar os públicos com base em seus comportamentos de aprendizado capturados do Learning Manager e use recursos de Marketo Engage como “Smart Lists”.

Como administrador de integração, você pode integrar o Learning Manager a uma instância do Marketo Engage para automatizar a sincronização de dados. Você pode exportar usuários internos e exportar inscrições de treinamento e eventos de conclusão de habilidades. As operações podem ser executadas de acordo com um cronograma e podem ser configuradas sob demanda.

Para que o Learning Manager se integre com a sua conta da Marketo, a sua conta da Marketo precisa ter a capacidade de criar esquemas por APIs.

No aplicativo Marketo, você pode baixar estes três relatórios:

* Relatório do usuário
* Transcrição de aprendizado
* Relatório de habilidades do usuário

Ao criar uma conexão Marketo Engage, você deve fornecer os seguintes detalhes:

* Nome da conexão
* ID do cliente
* Segredo do cliente
* Domínio Marketo Engage

![](assets/marketo-creds.png)

*Insira as credenciais para o Marketo*

>[!NOTE]
>
>Você pode obter a ID do cliente e o segredo do aplicativo Marketo Engage. No aplicativo da Marketo, você pode obter a ID do cliente e o segredo da seção **LaunchPoint** e o Domínio do Marketo da seção **WebServices**.

Na seção **Relatórios unificados** da conexão do Marketo Engage no aplicativo Learning Manager, você pode criar campanhas com base no seguinte:

* Um novo usuário foi adicionado ao Learning Manager
* Um novo usuário foi inscrito em um curso
* Um novo usuário concluiu um curso
* Um aluno foi inscrito em uma habilidade
* Um aluno obteve uma habilidade

Como qualquer outro conector, você pode programar e exportar dados sob demanda.

### Mapeamento de colunas no Marketo Engage {#column-mapping-in-marketo-engage}

No Marketo, há dois tipos de bancos de dados:

* Banco de dados de leads
* Banco de dados de objetos personalizados

O mapeamento de coluna é usado para criar o banco de dados de leads. Os clientes potenciais são os usuários exportados do Relatório do usuário.

Os campos do Relatório do usuário são listados na coluna Adobe Learning Manager. Os campos na coluna Marketo são os que o Marketo fornece. Usando as duas colunas, é possível mapear qualquer campo no Learning Manager para esse campo no Marketo. Em uma coluna do Learning Manager, você se associa a uma coluna relacionada do Marketo. Depois de unir as colunas, um banco de dados de leads é criado.

Em seguida, você pode exibir todos os usuários exportados no Marketo.

Na seção **Objetos personalizados do Marketo** no aplicativo Marketo, você pode ver que todos os três relatórios, Transcrição do aluno, Habilidade do usuário e Relatório do usuário, estão presentes. Esses relatórios têm a sequência de caracteres **”cp_”** anexada a cada um. Cada novo usuário que é exportado para o Marketo é considerado um lead.

### Eventos

Exporte dados de eventos do Learning Manager para uma instância do Marketo Engage. Selecione os eventos a serem exportados para o banco de dados do Marketo Engage sob demanda ou em uma programação.

* Adição de novo usuário
* Atualizar metadados do usuário
* Atualizar atividade do usuário
* Inscrição no treinamento
* Autoinscrição
* Conclusão de habilidade

<!--## BlueJeans Events {#bj-events}

BlueJeans Events connector connects Learning Manager and BlueJeans systems to automate data synchronization. Using this connector, you can:

* **Set up virtual sessions using BlueJeans Events:** Configure a new event in BlueJeans and setup a VC session in Learning Manager by selecting the appropriate BlueJeans event. Date and time details are picked automatically from the BlueJeans events.
* **Automated User Completion Syncing:** An Automated user completion syncing process allows the Learning Manager Administrator to fetch completion records for BlueJeans events automatically.

This new connector requires a separate set of credentials to configure the connector. The credentials of the existing BlueJeans Meetings connector will not work for BlueJeans Events connector.

![](assets/bj-event-connector.png) 
*Credentials for BlueJeans Event Connector*

### Workflow {#workflow}

1. The BlueJeans Event moderator creates an event from within BlueJeans.
1. The author creates BlueJeans event course using the BlueJeans event url, which is created in future dates.
1. Since BlueJeans events have a similar title for multiple events, the author must append the event attendee url to the room name, so that he/she can choose the appropriate event.

   The format to enter event url: ***event name--event attendee url***

   For Dynamic rooms, the behavior is similar to that of Adobe Connect.

   ![](assets/bj-eventname.png)
   *BlueJeans Events configuration*

1. Once the author enters the BlueJeans event url, the date and time will be auto populated.
1. Add an instructor to the event. The instructor will now have elevated privileges as a Presenter in a BlueJeans event.

Administrators, managers, and learners can enroll learners to the created course. Upon enrollment, the learner receives an email. The learner can sign in to their Learning Manager account to view the program details and take the course.

When the course is complete, the completion report gets triggered after a scheduled duration. The administrator can see the completion report to check the attendance and score of the learners.

If the BlueJeans Event moderator enables the recording during the session, after session ends, the recording is available in the learner app.

![](assets/bluejeans-event-configure.png)
*BlueJeans Events configuration*

When you enable the check-box **Fetch Events created by the other users**, you can then add the list of BlueJeans event creators in the **Additional Event Creators** field. In the Author app, only events created by these users are searchable via the type-ahead field.

If the **Additional Event Creators** field is left blank, all events created in BlueJeans will be available for searching in the Author App.

The Author, in the Author app, then selects an event from the list of available events. In addition, the Author can add instructors to the event. These instructors in Learning Manager would become the presenters within BlueJeans events.

>[!NOTE]
>
>All users must belong to the same enterprise in BlueJeans Events App.

>[!NOTE]
>
>We've added a caching mechanism that improves the overall user experience. It is applicable when you select additional event creators. In this mode, the events are fetched the first time when an author searches for an event. The cache persists for 30 mins so that authors know how long they must wait to fetch the new events.-->

## Conector do Microsoft Teams {#microsoft-teams-connector}

O Microsoft® Teams® é uma plataforma de colaboração baseada em bate-papo persistente que oferece compatibilidade com o compartilhamento de documentos, reuniões on-line e outros recursos para comunicações de negócios.

O Adobe Learning Manager usa um conector de sala de aula virtual que pode ser usado para integrar as reuniões do Microsoft Teams ao Learning Manager.

O conector do Microsoft Teams conecta os sistemas Learning Manager e Microsoft Teams para permitir a sincronização automática de dados. A lista a seguir descreve os recursos do conector do Microsoft Teams:

**Configurar sessões virtuais usando Microsoft Teams**

Este conector ajuda a integrar sua conta do Adobe Learning Manager com sua conta do Microsoft Teams. Uma vez integrado, o conector permite que um autor no Learning Manager use o Microsoft Teams como o provedor de serviços de tecnologia para os módulos de Sala de aula virtual criados no Learning Manager.

**Permitir que os Microsoft Teams autentiquem os alunos ao entrarem na sala de aula virtual**

Um organizador de reuniões pode permitir que a sala de espera restrinja a entrada na reunião, bem como controlar as outras opções de reunião, conforme fornecidas pelo Microsoft Teams.

**Usar a sincronização automática de conclusão do usuário**

O processo de sincronização automática de conclusão do usuário permite que um administrador do Learning Manager busque automaticamente os registros de conclusão e URL de gravação para reuniões do Teams.

Para mais informações, consulte [**Instalar o conector Microsoft Teams no Adobe Learning Manager**](install-microsoft-teams-connector.md).

## Conector de acesso a dados de treinamento {#training-data-access}

>[!IMPORTANT]
>
>Essa funcionalidade específica estará disponível somente se o Adobe Learning Manager for vendido como um complemento do Adobe Experience Manager. Os dados do curso ficariam obsoletos em 24 horas.

>[!NOTE]
>
>A seção destaca como a infraestrutura funciona, mas para criar uma experiência sem periféricos ou baseada em AEM não conectada, entre em contato conosco. Sugerimos a abordagem correta com base no seu caso de uso. No momento, essa funcionalidade não está disponível como autoatendimento.

O conector de **[!UICONTROL Acesso a Dados de Treinamento]** permite criar uma experiência sem periféricos. Essa experiência pode ser independente ou uma interface de usuário personalizada com base no AEM Sites. Isso ajuda a recuperar e exibir informações de treinamento para os alunos e permite pesquisar e filtrar. Quando o conector de dados estiver ativado, um conjunto de APIs públicas estará disponível para criar a interface, onde as informações do curso/caminho de aprendizado serão exibidas para os alunos.

### Configurar o conector {#configure-training-data-connector}

Use o conector **[!UICONTROL Acesso a Dados de Treinamento]** para integrar sua conta da Adobe Learning Manager com sistemas de armazenamento e pesquisa de dados. Isso ajuda a interface baseada no AEM Sites a obter dados de treinamento, exibir páginas da Web e oferecer melhores opções de pesquisa para os alunos.

Exporte metadados de treinamento do Adobe Learning Manager para os serviços de recuperação de dados e ativação de pesquisa usando as APIs. Você também pode criar um cronograma para automatizar essas exportações.

Para configurar o conector de acesso a dados de treinamento, siga estas etapas:

1. No aplicativo do Administrador de Integração, selecione **[!UICONTROL Acesso a Dados de Treinamento]** > **[!UICONTROL Introdução]**.
1. Selecione **[!UICONTROL Avançar]** na página **[!UICONTROL Introdução]**.
1. Digite o nome da conexão e os domínios com lista de permissões.

   ![](assets/connection-name-and-domain-name.png)
Digite o nome da conexão e o nome do domínio

1. Selecione o **[!UICONTROL Tipo de interface]** nas seguintes opções:

   * **[!UICONTROL Learning Manager nativo]**: esta é a oferta padrão, disponível somente para interface nativa.
   * **[!UICONTROL interfaces sem periféricos]**: esta é a oferta premium que expõe APIs para criar uma experiência não conectada.

   ![](assets/types-of-interface.png)
Tipos de interface

1. Selecione **[!UICONTROL Conectar]**. O URL base e o URL CDN serão gerados automaticamente.
Você pode usar esses URLs para recuperar os dados usando APIs.

   >[!NOTE]
   >
   >Os clientes que usam a oferta premium receberão um URL diferente daquele que usa a oferta padrão.


1. Selecione **[!UICONTROL Exportar metadados de treinamento]** na página do conector.
1. Selecione **[!UICONTROL Habilitar exportação de metadados de treinamento]** usando esta conexão para exportar os dados de treinamento.
1. Depois de ativar a conexão, as imagens de todos os cursos, caminhos de aprendizado e certificados são migradas para a CDN.
1. Exporte os metadados dos cursos, programações de estudo e certificados para o serviço de pesquisa e recuperação.
1. Você pode agendar a exportação de metadados selecionando a opção Ativar agendamento. A programação ocorrerá automaticamente a cada 3 horas para o plano premium.
1. Para obter um relatório por demanda, vá para **[!UICONTROL Por demanda]**, selecione a **[!UICONTROL Data de início]** e **[!UICONTROL clique]** em Executar.
Você pode verificar o status da execução do relatório na página **[!UICONTROL Status de Execução]**.

### Criar site no AEM {#create-website-in-aem}

**Pré-requisito:** instale o pacote AEM do [**Repositório GitHub**](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0).

1. Use os URLs de base e de recuperação, a ID do cliente, o Segredo do cliente e o Token de atualização do administrador e crie uma configuração no AEM.
1. Crie o site usando os componentes do AEM.
1. Publique o site.

Para obter mais informações, consulte este [**documento**](../../adobe-learning-manager-integration-aem.md).

### Alunos {#learners}

O site publicado exibe uma lista de todos os cursos, certificados e planos de aprendizado migrados que são recuperados do serviço de pesquisa para alunos não conectados.

Quando um aluno clica em Curso, Certificado ou Caminho de Aprendizado, a página Visão geral é aberta. Na página, quando o aluno se inscreve, ele deve fazer logon primeiro e, em seguida, fazer o curso.

### Experiência não conectada {#non-logged-in-experience}

A experiência não conectada permite criar uma experiência em tempo real para usuários não conectados. Por exemplo, uma experiência não conectada serve como uma página de aterrissagem para campanhas de marketing para incentivar inscrições.

A experiência não conectada no Adobe Learning Manager pode ser configurada usando o conector **[!UICONTROL Acesso a dados de treinamento]**. O conector fornece as seguintes ofertas:

* Oferta padrão
* Oferta premium

**Oferta padrão**

A oferta padrão é criar a versão nativa do Adobe Learning Manager. Os usuários podem criar uma experiência sem periféricos apenas para demonstração e não conectada. A experiência de demonstração sem periféricos é indimensionável e não deve ser usada em um ambiente de produção.

**Oferta premium**

A oferta premium ajuda os usuários a criar uma interface sem periféricos, que é configurada pelo conector **[!UICONTROL Acesso a Dados de Treinamento]**. Isso permite que os usuários obtenham dados em tempo real sobre o curso e os detalhes do caminho de aprendizado, como nome, descrição, autor, habilidades, duração etc. Para cenários de aprendizagem combinada, você também obtém limites de vagas em tempo real, vagas ocupadas, limites de listas de espera e contagens de listas de espera. Os clientes podem usar essas APIs para criar recursos de pesquisa e filtro e um resumo completo do curso para alunos não conectados.

Os clientes podem adquirir um plano premium para criar essa experiência não conectada altamente dimensionável.

>[!NOTE]
>
>Entre em contato com a equipe de suporte ou o CSM para adquirir o plano premium.

Depois que um usuário comprar um plano, a equipe de CSM ativará o plano premium para ele. Com o conector Acesso a dados de treinamento, os usuários podem configurar uma experiência não conectada com os recursos mencionados anteriormente.

## Conector do Adobe Commerce {#adobe-commerce-connector}

>[!NOTE]
>
>Essa funcionalidade específica estará disponível somente se o Adobe Learning Manager for vendido como um complemento do Adobe Experience Manager.

>[!NOTE]
>
>Esse conector também pode ser ativado para contas de avaliação.

O Adobe Learning Manager agora oferece integração com o Adobe Commerce, uma plataforma para criar experiências de comércio eletrônico para clientes B2B e B2C.

O Adobe Commerce é uma solução de habilitação de comércio extensível e dimensionável que permite criar experiências de comércio multicanal para clientes B2B e B2C em uma só plataforma. Use o conector do Adobe Commerce para conectar sua conta do Adobe Learning Manager ao Adobe Commerce e aproveitar os recursos de comércio eletrônico na plataforma de aprendizado.

Habilite esse conector e utilize os recursos do Adobe Commerce para fornecer as ofertas de aprendizado como treinamento pago. Observe que você precisa comprar o Adobe Commerce separadamente para poder integrá-lo ao Adobe Learning Manager usando esse conector.

O conector se integra ao Adobe Commerce enviando dados de treinamento para plataforma de comércio, o que permite que os alunos façam um pagamento e comprem um treinamento.

Além de iniciar uma compra, o conector também coleta os detalhes da compra da Adobe Commerce, que é usada pelo Adobe Learning Manager para validar a compra e desbloquear o acesso ao treinamento.

**Pré-requisitos**

1. Habilitar [RabbitMq](https://devdocs.magento.com/cloud/project/services-rabbit.html) ou qualquer outro agente de mensagens.
1. Habilitar [CRON](https://devdocs.magento.com/cloud/env/variables-deploy.html#cron_consumer_runner).
1. Para as etapas 1 e 2, edite os seguintes arquivos:

   1. .magento.app.yaml
   1. .magento/services.yaml
   1. .magento.env.yaml

1. Substitua o limite de opções por meio do módulo personalizado. Esta é uma etapa opcional, mas altamente recomendada para grandes conjuntos de dados.
1. Habilite todas as APIs assíncronas na página. Como pode haver muitos dados, a exportação ocorre de forma assíncrona. As APIs do Adobe Commerce são chamadas de carga útil de solicitação enviada. A solicitação envia as mensagens para uma fila e há um consumidor nessa fila, que processa essas mensagens e cria produtos no lado do comércio. O Adobe Commerce não fornece esse processamento assíncrono por padrão. É por isso que você deve ativar essa opção.
1. Adicione um link para retornar ao ALM na página de sucesso do pagamento. Esse URL de retorno deve ser configurado no Adobe Commerce. A URL a ser usada para o link. - `https://learningmanager.adobe.com/app/learner#/postPayment`
1. Altere a indexação de “Ao salvar” para “Agendado”.  Para obter mais informações, consulte estes [KB](https://support.magento.com/hc/en-us/articles/360040227191).
1. Aplique os seguintes patches. Para obter mais informações, consulte [Aplicar patches](https://devdocs.magento.com/cloud/project/project-patch.html).
1. Configure o Fastly.  O Fastly é necessário para o Adobe Commerce na infraestrutura de nuvem e é usado em ambientes de preparo e produção. Para mais informações, consulte [Configurar o Fastly](https://devdocs.magento.com/cloud/cdn/configure-fastly.html).

### Configurar o conector {#configure-connector}

Como administrador de integração, no conector do Adobe Commerce, clique em **[!UICONTROL Conectar]**.

Na página de configuração, insira os seguintes detalhes. Esses detalhes, as chaves de autorização, estão disponíveis no Adobe Commerce. Depois de criar uma integração no Adobe Commerce, as credenciais estarão disponíveis lá.

![](assets/adobe-commerce-configuration.png)
*Configurar o conector do Adobe Commerce*

Depois que a conexão do conector do Adobe Commerce é habilitada, um autor pode definir o preço de um curso, caminho de aprendizado ou certificado.

Depois que o curso, o caminho de aprendizado ou o certificado são publicados, um aluno pode comprar cursos no aplicativo do aluno.

* **Learning Manager nativo:** o aluno pode comprar um curso, plano de aprendizado ou um certificado no Learning Manager. Isso só é aplicável quando o autor adicionou um preço.
* **Personalizado usando sites do AEM:** o aluno pode comprar um curso de um site do AEM.

### Fluxo de trabalho (WRK) {#workflow}

O administrador do Adobe Commerce configura o Learning Manager como uma integração.

O autor marca os cursos, os caminhos de aprendizado ou os certificados como premium e atribui preços. Essa opção só aparece se o comércio eletrônico estiver habilitado para a conta. Para mais informações, consulte [Criar cursos](../../authors/feature-summary/courses.md).

O curso ou o plano de aprendizado não estarão disponíveis para compra até que os dados sejam sincronizados no Adobe Commerce.

### Exportar cursos para o Adobe Commerce {#export-commerce}

Depois que um autor tiver definido os preços em vários cursos, caminhos de aprendizado ou certificações, você, como administrador de integração, exportará os cursos, caminhos de aprendizado ou certificações para o Adobe Commerce.

>[!NOTE]
>
>Na versão de março de 2024 do Adobe Learning Manager, introduzimos suporte para o [Adobe Commerce 2.4.6](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-6.html?lang=pt-BR).


1. Clique em **[!UICONTROL Exportar metadados de treinamento]** > **[!UICONTROL Sob demanda]**.

1. Selecione as datas.

1. Clique em **[!UICONTROL Executar]**. Após a execução bem-sucedida, todos os cursos ou caminhos de aprendizado com preços definidos serão movidos para o Adobe Commerce. O aluno pode comprar o curso do Learning Manager.

### Learning Manager nativo com Adobe Commerce {#learning-manager-with-commerce}

#### Aluno {#learner}

Como aluno, você deve estar conectado para comprar um curso, certificado ou caminho de aprendizado.

Para comprar o curso, clique em Comprar agora. Você é redirecionado para o Adobe Commerce para concluir a compra. Depois que o pagamento é bem-sucedido, você pode ver uma mensagem solicitando que você retorne ao Learning Manager e inicie o curso. Você também deve fazer logon no Adobe Commerce separadamente para concluir a compra.

Ao adquirir um curso, certificado ou plano de aprendizado do ALM nativo ou do AEM, você recebe e-mails do ALM e do Adobe Commerce.

Além disso, você também pode ativar/desativar e-mails do Adobe Commerce.

### Sites AEM com Adobe Commerce {#aem-sites-with-adobe-commerce}

Quando a opção Personalizado usando sites do AEM está habilitada, você, como aluno, pode comprar cursos de um site do AEM personalizado.

O site do AEM terá todos os metadados do Learning Manager para permitir a pesquisa pelo Adobe Commerce. Os cursos são obtidos no Adobe Commerce em casos não conectados.

A experiência conectada e não conectada é possível. Usuários não conectados podem pesquisar e navegar no catálogo do curso, no plano de aprendizado e nos certificados. No entanto, se quiser comprar um curso, você deve fazer logon no site do AEM.

Como no Learning Manager nativo, após fazer logon, você pode adicionar um curso ao carrinho e, em seguida, visualizar ou comprar esse curso.

### Configurar o conector do Adobe Commerce {#setup-commerce-connector}

#### Pré-requisito {#pre-requisites}

O administrador ativa a caixa de seleção **Habilitar preços para treinamentos** em **Configurações > Geral** no aplicativo do administrador. Se a opção estiver ativada, os autores poderão especificar preços para treinamentos. Quando você adiciona uma conexão do Adobe Commerce, essa caixa de seleção é automaticamente selecionada e aplicada.

O Adobe Learning Manager oferece compatibilidade com o comércio eletrônico para comprar e vender treinamento. Aqui, os usuários podem vender treinamento para promover as vendas agregadas e cruzadas de seus produtos.

Com a integração do Adobe Commerce, o Adobe Learning Manager oferece compatibilidade com a compra e venda de treinamento para fornecer uma experiência do cliente mais completa em cenários de Treinamento de parceiros do cliente.

Os principais objetivos desta integração são os seguintes:

* Os usuários podem gerar receita vendendo cursos no Adobe Learning Manager ou em uma interface de aprendizado sem periféricos.
* Permita a integração do Adobe Commerce à plataforma para vender cursos usando o aplicativo nativo do Learning Manager e o AEM.
* Permita que os clientes do Learning Manager ofereçam aprendizado formal na forma de cursos pagos.
* Permita que os alunos visualizem cursos antes de decidir comprar o treinamento.

#### Nativo do Adobe Learning Manager {#native-learning-manager}

**Administrador de Integração**

1. Na página Administrador de integração, adicione o conector do Adobe Commerce. Obtenha as autenticações do aplicativo criado no Adobe Commerce.
1. Depois que o Adobe Commerce é habilitado, o comércio eletrônico é habilitado no Adobe Learning Manager. Os dados do Learning Manager ao Adobe Commerce são sincronizados de acordo com um agendamento. Os dados incluem todo o treinamento (pago) junto com os metadados (usuários, habilidades, nome do autor, preço etc.).

>[!NOTE]
>
>O Adobe Learning Manager e o Adobe Commerce têm logons diferentes.

### AEM {#aem}

Nesse modo, um aluno faz o curso de um site baseado no AEM, que é criado usando modelos e componentes baseados no AEM.

No site AEM, o aluno tem suporte para carrinho de compras, botão adicionar ao carrinho, excluir cursos do carrinho de compras e assim por diante.

Se o usuário não estiver conectado, ele ainda poderá procurar catálogos e ver detalhes do curso, mas não poderá comprar um curso. Como aluno, você deve estar conectado se quiser comprar um curso.

Depois que o aluno adquire o curso, ele é redirecionado para a página de visão geral do curso no estado inscrito, onde pode realizar o treinamento adquirido.

#### Sem periféricos - Não conectado {#headless-non-logged-in}

Um aluno pode:

* Procure qualquer treinamento na barra de pesquisa.
* Filtre qualquer treinamento por faixa de preços.

Um aluno não pode:

* Compre um curso na página Visão geral.
* Visualize o conteúdo pago.

#### Sem periféricos - Conectado {#headless-logged-in}

Um aluno pode:

* Explore, exiba, pesquise e filtre cursos de treinamento pagos ou gratuitos.

* Adicione um curso a um carrinho e, em seguida, faça o check-out para a compra.
* Adicione, atualize ou exclua cursos de treinamento no carrinho.
* Pague simultaneamente por vários cursos de treinamento.
* Visualize um curso pago no Player.
* Veja mensagens se houver um erro de pagamento.

* Veja a fatura como um anexo no e-mail após comprar o curso.

#### Sincronização sob demanda {#on-demand-sync}

A sincronização entre o Learning Manager e o Adobe Commerce acontece duas vezes ao dia. Depois que o administrador habilita uma conta para comércio eletrônico, a opção **Habilitar exportação de metadados de treinamento usando esta conexão** quando habilitada, armazena as imagens do curso, do plano de aprendizado e dos certificados em uma CDN pública.

Se os dados permanecerem não sincronizados, as informações de preço não serão exibidas para um aluno.

No Learning Manager nativo, se o comércio eletrônico estiver ativado e a sincronização entre o Learning Manager e o Adobe Commerce estiver concluída, os alunos poderão visualizar ou pesquisar treinamento pago ou gratuito.

Para o AEM, não há Comprar Agora, apenas um botão **Adicionar ao Carrinho**. Esse botão também permanece desabilitado se a sincronização não for executada.

#### Perguntas frequentes {#faqs}

+++Quais cursos não podem ser adquiridos?

Os cursos, como certificações recorrentes, treinamento no marketplace de conteúdo, treinamento adquirido, treinamento de conectores, ajudas de tarefa e cursos aprovados/indicados pelo gerente não podem ser adquiridos por um aluno.
+++

+++Há alguma alteração na transcrição do aluno e no relatório de treinamentos?

Esses relatórios exibem o preço e a data de compra de todos os treinamentos comprados na conta.
+++

+++Um aluno pode se inscrever em um treinamento gratuito?

Sim, um aluno pode se inscrever em treinamento gratuito. O treinamento gratuito exibe o botão Visualizar e Inscrever-se na página Visão geral do treinamento.
+++
