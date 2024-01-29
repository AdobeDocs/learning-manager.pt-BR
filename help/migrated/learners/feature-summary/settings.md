---
description: Leia este artigo para saber como definir as configurações do perfil do aluno e adicionar uma foto ao perfil. Saiba como baixar a transcrição do aluno para seu perfil.
jcr-language: en_us
title: Configurações do perfil
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 0%

---



# Configurações do perfil

Leia este artigo para saber como definir as configurações do perfil do aluno e adicionar uma foto ao perfil. Saiba como baixar a transcrição do aluno para seu perfil.

## Definindo as configurações do perfil {#configuringprofilesettings}

1. No canto superior direito da página, clique na seta suspensa ao lado de seu perfil ou foto.
1. Selecione Configurações do perfil.
1. Na caixa de diálogo pop-up exibida, você pode executar as seguintes ações:

   * Adicionar/atualizar foto de perfil: passe o mouse sobre a foto. Clique em Fazer upload e adicione uma foto. Clique em Editar para alterar a foto.
   * Excluir foto: passe o mouse sobre a foto do perfil. Clique em Excluir.
   * Adicione conteúdo Sobre mim clicando na área de texto abaixo.
   * Modifique o conteúdo de Sobre mim clicando em Editar ao lado do campo.
   * Defina a localidade do seu perfil. Na lista suspensa Local, selecione o idioma de sua escolha.
   * Defina a localidade atual do seu perfil.
   * Defina o fuso horário do seu perfil.
   * Baixe a transcrição dos alunos com seus dados.

   ![](assets/learner-preferences.png)
   *Exibir preferências do aluno*

   Ao clicar no link Baixar minha transcrição de aprendizado XLS, uma folha do Excel é baixada para o seu sistema. Essa planilha do Excel contém detalhes sobre os objetos de aprendizado consumidos por você, o status de conclusão de cada objeto de aprendizado, as datas de vencimento correspondentes, as habilidades obtidas e assim por diante. Baixe esta planilha para obter rapidamente alguns dados gerais para seu perfil de aprendizado.

1. Se um administrador ativou o E-mail de resumo e você não está na lista DND, você pode assinar ou cancelar os e-mails de resumo. Ative a opção abaixo.

   ![](assets/digest-email-option-learner.png)
   *Assinar ou cancelar a assinatura de e-mails de resumo*

   Com base na frequência definida pelo administrador, você, o aluno receberá o e-mail quinzenalmente ou mensalmente.

## Cancelar assinatura de e-mails de resumo {#unsubscribefromdigestemails}

Ao receber um email, você pode cancelar a assinatura do email de resumo clicando no **Cancelar inscrição** na parte inferior do email.

Depois de clicar em **[!UICONTROL Cancelar inscrição]**, você será redirecionado para sua **Configurações do perfil** , onde você pode desativar a opção de receber e-mails.

## Anatomia de um e-mail de resumo {#anatomyofadigestemail}

Um e-mail de resumo consiste nas seguintes seções:

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Seção</b></p></td>
   <td>
    <p><b>Descrição</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Resumo do treinamento pessoal</p></td>
   <td>
    <p>Esta seção personaliza as métricas de treinamento de um aluno mencionando o número de minutos gastos em treinamentos.</p>
    <p>Com base no tempo gasto pelo aluno, o conteúdo é personalizado de acordo com as regras definidas abaixo:</p>
    <p>Se (time_still) &gt;= 60 minutos, o seguinte texto é exibido:</p>
    <p><i>“Durante as últimas duas semanas/1 mês, você <b>(tempo_gasto)</b> minutos de treinamento para você se aperfeiçoar. Abaixo estão listadas algumas recomendações para que você possa saber mais.” </i></p>
    <p> Se (time_still) &lt;60 min, o seguinte texto é exibido:</p>
    <p><i>“Durante as últimas duas semanas/1 mês, você <b>(tempo_gasto)</b> minutos de treinamento para você se aperfeiçoar. Abaixo estão listadas algumas recomendações que esperamos que sejam úteis para começar e continuar.”</i></p></td>
  </tr>
  <tr>
   <td>
    <p>Atividade de treinamento</p></td>
   <td>
    <p>Esta seção exibe o resumo da atividade de treinamento dessa conta no nível da organização.</p>
    <p>O resumo da atividade de treinamento consiste no seguinte: </p>
    <ul>
     <li>Número de treinamentos disponíveis na conta.</li>
     <li>Número de coalunos que têm consumido ativamente as atividades de treinamento.</li>
     <li>Número de horas de aprendizado gastas pelos colegas de trabalho.</li>
     <li>Tempo médio (em minutos) gasto por colegas de trabalho na melhoria de habilidades na conta.</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Cursos recomendados</p></td>
   <td>
    <p>Esta é uma seção personalizada que inclui os treinamentos recomendados para os alunos. Nesta seção, um aluno pode ver três treinamentos que foram escolhidos pelo mecanismo de recomendação.</p>
    <p>Cada treinamento tem um botão Explorar que, quando clicado, redirecionará para a página inicial do aplicativo do aluno.  </p></td>
  </tr>
  <tr>
   <td>
    <p>Quadro de classificação</p></td>
   <td>
    <p>Exibe um gráfico de barras com cada barra representando um aluno e os pontos de gamificação de cada aluno (somente se o administrador tiver ativado a Gamificação para todos os alunos).</p>
    <p>O quadro de classificação exibe o seguinte:</p>
    <ul>
     <li>Pontos ganhos por um aluno.</li>
     <li>Pontos necessários para atingir o próximo nível.</li>
    </ul>
    <p>Há também um miniquadro de classificação que mostra o líder e dois alunos mais próximos do aluno nesse escopo de usuário.</p>
    <p>Se o quadro de classificação estiver vazio, esta seção não será exibida no email.</p></td>
  </tr>
  <tr>
   <td>
    <p><a>Publicações em redes sociais</a></p></td>
   <td>
    <p>Esta seção exibe as três postagens de redes sociais mais recentes.</p>
    <p>Um aluno pode ver a data de criação, o nome do quadro, o título da publicação, se houver, o nome de usuário e o ícone do criador. A publicação também pode conter um vídeo, documento, pdf ou qualquer outro arquivo.</p>
    <p>Cada publicação tem links para redirecionar o aluno para a página de aprendizado social no aplicativo do aluno.</p>
    <p>Se não houver publicações recentes, essa seção no e-mail não ficará visível para o aluno.</p></td>
  </tr>
 </tbody>
</table>

## Perguntas frequentes {#frequentlyaskedquestions}

**1. Como baixar uma transcrição do aluno como aluno?**

No canto superior direito, clique no **[!UICONTROL perfil do usuário]** > **[!UICONTROL Configurações do perfil]**. Na caixa de diálogo exibida, clique em **Baixar minha transcrição de aprendizado (XLS)**.

![](assets/dowload-lt.png)
*Baixar transcrição do aluno*
