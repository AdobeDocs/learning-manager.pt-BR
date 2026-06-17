---
jcr-language: en_us
title: Aplicar agrupar por e agregações em Report Builder
description: Resuma os dados do relatório do Adobe Learning Manager por um campo escolhido e calcule contagens, totais e porcentagens nas linhas agrupadas.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---


# Aplicar agrupar por e agregações em Report Builder

Agrupar por e agregação permitem produzir relatórios sumariados, como total de conclusões por professor, contagem de inscrições por catálogo ou porcentagem de conformidade por região.

## Quando usar Agrupar por

Use agrupar por quando desejar uma linha por categoria em vez de uma linha por registro. Por exemplo:

* Uma linha por professor, mostrando quantas sessões eles ensinaram
* Uma linha por catálogo, mostrando o total de inscrições
* Uma linha por grupo de usuários, mostrando o percentual de conformidade

Se quiser ver registros individuais do aluno ou linhas de inscrição individuais, não aplique agrupar por.

Quando você aplica agrupar por a uma coluna, todas as outras colunas do relatório devem ter uma função agregada aplicada. Não é possível mostrar um valor de campo bruto ao lado de uma coluna agrupada, apenas um valor calculado (contagem, soma, média etc.).

Por exemplo, se você agrupar por **Nome do professor**, não poderá mostrar valores individuais de **Nome da sessão** junto com ele. Em vez disso, você aplicaria **Contagem** ao campo **ID da Sessão** para mostrar quantas sessões cada professor ensinou.

## Aplicar agrupar por e agregações

Neste exemplo, você comparará o progresso da inscrição entre os alunos. Use este relatório para entender como os diferentes gerentes estão se saindo em termos de andamento e conclusão da inscrição.

### Selecionar colunas

1. Inicie o **Report Builder** e selecione **Criar Relatório**.
2. Digite o nome e a descrição do relatório:
a) **Nome:** Comparar progresso de inscrição entre usuários
b) **Descrição:** este relatório agrupa alunos por gerente e calcula métricas resumidas, como total de alunos, progresso médio e contagens de conclusão para o status da inscrição=CONCLUÍDO
3. Selecione as seguintes colunas: `<dataset>:<column name>`
a) Nome de Usuário\Gerente
b) Usuário\Nome
c) Inscrição\Status
d) Percentual de Inscrição\Andamento
e) Objeto de aprendizado\Contagem de conclusão

### Selecionar Agrupar por colunas

1. Selecione as seguintes colunas na seção **Agrupar por**:
a. Inscrição\Status
b. Nome do usuário\gerente
   ![](assets/image020.jpg)
2. Selecione **Aplicar**.

### Selecionar colunas a serem agregadas

As funções agregadas resumem o desempenho da inscrição do aluno por gerente e o status da inscrição, mostrando contagens distintas de alunos, porcentagens médias de progresso do treinamento e contagens médias de conclusão do objeto de aprendizado nos registros de treinamento agrupados.

1. Selecione **Contagem Distinta** para Usuário\Nome.
2. Selecione **Média** para o Percentual de Inscrição\Progresso.
3. Selecione **Média** para Objeto de Aprendizado\Contagem de Conclusão.
   ![](assets/image021.png)

### Aplicar filtros

Aplique filtros para incluir apenas inscrições concluídas e exclua registros com nomes de gerentes ausentes, garantindo que o relatório analise dados válidos do aluno para obter informações precisas sobre o progresso e a conclusão do treinamento de cada gerente.

1. Aplique um filtro em que _Enrollment-Status_ seja igual a _Concluído_.
2. Aplique um segundo filtro em que _Nome do Gerenciador de Usuários_ não esteja vazio.
3. Combine ambos os filtros usando a condição AND para incluir apenas registros válidos de aluno concluído.

### Salvar e baixar o relatório

Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório. Você receberá uma notificação para baixar o relatório no formato .csv assim que estiver pronto.

O CSV contém um resumo de gerentes sobre inscrições de alunos concluídas e o progresso do treinamento. Cada linha representa um gerente e inclui contagens de alunos, status da inscrição, porcentagem média de progresso e contagens médias de conclusão.

Em geral, o relatório compara a conclusão do treinamento e a atividade de aprendizado entre os gerentes, destacando as diferenças no envolvimento do aluno e o número de objetos de aprendizado concluídos.
