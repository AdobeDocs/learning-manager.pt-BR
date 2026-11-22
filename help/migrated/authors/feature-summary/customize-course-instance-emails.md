---
description: Personalize e-mails no nível do curso e no nível da instância no Adobe Learning Manager com o E-mail Builder e um layout fornecido pelo administrador.
jcr-language: en_us
title: Personalizar e-mails do curso e da instância no Email Builder
exl-id: 06499e3f-0610-4983-83f2-3e8b578fc8bf
source-git-commit: 172889a4ff67e54c8e7b9a39ef5f393af0a1d703
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%
---

# Personalizar e-mails do curso e da instância no Email Builder

Como autor, você pode personalizar e-mails para um curso ou para uma instância específica de um curso. Ambos os procedimentos começam em um layout fornecido pelo administrador.

## Personalizar um e-mail de nível de curso

1. Abrir o curso.
2. Selecione **Modelos de Email**.
3. Selecione **Layout do email do curso**.
4. Personalize o conteúdo do email. Para definir fontes, cores, linhas e botões.
5. Salve o modelo.
6. Publish o curso.

## Personalizar um email em nível de instância

Use um e-mail de nível de instância quando diferentes coortes precisarem de mensagens diferentes. Você gerencia essas coortes por meio de instâncias do curso.

1. Abra a instância do curso.
2. Abra o **Construtor de Email**.
3. Selecione um layout disponível ou herde o layout que a instância já usa.
4. Atualizar o conteúdo da mensagem.
5. Salve o modelo.

>[!NOTE]
>
>Quando ambos existem, os e-mails em nível de instância substituem os modelos em nível de curso.

## Usar a variável Título e uma imagem para cabeçalhos de email

Use a variável Title com um componente Image para criar o cabeçalho de e-mail em vez do componente Banner. A imagem do componente Banner não aparece em alguns clientes de email, como o Outlook.

A variável Title, EmailTitle, funciona como a variável ChannelName existente. Cada email tem seu próprio valor de título padrão.

Para adicionar um cabeçalho de título:

1. Adicione um componente Imagem para a imagem do cabeçalho.
2. Adicione um componente Texto e insira a variável de título na lista suspensa de variáveis no painel de configuração do componente.
3. Centralize o componente Texto. No layout global, coloque-o no cabeçalho superior.

   Emails individuais usam o cabeçalho do layout global por padrão. Em um email individual, você pode editar o componente Texto para:

4. Substituir a variável pelo texto personalizado
5. Adicionar texto antes ou depois da variável e manter `EmailTitle`

Se você adicionar uma imagem ao componente Banner, o Criador de e-mail mostrará um aviso de que a imagem pode não aparecer corretamente em alguns clientes de e-mail. O aviso sugere o uso de um componente Imagem e a variável de título.

## Solução de problemas

**Não é possível selecionar um layout.**
A herança do layout depende dos layouts pai disponíveis. Peça ao administrador para criar um layout de conta.

**Seu email não mostra alterações recentes no layout.**
O modelo pode ser desvinculado de seu layout. Modelos desvinculados não recebem mais atualizações de layout.

**Os alunos de uma instância recebem um email diferente do email do curso.**
Os e-mails em nível de instância substituem os modelos em nível de curso. Revise o modelo em nível de instância.

**Você não vê o Construtor de email para os emails do seu curso ou instância.**
O Adobe ativa o Construtor de e-mail em fases. Peça ao administrador para confirmar se o Construtor de e-mail está ativado para sua conta.

**A imagem do seu banner não aparece no email.**
Alguns clientes de email, como o Outlook, não exibem a imagem do componente Banner. Remova o componente Banner, adicione um componente Imagem e um componente Texto que usa a variável de título.
