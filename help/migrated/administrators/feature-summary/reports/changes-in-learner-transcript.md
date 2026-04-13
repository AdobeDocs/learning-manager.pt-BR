---
description: Saiba mais sobre as transcrições do aluno
jcr-language: en_us
title: Alterações nas transcrições do aluno
source-git-commit: cd0737061029e75953fa23cf3d12409b1407772a
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---


# Alterações nas transcrições do aluno na versão de abril

## Coluna Método de Conclusão

A coluna **Método de conclusão** indica como cada registro na transcrição do aluno do administrador foi concluído.

**Valores:**

1. **Direto** (para términos diretos)
2. **Alternativa** (para conclusões obtidas por meio de relações alternativas)
3. **Alternativa Revogada** (quando todas as conclusões alternativas são revogadas devido à inconclusão retroativa e remoção de relação)

>[!NOTE]
>
>Essa coluna não é visível no LT do aluno; ela só está disponível no LT do administrador para fins de relatório e rastreamento.

**Impacto**: habilita trilhas de auditoria claras, controle de conformidade e transparência para administradores em relação à forma como um curso foi concluído.

## Controle de conclusão alternativo em transcrições do aluno

As conclusões alternativas permitem que os alunos recebam crédito de conclusão para um curso de destino ou caminho de aprendizado quando tiverem concluído um curso ou caminho de origem equivalente, com base em relacionamentos estabelecidos.

Na transcrição do aluno (LT), as conclusões alternativas afetam três colunas existentes: **Status**, **Data de conclusão** e **Origem da conclusão**.

- **Status**: o status pode ser **Concluído**, mesmo que o aluno não tenha concluído diretamente o curso ou caminho de destino devido à conclusão alternativa. Outros status (**Não Iniciado**, **Em Andamento**, **Não Inscrito**) não são afetados.
- **Data de conclusão**: para conclusão alternativa, a data é herdada do curso ou caminho de origem. Se o aluno concluir o destino diretamente posteriormente, a data será atualizada para refletir a conclusão direta.
- **Origem da Conclusão**: captura as IDs de treinamento do(s) curso(s) de origem ou caminho(s) que forneceu a conclusão alternativa. Várias origens ativas estão listadas como IDs separadas por vírgula. Se as origens forem revogadas, apenas as ativas permanecerão. Quando existem várias fontes, a data de conclusão mais antiga é usada.

**Impacto**: as conclusões alternativas reduzem a reconciliação manual, automatizam o rastreamento do progresso em caminhos de aprendizado e certificações e oferecem suporte aos requisitos de conformidade.

>[!NOTE]
>
>As transcrições do aluno não exibem a coluna **Método de conclusão**. Esta coluna está disponível somente na transcrição do aluno administrador.

## Lógica de data de conclusão para alternativas

A coluna **Data de conclusão** na transcrição do aluno é usada para conclusões diretas e alternativas.

- Para conclusões alternativas, a data reflete quando o aluno concluiu o curso ou caminho de origem.
- Se o aluno concluir o destino diretamente posteriormente, a data de conclusão será atualizada para a data de conclusão direta.
- Nenhuma nova coluna foi introduzida para datas de conclusão alternativas.
- Se várias fontes fornecerem uma conclusão alternativa, a primeira data de conclusão ativa será usada.
- Se uma origem for revogada (com inconclusão retroativa ativada), a data será atualizada para a próxima origem ativa mais antiga ou será limpa se nenhuma origem ativa permanecer.

**Impacto**: garante o rastreamento histórico preciso e a geração de relatórios consistentes, mesmo quando as relações alternativas mudam com o tempo.

## Conclusões alternativas revogadas

As conclusões alternativas revogadas ocorrem quando todos os relacionamentos de origem de um curso ou caminho de aprendizado de destino são removidos, desde que a inconclusão retroativa esteja ativada.

### Condições de acionamento

- A inconclusão retroativa deve ser ativada no nível da conta.
- A revogação ocorre somente quando **todas** as relações de origem ativas são removidas.
- Se pelo menos uma origem permanecer, o preenchimento alternativo persiste e a coluna de origem do preenchimento é atualizada de acordo.

### Impacto na transcrição do aluno

- **Status**: se todas as conclusões alternativas forem revogadas e não houver conclusão direta, o status será atualizado (por exemplo, de **Concluído** para **Não Iniciado** ou **Em Andamento**).
- **Data de conclusão**: limpa se nenhuma fonte ativa permanecer e não houver conclusão direta.
- **Origem de Conclusão**: Atualizada para remover origens revogadas; desmarcada se todas as origens forem revogadas.

Se o aluno tiver uma conclusão direta, revogar origens alternativas não afeta o status de conclusão ou a data de conclusão.

>[!NOTE]
>
>Se várias fontes forneceram conclusão alternativa e apenas algumas foram revogadas, a transcrição reflete as fontes ativas restantes e sua data de conclusão mais antiga. Se todas as origens forem revogadas e não houver conclusão direta, o aluno perderá o status de conclusão do destino.

## Relatórios aprimorados para comentários do revisor da lista de verificação

Os comentários do revisor nos módulos de lista de verificação agora estão incluídos no relatório de transcrição do aluno em uma coluna renomeada, **Comentários do revisor**.

**Impacto**: permite que alunos e administradores visualizem comentários consolidados, melhorando a transparência e apoiando a avaliação de desempenho.

## Cálculo de tempo de aprendizado aprimorado

O relatório de transcrição do aluno agora usa lógica refinada para distinguir entre o tempo de aprendizado ativo e ocioso com base na atividade do usuário e no foco da guia do navegador.

**Impacto**: fornece uma medição mais precisa do envolvimento do aluno, oferecendo suporte a relatórios e análises de conformidade.
