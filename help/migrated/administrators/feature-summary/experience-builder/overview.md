---
description: Saiba mais sobre o Experience Builder, uma ferramenta sem código/de baixo código no Adobe Learning Manager que permite aos administradores criar e publicar páginas amigáveis e com marca sem conhecimento técnico especializado.
jcr-language: en_us
title: Experience Builder no Adobe Learning Manager
source-git-commit: b1225d4c1c322a75d97c813b0d97eb3229ffd35c
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 0%

---


# Visão geral

O Experience Builder é uma ferramenta sem código/de baixo código no Adobe Learning Manager que ajuda a criar portais de aprendizado personalizados. Ele permite que você crie portais de aprendizado de marca e intuitivos sem precisar de habilidades técnicas ou amplo conhecimento de codificação.

Com o Experience Builder, os administradores podem criar facilmente páginas, menus e widgets para fornecer experiências de aprendizado personalizadas sob medida para o público-alvo

Muitas organizações se esforçam para personalizar seus portais de aprendizado sem ajuda técnica ou integradores de sistema caros. Querem portais que combinem com a sua marca, forneçam conteúdo direcionado e se adaptem a diferentes grupos de alunos, sendo rápidos e fáceis de criar.

O Experience Builder é uma ferramenta sem código/de baixo código no Adobe Learning Manager que ajuda a criar portais de aprendizado personalizados. Ele permite que você crie portais de aprendizado de marca e intuitivos sem precisar de habilidades técnicas ou amplo conhecimento de codificação.
Com o Experience Builder, você pode criar novas páginas, menus e widgets para fornecer experiências de aprendizado personalizadas para seu público de maneira rápida e fácil. Com o Experience Builder, você pode criar rapidamente novas páginas, menus e widgets para fornecer experiências de aprendizado personalizadas para seu público-alvo.

## O problema que o Experience Builder resolve

O Experience Builder lida com os desafios comuns que as empresas enfrentam ao personalizar seus portais de aprendizado sem ajuda técnica significativa ou integradores de sistema caros. Ele preenche a lacuna entre duas opções principais:

* A experiência padrão pronta para uso, que oferece personalização limitada e pode fazer com que cada portal de aprendizado tenha uma aparência semelhante.
* Uma implementação sem periféricos, que permite portais totalmente personalizados e gamificados, mas apresenta desafios significativos, incluindo um longo tempo de entrada no mercado (geralmente de 3 a 6 meses), dependência de uma equipe de desenvolvimento e altos custos.

O Experience Builder oferece um meio-termo, permitindo a criação de portais de marca e jornadas de aprendizado exclusivas sem o alto custo e a sobrecarga de desenvolvimento de uma abordagem sem periféricos.

## Principais benefícios do uso do Experience Builder

A funcionalidade de usar páginas, widgets ou menus oferece vários benefícios importantes:

* **Fácil personalização**: você pode criar portais que correspondam precisamente à sua marca com cabeçalhos, rodapés, logotipos e layouts personalizados. A capacidade de injetar HTML personalizado, CSS e JavaScript fornece controle avançado para uma experiência de marca completa.
* **Aprendizado personalizado**: uma vantagem importante é a capacidade de fornecer experiências diferentes a alunos diferentes. Você pode configurar páginas e menus para grupos de usuários específicos (por exemplo, equipes de vendas, designers ou engenheiros), garantindo que eles vejam apenas o conteúdo relevante para eles. Isso é ideal para criar campanhas específicas de microaprendizagem para equipes ou períodos específicos.
* **Nenhuma interface de código/código baixo**: os administradores podem criar experiências de aprendizado por meio de uma interface visual guiada, em vez de escrever código. Essa abordagem permite que os administradores criem e gerenciem portais sofisticados de marca sem precisar de habilidades técnicas ou conhecimento extensivo de codificação.
* **Global e pronto para dispositivos móveis**: o Experience Builder oferece suporte à criação de páginas multilíngues para atender a diversos públicos globais e foi projetado para ser compatível com dispositivos móveis, garantindo uma experiência tranquila aos alunos em desktops, telefones e tablets.

## Casos de uso comuns

O Experience Builder pode ser usado para vários cenários de aprendizado que envolvem funcionários internos e usuários externos.

* **Portais de treinamento baseados em funções**: organizações com necessidades de treinamento departamentais específicas, como uma empresa financeira com equipes separadas de Vendas e Sucesso do Cliente, podem criar páginas de aprendizado dedicadas para cada grupo para garantir que o conteúdo seja altamente relevante.
* **Páginas de aprendizado específicas do evento**: você pode criar páginas temporárias e especializadas para eventos corporativos, como Tech Summit ou lançamento de vendas. Essas páginas podem apresentar informações de sessão, listas de oradores e um widget de calendário de eventos e podem ser direcionadas somente à equipe relevante por uma duração específica antes de reverter para a experiência padrão do portal.
* **Academias de clientes**: o Experience Builder permite que as agências criem academias voltadas para o cliente que refletem sua identidade de marca, obtendo uma experiência personalizada sem o tempo e o custo associados a uma compilação sem periféricos.

## Fluxos de trabalho de portal externos autenticados

As academias voltadas para o cliente criadas com o Experience Builder são gerenciadas inteiramente no Adobe Learning Manager. Esses portais usam a estrutura integrada de autenticação, permissões e segurança do Adobe Learning Manager.

Cada aluno externo deve fazer logon no Adobe Learning Manager e ser membro de pelo menos um grupo de usuários. No momento, o Experience Builder não é compatível com portais não autenticados ou públicos. Todas as experiências personalizadas exigem que os alunos façam logon no Adobe Learning Manager.

Os administradores podem usar a opção **[!UICONTROL Menu]** do Experience Builder para atribuir páginas personalizadas como páginas de aterrissagem para grupos de usuários específicos. Quando os alunos desse grupo fazem logon, o Adobe Learning Manager os direciona automaticamente para a página inicial atribuída, criando uma experiência personalizada e de marca para esse público, como treinamento de clientes, ativação de parceiros ou integração.

### Requisitos e limitações

* Autenticação necessária: conteúdo, páginas personalizadas e menus personalizados estão disponíveis somente para usuários autenticados no Adobe Learning Manager.
* Atribuição de grupo de usuários: os alunos devem ser adicionados aos grupos de usuários corretos para acessar as páginas iniciais e os menus designados.
* Páginas de aterrissagem com base em grupo: a configuração da página de aterrissagem se aplica a todos os membros de um grupo de usuários, garantindo experiências consistentes para públicos semelhantes.
* Escopo de personalização: o Experience Builder oferece suporte para personalização ampla de interface e layout usando widgets, HTML e iFrames. No entanto, integrações avançadas, como comércio eletrônico, SSO federado ou conexões de dados externos, podem exigir uma implementação híbrida ou sem periféricos.

### Fluxo de trabalho de configuração do portal externo

* Definir grupos de usuários: crie ou identifique grupos no ALM que representem seus públicos externos (por exemplo, clientes, parceiros ou distribuidores). Exiba [Grupos de usuários no Adobe Learning Manager](/help/migrated/administrators/feature-summary/user-group.md) para obter mais informações sobre grupos de usuários.
* Atribuir alunos aos grupos: adicione cada aluno externo ao grupo de usuários apropriado para que ele seja direcionado para a experiência de portal correta após o logon.
* Páginas do portal de design: use o Experience Builder para criar páginas com marca com widgets do Adobe Learning Manager, HTML e componentes do iFrame. Exiba [Criar uma página personalizada no Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/create-a-page.md) para obter mais informações.
* Configurar menus e páginas iniciais: no Criador de menus, atribua a cada grupo de usuários um menu exclusivo e designe sua página de portal personalizada como a página inicial. Exiba [Criar um menu](/help/migrated/administrators/feature-summary/experience-builder/create-a-menu.md) para obter mais informações.
* Teste e Publish: verifique a navegação, a visibilidade do conteúdo e o roteamento de páginas para cada grupo de usuários antes de publicar o portal.
