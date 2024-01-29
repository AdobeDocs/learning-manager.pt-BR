---
description: Este documento consiste na ajuda para criar módulos, instâncias e cursos para a função de administrador.
jcr-language: en_us
title: Criar módulos do curso, instâncias e programas de aprendizado
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '4544'
ht-degree: 0%

---



# Criar módulos do curso, instâncias e programas de aprendizado

Este documento consiste na ajuda para criar módulos, instâncias e cursos para a função de administrador.

Autores criam cursos. Os alunos podem realizar os cursos e os administradores podem controlar o desempenho dos alunos com base na utilização do curso.

## Visão geral {#overview}

Autores criam cursos. Os alunos fazem os cursos e os administradores podem controlar o desempenho dos alunos com base na utilização do curso. Os administradores podem exibir os cursos criados pelos autores e executar algumas atividades, conforme explicado nesta seção. Como administrador, você pode criar programas de aprendizado exclusivos com um conjunto predefinido de cursos para os alunos.

## Criar instância de um curso {#createinstanceofacourse}

Depois que um autor tiver criado um curso, você pode criar instâncias do curso. Ao criar instâncias de um curso, você pode oferecer o mesmo curso aos alunos em períodos diferentes. Os alunos podem escolher qualquer instância e se inscrever. Você pode configurar cada instância para ter seu próprio conjunto de medalhas, feedback e outras configurações.

Para criar uma instância,

1. No aplicativo Web do administrador, clique em **[!UICONTROL Cursos]** no painel esquerdo.
1. Na lista de cursos, escolha o curso necessário e clique em **[!UICONTROL Exibir curso]**.

   ![](assets/view-course.png)

   *Exibir um curso*

1. Para criar instâncias, clique em **[!UICONTROL Instâncias]** no painel esquerdo. Cada curso tem uma instância por padrão. Você pode modificar a instância default ou adicionar instâncias. Não é possível excluir esta instância do curso.
1. Para criar uma instância, clique em **[!UICONTROL Adicionar Nova Instância]** no canto superior direito das informações do curso. Uma nova instância do curso é exibida.
1. Insira as propriedades da instância:

   * No menu **[!UICONTROL Nome da Instância]** insira o nome da instância que deseja associar ao curso. Certifique-se de usar um nome exclusivo para a instância.
   * Especifique o prazo de conclusão para a instância. Os alunos devem obter o status de conclusão do curso até essa data.
   * Clique em **[!UICONTROL Mostrar mais opções]** para exibir outras opções de prazo.
   * **[!UICONTROL Prazo de Inscrição]:** Essa é a data até a qual um aluno deve se inscrever em um objeto de aprendizado em caso de autoinscrição.
   * **[!UICONTROL Prazo de Cancelamento de Inscrição]:** Você pode optar por restringir o cancelamento de inscrição pelo próprio aluno, estabelecendo um prazo para o cancelamento da inscrição.

   Um administrador pode decidir ter prazos de conclusão para um curso ou programa de aprendizado com base nos requisitos. No entanto, é recomendável ter um para treinamentos baseados em sala de aula/sala de aula virtual.

   ![](assets/create-an-instance.png)

   *Definir prazo de conclusão*

## Exibir propriedades da instância {#viewpropertiesoftheinstance}

![](assets/properties-of-aninstance.png)

*Exibir propriedades da instância*

1. **Módulos:** O número de módulos criados pelo autor do curso
1. **Alunos inscritos:** O número de alunos inscritos no curso pelo administrador.
1. **Sessões:** O número de módulos Sala de aula virtual e Sala de aula no curso.
1. **Feedback ativado:** Mostra se os feedbacks L1, L2 e L3 estão ativados para este curso.

## Desativar uma instância {#retireaninstance}

Para desativar uma instância, execute as etapas abaixo;

1. Na instância, clique no menu suspenso e escolha a opção **[!UICONTROL Desativar instância]**.

   ![](assets/retire-an-instance.png)

   *Desativar uma instância*

1. Para pesquisar todas as instâncias desativadas, clique na guia **[!UICONTROL Retirado]** na página Instâncias.

## Restaurar uma instância {#restoreaninstance}

Para restaurar uma instância desativada para um estado ativado, execute as seguintes etapas:

1. Na instância, clique no menu suspenso e escolha a opção **[!UICONTROL Reabrir instância]**.

   ![](assets/restore-an-instance.png)

   *Restaurar uma instância*

1. A instância agora é restaurada para um modo ativo.

## Enviar emails em nível de instância

Para enviar e-mails em nível de instância para alunos inscritos:

1. Na página Instâncias, selecione as opções em qualquer instância e clique em **[!UICONTROL Enviar e-mail aos alunos inscritos]**.

![e-mails em nível de instância](assets/adhoc-email.png)

*E-mail para alunos inscritos na instância*

1. Na caixa de diálogo Criar comunicado, selecione Digitar como email. Especifique o assunto, digite a mensagem e clique em Salvar. O treinamento é selecionado automaticamente.

   ![Criar comunicado como email](assets/email-announcement.png)

   *Criar comunicado como email*

1. Depois de clicar em **[!UICONTROL Salvar]**, você verá uma mensagem de confirmação para a criação bem-sucedida do comunicado. Para publicar o comunicado, clique em **[!UICONTROL Publicar agora]**.

   ![Anúncio criado com sucesso](assets/announcement-successful.png)

### Inscrever alunos em várias instâncias

1. Selecione um curso na lista de cursos.
1. Selecionar **[!UICONTROL Alunos]** no painel esquerdo.
1. Selecionar **[!UICONTROL Inscrever-se]**.

   ![Inscrever alunos](assets/enroll-learners-new.png)

   *Publicar o curso*

1. No menu [!UICONTROL **Inscrever alunos**] , você pode:

   * Selecione uma instância para inscrever um aluno na lista suspensa Selecionar instância.
   * Selecione o usuário ou os grupos de usuários ou ambos no campo Incluir alunos.
   * Selecione os alunos que você deseja excluir da instância no campo Excluir alunos.
   * Na parte inferior da caixa de diálogo, selecione Sim se quiser que um ou mais alunos se inscrevam na instância selecionada.

1. Selecionar **[!UICONTROL Continuar]**.

   ![continuar](assets/proceed.png)

   *Prossiga com a inscrição de alunos*

### Exibir relatório de inscrição de uma instância

1. Selecione um curso na lista de cursos.
1. Selecionar **[!UICONTROL Alunos]** no painel esquerdo.
1. Selecionar **[!UICONTROL Ações]** > **[!UICONTROL Exportar]**.

O arquivo do Excel contém planilhas para cada instância. Uma planilha consiste nos campos:

* Alunos
* E-mail
* ID exclusiva do usuário
* Nome do curso
* ID exclusiva do LO
* Status
* Critérios de seleção
* Data de inscrição/Data de cancelamento da inscrição (Fuso horário UTC)
* Data de conclusão (Fuso horário UTC)
* Data de vencimento (Fuso horário UTC)
* Data de início (Fuso horário UTC)
* Pontuação no quiz
* Nome do Gerente
* Endereço
* userState
* Área de especialização
* Comentários
* Número de Visitas
* Datas de Visita
* Carimbos de data e hora (Fuso horário UTC)
* Tempo gasto (min)

>[!NOTE]
>
>Observação: a ativação da inscrição múltipla resulta na adição de várias linhas ao Relatório de transcrição do aluno de cada curso (uma linha para cada instância).
>
>Se você tiver uma configuração de automação de relatórios que prevê apenas uma linha por curso, deverá fazer os ajustes necessários na automação de relatórios antes de ativar o recurso de Várias Inscrições.

## Definir nível de escalonamento {#escalation}

Para enviar as notificações por email, um administrador deve escolher explicitamente o nível de escalonamento para:

* Gerente
* Gerente e Ignorar Gerente de Nível

![](assets/escalation-notification.png)

*Definir nível de escalonamento*

## Moderação do curso {#coursemoderation}

Sempre que um autor adiciona, atualiza ou exclui módulos e republica um curso, todos os administradores recebem uma notificação sobre o mesmo. Como administrador, você pode visualizar as alterações, comparar o conteúdo antigo e o novo clicando no link e aprovar ou rejeitar as alterações adequadamente.

Para ativar a Moderação do curso, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Geral]**. Selecione o **[!UICONTROL Moderação do curso]** para ativar esse recurso.

![](assets/2.png)

*Ativar moderação do curso*

Clique na notificação para visualizar as alterações que o autor fez no curso. Em seguida, aprove ou rejeite as alterações feitas pelo autor. Se você optar por aprovar, o curso será publicado novamente. Se você rejeitar as atualizações, a versão anterior do curso continuará a existir. Em ambos os casos, uma notificação é enviada ao autor.

![](assets/1.png)

*Criar solicitações para atualizações de curso*

Se houver vários autores atualizando o mesmo curso, a alteração mais recente ou a última realizada refletirá na notificação do administrador. Você pode aprovar ou rejeitar as alterações mais recentes.

## Adicionar feedback N1 e N3 {#addl1andl3feedback}

Você pode adicionar opções de feedback N1 e N3 ao criar os cursos:

1. Clique em Cursos no painel esquerdo depois de fazer logon como administrador. A lista de todos os cursos é exibida na página do lado direito.
1. Clique no quadro do curso ao qual você deseja adicionar o feedback N1 ou N3
1. Clique no padrão da instância no painel esquerdo.
1. Clique no círculo no botão de alternância ao lado do feedback N1 ou N3 para ativá-lo.
1. Adicione pergunta de feedback N3 na área de texto abaixo da pergunta N3.

## Feedback N1 obrigatório {#mandatory-l1-feedback}

Você pode tornar todas as perguntas ou a primeira pergunta obrigatórias em um feedback N1.

![](assets/make-all-questionsmandatory.png)

*Tornar todas as perguntas ou a primeira pergunta obrigatórias em um feedback N1*

Agora, você pode criar as perguntas, que agora se tornam obrigatórias.

![](assets/create-mandatoryquestions.png)

*Criar as perguntas*

Se as duas perguntas obrigatórias, por algum motivo, não tiverem texto, as perguntas não aparecerão no formulário de feedback.

>[!NOTE]
>
>Não basta ativar essas configurações na instância do Programa de aprendizado. Você também deve ativar essas configurações no nível da Instância do curso para cada curso no Programa de aprendizado.

Na página Padrões de Instância, se você ativar **[!UICONTROL Tornar todas as perguntas obrigatórias]**, todas as novas instâncias criadas posteriormente herdarão essas configurações.

![](assets/instance-defaults-makeallquestionsmandatory.png)

*Exibir a página Defaults da Instância*

## Feedback N1 no nível do curso {#l1-feedback-course-level}

Nas versões anteriores do Learning Manager, um administrador podia ativar o feedback L1 para o Programa de Aprendizado.

Nesta versão do Learning Manager, o administrador pode enviar feedback L1 para todos os cursos que fazem parte do Programa de Aprendizado. O administrador deve garantir que o feedback L1 esteja ativado para todos os cursos no nível da instância do curso.

1. Para ativar o feedback L1 para cada curso, no aplicativo Admin, clique em **[!UICONTROL Programas de aprendizado]** > **[!UICONTROL Exibir Programa de Aprendizado]**.

1. Clique em **[!UICONTROL Instâncias]** > **[!UICONTROL Feedback L1 ativado]**.

1. Ativar a opção **[!UICONTROL Ativar para cada curso]**.

   ![](assets/enable-l1-feedbackforcourse.png)

   *Ativar feedback do curso*

   Ativar essa alternância apenas no nível do Programa de aprendizado não acionará o feedback L1 para os cursos dentro deste programa. Para ativar o feedback L1, vá para cada curso no Programa de aprendizado e ative a alternância do feedback L1.

   ![](assets/l1-reaction-feedback.png)

   *Ativar feedback L1 para cada curso*

   Se o feedback L1 estiver ativado para todos os cursos, mas estiver desativado na instância do programa de aprendizado, o feedback L1 não será acionado para os cursos.

## Relatórios de quiz específicos do idioma

Os relatórios do quiz ajudam a avaliar o desempenho de um aluno após a conclusão de um programa de aprendizado ou curso.

Atualmente, o Learning Manager facilita o aprendizado em 13 idiomas de interface e 32 idiomas de conteúdo. Embora essa opção seja amigável para o aluno e ofereça conveniência no suporte a nossos alunos globais, é de suma importância os administradores buscarem relatórios tentados em vários locais.

Os relatórios do quiz exibem dados em diferentes idiomas, desde que o curso esteja sendo oferecido em vários idiomas. Até agora, os relatórios gerados pelo administrador exibiam as respostas uma abaixo da outra, independentemente do idioma em que o quiz foi tentado. **Por exemplo:**, Se um usuário fizer um quiz em holandês, o administrador só poderá exibir os relatórios do quiz tentados por usuários em holandês de cada vez. O administrador que selecionou o inglês como um idioma de interface não pôde exibir os relatórios de todos os usuários de uma só vez, independentemente do local tentado.

Isso foi corrigido e o administrador agora pode exibir todos os relatórios no respectivo idioma que o aluno tentou tudo de uma vez, independentemente do local do conteúdo escolhido. O questionário tentado em idiomas diferentes será adicionado como colunas adicionais no relatório do questionário.

## Habilitar feedback L1 no nível da conta {#l1-feedback-account-level}

*Habilitar feedback L1 no nível da conta*

Um administrador poderá ativar o feedback L1 para cursos recém-criados e programas de aprendizado ativando essa configuração no nível da conta. No entanto, ativar essa configuração não afeta os cursos e programas de aprendizado existentes

Se ativada, todos os novos treinamentos e novas instâncias terão o feedback ativado por padrão. Caso um autor/administrador visite a instância, a instância assume o padrão e a desativa manualmente, em seguida, ela é respeitada.

Para ativar o feedback N1, no aplicativo Admin, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Feedback]**.

![](assets/l1-feedback-settings.png)

*Exibir a página Configurações de feedback*

Clique em **[!UICONTROL Editar]** no canto superior direito e ative a opção para ativar o feedback L1.

Quando um autor cria um curso, na página Instância do aplicativo do administrador, o **[!UICONTROL Feedback L1]** é ativado automaticamente para o novo curso.

<!--![](assets/l1-feedback-enabled.png)-->

Você também pode desativar o feedback L1 alternando o **[!UICONTROL Habilitar]** como mostrado abaixo:

![](assets/disable-l1-feedback.png)

*Ativar ou desativar o feedback L1*

## Adicionar perguntas descritivas para feedback N1 e N3 {#descriptive}

Como parte da versão de novembro do Learning Manager, foi fornecida uma opção para adicionar perguntas descritivas. Os administradores têm a opção de adicionar essas perguntas aos alunos. Essa condição está além do conjunto padrão de perguntas fornecidas pelo Learning Manager. Você também pode torná-las obrigatórias, se necessário, escolhendo a opção abaixo da pergunta.

Você pode adicionar duas perguntas descritivas do feedback N1 e uma pergunta descritiva do feedback N3.

Depois de ativar o feedback L1, você pode visualizar as opções conforme mostrado na captura de tela a seguir.

![](assets/l1-feedback-desc-questions.png)

*Adicionar perguntas descritivas para feedback N1 e N3*

Se quiser que o questionário seja exibido ao aluno imediatamente após a conclusão do curso, você pode escolher a opção adequadamente.

Um exemplo de saída do questionário L1 é fornecido abaixo para referência. Os alunos podem exibir o questionário no formato abaixo. Test-1 e Test-2 são as perguntas descritivas.

![](assets/l1-output.png)

*Um exemplo de perguntas de feedback do curso*

Depois de ativar o feedback N3, você pode visualizar as opções conforme mostrado na captura de tela abaixo:

![](assets/l3-feedback-desc-questions.png)

*Ativar feedback N3*

A pergunta 2 é a pergunta descritiva do feedback N3. Para torná-la obrigatória, clique na opção adequadamente abaixo da pergunta.

Um exemplo de saída do questionário L3 é fornecido abaixo para sua referência. Os alunos podem exibir o questionário no formato abaixo.

![](assets/l3-output.png)

*Exibir saída do feedback L3*

## Configurar questionário de feedback N1 e N3 {#setupl1andl3feedbackquestionnaire}

Você pode configurar o questionário de feedback N1 e N3 e também definir lembretes no nível da conta.

1. Clique em **[!UICONTROL Configurações]** e depois **[!UICONTROL Feedback]** no painel esquerdo depois de fazer logon como administrador.\
   A página de configurações do feedback é exibida com duas guias: **[!UICONTROL Feedback N1]** e **[!UICONTROL Feedback N3]**.\
   **[!UICONTROL Feedback N1]** consiste em uma lista de padrões **[!UICONTROL Feedback L1]** questionário para cursos em sala de aula e em ritmo individualizado junto com configurações de lembrete. Entrada **[!UICONTROL Feedback N3]** você pode ver a instrução padrão do feedback N3 e as configurações padrão.

1. Clique em Editar no canto superior direito da página para modificar o questionário existente.\
   Entrada **[!UICONTROL Feedback N1]** , você pode ativar/desativar cada pergunta clicando no botão de alternância Sim/Não.\
   Entrada **[!UICONTROL Feedback N3]** você pode modificar a instrução padrão do feedback.\
   Clique em **[!UICONTROL Adicionar novo lembrete]** na parte inferior da página e escolha quando enviar os lembretes.

1. Clique em **[!UICONTROL Salvar]** no canto superior direito da página.

No feedback N1, você pode ver dois conjuntos de questionários junto com uma pergunta padrão. O primeiro conjunto de questionários refere-se a cursos em ritmo individualizado que também podem ser usados para cursos baseados em atividade. O segundo conjunto de questionários pode ser usado para os tipos de cursos de sala de aula e sala de aula virtual.

## Exportar dados da lista de verificação {#export-checklist-data}

Na lista de cursos, abra um curso que contenha uma lista de verificação. No painel esquerdo, você verá uma opção **[!UICONTROL Lista de verificação]**.

![](assets/export-checklist.png)

*Exportar dados da lista de verificação*

Clique na opção e, na página do curso, execute o seguinte:

1. Selecione a instância e o módulo.
1. Clique em **[!UICONTROL Ações]** > **[!UICONTROL Exportar]** e exporte o relatório da lista de verificação do aluno.

Na guia **[!UICONTROL Lista de verificação]** um professor pode exportar o relatório da lista de verificação do **[!UICONTROL Ações]** lista suspensa.

O relatório CSV contém os seguintes campos:

* Nome de usuário
* Email do usuário
* Nome e email do gerente
* Nome do treinamento
* Instância de treinamento
* Nome e email do professor
* Enviado em
* Status da Avaliação
* Perguntas - com texto real
* Estado do usuário
* Perfil
* Campo(s) ativo(s)

Ao baixar um relatório após selecionar um filtro de status, o relatório de transcrição do aluno baixado conterá os dados do aluno com base no filtro de status aplicado. Esse filtro adicionado também será exibido para o administrador e gerente personalizado quando estiverem prestes a gerar uma transcrição do aluno.

## Visualizar cursos {#viewingcourses}

Como administrador, você pode exibir uma lista de todos os cursos disponíveis.   Clique em **[!UICONTROL Cursos]** no painel esquerdo para exibir a lista de cursos com opções de pesquisa e filtro. Você também pode ver a porcentagem de eficácia de cada curso nas miniaturas do curso.

>[!NOTE]
>
>Você pode retirar um curso depois que os alunos fizerem o curso ou quando quiser reservar um curso em particular depois de publicado. Você pode desativar um curso somente quando ele estiver em um estado publicado. A lista de todos os cursos retirados pode ser visualizada clicando no **[!UICONTROL Retirado]** guia.

## Exibir pontuações do quiz {#viewquizscores}

1. Clique no nome do curso na miniatura do curso.
1. Clique em Pontuação do quiz no painel esquerdo.

Você pode visualizar as pontuações do quiz de qualquer curso específico com base no nome do usuário ou em cada pergunta. Escolha as guias Por usuário ou Por pergunta adequadamente.

Escolha o tipo de instância na lista suspensa para exibir as pontuações com base em cada instância do curso.

## Gerenciar lista de alunos de um curso {#managelearnerslistforacourse}

1. Clique no nome do curso na miniatura do curso.
1. No painel esquerdo, clique em **[!UICONTROL Alunos]**.

![](assets/courses-learners.png)

*Selecionar alunos em um curso*

Você pode executar as seguintes ações na página Alunos:

* Selecione o aluno que deseja remover e clique em [!UICONTROL **Ações**] > [!UICONTROL **Remover**].
* Selecione o aluno cuja participação você deseja marcar e clique em [!UICONTROL **Ações**] > [!UICONTROL **Marcar como concluído**].

Para permitir que os alunos redefinam um módulo e o consumam novamente, clique em [!UICONTROL **Redefinir**]. Na caixa de diálogo pop-up, clique em Sim para confirmar a Redefinição. Os módulos que foram concluídos não podem ser redefinidos. Somente módulos com falha ou incompletos podem ser redefinidos.

Você também pode exportar a lista de alunos em uma planilha do Excel. Para exportar a lista de alunos, clique em [!UICONTROL **Ações**] > [!UICONTROL **Exportar**].

>[!NOTE]
>
>Se houver várias instâncias em um curso, a lista de alunos é fornecida em guias separadas no Excel. A lista de alunos consiste no nome, no status e nos critérios de seleção do aluno. O status dos alunos pode ser **Não iniciado**, ou **Em andamento**, ou **Concluído**.

## Exportar participação dos alunos {#attendance}

Para qualquer sala de aula e curso de sala de aula virtual, você pode baixar a lista de alunos que participaram deste curso, para qualquer instância.

Na página de detalhes do curso, clique em **[!UICONTROL Participação e Pontuação]** no painel direito.

No canto superior direito da página, clique no botão **[!UICONTROL Ações]** lista suspensa. Em seguida, clique na opção **[!UICONTROL Exportar lista de alunos (PDF)]**.

![](assets/export-list-of-learners.png)

*Exportar lista de alunos como PDF*

No PDF, você pode exibir o mesmo conjunto de alunos que um professor.

Ao baixar o PDF, você pode ver o fuso horário (em UTC) usado ao criar o curso.

## Exportar alunos no estado de aprovação pendente

Um administrador, gerente ou administrador personalizado pode exportar dados de alunos que estão no estado de inscrição de aprovação pendente. É possível exportar os dados por meio de **Curso > Aluno** e clique na lista suspensa Ação.

A opção estará presente quando nenhum aluno estiver inscrito/com aprovação pendente no curso aprovado pelo gerente e um relatório vazio será gerado. Você também pode exportar quando os alunos estiverem no estado de aprovação pendente, no estado inscrito, no estado pendente e no estado não inscrito.

O relatório contém dados de usuários ativos, excluídos e suspensos se estiverem pendentes de aprovação. Além disso, o relatório contém dados de usuários internos e externos que estão no estado de aprovação pendente.

Se um aluno que estava antes no estado de aprovação pendente cancelar a inscrição, o seu registro não estará presente no relatório. Além disso, se um aluno que estava antes no estado de aprovação pendente estiver inscrito no curso pela inscrição de administrador/gerente/administrador personalizado, o seu registro estará presente no relatório.

## Exibir feedback N1 e N3 {#viewl1andl3feedback}

Você pode ver o feedback N1 fornecido pelos alunos para um curso e o feedback N3 fornecido pelos gerentes para os alunos.

1. Clique em qualquer quadro do curso na lista Cursos.
1. Clique em Feedback N1 ou Feedback N3 no painel esquerdo para exibir o feedback recebido.
1. Selecione a instância na lista suspensa para exibir o feedback dessa instância específica.

## Visualizar cursos {#previewcourses}

O administrador pode visualizar cursos clicando no botão **[!UICONTROL Visualizar como aluno]** opção ao visualizar os módulos do curso.

1. Clique em **[!UICONTROL Cursos]** no painel esquerdo depois de fazer logon como administrador.
1. Clique em qualquer quadro do curso na lista de cursos da página.
1. Clique em Visualizar como aluno no painel esquerdo e clique no nome do módulo na página para visualizar o módulo do curso no reprodutor.

## Eficácia do curso {#courseeffectiveness}

A eficácia do curso é avaliada para entender a utilidade de um curso para o aluno. É uma combinação dos resultados do feedback do aluno sobre o conteúdo do curso, dos resultados dos testes de um aluno no curso e do feedback do gerente que avalia um aluno com base nos aprendizados do curso.

O administrador pode visualizar a classificação da eficácia do curso nas miniaturas do curso, conforme mostrado na captura de tela abaixo. Você pode ver a classificação deste curso como 100.

<!--![](assets/course-effectiveness-tag1.png)-->

O valor da classificação de eficácia do curso é obtido considerando os valores de feedback N1, N2 e N3. Para exibir a divisão de cada feedback, clique no valor da eficácia do curso. Uma janela pop-up é exibida conforme mostrado abaixo.

![](assets/course-effectiveness.png)

*Ver a eficácia do curso para feedback N1, N2 e N3*

Nesta captura de tela de amostra, todos os usuários receberam todos os três feedbacks, portanto, a pontuação é de 100/100. Nesta tabela, você pode entender que, se qualquer um dos três feedbacks (L1, L2 e L3 ) não for fornecido para um curso, haverá um impacto negativo na eficácia geral. Clique na seta para baixo no canto inferior direito da janela pop-up para ver como são feitos os cálculos da eficácia do curso.

![](assets/course-effectiveness-calculations.png)

*Cálculo da eficácia do curso*

Conforme o gráfico circular mostrado acima, o gerente atribui mais peso ao feedback N3.

## Pesquisar cursos e programas de aprendizado {#searchingcoursesandlearningprograms}

O Adobe Learning Manager permite encontrar mais facilmente os cursos/programas de aprendizado da sua escolha. Você pode pesquisar seus cursos de duas maneiras:

1. Usando o campo Pesquisar. Clique no ícone de pesquisa exibido no canto superior direito. Um campo de pesquisa é exibido. Digite o nome do curso ou quaisquer palavras-chave associadas aos seus cursos para localizar os cursos/programas de aprendizado. Você também pode pesquisar usando tags predefinidas como Captivate, C, Java e HTML. As tags são pesquisáveis no campo de pesquisa, o que significa que elas são exibidas no campo de pesquisa conforme você digita.
1. Filtrando a lista de cursos/programas de aprendizado usando os filtros. Você pode filtrar os cursos por estado, como Todos, Publicado, Rascunho e Retirado. No modo de administrador, o filtro de rascunho não é exibido.

Você pode pesquisar com base em competências clicando em Competências e escolhendo-as. Como administrador, você pode classificar os cursos de quatro maneiras para localizar melhor o curso necessário. Clique em Classificar por e escolha ordem alfabética crescente, ordem alfabética decrescente, data de atualização do curso ou eficácia dos cursos.

<!--![](assets/admin-sortby.png)-->

Você pode classificar os programas de aprendizado de três maneiras: ordem alfabética crescente, ordem alfabética decrescente e data de atualização.

## Inscrição de alunos {#enrollinglearners}

Você pode seguir as mesmas etapas para inscrever alunos no curso, no programa de aprendizado e nas certificações. Os gerentes também podem inscrever os alunos sob ele usando as seguintes etapas.

O administrador inscreve alguns alunos em cursos obrigatórios de acordo com os requisitos da organização:

1. Passe o mouse sobre os quadros dos cursos publicados e clique em Inscrever alunos.\
   Como alternativa, clique no quadro de qualquer curso publicado e clique em Alunos no painel esquerdo. Uma página é exibida com uma lista de alunos. Clique em Inscrever.\
   A caixa de diálogo Inscrever alunos é exibida.

1. Selecione a instância no menu suspenso Selecionar instância. A lista suspensa lista todas as instâncias, incluindo as instâncias ativas, desativadas e expiradas.

>[!NOTE]
>
>O administrador pode remover quaisquer alunos registrados de um curso clicando na seta suspensa na página dos alunos e clicando em **[!UICONTROL Ações]** > **[!UICONTROL Remover]**.

![](assets/enroll-learners.png)

*Adicionar comentários ao inscrever alunos*

*Inscrever alunos*

## Usuários

+++Incluir alunos

Selecione os grupos de usuários e os alunos individuais (usando a ID ou o nome do e-mail) que deseja incluir. Adicione todos os grupos de usuários em uma interseção no mesmo conjunto. Para adicionar outro grupo de usuários na união, use um novo conjunto de inclusão.

+++

+++Excluir alunos

Selecione os grupos de usuários e os alunos individuais (usando a ID ou o nome do e-mail) que deseja excluir. Adicione todos os grupos de usuários em uma interseção no mesmo conjunto. Para adicionar outro grupo de usuários em uma união, use um novo conjunto de inclusão.

+++

## ID de e-mail do usuário

+++ID de e-mail

Copie e cole as IDs de e-mail dos alunos que deseja inscrever, separadas por ponto-e-vírgula, vírgula ou espaçamento entre linhas. Use o **[!UICONTROL Validar Ids De Email]** opção para validar as entradas. Todas as entradas inválidas apareceriam marcadas em vermelho. Remova ou corrija essas entradas e continue clicando em **[!UICONTROL Continue.]**

![](assets/email-id-option.png)

*Inscrever alunos*

A caixa de diálogo de resumo aparece com o número de usuários do conjunto de inclusão, do conjunto de exclusão e dos usuários já inscritos na instância do curso.

+++

### Adicionar comentários ao inscrever alunos {#enroll-comments}

<!---![](assets/enroll-learners-dialog.png)-->

Como administrador ou gerente, você pode adicionar comentários ao inscrever alunos em um curso. Você pode mencionar informações adicionais sobre a coorte de usuários que está sendo inscrita. Esses dados são exportados nos relatórios do curso.

O comentário é **não** exibido ao aluno.

Quando um administrador gera o relatório do curso do aluno, qualquer comentário, se adicionado, aparece no relatório. A caixa de diálogo de resumo aparece com o número de usuários do conjunto de inclusão, do conjunto de exclusão e dos usuários já inscritos na instância do curso.

Na guia **[!UICONTROL Inscrever alunos]** , expanda a opção **[!UICONTROL Opções avançadas]**. No menu **[!UICONTROL Comentário adicional]** , insira o comentário necessário.

![](assets/comment-for-learner.png)

*Adicionar comentários para alunos*

## Pesquisar usuários inscritos {#searchforusers}

Pesquise usuários inscritos na seção Aluno do Objeto de aprendizado usando a pesquisa com preenchimento automático. Usando a pesquisa com preenchimento automático, é possível pesquisar progressivamente usuários inscritos usando nome, id de email e uuid.

![](assets/typeahead.gif)

*Passo a passo de pesquisa de usuários inscritos*

Esse tipo de pesquisa também é conhecido como preenchimento automático, pesquisa incremental, pesquisa por tipo, pesquisa incorporada ou pesquisa instantânea.

À medida que você digita para um aluno ou um grupo de usuários no campo de pesquisa, uma ou mais correspondências dos termos da pesquisa são encontradas e imediatamente apresentadas a você.

O processo permite encontrar o que você está procurando de uma forma muito mais rápida e menos incômoda do que executar várias pesquisas seguidas.

Alunos ou grupos de usuários em todas as instâncias são exibidos após uma pesquisa. Para cada aluno, a instância na qual o aluno está inscrito é exibida na **[!UICONTROL Instância]** coluna.

![](assets/search-result.png)

*Exibir resultados da pesquisa*

Com a pesquisa com preenchimento automático, você pode:

* Exibir todos os usuários inscritos, independentemente das instâncias.
* Exibir todos os grupos de usuários que tenham um ou mais usuários inscritos.

Depois que uma pesquisa é executada, não é possível filtrar alunos por instâncias. A opção de selecionar uma instância no **[!UICONTROL Selecionar instância]** a lista suspensa está desativada.

Além disso, usando os resultados da pesquisa, você pode escolher um aluno ou grupo de usuários e executar as seguintes ações:

* Cancelar inscrição
* Marcar conclusão
* Redefinir módulo

Ao realizar uma pesquisa, a opção Cancelar inscrição > Em massa na lista suspensa Ações é desativada para o curso/programa de aprendizado.

## Compartilhe o código QR com os alunos para inscrição, conclusão ou ambos {#shareqrcodewithlearnerstoenrollcompleteorboth}

Os administradores do Adobe Learning Manager podem compartilhar os códigos QR com os alunos para se inscreverem rapidamente no curso. Os três códigos QR diferentes são usados para marcar a &#39;inscrição&#39;, a &#39;conclusão&#39; ou a &#39;inscrição e conclusão&#39; de um curso.

Os alunos podem simplesmente usar o aplicativo Adobe Learning Manager para dispositivos móveis para digitalizar o respectivo código QR.

**Para baixar o código QR, faça o seguinte**:

1. Clique em **[!UICONTROL Cursos]** na seção Aprendizado no painel de navegação esquerdo.
1. Selecione um curso > **[!UICONTROL Exibir curso]**.
1. Clique em **[!UICONTROL Instâncias]** > **[!UICONTROL Mais]** > **[!UICONTROL QR Code]**.

   <!--![](assets/admin-instance-edit.png)-->

1. Ative o código QR e clique nos ícones de download “Inscrever-se”, “Concluir” e “Inscrever-se e concluir” para baixar um pdf contendo o código QR de cada um. O administrador pode compartilhar o código QR com os alunos.

   ![](assets/qr-code-download-01.png)

   *Compartilhar código QR com os pesquisadores*

## Ciclo de vida do curso {#courselifecycle}

Um ciclo de vida típico do curso tem a seguinte aparência:

**Rascunho** - Quando um autor termina de criar um curso e o salva. Nesse estado, o curso ainda não está disponível para os alunos. Você pode excluir um curso nesse estado.

**Publicado** - Quando um autor termina de publicar um curso. Nesse estado, o curso está disponível para os alunos se inscreverem.

**Retirado** - Depois de publicar um curso, um autor pode movê-lo para um estado Retirado se não quiser que o curso apareça no catálogo de cursos dos alunos. Você pode republicar ou excluir um curso nesse estado.

**Excluído** - Um curso no estado Excluído é aquele que foi removido completamente do aplicativo Adobe Learning Manager. Os cursos podem ser excluídos pelos autores somente quando estiverem no estado de rascunho. Você também pode excluir cursos do estado desativado.

![](assets/lifecycle-03.png)

*Fluxo de trabalho do ciclo de vida de um curso*

## Configurações de notificação {#notificationsettings}

Como administrador, você pode ajustar as configurações de notificação. Para obter mais informações, consulte [Notificações](user-notifications.md)

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como redefinir o módulo como administrador?

Na página Alunos de um curso, escolha o aluno ou alunos ou um grupo, clique em **[!UICONTROL Ações]** > **[!UICONTROL Redefinir Módulos]**.

![](assets/reset-modules.png)

*Opção Exibir para redefinir módulos*

Depois de clicar na opção, o status dos módulos de todos os alunos selecionados será redefinido. Os módulos concluídos não serão redefinidos.

+++

+++Como adicionar o URL do curso para que os alunos sejam redirecionados diretamente para o curso?

Passe o mouse sobre um cartão do curso e clique em **[!UICONTROL Copiar URL]**. Depois de copiar o URL, os alunos podem acessar o curso diretamente com o URL.

+++

+++Como reabrir uma instância?

Para reabrir uma instância desativada, clique no menu suspenso na instância e clique em **[!UICONTROL Reabrir instância]**.

+++
