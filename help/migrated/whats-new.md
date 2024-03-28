---
description: Saiba mais sobre os novos recursos e aprimoramentos na versão de março de 2024 do Adobe Learning Manager
jcr-language: en_us
title: Resumo dos novos recursos
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: 8dcfdc7336e5be7f327626d2973671ca56ec58ce
workflow-type: tm+mt
source-wordcount: '3764'
ht-degree: 1%

---

# Resumo dos novos recursos {#new-features-summary}

Saiba mais sobre os novos recursos e aprimoramentos na versão de março de 2024 do Adobe Learning Manager.

## Novidades desta versão {#whatsnewandchanged}

### Importar habilidades de fontes externas

Importe habilidades de provedores de conteúdo, como LinkedIn e Go1, usando os respectivos conectores. Esse aprimoramento é uma parte da meta para a capacidade do Learning Manager de se integrar a nuvens de habilidades e sistemas de gerenciamento de talentos externos. As habilidades importadas serão adicionadas às habilidades definidas pelo administrador no Learning Manager e estarão disponíveis para os autores durante o fluxo de trabalho de criação do curso. Também foram feitos aprimoramentos na funcionalidade de pesquisa de habilidades em toda a plataforma para fornecer uma melhor experiência de pesquisa quando a conta tem um grande número de habilidades.

Exibir [Importar habilidades](administrators/feature-summary/import-skills-external-sources.md) para saber mais.

### Marca personalizada

Agora você pode personalizar determinados elementos da interface do usuário: o nome da organização, o logotipo e o tema da interface do usuário com base nos grupos de usuários disponíveis na conta. Por exemplo, uma organização com várias divisões pode configurar um logotipo personalizado e um tema de interface do usuário a ser exibido para cada divisão.

>[!NOTE]
>
>Esse recurso de várias marcas não se aplica à exibição do administrador. Eles sempre verão a marca no nível da organização em suas contas. Isso ocorre porque este é um recurso voltado para o aluno e pode não ser desejado pelo administrador em sua conta.

Exibir [Várias marcas personalizadas](administrators/feature-summary/themes.md#multiple-branding) para obter mais informações.


## Alterações para contas com grande base de usuários

### Páginas Administrador - Curso ou Caminho de aprendizado

Se um grande número de alunos estiver inscrito no curso, por exemplo, mais de 50.000, a lista de alunos não será exibida. Você pode pesquisar um aluno na *Pesquisar alunos* barra de pesquisa ou selecione a **Baixar** na parte superior da barra de pesquisa para baixar a lista de alunos.

### Administrador - Página Alunos

Ao procurar qualquer usuário, o **Baixar aluno** e **Exportar** opções baixar o mesmo relatório. Enquanto isso, ao procurar um grupo de usuários, agora você pode baixar usuários filtrados desse grupo de usuários. Ao pesquisar um Grupo de usuários, a caixa de diálogo **Baixar lista de alunos** alterações em **Baixar lista de alunos para grupo de usuários** O **Exportar** opção faz download da lista inteira novamente.

### Página Admin- Usuários

#### Usuários internos

Se o número de usuários exceder, por exemplo, 50.000, haverá uma mensagem para baixar os dados para uma análise mais detalhada posteriormente. A barra de pesquisa agora está proeminente e exibe um usuário no formato *Nome, email | UUID*.

>[!NOTE]
>
>A UUID é exibida somente se a UUID estiver ativada para a conta.

#### Usuários externos

Para usuários externos, o mesmo comportamento se aplica. Se o número de usuários for grande, você poderá baixar os usuários e também recuperar os detalhes de um usuário após uma pesquisa no formato *Nome, email | UUID*.

#### Página Limpeza do Usuário

Na página Limpeza do Usuário, para usuários excluídos, removemos o recurso de classificação em **Data de exclusão**. Você só pode classificar pelos UUIDs.

### Páginas Admin- Instância

#### Curso ou caminho de aprendizado

Se o número de inscrições for grande, o Adobe Learning Manager não exibirá o número de alunos. Em vez disso, haverá um ícone, que você pode selecionar, exibir o número de alunos e navegar até a página Alunos.

O número de alunos será exibido como um valor aproximado. Por exemplo, se o número de alunos for mais de 50.000, o valor será exibido como 50K+.

### Admin- páginas L1/L3

Na página Feedback L1, se o número de inscrições no curso for grande, a lista de alunos não será exibida. Em vez disso, você pode exportar a lista de usuários para uma análise mais detalhada posteriormente.

A pesquisa suporta o tipo antecipado e os resultados são restritos à instância selecionada.

#### Página de Participação e Pontuação

Na página, quando você pesquisa um usuário, a pesquisa é executada em todas as instâncias disponíveis. No entanto, o resultado é para a instância selecionada.

Na página Presença, se você pesquisar um Grupo de Usuários e o número de usuários exceder 10.000 no Grupo de Usuários independentemente da inscrição, você só poderá executar ações em massa. Não será possível exibir a lista de usuários.

Se o número de usuários no grupo de usuários for inferior a 10.000, você poderá executar ações individuais no nível do usuário juntamente com ações em massa. Nesse caso, a listagem de usuários não é desativada.

### Página Admin- Certificações

Nas versões atuais do Adobe Learning Manager, se houver um grande número de usuários inscritos em uma certificação, você não poderá exibir os alunos não inscritos desde o **Status** O menu suspenso está desativado.

Nesta versão do Adobe Learning Manager, se o número de usuários inscritos for grande, o **Status** a lista suspensa exibe apenas duas opções- **Inscrito** e **Não inscrito**. A opção **Inscrito** está selecionado por padrão. Se você selecionar **Não inscrito**, a lista de alunos não inscritos é exibida.

#### Alterações no grupo de usuários

No caso de um Grupo de usuários, se o número de usuários no Grupo de usuários for inferior a, por exemplo, 50.000, o **Status** A lista suspensa exibe todas as opções: Certificado, Atribuído e Expirando.

Se o número de usuários em um Grupo de usuários for grande, o **Status** a lista suspensa exibe apenas duas opções- **Inscrito** e **Não inscrito**, de acordo com o novo design.

### Tabela de comparação

<table>
    <tbody>
        <tr>
            <td><b>Página</b></td>
            <td><b>Antes da alteração do limite</b></td>
            <td><b>Após a alteração do limite</b></td>
        </tr>
        <tr>
            <td>Admin- Instância do curso</td>
            <td>As instâncias são exibidas conforme projetado com o seguinte:
            <ul>
                <li>Módulos</li>
                <li>Alunos inscritos</li>
                <li>Sessões</li>
                <li>Medalha</li>
                <li>Feedback L1 habilitado</li>
                <li>Alertas de notificação</li>
                <li>Pontos de gamificação</li>
                <li>Código QR</li>
                <li>Extensão do Caminho de Aprendizado</li>
            </ul>
            <td>
                <ul>
                    <li>Se o número de inscrições exceder o limite predefinido, o ALM não exibirá a contagem; ele substituirá a contagem por um ícone, que, quando clicado, exibe o número real de alunos e um link para levá-lo à página Alunos.</li>
                    <li>O número de inscrições será exibido em um formato aproximado. Por exemplo, se o número for maior que 50.000, a contagem será exibida como mais de 50K no nível do curso.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Administrador - Página Alunos</td>
            <td>
                    <ul>
                        <li>A lista de alunos é exibida para cada instância.</li>
                        <li>Você pode pesquisar um usuário ou grupo de usuários inscrito em um curso.</li>
                        <li>O relatório exportado não consiste em nenhum filtro para Grupo de Usuários.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>A seleção de instância está desativada.</li>
                    <li>Baixar a lista de alunos também baixa os mesmos dados, exceto para um caso. Se você pesquisar um grupo de usuários e selecionar Baixar lista de alunos, ele baixará os dados desse grupo de usuários.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página de feedback N1/N3 do administrador</td>
            <td>
                <p>Nenhuma alteração no comportamento existente</p>
            </td>
            <td>
                <ul>
                    <li>A seleção de instância está desativada.</li>
                    <li>Se a inscrição em um curso estiver acima de 50 mil, o ALM não listará os alunos e exibirá apenas a barra de pesquisa. Se a inscrição for inferior a 50 mil, o ALM exibirá a lista de alunos e a barra de pesquisa.</li>
                    <li>A listagem está desativada por padrão.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página Admin- Presença e Pontuação</td>
            <td>
                <p>Nenhuma alteração no comportamento existente</p>
            </td>
            <td>
                <ul>
                    <li>A seleção de instância é desativada ao pesquisar um usuário.</li>
                    <li>Se o número de usuários exceder, por exemplo, 50.000, haverá uma mensagem adicional para baixar os dados para uma análise mais detalhada posteriormente. A barra de pesquisa agora está proeminente e exibe um usuário no formato Nome, email | UUID</li>
                    <li>Se o número de usuários no Grupo de usuários for inferior a 10.000, independentemente da inscrição, você poderá executar ações individuais no nível do usuário juntamente com ações em massa. Nesse caso, a listagem de usuários não é desativada.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin- Página de pontuação do quiz L2</td>
            <td>
                    <ul>
                        <li>A pesquisa de usuários também é implementada.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>A pesquisa de usuários também é implementada. Enquanto o typeahead pesquisa no nível do objeto de aprendizado, a listagem é filtrada para a instância selecionada no momento.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página Admin- Usuários (Interno, Externo)</td>
            <td>
                    <ul>
                        <li>A ID de e-mail é exibida ao pesquisar um usuário.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Se o número de usuários exceder, por exemplo, 50.000, haverá uma mensagem adicional para baixar os dados para uma análise mais detalhada posteriormente. A barra de pesquisa agora está proeminente e exibe um usuário no formato Nome, email | UUID</li>
                    <li>Na página Limpeza do Usuário, para usuários excluídos, removemos o recurso de classificação em **Data de exclusão**. Você só pode classificar pelos UUIDs.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Professores - Envio</td>
            <td>
                    <ul>
                        <li>Paginação dos módulos a serem enviados.</li>
                        <li>Como professor, agora você pode filtrar envios de arquivos dos alunos com base em status, término de Revisão, Envio pendente, Aprovado e Falha. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Você só pode pesquisar usuários, não grupos de usuários nessa instância.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Contar na visualização como página do aluno</td>
            <td>
                    <ul>
                        <li>A contagem inclui os dados de inscrição de ordem superior.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>A contagem exclui dados de inscrições de ordem superior.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Recursos avançados de pesquisa

Nesta versão, aprimoramos a experiência de pesquisa. Os resultados da pesquisa são buscados com base não apenas nos metadados, mas também na pesquisa semântica e no conteúdo para obter resultados com base na precisão, recenticidade e conteúdo relevante.

Essa alteração reflete no seguinte:

* Catálogo e página Meu aprendizado: a ação passar o mouse sobre o curso, o caminho de aprendizado e a certificação foi removida.
* A aparência da barra de pesquisa.
* Tags de filtro adicionadas ao aplicativo de aprendizado.

Para ativar os recursos de pesquisa, entre em contato com a equipe CSAM do Adobe Learning Manager.

## Mudanças na interface do usuário {#ui-changes}

### Página de criação do curso

Ao mapear os cursos para um nível de habilidade, a lista de habilidades é pesquisada primeiro. Em outras palavras, pesquise habilidades e veja uma lista de habilidades que correspondem ao termo pesquisado.

### Grupos de usuários

#### Administrador - Página Alunos

Ao procurar qualquer usuário, o **Baixar aluno** e **Exportar** opções baixar o mesmo relatório. Enquanto isso, ao procurar um grupo de usuários, agora você pode baixar usuários filtrados desse grupo de usuários. Ao pesquisar um Grupo de usuários, a caixa de diálogo **Baixar lista de alunos** alterações em **Baixar lista de alunos para grupo de usuários** O **Exportar** opção faz download da lista inteira novamente.

## Alterações nos relatórios

* As colunas Etiqueta(s) e Habilidade(s) no Relatório de treinamentos foram alteradas para Etiqueta e habilidades.
* Adicionado o relatório [Trilha de auditoria de gamificação](administrators/feature-summary/reports.md#gamification-audit-trail).
* Se uma conta tiver mais de 280.000 alunos atribuídos a uma habilidade, o relatório do aluno de habilidade será baixado como um csv compactado.
Se a conta tiver menos de 250.000 alunos, o mesmo relatório será baixado como um CSV.
Na página Administrador, selecione **Admin** > **Habilidades** > **Habilidade** > **Alunos**. O relatório é baixado como CSV.
* O [Relatório de resumo da sessão](administrators/feature-summary/reports.md#session-summary-report) A tem duas novas colunas- Informações do Local e região do Local.

## Alterações na criação da sala de aula

Com base em [Configurações do administrador](administrators/feature-summary/classroom.md#classroom-settings), você, como Autor, pode [criar, modificar e excluir locais](administrators/feature-summary/classroom.md#add-classroom-location).
>[!NOTE]
>
>Ao adicionar rótulos de local e catálogo, os autores (na página de criação do curso) e os administradores (na página de instância) verão uma lista preenchida automaticamente de locais e rótulos de catálogo, respectivamente.

Como administrador, você pode aplicar restrições a um autor para modificar ou excluir um local da sala de aula. Exibir [Configurações de sala de aula](administrators/feature-summary/classroom.md#classroom-settings) para obter mais informações.

## Alterações no Caminho de aprendizado flexível

Todas as contas (antigas e novas) em começarão incluindo Prazo de inscrição, Prazo de cancelamento de inscrição e Limite de vagas no aplicativo do aluno para um Caminho de aprendizado flexível.
Os alunos agora poderão se inscrever no Caminho de aprendizado flexível sem selecionar nenhuma instância do curso.

## Novo acionador para planos de aprendizado

Um novo acionador foi adicionado à página de configuração do Plano de aprendizado. Os autores e os administradores agora poderão acionar ações quando um aluno reprovar em um módulo de um curso.

Exibir [Planos de aprendizado](administrators/feature-summary/learning-plans.md) para obter mais informações.

## Novo status de envio

Como professor, agora você pode filtrar envios de arquivos dos alunos com base em status, término de Revisão, Envio pendente, Aprovado e Falha.

Exibir [Status do envio](instructors/feature-summary/learners.md#filter-file-submissions) para obter mais informações.

## Aprimoramentos na lista de verificação

Na versão de março de 2024 do Adobe Learning Manager, os aprimoramentos feitos ao fluxo de trabalho da lista de verificação são os seguintes:

### Não permitir progresso em caso de falha em uma lista de verificação

Ao criar uma lista de verificação, um autor pode selecionar **Habilitar** na seção Lista de verificação obrigatória. Isso impede que um aluno continue no módulo se falhar na lista de verificação. Eles só podem continuar se forem aprovados na lista de verificação.

Os revisores da lista de verificação, ou seja, professores ou gerentes, podem verificar o status da lista de verificação. Os revisores também podem revisar a lista de verificação de um aluno fora de ordem.

### Reavaliação de uma lista de verificação

Ao criar uma lista de verificação, um autor pode selecionar **Habilitar** na seção Reavaliação. Isso permite que um gerente ou professor reavalie um aluno até que ele seja aprovado na lista de verificação.

Se o módulo for obrigatório, a caixa de seleção de reavaliação será marcada por padrão.

Um professor ou gerente também pode alterar o status de uma lista de verificação de Reprovado para Aprovado quando a reavaliação estiver ativada.

Na página Lista de verificação, um professor pode ver o número de alunos no estado Pendente. Como professor, você pode avaliar um aluno e aprová-lo ou reprová-lo. Se um aluno estiver em um estado de falha, você só poderá ver a lista de verificação quando a reavaliação não estiver ativada.

Isto significa que a **Habilitar** a caixa de seleção não foi marcada na seção Reavaliação ao criar a lista de verificação. Se esta caixa de seleção estiver selecionada, você poderá ver o botão Exibir/Reavaliar na página Lista de verificação do professor.

Selecionar o botão permite reavaliar um aluno e marcá-lo como aprovado ou reprovado.

>[!NOTE]
>
>Esses dois recursos - Reavaliação e Tornando a lista de verificação obrigatória - se aplicam apenas aos módulos recém-criados. Depois que um curso é publicado, eles não podem ser ativados/desativados.


Exibir [Criar uma lista de verificação](authors/feature-summary/courses.md#checklist-fail) para obter mais informações.

## Outras melhorias

### Notificações de email relacionadas à sessão

Nas versões anteriores do Adobe Learning Manager, um aluno não tinha e-mails relacionados à sessão, detalhes da sessão atualizados, convite da sessão e lembrete da sessão quando:

* Os alunos concluíram um curso,
* Novas sessões são adicionadas a um curso ou
* Há alterações nas sessões existentes.

Na versão de março de 2024 do Adobe Learning Manager, estas são as novas alterações:

* Detalhes da sessão atualizados e convite da sessão (para aluno e professor)
   * Para sessões futuras, e-mails para **Detalhes da sessão atualizados**, **Convite de sessão** para alunos inscritos e professores atuais serão descontinuados. Para sessões anteriores, e-mails para **Detalhes da sessão atualizados** e **Convite de sessão** para alunos inscritos e professores atuais permanecerão como estão.
* E-mails de lembrete (para administrador e aluno)
   * Para sessões futuras, somente **Lembrete de sessão** emails serão enviados.

>[!NOTE]
>
>Os e-mails não dependem da sessão e da conclusão do curso.


### Alterações no local de referência AEM

Em um site de referência AEM, adicionamos suporte para adicionar o token de atualização do administrador ao token de acesso do aluno.

### Ocultar envios dos professores

Depois que os alunos fazem upload de seus arquivos usando o fluxo de trabalho de envio de arquivos, se um professor não realizar nenhuma ação (aprovar ou rejeitar) no envio, o URL de envio ficará oculto da exibição após um número de dias predefinido. Entre em contato com as equipes CSAM do Adobe Learning Manager para definir ou alterar o número de dias.

### Alterações na terminologia do produto

Adicionamos as colunas *Instância* e *Aluno* ao vocabulário de terminologia do produto.

### Alterações no aplicativo móvel

Nesta versão do aplicativo móvel, os alunos podem agendar e gerenciar lembretes de cursos vencidos. Clicar em uma notificação de lembrete atrasada permite que você acesse as seguintes opções:

* Cancelar
* Ir ao curso
* Lembrar-me novamente em 3 dias
* Lembrar-me novamente em uma semana

No Android: clicar na notificação por push o direcionará para a **Visão geral do curso** página.
No iOS: clicar na notificação por push o direcionará para a página inicial do aplicativo. Essa é uma limitação conhecida no iOS.

### Alterações na lista de verificação no aplicativo do aluno no Salesforce

Se um aluno não passar em uma lista de verificação, ele não poderá prosseguir para o próximo módulo ou curso. Quando a caixa de seleção Lista de verificação obrigatória está marcada, o aluno não pode prosseguir em um curso se não passar na lista de verificação.

Assim como no aplicativo Web, se um aluno falhar em uma lista de verificação no aplicativo Salesforce, ele verá uma mensagem e não avançará.

### Alterações no Connect VC

Nas versões atuais do Adobe Learning Manager, um aluno é marcado como **Não participou** quando eles estão inscritos para uma sessão de aula virtual do Connect, mas não atendiam aos critérios de conclusão.

Nesta versão, o status muda para **Ainda não marcado**.

### Rotulagem de branco no Adobe Learning Manager

O aplicativo móvel Adobe Learning Manager agora é compatível com rótulos brancos, o que significa que agora você pode liberar o aplicativo com sua própria marca.

Exibir rotulagem de branco em [Aplicativo móvel do Adobe Learning Manager](white-label.md) para obter mais informações.

### Nova coluna em CSVs de migração

Nesta versão, há uma nova coluna opcional, uniqueLoId, nos seguintes CSVs de migração.

* certification.csv
* course.csv
* learning_program.csv

A coluna, uniqueLoId, não é aplicável ao CSV de ajuda de tarefa.

>[!IMPORTANT]
>
>Os valores da coluna devem ser exclusivos na conta. Não é possível usar o mesmo valor com um curso ou certificação.

Baixe os CSVs no menu [Manual de migração](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs).


### Classificação do aplicativo

Um aluno pode fornecer seu feedback no aplicativo Adobe Learning Manager para aprimorar ainda mais a experiência no aplicativo. Se o aluno classificar quatro estrelas ou mais, será exibida uma janela pop-up que solicita que o aluno classifique o aplicativo na Play Store ou no App Store.

### A Bluejeans chegou ao fim da sua vida útil em fevereiro de 2024

Gostaríamos de informar que a Bluejeans atingiu seu fim de vida útil em fevereiro de 2024. Após fevereiro de 2024, o Bluejeans não receberá mais atualizações ou suporte. Nossas equipes de suporte e CSAM ajudarão você com quaisquer dúvidas ou preocupações que possa ter durante esse período de transição.

Exibir [Conectores no Adobe Learning Manager](integration-admin/feature-summary/connectors.md) para obter mais informações sobre como configurar conectores.

### Alterações no relatório Acesso de logon

O relatório Login Access estará disponível apenas para os últimos cinco trimestres. Se algum administrador de integração solicitar o download Por demanda da Exportação unificada com **Acesso de login** marcada, o Adobe Learning Manager exibirá uma mensagem de erro. No entanto, não há impacto em outros relatórios.

### Alterações do ADFS

Os campos Tipo de funcionário e ID do funcionário do AD FS agora estão disponíveis no Adobe Learning Manager, com base nos mapeamentos.

## Alterações da API nesta versão

### APIs do aluno

Nesta versão, adicionamos suporte de API para que os alunos visualizem o logotipo da marca e os temas personalizados no nível de Grupo de usuários.

As APIs /account e /user?include=account retornam quatro campos, que são substituídos específicos do campo ativo do usuário que pertence a logoUrl, logoStyling e themeData.

### Novos atributos

Um novo atributo, isExpiredSubmission, em learningObjectResource, que mostra se o envio no recurso expirou ou não.

* API GET /account: retorna novo atributo **expireSubmissionDuration** X, onde X é o número de dias definido. Se não definido, 0 será retornado
* API GET /LO com recurso inclui novo atributo **isExpiredSubmission**&quot; Verdadeiro ou Falso.
   * Verdadeiro, se o envio estiver expirado e “submissionUrl” não for exibido.
   * Se for False, o envio não expirará e “submissionUrl” será buscado.

### Alterações de API na lista de verificação

Um curso pode consistir em vários módulos dos quais a Lista de verificação é um tipo de módulo. Este módulo de lista de verificação é avaliado pelo professor e pode ser marcado como Reprovado ou Bem-sucedido com base na avaliação.

Mas, em ambos os casos, o status da lista de verificação é marcado como Concluído e, dessa forma, o curso é marcado como Concluído.

Nesta versão, a API do LO inclui o parâmetro *isChecklistMandatory*. Se o valor for True, a lista de verificação será obrigatória.

### Suporte a vários locais

Um administrador agora pode baixar o relatório de feedback L1 no idioma escolhido. No entanto, você ainda não pode baixar relatórios de feedback L1 para o Power BI. Na solicitação da API, use o parâmetro preferredLocale para especificar o local de sua escolha.

### Alterações no resumo de contagem de Instâncias

Isso é aplicável a contas onde as inscrições para um curso de Sala de aula/Sala de aula virtual são mais de 1.000.

Se o número for inferior a 1000, as inscrições invalidam o cache e retornam os valores atualizados em uma chamada de API de Resumo do GET, como número de inscrição, conclusão e limite de estação.

Se a conta estiver habilitada para esse recurso e o número de inscrições for maior que 1000, os valores serão recuperados do cache.

### Caminhos obsoletos

No momento, as APIs do Learning Manager seguem uma estrutura de dados de gráfico, que permite buscar dados atravessando o modelo de API por meio de inclusões. Mesmo que você pudesse atravessar uma API de até sete níveis, buscar os dados usando uma única chamada de API é computacionalmente caro.

Recomendamos que todos os clientes novos e existentes façam chamadas pequenas várias vezes em vez de uma chamada grande. Essa abordagem evitará que dados indesejados sejam carregados na chamada.

#### Quais caminhos estão obsoletos

Os caminhos a seguir estão obsoletos:

* /learningObjects
   * Caminhos obsoletos:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Caminhos existentes:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Caminho preterido:
      * enrollment.instances.subLoInstances.learningObject
   * Caminho existente:
      * enrollment.instances.subLoInstances
* /enrollments
   * Caminho preterido:
      * loInstance.learningObject.enrollment
   * Novo caminho:
      * loInstance.learningObject
* /learningObjects/{id}
   * Caminho preterido:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Novo caminho:
      * instance.subLoInstances

### Acesso de logon e alterações de arquivamento do relatório de auditoria do usuário para a API de trabalho

Com esta versão, a API de trabalho manterá o Relatório de acesso de logon por até cinco trimestres e o Relatório de auditoria do usuário por seis meses. Se quiser fazer download dos dados anteriores a esse período, você deve passar o parâmetro de arquivamento, especificando trimestre e ano. Consulte a carga de amostra.

```
{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateLoginAccessReport",
            "payload": {
                "fromDate": "2023-04-01T18:30:00.000Z",
                "toDate": "2023-04-30T18:30:00.000Z",
                "archive": {
                    "quarter": "4",
                    "year": "2021"
                }
            }
        }
    }
}
```

Se você tentar baixar o **Acesso de login** que ultrapasse cinco trimestres, será exibida uma mensagem de erro. Uma mensagem de erro semelhante é exibida se você tentar baixar o **Auditoria de usuário** que exceda seis meses.

### APIs obsoletas

Exibir [Descontinuações de API no Adobe Learning Manager](api-deprecations-list.md) para obter uma lista cumulativa de todas as APIs obsoletas no produto.

## Erros corrigidos nesta atualização {#bug-fixes}

* Quando um aluno está inscrito em um curso e tenta se inscrever em outro curso, é exibida uma mensagem de aviso.
* Um Grupo de usuários, mesmo depois de excluído, fica visível na pesquisa.
* Quando os usuários disparam muitas transcrições do aluno com uma grande quantidade de dados, a fila Transcrições do aluno é bloqueada e impede uma nova solicitação.
* Se uma conta filha solicitar que sua conta pai compartilhe um relatório, a conta pai não poderá fazer isso.
* Os URLs de um curso e de um caminho de aprendizado redirecionam para locais incorretos.
* Um aluno visualiza intermitentemente a instância do curso de um curso diferente clicando no link do curso na página do catálogo.
* O **Cancelar inscrição** não é exibido como esperado após a primeira inscrição, mas o botão é exibido após uma atualização.
* Não é possível salvar o Conteúdo ou um Quiz que tenha um espaço em branco no nome.
* Nos cursos aprovados pelo gerente, você pode reinscrever os alunos em um grupo de usuários.
* Em alguns casos, se você tentar adicionar outro campo ativo, a mensagem de erro “Não foi possível salvar os campos ativos” será exibida.
* O texto excede o nome de um curso dentro de um cartão do curso na seção Cursos relacionados.
* Depois de alternar uma instância e inscrever um aluno na instância, as instâncias antigas ainda existem no calendário do Outlook.
* Quando um aluno de uma conta entre parceiros tenta selecionar a miniatura de um curso, é exibida uma mensagem de erro.
* Quando os alunos se inscrevem em um curso, eles recebem várias notificações da inscrição.
* Se um usuário alterar manualmente o nome dos catálogos criados em um conector, novos catálogos serão criados e os cursos serão publicados nos catálogos incorretos.
* Os usuários que pertencem a contas inativas ainda recebem emails de assinatura.

### Correções de erros relacionados à API

* Os usuários/GET da API não recuperam os detalhes de um gerente.
* Em uma conta, os usuários são criados por meio de uma importação de usuários de FTP agendada durante um tempo de inatividade agendado.
* No aplicativo móvel ou modo imersivo, após excluir ou desativar uma instância do curso e selecionar a próxima instância ativa, o **Registrar interesse** é exibido em vez de **Inscrever-se**.
* Quando um aluno de uma conta entre parceiros tenta selecionar a miniatura de um curso usando a API do objeto de aprendizado, o erro 403 Proibido é exibido.

## Requisitos do sistema

Exibir [Requisitos de sistema do Adobe Learning Manager](system-requirements.md).

## Versões anteriores do Adobe Learning Manager

* [Versão de novembro de 2023](whats-new-november-2023.md)
* [Versão de julho de 2023](whats-new-2023-july.md)
