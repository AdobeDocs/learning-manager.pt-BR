---
jcr-language: en_us
title: Página inicial do aluno
description: Depois que o administrador ativa o layout imersivo, o aluno, após fazer logon no aplicativo, é recebido com uma interface de usuário completamente reformulada.
contentowner: saghosh
exl-id: 71b495c7-a6c8-4e6e-9f00-ec93d7b483ad
source-git-commit: 92ddeb8ad58d78ac139e7106bf22e7f1ff45b5b0
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 39%

---

# Página inicial do aluno

## Visão geral {#overview}

Depois que o administrador ativa o layout imersivo, o aluno é recebido com uma interface de usuário completamente reformulada ao fazer logon no aplicativo.

>[!NOTE]
>
>O navegador IE11 não é compatível com o layout Imersivo.

## Nova interface do usuário do aluno para layout imersivo

>[!IMPORTANT]
>
>Lançaremos a nova interface do usuário do aluno em fases.

Atualizamos a interface do aluno com um design mais elegante e atualizado. A nova interface tem como objetivo fornecer uma experiência de usuário consistente nas páginas de aterrissagem da **[!UICONTROL Página inicial do aluno]**, do **[!UICONTROL Meu aprendizado]**, do **[!UICONTROL Catálogo]** e da **[!UICONTROL Visão geral do curso]**. Os novos elementos visuais seguem os estilos de design atuais, tornando o produto mais fácil de usar e atraente. Esta atualização inclui uma nova manchete, um painel lateral e widgets contemporâneos.

>[!NOTE]
>
>A nova interface de usuário aplica-se somente ao layout Imersivo. O aplicativo/Web para dispositivos móveis ainda não é compatível com essas alterações e as atualizará em uma versão futura.

![](assets/old-ui.png)
_Interface de Usuário Antiga_

![](assets/home-page-new.jpg)
_Nova Interface De Usuário_

### Página inicial

A página inicial tem um novo design com um painel lateral aprimorado, cabeçalho superior, cartões de curso aprimorados e widgets.

![](assets/new-ui-homepage.png)
_Nova página inicial_

### Página Catálogo

As páginas do catálogo têm uma nova aparência com filtros organizados e cartões de curso aprimorados para fornecer uma experiência melhor ao usuário.

![](assets/catalog.jpg)
_Página do catálogo_

### Página Visão geral do curso

A página de visão geral do curso tem uma nova aparência com mais detalhes sobre o curso. Esta página ajuda os alunos a obter todas as informações de que precisam.

![](assets/course-overview.jpg)
_Página de visão geral do curso_

### Cartões do curso

Os cartões de curso também apresentam um layout reformulado para exibir detalhes com mais eficiência. Cartões de curso renovados destacam os metadados relevantes necessários para a inscrição. Esses metadados incluem datas de publicação ou vencimento, classificações e descrições corretas junto com seus autores ou provedores.

![](assets/old-course-cards.png)
_Cartão de curso antigo_

![](assets/new-course-card.jpg)
_Novo cartão do curso_

Para os cursos importados do **LinkedIn** e da plataforma **Go1**, os cartões de curso exibirão as datas de publicação originais do **LinkedIn** e do **Go1**. Você também pode exibir essas datas de publicação específicas na interface do usuário.

### Barra lateral e barra de pesquisa

A barra lateral é atualizada com novos elementos de interface para obter uma aparência mais limpa. A nova barra de pesquisa não tem nenhum botão de pesquisa, dando uma aparência mais limpa. Os alunos podem digitar uma palavra-chave e pressionar enter para iniciar a pesquisa ou selecionar resultados abaixo da barra de pesquisa.

![](assets/side-bar.png)
_Barra lateral e barra de pesquisa_

### Manchete {#masthead}

Apresenta um carrossel de imagens ou vídeo com um URL incorporado. O [administrador pode carregar qualquer ativo de imagem ou vídeo](../../administrators/feature-summary/announcements.md#masthead) como um manchete e definir sua visibilidade para um grupo de alunos.

![](assets/learner-masthead.png)

*Exibir manchete*

### Lista do meu aprendizado {#mylearninglist}

Exibe o treinamento que o aluno fez. Esses treinamentos são exibidos como cartões alinhados horizontalmente. Você pode clicar no botão direito ou esquerdo para navegar pelos cursos.

![](assets/learner-my-learning-list.png)

*Exibir minha lista de aprendizado*

Você também pode deslizar para a esquerda e para a direita para navegar pela lista.

Para retomar um curso, clique em **[!UICONTROL Continuar]** em um cartão e o reprodutor iniciará.

A aparência dos ícones em cada cartão de treinamento é habilitada/desabilitada pelo administrador por meio do aplicativo Admin (**Configurações** > **Geral** > **Habilitar ícones do cartão de treinamento**).

**Adicionar à Minha lista de aprendizado**

Se você passar o mouse em qualquer cartão do curso em **Recomendado com base em suas áreas de interesse** e **Recomendado com base em listas de atividades entre pares**, você verá uma opção para adicionar o curso à **Minha lista de aprendizado**. Clique em **[!UICONTROL +]** no cartão do curso e o curso será adicionado à **Minha lista de aprendizado**.

![](assets/add-my-learning.png)

*Adicionar à Minha lista de aprendizado*

## Escolher níveis de habilidade {#chooseskilllevels}

Como aluno, você pode filtrar o catálogo do curso de acordo com estes níveis:

* Iniciante
* Intermediário
* Avançado

Escolha uma opção e você poderá ver o catálogo do curso de acordo com a seleção.

![](assets/skill-levels.png)

*Selecionar níveis de habilidade*

## Widget de painel de conformidade

O widget do painel de conformidade permite que os alunos filtrem cursos/caminhos de aprendizado/certificações que têm prazos de conclusão futuros usando o rótulo Conformidade. Este recurso está disponível em todos os aplicativos do aluno, incluindo o aplicativo ALM Teams, AEM, o aplicativo para dispositivos móveis, o aplicativo imersivo e o aplicativo SF.

![](assets/compliance-status-learner.png)
_Widget de painel de conformidade_

## Calendário {#calendar}

Mostra as suas sessões agendadas e treinamento. Navegue no calendário para ver o treinamento para os meses subsequentes.

![](assets/learner-calendar.png)

*Exibir calendário para sessões agendadas*

O widget Calendário tem os seguintes recursos. Você pode exibir:

* Treinamento por mês. Role para a esquerda ou direita.
* Próxima sala de aula ou sala de aula virtual disponível para você se inscrever.
* Próxima sala de aula ou treinamento em sala de aula virtual em que você se inscreveu.
* Suas sessões de sala de aula virtual ou sala de aula concluída
* Treinamento em sala de aula virtual ou sala de aula aprovada pelo gerente.

Você pode aplicar o filtro **[!UICONTROL Exibir somente sessões inscritas]** para exibir somente as sessões inscritas no calendário.


## Feed social {#socialfeed}

![](assets/social-feed.png)

*Exibir feed social*

Veja o que outros usuários estão falando.

O widget resume a atividade por um período. Ele:

* Exibe os usuários ativos e as atividades dos usuários que estão em seu escopo ou grupo.
* Exibe postagens feitas nas últimas duas semanas.

## Habilidades de perfil {#profileskills}

As habilidades de perfil são usadas para as recomendações do curso. Se o administrador atribuir uma habilidade a um usuário ou grupo de usuários, a habilidade será adicionada às habilidades de perfil do aluno. Se o aluno adicionar uma habilidade ao seu perfil, todos os níveis da habilidade serão adicionados às habilidades de perfil do aluno. Quando um aluno passa o mouse sobre uma habilidade, ele/ela pode ver o nome da habilidade, o método de adição da habilidade, o nível, a porcentagem de conclusão da habilidade e os créditos.

![](assets/profile-skills.png)
*Exibir habilidades de perfil*

Se um aluno se inscrever em um curso, somente as habilidades externas que são baseadas em uma pontuação são adicionadas às habilidades de perfil. Além disso, um aluno pode pesquisar, selecionar e adicionar habilidades externas ao seu perfil.Se um aluno fez logon no aplicativo do aluno pela primeira vez e se as habilidades do aluno já estiverem presentes, as habilidades serão exibidas em Meu perfil.

## Recomendação baseada na sua área de interesse {#recommendationbasedonyourareaofinterest}

Exibe treinamento com base na área de interesse escolhida. A recomendação é orientada por um algoritmo de Aprendizado de Máquina.

![](assets/learner-recommendation.png)

*Exibir cursos recomendados*

Para obter mais recomendações direcionadas, você pode atualizar suas habilidades clicando em **Exibir/Atualizar**.

Depois de adicionar uma habilidade, as recomendações futuras se tornarão mais direcionadas e focadas de acordo com as suas preferências.

Se o administrador desabilitou a opção **Explorar habilidades**, você poderá adicionar interesse às suas habilidades.

Os cursos recomendados são exibidos como cartões. Ao passar o mouse sobre um cartão, você pode ver mais detalhes do curso.

A terminologia do produto também é suportada.

**Habilidades alinhadas ao setor**

Você poderá ver o gráfico de habilidades da rede se o administrador tiver ativado a opção **Alinhado ao setor** no aplicativo do administrador.

Essas habilidades só podem ser visualizadas quando o administrador definir o tipo de treinamento para Alinhado ao setor.

Na visualização do Mapa de habilidades, você pode procurar uma habilidade ou habilidades e adicioná-las.

![](assets/learner-add-industry-skills.png)

*Visualização do mapa de habilidades*

Habilite a opção **Mostrar habilidades para as quais os treinamentos estão presentes na minha conta**, se você deseja exibir todas as habilidades que estão na sua conta.

Depois de adicionar uma habilidade, você pode ver o gráfico de força direcionada com a habilidade selecionada como o vértice principal e as habilidades associadas como vértices menores.

As habilidades escolhidas também são exibidas na seção **Habilidades selecionadas**.

![](assets/learner-add-industry-skills-1.png)

*Habilidades selecionadas*

Para adicionar as habilidades, clique em **[!UICONTROL Adicionar]**.

## Recomendação baseada na atividade entre pares {#recommendationbasedonpeeractivity}

Exibe treinamento com base no que seus colegas estão fazendo. Isso é controlado novamente por um algoritmo de aprendizado de máquina. As recomendações são baseadas em treinamento para alunos personalizados e alinhados ao setor.
