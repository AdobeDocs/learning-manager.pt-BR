---
description: Leia este artigo para saber como incorporar o fluidic player em um aplicativo personalizado.
jcr-language: en_us
title: Fluidic player incorporável
contentowner: dvenkate
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 0%

---



# Fluidic player incorporável

Leia este artigo para saber como incorporar o fluidic player em um aplicativo personalizado.

Como corporação, agora você pode fornecer uma experiência personalizada para seus alunos, mesmo fora do Learning Manager. Usando a API pública, você pode obter todas as informações relacionadas aos objetos de aprendizado, às inscrições dos alunos e ao progresso do aprendizado e exibi-las no seu site. Mais importante ainda: você pode até mesmo incorporar o Fluidic Player do Learning Manager em seu site, para que o aluno possa consumir o conteúdo diretamente em seu site. O Fluidic Player lhe dá o poder de reproduzir qualquer conteúdo compatível com o Learning Manager. Quando incorporado em seu próprio site, ele tem exatamente os mesmos recursos que quando usado no Learning Manager.

**Reproduzir qualquer conteúdo de e-learning[](../../learners/feature-summary/fluidic-player.md#main-pars_text_779047019)**

O Fluidic Player reproduz praticamente qualquer tipo de conteúdo de e-learning da mesma maneira consistente e intuitiva, sem exigir plug-ins ou downloads. O aluno pode iniciar o conteúdo e, independentemente do tipo de arquivo de conteúdo, ele começa a ser reproduzido.

**Anotações e marcadores**

Você pode fazer anotações e marcar qualquer conteúdo independentemente do tipo de arquivo. Se quiser fazer uma determinada seleção de um arquivo ou vídeo longo, você pode marcar os próprios pontos onde encontrou as informações relevantes para suas necessidades. As anotações e os marcadores podem ser pesquisados ou enviados por email. Clicar neles coloca você no fluidic player exatamente nesse ponto do vídeo ou página do documento.

Para obter mais informações sobre o fluidic player, consulte [Fluidic player](../../learners/feature-summary/fluidic-player.md).

Aqui estão alguns exemplos de onde você pode usar o fluidic player incorporável.

* Você pode usar o fluidic player incorporável no seu *** site para listar os cursos inscritos do seu funcionário e também fornecer um link para iniciar um treinamento na mesma página. Isso significa que os alunos podem realizar treinamentos no site da intranet.

* Se você estiver no negócio de treinamento, talvez tenha um site no qual os clientes compram cursos. Você pode integrar o player incorporável com o mesmo site para que seus clientes possam consumir o conteúdo que compram no seu site.

## Etapas para incorporar o fluidic player em seu site {#stepstoembedfluidicplayerinyourwebsite}

A criação de um aplicativo personalizado para incorporar o fluidic player em seu site envolve três etapas básicas:

1. Criar um aplicativo no aplicativo do administrador de integração do Learning Manager.
1. Recuperar token de acesso.
1. Usar o token de acesso para recuperar recursos do Learning Manager usando a API pública.

### 1. Criar um aplicativo no administrador de integração {#1createanapplicationinintegrationadmin}

Esta etapa é necessária para criar uma ID de aplicativo/cliente e um segredo de aplicativo/cliente que é usado para recuperar o token de atualização e o token de acesso. Para obter mais informações sobre a criação de um aplicativo, consulte  [Processo de desenvolvimento de aplicativos.](developer-manual.md#main-pars_header_994876235)

1. Ir para **[!UICONTROL IntegrationAdmin]** aplicativo e abrir **[!UICONTROL Aplicativos]**.

1. Selecionar **[!UICONTROL Registrar]** no canto superior direito da página.
1. O **[!UICONTROL Registrar um novo aplicativo]** é aberta. Preencha os campos obrigatórios.
1. Se o aplicativo personalizado precisar ser compartilhado em várias contas, selecione **[!UICONTROL Não]** no campo de opção  **[!UICONTROL Apenas para esta conta?]**
1. Para salvar o aplicativo e gerar a ID e o segredo do aplicativo, clique em **[!UICONTROL Salvar]**.

### 2. Recuperar token de acesso {#2retrievingaccesstoken}

Como o Learning Manager usa o OAUTH2.0., o token de acesso é necessário para recuperar recursos usando a API pública. O token de acesso pode ser obtido usando o token de atualização, a ID do cliente ou o segredo do cliente.

**2.1 Token de atualização**

* Recuperar código OAuth

O código OAuth é necessário para recuperar o token de atualização. O Learning Manager redireciona o usuário para o URL de redirecionamento com o código OAuth quando conectado usando o URL abaixo (a extração do código OAuth é exemplificada no arquivo “oauthredirect.html” no aplicativo de amostra):

```
code https://learningmanager.adobe.com/oauth/o/authorize  
client_id= <application_id>  
&redirect_uri=<redirect_uri>  
&state=<dummy_data>  
&scope=learner:read,learner:write  
&response_type=CODE  
&account=<account_id>  
&email=<email_id>
```

Aqui, **[!UICONTROL id do cliente]** é a id do aplicativo obtida na etapa 1.
**[!UICONTROL redirect_url]** é o redirect_url definido na etapa 1.
**[!UICONTROL estado]** há qualquer dado fictício com base no qual precisamos filtrar o URL de redirecionamento para obter o código OAuth. Escopo é o escopo do aluno definido na Etapa 1.
**[!UICONTROL response_typ]**e é sempre “CODE”.\
**[!UICONTROL conta]**é um campo opcional\
**[!UICONTROL email]** é um campo opcional\
&#42; Se a ID da conta e o email forem fornecidos, o URL acima permitirá que o usuário faça logon na mesma conta. Este exemplo de ponto de extremidade é descrito no arquivo “index.html” no aplicativo de amostra.

* Recuperar token de atualização

Depois que o código OAuth é recebido, o token de atualização pode ser recuperado usando o código OAuth, a ID do cliente e o segredo do cliente recebidos do ponto de extremidade abaixo:

**https://learningmanager.adobe.com/oauth/token**

Como resposta à sua solicitação de postagem, você receberá o seguinte:

i. refresh_token\
ii) access_token\
iii) user_id\
iv) expires_in\
v. user_role\
vi) account_id

**2.2 Recuperar token de acesso do token de atualização**

Para recuperar seu token de acesso, envie outra solicitação com seu refresh_token, client_id e client_secret como um corpo de postagem para o URL abaixo:

**https://learningmanager.adobe.com/oauth/token/refresh**

Como resposta à sua solicitação de postagem, você receberá o seguinte:\
i. refresh_token\
ii) access_token\
iii) user_id\
iv) expires_in\
v. user_role\
vi) account_id

### 3. Recuperar recursos usando a API pública {#3retrieveresourcesusingpublicapi}

Como terceira etapa, você precisa usar o token de acesso para recuperar recursos do Learning Manager usando a api pública.  O token de acesso é necessário para fazer qualquer chamada de API pública e deve ser adicionado ao cabeçalho, conforme exemplificado no aplicativo de amostra.

## Reprodutor incorporável {#embeddableplayer}

Aplicativos de terceiros podem usar um reprodutor incorporável para reproduzir o conteúdo de um objeto de aprendizado.

**Abrir um curso no reprodutor incorporável**

1. Criar um URL incorporável

   Para abrir um curso usando o reprodutor incorporável, você precisa criar um URL incorporável conforme mostrado abaixo:

   `https://learningmanager.adobe.com/app/player?lo_id=<v2-api course id>&access_token=<access_token>`

   Aqui, o lo_id precisa estar em conformidade com o formato de ID do curso da API V2.

   Exemplo: `https://learningmanager.adobe.com/app/player?lo_id=course:123456&access_token=45b269b75ac65d6696d53617f512450f`

   Certificações, programas de aprendizado e ajudas de tarefa também podem ser reproduzidos no reprodutor incorporado.

   Exemplos: `https://learningmanager.adobe.com/app/player?lo_id=certification:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=learningProgram:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=jobAid:1234&access_token=c1a4847dfbf4007826a027d481b93c1e`

1. Defina esse URL no atributo “src” do iframe.

**Fechando o reprodutor incorporável**

```
code window.addEventListener("message", function closePlayer(){  
   if(event.data === "status:close"){  
     //handle closing event  
   }  
});
```

## Tutorial do aplicativo de amostra {#sampleapplicationtutorial}

O documento PDF anexado contém um tutorial de amostra do aplicativo.
[Tutorial de amostra e fonte do tutorial para incorporar o Fluidic Player.](assets/sample-applicationtutorial.zip) Conteúdos alternativos

Se você for um administrador, poderá configurar o material do curso de uma maneira que possa oferecer conteúdo alternativo aos alunos no fluidic player. Por exemplo, se você tiver alunos em vários locais geográficos que talvez queiram usar vários idiomas, poderá criar o mesmo conteúdo em vários idiomas. O Fluidic Player oferecerá ao aluno o idioma para o qual ele pode estar configurado, mas o aluno também tem a opção de mudar para o idioma alternativo diretamente do reprodutor.

Controles específicos de vídeo

A tecnologia de transmissão usada pelo Learning Manager fluidic player oferece experiência de reprodução de vídeo aos alunos sem atrasos na inicialização do vídeo e sem requisitos de espaço em disco em qualquer dispositivo. O Fluidic Player também oferece controles inteligentes como a velocidade de reprodução (1x, 1,5X) e a opção ignorar +-10 segundos, que são projetados para dar ao aluno o nível exato de controle de que ele precisa para corresponder à velocidade de aprendizado.

Esse é um esforço que precisa ser realizado por alguém de sua equipe de TI ou por um consultor externo que possa criar um aplicativo que será hospedado em seu site.

1. Modifique o URL do reprodutor incorporado do Learning Manager com parâmetros que apontem para o objeto de aprendizado exato que precisa ser tomado.

   URL:  [https://learningmanager.adobe.com/app/player](https://cpcontents.adobe.com/public/embedplayer/index22fa615ec2baa034a22090c8cd4289fa.html)

1. Use qualquer um destes parâmetros para iniciar um curso:

   * course_id : Esta é a ID do curso a ser iniciado
   * learning_program_id : esta é a ID do programa de aprendizado para iniciar
   * certification_id : esta é a ID da certificação a ser iniciada
   * lo_id : a id do objeto de aprendizado (curso/programa de aprendizado/certificação/ajuda de tarefa) a ser reproduzido


1. Use o token de acesso como um parâmetro obrigatório.

   * access_token : Este é o parâmetro de segurança, use o token de acesso oauth da API pública

   Você pode obter seu token configurando seu fluidic player incorporável no administrador de integração. Você pode obter seu token de autenticação, que pode ser usado como seu token de acesso.

   Exemplo de URL criado: https://learningmanager.adobe.com/app/player?lo_id=“+lo_id+”&amp;access_token=”+accToken

   Aqui, lo_id será a ID do curso, do programa de aprendizado, da certificação e da ajuda de tarefa.

   Exemplos de lo_id - course:21324, learningProgram:2143, certificação:23432, jobAid:237

1. Faça chamadas à API do Learning Manager para recuperar os parâmetros mencionados acima.

   Essas chamadas de API devem ser feitas pelo aplicativo que sua equipe de TI/consultor gravaria e hospedaria no seu site.

   Encontre mais detalhes sobre como usar a API aqui:

   API V1 do Learning Manager - [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



   API V2 do Learning Manager - [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)

   As IDs dos objetos diferem da V1 e da API V2. O reprodutor incorporável espera IDs no formato v2. Use a API de mapeamento de ID na V2 para converter de IDs V1 para IDs V2.

   Depois de construir o URL, uma maneira que o aplicativo o usaria para exibi-lo ao aluno é colocá-lo dentro de um iFrame. Clicar nesse link levaria o Fluidic Player a ser iniciado com o curso específico no contexto.

   ![](assets/salesforce-player.png)

   Para verificar os relatórios de progresso e conclusão, faça logon no Learning Manager.

   Quando o aluno fecha o Player, o fluidic player envia uma mensagem “close” para o elemento pai usando html5 postMessage. O controlador de carregamento deve manipular esta mensagem e continuar.

Modifique o URL do reprodutor incorporado do Learning Manager com parâmetros que apontem para o objeto de aprendizado exato que precisa ser tomado.

URL:  [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player)

Qualquer um desses parâmetros pode ser usado para iniciar um curso:

* course_id : Esta é a ID do curso a ser iniciado
* learning_program_id : esta é a ID do programa de aprendizado para iniciar
* certification_id : esta é a ID da certificação a ser iniciada
* lo_id : a id do objeto de aprendizado (curso/programa de aprendizado/certificação/ajuda de tarefa) a ser reproduzido

Parâmetro obrigatório:

* access_token : Este é o parâmetro de segurança, use o token de acesso oauth da API pública

Faça chamadas à API do Learning Manager para recuperar os parâmetros mencionados acima. Essas chamadas de API devem ser feitas pelo aplicativo que sua equipe de TI/consultor gravaria e hospedaria no seu site.

Encontre mais detalhes sobre como usar a API aqui:

API V1 do Learning Manager - [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



API V2 do Learning Manager -  [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)


