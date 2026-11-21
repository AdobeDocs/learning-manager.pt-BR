---
description: Saiba como cancelar e reativar sessões ILT e VILT no Adobe Learning Manager definindo o estado da sessão nos dados de migração do Workfront
jcr-language: en_us
title: Cancelamento do ALM Workfront
exl-id: 01500cf2-6e39-4ac3-84e2-823a5215f6cf
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '2112'
ht-degree: 1%
---

# Gatilho de cancelamento/atualização do ALM-Workfront

## Visão geral

O Adobe Learning Manager (Learning Manager) agora pode cancelar e reativar sessões guiadas por instrutor e virtual guiadas por instrutor (ILT/VILT) com base nas alterações feitas no Workfront. Se sua organização agenda sessões no Workfront e as traz para o Learning Manager por meio da migração de Workfront para Learning Manager, você pode definir o estado de cada sessão como Ativo ou Cancelado nos dados de migração. O Learning Manager aplica a alteração como se um administrador tivesse cancelado a sessão na interface do usuário.

Cancelar uma sessão pela migração se comporta da mesma forma que cancelá-la na interface do usuário do Learning Manager. A única diferença deliberada é a reativação, que está descrita em [Reativar uma sessão cancelada](#reactivate-a-cancelled-session).

### O requisito

As atualizações de uma sessão, como data e hora, professor, local ou link e capacidade, já fluem do Workfront para o Learning Manager durante a migração. Os cancelamentos não. Quando uma sessão era cancelada no Workfront, o Learning Manager não tinha como saber, o que causava os seguintes problemas:

* Os alunos permaneceram inscritos em uma sessão que não funcionava mais, levando à confusão e à não apresentação.
* Os administradores tinham que repetir o cancelamento manualmente no Learning Manager.
* O Workfront e o Learning Manager ficaram fora de sincronia, o que prejudicou o Workfront como a fonte confiável do agendamento.

### Como funciona

1. Um gerente de entrega cancela uma sessão no Workfront.
1. A linha de sessão nos dados de migração inclui a nova coluna de estado de sessão, definida como Cancelada.
1. Um administrador de sistemas executa a migração por meio da API.
1. O Learning Manager marca a sessão de correspondência como cancelada e envia as mesmas notificações que um cancelamento da interface do usuário envia.

>[!NOTE]
>
>Esse recurso estende o processo de migração existente em vez de adicionar um segundo caminho de integração em tempo real.

### Fluxo de trabalho completo

O diagrama a seguir mostra como uma linha de sessão se move do Workfront para o Learning Manager.

![Fluxograma mostrando uma linha de sessão do Workfront passando pela migração para criar, atualizar ou cancelar a sessão correspondente](assets/alm-workfront-cancellation-visual1.png "Fluxo de trabalho de estado de sessão do Workfront para o Learning Manager")

## Casos de uso

As funções a seguir estão envolvidas em um cancelamento iniciado no Workfront.

### Funções envolvidas

| Função | Descrição |
|---|---|
| Gerente de entrega | Agenda e gerencia o calendário de treinamento no Workfront, incluindo o cancelamento de sessões. Os gerentes de entrega não usam a interface do usuário do Learning Manager. A migração é o único caminho pelo qual o cancelamento chega ao Learning Manager. |
| Administrador de sistemas | Executa a migração por meio da API. Essa função opera o pipeline Workfront para Learning Manager e é separada do gerente de entrega e do administrador do Learning Manager. |
| Administrador | Gerencia os dados do curso e da sessão na interface do usuário do Learning Manager. Os administradores não precisam mais cancelar as sessões manualmente após serem informados sobre uma alteração no Workfront. |
| Autor | Possui o conteúdo do curso e da sessão na interface do usuário do Learning Manager. |
| O professor | É atribuído a sessões. Os professores veem o estado de sessão correto e são notificados quando uma sessão que instruem é cancelada. |
| Aluno | Está inscrito em uma sessão pelo Learning Manager. Os alunos são avisados imediatamente quando a sessão é cancelada. |

### Cenários comuns

| Cenário | O que você faz | Resultado |
|---|---|---|
| Uma sessão é cancelada no Workfront, por exemplo, porque um recurso está indisponível ou um fornecedor tem um problema. | Defina o estado da sessão como Cancelado na linha de migração da sessão e execute a migração. | A sessão é cancelada no Learning Manager e as pessoas afetadas são notificadas. |
| Os detalhes de uma alteração de sessão ativa no Workfront. | Inclua os valores alterados na linha de migração. Defina o estado da sessão como Ativo ou deixe-o em branco. | A sessão é atualizada. O Learning Manager envia um e-mail de sessão atualizada. |
| Uma sessão cancelada é restabelecida no Workfront. | Defina o estado da sessão como Ativo na linha de migração e execute a migração. | A sessão se torna ativa e pode ser modificada e cancelada novamente. |
| Os detalhes atualizados são enviados para uma sessão cancelada sem definir o estado como Ativo. | Nenhuma ação é necessária do usuário. | A sessão permanece cancelada, a linha retorna um erro de validação e nenhum detalhe é alterado. |
| Uma linha de migração não inclui um estado de sessão. | Deixe a coluna em branco ou omita-a. | O estado atual da sessão no Learning Manager permanece inalterado. |

## Principais recursos

* **Coluna de estado da sessão.** O esquema de migração inclui um campo de estado de sessão opcional que suporta Ativo e Cancelado.
* **Cancelamento por meio da migração.** Quando uma linha tem o estado Cancelado, a sessão correspondente no Learning Manager é cancelada. O Learning Manager usa a mesma chave de correspondência que a migração já usa para criar e atualizar sessões.
* **Nenhum trabalho manual no Learning Manager.** Os administradores não precisam cancelar a sessão novamente na interface de usuário.
* **Mesmo comportamento do cancelamento na interface do usuário.** O controle de inscrição, a visibilidade voltada para o aluno, os relatórios, a trilha de auditoria e as notificações correspondem a um cancelamento da interface do usuário.
* **Reativação.** Você pode definir uma sessão cancelada de volta para Ativa definindo o estado explicitamente nos dados de migração.
* **Proteção para sessões canceladas.** A migração não altera os detalhes de uma sessão cancelada, a menos que a linha defina explicitamente o estado como Ativo.
* **Compatibilidade com versões anteriores.** A coluna de estado é opcional, portanto os arquivos de migração existentes continuam a funcionar sem alterações.
* **Notificações concluídas.** Alunos, professores, administradores, autores e gerentes recebem os mesmos emails de cancelamento que recebem em um cancelamento na interface do usuário.

## Estados da sessão

Cada sessão no Learning Manager está em um de dois estados.

| Estado | Significado |
|---|---|
| Ativo | O estado padrão. A sessão é ao vivo e os alunos podem se inscrever e participar dela. |
| Cancelado | A sessão foi cancelada. Alunos, administradores, autores e gerentes inscritos são notificados, pois solicitam o cancelamento na interface do usuário. |

### Regras de transição de estado para migração

A tabela a seguir mostra o que acontece quando uma linha de migração é processada. O Learning Manager identifica a sessão usando a chave de correspondência que a migração já usa para criar e atualizar.

| Estado atual no Learning Manager | Estado da sessão na linha de migração | Resultado |
|---|---|---|
| A sessão não existe | Ativo ou em branco | A sessão é criada como ativa. |
| Ativo | Ativo ou em branco | A sessão permanece ativa. Os valores alterados na linha são aplicados. |
| Ativo | Cancelado | A sessão é cancelada e as notificações são enviadas. |
| Cancelado | Cancelado | A linha foi ignorada. Uma sessão cancelada não pode ser cancelada novamente. |
| Cancelado | Ativo | A sessão é reativada. Os valores alterados na linha são aplicados. |
| Cancelado | Em branco | A sessão permanece cancelada. Se a linha tiver valores alterados, um erro de validação será retornado e nenhum detalhe será alterado. |

### Regras para a coluna de estado de sessão

* A coluna é opcional em todas as linhas.
* Quando a coluna estiver vazia, a sessão será atualizada para Ativa.
* Uma sessão se torna ativa novamente por meio da migração somente quando a coluna diz explicitamente Ativo.

Use um dos seguintes valores na coluna de estado da sessão:

* `state = Active`
* `state = Cancelled`

>[!NOTE]
>
>O cabeçalho de coluna exato e os valores aceitos estão sendo confirmados. Use os nomes especificados pela documentação de migração.

## Atualizações de sessões canceladas

Não é possível atualizar os detalhes de uma sessão cancelada por meio da migração. Se uma linha de uma sessão cancelada contiver valores alterados e não definir o estado como Ativo, o Learning Manager retornará um erro de validação, deixará a sessão cancelada e não aplicará nem armazenará os detalhes alterados. O Learning Manager não envia um e-mail atualizado sobre a sessão para a tentativa.

### Cancelar uma sessão usando a migração

Use este procedimento quando uma sessão tiver sido cancelada no Workfront e você quiser que o Learning Manager reflita a alteração.

**Antes de começar**

* A sessão já existe no Learning Manager, importada por meio da migração de Workfront para Learning Manager.
* Você sabe a chave correspondente que a migração usa para identificar a sessão.

1. No **Workfront**, cancele a sessão.
1. No arquivo CSV de sessão usado para migração, localize a linha da sessão. Certifique-se de que a chave correspondente seja a mesma usada quando a sessão foi criada.
1. Na coluna de estado da sessão, insira **Cancelado**.
1. Execute a migração por meio da API.
1. No Learning Manager, verifique se a sessão foi cancelada.

O Learning Manager marca a sessão como cancelada, trata os alunos inscritos como faz em um cancelamento na interface do usuário e envia as notificações de cancelamento. Nenhuma ação é necessária na interface do usuário do Learning Manager.

>[!NOTE]
>
>Se a sessão já estiver cancelada, o Learning Manager ignora a linha.

### Atualizar uma sessão ativa

Para uma sessão ativa, o comportamento da atualização de migração existente permanece disponível. Defina o estado da sessão como Ativo ou deixe-o em branco e inclua os valores alterados na linha. Você pode continuar a atualizar detalhes como a data e a hora, o professor, o local ou o link e a capacidade por meio do pipeline de migração.

Ativo mantém o comportamento de criação e atualização existente. Cancelado chama o mesmo cancelamento de sessão que a interface de usuário fornece, por meio da migração do CSV da sessão.

### Reativar uma sessão cancelada

Uma sessão cancelada retorna ao estado ativo somente quando você define o estado como Ativo explicitamente. Você pode reativar uma sessão por meio da migração ou editando-a na interface do usuário.

1. No arquivo CSV da sessão, localize a linha da sessão cancelada. Certifique-se de que a chave correspondente seja a mesma usada quando a sessão foi criada.
1. Na coluna de estado da sessão, digite Ativo.
1. (Opcional) Atualize quaisquer outros valores na linha que deseja alterar, como data e hora, professor, local ou link ou capacidade.
1. Execute a migração por meio da API.

A sessão se torna ativa e seus detalhes podem ser modificados. Uma sessão que é reativada por meio da migração ou da interface do usuário pode ser cancelada novamente em qualquer caminho.

>[!IMPORTANT]
>
>Se você enviar detalhes atualizados de uma sessão cancelada sem definir o estado como Ativo, a sessão permanecerá cancelada e a linha retornará um erro de validação.

## Notificações

O Learning Manager envia todos os e-mails enviados para cancelamento na interface do usuário quando uma sessão é cancelada durante a migração. A cobertura do destinatário não é reduzida e o conteúdo usa o mesmo modelo, portanto, os destinatários não podem dizer como o cancelamento foi iniciado.

Os recipients, conforme aplicável à sessão, são os seguintes.

| Destinatário | Notificação |
|---|---|
| Alunos | Os alunos inscritos na sessão são informados de que a sessão foi cancelada. |
| Professores | Os professores atribuídos à sessão são notificados do cancelamento. |
| Gerentes | Os gerentes recebem a notificação de cancelamento. |

### Emails para sessões canceladas

Uma sessão cancelada não gera e-mails atualizados por sessão. Enquanto uma sessão é cancelada, as alterações na data e hora, professor, local ou link e capacidade não acionam o e-mail de atualização da sessão. Somente as notificações de cancelamento e reativação se aplicam a uma sessão cancelada.

## Considerações e limitações

* Como o recurso usa a migração, um cancelamento feito no Workfront entra em contato com o Learning Manager quando a migração é executada. O cancelamento em tempo real baseado em webhook não é compatível.
* A migração não pode alterar os detalhes de uma sessão cancelada. Para alterá-las, primeiro defina o estado como Ativo.
* A coluna de estado da sessão é opcional. As linhas que a omitem nunca alteram o estado de uma sessão.
* O recurso estende a integração de migração existente. Ele não adiciona um segundo caminho de integração em tempo real.
* O agendamento ou acionador de migração depende das ferramentas que sua organização usa para executá-la. Este guia não define um agendamento fixo.
* Os gerentes de entrega trabalham somente no Workfront. Eles não precisam de acesso à interface do usuário do Learning Manager para cancelar uma sessão.

## Medidas de sucesso

| Medida | Target |
|---|---|
| Cancelamentos que os administradores ou o suporte ao cliente replicam manualmente | Reduzido para 0 em um ciclo de lançamento completo após a inicialização. |
| Cancelamentos do Workfront refletidos no Learning Manager | 100% dos eventos de cancelamento processados em um ciclo de migração. |
| Paridade de notificação entre interface de usuário e cancelamentos de migração | 0 lacunas na cobertura do destinatário (administradores, autores, gerentes e alunos) e 0 e-mails de atualização desnecessários para sessões canceladas. |

## Solução de problemas

| Problema | Causa esperada ou possível | Ação |
|---|---|---|
| Uma sessão permanece ativa após ser cancelada no Workfront. | A migração ainda não processou o cancelamento ou a linha de migração não tinha o estado Cancelado explícito. | Verifique a entrada da migração e o resultado do processamento. |
| Os detalhes de uma sessão cancelada não são alterados. | Comportamento esperado enquanto a sessão permanece cancelada. | Reative a sessão definindo o estado como Ativo e, em seguida, aplique as alterações. |
| Nenhum email de atualização de sessão é enviado para uma sessão cancelada. | Comportamento esperado. Os emails de atualização comuns são suprimidos nas sessões canceladas. | Use o ciclo de vida de cancelamento e reativação em vez de uma atualização somente de detalhes. |
| Uma linha de cancelamento foi ignorada. | A sessão correspondente no Learning Manager já foi cancelada. | Nenhum cancelamento adicional é necessário. Reative a sessão primeiro se precisar voltar para ativo. |
| Um destinatário recebeu o mesmo email de cancelamento de um cancelamento na interface de usuário. | Comportamento esperado. O cancelamento da migração foi projetado para corresponder à interface do usuário. | Nenhuma ação é necessária. |
| O comportamento não é claro quando o estado da sessão está em branco. | Os requisitos de origem estão em conflito na manipulação de estado em branco. | Confirme o comportamento da autorização antes de confiar em um estado em branco para qualquer transição. |
