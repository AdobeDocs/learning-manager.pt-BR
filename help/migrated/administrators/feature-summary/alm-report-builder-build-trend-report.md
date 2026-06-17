---
jcr-language: en_us
title: Criar um relatório de tendências no Report Builder
description: Acompanhe as tendências de aprendizado mês a mês ou semana a semana no Adobe Learning Manager Report Builder usando agregadores de tendência em campos de data.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---


# Criar um relatório de tendências no Report Builder

Os relatórios de tendência mostram como as métricas, como contagem de cursos, contagem de inscrições ou conclusões, se alteram ao longo do tempo. Você escolhe uma coluna de data e uma granularidade de tendência (dia, semana ou mês) e Report Builder agrupa os dados por esse período.

## O que significam os dados de tendência

Os relatórios de tendências no Report Builder refletem **um instantâneo atual de dados, agrupados por data**. Eles não mostram o estado histórico dos dados em cada data passada.

Por exemplo, uma tendência de inscrição mensal mostra o número de inscrições existentes hoje, distribuídas pelos meses em que foram criadas. Se um aluno inscrito em janeiro e posteriormente cancelar a inscrição, esse registro de inscrição talvez não seja mais exibido. O relatório reflete o estado atual dos registros, não o que era verdade em janeiro.

Esta é uma distinção importante para fins de auditoria. Se você precisar de dados históricos point-in-time, use esse relatório para análise de tendência direcional em vez de registros históricos precisos.

## Criar um relatório de tendência de contagem de cursos

Este relatório mostra quantos cursos foram adicionados à conta mês a mês.

1. Selecione **Relatórios** > **Report Builder** e selecione a guia **Relatórios**.
2. Selecione **Criar relatório**. Digite um nome como Número de cursos MoM.
3. Adicione **ID do Objeto de Aprendizado** do conjunto de dados **Objeto de Aprendizado**.
4. Adicione **Data de Criação** do conjunto de dados **Objeto de Aprendizado**.
   ![](assets/image039.png)
5. Aplicar **Agrupar por** em **Data de Criação**. Defina a granularidade da tendência para **Mês**.
   ![](assets/image040.png)
6. Aplicar **Contagem** a **ID de Objeto de Aprendizado**. Insira o alias Contagem do curso.
   ![](assets/image041.png)
7. Classifique por **Data de Criação** em ordem crescente para mostrar a tendência cronologicamente.
   ![](assets/image042.png)
8. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

O arquivo baixado consiste em uma tendência mensal da atividade de criação do curso, mostrando o número de cursos criados ao longo do tempo. Ele ajuda a acompanhar os padrões de produção, picos, quedas e crescimento geral do conteúdo do curso.

## Criar um relatório de tendência de conclusões em todo o catálogo

Esse relatório mostra os totais de conclusão mensal por catálogo durante um período definido.

1. Selecione **Relatórios** > **Report Builder** e selecione a guia **Relatórios**.
2. Selecione **Criar relatório**. Digite um nome como Conclusões de catálogo MoM.
3. Adicione o **Nome do Catálogo** do conjunto de dados **Catálogo**.
4. Adicionar **Data de Conclusão** do conjunto de dados **Transcrição do Módulo**.
5. Adicione **ID do Objeto de Aprendizado** do conjunto de dados **Objeto de Aprendizado** para contar as conclusões.
6. Aplicar **Agrupar por** em **Nome do catálogo**. Aplique também **Agrupar por** em **Data de conclusão** com granularidade de **Mês**.
   ![](assets/image_043.png)
7. Aplicar **Contagem** a **ID de Objeto de Aprendizado**. Informe o apelido Total de conclusões.
8. Adicionar um filtro: **O catálogo** está em Segurança, PDV, Entrega (ou nos catálogos relevantes à sua conta).
9. Adicione um filtro: **A Data de Conclusão** está no ano passado.
   ![](assets/image044.png)
10. Classificar por **Data de conclusão** em ordem crescente.
    ![](assets/image_045.png)
11. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

## Práticas recomendadas

* Use **Data de conclusão** para tendências de conclusão e **Data de inscrição** para tendências de inscrição. O uso do campo de data incorreto produz resultados incorretos.
* Adicione um filtro de data para limitar a tendência a uma janela significativa, por exemplo, os últimos 12 meses para uma tendência mensal ou as últimas 8 semanas para uma tendência semanal.
* Rotule seu relatório de tendência com a granularidade e o intervalo de datas no nome, por exemplo, “Conclusões de catálogo - MoM - últimos 3 meses”, para que fique claro quando você visualizá-lo posteriormente.
