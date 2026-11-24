---
description: Procure o que os alunos podem fazer com o servidor do Protocolo de contexto de modelo da Adobe Learning Manager e quais ferramentas oferecem suporte a cada recurso.
jcr-language: en_us
title: Ferramentas do aluno para o servidor do Protocolo de Contexto Modelo
exl-id: 4509b984-d0ba-4b7e-a0bb-803aa235fd1e
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%
---

# Ferramentas do aluno para o servidor do Protocolo de Contexto Modelo

## Visão geral

Cada recurso é executado como o aluno conectado, depois que o aluno se conecta. Uma solicitação retorna apenas o que esse aluno pode acessar no Adobe Learning Manager. Saiba mais sobre [conectando seu cliente de IA](/help/migrated/learners/feature-summary/connect-ai-client-to-alm-learner.md).

## Recursos do aluno

| **Recurso** | **O que os alunos podem fazer** | **Exemplo de solicitação** |
|----|----|----|
| Pesquisar conteúdo de aprendizado | Encontrar cursos, certificações e programações de aprendizado | Quais cursos de liderança estão disponíveis? |
| Exibir inscrições | Verificar inscrições e vencimento de aprendizado | Quais dos meus cursos estão prestes a expirar? |
| Fazer perguntas de aprendizado | Obtenha respostas em conteúdo de aprendizado | O que significa o gerenciamento de riscos da cadeia de fornecimento no FedRAMP? |
| Gerar caminhos de aprendizado | Criar programações de aprendizado personalizadas | Ajude-me a encontrar cursos para aprimorar o gerenciamento de projetos. |
| Salvar caminhos de aprendizado | Salvar caminhos de aprendizado gerados | Salve este caminho de aprendizado. |

## Ferramentas MCP compatíveis

O servidor MCP do Adobe Learning Manager expõe as seguintes ferramentas do aluno.

| **Nome da ferramenta** | **Descrição** |
|----|----|
| search_learning_items | Pesquise no catálogo cursos, programações de aprendizado, certificações, ajudas de tarefa, medalhas, habilidades, catálogos e etiquetas. Filtre por estado do aluno, habilidade, tag, catálogo, formato de entrega, preço e idioma. Para perguntas do assunto, use answer_learning_content_question. Exemplo: “Cursos de Python para iniciantes”. |
| list_my_learning_enrollments | Liste os cursos inscritos, em andamento e concluídos do aluno, programações de aprendizado, certificações e ajudas de tarefa, com estado, progresso e prazo. Filtre por tipo de objeto de aprendizado ou status de conclusão. Os resultados mostram primeiro as inscrições mais recentes. Exemplo: “O que vence em breve?” |
| get_learning_object | Obtenha os detalhes completos de um curso, caminho de aprendizado, certificação ou ajuda de tarefa por ID, opcionalmente com instâncias, habilidades e objetos de subaprendizado. Obtenha a ID em search_learning_items ou list_my_learning_enrollments. |
| get_my_learning_profile | Obtenha o perfil do aluno, incluindo detalhes da conta e do gerente. Para inscrições e andamento, use list_my_learning_enrollments. |
| answer_learning_content_question | Responda a perguntas sobre conteúdo de aprendizado, fundamentado no material de aprendizado e citado nos objetos de aprendizado de origem. Resuma um objeto de aprendizado ou compare dois lado a lado em termos de cobertura, profundidade, pré-requisitos e público. Para localizar ou listar conteúdo, use search_learning_items ou list_my_learning_enrollments. Exemplo: “Explique o TCP versus o UDP conforme abordado no curso sobre rede.” |
| custom_learning_path | Recomendar cursos que correspondam aos objetivos, tópicos e necessidades de um aluno. Salve um caminho aprovado na conta do aluno. Liste os caminhos salvos ou obtenha os detalhes e os cursos de um caminho por ID. |

>[!IMPORTANT]
>
>Os nomes das ferramentas são mostrados para referência e podem variar dependendo da implementação do cliente.
