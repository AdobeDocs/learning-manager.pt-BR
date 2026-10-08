---
description: Como os planos de cobrança determinam se as contas podem compartilhar licenças licenciadas e o que acontece com os relacionamentos de compartilhamento quando um plano é alterado
jcr-language: en_us
title: Classificação por níveis - compartilhamento de estações
exl-id: 42b4cba4-1e44-40d8-aa57-ce2a855be258
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%
---

# Compartilhamento de vagas e planos de conta no Adobe Learning Manager

O compartilhamento de vagas permite que uma conta compartilhe uma parte de suas licenças licenciadas com outra conta, para que os alunos da conta de recebimento possam acessar o Adobe Learning Manager usando licenças da conta de compartilhamento. Quais contas podem compartilhar licenças e com quem, depende do plano de faturamento de cada conta.

## Quais planos oferecem suporte ao compartilhamento de licenças

O compartilhamento de vagas está disponível para contas no plano **Ultimate**. As contas no plano **Prime** não podem compartilhar licenças com outra conta e não podem receber licenças compartilhadas de outra conta.

As contas cobradas com cartão de crédito estão no plano Prime por padrão e, portanto, não são elegíveis para participar do compartilhamento de vagas.

As contas de avaliação são a única exceção: uma conta de avaliação pode receber licenças compartilhadas de uma conta do Ultimate. Enquanto um relacionamento de compartilhamento ativo estiver em vigor, a conta de avaliação terá acesso a recursos de nível mais avançado.

## Visibilidade da configuração de contas entre parceiros

A configuração de conta entre parceiros ficará visível no aplicativo do administrador da conta que compartilha esse recurso.

>[!NOTE]
>
>Se sua conta compartilha licenças com contas adicionais além da que você recebe licenças, por exemplo, se sua conta passa o acesso compartilhado junto a uma terceira conta, cada conta nessa cadeia deve estar no plano Ultimate para compartilhamento para continuar trabalhando de ponta a ponta.

## Combinações de conta que oferecem suporte ao compartilhamento de licenças

A tabela a seguir mostra se o compartilhamento de licenças é possível entre diferentes combinações de planos de conta.

| Conta de compartilhamento (pai) | Conta de recebimento (filho) | Compartilhamento compatível? |
|---|---|---|
| Prime (qualquer) | Qualquer | Não, o compartilhamento de licenças é restrito a contas de plano Ultimate |
| Ultimate | Ultimate | Sim |
| Ultimate | aplicativo | Não, incompatibilidade de planos |
| Ultimate | Uma conta faturada com cartão de crédito | Não, incompatibilidade de plano, pois as contas faturadas com cartão de crédito estão no plano Prime |
| Ultimate | Teste | Sim, a conta de avaliação recebe acesso de nível Ultimate enquanto o relacionamento está ativo |

>[!NOTE]
>
>Algumas restrições adicionais no compartilhamento de licenças entre configurações de conta específicas podem ser aplicadas independentemente do tipo de plano, por exemplo, com base em como a assinatura de uma conta foi originalmente configurada. Se você não conseguir estabelecer um relacionamento de compartilhamento entre duas contas Ultimate, entre em contato com o suporte da Adobe para confirmar a configuração da sua conta.

## O que acontece com o compartilhamento de licenças quando um plano é alterado

A qualificação de compartilhamento de vagas é avaliada na renovação. Se o plano de uma conta for alterado de uma forma que afete uma relação de compartilhamento existente, acontece o seguinte:

* Se o plano de uma conta de compartilhamento (pai) for alterado de Ultimate para Prime na renovação, seus relacionamentos de compartilhamento de assento existentes terminarão.
* Se a conta de recebimento tiver sua própria assinatura independente, essa assinatura não será afetada; somente o próprio relacionamento de compartilhamento será encerrado.
* Se a conta de recebimento for uma conta de avaliação que depende do acesso definitivo da conta pai, ela será revertida para o acesso no nível do Prime assim que o relacionamento de compartilhamento for encerrado.

Essas alterações entrarão em vigor na próxima renovação da conta para contas do ALM existentes, não imediatamente durante um período de contrato ativo. No entanto, eles não se aplicam a novas contas criadas após o recurso de classificação por níveis ter entrado em vigor.

>[!NOTE]
>
>As contas cobradas com cartão de crédito que atualmente têm acesso de nível superior serão transferidas para o plano Prime a partir de sua próxima renovação. Se essa conta tiver quaisquer relações de compartilhamento de sede ativas nesse ponto, essas relações terminarão como parte da mesma transição.
