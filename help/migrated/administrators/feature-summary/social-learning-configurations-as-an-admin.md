---
description: Como administrador, você pode ativar, desativar e monitorar as atividades executadas no Aprendizado social. Uma vez que o recurso Aprendizado social estiver ativado, os alunos podem visualizá-lo e podem começar a participar do Aprendizado social.
jcr-language: en_us
title: Monitoramento e moderação do Aprendizado social como administrador
contentowner: kuppan
exl-id: 83f0b494-d129-4fdf-a204-b5efeaaa168a
source-git-commit: 6862dc1958a34a369f0e0e7218f28151a47beb3b
workflow-type: tm+mt
source-wordcount: '3756'
ht-degree: 62%

---

# Monitoramento e moderação do Aprendizado social como administrador

Como administrador, você pode ativar, desativar e monitorar as atividades executadas no Aprendizado social. Uma vez que o recurso Aprendizado social estiver ativado, os alunos podem visualizá-lo e podem começar a participar do Aprendizado social.

O aprendizado social permite que os alunos estudem em qualquer lugar e compartilhem conteúdo com seus colegas. Esse recurso permite que os alunos interajam, troquem ideias e colaborem, aprimorando sua experiência de aprendizado geral.

## Ativar e definir as configurações no aprendizado social {#enableandconfiguresettingsinsociallearning}

Para ativar e configurar o recurso Aprendizado social, faça o seguinte:

1. Clique em **[!UICONTROL Aprendizado social]** no painel de navegação esquerdo. Você é redirecionado para a página de atividade.
1. Habilitar **[!UICONTROL Aprendizado social]** recurso usando o **[!UICONTROL Habilitar]** na página Atividade, se estiver ativando-o pela primeira vez. Caso contrário, ele poderá ser ativado na **[!UICONTROL Configurações]** página.

   É exibida uma caixa de diálogo pop-up como a captura de tela abaixo.

   ![](assets/artboard-20-2x.png) ![](assets/enable-social-learningforthefirsttime.png)

   *Habilitar aprendizado social*

<!-- ![](assets/enable-social-learningfeatureinsettings.png) ![](assets/enable-social-learningdialog.png)-->

O administrador pode definir as configurações de Aprendizado social. As configurações incluem tipos de curações de conteúdo, como **[!UICONTROL Curadoria apenas manual]** e **[!UICONTROL Sem curadoria]**. As configurações de escopo podem ser definidas com escopo diferente, como o tipo de usuário (interno/externo) ou qualquer outro campo ativo presente na conta. O administrador pode definir o caminho do URL onde os alunos podem baixar o aplicativo de desktop Adobe Learning Manager.

### Curadoria de conteúdo {#contentcuration}

Visto que o aprendizado social é um aprendizado informal, sua funcionalidade é semelhante a outras plataformas de mídia social. Muitas vezes, as pessoas acham que as mídias sociais distraem porque frequentemente consomem conteúdo irrelevante que afeta sua produtividade. A moderação e a curadoria de conteúdo podem acabar com essa ideia.

**[!UICONTROL Curadoria apenas manual]** e **[!UICONTROL Sem curadoria]** Há duas opções de curadoria que podem ser selecionadas pelo administrador.

**[!UICONTROL Curadoria manual assistida automaticamente]:** O Learning Manager tem um mecanismo de curadoria automática baseado em inteligência artificial que pode descobrir de forma inteligente a essência do conteúdo de qualquer formato que possa ser fornecido posteriormente aos alunos desejados. Ele também pode aprovar ou rejeitar que um conteúdo seja publicado com base na pontuação de confiança fornecida.

Por exemplo, Adarsh é um aluno e achou um blog interessante, então ele o publicou na plataforma de aprendizado social do Adobe Learning Manager. A publicação é então enviada ao Mecanismo de curadoria de conteúdo viabilizado por IA, que prevê as habilidades presentes no conteúdo e as compara com as habilidades associadas ao conselho. Se alguma das habilidades corresponder, o conteúdo será publicado; caso contrário, será enviado para curadoria manual.

A pontuação mínima de confiança necessária para o lançamento é de 50%.

**[!UICONTROL Curadoria apenas manual]:** Para verificar a autenticidade do conteúdo antes que ele entre no ar, o administrador pode ativar a configuração de curadoria apenas manual. Depois que a configuração Curadoria manual somente é ativada, ela vai para os principais SMEs (máximo 3) para a curadoria. Com base na resposta média, a publicação é aprovada/rejeitada adequadamente. Se a resposta for maior ou igual a 50%, a publicação é publicada, e não é rejeitada. Para obter mais informações sobre SMEs, [clique aqui](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).


No novo escopo, ele/ela obtém pontos para as atividades nos painéis.

Nas seções de quadro de classificação social, um usuário pode ver todos os usuários do seu escopo juntamente com os usuários especiais.

Se você recebeu privilégios de usuário especial, você pode ver todos os usuários da conta no seu quadro de classificação, independentemente dos escopos dos usuários.

Se os utilizadores especiais se tornarem PME através da obtenção de pontos suficientes, **[!UICONTROL Principais especialistas no assunto]** no quadro de classificação social.

Aguarde 60 minutos para que as alterações tenham efeito.

### Configurações do escopo {#scopesettings}

Em Aprendizado social, o Escopo define os painéis visíveis, controlando assim a visibilidade do conteúdo. Se um usuário tiver um escopo, por exemplo, ***Fornecedor_A***, ele só pode ver painéis de discussão e postagens associadas que foram criadas por outras pessoas que pertencem ao mesmo escopo ***Fornecedor_A***.

Assim, os Administradores podem tratar um conjunto de usuários — como fornecedores, parceiros ou departamentos — como uma organização distinta.

Ative o aprendizado social e o quadro de classificação para usuários internos e externos.

Existem seções distintas para ativar usuários internos e externos.

**Ativar para Alunos internos**

Nesta seção, você pode escolher a característica do usuário para definir o escopo do aprendizado social para usuários internos. Usuários com as mesmas características **valor** compartilhe o mesmo espaço de aprendizado social.

Na guia **Característica do usuário** , escolha a opção desejada.

![](assets/choose-value-of-usercharacteristic.png)

*Selecione as características do usuário para definir o escopo*

Por padrão, a opção **[!UICONTROL Todos os usuários internos]** na lista suspensa Característica do usuário, a opção está sempre selecionada.

Você pode definir o escopo de usuários internos com base em seus campos ativos.

**Ativar para Alunos externos**

Para definir o escopo de aprendizado dos usuários externos, use um perfil externo. Alunos com o mesmo perfil externo compartilham um Espaço de aprendizado social comum.

![](assets/choose-an-externalprofile.png)

*Ativar escopo para alunos externos*

O escopo dos usuários externos é definido com base em seus perfis externos.

Por exemplo, na lista acima, se você ativar **[!UICONTROL Acme Corp]**, os painéis criados por alunos da Acme Corp ficarão visíveis para todos esses alunos. Se você desativar a opção **Henry Cavill**, os alunos não poderão ver nenhum painel criado por Henry Cavill.

O administrador pode definir o escopo de visibilidade do conteúdo com base no campo ativo exibido no campo **[!UICONTROL Característica do usuário]**.

Por exemplo, o administrador pode definir o escopo como **[!UICONTROL Tipo de usuário usuários (interno/externo]**). Ao definir o escopo como Tipo de usuário, o conteúdo compartilhado na plataforma de aprendizado social por qualquer aluno interno só é visível para outros alunos internos da organização e não para usuários externos e vice-versa.

Depois que o administrador seleciona uma Característica do usuário, ele pode limitar o recurso Aprendizado social a alunos e grupo de alunos marcando a caixa de seleção abaixo do campo Característica do usuário. Clique no campo de valor para selecionar o aluno ou grupos de aluno para os quais você deseja ativar o recurso Aprendizado social.

Por padrão, o escopo é definido pelo **[!UICONTROL Tipo de usuário]** que são alunos internos ou externos.

Se o campo ativo não contém nenhum valor, a lista suspensa do campo **[!UICONTROL Valor]** não será visível para o administrador.

<!--![](assets/scope-settings.png) ![](assets/scope-settings1-png.jpg)-->

Os usuários também podem publicar conteúdo usando o aplicativo de desktop da Adobe Learning Manager. Dependendo se você for usuário do Mac ou do Windows, clique nos links para baixar o aplicativo de desktop e siga as etapas fornecidas para instalá-lo no sistema. Se tiver quaisquer problemas na instalação, [clique aqui](../../kb/troubleshooting-issues-with-adobe-learning-manager-desktop-app.md).

### Configurações de download {#downloadconfigurations}

<!--![](assets/download-config.png)-->

Para servidores corporativos, o administrador pode alterar o local de onde os alunos podem fazer o download do aplicativo de desktop para Windows e Mac.

![](assets/enterprise-servers.png)

*Alterar o local de download*

O URL do servidor corporativo deve estar hospedado publicamente.

### Permissões de criação de painel {#permission}

Para restringir a criação de painéis por todos os alunos e moderar os painéis de forma eficaz, um administrador pode conceder permissões para criar painéis para um grupo de usuários seleto.

![](assets/grant-permissiontocreateboards.png)

*Definir permissões para criar um painel*

A opção **[!UICONTROL Todos os alunos]** está ativada por padrão.

**[!UICONTROL Todos os alunos]:** Se você escolher essa opção, todos os usuários internos e externos poderão criar painéis.

**Um grupo de alunos:** se essa opção for selecionada, apenas usuários com permissão para criar painéis verão o link **[!UICONTROL Criar um novo painel]** no Aprendizado social. Escolha o grupo de usuários que deve receber permissão para criar um painel. Você também pode adicionar grupos de usuários gerados automaticamente e personalizados.

<!--![](assets/grant-permissiontoausergroup.png)-->

Usuários no mesmo escopo podem ver apenas o painel. O link **[!UICONTROL Criar um novo painel]** permanece invisível para usuários sem permissão.

Aguarde 60 minutos para que as alterações tenham efeito.

## Usuários especiais {#privilege}

Um administrador pode conceder privilégios especiais a um grupo de usuários, definindo quais membros do grupo podem participar em todos os painéis. Todas as restrições definidas na seção Configurações de escopo são ignoradas pelos grupo de usuários especiais.

O grupo de usuários pode ser gerado automaticamente ou personalizado.

Um usuário que recebeu esse privilégio tem acesso a todos os painéis, exceto aos **painéis privados**.

![](assets/special-users.png)

*Conceder privilégios especiais*

Quando o administrador seleciona um grupo de usuários, por padrão, todos os usuários do grupo podem acessar todos os painéis, independentemente do escopo do usuário. Qualquer usuário com esses privilégios elevados pode visualizar e participar em todos os painéis internos e externos.

Os usuários especiais recebem solicitações de curadoria em todos os escopos se tiverem pontos de SME suficientes para essa habilidade.

Se o usuário não tiver os pontos obrigatórios de SME, os privilégios de administração são enviados para os três principais SMEs dessa habilidade.

No novo escopo, ele/ela obtém pontos para as atividades nos painéis.

Nas seções de quadro de classificação social, um usuário pode ver todos os usuários do seu escopo juntamente com os usuários especiais.

Se você recebeu privilégios de usuário especial, você pode ver todos os usuários da conta no seu quadro de classificação, independentemente dos escopos dos usuários.

Se os utilizadores especiais se tornarem PME através da obtenção de pontos suficientes, **[!UICONTROL Principais especialistas no assunto]** no quadro de classificação social.

Aguarde 60 minutos para que as alterações tenham efeito.

### Personalizar o banner social {#customize-social-banner}

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

### Exibição Aprendizado Social

Um administrador pode selecionar a exibição de aprendizado social nas seguintes configurações:

* Exibição de publicação - Selecionar essa opção exibe as publicações individuais de todos os painéis.
* Exibição do quadro: selecionar essa opção exibe todos os painéis disponíveis.

## Curadoria automática de conteúdo {#autocuration}

A moderação manual de conteúdos é propensa a erros e consome muito tempo. Além disso, esse processo não é escalável e não atende um volume grande de atividades sociais. Dessa forma, a curadoria de conteúdo torna-se automaticamente essencial no atendimento a muitos usuários socialmente ativos.

No Learning Manager, você tem a opção de selecionar conteúdos automaticamente. Após o administrador mapear uma habilidade com as habilidades predefinidas, um mecanismo com IA gerencia o mapeamento de cada trabalho com as habilidades predefinidas. Para obter mais informações, consulte [Mapeamento de domínio de habilidades](curation-skills.md).

Os tipos de conteúdo a seguir são permitidos na curadoria automática:

* PDF
* Arquivos de áudio e vídeo
* Apresentações - PPT ou PPTX
* Documentos - .doc, .docx

Um administrador pode ativar a opção de organizar conteúdo automaticamente no Admin Console.

1. No painel esquerdo do Admin Console, clique em **[!UICONTROL Aprendizado social]**.
1. Na página, clique na guia **[!UICONTROL Configurações]**.
1. Ative a opção **[!UICONTROL Curadoria manual autoassistida]**.

   ![](assets/auto-curation.png)

   *Selecione a opção Curadoria manual assistida automaticamente*

Assim que um usuário carregar um conteúdo em um painel, um algoritmo baseado em IA varre o texto do conteúdo e o envia para o mecanismo de curadoria. O mecanismo de curadoria tenta localizar as habilidades presentes no conteúdo.

As habilidades previstas do conteúdo carregado são correspondidas com as do painel em que o conteúdo foi carregado.  Se alguma habilidade corresponder a uma pontuação de confiança de mais de 50% da habilidade do quadro, o conteúdo será publicado no quadro. Se a pontuação de confiança for inferior a 50%, o conteúdo é enviado para curadoria manual.

Sempre que um conteúdo passa por curadoria automática, o usuário recebe uma notificação de que o conteúdo está disponível no painel para o qual foi enviado.

![](assets/only-ai-based.png)

*Fluxograma de configurações de curadoria*

É recomendável que o administrador adicione SMEs para habilidades se a Curadoria manual somente estiver ativada. O administrador pode adicionar SMEs fornecendo anteriormente pontos de SME aos usuários com experiência em uma habilidade. Para saber mais sobre como fornecer pontos para as PME,  [clique aqui](social-learning-configurations-as-an-admin.md#SubjectMatterExpertsSMEs).

**Sem curadoria:** Todas as publicações do aluno são publicadas automaticamente sem qualquer moderação de conteúdo.

<!--![](assets/artboard-6-2x.png)-->

## Perguntas frequentes sobre curadoria automática de conteúdo {#faq-auto-curation}

+++Quanto tempo uma PME tem para organizar uma publicação?

Uma SME demora no mínimo 24 horas para fazer a curadoria de uma publicação. Devido a diferenças de fuso horário, ele pode ser aumentado para 47 horas.

+++

+++Vai para o próximo conjunto de três PMEs se todas as três estiverem disponíveis? São sempre três as SMEs que estão envolvidas?

O pedido de curadoria vai para o topo das SMEs no primeiro dia. Se não responderem, o pedido vai para as três próximas SMEs no dia seguinte.

Se as três novas SMEs não responderem, o pedido vai para os moderadores do fórum.

Se os moderadores do painel não responderem, a solicitação será aprovada automaticamente.

+++

+++Se duas SMEs fizerem curadoria e uma não, o pedido vai para a quarta SME ou o pedido toma a média, seja qual for a primeira rodada de SMEs que classifica a publicação?

É necessária uma taxa de aprovação de 50% para aprovar a publicação. Da mesma forma, a taxa de rejeição de 50% é usada para rejeitar a publicação. A cada aprovação feita por uma SME, avalia-se se atingiu 50%.

Se não atingir 50% após um dia, será enviado para o próximo conjunto de SMEs, expirando os pedidos anteriores de curadoria não atendidos.

Por exemplo, no primeiro dia, o pedido de curadoria é enviado a três SMEs; e um deles o aprova, dois não responderam. No dia seguinte, o pedido de curadoria vai para o próximo conjunto de três SMEs; neste momento, existem quatro SMEs ativas no total. Pelo menos dois SEMs devem aprovar o pedido para que a curadoria seja aprovada.(No caso de 2 aprovações e 2 rejeições, o que atingir os 50% iniciais será obtido.)

+++

+++Pelo o que vejo, um “Moderador” é atribuído apenas (e não é obrigatório) quando alguém cria um novo painel - Qual é o caso de uso para um Aluno atribuir um “Moderador” a um painel se as SMEs forem atribuídas à habilidade associada a um painel?

As responsabilidades de um moderador do Fórum Social são as seguintes:

* Capacidade de editar o nome do fórum, a descrição, as configurações de visibilidade do fórum e outras configurações.
* Capacidade de excluir uma publicaçaõ no fórum caso ela não seja adequada ao público-alvo.
* O moderador recebe notificações de “Denunciar abuso” para o painel.
* O moderador recebe solicitações de curadoria se nenhuma SME estiver presente no fórum.

+++

+++Nossa equipe de treinamento estará adicionando / monitorando as habilidades associadas ao nível de habilidade, bem como as SMEs atribuídas às habilidades.

As SMEs são adicionadas/atribuídas com base na habilidade, e não no nível da habilidade. Isto é o que foi projetado.

+++

+++Qual é a diferença entre um “moderador” de aprendizado social e um “SME” de aprendizado social?

**Moderadores:** Proprietários secundários do fórum. Eles são adicionados pelos criadores durante a criação do fórum para que eles possam controlar o fórum na ausência do criador. Por padrão, o criador do fórum é o moderador.

**PME:** Especialistas no assunto são especialistas em habilidades específicas. O administrador pode atribuir SMEs a uma determinada habilidade para fazer curadoria do conteúdo dessa habilidade. As SMEs recebem os pedidos de curadoria dos fórum ligados às suas habilidades. Os alunos também podem se tornar SMEs ganhando pontos de SME.

+++

+++Se houver duas ou três SMEs atribuídas a uma habilidade: a aprovação ou rejeição de uma pós-aprendizagem social depende de todas as curadorias das SMEs ou de quem fazer a curadoria primeiro?

É necessária uma taxa de aprovação de 50% para aprovar a publicação. Da mesma forma, a taxa de rejeição de 50% é usada para rejeitar a publicação. A cada aprovação feita por uma SME, avalia-se se atingiu 50%.

Se não atingir 50% após um dia, será enviado para o próximo conjunto de SMEs, expirando os pedidos anteriores de curadoria não atendidos.

+++

## Tendências {#trends}

As tendências de atividade social do aluno podem ser exibidas e rastreadas na guia Atividade na seção Tendências. Esses dados podem ser exibidos por períodos diferentes como últimos sete dias, último mês, últimos três meses e sempre.

Últimos sete dias é o valor padrão no filtro de data.

>[!NOTE]
>
>Últimos sete dias é o valor padrão no filtro de data.

A primeira vista fornece ao administrador as seguintes informações do período selecionado no filtro de datas:

1. **[!UICONTROL Novas publicações:]** exibe o número de publicações novas criadas dentro do período de data. Também é exibido o número total de publicações durante todo o período.
1. **[!UICONTROL Porcentagem de usuários ativos]**: exibe a porcentagem total de usuários ativos no aprendizado social em comparação ao número total de usuários disponível na conta.
1. **[!UICONTROL Novos painéis]**: exibe o número de novos painéis criados. Também é exibido o número total de painéis para o período inteiro.

A segunda vista é um gráfico de linha que exibe a tendência do número de painéis ou publicações criados com base no período selecionado no filtro de datas. Clique no filtro para exibir as diferentes opções de tempo como últimos sete dias, último mês, últimos três meses e sempre.

![](assets/trends.png)

*Gráfico de linhas exibindo a tendência*

## Habilidades {#skills}

Nesta seção, você pode visualizar todas as habilidades que foram usadas na plataforma de atividade social. O administrador pode usar o campo de pesquisa para procurar uma habilidade que ainda não foi usada ao criar um painel e ao mapear SMEs para tal habilidade. Ao fazer isso, os SMEs recebem uma notificação quando um painel é criado usando esta habilidades e podem analisar a publicação como parte do fluxo de trabalho de curadoria manual.

Para uma conta com o aprendizado social desativado, não é exibida nenhuma habilidade. A barra de pesquisa está disponível para essas contas também, de modo que o administrador tem a funcionalidade para pesquisar por uma habilidade e adicionar SMEs a ela.

O administrador pode visualizar a pontuação de atividade, o número de publicações, os painéis, os usuários e o nome de SMEs de cada habilidade que foi usada ao criar um painel ou uma publicação.

<!--![](assets/modify-smes-2.png)-->

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Letra Nº</b></p></td>
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
    <p>Exibe os nomes das habilidades usadas no aprendizado social.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Pontuação de atividade</p></td>
   <td>
    <p>Exibe a soma de pontos de atividades de todos os painéis pertencentes à habilidade.</p></td>
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
    <p>Painéis</p></td>
   <td>
    <p>Indica o número total de painéis criados usando uma habilidade.</p></td>
  </tr>
  <tr>
   <td>
    <p>5</p></td>
   <td>
    <p>Usuários</p></td>
   <td>
    <p>Exibe o número total de alunos que utilizaram tal habilidade.</p></td>
  </tr>
  <tr>
   <td>
    <p>6</p></td>
   <td>
    <p>SMEs</p></td>
   <td>
    <p>Exibe os três SMEs principais atuais de tal habilidade. O administrador pode adicionar ou modificar os SMEs clicando no link.</p></td>
  </tr>
 </tbody>
</table>

## Domínio de habilidade {#skilldomain}

Com base nas habilidades mais usadas pelos usuários finais do Learning Manager, a Adobe Learning Manager categorizou uma lista de 25 domínios de habilidades que o sistema de curadoria automática usa para selecionar conteúdo. O administrador deve mapear as habilidades empresariais configuradas para os domínios de habilidade fornecidos pelo Prime. O mapeamento de habilidades pode ser feito na página de habilidades do administrador ao criar uma habilidade ou modificar uma habilidade existente. Para obter mais informações sobre como mapear ou adicionar uma habilidade, [clique aqui](skills-levels.md#Createaskillandalevel).

+++Lista de domínios de habilidades usada pelo sistema de curadoria do Learning Manager

1. Contabilidade
1. Análise
1. Ética empresarial
1. Direito empresarial
1. Processo empresarial
1. Segurança da computação
1. Gerenciamento de relacionamento com o cliente
1. Design
1. Finanças
1. Gestão de recursos humanos
1. Tecnologia da informação
1. Aprendizado
1. Gestão
1. Marketing
1. Medicina
1. Produção e fabricação
1. Gestão da qualidade
1. Vendas
1. Pesquisa científica e engenharia
1. Redes sociais
1. Habilidades interpessoais
1. Gestão estratégica
1. Gestão de cadeia de suprimento
1. Comunicação técnica
1. Segurança no trabalho

+++

## Especialistas no assunto (SMEs) {#subjectmatterexpertssmes}

**Especialistas no assunto** são pessoas que têm um conhecimento e experiência consideráveis em uma habilidade. Um **PME** desempenha uma função importante no aprendizado social quando o administrador define as configurações de curadoria como manuais ou quando o método de curadoria automática falha em selecionar o conteúdo. Apenas os três principais SMEs são exibidos na coluna SMEs.

## Requisitos para ser um SME {#requirementstobeansme}

O status de SME pode ser obtido apenas ao receber muitos pontos de SME com as atividades no Aprendizado social. O administrador pode conceder pontos a um SME com base em sua experiência no nível de habilidade.

## Adicionar SMEs a uma habilidade {#addingsmestoaskill}

Para adicionar SMEs a uma habilidade, siga as etapas fornecidas:

1. Clique em **[!UICONTROL Adicionar SMEs]** ou **[!UICONTROL Modificar SMEs]**.

   ![](assets/add-smes-06.png)

   *Adicionar ou modificar SME*

1. Clique em **[!UICONTROL Opções avançadas]** na caixa de diálogo pop-up.

   ![](assets/advanced-optionssmes.png)

   *Exibir caixa de diálogo Opções avançadas*

1. Pesquise pelo usuário com experiência na habilidade. Depois que o usuário for encontrado, digite o número de pontos que deseja dar a ele na caixa **Adicionar pontos** caixa de entrada.

   Se o usuário já tiver pontos, os novos pontos dados ao usuário serão adicionados ao número atual de pontos.

   Por padrão, cada novo usuário do aprendizado social tem 0 ponto.

   ![](assets/advanced-options.png)

   *Adicionar pontos para um usuário*

1. Ao marcar a caixa de seleção **[!UICONTROL Ativar pontos mínimos de SME]**, você pode definir um limite para o número mínimo de pontos que um usuário deve ter para ser exibido como SME na lista de principais SMEs. Depois que o limite mínimo é definido, os SMEs com pontos iguais ou inferiores ao valor mínimo necessário não são exibidos na lista de SMEs.

   Se a opção **[!UICONTROL Habilitar Mínimo de SME Points]** não for marcada, os três principais usuários com os pontos mais altos serão considerados as SMEs para essa habilidade em particular.

1. Clique em **[!UICONTROL Salvar]** para exibir as alterações que foram feitas.

## Sistema de pontos do SME {#smepointsystem}

**Os SMEs recebem uma quantidade de pontos com base no seguinte:**

* O usuário recebe 2 pontos cada vez que outro usuário aprova uma publicação criada por ele.
* O usuário recebe 2 pontos cada vez que outro usuário aprova um comentário.
* O aluno recebe 5 pontos por responder a uma pergunta.
* O aluno recebe mais 2 pontos cada vez que a resposta fornecida recebe uma aprovação.

## Pontos de status SME com base na atividade de administração {#smestatuspointsbasedoncurationactivity}

**Os SMEs também recebem uma quantidade de pontos com base nas atividades de curadoria para o seguinte:**

* Quando uma publicação é enviada para curadoria manual porque a curadoria automática não tem certeza se o conteúdo é relevante ou não, o SME ganha 5 pontos pelo envio para moderação.

## Plano de faturamento das atividades sociais para usuários ativos mensalmente {#socialactivitiesformonthlyactiveusersbillingplan}

Toda vez que um usuário cria um novo conselho social, publicação social ou comentário social, ele contaria como atividade válida a ser contada no **Usuário de Ativação Mensal**(MAU) se a conta seguir o modelo de faturamento MAU. Para obter mais informações, consulte o [gerenciamento de faturamento](billing-management.md).

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como ativar o aprendizado social para alunos externos?

Entrada **[!UICONTROL Aprendizado social]** > **[!UICONTROL Configurações]**, na seção Configurações do escopo, ative a opção **[!UICONTROL Ativar para alunos externos]**. Na lista suspensa, escolha um perfil externo e defina o escopo do aprendizado para esse perfil.

![](assets/social-scope-external-users.png)

*Selecione a opção Ativar para alunos externos*
+++
