---
description: Saiba como adicionar usuários ou grupos de usuários no aplicativo Learning Manager.
jcr-language: en_us
title: Adicionar usuários e criar grupos de usuários
contentowner: manochan
exl-id: 7df98f2b-c422-4733-8ce4-5489506d4fdf
source-git-commit: aceee425ceb799fa3f742ac813bb35df16b34371
workflow-type: tm+mt
source-wordcount: '4061'
ht-degree: 61%

---

# Adicionar usuários e criar grupos de usuários

Saiba como adicionar usuários ou grupos de usuários no aplicativo Learning Manager.


<!--![](assets/user-mgmt-new.png)-->

## Gerenciar grupos de usuários

>[!INFO]
>
>Neste treinamento, você aprenderá como criar um grupo de usuários por nomes, IDs de e-mail e combinar vários grupos de usuários gerados automaticamente.<br><br>[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=QLD1P6BS&amp;mv=display&amp;mv2=display#/course/7555694)</br></br>

<!--[Launch training](https://learningmanager.adobe.com/app/learner?accountId=98632&sdid=QLD1P6BS&mv=display&mv2=display#/course/7555694)-->

<!--In this training, you will learn how to create a user group by names, email IDs, and combining multiple auto-generated user groups.-->

<!--[![button](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&sdid=QLD1P6BS&mv=display&mv2=display#/course/7555694)-->

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

## Visão geral {#overview}

No Adobe Learning Manager, você pode assumir as funções a seguir:

* **Administrador:** administradores definem a estratégia de treinamento da organização. Administradores podem adicionar alunos; pesquisar as habilidades necessárias dos alunos; gerenciar e atribuir cursos; criar planos de aprendizado, certificações e programas de aprendizado; e gerenciar relatórios para toda a organização.
* **Autor:** autores são Designers instrucionais e criadores de conteúdo. Um Autor pode adicionar módulos e cursos ao Learning Manager.
* **Gerente:** gerentes controlam as atividades de aprendizado de uma equipe. Um gerente pode indicar membros da equipe para um curso, aprovar solicitações de membros da equipe e fornecer feedback sobre o desempenho dos membros da equipe após a conclusão do treinamento. Gerentes também podem visualizar relatórios da equipe para acompanhar seu desempenho.
* **Aluno:** alunos podem acessar cursos, programas de aprendizado e certificações que lhe forem atribuídas. Além disso, alunos podem navegar por todos os cursos usando um catálogo e se inscrever em cursos, programas de aprendizado ou certificações.

Como administrador, você pode adicionar usuários de três maneiras:

* Internos
* Externos
* Grupos de usuários

## Adicionar um único usuário {#addasingleuser}

Adicione alunos internos ao Adobe Learning Manager usando uma opção de usuário único.

>[!INFO]
>
>Neste treinamento, você aprenderá como adicionar alunos internos ao Adobe Learning Manager.<br><br>[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=QGMZPB2T&amp;mv=display&amp;mv2=display#/course/7555534)</br></br>


Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

Para adicionar usuários,

1. Faça o logon no Adobe Learning Manager como administrador.
1. Na página inicial, clique em **[!UICONTROL Adicionar usuários]**. Nesta página, você pode adicionar um único usuário ou vários usuários por vez usando um arquivo CSV. Também é possível criar um link de autorregistro para funcionários internos ou criar um perfil de aluno externo.
1. Para adicionar um único usuário, clique em **[!UICONTROL Adicionar]** no canto superior direito e escolha a opção **[!UICONTROL Usuário único]**.

1. Para adicionar um único usuário, clique em **[!UICONTROL Adicionar]** no canto superior direito e escolha a opção **Usuário único**.


   ![](assets/single-user.png)
   *Adicionar um único usuário interno*

1. Na caixa de diálogo **[!UICONTROL Adicionar usuário]**, insira os detalhes do aluno. Para o campo **[!UICONTROL Nome do gerente]**, escolha o nome de um usuário existente no sistema.

   ![](assets/manager.png)
   *Caixa de diálogo Adicionar usuário*

1. Para adicionar o novo usuário no Learning Manager, clique em **[!UICONTROL Adicionar]**. Depois de adicionado, o usuário recebe um e-mail de verificação. O Aluno ativa a conta e começa a usar o Learning Manager. Este fluxo de trabalho é útil se você precisar adicionar um número limitado de alunos à sua conta do Learning Manager. Caso deseje inscrever todos os funcionários em uma organização grande, é possível adicioná-los de uma só vez. Para obter mais informações, consulte a próxima seção.

## Adicionar usuários em massa {#addusersinbulk}

### Gerenciar usuários

Neste treinamento, você aprenderá como atribuir e remover funções, enviar um email de boas-vindas e excluir e limpar usuários.

[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=4X3B8VJ2&amp;mv=display&amp;mv2=display#/course/7555586)

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

A maioria das organizações costuma usar Sistemas de Gerenciamento de RH (HRMS) para gerenciar todos os registros de funcionários, como designação, local, data de adesão ou hierarquia de funcionários. Esses dados podem ser exportados no formato CSV. Para importar um CSV, siga as etapas abaixo:


1. Clique em **[!UICONTROL Adicionar]** no canto superior direito e escolha a opção **[!UICONTROL Carregar um CSV]**.

   ![](assets/upload-a-csv.png)
   *Carregar um CSV para adicionar usuários em massa*

1. O arquivo CSV carregado consiste nos campos mostrados a seguir:

   ![](assets/csv.png)
   *Estrutura do CSV*

   Você deve manter um CSV mestre e executar todas as adições e exclusões no CSV mestre. O CSV mestre contém os seguintes campos:

   * nome &#42;
   * email &#42;
   * perfil
   * gerente

   (&#42;) Campo obrigatório.

1. Depois de clicar na opção **[!UICONTROL Carregar um CSV]**, o diálogo a seguir é exibido.

   ![](assets/upload-a-csv-dialog.png)
   *Carregar uma caixa de diálogo CSV*

1. Selecione o CSV ou arraste e solte o arquivo. Depois de escolher o arquivo, mapeie os campos de dados com os do arquivo CSV. Clique no menu suspenso solicitado e escolha o campo correto.

   ![](assets/map-data-fields.png)
   *Mapear campos no CSV*

1. Para iniciar a importação dos usuários, clique em **[!UICONTROL Salvar]**. Uma mensagem de confirmação será exibida.

   ![](assets/save-csv.png)
   *Mensagem de confirmação para carregamento bem-sucedido do CSV*

1. Os novos usuários foram adicionados à sua conta do Adobe Learning Manager. Para selecionar os novos usuários, marque a caixa de seleção ao lado dos nomes para que todos sejam selecionados.

   ![](assets/select-new-users.png)
   *Novos usuários adicionados*

>[!NOTE]
>
>Para obter mais informações, consulte as perguntas frequentes, [Adicionar usuários em massa](../add-users-in-bulk.md).

Depois de selecionar os usuários, você pode:

## Registrar um usuário {#registerauser}

Com o usuário selecionado, clique em **[!UICONTROL Ações]** no canto superior direito e clique em **[!UICONTROL Registrar]**.

Os usuários selecionados receberão um e-mail de Boas-vindas. Alunos que tiverem uma Adobe ID, poderão clicar nesse link. Se eles não tiverem uma Adobe ID existente, poderão clicar no link Bem-vindo para criar uma Adobe ID e vinculá-la à sua conta do Learning Manager.

## Atribuir uma função {#assignarole}

Depois de adicionar alunos à conta do Adobe Learning Manager, caso deseje alterar suas funções, clique em Ações no canto superior direito da página. Selecione a opção **[!UICONTROL Atribuir função]**. Aqui você pode optar por conceder acesso de Autor ou de Administrador ao aluno. Depois de atribuir uma função, esse aluno tem acesso de autor à conta e pode adicionar módulos e criar cursos.

![](assets/assign-a-role.png)
*Atribuir uma função a um usuário*

## Remover uma função {#removearole}

Você também pode remover o acesso de Autor ou de Administrador dos usuários. Selecione um ou mais alunos, clique em **[!UICONTROL Ações]** e selecione **[!UICONTROL Remover função]**. Escolha uma opção, por exemplo, **[!UICONTROL Remover autor]**, e o acesso de autor será revogado para este aluno.

>[!NOTE]
>
>Você não pode atribuir manualmente a função Gerente para um usuário no sistema. Eles recebem acesso ao Painel do gerente automaticamente quando um ou mais funcionários forem atribuídos a eles.

## Excluir um usuário {#deleteauser}

Para excluir um usuário, clique em **[!UICONTROL Ações]** e selecione **[!UICONTROL Excluir usuário]**. No diálogo de confirmação, clique em **[!UICONTROL Sim]** e o aluno será excluído.

![](assets/delete-a-role.png)
*Mensagem de confirmação para excluir um usuário*

## Editar um usuário {#editauser}

Na lista de usuários, clique em um usuário selecionado. Nos detalhes do usuário, clique no botão **[!UICONTROL Editar]** ( ![](assets/edit-pen.png)). Na caixa de diálogo **[!UICONTROL Editar usuário]**, faça as edições necessárias e clique em **[!UICONTROL Salvar]** para salvar as alterações.

![](assets/edit-user.png)
*Caixa de diálogo Editar Usuário*

## Campos ativos

### Gerenciar atributos de usuário

>[!INFO]
>
>Neste treinamento, você aprenderá como adicionar, personalizar e configurar campos ativos.<br><br>[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=55KD8M1Z&amp;mv=display&amp;mv2=display#/course/7555741)</br></br>

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

O Adobe Learning Manager preserva a diferenciação de maiúsculas e minúsculas do atributo de usuário e seu valor. **Por exemplo**, a diferenciação de maiúsculas e minúsculas de um atributo de usuário é &#39;location&#39; e seu valor como &#39;PARIS&#39; será preservado e exibido da mesma maneira. Em caso de problemas, o administrador agora pode editar o nome e os valores do atributo para corrigir quaisquer erros de diferenciação de maiúsculas e minúsculas.

O administrador pode fazer isso acessando o **[!UICONTROL Aplicativo do administrador]** > **[!UICONTROL Usuários]** > **[!UICONTROL Grupos de usuários]** e clicando no nome do grupo.

Um administrador pode adicionar e atualizar valores de atributo permitidos para um aluno por meio da interface do usuário.

Tipos de campos ativos:

* Agrupável: os alunos seriam agrupados com base nos valores
* Reportável: os grupos de usuários de relatórios seriam criados com base nos campos ativos
* Exportável: os campos serão exibidos no relatório de grupo de usuários exportado.

## Criar um link de autorregistro {#createaselfregistrationlink}

Também é possível permitir que funcionários da sua organização se registrem como Alunos na conta do Adobe Learning Manager sem a necessidade de um administrador. O administrador pode criar um link de autorregistro e compartilhar com os funcionários, que podem se registrar no Learning Manager usando suas credenciais de Adobe.



No canto superior direito da página, clique em **[!UICONTROL Adicionar]** e selecione **[!UICONTROL Autorregistro]**.


![](assets/self-registration.png)
*Criar link para se registrar como aluno*

A caixa de diálogo **[!UICONTROL Adicionar perfil de autorregistro]** é exibida. Dê um nome a este perfil. Em seguida, adicione o nome do gerente. É importante saber que o gerente já deve estar registrado como aluno no Learning Manager.

![](assets/add-self-registrationprofile.png)
*Adicionar perfil para autorregistro*

Depois de clicar em **[!UICONTROL Salvar]**, é gerado um URL que pode ser compartilhado com os alunos. Eles podem clicar na URL para se autorregistrarem.

## Inscrever alunos externos {#enrollexternallearners}

No Adobe Learning Manager, também é possível criar links de Registro para parceiros externos ou agências externos com acesso limitado à sua conta para fornecer-lhes material de aprendizagem.

Note que existem algumas diferenças entre registros internos e externos.

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
    <p>Faça o logon usando as credenciais da Adobe ID ou do SSO.</p></td>
   <td>
    <p>Faça o logon usando qualquer ID de e-mail.</p></td>
  </tr>
  <tr>
   <td>
    <p>A gamificação está disponível.</p></td>
   <td>
    <p>Gamificação disponível. O administrador deve ativar a gamificação para alunos externos nas configurações de gamificação.</p></td>
  </tr>
  <tr>
   <td>
    <p>As hierarquias de aluno estão disponíveis.</p></td>
   <td>
    <p>As hierarquias de aluno não estão disponíveis.</p></td>
  </tr>
 </tbody>
</table>

Para inscrever usuários externos, siga as etapas a seguir:

1. No painel de navegação à esquerda, clique em **[!UICONTROL Externo]**.

   ![](assets/click-external.png)

   *Inscrever usuários externos*

1. No canto superior direito da página, clique em **[!UICONTROL Adicionar]**.

1. Na caixa de diálogo **Adicionar perfil de registro externo**, preencha os detalhes a seguir:


   * O nome do perfil da organização parceira.
   * O endereço de email do gerente da organização parceira.
   * Limite de vagas para inscrição externa para este parceiro.
   * Data de vencimento para definir um prazo para interromper a permissão de novos registros para este grupo. Após a Data de expiração, apenas os usuários já registrados poderão acessar esse treinamento.

   ![](assets/map-data-fields-2.png)

   *Adicionar caixa de diálogo Perfil de Registro Externo*

   * Na seção **[!UICONTROL Configurações Avançadas]**, insira o seguinte:

      * **[!UICONTROL Requisito de Logon]:** Especifique um valor em dias. Os alunos são excluídos se não fizerem logon no período acima.
      * **[!UICONTROL Domínios permitidos]:** Uma lista separada por vírgulas de nomes de domínio de email na lista de exceções.
      * **[!UICONTROL Verificação de email necessária]:** selecione esta opção para tornar a verificação de email obrigatória para um aluno.

   ![](assets/email-verificationrequired.png)

   *Insira os detalhes na seção Configurações Avançadas*

1. Depois de clicar em **[!UICONTROL Salvar]**, você verá a mensagem de confirmação a seguir. Compartilhe o URL com seu parceiro externo.

   ![](assets/save-and-share-urlwithexternalusers.png)

## Ativar um perfil externo {#enableanexternalprofile}

Depois de criar um perfil externo, você precisará ativar seu status. Na lista de perfis externos, selecione o perfil necessário e ative o botão de status.

![](assets/choose-required-profiles.png)
*Habilitar um perfil externo*

Isso ativa o link de Inscrição externa. Um e-mail de boas-vindas será enviado automaticamente ao parceiro. Também é possível copiar e compartilhar o link clicando no ícone Copiar URL () ou reenviar o e-mail de boas-vindas à organização parceira no ícone de Enviar e-mail ().

O gerente do parceiro pode compartilhar o link com os funcionários que devem realizar o treinamento no PrLearning Manager. Ao clicarem no link, eles poderão se inscrever automaticamente após preencher alguns detalhes para criar um perfil no Learning Manager. Esses usuários não aparecerão no guia Alunos com os funcionários internos. Você pode consultar seus nomes na guia **[!UICONTROL Alunos externos]**.

## Pausar um perfil externo {#pause}

Depois de adicionar um grupo de usuários externo ao Learning Manager, você também pode pausar o processo de registro de usuários externos. Quando você pausa, o processo de registro de usuários externos é bloqueado. No entanto, esse processo funciona apenas para usuários que ainda não aceitaram o convite de registro.

Para pausar os grupos de usuários externos, selecione um ou mais grupos, clique em **[!UICONTROL Ações]** no canto superior direito da página e clique em **[!UICONTROL Pausar]**.

## Continuar um perfil externo {#resumeanexternalprofile}

O estado pausado de um parceiro externo pode ser revogado a qualquer para continuar com os serviços normais. Clique em **[!UICONTROL Ações]** no canto superior direito da página e selecione **[!UICONTROL Retomar]**.

Os estados a seguir aplicam-se a usuários externos:

* **Estado inativo** - neste estado, o registro de usuários externos expirou. Administradores definem a data de expiração dos usuários externos no fluxo de trabalho de adição de usuário.
* **Estado ativo** - neste estado, usuários externos podem se registrar no aplicativo Learning Manager e fazer logon no aplicativo.
* **Pausa** - neste estado, o processo de registro para usuários externos está bloqueado. No entanto, os usuários existentes podem continuar fazendo logon.

## Verificar vagas utilizadas {#checkusedseats}

Na lista de perfis externos, clique em **[!UICONTROL Vagas utilizadas]**. É possível visualizar o número de alunos adicionados na organização parceira.

![](assets/seats-used.png)
*Verificar licenças usadas*

## Excluir um usuário {#Deleteauser-1}

Escolha um usuário e, no canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Excluir usuário]**.

## Alterar perfil {#changeprofile}

Para mover um usuário para outro perfil externo, escolha um usuário no canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Alterar Perfil]**. Na lista de perfis, selecione um perfil e clique em **[!UICONTROL Alterar]**.

## Atribuir uma função {#Assignarole-1}

Escolha um usuário e, no canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Atribuir função]** > **Criar`<role>`**. O usuário receberá uma nova função.

## Remover uma função {#Removearole-1}

Escolha um usuário e, no canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Remover função]** > **Remover`<role>`**. A função selecionada será removida da lista de funções atribuídas ao usuário.

## Criar grupos de usuários {#createusergroups}

Um Grupo de usuários é um conjunto de usuários relacionados a uma categoria. Grupos de usuários ajudam os administradores a filtrar os alunos da organização com base em atributos e, em seguida, atribuir seus conteúdos de aprendizado. Além disso, Grupos de usuários permitem que administradores atribuam logotipos e catálogos personalizados aos alunos e mostrem relatórios personalizados sobre seu progresso.

Para acessar os Grupos de usuários, clique em **[!UICONTROL Grupos de usuários]** no painel de navegação esquerdo.

![](assets/user-groups.png)
*Criar grupos de usuários*

Existem dois tipos de grupos no Adobe Learning Manager: Personalizados e Gerados automaticamente. Ao adicionar alunos à sua conta, alguns grupos serão criados automaticamente com base em propriedades comuns.

Para consultar os grupos criados automaticamente, clique na guia **[!UICONTROL Gerados automaticamente]**.

![](assets/auto-generated.png)
*Exibir grupos gerados automaticamente*

Note que há vários grupos, como Todos os usuários internos, Todos os gerentes, grupos com base no Centro de custo, com base no departamento e nas equipes dos gerentes.

Além dos grupos Gerados automaticamente, é possível criar grupos Personalizados. Para adicionar um novo Grupo Personalizado, no canto superior direito, clique em **[!UICONTROL Adicionar]**.

1. Digite o nome e a descrição do grupo.
1. Para adicionar usuários, digite o nome de usuário ou o perfil no campo de pesquisa ao digitar e selecione na lista suspensa.

1. Para adicionar mais alunos, clique em **[!UICONTROL Adicionar Mais Usuários]**.

1. Para criar o grupo de usuários, clique em **[!UICONTROL Salvar]**.

O Grupo personalizado foi criado e adicionado ao perfil. Os Grupos de usuários criados são dinâmicos por natureza. Caso novos usuários com atributos similares sejam adicionados, eles serão adicionados automaticamente ao Grupo de usuários.

## Exclusão de grupos de usuários

Às vezes, você deseja excluir um pequeno conjunto de usuários de um grande grupo de usuários. Isso é necessário para inscrever esse conjunto específico de usuários no treinamento por meio de Planos de aprendizado ou para configurar a visibilidade correta dos catálogos. Nesta versão do Learning Manager, você pode excluir alunos ou grupos de usuários ao criar um grupo de usuários personalizado. Na caixa de diálogo Adicionar grupo de usuários, a seção Excluir alunos permite isso.

![](assets/exclude-user-groups.png)
*Excluir grupos de usuários*

Por exemplo: se você deseja configurar um Plano de aprendizado para que todos os usuários que pertencem à localização = Califórnia, exceto Loja-5 (localizada na Califórnia) sejam inscritos.

## Configurações avançadas {#advancedsettings}

### Fontes de dados {#datasources}

Você pode usar esse recurso quando quiser importar/sincronizar os usuários ou os dados de aprendizado do banco de dados da sua organização no aplicativo Learning Manager. Você também pode configurar a frequência dessa sincronização.


Clique em **[!UICONTROL Fontes de Dados]** no painel esquerdo, na seção **[!UICONTROL Avançadas]**.


![](assets/data-sources-add-users.png)

*Fontes de dados para importar ou sincronizar usuários*

Escolha o tipo de fonte de dados no menu suspenso **[!UICONTROL Fonte]**, selecione a frequência de atualização e clique em **[!UICONTROL Sincronizar agora]** se precisar sincronizar imediatamente ou clique em **[!UICONTROL Salvar].** tipos de fontes de dados são SFDC, FTP e assim por diante para usuários internos.

É possível adicionar várias origens de dados.

### Campos ativos {#activefields}

Esse recurso permite que os administradores adicionem mais campos ativos além dos fornecidos durante o registro do usuário.

Clique em **[!UICONTROL Campos Ativos]** disponíveis na página de usuários. Os alunos só podem escolher entre os valores fornecidos em valores personalizados.

![](assets/active-fields.png)
*Campos ativos*

### Configurar campos {#configurefields}

**Usuários internos**

É possível adicionar um valor personalizado nos campos do usuário para usuários internos.

Para adicionar valores personalizados, siga estas etapas:

1. Clique em **[!UICONTROL Modificar Valores]** para um usuário Interno.

   ![](assets/modify-values.png)
   *Modificar valores para usuários internos*

1. A caixa de diálogo **Valores no campo Personalizado** é exibida.

   ![](assets/values-in-customfields.png)
   *Caixa de diálogo Valores em Campos Personalizados*

1. Selecione o valor a ser adicionado na lista suspensa do menu **[!UICONTROL Selecionar campo]**.
1. Digite os novos valores no campo **[!UICONTROL Novo valor]**.
1. Clique em **[!UICONTROL Concluído]**.
1. Clique em Salvar no canto superior direito para **[!UICONTROL salvar]** as alterações.

**Usuários externos**

Adicione valores personalizados semelhantes aos usados para usuários internos.

![](assets/modify-values-forexternalusers.png)
*Modificar valores para usuários externos*

### Configurações {#settings}

**Exibição do usuário**

Se a opção **Mostrar apenas campos não preenchidos no logon do aluno** estiver habilitada, um usuário verá apenas os campos em branco no logon.

![](assets/settings-tab.png)
*Mostrar campos não preenchidos*

Com essa opção, administradores podem optar por mostrar ou ocultar esses campos assim que forem preenchidos.

## Restringir campos ativos nos relatórios {#restrictactivefields}

O Learning Manager 27.7 apresenta duas novas opções: **[!UICONTROL Relatável]** e **[!UICONTROL Exportável]**, para Campos Ativos.

![](assets/options-in-activefields.png)
*Opções em Campos Ativos*

Nos campos CSV e campos adicionados manualmente, se um Campo ativo estiver marcado como **[!UICONTROL Relatável]**, o Campo ativo será pesquisável em um filtro dentro de um relatório do painel.

![](assets/filters-in-a-dashboardreport.png)
*Filtros em um relatório do painel*

Se um Campo ativo estiver marcado como **[!UICONTROL Exportável]**, o Campo ativo aparecerá no arquivo Excel após o download de qualquer relatório em Excel.

Essas opções são exibidas para Campos ativos internos e externos.

Você pode excluir apenas um Campo ativo personalizado.

## Exibição do usuário

Você pode ocultar a página inteira “Concluir seu perfil” dos alunos. A página não aparecerá quando o aluno fizer logon.

Observe que o comportamento padrão existente não é alterado. Esse é um recurso opcional agora disponível para administradores.

Ative as opções abaixo:

![](assets/user-display.png)
*Seção de Exibição do Usuário*

## Suporte para campos CSV manuais por conectores FTP e Box {#import-connector}

Geralmente, os usuários querem que os campos Ativos sejam fornecidos manualmente quando um aluno faz logon no Learning Manager. Isso é possível no Learning Manager no momento, quando o usuário importa um CSV manualmente.

O CSV não pode conter todos os campos Ativos. Para todos os campos ativos que não são atualizados no CSV carregado, o usuário precisa inserir os dados desses campos ativos.

Atualmente, todos os campos ativos devem ser mapeados para algum campo do CSV de origem.

Ocorre que, às vezes, um usuário não deseja mapear um campo Ativo para um campo especificado no CSV. Nesses casos, o usuário pode mapear o campo Ativo para o valor **[!UICONTROL DontImportFromSource]**. Selecione esse valor na lista suspensa ao importar usuários de conectores FTP e Box.

## Funções personalizadas {#customroles}

Adicione qualquer campo de sua escolha como parte das informações do usuário e clique em **[!UICONTROL Salvar]**. Depois de adicionar os campos, você também pode verificar a disponibilidade dos campos na caixa de diálogo **[!UICONTROL Editar usuários]**.


Depois de adicionar os campos, note que os campos com marca de seleção vieram de uma fonte de dados ou de um CSV, conforme mencionado na captura a seguir. Administradores podem alterar esses campos importados ativando-os ou desativando-os.

**Valores para campos ativos no Learning Manager**

Os valores dos campos ativos são obtidos das seguintes maneiras:

1. O aplicativo Learning Manager importa metadados de fontes de dados associadas à sua conta.
1. Os metadados são capturados de um arquivo CSV importado manualmente.
1. Alunos preenchem metadados ao fazer o logon
1. Os administradores inserem dados para os usuários.

>[!NOTE]
>
>O aplicativo Learning Manager cria grupos de usuários automaticamente a partir desses metadados.

**Adicionar valor personalizado**

É possível adicionar um valor personalizado nos campos de usuários Internos e Externos.

Para adicionar valores personalizados, siga estas etapas:

Campos personalizados podem ser adicionados e excluídos e são aplicáveis a todos os usuários. Os campos CSV podem ser ativados ou desativados. Eles só entram em vigor quando o carregamento do CSV é realizado após as modificações nos campos Ativos. Todos os campos ativos internos são aplicáveis a todos os tipos de usuários Internos. Campos externos são aplicáveis apenas a usuários Externos. Caso um campo personalizado esteja presente no CSV, ele será automaticamente convertido em campo CSV automaticamente no próximo carregamento e será ativado.

## Valores para campos CSV {#valuesforcsvfields}

Caso a caixa de seleção **[!UICONTROL Restringir seleção]** esteja ativada, os usuários só poderão escolher a partir de campos predefinidos nos campos CSV.

![](assets/value-field-for-csv.png)
*Caixa de seleção Restringir seleção*

## Importar registros {#importlogs}

Neste espaço, é possível visualizar o histórico de importação de CSV dos usuários adicionados pelo administrador com o recurso de importação em massa. Você também pode clicar em **[!UICONTROL Adicionar]** no canto superior direito da página para adicionar usuários usando o recurso de carregamento de CSV.

## Campos ativos de valores múltiplos

Com esse recurso, você pode ter mais de um campo para um campo ativo. Em uma conta, pode haver no máximo três campos ativos com valores múltiplos. Os campos ativos de valores múltiplos estão disponíveis para usuários externos e internos.

Depois de marcar um campo ativo como valores múltiplos, você não poderá convertê-lo novamente em um único valor. Isto é irreversível.

Um campo de valor único existente não pode ser marcado como campo de valores múltiplos.

Para criar um campo ativo de valores múltiplos, siga as etapas abaixo:

1. Adicione um campo ativo.

   ![Adicionar um campo ativo](assets/add-active-field.png)
   *Adicionar um campo ativo*

1. Clique em Adicionar.
1. Na guia Configurações marque o novo campo como valores múltiplos.

   ![Marcar como valores múltiplos](assets/mark-multi-valued.png)
   *Marcar como valores múltiplos*

   Há outra caixa de seleção, **[!UICONTROL Configurável pelo aluno]**, que quando desabilitada, o aluno não poderá ver o campo na página Perfil.

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

Depois de adicionar um usuário e atribuir a ele uma função, você poderá registrar o usuário executando as etapas abaixo:

1. Com o usuário ou usuários selecionados, clique em **[!UICONTROL Ações]** no canto superior direito e clique em **[!UICONTROL Registrar]**.

1. Na janela pop-up, clique em **[!UICONTROL Sim]**.

Os usuários selecionados receberão um e-mail de boas-vindas. Alunos que tiverem uma Adobe ID, poderão clicar nesse link. Se eles não tiverem uma Adobe ID existente, poderão clicar no link Bem-vindo para criar uma Adobe ID e vinculá-la à sua conta do Learning Manager.

Os alunos devem obrigatoriamente clicar em um desses links do e-mail para que o Learning Manager possa verificar a conta do aluno.

+++

+++Como editar dados do usuário?

Para editar um usuário, siga as etapas abaixo:

1. Na lista de usuários, clique no usuário para quem você deseja editar os dados.
1. Clique no ícone de lápis, conforme mostrado abaixo.

![](assets/edit-user-data.png)

Na caixa de diálogo **Editar usuário**, atualize os campos corretamente. Para salvar as alterações, clique em **[!UICONTROL Salvar]**.

+++

+++Como pausar e retomar um usuário externo no Learning Manager?

Na lista de Usuários externos, escolha o usuário que deseja excluir. No canto superior direito, clique em **[!UICONTROL Ações]** > **[!UICONTROL Pausar]**.

Para obter mais informações, consulte [Pausar um perfil externo](add-users-user-groups.md#pause).

Depois de pausar um perfil, o perfil externo exibirá o status como ***Pausado***.

+++

+++Como enviar um e-mail de boas-vindas para um perfil externo recém-criado?

Ao adicionar um usuário externo, na caixa de diálogo **[!UICONTROL Adicionar Perfil de Registro Externo]**, insira o email do gerente externo. Quando você clica em Salvar, um e-mail de boas-vindas também é enviado para o endereço de e-mail especificado. Se quiser enviar o e-mail de boas-vindas novamente, clique no ícone de envelope, conforme mostrado abaixo:

![](assets/send-welcome-mail.png)

+++

+++Como criar grupos de usuários personalizados?

Clique em **[!UICONTROL Usuários]** > **[!UICONTROL Grupos de usuários]** e, na página Grupos de usuários, clique em **[!UICONTROL Adicionar]**. Na caixa de diálogo Adicionar grupo de usuários, adicione os usuários individualmente e como uma equipe.

![](assets/custom-user-group.png)

+++

+++Como desativar campos ativos já preenchidos?

Se você deseja que os alunos vejam apenas os campos ativos que não estão preenchidos por eles, siga as etapas abaixo:

1. Clique em **[!UICONTROL Usuários]** > **[!UICONTROL Campos Ativos]**.

1. Clique em **[!UICONTROL Configurações]** e habilite a opção **[!UICONTROL Mostrar apenas campos não preenchidos no logon do aluno]**.

1. Clique em **[!UICONTROL Salvar]**.

+++

+++Como impedir que os alunos insiram valores aleatórios nos campos ativos?

Você pode restringir a seleção dos alunos para que eles possam selecionar apenas os valores predefinidos e não digitar valores aleatórios. Siga as etapas abaixo:

1. Clique em **[!UICONTROL Usuários]** > **[!UICONTROL Campos Ativos]**.
1. Ative a opção **[!UICONTROL Restringir seleção]**.
1. Clique em **[!UICONTROL Concluído]**.

+++

+++Como diferenciar campos ativos CSV e campos ativos personalizados?

Você só pode ativar ou desativar campos ativos CSV, mas não pode excluí-los. Por outro lado, não é possível ativar ou desativar campos ativos personalizados.

+++
