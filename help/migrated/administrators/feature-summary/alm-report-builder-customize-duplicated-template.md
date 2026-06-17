---
jcr-language: en_us
title: Personalizar um modelo de Report Builder duplicado
description: Edite uma cópia de um modelo de Report Builder Adobe Learning Manager para atender às suas necessidades específicas de colunas, filtros e classificação.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---


# Personalizar um modelo de Report Builder duplicado

Depois de duplicar um modelo, você pode adicionar ou remover colunas, atualizar filtros, renomear colunas e ajustar a classificação antes de salvar e baixar\. Este artigo aborda cada etapa de personalização\.

Antes de começar, duplique um modelo da guia **Modelos**.

## Adicionar e remover colunas

1. Na exibição Editar, localize o conjunto de dados que contém a coluna que você deseja adicionar.
2. Selecione **+** ao lado do nome da coluna. A coluna aparece na tela do relatório.
3. Para adicionar a mesma coluna mais de uma vez, por exemplo, para contar dois valores de status diferentes. Selecione **+** novamente para essa coluna.
4. Para remover uma coluna, selecione-a na tela e, em seguida, selecione o ícone Remover.

## Reordenar e renomear colunas

1. Arraste uma coluna para a posição desejada na tela. A ordem na tela corresponde à ordem das colunas no arquivo baixado.
2. Para renomear uma coluna, selecione seu campo de alias e insira o nome que você deseja que apareça como o cabeçalho da coluna no relatório.

## Filtros de atualização

1. Para alterar um valor de filtro existente, selecione a linha de filtro, edite o valor e confirme.
2. Para adicionar um novo filtro, selecione **Adicionar filtro**.
3. Escolha o campo que você deseja filtrar.
4. Selecione um operador. Os operadores disponíveis dependem do tipo de dados do campo.
5. Insira ou selecione um valor:
   * Para campos de sequência de caracteres, digite para pesquisar e selecionar entre as sugestões.
   * Para campos de lista, selecione um ou mais valores no seletor.
   * Para campos de data, insira uma data ou escolha um intervalo relativo, como últimos 90 dias.
6. Para remover um filtro, selecione o ícone de exclusão nessa linha de filtro.

## Classificação de atualização

1. Selecione o ícone de classificação na coluna pela qual deseja classificar.
2. Selecione **Crescente** ou **Decrescente**.
3. Para classificar em colunas adicionais, repita para cada coluna. A primeira coluna classificada é primária; classificações adicionais são aplicadas dentro de vínculos.

>[!TIP]
>
>Sempre aplique pelo menos uma classificação. Sem classificação, a ordem das linhas pode diferir entre os downloads do mesmo relatório.

## Salvar e baixar

1. Selecione Salvar para salvar as alterações na guia **Relatórios**.
2. Selecione **Baixar** para gerar o relatório. Você receberá uma notificação no aplicativo quando o arquivo estiver pronto.
