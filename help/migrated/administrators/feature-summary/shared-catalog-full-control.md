---
jcr-language: en_us
title: Ativar controle total do catálogo compartilhado
description: Ativar o controle total do catálogo compartilhado no Adobe Learning Manager
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---



# Ativar controle total do catálogo compartilhado

## Criar catálogo {#createcatalog}

Como administrador, você pode criar um catálogo de cursos, programas de aprendizado, ajudas de tarefa e certificações.

Para obter mais informações, consulte [Catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

## Compartilhar catálogo {#sharecatalog}

Você pode compartilhar os catálogos com usuários internos de uma organização ou com qualquer usuário externo. No entanto, o compartilhamento é exclusivo. Em outras palavras, um catálogo compartilhado internamente não pode ser compartilhado com grupos externos e vice-versa.

Cursos, programas de aprendizado, ajudas de tarefa e certificações são os objetos de aprendizado compatíveis com o catálogo compartilhado.

Para obter mais informações, consulte [Compartilhar catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

## Ativar controle total do catálogo compartilhado {#fullcontrol}

Você pode conceder acesso total ao seu catálogo para contas externas. O administrador da conta pode aceitar o catálogo e, portanto, adicionar ou excluir aprendizados ou módulos.

Para conceder controle total a uma conta externa,

1. Depois de adicionar aprendizado(s) a um catálogo, você deve compartilhar o catálogo com usuários externos.
1. Na caixa de diálogo Conta externa, adicione o subdomínio e a ID de e-mail do administrador da organização externa.
1. Na opção Controle do catálogo, alterne o botão para permitir o controle total do catálogo para usuários externos.

   ![](assets/catalog-control.png)

   *Permitir controle total do catálogo compartilhado*

   Quando você permite o controle total do catálogo, o administrador da organização externa aceita a solicitação para permitir modificações no catálogo. O autor da organização externa pode editar os cursos ou adicionar módulos.

   Consulte as seções abaixo para obter mais informações.

## Administrador da organização externa {#administratorofexternalorganization}

Depois que o administrador da organização anterior permite o controle total do catálogo, o administrador da organização externa aceita a solicitação e o visualiza.

1. Clique no ícone de notificação para exibir a notificação de aceitação do catálogo.

   <!--![](assets/notification-to-acceptcatalog.png)-->

1. Para aceitar o convite para o catálogo, clique em Aceitar.
1. Na lista de catálogos, se você iniciar o catálogo que foi compartilhado com você, verá uma mensagem informando que o catálogo agora tem controle total.

   ![](assets/catalog-details.png)

   *Exibir detalhes do catálogo*

1. Você pode modificar o nome do catálogo e a descrição.

## Compartilhar catálogo de Programa de aprendizado, Certificação e ajudas de tarefa {#sharecatalogforlearningprogramcertificationandjobaids}

Assim como concede controle completo do catálogo dos cursos, o administrador também pode conceder controle completo do catálogo para o seguinte:

* Programas de aprendizado
* Certificações
* Ajudas de tarefa

## Redefinir curso {#resetcourse}

1. No cartão de catálogo com um link quebrado, clique em **[!UICONTROL Redefinir curso]**.

<!-- ![](assets/reset-course.png)-->

1. Você verá uma mensagem de alerta após clicar no botão Redefinir. Redefinindo o curso:

   * Remove todo o conteúdo recém-adicionado do catálogo.
   * Atualiza o catálogo em sincronia com o catálogo compartilhado original.
   * Restaura o relacionamento com o Objeto de aprendizado pai.

   A redefinição do catálogo é irreversível. Não é possível desfazer as alterações feitas no catálogo.

1. Para aceitar as alterações, clique em Sim.
1. No catálogo do curso, você pode ver que o catálogo não tem a mensagem *Link quebrado* mais.

   Ao exibir os detalhes do catálogo, você pode ver que o catálogo agora está restaurado ao seu estado original.

## Adicionar novamente um objeto de aprendizado {#readdalearningobject}

Se você removeu um curso, programa de aprendizado, certificação ou ajuda de tarefa inadvertidamente, pode restaurá-lo.

Para restaurar um objeto de aprendizado excluído, clique em Adicionar novamente.

Esta ação reverte a ação e restaura o Objeto de aprendizado na exibição do catálogo.

![](assets/re-add-button.png)

*Adicionar um objeto de aprendizado novamente*

Depois de clicar no botão Adicionar novamente, há uma mensagem de confirmação de que o objeto de aprendizado foi adicionado com êxito ao catálogo.

## Organização externa {#externalorganization}

Depois que o administrador da conta externa aceita o catálogo, o autor agora pode adicionar cursos e programas de aprendizado.

1. Como usuário, você recebe uma notificação de que o catálogo agora está disponível em sua conta.
1. Para ver a lista de cursos, clique em **[!UICONTROL Cursos]** no painel de navegação esquerdo. Você pode ver todos os cursos criados e compartilhados com você.
1. Para exibir os detalhes do curso, clique em **[!UICONTROL Exibir curso]** no cartão do curso.

   <!--![](assets/view-course.png)-->

1. Na página de detalhes do curso, você pode ver informações sobre o curso e os módulos compartilhados. Para adicionar um módulo, clique em Adicionar módulos. Quando você adiciona módulos aos módulos existentes, os novos módulos são exibidos no final dos módulos existentes. É possível reorganizar os módulos a qualquer momento.
1. Depois de adicionar os módulos, clique em Republicar.

   Depois de republicar os módulos, você verá uma mensagem no cartão do catálogo *Link quebrado*.

   Como você atualizou o catálogo original com novos módulos, o relacionamento existente com o curso adquirido não existe mais.

   O objeto de aprendizado estará fora de sincronia com a conta de origem, pois o conteúdo do objeto de aprendizado foi modificado.

   <!--![](assets/link-broken.png)-->

Depois de adicionar e publicar novamente o módulo, se você acha que adicionou ou excluiu inadvertidamente um curso no catálogo anteriormente, é possível redefinir o módulo e reverter o módulo ao seu estado original quando foi compartilhado pela primeira vez com controle total.
