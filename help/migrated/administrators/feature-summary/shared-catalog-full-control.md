---
jcr-language: en_us
title: Ativar controle total do catálogo compartilhado
description: Ativar o controle total do catálogo compartilhado no Adobe Learning Manager
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 89%

---



# Ativar controle total do catálogo compartilhado

## Criar catálogo {#createcatalog}

Como administrador, você pode criar um catálogo de tutoriais, programas de aprendizado, ajudas de tarefa e certificações.

Para obter mais informações, consulte [Catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

## Compartilhar catálogo {#sharecatalog}

Você pode compartilhar os catálogos com os usuários internos de uma empresa ou com todos os usuários externos. No entanto, o compartilhamento é exclusivo. Em outras palavras, um catálogo compartilhado internamente não pode ser compartilhado com grupos externos e vice-versa.

Tutoriais, programas de aprendizado, ajudas de tarefa e certificações são objetos de aprendizado compatíveis para catálogos compartilhados.

Para obter mais informações, consulte [Compartilhar catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

## Ativar controle total do catálogo compartilhado {#fullcontrol}

Você pode conceder às contas externas acesso total ao seu catálogo. O administrador da conta pode então aceitar o catálogo e pode adicionar ou excluir aprendizados ou módulos.

Para conceder controle total a uma conta externa,

1. Depois que os aprendizados são adicionados a um catálogo, você deve compartilhar o catálogo com usuários externos.
1. Na caixa de diálogo Conta externa, adicione o subdomínio e a ID do e-mail do administrador da empresa externa.
1. Na opção Controle de catálogo, alterne o botão para permitir o controle total do catálogo aos usuários externos.

   ![](assets/catalog-control.png)

   *Permitir controle total do catálogo compartilhado*

   Quando você ativa o controle total do catálogo, o administrador da empresa externa aceita a solicitação para permitir modificações no catálogo. O autor da empresa externa pode então editar cursos ou adicionar módulos.

   Consulte as seções abaixo para obter mais informações.

## Administrador da empresa externa {#administratorofexternalorganization}

Depois que o administrador da empresa anterior permite controle total do catálogo, o administrador da empresa externa aceita a solicitação, aceita o catálogo e pode vê-lo.

1. Clique no ícone de notificação para ver a notificação e aceitar o catálogo.

   <!--![](assets/notification-to-acceptcatalog.png)-->

1. Para aceitar o convite para o catálogo, clique em Aceitar.
1. Na lista de catálogos, se iniciar o catálogo compartilhado com você, poderá ver uma mensagem indicando que o catálogo agora tem controle total.

   ![](assets/catalog-details.png)

   *Exibir detalhes do catálogo*

1. Você pode alterar o nome e a descrição do catálogo.

## Compartilhar catálogo de programas de aprendizado, certificações e ajudas de tarefa {#sharecatalogforlearningprogramcertificationandjobaids}

Da mesma forma que é concedido o controle completo de catálogo para cursos, o administrador também pode conceder controle completo de catálogo para:

* Programas de aprendizado
* Certificações
* Ajudas de tarefa

## Redefinir curso {#resetcourse}

1. No cartão de catálogo com um link quebrado, clique em **[!UICONTROL Redefinir curso]**.

<!-- ![](assets/reset-course.png)-->

1. Você verá uma mensagem de alerta depois de clicar no botão Redefinir. A redefinição do curso:

   * Remove todo o conteúdo recém-adicionado do catálogo.
   * Atualiza o catálogo em sincronia com o catálogo compartilhado original.
   * Restaura a relação com o objeto de aprendizado principal.

   A redefinição do catálogo é irreversível. Não é possível desfazer as alterações feitas no catálogo.

1. Para aceitar as alterações, clique em Sim.
1. No Catálogo do curso, você pode ver que o catálogo não apresenta mais a mensagem *Vínculo interrompido*.

   Ao visualizar os detalhes do catálogo, você pode ver que o catálogo foi restaurado para seu estado original.

## Adicionar novamente um objeto de aprendizado {#readdalearningobject}

Se removeu um curso, um programa de aprendizado, uma certificação ou uma ajuda de tarefa inadvertidamente, você poderá restaurá-los.

Para restaurar um objeto de aprendizado excluído, clique Adicionar novamente.

Esta ação reverte a ação e restaura o objeto de aprendizado na visualização do catálogo.

![](assets/re-add-button.png)

*Adicionar um objeto de aprendizado novamente*

Após clicar no botão Adicionar novamente, é exibida uma mensagem de confirmação de que o objeto de aprendizado foi adicionado com êxito ao catálogo.

## Empresa externa {#externalorganization}

Depois que o administrador da conta externa aceitar o catálogo, o autor poderá adicionar cursos e programas de aprendizado.

1. Como usuário, você recebe uma notificação de que o catálogo está disponível em sua conta.
1. Para exibir a lista de cursos, clique em **[!UICONTROL Cursos]** no painel de navegação esquerdo. Você pode ver todos os cursos criados por você e compartilhados com você.
1. Para ver os detalhes do curso, clique em **[!UICONTROL Exibir curso]** no cartão do curso.

   <!--![](assets/view-course.png)-->

1. Na página de detalhes do curso, você pode ver as informações sobre o curso e os módulos compartilhados. Para adicionar um módulo, clique em Adicionar módulos. Ao adicionar módulos aos módulos existentes, os novos módulos aparecem no fim dos módulos existentes. Os módulos podem ser reorganizados a qualquer momento.
1. Depois de adicionar os módulos, clique em Publicar novamente.

   Depois de publicar novamente os módulos, no cartão do catálogo, você vê a mensagem *Vínculo interrompido*.

   Visto que você atualizou o catálogo original com módulos novos, a relação existente com o curso adquirido não existe mais.

   O objeto de aprendizado ficará fora de sincronia com a conta de origem devido a que o conteúdo do objeto de aprendizado foi modificado.

   <!--![](assets/link-broken.png)-->

Depois de adicionar e publicar novamente o módulo, se você acha que adicionou ou excluiu inadvertidamente um curso no catálogo anteriormente, é possível redefinir o módulo e reverter o módulo ao seu estado original quando foi compartilhado pela primeira vez com controle total.
