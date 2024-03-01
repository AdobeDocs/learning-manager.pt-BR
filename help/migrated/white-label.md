---
jcr-language: en_us
title: Descontinuações de API no Adobe Learning Manager
description: A rotulagem branca é uma prática de mudar a identidade visual de um aplicativo ou serviço com sua própria marca e personalizá-lo como se você fosse o criador original. No Adobe Learning Manager, você pode aplicar rótulos brancos ao aplicativo para dispositivos móveis, para que possa renomear a identidade visual do aplicativo e disponibilizá-lo aos usuários com sua própria marca.
contentowner: saghosh
source-git-commit: 7bd9877aa32c78988a5195116d2a0f25ded05c90
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---


# Rotulagem de branco no aplicativo Adobe Learning Manager para dispositivos móveis

O aplicativo móvel Adobe Learning Manager agora é compatível com rótulos brancos, o que significa que agora você pode liberar o aplicativo com sua própria marca.

## Como você deve começar a se preparar para iniciar seu aplicativo com rótulo branco

Para implantar e gerenciar seu próprio aplicativo com rótulo branco, siga as etapas:

1. Prepare os ativos (como imagem da tela inicial) e o texto para que ambos possam ser usados no aplicativo e na descrição na app/play store.

1. Atribua um recurso técnico capaz de:

* Gerando os arquivos de certificado de notificação por push.
* Assinar os binários do aplicativo fornecidos pela equipe do ALM.
* Carregando e gerenciando o processo de publicação. O processo de publicação requer comunicação entre seu gerente de aplicativos e as equipes da App/Play Store para que o aplicativo esteja em conformidade com todas as diretrizes de publicação. No ALM, você receberá um binário de aplicativo totalmente compatível.

## Visão geral

A rotulagem branca é uma prática de mudar a identidade visual de um aplicativo ou serviço com sua própria marca e personalizá-lo como se você fosse o criador original. No Adobe Learning Manager, você pode aplicar rótulos brancos ao aplicativo para dispositivos móveis, para que possa renomear a identidade visual do aplicativo e disponibilizá-lo aos usuários com sua própria marca.

## O que pode ser personalizado

O seguinte pode ser personalizado:

### Campos

<table>

    <tbody>

    <tr>

   <td>

    <p>ID da conta</p></td>

   <td>

    <p>A ID da sua conta. Observe que o aplicativo com rótulo branco não estará acessível aos alunos que pertencem a qualquer outra conta.</p></td>

  </tr>

  <tr>

   <td>

    <p>IDs de conta adicionais</p></td>

   <td>

    <p>Adicione várias contas (subdomínios), se desejar. Adicione os subdomínios como separados por vírgula sem espaços. Por exemplo, acc01,acc02,acc03 e assim por diante.<br> <b>Observação:</b> Você precisa adicionar a ID da conta ao especificar os subdomínios.</br> </p></td>

  </tr>

  <tr>

  <td>

  <p>Nome do aplicativo</p></td>

  <td>

  <p>O nome que você deseja usar para o aplicativo.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nome curto do aplicativo</p></td>

  <td>

  <p>Nos casos em que o nome do aplicativo for longo, dê ao aplicativo um nome curto que apareça no dispositivo.</p></td>

  </tr>

   <tr>

  <td>

  <p>Nome do aplicativo interno</p></td>

  <td>

  <p>O nome com o qual o sistema operacional identifica o aplicativo. O formato usado normalmente é: com.company-name.product-name.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nome do aplicativo interno - iOS</p></td>

  <td>

  <p>Nomeie o aplicativo de maneira diferente se os usuários estiverem no iOS. Recomendamos usar o mesmo nome para o iOS e o Android.</p></td>

  </tr>

  <tr>

  <td>

  <p>Ícone de aplicativo</p></td>

  <td>

  <p>O ícone do aplicativo é png. Este ícone é exibido no seu aplicativo. O formato para o nome é account-id_appIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>Tela inicial do aplicativo</p></td>

  <td>

  <p>Para a tela inicial do seu aplicativo, forneça uma imagem (png) que será exibida quando os usuários iniciarem o aplicativo. O formato para o nome é account-id_splashIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>ID do cliente e segredo do cliente</p></td>

  <td>

  <p>O administrador de integração da sua conta fornece os detalhes ao registrar o aplicativo. O administrador de integração deve usar o seguinte: * learner:read,learner:write as role * internal app name://redirect as redirect URL

  </p></td>

  </tr>

  <tr>

  <td>

  <p>Logotipo da conta</p></td>

  <td>

  <p>O URL que hospeda o logotipo da sua organização. Forneça um link cpcontents como o logotipo da conta. O URL precisa ser codificado na Web.</p></td>

  </tr>

  <tr>

  <td>

  <p>ID da loja de aplicativos do aplicativo (iOS)</p></td>

  <td>

  <p>A ID necessária para implementar a atualização forçada. O aplicativo precisa saber que o aluno deve ser redirecionado para a loja de aplicativos para atualizar o aplicativo.</p></td>

  </tr>

   <tr>

  <td>

  <p>ID da Google Play Store para o aplicativo (Android)</p></td>

  <td>

  <p>A ID necessária para implementar a atualização forçada.</p></td>

  </tr>

  <tr>

  <td>

  <p>Nome do host para deep linking</p></td>

  <td>

  <p>Para hospedar os links profundos, use o learningmanager. Se quiser usar outro URL de nome de host como um deep link, forneça o URL do host. Por exemplo, learningmanager.adobe.com.</p></td>

  </tr>

    </tbody>

</table>


#### Atualizar associação de site

Se estiver usando um domínio personalizado ou o learningmanager\*.adobe.com como host, você não precisa fazer nada. No entanto, se você usar uma solução personalizada ou um nome de host específico para os URLs, adicione os arquivos de associação de site.

Consulte os links a seguir para obter mais informações:

- [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)

- [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Gerar certificado de notificações por push

### Certificado de notificações por push no iOS

No desenvolvimento de aplicativos da iOS, um certificado de notificação por push é uma credencial criptográfica emitida pela Apple que permite que um servidor envie notificações por push com segurança para um dispositivo iOS por meio do Serviço de Notificação por Push (APNs) da Apple.

O certificado garante a comunicação segura entre o servidor (ou provedor) e os APNs da Apple ao enviar notificações push para dispositivos iOS.

Tanto o Android quanto o iOS usam o Firebase Cloud Messaging (FCM) como o serviço de envio de notificações por push para dispositivos.

### Como gerar o certificado no iOS

Siga o procedimento:

1. Gere ou baixe o **Certificado de notificação por push** e a chave privada (.p12). Para obter mais informações, consulte o [Documento do desenvolvedor do Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Instale o arquivo p12 após o download do arquivo. Use a senha para instalar no **Acesso às Chaves**.

1. Navegue até **Meus certificados** e exporte o certificado. Certifique-se de selecionar o tipo MIME .cer.

1. Assim que o arquivo p12 e o arquivo cer estiverem disponíveis, execute os seguintes comandos:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Se você puder se conectar ao servidor, o certificado que você criou será válido. No arquivo myapnappkey.pem, copie os valores do certificado e da chave privada.

1. Entre em contato com a equipe de CSM e obtenha os arquivos adicionados aos serviços SNS no AWS. Os usuários terão que obter a entrada registrada no serviço SNS para a notificação por push, que exigirá que eles compartilhem os certificados gerados acima para validação.

>[!NOTE]
>
>Para Android, o usuário precisa fornecer a chave do servidor do projeto Firebase criado para Android para adicionar a entrada no serviço SNS.


## Adicionar o projeto ao Firebase

### Android

[Adicionar o projeto](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) no Firebase e recupere o ***google-services.json*** arquivo.

### iOS

[Adicionar o projeto](https://firebase.google.com/docs/ios/setup) ao Firebase e recupere o ***GoogleService-Info.plist*** arquivo.

## Gerar os binários assinados

### iOS

```
sh""" xcodebuild -exportArchive -archivePath ./mobile-app-embedding-immersive/build/ios/archive/Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist ./deviceAppBuildScripts/${ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```

>[!NOTE]
>
>Você precisará do XCode 14.2 ou superior para criar os binários assinados.


## Android

```
sh""" ~/Library/Android/sdk/build-tools/30.0.3/apksigner sign --ks $storeFile --ks-pass "pass:$store\_password" --ks-key-alias $key\_alias --key-pass "pass:$key\_password" --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>Você precisará das ferramentas de compilação do sdk do Android para criar os binários assinados.

**Novidades**

Depois de gerar os binários, envie-os para a Play Store ou App Store.

## Como aplicar as alterações

Envia os ativos e arquivos necessários para a equipe de CSM. A equipe do CSM preenche, em seguida, o [formulário](https://forms.office.com/r/bJRRaRBvSh) com as alterações necessárias e anexa os ativos necessários. A equipe então analisará e informará as equipes de engenharia sobre as mudanças. A equipe de engenharia irá gerar uma compilação e compartilhar com a equipe de CSM.

A equipe do CSM compartilhará a compilação com o cliente.

## O que não pode ser personalizado

- Tela Atualizar senha
- Tela Criar uma conta