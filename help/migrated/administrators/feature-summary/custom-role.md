---
jcr-language: en_us
title: Funções personalizadas
description: O recurso Caminhos de aprendizado ajuda a definir funções personalizadas e atribuir responsabilidades específicas ao conjunto de usuários. Esse recurso permite atribuir responsabilidades fora do alcance da função existente do indivíduo.
contentowner: dvenkate
exl-id: dcc84f91-4e51-4ae2-b7cb-9eb29b398bc1
source-git-commit: f8473c0bfd1de5591d858e657dcc67c71c50ecd5
workflow-type: tm+mt
source-wordcount: '5467'
ht-degree: 24%

---

# Funções personalizadas

Esse recurso ajuda a definir funções personalizadas e atribuir responsabilidades específicas a um conjunto de usuários. Esse recurso permite atribuir responsabilidades fora do alcance da função existente do indivíduo.

O Adobe Learning Manager permite que os administradores completos deleguem responsabilidades de gerenciamento de função personalizada a administradores personalizados confiáveis, incluindo a criação, edição e atribuição de funções personalizadas, sem fornecer a eles credenciais de administrador completas. Esse recurso permite que administradores personalizados gerenciem outras funções sem sobrecarregar administradores com obrigações. Isso é controlado por meio do nível de permissão **Avançado** na seção **Usuários** de uma definição de função personalizada. Consulte [O que a permissão avançada de usuário desbloqueia](#advanced-user) para obter mais informações.

As organizações usam esse recurso para delegar o gerenciamento de funções de rotina a administradores personalizados designados. Por exemplo, para permitir que uma equipe dedicada crie e atribua funções de editor ou autor de forma contínua ou para permitir que uma equipe de operações limpe contas de usuários que deixaram a organização. Isso evita a necessidade de dar a essas equipes acesso total de administrador, que carrega privilégios mais amplos do que suas responsabilidades exigem.

Você pode criar uma função personalizada para fornecer habilidades limitadas de criação de um catálogo específico. Também pode criar uma função dedicada ao gerenciamento de relatórios. Tais funções podem, então, ser atribuídas a indivíduos que deveriam assumir essas responsabilidades específicas.

>[!NOTE]
>
>Adicionar uma nova função personalizada não afetará grupos de usuários personalizados existentes ou quaisquer grupos baseados em funções, como Todos os administradores, Todos os autores etc.

O administrador tem a capacidade de criar funções personalizadas de administrador e autor com permissões personalizadas para cada função. Veja abaixo uma visão geral das permissões associadas a cada função:

**Permissões de Função de Autor Personalizadas**

Autores personalizados podem realizar as seguintes tarefas:

* Acesse a biblioteca de conteúdo para adicionar, editar ou excluir conteúdo principal.
* Criar, editar e excluir:
  * Cursos
  * Ajudas de tarefa
  * Certificações
  * Caminhos de aprendizado
  * Planos de aprendizado

Os administradores e autores, incluindo administradores personalizados e autores personalizados, terão a capacidade de compartilhar objetos de aprendizado (LOs) em catálogos compartilhados externamente. Os administradores e autores devem poder pesquisar catálogos compartilhados externamente ao criar objetos de aprendizado (LOs).

**Permissões de função de administrador personalizada**

A função de administrador personalizada replica um conjunto de responsabilidades de administrador, incluindo o acesso a privilégios em nível de conta. Os administradores personalizados recebem permissões para gerenciar os principais recursos relacionados às atividades de aprendizado, como:

* Planos de aprendizado
* Catálogos
* Relatórios
* Etiquetas

Além disso, os administradores personalizados podem:

* Gerenciar cursos e ajudas de tarefa, incluindo a inscrição e a exclusão de usuários.
* Criar, editar e excluir certificações, programações de aprendizado e planos de aprendizado.
* Acessar os recursos de relatório e inscrição para todos os objetos de aprendizado (LOs).

Os administradores agora podem exibir as permissões criadas por CSV no Adobe Learning Manager. A opção Filtrar por filtra as funções personalizadas pelo administrador criadas e importadas por meio de um CSV. Depois de selecionar uma função personalizada, você pode ver suas permissões.

![](assets/filter.png)
_Filtrar funções personalizadas_

## Criar uma função personalizada {#create-role}

1. Faça logon como administrador. Abra **[!UICONTROL Usuários]** > **[!UICONTROL Função Personalizada]**.
2. Selecione **[!UICONTROL Criar Função]**. A guia **[!UICONTROL Criar Nova Função]** é aberta.

   ![](assets/create-new-role.png)

   *Criar uma função personalizada*

3. Insira o nome no campo **[!UICONTROL Nome da Função]**.
4. **[!UICONTROL Privilégios de conta]**: esses privilégios concedem aos proprietários da função acesso a aspectos específicos de configuração do sistema e que atuam na conta inteira. Escolha as permissões de acesso. O usuário recebe controle total sobre as permissões atribuídas.

   Os administradores podem conceder permissões detalhadas para a seção Usuário, que tem Usuários internos/externos, Grupos de usuários e Usuários avançados.

   >[!NOTE]
   >
   >   O escopo não é aplicável a esses privilégios.


   ![](assets/account-privileges.png)

   *Definir o escopo*

5. **Privilégios do recurso - recursos principais**: usado para conceder acesso a recursos específicos para gerenciar atividades de aprendizado. Através dessa opção é possível conceder permissões aos recursos a seguir.

   Os administradores podem fornecer permissões detalhadas, como somente leitura, criar, editar e excluir permissões para os catálogos.

   * Catálogos
   * Relatórios
   * Etiquetas

   ![](assets/core-features.png)

   *Definir escopo para catálogos, relatórios e marcas*

6. **Privilégios do recurso- Objetos de Aprendizado:** use esta opção para fornecer acesso aos recursos relacionados aos OAs. Os administradores podem fornecer permissões detalhadas para todos os objetos de aprendizado, incluindo cursos, programações de aprendizado, certificações e ajudas de tarefa. Eles podem atribuir permissões aos usuários, como criar, editar, excluir ou acesso somente leitura.

   * Certificações
   * Cursos
   * Ajudas de tarefa
   * Programas de aprendizado

   Você também pode conceder um controle de operação específico para os objetos de aprendizado. A permissão pode ser uma das seguintes opções:

   * Somente leitura
   * Criar
   * Editar
   * Excluir
   * Inscrição
   * Relatório

   Você também pode conceder controle total para os OAs.

   ![](assets/learningobjects.png)

   *Conceder permissões específicas*

7. **Escopo dos privilégios de recurso:** o escopo dos privilégios de Recurso alocados para esta função pode ser restrito a um Grupo de Usuários específico ou a um ou mais Catálogos.

   Catálogos: use o botão de opção para fornecer controle sobre **[!UICONTROL Todos os catálogos]** ou use a opção **[!UICONTROL Definir acesso por catálogo]** para fornecer acesso a catálogos específicos. Também é possível selecionar vários catálogos.

   Grupos de usuários: forneça acesso a **[!UICONTROL Todos os grupos de usuários]** ou use a opção **[!UICONTROL Definir acesso por grupo de usuários]** para fornecer acesso a grupos de usuários específicos. É possível especificar apenas um grupo de usuários.

   >[!NOTE]
   >
   >Se você selecionou Anúncio, Gamificação, Modelos de email, Habilidades e usuários em Privilégios da conta, o acesso ao grupo de usuários é fornecido a todos os grupos de usuários por padrão e essa opção é desativada.

   Se tiver selecionado Planos de aprendizado em Privilégios da conta, o acesso a todos os Catálogos e Grupos de usuários é fornecido por padrão e estas opções estão desativas em Escopo.

   ![](assets/define-scope-of-privileges.png)

   *Definir escopo de privilégios*

>[!NOTE]
>
>   No Learning Manager 27.6, é possível criar uma função personalizada que estará no escopo de vários catálogos e a cada catálogo será concedido um conjunto diferente de permissões.


Para obter mais permissões para os catálogos, siga as etapas abaixo:

1. Clique na opção **[!UICONTROL Definir acesso por catálogo]**.
1. Escolha os catálogos para você poder ver o nível de permissão de cada catálogo. As permissões são as seguintes:

   <table>
        <tbody>
        <tr>
          <td>
          <p><b>Permissão</b></p></td>
          <td>
          <p><b>Descrição</b></p></td>
        </tr>
        <tr>
          <td>
          <p>Controle total</p></td>
          <td>
          <p>Concede o controle total em todos os objetos de aprendizado. As permissões incluem adicionar, editar, excluir, ler, inscrever e relatar.<br></p></td>
        </tr>
        <tr>
          <td>
          <p>Relatório</p></td>
          <td>
          <p>Concede acesso somente à guia Relatórios do objeto de aprendizado.</p></td>
        </tr>
        <tr>
          <td>
          <p>Inscrever</p></td>
          <td>
          <p>Concede permissão para inscrições somente no objeto de aprendizado.</p></td>
        </tr>
        <tr>
          <td>
          <p>Somente leitura</p></td>
          <td>
          <p>Concede permissão somente para ver os objetos de aprendizado no catálogo.</p></td>
        </tr>
        </tbody>
      </table>

1. Ative ou desative as permissões de acordo com suas necessidades.
1. Para salvar as alterações, clique em **[!UICONTROL OK]**. Em seguida, para salvar as alterações na Função personalizada, clique em **[!UICONTROL Salvar]**.

Considere, por exemplo, o seguinte cenário.

A permissão resultante, que um usuário personalizado teria em um objeto de aprendizado, é uma interseção da permissão do objeto de aprendizado e da permissão do catálogo.

Um usuário personalizado tem permissão completa nos cursos e acesso de somente leitura no catálogo A, mas tem permissão completa no catálogo B. Os resultados são acesso de somente leitura nos cursos do catálogo A e controle total nos cursos do catálogo B.

Os usuários com função personalizada podem:

* Ver somente o conteúdo dos catálogos aos quais eles têm acesso.
* Acessar qualquer objeto de aprendizado com base nas permissões do catálogo do qual o objeto de aprendizado faz parte.

  Como administrador, você pode:

* Escolher mais de um catálogo para uma função personalizada.
* Modificar as permissões de um catálogo a qualquer momento.
* Remover os catálogos de um escopo para o qual você não deseja mais conceder permissões.
* Conceder implicitamente a permissão Somente leitura para um catálogo, ao conceder permissões para o catálogo.

  A tabela abaixo ilustra como as permissões são concedidas.

  <table>
    <tbody>
     <tr>
      <td>
       <p><strong> </strong></p></td>
      <td>
       <p><strong>Permissão no nível do catálogo</strong></p></td>
     </tr>
     <tr>
      <td>
       <p><strong>Objeto de aprendizado - Permissão de nível</strong></p>
       <p><strong>(Por exemplo: Cursos)</strong></p></td>
      <td>
       <p>Controle total</p></td>
      <td>
       <p>Inscrever</p></td>
      <td>
       <p>Relatório</p></td>
      <td>
       <p>Somente leitura</p></td>
     </tr>
     <tr>
      <td>
       <p>Controle total</p></td>
      <td>
       <p>Controle total</p></td>
      <td>
       <p>Inscrever</p></td>
      <td>
       <p>Relatório</p></td>
      <td>
       <p>Somente leitura</p></td>
     </tr>
     <tr>
      <td>
       <p>Inscrever</p></td>
      <td>
       <p>Inscrever</p></td>
      <td>
       <p>Inscrever</p></td>
      <td>
       <p>Somente leitura</p></td>
      <td>
       <p>Somente leitura</p></td>
     </tr>
     <tr>
      <td>
       <p>Editar e excluir</p></td>
      <td>
       <p>Editar e excluir</p></td>
      <td>
       <p>Somente leitura</p></td>
      <td>
       <p>Somente leitura</p></td>
      <td>
       <p>Somente leitura</p></td>
     </tr>
     <tr>
      <td>
       <p>Relatório</p></td>
      <td>
       <p>Relatório</p></td>
      <td>
       <p>Somente leitura</p></td>
      <td>
       <p>Relatório</p></td>
      <td>
       <p>Somente leitura</p></td>
     </tr>
    </tbody>
   </table>

1. **Usuários:** use esta opção para determinar quais usuários receberam esta função. É possível escolher um ou mais usuários usando a caixa de pesquisa.

   **Adicionar usuários ao carregamento de CSV de função personalizada:** para adicionar usuários por meio do carregamento de CSV, adicione uma coluna CustomRole ao arquivo .csv que o administrador usou para importar usuários. Insira a função do usuário na coluna CustomRole para os usuários aos quais você deseja atribuir uma função personalizada. Para carregar o arquivo CSV, clique em **[!UICONTROL Adicionar > Carregar um CSV]**.

   * Não é possível pesquisar Grupos de usuários.
   * Não é possível pesquisar usuários que já tenham uma função de administrador atribuída a eles.
   * A atribuição de uma nova função personalizada a um usuário substitui a função personalizada anterior do usuário.

   <!--![](assets/users.png)-->

   * Um administrador personalizado com permissão para Configurações poderá configurar o agendamento para sincronizar ou sincronizar usuários da Fonte de dados, mesmo se não tiver permissão para a entidade Usuários.
   * Se um administrador personalizado tiver permissão na entidade Usuários, ele poderá atribuir a si mesmo a função de administrador e se tornar um administrador padrão.

## <a id="advanced-user"></a>O que a permissão avançada de usuário desbloqueia {#whatadvanceduserpermissionunlocks}

Quando um administrador completo habilita o acesso **Avançado** sob **Usuários** em uma função personalizada, o administrador personalizado obtém acesso a quatro seções adicionais: **Funções personalizadas**, **Logs de importação**, **Campos ativos** e **Limpeza de usuário**.

Dois níveis de acesso estão disponíveis:

* **Somente Leitura**: o administrador personalizado pode exibir informações e baixar relatórios, mas não pode fazer alterações.
* **Controle Total**: o administrador personalizado pode criar, editar e excluir funções personalizadas, importar usuários e limpar usuários excluídos.

### Herança de permissão e escopo

Quando um administrador personalizado cria uma nova função personalizada ou modifica uma existente, as permissões e o escopo que podem atribuir são limitados ao que eles próprios mantêm. Um administrador personalizado não pode conceder permissões de função que excedam a própria e não pode estender o escopo de uma função para além do escopo atribuído por ele.

Isso significa que um administrador personalizado com acesso a um catálogo específico só pode criar funções com escopo para esse catálogo ou um subconjunto dele. Da mesma forma, eles só podem atribuir permissões que eles próprios detêm às funções que criam.

Ao atribuir usuários a uma função que você criou, é possível pesquisar e adicionar qualquer usuário na conta. Permissões relacionadas ao usuário em funções personalizadas sempre se aplicam ao escopo completo do grupo de usuários e ao escopo completo do catálogo. O escopo do grupo de usuários ou do catálogo não se aplica quando uma função personalizada inclui permissões de gerenciamento de usuários.

Se um administrador completo reduzir seu escopo ou remover uma permissão de sua função, quaisquer funções criadas anteriormente não serão afetadas imediatamente. Essas funções continuam a operar com suas permissões existentes até que um administrador completo abra e salve cada uma individualmente.

>[!IMPORTANT]
>
>**Somente funções criadas manualmente**: os recursos de administração de função personalizada expandida se aplicam apenas às funções criadas por meio da interface do administrador do Adobe Learning Manager. Não há suporte para funções importadas por meio de upload de CSV.


## Conceder permissões de usuário avançadas a uma função personalizada

Os administradores completos concluem esse procedimento para ativar o gerenciamento de usuários expandido para uma função personalizada.

1. Faça logon no Adobe Learning Manager como administrador.
2. Selecione **Usuários** na navegação à esquerda e selecione **Funções Personalizadas**.
3. Selecione **Criar Função Personalizada** para criar uma nova função ou selecione uma função existente para editá-la.
4. Em **Privilégios de Conta**, localize a seção **Usuários**.
5. Na seção **Usuários Avançados**, selecione **Somente Leitura** ou **Controle Total** com base no nível de acesso necessário.
6. Adicionar usuários à função na seção **Usuários**.
7. Selecione **Salvar**.

Os usuários atribuídos agora podem acessar as seções **Funções personalizadas**, **Campos ativos**, **Logs de importação** e **Limpeza de usuário** após o logon.

## O que os administradores personalizados podem fazer com o acesso somente leitura

### Importar registros

Administradores personalizados com acesso somente leitura podem exibir todos os logs de importação na conta. O botão **Adicionar** não está disponível. Não podem ser iniciadas novas importações.

### Limpeza de usuários

A seção **Limpeza do Usuário** está disponível no modo somente exibição. Os administradores personalizados podem:

* Exibir a lista de usuários excluídos
* Pesquisar usuários específicos
* Filtrar usuários excluídos por mês de exclusão
* Exibir outros usuários na conta

Nenhuma ação, como limpar, está disponível no acesso **Somente Leitura**.

### Funções personalizadas

Os administradores personalizados podem exibir todas as definições de função personalizadas na conta, incluindo as permissões atribuídas e as listas de usuários. Eles podem baixar o relatório de funções personalizadas. Eles não podem editar, criar ou excluir qualquer função.

## O que os administradores personalizados podem fazer com o acesso de Controle total

**Importar Logs**

Administradores personalizados com controle total podem exibir todos os registros e adicionar ou importar novos usuários por meio de CSV.

**Limpeza do Usuário**

O Controle Total dá acesso a todas as ações de limpeza do usuário:

* Exibir, pesquisar e filtrar usuários excluídos por mês de exclusão
* Selecionar usuários individuais ou selecionar tudo
* Remover usuários excluídos do sistema
* Procurar e remover outros usuários

**Funções personalizadas**

Administradores personalizados com controle total podem:

* Criar novas funções personalizadas, com permissões iguais ou menores que suas próprias
* Editar funções personalizadas existentes
* Excluir funções personalizadas
* Atribuir usuários a funções personalizadas
* Remover usuários de funções personalizadas
* Baixar o relatório de funções personalizadas
* Filtrar a lista de funções por **Todas**, **Criadas na interface do usuário** ou **Criadas no CSV**

>[!NOTE]
>
>Os administradores personalizados não podem se adicionar a outra função e também não podem editar sua própria função com permissões mais altas.

>[!IMPORTANT]
>
>As funções criadas por um administrador personalizado podem incluir acesso às Funções personalizadas, incluindo a permissão de usuário Avançada que permite o gerenciamento de Funções personalizadas. Isso significa que um administrador personalizado com Controle Total pode criar funções que concedem a outros usuários os mesmos recursos de Funções Personalizadas que eles possuem. As permissões disponíveis durante a criação da função ainda estão sujeitas ao modelo de delegação padrão. O administrador personalizado só pode atribuir permissões que ele detém pessoalmente, a menos que a conta tenha expandido a administração de funções habilitada.

### Exemplo - Criar funções com escopo como um administrador personalizado

Um administrador completo concede a um administrador personalizado Controle total com acesso a dois catálogos de produtos. O administrador personalizado então:

1. Cria uma função de editor com escopo para o primeiro catálogo e atribui autores a ele
1. Cria uma segunda função de editor com escopo para o segundo catálogo e atribui um conjunto diferente de autores
1. Atribui novos autores, que fazem parte da equipe, à função apropriada, sem envolver o administrador total

Cada função que o administrador personalizado cria herda um subconjunto das permissões do administrador personalizado. Os autores atribuídos a essas funções podem acessar e publicar conteúdo em seus respectivos catálogos. Eles não podem gerenciar funções personalizadas por conta própria, porque a seção Funções personalizadas não está disponível em funções criadas por administradores personalizados.

## Comparação de recursos

| Seção | Somente leitura | Controle total |
|---|---|---|
| Importar Logs: exibir logs | ✓ | ✓ |
| Importar Logs: adicionar ou importar usuários via CSV | — | ✓ |
| Limpeza do Usuário: exibir usuários excluídos, pesquisar, filtrar | ✓ | ✓ |
| Limpeza do Usuário: limpar usuários excluídos | — | ✓ |
| Funções Personalizadas: exiba todas as funções e definições | ✓ | ✓ |
| Funções Personalizadas: baixar relatório de funções personalizadas | ✓ | ✓ |
| Funções personalizadas: criar, editar e excluir funções | — | ✓ |
| Funções personalizadas: atribuir e remover usuários | — | ✓ |

## Compatibilidade com versões anteriores

Se uma conta tiver funções personalizadas existentes com acesso **Avançado** habilitado, essas funções incluirão automaticamente acesso a Logs de Importação quando sua conta for atualizada. Se o Acesso avançado estiver desativado no momento em uma função, não haverá alterações. A função continua a se comportar como antes.

>[!NOTE]
>
>Se as Opções avançadas de acesso estiverem ativadas para usuários, verifique quais funções têm esse privilégio e confirme se essas funções têm a intenção de mantê-lo.

## Trilha de auditoria para alterações de função personalizada

Todas as alterações em funções personalizadas, incluindo criação, edição, exclusão e atribuição de usuário, são registradas no relatório de auditoria de funções personalizadas. O relatório de auditoria agora mostra o nome da função personalizada responsável por cada alteração, em vez de um rótulo de administrador genérico. Nenhuma configuração é necessária para habilitar esse comportamento.

Administradores completos podem acessar o relatório de auditoria da seção **Relatórios**.

## Casos de uso reais

### Equipe de gerenciamento de funções

Uma grande organização tem uma equipe dedicada responsável por criar e atribuir funções de autor de conteúdo em dezenas de catálogos de produtos. Anteriormente, cada nova função exigia um administrador completo para criá-la. Com acesso de Controle Total, a equipe de gerenciamento de funções pode criar funções de editor e autor com escopo para catálogos específicos, atribuir novos autores e gerenciar essas funções de forma independente, sem qualquer envolvimento total do administrador para operações de rotina.

### Gerenciamento das operações de RH e do ciclo de vida do usuário

Uma equipe de operações de RH é responsável pela limpeza de contas quando os funcionários deixam a organização. Eles precisam remover os usuários excluídos regularmente, mas não devem ter acesso ao conteúdo do curso, aos dados do aluno ou às configurações do sistema. Conceder acesso de Controle Total Avançado, com escopo apenas para gerenciamento de usuários, dá à equipe de RH o acesso específico de que ela precisa para a limpeza do usuário e a importação sem expor outras funções administrativas.

### Equipe de conformidade e auditoria

Uma equipe de auditoria interna precisa revisar periodicamente quais funções personalizadas existem, quais permissões elas incluem e quem detém cada função. Com o acesso Somente Leitura, a equipe de auditoria pode exibir todas as definições de função e baixar o relatório de funções personalizadas para revisão, mas não pode modificar nada.

## O que os administradores personalizados podem fazer

Os procedimentos a seguir aplicam-se a administradores personalizados com acesso de **Controle Total**. Entre como administrador personalizado e navegue até **Usuários** > **Funções personalizadas** para começar.

### Revisar funções personalizadas existentes

1. Selecione **Usuários** > **Funções Personalizadas**.
1. Use o menu suspenso de filtro para restringir a lista:

   * **Todos**: cada função na conta
   * **Criado da interface do usuário**: funções criadas manualmente
   * **Criado a partir do CSV**: funções importadas via CSV

1. Selecione um nome de função para abrir sua definição completa, incluindo permissões, escopo e usuários atribuídos.

### Criar uma nova função personalizada

1. Selecione **Usuários** > **Funções personalizadas** e selecione **Criar Função**.
1. Insira um nome para a função.
1. Em **Privilégios de Conta**, configure as permissões. Somente as permissões no seu próprio escopo estão disponíveis para seleção. As permissões fora do escopo aparecem desativadas.
1. Defina o catálogo e o escopo do grupo de usuários para a função.
1. Na seção **Usuários**, pesquise e adicione os usuários que terão essa função.
1. Selecione **Salvar**.

>[!NOTE]
>
>Você não pode se adicionar a uma função criada e não pode criar uma função com permissões que excedam as suas. Se uma permissão for desabilitada durante a criação da função, ela estará fora do escopo atual.

### Editar uma função personalizada

1. Selecione **Usuários** > **Funções personalizadas** e abra a função que deseja atualizar.
1. Selecione **Editar**.
1. Atualize o nome, as permissões, o escopo ou as atribuições do usuário conforme necessário.
1. Selecione **Salvar**.

>[!NOTE]
>
>Você não pode editar as permissões de sua própria função personalizada. Entre em contato com um administrador completo se for necessário fazer alterações em sua própria função.

### Atribuir usuários a uma função personalizada

1. Abra a função personalizada de **Usuários** > **Funções personalizadas**.
1. Na seção **Usuários**, procure o usuário que deseja adicionar.
1. Selecione o usuário para adicioná-lo à função.
1. Selecione **Salvar**.

### Remover usuários de uma função personalizada

1. Abra a função personalizada de **Usuários** > **Funções personalizadas**.
1. Na seção **Usuários**, localize o usuário que você deseja remover.
1. Selecione a ação de remoção ao lado do nome.
1. Selecione **Salvar**.

### Remover usuários excluídos

1. Selecione **Usuários** na navegação à esquerda.
1. Selecione **Limpeza de Usuário**.
1. Use o campo de pesquisa ou o filtro Mês de exclusão para localizar os usuários que deseja remover.
1. Marque a caixa de seleção ao lado de usuários individuais ou selecione **Selecionar tudo** para selecionar todos os resultados.
1. Selecione **Ações** > **Limpar Usuário**.

## Atribuir várias funções personalizadas a um usuário

É possível atribuir várias funções personalizadas a usuários usando as seguintes maneiras:

* Usar a interface: é possível atribuir mais de uma função personalizada a um usuário diretamente da interface do Adobe Learning Manager.
* Usar upload de CSV: você pode fazer upload de um arquivo CSV para atribuir várias funções personalizadas a vários usuários ao mesmo tempo.

Isso facilita o gerenciamento do acesso do usuário e o controle de permissões no sistema.

### Atribuir várias funções personalizadas por meio da interface de usuário

Atribuir várias funções personalizadas por meio do Admin Console no Adobe Learning Manager é uma opção rápida e intuitiva ideal para integração, ajustes de permissão ou atualizações menores. As funções podem ser atribuídas visualmente, sem a necessidade de uploads de CSV, o que reduz o risco de erros e fornece visibilidade em tempo real. Esse método oferece suporte a atualizações rápidas à medida que as responsabilidades mudam e permite a alternância e a delegação de funções conforme necessário.

Para atribuir várias funções personalizadas a um usuário, siga estas etapas:

1. Faça logon como administrador e selecione **[!UICONTROL Usuários]**.
2. Selecione **[!UICONTROL Funções personalizadas]** no painel esquerdo.
3. Crie uma nova função personalizada e adicione privilégios de conta, catálogos, objetos de aprendizado ou escopos. Consulte as [etapas mencionadas aqui](#create-a-custom-role).
4. Adicionar usuários à função personalizada.

   ![](assets/add-users-in-custom-roles.png)
   _Atribuir usuários a uma função personalizada_

5. Selecione **[!UICONTROL Salvar]**.

Selecione várias funções personalizadas para um usuário conforme necessário. Cada usuário pode ter até 50 atribuições de função personalizadas. O número de funções disponíveis diminui com cada atribuição.

Depois de atribuir usuários a uma função personalizada adicional, você pode ver quantas atribuições de função permanecem disponíveis para cada usuário.

>[!NOTE]
>
>Você pode atribuir até 50 funções a cada usuário e adicionar até 3.500 usuários a cada função.

### Atribuir várias funções personalizadas usando CSV

Fazer upload de um arquivo CSV no Adobe Learning Manager permite a atribuição em massa eficiente de funções personalizadas. Esse processo é benéfico principalmente para a integração de um grande número de funcionários, a reorganização de equipes ou a atualização do acesso a novos treinamentos. As importações de CSV poupam o esforço manual, garantem atribuições consistentes e reduzem erros. Esse método é especialmente útil durante fusões, atualizações em todo o departamento ou implementações de treinamento global. Esse método ajuda os administradores a economizar tempo, padronizar funções e manter a governança.

Agora você pode atribuir várias funções a um usuário por meio da importação de CSV enviando dois arquivos para o Box:

* [role.csv](assets/role.csv)
* [user_role.csv](assets/user_role.csv)

O arquivo user_role.csv inclui os campos Função personalizada e IDs de usuário.

O arquivo role.csv inclui os campos, a função Personalizada, a Origem da criação e informações detalhadas para Catálogos, Usuários, Cursos, Caminhos de aprendizado e muito mais.

Se o arquivo CSV tiver dados incorretos ou ultrapassar os limites (50 funções por usuário e 3500 usuários por função), uma mensagem será exibida mostrando os erros.

![](assets/error-custom-role.png)
_Notificação de erro para funções personalizadas_
Os usuários recebem notificações por email quando as funções são atribuídas, incluindo o nome da função.

### Gerenciar funções personalizadas

Os administradores podem atualizar, adicionar ou remover funções personalizadas para usuários no Adobe Learning Manager à medida que as responsabilidades mudam. Isso garante que o acesso se alinhe às funções atuais sem afetar o histórico de aprendizado ou os dados de inscrição. Na página **[!UICONTROL Usuários]**, o administrador pode pesquisar usuários, exibir suas funções e ajustá-las usando a opção Gerenciar Funções Personalizadas. Essa interface guiada permite fácil adição ou remoção de funções, mantendo a governança e a segurança.

>[!NOTE]
>
>Os administradores personalizados não podem gerenciar funções personalizadas (adicionar ou remover função personalizada) ou promover a si mesmos para a função de administrador.

Depois de atribuir funções personalizadas aos usuários, você pode adicionar ou remover funções personalizadas da página **[!UICONTROL Usuários]**.

1. Pesquise um usuário na página **[!UICONTROL Usuários]**.

   ![](assets/search-user-role.png)
   _Pesquisar um usuário na página Usuários_

2. Selecione a seta suspensa no final da linha em que o nome de usuário é exibido e selecione **[!UICONTROL Gerenciar funções personalizadas]**.

   ![](assets/select-manage-custom-roles.png)
   _Selecione Gerenciar funções personalizadas na página do usuário_

3. É exibida uma caixa de diálogo com a lista de funções personalizadas atribuídas ao usuário. Selecione **[!UICONTROL Adicionar/remover funções]** para adicionar ou remover funções personalizadas atribuídas ao usuário.

   ![](assets/add-remove-roles.png)
   _Selecione Adicionar/Remover funções no prompt Gerenciar Funções Personalizadas_

4. Pesquise outras funções personalizadas a serem atribuídas ao usuário. Depois de localizar um, selecione a função personalizada.

   ![](assets/add-new-custom-role.png)
   _Selecione a função personalizada_

5. Selecione **[!UICONTROL Salvar]**. Uma caixa de diálogo de confirmação da alteração na função personalizada é exibida. Selecione **[!UICONTROL Sim]**.

   ![](assets/confirmation-prompt.png)
   _Selecione Sim no prompt de confirmação_

Uma terceira função personalizada é atribuída ao usuário.

Para remover as funções personalizadas, siga estas etapas:

1. Pesquise um usuário na página **[!UICONTROL Usuários]**.
2. Selecione a lista suspensa ao lado do usuário e selecione **[!UICONTROL Gerenciar funções personalizadas]**.
3. Selecione **[!UICONTROL Adicionar/remover funções]** para adicionar ou remover funções personalizadas.
4. Selecione o **[!UICONTROL ícone de remoção]** para excluir a função personalizada.

   ![](assets/remove-custom-roles.png)
   _Remover funções personalizadas_

### Alternar funções personalizadas

Para exibir e selecionar quaisquer funções personalizadas atribuídas a você, use a opção **[!UICONTROL Alternar função personalizada]**.

![](assets/switch-roles.png)
_Selecionar funções personalizadas_

Os usuários recebem notificações por email quando as funções personalizadas são atribuídas a eles. Os e-mails agora incluem nomes de funções para maior clareza.

## Baixar o relatório de função personalizada

Os administradores podem baixar um relatório CSV listando todas as funções personalizadas e suas permissões associadas. O relatório indica se cada função foi criada manualmente ou por meio de upload de CSV e fornece um resumo do acesso e dos privilégios atribuídos a cada função.

Para baixar o relatório, siga estas etapas:

1. Faça logon como **[!UICONTROL Administrador]**.
2. Selecione **[!UICONTROL Usuários]** > **[!UICONTROL Funções Personalizadas]**.
3. Selecione a opção **[!UICONTROL Baixar]** para baixar o relatório CSV.

![](assets/download-report.png)
_Baixar relatório de funções personalizadas_

O relatório tem dois arquivos CSV: role.csv e user_role.csv. O arquivo role.csv inclui:

* Função personalizada
* IDs de usuário
* Origem da criação.

O arquivo user_role.csv inclui os campos, a função Personalizada, a Origem da criação e informações detalhadas para Catálogos, Usuários, Cursos, Caminhos de aprendizado e muito mais.

## Trilha de auditoria para funções personalizadas

Os administradores podem baixar o relatório de auditoria da função personalizada para rastrear todas as alterações feitas nas funções personalizadas, incluindo a criação, modificação e exclusão de funções personalizadas e o acesso a seus recursos associados.

Consulte este artigo [Trilha de auditoria para funções personalizadas](/help/migrated/administrators/feature-summary/reports.md#audit-trail-for-custom-roles) para obter mais informações.

## Restringir o acesso de pasta para autores personalizados {#folder-custom-author}

O Learning Manager já oferece suporte à capacidade de conceder acesso à biblioteca de conteúdo usando funções personalizadas. Todos os autores personalizados que já têm acesso à biblioteca de conteúdo continuarão a ter acesso a todos os arquivos de conteúdo mesmo depois que as pastas de conteúdo forem configuradas. Isso é para manter o comportamento herdado. Os administradores não precisam fazer alterações caso queiram continuar com o comportamento atual.

Caso deseje restringir o acesso a esses autores personalizados, os administradores precisam editar a função personalizada existente e configurá-la fornecendo acesso apenas a pastas de conteúdo específicas.

![](assets/folder-access-forcustomauthors.png)

*Restringir o acesso de pasta para autores personalizados*

Ao criar um autor personalizado, será possível atribuir pastas de conteúdo ao autor. Escolha a opção **Pastas selecionadas**.

Depois de clicar na opção, uma nova caixa de diálogo é aberta. Nela, você poderá atribuir as pastas ao autor personalizado.

![](assets/choose-folder.png)

*Selecione as pastas para o autor personalizado*

Escolha as pastas e clique em **[!UICONTROL OK]**.

## Painel Resumo do aprendizado para administrador personalizado {#custom-admin-dashboard}

Os administradores personalizados podem ver a mesma exibição que um administrador vê. Um administrador personalizado pode ter dados fora do escopo. Isso só é aplicável se o administrador personalizado tiver escopo completo. Para conceder um escopo completo, ao criar um administrador personalizado, ative a opção **[!UICONTROL Controle total]** no Relatório de resumo da conta.

![](assets/create-custom-role.png)

*Criar uma função personalizada*

Como resultado, as opções **[!UICONTROL Todos os catálogos]** e **[!UICONTROL Todos os grupos de usuários]** serão selecionadas e o restante desativado.

![](assets/scope-of-featureprivileges.png)

*Definir escopo de privilégios*

## Permissões implícitas {#implicitpermissions}

Quando um usuário recebe uma função com uma entidade específica, pode haver casos nos quais ele precise acessar outras entidades para poder executar tarefas na entidade concedida. Na Instância, se um usuário recebe o acesso Criar na entidade Curso, ele precisa ter acesso às entidades Habilidades e Etiqueta para que ele possa se associar ao curso que está sendo criado. Estas tabelas fornecem informações sobre essas permissões implícitas.

<table>
 <tbody>
  <tr>
   <th>Tipo de acesso</th>
   <th>Permissão de entidade concedida pelo administrador</th>
   <th>Permissão implícita de entidade</th>
   <th>Acesso implícito</th>
  </tr>
  <tr>
   <td>Gerenciar</td>
   <td>Usuário</td>
   <td>Grupo</td>
   <td>Criar, ler, atualizar e excluir</td>
  </tr>
  <tr>
   <td>Inscrever</td>
   <td>Qualquer objeto de aprendizado (curso, ajuda de tarefa, programa de aprendizado, certificação)</td>
   <td>Usuário<br>
     Plano de aprendizado</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>Criar</td>
   <td>
    <p>Grupo de conteúdo<br>
      Ajuda de tarefa<br></p></td>
   <td>Etiqueta</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>Criar</td>
   <td>Curso</td>
   <td>Grupo de conteúdo<br>
     Tag<br>
     Habilidade<br>
     Medalha<br>
     Ajuda de tarefa</td>
   <td>Leitura em todos</td>
  </tr>
  <tr>
   <td>Criar</td>
   <td>Programa de aprendizado<br>
     Certificação<br></td>
   <td>Curso<br>
     Tag<br>
     Habilidade<br>
     Medalha</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>Criar</td>
   <td>Plano de aprendizado</td>
   <td>Catálogo<br>
     Agrupar<br>
     Habilidade<br>
     Todas as perdas (curso, ajuda de tarefa, programa de aprendizado, certificação)</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>Criar</td>
   <td>Anúncio</td>
   <td>Usuário<br>
     Agrupar<br>
     Todas as perdas (curso, ajuda de tarefa, programa de aprendizado, certificação)</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>Criar</td>
   <td>Gamificação</td>
   <td>Marca</td>
   <td>Escrever</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Usuário</td>
   <td>Faturamento</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Catálogo</td>
   <td>Grupo<br>
     Todas as perdas (curso, ajuda de tarefa, programa de aprendizado, certificação)</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Configuração</td>
   <td>Marca<br>
     Usuário</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Marca</td>
   <td>Configuração</td>
   <td>Ler</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Faturamento<br>
     Gamificação</td>
   <td>Usuário</td>
   <td>Ler</td>
  </tr>
 </tbody>
</table>

## Acessar uma função personalizada {#accessacustomrole}

Quando um administrador atribui uma função personalizada, você recebe uma notificação por e-mail.

Observação: Se já tiver feito logon no Learning Manager com uma função personalizada, você precisará fazer logon novamente no Learning Manager para acessar a nova função.

Para alternar entre funções, clique no ícone do perfil no canto superior direito do Learning Manager e selecione a função.

## Planos de aprendizado com escopo definido por funções configuráveis {#scopeconfigure}

Em versões anteriores do Learning Manager, qualquer função personalizada com permissão para criar planos de aprendizado podia ampliar o escopo do plano de aprendizado a todos os tipos de grupos de usuários e objetos de aprendizado.

A configuração de escopo era desativada quando era concedido acesso ao plano de aprendizado, o que dava ao usuário acesso a todos os catálogos e a todos os grupos de usuários por padrão.

Todos os planos de aprendizado criados por um administrador, por padrão, são aplicáveis a todos os usuários. Os usuários também podem ser atribuídos a qualquer objeto de aprendizado. Por outro lado, os usuários com funções personalizadas têm acesso a escopos completos, por exemplo, todos os catálogos, objetos de aprendizado ou grupos de usuários. Isso significava que os administradores não conseguiam criar funções personalizadas conforme o esperado, o que permitia o acesso aos planos de aprendizado para usuários com escopo limitado.

Nesta atualização do Learning Manager, você pode criar funções personalizadas para os planos de aprendizado que permitem criar o escopo de usuários e objetos de aprendizado. Em outras palavras, os Planos de aprendizado podem ser criados com um escopo limitado, derivado do escopo da função de um administrador personalizado.

Agora, um administrador pode definir ou restringir o escopo ao conceder acesso ao gerenciamento do plano de aprendizado.

Os administradores personalizados podem criar planos de aprendizado com um escopo limitado, determinado pelo escopo da função configurável do administrador personalizado. Esses planos de aprendizado só são acessíveis a administradores personalizados com a mesma função, além de serem acessíveis a administradores regulares. Além disso, os administradores personalizados não podem ver nenhum outro plano de aprendizado na conta.

Os administradores personalizados existentes, que têm acesso aos planos de aprendizado, sempre terão escopo completo (por definição). Eles terão acesso a todos os planos de aprendizado na conta, assim como os administradores regulares têm. Novas funções personalizadas criadas com escopo completo e novos administradores personalizados adicionados a essas funções continuarão a ter acesso a todos os planos de aprendizado.

Os planos de aprendizado criados pelo administrador e pelos administradores personalizados de escopo completo serão criados normalmente e não serão limitados pelo escopo.

Na seção **Escopo dos privilégios do recurso**, conceda acesso a grupos de usuários e/ou catálogo para a função personalizada.

![](assets/scope-for-featureprivileges.png)

*Conceder acesso a Grupos de Usuários e/ou Catálogo para a Função Personalizada*

Atribua um usuário à função personalizada.

![](assets/assign-users-to-customrole.png)

*Atribuir um usuário a uma Função Personalizada*

O usuário agora faz logon no Learning Manager como administrador personalizado e adiciona um plano de aprendizado.

Quando um novo aluno é adicionado, o administrador personalizado pode selecionar um treinamento somente nos catálogos com escopo da função configurável.

Agora, este plano de aprendizado é aplicável ao aluno apenas se o usuário também for adicionado ao grupo no grupo de usuários com escopo do plano de aprendizado. Todos os outros alunos são isentos deste plano de aprendizado.

## O aluno é adicionado ao grupo {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

O administrador personalizado pode selecionar qualquer grupo de usuários dentro do grupo de usuários com escopo da função.

Quando um usuário é adicionado ao grupo especificado, somente os usuários que já fazem parte do grupo de usuários com escopo do plano de aprendizado e foram adicionados ao grupo de usuários especificado serão atribuídos ao objeto de aprendizado.

## Alteração no escopo {#changeinscope}

Quando o administrador altera o escopo da função personalizada, a alteração também é transmitida em cascata para o administrador personalizado. Quando o administrador personalizado escolhe um plano de aprendizado que já estava no escopo de uma função personalizada anterior, uma mensagem é exibida, conforme mostrado abaixo:

![](assets/change-scope.png)

*Mensagem após alterações de escopo*

O administrador personalizado agora deve atualizar ou atualizar o escopo anterior para o novo escopo.

Clicar em **[!UICONTROL Atualizar escopo]** atualiza o escopo. É exibida uma mensagem de aviso.

![](assets/refresh-scope-message.png)

*Mensagem de aviso após atualizar um escopo*

Clicar em **[!UICONTROL Sim]** atualiza o escopo.

## Adicionar relatório de gamificação a uma função personalizada {#gamification-custom}

Um administrador pode ativar relatórios de gamificação para um usuário personalizado.

1. Na página **[!UICONTROL Funções personalizadas]**, digite o nome da função personalizada.
1. Na seção **[!UICONTROL Privilégios do Recurso: Recursos Principais]**, habilite a opção **[!UICONTROL Controle Total]** para a categoria **[!UICONTROL Relatórios]**.

1. Na seção **[!UICONTROL Usuários]**, selecione o usuário ao qual será atribuída a função personalizada recém-criada.
1. Clique em **[!UICONTROL Salvar]**.

Quando um usuário faz logon como administrador personalizado e clica em **[!UICONTROL Relatórios]** no painel esquerdo, as transcrições são exibidas, conforme mostrado abaixo:

![](assets/download-gamificationtranscripts.png)

*Baixar as transcrições de gamificação*

Clique em **[!UICONTROL Transcrições de gamificação]**, escolha um usuário e gere o relatório.

Se um administrador alterar os pontos de nível, os relatórios mostrarão os níveis de acordo com os pontos atuais.

Redefinir gamificação não redefine o nível atingido.

## Perguntas frequentes

**O que acontece se um administrador completo remover uma permissão da minha função personalizada?**

Sua função mantém as permissões existentes até a próxima vez que um administrador completo abrir e salvar sua definição de função. A alteração não tem efeito imediatamente. Suas permissões atuais permanecem em vigor até que sua função seja explicitamente editada e salva.

**Posso conceder acesso ao catálogo de funções aos catálogos que não posso acessar?**

Não. O escopo de qualquer função criada é limitado aos catálogos e grupos de usuários dentro de seu próprio escopo. Não é possível criar uma função com acesso mais amplo do que o que você mesmo retém, a menos que o administrador tenha configurado sua conta para permitir a administração de função expandida.

**Qual é a diferença entre Somente Leitura e Controle Total?**

**Somente Leitura** oferece a capacidade de exibir **Funções Personalizadas**, Campos Ativos, **Logs de Importação** e **Limpeza de Usuário**. Você pode procurar, pesquisar e baixar relatórios, mas não pode executar nenhuma ação. O **Controle Total** oferece todos esses recursos, além da capacidade de criar, editar e excluir funções, importar usuários via CSV, atribuir e remover usuários de funções e limpar usuários excluídos.

**Posso atribuir a uma função as mesmas permissões que tenho?**

Sim Você pode atribuir qualquer permissão que você possua pessoalmente às funções que criar. Você não pode exceder seu próprio conjunto de permissões, mas pode criar funções com o mesmo nível de acesso que você tem ou qualquer subconjunto dele.

**A trilha de auditoria mostra quem eu sou quando faço alterações?**

Sim O relatório de auditoria lista sua função personalizada como a origem de cada alteração. Isso significa que os administradores completos podem ver qual função personalizada fez determinada alteração no sistema.

**O que acontece com as funções existentes quando este recurso está habilitado para a conta?**

Funções personalizadas existentes com acesso **Avançado** já habilitadas obtêm acesso automático aos **Logs de Importação**. Todos os outros comportamentos existentes permanecem inalterados. As funções que não têm acesso Avançado ativado não são afetadas.

