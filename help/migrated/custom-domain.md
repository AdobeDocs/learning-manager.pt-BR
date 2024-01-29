---
jcr-language: en_us
title: Suporte para domínio personalizado
description: Domínios personalizados não são suportados em uma instância do Azure no Learning Manager.
contentowner: saghosh
source-git-commit: 8635072782253cbac3f913953797cae7c0bc5ef4
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---



# Suporte para domínio personalizado

Domínios personalizados não são suportados em uma instância do Azure no Learning Manager.

## Visão geral {#overview}

O suporte ao domínio personalizado permite que os clientes obtenham controle completo sobre o nome de domínio que podem usar na conta do Learning Manager. Um cliente precisa comprar o domínio personalizado separadamente e trabalhar com a equipe do Adobe para configurá-lo como seu URL de logon para sua plataforma de aprendizado.

Isso permite que o cliente rotule a experiência de logon e acesso, de modo que os usuários não vejam nenhuma presença de Adobe ou Adobe Learning Manager.

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

Como exemplo, vamos considerar que um cliente possui um domínio fictício, **acme.com**. O cliente deseja que o conteúdo do Learning Manager seja fornecido de **learning.acme.com**.

Siga as etapas abaixo para configurar um domínio personalizado.

1. O cliente precisa **adicionar três CNAME** registros no domínio:

   * **learning.acme.com:** Ponto de extremidade público ALB do Learning Manager compartilhado pelo Adobe
   * **lrs.learning.acme.com:** Ponto de extremidade público ALB apontado por learning.acme.com
   * **cdn.learning.acme.com:** Ponto de extremidade CDN compartilhado por Adobe

1. O cliente deve fornecer certificados SSL para estes domínios:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. O Adobe fará upload desses certificados SSL para o AWS ALB para atender solicitações aos domínios.
1. O Adobe adicionará learning.acme.com ao certificado de SAN.
1. O Adobe gerará os metadados SP para o cliente, pois os metadados conterão os URLs de domínio personalizados.

   * Se o cliente desejar fazer logon em redes sociais, o Adobe deverá incluir os padrões de URL de redirecionamento dos sites de redes sociais na lista de URLs permitidos.
   * Se o cliente ativou o SSO, ele deve trabalhar com o IDP para incluir seus domínios nos urls de redirecionamento. O cliente deve compartilhar o XML de metadados do IDP com o Adobe. O Adobe deve atualizar as configurações de SSO da conta do cliente.

1. O Adobe então modificará as regras do CORS S3 para incluir o domínio do cliente.
