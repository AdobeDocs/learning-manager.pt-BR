---
jcr-language: en_us
title: Criar um relatório personalizado no Report Builder
description: Crie um relatório totalmente personalizado no Adobe Learning Manager Report Builder selecionando suas próprias colunas, filtros, agrupar por configurações e classificando a partir de uma tela em branco.
contentowner: mmanuel
source-git-commit: b4540c4c23ad496c8fff01095be6715d18aa0512
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 2%

---


# Criar um relatório personalizado no Report Builder

Criar do zero funciona melhor quando você tem uma imagem clara das colunas e da saída necessárias e nenhum modelo existente corresponde ao seu caso de uso. Se você é novo no Report Builder, considere começar com um modelo.

Neste exemplo, você identificará os alunos de cada gerente que estão em risco para cursos de conformidade.

1. Faça logon no Adobe Learning Manager como administrador.
2. Selecione **Relatórios**, depois selecione **Report Builder**.
3. Selecione a guia **Relatórios** e, em seguida, selecione **Criar relatório**.
4. Informe um nome de relatório. Um nome é necessário. Opcionalmente, informe uma descrição.
   ![](assets/image011.png)
5. No painel coluna, selecione os seguintes conjuntos de dados e expanda-os:
a) Usuário
b) Objeto de aprendizado
c) Status da conformidade do usuário
6. Selecione **+** ao lado das colunas a seguir que você deseja incluir. As colunas selecionadas aparecem na tela do relatório.
a. Usuário\Nome
b. Nome do usuário\gerente
c. Objeto de aprendizado\Nome do objeto de aprendizado
d. Status de Conformidade do Usuário\% de Conclusão
e. Status de Conformidade do Usuário\Conformidade %
!   [](assets/image012.png)
7. Reordene as colunas arrastando-as na tela.
8. Para renomear uma coluna, digite um nome no campo alias da coluna. O alias aparece como o cabeçalho da coluna no arquivo baixado.
9. Selecione **Salvar Relatório**.

## Baixar o relatório

1. Selecione **Ações** no canto superior direito.
   ![](assets/image013.png)
2. Selecione Baixar. Você pode baixar o relatório no ícone de notificações quando estiver pronto.

O relatório baixado na extensão de arquivo .csv contém as seguintes colunas:

1. nome
2. managerName
3. nome
4. completionPct
5. compliancePct

## Aplicar agrupar por, filtros e classificação

### Filtro

Agora que você baixou o relatório, aplique um filtro onde completionPct OU compliancePct é igual a 100.

1. Abra o relatório e selecione **Editar** no canto superior direito.
2. Selecione **Adicionar filtro** e pesquise as colunas em que deseja aplicar os filtros.
   ![](assets/image014.png)
3. Selecione **Adicionar**.
4. Combine os filtros com a lógica AND/OR; selecione o operador para alternar entre as linhas de filtros.
   ![](assets/image015.png)
5. Selecione **Salvar relatório** e baixe o relatório.

O relatório baixado contém registros em que completionPct OU compliancePct é igual a 100.

### Agrupar por

Agrupar os registros por gerente para:

* Agregar dados do aluno por gerente
* Calcular médias no nível do gerente
* Contar alunos em cada gerente

1. Abra o relatório e selecione **Editar** no canto superior direito.
2. Selecione **Agrupar por:Select** e selecione a coluna **Nome do Gerenciador de Usuários**.
   ![](assets/image016.png)
3. Agregar as seguintes colunas:
a) Usuário\Nome
b) Objeto de aprendizado\Nome do objeto de aprendizado
4. Selecione **Count** como uma função de agregação para as colunas.
   ![](assets/image017.png)
5. Repita para Objeto de aprendizado\Nome do objeto de aprendizado.
   ![](assets/image018.png)
6. Selecione **Salvar relatório** e baixe o relatório.

O relatório baixado contém um resumo do desempenho do treinamento do aluno realizado pelo gerente. Ela mostra as taxas médias de conclusão, as pontuações médias de conformidade e o total de contagens de alunos para cada gerente. Os dados indicam a conclusão universal do treinamento em todos os grupos, enquanto o desempenho de conformidade varia significativamente entre os gerentes.

### Ordenar

Classifique o relatório em ordem decrescente pelo número de alunos de cada gerente.

1. Abra o relatório e selecione **Editar** no canto superior direito.
2. Selecione **Adicionar classificação**.
3. Procure o nome de usuário e selecione **Usuário\Nome**.
4. Selecione **Decrescente**.
   ![](assets/image019.png)
5. Selecione **Adicionar**.
6. Selecione **Salvar relatório** e baixe o relatório.

O relatório baixado contém o número de alunos por gerente em ordem decrescente.
