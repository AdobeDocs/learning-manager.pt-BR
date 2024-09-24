---
description: Crie, atribua e modifique habilidades e níveis.
jcr-language: en_us
title: Criar e modificar habilidades e níveis
contentowner: manochan
exl-id: b1461900-43e8-4e9d-bef1-a55c44d3bc8b
source-git-commit: b9809314014fcd8c80f337983c0b0367c060e348
workflow-type: tm+mt
source-wordcount: '1721'
ht-degree: 79%

---

# Criar e modificar habilidades e níveis

Crie, atribua e modifique habilidades e níveis.

O mapa de habilidades é um agrupamento dos conjuntos de habilidades, conhecimentos e características do funcionário de uma empresa. Esses mapas de habilidades ajudam companhias/empresas a definir ou aumentar as expectativas do desempenho de seus funcionários. As habilidades permitem que os funcionários conciliem suas condutas às expectativas da empresa.

O Adobe Learning Manager permite mapear o desempenho dos alunos com base em seu conjunto de habilidades através do mapa de habilidades. Quando os alunos terminam de realizar alguns cursos, eles podem saber sua classificação em relação a cada habilidade visualizando o mapa de habilidades.

O objetivo fundamental das habilidades no LMS do Learning Manager é fornecer ao administrador uma ferramenta que alinhe a aprendizagem com os objetivos comerciais.

## Adicionar uma habilidade {#addaskill}

Como administrador, você pode fazer o seguinte:

* Mapear um domínio para uma habilidade.
* Adicionar vários níveis de uma habilidade.
* Adicionar uma medalha a um nível.

Para adicionar uma habilidade, siga as etapas abaixo:

1. No painel esquerdo, selecione **[!UICONTROL Habilidades]** > **[!UICONTROL Adicionar]** > **[!UICONTROL Adicionar SKills]**. Dê um nome e faça uma descrição da habilidade.

   ![](assets/add-skill-name-anddescription.png)

   *Adicionar nome e descrição de uma habilidade*

1. Atribua um domínio à habilidade. Ao criar uma habilidade, você pode mapeá-la com os domínios de habilidade mais relevantes suportados pelo Learning Manager. Para obter mais informações, consulte [***Mapear habilidade com domínios***](/help/migrated/administrators/feature-summary/curation-skills.md).

   Comece a digitar o domínio no campo e você poderá ver as recomendações. Escolha a opção ou as opções mais relevantes para a habilidade.

   ![](assets/map-domain-with-skills.png)

   *Adicionar um domínio*

1. Atribua os níveis à habilidade. Para adicionar um nível, clique em **[!UICONTROL Adicionar]**.

   Você pode criar e atribuir habilidades aos funcionários. Há vários níveis de habilidades e cada nível requer um determinado número de créditos a ser obtido.

   Você pode atribuir um máximo de três níveis a uma habilidade. O caminho de aprendizagem é inscrever alunos em vários objetos de aprendizado, o que se converte em um determinado número de créditos que atendem aos requisitos dos diversos níveis de habilidade.

   Depois de concluir os objetos de aprendizado (LOs) e obter os níveis de habilidade, os alunos estão preparados para passar para um nível mais produtivo.

   ![](assets/add-skill-levels.png)

   *Adicionar níveis de habilidade*

   Ao adicionar uma habilidade, você também pode atribuir decimais aos créditos. Os créditos são exibidos com até duas casas decimais.

   O suporte a casas decimais está disponível somente em inglês.

1. Escolha uma medalha para o nível. Na lista suspensa **[!UICONTROL Medalha]**, selecione a imagem que deve ser usada como medalha para tal nível.
1. Para salvar as alterações, clique em **[!UICONTROL Salvar]**.

   Após criar a habilidade, você pode colocar a habilidade recém-criada na página **[!UICONTROL Habilidade]**. Você também pode ver os domínios e uma breve descrição da habilidade. Você também pode ver os níveis e os créditos que foram atribuídos a cada nível.

   ![](assets/list-of-skills.png)

   *Exibir lista de habilidades*

## Atribuir a habilidade aos alunos {#assigntheskilltolearners}

Os administradores podem atribuir habilidades aos alunos.

Depois de criar e salvar as habilidades, elas serão listadas na página de habilidades. Agora, você pode começar a atribuir essas habilidades aos alunos da seguinte forma:

1. Na página **[!UICONTROL Habilidade]**, clique no hiperlink com o número de alunos inscritos na habilidade. Em uma habilidade recém-criada, o número de alunos em todos os níveis é zero.

   ![](assets/number-of-learnersenrolledtoaskill.png)

   *Exibir alunos atribuídos a uma habilidade*

   Neste exemplo, adicione alunos no nível 1. Clique no hiperlink ao lado do nível 1.

1. Na caixa de diálogo Alunos, clique em **[!UICONTROL Adicionar alunos]**.

   ![](assets/add-learners.png)

   *Adicionar alunos*

1. Procure os alunos e adicione-os. Você também pode adicionar grupos de usuários.

   ![](assets/search-and-add-learners.png)

   *Pesquisar e adicionar alunos*

1. Para salvar as alterações, clique em **[!UICONTROL Salvar]**.

   Depois que você atribui um aluno, todos os alunos de um grupo de usuários, se houver, são automaticamente inscritos na habilidade, por padrão. É possível fazer com que os alunos cancelem a inscrição automática clicando no botão **[!UICONTROL Inscrição automática]**.

   ![](assets/turn-off-auto-enrollment.png)

   *Desabilitar registro automático*

   Alunos individuais podem se inscrever automaticamente ou podem ser inscritos pelo administrador em um programa de aprendizado.

1. Depois de clicar em **[!UICONTROL Fechar]**, você pode ver o número total de alunos que foram atribuídos à habilidade que criou.

   Neste exemplo, há dois alunos individuais e três alunos de um grupo de usuários.

   ![](assets/learners-assignedtoaskill.png)

   *Número de alunos atribuídos a uma habilidade*

## Atribuir a habilidade a um curso {#assignskilltocourse}

Depois de criar a habilidade, o autor pode criar um curso e atribuir a habilidade ao curso.

![](assets/assign-skill-to-acourse.png)

*Atribuir habilidades a um curso*

Depois que o autor publica o curso, na página **[!UICONTROL Habilidade]**, você pode ver o total de cursos associados a um nível de habilidade, que aumenta quando a habilidade é atribuída a um novo curso.

![](assets/skill-assigned-tothecourse.png)

*Número de cursos associados a um nível de habilidade*

## Atribuir uma ajuda de tarefa à habilidade {#assignajobaidtotheskill}

As ajudas de tarefa são um conteúdo de treinamento a que os alunos podem ter acesso sem se inscrever em um objeto de aprendizado específico, como um curso ou programa de aprendizado.

Ao criar uma ajuda de tarefa, o autor pode associar um nível de habilidade a ela. Ao criar uma ajuda de tarefa sem nenhuma habilidade e associá-la a um curso com uma habilidade não vinculará a habilidade à ajuda de tarefa.

![](assets/create-a-job-aid.png)

*Criar uma ajuda de tarefa*

Na página **[!UICONTROL Habilidade]**, você pode ver o número de ajudas de tarefa associado ao nível de habilidade.

![](assets/job-aid-assignedtotheskill.png)

*Número de ajudas de tarefa de uma habilidade*

## Pesquisar uma habilidade {#searchskill}

Procure qualquer habilidade digitando o nome dela e escolhendo-a dentre as opções presentes. A pesquisa com preenchimento automático também é aplicável aqui.

Você pode pesquisar por habilidades nas seções **[!UICONTROL Ativo]** e **[!UICONTROL Retirado]** da página Habilidades.

## Editar uma habilidade {#editaskill}

Na página **[!UICONTROL Habilidade]**, clique na habilidade que deseja modificar. Na caixa de diálogo **[!UICONTROL Editar Habilidade]**, faça as alterações necessárias, por exemplo:

* Adicionando ou excluindo um domínio de habilidade.
* Editando o nome e a descrição da habilidade.
* Adicionando um nível de habilidade ou modificando um nível existente.
* Adicionando ou excluindo uma medalha de uma habilidade.

Depois de ter feito as alterações, clique em **[!UICONTROL Salvar]**.

## Retirar uma habilidade {#retireaskill}

Para retirar uma habilidade, na página **[!UICONTROL Habilidade]**, selecione a habilidade que deseja retirar.

No menu **[!UICONTROL Ações]**, no canto superior direito da página, clique em **[!UICONTROL Retirar]**.

Quando você retira uma habilidade, ela não aparece mais no curso.

Quando uma habilidade é retirada, ela não pode ser associada a mais cursos ou ajudas de tarefa nem atribuída aos alunos até que seja publicada novamente. As associações e as atribuições existentes não são afetadas pela retirada da habilidade.

## Republicar uma habilidade {#republishaskill}

Depois que a habilidade é retirada, ela é exibida na guia **[!UICONTROL Retirado]**. A guia mostra a lista de todas as habilidades retiradas.

Para republicar uma habilidade retirada, escolha a habilidade e, no menu **[!UICONTROL Ações]**, clique em **[!UICONTROL Republicar]**.

Isso restaura a habilidade e você pode vê-la novamente na guia **[!UICONTROL Ativo]**.

## Excluir uma habilidade {#deleteaskill}

Você pode excluir uma habilidade somente depois que ela tiver sido retirada.

Na guia **[!UICONTROL Retirado]**, selecione a habilidade que deseja excluir e, no menu **[!UICONTROL Ações]**, clique em **[!UICONTROL Excluir]**.

Você pode excluir uma habilidade somente quando ela não estiver associada a nenhum aluno nem a cursos e ajudas de tarefa.

## Atribuir habilidades a professores

Adicione um arquivo CSV que consiste nas habilidades dos professores. Essas habilidades são adicionadas à lista de habilidades.

1. No canto superior direito da tela, selecione **[!UICONTROL Adicionar]** > **[!UICONTROL Atribuir habilidades ao professor]**.
1. Faça upload de um csv. As colunas no CSV são:

   * Nome da habilidade
   * Nível da habilidade
   * E-mail do professor ou UUID do professor

   Para contas habilitadas para UUID, substitua a coluna E-mail do professor pela UUID do professor.

   Clique em Salvar.

   ![Adicionar CSV de habilidades de professor](assets/instructor-skills.png)

   *Adicionar habilidades de professor de um CSV*

1. Você verá uma mensagem pop-up de confirmação.

   Observação: a seguinte mensagem de erro será exibida se o CSV tiver campos incorretos.

   ![Mensagem de erro se o CSV tiver campos incorretos](assets/error-csv-upload.png)

   *Mensagem de erro para campos incorretos*

### Página Habilidades

Na página Habilidades, há uma coluna chamada Professores, que indica o número de professores atribuídos a uma habilidade. Se você clicar no número de professores, verá uma janela pop-up, que exibe os professores atribuídos à habilidade.

![Habilidades atribuídas aos professores](assets/instructor-skill-assigned.png)

*Página de habilidades*

### Baixar o CSV de atribuição de habilidades

1. Na página Habilidades, clique em **[!UICONTROL Adicionar]** > **[!UICONTROL Atribuir habilidades ao professor]**.
1. Na caixa de diálogo, clique em **[!UICONTROL Atribuição adicionada anteriormente]**.
1. O último CSV que você carregou será baixado.

>[!NOTE]
>
>Recomendamos que você baixe o CSV de atribuição de habilidades primeiro, edite-o e carregue o arquivo.

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como posso remover um aluno de uma habilidade?

Você não pode remover um aluno de uma habilidade. No entanto, você pode adicionar novos alunos ou grupos de usuários à habilidade.
+++

+++Como inscrever automaticamente os alunos em uma habilidade?

O recurso de inscrição automática é válido apenas para grupos de usuários. Quando você inscreve um grupo de usuários, por exemplo, Todos os autores, em uma habilidade e a salva, por padrão, a inscrição automática é ativada. Portanto, a habilidade também é atribuída a qualquer nova adição ao grupo de usuários Todos os autores.

Se você interromper a inscrição automática desse nível de habilidade para Todos os autores, todos os novos usuários adicionados ao grupo de usuários Todos os autores não terão a habilidade atribuída a eles.
+++

+++Como reiniciar o registro automático?

Inscreva o mesmo grupo de usuários no nível de habilidade novamente para o qual a Inscrição automática foi interrompida.

Isso reinicia a Inscrição automática e também atribui a habilidade aos alunos que foram adicionados ao grupo quando esse recurso estava desativado.

Ou seja, sempre que você reinscreve um grupo de usuários para iniciar a Inscrição automática, os membros do grupo são atualizados e a habilidade é atribuída a todos os membros atuais.
+++

+++Como posso atribuir uma habilidade a um curso?

Consulte a seção [Atribuir habilidades a um curso](skills-levels.md#assignskilltocourse) para obter mais informações sobre o procedimento.
+++

+++Como alterar um nível de habilidade?

Para alterar um ou mais níveis de uma habilidade, edite a habilidade e modifique as propriedades dos níveis existentes.
+++

+++Como ativar medalhas e habilidades para que estejam vinculadas à conclusão do curso?

As habilidades podem ser vinculadas à conclusão do curso ao criar um curso como autor. Na seção Configurações, você pode definir os critérios da habilidade para a conclusão do curso.

![](assets/course-skills.png)

Para ativar as medalhas na conclusão do curso, na secção **[!UICONTROL Instâncias]** do aplicativo Autor, ative a medalha necessária.
+++

+++Um administrador pode marcar uma medalha como concluída mesmo se a medalha mostrar “Em andamento”?

Um administrador pode marcar um objeto de aprendizado como concluído. A habilidade e as medalhas estão associadas ao objeto de aprendizado e não podem ser marcadas como **[!UICONTROL concluídas]** separadamente.

Em outras palavras, para obter a medalha, **é preciso completar o objeto de aprendizado associado**.
+++

### Mais itens similares

* [Habilidades e Adobe Learning Manager](https://elearning.adobe.com/2018/11/skills-captivate-prime/)
