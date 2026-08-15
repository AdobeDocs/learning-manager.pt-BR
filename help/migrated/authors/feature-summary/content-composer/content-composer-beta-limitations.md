---
description: Analise as limitações do Content Composer beta — edição somente conversacional, questionários MCQ/True-False somente, contornos fixos — com soluções alternativas para cada um.
jcr-language: en_us
title: Limitações do Compositor de conteúdo beta
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---


# Limitações do Adobe Learning Manager Content Composer beta

Uma lista completa das restrições beta atuais do Compositor de conteúdo, com descrições e soluções alternativas quando disponíveis.

## Limitações atuais

A tabela a seguir aborda todas as restrições conhecidas na versão beta atual.

| **Limitação** | **Descrição** | **Solução alternativa** |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **A edição da estrutura de tópicos é apenas conversacional** | Não é possível selecionar uma lição ou tópico na tela para renomear, reordenar ou excluí-lo. Todas as alterações de estrutura de tópicos devem ser feitas por meio do painel de bate-papo do assistente. | Pergunte ao assistente: “Renomeie a lição 2 para “Higiene por senha” ou “Mova o tópico 1.3 para a lição 2”. |
| **A hierarquia da estrutura de tópicos está fixa** | A estrutura do curso é fixada em Lições > Tópicos. Não é possível criar subtópicos, níveis de hierarquia adicionais ou estruturas personalizadas. | Use os componentes disponíveis para adicionar profundidade a um tópico. |
| **A estrutura de tópicos não pode ser editada diretamente após a geração do curso** | Depois que um curso é gerado, os nomes dos tópicos e das lições permanecem como parte da estrutura de tópicos. Você deve retornar às conversas em nível de estrutura de tópicos para alterá-las. Não é possível renomeá-los selecionando um cabeçalho no editor de cursos. | Pergunte ao assistente no editor do curso: “Renomeie a lição 3 para “Resposta a incidente”.” |
| **Tipos de avaliação: somente MCQ e Verdadeiro/Falso** | A versão beta atual oferece suporte apenas a perguntas de múltipla escolha (**MCQ**) e perguntas Verdadeiro/Falso. Outros tipos de avaliação não estão disponíveis. | - |
| **Bancos de perguntas não disponíveis** | Não é possível importar ou gerenciar um banco de perguntas pré-criadas. | Crie perguntas adicionais conversando: “Adicione mais duas perguntas ao questionário da lição 1”. |
| **As verificações de conhecimento não estão graduadas** | As verificações de conhecimento incorporadas nas lições não são graduadas. Somente as avaliações do questionário de fim de aula são classificadas e registradas. | Use questionários (não verificações de conhecimento) para qualquer avaliação que deve produzir um registro de conclusão ou pontuação. |
| **Ações de conversa limitadas a recursos compatíveis** | O assistente pode discutir e fazer brainstorming livremente, mas as modificações reais do curso estão limitadas aos recursos compatíveis com o produto. As solicitações para gerar estruturas ou formatos de conteúdo sem suporte podem não ter êxito. | Se uma solicitação não funcionar, peça ao assistente para explicar o que ele pode fazer em vez disso. |
| **Geração restrita a documentos** | Quando a opção **Restringir saída ao conteúdo dos arquivos** estiver habilitada, o Compositor de Conteúdo gera conteúdo somente a partir dos documentos de origem carregados. Não introduz informações para além dessas fontes. | Desative a opção para permitir que a IA complete com conhecimento geral. |
| **Os recursos de colaboração estão evoluindo** | Compartilhar para revisão e Comentários e Compartilhar para alunos estão em desenvolvimento ativo. Os detalhes da implementação podem mudar antes do lançamento. | Use **Copiar link** para compartilhar um link de visualização para revisão informal. Para coedição, coordene turnos com colaboradores. A coedição simultânea não é compatível. |
| **O assistente no produto não é um sistema de ajuda do produto** | O assistente conversacional é projetado para tarefas de edição de curso, como gerar e modificar conteúdo. As respostas às perguntas sobre o uso do produto podem não ser confiáveis porque esse comportamento ainda não foi explicitamente criado. | Para perguntas de instruções, use a documentação de ajuda existente em vez de perguntar ao assistente no produto. |
