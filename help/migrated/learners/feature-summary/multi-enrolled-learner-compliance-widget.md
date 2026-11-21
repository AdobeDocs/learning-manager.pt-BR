---
description: Saiba como o widget Conformidade do aluno lista cada instância inscrita de um curso multiinscrito que tem um prazo e como a API oferece suporte a ele
jcr-language: en_us
title: Cursos com várias inscrições a serem exibidos no widget de Conformidade do aluno
exl-id: 6484c815-ecae-4a75-ba10-ef42e4ff50a6
source-git-commit: d762bc8f199b703169878acbb52d0d7e3e0d6973
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 1%
---

# Cursos com várias inscrições no widget de Conformidade do aluno

No Adobe Learning Manager, um aluno pode ser inscrito em mais de uma instância do mesmo curso. O widget Conformidade do aluno agora lista cada instância inscrita que tem um prazo, de modo que os alunos veem cada data de vencimento em vez de apenas a instância principal.

## O que muda nos cursos com várias inscrições

Antes dessa alteração, o widget Conformidade mostrava apenas a instância principal de um curso com várias inscrições. Um aluno inscrito em várias instâncias não podia ver os prazos dos outros no widget.

Agora, o widget Conformidade mostra todas as instâncias que atendem a todas essas condições:

* O aluno está inscrito na instância.
* A instância tem um prazo.
* O aluno não concluiu a instância.

Cada entrada exibe o nome da instância, para que os alunos possam distinguir instâncias do mesmo curso. Quando um aluno seleciona uma entrada, o Adobe Learning Manager abre essa instância diretamente.

Por exemplo, um aluno conclui um curso de treinamento inicial. Um administrador inscreve posteriormente o aluno nas edições de setembro, outubro e novembro do mesmo curso, cada uma com um prazo. O widget Conformidade lista todas as três edições.

O widget conta cada instância separadamente em cada categoria de conformidade: **Atrasado**, **Prazo nos próximos 30 dias** e **Em andamento**.

## Instâncias que aparecem no widget Conformidade

A tabela a seguir descreve como o widget trata cada situação de inscrição.

| Situação da inscrição | Aparece no widget | Notas |
|--------------------------------------------------|-----------------------------------|---------------------------------------|
| Inscrita, a instância tem um prazo, não concluída | Sim | Mostrado com o nome da instância |
| Inscrita, a instância não tem prazo | Não | Somente as instâncias com um prazo são exibidas |
| Instância concluída | Não | Uma instância concluída não está listada |
| Concluído em todas as instâncias registradas | Não | O curso não aparece mais |
| Uma instância com um prazo e outra sem | Somente a instância com um prazo |                                       |
| Somente uma instância registrada | Sim | O widget mostra essa instância |

Consulte [Suporte da API para instâncias com várias inscrições no aplicativo do aluno](/help/migrated/api-changes-dec-2026.md#multi-enrolled-compliance-widget) para obter informações sobre a API.
