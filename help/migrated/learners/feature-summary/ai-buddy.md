---
description: O Assistente de IA do aluno (Beta) é um complemento de bate-papo viabilizado por GenAI no Adobe Learning Manager que ajuda os alunos a obter respostas rápidas e precisas com base em seu conteúdo de aprendizado atribuído. Usando consultas de linguagem natural, os alunos podem recuperar instantaneamente respostas focadas com citações claras, facilitando a localização das informações certas, a verificação das fontes e o aprendizado de forma eficiente sem pesquisar em cursos inteiros.
jcr-language: en_us
title: Assistente de IA do aluno (Beta) no Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 0ef69eb5d95c4203a80cd5b4874b99855ebedcc4
workflow-type: tm+mt
source-wordcount: '2146'
ht-degree: 0%

---

# Introdução

O Assistente de IA (beta) para alunos os ajuda a encontrar rapidamente respostas a partir do conteúdo de aprendizado atribuído sem navegar pelos cursos inteiros. Você pode fazer perguntas em linguagem simples e receber respostas precisas e focadas com links de origem para o conteúdo relevante do curso.

>[!IMPORTANT]
>
>O Assistente de IA do aluno está atualmente na versão beta e está sendo lançado por meio de uma implementação em fases. O acesso pode variar de acordo com o usuário.


## O que é o Assistente de IA?

O Assistente de IA é um companheiro de bate-papo viabilizado por GenAI no Adobe Learning Manager que fornece respostas rápidas e precisas às perguntas do aluno usando o conteúdo de aprendizado confiável disponível para ele no Adobe Learning Manager. Também inclui citações para que os alunos sempre saibam a fonte das informações.

## Por que usá-lo?

* Os alunos enfrentam a sobrecarga de conteúdo e muitas vezes não sabem por onde começar nem qual recurso usar.

* As regras de acesso e catálogo dificultam a descoberta de qual conteúdo está disponível para eles.

* As jornadas de aprendizado são fragmentadas em vários formatos e tipos de treinamento, como cursos, salas de aula virtuais, ajudas de tarefa e avaliações.

* Não há uma maneira fácil e unificada de recuperar informações específicas de diversos formatos, como SCORM, PDF, documentos, vídeos ou transcrições.

* Diferentes funções e setores do aluno (por exemplo, vendas, marketing, suporte, operações) têm necessidades de informações exclusivas que exigem respostas rápidas e contextuais.

## Que tipos de conteúdo o Assistente do AI pode transcrever

O Assistente de IA pode localizar informações de todos os tipos de conteúdo de aprendizado atribuídos a você, incluindo:

* **Documentos:** PDF, Word, PowerPoint, Excel, HTML

* **Mídia:** áudio (mp3, wav, m4a), vídeo (mp4, mov, wmv)

* **Conteúdo Interativo:** SCORM 1.2, SCORM 2004,

* **Tipo de Objeto de Aprendizado:** Cursos, programações de aprendizado, certificações, ajudas de tarefa

O Adobe transcreve com segurança seu conteúdo de aprendizado usando serviços de processamento de terceiros confiáveis hospedados no ambiente VPC privado do Adobe.

**IMPORTANTE**

O Assistente do AI consome somente conteúdo que é:

* Disponível nos catálogos configurados para o Assistente do aluno por administradores e

* Parte de catálogos internos no Adobe Learning Manager.

Catálogos compartilhados, adquiridos, externos ou outros não internos não são compatíveis como fontes de conteúdo para o Assistente do AI na versão atual.

Se você não tiver acesso a um curso, os links de citação relacionados não estarão acessíveis para você. Bibliotecas de terceiros (como LinkedIn Learning ou Go1) não estão incluídas para recuperação de respostas.

## Recursos de conversação

O Assistente de IA oferece suporte a perguntas individuais e a conversas com vários turnos. Ele lembra suas consultas anteriores na mesma sessão.

**Exemplo de conversa:**

Você: “Qual é a política de reembolso?”
Assistente: fornece resumo
Você: “E quanto aos reembolsos após 30 dias?”
Assistente: retorna informações mais específicas

## Casos de uso do Assistente do AI

### Suporte a aprendizado Just-in-Time (todos os alunos)

Os alunos geralmente precisam de respostas rápidas enquanto trabalham, não de repetições completas do curso. O assistente de IA permite a recuperação instantânea de informações precisas do conteúdo de aprendizado atribuído.

**O que ajuda:**

* Obtenha respostas diretas a perguntas específicas de cursos, ajudas de tarefa e documentos

* Ir para seções referenciadas exatas usando citações

* Reduza o tempo gasto pesquisando em vários objetos de aprendizado

![Suporte a aprendizado just-in-time usando o Assistente de aluno](assets/just-in-time.png)

### Viabilização de vendas e conversas com clientes

As equipes de vendas precisam de informações rápidas e precisas sobre produtos e processos durante as interações ao vivo com os clientes. O assistente de IA atua como um complemento de conhecimento sob demanda.

**O que ajuda:**

* Recuperar recursos e posicionamento atualizados do produto

* Gerar scripts de vendas rápidas ou pontos de discussão a partir do conteúdo de treinamento

* Comparar versões ou ofertas de produtos usando o material de aprendizado atribuído

* Reforce o conhecimento de vendas sem refazer cursos inteiros

![Habilitação de vendas usando o Assistente do aluno](assets/sales-enablement.png)

**Exemplo 2**

**Objetivo:** mostre que o Assistente de IA pode ajudar os representantes de vendas a responder instantaneamente a perguntas de comparação de clientes.

**Aviso recomendado:** compare o Adobe Learning Manager e um LMS tradicional para treinamento corporativo. Mostrar a comparação em formato tabular.

![Saída tabular no Assistente do aluno](assets/tabular-format.png)

### Prontidão para marketing e campanha

As equipes de marketing geralmente precisam de atualizações rápidas antes de revisões, lançamentos ou discussões com as partes interessadas. O assistente de IA resume o conteúdo de aprendizado complexo em insights acionáveis.

**O que ajuda:**

* Resuma cursos longos ou vídeos nos principais pontos

* Atualizar conhecimento do processo ou do produto antes das reuniões

* Descubra conteúdo de aprendizado relacionado para aprofundar o conhecimento

![prontidão para marketing e campanha usando o Assistente de Aluno](assets/marketing-readiness.png)

### Esclarecimento operacional e de processo

Equipes internas, de operações e de suporte contam com documentação precisa do processo. O Assistente de IA ajuda a esclarecer instantaneamente políticas e fluxos de trabalho.

**O que ajuda:**

* Encontre respostas sobre processos internos, SOPs e diretrizes de conformidade

* Esclareça detalhes no nível de etapa sem navegar por documentos longos

* Reduzir a dependência de SMEs para perguntas repetitivas

![Documentação operacional e de processo usando o Assistente de Aluno](assets/operational-process.png)

### Integração e transições de função mais rápidas

Novas contratações e funcionários que passam a ter novas funções geralmente têm dificuldade em navegar por grandes catálogos de aprendizado. O assistente de IA acelera o aumento dos níveis ao orientá-los para respostas relevantes.

**O que ajuda:**

* Responder a perguntas comuns de integração a partir do conteúdo atribuído

* Fornecer explicações rápidas de conceitos específicos de função

* Suporte ao aprendizado autodirecionado sem sobrecarga de informações

![Integração de funcionários](assets/onboarding.png)

### Atualização de conhecimento e aprendizado contínuo

Os alunos experientes precisam de atualizações rápidas em vez de reciclagem completa. O Assistente do AI oferece suporte ao aprendizado contínuo no fluxo de trabalho.

**O que ajuda:**

* Atualize o conhecimento sob demanda sem ter de assistir novamente aos cursos

* Reforçar os resultados da aprendizagem após a conclusão do treino

* Incentive o engajamento frequente e de baixo esforço com conteúdo de aprendizado

![Resposta de atualização de conhecimento no Assistente de Aluno](assets/knowledge-refresh.png)

## Como o assistente de IA do aluno usa o conteúdo

O assistente de IA do aluno ajuda você a encontrar respostas precisas rapidamente enquanto aprende. Para usá-lo de forma eficaz, você deve entender qual conteúdo o assistente usa, o que ele não usa e como ele gera respostas.

### Qual conteúdo é usado pelo Assistente do AI

O Assistente de IA do aluno responde a perguntas usando somente o conteúdo de aprendizado atribuído a você no Adobe Learning Manager.

* O assistente usa o conteúdo dos catálogos internos que o administrador ativa para o assistente do Aluno AI.

* O assistente respeita sua função, associação a grupo e permissões de catálogo ao recuperar informações.

### Qual conteúdo o Assistente do AI não usa

O Assistente de IA do aluno limita as respostas ao escopo de aprendizado atribuído.

* Ele não usa conteúdo dos catálogos Padrão, Compartilhado, Adquirido, Externo ou outros catálogos não Internos.

* Ele não recupera informações de bibliotecas de conteúdo de terceiros, como o LinkedIn Learning ou o Go1.

* Ele não navega na internet nem acessa sites externos para gerar respostas.

### Como o Assistente de IA gera respostas

O Assistente de IA do aluno analisa o conteúdo de aprendizado atribuído para gerar respostas focadas e contextuais.

* Cada resposta inclui citações que fazem referência ao conteúdo original.

* Você pode selecionar uma citação para navegar diretamente para o curso, módulo ou documento relevante.

* As citações ajudam a verificar as informações e explorar o contexto adicional quando necessário.

### Usar o Assistente do AI com responsabilidade

Use o Assistente de IA do aluno como uma ajuda de aprendizado para explorar, atualizar e reforçar o conhecimento.

* Trate as respostas como orientação com base no conteúdo de aprendizado disponível.

* Consulte o material de origem citado para obter informações completas e oficiais.

### Como os administradores controlam o acesso

Os administradores gerenciam o acesso ao Assistente de IA do aluno e controlam o conteúdo usado.

* Os administradores atribuem o assistente a grupos de usuários específicos.

* Os administradores selecionam quais catálogos internos o assistente pode usar como fontes de conteúdo.

* Esses controles garantem que o assistente mostre apenas conteúdo de aprendizado aprovado e relevante.

## Sobre prompts internos

O Assistente de IA do aluno inclui um conjunto de prompts incorporados para ajudar os alunos a começar rapidamente com perguntas e cenários comuns. Esses prompts orientam os alunos sobre como interagir com o assistente e demonstram os tipos de perguntas que podem ser feitas.

![Prompts internos fornecidos pelo Assistente de Aluno](assets/built-in-prompts.png)

Os prompts internos são personalizáveis por conta. As organizações podem personalizar esses prompts para refletir seus objetivos de aprendizado, funções do aluno, terminologia ou casos de uso específicos.

Os administradores podem trabalhar com o Gerente de sucesso do cliente (CSM) para configurar, modificar ou atualizar os prompts incorporados para a conta. A personalização do prompt é gerenciada no nível da conta e não é configurável diretamente na interface de usuário do Adobe Learning Manager na versão atual.

Os prompts exibidos para os alunos podem variar por conta, com base na configuração definida com o Adobe.

## Ativar o Assistente de IA do aluno

![Assistente de aluno habilitado por IA](assets/learner-ai-assistant.png)

O Assistente de IA (beta) fornece suporte viabilizado por IA para ajudar os alunos a descobrir e se envolver com conteúdo de maneira mais eficaz. Os administradores controlam o acesso atribuindo o recurso a grupos de usuários e catálogos específicos. Somente catálogos internos devem ser usados ao configurar o Assistente do AI. O conteúdo de catálogos Compartilhados, Adquiridos, Externos ou outros não Internos não é compatível com a exibição de respostas e citações do Assistente do AI.

Os administradores selecionam quais grupos de usuários e catálogos internos podem acessar o recurso Assistente do AI. Eles devem garantir que os catálogos atribuídos incluam apenas o conteúdo de aprendizado apropriado para ser revelado em respostas e citações de IA e que esses catálogos sejam internos, não compartilhados, adquiridos ou externos.

Antes de configurar o Assistente do AI (beta), confirme se você tem credenciais de administrador e identificou quais grupos de usuários e catálogos devem ter acesso ao recurso.

### Configurar acesso ao Assistente do aluno

Para ativar o Assistente de IA do aluno:

&#x200B;1. Faça logon no Adobe Learning Manager como administrador.

2.Selecione **Configurações** na home page.

![Console do administrador com a opção Configurações no painel esquerdo](assets/settings-menu.png)

3.Selecione **Assistente de IA do aluno (Beta)** no menu **Configurações**.

![O console do administrador exibe a opção Assistente de IA do aluno no painel esquerdo](assets/learner-assistant-ai-beta.png)

4.Selecione a opção de alternância para habilitar o **Assistente de IA do aluno (Beta)**.

![O console de administradores exibe a alternância habilitada para o Assistente de IA do aluno](assets/learner-assistant-toggle.png)

5.Selecione um ou mais grupos de usuários na opção **Grupos de usuários qualificados**.

6.Selecione **Salvar** para aplicar as configurações do grupo de usuários.

7.Selecione um ou mais catálogos da opção **Catálogos qualificados**.

8.Selecione **Salvar** para aplicar as configurações do catálogo.

>[!IMPORTANT]
>
>O Assistente do AI oferece suporte somente a catálogos internos. Se um catálogo compartilhado, adquirido, externo ou outro não interno for selecionado, seu conteúdo não será revelado pelo Assistente do AI, mesmo se o catálogo for exibido na lista Catálogos qualificados.

## Acessar o Assistente de IA do aluno no Adobe Learning Manager

O Assistente de IA do aluno (Beta) do Adobe Learning Manager ajuda você a encontrar respostas rapidamente enquanto aprende. Essa ferramenta inteligente responde diretamente às suas perguntas sobre cursos, conteúdo e recursos da plataforma, tudo da conta do aluno.

O Assistente do AI só pode usar o conteúdo de catálogos internos que o administrador ativou para o Assistente do aluno. O conteúdo armazenado somente nos catálogos Compartilhados, Adquiridos ou Externos não será incluído.

O Assistente de IA do aluno (Beta) está disponível somente para os alunos selecionados.

### Iniciar o Assistente do AI

Para iniciar o Assistente de IA do aluno:

&#x200B;1. Faça logon no Adobe Learning Manager como aluno.

2.Selecione **Perguntar ao assistente de IA** na página inicial.

![A página inicial do aluno exibe Perguntar ao assistente de IA para selecionar e abrir o painel Assistente de IA do aluno](assets/ask-ai-assistant.png)

3.Quando a tela **Assistente de IA do aluno (Beta)** for exibida, selecione **Começar**.

![Selecione Começar para iniciar o Assistente de Aluno](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>Ao iniciar o Assistente do AI pela primeira vez, você deve dar seu consentimento antes de usá-lo. A caixa de diálogo de consentimento será exibida somente durante essa primeira inicialização. Para todas as inicializações subsequentes, você será direcionado ao Assistente do AI para inserir seus prompts.

&#x200B;4. Digite seu prompt no campo de texto.

![Digite o prompt no Assistente do aluno](assets/type-prompt.png)

5.Pressione **Enter** para receber uma resposta. Revise suas respostas, fontes e recomendações.

O Adobe permite a personalização imediata no nível da conta. Para configurar ou atualizar prompts integrados, entre em contato com o Gerente de Sucesso do Cliente (CSM) da Adobe.

As respostas do Assistente de IA incluem citações a cada resposta para que os alunos possam verificar facilmente de onde as informações vêm. Cada referência citada é vinculada ao módulo do curso original, à ajuda de tarefa ou a outro conteúdo de aprendizado.

Os alunos podem:

* Selecionar o número de citação embutido para saltar para a seção referenciada exata

* Abrir a lista completa de fontes selecionando **Mostrar fontes** na parte inferior da resposta

![Exibir fontes na resposta](assets/show-sources.png)

O Assistente do aluno inclui citações com cada resposta para mostrar de onde as informações vêm. Cada citação é vinculada diretamente ao curso, módulo ou objeto de aprendizado original usado para gerar a resposta.

Você pode selecionar qualquer citação para abrir a página real do curso no Adobe Learning Manager e revisar o conteúdo completo no contexto. As citações ajudam a verificar as informações, explorar detalhes adicionais e continuar aprendendo com a fonte confiável.

## Acessar o Assistente do AI usando a pesquisa

Os administradores também podem iniciar o Assistente do AI diretamente da barra de pesquisa. Basta digitar sua pergunta e selecionar **Perguntar ao Assistente de IA** nas opções que aparecem abaixo para obter respostas do conteúdo de aprendizado atribuído.

![Acessar o Assistente de Aluno na barra de pesquisa](assets/learner-assistant-search.png)

## Fornecer feedback sobre as respostas do Assistente de IA do aluno (Beta)

Seu feedback sobre as respostas geradas pelo Assistente de IA do aluno (Beta) ajuda a melhorar a precisão, a relevância e o desempenho geral.

### Curtir ou não curtir uma resposta

* Selecione **Miniaturas**, escolha o que achou útil na resposta, opcionalmente adicione comentários e selecione **Enviar**.

![Selecione Miniaturas para votar em uma resposta](assets/thumbs-up.png)

* Selecione **Miniaturas**, escolha o motivo pelo qual a resposta não foi útil, adicione comentários e selecione **Enviar**.

![Selecione Miniaturas para votar uma resposta](assets/thumbs-down.png)

## Iniciar novo bate-papo no Assistente do AI

Os alunos podem limpar a conversa atual e iniciar um novo bate-papo a qualquer momento.

* Selecione **Novo bate-papo** na tela do Assistente de IA e selecione **Sim**.

![Iniciar um novo chat no Assistente do Aluno](assets/start-new-chat.png)
