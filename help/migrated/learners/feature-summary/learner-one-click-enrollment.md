---
description: A inscrição com um clique permite que os alunos cliquem em qualquer link profundo para um módulo compartilhado por administradores e acessem o conteúdo imediatamente, sem passar por várias etapas para clicar em inscrever-se e, em seguida, iniciar o curso. Isso economiza tempo e melhora o acesso ao curso.
jcr-language: en_us
title: Usar a inscrição com um clique no Adobe Learning Manager
contentowner: mmanuel
source-git-commit: 87971737d1d9838d8b29035b5b9bf718742da1eb
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 1%

---


# Inscrição com um clique no Adobe Learning Manager

Receba o deep link do seu administrador por e-mail, bate-papo ou outra plataforma de mensagens para se inscrever em um módulo de treinamento ou curso. Selecione o link para se inscrever instantaneamente e inicie o módulo, sem etapas adicionais.

## Inscrever um aluno e redirecionar o aluno para o curso

Observe os seguintes cenários e suas ações correspondentes. Como aluno, se você clicar no link profundo que foi enviado para você, uma das seguintes opções acontecerá dependendo do cenário em que você está:

| SN | Cenário | Ação |
| --- | --- | --- |
| 1 | Curso de módulo único e não ordenado | Você será inscrito automaticamente e o reprodutor abrirá. Você precisa pressionar Reproduzir para reproduzir o vídeo. |
| 2 | Curso de vários módulos e não ordenado | Você será inscrito automaticamente e poderá acessar o módulo específico ao qual o deep link está vinculado. Você precisa pressionar Reproduzir para reproduzir o vídeo. |
| 3 | Curso de vários módulos e ordenado | Você será redirecionado para a página Visão geral com uma mensagem informando que é necessário concluir os cursos anteriores antes de iniciar o curso atual, caso não tenha concluído os anteriores. Nesse caso, você será inscrito automaticamente e entrará no primeiro módulo do curso. |
| 4 | O curso tem pré-requisitos | Se os pré-requisitos estiverem completos, você pode iniciar o módulo no player. Pressione Reproduzir para reproduzir o vídeo. Se não estiverem concluídos, a seguinte mensagem será exibida: “Não é possível ignorar os cursos de pré-requisito. Conclua todos os cursos de pré-requisito antes de iniciar este curso. |
| 5 | Curso com lista de espera | Você será inscrito. Você aparecerá na página de visão geral do curso e será adicionado à lista de espera. Você também verá uma mensagem informando que o curso está na lista de espera. |
| 6 | Se você já estiver inscrito no curso para o qual o deep link foi gerado. | Você pousará no módulo e o reprodutor iniciará. Pressione Reproduzir para reproduzir o vídeo. |

## Status da autenticação e comportamento do deep link

Além dos cenários acima, há mais dois comportamentos do usuário relacionados ao status de autenticação (conectado e desconectado).

* Se você clicar em um deep link e não estiver conectado à Adobe Learning Manager, será redirecionado para a página de logon. Efetue login e o deep link o redirecionará para o módulo específico.

* Se você clicar em um deep link e estiver conectado à Adobe Learning Manager, será redirecionado para o módulo diretamente.

## Suporte imersivo para dispositivos móveis e Web

Os cenários a seguir são aplicáveis às versões para dispositivos móveis e Web do Adobe Learning Manager.

* Se você não tiver a versão para desktop do Adobe Learning Manager e receber um deep link, selecionar o link o redirecionará para a página de logon do Adobe Learning Manager em seu navegador, se você não estiver conectado à versão para Web ou dispositivos móveis.
* Se você não tiver a versão para desktop do Adobe Learning Manager e receber um deep link, selecioná-lo redirecionará diretamente para o módulo do Adobe Learning Manager em seu navegador, se você já estiver conectado à versão para Web ou dispositivos móveis.

## Reprodução automática restrita pelo navegador

Quando você clica em um deep link, ele o redireciona para um módulo ou uma página de login, caso você não esteja conectado. Se o módulo for um vídeo, o reprodutor não reproduzirá o vídeo automaticamente. Em todos os casos, o navegador impede que o reprodutor reproduza o vídeo automaticamente. É necessário pressionar Reproduzir manualmente para reproduzir o vídeo.
