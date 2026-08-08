---
description: O prompt é a entrada mais importante no Compositor de conteúdo. Um prompt específico, como nomear o público, 2 a 3 tópicos e um sinal de escopo, produz um resumo mais preciso, um contorno mais forte e menos edição downstream.
jcr-language: en_us
title: Gravar prompts eficazes no Compositor de Conteúdo
source-git-commit: 9890dbe1895ff1b88e2ea946acaf40012980d5c5
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---


# Gravar prompts efetivos

Escreva prompts que produzam resumos precisos do curso, melhores contornos e conteúdo gerado por IA mais forte no Content Composer.

O prompt é a primeira entrada que você fornece ao Compositor de conteúdo e a mais importante. Um prompt claro e específico significa que a IA pré-preenche o resumo com mais precisão, gera um outline que corresponde à sua intenção e produz conteúdo do curso que precisa de menos edição.

## O que faz um prompt funcionar?

O compositor de conteúdo lê o seu prompt e o usa para pré-preencher três campos breves: o título do curso, o perfil do aluno e o objetivo de aprendizado. Quanto mais o seu prompt refletir essas três dimensões, menos correção será necessária para o resumo, e um resumo mais preciso produzirá um contorno mais relevante.

Um prompt que diz “Criar um curso sobre segurança” quase não dá à IA nada para trabalhar. Um prompt que nomeia o público, especifica os tópicos e sinaliza que o escopo fornece à IA o suficiente para gerar um resumo que você pode aceitar com alterações mínimas.

Os campos breves também amplificam o que quer que esteja no comando. Se o comando for vago, a IA gerará um resumo vago. Um resumo vago gera um resumo genérico.

## Estruturar um prompt forte

Um prompt forte responde a três perguntas em uma ou duas frases:

- **Quem** são os alunos? Nomeie sua função e nível de experiência.

- **O que** o curso cobrirá? Nomeie 2-3 tópicos específicos, não uma área ampla de assunto.

- **Que escopo ou resultado** você deseja? Duração do sinal, profundidade ou o que os alunos poderão fazer.

## Anatomia de um prompt efetivo

**[Nível de experiência + público]** + **[2-3 tópicos específicos]** + **[sinal de escopo ou resultado]**

**Exemplo**:

Quero criar um curso para novos representantes de vendas que abranja nossos níveis de preços corporativos, o fluxo de trabalho de aprovação de descontos e como lidar com as três objeções mais comuns dos clientes.

Quebrando isso:

- **Público-alvo:** novos representantes de vendas

- **Tópicos:** camadas de preços corporativos, fluxo de trabalho de aprovação de descontos, três objeções comuns

Depois de selecionar **Começar**, o Compositor de Conteúdo abre a etapa **Resumo**. Revise os campos pré-preenchidos, o título, o perfil do aluno e o objetivo que a IA gerou a partir do seu prompt e refine tudo o que não corresponde à sua intenção antes de gerar a estrutura de tópicos.

## O que fazer e o que não fazer de um aviso eficaz

| **Incluir** | **Evitar** |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Uma função específica do público-alvo (”novos representantes de vendas”, “gerentes de linha de frente”) | Audiências vagas (”toda a equipe”, “todos”, “usuários”) |
| 2-3 áreas temáticas concretas | Mais de 6 tópicos em um prompt - eles produzem contornos sobrecarregados; divida em cursos separados |
| Um sinal de escopo - duração, profundidade ou resultado do aluno | Objetivos genéricos (”ensinar tudo sobre X”, “cobrir todos os aspectos de”) |
| Contexto que molda o tom ou a profundidade (”para conformidade”, “para um público não técnico”, “com base em cenário”) | Fazer perguntas sobre IA. O prompt é breve, não uma conversa |
| O que os alunos poderão fazer após o curso | O que o curso conterá (deixe a estrutura para o estágio de estrutura de tópicos) |

## Prompts iniciais por tipo de curso

| **Tipo de curso** | **Prompt inicial** |
|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Treinamento de conformidade** | “Quero criar um curso de 20 minutos para todos os funcionários sobre o tratamento de dados do GDPR, abrangendo o que conta como dados pessoais, como armazená-los e compartilhá-los corretamente e o que fazer se ocorrer uma violação.” |
| **Integração** | “Desejo criar um módulo de integração para o novo \[função\] que abrange \[tópico 1\], \[tópico 2\] e \[tópico 3\]. |
| **Habilidades técnicas** | “Quero criar um curso para engenheiros de software júnior sobre práticas seguras de codificação, como prevenção de injeção de SQL, validação de entrada e como ler um relatório SAST.” |
| **Habilidades pessoais** | “Quero criar um curso de 30 minutos para os gerentes de varejo da linha de frente sobre como dar um feedback construtivo, como cobrir o modelo da SBI, como se preparar para uma conversa de feedback e como fazer o acompanhamento.” |
| **Política e procedimento** | “Quero criar um curso para a equipe do depósito sobre procedimentos de manuseio manual, como técnica de elevação correta, quando usar equipamentos e como relatar um quase erro.” |
| **Treinamento de produtos** | “Quero criar um curso para agentes de suporte ao cliente sobre nossa política de devoluções, como abordar os critérios de qualificação, como processar uma devolução em \[system\] e como lidar com escalonamentos.” |
| **Habilitação de vendas** | “Quero criar um curso para executivos de contas de nível médio sobre a negociação de negócios corporativos, por exemplo, que aborde como identificar tomadores de decisão, como lidar com objeções de preços usando nossa estrutura de valores e quando escalar para um diretor de vendas.” |
| **Desenvolvimento de liderança** | “Quero criar um curso de 45 minutos para gerentes de pessoas que trabalham pela primeira vez e que abrangem como executar um 1:1 semanal de forma eficaz, como definir uma agenda, dar reconhecimento e lidar com o desempenho insuficiente no início.” |
| **Treinamento em sistemas e ferramentas** | “Quero criar um curso para coordenadores de RH que são novos no Workday, como cobrir como criar uma requisição de cargo, mover um candidato por estágios de contratação e gerar um relatório de efetivo de pessoal.” |
| **Saúde e segurança** | “Quero criar um curso de atualização para todo o pessoal do local sobre procedimentos de segurança contra incêndios, por exemplo, cobrindo a rota de evacuação para cada zona de prédio, como usar um extintor de incêndio e o que fazer se você descobrir um incêndio fora do horário de trabalho.” |

## O que acontece quando um aviso é muito vago?

Se o seu prompt for amplo, a IA gerará um resumo amplo, que gera um outline genérico. O esboço pode cobrir a área do tema certa, mas não possui a estrutura específica de que seu curso precisa. Você passará mais tempo editando o esboço em conversas do que gastaria escrevendo um prompt melhor.

Os sinais mais comuns de que um comando foi muito vago:

- O perfil do aluno do resumo é genérico (”funcionários que desejam aprender sobre X”) em vez de específico a uma função

- O esboço tem títulos de lição que podem ser aplicados a qualquer curso sobre o tópico (”Introdução”, “Conceitos-chave”, “Resumo”)

- O objetivo não nomeia um comportamento mensurável. Em vez disso, descreve o tópico do curso

## Práticas recomendadas

- Escreva o prompt antes de abrir o Compositor de conteúdo. Uma frase redigida com antecedência tende a ser mais clara do que uma digitada sob a pressão do campo de entrada.

- Nomeie o público por função, não por tamanho. “Novos representantes de vendas” é mais útil do que “uma grande equipe de funcionários”.

- Limite o prompt a 2 ou 3 tópicos. Mais tópicos produzem tópicos sobrecarregados. Se o seu assunto exigir mais de três aulas, crie cursos separados.

- Trate o prompt como um ponto de partida. Os campos breves são editáveis. Se a sugestão da IA for fechada, mas não correta, refine o campo diretamente, em vez de reescrever o prompt do zero.
