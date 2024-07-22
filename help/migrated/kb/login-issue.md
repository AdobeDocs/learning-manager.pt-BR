---
jcr-language: en_us
title: Problemas de logon no Learning Manager
description: Problemas de logon no Adobe Learning Manager
contentowner: nluke
exl-id: 516c1a20-f185-4ace-a1e7-2cd89644863c
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 87%

---

# Problemas de logon no Learning Manager

## Problema

Não é possível fazer logon no Adobe Learning Manager.

## Erro

Ao tentar fazer logon no Adobe Learning Manager, a mensagem de erro, mostrada abaixo, é exibida:

![](assets/cp-error.png)

*Mensagem de erro para uma sessão expirada*

## Motivo

Quando um usuário faz logon por SSO, é criado um cookie de sessão que é armazenado no navegador. Isso também permite que o usuário faça logon em outros aplicativos. A maioria dos SSOs é configurada para fazer logoff após 24 horas. O usuário precisa autenticar novamente para uma nova sessão.

Em determinados casos, um usuário não pode acessar o sistema devido a cookies SSO obsoletos. Esses cookies são encaminhados ao Adobe Learning Manager para autenticação. A sessão não é finalizada se um usuário não fechar o navegador por muito tempo ou não tiver feito logoff.

O Adobe Learning Manager rejeita esses cookies obsoletos, resultando em um erro.

## Resolução

Se um cookie obsoleto for rejeitado pelo Adobe Learning Manager, tente as seguintes opções:

1. Limpe os cookies do navegador e o cache. Para mais informações, consulte este [documento](unable-log-in-learning-manager.md).

   Como alternativa, o administrador de IDP pode definir um logoff forçado após um determinado tempo definido. Esta etapa autentica o usuário novamente para iniciar uma nova sessão.

Há outras razões pelas quais esse erro ocorre, mas a acima é um cenário comum.

## Links de referência:

[Microsoft: sessão de acesso condicional em um tempo de vida](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
