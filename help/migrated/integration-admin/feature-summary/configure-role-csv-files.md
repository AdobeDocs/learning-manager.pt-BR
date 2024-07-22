---
jcr-language: en_us
title: Gerenciar funções personalizadas através de arquivos CSV
description: O administrador de integração pode adicionar várias funções personalizadas em massa à conta através do CSV, além de atribuir as mesmas a vários usuários. Essa abordagem automatiza o processo de criação de funções personalizadas.
contentowner: saghosh
exl-id: fce2f457-2834-491a-8331-64086f5a51b5
source-git-commit: f328076016d8c41455cad71f00d1dc9a1531e007
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 81%

---

# Gerenciar funções personalizadas através de arquivos CSV

O administrador de integração pode adicionar várias funções personalizadas em massa à conta através do CSV, além de atribuir as mesmas a vários usuários. Essa abordagem automatiza o processo de criação de funções personalizadas.

Você pode configurar funções usando os conectores de FTP e do Box no Learning Manager.

Depois de fazer logon na conta de armazenamento do Box, o administrador de integração pode adicionar os seguintes csvs à conta:

* user.csv
* role.csv
* user_role.csv

Para começar, baixe os CSVs e altere os valores de acordo com seus requisitos.

* Arquivo de exemplo: [role.csv](assets/role.csv)
* Arquivo de exemplo: [user_role.csv](assets/user_role.csv)

**role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Nome da coluna</b></p></td>
   <td>
    <p><b>Descrição</b></p></td>
   <td>
    <p><b>Valores de exemplo</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Name</p></td>
   <td>
    <p>Identifique a função a ser atribuída aos usuários no CSV.</p></td>
   <td>
    <p>Autor de vendas</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identifique o Tipo de Acesso (COMPLETO, GRAVAÇÃO, INSCRIÇÃO, RELATÓRIO, NENHUM) para cada tipo de entidade, como CURSO, CATÁLOGO etc.</p></td>
   <td>
    <p>COMPLETO</p>
    <p>NENHUM</p>
    <p>GRAVAÇÃO | RELATÓRIO</p>
    <p>Os nomes das colunas corresponderão aos nomes dos tipos de entidade, como Catálogo, Curso, Plano de aprendizado, etc.</p>
    <p>Uma coluna para cada tipo de entidade estará presente no CSV. Entidades que não devem receber permissões devem ser incluídas com o valor NONE</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador do escopo do catálogo</p></td>
   <td>
    <p>Nome do catálogo individual ou lista de nomes de catálogos separada por PIPE (|) que determina o escopo desta função.</p></td>
   <td>
    <p>Catálogo de vendas | Catálogo geral</p></td>
  </tr>
  <tr>
   <td>
    <p>Especificador de Escopo do Grupo de Usuários</p></td>
   <td>
    <p>Nome e valor do atributo do grupo de usuários que determinam o escopo dos usuários dessa função.</p>
    <p>Consulte a seção abaixo para obter os escopos.</p></td>
   <td>
    <p>location=Londres</p></td>
  </tr>
  <tr>
   <td>
    <p>Descrição</p></td>
   <td>
    <p>Descrição amigável opcional para ajudar a entender o propósito da função e para referência posterior.</p></td>
   <td>
    <p>Acesso total do autor aos OAs no catálogo de vendas</p></td>
  </tr>
 </tbody>
</table>

Todas as colunas com exceção da descrição são obrigatórias.

## Definir o escopo dos grupos de usuários {#definescopeofusergroups}

Você pode especificar escopos para grupos de usuários de vários tipos de grupos das seguintes maneiras:

* Nome do grupo de usuários como está (por exemplo, Todos os autores, Meu grupo personalizado)
* Atributo de folha e valor (por exemplo, Departament=RecursosHumanos)
* Grupos de perfis de autorregistro (self_registration=nomedeperfil)
* Grupos de perfis de registro externos (ext_registration=nomedeperfil)
* Uma equipe de subordinados diretos de um gerente (manager_direct=`<emailid>`)
* Uma organização completa de gerente (manager_org=`<emailid>`)

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
    <p>Id</p></td>
   <td>
    <p>ID do e-mail do usuário a ser atribuído a uma função configurável.</p></td>
   <td>
    <p>Se o usuário já tiver uma função configurável atribuída, a função será substituída pela nova função especificada no CSV. Nenhum erro foi relatado.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Nome da função configurável a ser atribuída ao usuário</p></td>
   <td>
    <p>O nome da função deve ser uma função existente, especificada no CSV. Funções criadas pelo administrador por meio da interface podem ser usadas aqui.</p></td>
  </tr>
 </tbody>
</table>

**Recursos do escopo completo**

Sempre que a permissão completa é atribuída para qualquer um dos seguintes recursos (recursos de nível da conta), o escopo do grupo de usuários e o escopo do catálogo são automaticamente designados como COMPLETO, já que o usuário não pode ter acesso limitado a esses recursos.

Os nomes de catálogo ou nomes de grupo de usuários fornecidos no CSV serão substituídos pela permissão COMPLETA.

* Comunicados
* Habilidades
* Gamificação
* Usuários
* Planos de aprendizado
* Modelos de e-mail

## Adicione os CSVs de função na conta {#addtherolecsvsintheaccount}

Na sua conta Box, escolha **Import > user> internal** e carregue os arquivos role.csv e user_role.csv.

* Os arquivos role.csv e user_role.csv devem ser copiados na pasta **Importar** > **usuário** > **interna** > **user_role**.
* O user.csv deve ser copiado na pasta **Importar** > **usuário** > **interna**.

Ambos os CSVs devem ser carregados somente por meio do Box e não podem ser carregados pela interface do usuário.

>[!NOTE]
>
>O arquivo CSV de Usuários é obrigatório, mas os CSVs de Função Personalizada são opcionais. Todos os arquivos presentes são processados, e os outros são ignorados.

As funções personalizadas criadas com o arquivo CSV não ficam visíveis na IU dos administradores. Essas funções não serão relacionadas ou afetadas por funções já criadas (ou criadas posteriormente) pela interface do usuário.

Funções personalizadas que foram criadas por um csv podem ser gerenciadas inteiramente por meio do próprio csv. Isso inclui adicionar, modificar e deletar atribuições.

As funções atribuídas podem ser revogadas removendo as entradas de atribuição do CSV user_role. Porém, as atribuições feitas através da IU do administrador não são afetadas por essa ação.

Para atribuir e revogar uma função personalizada, atualize os arquivos CSV.

## Sincronização de funções personalizadas {#synchronizationofcustomroles}

Depois que o administrador de integração fizer upload dos CSVs de função no armazenamento do Connector, ele pode habilitar a sincronização dos CSVs. Sempre que uma função personalizada for atualizada, adicionada ou excluída dos CSVs, o administrador pode sincronizar as informações nos arquivos para atualizar a lista de funções.

Na página Introdução do painel Administrador, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Fontes de Dados]**.

Na seção Configurações de sincronização, ative a opção **[!UICONTROL Ativar sincronização automática]**.

![](assets/sync-settings.png)

*Selecione a opção Habilitar Sincronização Automática*

Ao escolher essa opção, você pode programar o horário exato da sincronização no campo Horário da sincronização. Se você especificar como horário de sincronização 12:00 AM, as funções personalizadas serão atualizadas exatamente nesse horário todos os dias.

Se quiser sincronizar os dados sob demanda, clique em **[!UICONTROL Sincronizar agora]**.

## Restrições ao configurar funções {#constraintswhileconfiguringroles}

Em qualquer conta, o nome de uma Função deve ser exclusivo. Portanto, uma função criada por interface ou CSV não pode ter o mesmo nome de outra função já criada pela interface ou CSV.

No mesmo sentido, na interface do administrador, não é possível atribuir a um usuário uma função configurável criada por CSV, pois essas funções não estarão disponíveis.

No entanto, o CSV de atribuição de usuário pode ser usado para atribuir funções criadas pela interface.
