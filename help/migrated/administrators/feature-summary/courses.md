---
description: Este documento consiste na ajuda para criar módulos, instâncias e cursos para a função de administrador.
jcr-language: en_us
title: Criar instâncias do curso e programações de aprendizado
contentowner: manochan
exl-id: aba7417b-26a0-4160-878c-5814f84e5155
source-git-commit: 139e9224f94e6a39f497b45f5bdc600121a77bc8
workflow-type: tm+mt
source-wordcount: '4866'
ht-degree: 61%

---

# Criar instâncias do curso e programações de aprendizado

Este documento consiste na ajuda para criar módulos, instâncias e cursos para a função de administrador.

O autor cria cursos. Os alunos podem realizar os cursos e os administradores podem acompanhar o desempenho dos alunos com base no aproveitamento curso.

## Visão geral {#overview}

O autor cria cursos. Os alunos podem, então, realizar os cursos e os administradores podem acompanhar o desempenho dos alunos com base no aproveitamento do curso. Os administradores podem visualizar os cursos criados pelos autores e executar algumas atividades conforme explicado nesta seção. Como administrador, você pode criar programas de aprendizado únicos com um conjunto predefinido de cursos para os alunos.

## Criar a instância de um curso {#createinstanceofacourse}

### Gerenciar instâncias

>[!INFO]
>
>Neste treinamento, você aprenderá como editar detalhes e propriedades da instância.<br><br>[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=P79NQK8R&amp;mv=display&amp;mv2=display#/course/8318912)</br></br>


Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

### Como criar uma instância

Depois que um autor cria um curso, é possível criar as instâncias do curso. Ao criar as instâncias de um curso, você pode fornecer o mesmo curso a seus alunos em períodos de tempo diferentes. Os alunos podem escolher qualquer instância e se inscrever. É possível configurar cada instância para que tenha seu próprio conjunto de medalhas, feedback e outras configurações.

Para criar uma instância,

1. No aplicativo do administrador, clique em **[!UICONTROL Cursos]** no painel esquerdo.
1. Na lista de cursos, escolha o curso necessário e clique em **[!UICONTROL Exibir curso]**.

   ![](assets/view-course.png)

   *Exibir um curso*

1. Para criar instâncias, clique em **[!UICONTROL Instâncias]** no painel esquerdo. Por padrão, todo curso tem uma instância. Você pode modificar a instância padrão ou adicionar instâncias. Não é possível excluir essa instância do curso.
1. Para criar uma instância, clique em **[!UICONTROL Adicionar nova instância]** no canto superior direito das informações do curso. Uma nova instância do curso é exibida.
1. Insira as propriedades da instância:

   * No campo **[!UICONTROL Nome da instância]**, insira o nome da instância que você deseja associar ao curso. Certifique-se de usar um nome exclusivo para a instância.
   * Especifique o prazo de conclusão para a instância. Os alunos devem atingir o status de conclusão do curso até esta data.
   * Clique em **[!UICONTROL Mostrar mais opções]** para exibir outras opções de prazo.
   * **[!UICONTROL Prazo de inscrição]:** esta é a data até a qual um aluno deve se inscrever em um objeto de aprendizado em caso de autoinscrição.
   * **[!UICONTROL Prazo de cancelamento da inscrição]:** Você pode optar por restringir o cancelamento de inscrição pelo próprio aluno, estabelecendo um prazo para o cancelamento da inscrição.
   * **[!UICONTROL Fuso horário]:** Pesquise e selecione o **[!UICONTROL Fuso horário]** na lista suspensa.

   Um administrador pode decidir ter prazos de conclusão para um curso ou programa de aprendizado com base em requisitos. No entanto, é recomendável ter um prazo para os treinamentos com base em sala de aula/sala de aula virtual.

   ![](assets/create-an-instance.png)

   *Definir prazo de conclusão*

### Exibir propriedades de uma instância {#viewpropertiesoftheinstance}

![](assets/properties-of-aninstance.png)

*Exibir propriedades da instância*

1. **Módulos:** número de módulos criado pelo autor do curso
1. **Alunos inscritos:** número de alunos inscritos no curso pelo administrador.
1. **Sessões:** número de módulos de sala de aula virtual e de sala de aula no curso.
1. **Feedback habilitado:** exibe se os comentários L1, L2 e L3 estão habilitados neste curso.

>[!NOTE]
>
>O administrador cancela as sessões acessando Instâncias > Sessões e selecionando Cancelar sessão.

### Retirar uma instância {#retireaninstance}

Para retirar uma instância, execute as etapas abaixo.

1. Na instância, clique no menu suspenso e escolha a opção **[!UICONTROL Retirar instância]**.

   ![](assets/retire-an-instance.png)

   *Desativar uma instância*

1. Para procurar todas as instâncias retiradas, clique na guia **[!UICONTROL Retirada]** na página Instâncias.

### Restaurar uma instância {#restoreaninstance}

Para restaurar uma instância retirada, execute as seguintes etapas:

1. Na instância, clique no menu suspenso e escolha a opção **[!UICONTROL Reabrir instância]**.

   ![](assets/restore-an-instance.png)

   *Restaurar uma instância*

1. A instância agora é redefinida para um modo ativo.

### Deletar uma instância

Os administradores podem excluir a instância usando a opção **Excluir esta instância** imediatamente após a criação. Não é possível excluir instâncias se houver uma sessão vinculada a ela ou se algum aluno estiver inscrito nela.

![](assets/delete-this-instance.png)

*Excluir uma instância*

>[!NOTE]
>
>Não é possível excluir a instância padrão.

### Enviar e-mails em nível de instância

Para enviar e-mails em nível de instância aos alunos inscritos:

1. Na página **[!UICONTROL Instâncias]**, selecione as opções em qualquer instância e clique em **[!UICONTROL Enviar Email aos Alunos Inscritos]**.

![emails em nível de instância](assets/adhoc-email.png)

*Enviar email aos alunos inscritos na instância*

1. Na caixa de diálogo **[!UICONTROL Criar Comunicado]**, selecione Digitar como Email. Especifique o assunto, digite a mensagem e clique em **[!UICONTROL Salvar]**. O treinamento é selecionado automaticamente.

   ![Criar comunicado como email](assets/email-announcement.png)

   *Criar comunicado como email*

1. Depois de clicar em **[!UICONTROL Salvar]**, você verá uma mensagem de confirmação pela criação bem-sucedida do comunicado. Para publicar o comunicado, clique em **[!UICONTROL Publicar agora]**.

   ![Comunicado criado com êxito](assets/announcement-successful.png)

## Inscrever alunos nos cursos

Neste treinamento, você aprenderá como se inscrever, cancelar a inscrição e reinscrever alunos.

[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=PC1PQFJQ&amp;mv=display&amp;mv2=display#/course/8318916)

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

### Inscrever alunos em várias instâncias

1. Selecione um curso da lista de cursos.
1. Selecione **[!UICONTROL Alunos]** no painel esquerdo.
1. Selecione **[!UICONTROL Inscreva-se]**.

   ![Inscrever alunos](assets/enroll-learners-new.png)

   *Publish o curso*

1. Na caixa de diálogo [!UICONTROL **Inscrever alunos**], é possível:

   * Selecione uma instância para inscrever um aluno na lista suspensa Selecionar instância.
   * Selecione o usuário ou os grupos de usuários ou ambos no campo Incluir alunos.
   * Selecione os alunos que você deseja excluir da instância no campo Excluir alunos.
   * Na parte inferior da caixa de diálogo, selecione Sim se quiser que um ou mais alunos se inscrevam na instância selecionada.

1. Selecione **[!UICONTROL Continuar]**.

   ![continuar](assets/proceed.png)

   *Inscrever alunos*

### Exibir relatório de inscrição de uma instância

1. Selecione um curso da lista de cursos.
1. Selecione **[!UICONTROL Alunos]** no painel esquerdo.
1. Selecione **[!UICONTROL Ações]** > **[!UICONTROL Exportar]**.

O arquivo do Excel contém planilhas para cada instância. Uma planilha consiste nos campos:

* Alunos
* Email
* ID exclusiva do usuário
* Nome do curso
* ID exclusiva do OA
* Status
* Critérios de seleção
* Data de inscrição/Data de cancelamento da inscrição (fuso horário UTC)
* Data de conclusão (fuso horário UTC)
* Data de vencimento (fuso horário UTC)
* Data de início (fuso horário UTC)
* Pontuação do questionário
* Nome do gerente
* Endereço
* userState
* Área de especialização
* Comentários
* Número de visitas
* Datas de visita
* Carimbos de data/hora (fuso horário UTC)
* Tempo gasto (min)

>[!NOTE]
>
>Habilitar o recurso de Várias inscrições resulta na adição de várias linhas ao Relatório de transcrição do aluno para cada curso (uma linha para cada instância).
>
>Se você tiver uma configuração de automação de relatórios que prevê apenas uma linha por curso, deverá fazer os ajustes necessários na automação de relatórios antes de ativar o recurso de Várias Inscrições.

### Gerenciar a lista de alunos de um curso {#managelearnerslistforacourse}

1. Clique no nome do curso na miniatura do curso.
1. No painel esquerdo, clique em **[!UICONTROL Alunos]**.

![](assets/courses-learners.png)

*Selecionar alunos em um curso*

Na página Alunos, você pode executar as seguintes ações:

* Selecione o aluno que deseja remover e clique em [!UICONTROL **Ações**] > [!UICONTROL **Remover**].
* Selecione o aluno cuja participação você deseja marcar e clique em [!UICONTROL **Ações**] > [!UICONTROL **Marcar como concluído**].

Para permitir que os alunos redefinam um módulo e o consumam novamente, clique em [!UICONTROL **Redefinir**]. Na caixa de diálogo pop-up, clique em Sim para confirmar a redefinição. Os módulos que foram concluídos não podem ser redefinidos. Somente os módulos falhos ou incompletos podem ser redefinidos.

Você também pode exportar a lista de alunos para uma planilha do Excel. Para exportar a lista de alunos, clique em [!UICONTROL **Ações**] > [!UICONTROL **Exportar**].

>[!NOTE]
>
>Se houver várias instâncias em um curso, a lista de alunos é fornecida em guias separadas no Excel. A lista de alunos contém o nome do aluno, o status e os critérios de seleção. O status dos alunos pode ser **Não iniciado**, **Em andamento** ou **Concluído**.

### Exportar alunos no estado de aprovação pendente

Um administrador, gerente ou administrador personalizado pode exportar dados de alunos que estão no estado de inscrição de aprovação pendente. Você pode exportar os dados por meio da guia **Curso > Aluno** e clicar na lista suspensa Ação.

A opção estará presente quando nenhum aluno estiver inscrito/com aprovação pendente no curso aprovado pelo gerente e um relatório vazio será gerado. Você também pode exportar quando os alunos estiverem no estado de aprovação pendente, no estado inscrito, no estado pendente e no estado não inscrito.

O relatório contém dados de usuários ativos, excluídos e suspensos se estiverem pendentes de aprovação. Além disso, o relatório contém dados de usuários internos e externos que estão no estado de aprovação pendente.

Se um aluno que estava antes no estado de aprovação pendente cancelar a inscrição, o seu registro não estará presente no relatório. Além disso, se um aluno que estava anteriormente no estado de aprovação pendente estiver inscrito no curso pela inscrição de administrador/gerente/administrador personalizado, o seu registro estará presente no relatório.

## Lista de espera

A seção Lista de espera permite que os alunos estejam em lista de espera para cursos em sala de aula quando as vagas são limitadas, com base na ordem de inscrição. Os administradores podem gerenciar isso selecionando alunos na lista de espera e alocando vagas além do limite inicial. Depois que uma vaga é alocada pelo administrador, o aluno é imediatamente inscrito no curso.

## Exportar participação dos alunos {#attendance}

Para qualquer curso de sala de aula e sala de aula virtual, você pode baixar a lista de alunos que participaram de qualquer instância deste curso.

Na página de detalhes do curso, clique em **[!UICONTROL Participação e Pontuação]** no painel direito.

No canto superior direito da página, clique na lista suspensa **[!UICONTROL Ações]**. Em seguida, clique na opção **[!UICONTROL Exportar lista de alunos (PDF)]**.

![](assets/export-list-of-learners.png)

*Exportar lista de alunos como PDF*

No PDF, é possível visualizar o mesmo grupo de alunos visualizado pelo professor.

Ao baixar o PDF, é possível ver o fuso horário (em UTC) usado ao criar o curso.

## Adicionar feedback N1 e N3 {#addl1andl3feedback}

É possível adicionar opções de feedback N1 e N3 ao criar cursos:

1. Clique em Cursos no painel esquerdo depois de fazer logon como administrador. A lista de todos os cursos é exibida na página do lado direito.
1. Clique no quadro do curso ao qual você deseja adicionar o feedback N1 ou N3.
1. Clique no padrão da instância no painel esquerdo.
1. Clique no círculo no botão de alternância ao lado do feedback N1 ou N3 para habilitá-lo.
1. Adicione pergunta de feedback N3 na área de texto abaixo da pergunta N3.

### Feedback L1 obrigatório {#mandatory-l1-feedback}

Você pode tornar todas as perguntas ou a primeira pergunta obrigatórias em um feedback N1.

![](assets/make-all-questionsmandatory.png)

*Tornar todas as perguntas ou a primeira pergunta obrigatórias em um feedback N1*

Você já pode criar as perguntas, que agora se tornam obrigatórias.

![](assets/create-mandatoryquestions.png)

*Criar as perguntas*

Se as duas perguntas obrigatórias, por algum motivo, não tiverem texto, as perguntas não aparecerão no formulário de feedback.

>[!NOTE]
>
>Não basta ativar essas configurações na instância do Programa de aprendizado. Você também deve ativar essas configurações no nível da Instância do curso para cada curso no Programa de aprendizado.

Na página Padrões de Instância, se você habilitar **[!UICONTROL Tornar Todas as Perguntas Obrigatórias]**, todas as novas instâncias criadas posteriormente herdarão essas configurações.

![](assets/instance-defaults-makeallquestionsmandatory.png)

*Exibir a página Padrões de Instância*

### Feedback L1 no nível do curso {#l1-feedback-course-level}

Nas versões anteriores do Learning Manager, um administrador podia ativar o feedback L1 para o Programa de Aprendizado.

Nesta versão do Learning Manager, o administrador pode enviar feedback L1 para todos os cursos que fazem parte do Programa de Aprendizado. O administrador deve garantir que o feedback L1 esteja ativado para todos os cursos no nível da instância do curso.

1. Para habilitar o feedback L1 para cada curso, no aplicativo Admin, clique em **[!UICONTROL Programas de Aprendizado]** > **[!UICONTROL Exibir Programa de Aprendizado]**.

1. Clique Em **[!UICONTROL Instâncias]** > **[!UICONTROL Feedback N1 Habilitado]**.

1. Habilite a opção **[!UICONTROL Habilitar para Cada Curso]**.

   ![](assets/enable-l1-feedbackforcourse.png)

   *Habilitar comentários sobre o curso*

   Ativar essa alternância apenas no nível do Programa de aprendizado não acionará o feedback L1 para os cursos dentro deste programa. Para ativar o feedback L1, vá para cada curso no Programa de aprendizado e ative a alternância do feedback L1.

   ![](assets/l1-reaction-feedback.png)

   *Habilitar feedback L1 para cada curso*

   Se o feedback L1 estiver ativado para todos os cursos, mas estiver desativado na instância do programa de aprendizado, o feedback L1 não será acionado para os cursos.

### Relatórios de quiz específicos do idioma

Os relatórios do quiz ajudam a avaliar o desempenho de um aluno após a conclusão de um programa de aprendizado ou curso.

Atualmente, o Learning Manager facilita o aprendizado em 13 idiomas de interface e 32 idiomas de conteúdo. Embora essa opção seja amigável para o aluno e ofereça conveniência na compatibilidade com nossos alunos globais, é de suma importância que os administradores busquem relatórios tentados em vários locais.

Os relatórios do questionário exibem dados em diferentes idiomas, desde que o curso esteja sendo oferecido em vários idiomas. Até agora, os relatórios gerados pelo administrador exibiam as respostas uma abaixo da outra, independentemente do idioma em que o quiz foi tentado. **Por exemplo**, se um usuário fez um quiz em holandês, o administrador só poderá exibir os relatórios do quiz tentados por usuários em holandês de cada vez. O administrador que selecionou o inglês como um idioma de interface não pode exibir os relatórios de todos os usuários de uma só vez, independentemente do local tentado.

Isso foi corrigido e o administrador agora pode exibir todos os relatórios no respectivo idioma que o aluno tentou tudo de uma vez, independentemente do local do conteúdo escolhido. O questionário tentado em idiomas diferentes será adicionado como colunas adicionais no relatório do questionário.

### Habilitar feedback L1 no nível da conta {#l1-feedback-account-level}

*Habilitar feedback L1 no nível da conta*

Um administrador poderá ativar o feedback L1 para cursos recém-criados e programas de aprendizado ativando essa configuração no nível da conta. No entanto, ativar essa configuração não afeta os cursos e programas de aprendizado existentes

Se habilitado, todos os novos treinamentos e novas instâncias terão o feedback habilitado por padrão. Caso um autor/administrador visite a instância, ela é padronizada e desativada manualmente e, em seguida, é respeitada.

Para habilitar o feedback N1, no aplicativo Admin, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Comentários]**.

![](assets/l1-feedback-settings.png)

*Exibir a página Configurações de Comentários*

Clique em **[!UICONTROL Editar]** no canto superior direito e alterne a opção para habilitar o feedback L1.

Quando um autor cria um curso, na página Instância do aplicativo do administrador, o **[!UICONTROL feedback N1]** é habilitado automaticamente para o novo curso.

<!--![](assets/l1-feedback-enabled.png)-->

Você também pode desabilitar o feedback L1 alternando a opção **[!UICONTROL Habilitar]**, conforme mostrado abaixo:

![](assets/disable-l1-feedback.png)

*Habilitar ou desabilitar o feedback L1*

### Adicionar perguntas descritivas para feedback N1 e N3 {#descriptive}

Como parte da versão de novembro do Learning Manager, foi fornecida uma opção para adicionar perguntas descritivas. Os administradores têm a opção de adicionar essas perguntas aos alunos. Essa condição está também no conjunto padrão de perguntas fornecidas pelo Learning Manager. Você também pode torná-los obrigatórios se necessário selecionando a opção abaixo da pergunta.

Você pode adicionar duas perguntas descritivas do feedback N1 e uma pergunta descritiva do feedback N3.

Ao habilitar o feedback N1, você pode ver as opções conforme mostrado na imagem a seguir.

![](assets/l1-feedback-desc-questions.png)

*Adicionar perguntas descritivas para feedback N1 e N3*

Se quiser que o questionário seja exibido ao aluno imediatamente após a conclusão do curso, você poderá escolher tal opção.

É fornecido abaixo para referência o resultado de amostra de um questionário N1. Os alunos podem ver o questionário no formato abaixo. Teste 1 e Teste 2 são perguntas descritivas.

![](assets/l1-output.png)

*Um exemplo de perguntas de feedback sobre o curso*

Depois de ativar o feedback N3, você pode visualizar as opções conforme mostrado na captura de tela abaixo:

![](assets/l3-feedback-desc-questions.png)

*Habilitar feedback N3*

A pergunta 2 é uma pergunta descritiva do feedback N3. Você pode torná-la obrigatória clicando na opção abaixo da pergunta.

É fornecido abaixo para referência o resultado de amostra de um questionário N3. Os alunos podem ver o questionário no formato abaixo.

![](assets/l3-output.png)

*Exibir saída do feedback N3*

### Configurar o questionário de feedback N1 e N3 {#setupl1andl3feedbackquestionnaire}

Você pode configurar o questionário de feedback N1 e N3 e também definir lembretes no nível da conta.

1. Clique em **[!UICONTROL Configurações]** e depois em **[!UICONTROL Comentários]** no painel esquerdo depois de fazer logon como administrador.\
   A página de configurações do feedback é exibida com duas guias: **[!UICONTROL Comentários N1]** e **[!UICONTROL Comentários N3]**.\
   A guia **[!UICONTROL Comentários N1]** consiste em uma lista de questionário de **[!UICONTROL comentários N1]** padrão para cursos em sala de aula e em ritmo individualizado juntamente com as configurações do lembrete. Na guia **[!UICONTROL Feedback N3]**, você pode ver a instrução padrão do feedback N3 e as configurações padrão.

1. Clique em Editar no canto superior direito da página para modificar o questionário já existente.\
   Na guia **[!UICONTROL Feedback N1]**, você pode habilitar/desabilitar cada pergunta clicando no botão de alternância Sim/Não.\
   Na guia **[!UICONTROL Feedback N3]**, você pode modificar a instrução padrão do feedback.\
   Clique em **[!UICONTROL Adicionar novo lembrete]** na parte inferior da página e escolha quando enviar os lembretes.

1. Clique em **[!UICONTROL Salvar]** no canto superior direito da página.

No feedback N1, você pode exibir dois conjuntos de questionário junto com uma pergunta padrão. O primeiro conjunto de questionário se refere a cursos em ritmo individualizado que também pode ser usado para cursos baseados em atividade. O segundo conjunto de questionário pode ser usado para os tipos de cursos em sala de aula e sala de aula virtual.

## Exibir feedback N1 e N3 {#viewl1andl3feedback}

Você pode ver o feedback N1 fornecido a um curso pelos alunos e o feedback N3 fornecido aos alunos pelos gerentes.

1. Clique em qualquer quadro do curso na lista de cursos.
1. Clique em Feedback N1 ou Feedback N3 no painel esquerdo para ver os comentários recebidos.
1. Selecione a instância na lista suspensa para ver o feedback dessa instância específica.

## Quadro de discussão

O recurso Quadro de discussão permite que os alunos visualizem as discussões do curso. Como administrador, você pode excluir qualquer comentário, conforme necessário. Os administradores podem ativar essa opção nas configurações do curso.

## Moderação do curso {#coursemoderation}

Sempre que um autor adiciona, atualiza ou exclui módulos e republica um curso, todos os administradores recebem notificações. Como administrador, você pode ver as alterações, comparar o conteúdo antigo e o novo clicando no link, bem como aprovar ou rejeitar as alterações.

Para habilitar a Moderação do Curso, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Geral]**. Marque a caixa de seleção **[!UICONTROL Moderação do curso]** para habilitar esse recurso.

![](assets/2.png)

*Habilitar a moderação do curso*

Clique na notificação para ver as alterações que o autor fez no curso. Em seguida, aprove ou rejeite as alterações feitas pelo autor. Se você aprovar, o curso é republicado. Se rejeitar as atualizações, a versão anterior do curso continuará a existir. Em qualquer um dos casos, uma notificação é enviada para o autor.

![](assets/1.png)

*Criar solicitações para atualizações de curso*

Se houver vários autores atualizando o mesmo curso, a alteração mais recente será contemplada na notificação do administrador. Em seguida, você pode aprovar ou rejeitar as alterações mais recentes.

## Exportar dados da lista de verificação {#export-checklist-data}

Na lista de cursos, abra um curso que contenha uma lista de verificação. No painel esquerdo, você verá uma opção **[!UICONTROL Lista de verificação]**.

![](assets/export-checklist.png)

*Exportar dados da lista de verificação*

Clique na opção e, na página do curso, realize o seguinte procedimento:

1. Selecione a instância e o módulo.
1. Clique em **[!UICONTROL Ações]** > **[!UICONTROL Exportar]** e exporte o relatório da lista de verificação do aluno.

Na página **[!UICONTROL Lista de verificação]**, um professor pode exportar o relatório da lista de verificação da lista suspensa **[!UICONTROL Ações]**.

O relatório CSV contém os seguintes campos:

* Nome de usuário
* E-mail do usuário
* Nome do gerente e e-mail
* Nome do treinamento
* Instância de treinamento
* Nome e e-mail do professor
* Enviado em
* Status da avaliação
* Perguntas com texto real
* Estado do usuário
* Perfil
* Campo(s) ativo(s)

Ao baixar um relatório após selecionar um filtro de status, o relatório de transcrição do aluno baixado irá conter os dados do aluno com base no filtro de status aplicado. Esse filtro adicionado também será exibido para o Administrador e Gerente Personalizado quando estiverem prestes a gerar uma Transcrição do Aluno.

## Exibição de cursos {#viewingcourses}

Como administrador, você pode exibir uma lista de todos os cursos disponíveis.   Clique em **[!UICONTROL Cursos]** no painel esquerdo para exibir a lista de cursos com opções de pesquisa e filtro. Você também pode ver a porcentagem da eficácia de cada um dos cursos nas miniaturas do curso.

>[!NOTE]
>
>Você pode retirar um curso depois que os alunos fizerem o curso ou quando quiser reservar um curso em particular depois de publicado. Um curso só pode ser retirado quando estiver no estado Publicado. A lista de todos os cursos retirados pode ser visualizada clicando na guia **[!UICONTROL Retirado]**.

## Exibir pontuações do questionário {#viewquizscores}

1. Clique no nome do curso na miniatura do curso.
1. Clique em Pontuação do questionário no painel esquerdo.

Você pode visualizar as pontuações do questionário de qualquer curso específico com base no nome do usuário ou com base em cada pergunta. Escolha as guias Por usuário ou Por pergunta de acordo com a opção desejada.

Escolha o tipo de instância na lista suspensa para visualizar as pontuações com base em cada instância do curso.

## Instância padrão

Os administradores podem definir Medalhas, configurações de gamificação e lembretes padrão na página **[!UICONTROL Instância padrão]**. Para modificar as configurações da instância padrão, selecione **[!UICONTROL Instância padrão]** > **[!UICONTROL Editar]**.

* **[!UICONTROL Medalha]**: selecione as medalhas padrão no menu suspenso.
* **[!UICONTROL Gamificação]**: defina as configurações de gamificação, incluindo pontos para conclusão, conclusão antecipada e conclusão pontual. Os administradores têm a opção de selecionar configurações no nível da conta ou personalizar os pontos de gamificação para essa instância.
* **[!UICONTROL Feedback de reação N1]**: habilite perguntas predefinidas para feedback do aluno após a conclusão do curso, com opções para tornar as perguntas obrigatórias.
***[!UICONTROL Feedback N3 de Alteração de Comportamento]**: habilite as perguntas de feedback para o gerente do aluno na conclusão do curso.
***[!UICONTROL Configurações de Lembrete]**: defina e gerencie lembretes para prazos finais, com opções para escalonamento.

### Definir nível de escalonamento {#escalation}

Para enviar notificações por e-mail, um administrador deve escolher explicitamente o nível de escalonamento para:

* Gerente
* Gerente e Ignorar Gerenciador de Nível

![](assets/escalation-notification.png)

*Definir nível de escalonamento*

## Visualizar cursos {#previewcourses}

O administrador pode visualizar cursos clicando na opção **[!UICONTROL Visualizar como aluno]** ao visualizar os módulos do curso.

1. Clique em **[!UICONTROL Cursos]** no painel esquerdo depois de fazer logon como administrador.
1. Clique em qualquer quadro do curso na lista de cursos da página.
1. Clique em Visualizar como aluno no painel esquerdo e clique no nome do módulo na página para visualizar o módulo do curso no Player.

## Eficácia do curso {#courseeffectiveness}

A eficácia do curso é avaliada para compreender a utilidade de um curso para o aluno. É uma combinação dos resultados do feedback do aluno sobre o conteúdo do curso, dos resultados dos testes de um aluno no curso e do feedback do gerente que avalia um aluno com base nos aprendizados do curso.

O administrador pode ver a classificação da eficácia do curso nas miniaturas do curso conforme mostrado na imagem abaixo. Você pode ver a classificação desse curso como 100.

<!--![](assets/course-effectiveness-tag1.png)-->

O valor da classificação da eficácia do curso é calculado levando-se em consideração os valores dos feedbacks N1, N2 e N3. Para ver o detalhamento de cada feedback, clique no valor da eficácia do curso. Uma janela pop-up é exibida, conforme mostrado abaixo.

![](assets/course-effectiveness.png)

*Exibir eficácia do curso para feedback N1, N2 e N3*

Nessa imagem de amostra, todos os usuários receberam todos os três feedbacks, portanto, a pontuação é de 100/100. Nessa tabela, você pode compreender que, se nenhum dos três feedbacks (N1, N2 e N3) forem fornecidos a um curso, haverá um impacto negativo na eficácia total. Clique na seta para baixo no canto inferior direito da janela pop-up para ver como são feitos os cálculos da eficácia do curso.

![](assets/course-effectiveness-calculations.png)

*Cálculo de eficácia do curso*

Conforme o gráfico circular mostrado acima, o gerente atribui mais peso ao feedback N3.

## Pesquisar cursos e programas de aprendizado {#searchingcoursesandlearningprograms}

O Adobe Learning Manager permite encontrar mais facilmente os cursos/programas de aprendizado da sua escolha. Você pode pesquisar pelos cursos de duas formas:

1. Usando o campo Pesquisa. Clique no ícone de pesquisa exibido no canto superior direito. É exibido um campo de pesquisa. Digite o nome do curso ou quaisquer palavras-chave associadas aos seus cursos para localizar os cursos/programas de aprendizado. Você também pode pesquisar usando tags predefinidas como Captivate, C, Java e HTML. As tags são pesquisáveis no campo de pesquisa, o que significa que elas são exibidas no campo de pesquisa conforme você digita.
1. Filtrando a lista de cursos/programas de aprendizado usando os filtros. Você pode filtrar os cursos por status como Todos, Publicado, Rascunho e Retirado. No modo de administrador, o filtro de rascunho não é exibido.

É possível pesquisar com base em competências clicando em Competências e selecionando-as. Como administrador, você pode classificar os cursos de quatro maneiras para localizar melhor o curso necessário. Clique em Classificar por e escolha ordem alfabética crescente, ordem alfabética decrescente, data de atualização do curso ou eficácia dos cursos.

<!--![](assets/admin-sortby.png)-->

É possível ordenar os programas de aprendizado de três formas: ordem alfabética crescente, ordem alfabética decrescente e data de atualização.

## Inscrição de alunos {#enrollinglearners}

Você pode seguir as mesmas etapas para inscrever alunos em cursos, programas de aprendizado e certificações. Os gerentes também podem inscrever alunos usando as seguintes etapas.

Os administrador inscrevem alguns alunos nos cursos obrigatórios conforme os requisitos da empresa:

1. Passe o mouse sobre os quadros dos cursos publicados e clique em Inscrever alunos.\
   Como alternativa, clique no quadro de qualquer curso publicado e clique em Alunos no painel esquerdo. Será exibida uma página com uma lista de alunos. Clique em Inscrever.\
   A caixa de diálogo Inscrever alunos é exibida.

1. Selecione a instância na lista suspensa de seleção de instâncias. A lista suspensa lista todas as instâncias, incluindo as instâncias ativas, desativadas e expiradas.

>[!NOTE]
>
>O administrador pode remover quaisquer alunos registrados de um curso clicando na seta suspensa na página dos alunos e clicando em **[!UICONTROL Ações]** > **[!UICONTROL Remover]**.

![](assets/enroll-learners.png)

*Adicionar comentários ao inscrever alunos*

*Inscrever alunos*

## Usuários

+++Incluir alunos

Selecione os grupos de usuários e os alunos individuais (usando a ID de e-mail ou o nome) que deseja incluir. Adicione todos os grupos de usuários em uma interseção com o mesmo conjunto. Para adicionar outro grupo de usuários em uma união, use um novo conjunto de inclusão.

+++

+++Excluir alunos

Selecione os grupos de usuários e os alunos individuais (usando a ID de e-mail ou o nome) que deseja excluir. Adicione todos os grupos de usuários em uma interseção com o mesmo conjunto. Para adicionar outro grupo de usuários em uma união, use um novo conjunto de inclusão.

+++

## ID de e-mail do usuário

+++ID de e-mail

Copie e cole os IDs de e-mail dos alunos que deseja inscrever, separados por ponto e vírgula, vírgulas ou por espaçamento entre linhas. Use a opção **[!UICONTROL Validar IDs de e-mail]** para validar as entradas. Todas as entradas inválidas deveriam aparecer marcadas em vermelho. Remova ou corrija as entradas e continue clicando **[!UICONTROL Continuar.]**

![](assets/email-id-option.png)

*Inscrever alunos*

A caixa de diálogo de resumo é exibida com o número de usuários do conjunto de inclusão, do conjunto de exclusão e os usuários já inscritos na instância do curso.

+++

### Adicionar comentários ao inscrever alunos {#enroll-comments}

<!---![](assets/enroll-learners-dialog.png)-->

Como administrador ou gerente, você pode adicionar comentários ao inscrever alunos em um curso. Você pode mencionar informações adicionais sobre o coorte dos usuários que estão sendo inscritos. Esses dados são exportados nos relatórios do curso.

O comentário **não** é exibido ao aluno.

Quando um administrador gera o relatório do curso do aluno, qualquer comentário, se adicionado, aparece no relatório. A caixa de diálogo de resumo é exibida com o número de usuários do conjunto de inclusão, do conjunto de exclusão e os usuários já inscritos na instância do curso.

No caixa de diálogo **[!UICONTROL Inscrever alunos]**, expanda a opção **[!UICONTROL Opções avançadas]**. No campo **[!UICONTROL Comentário Adicional]**, insira o comentário necessário.

![](assets/comment-for-learner.png)

*Adicionar comentários para alunos*

## Pesquisar por usuários inscritos {#searchforusers}

Pesquise por usuários inscritos na seção Aluno do objeto de aprendizado usando a pesquisa de digitação antecipada. Usando a pesquisa de digitação antecipada, você pode pesquisar progressivamente os usuários inscritos através do nome, ID de e-mail e UUID.

![](assets/typeahead.gif)

*Passo a passo sobre como pesquisar usuários inscritos*

Esse tipo de pesquisa também é conhecido às vezes como pesquisa de preenchimento automático, pesquisa incremental, pesquisar conforme digita, pesquisa integrada ou pesquisa instantânea.

À medida que você digita o nome do aluno ou de um grupo de usuários no campo de pesquisa, uma ou mais correspondências dos termos de pesquisa são encontradas e apresentadas imediatamente.

O processo permite que você encontre o que está procurando de forma muito mais rápida e menos complicada do que executar várias pesquisas sucessivas.

Os alunos ou grupos de usuários de todas as instâncias são exibidos após uma pesquisa. Para cada aluno, a instância na qual o aluno está inscrito é exibida na coluna **[!UICONTROL Instância]**.

![](assets/search-result.png)

*Exibir resultados da pesquisa*

Usando a pesquisa de digitação antecipada, você pode:

* Ver todos os usuários, independentemente das instâncias nas quais estão inscritos.
* Ver todos os grupos de usuários que têm um ou mais usuários inscritos.

Depois que uma pesquisa é executada, você não pode filtrar alunos por instâncias. A opção de selecionar uma instância na lista suspensa **[!UICONTROL Selecionar instância]** é desabilitada.

Além disso, usando os resultados da pesquisa, você pode escolher um aluno ou grupo de usuários e executar as seguintes ações:

* Cancelar inscrição
* Marcar conclusão
* Redefinir módulo

Ao realizar uma pesquisa, a opção Cancelar inscrição > Em massa na lista suspensa Ações é desativada para o curso/programa de aprendizado.

## Compartilhar código QR com os alunos para inscrição, conclusão ou ambos {#shareqrcodewithlearnerstoenrollcompleteorboth}

No Adobe Learning Manager, os administradores podem compartilhar os códigos QR com os alunos para se inscreverem rapidamente no curso. Os três códigos QR diferentes são usados para marcar a &#39;inscrição&#39;, a &#39;conclusão&#39; ou a &#39;inscrição e conclusão&#39; de um curso.

Os alunos podem simplesmente usar o aplicativo Adobe Learning Manager para dispositivos móveis para digitalizar o respectivo código QR.

**Para baixar o código QR, faça o seguinte**:

1. Clique em **[!UICONTROL Cursos]** na seção Aprendizado no painel de navegação esquerdo.
1. Selecione um curso > **[!UICONTROL Exibir curso]**.
1. Clique em **[!UICONTROL Instâncias]** > **[!UICONTROL Mais]** > **[!UICONTROL QR code]**.

   <!--![](assets/admin-instance-edit.png)-->

1. Habilite o código QR e clique nos ícones de “Inscrever-se”, “Completar” e “Inscrever-se e completar” para baixar um pdf com o código QR de cada um. O administrador pode então compartilhar o código QR com os alunos.

   ![](assets/qr-code-download-01.png)

   *Compartilhar código QR com analistas*

## Ciclo de vida do curso {#courselifecycle}

Um ciclo de vida típico do curso é semelhante ao seguinte:

**Rascunho** - Quando um autor termina de criar um curso e o salva. Nesse estado, o curso ainda não está disponível para os alunos. Você pode excluir um curso nesse estado.

**Publicado** - quando um autor termina de publicar um curso. Nesse estado, o curso está disponível para os alunos se inscreverem.

**Retirado** - após ter publicado um curso, o autor pode movê-lo para o estado Retirado se não quiser que o curso apareça no catálogo de cursos dos alunos. Você pode republicar ou excluir um curso nesse estado.

**Excluído** - Um curso no estado Excluído é aquele que foi removido completamente do aplicativo Adobe Learning Manager. Os cursos podem ser excluídos pelos autores somente quando estiverem no estado Rascunho. Você também pode excluir cursos do estado desativado.

![](assets/lifecycle-03.png)

*Fluxo de trabalho do ciclo de vida de um curso*

## Configurações da notificação {#notificationsettings}

Como administrador, você pode ajustar as configurações de notificação. Para obter mais informações, consulte [Notificações.](user-notifications.md)

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como redefinir o módulo como administrador?

Na página Alunos de um curso, escolha o aluno ou alunos ou um grupo, clique em **[!UICONTROL Ações]** > **[!UICONTROL Redefinir módulos]**.

![](assets/reset-modules.png)

*Opção de exibição para redefinir módulos*

Depois de clicar na opção, o status dos módulos de todos os alunos selecionados será redefinido. Os módulos concluídos não serão redefinidos.

+++

+++Como adicionar o URL do curso para que os alunos sejam redirecionados diretamente para o curso?

Passe o mouse sobre um cartão do curso e clique em **[!UICONTROL Copiar URL]**. Depois de copiar o URL, os alunos podem acessar o curso diretamente com o URL.

+++

+++Como reabrir uma instância?

Para reabrir uma instância retirada, clique no menu suspenso na instância e clique em **[!UICONTROL Reabrir instância]**.

+++
