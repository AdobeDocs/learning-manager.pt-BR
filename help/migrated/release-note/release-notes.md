---
description: Saiba mais sobre os novos recursos e aprimoramentos no Adobe Learning Manager
jcr-language: en_us
title: Resumo dos novos recursos
contentowner: jayakarr
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '26196'
ht-degree: 0%

---



# Resumo dos novos recursos

<!--<table>
 <tbody>
  <tr>
   <td><img src="assets/cp-prime-appicon-88x84.png"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> was launched in August 2015. As part of our continuous improvement efforts to enhance the product, we have been rolling out regular updates. Read on to know the features enhanced/issues fixed in update releases.<br></p></td>
  </tr>
 </tbody>
</table>-->

+++Atualização 95: versão de novembro de 2023 do Adobe Learning Manager

**Data de lançamento:** 18 de novembro de 2023

## Novidades desta versão

Exibir [Novidades do Adobe Learning Manager](/help/migrated/whats-new.md) para obter mais informações.
+++

+++Atualização 94

**Data de lançamento:** 23 de agosto de 2023

## Novidades desta atualização

* Selecione o ícone de engrenagem do reprodutor para alterar a qualidade do vídeo.
* Alterar a qualidade e a velocidade de um vídeo nas redes sociais.
+++

+++Atualização 93: a versão de julho de 2023 do Adobe Learning Manager

**Data de lançamento:** 10 de julho de 2023

Novidades desta versão

### Recommendations aprimorado

O Adobe Learning Manager introduziu um novo e renovado sistema de recomendação para cursos. Esse recurso de recomendações usa algoritmos de IA e interesses de usuários, como produtos, funções e níveis, para fornecer recomendações de conteúdo personalizadas.

### Várias Inscrições

Nesta versão do Adobe Learning Manager, estamos introduzindo a multiinscrição para alunos que permite que eles se inscrevam em mais de uma instância de um curso em um ou diferentes períodos de tempo.

### Descontinuação Do Conector Exavault

Esta versão do Adobe Learning Manager incluirá um novo conector, que usará o protocolo SFTP da família AWS Transfer.

Para obter mais informações, consulte [Novidades do lançamento do Adobe Learning Manager em julho de 2023](/help/migrated/whats-new-2023-july.md).
+++

+++Atualização: 92

**Data de lançamento:** 23 de junho de 2023

**Erros corrigidos nesta atualização**

* Depois de concluir um módulo, a API Grade não é acionada automaticamente, o que resulta na exibição da marca de seleção verde como esperado na Interface do usuário.
* Depois de concluir alguns módulos em um caminho de aprendizado ou uma certificação, a marca de seleção verde, que indica a conclusão bem-sucedida, não é exibida conforme esperado.
* O Adobe Learning Manager não é iniciado como esperado após o upload de um CSV de usuário com campos incorretos.
* O pop-up de aviso sobre como entrar em contato com o administrador também exibe outros endereços de email.
* Todas as medalhas obtidas por um aluno não são exibidas na resposta.
* Durante o registro do usuário, um nome de usuário com &quot; &quot; deve ser aceito.

#### Reprodutor

* Adicionar um menu para selecionar a resolução da tela ao reproduzir um vídeo.
+++

+++Atualização 91

**Data de lançamento:** 01 de junho de 2023

### Conectores

* O conector do Adobe Connect requer APIs para enviar tokens CSRF. Para obter mais informações, consulte Melhorar a segurança da conta da Adobe Connect.

### Alteração de cadeia de caracteres

* Renomeamos a sequência de caracteres Classificar este treinamento para Classificar este curso, Classificar este caminho de aprendizado ou Classificar esta certificação, com base no treinamento que um aluno faz. Dependendo do tipo de treinamento, um aluno vê a sequência de caracteres de acordo.

### Erros corrigidos nesta atualização

* A descrição do aplicativo móvel Adobe Learning Manager da Play Store diz incorretamente que um aluno pode fazer um curso offline.
* Ocorreram problemas ao migrar o conteúdo (module_version.csv e course_module.csv) do LinkedIn para o Adobe Learning Manager.
* Se uma conta estiver em um estado inativo e tiver sido criada há mais de três anos, todos os usuários da conta serão excluídos do GDPR, independentemente do status dos usuários.
* No aplicativo do professor, ao definir o limite da lista de espera como zero em uma sessão e salvar a sessão, a interface do usuário exibe incorretamente “Não aplicável” em vez de zero.
* Ao gerar transcrições do aluno para o conector do Power BI, a coluna Duração do treinamento ou módulo (minutos) exibe valores nulos para determinados módulos de sala de aula ou sala de aula virtual.
* Depois de marcar um curso como concluído para alunos em uma instância ou em várias instâncias, todos os alunos do curso são marcados como concluídos, não apenas os alunos na instância ou instâncias atuais.
+++

+++Atualização 90

**Data de lançamento:** 04 de abril de 2023

### Erros Corrigidos Nesta Atualização

O logon no SAML falhará se o URL de logon com SSO contiver entity_id.
+++

+++Atualização 89: versão de março de 2023 do Adobe Learning Manager

**Data de lançamento:** 01 de abril de 2023

### Novidades desta atualização

**Aprimoramentos na experiência de ILT (Instructor Led Training, treinamento ministrado por instrutor)**

Foram feitos vários aprimoramentos na experiência ILT (Instructor-Led Training, treinamento ministrado por instrutor). Os principais aprimoramentos incluem: capacidade de filtrar sessões de sala de aula com base no local, capacidade de alternar instâncias (VILT) sem perder o progresso, um novo “Assistente de agendamento” para gerenciar conflitos em professores de reserva e salas de aula, capacidade de anexar “Habilidades” aos professores e escolher professores com base nas habilidades.

**Melhorias na lista de verificação de observação**:

Os autores agora podem selecionar “Gerente” e “Gerenciador de armazenamento” como o Observador para listas de verificação. Os gerentes podem exibir e concluir as listas de verificação na interface do gerente sem precisar alternar a função para um professor. A notificação é enviada a um gerente quando uma lista de verificação é atribuída a ele.

**Use qualquer câmera de aplicativo/smartphone para digitalizar códigos QR do Learning Manager**

Os alunos agora poderão usar qualquer aplicativo de digitalização do QR Code ou a câmera do smartphone para digitalizar os códigos QR gerados pelo Learning Manager para inscrição no curso, conclusão e muito mais.

**Melhorias nos relatórios**

Um novo relatório de utilização de instrutor, o relatório de revisão de treinamentos, o relatório de ajudas de tarefa e outros aprimoramentos na geração de relatórios.

**Suporte para sessões &#39;híbridas&#39;**

O Adobe Learning Manager agora oferece suporte à capacidade de criar sessões “híbridas” de ILT (Instructor Led Training, treinamento ministrado por instrutor). Sessões ILT virtuais podem ser criadas com informações opcionais de local para que os alunos possam participar da sessão pessoalmente também, se estiverem disponíveis no local.

**Melhor acompanhamento do progresso para ILT virtual e em sala de aula**

Os módulos Sala de aula e ILT virtual agora oferecem a capacidade de relatar o status do questionário de um aluno (aprovado ou reprovado) junto com o status de participação. Portanto, a participação e o sucesso do questionário podem ser considerados para decidir o progresso do aluno.

**Aplicativo Adobe Learning Manager para Microsoft Teams**

O novo aplicativo Adobe Learning Manager em Microsoft Teams foi projetado para promover o aprendizado no fluxo de trabalho e impulsionar o aprendizado social. Os alunos poderão acessar o conteúdo de aprendizado na plataforma Microsoft Teams sem a necessidade de alternar para um navegador. Entre em contato com seu CSAM para a versão beta do aplicativo Adobe Learning Manager no MS Teams.

### Erros corrigidos nesta atualização

**Curso**

* Um autor personalizado não pode visualizar um módulo quando o curso está no estado “UNDER_CONSTRUCTION”. A resposta mostra o Erro 404.
* O título do curso na página do curso/adicionar de um aplicativo do autor excede quando o título do curso ultrapassa determinado limite de caracteres.

**Autor**

* No aplicativo Autor, o título do curso (se for longo) excede os limites da página ao criar um curso.
* Às vezes, um curso é adicionado, mesmo que nenhum autor seja selecionado.

**Relatórios do painel**

* As dicas de ferramenta são exibidas corretamente quando o idioma da interface é inglês, mas gera um erro de console quando o idioma da interface é diferente.
* Renomeie “Obrigatório” para “Obrigatório” no painel do aluno.

**Aplicativo do professor**

* O formato de hora no aplicativo do professor não é consistente com os outros aplicativos.

**Social**

* Para certos tipos de publicações, após a publicação, o painel social não abre conforme esperado.

**Admin**

* Um usuário com uma função personalizada não pode baixar recursos ao visualizar um curso.

**Modelos de e-mail**

* Quando um aluno cancela a inscrição em um programa de aprendizado que contém um curso de sala de aula/sala de aula virtual, ele não recebe nenhum e-mail de cancelamento.

**Ajudas de tarefa**

* Você não pode ver o nome do curso no widget Ajuda de tarefa.

**Publicação**

* A descrição do módulo adicionada no Adobe Captivate não fica visível no Learning Manager quando o módulo é publicado no ALM.

**Campos ativos**

* Quando um CSV com um grande número de registros está em processamento, ele leva um tempo significativo, durante o qual, se um usuário fizer logon e inserir um valor para um dos atributos, poderá criar um novo grupo de usuários que poderá resultar em erros de CSV. Para corrigir isso, quando a importação de CSV estiver em andamento, a mensagem pop-up do atributo Campos ativos será desativada e reativada assim que o upload do CSV for concluído.
* Se a coluna no arquivo csv Usuários tiver o mesmo nome do campo ativo usuários externos, o upload do csv falhará.

**Correções relacionadas à API**

* Na resposta learningObjects, o atributo bookmark está ausente.
* Uma entrada de acesso é criada ao gerar tokens de atualização oauth para usuários excluídos.
* A API do LO retorna o formato lo incorreto, pois os módulos de pré-trabalho foram considerados para calcular o tipo de curso junto com o conteúdo principal.

**Problemas conhecidos nesta atualização**

* O botão Compartilhar no catálogo do aluno não funciona conforme o esperado no navegador safari e no aplicativo MS Teams para dispositivos móveis e iPad.
* As notificações não são exibidas na guia Atividade depois que o aplicativo é removido em outros computadores.
Nada acontece ao clicar nas notificações na guia Atividade do aplicativo no iPhone 14.
* No aplicativo MS Teams, as notificações do Learning Manager (concluído, inscrito, prazo e atrasado) não exibem o status e o nome do curso na guia Atividade.
* Uma janela pop-up com conteúdo XML é exibida quando o administrador de integração não aprova o aplicativo do MS Teams.
* O idioma da interface do usuário no aplicativo Adobe Learning Manager no MS Teams, às vezes, não é alterado conforme esperado quando o idioma é alterado.
* Você não pode interagir com a primeira notificação quando o foco está dentro das guias Iframe (Início e Catálogo).

**Limitações do aplicativo móvel Adobe Learning Manager**

* Exibição de conteúdo offline.
* Exibição em grade/lista na página Catálogo/Meu aprendizado.
* Várias tentativas de fazer um curso.
* Prazo de inscrição em um cartão do curso.
* Em dispositivos iOS, as notificações por push não aparecem quando o aplicativo está em primeiro plano.
* Links profundos em notificações por push não são redirecionados para a página de aterrissagem pretendida.
* Clicar no botão Registrar interesse redirecionará para a Web.
* Ao responder ou comentar em Aprendizado social, não é possível anexar um arquivo.
* Você não conseguirá fazer logon no LinkedIn Learning.
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
* Altere GetNotificationData de GET para POST. A execução inicial produziu o erro, **IllegalArgumentException: cabeçalho de solicitação muito grande**, que levou a notificações de falha.
+++

+++Atualização: 86

**Data de lançamento:** 17 de fevereiro de 2023

### Erro Corrigido Nesta Versão

No aplicativo do aluno, a pesquisa de usuários e grupos de usuários está falhando devido a alguns problemas com as configurações locais.
+++

+++Atualização 85

**Data de lançamento:** 13 de fevereiro de 2023

### O que mudou nesta atualização

Adição de suporte para código de idioma de quatro letras ao filtrar idiomas em GET learningmanagerapi/v2/learningObjects.

### Erros Corrigidos Nesta Atualização

Para algumas localidades, a pesquisa retorna resultados incorretos.
Os metadados do curso são substituídos quando o curso tem mais de uma variante do mesmo local.
+++

+++Atualização 84

**Data de lançamento:** 2 de fevereiro de 2023

### O que mudou nesta atualização

**Relatório de ajuda de tarefa**

Esta atualização apresenta um novo relatório de ajuda de tarefa que lista todas as ajudas de tarefa na conta.

**Controle de versão**

Adicionamos o controle de versão para recursos ao adicionar os recursos durante a criação de um curso.

**Relatório de tentativas**

Você pode visualizar um relatório de todas as tentativas e revisões feitas por um aluno para cada treinamento.

**API de redefinição de módulo**

Um administrador agora pode redefinir um módulo usando a API de redefinição de módulo. Para obter mais informações, consulte [Referência da API do Adobe Learning Manager](https://captivateprime.adobe.com/docs/primeapi/v2/).

**Modelo de email**

Para alguns modelos de e-mail, agora você pode adicionar um pré-requisito ao modelo.

**Outras alterações**

* Você pode adicionar um curso aprovado pelo gerente como um pré-requisito.
* Melhoria de desempenho ao atualizar o painel de resumo de aprendizado.
* As IDs de e-mail e de conta são verificadas antes do envio de um relatório de rejeição.

### ERROS CORRIGIDOS NESTA ATUALIZAÇÃO

* Nomes de autor duplicados aparecem na página de visão geral do curso.
* Um hiperlink na página de criação da conta levou ao Erro 404.
* A localidade tcheca não se refletia como esperado nas configurações do reprodutor.
* Em alguns casos, as habilidades são exibidas como indefinidas para alunos em andamento e não iniciados.
* O tempo gasto em vários dias mostra o tempo diferente gasto na transcrição do aluno e nos relatórios de inscrição.
* O botão Voltar não responde para os perfis de administrador e gerente no curso > Pontuação do quiz L2 > guia Por pergunta e Presença e pontuação, respectivamente.
* Em alguns locais, em um modelo de email, parte do conteúdo no corpo do email está ausente e a tradução do idioma no modelo não é consistente.
+++

+++Atualização 83

**Data de lançamento:** 18 de janeiro de 2023

### O que mudou nesta atualização

**Nova coluna**

Uma nova coluna, **unenrollmentAllowed**, é adicionado a course.xlsx. Baixe o arquivo deste manual.

**Conector do LinkedIn Learning**

Para o conector Vinculado no aprendizado, há uma nova caixa de seleção introduzida O aluno pode cancelar a inscrição na página Filtros. Para obter mais informações, consulte [Conector do linkedIn Learning](/help/migrated/integration-admin/feature-summary/connectors.md).

### Erros Corrigidos Nesta Atualização

* Ao passar o mouse sobre os gráficos de barras, a dica de ferramenta do relatório do painel aparece conforme esperado.
* Em Relatórios na atividade do usuário, o relatório Tempo gasto no aprendizado exibe dados incorretos para dados diários/mensais.
* Em alguns casos, o gráfico de pontuação do quiz exibe valores incorretos.
* Em um curso com conteúdo SCORM com várias tentativas definidas, quando um aluno tenta o curso, o botão Rever é desativado.
* Em alguns casos, depois de inscrever um aluno em um curso e baixar um registro de auditoria de e-mail, o e-mail é entregue, mas não aparece no registro.
* O convite do calendário para um professor deve incluir o professor de texto no assunto.
* O ícone de cartão de treinamento não reflete em cartões de recomendação de cursos relacionados e de Caminho de aprendizado presentes na página de visão geral do curso.
* Nas configurações da página inicial do aluno, adicione uma seção Salvo por mim.
* Para determinadas contas, um usuário é solicitado a fornecer o logon com SSO para uma conta na qual a ID de Adobe é necessária.
* Em fusos horários com Horário de Verão, o campo &#39;start_time&#39; é calculado com base na diferença de hora atual, não com base na diferença de hora na data e hora de início reais. Isso causou convites com horários incorretos.
* Sempre que uma certificação ocorre novamente, uma cópia dos cursos subjacentes é criada internamente no banco de dados. Esses cursos então aparecem em busca, ao contrário do comportamento esperado.
* Quando o upload de um CSV falha, você não recebe nenhuma notificação por email.
* Se os nomes dos campos ativos forem longos, eles desaparecerão ao serem arrastados e soltos. Depois disso, o botão Salvar também não funciona conforme o esperado.
* Um relatório de sessão não é exportado por meio da página de participação e pontuação de um curso se o primeiro usuário no relatório tiver um registro na tabela de níveis de atividade com o comentário como nulo.
* Ao usar a conta de administrador para recuperar as medalhas, você pode classificar a lista como esperado. Mas quando você executa o mesmo para um aluno, os resultados não são classificados.
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

**Data de lançamento:** 5 de novembro de 2022

**Observação:** Com esta versão do Adobe Learning Manager, os usuários com contas inativas não podem mais acessar suas contas usando subdomínios. As contas podem ser acessadas usando a ID da conta ou usando a página acapindex.html e inserindo a ID de e-mail.

### Novidades desta versão

A versão de novembro de 2022 do Adobe Learning Manager consiste no seguinte:

* Configuração de SSO Múltiplo
* Suporte a recurso não conectado
* Melhorias na página de visão geral do treinamento
* Personalização do reprodutor
* Representação do aluno e do gerente

Para obter mais informações, consulte [Novidades do lançamento do Adobe Learning Manager em novembro de 2022](/help/migrated/whats-new-2022-november.md).

**Observação:** Com a versão de novembro de 2022 do Adobe Learning Manager, o Zoom será descontinuado [Autenticação JWT até junho de 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). Da mesma forma, o conector do Zoom com JWT continuará funcionando até a data mencionada, mas recomendamos que os usuários criem um aplicativo OAuth de servidor para servidor para substituir a funcionalidade na conta deles. Qualquer nova conexão terá a autenticação OAuth do Zoom por padrão.

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

### Problemas conhecidos nesta atualização

* Em alguns casos, o gráfico de pontuação do quiz não é exibido conforme esperado. Ao redimensionar o gráfico, um espaço em branco é exibido no início. Além disso, nem todas as perguntas são exibidas e os dados incorretos são exibidos intermitentemente.
+++

+++Atualização 80

**Data de lançamento:** 20 de setembro de 2022

* Os problemas de logon no aplicativo móvel no iOS foram corrigidos.
* Correção de um problema com emails rejeitados.
* Os professores eram notificados incorretamente mesmo antes de os envios terem sido feitos pelos alunos.
* Um professor recebe uma notificação por e-mail mesmo que um aluno não tenha enviado uma atividade.
* Depois de criar uma sessão de aula virtual no MS Teams ou no Adobe Connect, os professores não recebem os convites de sessão.
* Status incorreto em um caminho de aprendizado.
* Desempenho aprimorado do aplicativo.
+++

+++Atualização 79

**Data de lançamento:** 18 de agosto de 2022

* A confirmação de convite do calendário para sessões ILT/VILT agora funciona com o calendário do Google.
* Um gerenciador de loja agora pode ver notificações para usuários abaixo deles, mesmo se eles forem removidos como um gerenciador de pessoas.
* Em alguns casos, a inscrição no curso falha e exibe o Erro 500.
* Em alguns casos, não é possível modificar uma instância virtual do curso para equipes.
* Os administradores e professores podem adicionar comentários para usuários que não participaram de sessões ILT/VILT.
* Melhorias no desempenho ao baixar relatórios de tamanho grande.
* Quando o email de um usuário é rejeitado, o administrador recebe uma notificação por email. O e-mail contém um link que, quando clicado, baixa um CSV com a lista de usuários cujos e-mails foram rejeitados. O administrador pode tomar as medidas necessárias.
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
* No campo /boards/{id}/posts na resposta da API, a propriedade “post.attributes.myPoll” aparece como um objeto vazio.
* Em alguns casos, para um usuário não conectado, o botão Adicionar ao carrinho é desativado para alguns cursos ou planos de aprendizado.
* URL de subdomínio incorreto na página de identidade visual.
+++

+++Atualização 77

**Data de lançamento:** 24 de maio de 2022

**Problemas corrigidos nesta atualização:**

* Os novos cursos não respeitam a sequência no aplicativo Salesforce. Se você alterar a sequência, o curso não será exibido na sequência desejada.
* Depois de modificar as configurações na página inicial clássica e salvá-las, as alterações não são salvas conforme esperado. Isso acontece intermitentemente.
* O código de HTML é exibido quando os alunos verificam suas notificações, o que afeta negativamente a experiência.
* No painel, o tempo gasto no aprendizado é exibido incorretamente como zero horas.

## ATUALIZAÇÃO: O Adobe Learning Manager será renomeado para Adobe Learning Manager

Este é uma atualização sobre uma alteração futura que ajudará você a se preparar para isso.

**O Adobe Learning Manager como um produto será renomeado para Adobe Learning Manager em julho de 2022**. Isso é um esforço estratégico feito para refletir com mais precisão o alinhamento do produto com determinadas prioridades de negócios.

A equipe de produto está tomando todas as medidas para garantir que não haja impacto no uso da plataforma. Você pode continuar a utilizar o produto como habitualmente. Os administradores da plataforma podem notar o novo nome da marca em determinadas telas em julho.

Como parte dessa alteração, os URLs de acesso do Learning Manager são afetados.

Por exemplo, se o URL de acesso da sua conta for `https://learningmanager.adobe.com/XYZ`, o novo URL será `https://learningmanager.adobe.com/XYZ`.

Todos os URLs existentes continuarão funcionando.

Para concluir esta ação, contate o departamento de TI da sua organização. Para obter mais informações, entre em contato conosco em `learningmanagersupport@adobe.com`.
+++

+++Atualização 76

**Data de lançamento:** 20 de abril de 2022

* Correções nas terminologias do produto em alguns relatórios do painel.
* Uma barra dupla (”//”) no URL de um ponto de extremidade resultou em erros de validação.
* Após atualizar uma página, a porcentagem de conclusão e os últimos campos visitados exibiram informações incorretas.
* Fizemos algumas alterações em como o valor Certificado ou um plano de aprendizado é calculado.
* Um administrador personalizado podia adicionar todos os usuários como professores, mesmo que tivesse permissão para adicionar apenas um usuário.
* Em um PDF de medalha, uma data de conclusão incorreta era exibida.
+++

+++Atualização 75

**Data de lançamento:** 29 de março de 2022

* Em algumas contas, após copiar o csv bruto no local do FTP, a importação do usuário não ocorre conforme o esperado e há várias notificações de erros.
* Em versões anteriores do Learning Manager, para configurar um conector do Zoom, era necessário configurar primeiro o FTP do Exavault para copiar o arquivo csv. Nesta versão, o conector FTP não será mais usado para o arquivo csv e, portanto, você não precisa configurar primeiro o FTP.
+++

+++Atualização 74: Instância do Learning Manager AWS India

**Data de lançamento:** 15 de fevereiro de 2022

### Visão geral

Um [instância](https://learningmanagerapac.adobe.com/acapindex.html) do Learning Manager agora será hospedado no AWS em Mumbai (ap-south-1). Para clientes que usam essa instância da Índia, as informações de identificação pessoal (PII) e os registros de aprendizado do usuário serão armazenados somente na região da Índia.

### O que é compatível

A instância da Adobe Learning Manager India está ao mesmo nível de outras instâncias, como regiões da UE e dos EUA, em termos de recursos. Existem alguns recursos que não são suportados na instância da Índia. São eles:

* Pagamento com cartão de crédito para compra de vagas
* catálogo de conteúdo do Creative Cloud
* Aplicativo Slack
* **&#42;** Aguardando certificação para conformidade com SOC2

### Perguntas frequentes

**Qual é a diferença entre essa instância em Mumbai e outros ambientes exclusivos para AWS?**

Não há diferença. A instância em Mumbai é a mesma de [AWS EUA](http://learningmanager.adobe.com/) ou [AWS EU](http://learningmanagereu.adobe.com/) instâncias. Essa instância é hospedada na Índia e todos os registros de aprendizado e dados do usuário permanecem nesse país. Os seguintes recursos não são suportados na instância da Índia:

* Pagamento com cartão de crédito para compra de vagas
* catálogo de conteúdo do Creative Cloud
* Aplicativo Slack
* **&#42;** Aguardando certificação para conformidade com SOC2

**Esse ambiente estará em conformidade com o Common Controls Framework (CCF)?**

Sim. A nova instância está em conformidade com o CCF (Common Control Framework).
+++

+++Atualização 73

Data de lançamento: 5 de fevereiro de 2022

* O suporte a modelos de e-mail agora está disponível para idiomas de conteúdo, incluindo húngaro e finlandês.
+++

+++Atualização 72 - Versão de janeiro de 2022 do Learning Manager

Data de lançamento: 15 de janeiro de 2022

### Novidades e alterações

* Adicionar locais de sala de aula
* Alterações de gamificação
* conector de Microsoft Teams
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

**Modelo de email**

* Convites de sessão que se estendem por vários dias, nos quais os convites não refletem as informações corretas sobre os dias que são bloqueados em alguns clientes de email. Esse problema já foi corrigido.
* A variável “Nome do local” estava ausente no modelo de e-mail “Lembrete da próxima sessão” para alunos na localidade alemã. Isso já foi adicionado.
* O link para criar a conta como parte do e-mail de boas-vindas para o usuário não estava considerando a localidade do usuário, o que foi corrigido.

**Lembretes de e-mail**

* Se os alunos foram inscritos no treinamento por meio de um plano de aprendizado, os e-mails de lembrete de conclusão eram enviados várias vezes com base no número de edições feitas nas datas de conclusão do mesmo plano de aprendizado. Agora esse problema foi corrigido.

**Usuário**

* A mensagem mostrada ao usuário quando sua conta está inativa/suspensa foi aprimorada, indicando que ele deve entrar em contato com o administrador para que suas contas sejam habilitadas novamente.

**Atividade**

* Um professor não podia exibir os envios do aluno se o nome do arquivo de envio tivesse um caractere especial. Esse problema já foi corrigido.

**Denunciar**

* Um administrador não conseguia baixar o relatório de inscrição do curso se ele contivesse um aluno que estava inscrito indiretamente neste curso por meio de uma programação de aprendizado flexível, mas ainda não tinha escolhido uma instância para este curso no caminho de aprendizado. Agora esse problema foi corrigido.
* Reorganizar relatórios no painel de relatórios para funções de administrador e gerente não estava preservando o estado da ordem de relatórios. Agora esse problema foi corrigido.

**Conteúdo**

* O conteúdo de áudio no treinamento não era reproduzido automaticamente na visualização como modo de aluno devido às políticas de reprodução automática do navegador. Agora isso foi corrigido para navegadores compatíveis, exceto o Safari.

**Gamificação**

* Se um aluno externo foi convertido como aluno interno na mesma conta, ele não conseguia acessar o quadro de classificação de gamificação no aplicativo do aluno. Agora esse problema foi corrigido.

**Reprodutor**

* O reprodutor não mostrava uma mensagem de aviso quando o usuário tentava pular módulos em um curso ordenado com o tipo AICC de módulos. Esse problema já foi corrigido.
* Para certos cursos adquiridos com módulos de vídeo em caso de LMS sem periféricos, a reprodução não funcionava para determinados usuários. Esse problema foi corrigido agora.

**Painel do gerente**

* Um gerente não podia exportar o relatório para sua equipe direta da página de habilidades da equipe do Painel do Gerente. Agora esse problema foi corrigido.

**Publicar**

* Na instância europeia do conteúdo do Learning Manager que foi publicado diretamente no Adobe Learning Manager pelo Adobe Captivate, o conteúdo estava sendo publicado no local Deutsch por padrão. Esse problema já foi corrigido.

**API**

* O campo de duração foi adicionado ao modelo de ajuda de tarefa.
* Para as APIs de recomendação, às vezes uma solicitação GET retorna o Erro 500.
* Ao migrar treinamentos por meio do Exavault e se o texto contivesse caracteres que não fossem do inglês, ele costumava ser atualizado com caracteres residuais no texto. Agora esse problema foi corrigido.

**Localização**

* `NormalTextRun  BCX0 SCXW38820519 For the`Aplicativos do administrador, autor e aluno, parte do conteúdo em alemão não aparece conforme esperado.

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

No Learning Manager, o **Compartilhar com Gerentes** O fluxo de trabalho permite que os administradores compartilhem treinamentos com gerentes, para que eles possam ser adicionados ao Painel de conformidade de um gerente. Assim, os gerentes não precisam realizar nenhuma ação e podem começar a monitorar a conformidade imediatamente.

Para obter mais informações, consulte  [**Compartilhar treinamento com gerentes**](../administrators/feature-summary/reports.md#share_training_managers).

### Erros corrigidos nesta atualização

* Se houver duas contas e o recurso Caminho de aprendizado aprimorado estiver desativado e houver um catálogo compartilhado da primeira conta para a outra, então o Caminho de aprendizado na segunda conta terá seções duplicadas na página do curso.
* Um FTP personalizado agora suporta sftp://, além de http:// e https://
* O conector Exavault agora usa APIs V2.
* Em alguns casos, a qualidade dos vídeos era inferior ao ideal. O problema já foi corrigido.
* Mesmo depois que um aluno tiver concluído um curso obrigatório e aprovado pelo gerente, a certificação permanece no estado Aprovação pendente.
* Se os nomes dos autores contiverem caracteres acentuados, a migração do curso falhará.
* Se o Campo ativo tiver valores em maiúsculas, ele não será salvo como esperado.
* Não é possível filtrar Caminhos de aprendizado com base em habilidades.
* Quando um administrador cria uma instância e adiciona uma nova sessão, um professor não recebe o e-mail de convite da sessão. Esse problema ocorre nos cursos por videoconferência no Zoom.
+++

+++Atualização 70

Data de lançamento: 28 de outubro de 2021

### Erros corrigidos nesta atualização

* Em alguns casos, as informações sobre um caminho de aprendizado não são refletidas em uma transcrição do aluno.
* O texto dentro do **Marcar conclusão** é atualizada para refletir que a operação é irreversível.
* A API dos objetos de aprendizado, em alguns casos, retornou um erro de metadados.
+++

+++Atualização 69 - Versão de outubro de 2021 do Learning Manager

**Data de lançamento:** 09 de outubro de 2021

### Caminho de Aprendizado

O **Versão de outubro de 2021 do Adobe Learning Manager** apresenta o conceito de Caminhos de aprendizado.

>[!NOTE]
>
>O **Configurações > Geral** tem uma nova opção para ativar os recursos estendidos de caminhos de aprendizado. Se essa opção estiver ativada, você pode adicionar caminhos de aprendizado em outro caminho de aprendizado. Não é possível alterar a opção depois de ativada.

Os Caminhos de aprendizado substituem nosso recurso existente de Programas de aprendizado. Imagine os programas de aprendizado obtendo aprimoramentos poderosos sem descartar os recursos existentes. Além disso, o recurso é marcado como um caminho de aprendizado.

Para obter mais informações, consulte [***Caminhos de aprendizado***](../administrators/feature-summary/learning-paths.md).

### Outras alterações

* Novo aplicativo do Salesforce
* Hub de Conteúdo
* Alterações de relatórios
* Relatório de resumo da sessão
* Alterações no sumário do reprodutor
* Alterações de API
* Alterações relacionadas ao conector

Para obter mais informações, consulte [***Novidades no lançamento de outubro de 2021 do Learning Manager***](../whats-new.md).

### Erros corrigidos nesta atualização

* Os modelos de e-mail, como Cancelamento de inscrição no curso, Cancelamento de inscrição no programa de aprendizado ou Cancelamento de inscrição de certificação, não refletem as terminologias de produtos mais recentes, conforme definidas no csv. Agora, o texto padrão nos modelos de e-mail oferecerá suporte a terminologias personalizadas.
* O idioma do usuário no Learning Manager não é suportado no fluxo de trabalho Publicar no Learning Manager. Se o idioma do usuário for diferente, Publicar no Learning Manager acontece em inglês.
* Se você adicionar muitos catálogos a uma função personalizada, ocorrerá um erro quando você atualizar a função. O limite de número de catálogos foi aumentado em até 50 catálogos.
* Em alguns casos, os treinamentos excluídos ainda são visíveis em um catálogo. Esse problema ocorreu somente no aplicativo de administração e está corrigido.
* Quando a função de gerente era alterada de um usuário para outro, a função de gerente do usuário anterior ainda refletia na interface do usuário. Esse problema já foi corrigido. Esse problema estava presente apenas para usuários externos, não para usuários internos.
* Em alguns cenários específicos para um grande conjunto de usuários que eram importados via csv do usuário, a importação falhava. Esse problema foi corrigido agora.
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
   * Conselho público e publicação
   * Painel particular e publicação com acesso
   * Painel particular e publicação sem acesso
   * Painel e publicação restritos
   * Comentário na publicação
   * Resposta ao comentário
   * Perfil de usuário social

* Para contas que usam domínio personalizado, o aplicativo do aluno não exibe o favicon.
* No AEM, o componente do Learning Manager exclui a configuração de outros componentes.
* A página de ajuda para o componente AEM é redirecionada para um local incorreto.
* Obtenção e armazenamento externo de e-mails/tokens do usuário para que os usuários possam implementar seu próprio back-end de armazenamento em vez de usar nós de usuário AEM.
* Ao editar a descrição de texto sem formatação em Cursos, Programas de aprendizado, Certificados e Ajudas de tarefa, uma mensagem de aviso é exibida.
* Os relatórios do Painel do gerente não são baixados quando um usuário tem funções personalizadas e de gerente.
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

O **Agosto de 2021** **lançamento do Adobe Learning Manager** O foco é melhorar os fluxos de trabalho da Experiência do aluno, Relatórios e Administrações. Alguns dos destaques incluem:

* **Marketplace de conteúdo:** O Learning Manager agora oferece mais de 70.000 cursos de campos variados, como Tecnologia, Gerenciamento, Liderança e assim por diante.
* **Suporte de acessibilidade aprimorado:** O suporte de acessibilidade para a função do aluno fortalece por meio da navegação do teclado aprimorada, capacidade do leitor de tela e conformidade com a taxa de contraste.
* **Formatação Rich Text:** O Learning Manager agora oferece edição de rich text para descrições em cursos, programas, certificados e ajudas de tarefa. Isso permite que os autores especifiquem descrições em rich text, incluindo hiperlinks, imagens e outras opções de formatação de texto, em vez de texto sem formatação.
* **Classificação por estrelas:** Um aluno agora pode classificar um curso em uma escala de 5 pontos. Um administrador pode selecionar entre a classificação da eficácia existente ou a classificação de 5 estrelas.
* **Integração do Badgr:** Os alunos agora podem autorizar o Learning Manager a enviar automaticamente as medalhas que ganharam no Learning Manager para a conta do Badgr, de onde podem compartilhar as medalhas em suas redes sociais.
* **Exportar eventos de aprendizado para o Salesforce:** O Learning Manager agora oferece a capacidade de exportar alguns eventos específicos no Learning Manager, como adição de novos usuários, inscrição e conclusão para um inquilino do Salesforce e fornece a capacidade de vinculá-los ao objeto de usuário ou ao objeto de contato apropriado no Salesforce.

Para obter mais informações, consulte [***Novidades e alterações na versão de agosto de 2021 do Learning Manager***](../whats-new.md).


**Data de lançamento:** 7 de agosto de 2021

### Erros corrigidos nesta atualização

**Experiência do aluno**

* Depois que um aluno é adicionado a dois grupos de usuários e um plano de aprendizado é adicionado, o aluno é inscrito em uma instância diferente do mesmo curso.
* Em alguns casos, após a inscrição e o início do curso, o curso não é reproduzido conforme esperado.
* A descrição do curso exibe tags HTML, que agora foram corrigidas.
* Se você comentar em uma publicação de um painel social que abrange várias linhas, o comentário será exibido em uma única linha. Esse problema já foi corrigido.

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

**Aplicativo do dispositivo**

* Em dispositivos Android e iPhone, um aluno não pode iniciar módulos do curso aleatoriamente. Isso produz o Erro 401 não autorizado.
* Um aluno pode digitalizar dois códigos QR, mas ao digitalizar o terceiro código QR, uma mensagem de erro é exibida.
* Em alguns dispositivos Android e iOS, um arquivo não é aberto como esperado para alguns cursos baixados.
* Tentar abrir uma ajuda de tarefa exibe uma mensagem de erro.
* O aplicativo do dispositivo se comporta inesperadamente quando um programa de aprendizado é usado offline.
* Quando um aluno volta online e abre o aplicativo, ele fica preso na tela inicial.
* Às vezes, quando um usuário está online novamente, o aplicativo muda para a exibição clássica.
* Às vezes, quando um curso é usado offline, o progresso não é salvo.
* Às vezes, o nome de um curso não é exibido como esperado desde o início quando o nome é longo.
* Na página do catálogo, os cursos não são classificados como esperado.
+++

+++Atualização 65

Data de lançamento: julho de 2021

### Erros corrigidos nesta atualização

* Problemas com logons de usuários.
* O modelo de e-mail de inscrição do curso para gerente não exibe o prazo de conclusão do curso se a variável for adicionada ao modelo.
* O TLS 1.0 e o TLS 1.1 foram descontinuados.
* Problemas com exclusão de dados do RGPD para um usuário.
+++

+++Atualização 64

Data de lançamento: julho de 2021

### Erros corrigidos nesta atualização

* A notificação de inscrição é enviada aos alunos que já estão inscritos em um curso.
* Quando um certificado personalizado como uma medalha é gerado, o formato de data não é suportado no idioma alemão.
+++

+++Atualização 63

Data de lançamento: junho de 2021

### Erros corrigidos nesta atualização

* Você pode criar um usuário com um nome em branco em um csv.
* Se houver um caractere &#39;/&#39; no campo ativo, depois de criar um trabalho para baixar user.csv, o estado do trabalho não é alterado de “Enviado” para “Concluído”.
* Os módulos ordenados não obedecem à sequência.
* Quando um autor externo é excluído, o curso que o autor criou não está mais disponível.
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
* Erros em um relatório se propagam para outros. Como resultado, esses relatórios levaram a erros.

**Ajudas de tarefa**

* Após baixar uma ajuda de tarefa, você não poderá excluí-la.

**Reprodutor**

* As legendas WebVTT não são exibidas conforme esperado.

**Aplicativo do aluno**

* Na página Visão geral da certificação, a certificação externa não exibe a duração adicionada por um autor.
* Adicionar a opção **Tudo** no filtro Habilidade.
* Os alunos recebiam vários e-mails de resumo.
* O número de linhas selecionadas não corresponde ao esperado em uma página.

**Componente AEM**

* Os widgets não são atualizados como esperado após uma atualização de página.

**Localização**

* Algumas cadeias de caracteres em alemão não estão localizadas conforme o esperado.
* A tradução de cadeias de caracteres é padrão para inglês se um aluno não selecionou a interface e o idioma do conteúdo.

**Certificação**

* A ordem do módulo pode ser ignorada se os pré-requisitos não forem aplicados.

**Navegador**

* Os aplicativos de autor, gerente ou aluno não são exibidos conforme esperado no IE 11.

**Gamificação**

* Os pontos de gamificação não são resgatados conforme esperado.

**Biblioteca de conteúdo**

* Os cursos do aplicativo de avaliação de conteúdo não funcionam conforme esperado.

**Reprodutor**

* O player carrega apenas no espaço onde o widget está presente.
* Os vídeos dentro de um módulo Captivate não são reproduzidos conforme esperado.

**Conector**

* Em alguns casos, os arquivos são excluídos de um conector FTP/Box.
* Os arquivos são excluídos do FTP se forem atualizados com os mesmos nomes.
* Um evento BlueJeans suporta paginação onde o número de eventos é maior que 100.

**Atualização do aplicativo móvel 3.3 - março de 2021**

Data de lançamento: 26 de março de 2021

### Novidades e alterações {#whatsnewandchanged}

A atualização do aplicativo móvel do Captivate Learning Manager 3.3 apresenta uma nova página inicial, que suporta manchetes e recomendações de treinamento baseadas em IA. Esta página inicial está disponível para todas as contas configuradas para a nova opção Layout imersivo. As contas configuradas com o Layout clássico continuam a ver a página inicial clássica/herdada. Elas não devem observar nenhuma alteração na página inicial.

Além disso, essa atualização também permite que os alunos baixem a medalha como PDF e uma imagem. A atualização também apresenta um pop-up de feedback, que permite aos alunos fornecer feedback anonimamente sobre o aplicativo.

Para obter mais informações, consulte  [Aplicativo de dispositivo do Learning Manager](../learners/feature-summary/ipad-android-tablet-users.md).

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

Para obter mais informações, consulte Novidades no [Atualização do Learning Manager em fevereiro de 2021](../whats-new.md).

### Erros corrigidos nesta atualização {#bug-fixes}

**Certificação**

* Em alguns casos, o aluno não conseguia tentar novamente um curso, que faz parte de uma certificação, embora o máximo de tentativas para o curso esteja definido como infinito. Agora esse problema foi corrigido.
* Em alguns casos, o aluno não conseguia se inscrever em uma certificação devido à **Inscrever-se** botão não visível como esperado.

**Biblioteca de conteúdo**

* URL de ajuda incorreto no **Adicionar Novo Conteúdo** página. O URL correto foi atualizado.

**Curso**

* Um relatório de pontuação do quiz L2 baixado para um módulo de conteúdo AICC mostra a pontuação incorreta na coluna Pontuação total do usuário/Pontuação do quiz. Esse problema foi corrigido.
* Baixar recursos de um curso não funcionava se ele fosse duplicado de outro curso e se o aluno não tivesse acesso ao curso original, o que costumava criar um curso duplicado.
* Imagens de banner que não são excluídas quando o autor as remove, estando o curso no estado de rascunho. Esse problema foi corrigido.

**AEM**

* Depois de inserir o componente do Learning Manager no AEM, a página demorava a carregar, impedindo o acesso aos outros componentes. Esse problema foi corrigido.

**Admin**

* Os cursos retirados não aparecem nos resultados da pesquisa conforme esperado. Esse problema foi corrigido.
* O administrador não conseguia pesquisar cursos retirados em **Aplicativo do administrador** -> **Relatórios personalizados** -> **Relatórios do Excel** -> **Relatórios do curso**, que já foi corrigido.

* Baixar um relatório do quiz como Excel não funcionará se o arquivo contiver alunos que realizaram os treinamentos antes e depois da atualização do conteúdo. Esse problema foi corrigido.
* Um upload de CSV falhará se os campos ativos contiverem caracteres especiais. Esse problema foi corrigido.
* Em alguns casos, quando um aluno fazia um quiz, criado em Captivate, as respostas não eram capturadas da maneira esperada.
* Depois de criar uma assinatura e tentar editar a assinatura, a **Salvar** e **Cancelar** não são exibidos conforme esperado. Esse problema foi corrigido.

**Reprodutor**

* Para um tipo específico de conteúdo do cenário de retomada SCORM-2004 que não estava funcionando. Assim, os alunos tinham que navegar até o ponto em que pararam. Esse problema já foi corrigido. O conteúdo agora deve ser retomado a partir do ponto que foi usado antes.
* Depois de se inscrever em um curso, em alguns casos, o conteúdo não era reproduzido conforme esperado. Esse problema foi corrigido.

**Cancelar inscrição**

* Um relatório de inscrição listava apenas 20 alunos não inscritos, mesmo quando havia mais alunos não inscritos no curso/certificação. Esse problema foi corrigido.
* Ocorria um problema ao exportar a lista de alunos não inscritos no relatório de inscrição em alguns casos. Esse problema já foi corrigido.

**Programa de aprendizado**

* Para um plano de aprendizado flexível, se um aluno estivesse inscrito em apenas uma instância do curso, ao clicar no link do curso dos outros cursos, cujas instâncias não foram selecionadas, uma página em branco era aberta.

**Aluno**

* Alguns alunos, cujos nomes de usuário têm caracteres especiais, não recebiam notificações por e-mail conforme esperado.
* Na exibição imersiva, em alguns casos, o widget Calendário não exibia as próximas sessões de aula virtual conforme esperado.
* No aplicativo do aluno, o menu **Habilidade** o filtro não funcionou como esperado. Esse problema foi corrigido.

**Pesquisar**

* Em um cenário específico, o Gerente não conseguia procurar um grupo de usuários de um gerente anteriormente. Esse problema foi corrigido para a função Gerente.

**Grupo de usuários**

* Ao exportar o relatório de grupo de usuários com mais de 500 usuários, os valores de dados e os cabeçalhos de coluna no relatório não correspondiam, o que foi corrigido.
* Quando o administrador editava a assinatura por e-mail em modelos de e-mail e adicionava várias linhas, ele via tags html somente na interface do administrador. Esse problema foi corrigido agora.
* Entrada **Aplicativo do administrador > Catálogo > procurar catálogo**, não é possível pesquisar.

**Usuários**

* Alguns usuários externos ativos estavam sendo excluídos. Fizemos algumas alterações e o problema foi corrigido.

**Importar**

* A importação de um csv falhará se o cabeçalho csv contiver espaços em branco à direita ou se o email de um usuário contiver acentos ou caracteres diacríticos.

**Envio de atividade**

* No aplicativo do instrutor - página de envios de atividade, o valor de data enviado costumava se sobrepor ao nome do arquivo, se fosse longo. Esse problema de interface do usuário agora está resolvido.

**Professor**

* Um professor recebe convites de sessão para todas as suas sessões, mesmo que apenas uma nova sessão seja adicionada. Esse problema foi corrigido.

**SCORM**

* Para determinados conteúdos do SCORM, há alguns problemas relacionados ao navegador, problemas de navegação do reprodutor e inconsistências na gravação da pontuação do quiz. Esses problemas foram corrigidos.

**SAML e SSO**

* Atualizamos a mensagem de erro exibida quando as credenciais do SSO expiravam.

**API do Learning Manager**

* A API getlearningObject retornou dados de inscrição incorretos devido a problemas no armazenamento em cache. Esse problema foi corrigido.
* Uma sessão de aula virtual agora exibe o URL da reunião no campo Local em um convite de reunião.
* Se você configurou várias integrações de provedor de aula virtual e se alguma delas não funcionava como esperado, o menu suspenso de seleção de aula virtual costumava mostrar uma lista vazia. Esse problema já foi corrigido. A integração de aula virtual restante é listada corretamente agora.
* Os modelos de aula virtual do Connect não eram carregados conforme esperado quando um professor entrava na sessão.
* Uma duração incorreta era mostrada na interface do usuário após a migração de módulos com duração no arquivo csv module_version.
* Para algumas contas, a atualização de um usuário não funciona conforme o esperado. Esse problema foi corrigido.

### Problemas conhecidos nesta atualização {#known-issues}

* Ao usar o comando **Duração** No aplicativo do aluno, o conteúdo e o filtro podem não estar sincronizados se o aluno usar algum outro conteúdo local e não fizer parte da instância padrão em termos de inscrição.

>[!NOTE]
>
>O treinamento &#39;**Duração**&#39; e &#39;**Formato** Os filtros &#39; são identificados com base no conteúdo de treinamento disponível para a instância padrão e para o local preferido da conta.

+++

+++Atualização 59

## Atualização 59

Data de lançamento: 18 de dezembro de 2020

### Conector do BlueJeans Events {#bluejeanseventconnector}

O conector do BlueJeans Events conecta os sistemas do Learning Manager e do BlueJeans para automatizar a sincronização de dados. Com esse conector, você pode:

* **Configurar sessões virtuais usando o BlueJeans Events:** Configure um novo evento no BlueJeans e configure uma sessão VC no Learning Manager selecionando o evento do BlueJeans apropriado. Os detalhes de data e hora são escolhidos automaticamente nos eventos do BlueJeans.
* **Sincronização de conclusão de usuário automatizada:** Um processo de sincronização automática de conclusão do usuário permite que o administrador do Learning Manager busque registros de conclusão para eventos do BlueJeans automaticamente.

Este novo conector requer um conjunto separado de credenciais para configurar o conector.

Para obter mais informações, consulte [***Conector do BlueJeans Events***](../integration-admin/feature-summary/connectors.md#bj-events).

+++

+++Atualização 58 - Versão de dezembro de 2020 do Learning Manager

## Atualização 58 - Versão de dezembro de 2020 do Learning Manager

Data de lançamento: 5 de dezembro de 2020

### Novidades e alterações {#Whatsnewandchanged-2}

Esta versão concentra-se no seguinte:

* Experiência de página inicial do novo aluno
* Layout móvel responsivo para a função do aluno
* Recomendação baseada em IA para alunos
* Emails de resumo semanal
* Lista de verificação
* Integração do Marketo
* Domínio personalizado
* Importação do questionário do Adobe Connect
* Link profundo para o catálogo dos alunos
* Aprimoramentos do linkedIn Learning
* ...e muito mais

Para obter mais informações, consulte  [***Novidades na versão de dezembro de 2020 do Adobe Learning Manager***](../whats-new.md).

### Recursos sem suporte em experiência imersiva móvel {#unsupportedfeaturesinmobileimmersiveexperience}

Os seguintes recursos não são compatíveis:

* Aplicativo social: um aluno é redirecionado para a experiência clássica se clicar no widget Social na página inicial
* Configurações de perfil/Editar perfil
* Exibir medalha/habilidades
* Quadro de classificação: um aluno é redirecionado para a experiência clássica se clicar no widget Quadro de classificação na página inicial
* Baixando ajudas de tarefa.
* Opções de filtro em Pesquisar.

### Erros corrigidos nesta atualização {#bug-fixes-1}

* Não é possível excluir uma pasta de conteúdo se ela contiver conteúdo excluído.
* O plano de aprendizado permite que os administradores configurem um curso com instância automática. Para um curso com o módulo de envio Atividade, as informações do professor não eram configuradas corretamente anteriormente. Agora o Learning Manager atribui o professor da instância padrão a essa instância automática automaticamente.
* Um emblema personalizado com um rótulo de catálogo com um espaço não permite que o pdf seja baixado conforme esperado.
* Um relatório baixado do painel é diferente do e-mail de assinatura recebido para o relatório do painel.
* Uma transcrição do aluno não tem dados atualizados para uma certificação recorrente.
* Depois de iniciar um curso, se você deixar o curso expirar, o número de tentativas não é exibido conforme esperado. Também há uma tela em branco às vezes quando você tenta um curso várias vezes.
* Ocorreu o erro 5xx após o upload de um módulo.
* Um painel social privado não é visível para todos os alunos.

### Problemas conhecidos nesta atualização {#known-issues-1}

Depois de concluir um curso ou uma certificação, você não vê o pop-up de feedback imediatamente. Esse problema ocorre somente quando você faz o curso na interface de usuário imersiva. Se você fizer o curso na interface do usuário clássica, poderá ver a janela pop-up de feedback como esperado.

+++

+++Atualização 57

## Atualização 57

Data de lançamento: 23 de setembro de 2020

**Biblioteca de conteúdo**

* Na biblioteca de conteúdo, desativar um conteúdo não remove o conteúdo na **Publicado** guia. Quando você atualiza a página, o conteúdo retirado não é mais exibido.
* Ao criar uma pasta de conteúdo, o **Nome** O campo não está marcado como obrigatório, o que na verdade é um campo obrigatório.

**Solicitação do cliente**

* Para identificar todos os cursos nos quais cada aluno está inscrito e se os concluiu, inclua os seguintes campos no painel, Relatório de assinatura:

   * UUID
   * Endereço de email

**Transcrição do aluno**

* Gerar uma transcrição do aluno no idioma indonésio estava causando erros.

**Pesquisar**

* Não é possível pesquisar um curso específico. Esse problema foi corrigido.

+++

+++Atualização 56 - Aplicativo móvel

Data de lançamento: 25 de agosto de 2020

### Fazer cursos do LinkedIn Learning {#takecoursesfromlinkedinlearning}

O Learning Manager já é compatível com os cursos do LinkedIn Learning dentro da plataforma de aprendizado. Agora os alunos podem realizar esses cursos do LinkedIn Learning no aplicativo móvel do Learning Manager. No aplicativo do dispositivo, procure um curso e, em seguida, inicie o curso.

Para obter mais informações, consulte Fazer cursos de [***Aprendizado linkedIn***](../learners/feature-summary/ipad-android-tablet-users.md#linkedin).

### Enviar notificação por push para inscrições de administradores {#pushnotificationforadminenrollments}

Quando o administrador inscreve alunos em treinamentos, os alunos recebem notificações sobre as inscrições.

Agora, a notificação por push também é compatível com os comunicados.

### Feedback N1 obrigatório {#mandatoryl1feedback}

Na versão de agosto de 2020 mais recente, o Learning Manager permite que os administradores configurem feedback L1 de modo que todas as perguntas se tornem obrigatórias. O mesmo agora é compatível com a perspectiva do aluno no aplicativo móvel.

### Melhorias na interface do usuário {#userinterfaceenhancements}

**Links do rodapé**

O administrador pode configurar vários links de rodapé na exibição do administrador na Web. Os alunos agora podem acessar esses links tocando no ícone de opções e no ícone Ajuda.

Por padrão, haverá dois links e o administrador poderá adicionar outros três links (pela exibição do administrador na Web) que aparecerão no aplicativo.

**Exibição de cartão para objetos de aprendizado**

Por padrão, nas seções Meu aprendizado e Catálogo do aplicativo, os treinamentos aparecem como cartões em vez de listas. Isso é uma alteração para os alunos, pois antes a exibição padrão era “Exibição em lista”.

No entanto, os alunos podem alternar a exibição entre a Exibição de lista e a Exibição de cartão.

+++

+++Atualização 55 - Versão de agosto de 2020 do Learning Manager

Data de lançamento: 23 de agosto de 2020

### Novidades e alterações {#Whatsnewandchanged-3}

Esta versão concentra-se no seguinte:

* Aprimoramentos nos relatórios
* Pastas de conteúdo privado
* FTP personalizado
* Suporte de legenda para vídeos
* Power BI aprimoramentos
* Aprimoramentos de feedback
* APIs novas e alteradas
* Alterações na política de retenção de dados
* ...e muito mais

Para obter mais informações, consulte  [***Novidades do lançamento do Adobe Learning Manager em agosto de 2020***](../whats-new.md).

### Observações sobre esta versão {#notes}

* Gerar uma transcrição do aluno (~1 GB) leva menos de 15 minutos.
* Nas versões anteriores do Learning Manager, Pontuação do quiz das colunas de transcrição do aluno e Pontuação do quiz mais alta usadas para fornecer a pontuação e a pontuação máxima no formato 25/100. Para oferecer suporte a melhor legibilidade e análise, a pontuação do quiz agora também é exportada como colunas separadas - **Quiz_score, Quiz_score_max, Highest_Quiz_score e Highest_Quiz_score_max**. Isso permite que os administradores façam cálculos e análises rápidos.

### Erros corrigidos nesta atualização {#bug-fixes-2}

**Conector**

* Um aluno não pode participar de duas reuniões diferentes ao mesmo tempo, que são criadas por dois autores diferentes.
* Clicar na opção Gerenciar conexões do cartão do Adobe Connect navega para a página de conexão FTP.
* Uma sincronização de FTP agendada é encerrada com uma exceção.
* Há problemas relacionados à senha ao conectar-se ao Exavault.

**Curso**

* Você pode criar um módulo de sala de aula virtual sem selecionar nenhum sistema de conferência. Como efeito colateral, o processo de criação de um curso gera o Erro 500.
* Um aluno não pode baixar recursos mesmo que esteja inscrito em um curso, que foi duplicado.
* Ao visualizar um curso como aluno, um administrador ou autor não pode baixar recursos, a menos que esteja inscrito no curso.

**Aplicativo do dispositivo**

* Em casos de inscrição específicos, o gráfico de rosca em Meu aprendizado pendente exibe valores diferentes do aplicativo do aluno do navegador para o aplicativo móvel.

**Certificação**

* O Status do filtro de relatório não funciona conforme o esperado ao tentar baixar um relatório do painel para certificação.

**Pesquisar**

* Na página do catálogo do aluno, quando você tenta pesquisar um curso pela nota, nenhum resultado da pesquisa é exibido.

**SCORM**

* Para alguns conteúdos, o player SCORM exibe uma tela em branco.
* Um conteúdo de Storyline é identificado como um conteúdo de Captivate se o projeto publicado de Storyline contiver um objeto da Web apontando para a saída de Captivate publicada.
* O conteúdo SCORM não pode ser iniciado devido à URL incorreta.

**Função personalizada**

* Para certos cenários, um administrador personalizado não pode ver a lista completa de objetos de aprendizado.
* Um administrador personalizado não pode pesquisar um Programa de Aprendizado ou Certificação nos relatórios do painel.
* Um administrador personalizado não pode procurar um gerente em um painel.
* As transcrições do aluno geradas por um administrador personalizado não contêm dados de usuários excluídos.
* Um autor ou administrador personalizado não pode duplicar um Programa de aprendizado, um curso ou uma certificação.

**Relatórios**

* A coluna Tipo em uma transcrição do aluno exibe o valor como curso para os cursos que fazem parte de uma certificação, se o aluno não estiver inscrito na certificação.

**Habilidades**

* Ao adicionar uma habilidade para um curso, há alguns problemas ao procurar uma habilidade.

**Gamificação**

* Se muitos usuários forem tornados confidenciais, ao clicar na guia Aluno confidencial no Edge e no Exemplo da Internet, o navegador se comporta de forma inesperada.
* Quando a frequência de um critério é alterada, os pontos calculados com frequência mais antiga são adicionados ao cálculo atual.

**Administrador**

* Os alunos não podem ser marcados como participantes se a instância do curso mapeada para um programa de aprendizado for alterada.

**Modelos de e-mail**

* Para Programas de aprendizado e Certificações, o botão de alternância no modelo de e-mail está ausente.

**Biblioteca de conteúdo**

* O conteúdo SCORM não é iniciado como esperado devido à URL incorreta.

**Transcrições do aluno**

* Ao gerar transcrições do aluno, se você adicionar um aluno excluído na caixa de entrada Selecionar alunos e ativar a opção “Incluir dados de alunos excluídos” em Avançado, a página se comporta de forma inesperada.

**Pesquisar**

* Não é possível pesquisar um curso usando as suas notas.

**Relatórios do Excel**

* Se um relatório de trilha de auditoria do usuário levar mais de uma hora para ser baixado devido a dados grandes ou processamento lento, a conexão expirará e o relatório nunca será baixado.
* Em uma transcrição do aluno, a coluna Tipo é exibida como “Curso” em vez de “Certificação” para os cursos que fazem parte da certificação, se o aluno tiver a inscrição cancelada da certificação.

**Aplicativo do aluno**

* Um aluno pode fazer um curso ordenado de uma forma não ordenada acessando os cursos por meio de um e-mail de cancelamento de inscrição ou uma notificação de cancelamento de inscrição.
* Um aluno não recebia e-mails de lembrete de sessão conforme esperado.
* Um curso não é iniciado como esperado se um determinado módulo estiver ausente.

**Comunicados**

* Se um comunicado contém a tag <a>, o comunicado não é criado conforme esperado.

**Conta**

* Em alguns casos, as contas são desativadas mesmo que uma conta tenha uma OC válida.

**API**

* Se você clicar em Gerenciar conexões no cartão do Adobe Connect, será redirecionado para a página Conexão FTP.
* Para alguns cenários, o administrador do Connect recebe alertas incorretos.
* A migração do linkedIn Learning produz alguns erros.

### Problemas conhecidos nesta atualização {#known-issues-2}

**Relatórios do painel**

* Quando um Programa de aprendizado de certificação é excluído, o relatório Treinamento ativo exibe os cursos presentes no Programa de aprendizado ou na certificação, mesmo que o Programa de aprendizado ou a certificação não tenham inscrições.

+++

+++Atualização 54 - Aplicativo móvel

## Atualização 54 - Aplicativo móvel

Data de lançamento: 16 de abril de 2020

Para obter os recursos e atualizações mais recentes e uma melhor experiência, recomendamos que você atualize o aplicativo do dispositivo para a versão mais recente. A atualização é **obrigatório**.

### Recursos novos e aprimorados {#newandenhancedfeatures}

Um administrador pode comunicar informações importantes a todos os usuários do aplicativo. Os comunicados podem ser do tipo vídeo ou imagem ou uma mensagem de texto simples. Com esta versão do aplicativo do dispositivo, agora oferecemos suporte a comunicados no aplicativo do dispositivo. Um novo comunicado será exibido assim que o aplicativo for iniciado, para que os alunos não percam nenhuma comunicação importante enviada pelos administradores. Os alunos podem lê-lo instantaneamente ou ler mais tarde visitando o **Comunicados** guia.

Quando houver um ou vários comunicados, você poderá vê-los na seção **Comunicados** seção.

Para ver um comunicado, toque em **Comunicados**. O comunicado mais recente é exibido na tela.

Para ver o próximo comunicado, toque em **Deslize para a esquerda para a próxima**.

### Comunicados {#announcements}

![](assets/read-later.png)

Se você não quiser ler o comunicado nesse momento, sempre poderá optar por ler o comunicado mais tarde. Toque em **Ler mais tarde** no comunicado e o comunicado volta para o estado não lido.

### Erros corrigidos nesta atualização {#bugsfixedinthisupdate}

* No iOS, a reprodução de um podcast é interrompida quando a tela é bloqueada. O problema foi corrigido e o áudio será reproduzido mesmo quando a tela estiver bloqueada.
* Se você fizer um curso no aplicativo do dispositivo, o slide de resultados às vezes pode aparecer em branco. Esse problema foi corrigido nesta atualização.

+++

+++Atualização 53 - Versão de abril de 2020 do Learning Manager

Data de lançamento: 4 de abril de 2020

A versão de abril de 2020 do Learning Manager focou no seguinte:

* [Aprimoramentos de desempenho](../whats-new.md#performance)
* [Treinamento em sala de aula](../whats-new.md#classroom)
* [Fluxos de trabalho do gerente](../whats-new.md#manager)
* [Aprendizado social](../whats-new.md#social)
* [Relatórios](../whats-new.md#reporting)
* [Experiência do aluno](../whats-new.md#learner)
* [Alterações no nível da API](../whats-new.md#api)

Para obter mais informações, consulte [***Novidades no lançamento de abril de 2020 do Learning Manager***](../whats-new.md).

+++

+++Atualização 52 - Aplicativo móvel

## Atualização 52 - Aplicativo móvel

Data de lançamento: 20 de dezembro de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-1}

#### Logotipo de marca da empresa {#companybrandinglogo}

O aplicativo agora tem a capacidade de exibir o nome da marca, o logotipo da marca ou ambos no aplicativo do dispositivo, dependendo das configurações definidas pelo administrador.

#### Links profundos {#deeplinks}

O Learning Manager agora inicia o aplicativo do dispositivo assim que você clica em um link/URL suportado pelo Learning Manager. Caso o aplicativo não esteja instalado no dispositivo, o URL abre no navegador.

Veja alguns casos de uso com suporte nesta atualização.

* Clique em um URL de treinamento recebido em um e-mail.
* URLs de treinamento padrão que aparecem nos modelos de e-mail.
* URL da conta que aparece nos modelos de e-mail.
* Meus go-URLs de aprendizado e catálogo.

Além disso, qualquer URL com domínio *learningmanager.adobe.com* é aberto no aplicativo do dispositivo.

#### Carregar ativos no certificado externo como comprovante de conclusão {#uploadassetsinexternalcertificateasproofofcompletion}

Nesta atualização, um aluno pode fazer upload de ativos como prova de conclusão para um certificado externo.

Um aluno pode abrir um certificado externo e carregar ativos, como arquivos PDF, de texto ou de imagem.

Para obter mais informações, consulte  [***Carregar ativos no certificado externo***](../learners/feature-summary/ipad-android-tablet-users.md#externalcert).****

### Problemas corrigidos nesta versão {#issuesfixedinthisrelease}

* Um usuário não consegue fazer logon no aplicativo do dispositivo se o email contiver caracteres especiais.
* Ao rolar, o ícone do Objeto de aprendizado pisca quando você está em uma exibição de lista.
* Agora você pode exibir todas as notificações por push sem tocar no botão de seta para baixo e exibir as mensagens uma de cada vez.
* Ao clicar em uma notificação de uma publicação que foi aceita ou rejeitada na curadoria, uma página em branco é aberta no aplicativo. Nesta atualização, a página do quadro é aberta.

+++

+++Atualização 51

Nesta atualização, você também pode alterar a imagem do banner de um Objeto de aprendizado.

Você também pode personalizar o banner em uma página de Aprendizado social.

## Atualização 51

Data de lançamento: 17 de dezembro de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-2}

### Planos de aprendizado com escopo de funções configuráveis {#learningplansscopedbyconfigurableroles}

Você pode criar funções personalizadas para planos de aprendizado que permitem o escopo de usuários e objetos de aprendizado. Em outras palavras, os planos de aprendizado podem ser criados com um escopo limitado derivado do escopo de função de um administrador personalizado.

Agora, um administrador pode definir ou restringir o escopo ao conceder acesso ao gerenciamento do plano de aprendizado.

Para obter mais informações, consulte [***Planos de aprendizado com escopo de funções configuráveis***](../administrators/feature-summary/custom-role.md#scopeconfigure).

### Restringir campos ativos nos relatórios {#restrictactivefieldsinreports}

Para Campos ativos, adicionamos duas novas opções: **Reportável** e **Exportável**.

Para campos CSV e campos adicionados manualmente, se um campo ativo estiver marcado como **Reportável**, o Campo ativo se torna pesquisável em um filtro dentro de um relatório do painel.

Para obter mais informações, consulte  [***Restringir campos ativos nos relatórios***](../administrators/feature-summary/add-users-user-groups.md#restrictactivefields)***.***

### Exibir descrição do módulo de conteúdo {#viewdescriptionofcontentmodule}

Como autor, você pode ver a descrição dos módulos ao adicionar o módulo a um curso.

Ao criar um módulo, adicione sua descrição. Para saber mais sobre como criar um curso, consulte [***Criar um curso***](../authors/feature-summary/courses.md).

### Exibir nomes do curso e da sessão {#displaycourseandsessionnames}

Como professor, você pode ver os nomes das sessões e dos cursos na exibição Presença. Você pode controlar as sessões que estão sendo modificadas.

### Anúncio para alunos {#announcementforlearners}

Os alunos agora podem ver um comunicado na exibição completa em vez de na exibição em lista. Isso acontece quando o aluno tem um comunicado não lido. Isso aprimora a experiência dos alunos ao visualizar o comunicado.

O Adobe Learning Manager agora permite que você personalize sua conta para proporcionar uma experiência mais completa aos seus usuários. Veja uma lista de elementos que podem ser personalizados. Contato [Suporte do Learning Manager](mailto:learningmanagersupport@adobe.com)para fazer essas alterações.

* Cores do cartão de treinamento.
* Ícone de progresso
* Imagem do ponteiro do mouse
* Fonte

Para obter mais informações, consulte [***Personalizar sua conta***](../administrators/feature-summary/themes.md#customize).

### Fazer upload de imagens de banner {#uploadbannerimages}

Nesta atualização, você também pode alterar a imagem do banner de um Objeto de aprendizado.

Você também pode personalizar o banner em uma página de Aprendizado social.

### Suporte à API {#apisupport}

Esta atualização do Learning Manager inclui API para as seguintes operações:

**Baixar PDF de medalha**

Esta atualização inclui uma permissão para a API do aluno para baixar a PDF de uma medalha.

**Baixar transcrição do aluno**

Esta atualização inclui uma permissão para a API do aluno para baixar a transcrição do aluno.

**Baixar relatório do questionário**

Esta atualização inclui uma permissão para a API do administrador para baixar relatórios do questionário.

**Gamificação paginada**

A API do aluno agora permite a busca de todos os alunos e pontos de gamificação no escopo do aluno. Isso ajuda na criação de um quadro de classificação de gamificação.

**API:** `GET /users`

**Solicitar:** `GET\\ users?page[offset]=0&page[limit]=10&sort=id&filter=gamification`

**Resposta:** *A resposta incluirá os usuários classificados por ordem de pontos de gamificação.*

**Não incomodar**

Atualmente, apenas administradores podem adicionar usuários a uma lista do tipo Não incomodar por meio da interface do usuário. Após esta versão, um aluno poderá definir essas permissões para si mesmo por meio da API, desde que essa API esteja ativada pelo administrador. Habilitar essa API para uma conta requer uma configuração de back-end. Essa API permite que o aluno edite as permissões abaixo relacionadas aos e-mails.

* Direcionar e-mails para o aluno
* E-mails de escalonamento para gerentes de alunos
* Sobre subordinados diretos
* Sobre relatórios de nível ignorado

Para obter mais informações sobre as APIs do Learning Manager, consulte o seguinte:

* [***Referência da API***](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v2/)
* [***Guia do desenvolvedor da API***](<https://helpx.adobe.com/captivate-Learning> Manager/integration-admin/feature-summary/developer-manual.html)

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-1}

* Somente os usuários que pertencem a um grupo de usuários específico devem receber comunicados destinados a eles. Outros usuários não devem receber os comunicados.
* O reprodutor exibe um ícone giratório de carregamento antes que o conteúdo seja exibido.
* Os metadados do usuário nos relatórios causam uma Exceção de Ponteiro Nulo.
* Ao adicionar um professor para uma instância padrão do curso Connect VC, a mensagem, *“Nenhuma sessão para este módulo”*, é exibido na página Instância do curso no aplicativo do administrador.

* Exportar uma transcrição do aluno leva a um comportamento inesperado durante uma transferência FTP.
* O nome de um autor é exibido incorretamente nos cursos de um programa de aprendizado.
* As alterações na terminologia dos produtos das ajudas de tarefa não se refletem conforme esperado.
* O nome de um módulo é truncado se o nome for longo e exibido no modo retrato móvel.
* Não é possível criar uma instância para um curso mais antigo do Connect após atualizar a instância padrão com a implementação mais antiga do Connect.
* Um professor recebe um convite do calendário mesmo antes de o curso ser publicado.

+++

+++Atualização 50

## Atualização 50

Data de lançamento: 24 de outubro de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-3}

#### Criar função personalizada com vários escopos de catálogo {#createcustomrolewithmultiplecatalogscopes}

Como administrador, você pode restringir uma função personalizada com base em catálogos e grupos de usuários. Todos os usuários que pertencem a essas funções podem ver somente os objetos de aprendizado do catálogo em seu escopo. Esses usuários só podem executar ações que foram definidas no escopo de seus grupos de usuários.

Até o momento no Learning Manager, uma função personalizada pode estar no escopo de vários catálogos de um único grupo de usuários com permissões completas.

Nesta atualização do Learning Manager, você pode criar uma função personalizada que estará no escopo de vários catálogos e a cada catálogo será concedido um conjunto diferente de permissões. Para obter mais informações, consulte [***Escopo de função personalizada em vários catálogos***](../administrators/feature-summary/custom-role.md#multi-scope).

### Aprimoramentos para pesquisar {#enhancementstosearch}

**Plano de aprendizado**

Na página Planos de aprendizado de administradores e autores, agora há uma barra de pesquisa que pode ser usada para pesquisar qualquer plano de aprendizado.

![](assets/search-for-as-learningplan.png)

**Aplicativos de administrador e autor**

Nesta atualização do Learning Manager, como administrador ou autor, além de executar uma pesquisa com preenchimento automático, é possível realizar a pesquisa livre para pesquisar qualquer objeto de aprendizado.

### O filtro de pesquisa é preservado {#searchfilterispreserved}

Isso se aplica somente a um perfil do aluno.

Na guia **Catálogo** e **Meu aprendizado** páginas, um aluno pode aplicar um filtro no painel esquerdo, por exemplo, **Cursos** ou **Programas de aprendizado** e, em seguida, clica em um item Curso ou Catálogo.

![](assets/choose-learning-objects.png)

Quando o aluno volta para a **Catálogo** ou **Meu aprendizado** páginas usando o botão voltar do navegador, o filtro permanecerá preservado. O filtro que um aluno aplicou anteriormente não é mais redefinido.

### Controlar a visibilidade dos filtros de pesquisa {#controlvisibilityofsearchfilters}

Nas versões anteriores do Learning Manager, os administradores não tinham controle sobre as opções de visibilidade de um filtro do catálogo para que os alunos não vissem as habilidades e as etiquetas. Nesta versão do Learning Manager, o administrador pode filtrar tipos, habilidades e etiquetas de um catálogo.

No menu **Configurações** , para a categoria Mostrar painéis de filtro, ao clicar em **[!UICONTROL Editar]**, você verá as seguintes opções. As opções determinam os painéis de filtro visíveis para os alunos, para que eles possam ajustar os resultados da pesquisa.

Para obter mais informações, consulte [***Mostrar painéis de filtro***](../administrators/feature-summary/settings.md#filter-panels).

### Baixar QR Code do aplicativo do administrador {#downloadqrcodefromadministratorapp}

Nas atualizações anteriores do Learning Manager, os administradores personalizados enfrentavam problemas ao baixar um código QR. Nesta atualização, um administrador personalizado que tinha acesso a **Todos os alunos** e permissão para **Inscrição no curso** Você pode baixar o código QR.

O código QR ainda não está disponível para usuários de função personalizada, caso eles tenham permissões para o escopo limitado de usuários.

### Adicionar comentários ao inscrever alunos {#addcommentswhileenrollinglearners}

Como administrador ou gerente, você pode adicionar comentários ao inscrever alunos em um curso. Você pode mencionar informações adicionais sobre a coorte de usuários que está sendo inscrita. Esses dados são exportados nos relatórios do curso.

Para obter mais informações, consulte [***Adicionar comentários ao inscrever alunos***](../administrators/feature-summary/courses.md#enroll-comments).

### Suporte à sala de reunião persistente do Adobe Connect {#supportforadobeconnectpersistentmeetingroom}

No Adobe Connect, os clientes usam salas de reunião existentes que já criaram no Connect. Todas as salas de reunião no Connect são persistentes e os modelos de sala de reunião são cuidadosamente configurados para fornecer uma experiência unificada para cada sala persistente.

Nesta versão do Learning Manager, a integração com o Adobe Connect agora foi aprimorada para suportar salas permanentes também. Isso significa que agora você pode criar uma sessão de sala de aula virtual usando uma sala já criada no Adobe Connect.

Agora, o Learning Manager também permite que os alunos entrem na sala do Connect para suas sessões virtuais usando a autenticação SSO.

Para obter mais informações, consulte [***Suporte a sala persistente no Adobe Connect***](../integration-admin/feature-summary/connectors.md#persistent).

### Aviso antes de marcar presença se a duração da sessão for zero {#warningbeforemarkingattendanceifthesessiondurationiszero}

Um autor ou administrador pode criar uma sessão com duração de 0. É possível quando:

* a data de início e/ou a data de término estão vazias.
* a hora de início e/ou de término estão vazias.

Nesta atualização, um **mensagem de aviso, que indica que a duração de uma sessão é zero**, é mostrado ao administrador, gerente ou professor.

### Aviso se um módulo Sala de aula for criado sem adicionar dados de sessão {#warningifaclassroommoduleiscreatedwithoutaddingsessiondata}

Se um autor cria um curso adicionando um módulo de sala de aula ou sala de aula virtual, o autor pode optar por:

* Não adicione uma data de início/término e uma hora de início/término.
* Adicione uma data, mas não uma hora de início/término.
* Adicione uma data e uma hora de início.

Em todas as opções acima, quando um administrador, um gerente ou um professor marca a participação ou a conclusão, os valores da data de início da sessão e da data de término da sessão se tornam iguais, o que significa que, em uma transcrição do aluno, o valor Tempo gasto no aprendizado é exibido como zero.

Nesta atualização, um **mensagem de aviso, que indica que os dados da sessão estão incompletos**, é mostrado ao Autor.

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-2}

**Aplicativo do aluno**

* Um aluno não pode visualizar um curso em um programa de aprendizado se o curso tiver sido criado por um autor externo.
* Se um administrador adicionar uma publicação a um painel externo, a solicitação de curadoria vai para um SME interno, que é atribuído a essa habilidade.
* Um aluno não pode exibir o botão Iniciar ou Continuar após se inscrever nos cursos do LinkedIn.

**E-mail**

* Quando havia um grande número de usuários em uma lista DND de e-mail, o **Configurações** a página carregaria muito lentamente. Nesta atualização, a paginação é adicionada a uma lista de DNDs de email.
* Um professor recebe atualizações/emails de sessões das quais não faz parte. Nesta atualização, esse problema foi corrigido.

**Habilidades**

* Em uma transcrição do aluno, o tipo de valor de uma habilidade é exibido incorretamente como texto.

**Aplicativo móvel**

* No aplicativo móvel, um aluno podia exibir e se inscrever em uma instância do Plano de Aprendizado, que não era o comportamento pretendido. Nesta atualização, esse problema foi corrigido.

**Funções personalizadas**

* Como administrador personalizado, você não pode procurar um gerente em um relatório do painel.

**Várias tentativas**

* Em algumas situações, alguns módulos do curso não são exibidos aos alunos.

**Inscrição externa**

* Você não poderá alterar o perfil externo de um usuário se as licenças tiverem sido preenchidas para os perfis superiores.

### Problemas conhecidos nesta versão {#knownissuesinthisrelease}

* Nos navegadores mencionados abaixo, quando você passa o mouse sobre o painel esquerdo, o texto aparece após um pequeno atraso.

   * Edge 42.17134.1.0
   * Edge 44.17763.1.0
   * Internet Explorer 11.1006
   * Internet Explorer 11.615

* Um aluno tem permissão para entrar em uma sala de reuniões do Connect antes e depois da sessão.

+++

+++Atualização 49

## Atualização 49

Data de lançamento: 26 de agosto de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-4}

**Aprimoramentos de desempenho**

* A importação de usuários no sistema é mais rápida em comparação com as versões anteriores. Há uma melhoria significativa ao importar grandes dados do usuário.
* Para Gerentes e Administradores, as opções na lista suspensa Configuração do relatório foram modificadas para carregar os dados por demanda.
* O desempenho da API foi aprimorado. Muitas APIs agora devem ter um tempo de resposta aprimorado.
* O tempo necessário para gerar a transcrição do aluno foi aprimorado.
* Não há atraso nas páginas em que os alunos internos e externos estão listados, especialmente quando há um grande número de usuários.

**Privilégios especiais de usuário**

Um administrador pode conceder privilégios especiais a um grupo de usuários, usando quais membros do grupo podem participar de todos os painéis. Todas as restrições definidas na seção Configurações do escopo são ignoradas pelo grupo de usuários especial. Para obter mais informações, consulte [***Privilégios especiais de usuário***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#privilege).

**Alterações na interface do usuário**

* No menu **Adicionar relatório** caixa de diálogo, a **Período de tempo** e **Filtros** os seletores aparecem como seções separadas, que estão no estado recolhido, por padrão. Para obter mais informações, consulte [***Criar relatórios***](../administrators/feature-summary/reports.md#report).

* No menu **Adicionar relatório** , para um grupo de usuários, você pode usar a pesquisa com preenchimento automático para escolher um ou vários grupos de usuários. Para obter mais informações, consulte [***Relatórios de grupo de usuários***](../administrators/feature-summary/reports.md#user-group-reporting).

**Alterações nos valores das colunas Tempo**

Nas transcrições do aluno, nas colunas tempo, os minutos são arredondados para o minuto mais próximo e o valor do segundo é 00. Para obter mais informações, consulte [***Colunas de tempo***](../administrators/feature-summary/learner-transcripts.md#datetime).

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-3}

**Painel do aluno**

* Um Calendário de aprendizado exibiu o status **Sessão Inscrita** mesmo quando um gerente ainda não tinha aprovado a inscrição. Agora o status correto **Pendente** é exibido ao aluno até que o gerente aprove a inscrição.

* Em um caso específico, para uma sessão, o Calendário de aprendizado exibia o status **Inscrito** mesmo que o aluno tenha concluído um curso.

**Painel do gerente**

* Os gerentes não podiam controlar os treinamentos de conformidade da sua equipe se os membros da equipe estivessem inscritos por meio dos Planos de aprendizado.

**Pesquisar**

* Na visualização do professor, não era possível pesquisar um aluno.

**Interface do usuário**

* Para uma conta com alterações de taxonomia aplicadas, as alterações não foram refletidas conforme esperado nas notificações.

### Problemas conhecidos nesta versão {#Knownissuesinthisrelease-1}

* Usando a barra de pesquisa, não é possível pesquisar usuários excluídos na lista Usuários Externos. Como solução alternativa, role para baixo para exibir a lista de todos os usuários e localize o usuário necessário manualmente.
* Se um usuário especial publicar em um conselho externo, a solicitação de curadoria será recebida pelas SMEs no seu escopo.

+++

+++Atualização 48

## Atualização 48

Data de lançamento: 2 de agosto de 2019

### Recursos novos e aprimorados {#Newandenhancedfeatures-5}

**Separação de escopo no aprendizado social para usuários internos e externos** Um administrador pode definir escopos separados para alunos internos e externos. Há duas novas seções para usuários internos e externos. Em ambas as seções, você pode definir os escopos dos grupos de alunos. Para usuários internos, você pode definir os valores da Característica do usuário. Para usuários externos, você pode definir o perfil externo, no qual os alunos podem compartilhar o mesmo espaço social. Para obter mais informações, consulte [***Configurações do escopo***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#scopesettings).  **Social-Restringir criação de painéis sociais** Para restringir a criação de painéis por todos os alunos e moderar os painéis de forma eficaz, um administrador pode conceder permissões para criar painéis para um grupo seleto de usuários. O administrador pode restringir a criação de um painel a apenas um grupo selecionado e não a todos os alunos que participam do aprendizado social. Para obter mais informações, consulte [***Permissões de criação de painel***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#permission).  **Exibir apenas campos ativos vazios para os alunos** Um administrador pode optar por exibir os campos ativos ou ocultá-los depois que os valores forem preenchidos. Para obter mais informações, consulte [***Exibição do usuário***](../administrators/feature-summary/add-users-user-groups.md#activefields).  **Os usuários internos são excluídos após uma duração especificada de inatividade** Um administrador pode definir a duração (em dias) dentro da qual um aluno interno é excluído se ele permanecer inativo durante a duração especificada. Para obter mais informações, consulte ***[Excluir usuários automaticamente](../administrators/feature-summary/settings.md#autodelete)***.  **Personalizar links no rodapé** Um administrador pode adicionar e personalizar links no rodapé. Os links também podem ser personalizados para vários locais. O método existente de adicionar o link Entrar em contato com o administrador no rodapé também está disponível no **Links de rodapé** seção. Para obter mais informações, consulte [***Personalizar links do rodapé***](../administrators/feature-summary/settings.md#footer).

### Problemas conhecidos nesta versão {#Knownissuesinthisrelease-2}

* Links de rodapé personalizados não são exibidos para funções de administrador de integração.

+++

+++Atualização 47 - Aplicativo móvel

## Atualização 47 - Aplicativo móvel

Data de lançamento: 24 de julho de 2019

Usuários do Android:

Esta atualização também suporta as alterações necessárias para aderir às recomendações revisadas da Google para implementar notificações por push. Portanto, você não receberá mais **notificações** se você estiver usando a versão 2.7.4 ou anterior.

Para receber notificações, recomendamos atualizar para a versão 2.8.

### Recursos novos e aprimorados {#Newandenhancedfeatures-6}

**Aprendizado social**

Compartilhe sua experiência com colegas na forma de conteúdo gerado pelo usuário e publicado em painéis de discussão baseados em tópicos. Outros alunos interessados em habilidades semelhantes podem seguir esses painéis para aprender e até contribuir com o tópico, semelhante a uma plataforma de mídia social.

Compartilhe ideias e insights significativos em um ambiente informal. Curtir, descurtir uma publicação, fazer upload de conteúdo e comentar em publicações. Para obter mais informações, consulte [***Aprendizado social no aplicativo para dispositivos móveis***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Compartilhar mídia em um painel**

Compartilhe imagens, documentos ou arquivos de áudio ou vídeo com qualquer painel, para que outros membros do painel possam visualizar sua publicação e iniciar uma interação.  Para obter mais informações, consulte [***Compartilhar publicação***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Enviar arquivos para os módulos de sala de aula e atividade**

Envie arquivos como prova de conclusão do curso ao seu professor. O professor pode aprovar ou rejeitar o envio, com base no conteúdo do arquivo. Para obter mais informações, consulte [***Enviar arquivo para aprovação***](../learners/feature-summary/ipad-android-tablet-users.md#submitfile).

**Suporte atualizado da plataforma**

O aplicativo móvel Learning Manager agora é compatível com dispositivos Android 7 e acima e dispositivos iOS 10 e superior. Para obter mais informações, consulte [***Requisitos de sistema***](../system-requirements.md).

### Problemas conhecidos nesta versão {#Knownissuesinthisrelease-3}

1. No Android, não é possível fazer upload de um arquivo de GIF em uma publicação, comentário ou ao responder a um comentário.
1. Como moderador de qualquer painel, você não pode excluir publicações, comentários ou respostas de usuários. No entanto, você pode fazer o mesmo no aplicativo da Web.
1. No aplicativo, você não pode marcar um tipo de pergunta.
1. Depois de ativar o Aprendizado social no aplicativo, reinicie o aplicativo para exibir a guia **Aprendizado social**. Se você não vir Aprendizado social, interrompa o aplicativo e reinicie-o. A guia Aprendizado social estará visível.

+++

+++Atualização 46

### Recursos novos e aprimorados {#Newandenhancedfeatures-7}

## Atualização 46

Data de lançamento: 20 de junho de 2019

**Curadoria automática de conteúdo**

O aprendizado social permite dois métodos de curadoria do conteúdo publicado pelos alunos: **Sem curadoria** e **Curadoria manual**. Nesta versão, o Adobe Learning Manager aprimora o aprendizado social com recursos de curadoria automática por IA. Depois que o conteúdo é publicado, ele é analisado para identificar se ele pertence à habilidade para a qual foi publicado. Com base na pontuação de confiança, o conteúdo é publicado ao vivo ou enviado para curadoria manual. Para obter mais informações, consulte *[** Curadoria assistida automática **](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#autocuration)**.***

**Mapear habilidades com domínios de habilidades**

Mapeie habilidades em sua conta com os domínios de habilidades presentes no LMS do Learning Manager. Isso ajuda a vincular as habilidades da sua conta aos domínios de habilidades que o Learning Manager oferece suporte para curadoria assistida automaticamente. Para obter mais informações, consulte [***Mapear habilidades com domínios***](../administrators/feature-summary/curation-skills.md).

**Especificações do CSV e CSVs de amostra**

Especificações do CSV atualizadas que você pode usar para mapear os dados de migração do LMS existentes. Use as especificações de csv para download mais recentes e os arquivos zip de csvs de amostra para entender o formato prescrito dos dados a serem inseridos. Para obter mais informações, consulte  [***Manual de migração***.](../integration-admin/feature-summary/migration-manual.md)

### Problemas corrigidos nesta versão {#Issuesfixedinthisrelease-4}

**API do Learning Manager**

* Quando um perfil externo é adicionado usando o método POST da API *externalProfile*, o e-mail de boas-vindas não é exibido.

**Painel do gerente**

* Quando um gerente selecionou a opção **Este trimestre**, os detalhes de inscrição, progressão e conclusão de um Objeto de aprendizado não foram exibidos. Nesta versão, esses detalhes agora são exibidos conforme esperado.

**Alunos em lista de espera**

* Nas versões anteriores do Learning Manager, depois que um gerente inscrevia os alunos, quando um professor queria verificar se havia alunos na lista de espera, uma mensagem de erro era exibida. Nesta versão, um professor pode navegar na lista de alunos na lista de espera sem encontrar nenhuma mensagem de erro.

**Visão geral da certificação**

* Depois que um autor criou um curso e uma certificação que continha uma descrição e um conteúdo de visão geral, quando um aluno aterrissava na página do curso, o conteúdo da visão geral não era exibido conforme esperado. O conteúdo, no entanto, ficava visível nas páginas de visualização do aluno nos aplicativos Administrador e Autor. Nesta versão, o conteúdo da visão geral aparece conforme esperado no aplicativo do aluno.

**Catálogo**

* Para cada catálogo, um aluno pode visualizar todos os objetos de aprendizado. Nas versões anteriores, se qualquer catálogo não contivesse um Objeto de aprendizado, o catálogo ainda aparecia no início de outros catálogos. Nesta versão, todos os catálogos que não têm objetos de aprendizado aparecem na parte inferior dos catálogos.

+++

+++Atualização 45

Data de lançamento: 30 de maio de 2019

**Recursos novos e aprimorados**

* Pesquisa consolidada em todas as instâncias para alunos inscritos na seção Aluno do objeto de aprendizado. Pesquise usuários inscritos na seção Aluno do Objeto de aprendizado usando a pesquisa com preenchimento automático. Para obter mais informações, consulte [***Pesquisar usuários inscritos***](../administrators/feature-summary/courses.md#searchforusers).
* Recursos completos de edição de objetos de aprendizado adquiridos por meio do catálogo compartilhado. Para obter mais informações, consulte [***Controle de catálogo compartilhado***](../administrators/feature-summary/shared-catalog-full-control.md). Para ativar o recurso, entre em contato com o suporte do Learning Manager.
* Os professores agora podem identificar facilmente as sessões e os módulos com revisões pendentes. Para obter mais informações, consulte [***Revisões pendentes***](../instructors/feature-summary/learners.md#pending).

* As habilidades agora oferecem suporte à adjudicação de valores de crédito em formato decimal. Isso permite que os autores concedam um valor de crédito de nível decimal a um determinado curso. Para obter mais informações, consulte [***Suporte a decimais***](../administrators/feature-summary/skills-levels.md#decimal).
* Automatizar a criação de funções personalizadas. Para obter mais informações, consulte [***Configurar funções por meio de arquivos csv***](../integration-admin/feature-summary/configure-role-csv-files.md).
* Os envios necessários para certificações externas e módulos de atividade agora são opcionais. Isso permite que gerentes e professores avaliem sem um envio. Para obter mais informações, consulte [***Envio opcional***](../managers/feature-summary/learning-objects.md#optional).
* Baixar transcrições do aluno para usuários excluídos. Para obter mais informações, consulte [***Transcrições do aluno***](../administrators/feature-summary/learner-transcripts.md).
* Suporte para os seguintes idiomas:

   * Coreano
   * Turco
   * Holandês
   * Polonês

**Problemas conhecidos**

* O suporte decimal em créditos de habilidade é suportado somente em inglês.
* Para os idiomas coreano, japonês e russo, o valor do meridiano de tempo da sessão não é exibido conforme esperado.

**Problemas corrigidos nesta versão**

* As pontuações do quiz não são salvas para um programa de aprendizado ou certificação nas guias Participação e Pontuação.
* Um administrador ou gerente não pode marcar como concluída uma certificação externa.
* Na caixa de diálogo Transcrições do aluno, um administrador não pode selecionar um intervalo de datas personalizado se o idioma estiver definido como português ou espanhol.
* Um administrador não pode criar um perfil externo quando o idioma do perfil é o francês.
* Os campos ativos não estão visíveis na caixa de diálogo Editar usuário se o idioma não for o inglês.

+++

+++Atualização 44 - Aplicativo móvel

Data de lançamento: 26 de abril de 2019

* **Alterações na interface do usuário:** No aplicativo, o  ![](assets/hamburger.jpg) e a  ![](assets/search-magnifying-glass-icon.png) as opções agora aparecem na parte superior.

![](assets/1.png)

* **Digitalize o código QR para registrar:** Os recursos de QR Code foram aprimorados. Além do suporte à marcação de presença pelo código QR, agora ele também oferece suporte à inscrição em cursos e à marcação da conclusão de um curso com o código QR.

  Para se inscrever e concluir um curso, você pode digitalizar um código QR fornecido pelo administrador. Para obter mais informações sobre a digitalização de códigos QR na versão Web do Learning Manager, consulte  [***Digitalizar QR Code***](<https://helpx.adobe.com/captivate-Learning> Manager/whats-new.html#QRcodetoenrollcompleteenrollcompleteacourse).

* **Várias tentativas no curso:** O aplicativo Learning Manager permite que o aluno realize cursos com várias tentativas ativadas. Para obter mais informações sobre a configuração de várias tentativas, consulte  [***Várias tentativas***](<https://helpx.adobe.com/captivate-Learning> Manager/authors/feature-summary/courses.html#Multitentativas).

+++

+++Atualização 43

## Atualização 43

Data de lançamento: 28 de janeiro de 2019

* O tempo de aprendizado gasto por um aluno em um módulo pode ser contado várias vezes ao marcar a participação mais de uma vez. Esse problema foi corrigido.
* Marcar a presença de um objeto de aprendizado em uma sessão de vários dias pode exibir uma data de início incorreta da sessão para um aluno em uma transcrição de aprendizado. Esse problema foi corrigido.
* Os usuários podem não conseguir visualizar um curso quando o curso é adicionado a um programa de aprendizado ou certificação concluído. Esse problema foi corrigido.
* O registro de usuários pode ocorrer incorretamente quando eles são movidos para fora de um grupo de usuários. Esse problema foi corrigido.
* O aluno e o professor podem não receber um e-mail quando os detalhes da sessão são alterados no aplicativo do professor. Esse problema foi corrigido.
* O URL do Adobe Connect pode não funcionar corretamente quando &#39;/&#39; é fornecido no final do URL. Esse problema foi corrigido.
* Uma mensagem de erro pode ser exibida ao selecionar pelo menos um módulo obrigatório para um curso já publicado. Esse problema foi corrigido.
* Quando um aluno conclui um curso e este é marcado como obrigatório pelo autor, a conclusão do curso não pode ser marcada como concluída. Esse problema foi corrigido.
* O valor marcado de um módulo selecionado para um curso duplicado pode não aparecer instantaneamente. Ela só é exibida como um curso duplicado quando a página é atualizada. Esse problema foi corrigido.
* Todos os módulos serão exibidos como desmarcados no modo de edição após a publicação de um curso. A página precisa ser atualizada para ver as alterações. Esse problema foi corrigido.
* A seleção de um módulo obrigatório pode ter estado disponível para um curso ordenado quando não deveria ter sido. Esse problema foi corrigido.
* Um módulo obrigatório continua a aparecer na caixa de seleção suspensa mesmo depois de removê-lo durante a edição do curso. Esse problema foi corrigido.
* Os módulos Pré-trabalho e Teste podem ser marcados como obrigatórios por padrão. Esse problema foi corrigido.
* Ao clicar no link do feedback N3 no seu e-mail, o modal de feedback pode não abrir. Esse problema foi corrigido.
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

* Os administradores podem controlar a permissão concedida aos alunos para visualizar as pontuações do quiz nas transcrições do aluno. Isso pode ser ativado/desativado na página Configurações.
* A inserção de notificações do usuário pode falhar aleatoriamente, fazendo com que os emails associados não sejam entregues. Esse problema foi corrigido.
* Os dados do Tempo gasto no aprendizado podem não aparecer na transcrição do aluno e nos relatórios do painel. Esse problema foi corrigido.
* Informações sobre atividades, como inscrição/conclusão, podem não estar presentes na transcrição do aluno baixada por um gerente. Esse problema foi corrigido.
* Os módulos que fazem parte de um curso ainda em andamento podem aparecer como concluídos na transcrição do aluno. Esse problema foi corrigido.
* A transcrição do aluno pode não exibir os dados baixados de acordo com o intervalo de datas selecionado. Esse problema foi corrigido.
* Para usuários com somente a função de autor atribuída, os catálogos não podem ser exibidos. Esse problema foi corrigido.
* Quando um administrador de função personalizada baixa a transcrição do aluno, o relatório baixado não terá informações sobre os OAs que faziam parte apenas dos catálogos padrão. Esse problema foi corrigido.
* Pode ocorrer incompatibilidade no número total de usuários e na lista de usuários na página do grupo de usuários. Esse problema foi corrigido.
* O pop-up Programa de aprendizado pode não aparecer mesmo quando ativado e os usuários podem ser redirecionados para a página do OA. Esse problema foi corrigido.
* Quando a lista de espera é desmarcada e os alunos são inscritos em um curso, o administrador pode receber uma notificação por e-mail com o nome mencionado em vez do nome do aluno ser mencionado. Esse problema foi corrigido.
* O Sobrenome pode não aparecer na interface do usuário para um usuário adicionado por meio da API de usuário do POST. Esse problema foi corrigido.

+++

+++Atualização 40

Atualização 40

Data de lançamento: setembro de 2018.

Aprimoramento de desempenho

* Os usuários podem enfrentar problemas de tempo limite ao baixar grandes conjuntos de transcrições do aluno. Esse problema foi corrigido.
* Os usuários podem observar lentidão ao baixar um grande conjunto de relatórios de inscrição no qual a pontuação do questionário do aluno é registrada. Esse problema foi corrigido.
* O download de um conjunto grande de relatórios de pontuação do quiz pode demorar mais do que o normal. Esse problema foi corrigido.
* Quando o aluno conclui um programa de aprendizado, o formulário de feedback L1 pode não ser exibido automaticamente mesmo quando o pop-up automático é ativado pelo administrador. Esse problema foi corrigido.
* Nos relatórios baixados da trilha de auditoria do usuário e da trilha de auditoria do conteúdo, as colunas modificadas por nome de usuário e modificadas por email do usuário podem não ser registradas. O relatório mostra o sistema em tais instâncias. Este item foi atualizado para ser marcado como Desconhecido.

+++

+++Atualização 39

Data de lançamento: 19 de maio de 2018.

* Esta versão do Adobe Learning Manager traz novos recursos e aprimoramentos. Ele oferece a capacidade de criar funções personalizadas, adicionar rótulos de catálogo, limpar usuários, gerenciar tags, renomear objetos de aprendizado, integração de Slack, novas integrações de conector, suporte a xAPI e muito mais. Para obter mais informações sobre os novos recursos e aprimoramentos, consulte  [Resumo do novo recurso](../whats-new.md#main-pars_text).

* O Learning Manager está em conformidade com o GDPR. Para obter mais informações, consulte [Conformidade do Learning Manager com o GDPR](/help/migrated/kb/prime-gdpr.md).

## Problema conhecido {#knownissue}

* O hiperlink para o número de cursos e certificações dentro do modal de tags inclui cursos paralelos e certificações recorrentes. Ao clicar no hiperlink, esses cursos e certificações podem não estar listados, causando uma discrepância nos números.

+++

+++Atualização 38

* Os alunos no estado Pendente ou em estado de aguardando aceitação estavam sendo marcados como concluídos. Esse problema foi corrigido.
* Quando um professor pesquisa e seleciona todos os alunos, o número de alunos selecionados e a contagem mostrada têm disparidades. Esse problema foi corrigido.
* Quando você pesquisa e seleciona qualquer aluno e marca a participação, o Learning Manager pode marcar a participação de todos os alunos. Esse problema foi corrigido.
* O Learning Manager exibia o tempo em e-mails no formato de 24 horas. Esse problema foi corrigido. A hora agora é exibida no formato de 12 horas.
* Quando um gerente nomeia um aluno para um curso usando o botão Indicar disponível na página de notificações, o modal Indicar não era carregado. Esse problema foi corrigido.
* Nos relatórios exportados do Excel, a data do prazo, que deve ser a data de inscrição + dias para concluir o valor definido na instância automática dos OAs, seria exibida incorretamente. Esse problema foi corrigido.

* Os resultados da pesquisa de usuários são exibidos vazios quando não há usuários presentes no grupo pesquisado. Esse problema já foi corrigido.
* Os gerentes não podiam ser excluídos mesmo se não houvesse subordinados diretos. Esse problema foi corrigido. Os gerentes agora podem ser excluídos.
* A funcionalidade de progresso do módulo de redefinição pode parar de funcionar. Esse problema já foi corrigido.
* A certificação excluída pode aparecer no widget para alunos. Esse problema foi corrigido.
* O problema com o cálculo da eficácia do curso foi resolvido.

* O problema para integrar a nova conta do Connect foi corrigido.
* O pop-up automático de feedback L1 pode não aparecer se ativado em instâncias não padrão. O problema foi corrigido.
* O professor pode não ser capaz de marcar a participação de todos os usuários de uma só vez nas sessões que fazem parte do programa de aprendizado/certificação. Esse problema foi corrigido.

+++

+++Atualização 37

Data de lançamento: 25 de março de 2018

A versão de março de 2018 do Adobe Learning Manager traz novos recursos e aprimoramentos incríveis. Ele traz até você, geração de relatórios de trilha de auditoria de usuários e relatórios de logon/acesso, fornece aos alunos a capacidade de escolher instâncias do curso, aprimoramentos para salas de aula e salas de aula virtuais e muito mais. Esta versão também traz correções de erros e aprimoramentos de desempenho.

Para ler tudo o que há de novo nesta versão, consulte  [Novidades no Adobe Learning Manager](../whats-new.md).

### Problema conhecido {#KnownIssue-1}

**Problema:** Acessar alguns objetos de aprendizado específicos que usam o Internet Explorer v11.1478.10586.0 pode travar o Learning Manager.

**Solução alternativa:** Atualize o navegador Internet Explorer 11 para a versão mais recente entrando em contato com a equipe de TI da sua empresa.

+++

+++Atualização 36

Data de lançamento: 22 de janeiro de 2018.

### Problemas corrigidos {#issuesfixed}

* Fazer qualquer alteração na configuração do modelo de email pode levar ao desaparecimento do banner de email. Esse problema foi corrigido.
* Os alunos podem não conseguir adicionar/iniciar ajudas de tarefa privadas. Esse problema foi corrigido.
* Grupos de usuários personalizados presentes em uma conta podem não estar listados no campo de grupo de usuários no modal Adicionar/editar relatório. Esse problema foi corrigido.
* Se uma imagem de medalha tiver espaço no nome, talvez ela não seja exibida para o aluno na página inicial.
* Quando um usuário inscrito é excluído de um curso, o relatório do curso e o relatório do questionário podem não ser gerados para esse curso específico. Esse problema foi corrigido.
* Se o administrador alterar o número de vagas indicadas para um gerente, a contagem pode parecer incorreta na solicitação de indicação quando aberta em diferentes lugares. Esse problema foi corrigido.
* Ao converter um usuário externo em um usuário interno, o usuário podia não ser adicionado ao grupo Todos os alunos internos. Esse problema foi corrigido.
* Se você pesquisar um aluno individual, selecioná-lo e executar a ação de cancelamento de inscrição, pode resultar no cancelamento da inscrição de todos os alunos nesse grupo em vez de apenas do selecionado. Esse problema foi corrigido.
* Como administrador, você pode não conseguir usar a caixa de seleção para selecionar um aluno dentro das certificações. Esse problema foi corrigido.
* A criação e atualização de grupos de usuários com mais de 600 usuários individuais podem falhar. Esse problema foi corrigido. Agora você pode criar grupos de usuários com mais de 600 usuários individuais.
* Se você excluir um grupo de usuários personalizado que faz parte de outro grupo de usuários personalizado, a regra de interseção poderá passar o número de usuário para o grupo superior. Esse problema foi corrigido.
* Quando o catálogo padrão é desativado e um novo catálogo é criado, e se o gerente tiver acesso a esse catálogo recém-criado, ele pode não ser capaz de pesquisar qualquer curso sob esse catálogo. Esse problema foi corrigido.
* Os usuários de aplicativos móveis podem não receber feedback L1 como notificações por push. Esse problema foi corrigido.

+++

+++Atualização 35

Data de lançamento: 7 de janeiro de 2018.

Esta versão do Learning Manager traz a você otimizações de desempenho voltadas para melhorar a escalabilidade, o desempenho e a segurança.

### Aprimoramentos {#enhancements}

* Experimente a pesquisa elástica ao pesquisar cursos e usuários em todos os aplicativos. Isso inclui a pesquisa de cursos, usuários e grupos de usuários.
* Suporte ao uso do conector Box para integrar o Learning Manager aos sistemas externos a fim de automatizar a sincronização dos dados. Para obter mais informações, consulte [Conector da caixa](../integration-admin/feature-summary/connectors.md#main-pars_header_302653946).
* Especificações do CSV atualizadas que você pode usar para mapear os dados de migração do LMS existentes. Use as especificações de csv para download mais recentes e os arquivos zip de csvs de amostra para entender o formato prescrito dos dados a serem inseridos. Para obter mais informações, consulte [Manual de migração.](../integration-admin/feature-summary/migration-manual.md)

+++

+++Atualização 34

### Problemas corrigidos {#IssuesFixed-1}

* Os comunicados podem falhar quando o número de usuários é alto. Esse problema foi resolvido.
* Acessar a conta do Learning Manager usando o URL de subdomínio na UE poderia redirecionar os usuários para uma página diferente. Esse problema foi resolvido.
* Quando um LP é solicitado, um aluno pode consumir o LP somente na ordem especificada. Os alunos podiam consumir cursos que não eram listados primeiro usando os hiperlinks do curso. Esse problema foi corrigido. Os alunos não podem mais iniciar um curso até que ele termine o anterior.

* A mensagem de erro de versão incompatível do navegador pode não aparecer em versões incompatíveis do Internet Explorer ( IE 7, IE 8, IE 9 e IE 10) e Safari ( versões 7, 8 e 9). Esse problema foi corrigido.



+++

+++Atualização 33

Data de lançamento: 5 de outubro de 2017.

### Problemas corrigidos {#IssuesFixed-2}

* As alterações feitas em um curso compartilhado podem não ser propagadas para a conta compartilhada se o autor na conta de origem salvar automaticamente o curso. Esse problema foi corrigido.
* Às vezes, em projetos específicos do Learning Manager, o conteúdo costumava congelar no Fluidic Player. Esse problema foi corrigido.

* A listagem de calendário no widget Calendário de aprendizado no painel do aluno pode aparecer em uma ordem aleatória. Esse problema foi corrigido. A listagem agora aparecerá de forma ordenada.
* Ao marcar a participação usando a opção selecionar tudo, os alunos são marcados como participantes nos objetos de aprendizado da mesma sessão. Esse problema foi corrigido.
* Em determinadas telas de alta resolução, o e-mail recebido do Learning Manager tinha problemas de alinhamento e truncamento na imagem e no texto do banner. Esse problema foi corrigido.
* Determinados e-mails do Learning Manager, como e-mails sem dados de notificação, não estavam sendo acionados para os usuários. Exemplo - Email recebido ao criar e ativar o perfil externo e Email recebido ao configurar a conta do Connect. Esse problema foi corrigido.
* Ao criar uma LP, definir um lembrete, inscrever usuários e, em seguida, alterar o prazo da instância, o prazo alterado pode não ser refletido nos lembretes. Esse problema foi corrigido. Os lembretes agora carregariam o prazo alterado.
* Em certos casos, para o conteúdo criado usando o Adobe Presenter, o tempo total e o tempo decorrido no fluidic player não estavam em sincronia com o conteúdo. Esse problema foi corrigido.
* Em certos casos, depois de adicionar um programa de aprendizado a um catálogo, a opção de adicionar ainda podia estar ativada. Esse problema foi corrigido.
* Abrir o Learning Manager em um navegador do dispositivo exibe uma opção para experimentar o Learning Manager no aplicativo do dispositivo. Clicar em sim deve iniciar a Play Store (Android) se o aplicativo não estiver instalado ou iniciar o aplicativo se instalado (no Android e no iOS). Este fluxo de trabalho tinha problemas e foi corrigido.

+++

+++Atualização 32

Data de lançamento: 17 de agosto de 2017

### Problemas corrigidos {#IssuesFixed-3}

**Curso com várias versões de um módulo volta para a versão anterior na ação de exclusão.**

Quando um curso tem várias entradas de versão de módulo para módulos específicos, ao excluir o módulo, ele reverteria para a versão anterior e não seria excluído completamente. Esse problema foi corrigido.

**As alterações feitas em um curso compartilhado não seriam propagadas se ele fosse salvo automaticamente ao mover-se pelas guias.**

As alterações feitas em um curso compartilhado podem não ser propagadas para a conta do locatário se o autor, na conta principal, salvar automaticamente o curso indo para a próxima guia. Esse problema foi corrigido.

**Os usuários não conseguiam alterar o prazo de conclusão das instâncias de um curso somente de atividade.**

Os usuários não conseguiam alterar o prazo de uma instância nos cursos de atividade, pois isso reverteria para a data de prazo anterior. Esse problema foi corrigido.

**Impossibilidade de usar uma ID exclusiva depois de removida de um objeto de aprendizado.**

Ao atribuir uma ID exclusiva a um curso e removê-la, você não poderá usá-la novamente. Esse problema foi corrigido.

**Um programa de aprendizado que já está inscrito como parte de um evento de plano de aprendizado pode aparecer como parte de outro evento no aplicativo do aluno.**

Se um programa de aprendizado já estiver inscrito como parte de um evento de plano de aprendizado, ele pode aparecer como parte de outro evento no aplicativo do aluno. Esse problema foi corrigido.

**O aluno recebe e-mails de lembrete com data de conclusão/hora da sessão especificados incorretamente.**

Os alunos geralmente recebiam e-mails com lembretes de prazo incorretos/lembretes de tempo da sessão devido a correções de fuso horário. Esse problema foi corrigido.

**O cronograma do quadro de classificação da gamificação mostra alunos externos se forem convertidos de aluno externo a aluno interno.**

A linha do tempo do quadro de classificação de gamificação interna de um aluno pode mostrar um aluno externo quando ele é convertido de externo para um aluno interno. Esse problema foi corrigido.

**O campo UUID de um aluno é exibido no formato editável ao criar usuários únicos e CSV em uma conta habilitada para UUID.**

O campo UUID era exibido ao aluno ao concluir seu perfil, mesmo quando o administrador fornecia a UUID para usuários únicos e CSV. Esse problema foi corrigido.

**O tempo de aprendizado gasto não está sendo captado nos relatórios em alguns casos.**

O tempo de aprendizado gasto não estava aparecendo nos relatórios de um aluno,

* Se a sua presença for marcada automaticamente pelo sistema para os módulos de conexão.
* Quando um código QR era digitalizado para os módulos CR e VC usando o aplicativo Learning Manager do dispositivo.

**Esta versão do Learning Manager também introduziu aprimoramentos e correções de erros relacionados ao reprodutor do dispositivo.**

* Problemas relacionados à conclusão dos módulos de atividade. Esse problema foi corrigido.
* Quando o aluno reproduz um vídeo no modo retrato, os botões +10 e -10 podem não funcionar. Esse problema foi corrigido
* Melhoria na experiência de reprodução de determinados projetos de amostra quando reproduzidos em um dispositivo Android (móvel e tablet), o que anteriormente podia ocorrer uma reprodução trêmula.
* Ao adicionar uma nova nota, o painel de notas deve ser fechado e a reprodução deve continuar no reprodutor. Isso pode não acontecer em certos casos. Esse problema foi corrigido.
* Ao abrir as notas adicionadas a um módulo, o botão Fechar pode não ser exibido. Esse problema foi corrigido.
* Quando o aluno abre o painel &#39;Notas&#39; usando o marcador de notas, pode ser necessário clicar duas vezes no ícone de notas para fechar o painel.
* Quando clicado no sumário, ele pode não ser recolhido automaticamente e precisa de fechamento manual para exibir o conteúdo. Esse problema foi corrigido.
* Um curso que tem um módulo com vários idiomas pode não exibir todos os idiomas disponíveis, pois a barra de rolagem pode não ser dimensionada de acordo. Esse problema foi corrigido.
* Ao abrir um módulo de curso de atividade de terceiros em um reprodutor no modo paisagem, a orientação do texto pode não se ajustar, dificultando a rolagem. Esse problema foi corrigido.
* Aumentada a área de toque do botão Fechar do reprodutor no modo online e offline.
* O sumário não fecha automaticamente quando a orientação do dispositivo é alterada. Esse problema foi corrigido.
* Alguns problemas menores relacionados à interface do usuário, como o alinhamento do botão Play, do botão de opção e de outras configurações nos modos paisagem e retrato, foram corrigidos.

* O problema da barra de busca ser exibida mesmo quando a opção mostrar controle de reprodução está desmarcada no conteúdo foi corrigido.
* O botão Fechar do reprodutor não estava visível para determinados projetos quando a orientação do dispositivo era alterada. Esse problema foi corrigido.
* O problema em relação à seção do sumário do módulo sendo truncado no modo paisagem no player do dispositivo foi corrigido. Em certos casos, o sumário não era visível para o conteúdo no player do dispositivo. Isso também foi corrigido.

**Esta versão do Learning Manager também trouxe os aprimoramentos e correções listados abaixo para o aplicativo do dispositivo**.

* As notificações por push relacionadas aos prazos de conclusão podem não ser entregues em determinados dispositivos. Esse problema foi resolvido.
* Agora também oferecemos suporte ao ciclo de vida do objeto de aprendizado no aplicativo do dispositivo. Os alunos agora podem acessar o conteúdo mais recente nos objetos de aprendizado se tiverem sido editados pelo autor.

* Os problemas de orientação do aplicativo (incluindo a orientação padrão - modo retrato) foram corrigidos.
* Talvez não haja uma opção para atualizar o conteúdo quando o usuário fizer a transição do modo offline para o modo online.
* A solicitação de módulos agora é compatível com cursos no aplicativo do dispositivo no modo online.

* Se um usuário não tiver baixado nenhuma ajuda de tarefa, clicar na guia Minhas ajudas de tarefa no modo offline poderá travar o aplicativo no IOS e mostrar uma mensagem dizendo erro ao carregar dados no Android. Isso foi resolvido.
* O aplicativo Learning Manager fecha ou exibe um erro se o curso for acessado imediatamente depois de desativar a Internet, mesmo se for um curso baixado. Agora esse problema foi corrigido.
* Às vezes, ao digitalizar o código QR, ele exibe uma imagem capturada da digitalização de código QR anterior. Isso foi corrigido.
* Tentar remover uma ajuda de tarefa que já foi adicionada da guia ajudas de tarefa em certas ocasiões mostraria uma mensagem de erro. Esse problema foi corrigido.

+++

+++Atualização 31

Data de lançamento: 16 de julho de 2017

### Aprimoramentos {#Enhancements-1}

**Gamificação**

Esta versão aprimora o escopo da gamificação. Os usuários externos agora podem participar da gamificação. Como administrador, você pode definir o escopo da gamificação alterando as configurações do escopo. É possível ativar de forma seletiva a gamificação entre usuários, grupos ou locais de perfil semelhantes.

**Aprimoramentos em usuários externos**

Com esse aprimoramento, você pode definir um intervalo de tempo após o qual os usuários são excluídos automaticamente após o período de inatividade. O aprimoramento também permite que o administrador adicione novamente o usuário como um aluno externo para alunos excluídos automaticamente e excluídos manualmente.

**Ajuda de tarefa, comunicados e relatório de cancelamento de inscrição**

Ajudas de tarefa são conteúdos de treinamento que um aluno pode acessar sem ter de se inscrever em qualquer objeto de aprendizado específico, como um curso ou programa de aprendizado. Com esse aprimoramento, os administradores podem extrair e baixar o relatório de ajudas de tarefa. Como administrador, você também pode gerar um relatório de todos os comunicados enviados por você. Os administradores e gerentes também podem extrair um relatório dos alunos cuja inscrição foi cancelada.

**Conectores do Learning Manager**

Agora você pode exportar habilidades do usuário para um local FTP para integração com qualquer sistema de terceiros usando a opção Exportação de dados. Você pode especificar o Nome da conexão para sua integração e escolher se deseja importar usuários internos ou exportar habilidades do usuário configurando-os ou buscando-os sob demanda.

**Copiar instâncias do curso**

Agora você pode copiar o URL da instância clicando na seta suspensa no canto superior direito de uma instância.

### Problemas corrigidos {#IssuesFixed-4}

**Usuários que não recebem convite do calendário ao ser inscrito no programa de aprendizado**

Às vezes, os usuários não recebiam o convite do arquivo de convite do calendário (.ics) ao se inscreverem em Programas de aprendizado, Certificados com sala de aula e sessões do Connect. Esse problema foi corrigido. Os usuários agora receberão arquivos .ics como anexos que mencionam os detalhes da sessão junto com o e-mail de inscrição.

**A descrição da atividade, mesmo se fornecida em vários idiomas, ainda podia ser exibida em inglês**

Um usuário cuja preferência de idioma do conteúdo esteja definida como diferente de inglês ainda poderá ver a descrição do módulo Atividade em inglês. Esse problema foi corrigido.

+++

+++Atualização 30

Data de lançamento: 30 de junho de 2017

### Aprimoramentos {#Enhancements-2}

**Vários objetos de aprendizado são compatíveis com o plano de aprendizado**

Como administrador ou autor, agora você pode atribuir vários objetos de aprendizado a um plano de aprendizado. Se qualquer instância do objeto de aprendizado for desativada ou expirar, todo o plano de aprendizado será desativado automaticamente. Com esse aprimoramento, você também pode pesquisar **[!UICONTROL Aprendizado Concluído]** e **[!UICONTROL Atribuir aprendizado]** usando IDs exclusivas de objetos de aprendizado.

**Acessibilidade**

Com esta atualização, o Learning Manager Learner Experience agora é compatível com o padrão de acessibilidade da seção 508. O Learning Manager também é compatível com a versão mais recente do **[!UICONTROL JAWS]**. Esse recurso é suportado apenas para o aplicativo do aluno. Use o Internet Explorer 11, o Windows Chrome ou o macOS Safari para acessar esse recurso.

### Problemas corrigidos {#IssuesFixed-5}

**Informações incorretas em determinados fusos horários**

Os lembretes de prazo mencionavam o número de dias restantes incorretamente para os alunos em determinados fusos horários. Esse problema foi corrigido.

**Problemas do Programa de aprendizado no caso de programas expirados**

A inicialização de módulos do Programa de aprendizado tinha problemas se a instância do Programa expirasse. Isso levou à expansão do módulo sem funcionar e os alunos não conseguiram iniciar o reprodutor e visitar o conteúdo. Esse problema foi corrigido.

**Problemas de tradução no aplicativo do aluno**

Os usuários do Learning Manager tiveram alguns problemas de tradução no aplicativo do aluno. Esses problemas foram corrigidos.

**Problemas relacionados à assinatura de uma habilidade**

Em certos casos, os alunos não podiam se inscrever em uma nova habilidade. Esse problema foi corrigido.

+++

+++Atualização 29

Data de lançamento: 9 de abril de 2017

### Novos recursos {#newfeatures}

Para obter uma lista dos novos recursos e aprimoramentos da versão de abril do Learning Manager, consulte [Novidades.](../whats-new.md)

**Aplicativo para aluno baseado em widget**

Use widgets na página inicial para gerenciar cursos, habilidades e conquistas. Use a barra de pesquisa para executar uma pesquisa em todo o LMS que abrange todos os objetos de aprendizado, catálogos, habilidades, notas e discussões

Para obter informações detalhadas sobre a nova home page, consulte  [Página inicial do aluno no Learning Manager](../learners/feature-summary/getting-started-learner.md).

**Configurações do administrador para o painel do aluno**

Como administrador, você pode controlar a página inicial do aluno ativando e desativando diferentes widgets.

**Aplicativo móvel do Learning Manager para alunos**

O novo aplicativo móvel do Learning Manager permite que os alunos usem o aplicativo para se inscreverem e realizarem cursos. O aplicativo também pode ser usado para gerenciar painéis.

Para saber mais sobre a utilização do Learning Manager em dispositivos móveis, consulte  [Aplicativo do aluno do Learning Manager para dispositivos móveis](../learners/feature-summary/ipad-android-tablet-users.md#main-pars_header_1451175907).

**Marcar participação usando o código QR**

Use o código de digitalização QR para marcar sua presença nas sessões de sala de aula usando dispositivos móveis.

**Função de professor**

O Learning Manager agora apresenta professores para os módulos. Os professores podem gerenciar as sessões do módulo, incluindo a hora, o local e o limite de vagas dos módulos atribuídos a eles.

Para exibir informações detalhadas sobre os professores, consulte  [Professores no Learning Manager](../instructors/feature-summary/getting-started.md#main-pars_header).

**Conta entre parceiros**

Se você for um administrador, poderá criar contas entre parceiros com quem poderá compartilhar as suas licenças compradas.

Para saber como criar e gerenciar contas entre parceiros, consulte  [Contas entre parceiros](../administrators/feature-summary/peer-account.md#main-pars_text).

**Ofertas de equivalência de curso**

Uso **[!UICONTROL Adicionar novo idioma]** opção quando você adiciona um módulo ou um curso para torná-lo disponível em vários idiomas e formato.

**Transcrição do aluno**

O Learning Manager oferece aos administradores e gerentes a capacidade de baixar os dados da transcrição para controlar o histórico de aprendizado dos indivíduos e das equipes.

**Integração com outros provedores de conteúdo**

O Learning Manager introduziu três novos conectores nesta versão, para que os alunos possam acessar e realizar cursos dos seguintes provedores de conteúdo: Lynda.com, getAbstract e Harvard ManageMentor.

Para saber como configurar e usar cada um desses conectores, consulte  [Conectores](../integration-admin/feature-summary/connectors.md#main-pars_header).

**ID exclusiva dos objetos de aprendizado**

Ao criar objetos de aprendizado, agora os autores e os administradores podem especificar IDs exclusivas para os cursos, programas de aprendizado ou certificações. Se quiser ativar a ID exclusiva ao criar um objeto de aprendizado, clique em Configurações > Geral. Marque a caixa de seleção Ativar ao lado da opção Ids exclusivas do objeto de aprendizado.

**Quadro de discussão dos alunos**

Use o quadro de discussão dos cursos para interagir com colegas e professores. Como aluno, você pode ver todas as publicações dos cursos. No entanto, você também pode excluir apenas as publicações inseridas. Para obter mais informações sobre o Quadro de discussão, consulte  [Exibindo e participando de discussões](../learners/feature-summary/courses.md#main-pars_header_1772461149).

### Aprimoramentos {#Enhancements-3}

**X de Y cursos**

Os critérios de conclusão para objetos de aprendizado, como cursos, certificações e planos de aprendizado, podem ser definidos de modo que os alunos precisem concluir apenas X de Y módulos ou cursos. Os autores também podem definir os critérios de conclusão para certificações e planos de aprendizado.

Para obter mais informações sobre esse recurso, consulte  [Critérios de conclusão do curso](../learners/feature-summary/courses.md#main-pars_image_1164377098).

**Moderação do curso**

Os administradores agora recebem notificações sempre que um autor edita ou atualiza módulos e publica novamente um curso.

**Configurações do administrador para redefinir módulos**

Agora, os administradores têm a capacidade de configurar a opção Redefinir módulo para permitir que os alunos redefinam um curso com falha ou incompleto.

**Catálogo de Relatórios**

Ao criar relatórios no Learning Manager, agora você pode gerar relatórios e gráficos dos catálogos.

**Aprimoramentos do plano de aprendizado**

Os administradores agora podem criar Planos de aprendizado dos tipos Na data. Com o plano de aprendizado na data, um administrador pode especificar o nome do evento, escolher a data para o evento e selecionar o grupo de usuários ao qual o evento pertence.

**Mensagens de inscrição específicas ao curso**

Agora, os administradores podem configurar e enviar mensagens de inscrição específicas ao curso através de e-mail para os alunos.

**Comunicados pop-up**

Como administrador, agora você pode habilitar o recurso Pop-up para comunicados.

**Suporte para URL em comunicados**

Você pode adicionar URLs como comunicados adicionando o URL no HTML.

**Adicionar novos tipos de entrega (cursos)**

O Adobe Learning Manager agora permite adicionar tipos de entrega dos cursos.

**Aprimoramentos na função de autor**

Os autores anteriores só podiam criar módulos e cursos. Agora, os autores também podem criar certificações e programas de aprendizado para os alunos.

**Função de autor para usuários externos**

Como administrador, agora você pode atribuir funções de autor a usuários externos.

**Vários autores**

O Learning Manager agora permite que vários autores editem simultaneamente o mesmo grupo de conteúdo.

**Aprimoramentos do Adobe Connect**

Agora você pode configurar um único URL do Adobe Connect com várias contas do Learning Manager.

**Suporte para novos idiomas**

Esta versão oferece suporte para japonês, português (brasileiro) e italiano.



+++

+++Atualização 28

Data de lançamento: 30 de janeiro de 2017

### Problemas corrigidos {#IssuesFixed-6}

#### Configurações da conta {#accountsettings}

Como administrador, quando você clica em Perfil externo e escolhe Ações > Alterar perfil, todos os perfis não são listados. Agora esse problema foi corrigido.

#### Ciclo de vida do curso {#courselifecycle}

* Ao iniciar um curso criado com a ferramenta de e-learning da biblioteca do Biz, a ação “Retomar” não funcionava. Esse problema foi corrigido.
* Alguns usuários não conseguiam iniciar um curso no iPad usando o link do curso em Comunicados. Esse problema já foi corrigido.
* Ao clicar no botão Continuar no programa do aluno, você não podia acessar os cursos na ordem. Esse problema já foi corrigido.
* O rótulo Visão geral do curso para os cursos no programa do aluno foi colocado anteriormente no lugar errado. Agora esse problema foi corrigido.

#### Aplicativo do aluno {#learnerapp}

* No dispositivo, se você abrir uma imagem de comunicado em modo de tela inteira, não será possível voltar ao aplicativo. Isso já foi corrigido.
* O conteúdo Tincan carregado do Captivate não era reproduzido no modo online nos sistemas operacionais Android e iOS. Esse problema foi corrigido.

#### Relatórios do curso {#coursereports}

São gerados relatórios incorretos de transcrição do aluno no Learning Manager quando o curso tem várias versões dos módulos. Esse problema já foi corrigido.

#### Camada da API {#apilayer}

Você encontra um erro sempre que tenta obter as informações de versão do módulo usando AP/courses/{coursesid}. Esse problema já foi corrigido.

+++

+++Atualização 27

Data de lançamento: 23 de dezembro de 2016.

### Novos recursos {#Newfeatures-1}

O Adobe permite que as empresas migrem os dados de treinamento e o conteúdo do treinamento da sua organização dos seus sistemas de gerenciamento de aprendizagem (LMS) existentes para o aplicativo de LMS do Learning Manager.

O Learning Manager fornece as ferramentas e modelos necessários para que o administrador de integração da sua organização possa configurar e executar as tarefas de migração.

Para obter mais informações sobre o recurso Migração, consulte  [Ajuda manual de migração](../integration-admin/feature-summary/migration-manual.md)

### Aprimoramentos {#Enhancements-4}

**Registro de usuário**

Como administrador, agora você pode adicionar nomes de domínio específicos ao adicionar usuários externos. Quando os alunos se registram na conta, eles podem inserir endereços de e-mail apenas a partir desses nomes de domínio.

Você também pode enviar links de verificação por email para o email dos usuários quando eles se registrarem na conta. Para obter mais informações sobre esse aprimoramento, consulte  [Adicionar usuários/grupos de usuários](../administrators/feature-summary/add-users-user-groups.md#main-pars_header_1217981931).

**Fluidic Player**

O Fluidic Player agora permite que você modifique a velocidade de reprodução. Você pode escolher entre cinco variantes de velocidade disponíveis. O Fluidic Player também permite que você controle as configurações de volume ao fazer um curso.

Como aluno, você também pode avançar ou retroceder 10 segundos usando os novos ícones em ambos os lados do botão de reprodução no Fluidic Player. Para obter mais informações sobre esses aprimoramentos, consulte  [Fluidic Player](../learners/feature-summary/fluidic-player.md).

Os aprimoramentos do Fluidic Player são aplicáveis somente a vídeos.

+++

+++Atualização 26

Data de lançamento: 6 de dezembro de 2016.

### Aprimoramento {#enhancement}

Como parte desta atualização, o Learning Manager fornece um ponto final [PATCH/users/{id}](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v1/#!/user/patch_users_id) para atualizar usuários em um aplicativo. Você pode acessar esse ponto final da API na função Administrador. Ao usar****este ponto final, você pode atualizar as seguintes informações dos usuários do Learning Manager:

* Nome
* E-mail
* Perfil
* Função
* Gerente

### Problema corrigido {#issuefixed}

**Fluidic player**

Quando você faz um curso desenvolvido em Captivate usando  `code cpQuizInfoStudentName` , o nome do aluno não aparecia conforme esperado. Esse problema foi corrigido.

+++

+++Atualização 25

Data de lançamento: 17 de novembro de 2016.

### Aprimoramentos {#Enhancements-5}

**Catálogos compartilhados**

O recurso Catálogo compartilhado permite que os administradores de contas compartilhem ou adquiram catálogos com objetos de aprendizado. Como uma extensão desse recurso de catálogo compartilhado, oferecemos suporte à propagação das atualizações para objetos de aprendizado, como Medalhas, Habilidades, Módulos, Cursos, Programas de aprendizado, Certificações e Ajudas de tarefa.

Para obter mais informações sobre esse recurso, consulte  [Ajuda de catálogos compartilhados](../administrators/feature-summary/catalogs.md#propagation)

**Feedback N1 e N3**

* A caixa de diálogo de feedback L1 aparece assim que um aluno conclui a realização do curso. Além disso, o aluno recebe uma notificação sobre a conclusão do feedback L1.
* Uma opção para adicionar perguntas descritivas foi fornecida no recurso de feedback N1 e N3. Os administradores podem adicionar essas perguntas descritivas aos alunos. Essa condição está além do conjunto padrão de perguntas fornecidas pelo Learning Manager. Você pode adicionar duas perguntas descritivas do feedback N1 e uma pergunta descritiva do feedback N3.\
  Para obter mais informações sobre esse recurso, consulte [Ajuda sobre as perguntas descritivas do feedback N1 e N3](../administrators/feature-summary/courses.md#descriptive)

**Exportar usuários**

* Com base na solicitação de alguns grandes usuários corporativos, foi fornecida uma nova opção de download da lista de todos os usuários da conta do Learning Manager. No logon do administrador, clique em **[!UICONTROL Usuários]** no painel esquerdo e clique em **[!UICONTROL Exportar dados do usuário]** para baixar a lista de usuários como uma planilha do excel.

### Problemas corrigidos {#Issuesfixed-1}

**Inscrições no curso**

* Em alguns casos, quando um administrador tentava exibir as inscrições no curso usando a guia Alunos, alguns dos nomes dos alunos inscritos não eram exibidos. Esse problema foi corrigido.

**Adicionar cursos**

* Ao adicionar uma habilidade ao curso, se um autor adicionasse uma habilidade que tivesse um espaço em branco no final do nome, ocorria um erro e o curso não era salvo. Esse problema foi corrigido.

**Consumir cursos**

* Em um curso ordenado, alguns alunos não conseguiam se mover de um módulo para outro durante a realização de um curso, pois os módulos não estavam sendo marcados como concluídos. Esse problema foi corrigido.
* Em um curso ordenado, os alunos não podiam navegar entre os módulos no sumário durante os modos normal e revisitar. Esse problema foi corrigido.

**Fluidic player**

* Em algumas ocorrências, quando um usuário faz upload do conteúdo de um módulo com quadros/slides ocultos, o Sumário no painel esquerdo costumava exibir os quadros/slides ocultos. Esse problema foi corrigido.

**Relatórios**

* O tempo necessário para carregar relatórios é maior na atualização mais recente do Learning Manager. Esse problema foi corrigido.

+++

+++Atualização 24

Data de lançamento: 12 de outubro de 2016.

### Aprimoramentos {#Enhancements-6}

**Relatórios do curso**

* Nas contas do Learning Manager habilitadas para o identificador exclusivo universal (UUID), o UUID aparece no relatório de inscrição do curso, nas transcrições do aluno e nos relatórios de pontuação do quiz.

### Problemas corrigidos {#Issuesfixed-2}

**Ajudas de tarefa**

* Em alguns casos, quando um aluno tentava navegar da guia Aprendizado > Ajudas de tarefa para Aprendizado > Cursos, os cursos não eram carregados conforme esperado na guia Aprendizado > Cursos. Esse problema foi corrigido.

**Adicionar usuários**

* Em alguns casos, quando um único usuário era adicionado ao aplicativo Learning Manager, o usuário não recebia a notificação por e-mail. Esse problema foi corrigido.
* Os administradores não conseguiriam baixar o arquivo CSV se o processo de upload de CSV falhasse. Esse problema foi corrigido; os administradores podem baixar o CSV mais recente mesmo se o processo de upload de CSV falhar.
* Se um CSV for importado após a modificação das informações do usuário autorregistrado com letras maiúsculas e minúsculas misturadas, os detalhes do usuário autorregistrado não foram exibidos na interface do usuário do administrador. Esse problema foi corrigido.

**Relatórios do curso**

* Em alguns casos, as pontuações do quiz não eram exibidas nos cursos, mesmo que as pontuações aparecessem nas transcrições do aluno. Esse problema foi corrigido.

**Relatórios de inscrição**

* Em alguns casos, os relatórios de inscrição do aluno no Excel não estavam sendo baixados para os objetos de aprendizado. Esse problema ocorria sempre que caracteres não ASCII ou especiais eram usados no nome de objetos de aprendizado. Esse problema foi corrigido.

**Logon de usuário**

* Ao configurar uma senha durante o registro ou durante a redefinição, a mensagem de erro não era exibida mesmo que a senha inserida não estivesse em conformidade com a política de senha. Esse problema foi corrigido.

**Eficácia do curso**

* Na função do aluno, a eficácia do curso era exibida como uma das **Classificar por** filtrar opções mesmo quando um administrador desativou a eficácia do curso para os alunos. Esse problema foi corrigido.

**Certificações**

* Quando um administrador removia alunos de uma certificação recorrente, ocorria um erro e o aplicativo Learning Manager travava. Esse problema foi corrigido.

**Relatórios**

* Quando um administrador tenta gerar um relatório de certificação com **Até a data** como opção, os usuários inativos não eram exibidos no relatório. Esse problema foi corrigido.
* Quando um administrador clica no link Relatórios do curso na guia Relatórios>Meus relatórios, uma caixa de diálogo pop-up costumava aparecer sem um botão Fechar. Esse problema foi corrigido.

**Fluidic player**

* Ao visualizar cursos como administrador ou autor, quando um usuário escolhe o modo de Tela cheia no Fluidic Player, a tela aparece em branco. Esse problema foi corrigido.

**Suporte a vários idiomas**

* Os caracteres de ponto de interrogação costumavam aparecer em vez de caracteres chineses em resposta a chamadas de API feitas por usuários. Esse problema foi corrigido.

**Camada da API**

* Um erro costumava ocorrer sempre que um usuário tentava obter a ID de catálogo padrão usando a API get/catalog/catalog Id. Uma ID de catálogo padrão pode ser semelhante a &#39;970_default&#39;. Esse problema foi corrigido.

**Interface do usuário**

* Alguns pequenos erros de digitação foram corrigidos na interface de usuário do aplicativo Learning Manager na função do aluno.

+++

+++Atualização 23

Data de lançamento: 19 de setembro de 2016.

### Problemas corrigidos {#Issuesfixed-3}

**Transcrições do aluno**

* Em alguns casos, se havia mais de vinte alunos inativos/excluídos em uma conta, os alunos inativos acima de vinte não eram exibidos na lista suspensa de pesquisa da caixa de diálogo de transcrição do aluno. Esse problema foi corrigido.
* Se uma conta de usuário externo tiver expirado, seus alunos não estavam listados na transcrição do aluno gerada. Esse problema foi corrigido.

**Catálogos**

* Alguns dos clientes estavam enfrentando um problema com a exibição de grupos de usuários em um catálogo. Mesmo que haja mais de vinte grupos de usuários em um catálogo, somente vinte grupos de usuários foram exibidos. Corrigimos esse problema exibindo 200 grupos de usuários em uma página.

+++

+++Atualização 22

Data de lançamento: 13 de setembro de 2016.

Nesta versão de atualização, corrigimos alguns dos problemas de back-end de engenharia de produto para aprimorar a experiência do cliente.

### Problemas corrigidos {#Issuesfixed-4}

* Ocorreu um problema com a exportação de dados do módulo em transcrições do aluno que resultava em dados de exportação inadequados. Esse problema foi corrigido.
* Se um usuário usava uma extensão de ID de e-mail com mais de quatro caracteres, ela não era compatível. Por exemplo, se uma ID de e-mail for <abcd@company.world> não era suportado, pois o mundo da extensão tinha mais de quatro caracteres. Corrigimos isso para oferecer suporte à extensão com mais de quatro caracteres.

+++

+++Atualização 21

Data de lançamento: 1 de setembro de 2016.

### Aprimoramentos {#Enhancements-7}

**Eficácia do curso**

Agora, os administradores podem personalizar o curso ou o recurso de eficácia do programa de aprendizado para ocultar a pontuação de eficácia da exibição dos alunos.

**Adicionar usuários externos**

O Learning Manager aumentou o limite máximo de registros externos a 5 dígitos.

**Relatórios**

Todos os relatórios e listas de alunos baixados de todos os objetos de aprendizado exibem os usuários excluídos agora com a demarcação clara dos usuários excluídos.

### Problemas corrigidos {#Issuesfixed-5}

**Ciclo de vida do curso**

Em alguns casos, quando um autor edita um curso compartilhado para atualizar informações de um módulo modificado, uma mensagem de aviso costumava aparecer, indicando que o usuário não pode editar, pois as alterações anteriores estão sendo processadas. Esse problema foi corrigido.

**Suporte a vários idiomas**

Em alguns recursos da interface do usuário do Learning Manager, as mensagens não eram traduzidas e não eram exibidas ao usuário em frases no idioma apropriado. Esse problema foi corrigido.

**Adicionar usuários**

* Quando um usuário excluído é adicionado novamente como um usuário único, o usuário não é adicionado ao grupo de usuários “todos os usuários” por padrão. Esse problema foi corrigido.
* Um número limitado de perfis usados para aparecer nas caixas de diálogo de alteração de perfil de inscrição externa e de autoinscrição. A paginação foi implementada agora.

**Ajudas de tarefa**

Sempre que um aluno acessava a guia Ajudas de tarefa na conta do aluno, uma mensagem de erro era exibida como “Esta ajuda de tarefa não existe mais na sua lista” antes de carregar o conteúdo. Esse problema foi corrigido.

**Catálogos**

Durante a criação do catálogo, ao adicionar cursos como conteúdo ao catálogo, o filtro Classificar por não funcionava conforme esperado. Esse problema foi corrigido.

**Configurações**

Nas configurações da conta, quando um administrador usava um subdomínio que já era usado por alguma outra conta, uma mensagem de erro não era exibida ao administrador. Esse problema foi corrigido.

**Camada da API**

* Quando o gerenciador de inclusão é usado ao buscar usuários, uma hierarquia completa de gerenciadores é obtida em vez do gerenciador imediato do usuário. Esse problema foi corrigido.
* Quando um usuário com permissão de autorização de escopo do aluno tentava adicionar usuários, uma mensagem de erro genérica era exibida. Esse problema foi corrigido e uma mensagem de acesso não autorizado é exibida ao aluno agora.
* Quando um usuário tentava excluir um último usuário existente em um grupo de usuários, uma mensagem de erro 204 era exibida ao usuário. Esse problema agora é corrigido exibindo uma mensagem de erro relevante para o usuário indicando que o grupo deve ter pelo menos um usuário.
* O espaço, se existir no início do nome, foi cortado ao exibir o nome de usuário na API GET/users. Isso já foi corrigido.
* Os cursos de rascunho também foram retornados em resposta quando o administrador tenta obter todos os cursos. Esses cursos de rascunho devem ser privados para o autor. Esse problema foi corrigido, os cursos de rascunho não retornam agora.

**Integração com o Adobe Connect**

* Em algumas instâncias das sessões de sala de aula virtual com base no Adobe Connect, a participação não era marcada automaticamente após a sessão. Esse problema ocorria apenas quando uma ID de logon era usada pelo professor para fazer logon em vez de uma ID de e-mail. Está corrigido agora.
* Em alguns casos, o nome do professor costumava aparecer várias vezes na lista suspensa do professor durante a criação do módulo de sala de aula virtual com base no Adobe Connect. Esse problema foi corrigido.

+++

+++Atualização 20

Data de lançamento: 22 de agosto de 2016.

### Aprimoramentos {#Enhancements-8}

**Camada da API**

Como parte desta atualização, adicionamos as seguintes novas APIs para atender a alguns dos requisitos dos clientes:

1. Usuários do POST
1. Usuários do DELETE
1. GETuserGroups
1. GET userGroups /{id}
1. DELETE userGroups /{id}/Usuários
1. POST userGroups /{id}/Usuários
1. GET /users/userId/userGroups

Também aprimoramos o modelo de usuário existente com as seguintes adições:

1. O modelo do gerente é adicionado como relacionamento com o modelo do usuário
1. userGroupId é adicionado como um novo parâmetro para GetUsers

**Transcrição do aluno**

Quando um usuário gerava a transcrição do aluno para um aluno, a caixa de diálogo pop-up costumava aparecer por um período muito curto e desaparecia sem solicitar a ação do usuário. Aprimoramos a experiência do usuário com um pop-up que pausa e solicita que o usuário clique em OK.

**Integração com o Adobe Connect**

A ID de logon é fornecida como um novo campo opcional nas configurações de integração do Adobe Connect para os usuários que não usam sua ID de e-mail para fazer logon.

### Problemas corrigidos {#Issuesfixed-6}

**Relatórios do curso**

* Quando um módulo de curso consistia em perguntas do tipo aberto ou somente perguntas de pesquisa, um relatório de pontuação do quiz em branco costumava aparecer quando era exportado. Esse problema foi corrigido.
* Em alguns casos, o relatório de pontuação do quiz não era baixado quando um usuário usava o link Exportar pontuação do quiz. Esse problema foi corrigido.

**Criar cursos**

A página Configurações do curso na função Autor não aparecia sempre que uma habilidade associada a esse curso era desativada pelo administrador. Esse problema foi corrigido.

**Registrador inteligente**

O campo de pesquisa não suportava caracteres especiais como entrada e, como resultado, os resultados da pesquisa não eram exibidos. Esse problema foi corrigido.

+++

+++Atualização 19

Data de lançamento: 11 de agosto de 2016.

### Aprimoramentos {#Enhancements-9}

**Registrador inteligente**

O desempenho do mecanismo de pesquisa foi aprimorado para fornecer resultados de pesquisa mais precisos aos usuários.

**Integração com o Adobe Connect**

O processo de verificação/autenticação da solicitação de integração foi aprimorado no aplicativo Learning Manager.

### Problemas corrigidos {#Issuesfixed-7}

**Adicionar usuários**

* Quando havia um grande número de usuários do Learning Manager, ocorria um atraso na página de carregamento dos usuários e dos grupos de usuários. Esse problema foi corrigido.
* Depois que o administrador conclui o upload do arquivo CSV com novos usuários, a lista de usuários na página não foi atualizada com novos usuários até que a página fosse atualizada. Esse problema foi corrigido.
* Às vezes, após importar usuários usando CSV, o valor da ID de usuário na página costumava ser substituído pela ID de email. Esse problema foi corrigido.

**Criar grupos de usuários**

Em alguns casos, a contagem do usuário não era exibida na página de grupos de usuários padrão do Learning Manager. Esse problema foi corrigido.

**Transcrição do aluno**

Os valores de atributo dos campos ativos eram exibidos incorretamente nas transcrições do aluno para certificações. Esse problema foi corrigido.

**Compartilhamento de várias contas**

Em um cenário em que um administrador de conta compartilhava um catálogo de cursos com o destinatário e atualizava o módulo de teste ou de pré-trabalho posteriormente, o conteúdo do módulo de pré-trabalho ou de teste de saída costumava ser reproduzido no módulo de conteúdo do destinatário. Esse problema foi corrigido.

**Temas e marcas**

Quando um administrador alterava um tema para o aplicativo usando o widget de visualização dinâmica e alterna sua função, o widget de visualização dinâmica não funcionava conforme esperado em uma nova função. Esse problema foi corrigido.

**Suporte a vários idiomas**

Quando um administrador altera o código do idioma do aplicativo para chinês simplificado ou espanhol, parte do conteúdo do menu no painel esquerdo, instruções online e mensagens pop-up não eram exibidas em palavras ou frases significativas. Esse problema foi corrigido.

**Fluidic player**

* Quando um autor cria um curso com conteúdo AICC ou Tin Can e tenta visualizar o conteúdo, o conteúdo não é reproduzido. Esse problema foi corrigido.
* A visualização do módulo não funcionava ao criar um curso ou ao editar o curso por um autor. Esse problema foi corrigido.

**Catálogos**

Quando um aluno tentava acessar o URL dos catálogos/programas de aprendizado diretamente no navegador, ele era redirecionado para os cursos. Esse problema foi corrigido.

**Integração com o Salesforce**

* Depois de estabelecer uma conexão com o Salesforce ou FTP, na página Mapear atributos as setas suspensas dos campos não eram exibidas nos navegadores IE, Edge e Safari. Além disso, algumas das mensagens pop-up não foram exibidas nos fluxos de trabalho. Esse problema foi corrigido.
* Em alguns casos, quando um administrador tentava sincronizar os dados .csv importados no conector FTP, a sincronização costumava falhar com as entradas replicadas. Esse problema foi corrigido.

**Camada da API**

* Quando um administrador autoriza o aluno externo usando a autenticação OAuth, às vezes os alunos externos não conseguiam fazer logon no aplicativo. Esse problema foi corrigido.
* Às vezes, quando há uma chamada de API para ajudas de tarefa do aluno, um erro de acesso não autorizado é exibido. Esse problema foi corrigido.

**Configurações**

Na página origens de dados, quando um horário de programação automática é definido e salvo, às vezes ele é revertido para o estado antigo. Esse problema foi corrigido.

**Relatórios de grupo de usuários**

Os valores de grupo de usuários no filtro não estavam sendo preenchidos quando o tipo de relatório foi escolhido como Personalizado. Esse problema foi corrigido.

**Integração com o Adobe Connect**

Título de cabeçalho inapropriado usado para aparecer para a integração do Adobe Connect após concluir a conexão com êxito. O texto do título da página foi corrigido.

**Relatórios**

Às vezes, mesmo se a opção “mostrar dados de valores atuais” estivesse selecionada, os dados mais recentes não eram mostrados nos relatórios. Esse problema foi corrigido.

+++

+++Atualização 18

Data de lançamento: 31 de julho de 2016.

## Novos recursos e aprimoramentos {#newfeaturesandenhancements}

Para obter uma lista dos novos recursos e aprimoramentos da versão de julho do Learning Manager, consulte [Novidades](../whats-new.md).

Alguns dos recursos de aprimoramento estão listados abaixo para sua referência.

**Transcrição do aluno**

O Learning Manager fornece um recurso para gerar transcrições para os alunos do Learning Manager da sua organização. Para obter mais informações, consulte  [Conteúdo de ajuda do recurso Transcrições do aluno](../administrators/feature-summary/learner-transcripts.md).

**Exportar medalha como PDF**

O Learning Manager permite que você exporte suas medalhas como arquivos PDF. Para obter mais informações, consulte  [Conteúdo de recurso de medalhas](../administrators/feature-summary/badges.md).

**Pontuação no quiz dos módulos**

Você pode adicionar a pontuação do quiz para os módulos Sala de aula, Sala de aula virtual e Atividade.

**Adicionar usuários**

* Você pode mover alunos de um grupo de autorregistro para outro grupo.
* Você pode mover usuários de um grupo externo para outro.
* Você pode tornar um usuário de um grupo externo um Gerente do mesmo grupo externo.
* Depois de adicionar um grupo de usuários externo ao Learning Manager, você também pode pausar o processo de registro de usuários externos. A qualquer momento, você sempre pode revogar o bloqueio (pausa) escolhendo uma opção Retomar.
* Agora, você pode editar o nome e a ID de e-mail dos alunos.

**Autoinscrição**

Os alunos também podem cancelar suas inscrições em objetos de aprendizado como curso, programa de aprendizado ou certificação. No entanto, o aluno não pode cancelar a inscrição em um objeto de aprendizado após concluir um objeto de aprendizado.

**Realização de objetos de aprendizado**

Agora, os administradores podem marcar uma atividade de aprendizado dos alunos como concluída.

**Relatórios**

* Você pode assinar relatórios de cursos, programas de aprendizado ou certificados. Você também pode assinar relatórios de curso individuais para obter dados como o status da pontuação do questionário e do aluno. As assinaturas serão enviadas à sua ID de e-mail conforme registrada na conta do Learning Manager. Você também pode alterar essa ID de e-mail.
* Quando você exporta o relatório de inscrição de certificação, uma nova coluna chamada **Data de vencimento** também é exportado. Esses dados da coluna permitem que os administradores conheçam os alunos que perderam os prazos de consumo do objeto de aprendizado.

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

Alguns clientes tiveram problemas ao usar o recurso de logon único no Learning Manager. Esse problema foi corrigido ao fazer referência à entityId do Learning Manager para um URL (<https://learningmanager.adobe.com>) em vez de uma palavra-chave. O Learning Manager está em conformidade com a especificação SAML 2.0.

+++

+++Atualização 15

Data de lançamento: 25 de maio de 2016

### Aprimoramentos {#Enhancements-10}

**Programas de aprendizado/certificações**

* Na lista de inscrição dos alunos para programas de aprendizado e certificações, o nome completo (nome e sobrenome) dos alunos é exibido. Anteriormente, somente o nome dos alunos era exibido.
* As habilidades com créditos de nível mais alto são consideradas da lista de cursos em certificações/programas de aprendizado e exibidas em cartões como habilidade no programa de aprendizado/certificação. Se houver vários cursos com o mesmo valor de créditos, eles serão selecionados em ordem alfabética. Anteriormente, os nomes de habilidades para programas de aprendizado/certificação eram retirados aleatoriamente de uma lista de cursos.

**Importar CSV**

No recurso de carregamento automático de CSV usando o FTP, os administradores recebem notificações por e-mail se houver alguma falha no carregamento do CSV.

**Adicionar parceiros externos**

Quando alunos externos visitam a página de registro usando um URL de perfil externo, o nome do perfil externo é exibido na página de registro para melhor identificação.

### Problemas corrigidos {#Issuesfixed-9}

**Visualizar e publicar cursos**

* Na função de autor, ao visualizar um curso que foi carregado do Captivate como um conteúdo SCORM+SWF com `code $$cpQuizInfoStudentName$$` variável, um valor nulo foi exibido para a variável. Esse problema foi corrigido.
* Quando um curso do Presenter com um título que continha apóstrofo (&#39;) era publicado e exibido no Learning Manager, os pontos de interrogação (???) eram exibidos no sumário. Esse problema foi corrigido.

**Certificações**

* Se uma certificação estiver associada a um catálogo e quando ela ocorrer novamente, ela aparecerá em todos os catálogos associados. Anteriormente, havia alguns casos em que os usuários não podiam visualizar as certificações recorrentes em seus catálogos.
* Ao criar certificações, se um administrador entrar no **dias para concluir** for maior ou igual ao período de validade da certificação, será exibida uma mensagem de aviso. Anteriormente, a mensagem de aviso não era exibida aos administradores.
* A certificação **validade** é exibido aos usuários em termos de meses. Anteriormente, o valor base era exibido em termos de anos.

**Definir programas de aprendizado**

O prazo não é exibido para instâncias padrão do programa de aprendizado. Anteriormente, costumava aparecer um prazo predefinido que pode não ser relevante para os usuários.

**Criar cursos usando módulos**

* Quando um autor atualizou um módulo de um curso misto, a página de participação não aparecia na função de administrador. Esse problema foi corrigido.
* Quando o nome de uma instância do curso contém dois pontos (:), a ação de exportação para a lista de alunos falhou. Esse problema foi corrigido.

+++

+++Atualização 14

Data de lançamento: 4 de maio de 2016

### Aprimoramentos {#Enhancements-11}

**Catálogos**

Quando um aluno acessa o catálogo, o foco padrão se desloca entre as guias com base na disponibilidade dos objetos de aprendizado, na seguinte ordem: 1. Cursos 2. Programas 3. Certificações e 4. Ajudas de tarefa. Por exemplo, se os cursos não estiverem disponíveis na guia Cursos para esse aluno, o foco mudará para o próximo objeto de aprendizado, que é Programas se houver programas de aprendizado.

**Configurações da conta**

Uma opção de feedback é fornecida na caixa de diálogo de confirmação de desativação de conta quando um administrador opta por desativar uma conta.

### Problemas corrigidos {#Issuesfixed-10}

**Exportar relatórios**

* A exportação da lista de alunos falhava quando um grande conjunto de usuários estava inscrito em um programa de aprendizado. Esse problema foi corrigido.
* Quando um curso tem duas instâncias com o mesmo nome e o nome da instância é longo, duas planilhas não foram criadas no arquivo do Excel exportado. Esse problema foi corrigido.

**Inscrição em massa**

Quando um grande número de alunos estava inscrito em objetos de aprendizado, como programas de aprendizado, cursos, certificações, ajudas de tarefa e planos de aprendizado, a inscrição costumava falhar. Esse problema foi corrigido.

+++

+++Atualização 13

Data de lançamento: 20 de abril de 2016

### Problemas corrigidos {#Issuesfixed-11}

**Criar cursos usando módulos**

Quando o conteúdo de um módulo com um nome de arquivo longo é carregado, ocorrem problemas com a aparência dos botões. Além disso, as opções de upload e exclusão do módulo não funcionavam conforme esperado. Esse problema foi corrigido.

**Importar CSV**

Conforme a solicitação dos clientes dos EUA, o tempo de upload automático do FTP CSV foi alterado de meia-noite GMT para meia-noite PST.

**Exportar relatórios**

A exportação dos dados de inscrição usados para falhar se um dos alunos inscritos for excluído após consumir o curso. Esse problema foi corrigido.

**Modelos de e-mail**

* A palavra **parceiros,** que foi utilizado para representar grupos externos,****&#x200B;é&#x200B;**** removido do corpo e título dos modelos de e-mail. Os grupos externos não são necessariamente chamados de parceiros.\
  **Observação:** Este modelo atualizado não é exibido se o modelo padrão já estiver modificado. Para exibir o modelo atualizado, clique em **Reverter para original** pol. **Visualização do modelo** diálogo.

* O URL não pode ser clicado no e-mail recebido pelos administradores sempre que **Perfil Criado (Autorregistro)** e **Perfil criado (externo/parceiros)** os modelos de e-mail são editados. Esse problema foi corrigido.

+++

+++Atualização 12

Data de lançamento: 7 de abril de 2016

### Aprimoramentos {#Enhancements-12}

**Ajudas de tarefa**

Crie ajudas de tarefa usando um URL. Você pode mencionar apenas um nome de URL no fluxo de trabalho de criação de ajuda de tarefa e criar ajuda de tarefa se quiser usar qualquer conteúdo online existente como uma ajuda de tarefa.

**Adicionar alunos**

A edição de dados de um único usuário, como nome, email, perfil e nome do gerente, é permitida. Todos os grupos de usuários correspondentes são atualizados com os dados mais recentes do usuário.

**Exportar relatórios**

As colunas Nome do gerente, Nome do objeto de aprendizado e Valor não exclusivo definido pelo usuário do CSV são adicionadas à lista de alunos exportada para objetos de aprendizado. Anteriormente, apenas os dados básicos dos alunos, como nome, data, e-mail e status, eram exibidos.

**Adicionar parceiros externos**

O aplicativo Learning Manager não permite que os alunos externos entrem no aplicativo após a conta ter expirado. Os parceiros externos podem exibir o status de suas contas no aplicativo.

**Certificações**

Você pode renovar as certificações em meses mencionando o valor em **Validade** campo. Anteriormente, a renovação da certificação era permitida apenas em termos de anos.

### Problemas corrigidos {#Issuesfixed-12}

**Comunicados**

No logon do administrador, a paginação não funcionava na página Comunicados. Esse problema foi corrigido.

**Programas e planos de aprendizado**

* Quando um aluno tentava ignorar um módulo de curso ordenado em um programa de aprendizado, uma mensagem de erro não era exibida. Esse problema foi corrigido agora. Uma mensagem de erro **Não é possível ignorar módulos**&#x200B;é exibida.
* Os cursos não eram adicionados aos programas de aprendizado sempre que a paginação era usada na lista de cursos. Esse problema foi corrigido.
* **Retirado** foi exibida duas vezes em Programas de aprendizado > instâncias. Esse problema foi corrigido.

**Ajudas de tarefa**

* Quando um aluno remove ajudas de tarefa da **Aprendizado** guia, **Nome** a classificação não funcionava conforme o esperado até que a página fosse atualizada. Esse problema foi corrigido.

* Se uma ajuda de tarefa fizesse parte de vários cursos, os cursos não eram exibidos na lista de ajudas de tarefa. Esse problema foi corrigido.
* Se um aluno aplicasse mais ou menos zoom ao navegador, a paginação da lista de ajudas de tarefa não funcionava conforme esperado. Esse problema foi corrigido.

**Realização do curso**

* Se um aluno aplicasse mais ou menos zoom ao navegador, a paginação dos cursos não funcionava conforme esperado. Esse problema foi corrigido.

**Criar habilidades**

No logon dos alunos, a dica de ferramenta do nome de habilidade no **Mapa de habilidades **foi** **não exibindo o****nome completo. Esse problema foi corrigido.

**Adicionar parceiros externos**

* Uma mensagem de texto foi incluída na página de registro de usuários externos como **Os usuários devem primeiro se registrar e criar uma senha de nome de usuário para logons subsequentes**.

**Notificações do usuário**

* Quando um aluno externo clica no botão **Abrir Anotações** link na notificação por e-mail de nova visita ao curso, o reprodutor abre, mas o painel notas não estava funcionando. Esse problema foi corrigido.
* Quando um aluno externo tenta abrir os módulos de pré-trabalho ou de teste final usando **Abrir Anotações** link na notificação por e-mail da nova visita ao curso, o conteúdo das notas não estava visível. Esse problema foi corrigido.

**Criar cursos usando módulos**

Quando um administrador tentava inscrever alunos em um curso misto que contém um módulo de sala de aula expirada, a caixa de diálogo de inscrição não era aberta. Esse problema foi corrigido.

**Exportar relatórios**

Se um texto de pergunta contiver mais de 255 caracteres e estiver habilitado para o formato SCORM 1.2, o relatório do quiz dessas perguntas não funcionará. Esse problema foi corrigido.

+++

+++Atualização 11

Data de lançamento: 15 de março de 2016

### Problemas corrigidos {#Issuesfixed-13}

**Criar cursos com módulos**

* No logon do administrador, ao tentar criar uma nova instância para cursos do **Retirado**, ocorria um erro. Esse problema foi corrigido.
* No logon do administrador do conteúdo localizado, ao inscrever alunos na instância do curso, as ações e os layouts da tela de inscrição eram distorcidos. Esse problema foi corrigido.
* Quando um autor está criando módulos de Sala de aula ou Sala de aula virtual, o mês padrão do calendário de datas costumava ser exibido em janeiro de 2015. Esse problema foi corrigido para refletir a data atual por padrão.
* Quando o nome de uma instância do curso consiste em uma barra inclinada para frente ou para trás, a ação de exportação da lista de alunos costumava falhar. Esse problema foi corrigido.

**Comunicados**

Quando um aluno passa o mouse sobre um comunicado em vídeo, o cursor não mudava para um dedo pontiagudo conforme esperado. Esse problema foi corrigido.

**Notificações do usuário**

Quando um aluno externo clica no botão **Abrir Anotações** na notificação por e-mail da nova visita ao curso, o programa não estava funcionando. Esse problema foi corrigido agora. Este link abre o reprodutor com notas, mesmo quando o usuário não estiver conectado no Learning Manager.

**Suporte aos idiomas francês e alemão**

Os URLs de Ajuda no recurso de upload de CSV estavam navegando para o conteúdo de ajuda em inglês. Esse problema foi corrigido.

**Visualizar e publicar cursos**

No logon do autor, ao visualizar o conteúdo da API TinCan (SWF/HTML) do Presenter 10 e 11, o conteúdo não funcionava. Esse problema foi corrigido.

**Emails personalizáveis**

Os nomes dos títulos nos modelos de e-mail não eram apropriados. O conteúdo é atualizado nesses títulos de modelo para torná-los legíveis.

**Ajudas de tarefa**

No navegador Internet Explorer 11, o nome e o ícone da ajuda de tarefa apareciam como distorcidos na visualização do autor e do administrador. Esse problema foi corrigido.

+++

+++Atualização 10

Data de lançamento: 28 de fevereiro de 2016.

## Novos recursos {#Newfeatures-2}

### Ajudas de tarefa

Ajudas de tarefa é um repositório de conteúdo de treinamento acessível aos alunos sem critérios de inscrição ou conclusão. Os alunos podem consultar essas ajudas de tarefa para obter assistência na execução de qualquer atividade ou tarefa em uma organização. O administrador pode acompanhar o número de downloads por ajuda de tarefa.

Para obter mais informações sobre esse recurso, consulte  [Ajuda de tarefa](../learners/feature-summary/job-aids.md).

### Comunicados

Um comunicado é uma mensagem multimídia (texto, imagem ou vídeo) que um administrador pode criar e transmitir para um conjunto definido de usuários. Use os comunicados para motivar os alunos a realizar treinamentos e, assim, construir uma cultura de aprendizado.

Para obter mais informações sobre esse recurso, consulte  [Ajuda de Comunicados](../learners/feature-summary/announcements.md).

### Suporte à Tin Can API

O Adobe Learning Manager oferece suporte à especificação Tin Can API (também conhecida como Experience API ou xAPI). Você pode carregar e monitorar conteúdo compatível com a API do Tin Can, semelhante ao modo como você monitora o conteúdo SCORM e AICC.

Para obter mais informações, entre em contato com a equipe de suporte da Adobe.

### Sequenciamento do curso

Você pode criar um caminho de aprendizado atribuindo um curso de acompanhamento ou qualquer atividade de aprendizado automaticamente.

Os eventos dos planos de aprendizado foram atualizados. Alguns novos eventos foram adicionados. Consulte  [Planos de aprendizado](../learners/feature-summary/learning-programs.md) para obter mais informações.

### Lembrete de notas

Se tomar notas durante um curso, o Learning Manager envia um lembrete após 15 dias com uma notificação para você revisar as notas.

### Gamificação no nível de grupo

Os administradores podem definir o escopo da gamificação alterando as configurações do escopo. É possível ativar de forma seletiva a gamificação entre usuários, grupos ou locais de perfil semelhantes. Consulte  [Gamificação](../learners/feature-summary/gamification.md) para obter mais informações.

### Suporte aos idiomas francês e alemão

O aplicativo Learning Manager está disponível em francês e alemão. Você pode personalizar o idioma para feedback, instâncias do curso e comunicação.

### Aprimoramentos {#Enhancements-13}

Há aprimoramentos significativos nos recursos existentes do Learning Manager. Alguns dos aprimoramentos predominantes são os seguintes:

### Importar CSV

Se você excluir usuários, não poderá adicionar os mesmos usuários novamente ao aplicativo usando a adição de um único usuário. No entanto, você pode adicionar de volta o usuário excluído usando o processo de upload de CSV. Há alterações significativas na restrição de campos obrigatórios no recurso de upload de CSV. Consulte  [Perguntas frequentes sobre CSV](../administrators/add-users-in-bulk.md) para obter mais informações.

### Exibição da lista de cursos

Por padrão, você pode exibir cursos como cartões. Uma exibição em lista foi introduzida nesta versão. Você pode clicar no ícone de barra tripla ao lado do campo de pesquisa para alterar a exibição.

### Excluir cursos

Agora você pode excluir cursos nos estágios de rascunho e retirado. Consulte  [Cursos](../administrators/feature-summary/courses.md) para obter mais informações. Se um objeto de aprendizado for excluído, todos os seus dados de relatório também serão excluídos. Se um curso for excluído e se fizer parte de qualquer outro objeto de aprendizado, uma mensagem apropriada aparecerá para o usuário.

**Programas e planos de aprendizado**

Você pode impor a ordem em que os alunos podem realizar os cursos dentro dos programas de aprendizado. É possível excluir programas de aprendizado nos estágios de rascunho e retirado. Se um objeto de aprendizado for excluído, todos os seus dados de relatório também serão excluídos.

**Certificações**

Você pode excluir certificações nos estágios de rascunho e retirado. Se um objeto de aprendizado for excluído, todos os seus dados de relatório também serão excluídos.

**Classificação da eficácia do curso**

No logon do administrador, você pode exportar os dados de feedback N1 e N3 de qualquer curso.

**Criar cursos com módulos**

Você pode impor que os alunos concluam os pré-requisitos antes de realizar os cursos.

**Notificações do usuário**

Os alunos recebem notificações sempre que são inscritos automaticamente em um programa de aprendizado.

**Módulos de sala de aula (ILT)**

Você pode criar cursos em salas de aula em uma data anterior. Esse recurso permite que os administradores da empresa alimentem as informações de cursos em salas de aula mais antigos no Learning Manager e gerem relatórios.

**Exportar relatórios**

Os relatórios dos alunos foram aprimorados. Você pode exibir o nome, e-mail, status do objeto de aprendizado, critérios de inscrição, data de inscrição, data de conclusão e data inicial no relatório.

**Adicionar parceiros externos**

Depois de ter inscrito os alunos externos na conta do Learning Manager, você também pode reduzir o número de alunos, se necessário. No entanto, não é possível reduzir o tamanho dos alunos além do número de vagas usado. Como solução alternativa, você pode excluir os alunos registrados primeiro e, em seguida, se inscrever novamente com o número necessário de vagas.

### Problemas corrigidos {#Issuesfixed-14}

**Participação dos alunos**

A folha de participação na exibição Administrador exibe o nome completo do funcionário, se disponível. Anteriormente, somente o nome do aluno era exibido.

**Programas e planos de aprendizado**

Todos os cursos dos programas de aprendizado são exibidos na ordem esperada. Anteriormente, havia problemas na ordem dos cursos em um programa de aprendizado. Esse problema foi corrigido.

**Adicionar alunos**

Se um usuário registrado automaticamente existente tentar se registrar novamente usando o processo de registro automático, será exibida uma mensagem apropriada. O formato e o conteúdo da mensagem são fixos.

**Relatórios**

Se você quiser que o conteúdo identifique o tempo gasto pelo usuário no consumo de conteúdo, é possível identificá-lo usando uma variável, `code cmi.core.session_time`. A variável não foi definida anteriormente. Esse problema foi corrigido.

**Criar cursos com módulos**

Sempre que um módulo de curso existente é substituído por outro módulo, uma nova versão dele é gerada. Se o quiz deste novo módulo fosse exportado, uma exceção ocorria e o relatório do quiz não era gerado. Esse problema foi corrigido agora.

**Modelos de e-mail**

Os erros de digitação nos modelos de e-mail foram corrigidos.

+++

+++Atualização 9

Data de lançamento: 9 de fevereiro de 2016.

## Comportamento de logoff atualizado {#signoutbehaviorupdated}

Quando os usuários clicarem **[!UICONTROL Sair]** no Learning Manager, agora eles estão desconectados do aplicativo Learning Manager e também estão desconectados das suas IDs de Adobe.

+++

+++Atualização 8

Data de lançamento: 20 de janeiro de 2016.

### Aprimoramentos {#Enhancements-14}

**E-mails personalizáveis**

* Os usuários podem modificar a seção de rodapé dos modelos de email. É possível personalizar o rodapé em um modelo de email com o texto de sua escolha. O rodapé personalizado é aplicado automaticamente a todos os tipos de modelos de email.

**Realização do curso**

* Os objetos de recursos no modo de visualização de um curso são listados um após o outro em uma nova linha. Anteriormente, havia ocorrências em que os recursos de um curso eram exibidos lado a lado em uma única linha.

**Link direto para objetos de aprendizado**

* Você pode acessar os objetos de aprendizado (exceto Certificação) usando um URL direto. O **[!UICONTROL Copiar URL]** é exibida nos blocos de objetos de aprendizado. Os usuários podem clicar em **[!UICONTROL Copiar URL]** e cole o link em uma página separada do navegador para acessar diretamente o objeto de aprendizado.

**Criar cursos usando módulos**

* Ao criar um curso, os autores podem organizar cursos de pré-requisito em qualquer ordem. Anteriormente, essa opção não estava disponível no Learning Manager.

* Os autores podem adicionar ou excluir cursos de pré-requisito em cursos publicados. Anteriormente, esse recurso estava disponível apenas para cursos em modo de Rascunho.

**Registro de usuário**

* Os usuários podem fazer logon no Learning Manager sem nenhuma verificação adicional do URL se a sua Adobe ID corresponder à ID de e-mail do Learning Manager. Ao adicionar usuários à conta, o administrador de uma empresa fornece a ID de e-mail do Learning Manager.

**Criar catálogo**

* Na função Administrador, ao criar catálogos usando **Adicionar objetos de aprendizado** , os cursos retirados não aparecem na lista de cursos.

**Outras correções**

* Na função Administrador, o nome completo dos alunos é exibido em **Alunos** guia. Anteriormente, somente o nome do aluno era exibido.

+++

+++Atualização 7

Data de lançamento: 13 de janeiro de 2016.

### Problemas corrigidos {#Issuesfixed-15}

**Realização do curso**

* Ao acessar o conteúdo do curso, a barra de reprodução do conteúdo aparece sempre na tela. Havia um problema anteriormente com a barra de reprodução de conteúdo, pois ela costumava desaparecer da tela intermitentemente.
* Ao acessar o conteúdo do curso, se o conteúdo tiver uma caixa de diálogo pop-up que aparece perguntando aos usuários se eles realmente querem sair ou ficar na página, pressionar a tecla Stay nessa caixa de diálogo levará o usuário de volta ao conteúdo. Em alguns casos, clicar no botão de permanência costumava tirar o usuário do conteúdo do curso.

**Outras correções**

* Alguns problemas relacionados à reprodução de conteúdo foram resolvidos.

+++

+++Atualização 6

Data de lançamento: 22 de dezembro de 2015

### Aprimoramentos {#Enhancements-15}

**Painel pessoal**

* Ao acessar cursos, catálogos e programas de aprendizado nas funções Administrador e Autor, a ordem das guias é alterada para **Publicado - Rascunho - Todos - Retirado**. A seleção padrão é **Publicado.**

### Problemas corrigidos {#Issuesfixed-16}

**Realização do curso**

* Na função do aluno, ao consumir um curso, se o reprodutor for fechado com o botão Voltar do navegador ou com a tecla Backspace do teclado, o tempo de aprendizado gasto no curso é capturado nos relatórios. Em algumas situações, ocorria um problema no qual essa duração não era registrada nos relatórios.

**Registro de usuário**

* Se um usuário registra uma conta do Learning Manager usando autorregistro habilitado para SSO, o nome do usuário aparece corretamente na lista de registros. Houve alguns casos em que o nome de usuário era exibido incorretamente.

**Criar cursos usando módulos**

* Quando um autor duplica um curso, os arquivos de recursos do curso duplicado podem ser removidos ou atualizados. Em algumas situações, os usuários enfrentavam problemas para atualizar ou remover os recursos dos cursos duplicados.

**Criar um catálogo personalizado para um grupo de usuários**

* Ao usar **Adicionar objetos de aprendizado** função Administrador, você pode filtrar cursos, escolher um curso e adicionar usando **Adicionar** na parte inferior da caixa de diálogo. Em alguns casos, **Adicionar** botão não estava aparecendo para alguns usuários.

+++

+++Atualização 5

Data de lançamento: 11 de dezembro de 2015

### Problemas corrigidos {#Issuesfixed-17}

**Logon de usuário**

* Quando um usuário tentava entrar no aplicativo Learning Manager sem usar o link de ativação, a mensagem de erro era exibida no formato errado. Esse problema foi corrigido.

**Aplicativo para tablets**

* Após instalar o Learning Manager em tablets Android ou iPhone, as mensagens de compatibilidade com o navegador não eram exibidas. Anteriormente, uma mensagem de compatibilidade de navegador era exibida para os usuários. Esse problema foi corrigido.

+++

+++Atualização 4

Data de lançamento: 9 de dezembro de 2015

### Aprimoramentos {#Enhancements-16}

**Adicionar usuários**

* Na função Administrador, quando o administrador registra usuários ou conclui a adição de um único usuário, é exibida uma mensagem indicando a conclusão bem-sucedida do fluxo de trabalho junto com as próximas etapas a serem seguidas.
* Quando um usuário tenta entrar no aplicativo Learning Manager diretamente sem usar o link de ativação do usuário, é exibida uma mensagem de erro solicitando que o usuário use o link de ativação.

**Navegadores compatíveis**

* Se algum usuário acessa o aplicativo Learning Manager em navegadores não suportados, ele recebe um alerta com a lista branca de navegadores.

### Problemas corrigidos {#Issuesfixed-18}

**Relatórios**

* Na função Administrador ou Gerente, ao criar um Relatório com o eixo secundário como tempo de aprendizado gasto, aplicar o filtro Gerente e salvar o relatório, o usuário não conseguia fazer download desses relatórios. Você pode baixar todos os tipos de relatórios.

**Adicionar usuários**

* Ocorreram alguns erros de digitação na mensagem de alerta exibida ao ativar alunos externos na função de administrador. O problema foi corrigido.
* Na função Administrador, uma mensagem de erro apropriada é exibida quando o campo Gerente não é selecionado corretamente durante a adição de um único usuário.

**Registro de usuário**

* O e-mail de boas-vindas recebido pelos novos usuários destaca a importância de vincular o Adobe ID à ID do Learning Manager para que o logon seja bem-sucedido.

**Emails personalizáveis**

* Quando você adiciona vários alunos aos cursos na sala de aula que têm sessões como anexos, alguns alunos não recebiam notificações por e-mail. Esse problema foi corrigido.
* Os e-mails para alunos sobre inscrições em objetos de aprendizado e outros eventos contêm o nome do objeto de aprendizado específico no assunto do e-mail.

**Outras correções**

* Os problemas relacionados aos links de URL nos modelos de e-mail foram corrigidos.
* Apoio previsto

   * Publicar no Learning Manager
   * Suporte mais rápido ao upload de conteúdo para a versão CP 8 (é necessário um patch CP803)

+++

+++Atualização 3

Data de lançamento: 26 de outubro de 2015.

### Aprimoramentos {#Enhancements-17}

**Adicionar usuários**

* Link da Ajuda online fornecido na caixa de diálogo Adicionar usuários > Upload de CSV para melhor entender os usuários ao fazer upload do arquivo CSV.

**Fluidic player**

* Quando você fazia upload do conteúdo do curso Captivate com mais de 500 MB, o conteúdo não era reproduzido no Fluidic Player. Essa restrição foi removida. Atualmente, o limite de tamanho foi alterado para 2 GB.

**Faturamento**

* Na função Administrador, quando um usuário insere o número de alunos e clica **Fazer pedido,** uma caixa de diálogo é exibida com detalhes sobre as taxas de assinatura mensais e anuais por usuário.

### Problemas corrigidos {#Issuesfixed-19}

**Criar cursos usando módulos**

* Ao criar cursos com módulos de atividade, os autores podem escolher URLs externos válidos, mesmo que contenham caminhos de pasta no URL. Anteriormente, os URLs com caminhos de pasta não eram compatíveis. Esse problema foi corrigido.
* Se o conteúdo do curso fosse um projeto carregado com um arquivo zip no Learning Manager e se esse arquivo zip contivesse os caminhos de pasta, como Zip>pasta>conteúdo, esse tipo de conteúdo não era suportado. Esse problema foi corrigido.

**Aplicativo para tablets**

* Quando um usuário tentava baixar os arquivos de recurso de um curso no aplicativo Learning Manager para Android, os arquivos de recurso não podiam ser baixados. Esse problema foi corrigido.
* Ao realizar um curso usando o Fluidic Player, quando um usuário registrava uma Observação e tentava baixá-la posteriormente, o curso não podia ser baixado. Esse problema foi corrigido.

+++

+++Atualização 2

Data de lançamento: 28 de setembro de 2015

### Aprimoramentos {#Enhancements-18}

**Criar cursos usando módulos**

* O aplicativo Learning Manager oferece suporte ao upload de conteúdo SCORM mesmo se a versão não for mencionada no arquivo manifest.xml. Por padrão, a versão é considerada como 1.2.
* Quando você fazia upload do conteúdo do curso Captivate com mais de 500 MB, o conteúdo não era reproduzido no Fluidic Player. Como parte da Atualização 2, o limite de tamanho foi alterado para 800 MB.

**Faturamento**

* Na função Administrador, ao comprar uma assinatura usando cartão de crédito, o usuário pode escolher a primeira ordem, começando com 10 alunos. O número mínimo de alunos necessários para a primeira ordem foi reduzido de 100 para 10.

**Registro de usuário**

* Um link de URL para criar o Adobe ID foi fornecido em um e-mail de boas-vindas recebido pelos alunos após o registro.

**Adicionar usuários**

* Na função Administrador, adicionar usuários usando a opção de upload de CSV diretamente da conta do Exavault não funcionava para alguns clientes. Esse problema foi corrigido.

### Problemas corrigidos {#Issuesfixed-20}

**Programas e planos de aprendizado**

* Os alunos podem ser inscritos automaticamente no mesmo programa de aprendizado como parte de vários planos de aprendizado. Anteriormente, havia algumas exceções a esse fluxo de trabalho. Esse problema foi corrigido.

**Exibir quadro de classificação e medalhas**

* Na função do aluno, depois de consumir um curso que contém uma medalha, a imagem da medalha não era exibida no mapa de medalhas do painel do aluno e no arquivo baixado. Esse problema foi corrigido.

**Aplicativo para tablets**

* Uma janela pop-up é exibida para indicar a disponibilidade do aplicativo do aluno quando o url do aplicativo do aluno é aberto em um navegador no dispositivo Android.

**Outras correções**

* Um problema com a criação da conta de usuário devido ao suporte ao armazenamento de rede do Akamai foi resolvido.
* Um problema relacionado ao upload de conteúdo do SCORM 1.2 que contém um arquivo zip com várias pastas foi resolvido.

+++
