---
jcr-language: en_us
title: Monitorar envolvimento por grupo de usuários no Report Builder
description: Crie um relatório no Adobe Learning Manager Report Builder que mostre o tempo total gasto e as inscrições por grupo de usuários, agrupados por mês.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Monitorar envolvimento por grupo de usuários no Report Builder

Esse relatório ajuda os gerentes de treinamento e os administradores de pesquisa e desenvolvimento a identificarem quais grupos de usuários estão mais ativos e como o envolvimento tende a cada mês. Ele usa os conjuntos de dados **Grupo de Usuários de Campo Ativo** e **Registro** com funções de agregação e agrupar por para produzir uma linha de resumo por grupo de usuários por mês.

## Criar o relatório de envolvimento por grupo de usuários

1. Inicie o **Report Builder** e selecione **Criar Relatório**.
2. Digite um nome, por exemplo, _Compromisso por grupo de usuários MoM_.
3. No painel **Selecionar colunas**, expanda o **Grupo de Usuários do Campo Ativo** e selecione **+** ao lado do **Nome do Grupo de Usuários**. A coluna aparece no painel **Colunas Selecionadas**.
4. Expanda **Inscrição** e selecione **+** ao lado de **Data de Inscrição**.
5. Selecione **+** próximo a **Tempo Gasto**. Selecione o ícone de **editar** (lápis) e insira o alias _Tempo total gasto_.
6. Expanda o **Objeto de Aprendizado** e selecione **+** ao lado da **Contagem de Usuários de Inscrição**. Selecione o ícone de edição e insira o alias _Total de inscrições_.
7. Selecione **Agrupar por: selecione** na parte superior do painel **Colunas Selecionadas**.
8. Escolha **Inscrição - Data de Inscrição** e defina a granularidade como **Mês**. Escolha **Grupo de Usuários do Campo Ativo - Nome do Grupo de Usuários**. Ambos aparecem como marcas: **Registro - Data de Registro (Mês)** e **Grupo de Usuários do Campo Ativo - Nome do Grupo de Usuários**.
9. Na linha **Inscrição - Tempo gasto**, selecione **Agregar por** e escolha **Soma**.
10. Na linha **Objeto de Aprendizado - Contagem de Usuários de Registro**, selecione **Agregar por** e escolha **Contagem**.
    ![](assets/image038.jpg)
11. Selecione **Adicionar filtro**. Escolha **Inscrição - Data de Inscrição** e selecione um intervalo relativo, como **Últimos 3 meses**, ou insira um intervalo de datas específico.
12. Selecione **+ Adicionar classificação**. Classifique por **Registro - Data de Registro** em ordem crescente e adicione uma classificação secundária em **Tempo total gasto** em ordem decrescente.
13. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

O relatório terá uma linha por grupo de usuários por mês, mostrando o tempo total gasto e o total de inscrições para esse período.

