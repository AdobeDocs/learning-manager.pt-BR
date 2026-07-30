---
description: Este documento resume as alterações dos relatórios de agosto de 2026 no Adobe Learning Manager. Ele aborda colunas novas e atualizadas na transcrição do aluno, no treinamento, na inscrição, na lista de espera, na participação, na auditoria de conteúdo e nos relatórios de usuário. Ele também explica o comportamento adaptável do curso, a pontuação do livro de notas, os registros de aprendizado externo, os relatórios de crédito da Gen AI, o rastreamento da certificação raiz, a padronização do carimbo de data e hora e as atualizações do autor da API.
jcr-language: en_us
title: Alterações de relatórios na versão de agosto de 2026 do Adobe Learning Manager
source-git-commit: 5c32d300f6e66e154a5c993a0d9701254ac8b4ce
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 2%

---


# Alterações de relatórios na versão de agosto de 2026 do Adobe Learning Manager

A versão de agosto de 2026 do Adobe Learning Manager apresenta aprimoramentos de relatórios no gradebook, no aprendizado externo, no uso de crédito da Gen AI e muito mais. Este artigo resume as novas colunas, relatórios e alterações comportamentais disponíveis para os administradores nesta versão.

## O que mudou

As atualizações de relatórios abrangem oito áreas de recursos: pontuação do catálogo de notas, aprendizado externo, exportações de usuários incrementais, uso de crédito de IA de geração, rastreamento da certificação raiz e alinhamento do carimbo de data e hora do webhook. As alterações afetam os seguintes relatórios de forma mais significativa:

- Transcrição do aluno (LT)
- Relatório de treinamento
- Relatório de inscrição
- Relatório de lista de espera
- Relatório de auditoria de conteúdo

A maioria das atualizações introduz novas colunas. Alguns introduziram novos tipos de relatório. Alguns mudaram a forma como os dados existentes são modelados ou formatados.

<!--
## Adaptive course reporting changes

### Training report

Three new columns in the Training report support adaptive course behavior.

| **Column**               | **Description**                                          | **Supported Values**                                                   |
|--------------------------|----------------------------------------------------------|------------------------------------------------------------------------|
| Adaptive Learning Object | Identifies whether a course is adaptive                  | true (adaptive), false (non-adaptive)                                  |
| Visibility User Groups   | Lists user groups that can view each module              | One or more user group names (for example, All Learners, UG-Australia) |
| Mandatory                | Indicates whether a module is mandatory for a user group | User group names for which the module is mandatory; blank = optional   |

You can combine **Visibility User Groups** and **Mandatory** to interpret adaptive completion rules directly in the report. For example, a module may be visible to **All Learners** but mandatory only for the **Administrator group**.


### Learner Transcript

A new **Previous Completions** column captures historical completion data when adaptive logic triggers recompletion.

| **Sub-field**         | **Description**                         |
|-----------------------|-----------------------------------------|
| completionRefreshDate | Timestamp when the completion was reset |
| completedDate         | Previous completion timestamp           |
| progressAtRefresh     | Learner progress before reset           |
| gradeAtRefresh        | Learner score at the time of reset      |

The Learner Transcript now supports multiple completion cycles. When a recompletion event occurs, for example, due to course updates or new mandatory modules, the previous completion moves to the **Previous Completions** column. The current completion remains in the standard transcript fields.

### Enrollment report

A new **Waitlisted** column indicates whether a learner is waitlisted in any module within a course.

| **Value** | **Meaning**                                             |
|-----------|---------------------------------------------------------|
| true      | The learner is waitlisted in one or more modules        |
| false     | Learner has confirmed enrollment in all visible modules |

### Waitlist report

Two new columns and an enhanced status-detail support module enable waitlist tracking at the module level.

| **Column**      | **Description**                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Module**      | Name of the module (classroom or virtual classroom session) where the learner is waitlisted. Appears after the Instance Status column. |
| **Module ID**   | Identifier of the module where the learner is waitlisted. Appears after the Module column.                                             |
| **Embedded In** | The learning path name and ID of any learning path that contains this course. Blank if the course is not part of a learning path.      |

The Waitlist report has shifted from a course-level model to a module session–level model. A learner can now be enrolled in some modules and waitlisted in others. The report also supports waitlist tracking within Flex learning paths, where seat limits are enforced at the module level.

### LP Enrollment report

The Learning Path Enrollment report also receives a new **Remarks** column. When a learner is in a waitlisted state on any classroom or virtual classroom session within the courses that make up the learning path, the Remarks column shows **Waitlisted**. When all sessions are confirmed, the column is blank.

### Attendance report

The **Learner status** column now distinguishes between confirmed and waitlisted learners.

| **Value**  | **Meaning**                            |
|------------|----------------------------------------|
| Confirmed  | The learner has an allocated seat      |
| Waitlisted | The learner is pending seat allocation |

-->

## Alterações no relatório de gradiente

### Transcrição do aluno

Uma nova coluna **Peso** representa a contribuição de cada módulo pontuável para a pontuação geral do curso.

| Valor **1}** | **Descrição** |
|----------------------------------------------|------------------------------------------------------|
| Porcentagem numérica (por exemplo, 20, 30, 50) | Contribuição do módulo para a pontuação do curso |
| Em branco | O módulo não é pontuável (por exemplo, PDF ou vídeos) |

### Relatório de auditoria de conteúdo

Dois novos eventos capturam alterações na configuração do gradiente.

| **Evento** | **Acionado quando** | **Dados capturados** |
|-----------------------|-----------------------------------------------------------------|----------------------------------------------------------|
| Gradebook atualizado | Gradebook ativado, desativado ou modificado no nível do curso | Alteração no estado do catálogo de notas; avaliando atualizações de configuração |
| Peso do módulo atualizado | O peso atribuído a um módulo é modificado | Identificador do módulo; valor de ponderação atualizado |

A transcrição do aluno reflete o peso mais recente. O relatório de auditoria de conteúdo controla as alterações históricas. Juntos, eles fornecem um quadro completo da atual lógica de pontuação e de como ela evoluiu.

## Alterações externas nos relatórios de aprendizado

### Transcrição do aluno

Três novas colunas são adicionadas para oferecer suporte a registros de aprendizado externos.

| **Coluna** | **Descrição** |
|------------------------|-----------------------------------------------------------------------------------------------------|
| Nome do aprendizado externo | Nome da atividade de aprendizado externa enviada pelo aluno |
| Campos personalizados | Uma coluna por campo personalizado configurado para aprendizado externo (texto, numérico, caixa de seleção ou suspenso) |
| Comentário de conclusão | Observações do gerente inseridas durante a aprovação ou rejeição |

**Observação:** na transcrição do aluno (exibição de autoatendimento do aluno), o posicionamento da coluna é diferente da transcrição do aluno administrador:

- O **Nome do Aprendizado Externo** é adicionado imediatamente após a coluna **Módulo** existente.

- O **Comentário de conclusão** é adicionado imediatamente após a coluna **Comentários do revisor** existente.

- As colunas do campo personalizado (uma por campo personalizado configurado) são anexadas ao final da transcrição.

Na transcrição do aluno administrador, todas as novas colunas, incluindo Nome do aprendizado externo e Comentário de conclusão, são anexadas ao final, seguidas por colunas de campo personalizado.

### Digite a coluna na transcrição do aluno

As entradas de aprendizado externas agora aparecem ao lado dos objetos de aprendizado existentes (cursos, programações de aprendizado, certificações) no Administrator LT. A coluna **Tipo** inclui uma nova classificação de aprendizado externo para facilitar a filtragem.

Os dados de aprendizado externos fluem para a transcrição do aluno e para o LT administrador. Campos principais, como data de conclusão, status e mapa de pontuação para colunas existentes. Os campos personalizados são acrescentados como colunas adicionais.

## Alterações incrementais no relatório do usuário

Um novo modelo de exportação incremental permite exportar somente usuários cujos dados tenham sido alterados dentro de uma janela de tempo especificada, em vez de gerar exportações completas de dados a cada vez.

| **Modo de exportação** | **Comportamento** |
|--------------------|-----------------------------------------------------------------|
| Exportação completa | Retorna todos os usuários na conta |
| Exportação incremental | Retorna somente usuários com alterações dentro do intervalo de datas especificado |

Para usar a exportação incremental, filtre por **da data** e **até a data** para definir a janela de alteração. Os relatórios de usuário agora são gerados usando um pipeline de plataforma de dados, e a saída é retornada em blocos para oferecer suporte a contas grandes.

## Gerar relatórios de crédito de IA

Um novo painel de controle de crédito e dois relatórios dão aos administradores visibilidade sobre o consumo de crédito do Gen AI.

### Painel de créditos

O painel mostra as seguintes métricas no nível da conta.

| **Métrica** | **Descrição** |
|-------------------|---------------------------------------------------|
| Créditos comprados | Total de créditos provisionados para a conta |
| Créditos usados | Créditos consumidos em recursos viabilizados por IA |
| Créditos restantes | Créditos disponíveis após consumo |
| Uso por recurso | Consumo de crédito dividido por recurso individual de IA |

### Novos relatórios

| **Denunciar** | **Descrição** |
|----------------------|---------------------------------------------------------------------------------------------|
| Relatório de uso mensal | Resume o consumo de crédito por mês, recurso e créditos consumidos |
| Relatório de trilha de auditoria | Fornece detalhes no nível do usuário: identificador do usuário, nome do recurso, créditos consumidos e carimbo de data/hora |

## Outras alterações comportamentais

### Certificação raiz: ID de treinamento raiz

Uma nova coluna **ID de treinamento raiz** é adicionada ao final da **Transcrição do aluno administrador** e da **Transcrição do aluno** (exibição de autoatendimento do aluno). Ele captura o identificador exclusivo que vincula todas as recorrências de uma certificação a uma única entidade raiz. Isso permite associar todas as instâncias recorrentes de uma certificação a uma única ID de raiz para controle e filtragem.

### Padronização de carimbo de data e hora do webhook e da transcrição do aluno

Os carimbos de data e hora do webhook agora estão alinhados à formatação da transcrição do aluno. Cada campo de data e hora no **objeto de dados** de uma carga de webhook agora tem seu valor de segundos definido como 00, fornecendo uma granularidade de nível de minuto consistente com os relatórios de transcrição do aluno. Isso elimina a necessidade de normalizar os formatos de carimbo de data/hora ao comparar os dados do webhook com os dados de transcrição do aluno.

### Informações do autor na resposta da API para cursos compartilhados

Quando um curso é compartilhado de uma conta do Adobe Learning Manager para outra por meio do compartilhamento do catálogo, a resposta do objeto de aprendizado (LO) da API agora retorna apenas os detalhes do autor original da conta de origem. Anteriormente, o administrador da conta de aceitação aparecia como autor do curso na resposta da API para sua conta

Essa alteração afeta apenas contas entre parceiros (recebimento). Quando você consulta o ponto de extremidade de detalhes do OA para um curso compartilhado em uma conta de recebimento, o campo authorNames agora reflete o autor original da conta de origem, não o administrador da conta de recebimento.

Não há nenhuma alteração em como os detalhes do autor aparecem ao consultar o OA na conta de origem.

**Observação:** se a integração depender do campo authorNames na resposta da API do LO para cursos compartilhados, verifique se os dados atualizados do autor não rompem nenhuma lógica downstream que presumiu que o nome do administrador da conta de recebimento apareceria nesse campo.
