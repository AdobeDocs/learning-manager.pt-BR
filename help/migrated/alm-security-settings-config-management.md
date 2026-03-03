---
title: Adobe Learning Manager - Gerenciamento de configurações e definições de segurança
description: Este documento descreve os tipos de conta administrativa do Adobe Learning Manager, as configurações relacionadas à segurança, os padrões seguros recomendados, os recursos da API, a funcionalidade de exportação, os métodos de comparação de configuração, as práticas de publicação e o histórico de versões. Ele fornece orientações detalhadas sobre como as contas privilegiadas operam, suas implicações de segurança e como o gerenciamento de configuração é suportado em toda a plataforma.
jcr-language: en-us
source-git-commit: 579573cbc1baaea2ac8e6ebf17f32c46624ea798
workflow-type: tm+mt
source-wordcount: '1940'
ht-degree: 0%

---


# Introdução

Este guia fornece respostas detalhadas às recomendações de FedRAMP (FRR-RSC-03 a FRR-RSC-08) para Adobe Learning Manager (ALM). Ele descreve as práticas recomendadas de segurança, padrões seguros recomendados e ferramentas para auditoria, exportação e gerenciamento de configurações de contas privilegiadas. O documento foi desenvolvido para administradores e equipes de conformidade para garantir a configuração e o gerenciamento seguros de contas do ALM.

Ele também destaca as áreas em que o ALM atende ou atende parcialmente aos padrões do FedRAMP, com referências a documentação de suporte e recursos disponíveis no Adobe Experience League.

+++Quais configurações relevantes de segurança só podem ser operadas por administradores personalizados ou administradores de integração no Adobe Learning Manager? Quais são suas implicações de segurança?

Dois tipos de conta privilegiada da Adobe Learning Manager: administrador personalizado e administrador de integração. Cada um tem um conjunto definido de configurações relevantes de segurança com implicações documentadas.

**Administrador personalizado — o que ele pode operar**:

* As funções personalizadas são configuradas pelo administrador completo em Administrador do ALM > Usuários > Funções personalizadas. Um administrador personalizado pode receber acesso a uma ou mais destas categorias de permissão: Privilégios da conta (comunicados, gamificação, habilidades, gerenciamento de usuário), Privilégios do recurso (catálogos, relatórios, marcas) e Privilégios do objeto de aprendizado (cursos, certificações, caminhos de aprendizado).
* Escopo é a configuração mais sensível à segurança: uma função personalizada pode ser restrita a grupos de usuários e/ou catálogos específicos. Sem restrição de escopo, uma função personalizada efetivamente tem acesso em toda a plataforma aos recursos concedidos — aproximando-se do espaço ocupado por um administrador total.
* Se uma função personalizada receber acesso de configurações em Privilégios da conta, esse administrador personalizado poderá modificar métodos de logon, configurações de notificação e configurações no nível da conta — um privilégio de alto impacto que só deve ser concedido com justificativa de negócios explícita.

**Administrador de integração — o que ele pode operar**:

* Os administradores de integração gerenciam registros do aplicativo OAuth 2.0 em Administrador de integração > Aplicativos > Registrar. Eles selecionam um dos seis escopos OAuth, que variam do acesso de leitura do aluno ao acesso de leitura/gravação da função de administrador. O escopo de leitura/gravação do administrador concede ao aplicativo registrado os mesmos privilégios que um administrador completo por meio da API.
* Os administradores de integração configuram FTP, SFTP, Salesforce, Workday e outros conectores que importam registros de usuário, atribuições de função e conclusões de curso — e exportam dados da plataforma para sistemas externos.
* Os administradores de integração configuram webhooks que enviam dados de eventos do ALM em tempo real (inscrições, conclusões, alterações de função) para URLs externos. Um ponto de extremidade do webhook comprometido ou configurado incorretamente é um risco de exfiltração de dados.
* Os administradores de integração podem configurar integrações de LTI. Uma vez habilitada, a LTI não pode ser desabilitada.

**Referências**:

* [Funções personalizadas | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)
* [Gerenciar funções personalizadas via CSV | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/configure-role-csv-files)
* [Manual do desenvolvedor de aplicativos | Adobe Learning Manager][https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual]
* [Conectores do Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/connectors)

+++

+++Quais são os padrões seguros recomendados para contas administrativas e privilegiadas de nível superior no Adobe Learning Manager e onde estão configurados?

O Adobe Learning Manager documenta padrões seguros específicos recomendados para a função Administrador e os tipos de conta privilegiada.

* **Padrões de conta de Administrador de Nível Superior (configurados no primeiro provisionamento)**:

* Método de logon para usuários internos: Single Sign-On (SSO) por SAML 2.0: configurado em Administrador do ALM > Configurações > Métodos de logon. Não use o Adobe ID para funcionários ou administradores.
* Verificação em duas etapas (2FA): aplicada a todos os usuários: configurada em Adobe Admin Console > Configurações > Privacidade e segurança > Configurações de autenticação.
* Duração máxima da sessão: 8 horas (ou por política organizacional): configurado em Adobe Admin Console > Configurações > Privacidade e segurança > Configurações avançadas.
* Tempo máximo de inatividade: 30 minutos (ou por política organizacional): mesmo local como acima.
* Exclusão automática de usuário inativo: ativada com um período de retenção definido pela organização (por exemplo, 90 dias de inatividade): administrador do ALM > Configurações > Geral.
* Expiração do perfil de usuário externo: defina em cada perfil externo na criação: Administrador do ALM > Usuários > Externo. Nenhum perfil externo indefinido.
* Restrições de acesso a IP: Restringir a intervalos de IP aprovados onde possível: Admin Console > Configurações > Configurações avançadas.

**Padrões de função de Administrador Personalizado (configurados ao criar cada função)**:

* Escopo OAuth para aplicativos registrados: escopo mínimo necessário. Nunca conceda acesso de leitura/gravação à função Administrador, a menos que seja estritamente necessário.
* Escopo de função personalizada: restringir a grupos de usuários e catálogos específicos. Não crie funções personalizadas com o escopo Todos os usuários e Todos os catálogos, a menos que a função realmente as exija.
* Acesso de configurações em funções personalizadas: não conceda a menos que a função específica o exija, dado o risco de escalação de privilégios.

**Padrões do administrador de integração**:

* Escopo OAuth da API: selecione o escopo mais restritivo que atenda aos requisitos de integração. Não conceda ao administrador acesso de leitura/gravação para aplicativos que precisam apenas do acesso de leitura do aluno.
* Credenciais do conector, credenciais de LTI e URLs de webhook: trate como segredos confidenciais — nunca compartilhe por email ou confirme no controle do código-fonte.

**Referências**:

* [Configurações | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)
* [Autenticação e senhas de usuário seguras | Adobe Admin Console](https://helpx.adobe.com/enterprise/using/authentication-settings.html)
* [Funções personalizadas | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role)

+++

+++O Adobe Learning Manager oferece uma maneira para os administradores compararem as configurações atuais da conta com os padrões seguros recomendados?

O Adobe Learning Manager não tem um painel de comparação dedicado que mostre automaticamente as configurações atuais juntamente com os padrões seguros recomendados.

**Relatório de Função Personalizada: atribuições de função privilegiadas atuais**:

* No ALM, navegue até Administrador > Usuários > Funções personalizadas e clique em Baixar (canto superior direito) para exportar um CSV de todas as funções personalizadas, seus conjuntos de permissões e suas atribuições de escopo.
* Compare essa exportação com os padrões recomendados na Seção 8 de FRR-RSC-02, verificando especificamente se uma função personalizada tem acesso de Configurações, escopo Todos os usuários ou escopo Todos os catálogos sem justificativa documentada.

**API REST ALM: recuperação de configuração programática**:

* O ponto de extremidade GET /account retorna dados de configuração no nível da conta no formato JSON, acessíveis usando o escopo OAuth da função de administrador. Os clientes podem chamar esse endpoint programaticamente e comparar a resposta com uma linha de base derivada dos padrões recomendados em FRR-RSC-02 Seção 8.
* O ponto de extremidade GET /users (com o filtro include=role) retorna atribuições de função atuais para todos os usuários, permitindo a detecção automática de atribuições de função inesperadas.

>[!NOTE]
>
>O Adobe Learning Manager não oferece uma interface de comparação lado a lado nativa. Os clientes que precisam de verificação de conformidade de configuração automatizada devem integrar a API REST do ALM com suas ferramentas existentes.

**Referência**

* [Manual do desenvolvedor de aplicativos | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)

+++

+++Os administradores podem exportar configurações e definições atuais relevantes de segurança do Adobe Learning Manager em um formato legível por computador?

O Adobe Learning Manager oferece suporte à exportação de dados de configuração relevantes de segurança por meio de vários mecanismos. Nenhuma exportação produz um instantâneo completo de todas as configurações de segurança de uma só vez, mas as exportações a seguir cobrem coletivamente todo o escopo dos dados relevantes de segurança.

**API REST ALM: exportação JSON de atribuições de função e configuração de conta atuais**:

* GET /account: retorna configurações no nível da conta em JSON, incluindo dados de configuração de logon ativo e metadados da conta.
* GET /users?include=role: retorna todos os usuários com suas funções atualmente atribuídas em JSON.
* GET /userGroups — retorna todos os grupos de usuários e suas associações, relevantes para a auditoria do escopo da função personalizada.
* Todas as respostas de API são JSON (vnd.api+json). A autenticação usa o OAuth 2.0 com escopo de leitura/gravação da função de administrador.

**Exportação de CSV de Função Personalizada: definições de função com privilégios atuais**:

* O administrador do ALM > Usuários > Funções personalizadas > Baixar exporta um CSV de todas as definições de função personalizadas, suas categorias de permissão e atribuições de escopo.
* Essa exportação pode ser usada como um instantâneo legível por computador da configuração de conta privilegiada atual.
**

**API de trabalhos: dados de usuário e função em massa**:

* A API de trabalhos do ALM oferece suporte à geração sob demanda de relatórios de usuário (incluindo atribuições de função) no formato CSV. Eles podem ser programados e consumidos por ferramentas externas de conformidade ou SIEM.

**Referência**

* [Manual do desenvolvedor de aplicativos | Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual)

+++

+++O Adobe Learning Manager fornece uma API por meio da qual as configurações relevantes de segurança podem ser visualizadas e ajustadas de forma programática?

O Adobe Learning Manager fornece uma API REST v2 completa que permite a visualização programática e o ajuste de configurações relevantes para segurança usando a autenticação OAuth 2.0. Veja a seguir os recursos específicos da API relevantes para as configurações de segurança:

**Autenticação e escopo**:

* Os aplicativos são registrados pelo administrador de integração em Administrador de integração > Aplicativos > Registrar. A ID do cliente OAuth 2.0 e o segredo são emitidos por aplicativo.
* Seis escopos estão disponíveis. Para o gerenciamento de configurações de segurança, é necessário ter acesso de leitura/gravação à função de administrador. Isso concede ao aplicativo o mesmo acesso que um administrador completo por meio da API.
* Os tokens de acesso são obtidos por meio do código de autorização OAuth padrão ou do fluxo de credenciais do cliente. URL base: https://learningmanager.adobe.com/primeapi/v2/

**Gerenciamento de usuários e funções por meio da API**:

* GET /users: recuperar todos os usuários e suas funções atuais
* POST /users: provisionar novos usuários de forma programática
* PATCH /users/{id}: atualizar atributos de usuário incluindo atribuições de função
* DELETE /users/{id}: desabilitar uma conta de usuário
* POST /users/{id}/purge: limpe permanentemente um usuário e todos os registros associados

Recuperação de configuração de conta:

* GET /account: retorna a configuração no nível da conta incluindo dados de configurações da conta no formato JSON, incluindo campos como complianceLabelDefaultID, showComplianceLabel e custom_injections.

+++

+++A Adobe Learning Manager publica suas diretrizes de configuração segura em um formato legível por computador, como OSCAL, JSON ou YAML?

No momento, a Adobe Learning Manager não publica o Guia de configuração segura em um formato legível por computador. As orientações no [FRR-RSC-01](/help/migrated/alm-administrative-lifecycle.md) e [FRR-RSC-02](/help/migrated/alm-secure-administration-guide.md) são publicadas como documentação legível no Adobe Experience League nos formatos HTML e documento para download.

Não há nenhuma definição de componente OSCAL, linha de base YAML ou arquivo de política JSON publicamente disponível que codifique os padrões seguros recomendados para o Adobe Learning Manager.

Os clientes que precisam de comparação automatizada das configurações atuais em relação às linhas de base recomendadas devem usar a [API REST ALM](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual) para recuperar os dados de configuração atuais no formato JSON.

+++

+++O Guia de configuração segura da Adobe Learning Manager está disponível publicamente sem exigir logon ou acesso especial?

**O que está disponível publicamente**:

* [FRR-RSC-01: Guia de Administração Segura](/help/migrated/alm-administrative-lifecycle.md): orientação de ciclo de vida completo para contas administrativas de nível superior.
* [FRR-RSC-02: Implicações e Configurações de Segurança Administrativas](/help/migrated/alm-secure-administration-guide.md): todas as configurações relevantes para a segurança, suas implicações e padrões recomendados.
* FRR-RSC-03-10 (este documento) — Respostas de perguntas e respostas para todas as oito recomendações FedRAMP SHOULD.

+++

+++A Adobe Learning Manager fornece o controle de versões e um histórico de versões que permite às agências rastrear alterações nas configurações relevantes de segurança e nos padrões recomendados ao longo do tempo?

A Adobe Learning Manager mantém um histórico de versões detalhado e disponível publicamente para cada atualização de produto. As alterações relevantes de segurança nas configurações administrativas, recursos de autenticação, endpoints de API e recursos de gerenciamento de funções são documentadas em cada versão.

**Notas de versão do ALM: numerado, histórico de alterações cumulativo**:

* O Adobe publica notas de versão numeradas para cada atualização do Adobe Learning Manager (por exemplo, atualização 100, atualização 99). Eles são publicados no Experience League e documentam todos os novos recursos, alterações nas configurações existentes, adições e remoções de API, alterações de conector e recursos obsoletos.
* Cada nota de versão inclui uma seção dedicada para alterações de API, listando novos pontos de extremidade, campos de resposta modificados e descontinuações, diretamente relevantes para recursos de configuração relevantes de segurança.

**Páginas de novidades: resumos de recursos por versão**:

* Cada versão principal tem uma página dedicada “Novidades” que documenta novos recursos relevantes para a segurança com contexto. Por exemplo, as notas de versão incluem alterações no tratamento de permissões de funções personalizadas, a adição de visibilidade de permissões criadas por CSV para funções personalizadas e alterações de limitação de taxa de API.

**Lista de Descontinuações de API: registro oficial de recursos de API removidos** s:

* O Adobe mantém uma página dedicada de descontinuações de API listando todos os endpoints de API do ALM descontinuados e removidos com a versão de lançamento em que cada descontinuação ocorreu.

**Referências**:

* [Notas de versão do Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/release-notes)
* [Novidades no Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/whats-new-july-2024)
* [Descontinuações de API no Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/api-deprecations-list)

+++

