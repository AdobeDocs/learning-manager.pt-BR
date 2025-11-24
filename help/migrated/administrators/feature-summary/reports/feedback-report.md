---
description: Saiba como acessar, baixar e interpretar o Relatório de feedback no Adobe Learning Manager. Entenda as colunas do relatório, os tipos de pergunta, as respostas do gerente e do aluno e como os insights de feedback apoiam a avaliação e o aprimoramento contínuo do treinamento.
jcr-language: en_us
title: Relatório de feedback no Adobe Learning Manager
source-git-commit: 6fceea6cc1f5fbe47e0dbb211cfb9e2de67957f6
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 8%

---


# Relatório de feedback

## Visão geral

O relatório de feedback no Adobe Learning Manager coleta o Nível 1 (feedback do aluno) e o Nível 3 (feedback do gerente) após os alunos concluírem os objetos de aprendizado. Este relatório apresenta uma visão geral estruturada das respostas subjetivas e objetivas dos alunos e seus gerentes.

O relatório acompanha os detalhes do aluno, como nome, e-mail, nome do formulário de feedback, versão e idioma, e captura respostas para perguntas definidas pelo administrador. Ele também registra a seleção do aluno para cada pergunta (por exemplo, Concordo totalmente, Concordo ou Discordo).

## Finalidade e benefícios

* Fornece insights acionáveis para melhorar a qualidade do curso e a eficácia geral do aprendizado.
* Refine os métodos de navegação, ritmo e entrega com base no feedback direto do usuário.

## Casos de uso

* **Identificar problemas de conteúdo rapidamente**: os administradores podem detectar classificações baixas ou comentários negativos repetidos e atualizar os objetos de aprendizado sem aguardar tíquetes de suporte ou escalonamentos.
* **Meça a eficácia do treinamento**: as equipes podem comparar o feedback do aluno em vários cursos ou versões para entender quais objetos de aprendizado estão tendo um bom desempenho e quais podem precisar retrabalhar.
* **Acompanhe o envolvimento do aluno com formulários de feedback**: os administradores podem ver quantos alunos estão respondendo ou ignorando perguntas, ajudando-os a refinar os formulários de feedback para melhorar a qualidade da resposta e as taxas de conclusão.

## Como baixar o relatório de feedback

1. Faça logon no Adobe Learning Manager como administrador.
2. Selecione **[!UICONTROL Relatórios]** no menu de navegação à esquerda.
   ![](assets/select-report.png)
   _A página inicial do Administrador mostra a opção Relatórios destacada para baixar relatórios_

3. Selecione **[!UICONTROL Relatórios Personalizados]** em Relatórios e selecione **[!UICONTROL Relatórios do Excel]**.
4. Selecione **[!UICONTROL Relatório de comentários]**.
   ![](assets/select-feedback-report.png)
   _A seção Relatórios Personalizados mostra a opção de selecionar Relatório de Comentários para acessar os dados de feedback do aluno e do gerente_

5. Selecione **[!UICONTROL Todos os treinamentos]** ou **[!UICONTROL Treinamentos selecionados]** e o intervalo de datas. Se selecionar a segunda opção, você pode adicionar até um máximo de 10 cursos ou caminhos de aprendizado e gerar o relatório de feedback. Além disso, você pode gerar o relatório por até um ano.
   ![](assets/feedback-report.png)
   _Configure o Relatório de Comentários selecionando o escopo do treinamento, definindo o intervalo de datas e escolhendo a opção de tradução antes de baixar_

6. Selecione o idioma para traduzir o feedback L1. As perguntas objetivas e suas respostas são traduzidas para o idioma selecionado quando essa versão do idioma é explicitamente definida. Somente as perguntas subjetivas que estão explicitamente definidas no idioma selecionado aparecem no relatório.  As respostas a perguntas subjetivas seriam na linguagem original de resposta.
7. Selecione **[!UICONTROL Baixar]** para baixar o relatório.

## O que o relatório de feedback contém

Estas são as colunas padrão no relatório no nível de conta:

| Coluna | Descrição |
|----|----|
| Tipo de feedback | Indica se o feedback é do aluno (L1) ou do gerente (L3) |
| Nome do usuário | Nome do aluno que concluiu o treinamento |
| E-mail do usuário | Endereço de e-mail do aluno |
| Id do treinamento | Um identificador exclusivo gerado pelo sistema atribuído a cada Objeto de aprendizado (curso, certificação ou caminho de aprendizado) |
| Nome do Treinamento | Nome do item de aprendizado para o qual o feedback é enviado |
| Instância do treinamento | Nome de instância do treinamento (para cursos de várias instâncias) |
| Tipo de Treinamento | Tipo de treinamento (curso, certificação, plano de aprendizado) |
| Tipo de formulário de feedback | Tipo/categoria do formulário de feedback usado (por exemplo, cursos mistos, cursos de ritmo individualizado e cursos em sala de aula) |
| Nome do formulário de feedback | Nome do formulário de comentários |
| Versão do feedback | Número de versão do formulário de feedback |
| Gerente atual | Nome do gerente do aluno |
| E-mail do gerente atual | Endereço de e-mail do gerente do aluno |
| Data de conclusão | A data em que o aluno concluiu o treinamento |
| Data do feedback | A data em que o aluno enviou o feedback |
| Idioma Original Do Feedback L1 | O idioma em que o aluno enviou originalmente o feedback L1 |

As seguintes colunas são exibidas no relatório no nível de conta com base nos quatro tipos de perguntas adicionados ao formulário de feedback:

| Coluna | Descrição |
|---|---|
| Eficácia do curso | A pergunta predefinida sobre eficácia do curso exibida no formulário |
| Resposta de eficácia do curso | A resposta do aluno à pergunta sobre a eficácia do curso |
| Pergunta NPS 1 | Pergunta da Primeira Pontuação de Promotor Líquido |
| Intervalo NPS 1 | Escala de classificação usada (por exemplo, 0 a 10) |
| Resposta NPS 1 | Classificação do aluno para Pergunta 1 do NPS |
| Pergunta Likert 1 | Primeira pergunta de escala Likert |
| Resposta Likert 1 | Resposta à Pergunta Likert 1 |
| Pergunta de Texto 1 | Primeira pergunta aberta/texto no formulário |
| Resposta de texto 1 | Resposta do aluno à Pergunta de Texto 1 |
| Pergunta 1 da Escala Likert L3 | Mede o desempenho do pós-treinamento do aluno usando uma escala de classificação |
| Resposta 1 da Escala Likert L3 | Resposta do gerente a esta pergunta da escala Likert |
| Pergunta 1 do Texto Livre do L3 | Pergunta de texto livre adicionada ao formulário de feedback N3 para gerentes. Pode ser configurada como opcional ou obrigatória. |
| Resposta 1 do Texto Livre L3 | A resposta do gerente a essa pergunta de texto livre |

>[!NOTE]
>
>O relatório no nível da conta também inclui todos os campos ativos configurados para alunos.

As seguintes colunas são exibidas no relatório de nível do Objeto de aprendizado:

| Coluna | Descrição |
|---|---|
| Aluno | Nome do aluno |
| Email | Endereço de e-mail do aluno |
| Nome do formulário de feedback | Nome do formulário de comentários |
| Versão do feedback | Número de versão do formulário de feedback |
| Idioma do aluno | Idioma selecionado pelo aluno |


