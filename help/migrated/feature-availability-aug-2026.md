---
description: Saiba quais superfícies do aplicativo são compatíveis com os novos recursos do Adobe Learning Manager na versão de agosto de 2026, incluindo APIs, dispositivos móveis e AEM Widget
jcr-language: en_us
title: Disponibilidade de recursos na versão de agosto de 2026 do Adobe Learning Manager
exl-id: e134937c-630d-4285-9181-2eca114717f6
source-git-commit: bb95f74b775d279e94fad319380d451446256636
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 2%

---


# Disponibilidade de recursos na versão de agosto de 2026 do Adobe Learning Manager

## Finalidade

Os clientes corporativos que criam ou estendem a plataforma por meio de seu próprio front-end (uma implementação “sem periféricos”) perguntam regularmente se um recurso novo ou alterado pode realmente ser usado fora da interface do usuário padrão da Web, por meio da API do aluno, da API do administrador, do widget de AEM ou de outra superfície de integração.

Este documento fornece uma resposta rápida e narrativa para cada recurso incluído nesta versão. Para cada recurso, este documento identifica superfícies de aplicativos compatíveis, disponibilidade de integração, suporte à migração e qualquer comportamento de notificação aplicável.

## Disponibilidade de recursos por recurso

### Construtor de e-mail baseado em componentes

Essa será uma ativação em fase para diferentes contas que se inscrevem após o lançamento do recurso: migrar essas contas do editor de email existente para o novo editor. Uma vez ativado, o cliente não pode usar o antigo editor de e-mail. (Para ativar recursos, entre em contato com CSM/Suporte).

* **Disponível em:** Aplicativo do administrador. Administradores e autores configuram layouts de email e modelos aqui.
* **Não aplicável:** interface do usuário voltada para o aluno, API sem periféricos e Widget de AEM, já que os alunos simplesmente recebem os emails resultantes por meio de seu próprio cliente de email.
* **Notificações:**
  * As notificações por e-mail continuam a ser entregues aos alunos em clientes de e-mail suportados.
  * Nenhum novo comportamento de notificação na plataforma é introduzido por esse recurso.

### Aprendizado externo

* **Disponível em:** Web nativa, API sem periféricos (aluno), Web móvel nativa e no aplicativo do administrador.
* **Ainda não disponível em:** aplicativo móvel nativo.
* **API de Trabalho:** não aplicável.
* **Migração:** ainda sem suporte.
* **Notificações:**
  * As notificações na plataforma estão disponíveis para alunos e gerentes quando as solicitações de aprovação de aprendizado externas são enviadas e quando as solicitações são aprovadas ou rejeitadas.
  * As notificações por email não estão disponíveis atualmente para este fluxo de trabalho.

### Relatório de Usuário Incremental

* **Disponível somente em:** API de trabalho. Fornece uma exportação incremental (delta) de dados do usuário para relatórios.
* **Não aplicável:** interface do usuário, outras superfícies da API e ferramentas de migração.

### Criador de relatórios

* **Disponível em:** Aplicativo do administrador.
* **Ainda não disponível em:** API de Trabalho. Uma exportação baseada em API de trabalho está planejada para uma versão futura.
* **Migração:** não aplicável.
* **Notificações:**
  * Os usuários recebem notificações na plataforma quando os downloads do relatório estão prontos ou quando a geração do relatório falha.
  * As notificações por email não são aplicáveis.

### Pastas de Conteúdo Hierárquico

* **Disponível em:** aplicativo do administrador e aplicativo do autor.
* **Migração:** Suportada.
* **API de Trabalho:** não aplicável. Nenhuma superfície de API dedicada no momento.

>[!NOTE]
>
>Os privilégios de função personalizados se aplicam apenas no nível da pasta raiz/pai, não a todas as pastas na hierarquia.

### Agente de insights

* **Disponível em:** Aplicativo do administrador. Atualmente limitado somente a administradores completos (não funções personalizadas).
* **API do administrador:** não disponível.
* **API/Migração de Trabalho:** Não aplicável.

### Agente de caminhos de aprendizado

* **Disponível em:** Web nativa e a API sem periféricos (aluno).
* **Ainda não disponível em:** Web Móvel Nativo, Aplicativo Móvel Nativo e Widget AEM.
* **API/Migração de Trabalho:** Não aplicável.

### Assistente do AI (aluno)

* **Disponível em:** Web nativa, API sem periféricos (aluno) e Web móvel nativa.
* **Ainda não disponível em:** Aplicativo Móvel Nativo e Widget AEM.
* **API/Migração de Trabalho:** Não aplicável.

>[!NOTE]
>
>Esse recurso deve ser ativado explicitamente para que apareça aos alunos.

### Hub ao vivo

* **Disponível em:** Web nativa, API sem periféricos (aluno), Web móvel nativa e no aplicativo do administrador.
* **API de Trabalho:** não aplicável.
* **Migração:** atualmente não suportada.

### Administradores Personalizados: Leia/Gerencie Outras Funções Personalizadas

* **Disponível em:** Aplicativo do administrador. Permite que os administradores personalizados visualizem e gerenciem outras funções de administrador personalizadas.
* **API/Migração de Trabalho:** Não aplicável. Nenhuma API dedicada para isso ainda.

### Quadro de notas

* **Disponível em:** Web nativa, API sem periféricos (aluno), Web móvel nativa, aplicativo móvel nativo e aplicativo do administrador.
* **Ainda não disponível em:** Widget AEM.
* **Migração:** atualmente não suportada.
* **Notificações:**
  * Nenhuma notificação por email.
  * Nenhuma notificação na plataforma.

### Canais

* **Disponível em:** Web nativa e no aplicativo do administrador. Atualmente na versão beta.
* **Ainda não disponível em:** API sem periféricos (aluno), Web móvel, aplicativo móvel, widget AEM e API do administrador.
* **API/Migração de Trabalho:** Não aplicável.
