---
jcr-language: en_us
title: Adicionar locais de sala de aula
description: Os administradores agora podem configurar uma biblioteca de locais de sala de aula. Para cada local da sala de aula, os administradores podem definir os metadados que incluem o nome do local, o limite de vagas, bem como informações adicionais, como o URL do local. Os autores e os administradores podem usar esses locais pré-configurados de sala de aula para configurar eventos de treinamento ministrados pelo professor (módulos de sala de aula).
contentowner: saghosh
exl-id: 51a1e38f-d4e2-4c19-bbf7-6696505c0dfd
source-git-commit: 8cb8a95812c97b0b59a2ae5188500cfafe09bd27
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 54%

---

# Sala de aula

## Visão geral

Os administradores agora podem configurar uma biblioteca de locais de sala de aula. Para cada local da sala de aula, os administradores podem definir os metadados que incluem o nome do local, o limite de vagas, bem como informações adicionais, como o URL do local. Os autores e os administradores podem usar esses locais pré-configurados de sala de aula para configurar eventos de treinamento ministrados pelo professor (módulos de sala de aula).

Você pode usar as duas seguintes maneiras para adicionar um local de sala de aula.

## Adicionar sala de aula usando a interface do usuário

Você pode adicionar um local da sala de aula usando a interface do usuário:

1. No aplicativo do administrador (a interface para funções de administrador), clique em **[!UICONTROL Configurações]** > **[!UICONTROL Locais de sala de aula]**.

1. Clique em **[!UICONTROL Adicionar]** > **[!UICONTROL Novo local]**.

1. No menu **[!UICONTROL Local da sala de aula]**, insira os seguintes detalhes:

   * Digite o **[!UICONTROL Nome do local]**. Use um nome exclusivo. Caso contrário, o Learning Manager exibirá uma mensagem de erro.
   * Digite a descrição do local no campo **[!UICONTROL Informações do local]**. Este campo é opcional.
   * Digite o **[!UICONTROL URL do local]**. O aluno pode ver essas informações nos detalhes da sala de aula. O URL também pode ser um URL de localização de mapas, se necessário. Este é um campo opcional.
   * Digite e selecione o **[!UICONTROL Região do Local]**. Este campo é opcional.
   * Digite o número de licenças disponíveis no campo **[!UICONTROL Limite de vagas]**. Isso indica a capacidade da sala de aula. Esse valor pode ser alterado ao criar o evento real de treinamento ministrado pelo professor.

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

**[!UICONTROL Limite de vagas]** - Exibe a capacidade da sala de aula.

**URL do local** - URL fornecido ao criar o local da sala de aula.

**Informações do local** - As informações de sala de aula que você forneceu ao criar a sala de aula.

### Editar os locais da sala de aula

Para editar os locais de sala de aula, siga as etapas abaixo:

1. No aplicativo do administrador (a interface para funções de administrador), selecione **[!UICONTROL Configurações]** > **[!UICONTROL Locais de sala de aula]**.

1. Passe o mouse sobre o local da sala de aula desejado que deseja editar.

1. Selecionar **[!UICONTROL Editar local da sala de aula]** ícone.

1. Modificar o local da sala de aula e selecionar **[!UICONTROL Salvar]**.

## Adicionar sala de aula usando CSV

Como alternativa, você pode adicionar um ou mais locais de sala de aula importando um CSV que contenha as informações da sala de aula.

Entrada **[!UICONTROL Aplicativo do administrador]** > **[!UICONTROL Configurações]** > **[!UICONTROL Locais de sala de aula]** > **[!UICONTROL Adicionar]**, clique no botão **[!UICONTROL Locais de importação em massa]** botão. Navegue até o local que contém o arquivo CSV e selecione o arquivo.

O arquivo CSV usa esses campos para armazenar detalhes sobre um ou mais locais de sala de aula:

* name
* informações
* url
* região
* limite de vagas

Você pode personalizar os cabeçalhos.

O arquivo CSV deve conter obrigatoriamente todas as colunas na mesma ordem especificada aqui.

Depois que o sistema importa o arquivo CSV, os locais são adicionados à biblioteca.

## Pesquisar salas de aula

Para pesquisar salas de aula, selecione o curso de sala de aula virtual e, em seguida, vá para **[!UICONTROL Instâncias]** > **[!UICONTROL Sessões]**. Um autor ou administrador pode começar a digitar o nome do local para ver os resultados relevantes que começam a aparecer. Eles podem, então, selecionar um local entre os resultados exibidos. Se nenhum local for exibido nos resultados do tipo adiantado, o usuário ainda poderá adicionar o novo nome do local da sala de aula. Observe que esse nome de local criado usando o fluxo de trabalho de criação da sessão não é adicionado à biblioteca de locais criada pelo administrador.

Quando uma sala de aula é adicionada, a plataforma de aprendizado também indica se a sala de aula já está reservada no período mencionado. Ela até fornece horários alternativos como sugestões. Portanto, isso permite que o autor ajuste o horário da reunião se decidir usar o mesmo local da sala de aula.

![](assets/classroom-search.png)

*Pesquisar salas de aula*

## Administrador

Como administrador, você pode gerenciar os professores e as instâncias do curso.

### Configurando professores:

No aplicativo de administração, em **[!UICONTROL Configurações]** > **[!UICONTROL Geral]**, os administradores podem encontrar o **[!UICONTROL Gerenciamento de professores]** opção. Esse recurso garante que apenas usuários pré-aprovados atribuídos como professores possam ser adicionados para conduzir sessões.

Para atribuir um professor, siga estas etapas:

1. Acesse o menu **[!UICONTROL Introdução]** e selecione **[!UICONTROL Usuários]** no painel esquerdo.

1. Selecione o usuário desejado.

1. Atribua ao usuário a função de professor selecionando **[!UICONTROL Ações]** > **[!UICONTROL Atribuir Função]**.

### Cancelando sessões:

Na guia **[!UICONTROL Instância do curso]** administradores podem cancelar uma ou mais sessões. Quando as sessões são canceladas, o sistema remove todos os detalhes da sessão, mas mantém o limite de vagas.

Além disso, os administradores podem:

* **[!UICONTROL Exibir inscrição]**: obtenha informações sobre alunos inscritos e na lista de espera para cada sessão.
* **[!UICONTROL Cancelar inscrição dos alunos]**: remova os alunos de um curso com sessões canceladas sem alterar seu status de inscrição.
* **[!UICONTROL Gerenciamento de Participação]**: marque a participação nas sessões, mesmo que elas sejam canceladas.
* **[!UICONTROL Conclusão do curso]**: os administradores podem marcar um curso como concluído mesmo se as sessões tiverem sido canceladas.
* **[!UICONTROL Reagendamento]**: agende sessões canceladas para datas posteriores e adicione um professor durante o reagendamento.

Observe que, após o cancelamento, os alunos permanecem inscritos na instância de treinamento. Seu status de inscrição—como inscrição confirmada, lista de espera e aguardando aprovação do gerente—permanece inalterado. Isso é útil porque o administrador pode configurar e reagendar a sessão cancelada no futuro.

## Autor

Se o administrador selecionar a opção **[!UICONTROL Gerenciamento de professores]** , um autor só pode pesquisar e adicionar os usuários com a função de professor para as sessões de sala de aula, sessões de sala de aula virtual, listas de verificação e módulos de envio de arquivos.

Além disso, o autor pode:

* Adicionar e remover professores das sessões existentes.
* Adicionar professores às sessões existentes que já têm um ou mais professores.

Portanto, depois que um administrador habilita o **[!UICONTROL Gerenciamento de professores]** , somente os usuários com a função de professor podem ser adicionados como professor.

>[!NOTE]
>
>Isso não é aplicável ao migrar sessões usando o arquivo CSV de sessões. Nesse caso, um usuário que não tem a função de professor pode ser adicionado como professor.

Na guia **[!UICONTROL Instância do curso]** um autor pode cancelar uma ou mais sessões. Quando as sessões são canceladas, o sistema remove todos os detalhes da sessão, mas mantém o limite de vagas.

Portanto, um autor pode usar o **[!UICONTROL Cancelar sessão]** links para cancelar uma ou mais sessões de sala de aula ou sessões de sala de aula virtual disponíveis na mesma instância ou em instâncias diferentes do curso.

## Restringir a lista predeterminada de professores

Atualmente, os usuários podem adicionar qualquer usuário registrado como professor ao criar uma sessão de sala de aula ou sala de aula virtual. Essa funcionalidade permanece inalterada nesta versão.

No entanto, os administradores agora têm uma opção adicional para controlar ainda mais quem é atribuído como professor na plataforma de aprendizado. Isso evita a adição acidental de um novo professor ao criar uma sessão.

## Cancelar sessão existente

Um autor ou administrador pode cancelar uma sessão e reagendá-la, se necessário.

Quando um usuário cancela uma sessão, o sistema envia um e-mail de cancelamento de reunião a todos os alunos e professores inscritos. O e-mail inclui os detalhes da sessão atualizada.

Há um modelo chamado **[!UICONTROL Cancelamento de sessão]** que ajuda no cancelamento de uma sessão.

Na página **[!UICONTROL Instância do curso]** cada sessão listada em uma instância do curso inclui uma opção para cancelar a sessão.

![](assets/cancel-session.png)

*Cancelar uma sessão existente*

Ao clicar no link **[!UICONTROL Cancelar sessão]**, é exibida uma mensagem de aviso.

Na caixa de diálogo de mensagem de aviso, se você clicar em **[!UICONTROL Continuar]**, o sistema cancela a sessão.

O sistema também limpa os seguintes detalhes após cancelar uma sessão:

* Data de início da sessão
* Data de término da sessão
* Hora de início da sessão
* Hora de término da sessão
* Professores adicionados à sessão
* URL da sala de aula virtual
* Local/lugar adicionado à sessão
* Limite de listas de espera adicionado pelo professor
