---
description: Pesquise o que os alunos podem fazer com o servidor do Protocolo de Contexto de Modelo da Adobe Learning Manager e quais ferramentas MCP oferecem suporte a cada recurso
jcr-language: en_us
title: Ferramentas do aluno para o servidor do Protocolo de Contexto Modelo
exl-id: 4509b984-d0ba-4b7e-a0bb-803aa235fd1e
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%
---

# Ferramentas do aluno para o servidor do Protocolo de Contexto Modelo

Cada recurso é executado como o aluno conectado, depois que o aluno se conecta. Uma solicitação retorna apenas o que esse aluno pode acessar no Adobe Learning Manager. Consulte [Conectar seu cliente de IA](/help/migrated/learners/feature-summary/connect-ai-client-to-alm-learner.md) para obter mais informações.

## Recursos do aluno

| **Recurso** | **O que os alunos podem fazer** | **Exemplo de solicitação** |
|----|----|----|
| Pesquisar conteúdo de aprendizado | Encontrar cursos, certificações e programações de aprendizado | Quais cursos de liderança estão disponíveis? |
| Exibir inscrições | Verificar inscrições e vencimento de aprendizado | Quais dos meus cursos estão prestes a expirar? |
| Fazer perguntas de aprendizado | Obtenha respostas em conteúdo de aprendizado | O que significa o gerenciamento de riscos da cadeia de fornecimento no FedRAMP? |
| Gerar caminhos de aprendizado | Criar programações de aprendizado personalizadas | Ajude-me a encontrar cursos para aprimorar o gerenciamento de projetos. |
| Salvar caminhos de aprendizado | Salvar caminhos de aprendizado gerados | Salve este caminho de aprendizado. |

## Ferramentas MCP compatíveis

O servidor MCP do Assistente do aluno expõe as seguintes ferramentas voltadas para o aluno.

| **Ferramenta MCP** | **Finalidade** | **Dá suporte a recursos** |
|----|----|----|
| Pesquisa | Pesquisar conteúdo de aprendizado disponível | Pesquisar conteúdo de aprendizado |
| Obter Inscrição | Recuperar informações de inscrição do aluno | Exibir inscrições |
| Agente de respostas | Responder a perguntas usando conteúdo de aprendizado | Fazer perguntas de aprendizado |
| Obter usuário | Identificar o aluno conectado para cada solicitação | Todos os recursos |
| Obter objeto de aprendizado | Recuperar detalhes de um objeto de aprendizado, como descrição e duração | Pesquisar conteúdo de aprendizado, Exibir inscrições |
| Gerar caminho de aprendizagem | Criar caminhos de aprendizado recomendados | Gerar caminhos de aprendizado |
| Salvar caminho de aprendizado | Salvar caminhos de aprendizado gerados | Salvar caminhos de aprendizado |

>[!IMPORTANT]
>
>Os nomes das ferramentas são mostrados para referência e podem variar dependendo da implementação do cliente.

