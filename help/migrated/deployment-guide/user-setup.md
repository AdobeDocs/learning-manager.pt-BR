---
jcr-language: en_us
title: Configurar usuários no Learning Manager
contentowner: shhivkum
preview: true
source-git-commit: 0fabd369e70e15ba22fead0177a24aafd851d88d
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 63%

---



# Configurar usuários no Learning Manager

## Usuários internos e externos {#internalandexternalusers}

Em qualquer LMS, incluindo o Learning Manager, gerenciar usuários é um aspecto importante. O Learning Manager permite classificar usuários como internos e externos. Usuários internos são aqueles usuários que pertencem a uma organização ou grupo específico. Geralmente, os usuários em uma corporação são usuários internos. Esses usuários têm objetos de aprendizado específicos com prazos específicos, conforme atribuídos por seus gerentes ou pelo administrador.

Por outro lado, os usuários externos geralmente são usuários temporários de uma conta específica do Learning Manager. Esses usuários podem acessar objetos de aprendizado específicos clicando em um link externo temporário que recebem por e-mail. Os perfis de usuário externos geralmente têm uma data de expiração. Por exemplo, uma organização que realiza certificações para Java pode ter qualquer usuário que faça logon temporariamente em cursos relevantes e, em seguida, tente a certificação. Normalmente, os treinamentos e cursos em sala de aula destinados a usuários externos também têm capacidade limitada.

Leia para saber como adicionar usuários internos e usuários externos no Learning Manager.

## Configurar usuários externos {#setupexternalusers}

Como administrador, você pode desejar adicionar usuários externos, como funcionários de organizações parceiras, à sua conta do Learning Manager. Para adicionar usuários externos:

1. Na página de logon do **[!UICONTROL **Administrador**]**&#x200B;clique em **[!UICONTROL **Usuários**]**&#x200B;no painel de navegação esquerdo.
1. Na página **[!UICONTROL **Usuários**]**&#x200B;s, clique em **[!UICONTROL **Externo**]**&#x200B;no painel de navegação esquerdo. O sistema exibe a página Usuários externos com uma lista de usuários externos (se aplicável).
1. Clique em **[!UICONTROL **Adicionar**]**&#x200B;no canto superior direito da página.

   ![](assets/set-up-external-users-step3.png)

1. Na caixa de diálogo pop-up **[!UICONTROL **Adicionar usuário**]**&#x200B;os seguintes campos são obrigatórios:

   * **[!UICONTROL **Nome do Perfil**:]**&#x200B;Especifique o nome do perfil externo que você está criando.
   * **[!UICONTROL **&#x200B; Email do gerente &#x200B;**:]** especifique o endereço de email do gerente para o usuário externo.
   * **[!UICONTROL **&#x200B; Vagas atribuídas &#x200B;**:]** especifique o número de alunos que podem se inscrever no curso.
   * **[!UICONTROL **&#x200B; Expiração &#x200B;**:]** especifique a data de expiração após a qual um usuário externo não pode registrar ou consumir o curso.

1. Clique em **[!UICONTROL **&#x200B; Configurações Avançadas &#x200B;**.]**
1. Opcionalmente, defina as seguintes opções ao criar um perfil externo:

   * **[!UICONTROL **&#x200B; Adicionar imagem &#x200B;**:]** arraste e solte a imagem desejada. Esta imagem é exibida na página do aluno para usuários.
   * **[!UICONTROL **&#x200B; Requisito de Logon &#x200B;**:]** especifique o número de dias em que o usuário precisa fazer logon. Se o usuário externo exceder esse período de logon, o aluno não poderá acessar ou consumir o objeto de aprendizado.
   * **[!UICONTROL **&#x200B; Domínios permitidos &#x200B;**:]** Especifique os domínios separados por vírgula. Somente os usuários com os domínios especificados podem se registrar na conta.
   * **[!UICONTROL **&#x200B; Verificação de email necessária &#x200B;**:]** Marque esta caixa de seleção se quiser que um email de verificação seja enviado aos usuários



1. Clique em **[!UICONTROL Salvar.]**



   ![](assets/set-up-external-users-step7.png)

   Uma caixa de diálogo suspensa com o URL é exibida. Você pode copiar esse URL e enviá-lo aos usuários externos. Por padrão, um e-mail com esse URL é enviado ao usuário.

1. À medida que você adiciona perfis externos, eles são exibidos na **[!UICONTROL **&#x200B; página Usuários externos &#x200B;**(**&#x200B; Administrador &#x200B;**>**&#x200B; Usuários &#x200B;**>**&#x200B; Externos &#x200B;**).]** O limite de vagas, a data de expiração e o requisito de logon também são exibidos para esses usuários.
1. Para editar as configurações de um usuário externo a qualquer momento, clique no nome do usuário. A caixa de diálogo **[!UICONTROL Editar inscrição externa]** é exibida. Modifique as configurações e clique em **[!UICONTROL **&#x200B; Salvar &#x200B;**.]**
1. Você também pode reenviar o e-mail de boas-vindas ou copiar o URL a qualquer momento clicando nos ícones de e-mail/copiar URL ao lado do perfil externo.

   ![](assets/set-up-external-users-step10.png)

## Pausar o perfil de usuário externo {#pausetheexternaluserprofile}

Depois de adicionar um grupo de usuários externo ao Learning Manager, você também pode pausar o processo de registro de usuários externos. Quando pausado, o processo de registro dos usuários externos fica bloqueado. No entanto, esse processo funciona apenas para usuários que ainda não aceitaram o convite de registro.

Para pausar os grupos de usuários externos, clique em **[!UICONTROL **Ações**]&#x200B;**no canto superior direito da página e escolha &#x200B;** [!UICONTROL Pausar]**.

## Retomar perfil de usuário externo {#resumeexternaluserprofile}

A qualquer momento, você pode revogar o bloqueio (pausa) selecionando a opção Retomar. Clique em **[!UICONTROL **Ações**]&#x200B;**no canto superior direito da página e escolha &#x200B;** [!UICONTROL Retomar]**.

**[!UICONTROL Estados de usuário externo]**

No Learning Manager, os seguintes estados são aplicáveis a usuários externos:

* **Estado inativo** - neste estado, o registro de usuários externos expirou. Administradores definem a data de expiração dos usuários externos no fluxo de trabalho de adição de usuário.
* **Estado ativo** - neste estado, usuários externos podem se registrar no aplicativo Learning Manager e também fazer logon no aplicativo.
* **Pausa** - neste estado, o processo de registro para usuários externos está bloqueado. No entanto, usuários existentes podem continuar a fazer logon.

## Configurar usuários internos {#setupinternalusers}

Como administrador, você pode querer configurar usuários para sua empresa ou organização. Esses usuários também são chamados de usuários internos. Os usuários internos podem fazer logon no aplicativo usando o logon único ou o Adobe ID. Esses usuários podem acessar e consumir os objetos de aprendizado de acordo com seus requisitos. Há três maneiras possíveis de configurar usuários internos para uma organização:

* Adicionar usuários em massa usando um CSV
* Adicionar usuários por meio do autorregistro
* Adicionar um único usuário interno



## Adicionar usuários usando um arquivo CSV {#addingusersusingacsvfile}

Você pode escolher esse método para adicionar usuários internos se o número de usuários for grande. Ao usar um CSV para adicionar usuários pela primeira vez, você deve mapear o conteúdo dos dados csv para os rótulos de aplicativos. Subsequentemente, quando você adicionar novos usuários ou atualizar os dados do usuário, o mesmo mapeamento será mantido. Para adicionar usuários internos em massa:

1. Na página **[!UICONTROL Início do Administrador]**, clique em **[!UICONTROL **Usuários**]**&#x200B;no painel de navegação esquerdo.
1. Clique em **[!UICONTROL **&#x200B; Adicionar &#x200B;**>**&#x200B; Carregar um CSV &#x200B;**.]**
1. Na caixa de diálogo pop-up, clique em **[!UICONTROL **&#x200B; Importar &#x200B;**.]**
1. Navegue até o local onde você salvou seu arquivo CSV. Clique em **[!UICONTROL Abrir]**.
1. Importe o arquivo CSV e mapeie o conteúdo do arquivo CSV com os rótulos do aplicativo. Essa etapa é aplicável somente quando você carrega o arquivo CSV pela primeira vez.
1. Clique em **[!UICONTROL **Salvar**]**&#x200B;para salvar o mapeamento.
1. Clique em **[!UICONTROL **Adicionar**]**&#x200B;para carregar o arquivo CSV que já está mapeado para os dados do aplicativo.

### Considerações ao criar o arquivo CSV para carregar: {#considerationswhencreatingthecsvfileforupload}

Ao criar o arquivo CSV para fazer upload de usuários internos, veja a seguir alguns dos campos obrigatórios para os quais você deve inserir dados: Nome do Funcionário, E-mail do Funcionário, Perfil ou Designação do Funcionário e Hierarquia de Gerentes.

O nome e o e-mail de cada funcionário podem ser mapeados diretamente para os dados do aplicativo. Observe que você deve especificar um e-mail especificado no arquivo CSV como o E-mail do gerente. Você pode definir a ID do gerente ao criar o arquivo CSV ou pode especificar a ID de e-mail correspondente à ID do gerente ao carregar o arquivo CSV.

***Antes de adicionar uma ID como ID de Gerente de um funcionário, verifique se o Gerente está adicionado como um funcionário no arquivo CSV.***

***Verifique se não há espaços extras entre as entradas para carregar o arquivo CSV com êxito.***

Veja uma imagem de exemplo de um arquivo CSV aqui:

![](assets/considerations-whencreatingthecsvfileforupload.png)

Para baixar um arquivo CSV de exemplo, baixe `<give link to zip file>`.

<!--Zip file reference, no source file-->

### Configurando o usuário raiz {#settinguprootuser}

Automatizando a importação em massa de usuários.

## Adicionar usuários por meio do autorregistro {#addingusersthroughselfregistration}

Além de adicionar usuários internos em massa, você também pode adicionar usuários por autorregistro. Você pode usar o autorregistro para permitir que os funcionários se registrem como alunos na sua conta do Learning Manager. Quando você cria um perfil de autorregistro, um URL exclusivo é criado. Compartilhe este URL com o funcionário para permitir que ele se registre no Learning Manager.

1. Na página **[!UICONTROL inicial do administrador]**, clique em **[!UICONTROL Usuários]** no painel de navegação à esquerda.
1. Clique em **[!UICONTROL **&#x200B; Adicionar &#x200B;**>**&#x200B; Autorregistro &#x200B;**.]**

   ![](assets/adding-users-throughself-registration-step2.png)

1. Na caixa de diálogo suspensa **[!UICONTROL Adicionar usuário]**, especifique o nome do funcionário no campo **[!UICONTROL Nome do perfil]**.
1. No campo **[!UICONTROL Nome do Gerente]**, insira o nome do gerente do funcionário.
1. Opcionalmente, você pode adicionar a imagem de perfil do funcionário usando o campo **[!UICONTROL Adicionar imagem]**.
1. Clique em **[!UICONTROL Salvar]**.

   ![](assets/adding-users-throughself-registration-step6.png)

   O sistema exibe outra caixa de diálogo suspensa com a mensagem de que o perfil foi criado com êxito. Um URL exclusivo também é gerado nessa caixa de diálogo.

1. Compartilhe esse URL com o funcionário para permitir que ele se registre como aluno.

   ![](assets/adding-users-throughself-registration-step7.png)

## Adicionar usuários únicos no Learning Manager {#addsingleusersincaptivateprime}

Adicionar usuários únicos é o terceiro método pelo qual você pode adicionar usuários internos à sua conta. Quando você deseja adicionar alguns usuários, esse procedimento é ideal. Adicionar um usuário único

1. Na página **[!UICONTROL inicial do administrador]**, clique em **[!UICONTROL Usuários]** no painel de navegação à esquerda.
1. Clique em **[!UICONTROL **&#x200B; Adicionar &#x200B;**>**&#x200B; Usuário único &#x200B;**.]**



1. Na caixa de diálogo suspensa Adicionar usuário, especifique os seguintes detalhes para usuários:

   * **[!UICONTROL Nome]** **[!UICONTROL :]** especifique o nome do funcionário ou do usuário interno. Este campo é obrigatório.

   * **[!UICONTROL Email]** **[!UICONTROL :]** especifique a ID de email do funcionário. Este campo é obrigatório.

   * **[!UICONTROL Perfil]** **[!UICONTROL :]** especifique a designação ou o cargo do funcionário.

   * **[!UICONTROL **&#x200B; Nome do gerente &#x200B;**:]** Especifique o nome do gerente. O gerente já deve estar adicionado ao banco de dados para ser especificado aqui.
   * **[!UICONTROL **&#x200B; DOJ &#x200B;**:]** especifique a data de ingresso do funcionário.
   * **[!UICONTROL **Local**:]**&#x200B;Especifique o local do funcionário. Por exemplo, se sua organização estiver em várias localidades geográficas, especifique a localidade onde o funcionário está localizado.



   ![](assets/add-single-usersincaptivateprime-step3.png)

1. Clique em **[!UICONTROL Adicionar]**.
1. O sistema exibe uma mensagem informando que o usuário foi adicionado com êxito. O usuário recebe um link de verificação na ID de e-mail especificada. O usuário pode clicar neste link para ativar sua conta e começar a acessar o Learning Manager.

   ![](assets/add-single-usersincaptivateprime-step5.png)

## Gerenciar grupos de usuários no Learning Manager {#managingusergroupsincaptivateprime}

O grupo de usuários é apenas um conjunto de usuários pertencentes a uma categoria definida. Como administrador, você pode usar grupos de usuários para selecionar alunos rapidamente com base em seus atributos. Além disso, você pode atribuir rapidamente logotipos ou catálogos ao grupo de usuários e gerar relatórios personalizados sobre seu progresso.

Há dois tipos de grupos de usuários no Learning Manager: Personalizados e Gerados automaticamente. Quando você adiciona alunos à sua conta, alguns grupos padrão são criados automaticamente com base nas funções e propriedades dos usuários na sua conta. Esses grupos são os gerados automaticamente. Por exemplo, um grupo com todos os alunos ou todos os autores.

***Não é possível editar o nome e a descrição de grupos gerados automaticamente.***

Para exibir os grupos de usuários gerados automaticamente no Learning Manager, clique no painel esquerdo **[!UICONTROL Gerados automaticamente]**. O aplicativo exibe uma lista de todos os grupos de usuários gerados automaticamente que estão disponíveis para sua conta.

Você também pode criar grupos personalizados com uma lista selecionada de usuários no Learning Manager. Os grupos personalizados permitem especificar um nome, uma descrição e os atributos do grupo de usuários. Os grupos personalizados criados no Learning Manager são dinâmicos por natureza. Ou seja, se novos usuários forem adicionados com atributos semelhantes, eles serão adicionados automaticamente a esses grupos de usuários.

## Criar grupos de usuários personalizados {#createcustomusergroups}

1. Na página inicial do administrador do Learning Manager, clique em **[!UICONTROL Usuários]**.
1. Na página Grupos de usuários personalizados, clique em **[!UICONTROL **Adicionar**]**&#x200B;no canto superior direito da página.

   O sistema exibe a caixa de diálogo **[!UICONTROL Adicionar grupo de usuários]**.

   ![](assets/creating-custom-usergroups.png)

1. Especifique o nome e a descrição do seu grupo de usuários. Por exemplo, Usuários desenvolvedores, que inclui usuários da equipe de desenvolvimento de produtos.
1. Adicione usuários ao grupo de usuários personalizado inserindo o nome de usuário ou o perfil do usuário no campo **[!UICONTROL **&#x200B; Adicionar usuários &#x200B;**.]**
1. Para adicionar mais usuários ao grupo personalizado, clique em **[!UICONTROL **&#x200B; Adicionar Mais Usuários &#x200B;**.]**
1. Depois de adicionar todos os usuários, clique em **[!UICONTROL Salvar]**&#x200B;para salvar o grupo de usuários personalizado.

