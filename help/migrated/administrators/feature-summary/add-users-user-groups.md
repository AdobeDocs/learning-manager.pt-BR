---
description: Saiba como adicionar usuários ou grupos de usuários no aplicativo Learning Manager.
jcr-language: en_us
title: Adicionar usuários e criar grupos de usuários
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3913'
ht-degree: 0%

---



# Adicionar usuários e criar grupos de usuários

Saiba como adicionar usuários ou grupos de usuários no aplicativo Learning Manager.

<!--![](assets/user-mgmt-new.png)-->

## Visão geral {#overview}

No Adobe Learning Manager, você pode assumir as seguintes funções:

* **Administrador:** Um administrador define a estratégia de treinamento para a organização. Um administrador pode adicionar alunos, pesquisar habilidades necessárias para os alunos, gerenciar e atribuir cursos, criar planos de aprendizado, certificações e programas de aprendizado e gerenciar relatórios para toda a organização.
* **Autor:** Os autores são designers instrucionais e criadores de conteúdo. Um autor pode adicionar módulos e cursos ao Learning Manager.
* **Gerente:** Um gerente gerencia as atividades de aprendizado de uma equipe. Um gerente pode indicar os membros da equipe para realizar um curso, aprovar solicitações dos membros da equipe e fornecer feedback sobre o desempenho dos membros da equipe após a conclusão do treinamento. Os gerentes também podem exibir relatórios para que sua equipe acompanhe seu desempenho.
* **Aluno:** Os alunos podem acessar cursos, programas de aprendizado e certificações atribuídas a eles. Os alunos também podem navegar por todos os cursos disponíveis usando um catálogo e se inscrevendo em cursos, programas de aprendizado ou certificações.

Como administrador, você pode adicionar usuários de três maneiras:

* Interno
* Externo
* Grupos de usuários

## Adicionar um único usuário {#addasingleuser}

Para adicionar usuários,

1. Faça logon no Adobe Learning Manager como administrador.
1. Na página inicial, clique em **[!UICONTROL Adicionar usuários]**. Nesta página, você pode adicionar um único usuário ou vários usuários por vez usando um CSV. Você também pode criar um link de autorregistro para funcionários internos ou criar um perfil de aluno externo.
1. Para adicionar um único usuário, clique em **[!UICONTROL Adicionar]** no canto superior direito e escolha a opção **[!UICONTROL Usuário único]**.

   ![](assets/single-user.png)
   *Adicionar um único usuário interno*

1. Na guia **[!UICONTROL Adicionar usuário]** , insira os detalhes do aluno. Para o campo **[!UICONTROL Nome do gerente]**, escolha o nome de um usuário existente no sistema.

   ![](assets/manager.png)
   *Caixa de diálogo Adicionar usuário*

1. Para adicionar o novo usuário no Learning Manager, clique em **[!UICONTROL Adicionar]**. Depois que o usuário é adicionado, ele recebe um e-mail de verificação. O aluno ativa a conta e começa a usar o Learning Manager. Este fluxo de trabalho é útil se você precisar adicionar um número limitado de alunos à sua conta do Learning Manager. Mas se você planeja inscrever todos os funcionários de uma grande organização, pode adicioná-los em uma única tentativa. Para obter mais informações, consulte a próxima seção.

## Adicionar usuários em massa {#addusersinbulk}

Normalmente, a maioria das organizações trabalha com um Sistema de Gerenciamento de RH (HRMS), que mantém todos os registros de funcionários, como designação, local, data de junção ou hierarquia de funcionários. Você pode exportar esses dados em um formato CSV. Para importar um CSV, siga as etapas abaixo:

1. Clique em **[!UICONTROL Adicionar]** no canto superior direito e escolha a opção **[!UICONTROL Fazer upload de um CSV]**.

   ![](assets/upload-a-csv.png)
   *Carregar um CSV para adicionar usuários em massa*

1. O CSV que você carregou consiste nos campos, conforme mostrado abaixo:

   ![](assets/csv.png)
   *Estrutura do CSV*

   Você deve manter um CSV mestre e executar todas as adições e exclusões no CSV mestre. O CSV mestre contém os seguintes campos:

   * nome &#42;
   * email &#42;
   * perfil
   * gerente

   (&#42;) Campo obrigatório.

1. Depois de clicar na opção **[!UICONTROL Fazer upload de um CSV]**, a caixa de diálogo a seguir é exibida.

   ![](assets/upload-a-csv-dialog.png)
   *Fazer upload de uma caixa de diálogo CSV*

1. Escolha o CSV ou arraste e solte o arquivo. Depois de escolher o arquivo, mapeie os campos de dados com os do arquivo CSV. Clique na lista suspensa desejada e escolha o campo certo.

   ![](assets/map-data-fields.png)
   *Mapear campos no CSV*

1. Para iniciar a importação dos usuários, clique em **[!UICONTROL Salvar]**. Você verá uma mensagem de confirmação.

   ![](assets/save-csv.png)
   *Mensagem de confirmação para upload bem-sucedido do CSV*

1. Os novos usuários foram adicionados à sua conta do Adobe Learning Manager. Para selecionar os novos usuários, marque a caixa de seleção ao lado dos nomes para que todos sejam selecionados.

   ![](assets/select-new-users.png)
   *Novos usuários adicionados*

>[!NOTE]
>
>Para obter mais informações, consulte as perguntas frequentes, [Adicionar usuários em massa](../add-users-in-bulk.md).

Depois de selecionar os usuários, você pode fazer o seguinte:

## Registrar um usuário {#registerauser}

Com o usuário selecionado, clique em **[!UICONTROL Ações]** no canto superior direito e clique em **[!UICONTROL Registrar]**.

Os usuários selecionados recebem um email de Boas-vindas. Se os alunos tiverem uma Adobe ID existente, eles poderão clicar neste link. Se eles não tiverem uma Adobe ID existente, poderão clicar no link Bem-vindo para criar uma Adobe ID e vinculá-la à sua conta do Learning Manager.

## Atribuir uma função {#assignarole}

Depois de adicionar alunos à conta do Adobe Learning Manager, se você quiser alterar suas funções, clique em Ações no canto superior direito da página. Escolha a opção **[!UICONTROL Atribuir Função]**. Aqui, você pode decidir se deseja conceder acesso de autor ou acesso de administrador ao aluno. Depois de atribuir uma função, esse aluno tem acesso de autor à conta e pode adicionar módulos e criar cursos.

![](assets/assign-a-role.png)
*Atribuir funções a usuários*

## Remover uma função {#removearole}

Você também pode remover o acesso de autor ou administrador para os usuários. Selecione um ou mais alunos, clique em **[!UICONTROL Ações]** e selecione **[!UICONTROL Remover Função]**. Escolha uma opção, por exemplo, **[!UICONTROL Remover autor]** e o acesso de autor é revogado para este aluno.

>[!NOTE]
>
>Você não pode atribuir manualmente uma função de gerente a alguém no sistema. Eles obtêm acesso automático ao painel Gerente quando um ou mais funcionários são adicionados a eles.

## Excluir um usuário {#deleteauser}

Para excluir um usuário, clique em **[!UICONTROL Ações]** e escolha **[!UICONTROL Excluir usuário]**. Na caixa de diálogo de confirmação, clique em **[!UICONTROL Sim]** e o aluno é excluído.

![](assets/delete-a-role.png)
*Mensagem de confirmação para excluir um usuário*

## Editar um usuário {#editauser}

Na lista de usuários, escolha um usuário e clique nele. Nos detalhes do usuário, clique no botão **[!UICONTROL Editar]** ( ![](assets/edit-pen.png)). Na guia **[!UICONTROL Editar usuário]** faça as edições necessárias e, para salvar as alterações, clique em **[!UICONTROL Salvar]**.

![](assets/edit-user.png)
*Caixa de diálogo Editar usuário*

## Fluxos de trabalho para campos ativos e valores de campo ativos preservando a diferenciação de maiúsculas e minúsculas

Nesta versão, o Learning Manager preserva a diferenciação de maiúsculas e minúsculas do atributo do usuário e seu valor. **Por exemplo:**, a diferenciação de maiúsculas e minúsculas de um atributo de usuário é &#39;location&#39; e seu valor como &#39;PARIS&#39; será preservado e exibido da mesma maneira. Em caso de problemas, o administrador agora pode editar o nome e os valores do atributo para corrigir quaisquer erros de diferenciação de maiúsculas e minúsculas.

O administrador pode fazer isso acessando **[!UICONTROL Aplicativo do administrador]** > **[!UICONTROL Usuários]** > **[!UICONTROL Grupos de usuários]** e clicando no nome do grupo.

O administrador pode adicionar e atualizar valores de atributo permitidos para um aluno por meio da interface do usuário.

Tipos de campos ativos:

* Agrupável: os alunos seriam agrupados com base nos valores
* Reportável: os grupos de usuários de relatórios seriam criados com base nos campos ativos
* Exportável: os campos serão exibidos no relatório de grupo de usuários exportado.

## Criar um link de autorregistro {#createaselfregistrationlink}

Você também pode permitir que os funcionários da sua organização se registrem como Alunos na conta do Adobe Learning Manager sem a necessidade de um administrador. O administrador pode criar um link de autorregistro e compartilhar com os funcionários, que podem se registrar no Learning Manager usando suas credenciais de Adobe.

No canto superior direito da página, clique em **[!UICONTROL Adicionar]** e escolha **[!UICONTROL Autorregistro]**.

![](assets/self-registration.png)
*Criar um link para se registrar como aluno*

O **[!UICONTROL Adicionar Perfil de Autorregistro]** é exibida. Dê um nome a este perfil. Em seguida, adicione o nome do gerente. É importante saber que o gerente já deve estar registrado como aluno no Learning Manager.

![](assets/add-self-registrationprofile.png)
*Adicionar perfil para autorregistro*

Depois de clicar em **[!UICONTROL Salvar]**, um URL é gerado e você pode compartilhar com os alunos para que eles possam clicar no URL e se registrarem por conta própria.

## Inscrever alunos externos {#enrollexternallearners}

No Adobe Learning Manager, também é possível criar links de Registro para parceiros externos ou agências externos com acesso limitado à sua conta para fornecer-lhes material de aprendizagem.

Há algumas diferenças entre registros internos e externos.

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Usuários internos</b></p></td>
   <td>
    <p><b>Usuários externos</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Faça logon usando as credenciais do Adobe ID ou SSO.</p></td>
   <td>
    <p>Faça logon usando qualquer ID de e-mail.</p></td>
  </tr>
  <tr>
   <td>
    <p>Gamificação disponível.</p></td>
   <td>
    <p>A gamificação não está disponível.</p></td>
  </tr>
  <tr>
   <td>
    <p>As hierarquias do aluno estão disponíveis.</p></td>
   <td>
    <p>As hierarquias do aluno não estão disponíveis.</p></td>
  </tr>
 </tbody>
</table>

Para inscrever usuários externos, siga as etapas abaixo:

1. No painel de navegação esquerdo, clique em **[!UICONTROL Externo]**.

   ![](assets/click-external.png)

   *Inscrever usuários externos*

1. No canto superior direito da página, clique em **[!UICONTROL Adicionar]**.
1. Na guia **[!UICONTROL Adicionar Perfil de Registro Externo]** adicione os seguintes detalhes:

   * O nome do perfil da organização parceira.
   * O endereço de email do gerente da organização parceira.
   * Limite de vagas para inscrição externa para este parceiro.
   * Data de vencimento para definir um prazo para interromper a permissão de novos registros para este grupo. Após a data de expiração, somente os usuários registrados existentes podem acessar este treinamento.

   ![](assets/map-data-fields-2.png)

   *Caixa de diálogo Adicionar Perfil de Registro Externo*

   * No menu **[!UICONTROL Configurações avançadas]** insira o seguinte:

      * **[!UICONTROL Requisito de logon]:** Especifique um valor em dias. Os alunos são excluídos se não fizerem logon pela duração acima.
      * **[!UICONTROL Domínios permitidos]:** Uma lista separada por vírgulas de nomes de domínio de email na lista de exceções.
      * **[!UICONTROL Verificação de Email Necessária]:** Selecione essa opção para tornar a verificação de e-mail obrigatória para um aluno.

   ![](assets/email-verificationrequired.png)

   *Insira os detalhes na seção Configurações avançadas*

1. Depois de clicar em **[!UICONTROL Salvar]**, você verá a seguinte mensagem de confirmação. Você deve compartilhar a URL com seu parceiro externo.

   ![](assets/save-and-share-urlwithexternalusers.png)

## Ativar um perfil externo {#enableanexternalprofile}

Depois que um perfil externo for criado, você deverá ativar seu status. Na lista de perfis externos, escolha o perfil necessário e ative o botão de status.

![](assets/choose-required-profiles.png)
*Ativar um perfil externo*

Isso ativa o link de inscrição externa. Um e-mail de boas-vindas é enviado automaticamente ao parceiro. Você também pode copiar o link e compartilhar com eles clicando no ícone Copiar URL (), ou pode reenviar o e-mail de boas-vindas à organização parceira clicando no ícone E-mail ().

O gerente do parceiro pode compartilhar o link com os funcionários que devem realizar o treinamento no PrLearning Manager. Ao clicar no link, eles podem se inscrever após preencher alguns detalhes para criar seu perfil no Learning Manager. Esses usuários não aparecerão na guia Alunos junto com os funcionários internos. Você pode ver os nomes deles sob **[!UICONTROL Alunos externos]** guia.

## Pausar um perfil externo {#pause}

Depois de adicionar um grupo de usuários externo ao Learning Manager, você também pode pausar o processo de registro de usuários externos. Quando você pausa, o processo de registro de usuários externos é bloqueado. No entanto, esse processo funciona apenas quando os usuários ainda não se registraram aceitando o convite.

Para pausar os grupos de usuários externos, escolha um grupo ou grupos, clique em **[!UICONTROL Ações]** no canto superior direito da página e clique em **[!UICONTROL Pausar]**.

## Retomar um perfil externo {#resumeanexternalprofile}

A qualquer momento, você sempre pode revogar o estado de pausa de um parceiro externo e retomar os serviços normais. Clique em **[!UICONTROL Ações]** no canto superior direito da página e escolha **[!UICONTROL Retomar]**.

Os seguintes estados são aplicáveis a usuários externos:

* **Estado inativo** - Neste estado, o registro de usuários externos expirou. Os administradores definem a data de expiração para os usuários externos ao adicioná-los por meio do fluxo de trabalho de adição de usuário.
* **Estado ativo** - Nesse estado, os usuários externos podem se registrar no aplicativo Learning Manager e fazer logon no aplicativo.
* **Pausar** - Neste estado, o processo de registro para usuários externos está bloqueado. No entanto, os usuários existentes podem continuar a fazer logon.

## Verificar assentos usados {#checkusedseats}

Na lista de perfis externos, clique em **[!UICONTROL Vagas usadas]**. Você pode ver o número de alunos na organização parceira que foram adicionados.

![](assets/seats-used.png)
*Verificar assentos usados*

## Excluir um usuário {#Deleteauser-1}

Escolha um usuário e, no canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Excluir usuário]**.

## Alterar perfil {#changeprofile}

Para mover um usuário para outro perfil externo, escolha um usuário no canto superior direito e clique em **[!UICONTROL Ações]** > **[!UICONTROL Alterar perfil]**. Na lista de perfis, escolha um perfil e clique em **[!UICONTROL Alterar]**.

## Atribuir uma função {#Assignarole-1}

Escolha um usuário e, no canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Atribuir Função]** > **Marca`<role>`**. O usuário recebe uma nova função.

## Remover uma função {#Removearole-1}

Escolha um usuário e, no canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Remover Função]** > **Remover`<role>`**. A função selecionada é removida da lista de funções que foram atribuídas ao usuário.

## Criar grupos de usuários {#createusergroups}

Um Grupo de usuários é um conjunto de usuários relacionados a uma categoria. Os grupos de usuários ajudam os administradores a selecionar alunos em sua organização com base em seus atributos e, em seguida, atribuem conteúdo de aprendizado a eles. Além disso, esses grupos de usuários permitem que os administradores atribuam logotipos e catálogos personalizados aos alunos e mostrem relatórios personalizados sobre seu progresso.

Para acessar Grupos de usuários, no painel de navegação esquerdo, clique em **[!UICONTROL Grupos de usuários]**.

![](assets/user-groups.png)
*Criar grupos de usuários*

Há dois tipos de grupos no Adobe Learning Manager: Personalizados e Gerados automaticamente. Quando você adiciona alunos à sua conta, alguns grupos são criados automaticamente com base em suas propriedades comuns.

Para ver os grupos criados automaticamente, clique na guia **[!UICONTROL Gerado automaticamente]**.

![](assets/auto-generated.png)
*Exibir grupos gerados automaticamente*

Você pode ver que há diferentes grupos, como Todos os usuários internos, Todos os gerentes, grupos com base no centro de custos, com base no departamento e nas equipes dos gerentes.

Além dos grupos Gerados automaticamente, você pode criar grupos Personalizados. Para adicionar um novo Grupo personalizado, no canto superior direito, clique em **[!UICONTROL Adicionar]**.

1. Insira o nome e a descrição do grupo.
1. Insira o nome de usuário ou perfil no campo de pesquisa e selecione-o na lista suspensa para adicionar usuários.
1. Para adicionar mais alunos, clique em **[!UICONTROL Adicionar Mais Usuários].**
1. Para criar o grupo de usuários, clique em **[!UICONTROL Salvar]**.

Este grupo personalizado foi criado e adicionado ao perfil. Os Grupos de usuários que você cria são dinâmicos por natureza. Se novos usuários forem adicionados com atributos semelhantes, eles serão adicionados automaticamente ao Grupo de usuários.

## Exclusão de grupos de usuários

Às vezes, você deseja excluir um pequeno conjunto de usuários de um grande grupo de usuários. Isso é necessário para inscrever esse conjunto específico de usuários no treinamento por meio de Planos de aprendizado ou para configurar a visibilidade correta dos catálogos. Nesta versão do Learning Manager, você pode excluir alunos ou grupos de usuários ao criar um grupo de usuários personalizado. Na caixa de diálogo Adicionar grupo de usuários, a seção Excluir alunos permite isso.

![](assets/exclude-user-groups.png)
*Excluir grupos de usuários*

Por exemplo: se você deseja configurar um Plano de aprendizado para que todos os usuários que pertencem à localização = Califórnia, exceto Loja-5 (localizada na Califórnia) sejam inscritos.

## Configurações avançadas {#advancedsettings}

## Fontes de dados {#datasources}

Você pode usar esse recurso quando quiser importar/sincronizar os usuários ou os dados de aprendizado do banco de dados da sua organização no aplicativo Learning Manager. Você também pode configurar a frequência dessa sincronização.

Clique em **[!UICONTROL Fontes de dados]** no painel esquerdo, em **[!UICONTROL Avançado]** seção.

![](assets/data-sources-add-users.png)

*Fontes de dados para importar ou sincronizar usuários*

Escolha o tipo de origem de dados na **[!UICONTROL Origem]** , selecione a frequência de atualização e clique em **[!UICONTROL Sincronizar agora]** se precisar sincronizar imediatamente ou clique em **[!UICONTROL Salvar].** Os tipos de origem de dados são SFDC, FTP e assim por diante para usuários internos.

É possível adicionar várias origens de dados.

## Campos ativos {#activefields}

Esse recurso permite que os administradores adicionem mais campos ativos além do que foi fornecido durante o registro do usuário.

Clique em **Campos ativos** disponível na página usuários. Os alunos só podem escolher entre os valores fornecidos em valores personalizados.

![](assets/active-fields.png)
*Campos ativos*

### Configurar campos {#configurefields}

**Usuários internos**

É possível adicionar um valor personalizado para campos de usuário para usuários internos.

Para adicionar valores personalizados, siga estas etapas:

1. Clique em  **[!UICONTROL Modificar Valores]** para um usuário interno.

   ![](assets/modify-values.png)
   *Modificar valores para usuários internos*

1. O **Valores no campo Personalizado** é exibida.

   ![](assets/values-in-customfields.png)
   *Caixa de diálogo Valores em campos personalizados*

1. Selecione o valor a ser adicionado na **[!UICONTROL Selecionar campo]** menu suspenso.
1. Insira novos valores no campo **[!UICONTROL Novo valor]** campo.
1. Clique em **[!UICONTROL Concluído]**.
1. Clique em Salvar no canto superior direito para **[!UICONTROL Salvar]** alterações.

**Usuários externos**

Adicione valores personalizados semelhantes aos dos usuários internos.

![](assets/modify-values-forexternalusers.png)
*Modificar valores para usuários externos*

### Configurações {#settings}

**Exibição do usuário**

Se a opção **Mostrar apenas campos não preenchidos no logon do aluno** estiver ativado, um usuário verá apenas os campos em branco ao fazer logon.

![](assets/settings-tab.png)
*Mostrar campos não preenchidos*

Usando essa opção, um administrador pode decidir se deseja mostrar os campos ou ocultá-los depois de preenchidos.

## Restringir campos ativos nos relatórios {#restrictactivefields}

O Learning Manager 27.7 apresenta duas novas opções: **[!UICONTROL Reportável]** e **[!UICONTROL Exportável]**, para Campos ativos.

![](assets/options-in-activefields.png)
*Opções em campos ativos*

Para campos CSV e campos adicionados manualmente, se um campo ativo estiver marcado como **[!UICONTROL Reportável]**, o Campo ativo se torna pesquisável em um filtro dentro de um relatório do painel.

![](assets/filters-in-a-dashboardreport.png)
*Filtros em um relatório do painel*

Se um campo ativo estiver marcado como **[!UICONTROL Exportável]**, o Campo Ativo aparecerá no arquivo do Excel ao baixar qualquer relatório do Excel.

Essas opções são exibidas para os Campos ativos internos e externos.

Você só pode excluir um Campo Ativo personalizado.

## Exibição do usuário

Você pode ocultar a página inteira “Concluir seu perfil” dos alunos. A página não aparecerá quando o aluno fizer logon.

Observe que o comportamento padrão existente não é alterado. Esse é um recurso opcional agora disponível para administradores.

Ative as opções abaixo:

![](assets/user-display.png)
*Seção Exibição do usuário*

## Suporte para campos CSV manuais por conectores FTP e Box {#import-connector}

Geralmente, os usuários querem que os campos Ativos sejam fornecidos manualmente quando um aluno faz logon no Learning Manager. Isso é possível no Learning Manager no momento, quando o usuário importa um CSV manualmente.

O CSV não pode conter todos os campos Ativos. Para todos os campos ativos que não são atualizados no CSV carregado, o usuário precisa inserir os dados desses campos ativos.

Atualmente, todos os campos ativos devem ser mapeados para algum campo do CSV de origem.

Ocorre que, às vezes, um usuário não deseja mapear um campo Ativo para um campo especificado no CSV. Nesses casos, o usuário pode mapear o campo Ativo para o valor **[!UICONTROL DontImportFromSource]**. Selecione esse valor na lista suspensa ao importar usuários de conectores FTP e Box.

## Funções personalizadas {#customroles}

Adicione qualquer campo de sua escolha como parte das informações do usuário e clique em **[!UICONTROL Salvar]**. Depois de adicionar os campos, você também pode verificar a disponibilidade dos campos na **[!UICONTROL Editar usuários]** diálogo.

Depois de adicionar os campos, você pode notar que os campos marcados com marca de seleção são provenientes de fontes de dados ou CSV, conforme mencionado na captura de tela abaixo. O administrador pode editar esses campos de origem ativando ou desativando os campos.

**Valores para campos ativos no Learning Manager**

Os valores dos campos ativos são obtidos das seguintes maneiras:

1. O aplicativo Learning Manager importa metadados de fontes de dados associadas à sua conta.
1. Metadados capturados do arquivo CSV importado manualmente.
1. Os alunos preenchem os metadados ao fazer logon
1. O administrador insere dados para os usuários.

>[!NOTE]
>
>O aplicativo Learning Manager cria grupos de usuários automaticamente a partir desses metadados.

**Adicionar valor personalizado**

Você pode adicionar um valor personalizado para os campos de usuário nos campos de usuário interno e externo.

Para adicionar valores personalizados, siga estas etapas:

Os campos personalizados podem ser adicionados e excluídos, e são aplicáveis a todos os usuários. Os campos CSV podem ser ativados ou desativados, eles entram em vigor somente quando você faz upload do CSV após fazer modificações nos campos Ativos. Todos os campos ativos internos são aplicáveis a todos os tipos de usuários internos. Os campos externos são aplicáveis somente a usuários externos. Se um campo personalizado estiver presente no CSV, no próximo carregamento, ele será convertido em um campo CSV automaticamente e será habilitado.

## Valores para campos CSV {#valuesforcsvfields}

Os usuários só podem escolher entre campos predefinidos para campos CSV se a **[!UICONTROL Restringir seleção]** está ativada.

![](assets/value-field-for-csv.png)
*Caixa de seleção Restringir seleção*

## Importar Logs {#importlogs}

Neste espaço, você pode exibir o histórico de importação de CSV dos usuários que o administrador adicionou usando o recurso de importação em massa. Você também pode clicar em **Adicionar** no canto superior direito da página para adicionar usuários usando o recurso de upload de CSV.

## Campos ativos de valores múltiplos

Com esse recurso, você pode ter mais de um campo para um campo ativo. Em uma conta, pode haver no máximo três campos ativos de valores múltiplos. Os campos ativos de valores múltiplos estão disponíveis para usuários externos e internos.

Depois de marcar um campo ativo como valores múltiplos, você não poderá convertê-lo novamente em um único valor. Isso é irreversível.

Um campo de valor único existente não pode ser marcado como campo de valores múltiplos.

Para criar um campo ativo de valores múltiplos, siga as etapas abaixo:

1. Adicione um campo ativo.

   ![Adicionar um campo ativo](assets/add-active-field.png)
   *Adicionar um campo ativo*

1. Clique em Adicionar.
1. Na guia Configurações marque o novo campo como valores múltiplos.

   ![Marcar como valores múltiplos](assets/mark-multi-valued.png)
   *Marcar como valores múltiplos*

   Há outra caixa de seleção, **[!UICONTROL Configurável pelo aluno]**, que quando desativado, o aluno não poderá ver o campo na página Perfil.

1. Adicione os valores usando um CSV ou clicando em Modificar Valores.

   ![Adicionar valores](assets/add-values.png)
   *Adicionar valores*

1. Clique em [!UICONTROL **Concluído**].

>[!NOTE]
>
>Depois que o grupo de usuários é criado e o campo é preenchido, vários valores não podem ser convertidos em valores únicos e vice-versa.

### Adicionar campo ativo de valores múltiplos por CSV

Siga as etapas abaixo:

1. Crie um CSV com os novos campos ativos como colunas (valores separados por vírgula ou únicos).
1. Importe o CSV.
1. Marque os campos como valores múltiplos na caixa de diálogo Valores em campos personalizados.
1. Importe o CSV novamente.

O CSV deve ter uma coluna com o mesmo nome de um campo ativo marcado como valores múltiplos.

O CSV contém os campos:

* **[!UICONTROL Usuário]**: grupos de usuários criados como funções.
* **[!UICONTROL Funções]**: campo ativo de valores múltiplos com valores.

Se o CSV for recarregado com novos valores ou valores excluídos, os campos e grupos ativos também serão atualizados adequadamente.

### Relatórios

Todos os relatórios incluem os campos ativos de valores múltiplos e seus valores.

O administrador pode adicionar campos ativos gerados automaticamente e configurar relatórios de atividade e treinamento do usuário.

O relatório de transcrição do aluno contém todos os campos ativos e valores separados por vírgula. O administrador pode então filtrar os dados adequadamente.

## Perguntas frequentes {#faq}

+++Como registrar usuários no Learning Manager?

Depois de adicionar um usuário e atribuir uma função ao usuário, você pode registrar o usuário executando as etapas abaixo:

1. Com o usuário ou usuários selecionados, clique em **[!UICONTROL Ações]** no canto superior direito e clique em **[!UICONTROL Registrar]**.

1. Na janela pop-up, clique em **[!UICONTROL Sim]**.

Os usuários selecionados receberão um email de Boas-vindas. Se os alunos tiverem uma Adobe ID existente, eles poderão clicar neste link. Se eles não tiverem uma Adobe ID existente, poderão clicar no link Bem-vindo para criar uma Adobe ID e vinculá-la à sua conta do Learning Manager.

Os alunos devem obrigatoriamente clicar em um desses links do e-mail para que o Learning Manager possa verificar a conta do aluno.

+++

+++Como editar dados do usuário?

Para editar um usuário, siga as etapas abaixo:

1. Na lista de usuários, clique no usuário para quem deseja editar os dados.
1. Clique no ícone de lápis, conforme mostrado abaixo.

![](assets/edit-user-data.png)

No menu **[!UICONTROL Editar usuário]** , atualize os campos adequadamente. Para salvar as alterações, clique em **[!UICONTROL Salvar]**.

+++

+++Como pausar e retomar um usuário externo no Learning Manager?

Na lista de Usuários Externos, escolha o usuário que deseja excluir. No canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Pausar]**.

Para obter mais informações, consulte [Pausar um perfil externo](add-users-user-groups.md#pause).

Depois de pausar um perfil, o perfil externo exibe o status como ***Pausado***.

+++

+++Como enviar um e-mail de boas-vindas para um perfil externo recém-criado?

Ao adicionar um usuário externo, no menu **[!UICONTROL Adicionar Perfil de Registro Externo]** , insira o e-mail do gerente externo. Quando você clica em Salvar, um e-mail de boas-vindas também é enviado para o endereço de e-mail especificado. Se quiser enviar o e-mail de boas-vindas novamente, clique no ícone de envelope, conforme mostrado abaixo:

![](assets/send-welcome-mail.png)

+++

+++Como criar grupos de usuários personalizados?

Clique em **[!UICONTROL Usuários]** > **[!UICONTROL Grupos de usuários]** e na página Grupos de usuários, clique em **[!UICONTROL Adicionar]**. Na caixa de diálogo Adicionar grupo de usuários, adicione os usuários individualmente e como uma equipe.

![](assets/custom-user-group.png)

+++

+++Como desativar campos ativos já preenchidos?

Se você deseja que os alunos vejam apenas os campos ativos que não estão preenchidos por eles, siga as etapas abaixo:

1. Clique em **[!UICONTROL Usuários]** > **[!UICONTROL Campos ativos]**.

1. Clique em **[!UICONTROL Configurações]** e ative a opção **[!UICONTROL Mostrar apenas campos não preenchidos no logon do aluno]**.

1. Clique em **[!UICONTROL Salvar]**.

+++

+++Como impedir que os alunos insiram valores aleatórios nos campos ativos?

Você pode restringir a seleção dos alunos para que eles possam selecionar apenas os valores predefinidos e não digitar valores aleatórios. Siga as etapas abaixo:

1. Clique em **[!UICONTROL Usuários]** > **[!UICONTROL Campos ativos]**.
1. Na seção **[!UICONTROL Configurar campos]**, clique em **[!UICONTROL Modificar Valores]**.

1. Ativar a opção **[!UICONTROL Restringir seleção]**.
1. Clique em **[!UICONTROL Concluído]**.

+++

+++Como diferenciar campos ativos CSV e campos ativos personalizados?

Você só pode ativar ou desativar campos ativos CSV, mas não pode excluí-los. Por outro lado, não é possível ativar ou desativar campos ativos personalizados.

+++
