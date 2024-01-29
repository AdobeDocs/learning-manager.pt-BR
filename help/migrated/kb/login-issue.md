---
jcr-language: en_us
title: Problemas de logon no Learning Manager
description: Problemas de login no Adobe Learning Manager
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---



# Problemas de logon no Learning Manager

## Problema

Não é possível fazer logon no Adobe Learning Manager.

## Erro

Ao tentar fazer logon no Adobe Learning Manager, a mensagem de erro, mostrada abaixo, é exibida:

![](assets/cp-error.png)

*Mensagem de erro para uma sessão expirada*

## Motivo

Quando um usuário faz logon por SSO, é criado um cookie de sessão que é armazenado no navegador. Ele também permite que o usuário faça logon em outros aplicativos. A maioria dos SSOs é configurada para fazer logoff após 24 horas. O usuário precisa autenticar novamente para uma nova sessão.

Em certos casos, um usuário não pode acessar o sistema devido a cookies SSO obsoletos. Esses cookies são encaminhados ao Adobe Learning Manager para autenticação. A sessão não é encerrada se um usuário não fechar o navegador por muito tempo ou não tiver feito logoff.

O Adobe Learning Manager rejeita esses cookies obsoletos, resultando em um erro.

## Resolução

Se um cookie obsoleto for rejeitado pelo Adobe Learning Manager, tente as seguintes opções:

1. Limpe os cookies do navegador e o cache. Para obter mais informações, consulte esta página [documento](unable-log-in-learning-manager.md).

   Como alternativa, o administrador de IDP pode definir um logoff forçado após um determinado tempo definido. Esta etapa autentica o usuário novamente para iniciar uma nova sessão.

Há outras razões pelas quais esse erro ocorre, mas a acima é um cenário comum.

## Links de referência:

[Microsoft: sessão de acesso condicional em uma vida](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
