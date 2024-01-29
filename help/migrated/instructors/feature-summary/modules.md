---
description: Leia este artigo para saber como gerenciar módulos como professor no Learning Manager.
jcr-language: en_us
title: Módulos
contentowner: shhivkum
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 0%

---



# Módulos

Leia este artigo para saber como gerenciar módulos como professor no Learning Manager.

## Exibir visão geral da sessão {#viewsessionoverview}

1. No painel esquerdo, clique em Próxima sessão.
1. Na lista de suas próximas sessões, selecione a sessão cujos detalhes você deseja exibir.

   O aplicativo exibe a visão geral da sessão com detalhes como o nome da sessão, local, horários, limite de inscrição, limite da lista de espera e assim por diante.

   ![](assets/upcomingsessions.png)
   *Exibir sessões futuras*

## Configurar detalhes da sessão {#configuresessiondetails}

1. No painel esquerdo, clique em Próxima sessão.
1. Selecione a sessão que deseja atualizar.
1. Clique em Editar no canto superior direito.

   ![](assets/sessiondetails.png)
   *Configurar detalhes da sessão*

1. Na página Visão geral da sessão, você pode editar os horários, a data, o local e assim por diante. Você também pode editar ou adicionar os seguintes detalhes da sessão:

   * Especifique o Limite de inscrição para definir o número máximo de alunos permitidos para a sessão.
   * Especifique o Limite da lista de espera se quiser definir o número máximo de alunos permitidos na lista de espera para a sessão.
   * No campo Permitir envios, selecione Sim para permitir que os alunos enviem atribuições. Se você selecionar Não, os alunos não poderão carregar envios de atribuição para a sessão.

   ![](assets/editsessiondetails.png)
   *Editar os detalhes da sessão*

1. Clique em Salvar.

   Você não pode editar o campo Professor nesta página.

## Fazer upload de arquivos de recurso para sua sessão {#uploadresourcefilesforyoursession}

Como professor, você pode fazer upload de arquivos de recurso, como arquivos de atribuição ou apresentações para os módulos ou arquivos de atividade para o módulo. Use o menu Recursos para adicionar arquivos de recursos para o módulo ou sessão.

1. No aplicativo do professor, clique em Próximas sessões > Recursos.

   Você pode ver a página Recursos, que já tem um link para os recursos que os autores podem ter carregado para o curso associado ao seu módulo. Além disso, os professores também podem fazer upload de arquivos de recursos para os módulos.

1. Clique em Adicionar.

   ![](assets/addresource.png)
   *Adicionar um recurso para a sessão*

1. Procure o arquivo apropriado em seu computador. Selecione o arquivo e clique em Abrir.
1. Após o upload do arquivo, você poderá vê-lo juntamente com a data em que foi adicionado.

   Os alunos inscritos neste módulo podem ver seus arquivos depois de carregados, na seção Recursos em Cursos.

   Para excluir um arquivo de recurso, selecione o arquivo ou arquivos que deseja excluir. Clique em Ações > Excluir arquivo na página Recursos.

## Envio de arquivos para módulos de atividade {#filesubmissionforactivitymodules}

O Módulo de atividade oferece suporte ao fluxo de trabalho de Envio de arquivos. Como autor, crie um módulo de atividade e selecione o  **[!UICONTROL Envio de arquivo]** opção. Isso permite que os alunos enviem um arquivo.

Esses arquivos podem ser aprovados/rejeitados pelos professores do módulo. O módulo é concluído somente depois que o professor aprova o envio.

![](assets/activity-modules.png) ![](assets/approve-reject-option.png)
*Aprovar ou rejeitar arquivos*

## Avaliar módulo de lista de verificação {#evaluate-checklist-module}

Depois que o aluno faz o curso, o professor vê o módulo da lista de verificação na página Envios/Listas de verificação na **Módulos** seção. Esta página contém todos os módulos de lista de verificação de atividades junto com os módulos de envio de atividades para os quais as revisões devem ser feitas. Para cada módulo, o número de alunos é exibido para quem a avaliação é devida.

Na página abaixo, você pode exibir módulos do tipo **Envio** e **Lista de verificação**. Para este exemplo, usaremos o módulo Lista de verificação.

![](assets/modules-list.png)
*Exibir lista de módulos*

Clique no módulo Lista de verificação. Na guia **Lista de verificação** , você verá o seguinte:

* O nome do módulo
* O nome do curso
* Instância à qual o curso pertence
* Critérios de aprovação definidos pelo autor
* Número de perguntas da lista de verificação

![](assets/checklist-page.png)
*Exibir a página da lista de verificação*

Para avaliar um aluno, clique em **[!UICONTROL Avaliar]** na caixa **[!UICONTROL Lista de verificação]** coluna. Você também pode ver que o status da revisão é **Pendente**.

Avalie o aluno e clique em **[!UICONTROL Enviar]**. Como professor, você deve responder a todas as perguntas de avaliação.

![](assets/checklist-evaluation-screen.png)
*Lista de verificação para avaliação*

Dependendo dos critérios de aprovação, o Status será Com Falha ou Aprovado.

Uma lista de verificação, depois de avaliada, não pode ser reavaliada.

Um professor também pode exibir as respostas enviadas por outros professores do módulo.

Você pode exportar os alunos como um csv com base no filtro de pesquisa aplicado.

Depois que o professor avalia o curso usando a Lista de verificação, o aluno vê o status do módulo como **Passagem** e o status do curso como **Concluído**, ou o status do módulo como **Falha** e o status do curso como **Concluído**.

## Comentários do professor para a rejeição de uma atividade {#rejection-comments}

Um aluno pode ver o comentário de um professor na notificação enviada para rejeição. O aluno pode reenviar fornecendo mais informações na forma de comentários.

Este é o fluxo de trabalho:

1. Um autor cria um curso com um módulo de atividade, atribui um professor e, em seguida, publica o curso.

1. Um aluno consome o curso e, após concluí-lo, envia o comprovante de conclusão.

   ![](assets/proof-of-completion.png)
   *Enviar comprovante de conclusão*

1. O professor seleciona o módulo de atividade que está atribuído a ele. Na página Envios do módulo, o professor clica em **Editar**. Em seguida, ele pode inserir os comentários para rejeição e ativar a opção Mostrar comentário, para que o aluno possa visualizar o comentário na notificação.

   ![](assets/enter-comments.png)
   *Inserir comentários de conclusão*

1. O professor pode clicar em **Rejeitar**. O status do envio muda para **Marcado para rejeição**.

   ![](assets/marked-for-rejection.png)
   *Rejeitar um envio*

1. Após o envio, o status muda para **Rejeitado**.

   ![](assets/rejected-status.png)
   *Exibir status de rejeição*

1. O aluno agora vê uma notificação de que o envio foi rejeitado. Os comentários do professor também aparecem na notificação.

   ![](assets/notification-of-rejection.png)
   *Receber notificação de rejeição*

Para acomodar as alterações, o Adobe atualizou o modelo de e-mail para **Envio rejeitado**.

## Adicionar pontuações e comentários aos módulos de atividade {#addscoresandcommentsforactivitymodules}

Para adicionar pontuações e comentários aos módulos de atividade que foram enviados para envio, siga as etapas abaixo:

1. No painel esquerdo, clique em **[!UICONTROL Aluno]**.

   ![](assets/learners.png)
   *Selecionar um aluno*

1. Na página do aluno, clique em **[!UICONTROL Ações]** > **[!UICONTROL Editar pontuações e comentários]**.

   ![](assets/edit-scores-comments.png)
   *Adicionar comentários*

   Para alunos que não concluíram o curso, o campo de entrada de pontuação e comentários não será exibido.

   ![](assets/editing-scores-andcomments.png)
   *Editar pontuações e comentários*

1. Clique em **[!UICONTROL Salvar]**.
