---
description: Saiba mais sobre como definir Configurações avançadas no Adobe Learning Manager
jcr-language: en_us
title: Configurações avançadas no Adobe Learning Manager
exl-id: 7047c89f-5f1c-4e0a-a908-20ef0eb9667d
source-git-commit: 0862e0d042fac74377b44c3387a72336ec625161
workflow-type: tm+mt
source-wordcount: '2357'
ht-degree: 1%

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

As pastas de conteúdo no Adobe Learning Manager controlam quais autores podem ver e acessar o conteúdo na Biblioteca de conteúdo. Com pastas hierárquicas de conteúdo, os administradores podem organizar grandes bibliotecas de conteúdo em até três níveis de pastas privadas aninhadas, facilitando a localização, o gerenciamento e a reutilização do conteúdo em toda a organização.

### O que é uma pasta de conteúdo

Uma pasta de conteúdo é um contêiner que agrupa conteúdo relacionado e determina quem pode acessá-lo. Todos os arquivos de conteúdo no Adobe Learning Manager pertencem a pelo menos uma pasta o tempo todo.

Há dois tipos de pastas de conteúdo:

**Pasta pública**- presente em todas as contas por padrão. A pasta pública tem as seguintes propriedades:

* Todos os autores na conta podem acessar o conteúdo na pasta pública.
* O conteúdo da pasta pública não pode estar em nenhuma pasta privada. O inverso também é verdadeiro. O conteúdo de uma pasta particular não pode estar na pasta pública.
* A pasta pública não faz parte da configuração de acesso com base na função. Restringir uma função personalizada a pastas particulares específicas não restringe o acesso à pasta pública.

**Pastas privadas**- criadas por administradores. Pastas privadas oferecem suporte a uma hierarquia de três níveis, e seu acesso é controlado por meio da configuração de funções.

**Compreender os níveis de hierarquia de pastas**

As pastas de conteúdo privado aceitam até três níveis de aninhamento:

* **Pastas de nível 1**- pastas de nível superior na raiz da sua biblioteca de conteúdo

* **Pastas de nível 2**- subpastas aninhadas dentro de uma pasta de nível 1

* **Pastas de nível 3**- subpastas aninhadas dentro de uma pasta de nível 2

Essa estrutura dá às organizações a flexibilidade de espelhar a organização do conteúdo real, por área de tópico, tipo de entrega, público ou equipe, em vez de gerenciar milhares de arquivos em uma lista simples.

Somente os administradores podem criar, editar ou excluir pastas em qualquer nível. Autores e usuários personalizados interagem com a hierarquia, mas não podem modificá-la.

### Regras de nomeação de pasta

Os nomes de pastas devem ser exclusivos dentro do mesmo nível na mesma pasta pai. Especificamente:

| **Cenário** | **Permitido?** |
|----------------------------------------------------------------------------------------------|--------------------------|
| Duas pastas de Nível 1 com o mesmo nome | Não |
| Duas pastas de Nível 2 na mesma pasta de Nível 1 com o mesmo nome | Não |
| Duas pastas de Nível 2 em diferentes pastas de Nível 1 com o mesmo nome | Sim |
| Uma pasta de Nível 2 e uma pasta de Nível 3 com o mesmo nome | Sim Os níveis são distintos |
| Uma pasta de Nível 3 e outra pasta de Nível 3 na mesma pasta de Nível 2 com o mesmo nome | Não |


### Como os caminhos da pasta são exibidos

A Biblioteca de conteúdo exibe cada caminho de pasta completo do arquivo de conteúdo. Por exemplo, **Programas de treinamento** > **Integração** > **Ativos SCORM**. Este caminho mostra o local completo do conteúdo.

Se um arquivo existir em mais de uma pasta, todos os caminhos aparecerão separados por vírgulas. Se um caminho for longo, ele ficará truncado desde o início com reticências (...) e o nome de pasta mais profundo será sempre exibido.

### Acesso baseado em função a pastas

O acesso a pastas particulares é atribuído somente no **Nível 1**. Quando uma função personalizada recebe acesso a uma pasta de Nível 1, esse acesso automaticamente é distribuído em cascata para todas as subpastas de Nível 2 e Nível 3 dentro dela. Não há opção para conceder acesso no nível da subpasta de maneira independente.

A tabela a seguir descreve o que cada função pode fazer com a hierarquia de pastas.

| **Função** | **O que eles podem fazer** |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administrador | Crie, renomeie e exclua pastas particulares de Nível 1, Nível 2 e Nível 3; configure o acesso à pasta de Nível 1 para funções personalizadas |
| Administrador personalizado | Gerenciar pastas dentro de ramificações de Nível 1 acessíveis, sujeito aos privilégios atribuídos |
| Autor | Procure pastas, filtre conteúdo por pasta, adicione conteúdo a pastas, copie e mova conteúdo entre pastas, selecione conteúdo ao adicionar módulos a um curso |
| Autor personalizado | Igual ao autor, mas limitado a pastas acessíveis por meio de seus privilégios de Nível 1 atribuídos |

### Limites da estrutura de pastas

| **Limite** | Valor **1&rbrace;** |
|---------------------------------------|-----------|
| Pastas de nível 1 por conta | Sem limite |
| Subpastas de nível 2 por pasta de nível 1 | 25 |
| Subpastas de nível 3 por pasta de nível 2 | 25 |
| Profundidade máxima da pasta | 3 níveis |


### Comportamento de seleção de pasta

Ao selecionar uma pasta, por exemplo, durante a filtragem ou a exclusão, a seleção segue em cascata pela hierarquia da seguinte maneira:

* Selecionar uma **pasta do Nível 1** seleciona automaticamente todas as pastas de Nível 2 e de Nível 3 abaixo dela.

* Selecionar uma **pasta de Nível 2** seleciona automaticamente todas as pastas de Nível 3 abaixo dela. Outras pastas de Nível 2 na mesma pasta de Nível 1 não são selecionadas.

* Selecionar uma **pasta de Nível 3** seleciona apenas essa pasta. Nenhuma outra pasta foi selecionada.

>[!NOTE]
>
>Quando você seleciona uma subpasta sem selecionar sua pasta pai, a pasta pai não exibe um indicador de seleção parcial ou mista. Isso é intencional. Porque uma pasta pai pode conter conteúdo, não apenas subpastas. Selecionar uma pasta pai significa “incluir todo o conteúdo desta pasta e tudo o que estiver abaixo dela”. Um indicador parcial sugere que o conteúdo da própria pasta pai está parcialmente incluído, o que seria enganoso. Se você desejar filtrar por apenas uma subpasta específica, selecione essa subpasta diretamente. Se quiser todo o conteúdo de uma pasta pai e suas subpastas, selecione a pasta pai.

### Quando usar uma estrutura de pastas hierárquica

As pastas hierárquicas de conteúdo são especialmente valiosas quando sua empresa gerencia muitos arquivos de conteúdo e precisa de uma maneira estruturada de navegar, reutilizar e controlar o acesso a eles.

Os cenários comuns incluem:

* **Bibliotecas de conteúdo grandes**: quando você tem milhares de arquivos de conteúdo, uma hierarquia de três níveis permite que os autores naveguem diretamente para o que precisam, em vez de percorrerem uma lista simples.

* **Várias equipes ou projetos**: as pastas de nível 1 podem separar áreas de equipe ou de projeto; as pastas de nível 2 podem ser organizadas por tipo de entrega; as pastas de nível 3 podem conter ativos individuais.

* **Separação de conteúdo baseada em função**: quando diferentes equipes de autor devem acessar apenas o conteúdo relevante para o trabalho, a atribuição de acesso a pastas de Nível 1 mantém o conteúdo privado de cada equipe.

### Casos de uso reais de pastas de conteúdo hierárquico

**Caso de uso 1- Treinamento de conformidade com conteúdo específico da jurisdição**

Uma organização global executa treinamento obrigatório de conformidade em várias regiões. Cada região tem módulos principais que se aplicam a todos, além de adendos legais específicos da jurisdição, como regulamentos de privacidade de dados, lei trabalhista local, requisitos de divulgação financeira, que variam de acordo com o país ou a região.

Sem pastas hierárquicas, todos os ativos de conformidade ficam em uma lista simples, dificultando para as equipes de conteúdo regionais saber quais arquivos pertencem a qual programa ou jurisdição.

Com uma estrutura de três níveis:

* Nível 1: treinamento de conformidade

* Nível 2: EMEA / APAC / Américas (uma subpasta por região)

* Nível 3: módulos ou ativos específicos por região (PDF de regulamentação de privacidade, planos de políticas locais, arquivos de avaliação)

As equipes de autores regionais recebem acesso apenas às respectivas filiais de Nível 1 ou Nível 2. Eles podem localizar, atualizar e reutilizar apenas os ativos relevantes para sua jurisdição sem ver ou modificar acidentalmente o conteúdo de outra região.

**Caso de uso 2- Programa de integração em grande escala com muitas funções**

Uma organização integra milhares de funcionários por ano em várias funções distintas: colaboradores individuais, gerentes, prestadores de serviço e especialistas técnicos. Cada função tem seu próprio rastreamento de integração com conteúdo básico compartilhado e módulos específicos à função.

Com uma estrutura de três níveis:

* Nível 1: integração

* Nível 2: Função (Colaborador individual/Gerente/Contratado/Especialista técnico)

* Nível 3: tipo de módulo (pacotes SCORM / plataformas ILT / guias de atividade / avaliações)

Os autores que criam cursos para cada função navegam diretamente para o Nível 2 e encontram os arquivos exatos dessa faixa. Quando um módulo é reutilizado entre funções, como um vídeo de valores de empresa, ele pode ser copiado ou vinculado a várias pastas sem criar duplicatas. O conteúdo permanece como uma única fonte, mas aparece em todas as ramificações relevantes.

**Caso de uso 3- Biblioteca de habilidades técnicas de alto volume com várias equipes de conteúdo**

Uma empresa de tecnologia mantém uma biblioteca interna de treinamento de habilidades com milhares de arquivos de conteúdo em linhas de produtos, infraestrutura em nuvem, ferramentas de desenvolvedor, segurança e engenharia de dados. Várias equipes de autores contribuem, cada uma responsável por uma área de produto. Os módulos do curso podem executar de 40 a 60 arquivos por curso.

Sem hierarquia, todos os milhares de arquivos ficam em algumas pastas de nível superior, e autores de diferentes equipes frequentemente escolhem a versão incorreta do arquivo ou substituem acidentalmente os ativos compartilhados.

Com uma estrutura de três níveis:

* Nível 1: Área de produto (Cloud / Ferramentas de desenvolvimento / Segurança / Engenharia de dados)

* Nível 2: nome do curso

* Nível 3: tipo de ativo (vídeos/PDF/SCORM/questionários)

Cada equipe de produto recebe acesso apenas à sua pasta de Nível 1. Localizar um quiz específico para um curso específico significa navegar exatamente até a pasta de Nível 3 correta, em vez de pesquisar em milhares de arquivos. Quando a equipe de segurança atualiza um pacote SCORM, ela sabe que ele está em Segurança > [Nome do curso] > SCORM e não pode aterrissar acidentalmente em outra filial da equipe.

### Gerenciar pastas de conteúdo como administrador

Como administrador no Adobe Learning Manager, você cria e mantém a hierarquia de pastas de conteúdo, controla quais funções personalizadas têm acesso a pastas específicas e gerencia nomes e exclusões de pastas. Os autores podem adicionar conteúdo às pastas e organizar conteúdo dentro da hierarquia, mas somente os administradores podem criar, renomear ou excluir pastas.

#### Criar uma pasta de conteúdo

>[!NOTE]
>
>Duas pastas no mesmo nível sob o mesmo pai não podem compartilhar um nome. O mesmo nome é permitido em ramificações diferentes ou em níveis diferentes.

1. Faça logon no Adobe Learning Manager como administrador.
2. Na navegação à esquerda, selecione **Configurar** > **Configurações**.
3. Na seção **Avançado**, selecione **Pasta de Conteúdo**.
4. Selecione **Adicionar** no canto superior direito da página. A caixa de diálogo **Adicionar Nova Pasta** é aberta.
5. Insira um nome e uma descrição opcional para a pasta.
6. Selecione **Salvar**. A pasta é criada e exibida na lista de pastas.


#### Criar uma subpasta

1. Na página **Pasta de Conteúdo**, localize a pasta pai.
2. Selecione a opção **Criar subpasta** ao lado do nome da pasta.
3. Insira um nome e uma descrição opcional para a subpasta.
4. Selecione **Salvar**. A subpasta aparece recuada abaixo de seu pai na lista de pastas.

>[!NOTE]
>
>Cada pasta pode conter até 25 subpastas diretas. O Nível 3 é a profundidade máxima. Não é possível criar uma subpasta dentro de uma pasta de Nível 3.

#### Renomear uma pasta

1. Na página **Pasta de Conteúdo**, selecione a pasta que você deseja renomear. A pasta é aberta no modo de edição.
2. Atualize o nome da pasta e, se necessário, a descrição.
3. Selecione **Salvar**. A pasta é salva com o novo nome.

#### Excluir uma pasta

Antes de excluir, esteja ciente das seguintes regras:

* Você pode excluir uma pasta vazia em qualquer nível.
* Não é possível excluir uma pasta se ela contiver conteúdo que não está vinculado a nenhuma outra pasta. Mova esse conteúdo para outra pasta primeiro.
* A exclusão de uma pasta pai exclui todas as suas subpastas. Selecionar uma pasta pai seleciona automaticamente todos os seus filhos.

#### Excluir a pasta pai

1. Na página **Pasta de Conteúdo**, marque a caixa de seleção ao lado de cada pasta que deseja excluir.
2. Selecione **Ações** > **Excluir pasta** no canto superior direito da página.
3. Confirme a exclusão quando solicitado. Todas as subpastas dentro das pastas pai também são excluídas.

#### Excluir uma subpasta

1. Na página **Pasta de Conteúdo**, marque a caixa de seleção ao lado da subpasta que deseja excluir.
2. Selecione **Ações** > **Excluir pasta** no canto superior direito da página.
3. Confirme a exclusão quando solicitado. A subpasta é excluída.

>[!CAUTION]
>
>A exclusão de uma pasta é permanente. Verifique se todo o conteúdo dentro da pasta foi movido para outro local antes de confirmar.


#### Configurar acesso à pasta para funções personalizadas

Você pode restringir funções personalizadas a pastas específicas de Nível 1 para que os administradores personalizados e autores com essas funções vejam apenas o conteúdo relevante para eles.

O acesso é definido somente no **nível 1 da pasta**. Quando você concede acesso a uma função personalizada para uma pasta de Nível 1, essa função automaticamente obtém acesso a todas as subpastas de Nível 2 e de Nível 3 dentro dela. Não é possível atribuir acesso no nível de subpasta de maneira independente.

1. Na navegação à esquerda, selecione **Usuários** > **Funções personalizadas**.
2. Abra a função personalizada que deseja configurar ou crie uma nova.
3. Em **Privilégios de Conta**, localize a seção **Pastas de Conteúdo**.
4. Selecione **Pastas Selecionadas**.
5. Selecione as pastas de Nível 1 às quais esta função deve ter acesso.
6. Selecione **OK**.

Os usuários com essa função veem apenas o conteúdo nas pastas de Nível 1 selecionadas e em suas subpastas. O conteúdo em outras pastas privadas e na pasta pública permanece inacessível para elas.

#### Práticas recomendadas

As práticas a seguir ajudam a criar uma estrutura de pastas que é bem dimensionada e permanece fácil de navegar.

1. **Planeje sua estrutura antes de criar pastas.** Uma vez que o conteúdo é organizado em uma hierarquia, a reestruturação requer a movimentação de grandes volumes de conteúdo. Decida as categorias de Nível 1, como linhas de produtos, departamentos ou programas de treinamento, antes de começar.

2. **Use três níveis para agrupamentos significativos.** Um padrão comum é: Nível 1 para um domínio ou programa amplo, Nível 2 para tipo de entrega ou equipe, Nível 3 para ativos individuais. Por exemplo:

   * Nível 1: Treinamento de vendas

   * Nível 2: módulos em ritmo individualizado

   * Nível 3: Ativos do PDF

3. **Mantenha nomes curtos, descritivos e exclusivos dentro de seu pai.** Evite nomes genéricos como “Módulo 1” ou “Conteúdo”. Use identificadores que façam sentido para os autores que navegam na biblioteca.

4. **Atribua acesso à função personalizada somente no Nível 1.** Como o acesso é realizado em cascata automaticamente, atribuir no Nível 1 é suficiente e mantém o gerenciamento de acesso simples. Não é necessário atualizar o acesso ao adicionar subpastas de Nível 2 ou de Nível 3.

5. **Mover conteúdo antes de excluir pastas.** Se uma pasta contiver conteúdo que não está vinculado a nenhum outro lugar, a exclusão será bloqueada. Crie um hábito de revisar o conteúdo da pasta antes de excluí-la.


<!--

**Key points:**

A folder is a repository of content, which is a subset of the entire content library available in an account with the following properties:

* Only you (administrator) can create, edit, or delete a folder.
* You can control access to folders as part of defining roles only for custom administrators.
* Content must at all times be associated with at least one folder. To start with, all content will be associated with the public folder, which can later be changed.
* Content can be associated with multiple folders at the time of creation, which will also be possible by a copy operation
* All folder names must be unique within the account, otherwise there will be an error in naming a folder.

Folders only control visibility of content and don't create copies of content. Therefore, editing content will reflect in all the associated folders.

**Public folder**

A public folder is always present in an account and initially, all content will be part of this folder. Later, authors can move content out of this folder into other folders. A public folder has the following properties:

* All content associated with this folder will be accessible to all types of authors, by default.
* Any content that is a part of a public folder, cannot be part of any other folder. The converse also holds true.

This folder cannot be part of configurable role definition. Consequently, not having a public folder in configurable role definition doesn't restrict access to a public folder.

**Private folder**

Any folder created by you is a private folder.

**Add a content folder**

To add a content folder, follow the steps:

1. Select **[!UICONTROL Settings]** > **[!UICONTROL Content Folder]**.
2. Select **[!UICONTROL Add]** to create a new folder.
3. Type the name and description of the folder to be created.
 
    ![alt text](assets/advanced-settings-picture1.png)

4. Select **[!UICONTROL Save]** to create the folder.

**Folder operations**

* **[!UICONTROL Add a folder]**: To add a folder, select the folder, and then select **[!UICONTROL Add]** on the upper-right corner of the screen.
* **[!UICONTROL Delete a folder]**: To delete a folder, select the folder to delete, select the **[!UICONTROL Actions]** menu, and then select **[!UICONTROL Delete Folder]**.
-->

## Locais de sala de aula

Criar e gerenciar uma biblioteca de locais de sala de aula física ou virtual. Esses locais podem ser usados por autores e administradores para configurar eventos de ILT (Instructor-Led Training, treinamento ministrado por instrutor). O recurso garante que os detalhes da sala de aula, como limites de vagas e informações de local, sejam pré-configurados e facilmente acessíveis.

Consulte [Adicionar locais de sala de aula no Adobe Learning Manager](/help/migrated/administrators/feature-summary/classroom.md) para obter mais informações.

## Relatórios

Esta seção permite configurar os painéis de controle de Conformidade e Sucesso do Grupo.

![texto alternativo](assets/advanced-settings-picture2.png)

Consulte o seguinte para obter mais informações:

* [Painel de conformidade](/help/migrated/administrators/feature-summary/reports.md#compliance-dashboard)
* [Painel de Sucesso do Grupo](/help/migrated/administrators/feature-summary/group-success-dashboard.md)
