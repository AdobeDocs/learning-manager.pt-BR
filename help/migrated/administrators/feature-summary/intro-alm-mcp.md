---
description: Estenda o Adobe Learning Manager no Claude, no ChatGPT Enterprise e nos agentes personalizados para que os alunos possam encontrar cursos, acompanhar o progresso e obter respostas.
jcr-language: en_us
title: Servidor do Protocolo de Contexto de Modelo da Adobe Learning Manager
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%
---

# Servidor do Protocolo de Contexto de Modelo da Adobe Learning Manager

O protocolo MCP é um padrão aberto que permite que um cliente AI descubra e chame ferramentas externas. O servidor Adobe Learning Manager MCP expõe as ferramentas do aluno do Adobe Learning Manager a qualquer cliente compatível com MCP, como um agente corporativo personalizado, Claude ou ChatGPT Enterprise. Os alunos fazem treinamento e progridem com o cliente que já usam, enquanto o conteúdo e os registros de aprendizado permanecem no Adobe Learning Manager.

## Como funciona

Um aluno envia uma solicitação de linguagem natural a um cliente do AI. O cliente seleciona a ferramenta do aluno mais relevante e chama o servidor MCP com o token de acesso OAuth do aluno. O Adobe Learning Manager executa a ferramenta como esse aluno e retorna o resultado, e o cliente compõe a resposta final.

Cada chamada carrega a identidade do aluno. Portanto, um aluno pode recuperar apenas o conteúdo e os registros aos quais já tem permissão de acesso.

O cliente do AI chama o servidor MCP, que encaminha cada solicitação para a ferramenta do aluno correspondente.

## Recursos do aluno

Os alunos trabalham em linguagem natural no cliente de IA que já usam. O cliente interpreta cada solicitação, chama a ferramenta apropriada do aluno do Adobe Learning Manager e retorna uma resposta com base no que o aluno pode acessar. Os alunos podem:

* Descubra os cursos, certificações e programações de aprendizado que estão disponíveis para eles.
* Acompanhe suas inscrições, andamento e prazos, incluindo o aprendizado que está prestes a expirar.
* Obtenha respostas com base no conteúdo de aprendizado.
* Gere um caminho de aprendizado personalizado a partir de seus objetivos e salve-o.

Para ver a lista completa, exiba a **referência das ferramentas do aluno**.

## Treinamento do cliente e do parceiro

>[!IMPORTANT]
>
>Os clientes que criam seus próprios agentes corporativos também podem se conectar ao servidor. Por exemplo, uma organização parceira pode oferecer aos seus próprios clientes acesso ao aprendizado por meio de seu próprio agente.

O treinamento de clientes e parceiros é o principal uso do servidor MCP. As organizações que criam seus próprios agentes corporativos de IA podem conectá-los às ferramentas do aluno do Adobe Learning Manager. Seus clientes e parceiros aprendem dentro do assistente que já usam, sem passar para um assistente de aprendizado separado.

Por exemplo, a Acme Inc. desenvolve seu próprio assistente corporativo de IA. Um parceiro da Acme Inc. visita o assistente para saber mais sobre os produtos da Acme Inc. O assistente se conecta à conta da Adobe Learning Manager da Acme Inc. por meio do servidor MCP e retorna respostas relacionadas ao aprendizado. O parceiro nunca sai da experiência da Acme Inc.

Essa abordagem permite que as organizações:

* Fornecer aprendizado dentro da experiência de IA existente de um parceiro.
* Estenda os agentes corporativos personalizados com as ferramentas do aluno do Adobe Learning Manager.
* Incorpore o aprendizado em seus próprios fluxos de trabalho.
* Integrar o aprendizado ao seu ecossistema corporativo de IA.

## Formação educacional do funcionário

Funcionários que já usam um cliente de IA, como Claude, podem obter suas informações de aprendizado lá. Por exemplo, um funcionário pode verificar o aprendizado atribuído, revisar as inscrições, localizar cursos em um tópico ou solicitar uma programação de aprendizado, sem alternar para o Adobe Learning Manager. Para solicitações de exemplo, saiba mais sobre [solicitações de exemplo para alunos](/help/migrated/learners/feature-summary/sample-prompts-for-learners.md).

Essa abordagem permite que os funcionários:

* Permaneça nas ferramentas que já usam.
* Alcance seu aprendizado onde quer que eles trabalhem.
* Use qualquer cliente de IA compatível com MCP como um ponto de entrada para o Adobe Learning Manager.
* Recupere informações de aprendizado sem alterar o contexto.

## Um servidor para ambos os públicos

Treinamento do cliente e do parceiro e treinamento do funcionário usam as mesmas ferramentas do aluno e o mesmo servidor. Somente o público muda. Escolha a abordagem que se adapta a quem são seus alunos.

| **Público-alvo** | **Exemplo** | **Onde os alunos trabalham** |
|----|----|----|
| Externos | Clientes e parceiros | Agente corporativo de IA da sua organização |
| Internos | Funcionários | Um cliente corporativo de IA, como Claude ou ChatGPT Enterprise |

## Configurar funções

A configuração é dividida em três funções.

* **Administrador:** cria um aplicativo cliente MCP no Adobe Learning Manager e o gerencia. Saiba mais sobre [configuração de um servidor MCP](/help/migrated/administrators/feature-summary/configure-mcp-admin.md).
* **Administrador de cliente de IA:** adiciona o servidor ao cliente de IA corporativa da organização, como Claude ou ChatGPT Enterprise.
* **Aluno:** seleciona **Conectar** no cliente AI, autentica a conexão e fornece os detalhes da conta do Adobe Learning Manager.

## Segurança das solicitações do aluno

Cada aluno autentica a conexão e fornece os detalhes da conta da Adobe Learning Manager. Cada solicitação é executada como esse aluno, portanto o cliente do AI retorna apenas as informações que o aluno pode acessar no Adobe Learning Manager. O servidor não concede aos alunos acesso adicional.

## Limitações

* O servidor MCP está disponível somente para contas de nível Adobe Learning Manager Ultimate.
* A disponibilidade de ferramentas depende do que o cliente de IA oferece suporte.
* O servidor trata cada solicitação como nova. As conversas de turnos múltiplos funcionam somente se o cliente de IA mantiver o contexto da conversa.
