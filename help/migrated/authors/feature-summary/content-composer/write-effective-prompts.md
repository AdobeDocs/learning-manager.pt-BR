---
description: O prompt é a entrada mais importante no Compositor de conteúdo. Um prompt específico, como nomear o público, 2 a 3 tópicos e um sinal de escopo, produz um resumo mais preciso, um contorno mais forte e menos edição downstream.
jcr-language: en_us
title: Gravar prompts eficazes no Compositor de Conteúdo
source-git-commit: c58fff50e6ccf6ab45722a0aafb7f4cee73752b5
workflow-type: tm+mt
source-wordcount: '2339'
ht-degree: 0%

---


# Gravar prompts eficazes no Compositor de Conteúdo

Saiba como escrever prompts eficazes em cada estágio do Compositor de conteúdo, desde o prompt de abertura até o resumo, o esboço e o editor de cursos, para produzir cursos precisos, bem estruturados e gerados por IA com menos edição.

O Compositor de conteúdo é conversacional por toda parte. A qualidade do que ele produz em cada estágio depende da qualidade do que você oferece. Este guia aborda como se comunicar com a IA de maneira eficaz em cada um dos quatro estágios: **Início**, **Resumo**, **Contorno** e **Curso**.

## Estágio 1: Início - escreva seu prompt de abertura

O prompt de abertura é o seu ponto de partida. Não precisa ser perfeito. O Compositor de conteúdo lê seu prompt e o usa para abrir uma conversa. Até mesmo um prompt áspero faz com que o processo se mova; o assistente fará perguntas de acompanhamento no estágio Breve para preencher o que está faltando.

Dito isso, um prompt mais específico significa que a IA pré-preenche o Resumo com mais precisão, reduzindo a oscilação antes de gerar o outline. Se você tiver uma ideia clara do público, dos tópicos e do objetivo, coloque-a no prompt.

Um comando vago produz um resumo vago. Um resumo vago produz um contorno genérico. Um contorno genérico produz um curso que precisa de edição significativa. A especificidade no estágio de solicitação segue adiante em todas as etapas subsequentes.

### O que o Content Composer espera

O compositor de conteúdo espera o seguinte em uma ou duas frases:

- **Quem** são os alunos? Nomeie sua função e nível de experiência.
  - **O que** o curso cobrirá? Descreva 2 a 3 áreas de assunto específicas em vez de um domínio amplo. Por exemplo, “reconhecimento de phishing, higiene de senha e configuração de MFA” é mais útil do que “segurança de TI”.
- **Qual é o objetivo do aprendizado?** Descreva o resultado ou a alteração de comportamento que você deseja que os alunos realizem após concluir o curso.

### Anatomia de um prompt efetivo

**[Nível de audiência + experiência]** + **[2-3 tópicos específicos]** + **[objetivo de aprendizado]**

**Exemplo**:

Quero criar um curso para novos representantes de vendas que abranja nossos tipos de preços corporativos e o fluxo de trabalho de aprovação de desconto. No final, eles devem ser capazes de lidar com as três objeções mais comuns dos clientes de maneira confidencial.

Quebrando isso:

- **Público-alvo:** novos representantes de vendas

- **Tópicos:** camadas de preços corporativos, fluxo de trabalho de aprovação de descontos, três objeções comuns
  - **Objetivo de aprendizado**: lidar com as três objeções mais comuns do cliente de maneira confidencial - um resultado comportamental mensurável, não um tópico a ser abordado

Depois de selecionar **Começar**, o Compositor de Conteúdo abre a etapa **Resumo**. Revise os campos pré-preenchidos, o título, o perfil do aluno e o objetivo que a IA gerou a partir do seu prompt e refine tudo o que não corresponde à sua intenção antes de gerar a estrutura de tópicos.

### O que fazer e o que não fazer de um aviso eficaz

| **Incluir** | **Evitar** |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Uma função específica do público-alvo (”novos representantes de vendas”, “gerentes de linha de frente”) | Audiências vagas (”toda a equipe”, “todos”, “usuários”) |
| 2-3 áreas temáticas concretas | Mais de 6 tópicos em um prompt - eles produzem contornos sobrecarregados; divida em cursos separados |
| Um sinal de escopo - duração, profundidade ou resultado do aluno | Objetivos genéricos (”ensinar tudo sobre X”, “cobrir todos os aspectos de”) |
| Contexto que molda o tom ou a profundidade (”para conformidade”, “para um público não técnico”, “com base em cenário”) | Fazer perguntas sobre IA. O prompt é breve, não uma conversa |
| O que os alunos poderão fazer após o curso | O que o curso conterá (deixe a estrutura para o estágio de estrutura de tópicos) |

### Prompts iniciais por tipo de curso

| **Tipo de curso** | **Prompt inicial** |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Treinamento de conformidade** | “Quero criar um curso para todos os funcionários sobre o tratamento de dados do GDPR, abrangendo o que conta como dados pessoais, como armazená-los e compartilhá-los corretamente e o que fazer se ocorrer uma violação.” |
| **Integração** | “Desejo criar um módulo de integração para o novo \[função\] que abrange \[tópico 1\], \[tópico 2\] e \[tópico 3\]. |
| **Habilidades técnicas** | “Quero criar um curso para engenheiros de software júnior sobre práticas seguras de codificação, como prevenção de injeção de SQL, validação de entrada e como ler um relatório SAST.” |
| **Habilidades pessoais** | “Quero criar um curso para os gerentes de varejo da linha de frente sobre como dar um feedback construtivo, como cobrir o modelo da SBI, como se preparar para uma conversa de feedback e como fazer o acompanhamento.” |
| **Política e procedimento** | “Quero criar um curso para a equipe do depósito sobre procedimentos de manuseio manual, como técnica de elevação correta, quando usar equipamentos e como relatar um quase erro.” |
| **Treinamento de produtos** | “Quero criar um curso para agentes de suporte ao cliente sobre nossa política de devoluções, como abordar os critérios de qualificação, como processar uma devolução em \[system\] e como lidar com escalonamentos.” |
| **Habilitação de vendas** | “Quero criar um curso para executivos de contas de nível médio sobre a negociação de negócios corporativos, por exemplo, que aborde como identificar tomadores de decisão, como lidar com objeções de preços usando nossa estrutura de valores e quando escalar para um diretor de vendas.” |
| **Desenvolvimento de liderança** | “Quero criar um curso para gerentes de pessoas que trabalham pela primeira vez e que abrangem como executar um teste semanal de 1:1 de forma eficaz, como definir uma agenda, dar reconhecimento e lidar com o desempenho insuficiente no início.” |
| **Treinamento em sistemas e ferramentas** | “Quero criar um curso para coordenadores de RH que são novos no Workday, como cobrir como criar uma requisição de cargo, mover um candidato por estágios de contratação e gerar um relatório de efetivo de pessoal.” |
| **Saúde e segurança** | “Quero criar um curso de atualização para todo o pessoal do local sobre procedimentos de segurança contra incêndios, por exemplo, cobrindo a rota de evacuação para cada zona de prédio, como usar um extintor de incêndio e o que fazer se você descobrir um incêndio fora do horário de trabalho.” |

## Estágio 2: resumo - aprimorar as sugestões da IA

Depois de enviar o prompt, o compositor de conteúdo abre o estágio Resumo e preenche três campos: o título do curso, o perfil do aluno e o objetivo de aprendizado. A IA faz perguntas de acompanhamento para ajustar a nitidez de cada campo antes de gerar o contorno.

Este é um estágio de conversação. A qualidade das respostas às perguntas da IA determina diretamente a qualidade do outline que ela produz.

### Título do curso

A IA sugere duas opções de título. Selecione a opção ideal ou digite a sua própria. Se nenhum dos dois estiver certo, descreva a lacuna:

“Nem. O curso é especificamente sobre o fluxo de trabalho de aprovação, não sobre preços gerais.”

Um bom título é voltado para o aluno. Ele descreve o que o aluno poderá fazer, não o que o curso abrange.

### Perfil do aluno

A IA pergunta sobre a função, o nível de experiência e com o que os alunos atualmente enfrentam dificuldades. Seja específico sobre o que eles sabem e o que não sabem:

| Menos útil | Mais útil |
|---|---|
| “Todos os funcionários” | “Desenvolvedores de software no meio da carreira familiarizados com a agile, mas sem experiência em conformidade com a segurança corporativa” |
| “Novo no tópico” | “Gerentes de carreira iniciais promovidos de funções individuais de colaboradores sem treinamento formal de gerenciamento” |
| “Nossa equipe de vendas” | “Novos executivos de conta em seus primeiros 90 dias, familiarizados com as ferramentas de CRM, mas não familiarizados com as estruturas de preços corporativos” |

### Objetivo de aprendizado

A IA pergunta o que os alunos poderão fazer no trabalho após concluírem o curso. Esse é o campo Resumo mais importante. Ele controla quais prioridades da IA nos arquivos de origem, como o esboço está estruturado e o que é testado no questionário.

Escreva o objetivo como um comportamento começando com um verbo de ação:

| Objetivo fraco | Objetivo forte |
|---|---|
| “Compreender a proteção de dados” | “Identifique dados pessoais, aplique práticas corretas de armazenamento e compartilhamento e relate uma suspeita de violação usando o processo de emissão de relatórios da organização” |
| “Saiba mais sobre como lidar com objeções” | “Responda às três objeções mais comuns do cliente usando a estrutura de mensagens aprovada, sem encaminhar a um diretor de vendas” |
| “Conheça o processo de integração” | “Preencha a lista de verificação de integração na primeira semana, envie os formulários de conformidade necessários e acesse as ferramentas necessárias para sua função sem a assistência da TI” |

>[!IMPORTANT]
>
>**Antes de gerar a estrutura de tópicos:** ela é criada inteiramente a partir do Resumo, não do prompt original. Antes de selecionar **Gerar estrutura de tópicos**, confirme se o título é voltado para o aluno, se o perfil do aluno nomeia uma função e um nível de experiência específicos e se o objetivo de aprendizado descreve um comportamento mensurável no trabalho. Um resumo bem definido produz um contorno bem estruturado. Se algum campo ainda parecer genérico, refine-o agora.  Essa opção salva uma edição significativa posteriormente.

### Assina que o resumo precisa de mais trabalho

- O perfil do aluno diz “funcionários que desejam aprender sobre X” em vez de nomear uma função específica e nível de experiência
- O objetivo de aprendizado descreve uma área do assunto em vez de um comportamento mensurável no trabalho
- O título é um rótulo de tópico (”Segurança de TI”) em vez de um resultado voltado para o aluno (”Identificar e responder a tentativas de phishing”)

## Estágio 3: contorno - edite por meio da conversa

Depois de confirmar o Resumo, o Compositor de conteúdo gera uma estrutura de tópicos e lições. Você o revisa e solicita alterações por meio do painel de bate-papo antes de gerar o curso completo.

A edição de contorno é totalmente conversacional na versão atual. Não é possível selecionar uma lição ou tópico na tela para renomeá-lo ou reordená-lo. Todas as alterações são feitas digitando solicitações em linguagem simples.

Esta é também a fase mais eficiente para a realização de mudanças estruturais. A edição do contorno leva segundos. Reestruturar um curso gerado leva significativamente mais tempo.

### Como formatar solicitações de edição de estrutura de tópicos

Seja direto e específico. Nomeie a lição ou o tópico pelo título atual, descreva a alteração desejada e, se desejar, explique o porquê.

**Renomear:**

- “Renomeie a Lição 1 para &#39;Como os Ataques de Phishing Funcionam&#39;.”
- “Renomeie o tópico 2.3 para &#39;Caminhos e linhas do tempo de escalonamento&#39;.”

**Adicionar:**

- “Adicione um novo tópico à Lição 2 sobre phishing com código QR.”
- “Adicione uma lição sobre a resposta a incidentes após a lição 4.”

**Remover:**

- “Remover tópico 1.3.”
- “Exclua a lição 5. Esse conteúdo é abordado em um curso separado.”

**Reordenar:**

- “Transfira a lição 3 para ser a segunda lição.”
- “Mova o tópico 2.1 para o final da lição 2.”

**Divisão:**

- “Divida a lição 3 em duas lições, uma cobrindo filtros de spam e outra cobrindo o gerenciamento de patches.”

**Mesclar:**

- “Combine as Lições 4 e 5 em uma única lição chamada &#39;Resposta e recuperação de incidentes&#39;.”

**Regenerar:**

- “Gere novamente o esboço com um foco mais forte na higiene de senhas e MFA.”
- “Regenerar o esboço — a estrutura atual é muito técnica para um público não-técnico.”

### O que o estágio de estrutura de tópicos não pode fazer

- A hierarquia é definida como Lições > Tópicos. Não é possível criar subtópicos ou estruturas de três níveis.
- Não é possível definir objetivos individuais de lição nesse estágio — o objetivo geral de aprendizado do Resumo aplica-se ao curso completo.
- Não é possível adicionar componentes ou mídia neste estágio. Elas são adicionadas no Editor de curso.

### Quando gerar novamente e quando editar

| Usar edição de conversação quando... | Gerar novamente quando... |
|---|---|
| A estrutura geral está certa, mas os nomes ou tópicos individuais precisam ser ajustados | A estrutura geral não corresponde à sua intenção |
| Você deseja adicionar ou remover itens específicos | O Resumo foi refinado significativamente após a geração do primeiro esboço |
| Uma lição precisa ser dividida ou mesclada | A estrutura parece genérica e não tem o contexto específico da sua organização |

## Etapa 4: curso - refinar conteúdo por meio do assistente

Depois de aprovar a estrutura de tópicos e gerar o curso, o painel **Criar com compositor de conteúdo** permanece aberto no lado direito da tela. Você pode usá-la para refinar, expandir ou ajustar qualquer parte do curso gerado por meio de uma conversa.

O assistente no Editor de cursos é projetado para tarefas de edição de conteúdo. Para perguntas de instruções sobre produtos, use esta documentação de ajuda em vez de perguntar ao assistente.

### Como formatar solicitações de edição de curso

**Reescreva ou ajuste uma seção específica:**

- “Reescreva o parágrafo na segunda seção da Lição 1 para ser mais conciso — procure três frases.”
- “Torne o conteúdo do tópico 2.1 menos técnico. O público não tem experiência em TI.”
- “Adicione um exemplo real à introdução da Lição 1.”

**Ajustar tom:**

- “Reescreva a lição 2 em um tom mais conversacional.”
- “Torne o conteúdo do tópico 3.2 mais confiável — este é um curso de conformidade.”

**Expandir ou adicionar conteúdo:**

- “Adicione um exemplo baseado em cenário ao tópico 1.3 mostrando como um e-mail de phishing pode ser exibido.”
- “Expanda a seção sobre MFA para incluir instruções para configurá-la em dispositivos móveis.”

**Reduza ou simplifique:**

- “Diminua o texto do slide 5 para três pontos de marcador.”
- “Resuma o segundo parágrafo do tópico 2.2 em uma frase.”

**Ajuste o quiz:**

- “Gere novamente o quiz para a Lição 2 com perguntas mais difíceis.”
- “Substitua a pergunta 3 por uma pergunta baseada em cenário sobre como reconhecer uma tentativa de engenharia social.”
- “Adicione mais duas perguntas ao questionário da Lição 1 com foco na configuração de MFA.”

**Ajustar imagens:**

- “Substitua a imagem no tópico 2.2 por algo que mostre um cenário de engenharia social.”
- “Gere uma imagem para o tópico 1.1 que ilustre um e-mail de phishing na tela de um laptop.”

**Adicionar ou modificar componentes:**

- “Adicione um flip card ao tópico 3.1 com as três definições de tipo de preço.”
- “Adicione uma sanfonada ao tópico 2.3 com as etapas de escalonamento — um painel por etapa.”
- “Converta a lista de marcadores no tópico 1.2 em um componente de linha do tempo.”

### O que o assistente do curso não pode fazer

- Renomeie lições ou tópicos diretamente na tela. Use o assistente: “Renomeie a lição 2 para “Higiene da senha”.”
- Crie caminhos ramificados ou adaptativos. A estrutura do curso é linear.
- Adicione novas lições ou reestruture a estrutura de tópicos. As alterações estruturais requerem o retorno ao estágio Estrutura de Tópicos.

## Práticas recomendadas em todas as etapas

- **Descreva o que você deseja compilar antes de abrir o Compositor de Conteúdo.** Uma frase redigida com antecedência tende a ser mais clara do que uma digitada sob a pressão do campo de entrada.
- **Invista tempo no objetivo de aprendizado.** O objetivo no Resumo controla a estrutura de tópicos, a priorização do arquivo de origem e o alinhamento do quiz. Um objetivo específico e focado no comportamento reduz a edição em cada estágio subsequente.
- **Refine o Resumo antes de gerar a estrutura de tópicos.** O contorno é criado a partir do resumo, não do prompt original. Um Resumo bem definido com um perfil e objetivo de aprendizado específicos do aluno produz um resumo estruturado e relevante.
- **Edite a estrutura de tópicos antes de gerar o curso.** As alterações estruturais no estágio de estrutura de tópicos levam segundos. As mesmas mudanças após a geração do curso levam muito mais tempo.
- **Use o assistente de curso para conteúdo, não para estrutura.** As alterações estruturais, a adição de lições, a reorganização de tópicos pertencem ao estágio Estrutura de tópicos. Use o assistente do curso para refinar texto, tom, exemplos e perguntas do quiz.
- **Seja específico em cada solicitação.** Nomeie a lição, o tópico, o slide ou a pergunta que deseja alterar. “Tornar melhor” não oferece à IA nada para se opor. “Torne o tópico 2.1 mais conciso e adicione um exemplo do mundo real”.
