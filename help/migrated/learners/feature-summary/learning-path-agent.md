---
description: O agente do Caminho de aprendizado no Adobe Learning Manager é um assistente viabilizado por IA que gera um plano de aprendizado personalizado e sequenciado com base em suas metas, no plano de fundo e no tempo disponível.
jcr-language: en_us
title: Learning Path Agent (beta) no Adobe Learning Manager
source-git-commit: d61e81b0df6a6043b938c65adaabecb5699c2ce9
workflow-type: tm+mt
source-wordcount: '1956'
ht-degree: 0%

---


# O que é o Learning Path Agent

Um agente do Caminho de aprendizado cria um Caminho de aprendizado estruturado usando o assistente do AI. Diferentemente dos caminhos de aprendizado padrão atribuídos pelo administrador, esses caminhos são gerados por meio de uma conversa guiada. Você descreve sua meta e o agente constrói um caminho correspondente às suas necessidades de aprendizado.

O agente extrai primeiro o conteúdo do catálogo interno de cursos da sua organização, priorizando os cursos aprovados e relevantes para a sua equipe. Se o seu administrador ativou o conteúdo de terceiros, o agente também pode incluir cursos de provedores externos conectados para preencher quaisquer lacunas na cobertura. Você está sempre inscrito automaticamente nos cursos do caminho salvo para começar a aprender imediatamente.

Os Caminhos de aprendizado personalizados foram desenvolvidos para dois casos de uso principais:

- **Desenvolvimento de habilidades direcionado**: quando você precisa alcançar um resultado comercial específico ou atingir uma meta de desempenho rapidamente, como preparar-se para uma nova responsabilidade ou preencher uma lacuna de habilidades identificada em uma revisão.
- **Criando experiência profunda**: quando você deseja avançar de iniciante a especialista em um domínio, tecnologia ou disciplina escolhido em um período mais longo.

## Como funciona a abordagem baseada em conversação

O agente encontra você onde você está. Você começa descrevendo o que deseja aprender em linguagem simples, com o máximo ou mínimo de detalhes possível. O agente então faz perguntas de acompanhamento para entender sua função, seus desafios específicos e quanto tempo você pode dedicar ao aprendizado a cada semana.

A partir de suas respostas, o agente identifica de 3 a 5 tópicos de aprendizado com níveis de proficiência sugeridos. Você pode revisar esses tópicos, solicitar alterações ou confirmá-los antes que o agente procure cursos correspondentes. O agente gera um caminho de aprendizado nomeado mostrando cada curso, sua descrição, duração e contagem do módulo. Você pode ajustar o caminho antes de salvá-lo.

Ao salvar o caminho, você é automaticamente inscrito em todos os cursos. O caminho aparece na sua página inicial, na seção _Caminhos de Aprendizado Personalizados_, pronto para começar.

### Fontes de conteúdo e seleção do curso

O agente seleciona cursos com base na relevância para sua meta declarada, seu nível de proficiência atual, o tempo total disponível e a recente atualização do conteúdo. Quando o agente não consegue encontrar cursos correspondentes para um tópico específico no catálogo disponível, ele informa e sugere entrar em contato com o administrador para solicitar conteúdo adicional para essa área.

### Caminhos de aprendizado personalizados na página inicial

Todos os caminhos de aprendizado personalizados salvos aparecem na faixa _Caminhos de aprendizado personalizados_ na sua página inicial. Cada cartão mostra o nome do caminho, o número de cursos e um botão _Continuar_ para continuar de onde você parou.

### Compartilhando um caminho de aprendizado

Depois de salvar um caminho de aprendizado personalizado, você pode compartilhá-lo com os colegas. O compartilhamento envia a eles um link ou um convite por email. Quando um colega abre um caminho compartilhado, ele pode se inscrever com uma única ação. Compartilhar é útil quando várias pessoas da equipe têm objetivos de aprendizado semelhantes e você deseja que elas sigam o mesmo plano estruturado.

### Práticas recomendadas

- Descreva seu objetivo de aprendizado da maneira mais específica possível ao iniciar a conversa. Quanto mais contexto o agente tiver, mais relevante será o seu caminho.
- Forneça seu compromisso de tempo antecipadamente, para que o caminho gerado se ajuste à sua programação real. O agente entende a linguagem natural: “duas noites por semana” ou “30 minutos por dia” são ambas válidas.
- Revise os tópicos sugeridos antes de pedir ao agente para gerar cursos. Confirmar ou ajustar tópicos nesse estágio economiza tempo em comparação à revisão posterior da lista de cursos.
- Se um tópico não mostrar conteúdo correspondente, anote-o e entre em contato com seu administrador para solicitar que os cursos relevantes sejam adicionados ao catálogo.

## Configurar o agente do Caminho de aprendizado personalizado

O agente Caminho de aprendizado personalizado é ativado por padrão no Adobe Learning Manager quando você ativa a opção Assistente de IA em Configurações.

>[!NOTE]
>
> A visibilidade de conteúdo segue suas regras existentes de acesso ao catálogo. Um aluno verá e receberá apenas os cursos dos catálogos aos quais já tem acesso. O agente do Caminho de aprendizado personalizado não ignora as restrições do catálogo.

Dentro de cada origem, o agente classifica os cursos por relevância para a meta do aluno e o nível do curso corresponde à proficiência declarada do aluno.

Se nenhum curso correspondente estiver disponível para um tópico no catálogo, o agente informará o aluno e sugerirá que ele entre em contato com um administrador para solicitar conteúdo para essa área.

<!-- 
### Monitor credit usage

The Personalized Learning Path agent consumes AI credits each time a learner generates a path. To monitor and manage usage:

1. In the left navigation of the administrator's home page, select **Billing**.
2. Select the **AI Credits** tab. The **Learning Path** agent appears as a line item in the features list.
3. Review current usage and adjust the credit allocation or usage limit as needed.

>[!CAUTION]
>
>If the credit limit for the Learning Path agent is reached, learners receive an in-app message that the agent is unavailable and are directed to contact an administrator. Increase the allocation to restore access. 
-->

## Criar um caminho de aprendizado personalizado com o assistente IA do aluno

Use o assistente de IA do aluno no Adobe Learning Manager para gerar um caminho de aprendizado personalizado que corresponda à sua meta, ao seu plano de fundo e ao tempo disponível. Em seguida, salve-o em seu perfil e comece a aprender imediatamente.

### Abra o assistente IA do aluno e inicie uma conversa

1. Selecione **Assistente de IA** na sua home page.
2. Digite seu objetivo de aprendizado no campo de texto. Seja o mais específico possível. Por exemplo:
   - *Sou um desenvolvedor de software e quero criar um agente de IA usando o cursor.*
   - *Acabei de ser promovido a gerente e quero aprender a lidar com conversas difíceis.*
   - *Desejo dominar a modelagem financeira como analista.*
     ![](assets/ai-assistant.png)

3. Opcionalmente, selecione _+ Novo chat_ para iniciar uma nova conversa se você tiver sessões anteriores abertas.

Observações:

- Opcionalmente, anexe um documento usando o ícone de _clipe de papel_, como um currículo, um email de feedback do gerente ou um resumo do projeto. O agente usa o documento para obter mais contexto sobre seu objetivo de aprendizado e plano de fundo.
- Selecione _Enviar_.

### Descreva sua meta e histórico

O agente responde com uma mensagem confirmando seu objetivo e solicita contexto adicional para personalizar seu caminho. Ele normalmente pergunta sobre:

- _Sua função atual e plano de fundo_ o que você já sabe, há quanto tempo está em sua função ou qualquer experiência relevante.
- _Seus desafios ou cenários específicos_ são as situações reais que você precisa que este aprendizado resolva imediatamente.
- _Seu compromisso de tempo_ é o número de horas por semana que você pode dedicar realisticamente ao aprendizado.

![](assets/goal-background.png)

Você não precisa responder a todas as perguntas. A única entrada necessária é sua meta de aprendizado ou desafio. O agente prosseguirá com qualquer contexto que você fornecer.

>[!TIP]
>
>O agente entende expressões de tempo natural. Você pode dizer “duas noites por semana”, “cerca de 30 minutos por dia” ou “algumas horas nos finais de semana”, e o agente converte para horas semanais para estimar e confirmar isso com você.

Digite sua resposta e selecione _Enviar_.

![](assets/time-commitment.png)

Continue a conversa até que o agente apresente os tópicos sugeridos.

![](assets/suggested-topics.png)

### Revisar os tópicos sugeridos

Depois de reunir contexto suficiente, o agente apresenta uma lista de 3 a 5 tópicos de aprendizado, cada um com um título, uma breve descrição e um nível de proficiência sugerido.

1. Leia a lista de tópicos com atenção. O agente seleciona níveis de proficiência com base no que você compartilhou, mas é possível solicitar alterações.
2. Para ajustar um tópico, por exemplo, para alterar o nível de proficiência ou trocar um tópico, digite seu feedback no bate-papo. Por exemplo, eu já tenho algum conhecimento do primeiro tópico. Você pode definir esse como intermediário?
3. Se você estiver satisfeito com os tópicos, confirme-os respondendo no chat ou selecionando o prompt de confirmação sugerido, se aparecer.

### Revisar o caminho de aprendizado

O agente pesquisa o catálogo disponível e cria um caminho de aprendizado nomeado. O caminho mostra:

- O nome do caminho e a duração total estimada
- Cada título, descrição, duração e contagem de módulos do curso
- Uma indicação de que alguns tópicos não tinham conteúdo correspondente disponível

Se alguns tópicos não tiverem conteúdo correspondente:

O agente informa que não encontrou cursos para esses tópicos específicos e sugere entrar em contato com o administrador para solicitar conteúdo para essas áreas. O caminho ainda é gerado para os tópicos onde os cursos foram encontrados.

<!-- - Review the path. If you want to change something, for example, remove a course, adjust the scope, or explore different topics. Type your request in the chat\. For example, Can you remove the first course and replace it with something shorter? -->
Quando estiver satisfeito com o caminho, peça ao agente para salvá-lo digitando salvar o caminho de aprendizado.

![](assets/create-lp.png)

### Salvar e acessar o seu Caminho de Aprendizado

Quando você salva o caminho, o agente confirma o salvamento e inscreve você automaticamente em todos os cursos no caminho.

Para acessar seu caminho:

- Selecione _Ir para o Caminho de Aprendizado_ na mensagem de confirmação para abri-lo imediatamente ou
- Encontre-o na faixa _Caminhos de aprendizado personalizados_ em sua página inicial a qualquer momento.

### Compartilhar seu caminho de aprendizado

Na página de visão geral do caminho, você pode compartilhar o caminho salvo com colegas.

1. Abra o caminho salvo na faixa _Caminhos de Aprendizado Personalizados_ em sua página inicial.
2. Selecione _Compartilhar_.
3. Compartilhe o link gerado ou insira os endereços de email para enviar um convite direto.

Um colega que recebe o link compartilhado pode se inscrever no caminho com uma única ação.

## Práticas recomendadas

- Forneça contexto sobre sua função e os desafios atuais. Quanto mais específico você for, mais relevante será a seleção do curso.
- Mencione seu compromisso de tempo semanal em linguagem natural. O agente confirmará sua interpretação antes de gerar o caminho.
- Revise os tópicos sugeridos antes de pedir a geração do caminho. Ajustar tópicos nesse estágio é mais rápido do que revisar a lista de cursos posteriormente.
- Se o caminho gerado incluir cursos que você já concluiu, avise o agente. Ela pode sugerir alternativas.

## Perguntas frequentes

_Onde encontro meus caminhos de aprendizado personalizados salvos?_

Todos os seus caminhos salvos aparecerão na faixa _Caminhos de Aprendizado Personalizados_ em sua página inicial. Cada cartão mostra o nome do caminho e um botão _Continuar_. Você também pode abrir qualquer caminho a partir daí para ver a lista completa do curso e seu progresso.

_Quantos caminhos de aprendizado personalizados posso salvar?_

A faixa _Caminhos de Aprendizado Personalizados_ na sua página inicial mostra um máximo de 10 caminhos.

_Quais informações devo fornecer para obter um Caminho de Aprendizado relevante?_

Descreva, no mínimo, sua meta de aprendizado ou o desafio específico que você está tentando enfrentar. Quanto mais contexto você fornecer, melhor o caminho. As informações úteis incluem sua função atual, há quanto tempo você está fazendo isso, qualquer experiência anterior relevante e quantas horas por semana você pode dedicar realisticamente à aprendizagem.

_O que acontece se o agente não conseguir encontrar cursos correspondentes para meus tópicos?_

O agente informa diretamente na conversa que não encontrou cursos correspondentes para um ou mais de seus tópicos. Isso gera o caminho usando apenas os tópicos onde os cursos estavam disponíveis.

Se o agente não conseguir encontrar cursos para nenhum dos seus tópicos, ele informará que não consegue criar um caminho para essa meta. Em ambos os casos, entre em contato com o administrador de aprendizado e informe quais tópicos não tinham conteúdo disponível. Eles podem adicionar cursos relevantes ao catálogo para que solicitações futuras de caminho sejam cobertas.

<!-- 
_How does the agent decide which courses to include?_

The agent prioritizes your organization's internal course catalog above external sources. It selects courses based on relevance to your stated goal, whether the course level matches your proficiency, how recently the content was published or updated, and quality signals such as ratings and completion rates\. Your administrator controls which content sources are available. 
-->

_Posso ajustar os tópicos no meu caminho de aprendizado?_

Sim Durante a conversa, você pode pedir ao agente para adicionar, remover ou alterar tópicos antes que o caminho seja gerado. O agente atualizará a lista de tópicos e regenerará o caminho para corresponder.

_Posso alterar os cursos individuais em um caminho gerado?_

Não. Depois que o agente gera um caminho, a seleção do curso é corrigida. Não é possível trocar, remover ou substituir cursos individuais. O que o agente recomenda é o caminho.

Se os cursos sugeridos não parecem corretos, a melhor abordagem é voltar e ajustar os tópicos antes de gerar. O agente seleciona cursos com base nos tópicos que você confirma, portanto, alterar o escopo do tópico ou o nível de proficiência produzirá um conjunto de cursos diferente.

_Por que o agente continua fazendo perguntas de acompanhamento?_

O agente precisa de clareza suficiente sobre sua meta de aprendizado para identificar tópicos relevantes. Se sua mensagem inicial era ampla, como “Eu quero aprender marketing”, ela fará perguntas para restringir o escopo. Fornecer detalhes mais específicos sobre sua função, os desafios enfrentados e o que você deseja fazer após o aprendizado ajudará o agente a passar para a geração de tópicos mais rapidamente.