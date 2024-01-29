---
description: Saiba como baixar a transcrição do aluno baseada nos usuários, nos objetos de aprendizado ou nas habilidades no Learning Manager.
jcr-language: en_us
title: Transcrições do aluno
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 0%

---



# Transcrições do aluno

Saiba como baixar a transcrição do aluno baseada nos usuários, nos objetos de aprendizado ou nas habilidades no Learning Manager.

O Adobe Learning Manager permite que os gerentes de uma empresa gerem transcrições associadas aos alunos.

## Gerar transcrições do aluno {#generatelearnertranscripts}

1. Para gerar transcrições do aluno, clique em **[!UICONTROL Relatórios]** no painel esquerdo de login do Gerente.
1. Clique em **[!UICONTROL Meus Relatórios]** na página.
1. Clique em **[!UICONTROL Transcrições do aluno]** link.

   ![](assets/learner-transcripts.png)

   *Criar relatórios para transcrições do aluno*

1. Uma caixa de diálogo de transcrições do aluno é exibida. Escolha o intervalo de datas para o qual você precisa da transcrição gerada.

   >[!NOTE]
   >
   >Por padrão, a data inicial é a data de registro do aluno e a data final é sempre a data atual. É possível modificar apenas a data inicial a partir de quando você precisa dos dados.

1. Escolha os nomes dos alunos no campo Selecionar alunos e clique em **[!UICONTROL Gerar]**.

Você pode escolher um único aluno ou grupos de alunos. Para adicionar mais de um aluno, clique em Adicionar mais alunos.

As transcrições são geradas e baixadas no computador como arquivos .xls. Cada arquivo .xls excel tem sete folhas, cujos detalhes são mencionados abaixo:

## Baixar transcrição do aluno com base no fuso horário {#lt-timezone}

Como um administrador, um gerente também pode escolher as colunas a serem exportadas. Além disso, um gerente pode baixar a transcrição do aluno com base no fuso horário selecionado nas configurações do perfil.

Se o gerente ativar essa opção, o fuso horário será selecionado no conjunto da página de configurações do perfil, mostrada abaixo.

>[!NOTE]
>
>Para um novo gerente, a caixa de seleção Fuso horário é desativada.

![](assets/image030.png)

*Baixar transcrições do aluno para um fuso horário*

## Conteúdo do arquivo de transcrição do aluno {#learnertranscriptfilecontent}

Um arquivo de transcrição do aluno típico consiste em seis planilhas do Excel em um único arquivo. As folhas de transcrição do aluno fornecem uma visão geral dos dados, incluindo o número de alunos envolvidos por curso, suas habilidades, a porcentagem de conclusão com base no curso ou aluno e um painel de conformidade. Estes são os painéis disponíveis nas transcrições do aluno:

**Transcrição do aluno**

Na folha de excel de transcrição do aluno, juntamente com os detalhes do perfil sobre o aluno, são fornecidos detalhes de consumo de objetos de aprendizado, como data de inscrição, data de início, nota obtida, pontuação do questionário obtida e assim por diante. Se os cursos fizerem parte de qualquer programa de aprendizado, eles serão listados separadamente, além dos detalhes de consumo individuais do curso.

**1 - Painel da atividade de aprendizado**

Neste painel específico do OA, você pode ver o número de alunos de cada curso, programa de aprendizado ou certificação. Você pode exibir a planilha de progresso dos alunos de um objeto de aprendizado específico. Essa planilha exibe dados como o número de alunos que concluíram o curso ou o programa de aprendizado, os alunos em andamento e as datas de vencimento dos alunos.

O progresso dos usuários para o curso específico é calculado com base nos Campos de entrada, onde você especifica a data de vencimento e os limites de porcentagem de progresso. Por exemplo, se você especificar 7 dias e 70% como valores no campo de entrada, é exibido o progresso do curso para os cursos vencidos em 7 dias, e para os cursos que têm mais de 70% de progresso. Você também pode alterar o período nesta planilha, em que os dados modificados são exibidos automaticamente neste painel.

**2 - Painel da atividade de aprendizado**

Esse painel de aprendizado exibirá dados para um usuário específico. Nesse painel, você pode ver os cursos, programas de aprendizado ou certificações nos quais um usuário específico se inscreveu. A tabela também exibe dados sobre quais objetos de aprendizado o usuário concluiu, os objetos de aprendizado em andamento e as datas de vencimento iminentes do usuário.

O progresso dos usuários em cada curso é calculado com base nas entradas especificadas. Ou seja, os valores de data de vencimento e porcentagem de andamento. Por exemplo, se você especificar 7 dias e 70% como valores no campo de entrada, é exibido o progresso de cursos diferentes para os cursos vencidos em 7 dias, e para os cursos que têm mais de 70% de progresso.

**Habilidade**

Na planilha de habilidades, são fornecidos o nome da habilidade, o nível de habilidade, os créditos necessários, os créditos ganhos, a porcentagem de conclusão e outros detalhes do perfil. Um instantâneo de amostra da planilha habilidades do Excel é fornecido abaixo para referência.

**Painel de habilidade**

Nesse painel, você pode ver se sua organização está equipada com várias habilidades. Para uma habilidade específica, você pode verificar o número de usuários em uma organização que devem ter essa habilidade em comparação com o número que realmente tem a habilidade. Esse painel também especifica os usuários que podem precisar atualizar suas habilidades. Esse valor é calculado com base na entrada inserida no campo Entrada. Por exemplo, se você inserir 50 dias como entrada, o painel fornecerá dados sobre usuários que podem precisar atualizar suas habilidades após 50 dias.

Esse painel de habilidades é mais específico do usuário. Você pode filtrar um usuário específico ou vários usuários e exibir seu nível de habilidade como um painel. Essa planilha pode ajudar gerentes e administradores a controlar o nível de qualificação de cada aluno em comparação com o nível de qualificação esperado. O painel Habilidade também ilumina os alunos que precisam atualizar suas habilidades. A lista de atualização de alunos é calculada com base no número de dias inserido no campo de entrada.

**Painel de Conformidade**

O Painel de conformidade tem duas partes: relatório de conformidade por usuário e relatório de conformidade por treinamento. Para o relatório baseado no usuário, você pode usar o Painel de Conformidade para rastrear usuários com datas de vencimento iminentes para iniciativas de conformidade importantes. Para o relatório baseado em treinamento, você pode filtrar por programa de aprendizado ou certificação.

Para ambos os relatórios de conformidade, filtre pela data de vencimento para exibir os dados apropriados.
