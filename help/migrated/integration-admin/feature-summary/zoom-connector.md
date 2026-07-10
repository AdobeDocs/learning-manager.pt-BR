---
description: Saiba como integrar o conector do Zoom ao Adobe Learning Manager
jcr-language: en_us
title: Conector do Zoom
contentowner: mmanuel
source-git-commit: 481eed24a5ac72329228c8d27b625d443bd637ce
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Conector do Zoom no Adobe Learning Manager

## Introdução

O conector do Zoom no Adobe Learning Manager permite uma integração perfeita com o Zoom para oferecer sessões ao vivo de sala de aula virtual. Com essa integração, os professores podem hospedar reuniões do Zoom diretamente no Learning Manager, inscrever alunos e acompanhar dados de participação e conclusão. Os alunos recebem convites automáticos e podem ingressar nas sessões por meio de suas contas da Adobe Learning Manager. Após a sessão, os dados de presença e desempenho são sincronizados com a Adobe Learning Manager para fins de relatório e acompanhamento.

## Configurar o conector do Zoom

Para configurar o conector do Zoom:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco **Zoom**.

   ![](assets/zoom-connector1.png)
   _Configurar o conector do Zoom no Adobe Learning Manager_

3. Selecione **Conectar**. A página Configuração do conector do Zoom é aberta.
4. Digite os seguintes detalhes da conta nos respectivos campos. Você pode obter essas credenciais do administrador da conta do Zoom:

   * Nome da conexão
   * ID da conta do Zoom
   * ID do cliente
   * Segredo do cliente
   * Endereço de email do superadministrador

   ![](assets/zoom-connector2.png)
   _Digite os detalhes da configuração para definir o conector do Zoom_

5. Selecione **Conectar** para estabelecer a integração.

>[!NOTE]
>
>Ao habilitar o conector, **os alunos devem usar o mesmo endereço de email** para suas contas do Zoom e do Adobe Learning Manager para garantir que os dados do usuário sejam sincronizados corretamente.

## Criar cursos do Zoom

Depois que a conexão for estabelecida:

1. Faça logon como **Autor** e crie um novo curso de Sala de Aula Virtual.
2. Selecione **Zoom** como o sistema de conferência durante a criação do curso.
3. Atribua alunos ao curso por meio de administradores, gerentes ou por meio da autoinscrição.
4. Após a inscrição, os alunos recebem um e-mail com os detalhes do curso.
5. Os alunos podem fazer logon na conta da Adobe Learning Manager para acessar o curso e ingressar na sessão de zoom.

## Rastrear a participação e a conclusão

Após o término da sessão virtual:

* O Adobe Learning Manager recebe automaticamente o status de conclusão do Zoom.
* Os administradores podem exibir os relatórios de participação e pontuação no Adobe Learning Manager para monitorar a participação e o desempenho do aluno.

## Criar um aplicativo OAuth de servidor para servidor do Zoom

Para usar o conector do Zoom com o Adobe Learning Manager, você deve criar um aplicativo OAuth de servidor para servidor do Zoom e configurar os escopos necessários.

### Escopos OAuth necessários

Ao criar o aplicativo no Zoom, verifique se os seguintes escopos estão selecionados:

```
| Scope Description | Zoom Scope |
|---|---|
| View all user meetings | meeting:read:admin |
| View and manage all user meetings | meeting:write:admin |
| View report data | report:read:admin |
| View all user information | user:read:admin |
| Manage users | user:write:admin |
| Add a meeting registrant | meeting:write:registrant:admin |
| List all meeting registrants | meeting:read:list_registrants:admin |
| Manage sub-account meetings | meeting:write:meeting:master |
| View meeting participants report | report:read:list_meeting_participants:admin |
```
