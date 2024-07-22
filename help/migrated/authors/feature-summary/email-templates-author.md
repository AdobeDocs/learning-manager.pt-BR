---
description: Leia este artigo para saber como configurar modelos de e-mail para eventos relacionados a todos os objetos de aprendizado.
jcr-language: en_us
title: Modelos de e-mail
exl-id: 3b17f889-52be-4073-ab91-7c76dd79f1d2
source-git-commit: 6862dc1958a34a369f0e0e7218f28151a47beb3b
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 72%

---

# Modelos de e-mail

Leia este artigo para saber como configurar modelos de e-mail para eventos relacionados a todos os objetos de aprendizado.

O aplicativo Learning Manager envia notificações por e-mail a várias funções de usuários com base em eventos.

Como autor, você pode personalizar os modelos de e-mail adicionando ou alterando o conteúdo e enviando notificações aos usuários dos diversos eventos acionados pelas atividades dos alunos, gerentes e autores. Por exemplo, você pode enviar um e-mail personalizado sempre que um aluno se inscrever no seu curso. Ao se inscrever, o aluno receberá automaticamente o e-mail específico do curso.

Você também pode optar por não enviar notificações por e-mail para determinados eventos, desativando a opção de modelo de e-mail.

## Configurar notificações por email {#settingemailnotifications}

1. No aplicativo Autor, selecione o objeto de aprendizado para o qual deseja configurar o modelo de e-mail. Por exemplo, Cursos.

1. Na página Objeto de aprendizado, clique no curso, certificação ou programa de aprendizado para o qual deseja definir as configurações de e-mail.

1. Na página de detalhes do objeto de aprendizado, selecione **Modelos de email** > **Todos os modelos**. Modelos de email estão disponíveis para a **Instância padrão** e o **Curso atual**. Você pode alternar entre elas usando a lista suspensa no canto superior direito.

   Você pode ver a lista de modelos disponíveis para o objeto de aprendizado escolhido.

   ![](assets/email-templates-forlearningprograms.png)
   *Lista de modelos*

1. Clique no nome do evento para visualizar o modelo no modo de visualização.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Ver visualização do modelo*

   Você pode personalizar cada modelo clicando no texto do corpo do modelo. Você pode inserir variáveis no texto clicando nos ícones apropriados, conforme mostrado na imagem. Passe o mouse sobre cada ícone para ver os nomes.

   ![](assets/insert-variable.png)
   *Inserir uma variável*

   Estão disponíveis as seguintes variáveis:

   * LPName
   * LPCompletionDeadline
   * LearnerName
   * LearnerEmail
   * CourseName
   * CourseDescription
   * CourseCompletionDeadline
   * CourseSkillDetails
   * CourseBadge

   Você pode redefinir a mensagem com o conteúdo padrão clicando no link Reverter para o original acima do modelo.

   Como você vê na parte superior do modelo, é possível personalizar o modelo em várias funções (gerente, aluno e assim por diante) dependendo do tipo de notificação por e-mail.

1. Clique em Salvar na parte inferior da página dos modelos.
1. Na página Modelos de e-mail, clique no botão circular de alternância Sim/Não para enviar ou desativar a notificação.

![](assets/email-notification-e1437624109719.png)
*Habilitar ou desabilitar a notificação por email*

Se o círculo no botão de notificação de cada nome do evento estiver adjacente a Sim (com a cor azul como plano de fundo), a notificação está ativada. Se estiver em cinza e o círculo estiver adjacente a Não, a notificação está desativada.

Sempre que você configurar um modelo de e-mail no nível do curso, ele terá precedência sobre as configurações no nível do administrador nesse curso específico.

## Configurações do modelo de email

O autor pode configurar o seguinte nas configurações do modelo de email:

* **Banner de email**: permite modificar o banner de email.

* **Assinatura de email**: permite adicionar ou editar a assinatura de email.
