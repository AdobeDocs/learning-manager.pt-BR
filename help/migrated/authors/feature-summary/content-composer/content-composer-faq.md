---
description: Encontre respostas para as perguntas mais comuns do Compositor de conteúdo, incluindo por que Gerar contorno está esmaecido, como renomear uma lição, por que as perguntas do quiz parecem desalinhadas e o que fazer quando o Publish está desativado.
jcr-language: en_us
title: Perguntas frequentes sobre o Adobe Learning Manager Content Composer
source-git-commit: ea6d296fa99686136ab08d756a20570a4681d704
workflow-type: tm+mt
source-wordcount: '584'
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
