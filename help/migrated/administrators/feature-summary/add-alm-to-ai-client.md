---
description: Adicione o servidor Adobe Learning Manager MCP ao seu cliente corporativo de IA, como Claude ou ChatGPT Enterprise, para que os alunos possam se conectar a ele
jcr-language: en_us
title: Adicionar o Adobe Learning Manager ao seu cliente corporativo de IA
exl-id: d893efb7-dc0d-4a3a-88d6-b315340e5daa
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%
---

# Adicionar o Adobe Learning Manager ao seu cliente corporativo de IA

Você precisa de privilégios de administrador no seu cliente AI. Obtenha primeiro o URL do ponto de extremidade, a ID do cliente e a chave secreta do seu administrador do Adobe Learning Manager. Exiba **Configurar um servidor do Protocolo do Contexto do Modelo** para obter mais detalhes.

## Adicionar o conector

1. Faça logon no cliente corporativo de IA como administrador.
2. Abra as configurações do administrador para conectores.
3. Adicione um conector personalizado que use o Protocolo de Contexto de Modelo.
4. Insira o URL do ponto de extremidade do Adobe Learning Manager MCP.
5. Insira a ID do cliente e a chave secreta do administrador do Adobe Learning Manager.
6. Salve o conector.
7. Disponibilize o conector para seus alunos.

>[!NOTE]
>
>As interfaces de cliente de IA mudam com frequência. Se essas etapas não corresponderem ao seu cliente, consulte a documentação do fornecedor do cliente AI para adicionar um conector remoto.

## Solução de problemas

**Os alunos não veem o conector.** Confirme se o conector está ativado para o espaço de trabalho ou grupo do aluno.

**A autorização falha quando um aluno seleciona Conectar.** Verifique se a ID do cliente e a chave secreta correspondem aos valores na página **Credenciais do cliente** do servidor no Adobe Learning Manager.
