---
jcr-language: en_us
title: Gerenciar funções personalizadas por meio de arquivos CSV
description: O administrador de integração pode adicionar um número de funções personalizadas à sua conta em massa via CSV, bem como atribuir as mesmas funções a vários usuários. Essa abordagem automatiza o processo de criação de funções personalizadas.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---



# Gerenciar funções personalizadas por meio de arquivos CSV

O administrador de integração pode adicionar um número de funções personalizadas à sua conta em massa via CSV, bem como atribuir as mesmas funções a vários usuários. Essa abordagem automatiza o processo de criação de funções personalizadas.

Você pode configurar funções usando os conectores FTP e Box no Learning Manager.

Depois de fazer logon na conta de armazenamento do Box ou ExaVault, o administrador de integração pode adicionar os seguintes csvs na conta:

* role.csv
* user_role.csv

Para começar, baixe os csvs e altere os valores de acordo com seus requisitos.

**role.csv**
[Arquivo de exemplo - role.csv](assets/role.csv) [Arquivo de exemplo- user_role.csv](assets/user-role.csv)

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nome da coluna</b></p></td>
   <td>
    <p><b>Descrição</b></p></td>
   <td>
    <p><b>Valores de Exemplo</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Nome</p></td>
   <td>
    <p>Identifique a função no CSV a ser atribuída aos usuários.</p></td>
   <td>
    <p>Autor de Vendas</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifique o Tipo de Acesso (COMPLETO, GRAVAÇÃO, INSCRIÇÃO, RELATÓRIO, NENHUM) para cada tipo de entidade, como CURSO, CATÁLOGO etc.</p></td>
   <td>
    <p>COMPLETO</p>
    <p>NENHUM</p>
    <p>GRAVAR | RELATÓRIO</p>
    <p>Os nomes das colunas corresponderão aos nomes dos tipos de entidade, como Catálogo, Curso, Plano de Aprendizado etc.</p>
    <p>Uma coluna para cada tipo de entidade estará presente no CSV. As entidades para as quais não deve ser dada autorização devem ser incluídas com um valor de NENHUM</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador de Escopo do Catálogo</p></td>
   <td>
    <p>Nome de catálogo único ou uma lista separada por PIPE (|) de nomes de catálogo que determinam o escopo dessa função.</p></td>
   <td>
    <p>Catálogo de Vendas | Catálogo Geral</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador de Escopo do Grupo de Usuários</p></td>
   <td>
    <p>Nome e valor do Atributo do Grupo de Usuários que determinam o escopo dos usuários desta função.</p>
    <p>Consulte a seção abaixo para ver os escopos.</p></td>
   <td>
    <p>location=Londres</p></td>
  </tr>
  <tr>
   <td>
    <p>Descrição</p></td>
   <td>
    <p>Descrição amigável opcional para ajudar a entender a finalidade da função e da referência posterior.</p></td>
   <td>
    <p>Acesso total do autor aos LOs no catálogo de vendas</p></td>
  </tr>
 </tbody>
</table>

Todas as colunas, exceto Descrição, são obrigatórias.

## Definir escopo dos grupos de usuários {#definescopeofusergroups}

É possível especificar escopos para grupos de usuários de vários tipos de grupos das seguintes maneiras:

* O nome do grupo de usuários como está (por exemplo, Todos os autores, Meu grupo personalizado)
* Atributo folha e valor (por exemplo, Departamento=HR)
* Grupos de perfis de autorregistro (self_registration=profilename)
* Grupos de perfis de registro externo (ext_registration=profilename)
* Uma equipe de subordinados diretos do gerente (manager_direct=`<emailid>`)
* Organização completa de um gerente (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nome da coluna</b></p></td>
   <td>
    <p><b>Descrição</b></p></td>
   <td>
    <p><b>Comentário</b></p></td>
  </tr>
  <tr>
   <td>
    <p>ID</p></td>
   <td>
    <p>A ID de email do usuário a ser atribuído a uma função configurável.</p></td>
   <td>
    <p>Se o usuário já tiver uma função configurável atribuída, a função será substituída por uma nova função especificada no CSV. Nenhum erro informado.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Nome da função configurável a ser atribuída ao usuário</p></td>
   <td>
    <p>O nome da função deve ser uma função existente conforme especificado no CSV. As funções criadas pelo administrador por meio da interface podem ser usadas aqui.</p></td>
  </tr>
 </tbody>
</table>

**Recursos do escopo completo**

Sempre que a Permissão Completa for atribuída a qualquer um dos seguintes recursos (recursos no nível da conta), o Escopo do Grupo de Usuários e o Escopo do Catálogo são considerados automaticamente COMPLETOS, pois o usuário não pode ter acesso limitado a esses recursos.

Se algum nome de catálogo ou nome de grupo de usuários for fornecido no CSV, ele será substituído com a permissão FULL.

* Comunicados
* Habilidades
* Gamificação
* Usuários
* Planos de aprendizado
* Modelos de e-mail

## Adicione os role-CSVs na conta {#addtherolecsvsintheaccount}

Na sua conta do Box, selecione **Importar > usuário > interno** e faça upload dos arquivos role.csv e user_role.csv.

* Os CSVs de função personalizada devem ser copiados na pasta “import->user->internal->user_role”
* O CSV de Usuários deve ser copiado na pasta “import->user->internal”

Os arquivos CSV devem ser carregados somente via Box ou FTP e não podem ser carregados pela interface do usuário.

>[!NOTE]
>
>O arquivo CSV de Usuários é obrigatório, mas os CSVs de Função Personalizada são opcionais. Todos os arquivos presentes são processados e outros são ignorados.

As funções personalizadas criadas usando o arquivo csv não são visíveis para administradores na interface do usuário. Essas funções não serão relacionadas ou afetadas por funções criadas (ou a serem criadas posteriormente) pela interface do usuário.

Funções personalizadas que foram criadas por um csv podem ser gerenciadas inteiramente por meio do próprio csv. Isso inclui adicionar, modificar e deletar atribuições.

As funções atribuídas podem ser revogadas removendo entradas de atribuição do csv user_role. Mas as atribuições feitas por meio da interface do administrador não são afetadas por isso.

Para atribuir e revogar uma função personalizada, atualize os arquivos csv.

## Sincronização de funções personalizadas {#synchronizationofcustomroles}

Depois que o administrador de integração faz upload dos CSVs baseados em função no armazenamento do conector, o administrador pode ativar a sincronização com os CSVs. Toda vez que uma função personalizada é atualizada, adicionada ou excluída nos CSVs, o administrador pode sincronizar as informações nos arquivos e tornar a lista de funções atual.

Na página Introdução do painel Administrador, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Fontes de dados]**.

Na seção Configurações de sincronização, ative a opção **[!UICONTROL Ativar sincronização automática]**.

![](assets/sync-settings.png)

*Selecione a opção Ativar sincronização automática*

Ao selecionar essa opção, você pode programar o horário da sincronização no horário exato especificado no campo Horário de sincronização. Se você especificar a hora da sincronização como 00:00, as funções personalizadas serão atualizadas exatamente na hora especificada todos os dias.

Se quiser sincronizar os dados sob demanda, clique em **[!UICONTROL Sincronizar Agora]**.

## Restrições ao configurar funções {#constraintswhileconfiguringroles}

Em qualquer conta, o nome de uma função deve ser exclusivo. Portanto, uma função criada por meio da interface do usuário ou do CSV não deve ter o mesmo nome de outra função já criada pela interface do usuário ou pelo CSV.

Em linhas semelhantes, na interface do administrador, não é possível atribuir uma função configurável a um usuário criada por meio de CSV, pois essas funções não estarão disponíveis.

No entanto, o CSV de atribuição de usuário pode ser usado para atribuir funções criadas pela interface do usuário.
