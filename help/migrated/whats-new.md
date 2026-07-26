---
description: Saiba mais sobre os novos recursos e aprimoramentos, incluindo alterações de API e webhooks, na versão de abril de 2026 do Adobe Learning Manager
jcr-language: en_us
title: Novidades do Adobe Learning Manager na versão de agosto de 2026
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
source-git-commit: 92789c5c943c1b4de68bf70ce9781e9f7832a9df
workflow-type: tm+mt
source-wordcount: '2889'
ht-degree: 0%

---

# Novidades na versão de agosto de 2026 do Adobe Learning Manager

>[!IMPORTANT]
>
>Os recursos descritos neste artigo estão disponíveis como parte da versão beta. Os recursos beta do Adobe Learning Manager são fornecidos para fins de avaliação e podem ser modificados, limitados ou removidos antes do lançamento de disponibilidade geral. Nomes de recursos, comportamento e opções de configuração estão sujeitos a alterações sem aviso prévio.


## Cursos adaptativos

Os cursos adaptativos permitem fornecer treinamento personalizado controlando quais módulos cada aluno vê e quais são necessários, com base nos grupos de usuários aos quais pertencem. Um único curso apresenta dinamicamente o conteúdo certo para a pessoa certa automaticamente.

Os autores configuram cada módulo com **Opcional** e **Obrigatório** para regras de grupo de usuários. Os alunos de diferentes grupos de usuários podem concluir conjuntos de módulos totalmente diferentes e ainda concluir o mesmo curso. Os limites de vagas para sessões de sala de aula e sala de aula virtual agora são aplicados no nível do módulo, de modo que um aluno pode ser inscrito em um curso enquanto está em lista de espera em uma sessão específica apenas. Para mais informações, consulte [Cursos adaptativos - Autor](/help/migrated/authors/feature-summary/adaptive-course-author.md)

Principais recursos:

* Visibilidade no nível do módulo e regras de conclusão por grupo de usuários
* Lógica OR-merge: se qualquer grupo tornar um módulo obrigatório, ele será obrigatório para esse aluno
* Lista de espera no nível do módulo para sessões de sala de aula e sala de aula virtual
* Conclusão de atualização acionada quando o perfil de um aluno é alterado
* Compatível com programações de aprendizado e certificações com limitações documentadas para certificações recorrentes

Saiba mais sobre os cursos adaptáveis.

## Quadro de notas

Um catálogo de notas no Adobe Learning Manager adiciona pontuação ponderada aos cursos, permitindo que os autores atribuam uma porcentagem de contribuição a cada módulo pontuado e definam uma pontuação agregada mínima para a conclusão do curso. Os alunos podem controlar suas notas ao longo do curso e os administradores podem visualizar as pontuações finais e baixar transcrições relevantes.

### O que a agenda faz

Um curso habilitado para livro de notas calcula a pontuação final de cada aluno combinando pontuações individuais do módulo de acordo com a porcentagem de ponderação atribuída a cada módulo. Isso fornece uma medida precisa e ponderada do desempenho, em vez de uma simples soma de pontuações ou um marcador de aprovação/reprovação baseado apenas na conclusão.

Gradebook suporta dois modelos de conclusão:

* **Somente módulos obrigatórios**: o curso é concluído quando todos os módulos obrigatórios são concluídos. As pontuações de gradebook ainda são calculadas e visíveis, mas a pontuação agregada não contribui para os critérios de aprovação.

* **Módulos obrigatórios mais pontuação agregada**: o aluno deve concluir todos os módulos obrigatórios e obter uma pontuação agregada no limite mínimo de aprovação ou acima dele. Ambas as condições devem ser cumpridas para obter um grau de aprovação.

### Como as pontuações dos cursos são calculadas

Para cada módulo pontuável, a contribuição para a pontuação agregada do curso é:

(Pontuação alcançada ÷ Pontuação máxima) × % de Ponderação = Contribuição do módulo

A pontuação agregada do curso é a soma de todas as contribuições do módulo. As porcentagens de ponderação em todos os módulos pontuáveis devem totalizar exatamente 100. A configuração do livro de notas não pode ser salva até que esta condição seja atendida.

A pontuação agregada do curso é a soma de todas as contribuições do módulo. As porcentagens de ponderação em todos os módulos pontuáveis devem totalizar exatamente 100. A configuração do livro de notas não pode ser salva até que esta condição seja atendida.

A escala de pontuação não precisa ser consistente em todos os módulos. Uma sessão de sala de aula com pontuação de 100 e um módulo SCORM com pontuação de 10 podem coexistir no mesmo livro de notas. A fórmula normaliza cada contribuição antes de aplicar a ponderação.

**Módulos pontuáveis e não pontuáveis**

Somente os módulos que produzem uma pontuação são qualificados para ponderação. Os tipos de módulo pontuáveis incluem:

* Conteúdo SCORM, AICC e xAPI com pontuação ativada
* Pacotes de conteúdo do Captivate
* Quizzes nativos no Adobe Learning Manager
* Sessões de sala de aula e sala de aula virtual nas quais o professor ou o administrador insere uma pontuação
* Módulos de atividade pontuados por um professor ou administrador

Tipos de módulos não pontuáveis, arquivos de PDF, arquivos de vídeo, arquivos de áudio, apresentações do PowerPoint, documentos do Word, arquivos do Excel e conteúdo de HTML não podem receber uma porcentagem de ponderação atribuída e não contribuem para a pontuação agregada. Esses módulos ainda podem ser necessários para a conclusão do curso. Quando a opção Incluir módulos que não contribuem para a nota final estiver ativada, eles serão exibidos no catálogo de notas sem um valor de ponderação.

Para obter mais informações, consulte [Gradebook para autores](/help/migrated/authors/feature-summary/alm-author-gradebook.md)

## Pastas hierárquicas de conteúdo

A Biblioteca de conteúdo agora oferece suporte a até três níveis de hierarquia de pastas privadas. Os administradores criam a estrutura de pastas e controlam quais funções personalizadas podem acessar quais pastas de Nível 1. Acesse em cascata automaticamente para todas as subpastas em uma pasta de Nível 1.

Os autores podem copiar e mover conteúdo entre pastas, filtrar a Biblioteca de conteúdo por pasta e navegar pela hierarquia ao adicionar módulos a um curso.

Principais recursos:

* Até três níveis de aninhamento (máximo de 25 subpastas por pai)
* Acesso baseado em função atribuído apenas no Nível 1
* O conteúdo pode aparecer em várias pastas sem duplicação
* A pasta pública e a estrutura de pasta privada são mutuamente exclusivas
* Explorar a experiência de pastas ao selecionar módulos na criação do curso

Para obter mais informações sobre as funcionalidades no nível de administrador, consulte [Pastas de conteúdo hierárquico](/help/migrated/administrators/feature-summary/settings/advanced-settings.md#content-folder). Para obter mais informações sobre as funcionalidades no nível de autor, consulte [Pastas de conteúdo hierárquico](/help/migrated/authors/feature-summary/content-library.md#add-content-to-a-folder).

Se estiver migrando o conteúdo de aprendizado de outra plataforma para o Adobe Learning Manager e quiser preservar sua organização de pastas existente, você pode usar arquivos CSV para criar uma estrutura de pastas hierárquica e associar seus arquivos de conteúdo às pastas apropriadas. Saiba mais sobre a migração em [Migrar hierarquia de pastas de conteúdo](/help/migrated/integration-admin/feature-summary/migration-manual.md#migratecontentfolderhierarchy)

## Hub ao vivo

O Live Hub é uma experiência de treinamento virtual viabilizada por IA no Adobe Learning Manager que ajuda as organizações a oferecer aprendizado dinâmico envolvente e impactante. Com recursos inteligentes, como pesquisas com IA, orquestração de salas para sessão de grupo, espaços de aprendizado persistentes e assistência viabilizada por IA, o Live Hub superrecarrega a produtividade do professor enquanto reduz a complexidade da entrega da sessão.

Principais destaques:

* Aprimore o aprendizado ao vivo com uma experiência nativa do Adobe Learning Manager que melhora a qualidade instrucional e os resultados do aluno.
* Dê aos professores um cofacilitador viabilizado por IA que orienta o engajamento por meio de pesquisas inteligentes, suporte a perguntas e respostas e insights de sala de sessão de grupo.
* Ajude os alunos a obter mais de cada sessão com resumos gerados por IA e gravações de sessão pesquisáveis por tópicos.
* Meça o que é importante com análises de envolvimento que vão além da participação para revelar a participação real no aprendizado.
* Ajude seus autores a usar o localizador de professores viabilizado por IA para combinar com o professor certo por habilidades, disponibilidade, horários preferenciais, fuso horário e utilização atual.

>[!NOTE]
>
>O Live Hub está atualmente na versão beta e estará disponível na próxima versão de agosto do Adobe Learning Manager. A documentação do Live Hub estará disponível assim que o recurso for lançado.


## Criador de modelos de email baseados em componentes

As organizações agora podem criar notificações por email de marca, de nível corporativo, no Adobe Learning Manager usando um editor de componentes WYSIWYG moderno. Os administradores podem criar um layout global uma vez, com um cabeçalho, um rodapé e elementos de marca reutilizáveis, e aplicá-los a todos os modelos de email no nível da conta. Modelos individuais podem ser personalizados no nível do curso ou da instância, herdando o layout principal por padrão e substituindo-o somente quando necessário.

Principais recursos:

* Editor WYSIWYG com uma biblioteca de componentes reutilizáveis (texto, imagem, botão, divisor, cabeçalho, rodapé)
* Suporte a variáveis: insira campos dinâmicos, como nome do aluno, nome do curso e data de vencimento
* Hierarquia de modelos vinculados e não vinculados: as alterações feitas em um modelo vinculado são propagadas para todos os modelos filhos; os modelos não vinculados são editáveis de maneira independente
* Suporte a modelos em vários idiomas
* Visualizar e testar-enviar antes de publicar
* Compatibilidade com versões anteriores: os modelos de email existentes continuam funcionando

Para obter mais informações, consulte [Criador de email baseado em componentes](/help/migrated/administrators/feature-summary/email-builder.md)

## Suporte externo ao aprendizado

Os alunos agora podem enviar treinamento fora da plataforma, como certificações, workshops, conferências e cursos externos, para aprovação do gerente diretamente do painel do aluno. Os envios aprovados aparecem na transcrição do aluno.

Principais recursos:

* Formulário de envio configurável com campos padrão e personalizados
* Fluxo de trabalho de revisão e aprovação do gerente com suporte para comentários
* Os envios aprovados aparecem na transcrição do aluno com metadados completos
* O administrador pode configurar campos obrigatórios, incluindo campos personalizados
* Novas colunas nas transcrições do administrador e do aluno: nome do aprendizado externo, comentário de conclusão, colunas de campo personalizado
* Suporte à API: cinco novos pontos de extremidade no escopo do aluno para criar, recuperar e atualizar envios

Para obter mais informações no nível de administrador, consulte [Suporte a aprendizado externo](/help/migrated/administrators/feature-summary/settings/basic-settings.md). Para obter mais informações no nível de gerente, consulte [Suporte de aprendizado externo](/help/migrated/managers/feature-summary/review-external-learning-requests.md). Para obter mais informações no nível do aluno, consulte [Suporte de aprendizado externo](/help/migrated/learners/feature-summary/submit-external-learning.md).

## Recursos de IA

### Assistente de IA para alunos

O Assistente de IA para alunos agora oferece suporte a quatro novos recursos, além de responder a perguntas de conteúdo de aprendizado atribuído:

* **Resumos do curso**: use o comando / para selecionar um item de catálogo e gerar um resumo sem abrir o curso
* **Comparação de objetos de aprendizado**: selecione até dois objetos de aprendizado usando o comando / e peça que o assistente os compare
* **Respostas do Adobe Experience League**: o assistente agora fornece respostas para perguntas sobre instruções da documentação de ajuda do Adobe Learning Manager
* **Consultas de conteúdo de terceiros**: o conteúdo do catálogo do Go1 e do LinkedIn Learning pode ser consultado (somente metadados; somente inglês; a ingestão leva de 1 a 2 horas após o catálogo ser adicionado)

Para obter mais informações, consulte [Assistente do AI para alunos](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

### Agente do Caminho de Aprendizado

Os alunos agora podem ter uma conversa guiada com o Assistente de IA para gerar um caminho de aprendizado personalizado e sequenciado com base em seus objetivos, plano de fundo e tempo disponível. O caminho de aprendizado é criado automaticamente e o aluno é inscrito.

Principais recursos:

* A conversa de várias rodadas orienta o aluno na seleção de tópico, na revisão do curso e na confirmação do caminho
* Até cinco tópicos de aprendizado sugeridos por conversa
* Seleção de curso dos catálogos atribuídos
* No máximo 10 programações de aprendizado personalizadas visíveis na página inicial do aluno
* Caminhos concluídos podem ser compartilhados com colegas

Para obter mais informações, consulte [Agente do Caminho de Aprendizado](/help/migrated/learners/feature-summary/learning-path-agent.md).

### Agente de insights

O Agente do Insights ajuda os administradores a analisar dados de aprendizado por meio de consultas a idiomas naturais. Faça perguntas sobre tendências de inscrição, taxas de conclusão, envolvimento do aluno e lacunas de habilidades. O agente gera relatórios e visualizações em resposta.

Para obter mais informações, consulte [Agente do Insights](/help/migrated/administrators/feature-summary/insights-agent.md)

### Créditos de IA da geração

O Adobe Learning Manager integra recursos com IA gerenciados por meio de um sistema baseado em crédito vinculado a licenças do Agent Orchestrator. Esse sistema exige que os administradores ativem recursos, definam limites de crédito e monitorem o uso por meio da página Faturamento. Vincular a conta do Adobe Learning Manager a uma organização do Adobe Admin Console com uma licença ativa do Agent Orchestrator é essencial para ativar os recursos do Gen AI.

Para obter mais informações, consulte [Créditos de IA da geração](/help/migrated/administrators/feature-summary/billing-management.md#genaicredits)

## Canais

Os canais fornecem um modo centralizado de organizar, publicar e descobrir conteúdo de vídeo a partir de páginas da Web e de Confluência. Os administradores podem criar e gerenciar canais conectando páginas da Web ou páginas da conferência compatíveis, definir configurações de canal, controlar a visibilidade e sincronizar o conteúdo da origem. Os alunos podem navegar pelos canais disponíveis, assinar canais de interesse e assistir a conteúdos de vídeo selecionados em um único local.

Para obter mais informações, consulte [Criar Canais](/help/migrated/administrators/feature-summary/create-channels.md)

## Criador de relatórios

O Report Builder oferece aos administradores uma ferramenta de emissão de relatórios de autoatendimento flexível que vai além dos tipos de relatórios fixos disponíveis em outras partes do Adobe Learning Manager. Em vez de se limitarem a estruturas de relatório predefinidas, os administradores podem unir campos de vários conjuntos de dados, como Usuário, Grupos de usuários, Cursos e Caminhos de aprendizado, Módulos, Transcrição, Catálogos e muito mais, em um único relatório personalizado personalizado personalizado personalizado adaptado às necessidades de dados específicas de sua organização.

Os relatórios são criados uma vez e salvos para uso repetido. Não há necessidade de recriar filtros, reaplicar agrupamentos ou reingressar conjuntos de dados em cada download. Os relatórios salvos podem ser baixados por demanda, compartilhados com outros administradores ou configurados com uma assinatura para que os destinatários recebam relatórios atualizados automaticamente em um intervalo regular.

Para obter mais informações, consulte [Report Builder](/help/migrated/administrators/feature-summary/alm-report-builder.md).

## Alterações de função personalizada

Os administradores personalizados agora podem receber recursos expandidos de gerenciamento de usuários por meio do nível de permissão Avançado em Usuários em uma definição de função personalizada.

Dois níveis de acesso estão disponíveis:

| Nível de acesso | O que o administrador personalizado pode fazer |
|---|---|
| **Somente leitura** | Exibir todas as funções personalizadas, logs de importação e usuários excluídos; baixar o relatório de funções personalizadas |
| **Controle total** | Todos os recursos somente leitura, além de: criar, editar, excluir e atribuir funções personalizadas; importar usuários via CSV; limpar usuários excluídos |

Saiba mais sobre Alterações de função personalizada. Para obter mais informações, consulte [O que a permissão avançada de usuário desbloqueia](/help/migrated/administrators/feature-summary/custom-role.md#whatadvanceduserpermissionunlocks)

## deep linking LTI

Os administradores de integração agora podem ativar a Vínculo profundo de LTI para configurações de ferramentas de LTI, permitindo que os autores do curso naveguem e incorporem cursos do Adobe Learning Manager diretamente de um LMS externo sem copiar manualmente os URLs do curso.

Uma vez habilitado, os autores veem um botão **Selecionar conteúdo** na configuração de atividade LMS externa. Eles podem navegar por catálogos aprovados, selecionar cursos e confirmar a seleção — com todos os campos preenchidos automaticamente.

Para obter mais informações, consulte [deep links de LTI](/help/migrated/integration-admin/feature-summary/lti-deep-links.md).

## Locais de sala de aula

Os locais de sala de aula agora oferecem suporte a um **formato de local de quatro campos** estruturado, incluindo País, Estado/Província/Região, Cidade e Nome do Local, facilitando o gerenciamento e a organização de locais de treinamento em todas as regiões. A atualização inclui uma migração única do formato herdado de campo único e adiciona suporte multilíngue aos campos **Nome do local** e **Informações da sala**, permitindo detalhes da sala de aula localizados para os alunos.

Para mais informações, consulte [Locais de sala de aula](/help/migrated/administrators/feature-summary/classroom.md)

## Em breve: Adobe Learning Manager Content Composer

O Adobe Learning Manager Content Composer é uma futura ferramenta de criação de curso de IA no Adobe Learning Manager que ajuda a criar um curso pronto para publicação em um piscar de olhos.

Um assistente de IA conversacional guiará você por todo o processo: Prompt, Resumo, Esquema e Curso, para que você mantenha o controle em cada etapa, revisando e refinando antes de seguir em frente. Você poderá mover conteúdo em seus próprios documentos de origem, aplicar temas instantâneos do curso e compartilhar ou exportar cursos concluídos por meio do SCORM ou publicar diretamente no Adobe Learning Manager.

## Relatório de alterações na versão

Saiba mais sobre as [alterações de relatórios na versão de agosto de 2026 do Adobe Learning Manager](/help/migrated/reporting-changes-august-2026.md).

## Alterações de API na versão

Saiba mais sobre as [alterações de API na versão de agosto de 2026 do Adobe Learning Manager](/help/migrated/api-changes-august-2026.md).

## Outros aprimoramentos na versão

| Aprimoramento | Descrição |
|---|---|
| **MQA: pontuação mais recente vs. mais alta** | Para módulos com várias tentativas, os autores agora podem escolher se a pontuação da tentativa Mais recente ou Mais alta é gravada na transcrição do aluno e usada nos cálculos do catálogo de notas. O padrão existente era o mais recente e assim permanecerá quando a configuração não estiver definida. Para obter mais informações, consulte [Gradebook para autores](/help/migrated/authors/feature-summary/alm-author-gradebook.md#configurescoresettingsmultipleattempts). |
| **Visualização de conteúdo na Biblioteca de Conteúdo** | Os autores agora podem visualizar os arquivos de conteúdo carregados diretamente na Biblioteca de conteúdo antes de adicioná-los aos cursos. Para obter mais informações, consulte [Visualizar Biblioteca de Conteúdo](/help/migrated/authors/feature-summary/content-library.md#previewcontentlibrary). |
| **Relatório de usuário incremental** | Um novo relatório de usuário baseado em API retorna apenas os usuários criados ou modificados desde a última solicitação, reduzindo a transferência de dados para contas grandes usando fluxos de trabalho de sincronização automática de usuários. Para obter mais informações, consulte [Relatório de Usuário Incremental](/help/migrated/incremental-user-report.md). |
| **11 novos idiomas no fluidic player** | O Fluidic Player agora oferece suporte a 11 idiomas adicionais, incluindo suporte a script da direita para a esquerda (RTL). Para obter mais informações, consulte [Fluidic Player](/help/migrated/learners/feature-summary/fluidic-player.md). |
| **Migração de módulo de LTI** | Os módulos existentes da LTI 1.1 agora podem ser migrados para a LTI 1.3 usando a ferramenta de migração. Para obter mais informações, consulte [Migração de LTI de módulos](/help/migrated/integration-admin/feature-summary/migration-manual.md#migrationofltimodules). |
| **Construtor de Email: Suporte ao Editor de Rich Text** | Os modelos de e-mail no Adobe Learning Manager agora são compatíveis com formatação de rich text, anexos e automações personalizadas. Para obter mais informações, consulte o [Criador de Email](/help/migrated/administrators/feature-summary/email-builder.md). |
| **Construtor de Email: recurso de visualização** | Use a opção Visualizar para verificar como o email composto será exibido no final do destinatário. Para obter mais informações, consulte o [Criador de Email](/help/migrated/administrators/feature-summary/email-builder.md). |
| **Padronização de carimbo de data/hora do webhook** | Todos os campos de data e hora no objeto `data` de cargas de webhook agora têm segundos definidos como `00`, fornecendo uma precisão de nível de minuto consistente com os relatórios de Transcrição do aluno. |
| **Aprimoramentos do Connect** | Atualizações do conector do Azure Data Lake Storage (ADLS); suporte a nome de sala persistente para sessões recorrentes de sala de aula virtual; controle de participação baseado em exibição de gravação. |
| **Melhorias no desempenho do reprodutor** | O Fluidic Course Player foi otimizado para tempos de carregamento mais rápidos e transições mais suaves entre módulos. |
| **Aviso de impacto antes de retirar cursos/LPs** | Os administradores agora veem um aviso listando todas as inscrições ativas e caminhos de aprendizado dependentes antes que um curso ou caminho de aprendizado possa ser desativado. |
| **Módulo CR/VC: duração esperada** | Os autores agora podem definir uma duração esperada para os módulos de sala de aula e sala de aula virtual, separados do tempo de sessão agendada. Esse valor aparece nos relatórios e nas informações do curso voltado para o aluno. |
| **Confirmação antes de editar cursos adquiridos** | Os administradores em contas entre parceiros agora veem uma caixa de diálogo de confirmação antes de editar um curso adquirido por meio do compartilhamento de catálogo, evitando alterações não intencionais no conteúdo compartilhado. |
| **URL de sessão com ID de instância** | Os URLs de inicialização da sessão para sessões do Microsoft Teams, Adobe Connect e Zoom agora incluem a ID da instância, garantindo que os alunos sejam direcionados para a sessão correta quando houver várias instâncias. |
| **Aviso para comunicados de grandes audiências** | Ao enviar um email de anúncio ad-hoc para mais de um limite configurável de destinatários, os administradores agora veem um aviso de volume antes de enviar. |
| **Modelos de email: URL da conta para alunos externos** | Os modelos de notificação por e-mail agora podem incluir um URL de conta separado especificamente para alunos externos, encaminhando-os para a experiência de logon correta. |
| **AEM Sites** | Agora há apenas um botão **Editar** na seção **Seu perfil** > Suas áreas de interesse para editar suas preferências de Produtos e Funções e Habilidades. Isso também faz parte do learning manager nativo. |
| **AEM Sites** | Anteriormente, havia dois botões **Editar**, mas agora o botão **Editar** é um botão consolidado para modificar suas preferências de Produtos e Funções e Habilidades. |
| **Fuso Horário** | Uma nova caixa de pesquisa foi adicionada logo abaixo do campo Fuso horário nas Configurações do perfil do usuário conectado. A caixa de pesquisa pode ser usada para procurar um fuso horário diretamente, em vez de percorrer toda a lista de fusos horários disponíveis. Se quiser alterar o fuso horário existente, selecione um novo fuso horário e clique em Salvar. O novo fuso horário é salvo. O botão Salvar aparece somente quando você seleciona um fuso horário. |

## Requisitos do sistema

Exibir [requisitos de sistema do Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notas de versão

Confira as [notas de versão](/help/migrated/release-note/release-notes.md) para obter as atualizações de versão mais recentes.

## Versões anteriores do Adobe Learning Manager

* [Versão de abril de 2026 do Adobe Learning Manager](/help/migrated/whats-new-april-2026.md)
* [Versão de outubro de 2025 do Adobe Learning Manager](/help/migrated/whats-new-october-2025.md)
