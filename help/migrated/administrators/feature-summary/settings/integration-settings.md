---
description: Saiba mais sobre como as Configurações de integração conectam o Adobe Learning Manager a soluções de terceiros
jcr-language: en_us
title: Configurações de integração no Adobe Learning Manager
source-git-commit: 03123dcd8d9066cdfcb0fe97e61acb3df625a23e
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 4%

---


# Configurações de integração no Adobe Learning Manager

## Métodos de login

O Adobe Learning Manager fornece vários métodos de logon para garantir acesso seguro e flexível para usuários internos e externos. Os administradores podem configurar esses métodos de logon com base em requisitos organizacionais.

Os métodos de logon disponíveis são:

* ID do Adobe Learning Manager
* Adobe ID
* Logon único

### Usuários internos

A seção Usuários internos permite configurar opções de login especificamente para usuários internos. Os usuários internos podem acessar a conta usando a Adobe ID ou o logon único (SSO).

**Adobe ID:**

* Os usuários internos podem fazer logon usando suas credenciais do Adobe ID.
* Adequado para organizações que já usam serviços da Adobe.

**Logon Único (SSO):**

* Permite o SSO para usuários internos usarem o provedor de identidade (IdP) da organização.
* Compatível com autenticação baseada em SAML 2.0 para experiências de logon simplificadas.

Para permitir logons de SSO para usuários internos, selecione Ativar logon único múltiplo (SSO) para logon e comece a configurar o SSO.

O **[!UICONTROL Campo Ativo do SSO]** no Adobe Learning Manager é usado para mapear configurações de Logon Único (SSO) para atributos ou grupos de usuários específicos. Você pode configurar este campo para ativar várias configurações de SSO para usuários internos com base em sua organização, local ou outros critérios.

### Usuários externos

A seção Usuários externos no Adobe Learning Manager permite gerenciar alunos externos, como parceiros ou agências, que precisam de acesso limitado à conta do Adobe Learning Manager. Esta seção fornece ferramentas para criar perfis de registro, gerenciar grupos de usuários externos e definir configurações específicas para alunos externos.

Os usuários externos podem fazer logon usando o seguinte:

* Adobe ID: usuários externos podem fazer logon usando suas credenciais do Adobe ID.
* Logon único (SSO): usuários externos podem fazer logon por SSO se configurados pelo administrador.
* Adobe Learning Manager ID: usuários externos podem criar um nome de usuário e uma senha do Learning Manager para acessar a plataforma.

**Pontos principais:**

* Você pode ativar um ou mais métodos de logon para usuários externos.
* Se a ID Adobe Learning Manager for selecionada, os usuários externos deverão criar suas próprias credenciais.
* O SSO pode ser configurado para usuários externos com base nas necessidades organizacionais.

### Configuração de SSO no Adobe Learning Manager

A Adobe Learning Manager oferece suporte ao logon único (SSO) para permitir que os usuários autentiquem uma vez e obtenham acesso a vários aplicativos. Os administradores podem configurar o SSO para usuários internos e externos usando provedores baseados em SAML 2.0.

Consulte [Logons de SSO no Adobe Learning Manager](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) para obter mais informações.

>[!NOTE]
>
>* Até 20 configurações de SSO podem ser adicionadas a uma conta.
>* Entre em contato com o suporte da Adobe para obter assistência com provedores de SSO baseados em SAML 2.0.

## Fontes de dados

As fontes de dados permitem que você ou os administradores de integração integrem sistemas externos para importar e sincronizar dados do usuário e de aprendizado. Esse recurso garante o gerenciamento e a sincronização perfeitos de dados com sistemas como HRMS, Salesforce, FTP e outros.

**Exemplos de tipos de fontes de dados**

* **Conectores FTP**: as fontes de dados baseadas em FTP permitem que as organizações carreguem arquivos de dados do usuário diretamente no Adobe Learning Manager por meio de protocolos de transferência de arquivos seguros. Essas conexões são particularmente úteis para importações em lote de informações do usuário, inscrições no curso e outras operações de dados em massa.
* **Integrações de terceiros**: o Adobe Learning Manager oferece suporte à integração com vários sistemas corporativos por meio de conectores pré-criados. Essas integrações podem incluir sistemas de gerenciamento de RH, plataformas de gerenciamento de relacionamento com o cliente e outros sistemas de gerenciamento de aprendizagem.
*** Integração com o Salesforce**: o conector do Salesforce permite a sincronização direta de dados do usuário, informações do curso e registros de aprendizado entre o Salesforce e o Adobe Learning Manager.

Consulte [Conectores no Adobe Learning Manager](/help/migrated/integration-admin/feature-summary/connectors.md) para obter mais informações.

## Contas entre parceiros

Contas entre parceiros no Adobe Learning Manager permitem compartilhar licenças compradas e exibir relatórios entre contas associadas. Esse recurso é útil para organizações que precisam colaborar ou compartilhar recursos entre diferentes contas.

Consulte [Contas entre parceiros](/help/migrated/administrators/feature-summary/peer-account.md) no Adobe Learning Manager para obter mais informações.





