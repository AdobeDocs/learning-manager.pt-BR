---
jcr-language: en_us
title: Configurar armazenamento de Creative Cloud para o Adobe Learning Manager Content Composer
description: Saiba como configurar o armazenamento de Creative Cloud para o Adobe Learning Manager Content Composer. Este guia explica por que o armazenamento do Creative Cloud é necessário, como os administradores podem atribuir a oferta de associação gratuita no Adobe Admin Console e como solucionar problemas de acesso relacionados ao armazenamento.
contentowner: saghosh
source-git-commit: 15e1f5c383442fb93706acdf68eb889c16511859
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 0%

---


# Configurar armazenamento de Creative Cloud para o Adobe Learning Manager Content Composer

>[!IMPORTANT]
>
>Para quem este documento se destina: administradores que precisam ativar o armazenamento de Creative Cloud para usuários do Adobe Learning Manager para que possam acessar e usar o Compositor de conteúdo. É especialmente útil para administradores que solucionam problemas de erros de logon ou acesso relacionados ao armazenamento e que atribuem a oferta de associação gratuita por meio do Adobe Admin Console.


O compositor de conteúdo do Adobe Learning Manager (ALM) requer que os usuários tenham armazenamento de Creative Cloud associado à sua conta de Adobe. Os usuários que não têm armazenamento de Creative Cloud podem não conseguir acessar o Compositor de conteúdo e podem encontrar erros de logon ou relacionados ao acesso.

Para ajudar as organizações a provisionar armazenamento para os usuários afetados, o Adobe oferece uma oferta de associação gratuita que os administradores podem atribuir por meio do Adobe Admin Console. Esta oferta inclui armazenamento em Creative Cloud e pode ser usada quando um usuário ainda não tem um plano que forneça direitos de armazenamento.

## Antes de começar

Verifique se:

* Você tem acesso de administrador do Adobe Admin Console.
* O usuário que precisa de acesso ao Compositor de conteúdo é identificado.
* Você verificou se o usuário já tem um plano que inclui armazenamento em Creative Cloud.

## Por que os usuários precisam de armazenamento de Creative Cloud

O Content Composer usa armazenamento de Creative Cloud para armazenar cursos. Os usuários que não possuem armazenamento atribuído ao seu perfil de Adobe podem receber um erro ao tentar usar o Compositor de conteúdo.

![Erro de armazenamento do Compositor de Conteúdo](../assets/coco-storage1.png)

Muitos clientes de Adobe já têm armazenamento de Creative Cloud por meio de produtos Adobe existentes e não são afetados. No entanto, alguns clientes da Adobe Learning Manager podem não ter armazenamento provisionado por padrão e podem precisar de um administrador para ativá-lo.

## Ativar armazenamento de Creative Cloud gratuito para usuários

Se um usuário não tiver armazenamento em Creative Cloud, atribua a oferta de associação gratuita da Adobe Admin Console.

1. Entre no [Adobe Admin Console](https://adminconsole.adobe.com/) usando uma conta com privilégios de administrador. Somente os administradores podem atribuir produtos e ofertas aos usuários.
2. No Admin Console, selecione Produtos > Versões de avaliação e ofertas especiais.

   ![Versões de avaliação e ofertas especiais em Admin Console](../assets/coco-storage2.png)

3. Encontre a oferta de associação gratuita que está disponível em Avaliações e ofertas especiais. Esta é a oferta discutida como o método recomendado para ativar o armazenamento em Creative Cloud para usuários que ainda não têm direitos de armazenamento.

   ![Oferta de associação gratuita](../assets/coco-storage3.png)

4. Atribua a oferta de associação gratuita aos usuários necessários. A atribuição só pode ser concluída por um administrador com as permissões de Admin Console apropriadas.
5. Após a atribuição, verifique se o usuário tem armazenamento em Creative Cloud disponível e peça para ele fazer logon novamente no Compositor de conteúdo.

## Armazenamento fornecido por meio de associação gratuita

Os usuários com a oferta de associação gratuita recebem aproximadamente 2 GB de armazenamento em Creative Cloud, o que permite que eles usem o Compositor de conteúdo.

## Solução de problemas

**O usuário recebe um erro ao acessar o Compositor de Conteúdo**

Verifique se o usuário tem armazenamento em Creative Cloud disponível em seu perfil de Adobe.

**O usuário não pode ver a oferta de associação gratuita**

Confirme se:

* Você fez logon como administrador.
* Você está visualizando a área Produtos do Adobe Admin Console.
* A organização está qualificada para acessar a oferta.

## Perguntas frequentes

**Todos os usuários da Adobe Learning Manager recebem armazenamento de Creative Cloud automaticamente?**

Não. Alguns usuários do ALM podem não ter armazenamento provisionado por padrão e podem exigir direitos adicionais por meio da oferta de associação gratuita.

**Os usuários podem habilitar o armazenamento por conta própria?**

Não. O direito de armazenamento deve ser atribuído por um administrador de Adobe através de Admin Console.

**O armazenamento de Creative Cloud é necessário para o Compositor de Conteúdo?**

Sim O Compositor de conteúdo depende dos usuários terem armazenamento em Creative Cloud associado à sua conta de Adobe.

**O que os administradores devem fazer se um usuário encontrar um erro relacionado ao armazenamento?**

Verifique se o usuário tem direito de armazenamento de Creative Cloud. Caso contrário, atribua a oferta de associação gratuita por meio do Adobe Admin Console e peça ao usuário para tentar novamente.

**O que os administradores devem fazer se ainda tiverem problemas de acesso ou direito?**

Se o administrador do Adobe Admin Console enfrentar um problema ao atribuir armazenamento de Creative Cloud ou ao depurar problemas relacionados ao acesso, o problema pode exigir suporte no nível de conta corporativa. Nesses casos, entre em contato com o Suporte para corporações da Adobe por meio das opções de suporte disponíveis em Admin Console.

Para obter mais informações, consulte [Opções de suporte para Adobe corporativos](https://helpx.adobe.com/br/business/enterprise/get-help/support-options/support-for-enterprise.html)
