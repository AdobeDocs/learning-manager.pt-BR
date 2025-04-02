---
description: Os administradores podem iniciar uma sessão representada na qual podem fazer logon em nome de qualquer usuário de conta nas funções de aluno e gerente.
jcr-language: en_us
title: Representação do aluno e do gerente
contentowner: saghosh
exl-id: 0306f255-283f-43b9-9494-11b3dc3765da
source-git-commit: 1693bb3905895be0c9a883339a1a5c7d71bb3f33
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 64%

---

# Representação do aluno e do gerente {#impersonation-of-learner-and-manager}

Em grandes organizações, a equipe de suporte ao cliente precisa de capacidade de representação para depurar problemas enfrentados pelos alunos.

Com essa capacidade de representar outros usuários, os administradores podem identificar e executar todas as atividades feitas pelos alunos e gerentes de suas organizações.

>[!NOTE]
>
>Os administradores personalizados não têm a capacidade de representar usuários; somente os administradores podem realizar a representação do usuário.

## Como funciona

Os administradores podem pesquisar um usuário (interno ou externo) e, em seguida, representar um usuário. O administrador é redirecionado para a página do usuário (aplicativo do gerente, se aplicável, ou aplicativo do aluno) e faz o logon do administrador fora da sessão. O administrador é redirecionado para a página Concluir seu perfil, caso ela esteja configurada para o usuário que foi representado pelo administrador.

Aqui está o que você deve ter em mente ao representar um usuário:

* Todos os administradores veem esse recurso por padrão.
* Somente usuários ativos na conta podem ser representados.
* Um administrador não pode se representar.
* Um administrador personalizado que tenha acesso à página Usuários pode representar usuários.
* Um administrador/administrador personalizado só pode representar por 60 minutos.
* Um administrador personalizado com acesso somente leitura não pode representar usuários.

## Representar um usuário

Para representar um usuário, siga as etapas abaixo:

1. Faça logon no aplicativo como administrador.
1. Selecione Perfil > Representar usuário.

   Você só pode representar um usuário por vez.

1. Procure um usuário (interno/externo) na caixa de pesquisa presente na janela modal. Você só pode representar um usuário por vez. Selecione Continuar.

   Você também pode pesquisar com e-mail do usuário, UUID e assim por diante.

1. Uma mensagem é exibida com a confirmação de que você representará um usuário.

   Selecione Continuar.

   Uma mensagem de confirmação, “Modo de representação: Você está conectado como “username (user email)”. Logout” aparece no cabeçalho da página.

**Uma sessão representada dura 60 minutos.**

Ao alterar para a função de aluno ou gerente, é exibida uma mensagem indicando que o administrador/administrador personalizado está no modo de representação do usuário.

## Relatório de logon e acesso

O logon e o acesso de um administrador são capturados no logon e no relatório de acesso. Para cada usuário representado pelo administrador, um registro é criado no relatório.

As colunas que fazem parte desse recurso são:

* Representado por Nome de Usuário
* Representado por E-mail do Usuário

Essas colunas são adicionadas no final do relatório.

Cada logon é contado separadamente no relatório.

## O que não é suportado

* Representação de componentes AEM
* Representação no aplicativo para dispositivos móveis.
* Representação em dispositivos móveis imersivos.
* Representação de aplicativos imersivos. Aplicável somente a aplicativos ALM.

## Perguntas frequentes

+++Posso fazer logon no Adobe Learning Manager mesmo quando estou sendo representado?

Sim, o logon de um usuário é independente da representação.
+++

+++Os eventos de representação são contados de forma exclusiva?

Sim, cada acesso/visita de logon por administrador enquanto a representação será contada separadamente.
+++

+++Qual é o tempo limite de representação?

60 minutos. Se um usuário que está representando fechar a janela do navegador e navegar para qualquer URL principal em 60 minutos, a atividade de representação continuará e a mensagem do banner deverá ser exibida.
+++
