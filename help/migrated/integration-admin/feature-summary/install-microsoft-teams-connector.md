---
description: Instalar o conector do Microsoft Teams no Adobe Learning Manager
jcr-language: en_us
title: Instalar o conector do Microsoft Teams no Adobe Learning Manager
contentowner: saghosh
exl-id: 68092187-ac69-4727-a3dc-f3047a1e164d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '1258'
ht-degree: 24%

---

# Instalar o conector do Microsoft Teams no Adobe Learning Manager

## Visão geral

O Microsoft® Teams® é uma plataforma de colaboração baseada em bate-papo persistente que oferece suporte total ao compartilhamento de documentos, reuniões online e outros recursos para comunicações de negócios.

O Adobe Learning Manager usa um conector de sala de aula virtual que pode ser usado para integrar reuniões Microsoft Teams com o Learning Manager.

O conector do Microsoft Teams conecta os sistemas Learning Manager e Microsoft Teams para permitir a sincronização automática de reuniões virtuais. A lista a seguir descreve os recursos do conector do Microsoft Teams:

**Configurar sessões virtuais usando Microsoft Teams**

Este conector ajuda a integrar sua conta do Adobe Learning Manager com sua conta do Microsoft Teams. Uma vez integrado, o conector permite que um autor no Learning Manager use o Microsoft Teams como o provedor de serviços de tecnologia para os módulos de Sala de aula virtual criados no Learning Manager.

**Permitir que os Microsoft Teams autentiquem os alunos ao entrarem na sala de aula virtual**

Este conector ajuda a configurar o organizador de reuniões do Microsoft Teams no Learning Manager ao criar uma reunião. O Organizador de Reuniões pode gerenciar a sala de espera para restringir ou admitir a entrada em uma reunião, bem como controlar outras opções de reunião fornecidas pelo Microsoft Teams.

**Usar a sincronização automática de conclusão do usuário**

O processo de sincronização automática de conclusão do usuário permite que um administrador do Learning Manager busque automaticamente os registros de conclusão e URL de gravação para reuniões do Microsoft Teams.

## Funções no Microsoft Teams

Se estiver organizando uma reunião com vários participantes, você pode atribuir funções a cada participante para que um participante saiba o que pode fazer na reunião.

Há duas funções para escolher: **apresentador** e **participante**.

Para obter mais informações, consulte [Funções em uma reunião no Microsoft](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## Configurar o conector do Microsoft Teams

>[!NOTE]
>
>Os itens marcados como &lt;Desenvolvedor/Opcional> abaixo são opcionais e principalmente para configurar locatários de teste/desenvolvedor com a Microsoft, caso o usuário não tenha um locatário de produção. Eles são opcionais, uma vez que a maioria já teria sido realizada pelo administrador da sua equipe.

## Criar conta do desenvolvedor E5 da Microsoft &lt;Desenvolvedor/Opcional>

Você pode acessar o conector Microsoft Teams se tiver o Office 365 E3 ou o Office 365 E5. A opção recomendada é o Office 365 E5.

* Visite a [página de planos da Microsoft](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&amp;ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;lnkd=Google_O365SMB_Brand&amp;gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE) . Na página da Web, você pode comprar uma conta E3 ou E5 ou clicar em Experimente gratuitamente.

* Forneça as informações necessárias e crie uma conta.

>[!NOTE]
>
>A conta deve usar o formato `<username>@<company name>.onmicrosoft.com`.

## Criar aplicativo para o conector do Microsoft Teams

1. Visite o [portal do Microsoft Azure®](https://portal.azure.com/).
1. Faça logon com a conta do Microsoft E5 que você criou na seção anterior.
1. Pesquise por **Azure Ative Diretory**.
1. Clique em **[!UICONTROL Registros de Aplicativo]**.
1. Clique em **[!UICONTROL Novo Registro]**, insira os seguintes detalhes e registre o aplicativo:

   1. **Nome** - Qualquer nome da sua escolha.
   1. **Tipos de contas suportados** - contas em qualquer diretório organizacional (Qualquer Ative Diretory do Azure - multilocatário).
   1. **URI de redirecionamento (opcional)** - Campo opcional que indica a URL de resposta.

1. Na coluna **Essentials**, observe as seguintes IDs, que serão usadas posteriormente durante a integração:

   1. **ID do aplicativo (cliente)**
   1. **ID do diretório (locatário)**

1. Pesquise as credenciais do cliente e clique em **[!UICONTROL Adicionar um certificado ou segredo]**.
1. Clique em **[!UICONTROL Novo segredo do cliente]** e adicione os seguintes detalhes:

   1. **Descrição** - Insira qualquer nome.
   1. **Expira** - Defina qualquer valor (o valor recomendado é 24 meses. Certifique-se de que novas credenciais de cliente sejam geradas assim que a anterior expirar).

Observe o segredo do cliente, que será usado posteriormente durante a integração.

## Obter permissão de acesso para o conector Microsoft Teams

1. Visite o [portal do Microsoft Azure](https://portal.azure.com/).
1. Faça logon com o Microsoft E5 que você criou anteriormente.
1. Pesquise por **Azure Ative Diretory**.
1. Clique em **[!UICONTROL Registros de Aplicativo]**.
1. Clique no aplicativo que você criou na seção anterior.
1. Clique em **[!UICONTROL Permissões de API]**.
1. Clique em **[!UICONTROL Adicionar uma permissão]**.
1. Selecione **[!UICONTROL Microsoft Graph]** > **[!UICONTROL Permissões do aplicativo]** e adicione as seguintes permissões:

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All

1. Clique em **[!UICONTROL Conceder acesso de administrador para Adobe]**.
1. Clique em **[!UICONTROL Funções de aplicativo]** > **[!UICONTROL Criar função de aplicativo]**.
1. Insira os seguintes valores:

   1. **Nome de exibição** - Nome da API/Nome da permissão (por exemplo, Calendars.ReadWrite).

   1. **Tipos de membros permitidos** - Especifique usuários e aplicativos (Usuários/Grupos + Aplicativos).

   1. **Valor** - Nome da API/Nome da permissão (por exemplo, Calendars.ReadWrite).

   1. **Descrição** - Nome da API/Nome da permissão (por exemplo, Calendars.ReadWrite).

   1. **Deseja habilitar esta função de aplicativo?** - Marque esta caixa de seleção.

1. Repita as etapas anteriores para todas as nove API/Permissões que foram adicionadas.

## Configurar política de acesso usando scripts do PowerShell

Para configurar a política de acesso do aplicativo para o conector Microsoft Teams executando scripts do PowerShell, siga o procedimento descrito neste [documento](https://docs.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

Isso permite que o conector acesse reuniões online do Microsoft Teams.

>[!NOTE]
>
>No documento acima, execute a etapa opcional 5 também para garantir que qualquer usuário ativo possa receber a função de organizador de dentro do aplicativo Learning Manager Author. Se esta etapa não for executada, os usuários não terão as permissões de acesso necessárias para serem organizadores e a criação da reunião falhará (APIs do Microsoft consideram o organizador o criador de uma reunião do Teams).

## Configurar o conector de Microsoft Teams no Learning Manager

1. Faça logon no Learning Manager como Administrador de Integração.

1. Na página Conectores, selecione o conector Microsoft Teams e clique em **[!UICONTROL Conectar]**.

1. Insira estes valores:

   1. **Nome da Conexão** - Dê o nome que o autor verá ao criar a sessão.

   1. **ID do locatário de Microsoft Teams** - Insira o valor determinado anteriormente.

   1. **ID do cliente Microsoft Teams** - insira o valor determinado anteriormente.

   1. **Segredo do cliente de Microsoft Teams** - insira o valor determinado anteriormente.

   1. **Email do usuário administrador de Microsoft Teams** - Insira o email padrão do organizador. Este usuário (normalmente um usuário de serviço) seria o criador da reunião no caso de nenhum organizador explícito ser selecionado no aplicativo Learning Manager Author.

## Alocar licenças para usuários &lt;Desenvolvedor/Opcional>

1. Visite [https://admin.microsoft.com/#/homepage](https://admin.microsoft.com/#/homepage).
1. Clique em **[!UICONTROL Usuários]** > **[!UICONTROL Usuários ativos]**.
1. Clique em **[!UICONTROL Mais ações para usuários]** para os usuários para os quais deseja fornecer acesso a Microsoft Teams.
1. Clique em **[!UICONTROL Gerenciar Licenças de Produtos]**.
1. Ative a licença para o Office 365 E5 sem conferência de áudio.

## Gravar uma sessão

A API usada para gravar uma sessão é uma API protegida. Para acessar a API, você deve solicitar acesso da Microsoft. Para obter mais informações, consulte este [documento](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

No documento,

*”Para solicitar acesso a essas APIs protegidas, complete o seguinte [formulário de solicitação](https://aka.ms/teamsgraph/requestaccess). Revisamos as solicitações de acesso todas as quartas-feiras e implantamos as aprovações todas as sextas-feiras, exceto durante as principais semanas de feriados nos EUA. Os envios durante essas semanas serão processados &#x200B;&#x200B;na semana seguinte sem feriados. Para verificar se sua solicitação foi aprovada, teste o acesso do aplicativo na próxima segunda-feira aplicável.”*

Para os alunos, o URL de gravação é exibido na página de visão geral do curso da sala de aula virtual.

Após 30 minutos de conclusão de um curso, a frequência do aluno é marcada.

## Perguntas frequentes

+++Quem é um organizador e um apresentador?

Consulte a [documentação](https://support.microsoft.com/en-us/office/roles-in-a-teams-meeting-c16fa7d0-1666-4dde-8686-0a0bfe16e019) da Microfsoft para diferentes funções e recursos que são suportados por Microsoft Teams.

+++

+++Um organizador deve ser um usuário registrado no Learning Manager e nos Microsoft Teams?

Sim, o organizador também deve fazer parte do Learning Manager e do Microsoft Teams. Além disso, o organizador deve fazer parte do mesmo locatário da Microsoft, que está configurado no aplicativo do administrador de integração.

+++

+++Um apresentador deve ser um usuário registrado no Learning Manager e nos Microsoft Teams?

Sim, o apresentador também deve fazer parte do Learning Manager e do Microsoft Teams. O apresentador deve ter uma ID do Azure Ative Diretory (pode ser parte do mesmo locatário que o organizador ou parte de qualquer outro locatário). Além disso, até mesmo usuários anônimos (usuários que fazem logon apenas com o nome de usuário e não fazem parte do Ative Diretory) também podem se tornar apresentadores pelo organizador/apresentadores existentes durante a reunião.

+++

+++Microsoft Teams tem reuniões, webinars e eventos ao vivo. Qual deles faz o suporte do conector do Teams?

No momento, o conector do Teams oferece suporte apenas a reuniões em Microsoft Teams. Para obter mais informações, consulte este [documento](https://docs.microsoft.com/en-us/microsoftteams/quick-start-meetings-live-events).

+++
