---
jcr-language: en_us
title: Revisar o desempenho do professor com o Report Builder
description: Crie um relatório no Adobe Learning Manager Report Builder que mostre as sessões ensinadas, o total de inscrições e as conclusões por professor.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# Revisar o desempenho do professor com o Report Builder

## Visão geral

Esse relatório ajuda os gerentes de treinamento a identificar quais professores estão mais ativos, quantos alunos eles alcançam e quantos alunos concluem os cursos que oferecem.

## Criar um relatório de eficiência do professor

1. Inicie o Report Builder e selecione **Criar Relatório**.
2. Digite um nome como **Eficiência do professor**.
3. Adicione **Nomes de Professores** do conjunto de dados **Módulo**.
4. Adicionar **ID do Módulo** do conjunto de dados **Módulo**. Agregaremos isso para contar as sessões.
5. Adicione **Status** da **Transcrição do módulo** ao conjunto de dados. Você usará a contagem se quiser contar as conclusões.
6. Selecione **Agrupar por** em **Nomes de Professores**.
7. Aplicar **Contagem** a **ID de módulo**. Digite o alias Total de sessões.
8. Aplicar **Contagem se** a **Status**, selecione Concluído. Digite o alias **Total de conclusões**.
9. Para mostrar também o total de inscrições, adicione **Status** uma segunda vez. Aplicar **Contagem if** a Não Iniciado. Digite o apelido Total de inscrições.

   ![](assets/report-builder-0037.png)

10. Filtrar **Nomes de Professores** para não ficar vazio.

    ![](assets/report-builder-0038.png)

11. Classifique por **Total de conclusões** descendentes para destacar primeiro os professores com melhor desempenho.

    ![](assets/report-builder-0039.png)

12. Selecione **Salvar Relatório** e selecione **Ações** > **Baixar** para baixar o relatório.

O relatório baixado resume a eficiência do professor comparando o total de sessões de treinamento, a conclusão do aluno e as inscrições não iniciadas para cada professor, ajudando a avaliar o envolvimento, o desempenho da conclusão e as possíveis necessidades de acompanhamento do treinamento.

## Práticas recomendadas

* Use etiquetas de catálogo para enquadrar os relatórios do professor em uma unidade de negócios, local ou programa específico. Isso é mais preciso do que filtrar apenas por nome de catálogo.
* Adicione um filtro de data, como **Data de Inscrição** nos últimos 90 dias, para definir o escopo do relatório para um período recente, em vez de dados de todos os tempos.
* Classifique por uma métrica significativa, como **Total de conclusões**, em vez de pelo nome do professor, para que as diferenças de desempenho fiquem imediatamente visíveis.
