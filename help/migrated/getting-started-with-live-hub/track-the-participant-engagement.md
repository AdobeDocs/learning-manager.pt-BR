---
title: Acompanhar o envolvimento do participante
description: Saiba como os professores usam o indicador de envolvimento do participante em tempo real no Live Hub para monitorar o foco do navegador, a atividade de bate-papo e a participação em enquetes.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 5d89078fff50bbd3be1a2d01085efd568b8e0130
workflow-type: tm+mt
source-wordcount: '1408'
ht-degree: 0%
---

# Acompanhar o envolvimento do participante

O envolvimento do participante no Live Hub fornece aos professores uma exibição em tempo real do envolvimento do aluno ou participante durante uma sessão ao vivo. Ele combina o foco do navegador, a atividade de bate-papo e a participação nas pesquisas em um único nível de engajamento, exibido como um indicador verde, amarelo ou vermelho. Use-a para detectar mergulhos de atenção e ajustar o fornecimento em tempo real.

O envolvimento do participante exibe o nível médio de envolvimento de todos os alunos na sala principal em um determinado momento. O nível é atualizado assim que um aluno entra na sessão.

O envolvimento do participante é calculado e exibido somente durante uma sessão ao vivo.

>[!NOTE]
>
> Somente os professores podem ver o envolvimento do participante. Os alunos não têm acesso a ela.

## Compreender os cálculos do nível de compromisso

A pontuação de envolvimento do participante ajuda a monitorar a atenção do aluno em tempo real durante uma sessão ao vivo. Este emblema de engajamento na parte superior da tela exibe o nível geral de engajamento como **Baixo**, **Médio** ou **Alto**, permitindo que você ajuste a entrega da sua sessão e incentive a participação conforme necessário.

O indicador é visível apenas para professores na sala principal.

![Indicador de Nível de Compromisso](assets/engagement-level-indicator.png)
*Interface do Live Hub exibindo o envolvimento do participante no canto superior direito.*

## Como a pontuação do compromisso é calculada

Cada aluno ou participante tem pontuação de envolvimento que varia de 0 a 100, com base nos seguintes fatores:

- **Atenção à sessão**: quando um aluno ou participante mantém a janela da sessão ativa, o nível de envolvimento é Alto, por padrão. Se eles alternarem para outra janela ou guia do navegador, o nível de envolvimento cairá para Baixo, a menos que continuem participando de atividades de sessão.
- **Participação na sessão**: atividades como falar, compartilhar uma tela, enviar mensagens de chat, responder a pesquisas ou questionários, desenhar no quadro de comunicações, levantar a mão, enviar reações e clicar na sessão aumentam a pontuação do engajamento.

### Como as pontuações de engajamento mudam

A pontuação de envolvimento do aluno muda ao longo de uma sessão ao vivo com base em sua atenção e participação. As seguintes condições afetam como a pontuação do compromisso é calculada:

- **Duração da atividade**: a maioria das atividades de participação aumenta temporariamente a pontuação do compromisso, com sua contribuição diminuindo gradualmente em aproximadamente cinco minutos. Por exemplo, se um aluno fala durante uma sessão e depois muda para outra janela, a pontuação de envolvimento diminui gradualmente, em vez de imediatamente
- **Compartilhamento de tela**: a pontuação do envolvimento permanece em 100 enquanto um aluno ou participante compartilha sua tela.
- **Atividades simultâneas**: quando um aluno ou um participante executa várias atividades simultaneamente, apenas a atividade com o valor de compromisso mais alto é considerada. As pontuações de atividades individuais não são combinadas, garantindo que a pontuação do contrato não exceda 100.
- **Vários dispositivos**: se um aluno ou um participante ingressar na sessão de vários dispositivos, a pontuação de engajamento mais alta nesses dispositivos será considerada.

## Pontuação geral de envolvimento

O emblema de envolvimento do participante exibe o nível de engajamento geral com base na pontuação média de engajamento de todos os alunos na sala principal, arredondado para o número inteiro mais próximo.

As seguintes condições se aplicam ao calcular a pontuação geral do compromisso:
- **Professores e bots de gravação**: professores e bots de gravação são excluídos do cálculo geral da pontuação de envolvimento. Os bots de gravação não aparecem na lista de participantes.
- **Salas para sessão de grupo**: alunos ou participantes em salas para sessão de grupo não são incluídos na pontuação geral do compromisso. Quando os alunos se movem entre a sala principal e uma sala de sessão de grupo, as pontuações individuais de engajamento são redefinidas e recalculadas em um a dois minutos.
- **Novos alunos**: a pontuação de envolvimento do participante fica disponível aproximadamente um minuto após ingressar na sessão. Até que a pontuação esteja disponível, o aluno ou participante será excluído do cálculo da pontuação geral do compromisso.
- **Sala principal vazia**: quando nenhum aluno ou participante está presente na sala principal, a medalha exibe o envolvimento do participante sem um nível de envolvimento.

## Identificar níveis e indicadores do contrato

O emblema de engajamento do participante exibe um dos seguintes níveis de engajamento com base na pontuação geral do engajamento. Você pode usar esses níveis para monitorar a atenção do aluno e ajustar a entrega da sessão conforme necessário.  Veja o que cada nível significa:

| **Nível de compromisso** | **Pontuação** | **Descrição** |
|----|----|----|
| Alto | 61 a 100 | Os alunos participam ativamente da sessão. |
| Médio | 31 a 60 | Os alunos mostram interação ocasional com participação moderada. |
| Baixo | 0 a 30 | Os alunos mostram pouca ou nenhuma interação ou foco reduzido durante a sessão. |

>[!NOTE]
>
> - A pontuação de engajamento indica a atenção do participante durante uma sessão. Não mede os resultados da aprendizagem nem o desempenho.
> 
> - As pontuações de engajamento são calculadas a cada minuto. As alterações podem levar até dois minutos para aparecerem no emblema de engajamento.

## Perguntas frequentes

+++ A pontuação do engajamento detecta se um participante está assistindo ativamente à sessão?

Não. A pontuação de engajamento é calculada com base na ativação da janela da sessão e nas atividades do participante, como falar, enviar mensagens de bate-papo e responder a pesquisas. Ele não usa vídeo da câmera, rastreamento ocular ou status de microfone sem áudio para medir o engajamento.

+++

+++ O que acontece quando um participante sai da janela de sessão?

Quando um participante alterna para outra guia do navegador, janela ou aplicativo, a janela da sessão não é mais considerada ativa. Mesmo que a janela da sessão permaneça visível, ela é considerada inativa quando outra janela está em foco.

+++

+++ Todas as atividades de participação contribuem igualmente para a pontuação do contrato?

Falar, compartilhar a tela, enviar mensagens de bate-papo, responder a pesquisas ou questionários, desenhar no quadro branco, levantar a mão e enviar reações contribuem igualmente para a pontuação do engajamento. Clicar dentro da sessão contribui um pouco menos.

+++

+++ Como a pontuação do contrato muda após uma atividade de participação?

A contribuição da maioria das atividades de participação diminui gradualmente ao longo de cerca de cinco minutos. Por exemplo, se um participante mudar para outra janela e depois falar, a pontuação de engajamento aumenta para 100 na próxima atualização. Nos minutos seguintes, a pontuação diminui gradualmente para 80, 60, 40 e 20, onde permanece até que o participante retorne à janela da sessão ou participe novamente.

Um participante que mantém a janela de sessão ativa mantém um nível de envolvimento Alto.

+++

+++ Os participantes em salas para sessão de grupo estão incluídos na pontuação geral do compromisso?

Não. Somente os participantes da sala principal são incluídos no cálculo da pontuação geral do compromisso. A medalha de noivado não é exibida quando um professor está em uma sala de sessão de grupo.

+++

+++ Por que a pontuação geral de engajamento diminui após o término das salas para sessão de grupo?

Quando os participantes se movem das salas para a sala principal, suas pontuações individuais de engajamento são redefinidas e recalculadas em um ou dois minutos. Isso pode diminuir temporariamente a pontuação geral do compromisso.

+++

+++ Como a pontuação de engajamento é calculada quando um participante ingressa em vários dispositivos?

Se um participante ingressar na sessão usando vários dispositivos, a pontuação de engajamento mais alta nesses dispositivos será considerada. Uma sessão inativa em um dispositivo não reduz a pontuação de engajamento registrada em outro dispositivo ativo.

+++

+++ Por que a medalha de engajamento leva até dois minutos para ser atualizada?

A pontuação de engajamento de cada participante é calculada uma vez a cada minuto. A pontuação geral do contrato é atualizada uma vez a cada minuto, portanto as alterações podem levar até dois minutos para aparecerem no emblema do contrato.

+++

+++ O que os professores podem fazer quando o emblema de engajamento exibe Baixa?

Um nível de envolvimento baixo indica que a maioria dos participantes saiu da janela da sessão e não está participando ativamente. Os professores podem usar pesquisas, questionários, prompts de bate-papo ou perguntas de discussão para incentivar a participação e chamar a atenção dos participantes de volta à sessão.

+++

+++ Os professores podem usar as pontuações de envolvimento para controlar a participação ou avaliar os alunos?

As pontuações de engajamento fornecem uma indicação geral da atenção e da atividade dos participantes durante uma sessão. Um participante pode manter um alto nível de envolvimento mantendo a janela da sessão ativa, mesmo sem participar ativamente ou demonstrar o aprendizado. Portanto, as pontuações do compromisso podem não ser adequadas para avaliar o desempenho do aluno ou monitorar a participação.

+++

+++ Os participantes podem exibir suas pontuações de engajamento?

Não. A medalha de noivado é visível somente para professores.

+++

+++ Os professores podem exibir as pontuações de envolvimento dos participantes individuais?

Não. O emblema de engajamento exibe apenas a pontuação geral do engajamento da sala principal. As pontuações de participantes individuais não estão disponíveis.

+++

+++ Os professores podem desativar o rastreamento de engajamento?

Não. O controle de envolvimento está sempre habilitado e não pode ser desabilitado.

+++

+++ As pontuações do contrato estão disponíveis em relatórios ou no histórico da sessão?

Não. O emblema do engajamento exibe apenas a pontuação geral do engajamento atual. As pontuações de compromisso não são salvas nem incluídas no histórico de relatórios ou sessões.

+++

+++ Os coprofessores podem visualizar a medalha de envolvimento?

Sim Os coinstrutores também podem ver a medalha de envolvimento durante uma sessão.

+++

+++ Como as pontuações de engajamento são calculadas em dispositivos móveis?

Os participantes podem acessar sessões do Live Hub usando navegadores para dispositivos móveis. As pontuações de engajamento são calculadas usando os mesmos critérios dos navegadores de desktop.

+++
