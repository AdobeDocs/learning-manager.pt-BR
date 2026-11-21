---
description: Saiba como os professores e gerentes de coortes obtêm resumos por email da atividade do quadro de discussão e como gerenciar configurações e assinantes com APIs
jcr-language: en_us
title: Notificações do professor no quadro de discussão
exl-id: 370c9add-5572-4555-8a95-ddb470c230f4
source-git-commit: 650ec8159a4291189dfc38b03701b7b96932233d
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Notificações do professor no quadro de discussão

## Visão geral

As notificações do professor no quadro de discussão fornecem aos professores, gerentes de coorte e administradores um resumo por e-mail das atividades recentes nos quadros de discussão que monitoram. Isso é útil para professores que gerenciam vários grupos e participam de vários painéis ao mesmo tempo.

Um gerente de coorte é a pessoa que gerencia um grupo de alunos (uma coorte) que passam por um curso ou programa juntos no mesmo agendamento.

Em vez de abrir cada painel individualmente, os professores recebem alertas no aplicativo em tempo real e um resumo por email, na frequência configurada, para os painéis em que estão inscritos. Você gerencia as configurações de assinaturas e notificações do painel por meio da [`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-sequence) e da [API de assinantes](api-changes-dec-2026.md#api-get-subscribers).

## Principais recursos

* Você pode inscrever usuários ativos do Adobe Learning Manager em quadros de discussão selecionados usando a API de assinantes ([`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users), escopo `admin:write`). Um usuário deve ter acesso ao painel quando as notificações são enviadas.
* Os usuários recebem notificações no aplicativo em tempo real sobre os tipos de evento ativados e uma compilação por email agrupada por quadro. Os tipos de evento são controlados pelas configurações no nível de conta (`notifyNewPost`, `notifyComment` e `notifyReply`) na API [`boardSubscriptionSettings`](api-changes-dec-2026.md#api-sequence).
* A janela de resumo é o período de tempo cuja atividade é coletada em um e-mail de resumo. Defina-o no nível da conta com o atributo `digestFrequencyHours`, de 1 a 168 horas (por exemplo, 24 horas para uma compilação diária). Aplica-se a todos os usuários na conta.
* Você pode inscrever usuários por ID ou endereço de email e adicionar vários usuários em uma solicitação ([assinaturas em massa](api-changes-dec-2026.md#bulk-subscriptions)). Os usuários são criados no Learning Manager normalmente primeiro.
* O e-mail de resumo lista cada nova publicação, comentário e resposta para os tipos de evento ativados, com o nome do painel, o nome do autor e o endereço de e-mail, e um link direto. Ele também mostra uma contagem das atualizações desde o início do período de resumo.
* A API `boardSubscriptionSettings` e a API de assinantes são APIs públicas, portanto, você pode gerenciar configurações e assinaturas sem uma interface de usuário (integrações orientadas por API).

## Casos de uso

Os seguintes casos de uso mostram como as notificações do professor ajudam:

| Caso de uso | Como a notificação ajuda |
|---|---|
| Monitorar várias coortes | Um professor responsável por vários grupos pode receber atividade resumida dos conselhos associados a esses grupos. |
| Revisar o envolvimento do aluno | Um Gerente de Coorte pode monitorar novas contribuições e identificar discussões ativas sem verificar cada conselho separadamente. |
| Monitorar conversas de acompanhamento | Comentários e respostas incluídos na compilação ajudam os professores a identificar discussões que podem exigir orientação ou moderação. |

## Considerações importantes

* Um usuário deve ser capaz de acessar um painel quando uma notificação é enviada. O acesso é verificado novamente no momento da entrega, não apenas quando o usuário está inscrito. Se um assinante perder o acesso a um painel, a assinatura será mantida, mas as notificações para esse painel serão ignoradas.
* O resumo é enviado como um e-mail, portanto, um quadro ocupado pode ficar muito longo. Por exemplo, uma coorte de cerca de 40 alunos podia postar várias centenas de comentários em seis horas.
* Se as placas estiverem muito ativas, use uma frequência de compilação mais curta, como a cada seis horas, para que cada e-mail permaneça gerenciável. Defina a frequência com `digestFrequencyHours` na API [`boardSubscriptionSettings` ](api-changes-dec-2026.md#api-create-settings).
* O número de publicações no resumo por email é limitado a 20 por painel por resumo. O mesmo limite aplica-se independentemente às observações (20) e respostas (20) por conselho de administração. Apenas as listas exibidas estão truncadas; as contagens de títulos/subtítulos sempre refletem a atividade verdadeira e não truncada da janela.
* O número de assinantes é limitado a 200 por placa.
* Como o conteúdo é enviado diretamente no email, e não como um anexo, o corpo do email também tem um limite de tamanho.

## Modelo de assinatura, permissões e qualificação

* Um assinante é um usuário que recebe notificações de um painel. Uma assinatura do painel é independente do relacionamento de acompanhamento existente com o usuário do painel.
* Qualquer pessoa que se autentique com o OAuth e tenha os escopos `admin:read` e `admin:write` pode usar as configurações de assinatura e as APIs de assinantes. `admin:read` permite listar assinantes e ler configurações. `admin:write` permite adicionar ou remover assinantes e alterar configurações.
* Você pode assinar qualquer usuário do Learning Manager, mas o usuário deve existir, estar ativo e ter acesso ao painel para receber notificações. O acesso é verificado novamente quando notificações e resumos são enviados.
* Se um usuário perder o acesso, a entrega desse painel será ignorada e a assinatura será mantida. A entrega será retomada se o acesso retornar.
* É possível adicionar vários usuários a um painel em uma solicitação (assinaturas em massa). Se um usuário já estiver inscrito, a solicitação ainda será bem-sucedida e nenhuma duplicata será criada. Consulte [Assinaturas em massa](api-changes-dec-2026.md#bulk-subscriptions) para o formato de solicitação, a resposta de Status Múltiplo 207 e os casos de falha.

## Conteúdo de resumo

### Eventos incluídos

O resumo inclui novas postagens, comentários e respostas quando a configuração correspondente for `true` na API [`boardSubscriptionSettings` ](api-changes-dec-2026.md#api-create-settings): `notifyNewPost`, `notifyComment` e `notifyReply`. Você os definiu com `POST` ou `PATCH /boardSubscriptionSettings`. Todas as configurações são `false` por padrão.

### Eventos excluídos

O resumo exclui eventos cuja configuração correspondente na API [`boardSubscriptionSettings` ](api-changes-dec-2026.md#api-create-settings) (por exemplo, `notifyComment`) é `false`. Nenhuma compilação é enviada quando não há nenhuma atividade qualificada.

### Amostra de layout de email de resumo

Um e-mail de resumo é enviado para cada painel inscrito que tinha uma atividade qualificada. Está estruturado da seguinte forma:

* **Linha de resumo:** o email é aberto com o número total de atualizações no painel (por exemplo, sete atualizações) e uma divisão por tipo (por exemplo, novas postagens e comentários), juntamente com o tempo a partir do qual a atividade é contada.
* **Seção do painel:** a atividade está agrupada sob o nome do painel. Cada post está listado abaixo dele.
* **Detalhes do item:** cada postagem, comentário ou resposta mostra o nome e o endereço de email do usuário que o criou, além de um link para o item.
* **Links:** selecionar um link abre diretamente a postagem, o comentário ou a resposta. O destinatário deve estar conectado para que o link seja aberto.
* **Comentários e respostas:** eles aparecem no mesmo email que publicações, para que os professores possam ver conversas de acompanhamento juntamente com novos tópicos.

## Configurar notificações

### Definir configurações usando APIs

Você gerencia notificações por meio de duas APIs públicas: a [`boardSubscriptionSettings` API](api-changes-dec-2026.md#api-sequence), que se aplica no nível da conta, e a [API de assinantes](api-changes-dec-2026.md#api-get-subscribers), que se aplica a cada quadro. Ambos usam os escopos OAuth `admin:read` e `admin:write`. Chame-os nesta sequência:

1. Defina as configurações no nível da conta com [`POST /boardSubscriptionSettings`](api-changes-dec-2026.md#api-create-settings).
1. Altere as configurações posteriormente, quando necessário, com [`PATCH /boardSubscriptionSettings`](api-changes-dec-2026.md#api-update-settings).
1. Recupere as configurações no nível da conta com [`GET /boardSubscriptionSettings`](api-changes-dec-2026.md#api-get-settings).
1. Liste os usuários inscritos em um painel com [`GET /boards/{id}/subscribers`](api-changes-dec-2026.md#api-get-subscribers).
1. Inscreva usuários em um painel com [`POST /boards/{id}/subscribers`](api-changes-dec-2026.md#api-subscribe-users).
1. Cancelar a assinatura de um usuário de um painel com [`DELETE /boards/{id}/subscribers/{userId}`](api-changes-dec-2026.md#api-unsubscribe-user).

Use a API `boardSubscriptionSettings` para definir a frequência de resumo em horas e ativar ou desativar postagens, comentários e respostas para o resumo. Por exemplo, uma conta com uma frequência de resumo de 1 hora recebe um e-mail de resumo a cada hora. Todas as configurações de evento são `false` por padrão.

### Gerenciar assinantes

Use a API de assinantes para escolher quais usuários ativos do Learning Manager estão inscritos em quais painéis. Uma assinatura é separada do relacionamento de acompanhamento do painel existente. Um usuário deve ter visibilidade de um painel para receber suas notificações, o que significa que o usuário deve estar conectado. A perda de visibilidade suprime a entrega, mas não remove a assinatura.

### Ativar o recurso

Para habilitar as notificações do professor, crie as configurações no nível da conta e inscreva os usuários nos painéis, conforme descrito em [Alterações na API em novembro de 2026](api-changes-dec-2026.md). Depois disso, o sistema coleta novas publicações, comentários e respostas criados durante o intervalo configurado. No final do intervalo, os assinantes recebem uma notificação resumida que abrange a atividade qualificada nos painéis inscritos.

Saiba mais sobre as alterações de API em [Alterações de API em dezembro de 2026](api-changes-dec-2026.md).
