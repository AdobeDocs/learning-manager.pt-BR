---
jcr-language: en_us
title: Integrar o Adobe Learning Manager ao AEM
description: O Learning Manager é um Sistema de Gerenciamento de Aprendizado com um Sistema de Gerenciamento de Conteúdo de Aprendizado interno. Os usuários gerenciam o conteúdo de aprendizado fazendo upload para o Learning Manager para que ele execute o controle de versão, a alocação para os cursos, a definição da visibilidade para os alunos, o controle do consumo e a emissão de relatórios para os administradores.
contentowner: saghosh
exl-id: 61fae7bd-1703-4ed1-9bd9-07387d67a91c
source-git-commit: ffd45cb8cb2d35817e8fc19d5256c14931e31ff3
workflow-type: tm+mt
source-wordcount: '3163'
ht-degree: 54%

---


# Integrar o Adobe Learning Manager ao AEM

O Adobe Learning Manager (ALM) integra-se aos sites do Adobe Experience Manager (AEM). Isso permite que você crie seu próprio site e interfaces móveis responsivas para o Adobe Learning Manager com o mínimo esforço de codificação. Com essa integração, você pode criar experiências de aprendizado personalizadas para seus usuários.

Para criar essa experiência, o ALM fornece um pacote de site de referência do Adobe Learning Manager (pacote do site de referência ALM) para os sites do AEM na forma de um arquivo ZIP que você pode instalar na sua instância do AEM Sites.

O pacote inclui modelos de página da Web e componentes do AEM Sites junto com widgets incorporáveis, por exemplo, catálogo de aprendizado, widgets incorporáveis, calendário e assim por diante.

Depois de instalar o pacote do site de referência ALM, você pode começar a criar um site para o Adobe Learning Manager, que você pode hospedar na sua instância do AEM Sites. Seus usuários podem arrastar e soltar os componentes no site.

>[!IMPORTANT]
>
>Os pacotes Adobe Learning Manager (ALM) para AEM Sites fornecem um bloco de código de início rápido para implementação. Este pacote foi desenvolvido para implantações sem periféricos. Após a implementação da base de código fornecida, a manutenção contínua e o desenvolvimento posterior serão de responsabilidade da parte executora, como é prática padrão com aplicativos sem periféricos baseados no Adobe Learning Manager.

## Instalar pacote do site de referência ALM

### Pré-requisitos

* Licenças para AEM Sites e Adobe Commerce.
* AEM on-premise 6.5 ou Adobe Experience Manager - Cloud Service
* Adobe Commerce 2.4.3

Depois de proteger seu ambiente do AEM Sites, você deve instalar o pacote do site de referência ALM. Esse pacote inclui páginas da Web e componentes de sites do AEM que ajudam a construir a plataforma de aprendizado.

O pacote do site de referência está hospedado no [**Repositório GitHub**](https://github.com/adobe/adobe-learning-manager-reference-site/releases).

Para mais informações, consulte o README:

## Baixar o pacote de conteúdo {#downloadthecontentpackage}

O instalador é enviado como um pacote de conteúdo do AEM. [***Baixe o pacote***](https://github.com/adobe/adobe-learning-manager-reference-site).

O pacote de conteúdo está disponível com arquivo zip e é compatível com AEM 6.4 e AEM 6.5.

## Instalar componente do Learning Manager {#installcaptivateprimecomponent}

Instale o pacote de conteúdo do Learning Manager usando o Gerenciador de pacotes do AEM:

>[!NOTE]
>
>Para obter informações sobre a instalação de pacotes, consulte [***Como trabalhar com pacotes***](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=pt-BR#how-to-work-with-packages).

1. Como autor do AEM, abra o Gerenciador de pacotes do AEM.
1. Clique no botão **[!UICONTROL Carregar pacote]**.
1. Clique em **[!UICONTROL Procurar]** e carregue o pacote de conteúdo.
1. Clique em **[!UICONTROL Carregar]**.
1. Após ser carregado, instale o pacote de conteúdo selecionando-o e clicando em **[!UICONTROL Instalar]**.

   ![](assets/install-package.jpg)

   *Instalar o pacote de conteúdo*

## Criar um aplicativo em [!DNL Adobe Learning Manager]

Depois de instalar o pacote do site do AEM, você deve configurar um aplicativo ALM para conectar seu portal de aprendizado ao site do AEM.

Esse cenário é aplicável quando o AEM é usado com [!DNL Adobe Learning Manager].

Siga as etapas abaixo:

1. Como administrador de integração, clique em **[!UICONTROL Aplicativos]**.
1. Para criar um no aplicativo, no canto superior direito da página, clique em **[!UICONTROL Registrar]**.
1. Na tela Registrar um novo aplicativo, insira os seguintes detalhes:

   1. Nome do aplicativo: o nome do aplicativo que você está criando.
   1. URL: o URL da sua organização.
   1. Domínios de redirecionamento: os domínios de hospedagem do site do AEM. Você também pode especificar curingas.
   1. Descrição: a descrição do aplicativo.
   1. Escopos: selecione o acesso de leitura da função Aluno e o acesso de gravação da função Aluno.
   1. Apenas para esta conta?: selecione Sim se quiser usar o aplicativo para a conta do ALM existente.

1. Após fazer as alterações, clique em Salvar.

Anote as credenciais do aplicativo na tela.

![](assets/application-credentials.png)
*Credenciais do aplicativo*

Para aprovar o aplicativo, clique em **[!UICONTROL Aprovar]**.

## Obter os tokens

1. Na guia Recursos do Desenvolvedor, clique em **[!UICONTROL Tokens de Acesso para Teste e Desenvolvimento]**.

   ![](assets/access-tokens.png)

   *Selecionar Tokens de Acesso para Teste e Desenvolvimento*

1. Insira os seguintes detalhes:

   ![](assets/access-token-details.png)
   *Insira os detalhes do token*

   1. Obter código OAuth: Insira a ID do cliente da seção anterior e altere o escopo. Clique em Enviar para obter o código Oauth.
   1. Obter token de atualização: insira a ID do cliente e o segredo da seção anterior. Insira também o código OAuth obtido na etapa anterior. Clique em Enviar.
   1. Obter token de acesso: insira a ID do cliente e o segredo da seção anterior. Além disso, insira o token de atualização obtido na etapa anterior. Clique em Enviar.
   1. Obter detalhes do token de acesso: insira o token de acesso obtido na etapa anterior. Clique em Enviar.

1. Você pode obter os detalhes da resposta JSON a seguir. A resposta consiste no token de acesso, token de atualização, função do usuário, ID da conta, ID do usuário e o tempo de expiração. Anote o token de atualização, pois você o reutilizará.

## Configurar conta do ALM no AEM

1. Inicie sua instância do AEM.
1. Clique em Configurações > Cloud Service.
1. Clique em Configuração do Adobe Learning Manager.

   ![](assets/alm-configuration.png)
   *Selecionar a configuração do Adobe Learning Manager*

1. Clique em Criar > Pasta de configuração. Nomeie sua pasta.

   ![](assets/create-folder.png)
   *Criar configuração*

1. No projeto de aprendizado, selecione a configuração que você criou.

1. Insira os detalhes da configuração.

   ![](assets/account-congiguration.png)
   *Criar pasta de configuração*

   1. Modo Adobe Learning Manager: escolha como deseja a experiência de aprendizado para alunos conectados e não conectados.
   1. URL do Adobe Learning Manager: insira o URL da instância do ALM onde os serviços de aprendizado estão hospedados.
   1. ID da conta: a ID da conta do ALM.
   1. ID do cliente, Segredo do cliente e Token de atualização do autor: insira as credenciais que você obteve ao criar o aplicativo no ALM.
   1. Personalização do Widget: para obter mais informações, consulte [Integrar com AEM](/help/migrated/integrate-aem-learning-manager.md) `.`

1. Salve e feche a configuração.

### AEM + Adobe Learning Manager (usuários conectados/não conectados)

O Adobe Learning Manager agora permite que você mostre seu produto e treinamento para seus clientes atuais e potenciais e parceiros sem exigir a criação de contas ou logon. Essa funcionalidade ajudará a impulsionar a adoção de produtos e treinamentos, oferecendo aos alunos uma visualização rápida e fácil do treinamento, o que ajuda a destacar e promover recursos do produto. Portanto, você pode apresentar seus produtos e ofertas com eficácia, especialmente para clientes potenciais e parceiros, resultando em um maior reconhecimento do produto. A facilidade de acesso e melhor acessibilidade aumenta o interesse, o que ajuda a impulsionar inscrições em treinamentos e a adoção de aprendizado.

Usando esse fluxo de trabalho, um aluno pode visualizar um treinamento, acessar informações de treinamento ou procurar por treinamento sem fazer logon no Adobe Learning Manager. Esse fluxo de trabalho não é aplicável à interface nativa do Learning Manager (aplicável SOMENTE para o AEM Sites e outras interfaces sem periféricos).

**Configurar e habilitar o conector da plataforma de aprendizado**

Esta seção sublinha as etapas necessárias para configurar e ativar o seguinte conector:

**Acesso a Dados de Treinamento**

Esse conector permite que sua interface de usuário baseada no AEM Sites ou uma outra interface de usuário sem periféricos personalizada recupere e renderize informações de treinamento para os alunos e realize uma pesquisa de informações de treinamento contínua antes ou depois de um aluno fazer logon.

Esse conector só é necessário se você estiver usando interfaces baseadas no AEM Sites ou outras interfaces sem periféricos.

O conector exporta metadados de treinamento para uma solução de armazenamento e recuperação de dados, bem como um sistema de habilitação de pesquisa. Portanto, você pode configurar sua interface de usuário baseada no AEM Sites ou uma outra interface de usuário sem periféricos personalizada para usar esses dois serviços para recuperar dados de treinamento, renderizar páginas da Web e fornecer funcionalidade de pesquisa de treinamento otimizado aos alunos. Por exemplo, uma interface não conectada no AEM Sites pode usar os metadados exportados para ajudar um aluno a pesquisar, navegar e acessar páginas de treinamento que mostram informações de treinamento.

Ative este conector para criar e renderizar suas páginas da Web baseadas no AEM Sites e fornecer experiências personalizadas aos alunos antes e depois do logon. Ative este conector para criar e renderizar suas páginas da Web baseadas no AEM Sites e fornecer experiências personalizadas aos alunos antes e depois do logon.

* URL de base do cdn do Adobe Learning Manager - insira o URL de base do caminho do serviço CDN de recuperação de dados na página de conexão do Acesso a dados de treinamento.
* Token de atualização do administrador - insira o token de atualização que você determinou na seção anterior.
* URL de base de metadados de treinamento - insira o URL de base do caminho do serviço de ativação de pesquisa e recuperação de dados de pesquisa na página de conexão Acesso a dados de treinamento.
* URL de registro do Adobe Learning Manager - insira o URL de registro automático gerado pelo administrador de integração para a conta, que é usado pelos alunos para se inscreverem no treinamento.

### AEM + Adobe Learning Manager + Adobe Commerce (usuários conectados/não conectados)

O Adobe Learning Manager agora fornece soluções para ajudar você a integrar perfeitamente a plataforma de aprendizado com o Adobe Commerce. Esta versão permitirá que você conecte facilmente suas interfaces nativas, baseadas no AEM Sites ou outras interfaces sem periféricos do Learning Manager ao Adobe Commerce. Essa integração permite compreender os recursos de e-commerce na sua plataforma de aprendizado. Agora você pode oferecer treinamento pago para seus clientes e parceiros de negócios, bem como permitir compras de treinamento facilmente nas interfaces nativas e não nativas do Learning Manager. Um aluno também pode visualizar um treinamento, acessar informações de treinamento ou procurar por treinamento sem fazer logon no Adobe Learning Manager.

Um usuário já pode usar o aplicativo AEM e aprová-lo, em vez de criar um.

* URL de base do cdn do Adobe Learning Manager - insira o URL de base do caminho do serviço CDN de recuperação de dados na página de conexão do Adobe Commerce.
* URL do Adobe Commerce: insira o URL da instância do Adobe Commerce que você está usando.
* Caminho do proxy do GraphQL - Os componentes do Learning Manager do lado do cliente acessam o ponto de extremidade do Adobe Commerce GraphQL diretamente e, portanto, pode ocorrer um erro CORS. Para evitar esse erro, todas as chamadas devem ser atendidas do mesmo ponto de extremidade que o AEM ou por meio de um proxy que adicione cabeçalhos CORS.
* Nome da loja da Adobe Commerce - insira o nome da loja da Adobe Commerce que você determinou na seção anterior.
* Tempo de vida útil do token do cliente Adobe Commerce (em segundos) - insira o tempo de vida útil do token do cliente, indicando o período predeterminado para uma sessão de logon.
* Token de atualização do administrador - insira o token de atualização que você determinou na seção anterior.

## Personalizar páginas da Web

Personalize suas páginas da Web usando o site de referências AEM e os widgets disponíveis.

1. Inicie sua instância do AEM.
1. Clique em Sites e abra a página de configuração.
1. Clique em **[!UICONTROL Site de Aprendizado]** > **[!UICONTROL Mestres de Idiomas]** > **[!UICONTROL Inglês]**. Todas as páginas da Web do projeto são incluídas na pasta.

   ![](assets/list-webpages.png)
   *Exibir todas as páginas da Web*

1. Selecione qualquer modelo e clique em **[!UICONTROL Editar]**.

1. Na página, clique no botão de configurações do componente e altere as propriedades do componente.

   ![](assets/settings-button.png)
   *Botão Selecionar Configurações*

1. Visualize suas alterações ou publique a página.

## Criar páginas da Web

Além dos modelos que você pode usar que são fornecidos pelo pacote do site de referência, você também pode criar páginas da Web com base nos modelos do AEM.

1. Na página principal do AEM, clique em Criar > Página.

1. Escolha o modelo que deseja personalizar. Clique em Avançar.

1. Insira as propriedades da página.

   ![](assets/page-properties.png)
   *Propriedades da página*

1. Para criar a página, clique em **[!UICONTROL Criar]**.

1. Selecione a nova página e clique em **[!UICONTROL Editar]**.

1. Insira um componente na página, por exemplo, **Aprendizado- Conteúdo**.

   ![](assets/learning-content.png)
   *Filtrar por site*

1. Escolha os filtros necessários do Catálogo que serão exibidos na página.

## Criar site a partir do Blueprint

O pacote do site de referência do ALM fornece um “Plano do site de aprendizado”, que permite criar um site para sua plataforma de aprendizado. Os blueprints do AEM permitem criar páginas da web diretamente dos componentes do AEM Sites. Você não precisa usar nenhum modelo.

1. Na página inicial do AEM, clique em **[!UICONTROL Sites]**.

1. Clique em **[!UICONTROL Criar]** > **[!UICONTROL Site]**.

1. Clique em Blueprint do site de aprendizado.

   ![](assets/learning-site-blueprint.png)

   *Criar site a partir do esquema*

1. Clique em Avançar.

1. Na página de propriedades, insira os metadados da página. Clique em Criar.

   ![](assets/blueprint-properties.png)
   *Selecionar Blueprint do Site de Aprendizado*

1. Clique no hiperlink Início para navegar até a página inicial do site que você criou. Nesta página, você pode personalizar os widgets e os componentes do catálogo.

## Programar seu site

Além de usar os modelos integrados e criar seu site do zero usando os componentes do WYSIWYG, você também pode escrever código e criar o site.

O código está no [Repositório GitHub do site de referência](https://github.com/adobe/adobe-learning-manager-reference-site) para você começar.

As principais partes do modelo são:

* core: pacote Java que contém todas as funcionalidades principais, como serviços OSGi, ouvintes ou agendadores, bem como código Java relacionado a componentes, como servlets ou filtros de solicitação.
* ui.apps: contém as partes /apps (e /etc) do projeto, ou seja, bibliotecas de clientes JS&amp;CSS, componentes, modelos.
* ui.content: contém conteúdo de amostra que usam os componentes do ui.apps
* ui.frontend: contém componentes do React.

Todos os códigos estão no repositório para você começar a trabalhar.

## Importar e adicionar componentes do Learning Manager para páginas da Web ou modelos existentes

Instalar o pacote do site de referência do AEM adiciona os componentes do Learning Manager à sua instância do AEM Sites. Por padrão, você pode adicionar esses componentes ao site de aprendizado do projeto da Web (site) que fornecemos prontos para uso. Esses componentes também estão disponíveis no site que você cria a partir do Blueprint do site de aprendizado.

No entanto, se quiser usar esses componentes recém-adicionados do Learning Manager em seu projeto da Web ou site existente, você deve importá-los usando o procedimento a seguir.

1. Instale o pacote do site de referência do ALM.

1. Abra o projeto da Web e navegue até o arquivo HTML (da página da Web ou do modelo da Web em que deseja adicionar os componentes do Learning Manager).
1. Ingressando em uma reunião

   Abra o arquivo HTML e adicione os seguintes snippets de código ao componente de página para que o código seja executado antes dos componentes de aprendizado presentes na renderização da página.

   *`<sly data-sly-use.configModel="com.adobe.learning.core.models.GlobalConfigurationModel"/>`*
   *`<meta name="cp-config" content="${configModel.config}" />`*

   O código anterior adiciona a configuração mapeada na marca meta da página, que é necessária para que os componentes de aprendizado sejam renderizados. Para obter mais detalhes, consulte o [site de referência da Adobe Learning Manager](https://github.com/adobe/adobe-learning-manager-reference-site/blob/master/ui.apps/src/main/content/jcr_root/apps/learning/components/page/customheaderlibs.html).

1. Certifique-se de ter mapeado a configuração com o projeto da Web.
1. Abra o modelo do AEM Sites onde deseja importar os componentes do Learning Manager.
1. No editor de página de modelo, navegue até o contêiner Componentes permitidos e selecione **Política**.
1. Na página Política, navegue até Propriedades > Componentes permitidos e selecione os seguintes componentes: “Aprendizado - Conteúdo”, “Aprendizado - Formulário” e “Aprendizado - Estrutura”

O procedimento a seguir permite que o modelo atenda às dependências da biblioteca do cliente dos componentes importados do Learning Manager.

As páginas da Web que incluem esses componentes devem carregar essas bibliotecas para renderizar e usar os componentes com êxito.

1. No editor da página de modelo, clique em Informações da página e em Política da página.
1. Na página Política, navegue até Propriedades > Bibliotecas do cliente e adicione-as à página do modelo:

   1. learning.site
   1. learning.ui
   1. learning.commerce

Depois de salvar este modelo, você pode adicionar os componentes do Learning Manager em todas as páginas da Web derivadas deste modelo.

## Configurar o widget no AEM {#configurethewidgetinaem}

Para a configuração do widget, o autor do AEM requer apenas o token de atualização fornecido pelo administrador de integração do Learning Manager.

Você também pode definir várias configurações de conta em várias páginas.

1. Clique em **[!UICONTROL Ferramentas]** > **[!UICONTROL Cloud Service]** > **[!UICONTROL Configuração do Widget do Learning Manager]**.
1. Clique em **[!UICONTROL Criar]**.
1. Digite o token de atualização aqui. Configure as outras configurações.
1. O nome do host deve ser alterado para “learningmanagereu” para as regiões da UE.
1. Salve e feche a configuração.
1. Selecione uma configuração e publique-a.

## Autor do AEM {#aemauthor}

O autor do AEM deve primeiro adicionar o componente no modelo do AEM

O autor do AEM poderá arrastar e soltar o componente Adobe Learning Manager e configurar adequadamente.

O componente do Learning Manager requer que a configuração criada na etapa acima seja mapeada para a página.  O autor pode mapear a configuração editando as propriedades da página em **[!UICONTROL Avançado]** > **[!UICONTROL Configuração]** > **[!UICONTROL Configuração na nuvem]** e fornecer o caminho da configuração. Dessa forma, o autor pode criar configurações para várias contas do Learning Manager e mapear cada uma para páginas de sites diferentes. Se uma configuração não for mapeada para a página, o componente lerá a configuração da página pai recursivamente até encontrar uma.

## Aluno {#learner}

O aluno pode fazer os cursos de dentro da página.

Para poder acessar o widget do Learning Manager, o aluno deve ser um usuário do AEM conectado. Além disso, a propriedade **email** deve estar presente no nó “/profile” do nó rep:User do aluno. Este e-mail deve ser exatamente igual ao da conta do Learning Manager.

O aluno pode fazer os cursos de dentro da página.

O progresso do curso também é salvo.

Os seguintes widgets são fornecidos:

1. Gamificação
1. Calendário de aprendizado
1. Widget social
1. Widget Catálogo
1. Meu aprendizado
1. Recomendação baseada no aprendizado entre pares
1. Recomendações do administrador
1. Recomendação baseada nos interesses do aluno

Se não houver recomendações, o widget aparecerá em branco.

## Suporte para Skyline

Skyline é a versão em nuvem do AEM. Você deve primeiro instalar o Skyline a partir do gerenciador de pacotes. Para usar o componente do Skyline no AEM, um usuário deve estar presente na conta do Learning Manager. Em outras palavras, o endereço de email do usuário deve existir na conta.

### Implantar o Skyline

As etapas para configurar o Skyline estão descritas no [repositório do GitHub](https://github.com/adobe/captivate-prime-aem-components).

## Widget Meu aprendizado

O widget **[!UICONTROL Meu Aprendizado]** permite exibir o treinamento de um catálogo específico ou de um conjunto de catálogos para um usuário.

Na seção **[!UICONTROL Propriedades]** das propriedades da página, selecione **[!UICONTROL Catálogo]** nas opções listadas.

<!--![](assets/catalog-widget.png)-->

As opções do Catálogo contêm as seguintes opções:

* **[!UICONTROL IDs de catálogo]:** IDs de catálogo separadas por vírgula para as quais o treinamento precisa ser exibido.
* **[!UICONTROL Classificação]:** Ordem de classificação para o treinamento. As opções são: nome, data, data de criação, data de inscrição e assim por diante.
* **[!UICONTROL Estado do Aluno]:** retorna todos os treinamentos que usam os seguintes filtros: inscrito, iniciado, concluído e não inscrito. Os resultados da pesquisa não serão exibidos se a opção de classificação for data de inscrição, data de conclusão ou data de inscrição.
* **[!UICONTROL Nome da habilidade]:** A habilidade usada para filtrar o treinamento exato.
* **[!UICONTROL Nome da marca]:** A marca usada para filtrar resultados exatos.

Veja aqui alguns componentes adicionais que você pode personalizar:

**[!UICONTROL Tipos de Objetos de Aprendizado]:** Filtre de acordo com o tipo do Objeto de Aprendizado. Os tipos suportados são: curso, certificação, ajuda de tarefa e programa de aprendizado.

No AEM, o título de um cartão em uma tira estará vazio inicialmente. Em Propriedades, digite o nome do título em widgets.html.

**Personalização**

Você pode personalizar a aparência do layout usando widgets.html. Você pode alterar a aparência dos cartões que aparecem e personalizar o tema.

Na seção **[!UICONTROL Configurações Gerais]**, você pode escolher as cores primárias e secundárias para os cartões e especificar as propriedades para personalizar o tema.

```
{ 
 "globalCssText":"@import url('https://fonts.googleapis.com/css2?family=Grandstander:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');", 
 "fontNames":"Grandstander", 
 "cardLayout":{ 
 "cardLayoutName":"compact", 
 "cardPrimaryColor":"#376BA4", 
 "cardSecondaryColor":"#F98EB0", 
 "startedStateTextColor":"#ffffff", 
 "continueStateTextColor":"#ffffff", 
 "revisitStateTextColor":"#ffffff", 
 "startedStateColor":"#a0a0a0", 
 "continueStateColor":"#f9a122", 
 "revisitedStateColor":"#7fbc64", 
 "textPrimaryColor":"#ffffff", 
 "textSecondaryColor":"#d93f3f", 
 "navIconColor":"#a0a0a0" 
 } 
}
```

### Configurar os widgets Meus cursos salvos em sites AEM

O widget Meus cursos salvos permite que os alunos visualizem os cursos marcados ou salvos diretamente em suas páginas de aprendizado, fornecendo acesso fácil aos cursos que desejam revisitar ou concluir mais tarde.

Para configurar o widget Meus cursos salvos em sites AEM:

1. Abra os sites de AEM.
2. Abra a página no modo **[!UICONTROL Editar]**.
3. Vá para o **[!UICONTROL Navegador de Componentes]** e adicione o **[!UICONTROL widget Meu Aprendizado]** à página.
4. Selecione o componente e selecione **[!UICONTROL Configurar]**.
5. Selecione **[!UICONTROL Meus cursos salvos]** no menu suspenso em **[!UICONTROL Propriedades]**.
6. Selecione **[!UICONTROL Concluído]** e atualize a página no modo **[!UICONTROL Visualizar]** ou **[!UICONTROL Publish]**.

Os alunos podem exibir os cursos salvos na faixa **[!UICONTROL Salvos por mim]** na página inicial do aluno.A faixa **[!UICONTROL Salvos por mim]** leva os alunos à página do catálogo e exibe o número exato de cursos marcados.

Quando você aplica outro filtro no catálogo, somente os resultados correspondentes a esse filtro são exibidos. Os itens marcados não são incluídos automaticamente.

### Ignorar inscrição do OA de ordem superior

Se a caixa de seleção **Ignorar inscrição do OA de ordem superior** estiver habilitada e um usuário estiver inscrito diretamente em um programa de aprendizado ou certificação, os cursos para essa certificação ou programa de aprendizado aparecerão para o usuário nos widgets.

Se a caixa de seleção estiver desativada, os cursos presentes no Programa de aprendizado ou na Certificação, nos quais o usuário não se inscreveu diretamente, não aparecerão.

![](assets/higher-order-lo.png)

*Marque a caixa de seleção Ignorar inscrição do OA de ordem superior.

A configuração é então aplicada no widget.

### Segurança

Os campos ID do cliente e Segredo do cliente estão adicionados. Além disso, o token de atualização fica mascarado. Depois que um usuário cria a configuração inteira, se ele abrir a configuração novamente para editá-la ou se algum outro usuário abrir essa configuração, o token de atualização será mascarado.
