---
jcr-language: en_us
title: Limitações do Report Builder no Adobe Learning Manager
description: Entenda o que o Report Builder não suporta nesta versão para que você possa planejar sua abordagem de relatórios de acordo.
contentowner: mmanuel
source-git-commit: 14970e9119077860dba6b4e60b3299b63f7db74c
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Limitações do Report Builder no Adobe Learning Manager

O Report Builder abrange uma ampla variedade de necessidades de relatórios personalizados, mas alguns tipos de relatórios, conjuntos de dados e configurações não são suportados nesta versão. Esta seção lista as limitações conhecidas e sugere soluções alternativas quando disponíveis.

## Certificações recorrentes

Certas consultas que envolvem certificações recorrentes não funcionam corretamente no Report Builder nesta versão. Se o relatório envolver ciclos de certificação recorrentes, como o rastreamento da reinscrição ou da conclusão em vários períodos de certificação, use os relatórios de certificação existentes no Adobe Learning Manager.

## Conjuntos de dados e tipos de relatório sem suporte

Os seguintes itens não estão disponíveis no Report Builder nesta versão:

* **Dados de resultado de negócios**: o Report Builder não oferece suporte às integrações do recurso Trazer Seus Próprios Dados (BYOD). Relatórios que combinam dados comerciais externos com dados LMS não são suportados.
* **Relatórios de auditoria**: as trilhas de auditoria do sistema e os logs de atividade do administrador não podem ser compilados no Report Builder. Use os relatórios de auditoria existentes na exibição do administrador para esses dados.
* **Relatórios incrementais**: o Report Builder gera relatórios de instantâneos completos sempre. Não há suporte para relatórios incrementais que retornam apenas registros alterados desde o último download. Para dados incrementais, use a API de trabalho.

## Limitações do relatório de tendências

### Apenas uma coluna de data por relatório de tendência

Um único relatório de tendências só pode ser agrupado por uma coluna baseada em data. Não é possível combinar duas tendências baseadas em data diferentes no mesmo relatório.

Por exemplo, você pode criar:

* Um relatório que mostra **inscrições por mês** (agrupadas por Data de Inscrição)
* Um relatório separado que mostra **conclusões por mês** (agrupadas por Data de Conclusão)

Você não pode criar um único relatório que mostre o mês de inscrição e o mês de conclusão como colunas de tendência separadas. Para obter ambos, crie dois relatórios separados e analise-os lado a lado.

### As tendências refletem os dados atuais, não instantâneos históricos

Os relatórios de tendências no Report Builder são baseados em dados point-in-time atuais, não em instantâneos históricos. O relatório reflete o estado dos registros como eles existem hoje, distribuídos em seus campos de data.

Isto significa:

* Um aluno que se inscreveu em janeiro, mas depois cancelou a inscrição, pode não aparecer na tendência de inscrição de janeiro
* Um grupo de usuários reorganizado não refletirá sua associação histórica nos últimos meses
* Os registros excluídos podem não aparecer na tendência do período em que estavam ativos

Use relatórios de tendências para análise direcional. Para fins precisos de registros históricos ou auditoria, use os relatórios fixos existentes ou exportações de API de trabalho.
