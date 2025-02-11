---
jcr-language: en_us
title: Documentação da API de interação do reprodutor incorporado
description: Saiba mais sobre as várias APIs para ouvir eventos e acionar ações no reprodutor incorporado
contentowner: chandrum
exl-id: 4734ecc1-cc8a-40b0-8997-32a31ec661ec
source-git-commit: 3d183dc40e4d1962d25160b74d8cf6cfa26e3171
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 69%

---

# Documentação da API de interação do reprodutor incorporado

O Adobe Learning Manager fornece uma biblioteca que pode ser integrada a um aplicativo. Esta biblioteca fornece várias APIs para ouvir eventos e acionar ações no reprodutor incorporado.

Usando as APIs fornecidas, você pode reproduzir, pausar e executar outras ações no reprodutor.

## Carregar a biblioteca

A biblioteca está disponível neste [local](https://cpcontents.adobe.com/public/publiccdn/playerInteractionLib.min.js).

Para carregar a biblioteca, siga as etapas abaixo:

1. Carregue o arquivo js no aplicativo do cliente.
2. Ao carregar a biblioteca, window.cpPlayerLib será preenchido.

>[!NOTE]
>
>Se você não estiver usando prod US, defina os parâmetros cpPlayerLib.env e cpPlayerLib.sourceOrigin com base em seu env.

Os valores padrão são:

* window.cpPlayerLib.env = [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player);
* window.cpPlayerLib.sourceOrigin = &quot;[https://cpcontents.adobe.com](https://cpcontents.adobe.com/)&quot;;

### Métodos disponíveis

A biblioteca cpPlayerLib consiste nas seguintes funções:

**startPlayer**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>startPlayer</td>
</tr>
<tr>
<td>Descrição</td>
<td>Carrega um reprodutor no aplicativo.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>loId: a ID do objeto de aprendizado.</li><li>accountId: a ID da conta da conta do ALM.</li><li>userId: a ID do usuário.</li><li>accessToken: o token de acesso.</li><li>domRefId: a ID do contêiner div no qual o reprodutor deve ser renderizado.</li><li>onModuleLoaded: esta função será invocada quando os módulos com os detalhes abaixo forem carregados.</li><br><li>contentType</li><li>loID</li><li>moduleId</li><li>concluído</li><li>currentLanguage</li><li>availableLanguages</li><li>isCCAvailable</li><li>ccEnabled</li></br></td>
</tr>
<tr>
<td>Devoluções</td>
<td>Retorna uma promessa. Na resolução da promessa, um playerObj será passado.</td>
</tr>
<tr>
<td>Exceção</td>
<td>A promessa resultará em uma exceção.</td>
</tr>
<tr>
<td>Código de exemplo</td>
<td>cpPlayerLib.startPlayer(loId, accountId, userId, accessToken, domRefId, onModuleLoaded).then((playerObj) =&gt; {//playerObj tem as apis para interagir com o reprodutor}) &gt;</td>
</tr>
</tbody>
</table>

**getAllPlayers**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>getAllPlayers</td>
</tr>
<tr>
<td>Descrição</td>
<td>Devolve todos os objetos do leitor na página atual.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td>Nenhum</td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>cpPlayerLib.getAllPlayers()</td>
</tr>
</tbody>
</table>

**getPlayer**


<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>getPlayer</td>
</tr>
<tr>
<td>Descrição</td>
<td>Retorna um objeto do reprodutor com a ID do objeto de aprendizado especificada.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>loId: a ID do objeto de aprendizado.</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>cpPlayerLib.getPlayer(loId)</td>
</tr>
</tbody>
</table>

**navigateToModule**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>navigateToModule</td>
</tr>
<tr>
<td>Descrição</td>
<td>Navegar para o próximo módulo.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>moduleId: A ID do módulo.</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.navigateToModule(moduleID)</td>
</tr>
</tbody>
</table>

**próximo**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>próximo</td>
</tr>
<tr>
<td>Descrição</td>
<td>Navegar para o próximo módulo.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.next()</td>
</tr>
</tbody>
</table>

**anterior**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>anterior</td>
</tr>
<tr>
<td>Descrição</td>
<td>Navegue para o módulo anterior.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.previous()</td>
</tr>
</tbody>
</table>

**toggleTOC**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>toggleTOC</td>
</tr>
<tr>
<td>Descrição</td>
<td>Alterne o painel de sumário no reprodutor.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.toggleTOC()</td>
</tr>
</tbody>
</table>

**toggleNotes**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>toggleNotes</td>
</tr>
<tr>
<td>Descrição</td>
<td>Alterna o painel de notas no reprodutor.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.toggleNotes()</td>
</tr>
</tbody>
</table>

**toggleClosedCaption**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>toggleClosedCaption</td>
</tr>
<tr>
<td>Descrição</td>
<td>Alterna a exibição de legendas codificadas no reprodutor.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.toggleClosedCaption()</td>
</tr>
</tbody>
</table>

**changeLanguage**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>changeLanguage</td>
</tr>
<tr>
<td>Descrição</td>
<td>Altere o idioma do conteúdo no reprodutor.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>idioma: o código do idioma a ser especificado.</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.changeLanguage("es")</td>
</tr>
</tbody>
</table>

**closePlayer**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>closePlayer</td>
</tr>
<tr>
<td>Descrição</td>
<td>Feche o player e remova-o da página. </td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.closePlayer()</td>
</tr>
</tbody>
</table>

**togglePlayPause**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>togglePlayPause</td>
</tr>
<tr>
<td>Descrição</td>
<td>Alterne entre reproduzir e pausar o conteúdo no reprodutor.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.togglePlayPause()</td>
</tr>
</tbody>
</table>

**setVolume**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>setVolume</td>
</tr>
<tr>
<td>Descrição</td>
<td>Defina o volume do reprodutor. O valor deve estar entre 0 e 1.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>volume: o valor do volume. O intervalo válido é de 0 a 1. </li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.setVolume(0.5)</td>
</tr>
</tbody>
</table>

**setPlayBackSpeed**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>setPlayBackSpeed</td>
</tr>
<tr>
<td>Descrição</td>
<td>Defina a velocidade da reprodução no reprodutor.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>velocidade: o valor da velocidade a ser especificado. Os valores válidos são 0,25, 0,5, 0,75, 1, 1,25, 1,5, 1,75, 2.</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.setPlayBackSpeed(1.25)</td>
</tr>
</tbody>
</table>

**buscar**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>buscar</td>
</tr>
<tr>
<td>Descrição</td>
<td>Pule para qualquer tempo no vídeo.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>tempo: o tempo para o qual pular. O tempo é em segundos.</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.seek(50)</td>
</tr>
</tbody>
</table>

**avançar**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>avançar</td>
</tr>
<tr>
<td>Descrição</td>
<td>Avance o vídeo em 10 segundos.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.forward()</td>
</tr>
</tbody>
</table>

**retroativo**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>retroceder</td>
</tr>
<tr>
<td>Descrição</td>
<td>Retroceda 10 segundos no vídeo.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.backward()</td>
</tr>
</tbody>
</table>

**navigateToPage**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>navigateToPage</td>
</tr>
<tr>
<td>Descrição</td>
<td>Pule para a página especificada no PPT/PDF.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>pageNumber: O número da página para a qual saltar.</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.navigateToPage (5)</td>
</tr>
</tbody>
</table>

**próximaPágina**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>nextPage</td>
</tr>
<tr>
<td>Descrição</td>
<td>Vá para a próxima página no PPT/PDF.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.nextPage()</td>
</tr>
</tbody>
</table>

**páginaAnterior**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>previousPage</td>
</tr>
<tr>
<td>Descrição</td>
<td>Pule para a página anterior no PPT/PDF.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.previousPage()</td>
</tr>
</tbody>
</table>

**Mais zoom**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>zoomIn</td>
</tr>
<tr>
<td>Descrição</td>
<td>Amplie o conteúdo em um PPT/PDF.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.zoomIn()</td>
</tr>
</tbody>
</table>

**Menos zoom**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>zoomOut</td>
</tr>
<tr>
<td>Descrição</td>
<td>Diminua o zoom no conteúdo em um PPT/PDF.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.zoomOut()</td>
</tr>
</tbody>
</table>

**downloadJobAid**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>downloadJobAid</td>
</tr>
<tr>
<td>Descrição</td>
<td>Baixar uma ajuda de tarefa de um curso.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.downloadJobAid()</td>
</tr>
</tbody>
</table>

**toggleJobAidPullout**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>toggleJobAidPullout</td>
</tr>
<tr>
<td>Descrição</td>
<td>Se você deseja ou não baixar uma ajuda de tarefa.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.toggleJobAidPullout()</td>
</tr>
</tbody>
</table>

**tela cheia**

<table>
<tbody>
<tr>
<td>Nome do método</td>
<td>fullScreen</td>
</tr>
<tr>
<td>Descrição</td>
<td>Definir o reprodutor para o Modo de tela inteira.</td>
</tr>
<tr>
<td>Parâmetros</td>
<td><li>Nenhum</li></td>
</tr>
</tr>
<tr>
<td>Código de exemplo</td>
<td>playerObj.fullScreen()</td>
</tr>
</tbody>
</table>

## Lista de eventos

**onPlayerEvents(callBack)**

Ao registrar, a função de retorno de chamada será invocada em todos os eventos do reprodutor. Os nomes dos eventos são os seguintes:

* PLAY (Vídeo/ Áudio/ PC)
* PAUSE (Vídeo/ Áudio/ PC)
* TIMEUPDATE (Vídeo/ Áudio/ CP)
* PAGECHANGE (PPT/ PDF)
* NOTEADDED (Todos os conteúdos)
* LAUNCHED (Todos os conteúdos)
* STARTED (Todos os conteúdos)
* COMPLETED (Todos os conteúdos)
* PASSED (Todos os conteúdos)
* FAILED (todos os conteúdos)

**onStreamingEvents(callBack)**

Ao registrar, a função de retorno de chamada será invocada em todas as instruções do reprodutor enviadas para acompanhar a atividade do usuário.
