---
description: Saiba mais sobre os relatórios associados à função de administrador no aplicativo Learning Manager.
jcr-language: en_us
title: Relatórios
contentowner: manochan
exl-id: 31b176b7-4b8f-4851-a0c5-4eee58bceb41
source-git-commit: f6bc1fa9384fc728f6abca7bb0fd9f62bb1f9e04
workflow-type: tm+mt
source-wordcount: '7809'
ht-degree: 52%

---

# Relatórios

Saiba mais sobre os relatórios associados à função de administrador no aplicativo Learning Manager.

O Adobe Learning Manager lhe permite criar relatórios variados para acompanhar, monitorar e gerenciar as atividades do Aluno. As atividades dos Alunos são acompanhadas e capturadas automaticamente no banco de dados. Os relatórios de Gerente e Administrador são gerados a partir do banco de dados.

## Visão geral {#overview}

O processo de geração de relatórios é o semelhante para o administrador e para o gerente. Os Gerentes podem ver os relatórios que correspondem aos seus subordinados enquanto que o Administrador pode vir todos os relatórios no âmbito da organização.

Os relatórios são agregados em um painel. Um relatório deve existir dentro de um painel. Um **[!UICONTROL Painel Padrão]** existe por padrão na página de relatórios. Qualquer relatório adicionado por você é movido para este painel padrão. Para adicionar relatórios a painéis individuais, use a seta suspensa e escolha **[!UICONTROL Adicionar Relatório]**. Para obter mais informações sobre como criar painéis, consulte a seção Painéis nesta página.

## Tipos de relatórios {#typesofreports}

O Adobe Learning Manager é compatível com quatro tipos principais de relatório, por exemplo, conclusão, tempo gasto, habilidades e eficácia. Você pode usar os seguintes tipos de relatório para gerar relatórios de mais de 300 variações:

* Estatísticas de entrega do curso para Alunos
* Relatório da eficácia dos cursos
* Relatório baseado na habilidade do aluno
* Estatísticas de inscrição no programa de aprendizado para Alunos
* Tempo gasto no aprendizado pelos Alunos
* Pontuação do aluno
* Conclusão da certificação

## Painéis de atividades do usuário {#useractivitydashboards}

Veja um resumo de todas as atividades do usuário na plataforma ao longo do tempo. Configure grupos de usuários e aplique filtros.

O painel de atividades do usuário exibe a atividade dos usuários na conta. Os três relatórios listados são:

* **Usuários Registrados:** este relatório fornece informações sobre o número de usuários registrados em sua conta, semana após semana. Para contas com licenciamento de unidades ativas mensais, o relatório mostra as unidades do MAU.

* **Relatório de Visitas do Usuário:** este relatório fornece informações sobre o número de usuários que acessam a plataforma diariamente. O relatório mensal também está disponível.

* **Relatório de Tempo Gasto no Aprendizado:** este relatório fornece informações sobre o Tempo Gasto no Aprendizado na plataforma diariamente. O relatório mensal também está disponível.

### Usuários registrados {#registeredusers}

O Learning Manager registra o número de usuários registrados no sistema todas as semanas. Os administradores podem visualizar este relatório para entender a contagem de usuários registrados naquele dia da semana. Uma vez armazenada por uma semana, a contagem registrada não se altera. Portanto, a contagem histórica registrada não está relacionada ao conjunto atual de alunos no sistema.

Este relatório fornece informações sobre o número de usuários registrados em sua conta, semana após semana.

Para contas com licenciamento de unidades ativas mensais, o relatório mostra as unidades do MAU.

![](assets/registered-usersreport.png)
*Relatório de usuários registrados*

***Para contas da unidade de acesso mensal:***

**Relatório mensal de usuários ativos**

Este relatório mostra a contagem de alunos ativos na plataforma de aprendizado todos os meses. O usuário é considerado ativo para o mês se executar alguma das ações de aprendizado mencionadas aqui. As unidades ativas mensais são contadas dessa forma.

A contagem mensal ativa, uma vez contada e armazenada por um mês, não se altera. Portanto, a contagem histórica exibida não está relacionada ao conjunto atual de alunos no sistema.

### Visitas do usuário {#uservisits}

Este relatório mostra o total de alunos acessando o sistema diária ou mensalmente. Navegar na plataforma de aprendizado sem realizar nenhum aprendizado também é considerado como &#39;acessar&#39; a plataforma de aprendizado. Isso ajuda o administrador a entender o conjunto total de usuários acessando o sistema. No primeiro dia do mês, o Learning Manager cria um registro do total de usuários acessando a plataforma no mês anterior. Ele também captura as informações do grupo de usuários para esses usuários.

Somente os grupos de usuários configurados pelo administrador são registrados. Isso permite que os administradores apliquem filtros em grupos de usuários para dados históricos mensais também. Observe que a configuração do caso de grupos de usuários é modificada e o Learning Manager não registrou dados para esse grupo de usuários nos meses anteriores; então, o Learning Manager não pode exibir os dados para esses grupos de usuários recém-configurados nos meses anteriores.

Este relatório contém usuários que acessam a plataforma usando todos os formatos, como a Web, aplicativos para dispositivos móveis, soluções personalizadas sem cabeçalho e assim por diante. O gráfico de uso do aplicativo de dispositivo menciona especificamente apenas os usuários que acessam a plataforma usando o aplicativo do dispositivo do Learning Manager. Isso ajuda os administradores a identificar o uso do aplicativo móvel em suas contas

![](assets/user-visit-report.png)
*Relatório de visita do usuário*

### Relatório de tempo gasto no aprendizado {#learningtimespentreport}

Aqui, você pode ver um gráfico de linhas de eixo duplo que mostra o tempo total gasto no aprendizado para todos os alunos em um período de 12 meses. O segundo eixo representa o tempo mediano gasto no aprendizado para um indivíduo.

O tempo gasto para diferentes objetos de aprendizado, como programas e certificações de aprendizado, é calculado para o seguinte:

* Curso em um ritmo individualizado com conteúdo estático e interativo
* Cursos de atividade com URL.
* Sessões de fim de semana com o sinalizador de fim de semana habilitado.
* Sessão de conexão da VC na qual a presença é marcada automaticamente.
* O tempo gasto em diferentes objetos de aprendizado, como programas e certificações de aprendizado
* Instruções xAPI para um curso de atividade xAPI.

Você pode exportar o gráfico como uma planilha do Excel.

É fornecido um filtro para escolher a configuração do grupo de usuários, o que ajudará na visualização dos dados em relação a diferentes grupos de usuários.

A data selecionada e o filtro do grupo de usuários são aplicados a todos os gráficos relevantes no painel.

>[!NOTE]
>
>Para as **[!UICONTROL Visitas do usuário]** e o **[!UICONTROL Tempo gasto no aprendizado]** os dados padrão (quando nenhum grupo de usuários está configurado) exibidos serão para toda a conta.

## Painel de conteúdo de treinamento {#trainingcontentdashboard}

O painel de conteúdo de treinamento oferece informações sobre os treinamentos disponíveis na plataforma. Você pode visualizar treinamentos populares ou acompanhar todos os treinamentos disponíveis.

### Relatórios de treinamento {#trainingsreport}

Este relatório fornece informações do total de treinamentos disponíveis na plataforma (no estado publicado) mês a mês. Ele fornece uma indicação do número de treinamentos oferecidos ao longo do tempo.

![](assets/training-report.png)
*Relatório de treinamento*

### Relatório de treinamentos ativos {#activetrainingsreport}

Este relatório fornece informações sobre os treinamentos ativos no intervalo de tempo selecionado. Treinamentos ativos são treinamentos registrados, visualizados no reprodutor ou concluídos no tempo determinado.

Para treinamentos ativos, os dados de todos os grupos internos de usuários raiz (com função de gerente) estarão disponíveis para seleção quando nenhuma configuração de grupo de usuários for feita. Além dos grupos de usuários raiz, você pode configurar mais 10 grupos de usuários, se necessário.

![](assets/active-trainingsreport.png)
*Relatório de treinamentos ativos*

>[!NOTE]
>
>Os dados não são exibidos conforme esperado quando os filtros **[!UICONTROL Todos os Usuários]** e **[!UICONTROL 12 meses]** são selecionados, mas os dados são exibidos quando você seleciona **[!UICONTROL Todos os grupos de usuários internos].**

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
    <p>Taxa de início (%)</p></td>
   <td>
    <p>Proporção do número de alunos que iniciaram o curso e do número de matrículas.</p></td>
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
    <p>Média de todas as respostas de feedback L3 recebidas em uma escala de 1 a 5, arredondadas até o número inteiro mais próximo.<br></p></td>
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

## Painéis de resumo do aprendizado {#dashboards}

### Gerar Relatórios do Painel

>[!INFO]
>
>Neste treinamento, você aprenderá a gerar relatórios do painel a partir do banco de dados.<br><br>[![botão](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318854)</br></br>


Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

Veja um relatório resumido de todas as atividades de aprendizado na plataforma. Nesta página, você pode ver as seguintes informações de resumo para a equipe do usuário raiz selecionado e seus perfis externos. O intervalo de tempo também pode ser selecionado:

* Resumo do aprendizado na forma de Inscrições, Exibições e Conclusões
* Principais habilidades
* Resumo de conformidade

![](assets/summary-charts.png)
*Gráficos de resumo*

Se houver gerenciadores de nível raiz internos, eles serão exibidos um após o outro.

Todos os perfis externos serão listados após os perfis internos (usuários internos de nível raiz).

Se um perfil externo tiver um gerente, a hierarquia do gerente será exibida na lista suspensa **[!UICONTROL Mostrando Dados para]**. O usuário será listado na hierarquia do gerente em todas as páginas de detalhes (resumo do aprendizado, conformidade e status da habilidade)

Caso contrário, todos os detalhes de usuário individuais serão exibidos na lista.

Para ver detalhes mais granulares das inscrições de várias equipes internas, clique em **[!UICONTROL Detalhes do Resumo do Aprendizado]**.

![](assets/learning-sunnarydetails.png)
*Detalhes do Resumo do Aprendizado*

Ao clicar em qualquer inscrição, você pode ver os alunos de cada gerente e a inscrição em quais objetos de aprendizado. Você também pode ver os detalhes de andamento e conclusão de cada aluno.

![](assets/learners-for-a-manager.png)
*alunos atribuídos a um gerente*

Clique em qualquer equipe e exporte seu relatório como CSV. Um administrador pode exportar o relatório de qualquer grupo de usuários ou usuário individual selecionando o grupo de usuários ou usuário individual e, em seguida, exportar detalhes da lista suspensa **[!UICONTROL Ação]**.

Além disso, você pode ver um gráfico de barras que mostra as habilidades que estão em andamento e foram obtidas. Você pode adicionar/remover habilidades que deseja destacar no gráfico.

![](assets/skill-status-stackedbarchart.png)
*Gráfico de barras empilhadas do status da habilidade*

### Painel de conformidade

O **Adobe Learning Manager** oferece um painel de conformidade para todos os administradores e gerentes. Os administradores podem criar um painel de conformidade e compartilhá-lo com os gerentes. Os gerentes poderão visualizar o painel recém-compartilhado em seu aplicativo e controlar facilmente a conformidade dos membros da equipe para um treinamento específico. O painel de conformidade permite que os administradores categorizem cursos de conformidade personalizados em categorias específicas (por exemplo, Vendas, Marketing e Jurídico). As categorias de conformidade personalizadas são viabilizadas por **[!UICONTROL Etiquetas de catálogo]**.

![](assets/compliance-dashboard-admin.png)

_Exibição do administrador do painel de conformidade_

Os administradores também podem verificar o status de conformidade de cada equipe de gerente selecionando **[!UICONTROL Ir para o painel de Conformidade]**. Os administradores podem compartilhar um conjunto de cursos de treinamento com gerentes individualmente ou com um grupo. Isso ajuda os gerentes a controlar facilmente a conformidade de seus colegas de equipe para o treinamento especificado.

#### Fluxo de trabalho do administrador

##### Criar rótulos de conformidade personalizados

Um rótulo de conformidade é um tipo de rótulo de catálogo que categoriza cursos/programações de aprendizado/certificações como um tipo de conformidade.
Para criar um rótulo de conformidade personalizado, siga estas etapas:

1. No aplicativo do administrador, vá para **[!UICONTROL Configurações]** > **[!UICONTROL Geral]**.
1. Selecione a opção **[!UICONTROL Tipo de Conformidade Personalizada]** para habilitar o rótulo de conformidade personalizado.


   ![](assets/custom-compliance.png)
   _Habilitar Conformidade Personalizada_

   >[!NOTE]
   >
   >Esse novo rótulo de catálogo foi introduzido para categorizar os cursos, programações de aprendizado e certificações como um tipo de conformidade. Para habilitar a opção **[!UICONTROL Conformidade Personalizada]**, primeiro você deve habilitar a opção **[!UICONTROL Mostrar Etiqueta de Catálogo]** na mesma página.

1. Vá para **[!UICONTROL Configurações]** > **[!UICONTROL Etiqueta de catálogo]** e selecione o **[!UICONTROL Tipo de conformidade]**.
1. Digite os valores (por exemplo, Legal, Vendas) na caixa de texto **[!UICONTROL Valor]** e selecione **[!UICONTROL Adicionar Valor]**.

   ![](assets/custom-compliance-values.png)
   _Adicionar valores para Conformidade Personalizada_

1. Selecione **[!UICONTROL Salvar]**.

>[!NOTE]
>
>O autor deve adicionar esses rótulos de conformidade ao criar/editar os cursos em seu aplicativo. Consulte [Adicionar rótulos de conformidade a um curso/caminho de aprendizado/certificação](/help/migrated/authors/feature-summary/courses.md#add-compliance-labels-to-courselearning-pathcertification).

##### Criar e compartilhar um painel de conformidade

Para criar e compartilhar um painel de conformidade, siga estas etapas:

1. Vá para **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]**.
1. Na seção **[!UICONTROL Painel de Conformidade]**, selecione **[!UICONTROL Compartilhado com Gerentes]**.
1. Selecione **[!UICONTROL Compartilhar painel]** e selecione os rótulos criados no menu suspenso **[!UICONTROL Selecionar Rótulo de Conformidade]**.


   ![](assets/compliance-type.png)
   _Selecione o tipo de Conformidade_

1. Digite e selecione o nome do gerente na caixa de texto **[!UICONTROL Compartilhar com]**.
1. Selecione **[!UICONTROL Compartilhar]** para enviar o painel para o gerente selecionado.

>[!NOTE]
>
>Compartilhar o novo painel substituirá o painel existente no aplicativo do gerente selecionado. Os gerentes poderão exibir o painel recém-compartilhado pelos administradores.

#### Compartilhar o painel de conformidade com administradores e administradores personalizados

Os administradores podem compartilhar o painel com outros administradores e administradores personalizados, dando a eles acesso instantâneo a todos os painéis de conformidade.

Siga estas etapas para compartilhar o painel com administradores e administradores personalizados:

1. Faça logon como **[!UICONTROL Administrador]**.
2. Navegue até **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]**.
3. Selecione **[!UICONTROL Exibição do Administrador]** na seção **[!UICONTROL Painel de Conformidade]**.
4. Selecione o botão **[!UICONTROL Compartilhar Painel]**.

   ![](assets/share-dashboard.png)
   _Compartilhar painel - Administrador_

5. Selecione os rótulos de conformidade no menu suspenso **[!UICONTROL Selecionar conformidade personalizada]**. Essa opção selecionará todos os cursos com os rótulos de conformidade selecionados.
6. Selecione os cursos adicionais, programações de aprendizado ou certificações que deseja compartilhar com administradores.

   ![](assets/share-button.png)
   _Compartilhar painel de conformidade_

7. Selecione os usuários ou grupos de usuários que deseja compartilhar o painel e selecione **[!UICONTROL Compartilhar]**.

##### Exibir o painel de conformidade - Administradores personalizados e outros administradores

Todos os administradores personalizados e outros administradores do grupo de usuários selecionado podem ver o painel de conformidade em seu aplicativo.

Siga estas etapas para exibir o painel de conformidade:

1. Navegue até o **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]** > **[!UICONTROL Painel de conformidade]**.
2. Selecione **[!UICONTROL Sua Exibição]** na seção **[!UICONTROL Painel de Conformidade]**.
3. Selecione a opção **[!UICONTROL Ir para o Painel de Conformidade]** e você poderá ver o novo painel de conformidade compartilhado pelo administrador.

   ![](assets/compliance-custom-view.png)
   _Exibir o painel de conformidade - Administrador personalizado_

#### Compartilhar com gerentes de loja

Os administradores podem compartilhar o painel de conformidade com os gerentes de loja, o que permite que eles monitorem o progresso de conformidade do aluno.

Siga estas etapas para compartilhar o painel com gerentes de loja:

1. Faça logon como **[!UICONTROL Administrador]**.
2. Navegue até o **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]** > **[!UICONTROL Painel de conformidade]**.
3. Selecione **[!UICONTROL Exibição do Gerente]** na seção **[!UICONTROL Painel de Conformidade]**.
4. Selecione o botão **[!UICONTROL Compartilhar Painel]**.

   ![](assets/share-manager.png)
   _Compartilhar o painel de conformidade com Gerentes_

5. Selecione os rótulos de conformidade no menu suspenso **[!UICONTROL Selecionar conformidade personalizada]**.
Essa opção selecionará todos os cursos com os rótulos de conformidade selecionados.
6. Selecione os cursos adicionais, programações de aprendizado ou certificações que deseja compartilhar com administradores.
7. Selecione os usuários ou grupos de usuários que deseja compartilhar o painel e selecione **[!UICONTROL Compartilhar]**.

##### Exibir o painel de conformidade - Gerente

Consulte este artigo [Exibir o painel de conformidade](/help/migrated/managers/feature-summary/manager-dashboard.md#view-the-dashboard) para obter mais informações.

#### Editar o painel

Siga estas etapas para editar o painel de conformidade:

1. Faça logon como **[!UICONTROL Administrador]**.
2. Navegue até o **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]** > **[!UICONTROL Painel de conformidade]**.
3. Selecione **[!UICONTROL Exibição do Administrador]** ou **[!UICONTROL Exibição do Gerente]** na seção **[!UICONTROL Painel de Conformidade]**. Você pode ver os painéis de conformidade nesta seção.
4. Selecione **[!UICONTROL Editar]** no painel de conformidade que você deseja editar.

   ![](assets/edit.png)
   _Editar o painel de conformidade_

5. Altere os detalhes necessários e selecione **[!UICONTROL Compartilhar]**.
6. O painel de conformidade será compartilhado com os gerentes selecionados.

#### Retirar o painel - Administrador

Siga estas etapas para retirar o painel de conformidade:

1. Faça logon como **[!UICONTROL Administrador]**.
2. Navegue até o **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]** > **[!UICONTROL Painel de conformidade]**.
3. Selecione **[!UICONTROL Exibição do Administrador]** ou **[!UICONTROL Exibição do Gerente]** na seção **[!UICONTROL Painel de Conformidade]**. Você pode ver os painéis de conformidade nesta seção.
4. Selecione **[!UICONTROL Retirar]** no painel de conformidade que deseja remover e selecione **[!UICONTROL Continuar]**.
5. Esta ação removerá o painel de conformidade compartilhado do aplicativo do gerente.

   ![](assets/manager-edit.png)
   _Retirar o painel de conformidade_

#### Definir widget de conformidade padrão para alunos

Siga estas etapas para definir o widget de conformidade padrão dos alunos:

1. Faça logon como **[!UICONTROL Administrador]**.
2. Navegue até o **[!UICONTROL Relatórios]** > **[!UICONTROL Resumo do aprendizado]** > **[!UICONTROL Painel de conformidade]**.
3. Selecione **[!UICONTROL Exibição do Aluno]** na seção **[!UICONTROL Painel de Conformidade]**.
4. Selecione **[!UICONTROL Alterar]** na seção **[!UICONTROL Exibição do aluno]**.

   ![](assets/learner-widget.png)
   _Definir widget de conformidade padrão para alunos_
5. Selecione os rótulos de conformidade na lista suspensa **[!UICONTROL Conformidade personalizada]**. Essa opção selecionará todos os cursos com os rótulos de conformidade selecionados.
6. Selecione **[!UICONTROL Continuar]** para definir o widget de conformidade padrão.

Os alunos podem ver os cursos selecionados ou caminhos de aprendizado no widget de conformidade em sua página inicial. Consulte [Widget de painel de conformidade](/help/migrated/learners/feature-summary/learner-home-page.md#compliance-dashboard-widget) para obter mais informações.

## Relatórios personalizados

Os administradores podem gerar relatórios específicos usando o modelo personalizado disponível na seção **[!UICONTROL Relatórios]**.

### Relatórios de amostra {#samplereports}

A guia **[!UICONTROL Relatórios de amostra]** mostra alguns relatórios indicativos que estão baseados em pontos de dados de amostra. Explore esses relatórios para ter uma ideia dos diferentes tipos de relatórios com recursos avançados que você pode gerar usando os dados da sua conta.

### Relatórios do painel {#dashboardreports}

Um painel é uma coleção de relatórios. Os relatórios podem ser agrupados em um painel de acordo com sua escolha. Para exibir todos os painéis que você criou, clique nesta guia de painel. Na lista suspensa **[!UICONTROL Exibir Painel]**, você pode selecionar o painel padrão ou um painel que você criou.

### Relatórios do Excel {#excelreports}

A guia **[!UICONTROL Relatórios do Excel]** permite exportar relatórios no formato de arquivo XLS.

Estes são os tipos de relatório disponíveis para download.

* Relatórios do curso
* Transcrições do aluno
* Relatório de comunicados
* Relatório de ajudas de tarefa
* Registro de auditoria do conteúdo
* Registro de auditoria do usuário
* Relatório de logon/acesso
* Transcrições da gamificação
* Trilha de Auditoria de Gamificação

### Relatórios do curso {#coursereports}

Como administrador, você pode baixar relatórios dos cursos. Siga estas etapas:

1. Abra **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatórios Do Excel]** > **[!UICONTROL Relatórios Do Curso]**.
1. A caixa de diálogo **[!UICONTROL Relatório do curso]** é exibida. Selecione o curso do que deseja obter o relatório e clique em **[!UICONTROL Mostrar]**.

   ![](assets/course-reports.png)
   *Relatórios do curso*

1. Você será redirecionado para a página do curso. Você pode exportar a pontuação do quiz por usuário e por pergunta com base em cada inscrição escolhendo o tipo de inscrição específico.
1. Selecione **[!UICONTROL Exportar pontuação do questionário]** para exportar o relatório. É exibida a caixa de diálogo **[!UICONTROL Gerar solicitação de relatório]**. Clique em **[!UICONTROL OK]** para confirmar.

   ![](assets/generating-reportrequest.png)
   *Gerando Solicitação de Relatório*

   >[!NOTE]
   >
   >O relatório exportado da pontuação do questionário conterá os detalhes da pontuação de cada tentativa se a opção de várias tentativas estiver configurada no módulo.

### Gerar relatórios de curso

>[!INFO]
>
>Neste treinamento, você aprenderá a exportar relatórios de curso e configurar assinaturas de e-mail para esses relatórios.<br><br>[![botão](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318904)</br></br>


Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

### Transcrições do aluno {#LearnerTranscripts-1}

O Adobe Learning Manager permite que os administradores de uma organização gerem transcrições associadas aos alunos. O relatório de transcrição do aluno contém o seguinte:

1. Transcrição do aluno: Painel da atividade de aprendizado
1. Habilidade: painel de habilidade
1. Painel de conformidade

As transcrições do aluno nos relatórios do Excel exibem as colunas Créditos necessários e Créditos obtidos em números decimais.

Para obter informações sobre a geração de relatórios das transcrições dos alunos e mais informações, consulte [Transcrições do aluno](learner-transcripts.md).

### Relatórios de comunicados {#announcementsreports}

Como administrador, você pode gerar um relatório de todos os comunicados que você enviou. O relatório traz detalhes sobre:

* Tipo de comunicado
* Nome do comunicado
* Data do comunicado
* Estado do comunicado
* Nome do aluno

Para baixar um relatório, siga qualquer uma dessas etapas:

1. Abra **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatórios Do Excel]** > **[!UICONTROL Relatório De Comunicados]**. A caixa de diálogo **[!UICONTROL Gerando Solicitação de Relatório]** é aberta. Clique em Ok.
1. [!UICONTROL **Comunicados**] > [!UICONTROL **Ações**] > [!UICONTROL **Exportar Relatório**].

   ![](assets/announcements.png)
   *Relatório de comunicados*

1. Você pode extrair um relatório para um comunicado específico clicando em **[!UICONTROL Exportar Relatório]** sob o ícone de configurações.

   ![](assets/announcements-specific-report.png)
   *Relatório para comunicados específicos*

### Relatório de ajudas de tarefa {#jobaidsreport}

As ajudas de tarefa são um conteúdo de treinamento a que os alunos podem ter acesso sem ter de se inscrever em um objeto de aprendizado específico, como um curso ou programa de aprendizado. Os administradores podem extrair e baixar relatórios das ajudas de tarefa.

O relatório extraído inclui informações sobre o seguinte:

* Nome
* Tipo de ajuda de tarefa
* Estado da ajuda de tarefa (publicada ou retirada)
* Data da inscrição
* Data de conclusão
* Data de download
* Nome do aluno
* Nome do gerente
* Criado por

Para baixar um relatório, siga um destes procedimentos:

* Abra **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatórios Do Excel]** > **[!UICONTROL Relatórios De Ajuda De Trabalho]**. É exibida a caixa de diálogo **[!UICONTROL Gerar solicitação de relatório]**. Clique em **[!UICONTROL Ok]**.
* Abrir **[!UICONTROL Ajuda de Trabalho]** > **[!UICONTROL Ações]** > **[!UICONTROL Exportar Relatório]**.

![](assets/job-aids.png)
*Relatório de ajudas de tarefa*

* Você também pode extrair um relatório de uma ajuda de tarefa específica clicando em **[!UICONTROL Exportar relatório]** no ícone de configurações.

![](assets/job-aid-specific-download.png)
*Relatório de ajuda de tarefa específica*

### Relatório de ajudas de tarefa

Depois de selecionar **[!UICONTROL Relatório de ajudas de tarefa]** na lista, você verá duas opções:

![relatório de ajudas de tarefa](assets/job-aids-new.png)
*Baixar Relatório de Inscrição do Usuário de Ajudas de Trabalho*

**Todas as ajudas de tarefa**: se o número de ajudas de tarefa na conta for inferior a 10 milhões, o relatório gerado conterá informações de inscrição de todas as ajudas de tarefa. Essa será a seleção padrão. Se o número de linhas exceder 10 milhões, será exibido um erro, e você deverá selecionar manualmente as ajudas de tarefa necessárias.

**Ajudas de tarefa selecionadas**: se você selecionar esta opção, poderá inserir as ajudas de tarefa para as quais deseja gerar o relatório. Você pode selecionar no máximo 10 ajudas de tarefa. A Adobe Learning Manager verifica se o número de ajudas de tarefa excede 10 milhões.

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
* Data de publicação (Fuso horário central da Europa)
* Criado por nome
* Criado por e-mail
* Criado por ID exclusiva do usuário
* Catálogo(s)
* Caminho(s) de aprendizado
* Curso(s)
* Marca(s)
* Habilidade(s)

**Relatório de Inscrição do Usuário de Ajudas de Trabalho**

O relatório de inscrição contém detalhes sobre a inscrição do usuário e outras informações.

O relatório baixado consiste nos seguintes campos:

* Nome da ajuda de tarefa
* Tipo
* Estado
* Data de inscrição (fuso horário UTC)
* Data de conclusão (fuso horário UTC)
* Data do download (fuso horário UTC)
* Nome do aluno
* Email
* ID exclusiva do usuário
* Nome do gerente
* E-mail do gerente
* ID exclusiva do usuário do gerente
* Atribuído por nome
* Atribuído por e-mail
* Atribuído por ID exclusiva do usuário
* Criado por nome
* Criado por e-mail
* Criado por ID exclusiva do usuário
* Código da tarefa
* Novo campo
* Perfil

### Relatórios de registros de auditoria do conteúdo {#contentaudittrailreports}

Use o gerador de relatórios da **[!UICONTROL Trilha de auditoria de conteúdo]** para gerar um relatório de todas as alterações e edições feitas em um curso durante sua vida útil no sistema. O relatório gerado tem as seguintes informações.

* ID do objeto
* Nome do objeto
* Tipo de objeto
* Tipo de modificação
* Descrição
* ID do objeto referenciado
* Nome do objeto referenciado
* Modificado por nome de usuário
* Modificado por ID de usuário
* Data da modificação (fuso horário do Horário Universal Coordenado)

Na coluna **Tipo de modificação**, você obterá os seguintes detalhes:

| Tipo de modificação | Descrição |
| --- | --- |
| Criar  | Curso criado |
| Adicionar Certificação | Certificação adicionada ao catálogo |
| Remoção de certificação | Certificação removida do catálogo |
| Adição de conteúdo | Conteúdo adicionado ao módulo |
| Adicionar curso | Curso adicionado ao Caminho de Aprendizado |
| Remoção do curso | Curso removido do Caminho de aprendizado |
| Adicionar rótulo personalizado | Etiqueta personalizada adicionada ao catálogo |
| Remoção de rótulo personalizado | Etiqueta personalizada removida do catálogo |
| Excluir | Catálogo excluído |
| Adição de ajuda de tarefa | Ajuda de tarefa adicionada ao catálogo |
| Remover ajuda de tarefa | Ajuda de tarefa removida do catálogo |
| Adicionar Caminho de Aprendizado | Caminho de Aprendizado adicionado ao catálogo |
| Remoção do Caminho de Aprendizado | Caminho de Aprendizado removido do catálogo |
| Adição de conteúdo do módulo | Módulo adicionado ao curso(seção Conteúdo) |
| Remoção de conteúdo do módulo | Módulo removido do curso(seção Conteúdo) |
| Publicado | Curso ou caminho de aprendizado publicado e adicionado ao catálogo padrão |
| Republicado | Curso republicado |
| Adição de recurso | Recurso adicionado ao curso |
| Remoção de recurso | Recurso removido do curso |
| Aposentado | Curso desativado |
| Adicionar Catálogo Compartilhado | Catálogo compartilhado para Catálogo |
| Remoção do catálogo compartilhado | Compartilhamento de catálogo removido do catálogo |
| Atualização do catálogo compartilhado | Estado de compartilhamento de catálogo: ativo |
| Atualização | Curso ou caminho de aprendizado atualizado |
| Adicionar Grupo de Usuários | Grupo de usuários adicionado ao catálogo |
| Remover grupo de usuários | Grupo de usuários removido do catálogo |

As informações que dizem respeito aos metadados não são obtidas no relatório gerado.

Para gerar um relatório de registro de auditoria do curso, siga estas etapas.

1. Selecione **[!UICONTROL Relatório]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Trilha de auditoria do curso]**. É exibida a caixa de diálogo **[!UICONTROL Registro de auditoria do conteúdo]**.

   ![](assets/course-audit-trial.png)
   *Trilha de auditoria do curso*

1. Selecione o curso, o programa de aprendizado e a certificação para os quais deseja baixar o relatório. Se não especificado, todos os relatórios são baixados por padrão.
1. Selecione um intervalo de datas para o relatório e clique em **[!UICONTROL Gerar]**.
1. O relatório é gerado e você é notificado de que o relatório de auditoria do conteúdo está pronto. Você pode baixar o relatório.

### Relatórios de registros de auditoria do usuário {#useraudittrailreports}

A trilha de auditoria do usuário captura o ciclo de vida de usuários, grupos de usuários e perfis de autorregistro. Adições, exclusões, alterações de usuários no Gerente, são todas capturadas. A criação e exclusão de perfis de autorregistro também são registradas. Você também pode pausar e continuar o perfil de autorregistro.

Nos perfis externos é possível adicionar, habilitar, desabilitar, pausar ou continuar enquanto que no autorregistro é possível adicionar, excluir, pausar e continuar. Os uploads de CSV também são capturados.

1. Selecione **[!UICONTROL Relatório > Relatório do Excel > Trilha do usuário]**. A caixa de diálogo Registro de auditoria do usuário é exibida.
1. É exibida a caixa de diálogo Registro de auditoria do usuário. Selecione o intervalo de data no menu pop-up. Você pode optar por gerar o relatório da última semana, do último mês ou pode selecionar uma data personalizada.

   ![](assets/user-audit-trail.png)
   *Trilha de auditoria do usuário*

1. Clique em **[!UICONTROL Gerar]** para gerar o relatório.

Há dois filtros na caixa de diálogo **[!UICONTROL Relatório de registro de auditoria do usuário]**.

**Filtro de classificação por data:** escolha o intervalo de datas para o qual você deseja gerar o relatório. Há três opções:

* Última semana
* Último mês
* Data personalizada

Selecione o filtro Alunos: pesquise um usuário ou um grupo de usuários.

O relatório exportado conterá dados de usuários que atenderem aos critérios de pesquisa especificados.

![](assets/user-audit-trail.png)
*Trilha de auditoria do usuário*

>[!NOTE]
>
>Quando uma habilidade é atribuída ou removida, ela pode ser rastreada para o Relatório de auditoria do usuário para atribuída ou removida.

### Relatório de configuração de extensão

Este relatório fornece informações sobre os detalhes de configuração de todas as extensões nativas adicionadas, incluindo o estado de ativação. Saiba como baixar o relatório de extensões. Consulte [Baixar relatório de extensões](native-extensibility.md#download-extension-report).

### Relatório de atividades da xAPI

Este relatório fornece os dados de todas as instruções xAPI registradas e geradas durante os módulos de atividade da xAPI.

Para baixar esse relatório, siga estas etapas:

1. Selecione **[!UICONTROL Relatório > Relatório do Excel > Relatório de atividades da xAPI]**. A caixa de diálogo Relatório de atividades da xAPI é exibida.
1. Selecione o intervalo de data no menu pop-up. Você pode optar por gerar o relatório da última semana, do último mês ou pode selecionar uma data personalizada.
1. Selecione os alunos e a atividade no menu suspenso.
1. Selecione **[!UICONTROL Gerar]** para gerar o relatório.

### Relatórios de gamificação {#gamification}

Os administradores podem baixar a transcrição da gamificação no formato CSV. Você pode baixar o relatório para usuários individuais ou grupos de usuários. Nome do usuário, email do usuário, UUID do usuário, total de pontos do usuário pontuados, divisão de pontos coletados, nome dos grupos que o usuário joga, nome do gerente e valores de campo ativos são todos obtidos no relatório. Os administradores podem usar esse relatório para avaliar e entender as classificações do usuário no âmbito da empresa ou em um grupo específico.

1. Selecione Relatório > Relatório do Excel > Relatório de gamificação.

   ![](assets/gamification.png)
   *Relatório de gamificação*

1. É exibida a caixa de diálogo Transcrições da gamificação. Selecione alunos usando seu nome, perfil, grupos de usuários, ID de e-mail ou UUID.

   ![](assets/gamification-transcriptsdialog.png)
   *Caixa de diálogo de transcrições de gamificação*

1. Clique em **[!UICONTROL Gerar]** para gerar o relatório.

   Depois de gerar o relatório de um aluno, você deve ser capaz de exportar as informações atuais e de nível alcançado para todos os usuários (internos, externos ou excluídos) na conta. Você também pode verificar as datas dos níveis atingidos por um aluno:

   * Data de obtenção do bronze
   * Data de obtenção da prata
   * Data de obtenção do ouro
   * Data de obtenção da platina

   Essas colunas contêm as datas em que o nível foi atingido pela primeira vez. A coluna **[!UICONTROL Nível Atual]** exibe o nível atual do aluno.

   Quando o administrador redefine a gamificação, todos os pontos do aluno são redefinidos adequadamente.

### Relatório de trilha de auditoria de gamificação {#gamification-audit-trail}

Este relatório contém o histórico e os motivos dos pontos de gamificação dos alunos obtidos para cada regra.

### Baixar o relatório

1. Selecione o URL da trilha de auditoria de gamificação.
1. No pop-up **Trilha de auditoria de gamificação**, selecione o intervalo de datas.
1. Selecione **Gerar**.

O relatório é baixado como um arquivo CSV. O arquivo contém as seguintes colunas:

* Nome
* Email/ UUID,
* Status
* Ação
* Pontos,
* Pontos de Equilíbrio
* Regra/Tarefa
* Subtarefa de Regra/Tarefa,
* Detalhes de regra/tarefa
* Tipo,
* Nome,
* Data da Nome da Instância Obtida (Fuso Horário UTC)
* Hora de Início da Regra/ Tarefa
* Hora de Término da Regra/ Tarefa

### Relatório de inscrição e cancelamento de inscrição {#enrollmentandunenrollmentreport}

Os administradores e gerentes podem extrair um relatório dos alunos que foram inscritos e cancelados. Como administrador, você pode ver qualquer aluno, administrador ou gerente que se inscreveu ou cancelou a inscrição em uma instância de um curso, de um programa de aprendizado ou de uma certificação, bem como exportar o relatório. Enquanto gerente, você só pode obter um relatório dos membros da sua equipe. Como gerente, você não pode ver os alunos excluídos ou seu próprio nome no aplicativo do gerente como um aluno inscrito ou não inscrito.

Para baixar um relatório, siga estas etapas: Abra o **[!UICONTROL Programa de aprendizado/Certificação]** > **[!UICONTROL Alunos]** > **[!UICONTROL Ação]** > **[!UICONTROL Exportar relatório]**.

![](assets/unenrollment.png)
*Relatório de cancelamento de inscrição*

### Relatório de feedback {#feedback-report}

Como administrador, você pode buscar o feedback do aluno (L1) e o feedback do gerente (L3) para treinamentos selecionados por um período especificado.

Você pode exportar os dados da interface do usuário ou por meio do conector PowerBI para uma análise mais detalhada.

Os relatórios de feedback L1 e L3 oferecem uma opção de download de um relatório de feedback consolidado para as respostas L1 e L3 para treinamentos selecionados para um intervalo de **um ano** ou para até 10 treinamentos selecionados para qualquer período.

Faça logon como administrador, clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios personalizados]** e, na lista de relatórios, clique em **[!UICONTROL Relatório de comentários]**.

![](assets/download-feedbackreport.png)
*Baixar relatório de comentários*

Ao clicar em Baixar após selecionar os filtros, você receberá uma notificação para baixar o relatório no formato CSV.

O relatório baixado terá detalhes como nome e tipo do treinamento, nome da instância, nome do aluno e e-mail, tipo de feedback: L1 ou L3, datas do feedback enviado para novos dados.

Para os dados existentes antes da implementação desse recurso, a data de conclusão do OA será exibida, a data de conclusão do OA, o texto real do Ritmo do próprio comentário da pergunta L1 e o Texto da sala de aula em colunas diferentes, as respectivas respostas do Feedback L1, o nome do gerente e o email, o valor do feedback L3 e a data de envio, os Campos ativos.

Você também pode exportar os dados da interface do usuário ou para o Power BI, que oferece suporte a todos os treinamentos para qualquer período para uma análise mais aprofundada.

### Relatórios de treinamento {#training-report}

O Learning Manager é compatível com o Relatório de treinamento, que permite que os administradores baixem detalhes de treinamento e seus metadados associados, como autor, data de publicação, habilidades, etiquetas do catálogo etc.

No aplicativo de administração, clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios personalizados]** > **[!UICONTROL Relatórios do Excel]** > **[!UICONTROL Relatório de treinamentos]**.

Você pode baixar relatórios para o seguinte:

* Treinamentos selecionados (10 no limite) - Seleciona um ou vários treinamentos (até 10) de qualquer catálogo.
* Os treinamentos no catálogo selecionado (5 no limite) - (a seleção do catálogo estará disponível para até cinco catálogos).
* Todos os treinamentos - (todos os treinamentos na conta).

![](assets/download-trainingreport.png)
*Baixar relatório de treinamento*

Na seção Opções avançadas, as seguintes opções estão disponíveis:

* Incluir mapeamentos de cursos com programa de aprendizado/certificação
* Incluir informações de nível do módulo

Depois de selecionar os filtros e clicar em Baixar, você receberá uma notificação para baixar o relatório no formato CSV.

O relatório terá os seguintes campos:

*Nome do catálogo, Tipo de treinamento, ID do treinamento, ID exclusiva de treinamento, Nome do treinamento, Subtreinamentos, Módulos, Duração do módulo ou treinamento, Formato, Status do treinamento, Habilidades, Autor, Última data de publicação, Última data de conclusão, Contagem de inscrição dos professores, Contagem de início, Contagem de conclusão, Pontuação L1 média, Pontuação L2 média, Pontuação L3 média, Respostas L1 recebidas, Respostas L2 recebidas, Respostas L3 recebidas, Etiquetas do catálogo e Tags.*

![](assets/more-options.png)
*Opções adicionais*

### Relatório de resumo da sessão {#session-summary-report}

O Relatório de resumo da sessão contém todas as sessões planejadas para um aluno em uma data especificada.

Isso permite que o administrador exporte todos os detalhes da sessão de sala de aula e virtual que estão no intervalo de datas especificado. O administrador também pode exportar o relatório de sessão em relação a treinamentos ou professores específicos.

Isso também ajudará o administrador a entender as sessões planejadas mensalmente e identificar a agenda dos professores e as sessões já entregues.

Como administrador, clique em **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatório de Resumo da Sessão]**.

Na caixa de diálogo a seguir, escolha o intervalo de datas e o treinamento ou o professor para obter um resumo.

![](assets/session-summary-report.png)
*Relatório de resumo da sessão*

O csv baixado contém os seguintes campos:

* Data e hora de início
* Data e hora de término

* Nome do módulo
* Duração da sessão (em minutos)
* Número de vagas
* Localização
* Nome da instância
* Nome do curso
* ID do curso
* Nome do professor
* E-mail do professor
* Número de inscrições
* Tipo de sessão
* Limite de listas de espera
* Número de listas de espera
* E-mail do usuário da lista de espera
* Informações do Local
* Região do local

### Relatório de Utilização do Professor

Este relatório captura o tempo (em minutos) gasto diariamente por um professor ensinando sessões atribuídas. O relatório pode ser baixado por um período de três meses a partir da data de início selecionada.

Para baixar o relatório, clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios Personalizados]** > **[!UICONTROL Relatório de Utilização do Professor]**.

Selecione um professor ou vários e o intervalo de datas.

![Baixar Relatório de Utilização de Professor](assets/utilization-report.png)
*Baixar Relatório de Utilização de Professor*

O relatório baixado contém os seguintes campos:

* Nome do professor
* ID do professor
* Nível de competência
* Datas como colunas. Se o professor for utilizado em uma data, o número de sessões será listado. Se o professor não for utilizado em um dia, o valor exibirá zero.

O relatório contém registros de três meses a partir do mês selecionado.

Para recuperar registros de todos os professores, deixe o campo Professor em branco.

Além disso, um administrador personalizado com permissão para gerar relatórios pode recuperar este relatório.

### Relatório de Trilha de Auditoria do Usuário

Este relatório captura informações sobre os alunos que alternaram instâncias, “de instância” para “para instância”, alternados por hora, data etc.

Selecione os alunos ou um grupo de usuários.

Para baixar o relatório, clique em **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios personalizados]** > **[!UICONTROL Relatório de registro de auditoria do usuário]**.

![Baixar Relatório de Registro de Auditoria do Usuário](assets/user-audit-report.png)

*Baixar Relatório de Registro de Auditoria do Usuário*

### Relatório do plano de aprendizado

Este relatório contém detalhes de todos os planos de aprendizado em uma conta, por exemplo, grupos de usuários relacionados, status e informações sobre o acionador.

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
* Inscrever-se depois
* Tipos de elemento de aprendizado
* Elementos de aprendizado
* Instâncias do elemento de aprendizado
* Elemento de aprendizado
* Data de conclusão
* Lembrete do elemento de aprendizado
* Escopo/Catálogo
* Escopo/Grupo de usuários

### Trilha de auditoria para funções personalizadas

Os administradores podem baixar o relatório de auditoria da função personalizada para acompanhar todas as alterações feitas nas funções personalizadas, incluindo criar, modificar e excluir funções personalizadas e seu acesso a recursos associado.

Para baixar o relatório, siga estas etapas:

1. Faça logon como administrador.
2. Selecione Relatórios > Relatórios personalizados.
3. Selecionar trilha de auditoria da função personalizada e escolher o intervalo de datas
4. Selecione Gerar para baixar o relatório.

O relatório Trilha de auditoria da função personalizada contém os seguintes campos:

* ID da função
* Nome da função
* Tipo de atividade
* Tipo de modificação
* Descrição
* Tipo de objeto referenciado
* ID do objeto referenciado
* Nome do objeto referenciado
* E-mail do objeto referenciado
* Modificado por nome de usuário
* Modificado pelo UUID do usuário
* Modificado por e-mail de usuário
* Data de modificação (Fuso horário UTC)
* Origem

## Assinaturas de e-mail {#emailsubscriptions}

Você pode obter seus relatórios favoritos por e-mail inscrevendo-se para recebê-los.

### Configurar assinaturas de email

>[!INFO]
>
>Neste treinamento, você aprenderá como configurar assinaturas de email para relatórios do painel.<br><br>[![botão](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318927)</br></br>


Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

Na página **[!UICONTROL Relatórios]**, clique na guia **[!UICONTROL Assinatura]**. A página de inscrição no relatório é exibida.

Para selecionar o nome do relatório na lista suspensa, comece a digitar o nome do relatório no campo Relatórios. Escolha a frequência de e-mail na lista suspensa. Você pode adicionar o assunto do e-mail e fornecer uma ID de e-mail de backup.

É possível editar e excluir assinaturas.

## Relatórios históricos

Os relatórios históricos no Adobe Learning Manager (ALM) referem-se aos relatórios que capturam os dados históricos e as atividades na plataforma de aprendizado. Esses relatórios fornecem informações sobre atividades passadas do aluno, conteúdo de treinamento, desempenho do grupo de usuários e outros dados relevantes. Os relatórios históricos permitem que os administradores controlem, monitorem e analisem o progresso e a eficácia das iniciativas de aprendizado ao longo do tempo.

### Relatórios de acesso ao curso

Os relatórios de acesso ao curso fornecem informações sobre a revisão de cada curso.

Para baixar esse relatório, siga estas etapas:

1. Vá para **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios personalizados]** > **[!UICONTROL Relatórios de histórico]**.
1. Selecione **[!UICONTROL Relatório de acesso ao curso]**. A caixa de diálogo Gerando solicitação de relatório é aberta.
1. Selecione o ano e o trimestre no menu suspenso.
1. Selecione **[!UICONTROL Gerar]**.

### Relatórios de logon/acesso

Os relatórios de login/acesso fornecem informações sobre logons e acesso de usuários. Você pode gerar um relatório contendo dados de três meses por vez.

Para baixar esse relatório, siga estas etapas:

1. Vá para **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios personalizados]** > **[!UICONTROL Relatórios de histórico]**.
1. Selecione **[!UICONTROL Relatório de logon/acesso]**. A caixa de diálogo Gerando solicitação de relatório é aberta.
1. Selecione o ano e o trimestre no menu suspenso.
1. Selecione **[!UICONTROL Gerar]**.

## Criar um painel {#createadashboard}

1. Para começar a criar seus próprios painéis, clique em Adicionar painel no lado direito da página.

   ![](assets/add-dashboards.png)
   *Adicionar painéis*

1. Forneça o nome e a descrição do painel.
1. Se você deseja compartilhar o painel com qualquer Gerente, escolha-os no campo **[!UICONTROL Compartilhar com]**. Você pode usar todos os critérios de seleção normal nesta operação.
1. Clique em **[!UICONTROL Salvar].**

Você pode visualizar o painel criado recentemente na guia **[!UICONTROL Relatórios de painel]**.

Para adicionar relatórios ao seu painel, clique na lista suspensa no canto superior direito da janela do painel e clique em **[!UICONTROL Adicionar relatório]**. O relatório que você cria desta forma é associado ao seu painel.

>[!NOTE]
>
>Os relatórios que você cria ao clicar em Adicionar no canto superior direito da página Relatórios, são adicionados ao painel padrão.

## Painéis compartilhados {#shareddashboards}

Os relatórios compartilhados são uma conjunto de relatórios que foram compartilhados com você por outros usuários da sua empresa. Todos os relatórios que você adiciona a um painel compartilhado são compartilhados automaticamente com outros usuários que têm acesso a esse painel.

É possível compartilhar o painel das seguintes maneiras:

* Inserindo usuários no campo **[!UICONTROL Compartilhar com]** com quem o painel é compartilhado.
* Escolha Editar painel na lista suspensa e insira detalhes do usuário para compartilhar o painel.

>[!NOTE]
>
>Um gerente pode ver somente os relatórios dos membros da sua equipe em um painel compartilhado.

## Downloads {#downloads}

A planilha de relatórios do painel exportada fornece informações detalhadas em vez de resumo de relatório. O relatório baixado segue o formato de uma Transcrição do aluno.

## Criar relatórios {#report}

1. Clique em Relatórios no painel esquerdo. A página de resumo de relatório será exibida.

   >[!NOTE]
   >
   >Por padrão, são exibidos pelo menos três relatórios de amostra na guia Painel de amostra. Você pode ver apenas os relatórios de amostra para ter uma ideia de como é possível criá-los e personalizá-los.

1. No canto superior direito da página, clique em **[!UICONTROL Adicionar]**.
1. Na caixa de diálogo **[!UICONTROL Adicionar relatório]**, na lista suspensa Tipo, você pode escolher um dos relatórios predefinidos ou pode selecionar **[!UICONTROL Personalizado]**. Se você selecionar um relatório predefinido, é possível ver o formulário é preenchido. Você pode fazer alterações posteriores a qualquer um dos campos e clicar em **[!UICONTROL Salvar]**. Isso adiciona o relatório ao painel padrão.

   ![](assets/create-report.png)
   *Criar relatório*

   Em **[!UICONTROL Tipo de relatório]**, você pode escolher um conjunto predefinido de relatórios ou escolher valores personalizados. Você pode exibir os seguintes relatórios como parte do conjunto predefinido de relatórios:

   * Conhecimentos atribuídos e alcançados
   * Cursos inscritos e concluídos
   * Eficácia dos cursos
   * Programas de aprendizado inscritos e concluídos
   * Tempo gasto no aprendizado por curso
   * Tempo gasto no aprendizado por trimestre
   * Conclusão da certificação

1. Escolha o **[!UICONTROL Eixo Y]** para o relatório nas opções suspensas. Para qualquer um dos critérios selecionados, você pode escolher um ou vários estados nas opções de estados. Por exemplo, para o critério principal das estatísticas de inscrição em um curso, os estados podem ser concluído, incompleto e inscrito. Os dados da faixa principal são representados na forma de gráficos de barra no relatório.

   ![](assets/axes-for-reports.png)
   *Eixos para relatórios*

1. Escolha o critério/intervalo do **[!UICONTROL eixo Y]** do seu relatório nas opções suspensas. Por exemplo, na opção de inscrição em um programa de aprendizado, escolha um ou vários estados na caixa suspensa Estados. Os dados da faixa secundária são representados na forma de gráficos de linha no relatório.
1. Escolha os critérios apropriados do eixo X*** para o relatório nas opções suspensas. Se o eixo X for selecionado como uma data, então, estará disponível uma opção para agrupar o critério do eixo X por dia, mês, trimestre e ano.
1. Na seção Intervalo de tempo, escolha a opção apropriada suspensa. As opções disponíveis são:

   * Último mês
   * Trimestre
   * Ano
   * Início do trimestre até a data atual (últimos 90 dias)
   * Início do ano até a data atual (últimos 365 dias)
   * Intervalo de datas. Forneça os valores nos campos de data **[!UICONTROL De]** e **[!UICONTROL A]**.

   ![](assets/time-filter-for-report.png)

1. **Seção Filtros**

   Os filtros são exibidos na caixa de diálogo Adicionar na parte inferior com base nos tipos de relatórios que você escolheu. Alguns filtros importantes são mencionados abaixo.

   * **Gerente:** você pode escolher qualquer um dos gerentes com base na hierarquia. Para alguns gerentes, pode haver gerentes subordinados e vários funcionários se comunicando com cada gerente subordinado.
   * **Perfil:** escolha a designação para seu funcionário. Seria útil ver os relatórios dos funcionários com base em seu perfil/designação. Por exemplo, informático, engenheiro.
   * **Grupo de usuários:** escolha o grupo de usuários para o qual deseja filtrar os relatórios. O Learning Manager pega os grupos de usuário definidos para sua conta a partir do recurso Usuários.
   * **Conteúdo:** você pode filtrar o relatório com base em qualquer curso escolhendo-os na lista suspensa.

   Expanda esta seção e escolha os filtros necessários.

   ![](assets/choose-filters.png)
   *Escolher filtros*

1. Clique em **[!UICONTROL Salvar]** para concluir a criação de um relatório.

   ![](assets/sample-report.png)
   *Relatório de exemplo*

## Editar um relatório {#editareport}

No relatório, clique na seta suspensa e selecione a opção **[!UICONTROL Editar relatório]**.

![](assets/edit-a-report-1.png)
*Editar um relatório*

Faça as alterações necessárias no relatório. Para salvar as alterações, clique em **[!UICONTROL Salvar]**.

## Mover um relatório para um painel {#moveareporttoadashboard}

Escolha essa opção para mover o relatório atual para um painel. Para mover o relatório, clique na opção **[!UICONTROL Mover para o painel]**.

![](assets/move-a-report.png)
*Mover um relatório para um painel*

Escolha o painel para o qual deseja mover o relatório e clique em **[!UICONTROL Mover]**.

## Criar uma cópia de um relatório {#createacopyofareport}

Para criar uma cópia do relatório, selecione a opção **[!UICONTROL Criar uma Cópia]**.

![](assets/copy-a-report.png)
*Criar uma cópia de um relatório*

Escolha o painel no qual você deseja copiar o relatório. Para iniciar a cópia, clique em **[!UICONTROL Copiar]**.

## Excluir um relatório {#deleteareport}

Para excluir um relatório, escolha a opção **[!UICONTROL Excluir relatório]**. Após excluir o relatório, você não pode restaurar o relatório. O processo é irreversível. Tenha cuidado ao excluir um relatório.

![](assets/delete-a-report.png)
*Excluir um relatório*

## Baixar um relatório {#downloadareport}

Para baixar o relatório, selecione a opção **[!UICONTROL Baixar relatório]**.

![](assets/download-a-report.png)
*Baixar um relatório*

## Redimensionar um relatório {#resizeareport}

Você pode redimensionar seus relatórios para os tamanhos 1 × 1 (médio) e 1 × 2 (grande). Isso oferece uma melhor forma de visualizar os relatórios. Além disso, você pode facilmente aplicar zoom ou panorâmica nesses relatórios.

## Filtros {#filters}

Os filtros são exibidos na caixa de diálogo **[!UICONTROL Adicionar]** na parte inferior com base nos tipos de relatórios que você escolheu. Alguns filtros importantes são mencionados abaixo.

**Gerente** Você pode escolher qualquer um dos gerentes com base na hierarquia. Para alguns gerentes, pode haver gerentes subordinados e vários funcionários se comunicando com cada gerente subordinado.

**Perfil** Escolha a designação para seu funcionário. Seria útil ver os relatórios dos funcionários com base em seu perfil/designação. Por exemplo, informático, engenheiro.

**Grupo de usuários** Escolha o grupo de usuários com base no qual você deseja filtrar os relatórios. O Learning Manager pega os grupos de usuário definidos para sua conta a partir do recurso Usuários.

**Curso** Você pode filtrar o relatório com base em qualquer curso ao escolher o mesmo na lista suspensa.

![](assets/sample-report-admin.png)
*Filtrar um relatório*

Acima da legenda do gráfico, você pode exibir uma caixa de zoom. Mova o cursor do mouse sobre ela, clique e arraste a barra transversal sobre qualquer parte da área do gráfico da caixa de zoom para aplicar o zoom.

Você pode exibir os valores do eixo Y secundário na forma de uma linha entre as barras no gráfico. Por exemplo, na amostra acima, você pode ver os valores para a Eficiência na linha cinza através do gráfico.

## Relatórios de grupo de usuários {#user-group-reporting}

Acompanhe o desempenho de grupos, tal coo departamento, parceiros externos e funções, em comparação com outros grupos ou em relação a outros objetivos de aprendizado.

### Grupos de usuários {#usergroups}

Para gerar relatórios com base em grupos de usuários, escolha **[!UICONTROL Grupo de Usuários]** no eixo x na lista de opções suspensas, conforme mostrado na captura de tela abaixo.

![](assets/user-group-reports.png)
*Relatórios de grupos de usuários*

Para selecionar um grupo de usuários, digite o nome do grupo. Você pode ver os grupos sugeridos exibidos de acordo com a string inserida. Quando a lista de grupos for exibida, escolha o grupo de usuários necessário.

Você também pode escolher vários grupos de usuários com a ajuda da pesquisa com preenchimento automático.

Após salvar e gerar este relatório, se tiver selecionado vários grupos de usuários, o relatório é gerado com todos os grupos de usuários representados no gráfico de barras ao lado um do outro no eixo X.

Este relatório do grupo de usuários permite comparar o desempenho de um departamento/divisão/função em relação ao outro para avaliar as suas realizações de aprendizagem.

### Atributos personalizados de grupos de usuários/usuário {#customusergroupsuserattributes}

Você também pode criar grupos de usuários personalizados usando o recurso Adicionar usuários/grupos de usuários no Learning Manager. Após criar os grupos de usuários, você pode gerar relatórios para esses grupos de usuários personalizados com a ajuda de uma lista de atributos, tal como local, filial.

No eixo x, escolha a opção de atributo de usuário e selecione o atributo no menu suspenso **selecionar** ao lado dele. Para criar um relatório de grupo de usuários personalizado com base nesses atributos, você também deve escolher o grupo de usuários apropriado no filtro.

## Exibição de relatórios {#viewingreports}

Na página Relatórios, você pode exibir todos os relatórios. Você pode minimizar cada relatório clicando no ícone de menos (-) no canto superior direito de cada relatório. Clique no ícone de mais (+) para exibir novamente seu relatório.

## Exibição rápida com diferentes datas {#quickviewwithdifferentdates}

Você pode alterar o intervalo/valor da data de todos os relatórios e exibir rapidamente em uma data diferente sem modificar nem salvar o relatório. Clique no ícone de edição (conforme mostrado com uma seta na captura de tela abaixo) próximo ao intervalo de datas, como QTD, do último ano. Para confirmar a alteração, selecione o novo valor no menu pop-up e clique na marca de seleção. Você pode cancelar a alteração clicando na marca X.

>[!NOTE]
>
>O valor da data que você usa para exibir o relatório é temporário. Essa exibição do relatório não é baixada quando você escolhe a opção de download. Esta exibição é apenas uma exibição temporária.

![](assets/learner-count-report.png)
*Exibir contagem de alunos*

## Exibição rápida com diferentes gerentes {#quickviewwithdifferentmanagers}

Se houver múltiplos Gerentes que se reportam a você, poderá exibir os relatórios rapidamente para cada Gerente. Para exibir o relatório exclusivo de cada gerente, escolha o nome do gerente na lista suspensa.

>[!NOTE]
>
>Os valores do gerente que você usa para exibir o relatório são temporários. Essa exibição de relatório não é baixada quando você escolhe a opção de download. Esta exibição é apenas uma exibição temporária.

## Exibir relatórios do curso {#viewcoursereports}

Você pode exibir relatórios específicos para cada curso seguindo as etapas abaixo:

1. Clique no link **[!UICONTROL Exibir relatórios de curso]** na guia Meus painéis na página Relatórios.\
   Uma caixa de diálogo suspensa será exibida. Um campo de entrada de texto aparece onde você pode inserir o curso obrigatório e os nomes dos cursos sugeridos aparecem na lista suspensa. Escolha o curso na lista exibida.

   ![](assets/view-course-report-300x117.png)

   *Exibir relatórios de curso*

1. Selecione o curso da sua escolha na lista suspensa e clique em Mostrar.
1. Você será redirecionado para a página de resultados da pontuação do questionário do curso selecionado para visualizar o relatório específico do curso.

**Editar/Mover para o painel/Criar uma cópia/Excluir/Redimensionar relatório**

Para ver as opções da lista suspensa, tal como Editar/Mover para o painel/Criar uma cópia/Excluir/Redimensionar, clique na seta suspensa no canto superior direito de cada relatório.

![](assets/edit-options-dashboard-300x126.png)

*Editar/Mover para o painel/Criar uma cópia/Excluir/Redimensionar relatórios*

**[!UICONTROL Editar]** Para voltar aos valores iniciais ao modificar dados, clique em Redefinir. Clique em Salvar após modificar os valores.

**[!UICONTROL Mover para o Painel]** Você pode mover o relatório atual para outro painel, que é escolhido na lista de painéis.

**[!UICONTROL Criar uma Cópia]** Você pode copiar o relatório para o mesmo painel ou para outro painel, que é escolhido na lista de painéis.

**[!UICONTROL Excluir]** Clique em Excluir para remover o relatório. Uma mensagem de advertência/confirmação aparece antes que você possa excluir o relatório.

**[!UICONTROL Redimensionar]** Você pode redimensionar seus relatórios em tamanhos 1×1(médio) e 2×2(grande).

## Gerar e exibir relatórios de contas entre parceiros {#generateandviewreportsforpeeraccount}

Como administrador, além de gerar relatórios da sua conta, você também pode gerar e visualizar relatórios das contas entre parceiros definidas por você.

Ao definir uma conta entre parceiros com outro usuário, você pode exibir os relatórios dessa conta na página **[!UICONTROL Relatórios]**. Ao criar um relatório, encontra-se o campo **[!UICONTROL Selecionar conta]**. Na lista suspensa, que lista todas as contas entre parceiros às quais você está associado, selecione a conta para a qual você deseja visualizar os relatórios compartilhados.

Ao criar uma conta entre parceiros, se a opção Compartilhar catálogo não tiver sido selecionada, você não poderá exibir essa conta entre parceiros nesta lista.

![](assets/acc1-jpg.png)
*Gerenciar relatórios para conta entre parceiros*

1. Selecione o eixo X e o eixo Y, e a data desse relatório.
1. Observe que, no campo de filtros, o botão Catálogos compartilhados é habilitado automaticamente. É obrigatório. Se a opção Catálogo compartilhado não estiver habilitada, significa que você não poderá gerar ou visualizar relatórios da conta entre parceiros.
1. Na lista suspensa abaixo de Catálogo compartilhado, selecione o catálogo compartilhado para o qual você deseja exibir o relatório.
1. Clique em [!UICONTROL **Salvar**].

   ![](assets/acc2.png)
   *Selecionar Catálogo Compartilhado para conta entre parceiros*

1. Depois de clicar em **[!UICONTROL Salvar]**, você poderá exibir a representação gráfica de seus relatórios no painel padrão. Nesse painel, você pode filtrar o relatório por gerente para obter a conta específica do colega.
1. Se houver alguma alteração no catálogo pro sua parte, as alterações são refletidas imediatamente nos relatórios e no painel gerados pelo colega. No entanto, quando o colega modificar o catálogo, as alterações não serão exibidas no seu painel automaticamente.
1. Se desejar que o seu painel seja atualizado automaticamente, o colega deve enviar uma nova solicitação a você.

   >[!NOTE]
   >
   >Os gerentes não podem visualizar relatórios entre parceiros.

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como compartilhar um painel personalizado com um gerente?

Ao criar um painel, insira o nome e a descrição. Para compartilhar com gerentes, insira o nome do gerente no campo **[!UICONTROL Compartilhar com]**.

![](assets/share-dashboard-manager.png)
*Compartilhar um painel*
+++
