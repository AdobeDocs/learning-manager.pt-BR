---
title: Ciclo de vida da conta administrativa do Adobe Learning Manager
description: Este documento fornece orientação abrangente sobre o gerenciamento seguro de contas administrativas de nível superior no Adobe Learning Manager (ALM) para atender à conformidade com o FedRAMP e às práticas recomendadas de segurança.
jcr-language: en-us
source-git-commit: db3ed4dc44da75b418e923999bdf3776bf81b11f
workflow-type: tm+mt
source-wordcount: '2122'
ht-degree: 0%

---


# Tipos de conta administrativa no Adobe Learning Manager

## Mapeamento de funções do ALM

No Adobe Learning Manager, a conta administrativa de nível superior é a função Administrador. Esta é a função a que se refere sempre que este guia usa o termo FedRAMP &#39;conta administrativa de nível superior&#39;. Os administradores personalizados e os administradores de integração são tratados como contas privilegiadas (com escopo).

A tabela abaixo mapeia os níveis de conta do FedRAMP para as funções específicas usadas no Adobe Learning Manager:

| Termo FedRAMP | Nome da Função do ALM | Descrição |
|--------------------------------------|----------------------------|-------------|
| Conta administrativa de nível superior | Administrador | Função de maior privilégio no ALM. Controle total sobre usuários, funções, conteúdo de aprendizado, relatórios, integrações e todas as configurações do sistema. Mapeia diretamente para a definição de conta administrativa de nível superior do FedRAMP. |
| Conta privilegiada (com escopo) | Administrador personalizado | Um subconjunto definido de permissões de Administrador com escopo para funções específicas (por exemplo, relatórios, gerenciamento de catálogo). Não tem controle total no nível de conta. |
| Conta privilegiada (integração) | Administrador de integração | Gerencia integrações e acesso baseado em API entre o ALM e sistemas externos. Privilégios elevados limitados somente ao gerenciamento de integração. |


O Adobe Learning Manager usa um modelo de controle de acesso baseado em função (RBAC) para gerenciar o acesso administrativo. As funções administrativas são atribuídas somente por administradores autorizados.

Consulte [Funções personalizadas no Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role) para obter mais informações

## Tipos de identidade e autenticação recomendada

O Adobe Admin Console oferece suporte a três tipos de identidade para contas de administrador. A escolha do tipo de identidade tem implicações diretas de segurança:

| Tipo de identidade | Descrição | Recomendação de segurança |
|---------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Adobe ID (ID pessoal) | Tipo padrão; gerenciado por Adobe. Qualquer um pode criar um. | NÃO RECOMENDADO para administradores. A organização não tem controle sobre esse tipo de conta. |
| Enterprise ID | Conta de propriedade da organização gerenciada por um Administrador do Sistema Admin Console. | Aceitável se o Federated ID/SSO não estiver disponível. Aplicar 2FA. |
| Federated ID (SSO) | Propriedade da organização; integrado ao SSO SAML 2.0. A organização controla inteiramente a autenticação. | RECOMENDADO. Autentica por meio do IdP da organização; oferece suporte à imposição de MFA no nível do provedor de identidade. |

Consulte o seguinte para obter mais informações:

* [Tipos de identidade](https://helpx.adobe.com/enterprise/using/admin-console.html)
* [Autenticação e senhas de usuário seguras](https://helpx.adobe.com/enterprise/using/authentication-settings.html)

## Atribuição de funções e controle de acesso

O acesso às contas administrativas no Adobe Learning Manager é controlado por meio da [atribuição de função](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) explícita por um administrador existente. As principais características do acesso administrativo seguro incluem:

* As funções administrativas são atribuídas somente por administradores autorizados.
* O acesso é baseado em função e com escopo de acordo com as permissões atribuídas.
* As organizações são responsáveis por limitar o acesso administrativo a usuários com necessidades comerciais legítimas.

A Adobe recomenda que os clientes revisem periodicamente o acesso administrativo para garantir a adesão ao princípio do menor privilégio.

## Aplicar a Autenticação Multifator (MFA)

A Adobe recomenda que os administradores apliquem a verificação em duas etapas (2FA) em toda a organização. O MFA se aplica a usuários de Enterprise ID e Adobe ID. Os usuários do Federated ID devem ter o MFA aplicado no provedor de identidade de sua organização.

Para aplicar 2FA no Adobe Admin Console:

1. Faça logon no Adobe Admin Console.
2. Navegue até Configurações > Privacidade e segurança > Configurações de autenticação.
3. Ative a Verificação em duas etapas e selecione a opção Impor para evitar que os usuários a desativem.
4. Opcionalmente, defina restrições de acesso baseadas em IP e configurações avançadas de sessão (Tempo máximo de sessão ativa / Tempo máximo de inatividade).

>[!IMPORTANT]
>
>A Adobe recomenda aplicar 2FA e não deixá-lo opcional para os usuários. 2FA pode levar até 24 horas para ser aplicado. Para usuários do Federated ID, aplique o MFA em seu provedor de identidade.

Consulte [Autenticação de usuário segura para obter mais informações](https://helpx.adobe.com/enterprise/using/authentication-settings.html).


## Fazer logon como administrador

[Administradores](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-admin) do ALM entram diretamente na plataforma do ALM usando credenciais organizacionais gerenciadas por meio do Admin Console.

### Atribuir uma função de administrador

Na plataforma do ALM, os administradores configuram o acesso administrativo criando e gerenciando funções, atribuindo permissões aos usuários e definindo o escopo de permissão com base nas responsabilidades operacionais.

Para atribuir a função Administrador no ALM:

1. Faça logon no Adobe Learning Manager como um administrador existente.
2. Navegue até Usuários > Interno.
3. Pesquise ou selecione o usuário de destino.
4. Selecione Ações > Atribuir função > Criar administrador.

As funções administrativas personalizadas permitem que os clientes deleguem tarefas administrativas enquanto mantêm o controle centralizado sobre os privilégios no nível da conta. Os administradores personalizados podem ter o escopo definido para catálogos ou grupos de usuários específicos.

Consulte [Adicionar usuários e grupos de usuários](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) para obter mais informações.

## Configurar métodos de logon e SSO

Os administradores do ALM controlam os métodos de logon disponíveis para todos os usuários por meio de Configurações > Métodos de logon, uma configuração crítica relevante para a segurança:

* **Usuários internos**: defina o modo de logon como Adobe ID ou logon único (SSO). O SSO via SAML 2.0 é altamente recomendado.
* **Usuários externos**: defina o modo de logon como Adobe ID, SSO ou Learning Manager ID. Alinhe o método selecionado com a política de segurança da sua organização.

O Adobe recomenda o uso do SSO Federated ID / SAML 2.0 como o método de logon para todos os usuários internos. Isso garante que a autenticação seja totalmente controlada pelo provedor de identidade da sua organização, permitindo a aplicação centralizada de MFA e o cancelamento imediato da conta após a saída do usuário.

Consulte [Configurações](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/settings) para obter mais informações.

## Padrões seguros recomendados no provisionamento

Quando uma conta do ALM é provisionada pela primeira vez, o Adobe recomenda verificar as seguintes configurações padrão antes de conceder a qualquer usuário administrativo acesso operacional:

| Configuração | Padrão seguro recomendado | Onde configurar |
|------------------------------|------------------------------------------------------------------|-------------------------------------------------|
| Método de logon — usuários internos | Logon único (SSO)/Federated ID | ALM > Configurações > Métodos de logon |
| Verificação em duas etapas (2FA) | Imposto (não opcional para nenhum usuário) | Admin Console > Configurações > Privacidade e segurança |
| Tempo máximo de sessão ativa | 8 horas ou por política da organização | Admin Console > Configurações > Configurações avançadas |
| Tempo máximo de inatividade | 30 minutos ou por política da organização | Admin Console > Configurações > Configurações avançadas |
| Escopo da função de administrador | Menor privilégio; usar funções de administrador personalizadas sempre que possível | ALM > Usuários > Funções personalizadas |
| Expiração do usuário externo | Definir uma data de expiração em cada perfil de usuário externo | ALM > Usuários > Externo |

### Lista de verificação de configuração inicial para Novos administradores

Ao provisionar uma nova conta de administrador de nível superior, conclua o seguinte antes de conceder acesso operacional:

* Confirme se o tipo de identidade é Enterprise ID ou Federated ID — não Adobe ID Pessoal.
* Aplique 2FA no nível de Admin Console (Configurações > Configurações de autenticação).
* Configure o SSO/Federated ID se ainda não estiver ativado.
* Defina o Tempo máximo de sessão ativa e o Tempo máximo de inatividade em Admin Console > Configurações > Configurações avançadas.
* Limitar escopo da função de administrador — atribua apenas as permissões necessárias para as responsabilidades do usuário.
* Verifique se a conta do administrador está vinculada a um endereço de email organizacional controlado pela equipe de TI.
* Documente a conta no registro de acesso privilegiado da sua organização.

## Funcionamento das contas administrativas

### Tarefas administrativas diárias

As contas administrativas são usadas para executar tarefas operacionais diárias, incluindo:

* **Gerenciamento do ciclo de vida do usuário**: criação de usuários, atualização de perfis e alterações de função.
* **Gerenciamento de conteúdo de aprendizado**: gerenciar cursos, programas de aprendizado, certificações e catálogos.
* **Relatórios e análises**: gerar e revisar relatórios sobre o progresso do aluno e o uso da plataforma.
* **Integrações e configuração do sistema**: gerenciamento de conectores, acesso baseado em API e configurações no nível do sistema.

Espera-se que os administradores sigam as políticas de controle de acesso interno e de gerenciamento de alterações de sua organização ao executar ações administrativas.

Consulte [Perguntas frequentes para administradores do Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/faq/frequently-asked-questions-for-administrators)


### Hierarquia de funções e delegação

O Adobe Admin Console usa uma estrutura administrativa hierárquica. Os administradores de sistema podem delegar responsabilidades a funções de privilégio inferior para reduzir a superfície de ataque da conta de administrador de nível superior:

* Administrador de produto: gerencia o acesso a produtos de Adobe específicos (por exemplo, Adobe Learning Manager).
* Administrador de perfil de produto: gerencia a associação do usuário em perfis de produto específicos.
* Administrador de grupo de usuários: gerencia a associação de grupo de usuários.
* Administrador personalizado do ALM: administrador com escopo no ALM com permissões configuráveis por catálogo e grupo de usuários.

### Práticas de governança contínuas

As práticas a seguir devem ser seguidas por organizações que operam contas de administrador do ALM de forma contínua:

* **Revisão periódica de acesso**: faça auditoria regularmente da lista de administradores de sistema no Admin Console (Usuários > Administradores) e administradores do ALM (Usuários > Internos) para garantir que apenas a equipe autorizada e atual tenha essas funções.
* **Monitoramento de log de auditoria**: o Log de Auditoria do Admin Console registra todas as alterações feitas pelos administradores. Os administradores do sistema têm visibilidade total. Revise o registro regularmente em busca de alterações não autorizadas.
* **Acesso permanente mínimo**: evite usar contas de administrador de nível superior para tarefas de rotina. Reserve acesso total de administrador para tarefas que o exijam especificamente.
* **Segurança de sessão**: configure o tempo máximo de sessão ativa e inativa em Admin Console > Configurações > Configurações avançadas para limitar a exposição de sessões autônomas.

Consulte [Visão geral do Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html) para obter mais informações.

### Gerenciar contas de usuário sob controle do administrador

Os administradores do ALM gerenciam contas de usuários internas e externas. As operações relevantes de segurança incluem:

* Exclusão automática do usuário: em Configurações, os administradores podem configurar usuários internos inativos para que sejam excluídos automaticamente após um número especificado de dias, reduzindo o risco de conta inativa.
* Expiração do usuário externo: os administradores definem uma data de expiração ao criar perfis de usuário externo. As contas expiradas são movidas automaticamente para um estado inativo.
* Exclusão de usuário: os administradores podem excluir usuários manualmente por meio de Usuários > Internos > Ações > Excluir usuário.
* Remoção de usuários: após a exclusão, os administradores podem remover permanentemente os registros de usuários para cumprir as políticas de retenção de dados e impedir o acesso não autorizado a dados obsoletos de usuários.

Consulte o seguinte para obter mais informações:

* [Adicionar usuários e grupos de usuários](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups)
* [Remover usuários](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/purge-users)

## Desativação das contas administrativas

O acesso administrativo deve ser removido quando não for mais necessário. As contas administrativas de desmantelamento podem incluir:

* Revogando funções administrativas dos usuários.
* Redução de privilégios quando o acesso administrativo completo não é mais necessário.
* Remoção de usuários do sistema quando apropriado.

A revisão e a remoção regulares do acesso administrativo desnecessário ajudam a manter o acesso menos privilegiado.

### Removendo direitos de administrador do sistema (Admin Console)

Quando um administrador do sistema deixa a organização ou altera funções, os privilégios devem ser revogados imediatamente:

1. Faça logon no Adobe Admin Console como administrador de sistema.
2. Navegue até Usuários > Administradores.
3. Selecione o administrador a ser removido.
4. Clique no ícone Mais opções (...) > Editar administrador e remova a função de administrador de sistema — OU selecione Remover usuário para remover o usuário totalmente da organização.
5. Caso o administrador tenha outras funções (administrador de produto, administrador de suporte etc.), revogue-as também.

>[!IMPORTANT]
>
>Se o administrador de partida for o Proprietário do Contrato da organização, a função Proprietário do Contrato deverá ser transferida para outra pessoa antes que ela possa ser removida. Entre em contato com o suporte de Adobe, se necessário.

Consulte o seguinte para obter mais informações:

* [Criar, atualizar ou remover contas de usuário no Admin Console](https://helpx.adobe.com/enterprise/using/manage-users-individually.html)
* [Como sair da conta da organização](https://helpx.adobe.com/enterprise/using/leave-organization.html)

### Remover a função de administrador do ALM

Para revogar o acesso de administrador do ALM sem excluir a conta do usuário (por exemplo, quando a pessoa permanece como aluno):

1. Faça logon no Adobe Learning Manager como administrador.
2. Navegue até Usuários > Interno.
3. Pesquise e selecione o usuário.
4. Selecione Ações > Remover função > Remover administrador.

O usuário reverte para a função do aluno. Seu histórico de aprendizado e as inscrições no curso são preservados.

Consulte [Adicionar usuários e grupos de usuários](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/user-management/add-users-user-groups) para obter mais informações.

### Excluir e remover usuários

Quando um usuário sai totalmente da organização e sua conta deve ser removida da plataforma:

* Exclua o usuário: Usuários > Internos > selecione usuário > Ações > Excluir usuário. Isso desabilita a conta e remove o acesso ativo.
* Remover o usuário: após a exclusão, acesse Usuários > Limpeza de usuário, selecione o mês de exclusão, selecione o usuário e escolha Ações > Remover usuário. A limpeza remove permanentemente todos os registros de usuário.

Consulte [Remover usuários](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/purge-users) para obter mais informações.


## Segurança e responsabilidade partilhada

A Adobe Learning Manager opera sob um modelo de responsabilidade compartilhada:

* O Adobe é responsável por proteger a plataforma e a infraestrutura subjacentes do ALM.
* Os clientes são responsáveis por gerenciar o acesso administrativo, as atribuições de função e as atividades do ciclo de vida do usuário em sua conta do ALM.

Informações adicionais sobre práticas de segurança da Adobe Learning Manager estão disponíveis em [Visão geral da segurança da Adobe Learning Manager (PDF)](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Manutenção do documento

Este documento pode ser atualizado periodicamente para refletir alterações na funcionalidade do Adobe Learning Manager ou nas práticas administrativas recomendadas. A versão e a data da última atualização são mantidas nos metadados do documento e no pacote de autorização do FedRAMP. Os clientes devem consultar a versão disponível publicamente no Adobe Experience League para garantir que estejam usando as diretrizes mais recentes.

## Cobertura aprimorada dos recursos de segurança

### SCG-ENH-CMP

O Adobe mantém processos documentados de gerenciamento de ciclo de vida, propriedade e inventário de componentes para garantir a conformidade e a configuração controladas em todos os componentes do sistema.

### SCG-ENH-API

O Adobe aplica controles de segurança de API padronizados, incluindo autenticação, autorização e monitoramento, com suporte de controle documentado e salvaguardas de plataforma.

### SCG-ENH-MRG

O Adobe aplica processos formais de gerenciamento de alterações e fusão, incluindo controles de revisão e aprovação, para manter a integridade do sistema e reduzir o risco de implantação.

### SCG-ENH-VRH

O Adobe segue um processo definido de gerenciamento e correção de vulnerabilidades que abrange identificação, priorização, rastreamento e resolução em tempo hábil.
