---
description: Explica como o Experience Builder pode publicar páginas de aprendizado e catálogos públicos para visitantes anônimos, incluindo recursos principais, widgets compatíveis, pré-requisitos (Training Data Access Connector), limitações e orientação para configuração, escalabilidade e migração da página inicial herdada não conectada.
jcr-language: en_us
title: Configurar e gerenciar páginas não conectadas no Experience Builder
exl-id: e4685cab-08ca-4b6b-93f4-a9eecf382dc4
source-git-commit: ef6f7a9acd27b7fb4c08fe9a8b366d628d199050
workflow-type: tm+mt
source-wordcount: '6051'
ht-degree: 1%

---


# Introdução

A experiência não conectada no Experience Builder permite que as organizações exibam o conteúdo de aprendizado e as páginas do portal para todos os visitantes, incluindo aqueles que não fizeram logon. Esse recurso foi desenvolvido para atrair, informar e envolver alunos potenciais, oferecendo uma visualização suave e com marca de suas ofertas de treinamento antes de exigir que eles façam logon ou se inscrevam.

Esse recurso permite criar e personalizar páginas voltadas para o público usando a mesma interface de arrastar e soltar amigável encontrada no Experience Builder padrão. Você pode exibir catálogos, categorias, caminhos e conteúdo estático avançado do curso, incluindo imagens, texto, HTML e iframes incorporados, para qualquer pessoa que visitar seu portal. Isso facilita destacar seus programas de aprendizado, promover novos cursos e fornecer informações essenciais a um público mais amplo.

Os visitantes podem navegar no catálogo, visualizar detalhes sobre cursos e instâncias e utilizar a pesquisa global para explorar as oportunidades de treinamento disponíveis. No entanto, ações que exigem a identidade de um usuário, como se inscrever em um curso, acessar recursos personalizados (como Calendário, Conformidade, Quadro de classificação ou Aprendizado social) ou realizar treinamento exigirão que o visitante faça logon. Essa abordagem garante que informações confidenciais e personalizadas permaneçam seguras, ao mesmo tempo em que permite uma experiência de visualização abrangente.

Os administradores têm a capacidade de configurar quais páginas e widgets ficam visíveis para usuários que não estão conectados, garantindo que apenas o conteúdo adequado seja exibido. As páginas podem ser configuradas para serem acessíveis a usuários conectados e não conectados ou exclusivamente para um desses grupos. O Experience Builder oferece um modo de visualização, permitindo que você veja exatamente como as páginas serão exibidas aos visitantes antes que sejam publicadas.

Para ativar esse recurso, o administrador de integração do ALM deve ativar o Conector de Acesso a Dados de Treinamento. Esse conector garante que os metadados do curso estejam acessíveis publicamente.

A identidade visual e a localização são totalmente compatíveis, permitindo que você personalize títulos de página, favicons e configurações de idioma para alinhar com a identidade da sua organização e atender às necessidades do seu público. Como parte da transição para essa experiência aprimorada, o recurso de página inicial herdada para usuários não conectados será descontinuado. Portanto, todo conteúdo público novo deve ser criado usando o Experience Builder.

## Finalidade do recurso

A experiência não conectada no Experience Builder permite que as organizações exibam publicamente seu conteúdo de aprendizado e páginas do portal para qualquer pessoa, sem exigir que os usuários façam logon. Isso ajuda a atrair, informar e envolver alunos potenciais, fornecendo uma visualização do treinamento e dos recursos disponíveis antes que a inscrição ou a autenticação seja necessária.

## Casos de uso reais em experiência não conectada

- **Marketing e extensão**: as organizações podem promover seus programas de treinamento para públicos externos, como clientes potenciais, parceiros ou candidatos a emprego, tornando catálogos de cursos e detalhes do programa acessíveis publicamente.
- **Exploração de pré-inscrição**: os alunos podem procurar cursos disponíveis, visualizar visões gerais e explorar categorias antes de decidir se inscrever ou fazer logon, ajudando-os a tomar decisões de inscrição informadas.
- **Portais de treinamento corporativo**: as empresas podem fornecer um portal público para informações de conformidade ou integração, permitindo que novos contratados ou prestadores de serviço vejam qual treinamento está disponível antes de receberem credenciais.
- **Páginas de aterrissagem de evento ou campanha**: as organizações que executam campanhas de aprendizado ou eventos podem criar páginas públicas dedicadas para destacar cursos, agendas ou recursos em destaque, aumentando a visibilidade e o envolvimento.
- **SEO e capacidade de descoberta**: ao tornar públicas páginas e catálogos selecionados, as organizações melhoram a visibilidade de seus mecanismos de pesquisa, facilitando para as pessoas descobrirem suas ofertas de aprendizado online.

## Principais conceitos de experiência não conectada

A experiência não conectada do Experience Builder permite exibir publicamente conteúdo de aprendizado e páginas do portal, permitindo que os visitantes naveguem sem fazer logon.

- **Criar páginas e menus públicos**: você configura páginas e um único menu que todos podem acessar, independentemente do status de logon.
- **Adicionar apenas widgets com suporte**: você inclui widgets que não precisam de contexto de usuário (categorias, cursos e caminhos de aprendizado, caixa de conteúdo, HTML, iframe), enquanto o sistema oculta widgets específicos do usuário.
- **Configurar comportamento de página adaptável**: você decide se uma página é exibida para usuários conectados e não conectados, e o sistema adapta widgets visíveis e conteúdo com base no estado de logon.
- **Visualize as duas experiências**: use opções de visualização para ver como as páginas são exibidas para usuários conectados e não conectados, com diferenças na visibilidade e no conteúdo do widget.
- **Habilitar pesquisa global**: os visitantes pesquisam cursos e conteúdo, mas só obtêm recursos de pesquisa básicos sem integração avançada com IA.
- **Permitir que os visitantes pesquisem o catálogo e as visões gerais do curso**: os visitantes exploram páginas do catálogo, detalhes do curso e instâncias, mas devem fazer logon para se inscrever ou acessar recursos personalizados.
- **Personalizar identidade visual e localização**: defina favicons e configurações de idioma para atender às necessidades de identidade visual e acessibilidade da sua organização.
- **Habilitar o Conector de Acesso a Dados de Treinamento**: ative este conector para exportar metadados do curso para exibição pública, mantendo atualizadas as páginas não conectadas.
- **Tratar alto tráfego com infraestrutura compartilhada**: o sistema gerencia grandes volumes de visitantes anônimos usando recursos compartilhados e limitação de taxa.
- **Otimizar para SEO**: a plataforma prepara páginas públicas para indexação do mecanismo de pesquisa, facilitando a localização do seu conteúdo de aprendizado.

## Pré-requisitos para experiência não conectada

- Você deve ativar o Conector de acesso a dados de treinamento no administrador de integração antes de usar a experiência não conectada.
- O conector exporta os metadados do curso para um repositório público, que mantém as páginas não conectadas atualizadas.

### Inicialização do conector TDA

O conector TDA (Training Data Access, acesso a dados de treinamento) é um pré-requisito crítico para ativar o novo recurso criador de experiências não conectado no ALM. Esse conector facilita a exportação de metadados de treinamento, permitindo que seu portal exiba as informações do curso para os usuários que não estão conectados.

- **Ativação do conector**: você deve habilitar o conector TDA no painel do administrador de integração. Esta etapa desbloqueia a funcionalidade do criador de experiências não conectado e torna visíveis as opções de interface relevantes na interface do administrador.
- **Exportação de metadados**: depois de ativado, o conector exporta metadados de treinamento essenciais (como nome do curso, descrição, visão geral, classificação, duração e habilidades) do ALM para um repositório público. Esses dados são usados para preencher páginas e widgets que não estão conectados.
- **Agendamento e sincronização**: o processo de exportação pode ser agendado (por exemplo, diariamente) para garantir que seu portal reflita as atualizações mais recentes do curso. As alterações feitas no ALM aparecerão em suas páginas não conectadas após o próximo ciclo de exportação, sujeitas ao armazenamento em cache e à frequência de exportação.
- **Disponibilidade de recursos**: os recursos do Experience Builder não conectados, incluindo criação de menus, suporte a widgets e visibilidade de catálogo, só são acessíveis depois que o conector TDA é inicializado. Se o conector não estiver ativado, o Experience Builder permanecerá limitado a cenários de usuário conectado.
- **Migração e suporte**: para contas que estão migrando de recursos de home page não conectados, inicializar o conector TDA é a primeira etapa para a migração. Isso garante que você possa aproveitar a flexibilidade e os recursos aprimorados do novo criador de experiências.

## O que os visitantes podem fazer sem fazer logon

Em um site não conectado do Experience Builder, os visitantes podem navegar pelo catálogo de treinamento abrindo a página do catálogo de catálogos públicos. Eles podem usar filtros como catálogo, produto, função, tipo, habilidades e tags, dependendo de como você configurou o site. Os visitantes também podem pesquisar treinamentos usando a barra de pesquisa global no cabeçalho (se ativada) e exibir os resultados da pesquisa diretamente na página do catálogo.

Os visitantes podem exibir detalhes do treinamento abrindo páginas de visão geral para cursos, programações de aprendizado e certificações. Essas páginas exibem os principais metadados, incluindo título, descrição, autor, duração, formato, tags e habilidades.

Além disso, os visitantes podem explorar conteúdo estático e promocional. Eles podem ler blocos de texto e conteúdo avançado, exibir banners e blocos de imagens e interagir com iframes incorporados, como microsites externos, vídeos ou ferramentas.

Se um visitante clicar em Inscrever-se ou tentar iniciar o treinamento, o sistema solicitará que faça logon ou se inscreva. Após o login bem-sucedido, o visitante é redirecionado para a página apropriada, seja ela a página inicial, uma página personalizada ou o treinamento específico selecionado.

## O que não está disponível sem efetuar login

Em um site não conectado do Experience Builder, os visitantes não podem acessar recursos ou conteúdo que exigem autenticação do usuário. Eles não podem se inscrever em treinamentos, iniciar ou consumir cursos ou acessar widgets personalizados, como Meu aprendizado, Calendário, Conformidade, Quadro de classificação ou Aprendizado social. Esses widgets dependem de dados específicos do usuário e só ficam disponíveis após o login.

Os visitantes também não podem executar ações como se inscrever em um curso ou acessar qualquer conteúdo que exija acompanhamento do progresso ou do contexto do usuário. A tentativa de se inscrever ou iniciar um treinamento solicita que o visitante faça logon ou se inscreva antes de continuar.

## Widgets compatíveis em modo não conectado

No modo não conectado, somente os widgets que não exigem dados específicos do usuário são compatíveis. São eles:

- O widget Categorias, que exibe as categorias de treinamento disponíveis.
- Widget Cursos e caminhos, que mostra cursos e caminhos de aprendizado do catálogo público. 1
- Caixa Conteúdo, para adicionar texto estático, imagens ou conteúdo promocional.
- widget HTML, para incorporar o conteúdo de HTML personalizado.
- Widget Iframe, para exibir sites, vídeos ou ferramentas externas na página.
- Os widgets que exigem contexto de usuário, como Meu aprendizado, Calendário, Conformidade, Quadro de classificação e Aprendizado social, não estão disponíveis no modo não conectado.

Os widgets que exigem contexto de usuário, como Meu aprendizado, Calendário, Conformidade, Quadro de classificação e Aprendizado social, não estão disponíveis no modo não conectado

## Páginas e menus na experiência não conectada

- Somente um menu não conectado é suportado, visível para todos os visitantes sem autenticação.
- As páginas podem ser adicionadas a menus conectados e não conectados; se uma página estiver em ambos, ela adapta seus widgets e conteúdo com base no estado de logon do usuário.
- Menus não conectados não têm direcionamento de público ou personalização. Todos veem o mesmo conjunto de páginas.
- Os widgets não compatíveis com o modo não conectado são ocultados automaticamente; o layout da página se ajusta para preencher as lacunas.
- O gerenciamento de menus e páginas (adição, visualização, exclusão) é semelhante ao modo conectado, mas com adaptações para restrições não conectadas.

## Comportamento de pesquisa e catálogo

No modo não conectado, os usuários podem acessar a página do catálogo e usar a pesquisa para procurar cursos e programações de aprendizado disponíveis. A página do catálogo exibe todos os cursos públicos, juntamente com os filtros e a funcionalidade de pesquisa, seguindo as mesmas configurações de conta que no modo conectado. Quando um usuário pesquisa, os resultados aparecem na página do catálogo e os usuários podem visualizar as páginas de visão geral do curso e da instância sem fazer logon. No entanto, ações como inscrição exigem logon.

Se um usuário tentar se inscrever, o sistema exigirá que ele faça logon primeiro. A pesquisa por usuários não conectados é mais simples do que a pesquisa por usuários conectados e não inclui recursos avançados, como a integração do Assistente do AI.

## Implementação técnica

### Configuração do conector de acesso a dados de treinamento

Você deve ativar o conector de acesso a dados de treinamento no painel do administrador de integração antes de usar o recurso criador de experiências não conectado. Esse conector exporta metadados de treinamento do ALM para um repositório público, tornando-o acessível por meio de APIs para páginas não conectadas. A configuração do conector é um pré-requisito para ativar o recurso e garante que seu portal exiba informações de treinamento atualizadas.

Exportação e sincronização de metadados\
O conector exporta os principais campos de metadados, como nome do curso, visão geral, descrição, classificação, duração e habilidades. Você pode agendar exportações (por exemplo, diariamente) para manter seu portal sincronizado com o ALM. Nem todos os campos de metadados podem ser incluídos; consulte a equipe de engenharia para obter uma lista completa. Os dados exportados são usados para preencher páginas não conectadas e as alterações no ALM aparecerão após o próximo ciclo de exportação.

Frequência de cache e exportação\
O sistema usa a frequência de exportação de back-end e o cache de front-end para gerenciar as atualizações de dados. As alterações feitas no ALM são refletidas em seu portal após a exportação agendada e a atualização do cache. Algumas atualizações podem não aparecer imediatamente devido a esses mecanismos. Se precisar de atualizações mais rápidas, ajuste o agendamento de exportação ou limpe o cache conforme necessário.

Suporte à personalização de CSS/JS\
Você pode aplicar CSS personalizado e JavaScript a páginas conectadas e não conectadas usando a guia Personalização. Isso permite manter a consistência de marca, adicionar elementos personalizados de interface e aprimorar a experiência do usuário em todo o portal. Todas as personalizações são aplicadas globalmente, garantindo uma aparência unificada.

Diferenças de URL e marcas (favicon, título da página)\
Páginas não conectadas e conectadas podem ter URLs diferentes para distinguir os estados de usuário. Você pode personalizar o favicon e o título da página do seu portal, ajudando a reforçar a identidade da sua marca. Esses recursos estão disponíveis no Experience Builder. Consulte o departamento de engenharia para obter o status mais recente no suporte não conectado.

## Desempenho e escalabilidade

### Pilha compartilhada vs. pilha premium

A pilha compartilhada permite que vários clientes usem o criador de experiências não conectado em uma infraestrutura comum, oferecendo suporte a níveis de tráfego padrão. A pilha premium é uma opção paga que fornece recursos dedicados, recursos em tempo real e limites de vagas mais altos para clientes com necessidades avançadas. Escolha a pilha com base no tráfego esperado e nas necessidades dos negócios.

### Limites de tráfego e limitação da taxa

A pilha compartilhada impõe limites de tráfego para garantir o uso justo entre os clientes. A engenharia implementará a limitação de taxa para evitar que um único cliente consuma todos os recursos. Se você planeja campanhas de marketing ou espera alto tráfego, coordene-se com a engenharia para entender seus limites e evitar interrupções no serviço. A limitação de taxa ajuda a manter a estabilidade e o desempenho do sistema para todos os usuários.

Considerações sobre multilocação e SEO\
A plataforma oferece suporte a multilocação, permitindo que vários clientes hospedem seus portais em uma infraestrutura compartilhada. As páginas não conectadas são compatíveis com SEO, juntamente com sitemap.xml e robots.txt para otimizar a visibilidade do mecanismo de pesquisa. Isso garante que seu portal seja detectável e indexado adequadamente pelos mecanismos de pesquisa.

## Migração e obsolescência

### Transição da página inicial não conectada existente

O recurso antigo de página inicial não conectada será descontinuado. As novas contas não verão essa opção, e as contas existentes que a usarem serão notificadas para migrar para a solução baseada no Experience Builder. Você deve recriar sua página inicial usando o novo Experience Builder para flexibilidade aprimorada, suporte a widgets e experiência do usuário aprimorada. O plano de transição garante interrupção mínima e suporte contínuo.

Plano de comunicação\
Os clientes que usam a página inicial herdada receberão uma comunicação clara sobre o cronograma de descontinuação e as etapas de migração. Será fornecido suporte para ajudá-lo a mover sua página inicial para a nova plataforma do Experience Builder, garantindo que você se beneficie de novos recursos e atualizações contínuas.

### Suporte a localização e login

Lógica de fallback de localidade\
O sistema exibe as páginas no local em que foram criadas. Se a localidade de um usuário não estiver disponível, o sistema usará uma lógica de fallback para selecionar a próxima melhor localidade disponível. Isso garante que os usuários sempre vejam o conteúdo em um idioma compatível, melhorando a acessibilidade e a satisfação do usuário.

Tipos de logon compatíveis\
A experiência não conectada é compatível com todos os tipos de logon disponíveis no ALM, incluindo logon único e logon padrão. Os usuários podem navegar pelo conteúdo sem fazer logon e serão solicitados a fazer logon quando necessário, como se inscrever em um curso ou acessar recursos personalizados. Isso fornece uma transição tranquila da navegação para o engajamento.

## APIs não conectadas

### API do objeto de aprendizado do administrador

As páginas do Experience Builder e os portais sem periféricos não conectados geralmente organizam ou filtram cursos com base no produto e na função. A API do Admin LO foi aprimorada para garantir que essas associações sejam acessíveis consistentemente para integrações back-end e sem periféricos, bem como para o conector TDA.

**Ponto de extremidade e comportamento**

Você continua a usar o ponto de extremidade do OA do administrador existente:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=produtos,funções


Onde:

- loId é a ID do objeto de aprendizado (por exemplo, curso:12345).
- enforcedFields[learningObject] instrui a API a incluir explicitamente produtos e funções para esse LO.

Isso é feito garantindo que as associações de produto e função do OA estejam presentes na resposta quando solicitadas por meio de enforcedFields. A resposta contém, em atributos, os metadados de produto e função necessários para calcular ou expor os produtos (rec_products) e funções (rec_roles) recomendados para o Experience Builder e outros consumidores.

Uma chamada típica de um administrador ou integração se parece com:

curl -X GET \
  “https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=produtos,funções” \
  -H “Autorização: Portador {admin_token}” \
  -H “Aceitar: application/vnd.api+json”

O JSON do LO retornado tem a mesma estrutura básica de antes, mas agora você pode confiar na presença dos campos de produto/função ao solicitá-los por meio de enforcedFields. As integrações que não usam enforcedFields continuam se comportando como antes.

### Listagem de objetos de aprendizado - Suporte a JobAid no filtro effectiveModifiedDate

**Finalidade**

O conector TDA (Acesso a dados de treinamento) e as implementações sem periféricos geralmente precisam executar uma sincronização incremental, com base na **data de modificação efetiva** dos objetos de aprendizado. Até esta versão, as ajudas de tarefa (do tipo OA, ajuda de tarefa) não eram tratadas corretamente quando combinadas com os filtros effectiveModifiedDate. Esta versão corrige isso para que as ajudas de tarefa possam ser sincronizadas incrementalmente, assim como os cursos e caminhos de aprendizado.

**Ponto de extremidade e comportamento**

Você usa o ponto de extremidade da listagem do LO existente com filtros de data e tipo de LO:

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Anteriormente, quando filter.loTypes=jobAid era combinado com um intervalo effectiveModifiedDate, o filtro excluía efetivamente JobAids e a chamada se comportava como se JobAids não fosse suportado.

A partir dessa atualização, a chamada retorna apenas objetos de aprendizado JobAid cuja effectiveModifiedDate esteja dentro da janela especificada.

```
{  
  "links": {  
    "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"  
  },  
  "data": [  
    {  
      "id": "jobAid:144968",  
      "type": "learningObject",  
      "attributes": {  
        "authorNames": ["Sid"],  
        "dateCreated": "2026-01-20T08:48:55.000Z",  
        "datePublished": "2026-01-20T08:48:55.000Z",  
        "dateUpdated": "2026-01-20T08:48:55.000Z",  
        "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",  
        "loType": "jobAid",  
        "loFormat": "Content",  
        "loResourceType": "Content",  
        "localizedMetadata": [  
          {  
            "description": "Link jobAid new",  
            "locale": "en-US",  
            "name": "Link jobAid new"  
          },  
          {  
            "description": "Link jobAid new fre",  
            "locale": "fr-FR",  
            "name": "Link jobAid new fre"  
          }  
        ],  
        "relationships": {  
          "authors": {  
            "data": [  
              { "id": "13385176", "type": "user" }  
            ]  
          },  
          "instances": {  
            "data": [  
              { "id": "jobAid:144891_-1", "type": "learningObjectInstance" }  
            ]  
          }  
        }  
      }  
    }  
  ]  
}
```

Isso significa que agora você pode implementar com segurança sincronizações incrementais de JobAid com base em effectiveModifiedDate, da mesma maneira que você já faz para outros tipos.

Se você omitir filter.loTypes=jobAid, o comportamento de outros tipos de LO não será alterado; a alteração afetará apenas a combinação de JobAid com esse filtro.

### **API de Menu: Filtro de Menu Não Conectado**

**Finalidade**

O Experience Builder e os front-ends sem periféricos precisam de uma maneira direta de recuperar o **menu não conectado**, aquele que define a navegação para visitantes públicos. Antes desta versão, você tinha que buscar todos os menus e, em seguida, aplicar a lógica personalizada para identificar qual representava a navegação não conectada. Esta versão adiciona um filtro simples do lado do servidor.

**Ponto de extremidade e comportamento**

Use o ponto de extremidade da listagem de menus existente com um novo parâmetro de consulta:

GET /primeapi/v2/templates/menus?include=páginas,subMenus.pages&amp;isNonLoggedIn=true


Os pontos principais:

- include=pages,subMenus.pages é opcional, mas recomendável quando precisar dos detalhes da página e da página do submenu na mesma resposta.
- isNonLoggedIn=true é novo nesta versão e instrui o servidor a retornar somente menus sinalizados como menus não conectados.

Sem o parâmetro isNonLoggedIn, o ponto de extremidade se comporta exatamente como antes e retorna menus de acordo com o comportamento padrão existente. Com isNonLoggedIn=true, ele normalmente retorna o menu único usado pela experiência não conectada para sua conta (já que normalmente há apenas um menu não conectado por conta).

Na prática, um cliente agora pode emitir:

curl -X GET \
  “https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&amp;isNonLoggedIn=true” \
  -H “Autorização: Portador {admin_token}” \
  -H “Aceitar: application/vnd.api+json”


e obtenha de volta a estrutura de navegação não conectada em uma chamada, com todas as páginas que devem estar visíveis para visitantes anônimos.

Isso é particularmente útil ao criar um site independente não conectado e desejar espelhar a mesma navegação que o Experience Builder usa ou ao depurar se o menu não conectado foi configurado corretamente.

## Permitir listagem de domínios personalizados

A pilha não conectada consiste em:

- Um domínio CDN público (por exemplo, cpcontents.adobe.com ou yourdomain.example.com) que fornece layouts, config JSON e ativos estáticos.
- Um ponto de extremidade de Elasticsearch público (ES) que fornece dados de catálogo e pesquisa, mas somente se a solicitação vier de um **domínio com lista de permissões** para essa conta do ALM.

Quando você introduz um domínio personalizado, ele funciona perfeitamente sem nenhum esforço adicional após o processo existente para adicionar um domínio personalizado.

### Pré-requisitos

Antes de incluir na lista de permissões um domínio personalizado para usuários não conectados:

1. O domínio personalizado é configurado para sua conta ALM (por exemplo, DNS para academy.yourcompany.com aponta para Adobe / Akamai e certificados são provisionados).
2. O **conector TDA (Acesso a Dados de Treinamento)** está habilitado para a conta.
3. O recurso **Experience Builder** não conectado está habilitado (lado Adobe).

Essas etapas garantem que:

- Sua conta tem um JSON **de conta não conectado (geralmente referenciado como accountConfig / experienceBuilderConfig), que inclui campos como cpDomain, almDomain, almCdnBaseUrl, esBaseUrl e domínios com permissão listada.**
- A pilha não conectada sabe onde fornecer dados e de que domínios deve aceitar solicitações.

### Como funciona a listagem de permissões

A lista de permissões é armazenada na configuração que o TDA exporta e a pilha não conectada lê. Essa configuração inclui:

- Os domínios do ALM (cpDomain, almDomain).
- A **URL base da CDN** para conteúdo não conectado (almCdnBaseUrl).
- A **URL de base de pesquisa pública** (esBaseUrl).
- A lista de domínios que podem fazer chamadas públicas não conectadas para essa conta.

Para que o Experience Builder não conectado funcione em um domínio personalizado:

- O navegador deve carregar o HTML não conectado desse domínio personalizado (ou do domínio CDN não conectado ao ALM, dependendo da sua configuração).
- Chamadas desse domínio para os endpoints públicos ES e CDN devem ser aceitas. Isso só acontece se o domínio estiver presente na lista de permissões.

Esta versão adiciona um novo domínio CDN não conectado, cpcontents.adobe.com, e especifica que ele deve ser colocado nos **domínios listados de permissão** no conector TDA. Para usuários nativos não conectados, isso requer uma atualização.

### Permitir listagem de um domínio personalizado

**Configurar o domínio personalizado no ALM**

Trabalhe com o Adobe para registrar seu domínio, por exemplo, academy.yourcompany.com, como o domínio personalizado para sua conta do ALM. Você atualiza o DNS para apontar para o Adobe Akamai, conforme instruído, e aguarda a conclusão do SSL e do roteamento.

Nesse ponto, o tráfego conectado e não conectado pode acessar o ALM por meio desse domínio, mas chamadas de pesquisa e catálogo não conectadas ainda poderão ser bloqueadas se o domínio não estiver na lista de permissões.

**Habilitar TDA e Experience Builder não conectado**

Verifique se:

- O **Conector de Acesso a Dados de Treinamento** está habilitado.
- O recurso **Experience Builder não conectado** está ativado para a conta.

A ativação do TDA cria ou atualiza o JSON da conta não conectada. Para novas contas, o processo também permite a pré-listagem do novo domínio CDN não conectado (cpcontent.adobe.com) por padrão, de modo que o ponto de extremidade ES público espera chamadas desse domínio.

Para contas que já estavam usando a pilha mais antiga não conectada, a especificação do M45 indica que os conectores existentes devem ser excluídos e recriados para selecionar o novo domínio.

**Adicionar o domínio personalizado à lista de permissões**

A parte crítica é informar à pilha ES não conectada que academy.yourcompany.com é uma origem aprovada. Há dois caminhos comuns.

1. **Reabilite o conector TDA (simples, amigável ao autoatendimento)**

O wiki do Experience Builder M45 explica que os usuários nativos não conectados precisarão excluir e reativar a conexão TDA para que o novo domínio seja automaticamente incluído na lista de permissões. Isso permite duas coisas:
1. A conta não conectada JSON é gerada novamente.
2. Os domínios listados de permissão são atualizados para incluir o novo domínio CDN não conectado e seu domínio personalizado.

Isso é recomendado quando você tem um pequeno número de contas e pode tolerar a desativação e reativação temporárias do conector.

1. **Verifique se o domínio está na lista de permissões**

Após a listagem de permissões, abra o site não conectado no domínio personalizado e inspecione as chamadas de rede do navegador.

Você deseja ver:

- Solicitações para almCdnBaseUrl (por exemplo, [https://cpcontent.adobe.com/](https://cpcontent.adobe.com/)...) 200/304.
- Solicitações para esBaseUrl (API de pesquisa pública, por exemplo [https://primeapps.adobe.com/almsearch/api/v1/](https://primeapps.adobe.com/almsearch/api/v1/)...) êxito ao retornar JSON com dados de pesquisa/catálogo.

Se essas chamadas retornarem 4xx ou erros explícitos sugerindo “domínio não confiável” ou “origem não permitida”, a lista de permissões estará incompleta ou configurada incorretamente e o suporte precisará ajustá-la.

O LLD não conectado também observa que a configuração da conta pode conter um valor de domínio esperado. No tempo de execução, o site verifica se o domínio no URL corresponde ao que está definido na configuração; se não corresponder, o usuário poderá ser redirecionado para uma página de erro. Isso protege contra o acesso da configuração de um cliente por meio do domínio de outro cliente.

## Usar recomendações no Experience Builder não conectado

O Experience Builder não conectado permite criar páginas de aprendizado públicas nas quais os visitantes podem navegar no catálogo e ver o conteúdo destacado antes de fazer logon. Mesmo que esses visitantes sejam anônimos, você ainda pode apresentar treinamentos recomendados usando metadados e widgets.

No aplicativo do aluno conectado, as recomendações podem ser personalizadas: elas podem depender do perfil, do histórico, das habilidades e do progresso do aluno. Na experiência **não conectada**, ainda não há nenhuma identidade do aluno, portanto, a plataforma não pode personalizar por usuário.

O Recommendations no modo não conectado é:

- **Com curadoria ou baseado em regras**: baseado em catálogo, produto, função, rótulos, marcas e outros metadados.
- **Orientado a segmentos**: “recomendado para desenvolvedores”, “recomendado para parceiros”, “apresentado para iniciantes”.
- **Foco em marketing**: usado para atrair e orientar os visitantes a se inscreverem assim que fizerem logon.

### Metadados e APIs que oferecem suporte a recomendações

Em segundo plano, as páginas não conectadas usam:

- O **conector TDA** para exportar metadados de objetos de aprendizado (cursos, caminhos, certificações, ajudas de tarefa) para um índice de pesquisa público.
- A **pilha de pesquisa pública** para responder a consultas de widgets não conectados (catálogo, pesquisa, cursos e caminhos, categorias).
- A **API de Objetos de Aprendizado de Administrador** para expor metadados de produto e função que podem ser usados para regras de recomendação.

Nesta versão, a API do Admin LO foi estendida para que as associações de produto e função estivessem disponíveis de forma confiável:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=produtos,funções

Isso permite que widgets e integrações sem periféricos criem recomendações baseadas em regras usando produtos, funções, etiquetas de catálogo, tags e outros campos de forma consistente.

### Criar seções de recomendação com os widgets do Experience Builder

Crie seções de recomendação em páginas não conectadas ao combinar **widgets do Experience Builder** com filtros de metadados.

#### **Widget Cursos e caminhos**

Use o widget **Cursos e caminhos** quando quiser mostrar uma linha ou grade de itens recomendados. Em sua configuração, você pode escolher:

- De quais catálogos extrair.
- Quais rótulos de catálogo, produtos, funções ou tags usar como filtros.
- Se deve mostrar cursos, caminhos, certificações, ajudas de tarefa ou uma combinação.
- Classificação e número máximo de itens.

Por exemplo, você pode criar:

- “Recomendado para desenvolvedores”: filtre por produto ou função usada para conteúdo de desenvolvedor.
- “Iniciar aqui”: filtre por um rótulo, como “Inicial” ou “Integração”.
- “Este trimestre em destaque”: filtre por um rótulo com limite de tempo, como destaque-q3-2026.

O widget não está aprendendo com o comportamento. Ele mostra tudo o que corresponde às regras de metadados que você definir. Do ponto de vista de um visitante, no entanto, parece uma faixa de recomendação.

#### **Widget de categorias**

Use o widget **Categorias** para ajudar os visitantes a navegar nos conjuntos de conteúdo “recomendados”, mesmo que eles não saibam os nomes dos seus produtos.

É possível configurar ladrilhos que representem um segmento, como:

- “Para administradores”
- “Para equipes de vendas”
- “Para parceiros”
- “Por linha de produto”

Cada bloco pode ser vinculado a:

- Uma página de catálogo filtrada (por exemplo, o catálogo filtrado por determinados produtos ou rótulos).
- Uma página dedicada não conectada que usa cursos e caminhos pré-configurados para esse segmento.

Isso proporciona uma experiência de “caminhos recomendados por segmento” sem personalização.

### Criação de recomendações baseadas em segmentos

Como os visitantes não conectados ainda não têm um perfil ALM, é útil criar recomendações **por segmento** e permitir que os visitantes selecionem por conta própria.

1. Use uma **página inicial não conectada** que explique brevemente para quem é a sua academia e mostre um pequeno número de pontos de entrada de segmento (por exemplo, “Desenvolvedores”, “Profissionais de marketing”, “Parceiros”, “Novos funcionários”). Isso pode ser feito com um widget Categorias ou uma caixa de Conteúdo ou seção HTML simples com botões.
2. Para cada segmento, crie uma **página dedicada não conectada** no Experience Builder. Nessa página, use um ou mais widgets Cursos e caminhos configurados com filtros que representem o que é “recomendado” para esse grupo. Por exemplo, para “Desenvolvedores” você pode filtrar em:
   1. Catalog = “Treinamento público”
   2. Produto = “Adobe Experience Manager”
   3. Tags = “Fundamentos do desenvolvedor”
3. Use essas páginas de segmento como destino de suas campanhas de marketing e como destino dos blocos na home page não conectada.

Os visitantes percebem que estão vendo recomendações personalizadas para sua situação, mesmo que a lógica seja definida em tempo de design através de metadados.

### Transição de recomendações não conectadas para personalizadas

As recomendações não conectadas são principalmente sobre **capacidade de descoberta** e **conversão**. Depois que os visitantes decidirem se inscrever ou iniciar o treinamento, eles farão logon e se tornarão alunos completos com um perfil e um histórico.

O fluxo normal é:

1. Um visitante descobre conteúdo por meio de seções de recomendação não conectadas (recomendações iniciais, páginas iniciais de segmentos, linhas em destaque).
2. Eles clicam em uma visão geral do curso ou caminho e escolhem se inscrever ou começar.
3. O ALM solicita que se inscrevam ou façam logon.
4. Depois de fazer logon, a experiência padrão do aluno conectado assume o controle, incluindo:
   1. “Meu aprendizado”
   2. Catálogo conectado com progresso pessoal
   3. Qualquer sistema de recomendação interno usado para os alunos existentes.

Em outras palavras, as recomendações conectadas os ajudam a decidir o que fazer em seguida e a continuar.

## Como as ajudas de tarefa podem ser usadas no novo Experience Builder não conectado

Na **Interface de Usuário**, as ajudas de tarefa participam de experiências não conectadas principalmente por meio de widgets que podem mostrar objetos de aprendizado:

1. **Widget de cursos e caminhos**\
   Este widget pode mostrar vários tipos de objeto de aprendizado, incluindo ajudas de tarefa. Em páginas não conectadas, você pode configurá-las para:
   1. Incluir ou excluir ajudas de tarefa explicitamente.
   2. Filtre ajudas de tarefa por catálogo, produto, função, rótulos, marcas e outros metadados.
   3. Apresente-os ao lado de cursos e caminhos ou como uma faixa separada de “Recursos”.

Por exemplo, em uma página de aterrissagem pública, você pode configurar uma faixa intitulada “Recursos úteis”, que mostra apenas ajudas de tarefa, e outra faixa intitulada “Cursos recomendados”, que mostra cursos e caminhos.

1. **Página e pesquisa do catálogo**\
   As superfícies do **catálogo** e da **pesquisa** não conectadas usam o índice de pesquisa público (alimentado pelo conector de Acesso a Dados de Treinamento). Esse índice agora suporta ajudas de tarefa corretamente, portanto:
   1. Os resultados de pesquisa não conectados podem incluir ajudas de tarefa.
   2. Filtros de catálogo não conectados (por tipo, produto, marcas etc.) pode incluir ajudas de tarefa, desde que a configuração da sua conta e os widgets estejam configurados para exibi-los.
2. **Páginas de visão geral do LO**\
   Quando um visitante clica em uma ajuda de tarefa de qualquer widget ou do catálogo, ele vai para uma **página de visão geral do OA** dessa ajuda de tarefa no modo não conectado. A partir daí, eles podem ler a descrição e os metadados. O download ou o consumo real normalmente ainda requer logon, mas a presença e a capacidade de descoberta da ajuda de tarefa em si são tratadas pela experiência não conectada.

### Como as ajudas de tarefa são expostas por meio de APIs não conectadas

No **lado da API**, as ajudas de tarefa são suportadas por:

1. O **Conector de Acesso a Dados de Treinamento e a pesquisa pública**\
   O TDA exporta metadados de ajuda de tarefa junto com outros tipos de objeto de aprendizado para o índice de pesquisa pública que atende a consultas de pesquisa e catálogo não conectadas. É nisso que o Experience Builder e os front-ends sem periféricos dependem.
2. A listagem de **Objetos de Aprendizado com effectiveModifiedDate**\
   Nesta versão, o ponto de extremidade da lista de OAs foi corrigido para que as ajudas de tarefa funcionem corretamente com o filtro effectiveModifiedDate. Agora você pode ligar para:

GET /primeapi/v2/learningObjects\
?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z\
&amp;filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z\
&amp;filter.loTypes=jobAid


Antes dessa alteração, a combinação de effectiveModifiedDate com loTypes=jobAid não retornou ajudas de tarefa de forma confiável. Agora, como documentado no wiki *Alterações de API Pública do M45*. Ou seja:

1. Seus trabalhos TDA ou ETL podem **sincronizar incrementalmente ajudas de tarefa** para experiências não conectadas, da mesma forma que fazem para cursos e caminhos.
2. Qualquer implementação sem periféricos que compila um diretório público de ajuda de tarefa pode consultar alterações com base em effectiveModifiedDate e loType=jobAid.

A resposta de amostra no documento M45 mostra um learningObject com loType: “jobAid” e loFormat: “Content” sendo retornados ao usar esse padrão.

1. A **API do OA do administrador**\
   Embora não seja específico para usuários não conectados, o M45 também atualiza a API do LO do administrador para expor consistentemente os metadados de produto e função para todos os tipos de LO por meio de:

GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=produtos,funções


Para ajudas de tarefa, isso significa que você pode gerenciar seus produtos, funções, etiquetas e etiquetas centralmente e confiar nesses metadados em experiências públicas não conectadas, por exemplo, nas seções “Recursos para profissionais de marketing” ou nas páginas iniciais específicas do produto.

**Observação**:

No estado não conectado:

- As ajudas de tarefa são principalmente **detectáveis**: os visitantes podem ver que elas existem, ler descrições e entender como elas oferecem suporte a tópicos ou cursos.
- O **consumo** real (baixar ou abrir o conteúdo de ajuda de tarefa) normalmente ainda requer logon, especialmente se as ajudas de tarefa forem consideradas parte de conteúdo licenciado ou interno.

## Alterações na “breve descrição” na pesquisa do LO (não conectado)

Na pilha não conectada, a pesquisa e a listagem de objetos de aprendizado (LOs) são acionadas pelo conector Acesso a dados de treinamento (TDA) e por um índice de Elasticsearch público. Historicamente, essa pilha usava um único campo de visão geral/descrição para cada LO. Os clientes que criam portais sem periféricos não conectados queriam mostrar a mesma descrição curta em blocos do OA que a interface do aluno conectada mostra, em vez de apenas a visão geral longa.

A alteração introduz suporte para o OA **breve descrição** em APIs de pesquisa e listagem não conectadas:

- Para **cursos**, a semântica da interface do usuário existente é:
   - Cartões conectados mostram “Breve descrição” (campo de 140 caracteres), se presente; caso contrário, eles voltam para a longa “Visão geral detalhada”.
- Para **caminhos de aprendizado**, a interface de usuário conectada usa o campo “Benefícios” como a descrição curta, se definida, e retorna para a visão geral caso contrário.
- Para **certificações**, uma “Descrição” curta é usada, com uma “Visão geral da certificação” mais longa como fallback.
- Para **ajudas de tarefa**, o campo de descrição principal é usado.

## Outras alterações

### Restrição de que duas contas não podem compartilhar o mesmo domínio personalizado

Nas arquiteturas não conectadas e conectadas do Adobe Learning Manager, um **domínio personalizado** (por exemplo, academy.example.com) é tratado como uma chave globalmente exclusiva que deve ser mapeada para exatamente uma conta do ALM, para que a plataforma aplique uma restrição rígida de que **nenhuma conta pode compartilhar o mesmo domínio personalizado**. Isso é necessário para segurança, roteamento e SEO: a camada de roteamento e a pilha não conectada usam o domínio para pesquisar a configuração correta da conta (incluindo sua conta não conectada JSON, menus do Experience Builder, identidade visual e pontos de extremidade TDA/pesquisa),

Permitir o mesmo domínio personalizado em duas contas tornaria impossível garantir que os dados da conta sejam retornados, poderia causar vazamento entre locatários e também corromperia artefatos gerados, como sitemap.xml e robots.txt, que são produzidos por conta, mas descobertos por mecanismos de pesquisa por host. Operacionalmente, isso significa que, ao atribuir ou mover um domínio personalizado, primeiro você deve garantir que ele não esteja anexado a nenhuma outra conta (ou cancelar o registro dele), e as ferramentas internas do Adobe rejeitarão as tentativas de vincular o mesmo domínio a várias contas.

### Cache de navegador de recursos na experiência não conectada

Na experiência não conectada do Adobe Learning Manager, o cache de recursos do navegador é uma parte central da estratégia de desempenho e escala, porque as páginas públicas devem lidar com tráfego de marketing grande, às vezes pontiagudo, com baixa latência e carga mínima de origem. Ativos estáticos e semiestáticos, como o shell de HTML não conectado (por exemplo, index.html/guest.html), a configuração no nível de conta JSON (account.json ou config.json), o layout de página do Experience Builder JSON (menus, layouts de widget, configurações de cartão), CSS, JS, imagens e favicons são fornecidos de um CDN do Akamai (cpcontents.adobe.com / cpcontent.adobe.com) com cabeçalhos de cache que incentivam a reutilização no lado do CDN e no lado do navegador, para que, após o primeiro carregamento de página, o navegador possa renderizar páginas não conectadas subsequentes em grande parte de seu cache, revalidando apenas quando necessário via ETag ou Última modificação.

## Executar as opções da página inicial

Na página inicial do Adobe Learning Manager, selecione **Marcas**. Em seguida, no painel esquerdo, selecione Não conectado na página inicial.

![opções de home page](/help/migrated/administrators/feature-summary/assets/non-logged-in-homepage.png)

*Selecione a opção Não conectado na Página Inicial*

## Adicionar um banner

Adicione um banner a qualquer anúncio de marketing ou destaque os tópicos em alta do dia. Selecione **Adicionar banner**.

![banner](/help/migrated/administrators/feature-summary/assets/add-banner-image.png)

*Adicionar um banner*

Navegue até o local da imagem a ser usada como banner. Em seguida, forneça um link como um botão de ação na imagem do banner.

## Adicionar categorias

Este componente pode ser usado para filtrar o catálogo por marcas, habilidades e catálogo. Esta seção contém um cabeçalho e uma descrição para cada categoria. Ao clicar, o usuário é redirecionado para a página do catálogo com os filtros aplicados.

Selecione **[!UICONTROL Adicionar categoria]**. Em seguida, insira os detalhes da categoria.

![adicionar categoria](/help/migrated/administrators/feature-summary/assets//add-category.png)

*Adicionar as categorias*

Salve a categoria. A categoria é adicionada à seção.

## Adicionar um catálogo

Adicione um catálogo para usuários não conectados para que eles possam navegar por todo o treinamento na plataforma.

![adicionar catálogo](/help/migrated/administrators/feature-summary/assets//add-catalog.png)

*Adicionar um catálogo*

Todo o treinamento exportado estará presente.
