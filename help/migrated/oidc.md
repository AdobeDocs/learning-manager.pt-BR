---
description: Saiba mais sobre o método de login OIDC
jcr-language: en_us
title: Fazer logon no Adobe Learning Manager com o OpenID Connect
source-git-commit: 7c430e3fbb2716455310f2130d73af10ce2e56c7
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---


# Fazer logon no Adobe Learning Manager com OpenID Connect (OIDC)

Saiba como o logon com o OpenID Connect funciona no Adobe Learning Manager para alunos, autores e administradores. Este artigo aborda a experiência, não a implementação.

## Entenda o logon do OpenID Connect

O OpenID Connect (OIDC) é um método de logon comum desenvolvido em padrões da Web. Muitas organizações usam um provedor de identidade (por exemplo, Okta, Google Workspace ou Microsoft Entra ID) para funcionários e parceiros.

Quando sua organização ativa o OIDC para Adobe Learning Manager:

* Você faz logon usando a página de logon usual de sua organização, não uma senha que se aplique apenas à Adobe Learning Manager, a menos que sua organização escolha o contrário.
* Depois de autenticar, a Adobe Learning Manager recebe as informações permitidas por sua organização (como atributos de email e perfil) e abre a experiência certa para você: aluno, autor, administrador ou outras funções compatíveis com sua conta.

O OIDC é uma alternativa a outras opções de logon que sua conta pode oferecer, como Adobe ID ou logon único baseado em SAML (SSO). Seu administrador decide quais métodos estão disponíveis.

## Por que as organizações escolhem o OpenID Connect

As organizações geralmente escolhem o OIDC porque:

* Os usuários veem a mesma experiência de identidade corporativa ou na nuvem que usam para outros aplicativos.
* Políticas de senha, autenticação de vários fatores e ciclo de vida da conta são gerenciados no provedor de identidade, de forma consistente com outros aplicativos corporativos.
* O OIDC segue padrões semelhantes a outros fluxos de entrada modernos da perspectiva do usuário e de TI, sem a troca de documentos mais pesada associada a algumas configurações somente de SAML.

Sua experiência ainda é: acesse o Learning Manager, faça logon no aplicativo desejado pela sua organização e acesse-a no aplicativo.

## O que você vê ao fazer logon

### Abrir o Adobe Learning Manager

Você pode usar:

* O URL principal do Adobe Learning Manager do seu ambiente
* Um domínio personalizado que sua organização configurou, se aplicável
* Um link de uma página de email, convite ou autorregistro
* Um marcador ou link profundo para um curso, página de catálogo ou recurso específico

Se sua conta usa OIDC, iniciar o logon normalmente redireciona seu navegador para o provedor de identidade de sua organização.

### Fazer logon com sua organização

Na página do provedor de identidade, insira suas credenciais e conclua todas as etapas adicionais necessárias à sua organização, como autenticação de vários fatores. Essa etapa acontece fora do próprio formulário de logon da Adobe Learning Manager quando OIDC é o método em uso. Do seu ponto de vista, parece que você está fazendo logon na sua conta empresarial ou de estudante. Talvez você não veja termos técnicos como *OIDC* ou *OAuth* durante esta etapa.

### Voltar ao Adobe Learning Manager

Após um logon bem-sucedido, seu navegador o retornará à Adobe Learning Manager. O produto então:

* Reconhece você usando as informações de email e perfil que seu provedor de identidade compartilha, de acordo com as configurações da sua organização
* Aplica suas permissões no Adobe Learning Manager (aluno, autor, administrador, administrador de integração etc.)
* Abre a área ou o aplicativo apropriado (por exemplo, a experiência do aluno comparada com experiências de administrador ou autor), de acordo com como a Adobe Learning Manager atribui funções para sua conta

Se algo der errado (por exemplo, sua conta não foi provisionada ou sua organização bloqueia o acesso), você pode ver um erro ou não conseguir continuar. Entre em contato com a equipe de TI interna ou com o administrador do Adobe Learning Manager.

## Usar outras opções de entrada com o OpenID Connect

O Adobe Learning Manager pode oferecer suporte a mais de um método de logon em uma conta (várias opções de SSO). Por exemplo:

* Alguns usuários fazem logon com a Adobe ID
* Outras pessoas usam o SAML SSO
* Outros usam OIDC

As opções exibidas dependem de como sua conta está configurada. Ativar o OIDC para sua organização não remove, por si só, outros métodos, a menos que seus administradores alterem essa configuração.

## Recursos e cenários com suporte

Os seguintes comportamentos são compatíveis quando sua organização usa OIDC com Adobe Learning Manager, de acordo com a expectativa de que outros métodos de logon corporativo funcionem.

### Tabela 1. Suporte OIDC em cenários comuns

| Área | O que isso significa para você |
| --- | --- |
| Usuários internos e externos | Funcionários e usuários externos convidados (por exemplo, parceiros) podem usar o OIDC onde o administrador ativá-lo, incluindo os fluxos que começam dos links de autorregistro quando a conta é configurada para isso. |
| Primeiro acesso | Se você for permitido por política, seu primeiro logon OIDC bem-sucedido poderá criar ou vincular seu usuário no Adobe Learning Manager de acordo com as regras da sua organização, semelhante a outras opções de SSO. |
| Perfil e atributos | Informações como email e outros atributos podem ser atualizadas no seu provedor de identidade ao longo do tempo, para que o seu perfil da Adobe Learning Manager permaneça alinhado com o diretório da sua organização no que o seu administrador configura. |
| Links profundos | Os links que apontam para uma página ou um recurso específico no Learning Manager (não apenas a página inicial) são compatíveis. Você pode acessar o conteúdo desejado após o logon quando a configuração da sua organização permitir. |
| Caminho de retorno | Após a autenticação, você pode retornar ao local que estava tentando acessar (por exemplo, o mesmo curso ou URL do catálogo do qual começou), em vez de sempre chegar em uma página inicial genérica. |
| Domínio personalizado | Se sua empresa usa um nome de host personalizado para o Adobe Learning Manager, o logon OIDC também é compatível com esse contexto. |
| Dispositivos móveis | É possível fazer logon em celulares e tablets por meio de navegadores ou experiências compatíveis. |
| Publish para Adobe Learning Manager (Prime) | Os fluxos de trabalho que envolvem a publicação de conteúdo no Learning Manager a partir de ferramentas conectadas permanecem compatíveis quando sua conta usa OIDC, de acordo com a configuração de integração. |
| Logon com base em identificador | Nos casos em que sua conta depende de identificadores estáveis (além do email sozinho) para contas correspondentes, esses fluxos são compatíveis com OIDC de acordo com a configuração do administrador. |

Se um fluxo de trabalho específico não funcionar, a causa pode ser configurações do provedor de identidade, provisionamento de conta ou atribuição de função Adobe Learning Manager. O administrador pode verificar.

## Como funcionam as funções após o logon

O Adobe Learning Manager determina o que você pode fazer a partir das funções e permissões da sua conta, não do protocolo OIDC em si. O OIDC só estabelece quem você é, a contento do provedor de identidade e o que sua organização compartilha com a Adobe Learning Manager.

* Os alunos geralmente veem treinamento, catálogos e planos de aprendizado.
* Os autores podem criar ou selecionar conteúdo.
* Administradores gerenciam usuários, configurações e relatórios.

Se você aterrissar na área errada ou não tiver acesso esperado, peça ao administrador do Adobe Learning Manager para verificar seu perfil e a associação ao grupo.

## Solução de problemas comuns

### Tabela 2. Solução de problemas de logon OIDC

| Problema | O que experimentar |
| --- | --- |
| Redirecionar loop ou página em branco | Limpe os cookies do seu URL do Learning Manager e do seu provedor de identidade, tente com outro navegador ou experimente uma janela privada. Se o problema persistir, entre em contato com o departamento de TI. As políticas corporativas de proxies ou de sessão de provedor de identidade às vezes interferem. |
| “Acesso negado” ou semelhante após o logon do provedor de identidade | Seu provedor de identidade aceitou você, mas a Adobe Learning Manager pode não ter um usuário correspondente ou sua conta pode não ter uma licença ou função. Entre em contato com o administrador do Adobe Learning Manager. |
| Idioma ou detalhes do perfil incorretos | O mapeamento de atributos é controlado pela sua organização. Pergunte ao administrador se os atributos de diretório devem direcionar campos de localidade ou perfil. |
| O deep link abriu a página inicial em vez do recurso | O comportamento do caminho de retorno e do deep-link pode depender de como o link foi compartilhado e da sua sessão. Tente o link novamente após um logon completo ou pergunte ao administrador se o formato do link é compatível com usuários externos. |

## O que os administradores devem saber

Se você configurar o Adobe Learning Manager para sua organização, o OIDC será configurado com o registro do aplicativo do provedor de identidade: identificadores de cliente, pontos de extremidade para autorização, tokens, informações do usuário e o URL de redirecionamento que a Adobe Learning Manager usa para concluir o logon. Esses valores são provenientes da documentação do provedor de identidade. As configurações devem corresponder entre seu provedor de identidade e o Learning Manager para que os usuários vejam um redirecionamento e um retorno suaves.

Os usuários finais não precisam gerenciar esses valores. Eles só precisam do URL correto do Learning Manager (ou domínio personalizado) e, quando aplicável, dos links de convite ou autorregistro da sua equipe.

## Resumo

* O OIDC permite que os usuários façam logon na Adobe Learning Manager por meio do provedor de identidade padrão de sua organização, com um fluxo familiar de redirecionamento e retorno.
* Após o logon, o Adobe Learning Manager usa atributos de email e compartilhados para identificar o usuário e aplicar funções (aluno, autor, administrador etc.).
* Autorregistro, várias opções de SSO, atualizações de atributo, provisionamento de usuário pela primeira vez, links profundos, caminho de retorno, domínios personalizados, dispositivos móveis, Publish para Adobe Learning Manager e correspondência baseada em identificador são compatíveis de acordo com a configuração de sua conta.
* Outros métodos de logon (como Adobe ID ou SAML) permanecem disponíveis quando os administradores os mantêm ativados.
