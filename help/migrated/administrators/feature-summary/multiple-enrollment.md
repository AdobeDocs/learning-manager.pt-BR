---
title: Inscrição múltipla no Adobe Learning Manager
description: Como administrador da conta, uma das suas principais tarefas é criar instâncias diferentes de sessões VILT em fusos horários diferentes e, possivelmente, criar sessões para grupos de usuários específicos.
exl-id: c430545d-b48e-432d-a278-658c9281818f
source-git-commit: 5676ddb238309bc643394af1dde3cba7f8ac6699
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 65%

---

# Inscrição múltipla no Adobe Learning Manager

No Adobe Learning Manager, cada curso pode ter instâncias diferentes. Como administrador da conta, uma das suas principais tarefas é criar instâncias diferentes de sessões VILT em fusos horários diferentes e, possivelmente, criar sessões para grupos de usuários específicos.

Antes da versão de julho de 2023, quando um administrador inscrevia um aluno, ele podia se inscrever em apenas uma instância. Se um aluno quisesse fazer um curso em instâncias diferentes, o administrador criava muitos cursos, um para cada instância.

O recurso de inscrição múltipla do Adobe Learning Manager ajuda um administrador a evitar esses cenários.

## Gerenciar instâncias

>[!INFO]
>
>Neste treinamento, você aprenderá como editar detalhes e propriedades da instância.<br><br>[![botão](assets/launch-training-button.png)](https://content.adobelearningmanageracademy.com/app/learner?accountId=98632#/course/8318912)</br></br>

Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

## O que é inscrição múltipla

A inscrição múltipla inscreve um aluno várias vezes em um curso por meio de várias instâncias disponíveis.  Um aluno pode se inscrever em várias instâncias do curso independentemente do estado em que está inscrito, concluído ou ainda não iniciado. Quando o autor ativa a opção [!UICONTROL Inscrição múltipla], um aluno pode se inscrever em várias instâncias do curso.

![imagem de várias inscrições](assets/multi-enrollment-author.png)
*Iniciar Vários Registros a partir de Configurações*

O progresso de cada instância pode ser acompanhado individualmente, e um relatório pode ser exportado para acompanhar o progresso de cada instância.

## Pontos importantes

* A inscrição múltipla é aplicável somente quando um curso tem várias instâncias.
* Quando a opção inscrição múltipla estiver ativada e os usuários estiverem inscritos em várias instâncias, novas linhas são criadas para cada curso no relatório de transcrição do aluno (uma linha para cada instância e cada aluno)
* Caso a automação de relatórios estiver configurada para antecipar apenas uma linha por curso, você deve fazer os ajustes necessários na automação de relatórios antes de habilitar o recurso Inscrição Múltipla.

## Como ativar a Inscrição Múltipla

1. Faça logon na sua conta da Adobe Learning Manager como autor.
1. Selecione o curso no qual deseja que os alunos se inscrevam várias vezes.
1. No painel esquerdo, selecione **[!UICONTROL Configurações]** > **[!UICONTROL Editar]** > **[!UICONTROL Configuração de instância]** > **[!UICONTROL Habilitar várias inscrições]**.

![imagem de várias inscrições](assets/multi-enrollment-author.png)
*Habilitar Vários Registros*

>[!NOTE]
>
>Como autor, você não pode ter a Opção de Instância e Inscrição Múltipla habilitadas simultaneamente.

## Exibição do aluno

Várias inscrições são úteis quando um aluno deseja se inscrever em um curso de sala de aula ou sala de aula virtual ou deseja concluir um curso novamente antes de passar para outro curso.

Para os alunos que não se inscreveram, ao selecionar um curso, eles visualizarão a tela do curso com várias instâncias. Depois, podem selecionar cada instância e se inscrever.

![imagem de exibição do aluno](assets/learner-view.png)
*Exibir as instâncias*

Depois de se inscreverem em uma instância, eles podem se inscrever em outras instâncias selecionando a opção Exibir Todas as Instâncias no painel direito.

![imagem do curso de várias inscrições](assets/enroll-instance.png)
*Inscrever-se em uma instância*

O progresso em cada instância pode ser acompanhado da seguinte maneira:

![acompanhar progresso](assets/check-progress.png)
*Acompanhar o progresso de cada instância*

## Alterações de Inscrição Múltipla no administrador

**Registro:**

Ao inscrever os alunos, você pode ativar as seguintes caixas de seleção:

*”Os alunos selecionados podem já estar inscritos em outras instâncias deste curso. Permita que esses alunos também sejam inscritos na instância ...”*

![alterações de administrador](assets/admin-changes.png)
*Opção de registro para administradores*

Se o aluno já estiver inscrito em uma instância e você, como administrador, estiver tentando inscrevê-lo em uma instância diferente do curso, selecione Sim.

## Relatórios

Para um aluno inscrito em duas instâncias do mesmo curso, duas linhas são criadas para cada instância do curso. O relatório também exibe o progresso das instâncias.
