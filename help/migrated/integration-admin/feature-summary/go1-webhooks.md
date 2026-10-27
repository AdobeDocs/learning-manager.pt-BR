---
description: Saiba como os webhooks de conclusão do Go1 ajudam o Adobe Learning Manager a capturar conclusões de cursos, mesmo quando os alunos fecham o navegador antecipadamente
jcr-language: en_us
title: Rastreamento de conclusão Go1 com webhooks
exl-id: 25c9c401-905f-4408-89ac-ac630a45a0c7
source-git-commit: aaea92d190b8ab22ce9f08c309faf5caa0b58a69
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%
---

# Rastreamento de conclusão Go1 com webhooks

## Visão geral

O Adobe Learning Manager agora oferece suporte ao rastreamento de conclusão baseado em webhook para conteúdo Go1. Esse aprimoramento melhora a confiabilidade da sincronização da conclusão do curso entre o Go1 e o Learning Manager. Os eventos de conclusão são capturados mesmo quando os alunos saem do reprodutor do curso logo após concluírem um curso.

O Go1 usa webhooks para enviar notificações de conclusão do curso para o Learning Manager sempre que um aluno conclui um curso Go1. O Learning Manager recebe e processa esses eventos de conclusão independentemente da sessão do navegador do aluno.

O Go1 também repete a entrega do webhook até que o Learning Manager confirme o recebimento do evento de conclusão. Isso ajuda a evitar registros de aprendizado perdidos ou incompletos.

## Problema resolvido por este aprimoramento

Anteriormente, o rastreamento da conclusão dependia da comunicação entre o player Go1 e o Learning Manager enquanto a sessão do navegador do aluno permanecia ativa. Se um aluno fechasse a janela do navegador ou navegasse antes do status de conclusão ser totalmente processado, o registro de conclusão poderia ser perdido.

Como resultado:

* As conclusões do curso podem não aparecer nas transcrições do aluno.
* Os administradores puderam encontrar discrepâncias entre as conclusões reais e as registradas.
* Os eventos de conclusão perdidos não puderam ser recuperados automaticamente.

## Fluxo de trabalho do evento

1. Um aluno inicia e conclui um curso Go1.
1. Go1 registra a conclusão.
1. O Go1 envia um webhook de conclusão para o Learning Manager.
1. O Learning Manager valida e aceita o evento de conclusão.
1. O Learning Manager atualiza o status de conclusão do aluno.
1. Se o Learning Manager não reconhecer o evento, o Go1 tentará a entrega novamente de forma automática.

## Perguntas frequentes

**Esta alteração requer configuração do administrador**

Não, essa alteração não requer nenhuma configuração de administrador.

**Os cursos Go1 existentes são afetados**

Não, os cursos Go1 existentes não são afetados. O aprimoramento melhora a sincronização de conclusão para o conteúdo Go1.

**O que acontece se um aluno fechar o navegador antecipadamente**

O Go1 envia o webhook de conclusão independentemente da sessão do navegador do aluno. Mesmo se o aluno sair do reprodutor do curso, o Go1 continuará tentando a entrega até que o Learning Manager confirme o evento de conclusão.
