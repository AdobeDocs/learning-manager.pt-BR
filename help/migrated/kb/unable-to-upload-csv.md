---
description: Ao carregar um CSV, um erro é exibido. Continue lendo para resolver o problema.
jcr-language: en_us
title: Não é possível carregar CSV
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---



# Não é possível carregar CSV

## Erro: Truncamento de dados: Dados muito longos para a coluna

Ao tentar carregar um CSV no Adobe Learning Manager, você vê a seguinte mensagem de erro.

![](assets/csv-upload-failed.png)

*Mensagem de erro informando que o processamento de CSV falhou*

## Causa

O erro ocorre se os dados presentes na coluna especificada excederem o limite de caracteres definido para a coluna.

## Resolução

* Abra o CSV.
* Verifique os dados na coluna mencionada no erro.
* Se houver um valor grande (por exemplo, maior que 60 caracteres), altere o valor para corrigir os dados.

## Erro: a primeira coluna no CSV exibe um caractere especial

Não é possível carregar um CSV porque a primeira coluna exibe um caractere especial ao mapear as colunas.

![](assets/csv-2.png)

*Caractere especial na coluna Nome*

## Causa

O problema ocorre quando o CSV é salvo como um formato UTF-8 no Excel. Quando você salva um CSV no Excel como UTF-8, o arquivo é salvo em um formato UTF-BOM. Você pode verificar isso usando o Notepad++ ou ao carregar um CSV no Learning Manager. Ao mapear as colunas, a primeira coluna exibe um caractere especial.

## Resolução

* **R:** Salvando pelo Excel:

   1. Abra o CSV no Excel.
   1. Salve o arquivo como um CSV normal.

* **B:** Salvar no Bloco de Notas ou no Notepad++:

   * Abra o CSV no Bloco de notas ou no Notepad++.
   * Salve o arquivo no formato UTF-8.

## Erro: Endereço de email do usuário já presente no sistema

Não é possível carregar um CSV porque o processamento de CSV falhou. Você verá a mensagem de erro abaixo:

![](assets/csv-3.png)

*Mensagem de erro para um usuário duplicado*

## Causa

Esse problema ocorre se houver um usuário que já esteja presente no sistema com o mesmo endereço de e-mail ou UUID.

## Resolução

### Cenário 1

**Contas nas quais a UUID não está ativada.**

Nesse cenário, há duas razões para esse erro:

1. O usuário que você está tentando adicionar é um gerente de um perfil externo. Para resolver isso, abra o perfil externo do qual o usuário faz parte, selecione o usuário, clique em **[!UICONTROL Ações]** > **[!UICONTROL Atribuir Função]** > **[!UICONTROL Gerente]** e altere o Gerente do perfil.
1. O usuário que você está tentando adicionar foi removido. Nesse cenário, você não poderá adicionar o usuário com o mesmo endereço de e-mail até que o processo de limpeza seja concluído. Como solução alternativa**, adicione ao usuário um endereço de e-mail secundário para fornecer acesso à plataforma. Quando o processo de limpeza estiver concluído, edite o usuário e altere o endereço de e-mail para o endereço de e-mail correto.

### Cenário 2

**Contas habilitadas para UUID.**

Para contas habilitadas para UUID, esse problema pode ocorrer se um usuário recebeu uma UUID que já está sendo usada por outro usuário na conta ou se o usuário tem um endereço de e-mail diferente.

Por exemplo: deve haver dois usuários, A e B, com endereços de e-mail,  <a@xyz.com> e <b@xyz.com> com UUID 1 e 2, respectivamente.

Agora, se você carregar um CSV que tenha a UUID do usuário A como 3 e a UUID do usuário B como 2, você verá um erro.

>[!TIP]
>
>Para resolver esse problema, **você deve ter o mesmo endereço de email e UUID para o usuário no CSV e no sistema.**

