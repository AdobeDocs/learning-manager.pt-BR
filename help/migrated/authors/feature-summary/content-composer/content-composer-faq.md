---
description: Encontre respostas para perguntas comuns do Compositor de conteúdo sobre edição de tópicos, comportamento do questionário, compatibilidade de Captivate, publicação e Compartilhar para revisão.
jcr-language: en_us
title: Perguntas frequentes sobre o Adobe Learning Manager Content Composer
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '1438'
ht-degree: 0%

---


# Perguntas frequentes sobre o Adobe Learning Manager Content Composer

Obtenha respostas às perguntas frequentes sobre o uso do Compositor de conteúdo.

**O botão Gerar Estrutura de Tópicos está esmaecido. O que devo fazer?**

Todos os três campos **Resumo**, **Título**, **Alunos** e **Objetivo** devem conter conteúdo antes de **Gerar Estrutura de Tópicos** ser ativado. Verifique na tela se há algum campo que ainda mostre texto de espaço reservado em itálico, como *Insira o perfil dos alunos aqui* ou *Insira o objetivo deste curso*. Preencha o campo vazio e o botão será ativado imediatamente.

**Não é possível selecionar a estrutura de tópicos para renomear uma lição. Por quê?**

A edição de contorno é conversacional na versão beta atual. Não é possível selecionar uma lição ou tópico na tela para renomeá-lo ou reordená-lo. Digite sua alteração em linguagem simples no painel de bate-papo do assistente.

Exemplos:

- “Renomear a Lição 1 para &#39;Como o Phishing Funciona&#39;”

- “Mover o tópico 1.3 para ser o primeiro tópico da Lição 2”

- “Excluir a lição 4 e distribuir seus tópicos na lição 3”

**A estrutura de tópicos gerada não corresponde ao que eu queria. O que deu errado?**

A estrutura de tópicos reflete o prompt e o resumo. Se a estrutura parecer inadequada, as causas mais comuns são um alerta que abrange muitos tópicos de uma só vez ou um objetivo de aprendizado que não nomeia as habilidades ou comportamentos específicos que o curso deve desenvolver.

**A IA ignorou uma seção importante do meu arquivo carregado. Como corrigir isso?**

O compositor de conteúdo prioriza as seções do arquivo de origem que são mais relevantes para o seu objetivo de aprendizado. Se uma seção foi ignorada, provavelmente não foi refletida no objetivo.

Para corrigir isso:

1. Retorne ao painel **Resumo** e atualize o objetivo para nomear explicitamente o tópico ausente.

2. Peça ao assistente para regenerar a estrutura de tópicos: “Regenerar a estrutura de tópicos, certificando-se de incluir a seção de política de retenção de dados”.

Você também pode adicionar o conteúdo ausente manualmente como um novo tópico na conversa do outline: “Adicione um novo tópico à Lição 2 chamado &#39;Política de retenção de dados&#39;.”

**Posso usar o Compositor de Conteúdo com o Adobe Captivate?**

Não. O Compositor de conteúdo e o Adobe Captivate não compartilham um fluxo de trabalho de ida e volta. Não é possível abrir projetos do Compositor de conteúdo no Captivate nem abrir projetos do Captivate no Compositor de conteúdo.

Um MP4 exportado em Captivate pode ser inserido como um componente de **Vídeo** no Compositor de Conteúdo.

**Posso usar o Compositor de Conteúdo para treinamento regulamentado ou de conformidade?**

Sim Este é um dos seus casos mais fortes. Faça upload dos documentos de política ou procedimento em Gerenciar arquivos de origem e selecione Restringir saída ao conteúdo dos arquivos para que o AI gere apenas do que você forneceu, em vez de complementar com conhecimento geral.

**Por que as verificações de conhecimento não estão graduadas?**

As verificações de conhecimento no Compositor de conteúdo são projetadas para o reforço da aprendizagem durante uma aula, não para pontuação. Eles fornecem feedback imediato ao aluno, mas não produzem uma nota ou registro de conclusão.

Somente as avaliações do questionário de fim de aula são classificadas. Se precisar de uma avaliação que contribua para a pontuação de um aluno, use o quiz, não um componente de verificação de conhecimento.

**As perguntas do quiz não correspondem ao que o curso ensina. Como corrigir isso?**

O compositor de conteúdo usa IA para gerar perguntas do quiz, e a saída de IA é não determinística. As perguntas nem sempre podem refletir exatamente o que você espera. Revise todas as perguntas do quiz após o curso ser gerado, edite qualquer pergunta que precise de ajuste diretamente no Editor de cursos e verifique se o conteúdo é preciso antes de publicar.

## Sobre o recurso Compartilhar para revisão

**O que é Compartilhar para Revisão no Compositor de Conteúdo?**

Compartilhar para revisão permite distribuir um curso para revisores para feedback antes de publicar. Os revisores abrem o curso em um navegador, adicionam comentários em qualquer componente e tentam fazer o quiz, sem instalar o Compositor de conteúdo ou precisar de uma assinatura.

**Os revisores precisam de uma licença do Compositor de Conteúdo?**

Não. Os revisores não precisam de uma assinatura ou instalação do Compositor de conteúdo. Qualquer pessoa com o link de revisão pode abrir o curso em seu navegador.

**Os revisores precisam de uma Adobe ID para participar?**

Sim Revisar um curso exige fazer logon, portanto, é necessário ter uma Adobe ID para participar. Depois de fazer logon, os revisores podem abrir o curso, adicionar comentários, tentar fazer o quiz e usar @mentions para marcar o autor ou outros revisores.

**Os revisores podem editar o conteúdo do curso?**

Não. O acesso de revisão é somente para comentários. Os revisores podem adicionar, responder, resolver e filtrar comentários, mas não podem alterar o texto, as imagens ou a estrutura do curso.

Onde os arquivos de revisão são armazenados? Os arquivos de revisão estão hospedados na nuvem Adobe. Os autores não precisam gerenciar o armazenamento de arquivos ou enviar os arquivos do curso diretamente aos revisores.

### Compartilhamento e acesso

**Quem pode acessar um link de revisão?**

Por padrão, somente as pessoas que você convida por nome ou email podem acessar o projeto. Verifique isso na seção Quem tem acesso do painel Compartilhar projeto antes de enviar o link.

**Posso convidar colaboradores externos que não sejam usuários do Adobe?**

Sim, você pode convidar qualquer pessoa por endereço de email. No entanto, eles precisam de uma conta Adobe para fazer logon e revisar o curso.

**Posso adicionar revisores depois que a revisão já tiver sido iniciada?**

Sim Abra o painel Compartilhar projeto a qualquer momento, adicione nomes ou endereços de email e selecione Convidar para comentar. Os novos revisores recebem um convite imediatamente.

**Posso remover um revisor após o compartilhamento?**

Sim No painel Compartilhar projeto, localize o revisor em Quem tem acesso e remova-o. Se eles tentarem abrir o curso usando um link compartilhado anteriormente, verão uma mensagem de acesso negado.

**O que acontece se um revisor perder o acesso?**

Eles podem selecionar Solicitar acesso na tela de acesso negado. O proprietário do curso recebe uma notificação para restaurar o acesso.

### Comentários e feedback

Os revisores podem comentar em uma parte específica do curso?

Sim Os revisores selecionam qualquer componente do curso — um bloco de texto, imagem ou pergunta do quiz — e adicionam um comentário diretamente sobre esse elemento. Os comentários permanecem contextualmente vinculados ao componente no qual foram adicionados.

**Vários revisores podem comentar ao mesmo tempo?**

Sim Todos os revisores veem os comentários uns dos outros no painel Comentários e podem responder, resolver ou @mention uns aos outros.

**Posso filtrar comentários para encontrar comentários não resolvidos?**

Sim Use o filtro Resolvido no painel Comentários para mostrar apenas comentários não resolvidos. Você também pode filtrar por Revisores para ver o feedback de uma pessoa específica ou por Tempo para encontrar os comentários mais recentes.

**Como marcar outro revisor em um comentário?**

Digite @ seguido do nome ou endereço de email e selecione-os na lista suspensa. Os usuários marcados receberão uma notificação. Isso requer que o revisor faça logon com uma Adobe ID.

#### Acesso ao quiz e ao aluno

**Os revisores podem tentar fazer o quiz?**

Sim Os revisores podem tentar fazer o quiz até o número especificado de tentativas. Suas pontuações não são registradas e não afetam o curso ou qualquer relatório LMS.

**Qual é a diferença entre compartilhar para revisão e compartilhar para alunos?**

Compartilhar para revisão dá acesso ao curso com o painel de comentários ativado, destinado a colegas e partes interessadas que dão feedback. Compartilhar para alunos fornece acesso ao curso sem comentários, destinado a alunos que não estão inscritos por meio de um LMS. As pontuações dos alunos também não são registradas por meio de um link direto.

### Atualizar e fechar uma revisão

**Preciso criar uma nova revisão após fazer alterações?**

Não. O URL de revisão permanece o mesmo depois que você atualiza o curso. Selecione **Compartilhar** para notificar os revisores de que uma versão atualizada está disponível.

**Os revisores serão notificados quando eu atualizar o curso?**
Os revisores veem um banner de notificação ao abrirem o link de revisão após uma atualização. Eles podem selecionar Recarregar para exibir a versão mais recente.

**Os comentários antigos permanecem após a atualização de um curso?**

Sim Os comentários existentes persistem nas atualizações. Os revisores e autores podem continuar resolvendo os comentários na versão atualizada.

**O que acontece com o link de um aluno após eu atualizar o curso?**

O link do aluno existente continua a mostrar a versão anterior. Gere um novo link após cada atualização e compartilhe-o com os alunos para garantir que eles acessem o conteúdo mais recente.

**Como exibir as atualizações do projeto?**

Se o autor atualizar o curso enquanto você o estiver revisando, uma notificação será exibida.

![](../assets/68_newer_version_available_reload_notification.png)

- Selecione **Recarregar** para carregar a versão mais recente ou descarte a notificação para continuar revisando a versão atual. É seguro recarregar. Seus comentários existentes persistem mesmo após as atualizações do projeto, portanto, você não perderá nenhum feedback que já tenha adicionado.

## Tentar o quiz como revisor

Como revisor, você pode tentar fazer o quiz até o número especificado de vezes, mas suas pontuações não são gravadas.

- Selecione **INICIAR QUIZ** para tentar fazer o quiz.

  ![](../assets/66_final_quiz_start_screen_attempts_info.png)

- Após a conclusão, os resultados são exibidos. Aqui, você pode selecionar Revisar respostas para ver quais perguntas acertaram ou erraram ou Refazer o quiz para tentar novamente.

  ![](../assets/67_quiz_results_attempts_remaining_reviewer.png)




