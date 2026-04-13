---
description: Saiba mais sobre como definir Configurações avançadas no Adobe Learning Manager
jcr-language: en_us
title: Configurações avançadas no Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 34%

---


# Configurações avançadas no Adobe Learning Manager

## Etiquetas de catálogo

As etiquetas de catálogo no Adobe Learning Manager são usadas para marcar objetos de aprendizado (cursos, certificações, programações de aprendizado etc.) com campos e valores específicos. Esses rótulos ajudam você e os autores a categorizar e organizar conteúdo de maneira eficaz, permitindo melhor filtragem, rastreamento e emissão de relatórios.

Consulte [Etiquetas de catálogo no Adobe Learning Manager](/help/migrated/administrators/feature-summary/catalog-labels.md) para obter mais informações.


>[!NOTE]
>
>* Rótulos obrigatórios: você pode optar por tornar os rótulos do catálogo obrigatórios para os autores durante a criação do curso.
>* Fluxo de trabalho do autor: os autores devem adicionar rótulos de conformidade ao criar ou editar cursos para garantir a categorização adequada.

## Pasta de conteúdo

As pastas de conteúdo permitem organizar e gerenciar conteúdo criando pastas privadas ou públicas. Essa funcionalidade garante que o conteúdo seja acessível apenas a autores ou grupos específicos, fornecendo melhor controle sobre a visibilidade e o gerenciamento do conteúdo.

**Pontos principais:**

Uma pasta é um repositório de conteúdo, que é um subconjunto de toda a biblioteca de conteúdo disponível em uma conta com as seguintes propriedades:

* Somente você (administrador) pode criar, editar ou excluir uma pasta.
* Você pode controlar o acesso a pastas como parte da definição de funções somente para administradores personalizados.
* O conteúdo deve estar sempre associado a pelo menos uma pasta. Para começar, todo o conteúdo será associado à pasta pública, que pode ser alterada posteriormente.
* O conteúdo pode ser associado a várias pastas no momento da criação, o que também será possível através de operações de cópia.
* Todos os nomes de pastas devem ser exclusivos dentro da conta, caso contrário, ocorrerá um erro ao nomear uma pasta.

As pastas controlam apenas a visibilidade do conteúdo e não criam cópias do conteúdo. Portanto, a edição de conteúdo refletirá em todas as pastas associadas.

**Pasta pública**

Uma pasta pública está sempre presente em uma conta e, inicialmente, todo o conteúdo será parte dessa pasta. Mais tarde, os autores podem mover o conteúdo dessa pasta para outras pastas. Uma pasta pública tem as seguintes propriedades:

* Por padrão, todo o conteúdo associado a essa pasta estará acessível a todos os tipos de autores.
* Qualquer conteúdo que faça parte de uma pasta pública não pode fazer parte de nenhuma outra pasta. O inverso também é verdadeiro.

Esta pasta não pode fazer parte da definição de função configurável. Consequentemente, não ter uma pasta pública na definição de função configurável não restringe o acesso a uma pasta pública.

**Pasta particular**

Qualquer pasta criada por você é uma pasta privada.

**Adicionar uma pasta de conteúdo**

Para adicionar uma pasta de conteúdo, siga as etapas:

1. Selecione **[!UICONTROL Configurações]** > **[!UICONTROL Pasta de Conteúdo]**.
2. Selecione **[!UICONTROL Adicionar]** para criar uma nova pasta.
3. Digite o nome e a descrição da pasta a ser criada.

   ![texto alternativo](assets/advanced-settings-picture1.png)

4. Selecione **[!UICONTROL Salvar]** para criar a pasta.

**Operações de pasta**

* **[!UICONTROL Adicionar uma pasta]**: para adicionar uma pasta, selecione-a e, em seguida, selecione **[!UICONTROL Adicionar]** no canto superior direito da tela.
* **[!UICONTROL Excluir uma pasta]**: para excluir uma pasta, selecione a pasta a ser excluída, selecione o menu **[!UICONTROL Ações]** e selecione **[!UICONTROL Excluir Pasta]**.

## Locais de sala de aula

Criar e gerenciar uma biblioteca de locais de sala de aula física ou virtual. Esses locais podem ser usados por autores e administradores para configurar eventos de ILT (Instructor-Led Training, treinamento ministrado por instrutor). O recurso garante que os detalhes da sala de aula, como limites de vagas e informações de local, sejam pré-configurados e facilmente acessíveis.

Consulte [Adicionar locais de sala de aula no Adobe Learning Manager](/help/migrated/administrators/feature-summary/classroom.md) para obter mais informações.

## Relatórios

Esta seção permite configurar os painéis de controle de Conformidade e Sucesso do Grupo.

![texto alternativo](assets/advanced-settings-picture2.png)

Consulte o seguinte para obter mais informações:

* [Painel de conformidade](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Painel de Sucesso do Grupo](/help/migrated/administrators/feature-summary/group-success-dashboard.md)


