---
jcr-language: en_us
title: Classificar colunas do relatório no Report Builder
description: Aplique classificação de coluna única ou múltipla no Adobe Learning Manager Report Builder para controlar a ordem das linhas dos relatórios baixados.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Classificar colunas do relatório no Report Builder

A classificação determina a ordem das linhas no arquivo de relatório baixado. Aplique a classificação sempre que um resultado consistente for importante.

## Adicionar uma classificação

Neste exemplo, você encontrará os cursos com as conclusões mais altas.

1. Inicie o Report Builder e selecione **Criar Relatório**.
2. Digite o nome e a descrição do relatório.
3. Selecione as seguintes colunas: `<dataset>:<column name>`
a) Objeto de aprendizado - Nome do objeto de aprendizado
b) Objeto de aprendizado - Status do objeto de aprendizado
c) Objeto de aprendizado - Contagem de conclusão
4. Na seção Classificação, selecione **Adicionar classificação**.
5. Selecione **Objeto de Aprendizado - Contagem de Conclusão**.
6. Selecione uma ordem de classificação **Crescente** ou **Decrescente**.
   ![](assets/image032.jpg)
7. Selecione **Adicionar**.
8. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

O relatório baixado lista todos os registros, classificados pelo número de conclusões do curso.

## Adicionar classificação de várias colunas

Neste exemplo, você gerará um relatório para medir o desempenho entre gerentes.

Para classificar por mais de uma coluna:

1. Inicie o **Report Builder** e selecione **Criar Relatório**.
2. Digite o nome e a descrição do relatório.
3. Selecione as seguintes colunas: `<dataset>:<column name>`
a) Usuário - Nome
b) Usuário - Nome do Gerente
c) Transcrição do módulo - Status
d) Transcrição do módulo - Percentual de andamento
4. Adicione os seguintes agregados:
a. Agrupar por Usuário - Nome do Gerente
b. Contar Usuário Distinto - Nome
c. Count If=Transcrição COMPLETA do módulo - Status
d. Transcrição média do módulo - Percentual de andamento
   ![](assets/image033.png)
5. Na seção **Classificar**, adicione a seguinte classificação de várias colunas:
a. Transcrição do módulo - Status: Decrescente
b. Usuário - Nome do Gerente: Crescente
   ![](assets/image034.jpg)
6. Selecione Salvar relatório e Ações > Baixar para baixar o relatório.

O relatório baixado fornece um resumo do desempenho do gerente, mostrando contagens distintas de alunos, contagens de inscrições baseadas no status e porcentagens médias de progresso. Ele destaca os níveis de participação e o progresso do treinamento nos diferentes grupos de gerentes.
