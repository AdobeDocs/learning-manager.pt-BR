---
description: Este documento resume as alterações dos relatórios de agosto de 2026 no Adobe Learning Manager. Ele aborda colunas novas e atualizadas na transcrição do aluno, no treinamento, na inscrição, na lista de espera, na participação, na auditoria de conteúdo e nos relatórios de usuário. Ele também explica o comportamento adaptável do curso, a pontuação do livro de notas, os registros de aprendizado externo, os relatórios de crédito da Gen AI, o rastreamento da certificação raiz, a padronização do carimbo de data e hora e as atualizações do autor da API.
jcr-language: en_us
title: Alterações de relatórios na versão de agosto de 2026 do Adobe Learning Manager
source-git-commit: 2d60f665d2e00c95edfc96360ee65fdae013c0cd
workflow-type: tm+mt
source-wordcount: '1434'
ht-degree: 2%

---


# Alterações de relatórios na versão de agosto de 2026 do Adobe Learning Manager

A versão de agosto de 2026 do Adobe Learning Manager apresenta aprimoramentos de relatórios em cursos adaptáveis, gradientes, aprendizado externo, uso de créditos de IA da geração e muito mais. Este artigo resume as novas colunas, relatórios e alterações comportamentais disponíveis para os administradores nesta versão.

## O que mudou

As atualizações de relatórios abrangem oito áreas de recursos: comportamento adaptável do curso, lista de espera adaptável, pontuação do livro de notas, aprendizado externo, exportações incrementais de usuários, uso de crédito de IA de geração, rastreamento da certificação raiz e alinhamento do carimbo de data e hora do webhook. As alterações afetam os seguintes relatórios de forma mais significativa:

- Transcrição do aluno (LT)
- Relatório de treinamento
- Relatório de inscrição
- Relatório de lista de espera
- Relatório de auditoria de conteúdo

A maioria das atualizações introduz novas colunas. Alguns introduziram novos tipos de relatório. Alguns mudaram a forma como os dados existentes são modelados ou formatados.

## Alterações adaptativas nos relatórios do curso

### Relatório de treinamento

Três novas colunas no relatório de treinamento oferecem suporte ao comportamento adaptável do curso.

| **Coluna** | **Descrição** | **Valores com Suporte** |
|--------------------------|----------------------------------------------------------|------------------------------------------------------------------------|
| Objeto de aprendizado adaptativo | Identifica se um curso é adaptativo | verdadeiro (adaptável), falso (não adaptável) |
| Grupos de usuários de visibilidade | Lista os grupos de usuários que podem exibir cada módulo | Um ou mais nomes de grupos de usuários (por exemplo, Todos os alunos, UG-Austrália) |
| Obrigatório | Indica se um módulo é obrigatório para um grupo de usuários | Nomes de grupos de usuários para os quais o módulo é obrigatório; em branco = opcional |

Você pode combinar **Grupos de usuários de visibilidade** e **Obrigatórios** para interpretar regras de conclusão adaptáveis diretamente no relatório. Por exemplo, um módulo pode estar visível para **Todos os alunos**, mas é obrigatório apenas para o **grupo de administradores**.

### Transcrição do aluno

Uma nova coluna **Conclusões anteriores** captura dados históricos de conclusão quando a lógica adaptativa aciona a reconclusão.

| **Subcampo** | **Descrição** |
|-----------------------|-----------------------------------------|
| completionRefreshDate | Carimbo de data/hora de quando a conclusão foi redefinida |
| completedDate | Carimbo de data/hora de conclusão anterior |
| progressAtRefresh | Progresso do aluno antes de redefinir |
| gradeAtRefresh | Pontuação do aluno no momento da redefinição |

A transcrição do aluno agora suporta vários ciclos de conclusão. Quando ocorre um evento de reconclusão, por exemplo, devido a atualizações do curso ou novos módulos obrigatórios, a conclusão anterior passa para a coluna **Conclusões anteriores**. A conclusão atual permanece nos campos de transcrição padrão.

### Relatório de inscrição

Uma nova coluna **Em lista de espera** indica se um aluno está em lista de espera em qualquer módulo de um curso.

| Valor **1&rbrace;** | **Significado** |
|-----------|---------------------------------------------------------|
| verdadeiro | O aluno está em lista de espera em um ou mais módulos |
| falso | O aluno confirmou a inscrição em todos os módulos visíveis |

### Relatório de lista de espera

Duas novas colunas e um módulo de suporte aprimorado de detalhes de status habilitam o controle de lista de espera no nível do módulo.

| **Coluna** | **Descrição** |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Módulo** | Nome do módulo (sala de aula ou sessão de sala de aula virtual) em que o aluno está na lista de espera. Aparece após a coluna Status da Instância. |
| **ID do módulo** | Identificador do módulo em que o aluno está na lista de espera. Aparece após a coluna Módulo. |
| **Incorporado Em** | O nome e a ID do caminho de aprendizado que contém este curso. Em branco se o curso não fizer parte de um caminho de aprendizado. |

O relatório de lista de espera foi alterado de um modelo de nível de curso para um modelo de nível de sessão do módulo. Um aluno agora pode ser inscrito em alguns módulos e colocado em lista de espera em outros. O relatório também oferece suporte ao controle de lista de espera nos caminhos de aprendizado do Flex, em que os limites de vagas são aplicados no nível do módulo.

### Relatório de inscrição de LP

O relatório de Inscrição do Caminho de Aprendizado também recebe uma nova coluna **Comentários**. Quando um aluno está em um estado de lista de espera em qualquer sala de aula ou sessão de sala de aula virtual nos cursos que compõem o caminho de aprendizado, a coluna Comentários mostra **Lista de espera**. Quando todas as sessões forem confirmadas, a coluna ficará em branco.

### Relatório de participação

A coluna **Status do aluno** agora distingue entre alunos confirmados e em lista de espera.

| Valor **1&rbrace;** | **Significado** |
|------------|----------------------------------------|
| Confirmado | O aluno tem uma vaga alocada |
| Em lista de espera | O aluno tem alocação de vagas pendente |

## Alterações no relatório de gradiente

### Transcrição do aluno

Uma nova coluna **Peso** representa a contribuição de cada módulo pontuável para a pontuação geral do curso.

| Valor **1&rbrace;** | **Descrição** |
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
