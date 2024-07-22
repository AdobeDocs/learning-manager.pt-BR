---
description: Leia este artigo para saber como gerenciar módulos como professor no Learning Manager.
jcr-language: en_us
title: Módulos
contentowner: shhivkum
exl-id: b81e7ee4-b25f-498d-a780-3ef897f38268
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '954'
ht-degree: 63%

---

# Módulos

Leia este artigo para saber como gerenciar módulos como professor no Learning Manager.

## Exibir a visão geral da sessão {#viewsessionoverview}

1. No painel esquerdo, clique em Próxima sessão.
1. Na lista das próximas sessões, selecione a sessão cujas informações você deseja visualizar.

   O aplicativo exibe a visão geral da sessão com detalhes, tais como nome da sessão, local, dias e horários, limite de inscrições, limite da lista de espera, e assim por diante.

   ![](assets/upcomingsessions.png)
   *Exibir as próximas sessões*

## Configurar detalhes da sessão {#configuresessiondetails}

1. No painel esquerdo, clique em Próxima sessão.
1. Selecione a sessão que deseja atualizar.
1. Clique em Editar no canto superior direito.

   ![](assets/sessiondetails.png)
   *Configurar detalhes da sessão*

1. Na página de visão geral da sessão, você pode editar o horário, a data, o local da sessão, etc. Você também pode editar ou adicionar os seguintes detalhes da sessão:

   * Especifique o limite de inscrições para definir o número máximo de alunos permitido na sessão.
   * Especifique o limite da lista de espera se quiser definir o número máximo de alunos permitido na lista de espera da sessão.
   * No campo Permitir envios, selecione Sim para permitir que os alunos enviem atribuições. Se você selecionar Não, os alunos não poderão carregar envios de atribuição para a sessão.

   ![](assets/editsessiondetails.png)
   *Editar os detalhes da sessão*

1. Clique em Salvar.

   Você não pode editar o campo Professor desta página.

## Carregar arquivos de recurso na sessão {#uploadresourcefilesforyoursession}

Como professor, você pode carregar arquivos de recurso, como arquivos de atribuição ou apresentações dos módulos ou arquivos de atividade do módulo. Use o menu Recursos para adicionar arquivos de recursos do módulo ou sessão.

1. No Aplicativo do professor, clique em Próximas sessões > Recursos.

   Você pode visualizar a página Recursos, que já tem um link para os recursos que os autores possam ter carregado no curso associado ao módulo. Além disso, os professores também podem carregar arquivos de recursos para os módulos.

1. Clique em Adicionar.

   ![](assets/addresource.png)
   *Adicionar um recurso para a sessão*

1. Procure o arquivo apropriado no computador. Selecione o arquivo e clique em Abrir.
1. Depois que o arquivo é carregado, você pode visualizar o arquivo junto com a data em que foi adicionado.

   Os alunos que se inscreveram neste módulo podem visualizar seus arquivos, assim que forem carregados, na seção Recursos em Cursos.

   Para excluir um arquivo de recurso, selecione o arquivo ou arquivos que deseja excluir. Clique em Ações > Excluir arquivo na página Recursos.

## Envio de arquivo nos módulos de atividade {#filesubmissionforactivitymodules}

O módulo de atividade suporta o fluxo de trabalho de envio de arquivo. Como Autor, crie um módulo de atividade e selecione a opção **[!UICONTROL Envio de arquivo]**. Isso permite que os alunos enviem arquivos.

Esses arquivos podem ser aprovados/rejeitados pelos professores do módulo. O módulo é concluído somente depois que o professor aprovar o envio.

![](assets/activity-modules.png) ![](assets/approve-reject-option.png)
*Aprovar ou rejeitar arquivos*

## Avaliar módulo de lista de verificação {#evaluate-checklist-module}

Depois que o aluno faz o curso, o professor vê o módulo da lista de verificação na página Envios/Listas de verificação na seção **Módulos**. Esta página contém todos os módulos de lista de verificação de atividades junto com os módulos de envio de atividades para os quais as revisões devem ser feitas. Para cada módulo, o número de alunos é exibido para quem a avaliação deve ser realizada.

Na página abaixo, você pode exibir módulos do tipo **Envio** e **Lista de Verificação**. Neste exemplo, usaremos o módulo Lista de verificação.

![](assets/modules-list.png)
*Exibir lista de módulos*

Clique no módulo Lista de verificação. Na página **Lista de Verificação**, você verá o seguinte:

* O nome do módulo
* O nome do curso
* Instância à qual o curso pertence
* Critérios de aprovação definidos pelo autor
* Número de perguntas da lista de verificação

![](assets/checklist-page.png)
*Exibir a página da lista de verificação*

Para avaliar um aluno, clique em **[!UICONTROL Avaliar]** na coluna **[!UICONTROL Lista de verificação]**. Você também pode ver que o status da revisão está **Pendente**.

Avalie o aluno e clique em **[!UICONTROL Enviar]**. Como professor, você deve responder a todas as questões da avaliação.

![](assets/checklist-evaluation-screen.png)
*Lista de verificação para avaliação*

Dependendo dos critérios de aprovação, o status será com Reprovado ou Aprovado.

Uma lista de verificação, uma vez avaliada, não pode ser reavaliada.

Um professor também pode ver as respostas enviadas por outros professores do módulo.

Você pode exportar os alunos como um csv com base no filtro de pesquisa aplicado.

Depois que o professor avalia o curso usando a Lista de verificação, o aluno vê o status do módulo como **Aprovado** e o status do curso como **Concluído** ou o status do módulo como **Reprovado** e o status do curso como **Concluído**.

## Comentários do professor para rejeição de uma atividade {#rejection-comments}

Um aluno pode ver o comentário de um professor na notificação enviada para rejeição. O aluno pode reenviar fornecendo mais informações na forma de comentários.

Este é o fluxo de trabalho:

1. Um autor cria um curso com um módulo de atividade, atribui um professor e, em seguida, publica o curso.

1. Um aluno consome o curso e, após concluí-lo, envia o comprovante de conclusão.

   ![](assets/proof-of-completion.png)
   *Enviar comprovante de conclusão*

1. O professor seleciona o módulo de atividade que está atribuído a ele. Na página Envios do módulo, o professor clica em **Editar**. Em seguida, ele pode inserir os comentários para rejeição e ativar a opção Mostrar comentário, para que o aluno possa visualizar o comentário na notificação.

   ![](assets/enter-comments.png)
   *Insira comentários sobre a conclusão*

1. O professor pode clicar em **Rejeitar**. O status do envio muda para **Marcado para Rejeição**.

   ![](assets/marked-for-rejection.png)
   *Rejeitar um envio*

1. Após o envio, o status muda para **Rejeitado**.

   ![](assets/rejected-status.png)
   *Exibir status de rejeição*

1. O aluno agora vê uma notificação de que o envio foi rejeitado. Os comentários do professor também aparecem na notificação.

   ![](assets/notification-of-rejection.png)
   *Receber notificação de rejeição*

Para acomodar as alterações, o Adobe atualizou o modelo de email para **Envio rejeitado**.

## Adicionar pontuações e comentários nos módulos de atividade {#addscoresandcommentsforactivitymodules}

Para adicionar pontuações e comentários nos módulos de atividade que foram encaminhados para envio, siga as etapas abaixo:

1. No painel esquerdo, clique em **[!UICONTROL Aluno]**.

   ![](assets/learners.png)
   *Selecione um aluno*

1. Na página Alunos, clique em **[!UICONTROL Ações]** > **[!UICONTROL Editar pontuações e comentários]**.

   ![](assets/edit-scores-comments.png)
   *Adicionar comentários*

   Para os alunos que não concluíram o curso, o campo de entrada da pontuação e dos comentários não será exibido.

   ![](assets/editing-scores-andcomments.png)
   *Editar pontuações e comentários*

1. Clique em **[!UICONTROL Salvar]**.
