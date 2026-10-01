---
description: Saiba como criar, configurar e publicar uma representação de coach virtual, desde a configuração pessoal e de tópicos até as configurações de pontuação e avançadas
jcr-language: en_us
title: Criar e publicar uma interpretação de funções de treinador virtual
exl-id: f37e93ef-6d76-4b7c-b4c3-f3f8c57b143c
source-git-commit: 449f25df93867bf4d5ec11af057f8da7c405a09f
workflow-type: tm+mt
source-wordcount: '4850'
ht-degree: 0%
---

# Criar e publicar uma interpretação de funções de treinador virtual

Crie um cenário de roleplay de IA no Adobe Learning Manager Virtual Coach para que os alunos possam praticar conversas do mundo real como parte de um curso ou ajuda de tarefa. Este artigo aborda todo o processo de criação de uma interpretação de papéis de treinador virtual, desde a escolha de um modelo até a publicação e a biblioteca de conteúdo.

Antes de começar, confirme se o Adobe Learning Manager Virtual Coach está ativado em sua conta e se você está conectado como autor. O Virtual Coach cria todas as funções a partir dos materiais e detalhes de solicitação fornecidos, sem incluir automaticamente o conteúdo do curso existente em sua organização. Se ainda não o fez, [reúna materiais para uma atuação de treinador virtual](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) antes de começar.

Para criar um cenário de execução de IA no Virtual Coach:
1. No painel de navegação esquerdo, selecione **Virtual Coach** e selecione **Criar agora**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach1.png)

2. Na seção **Em destaque**, escolha um modelo **individual** ou **multipessoal**. Neste exemplo, estamos assumindo que esta interpretação é baseada em uma única pessoa. Para etapas que envolvem várias pessoas, consulte [interpretação de funções de várias pessoas](#configure-a-multi-persona-role-play)

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach2.png)

   A janela **Criar Role-Play** é aberta.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach14.png)

3. Ou faça upload do material de origem e selecione **Cocriar com IA**.
4. Configurar os tópicos de persona, abertura da conversa e avaliação.
5. Selecione **Editar** na seção **Tópicos a abordar**. Defina os pesos de pontuação e quaisquer tópicos de **Criar ou Interromper**.
6. Cada uma das seções pode ser editada dessa maneira.
7. Se você estiver satisfeito com o conteúdo, selecione **Aprovar conteúdo e continuar**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach16.png)

8. Visualize a reprodução de função e depois o **Publish**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach17.png)

## Abra o Virtual Coach e inicie um role-play

Há duas maneiras de criar uma representação de treinador virtual: comece com um modelo ou crie uma do zero com o assistente de cocriação do AI. Esta seção aborda a criação do zero.

1. Faça logon no Adobe Learning Manager como autor.
2. Selecione **Virtual Coach** no painel de navegação à esquerda.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach1.png)
   *Selecione Virtual Coach em Criar, no painel de navegação à esquerda, para começar a criar um role-play.*

3. Na página **Treinador virtual**, selecione **Criar agora**.
4. Selecione um modelo na seção **Em destaque** ou na seção **Modelos disponíveis**. Os modelos em destaque incluem duas opções para criar do zero:
   - **Reprodução de função de uma pessoa (Assistente de IA)**: o aluno interage com uma pessoa de IA. Use isso para uma conversa com o cliente, uma discussão sobre liderança, uma chamada de detecção ou uma conversa de orientação.
   - **Reprodução de função de várias pessoas (beta)**: o aluno interage com até quatro pessoas de IA na mesma conversa. Use isso para uma análise do comitê executivo, um painel de compras, finanças e jurídico ou para uma negociação com o cliente envolvendo várias partes interessadas — por exemplo, um cenário de prontidão para lançamento do produto em que um representante deve apresentar uma nova oferta a um CFO, um gerente de compras, um Director de TI e um especialista em usuários finais em uma sessão.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach2.png)
   *Escolha Single-Persona Role-Play ou Multi-Persona Role-Play na seção Em destaque para criar um cenário do zero ou selecione um modelo pré-criado abaixo.*

   Para este exemplo, selecione **Reprodução de função de uma única pessoa (Assistente de IA)** na seção **Recursos**. Para começar com um cenário pronto, consulte [criar uma função usando um modelo de Treinador Virtual](/help/migrated/authors/feature-summary/virtual-coach/create-role-play-using-virtual-coach-template.md).
5. Opcionalmente, selecione **Carregar arquivos** para adicionar documentos de suporte, como uma folha de dados de produto, playbook ou gravação de chamadas. O Assistente de cocriação de IA os usa para criar um cenário mais preciso. Pule esta etapa se não tiver arquivos relevantes.
6. Selecione **Cocriar com IA**. Quando a mensagem de confirmação aparecer, selecione **Gerar**.
7. Insira uma descrição para sua interpretação. Use uma descrição que contorne o cenário, como `Handling price objections in enterprise sales` ou `Pitching our new product to a buying committee`.
8. Continue a conversa com o assistente de IA, adicionando mais contexto sobre o cenário. O assistente explica que uma função tem três componentes principais: **Visão geral** (título e contexto de conversa), **personalidade de IA** (nome, organização, função, plano de fundo, preocupações etc.) e **Tópicos de avaliação** (os critérios usados para pontuar os alunos). O assistente pergunta se você deseja criar esses tópicos passo a passo ou gerá-los todos de uma vez.
9. Continue adicionando informações ou selecione **Aprovar conteúdo e continuar** quando estiver satisfeito.

## Definir configurações de interpretação de papéis

Depois de criar uma reprodução de função de treinador virtual usando o assistente de cocriação de IA, a tela **Editar reprodução de função** é aberta. Seu progresso é salvo automaticamente, como mostra o indicador **Salvo** no canto superior direito. Você pode sair e voltar a esta tela a qualquer momento sem perder o trabalho.

Nessa tela, há três opções:

- **Visualizar** executa uma sessão de teste ao vivo para que você possa experimentar a representação como aluno antes que qualquer outra pessoa o faça. Use isso para verificar se a persona soa natural e os tópicos fluem corretamente.
- **Salvar** salva o estado atual sem publicar. A função é adicionada à seção **Modelos Disponíveis** da sua biblioteca de Instruções Virtuais, onde você pode voltar para editá-la mais tarde.
- O **Publish** adiciona a função à **Biblioteca de Conteúdo** para que ela possa ser atribuída a um curso ou ajuda de tarefa.

Para fazer alterações no conteúdo gerado sem editar campos manualmente, selecione **Editar com IA** à direita. Isso abre a interface de bate-papo do AI e permite descrever as alterações desejadas em linguagem simples, por exemplo, `make the persona more formal` ou `add a topic about pricing objections`.

>[!NOTE]
>
>Isso é diferente da edição em toda a seção. A opção de edição em toda a seção oferece acesso a todas as seções ao mesmo tempo. A interface de bate-papo por IA, por outro lado, oferece a opção de descrever livremente exatamente o que deseja alterar.

Selecione **Editar** ao lado do **título de reprodução de função** para alterar o título.

## Personalize sua simulação de Virtual Coach

Defina o contexto da conversa, o histórico da pessoa e as preocupações da pessoa para tornar seu cenário de interpretação de papéis realista e desafiador. Quanto mais detalhes você fornecer em cada campo, mais precisa e consistente será o comportamento da pessoa da IA durante a simulação.

Se você usou a **Cocriação com IA** ou a **Geração automática de reprodução de função**, esses campos serão pré-preenchidos com base nas suas entradas. Revise e refine-os antes de publicar.

### Contexto da conversa

O campo **Contexto da Conversa** define o estágio para o aluno. Ele informa à persona de IA o fundo e o propósito da interpretação, para que a pessoa entenda por que a conversa está acontecendo e qual deve ser o foco principal.

>[!NOTE]
>
>Esse campo foi escrito para a persona de IA, não para o aluno. Não inclua instruções ou diretrizes destinadas ao aluno aqui. Use o campo **Abridor de instrutores de IA**, descrito posteriormente neste artigo, para o contexto voltado para o aluno.

Ao gravar o contexto da conversa:

- **Explique a situação.** Descreva que tipo de conversa é esta, como uma chamada de descoberta de vendas, uma chamada fria ou uma proposta de elevador, e quem a iniciou.
- **Descreva a posição da personalidade de IA.** Explique quem é a pessoa em relação ao aluno. Por exemplo, um cliente avaliando um produto, um CFO revisando uma proposta de orçamento ou um funcionário recebendo feedback.
- **Use “o aluno” de maneira consistente.** Ao se referir à pessoa com quem a pessoa está falando, sempre escreva “o aluno”. Evite rótulos como “o agente”, “o vendedor” ou “o representante”, que podem causar comportamento inconsistente da pessoa.
- **Manter conciso.** Inclua apenas informações relevantes para a configuração da conversa. Salve detalhes específicos da pessoa para **Informações Pessoais de Fundo**.

**Exemplo:** “Esta é uma chamada de descoberta de vendas. O aluno entrou em contato para agendar uma ligação introdutória com Karen Mitchell, a Director de Assuntos Médicos de uma rede de hospitais de médio porte. Karen concordou com uma ligação de 15 minutos para saber mais sobre a plataforma de aprendizado. Ela tem pouco tempo e está avaliando se a plataforma atende aos padrões de qualidade do conteúdo clínico antes de envolver sua equipe.”

### Informações pessoais

O campo **Informações pessoais de fundo** dá personalidade à pessoa de IA. Quanto mais detalhes você inserir, mais precisas e consistentes serão as respostas da pessoa durante toda a simulação.

Incluir:

- **Detalhes básicos**: o nome, a idade, a função e a situação atual da pessoa, pois estão relacionados ao tópico e ao objetivo da interpretação de funções.
- **Motivações e objetivos**: o que a pessoa se importa, quer alcançar ou quer mudar e seus pontos problemáticos.
- **Crenças e atitudes**: como a pessoa se sente sobre o tópico da conversa e sobre a organização do aluno.
- **Comportamentos e hábitos**: tendências que moldam a Perspectiva da pessoa, como a tomada de decisões cautelosa ou a ânsia de adotar novas ferramentas.
- **Critérios de decisão**: o que convence a pessoa a seguir em frente e quaisquer restrições nas quais ela esteja trabalhando, como tempo, orçamento ou processos de aprovação.

>[!TIP]
>
>Detalhes específicos ajudam a pessoa a responder de forma natural e crível. Fundos genéricos produzem comportamento genérico.

### Preocupações pessoais

**Preocupações pessoais** define as questões específicas, preocupações ou perguntas que a pessoa levanta durante a conversa. Essas preocupações impulsionam o fluxo da interpretação e garantem que o aluno responda a desafios realistas.

- **Liste de três a cinco preocupações.** Expresse cada um como uma preocupação ou pergunta e torne-o específico e acionável. Evite preocupações vagas, como “preocupação com o custo”; escreva “preocupação de que o custo anual da licença exceda o orçamento discricionário do departamento sem a aprovação do CFO”.
- **Concentre cada preocupação em um único tópico.** Uma preocupação por problema mantém a conversa gerenciável e garante que cada desafio seja claramente avaliado.
- **Especifique quando a preocupação surgir.** Indique o ponto na conversa quando a pessoa criá-lo.
- **Defina o que é bom o suficiente para continuar.** Descreva o que deixaria a conversa avançar. Por exemplo, o aluno tranquiliza a pessoa, fornece uma referência ou oferece documentação.

Escreva cada preocupação usando esta estrutura: **preocupação → quando ela surgir → o que é bom o suficiente para avançar.**

**Exemplo:** “Preocupação — precisão do conteúdo clínico: aparece quando o aluno descreve o processo de criação de conteúdo. Bom o suficiente: o aluno afirma explicitamente que o conteúdo é de autoria de profissionais médicos, revisado por pares e vinculado à literatura primária ou a diretrizes clínicas reconhecidas.”

Depois de preencher as informações relevantes, selecione **Salvar**.

>[!TIP]
>
>Testar o tempo da preocupação com **Visualização**. Uma preocupação que pareça muito cedo ou muito tarde interrompe o fluxo da conversa.

>[!NOTE]
>
>As alterações nas configurações personalizadas entrarão em vigor imediatamente para qualquer interpretação de função não publicada. Se você editar uma ação já publicada e atribuída aos alunos, republique-a para aplicar a personalidade atualizada às sessões futuras.

## Configurar uma apresentação para sua simulação

Use a seção **Configurações de Apresentação** para anexar um conjunto de slides à sua simulação de interpretação de função. Quando uma apresentação é anexada, os alunos podem visualizá-la durante a sessão como uma referência ou auxílio para fala. Por exemplo, uma apresentação da visão geral do produto usada durante uma simulação de apresentação de vendas.

1. Selecione **Carregar PDF ou PPTX** em **Detalhes da Apresentação**.
2. Selecione seu arquivo. Os formatos PDF e PPTX são compatíveis, com um tamanho máximo de arquivo de 100 MB.
3. Após o upload, o nome do arquivo aparece abaixo do botão, confirmando o anexo.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach3.png)
   *Anexe uma apresentação para que os alunos possam referenciá-la como um auxílio para fala durante a simulação.*

4. Selecione **Concluído** para salvar a configuração e retornar à configuração de reprodução de função.

Depois de carregar uma apresentação, a opção **Permitir que os alunos carreguem sua própria apresentação** é ativada automaticamente. Você também pode baixar ou excluir o arquivo anexado usando os botões à direita.

Selecione **Permitir que os alunos carreguem sua própria apresentação** se quiser que cada aluno pratique com sua própria versão de uma plataforma, em vez de uma versão compartilhada. Isso é útil quando os alunos são avaliados em uma apresentação que eles prepararam pessoalmente, como uma revisão de negócios ou uma proposta de vendas personalizada. Essa alternância é desativada por padrão; quando ativada, os alunos veem um prompt de upload no início da sessão.

>[!NOTE]
>
>Certifique-se de que qualquer apresentação que você enviar esteja acessível. Use contraste de cores suficiente, inclua texto alternativo para imagens e evite conteúdos que dependam apenas da cor para transmitir significado.

## Configurar a persona de IA

A seção **Configuração do AI Persona** controla com quem o aluno fala durante a simulação, juntamente com sua aparência, voz, função e personalidade comportamental. Acertar esta seção é uma das partes mais importantes de como você cria um cenário de reprodução de ações de IA, uma vez que uma persona bem configurada de avatar de IA faz com que a reprodução de ações se sinta realista e garante que a IA se comporte de forma consistente com o cenário que você criou.

### Escolher uma pessoa

Duas guias estão disponíveis: **Pessoas do Sistema** e **Pessoas Personalizadas**.

**Pessoas do sistema** são caracteres pré-compilados fornecidos pelo Adobe. Cada um tem um nome, uma foto e um ou dois modos de interação compatíveis: **Voz e Vídeo** (a persona aparece como um avatar animado com uma voz falada) ou **Voz** (somente voz falada, sem avatar de vídeo). Selecione uma persona do sistema selecionando seu bloco.

**Pessoas personalizadas** são pessoas que você criou anteriormente. Selecione esta guia para reutilizar uma persona de avatar de IA de uma interpretação anterior em vez de criar uma do zero.

![](/help/migrated/authors/feature-summary/assets/virtual_coach4.png)
*Reutilize uma persona personalizada de uma interpretação anterior em vez de criar uma nova do zero.*

Você pode reutilizar uma pessoa de duas maneiras: edite seus detalhes diretamente para transformá-la em uma pessoa diferente ou selecione **Duplicar** para criar uma cópia e alterar os detalhes da cópia. Para ver ambas as opções, selecione o ícone de reticências verticais (**&#x200B;**) que aparece no canto superior direito da imagem de uma pessoa quando você passa o mouse sobre ela ou a seleciona.

### Configurar detalhes e personalidade pessoais

Depois de selecionar uma pessoa, preencha os **campos de Detalhes da Pessoa no AI**:

1. Insira a **Função** da pessoa, o título do cargo que ela deve aparecer na simulação, por exemplo, Director de Assuntos Médicos.
2. Insira a **Organização** da pessoa — a empresa ou instituição para a qual ela trabalha. Por exemplo, Northgate Health.
3. Selecione uma **Personalidade** que corresponda ao nível de desafio e ao contexto do cenário:

   | Personalidade | Comportamento |
   |---|---|
   | Cético | Questiona tudo e exige prova |
   | Indiferente | Desengatada e difícil de excitar |
   | Entusiasta | Empolgado com a solução e pronto para participar |
   | Orientado a Relacionamento | Valores de confiança e conexão pessoal acima de tudo |
   | Neutro | Permanece equilibrado e avalia as opções sem viés |
   | Assertivo | Diminuição, ritmo acelerado e tendência a desafiar os outros |

4. Opcionalmente, habilite **Permitir que os alunos selecionem esta opção antes que a reprodução de funções comece** para permitir que os alunos escolham a personalidade da pessoa antes de iniciar a sessão. Isso é útil para cenários de modo de prática em que os alunos desejam controlar a dificuldade.
5. Selecione **Concluído** para salvar a configuração pessoal.

>[!TIP]
>
>Combine a personalidade com o desafio do cenário. Um cenário de cold call se beneficia de uma personalidade **Cética** ou **Indiferente** para simular um cliente potencial difícil. Um cenário de feedback de liderança funciona bem com o **Assertivo** ou o **Orientado ao Relacionamento** para refletir a dinâmica realista de gerente-funcionário.

### Criar uma persona personalizada

Se as pessoas do sistema não se encaixarem no seu cenário, crie uma nova na guia **Pessoas Personalizadas**.

1. Selecione **Pessoas Personalizadas** e selecione **Criar Nova Pessoa**.
2. Carregue uma foto para a persona. A imagem deve ter no mínimo 640 x 360 pixels e no máximo 1 MB.
3. Insira o **Nome** da pessoa.
4. Selecione uma **Voz** no menu suspenso para definir a voz de fala da IA.
5. Ajuste o controle deslizante de **Taxa de voz** para controlar a velocidade de fala, de -100 (a mais lenta) a +100 (a mais rápida). O padrão é 0 (espaço neutro). Selecione **Testar Voz** para visualizar como a voz soa antes de salvar.
6. Selecione **Criar persona**. A nova persona será salva na guia **Personas Personalizadas** e estará disponível para uso em qualquer role-play futuro.

>[!NOTE]
>
>Personagens personalizadas dão suporte à interação de voz. Confirme se a taxa de voz soa natural para o cenário antes de publicar. Uma taxa muito rápida ou muito lenta pode fazer com que a simulação não pareça natural e afetar a pontuação do ritmo do aluno.

Habilitar o **Avatar de vídeo** adiciona um avatar de vídeo AI fotorrealista à reprodução de função. Os avatares de vídeo estão disponíveis para pessoas que oferecem suporte ao modo de **Voz e Vídeo**. Cada aluno recebe 300 minutos de role-play de vídeo por mês; uma vez que esse limite é atingido, a experiência muda para um avatar estático.

### Configurar uma interpretação de funções multipessoal

Use uma ação de função multipessoal quando o aluno precisar navegar por uma conversa que envolva mais de um colaborador na mesma sessão. Por exemplo, a apresentação de um novo produto para um comitê de compra formado por um CFO, um gerente de compras, um Director de TI e um campeão para o usuário final. As funções multipessoais oferecem suporte a **até quatro pessoas** em um único cenário.

1. Selecione **Reprodução de função de várias pessoas** como seu modelo quando você iniciar a reprodução de função.
2. Adicione cada pessoa e atribua a ela uma função distinta. Por exemplo, CFO, Procurement Manager, IT Director e Champion.
3. Configure uma personalidade separada para cada pessoa, seguindo as mesmas **etapas dos Detalhes da personalidade de IA** descritas acima.
4. Defina preocupações exclusivas para cada pessoa, usando a mesma estrutura de preocupação descrita em **Preocupações pessoais** Cada pessoa faz perguntas e levanta objeções a partir de sua própria Perspectiva, de modo que o aluno tem que adaptar sua mensagem para cada parte interessada em vez de dar uma proposta genérica.

## Configurar a abertura da conversa

A seção **Abertura da conversa** controla as duas primeiras coisas que um aluno ouve quando uma simulação é iniciada: uma breve instrução de contexto do instrutor de IA, seguida da linha de abertura da pessoa de IA.

![](/help/migrated/authors/feature-summary/assets/virtual_coach5.png)
*O instrutor de IA define o palco primeiro e, em seguida, a pessoa de IA abre a conversa no personagem.*

O **Abridor de Instrutores de IA** é uma mensagem curta dita pelo instrutor, não pela pessoa, antes do início da conversa. Ela informa ao aluno com quem ele está prestes a falar, qual é o objetivo e o contexto relevante no qual ele precisa entrar. Selecione **Editar** para atualizar o texto. Seja breve e direto. Para cenários mais exigentes, inclua o objetivo explicitamente, por exemplo: “Você está prestes a fazer uma cold call para um lead de aquisição sênior. Seu objetivo é garantir uma reunião de acompanhamento.”

O **Abridor de Persona de IA** é a primeira linha que a persona de IA entrega ao aluno, iniciando a conversa. Ela deve refletir a personalidade da pessoa e colocar o aluno no local desde a primeira troca. Selecione **Editar** para atualizar o texto.

| Cenário | Exemplo de abridor |
|---|---|
| Chamada fria | “Alô? Quem é?” |
| Chamada de descoberta agendada | “Olá, obrigado por entrar em contato. O que você queria abordar hoje?” |
| Conversa com feedback | “Você tem um minuto? Eu queria falar sobre a semana passada.” |
| Apresentação executiva | “Eu só tenho dez minutos. O que você tem para mim?” |

Selecione **Visualizar** para ouvir os dois abridores reproduzidos em sequência, exatamente como o aluno os experimentará no início de uma sessão.

>[!TIP]
>
>Se o abridor de instrutores de IA e o abridor de personalidade de IA tiverem um tom muito semelhante, a transição entre eles pode ser confusa. Mantenha o abridor de instrutores neutro e instrutivo; deixe que o abridor de persona carregue a personalidade.

## Configurar tópicos e critérios de avaliação

A seção **Tópicos a serem abordados** define o que o aluno deve abordar durante a simulação e como a IA avalia seu desempenho em cada tópico; essa é sua rubrica de pontuação no roleplay de IA. Cada tópico adicionado torna-se um componente pontuado no relatório de conhecimento do aluno.

**Antes de começar:** primeiro, conclua a seção **Personalizar sua simulação**. A IA usa o contexto da conversa e o plano de fundo pessoal para gerar diretrizes de avaliação precisas para cada tópico.

Cada linha na tabela de tópicos representa uma área de conversa obrigatória:

| Coluna | Finalidade |
|---|---|
| Tópico | O nome da área de conversa que o aluno deve cobrir |
| Diretrizes de avaliação | Os critérios usados pela IA para avaliar se o tópico foi abordado adequadamente; essas diretrizes também aparecem como feedback na página de análise do aluno |
| Espessura | A porcentagem de pontuação do conhecimento com a qual este tópico contribui; todos os pesos de tópico devem totalizar 100% |
| Vídeo de exemplo | Um vídeo opcional que o aluno pode assistir na página de análise para ver como o tópico deve ser tratado |
| Link útil | Um URL opcional mostrado na página de análise do aluno ao lado dos critérios de avaliação |
| Criar ou Interromper | Quando ativada, se o aluno não abordar este tópico, a pontuação final da simulação é 0, independentemente do desempenho em outros tópicos |

![](/help/migrated/authors/feature-summary/assets/virtual_coach6.png)
*Cada linha de tópico define o que avaliar, quanto vale e se é necessário passar.*

### Adicionar um tópico

1. Selecione **Editar** na seção **Tópicos a serem abordados** para abrir a tabela de tópicos.
2. Selecione **Adicionar tópico**. Uma nova linha aparece com campos vazios.
3. Insira o nome do tópico no campo **Tópico**. Use um rótulo curto e descritivo que reflita a área de conversa, por exemplo, `Opening and Rapport`, `Handling Objections` ou `Agreeing Next Steps`.
4. Insira as diretrizes de avaliação no campo **Diretrizes de avaliação**. Escreva-os como uma declaração de conclusão começando com “Para abordar esse tópico com sucesso, o aluno precisa...”
5. Insira uma porcentagem no campo **Peso**. Distribua pesos em todos os tópicos para que o total seja igual a 100%.
6. Opcionalmente, selecione **Clique para adicionar vídeo** para anexar um vídeo de exemplo ou **Clique para adicionar URL** para anexar um link útil, como um artigo da base de dados de conhecimento ou um produto de página única.
7. Opcionalmente, habilite **Criar ou Interromper** para tópicos não negociáveis.
8. Repita para cada tópico que deseja incluir e selecione **Concluído**.

### Editar ou remover um tópico

- Para editar qualquer campo em uma linha de tópico existente, selecione o campo diretamente e atualize o texto ou o valor.
- Para regenerar as diretrizes de avaliação usando IA com base na sua personalidade e contexto, selecione o ícone de atualização (**↻**) na célula **Diretrizes de avaliação**.
- Para remover um tópico, selecione o menu de opções (**&#x200B;**) no final da linha e selecione **Excluir tópico**.
- Para duplicar um tópico e usá-lo como base para outro semelhante, selecione **Duplicar tópico** no mesmo menu.

### Diretrizes para escrever tópicos eficazes

Uma forte rubrica de pontuação do RPG de IA faz a diferença entre uma interpretação que parece justa e uma que parece arbitrária. Lembre-se destas diretrizes:

- **Nomeie tópicos após os estágios de conversa, não recursos do produto.** Tópicos como `Opening and Rapport`, `Needs Discovery` e `Agreeing Next Steps` refletem a estrutura de uma conversa real.
- **Escrever diretrizes de avaliação como ações observáveis.** A IA avalia o que o aluno disse, portanto, as diretrizes devem descrever comportamentos específicos, audíveis e não intenções. Compare “o aluno deve entender as preocupações da pessoa” (fracas) com “o aluno precisa pedir à pessoa para nomear sua preocupação principal e confirmar que a ouviu antes de responder” (fortes).
- **Use Criar ou Quebrar com moderação.** Reserve-o para um ou dois tópicos em que a omissão total tornaria a conversa um fracasso claro, como falhar em se apresentar em uma “cold call”. Aplicá-lo a muitos tópicos dificulta a aprovação dos alunos até mesmo em uma tentativa razoável.
- **Equilibre os pesos para refletir a importância da conversa.** Um tópico que ocupa a maior parte de uma conversa típica, como a descoberta de necessidades em uma chamada de vendas, deve ter um peso maior do que um breve início ou encerramento.
- **Adicione links úteis a tópicos de baixa pontuação.** Se os alunos obtiverem pontuações baixas consistentemente em um tópico específico nas sessões, anexe um link de recurso para que eles tenham algo para estudar entre as tentativas.

## Definir configurações de idioma

A seção **Configurações de idioma** controla se os alunos podem escolher o idioma em que praticam ao iniciar a simulação. Habilite **Permitir que os alunos escolham seu idioma de prática** para permitir que cada aluno selecione seu idioma preferido no início da sessão. Deixe isso desativado se quiser que todos os alunos pratiquem no idioma em que a função foi criada — a configuração recomendada para avaliações formais em que a consistência do idioma faz parte dos critérios de avaliação.

>[!NOTE]
>
>O Virtual Coach oferece suporte ao conteúdo de simulação em nove idiomas. A seleção do idioma do aluno só é significativa se o conteúdo do cenário e a persona forem escritos para suportar o uso multilíngue; se as diretrizes de avaliação e o plano de fundo pessoal forem escritos em um único idioma, ativar essa configuração pode produzir respostas inconsistentes de IA para os alunos que selecionam um idioma diferente.

## Configurar análise de ação na tela

A seção **Análise de ação na tela** permite carregar um vídeo de práticas recomendadas que mostra à IA como pontuar as ações que um aluno executa durante a interpretação de funções. Isso é mais útil para simulações em que se espera que o aluno demonstre ações específicas visivelmente na tela, como navegar em uma interface de software, preencher um formulário ou seguir um processo definido passo a passo.

>[!NOTE]
>
>Esta opção será desabilitada se você tiver carregado somente arquivos do PowerPoint ou PDF na seção **Configurações de Apresentação**.

1. Selecione **Selecionar arquivo** para abrir o navegador de arquivos.
2. Selecione seu arquivo de vídeo e confirme o carregamento.
3. Após o upload, o nome do arquivo aparece na linha de resumo da **Análise de Ações na Tela**.

Seu vídeo deve atender aos seguintes requisitos:

| Requisito | Especificação |
|---|---|
| Formato de arquivo | WEBM, MP4, WMV ou MPEG |
| Tamanho máximo do arquivo | 200 MB |
| Resolução mínima | 1280 x 720 pixels |
| Taxa mínima de quadro | 5 QPS |
| Proporções | Entre 4:3 e 21:9 |

Ao gravar um vídeo de acordo com as práticas recomendadas, descreva cada ação ao mesmo tempo no áudio e na tela. Por exemplo, digamos “Agora estou selecionando o botão Enviar” ao fazer isso, uma vez que a IA depende tanto da narração quanto da ação visual. Mantenha a gravação focada na tarefa, remova notificações e conteúdo não relacionado e combine o vídeo com suas diretrizes de avaliação para que ele demonstre cada ação necessária no ponto do fluxo de trabalho em que deve ocorrer.

## Definir configurações de pontuação

**Pontuação de Aprovação** é a pontuação geral mínima que um aluno deve obter para que a simulação seja marcada como aprovada, aplicada à combinação ponderada de pontuações de conhecimento e estilo. Insira um número entre 1 e 100 no campo **Pontuação de aprovação** (o padrão é 80) e selecione **Concluído**.

>[!TIP]
>
>Para avaliações formais, uma pontuação de aprovação de 75 a 80 é típica. Para desempenhos de função no modo de prática, onde o objetivo é o desenvolvimento de habilidades em vez da certificação, considere um limite inferior ou habilite o **Modo de prática**.

**Pesos de pontuação da IA** define quanto o componente Conhecimento (se o aluno abordou os tópicos necessários e forneceu informações precisas) e o componente Estilo (ritmo, clareza, palavras de preenchimento, comprimento da frase, energia) contribuem para a pontuação geral. Arraste o controle deslizante para ajustar o equilíbrio. Os dois valores sempre somam 100% e o padrão é Conhecimento 70% / Estilo 30%. Para obter orientação sobre como os alunos interpretam essas pontuações, consulte [entender seu relatório de desempenho de coach virtual](/help/migrated/learners/feature-summary/virtual-coach/understand-virtual-coach-performance-report.md).

| Tipo de cenário | Proporção recomendada | Motivo |
|---|---|---|
| Avaliação de habilidades ou certificação | 80% de conhecimento/20% de estilo | A precisão do conteúdo é a medida principal |
| Ativação de vendas | 60% de conhecimento/40% de estilo | A entrega é tão importante quanto a mensagem nas conversas com os clientes |
| Desenvolvimento de liderança | 70% de conhecimento/30% de estilo | Equilibrado — tanto o conteúdo quanto o tom são essenciais nas conversas das pessoas |
| Coaching de comunicação | 40% de conhecimento/60% de estilo | O estilo é o objetivo de aprendizado principal |

**Habilitar o Modo de Prática para alunos** permite que os alunos solicitem dicas durante a simulação para ajudá-los a se manter nos trilhos. Isso é útil para o aprendizado no estágio inicial. Quando habilitado, você pode definir o **Máximo de Dicas por Sessão** (padrão 5, ajustável de 1 a 10) e a duração da visibilidade da dica (padrão 30 segundos).

>[!NOTE]
>
>As dicas não estão disponíveis durante as avaliações formais. Se você estiver usando esta interpretação como uma avaliação graduada, desative o Modo de prática para que todos os alunos sejam avaliados nas mesmas condições.

**Ocultar pontuação** impede que os alunos vejam sua pontuação numérica após a sessão; eles ainda recebem feedback qualitativo e análise em nível de tópico. Use isso quando o role-play for apenas para prática, quando apenas um gerente avaliador deve ver o resultado, ou quando você deseja reduzir a ansiedade da pontuação nos estágios iniciais de aprendizado.

## Definir configurações avançadas de interpretação de funções

Essas configurações opcionais controlam como e quando a simulação termina e como o ambiente da sessão é configurado.

**Permitir que a IA encerre a reprodução de função.** Por padrão, somente o aluno pode encerrar uma simulação selecionando **Encerrar Simulação**. Ative essa opção e descreva a condição sob a qual a pessoa deve fechar a conversa naturalmente, por exemplo: “Quando o aluno agenda com sucesso uma reunião de acompanhamento ou a pessoa recusa três vezes, a pessoa deve encerrar a chamada educadamente”. Use isso para cenários avançados em que o ponto de extremidade natural da conversa, não um temporizador, deve determinar quando a sessão é fechada.

**Limite de tempo de simulação.** Insira um número entre 1 e 59 minutos para definir uma duração máxima da sessão. Quando atingida, a simulação termina automaticamente e o aluno é levado à página de análise.

| Tipo de cenário | Limite sugerido |
|---|---|
| Cold call ou breve prática de abertura | 3 a 5 minutos |
| Chamada de detecção ou avaliação de necessidades | 10 a 15 minutos |
| Discussão completa sobre vendas ou liderança | 15 a 20 minutos |
| Avaliação formal com vários tópicos | Corresponder à duração esperada da conversa no mundo real |

A **Penalidade de sessão curta** desestimula os alunos a encerrarem sessões muito rapidamente aplicando uma redução de pontuação se a sessão ficar abaixo de uma duração mínima definida. Use essa opção quando a duração da sessão for significativa para o objetivo de aprendizado. Por exemplo, em uma chamada de detecção em que o aluno deve passar tempo suficiente descobrindo as necessidades antes de propor uma solução.

>[!NOTE]
>
>Não use a Penalidade de sessão curta em role-plays no modo de prática, em que os alunos ainda estão construindo confiança, uma vez que penalizar saídas precoces pode aumentar a ansiedade e desencorajar tentativas repetidas.

**Habilitar o compartilhamento de tela** permite que os alunos compartilhem a tela durante a simulação. Isso é relevante para cenários que incluem um componente de **Análise de Ação na Tela**. Ela fica desabilitada por padrão se você tiver carregado somente documentos do PowerPoint ou PDF em **Configurações de Apresentação**.

**Habilitar legendas de IA pessoal** exibe em tela o texto do que a pessoa de IA está dizendo em tempo real. Ative essa opção para alunos com dificuldades de audição ou que estão praticando em um segundo idioma, em ambientes ruidosos ou em cenários em que a leitura das palavras exatas da pessoa seja importante para a compreensão de objeções sutis.

## Publish, a interpretação de papéis da Virtual Coach

Após configurar todas as seções, selecione **Publish**.

![](/help/migrated/authors/feature-summary/assets/virtual_coach7.png)
*Conclua os detalhes da publicação e selecione Salvar para adicionar sua interpretação à Biblioteca de Conteúdo.*

1. Insira o título da interpretação de papéis.
2. Selecione a pasta em que deseja adicionar a representação.
3. Ou adicione tags e uma data de expiração.
4. Selecione **Salvar**. A função é adicionada à **Biblioteca de Conteúdo**.

Agora você criou uma função de treinador virtual do início ao fim no Adobe Learning Manager Virtual Coach. Continue a [adicionar uma representação de treinador virtual a um curso](/help/migrated/authors/feature-summary/virtual-coach/add-virtual-coach-role-play-to-course.md) para disponibilizá-lo para os alunos. Para obter respostas às perguntas comuns de criação, incluindo por que uma interpretação de função pode obter zero, quantas pessoas são compatíveis com a interpretação de função de várias pessoas e como escrever um bom prompt para o Assistente de Cocriação de IA, consulte as [Perguntas frequentes sobre o Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/virtual-coach-faq.md).
