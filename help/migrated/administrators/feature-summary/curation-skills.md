---
jcr-language: en_us
title: Mapear habilidades com domínios de habilidades
description: Para que o Mecanismo de curadoria por AI selecione automaticamente uma publicação de usuário para um domínio de habilidade específico, a empresa do usuário precisa ter mapeado suas habilidades personalizadas nos domínios de habilidade presentes no LMS do Learning Manager.
contentowner: kuppan
exl-id: 46db9d92-fe88-4850-ae06-d434062fa2bf
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 90%

---

# Mapear habilidades com domínios de habilidades

Para que o Mecanismo de curadoria por AI selecione automaticamente uma publicação de usuário para um domínio de habilidade específico, a empresa do usuário precisa ter mapeado suas habilidades personalizadas nos domínios de habilidade presentes no LMS do Learning Manager.

Ao criar uma habilidade, o administrador pode mapeá-la com os domínios de habilidade mais relevantes suportados pelo Learning Manager. Posteriormente, isso será levado em conta no processo de curadoria automática. O LMS do Learning Manager lista as seguintes habilidades:

* Gestão de cadeia de suprimento
* Contabilidade
* Pesquisa científica e engenharia
* Segurança da computação
* Gestão estratégica
* Redes sociais
* Medicina
* Finanças
* Segurança no trabalho
* Habilidades interpessoais
* Direito empresarial
* Gestão
* Gestão de recursos humanos
* Comunicação técnica
* Ética empresarial
* Gerenciamento de relacionamento com o cliente
* Tecnologia da informação
* Produção e fabricação
* Marketing
* Gestão da qualidade
* Processo empresarial
* Aprendizado
* Design
* Análise
* Vendas

>[!NOTE]
>
>De acordo com o algoritmo, se a pontuação de confiança for inferior a 50%, o conteúdo é marcado para curadoria manual.


Siga as etapas abaixo para adicionar um domínio de habilidades:

1. No painel esquerdo do Admin Console, clique em **[!UICONTROL Habilidades]**.
1. Para adicionar uma habilidade, clique em **[!UICONTROL Adicionar]** no canto superior direito da página.
1. Na caixa de diálogo **[!UICONTROL Adicionar habilidade]**, adicione uma habilidade e sua descrição.
1. Na seção **[!UICONTROL Domínio de habilidades]**, adicione os domínios de habilidades. Ao digitar um domínio, vários domínios aparecem. Esses domínios são preenchidos a partir da lista mencionada.

   ![](assets/skill-domain-mapping.png)

   *Adicionar os domínios de habilidade na seção Domínio de Habilidade*

1. Para salvar as alterações, clique em **[!UICONTROL Salvar]**.

Quando um usuário publica conteúdo em um painel, o conteúdo é selecionado e pode acabar aprovado ou rejeitado, dependendo da pontuação de confiança em relação à habilidade mapeada no painel.

<!--![](assets/content-uploaded.png)-->

Se o conteúdo carregado tiver uma pontuação de confiança acima de 50%, ele será enviado ao painel. Se o conteúdo atender aos critérios, você receberá uma notificação informando que o conteúdo foi selecionado com êxito e já está disponível no painel.

![](assets/curation-notification.png)

*Exibir notificações dependendo da pontuação de confiança*
