---
description: As transcrições do aluno no Adobe Learning Manager (ALM) permitem que os administradores monitorem o progresso do aluno em cursos, módulos, programações de aprendizado e certificações. Ele oferece suporte a avaliações de desempenho, monitoramento de conformidade, auditorias e emissão de relatórios externos. O relatório oferece um resumo completo do envolvimento e do desempenho de um aluno.
jcr-language: en_us
title: Transcrições do aluno no Adobe Learning Manager
source-git-commit: 85799b32f3a24fc0e6beb34ae39a502ff8e7a7b4
workflow-type: tm+mt
source-wordcount: '4354'
ht-degree: 8%

---


# Transcrições do aluno no Adobe Learning Manager

## Visão geral

As transcrições do aluno no Adobe Learning Manager (ALM) permitem que os administradores controlem o progresso do aluno em um nível granular em cursos, módulos, programações de aprendizado e certificações. Os dados de transcrição ajudam nas revisões de desempenho, no controle de conformidade, nas auditorias e nas necessidades de emissão de relatórios externos.

>[!NOTE]
>
>As transcrições do aluno estão disponíveis para download por administradores, administradores personalizados, gerentes ou alunos.

No caso dos alunos, eles devem iniciar as configurações do perfil e baixar as transcrições de aprendizado como um arquivo do Excel. Essa transcrição, gerada para um aluno individual, detalha sua jornada de aprendizado pessoal. Inclui os nomes dos caminhos de aprendizado, cursos, instâncias e módulos, juntamente com as principais datas, como inscrição, conclusão e prazos finais. Ele também acompanha o progresso dos alunos por meio de status, notas, pontuações no quiz (incluindo as pontuações mais altas e máximas) e tentativas realizadas. Além disso, ele mostra IDs de treinamento, durações, datas de cancelamento da inscrição, preços e comentários de envio. Este relatório fornece uma visão geral abrangente do envolvimento e do desempenho de um único aluno.

As organizações podem usar as transcrições do aluno para adicionar os dados do comportamento de aprendizado a um data warehouse corporativo, onde é possível combinar dados de aprendizado com outros dados corporativos para analisar correlações entre o comportamento de aprendizado e outros dados de processo.

## Finalidade e benefícios

* Cria registros prontos para auditoria para requisitos normativos com carimbos de data e hora e comprovantes de conclusão.
* Conecta atividades de aprendizado ao desenvolvimento e à aquisição de habilidades dos funcionários.
* Controla o status de certificação para funções que exigem treinamento obrigatório.
* Suporta medição quantitativa da eficácia do programa de aprendizado.

## Casos de uso de transcrições do aluno

As transcrições do aluno no Adobe Learning Manager controlam o treinamento, a conformidade e o desenvolvimento de habilidades, permitindo que os departamentos verifiquem a conclusão e avaliem a eficácia do programa em toda a organização.  Veja alguns casos de uso que as transcrições do aluno abordam:

* Uma organização de serviços financeiros deve fornecer evidências de que todos os funcionários voltados para o cliente concluíram o treinamento obrigatório de conformidade antes do prazo regulamentar.
* O departamento de TI precisa avaliar os recursos atuais de programação Java em relação aos requisitos futuros do projeto.
* O HR deseja avaliar a eficácia do novo programa de integração de funcionários em diferentes departamentos.
* A equipe de operações precisa garantir que todos os técnicos de campo mantenham as certificações de segurança necessárias.

## Controle de acesso e permissões

**Administradores**

* Pode gerar transcrições para todos os alunos em todos os catálogos.
* Pode acessar todas as funções de relatório, mas pode ter restrições de catálogo ou grupo de usuários.
* Administradores personalizados: acesso limitado por escopo e permissões atribuídos.

**Restrições baseadas em escopo**

* Os administradores personalizados podem exibir apenas transcrições para alunos em seus grupos de usuários atribuídos.
* Os relatórios incluirão apenas objetos de aprendizado de catálogos que o administrador tenha permissão para acessar.

## Como gerar transcrições do aluno

1. Faça logon no Adobe Learning Manager como administrador.
2. Selecione **[!UICONTROL Relatórios]** no menu de navegação à esquerda.
3. Selecione **[!UICONTROL Relatórios Personalizados]** em Relatórios e selecione **[!UICONTROL Relatórios do Excel]**.
4. Selecione **[!UICONTROL Transcrições Do Aluno]**.
5. Selecione **[!UICONTROL Gerar Novo]**.
6. Selecione o intervalo de datas para o qual você precisa da transcrição gerada. Por padrão, a data **[!UICONTROL De]** é a data de registro do aluno e a data **[!UICONTROL Até]** é sempre a data atual. É possível modificar apenas a data inicial a partir de quando você precisa dos dados.
7. Selecione o seguinte:
a. Selecione os nomes dos alunos na seção **[!UICONTROL Selecionar alunos]**. Você pode selecionar usuários ou grupos de usuários ou copiar e colar os endereços de e-mail dos alunos para os quais deseja gerar transcrições. Consulte a seção [Gerar transcrição do aluno](#generate-learner-transcript-using-copy-paste) usando copiar e colar para obter mais informações.
b. Selecione catálogos específicos na lista suspensa **[!UICONTROL Selecionar catálogos]**. A transcrição só é baixada para os catálogos especificados.\
   c. Selecione o **[!UICONTROL Status de inscrição]**. Essa lista suspensa contém as seguintes opções:

       * Selecionar Tudo
       * Concluído
       * Em Andamento
       * Não Iniciado
       * Não Inscrito
   &#x200B;8. Opções avançadas: selecione **[!UICONTROL Opções avançadas]** para baixar as transcrições para incluir o seguinte:

   a. Baixe as transcrições dos alunos que foram excluídos de uma conta marcando a caixa de seleção **[!UICONTROL Incluir alunos excluídos]**.
b. Baixe as informações de nível do módulo na transcrição do aluno ativando a caixa de seleção **[!UICONTROL Habilitar informações de nível do módulo]**. Nesse caso, os nomes dos módulos e o tempo gasto em cada módulo são obtidos como parte da transcrição se essa opção estiver ativada.
c. Baixe dados de habilidades e folhas de resumo ativando a opção **[!UICONTROL Incluir dados de habilidades e folhas de resumo]**. Consulte a seção Relatórios do Excel para obter mais informações.
&#x200B;9. Você também pode selecionar os valores de coluna a serem preenchidos no relatório. Isso fornece flexibilidade para baixar relatórios com valores de coluna específicos, conforme necessário. Selecione as colunas no menu suspenso.
As transcrições são geradas e baixadas no computador como arquivos .zip quando os dados da habilidade não estão incluídos. Se a caixa de seleção Dados de habilidades estiver ativada, as transcrições serão geradas e baixadas como . arquivos xlsx.

### Gerar transcrição do aluno usando copiar e colar

Obter transcrições do aluno se torna um processo tedioso, pois podem ser obtidas apenas para um aluno ou grupo de usuários, um de cada vez. Aqui, com o recurso copiar e colar, você pode copiar a lista de IDs de e-mail do aluno e colá-la de uma só vez.

1. Selecione a guia **[!UICONTROL IDs de email]** para inserir a lista copiada de IDs de email exclusivas.
2. Cole IDs de e-mail exclusivas dos alunos que você deseja adicionar, separadas por vírgula, ponto-e-vírgula ou quebra de linha.
3. Selecione **[!UICONTROL Validar Ids de Email]** para verificar se a ID de email inserida é válida. Caso a ID de e-mail inserida esteja incorreta, ela será destacada em vermelho juntamente com uma mensagem de validação.

   >[!NOTE]
   >
   >O botão Gerar permanecerá desativado a menos que todas as IDs de e-mail inseridas estejam corretas.

4. Selecione **[!UICONTROL Gerar]** para gerar transcrições do aluno para todas as IDs de e-mail mencionadas.

   >[!NOTE]
   >
   >Gerar transcrições do aluno pode ser combinado para IDs de e-mail inseridas na guia Usuários e IDs de e-mail.

### O que o relatório de transcrições do aluno contém

O relatório de transcrição do aluno é uma combinação de informações relacionadas ao usuário, à inscrição e aos objetos de aprendizado.
As tabelas a seguir descrevem cada tipo:

**Informações relacionadas ao usuário**

As colunas a seguir identificam o aluno.

| Campo | Descrição |
|---|---|
| Nome | Nome do aluno. |
| Email | Endereço de e-mail do aluno |
| Adobe ID | Este campo é preenchido somente quando os usuários fazem logon usando sua Adobe ID. Se eles acessarem o Adobe Learning Manager por meio de um [Logon Único (SSO)](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) definido pela organização, o campo do Adobe ID permanecerá em branco. |
| ID exclusiva do usuário | A ID exclusiva do usuário é uma ID externa gerada pelas contas caso elas não tenham IDs de email de todos os usuários ou IDs de email exclusivas de todos os usuários. <br>O campo ID exclusiva do usuário é um campo opcional que pode ser habilitado para uma conta. O objetivo principal desse campo é permitir que as contas marquem cada usuário com uma ID exclusiva para rastreá-los, atualizar registros de usuário por meio de APIs, auditar ou sincronizar dados em fluxos de trabalho automatizados. A marcação de cada usuário acontece por meio da importação de CSV dos usuários.</br><br>Se uma conta tiver optado por uma ID de usuário exclusiva, os relatórios, como transcrições do aluno, a Adobe Learning Manager fornecerão a coluna nos relatórios.</br> |

**Informações relacionadas à inscrição**

As colunas a seguir capturam atividade, progresso ou tentativas.

| Campo | Descrição |
|---|---|
| Data de inscrição (fuso horário UTC) | Data e carimbo de hora da inscrição do aluno no tipo de Objeto de aprendizado, que é curso, certificação ou Caminho de aprendizado. |
| Marcar data de conclusão (fuso horário UTC) | Carimbo de data e hora de quando um professor marca uma sessão ou módulo como concluído. Observe que se uma sessão não tiver ocorrido, a coluna aparecerá em branco no relatório. Além disso, se uma sessão tiver ocorrido e o professor não tiver marcado a sessão como concluída, a coluna aparecerá em branco no relatório. |
| Data de início (fuso horário UTC) | Data e hora em que o aluno iniciou o Objeto de aprendizado. Vazio significa que o aluno ainda não iniciou isso. |
| Data de conclusão (fuso horário UTC) | Data e hora em que o aluno concluiu isso. Vazio significa que o aluno ainda não concluiu isso. |
| Prazo de conclusão (Fuso horário central da Europa) | Data e hora em que o aluno deve concluir este Objeto de aprendizado. Vazio significa que não há prazo para isso. |
| Em atraso | Status de atraso atual do aluno inscrito no Objeto de aprendizado. Sim/Não |
| Status | Indica o status do aluno ao realizar o curso, certificação ou caminho de aprendizado.  Os status disponíveis são Não iniciado, Não inscrito, Em andamento ou Concluído. |
| % de progresso | % do progresso atual do aluno em relação ao curso, certificação ou caminho de aprendizado. |
| Tempo gasto (minutos) | O tempo de aprendizado gasto pelo aluno no OA, as linhas no nível do módulo exibem o tempo gasto de aprendizado no módulo individual. As linhas do curso/caminho de aprendizado/nível de certificado exibem o tempo de aprendizado gasto agregado. |
| Nota | Indica o sucesso do aluno. &#39;Aprovado&#39;, se o usuário atendeu aos critérios de sucesso para isso, caso contrário, &#39;Reprovado&#39;. |
| Pontuação_no_questionário | A coluna é usada para gravar a pontuação da tentativa mais recente de um quiz. Por exemplo, se um usuário fizer várias tentativas (por exemplo, pontuações 10, 50 e 30 em três tentativas), a coluna Quiz_score exibirá a pontuação da última tentativa, que é 30. Suponha que um quiz tenha uma pontuação máxima de 100 e um usuário faça três tentativas, pontuando 30, 60 e 90. A coluna Quiz_score mostrará 90 (a pontuação mais recente), enquanto a Highest_Quiz_score mostrará 90 (a melhor pontuação em todas as tentativas) e Quiz_score_max permanecerá 100 (a pontuação máxima possível). |
| Quiz_score_max | A coluna Quiz_score_max representa a pontuação máxima possível que pode ser obtida para um quiz ou módulo específico. Como Quiz_score_max permanece constante, é útil em relatórios para mostrar a pontuação total atingível para um quiz ou módulo, independentemente do desempenho do usuário. |
| Highest_Quiz_score | A coluna Highest_Quiz_score representa a maior pontuação obtida por um usuário em todas as tentativas de um quiz específico. Por exemplo, se um usuário fizer três tentativas, pontuando 10, 20 e 15, a Highest_Quiz_score exibirá 20, pois é a maior pontuação obtida. |
| Highest_Quiz_score_max | A pontuação máxima possível associada à maior tentativa de questionário feita por um aluno em várias tentativas. Não é a pontuação mais alta que o aluno obteve. Em vez disso, ele captura a pontuação máxima possível na tentativa em que o aluno obteve a pontuação mais alta. |
| Tentativas realizadas | O número total de tentativas realizadas pelo aluno até agora para este módulo. |
| Máximo de tentativas permitidas | O número máximo de tentativas permitidas para o aluno consumir o módulo. |
| Comentários da inscrição | Comentários do gerente de um aluno após concluírem um objeto de aprendizado.<br>Os dados de comentários de envio fornecidos pelo professor estão incluídos no módulo de envio de arquivos. Consulte <a href="https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/instructor/modules#filesubmissionforactivitymodules">Modules-Adobe Learning Manager para obter mais informações.</a></br> |
| Origem da Conclusão | Refere-se à origem ou ao método pelo qual é registrada a conclusão de um curso, programa de aprendizado ou certificação de um aluno. Isso ajuda os administradores a entender como a conclusão foi alcançada ou registrada no sistema. A coluna identifica se a conclusão foi relatada automaticamente, registrada automaticamente ou facilitada por uma função ou configuração específica. <b>Observação:</b> para fluxos de trabalho de participação no conector VC, quando um aluno é marcado como participado automaticamente, a origem exibirá “SELF, (learner_email)”. |
| Comentário de conclusão | Os comentários feitos pelo administrador ao marcar um aluno como concluído após concluir um curso, certificação ou caminho de aprendizado. O administrador pode adicionar os comentários de conclusão de um ou vários alunos. |

**Informações relacionadas aos Objetos de Aprendizado**

Eles se referem a cursos, módulos, caminhos de aprendizado, certificações e assim por diante.

| Campo | Descrição |
|---|---|
| Nome do plano de aprendizado | Título do Plano de Aprendizado. |
| LP/Certificação/Curso | O título do Objeto de aprendizado. |
| Tipo | O tipo de Objeto de aprendizado no qual o usuário foi inscrito. Por exemplo,<ul><li>Caminho do aprendizado</li><li>Certificação</li><li>Curso</li></ul> |
| Caminho incorporado | Um caminho incorporado é um tipo de caminho de aprendizado incluído como parte de outro curso     ou um Caminho de aprendizado. O campo indica que um aluno está concluindo esse caminho de aprendizado como parte de outro caminho de aprendizado, em vez de uma atribuição individual. |
| Curso | Nome do curso no qual o usuário está inscrito. Quando estiver vazia, a linha representa um Caminho de Certificação ou de Aprendizado. <br><b>Observação:</b> embora Caminhos de Aprendizado e Certificações    sejam compostos por cursos individuais ou caminhos de aprendizado aninhados, cada componente mantém seu próprio registro independente. Isso garante que os dados de progresso, conclusão e relatório sejam rastreados separadamente para os elementos pai e filho.</br> |
| ID exclusiva do OA | A ID exclusiva do objeto de aprendizado. Será necessário se o cliente tiver o LO em um sistema externo que tenha sua própria ID. Isso é útil se você deseja mapear o LO Id do sistema externo e o LO do Adobe Learning Manager.<br>Um administrador pode habilitar a opção Ids exclusivas do objeto de aprendizado na página Configurações. Quando ativada, o Adobe Learning Manager atribui uma ID exclusiva a um objeto de aprendizado sempre que um autor cria um curso, certificação ou caminho de aprendizado. </br> |
| Instância | O nome da instância do usuário do Objeto de aprendizado está inscrito. |
| Critérios de seleção | Base da inscrição (como este aluno se inscreveu neste Objeto de Aprendizado).<br>No Adobe Learning Manager, os alunos podem se inscrever em objetos de aprendizado por meio de vários métodos: Inscrição Indicada pelo Gerente: os gerentes indicam os alunos para cursos específicos. Os alunos não podem se inscrever nesses cursos.</br><ul><li>Inscrição aprovada pelo gerente: os alunos se inscrevem nos cursos, mas a inscrição exige a aprovação do gerente.</li><li>Autoinscrição: os alunos se inscrevem diretamente nos cursos sem precisar de aprovação.</li><li>Inscrição do administrador: os administradores inscrevem manualmente os alunos nos cursos.</li></ul> |
| Módulo | Nome do módulo nos cursos. Apenas os módulos com status Concluído ou Em andamento são exibidos no relatório. Se o status for Não Iniciado ou Cancelar Inscrição, a coluna Módulo permanecerá vazia.<br>Baixe informações de nível de módulo na transcrição do aluno marcando a caixa de seleção <b>Habilitar informações de nível de módulo</b>. Nesse caso, os nomes dos módulos e o tempo gasto em cada módulo são obtidos como parte da transcrição se esta opção estiver habilitada.</br> |
| ID do módulo | A ID exclusiva do módulo.<br><b>Observação:</b> a coluna ID do módulo aparece no relatório somente se você selecionou a caixa de seleção Incluir informações do módulo ao gerar a transcrição.</br> |
| Versão | A versão do módulo se refere à versão específica de um módulo com o qual um aluno interagiu. Isso é particularmente útil quando um módulo passou por atualizações ou alterações, pois permite que os administradores controlem qual versão do módulo foi acessada pelo aluno.<br>Quando um autor carrega uma nova versão de um módulo, o Adobe Learning Manager o trata como uma nova versão do módulo existente. Isso permite que o conteúdo seja atualizado sem interromper todos os alunos.</br><br>A Versão aparecerá se a caixa de seleção <b>Habilitar informações de nível de módulo</b> tiver sido selecionada ao gerar o relatório.</br><br>Consulte <a href="https://elearning.adobe.com/2023/03/updating-the-module-in-adobe-learning-manager-how-to-replace-a-content-module-in-a-course-without-disturbing-the-users-progress" />Atualizando um módulo no Adobe Learning Manager</a> para obter mais informações.</br> |
| Tipo de entrega | Indica como o módulo é fornecido: misto, sala de aula ou sala de aula virtual. |
| Idioma | Idioma em que o módulo é consumido pelo aluno. Esta coluna mostra o valor somente para módulos de e-learning. |
| Em atraso | Status de atraso atual do aluno inscrito no Objeto de aprendizado. Sim/Não |
| Nota | Indica o sucesso do aluno. &#39;Aprovado&#39;, se o usuário atendeu aos critérios de sucesso para isso, caso contrário, &#39;Reprovado&#39;. |

>[!INFO]
>
>As seguintes colunas estão ocultas nas transcrições do aluno:
>
>* Número de inscrições
>* Contagem iniciada
>* Contagem de Conclusões
>* Vence em N dias
>* Vence em N dias para o usuário
>* Contagem de (Progresso maior que N %)
>* Contagem de (Progresso maior que N %) para o usuário
>
>Essas colunas só aparecem se você selecionou Incluir dados de habilidades e folhas de resumo ao gerar a transcrição. Essas colunas são usadas para calcular os detalhes resumidos de um aluno inscrito em um Objeto de aprendizado.

| Campos | Descrição |
|---|---|
| ID do treinamento | Um identificador exclusivo gerado pelo sistema atribuído à inscrição de cada aluno em um curso, certificado ou caminho de aprendizado específico. Se um aluno se inscrever novamente no mesmo curso, uma nova ID de treinamento será gerada. Um aluno pode ter várias IDs de treinamento para o mesmo curso. |
| Duração do treinamento ou módulo (em minutos) | Esta coluna mostra a duração esperada (em minutos) de um curso, módulo ou atividade de treinamento conforme definido ao criar o curso. Não é o tempo real que um aluno gasta, mas a duração configurada/atribuída que representa quanto tempo o treinamento deve levar. <br>Esta coluna mostra a duração total (em minutos) do item de aprendizado atribuído, que pode ser um caminho de aprendizado ou um curso individual.</br><br><b>Duração do caminho de aprendizado:<b> se o item de treinamento for um caminho de aprendizado, sua duração será calculada como a soma das durações de todos os cursos dentro do caminho de aprendizado.</br><br>Exemplo: se Curso 1 = 50 minutos e Curso 2 = 60 minutos, a Duração do Caminho de Aprendizado = 110 minutos.</br><br><b>Duração individual do curso:</b>Se o item de treinamento for um curso individual (não parte de um caminho de aprendizado), a duração refletirá o tempo necessário apenas para esse curso.</br> |
| Embedded_Course_ID | A ID do curso que faz parte de um caminho de aprendizado ou de qualquer outro curso.<br>A coluna é preenchida quando a linha representa um Caminho de Aprendizado ou a própria certificação. Ela mostra as IDs dos cursos individuais incorporados no Caminho de Aprendizado ou na certificação. Não é populado quando a própria linha é um curso apenas, pois não há itens inseridos.</br> |
| ID do caminho incorporado | A ID do caminho no qual o curso incorporado existe.<br>A coluna identifica a ID exclusiva de Caminhos de Aprendizado inseridos. Ajuda a rastrear cursos nos Caminhos de Aprendizado e fornece visibilidade da estrutura hierárquica dos Caminhos de Aprendizado.</br> |
| Data de cancelamento da inscrição (fuso horário central da Europa) | Data do cancelamento da inscrição pelo aluno no tipo de Objeto de aprendizado. |
| Preço ($) | O preço do Objeto de aprendizado pelo qual ele é comprado no catálogo do curso. Para que esta coluna apareça na transcrição do aluno, o administrador deve ativar a caixa de seleção Ativar preços para cursos/caminhos de aprendizado/certificações nas configurações da conta. |

## Relatórios do Excel

A caixa de diálogo Transcrições do aluno também permite que você baixe dados de habilidades e folhas de resumo como arquivos do Excel. Marque a caixa de seleção **[!UICONTROL Incluir dados de habilidades e folhas de resumo]** e selecione **[!UICONTROL Gerar]** para baixar um arquivo do Excel com as seguintes folhas:

* Resumo de Aprendizado I
* Resumo de Aprendizado II
* Resumo de conformidade
* Transcrição de habilidade
* Resumo de habilidade I
* Resumo de Habilidades II

### O que a planilha Resumo do aprendizado I contém

Acompanhe os caminhos de aprendizado, cursos ou certificações utilizados ativamente. Acompanhe as atividades em andamento, bem como as datas de vencimento iminentes do treinamento.

* Número de alunos inscritos: indica quantos alunos foram inscritos em um objeto de aprendizado específico (curso, caminho de aprendizado ou certificação), independentemente de terem iniciado ou não.
* Número de alunos que iniciaram: mostra a contagem de alunos que iniciaram ou iniciaram o curso, a certificação ou o caminho de aprendizado.
* Número de alunos que concluíram: exibe quantos alunos concluíram o treinamento com êxito e atenderam a todos os seus critérios de conclusão.
* Número de alunos que progrediram ≥ N%: reflete a contagem de alunos que alcançaram pelo menos o limite de progresso especificado (por exemplo, 70%) no treinamento, mesmo se não o tiverem concluído.
* Número de alunos com data de vencimento em N dias: indica quantos alunos têm treinamento vencido nos próximos “N” dias (por exemplo, 7 dias), útil para identificar futuros prazos.

### Como interpretar os dados

Este relatório do Resumo de aprendizado I rastreia dois caminhos de aprendizado atribuídos ao aluno.

* O usuário está inscrito em dois Caminhos de aprendizado e iniciou ambos.
* Nenhum dos caminhos de aprendizado foi concluído ainda.
* O aluno ainda não progrediu além do limite de 70% em nenhum caminho.
* Nenhuma data de vencimento está nos próximos sete dias para nenhum dos treinamentos.

### O que a planilha Resumo de aprendizado II contém

Controle a atividade de aprendizado por aluno. Rastreie inscrições, atividades em andamento e datas de vencimento dos alunos.

* Número de objetos de aprendizado inscritos: contagem total de objetos de aprendizado (LOs) em que o aluno está inscrito em cada curso, certificação ou caminho de aprendizado. conta separadamente.
* Número de objetos de aprendizado iniciados: indica quantos dos objetos de aprendizado inscritos o aluno iniciou ou começou.
* Número de objetos de aprendizado concluídos: mostra quantos OAs iniciados o aluno concluiu totalmente.
* Número de objetos de aprendizado que progrediram ≥ N%: reflete o número de OAs nos quais o aluno alcançou pelo menos o limite de progresso especificado (neste caso, 70%).
* Número de objetos de aprendizado com data de vencimento em N dias: identifica os OAs que vencem no próximo número definido de dias (nesse caso, 7 dias), ajudando a rastrear os prazos que se aproximam.

### Como interpretar os dados

* O aluno está inscrito em dois objetos de aprendizado e iniciou ambos.
* Nenhum objeto de aprendizado foi concluído.
* O aluno ainda não alcançou 70% de progresso em nenhum deles.
* Nenhum dos objetos de aprendizado vence nos próximos 7 dias.

### O que a planilha Resumo de conformidade contém

Acompanhe os alunos com datas de vencimento iminentes dos principais cursos, caminhos de aprendizado ou certificações.

| Coluna | Descrição |
|---|---|
| Tipo | O tipo de OA para o qual a tabela Resumo do aprendizado deve mostrar dados. |
| Rótulos de linha (coluna do lado esquerdo) | O nome do aluno com a lista de OAs nos quais o aluno está inscrito. |

### O que a folha de transcrição de habilidade contém

| Coluna | Descrição |
|---|---|
| Nome | Nome completo do aluno associado à transcrição da habilidade. |
| Email | Endereço de e-mail do aluno. |
| ID exclusiva do usuário | Identificador exclusivo definido pela organização para o aluno. |
| Habilidade | O nome da habilidade atribuída ao aluno (por exemplo, Programação Java, Liderança). |
| Nível da habilidade | O nível de experiência na habilidade que o aluno deve atingir (por exemplo, Iniciante, Intermediário, Avançado). |
| Créditos necessários | Número de créditos de aprendizado necessários para atingir o nível de habilidade atribuído. |
| Créditos obtidos | Número de créditos que o aluno ganhou para concluir o nível de habilidade atribuído. |
| Porcentagem de conclusão | A porcentagem de créditos necessários que o aluno concluiu. |
| Data da Atribuição (UTC) | A data em que a habilidade foi atribuída ao aluno. |
| Data da obtenção (UTC) | A data em que o aluno obteve os créditos necessários e atendeu aos critérios de nível de habilidade. |
| Nome do gerente | Nome do gerente do aluno que supervisiona o progresso do aprendizado. |

### O que a planilha Resumo de habilidades I contém

| Coluna | Descrição |
|---|---|
| Depois | Representa o número de alunos que obtiveram uma habilidade antes de um período definido (em dias), além do qual a habilidade é considerada desatualizada ou requer atualização. Útil para identificar alunos com habilidades que se aproximam ou expiraram.<br>Consulte <a href="https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/admin/skills-levels">níveis de habilidade</a> para obter mais informações. |
| Nome | Nome completo do aluno ao qual a habilidade está atribuída. |
| Nome do gerente | Nome do gerente de relatórios do aluno. |
| Rótulos de linha | O nome da habilidade específica atribuída aos alunos que aparecem nesta linha. Usado como um cabeçalho de agrupamento para resumir os dados de habilidade do aluno em cada categoria de habilidade. |
| Número de usuários que devem ter essa habilidade | Número total de alunos aos quais foi atribuída a habilidade específica. |
| Número de usuários que obtiveram essa habilidade | Número de alunos que concluíram com êxito os objetos de aprendizado necessários para obter a habilidade. |
| Número de alunos cujas habilidades precisam ser atualizadas | O número de alunos cujas datas de obtenção de habilidades excedem o limite de atualização definido. |
| Porcentagem de conformidade (com base na habilidade obtida) | A taxa de conformidade ou adoção da habilidade. |


### O que a planilha Resumo de habilidades II contém

| Coluna | Descrição |
|---|---|
| Depois | Número de habilidades obtidas pelo aluno antes do limite de atualização definido (em dias). Isso identifica habilidades que podem estar desatualizadas e que precisam ser atualizadas. |
| Habilidade | Nome da(s) habilidade(s) atribuída(s) aos alunos. Isso pode estar vinculado a um ou mais objetos de aprendizado, como cursos, certificações ou caminhos de aprendizado. |
| Nome do gerente | O nome do gerente direto do aluno. |
| Rótulos de linha | O nome completo do aluno. Para cada aluno, as habilidades e o progresso são exibidos nas colunas subsequentes. |
| Número de habilidades que cada usuário deve ter | Número total de habilidades atribuídas ao aluno. |
| Número de habilidades que cada usuário possui | Número total de habilidades que o aluno obteve com êxito por meio da conclusão do(s) Objeto(s) de aprendizado associado(s). |
| Número de habilidades que precisam de atualização | O número de habilidades obtidas que ultrapassaram a duração da atualização e agora requerem revalidação. Esse valor ajuda a controlar as necessidades de renovação do treinamento para conformidade ou desenvolvimento contínuo. |
| Porcentagem de conformidade | Indica o nível de conformidade geral do aluno com base na obtenção de habilidade. |

## Histórico de downloads da transcrição do aluno

O histórico de downloads de transcrição do aluno permite que os administradores controlem quem baixou a transcrição de cada aluno e quais usuários acessaram. Esse recurso é benéfico principalmente em configurações corporativas e voltadas para a conformidade, em que várias partes interessadas podem precisar visualizar registros de aprendizado.

Após baixar uma transcrição do aluno, a página Transcrições do aluno lista todas as transcrições geradas por qualquer pessoa na plataforma.

A lista exibe os seguintes atributos:

* De e Para: duração das transcrições a serem baixadas.
* Gerado por: O email do usuário que baixou o relatório ou solicitou o download.
* Alunos: os alunos ou grupos de alunos cujas transcrições devem ser baixadas.
* Filtros Aplicados: Os filtros que foram aplicados para o Status da Inscrição.
* Dados adicionais incluídos: os dados adicionais (alunos excluídos, informações do módulo, dados de habilidades e folhas de resumo) que o administrador solicitou da opção Avançado no modal Adicionar transcrição do aluno
* Status: Baixado, enfileirado ou em andamento.
* Cancelar: cancele a geração do relatório a qualquer momento.

## Considerações adicionais para transcrições do aluno

As transcrições do aluno incluem vários comportamentos dos quais os administradores devem estar cientes:

**Exibição do Caminho de Aprendizado e do progresso do curso**

Todos os cursos que fazem parte de um caminho de aprendizado (LP) aparecerão na transcrição do aluno, mesmo que o aluno tenha feito progresso em apenas um dos cursos. Isso garante a visibilidade completa de um caminho de aprendizado, mesmo quando o progresso está parcialmente concluído.

**Dados de alunos excluídos**

Se um aluno foi excluído da plataforma, a transcrição não mostrará seus registros em nenhum relatório gerado para o grupo de usuários do qual ele fazia parte. Isso significa que os registros de alunos excluídos serão excluídos de quaisquer relatórios filtrados criados usando os filtros de grupo de usuários.

Mas você ainda pode baixar os dados dos alunos excluídos. Se você selecionou a opção **[!UICONTROL Incluir alunos excluídos]** ao definir os filtros para gerar o relatório, poderá baixar o relatório dos alunos excluídos.

**Comportamento dos administradores personalizados**

Administradores personalizados com um escopo definido (por exemplo, limitado a catálogos ou grupos de usuários específicos) verão dados de transcrição filtrados com base em seu escopo:

* Escopo do grupo de usuários: somente os alunos do grupo de usuários com escopo do administrador personalizado serão incluídos no relatório.
* Escopo do catálogo: somente os objetos de aprendizado (cursos, certificações e caminhos de aprendizado) atribuídos aos catálogos com escopo serão incluídos no relatório.
* Colunas filtradas: as colunas permanecem as mesmas. Somente as linhas terão o escopo definido com base nos escopos de catálogos e grupos de usuários.

Isso garante que os administradores personalizados com escopo exibam apenas os dados e o conteúdo de aprendizado do aluno que estão autorizados a gerenciar.

**Suporte ao conector**

O relatório de transcrição do aluno pode ser acessado pela interface do usuário do administrador, [FTP, Box, API de trabalho ou Power BI](/help/migrated/integration-admin/feature-summary/connectors.md). Não está incluído nos relatórios unificados do Salesforce, Power BI e Marketo Engage.

Os relatórios unificados baixados do Salesforce, Marketo Engage e Power BI contêm menos colunas do que as transcrições do aluno.






