---
description: Saiba mais sobre como remover dados do usuário no Learning Manager.
jcr-language: en_us
title: Remover usuários
contentowner: dvenkate
source-git-commit: 0534bd52c80b77d985cfe715f74054f3aabac9a2
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 72%

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

### Gerenciar usuários

Neste treinamento, você aprenderá como atribuir e remover funções, enviar um email de boas-vindas e excluir e limpar usuários.

[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=4X3B8VJ2&amp;mv=display&amp;mv2=display#/course/7555586)

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

## Como remover usuários

Para remover usuários, siga estas etapas:

1. Como administrador, selecione **[!UICONTROL Usuários]** no painel esquerdo. A página **[!UICONTROL Usuários internos]** é aberta.
1. Exclua os usuários que deseja remover. Para excluir, selecione um ou mais usuários usando a caixa de seleção. Abra o **[!UICONTROL Ação]** e selecione **[!UICONTROL Excluir usuário.]**
1. No painel esquerdo, selecione **[!UICONTROL Limpeza do usuário]**. A página **[!UICONTROL Limpeza do Usuário]** é exibida com a lista de usuários excluídos. Use os botões de opção para selecionar o usuário a ser removido. Você só pode remover um usuário por vez.

   ![](assets/purge-1.png)

   *Selecione um usuário para remover*

1. Abra o **[!UICONTROL Ações]** menu suspenso e selecione **[!UICONTROL Remover usuário]**.

   ![](assets/purge-2.png)

   *Selecione a opção Remover usuário*

1. Uma caixa de diálogo é exibida para confirmar. Após remover, todos os dados e registros de aprendizado associados ao usuário selecionado serão excluídos permanentemente. Uma vez removido, a ação não pode ser desfeita. Para confirmar, clique em **[!UICONTROL Limpar]**.

   ![](assets/purge-3.png)

   *Mensagem de confirmação após remover um usuário*

1. Após confirmar e clicar em Remover, a solicitação de remoção será aceita. Você receberá uma notificação assim que a ação for concluída. Uma ID de solicitação de remoção também é fornecida. Você pode fornecer essa ID ao CSM para rastrear a solicitação.

## Remoção em massa de usuários

Você pode selecionar os 50 primeiros usuários e removê-los de uma só vez. Isso permite que os administradores selecionem 50 usuários e os removam de uma só vez. Isso ajuda os administradores quando desejarem remover usuários em massa. É sempre uma prática recomendada verificar os usuários selecionados para exclusão. Isso é importante para garantir que apenas o conjunto correto de usuários esteja sendo removido.

![](assets/bulk-purge-users.png)

*Remover usuários em massa*

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

O Learning Manager agora está em conformidade com o GDPR. Para obter mais informações sobre a conformidade com o GDPR, consulte  [Conformidade do Learning Manager com o GDPR](../../kb/prime-gdpr.md).

## Perguntas frequentes {#frequentlyaskedquestions}

+++Quantos dias leva uma solicitação de remoção para ser concluída?

Uma solicitação para remover usuários leva no máximo 30 dias para ser concluída.
+++

+++É possível executar uma remoção em massa no Learning Manager?

Sim, você pode executar uma remoção em massa. No entanto, você só pode executar uma remoção em massa de 50 usuários.
+++
