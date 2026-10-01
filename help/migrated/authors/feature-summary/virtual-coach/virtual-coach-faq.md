---
description: Encontre respostas para perguntas comuns sobre Virtual Coach authoring, licenciamento, segurança, privacidade de dados, pontuação e a experiência do aluno
jcr-language: en_us
title: Perguntas frequentes sobre o Virtual Coach
exl-id: b8955b04-4655-413a-b570-a05b1f76285c
source-git-commit: 449f25df93867bf4d5ec11af057f8da7c405a09f
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 0%
---

# Perguntas frequentes sobre o Virtual Coach

## Criação

Obtenha respostas para perguntas comuns sobre a criação, configuração e solução de problemas de uma função de treinador virtual.

1. **Por que minha interpretação de função teve zero, embora eu tenha abordado a maioria dos tópicos?**
Verifique se um dos seus tópicos está habilitado para **Criar ou Interromper**. Se um aluno não abordar um tópico Criar ou Quebrar durante a conversa, a pontuação final da simulação é 0, independentemente de quão bem ele se apresentou em todo o resto. Reserve Faça ou Interrompa um ou dois tópicos genuinamente não negociáveis para evitar que isso aconteça em uma tentativa razoável. Para obter a configuração completa, consulte [criar e publicar uma função de treinador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

2. **Quantas pessoas podem ser incluídas em uma representação multipessoal?**
Até quatro pessoas em um único cenário, cada uma configurada individualmente com sua própria **Função**, **Personalidade** e **Preocupações pessoais**. Use isso quando um aluno precisar navegar por mais de uma parte interessada na mesma conversa, como uma apresentação do comitê de compra ou uma revisão do painel executivo.

3. **Como escolho entre voz, bate-papo e vídeo para uma interpretação de função?**
Isso depende do tipo de pessoa selecionado. **Pessoas do Sistema** oferecem suporte apenas a **Voz e Vídeo** (um avatar animado com voz falada) ou **Voz**. As **Pessoas personalizadas** oferecem suporte à interação de voz, e você pode habilitar o **Avatar de vídeo** separadamente para pessoas que oferecem suporte ao modo de Voz e Vídeo. Escolha Voz e vídeo para a simulação mais realista, ou Voz apenas para cenários em que um avatar visual não é necessário, como treinamento por telefone.

4. **Como escrevo um bom aviso para o Assistente de Cocriação de IA?**
Insira uma breve descrição que contorne o cenário, como `Handling price objections in enterprise sales` ou `Pitching our new product to a buying committee`. O assistente de IA faz perguntas de acompanhamento para ajudar você a criar os tópicos Visão geral, personalidade da IA e Avaliação. Forneça o máximo de contexto possível sobre a situação, o papel e as preocupações da pessoa, e como você quer medir o sucesso. Mais detalhes em sua descrição inicial significam menos idas e vindas no bate-papo. Consulte [reunir materiais para uma interpretação de função de treinador virtual](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) para obter um modelo de prompt mais completo.

5. **Posso editar uma reprodução de função após sua publicação?**
Sim As alterações nas configurações personalizadas, nos tópicos e em outras configurações entram em vigor imediatamente para qualquer interpretação de função não publicada. Se uma ação já estiver publicada e atribuída aos alunos, republice-a depois de fazer alterações para que os alunos vejam a versão mais recente.

Para perguntas gerais sobre produtos, licenciamento e administração, consulte as [Perguntas frequentes sobre o Adobe Learning Manager Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/virtual-coach-faq.md).

## Treinamento e conformidade

1. **Como o Virtual Coach protege os dados do cliente e do aluno?**
Os dados do cliente são armazenados usando criptografia AES-256, protegidos em trânsito usando TLS 1.3+ e separados logicamente por identificadores exclusivos do cliente para garantir o isolamento entre os ambientes do cliente. Esses controles são validados por meio de testes anuais de penetração de terceiros.

2. **Onde os dados da Instrução Virtual são armazenados e processados?**
Os dados do cliente são armazenados em data centers da UE, oferecendo suporte ao alinhamento com os requisitos europeus de privacidade.

3. **Por quanto tempo o Virtual Coach retém os dados do cliente e do aluno e pode ser excluído?**
Os dados da sessão podem ser retidos durante a vigência do contrato de serviço, e os clientes podem configurar políticas de retenção específicas da empresa. Usuários individuais podem excluir suas próprias gravações, administradores podem executar exclusões em massa e os dados podem ser exportados antes da exclusão. Mecanismos de exclusão automática e registro de auditoria também são compatíveis.

4. **O conteúdo carregado pelo cliente é usado para fins diferentes da geração da função, como treinamento de IA ou melhoria do produto?**
Não, os dados do cliente não são usados para treinamento de IA.

5. **Como o Virtual Coach usa IA e quais salvaguardas estão em vigor para respostas geradas por IA?**
Virtual Coach usa IA generativa para criar experiências interativas de interpretação de papéis. Várias salvaguardas estão em vigor, incluindo filtros de conteúdo do Azure OpenAI para categorias como violência, discurso de ódio, conteúdo sexual e automutilação; proteções de nível de solicitação e controles contextuais que mantêm a IA focada em casos de uso de aprendizado e desenvolvimento. Testes de segurança por IA também são conduzidos, e salvaguardas como Transformação de aviso com base em segurança e comportamento de esclarecer e depois recusar são usadas para solicitações sensíveis. Além disso, os compromissos contratuais exigem a divulgação de resultados gerados por IA e a conformidade com os regulamentos de IA aplicáveis.

6. **A Virtual Coach oferece suporte a quais padrões de privacidade e conformidade?**
O Virtual Coach oferece suporte a proteções de privacidade relacionadas ao GDPR, controles de retenção configuráveis, registro de auditoria, recursos de exclusão de usuários e hospedagem de dados com base na UE. O contrato também exige conformidade com as leis e regulamentos aplicáveis, incluindo a Lei de IA da UE e a Lei de Transparência de IA da Califórnia (SB-942).

7. **Quem possui o conteúdo carregado para o Virtual Coach e o conteúdo gerado durante uma sessão?**
O cliente é proprietário do conteúdo carregado no Virtual Coach e do conteúdo gerado durante uma sessão.

8. **Onde residem os dados do Virtual Coach, no Adobe Learning Manager ou com o provedor de serviços Virtual Coach?**
Os dados Role-play são armazenados na infraestrutura em nuvem do provedor de serviços Virtual Coach e hospedados em data centers da UE.

## Produto

1. **Como o Virtual Coach é ativado para um cliente do Adobe Learning Manager existente?**
Consulte [Ativando Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md#activatevirtualcoach)

2. **Por quanto tempo a ativação da Instrução Virtual é válida e como ela é renovada?**
A ativação da Virtual Coach no Adobe Learning Manager é válida pela duração do seu contrato de assinatura de complemento. Não é automaticamente perpétuo. Em vez disso, a validade está de acordo com o período de assinatura.

   **Renovação:** para continuar usando o Virtual Coach após o término do período de seu contrato, você deve renovar sua assinatura. No momento da compra, o Adobe fornece uma chave de ativação, que o administrador de conta usa para ativar o Treinador virtual na seção Faturamento. Se renovar o contrato, você receberá instruções e uma nova chave de ativação, se necessário, para manter o acesso ininterrupto.

   Créditos do Usuário Ativo Mensal (MAU) também são alocados para cada período de contrato. Todos os créditos não utilizados no final do contrato caducam. Não transitam para um período renovado ou novo. Sua ativação dura enquanto sua assinatura paga do Virtual Coach estiver ativa, e a renovação ocorre estendendo sua assinatura, conforme gerenciada por meio de sua conta Adobe.

3. **O que acontece com os documentos de origem carregados e com os dados de sessão gerados após uma reprodução de função ser criada ou concluída?**
Os documentos de origem carregados podem ser usados para criar e configurar cenários de interpretação de funções, personas e critérios de avaliação. Depois que os alunos concluem uma função, o Virtual Coach gera resultados de avaliação, pontuações, feedback de coaching e informações de conclusão para dar suporte às atividades de aprendizado e relatório. Os dados associados às funções exercidas permanecem disponíveis de acordo com o ciclo de vida do conteúdo aplicável e as políticas de retenção.

4. **Os alunos podem repetir uma interpretação de função?**
Sim Os alunos podem repetir uma sessão de interpretação de funções várias vezes para praticar suas habilidades, aplicar feedback de orientação e melhorar seu desempenho. Depois de concluir uma ação, os alunos podem revisar seus comentários e começar outra tentativa de continuar desenvolvendo suas habilidades.

## Geral

1. **O que é Virtual Coach?**
Virtual Coach é um recurso de interpretação e orientação baseado em IA integrado ao Adobe Learning Manager. Ele permite que os alunos pratiquem conversas no mundo real com uma pessoa de IA que responde de forma inteligente em tempo real e, em seguida, receba um relatório de desempenho instantâneo sobre o que disseram e como disseram. Para obter uma explicação completa, consulte [o que é Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md).

2. **Quem usa o Virtual Coach?**
As organizações usam o Virtual Coach para treinar representantes de vendas, equipes de atendimento ao cliente, agentes de call center, gerentes e líderes, novas contratações, parceiros e funcionários que estão aprendendo novos produtos ou processos. O Virtual Coach está disponível para todos os alunos, autores e administradores em uma conta do Adobe Learning Manager na qual foi ativado. Os alunos acessam e concluem sessões de interpretação de funções, os autores criam e publicam cenários de interpretação de funções e os administradores gerenciam créditos e visualizam relatórios.

3. **O Virtual Coach usa automaticamente meu conteúdo do Adobe Learning Manager existente?**
Não. Os autores devem fornecer materiais de referência, como playbooks, plataformas de vendas, transcrições e rubricas de pontuação, ou um prompt escrito, para cada role-play que criarem. O Virtual Coach usa esses materiais carregados e definições personalizadas para conduzir a conversa. Ele não utiliza automaticamente o conteúdo já presente em sua biblioteca de conteúdo ou cursos. Consulte [reunir materiais para uma interpretação de função de treinador virtual](/help/migrated/authors/feature-summary/virtual-coach/gather-materials-for-virtual-coach-role-play.md) para saber o que preparar.

4. **Quais tipos de funções estão disponíveis?**
O Virtual Coach oferece suporte a três domínios: capacitação de vendas, desenvolvimento de liderança e avaliação de habilidades. Os autores escolhem entre modelos pré-criados que abrangem cenários como chamadas de detecção B2B, “cold calls”, tratamento de objeções, fornecimento de feedback difícil e diminuição de reclamações de clientes. Os autores também podem criar cenários personalizados do zero usando o assistente de IA. Consulte [criar e publicar uma função de treinador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).

5. **Quais idiomas são compatíveis com o Virtual Coach?**
O Virtual Coach está disponível em nove idiomas para a interface e o conteúdo de simulação: alemão (Alemanha), espanhol (América Latina), espanhol (Espanha), francês (França), italiano (Itália), português (Portugal), português (Brasil), holandês (Países Baixos) e inglês.

6. **Como o Virtual Coach é licenciado e cobrado?**
O Virtual Coach está disponível como uma assinatura complementar do Adobe Learning Manager. O uso é medido em Usuários Ativos Mensais (MAUs). Um crédito MAU é consumido quando um aluno inicia um curso em um mês; as sessões adicionais do mesmo aluno nesse mês não consomem créditos adicionais. Os créditos não utilizados no final do contrato anual caducam. Consulte [gerenciar o uso e o faturamento do Virtual Coach](/help/migrated/administrators/feature-summary/virtual-coach/manage-virtual-coach-usage-billing.md).

7. **Como é calculada a pontuação de um aluno?**
Cada sessão produz uma pontuação de conhecimento e uma pontuação de estilo. A pontuação do conhecimento reflete se o aluno abordou os tópicos obrigatórios e forneceu informações precisas. A pontuação de estilo reflete como o aluno se comunicou, incluindo ritmo, clareza, palavras de preenchimento, força da frase e energia vocal. Os autores definem o peso de cada componente ao configurar o cenário; uma configuração comum é 70% de conhecimento e 30% de estilo. Consulte [entender seu relatório de desempenho do Virtual Coach](/help/migrated/learners/feature-summary/virtual-coach/understand-virtual-coach-performance-report.md).

8. **Os alunos podem baixar o relatório de desempenho?**
Sim Além de exibir o relatório na tela, os alunos podem baixá-lo como um PDF para manter seus próprios registros ou compartilhá-lo com um gerente.

9. **Um aluno pode repetir uma interpretação de função?**
Sim Os alunos podem tentar uma interpretação de papéis quantas vezes quiserem. Cada tentativa é uma nova sessão independente e gera um novo relatório de desempenho. Somente a primeira sessão em um mês consome um crédito MAU.

10. **Os alunos podem enviar suas sessões para revisão humana?**
Não.

11. **O Virtual Coach está disponível em dispositivos móveis?**
O Virtual Coach é compatível com o Adobe Learning Manager para desktop, dispositivos móveis e Web, além de APIs. Ela não está disponível no aplicativo Adobe Learning Manager para dispositivos móveis (iOS/Android) na versão atual.

12. **Os dados do aluno são usados para treinar a IA?**
Não. O Virtual Coach está hospedado em uma infraestrutura compatível com o GDPR e nenhum dado pessoal do aluno é usado para treinar modelos de IA.

13. **Qual é a diferença entre uma ajuda de tarefa e um módulo de curso para Virtual Coach?**
Uma ajuda de tarefa é um recurso independente e por demanda que os alunos podem acessar diretamente do catálogo a qualquer momento sem estar inscritos em um curso. Um módulo de curso é acessado como parte de uma sequência de cursos estruturados com inscrição, rastreamento da conclusão e avaliação formal. A mesma interpretação pode ser publicada como uma ajuda de tarefa e adicionada a vários cursos simultaneamente. Consulte [adicionar uma representação de função de treinador virtual a um curso](/help/migrated/authors/feature-summary/virtual-coach/add-virtual-coach-role-play-to-course.md).

14. **Como empacotar Virtual Coach (Treinador Virtual) ao lançar um novo processo ou produto?**
Empacotar a interpretação dentro de um curso ou jornada de aprendizado juntamente com o conteúdo de treinamento relacionado e distribuir o link do curso por e-mail ou outras comunicações de gerenciamento de alterações. O Virtual Coach funciona melhor posicionado como a última milha do treinamento: o ponto de verificação logo após os alunos concluírem o conteúdo relacionado, no qual demonstram que podem aplicá-lo, em vez de ser uma atividade independente.

15. **O Virtual Coach é compatível com implementações sem periféricos ou de API?**
As APIs públicas para buscar cursos e ajudas de tarefa também buscam cursos de orientação virtual e ajudas de tarefa. O filtro `jobAidType` está disponível especificamente para obter ajudas de tarefa de Treinador Virtual. O conteúdo do Virtual Coach é compatível com o player sem periféricos, além de cursos e ajudas de tarefa que contêm o trabalho do Virtual Coach no Fluidic Player.

Para perguntas sobre a criação e a configuração de uma interpretação de papéis, consulte esta página de perguntas frequentes.
