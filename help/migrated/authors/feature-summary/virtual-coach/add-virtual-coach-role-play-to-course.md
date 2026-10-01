---
description: Saiba como publicar uma interpretação de função de treinador virtual como uma ajuda de tarefa e depois adicioná-la a um curso como parte de uma jornada de aprendizado estruturada
jcr-language: en_us
title: Adicionar uma interpretação de função de treinador virtual a um curso
exl-id: c33ec5e4-0e96-4452-ada7-d48f9c71a123
source-git-commit: 8bde6827835a7f8cd8cc28f3d2c4014527e4a96c
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%
---

# Adicionar uma interpretação de função de treinador virtual a um curso

O Publish é uma encenação de treinador virtual como uma ajuda de tarefa e, em seguida, adiciona-a a um curso para que os alunos possam acessá-la como parte de uma jornada de aprendizado estruturada.

As funções de treinador virtual não são adicionadas aos cursos diretamente. Em vez disso, primeiro publique a representação de função como uma ajuda de tarefa e, em seguida, adicione essa ajuda de tarefa a um curso como um módulo. Esse processo em duas etapas permite reutilizar a mesma interpretação em vários cursos sem duplicá-la. Sob o capô, uma interpretação publicada é adicionada à sua biblioteca de conteúdo como um módulo de LTI, que é como ela pode ser implantada como uma ajuda de tarefa independente ou um módulo de curso. Antes de começar, [crie e publique uma reprodução de função de treinador virtual](/help/migrated/authors/feature-summary/virtual-coach/create-publish-virtual-coach-role-play.md), se ainda não o fez.

## Adicionar a representação como uma ajuda de tarefa

1. No painel de navegação à esquerda da página inicial do Autor, selecione **Ajudas de tarefa**.
2. Selecione **Criar** > **Treinador virtual** no canto superior direito.
3. Insira um nome e uma descrição para a ajuda de tarefa.
4. Selecione a interpretação de função **Treinador Virtual** que deseja usar no campo **Pesquisar e Selecionar Treinador Virtual**.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach8.png)
   *Pesquise e selecione a representação de função publicada que deseja transformar em uma ajuda de trabalho.*

5. Definir visibilidade:
   - Deixe a configuração padrão **Compartilhado** para permitir que outros autores atribuam esta ajuda de tarefa aos seus cursos.
   - Selecione **Particular** para restringir o acesso aos seus próprios cursos.
6. Opcionalmente, insira o tempo de conclusão esperado em minutos no campo **Duração**.
7. No campo **Marcas**, insira palavras-chave para tornar a ajuda de tarefa detectável na pesquisa e no catálogo.
8. Opcionalmente, atribua habilidades e níveis de habilidade. Apenas habilidades que já existem em sua conta da Adobe Learning Manager podem ser usadas. Não é possível criar habilidades nessa tela e atribuí-las não é obrigatório.
9. Selecione **Salvar**. A ajuda de tarefa é publicada e está disponível para adicionar a um curso.

## Adicionar a interpretação de função a um curso

Depois que a ajuda de tarefa for publicada, adicione-a a qualquer curso como um módulo. A interpretação de papéis aparece para os alunos como parte da sequência do curso junto com outros conteúdos, como vídeos, documentos ou questionários.

1. No painel de navegação à esquerda da página inicial do Autor, selecione **Cursos**.
2. Abra o curso ao qual deseja adicionar a representação de função ou selecione **Criar** para iniciar um novo curso. Se você estiver abrindo um curso existente, selecione **Editar** após abri-lo.
3. Adicione o nome e a descrição do curso.
4. Navegue até a seção **Módulos** do editor de cursos.
5. Há três seções onde você pode adicionar módulos. Quando você quiser selecionar um coach virtual, navegue até a primeira seção chamada **Conteúdo**, selecione **Adicionar módulo** e depois selecione **Coach virtual**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach18.png)

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach9.png)
   *Escolha o Treinador Virtual como o tipo de módulo para adicionar sua representação publicada a um curso.*

6. Pesquise a ação de função de treinador virtual que você criou e selecione-a.

   ![](/help/migrated/authors/feature-summary/assets/virtual_coach10.png)
   *Pesquise a ajuda de tarefa por nome ou marca e marque a caixa de seleção correspondente para adicioná-la ao curso.*

7. Selecione **Adicionar**.
8. Configure os critérios de conclusão e sucesso do módulo de acordo com o design do seu curso.
9. Selecione **Republicar** se você atualizou um curso existente. Se você atualizou um curso existente, verá apenas o botão **Republicar**. Selecione **Salvar** se você criou o curso novamente. Você verá apenas o botão **Salvar** se tiver criado o curso novamente. Clicar no botão **Salvar** salvará o curso na guia **Rascunho** da página Catálogo de Cursos. Para publicar o mesmo curso, navegue até o mesmo curso na página **Catálogo do curso**, selecione as reticências e selecione **Curso do Publish**.

   ![](/help/migrated/authors/feature-summary/assets/virtual-coach19.png)

>[!NOTE]
>
>Todas as atualizações feitas na ajuda de tarefa, incluindo alterações no conteúdo de representação, são refletidas automaticamente em todos os cursos aos quais foram adicionadas. Se a interpretação fizer parte de uma avaliação formal, republique a ajuda de tarefa depois de fazer alterações para que os alunos vejam a versão mais recente.

## Empacotar virtual coach como parte de uma jornada de aprendizado

O Virtual Coach foi projetado para funcionar melhor como a “última milha” do treinamento — o ponto em que os alunos demonstram que podem aplicar o que acabaram de aprender, em vez de uma atividade independente. Empacotar a interpretação dentro de um curso ou de uma jornada de aprendizado juntamente com o conteúdo relacionado e distribuir o link do curso por e-mail ou outras comunicações de gerenciamento de alterações para que os alunos saibam exatamente quando e por que concluí-lo.

Essa abordagem de empacotamento se aplica bem a várias implementações comuns:

- **Integração e aumento de novas contratações**, em que a interpretação de funções acompanha o conteúdo de integração e confirma que uma nova contratação está pronta para a primeira conversa ao vivo.
- **Certificação e reforço de vendas**, em que role-play é o ponto de verificação de certificação no final de um curso de habilitação de vendas.
- **Prontidão para lançamento do produto**, em que a função acompanha o treinamento de lançamento e confirma que os representantes podem posicionar o novo produto antes que ele seja lançado no mercado — por exemplo, o cenário de prontidão para lançamento do produto descrito em [o que é o Virtual Coach](/help/migrated/authors/feature-summary/virtual-coach/what-virtual-coach-is.md), em que um representante deve adaptar sua proposta em um comitê de compra multipessoal.
- **Treinamento de liderança e gerente**, em que a representação de funções segue um curso de habilidades de gerenciamento e precede uma conversa sobre desempenho real.
- **Programas de preparação para parceiros**, nos quais a função confirma que um parceiro externo pode representar seu produto corretamente antes que ele seja certificado.
- **Treinamento de gerenciamento e comunicação de alterações**, em que a representação de funções reforça um novo processo ou uma mensagem de reorganização depois que os funcionários concluem o conteúdo relacionado.

Depois que os alunos puderem encontrar e iniciar a interpretação, consulte [praticar uma interpretação com o Virtual Coach](/help/migrated/learners/feature-summary/virtual-coach/practice-role-play-with-virtual-coach.md) para saber o que eles experimentarão.
