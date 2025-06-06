---
description: Saiba mais sobre como remover dados do usuário no Learning Manager.
jcr-language: en_us
title: Remover usuários
contentowner: dvenkate
exl-id: 4449146c-6247-44fb-b695-a12023c31dc6
source-git-commit: 7c21986eff480f15cb788cf9a1cb51644bc083c8
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 52%

---

# Remover usuários

Saiba mais sobre como remover dados do usuário no Learning Manager.

## Visão geral {#overview}

Use o recurso de remoção do usuário para remover informações pessoais identificáveis e registros de aprendizado do usuário do Learning Manager. Observe que Excluir e Remover usuário são dois recursos diferentes. Embora um usuário excluído possa ser restaurado, todos os dados do usuário e registros de aprendizado associados a um usuário removido não podem ser restaurados.

A ação de remover um usuário pode ter os seguintes resultados:

* Se um usuário for removido, os links nos registros de importação não funcionarão para evitar o download de CSVs antigos e trazer os dados do usuário novamente para o sistema.
* Se um autor for removido, o seu nome será substituído pelo nome do administrador que removeu o usuário.
* Se os professores forem removidos, eles serão removidos das sessões. O administrador precisa substituir/adicionar professores para essas sessões.
* Remover um usuário no Learning Manager não remove o usuário em nenhum aplicativo externo (sistemas de terceiros ou outros aplicativos criados por você). Entre em contato com proprietários de aplicativos externos para remover os usuários desses aplicativos.
* Se um usuário removido for referido nas configurações de um conector, o conector será desativado. O conector precisa ser reconfigurado pelo administrador para continuar.

<!---### Manage users

In this training, you will learn how to assign and remove roles, send a welcome email, and delete and purge users. 

[![button](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&sdid=4X3B8VJ2&mv=display&mv2=display#/course/7555586)

If you're unable to launch the training, write to <almacademy@adobe.com>.-->

## Como remover usuários

Para remover usuários, siga estas etapas:

1. Como administrador, selecione **[!UICONTROL Usuários]** no painel esquerdo. A página **[!UICONTROL Usuários internos]** é aberta.
1. Exclua os usuários que deseja remover. Para excluir, selecione um ou mais usuários usando a caixa de seleção. Abra o menu suspenso **[!UICONTROL Ação]** e selecione **[!UICONTROL Excluir Usuário.]**
1. No painel esquerdo, selecione **[!UICONTROL Limpeza do usuário]**. A página **[!UICONTROL Limpeza do Usuário]** é exibida com a lista de usuários excluídos. Use os botões de opção para selecionar o usuário a ser removido. Você só pode remover um usuário por vez.

   ![](assets/purge-1.png)

   *Selecione um usuário a ser removido*

1. Abra o menu suspenso **[!UICONTROL Ações]** e selecione **[!UICONTROL Limpar Usuário]**.

   ![](assets/purge-2.png)

   *Selecione a opção Limpar Usuário*

1. Uma caixa de diálogo é exibida para confirmar. Após remover, todos os dados e registros de aprendizado associados ao usuário selecionado serão excluídos permanentemente. Uma vez removido, a ação não pode ser desfeita. Para confirmar, clique em **[!UICONTROL Limpar]**.

   ![](assets/purge-3.png)

   *Mensagem de confirmação após limpar um usuário*

1. Após confirmar e clicar em Remover, a solicitação de remoção será aceita. Você receberá uma notificação assim que a ação for concluída. Uma ID de solicitação de remoção também é fornecida. Você pode fornecer essa ID ao CSM para rastrear a solicitação.

>[!NOTE]
>
>Depois que o usuário excluído é adicionado de volta ao sistema, as funções anteriores (por exemplo, administrador, gerente, autor, professor etc.) não serão mantidas. Elas serão adicionadas com a função de aluno.

## Remoção em massa de usuários

Você pode selecionar os 50 primeiros usuários e removê-los de uma só vez. Isso permite que os administradores selecionem 50 usuários e os removam de uma só vez. Isso ajuda os administradores quando desejarem remover usuários em massa. É sempre uma prática recomendada verificar os usuários selecionados para exclusão. Isso é importante para garantir que apenas o conjunto correto de usuários esteja sendo removido.

![](assets/bulk-purge-users.png)

*Limpar usuários em massa*

## Filtrar usuários excluídos antes de limpar

O Adobe Learning Manager permite que os administradores removam permanentemente usuários que já foram excluídos da plataforma. Esse processo, chamado de remoção, ajuda as empresas a manter um banco de dados limpo do aluno, cumprir as políticas de retenção de dados e impedir qualquer acesso não autorizado aos dados do usuário.
Isso é particularmente útil para manter a higiene dos dados e garantir que dados antigos e não utilizados do usuário sejam removidos do sistema.
Remover usuários é essencial para cumprir as diretrizes de privacidade de dados ou manter um armazenamento de dados limpo, removendo registros redundantes.

### Filtrar usuários excluídos por mês

Você pode filtrar usuários excluídos selecionando um mês específico e, em seguida, excluí-los permanentemente.

Para filtrar os usuários excluídos usando o mês de exclusão:

1. Selecione **[!UICONTROL Usuários]** na home page do administrador e selecione **[!UICONTROL Limpeza do Usuário]**.
2. Selecione o seletor de data **[!UICONTROL Selecionar Mês de Exclusão]** e selecione a data.

   ![](assets/deletion-date.png)
   _Selecione o mês em que os usuários foram excluídos_

   A lista de usuários excluídos no mês selecionado é exibida.

   ![](assets/list-of-user-deleted.png)
   _Lista de usuários excluídos exibidos para o mês selecionado_

### Classificar usuários excluídos por mês

Você pode classificar os usuários filtrados por **[!UICONTROL ID de Usuário Exclusiva]** e **[!UICONTROL Data de exclusão]**.

1. Na lista de usuários excluídos, classifique os usuários de acordo com suas IDs de usuário ou data de exclusão.

   ![](assets/sort-by-date.png)
   _Lista de usuários filtrada por ID de Usuário Exclusivo_

2. Selecione um ou vários usuários.
3. Selecione **[!UICONTROL Ações]** e selecione **[!UICONTROL Limpar Usuário]**.
4. Selecione Limpar na mensagem de confirmação para excluir permanentemente os registros de usuário do Adobe Learning Manager.

   ![](assets/select-purge.png)
   _Confirmação final antes de remover permanentemente os usuários_

>[!NOTE]
>
>Remover usuários remove permanentemente seus dados. Verifique a seleção antes de continuar.

+++Leia sobre os resultados da ação Remover usuário

<table>
 <tbody>
  <tr>
   <th><strong>Remover usando a interface do usuário do Learning Manager - Corporativo</strong></th>
   <th> </th>
  </tr>
  <tr>
   <td>Exclua o usuário selecionado da conta corporativa solicitante.<br></td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclua todos os usuários de todas as contas de avaliação cujos e-mails, adobe_id, correspondem aos e-mails dos usuários selecionados.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclua todos os usuários de todas as contas de avaliação cujos e-mails, adobe_id, correspondem aos e-mails dos usuários selecionados e são os criadores das contas de avaliação.</td>
   <td>Não</td>
  </tr>
  <tr>
   <td>Exclua o e-mail do usuário de todos os outros campos da conta corporativa solicitante e de todas as contas de avaliação.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Notificar o iniciador da confirmação de exclusão.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td><strong>Remover usando a interface do usuário do Learning Manager - Não-corporativa</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Exclua o usuário selecionado da conta de avaliação solicitante.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclua todos os usuários de todas as contas de avaliação cujos e-mails, adobe_id, correspondem aos e-mails dos usuários selecionados.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclua todos os usuários de todas as contas de avaliação cujos e-mails, adobe_id, correspondem aos e-mails dos usuários selecionados e são os criadores das contas de avaliação.</td>
   <td>Não</td>
  </tr>
  <tr>
   <td>Exclua o e-mail do usuário de todos os outros campos de todas as contas de avaliação.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Notificar o iniciador da confirmação de exclusão.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td><strong>Remover outros usuários - Corporativos (indivíduos que não são usuários internos ou externos do Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Exclua o usuário selecionado de todos os outros campos da conta corporativa solicitante e de todas as contas de avaliação.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclusão do usuário das contas.</td>
   <td>Não</td>
  </tr>
  <tr>
   <td>Notificar o iniciador da confirmação de exclusão. </td>
   <td>Sim</td>
  </tr>
  <tr>
   <td><strong>Limpar</strong> <strong>outros usuários - Não-corporativos (indivíduos que não são usuários internos ou externos do Learning Manager)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Exclua o usuário selecionado de todos os outros campos de todas as contas de avaliação.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclusão do usuário das contas.</td>
   <td>Não</td>
  </tr>
  <tr>
   <td>Notificar o iniciador da confirmação de exclusão.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td><strong>Remover usando Adobe IMS - Corporativo</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Notificar o administrador corporativo sobre a solicitação.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Verifique os campos do e-mail para enviar notificações.</td>
   <td>Não</td>
  </tr>
  <tr>
   <td><strong>Remover usando Adobe IMS - Não-corporativo</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Exclua todos os usuários que possuem a AdobeID/E-mail fornecida de todas as contas de avaliação.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclua todos os usuários de uma conta de avaliação se o E-mail/AdobeId fornecido for o criador da conta.</td>
   <td>Sim</td>
  </tr>
  <tr>
   <td>Exclua a ID de e-mail selecionada de todos os outros campos de todas as contas de avaliação.</td>
   <td>Sim</td>
  </tr>
 </tbody>
</table>

+++

## Perguntas frequentes {#frequentlyaskedquestions}

+++Quantos dias leva uma solicitação de remoção para ser concluída?

Uma solicitação para remover usuários leva no máximo 30 dias para ser concluída.
+++

+++É possível executar uma remoção em massa no Adobe Learning Manager?

Sim, você pode executar uma remoção em massa. No entanto, você só pode executar uma remoção em massa de 50 usuários.
+++

+++Posso restaurar um usuário removido?

Não. Após remover, todos os dados do usuário são excluídos permanentemente e não podem ser recuperados.

+++
