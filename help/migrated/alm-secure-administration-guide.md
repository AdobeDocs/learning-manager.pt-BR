---
title: Adobe Learning Manager - guia seguro de administração
description: Este guia descreve as configurações de segurança, funções e práticas recomendadas para gerenciar a segurança administrativa e o controle de acesso no Adobe Learning Manager para garantir a conformidade e a segurança.
jcr-language: en-us
exl-id: 67dd9334-9718-4b2a-841e-5d8bd5c42714
source-git-commit: 5682c45a4e5789a3eede53faf7cb257cd9685759
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---

# Configurações administrativas de segurança e implicações de segurança

## Funções administrativas com impacto na segurança

O Adobe Learning Manager usa um modelo de controle de acesso baseado em função (RBAC). A tabela a seguir mapeia as camadas da conta FedRAMP para as funções do ALM referenciadas neste documento:

| Termo FedRAMP | Função do ALM | Relevância de segurança |
|-------------|---------|------------------|
| Conta administrativa de nível superior | Administrador | Controle total em nível de conta. Acesso exclusivo a todas as configurações relevantes de segurança descritas neste documento. Essa é a função mencionada em todo este guia quando o termo “conta administrativa de nível superior” é usado. |
| Conta privilegiada (com escopo) | Administrador personalizado | Acesso administrativo delegado com escopo para funções, grupos de usuários ou catálogos específicos. Não é possível acessar as configurações de segurança no nível da conta, a menos que explicitamente concedido. |
| Conta privilegiada (integração) | Administrador de integração | Gerencia integrações, registros de API e configurações de conector. Privilégios elevados no escopo do gerenciamento de integração. Não é possível modificar outras configurações de segurança no nível de conta. |

>[!NOTE]
>
>Somente os usuários explicitamente atribuídos a essas funções podem modificar configurações administrativas ou relevantes para a segurança. As configurações documentadas nas Seções 3 a 7 são acessíveis exclusivamente para a função Administrador, a menos que estabelecido de outra forma.

## Configurações de logon e autenticação

As configurações de logon e autenticação controlam como todos os usuários — incluindo administradores — acessam a plataforma ALM. Essas configurações são definidas exclusivamente pela função de administrador e têm um impacto direto e significativo na postura de segurança de toda a conta.

### Configuração do método de logon

**Local:** Administrador do ALM > Configurações > Métodos de Logon

O administrador controla o método de autenticação usado para todos os usuários internos e externos. As opções incluem:

- **Adobe ID:** os usuários são autenticados por meio de suas contas de Adobe pessoais. Gerenciado pelo Adobe, não pela organização.
- **Logon Único (SSO) via SAML 2.0:** os usuários são autenticados por meio do provedor de identidade (IdP) da organização. A organização controla totalmente a autenticação, o MFA e a política de sessão.
- **Learning Manager ID:** Disponível somente para usuários externos. Os usuários criam um nome de usuário e uma senha específicos da plataforma.
- **Várias configurações de SSO:** até 20 configurações de SSO podem ser adicionadas para dar suporte a diferentes grupos de usuários, locais ou divisões organizacionais

| Método de logon | Implicação de segurança | Recomendação |
|-------------|---------------------|----------------|
| **Adobe ID** | A organização não tem controle sobre a política de senha, MFA ou recuperação de conta. Uma conta de Adobe pessoal comprometida concede acesso à plataforma ALM. | **NÃO RECOMENDADO** para usuários administrativos ou internos. Use somente quando o SSO estiver indisponível. |
| **SSO (SAML 2.0 / Federated ID)** | A autenticação é totalmente controlada pelo IdP da organização. MFA, tempos limite de sessão e políticas de acesso condicional são aplicados no nível de IdP. Revogação imediata na partida do usuário. | **RECOMENDADO** para todos os usuários e administradores internos. Fornece o nível mais alto de controle organizacional. |
| **ID do Learning Manager** | Os usuários gerenciam senhas por conta própria fora da infraestrutura de identidade da organização. Não é possível impor o MFA por meio do ALM. A força da senha depende do comportamento do usuário. | Aceitável somente para usuários externos. Inadequado para funcionários ou administradores. |

>[!CAUTION]
>
>Se o método de logon for definido como Adobe ID para usuários internos, a organização perderá a capacidade de aplicar a autenticação de vários fatores, controlar a complexidade da senha ou revogar imediatamente o acesso quando um usuário sair. Isso aumenta significativamente o risco de acesso não autorizado.

Consulte [Funções personalizadas](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role) para obter mais informações.

### Autenticação multifator (MFA)

**Local:** Adobe Admin Console > Configurações > Privacidade e segurança > Configurações de autenticação

A imposição de MFA para usuários do **Adobe ID** e do **Enterprise ID** está configurada pelo **Administrador do Sistema** no Adobe Admin Console, não no próprio aplicativo ALM.  Para usuários de **Federated ID / SSO**, o MFA é imposto no provedor de identidade da organização.

- **2FA imposto:** os usuários não podem desabilitar a verificação em duas etapas. Oferece proteção sólida contra roubo de credenciais e phishing.
- **2FA opcional:** os usuários escolhem se a verificação em duas etapas deve ser habilitada. Postura de segurança significativamente mais fraca.
- **MFA não configurado:** somente as senhas protegem o acesso. Risco elevado, em especial para as contas administrativas.

>[!IMPORTANT]
>
>As contas administrativas sem assistência macrofinanceira obrigatória correm um risco significativamente mais elevado de acesso não autorizado. Uma credencial de administrador comprometida sem MFA concede controle total da conta, incluindo a capacidade de modificar todas as configurações de segurança.

### Tempo Limite de Vida da Sessão e Tempo Limite de Ociosidade

**Local:** Adobe Admin Console > Configurações > Privacidade e segurança > Configurações avançadas

O **Administrador do Sistema** configura o tempo de vida máximo da sessão ativa e o tempo limite de sessão ociosa para a organização. Essas configurações aplicam-se a todos os usuários, incluindo administradores.

- **Vida Máxima da Sessão:** força a reautenticação após um período definido, independentemente da atividade. Limita a janela de oportunidade se uma sessão for comprometida.
- **Tempo Máximo de Inatividade:** encerra as sessões que ficaram inativas por um período definido. Protege contra sessões autenticadas autônomas em dispositivos compartilhados ou desbloqueados.

## Definições de Atribuição de Função e Escopo do Privilégio

As configurações de atribuição de função e escopo de privilégio determinam quem tem acesso administrativo no ALM e o que podem fazer. Essas estão entre as configurações de segurança de maior impacto na plataforma. Somente a função Administrador pode criar, atribuir, modificar ou revogar funções administrativas.

### Atribuição de Função Administrativa

**Local:** Administrador do ALM > Usuários > Interno > Ações > Atribuir Função/Remover Função

O **Administrador** pode conceder ou revogar as seguintes funções:

- **Administrador:** acesso completo em nível de conta
- **Autor:** acesso de criação de conteúdo
- **Administrador personalizado:** acesso administrativo com escopo (consulte a Seção 4.2)
- **Administrador de Integração:** acesso à integração e à API (consulte a Seção 7)

| Configuração / Ação | Implicação de segurança | Prática recomendada |
|---|---|---|
| **Concedendo função de Administrador** | Controle total da conta. Um usuário com essa função pode modificar todas as configurações neste documento, incluindo a reconfiguração da autenticação e a revogação do acesso de outros administradores. | Atribua apenas a um número mínimo de usuários com uma necessidade corporativa verificada. Manter uma lista documentada de todos os titulares da função de administrador. |
| **Falha ao revogar funções na partida** | Os usuários que partem mantêm o acesso às funções administrativas. Risco de acesso não autorizado, exfiltração de dados ou sabotagem. | Remova funções imediatamente quando as responsabilidades administrativas ou empregatícias de um usuário forem alteradas. Realizar revisões periódicas de acesso. |
| **Atribuindo funções amplas em excesso** | O amplo acesso administrativo aumenta o impacto potencial de uma conta comprometida e reduz a responsabilidade por ações administrativas. | Aplique o princípio do menor privilégio. Prefira funções com escopo (por exemplo, administrador personalizado) quando possível. |

### Configuração de Função Administrativa Personalizada

**Local:** Administrador do ALM > Usuários > Funções personalizadas > Criar função

Aplique o princípio do **privilégio mínimo**. Use funções de **Administrador Personalizado** para delegar funções específicas (consulte a Seção 4.2).

O **Administrador** pode criar funções personalizadas que concedem um subconjunto definido de permissões administrativas. Funções personalizadas podem ter escopo definido para grupos de usuários, catálogos ou conjuntos de recursos específicos, limitando o alcance do acesso administrativo delegado.

**As categorias de permissão disponíveis incluem:**

- **Privilégios de conta:** acesso a configurações de todo o sistema, como comunicados, gamificação, habilidades e gerenciamento de usuários.
- **Privilégios de recurso (principais):** acesso a catálogos, relatórios e marcas.
- **Privilégios de recursos (objetos de aprendizado):** acesso a cursos, certificações, programações de aprendizado e ajudas de tarefa.
- **Escopo:** restringe a função a grupos de usuários e/ou catálogos específicos.

| Decisão de configuração | Implicação de segurança | Prática recomendada |
|---|---|---|
| **Criando uma função personalizada muito ampla** | Uma função personalizada com privilégios excessivos fornece pouco benefício de segurança em relação à função de administrador completa e aumenta o raio de explosão de uma conta comprometida. | Defina o escopo das funções personalizadas de acordo com o conjunto mínimo de permissões necessárias para a função específica. Preferir funções com escopo de catálogo e de grupo de usuários. |
| **Concedendo acesso de configurações a um administrador personalizado** | Os administradores personalizados com acesso a Configurações podem modificar métodos de logon, configurações de notificação e outras configurações no nível da conta. | Conceda às Configurações acesso a funções personalizadas somente quando explicitamente necessário. Audite quais funções personalizadas têm esse privilégio regularmente. |
| **Não auditando atribuições de função personalizadas** | Funções personalizadas não documentadas ou não revisadas podem se acumular ao longo do tempo, levando a deslizamento de privilégios. | Baixe periodicamente o Relatório de Função Personalizada (**Usuários > Funções Personalizadas > Baixar**) e revise todas as atribuições de função personalizada ativas. |

## Configurações de Gerenciamento de Acesso e Provisionamento de Usuários

As configurações de provisionamento de usuários controlam como os usuários são adicionados à plataforma, por quanto tempo eles permanecem ativos e quando seus dados são removidos. Essas configurações são definidas exclusivamente pela função Administrador e têm implicações diretas de segurança para a exposição de dados e o controle de acesso.

| Configuração | Localização | Implicação de segurança | Padrão recomendado |
|---|---|---|---|
| **Exclusão automática de usuário inativo** | Administrador do ALM > Configurações > Geral | Sem a exclusão automática, as contas inativas se acumulam. Contas inativas são um alvo comum de acesso não autorizado, pois podem não ser monitoradas. | Ativar. Defina um período de retenção alinhado com a política organizacional (por exemplo, 90 dias de inatividade). |
| **Expiração do perfil de usuário externo** | Administrador do ALM > Usuários > Externo > Adicionar perfil | Perfis de usuários externos sem data de expiração permanecem acessíveis indefinidamente. Os parceiros ou contratados que não precisam mais de acesso mantêm um ponto de entrada ativo. | Defina uma data de expiração em cada perfil de usuário externo no momento da criação. |
| **Controles de link de autorregistro** | Administrador do ALM > Usuários > Interno > Adicionar > Autorregistro | Um link de autorregistro permite que qualquer usuário com o URL crie uma conta de aluno. Se não for gerenciado, isso pode fazer com que usuários não autorizados ou inesperados obtenham acesso à plataforma. | Gere links de autorregistro somente quando necessário. Desative ou revogue links não utilizados imediatamente. |
| **Pausa/retomada do perfil externo** | Administrador do ALM > Usuários > Externo > Ações > Pausar | Pausar um perfil externo impede que novos usuários se registrem, mas não afeta os que já estão registrados. Falhar ao pausar perfis externos inativos pode permitir registros não intencionais. | Pausar perfis externos quando o registro não for mais necessário. Excluir perfis que estão permanentemente inativos. |
| **Exclusão e limpeza de usuários** | Administrador do ALM > Usuários > Interno > Ações > Excluir / Limpeza do usuário > Limpar | Os usuários excluídos são desativados, mas seus dados são mantidos. Remover permanentemente remove todos os dados do usuário. A falha ao remover os usuários removidos pode reter registros de aprendizado confidenciais e PII além do período de retenção necessário. | Remover registros de usuários de acordo com as políticas de privacidade e retenção de dados da empresa. A limpeza é irreversível. |

>[!IMPORTANT]
>
>A limpeza é permanente e irreversível. Todos os registros de aprendizado, dados de inscrição e informações do usuário são excluídos. Se um usuário removido for referenciado em configurações de conector, esses conectores serão desabilitados. Confirme a seleção cuidadosamente antes de executar uma remoção.

## Configurações de Relatórios e Acesso a Dados

As configurações de relatório e acesso a dados determinam quais usuários podem exibir, gerar e exportar dados da plataforma. A configuração incorreta dessas configurações pode resultar na exposição de informações pessoais, organizacionais ou relacionadas à conformidade confidenciais.

| Configuração | Localização | Implicação de segurança | Padrão recomendado |
|---|---|---|---|
| **Concedendo acesso de relatório a funções personalizadas** | Administrador do ALM > Usuários > Funções personalizadas > Privilégios do recurso > Relatórios | Os relatórios podem conter informações de identificação pessoal (PII), dados de conclusão do curso, pontuações de avaliação e progresso do aluno. O acesso aos recursos de emissão de relatórios deve ser limitado aos usuários com necessidades comerciais verificadas. | Conceda acesso ao relatório somente para funções com uma necessidade específica e documentada. Use o acesso somente leitura onde o acesso de gravação não é necessário. |
| **Controle Total vs. Escopo do relatório Somente Leitura** | Administrador do ALM > Usuários > Funções personalizadas > Relatório de resumo da conta | O Controle total no Relatório de resumo da conta concede ao administrador personalizado a visibilidade de todos os grupos de usuários e catálogos, independentemente do escopo de sua função. Isso pode expor dados fora do escopo pretendido de uma função de administrador com escopo. | Conceda Controle Total sobre o Relatório de Resumo da Conta somente para funções que realmente exijam visibilidade de relatórios em toda a organização. |
| **Acesso à xAPI e ao relatório por email** | Administrador do ALM > Usuários > Funções personalizadas | Os relatórios xAPI e os relatórios de e-mail estão disponíveis somente para a função de administrador completa. Esses relatórios podem conter dados comportamentais e de comunicação detalhados. O acesso é restrito por design. | Não tente delegar acesso a relatórios de xAPI ou email por meio de funções personalizadas. Eles são apenas para administradores conforme o projeto. |
| **Dados de usuário exportados** | Administrador do ALM > Usuários > Interno > Exportar dados do usuário | A função Exportar dados do usuário gera um arquivo para download que contém todos os registros internos do usuário. Esses dados devem ser tratados de acordo com as políticas organizacionais de segurança e privacidade. | Limitar a capacidade de exportação ao pessoal autorizado. Trate os dados exportados como confidenciais. Não o armazene nem transmita para fora dos sistemas aprovados. |

## Configurações de Integração e Acesso à API

As configurações de integração e acesso à API controlam como os sistemas externos se conectam ao Adobe Learning Manager. Essas configurações estendem o acesso além da interface do usuário do ALM e, se configuradas incorretamente, podem expor dados e funcionalidade da plataforma a sistemas não autorizados.  As configurações de integração são gerenciadas pela função Administrador de Integração. A função de administrador completa mantém a capacidade de revisar, aprovar e revogar aplicativos registrados.

| Configuração | Localização | Implicação de segurança | Padrão recomendado |
|---|---|---|---|
| **Registro de aplicativo de API** | Administrador de integração > Aplicativos > Registrar | Registrar um aplicativo cria credenciais OAuth 2.0 (ID do cliente e segredo) que podem ser usadas para acessar dados e funções do ALM de forma programática. Escopos OAuth muito amplos (por exemplo, leitura/gravação da função de administrador) concedem acesso administrativo completo à API. | Conceda os escopos OAuth mínimos necessários. Revisar e revogar periodicamente registros de aplicativos não utilizados ou antigos. Trate as credenciais do cliente como segredos confidenciais. |
| **Escopo do aplicativo OAuth** | Administrador de integração > Aplicativos > Registrar > Escopos | Os escopos OAuth disponíveis variam do acesso de leitura do aluno ao acesso de leitura/gravação do administrador. A leitura/gravação da função de administrador permite que um aplicativo modifique qualquer dado que um administrador possa modificar, incluindo funções de usuário e configurações de segurança. | Use o escopo OAuth mais restritivo que atenda aos requisitos de integração. Nunca conceda acesso de leitura/gravação à função Administrador, a menos que seja estritamente necessário. |
| **Configuração do conector (FTP, Salesforce, HRIS etc.)** | Administrador de integração > Conectores | Os conectores permitem a importação e a exportação automatizadas de dados do usuário, habilidades e conclusões de cursos. Conectores configurados incorretamente podem importar dados de usuário incorretos, atribuir funções não intencionais ou exportar dados confidenciais para destinos não autorizados. | Revise todas as configurações de conectores ativos periodicamente. Verifique se as fontes de dados e os destinos estão autorizados. Desabilite conectores que não estão mais em uso. |
| **Configuração do webhook** | Administrador de integração > Webhooks | Os webhooks enviam dados de eventos do ALM em tempo real (inscrições, conclusões, alterações de usuário) para um URL externo especificado. Um ponto de extremidade do webhook mal configurado ou comprometido pode resultar em exfiltração de dados ou exposição de eventos sensíveis do aluno. | Registre apenas URLs de webhook verificados e aprovados pela organização. Revise as configurações ativas do webhook regularmente. Remova imediatamente webhooks inativos ou não reconhecidos. |
| **Configuração de integração de LTI** | Administrador de integração > Integrações de LTI | A integração de LTI permite que o ALM atue como um provedor ou consumidor de LTI, permitindo que plataformas LMS externas acessem os cursos do ALM. Uma vez habilitada, a LTI não pode ser desabilitada. As credenciais de LTI expostas podem permitir acesso não autorizado ao conteúdo do curso. | Habilite a LTI somente quando existir um requisito de integração verificado. Trate as credenciais de LTI como confidenciais. Compartilhe credenciais somente com administradores autorizados do LMS. |

## Responsabilidades de Configuração Administrativa e Responsabilidade Compartilhada

As configurações administrativas no Adobe Learning Manager são configuráveis pelos clientes e fazem parte dos controles de segurança gerenciados pelo cliente no modelo de responsabilidade compartilhada da Adobe.

| Responsabilidades do Adobe | Responsabilidades do cliente |
|---|---|
| Operação segura da plataforma do ALM e da infraestrutura subjacente. | Configuração de todas as funções e permissões administrativas. |
| Aplicação do modelo de controle de acesso baseado em função (RBAC). | Selecionando e aplicando métodos de login e MFA apropriados. |

Informações adicionais sobre as práticas de segurança da Adobe Learning Manager estão disponíveis em:

**Referência:** [Visão Geral da Segurança da Adobe Learning Manager (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Manutenção do documento

Este documento pode ser atualizado periodicamente para refletir alterações na funcionalidade da Adobe Learning Manager ou nas orientações de segurança. A versão e a data da última atualização são mantidas nos metadados do documento e no pacote de autorização do FedRAMP. Os clientes devem consultar a versão disponível publicamente no Adobe Experience League para garantir que estejam usando as diretrizes mais recentes.
