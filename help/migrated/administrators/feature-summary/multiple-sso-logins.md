---
description: O Adobe Learning Manager oferece suporte a vários métodos de logon por meio de configurações de SSO múltiplo para usuários internos e externos.
title: Logons de SSO Múltiplo
contentowner: saghosh
source-git-commit: d59e748472c77527c22b286aea5412f776f6441b
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 39%

---


# Logons de SSO Múltiplo {#multiple-sso-logins}

Um administrador pode configurar vários métodos de logon para usuários internos e externos. O Adobe Learning Manager oferece suporte a logons de SSO múltiplo que ajudarão os administradores a configurar o método de logon com base em suas necessidades e casos de uso.

A intenção é permitir que os administradores configurem diferentes SSOs para diferentes grupos de usuários com base em sua localização, organização etc.

Até 20 configurações de SSO podem ser adicionadas a uma conta. Elas podem ser usadas para configurar o SSO para usuários internos e externos.

>[!NOTE]
>
>Ao ativar o SSO Múltiplo, você pode escolher valores ou grupos de usuários no perfil de autorregistro. Ao escolher um valor, um grupo de usuários com zero usuários é criado. Esse grupo de usuários não tem nenhum usuário. Quando o próximo CSV for importado, esse grupo de usuários será removido.

## Ativar SSO múltiplo

Para ativar SSO múltiplo, selecione **Configurações** > **Métodos de logon**.

Na página de configuração, marque a caixa de seleção &#39;Ativar logon único múltiplo (SSO)&#39; para usuários internos ou externos.

Quando o SSO Múltiplo está ativado, o método de logon selecionado para &#39;Método de logon padrão&#39; se torna o tipo de logon padrão para grupos de usuários/perfis que não estão vinculados a nenhuma configuração de SSO. O logon padrão pode ser Adobe ID, SSO ou ALM ID (usuários externos).

Para configurar um SSO, siga as etapas abaixo:

1. Clique em Configuração de logon único (SSO).
1. Clique em Adicionar nova configuração de SSO.
1. Na caixa de diálogo Configuração de SSO, adicione o seguinte:

   * Insira o nome do SSO.
   * Selecione o tipo de SSO- IDP iniciado ou SP iniciado.

      * Se você selecionou IDP iniciado, insira o URL do IDP. Esse será o URL que será o identificador exclusivo do seu aplicativo e as informações fornecidas pelo provedor de serviços de IDP. Este é o URL para o qual todos os usuários do Adobe Learning Manager serão redirecionados após o logon.
      * Carregue o XML de metadados de IDP do seu provedor de IDP. Esse arquivo contém informações sobre o IdP que permite que o Adobe Learning Manager aceite asserções SAML dele
      * Se você selecionou SP iniciado, insira a ID da entidade. A ID da entidade é um URL fornecido pelo provedor de serviços (SP).
      * Digite o URL de login do SP. Essa URL é usada pelos usuários para fazer logon no aplicativo.

1. A configuração de SSO é adicionada à lista.

## Configurar SSO para usuários internos

### Usuários de um CSV

Siga as etapas abaixo:

1. Importe o CSV que contém os campos ativos e seus valores.
1. Clique em Configurações > Métodos de logon.
1. Ative a caixa de seleção Ativar Logon Único Múltiplo (SSO) para logon.
1. Mapeie as configurações de SSO para os valores do campo ativo.
1. Salve as configurações. Importe o CSV novamente.

### Usuário único

Siga as etapas abaixo:

1. Clique em Configurações > Métodos de logon.
1. Ative a caixa de seleção Ativar Logon Único Múltiplo (SSO) para logon.
1. Selecione um campo ativo para um SSO.
1. Vincule as configurações de SSO aos valores do campo.
1. Salve as configurações. Adicione um único usuário e atribua um valor para o campo ativo.

### Usuários autorregistrados

Siga as etapas abaixo:

1. Clique em Configurações > Métodos de logon.
1. Ative a caixa de seleção Ativar Logon Único Múltiplo (SSO) para logon.
1. Vincule as configurações de SSO aos valores do campo.
1. Salve as configurações. Adicione um único usuário e atribua um valor para o campo ativo.
1. Adicione um perfil de autorregistro.
1. Selecione um valor para o campo do SSO configurado.

Depois de salvar as configurações do perfil, o URL copiado redireciona os usuários para o SSO vinculado ao valor escolhido para o perfil.

### Configurar SSO para usuários externos

Siga as etapas abaixo:

1. Crie um perfil externo.
1. Clique em Configurações > Métodos de logon.
1. Ative a caixa de seleção Ativar Logon Único Múltiplo (SSO) para logon.
1. Vincule a configuração de SSO ao perfil externo criado.
1. Salve as configurações.

Depois de salvar as configurações do perfil, o URL do perfil externo copiado redirecionará os usuários para o SSO vinculado ao perfil.

## Perguntas frequentes

+++ Quem pode ativar vários SSOs para usuários?

O administrador e o administrador personalizado podem ativar vários SSOs.
+++

+++Posso usar um campo ativo de valor único existente ou novo?

Sim, você pode usar um campo ativo de valor único existente ou novo para configurar vários SSOs.
+++

+++Se houver campos desativados em um CSV, a configuração de vários SSOs falhará?

Não, isso não afetará a configuração dos SSOs. Os usuários serão redirecionados para um SSO já configurado.
+++

+++Um administrador pode adicionar novos valores ao campo ativo na página ao configurar o SSO Múltiplo?

Sim, um administrador pode adicionar novos valores aos campos ativos.
+++

+++Posso desativar ou excluir campos vinculados ao SSO?

Sim, você pode desativar ou excluir campos vinculados ao SSO até desvincular os campos da página de configuração de SSO.
+++
