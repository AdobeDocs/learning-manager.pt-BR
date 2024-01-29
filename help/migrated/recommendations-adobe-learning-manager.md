---
title: Recommendations no Adobe Learning Manager
description: O núcleo do mecanismo de recomendação é orientado pelo novo algoritmo de classificação de cursos do Learning Manager. O algoritmo usa 50 milhões de pontos de dados e cinco anos de dados de aprendizado agregados em milhões de usuários para classificar os cursos com base na probabilidade de inscrição. Essa classificação garante que a maioria dos cursos inscritos seja exibida antecipadamente para os alunos.
source-git-commit: 40f6732147b7babeb1f11ce52045e6baf6338ce1
workflow-type: tm+mt
source-wordcount: '1435'
ht-degree: 0%

---



# Recommendations no Adobe Learning Manager

O Adobe Learning Manager introduziu um novo e renovado sistema de recomendação para cursos. Esse recurso de recomendações usa algoritmos de IA e interesses de usuários, como produtos, funções e níveis, para fornecer recomendações de conteúdo personalizadas.

O novo sistema de recomendações permite criar parâmetros personalizados que os alunos podem selecionar para receber recomendações personalizadas. Essas recomendações serão exibidas como Cursos, Caminhos de aprendizado e Certificações para os alunos no feed da página inicial.

Para começar a usar este recurso, você deve ativá-lo no aplicativo do administrador.

## Ativar e configurar as recomendações

1. Faça upload dos dados do curso e do usuário (opcional).
1. Faça as alterações em tempo real.
1. Depois de ativar e configurar as recomendações, carregue os dados no Adobe Learning Manager para que as recomendações comecem a funcionar. Esses dados consistem em:

   * Dados do curso
   * Dados do usuário (opcional)

## Algoritmo de classificação do curso

O núcleo do mecanismo de recomendação é orientado pelos novos **[!UICONTROL Algoritmo de classificação do curso]**. O algoritmo usa 50 milhões de pontos de dados e cinco anos de dados de aprendizado agregados em milhões de usuários para classificar os cursos com base na probabilidade de inscrição. Essa classificação garante que a maioria dos cursos inscritos seja exibida antecipadamente para os alunos.

## Termos chave

O novo mecanismo de recomendação baseado em IA do Learning Manager fornece aos líderes de aprendizado um sistema de recomendação configurável baseado em parâmetros para criar uma experiência personalizada para os alunos.

Os parâmetros são - **Produtos/tópicos**, **Funções** e **Níveis**. Além disso, esses parâmetros podem ser renomeados para atender às suas necessidades. Portanto, “produtos” podem se tornar “tópicos” ou “funções” podem se tornar “região”.

## Configurar o sistema de recomendação

O novo mecanismo de recomendação do Adobe Learning Manager simplifica o fluxo de trabalho do administrador envolvido na configuração de recomendações personalizadas, pois os dados sobre produtos e funções associados a um cliente/parceiro geralmente estão disponíveis para os administradores (por exemplo, a partir de registros de compra).

Há principalmente três workflows envolvidos na configuração do novo mecanismo de recomendação:

* Admin
* Autor
* Aluno

Os administradores configuram os valores de parâmetro Produtos, Funções e Níveis da conta. Por exemplo, um provedor de soluções de TI com bancos como sua base de clientes principal pode configurar o parâmetro “Produto” para ter valores como Gateway de Pagamento, Armazenamento Seguro na Nuvem, Sistema de Detecção de Fraude, Plataforma de Negociação etc. e o parâmetro “Função” para ter valores como Especialista em Integração, Administrador de Rede, Analista de Risco, Responsável pela Conformidade etc.

Os administradores recebem um fluxo de trabalho guiado no Learning Manager para configurar o mecanismo de recomendação e personalizar o mecanismo de acordo com o caso de uso da conta. Além disso, os administradores também têm a opção de configurar recomendações PRL por meio de um upload de CSV único.

1. Selecionar **[!UICONTROL Recommendations]** no aplicativo de administração.

   ![Selecionar Recommendations no aplicativo de administração](assets/image831538.png)

   *Selecione a opção Recommendations*

1. Clique em **[!UICONTROL Atualizar]**.

   ![Atualizar para o novo sistema](assets/image784236.png)

   *Selecione a opção Atualizar*

1. Clique em **[!UICONTROL Continuar]** para atualizar para o novo sistema de recomendação.

   ![Prosseguir para o novo sistema](assets/image521152.png)
   *Selecione o botão Continuar*

1. Crie os parâmetros de recomendação para Produtos e Funções.

   ![Criar os parâmetros](assets/image43406.png)
   *Criar parâmetros para recomendação*

1. Clique em **[!UICONTROL Adicionar mais valores]**.
1. Adicione os produtos. Digite o nome de um produto e pressione Enter.

   Você deve adicionar pelo menos dois produtos para começar a usar.

   ![adicionar produtos](assets/image623058.png)
   *Adicionar produtos*

1. Adicione as funções. Digite os nomes das funções e pressione Enter.

   ![adicionar funções](assets/image156786.png)
   *Adicionar as funções*

1. Clique em **[!UICONTROL Continuar]**.

   Os Produtos e as Funções agora aparecem na lista de Parâmetros.

   ![produtos e funções](assets/image266930.png)
   *Lista de produtos e funções*

## Preparação dos dados

Os dados de interesse do usuário, Produto, Funções e Níveis devem ser carregados para que as recomendações funcionem corretamente.

**Opções de upload de dados**

O recurso de recomendações é configurável. Portanto, em vez de produtos/funções/níveis, você pode usar tópicos/funções/nível ou escolher qualquer uma destas opções: somente produto/tópicos, somente funções, somente produto/tópicos e funções, somente níveis de funções ou somente níveis de produtos.

Com base na configuração de recomendação escolhida, modifique as folhas de dados adequadamente.

A seção a seguir explica a opção mais ampla de usar produtos, funções e níveis.

O administrador deve fazer upload dos dados do usuário em um formato predeterminado. Os dados carregados serão alimentados no algoritmo de recomendação, para que um aluno receba recomendações para os cursos certos com base em suas funções e níveis.

**Pré-requisitos**

Para fazer upload dos dados para que as recomendações funcionem, preencha os Produtos, Funções e Níveis nos CSVs do Usuário e do RecommendationLO.

Como parte do exercício de preparação de dados, estamos fornecendo dois modelos CSV:

**RecUser.csv**

* ID do usuário
* Produtos
* Funções
* Níveis (Iniciante, Intermediário ou Avançado)

Veja a seguir um exemplo de registros no csv:

| ID do usuário | Produtos | Funções | Níveis |
|--- |--- |--- |--- |
| 123 | Ciência de dados | Analista | Analista: intermediário |
| 456 | Aerospace Engg | Técnico | Técnico: Avançado |

**RecLO.csv**

* Treinamento
* Tipo de treinamento
* Nome do treinamento
* Produtos
* Funções
* Níveis
* Tags
* Habilidades

Veja a seguir um exemplo de registros no csv:

| ID do treinamento | Tipo de treinamento | Nome do treinamento | Produtos | Funções | Níveis | Tags | Habilidades |
|---|---|---|---|---|---|---|---|
| 111 | CURSO | Python 101 | Ciência de dados | Analista | Analista: intermediário | dados | Geral |
| 222 | CURSO | Julia 101 | Ciência de dados | Analista | Analista: avançado | dados | Geral |

Preencha esses CSVs e entre em contato com sua equipe de sucesso do cliente para baixar os formatos e fazer upload desses CSVs.

## Disponibilize as recomendações

Após o upload de ambos os CSVs, clique em Ativar. Isso tornará o novo sistema de recomendação visível para os alunos.

![colocar ao vivo](assets/computerdescription-automatically.png)
*Disponibilize as recomendações*

O sistema de recomendação agora está disponível para seus alunos.

## Editar um parâmetro

1. Na lista de parâmetros, selecione o ícone de três pontos e selecione **[!UICONTROL Editar nome do parâmetro]**.

   ![Editar parâmetro](assets/edit-parameter.png)

1. Altere o nome do parâmetro e clique em **[!UICONTROL Salvar]**.

   ![resultados](assets/image688522.png)
   *Editar o parâmetro*

## Excluir um parâmetro

1. Na lista de parâmetros, selecione o ícone de três pontos e selecione **[!UICONTROL Excluir parâmetro]**.

![excluir parâmetro](assets/delete-parameter.png)
*Excluir o parâmetro*

## Página de configurações do curso

Na página de configurações de um curso, as recomendações para produtos e funções são listadas. Os alunos serão recomendados para este curso se tiverem manifestado interesse nestes produtos e funções.

![configuração de imagem](assets/course-settings-image.png)
*Página de configurações do curso*

## Exibição do aluno

Para uma conta com recomendações baseadas em PRL configuradas, quando um aluno faz logon na plataforma de aprendizado, um fluxo de trabalho guiado ajuda o aluno a configurar recomendações com base em seu produto, função e preferências de nível. Isso cria o perfil do aluno para o mecanismo de recomendação analisar.

Os alunos em contas que mudaram para o novo sistema de recomendação podem visualizar os cursos e treinamentos recomendados.

Os alunos podem ver o seguinte:

* Produtos, Funções - Níveis: os alunos são solicitados a selecionar Produtos primeiro, Funções e depois Níveis para cada uma das funções selecionadas
* Produto - Níveis: os alunos são solicitados a selecionar Produtos primeiro e, em seguida, Níveis para cada um dos produtos selecionados
* Funções - Níveis: os alunos são solicitados a escolher Funções primeiro e, em seguida, Níveis para cada função selecionada.
* Produtos e funções: os alunos são solicitados a escolher Produtos primeiro e, em seguida, Funções.
* Produtos: os alunos são solicitados a selecionar apenas os produtos.
* Funções: os alunos são solicitados a escolher apenas funções.

Depois de selecionar Recommendations no painel esquerdo, o aluno vê um pop-up para configurar as recomendações.

![configurar recomendações](assets/image575540.png)
*O aluno configura a recomendação*

Clicar em Configurar Recommendations leva o aluno ao pop-up de seleção de produto.

![pop-up de seleção de produto](assets/product-selection-popup.png)
*Selecionar produtos*

Em seguida, no próximo pop-up, o aluno pode selecionar a função.

![selecionar função](assets/image270860.png)
*Selecionar funções*

O aluno pode adicionar os níveis.

![adicionar níveis](assets/image650040.png)
*Selecionar níveis*

## Faixas de aprendizado no aplicativo do aluno

Um aluno pode ver as seguintes faixas no aplicativo:

* Minha tira de aprendizado
* Remover com widget de calendário, redes sociais e gamificação
* Salvo por mim tira
* Faixa super relevante
* Faixa do produto - 1
* Faixa do produto - 2
* Faixa de descoberta
* Faixa recomendada pelo administrador
* Procurar por tira de catálogo

### Cartões na minha tira de aprendizado

![cartões de tira de aprendizado](assets/image770606.png)
*Cartões na tira de aprendizado*

Cada cartão possui classificação, imagem do cartão, título, habilidade, data de publicação, autor, duração, barra de progresso e o botão Continuar ou Explorar.

### Cartões salvos por mim tira

![cartões salvos](assets/cards-saved-by-me.png)
*Cartões salvos*

Cada cartão tem classificação, imagem do cartão, título, habilidade, data de publicação, autor, duração, barra de progresso e botão Iniciar ou Explorar ou Continuar ou Rever.

Não há barra de progresso no cartão depois que um aluno inicia o curso. Um aluno também pode Cancelar o salvamento do curso.

### Cartões em faixa super relevante

![cartões de strip super relevantes](assets/super-relevant-cards.png)
*Cartões relevantes*

Cada cartão tem classificação, imagem do cartão, título, habilidade, data de publicação, autor, duração, barra de progresso e botão Iniciar ou Explorar ou Continuar ou Rever.

Não há barra de progresso no cartão depois que um aluno inicia o curso.

No menu, há duas opções: **[!UICONTROL Salvar]** e **[!UICONTROL Não recomendar]**. Se o aluno clicar **[!UICONTROL Salvar]**, o curso é salvo na faixa “Salvo por mim”. Se o aluno clicar **[!UICONTROL Não recomendar]**, o treinamento recomendado será removido da lista.
