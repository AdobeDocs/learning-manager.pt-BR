---
description: Saiba mais sobre os novos recursos e aprimoramentos na versão de março de 2024 do Adobe Learning Manager
jcr-language: en_us
title: Resumo dos novos recursos
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: c833d92533b7fbf5a87c980d8b5e088185d02ef5
workflow-type: tm+mt
source-wordcount: '3903'
ht-degree: 1%

---

# Resumo dos novos recursos {#new-features-summary}

Saiba mais sobre os novos recursos e aprimoramentos na versão de março de 2024 do Adobe Learning Manager.

Explore alguns dos recursos mais recentes do Adobe Learning Manager, como:

1. Importar habilidades de origens externas
1. Suporte a várias marcas
1. Módulo de re-avaliação e atividade da lista de verificação
1. Aplicativo de aprendizagem móvel com etiqueta branca

>[!NOTE]
>
>Confira este [webinário](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) para saber mais sobre os novos recursos desta versão.


## Novidades desta versão {#whatsnewandchanged}

### Importar habilidades de origens externas

Importe habilidades de provedores de conteúdo, como o LinkedIn e o Go1, usando os respectivos conectores. Esse aprimoramento é uma parte do objetivo para a capacidade do Gerenciador de aprendizado de integração com os sistemas externos de gerenciamento de habilidades e de gerenciamento de talentos. As habilidades importadas serão adicionadas às habilidades definidas pelo administrador no Gerenciador de aprendizagem e estarão disponíveis para os autores durante o fluxo de trabalho de criação do curso. Também foram feitos aprimoramentos na funcionalidade de pesquisa de habilidades em toda a plataforma para oferecer uma melhor experiência de pesquisa quando a conta tiver um grande número de habilidades.

Exibir [habilidades](administrators/feature-summary/import-skills-external-sources.md) de importação para saber mais.

### Marca personalizada

Agora você poderá personalizar determinados elementos da interface do usuário, o nome da organização, o logotipo e o tema da interface do usuário, com base nos grupos de usuários disponíveis na conta. Por exemplo, uma organização com várias divisões pode configurar um logotipo personalizado e um tema de interface do usuário para serem exibidos para cada divisão.

>[!NOTE]
>
>Esse recurso de marcação múltipla não se aplica à exibição do administrador. Eles sempre verão marcas no nível da organização em suas contas. Isso ocorre porque este é um recurso voltado para o aluno, e o administrador pode não querer isso em sua conta.

Consulte [Várias marcas](administrators/feature-summary/themes.md#multiple-branding) personalizadas para obter mais informações.


## Alterações em contas com grande base de usuários

### Páginas Demarcador de aprendizado ou curso de administração

Se um grande número de alunos estiver inscrito no curso, por exemplo, mais de 50.000, a lista de alunos não será exibida. Você pode pesquisar por um aluno na barra de pesquisa dos *Alunos* de pesquisa ou selecionar o **link Download** na parte superior da barra de pesquisa para baixar a lista de alunos.

### Página De administrador- Alunos

Ao pesquisar por qualquer usuário, as **opções Baixar aluno** e **Exportar** baixam o mesmo relatório. Enquanto isso, ao pesquisar por um grupo de usuários, você pode baixar usuários filtrados desse grupo de usuários. Ao pesquisar um grupo de usuários,
a **lista** de alunos de download muda para **Baixar lista de alunos do grupo** de usuários A **opção Exportar** novamente baixa toda a lista.

### Página do administrador - Usuários

#### Usuários internos

Se o número de usuários exceder, por exemplo, 50.000, haverá uma mensagem para baixar os dados para uma análise mais detalhada mais tarde. A barra de pesquisa agora destaca-se e exibe um usuário nos *formatos Nome e Email | UUID*.

>[!NOTE]
>
>A UUID é exibida somente se a UUID estiver habilitada para a conta.

#### Usuários externos

Para usuários externos, o mesmo comportamento se aplica. Se o número de usuários for grande, você poderá baixar os usuários e também recuperar os detalhes de um usuário após uma pesquisa no nome do formato *, email | UUID*.

#### Página Limpeza de usuários

Na página Limpeza de usuários, para usuários excluídos, removemos o recurso de classificação na **data excluído**. Você só pode classificar em UUIDs.

### Administrador - Páginas da instância

#### Caminho do curso ou do aprendizado

Se o número de inscrições for grande, o Gerente de aprendizado da Adobe não exibirá o número de alunos. Em vez disso, haverá um ícone, que você pode selecionar, e exibir o número de alunos e navegar até a página Alunos.

O número de alunos será exibido como um valor aproximado. Por exemplo, se o número de alunos for maior que 50.000, o valor será exibido como 50k+.

### Páginas do administrador N1/N3

Na página Feedback N1, se o número de inscrições no curso for grande, a lista de alunos não será exibida. Em vez disso, você pode exportar a lista de usuários para uma análise mais detalhada posteriormente.

A pesquisa oferece suporte para textos com antecedência e os resultados ficam restritos à instância selecionada.

#### Página de participação e pontuação

Na página, quando você pesquisa um usuário, a pesquisa é executada em todas as instâncias disponíveis. No entanto, o resultado será para a instância selecionada.

Na página de Presença, se você procurar um grupo de usuários e o número de usuários exceder 10.000 no grupo de usuários independentemente da inscrição, só será possível realizar ações em nível de massa. Você não poderá visualizar a lista de usuários.

Se o número de usuários no grupo de usuários for menor que 10.000, você pode executar ações individuais em nível de usuário juntamente com ações em nível de massa. Nesse caso, a listagem de usuários não é desativada.

### Página Administrador - Certificações

Nas versões atuais do Adobe Learning Manager, se houver um grande número de usuários inscritos em uma certificação, você não poderá ver os alunos não inscritos, pois o **menu suspenso de Status** está desativado.

Nesta versão do Adobe Learning Manager, se o número de usuários inscritos for grande, o **menu suspenso de Status** exibirá apenas duas opções: **Inscrito** e **Não inscrito**. A opção **Inscrito** é selecionada por padrão. Se você selecionar **Cancelar inscrição**, será exibida a lista de alunos sem inscrição.

#### Alterações no grupo de usuários

No caso de um grupo de usuários, se o número de usuários no grupo de usuários for menor que, por exemplo, 50.000, o **menu suspenso Status** exibirá todas as opções: Certificado, Atribuído e Expiração.

Se o número de usuários em um grupo de usuários for grande, o **menu suspenso status** exibirá apenas duas opções: **Inscrito** e **Cancelar inscrição**, de acordo com o novo design.

### Tabela de comparação

<table>
    <tbody>
        <tr>
            <td><b>Página</b></td>
            <td><b>Antes da alteração do limite</b></td>
            <td><b>Após a alteração do limite</b></td>
        </tr>
        <tr>
            <td>Administrador - Instância do curso</td>
            <td>As instâncias são exibidas conforme projetadas com o seguinte:
            <ul>
                <li>Módulos</li>
                <li>Alunos inscritos</li>
                <li>Sessões</li>
                <li>Medalha</li>
                <li>Feedback L1 habilitado</li>
                <li>Alertas de notificação</li>
                <li>Pontos de gamificação</li>
                <li>Código QR</li>
                <li>Extensão do caminho de aprendizagem</li>
            </ul>
            <td>
                <ul>
                    <li>Se o número de inscrições exceder o limite predefinido, o ALM não exibirá o número; substituirá a contagem por um ícone que, ao ser clicado, exibe o número real de alunos e um link para levá-lo à página Alunos.</li>
                    <li>O número de inscrições será exibido em um formato aproximado. Por exemplo, se o número for maior que 50.000, o total será exibido como 50K+ no nível do curso.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página De administrador- Alunos</td>
            <td>
                    <ul>
                        <li>A lista de alunos é exibida para cada instância.</li>
                        <li>Você pode pesquisar um usuário ou um grupo de usuários inscrito em um curso.</li>
                        <li>O relatório exportado não consiste em nenhum filtro para o Grupo de usuários.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>A seleção da instância está desativada.</li>
                    <li>A lista de alunos de download também baixa os mesmos dados, exceto para um caso. Se você procurar um grupo de usuários e, em seguida, selecionar a lista Baixar aluno, eles baixarão os dados desse grupo de usuários.</li>
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
                    <li>A seleção da instância está desativada.</li>
                    <li>Se a inscrição em um curso for superior a 50 mil, o ALM não lista os alunos e exibe apenas a barra de pesquisa. Se a inscrição for inferior a 50 mil, o ALM exibe a lista de alunos e a barra de pesquisa.</li>
                    <li>A listagem fica desativada por padrão.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página de participação e pontuação do administrador</td>
            <td>
                <p>Nenhuma alteração no comportamento existente</p>
            </td>
            <td>
                <ul>
                    <li>A seleção de ocorrência é desativada ao pesquisar um usuário.</li>
                    <li>Se o número de usuários exceder, por exemplo, 50.000, haverá uma mensagem adicional para baixar os dados para uma análise mais detalhada mais tarde. A barra de pesquisa agora destaca-se e exibe um usuário nos formatos Nome e Email | UUID.</li>
                    <li>Se o número de usuários no grupo de usuários for menor que 10.000, independentemente da inscrição, você pode realizar ações individuais em nível de usuário junto com ações em nível de massa. Nesse caso, a listagem de usuários não é desativada.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página de pontuação do administrador- N2 quiz</td>
            <td>
                    <ul>
                        <li>A pesquisa de usuários também é implementada.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>A pesquisa de usuários também é implementada. Enquanto o typeahead pesquisa no nível de LO, a lista é filtrada para a instância atualmente selecionada.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Página Usuários (interno, externo)</td>
            <td>
                    <ul>
                        <li>A ID de e-mail é exibida ao pesquisar um usuário.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Se o número de usuários exceder, por exemplo, 50.000, haverá uma mensagem adicional para baixar os dados para uma análise mais detalhada mais tarde. A barra de pesquisa agora destaca-se e exibe um usuário nos formatos Nome e Email | UUID.</li>
                    <li>Na página Limpeza de usuários, para usuários excluídos, removemos o recurso de classificação em **Date deleted**. Você só pode classificar em UUIDs.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Professores - Envio</td>
            <td>
                    <ul>
                        <li>Paginação dos módulos a serem enviados.</li>
                        <li>Como professor, agora você pode filtrar os envios de arquivos dos alunos com base no status, finalizando revisão, Envio pendente, Aprovado e Reprovado. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Você só pode pesquisar usuários, não grupos de usuários nesse caso.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Contagem na visualização como página do aluno</td>
            <td>
                    <ul>
                        <li>A contagem inclui os dados de inscrição em pedidos mais altos.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>A contagem exclui dados de inscrições em ordem mais alta.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Recursos de pesquisa avançados

Nesta versão, aprimoramos a experiência de pesquisa. Os resultados da pesquisa são obtidos com base não apenas nos metadados, mas também na busca semântica e no conteúdo para gerar resultados baseados na precisão, na relevância e no conteúdo relevante.

Essa alteração reflete o seguinte:

* Página Catálogo e Meu aprendizado: a ação Focal no curso, no caminho do aprendizado e na certificação foi removida.
* A aparência da barra de pesquisa.
* Adição de tags de filtro no aplicativo de aprendizado.

Para ativar os recursos de pesquisa, entre em contato com a equipe CSAM do Adobe Learning Manager.

## Mudanças na interface do usuário {#ui-changes}

### Página de criação do curso

Ao mapear os cursos para um nível de habilidade, a lista de habilidades é pesquisada primeiro. Em outras palavras, as habilidades de pesquisa e você verá uma lista de habilidades que correspondem ao termo pesquisado.

### Grupos de usuários

#### Administrador: página Alunos

Ao pesquisar por qualquer usuário, as **opções Baixar aluno** e **Exportar** baixam o mesmo relatório. Enquanto isso, ao pesquisar por um grupo de usuários, você pode baixar usuários filtrados desse grupo de usuários. Ao pesquisar um grupo de usuários, a **lista** de alunos de download muda para **Baixar lista de alunos para grupo** de usuários A **opção Exportar** baixa novamente a lista inteira.

## Alterações nos relatórios

* As colunas Tag(s) e Habilidade(s) no Relatório de treinamentos são alteradas para Tag e Habilidades.
* Adicionado o relatório [, Trilha](administrators/feature-summary/reports.md#gamification-audit-trail) de auditoria de gamificação.
* Se uma conta contiver mais de 28.000 alunos atribuídos a uma habilidade, o relatório do aluno-habilidade será baixado como um csv compactado.
Se a conta tiver menos de 2.50000 alunos, o mesmo relatório será baixado como um CSV.
Na página do administrador, selecione Administrador > Habilidades**>** Habilidades **>** Alunos **.****** O relatório é baixado como CSV.
* O [relatório](administrators/feature-summary/reports.md#session-summary-report) de Resumo da sessão tem duas novas colunas: Informações de localização e região de Local.

## Alterações na criação da sala de aula

Com base nas [configurações](administrators/feature-summary/classroom.md#classroom-settings) do administrador, você, como autor, pode [criar, modificar e excluir locais](administrators/feature-summary/classroom.md#add-classroom-location).

>[!NOTE]
>
>Ao adicionar rótulos de local e de catálogo, os autores (na página de criação do curso) e os administradores (na página da instância) verão uma lista preenchida automaticamente de locais e rótulos do catálogo, respectivamente.

Como administrador, você pode impor restrições ao autor para modificar ou excluir um local de sala de aula. Consulte as [configurações](administrators/feature-summary/classroom.md#classroom-settings) da sala de aula para obter mais informações.

## Mudanças no caminho flexível de aprendizagem

Todas as contas (antigas e novas) começarão incluindo o Prazo de inscrição, o Prazo de inscrição e o limite de licença no aplicativo do aluno para um caminho de aprendizado flexível.
Os alunos agora poderão se inscrever no Caminho flexível de aprendizagem sem selecionar nenhuma instância do curso.

## Novo acionador dos planos de aprendizado

Um novo acionador foi adicionado à página de configuração do plano de aprendizado. Os autores e os administradores agora poderão acionar ações quando um aluno falhar em um módulo de um curso.

Consulte [os planos de](administrators/feature-summary/learning-plans.md) aprendizado para obter mais informações.

## Novo status de envio

Como professor, agora você pode filtrar os envios de arquivos dos alunos com base no status, finalizando revisão, Envio pendente, Aprovado e Reprovado.

Exibir [o status](instructors/feature-summary/learners.md#filter-file-submissions) de envio para obter mais informações.

## Aprimoramentos da lista de verificação

Na versão de março de 2024 do Adobe Learning Manager, os aprimoramentos feitos no fluxo de trabalho da lista de verificação são os seguintes:

### Desautoriza o progresso ao falhar em uma lista de verificação

Ao criar uma lista de verificação, um autor pode selecionar **Ativar** na seção Lista de verificação obrigatória. Isso impede que um aluno prossiga no módulo se falhar na lista de verificação. Eles só podem continuar se passarem pela lista de verificação.

Os revisores de listas de verificação, ou seja, professores ou gerentes podem verificar o status da lista de verificação. Os revisores também podem revisar a lista de verificação fora da ordem de um aluno.

### Avaliar novamente uma lista de verificação

Ao criar uma lista de verificação, um autor pode selecionar **Ativar** na seção Re-avaliação. Isso permite que um gerente ou um instrutor avaliem novamente um aluno até que passem pela lista de verificação.

Se o módulo for obrigatório, a caixa de seleção de re-avaliação é selecionada por padrão.

Um instrutor ou gerente também pode alterar o status de uma lista de verificação de Falha para Aprovado quando a nova avaliação estiver ativada.

Na página Lista de verificação, um professor pode ver o número de alunos no estado Pendente. Como instrutor, você pode avaliar um aluno e passá-lo ou reprovar. Se um aluno estiver em um estado com falha, você só poderá ver a lista de verificação quando a nova avaliação não estiver ativada.

Isso significa que a **caixa de seleção Ativar** não foi selecionada na seção Re-avaliação ao criar a lista de verificação. Se essa caixa de seleção estiver selecionada, você poderá ver o botão Exibir/Avaliar novamente na página Lista de verificação do professor.

Selecionar o botão permite que você rea avalie novamente um aluno e marque-o como aprovado ou reprovado.

>[!NOTE]
>
>Ambos os recursos, com nova avaliação e tornando a lista de verificação obrigatória, se aplicam somente aos módulos recém-criados. Uma vez que um curso é publicado, eles não podem ser ativados ou desativados.


Consulte [Criar uma lista de verificação](authors/feature-summary/courses.md#checklist-fail) para obter mais informações.

## Outras melhorias

### Notificações de email relacionadas à sessão

Nas versões anteriores do Adobe Learning Manager, um aluno não fazia emails relacionados à sessão, detalhes da sessão atualizados, Convite da sessão e Lembrete de sessão quando:

* Os alunos concluíram um curso,
* As novas sessões são adicionadas a um curso ou
* Há alterações nas sessões existentes.

Na versão de março de 2024 do Adobe Learning Manager, as seguintes alterações são:

* Detalhes da sessão atualizados e Convite da sessão (para aluno e professor)
   * Para sessões futuras, os e-mails dos **Detalhes da sessão atualizados**, **o Convite** da sessão para alunos inscritos e os professores atuais serão descontinuados. Nas sessões anteriores, os e-mails dos **Detalhes da sessão foram atualizados** e **o convite** da sessão para os alunos inscritos e os professores atuais permanecerão como estão.
* E-mails de lembrete (para administrador e aluno)
   * Para sessões futuras, somente **os emails de Lembrete** de sessão serão enviados.

>[!NOTE]
>
>Os emails não dependem da conclusão da sessão e do curso.


### Alterações de site de referência do AEM

Em um site de referência do AEM, adicionamos suporte para adicionar o Token de atualização de administrador ao token de acesso do aluno.

### Ocultar envios de professores

Depois que os alunos fazem upload de seus arquivos usando o fluxo de trabalho de envio de arquivos, se um professor não fizer nenhuma ação (aprovar ou rejeitar) no envio, o URL de envio fica oculto da exibição após um número predefinido de dias. Entre em contato com as equipes de CSAM do Adobe Learning Manager para definir ou alterar o número de dias.

### Mudanças na terminologia do produto

Adicionamos a Instância *de colunas* e *o Aluno* ao vocabulário da terminologia do produto.

### Alterações no aplicativo para dispositivos móveis

Nesta versão do aplicativo móvel, os alunos podem agendar e gerenciar lembretes de curso atrasado. Clicar em uma notificação de lembrete atrasada permite acessar as seguintes opções:

* Cancelar
* Ir ao curso
* Lembre-me novamente em 3 dias.
* Lembre-me novamente em uma semana.

No Android: clicar na notificação push o direcionará à página Visão geral **do**curso.
No iOS: clicar na notificação push direciona você para a página inicial do aplicativo. Essa é uma limitação conhecida no iOS.

### Alterações na lista de verificação no aplicativo do aluno no Salesforce

Se um aluno falhar em uma lista de verificação, ele não poderá prosseguir para o próximo módulo ou curso. Quando a caixa de seleção Lista de seleção obrigatória é selecionada, o aluno não consegue avançar em um curso se falhar na lista de verificação.

Como com o aplicativo da Web, se um aluno falhar em uma lista de verificação no aplicativo Salesforce, ele verá uma mensagem e não avançará.

### Alterações no Connect VC

Nas versões atuais do Adobe Learning Manager, um aluno era marcado como **Não Participar quando** estava inscrito em uma sessão vc do Connect, mas não atendeu aos critérios de conclusão.

Nesta versão, o status muda para **Ainda para marcar**.

### Rotulagem de branco no Adobe Learning Manager

O aplicativo para dispositivos móveis Adobe Learning Manager agora oferece suporte à rotulagem branca, o que significa que agora você pode liberar o aplicativo sob sua própria marca.

Consulte a rotulagem em branco no [aplicativo](white-label.md) móvel Adobe Learning Manager para obter mais informações.

### Nova coluna nos CSVs de migração

Nesta versão, há uma coluna nova opcional, uniqueLoId, nos CSVs de migração a seguir.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>A **coluna uniqueLoId** é opcional.


Se você realizar uma migração para atualizar um curso ou um plano de aprendizagem ou certificação existente, o curso, o plano de aprendizagem ou a certificação com a **uniqueLOId** são adicionados ao aplicativo do autor.

Ao migrar, é necessário atualizar os **valores uniqueLOId** nos CSVs para o curso, o plano de aprendizagem ou a certificação, mesmo que seja uma coluna opcional.

Se a **coluna uniqueLoId** não for adicionada antes de realizar a migração enquanto atualiza o curso existente, o plano de aprendizagem ou a certificação que tem **uniqueLOId**, depois da migração os **valores uniqueLOId** serão substituídos por valores NULOS.

>[!NOTE]
>
>A coluna **uniqueLoId** não se aplica ao CSV da ajuda de tarefa.


>[!IMPORTANT]
>
>Os valores de coluna devem ser exclusivos na conta. Você não pode usar o mesmo valor com um curso ou certificação.

Baixe os CSVs do [manual](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs) de migração.


### Avaliação do aplicativo

Um aluno pode fornecer seu feedback no aplicativo do Adobe Learning Manager para aprimorar ainda mais a experiência do aplicativo. Se o aluno classificar quatro estrelas ou mais, uma janela pop-up é exibida e solicita que o aluno avalie o aplicativo na Play Store ou na App Store.

### O Bluejeans chegou ao fim da vida útil (EOL) em fevereiro de 2024

Gostaríamos de informá-lo de que o Bluejeans chegou ao fim da vida útil (EOL) em fevereiro de 2024. Após fevereiro de 2024, o Bluejeans não receberá mais atualizações ou suporte. Nossas equipes de CSAM e suporte ajudarão você a tirar dúvidas ou preocupações sobre você durante esse período de transição.

Exiba [os conectores no Adobe Learning Manager](integration-admin/feature-summary/connectors.md) para obter mais informações sobre como configurar conectores.

### Alterações no relatório de acesso ao logon

O relatório de acesso ao logon só estará disponível nos últimos cinco trimestres. Se qualquer administrador de integração solicitar o download sob demanda da Exportação unificada com acesso **ao logon** selecionada, o Adobe Learning Manager exibirá uma mensagem de erro. No entanto, não há impacto sobre outros relatórios.

### Alterações no ADFS

Os campos Tipo de funcionário e ID do funcionário do ADFS agora estão disponíveis no Adobe Learning Manager, com base nos mapeamentos.

## Alterações da API nesta versão

### APIs do aluno

Nesta versão, adicionamos suporte à API para que os alunos visualizem o logotipo da marca e os temas personalizados em nível de Grupo de usuários.

As APIs /conta e /user?include=account retornam quatro campos, que serão substituídos de modo específico ao campo ativo do usuário que pertence a logoUrl, logoStyling e themeData.

### Novos atributos

Um novo atributo, isExpiredSubmission, em learningObjectResource, que mostra se o envio no recurso expirou ou não.

* GET /API da conta: Retorna o novo atributo **expireSubmissionDuration** X, onde X é o número de dias definido. Se não estiver definido, 0 será retornado
* API GET /LO com recurso inclui um novo atributo **isExpiredSubmission**&quot; True ou False.
   * Verdadeiro, se o envio for expirado e &quot;submissionUrl&quot; não for exibido.
   * Se for falso, o envio não expirou e &quot;submissionUrl&quot; é obtido.

### Alterações na API na lista de verificação

Um curso pode consistir em vários módulos dos quais a lista de verificação é um tipo de módulo. Este módulo de lista de verificação é avaliado pelo instrutor e pode ser marcado como Reprovado ou Êxito com base na avaliação.

Mas, em ambos os casos, o status da lista de verificação é marcado como Concluído e, dessa forma, o curso é marcado como Concluído.

Nesta versão, a API LO inclui o parâmetro *isChecklistMandatory*. Se o valor for Verdadeiro, a lista de verificação é obrigatória.

### Suporte a vários locais

Agora, um administrador pode baixar o relatório de feedback N1 no idioma de sua escolha. No entanto, ainda não é possível baixar relatórios de feedback N1 para o Power BI. Na solicitação de API, use o parâmetro preferidoLocale para especificar o local de sua preferência.

### Alterações na contagem de resumo da instância

Isso se aplica às contas em que as inscrições em um curso de sala de aula/sala de aula vc são superiores a 1000.

Se o número for menor do que 1000, as inscrições invalidam o cache e retornam os valores atualizados em uma chamada de API de resumo get, como, número de inscrição, conclusão e seatLimit.

Se a conta estiver habilitada para esse recurso e o número de inscrições for maior que 1000, os valores serão recuperados do cache.

### Caminhos obsoletos

Atualmente, as APIs do Gerenciador de aprendizado seguem uma estrutura de dados de gráfico que permite buscar dados atravessando o modelo de API por meio de inclusões. Mesmo que você possa percorrer uma API de até sete níveis, buscar os dados usando uma única chamada de API é computacionalmente caro.

Recomendamos que todos os clientes existentes e novos façam chamadas pequenas várias vezes em vez de uma chamada grande. Essa abordagem impedirá que dados indesejados sejam carregados na chamada.

#### Quais caminhos são obsoletos

Os seguintes caminhos são obsoletos:

* /learningObjects
   * Demarcadores obsoletos:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Caminhos existentes:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Caminho obsoleto:
      * enrollment.instances.subLoInstances.learningObject
   * Demarcador existente:
      * enrollment.instances.subLoInstances
* /Inscrições
   * Caminho obsoleto:
      * loInstance.learningObject.enrollment
   * Novo demarcador:
      * loInstance.learningObject
* /learningObjects/{id}
   * Caminho obsoleto:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Novo demarcador:
      * instance.subLoInstances

### Acesso de logon e alterações no arquivamento de relatórios de auditoria do usuário para API de tarefa

Com esta versão, a API de emprego manterá o Relatório de acesso ao logon em até cinco trimestres e o Relatório de auditoria do usuário por seis meses. Se quiser baixar os dados mais antigos que esse período, você deverá passar pelo parâmetro de arquivamento, especificando trimestre e ano. Consulte a carga de amostra.

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

Se você tentar baixar o **relatório de acesso** ao logon que ultrapassa cinco quartos, será exibida uma mensagem de erro. Uma mensagem de erro semelhante é exibida se você tentar baixar o relatório de auditoria **do** usuário que ultrapassa seis meses.

### APIs obsoletas

Exibir [reprovações de API no Adobe Learning Manager](api-deprecations-list.md) para obter uma lista cumulativa de todas as APIs obsoletas no produto.

## Erros corrigidos nesta atualização {#bug-fixes}

* Quando um aluno está inscrito em um curso e tenta se inscrever em outro curso, uma mensagem de aviso é exibida.
* Um grupo de usuários, mesmo depois de ser excluído, fica visível na pesquisa.
* Quando os usuários acionam muitas transcrições do aluno com uma grande quantidade de dados, a fila transcrições do aluno é bloqueada e evita uma nova solicitação.
* Se uma conta filho solicitar que sua conta principal compartilhe um relatório, a conta pai não poderá fazê-lo.
* Os URLs de um curso e um caminho de aprendizado são redirecionamentos para locais incorretos.
* Um aluno visualiza intermitentemente a instância de um curso diferente ao clicar no link do curso na página do catálogo.
* O **botão Cancelar inscrição** não é exibido como esperado após a primeira inscrição, mas o botão é exibido após uma atualização.
* Não é possível salvar conteúdo ou um quiz que tenha um espaço em branco no nome.
* Nos cursos aprovados pelo gerente, você pode inscrever novamente os alunos em um grupo de usuários.
* Em alguns casos, se você tentar adicionar um campo ativo adicional, a mensagem de erro &quot;Campos ativos não puderam ser salvos.&quot;, é exibida.
* O texto extravasa no nome de um curso dentro do cartão de um curso na seção Cursos relacionados.
* Depois de alterar uma instância e inscrever um aluno para a instância, as instâncias antigas ainda existem no calendário do Outlook.
* Quando um aluno de uma conta de parceiro tenta selecionar a miniatura de um curso, é exibida uma mensagem de erro.
* Quando os alunos se inscrevem em um curso, eles recebem várias notificações para a inscrição.
* Se um usuário altera manualmente o nome dos catálogos criados em um conector, os novos catálogos são criados e os cursos são publicados nos catálogos incorretos.
* Os usuários que pertencem a contas inativas ainda recebem emails de assinatura.

### Correções de erros relacionados à API

* A API GET/users não recupera detalhes de um Gerente.
* Em uma conta, os usuários foram criados através de uma importação programada de usuários de FTP durante um tempo de inatividade programado.
* No aplicativo móvel ou no modo imersivo, depois de excluir ou retirar uma instância do curso e selecionar a próxima instância ativa, o **botão Registrar interesse** é exibido em vez de **Inscrever-se**.
* Quando um aluno de uma conta entre parceiros tenta selecionar a miniatura de um curso usando a API do objeto de aprendizado, o erro 403 Proibido é exibido.

## Requisitos do sistema

Visualizar [os requisitos](system-requirements.md) de sistema do Adobe Learning Manager.

## Versões anteriores do Adobe Learning Manager

* [Versão de novembro de 2023](whats-new-november-2023.md)
* [Versão de julho de 2023](whats-new-2023-july.md)
