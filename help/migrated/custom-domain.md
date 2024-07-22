---
jcr-language: en_us
title: Suporte para domínio personalizado
description: Domínios personalizados não são suportados em uma instância do Azure no Learning Manager.
contentowner: saghosh
exl-id: 162ce268-48e3-4c7e-acb1-5181cebbb18d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 67%

---

# Suporte para domínio personalizado

Domínios personalizados não são suportados em uma instância do Azure no Learning Manager.

## Visão geral {#overview}

O suporte ao domínio personalizado permite que os clientes obtenham controle completo sobre o nome de domínio que podem usar na conta do Learning Manager. Um cliente precisa comprar o domínio personalizado separadamente e trabalhar com a equipe da Adobe para configurá-lo como URL de logon para a sua plataforma de aprendizado.

Isso permite que o cliente rotule a experiência de logon e acesso, de modo que os usuários não vejam nenhuma presença da Adobe ou do Adobe Learning Manager.

Por exemplo, você gostaria de personalizar seu domínio para que os usuários tenham a mesma experiência como se estivessem no domínio Adobe. Se a ABC Inc quiser treinar seus clientes, ela gostaria que eles pousassem em um domínio chamado `abc.com/mylearning`, em vez de `learningmanager.adobe.com/abc-inc/mylearning`.

>[!NOTE]
>
>Como pré-requisito, você deve registrar o domínio e, em seguida, o Adobe o guiará pela personalização do url.


O recurso de domínio personalizado está disponível por um custo adicional. Entre em contato com seu gerente de sucesso do cliente para saber mais detalhes.

* Para a função de aluno, o domínio começará com `https://cdn.<customer_custom_domain>/` Por exemplo, `https://cdn.elearningstage1.cpdomaintest.in/`
* Para todas as outras funções, o domínio começará com `https://<customer_custom_domain>/`. Por exemplo, `https://elearningstage1.cpdomaintest.in/`

`<customer_custom_domain>` é a parte personalizável.

## Como configurar um domínio personalizado em uma conta {#howtosetupacustomdomainonanaccount}

Como pré-requisito, um cliente deve possuir um nome de domínio e comprar o domínio de um provedor.

Por exemplo: consideremos que um cliente possui um domínio fictício, **acme.com**. O cliente deseja que o conteúdo do Learning Manager seja fornecido de **learning.acme.com**.

Siga as etapas abaixo para configurar um domínio personalizado.

1. O cliente deve **adicionar três registros CNAME** no domínio:

   * **learning.acme.com:** ponto de extremidade público ALB do Learning Manager compartilhado pelo Adobe
   * **lrs.learning.acme.com:** ponto de extremidade público ALB apontado por learning.acme.com
   * **cdn.learning.acme.com:** ponto de extremidade CDN compartilhado por Adobe

1. O cliente deve fornecer certificados SSL para estes domínios:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. A Adobe fará upload desses certificados SSL no AWS ALB para atender solicitações para os domínios.
1. A Adobe adicionará learning.acme.com em seu certificado SAN.
1. A Adobe gerará os metadados do provesor de serviço para o cliente, pois os metadados conterão os URLs de domínio personalizados.

   * Se o cliente desejar iniciar sessão em redes sociais, então a Adobe deve incluir os padrões de URL de redirecionamento dos sites de redes sociais na lista de URLs permitidos.
   * Se o cliente ativou o SSO, o cliente deve trabalhar com o seu IDP para incluir os domínios nos URLs de redirecionamento. O cliente deve compartilhar o XML de metadados IDP com a Adobe. A Adobe deve atualizar as configurações de SSO da conta do cliente.

1. A Adobe modificará as regras do CORS S3 para incluir o domínio do cliente.
