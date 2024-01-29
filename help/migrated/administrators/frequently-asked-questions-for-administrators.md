---
jcr-language: en_us
title: Perguntas frequentes para administradores
description: Perguntas frequentes para administradores do Adobe Learning Manager
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 0%

---



# Perguntas frequentes para administradores

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Continue lendo para conhecer as perguntas frequentes do Learning Manager associadas à função Administrador. </p></td>
  </tr>
 </tbody>
</table>

+++Posso adicionar usuários em massa? Como?

Sim, você pode adicionar usuários em massa usando o recurso de upload de CSV. Clique em  [aqui](/help/migrated/administrators/add-users-in-bulk.md) para obter mais informações.

+++

+++Eu digito incorretamente a id de e-mail ao criar logon para meus alunos. Como corrigir isso?

Para corrigir o logon do usuário, é necessário importar CSV no Learning Manager. Um arquivo CSV de exemplo é anexado na parte inferior desta página para sua referência. Como o email é considerado um identificador exclusivo de uma pessoa, ele não pode ser editado. Siga estas etapas:

1. Adicione o mesmo usuário com a ID de e-mail correta no CSV e verifique se ele permanece como Gerente de outros usuários adicionando sua ID de e-mail à coluna “E-mail do Gerente do Funcionário” no CSV de exemplo.
1. Adicione outros usuários em sua conta ao CSV, incluindo você mesmo
1. Importe este arquivo no aplicativo de administração do Learning Manager->Usuários->Adicionar->Importar CSV
1. Mapeie todos os campos, conforme solicitado na caixa de diálogo, para as colunas CSV correspondentes.
1. Clique em Salvar.

Os usuários devem ser adicionados na página Alunos.

[CSV.csv de exemplo do Learning Manager](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Como configurar alertas?

Na versão 1.0 do Adobe Learning Manager, você pode criar notificações. Consultar  [pergunta de notificações](/help/migrated/administrators/feature-summary/user-notifications.md) para obter mais informações.

+++

+++Como adicionar certificados para os cursos?

O Adobe Learning Manager não fornece certificados para os cursos. No entanto, o administrador pode criar medalhas para cada curso clicando na guia Medalhas no painel esquerdo. Quando o administrador inscreve alunos em um curso, ele também pode associar uma medalha junto com o curso.

+++

+++Como importar assinaturas para os certificados?

No Adobe Learning Manager, não há nenhum recurso para importar assinaturas para a certificação ou medalha.

+++

+++Posso configurar um calendário para os cursos? Como?

Na versão 1.0 do Adobe Learning Manager, não temos nenhuma provisão para configurar o calendário dos cursos.

+++

+++Como inscrever diretamente os alunos da lista de espera?

Os alunos são colocados em lista de espera de qualquer curso em sala de aula quando as vagas são limitadas, com base na ordem de inscrição. Os administradores podem selecionar os alunos da lista de espera e atribuir vagas que ultrapassam o limite de vagas para qualquer curso em sala de aula. Os alunos são inscritos no curso assim que o administrador atribui uma vaga.

1. Clique em Cursos no painel esquerdo depois de fazer logon como administrador.
1. Na lista de cursos disponíveis, clique no nome do curso de qualquer curso de sala de aula de sua escolha. Uma nova página é exibida com informações detalhadas sobre o curso.
1. Clique em Lista de espera no painel esquerdo da página de detalhes do curso. Uma lista de alunos na lista de espera é exibida na página.
1. Selecione os alunos e clique em Atribuir vagas para inscrever os alunos diretamente nos cursos, substituindo o limite de vagas.

Para obter mais informações, consulte  [lista de espera e presença](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) recurso.

+++

+++Como registrar a participação dos alunos do módulo de sala de aula?

Sim, você pode registrar a participação seguindo as etapas abaixo:

1. Clique em Cursos no painel esquerdo depois de fazer logon como administrador.
1. Na lista de cursos disponíveis, clique no nome do curso de qualquer módulo de sala de aula/curso da sua escolha. Uma nova página é exibida com informações detalhadas sobre o curso.
1. Selecione os alunos e clique em Salvar para registrar a conclusão do curso.

Se houver vários módulos em um curso e o aluno tiver concluído apenas um deles, você pode selecionar um único módulo e clicar em Salvar para marcar a conclusão para o aluno. Se o aluno concluir todos os módulos de um curso, você pode clicar na opção Selecionar tudo e clicar em Salvar.

Para obter mais informações, consulte  [lista de espera e presença](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) recurso.

+++

+++Como incluir a opção de feedback N3?

Você pode adicionar o feedback N3 enquanto inscreve os alunos nos cursos. Adicione a pergunta do feedback N3 seguindo as etapas abaixo:

1. Clique em Cursos no painel esquerdo depois de fazer logon como administrador. As listas de todos os cursos são exibidas na página do lado direito.
1. Clique no quadro do curso ao qual você deseja adicionar o feedback N3
1. Clique no padrão da instância no painel esquerdo.
1. Clique no círculo no botão de alternância ao lado de N3 - Feedback de mudança de comportamento para selecioná-lo.
1. Adicione pergunta de feedback N3 na área de texto abaixo da pergunta N3.

+++

+++Como buscar a indicação do gerente para o curso nomeado pelo gerente?

Como administrador, você pode solicitar a indicação do gerente para os cursos seguindo as etapas abaixo:

1. Clique em Cursos no painel esquerdo
1. Passe o mouse sobre qualquer curso indicado pelo gerente e clique em **[!UICONTROL Buscar indicação do gerente]**.

1. Na lista de instâncias, clique em **[!UICONTROL Gerentes indicados]** link seguido por **[!UICONTROL Adicionar Gerentes]** link.

1. Adicione o nome do gerente, o número de licenças atribuídas e clique na marca de seleção para salvar as alterações.

Ao criar os cursos, o autor escolhe o tipo de curso como Indicado pelo gerente.

+++

+++Como inscrever o aluno em um curso específico?

Inscreva os alunos nos cursos seguindo as etapas abaixo:

1. Clique em Cursos no painel esquerdo depois de fazer logon como administrador. A lista de todos os cursos é exibida na página do lado direito.
1. Escolha o curso ao qual deseja adicionar alunos e passe o mouse sobre ele.
1. Clique em Inscrever alunos e adicione o nome dos alunos. **Observação:** Você pode adicionar um ou vários alunos por vez.

+++

+++Como atribuir alunos a uma habilidade específica?

Atribua alunos a competências seguindo as etapas abaixo:

1. Clique em **[!UICONTROL Habilidades]** no painel esquerdo depois de fazer logon como administrador.
1. Selecione uma ou várias habilidades clicando nas caixas de seleção em relação a cada competência e clique em **[!UICONTROL Ações]** no canto superior direito da página.
1. Clique em Atribuir aos usuários.
1. Comece a digitar o nome do usuário, escolha na lista suspensa e clique em **[!UICONTROL Salvar]**.

   >[!NOTE]
   >
   >Você pode inscrever vários alunos para obter habilidades clicando em Adicionar mais usuários e repetindo a 4ª etapa.

+++

+++Como criar uma sessão do programa de aprendizado?

Para criar um programa de aprendizado, siga as etapas abaixo:

1. Clique em Programa de aprendizado no painel esquerdo. A página Programas de aprendizado é exibida com uma lista de programas de aprendizado existentes.
1. Clique em Adicionar no canto superior direito da página.\
   Insira o nome do programa, a visão geral, a descrição e clique em Salvar.
1. Clique em Cursos no painel esquerdo.
1. Adicione um ou vários cursos clicando em + em cada quadro do curso.

   >[!NOTE]
   >
   >Você precisa publicar o programa de aprendizado antes de inscrever alunos ou uma instância.

1. Clique em Instâncias no painel esquerdo e clique em **[!UICONTROL Adicionar novas instâncias]** no canto direito da página para incluir detalhes da instância.

Para obter mais informações sobre programas de aprendizado, consulte  [Recurso Programas de aprendizado.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Como modificar ou personalizar relatórios para todas as funções?

Clique na seta suspensa no canto superior direito de cada relatório para editar/modificar relatórios. Clique em Salvar após concluir as alterações e visualize o relatório modificado.

+++

+++Como modificar cursos, programas de aprendizado e perfil da empresa?

Você pode editar cursos ou programas de aprendizado mesmo depois de publicá-los. Para obter mais informações, consulte  [Cursos](/help/migrated/administrators/feature-summary/courses.md) e  [programas de aprendizado](/help/migrated/administrators/feature-summary/learning-programs.md) Conteúdo de ajuda.

Para modificar o perfil da empresa, clique em **[!UICONTROL Configurações]** no painel esquerdo e clique em **[!UICONTROL Alterar]** no canto superior direito da página.

+++

+++Como pesquisar os cursos?

Clique em Cursos no painel esquerdo depois de fazer logon como administrador. Uma lista de todos os cursos disponíveis é exibida.

Você pode pesquisar cursos de duas maneiras:

1. Clique no ícone de pesquisa exibido no canto superior direito. Um campo de pesquisa é exibido. Digite o nome do curso ou qualquer palavra-chave associada aos seus cursos para localizá-los.
1. Filtrando a lista de cursos usando os filtros.

Você pode filtrar os cursos por estado, como Todos, Publicado e Retirado clicando em cada uma dessas opções. Você também pode pesquisar com base em competências clicando em Competências e escolhendo cada uma delas.

Com base na sua escolha, você pode exibir a lista filtrada de cursos e selecionar os cursos necessários.

+++

+++Posso alterar os temas do aplicativo? Como?

Sim, você pode alterar os temas e a marca do aplicativo Learning Manager de acordo com os requisitos da sua organização. Um conjunto de cinco imagens representativas é fornecido para visualizar as alterações do tema de cores antes de aplicá-las ao aplicativo. Navegue por essas imagens clicando nos símbolos &lt; e > no lado esquerdo e direito das imagens, respectivamente, para visualizar.

Clique em **[!UICONTROL Marca]** no painel esquerdo para atualizar o nome da sua organização, altere o subdomínio, os estilos de registro e os temas. Clique em **[!UICONTROL Editar]** adjacentes a cada um desses tópicos para modificar o conteúdo.

Consulte  [Ajuda sobre temas de cores e marcas](/help/migrated/administrators/feature-summary/themes.md) para obter mais informações.

+++

+++Como configurar medalhas para os cursos?

1. Clique em Medalhas no painel esquerdo depois de fazer logon como administrador.
1. Clique em Adicionar no canto superior direito da página exibida.
1. Adicione o nome da medalha.
1. Carregue a medalha clicando em Carregar medalha e clique em Salvar.

+++

+++Como configurar pontos de gamificação para os cursos?

Você pode configurar pontos de gamificação para os alunos seguindo as etapas abaixo:

1. Clique em Gamificação depois de fazer logon como administrador. Uma página é exibida com uma lista de níveis de bronze, prata, ouro e platina e os pontos necessários para atingir o correspondente para cada nível. Uma lista de tarefas e pontos correspondentes estão disponíveis.
1. Clique no ícone Editar ao lado de cada tarefa para configurar/modificar os pontos.

Consultar  [Recurso de gamificação](/help/migrated/administrators/feature-summary/gamification.md) para obter mais informações.

+++

+++Como criar relatórios para gerentes e alunos?

Você pode criar relatórios seguindo as etapas abaixo:

1. Clique em Relatórios no painel esquerdo. A página Resumo do relatório é exibida.
1. Na página Relatórios, clique em **[!UICONTROL Adicionar]** no canto superior direito.

   **[!UICONTROL Adicionar relatório]** é exibida.

1. Preencha todos os campos obrigatórios e clique em Salvar.

Somente administradores e gerentes podem criar ou exibir relatórios. Consulte [recurso de relatórios](/help/migrated/administrators/feature-summary/reports.md) para obter mais informações.

+++

+++Como alterar as funções de aluno, gerente e autor?

Você pode alternar o logon da sua conta para outras funções, como aluno, gerente e autor, sem fazer logoff da sua conta.

1. Clique na seta suspensa ao lado da imagem do seu perfil no canto superior direito da página.\
   Um menu pop-up é exibido.
1. Selecione cada função disponível para obter acesso às respectivas contas de função.

+++

+++Como incluir notificações para os usuários?

Gerentes, autores e alunos podem ver notificações com base nas atividades do curso. O administrador pode ativar/desativar as notificações para todos os usuários seguindo as etapas abaixo:

1. Clique em Modelos de e-mail no painel esquerdo e escolha as guias Geral, Inscrições do usuário, Conclusões e Feedback.
1. Nos eventos listados abaixo, clique nos botões de alternância Não/Sim ao lado de **cada **evento e escolha Sim para ativar a notificação. Clique em Não para desativar o envio de notificações para um evento específico.

+++

+++Como permitir a inscrição externa para os cursos?

O Adobe Learning Manager fornece a você a facilidade de inscrever membros de departamentos externos ou funcionários externos de sua organização no aplicativo.

1. Clique em **[!UICONTROL Usuários]** no painel esquerdo.
1. Clique em **[!UICONTROL Externo]** no painel esquerdo.
1. Clique em **[!UICONTROL Adicionar]** no canto superior direito da página.

   A caixa de diálogo Adicionar usuário é exibida.

1. Adicione o nome do perfil, e-mail do gerente, vagas atribuídas e informações de expiração. Você também pode adicionar imagem ao perfil externo.
1. Clique em **[!UICONTROL Salvar]**.

O administrador pode copiar o URL de registro e enviá-lo ao grupo de inscrição externo. Os usuários externos podem se registrar, fazer logon no aplicativo Learning Manager e acessar os seus cursos.

+++

+++Como adicionar questionário para o feedback N1?

Crie um questionário de feedback que pode ser usado pelos alunos após a conclusão dos cursos. Três perguntas de exemplo estão disponíveis por padrão. Siga as etapas abaixo para criar um questionário.

1. Clique em Feedback no painel esquerdo. Uma janela de questionário de feedback é exibida.
1. Clique em **[!UICONTROL Editar]** para adicionar/modificar o questionário.

Você pode adicionar um conjunto de questionários e optar por não exibi-los se não precisar. Clique na caixa de seleção para ativar/desativar uma pergunta específica.

+++

+++Como configurar as habilidades e os níveis?

1. Clique em Competências no painel esquerdo da janela Administrador.
1. Clique em Adicionar para adicionar novas competências.
1. Adicione o nome da competência, a descrição e os créditos correspondentes de acordo com cada nível.

   Por padrão, um nível único com 0 créditos estará disponível para cada competência.

1. Clique em [!UICONTROL **Adicionar nível**] para adicionar um novo nível a cada competência e clique em Salvar. Você pode adicionar até 5 níveis.

Depois que a competência é salva, não é possível remover níveis da competência. O administrador também pode atribuir alunos a uma determinada competência e nível.

+++

+++Como configurar o sistema de faturamento para os cursos da minha organização?

1. Clique em [!UICONTROL **Faturamento**] no painel esquerdo.

   As informações de cobrança são exibidas na página.

1. Clique no botão [!UICONTROL **Assinar**] guia.
1. Digite o número de pacotes que deseja solicitar no campo Pacotes do aluno e clique em Fazer pedido no canto superior direito da página.

   Escolha o número de pacotes com base no número de alunos da sua organização e faça o seu pedido. Para um processo orientado por ordem de compra, escreva-nos em  [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Insira suas informações de contato, escolha o tipo de cartão de crédito, forneça os detalhes do cartão de crédito e clique em Concluir pedido.

Consultar [Gerenciamento de faturamento](/help/migrated/administrators/feature-summary/billing-management.md) para obter mais informações.

+++

+++É possível personalizar o design do certificado? Como?

No Adobe Learning Manager, você pode reconhecer os alunos emitindo medalhas. Consulte o recurso Medalhas para mais informações.  Consulte também o recurso de certificação.

+++

+++Como configurar o perfil da minha empresa?

1. Depois de fazer logon como administrador, clique em **[!UICONTROL Informações da empresa]** no painel esquerdo.
1. Adicione o perfil da empresa, subdomínio e logotipo clicando em cada uma dessas opções na página.

+++

+++Como adicionar cursos?

Para adicionar cursos, você precisa mudar sua função como autor. Você só pode exibir a lista de cursos disponíveis com base em seu estado como **[!UICONTROL Concluído]**, **[!UICONTROL Publicado]** e **[!UICONTROL Retirado]**.

Para exibir os cursos, clique em **[!UICONTROL Cursos]** no painel esquerdo. Consultar  [Criação de cursos](/help/migrated/administrators/feature-summary/courses.md)para obter mais informações

+++

+++Como adicionar funções diferentes ao aplicativo?

Para adicionar novos usuários, siga as etapas abaixo:

1. Clique em Usuários no painel esquerdo depois de fazer logon como administrador. Você também pode adicionar usuários clicando em Introdução no painel esquerdo da janela e clicando em Adicionar usuários.
1. Para adicionar novos usuários, clique em Adicionar no canto superior direito da página.

Por padrão, todos os novos usuários são atribuídos com uma função de aluno. Você pode atribuir funções de administrador ou autor aos alunos clicando em **[!UICONTROL Ações]** no canto superior direito da página e escolhendo **[!UICONTROL Atribuir Função]** > **[!UICONTROL Criar autor]** ou **[!UICONTROL Criar administrador]**.

Consultar  [Adicionar novos usuários](/help/migrated/administrators/feature-summary/add-users-user-groups.md) para obter informações detalhadas sobre como adicionar alunos, autores e administradores.

+++

+++Como alterar uma imagem de fundo para um aluno?

Entre em contato com a equipe de suporte do Learning Manager.

+++

+++Onde encontrar a ID da minha conta do Learning Manager?

Você pode obter a ID da conta no navegador onde o Learning Manager está aberto.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++
