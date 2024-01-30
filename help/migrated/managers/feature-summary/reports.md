---
description: Criar e gerenciar relatórios para Gerentes.
jcr-language: en_us
title: Relatórios
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 63%

---



# Relatórios

Criar e gerenciar relatórios para Gerentes.

O Adobe Learning Manager lhe permite criar relatórios variados para acompanhar, monitorar e gerenciar as atividades do Aluno. As atividades dos Alunos são acompanhadas e capturadas automaticamente no banco de dados. Os relatórios de Gerente e Administrador são gerados a partir do banco de dados.

## Visão geral {#overview}

O processo de geração de relatórios é o mesmo para o Administrador e Gerente. Os Gerentes podem ver os relatórios que correspondem aos seus subordinados enquanto que o Administrador pode vir todos os relatórios no âmbito da organização.

Os relatórios são agregados em um painel. Um relatório deve existir dentro de um painel. A **Painel padrão** existe por padrão na página relatórios. Qualquer relatório adicionado por você é movido para este painel padrão. Para adicionar relatórios a painéis de controle individuais, use a seta suspensa e escolha Adicionar relatório. Para obter mais informações sobre como criar painéis, consulte a seção Painéis nesta página.

## Painéis do gerente {#manager-dashboards}

Um gerente pode exibir informações sobre sua equipe direta ou indireta, como um resumo.

O gerente pode filtrar o relatório de acordo com intervalos como, trimestre, este mês, últimos três meses inteiros e últimos 12 meses inteiros.

## Resumo do aprendizado {#learningsummary}

![](assets/manager-learningsummary.png)

*Exibir resumo de aprendizado*

![](assets/manager-dashboard.jpg)

*Filtrar resumo de aprendizado por data*

## Painel de conformidade {#compliancedashboard}

Veja a conformidade de sua equipe e qual membro está próximo da não conformidade. Escolha os objetos de aprendizado e veja o status de cada um.

![](assets/compliance-dashboard.png)

*Exibir painel de conformidade*

## Status das habilidades {#skillsstatus}

Veja a porcentagem de alunos para cada habilidade. Escolha no máximo cinco habilidades para as quais deseja ver as habilidades dos alunos. A visualização está na forma de um gráfico de barras empilhadas. Ao passar o mouse sobre cada barra, você pode ver a divisão do status dessa habilidade.

![](assets/manager-skills-status.png)

*Exibir o status das habilidades de um aluno*

## Rastreador de habilidades {#skilstracker}

Veja uma projeção da conclusão de habilidades de uma equipe. Escolha a porcentagem de conclusão prevista e a data de uma habilidade.

Com base em dados históricos, você pode ver uma representação gráfica da projeção de conclusão de habilidade na data selecionada.

![](assets/historical-data.png)

*Exibir projeção de conclusão de habilidade*

## Criar relatórios {#creatingreports}

1. Clique em Relatórios no painel esquerdo. A página de resumo de relatório será exibida.\
   **Observação**
Por padrão, pelo menos três relatórios de amostra aparecem na página de resumo de relatório. Você somente pode ver esses relatórios de amostra para obter uma ideia sobre como é possível criar e personalizar os mesmos.

1. Na página de resumo de relatório, clique em Adicionar. A caixa de diálogo de criação de relatórios será exibida.
1. Clique em Salvar para concluir a criação de um relatório. Um relatório de amostra é mostrado abaixo como referência.

![](assets/add-report.png)

*Caixa de diálogo Adicionar relatório*

Em Tipo de relatório, você pode escolher um conjunto predefinido de relatórios ou escolher personalizado. Você pode exibir os seguintes relatórios como parte do conjunto predefinido de relatórios:

* Conhecimentos atribuídos e alcançados
* Cursos inscritos e concluídos
* Eficácia dos cursos
* Programas de aprendizado inscritos e concluídos
* Tempo gasto no aprendizado por curso
* Tempo gasto no aprendizado por trimestre

Você pode usar os tipos de relatórios acima mencionados para gerar relatórios de 300 ou mais variações.

Nome do Relatório Digite um título para o relatório.

**Eixo Y principal** Escolha o primeiro critério/critério principal para o relatório nas opções suspensas. Para alguns dos critérios selecionados, você tem a opção de escolher um ou vários estados na caixa suspensa Estados adjacentes. Por exemplo, para um critério principal das estatísticas de inscrição do curso, os estados podem ser concluídos, incompletos, inscritos e assim por diante. Os dados da faixa principal são representados na forma de gráficos de barra no relatório.

**Eixo Y secundário** Escolha o critério/intervalo do eixo Y secundário para o relatório nas opções suspensas. Por exemplo, na opção de inscrição no programa de aprendizado, escolha um ou vários estados na lista suspensa Estados adjacentes. Os dados da faixa secundária são representados na forma de gráficos de linha no relatório.

**Eixo X** Escolha os critérios apropriados do eixo x para o relatório nas opções suspensas. Se o eixo X for selecionado como uma data, então uma opção para agrupar seu critério do eixo X por dia, mês, trimestre e ano está disponível.

**Data** Escolha a opção apropriada na lista suspensa. Opções: último um mês, trimestre, ano, trimestre até a data (últimos 90 dias), ano até a data (últimos 365 dias) e a faixa de datas. Se você escolher faixa de datas, forneça a data De e Para como se segue:

**De** Escolha a data inicial a partir da qual você gostaria de ver o relatório.

**Para** Escolha a data final para o relatório.

## Filtros {#filters}

Os filtros são exibidos na caixa de diálogo Adicionar na parte inferior com base nos tipos de relatórios que você escolheu. Alguns filtros importantes são mencionados abaixo.

**Gerente** Você pode escolher qualquer um dos gerentes com base na hierarquia. Para alguns gerentes, pode haver gerentes subordinados e vários funcionários se comunicando com cada gerente subordinado.

**Perfil** Escolha a designação para seu funcionário. Seria útil ver os relatórios dos funcionários com base em seu perfil/designação. Por exemplo, cientista da computação, engenheiro, e assim por diante.

**Grupo de usuários** Escolha o grupo de usuários com base no qual você deseja filtrar os relatórios. O Learning Manager pega os grupos de usuário definidos para sua conta a partir do recurso Usuários.

**Curso** Você pode filtrar o relatório com base em qualquer curso ao escolher o mesmo na lista suspensa.

![](assets/sample-report-admin.png)

*Exibir gráfico de cursos inscritos e concluídos*

>[!NOTE]
>
>Acima da legenda do gráfico, você pode exibir uma caixa de zoom. Você pode mover o cursor do mouse sobre ela, clicar e arrastar a barra transversal sobre qualquer parte da área da caixa de zoom na qual deseja aplicar o zoom.

Você pode exibir os valores do eixo Y secundário na forma de uma linha entre as barras no gráfico. Por exemplo, na amostra acima, você pode ver os valores para a Eficiência na linha cinza através do gráfico.

## Relatórios de grupo de usuários {#user-group-reporting}

Acompanhe o desempenho de grupos, tal coo departamento, parceiros externos e funções, em comparação com outros grupos ou em relação a outros objetivos de aprendizado.

### Grupos de usuários {#usergroups}

Para gerar relatórios com base em grupos de usuários, escolha **Grupo de usuários** no eixo X na lista de opções suspensas, conforme mostrado na captura de tela abaixo.

![](assets/x-axis-reporting.png)

*Gerar relatórios de Grupo de Usuários*

Outra lista suspensa **Selecionar** aparece adjacente ao eixo X com uma lista de grupos de usuários disponíveis para a sua conta. Nesta lista suspensa, você pode selecionar um ou vários grupos de usuários.

Após você salvar e gerar este relatório, se selecionou múltiplos grupos de usuários, o relatório é gerado com todos os grupos de usuários representados no gráfico de barras adjacentes entre si no eixo X.

Este relatório do grupo de usuários permite comparar o desempenho de um departamento/divisão/função em relação ao outro para avaliar as suas realizações de aprendizagem.

### Atributos personalizados de grupos de usuários/usuário {#customusergroupsuserattributes}

Você também pode criar grupos de usuários personalizados usando o recurso Adicionar usuários/grupos de usuários no Learning Manager. Após criar grupos de usuários, você pode gerar relatórios para esses grupos de usuários personalizados com a ajuda de uma lista de atributos, tal como local, filial, e assim por diante.

No eixo X, escolha a opção de atributo do usuário e selecione o atributo de **selecionar** ao lado dele. Para criar um relatório personalizado de grupo de usuários com base nesses atributos, você também precisa escolher o grupo de usuários apropriado no filtro.

Os Gerentes podem criar relatórios do grupo de usuários somente para seus próprios membros da equipe como Alunos.

## Tipos de relatórios {#typesofreports}

* Estatísticas de entrega do curso para Alunos
* Relatório da eficácia dos cursos
* Relatório com base no conhecimento do Aluno
* Estatísticas de inscrição no programa de aprendizado para Alunos
* Tempo gasto no aprendizado pelos Alunos
* Certificação de conclusão

## Meus relatórios {#myreports}

Um painel é uma coleção de relatórios. Os relatórios podem ser agrupados em um painel de acordo com sua escolha.

**Relatórios de amostra**

Clique nesta guia para exibir alguns relatórios indicativos baseados em pontos de dados de amostra. Explore esses relatórios para obter uma ideia dos diferentes tipos de relatórios com recursos avançados que você pode gerar usando os dados da sua conta.

**Meus relatórios**

Clique nesta guia de painel para exibir todos os painéis que você criou. Na lista suspensa Exibir painel, você pode selecionar o painel padrão ou qualquer um dos painéis criados.

**Adicionar painel**

1. Clique em Adicionar painel no lado direito da página, para começar a criar seus próprios painéis.

   ![](assets/add-dashboard.png)

   *Criar seu próprio painel*

1. Forneça o nome e a descrição do painel e clique em **[!UICONTROL Salvar]**.

Você pode visualizar o painel recentemente criado na lista Meus painéis.

Para adicionar relatórios ao painel, clique na lista suspensa no canto superior direito da janela do painel e clique em Adicionar relatório. O relatório que você cria desta forma é associado ao seu painel.

>[!NOTE]
>
>Os relatórios que você cria ao clicar em Adicionar no canto superior direito da página Relatórios, são adicionados ao painel padrão.

**Relatórios compartilhados**

Os relatórios compartilhados são uma coleção de relatórios que foram compartilhados com você por outros usuários em sua organização. Se você tiver as permissões, poderá baixar ou duplicar os relatórios compartilhados. Entre em contato com o Administrador da sua organização para obter os direitos de acesso para baixar/duplicar relatórios compartilhados.

**Relatórios inscritos**

Você pode se inscrever para relatórios favoritos fornecendo sua ID de e-mail aqui. Seus relatórios inscritos lhe serão enviados por e-mail.

Clique no botão **Editar** no canto direito do seu nome de relatório na lista relatórios para modificar sua assinatura a qualquer momento.

## Exibir relatórios {#viewingreports}

Na página Resumo do relatório, você pode exibir todos os relatórios. Você pode minimizar cada relatório ao clicar no ícone de menos (-) no canto superior direito de cada relatório. Clique no ícone de mais para exibir novamente seu relatório.

**Exibição rápida com diferentes datas** 

O valor da data que você usa para exibir o relatório é temporário. A exibição do relatórios não é baixada quando você escolhe a opção de download. Esta é apenas exibição temporária.

Você pode alterar a faixa/valor da data para todos os relatórios e exibir rapidamente para uma data diferente sem modificar e salvar o relatório. Clique no ícone Editar (como mostrado com uma seta na captura de tela abaixo) junto a faixa de datas, tal como trimestre até a data, último ano, e assim por diante. Selecione o novo valor no menu suspenso e clique na marca de seleção para confirmar a alteração. Você pode cancelar a alteração clicando na marca X.

**Exibição rápida com diferentes Gerentes** 

Se houver múltiplos Gerentes que se reportam a você, poderá exibir os relatórios rapidamente para cada Gerente. Escolha o nome do gerente na lista suspensa para exibir um relatório exclusivo para cada gerente.
**Editar/Mover para o painel/Criar uma cópia/Excluir/Redimensionar relatórios** Clique na seta suspensa no canto superior direito de cada relatório para exibir as opções suspensas como Editar/Mover para Painel/Criar uma cópia/Excluir/Redimensionar.

<!--![](assets/edit-options-dashboard-300x126.png)-->

**Editar** Ao modificar dados, para voltar aos valores iniciais, clique em Redefinir. Clique em Salvar após modificar os valores.

**Mover para o Painel** Você pode mover o relatório atual para outro painel, que é escolhido na lista de painéis.

**Criar uma cópia** Você pode copiar o relatório para o mesmo painel ou para outro painel, que é escolhido na lista de painéis.

**Excluir** Clique em Excluir para remover o relatório. Uma mensagem de advertência/confirmação aparece antes que você possa excluir o relatório.

**Redimensionar** Você pode redimensionar seus relatórios em tamanhos 1 × 1 (médio) e 2 × 2 (grande).

## Inscrições de e-mail {#emailsubscriptions}

Você pode obter seus relatórios favoritos no e-mail, inscrevendo-se para os mesmos.

Na página Relatórios, clique em Inscrição de e-mail adjacente ao botão Adicionar no canto superior direito da página. A página Inscrição no relatório será exibida.

Comece a digitar o nome do relatório no campo Relatórios para selecionar o nome do relatório na lista suspensa. Escolha a frequência de e-mails como diária, semanal, mensal de acordo com sua escolha, adicione o assunto do e-mail e clique em Adicionar para assinar.

Clique em Editar para modificar a assinatura. Clique em Remover para excluir a inscrição.
