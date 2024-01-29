---
description: Saiba mais sobre os relatórios associados à função de administrador no aplicativo Learning Manager.
jcr-language: en_us
title: Relatórios
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '6441'
ht-degree: 0%

---



# Relatórios

Saiba mais sobre os relatórios associados à função de administrador no aplicativo Learning Manager.

O Adobe Learning Manager permite que você crie relatórios variados para acompanhar, monitorar e controlar as atividades do aluno. As atividades dos alunos são rastreadas e capturadas automaticamente no banco de dados. Os relatórios do Gerente e do Administrador são gerados a partir do banco de dados.

## Visão geral {#overview}

O processo de geração de relatórios é semelhante para o administrador e o gerente. Os gerentes podem exibir relatórios correspondentes aos seus subordinados, enquanto o administrador pode exibir todos os relatórios da organização.

Os relatórios são agregados em um painel. Um relatório deve existir em um painel. A **[!UICONTROL Painel padrão]** existe por padrão na página relatórios. Qualquer relatório adicionado por você passa para esse painel padrão. Para adicionar relatórios a painéis de controle individuais, use a seta suspensa e escolha **[!UICONTROL Adicionar relatório]**. Para obter mais informações sobre a criação de painéis, consulte a seção Painéis nesta página.

## Painéis Resumo do aprendizado {#dashboards}

Veja um relatório resumido de todas as atividades de aprendizado na plataforma. Nesta página, você pode ver as seguintes informações de resumo para a equipe do usuário raiz selecionado e seus perfis externos. O intervalo de tempo também pode ser selecionado:

* Resumo do aprendizado na forma de inscrições, exibições e conclusões
* Principais habilidades
* Resumo de conformidade

![](assets/summary-charts.png)
*Gráficos de resumo*

Se houver gerenciadores de nível raiz internos, eles serão exibidos um após o outro.

Todos os perfis externos serão listados após os perfis internos (usuários internos de nível raiz).

Se um perfil externo tiver um gerente, a hierarquia do gerente será exibida na **[!UICONTROL Mostrando Dados Para]** lista suspensa. - O usuário será listado na hierarquia do gerente em todas as páginas de detalhes (resumo do aprendizado, conformidade e status da habilidade)

Caso contrário, todos os detalhes de usuário individuais serão exibidos na lista.

Para ver detalhes mais granulares das inscrições de várias equipes internas, clique em **[!UICONTROL Detalhes do Resumo do Aprendizado]**.

![](assets/learning-sunnarydetails.png)
*Detalhes do Resumo do aprendizado*

Ao clicar em qualquer inscrição, você pode ver os alunos de cada gerente e a inscrição em quais objetos de aprendizado. Você também pode ver os detalhes de andamento e conclusão de cada aluno.

![](assets/learners-for-a-manager.png)
*Alunos Aee atribuídos a um gerente*

Clique em qualquer equipe e exporte o relatório como um csv. Um administrador pode exportar o relatório de qualquer grupo de usuários ou usuário individual selecionando o grupo de usuários ou usuário individual e, em seguida, exportar detalhes na lista suspensa Ação.

Além disso, você pode ver um gráfico de barras que mostra as habilidades que estão em andamento e foram obtidas. Você pode adicionar/remover habilidades que deseja apresentar no gráfico.

![](assets/skill-status-stackedbarchart.png)
*Gráfico de barras empilhadas do status da habilidade*

Na visualização final, você pode verificar o status de conformidade dos alunos e tomar as medidas apropriadas.

Além disso, um administrador pode exibir dados de treinamento individuais no Painel de conformidade.

Por exemplo, o administrador identificou três treinamentos para controlar a conformidade. O Learning Manager fornece a captura de tela da conformidade para todos os três treinamentos de uma só vez.

Agora um administrador pode clicar em qualquer treinamento e visualizar rapidamente a conformidade do treinamento selecionado.

![](assets/compliance-dashboard.png)
*Exibir painel de Conformidade*

Você também pode ver o status de conformidade de cada equipe interna.

Clique no link **[!UICONTROL Detalhes do Status de Conformidade]** na parte inferior da visualização.

Você pode ver que, para uma equipe, o número de alunos da equipe está violando ou honrando a conformidade de aprendizado.

![](assets/compliance-statusofateam.png)
*Status de conformidade de uma equipe*

## Compartilhar treinamento com gerentes

O Learning Manager oferece um painel de conformidade para todos os administradores e gerentes. Os gerentes acham muito útil controlar a conformidade dos membros da equipe para um treinamento específico. Ao mesmo tempo, os administradores gostariam que todos os gerentes adicionassem treinamentos de conformidade ao painel e os monitorassem.

No Learning Manager, o **[!UICONTROL Compartilhar com Gerentes]** O fluxo de trabalho permite que os administradores compartilhem treinamentos com gerentes, para que eles possam ser adicionados ao Painel de conformidade de um gerente. Assim, os gerentes não precisam realizar nenhuma ação e podem começar a monitorar a conformidade imediatamente.

Um administrador pode compartilhar um conjunto de cursos de treinamento com gerentes individualmente ou com um grupo. Esse compartilhamento pode ajudar um gerente a controlar facilmente a conformidade de sua equipe com o treinamento especificado.

O administrador pode “enviar” uma lista padrão de treinamento de conformidade para ser exibida no painel de conformidade do gerente.

### Compartilhar treinamento

1. Entrada **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]**, role para baixo e clique na guia **[!UICONTROL Compartilhar com Gerentes]**.

   ![](assets/share-with-managers.png)
   *Compartilhar treinamento com gerentes*

1. Para adicionar treinamento ou vários treinamentos, clique em **[!UICONTROL Compartilhar mais]**.

1. No menu **[!UICONTROL Compartilhar com Gerentes]** escolha o(s) treinamento(s) e o(s) gerente(s).

   ![](assets/select-training.png)
   *Selecionar treinamento para compartilhar com gerentes*

1. Clique em **[!UICONTROL Compartilhar]**.

O treinamento é compartilhado com o gerente especificado.

### Exibir treinamento

Na lista de treinamento compartilhado, clique em **[!UICONTROL Exibir]**. Você pode ver o treinamento atribuído a um gerente ou a alguns gerentes.

### Retirar treinamento

1. Para remover o treinamento de um gerente, clique em **[!UICONTROL Retirar]**.

1. Clique em **[!UICONTROL Continuar]**. Isso retira o treinamento compartilhado anteriormente do painel de conformidade do gerente.

## Painéis de atividade do usuário {#useractivitydashboards}

Veja um resumo de todas as atividades do usuário na plataforma ao longo do tempo. Configure grupos de usuários e aplique filtros.

O painel de atividade do usuário exibe a atividade dos usuários na conta. Os três relatórios listados são:

* **Usuários Registrados:** Este relatório fornece informações sobre o número de usuários registrados em sua conta, semana após semana. Para contas com licenciamento de unidades ativas mensais, o relatório mostra as unidades do MAU.

* **Relatório de Visitas do Usuário:** Este relatório fornece informações sobre o número de usuários que acessam a plataforma diariamente. O relatório mensal também está disponível.

* **Relatório de tempo gasto no aprendizado:** Este relatório fornece informações sobre o Tempo gasto no aprendizado na plataforma diariamente. O relatório mensal também está disponível.

## Usuários registrados {#registeredusers}

O Learning Manager registra o número de usuários registrados no sistema todas as semanas. Os administradores podem exibir este relatório para entender a contagem registrada de usuários naquele dia da semana. A contagem registrada uma vez armazenada por uma semana não é alterada. Portanto, a contagem histórica registrada não está relacionada ao conjunto atual de alunos no sistema.

Este relatório fornece informações sobre o número de usuários registrados em sua conta, semana após semana.

Para contas com licenciamento de unidades ativas mensais, o relatório mostra as unidades do MAU.

![](assets/registered-usersreport.png)
*Relatório de Usuários Registrados*

***Para contas da unidade de acesso mensal:***

**Relatório mensal de usuários ativos**

Este relatório mostra a contagem de alunos ativos na plataforma de aprendizado a cada mês. O usuário é considerado ativo no mês se realizar alguma das ações de aprendizado mencionadas aqui. As unidades ativas mensais são contadas da mesma forma.

A contagem mensal ativa uma vez contada e armazenada por um mês, não é alterada. Portanto, a contagem histórica exibida não está relacionada ao conjunto atual de alunos no sistema.

## Visitas do usuário {#uservisits}

Este relatório mostra o total de alunos acessando o sistema em um período de dia ou mês. Navegar pela plataforma de aprendizado sem consumir qualquer aprendizado também é considerado como “acesso” à plataforma de aprendizado. Isso ajuda o administrador a entender o conjunto total de usuários que acessam o sistema. No primeiro dia do mês, o Learning Manager cria um registro do total de usuários acessando a plataforma no mês anterior. Ele também captura as informações do grupo de usuários para esses usuários.

Somente os grupos de usuários configurados pelo administrador são registrados. Isso permite que os administradores apliquem filtros em grupos de usuários para dados históricos mensais também. Observe que a configuração do caso de grupos de usuários é modificada e o Learning Manager não registrou dados para esse grupo de usuários nos meses anteriores; então, o Learning Manager não pode exibir os dados para esses grupos de usuários recém-configurados nos meses anteriores.

Este relatório contém usuários que acessam a plataforma usando todos os formatos, como Web, aplicativo móvel, soluções personalizadas sem periféricos e assim por diante. O gráfico de uso do aplicativo de dispositivo menciona especificamente apenas os usuários que acessam a plataforma usando o aplicativo do dispositivo do Learning Manager. Isso ajuda os administradores a identificar o uso do aplicativo móvel em suas contas.

![](assets/user-visit-report.png)
*Relatório de Visita do Usuário*

## Relatório de Tempo Gasto no Aprendizado {#learningtimespentreport}

Aqui, você pode ver um gráfico de linhas de eixo duplo que mostra o tempo total de aprendizado gasto para todos os alunos em um período de 12 meses. O segundo eixo representa a mediana do tempo gasto no aprendizado de um indivíduo.

O tempo gasto em diferentes objetos de aprendizado, como programas de aprendizado e certificações, é calculado para o seguinte:

* Curso individualizado com conteúdo estático e interativo
* Cursos de atividade com URL.
* Sessões de fim de semana com o sinalizador de fim de semana ativado.
* Sessão de conexão de aula virtual na qual a participação é marcada automaticamente.
* O tempo gasto em diferentes objetos de aprendizado, como programas de aprendizado e certificações
* Instruções xAPI para um curso de atividade xAPI.

Você pode exportar o gráfico como uma planilha do Excel.

É fornecido um filtro para escolher a configuração de grupo de usuários que ajudará na visualização dos dados em relação a diferentes grupos de usuários.

O filtro de data e grupo de usuários selecionado é aplicado a todos os gráficos relevantes no painel.

>[!NOTE]
>
>Para **[!UICONTROL Visitas do usuário]** e **[!UICONTROL Tempo gasto no aprendizado]** relatórios, os dados padrão (quando nenhum grupo de usuários estiver configurado) exibidos serão para toda a conta.

## Painel Conteúdo do treinamento {#trainingcontentdashboard}

O painel de conteúdo do treinamento oferece insights sobre treinamentos disponíveis na plataforma. Você pode visualizar treinamentos populares ou acompanhar todos os treinamentos disponíveis.

## Relatório de treinamentos {#trainingsreport}

Este relatório fornece informações sobre o total de treinamentos disponíveis na plataforma (no estado publicado) mês a mês. Ele fornece uma indicação do número de treinamentos oferecidos ao longo do tempo.

![](assets/training-report.png)
*Relatório de treinamento*

## Relatório de treinamentos ativos {#activetrainingsreport}

Este relatório fornece informações sobre os treinamentos que estão ativos no intervalo de tempo selecionado. Treinamentos ativos são treinamentos que são inscritos, visualizados no reprodutor ou concluídos no período determinado.

Para treinamentos ativos, os dados de todos os grupos internos do usuário raiz (com função de gerente) estarão disponíveis para seleção quando nenhuma configuração de grupo de usuários for feita. Além dos grupos de usuários raiz, você pode configurar mais 10 grupos de usuários, se necessário.

![](assets/active-trainingsreport.png)
*Relatório de treinamentos ativos*

>[!NOTE]
>
>Os dados não são exibidos como esperado quando **[!UICONTROL Todos os usuários]** e **[!UICONTROL 12 meses]** filtros são selecionados, mas os dados são exibidos quando você seleciona **[!UICONTROL Todos os grupos de usuários internos].**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Referência</b></p></td>
   <td>
    <p><b>Métrica</b></p></td>
   <td>
    <p><b>Descrição</b></p></td>
  </tr>
  <tr>
   <td>
    <p>1</p></td>
   <td>
    <p>Taxa de Início (%)</p></td>
   <td>
    <p>Proporção do número de alunos que iniciaram o curso e do número de inscrições.</p></td>
  </tr>
  <tr>
   <td>
    <p>2</p></td>
   <td>
    <p>Taxa de conclusão (%)</p></td>
   <td>
    <p>Proporção do total de usuários que concluíram o curso e do total de usuários que iniciaram o curso.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>3</p></td>
   <td>
    <p>Feedback do aluno</p></td>
   <td>
    <p>Média de todas as respostas de feedback L1 recebidas em uma escala de 1 a 10, arredondadas até o número inteiro mais próximo.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>4</p></td>
   <td>
    <p>Feedback do gerente</p></td>
   <td>
    <p>Média de todas as respostas de feedback L3 recebidas em uma escala de 1 a 5, arredondadas até o número inteiro mais próximo<br></p></td>
  </tr>
 </tbody>
</table>

O relatório de treinamento tem duas colunas adicionais:

1. Classificação de estrelas média de um curso.
1. Número de alunos que avaliaram o curso.
1. Caminho incorporado
1. ID do caminho incorporado
1. ID do curso incorporado

>[!NOTE]
>
>A taxa de início, a taxa de conclusão, o feedback do aluno e o feedback do gerente não são afetados pelos filtros aplicados. Os filtros afetam apenas a inscrição, as visualizações e as conclusões.

>[!NOTE]
>
>Para ambos os relatórios (Conteúdo de treinamento, Atividade do usuário), você pode configurar no máximo 10 grupos de usuários. Pode levar até 24 horas para o processamento ser concluído e disponibilizar os filtros recém-configurados.

## Relatórios do painel {#dashboardreports}

Um painel é uma coleção de relatórios. Os relatórios podem ser agrupados em um painel de acordo com sua escolha.

## Relatórios de amostra {#samplereports}

O **[!UICONTROL Relatórios de amostra]** para mostrar alguns relatórios indicativos que são baseados em pontos de dados de amostra. Explore estes relatórios para ter uma ideia de diferentes tipos de relatórios com muitos recursos que você pode gerar usando os dados da sua conta.

## Relatórios do painel {#DashboardReports-1}

Para exibir todos os painéis que você criou, clique nesta guia de painel. Na guia **[!UICONTROL Exibir painel]** , você pode selecionar o painel padrão ou um painel que criou.

## Criar um painel {#createadashboard}

1. Para começar a criar seus próprios painéis, clique em Adicionar painel no lado direito da página.

   ![](assets/add-dashboards.png)
   *Adicionar painéis*

1. Forneça o nome e a descrição do painel.
1. Se quiser compartilhar o painel com qualquer gerente, escolha-o em **[!UICONTROL Compartilhar com]** campo. Você pode usar qualquer critério de seleção normal para esta operação.
1. Clique em **[!UICONTROL Salvar].**

Você pode ver o painel criado recentemente na seção **[!UICONTROL Relatórios do painel]** guia.

Para adicionar relatórios ao painel, clique na lista suspensa no canto superior direito da janela do painel e clique em **[!UICONTROL Adicionar relatório]**. O relatório criado dessa maneira é associado ao seu painel.

>[!NOTE]
>
>Os relatórios que você cria ao clicar em Adicionar no canto superior direito da página Relatórios, são adicionados ao painel padrão.

## Painéis compartilhados {#shareddashboards}

Painéis compartilhados são uma coleção de relatórios que foram compartilhados com você por outros usuários em sua organização. Todos os relatórios adicionados a um painel compartilhado são compartilhados automaticamente com outros usuários que têm acesso a esse painel.

É possível compartilhar o painel das seguintes maneiras:

* Inserindo usuários em **[!UICONTROL Compartilhar com]** com quem o painel é compartilhado.
* Escolha Editar painel na lista suspensa e insira os detalhes do usuário para compartilhar o painel.

>[!NOTE]
>
>Um gerente pode exibir apenas os relatórios dos membros de sua equipe em um painel compartilhado.

## Downloads {#downloads}

A planilha de relatórios do painel exportada fornece informações detalhadas em vez de resumo de relatório. O relatório baixado segue o formato de uma transcrição do aluno.

## Criar relatórios {#report}

1. Clique em Relatórios no painel esquerdo. A página Resumo do relatório é exibida.

   >[!NOTE]
   >
   >Por padrão, pelo menos três relatórios de amostra aparecem na guia painel de amostra. Você só pode exibir os relatórios de amostra para ter uma ideia de como criá-los e personalizá-los.

1. No canto superior direito da página, clique em **[!UICONTROL Adicionar]**.
1. No menu **[!UICONTROL Adicionar relatório]** caixa de diálogo, na lista suspensa Tipo, você pode escolher um dos relatórios predefinidos ou selecionar **[!UICONTROL Personalizado]**. Se você selecionar um relatório predefinido, poderá ver que o formulário é pré-preenchido. Você pode fazer alterações em alguns dos campos e clicar em **[!UICONTROL Salvar]**. Isso adiciona o relatório ao painel padrão.

   ![](assets/create-report.png)
   *Criar relatório*

   Entrada **[!UICONTROL Tipo de relatório]**, você pode escolher um conjunto predefinido de relatórios ou escolher valores personalizados. Você pode exibir os seguintes relatórios como parte de um conjunto predefinido de relatórios:

   * Habilidades atribuídas e obtidas
   * Curso inscrito e concluído
   * Eficácia dos cursos
   * Programas de aprendizado inscritos e concluídos
   * Tempo de aprendizado gasto por curso
   * Tempo de aprendizado gasto por trimestre
   * Conclusão da certificação

1. Escolha o **[!UICONTROL Eixo Y]** para seu relatório a partir das opções suspensas. Para alguns dos critérios selecionados, você pode escolher um ou vários estados nas opções Estados. Por exemplo, para um critério principal das estatísticas de inscrição do curso, os estados podem ser concluídos, incompletos e inscritos. Os dados do intervalo principal são representados na forma de gráficos de barras no relatório.

   ![](assets/axes-for-reports.png)
   *Eixos para relatórios*

1. Escolher o secundário **[!UICONTROL Eixo Y]** critérios/faixa para o relatório nas opções suspensas. Por exemplo, para uma opção de inscrição em um programa de aprendizado, escolha um ou vários estados na lista suspensa Estados. Os dados do intervalo secundário são representados na forma de gráficos de linhas.
1. Escolha os critérios apropriados do eixo X*** para o relatório nas opções suspensas. Se o eixo x for escolhido como data, uma opção para agrupar os critérios do eixo x por dia, mês, trimestre e ano estará disponível.
1. Na seção Período de tempo, escolha a opção apropriada no menu suspenso. As opções disponíveis são:

   * Último mês
   * Um quarto
   * Ano
   * QTD (últimos 90 dias)
   * YTD (últimos 365 dias)
   * Intervalo de datas. Forneça valores no campo **[!UICONTROL De]** e **[!UICONTROL Para]** campos de data.

   ![](assets/time-filter-for-report.png)

1. **Seção Filtros**

   Os filtros aparecem na caixa de diálogo Adicionar relatório na parte inferior com base nos tipos de relatórios escolhidos. Alguns dos filtros de destaque são mencionados abaixo.

   * **Gerente:** Você pode escolher qualquer um dos gerentes com base na hierarquia. Para alguns gerentes, pode haver gerentes subordinados e vários funcionários subordinados a cada gerente subordinado.
   * **Perfil:** Escolha a designação do funcionário. Isso ajudaria na exibição de relatórios de funcionários com base em seu perfil/designação. Por exemplo, cientista da computação, engenheiro.
   * **Grupo de usuários:** Escolha o grupo de usuários com base no qual deseja filtrar os relatórios. O Learning Manager pega os grupos de usuário definidos para sua conta a partir do recurso Usuários.
   * **Conteúdo:** Você pode filtrar o relatório com base em qualquer curso ao escolher o mesmo na lista suspensa.

   Expanda esta seção e escolha os filtros necessários.

   ![](assets/choose-filters.png)
   *Escolher filtros*

1. Clique em **[!UICONTROL Salvar]** para concluir a criação de um relatório.

   ![](assets/sample-report.png)
   *Relatório de amostra*

## Editar um relatório {#editareport}

No relatório, clique na seta suspensa e selecione a opção **[!UICONTROL Editar relatório]**.

![](assets/edit-a-report-1.png)
*Editar um relatório*

Faça as alterações necessárias no relatório. Para salvar as alterações, clique em **[!UICONTROL Salvar]**.

## Mover um relatório para um painel {#moveareporttoadashboard}

Escolha esta opção para mover o relatório atual para um painel existente. Para mover o relatório, clique na opção **[!UICONTROL Mover para o Painel]**.

![](assets/move-a-report.png)
*Mover um relatório para um painel*

Escolha o painel para onde deseja mover o relatório e clique em **[!UICONTROL Mover]**.

## Criar uma cópia de um relatório {#createacopyofareport}

Para criar uma cópia do relatório, selecione a opção **[!UICONTROL Criar uma cópia]**.

![](assets/copy-a-report.png)
*Criar uma cópia de um relatório*

Escolha o painel no qual deseja copiar o relatório. Para começar a copiar, clique em **[!UICONTROL Copiar]**.

## Excluir um relatório {#deleteareport}

Para excluir um relatório, escolha a opção **[!UICONTROL Excluir relatório]**. Depois de excluir o relatório, você não poderá restaurá-lo. O processo é irreversível. Continue com cuidado ao excluir um relatório.

![](assets/delete-a-report.png)
*Excluir um relatório*

## Baixar um relatório {#downloadareport}

Para baixar o relatório, escolha a opção **[!UICONTROL Baixar relatório]**.

![](assets/download-a-report.png)
*Baixar um relatório*

## Redimensionar um relatório {#resizeareport}

Você pode redimensionar seus relatórios em tamanhos 1×1 (médio) e 1×2 (grande). Isso proporciona um melhor espaço físico para exibir seus relatórios. Além disso, você pode deslocar e aplicar zoom facilmente a esses relatórios.

## Filtros {#filters}

Os filtros aparecem na **[!UICONTROL Adicionar]** caixa de diálogo de relatório na parte inferior com base nos tipos de relatórios escolhidos. Alguns dos filtros de destaque são mencionados abaixo.

**Gerente** Você pode escolher qualquer um dos gerentes com base na hierarquia. Para alguns gerentes, pode haver gerentes subordinados e vários funcionários subordinados a cada gerente subordinado.

**Perfil** Escolha a designação do funcionário. Isso ajudaria na exibição de relatórios de funcionários com base em seu perfil/designação. Por exemplo, cientista da computação, engenheiro.

**Grupo de usuários** Escolha o grupo de usuários com base no qual deseja filtrar os relatórios. O Learning Manager pega os grupos de usuário definidos para sua conta a partir do recurso Usuários.

**Curso** Você pode filtrar o relatório com base em qualquer curso ao escolher o mesmo na lista suspensa.

![](assets/sample-report-admin.png)
*Filtrar um relatório*

Acima da legenda para o gráfico, você pode exibir uma caixa de zoom. Mova o cursor sobre ele, clique e arraste a barra transversal sobre qualquer parte da área do gráfico da caixa de zoom para aumentar o zoom.

Você pode exibir os valores secundários do eixo y na forma de uma linha ao longo das barras do gráfico. Por exemplo, na amostra acima, você pode ver os valores de Eficácia na linha cinza ao longo do gráfico.

## Relatórios de grupo de usuários {#user-group-reporting}

Acompanhe o desempenho de grupos de usuários, como departamentos, parceiros externos e funções, em comparação com outros grupos de usuários ou com outros objetivos de aprendizado.

### Grupos de usuários {#usergroups}

Para gerar relatórios com base em grupos de usuários, escolha **[!UICONTROL Grupo de usuários]** no eixo x na lista de opções suspensas, conforme mostrado na captura de tela abaixo.

![](assets/user-group-reports.png)
*Relatórios de grupo de usuários*

Para escolher um grupo de usuários, digite o nome do grupo. Você pode ver os grupos sugeridos que são exibidos de acordo com a string digitada. Depois de ver uma lista de grupos, escolha o grupo de usuários necessário.

Também é possível escolher vários grupos de usuários com a ajuda da pesquisa com preenchimento automático.

Depois de salvar e gerar este relatório, se você selecionou vários grupos de usuários, o relatório será gerado com todos os grupos de usuários representados no gráfico de barras próximos um do outro no eixo x.

Esse relatório de grupo de usuários permite comparar o desempenho de um departamento/divisão/função com o outro para avaliar suas realizações de aprendizado.

### Atributos de usuários/grupos de usuários personalizados {#customusergroupsuserattributes}

Você também pode criar grupos de usuários personalizados usando o recurso Adicionar usuários/grupos de usuários no Learning Manager. Depois de criar os grupos de usuários, você pode gerar relatórios para esses grupos de usuários personalizados com a ajuda de uma lista de atributos como local, ramificação.

No eixo x, escolha a opção de atributo do usuário e selecione o atributo na **selecionar** ao lado dele. Para criar um relatório de grupo de usuários personalizado com base nesses atributos, você também deve escolher o grupo de usuários apropriado no filtro.

## Tipos de relatórios {#typesofreports}

O Adobe Learning Manager suporta quatro tipos principais de relatórios, como conclusão, tempo gasto, habilidades e eficácia. Você pode usar os seguintes tipos de relatório para gerar relatórios de mais de 300 variações:

* Estatísticas de entrega do curso para alunos
* Relatório de eficácia dos cursos
* Relatório do aluno baseado em habilidades
* Estatísticas de inscrição do programa de aprendizado para alunos
* Tempo de aprendizado gasto pelos alunos
* Contagem de alunos
* Conclusão da certificação

## Exibição de relatórios {#viewingreports}

Na página Relatórios, você pode exibir todos os relatórios. Você pode minimizar cada relatório clicando no ícone de menos (-) no canto superior direito de cada relatório. Clique no ícone (+) para exibir o relatório novamente.

## Exibição rápida com diferentes datas {#quickviewwithdifferentdates}

Você pode alterar o intervalo/valor de datas de qualquer relatório e exibir rapidamente uma data diferente sem modificar e salvar o relatório. Clique no ícone de edição (conforme mostrado com uma seta na captura de tela abaixo) próximo ao intervalo de datas, como QTD, do último ano. Para confirmar a alteração, escolha o novo valor no menu pop-up e clique na marca de seleção. Para cancelar a alteração, clique na marca X.

>[!NOTE]
>
>Os valores de data que você usa para exibir o relatório são temporários. Essa exibição do relatório não é baixada quando você escolhe a opção de download. Esta exibição é apenas temporária.

![](assets/learner-count-report.png)
*Exibir contagem de alunos*

## Exibição rápida com diferentes gerentes {#quickviewwithdifferentmanagers}

Se houver vários gerentes subordinados a você, você poderá exibir os relatórios rapidamente para cada gerente. Para exibir um relatório exclusivo para cada gerente, escolha o nome do gerente na lista suspensa.

>[!NOTE]
>
>Os valores do gerente que você usa para exibir o relatório são temporários. Esta visualização do relatório não é baixada quando você escolhe a opção de download. Esta exibição é apenas temporária.

## Exibir relatórios do curso {#viewcoursereports}

Você pode visualizar os relatórios específicos de cada curso seguindo as etapas abaixo:

1. Clique em **[!UICONTROL Exibir relatórios do curso]** link na guia Meus painéis na página Relatórios.\
   Uma caixa de diálogo suspensa será exibida. Um campo de entrada de texto aparece onde você pode inserir o curso obrigatório e os nomes dos cursos sugeridos aparecem na lista suspensa. Escolha o curso na lista mostrada.

   ![](assets/view-course-report-300x117.png)

   *Exibir relatórios do curso*

1. Selecione o curso de sua escolha na lista suspensa e clique em Mostrar.
1. Você é redirecionado para a página Resultados da pontuação do quiz do curso selecionado para visualizar o relatório específico do curso.

**Editar/Mover para o painel/Criar uma cópia/Excluir/Redimensionar relatório**

Para exibir as opções suspensas como Editar/Mover para painel de controle/Criar uma cópia/Excluir/Redimensionar, clique na seta suspensa no canto superior direito de cada relatório.

![](assets/edit-options-dashboard-300x126.png)

*Editar/Mover para o painel/Criar uma cópia/Excluir/Redimensionar relatórios*

**[!UICONTROL Editar]** Para voltar aos valores iniciais ao modificar dados, clique em Redefinir. Clique em Salvar após modificar os valores.

**[!UICONTROL Mover para o Painel]** Você pode mover o relatório atual para outro painel, que é escolhido na lista de painéis.

**[!UICONTROL Criar uma cópia]** Você pode copiar o relatório para o mesmo painel ou para outro painel, que é escolhido na lista de painéis.

**[!UICONTROL Excluir]** Clique em Excluir para remover o relatório. Uma mensagem de aviso/confirmação é exibida antes da exclusão do relatório.

**[!UICONTROL Redimensionar]** Você pode redimensionar seus relatórios em tamanhos 1 × 1 (médio) e 2 × 2 (grande).

## Gerar e exibir relatórios para conta entre parceiros {#generateandviewreportsforpeeraccount}

Como administrador, além de gerar relatórios para sua conta, você também pode gerar e exibir relatórios para contas entre parceiros que você definiu.

Ao estabelecer uma conta entre parceiros com outro usuário, você pode visualizar os relatórios dessa conta entre parceiros no **[!UICONTROL Relatórios]** página. Ao criar um relatório, você encontrará o **[!UICONTROL Selecionar conta]** campo. Na lista suspensa, que lista toda a conta entre parceiros à qual você está associado, selecione a conta para a qual deseja exibir os relatórios compartilhados.

Ao criar uma conta entre parceiros, se a opção Compartilhar catálogo não tiver sido selecionada, você não poderá exibir essa conta entre parceiros nesta lista.

![](assets/acc1-jpg.png)
*Gerenciar relatórios para conta entre parceiros*

1. Selecione o eixo x e o eixo y para este relatório e selecione a data para este relatório.
1. Observe que no campo Filtros, o botão Catálogos compartilhados é ativado automaticamente. É obrigatório. Se o Catálogo Compartilhado não estiver ativado, significa que você não poderá gerar ou exibir relatórios para a conta entre parceiros.
1. Na lista suspensa abaixo de Catálogo Compartilhado, selecione o catálogo compartilhado para o qual deseja exibir o relatório.
1. Clique em [!UICONTROL **Salvar**].

   ![](assets/acc2.png)
   *Selecionar Catálogo Compartilhado para conta entre parceiros*

1. Depois de clicar em **[!UICONTROL Salvar]**, você pode exibir a representação gráfica de seus relatórios no painel padrão. Nesse painel, você pode filtrar ainda mais o relatório do gerente para a conta entre parceiros específica.
1. Se houver alterações no catálogo do seu lado, as alterações serão refletidas imediatamente nos relatórios e no painel gerado pelo parceiro. No entanto, quando o item de mesmo nível modifica o catálogo, as alterações não aparecem no painel automaticamente.
1. Se você quiser que seu painel seja atualizado automaticamente, seu parceiro deverá enviar uma nova solicitação de parceiro para você.

   >[!NOTE]
   >
   >Os gerentes não podem exibir relatórios de colegas.

## Assinaturas de email {#emailsubscriptions}

Você pode obter seus relatórios favoritos em um email assinando-os.

Entrada **[!UICONTROL Relatórios]** clique no botão  **[!UICONTROL Assinatura]** guia. A página de assinatura Relatórios é exibida.

Para selecionar o nome do relatório na lista suspensa, comece a digitar o nome do relatório no campo Relatórios. Escolha a frequência de e-mails na lista suspensa. Você pode adicionar o assunto do email e fornecer uma ID de email alternativa.

Você pode Editar e Excluir assinaturas.

## Relatórios do Excel {#excelreports}

O **[!UICONTROL Relatórios do Excel]** permite exportar relatórios no formato de arquivo XLS.

Veja a seguir os tipos de relatório disponíveis para download.

* Relatórios do curso
* Transcrições do aluno
* Relatório de comunicados
* Relatório de ajudas de tarefa
* Registro de auditoria do conteúdo
* Registro de auditoria do usuário
* Relatório de login/ acesso
* Transcrições de gamificação

## Transcrições do aluno {#learnertranscripts}

As transcrições do aluno nos relatórios do Excel exibem as colunas Créditos necessários e Créditos obtidos em números decimais.

## Relatórios do curso {#coursereports}

Como administrador, você pode baixar relatórios de cursos. Siga estas etapas:

1. Abrir **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Relatórios do curso]**.
1. O **[!UICONTROL Relatório do curso]** é exibida. Selecione o curso do qual deseja obter o relatório e clique em **[!UICONTROL Mostrar]**.

   ![](assets/course-reports.png)
   *Relatórios do curso*

1. Você é redirecionado para a página do curso. Você pode exportar a pontuação do quiz por usuário e por pergunta com base em cada inscrição escolhendo o tipo de inscrição específico.
1. Selecionar **[!UICONTROL Exportar pontuação do quiz]** para exportar o relatório. A **[!UICONTROL Gerando solicitação de relatório]** é exibida. Clique em **[!UICONTROL OK]** para confirmar.

   ![](assets/generating-reportrequest.png)
   *Gerando solicitação de relatório*

   >[!NOTE]
   >
   >O relatório de pontuação do quiz exportado conterá os detalhes de pontuação de cada tentativa se a opção de várias tentativas estiver configurada para o módulo.

## Transcrições do aluno {#LearnerTranscripts-1}

O Adobe Learning Manager permite que os administradores de uma empresa gerem transcrições associadas aos alunos. O relatório de transcrição do aluno contém o seguinte:

1. Transcrição do aluno: Painel da atividade de aprendizado
1. Habilidade: painel de habilidade
1. Painel de Conformidade

As transcrições do aluno nos relatórios do Excel exibem as colunas Créditos necessários e Créditos obtidos em números decimais.

Para obter informações sobre a geração de relatórios das transcrições dos alunos e mais informações, consulte [Transcrições do aluno](learner-transcripts.md).

## Relatórios de comunicados {#announcementsreports}

Como administrador, você pode gerar um relatório de todos os comunicados enviados. O relatório contém detalhes sobre:

* Tipo de anúncio
* Nome do anúncio
* Data do anúncio
* Estado do comunicado
* Nome do aluno

Para baixar um relatório, siga uma destas etapas:

1. Abrir **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Relatório de comunicados]**. O **[!UICONTROL Gerando solicitação de relatório]** é aberta. Clique em Ok.
1. [!UICONTROL **Comunicados**] > [!UICONTROL **Ações**] > [!UICONTROL **Exportar relatório**].

   ![](assets/announcements.png)
   *Relatório de comunicados*

1. Você pode extrair um relatório para um comunicado específico clicando em Exportar relatório no ícone de configurações.

   ![](assets/announcements-specific-report.png)
   *Relatório de anúncios específicos*

## Relatório de ajudas de tarefa {#jobaidsreport}

Ajudas de tarefa são conteúdos de treinamento que um aluno pode acessar sem ter de se inscrever em qualquer objeto de aprendizado específico, como um curso ou programa de aprendizado. Os administradores podem extrair e baixar o relatório de ajudas de tarefa.

O relatório extraído inclui informações sobre o seguinte:

* Nome
* Tipo de ajuda de tarefa
* State of Job Aid (publicado ou retirado)
* Data de inscrição
* Data de conclusão
* Data do download
* Nome do aluno
* Nome do gerente
* Criado por

Para baixar um relatório, siga um destes procedimentos:

* Abrir  **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Relatórios de ajuda de tarefa]**. O **[!UICONTROL Gerando solicitação de relatório]** é exibida. Clique em **[!UICONTROL Ok]**.
* Abrir **[!UICONTROL Ajuda de tarefa]** > **[!UICONTROL Ações]** > **[!UICONTROL Exportar relatório]**.

![](assets/job-aids.png)
*Relatório de ajudas de tarefa*

* Você também pode extrair um relatório para uma ajuda de tarefa específica clicando em **[!UICONTROL Exportar relatório]** no ícone configurações.

![](assets/job-aid-specific-download.png)
*Relatório de ajuda de tarefa específica*

### Relatório de ajudas de tarefa

Depois de selecionar **[!UICONTROL Relatório de ajudas de tarefa]** na lista, você verá duas opções:

![relatório de ajudas de tarefa](assets/job-aids-new.png)
*Baixar Relatório de Inscrição de Usuários de Ajudas de Tarefa*

**Todas as ajudas de tarefa**: se o número de ajudas de tarefa na conta for inferior a 10 milhões, o relatório gerado conterá informações de inscrição de todas as ajudas de tarefa. Essa será a seleção padrão. Se o número de linhas exceder 10 milhões, será exibido um erro, e você deverá selecionar manualmente as ajudas de tarefa necessárias.

**Ajudas de tarefa selecionadas**: Se você selecionar essa opção, poderá informar as ajudas de tarefa para as quais deseja gerar o relatório. Você pode selecionar no máximo 10 ajudas de tarefa. O Adobe Learning Manager verifica se o número de ajudas de tarefa excede 10 milhões.

![inscrição no relatório de ajudas de tarefa](assets/job-aids-2-new.png)
*Selecionar uma ajuda de tarefa*

**Relatório de ajudas de tarefa**

Se você selecionar essa opção, os detalhes de todas as ajudas de tarefa presentes no sistema, juntamente com seus metadados e treinamento, serão baixados.

O relatório baixado consiste nos seguintes campos:

* Nome da ajuda de tarefa
* Idioma(s)
* ID
* Tipo
* Duração (minutos)
* Estado
* Data de publicação (Fuso horário UTC)
* Criado por Nome
* Criado por Email
* Criado por ID exclusiva do usuário
* Catálogo(s)
* Caminho(s) de aprendizado
* Curso(s)
* Etiqueta(s)
* Habilidade(s)

**Relatório de inscrição do usuário de ajudas de tarefa**

O relatório de inscrição contém detalhes sobre a inscrição de usuários e outras informações.

O relatório baixado consiste nos seguintes campos:

* Nome da ajuda de tarefa
* Tipo
* Estado
* Data de inscrição (fuso horário UTC)
* Data de conclusão (fuso horário UTC)
* Data do download (fuso horário UTC)
* Nome do aluno
* E-mail
* ID exclusiva do usuário
* Nome do Gerente
* E-mail do gerente
* ID Exclusiva do Usuário Gerente
* Atribuído por nome
* Atribuído por Email
* Atribuído por ID exclusiva do usuário
* Criado por nome
* Criado por Email
* Criado por ID exclusiva do usuário
* Código de Trabalho
* Novo campo
* Perfil

### Relatórios de trilha de auditoria de conteúdo {#contentaudittrailreports}

Use o **[!UICONTROL Registro de auditoria do conteúdo]** gerador de relatórios para gerar um relatório de todas as alterações e edições feitas em um curso durante sua vida útil no sistema. O relatório gerado tem as seguintes informações buscadas.

* ID do objeto
* Nome do objeto
* Tipo de objeto
* Tipo de modificação
* Descrição
* ID do objeto referenciado
* Nome do objeto referenciado
* Modificado por nome de usuário
* Modificado por ID de usuário
* Data da modificação (fuso horário UTC)

As informações relacionadas aos metadados não são buscadas no relatório gerado.

Para gerar um relatório de auditoria da trilha do curso, siga estas etapas.

1. Selecionar **[!UICONTROL Denunciar]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Trilha de auditoria do curso]**. O **[!UICONTROL Registro de auditoria do conteúdo]** é exibida.

   ![](assets/course-audit-trial.png)
   *Trilha de auditoria do curso*

1. Selecione o curso, o programa de aprendizado e a certificação de que deseja baixar o relatório. Se não for especificado, todos os relatórios serão baixados por padrão.
1. Selecione um intervalo de datas para o relatório e clique em **[!UICONTROL Gerar]**.
1. O relatório é gerado e você é notificado de que o relatório de auditoria de conteúdo está pronto. Você pode baixar o relatório.

## Relatórios de trilha de auditoria do usuário {#useraudittrailreports}

A trilha de auditoria do usuário captura o ciclo de vida de usuários, grupos de usuários e perfis de autorregistro. Adição de usuário, exclusão, alteração no Gerenciador, são todas capturadas. A criação e a exclusão de perfis de autorregistro são registradas. Você também pode pausar e retomar o autorregistro.

Você pode Adicionar, Ativar, Desativar, Pausar ou Retomar para perfis externos enquanto pode Adicionar, Excluir, Pausar ou Retomar para autorregistro. Os uploads de CSV também são capturados.

1. Selecionar  **[!UICONTROL Relatório > Relatório do Excel > Trilha do usuário]**. A caixa de diálogo Registro de auditoria do usuário é exibida.
1. A caixa de diálogo Registro de auditoria do usuário é exibida. Selecione o intervalo de datas no menu pop-up. Você pode optar por gerar o relatório da última semana, do último mês ou selecionar uma data personalizada.

   ![](assets/user-audit-trail.png)
   *Trilha de auditoria do usuário*

1. Clique em **[!UICONTROL Gerar]** para gerar o relatório.

Há dois filtros na **[!UICONTROL Relatório de registro de auditoria do usuário]** diálogo.

**Filtro de classificação por data:** Escolha a faixa de datas para a qual deseja gerar o relatório. Há três opções:

* Última semana
* Último mês
* Data personalizada

Selecione o filtro Alunos: pesquise um usuário ou um grupo de usuários.

O relatório exportado conterá dados dos usuários que atenderem aos critérios de pesquisa especificados.

![](assets/user-audit-trail.png)
*Trilha de auditoria do usuário*

>[!NOTE]
>
>Quando uma habilidade é atribuída ou removida, ela pode ser rastreada para o Relatório de auditoria do usuário para ambas atribuídas ou removidas.

## Relatórios de gamificação {#gamification}

Os administradores podem baixar a transcrição de gamificação no formato CSV. Você pode baixar o relatório para usuários individuais ou grupos de usuários. Nome do usuário, email do usuário, UUID do usuário, total de pontos do usuário pontuados, divisão de pontos coletados, nome dos grupos que o usuário joga, nome do gerente e valores de campo ativos são todos obtidos no relatório. Os administradores podem usar esse relatório para avaliar e entender as classificações de usuário no nível da organização ou de um grupo específico.

1. Selecione Relatório > Relatório do Excel > Relatório de gamificação.

   ![](assets/gamification.png)
   *Relatório de gamificação*

1. A caixa de diálogo Transcrições de gamificação é exibida. Selecione os alunos usando seu nome, perfil, grupos de usuários, ID de e-mail ou UUID.

   ![](assets/gamification-transcriptsdialog.png)
   *Caixa de diálogo Transcrições de gamificação*

1. Clique em  **[!UICONTROL Gerar]** para gerar o relatório.

   Depois de gerar o relatório de um aluno, você deve ser capaz de exportar as informações atuais e de nível alcançado para todos os usuários (internos, externos ou excluídos) na conta. Você também pode verificar as datas dos níveis obtidos por um aluno:

   * Data de obtenção do bronze
   * Data da Prata Obtida
   * Data da obtenção do ouro
   * Data da obtenção do Platinum

   Estas colunas contêm as datas em que o nível foi alcançado na primeira vez. A coluna **[!UICONTROL Nível atual]** exibe o nível atual do aluno.

   Quando o administrador redefine a gamificação, todos os pontos do aluno são redefinidos de acordo.

## Relatório de Inscrição e Cancelamento de Inscrição {#enrollmentandunenrollmentreport}

Os administradores e gerentes podem extrair um relatório dos alunos que foram inscritos e cancelados. Como administrador, você pode ver qualquer aluno, administrador ou gerente que tenha sido inscrito ou cancelado em uma instância de um curso, programa de aprendizado ou certificação e exportar o relatório. Enquanto gerente, você só pode obter um relatório dos membros da sua equipe. Como gerente, você não pode ver os alunos excluídos ou seu próprio nome no aplicativo do gerente como um aluno inscrito ou não inscrito.

Para baixar um relatório, siga estas etapas: Abrir o  **[!UICONTROL Curso/Programa de aprendizado/Certificação]** > **[!UICONTROL Alunos]** > **[!UICONTROL Ação]** > **[!UICONTROL Exportar relatório]**.

![](assets/unenrollment.png)
*Relatório de cancelamento de inscrição*

## Relatório de feedback {#feedback-report}

Como administrador, agora você pode buscar feedback do aluno (L1) e feedback do gerente (L3) para treinamentos selecionados por um período especificado.

Você pode exportar os dados da interface do usuário ou por meio do conector PowerBI para uma análise mais detalhada.

Os relatórios de feedback L1 e L3 oferecem uma opção de download de um relatório de feedback consolidado para as respostas L1 e L3 para treinamentos selecionados para um **um ano** ou até 10 treinamentos selecionados para qualquer período.

Faça logon como administrador e clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** e, na lista de relatórios, clique em **[!UICONTROL Relatório de feedback]**.

![](assets/download-feedbackreport.png)
*Baixar relatório de feedback*

Ao clicar em Baixar após selecionar os filtros, você receberá uma notificação para baixar o relatório no formato CSV.

O relatório baixado terá detalhes como nome e tipo do treinamento, nome da instância, nome do aluno e e-mail, tipo de feedback: L1 ou L3, datas do feedback enviado para novos dados.

Para os dados existentes antes da implementação desse recurso, a data de conclusão do OA será exibida, a data de conclusão do OA, o texto real do Ritmo do próprio comentário da pergunta L1 e o Texto da sala de aula em colunas diferentes, as respectivas respostas do Feedback L1, o nome do gerente e o email, o valor do feedback L3 e a data de envio, os Campos ativos.

Você também pode exportar os dados da interface do usuário ou para o Power BI, que oferece suporte a todos os treinamentos para qualquer período para uma análise mais aprofundada.

## Relatório de treinamentos {#training-report}

O Learning Manager é compatível com o Relatório de treinamento, que permite que os administradores baixem detalhes de treinamento e seus metadados associados, como autor, data de publicação, habilidades, etiquetas do catálogo etc.

No aplicativo de administração, clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Relatório de treinamentos]**.

Você pode baixar relatórios para o seguinte:

* Treinamentos selecionados (10 no limite) - Seleciona um ou vários treinamentos (até 10) de qualquer catálogo.
* Os treinamentos no catálogo selecionado (5 no limite) - (a seleção do catálogo estará disponível para até cinco catálogos)
* Todos os treinamentos - (todos os treinamentos na conta)

![](assets/download-trainingreport.png)
*Baixar relatório de treinamento*

Na seção Opções avançadas, as seguintes opções estão disponíveis:

* Incluir mapeamentos de cursos com programa de aprendizado/certificação
* Incluir informações de nível de módulo

Depois de selecionar os filtros e clicar em Baixar, você receberá uma notificação para baixar o relatório no formato CSV.

O relatório terá os seguintes campos:

*Nome do catálogo, Tipo de treinamento, ID do treinamento, ID exclusiva de treinamento, Nome do treinamento, Subtreinamentos, Módulos, Duração do módulo ou treinamento, Formato, Status do treinamento, Habilidades, Autor, Última data de publicação, Última data de conclusão, Contagem de inscrição dos professores, Contagem de início, Contagem de conclusão, Pontuação L1 média, Pontuação L2 média, Pontuação L3 média, Respostas L1 recebidas, Respostas L2 recebidas, Respostas L3 recebidas, Etiquetas do catálogo e Tags.*

![](assets/more-options.png)
*Opções adicionais*

## Relatório de resumo da sessão

O Relatório de resumo da sessão contém todas as sessões planejadas para um aluno em uma data especificada.

Isso permite que o administrador exporte todos os detalhes da sessão de sala de aula e virtual que estão no intervalo de datas especificado. O administrador também pode exportar o relatório de sessão em relação a treinamentos ou professores específicos.

Isso também ajudará o administrador a entender as sessões planejadas mensalmente e identificar a agenda dos professores e as sessões já entregues.

Como administrador, clique em **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatório de resumo da sessão]**.

Na caixa de diálogo a seguir, escolha o intervalo de datas e o treinamento ou o professor para obter um resumo.

![](assets/session-summary-report.png)
*Relatório de resumo da sessão*

O csv baixado contém os seguintes campos:

* Data e hora de início
* Data e hora final

* Nome do módulo
* Duração da sessão (em minutos)
* Contagem de vagas
* Localização
* Nome da Instância

* Nome do curso
* ID do curso
* Nome do professor
* Email do professor
* Contagem de inscrições

* Tipo de sessão
* Limite da Lista de Espera
* Contagem de listas de espera
* Emails de usuário da lista de espera

## Relatório de Utilização do Professor

Esse relatório captura o tempo (em minutos) gasto diariamente por um professor ensinando sessões atribuídas. O relatório pode ser baixado por um período de três meses a partir da data de início selecionada.

Para baixar o relatório, clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatório de Utilização do Professor]**.

Selecione um ou vários professores e o intervalo de datas.

![Baixar Relatório de Utilização de Professor](assets/utilization-report.png)
*Baixar Relatório de Utilização de Professor*

O relatório baixado contém os seguintes campos:

* Nome do professor
* ID do professor
* Nível de competência
* Datas como colunas. Se o professor for utilizado em uma data, o número de sessões será listado. Se o professor não for utilizado em um dia, o valor exibe zero.

O relatório contém registros de três meses do mês selecionado.

Para recuperar registros de todos os professores, deixe o campo Professor em branco.

Além disso, um administrador personalizado com permissão para gerar relatórios pode recuperar esse relatório.

## Relatório de registro de auditoria do usuário

Este relatório captura informações sobre os alunos que alternaram instâncias, “de instância” para “para instância”, alternados por hora, data etc.

Selecione os alunos ou um grupo de usuários.

Para baixar o relatório, clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatório de registro de auditoria do usuário]**.

![Baixar relatório de registro de auditoria do usuário](assets/user-audit-report.png)

*Baixar relatório de registro de auditoria do usuário*

## Relatório do plano de aprendizado

Esse relatório contém detalhes de todos os planos de aprendizado em uma conta, por exemplo, grupos de usuários relacionados, status e informações de acionador.

O relatório contém o seguinte:

* Nome do plano de aprendizado
* Tipo (ocorre quando)
* Treinamento (concluído)
* Habilidade (obtida)
* Data (na data)
* Ação
* Status, criado por
* Data de criação
* Data da última modificação
* Grupo de usuários (aplica-se a)
* Grupo de usuários (adicionar a)
* Inscrever-se após
* Tipo(s) de elemento de aprendizagem
* Elemento(s) de aprendizagem
* Instância(s) do elemento de aprendizado
* Elemento de aprendizado
* Data de conclusão
* Lembrete do elemento de aprendizado
* Scope-Catalog
* Scope-Usergroup

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como compartilhar um painel personalizado com um gerente?

Ao criar um painel, insira o nome e a descrição. Para compartilhar com gerentes, insira o nome do gerente na caixa **[!UICONTROL Compartilhar com]** campo.

![](assets/share-dashboard-manager.png)
*Compartilhar um painel*
+++
