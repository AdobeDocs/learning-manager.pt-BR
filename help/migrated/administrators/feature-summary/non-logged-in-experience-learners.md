---
title: Experiência não conectada para alunos
description: O portal nativo do Adobe Learning Manager oferecerá suporte a uma forma não registrada de acessar o site de treinamento. Com esse modo ativado, os alunos podem descobrir e acessar o site de treinamento e verificar vários cursos e conteúdos disponíveis. A experiência não conectada permite que os alunos naveguem nos cursos sem estar conectados a um portal.
source-git-commit: aef2dfe9d6f49dcccaf1f71b57ffa25a3075efe8
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# Experiência não conectada para alunos

O portal nativo do Adobe Learning Manager oferecerá suporte a uma forma não registrada de acessar o site de treinamento. Com esse modo ativado, os alunos podem descobrir e acessar o site de treinamento e verificar vários cursos e conteúdos disponíveis.

A experiência não conectada permite que os alunos naveguem nos cursos sem estar conectados a um portal.

Para que a página inicial não conectada seja ativada, o administrador de integração deve ativar e configurar o [Conector de dados de treinamento](/help/migrated/integration-admin/feature-summary/connectors.md#training-data-access).

O treinamento pode ser exportado do conector.

>[!NOTE]
>
>Verifique se a opção Learning Manager nativo está selecionada.

O administrador pode modificar e configurar a página inicial, que se destina a usuários não conectados.

## Iniciar as opções da página inicial

Na página inicial do Adobe Learning Manager, selecione **Marca**. Em seguida, no painel esquerdo, selecione Não conectado na página inicial.

![opções da página inicial](assets/non-logged-in-homepage.png)

*Selecione a opção Não conectado na página inicial*

## Adicionar um banner

Adicione um banner a qualquer anúncio de marketing ou destaque os tópicos em alta do dia. Selecionar **Adicionar banner**.

![banner](assets/add-banner-image.png)

*Adicionar um banner*

Navegue até o local da imagem a ser usada como banner. Em seguida, forneça um link como um botão de ação na imagem do banner.

## Adicionar categorias

Este componente pode ser usado para filtrar o catálogo por marcas, habilidades e catálogo. Esta seção contém um cabeçalho e uma descrição para cada categoria. Ao clicar, o usuário é redirecionado para a página do catálogo com os filtros aplicados.

Selecionar **[!UICONTROL Adicionar categoria]**. Em seguida, insira os detalhes da categoria.

![adicionar categoria](assets/add-category.png)

*Adicionar as categorias*

Salve a categoria. A categoria é adicionada à seção.

## Adicionar um catálogo

Adicione um catálogo para usuários não conectados para que eles possam navegar por todo o treinamento na plataforma.

![adicionar catálogo](assets/add-catalog.png)

*Adicionar um catálogo*

Todo o treinamento exportado estará presente.

## Recursos sem suporte

* As ajudas de tarefa não serão exportadas. No entanto, os alunos podem vê-las depois de fazer logon.
* Classificar por no componente de catálogo.
* Configuração de exibição padrão usada no aplicativo do administrador (Configurações > Geral > Exibição de lista).
* Classificação por estrelas/eficácia.
* Configuração do ícone de cartão.
* Configuração de habilidades e tags relevantes.
* Exibição do aplicativo do aluno exibida em todo o catálogo.
* Páginas de visão geral de treinamento: clicar no cartão redireciona para Inscrever-se, após o qual um usuário é redirecionado para a página de visão geral de treinamento/página de instância.
* Todos os catálogos habilitados estarão presentes. Qualquer aluno que não tenha acesso a um catálogo não poderá ver o catálogo e o treinamento nele após fazer logon.
