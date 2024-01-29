---
description: Baixar transcrição do aluno e gerenciar relatórios usando o Learning Manager.
jcr-language: en_us
title: Transcrições do aluno
contentowner: jayakarr
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '1910'
ht-degree: 0%

---



# Transcrições do aluno

Baixar transcrição do aluno e gerenciar relatórios usando o Learning Manager.

O Adobe Learning Manager permite que os administradores de uma empresa gerem transcrições associadas aos alunos.

## Gerar transcrições do aluno {#generatelearnertranscripts}

1. Para gerar transcrições do aluno, clique em **[!UICONTROL Relatórios]** no painel esquerdo de login do administrador.

   O administrador navega até a guia Relatórios do Excel na **[!UICONTROL Relatórios]** página.

1. Clique no link **[!UICONTROL Transcrições do aluno]**.

   O **[!UICONTROL Transcrição do aluno]** a página de histórico é exibida com a mensagem- **Nenhuma transcrição do aluno foi gerada ainda** ou uma lista de downloads que foram acionados após a implementação da página de histórico de transcrições de aprendizado.

   <!--[](assets/learner-transcripts.png)-->

   Uma caixa de diálogo de transcrições do aluno é exibida. Escolha o intervalo de datas para o qual você precisa da transcrição gerada.

   >[!NOTE]
   >
   >Por padrão, a data inicial é a data de registro do aluno e a data final é sempre a data atual. É possível modificar apenas a data inicial a partir de quando você precisa dos dados.

1. Escolha os nomes dos alunos na **[!UICONTROL Selecionar alunos]** e clique em **[!UICONTROL Gerar].**
1. Você pode escolher um único aluno ou grupos de alunos. Para adicionar mais de um aluno, clique em **[!UICONTROL Adicionar mais alunos]**.

   ![](assets/add-learners-lt.png)

   *Adicionar mais alunos*

1. Você pode escolher catálogos específicos ativando a caixa de seleção. A transcrição só é baixada para os catálogos especificados. Você pode escolher catálogos específicos selecionando o catálogo na **[!UICONTROL Selecionar catálogos]** lista suspensa.

   ![](assets/select-catalogs-lt.png)

1. Ao exportar transcrições do aluno, há uma opção, **[!UICONTROL Status da Inscrição]**. Esse menu suspenso contém as seguintes opções:

   * Selecionar tudo
   * Concluído
   * Em andamento
   * Não iniciado
   * Não inscrito

   ![](assets/add-enrollment-status-lt.png)

   *Selecionar o catálogo*

1. Você também pode baixar as transcrições dos alunos que foram excluídos de uma conta.

   Para baixar as transcrições do aluno dos usuários excluídos, clique no botão **[!UICONTROL Opções avançadas]** e ative a caixa de seleção **[!UICONTROL Incluir dados de alunos excluídos]**.

   ![](assets/data-deleted-learners.png)

   *Baixar transcrições dos alunos excluídos*

1. Você pode optar por baixar as informações de nível do módulo na transcrição do aluno ativando o &quot;**[!UICONTROL Habilitar informações de nível do módulo]**“. Nesse caso, os nomes dos módulos e o tempo gasto em cada módulo são obtidos como parte da transcrição, se esta opção estiver ativada.
1. Você pode optar por baixar dados de habilidades e folhas de resumo ativando a opção &quot;**[!UICONTROL Incluir dados de habilidades e folhas de resumo]**“.

   As transcrições são geradas e baixadas no computador como arquivos .csv quando os dados das habilidades não estão incluídos. Se a caixa de seleção Dados de habilidades estiver ativada, as transcrições serão geradas e os arquivos .xls serão baixados.

## Gerar transcrição do aluno usando copiar e colar

Obter transcrições do aluno se torna um processo tedioso, pois podem ser obtidas apenas para um aluno ou grupo de usuários, um de cada vez. Aqui, com o recurso copiar e colar, você pode copiar a lista de IDs de e-mail do aluno e colá-la de uma só vez.

1. Fazer logon como **[!UICONTROL Administrador]** ou **[!UICONTROL Gerente]**.
1. Ir para **[!UICONTROL Relatórios]** sob **[!UICONTROL Gerenciar]**, ele carrega o **[!UICONTROL Atividade do usuário]** página.
1. Clique em **[!UICONTROL Relatórios Personalizados]** no painel esquerdo e selecione **[!UICONTROL Transcrições do aluno]** da lista.
1. Na guia **[!UICONTROL Transcrições do aluno]** , clique em **[!UICONTROL Gerar novo]** no canto superior esquerdo.
1. Selecione as datas preferenciais clicando em **[!UICONTROL Selecionar intervalo de datas]** menu suspenso. Clique em **[!UICONTROL IDs de e-mail]** para inserir a lista copiada de ids de email exclusivas.

   ![](assets/cp-copy-paste-feature.png)

   *Copiar e colar IDs de e-mail*

1. Uso **[!UICONTROL Validar Ids De Email]** para verificar se a id inserida está correta.

   ![](assets/cp-learnertran-gdpr.png)

   *Validar as IDs de email*

   Caso a ID de e-mail inserida esteja incorreta, ela será destacada em vermelho juntamente com uma mensagem de validação como acima.

   **[!UICONTROL Gerar]** O botão não estará disponível a menos que todas as IDs de e-mail inseridas estejam corretas.

   ![](assets/cp-copy-paste-generate.png)

   *Gerar as transcrições do aluno*

1. Clique em **[!UICONTROL Gerar]** para gerar transcrições do aluno para todas as IDs de e-mail mencionadas. Você receberá uma mensagem de confirmação, como abaixo, informando a geração do relatório.

   ![](assets/cp-copy-paste-gmessage.png)

   *Mensagem de confirmação do relatório que está sendo gerado*

   Gerar transcrições do aluno pode ser combinado para IDs de e-mail inseridas em ambos **[!UICONTROL Usuários]** e **[!UICONTROL IDs de e-mail]** guia.

## Histórico de downloads de transcrição do aluno {#ltdownload}

Na guia **[!UICONTROL Transcrição do aluno]** página de download, para gerar um relatório, ao clicar no botão **[!UICONTROL Gerar novo]** , a caixa de diálogo Transcrições do aluno é exibida.

![](assets/history-lt.png)

*Gerar um relatório de todas as transcrições do aluno*

Clique em **[!UICONTROL Opções avançadas]** e expanda o painel.

Escolha os usuários e o catálogo ao qual eles pertencem. Depois de clicar no botão **[!UICONTROL Gerar]** , uma caixa de diálogo é exibida mencionando o tempo aproximado que será necessário para baixar o relatório. Para gerar o relatório, clique em **[!UICONTROL Gerar]**.

![](assets/download-learnertranscripts.png)

*Selecione o botão Gerar*

A transcrição é gerada em segundo plano, e você pode continuar com suas tarefas no Learning Manager. Depois que a transcrição é gerada, você pode baixar a transcrição na lista.

Como administrador, você pode exibir todas as transcrições geradas por qualquer pessoa no sistema.

![](assets/download-history.png)

*Exibir histórico de downloads*

A lista de download exibe os seguintes atributos:

* **Alunos:** Os alunos/grupos de alunos cujas transcrições devem ser baixadas.
* **Dados adicionais incluídos:** Depende dos dados adicionais que o administrador deseja baixar da opção Avançado no modal Adicionar transcrição do aluno
* **Status:** Baixado, enfileirado ou em andamento.
* **De** e **Para**: Duração das transcrições a serem baixadas.
* **Filtros aplicados:** Se você aplicou os filtros para o Status de Inscrição.
* **Gerado por:** A ID do usuário do Learning Manager que solicitou o download.
* **Status:** Baixado, enfileirado ou em andamento.

Você pode cancelar o download a qualquer momento. Se uma tarefa for cancelada pelo administrador, o Learning Manager enviará uma notificação no aplicativo para o usuário que acionou a transcrição do aluno.

![](assets/queued-status.png)

*Fila de download da transcrição do aluno*

Você pode **cancelar** o download a qualquer momento. Se uma tarefa for cancelada, o Learning Manager enviará uma notificação no aplicativo ao usuário que cancelou a tarefa.

## Dados de alunos excluídos {#dataofdeletedlearners}

Você pode incluir os dados dos alunos excluídos na lista de transcrição do aluno. Na caixa de diálogo Transcrições do aluno, ative a opção **[!UICONTROL Incluir dados de alunos excluídos]**.

Depois de ativar a opção e clicar em **[!UICONTROL Gerar]**, os recursos de dados dos alunos excluídos na página de download da transcrição do aluno, conforme mostrado abaixo:

![](assets/deleted-learnersondownloadpage.png)

*Exibir dados de alunos excluídos*

## Personalizar colunas {#customize-columns-lt}

Um administrador pode personalizar as colunas exportadas em um relatório de transcrição do aluno. Administradores, administradores personalizados e gerentes podem configurar as colunas antes de exportar o relatório.

Na guia **[!UICONTROL Transcrições do aluno]** , clique em **[!UICONTROL Opções avançadas]**. No menu **[!UICONTROL Configurar formato de exportação]** escolha as colunas que deseja exportar.

![](assets/image024.png)

*Personalizar colunas para exportar*

A personalização é permitida somente quando um usuário baixa a transcrição do aluno no formato .CSV. Quando baixada no formato .XLSX, a seleção de preferência de coluna não será honrada e todas as colunas padrão serão exportadas.

## Conteúdo do arquivo de transcrição do aluno {#learnertranscriptfilecontent}

Um arquivo de transcrição do aluno típico consiste em seis planilhas do Excel em um único arquivo. As folhas de transcrição do aluno fornecem uma visão geral dos dados, incluindo o número de alunos envolvidos por curso, suas habilidades, a porcentagem de conclusão com base no curso ou aluno e um painel de conformidade. Estes são os painéis disponíveis nas transcrições do aluno:

**Transcrição do aluno**

Na folha de excel de transcrição do aluno, juntamente com os detalhes do perfil sobre o aluno, os detalhes de consumo de um objeto de aprendizado são fornecidos, como data de inscrição, data de início, nota obtida, pontuação do questionário obtida. Se os cursos fizerem parte de qualquer programa de aprendizado, eles serão listados separadamente, além dos detalhes individuais de consumo do curso.

**1 - Painel da atividade de aprendizado**

Neste painel específico do OA, você pode ver o número de alunos de cada curso, programa de aprendizado ou certificação. Você pode exibir a planilha de progresso dos alunos de um objeto de aprendizado específico. Essa planilha exibe dados como o número de alunos que concluíram o curso ou o programa de aprendizado, os alunos em andamento e as datas de vencimento dos alunos.

O progresso dos usuários para o curso específico é calculado com base nos Campos de entrada, onde você especifica a data de vencimento e os limites de porcentagem de progresso. Por exemplo, se você especificar 7 dias e 70% como valores no campo de entrada, é exibido o progresso do curso para os cursos vencidos em 7 dias, e para os cursos que têm mais de 70% de progresso. Você também pode alterar o período nesta planilha, em que os dados modificados são exibidos automaticamente neste painel.

**2 - Painel da atividade de aprendizado**

Esse painel de aprendizado exibe dados para um usuário específico. Nesse painel, você pode ver os cursos, programas de aprendizado ou certificações nos quais um usuário específico se inscreveu. A tabela também exibe dados sobre quais objetos de aprendizado o usuário concluiu, os objetos de aprendizado em andamento e as datas de vencimento iminentes do usuário.

O progresso dos usuários em cada curso é calculado com base nas entradas especificadas. Ou seja, os valores de data de vencimento e porcentagem de andamento. Por exemplo, se você especificar 7 dias e 70% como valores no campo de entrada, é exibido o progresso de cursos diferentes para os cursos vencidos em 7 dias, e para os cursos que têm mais de 70% de progresso.

**Habilidade**

Na planilha de habilidades, são fornecidos o nome da habilidade, o nível de habilidade, os créditos necessários, os créditos ganhos, a porcentagem de conclusão e outros detalhes do perfil. Um instantâneo de amostra da planilha habilidades do Excel é fornecido abaixo para referência.

![](assets/skills-learner-transcript.png)

*Amostra da planilha de habilidades do Excel*

**1 - Painel de habilidade**

Nesse painel, você pode ver se sua organização está equipada com várias habilidades. Para uma habilidade específica, você pode verificar o número de usuários em uma organização que devem ter essa habilidade em comparação com o número que realmente tem a habilidade. Esse painel também especifica os usuários que devem atualizar suas habilidades. Esse valor é calculado com base na entrada inserida no campo Entrada. Por exemplo, se você inserir 50 dias como entrada, o painel fornecerá dados sobre os usuários que precisam que suas habilidades sejam atualizadas após 50 dias.

**2 - Painel de habilidade**

Esse painel de habilidades é mais específico do usuário. Você pode filtrar um usuário específico ou vários usuários e exibir seu nível de habilidade como um painel. Essa planilha pode ajudar gerentes e administradores a controlar o nível de qualificação de cada aluno em comparação com o nível de qualificação esperado. O painel Habilidade também ilumina os alunos que precisam atualizar suas habilidades. A lista de atualização de alunos é calculada com base no número de dias inserido no campo de entrada.

**Painel de Conformidade**

O Painel de conformidade tem duas partes: relatório de conformidade por usuário e relatório de conformidade por treinamento. Para o relatório baseado no usuário, você pode usar o Painel de Conformidade para rastrear usuários com datas de vencimento iminentes para iniciativas de conformidade importantes. Para o relatório baseado em treinamento, você pode filtrar por programa de aprendizado ou certificação.

Para ambos os relatórios de conformidade, filtre pela data de vencimento para exibir os dados apropriados.

### Colunas de data e hora na transcrição {#datetime}

Os valores nas colunas a seguir têm minutos arredondados para o minuto mais próximo e segundos para 00:

* Data de inscrição (Fuso horário UTC)
* Data de início (Fuso horário UTC)
* Data de conclusão (Fuso horário UTC)

![](assets/time-columns-in-thetranscript.png)

*Colunas de data e hora na planilha do Excel*

### Colunas de duração do módulo e ID na transcrição {#moduledurationandidcolumnsinthetranscript}

A transcrição do aluno também exibe as colunas- **[!UICONTROL Duração do módulo]** e **[!UICONTROL ID]**.

![](assets/lt-id-duration.png)

*Colunas de duração do módulo e ID na transcrição*

### OUTRAS colunas na transcrição {#ModuledurationandIDcolumnsinthetranscript-1}

| **Coluna** | **Descrição** |
|---|---|
| Depois | Número de alunos que obtiveram a habilidade antes do número de dias inserido (valor), o qual precisa ser atualizado |
| Habilidade | Os nomes das habilidades atribuídos aos alunos |
| Nome do Gerente | O nome do gerente cujos dados de envolvimento de habilidade subordinados devem ser exibidos na tabela de resumo Habilidade |
| Rótulos de linha | O nome do aluno com a lista de habilidades atribuídas |
| Número de habilidades que cada usuário deve ter | Número de habilidades atribuídas ao aluno |
| Número de habilidades que cada usuário possui | Número de habilidades obtidas pelo aluno |
| Número de habilidades que precisam de atualização | Número de alunos cuja habilidade precisa ser atualizada |
| Porcentagem de conformidade | A porcentagem de progresso da habilidade atribuída |
| Caminho incorporado | Essas linhas mostrarão o nome do programa de aprendizado incorporado. |
| ID do caminho incorporado | Essas linhas mostrarão as IDs do programa de aprendizado incorporado |
| Idioma do caminho incorporado | Essas linhas exibirão o idioma em que o programa de aprendizado foi criado. |
