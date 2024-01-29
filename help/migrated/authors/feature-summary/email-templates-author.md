---
description: Leia este artigo para saber como configurar modelos de e-mail para eventos relacionados a todos os objetos de aprendizado.
jcr-language: en_us
title: Modelos de e-mail
source-git-commit: fda58bc18bee6d21ee904a442884e4759587d053
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---



# Modelos de e-mail

Leia este artigo para saber como configurar modelos de e-mail para eventos relacionados a todos os objetos de aprendizado.

O aplicativo Learning Manager envia notificações por e-mail a várias funções de usuários com base em eventos.

Como autor, você pode personalizar modelos de e-mail adicionando ou modificando conteúdo e enviando notificações aos usuários para vários eventos acionados por alunos, gerentes e atividades de autor. Por exemplo, você pode enviar um e-mail personalizado sempre que um aluno se inscrever no seu curso. Ao se inscrever, o aluno receberá o e-mail específico do curso automaticamente.

Você também pode optar por não enviar notificações por e-mail para determinados eventos desativando a opção de modelo de e-mail.

## Definir notificações por email {#settingemailnotifications}

1. No aplicativo Autor, clique no objeto de aprendizado para o qual deseja configurar o modelo de e-mail. Por exemplo, Cursos.
1. Na página Objeto de aprendizado, clique no curso, certificação ou programa de aprendizado que deseja definir as configurações de e-mail.
1. Na página de detalhes do objeto de aprendizado, clique em Modelos de e-mail.

   Você pode ver a lista de modelos disponíveis para o objeto de aprendizado escolhido.

   ![](assets/email-templates-forlearningprograms.png)
   *Lista de modelos*

1. Clique no nome do evento para exibir o modelo no modo de visualização.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Ver visualização do modelo*

   Você pode personalizar cada modelo clicando no texto no corpo do modelo. Você pode inserir variáveis no texto clicando nos ícones apropriados conforme mostrado no instantâneo. Passe o mouse sobre cada ícone para exibir os nomes.

   ![](assets/insert-variable.png)
   *Inserir uma variável*

   As seguintes variáveis estão disponíveis:

   * LPName
   * LPCompletionDeadline
   * LearnerName
   * LearnerEmail
   * CourseName
   * CourseDescription
   * PrazoDeConclusãoDoCurso
   * DetalhesDaHabilidadeDoCurso
   * CourseBadge

   Você pode redefinir a mensagem para o conteúdo padrão clicando no link Reverter para original acima do modelo.

   Como você vê na parte superior do modelo, é possível personalizar o modelo em várias funções (gerente, aluno e assim por diante) dependendo do tipo de notificação por e-mail.

1. Clique em Salvar na parte inferior da página de modelos.
1. Na página Modelos de email, clique no botão de alternância Sim/Não circular para enviar ou desativar a notificação.

![](assets/email-notification-e1437624109719.png)
*Ativar ou desativar a notificação por email*

Se o círculo no botão de notificação em relação a cada nome de evento for adjacente a Sim (com sombreamento azul como plano de fundo), a notificação será ativada. Se estiver na sombra cinza e o círculo for adjacente a Não, a notificação será desativada.

Sempre que você configura um modelo de e-mail no nível do curso, ele tem precedência sobre as configurações no nível do administrador para esse curso específico.
