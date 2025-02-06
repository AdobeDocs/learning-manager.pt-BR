---
description: Notas de versão do Adobe Learning Manager
jcr-language: en_us
title: Notas de versão do Adobe Learning Manager
contentowner: jayakarr
exl-id: ae9251b6-5326-42c2-881e-2ab3393d9e17
source-git-commit: 96e875a2b2cd2866a624068b5e8e18aabb39d888
workflow-type: tm+mt
source-wordcount: '26470'
ht-degree: 72%

---

# Notas de versão do Adobe Learning Manager

<!--<table>
 <tbody>
  <tr>
   <td><img src="assets/cp-prime-appicon-88x84.png"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> was launched in August 2015. As part of our continuous improvement efforts to enhance the product, we have been rolling out regular updates. Read on to know the features enhanced/issues fixed in update releases.<br></p></td>
  </tr>
 </tbody>
</table>-->

+++Atualização 99: versão de fevereiro de 2025 do Adobe Learning Manager

## Configurar o idioma da interface por meio do SAML

O Adobe Learning Manager (ALM) agora aceita um atributo SAML para o idioma. Esse atributo é mapeado para a interface do usuário e as configurações de idioma do conteúdo, garantindo uma interação tranquila com o LMS no idioma de sua preferência. A configuração dessas configurações de idioma é gerenciada por meio da plataforma IAM (Identity and Access Management), que utiliza SAML para logon único (SSO). Isso oferece suporte tanto a logons iniciados por provedor de serviços (SP) quanto a logons iniciados por provedor de identidade (IdP), permitindo que os usuários vejam a interface e o conteúdo em seu idioma escolhido.

Consulte este [artigo](/help/migrated/administrators/feature-summary/set-up-interface-language-through-saml.md) para obter mais informações.

## Aprimoramento nas APIs de migração

Anteriormente, os módulos de atividade com links externos migrados usando APIs (`GET /bulkimport/cansync` e `POST /bulkimport/startrun`) não exibiam a opção **[!UICONTROL Marcar como concluído]** para alunos após acessar o link. Esse problema foi resolvido. Agora, os módulos de atividade com links externos migrados por meio de APIs exibirão corretamente a opção **[!UICONTROL Marcar como concluído]** para os alunos.

## Classificação da funcionalidade no aplicativo do aluno

O recurso de classificação no aplicativo do aluno fornece recomendações personalizadas do curso com base no conteúdo e no idioma da interface. &#x200B; Esse aprimoramento simplifica o processo para que os alunos encontrem cursos em seu idioma de preferência e utilizem opções de classificação mais inteligentes.

Consulte este [artigo](/help/migrated/learners/feature-summary/catalogs.md#sorting-functionality-in-the-learner-app) para obter mais informações.

+++

+++Atualização 98: a versão de novembro de 2024 do Adobe Learning Manager

**Data de lançamento**: 16 de novembro de 2024

## Novidades desta versão

Consulte [Novidades do Adobe Learning Manager](/help/migrated/whats-new.md) para obter mais informações.
+++

+++Atualização 97: a versão de julho de 2024 do Adobe Learning Manager

**Data de lançamento:** 13 de julho de 2024

## Novidades desta versão

Consulte [Novidades do Adobe Learning Manager](/help/migrated/whats-new-july-2024.md) para obter mais informações.
+++

+++Atualização 96: a versão de março de 2024 do Adobe Learning Manager

**Data de lançamento:** 1 de março de 2023

## Novidades desta versão

Consulte [Novidades do Adobe Learning Manager](/help/migrated/whats-new-march-2024.md) para obter mais informações.
+++

+++Atualização 95: versão de novembro de 2023 do Adobe Learning Manager

**Data de lançamento:** 18 de novembro de 2023

## Novidades desta versão

Consulte [Novidades do Adobe Learning Manager](/help/migrated/whats-new-november-2023.md) para obter mais informações.
+++

+++Atualização 94

**Data de lançamento:** quinta-feira, 23 de agosto de 2023

## Novidades desta atualização

* Selecione o ícone de engrenagem do reprodutor para alterar a qualidade do vídeo.
* Altere a qualidade e a velocidade de um vídeo nas redes sociais.
+++

+++Atualização 93: a versão de julho de 2023 do Adobe Learning Manager

**Data de lançamento:** 10 de julho de 2023

Novidades desta versão

### Recomendações aprimoradas

O Adobe Learning Manager introduziu um sistema de recomendação novo e aprimorado para os cursos. Esse recurso de recomendações usa algoritmos de IA e interesses de usuários, como produtos, funções e níveis, para fornecer recomendações de conteúdo personalizadas.

### Várias Inscrições

Nesta versão do Adobe Learning Manager, estamos introduzindo o recurso de várias inscrições para alunos que permite que eles se inscrevam em mais de uma instância de um curso em um período ou em diferentes períodos de tempo.

### Descontinuação Do Conector Exavault

Esta versão do Adobe Learning Manager incluirá um novo conector, que usará o protocolo SFTP da família AWS Transfer.

Para obter mais informações, consulte [Novidades do lançamento do Adobe Learning Manager em julho de 2023](/help/migrated/whats-new-2023-july.md).
+++

+++Atualização: 92

**Data de lançamento:** 23 de junho de 2023

**Erros corrigidos nesta atualização**

* Depois de concluir um módulo, a API Grade não é acionada automaticamente, o que resulta na exibição da marca de seleção verde como esperado na Interface do usuário.
* Depois de concluir alguns módulos em um caminho de aprendizado ou uma certificação, a marca de seleção verde, que indica a conclusão bem-sucedida, não é exibida conforme esperado.
* O Adobe Learning Manager não é iniciado como esperado após o carregamento de um CSV de usuário com campos incorretos.
* O pop-up de aviso sobre como entrar em contato com o administrador também exibe outros endereços de e-mail.
* Todas as medalhas obtidas por um aluno não são exibidas na resposta.
* Durante a inscrição do usuário, um nome de usuário com &quot; &quot; deve ser aceito.

#### Reprodutor

* Adicione um menu para selecionar a resolução da tela ao reproduzir um vídeo.
+++

+++Atualização 91

**Data de lançamento:** sexta-feira, 1 de junho de 2023

### Conectores

* O conector do Adobe Connect requer APIs para enviar tokens CSRF. Para obter mais informações, consulte Melhorar a segurança da conta da Adobe Connect.

### Alteração da cadeia de caracteres

* Renomeamos a sequência de caracteres Classificar este treinamento para Classificar este curso, Classificar este caminho de aprendizado ou Classificar esta certificação, com base no treinamento que um aluno faz. Dependendo do tipo de treinamento, um aluno vê a sequência de caracteres de acordo.

### Erros corrigidos nesta atualização

* A descrição do aplicativo para dispositivos móveis Adobe Learning Manager da Play Store diz incorretamente que um aluno pode fazer um curso offline.
* Ocorreram problemas ao migrar o conteúdo (module_version.csv e course_module.csv) do LinkedIn para o Adobe Learning Manager.
* Se uma conta estiver em um estado inativo e tiver sido criada há mais de três anos, todos os usuários da conta serão excluídos do GDPR, independentemente do status dos usuários.
* No Aplicativo do instrutor, quando você define o limite da lista de espera para zero em uma sessão e salva a sessão, a interface do usuário exibe incorretamente &quot;Não aplicável&quot; em vez de zero.
* Ao gerar transcrições do aluno para o conector do Power BI, a coluna Duração do módulo ou treinamento (min) exibe valores nulos para determinados módulos de sala de aula ou de sala de aula virtual.
* Depois de marcar um curso como concluído para alunos em uma ou várias instâncias, todos os alunos do curso são marcados como concluídos, não apenas os alunos na instância ou instâncias atuais.
+++

+++Atualização 90

**Data de lançamento:** 04 de abril de 2023

### Erros Corrigidos Nesta Atualização

O logon no SAML falhará se o URL de logon com SSO contiver entity_id.
+++

+++Atualização 89: a versão de março de 2023 do Adobe Learning Manager

**Data de lançamento:** 04 de abril de 2023

### Novidades desta atualização

**Aprimoramentos na Experiência ILT (Instructor Led Training, treinamento ministrado por instrutor)**

Foram feitos vários aprimoramentos na experiência ILT (Instructor-Led Training, treinamento ministrado por instrutor). Os principais aprimoramentos incluem: capacidade de filtrar sessões de sala de aula com base no local, capacidade de alternar instâncias (VILT) sem perder o progresso, um novo “Assistente de agendamento” para gerenciar conflitos em professores de reserva e salas de aula, capacidade de anexar “Habilidades” aos professores e escolher professores com base nas habilidades.

**Melhorias na Lista de Verificação de Observação**:

Os autores agora podem selecionar “Gerente” e “Gerenciador de armazenamento” como o Observador para listas de verificação. Os gerentes podem visualizar e concluir as listas de verificação na interface do gerente sem precisar trocar a função para um professor. A notificação é enviada a um gerente quando uma lista de verificação é atribuída a ele.

**Usar qualquer câmera de aplicativo/smartphone para digitalizar códigos QR do Learning Manager**

Os alunos agora poderão usar qualquer aplicativo de digitalização do QR Code ou a câmera do smartphone para digitalizar os códigos QR gerados pelo Learning Manager para inscrição no curso, conclusão e muito mais.

**Aprimoramentos nos Relatórios**

Um novo relatório de utilização de instrutor, o relatório de revisão de treinamentos, o relatório de ajudas de tarefa e outros aprimoramentos na geração de relatórios.

**Suporte para Sessões &#39;Híbridas&#39;**

O Adobe Learning Manager agora oferece suporte à capacidade de criar sessões “híbridas” de ILT (Instructor Led Training, treinamento ministrado por instrutor). As sessões virtuais do ILT podem ser criadas com informações opcionais de local para que os alunos possam também participar da sessão pessoalmente, se estiverem disponíveis no local.

**Acompanhamento de progresso melhor para sala de aula e ILT virtual**

Os módulos Sala de aula e ILT virtual agora oferecem a capacidade de relatar o status do questionário de um aluno (aprovado ou reprovado) junto com o status de participação. Portanto, a participação e o sucesso do questionário podem ser considerados para decidir o progresso do aluno.

**Aplicativo Adobe Learning Manager para Microsoft Teams**

O novo aplicativo Adobe Learning Manager no Microsoft Teams foi desenvolvido para promover o aprendizado no fluxo de trabalho e impulsionar o aprendizado social. Os alunos poderão acessar o conteúdo de aprendizado na plataforma Microsoft Teams sem a necessidade de mudar para um navegador. Entre em contato com seu CSAM para obter a versão beta do aplicativo Adobe Learning Manager no MS Teams.

### Erros corrigidos nesta atualização

**Curso**

* Um autor personalizado não pode visualizar um módulo quando o curso está no estado &quot;UNDER_CONSTRUCTION&quot;. A resposta mostra o Erro 404.
* O título do curso na página do curso/adicionar de um aplicativo do autor excede quando o título do curso ultrapassa determinado limite de caracteres.

**Autor**

* No aplicativo Autor, o título do curso (se for longo) excede os limites da página ao criar um curso.
* Às vezes, um curso é adicionado, mesmo que nenhum autor seja selecionado.

**Relatórios do painel**

* As dicas de ferramenta são exibidas corretamente quando o idioma da interface é inglês, mas gera um erro de console quando o idioma da interface é diferente.
* Renomeie “Obrigatório” para “Obrigatório” no painel do aluno.

**Aplicativo do professor**

* O formato de hora no aplicativo do professor não é consistente com os outros aplicativos.

**Redes sociais**

* Para certos tipos de postagens, após a postagem, o painel social não abre como esperado.

**Admin**

* Um usuário com uma função personalizada não pode baixar recursos ao visualizar um curso.

**Modelos de e-mail**

* Quando um aluno cancela a inscrição em um programa de aprendizado que contém um curso de sala de aula/sala de aula virtual, ele não recebe nenhum e-mail de cancelamento.

**Ajudas de tarefa**

* Não é possível ver o nome do curso no widget Ajuda de tarefa.

**Publicação**

* A descrição do módulo adicionada no Adobe Captivate não fica visível no Learning Manager quando o módulo é publicado no ALM.

**Campos ativos**

* Quando um CSV com um grande número de registros está em processamento, ele leva um tempo significativo, durante o qual, se um usuário fizer logon e inserir um valor para um dos atributos, poderá criar um novo grupo de usuários que poderá resultar em erros de CSV. Para corrigir isso, quando a importação de CSV estiver em andamento, a mensagem pop-up do atributo Campos ativos será desativada e reativada assim que o upload do CSV for concluído.
* Se a coluna no arquivo csv de Usuários tiver o mesmo nome do campo ativo de usuários externos, o carregamento do csv falhará.

**Correções relacionadas à API**

* Na resposta learningObjects, o atributo bookmark está ausente.
* Uma entrada de acesso é criada ao gerar tokens de atualização oauth para usuários excluídos.
* A API do LO retorna o formato lo incorreto, pois os módulos de pré-trabalho foram considerados para calcular o tipo de curso junto com o conteúdo principal.

**Problemas conhecidos nesta atualização**

* O botão Compartilhar no catálogo do aluno não funciona conforme o esperado no navegador safari e no aplicativo MS Teams para dispositivos móveis e iPad.
* As notificações não são exibidas na guia Atividade depois que o aplicativo é removido em outros computadores.
Nada acontece quando você clica nas notificações na guia Atividade do aplicativo no iPhone 14.
* No aplicativo MS Teams, as notificações do Learning Manager (conclusão, inscrição, prazo e encerramento) não exibem o status e o nome do curso na guia Atividade.
* Um pop-up com conteúdo XML é exibida quando o administrador de integração não aprova o aplicativo MS Teams.
* O idioma da interface do usuário no aplicativo Adobe Learning Manager no MS Teams às vezes não muda conforme esperado quando o idioma é alterado.
* Não é possível interagir com a primeira notificação quando o foco está no Iframe (Guias Início e Catálogo).

**Limitações do aplicativo Adobe Learning Manager para dispositivos móveis**

* Exibição de conteúdo offline.
* Exibição em grade/lista na página Catálogo/Meu aprendizado.
* Várias tentativas de fazer um curso.
* Prazo final para inscrição em um cartão do curso.
* Em dispositivos iOS, as notificações por push não aparecem quando o aplicativo está em primeiro plano.
* Links profundos em notificações push não são redirecionados para a página de aterrissagem desejada.
* Clicar no botão Registrar interesse redirecionará para a Web.
* Ao responder ou comentar no Aprendizado Social, você não poderá anexar um arquivo.
* Você não poderá fazer logon no LinkedIn Learning.
+++

+++Atualização 88

**Data de lançamento:** 7 de março de 2023

### Melhorias De Desempenho Nesta Versão

Quando uma inscrição em massa dos alunos é executada, não haverá nenhum arquivo de log gerado para cada aluno.
Otimizamos o processamento de planos de aprendizado para contas grandes. Isso evita quaisquer problemas ou lentidão na pesquisa.
+++

+++Atualização 87

**Data de lançamento:** 1 de março de 2023

## Erros Corrigidos Nesta Atualização

* Um aluno não recebia o e-mail de cancelamento de sessão se o módulo CR/VC fosse removido do curso inscrito.
* Altere GetNotificationData de GET para POST. A implementação original produziu o erro, **IllegalArgumentException: o cabeçalho da solicitação é muito grande**, que levou a notificações com falha.
+++

+++Atualização: 86

**Data de lançamento:** 17 de fevereiro de 2023

### Erro Corrigido Nesta Versão

No aplicativo do aluno, a pesquisa de usuários e grupos de usuários está falhando devido a alguns problemas com as configurações de localidade.
+++

+++Atualização 85

**Data de lançamento:** terça-feira, 13 de fevereiro de 2023

### O que mudou nesta atualização

Adição de suporte para código de idioma de quatro letras ao filtrar idiomas em GET learningmanagerapi/v2/learningObjects.

### Erros Corrigidos Nesta Atualização

Para algumas localidades, a pesquisa retorna resultados incorretos.
Os metadados do curso são substituídos quando o curso tem mais de uma variante da mesma localidade.
+++

+++Atualização 84

**Data de lançamento:** sexta-feira, 2 de fevereiro de 2023

### O que mudou nesta atualização

**Relatório de ajuda de tarefa**

Esta atualização apresenta um novo relatório de ajuda de tarefa que lista todas as ajudas de tarefa na conta.

**Controle de versão**

Adicionamos o controle de versão para recursos ao adicionar os recursos durante a criação de um curso.

**Relatório de tentativas**

Você pode exibir um relatório de todas as repetições e revisões feitas por um aluno para cada treinamento.

**API de redefinição de módulo**

Um administrador agora pode redefinir um módulo usando a API de redefinição de módulo. Para mais informações, consulte [Referência da API do Adobe Learning Manager](https://captivateprime.adobe.com/docs/primeapi/v2/).

**Modelo de e-mail**

Para alguns modelos de e-mail, agora você pode adicionar um pré-requisito ao modelo.

**Outras alterações**

* Você pode adicionar um curso aprovado pelo gerente como pré-requisito.
* Melhoria de desempenho ao atualizar o painel de resumo do aprendizado.
* As IDs de e-mail e de conta são verificadas antes do envio de um relatório de rejeição.

### ERROS CORRIGIDOS NESTA ATUALIZAÇÃO

* Nomes de autor duplicados aparecem na página de visão geral do curso.
* Um hiperlink na página de criação da conta levou ao Erro 404.
* A localidade tcheca não refletia conforme o esperado nas configurações do reprodutor.
* Em alguns casos, as habilidades são exibidas como indefinidas para alunos em andamento e não iniciados.
* O tempo gasto em vários dias mostra o tempo diferente gasto na transcrição do aluno e nos relatórios de inscrição.
* O botão Voltar não responde para os perfis de administrador e gerente no curso > Pontuação do quiz L2 > guia Por pergunta e Presença e pontuação, respectivamente.
* Em alguns locais, em um modelo de email, parte do conteúdo no corpo do email está ausente e a tradução do idioma no modelo não é consistente.
+++

+++Atualização 83

**Data de lançamento:** 18 de janeiro de 2023

### O que mudou nesta atualização

**Nova coluna**

Uma nova coluna, **unenrollmentAllowed**, é adicionada a course.xlsx. Baixe o arquivo deste manual.

**Conector do Linkedin Learning**

Para o conector do LinkedIn Learning, há uma nova caixa de seleção apresentada que aluno pode cancelar a inscrição na página Filtros. Para mais informações, consulte [Conector de aprendizado do LinkedIn](/help/migrated/integration-admin/feature-summary/connectors.md).

### Erros Corrigidos Nesta Atualização

* Ao passar o mouse sobre os gráficos de barras, a dica de ferramenta do relatório do painel aparece conforme esperado.
* Em Relatórios na atividade do usuário, o relatório Tempo gasto no aprendizado exibe dados incorretos para dados diários/mensais.
* Em alguns casos, o gráfico de pontuação do questionário exibe valores incorretos.
* Em um curso com conteúdo SCORM com várias tentativas definidas, quando um aluno tenta o curso, o botão Rever é desativado.
* Em alguns casos, após inscrever um aluno em um curso e baixar um registro de auditoria de e-mail, o e-mail é entregue, mas não aparece no registro.
* O convite do calendário para um professor deve incluir o professor de texto no assunto.
* O ícone do cartão de treinamento não reflete na recomendação de cursos relacionados e nos cartões do plano de aprendizado presentes na página de visão geral do curso.
* Nas configurações da página inicial do aluno, adicione uma seção Salvo por mim.
* Para determinadas contas, um usuário é solicitado a fazer logon SSO para uma conta em que a ID Adobe é necessária.
* Em fusos horários com horário de verão, o campo &#39;start_time&#39; é calculado com base na diferença de hora atual, não com base na diferença de hora na data e hora de início reais. Isso causou convites com horários incorretos.
* Sempre que uma certificação se repete, uma cópia dos cursos subjacentes é criada internamente no banco de dados. Esses cursos então aparecem em busca, ao contrário do comportamento esperado.
* Quando o upload de um CSV falha, você não recebe nenhuma notificação por e-mail.
* Se os nomes dos campos ativos forem longos, eles desaparecem quando arrastados e soltos. Depois disso, o botão Salvar também não funciona conforme o esperado.
* Um relatório de sessão não é exportado por meio da página de participação e pontuação de um curso se o primeiro usuário no relatório tiver um registro na tabela de níveis de atividade com o comentário como nulo.
* Ao usar a conta de administrador para recuperar as medalhas, você pode classificar a lista conforme esperado. Mas quando você executa o mesmo para um aluno, os resultados não são classificados.
* Se você escolher um curso nos resultados da pesquisa e tentar voltar aos resultados usando o botão Voltar, os resultados da pesquisa desaparecem.
* Nem todos os usuários são adicionados a um grupo de usuários como professores em uma sessão.
* Modelos que contêm vários modelos de usuário, seu assunto é substituído por alguns valores.
+++

+++Atualização 82

**Data de lançamento:** 15 de dezembro de 2022

* A API do GET agora inclui informações de preços, se disponíveis.
* Uma nova coluna, Concluído por, é adicionada aos relatórios LT. Isso ajuda o administrador a identificar a fonte de conclusão de um LO.
* Adicionamos um novo módulo ILT que pode gravar o status de aprovação/reprovação do aluno junto com a participação. Os professores agora podem marcar um aluno como participou com aprovação ou participou com reprovação.
* Um administrador agora pode exigir que os alunos concluam e sejam aprovados antes de consumir o próximo módulo/curso. Isso se aplica a pré-requisitos, cursos solicitados e LPs.

**Correções de erros**

* Problemas do idioma Bahasa de experiência móvel imersiva na barra lateral e rodapé.
* Correções da exibição imersiva relacionadas à visualização do módulo.
* Uma pesquisa do curso em administrador e autor retorna resultados em um local diferente do local digitado.
* As alterações nos modelos de e-mail de boas-vindas não foram salvas após a edição.
* Os usuários com IDs de e-mail e Adobe IDs diferentes não conseguiam fazer logon no aplicativo móvel.
* Os usuários foram identificados incorretamente ao ingressar nas sessões de aula virtual do Zoom/BJ.
+++

+++Atualização 81 - Versão de novembro de 2022 do Adobe Learning Manager

**Data de lançamento:** 05 de novembro de 2022

**Observação:** com esta versão do Adobe Learning Manager, os usuários com contas inativas não podem mais acessar suas contas usando subdomínios. As contas podem ser acessadas usando a ID da conta ou usando a página acapindex.html e inserindo a ID de e-mail.

### Novidades desta versão

A versão de novembro de 2022 do Adobe Learning Manager consiste no seguinte:

* Configuração de SSO múltiplo
* Suporte ao recurso não conectado
* Melhorias na página de visão geral do treinamento
* Personalização do reprodutor
* Representação do aluno e do gerente

**Observação:** com a versão de novembro de 2022 do Adobe Learning Manager, o Zoom descontinuará a autenticação [JWT até junho de 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). Da mesma forma, o conector do Zoom com JWT continuará funcionando até a data mencionada, mas recomendamos que os usuários criem um aplicativo OAuth de servidor para servidor para substituir a funcionalidade na conta dele. Toda nova conexão terá a autenticação OAuth do Zoom por padrão.

### Erros corrigidos nesta atualização

* Como aluno, quando você tenta acessar um programa de aprendizado com mais de 10 cursos no dispositivo móvel, uma mensagem de erro é exibida.
* Se um curso definiu um lembrete para ser enviado n dias após o fim do prazo, o e-mail está sendo enviado após n dias, conforme esperado, mas o número de dias em que o prazo foi perdido é n-1 em vez de n.
* Um vídeo não é carregado no reprodutor se o feedback L1 estiver ativado para o curso no aplicativo do aluno e o usuário tiver apenas uma função de aluno.
* Um e-mail de lembrete de conclusão não exibe a hora no fuso horário do usuário conforme esperado.
* As transcrições do aluno geradas por relatórios do painel não obedecem os filtros e exibem mais informações do que o necessário.
* Não é possível selecionar conteúdo no qual o idioma da interface não é adicionado como idioma do conteúdo.
* Ao se registrar automaticamente em um curso pela segunda vez, o URL exibido estava incorreto.
* Quando um professor é removido de uma sessão de sala de aula virtual, ele não recebe nenhum e-mail notificando-o do cancelamento da sessão.
* O texto “minuto” em um bloco na página de treinamento do aluno não é traduzido para o indonésio bahasa como esperado.
* O painel Conformidade exibe dados incorretos para alunos que não estão em conformidade.
* Ao adicionar um relatório, não é possível selecionar cursos ou catálogos nos quais o idioma da interface não foi adicionado ao idioma do conteúdo.
* Adicionamos os seguintes idiomas de conteúdo nesta versão:
   * Búlgaro
   * Flamengo
   * Português (Brasil)

### Problemas conhecidos desta atualização

* Em alguns casos, o gráfico de pontuação do questionário não é exibido conforme esperado. Ao redimensionar o gráfico, um espaço em branco é exibido no início. Além disso, nem todas as perguntas são exibidas e os dados incorretos são exibidos intermitentemente.
+++

+++Atualização 80

**Data de lançamento:** 20 de setembro de 2022

* Os problemas de logon no aplicativo móvel no iOS foram corrigidos.
* Corrigido um problema com e-mails rejeitados.
* Os professores eram notificados incorretamente mesmo antes de os envios terem sido feitos pelos alunos.
* Um professor recebe uma notificação por e-mail mesmo que um aluno não tenha enviado uma atividade.
* Depois de criar uma sessão de aula virtual no MS Teams ou no Adobe Connect, os professores não recebem os convites de sessão.
* Status incorreto em um Caminho de Aprendizado.
* Desempenho aprimorado do aplicativo.
+++

+++Atualização 79

**Data de lançamento:** sexta-feira, 18 de agosto de 2022

* A confirmação de convite do calendário para sessões ILT/VILT agora funciona com o calendário do Google.
* Um gerenciador de loja agora pode ver notificações para usuários abaixo deles, mesmo se eles forem removidos como um gerenciador de pessoas.
* Em alguns casos, a inscrição no curso falha e exibe o Erro 500.
* Em alguns casos, não é possível modificar uma instância virtual do curso para Equipes.
* Os administradores e professores podem adicionar comentários para usuários que não participaram de sessões ILT/VILT.
* Melhorias no desempenho ao baixar relatórios de tamanho grande.
* Quando o e-mail de um usuário é rejeitado, o administrador recebe uma notificação por e-mail. O e-mail contém um link que, quando clicado, baixa um CSV com a lista de usuários cujos e-mails foram rejeitados. O administrador pode tomar as medidas necessárias.
   * O e-mail é acionado quando um e-mail retorna ou é rejeitado.
   * O e-mail é acionado uma vez por dia para todos os administradores adicionados à lista.
   * O link expira em sete dias.
* Uma mensagem de erro é exibida ao tentar integrar uma conta do Adobe Connect já integrada a outra conta do Learning Manager.
+++

+++Atualização 78

**Data de lançamento:** 4 de agosto de 2022

### Erros corrigidos nesta atualização

* Se você tiver um curso que contém um módulo com uma visualização e usar uma API para recuperar os recursos do curso, a resposta não conterá nenhum dado de location, contentZipUrl e contentStructureInfoUrl.
* Resposta incorreta após enviar uma solicitação XAPI do documento Swagger, onde o nome do domínio é learningmanager.
* Na resposta da API /boards/{id}/posts, a propriedade “post.attributes.myPoll” aparece como um objeto vazio.
* Em alguns casos, para um usuário não conectado, o botão Adicionar ao carrinho é desativado para alguns cursos ou planos de aprendizado.
* URL de subdomínio incorreto na página de identidade visual.
+++

+++Atualização 77

**Data de lançamento:** 24 de maio de 2022

**Problemas corrigidos nesta atualização:**

* Os novos cursos não respeitam a sequência no aplicativo Salesforce. Se você alterar a sequência, o curso não será exibido na sequência desejada.
* Depois de modificar as configurações na página inicial clássica e salvá-las, as alterações não são salvas conforme esperado. Isso acontece intermitentemente.
* O código HTML é exibido quando os alunos verificam suas notificações, o que afeta negativamente a experiência.
* No painel, o tempo gasto no aprendizado é exibido incorretamente como zero horas.

## ATUALIZAÇÃO: O Adobe Learning Manager será renomeado para Adobe Learning Manager

Este é uma atualização sobre uma alteração futura que ajudará você a se preparar para isso.

O **Adobe Learning Manager como um produto será renomeado para Adobe Learning Manager em julho de 2022**. Isso é um esforço estratégico feito para refletir com mais precisão o alinhamento do produto com determinadas prioridades de negócios.

A equipe de produto está tomando todas as medidas para garantir que não haja impacto no uso da plataforma. Você pode continuar a utilizar o produto como habitualmente. Os administradores da plataforma podem notar o novo nome da marca em determinadas telas em julho.

Como parte dessa alteração, os URLs de acesso do Learning Manager são afetados.

Por exemplo, se a URL de acesso da sua conta for `https://learningmanager.adobe.com/XYZ`, a nova URL será `https://learningmanager.adobe.com/XYZ`.

Todos os URLs existentes continuarão funcionando.

Para concluir esta ação, contate o departamento de TI da sua organização. Para obter mais informações, entre em contato conosco em `learningmanagersupport@adobe.com`.
+++

+++Atualização 76

**Data de lançamento:** quinta-feira, 20 de abril de 2022

* Correções nas terminologias do produto em alguns relatórios do painel.
* Uma barra dupla (&quot;//&quot;) no URL de um ponto de extremidade resultou em erros de validação.
* Após atualizar uma página, a porcentagem de conclusão e os últimos campos visitados exibiram informações incorretas.
* Fizemos algumas alterações em como o valor Certificado ou um plano de aprendizado é calculado.
* Um administrador personalizado podia adicionar todos os usuários como professores, mesmo que tivesse permissão para adicionar apenas um usuário.
* Em um PDF de medalha, uma data de conclusão incorreta era exibida.
+++

+++Atualização 75

**Data de lançamento:** quarta-feira, 29 de março de 2022

* Em algumas contas, após copiar o csv bruto no local do FTP, a importação do usuário não ocorre conforme o esperado e há várias notificações de erros.
* Em versões anteriores do Learning Manager, para configurar um conector do Zoom, era necessário configurar primeiro o FTP do Exavault para copiar o arquivo csv. Nesta versão, o conector FTP não será mais usado para o arquivo csv e, portanto, você não precisa configurar primeiro o FTP.
+++

+++Atualização 74: Instância do Learning Manager AWS India

**Data de lançamento:** quarta-feira, 15 de fevereiro de 2022

### Visão geral

Uma [instância](https://learningmanagerapac.adobe.com/acapindex.html) do Learning Manager agora será hospedada no AWS em Mumbai (ap-south-1). Para clientes que usam essa instância da Índia, as informações de identificação pessoal (PII) e os registros de aprendizado do usuário serão armazenados somente na região da Índia.

### O que é suportado

A instância da Adobe Learning Manager India está ao mesmo nível de outras instâncias, como regiões da UE e dos EUA, em termos de recursos. Existem alguns recursos que não são suportados na instância da Índia. São eles:

* Pagamento com cartão de crédito para compra de vagas
* catálogo de conteúdo do Creative Cloud
* Aplicativo Slack
* **&#42;** Aguardando certificação para conformidade com SOC2

### Perguntas frequentes

**Qual é a diferença entre esta instância em Mumbai e outros ambientes exclusivos para AWS?**

Não há diferença. A instância em Mumbai é igual as instãncias [AWS EUA](http://learningmanager.adobe.com/) ou [AWS UE](http://learningmanagereu.adobe.com/). Essa instância é hospedada na Índia e todos os registros de aprendizado e dados do usuário permanecem nesse país. Os seguintes recursos não são suportados na instância da Índia:

* Pagamento com cartão de crédito para compra de vagas
* catálogo de conteúdo do Creative Cloud
* Aplicativo Slack
* **&#42;** Aguardando certificação para conformidade com SOC2

**Este ambiente estará em conformidade com o CCF (Common Controls Framework)?**

Sim A nova instância está em conformidade com o CCF (Common Controls Framework).
+++

+++Atualização 73

Data de lançamento: 05 de fevereiro de 2022

* O suporte a modelos de e-mail já está disponível para idiomas de conteúdo, incluindo húngaro e finlandês.
+++

+++Atualização 72 - Versão de janeiro de 2022 do Learning Manager

Data de lançamento: 28 de janeiro de 2019

### Novidades e alterações

* Adicionar locais de sala de aula
* Alterações de gamificação
* Conector do Microsoft Teams
* Alterações de API
* Alterações na Web imersivas para dispositivos móveis

<!--
For more information, see What's new in the [**January 2022 release of Adobe Learning Manager**](../whats-new.md).
-->

### Erros corrigidos nesta versão

**Biblioteca de conteúdo**

* A pesquisa de arquivos de conteúdo em pastas de conteúdo privadas não estava funcionando para usuários com privilégios de função personalizados. Esse problema já foi corrigido.

**Cursos**

* A exclusão de um curso ou de uma programação de aprendizado não era possível se eles tivessem uma associação histórica com um plano de aprendizado. Esse problema já foi corrigido. Agora, os usuários podem excluir um curso ou uma programação de aprendizado se não estiverem associados a um plano de aprendizado.
* Ao visualizar um curso ou caminho de aprendizado, se o arquivo de recurso tiver um nome longo sem espaços, o nome do arquivo não será quebrado conforme esperado e transbordará para a próxima linha. Esse problema foi corrigido.
* No caso da sala de aula virtual, anteriormente você podia criar um módulo sem selecionar qualquer sistema de conferência de sala de aula virtual por meio de uma nova instância; o URL da sala de aula virtual não tinha as informações necessárias. Isso agora é evitado por uma mensagem de erro no estágio de criação do módulo solicitando que você especifique o sistema de conferência de sala de aula virtual antes de salvar o módulo.
* A página da lista de espera estava exibindo uma mensagem de banner incorreta nos usuários registrados, que foi removida agora.
* No caso do cancelamento de inscrição em massa dos cursos, o pop-up para inserir IDs de e-mail não era exibido, o que foi corrigido.
* A opção de enviar e-mail aos alunos na guia Participação e pontuação no aplicativo do administrador e professor não excluía os alunos desmarcados após a execução de todas as operações selecionadas. Portanto, o Learning Manager estava enviando um e-mail a todos os alunos. Agora esse problema foi corrigido.
* O relatório de inscrição é exibido como “Não iniciado”, mesmo que um aluno já tenha concluído o curso.

**SSO**

* Na configuração de SSO, se a ID da entidade tivesse espaços de treinamento ou de entrelinha, a configuração de logon não funcionava. Isso agora está sendo tratado como parte da correção.

**Comunicados**

* Como administrador, as datas de início e término de um comunicado não eram salvas se a interface e o idioma do conteúdo fossem definidos como Deutsch/Espanol. Agora esse problema foi corrigido.

**Modelo de e-mail**

* Convites de sessão que se estendem por vários dias, nos quais os convites não refletem as informações corretas sobre os dias que são bloqueados em alguns clientes de email. Esse problema já foi corrigido.
* A variável “Nome do local” estava ausente no modelo de e-mail “Lembrete da próxima sessão” para alunos na localidade alemã. Isso já foi adicionado.
* O link para criar a conta como parte do e-mail de boas-vindas para o usuário não estava considerando a localidade do usuário, o que foi corrigido.

**Lembretes de email**

* Se os alunos foram inscritos no treinamento por meio de um plano de aprendizado, os e-mails de lembrete de conclusão eram enviados várias vezes com base no número de edições feitas nas datas de conclusão do mesmo plano de aprendizado. Agora esse problema foi corrigido.

**Usuário**

* A mensagem mostrada ao usuário quando sua conta está inativa/suspensa foi aprimorada, indicando que ele deve entrar em contato com o administrador para que suas contas sejam habilitadas novamente.

**Atividade**

* Um professor não podia ver os envios do aluno se o nome do arquivo de envio tivesse um caractere especial. Esse problema já foi corrigido.

**Denunciar**

* Um administrador não conseguia baixar o relatório de inscrição do curso se ele contivesse um aluno que estava inscrito indiretamente neste curso por meio de uma programação de aprendizado flexível, mas ainda não tinha escolhido uma instância para este curso no caminho de aprendizado. Agora esse problema foi corrigido.
* Reorganizar relatórios no painel de relatórios para funções de administrador e gerente não estava preservando o estado da ordem de relatórios. Agora esse problema foi corrigido.

**Conteúdo**

* O conteúdo de áudio no treinamento não era reproduzido automaticamente na visualização como modo de aluno devido às políticas de reprodução automática do navegador. Agora isso foi corrigido para navegadores compatíveis, exceto o Safari.

**Gamificação**

* Se um aluno externo foi convertido como aluno interno na mesma conta, ele não conseguia acessar o quadro de classificação de gamificação no aplicativo do aluno. Agora esse problema foi corrigido.

**Player**

* O reprodutor não mostrava uma mensagem de aviso quando o usuário tentava pular módulos em um curso ordenado com o tipo AICC de módulos. Esse problema já foi corrigido.
* Para certos cursos adquiridos com módulos de vídeo em caso de LMS sem periféricos, a reprodução não funcionava para certos usuários. Esse problema já foi corrigido.

**Painel do gerente**

* Um gerente não podia exportar o relatório para sua equipe direta da página de habilidades da equipe do Painel do Gerente. Agora esse problema foi corrigido.

**Publish**

* Na instância europeia do conteúdo do Learning Manager que foi publicado diretamente no Adobe Learning Manager pelo Adobe Captivate, o conteúdo estava sendo publicado no local Deutsch por padrão. Esse problema já foi corrigido.

**API**

* O campo de duração foi adicionado ao modelo de ajuda de tarefa.
* Para as APIs de recomendação, às vezes uma solicitação GET retorna o Erro 500.
* Ao migrar treinamentos por meio do Exavault e se o texto contivesse caracteres que não fossem do inglês, ele costumava ser atualizado com caracteres residuais no texto. Agora esse problema foi corrigido.

**Localização**

* `NormalTextRun  BCX0 SCXW38820519 For the`Aplicativos de administrador, autor e aluno, parte do conteúdo em alemão não aparece conforme esperado.

## Problemas conhecidos nesta versão

* Na página Aprendizado social, ao criar uma publicação, não é possível gravar um áudio ou carregar o áudio depois de tocar no botão do microfone. Essa é uma limitação do navegador.
* No iOS, os arquivos de áudio H264 e WMA não são compatíveis com o navegador para dispositivos móveis.
* Os alunos que têm um + em seu endereço de e-mail não têm o progresso marcado. Isso é depois que eles fazem um curso de sala de aula virtual em Microsoft Teams.
* No navegador Safari para dispositivo móvel, os alunos não poderão carregar mais de 200 mb de arquivo no Aprendizado social. Esta é uma limitação do navegador.
+++

+++Atualização 71

Data de lançamento: 17 de novembro de 2021

### Compartilhar treinamento com gerentes

O Learning Manager oferece um painel de conformidade para todos os administradores e gerentes. Os gerentes acham muito útil controlar a conformidade dos membros da equipe para um treinamento específico. Ao mesmo tempo, os administradores gostariam que todos os gerentes adicionassem treinamentos de conformidade ao painel e os monitorassem.

No Learning Manager, o fluxo de trabalho **Compartilhar com Gerentes** permite que os administradores compartilhem treinamentos com gerentes, para que eles possam ser adicionados ao Painel de Conformidade de um gerente. Assim, os gerentes não precisam realizar nenhuma ação e podem começar a monitorar a conformidade imediatamente.

Para obter mais informações, consulte [**Compartilhar treinamento com gerentes**](../administrators/feature-summary/reports.md#share_training_managers).

### Erros corrigidos nesta atualização

* Se houver duas contas e o recurso Caminho de aprendizado aprimorado estiver desativado e houver um catálogo compartilhado da primeira conta para a outra, então o Caminho de aprendizado na segunda conta terá seções duplicadas na página do curso.
* Um FTP personalizado agora suporta sftp:// além de http:// e https://
* O conector Exavault agora usa APIs V2.
* Em alguns casos, a qualidade dos vídeos era inferior ao ideal. O problema já foi corrigido.
* Mesmo após um aluno ter concluído um curso obrigatório e aprovado pelo gerente, a certificação permanece no estado Aprovação pendente.
* Se os nomes dos autores contiverem caracteres acentuados, a migração do curso falhará.
* Se o Campo ativo tiver valores em maiúsculas, ele não será salvo como esperado.
* Não é possível filtrar Caminhos de aprendizado com base em habilidades.
* Quando um administrador cria uma instância e adiciona uma nova sessão, um professor não recebe o e-mail de convite da sessão. Esse problema ocorre nos cursos por videoconferência no Zoom.
+++

+++Atualização 70

Data de lançamento: 28 de outubro de 2021

### Erros corrigidos nesta atualização

* Em alguns casos, as informações sobre um caminho de aprendizado não são refletidas em uma transcrição do aluno.
* O texto dentro da caixa de diálogo **Marcar conclusão** é atualizado para refletir que a operação é irreversível.
* A API dos objetos de aprendizado, em alguns casos, retornou um erro de metadados.
+++

+++Atualização 69 - Versão de outubro de 2021 do Learning Manager

**Data de lançamento:** 09 de outubro de 2021

### Caminho do aprendizado

A versão de **outubro de 2021 do Adobe Learning Manager** apresenta o conceito de Caminhos de Aprendizado.

>[!NOTE]
>
>A página **Configurações > Geral** tem uma nova opção para habilitar os recursos estendidos de Caminhos de Aprendizado. Se essa opção estiver ativada, você pode adicionar caminhos de aprendizado em outro caminho de aprendizado. Não é possível alterar a opção depois de ativada.

Os Caminhos de aprendizado substituem o nosso recurso existente de programas de aprendizado. Imagine os programas de aprendizado obtendo aprimoramentos poderosos sem descartar os recursos existentes. Além disso, o recurso é marcado como um caminho de aprendizado.

Para mais informações, consulte [***Caminhos de aprendizado***](../administrators/feature-summary/learning-paths.md).

### Outras alterações

* Novo aplicativo do Salesforce
* Hub de Conteúdo
* Alterações de relatórios
* Relatório de resumo da sessão
* Alterações no sumário do reprodutor
* Alterações de API
* Alterações relacionadas ao conector

Para mais informações, consulte [***Novidades do lançamento do Learning Manager em outubro de 2021***](../whats-new.md).

### Erros corrigidos nesta atualização

* Os modelos de e-mail, como Cancelamento de inscrição no curso, Cancelamento de inscrição no programa de aprendizado ou Cancelamento de inscrição de certificação, não refletem as terminologias de produtos mais recentes, conforme definidas no csv. Agora, o texto padrão nos modelos de e-mail oferecerá suporte a terminologias personalizadas.
* O idioma do usuário no Learning Manager não é suportado no fluxo de trabalho Publicar no Learning Manager. Se o idioma do usuário for diferente, o Publish para Learning Manager acontece em inglês.
* Se você adicionar muitos catálogos a uma função personalizada, ocorrerá um erro quando você atualizar a função. O limite de número de catálogos foi aumentado em até 50 catálogos.
* Em alguns casos, os treinamentos excluídos ainda são visíveis em um catálogo. Esse problema ocorreu somente no aplicativo de administração e está corrigido.
* Quando a função de gerente era alterada de um usuário para outro, a função de gerente do usuário anterior ainda refletia na interface do usuário. Esse problema já foi corrigido. Esse problema estava presente apenas para usuários externos, não para usuários internos.
* Em alguns cenários específicos para um grande conjunto de usuários que eram importados via csv do usuário, a importação falhava. Esse problema já foi corrigido.
* Uma transcrição de aprendizado não exibe a data de conclusão de um certificado externo se um curso obrigatório for adicionado após a criação do certificado externo e um usuário estiver inscrito nele. Esse problema já foi corrigido.
* Um certificado não exibia o nome localizado do aluno conforme esperado. Esse problema já foi corrigido.
* No caso de sessões de vídeo conferência do Zoom, um professor nem sempre recebia o convite para a sessão. Esse problema já foi corrigido. O professor agora recebe a comunicação necessária.
* Um aluno não recebia convites para uma sessão se os modelos de nível de curso estivessem ativados, mas os modelos de nível de conta estavam desativados. Esse problema já foi corrigido.
* Para fusos horários específicos, lembretes por e-mail eram entregues um dia depois do esperado. Esse problema já foi corrigido.
* Os alunos não recebiam e-mails de notificação de sessão se determinados modelos de e-mail estivessem desativados.
* Caso uma reunião do BlueJeans fosse atualizada por autores ou administradores, o URL da reunião do BJ ficava inutilizável. Esse problema já foi corrigido.
* Ao executar a API GET /LO, em alguns casos, os cursos que faziam parte de um programa de aprendizado não eram retornados.
* Se o aluno tentasse carregar o conteúdo cujo nome tivesse espaço em branco, ele encontraria um erro interno no servidor.
* Os PDF de emblema gerados para os alunos tinham problemas de formatação quando eram gerados em locais diferentes do inglês. Esses problemas já foram corrigidos.
+++

+++Atualização 68

Data de lançamento: 28 de setembro de 2021

### Erros corrigidos nesta atualização

* No navegador móvel, links profundos foram ativados para o seguinte:

   * Todos os painéis
   * Painel público e publicação
   * Painel particular e publicação com acesso
   * Painel particular e publicação sem acesso
   * Painel restrito e publicação
   * Comentário na publicação
   * Resposta ao comentário
   * Perfil de usuário social

* Para contas que usam domínio personalizado, o aplicativo do aluno não exibe o favicon.
* No AEM, o componente do Learning Manager exclui a configuração de outros componentes.
* A página de ajuda para o componemte do AEM é redirecionada para um local incorreto.
* Obtenção e armazenamento externo de e-mails/tokens do usuário para que os usuários possam implementar seu próprio back-end de armazenamento em vez de usar nós de usuário AEM.
* Ao editar a descrição de texto sem formatação em Cursos, Programas de aprendizado, Certificados e Ajudas de tarefa, uma mensagem de aviso é exibida.
* Os relatórios do painel Gerente não são baixados quando um usuário tem funções personalizadas e de gerente.
* Uma compilação por e-mail exibe um valor incorreto da atividade de treinamento.
* Em alguns casos, o Learning Manager se comporta inesperadamente quando você se move do Marketplace de Conteúdo para a página do Aluno.
* No aplicativo Social, os filtros não funcionam conforme esperado na exibição de lista.
* O e-mail de boas-vindas que os usuários internos recebem também é recebido por usuários externos.
* Adicione o widget do Learning Manager no modelo de página no AEM.
* Se quiser publicar novamente um certificado após remover um curso, não será possível fazer isso.
* Os alunos não recebem e-mails que contêm detalhes de uma sessão.
+++

+++Atualização 67 - Atualizações para o Azure

Esta atualização apresenta uma nova instância do Azure.

>[!NOTE]
>
>Os seguintes itens não são suportados na instância:
>
>* [Domínio personalizado](../custom-domain.md)
>* [Compra com cartão de crédito](../administrators/feature-summary/billing-management.md)
>* [Catálogo de conteúdo](../administrators/feature-summary/content-catalogs.md)

+++

+++Atualização 66 - Versão de agosto de 2021 do Learning Manager

A **versão de** agosto de 2021 **do Adobe Learning Manager** visa melhorar os fluxos de trabalho da Experiência do Aluno, Relatórios e Administrações. Alguns dos destaques incluem:

* **Marketplace de conteúdo:** o Learning Manager agora oferece mais de 70.000 cursos de campos variados, como Tecnologia, Gerenciamento, Liderança e assim por diante.
* **Suporte de acessibilidade aprimorado:** o suporte de acessibilidade para a função do aluno fortalece por meio da navegação do teclado aprimorada, capacidade do leitor de tela e conformidade com a taxa de contraste.
* **Formatação de Rich Text:** o Learning Manager agora oferece edição de rich text para descrições em cursos, programas, certificados e ajudas de tarefa. Isso permite que os autores especifiquem descrições em rich text, incluindo hiperlinks, imagens e outras opções de formatação de texto, em vez de texto sem formatação.
* **Classificação por estrelas:** agora um aluno pode classificar um curso em uma escala de 5 pontos. Um administrador pode selecionar entre a classificação da eficácia existente ou a classificação de 5 estrelas.
* **Integração do Badgr:** os alunos agora podem autorizar o Learning Manager a enviar automaticamente as medalhas que ganharam no Learning Manager para a conta do Badgr, de onde podem compartilhar as medalhas em suas redes sociais.
* **Exportar eventos de aprendizado para o Salesforce:** o Learning Manager agora oferece a capacidade de exportar alguns eventos específicos no Learning Manager, como adição de novos usuários, inscrição e conclusão para um inquilino do Salesforce e fornece a capacidade de vinculá-los ao objeto de usuário ou ao objeto de contato apropriado no Salesforce.

Para obter mais informações, consulte [***Novidades do lançamento do Learning Manager em agosto de 2021***](../whats-new.md).


**Data de lançamento:** 7 de agosto de 2021

### Erros corrigidos nesta atualização

**Experiência do aluno**

* Depois que um aluno é adicionado a dois grupos de usuários e um plano de aprendizado é adicionado, o aluno é inscrito em uma instância diferente do mesmo curso.
* Em alguns casos, após a inscrição e o início do curso, o curso não é reproduzido conforme esperado.
* A descrição do curso exibe tags HTML, que agora foi corrigida.
* Se você comentar em uma publicaçao em um painel social que abrange várias linhas, o comentário será exibido em uma única linha. Esse problema já foi corrigido.

**Criação**

* Em alguns casos com inscrições automáticas, os alunos recebem vários e-mails de inscrição.

**Relatórios**

* Quando a interface é definida para alguns locais que não são em inglês, as transcrições do aluno não são geradas conforme o esperado.
* Capacidade de redefinir o progresso de um curso dentro de um programa de aprendizado e certificação.
* Se um CSV contiver campos ativos com o mesmo nome, mas com distinção de maiúsculas e minúsculas diferente, o CSV produzirá uma exceção.

**Outros**

* A opção para editar pontuações e comentários deve ser desativada quando nenhum aluno estiver selecionado ou se a presença do aluno selecionado não estiver marcada.
* Os valores nos campos ativos são exibidos em minúsculas na caixa de diálogo Editar usuário, mesmo que um usuário tenha adicionado os valores anteriormente em maiúsculas.
* Capacidade de administradores e gerentes visualizarem aprovações pendentes para cursos. Isso permite que o gerenciamento garanta que os gerentes controlem o aprendizado e o treinamento dos funcionários, além de permitir que os administradores do Learning Manager aprovem a inscrição no curso conforme necessário.
* Um usuário que tenha uma permissão personalizada de autor ou administrador/autor não pode editar uma ajuda de tarefa criada por outro usuário.
* Na função Administrador, quando o usuário navega até Curso > Instância e seleciona “Alunos inscritos” para qualquer instância, antes era usado para mostrar os alunos de “Instância padrão”. O administrador precisava alterar a instância no menu suspenso manualmente. Agora o Learning Manager direciona corretamente o usuário para a página dos alunos com a instância correta selecionada.

**Aplicativo de dispositivo**

* Em dispositivos Android e iPhone, um aluno não pode iniciar módulos do curso aleatoriamente. Isso produz o Erro 401 não autorizado.
* Um aluno pode digitalizar dois códigos QR, mas ao digitalizar o terceiro código QR, uma mensagem de erro é exibida.
* Em alguns dispositivos Android e iOS, um arquivo não é aberto como esperado para alguns cursos baixados.
* Tentar abrir uma ajuda de tarefa exibe uma mensagem de erro.
* O aplicativo do dispositivo se comporta inesperadamente quando um programa de aprendizado é usado offline.
* Quando um aluno volta online e abre o aplicativo, ele fica preso na tela inicial.
* Às vezes, quando um usuário está novamente online, o aplicativo muda para a exibição clássica.
* Às vezes, quando um curso é usado offline, o progresso não é salvo.
* Às vezes, o nome de um curso não é exibido como esperado desde o início quando o nome é longo.
* Na página do catálogo, os cursos não são classificados como esperado.
+++

+++Atualização 65

Data de lançamento: julho de 2021.

### Erros corrigidos nesta atualização

* Problemas com logons de usuários.
* O modelo de e-mail de inscrição do curso para gerente não exibe o prazo de conclusão do curso se a variável for adicionada ao modelo.
* TLS 1.0 e TLS 1.1 foram descontinuados.
* Problemas com exclusão de dados do RGPD para um usuário.
+++

+++Atualização 64

Data de lançamento: julho de 2021.

### Erros corrigidos nesta atualização

* A notificação de inscrição é enviada aos alunos que já estão inscritos em um curso.
* Quando um certificado personalizado como uma medalha é gerado, o formato de data não é suportado no idioma alemão.
+++

+++Atualização 63

Data de lançamento: junho de 2021

### Erros corrigidos nesta atualização

* Você pode criar um usuário com um nome em branco em um csv.
* Se houver um caractere &#39;/&#39; no campo ativo, depois de criar um trabalho para baixar user.csv, o estado do trabalho não é alterado de &quot;Enviado&quot; para &quot;Concluído&quot;.
* Os módulos ordenados não obedecem à sequência.
* Quando um autor externo é excluído, o curso que o autor criou não estará mais disponível.
* Pesquisar um objeto de aprendizado com mais de uma habilidade produz resultados inesperados.
+++

+++Atualização 62

Data de lançamento: junho de 2021

### Erros corrigidos nesta atualização

* Não é possível fazer logon no aplicativo quando a conta é iniciada pelo logon SP.
* Os vídeos não são renderizados da Brightcove conforme esperado.
* A API userGroupInfo não fica visível ao visitar o programa de aprendizado em nenhum dos aplicativos.
* Não é possível pesquisar um programa de aprendizado e uma certificação inativos ao criar um relatório do Painel.
* Um autor não pode editar ou atualizar uma ajuda de tarefa criada por outro autor.
* A API para envio de arquivos não funciona como esperado no cluster da UE.
+++

+++Atualização 61

Data de lançamento: maio de 2021

### Erros corrigidos nesta atualização

* Melhoria de desempenho em chamadas userGroupInfo.
* Depois de ativar os novos perfis da Brightcove, o Learning Manager suporta conteúdo com módulos de vídeo e áudio.
* As transcrições de aprendizado não capturam os dados se um intervalo de datas estreito for selecionado.
* Um convite de sessão é enviado aos alunos inscritos para todas as sessões, mesmo quando apenas uma nova sessão é adicionada.
* Os módulos de áudio não estão sendo carregados como esperado.
+++

+++Atualização 60

Data de lançamento: abril de 2021

### Erros corrigidos nesta atualização

**Denunciar**

* Depois de criar um relatório, se você procurar um curso inativo, não será possível fazer isso.
* Erros em um relatório se espalham para outros. Como resultado, esses relatórios levam a erros.

**Ajudas de tarefa**

* Após baixar uma ajuda de tarefa, você não poderá excluí-la.

**Player**

* As legendas WebVTT não são exibidas conforme esperado.

**Aplicativo do aluno**

* Na página Visão geral da certificação, a certificação externa não exibe a duração adicionada por um autor.
* Adicione a opção **Todos** no filtro Habilidade.
* Os alunos recebiam vários e-mails de resumo.
* O número de linhas selecionadas não corresponde ao esperado em uma página.

**Componente AEM**

* Os widgets não são atualizados como esperado após uma atualização de página.

**Localização**

* Algumas cadeias de caracteres em alemão não estão traduzidas como esperado.
* A tradução de cadeia de caracteres é padrão para inglês se um aluno não selecionou a interface e o idioma do conteúdo.

**Certificação**

* A ordem do módulo pode ser ignorada se os pré-requisitos não forem aplicados.

**Navegador**

* Os aplicativos de autor, gerente ou aluno não são exibidos conforme esperado no IE 11.

**Gamificação**

* Os pontos de gamificação não são resgatados como esperado.

**Biblioteca de conteúdo**

* Os cursos do aplicativo de avaliação de conteúdo não funcionam como esperado.

**Player**

* O player carrega apenas no espaço onde o widget está presente.
* Os vídeos dentro de um módulo do Captivate não são reproduzidos conforme esperado.

**Conector**

* Em alguns casos, os arquivos são excluídos de um conector FTP/Box.
* Os arquivos são excluídos do FTP se forem atualizados com os mesmos nomes.
* Um evento BlueJeans suporta paginação onde o número de eventos é maior que 100.

**Atualização do aplicativo móvel 3.3 - março de 2021**

Data de lançamento: 26 de março de 2021

### Novidades e alterações {#whatsnewandchanged}

A atualização do aplicativo móvel do Captivate Learning Manager 3.3 apresenta uma nova página inicial, que suporta manchetes e recomendações de treinamento baseadas em IA. Esta página inicial está disponível para todas as contas configuradas para a nova opção Layout imersivo. As contas configuradas com o Layout clássico continuam a ver a página inicial clássica/herdada. Elas não devem observar nenhuma alteração na página inicial.

Além disso, essa atualização também permite que os alunos baixem a medalha como PDF e uma imagem. A atualização também apresenta um pop-up de feedback, que permite aos alunos fornecer feedback anonimamente sobre o aplicativo.

Para mais informações, consulte [Aplicativo do dispositivo Learning Manager](../learners/feature-summary/ipad-android-tablet-users.md).

Leia para saber mais.

#### Nova página inicial

Para todas as contas com a opção Layout imersivo ativada, há uma nova página inicial para suportar a configuração de Layout imersivo.

#### Classificação de feedback

Nesta versão, o Learning Manager solicita que o usuário forneça feedback sobre a sua experiência com o aplicativo móvel.

#### Baixar medalha

Essa atualização permite que os alunos baixem medalhas no formato PDF e de imagem.

<!--## Previous update releases {#previousupdatereleases}-->
+++

+++Atualização 60 - Versão de fevereiro de 2021 do Learning Manager

Data de lançamento: 20 de fevereiro de 2021

### Novidades e alterações {#Whatsnewandchanged-1}

* Exibição do quadro no social.
* Personalizar o banner social.
* Filtros de catálogo no aplicativo do aluno.
* Cancelar inscrição no treinamento.
* Importar usuários dos contatos do Salesforce.
* ...e muito mais.

Para mais informações, consulte Novidades da [atualização do Learning Manager de fevereiro de 2021](../whats-new.md).

### Erros corrigidos nesta atualização {#bug-fixes}

**Certificação**

* Em alguns casos, o aluno não conseguiu tentar novamente um curso, que faz parte de uma certificação, embora o máximo de tentativas para o curso esteja definido como infinito. Esse problema já foi corrigido.
* Em alguns casos, o aluno não pode se inscrever em uma certificação, pois o botão **Inscrever-se** não está visível como esperado.

**Biblioteca de conteúdo**

* URL de ajuda incorreto na página **Adicionar novo conteúdo**. O URL correto foi atualizado.

**Curso**

* Um relatório de pontuação do quiz L2 baixado para um módulo de conteúdo AICC mostra a pontuação incorreta na coluna Pontuação total do usuário/Pontuação do quiz. Esse problema foi corrigido.
* Baixar recursos de um curso não funcionava se ele fosse duplicado de outro curso e se o aluno não tivesse acesso ao curso original, o que costumava criar um curso duplicado.
* Imagens de banner que não são excluídas quando o autor as remove, estando o curso no estado de rascunho. Esse problema foi corrigido.

**AEM**

* Após inserir o componente do Learning Manager no AEM, a página demorava a carregar, impedindo o acesso aos outros componentes. Esse problema foi corrigido.

**Admin**

* Os cursos retirados não aparecem nos resultados da pesquisa conforme esperado. Esse problema foi corrigido.
* O administrador não conseguiu pesquisar cursos retirados no **Aplicativo do administrador** -> **Relatórios personalizados** -> **Relatórios do Excel** -> **Relatórios do curso**, que agora foi corrigido.

* Baixar um relatório do quiz como Excel não funcionará se o arquivo contiver alunos que realizaram os treinamentos antes e depois da atualização do conteúdo. Esse problema foi corrigido.
* Um upload de CSV falhará se os campos ativos contiverem caracteres especiais. Esse problema foi corrigido.
* Em alguns casos, quando um aluno fazia um quiz, criado no Captivate, as respostas não eram capturadas da maneira esperada.
* Depois de criar uma assinatura e tentar editar a assinatura, os botões **Salvar** e **Cancelar** não aparecem conforme esperado. Esse problema foi corrigido.

**Player**

* Para um tipo específico de conteúdo do cenário de retomada SCORM-2004 que não estava funcionando. Assim, os alunos tinham que navegar até o ponto em que pararam. Esse problema já foi corrigido. O conteúdo agora deve ser retomado a partir do ponto que foi usado antes.
* Depois de se inscrever em um curso, em alguns casos, o conteúdo não era reproduzido conforme esperado. Esse problema foi corrigido.

**Cancelamento da inscrição**

* Um relatório de inscrição listava apenas 20 alunos não inscritos, mesmo quando havia mais alunos não inscritos no curso/certificação. Esse problema foi corrigido.
* Ocorria um problema ao exportar a lista de alunos não inscritos no relatório de inscrição em alguns casos. Agora esse problema foi corrigido.

**Programa de aprendizado**

* Para um plano de aprendizado flexível, se um aluno estivesse inscrito em apenas uma instância do curso, ao clicar no link do curso dos outros cursos, cujas instâncias não foram selecionadas, uma página em branco era aberta.

**Aluno**

* Alguns alunos, cujos nomes de usuário têm caracteres especiais, não recebiam notificações por e-mail conforme esperado.
* Na exibição imersiva, em alguns casos, o widget Calendário não exibia as próximas sessões de aula virtual conforme esperado.
* No aplicativo do aluno, o filtro **Habilidade** não funcionava conforme esperado. Esse problema foi corrigido.

**Pesquisa**

* Em um cenário específico, o Gerente não conseguia procurar um grupo de usuários de um gerente anteriormente. Esse problema foi corrigido para a função Gerente.

**Grupo de usuários**

* Ao exportar o relatório de grupo de usuários com mais de 500 usuários, os valores de dados e os cabeçalhos de coluna no relatório não correspondiam, o que foi corrigido.
* Quando o administrador editava a assinatura por e-mail em modelos de e-mail e adicionava várias linhas, ele via tags html somente na interface do administrador. Esse problema já foi corrigido.
* No **Aplicativo do Administrador > Catálogo > procurar catálogo**, não é possível pesquisar.

**Usuários**

* Alguns usuários externos ativos estavam sendo excluídos. Fizemos algumas alterações e o problema foi corrigido.

**Importar**

* A importação de um csv falhava se o cabeçalho csv contivesse espaços em branco à direita ou se o e-mail de um usuário contivesse acentos ou caracteres diacríticos.

**Envio de atividade**

* No aplicativo do instrutor - página de envios de atividade, o valor de data enviado costumava se sobrepor ao nome do arquivo, se fosse longo. Esse problema de interface do usuário agora está resolvido.

**O professor**

* Um professor recebe convites de sessão para todas as suas sessões, mesmo que apenas uma nova sessão seja adicionada. Esse problema foi corrigido.

**SCORM**

* Para determinados conteúdos do SCORM, havia alguns problemas relacionados ao navegador, problemas de navegação do reprodutor e inconsistências na gravação da pontuação do quiz. Esses problemas foram corrigidos.

**SAML e SSO**

* Atualizamos a mensagem de erro exibida quando as credenciais do SSO expiravam.

**API do Learning Manager**

* A API getlearningObject retornou dados de inscrição incorretos devido a problemas no armazenamento em cache. Esse problema foi corrigido.
* Uma sessão de aula virtual agora exibe o URL da reunião no campo Local em um convite de reunião.
* Se você configurou várias integrações de provedor de aula virtual e se alguma delas não funcionava como esperado, o menu suspenso de seleção de aula virtual costumava mostrar uma lista vazia. Esse problema já foi corrigido. A integração de aula virtual restante é listada corretamente agora.
* Os modelos de aula virtual do Connect não eram carregados como esperado quando um instrutor entrava na sessão.
* Uma duração incorreta era mostrada na interface do usuário após a migração de módulos com duração no arquivo csv module_version.
* Para algumas contas, a atualização de um usuário não funcionava como esperado. Esse problema foi corrigido.

### Problemas conhecidos desta atualização {#known-issues}

* Ao usar o filtro **Duração** no aplicativo do aluno, o conteúdo e o filtro podem não estar sincronizados se o aluno usar algum outro conteúdo local e não fizer parte da instância padrão em termos de inscrição.

>[!NOTE]
>
>Os filtros &#39;**Duração**&#39; e &#39;**Formato**&#39; de treinamento são identificados com base no conteúdo de treinamento disponível para a instância padrão e para a localidade preferida da conta.

+++

+++Atualização 59

## Atualização 59

Data de lançamento: 18 de dezembro de 2020

### Conector do BlueJeans Events {#bluejeanseventconnector}

O conector do BlueJeans Events conecta os sistemas do Learning Manager e do BlueJeans para automatizar a sincronização de dados. Com esse conector, você pode:

* **Configurar sessões virtuais usando o BlueJeans Events:** configure um novo evento no BlueJeans e configure uma sessão VC no Learning Manager selecionando o evento do BlueJeans apropriado. Os detalhes de data e hora são escolhidos automaticamente nos eventos do BlueJeans.
* **Sincronização de conclusão de usuário automatizada:** um processo automatizado de sincronização de conclusão do usuário permite que o administrador do Learning Manager busque registros de conclusão para eventos do BlueJeans automaticamente.

Este novo conector requer um conjunto separado de credenciais para configurar o conector.

Para obter mais informações, consulte [***Conector do BlueJeans Events***](../integration-admin/feature-summary/connectors.md#bj-events).

+++

+++Atualização 58 - Versão de dezembro de 2020 do Learning Manager

## Atualização 58 - Versão de dezembro de 2020 do Learning Manager

Data de lançamento: 05 de dezembro de 2020

### Novidades e alterações {#Whatsnewandchanged-2}

Esta versão concentra-se no seguinte:

* Experiência de página inicial do novo aluno
* Layout móvel responsivo para a função do aluno
* Recomendação baseada em IA para alunos
* E-mails de resumo semanais
* Lista de verificação
* Marketo para envolver a integração
* Domínio personalizado
* Importação do questionário do Adobe Connect
* Link profundo para o catálogo dos alunos
* Aprimoramentos do LinkedIn Learning
* ...e muito mais

Para obter mais informações, consulte [***Novidades do lançamento do Adobe Learning Manager em dezembro de 2020***](../whats-new.md).

### Recursos não suportados em experiência imersiva móvel {#unsupportedfeaturesinmobileimmersiveexperience}

Os seguintes recursos não são suportados:

* Aplicativo Social: um aluno é redirecionado para a experiência Clássica se clicar no widget Social na Página inicial
* Configurações de perfil/Editar perfil
* Exibir medalha/habilidades
* Quadro de classificação: um aluno é redirecionado para a experiência Clássica se clicar no widget Quadro de classificação na Página inicial
* Baixando ajudas de tarefa.
* Opções de filtro na Pesquisa.

### Erros corrigidos nesta atualização {#bug-fixes-1}

* Não é possível excluir uma pasta de conteúdo se ela contiver conteúdo excluído.
* O Plano de aprendizado permite que os administradores configurem um curso com instância automática. Para um curso com o módulo de envio de atividade, as informações do professor não estavam sendo configuradas corretamente anteriormente. Agora o Learning Manager atribui o professor da instância padrão a essa instância automática automaticamente.
* Um emblema personalizado com um rótulo de catálogo com um espaço não permite que o pdf seja baixado conforme esperado.
* Um relatório baixado do painel é diferente do e-mail de assinatura recebido para o relatório do painel.
* Uma transcrição do aluno não tem dados atualizados para uma certificação periódica.
* Após iniciar um curso, se você deixar o curso expirar, o número de tentativas não será exibido conforme esperado. Também, há uma tela em branco às vezes quando você tenta um curso várias vezes.
* Há o erro 5xx após o carregamento de um módulo.
* Um quadro social privado não é visível para todos os alunos.

### Problemas conhecidos desta atualização {#known-issues-1}

Após concluir um curso ou certificação, você não verá o pop-up de feedback imediatamente. Esse problema ocorre somente quando você faz o curso na interface do usuário imersiva. Se você fizer o curso na interface do usuário clássica, poderá ver a janela pop-up de feedback como esperado.

+++

+++Atualização 57

## Atualização 57

Data de lançamento: 23 de setembro de 2020

**Biblioteca de conteúdo**

* Na biblioteca de conteúdo, desativar um conteúdo não remove o conteúdo na guia **Publicado**. Quando você atualiza a página, o conteúdo retirado não é mais exibido.
* Ao criar uma pasta de conteúdo, o campo **Nome** não é marcado como obrigatório, o que na verdade é um campo obrigatório.

**Solicitação do cliente**

* Para identificar todos os cursos nos quais cada aluno está inscrito e se os concluiu, inclua os seguintes campos no painel, Relatório de assinatura:

   * UUID
   * Endereço de email

**Transcrição do aluno**

* Gerar uma transcrição do aluno no idioma indonésio estava causando erros.

**Pesquisa**

* Não é possível pesquisar um curso específico. Esse problema foi corrigido.

+++

+++Atualização 56 - Aplicativo móvel

Data de lançamento: 25 de agosto de 2020

### Faça cursos no LinkedIn Learning {#takecoursesfromlinkedinlearning}

O Learning Manager já é compatível com os cursos do LinkedIn Learning dentro da plataforma de aprendizado. Agora os alunos podem realizar esses cursos do LinkedIn Learning no aplicativo móvel do Learning Manager. No aplicativo do dispositivo, pesquise um curso e inicie-o.

Para obter mais informações, consulte Realizar cursos do [***LinkedIn Learning***](../learners/feature-summary/ipad-android-tablet-users.md#linkedin).

### Notificação push para inscrições de administrador {#pushnotificationforadminenrollments}

Quando o administrador inscreve os alunos em treinamentos, eles receberão notificações sobre as inscrições.

A notificação push agora também é suportada para comunicados.

### Feedback L1 obrigatório {#mandatoryl1feedback}

Na versão de agosto de 2020 mais recente, o Learning Manager permite que os administradores configurem feedback L1 de modo que todas as perguntas se tornem obrigatórias. O mesmo agora é compatível com a perspectiva do aluno no aplicativo móvel.

### Melhorias na interface do usuário {#userinterfaceenhancements}

**Links do rodapé**

O administrador pode configurar vários links de rodapé na exibição Administrador na Web. Os alunos agora podem acessar esses links tocando no ícone Hambúrguer e no ícone Ajuda.

Por padrão, haverá dois links e o administrador pode adicionar outros três links (por meio da visualização do administrador na Web) que serão exibidos no aplicativo.

**Exibição de cartão para objetos de aprendizado**

Por padrão, nas seções Meu aprendizado e Catálogo do aplicativo, os treinamentos são exibidos como cartões em vez de listas. Isso é uma alteração para os alunos, pois antes a exibição padrão era “Exibição em lista”.

No entanto, os alunos podem alternar a exibição entre a Exibição em lista e a Exibição em cartão.

+++

+++Atualização 55 - Versão de agosto de 2020 do Learning Manager

Data de lançamento: 23 de agosto de 2020

### Novidades e alterações {#Whatsnewandchanged-3}

Esta versão concentra-se no seguinte:

* Melhorias nos relatórios
* Pastas de conteúdo privadas
* FTP personalizado
* Suporte a legendas para vídeos
* Melhorias no Power BI
* Melhorias no feedback
* APIs novas e alteradas
* Alterações na política de retenção de dados
* ...e muito mais

Para obter mais informações, consulte [***Novidades do lançamento do Adobe Learning Manager em agosto de 2020***](../whats-new.md).

### Notas sobre esta versão {#notes}

* Gerar uma transcrição do aluno (~1 GB) leva menos de 15 minutos.
* Em versões anteriores do Learning Manager, Pontuação do questionário das colunas de transcrição do aluno e Pontuação do questionário mais alta usadas para fornecer a pontuação e a pontuação máxima no formato 25/100. Para oferecer suporte a fim de uma melhor legibilidade e análise, a pontuação do questionário agora também é exportada como colunas separadas - **Pontuação_no_quiz, Pontuação_máxima_no_quiz, Pontuação_mais_alta_no_Quiz e Maior_pontuação_máxima_no_quiz**. Isso permite que os administradores façam cálculos e análises rápidamente.

### Erros corrigidos nesta atualização {#bug-fixes-2}

**Conector**

* Um aluno não pode participar de duas reuniões diferentes ao mesmo tempo, que são criadas por dois autores diferentes.
* Clicar na opção Gerenciar conexões do cartão Adobe Connect leva até a página de conexão FTP.
* Uma sincronização FTP programada é encerrada com uma exceção.
* Há problemas relacionados a senha ao se conectar ao Exavault.

**Curso**

* Você pode criar um módulo VC sem selecionar qualquer sistema de conferência. Como efeito colateral, o processo de criação de um curso gera o Erro 500.
* Um aluno não pode baixar recursos mesmo que esteja inscrito em um curso que foi duplicado.
* Ao visualizar um curso como aluno, um administrador ou autor não pode baixar recursos a menos que esteja inscrito no curso.

**Aplicativo de dispositivo**

* Em casos específicos de inscrições, o gráfico de rosca em Meu aprendizado pendente exibe valores diferentes do aplicativo do aluno do navegador para o aplicativo móvel.

**Certificação**

* O status do filtro de relatório não funciona como esperado ao tentar baixar um relatório do painel para certificação.

**Pesquisa**

* Na página do catálogo do aluno, quando você tenta pesquisar um curso pela nota, nenhum resultado de pesquisa é exibido.

**SCORM**

* Para alguns conteúdos, o player do SCORM exibe uma tela em branco.
* Um conteúdo do Storyline é identificado como um conteúdo do Captivate, se o projeto do Storyline publicado tiver um objeto da Web apontando para a saída publicada do Captivate.
* O conteúdo do SCORM não pode ser iniciado devido ao url incorreto.

**Função personalizada**

* Em determinadas situações, um administrador personalizado não pode ver a lista completa de objetos de aprendizado.
* Um administrador personalizado não pode procurar por um programa de aprendizado ou certificação nos relatórios do painel.
* Um administrador personalizado não pode procurar por um gerente em um painel.
* As transcrições do aluno geradas por um administrador personalizado não contêm dados de usuários excluídos.
* Um autor ou administrador personalizado não pode duplicar um programa de aprendizado ou um curso ou certificação.

**Relatórios**

* A coluna Tipo em uma transcrição do aluno exibe o valor como curso para os cursos que fazem parte de uma certificação, se o aluno não estiver inscrito na certificação.

**Habilidades**

* Ao adicionar uma habilidade para um curso, há alguns problemas ao procurar por uma habilidade.

**Gamificação**

* Se muitos usuários forem considerados confidenciais, ao clicar na guia confidencial do aluno no Edge e Internet Explorer, o navegador se comporta de forma inesperada.
* Quando a frequência de um critério é alterada, os pontos calculados com frequência mais antiga são adicionados ao cálculo atual.

**Administrador**

* Os alunos não podem ser marcados como participantes se a instância do curso mapeada para um programa de aprendizado for alterada.

**Modelos de e-mail**

* Para Programas de aprendizado e Certificações, o botão alternar no modelo de e-mail está ausente.

**Biblioteca de conteúdo**

* O conteúdo do SCORM não é iniciado conforme esperado devido ao url incorreto.

**Transcrições do aluno**

* Ao gerar transcrições do aluno, se você adicionar um aluno excluído na caixa de entrada Selecionar alunos e ativar a opção &quot;Incluir dados de alunos excluídos&quot; em Avançado, a página se comporta de forma inesperada.

**Pesquisa**

* Não é possível pesquisar um curso usando as suas notas.

**Relatórios do Excel**

* Se um relatório de trilha de auditoria do usuário levar mais de uma hora para baixar devido a dados grandes ou processamento lento, a conexão expira e o relatório nunca é baixado.
* Em uma transcrição do aluno, a coluna Tipo é exibida como &quot;Curso&quot; em vez de &quot;Certificação&quot; para os cursos que fazem parte da certificação, se o aluno não estiver inscrito na certificação.

**Aplicativo do aluno**

* Um aluno pode realizar um curso solicitado de forma não ordenada acessando os cursos por meio de um e-mail de cancelamento de inscrição ou de uma notificação de cancelamento de inscrição.
* Um aluno não recebe os e-mails de lembrete de sessão conforme esperado.
* Um curso não é iniciado como esperado se um determinado módulo estiver ausente.

**Comunicados**

* Se um comunicado contém a marca `<a>`, ele não é criado conforme esperado.

**A conta**

* Em alguns casos, as contas são desativadas mesmo que uma conta tenha uma OC válida.

**API**

* Se clicar em Gerenciar conexões no cartão do Adobe Connect, você será redirecionado para a página Conexão FTP.
* Em alguns casos, o administrador do Connect recebe alertas incorretos.
* A migração do LinkedIn Learning produz alguns erros.

### Problemas conhecidos desta atualização {#known-issues-2}

**Relatórios do painel**

* Quando um Programa de aprendizado de certificação é excluído, o relatório Treinamento ativo exibe os cursos presentes no Programa de aprendizado ou na certificação, mesmo que o Programa de aprendizado ou a certificação não tenham inscrições.

+++

+++Atualização 54 - Aplicativo móvel

## Atualização 54 - Aplicativo móvel

Data de lançamento: 16 de abril de 2020

Para obter os recursos mais recentes, atualizações e uma experiência melhor, recomendamos atualizar o aplicativo para dispositivos para a versão mais recente. A atualização é **obrigatória**.

### Recursos novos e aprimorados {#newandenhancedfeatures}

Um administrador pode comunicar informações importantes a todos os usuários do aplicativo. Os comunicados podem ser do tipo vídeo ou imagem ou uma mensagem de texto simples. Com esta versão do aplicativo para dispositivos, agora oferecemos suporte a comunicados no aplicativo. Um novo comunicado será exibido assim que o aplicativo for iniciado, para que os alunos não percam nenhuma comunicação importante enviada pelos administradores. Os alunos podem lê-lo instantaneamente ou posteriormente acessando a guia **Comunicados**.

Quando houver um anúncio ou vários comunicados, você poderá ver os comunicados na seção **Anúncios**.

Para ver um anúncio, toque em **Anúncios**. O anúncio mais recente é exibido na tela.

Para ver o próximo anúncio, toque em **Deslizar para a esquerda para ir para o próximo**.

### Comunicados {#announcements}

![](assets/read-later.png)

Se você não quiser ler o anúncio nesse momento, poderá optar por ler o anúncio mais tarde. Toque em **Ler mais tarde** no anúncio e o anúncio retornará ao estado não lido.

### Erros corrigidos nesta atualização {#bugsfixedinthisupdate}

* No iOS, um podcast para de ser reproduzido quando a tela estiver bloqueada. O problema foi corrigido e o áudio será reproduzido mesmo quando a tela estiver bloqueada.
* Se você fizer um curso no aplicativo para dispositivos, o slide de resultado pode às vezes aparecer em branco. Esse problema foi corrigido nesta atualização.

+++

+++Atualização 53 - Versão de abril de 2020 do Learning Manager

Data de lançamento: 04 de abril de 2020

O lançamento do Learning Manager em abril de 2020 focou no seguinte:

* [Aprimoramentos do desempenho](../whats-new.md#performance)
* [Treinamento em sala de aula](../whats-new.md#classroom)
* [Fluxos de trabalho do gerente](../whats-new.md#manager)
* [Aprendizado social](../whats-new.md#social)
* [Relatórios](../whats-new.md#reporting)
* [Experiência do aluno](../whats-new.md#learner)
* [Alterações a nível da API](../whats-new.md#api)

Para mais informações, consulte [***Novidades do lançamento do Learning Manager em abril de 2020***](../whats-new.md).

+++

+++Atualização 52 - Aplicativo móvel

## Atualização 52 - Aplicativo móvel

Data de lançamento: 20 de dezembro de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-1}

#### Logotipo da marca da empresa {#companybrandinglogo}

O aplicativo agora tem a capacidade de exibir o nome da marca, o logotipo da marca ou ambos dentro do aplicativo do dispositivo, dependendo das configurações definidas pelo administrador.

#### Links profundos {#deeplinks}

O Learning Manager agora inicia o aplicativo do dispositivo assim que você clica em um link/URL suportado pelo Learning Manager. Se o aplicativo não estiver instalado no dispositivo, o URL é aberto no navegador.

Aqui estão alguns casos de uso, que serão suportados nesta atualização.

* Clique no URL de um treinamento recebido por e-mail.
* URLs de treinamento padrão que aparecem nos modelos de e-mail.
* URL da conta que aparece nos modelos de e-mail.
* URLs de acesso a Meus aprendizado e ao Catálogo.

Além disso, qualquer URL com um domínio *learningmanager.adobe.com* é aberto no aplicativo do dispositivo.

#### Carregar ativos no certificado externo como comprovante de conclusão {#uploadassetsinexternalcertificateasproofofcompletion}

Nesta atualização, o aluno pode carregar ativos como comprovante de conclusão de um certificado externo.

O aluno pode abrir um certificado externo e carregar ativos, tais como pdf, texto ou arquivos de imagem.

Para obter mais informações, consulte [***Carregar ativos no certificado externo***](../learners/feature-summary/ipad-android-tablet-users.md#externalcert).****

### Problemas corrigidos nesta versão {#issuesfixedinthisrelease}

* O usuário não consegue fazer logon no aplicativo do dispositivo se o e-mail contiver caracteres especiais.
* Ao rolar, o ícone do Objeto de aprendizado pisca quando você estiver na visualização de lista.
* Agora você pode visualizar todas as notificações por push sem pressionar o botão de seta para baixo e ver as mensagens uma de cada vez.
* Ao clicar em uma notificação de uma publicação que foi aceita ou rejeitada na curadoria, uma página em branco é aberta no aplicativo. Nesta atualização, a página do painel é aberta.

+++

+++Atualização 51

Nesta atualização, você também pode alterar a imagem do banner de um Objeto de aprendizado.

Você também pode personalizar o banner em uma página de Aprendizado social.

## Atualização 51

Data de lançamento: 17 de dezembro de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-2}

### Planos de aprendizado com escopo definido por funções configuráveis {#learningplansscopedbyconfigurableroles}

Você pode criar Funções personalizadas para Planos de aprendizado que permitam a definição de escopo de usuários e Objetos de aprendizado. Em outras palavras, os Planos de aprendizado podem ser criados com um escopo limitado, derivado do escopo da função de um administrador personalizado.

Agora, um Administrador pode definir ou restringir o escopo enquanto concede acesso ao gerenciamento do plano de aprendizado.

Para obter mais informações, consulte [***Planos de aprendizado com escopo definido por funções configuráveis***](../administrators/feature-summary/custom-role.md#scopeconfigure).

### Restringir campos ativos nos relatórios {#restrictactivefieldsinreports}

Para Campos Ativos, adicionamos duas novas opções: **Relatável** e **Exportável**.

Nos campos CSV e campos adicionados manualmente, se um Campo ativo estiver marcado como **Relatável**, o Campo ativo será pesquisável em um filtro dentro de um relatório do painel.

Para obter mais informações, consulte [***Restringir campos ativos nos relatórios***](../administrators/feature-summary/add-users-user-groups.md#restrictactivefields)***.***

### Exibir descrição do módulo de conteúdo {#viewdescriptionofcontentmodule}

Como autor, você pode ver a descrição dos módulos enquanto adiciona o módulo a um curso.

Ao criar um módulo, adicione sua descrição. Para saber mais sobre como criar um curso, consulte [***Criar um curso***](../authors/feature-summary/courses.md).

### Exibir nomes de curso e sessão {#displaycourseandsessionnames}

Como professor, você pode ver os nomes dos cursos e das sessões na visualização Presença. Você pode acompanhar as sessões que estão sendo modificadas.

### Anúncio para os alunos {#announcementforlearners}

Agora, os alunos podem visualizar um anúncio em tela cheia, em vez de em uma lista. Isso acontece quando o aluno tem um anúncio não lido. Isso melhora a experiência dos alunos na visualização do anúncio.

O Adobe Learning Manager agora permite que você personalize sua conta para proporcionar uma experiência mais completa aos seus usuários. Veja uma lista de elementos que podem ser personalizados. Contate o [suporte do Learning Manager](mailto:learningmanagersupport@adobe.com)para fazer essas alterações.

* Cores do cartão de treinamento.
* Ícone Progresso
* Imagem do ponteiro do mouse
* Fonte

Para obter mais informações, consulte [***Personalizar sua conta***](../administrators/feature-summary/themes.md#customize).

### Carregar imagens do banner {#uploadbannerimages}

Nesta atualização, você também pode alterar a imagem do banner de um Objeto de aprendizado.

Você também pode personalizar o banner em uma página de Aprendizado social.

### Suporte à API {#apisupport}

Esta atualização do Learning Manager inclui API para as seguintes operações:

**Baixar PDF da medalha**

Esta atualização inclui uma permissão para a API do aluno para baixar a medalha em PDF.

**Baixar transcrição do aluno**

Esta atualização inclui uma permissão para a API do aluno para baixar a transcrição do aluno.

**Baixar relatório do questionário**

Esta atualização inclui uma permissão para a API do administrador para baixar relatórios do questionário.

**Gamificação paginada**

A API do aluno agora permite a busca de todos os pontos do aluno e de gamificação no escopo do aluno. Isso ajuda a construir um quadro de classificação de gamificação.

**API:** `GET /users`

**Solicitação:** `GET\\ users?page[offset]=0&page[limit]=10&sort=id&filter=gamification`

**Resposta:** *A resposta conterá os usuários classificados por ordem de pontos de gamificação.*

**Não incomodar**

Atualmente, apenas os administradores podem adicionar usuários a uma lista Não perturbe através da interface do usuário. Após esta versão, o aluno poderá definir essas permissões por meio da API, desde que essa API seja ativada pelo administrador. A ativação da API em uma conta requer uma configuração de backend. Essa API permite que o aluno edite as permissões abaixo relacionadas aos e-mails.

* Direcionar e-mails ao aluno
* E-mails de escalonamento para gerentes de alunos
* Relatórios diretos do Sobre
* Sobre relatórios de nível superior

Para obter mais informações sobre as APIs do Learning Manager, consulte o site a seguir:

* [***Referência de API***](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v2/)
* [***guia do desenvolvedor da API***](<https://helpx.adobe.com/captivate-Learning> Manager/integration-admin/feature-summary/developer-manual.html)

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-1}

* Somente usuários pertencentes a um grupo de usuários específico devem receber anúncios destinados a eles. Outros usuários não devem receber os anúncios.
* O reprodutor exibe um ícone giratório de carregamento antes da exibição do conteúdo.
* Os metadados do usuário nos relatórios causam uma exceção Null Pointer.
* Ao adicionar um professor para uma instância padrão do curso Connect VC, a mensagem *&quot;Sem sessão para este módulo&quot;* é exibida na página Instância do curso do aplicativo do administrador.

* A exportação de uma transcrição do aluno gera um comportamento inesperado durante uma transferência FTP.
* O nome de um autor é exibido incorretamente nos cursos de um programa de aprendizado.
* As alterações na terminologia do produto da ajuda de tarefa não refletem conforme o esperado.
* O nome de um módulo fica truncado se o nome for longo e for exibido no modo retrato móvel.
* Não é possível criar uma instância para um curso mais antigo do Connect após atualizar a instância padrão com a implementação mais antiga do Connect.
* Um professor recebe um convite de calendário mesmo antes da publicação do curso.

+++

+++Atualização 50

## Atualização 50

Data de lançamento: 24 de outubro de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-3}

#### Criar função personalizada com vários escopos de catálogo {#createcustomrolewithmultiplecatalogscopes}

Como administrador, você pode restringir uma função personalizada com base em catálogos e grupos de usuários. Todos os usuários pertencentes a essas funções podem ver apenas os objetos de aprendizado no catálogo que estão em seus escopos. Esses usuários podem executar somente as ações que foram definidas no escopo dos seus grupos de usuários.

Até o momento no Learning Manager, uma função personalizada pode estar no escopo de vários catálogos de um único grupo de usuários com permissões completas.

Nesta atualização do Learning Manager, você pode criar uma função personalizada que estará no escopo de vários catálogos e a cada catálogo será concedido um conjunto diferente de permissões. Para obter mais informações, consulte [***O escopo da função personalizada em vários catálogos***](../administrators/feature-summary/custom-role.md#multi-scope).

### Aprimoramentos na pesquisa {#enhancementstosearch}

**Plano de aprendizado**

Na página Planos de aprendizado de administradores e autores, agora existe uma barra de pesquisa que pode ser usada para pesquisar qualquer plano de aprendizado.

![](assets/search-for-as-learningplan.png)

**Aplicativos para administrador e autor**

Nesta atualização do Learning Manager, como administrador ou autor, além de executar uma pesquisa com preenchimento automático, é possível realizar a pesquisa livre para pesquisar qualquer objeto de aprendizado.

### O filtro de pesquisa é preservado {#searchfilterispreserved}

Isso se aplica somente a um perfil do aluno.

Nas páginas **Catálogo** e **Meu aprendizado**, o aluno pode aplicar filtros no painel esquerdo, por exemplo, **Cursos** ou **Programas de aprendizado** e, a seguir, clicar no item Curso ou Catálogo.

![](assets/choose-learning-objects.png)

Quando o estudante volta para as páginas **Catálogo** ou **Meu aprendizado** utilizando o botão Voltar do navegador, o filtro é preservado. O filtro que um aluno aplicou anteriormente não é mais redefinido.

### Controlar a visibilidade dos filtros de pesquisa {#controlvisibilityofsearchfilters}

Nas versões anteriores do Learning Manager, os administradores não tinham controle sobre as opções de visibilidade de um filtro do catálogo para que os alunos não vissem as habilidades e as etiquetas. Nesta versão do Learning Manager, o administrador pode filtrar tipos, habilidades e etiquetas de um catálogo.

Na página **Configurações**, na categoria Mostrar painéis de filtro, ao clicar em **[!UICONTROL Editar]**, é possível ver as seguintes opções. As opções determinam os painéis de filtro que estarão visíveis aos alunos para que os alunos possam definir os resultados da pesquisa.

Para obter mais informações, consulte [***Mostrar painéis de filtro***](../administrators/feature-summary/settings.md#filter-panels).

### Baixar código QR do aplicativo do administrador {#downloadqrcodefromadministratorapp}

Nas atualizações anteriores do Learning Manager, os administradores personalizados enfrentavam problemas ao baixar um código QR. Nesta atualização, os administradores personalizados que têm acesso a **Todos os alunos** e permissão para **Inscrição no curso** podem baixar o código QR.

O código QR ainda não está disponível para usuários personalizados com função personalizada caso eles tenham permissão para um escopo limitado de usuários.

### Adicionar comentários ao inscrever alunos {#addcommentswhileenrollinglearners}

Como administrador ou gerente, você pode adicionar comentários ao inscrever alunos em um curso. Você pode mencionar informações adicionais sobre o coorte dos usuários que estão sendo inscritos. Esses dados são exportados nos relatórios do curso.

Para obter mais informações, consulte [***Adicionar comentários ao inscrever alunos***](../administrators/feature-summary/courses.md#enroll-comments).

### Suporte para sala de reunião permanente do Adobe Connect {#supportforadobeconnectpersistentmeetingroom}

No Adobe Connect, os clientes usam as salas de reuniões existentes que já foram criadas no Connect. Todas as salas de reunião do Connect são permanentes e os modelos de sala de reuniões são configurados com cuidado para fornecer uma experiência unificada para cada sala permanente.

Nesta versão do Learning Manager, a integração com o Adobe Connect foi aprimorada agora para oferecer suporte também a salas permanentes. Isso significa que agora é possível criar uma sessão de sala de aula virtual usando uma sala já criada no Adobe Connect.

Agora, o Learning Manager também permite que os alunos entrem na sala do Connect para suas sessões virtuais usando a autenticação SSO.

Para obter mais informações, consulte [***Suporte a sala permanente no Adobe Connect***](../integration-admin/feature-summary/connectors.md#persistent).

### Aviso antes de marcar a participação se a duração da sessão for zero {#warningbeforemarkingattendanceifthesessiondurationiszero}

O autor ou administrador pode criar uma sessão com uma duração de 0. Isso é possível quando:

* A data de início e/ou a data de término estão vazias.
* A hora de início e/ou a hora de término estão vazias.

Nesta atualização, a **mensagem de aviso que afirma que a duração de uma sessão é zero** é mostrada ao administrador, gerente ou professor.

### Aviso se um módulo de sala de aula for criado sem adicionar dados da sessão {#warningifaclassroommoduleiscreatedwithoutaddingsessiondata}

Se um autor cria um curso adicionando um módulo de sala de aula ou de sala de aula virtual, o autor pode:

* Não adicionar uma data/hora de início/término.
* Adicionar uma data, mas não hora de início/término.
* Adicionar uma data e uma hora de início.

Em qualquer uma das situações acima, quando um administrador, gerente ou professor marca a participação ou a conclusão, os valores da data de início e da data de término da sessão são igualados, o que significa que em uma transcrição do aluno, o valor do tempo de aprendizado gasto é exibido como zero.

Nesta atualização, uma **mensagem de aviso que indica que os dados da sessão estão incompletos** é exibida ao autor.

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-2}

**Aplicativo do aluno**

* Um aluno não pode visualizar um curso em um Programa de aprendizado se o curso tiver sido criado por um autor externo.
* Se um administrador adiciona uma publicação a um painel externo, a solicitação de curadoria vai para um SME interno, que tem essa habilidade atribuída a ele.
* Um aluno não pode visualizar o botão Iniciar ou Continuar depois de se inscrever nos cursos do LinkedIn.

**E-mail**

* Quando havia um grande número de usuários em uma lista de DNDs de e-mail, a página **Configurações** era carregada muito lentamente. Nesta atualização, é adicionada a paginação a uma lista de DNDs de e-mail.
* Um professor recebe atualizações/e-mails de sessões das quais não faz parte. Nesta atualização, isso foi corrigido.

**Habilidades**

* Em uma transcrição do aluno, o tipo de valor de uma habilidade é exibido incorretamente como texto.

**Aplicativo para dispositivos móveis**

* No aplicativo móvel, um aluno podia visualizar e se inscrever em uma instância do Plano de aprendizado, o que não era o comportamento pretendido. Nesta atualização, isso foi corrigido.

**Funções personalizadas**

* Como administrador personalizado, você não pode pesquisar por um gerente em um relatório do painel.

**Várias tentativas**

* Em algumas situações, alguns módulos do curso não são exibidos aos alunos.

**Inscrição externa**

* Não é possível alterar o perfil externo de um usuário se as vagas dos perfis principais foram preenchidas.

### Problemas conhecidos nesta versão {#knownissuesinthisrelease}

* Nos navegadores mencionados abaixo, ao passar o mouse sobre o painel esquerdo, o texto aparece após um pequeno atraso.

   * Edge 42.17134.1.0
   * Edge 44.17763.1.0
   * Internet Explorer 11.1006
   * Internet Explorer 11.615

* Um aluno pode entrar na sala de reuniões do Connect antes e depois da sessão.

+++

+++Atualização 49

## Atualização 49

Data de lançamento: 26 de agosto de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-4}

**Aprimoramentos do desempenho**

* A importação de usuários no sistema é mais rápida em comparação às versões anteriores. Há uma melhoria importante ao importar grandes dados do usuário.
* Para gerentes e administradores, as opções na lista suspensa Configuração do relatório foram modificadas para carregar os dados sob demanda.
* O desempenho da API foi melhorado. Muitas APIs devem ter agora um melhor tempo de resposta.
* O tempo necessário para gerar transcrições do aluno melhorou.
* Não há atraso nas páginas nas quais os alunos internos e externos estão listados, especialmente quando há um grande número de usuários.

**Privilégios especiais de usuário**

Um administrador pode conceder privilégios especiais a um grupo de usuários, definindo quais membros do grupo podem participar em todos os painéis. Todas as restrições definidas na seção Configurações de escopo são ignoradas pelos grupo de usuários especiais. Para obter mais informações, consulte [***Privilégios especiais de usuário***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#privilege).

**Alterações na interface do usuário**

* Na caixa de diálogo **Adicionar relatório**, os seletores de **Intervalo de tempo** e **Filtros** aparecem como seções separadas, que estão no estado recolhido, por padrão. Para obter mais informações, consulte [***Criar relatórios***](../administrators/feature-summary/reports.md#report).

* Na caixa de diálogo **Adicionar relatórios** de um grupo de usuários, você pode usar a pesquisa com preenchimento automático para escolher um único ou vários grupos de usuários. Para obter mais informações, consulte [***Relatórios do grupo de usuários***](../administrators/feature-summary/reports.md#user-group-reporting).

**Alterações nos valores das colunas Tempo**

Nas transcrições do aluno, nas colunas de tempo, os minutos são arredondados até o minuto mais próximo e o valor do segundo é 00. Para obter mais informações, consulte [***Colunas de tempo***](../administrators/feature-summary/learner-transcripts.md#datetime).

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-3}

**Painel do aluno**

* Um Calendário de Aprendizado exibiu o status **Sessão Inscrita** mesmo quando um Gerente ainda não estava para aprovar a inscrição. Agora o status correto **Pendente** é exibido ao aluno até que o gerente aprove a inscrição.

* Em um caso específico, para uma sessão, o Calendário de aprendizado exibia o status **Inscrito**, mesmo que o aluno tenha concluído um curso.

**Painel do gerente**

* Os gerentes não podiam controlar os treinamentos de conformidade da sua equipe se os membros da equipe tivessem se inscrito através dos Planos de aprendizado.

**Pesquisa**

* Na visualização do professor, não era possível procurar um aluno.

**Interface do usuário**

* Em uma conta com alterações de taxonomia, as alterações não eram refletidas conforme esperado nas notificações.

### Problemas conhecidos nesta versão {#Knownissuesinthisrelease-1}

* Usando a barra de pesquisa, não é possível pesquisar por usuários excluídos na lista de usuários externos. Como solução alternativa, role para baixo para exibir a lista de todos os usuários e localize o usuário necessário manualmente.
* Se um usuário especial publicar em um painel externo, a solicitação de curadoria é recebida pelos SMEs no escopo seu escopo.

+++

+++Atualização 48

## Atualização 48

Data de lançamento: 02 de agosto de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-5}

**Separação de escopo no Aprendizado social para usuários internos e externos** Um administrador pode definir escopos separados para alunos internos e externos. Existem duas novas seções para usuários internos e externos. Em ambas as seções, você pode definir os escopos para os grupos de alunos. Para usuários internos, você pode definir os valores da Característica do usuário. Para usuários externos, você pode definir o perfil externo, em que os alunos podem compartilhar o mesmo espaço social. Para obter mais informações, consulte [***Configurações do escopo***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#scopesettings).  **Social-Restringir criação de painéis sociais** Para restringir a criação de painéis por todos os alunos e moderar os painéis de forma eficaz, um administrador pode conceder permissões para criar painéis para um grupo seleto de usuários. O administrador pode restringir a criação de um painel a apenas um grupo selecionado e não a todos os alunos que participam do aprendizado social. Para obter mais informações, consulte [***Permissões de criação de painel***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#permission).  **Exibir apenas campos ativos vazios para os alunos** Um administrador pode optar por exibir os campos ativos ou ocultá-los depois que os valores forem preenchidos. Para obter mais informações, consulte [***Exibição do usuário***](../administrators/feature-summary/add-users-user-groups.md#activefields).  **Os usuários internos são excluídos após uma duração especificada de inatividade** Um administrador pode definir a duração (em dias) dentro da qual um aluno interno é excluído se ele permanecer inativo durante a duração especificada. Para obter mais informações, consulte ***[Excluir usuários automaticamente](../administrators/feature-summary/settings.md#autodelete)***.  **Personalizar links no rodapé** Um administrador pode adicionar e personalizar links no rodapé. Os links também podem ser personalizados para várias localidades. O método existente de adicionar o link Contatar administrador no rodapé também está disponível na seção **Links de rodapé**. Para obter mais informações, consulte [***Personalizar links de rodapé***](../administrators/feature-summary/settings.md#footer).

### Problemas conhecidos nesta versão {#Knownissuesinthisrelease-2}

* Os links de rodapé personalizados não aparecem para as funções do administrador de integração.

+++

+++Atualização 47 - Aplicativo móvel

## Atualização 47 - Aplicativo móvel

Data de lançamento: 24 de julho de 2019

Usuários do Android:

Esta atualização também suporta as alterações necessárias para aderir às recomendações revisadas da Google para implementar notificações por push. Portanto, você não receberá mais **notificações** se estiver usando a versão 2.7.4 ou mais antiga.

Para receber notificações, recomendamos atualizar para a versão 2.8.

### Recursos novos e aprimorados {#Newandenhancedfeatures-6}

**Aprendizado social**

Compartilhe sua experiência com colegas na forma de conteúdo gerado pelo usuário publicado em painéis de discussão baseados em tópicos. Outros alunos interessados em habilidades semelhantes podem seguir esses painéis para contribuir e aprender sobre o tópico, como em uma plataforma de mídia social.

Compartilhe ideias e insights significativos em um ambiente informal. Curta e deixe de curtir publicações, carregue conteúdo e comente em publicações. Para obter mais informações, consulte [***Aprendizado social no aplicativo móvel***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Compartilhar mídia em um painel**

Compartilhe imagens, documentos ou arquivos de áudio ou vídeo com qualquer painel, para que outros membros do painel possam visualizar sua publicação e iniciar uma interação.  Para obter mais informações, consulte [***Compartilhar publicação***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Enviar arquivos para os módulos de sala de aula e de atividade**

Envie de arquivos como comprovantes de conclusão do curso ao professor. O professor pode aprovar ou rejeitar o envio, com base no conteúdo do arquivo. Para obter mais informações, consulte [***Enviar arquivo para aprovação***](../learners/feature-summary/ipad-android-tablet-users.md#submitfile).

**Suporte atualizado da plataforma**

O aplicativo móvel Learning Manager para dispositivos móveis agora é compatível com dispositivos Android 7 e acima e dispositivos iOS 10 e superior. Para obter mais informações, consulte [***Requisitos do sistema***](../system-requirements.md).

### Problemas conhecidos nesta versão {#Knownissuesinthisrelease-3}

1. No Android, você não pode carregar um arquivo GIF em uma publicação, fazer comentários ou ao responder a um comentário.
1. Como moderador de qualquer painel, você não pode excluir publicações, comentários ou respostas dos usuários. No entanto, você pode executar essas ações no aplicativo da Web.
1. No aplicativo, você não pode marcar um tipo de pergunta.
1. Depois de ativar o aprendizado social no aplicativo, reinicie o aplicativo para ver a guia **Aprendizado social**. Se não vir a guia Aprendizado social, feche o aplicativo e, em seguida, reinicie-o. A guia Aprendizado social deveria estar visível.

+++

+++Atualização 46

### Recursos novos e aprimorados {#Newandenhancedfeatures-7}

## Atualização 46

Data de lançamento: 20 de junho de 2019

**Curadoria automática de conteúdo**

O aprendizado social permite dois métodos de curadoria do conteúdo publicado pelos alunos: **Sem curadoria** e **Curadoria manual**. Nesta versão, o Adobe Learning Manager aprimora o aprendizado social com recursos de curadoria automática por IA. Depois de publicado, o conteúdo é analisado para identificar se o conteúdo corresponde à habilidade atribuída. Com base na pontuação de confiança, o conteúdo é publicado ao vivo ou enviado para curadoria manual. Para obter mais informações, consulte *[** Curadoria assistida automaticamente **](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#autocuration)**.***

**Mapear habilidades com domínios de habilidades**

Mapeie habilidades em sua conta com os domínios de habilidades presentes no LMS do Learning Manager. Isso ajuda a vincular as habilidades da sua conta aos domínios de habilidades que o Learning Manager oferece suporte para curadoria assistida automaticamente. Para obter mais informações, consulte [***Mapear habilidade com domínios***](../administrators/feature-summary/curation-skills.md).

**Especificações do CSV e CSVs de amostra**

Especificações CSV atualizadas que você pode usar para mapear os dados existentes de migração do LMS. Use as especificações de csv para download mais recentes e os arquivos zip de csvs de amostra para entender o formato prescrito dos dados a serem inseridos. Para obter mais informações, consulte o [***Manual de migração***.](../integration-admin/feature-summary/migration-manual.md)

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-4}

**API do Learning Manager**

* Quando um perfil externo é adicionado pelo método POST da API *externalProfile*, o e-mail de boas-vindas não é exibido.

**Painel do gerente**

* Quando um gerente selecionou a opção **Neste trimestre**, os detalhes da inscrição, da progressão e da conclusão de um Objeto de Aprendizado não eram exibidos. Nesta versão, os detalhes são exibidos como esperado.

**Alunos em lista de espera**

* Nas versões anteriores do Learning Manager, depois do gerente inscrever os alunos, se um instrutor quisesse consultar os alunos em listas de espera, aparecia uma mensagem de erro. Nesta versão, um professor pode navegar na lista de alunos em lista de espera sem encontrar qualquer mensagem de erro.

**Visão geral da certificação**

* Quando um autor havia criado um curso e uma certificação com descrição e visão geral do conteúdo, caso um aluno acessasse a página do curso, a visão geral não era exibida como esperado. No entanto, o conteúdo estava visível nas páginas de visualização dos alunos nos aplicativos de Administrador e de Autor. Nesta versão, a visão geral aparece corretamente no aplicativo do Aluno.

**Catálogo**

* Em cada catálogo, o aluno pode exibir todos os objetos de aprendizado. Em versões anteriores, catálogos sem objetos de aprendizado ainda apareciam no início de outros catálogos. Nesta versão, catálogos que não possuem objetos de aprendizado aparecem na parte inferior dos catálogos.

+++

+++Atualização 45

Data de lançamento: 30 de maio de 2019

**Recursos novos e aprimorados**

* Pesquisa consolidada em todas as instâncias para alunos inscritos na seção Aluno do objeto de aprendizado. Pesquise por usuários inscritos na seção Aluno do objeto de aprendizado usando a pesquisa de digitação antecipada. Para obter mais informações, consulte [***Pesquisar por usuários inscritos***](../administrators/feature-summary/courses.md#searchforusers).
* Recursos completos de edição de objetos de aprendizado adquiridos por meio do catálogo compartilhado. Para obter mais informações, consulte [***Controle de catálogo compartilhado***](../administrators/feature-summary/shared-catalog-full-control.md). Para ativar o recurso, entre em contato com o suporte do Learning Manager.
* Os professores agora podem identificar facilmente as sessões e os módulos com revisões pendentes. Para obter mais informações, consulte [***Revisões pendentes***](../instructors/feature-summary/learners.md#pending).

* As habilidades agora oferecem suporte à concessão de valores de crédito no formato decimal. Isso permite que os autores concedam um valor de crédito de nível decimal a um determinado curso. Para obter mais informações, consulte [***Suporte a decimais***](../administrators/feature-summary/skills-levels.md#decimal).
* Automatize a criação de funções personalizadas. Para obter mais informações, consulte [***Configurar funções através de arquivos .csv***](../integration-admin/feature-summary/configure-role-csv-files.md).
* Os envios necessários para certificações externas e módulos de atividade agora são opcionais. Isso permite que gerentes e professores avaliem sem um envio. Para obter mais informações, consulte [***Envio opcional***](../managers/feature-summary/learning-objects.md#optional).
* Baixe as transcrições de aluno dos usuários excluídos. Para obter mais informações, consulte [***Transcrições do aluno***](../administrators/feature-summary/learner-transcripts.md).
* Suporte para os seguintes idiomas:

   * Coreano
   * Turco
   * Holandês
   * Polonês

**Problema conhecido**

* Os suporte a casas decimais nos créditos das habilidade é oferecido somente em inglês.
* Para os idiomas coreano, japonês e russo, o valor da hora do Meridiano de Greenwich da sessão não é exibido conforme o esperado.

**Problemas corrigidos nesta versão**

* As pontuações do questionário de um programa de aprendizado ou de uma certificação não são salvas nas guias Participação e Pontuação.
* Um administrador ou gerente não pode marcar como concluída uma certificação externa.
* Na caixa de diálogo Transcrições do aluno, um administrador não pode selecionar um intervalo de data personalizado se o idioma estiver definido como português ou espanhol.
* Um administrador não pode criar um perfil externo quando o idioma do perfil é o francês.
* Os campos ativos não estão visíveis na caixa de diálogo Editar usuário se o idioma não for o inglês.

+++

+++Atualização 44 - Aplicativo móvel

Data de lançamento: 26 de abril de 2019

* **Alterações na interface do usuário:** no aplicativo, as opções ![](assets/hamburger.jpg) e ![](assets/search-magnifying-glass-icon.png) agora aparecem na parte superior.

![](assets/1.png)

* **Digitalizar código QR para registrar:** os recursos de código QR foram aprimorados. Além do suporte à marcação de presença pelo código QR, esse recurso agora também oferece suporte à inscrição em cursos e à marcação da conclusão de um curso com o código QR.

  Para se inscrever e concluir um curso, você pode digitalizar um código QR fornecido pelo administrador. Para obter mais informações sobre a digitalização de códigos QR na versão Web do Learning Manager, consulte [***Digitalizar código QR***](<https://helpx.adobe.com/captivate-Learning> Manager/whats-new.html#QRcodetoenrollcompleteenrollcompletecourse).

* **Várias tentativas no curso:** o aplicativo Learning Manager permite que o aluno realize cursos com várias tentativas habilitadas. Para obter mais informações sobre como configurar várias tentativas, consulte [***Várias tentativas***](<https://helpx.adobe.com/captivate-Learning> Manager/authors/feature-summary/courses.html#Várias tentativas).

+++

+++Atualização 43

## Atualização 43

Data de lançamento: 28 de janeiro de 2019

* O tempo de aprendizagem usado por um aluno em um módulo podia ser contado várias vezes ao participar mais de uma vez. Esse problema foi corrigido.
* Marcar a presença de um objeto de aprendizado em uma sessão de vários dias pode exibir uma data de início incorreta da sessão para um aluno em uma transcrição de aprendizado. Esse problema foi corrigido.
* Os usuários podiam não ver um curso quando este curso era adicionado a um programa ou certificação de aprendizado concluído. Esse problema foi corrigido.
* O registro de usuários pode ocorrer incorretamente quando eles são movidos para fora de um grupo de usuários. Esse problema foi corrigido.
* O aluno e o instrutor podiam não receber um e-mail quando os detalhes da sessão eram alterados no aplicativo do instrutor. Esse problema foi corrigido.
* O URL do Adobe Connect podia não funcionar corretamente quando &#39;/’ era fornecido no final do URL. Esse problema foi corrigido.
* Uma mensagem de erro podia ser exibida na seleção de pelo menos um módulo obrigatório de um curso já publicado. Esse problema foi corrigido.
* Quando um aluno conclui um curso e este é marcado como obrigatório pelo autor, a conclusão do curso não pode ser marcada como concluída. Esse problema foi corrigido.
* O valor marcado de um módulo selecionado em um curso duplicado podia não aparecer imediatamente. Ele era exibido apenas como um curso duplicado quando a página era atualizada. Esse problema foi corrigido.
* Todos os módulos eram exibidos como desmarcados no modo de edição após a publicação de um curso. A página precisa ser atualizada para visualizar as alterações. Esse problema foi corrigido.
* A seleção de um módulo obrigatório podia estar disponível para um curso solicitado quando não deveria. Esse problema foi corrigido.
* Um módulo obrigatório continuava a aparecer na caixa de seleção suspensa mesmo após a remoção dele ao editar o curso. Esse problema foi corrigido.
* Os módulos de pré-trabalho e teste podiam estar marcados como obrigatórios por padrão. Esse problema foi corrigido.
* Ao clicar no link de feedback N3 no e-mail, o modo de feedback podia não abrir. Esse problema foi corrigido.
* A certificação está ausente no menu suspenso de relatório do painel, embora esteja visível no aplicativo do gerenciador e na lista de APIs de dados. Esse problema foi corrigido.
* Alguns objetos de aprendizado não puderam ser retirados pelo administrador devido à falta de permissões, embora os catálogos compartilhados sejam independentes das contas do Learning Manager. Esse problema foi corrigido.

+++

+++Atualização 42

Atualização 42

Data de lançamento: 11 de janeiro de 2019.

* A inserção de notificações do usuário pode falhar aleatoriamente, fazendo com que os emails associados não sejam entregues. Esse problema foi corrigido.
* `If a Learner is enrolled in Learning Program 1 and a Course in Learning Program 2, when the Learning Transcript is downloaded for a user group or more than one individual, the Learning Transcript may have missing data. This issue is fixed.`

+++

+++Atualização 41

Atualização 41Data de lançamento: 1º de dezembro de 2018.

* Os administradores podem controlar a permissão dada aos alunos para ver as pontuações do questionário nas transcrições do aluno. Isso pode ser ativado/desativado na página Configurações.
* A inserção de notificações do usuário pode falhar aleatoriamente, fazendo com que os emails associados não sejam entregues. Esse problema foi corrigido.
* Os dados do tempo gasto no aprendizado podem não ser exibidos na transcrição do aluno e nos relatórios do painel. Esse problema foi corrigido.
* Informações sobre atividades, como inscrição/conclusão, podem não estar presentes na transcrição do aluno baixada por um gerente. Isso foi corrigido.
* Os módulos que fazem parte de um curso em andamento podem aparecer como concluídos na transcrição do aluno. Esse problema foi corrigido.
* A transcrição do aluno pode não exibir os dados baixados conforme o intervalo de datas selecionado. Esse problema foi corrigido.
* Somente para usuários com a função Autor atribuída, os catálogos podem não aparecer. Esse problema foi corrigido.
* Quando um administrador de função personalizada baixa a transcrição do aluno, o relatório baixado não terá informações sobre os OAs que faziam parte apenas dos catálogos padrão. Esse problema foi corrigido.
* Pode ocorrer incompatibilidade no número total de usuários e na lista de usuários na página do grupo de usuários. Isso foi corrigido.
* A janela pop-up do programa de aprendizado pode não ser exibida mesmo quando ativada e os usuários podem ser redirecionados para a página do objeto de aprendizado. Esse problema foi corrigido.
* Quando a lista de espera é apagada e os alunos estão registrados em um curso, o administrador pode receber uma notificação por e-mail com seu nome em vez do nome do aluno que está sendo indicado. Esse problema foi corrigido.
* O Sobrenome pode não aparecer na interface do usuário para um usuário adicionado por meio da API de usuário do POST. Esse problema foi corrigido.

+++

+++Atualização 40

Atualização 40

Data de lançamento: setembro de 2018.

Aprimoramento do desempenho

* Os usuários podem enfrentar problemas de tempo limite ao fazer grandes conjuntos de transcrição do aluno. Esse problema foi corrigido.
* Os usuários podem sofrer atraso ao baixar grandes conjuntos de relatórios de inscrição nos quais está gravada a pontuação do questionário do aluno. Esse problema foi corrigido.
* Baixar grandes conjuntos de relatórios de pontuação do questionário pode levar mais tempo que o normal. Isso foi corrigido.
* Quando o aluno termina um programa de aprendizado, o formulário de comentários N1 pode não ser exibido automaticamente, mesmo quando a janela pop-up automática é ativada pelo Admin Console. Esse problema foi corrigido.
* Nos relatórios baixados de registro de auditoria do usuário e do conteúdo, as colunas modificadas pelo nome do usuário e pelo e-mail do usuário podem não ser registradas. O relatório mostra o sistema em tais instâncias. Isso foi atualizado para ser marcado como Desconhecido.

+++

+++Atualização 39

Data de lançamento: 19 de maio de 2018.

* Esta versão do Adobe Learning Manager traz novos recursos e aprimoramentos. Ele oferece a capacidade de criar funções personalizadas, adicionar rótulos de catálogo, limpar usuários, gerenciar tags, renomear objetos de aprendizado, integração de Slack, novas integrações de conector, suporte a xAPI e muito mais. Para obter mais informações sobre os novos recursos e aprimoramentos, consulte [Resumo dos novos recursos](../whats-new.md#main-pars_text).

* O Learning Manager está em conformidade com o GDPR. Para mais informações, consulte [Conformidade do Learning Manager com o GDPR](/help/migrated/kb/prime-gdpr.md).

## Problema conhecido {#knownissue}

* O hiperlink para o número de cursos e certificações dentro do modal de tags inclui cursos paralelos e certificações recorrentes. Ao clicar no hiperlink, estes cursos e certificações podem não ser listados, causando discrepância nos números.

+++

+++Atualização 38

* Os alunos nos estados Pendente ou Aguardando aceitação estavam sendo marcados como concluídos. Esse problema foi corrigido.
* Quando um professor pesquisa e seleciona todos os alunos, o número de alunos selecionados e a contagem mostrada têm disparidades. Esse problema foi corrigido.
* Quando você pesquisa e seleciona qualquer aluno e marca a participação, o Learning Manager pode marcar a participação de todos os alunos. Isso foi corrigido.
* O Learning Manager exibia o tempo em e-mails no formato de 24 horas. Esse problema foi corrigido. A hora é exibida agora no formato de 12 horas.
* Quando um gerente indica um aluno para um curso usando o botão disponível na página de notificações, a janela modal de indicação pode não ser carregada. Esse problema foi corrigido.
* Nos relatórios exportados do Excel, a data do prazo, que deve ser a data de inscrição + dias para concluir o valor definido na instância automática dos OAs, seria exibida incorretamente. Esse problema foi corrigido.

* Os resultados da pesquisa de usuários são exibidos vazios quando não há nenhum usuário no grupo pesquisado. Esse problema já foi corrigido.
* Os gerentes não podiam ser excluídos mesmo se não houvesse subordinados diretos. Esse problema foi corrigido. Os gerentes agora podem ser excluídos.
* A funcionalidade de redefinição do progresso do módulo podia parar de funcionar. Esse problema já foi corrigido.
* A certificação excluída pode aparecer no widget para alunos. Esse problema foi corrigido.
* O problema com o cálculo da eficácia do curso foi resolvido.

* O problema de integração de novas contas do Connect foi corrigido.
* O pop-up automático do Feedback N1 podia não ser exibido se estivesse ativado nas instâncias não padrão. O problema foi corrigido.
* O professor pode não ser capaz de marcar a participação de todos os usuários de uma só vez nas sessões que fazem parte do programa de aprendizado/certificação. Isso foi corrigido.

+++

+++Atualização 37

Data de lançamento: 25 de março de 2018

A versão de março de 2018 de Adobe Learning Manager traz novos recursos e aprimoramentos incríveis. Ele traz até você, geração de relatórios de trilha de auditoria de usuários e relatórios de logon/acesso, fornece aos alunos a capacidade de escolher instâncias do curso, aprimoramentos para salas de aula e salas de aula virtuais e muito mais. Esta versão também oferece a você correções de erros e aprimoramentos no desempenho.

Para ler tudo o que há de novo nesta versão, consulte [Novidades no Adobe Learning Manager](../whats-new.md).

### Problema conhecido {#KnownIssue-1}

**Problema:** acessar alguns objetos de aprendizado específicos que usam o Internet Explorer v11.1478.10586.0 pode travar o Learning Manager.

**Solução alternativa:** atualize o navegador Internet Explorer 11 para a versão mais recente entrando em contato com a equipe de TI da sua organização.

+++

+++Atualização 36

Data de lançamento: 22 de janeiro de 2018.

### Problemas corrigidos {#issuesfixed}

* Fazer qualquer alteração na configuração do modelo de e-mail pode fazer com que o banner de e-mail desapareça. Esse problema foi corrigido.
* Os alunos podem não conseguir adicionar/iniciar ajudas de tarefa privadas. Isso foi corrigido.
* Os grupos de usuários personalizados presentes em uma conta podem não estar listados no campo do grupo de usuários no modal de adicionar/editar relatório. Esse problema foi corrigido.
* Se uma imagem de medalha tiver espaço no nome, talvez ela não seja exibida para o aluno na página inicial.
* Quando um usuário registrado é excluído de um curso, o relatório do curso e o relatório do questionário podem não ser gerados para esse curso específico. Esse problema foi corrigido.
* Se o administrador muda o número de vagas indicadas de um gerente, o total pode parecer incorreto na solicitação de indicação quando aberto em locais diferentes. Esse problema foi corrigido.
* Ao converter um usuário externo em um usuário interno, o usuário pode não ser adicionado ao grupo Todos os alunos internos. Esse problema foi corrigido.
* Se pesquisar por um aluno individual, selecioná-lo e executar a ação de cancelar a inscrição, pode resultar em um cancelamento de inscrição de todos os alunos de tal grupo em vez de apenas o aluno selecionado. Esse problema foi corrigido.
* Como administrador, você pode não ser capaz de usar a caixa de verificação para selecionar um aluno dentro dos certificados. Esse problema foi corrigido.
* A criação e a atualização dos grupos de usuários com mais de 600 usuários individuais podem falhar. Esse problema foi corrigido. Agora você pode criar grupos de usuários com mais de 600 usuários individuais.
* Se excluir um grupo de usuários personalizado que faz parte de outro grupo de usuários personalizado, a regra de intersecção pode transferir o número de usuários para o grupo maior. Esse problema foi corrigido.
* Quando o catálogo padrão é desativado e um novo catálogo é criado, e se o gerente tiver acesso a esse catálogo recém-criado, ele pode não ser capaz de pesquisar qualquer curso sob esse catálogo. Esse problema foi corrigido.
* Os usuários de aplicativos móveis podem não receber feedback L1 como notificações por push. Esse problema foi corrigido.

+++

+++Atualização 35

Data de lançamento: 7 de janeiro de 2018.

Essa versão do Learning Manager traz as otimizações de desempenho voltadas para melhorar a estabilidade, o desempenho e a segurança.

### Aprimoramentos {#enhancements}

* Experimente pesquisas flexíveis ao pesquisar por cursos e usuários em todos os aplicativos. Isso inclui a pesquisa de cursos, usuários e grupo de usuários.
* Suporte ao uso do conector Box para integrar o Learning Manager aos sistemas externos a fim de automatizar a sincronização dos dados. Para obter mais informações, consulte o [conector Box](../integration-admin/feature-summary/connectors.md#main-pars_header_302653946).
* Especificações CSV atualizadas que você pode usar para mapear os dados existentes de migração do LMS. Use as especificações de csv para download mais recentes e os arquivos zip de csvs de amostra para entender o formato prescrito dos dados a serem inseridos. Para obter mais informações, consulte [Migração manual](../integration-admin/feature-summary/migration-manual.md).

+++

+++Atualização 34

### Problemas corrigidos {#IssuesFixed-1}

* Os comunicados podem falhar quando o número de usuários é alto. Esse problema foi corrigido.
* Acessar a conta do Learning Manager usando o URL de subdomínio na União Europeia poderia redirecionar os usuários para uma página diferente. Esse problema foi corrigido.
* Quando um LP é solicitado, um aluno pode consumir o LP somente na ordem especificada. Os alunos podiam realizar os cursos que não estavam listados primeiro usando os hiperlinks do curso. Esse problema foi corrigido. Os alunos não podem mais iniciar um curso até que ele termine o anterior.

* A mensagem de erro “Versão do navegador não suportada” pode não aparecer em versões não suportadas do Internet Explorer (IE 7, IE 8, IE 9 e IE 10) e do Safari (versão 7, 8 e 9). Esse problema foi corrigido.



+++

+++Atualização 33

Data de lançamento: 5 de outubro de 2017.

### Problemas corrigidos {#IssuesFixed-2}

* As alterações feitas em um curso compartilhado podem não ser propagadas para a conta compartilhada se o autor na conta de origem salvar automaticamente o curso. Esse problema foi corrigido.
* Às vezes, em projetos específicos do Learning Manager, o conteúdo costumava congelar no Fluidic Player. Esse problema foi corrigido.

* A listagem do calendário no widget Calendário do aprendizado no Painel do aluno podia aparecer em ordem aleatória. Esse problema foi corrigido. A listagem agora será exibida de forma ordenada.
* Ao marcar a participação usando a opção Selecionar todos, a presença dos alunos era marcada em todos os objetos de aprendizado da mesma sessão. Esse problema foi corrigido.
* Em certas telas de alta resolução, o e-mail recebido do Learning Manager tinha problemas de alinhamento e truncamento na imagem e no texto do banner. Esse problema foi corrigido.
* Certos e-mails do Learning Manager, como e-mails sem dados de notificação, não estavam sendo acionados para os usuários. Exemplo - Email recebido ao criar e ativar o perfil externo e Email recebido ao configurar a conta do Connect. Esse problema foi corrigido.
* Ao criar uma LP, definir um lembrete, inscrever usuários e, em seguida, alterar o prazo da instância, o prazo alterado pode não ser refletido nos lembretes. Isso foi corrigido. Os lembretes agora mostram o prazo alterado.
* Em certos casos, para o conteúdo criado usando o Adobe Presenter, o tempo total e o tempo decorrido no fluidic player não estavam em sincronia com o conteúdo. Esse problema foi corrigido.
* Em certos casos, depois de adicionar um programa de aprendizado a um catálogo, a opção de adicionar ainda podia estar ativada. Esse problema foi corrigido.
* Abrir o Learning Manager em um navegador do dispositivo exibe uma opção para experimentar o Learning Manager no aplicativo do dispositivo. Clicar em sim deve iniciar a Play Store (Android) se o aplicativo não estiver instalado ou iniciar o aplicativo se instalado (no Android e no iOS). Este fluxo de trabalho tinha problemas e foi corrigido.

+++

+++Atualização 32

Data de lançamento: 17 de agosto de 2017

### Problemas corrigidos {#IssuesFixed-3}

**Curso com várias versões de um módulo volta para a versão anterior na ação de exclusão.**

Quando um curso tem várias entradas de versão de um módulo em módulos específicos, ao excluir o módulo, ele podia voltar para a versão anterior e não ser totalmente excluído. Esse problema foi corrigido.

**As alterações feitas em um curso compartilhado podiam não ser propagadas se ele fosse salvo automaticamente ao mover-se pelas guias.**

As alterações feitas em um curso compartilhado podiam não ser propagadas para a conta inquilina se o autor na conta principal salvasse automaticamente o curso movendo para a guia seguinte. Esse problema foi corrigido.

**Os usuários não conseguiam alterar o prazo de conclusão das instâncias de um curso somente de atividade.**

Os usuários não conseguiam alterar o prazo de conclusão de uma instância em cursos de atividade visto que o prazo podia ser revertido para a data anterior. Esse problema foi corrigido.

**Impossibilidade de usar uma ID exclusiva depois de removida de um objeto de aprendizado.**

Ao atribuir uma ID exclusiva a um curso e removê-la, podia não ser possível usar a ID novamente. Esse problema foi corrigido.

**Um programa de aprendizado que já está registrado como parte de um evento de plano de aprendizagem pode aparecer como parte de outro evento no aplicativo do aluno.**

Se um programa de aprendizado já estivesse registrado como parte de um evento de plano de aprendizagem, ele podia aparecer como parte de outro evento no aplicativo do aluno. Esse problema foi corrigido.

**O aluno recebe e-mails de lembretes com data de conclusão/hora da sessão especificados incorretamente.**

Os alunos geralmente recebiam e-mails com lembretes de prazo incorretos/lembretes de tempo da sessão devido a correções de fuso horário. Esse problema foi corrigido.

**O cronograma do quadro de classificação da gamificação mostra alunos externos se forem convertidos de aluno externo em aluno interno.**

A linha do tempo do quadro de classificação de gamificação interna de um aluno pode mostrar um aluno externo quando ele é convertido de externo para um aluno interno. Esse problema foi corrigido.

**O campo UUID de um aluno é exibido no formato editável ao criar usuários únicos e CSV em uma conta habilitada para UUID.**

O campo UUID era exibido ao aluno ao completar seu perfil mesmo quando o administrador tinha fornecido o UUID para usuários únicos e CSV. Esse problema foi corrigido.

**O tempo de aprendizagem gasto não está sendo captado nos relatórios em alguns casos.**

Os dados do tempo de aprendizado gasto não estavam sendo exibidos nos relatórios de um aluno:

* Se a sua presença for marcada automaticamente pelo sistema para os módulos de conexão.
* Quando um código QR era digitalizado para os módulos CR e VC usando o aplicativo Learning Manager do dispositivo.

**Esta versão do Learning Manager também introduziu aprimoramentos e correções de erros relacionados ao reprodutor do dispositivo.**

* Problemas relacionados à conclusão dos módulos de atividade. Esse problema foi corrigido.
* Quando o aluno estava reproduzindo um vídeo no modo retrato, os botões +10 e -10 podiam não funcionar. Esse problema foi corrigido
* A experiência de reprodução de determinados projetos de amostra foi aprimorada quando reproduzidos em um dispositivo Android (móvel e tablet), visto que anteriormente podia ocorrer uma reprodução trêmula.
* Quando uma nova nota é adicionada, o painel de notas deveria fechar e a reprodução deveria continuar no reprodutor. Isso não pode ocorrer em alguns casos. Esse problema foi corrigido.
* Ao abrir as notas adicionadas a um módulo, o botão Fechar podia não ser exibido. Esse problema foi corrigido.
* Quando o estudante abre o painel ‘Notas’ usando o marcador de notas, pode ser necessário clicar duas vezes no ícone de notas para fechar o painel.
* Quando clicado no sumário, ele pode não ser recolhido automaticamente e precisa de fechamento manual para exibir o conteúdo. Esse problema foi corrigido.
* Um curso com um módulo em vários idiomas não podia exibir todos os idiomas disponíveis porque a barra de rolagem não se ampliava corretamente. Esse problema foi corrigido.
* Ao abrir um módulo de curso da atividade de terceiros em um reprodutor no modo paisagem, a orientação do texto podia na se ajustar, dificultando a navegação. Esse problema foi corrigido.
* A área de toque do botão Fechar do reprodutor foi aumentada nos modos on-line e off-line.
* O sumário não fecha automaticamente quando a orientação do dispositivo é alterada. Esse problema foi corrigido.
* Alguns problemas menores relacionados à interface do usuário, como o alinhamento do botão Play, do botão de opção e de outras configurações nos modos paisagem e retrato, foram corrigidos.

* O problema da barra de busca ser exibida mesmo quando a opção mostrar controle de reprodução está desmarcada no conteúdo foi corrigido.
* O botão Fechar do reprodutor não estava visível para determinados projetos quando a orientação do dispositivo era alterada. Esse problema foi corrigido.
* O problema relacionado à seção do índice do módulo que aparecia truncada no modo paisagem no reprodutor do dispositivo foi corrigido. Em alguns casos, o índice não era visível para o conteúdo no reprodutor do dispositivo. Isso também foi corrigido.

**Esta versão do Learning Manager também trouxe os aprimoramentos e correções listados abaixo para o aplicativo do dispositivo**.

* A notificação de envio relacionada aos prazos de conclusão podia não ser entregue em alguns dispositivos. Esse problema foi corrigido.
* Agora também oferecemos suporte ao ciclo de vida do objeto de aprendizado no aplicativo do dispositivo. Os alunos agora podem acessar o conteúdo mais recente nos objetos de aprendizado se tiverem sido editados pelo autor.

* Os problemas de orientação do aplicativo (incluindo a orientação padrão - modo retrato) Learning Manager foram corrigidos.
* Podia não haver uma opção para atualizar o conteúdo quando o usuário passava do modo off-line para o modo on-line.
* A ordenação do módulo agora é suportada nos cursos no aplicativo do dispositivo no modo on-line.

* Se um usuário não tiver baixado nenhuma ajuda de tarefa, clicar na guia Minhas ajudas de tarefa no modo offline poderá travar o aplicativo no IOS e mostrar uma mensagem dizendo erro ao carregar dados no Android. Isso foi resolvido.
* O aplicativo Learning Manager fechava ou exibia um erro se o curso fosse acessado imediatamente depois de desativar a Internet, mesmo se fosse um curso baixado. Esse problema já foi corrigido.
* Às vezes, quando você digitalizava o código QR, ele exibia uma imagem capturada da digitalização anterior do código QR. Isso foi corrigido.
* Tentar remover uma ajuda de tarefa que já foi adicionada da guia ajudas de tarefa em certas ocasiões mostraria uma mensagem de erro. Esse problema foi corrigido.

+++

+++Atualização 31

Data de lançamento: 16 de julho de 2017

### Aprimoramentos {#Enhancements-1}

**Gamificação**

Esta versão aumenta o escopo da gamificação. Os usuários externos agora podem participar da gamificação. Como administrador, você pode definir o escopo da gamificação alterando as configurações do escopo. É possível ativar de forma seletiva a gamificação entre usuários, grupos ou locais de perfil semelhantes.

**Aprimoramentos em usuários externos**

Com esse aprimoramento, é possível definir uma escala de tempo depois do qual os usuários são excluídos automaticamente após o período de inatividade. O aprimoramento também permite que o administrador adicione novamente o usuário como aluno externo no caso de alunos excluídos manual e automaticamente.

**Ajuda de tarefa, comunicados e relatório de cancelamento de inscrição** 

As ajudas de tarefa são um conteúdo de treinamento a que os alunos podem ter acesso sem ter de se inscrever em um objeto de aprendizado específico, como um curso ou programa de aprendizado. Com esse aprimoramento, os administradores podem extrair e baixar o relatório de ajudas de tarefa. Como administrador, você também pode gerar um relatório de todos os comunicados enviados por você. Os administradores e gerentes também podem extrair um relatório dos alunos cuja inscrição foi cancelada.

**Conectores do Learning Manager**

Agora é possível exportar habilidades do usuário para um local FTP para fazer a integração com qualquer sistema de terceiros usando a opção de exportação dos dados. Você pode especificar o Nome da conexão para sua integração e escolher se deseja importar usuários internos ou exportar habilidades do usuário configurando-os ou buscando-os sob demanda.

**Copiar instâncias do curso** 

Agora você pode copiar o URL da instância clicando na seta suspensa no canto superior direito de uma instância.

### Problemas corrigidos {#IssuesFixed-4}

**Usuários que não recebem convite do calendário ao ser inscrito no programa de aprendizado**

Os usuários às vezes não recebiam o arquivo (.ics) de convite do calendário quando se inscreviam em programas de aprendizado, certificados em sala de aula e sessões do Connect. Esse problema foi corrigido. Agora os usuários receberão os arquivos .ics como anexos informando os detalhes da sessão junto com o e-mail de inscrição.

**A descrição da atividade, mesmo se fornecida em vários idiomas, ainda podia ser exibida em inglês**

Um usuário cuja a preferência de idioma do conteúdo estava definida como um idioma diferente do inglês via, ainda assim, a descrição do módulo de atividade em inglês. Esse problema foi corrigido.

+++

+++Atualização 30

Data de lançamento: 30 de junho de 2017

### Aprimoramentos {#Enhancements-2}

**Os objetos de aprendizado múltiplos oferecem suporte ao plano de aprendizagem**

Como administrador ou autor, você pode atribuir vários objetos de aprendizado a um plano de aprendizagem. Se uma instância do objeto de aprendizado se aposentar ou se expirar, o plano de aprendizagem inteiro será desativado automaticamente. Com este melhoria, você também pode pesquisar nos campos **[!UICONTROL Aprendizados concluídos]** e **[!UICONTROL Aprendizados inscritos]** usando as IDs exclusivas de objetos de aprendizado.

**Acessibilidade**

Com esta atualização, o Learning Manager Learner Experience agora é compatível com o padrão de acessibilidade da seção 508. O Learning Manager também é compatível com a versão mais recente do **[!UICONTROL JAWS]**. Este recurso é compatível somente com o Aplicativo do aluno. Use o Internet Explorer 11, Windows Chrome ou Safari do MacOS para acessar esse recurso.

### Problemas corrigidos {#IssuesFixed-5}

**Informação incorreta em determinados fusos horários**

Os lembretes de prazo mencionavam o número de dias restantes incorretamente para os alunos em determinados fusos horários. Esse problema foi corrigido.

**Problemas do Programa de Aprendizado no caso de uma instância do Programa expirada**

O lançamento dos módulos do Programa de aprendizado apresentava problemas se a ocorrência do programa houvesse expirado. Isso levou à expansão do módulo não funcionar e alunos não puderam iniciar o player e visitar o conteúdo. Esse problema foi corrigido.

**Problemas de tradução no aplicativo do aluno**

Os usuários avançados do Learning Manager tiveram alguns problemas de tradução no aplicativo do aluno. Esses problemas foram corrigidos.

**Problemas relacionados à assinatura de uma habilidade**

Em alguns casos, os alunos não conseguiam assinar uma habilidade nova. Esse problema foi corrigido.

+++

+++Atualização 29

Data de lançamento: 9 de abril de 2017

### Novos recursos {#newfeatures}

Para obter uma lista dos novos recursos e aprimoramentos da versão de abril do Learning Manager, consulte [Novidades](../whats-new.md).

**Aplicativo para aluno baseado em widget**

Use widgets na página inicial para gerenciar cursos, habilidades e conquistas. Use a barra de pesquisa para realizar pesquisas em todo o LMS que inclui todos os objetos de aprendizado, catálogos, habilidades, notas e discussões

Para obter informações detalhadas sobre a nova página inicial, consulte [Página inicial do aluno no Learning Manager](../learners/feature-summary/getting-started-learner.md).

**Configurações do administrador para o painel do aluno**

Como administrador, você pode controlar a página inicial do aluno ativando e desativando diferentes widgets.

**Aplicativo móvel do Learning Manager para alunos**

O novo aplicativo móvel do Learning Manager permite que os alunos usem o aplicativo para se inscreverem e realizarem cursos. O aplicativo também pode ser usado para gerenciar painéis.

Para saber mais sobre a utilização do Learning Manager em dispositivos móveis, consulte [Aplicativo para alunos do Learning Manager para dispositivos móveis](../learners/feature-summary/ipad-android-tablet-users.md#main-pars_header_1451175907).

**Marcar presença usando o código QR**

Use o código de digitalização QR para marcar sua presença nas sessões de sala de aula usando dispositivos móveis.

**Função de professor**

Agora o Learning Manager inclui professores nos módulos. Os professores podem gerenciar as sessões do módulo incluindo a hora, o local e o limite de vagas dos módulos que são atribuídos a eles.

Para exibir informações detalhadas sobre os professores, consulte [Professores no Learning Manager](../instructors/feature-summary/getting-started.md#main-pars_header).

**Conta entre parceiros**

Se for administrador, você pode criar contas entre parceiros com os quais pode compartilhar suas licenças compradas.

Para saber como criar e gerenciar contas entre parceiros, consulte [Contas entre parceiros](../administrators/feature-summary/peer-account.md#main-pars_text).

**Solicitações de equivalência de curso**

Use a opção **[!UICONTROL Adicionar Novo Idioma]** ao adicionar um módulo ou curso para disponibilizá-lo em vários idiomas e formatos.

**Transcrição do aluno**

O Learning Manager oferece aos administradores e gerentes a capacidade de baixar os dados da transcrição para controlar o histórico de aprendizagem dos indivíduos e das equipes.

**Integração com outros provedores de conteúdo**

O Learning Manager introduziu três novos conectores nesta versão, para que os alunos possam acessar e realizar cursos dos seguintes provedores de conteúdo: Lynda.com, getAbstract e Harvard ManageMentor.

Para saber como configurar e usar cada um desses conectores, consulte [Conectores](../integration-admin/feature-summary/connectors.md#main-pars_header).

**ID exclusiva dos objetos de aprendizado**

Ao criar objetos de aprendizado, agora os autores e os administradores podem especificar IDs exclusivas para os cursos, programas de aprendizado ou certificações. Se desejar ativar a ID exclusiva ao criar um objeto de aprendizado, clique em Configurações > Geral. Selecione a caixa de seleção Ativar ao lado da opção IDs exclusivas do objeto de aprendizado.

**Quadro de discussão dos alunos**

Use o quadro de discussão dos cursos para interagir com colegas e professores. Como aluno, você pode exibir todas as postagens dos cursos. No entanto, pode excluir apenas as postagens que você publicou. Para obter mais informações sobre o Quadro de discussão, consulte [Exibindo e participando de discussões](../learners/feature-summary/courses.md#main-pars_header_1772461149).

### Aprimoramentos {#Enhancements-3}

**X de Y cursos**

Os critérios de conclusão dos objetos de aprendizado, como cursos, certificações e planos de aprendizado, podem ser configurados de forma que os alunos precisem concluir apenas X de Y módulos ou cursos. Os autores podem, da mesma forma, definir os critérios de conclusão das certificações e planos de aprendizagem.

Para obter mais informações sobre este recurso, consulte [Critérios de conclusão do curso](../learners/feature-summary/courses.md#main-pars_image_1164377098).

**Moderação do curso**

Os administradores agora recebem notificações sempre que um autor edita ou atualiza os módulos e republica um curso.

**Configurações de redefinição de módulos do administrador**

Agora, os administradores têm a capacidade de configurar a opção Redefinir módulo para permitir que os alunos redefinam um curso com falha ou incompleto.

**Catálogo do relatório**

Ao criar relatórios no Learning Manager, agora você pode gerar relatórios e gráficos dos catálogos.

**Aprimoramentos do plano de aprendizagem**

Agora, os administradores podem criar os planos de aprendizado dos tipos Dentro do prazo. No Plano de aprendizagem dentro do prazo, um administrador pode especificar o nome do evento, escolher a data do evento e selecionar o grupo de usuários ao qual o evento pertence.

**Mensagens de inscrição específicas aos curso**

Agora, os administradores podem configurar e enviar mensagens de inscrição específicas ao curso através de e-mail para os alunos.

**Comunicados pop-up**

Como administrador, agora você pode habilitar o recurso Pop-up para comunicados.

**Suporte a URL em comunicados**

Você pode adicionar URLs como comunicados adicionando o URL no HTML.

**Adicionar novos tipos de entrega (cursos)**

O Adobe Learning Manager agora permite adicionar tipos de entrega dos cursos.

**Aprimoramentos da função de autor**

Os autores anteriores só podiam criar módulos e tutoriais. Agora, os autores também têm a capacidade de criar as certificações e programas de aprendizado para alunos.

**Função de autor para usuários externos**

Como administrador, você pode atribuir funções de autor aos usuários externos.

**Vários autores**

O Learning Manager agora permite que vários autores editem simultaneamente o mesmo grupo de conteúdo.

**Aprimoramentos do Adobe Connect**

Agora você pode configurar um único URL do Adobe Connect com várias contas do Learning Manager.

**Suporte a novos idiomas**

Nessa versão, há suporte aos idiomas japonês, português do Brasil e italiano.



+++

+++Atualização 28

Data de lançamento: 30 de janeiro de 2017

### Problemas corrigidos {#IssuesFixed-6}

#### Configurações da conta {#accountsettings}

Como administrador, ao clicar em Perfil externo e escolher Ações > Alterar perfil, não eram listados todos os perfis. Esse problema já foi corrigido.

#### Ciclo de vida do curso {#courselifecycle}

* Ao iniciar um curso criado com a ferramenta de e-learning da biblioteca do Biz, a ação “Retomar” não funcionava. Esse problema foi corrigido.
* Alguns usuários não conseguiam iniciar um curso no iPad usando o link do curso nos comunicados. Esse problema já foi corrigido.
* Ao clicar no botão Continuar no programa do aluno, você não podia acessar os cursos na ordem. Esse problema já foi corrigido.
* O rótulo Visão geral do curso para os cursos no programa do aluno foi colocado anteriormente no lugar errado. Esse problema já foi corrigido.

#### Aplicativo do aluno {#learnerapp}

* Em seu dispositivo, se você abrisse a imagem de um comunicado no modo de tela cheia, não era possível voltar ao aplicativo. Agora esse problema foi corrigido.
* O conteúdo da Tincan carregado do Captivate não era reproduzido no modo on-line em sistemas operacionais Android e iOS. Esse problema foi corrigido.

#### Relatórios do curso {#coursereports}

São gerados relatórios incorretos de transcrição do aluno no Learning Manager quando o curso tem várias versões dos módulos. Esse problema já foi corrigido.

#### Camada da API {#apilayer}

Ocorria um erro sempre que você tentava obter as informações de versão do módulo usando AP/cursos/{coursesid}. Isso agora foi corrigido.

+++

+++Atualização 27

Data de lançamento: 23 de dezembro de 2016.

### Novos recursos {#Newfeatures-1}

A Adobe permite que as empresas migrem os dados de treinamento e o conteúdo do treinamento da sua organização dos seus sistemas de gerenciamento de aprendizagem (LMS) existentes para o aplicativo de LMS do Learning Manager.

O Learning Manager fornece as ferramentas e modelos necessários para que o administrador de integração da sua organização possa configurar e executar as tarefas de migração.

Para obter mais informações sobre o recurso Migração, consulte a [Ajuda manual sobre migração](../integration-admin/feature-summary/migration-manual.md)

### Aprimoramentos {#Enhancements-4}

**Registro do usuário**

Como administrador, você pode adicionar nomes de domínio específicos ao adicionar usuários externos. Quando os alunos se registram na conta, podem inserir endereços de e-mail apenas desses nomes de domínio.

Você também pode enviar links de verificação de e-mail para o e-mail dos usuários quando os usuários se registram na conta. Para obter mais informações sobre esse aprimoramento, consulte [Adicionar usuários/grupos de usuários](../administrators/feature-summary/add-users-user-groups.md#main-pars_header_1217981931).

**Fluidic Player**

O Fluidic Player permite agora que você altere a velocidade de reprodução. Você pode escolher cinco variantes de velocidade disponíveis. O Fluidic Player também permite que você controle as configurações de volume ao fazer um curso.

Como aluno, você também pode avançar ou retroceder 10 segundos usando os novos ícones nos dois lados do botão Reproduzir do Fluidic Player. Para obter mais informações sobre esses aprimoramentos, consulte [Fluidic Player](../learners/feature-summary/fluidic-player.md).

Os aprimoramentos do Fluidic Player se aplicam somente aos vídeos.

+++

+++Atualização 26

Data de lançamento: 06 de dezembro de 2016.

### Aprimoramento {#enhancement}

Como parte desta atualização, o Learning Manager fornece um ponto de extremidade [PATCH/usuários/{id}](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v1/#!/user/patch_users_id) para atualizar usuários em um aplicativo. Você pode acessar esse ponto final da API na função Administrador. Ao usar****este ponto final, você pode atualizar as seguintes informações dos usuários do Learning Manager:

* Nome
* Email
* Perfil
* Função
* Gerente

### Problema corrigido {#issuefixed}

**Fluidic Player**

Quando você consumia um curso desenvolvido em Captivate usando a variável `code cpQuizInfoStudentName`, o nome do aluno não aparecia conforme esperado. Esse problema foi corrigido.

+++

+++Atualização 25

Data de lançamento: 17 de novembro de 2016.

### Aprimoramentos {#Enhancements-5}

**Catálogos compartilhados**

O recurso Catálogo compartilhado permite que os administradores em todas as contas compartilhem ou adquiram Catálogos com objetos de aprendizado. Como extensão desse recurso de catálogo compartilhado, damos suporte à propagação das atualizações para os objetos de aprendizado, como Medalhas, Habilidades, Módulos, Cursos, Programas de aprendizado, Certificações e Ajudas de tarefa.

Para obter mais informações sobre este recurso, consulte a [Ajuda sobre catálogos compartilhados](../administrators/feature-summary/catalogs.md#propagation)

**Feedback N1 e N3**

* A caixa de diálogo do feedback N1 aparece assim que um aluno concluir a realização do curso. Além disso, o aluno recebe uma notificação sobre a conclusão do feedback N1.
* Uma opção para adicionar perguntas descritivas foi fornecida no recurso de feedback N1 e N3. Os administradores podem adicionar essas perguntas descritivas aos alunos. Essa condição está também no conjunto padrão de perguntas fornecidas pelo Learning Manager. Você pode adicionar duas perguntas descritivas do feedback N1 e uma pergunta descritiva do feedback N3.\
  Para obter mais informações sobre esse recurso, consulte Ajuda sobre as [Perguntas descritivas do feedback N1 e N3](../administrators/feature-summary/courses.md#descriptive)

**Exportar usuários**

* Com base na solicitação de alguns grandes usuários corporativos, foi fornecida uma nova opção de download da lista de todos os usuários da conta do Learning Manager. No logon do administrador, clique em **[!UICONTROL Usuários]** no painel esquerdo e clique em **[!UICONTROL Exportar dados do usuário]** para baixar a lista de usuários como uma planilha do Excel.

### Problemas corrigidos {#Issuesfixed-1}

**Inscrições no curso**

* Em alguns casos, quando um administrador tentava visualizar as inscrições do curso usando a guia dos alunos, alguns dos nomes dos alunos inscritos não eram exibidos. Esse problema foi corrigido.

**Adicionar cursos**

* Ao adicionar uma habilidade ao curso, se o autor adicionava uma habilidade que tivesse um espaço em branco no final do nome, ocorria um erro e o curso não era salvo. Esse problema foi corrigido.

**Realizar cursos**

* Em um curso solicitado, alguns alunos não conseguiam passar de um módulo para outro durante a realização do curso porque os módulos não eram marcados como concluídos. Esse problema foi corrigido.
* Em um curso solicitado, os alunos não conseguiam navegar entre os módulos dentro do sumário durante os modos normais e de revisão. Esse problema foi corrigido.

**Fluidic Player**

* Em alguns casos, quando um usuário carregava um conteúdo do módulo com quadros/slides ocultos, o sumário no painel esquerdo exibia os quadros/slides ocultos. Esse problema foi corrigido.

**Relatórios**

* O tempo necessário para carregar relatórios é maior na última atualização do Learning Manager. Esse problema foi corrigido.

+++

+++Atualização 24

Data de lançamento: 12 de outubro de 2016.

### Aprimoramentos {#Enhancements-6}

**Relatórios do curso**

* Nas contas do Learning Manager habilitadas para o identificador exclusivo universal (UUID), o UUID é exibido no relatório de inscrição do curso, nas transcrições do aluno e nos relatórios de pontuação do questionário.

### Problemas corrigidos {#Issuesfixed-2}

**Ajudas de tarefa**

* Em alguns casos, quando um aluno tentava navegar da guia Aprendizado>Ajudas de tarefa para Aprendizado>Cursos de aprendizado, os cursos não eram carregados conforme o esperado na guia Aprendizado>Cursos. Esse problema foi corrigido.

**Adicionar usuários**

* Em alguns casos, quando um único usuário era adicionado ao aplicativo Learning Manager, o usuário não recebia a notificação por e-mail. Esse problema foi corrigido.
* Os administradores não conseguiam fazer download do arquivo CSV se o processo de carregamento do CSV falhasse. Esse problema foi corrigido. Os administradores podem fazer download do CSV mais recente mesmo se o processo de carregamento do CSV falhar.
* Se um CSV fosse importado depois da modificação das informações do usuário que se registrou com letras maiúsculas e minúsculas misturadas, os detalhes do usuário inscrito não eram exibidos na interface do usuário do administrador. Esse problema foi corrigido.

**Relatórios do curso**

* Em alguns casos, as pontuações do questionário dos cursos não eram exibidas mesmo se as pontuações fossem exibidas nas transcrições do aluno. Esse problema foi corrigido.

**Relatórios de inscrição**

* Em alguns casos, os relatórios em Excel de inscrição do aluno não eram transferidos para os objetos de aprendizado. Esse problema ocorria sempre que caracteres especiais ou não ASCII eram utilizados no nome dos objetos de aprendizado. Esse problema foi corrigido.

**Logon do usuário**

* Ao configurar uma senha durante o registro ou durante a restauração, a mensagem de erro não era exibida mesmo se a senha inserida não estivesse de acordo com a política de senha. Esse problema foi corrigido.

**Eficácia do curso**

* Na função de aluno, a eficácia do curso era exibida como uma das opções de filtro **Classificar por** mesmo quando um administrador desativava a eficácia do curso para os alunos. Esse problema foi corrigido.

**Certificações**

* Quando um administrador removia alunos de uma certificação periódica, ocorria um erro e o aplicativo Learning Manager travava. Esse problema foi corrigido.

**Relatórios**

* Quando um administrador tenta gerar um relatório de certificação com **Data da caixa** como uma opção, os usuários inativos não são exibidos no relatório. Esse problema foi corrigido.
* Quando um administrador clicava no link Relatórios do curso na guia Relatórios>Meus relatórios, era exibida uma caixa de diálogo pop-up sem o botão Fechar. Esse problema foi corrigido.

**Fluidic Player**

* Ao visualizar cursos como administrador ou autor, quando um usuário escolhe o modo de Tela cheia no Fluidic Player, a tela aparece em branco. Esse problema foi corrigido.

**Suporte multilíngue**

* Eram exibidos caracteres de ponto de interrogação no lugar dos caracteres chineses em resposta às chamadas de API pelos usuários. Esse problema foi corrigido.

**Camada da API**

* Um erro costumava ocorrer sempre que um usuário tentava obter a ID de catálogo padrão usando a API get/catalog/catalog Id. Uma id de catálogo padrão pode ser semelhante a &#39;970_default&#39;. Esse problema foi corrigido.

**Interface do usuário**

* Alguns pequenos erros de digitação foram corrigidos na interface de usuário do aplicativo Learning Manager na função do aluno.

+++

+++Atualização 23

Data de lançamento: 19 de setembro de 2016.

### Problemas corrigidos {#Issuesfixed-3}

**Transcrições do aluno**

* Em alguns casos, se houvesse mais de vinte alunos inativos/excluídos em uma conta, os alunos inativos acima de vinte não eram exibidos na lista suspensa de pesquisa da caixa de diálogo de transcrição do aluno. Esse problema foi corrigido.
* Se uma conta de usuário externo estivesse vencida, os alunos não eram listados na transcrição gerada do aluno. Esse problema foi corrigido.

**Catálogos**

* Alguns dos clientes tinham problema com a exibição dos grupos de usuários em um catálogo. Mesmo se houvesse mais de vinte grupos de usuários em um catálogo, apenas 20 grupos de usuários eram exibidos. Nós corrigimos o problema exibindo 200 grupos de usuários em uma página.

+++

+++Atualização 22

Data de lançamento: 13 de setembro de 2016.

Nessa versão da atualização, corrigimos alguns dos problemas de backend da engenharia de produto para aprimorar a experiência do cliente.

### Problemas corrigidos {#Issuesfixed-4}

* Havia um problema com exportação dos dados do módulo nas transcrições do aluno resultando em dados de exportação inapropriados. Esse problema foi corrigido.
* Se um usuário usasse uma extensão de id do e-mail com mais de quatro caracteres, ela não era aceita. Por exemplo, se uma ID de email for <abcd@company.world>, ela não terá suporte, pois o universo da extensão tem mais de quatro caracteres. Corrigimos isso para oferecer suporte a extensões com mais de quatro caracteres.

+++

+++Atualização 21

Data de lançamento: 01 de setembro de 2016.

### Aprimoramentos {#Enhancements-7}

**Eficácia do curso**

Agora, os administradores podem personalizar o recurso de eficácia do curso ou do programa de aprendizado para ocultar a pontuação da eficácia da exibição dos alunos.

**Adicionar usuários externos**

O Learning Manager aumentou o limite máximo de registros externos a 5 dígitos.

**Relatórios**

Todos os relatórios e listas de alunos baixados de todos os objetos de aprendizado exibem usuários excluídos agora com delimitação clara dos usuários excluídos.

### Problemas corrigidos {#Issuesfixed-5}

**Ciclo de vida do curso**

Em alguns casos, quando um autor editava um curso compartilhado para atualizar informações alteradas do módulo, uma mensagem de aviso era exibida dizendo que o usuário não podia editar porque as alterações anteriores estavam sendo processadas. Esse problema foi corrigido.

**Suporte multilíngue**

Em alguns recursos da interface do usuário do Learning Manager, as mensagens não eram traduzidas e não eram exibidas ao usuário em frases no idioma apropriado. Esse problema foi corrigido.

**Adicionar usuários**

* Quando um usuário excluído era novamente adicionado como um único usuário, o usuário não era adicionado ao grupo de usuários ‘Todos os usuários’ por padrão. Esse problema foi corrigido.
* Um número limitado de perfis era exibido nas caixas de diálogo de alteração de perfil das inscrições externas e das autoinscrições. A paginação está agora implementada.

**Ajudas de tarefa**

Sempre que um aluno acessava a guia Ajudas de tarefa na conta do aluno, a mensagem de erro ‘Essa ajuda de tarefa não existe mais em sua lista&#39; era exibida antes de carregar o conteúdo. Esse problema foi corrigido.

**Catálogos**

Durante a criação do catálogo, ao adicionar cursos como conteúdo ao catálogo, o filtro Classificar por não funcionava conforme o esperado. Esse problema foi corrigido.

**Configurações**

Nas configurações da conta, quando um administrador usava um subdomínio que já era usado por outra conta, não era exibida uma mensagem de erro para o administrador. Esse problema foi corrigido.

**Camada da API**

* Quando a opção incluir gerente era usada ao pesquisar usuários, a hierarquia completa de gerentes era pesquisada em vez do gerente imediato do usuário. Esse problema foi corrigido.
* Quando um usuário com permissão de autorização do escopo do aluno tentava adicionar usuários, uma mensagem de erro genérica era exibida. Esse problema foi corrigido e agora uma mensagem de acesso não autorizado é exibida para o aluno.
* Quando um usuário tentava excluir o último usuário existente de um grupo de usuários, uma mensagem de erro 204 era exibida para o usuário. Esse problema foi corrigido exibindo uma mensagem de erro relevante para o usuário indicando que o grupo deve ter pelo menos um usuário.
* O espaço, se houvesse no início do nome, era cortado ao exibir o nome do usuário na API GET/users. Agora esse problema foi corrigido.
* Os cursos de rascunho também eram devolvidos em resposta quando o administrador tentava pesquisar todos os cursos. Esses cursos de rascunho deveriam ser privados para o autor. Esse problema foi corrigido e os cursos de rascunho agora não são devolvidos.

**Integração do Adobe Connect**

* Em algumas instâncias das sessões de sala de aula virtual com base no Adobe Connect, a presença não estava sendo marcada automaticamente após a sessão. Esse problema ocorria somente quando uma id de logon era usada pelo professor para fazer logon em vez da id de e-mail. Agora esse problema foi corrigido.
* Em alguns casos, o nome do professor era exibido várias vezes na lista suspensa Professor durante a criação do módulo da sala de aula virtual com base no Adobe Connect. Esse problema foi corrigido.

+++

+++Atualização 20

Data de lançamento: 22 de agosto de 2016.

### Aprimoramentos {#Enhancements-8}

**Camada da API**

Como parte da atualização, adicionamos as seguintes novas APIs para atender a alguns de nossos requisitos do cliente:

1. POST Users
1. DELETE Users
1. GET userGroups
1. GET userGroups /{id}
1. DELETE userGroups /{id}/Users
1. POST userGroups /{id}/Users
1. GET /users/userId/userGroups

Também aprimoramos o modelo de usuário existente com as seguintes adições:

1. O modelo do gerente é adicionado como relação ao modelo do usuário
1. O userGroupId é adicionado como um novo parâmetro ao GetUsers

**Transcrição do aluno**

Quando um usuário gerava a transcrição para um aluno, a caixa de diálogo pop-up era exibida por pouco tempo e desaparecia sem solicitar nenhuma ação do usuário. Melhoramos a experiência do usuário fornecendo uma pop-up que pausa e solicita que o usuário clique em OK.

**Integração do Adobe Connect**

A ID de logon é fornecida como um campo opcional novo nas configurações de integração do Adobe Connect para usuários que não usam sua id de e-mail para fazer logon.

### Problemas corrigidos {#Issuesfixed-6}

**Relatórios do curso**

* Quando um módulo do curso continha perguntas abertas ou somente perguntas de pesquisa, um relatório vazio da pontuação do questionário era exibido ao ser exportado. Esse problema foi corrigido.
* Em alguns casos, o relatório de pontuação do questionário não era baixado quando o usuário usava o link de pontuação do questionário da exportação. Esse problema foi corrigido.

**Criar cursos**

A página Configurações do curso na função Autor não era exibida quando uma habilidade associada a esse curso era retirada pelo administrador. Esse problema foi corrigido.

**Recrutador inteligente**

O campo de pesquisa não oferecia suporte a caracteres especiais como entrada e, consequentemente, os resultados da pesquisa não eram exibidos. Esse problema foi corrigido.

+++

+++Atualização 19

Data de lançamento: 11 de agosto de 2016.

### Aprimoramentos {#Enhancements-9}

**Recrutador inteligente**

O desempenho do mecanismo de pesquisa foi aprimorado para proporcionar resultados de pesquisa mais precisos aos usuários.

**Integração do Adobe Connect**

O processo de verificação/autenticação da solicitação de integração foi melhorado no aplicativo Learning Manager.

### Problemas corrigidos {#Issuesfixed-7}

**Adicionar usuários**

* Quando havia um grande número de usuários do Learning Manager, ocorria um atraso na página de carregamento dos usuários e dos grupos de usuários. Esse problema foi corrigido.
* Depois que o administrador finalizava o carregamento do arquivo CSV com novos usuários, a lista de usuários na página não era atualizada com os novos usuários até que a página fosse atualizada. Esse problema foi corrigido.
* Às vezes, após a importação de usuários que usam CSV, o valor da id do usuário na página era substituído pela id de e-mail. Esse problema foi corrigido.

**Criar grupos de usuários**

Em alguns casos, a contagem do usuário não era exibida na página de grupos de usuários padrão do Learning Manager. Esse problema foi corrigido.

**Transcrição do aluno**

Os valores de atributo dos campos ativos eram exibidos incorretamente nas transcrições do aluno em Certificações. Esse problema foi corrigido.

**Compartilhamento entre várias contas**

Em uma situação na qual o administrador de conta compartilhava o catálogo do curso com o destinatário e atualizava mais tarde os módulos de avaliação ou de trabalho prévio, o conteúdo dos módulos de avaliação e de trabalho prévio era reproduzido no módulo de conteúdo do destinatário. Esse problema foi corrigido.

**Temas e marcas**

Quando um administrador alterava um tema no aplicativo usando o widget de visualização ao vivo e alternava sua função, o widget de visualização ao vivo não funcionava conforme o esperado em uma nova função. Esse problema foi corrigido.

**Suporte multilíngue**

Quando um administrador alterava o idioma do aplicativo para chinês simplificado ou espanhol, parte do conteúdo do menu no painel esquerdo, as instruções on-line e as mensagens pop-up eram exibidas em palavras ou frases sem significado. Esse problema foi corrigido.

**Fluidic Player**

* Quando um autor criava um curso com o conteúdo AICC ou Tin Can e tentava visualizá-lo, o conteúdo não era reproduzido. Esse problema foi corrigido.
* A visualização do módulo não funcionava quando o autor criava ou editava um curso. Esse problema foi corrigido.

**Catálogos**

Quando um aluno tentava acessar o URL dos programas de aprendizado/catálogos diretamente no navegador, ele era redirecionado para os cursos. Esse problema foi corrigido.

**Integração ao Salesforce**

* Depois de definir uma conexão FTP ou Salesforce, na página Atributos do mapa, as setas suspensas dos campos não eram exibidas nos navegadores IE, Edge e Safari. Além disso, algumas das mensagens pop-up não eram exibidas nos fluxos de trabalho. Esse problema foi corrigido.
* Em alguns casos, quando um administrador tentava fazer a sincronização dos dados do .csv importados no conector FTP, a sincronização falhava com entradas replicadas. Esse problema foi corrigido.

**Camada da API**

* Quando um administrador autorizava o aluno externo usando a autenticação OAuth, às vezes, os alunos externos não podiam fazer logon no aplicativo. Esse problema foi corrigido.
* Às vezes, quando havia uma chamada de API das Ajudas de tarefa, o erro de acesso não autorizado era exibido. Esse problema foi corrigido.

**Configurações**

Na página das fontes de dados, quando um horário agendado automático era definido e salvo, às vezes, ele era revertido para o estado antigo. Esse problema foi corrigido.

**Relatórios de grupo de usuários**

Os valores do grupo de usuários no filtro não eram preenchidos quando o tipo de relatório era escolhido como personalizado. Esse problema foi corrigido.

**Integração do Adobe Connect**

Era exibido um título de cabeçalho incorreto da integração do Adobe Connect depois de concluir a conexão com êxito. O texto do cabeçalho da página foi corrigido.

**Relatórios**

Às vezes, mesmo se a opção “mostrar dados de valores atuais” estivesse selecionada, os dados mais recentes não eram mostrados nos relatórios. Esse problema foi corrigido.

+++

+++Atualização 18

Data de lançamento: 31 de julho de 2016.

## Novos recursos e melhorias {#newfeaturesandenhancements}

Para obter uma lista dos novos recursos e aprimoramentos da versão de julho do Learning Manager, consulte [Novidades](../whats-new.md).

Alguns dos recursos de aprimoramento estão listados abaixo para sua referência.

**Transcrição do aluno**

O Learning Manager fornece um recurso para gerar transcrições para os alunos do Learning Manager da sua organização. Para obter mais informações, consulte o [conteúdo de ajuda do recurso Transcrições do aluno](../administrators/feature-summary/learner-transcripts.md).

**Exportar medalha como PDF**

O Learning Manager permite que você exporte suas medalhas como arquivos PDF. Para obter mais informações, consulte o conteúdo do recurso [Medalhas](../administrators/feature-summary/badges.md).

**Pontuação no questionário dos módulos**

Você pode adicionar a pontuação do questionário nos módulos de sala de aula, sala de aula virtual e atividade.

**Adicionar usuários**

* Você pode mover alunos de um grupo de inscrição automática para outro grupo.
* Você pode mover usuários de um grupo externo para outro grupo externo.
* Você pode transformar um usuário do grupo externo em um Gerente do mesmo grupo externo.
* Depois de adicionar um grupo de usuários externo ao Learning Manager, você também pode pausar o processo de registro de usuários externos. A qualquer momento, você sempre pode revogar o bloqueio (pausa) escolhendo uma opção Retomar.
* Agora, você pode editar o nome e a id de e-mail dos alunos.

**Autoinscrição**

Os alunos também podem cancelar suas inscrições em objetos de aprendizado como curso, programa de aprendizado ou certificação. No entanto, o aluno não poderá cancelar sua inscrição em um objeto de aprendizado depois de concluí-lo.

**Realização dos objetos de aprendizado**

Agora, os administradores podem marcar como concluída uma atividade de aprendizado dos alunos.

**Relatórios**

* Você pode assinar relatórios de cursos, programas de aprendizado ou certificados. Você também pode assinar relatórios de curso individuais para obter dados como o status da pontuação do questionário e do aluno. As assinaturas serão enviadas à sua ID de e-mail conforme registrada na conta do Learning Manager. Você também pode alterar essa ID de e-mail.
* Quando você exporta o relatório de inscrição de certificação, uma nova coluna denominada **Data de vencimento** também é exportada. Esses dados da coluna permitem que os administradores conheçam os alunos que perderam os prazos de consumo do objeto de aprendizado.

**Modelos de e-mail**

Agora, você pode editar o cabeçalho dos modelos de e-mail.

+++

+++Atualização 17

Data de lançamento: 15 de junho de 2016.

### Problemas corrigidos {#Issuesfixed-8}

**Adicionar usuários**

Quando havia um grande número de usuários do Learning Manager, ocorria um atraso na página de carregamento dos usuários e dos grupos de usuários. Esse problema foi corrigido.

**Criar grupos de usuários**

Em alguns casos, a contagem do usuário não era exibida na página de grupos de usuários padrão do Learning Manager. Esse problema foi corrigido.

+++

+++Atualização 16

Data de lançamento: 10 de junho de 2016.

## Problema corrigido {#Issuefixed-1}

Alguns clientes tiveram problemas ao usar o recurso de logon único no Learning Manager. Esse problema foi corrigido ao fazer referência à entityId do Learning Manager para uma URL (<https://learningmanager.adobe.com>) em vez de uma palavra-chave. O Learning Manager está em conformidade com a especificação SAML 2.0.

+++

+++Atualização 15

Data de lançamento: 25 de maio de 2016

### Aprimoramentos {#Enhancements-10}

**Programas de aprendizado/certificações**

* Na lista de inscrição dos alunos nos programas de aprendizado e certificações, é exibido o nome completo (primeiro e último nomes). Anteriormente, somente o primeiro nome dos alunos era exibido.
* As habilidades com os níveis de créditos mais elevados são tomadas da lista de cursos nos programas de aprendizado/certificações e exibidas nos cartões como habilidades do programa de aprendizado/certificação. Se houver vários cursos com o mesmo valor de créditos, eles serão selecionados em ordem alfabética. Anteriormente, os nomes de habilidade dos programas de aprendizado/certificação eram retirados aleatoriamente de uma lista de cursos.

**Importar CSV**

No recurso de carregamento automático de CSV usando o FTP, os administradores recebem notificações por e-mail se houver alguma falha no carregamento do CSV.

**Adicionar parceiros externos**

Quando os alunos externos visitam a página de registro usando um URL de perfil externo, o nome do perfil externo é exibido na página de registro para uma melhor identificação.

### Problemas corrigidos {#Issuesfixed-9}

**Visualizar e publicar cursos**

* Na função de autor, ao visualizar um curso que foi carregado do Captivate como um conteúdo SCORM+SWF com a variável `code $$cpQuizInfoStudentName$$`, um valor nulo era exibido para a variável. Esse problema foi corrigido.
* Quando um curso do Presenter com um título que continha apóstrofo (&#39;) era publicado e exibido no Learning Manager, os pontos de interrogação (???) eram exibidos no sumário. Esse problema foi corrigido.

**Certificações**

* Se uma certificação está associada a um catálogo e quando a certificação se repete, ela aparece em todos os catálogos associados. Anteriormente, havia algumas poucas ocorrências nas quais os usuários não podiam ver as certificação periódicas em seus catálogos.
* Ao criar certificações, se um administrador inserir o valor de **dias para concluir**, que é maior ou igual ao período de validade da certificação, uma mensagem de aviso será exibida. Anteriormente, a mensagem de aviso não era exibida aos administradores.
* A **vigência** da certificação é exibida aos usuários em meses. Anteriormente, o valor base estava era exibido em anos.

**Definir programas de aprendizado**

O prazo não aparece nas instâncias do programa de aprendizado padrão. Anteriormente, era exibido um prazo predefinido, o que podia não ser relevante para os usuários.

**Criar cursos usando módulos**

* Quando um autor atualizava um módulo de um curso misto, a página de participação não era exibida na função de administrador. Esse problema foi corrigido.
* Quando o nome de uma instância do curso continha dois pontos (:), a ação de exportação da lista de alunos falhava. Esse problema foi corrigido.

+++

+++Atualização 14

Data de lançamento: 04 de maio de 2016

### Aprimoramentos {#Enhancements-11}

**Catálogos**

Quando um aluno acessa o catálogo, o foco padrão se alterna entre as guias com base na disponibilidade dos objetos de aprendizado, na seguinte ordem: 1. Cursos 2. Programas 3. Certificações e 4. Ajudas de tarefa. Por exemplo, se os cursos não estão disponíveis na guia Cursos de tal aluno, o foco alterna para o próximo objeto de aprendizado que é Programas se houver programas de aprendizado.

**Configurações da conta**

Uma opção de feedback é fornecida na caixa de diálogo de confirmação de desativação da conta quando um administrador opta por desativar uma conta.

### Problemas corrigidos {#Issuesfixed-10}

**Exportar relatórios**

* A exportação da lista dos alunos costumava falhar quando um grande conjunto de usuários estava inscrito em um programa de aprendizado. Esse problema foi corrigido.
* Quando um curso tinha duas instâncias com o mesmo nome e o nome da instância era longo, não eram criadas duas planilhas no arquivo Excel exportado. Esse problema foi corrigido.

**Inscrição em massa**

Quando um grande número de usuários estavam inscritos nos objetos de aprendizado, como programas de aprendizado, cursos, certificações, ajudas de tarefa e planos da aprendizado, a inscrição falhava. Esse problema foi corrigido.

+++

+++Atualização 13

Data de lançamento: 20 de abril de 2016

### Problemas corrigidos {#Issuesfixed-11}

**Criar cursos usando módulos**

Quando o conteúdo de um módulo com nome de arquivo longo era carregado, havia problemas com aparência dos botões. Além disso, as opções de carregamento e exclusão do módulo não funcionava conforme esperado. Esse problema foi corrigido.

**Importar CSV**

Conforme a solicitação dos clientes dos EUA, o tempo de carregamento automático de FTP CSV foi alterado da meia-noite do horário GTM para a meia-noite do horário PST.

**Exportar relatórios**

A exportação de dados de inscrição costumava falhar se um dos alunos inscritos era excluído após realizar o curso. Esse problema foi corrigido.

**Modelos de e-mail**

* A palavra **parceiros,** que foi usada para representar grupos externos,**** foi **** removida do corpo e do título dos modelos de email. Os grupos externos não são chamados necessariamente de parceiros.\
  **Observação:** este modelo atualizado não será exibido se o modelo padrão já estiver modificado. Para exibir o modelo atualizado, clique em **Reverter para Original** na caixa de diálogo **Visualização do Modelo**.

* A URL não pode ser clicada no email recebido pelos Administradores sempre que os modelos de email **Perfil Criado(Autorregistro)** e **Perfil Criado(Externo/Parceiros)** forem editados. Esse problema foi corrigido.

+++

+++Atualização 12

Data de lançamento: 07 de abril de 2016

### Aprimoramentos {#Enhancements-12}

**Ajudas de tarefa**

Criar ajudas de tarefa usando um URL. Você pode mencionar apenas um nome de URL no fluxo de trabalho da ajuda de tarefa e criar ajudas de tarefa se quiser usar qualquer conteúdo existente on-line como uma ajuda de tarefa.

**Adicionar alunos**

É permitida a edição de dados de um único usuário, como nome, e-mail, perfil e nome do gerente. Todos os grupos de usuários correspondentes são atualizados com os dados de usuário mais recentes.

**Exportar relatórios**

O nome do gerente, o nome do objeto de aprendizado e as colunas de valores não exclusivos definidas pelo usuário do CSV são adicionados à lista de alunos exportados dos objetos de aprendizado. Anteriormente, somente os dados básicos dos alunos, como nome, data, e-mail e status, eram exibidos.

**Adicionar parceiros externos**

O aplicativo Learning Manager não permite que os alunos externos entrem no aplicativo após a conta ter expirado. Os parceiros externos podem exibir o status da sua conta no aplicativo.

**Certificações**

Você pode renovar as certificações em termos de meses indicando o valor no campo **Vigência**. Anteriormente, a renovação da certificação era permitida apenas em termos de anos.

### Problemas corrigidos {#Issuesfixed-12}

**Comunicados**

No logon do administrador, a paginação não funcionava na página Comunicados. Esse problema foi corrigido.

**Planos e programas de aprendizado**

* Quando um aluno tentava pular o módulo de um curso ordenado em um programa de aprendizado, não era exibida nenhuma mensagem de erro. Esse problema já foi corrigido. Uma mensagem de erro **Não é possível ignorar módulos** aparece.
* Os cursos não eram adicionados aos programas de aprendizado quando a paginação era usada na lista de cursos. Esse problema foi corrigido.
* A guia **Retirado** foi exibida duas vezes em Programas de aprendizado > instâncias. Esse problema foi corrigido.

**Ajudas de tarefa**

* Quando um aluno removia a ajuda de tarefa da guia **Aprendizado**, a classificação por **Nome** não funcionava conforme o esperado até que a página fosse atualizada. Esse problema foi corrigido.

* Se uma ajuda de tarefa fizesse parte de vários cursos, os cursos não eram exibidos na lista de ajudas de tarefa. Esse problema foi corrigido.
* Se um aluno aumentava ou diminuía o zoom no navegador, a paginação da lista de ajudas de tarefa não funcionava conforme o esperado. Esse problema foi corrigido.

**Realização do curso**

* Se um aluno aumentava ou diminuía o zoom no navegador, a paginação dos cursos não funcionava conforme o esperado. Esse problema foi corrigido.

**Criar habilidades**

No logon dos alunos, a dica de ferramenta de nome de habilidade em **Mapa de habilidades **não exibia ****o nome completo****. Esse problema foi corrigido.

**Adicionar parceiros externos**

* Uma mensagem de texto foi incluída na página de registro de usuários externos como **Os usuários devem primeiro se registrar e criar uma senha do nome de usuário para logons subsequentes**.

**Notificações do usuário**

* Quando um aluno externo clica no link **Abrir notas** na notificação por email sobre o curso novamente visitado, o reprodutor abre, mas o painel de notas não estava funcionando. Esse problema foi corrigido.
* Quando um aluno externo tentava abrir os módulos de pré-trabalho ou de teste usando o link **Abrir Notas** na notificação por e-mail da revisita do curso, o conteúdo das notas não estava visível. Esse problema foi corrigido.

**Criar cursos usando módulos**

Quando um administrador tentava inscrever alunos em um curso misto que continha um módulo expirado de sala de classe, a caixa de diálogo de inscrição não abria. Esse problema foi corrigido.

**Exportar relatórios**

Se um texto de pergunta contiver mais de 255 caracteres e estiver habilitado para o formato SCORM 1.2, o relatório do quiz dessas perguntas não funcionará. Esse problema foi corrigido.

+++

+++Atualização 11

Data de lançamento: 15 de março de 2016

### Problemas corrigidos {#Issuesfixed-13}

**Criar cursos com módulos**

* No logon do administrador, ao tentar criar uma nova instância para cursos da guia **Retirado** ocorria um erro. Esse problema foi corrigido.
* No logon de administrador do conteúdo localizado, durante a inscrição de alunos em uma instância do curso, os layouts das ações e da tela de inscrição ficavam distorcidos. Esse problema foi corrigido.
* Quando um autor estava criando módulos de sala de aula ou de sala de aula virtual, o mês padrão do calendário era exibido como janeiro de 2015. Esse problema foi corrigido para refletir a data atual por padrão.
* Quando um nome da instância de um curso continha barra inclinada ou barra invertida, a ação de exportação da lista dos alunos falhava. Esse problema foi corrigido.

**Comunicados**

Quando um aluno passava o mouse sobre um comunicado em vídeo, o cursor não se alterava para a forma de mão com o indicador esticado conforme o esperado. Esse problema foi corrigido.

**Notificações do usuário**

Quando um aluno externo clica no link **Abrir Notas** na notificação por e-mail de nova visita ao curso, ele não funcionava. Esse problema já foi corrigido. Este link abre o reprodutor com notas, mesmo quando o usuário não estiver conectado no Learning Manager.

**Suporte aos idiomas francês e alemão**

Os URLs da ajuda no recurso de carregamento do CSV passavam para o conteúdo da ajuda em inglês. Esse problema foi corrigido.

**Visualizar e publicar cursos**

No logon do autor, ao visualizar o conteúdo da TinCan API do Presenter 10 e 11 (SWF/HTML), o conteúdo não funcionava. Esse problema foi corrigido.

**E-mails personalizáveis**

Os nomes de título em modelos de e-mail não eram apropriados. O conteúdo é atualizado nesses títulos de modelo para torná-los legíveis.

**Ajudas de tarefa**

No navegador Internet Explorer 11, o nome e o ícone da ajuda de tarefa eram exibidos distorcidos na visualização do autor e do administrador. Esse problema foi corrigido.

+++

+++Atualização 10

Data de lançamento: 28 de fevereiro de 2016.

## Novos recursos {#Newfeatures-2}

### Ajudas de tarefa

Ajudas de tarefa é um repositório de conteúdo de treinamento acessível aos alunos sem critérios de inscrição ou conclusão. Os alunos podem consultar essas ajudas de tarefa para obter assistência na execução de qualquer atividade ou tarefa em uma empresa. O administrador pode controlar o número de downloads por ajuda de tarefa.

Para obter mais informações sobre este recurso, consulte a [Ajuda de ajudas de tarefa](../learners/feature-summary/job-aids.md).

### Comunicados

Um comunicado é uma mensagem multimídia (texto, imagem ou vídeo) que um administrador pode elaborar e transmitir para um conjunto definido de usuários. Use os comunicados para motivar alunos a realizarem treinamentos e, assim, criar para uma cultura de aprendizado.

Para obter mais informações sobre este recurso, consulte a [Ajuda de comunicados](../learners/feature-summary/announcements.md).

### Suporte à Tin Can API

O Adobe Learning Manager oferece suporte à especificação Tin Can API (também conhecida como Experience API ou xAPI). Você pode carregar e controlar o conteúdo compatível com a Tin Can API assim como controlar o conteúdo do SCORM e AICC.

Para obter mais informações, entre em contato com a equipe de suporte da Adobe.

### Sequência do curso

Você pode criar um caminho de aprendizagem atribuindo automaticamente um curso de seguimento ou qualquer atividade de aprendizagem.

Os eventos de planos de aprendizado foram atualizados. Foram adicionados um par de novos eventos. Consulte [Planos de aprendizado](../learners/feature-summary/learning-programs.md) para obter mais informações.

### Lembrete de notas

Se tomar notas durante um curso, o Learning Manager envia um lembrete após 15 dias com uma notificação para você revisar as notas.

### Gamificação do nível de grupo

Os administradores podem definir o escopo da gamificação alterando as configurações do escopo. É possível ativar de forma seletiva a gamificação entre usuários, grupos ou locais de perfil semelhantes. Consulte o recurso [Gamificação](../learners/feature-summary/gamification.md) para obter mais informações.

### Suporte aos idiomas francês e alemão

O aplicativo Learning Manager está disponível em francês e alemão. Você pode personalizar o idioma do feedback, das fases do curso e da comunicação.

### Aprimoramentos {#Enhancements-13}

Há aprimoramentos significativos nos recursos existentes do Learning Manager. Alguns dos aprimoramentos predominantes são os seguintes:

### Importar CSV

Se você excluir usuários, não poderá adicionar os mesmos usuários de volta ao aplicativo usando a adição do único usuário. No entanto, você pode adicionar o usuário excluído novamente usando o processo de carregamento de CSV. Há alterações significativas na restrição dos campos obrigatórios no recurso de carregamento de CSV. Consulte [Perguntas frequentes sobre CSV](../administrators/add-users-in-bulk.md) para obter mais informações.

### Exibição da lista de cursos

Por padrão, você pode ver os cursos como cartões. Uma exibição em lista foi introduzida nesta versão. Você pode clicar no ícone da barra tripla ao lado do campo de pesquisa para alterar a exibição.

### Excluir cursos

Agora você pode excluir cursos nas fases de rascunho e retirado. Consulte o recurso [Cursos](../administrators/feature-summary/courses.md) para mais informações. Se um objeto de aprendizado for excluído, todos os seus dados de relatório também serão excluídos. Se um curso for excluído e se fizer parte de qualquer outro objeto de aprendizado, uma mensagem apropriada aparecerá para o usuário.

**Planos e programas de aprendizado**

Você pode impor a ordem em que os alunos podem realizar os cursos dentro dos programas de aprendizado. É possível excluir programas de aprendizado nos estágios de rascunho e retirado. Se um objeto de aprendizado for excluído, todos os seus dados de relatório também serão excluídos.

**Certificações**

Você pode excluir certificações nos estágios de rascunho e retirado. Se um objeto de aprendizado for excluído, todos os seus dados de relatório também serão excluídos.

**Classificação da eficácia do curso**

No logon do administrador, você pode exportar dados do feedback N1 e N3 de qualquer curso.

**Criar cursos com módulos**

Você pode impor que os alunos façam cursos de pré-requisito antes de realizarem os cursos.

**Notificações do usuário**

Os alunos obtêm notificações sempre que se inscreverem em um programa de aprendizado.

**Módulos de sala de aula (ILT)**

É possível criar cursos em salas de aula em uma data anterior. Esse recurso permite que os administradores da empresa alimentem as informações de cursos em salas de aula mais antigos no Learning Manager e gerem relatórios.

**Exportar relatórios**

Os relatórios dos alunos foram aprimorados. É possível visualizar nome, e-mail, status do objeto de aprendizado, critérios de inscrição, data de inscrição, data de conclusão e data de início no relatório.

**Adicionar parceiros externos**

Depois de ter inscrito os alunos externos na conta do Learning Manager, você também pode reduzir número de alunos, se necessário. No entanto, não é possível reduzir o número de alunos além do número de vagas usadas. Como solução, você pode excluir os alunos inscritos primeiro e, depois, fazer novamente as inscrições com o número necessário de vagas.

### Problemas corrigidos {#Issuesfixed-14}

**Presença dos alunos**

Folha de presença na exibição do administrador exibe o nome completo do funcionário se estiver disponível. Anteriormente, somente o primeiro nome dos alunos era exibido.

**Planos e programas de aprendizado**

Todos os cursos dos programas de aprendizado são exibidos na ordem esperada. Anteriormente, havia problemas na ordenação dos cursos nos programas de aprendizado. Esse problema foi corrigido.

**Adicionar alunos**

Se um usuário já registrado tenta se registrar novamente usando o processo de autorregistro, uma mensagem apropriada é exibida. O formato e o conteúdo da mensagem foram corrigidos.

**Relatórios**

Para que o conteúdo identifique o tempo gasto pelo usuário no consumo de conteúdo, é possível identificá-lo usando uma variável, `code cmi.core.session_time`. A variável não estava definida anteriormente. Esse problema foi corrigido.

**Criar cursos com módulos**

Sempre que um módulo de curso existente é sobrescrito por outro módulo, uma nova versão dele é gerada. Se o questionário deste novo módulo fosse exportado, ocorria uma exceção e o relatório do questionário não era gerado. Esse problema já foi corrigido.

**Modelos de e-mail**

Os erros ortográficos nos modelos de e-mail foram corrigidos.

+++

+++Atualização 9

Data de lançamento: 09 de fevereiro de 2016.

## Comportamento atualizado da ação Fazer logoff {#signoutbehaviorupdated}

Quando os usuários clicam em **[!UICONTROL Sair]** no Learning Manager, agora eles saem do aplicativo Learning Manager e também se desconectam das suas IDs de Adobe.

+++

+++Atualização 8

Data de lançamento: 20 de janeiro de 2016.

### Aprimoramentos {#Enhancements-14}

**E-mails personalizáveis**

* Os usuários podem modificar a seção de rodapé dos modelos de e-mail. Você pode personalizar o rodapé de um modelo de e-mail com o texto de sua preferência. O rodapé personalizado é aplicado automaticamente a todos os tipos de modelos de e-mail.

**Realização do curso**

* Os objetos de recurso no modo de visualização de um curso são listados um após o outro em uma nova linha. Anteriormente, havia casos em que os recursos de um curso eram exibidos próximos um do outro em uma única linha.

**Link direto aos objetos de aprendizado**

* Você pode acessar os objetos de aprendizado (exceto a certificação) usando um URL direto. A opção **[!UICONTROL Copiar URL]** é exibida nos blocos de objetos de aprendizado. Os usuários podem clicar em **[!UICONTROL Copiar URL]** e colar o link em uma página separada do navegador para acessar diretamente o objeto de aprendizado.

**Criar cursos usando módulos**

* Ao criar um curso, os autores podem organizar cursos de pré-requisito em qualquer ordem. Anteriormente, essa opção não estava disponível no Learning Manager.

* Os autores podem adicionar ou excluir cursos de pré-requisito em cursos publicados. Anteriormente, este recurso estava disponível somente para cursos de rascunho.

**Registro do usuário**

* Os usuários podem fazer logon no Learning Manager sem nenhuma verificação adicional do URL se a sua ID da Adobe corresponder à ID de e-mail do Learning Manager. Ao adicionar usuários à conta, o administrador de uma empresa fornece a ID de e-mail do Learning Manager.

**Criar catálogo**

* Na função Administrador, ao criar catálogos usando a caixa de diálogo **Adicionar objetos de aprendizado**, os cursos retirados não eram exibidos na lista de cursos.

**Outras correções**

* Na função Administrador, o nome completo dos alunos é exibido na guia **Alunos**. Anteriormente, somente o primeiro nome dos alunos era exibido.

+++

+++Atualização 7

Data de lançamento: 13 de janeiro de 2016.

### Problemas corrigidos {#Issuesfixed-15}

**Realização do curso**

* Ao acessar conteúdo do curso, a barra de reprodução do conteúdo sempre aparece na tela. Havia um problema anterior com a barra de reprodução do conteúdo viso que ela desaparecia da tela de forma intermitente.
* Ao acessar o conteúdo do curso, se o conteúdo tiver uma caixa de diálogo pop-up que solicita aos usuários que confirmem se desejam realmente sair ou permanecer na página, ao optar por permanecer nessa caixa de diálogo, o usuário volta ao conteúdo. Em algumas situações, ao clicar no botão Permanecer, o usuário era levado para fora do conteúdo do curso.

**Outras correções**

* Alguns problemas relacionados à reprodução de conteúdo foram resolvidos.

+++

+++Atualização 6

Data de lançamento: 22 de dezembro de 2015

### Aprimoramentos {#Enhancements-15}

**Painel pessoal**

* Ao acessar cursos, catálogos e programas de aprendizado nas funções Administrador e Autor, a ordem das guias foi alterada para **Publicado - Rascunho - Todos - Retirado**. A seleção padrão é **Publicada.**

### Problemas corrigidos {#Issuesfixed-16}

**Realização do curso**

* Na função do aluno, ao consumir um curso, se o reprodutor for fechado com o botão Voltar do navegador ou com a tecla Backspace do teclado, o tempo de aprendizado gasto no curso é capturado nos relatórios. Em algumas situações, ocorria um problema no qual essa duração não era registrada nos relatórios.

**Registro do usuário**

* Se um usuário registra uma conta do Learning Manager usando autorregistro habilitado para SSO, o nome do usuário aparece corretamente na lista de nomes nos registros. Em alguns casos, o nome de usuário não era exibido corretamente.

**Criar cursos usando módulos**

* Quando um autor duplica um curso, os arquivos de recurso do curso duplicado podem ser removidos ou atualizados. Em alguns casos, os usuários tinham problema ao atualizar ou remover recursos dos cursos duplicados.

**Criar catálogos personalizados para grupo de usuários**

* Ao usar a caixa de diálogo **Adicionar objetos de aprendizado** na função Administrador, você pode filtrar cursos, escolher um curso e adicionar usando o botão **Adicionar** na parte inferior da caixa de diálogo. Em alguns casos, o botão **Adicionar** não estava aparecendo para alguns usuários.

+++

+++Atualização 5

Data de lançamento: 11 de dezembro de 2015

### Problemas corrigidos {#Issuesfixed-17}

**Logon do usuário**

* Quando um usuário tentava entrar no aplicativo Learning Manager sem usar o link de ativação, a mensagem de erro era exibida no formato errado. Esse problema foi corrigido.

**Aplicativo para tablets**

* Após instalar o Learning Manager em tablets Android ou iPhone, as mensagens de compatibilidade com o navegador não eram exibidas. Anteriormente, uma mensagem de compatibilidade com o navegador era exibida para os usuários. Esse problema foi corrigido.

+++

+++Atualização 4

Data de lançamento: 09 de dezembro de 2015

### Aprimoramentos {#Enhancements-16}

**Adicionar usuários**

* Na função Administrador, quando o administrador registra usuários ou termina a adição de um único usuário, uma mensagem é exibida indicando a conclusão bem-sucedida do fluxo de trabalho junto com as próximas etapas a seguir.
* Quando um usuário tenta entrar no aplicativo Learning Manager diretamente sem usar o link de ativação do usuário, é exibida uma mensagem de erro solicitando que o usuário use o link de ativação.

**Navegadores suportados**

* Se algum usuário acessa o aplicativo Learning Manager em navegadores não suportados, ele recebe um alerta com a lista branca de navegadores.

### Problemas corrigidos {#Issuesfixed-18}

**Relatórios**

* Na função Administrador ou Gerente, ao criar um relatório com o eixo secundário como tempo de aprendizado gasto, aplicar o filtro Gerente e salvar o relatório, o usuário não conseguia fazer download desses relatórios. É possível fazer download de todos os tipos de relatórios.

**Adicionar usuários**

* Havia alguns erros de digitação na mensagem de alerta exibida ao ativar alunos externos na função Administrador. O problema foi corrigido.
* Na função Administrador, uma mensagem de erro apropriada é exibida quando o campo Gerente não estiver selecionado durante a adição de um único usuário.

**Registro do usuário**

* O e-mail de boas-vindas recebido pelos novos usuários realça a importância vincular a ID da Adobe à ID do Learning Manager para que o logon seja bem sucedido.

**E-mails personalizáveis**

* Ao adicionar vários alunos aos cursos em salas de aula que têm sessões como anexos, alguns alunos não recebiam notificações por e-mail. Esse problema foi corrigido.
* Os e-mails enviados aos alunos em relação às inscrições em objetos de aprendizado e outros eventos contêm o nome específico do objeto de aprendizado no assunto do e-mail.

**Outras correções**

* Os problemas relacionados aos links de URL nos modelos de e-mail foram corrigidos.
* O suporte fornecido a

   * Publish para Learning Manager
   * Suporte ao carregamento mais rápido de conteúdo para a versão CP 8 (a correção CP803 é necessária)

+++

+++Atualização 3

Data de lançamento: 26 de outubro de 2015.

### Aprimoramentos {#Enhancements-17}

**Adicionar usuários**

* Link da ajuda on-line, fornecido na caixa de diálogo Adicionar usuários > Carregamento de CSV, para que os usuários entendam melhor como carregar o arquivo CSV.

**Fluidic Player**

* Ao carregar o conteúdo do curso do Captivate com mais de 500 MB, o conteúdo não era reproduzido no Fluidic Player. Essa restrição foi removida. Atualmente, o limite de tamanho foi alterado para 2 GB.

**Faturamento**

* Na função Administrador, quando um usuário insere o número de alunos e clica em **Fazer pedido**, é exibida uma caixa de diálogo com detalhes sobre as cobranças de assinaturas mensais e anuais por usuário.

### Problemas corrigidos {#Issuesfixed-19}

**Criar cursos usando módulos**

* Ao criar cursos com módulos de atividades, os autores podem escolher URLs externos válidos mesmo que contenham caminhos de pasta no URL. Anteriormente, os URLs com caminhos de pasta não eram suportados. Esse problema foi corrigido.
* Se o conteúdo do curso fosse um projeto carregado com um arquivo zip no Learning Manager e se esse arquivo zip contivesse os caminhos de pasta, como Zip>pasta>conteúdo, esse tipo de conteúdo não era suportado. Esse problema foi corrigido.

**Aplicativo para tablets**

* Quando um usuário tentava baixar os arquivos de recurso de um curso no aplicativo Learning Manager para Android, os arquivos de recurso não podiam ser baixados. Esse problema foi corrigido.
* Ao realizar um curso usando o Fluidic Player, quando um usuário gravava a nota e tentava baixá-la mais tarde do curso, ela não estava disponível para download. Esse problema foi corrigido.

+++

+++Atualização 2

Data de lançamento: 28 de setembro de 2015

### Aprimoramentos {#Enhancements-18}

**Criar cursos usando módulos**

* O aplicativo Learning Manager oferece suporte ao carregamento de conteúdo SCORM mesmo se a versão não for indicada no arquivo manifest.xml. Por padrão, a versão é considerada como 1.2.
* Ao carregar o conteúdo do curso do Captivate com mais de 500 MB, o conteúdo não era reproduzido no Fluidic Player. Como parte da atualização 2, o limite de tamanho foi alterado para 800 MB.

**Faturamento**

* Na função Administrador, ao adquirir uma assinatura usando o cartão de crédito, o usuário poderá optar por fazer o primeiro pedido com 10 alunos. Os alunos mínimos necessários para o primeiro pedido diminuiu de 100 para 10.

**Registro do usuário**

* Um link de URL para criar a ID da Adobe foi fornecido no e-mail de boas-vindas recebido pelos alunos depois do registro.

**Adicionar usuários**

* Na função Administrador, a adição de usuários usando a opção de carregamento de CSV diretamente na conta de Exavault não funcionava para alguns clientes. Esse problema foi corrigido.

### Problemas corrigidos {#Issuesfixed-20}

**Planos e programas de aprendizado**

* Os alunos podem ser inscritos automaticamente no mesmo programa de aprendizado como parte de vários planos de aprendizado. Anteriormente, havia algumas exceções nesse fluxo de trabalho. Esse problema foi corrigido.

**Exibir quadro de classificação e medalhas**

* Na função do aluno, depois de realizar um curso que continha uma medalha, a imagem da medalha não era exibida no mapa de medalhas do painel do aluno nem no arquivo baixado. Esse problema foi corrigido.

**Aplicativo para tablets**

* Uma janela pop-up é exibida para indicar a disponibilidade do aplicativo do aluno quando o URL do aplicativo do aluno está aberto em navegador de dispositivos Android.

**Outras correções**

* Foi resolvido um problema com a criação de uma conta de usuário devido ao suporte líquido de armazenamento do Akamai.
* Foi resolvido um problema relacionado ao carregamento de conteúdo SCORM 1.2 que contém um arquivo zip com várias pastas.

+++
