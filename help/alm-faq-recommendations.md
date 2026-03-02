---
title: Ciclo de vida da conta administrativa do Adobe Learning Manager
description: Este documento fornece um resumo abrangente dos recursos de gerenciamento de conta de segurança, configuração e conformidade da Adobe Learning Manager (ALM), alinhados às recomendações do FedRAMP.
jcr-language: en-us
source-git-commit: 06051e44c0a6bc8ae60e44272ba088f2f6ff281f
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 0%

---


# Recomendações de segurança do Adobe Learning Manager

## Quais configurações relevantes de segurança só podem ser operadas por administradores personalizados ou administradores de integração no Adobe Learning Manager? Quais são suas implicações de segurança?

Os dois tipos de conta privilegiada da Adobe Learning Manager — administrador personalizado e administrador de integração — têm, cada um, um conjunto definido de configurações relevantes de segurança com implicações documentadas.

### Administrador personalizado: o que eles podem operar:

* As funções personalizadas são configuradas pelo administrador completo em Administrador do ALM > Usuários > Funções personalizadas. Um administrador personalizado pode receber acesso a uma ou mais destas categorias de permissão: Privilégios da conta (comunicados, gamificação, habilidades, gerenciamento de usuário), Privilégios do recurso (catálogos, relatórios, marcas) e Privilégios do objeto de aprendizado (cursos, certificações, caminhos de aprendizado).
* Escopo é a configuração mais sensível à segurança: uma função personalizada pode ser restrita a grupos de usuários e/ou catálogos específicos. Sem restrição de escopo, uma função personalizada efetivamente tem acesso em toda a plataforma aos recursos concedidos — aproximando-se do espaço ocupado por um administrador total.
* Se uma função personalizada receber acesso de configurações em Privilégios da conta, esse administrador personalizado poderá modificar métodos de logon, configurações de notificação e configurações no nível da conta — um privilégio de alto impacto que só deve ser concedido com justificativa de negócios explícita.
* Um administrador personalizado com acesso a Configurações que também tem acesso à entidade Usuários pode atribuir a função de administrador completa a si mesmo, encaminhando efetivamente para o controle administrativo completo.

### Administrador de integração: o que ele pode operar:

* Os administradores de integração gerenciam registros do aplicativo OAuth 2.0 em Administrador de integração > Aplicativos > Registrar. Eles selecionam um dos seis escopos OAuth, que variam do acesso de leitura do aluno ao acesso de leitura/gravação da função de administrador. O escopo de leitura/gravação do administrador concede ao aplicativo registrado os mesmos privilégios que um administrador completo por meio da API.
* Os administradores de integração configuram FTP, SFTP, Salesforce, Workday e outros conectores que importam registros de usuário, atribuições de função e conclusões de curso, e exportam dados da plataforma para sistemas externos.
* Escopo OAuth para aplicativos registrados: escopo mínimo necessário. Nunca conceda acesso de leitura/gravação à função Administrador, a menos que seja estritamente necessário.
* Os administradores de integração configuram webhooks que enviam dados de eventos do ALM em tempo real (inscrições, conclusões, alterações de função) para URLs externos. Um ponto de extremidade do webhook comprometido ou configurado incorretamente é um risco de exfiltração de dados.
* Os administradores de integração podem configurar integrações de LTI. Uma vez habilitada, a LTI não pode ser desabilitada. As credenciais de LTI expostas permitem acesso não autorizado ao conteúdo do curso a partir de plataformas LMS externas.


## Quais são os padrões seguros recomendados para contas administrativas e privilegiadas de nível superior no Adobe Learning Manager e onde estão configurados?

### Padrões de conta de administrador de nível superior (configurados no primeiro provisionamento):

* Método de logon para usuários internos: Single Sign-On (SSO) por SAML 2.0: configurado em Administrador do ALM > Configurações > Métodos de logon. Não use o Adobe ID para funcionários ou administradores.
* Verificação em duas etapas (2FA): aplicada a todos os usuários: configurada em Adobe Admin Console > Configurações > Privacidade e segurança > Configurações de autenticação.
* Duração máxima da sessão: 8 horas (ou por política organizacional): configurado em Adobe Admin Console > Configurações > Privacidade e segurança > Configurações avançadas.
* Tempo máximo de inatividade: 30 minutos (ou por política organizacional): mesmo local como acima.
* Exclusão automática de usuário inativo: ativada com um período de retenção definido pela organização (por exemplo, 90 dias de inatividade): administrador do ALM > Configurações > Geral.
* Expiração do perfil de usuário externo: defina em cada perfil externo na criação: administrador do ALM > Usuários > Externo. Nenhum perfil externo indefinido.
* Restrições de acesso a IP: Restrinja a intervalos de IP aprovados onde possível - Admin Console > Configurações > Configurações avançadas.

### Padrões da função Administrador Personalizado (configurados ao criar cada função):

* Escopo OAuth para aplicativos registrados: escopo mínimo necessário. Nunca conceda acesso de leitura/gravação à função Administrador, a menos que seja estritamente necessário.
* Escopo de função personalizada: restringir a grupos de usuários e catálogos específicos. Não crie funções personalizadas com o escopo Todos os usuários e Todos os catálogos, a menos que a função realmente as exija.
* Acesso de configurações em funções personalizadas: não conceda a menos que a função específica o exija, dado o risco de escalação de privilégios.

### Padrões do administrador de integração:

* Escopo OAuth da API: selecione o escopo mais restritivo que atenda aos requisitos de integração. Não conceda ao administrador acesso de leitura/gravação para aplicativos que precisam apenas do acesso de leitura do aluno.
* Credenciais do conector, credenciais de LTI e URLs de webhook: trate como segredos confidenciais — nunca compartilhe por email ou confirme no controle do código-fonte.

## O Adobe Learning Manager oferece uma maneira para os administradores compararem as configurações atuais da conta com os padrões seguros recomendados?

O Adobe Learning Manager não tem um painel de comparação dedicado que mostre automaticamente as configurações atuais juntamente com os padrões seguros recomendados. No entanto, três recursos de plataforma permitem que os administradores auditem e comparem configurações atuais de modo manual ou programático.

### Relatório de função personalizada - atribuições de função privilegiada atuais:

No ALM, navegue até Administrador > Usuários > Funções personalizadas e clique em Baixar (canto superior direito) para exportar um CSV de todas as funções personalizadas, seus conjuntos de permissões e suas atribuições de escopo.

### API REST ALM - recuperação programática de configuração:

* O ponto de extremidade GET /account retorna dados de configuração no nível da conta no formato JSON, acessíveis usando o escopo OAuth da função de administrador. Os clientes podem chamar esse ponto de extremidade programaticamente.
* O ponto de extremidade GET /users (com o filtro include=role) retorna atribuições de função atuais para todos os usuários, permitindo a detecção automática de atribuições de função inesperadas. Use a API Trabalhos para exportações de usuários em massa.

## Os administradores podem exportar configurações e definições atuais relevantes de segurança do Adobe Learning Manager em um formato legível por computador?

O Adobe Learning Manager oferece suporte à exportação de dados de configuração relevantes de segurança por meio de vários mecanismos. Nenhuma exportação produz um instantâneo completo de todas as configurações de segurança de uma só vez, mas as exportações a seguir cobrem coletivamente todo o escopo dos dados relevantes de segurança.

### Registro de auditoria do Admin Console — exportação de CSV de todas as alterações de autenticação e função:

* No Adobe Admin Console, navegue até **Insights > Registros > Registro de auditoria**, aplique filtros conforme necessário e clique em **Exportar CSV**
* O CSV exportado registra cada ação administrativa, incluindo: 2alterações de imposição de FA, alterações de limite de sessão, atribuições e remoções de função de administrador, exclusões de usuários e alterações de direito do produto, tudo com carimbos de data e hora e identidade do ator.
* Os dados são mantidos por 90 dias. os usuários do Global Admin Console podem exportar logs em todas as organizações.

### API REST ALM — Exportação JSON de atribuições de função e configuração de conta atuais:

* `GET /account` — retorna as configurações no nível da conta em JSON, incluindo dados de configuração de logon ativo e metadados da conta.
* `GET /users?include=role` — retorna todos os usuários com suas funções atualmente atribuídas em JSON.
* `GET /userGroups` — retorna todos os grupos de usuários e suas associações, relevantes para a auditoria do escopo de função personalizada.
* Todas as respostas de API são JSON (`vnd.api+json`). A autenticação usa o OAuth 2.0 com escopo de leitura/gravação da função de administrador.

### Exportação de CSV de função personalizada — definições de função privilegiada atuais:

* O administrador do ALM > Usuários > Funções personalizadas > Baixar exporta um CSV de todas as definições de função personalizadas, suas categorias de permissão e atribuições de escopo.
* Essa exportação pode ser usada como um instantâneo legível por computador da configuração de conta privilegiada atual.

### API de trabalhos — dados de usuário e função em massa:

* A API de trabalhos do ALM oferece suporte à geração sob demanda de relatórios de usuário (incluindo atribuições de função) no formato CSV. Eles podem ser programados e consumidos por ferramentas externas de conformidade ou SIEM.

Consulte [Adobe Learning Manager- Manual do desenvolvedor de aplicativos](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/developer-manual) para obter mais informações.

## O Adobe Learning Manager fornece uma API por meio da qual as configurações relevantes de segurança podem ser visualizadas e ajustadas de forma programática?

O Adobe Learning Manager fornece uma API REST v2 completa que permite a visualização programática e o ajuste de configurações relevantes para segurança usando a autenticação OAuth 2.0. Veja a seguir os recursos específicos da API relevantes para as configurações de segurança:

### Autenticação e escopo

* Os aplicativos são registrados pelo Administrador de Integração em **Administrador de Integração > Aplicativos > Registrar**. A ID do cliente OAuth 2.0 e o segredo são emitidos por aplicativo.
* Seis escopos estão disponíveis. Para o gerenciamento de configurações de segurança, é necessário o acesso de leitura/gravação da **função de administrador**. Isso concede ao aplicativo o mesmo acesso que um administrador completo por meio da API.
* Os tokens de acesso são obtidos por meio do código de autorização OAuth padrão ou do fluxo de credenciais do cliente.\
  **URL Base:**\
  `https://learningmanager.adobe.com/primeapi/v2/`

### Gerenciamento de usuários e funções por meio da API

* `GET /users` — recuperar todos os usuários e suas funções atuais
* `POST /users` — provisionar novos usuários de forma programática
* `PATCH /users/{id}` — atualizar atributos de usuário incluindo atribuições de função
* `DELETE /users/{id}` — desabilitar uma conta de usuário
* `POST /users/{id}/purge` — limpar permanentemente um usuário e todos os registros associados

### Recuperação de Configuração de Conta

* `GET /account` — retorna a configuração no nível da conta incluindo dados de configurações da conta no formato JSON, incluindo campos como:
   * `complianceLabelDefaultID`
   * `showComplianceLabel`
   * `custom_injections`

### API de gerenciamento de usuários do Adobe (camada de Admin Console)

* A API de gerenciamento de usuários do Adobe (UMAPI) fornece acesso programático às operações de Admin Console:
   * Provisionamento de usuários
   * Atribuição de direitos de produto
   * Atribuição de funções de Administrador do Sistema no nível da organização
* A UMAPI é separada da API REST do ALM e opera no nível da organização Adobe. Use-o para automatizar atribuições de função de Admin Console e provisionamento de usuários.

## A Adobe Learning Manager publica suas diretrizes de configuração segura — os padrões recomendados — em um formato legível por computador, como OSCAL, JSON ou YAML?

No momento, a Adobe Learning Manager não publica o Guia de configuração segura em um formato legível por computador.

## O Guia de configuração segura da Adobe Learning Manager está disponível publicamente sem exigir logon ou acesso especial?

Sim O Guia de configuração segura da Adobe Learning Manager está disponível publicamente no Adobe Experience League. Nenhuma conta, logon ou licença é necessária para acessá-la.

O que está disponível publicamente:

* FRR-RSC-01: Guia de administração segura: orientação do ciclo de vida completo para contas administrativas de nível superior.
* FRR-RSC-02: Implicações e Configurações de Segurança Administrativas — todas as configurações relevantes de segurança, suas implicações e padrões recomendados.

## A Adobe Learning Manager fornece o controle de versões e um histórico de versões que permite às agências rastrear alterações nas configurações relevantes de segurança e nos padrões recomendados ao longo do tempo?

A Adobe Learning Manager mantém um histórico de versões detalhado e disponível publicamente para cada atualização de produto. As alterações relevantes de segurança nas configurações administrativas, recursos de autenticação, endpoints de API e recursos de gerenciamento de funções são documentadas em cada versão.

### Notas de versão do ALM — histórico de alterações cumulativo e numerado

* O Adobe publica notas de versão numeradas para cada atualização do Adobe Learning Manager (por exemplo, *Atualização 100*, *Atualização 99*).
* Eles foram publicados no **Experience League** e no documento:
   * Novos recursos
   * Alterações nas configurações existentes
   * Adições e remoções de API
   * Alterações no conector
   * Recursos obsoletos
* Cada nota de versão inclui uma seção dedicada para **alterações de API**, listando:
   * Novos pontos de extremidade
   * Campos de resposta modificados
   * Descontinuações
   * Eles são diretamente relevantes para os recursos de configuração relevantes para a segurança.

### Páginas “Novidades” — Resumos de recursos por versão

* Cada versão principal tem uma página dedicada **”Novidades”** que documenta novos recursos relevantes para a segurança com contexto.
* Exemplos de atualizações documentadas relacionadas à segurança incluem:
   * Alterações na manipulação de permissão de função personalizada
   * Adição de visibilidade de permissões criadas por CSV para funções personalizadas
   * Alterações de limitação de taxa de API

### Lista de obsolescências de API — Registro oficial de recursos de API removidos

* O Adobe mantém uma página **Descontinuações de API** dedicada listando todos os endpoints de API do ALM substituídos e removidos, incluindo a versão de lançamento em que cada descontinuação ocorreu.
* Exemplos de descontinuações relevantes para a segurança incluem:
   * Alterações no comportamento de classificação e substituição do ponto de extremidade `GET /users`
   * Notificação, requisitos de filtro de data de relatório

