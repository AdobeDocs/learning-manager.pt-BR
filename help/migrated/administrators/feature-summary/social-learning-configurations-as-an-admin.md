---
description: Como administrador, você pode ativar, desativar e monitorar as atividades executadas no Aprendizado social. Quando o recurso Aprendizado social estiver ativado, os alunos podem visualizá-lo e começar a participar do Aprendizado social.
jcr-language: en_us
title: Monitoramento e moderação do Aprendizado social como administrador
contentowner: kuppan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3604'
ht-degree: 0%

---



# Monitoramento e moderação do Aprendizado social como administrador

Como administrador, você pode ativar, desativar e monitorar as atividades executadas no Aprendizado social. Quando o recurso Aprendizado social estiver ativado, os alunos podem visualizá-lo e começar a participar do Aprendizado social.

## Ativar e definir configurações no aprendizado social {#enableandconfiguresettingsinsociallearning}

Para ativar e configurar o recurso Aprendizado social, faça o seguinte:

1. Clique em **[!UICONTROL Aprendizado social]** no painel de navegação esquerdo. Você é redirecionado para a página de atividade.
1. Habilitar **[!UICONTROL Aprendizado social]** recurso usando o **[!UICONTROL Habilitar]** na página Atividade, se estiver ativando-o pela primeira vez. Caso contrário, ele poderá ser ativado na **[!UICONTROL Configurações]** página.

   Uma caixa de diálogo pop-up aparece, como a captura de tela abaixo.

   ![](assets/artboard-20-2x.png) ![](assets/enable-social-learningforthefirsttime.png)

   *Habilitar aprendizado social*

<!-- ![](assets/enable-social-learningfeatureinsettings.png) ![](assets/enable-social-learningdialog.png)-->

O administrador pode definir as configurações de Aprendizado social. As configurações incluem tipos de curações de conteúdo, como **[!UICONTROL Curadoria apenas manual]** e **[!UICONTROL Sem curadoria]**. As configurações de escopo podem ser definidas com escopo diferente, como o tipo de usuário (interno/externo) ou qualquer outro campo ativo presente na conta. O administrador pode definir o caminho do URL onde os alunos podem baixar o aplicativo de desktop Adobe Learning Manager.

## Curadoria de conteúdo {#contentcuration}

Como o Aprendizado social é um aprendizado informal, sua funcionalidade é semelhante a outras plataformas de mídia social. Muitas vezes, as pessoas acham que as mídias sociais distraem porque frequentemente consomem conteúdo irrelevante que afeta sua produtividade. Esse pensamento pode ser atendido pela moderação de conteúdo e curadoria.

**[!UICONTROL Curadoria apenas manual]** e **[!UICONTROL Sem curadoria]** Há duas opções de curadoria que podem ser selecionadas pelo administrador.

**[!UICONTROL Curadoria manual assistida automaticamente]:** O Learning Manager tem um mecanismo de curadoria automática baseado em inteligência artificial que pode descobrir de forma inteligente a essência do conteúdo de qualquer formato que possa ser fornecido posteriormente aos alunos desejados. Ele também pode aprovar ou rejeitar que um conteúdo seja publicado com base na pontuação de confiança fornecida.

Por exemplo, Adarsh é um aluno e achou um blog interessante, então ele o publicou na plataforma de aprendizado social do Adobe Learning Manager. A publicação é então enviada ao Mecanismo de curadoria de conteúdo viabilizado por IA, que prevê as habilidades presentes no conteúdo e as compara com as habilidades associadas ao conselho. Se alguma das habilidades corresponder, o conteúdo será publicado; caso contrário, será enviado para curadoria manual.

A pontuação mínima de confiança necessária para o lançamento é de 50%.

**[!UICONTROL Curadoria apenas manual]:** Para verificar a autenticidade do conteúdo antes que ele entre no ar, o administrador pode ativar a configuração de curadoria apenas manual. Quando a configuração de curadoria Somente manual está ativada, ela vai para os Principais SMEs (Máximo 3) para curadoria. Com base na resposta média, a publicação é aprovada/rejeitada adequadamente. Se a resposta for maior do que 50 por cento, a postagem será publicada ou rejeitada. Para mais informações sobre as PME, [clique aqui](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

## Curadoria automática de conteúdo {#autocuration}

A moderação manual do conteúdo geralmente está sujeita a erros e é demorada. Além disso, o processo não é escalável e é inadequado para um grande volume de atividades sociais. Portanto, a curadoria de conteúdo automaticamente se torna essencial ao atender muitos usuários que estão ativos socialmente.

No Learning Manager, há uma opção para selecionar conteúdo automaticamente. A curadoria é realizada por um mecanismo habilitado por IA, que mapeia trabalhos com as habilidades predefinidas, depois que o administrador mapeia as habilidades predefinidas com uma habilidade. Para obter mais informações, consulte [Mapeamento de domínio de habilidade](curation-skills.md).

Na curadoria automática, os seguintes tipos de conteúdo são permitidos:

* PDF
* Arquivos de áudio e vídeo
* Presentations - PPT ou PPTX
* Documentos- .doc, .docx

Um administrador pode ativar a opção de selecionar conteúdo automaticamente no aplicativo do administrador.

1. No painel esquerdo do aplicativo de administração, clique em **[!UICONTROL Aprendizado social]**.
1. Na página, clique na guia **[!UICONTROL Configurações]**.
1. Ativar a opção **[!UICONTROL Curadoria manual assistida automaticamente]**.

   ![](assets/auto-curation.png)

   *Selecione a opção Curadoria manual assistida automaticamente*

Quando um usuário faz upload de um conteúdo em um painel, um algoritmo baseado em IA retira o texto do conteúdo e o texto é passado para o mecanismo de curadoria. O mecanismo de curadoria tenta encontrar as habilidades presentes no conteúdo.

As habilidades previstas do conteúdo carregado são correspondidas com as do painel em que o conteúdo foi carregado.  Se alguma habilidade corresponder a uma pontuação de confiança de mais de 50% da habilidade do quadro, o conteúdo será publicado no quadro. Se a pontuação de confiança for inferior a 50%, o conteúdo será enviado para curadoria manual.

Sempre que um conteúdo é selecionado automaticamente, o usuário recebe uma notificação de que o conteúdo está disponível no quadro em que foi carregado anteriormente.

![](assets/only-ai-based.png)

*Fluxograma de configurações de curadoria*

Recomenda-se que o administrador adicione SMEs para habilidades se a curadoria Somente manual estiver ATIVADA. O administrador pode adicionar SMEs fornecendo pontos de SME com antecedência aos usuários com experiência em uma habilidade. Para saber mais sobre como fornecer pontos para as PME,  [clique aqui](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

**Sem curadoria:** Todas as publicações do aluno são publicadas automaticamente sem qualquer moderação de conteúdo.

<!--![](assets/artboard-6-2x.png)-->

## Perguntas frequentes sobre curadoria automática de conteúdo {#faq-auto-curation}

+++Quanto tempo uma PME tem para organizar uma publicação?

Uma SME demora no mínimo 24 horas para fazer a curadoria de uma publicação. Devido a diferenças de fuso horário, ele pode ser aumentado para 47 horas.

+++

+++Vai para o próximo conjunto de três PMEs se todas as três estiverem disponíveis? São sempre três as PME que se envolvem?

A solicitação de curadoria vai para o topo das SMEs no primeiro dia. Se eles não responderem, a solicitação será enviada para as próximas três SMEs no dia seguinte.

Se as três novas SMEs não responderem, a solicitação será encaminhada aos moderadores do conselho.

Se os moderadores do painel não responderem, a solicitação será aprovada automaticamente.

+++

+++Se duas SMEs fizerem curadoria e uma não, o pedido vai para a quarta SME ou o pedido toma a média, seja qual for a primeira rodada de SMEs que classifica a publicação?

É necessário um índice de aprovação de 50% para aprovar a vaga. Da mesma forma, a classificação de rejeição de 50% é usada para rejeitar a publicação. Em cada aprovação feita por uma SME, avalia-se se ela atingiu 50%.

Se não atingir 50% após um dia, ele será enviado para o próximo conjunto de SMEs que expirar as solicitações anteriores de curadoria não respondidas.

Por exemplo, no primeiro dia, a solicitação de curadoria é enviada a três SMEs; e uma delas aprova, duas delas não responderam. No dia seguinte, a solicitação de curadoria vai para o próximo conjunto de três SMEs. Nesse nível, agora há quatro SMEs ativas no total. Pelo menos duas SEMs devem aprová-la para que a curadoria seja aprovada.(Caso 2 aprove e 2 rejeite, o que atingir os primeiros 50% será usado.)

+++

+++Pelo o que vejo, um “Moderador” é atribuído apenas (e não é obrigatório) quando alguém cria um novo painel - Qual é o caso de uso para um Aluno atribuir um “Moderador” a um painel se as SMEs forem atribuídas à habilidade associada a um painel?

São responsabilidades de um moderador do Conselho Social:

* Capacidade de editar o nome, a descrição, as configurações de visibilidade do painel e outras configurações.
* Capacidade de excluir uma publicação no painel caso a publicação não seja adequada ao público.
* O moderador recebe notificações de “Denunciar abuso” para o painel.
* O moderador recebe solicitações de curadoria se nenhum SME estiver presente para o painel.

+++

+++Nossa equipe de treinamento estará adicionando / monitorando as habilidades associadas ao nível de habilidade, bem como as SMEs atribuídas às habilidades.

Os SMEs são adicionados/atribuídos com base na habilidade, não no nível de habilidade. Isto é o que foi projetado.

+++

+++Qual é a diferença entre um “moderador” de aprendizado social e um “SME” de aprendizado social?

**Moderadores:** Proprietários secundários do painel. Eles são adicionados pelos criadores durante a criação do painel para que possam controlar o painel na ausência do criador. Por padrão, o criador do painel é o moderador.

**PME:** Especialistas no assunto são especialistas em habilidades específicas. O administrador pode atribuir SMEs a uma habilidade específica para selecionar o conteúdo dessa habilidade. As SMEs recebem os pedidos de curadoria para conselhos vinculados às suas habilidades. Os alunos também podem se tornar PME ganhando pontos de SME.

+++

+++Se houver duas ou três SMEs atribuídas a uma habilidade: a aprovação ou rejeição de uma pós-aprendizagem social depende de todas as curadorias das SMEs ou de quem fazer a curadoria primeiro?

É necessário um índice de aprovação de 50% para aprovar a vaga. Da mesma forma, a classificação de rejeição de 50% é usada para rejeitar a publicação. Em cada aprovação feita por uma SME, avalia-se se ela atingiu 50%.

Se não atingir 50% após um dia, ele será enviado para o próximo conjunto de SMEs que expirar as solicitações anteriores de curadoria não respondidas.

+++

## Configurações do escopo {#scopesettings}

No Aprendizado social, um escopo determina os painéis que você vê, que controlam a visibilidade do conteúdo. Se um usuário tiver um escopo, por exemplo, ***Fornecedor_A***, ele só pode ver painéis de discussão e postagens associadas que foram criadas por outras pessoas que pertencem ao mesmo escopo ***Fornecedor_A***.

Isso permite que os administradores mantenham um grupo de usuários, por exemplo, fornecedores, parceiros ou departamentos em uma organização separada.

Ative o aprendizado social e o quadro de classificação para usuários internos e externos.

Há seções separadas para habilitar usuários internos e externos.

**Ativar para alunos internos**

Nesta seção, você pode escolher a característica do usuário para definir o escopo do aprendizado social para usuários internos. Usuários com as mesmas características **valor** compartilhe o mesmo espaço de aprendizado social.

Na guia **Característica do usuário** , escolha a opção desejada.

![](assets/choose-value-of-usercharacteristic.png)

*Selecione as características do usuário para definir o escopo*

Por padrão, a opção **[!UICONTROL Todos os usuários internos]** na lista suspensa Característica do usuário, a opção está sempre selecionada.

Você pode definir o escopo dos usuários internos com base em seus campos ativos.

**Ativar para alunos externos**

Para definir o escopo do aprendizado para usuários externos, use um perfil externo. Os alunos com o mesmo perfil externo compartilham um espaço comum de aprendizado social.

![](assets/choose-an-externalprofile.png)

*Ativar escopo para alunos externos*

Os usuários externos têm o escopo definido com base em seus perfis externos.

Por exemplo, na lista acima, se você ativar **[!UICONTROL Acme Corp]**, todos os alunos pertencentes à Acme Corp podem ver os painéis que criaram. Se você desativar a opção **Henry Cavill** No entanto, os alunos não podem ver nenhum painel criado por Henry Cavill.

O administrador pode definir o escopo da visibilidade do conteúdo com base no campo ativo exibido na **[!UICONTROL Característica do usuário]** campo.

Por exemplo, o administrador pode definir o escopo como **[!UICONTROL Tipo de Usuário (Interno/Externo)]** usuários. Ao definir o escopo como Tipo de usuário, o conteúdo compartilhado na plataforma de aprendizado social por qualquer aluno interno só é visível para outros alunos internos da organização e não para usuários externos e vice-versa.

Depois que uma Característica do usuário é selecionada pelo administrador, ele pode limitar o recurso Aprendizado social a alunos e grupos de alunos selecionando a caixa de seleção abaixo do campo de característica do usuário. Clique no campo de valor para selecionar o aluno ou os grupos de alunos para os quais deseja ativar o recurso Aprendizado social.

Por padrão, o escopo é definido pelo **[!UICONTROL Tipo de usuário]** que são alunos internos ou externos.

Se o campo ativo não contiver nenhum valor, o campo **[!UICONTROL Valor]** a lista suspensa de campos não estará visível para o administrador.

<!--![](assets/scope-settings.png) ![](assets/scope-settings1-png.jpg)-->

Os usuários também podem publicar seu conteúdo usando o aplicativo de desktop Adobe Learning Manager. Dependendo se você é um usuário do Mac ou do Windows, clique nos links fornecidos para baixar o aplicativo de desktop e siga as etapas abaixo para instalá-lo em seu sistema. Se estiver enfrentando dificuldades na instalação, [clique aqui](../../kb/troubleshooting-issues-with-adobe-learning-manager-desktop-app.md).

## Permissões de Criação do Painel {#permission}

Para restringir a criação de painéis por todos os alunos e moderar os painéis de forma eficaz, um administrador pode conceder permissões para criar painéis para um grupo seleto de usuários.

![](assets/grant-permissiontocreateboards.png)

*Definir permissões para criar um painel*

Por padrão, a opção **[!UICONTROL Todos os alunos]** está ativado.

**[!UICONTROL Todos os alunos]:** Se você escolher essa opção, todos os usuários internos e externos poderão criar painéis.

**Um grupo de alunos:** Se você escolher essa opção, somente os usuários com permissões para criar um painel verão o **[!UICONTROL Criar novo painel]** link no Aprendizado social. Escolha o grupo de usuários que deve receber permissão para criar um painel. Você também pode adicionar grupos de usuários gerados automaticamente e personalizados.

<!--![](assets/grant-permissiontoausergroup.png)-->

Os usuários que compartilham o mesmo escopo só podem ver o quadro. Para usuários que não têm permissão, o **[!UICONTROL Criar novo painel]** permanece invisível.

Para que as alterações entrem em vigor, aguarde 60 minutos.

## Usuários especiais {#privilege}

Um administrador pode conceder privilégios especiais a um grupo de usuários, usando quais membros do grupo podem participar de todos os painéis. Todas as restrições definidas na seção Configurações do escopo são ignoradas pelo grupo de usuários especial.

O grupo de usuários pode ser gerado automaticamente ou personalizado.

Um usuário que recebeu esse privilégio tem acesso a todos os painéis, exceto **placas privadas**.

![](assets/special-users.png)

*Conceder privilégios especiais*

Quando o administrador seleciona um grupo de usuários, por padrão, todos os usuários no grupo podem acessar todos os painéis, independentemente do escopo do usuário. Qualquer usuário com esses privilégios elevados pode visualizar e participar de todas as placas internas e externas.

Usuários especiais recebem solicitações de curadoria em todos os escopos se tiverem pontos SME suficientes para essa habilidade.

Se o usuário não tiver os pontos do SME necessários, os privilégios de curadoria serão passados para os três SMEs principais dessa habilidade.

No novo escopo, ele obtém pontos para atividades em todos os painéis.

Nas seções do quadro de classificação social, um usuário pode ver todos os usuários de seu escopo junto com os usuários especiais.

Caso tenha recebido privilégios especiais de usuário, você poderá ver todos os usuários na conta no quadro de classificação, independentemente dos escopos dos usuários.

Se os utilizadores especiais se tornarem PME através da obtenção de pontos suficientes, **[!UICONTROL Principais especialistas no assunto]** no quadro de classificação social.

Para que as alterações entrem em vigor, aguarde 60 minutos.

## Personalizar o banner social {#customize-social-banner}

O administrador pode personalizar o título e o subtítulo exibidos na imagem do cabeçalho na página inicial do Aprendizado Social. Qualquer que seja a decisão do administrador de inserir como título e subtítulo, o mesmo aparece na página de aprendizado social do aluno.

1. No aplicativo de administração, clique em **[!UICONTROL Aprendizado social]** > **[!UICONTROL Configurações]**.
1. Clique em **[!UICONTROL Personalizar]**.
1. Alterar a imagem do banner. As dimensões da imagem devem ser de pelo menos **1600 px X 240 px**.
1. Alterne a opção para ocultar ou exibir o **[!UICONTROL Saiba mais]** no banner.
1. Insira o título e o subtítulo nos campos especificados abaixo:

   ![](assets/image012.png)

   *Personalizar o banner social*

Você tem algumas outras opções:

* **[!UICONTROL Idioma]:** Na lista suspensa, escolha o idioma para traduzir o título e o subtítulo. Você também pode adicionar texto personalizado para idiomas diferentes.
* **[!UICONTROL Replicar]:** Clique nesse botão para replicar o título e o subtítulo em todos os idiomas.
* **[!UICONTROL Redefinir]:** Clique nesse botão para reverter para o título e o subtítulo originais.

Na página inicial do Aprendizado social, as informações fornecidas pelo administrador são exibidas como o cabeçalho da página.

<!--![](assets/banner-learner.png)-->

## Tendências {#trends}

As tendências de atividade social do aluno podem ser exibidas e rastreadas na guia Atividade na seção Tendências. Esses dados podem ser visualizados por diferentes períodos, como os últimos sete dias, o último mês, os últimos três meses e todos os tempos.

Os últimos sete dias são o valor padrão no filtro de data.

>[!NOTE]
>
>Os últimos sete dias são o valor padrão no filtro de data.

O primeiro visual fornece ao administrador as seguintes informações sobre o período selecionado no filtro de data:

1. **[!UICONTROL Novas postagens]**: exibe o número de novos posts criados no período de data. Também é exibido o número total de publicações para o período inteiro.
1. **[!UICONTROL Porcentagem de usuários ativos]**: exibe a porcentagem total de usuários ativos no aprendizado social em comparação com o número total de usuários disponíveis na conta.
1. **[!UICONTROL Novos painéis]**: exibe o número de novos painéis criados. Também é exibido o número total de painéis para o período inteiro.

O segundo visual é um gráfico de linhas que exibe a tendência do número de painéis ou publicações criados com base no período selecionado no filtro de data. Clique no filtro para exibir as diferentes opções de tempo, como últimos sete dias, último mês, últimos três meses e todo o tempo.

![](assets/trends.png)

*Gráfico de linhas exibindo a tendência*

## Habilidades {#skills}

Você pode ver todas as habilidades que foram usadas na plataforma de atividade social nesta seção. O administrador pode usar o campo de pesquisa para procurar uma habilidade que ainda não foi usada ao criar um painel e mapear SMEs para ele. Ao realizar isso, as SMEs recebiam uma notificação quando um painel era criado usando essa habilidade e podiam revisar a publicação como parte do fluxo de trabalho de curadoria manual.

Para uma conta com Aprendizado social desativado, nenhuma habilidade é exibida. A barra de pesquisa também está disponível para essas contas, para que o administrador tenha a funcionalidade de pesquisar uma habilidade e adicionar SMEs a ela.

O administrador pode exibir a Pontuação da atividade, o número de publicações, painéis, usuários e o nome das SMEs para cada habilidade usada ao criar um painel ou publicação.

<!--![](assets/modify-smes-2.png)-->

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Sl. Não.</b></p></td>
   <td>
    <p><b>Nome da coluna</b></p></td>
   <td>
    <p><b>Explicação</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Nome da habilidade</p></td>
   <td>
    <p>Exibe nomes de habilidades usadas no Aprendizado social.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Pontuação da Atividade</p></td>
   <td>
    <p>Exibe a soma dos pontos de atividade de todos os painéis que pertencem à habilidade.</p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Publicações</p></td>
   <td>
    <p>Exibe o número total de publicações criadas usando uma habilidade.</p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Placas</p></td>
   <td>
    <p>Exibe o número total de painéis criados usando uma habilidade.</p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>Usuários</p></td>
   <td>
    <p>Exibe o número total de alunos que usaram essa habilidade.</p></td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>PME</p></td>
   <td>
    <p>Exibe os 3 principais SMEs atuais para essa habilidade. O administrador pode adicionar ou modificar SMEs clicando no link.</p></td>
  </tr>
 </tbody>
</table>

## Domínio de habilidade {#skilldomain}

Com base nas habilidades usadas principalmente pelos usuários finais do Learning Manager, o Adobe Learning Manager categorizou uma lista de 25 domínios de habilidades que o sistema de curadoria automática usa para selecionar conteúdo. O administrador deve mapear as habilidades empresariais configuradas para os domínios de habilidade fornecidos pelo Prime. O mapeamento de habilidades pode ser feito na página de habilidades do administrador ao criar uma habilidade ou modificar uma habilidade existente. Para obter mais informações sobre como mapear ou adicionar uma habilidade, [clique aqui](skills-levels.md#Createaskillandalevel).

+++Lista de domínios de habilidades usada pelo sistema de curadoria do Learning Manager

1. Contabilidade
1. Analytics
1. Ética comercial
1. Direito comercial
1. Processo empresarial
1. Segurança do computador
1. Gerenciamento de relacionamento com o cliente
1. Design
1. Finanças
1. Gestão dos recursos humanos
1. Tecnologia da informação
1. Aprendizado
1. Gerenciamento
1. Marketing
1. Medicina
1. Produção e fabrico
1. Gerenciamento de qualidade
1. Vendas
1. Pesquisa científica e engenharia
1. Redes sociais
1. Habilidades pessoais
1. Gerenciamento estratégico
1. Gerenciamento da cadeia de fornecimento
1. Comunicação técnica
1. Segurança do local de trabalho

+++

## Especialistas no assunto (SMEs) {#subjectmatterexpertssmes}

**Especialistas no assunto** são pessoas que têm um conhecimento e experiência consideráveis em uma habilidade. Um **PME** desempenha uma função importante no aprendizado social quando o administrador define as configurações de curadoria como manuais ou quando o método de curadoria automática falha em selecionar o conteúdo. Somente os três SMEs principais são exibidos na coluna SMEs.

## Requisitos para ser uma PME {#requirementstobeansme}

O estatuto de PME só pode ser obtido através da obtenção de pontos de PME através de atividades no domínio da aprendizagem social. O administrador pode conceder pontos a um SME com base em sua experiência no nível de habilidade.

## Adicionar SMEs a uma habilidade {#addingsmestoaskill}

Para adicionar SMEs a uma habilidade, siga as etapas fornecidas:

1. Clique em **[!UICONTROL Adicionar SMEs]** ou **[!UICONTROL Modificar SMEs]**.

   ![](assets/add-smes-06.png)

   *Adicionar ou modificar SME*

1. Clique em **[!UICONTROL Opções avançadas]** na caixa de diálogo pop-up.

   ![](assets/advanced-optionssmes.png)

   *Exibir caixa de diálogo Opções avançadas*

1. Pesquise o usuário com experiência na habilidade. Depois que o usuário for encontrado, digite o número de pontos que deseja dar a ele na caixa **Adicionar pontos** caixa de entrada.

   Se o usuário já tiver pontos, o número de novos pontos fornecido ao usuário é adicionado ao número atual de pontos.

   Por padrão, para cada novo usuário do aprendizado social, o ponto atual é 0.

   ![](assets/advanced-options.png)

   *Adicionar pontos para um usuário*

1. Ao selecionar a opção **[!UICONTROL Habilitar Mínimo de SME Points]** , você pode definir um limite para o número mínimo de pontos que um usuário requer para ser exibido como SME na lista Principais SMEs. Depois que o valor do limiar é definido, as SMEs com pontos menores ou iguais ao valor mínimo de pontos necessário não são listadas nas listas de SME.

   Se a opção **[!UICONTROL Habilitar Mínimo de SME Points]** não for marcada, os três principais usuários com os pontos mais altos serão considerados as SMEs para essa habilidade em particular.

1. Clique em **[!UICONTROL Salvar]** para exibir as alterações que foram feitas.

## Sistema de pontos SME {#smepointsystem}

**Os SMEs recebem uma quantidade de pontos com base no seguinte:**

* 2 pontos são dados a um usuário cada vez que outro usuário anula uma postagem criada por ele.
* Dois pontos são dados a um usuário sempre que outro usuário aprovar seu comentário.
* Cinco pontos são dados a um aluno para responder a uma pergunta.
* Mais dois pontos são dados ao aluno sempre que a resposta fornecida recebe um voto favorável.

## Pontos de status de SME com base na atividade de curadoria {#smestatuspointsbasedoncurationactivity}

**Os SMEs também recebem uma quantidade de pontos com base nas atividades de curadoria para o seguinte:**

* Quando uma publicação é enviada para curadoria manual porque a curadoria automática não tem certeza se o conteúdo é relevante ou não, o SME ganha 5 pontos no envio da moderação.

## Baixar configurações {#downloadconfigurations}

<!--![](assets/download-config.png)-->

Para servidores corporativos, o administrador pode alterar o local de onde os alunos podem baixar o aplicativo de desktop para Windows e Mac.

![](assets/enterprise-servers.png)

*Alterar o local de download*

A URL do Servidor Enterprise deve ser hospedada publicamente.

## Atividades sociais para o plano de cobrança de Usuários Ativos Mensais {#socialactivitiesformonthlyactiveusersbillingplan}

Toda vez que um usuário cria um novo conselho social, publicação social ou comentário social, ele contaria como atividade válida a ser contada no **Usuário de Ativação Mensal**(MAU) se a conta seguir o modelo de faturamento MAU. Para obter mais informações, consulte [gerenciamento de faturamento](billing-management.md).

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como ativar o aprendizado social para alunos externos?

Entrada **[!UICONTROL Aprendizado social]** > **[!UICONTROL Configurações]**, na seção Configurações do escopo, ative a opção **[!UICONTROL Ativar para alunos externos]**. Na lista suspensa, escolha um perfil externo e defina o escopo do aprendizado para esse perfil.

![](assets/social-scope-external-users.png)

*Selecione a opção Ativar para alunos externos*
+++
