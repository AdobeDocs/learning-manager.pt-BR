---
description: Criação e gerenciamento de relatórios para Gerentes.
jcr-language: en_us
title: Relatórios
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '1840'
ht-degree: 0%

---



# Relatórios

Criação e gerenciamento de relatórios para Gerentes.

O Adobe Learning Manager permite que você crie relatórios variados para acompanhar, monitorar e controlar as atividades do aluno. As atividades dos alunos são rastreadas e capturadas automaticamente no banco de dados. Os relatórios do Gerente e do Administrador são gerados a partir do banco de dados.

## Visão geral {#overview}

O processo de geração de relatórios é o mesmo para o administrador e o gerente. Os gerentes podem exibir relatórios correspondentes aos seus subordinados, enquanto o administrador pode exibir todos os relatórios da organização.

Os relatórios são agregados em um painel. Um relatório deve existir em um painel. A **Painel padrão** existe por padrão na página relatórios. Qualquer relatório adicionado por você passa para esse painel padrão. Para adicionar relatórios a painéis de controle individuais, use a seta suspensa e escolha Adicionar relatório. Para obter mais informações sobre a criação de painéis, consulte a seção Painéis nesta página.

## Painéis do gerente {#manager-dashboards}

Um gerente pode exibir informações sobre sua equipe direta ou indireta, como um resumo.

O gerente pode filtrar o relatório de acordo com intervalos como, trimestre, este mês, últimos três meses inteiros e últimos 12 meses inteiros.

## Resumo do aprendizado {#learningsummary}

![](assets/manager-learningsummary.png)

*Exibir resumo de aprendizado*

![](assets/manager-dashboard.jpg)

*Filtrar resumo de aprendizado por data*

## Painel de Conformidade {#compliancedashboard}

Veja a conformidade de sua equipe e qual membro está próximo da não conformidade. Escolha os objetos de aprendizado e veja o status de cada um.

![](assets/compliance-dashboard.png)

*Exibir painel de conformidade*

## Status das Habilidades {#skillsstatus}

Veja a porcentagem de alunos de cada habilidade. Escolha no máximo cinco habilidades para as quais deseja ver as habilidades dos alunos. A visualização está na forma de um gráfico de barras empilhadas. Ao passar o mouse sobre cada barra, você pode ver a divisão do status dessa habilidade.

![](assets/manager-skills-status.png)

*Exibir o status das habilidades de um aluno*

## Rastreador de habilidades {#skilstracker}

Veja uma projeção da conclusão das habilidades em uma equipe. Escolha a porcentagem de conclusão prevista e a data de uma habilidade.

Com base em dados históricos, você pode ver uma representação gráfica da projeção de conclusão de habilidade na data selecionada.

![](assets/historical-data.png)

*Exibir projeção de conclusão de habilidade*

## Criação de relatórios {#creatingreports}

1. Clique em Relatórios no painel esquerdo. A página Resumo do relatório é exibida.\
   **Observação**
Por padrão, pelo menos três relatórios de amostra aparecem na página de resumo de relatório. Você só pode exibir esses relatórios de amostra para ter uma ideia de como criá-los e personalizá-los.

1. Na página Resumo do relatório, clique em Adicionar. A caixa de diálogo de criação de relatório é exibida.
1. Clique em Salvar para concluir a criação de um relatório. Um relatório de exemplo é mostrado abaixo para referência.

![](assets/add-report.png)

*Caixa de diálogo Adicionar relatório*

Em Tipo de Relatório, você pode escolher um conjunto predefinido de relatórios ou escolher personalizado. Você pode exibir os seguintes relatórios como parte de um conjunto predefinido de relatórios:

* Habilidades atribuídas e obtidas
* Curso inscrito e concluído
* Eficácia para cursos
* Programas de aprendizado inscritos e concluídos
* Tempo de aprendizado gasto por curso
* Tempo de aprendizado gasto por trimestre

Você pode usar os tipos de relatório mencionados acima para gerar relatórios de mais de 300 variações.

Nome do Relatório Digite um título para o relatório.

**Eixo Y principal** Escolha o primeiro critério/critério principal para o relatório nas opções suspensas. Para alguns dos critérios selecionados, você tem a opção de escolher um ou vários estados na caixa suspensa Estados adjacentes. Por exemplo, para um critério principal das estatísticas de inscrição do curso, os estados podem ser concluídos, incompletos, inscritos e assim por diante. Os dados do intervalo principal são representados na forma de gráficos de barras no relatório.

**Eixo Y secundário** Escolha o critério/intervalo do eixo Y secundário para o relatório nas opções suspensas. Por exemplo, na opção de inscrição no programa de aprendizado, escolha um ou vários estados na lista suspensa Estados adjacentes. Os dados do intervalo secundário são representados na forma de gráficos de linhas.

**Eixo X** Escolha os critérios apropriados do eixo x para o relatório nas opções suspensas. Se o eixo x for escolhido como data, uma opção para agrupar o critério do eixo x por dia, mês, trimestre e ano estará disponível.

**Data** Escolha a opção apropriada na lista suspensa. Opções: último mês, trimestre, ano, QTD (últimos 90 dias), YTD (últimos 365 dias) e o intervalo de datas. Se você escolher a faixa de datas, forneça as datas De e Até da seguinte maneira:

**De** Escolha a data inicial a partir da qual você gostaria de ver o relatório.

**Para** Escolha a data final para o relatório.

## Filtros {#filters}

Os filtros aparecem na caixa de diálogo Adicionar relatório na parte inferior com base nos tipos de relatórios escolhidos. Alguns dos filtros de destaque são mencionados abaixo.

**Gerente** Você pode escolher qualquer um dos gerentes com base na hierarquia. Para alguns gerentes, pode haver gerentes subordinados e vários funcionários subordinados a cada gerente subordinado.

**Perfil** Escolha a designação do funcionário. Isso ajudaria na exibição de relatórios de funcionários com base em seu perfil/designação. Por exemplo, cientista da computação, engenheiro etc.

**Grupo de usuários** Escolha o grupo de usuários com base no qual deseja filtrar os relatórios. O Learning Manager pega os grupos de usuário definidos para sua conta a partir do recurso Usuários.

**Curso** Você pode filtrar o relatório com base em qualquer curso ao escolher o mesmo na lista suspensa.

![](assets/sample-report-admin.png)

*Exibir gráfico de cursos inscritos e concluídos*

>[!NOTE]
>
>Acima da legenda para o gráfico, você pode exibir uma caixa de zoom. Você pode mover o cursor sobre ela, clicar e arrastar a barra transversal sobre qualquer parte da área da caixa de zoom na qual deseja aplicar mais zoom.

Você pode exibir os valores secundários do eixo y na forma de uma linha ao longo das barras do gráfico. Por exemplo, na amostra acima, você pode ver os valores de Eficácia na linha cinza ao longo do gráfico.

## Relatórios de grupo de usuários {#user-group-reporting}

Acompanhe o desempenho de grupos de usuários, como departamentos, parceiros externos e funções, em comparação com outros grupos de usuários ou com outros objetivos de aprendizado.

### Grupos de usuários {#usergroups}

Para gerar relatórios com base em grupos de usuários, escolha **Grupo de usuários** no eixo X na lista de opções suspensas, conforme mostrado na captura de tela abaixo.

![](assets/x-axis-reporting.png)

*Gerar relatórios de Grupo de Usuários*

Outro **Selecionar** é exibida ao lado do eixo X com uma lista de grupos de usuários disponíveis para sua conta. Nesta lista suspensa, você pode selecionar um ou vários grupos de usuários.

Depois de salvar e gerar este relatório, se você selecionou vários grupos de usuários, o relatório será gerado com todos os grupos de usuários representados em um gráfico de barras adjacente entre si no eixo x.

Esse relatório de grupo de usuários permite comparar o desempenho de um departamento/divisão/função com o outro para avaliar suas realizações de aprendizado.

### Atributos de usuários/grupos de usuários personalizados {#customusergroupsuserattributes}

Você também pode criar grupos de usuários personalizados usando o recurso Adicionar usuários/grupos de usuários no Learning Manager. Depois de criar os grupos de usuários, você pode gerar relatórios para esses grupos de usuários personalizados com a ajuda de uma lista de atributos como local, ramificação e assim por diante.

No eixo X, escolha a opção de atributo do usuário e selecione o atributo de **selecionar** ao lado dele. Para criar um relatório personalizado de grupo de usuários com base nesses atributos, você também precisa escolher o grupo de usuários apropriado no filtro.

Os gerentes podem criar relatórios de grupos de usuários apenas para os membros de sua própria equipe como alunos.

## Tipos de relatórios {#typesofreports}

* Estatísticas de entrega do curso para alunos
* Relatório de eficácia dos cursos
* Relatório baseado em habilidades do aluno
* Estatísticas de inscrição do programa de aprendizado para alunos
* Tempo de aprendizado gasto pelos alunos
* Conclusão da certificação

## Meus relatórios {#myreports}

Um painel é uma coleção de relatórios. Os relatórios podem ser agrupados em um painel de acordo com sua escolha.

**Relatórios de amostra**

Clique nesta guia para exibir alguns relatórios indicativos baseados em pontos de dados de amostra. Explore estes relatórios para ter uma ideia de diferentes tipos de relatórios com muitos recursos que você pode gerar usando os dados da sua conta.

**Meus relatórios**

Clique nesta guia de painel para exibir todos os painéis que você criou. Na lista suspensa Exibir painel, você pode selecionar o painel padrão ou qualquer um dos painéis criados.

**Adicionar painel**

1. Clique em Adicionar painel no lado direito da página, para começar a criar seus próprios painéis.

   ![](assets/add-dashboard.png)

   *Criar seu próprio painel*

1. Forneça o nome e a descrição do painel e clique em **[!UICONTROL Salvar]**.

Você pode ver o painel criado recentemente na lista Meus painéis.

Para adicionar relatórios ao painel, clique na lista suspensa no canto superior direito da janela do painel e clique em Adicionar relatório. O relatório criado dessa maneira é associado ao seu painel.

>[!NOTE]
>
>Os relatórios que você cria ao clicar em Adicionar no canto superior direito da página Relatórios, são adicionados ao painel padrão.

**Relatórios compartilhados**

Relatórios compartilhados são uma coleção de relatórios que foram compartilhados com você por outros usuários em sua organização. Se você tiver as permissões, poderá baixar ou duplicar os relatórios compartilhados. Entre em contato com o administrador da sua organização para obter direitos de acesso de download/duplicação aos relatórios compartilhados.

**Relatórios inscritos**

Você pode assinar seus relatórios favoritos fornecendo sua ID de e-mail aqui. Seus relatórios inscritos são enviados a você por email.

Clique no botão **Editar** no canto direito do seu nome de relatório na lista relatórios para modificar sua assinatura a qualquer momento.

## Exibição de relatórios {#viewingreports}

Na página Resumo do relatório, você pode exibir todos os relatórios. Você pode minimizar cada relatório clicando no ícone de menos (-) no canto superior direito de cada relatório. Clique no ícone + para exibir o relatório novamente.

**Exibição rápida com diferentes datas**

Os valores de data que você usa para exibir o relatório são temporários. Esta visualização do relatório não é baixada quando você escolhe a opção de download. Esta é apenas uma exibição temporária.

Você pode alterar o intervalo/valor de datas de qualquer relatório e exibir rapidamente datas diferentes sem modificar e salvar o relatório. Clique no ícone de edição (conforme mostrado com uma seta na captura de tela abaixo) próximo ao intervalo de datas, como QTD, do último ano e assim por diante. Escolha o novo valor no menu suspenso e clique na marca de seleção para confirmar a alteração. Para cancelar a alteração, clique na marca X.

**Exibição rápida com diferentes gerentes**

Se houver vários gerentes subordinados a você, você poderá exibir os relatórios rapidamente para cada gerente. Escolha o nome do gerente na lista suspensa para exibir um relatório exclusivo para cada gerente.
**Editar/Mover para o painel/Criar uma cópia/Excluir/Redimensionar relatórios** Clique na seta suspensa no canto superior direito de cada relatório para exibir as opções suspensas como Editar/Mover para Painel/Criar uma cópia/Excluir/Redimensionar.

<!--![](assets/edit-options-dashboard-300x126.png)-->

**Editar** Ao modificar dados, para voltar aos valores iniciais, clique em Redefinir. Clique em Salvar após modificar os valores.

**Mover para o Painel** Você pode mover o relatório atual para outro painel, que é escolhido na lista de painéis.

**Criar uma cópia** Você pode copiar o relatório para o mesmo painel ou para outro painel, que é escolhido na lista de painéis.

**Excluir** Clique em Excluir para remover o relatório. Uma mensagem de aviso/confirmação é exibida antes da exclusão do relatório.

**Redimensionar** Você pode redimensionar seus relatórios em tamanhos 1 × 1 (médio) e 2 × 2 (grande).

## Assinaturas de email {#emailsubscriptions}

Você pode obter seus relatórios favoritos em emails assinando-os.

Na página Relatórios, clique em Assinatura de email ao lado do botão Adicionar no canto superior direito da página. A página de assinatura Relatórios é exibida.

Comece a digitar o nome do relatório no campo Relatórios para selecionar o nome do relatório na lista suspensa. Escolha a frequência de e-mails como diária, semanal, mensal de acordo com sua escolha, adicione o assunto do e-mail e clique em Adicionar para assinar.

Clique em Editar para modificar a assinatura. Clique em Remover para excluir a assinatura.
