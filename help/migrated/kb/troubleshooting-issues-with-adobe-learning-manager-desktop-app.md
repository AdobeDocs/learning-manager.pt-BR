---
description: Este documento contém dicas básicas de solução de problemas para solucionar alguns dos problemas típicos que podem ser encontrados ao instalar e usar o aplicativo de desktop Adobe Learning Manager.
jcr-language: en_us
title: Solução de problemas com o aplicativo de desktop Adobe Learning Manager
contentowner: kuppan
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 0%

---



# Solução de problemas com o aplicativo de desktop Adobe Learning Manager

Este documento contém dicas básicas de solução de problemas para solucionar alguns dos problemas típicos que podem ser encontrados ao instalar e usar o aplicativo de desktop Adobe Learning Manager.

## Não consigo fazer o seguinte {#iamunabletodothefollowing}

+++Não consigo baixar o aplicativo de desktop Adobe Learning Manager

1. Verifique sua conexão com a Internet e as configurações do firewall.
1. Em Aprendizado social, clique em **[!UICONTROL Nova publicação]** para criar uma publicação. Se não tiver um painel, primeiro crie um painel.
1. Clique em qualquer uma das seguintes opções de botão da publicação que aparece para criar conteúdo, como Captura de tela, Gravar áudio, Gravar vídeo, Galeria do Learning Manager. Você é redirecionado para a página do aplicativo de desktop Adobe Learning Manager, na qual é possível baixar o aplicativo de desktop Adobe Learning Manager para o seu desktop.
1. Você precisa de uma conta válida do Adobe Learning Manager que tenha o Aprendizado social ativado por seu administrador. Seu administrador também pode ter desativado os downloads por meio do navegador da Web. Entre em contato com o administrador do Adobe para obter mais informações sobre o download do aplicativo de desktop Adobe Learning Manager.

+++

+++Não consigo instalar o aplicativo de desktop Adobe Learning Manager

1. Certifique-se de que seu sistema atende aos requisitos mínimos do sistema. Consulte [Requisitos de sistema do aplicativo de desktop Adobe Learning Manager](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Limpe qualquer instalação anterior do aplicativo de desktop Adobe Learning Manager. Para obter mais informações, consulte  [Como limpar instalações anteriores](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) para obter mais informações.
1. Para erros durante o processo de instalação, consulte [Como encontrar os registros do aplicativo](#howtofindapplicationlogs). Entre em contato com o administrador do aplicativo de desktop Adobe Learning Manager para obter mais ajuda.

+++

+++Não consigo iniciar o aplicativo de desktop Adobe Learning Manager

1. Certifique-se de que o aplicativo de desktop Adobe Learning Manager tenha sido baixado e instalado.
1. Em Aprendizado social, clique em **[!UICONTROL Nova publicação]** (se você não tiver um painel, crie um painel). Clique em qualquer uma das seguintes opções de botão da publicação que aparece para criar conteúdo tal como Captura de tela, Gravar áudio, Gravar vídeo, Galeria do Adobe Learning Manager. Você é redirecionado para a página do aplicativo de desktop Adobe Learning Manager.
1. Caso o aplicativo não seja iniciado, você também pode iniciá-lo no menu Iniciar do Windows ou no Launchpad do Mac OS X.

+++

+++Não consigo fazer logon na minha conta do aplicativo de desktop Adobe Learning Manager

1. Verifique se você está conectado à Internet e se as configurações do firewall não bloqueiam o aplicativo de desktop Adobe Learning Manager.
1. Assegure-se de ter uma conta de aluno válida do Adobe Learning Manager com o Aprendizado social ativado.
1. Se ainda não conseguir fazer logon, saia e reinicie o aplicativo de desktop Adobe Learning Manager e, a seguir, tente novamente.
1. Para obter mais ajuda, entre em contato com seu administrador do Adobe Learning Manager.

+++

+++Não consigo ver minha webcam nem meu microfone listados no aplicativo de desktop Adobe Learning Manager

1. Certifique-se de que a webcam ou o microfone esteja corretamente conectado ao sistema e que esteja funcionando corretamente.
1. Verifique se você instalou os drivers mais recentes para a webcam/microfone. Alguns dispositivos não funcionam corretamente sem drivers dedicados.
1. Redefina as preferências do aplicativo e, a seguir, reinicie o aplicativo de desktop Adobe Learning Manager e tente novamente. Para obter mais informações, consulte [Como redefinir as preferências do aplicativo](#howtoresetapplicationpreferences).
1. Se estiver no Mac OS X Mojave 10.14, conceda as permissões para que o aplicativo de desktop Adobe Learning Manager acesse a webcam/microfone. Para obter mais informações, consulte [Como definir as permissões para a webcam/microfone no OSX Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave).

+++

+++Não consigo publicar minhas publicações a partir do aplicativo de desktop Adobe Learning Manager

1. Assegure-se de ter uma conta de aluno válida do Adobe Learning Manager com o Aprendizado social ativado pelo seu administrador do Adobe Learning Manager.
1. Redefina as preferências do aplicativo e, a seguir, reinicie o aplicativo de desktop Adobe Learning Manager e tente novamente. Para obter mais informações, consulte [Como redefinir as preferências do aplicativo](#howtoresetapplicationpreferences).
1. Para erros durante a publicação, habilite o registro avançado. Para obter mais informações, consulte [Como ativar o registro avançado](#howtoenableadvancedlogging), reinicie o aplicativo de desktop Adobe Learning Manager, refaça as etapas acima que causam o erro. Envie os registros mais recentes do aplicativo ao seu administrador do Adobe Learning Manager para obter ajuda. Para obter mais informações, consulte [Como encontrar os registros do aplicativo](#howtofindapplicationlogs).

+++

+++Não consigo ver nem abrir meus projetos mais antigos

1. Você só pode ver os projetos criados com sua conta do Adobe Learning Manager no mesmo computador em que eles foram criados.
1. Redefina as preferências do aplicativo e, a seguir, reinicie o aplicativo de desktop Adobe Learning Manager e tente novamente. Para obter ajuda, consulte [Como redefinir as preferências do aplicativo](#howtoresetapplicationpreferences).
1. Para erros ao abrir projetos, ative o registro avançado. Para obter mais informações, consulte [Como ativar o registro avançado](#howtoenableadvancedlogging). Reinicie o aplicativo de desktop Adobe Learning Manager e refaça as etapas que causam o erro. Envie os registros mais recentes do aplicativo ao seu administrador do Adobe Learning Manager para obter ajuda. Para obter mais informações, consulte [Como encontrar os registros do aplicativo](#howtofindapplicationlogs).

+++

## Como redefinir as preferências do aplicativo? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Para abrir a caixa de diálogo Executar, pressione a tecla **Windows + R** chaves.
1. Tipo `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` e pressione Enter.
1. Excluir os arquivos nomeados **preferences.json** e **preferences.xml**.

### MAC OS X {#macosx}

1. Abra o Finder.
1. Para abrir o **Ir para** caixa de diálogo da pasta, pressione **Cmd + Shift + G** chaves.
1. Tipo `**~/Library/Application Support/Adobe/Learning Manager 1.0**` e pressione Enter.
1. Excluir os arquivos nomeados **preferences.json** e **preferences.xml**.

## Como encontrar os registros do aplicativo? {#howtofindapplicationlogs}

### Windows {#application-logs}

1. Para abrir a caixa de diálogo Executar, pressione **Windows + R** chaves.
1. Tipo `**%TEMP%\\elthor**` e pressione Enter.
1. Classificar as pastas pelo **Data de modificação** e abra a pasta mais recente. Essa pasta contém os registros mais recentes do aplicativo.

### MAC OS X {#MacOSX-1}

1. Abrir **Finder**.
1. Para abrir o **Ir para a pasta** , pressione **Cmd + Shift + G** chaves.
1. Tipo &quot;**/var/folders**&quot; (sem aspas) e pressione Enter.
1. Procurar por &quot;**elthor**&quot; na barra de pesquisa e abra a pasta.
1. Classifique as pastas por **Data de modificação **e abra a pasta mais recente. Essa pasta contém os registros mais recentes do aplicativo.

## Como ativar o registro avançado? {#howtoenableadvancedlogging}

### Windows {#Windows-1}

1. Para abrir a caixa de diálogo Executar, pressione **Tecla Windows + R**.****
1. Tipo &quot;**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**&quot; (sem aspas) e pressione Enter.****
1. Fazer backup do arquivo **preferences.json** e abra-o em um editor de texto.***
1. Procurar a chave **debugMode** e altere o valor da propriedade desta chave para &quot;**verdadeiro**&quot; (sem aspas).

### MAC OS X {#MacOSX-2}

1. Abra o Finder.
1. Para abrir o **Ir para a pasta** , pressione **Cmd + Shift + G**.
1. Tipo &quot;**~/Library/Application Support/Adobe/Learning Manager 1.0**&quot; (sem aspas) e pressione Enter.
1. Fazer backup do arquivo **preferences.json** e abra-o em um editor de texto.
1. Procurar a chave **debugMode** e altere o valor da propriedade desta chave para &quot;**verdadeiro**&quot; (sem aspas)

## Como definir as permissões para a webcam/microfone no Mac OS X Mojave? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Clique em **[!UICONTROL Preferências do sistema]** ícone no Dock.
1. Clique em **[!UICONTROL Segurança e privacidade]** > **[!UICONTROL Privacidade].**
1. Clique em **[!UICONTROL Opções de webcam e microfone]** e certifique-se de que a caixa de seleção do Adobe Learning Manager esteja marcada. Se não encontrar o Adobe Learning Manager listado, primeiro instale e inicie o aplicativo de desktop Adobe Learning Manager.

## Como limpar o Adobe do Learning Manager para o cache de atualizações no desktop? {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Para abrir a caixa de diálogo Executar, pressione **Tecla Windows + R**.
1. Tipo `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` e pressione Enter.
1. Exclua a pasta denominada **atualizações**.

### MAC OS X {#MacOSX-3}

1. Abra o Finder.
1. Para abrir o **Ir para a pasta** , pressione **Cmd + Shift + G**.
1. Tipo `**~/Library/Application Support/Adobe/Learning Manager 1.0**` e pressione Enter.
1. Exclua a pasta denominada **atualizações**.

## Como limpar o Adobe do Learning Manager para a pasta temp do desktop? {#howtocleanupadobecaptivateprimefordesktoptempfolder}

### Windows {#clean-previous-installation-1}

1. Para abrir a caixa de diálogo Executar, pressione **Tecla Windows + R**.
1. Tipo &quot;**%TEMP%**&quot; (sem aspas) e pressione Enter.
1. Exclua a pasta denominada &quot;**elthor**“.

### MAC OS X {#MacOSX-4}

1. Abra o Finder.
1. Para abrir o **Ir para a pasta** , pressione **Cmd + Shift + G** chaves.
1. Tipo &quot;**/var/folders**&quot; (sem aspas) e pressione Enter.
1. Procurar por &quot;**elthor**&quot; na barra de pesquisa.
1. Exclua a pasta denominada &quot;**elthor**“.

## Como localizar o Adobe Learning Manager para projetos no desktop? {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Para abrir a caixa de diálogo Executar, pressione **Tecla Windows + R**.
1. Tipo &quot;**~/Documents/My Adobe Learning Manager Projetos**&quot; (sem aspas) e pressione Enter.
1. Você ou seu administrador do Adobe Learning Manager pode ter alterado a localização padrão da pasta de projetos. Entre em contato com o administrador para obter mais ajuda para localizar e limpar projetos.

### MAC OS X {#MacOSX-5}

1. Abra o Finder.
1. Para abrir o **Ir para a pasta** , pressione **Cmd + Shift + G** chaves.
1. Tipo &quot;**~/Documents/My Adobe Learning Manager Projetos**&quot; (sem aspas) e pressione Enter.

   Você ou seu administrador do Adobe Learning Manager pode ter alterado a localização padrão da pasta de projetos. Entre em contato com o administrador para obter mais ajuda para localizar e limpar projetos.

## Como limpar as instalações anteriores do aplicativo de desktop Adobe Learning Manager? {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Para abrir o **Caixa de diálogo Executar,** pressione **Teclas Windows + R**.
1. Digite regedit e pesquise &quot;**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**&quot; (sem aspas) ou &quot;**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**&quot; (sem aspas) e pressione Enter.
1. Localize a pasta denominada Adobe Learning Manager e a instalação anterior. Exclua a entrada do registro.  É possível encontrar a tecla pressionando a tecla F3.

### MAC OS X {#MacOSX-6}

Mova os arquivos do seguinte caminho &quot;**/Aplicativos/Adobe Learning Manager/Usuários/Compartilhado/Adobe/Learning Manager Assets/1.0**&quot; para a lixeira e depois esvazie a lixeira.
