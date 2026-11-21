---
description: Saiba como integrar o conector do Zoom ao Adobe Learning Manager
jcr-language: en_us
title: Conector do Zoom
contentowner: mmanuel
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 3628dd3701949da127b138e0e1ffc2db8e84eab1
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 2%
---

# Conector do Zoom no Adobe Learning Manager

## Introdução

O conector do Zoom no Adobe Learning Manager permite que as organizações ofereçam sessões de sala de aula virtual ao vivo, gerenciem a inscrição do aluno e monitorem a participação e a conclusão. Ele também oferece suporte a várias conexões do Zoom em uma única conta, permitindo que os administradores de integração gerenciem o acesso com base em funções ou grupos de usuários, e que os autores selecionem as conexões disponíveis para as sessões do curso. Após a sessão, os dados de presença e desempenho são sincronizados com a Adobe Learning Manager para fins de relatório e acompanhamento.

## Configurar o conector do Zoom

Para configurar o conector do Zoom:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco **Zoom**.

   ![](assets/zoom-connector1.png)
   _Configurar o conector do Zoom no Adobe Learning Manager_

3. Selecione **Conectar**. A página Configuração do conector do Zoom é aberta.
4. Digite os seguintes detalhes da conta nos respectivos campos. Você pode obter essas credenciais do administrador da conta do Zoom:

   * Nome da conexão
   * ID da conta do Zoom
   * ID do cliente
   * Segredo do cliente
   * Endereço de email do superadministrador
   * Funções ou grupos que podem usar este conector (opcional)

   ![](assets/zoom-connector2.png)
   _Digite os detalhes da configuração para definir o conector do Zoom_

5. Selecione **Conectar** para estabelecer a integração.

>[!NOTE]
>
>Ao habilitar o conector, **os alunos devem usar o mesmo endereço de email** para suas contas do Zoom e do Adobe Learning Manager para garantir que os dados do usuário sejam sincronizados corretamente.

## Adicionar várias conexões do Zoom

É possível adicionar várias conexões do Zoom ao Adobe Learning Manager, com cada conexão vinculada a uma conta diferente do Zoom. Por exemplo, você pode criar conexões separadas para parceiros ou equipes diferentes e especificar quais funções ou grupos de usuários podem usar cada conexão.

O número de conexões que você pode adicionar depende do nível da sua conta da Adobe Learning Manager:

| **Camada de conta** | **Máximo de conexões do Zoom** |
|---|---|
| aplicativo | 6 |
| Ultimate | 50 |

## Criar cursos do Zoom

Depois que a conexão for estabelecida:

1. Faça logon como **Autor** e crie um novo curso de Sala de Aula Virtual.
2. Selecione **Zoom** como o sistema de conferência e selecione na lista a conexão do Zoom que deseja usar.
   >[!NOTE]
   >
   >A lista mostra apenas as conexões disponíveis para sua função ou grupo de usuários, e uma sessão usa uma conexão por vez.
3. Atribua alunos ao curso por meio de administradores, gerentes ou por meio da autoinscrição.
4. Após a inscrição, os alunos recebem um e-mail com os detalhes do curso.
5. Os alunos podem fazer logon na conta da Adobe Learning Manager para acessar o curso e ingressar na sessão de zoom.

## Conexões do Zoom disponíveis para Autores

Ao criar ou editar uma sessão do curso, você pode selecionar entre as conexões do Zoom disponíveis para sua função ou grupo de usuários. O administrador de integração define quais funções ou grupos de usuários podem acessar cada conexão do Zoom.

Por exemplo, suponha que um administrador de integração configure duas conexões do Zoom, **Zoom do Parceiro A** e **Zoom do Parceiro B**, e atribua cada conexão a um grupo de usuários diferente:

* Se você pertencer a ambos os grupos de Parceiro A e Parceiro B, poderá selecionar qualquer conexão.
* Se você pertence somente ao grupo Parceiro A, selecione **Zoom do Parceiro A**.
* Se você não pertencer a nenhum dos grupos, essas conexões não estarão disponíveis para seleção.

>[!NOTE]
>
>Você pode usar somente uma conexão do Zoom para uma sessão. Se várias conexões estiverem disponíveis para você, selecione a conexão que deseja usar para a sessão.

## Gerenciar conexões do Zoom

A página **Gerenciar Conexões** exibe as conexões de Zoom configuradas para sua conta. A coluna **Visível para** indica as funções ou grupos de usuários que podem usar cada conexão. Nesta página, você pode editar, ativar ou desativar e excluir conexões existentes do Zoom.

![Conexão de zoom Configurar página com Habilitar configurações de Conexão, Credenciais e Funções ou grupos](assets/zoom-connection-configure-page.png "Conexão de zoom Configurar página com Habilitar configurações de Conexão, Credenciais e Funções ou grupos")

### Editar uma conexão com o Zoom

Para editar uma conexão com o Zoom existente:

1. Selecione a conexão na página **Gerenciar Conexões** que deseja editar.
1. Na guia Configurar, atualize qualquer uma das seguintes opções:

   1. Para atualizar as credenciais da conta do Zoom, selecione **Editar** ao lado de **Credenciais** e atualize os detalhes necessários.
   1. Para alterar quem pode usar a conexão, atualize **Funções ou grupos** que podem usar este conector.

1. Selecione **Salvar**.

### Ativar ou desativar uma conexão com o Zoom

Novas conexões de Zoom são habilitadas por padrão. É possível desativar uma conexão para impedir que os autores a usem sem excluir a conexão.

Para desativar uma conexão:

1. Na página **Gerenciar Conexões**, selecione a conexão que deseja desabilitar.
1. Ative a **Habilitar Conexão**.
1. Selecione **Salvar**.

   A conexão desabilitada não está mais disponível para usuários nas funções ou grupos associados.

Para habilitar a conexão novamente, selecione **Habilitar Conexão** e selecione **Salvar**.

### Excluir uma conexão do Zoom

Para excluir uma conexão do Zoom:

1. Na página **Gerenciar Conexões**, navegue até a conexão que deseja excluir.
1. Selecione o ícone **Excluir** ao lado da conexão.
1. Selecione **Excluir**.

## Rastrear a participação e a conclusão

Após o término da sessão virtual:

* O Adobe Learning Manager recebe automaticamente o status de conclusão do Zoom.
* Os administradores podem exibir os relatórios de participação e pontuação no Adobe Learning Manager para monitorar a participação e o desempenho do aluno.

## Criar um aplicativo OAuth de servidor para servidor do Zoom

Para usar o conector do Zoom com o Adobe Learning Manager, você deve criar um aplicativo OAuth de servidor para servidor do Zoom e configurar os escopos necessários.

### Escopos OAuth necessários

Ao criar o aplicativo no Zoom, verifique se os seguintes escopos estão selecionados:

| O que você quer | Pesquisar esta palavra-chave | Em seguida, escolha |
|---|---|---|
| Exibir todas as reuniões de usuários | reunião | `meeting:read:meeting:admin, meeting:read:list_meetings:admin` |
| Exibir/gerenciar todas as reuniões de usuários | reunião | `meeting:update:meeting:admin, meeting:delete:meeting:admin, meeting:write:meeting:admin` |
| Exibir dados do relatório | resumo | `report:read:meeting:admin, report:read:user:admin` (Escolha aquele que corresponde ao seu ponto de extremidade.) |
| Exibir todas as informações do usuário | usuário | `user:read:user:admin, user:read:list_users:admin` |
| Gerenciar usuários | usuário | `user:update:user:admin, user:write:user:admin` |
| Adicionar um inscrito de reunião | inscrito | `meeting:write:registrant:admin` |
| Listar todos os inscritos na reunião | inscrito | `meeting:read:list_registrants:admin` |
| Reuniões de subcontas | reunião + procurar :master | `meeting:write:meeting:master` |
| Relatório de participantes da reunião | participante | `report:read:list_meeting_participants:admin` |

