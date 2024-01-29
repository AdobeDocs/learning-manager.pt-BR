---
jcr-language: en_us
title: Adicionar locais de sala de aula
description: Os administradores agora podem configurar uma biblioteca de locais de sala de aula. Para cada local da sala de aula, os administradores podem definir os metadados que incluem o nome do local, o limite de vagas, bem como informações adicionais, como o URL do local. Os autores e os administradores podem usar esses locais pré-configurados de sala de aula para configurar eventos de treinamento ministrados pelo professor (módulos de sala de aula).
contentowner: saghosh
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---



# Sala de aula

## Visão geral

Os administradores agora podem configurar uma biblioteca de locais de sala de aula. Para cada local da sala de aula, os administradores podem definir os metadados que incluem o nome do local, o limite de vagas, bem como informações adicionais, como o URL do local. Os autores e os administradores podem usar esses locais pré-configurados de sala de aula para configurar eventos de treinamento ministrados pelo professor (módulos de sala de aula).

Você pode usar as duas seguintes maneiras para adicionar um local de sala de aula.

## Adicionar sala de aula usando a interface do usuário

Você pode adicionar um local da sala de aula usando a interface do usuário:

1. No aplicativo do administrador (a interface para funções de administrador), clique em **[!UICONTROL Configurações]** > **[!UICONTROL Locais de sala de aula]**.

1. Clique no botão **[!UICONTROL Adicionar mais]** botão.

1. No menu **[!UICONTROL Local da sala de aula]** , insira os seguintes detalhes:

   * Digite o **[!UICONTROL Nome do Local da Sala de Aula]**. Use um nome exclusivo. Caso contrário, o Learning Manager exibirá uma mensagem de erro.
   * Digite a descrição do local na caixa **[!UICONTROL Informações do local]** campo. Este campo é opcional.
   * Digite o **[!UICONTROL URL do local]**. O aluno pode ver essas informações nos detalhes da sala de aula. O URL também pode ser um URL de localização de mapas, se necessário. Este é um campo opcional.
   * Digite o número de licenças disponíveis no **[!UICONTROL Limite de vagas]** campo. Isso indica a capacidade da sala de aula. Esse valor pode ser alterado ao criar o evento real de treinamento ministrado pelo professor.

   ![](assets/add-classroom-location.png)

   *Adicionar um local de sala de aula*

Depois de adicionar o local, o **[!UICONTROL Configurações]** > **[!UICONTROL Locais de sala de aula]** A página lista as salas de reunião:

![](assets/list-meeting-rooms.png)

*Exibir todas as salas de reunião*

A lista tem os seguintes campos:

**[!UICONTROL Nome do local]** - Nome do local da sala de aula.

**[!UICONTROL Sessões futuras]** - Número de eventos que ocorrerão no local correspondente. Clique no número para exibir os detalhes em uma caixa de diálogo.

![](assets/sessions-list.png)

*Exibir sessões futuras*

A caixa de diálogo exibe os detalhes de cada sessão, incluindo o nome da sessão, o nome do treinamento que inclui a sessão e o horário da sessão. A hora exibida se alinha com o fuso horário do sistema do aluno.

O **[!UICONTROL Sessões futuras]** exibições de campo **zero** quando a sala de aula não é usada para nenhuma sessão ou quando a sala de aula está associada a sessões passadas.

**URL do local** - URL fornecido ao criar o local da sala de aula.

**Informações do local** - As informações de sala de aula que você forneceu ao criar a sala de aula.

## Adicionar sala de aula usando CSV

Como alternativa, você pode adicionar um ou mais locais de sala de aula importando um CSV que contenha as informações da sala de aula.

Entrada **[!UICONTROL Aplicativo do administrador]** > **[!UICONTROL Configurações]** > **[!UICONTROL Locais de sala de aula]**, clique no botão **[!UICONTROL Importar CSV de locais]** botão. Navegue até o local que contém o arquivo CSV e selecione o arquivo.

O arquivo CSV usa esses campos para armazenar detalhes sobre um ou mais locais de sala de aula:

* nome
* informações
* url
* LimitodeAssentos

Você pode personalizar os cabeçalhos.

O arquivo CSV deve conter obrigatoriamente todas as colunas na mesma ordem especificada aqui.

Depois que o sistema importa o arquivo CSV, os locais são adicionados à biblioteca.

## Pesquisar salas de aula

Um autor ou administrador pode começar a digitar o nome do local para ver os resultados relevantes que começam a aparecer. Um autor ou administrador pode selecionar um local nos resultados exibidos. Se nenhum local for exibido nos resultados do preenchimento automático, o usuário ainda poderá adicionar o novo nome do local da sala de aula. Observe que esse nome de local criado usando o fluxo de trabalho de criação da sessão não é adicionado à biblioteca de locais criada pelo administrador.

Quando uma sala de aula é adicionada, a plataforma de aprendizado também indica se a sala de aula já está reservada no período mencionado. Ele até fornece horários alternativos como sugestões. Portanto, isso permite que o autor ajuste o horário da reunião se decidir usar o mesmo local da sala de aula.

![](assets/classroom-search.png)

*Pesquisar salas de aula*

## Limitar a lista predeterminada de professores

Atualmente, os usuários podem adicionar qualquer usuário registrado como professor ao criar uma sessão de sala de aula ou sala de aula virtual. Essa funcionalidade permanece inalterada nesta versão.

No entanto, os administradores agora têm uma opção adicional para controlar ainda mais quem é atribuído como professor na plataforma de aprendizado. Isso evita a adição acidental de um novo professor ao criar uma sessão.

## Administrador

Um administrador pode selecionar o **[!UICONTROL Gerenciamento de professores]** opção (disponível em **[!UICONTROL Aplicativo do administrador]** > **[!UICONTROL Configurações]** > **[!UICONTROL Geral]**) para garantir que apenas os usuários que são professores predeterminados possam ser adicionados como um professor para uma sessão.

Para configurar um professor, os administradores podem selecionar **[!UICONTROL GERENCIAR]** > **[!UICONTROL Usuários]** para abrir a página Gerenciamento de usuários, selecione um usuário e atribua a função de professor ao usuário (usando **[!UICONTROL Ações]** > **[!UICONTROL Atribuir Função]**).

## Autor

Se o administrador selecionar a opção **[!UICONTROL Gerenciamento de professores]** , um autor só pode pesquisar e adicionar os usuários com a função de professor para as sessões de sala de aula, sessões de sala de aula virtual, listas de verificação e módulos de envio de arquivos.

Além disso, o autor pode:

* Adicionar e remover professores das sessões existentes.
* Adicionar professores às sessões existentes que já têm um ou mais professores.

Portanto, depois que um administrador habilita o **[!UICONTROL Gerenciamento de professores]** , somente os usuários com a função Professor podem ser adicionados como professor.

>[!NOTE]
>
>Isso não é aplicável ao migrar sessões usando o arquivo CSV de sessões. Nesse caso, um usuário que não tem a função de professor pode ser adicionado como professor.

## Cancelar sessão existente

Um autor ou administrador pode cancelar uma sessão e reagendá-la, se necessário.

Quando um usuário cancela uma sessão, o sistema envia um e-mail de cancelamento de reunião a todos os alunos e professores inscritos. O e-mail inclui os detalhes da sessão atualizada.

Há um modelo chamado **[!UICONTROL Cancelamento de sessão]** que ajuda no cancelamento de uma sessão.

Na guia **[!UICONTROL Instância do curso]** cada sessão listada em uma instância do curso inclui uma opção para cancelar a sessão.

![](assets/cancel-session.png)

*Cancelar uma sessão existente*

Ao clicar no botão **[!UICONTROL Cancelar sessão]** , uma mensagem de aviso é exibida.

Na caixa de diálogo de mensagem de aviso, se você clicar em **[!UICONTROL Continuar]**, o sistema cancela a sessão.

O sistema também limpa os seguintes detalhes após cancelar uma sessão:

* Data de início da sessão
* Data de término da sessão
* Hora de início da sessão
* Hora de término da sessão
* Professores adicionados à sessão
* URL da sala de aula virtual
* Local/local adicionado à sessão
* Limite de listas de espera adicionado pelo professor

## Administrador

Na guia **[!UICONTROL Instância do curso]** um administrador pode cancelar uma ou mais sessões. Depois que o administrador cancela uma sessão, o sistema limpa todos os detalhes da sessão, exceto o limite de vagas.

Além disso, um administrador pode:

* Exiba os alunos inscritos e os alunos na lista de espera de uma sessão.
* Cancelar a inscrição dos alunos em um curso com uma ou mais sessões canceladas.
* Marcar presença para sessões canceladas.
* Marcar um curso como concluído que contém uma ou mais sessões canceladas.
* Reagendar uma sessão cancelada.
* Adicionar um professor a uma sessão cancelada ao reagendá-la.

Observe que, mesmo após o cancelamento, os alunos inscritos na instância de treinamento continuam inscritos. Seus status de inscrição - incluindo inscrição confirmada, lista de espera e aguardando aprovação do gerente - não são alterados. Isso é útil porque o administrador pode configurar e reagendar a sessão cancelada no futuro.

## Autor

Na guia **[!UICONTROL Instância do curso]** um autor pode cancelar uma ou mais sessões. Depois que o autor cancela uma sessão, o sistema limpa todos os detalhes da sessão, exceto o limite de vagas.

Portanto, um autor pode usar o **[!UICONTROL Cancelar sessão]** links para cancelar uma ou mais sessões de sala de aula ou sessões de sala de aula virtual disponíveis na mesma instância ou em instâncias diferentes do curso.
