---
jcr-language: en_us
title: Perguntas frequentes (Report Builder)
description: Obtenha respostas às perguntas frequentes sobre o Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: 8823a5481bc3b34266f7ec36a8f3c26cb923e1ce
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---


# Perguntas frequentes (Report Builder)

**Qual é a diferença entre um modelo e um relatório?**

Os modelos são configurações de relatório predefinidas fornecidas pela Adobe Learning Manager. Eles foram projetados para casos de uso comuns, prontos para download imediato e somente leitura. Não é possível editá-los. Os relatórios são suas próprias configurações salvas. Para criá-los, crie do zero ou duplique um modelo e edite a cópia. Os relatórios aparecem na guia **Relatórios**; os modelos aparecem na guia **Modelos**.

**Posso editar um modelo diretamente?**

Não. Os modelos são somente leitura. Para personalizar um modelo, selecione **Duplicar** para criar uma cópia editável. Suas alterações são salvas como um novo relatório na guia **Relatórios** e não afetam o modelo original.

Linhas duplicadas aparecem quando um campo nos dados tem um relacionamento um-para-muitos com o registro principal. As causas comuns incluem sessões com vários professores (uma linha por professor por sessão) e objetos de aprendizado com vários autores. Para resolver isso, adicione o campo que tem vários valores, como **Nomes de Instrutor** ou **Nome do Autor**, como uma coluna.

**Por que as datas são exibidas em UTC?**

Report Builder retorna os valores de data em UTC nesta versão. O fuso horário configurado da sua conta será aplicado aos campos de data em uma versão futura. Ao analisar dados baseados em data, fatore no deslocamento UTC relevante para o fuso horário principal da sua conta.

**Quanto tempo leva para que os novos dados de inscrição ou conclusão apareçam?**

Report Builder obtém do banco de dados do Adobe Learning Manager, que tem uma latência máxima de aproximadamente 15 minutos a partir de quando um evento ocorre no sistema. Se você acabou de gravar uma inscrição ou conclusão e ela não aparece no seu relatório, aguarde pelo menos 15 minutos e baixe novamente.

**Há um limite em linhas ou colunas em um relatório?**

Os relatórios estão limitados a aproximadamente 1 milhão de linhas. Não há limite para o número de colunas nesta versão. Se o relatório exigir mais de 1 milhão de linhas, aplique filtros para reduzir o escopo.

**Há um limite de tamanho de arquivo ao exportar relatórios do Report Builder?**

Atualmente, arquivos de relatório exportados maiores que 5 GB não são compatíveis com Report Builder. Se a expectativa for que o seu relatório exceda esse tamanho, considere a aplicação de filtros adicionais ou a redução do número de linhas para manter a exportação abaixo de 5 GB.

**Posso extrair dados de Report Builder por meio de uma API ou automação?**

O acesso automatizado da API aos relatórios de Report Builder está planejado para uma versão futura. Na versão atual, os relatórios são baixados manualmente por meio da interface do Report Builder ou recebidos de forma programada por meio do recurso de assinatura.
