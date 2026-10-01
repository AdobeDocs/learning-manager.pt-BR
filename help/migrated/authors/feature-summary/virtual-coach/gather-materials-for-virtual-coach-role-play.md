---
description: Saiba quais documentos, contexto e detalhes do prompt devem ser preparados antes de criar uma função de treinador virtual com o assistente de IA
jcr-language: en_us
title: Reúna materiais para uma interpretação de coach virtual
exl-id: 1a119554-af8d-445a-9c19-010dafd3e7ab
source-git-commit: 8bde6827835a7f8cd8cc28f3d2c4014527e4a96c
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%
---

# Reúna materiais para uma interpretação de coach virtual

Use essa referência para preparar os documentos, o contexto e os detalhes do prompt necessários para uma interpretação do Virtual Coach antes de começar a criar.

O assistente Virtual Coach AI faz o trabalho pesado: escreve seu cenário, constrói sua personalidade e gera seus critérios de avaliação. Para fazer isso bem, ele precisa entender para que você está treinando. Quanto mais contexto você trouxer, melhor será o seu papel. O Virtual Coach não usa automaticamente o conteúdo do curso do Adobe Learning Manager existente na sua organização. Você deve fornecer materiais de referência ou um prompt para cada interpretação que criar.

## Documentos para trazer

O assistente de IA pode usar qualquer material que você compartilhar. A tabela a seguir mostra para que cada tipo de documento é mais útil.

| Tipo de documento | Formatos aceitos | O que ele ajuda a criar |
|---|---|---|
| Gravações ou transcrições de chamadas | MP4, WAV, WEBM | Cenário e contexto da conversa |
| Guias sobre playbooks, falas ou como lidar com objeções | PDF, DOCX | As preocupações e objeções da pessoa |
| Apresentação de produtos para um único pager ou apresentações | PPTX, PDF, DOCX | O que o aluno deve apresentar e explicar |
| Personalidade do comprador ou perfis de cliente ideais | PDF, DOCX | A função, o tom e as prioridades da pessoa |
| Rubricas de pontuação ou estruturas de orientação | PDF, DOCX, CSV | Critérios de avaliação e classificação |

Cada tipo de documento alimenta uma parte diferente da interpretação de função gerada por IA. Portanto, trazer mais de um tipo produz um cenário mais completo.

>[!NOTE]
>
>Os tipos de arquivo aceitos são PDF, DOCX, PPTX, TXT, CSV, MP4, WAV e WEBM. Você pode fazer upload de até 20 arquivos por sessão, até 200 MB por arquivo. Se você fizer upload de mais de 20 arquivos, somente os primeiros 20 serão processados; o restante será ignorado sem aviso. Arquivos do Excel (.xlsx) não são compatíveis — exporte o conteúdo .xlsx para CSV antes de fazer upload.

>[!TIP]
>
>Até mesmo notas ásperas ou pontos de marcador ajudam. Você não precisa de documentos refinados, apenas de contexto suficiente para que a IA entenda seu cenário e suas metas de treinamento.

## Quatro perguntas para pensar

Você não precisa de respostas completas por escrito para estas perguntas. Apenas venha com o seu pensamento. O assistente de IA faz perguntas de acompanhamento e ajuda você a preencher as lacunas.

**Qual é o cenário?**
Qual é a situação dos negócios, e por que essas duas pessoas estão falando? Pense sobre o contexto, o estágio de relacionamento, e o propósito da chamada. Por exemplo, uma primeira chamada para detecção, um acompanhamento após uma demonstração, uma conversa de renovação ou uma sessão interna de treinamento.

**Quem é a persona?**
Com quem o aluno falará? Pense sobre o título, a atitude, o estilo de comunicação da pessoa e quais pressões ou prioridades moldam como ela aparece. Por exemplo, um vice-presidente de vendas cético, um Director de TI com orçamento restrito ou um líder de RH colaborativo, mas distraído.

**Qual é o objetivo da conversa?**
Como é uma conversa de sucesso e o que o aluno deve realizar até o final? Pense sobre o resultado em que você está treinando, não apenas os tópicos. Por exemplo, descubra problemas, ganhe uma reunião de acompanhamento, apresente uma proposta personalizada ou lide com uma objeção específica e avance o negócio.

**Como o aluno será graduado?**
Quais são as três a seis principais habilidades ou comportamentos que definem um ótimo desempenho nesta conversa? Pense em ações verbais específicas que você gostaria de ouvir em uma transcrição, não em traços de atitude ou personalidade. O “valor discutido” é vago. “Explicamos como a plataforma reduz o tempo de integração em 40%” é escalonável.

Consulte nosso [guia de design](/help/migrated/authors/feature-summary/virtual-coach/role-play-design.md) para saber mais sobre como criar uma interpretação de funções.

## Lista de verificação rápida antes de iniciar

- Você tem pelo menos um documento ou cenário que pode descrever para compartilhar com o assistente do AI.
- Você conhece o cenário geral e o contexto do relacionamento.
- Você pode descrever a função, o tom e a preocupação principal da persona.
- Você sabe como um resultado bem-sucedido se parece para o aluno.
- Você tem uma noção grosseira das habilidades ou comportamentos que deseja graduar.

## Modelo de prompt de práticas recomendadas

Use este modelo como ponto de partida ao escrever seu prompt inicial para o assistente do AI:

_Quero criar uma única [conversa do tipo ] com foco em [habilidade, produto, proposta, processo ou conversa comercial]. O cenário deve colocar o aluno, uma [função/título do aluno] na [empresa ou equipe do aluno], em uma [configuração de conversa] com [nome pessoal ou tipo pessoal], uma [função/título pessoal] no [tipo de empresa ou organização pessoal]. A conversa está acontecendo porque [acionador comercial realista, evento anterior, necessidade do cliente, contexto de mercado ou estágio de relação]._

_A função deve testar se o aluno pode [realizar a tarefa principal naturalmente no momento], ao mesmo tempo que [habilidade secundária ou comportamento de conversa]. O desempenho sólido deve soar [para descrever o estilo de comunicação desejado: natural, consultivo, executivo, conciso, empático, comercialmente relevante e assim por diante] e deve incluir [mensagens principais, áreas de descoberta, pontos de prova, perguntas, manipulação de objeções ou comportamento da próxima etapa]. A simulação deve premiar [comportamentos observáveis específicos a serem incentivados] e evitar a recompensa de [lançamentos genéricos, descobertas vagas, dumping de produtos, conversações excessivas, linguagem de script, descobertas ignoradas, fechamento fraco etc.]._

**Exemplo, usando o caso de uso de prontidão para lançamento do produto:** _”Quero criar uma única apresentação de papéis de várias pessoas com foco no posicionamento do nosso novo complemento de segurança para um comitê de compra de empresas. O cenário deve colocar o aluno, um executivo de conta em nossa empresa, em uma reunião programada para análise da solução com quatro partes interessadas em uma empresa de logística de médio porte: um CFO com foco no ROI, um gerente de compras com foco nos termos do contrato, um Director de TI com foco na segurança e na integração e um especialista em usuários finais com foco na usabilidade diária. A conversa está acontecendo porque o cliente está avaliando o complemento antes da renovação do contrato.”_

Assim que você tiver seus documentos e respostas prontos, continue [criando e publicando uma função de treinador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md).
