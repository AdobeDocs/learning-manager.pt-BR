---
description: Leia este artigo para saber como definir as configurações do perfil do aluno e adicionar uma foto do perfil. Saiba como baixar a transcrição do aluno para seu perfil.
jcr-language: en_us
title: Configurações do perfil
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 75%

---



# Configurações do perfil

Leia este artigo para saber como definir as configurações do perfil do aluno e adicionar uma foto do perfil. Saiba como baixar a transcrição do aluno para seu perfil.

## Definir configurações do perfil {#configuringprofilesettings}

1. Na parte superior direita da página, clique na seta suspensa ao lado de seu perfil ou foto.
1. Selecione Configurações do perfil.
1. Na caixa de diálogo pop-up exibida, você poderá realizar as seguintes ações:

   * Adicionar/atualizar foto de perfil: passe o mouse sobre a foto. Clique em Carregar e adicione uma foto. Clique em Editar para alterar a foto.
   * Excluir foto: passe o mouse sobre a foto do perfil. Clique em Excluir.
   * Adicione o conteúdo Sobre mim clicando na área de texto abaixo dela.
   * Modifique o conteúdo Sobre mim clicando em Editar ao lado do campo.
   * Defina a localidade para seu perfil. No menu suspenso Localidade, selecione o idioma de sua escolha.
   * Ajuste o Local atual do seu perfil.
   * Defina o Fuso horário para seu perfil.
   * Baixe a transcrição dos alunos com seus dados.

   ![](assets/learner-preferences.png)
   *Exibir preferências do aluno*

   Ao clicar no link Baixar XLS da minha transcrição de aprendizado, é baixada uma planilha do Excel no sistema. Esta planilha do Excel contém detalhes sobre os objetos de aprendizado consumidos por você, o status de conclusão de cada objeto de aprendizado, as datas de vencimento correspondentes, as habilidades alcançadas, e assim por diante. Faça download dessa planilha para obter rapidamente alguns dados totais para seu perfil de aprendizagem.

1. Se um administrador ativou o E-mail de resumo e você não está na lista DND, você pode assinar ou cancelar os e-mails de resumo. Ative a opção abaixo.

   ![](assets/digest-email-option-learner.png)
   *Assinar ou cancelar a assinatura de e-mails de resumo*

   Com base na frequência definida pelo administrador, você receberá o e-mail quinzenalmente ou mensalmente.

## Cancelar a assinatura de e-mails de resumo {#unsubscribefromdigestemails}

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
    <p>Se (time_used) &gt;= 60 minutos, o seguinte texto é exibido:</p>
    <p><i>“Durante as últimas duas semanas/1 mês, você <b>(tempo_gasto)</b> minutos de treinamento para você se aperfeiçoar. Abaixo estão listadas algumas recomendações para que você possa saber mais.” </i></p>
    <p> Se (time_still) &lt;60 min, o seguinte texto é exibido:</p>
    <p><i>“Durante as últimas duas semanas/1 mês, você <b>(tempo_gasto)</b> minutos de treinamento para você se aperfeiçoar. Abaixo estão listadas algumas recomendações que esperamos que sejam úteis para começar e continuar.”</i></p></td>
  </tr>
  <tr>
   <td>
    <p>Atividade de treinamento</p></td>
   <td>
    <p>Esta seção exibe o resumo da atividade de treinamento em nível de organização para essa conta.</p>
    <p>O resumo da atividade de treinamento consiste no seguinte: </p>
    <ul>
     <li>Número de treinamentos disponíveis na conta.</li>
     <li>Número de co-alunos que têm consumido ativamente as atividades de treinamento.</li>
     <li>Número de horas de aprendizado gastas pelos colegas de trabalho.</li>
     <li>Tempo médio (em minutos) gasto pelos colegas na melhoria das qualificações na conta.</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Cursos recomendados</p></td>
   <td>
    <p>Esta é uma seção personalizada que inclui os treinamentos recomendados para os alunos. Nesta seção, um aluno pode ver três treinamentos escolhidos pelo mecanismo de recomendação.</p>
    <p>Cada treinamento tem um botão Explorar, que, quando clicado, redirecionará para a página inicial do aplicativo do aluno.  </p></td>
  </tr>
  <tr>
   <td>
    <p>Quadro de classificação</p></td>
   <td>
    <p>Exibe um gráfico de barras com cada barra representando um aluno junto com os pontos de gamificação de cada aluno (somente se o administrador ativou Gamificação para todos os alunos).</p>
    <p>O quadro de classificação exibe o seguinte:</p>
    <ul>
     <li>Pontos obtidos por um aluno.</li>
     <li>Pontos necessários para alcançar o próximo nível.</li>
    </ul>
    <p>Há também um miniquadro de classificação que mostra o líder e dois alunos mais próximos do aluno no escopo do usuário.</p>
    <p>Se o quadro de classificação estiver vazio, esta seção não será mostrada no e-mail.</p></td>
  </tr>
  <tr>
   <td>
    <p><a>Publicações em redes sociais</a></p></td>
   <td>
    <p>Esta seção exibe as três publicações em redes sociais mais recentes.</p>
    <p>Um aluno pode ver a data de criação, o nome do quadro, o título da publicação, se houver, o nome de usuário e o ícone do criador. A publicação também pode conter vídeo, documento, pdf ou qualquer outro arquivo.</p>
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
