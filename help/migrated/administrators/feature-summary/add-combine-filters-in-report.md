---
jcr-language: en_us
title: Adicionar e combinar filtros em um relatório
description: Restrinja os dados de relatório no Adobe Learning Manager Report Builder usando filtros únicos, lógica AND / OR e grupos de filtros aninhados.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---


# Adicionar e combinar filtros em um relatório

## Visão geral

Os filtros permitem definir o escopo do relatório exatamente para os registros necessários. Você pode aplicar um único filtro, combinar vários filtros com a lógica AND ou OR e criar grupos aninhados para condições complexas.

## Adicionar um filtro

Use filtros para limitar seu relatório a um subconjunto específico de dados em vez de exibir tudo.

Por exemplo, você pode querer entender quantos alunos se inscreveram nos cursos nos últimos 365 dias. Nesse caso, aplique um filtro de data na data de inscrição para incluir apenas atividades recentes.

1. Inicie o Report Builder e selecione **Criar Relatório**.
2. Digite o nome e a descrição do relatório.
3. Selecione as seguintes colunas: <dataset>:<column name>

   * Inscrição - Data de Inscrição
   * Usuário - Nome

   ![](assets/report-builder-0024.png)

4. Na seção Relatórios, selecione **Adicionar filtro**.
5. Procure ou navegue até o campo pelo qual deseja filtrar. Neste exemplo, selecione **Inscrição - Data de Inscrição**.

   ![](assets/report-builder-0025.png)

6. Selecione **Adicionar**.
7. Selecione um operador. Os operadores disponíveis dependem do tipo de dados do campo:

   * Campos de sequência de caracteres - contém, é igual a, começa com
   * Campos numéricos - maior que, menor que, igual a, entre
   * Campos de data - igual a, antes, depois, entre, últimos N dias
   * Campos de lista (enum) - está em, não está em

8. Neste caso, selecione **está no último ano**.

   ![](assets/report-builder-0026.png)

9. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

O relatório baixado lista todos os usuários que se inscreveram em um Objeto de aprendizado nos últimos 365 dias.

## Adicionar vários filtros com a lógica AND / OR

Quando você adiciona um segundo filtro, a relação padrão entre os filtros é AND; ambas as condições devem ser verdadeiras para que uma linha seja exibida.

Por exemplo, você pode identificar os alunos que se inscreveram nos cursos nos últimos 365 dias E relatá-los a um gerente específico. Nesse caso, ambas as condições devem ser verdadeiras, de modo que os filtros são combinados usando a lógica AND.

1. Inicie o Report Builder e selecione **Criar Relatório**.
2. Digite o nome e a descrição do relatório.
3. Selecione as seguintes colunas: <dataset>:<column name>

   * Usuário - Nome
   * Usuário - Nome do Gerente
   * <span class="mark">Inscrição - Data de Inscrição</span>

4. Agrupar pela coluna **Nome do Gerenciador de Usuários**.
5. Na seção Filtro, selecione os seguintes filtros:

   * Inscrição - A data de inscrição é **s no último ano**
   * O Nome de Usuário - Gerente **começa com** N
   * O Nome de Usuário - Gerente **não está vazio**

     ![](assets/report-builder-0027.png)

6. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

O relatório baixado lista todos os usuários que se inscreveram em um Objeto de Aprendizado nos últimos 365 dias **e** relatam a um gerente cujo nome começa com N.

## Criar grupos de filtros aninhados

Os grupos aninhados permitem criar condições com vários níveis lógicos, equivalentes a colchetes em uma fórmula. Por exemplo: (Catálogo = Segurança OU Catálogo = Higiene) E a Data de conclusão está nos últimos 90 dias.

Use grupos de filtros aninhados quando a lógica incluir uma combinação de condições AND e OR que devem ser avaliadas em conjunto.

Por exemplo, use a lógica de filtro aninhado para identificar inscrições incompletas nas quais os alunos têm progresso abaixo de 50% ou treinamento vencido, demonstrando como as condições E e OU funcionam juntas.

1. Inicie o Report Builder e selecione **Criar Relatório**.
2. Digite o nome e a descrição do relatório.
3. Selecione as seguintes colunas: <dataset>:<column name>

   * Inscrição - Status
   * Inscrição - Percentual de Andamento
   * Inscrição - Vencida

     ![](assets/report-builder-0028.png)

4. Na seção **Filtro**, selecione os seguintes filtros:

   * O registro -Status **não é igual a nenhum de** Concluído.
   * Selecione +.
   * Procure por Percentual de Andamento da Inscrição.
   * Selecione o filtro.
   * Selecione **Adicionar como grupo**.

     ![](assets/report-builder-0029.png)

5. Adicionar Inscrição - Percentual de Progresso **menor que** 50.

   ![](assets/report-builder-0030.png)

6. Selecione +.
7. Pesquise por **Inscrição Atrasada**.
8. Selecione o filtro.
9. Selecione **Adicionar como grupo**.

   ![](assets/report-builder-0031.png)

10. Adicionar Inscrição Vencida é igual a VERDADEIRO.
11. Altere o AND aninhado para OR.

    ![](assets/report-builder-0032.png)

12. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

O relatório baixado lista todas as inscrições em andamento ou não iniciadas, cujo percentual de andamento seja inferior a 50% ou que estejam vencidas.
