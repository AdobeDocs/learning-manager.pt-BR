---
jcr-language: en_us
title: Interpretar o CSV de transcrição do aluno
description: Interpretar o CSV de transcrição do aluno
contentowner: saghosh
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 88%

---



# Interpretar o CSV de transcrição do aluno

A transcrição do aluno é um dos relatórios mais populares usados no Adobe Learning Manager. O relatório permite obter quase todos os detalhes possíveis em um único relatório no formato CSV.

Além de ser um relatório que os usuários podem buscar para acompanhar e analisar comportamentos de aprendizado, o relatório também pode ser visto no formato no qual o Learning Manager pode ser configurado para exportar dados sobre comportamentos de aprendizado para aplicativos/sistemas externos.

Um cenário corporativo típico é fazer uma exportação periódica da transcrição do aluno para o Learning Manager, analisá-la para extrair os alunos que concluem um importante programa de aprendizado e fazer um pedido para que um comprovante de presente reconheça e recompense conclusões no prazo adequado.

Outro caso de uso é adicionar os dados do comportamento de aprendizado a um data warehouse corporativo, onde se pode querer combinar dados de aprendizado com outros dados corporativos para analisar as correlações entre o comportamento de aprendizado e outros dados de processo.

No restante do documento, descrevemos brevemente como é possível obter a transcrição do aluno do Learning Manager e, em seguida, fornecer os detalhes sobre como cada linha e coluna do relatório deve ser interpretada.

Essas informações podem ser úteis para qualquer desenvolvedor que deseje integrar o Learning Manager a outros sistemas por meio do processamento dos dados de transcrição do aluno exportados.

## Obter transcrição do aluno na interface do usuário {#fetchlearnertranscriptfromtheuserinterface}

Nas Configurações do perfil, um aluno pode baixar a transcrição. Para obter mais informações, consulte *** [Baixar transcrição do aluno](../../administrators/feature-summary/learner-transcripts.md)***.

Os administradores podem gerar transcrições do aluno para toda a organização; um conjunto específico de usuários ou um conjunto específico de objetos de aprendizado ou um conjunto específico de usuários e objetos de aprendizado. Eles também podem obter todos os registros de aprendizado para uma duração de intervalo de tempo e indicar se as informações de nível de módulo são necessárias (por padrão, as informações de nível de módulo são omitidas). Para obter mais detalhes, consulte [***Baixar transcrições do aluno***](../../administrators/feature-summary/learner-transcripts.md).

<!--Update above link?-->

Os administradores também podem configurar o sistema para enviar periodicamente a transcrição do aluno por e-mail.

A transcrição do aluno gerada por meio da interface do usuário será um arquivo do Excel, que também contém a “Transcrição de habilidade”. Neste documento, indicaremos o que é gerado no formato CSV, um relatório que contém atividades de aprendizado relacionadas à inscrição, ao início, ao progresso ou à conclusão de um objeto de aprendizado.

## Exportar transcrição do aluno {#exportlearnertranscript}

Quando a transcrição do aluno precisa ser consumida por um sistema externo, o Learning Manager fornece um recurso chamado Exportar dados, onde a transcrição do aluno é um dos tipos de dados que podem ser exportados. Como explicado no preâmbulo, isso é necessário para a integração do Learning Manager com um sistema externo que precisa processar dados de comportamento de aprendizado ou para preencher um data warehouse corporativo com dados de comportamento de aprendizado.

Para obter detalhes sobre como os conectores que suportam a exportação da transcrição do aluno, consulte a [seção Exportar dados](/help/migrated/integration-admin/feature-summary/connectors.md) no FTP, Box e conectores PowerBI.

A finalidade servida por esses conectores é exportar dados para um aplicativo de downstream periodicamente (uma vez em N dias). Então, esses conectores exportam apenas os dados do comportamento de aprendizado incremental em cada execução. Observe que esses conectores não permitem a busca de registros pertencentes a um subconjunto específico de usuários ou objetos de aprendizado - são sempre dados sobre todos os usuários e todos os objetos de aprendizado nessa conta.

No caso do PowerBI, o cliente deve fornecer um espaço de trabalho onde o Learning Manager possa continuar exportando esses dados incrementalmente para um conjunto de dados criado dinamicamente. Esse conector apenas exporta dados, e os clientes devem criar seus próprios relatórios/painéis com base nesse conjunto de dados conforme necessário.

A próxima seção fornece detalhes sobre como um sistema downstream deve interpretar os registros na transcrição do aluno.

## Interpretar a transcrição do aluno {#interpretthelearnertranscript}

Cada linha em uma transcrição do aluno pode ser considerada como um comportamento de aprendizado que foi capturado no Learning Manager em um período específico. Normalmente, os conectores exportam “dados incrementais” e, portanto, as linhas representam atividades de aprendizado que ocorreram entre a última execução do conector e a execução atual.

É claro que os conectores também permitem buscar a transcrição do aluno sob demanda, e nesse caso o usuário pode especificar uma data de início e a data de término é assumida como agora. Geralmente, isso era feito inicialmente e, em seguida, o conector era configurado para exportar a transcrição incremental do aluno em um horário específico do dia, uma vez em N dias (o valor padrão de N, sendo 1).

Vamos agora definir o que significa transcrição incremental do aluno

Na transcrição do aluno, cada linha representa uma atividade específica que envolve um aluno específico e um objeto de aprendizado específico. Estamos principalmente interessados em qual estado um aluno está em relação ao objeto de aprendizado - **Inscrito**, **Iniciado**, **Em andamento** e **Concluído**. Portanto, a transcrição do aluno também captura quatro datas correspondentes.

Agora há três tipos de objetos de aprendizado, nos quais o Learning Manager acompanha o progresso do aluno; e os dados exportados contêm informações de progresso no nível do módulo, que é a unidade de conteúdo mais granular que um aluno pode experimentar no Learning Manager.

* **Curso** - uma composição de um ou mais módulos
* **Programa de aprendizado** - uma composição de um ou mais cursos
* **Certificação** - uma composição de um ou mais cursos.

Cada linha na transcrição do aluno pode estar relacionada ao envolvimento de um usuário específico com um módulo, curso, programa de aprendizado ou certificação. Quando um usuário está inscrito em um Programa de aprendizado, a transcrição indicará que ele é e

As colunas da transcrição do aluno fornecem várias informações relacionadas a cada atividade de aprendizado, e as tabelas a seguir descrevem a semântica de cada coluna.

## Transcrição do aluno

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Nome da coluna</b></p></th> 
   <th width="160" valign="bottom"><p><b>Tipo de valor</b></p></th> 
   <th width="306" valign="bottom"><p><b>Descrição</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Nome</b></p></td> 
   <td><p>Nunca vazio</p></td> 
   <td><p>Nome do aluno</p></td> 
  </tr> 
  <tr> 
   <td><p><b>e-mail</b></p></td> 
   <td><p>Nunca vazio</p></td> 
   <td><p>Endereço de e-mail do aluno</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Pode estar vazio</td> 
   <td valign="bottom">Adobe ID do aluno</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID exclusiva do usuário</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">ID exclusiva do usuário do aluno. Essa coluna é baseada na configuração de back-end, se ativada/desativada no nível da conta.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Nome do plano de aprendizado</b></p></td> 
   <td valign="middle"><p>Pode estar vazio</p></td> 
   <td valign="middle">Nome do plano de aprendizado (se houver) através do qual o usuário foi atribuído automaticamente.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>LP/Certificação/Curso</b></p></td> 
   <td valign="middle"><p>Nunca vazio</p></td> 
   <td valign="middle"><p>Nome do programa de aprendizado, certificação ou curso</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Tipo</b></p></td> 
   <td valign="middle">Nunca vazio</td> 
   <td valign="middle"><p>O tipo do objeto de aprendizado no qual o usuário foi inscrito.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Curso</b></p></td> 
   <td valign="middle"><p>Pode estar vazio</p></td> 
   <td valign="middle">Nome do curso no qual o usuário está inscrito. Quando estiver vazia, a linha representa um Programa de Certificação ou Aprendizado. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID exclusiva do OA</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">ID exclusiva do objeto de aprendizado do OA. Esta coluna baseia-se na definição se ativada/desativada no nível da conta</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instância  </b></p></td> 
   <td valign="middle">Nunca vazio</td> 
   <td valign="middle">O nome da instância do usuário do LO está inscrito. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Critérios de seleção</b></p></td> 
   <td valign="middle"><p>Nunca vazio</p></td> 
   <td valign="middle"><p>Base da inscrição (como este aluno se inscreveu neste LO).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Módulo</b></p></td> 
   <td valign="middle"><p>Pode estar vazio</p></td> 
   <td valign="middle">Nome do módulo nos cursos. Quando vazia, esta linha representa um curso, um programa de aprendizado ou uma certificação.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Versão</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">Versão do módulo</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Tipo de entrega</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">Tipo de entrega do módulo - eLearning, F2F, VC, Atividade.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Idioma</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">Idioma em que o módulo é consumido pelo aluno. Esta coluna mostra o valor somente para módulos de e-learning.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Comentário</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">Comentários adicionados pelo administrador, o professor do aluno ao marcar a presença do usuário.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Data de inscrição (Fuso horário da Ásia/Calcutá)</b></td> 
   <td height="19" width="283">Nunca vazio</td> 
   <td height="19" width="728">Data de inscrição pelo aluno no tipo de OA.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Data de início (Fuso horário da Ásia/Calcutá)</b></td> 
   <td><p>Pode estar vazio</p></td> 
   <td height="19" width="728">Data em que o aluno iniciou o OA. Vazio significa que o aluno ainda não iniciou isso.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Data de conclusão (Fuso horário da Ásia/Calcutá)</b></td> 
   <td><p>Pode estar vazio</p></td> 
   <td><p>Data em que o aluno concluiu isso. Vazio significa que o aluno ainda não concluiu isso.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Prazo (fuso horário da Ásia/Calcutá)</b></td> 
   <td><p>Pode estar vazio</p></td> 
   <td height="19" width="728">Data na qual o aluno deve concluir este OA. Vazio significa que não há prazo para isso.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Em atraso</b></td> 
   <td height="19" width="283">Sim/Não</td> 
   <td height="19" width="728">Status de atraso atual do aluno inscrito no OA. Sim/Não</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Status</b></p></td> 
   <td valign="middle">Não iniciado/Concluído/Em andamento/Não inscrito</td> 
   <td valign="middle">% do progresso atual do aluno inscrito no OA.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>% de progresso</b></p></td> 
   <td valign="middle">Pode estar vazio</td> 
   <td valign="middle"><p>Indica a extensão em que o aluno concluiu isso.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Tempo gasto (minutos)</b></td> 
   <td height="38" width="283">Pode estar vazio</td> 
   <td height="38" width="728">O tempo de aprendizado gasto pelo aluno no OA, as linhas no nível do módulo exibem o tempo gasto de aprendizado no módulo individual. As linhas do curso/programa/nível de certificado exibem o tempo de aprendizado gasto agregado.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Nota</b></p></td> 
   <td valign="middle">Aprovado/Reprovado</td> 
   <td valign="middle">Indica o sucesso do aluno. 'Aprovado', se o usuário atendeu aos critérios de sucesso para isso, caso contrário, 'Reprovado'.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Pontuação do questonário</b></p></td> 
   <td valign="middle">Pode estar vazio</td> 
   <td valign="middle">A pontuação mais recente do questionário obtida pelo aluno. Pode estar vazio, se o aluno não tiver tentado fazer o questionário ou se o conteúdo não tiver nenhum questionário ou se o administrador/professor não tiver atribuído nenhuma pontuação.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Pode estar vazio</td> 
   <td height="38" width="728">A pontuação máxima mais recente do questionário possível para o módulo. Pode ficar vazio, se o aluno não tiver tentado fazer o questionário ou se o conteúdo não tiver nenhum questionário nele.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score</b></td> 
   <td height="38" width="283">Pode estar vazio</td> 
   <td height="38" width="728">A maior pontuação do questionário obtida pelo aluno em várias tentativas. Pode estar vazio, se o aluno não tiver tentado fazer o questionário ou se o conteúdo não tiver nenhum questionário ou se o administrador/professor não tiver atribuído nenhuma pontuação.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Pode estar vazio</td> 
   <td height="38" width="728">A pontuação máxima do questionário mais alta possível para o módulo. Pode ficar vazio, se o aluno não tiver tentado fazer o questionário ou se o conteúdo não tiver nenhum questionário nele.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Tentativas realizadas</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">O número total de tentativas realizadas pelo aluno até agora para este módulo.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Máximo de tentativas permitidas</b></td> 
   <td height="19" width="283">Pode estar vazio</td> 
   <td height="19" width="728">O número máximo de tentativas permitidas para o aluno consumir o módulo.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>userState</b></p></td> 
   <td valign="middle">Nunca vazio</td> 
   <td valign="middle">Estado do usuário do aluno: Ativo/Excluído/Suspenso.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Campo Ativo Agrupável</b></td> 
   <td height="38" width="283">Pode estar vazio</td> 
   <td height="38" width="728">Para cada campo ativo agrupável na conta, haverá uma coluna, onde o nome da coluna é o do campo ativo e o valor será o valor específico que o aluno tem para esse campo.</td> 
  </tr> 
  <tr> 
   <td><p><b>Nome do gerente</b></p></td> 
   <td><p><i>Pode estar vazio</i></p></td> 
   <td height="19" width="728">O nome do gerente do aluno</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Número de inscrições</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Contagem de inscrições do aluno para o OA. A linha de nível mais alto do OA mostra um valor = '1'. Os subtreinamentos exibem um valor 0.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Contagem iniciada</b></td> 
   <td height="19" width="283">1 ou 0</td> 
   <td height="19" width="728">Contagem iniciada do aluno para o OA. A linha de nível mais alto do OA mostra um valor = '1'. Os subtreinamentos exibem um valor 0.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Contagem de Conclusões</b></td> 
   <td height="58" width="283">1 ou 0</td> 
   <td height="58" width="728">Contagem de conclusão do aluno para o OA. A linha de nível mais alto do OA mostra um valor = '1' se o aluno estiver com conclusão pendente nesse treinamento. Os subtreinamentos exibem um valor 0 mesmo quando no estado Pendente. A linha de nível mais alto do OA mostra um valor = '0', se o aluno concluiu o treinamento.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Vence em N dias</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Isso mostra um valor de "1" ou "0", dependendo do prazo da instância em que o aluno do treinamento está inscrito. Depende do valor inserido na planilha Resumo de aprendizado I &gt; campo "Data de vencimento em breve".</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Vence em N dias para o usuário</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Isso mostra um valor de "1" ou "0", dependendo do prazo da instância em que o aluno do treinamento está inscrito. Depende do valor inserido na planilha Resumo de aprendizado II &gt; campo "Data de vencimento em breve".</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Contagem de (Progresso maior que N %)</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Isso mostra um valor de "1" ou "0" dependendo do progresso do aluno no treinamento. Depende do valor inserido na planilha Resumo Ide aprendizado I &gt; campo "Progresso maior que".</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Contagem de (Progresso maior que N %) para o usuário</b></td> 
   <td height="38" width="283">1 ou 0</td> 
   <td height="38" width="728">Isso mostra um valor de "1" ou "0" dependendo do progresso do aluno no treinamento. Depende do valor inserido na planilha Resumo de aprendizado II &gt; campo "Progresso maior que".</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>ID de treinamento</b></td> 
   <td height="19" width="283">Nunca vazio</td> 
   <td height="19" width="728">ID de treinamento do treinamento.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Duração do treinamento ou módulo (em minutos)</b></td> 
   <td height="20" width="283">Nunca vazio</td> 
   <td height="20" width="728">Total da duração do treinamento ou módulo (em minutos) da instância padrão do treinamento.</td> 
  </tr> 
 </tbody> 
</table>

### Resumo de aprendizado I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Nome da coluna<br></th> 
   <th>Tipo de valor</th> 
   <th>Descrição</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Tipo</td> 
   <td height="19" width="253">Todos, Programa de aprendizado, Certificado, Curso.</td> 
   <td height="19" width="412">O tipo de OA para o qual a tabela Resumo de aprendizado deve mostrar dados.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Campo(perfil) agrupável</td> 
   <td height="19" width="253">Nunca vazio</td> 
   <td height="19" width="412">O perfil para o qual a tabela de resumo de aprendizado deve mostrar dados.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Nome do gerente</td> 
   <td height="38" width="253">Nunca vazio</td> 
   <td height="38" width="412">O nome do gerente cujos dados de envolvimento do OA subordinados devem ser exibidos na tabela de resumo de aprendizado</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Rótulos de linha</td> 
   <td height="19" width="253">Nunca vazio</td> 
   <td height="19" width="412">O nome do OA com a lista de alunos inscritos no OA.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alunos inscritos</td> 
   <td height="19" width="253">Nunca vazio</td> 
   <td height="19" width="412">Número de alunos inscritos no OA.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alunos que iniciaram</td> 
   <td height="19" width="253">Nunca vazio</td> 
   <td height="19" width="412">Número de alunos que iniciaram o OA.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Número de alunos que concluíram</td> 
   <td height="19" width="253">Nunca vazio</td> 
   <td height="19" width="412">Número de alunos que concluíram o OA.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Número de alunos que progrediram &gt;= N %</td> 
   <td height="38" width="253">Nunca vazio</td> 
   <td height="38" width="412">Número de alunos que progrediram &gt;= N % (valores).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Número de alunos com data de vencimento em N dias</td> 
   <td height="39" width="253">Nunca vazio</td> 
   <td height="39" width="412">Número de alunos com data de vencimento em N dias (valores).</td> 
  </tr> 
 </tbody> 
</table>

### Resumo de aprendizado II

| Nome da coluna | Tipo de valor | Descrição |
|---|---|---|
| Tipo | Todos, Programa de aprendizado, Certificado, Curso. | O tipo de OA para o qual a tabela Resumo de aprendizado deve mostrar dados. |
| Campo(perfil) agrupável | Nunca vazio | O perfil para o qual a tabela de resumo de aprendizado deve mostrar dados. |
| Nome do gerente | Nunca vazio | O nome do gerente cujos dados de envolvimento do OA subordinados devem ser exibidos na tabela de resumo de aprendizado |
| Rótulos de linha | Nunca vazio | O nome do aluno com a lista de OAs que o aluno está inscrito. |
| Número de objetos de aprendizado inscritos | Nunca vazio | O número de objetos de aprendizado que o aluno está inscrito. |
| Número de objetos de aprendizado iniciados | Nunca vazio | O número de objetos de aprendizado iniciados peloo aluno. |
| Número de objetos de aprendizado concluídos | Nunca vazio | Número de objetos de aprendizado concluídos pelo aluno. |
| Número de objetos de aprendizado que progrediram >= N % | Nunca vazio | Número de objetos do aluno que o aluno progrediu >= N %. |
| Número de objetos de aprendizado com data de vencimento em N dias | Nunca vazio | Número de objetos de aprendizado com data de vencimento em N dias. |

### Resumo de conformidade

| Nome da coluna | Tipo de valor | Descrição |
|---|---|---|
| Tipo | Todos, Programa de aprendizado, Certificado, Curso. | O tipo de OA para o qual a tabela Resumo de aprendizado deve mostrar dados. |
| Rótulos de linha (coluna do lado esquerdo) | Nunca vazio | O nome do aluno com a lista de OAs que o aluno está inscrito. |
| Rótulos de linha (coluna do lado esquerdo) | Nunca vazio | O nome do aluno com a lista de OAs que o aluno está inscrito. |

### Transcrição de habilidade

| .Nome da coluna | Tipo de valor | Descrição |
|---|---|---|
| Nome | Nunca vazio | Nome do aluno |
| e-mail | Nunca vazio | Endereço de e-mail do aluno |
| Adobe ID | Pode estar vazio | Adobe ID do aluno |
| ID exclusiva do usuário | Pode estar vazio | ID exclusiva do usuário do aluno. Essa coluna é baseada na configuração de back-end, se ativada/desativada no nível da conta. |
| Habilidade | Nunca vazio | Nome da habilidade atribuída ao aluno. |
| Nível da habilidade | Nunca vazio | Nível da habilidade atribuída ao aluno. |
| Créditos necessários | Nunca vazio | Total de créditos necessários para o aluno obter a habilidade. |
| Créditos obtidos | Nunca vazio | Total de créditos obtidos pelo aluno para a habilidade. |
| Porcentagem de conclusão | Nunca vazio | Porcentagem de progresso para obter a habilidade. |
| Data da atribuição (Fuso horário UTC) | Nunca vazio | Data na qual a habilidade foi atribuída ao aluno. |
| Data da obtenção (Fuso Horário UTC) | Nunca vazio | Data em que o aluno obteve a habilidade. |
| userState | Nunca vazio | Estado do usuário do aluno: Ativo/Excluído/Suspenso. |
| Campo Ativo Agrupável | Pode estar vazio | Para cada campo ativo agrupável na conta, haverá uma coluna, onde o nome da coluna é o do campo ativo e o valor será o valor específico que o aluno tem para esse campo. |
| Nome do gerente | Pode estar vazio | O nome do gerente do aluno. |

### Resumo de habilidade I

| Nome da coluna | Tipo de valor | Descrição |
|---|---|---|
| Depois | Nunca vazio | Número de alunos que alcançaram a habilidade antes do número de dias inserido (valor) que precisa ser atualizado. |
| Nome | Todos ou qualquer nome do aluno | O nome do aluno que tem uma habilidade atribuída. |
| Nome do gerente | Nunca vazio | O nome do gerente cujos dados de envolvimento de habilidade subordinados devem ser exibidos na tabela de resumo de habilidade. |
| Rótulos de linha | Nunca vazio | O nome da habilidade com a lista de alunos atribuídos à habilidade. |
| Número de usuários que devem ter essa habilidade | Nunca vazio | Número de alunos atribuídos à habilidade. |
| Número de usuários que obtiveram essa habilidade | Nunca vazio | Número de alunos que obtiveram a habilidade. |
| Número de alunos cujas habilidades precisam ser atualizadas | Nunca vazio | Número de alunos cuja habilidade precisa ser atualizada. |
| Porcentagem de conformidade (com base na habilidade obtida) | Nunca vazio | A porcentagem de progresso da habilidade atribuída. |

### Resumo de habilidade II

| Nome da coluna | Tipo de valor | Descrição |
|---|---|---|
| Depois | Nunca vazio | Número de alunos que obtiveram a habilidade antes do número de dias inserido (valor), o qual precisa ser atualizado. |
| Habilidade | Todos ou qualquer nome de habilidade | Os nomes das habilidades atribuídos aos alunos. |
| Nome do gerente | Nunca vazio | O nome do gerente cujos dados de envolvimento de habilidade subordinados devem ser exibidos na tabela de resumo de habilidade. |
| Rótulos de linha | Nunca vazio | O nome do aluno com a lista de habilidades atribuídas. |
| Número de habilidades que cada usuário deve ter | Nunca vazio | Número de habilidades atribuídas ao aluno. |
| Número de habilidades que cada usuário possui | Nunca vazio | Número de habilidades obtidas pelo aluno. |
| Número de habilidades que precisam de atualização | Nunca vazio | Número de alunos cuja habilidade precisa ser atualizada. |
| Porcentagem de conformidade | Nunca vazio | A porcentagem de progresso da habilidade atribuída. |

* Às vezes, os administradores podem marcar a conclusão de um objeto de aprendizado manualmente (especialmente nos cursos da sala de aula) muito depois da aula. Nesse cenário, se Exportar dados estiver configurado para exportar LT diariamente, a data real de conclusão já pode ter passado e, portanto, a exportação nunca receberá registros de conclusão marcados como concluídos muito depois que a aula aconteceu. Quando isso for detectado, considere exportar a transcrição de uma determinada data de início até a data (por demanda) na interface do usuário e, em seguida, levá-la ao aplicativo downstream para “processamento atrasado”. Ao fazer isso, talvez seja necessário ignorar os registros que já foram processados.
* Várias tentativas para um módulo depende se ele está ativado para esse LO. Quando ativado, o que você vê agora em uma linha CSV relacionada a um módulo é uma tentativa. Nem todas as tentativas em um dia podem ser informadas e, portanto, você pode ver o número total de tentativas aumentando em mais de uma. Além disso, uma tentativa pode não necessariamente melhorar uma pontuação e, em um dado momento, você só terá a melhor pontuação.
