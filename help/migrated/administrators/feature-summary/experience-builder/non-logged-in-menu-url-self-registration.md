---
description: Saiba como compartilhar um URL de menu não conectado para cada perfil de autorregistro para que usuários externos se associem ao perfil correto no Adobe Learning Manager
jcr-language: en_us
title: Usar um URL de menu não conectado para autorregistro
exl-id: c4b3f1f5-a785-45ab-b820-621dae16526d
source-git-commit: 8cf3817fc740f8a0219ca6b4f3fe6c637633c955
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 0%
---

# Usar um URL de menu não conectado para autorregistro

Os perfis de autorregistro permitem que usuários externos, como parceiros ou membros de várias organizações, criem suas próprias contas no Adobe Learning Manager. Agora você pode compartilhar um URL de menu não conectado para cada perfil de autorregistro. O menu é integrado ao Experience Builder.

Quando os usuários selecionam **Inscrever-se** em uma página acessada por meio dessa URL, o Adobe Learning Manager os adiciona ao perfil ao qual a URL pertence. Isso permite manter usuários de diferentes organizações, como diferentes agências ou empresas parceiras, em perfis separados.

Anteriormente, uma URL de página não conectada sempre adicionava novos usuários a um perfil selecionado em **Marcas**. O URL de menu não conectado remove essa limitação: cada perfil tem seu próprio URL e todos os URLs abrem a mesma página de aterrissagem.

## Antes de começar

1. Crie o menu não conectado no Experience Builder e selecione a página de aterrissagem em **Marcas**. Todos os URLs de perfil abrem esta página de aterrissagem.

1. Crie o perfil de autorregistro em **Usuários** > **Externos**. Cada perfil tem sua própria ID de grupo e chave de acesso, que os usuários precisam inscrever.

## Copiar o URL de inscrição de um perfil

1. Selecione **Usuários** > **Externos** e selecione **Autorregistro**.

1. Na coluna **URL da página de aterrissagem a ser copiada**, selecione **Não conectado** para um perfil.

   ![URL da página de aterrissagem a ser copiada para uma coluna de um perfil de autorregistro](assets/Use-a-non-logged-in-menu-URL-for-self-registration-image1.png "URL da página de aterrissagem a ser copiada")

1. Copie o URL e compartilhe-o com os usuários que deseja convidar.

A lista **URL da página de aterrissagem a ser copiada** inclui estas opções:

* **Registro**: a URL de registro padrão
* **Página inicial não conectada (herdada)**: a URL da página inicial herdada não conectada
* **Menu Não conectado**: a URL do menu não conectado no Experience Builder

## O que os usuários veem

1. O usuário abre a URL e chega na página de aterrissagem não conectada que você selecionou em **Marcas**.

1. O usuário seleciona **Inscrever-se** e insere a ID de grupo e a chave de acesso para o perfil.

1. O usuário insere seu nome, endereço de email e senha e, em seguida, conclui o registro.

O Adobe Learning Manager adiciona o usuário ao perfil ao qual o URL pertence. Você pode ver o novo usuário nesse perfil em **Usuários** > **Externos**.

>[!NOTE]
>
>Cada URL de perfil mostra a mesma página de aterrissagem. Somente o perfil ao qual os usuários são adicionados é diferente.

## Enviar um email de boas-vindas com o URL

1. Selecione **Usuários** > **Externos** e selecione o perfil de autorregistro.

1. Na lista **URL da página de aterrissagem a ser copiada**, selecione a URL a ser incluída no email.

   ![Lista de URLs da página de aterrissagem com os ícones de email e cópia](assets/Use-a-non-logged-in-menu-URL-for-self-registration-image2.png "Lista de URLs da página de aterrissagem")

1. Selecione o ícone de email para enviar o email. Como alternativa, selecione o ícone de cópia para copiar o URL.

O Adobe Learning Manager envia o email usando o modelo **Perfil Criado (Externo/Parceiros)**. O e-mail contém o URL exclusivo selecionado, o limite de vagas para o perfil e a data de expiração do URL. Compartilhe o URL com os usuários que deseja convidar.

## Mover da página inicial herdada não conectada

As versões anteriores desta lista mostravam a opção **Não conectado**. Agora ele se chama **Página inicial não conectada (herdada)**.

A página inicial legada não conectada será descontinuada em uma versão futura. Se você o utilizar, vá para o menu não conectado no Experience Builder para manter a mesma funcionalidade.
