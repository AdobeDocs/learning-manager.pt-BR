---
description: Permita que os alunos descubram cursos, acompanhem o progresso e obtenham respostas do conteúdo do Adobe Learning Manager dentro do Claude, do ChatGPT Enterprise e de agentes personalizados.
jcr-language: en_us
title: Servidor do Protocolo de Contexto de Modelo da Adobe Learning Manager
exl-id: 8d0a25a6-1301-4f68-8db7-e3b1d3ff6537
source-git-commit: f6dc1e97076edf812862b80a6ed5931989c660da
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%
---

# Servidor do Protocolo de Contexto de Modelo da Adobe Learning Manager

## Visão geral

O Protocolo de contexto de modelo (MCP) é uma maneira padrão para um cliente AI se conectar a ferramentas. O servidor MCP do Adobe Learning Manager leva o aprendizado para onde os alunos já trabalham. Ele expõe as ferramentas do aluno do Adobe Learning Manager a qualquer cliente de IA compatível com MCP, como um agente corporativo personalizado, Claude ou ChatGPT. Os alunos podem acessar seus treinamentos e progredir no mesmo cliente, enquanto o conteúdo permanece no Adobe Learning Manager.

## Recursos do aluno

Os alunos trabalham em linguagem natural no cliente de IA que já usam. O cliente interpreta cada solicitação, chama a ferramenta apropriada do aluno do Adobe Learning Manager e retorna uma resposta com base no que o aluno pode acessar. Os alunos podem:

* Descubra os cursos, certificações e programações de aprendizado que estão disponíveis para eles.
* Acompanhe suas inscrições, andamento e prazos, incluindo o aprendizado que está prestes a expirar.
* Obtenha respostas com base no conteúdo de aprendizado.
* Gere um caminho de aprendizado personalizado a partir de seus objetivos e salve-o.
Para ver a lista completa, exiba a **referência das ferramentas do aluno**.

O cliente do AI chama o servidor MCP, que encaminha cada solicitação para a ferramenta do aluno correspondente.

Para ver a lista completa, exiba a **referência das ferramentas do aluno**.

## Treinamento do cliente e do parceiro

O treinamento de clientes e parceiros é o principal uso do servidor MCP. As organizações que criam seus próprios agentes corporativos de IA podem conectá-los às ferramentas do aluno do Adobe Learning Manager. Seus clientes e parceiros aprendem dentro do assistente que já usam, sem passar para um assistente de aprendizado separado.

Por exemplo, a Acme Inc. desenvolve seu próprio assistente corporativo de IA. Um parceiro da Acme Inc. visita o ambiente da Tech Corp para conhecer os produtos da Tech Corp. O assistente da Acme se conecta à sua conta da Adobe Learning Manager por meio do servidor MCP e retorna respostas relacionadas à aprendizagem, de modo que o parceiro nunca sai da experiência da Acme.

Essa abordagem permite que as organizações:

* Ofereça aprendizado dentro da experiência de IA existente de um parceiro.
* Permita que os agentes corporativos personalizados usem as ferramentas do aluno do Adobe Learning Manager.
* Crie aprendizado em seus próprios fluxos de trabalho.
* Integrar o aprendizado ao seu ecossistema corporativo de IA.

## Formação educacional do funcionário

Funcionários que já usam um cliente de IA, como Claude, podem obter suas informações de aprendizado lá. Por exemplo, um funcionário pode verificar o aprendizado atribuído, revisar as inscrições, localizar cursos em um tópico ou solicitar uma programação de aprendizado, sem alternar para o Adobe Learning Manager. Para solicitações de exemplo, consulte [exemplos de prompts para alunos](https://word-edit.officeapps.live.com/docs/sample-prompts-adobe-learning-manager-learners).

Essa abordagem permite que os funcionários:

* Fique nas ferramentas que eles já usam.
* Alcance seu aprendizado onde quer que eles trabalhem.
* Use qualquer cliente AI compatível com MCP como ponto de entrada para o Adobe Learning Manager.
* Obtenha informações de aprendizado sem alterar o contexto.

## Um servidor para ambos os públicos

Treinamento do cliente e do parceiro e treinamento do funcionário usam as mesmas ferramentas do aluno e o mesmo servidor. Somente o público muda. Escolha a abordagem que se adapta a quem são seus alunos.

| **Público-alvo** | **Exemplo** | **Onde os alunos trabalham** |
|----|----|----|
| Externos | Clientes e parceiros | Agente corporativo de IA da sua organização |
| Internos | Funcionários | Um cliente corporativo de IA, como Claude ou ChatGPT Enterprise |

## Configurar funções

A configuração é dividida entre três funções.

* **Administrador:** cria um aplicativo cliente MCP no Adobe Learning Manager e o gerencia. Consulte [configurar um servidor MCP](https://word-edit.officeapps.live.com/docs/configure-model-context-protocol-server-adobe-learning-manager).
* **Administrador de cliente de IA:** adiciona o servidor ao cliente de IA corporativa da organização, como Claude ou ChatGPT Enterprise.
* **Aluno:** seleciona **Conectar** no cliente AI, autentica a conexão e fornece os detalhes da conta do Adobe Learning Manager.

## Segurança das solicitações do aluno

Cada aluno autentica a conexão e fornece os detalhes da conta da Adobe Learning Manager. A solicitação é executada como esse aluno, portanto o cliente do AI retorna apenas as informações que o aluno pode acessar no Adobe Learning Manager. O servidor não concede aos alunos acesso extra.

## Limitações do MCP nesta atualização

* A disponibilidade de ferramentas depende do que o cliente de IA oferece suporte.
* Cada solicitação é tratada como nova. As conversas de turnos múltiplos funcionam somente se o cliente de IA mantiver o contexto da conversa.
