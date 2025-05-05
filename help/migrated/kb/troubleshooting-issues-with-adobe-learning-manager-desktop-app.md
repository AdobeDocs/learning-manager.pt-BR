---
description: Este documento contém dicas básicas de solução de problemas para solucionar alguns dos problemas típicos que podem ser encontrados ao instalar e usar o aplicativo de desktop Adobe Learning Manager.
jcr-language: en_us
title: Solução de problemas com o aplicativo Adobe Learning Manager para desktop
contentowner: kuppan
exl-id: 68d40a52-e048-43af-a7aa-917b569b583d
source-git-commit: a0c01c0d691429bd66a3a2ce4cfc175ad0703157
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 54%

---

# Solução de problemas com o aplicativo Adobe Learning Manager para desktop

Este documento contém dicas básicas de solução de problemas para solucionar alguns dos problemas típicos que podem ser encontrados ao instalar e usar o aplicativo de desktop Adobe Learning Manager.

## Não consigo fazer o seguinte {#iamunabletodothefollowing}

+++Não consigo baixar o aplicativo de desktop da Adobe Learning Manager

1. Verifique a conexão com a Internet e as configurações do firewall.
1. Em Aprendizado social, clique em **[!UICONTROL Nova publicação]** para criar uma publicação. Se não tiver um painel, primeiro crie um painel.
1. Clique em qualquer uma das seguintes opções de botão da publicação que aparece para criar conteúdo tal como Captura de tela, Gravar áudio, Gravar vídeo, Galeria do Learning Manager. Você é redirecionado para a página do aplicativo de desktop Adobe Learning Manager, na qual é possível baixar o aplicativo de desktop Adobe Learning Manager para o seu desktop.
1. Você precisa ter uma conta válida do Adobe Learning Manager que tenha o Aprendizado social ativado por seu administrador. Seu administrador pode também ter desativado os downloads através do navegador da Web. Contate o administrador do Adobe Learning Manager para obter mais informações sobre o download do aplicativo de desktop Adobe Learning Manager.

+++

+++Não consigo instalar o aplicativo de desktop da Adobe Learning Manager

1. Verifique se seu sistema atende aos requisitos mínimos do sistema. Consulte [Requisitos de sistema para o aplicativo de desktop Adobe Learning Manager](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Limpe quaisquer instalações anteriores do aplicativo de desktop Adobe Learning Manager. Para obter mais informações, consulte [Como limpar instalações anteriores](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) para obter mais informações.
1. Para erros durante o processo de instalação, consulte [Como localizar logs de aplicativos](#howtofindapplicationlogs). Entre em contato com seu administrador do aplicativo de desktop Adobe Learning Manager para obter mais ajuda.

+++

+++Não consigo iniciar o aplicativo de desktop da Adobe Learning Manager

1. Assegure-se de que o aplicativo de desktop Adobe Learning Manager tenha sido baixado e instalado.
1. Em Aprendizado social, clique em **[!UICONTROL Nova publicação]** (se não tiver um painel, primeiro crie um painel). Clique em qualquer uma das seguintes opções de botão da publicação que aparece para criar conteúdo tal como Captura de tela, Gravar áudio, Gravar vídeo, Galeria do Adobe Learning Manager. Você é redirecionado para a página do aplicativo de desktop Adobe Learning Manager.
1. Caso o aplicativo não se inicie, você também pode iniciá-lo no menu Início do Windows ou no Launchpad do Mac OS X.

+++

+++Não consigo fazer logon na minha conta do aplicativo de desktop da Adobe Learning Manager

1. Verifique se você está conectado à Internet e se suas configurações de firewall não bloqueiam o aplicativo de desktop Adobe Learning Manager.
1. Assegure-se de ter uma conta de aluno válida do Adobe Learning Manager com o Aprendizado social ativado.
1. Se ainda não conseguir fazer logon, saia e reinicie o aplicativo de desktop Adobe Learning Manager e, a seguir, tente novamente.
1. Entre em contato com seu administrador do aplicativo de desktop Adobe Learning Manager para obter mais ajuda.

+++

+++Não consigo ver minha webcam nem meu microfone listados no aplicativo de desktop da Adobe Learning Manager

1. Assegure-se de que a webcam ou o microfone esteja apropriadamente conectado ao sistema e que esteja funcionando corretamente.
1. Verifique se você instalou os drivers mais recentes para a webcam/microfone. Alguns dispositivos não funcionam corretamente sem drivers dedicados.
1. Redefina as preferências do aplicativo e, a seguir, reinicie o aplicativo de desktop Adobe Learning Manager e tente novamente. Para obter mais informações, consulte [Como redefinir as preferências do aplicativo](#howtoresetapplicationpreferences).
1. Se estiver no Mac OS X Mojave 10.14, conceda as permissões para que o aplicativo de desktop Adobe Learning Manager acesse a webcam/microfone. Para obter mais informações, consulte [Como definir as permissões para a webcam/microfone no OSX Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave).

+++

+++Não consigo publicar minhas publicações a partir do aplicativo de desktop da Adobe Learning Manager

1. Assegure-se de ter uma conta de aluno válida do Adobe Learning Manager com o Aprendizado social ativado pelo seu administrador do Adobe Learning Manager.
1. Redefina as preferências do aplicativo e, a seguir, reinicie o aplicativo de desktop Adobe Learning Manager e tente novamente. Para obter mais informações, consulte [Como redefinir as preferências do aplicativo](#howtoresetapplicationpreferences).
1. Para erros durante a publicação, habilite o registro avançado. Para obter mais informações, consulte [Como ativar o registro avançado](#howtoenableadvancedlogging), reinicie o aplicativo de desktop Adobe Learning Manager, refaça as etapas acima que causam o erro. Envie os registros mais recentes do aplicativo ao seu administrador do Adobe Learning Manager para obter ajuda. Para obter mais informações, consulte [Como encontrar os registros do aplicativo](#howtofindapplicationlogs).

+++

+++Não consigo ver nem abrir meus projetos mais antigos

1. Você pode ver somente os projetos criados com sua conta do Adobe Learning Manager no mesmo computador no qual eles foram criados.
1. Redefina as preferências do aplicativo e, a seguir, reinicie o aplicativo de desktop Adobe Learning Manager e tente novamente. Para obter Ajuda, consulte [Como redefinir as preferências do aplicativo](#howtoresetapplicationpreferences).
1. Para erros ao abrir projetos, ative o registro avançado. Para obter mais informações, consulte [Como habilitar o log avançado](#howtoenableadvancedlogging). Reinicie o aplicativo de desktop Adobe Learning Manager e refaça as etapas que causam o erro. Envie os registros mais recentes do aplicativo ao seu administrador do Adobe Learning Manager para obter ajuda. Para obter mais informações, consulte [Como encontrar os registros do aplicativo](#howtofindapplicationlogs).

+++

## Como redefinir as preferências do aplicativo? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Para abrir a caixa de diálogo Executar, pressione as teclas **Windows + R**.
1. Digite `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` e pressione Enter.
1. Exclua os arquivos denominados **preferences.json** e **preferences.xml**.

### Mac OS X {#macosx}

1. Abra o Finder.
1. Para abrir a caixa de diálogo de pasta **Ir para**, pressione as teclas **Cmd + Shift + G**.
1. Digite `**~/Library/Application Support/Adobe/Learning Manager 1.0**` e pressione Enter.
1. Exclua os arquivos denominados **preferences.json** e **preferences.xml**.

## Como encontrar os registros do aplicativo? {#howtofindapplicationlogs}

### Windows {#application-logs}

1. Para abrir a caixa de diálogo Executar, pressione as teclas **Windows + R**.
1. Digite `**%TEMP%\\elthor**` e pressione Enter.
1. Classifique as pastas pela **Data de modificação** e abra a pasta mais recente. Essa pasta contém os registros mais recentes do aplicativo.

### Mac OS X {#MacOSX-1}

1. Abra o **Finder**.
1. Para abrir a caixa de diálogo **Ir para Pasta**, pressione as teclas **Cmd + Shift + G**.
1. Digite “**/var/folders**” (sem aspas) e pressione Enter.
1. Pesquise por “**elthor**” na barra de pesquisa e abra a pasta.
1. Classifique as pastas por **Data de modificação &#x200B;** e abra a pasta mais recente. Essa pasta contém os registros mais recentes do aplicativo.

## Como ativar o registro avançado? {#howtoenableadvancedlogging}

### Windows {#Windows-1}

1. Para abrir a caixa de diálogo Executar, pressione a tecla **Windows + R**.**&#x200B;**
1. Digite “**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**” (sem aspas) e pressione Enter.**&#x200B;**
1. Faça backup do arquivo **preferences.json** e, a seguir, abra-o em um editor de texto.**&#x200B;**
1. Procure a chave **debugMode** e altere a propriedade value dessa chave para “**true**” (sem aspas).

### Mac OS X {#MacOSX-2}

1. Abra o Finder.
1. Para abrir a caixa de diálogo **Ir para Pasta**, pressione **Cmd + Shift + G**.
1. Digite “**~/Library/Application Support/Adobe/Learning Manager 1.0**” (sem aspas) e pressione Enter.
1. Faça backup do arquivo **preferences.json** e, a seguir, abra-o em um editor de texto.
1. Procure a chave **debugMode** e altere a propriedade value dessa chave para “**true**” (sem aspas)

## Como definir as permissões para a webcam/microfone no Mac OS X Mojave? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Clique no ícone **[!UICONTROL Preferências do Sistema]** no Dock.
1. Clique em **[!UICONTROL Segurança e Privacidade]** > **[!UICONTROL Privacidade].**
1. Clique em **[!UICONTROL Opções de webcam e microfone]** e assegure-se de que a caixa de seleção do Adobe Learning Manager esteja selecionada. Se o Adobe Learning Manager não estiver na lista, primeiro instale e inicie o aplicativo de desktop Adobe Learning Manager.

## Como limpar o Adobe Learning Manager para o cache de atualizações no desktop? {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Para abrir a caixa de diálogo Executar, pressione a **tecla Windows + R**.
1. Digite `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` e pressione Enter.
1. Exclua a pasta denominada **atualizações**.

### Mac OS X {#MacOSX-3}

1. Abra o Finder.
1. Para abrir a caixa de diálogo **Ir para Pasta**, pressione **Cmd + Shift + G**.
1. Digite `**~/Library/Application Support/Adobe/Learning Manager 1.0**` e pressione Enter.
1. Exclua a pasta denominada **atualizações**.

## Como limpar o Adobe Learning Manager para a pasta temp do desktop? {#howtocleanupadobecaptivateprimefordesktoptempfolder}

### Windows {#clean-previous-installation-1}

1. Para abrir a caixa de diálogo Executar, pressione a **tecla Windows + R**.
1. Digite “**%TEMP%**” (sem aspas) e pressione Enter.
1. Exclua a pasta denominada “**elthor**”.

### Mac OS X {#MacOSX-4}

1. Abra o Finder.
1. Para abrir a caixa de diálogo **Ir para Pasta**, pressione as teclas **Cmd + Shift + G**.
1. Digite “**/var/folders**” (sem aspas) e pressione Enter.
1. Pesquise por “**elthor**” na barra de pesquisa.
1. Exclua a pasta denominada “**elthor**”.

## Como localizar o Adobe Learning Manager para projetos no desktop? {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Para abrir a caixa de diálogo Executar, pressione a **tecla Windows + R**.
1. Digite “**~/Documents/My Adobe Learning Manager Projects**” (sem aspas) e pressione Enter.
1. Você ou seu administrador do Adobe Learning Manager pode ter alterado a localização padrão da pasta de projetos. Entre em contato com o administrador para obter mais ajuda para localizar e limpar projetos.

### Mac OS X {#MacOSX-5}

1. Abra o Finder.
1. Para abrir a caixa de diálogo **Ir para Pasta**, pressione as teclas **Cmd + Shift + G**.
1. Digite “**~/Documents/My Adobe Learning Manager Projects**” (sem aspas) e pressione Enter.

   Você ou seu administrador do Adobe Learning Manager pode ter alterado a localização padrão da pasta de projetos. Entre em contate com seu administrador para obter mais ajuda para localizar e limpar projetos.

## Como limpar as instalações anteriores do aplicativo de desktop Adobe Learning Manager? {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Para abrir a caixa de diálogo **Executar,** pressione **as teclas do Windows + R**.
1. Digite regedit e pesquise “**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**” (sem aspas) ou “**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**” (sem aspas) e pressione Enter.
1. Localize a pasta denominada Adobe Learning Manager e a instalação anterior. Exclua a entrada do registro.  É possível encontrar a tecla pressionando a tecla F3.

### Mac OS X {#MacOSX-6}

Mova os arquivos do seguinte caminho “**/Applications/Adobe Learning Manager/Users/Shared/Adobe/Learning Manager Assets/1.0**” para a lixeira e, a seguir, esvazie a lixeira.
