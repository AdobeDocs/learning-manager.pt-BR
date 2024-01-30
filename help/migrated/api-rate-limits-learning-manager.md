---
jcr-language: en_us
title: Limites de taxa da API no Learning Manager
contentowner: saghosh
preview: true
source-git-commit: 544c695a77c21dd9162b9b943b6119d27aa373dc
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 51%

---



# Limites de taxa da API no Learning Manager

## Introdução à limitação das taxas {#introductiontoratelimiting}

O Adobe Learning Manager expõe um conjunto avançado de APIs REST que ajuda os clientes a criar aplicativos que se integram ao Learning Manager ou até mesmo experiências de usuário personalizadas e extensões para fluxos de trabalho que ajudam seus negócios.

Sempre que uma API é chamada, há recursos computacionais compartilhados que são utilizados nos servidores do Learning Manager e, portanto, devemos ter cuidado e cuidado para garantir que os aplicativos sejam executados corretamente e não prejudiquem as características de desempenho e disponibilidade da plataforma. Isso é feito introduzindo limites em como os clientes da API fazem chamadas (frequência e velocidade).

Por exemplo, um aplicativo pode estar tentando obter todos os usuários nessa conta e pode fazer várias chamadas de API paginadas rapidamente. E, por engano, um desenvolvedor pode chamar isso em um loop fechado, resultando em uma enorme carga no servidor e tornando os aplicativos lentos e até mesmo colocando em risco a plataforma, consumindo mais recursos do que o pretendido ou necessário.

Para resolver esse problema, estamos introduzindo limites de taxa para quantas chamadas de API podem ser feitas por um único usuário em um aplicativo cliente específico de uma conta específica. Nós medimos isso em termos de Solicitações por minuto, abreviado como RPM. Por exemplo, quando dizemos que o limite para chamadas de API GET é de 600 RPM, isso simplesmente significa que um único usuário não pode exceder um máximo de 600 chamadas em um minuto e, se o usuário exceder esse limite, o usuário terá uma taxa limitada. As solicitações são controladas em granularidade de milissegundos, portanto, esse limite corresponde a 1 solicitação a cada 100 milissegundos (ms). Há mais um parâmetro, chamado Intermitência, que também é definido junto com o limite de taxa, que define quantas solicitações um usuário pode fazer além da taxa especificada (no nosso caso, 600 RPM). Por exemplo, se o parâmetro Intermitência for 10; isso significa que até 10 slots serão alocados em uma fila e quando uma solicitação chegar “muito cedo” (no nosso caso, antes de 100 ms), ela será processada imediatamente se houver um slot disponível para ela na fila. O slot é então marcado como “tirado” e não é liberado para uso por outra solicitação até que o tempo apropriado tenha passado (no nosso caso, após 100 ms). O tráfego real geralmente é feito com intermitências, e é aí que o parâmetro de Intermitência ajuda. Para a plataforma do Learning Manager, definimos limites para uma versão específica da API (por exemplo, V2), função (Aluno/Administrador) e um verbo (GET/PUT/POST/DELETE/PATCH). No exemplo, descreva acima, diríamos que o limite de taxa é (600, 10).

Embora sempre tenhamos tido limites de taxa para a API pública no Learning Manager, temos sido bastante liberais ao permitir um RPM muito alto até agora. No entanto, com o crescimento de sua plataforma de aprendizado favorita, vimos um rápido crescimento no uso de nossa API e decidimos fazer com que esses limites de taxa sejam explicitamente documentados para o benefício de todos os nossos clientes e para um melhor gerenciamento da plataforma. Neste contexto, atualizamos nossa API para começar a retornar uma nova resposta de API (Código de status HTTP 429); que você não viu até agora. Esta resposta é fornecida aos clientes da API quando o limite da taxa é violado. Os aplicativos cliente agora precisarão manipular esse código de resposta como adequado à lógica de seu aplicativo. E este documento destina-se principalmente a ajudar os desenvolvedores com as informações necessárias para incorporar a lógica correta em seu código quando eles virem tal resposta.

## Como confirmar os limites de taxa impostos? {#howtoconfirmtheenforcedratelimits}

Para cada solicitação, os cabeçalhos de resposta contêm as seguintes informações:

```
x-rate-limit: 600r/m 
x-burst: 10
```

* x-rate-limit especifica o limite da taxa de solicitação base em termos de solicitações por minuto.
* x-burst especifica quantas solicitações excedentes acima da taxa de solicitação base são aceitas para serem processadas imediatamente.

## Como detectar erros causados por limites de taxa? {#howtocatcherrorscausedbyratelimits}

Para cada solicitação, você pode verificar se esbarrou no limite de taxa. Se você receber um código de resposta de 429, “{”message”:”429 Too many requests”}”, você atingiu o limite de taxa.

É recomendado incluir no script um código que capture 429 respostas. Se o script ignorar o erro “Muitas solicitações” e continuar tentando fazer solicitações, você poderá começar a receber erros nulos. A essa altura, as informações de erro não serão úteis no diagnóstico do problema.

Por exemplo, uma solicitação curl que atinge o limite de taxa pode retornar a seguinte resposta:

```
< HTTP/2 429 
< date: Wed, 04 Nov 2020 06:53:04 GMT 
< content-type: application/json; charset=utf-8 
< server: openresty 
< x-rate-limit: 60r/m 
< x-burst: 10 
< retry-after: 10.752 
< access-control-allow-credentials: true 
< access-control-allow-methods: GET, POST, OPTIONS, PUT, HEAD, DELETE, PATCH 
< access-control-allow-headers: X-acap-all-roles, X-acap-account,X-acap-user,X-acap-caller-role,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type, x-experience-api-version, Authorization, X-CSRF-TOKEN, X-HTTP-Method-Override 
< strict-transport-security: max-age=31536000; includeSubDomains 
< x-frame-options: SAMEORIGIN 
< x-xss-protection: 1 
< x-content-type-options: nosniff 
< x-request-id: gwBBFC9741-58A5-43B1-B1FE-7D14275961E7 
< strict-transport-security: max-age=31536000; includeSubDomains
```

A resposta contém informações sobre as seguintes chaves:

```
status: 429 
retry-after: 10.752
```

O código de status de 429 significa “muitas solicitações” e que a solicitação atual não é processada. O cabeçalho retry-after especifica que você pode repetir a chamada de API em 10,752 segundos. Seu código deve parar de fazer solicitações adicionais de API até que tenha passado tempo suficiente para tentar novamente.

O seguinte pseudocódigo mostra uma maneira simples de capturar erros de limite de taxa:

```
response = request.get(url) 
if response.status equals 429: 
    alert('Rate limited. Waiting to retry…') 
    wait(response.retry-after) 
    retry(url)
```

Na verdade, criamos até mesmo uma API fictícia do Learning Manager para você experimentar e se sentir à vontade para manipular o código de status 429.

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: oauth < 
<token>
  >' 'https://learningmanager.adobe.com/learningmanagerapi/v2/dummy 
</token>
```

Esta API fictícia tem um limite de:

```
x-rate-limit: 5r/m 
x-burst: 2
```

O limite para a API fictícia é intencionalmente baixo para que você atinja os limites de taxa muito rapidamente e possa se concentrar mais no desenvolvimento do código para detectar e manipular os erros de limite de taxa.

## Teste da API fictícia {#testingthedummyapi}

Fornecemos um ponto de extremidade para você verificar como a limitação de taxa funciona. Para isso, criamos um ponto de extremidade especial chamado GET /dummy que tem o escopo de leitura do aluno. Essa API foi configurada deliberadamente para um limite de taxa muito restrito de 5 solicitações por minuto, com limite de intermitência = 2.

Você pode testar isso facilmente atingindo esse ponto final com taxas abaixo de 5 RPM e acima de 5 RPM. Escreva o código para manipular o código de status HTTPS de 429 e com base nas informações nos cabeçalhos de resposta.

Para facilitar, você pode verificar este código JavaScript de amostra que ilustra isso. Clique aqui [violino](https://jsfiddle.net/ACAPJS/9yv8zcmL/) e veja o código em ação.

Este aplicativo exige que você forneça um token de aplicativo da função de aluno para sua conta. Consulte [Manual do desenvolvedor de aplicativos](https://captivateLearning Manager.adobe.com/docs/Learning Managerapi/v2/) para obter informações sobre tokens de API e usar o Token Helper na seção de recursos do desenvolvedor do aplicativo Learning Manager Integration Admin para gerar os tokens.

Este aplicativo está fazendo 10 chamadas para a API fictícia em um loop, de uma só vez. Como o limite de taxa é (5, 2) para a API fictícia, o limite de taxa será violado depois que as primeiras chamadas 5+2 recebidas pelo Learning Manager forem bem-sucedidas e você verá uma resposta de sucesso para elas.

No entanto, observe como esse aplicativo está procurando pelo código de status 429 em resposta e lidando com eles. Quando esse aplicativo obtém essa resposta, ele imprime os detalhes na resposta da API, aguarda o tempo sugerido e repete as tentativas com falha.

## Práticas recomendadas para lidar com a limitação de taxa {#bestpracticestohandleratelimiting}

Muitas vezes, os dados de uma conta não são alterados com tanta frequência. Por exemplo, os cursos em uma conta podem não ser alterados com tanta frequência. Em vez de tentar obter todos os dados todas as vezes, veja se você pode obter os dados específicos quando precisar deles e considere o uso de um mecanismo de cache. Dessa forma, quando seu aplicativo realmente precisar fazer muitas chamadas, você terá cota suficiente dentro dos limites da taxa para fazer essas chamadas importantes.

Alguns dados podem ser alterados com mais frequência e talvez você precise obtê-los com mais frequência. Mesmo assim, pergunte-se se o aplicativo pode ter dados ligeiramente obsoletos (algo que pode estar no cache, obtido há N minutos), porque ele pode não ter impacto no fluxo de trabalho do usuário. Mesmo que você precise obter dados novos dos servidores, você pode novamente ser criterioso ao buscar apenas os dados específicos de que precisa, em vez de obter tudo.

Também haverá momentos em que você não terá escolha de obter muitos dados, pois a API pode não ser flexível o suficiente para fornecer exatamente o que deseja com apenas uma chamada. Veja se a API fornece filtros e critérios de classificação que podem ser usados para minimizar o número de chamadas; e você ainda deve considerar o armazenamento em cache porque muitos usuários em sua conta podem precisar dos mesmos dados.

Quando você está obtendo muitos dados no contexto de um aplicativo interativo com uma GUI, é provável que o aplicativo esteja tentando fazer muito e pode sobrecarregar o usuário com muitas informações/funcionalidades afetando a experiência do usuário de seu aplicativo.

Ao criar um aplicativo não interativo (talvez algo como um trabalho diário), talvez seja necessário buscar muitos dados em massa. Nesses casos, considere o uso da API de trabalho, projetada principalmente para retornar dados em massa no formato CSV. Observe que a API de trabalho terá uma restrição de cota que você pode invocá-la N vezes por dia.

Desde que o Learning Manager implementou as especificações JSONAPI, há API onde você também pode sideload de alguns dados. Isso ajudará você a não fazer mais chamadas de API, mas você terá que trocar isso por obter dados muito ansiosamente. Como os dados de sideload às vezes podem ser muito grandes, em chamadas paginadas de API, você faz o tamanho máximo da página limitado a 10; mas para chamadas de API sem inclusões, você pode especificar um tamanho de página maior (até 100)

Eventualmente, se você fizer muitas solicitações de API em um curto período de tempo, você atingirá o limite de taxa de API para solicitações. Quando você atingir o limite, o Learning Manager parará de processar mais solicitações até um determinado período de tempo.

Os limites de taxa estão descritos na última seção deste artigo. É recomendável que você se familiarize com os limites.

## Limites de Taxa para Pontos de Extremidade da API V2 {#ratelimitsforv2apiendpoints}

A tabela a seguir fornece os limites para os vários endpoints V2. Atualmente, os limites de taxas não estão sendo impostos aos clientes, mas serão aplicados a partir de DD/MM/AAAA. Portanto, torna-se importante que os clientes revisem o código de seus aplicativos existentes para ver como podem ajustar seu código a fim de estarem cientes desses limites de taxa e lidarem com as respostas da API com o código de status HTTP 429.

<table> 
 <tbody>
  <tr> 
   <td><p><b>Operação</b></p></td> 
   <td><p><b>API do administrador</b></p></td> 
   <td><p><b>API do aluno</b></p></td> 
  </tr> 
  <tr> 
   <td><p>DELETE</p></td> 
   <td><p>(25, 10) <br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PATCH</p></td> 
   <td><p>(60, 20)</p></td> 
   <td><p>(15, 5) <br></p></td> 
  </tr> 
  <tr> 
   <td><p>POST</p></td> 
   <td><p>(30, 10)<br></p></td> 
   <td><p>(30, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PUT</p></td> 
   <td><p>(20, 10)<br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>GET</p></td> 
   <td><p>(100, 100)<br></p></td> 
   <td><p>(100, 30)<br></p></td> 
  </tr> 
 </tbody>
</table>

