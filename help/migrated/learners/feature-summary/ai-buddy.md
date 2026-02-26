---
description: O Assistente de IA (beta) para alunos é um complemento de bate-papo viabilizado por GenAI no Adobe Learning Manager que ajuda os alunos a obter respostas rápidas e precisas de seu conteúdo de aprendizado atribuído. Usando consultas de linguagem natural, os alunos podem recuperar instantaneamente respostas focadas com citações claras, facilitando a localização das informações certas, a verificação das fontes e a aprendizagem eficiente sem pesquisar em cursos inteiros.
jcr-language: en_us
title: Assistente do AI (beta) para alunos no Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 3534061465070cc98747c8273e1a005707e5a22b
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 0%

---

# Assistente de IA para alunos

O Assistente de IA (beta) para alunos os ajuda a encontrar rapidamente respostas a partir do conteúdo de aprendizado atribuído sem navegar pelos cursos inteiros. Você pode fazer perguntas em linguagem simples e receber respostas precisas e focadas com links de origem para o conteúdo relevante do curso.

>[!IMPORTANT]
>
>O Assistente de IA para alunos está disponível no momento como um recurso beta. Os recursos, cenários compatíveis e limitações podem mudar à medida que o recurso evolui.


## O que é o assistente de IA para alunos

O Assistente de IA é um companheiro de bate-papo alimentado pela GenAI no Adobe Learning Manager que fornece respostas rápidas e precisas às perguntas do aluno usando o conteúdo de aprendizado confiável disponível para ele no Adobe Learning Manager. Também inclui citações para que os alunos sempre saibam a fonte da informação.

### Principais recursos do Assistente de IA

1. Resposta inteligente de perguntas
   * Conversações em turnos simples e turnos múltiplos
   * Compreensão da linguagem natural em inglês
   * Respostas derivadas de cursos, certificações, caminhos de aprendizado e ajudas de tarefa
   * Questões de esclarecimento inteligente quando as consultas são ambíguas
   * Com a tecnologia Azure open AI LLM para gerar respostas
2. Fontes de conteúdo e citações
   * Recupera respostas de recursos disponíveis presentes em catálogos compatíveis.
   * Fornece citações com links diretos para materiais de origem
   * Suporta todos os formatos de conteúdo ALM estáticos e interativos: PDF, DOCX, PPTX, XLSX, Áudio (mp3, wav, m4a), Vídeo (mp4, mov, wmv), HTML, SCORM 2004, SCORM 1.2
3. Experiência do usuário
   * Interface do painel lateral acessível em todas as páginas do aluno
   * Design responsivo que se adapta à área de conteúdo
   * Histórico de bate-papo mantido na sessão do navegador
   * Atualização clara de novos logons ou páginas
   * Tom de professor ou tutor: amigável, claro e pedagogicamente sólido
4. Controles do administrador
   * Ativar ou desativar o recurso no nível da conta
   * Controlar o acesso por grupos de usuários
   * Selecione quais catálogos são incluídos para respostas de IA
   * Requisito de aceitação dos Termos de uso para seguir as diretrizes de IA da Adobe

## A quais tipos de conteúdo o Assistente do AI oferece suporte

O Assistente de IA recupera informações do conteúdo de aprendizado atribuído a você, incluindo:

* **Documentos:** PDF, Word, PowerPoint, Excel, HTML
* **Mídia:** áudio (mp3, wav, m4a), vídeo (mp4, mov, wmv)
* **Conteúdo interativo:** SCORM 1.2, SCORM 2004
* **Tipos de objetos de aprendizado:** cursos, programações de aprendizado, certificações, ajudas de tarefa

O Adobe transcreve com segurança o conteúdo de aprendizado usando serviços de processamento de terceiros confiáveis hospedados em um ambiente VPC privado Adobe.

### Limitações do catálogo e da fonte de conteúdo

O Assistente de IA do aluno usa somente conteúdo de **catálogos internos** explicitamente configurados por administradores.

As seguintes fontes de conteúdo **não têm suporte** na versão atual:

* Catálogos compartilhados
* Catálogos adquiridos
* Catálogos externos
* Catálogos padrão
* Bibliotecas de conteúdo de terceiros (por exemplo, LinkedIn Learning ou Go1)

Se um aluno não tiver acesso a um curso ou ajuda de tarefa, o Assistente de IA não exibirá informações desse conteúdo e os links de citação não estarão acessíveis.

## Casos de uso do Assistente do AI

### Aluno técnico

Sarah é engenheira de vendas e está aprendendo sobre placas gráficas. Ela precisa entender rapidamente as especificações técnicas e os benefícios para responder às perguntas dos clientes com segurança.

O Assistente de IA ajuda Sarah com:

* Explicação técnica clara de uma arquitetura de GPU complexa
* Aprofunde a compreensão sobre várias placas gráficas e suas diferenças
* Explicação de exemplos para que Sarah possa relacionar recursos a casos de uso reais

### Suporte ao cliente

Marcus é especialista em suporte em uma empresa parceira. Ele precisa de respostas rápidas sobre os recursos do produto para ajudar os clientes sem precisar transferir para equipes de engenharia.

O Assistente de IA ajuda Marcus com:

* Encontrar conteúdo de suporte relevante para consultas frequentes de clientes
* Fazer perguntas claras quando a resposta inicial não é específica o suficiente
* Encontrar recomendações para cursos relacionados de solução de problemas para melhorar suas habilidades

### Integração de novo funcionário

Jennifer acabou de entrar na empresa e está sobrecarregada com a quantidade de material de treinamento. Ela precisa de uma maneira de encontrar informações específicas sem revisar cursos inteiros.

O Assistente de IA ajuda Jennifer com:

* Como obter uma orientação passo a passo sobre como enviar relatórios de despesas
* Descobrindo cursos sobre políticas da empresa sem navegar em todo o catálogo
* Guiando-a para a seção apropriada de um curso sem fazê-la assistir horas de vídeo

## Como o Assistente de IA usa o conteúdo

O Assistente de IA ajuda você a encontrar respostas precisas rapidamente enquanto aprende. Para usá-lo de maneira eficaz, você deve entender qual conteúdo o assistente usa, o que não usa e como ele gera respostas.

### Qual conteúdo o Assistente de IA usa

O Assistente de IA responde a perguntas usando somente o conteúdo de aprendizado ativado pelo administrador da conta. O conteúdo do catálogo é indexado.

O Assistente de IA analisa o conteúdo de aprendizado atribuído para gerar respostas focadas e contextuais.

* Cada resposta inclui citações que fazem referência ao conteúdo original.
* Você pode selecionar uma citação para navegar diretamente para o curso, módulo ou documento relevante.
* As citações ajudam a verificar as informações e explorar o contexto adicional quando necessário.

### Transmissão de respostas

Uma resposta de streaming significa que o Assistente de IA fornece a resposta progressivamente conforme ela é gerada, para que os usuários possam começar a ler a resposta imediatamente, sem esperar que toda a resposta termine de carregar.

### Citações e transparência da origem

Cada resposta do Assistente de IA inclui citações vinculadas diretamente ao curso, módulo ou objeto de aprendizado original. As citações permitem:

* Selecione um número de citação embutido para ir para a seção referenciada exata
* Abrir a lista completa de fontes selecionando Mostrar fontes na parte inferior da resposta
* Verifique as informações e explore o contexto adicional da fonte oficial

>[!IMPORTANT]
>
>O Assistente do AI fornece respostas com base no conteúdo ativado pelo administrador, mas se um usuário não tiver acesso a um item referenciado, ele verá uma mensagem de “não compatível” ao abri-lo.


## Prompts internos

O Assistente de IA inclui prompts incorporados para ajudar os alunos a começar rapidamente com perguntas e cenários comuns. Esses prompts orientam os alunos sobre como interagir com o assistente e demonstram os tipos de perguntas que podem ser feitas.

![Prompts internos fornecidos pelo Assistente de Aluno](assets/built-in-prompt-new.png)

Os prompts internos são personalizáveis por conta. As organizações podem personalizá-los para refletir seus objetivos de aprendizado, funções do aluno, terminologia ou casos de uso específicos. Os administradores podem trabalhar com o Gerente de sucesso do cliente (CSM) para configurar ou atualizar prompts incorporados.

A personalização do prompt é gerenciada no nível da conta e não é configurável diretamente na interface de usuário do Adobe Learning Manager na versão atual.

## Configuração do administrador - Ativar o assistente do AI para alunos

![Assistente de aluno habilitado por IA](assets/learner-ai-assistant-new.png)

Os administradores selecionam quais grupos de usuários e catálogos internos podem acessar o recurso Assistente do AI. Eles devem garantir que os catálogos atribuídos incluam apenas o conteúdo de aprendizado apropriado para ser revelado em respostas e citações de IA e que esses catálogos sejam Padrão, Interno, não Compartilhado, Adquirido ou Externo.

Antes de configurar o Assistente do AI, confirme se você tem credenciais de administrador e identificou quais grupos de usuários e catálogos devem ter acesso ao recurso.

### Configurar acesso ao Assistente do AI

Para ativar o Assistente de IA do aluno:

1. Faça logon no Adobe Learning Manager como administrador.

2. Selecione **Configurações** na home page.
   ![Console do administrador com a opção Configurações no painel esquerdo](assets/settings-menu.png)

3. Selecione **Assistente de IA do aluno (Beta)** no menu **Configurações**.
   ![O console do administrador exibe a opção Assistente de IA do aluno no painel esquerdo](assets/learner-assistant-ai-beta.png)

4. Selecione a opção de alternância para habilitar o **Assistente de IA do aluno (Beta)**.
   ![O console de administradores exibe a alternância habilitada para o Assistente de IA do aluno](assets/learner-assistant-toggle.png)

5. Selecione um ou mais grupos de usuários da opção **Grupos de usuários qualificados**.

6. Selecione **Salvar** para aplicar as configurações do grupo de usuários.

7. Selecione um ou mais catálogos da opção **Catálogos qualificados**.

8. Selecione **Salvar** para aplicar as configurações do catálogo.

>[!IMPORTANT]
>
>O Assistente do AI oferece suporte somente a catálogos internos. Se um catálogo compartilhado, adquirido, externo ou outro não interno for selecionado, seu conteúdo não será revelado pelo Assistente do AI, mesmo se o catálogo for exibido na lista Catálogos qualificados.

## Guia do aluno - Iniciar o assistente de IA

### Iniciar o Assistente do AI

Para iniciar o Assistente do AI:

1. Faça logon no Adobe Learning Manager como aluno.

2. Selecione **Perguntar ao assistente de IA** na página inicial.
   ![A página inicial do aluno exibe Perguntar ao assistente de IA para selecionar e abrir o painel Assistente de IA do aluno](assets/ask-ai-assistant.png)

3. Quando a tela **Assistente de IA do aluno** for exibida, selecione **Introdução**.
   ![Selecione Começar para iniciar o Assistente de Aluno](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>Ao iniciar o Assistente do AI pela primeira vez, você deve dar seu consentimento antes de usá-lo. A caixa de diálogo de consentimento será exibida somente durante essa primeira inicialização. Para todas as inicializações subsequentes, você será direcionado ao Assistente do AI para inserir seus prompts.

&#x200B;4. Digite seu prompt no campo de texto.

![Digite o prompt no Assistente do aluno](assets/type-prompt-new.png)

5.Pressione **Enter** para receber uma resposta. Revise suas respostas, fontes e recomendações.

Você pode:

* Selecionar o número de citação embutido para saltar para a seção referenciada exata
* Abra a lista completa de fontes selecionando **Mostrar fontes** na parte inferior da resposta

![Exibir fontes na resposta](assets/show-sources-latest.png)

O Assistente de IA inclui citações em todas as respostas para mostrar de onde vêm as informações. Cada citação está vinculada diretamente ao curso, módulo ou objeto de aprendizado original usado para gerar a resposta.

Você pode selecionar qualquer citação para abrir a página do curso real no Adobe Learning Manager e revisar o conteúdo completo no contexto. As citações ajudam a verificar as informações, explorar detalhes adicionais e continuar aprendendo com a fonte confiável.

## Acessar o Assistente do AI por meio de pesquisa

Você também pode iniciar o Assistente do AI diretamente da barra de pesquisa. Digite sua pergunta no campo de pesquisa e selecione **Perguntar ao assistente de IA** nas opções que parecem obter respostas do conteúdo de aprendizado atribuído. O conteúdo de aprendizado atribuído.

![Acessar o Assistente de Aluno na barra de pesquisa](assets/learner-assistant-search-new.png)


## Fornecer feedback sobre as respostas do Assistente de IA do aluno

Seus comentários sobre as respostas geradas pelo Assistente de IA do aluno (Beta) ajudam a melhorar a precisão, a relevância e o desempenho geral.

### Curtir ou não curtir uma resposta

* Selecione **Miniaturas**, escolha o que achou útil na resposta, opcionalmente adicione comentários e selecione **Enviar**.

![Selecione Miniaturas para votar em uma resposta](assets/la-feedback.png)

* Selecione **Miniaturas**, escolha o motivo pelo qual a resposta não foi útil, adicione comentários e selecione **Enviar**.

## Iniciar um novo bate-papo no Assistente do AI

Iniciar um novo bate-papo permite que o usuário inicie uma nova conversa, limpando o contexto anterior para que o assistente possa se concentrar no novo tópico sem fazer referência a interações anteriores. Isso é importante ao alternar tópicos ou procurar respostas não relacionadas a perguntas anteriores.

Limpar a conversa atual e iniciar um novo chat a qualquer momento.

Selecione **Novo bate-papo** na tela do Assistente de IA e selecione **Sim**.

![Iniciar um novo chat no Assistente do Aluno](assets/start-new-chat.png)

O Assistente de IA fornece aos alunos respostas rápidas e contextuais, é compatível com vários tipos de conteúdo e oferece citações embutidas para transparência. Os administradores podem controlar o acesso, garantindo que o Assistente de IA esteja adaptado às necessidades organizacionais e aprimore a experiência de aprendizado.


## Solução de problemas

>[!NOTE]
>
>Após configurar um novo catálogo, aguarde de 4 a 5 horas para que o conteúdo seja indexado e fique disponível para respostas do Assistente do AI.

### Cenário 1: Sem acesso ao conteúdo

Problema: o aluno tem acesso ao Assistente de aluno, mas recebe respostas do tipo &quot;Não tenho uma resposta para esta pergunta&quot;.

**Causas possíveis**

* Os catálogos do aluno não são incluídos ao configurar o AI Assistant
* O conteúdo relacionado à pergunta não está nos catálogos selecionados ou os catálogos estão em branco
* O aluno não tem visibilidade do conteúdo relevante

**Solução**

* Verificar o acesso ao catálogo do aluno
* Verificar quais catálogos estão ativados nas configurações do Assistente do aluno
* Verifique se o conteúdo relevante existe nesses catálogos
* aguarde algumas horas após adicionar novo conteúdo para que ele seja indexado

### Cenário 2: respostas irrelevantes ou de baixa qualidade

**Problema**: o Assistente de IA fornece respostas que não correspondem à pergunta ou são de baixa qualidade.

**Causas possíveis**

* A pergunta é muito ampla ou ambígua
* O conteúdo relevante tem metadados inadequados (descrições, tags)
* A estrutura do conteúdo dificulta a extração de informações

**Solução**

* Incentivar os alunos a fazer perguntas mais específicas
* Revisar e melhorar as descrições e os metadados do curso
* Garantir que o conteúdo tenha cabeçalhos e estrutura claros
* Revisar o relatório detalhado de uso para identificar padrões
* Considere criar ajudas de tarefa para perguntas frequentes

### Cenário 3: perguntas fora do escopo

**Problema**: o aluno faz perguntas não relacionadas ao conteúdo do treinamento.

**Exemplos**:

* Perguntas de conhecimento geral (&#39;Quem é o presidente?&#39;)
* Opiniões pessoais (&#39;O que você pensa sobre X?&#39;)
* Conteúdo inadequado
