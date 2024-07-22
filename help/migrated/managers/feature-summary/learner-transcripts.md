---
description: Saiba como baixar a transcrição do aluno baseada nos usuários, nos objetos de aprendizado ou nas habilidades no Learning Manager.
jcr-language: en_us
title: Transcrições do aluno
exl-id: 8204aa1e-0e0d-4d9e-9dc0-6260667bf4e7
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 85%

---

# Transcrições do aluno

Saiba como baixar a transcrição do aluno baseada nos usuários, nos objetos de aprendizado ou nas habilidades no Learning Manager.

O Adobe Learning Manager permite que os gerentes de uma empresa gerem transcrições associadas aos alunos.

## Gerar transcrições do aluno {#generatelearnertranscripts}

1. Para gerar transcrições do aluno, clique em **[!UICONTROL Relatórios]** no painel esquerdo de login do gerente.
1. Clique na guia **[!UICONTROL Meus Relatórios]** na página.
1. Clique no link **[!UICONTROL Transcrições do aluno]**.

   ![](assets/learner-transcripts.png)

   *Criar relatórios para transcrições do aluno*

1. É exibida a caixa de diálogo Transcrições do aluno. Escolha o intervalo de datas das quais você precisa que a transcrição seja gerada.

   >[!NOTE]
   >
   >Por padrão, a data inicial é a data de registro do aluno e a data final é sempre a data atual. É possível modificar apenas a data inicial a partir de quando você precisa dos dados.

1. Escolha os nomes dos alunos no campo Selecionar alunos e clique em **[!UICONTROL Gerar]**.

É possível escolher um único aluno ou grupos de alunos. Para adicionar mais de um aluno, clique em Adicionar mais alunos.

As transcrições são geradas e baixadas no seu computador como arquivos de .xls. Cada arquivo .xls excel tem sete folhas, cujos detalhes são mencionados abaixo:

## Baixar transcrição do aluno com base no fuso horário {#lt-timezone}

Como um administrador, um gerente também pode escolher as colunas a serem exportadas. Além disso, um gerente pode baixar a transcrição do aluno com base no fuso horário selecionado nas configurações do perfil.

Se o gerente ativar essa opção, o fuso horário será selecionado no conjunto da página de configurações do perfil, mostrada abaixo.

>[!NOTE]
>
>Para um novo gerente, a caixa de seleção Fuso horário é desativada.

![](assets/image030.png)

*Baixar transcrições do aluno para um fuso horário*

## Conteúdo do arquivo de transcrição do aluno {#learnertranscriptfilecontent}

Um arquivo típico de transcrição do aluno consiste em seis planilhas do Excel em um único arquivo. As planilhas de transcrição do aluno oferecem uma ideia total dos dados, incluindo o número de alunos envolvidos por curso, suas habilidades, a porcentagem de concorrência com base no curso ou no aluno e um painel de conformidade. Estes são os painéis disponíveis nas transcrições do aluno:

**Transcrição do aluno**

Na planilha do Excel de transcrição do aluno, junto com os detalhes do perfil sobre o aluno, são fornecidos detalhes de consumo inteligentes do objeto de aprendizado, como data de inscrição, data inicial, classificação alcançada, pontuação obtida no questionário e assim por diante. Se os cursos fizerem parte de qualquer programa de aprendizado, serão listados separadamente em relação aos detalhes individuais do consumo do curso.

**1 - Painel da atividade de aprendizado**

Nesse painel específico do objeto de aprendizado, é possível ver o número de alunos de cada curso, programa de aprendizado ou certificação. Você pode visualizar a planilha de progresso dos alunos de um objeto de aprendizado específico. Esta página exibe dados como o número de alunos que concluíram o curso ou o programa de aprendizado, os alunos em andamento e as datas de vencimento dos alunos.

O progresso dos usuários para o curso especificado é calculado com base nos Campos de entrada, onde você especifica os limites da porcentagem da data de vencimento e do progresso. Por exemplo, se você especificar 7 dias e 70% como valores no campo de entrada, é exibido o progresso do curso para os cursos vencidos em 7 dias, e para os cursos que têm mais de 70% de progresso. Você também pode alterar o período nesta planilha, na qual os dados modificados são automaticamente exibidos nesse painel.

**2 - Painel da atividade de aprendizado**

Esse painel de aprendizado exibirá os dados de um usuário específico. Nesse painel, é possível visualizar os tutoriais, os programas de aprendizado ou as certificações em que um determinado usuário se inscreveu. A tabela também exibe os dados sobre os objetos de aprendizado concluídos pelo usuário, os objetos de aprendizado em andamento e as próximas datas de vencimento do usuário.

O progresso dos usuários para cada curso é calculado com base nas entradas que você especificar. Isto é, os valores de porcentagem da data de vencimento e do progresso. Por exemplo, se você especificar 7 dias e 70% como valores no Campo de entrada, é exibido o progresso de cursos diferentes para os cursos vencidos em sete dias, e para os cursos que têm mais de 70% de progresso.

**Habilidade**

Na planilha Habilidades, são fornecidos o nome e o nível de habilidade, os créditos exigidos, os créditos necessários, a porcentagem de conclusão e outros detalhes do perfil. Para referência, é fornecido abaixo um instantâneo de exemplo da planilha do Excel de habilidades.

**Painel de habilidade**

Nesse painel, é possível ver se a sua organização está equipada em várias habilidades.  Para uma habilidade específica, você pode verificar o número de usuários em uma organização que deve ter essa habilidade em comparação com o número que tem realmente a habilidade. Esse painel também especifica os usuários que podem precisar atualizar suas habilidades. Esse valor é calculado com base na entrada inserida no campo de entrada. Por exemplo, se você inserir 50 dias como sua entrada, o painel fornece dados sobre os usuários que podem precisar de suas habilidades atualizadas após o período de 50 dias.

Este painel de habilidade é mais específico ao usuário. É possível filtrar um usuário específico ou vários usuários e visualizar seu nível de habilidade como um painel. Esta página pode ajudar os gerentes e administradores a controlarem o grau de habilidade de cada aluno em comparação ao que se espera dele. O painel Habilidade também ajuda a identificar os alunos que precisam atualizar suas habilidades. A lista de atualização de alunos é calculada com base no número de dias inserido no campo de entrada.

**Painel de conformidade**

O painel de conformidade tem duas partes: relatório de conformidade por usuário e relatório de conformidade por treinamento. No relatório baseado em usuário, você pode usar o painel de conformidade para controlar os usuários cujas datas de vencimento de iniciativas importantes de conformidade estão próximas. No relatório baseado em treinamento, você pode filtrar por certificação ou programa de aprendizado.

Em ambos os relatórios de conformidade, filtre pela data de vencimento para ver os dados apropriados.
