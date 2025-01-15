---
jcr-language: en_us
title: Rotulagem de branco no aplicativo Adobe Learning Manager para dispositivos móveis
description: A rotulagem branca é uma prática de mudar a identidade visual de um aplicativo ou serviço com sua própria marca e personalizá-lo como se você fosse o criador original. No Adobe Learning Manager, você pode aplicar rótulos brancos ao aplicativo para dispositivos móveis, além de remarcar o aplicativo e disponibilizá-lo para seus usuários com sua própria marca.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: b7050db4b7129028ada51b15e2d76fce2bb62f64
workflow-type: tm+mt
source-wordcount: '1987'
ht-degree: 0%

---

# Rotulagem de branco no aplicativo Adobe Learning Manager para dispositivos móveis

O aplicativo Adobe Learning Manager para dispositivos móveis agora é compatível com a rotulagem branca, o que significa que agora você pode lançá-lo sob sua própria marca.

O ALM disponibilizará arquivos binários rotulados em branco atualizados de acordo com as seguintes linhas do tempo:

1. Para versões principais do aplicativo móvel, os arquivos serão disponibilizados com duas semanas de antecedência
2. Para todas as atualizações planejadas de correções urgentes, os arquivos serão disponibilizados com uma semana de antecedência
3. Para correções não planejadas, urgentes e imediatas, os arquivos serão disponibilizados na base do melhor esforço possível

Os binários serão disponibilizados nas pastas designadas do cliente. Entre em contato com seus CSMs para acessar os arquivos. O cliente é responsável pela publicação oportuna e pelos processos relacionados.

## Como você deve começar a se preparar para iniciar seu aplicativo com rótulo branco

Para implantar e gerenciar seu próprio aplicativo com rótulo branco, siga as etapas:

1. Prepare os ativos (como imagem da tela inicial) e o texto para que ambos possam ser usados no aplicativo e na descrição na app/play store.

1. Atribua um recurso técnico capaz de:

   * Gerando os arquivos de certificado de notificação por push.
   * Assinar os binários do aplicativo fornecidos pela equipe do ALM.
   * Carregando e gerenciando o processo de publicação. O processo de publicação requer comunicação entre seu gerente de aplicativos e as equipes da App/Play Store para que o aplicativo esteja em conformidade com todas as diretrizes de publicação. No ALM, você receberá um binário de aplicativo totalmente compatível.

## Visão geral

A rotulagem branca é uma prática de mudar a identidade visual de um aplicativo ou serviço com sua própria marca e personalizá-lo como se você fosse o criador original. No Adobe Learning Manager, você pode aplicar rótulos brancos ao aplicativo para dispositivos móveis, além de remarcar o aplicativo e disponibilizá-lo para seus usuários com sua própria marca.

## O que pode ser personalizado

O seguinte pode ser personalizado:

### Campos

<table>

 <tbody>

  <tr>

   <td>

    <p>ID da conta</p>

   </td>

   <td>

    <p>A ID da sua conta. Observe que o aplicativo com rótulo branco não estará acessível aos alunos que pertencem a qualquer outra conta.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>IDs de conta adicionais</p>

   </td>

   <td>

    <p>Adicione várias contas (subdomínios), se desejar. Adicione os subdomínios como separados por vírgula sem espaços. Por exemplo, acc01,acc02,acc03 e assim por diante.<br> <b>Observação:</b> é necessário adicionar a ID da conta ao especificar os subdomínios.</br> </p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nome do aplicativo</p></td>

   <td>

    <p>O nome que você deseja usar para o aplicativo.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nome curto do aplicativo</p>

   </td>

   <td>

    <p>Nos casos em que o nome do aplicativo for longo, dê ao aplicativo um nome curto que apareça no dispositivo.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nome do aplicativo interno</p></td>

   <td>

    <p>O nome com o qual o sistema operacional identifica o aplicativo. O formato usado normalmente é: com.company-name.product-name.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nome do aplicativo interno - iOS</p>

   </td>

   <td>

    <p>Nomeie o aplicativo de maneira diferente se os usuários estiverem no iOS. Recomendamos usar o mesmo nome para o iOS e o Android.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Ícone de aplicativo</p>

   </td>

   <td>

    <p>O ícone do aplicativo é png. Este ícone é exibido no seu aplicativo. O formato para o nome é account-id_appIcon.png. As dimensões do ícone do aplicativo são 512 × 512 pixels.<div>Observe que o Apple não permite o canal Alpha em ícones de aplicativos. Portanto, remova o canal de Alpha do ativo antes de enviá-lo.</div></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Tela inicial do aplicativo</p></td>

   <td>

    <p>Para a tela inicial do seu aplicativo, forneça uma imagem (png) que será exibida quando os usuários iniciarem o aplicativo. O formato para o nome é account-id_splashIcon.png. As dimensões das telas de splash quadradas são de 1052 × 1052 pixels e as telas de splash em círculo são de 768 x 768 pixels.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>ID do cliente e segredo do cliente</p>

   </td>

   <td>

    <p>O administrador de integração da sua conta fornece os detalhes ao registrar o aplicativo. O administrador de integração deve usar o seguinte:<ul><li>aluno:ler,aluno:gravar como função</li><li>aplicativo interno name://redirect como URL de redirecionamento</li></ul></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Logotipo da conta</p>

   </td>

   <td>

    <p>O URL que hospeda o logotipo da sua organização. Forneça um link cpcontents como o logotipo da conta. O URL precisa ser codificado na Web.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>ID da loja de aplicativos do aplicativo (iOS)</p>

   </td>

   <td>

    <p>A ID necessária para implementar a atualização forçada. O aplicativo precisa saber que o aluno deve ser redirecionado para a loja de aplicativos para atualizar o aplicativo.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>ID da Google Play Store para o aplicativo (Android)</p>

   </td>

   <td>

    <p>A ID necessária para implementar a atualização forçada.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Nome do host para deep linking</p>

   </td>

   <td>

    <p>Para hospedar os links profundos, use o learningmanager. Se quiser usar outro URL de nome de host como um deep link, forneça o URL do host. Por exemplo, learningmanager.adobe.com.</p>

   </td>

  </tr>

 </tbody>

</table>

>[!NOTE]
>
>Forneça os dados aos CSAMs para que eles possam adicioná-los ao binário do aplicativo personalizado.


#### Atualizar associação de site para manipular deplinks personalizados

Se estiver usando um domínio personalizado ou o learningmanager\*.adobe.com como host, você não precisa fazer nada. No entanto, se você usar uma solução personalizada ou um nome de host específico para os URLs, adicione os arquivos de associação de site.

>[!CAUTION]
>
>Se os arquivos não estiverem presentes, os deplinks não funcionarão. Verifique se os arquivos estão presentes.


Consulte os links a seguir para obter mais informações:

* [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)
* [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Gerar notificações por push

O envio de notificações por push para aplicativos Android e iOS requer dois mecanismos diferentes.

* Para o iOS, gere os certificados de notificação por push.
* Para Android, forneça uma chave do servidor gerada a partir do projeto Firebase.

Siga as instruções abaixo para configurar os projetos no Firebase:

### Notificações por push no iOS

No desenvolvimento de aplicativos da iOS, um certificado de notificação por push é uma credencial criptográfica emitida pela Apple que permite que um servidor envie notificações por push com segurança para um dispositivo iOS por meio do Serviço de Notificação por Push (APNs) da Apple.

O certificado garante a comunicação segura entre o servidor (ou provedor) e os APNs da Apple ao enviar notificações push para dispositivos iOS.

Tanto o Android quanto o iOS usam o Firebase Cloud Messaging (FCM) como o serviço de envio de notificações por push para dispositivos.

### Como gerar o certificado no iOS

Siga o procedimento:

1. Gere ou baixe o **Certificado de notificação por push** e a chave privada (.p12). Para obter mais informações, consulte o [documento do desenvolvedor do Apple](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Instale o arquivo p12 após o download do arquivo. Use a senha para instalar no **Acesso às Chaves**.

1. Navegue até **Meus certificados** e exporte o certificado. Certifique-se de selecionar o tipo MIME .cer.

1. Assim que o arquivo p12 e o arquivo cer estiverem disponíveis, execute os seguintes comandos:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Se você puder se conectar ao servidor, o certificado que você criou será válido. No arquivo myapnappkey.pem, copie os valores do certificado e da chave privada.

### Notificações por push no Android

Para Android, o usuário precisa fornecer o arquivo services.json do projeto Firebase para adicionar a entrada no serviço SNS.

Crie um projeto no Firebase e compartilhe o arquivo services.json com a equipe do CSM. Esse arquivo é necessário para a entrada baseada em token no SNS. Observe que a chave do servidor não é mais usada. Consulte [Criar projeto no Firebase](#create-project-in-firebase).

Para baixar o arquivo services.json, siga estas etapas:

1. Faça logon no console **Firebase**.
1. Vá para **Configurações do projeto** e selecione **Mensagens na nuvem**.
1. Localize a **API do Firebase Cloud Messaging** e selecione **Gerenciar Contas de Serviço**.
1. Na página **Contas de serviço**, selecione as **Contas de serviço** no painel esquerdo.
1. Localize sua entrada do projeto e selecione **Gerenciar detalhes** em Ações.

   >[!NOTE]
   >
   >   O formato de entrada do projeto será &lt;-accountname->@appspot.gserviceaccount.com.

1. Vá para a guia **Chaves** e selecione **Adicionar Chave**.
1. Se não houver uma chave, selecione **Criar nova chave** e selecione **JSON** como o tipo de chave. Isso vai gerar e baixar o arquivo JSON.
1. Se já houver uma chave, selecione **Carregar chave existente**, cole a chave e carregue-a. Isso vai gerar e baixar o arquivo JSON.

<!-- Set up a project in Firebase and share the server key with the CSAM.-->

Entre em contato com a equipe de CSM e compartilhe o arquivo JSON para adicionar a entrada aos serviços SNS no AWS. Os usuários terão que obter a entrada registrada no serviço SNS para a notificação por push, que exigirá que eles compartilhem os certificados gerados acima para validação.

## Criar projeto no Firebase {#create-project-in-firebase}

### Android

Reutilize o mesmo projeto que você criou nas etapas acima para notificações por push.

[Adicione o projeto](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) no Firebase e recupere o arquivo ***google-services.json***.

### iOS

[Adicione o projeto](https://firebase.google.com/docs/ios/setup) ao Firebase e recupere o arquivo ***GoogleService-Info.plist***.

>[!IMPORTANT]
>
>Envie os arquivos para a equipe Adobe Learning Manager CSAM para serem incluídos na compilação do arquivo binário do aplicativo.


## Gerar os binários assinados

### iOS

<!--```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist {ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```-->

A pasta `<root>` contém o arquivo **Runner.xcarchive.zip**. Execute os comandos abaixo para gerar o binário assinado:

1. Execute o seguinte comando para descompactar o arquivo:

   ```
   unzip Runner.xcarchive.zip
   ```

2. Navegue até o diretório do aplicativo:

   ```
   cd Runner.xcarchive/Products/Applications/Runner.app
   ```

3. Copie o arquivo de provisionamento móvel:

   ```
   cp <path>/<mobile-provisioningfile>.mobileprovision embedded.mobileprovision
   ```

4. Execute o seguinte comando para atualizar suas informações de assinatura para a biblioteca de estrutura:

   ```
   codesign -f -s "Distribution Certificate Name" Frameworks/*
   ```

5. Retorne à pasta `<root>` (onde Runner.xcarchive.zip está localizado):

   ```
   cd <root>
   ```

6. Exporte o arquivo usando o xcodebuild:

   ```
   xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath ipa_path/ -exportOptionsPlist <path>/<ExportOptions-file>.plist
   ```

7. Localize o arquivo .ipa na pasta ipa_path.
8. Carregar o arquivo .ipa no site `Diawi`.
9. Após o upload completo, selecione o botão **[!UICONTROL Enviar]**.
10. Após a conclusão, você receberá um código QR e um link.
11. Abra o código QR ou link diretamente no Safari.

Se o dispositivo estiver incluído no perfil de provisionamento, a instalação deverá continuar no dispositivo.

>[!NOTE]
>
>Você precisará do XCode 15.2 ou superior para criar os binários assinados.


### Android

**Para arquivo apk**

>[!IMPORTANT]
>
>Antes de executar o comando `apksigner`, execute os seguintes comandos para exportar a senha do armazenamento de chaves e a senha do alias da chave como variáveis de ambiente:
>
>```
>export KS_PASS=your_keystore_password
>export KEY_PASS=your_key_password
>```

```
sh""" <path>/apksigner sign --ks $storeFile. --ks-pass env:KS_PASS --ks-key-alias $key_alias --key-pass env:KEY_PASS --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>O caminho para a ferramenta `apksigner` geralmente é semelhante a: ~/Library/Android/sdk/build-tools/30.0.3/apksigner.

**Para arquivo aab**

>[!NOTE]
>
>Você precisará das ferramentas de compilação do sdk do Android para criar os binários assinados.

A Play Store requer binários Android no formato aab para publicação. Portanto, forneceremos o arquivo .aab não assinado.

>[!NOTE]
>
>Ao criar um arquivo keystore, você precisa gerar uma senha keystore, um alias de chave de assinatura e uma senha de alias de chave de assinatura.

Siga as etapas abaixo para assinar o arquivo .aab:

Execute o seguinte comando:

```
<path>/jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 -keystore <keystore-file> app-release.aab <signingKeyAlias>
```

>[!NOTE]
>
>O **[!UICONTROL jarsigner]** está incluído no Java. Certifique-se de estar usando o Java 21.

Quando solicitado, insira as seguintes senhas:

* Senha do armazenamento de chaves
* senha para alias da chave de assinatura

Você pode usar o apk fornecido. No entanto, se você precisa gerar um apk a partir de um arquivo aab, por favor, siga estes passos:

>[!NOTE]
>
>Você precisará instalar o **[!UICONTROL bundletool]** para gerar APKs.


Execute o seguinte comando para criar o arquivo apk:

```
java -jar <path>/bundletool-all.jar  build-apks --bundle=app-release.aab --output=my_app.apks --mode=universal
```

Para descompactar o arquivo, execute o seguinte comando:

```
unzip my_app.apks -d output_dir
```

Você obterá o arquivo apk da pasta **[!UICONTROL output_dir]**.

**Novidades**

Depois de gerar os binários, envie-os para a Play Store ou App Store.

### Enviar os aplicativos para a loja para revisão

Depois de obter os binários finais, você pode carregá-los nas respectivas lojas de aplicativos (iOS ou Android) para revisão. Siga estas etapas para carregar os binários nas lojas de aplicativos.

**iOS**

1. Faça logon no aplicativo Transporter com suas credenciais do App Store.
2. Selecione o botão **+** no canto superior esquerdo e carregue o certificado de produção (arquivo .ipa).
3. Se o arquivo .ipa estiver correto, você será solicitado a fazer upload do aplicativo no App Store.
4. Após a entrega do aplicativo, faça logon no App Store. Dentro de algumas horas, o binário aparecerá na seção TestFlight. Você pode ativá-lo para o teste de sanidade final no TestFlight antes da revisão do aplicativo e usar este IPA como binário ao enviar o aplicativo para uma nova versão.

**Android**

1. Abra o Console da Google Play Store.
2. Vá para **[!UICONTROL Painel]** > **[!UICONTROL Exibir Versões de Aplicativos]** > **[!UICONTROL Painel de Versões]** e selecione **[!UICONTROL Criar Nova Versão]**.
3. Faça upload do arquivo .aab gerado como o pacote de aplicativos e digite os detalhes da versão, como o número da versão e as informações de Novidades.
4. Salve suas alterações e envie o aplicativo para revisão.
5. Defina a distribuição do aplicativo como 100% (por padrão, o Google define-a como 20%).

#### Links úteis para publicação de aplicativos

**Android**

[Criar e configurar seu aplicativo](https://support.google.com/googleplay/android-developer/answer/9859152?hl=en)
[Prepare seu aplicativo para revisão](https://support.google.com/googleplay/android-developer/answer/9859455?sjid=2454409340679630327-AP)

**iOS**

[Enviar para revisão](https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-for-review)

## Como aplicar as alterações

Envia os ativos e arquivos necessários para a equipe de CSM. A equipe do CSM preenche o [formulário](https://forms.office.com/r/bJRRaRBvSh) com as alterações necessárias e anexa os ativos necessários. A equipe então analisará e informará as equipes de engenharia sobre as mudanças. A equipe de engenharia irá gerar uma compilação e compartilhar com a equipe de CSM.

A equipe do CSM compartilhará a compilação com o cliente.

## O que não pode ser personalizado

* Tela Atualizar senha
* Tela Criar uma conta
