---
description: Criação de planos de aprendizado para administradores no Learning Manager.
jcr-language: en_us
title: Planos de aprendizado
contentowner: manochan
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---


# Planos de aprendizado

Criação de planos de aprendizado para administradores no Learning Manager.

## Visão geral {#overview}

Um plano de aprendizado é um conjunto de regras que inscreve os alunos em treinamentos específicos com base em determinados critérios.

Um plano de aprendizado permite que um administrador atribua automaticamente cursos, programas de aprendizado ou certificações com base na ocorrência de determinados eventos, como a integração de um novo funcionário ou a alteração na designação ou no local dos funcionários.

Por exemplo, quando um funcionário entra em uma organização, o Programa de Orientação para Novos Funcionários é atribuído automaticamente ao funcionário. Da mesma forma, se um funcionário for promovido como gerente, um Novo Programa de Orientação do Gerente será atribuído automaticamente ao funcionário.

Você pode inscrever os alunos em qualquer curso e programas de aprendizado automaticamente com base em um conjunto predefinido de eventos. Você pode criar caminhos de aprendizado para os alunos atribuindo automaticamente uma atividade de aprendizado de acompanhamento depois que um aluno conclui uma habilidade, um curso ou um programa de aprendizado.

## Criar planos de aprendizado {#createlearningplans}

Para criar um plano de aprendizado, você deve fazer logon como administrador.

1. No painel esquerdo, clique em **[!UICONTROL Planos de aprendizado]**. Se houver eventos existentes, eles serão listados na página. No entanto, se estiver configurando o recurso plano de aprendizado pela primeira vez, vá para a próxima etapa.
1. No canto superior direito da página, clique em **[!UICONTROL Adicionar]**. No menu **[!UICONTROL Adicionar plano de aprendizado]** , insira o nome do Plano de Aprendizado que um funcionário deve ter.

   ![](assets/add-learning-plandialog.png)

1. No menu **[!UICONTROL Ocorre quando]** selecione o evento necessário. As opções determinam quando um aluno faz o curso. Depois de selecionar o tipo de evento, selecione o treinamento, os cursos, o programa de aprendizado ou a certificação apropriados.

   **Observação:** Administradores e autores podem criar eventos de inscrição automática.

   Os eventos são:

   **1 - Novo aluno adicionado:** Quando um novo usuário ou funcionário entra na organização.

   ![](assets/new-learner-is-added.png)

   **2 - O aluno é adicionado a um grupo:** Quando um novo usuário ou funcionário ingressa em um grupo.  Insira e selecione o grupo de usuários na lista suspensa, ao qual este evento é aplicável. É possível escolher vários grupos. Além disso, você pode atribuir esse evento a todos os membros existentes desses grupos selecionando a opção.

   ![](assets/learner-gets-addedtoagroup.png)

   Este plano de aprendizado foi projetado especificamente para ***Personalizado - Grupo*** usuários. Digite o nome do grupo no campo e, usando a pesquisa com preenchimento automático, escolha o grupo ou grupos.

   **3 - O aluno conclui um objeto de aprendizado:** O evento é acionado quando um aluno conclui qualquer objeto de aprendizado, como curso, programa de aprendizado e assim por diante. Selecione o objeto de aprendizado ao qual esse evento se aplica. Selecione o status de conclusão do evento. Opcionalmente, você também pode escolher o grupo de usuários ao qual este aluno pertence. Insira o número de dias, após a conclusão do objeto de aprendizado, em que esse evento é acionado. Selecione a opção se quiser atribuir esse evento a usuários existentes que já concluíram esse objeto de aprendizado.

   ![](assets/learner-completealearningobject.png)

   **4 - O aluno atinge um nível de habilidade:** Insira o nome da habilidade e selecione o nível de habilidade. Você também pode escolher o grupo de usuários ao qual este aluno pertence. É opcional. Insira o número de dias, após obter a habilidade, em que esse evento será acionado. Selecione a opção se quiser atribuir esse evento a alunos existentes que já obtiveram essa habilidade.

   ![](assets/learner-achievesaskilllevel.png)

   Além disso, defina o número de dias após os quais o plano de aprendizado deve ser atribuído aos alunos.

   ![](assets/assign-learning.png)

   **5 - Em uma data específica:** Quando os eventos devem ocorrer em uma data específica. Selecione a data na qual o evento deve ser atribuído. Selecione os grupos de usuários para os quais o evento precisa ser atribuído automaticamente. Selecione as instâncias que precisam ser atribuídas e, opcionalmente, insira após quantos dias o evento precisa ser acionado.

   ![](assets/on-a-specific-date.png)

1. Para todos os eventos, você pode selecionar a instância no **[!UICONTROL Instância]** lista suspensa. Você também pode selecionar instâncias do aprendizado atribuído para qualquer evento.

   ![](assets/choose-instance.png)

   No Learning Manager, um plano de aprendizado cria sua própria instância, Automático. Ao escolher um grupo, por exemplo, Todos os alunos, por padrão, todos os alunos do plano de aprendizado são inscritos na instância Automático.

   Ao salvar o plano de aprendizado, a instância Automático aparece como uma opção na **[!UICONTROL Selecionar instância]** na seção Alunos de um curso.

1. Para salvar o plano de aprendizado, clique em **[!UICONTROL Salvar]**.

## Cancelar inscrição no treinamento {#unenroll-training}

Ao adicionar um plano de aprendizado, um administrador pode cancelar a inscrição de usuários de treinamentos específicos com base em determinados acionadores.

No aplicativo de administração, clique em **[!UICONTROL Planos de aprendizado]** > **[!UICONTROL Adicionar]**.

As próximas seções representam os acionadores nos quais a opção **[!UICONTROL Cancelar inscrição no treinamento]** foi adicionado.

## O aluno é removido de um grupo {#learnergetsremovedfromagroup}

1. Adicione um ou mais grupos de usuários. No caso de vários grupos serem selecionados, o plano é acionado quando um aluno é removido de qualquer um dos grupos mencionados.
1. Escolha a ação como **[!UICONTROL Cancelar inscrição no treinamento]**.

   1. O administrador pode escolher os treinamentos dos quais o usuário será cancelado quando removido do grupo de usuários.
   1. A Instância e a Data de Conclusão não serão aplicáveis neste cenário.

![](assets/image038.png)

## O aluno conclui um treinamento {#learnercompletesatraining}

1. Adicione um ou mais grupos de usuários. Caso vários grupos sejam selecionados, o plano é acionado quando um aluno conclui o treinamento especificado.
1. Escolha a ação como **[!UICONTROL Cancelar inscrição no treinamento]**.

   1. O administrador pode escolher os treinamentos dos quais o usuário será cancelado quando adicionado ao grupo de usuários.
   1. A Instância e a Data de Conclusão não serão aplicáveis neste caso.

![](assets/image040.png)

## O aluno é adicionado a um grupo {#learnergetsaddedtoagroup}

1. Adicione um ou mais grupos de usuários. No caso de vários grupos serem selecionados, o plano é acionado quando um aluno é adicionado a qualquer um dos grupos mencionados.
1. Escolha a ação como Cancelar inscrição no treinamento.

   1. O administrador pode escolher os treinamentos dos quais o usuário será cancelado quando adicionado ao grupo de usuários.
   1. A Instância e a Data de Conclusão não serão aplicáveis neste caso.

![](assets/image043.png)

## O aluno alcançou um nível de habilidade {#learnerachievesaskilllevel}

1. Especifique a habilidade a ser obtida.
1. Adicione um ou mais grupos de usuários. Caso vários grupos sejam selecionados, o plano é acionado quando um aluno obtém a habilidade selecionada.

![](assets/image045.png)

## Em uma data específica {#onaspecificdate}

1. Escolha a data na qual os alunos devem ter suas inscrições canceladas.
1. Adicione um ou mais grupos de usuários. Caso vários grupos sejam selecionados, o plano é acionado na data e cancela a inscrição dos usuários que fazem parte dos grupos selecionados.
1. Escolha a ação como Cancelar inscrição no treinamento.

   1. O administrador pode escolher os treinamentos dos quais o usuário terá a sua inscrição cancelada quando não estiver inscrito na data especificada.
   1. A Instância e a Data de Conclusão não serão aplicáveis neste caso.

![](assets/image047.png)

## Editar um plano de aprendizado {#editalearningplan}

Depois de criar um plano de aprendizado, o administrador pode editar/atualizar o plano a qualquer momento. Para editar, clique no nome do plano de aprendizado e modifique os valores na **[!UICONTROL Editar plano de aprendizado]** caixa de diálogo pop-up que aparece. Clique em **[!UICONTROL Salvar]**.

## Ativar um plano de aprendizado {#enablealearningplan}

Por padrão, todos os novos planos de aprendizado criados estão em um estado desativado. Você deve ativar um plano ao qual um aluno será atribuído. Quando você ativa a caixa de seleção **[!UICONTROL Alunos atuais]**, o evento é ativado sozinho.

Para ativar um plano de aprendizado,

1. Na lista de Planos de aprendizado, escolha o plano que deseja ativar.

   ![](assets/list-of-learningplans.png)

1. No canto superior direito da página, clique em **[!UICONTROL Ações]** > **[!UICONTROL Habilitar]**. Isso ativa o Plano de aprendizado.

## Excluir um plano de aprendizado {#deletealearningplan}

Para excluir um plano de aprendizado,

1. Na lista de Planos de aprendizado, escolha o plano que deseja excluir.
1. No canto superior direito da página, clique em **[!UICONTROL Ações]** > **[!UICONTROL Excluir]**.

## Desativar um plano de aprendizado {#disablealearningplan}

Para desativar um plano de aprendizado,

1. Clique na guia **[!UICONTROL Habilitado]**.
1. Na lista de Planos de aprendizado, escolha o plano que deseja desativar.
1. No canto superior direito da página, clique em **[!UICONTROL Ações]** > **[!UICONTROL Desativar]**. Isso move o plano para a **[!UICONTROL Desativado]** guia.

## Filtrar um plano de aprendizado {#filteralearningplan}

Você pode filtrar Planos de aprendizado de acordo com o tipo de evento usado ao criar um Plano de aprendizado. Clique em **[!UICONTROL Tipo]** e escolha qualquer opção para exibir os Planos de aprendizado que correspondem à seleção.

![](assets/filter-a-learningplan.png)

## Perguntas frequentes {#frequentlyaskedquestions}

1. Como configuro o Learning Manager para configurar inscrições automáticas para os novos funcionários contratados?

   No menu **[!UICONTROL Ocorre quando]** , escolha a opção **[!UICONTROL Novo aluno adicionado]**. Em seguida, atribua os Objetos de aprendizado, a instância e a data de conclusão do aluno. Administradores e autores podem criar eventos de inscrição automática. Ative o evento depois de criá-lo.

1. Como configurar um plano de aprendizado/inscrição automática para o curso em sala de aula e sala de aula virtual?

   É recomendável configurar a instância do curso com os detalhes da sessão necessários. Em seguida, configure um plano de aprendizado e mapeie-o para a instância do curso, que já foi criada.

1. Como visualizar a lista de alunos inscritos em um plano de aprendizado específico?

   Quando a instância, Automático, for criada, clique em **[!UICONTROL Curso]** > **[!UICONTROL Alunos]** e escolha a instância necessária no menu **[!UICONTROL Instância]** lista suspensa.
