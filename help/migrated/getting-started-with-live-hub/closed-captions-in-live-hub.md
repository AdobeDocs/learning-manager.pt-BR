---
title: Legendas ocultas em sessões do Live Hub
description: Saiba como as legendas ocultas exibem conteúdo falado em tempo real para que professores e alunos possam acompanhar durante as sessões do Live Hub.
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 574ba5fd9ac9dc02130a39006574c9ca1ce6c1d1
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 4%
---

# Entenda as legendas codificadas

As legendas ocultas são geradas automaticamente durante uma sessão do Live Hub e atualizadas continuamente enquanto os participantes falam. As legendas aparecem em uma área de exibição dedicada e são exibidas no idioma selecionado pelo professor em **Configurações da sala**.

Professores e participantes podem exibir legendas. Cada participante pode mostrar ou ocultar legendas de maneira independente, sem afetar as configurações de legenda de outros participantes.

Somente professores podem alterar o idioma da legenda. Os participantes podem exibir apenas as legendas no idioma escolhido pelos professores. Os participantes não podem alterar o idioma das legendas.

## Como o Live Hub determina o idioma da legenda

O Live Hub seleciona automaticamente o idioma da legenda com base na seguinte ordem de prioridade:

1. **Idioma do curso:** o Live Hub usa o idioma do curso se houver suporte para legendas. Para um curso multilíngue, se a instância do curso atual usar um idioma que não oferece suporte a legendas codificadas, o Live Hub seleciona o idioma da primeira instância do curso que oferece suporte a legendas codificadas. Exiba [Idiomas com suporte no ALM](../../migrated/languages-supported.md) para obter mais informações.
1. **Idioma da conta:** se não houver suporte para o idioma do curso, o Live Hub verificará o idioma da conta e o usará, se houver suporte.

>[!NOTE]
>
>Se nem o idioma do curso nem o idioma da conta for suportado, o Live Hub seleciona o inglês como o idioma da legenda. Além disso, as legendas são desativadas por padrão e devem ser ativadas manualmente.

## Idiomas com suporte para legendas ocultas

O Live Hub oferece suporte a legendas codificadas nos seguintes idiomas:

* Inglês
* Francês
* Alemão
* Chinês
* Espanhol
* Italiano
* Japonês
* Português
* Dinamarquês
* Holandês
* Finlandês
* Turco
* Coreano
* Norueguês
* Sueco
* Russo

## Como funcionam as legendas codificadas

Em uma sessão do Live Hub, as legendas codificadas são geradas automaticamente. As legendas são exibidas em um painel dedicado e atualizadas continuamente conforme os participantes falam. Professores e Alunos podem exibir legendas.

Cada participante pode mostrar ou ocultar legendas da maneira que preferir. A alteração dessa configuração não afeta outros participantes.

![](assets/closed-captions-overview.png)
*Interface do Live Hub mostrando as legendas codificadas na sessão*

## Funções e permissões

O recurso **legendas ocultas** está disponível para professores e alunos em uma sessão do Live Hub. As ações disponíveis variam de acordo com a função do usuário.

| **Professores** | **Alunos** |
|---|---|
| [Exibir legendas codificadas](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#display-closed-captions) | [Exibir legendas codificadas](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#display-closed-captions) |
| [Alterar a aparência das legendas codificadas](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#change-the-appearance-of-closed-captions) | [Alterar a aparência das legendas codificadas](../getting-started-with-live-hub/manage-closed-captions-as-a-learner.md#change-the-appearance-of-closed-captions) |
| [Selecionar o idioma da legenda](../getting-started-with-live-hub/manage-closed-captions-as-an-instructor.md#select-the-caption-language) | |