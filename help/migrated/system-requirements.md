---
jcr-language: en_us
title: Requisitos do sistema
description: Requisitos de sistema do Adobe Learning Manager
contentowner: dvenkate
exl-id: 3bf9818a-4b86-47e9-9b86-1c32b8bfee3a
source-git-commit: f964dd3f1adeadb76f4843c9af229ce5f09afde1
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 62%

---

# Requisitos de sistema do Adobe Learning Manager

## Desktop

### Sistema operacional

Windows 10 e 11, macOS X 10.12, 10.13, 10.14, 10.15

### Processador

Intel® CoreTM i5 ou mais rápido.

### RAM

Mínimo de 8 GB necessário.

### Resolução da tela

1366 x 768 pixels

### Espaço em disco

Mínimo de 5 GB de espaço em disco disponível.

### Gravação

É necessário um microfone para gravação de áudio; uma webcam é necessária para gravação de vídeo.

## Aplicativo móvel

### Dispositivos

* iOS: as duas últimas versões principais.
* Android: as duas últimas versões principais.

### Navegadores

* Chrome no Android.
* Safari no iOS.

### Velocidade da rede

* 1 Mbps

### CPU, dispositivos de memória (mín.)

* Qualcomm® Snapdragon™ 695 5G ou equivalente, 6 GB de memória

### Scanner de código QR/espaço em disco necessário

* 250 MB

>[!NOTE]
>
>O navegador móvel oferece suporte somente à função do aluno no **layout imersivo**.

>[!NOTE]
>
>O aplicativo móvel do Learning Manager é compatível somente com a função do aluno.

## Diversos

São necessárias uma conexão ativa com a Internet e uma conta de aluno do Adobe Learning Manager para usar o aplicativo.

## Especificações do navegador

A página inicial de layout imersivo não é compatível com navegadores IE 11.

* Versão 43 do Google Chrome e posterior.
* Versões mais recentes do Edge, Safari (versão 13 e posterior) e Firefox.
* Internet Explorer versão 11 e posterior

## Tamanho recomendado das imagens {#recommendedsizeofimages}

* Manchete:
   * Para configurações tão grandes: 1280 x 360 PX
   * Para configurações como médias: 1280 x 273 PX
   * Para configurações tão pequenas: 1280 x 187 PX
* Imagem no cartão de catálogo: 280 x 100 px
* Dimensão do cartão de treinamento: 300 x 240 px
* Banner social: 1600 x 240 px

## Tamanho máximo de conteúdo {#maximumcontentsize}

O tamanho máximo do arquivo que pode ser carregado é de 600 MB.

>[!NOTE]
>
>Se o tamanho do arquivo *user.csv* exceder 100 MB, a importação desse arquivo pode fazer com que o navegador se comporte de forma imprevisível. O problema ocorre porque o navegador fica sem memória.

Recomendamos importar arquivos *user.csv* de tamanho grande usando o fluxo de trabalho automatizado do Box/Exavault. Para saber mais, consulte [Migrando arquivos](/help/migrated/integration-admin/feature-summary/migration-manual.md).


## Formatos de conteúdo suportados

### Carregar o módulo {#moduleupload}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Tipo de conteúdo</b></p></td>
   <td>
    <p><b>Extensões</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Documentos</p></td>
   <td>
    <p>"pdf", "docx", "doc", "xls", "xlsx"</p></td>
  </tr>
  <tr>
   <td>
    <p>Apresentações do PowerPoint</p></td>
   <td>
    <p>"pptx", "ppt"</p></td>
  </tr>
  <tr>
   <td>
    <p>Vídeos</p></td>
   <td>
    <p>"mp4", "wmv", "3gp", "3g2", "3gp2", "asf", "avi", "f4v", "h264", "mpe", "mpeg", "mpg", "mpg2", "m4v", "mov", "wmv"</p></td>
  </tr>
  <tr>
   <td>
    <p>SCORM 1.2</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>SCORM 2004</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>CAPI</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>AICC</p></td>
   <td>
    <p>"zip"</p></td>
  </tr>
  <tr>
   <td>
    <p>Áudio</p></td>
   <td>
    <p>“mp3”, “wav”, “aac”, “m4a”, “wma”, “vorbis”, “pcm”, “eac3”, “amr”, “ac3”</p></td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p><strong>Medalhas</strong></p></td>
   <td>
    <p>“png”, “jpg”, “jpeg”, “gif”</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Foto no perfil do usuário</strong></p></td>
   <td>
    <p>“png”, “jpg”, “jpeg”, “gif”</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Logotipo da empresa</strong></p></td>
   <td>
    <p>“png”, “jpg”, “jpeg”, “bmp”, “gif”</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Carregar certificações</strong></p></td>
   <td>
    <p> “png”, “jpg”, “jpeg”, “pdf”, “doc”, “docx”, “gif”</p></td>
  </tr>
  <tr>
   <td>
    <p><strong>Recursos/anexos do curso</strong></p></td>
   <td>
    <p> Todos os formatos de arquivo</p></td>
  </tr>
 </tbody>
</table>

## Especificação de altura e largura para carregar elementos {#heightandwidthspecificationforuploadingelements}

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Elementos</b></p></td>
   <td>
    <p><b>Tamanho</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Crachá no quadro Realizações do Aluno</p></td>
   <td>
    <p>40 x 40 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Crachá expandido no aplicativo do Aluno</p></td>
   <td>
    <p>90 x 90 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Foto no perfil do usuário nas Realizações do Aluno</p></td>
   <td>
    <p>100 x 100 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Foto no perfil do usuário no menu suspenso Logout</p></td>
   <td>
    <p>42 x 42 pixels</p></td>
  </tr>
  <tr>
   <td>
    <p>Logotipo da empresa no cabeçalho</p></td>
   <td>
    <p>45 pixels de altura, a largura é calculada de acordo.</p></td>
  </tr>
  <tr>
   <td>
    <p>Logotipo da empresa na página inicial do Learning Manager</p></td>
   <td>
    <p>100 pixels de altura, a largura é calculada de acordo.</p></td>
  </tr>
 </tbody>
</table>

## Acessibilidade

### Navegadores e leitores de tela compatíveis

As seguintes combinações são suportadas:

* Chrome + NVDA
* Edge + Narrador
* Mac Safari + VoiceOver

### Suporte para o dispositivos móveis imersivo

São suportados os seguintes:

* Android+Talkback
* iOS+voiceOver

## Requisitos de rede {#networkrequirements}

Certifique-se de que os seguintes domínios de terceiros estão permitidos se você estiver em qualquer rede que tenha restrições.

* &#42;.adobe.com
* &#42;.boltdns.net
* &#42;.brightcove.com
* &#42;.amazon.com
* &#42;.adobedtm.com
* &#42;.typekit.net
* &#42;.demdex.net
* &#42;.brightcove.net
* &#42;.zencdn.net
* &#42;.cloudflare.com
* bam.nr-data.net
* &#42;.akamaihd.net


### Casos estendidos específicos {#specificextendedcases}

<table>
 <tbody>
  <tr>
   <th>Recurso</th>
   <th>Serviços utilizados</th>
  </tr>
  <tr>
   <td>Conector FTP</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a></td>
  </tr>
  <tr>
   <td>Migração</td>
   <td><a href="https://www.box.com/" target="_blank">www.box.com</a><br><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a></td>
  </tr>
  <tr>
   <td>Conector Lynda</td>
   <td><a href="https://www.box.com/" target="_blank">www.box.com</a><br><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://www.lynda.com/" target="_blank">www.lynda.com</a></td>
  </tr>
  <tr>
   <td>Conector Harvard ManageMentor</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://myhbp.org" target="_blank">www.myhbp.org</a></td>
  </tr>
  <tr>
   <td>Conector GetAbstracts</td>
   <td><a href="https://www.exavault.com/" target="_blank">www.exavault.com</a><br><a href="https://www.getabstract.com/en/" target="_blank">www.getabstract.com </a></td>
  </tr>
  <tr>
   <td>Conector Box</td>
   <td>Box Zones localizado em Frankfurt</td>
  </tr>
  <tr>
   <td>Conector Mini Orange</td>
   <td>Mini Orange</td>
  </tr>
  <tr>
   <td>Conector Workday</td>
   <td>Workday</td>
  </tr>
  <tr>
   <td>Conector Blue Jeans<br></td>
   <td>Blue Jeans</td>
  </tr>
  <tr>
   <td>Microsoft Power BI</td>
   <td>Licença comercial de Power BI suportada apenas.</td>
  </tr>
 </tbody>
</table>

## Visão geral técnica {#technicaloverview}

[Visão geral técnica do Learning Manager](assets/learning-manager-technicaloverview.pdf)

## Informe oficial de segurança do ALM

[Informe oficial do ALM](assets/alm-security-whitepaper-2024.pdf)
