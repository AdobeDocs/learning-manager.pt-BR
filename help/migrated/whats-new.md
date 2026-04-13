---
description: Saiba mais sobre os novos recursos e aprimoramentos, incluindo alterações de API e webhooks, na versão de abril de 2026 do Adobe Learning Manager
jcr-language: en_us
title: Novidades na versão de abril de 2026 do Adobe Learning Manager
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
source-git-commit: 971a9c79fc2b831b990e30a44a2eeab5d5c5ce63
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 0%

---

# Novidades na versão de abril de 2026 do Adobe Learning Manager

**Para alunos:** o Fluidic Player agora mostra o nome do próximo módulo e um botão Limpar saída. O idioma do reprodutor pode ser definido por meio de LTI para uma experiência consistente em todas as plataformas. O nome do parâmetro personalizado é &#39;locale&#39; e aceita o código de localidade. Por exemplo, locale=fr-FR. o conteúdo do Captivate inclui um sumário unificado, marcas de conclusão no nível do slide e exportações de notas confiáveis. O suporte a vários idiomas está disponível para ajudas de tarefa, perguntas de lista de verificação e faixas de texto de vídeo (VTT). O Assistente de IA ajuda os alunos a obter respostas dentro da experiência de aprendizado.

**Para administradores e autores:** o conector do Zoom oferece suporte a várias sessões VILT simultâneas. Os cursos compartilhados em contas entre parceiros exibem o autor real em vez de “Autor externo”. Os administradores podem restringir quando os módulos podem ser iniciados. As datas de expiração do objeto de aprendizado são expostas nas APIs do aluno. Os módulos de lista de verificação oferecem suporte à pontuação ponderada, ao texto da pergunta multilíngue e aos comentários opcionais do revisor. Os certificados personalizados oferecem um editor de arrastar e soltar com campos dinâmicos e planos de fundo gerados por IA. O Experience Builder não conectado permite criar páginas de aprendizado público sem exigir logon.

**Para professores:** gere códigos QR para registro de instância e presença de sessão. Adicione comentários ou feedback durante a avaliação da lista de verificação.

**Relatórios e análises:** o conteúdo do SCORM agora pode relatar várias tentativas de questionário nos relatórios L2. O tempo de aprendizado gasto no cálculo foi aprimorado nas transcrições do aluno. Os relatórios de transcrição de aprendizado dos administradores são atualizados. Aprimoramentos de pesquisa avançada estão disponíveis.

**Método de logon:** saiba como o logon do OpenID Connect funciona no Adobe Learning Manager para alunos, autores e administradores. O OpenID Connect (OIDC) é um método de logon comum desenvolvido em padrões da Web. Muitas organizações usam
um provedor de identidade (por exemplo, Okta, Google Workspace ou Microsoft Entra ID) para funcionários e parceiros.

Exiba [logon com OIDC](/help/migrated/oidc.md) para obter mais informações.

## Webhooks e migração em alternativas e equivalentes

### Webhooks

Quando um aluno conclui um curso por meio de uma alternativa ou relação, o ALM aciona um evento de webhook separado do webhook de conclusão de curso padrão. Isso garante que as integrações possam responder de forma diferente a conclusões alternativas, quando necessário. Os eventos do webhook também são acionados quando ocorre conclusão retroativa ou inconclusão retroativa, abrangendo atualizações históricas, bem como alterações de relacionamento.

Exiba [Webhooks](/help/migrated/integration-admin/feature-summary/webhooks.md#webhooks-for-alternates) para obter mais informações.

### Migração

O modelo de dados baseado em CSV e o comportamento de migração para introduzir a equivalência do objeto de aprendizado (LO) no sistema estão descritos em [Webhooks](/help/migrated/integration-admin/feature-summary/migration-manual.md#migration-for-alternates-and-equivalents).

## Remoção automática de usuários excluídos

A remoção automática de usuários excluídos é um recurso que limpa os dados de usuários que já foram excluídos no ALM. A remoção ocorre após um período de retenção configurável, com foco em operações em massa, para que as contas grandes de clientes possam ser tratadas de forma eficiente sem prejudicar o desempenho.

Exiba [Limpeza automática de usuários excluídos](/help/migrated/administrators/feature-summary/purge-users.md#auto-purge-of-deleted-users) para obter mais informações.

## Definir controle de tempo de acesso ao módulo

O aprimoramento permite que autores e administradores no Adobe Learning Manager definam uma janela de tempo durante a qual os alunos têm permissão para iniciar um módulo. Fora da janela inicial/final configurada, o módulo permanece visível na estrutura do curso, mas os alunos não podem iniciá-lo.

Exiba [Definir controle de tempo de acesso ao módulo](/help/migrated/administrators/feature-summary/module-access-time-control.md) para obter mais informações.

## Alterações nas transcrições do aluno

Esta versão aprimora o relatório de transcrições de aprendizado (LT) com maior capacidade de auditoria e suporte de conformidade.

* Uma nova coluna Método de conclusão no LT de administração mostra se as conclusões foram diretas, alternativas ou revogadas, enquanto as conclusões alternativas agora influenciam o status, a data de conclusão e a origem da conclusão usando datas herdadas de treinamentos de origem e atualizando quando as origens são revogadas ou ocorrem conclusões diretas.
* As alternativas revogadas ajustam automaticamente o status, a data de conclusão e a origem da conclusão quando todos os relacionamentos qualificados são removidos com inconclusão retroativa ativada.
* O feedback do revisor nos módulos de lista de verificação é padronizado na coluna Comentários do revisor renomeada nos LTs do administrador e do aluno e em todos os canais de exportação.
* Finalmente, os cálculos do tempo de aprendizado agora distinguem melhor o tempo ativo do tempo ocioso, melhorando a precisão do compromisso e da emissão de relatórios de conformidade.

Exiba [Alterações no relatório de transcrição do aluno](/help/migrated/administrators/feature-summary/reports/changes-in-learner-transcript.md) para obter mais informações.

## Lista de verificação com recurso de comentários para revisor

Esse recurso permite que os revisores adicionem comentários ou feedback durante a avaliação da lista de verificação. Você pode fornecer feedback personalizado e acionável para cada aluno. Você também pode optar por exibir seu nome com seus comentários para transparência. Todos os comentários são salvos na transcrição do aluno e incluídos nos relatórios da lista de verificação.

Exiba [Configurar lista de verificação com comentários](/help/migrated/authors/feature-summary/courses.md#checklist-with-commenting) para obter mais informações.

## Suporte a vários idiomas para lista de verificação

Este recurso permite criar e gerenciar módulos de lista de verificação em vários idiomas. Cada pergunta, instrução e critério de avaliação da lista de verificação pode ser traduzida para que os revisores e alunos interajam com a lista de verificação em seu idioma preferido. O sistema exibe a lista de verificação no idioma de conteúdo selecionado do usuário, o que melhora a acessibilidade e a conformidade para equipes globais.

Exibir [Criar lista de verificação de vários idiomas nos módulos](/help/migrated/authors/feature-summary/courses.md#create-a-multi-language-checklist)

## Ponderação de pergunta da lista de verificação para avaliações do professor

Esse recurso permite atribuir pontuações máximas diferentes (ponderação) a cada pergunta da lista de verificação. Você pode refletir a importância ou dificuldade variável de cada pergunta, o que permite avaliações mais precisas e significativas. O sistema calcula a pontuação total com base na sua entrada e determina se o aluno é aprovado ou reprovado de acordo com os critérios definidos.

Exibir [Criar perguntas de lista de verificação ponderadas](/help/migrated/authors/feature-summary/courses.md#how-to-create-a-weighted-checklist)

## Certificados personalizados

Os certificados personalizados no Adobe Learning Manager (ALM) permitem que administradores e autores projetem, gerenciem e emitam certificados personalizados para alunos.

O recurso inclui um editor de arrastar e soltar, campos dinâmicos, suporte a vários idiomas e planos de fundo gerados por IA, permitindo que as organizações criem certificados de marca sem conhecimento técnico.

Exibir [Criar certificados personalizados](/help/migrated/administrators/feature-summary/create-customize-certificate.md)

## Experiência não conectada no Experience Builder

A experiência não conectada no Experience Builder permite que as organizações exibam o conteúdo de aprendizado e as páginas do portal para todos os visitantes, incluindo aqueles que não fizeram logon. Esse recurso foi desenvolvido para atrair, informar e envolver alunos potenciais, oferecendo uma visualização suave e com marca de suas ofertas de treinamento antes de exigir que eles façam logon ou se inscrevam.

Exibir [Experiência não conectada no Experience Builder](/help/migrated/administrators/feature-summary/experience-builder/non-logged-in-experience.md)

## Aprimoramentos de pesquisa avançada

Os resultados da pesquisa em Pesquisa avançada agora são mais precisos e relevantes. As correspondências de palavras-chave exatas são classificadas mais alto na pesquisa de conteúdo e nos metadados, facilitando para os alunos encontrar exatamente o que estão procurando.

Os alunos agora também podem ver os objetos de aprendizado inscritos nos resultados de pesquisa, mesmo que não façam parte de um catálogo acessível, garantindo que nenhum conteúdo relevante seja perdido. Além disso, a classificação da ajuda de tarefa foi aprimorada tanto na pesquisa avançada quanto na pesquisa de conteúdo, trazendo à tona os recursos mais relevantes mais rapidamente.

## Ajudas de tarefa em vários idiomas

As ajudas de tarefa multilíngues no Adobe Learning Manager (ALM) permitem que autores e administradores forneçam documentos complementares, guias ou recursos em vários idiomas em uma única entrada de ajuda de tarefa. Os alunos em diferentes regiões podem acessar materiais relevantes em seu idioma de preferência, o que melhora a compreensão, a conformidade e a experiência do usuário.

Exiba [Adicionar ajudas de tarefa multilíngues](/help/migrated/authors/feature-summary/job-aids.md#create-a-multilingual-job-aid) para obter mais informações.

## Suporte a Faixas de texto de vídeo (VTT) multilíngues (para autores)

O suporte a Faixas de texto de vídeo (VTT) multilíngues no Adobe Learning Manager permite que os autores forneçam legendas para conteúdo de áudio e vídeo em vários idiomas. Esse recurso simplifica a localização, tornando o treinamento acessível a um público global e garantindo a conformidade com os padrões de acessibilidade. Os autores podem gerar, traduzir, revisar e editar automaticamente arquivos VTT diretamente na plataforma.

Consulte [Suporte a VTT multilíngue](/help/migrated/authors/feature-summary/content-library.md#multi-lingual-vtt-support) para obter mais informações.

## Mostrar o autor original dos cursos compartilhados em contas entre parceiros

Quando um curso é compartilhado pelo catálogo para uma conta entre parceiros, o Adobe Learning Manager atualmente rotula o autor como “Autor externo” nas exibições do aluno, administrador e autor da conta de recebimento. Isso pode criar desafios para alunos e administradores, especialmente em grandes empresas, pois torna-se difícil identificar e entrar em contato com o proprietário de conteúdo apropriado quando surgem problemas ou dúvidas.

O aprimoramento garante que as informações do autor sejam preservadas e apresentadas em cursos compartilhados em contas entre parceiros, em vez de serem substituídas por um espaço reservado genérico.

### Novidades

Mostrar nome do autor real dos cursos compartilhados em contas entre parceiros

Para cursos compartilhados por meio de catálogos externos ou de mesmo nível, o nome do autor original da conta de origem agora é exibido na conta de recebimento em vez de “Autor externo”.

Aplica-se a:

* Aplicativo do aluno (cartão do curso ou detalhes do curso).
* Visualizações do administrador e do autor ao visualizar como aluno.

Exiba a [exibição do nome do autor dos cursos compartilhados](/help/migrated/administrators/feature-summary/peer-account.md#author-name-display-for-shared-courses-including-previously-acquired-courses) para obter mais informações.

## Equivalentes e suplentes

Forneça uma experiência de aprendizado sem problemas e elimine o treinamento redundante com equivalentes e alternativos no ALM. Esse novo recurso permite que os administradores configurem regras unidirecionais (alternativas) ou bidirecionais (equivalentes), onde a conclusão de um treinamento concede automaticamente a conclusão alternativa para outro. Projetado para otimizar grandes ecossistemas de aprendizado, esse recurso garante que os alunos ignorem o conteúdo que já dominaram e as organizações reduzam drasticamente os tíquetes de suporte administrativo, eliminem substituições manuais e mantenham um registro de aluno mais limpo e preciso.

Exiba [Equivalentes e alternativas](/help/migrated/administrators/feature-summary/alternates-equivalence.md) para obter mais informações.

## Códigos QR do professor para inscrição de instância e participação na sessão

Os professores podem gerar códigos QR por conta própria para:

* Inscrição na instância do curso,
* Participação na sessão ou
* Inscrição + participação conjunta

no nível da sessão. Ele foi projetado para situações em que os alunos entram em uma sala de aula física ou híbrida e exigem uma opção rápida de autoatendimento para se inscrever e registrar sua participação usando um código QR.

Exiba [Baixar códigos QR para inscrição e presença do aluno](/help/migrated/instructors/feature-summary/learners.md#download-qr-codes-for-learner-enrollment-and-attendance) para obter mais informações.

## Convites do calendário (ICS) com links de sessão

O Adobe Learning Manager inclui o **link de ingresso na sessão diretamente em convites do calendário (arquivos ICS)** enviados para alunos e professores. Isso permite que os participantes ingressem em sessões diretamente de seu calendário sem pesquisar o email da sessão.

Esse aprimoramento melhora a experiência de clientes de calendário, como o **Gmail** e o **Outlook**.

Exiba [Convites de calendário com links de sessão](/help/migrated/instructors/feature-summary/learners.md#joining-a-session-from-gmail) para obter mais informações.

## Assistente de IA para alunos

O Assistente de IA (beta) para alunos os ajuda a encontrar rapidamente respostas a partir do conteúdo de aprendizado atribuído sem navegar pelos cursos inteiros. Você pode fazer perguntas em linguagem simples e receber respostas precisas e focadas com links de origem para o conteúdo relevante do curso.

Os recursos, os cenários compatíveis e as limitações podem mudar conforme o recurso evolui. O Assistente de IA é um complemento de bate-papo gerado por IA no Adobe Learning Manager que fornece respostas rápidas e precisas usando conteúdo de aprendizado confiável. Inclui citações para que você sempre saiba a fonte da informação.

Exibir o [Assistente de IA para alunos](/help/migrated/learners/feature-summary/learner-ai-assistant.md)


## Alterações de API na versão

A versão de abril de 2026 do Adobe Learning Manager apresenta aprimoramentos focados na API pública em torno de alternativas e equivalentes, acesso em janela de tempo ao conteúdo, tentativas de questionário orientadas por conteúdo, experiências não conectadas e manipulação de ajuda de tarefa. As alterações são projetadas para serem amplamente compatíveis com versões anteriores, permitindo integrações mais precisas.

Exibir [alterações de API na versão de abril](/help/migrated/api-changes-alm.md)

## Requisitos do sistema

Exibir [requisitos de sistema do Adobe Learning Manager](/help/migrated/system-requirements.md).

## Notas de versão

Confira as [notas de versão](/help/migrated/release-note/release-notes.md) para obter as atualizações de versão mais recentes.

## Versões anteriores do Adobe Learning Manager

* [Versão de outubro de 2025 do Adobe Learning Manager](/help/migrated/whats-new-october-2025.md)
* [Versão de maio de 2025 do Adobe Learning Manager](/help/migrated/whats-new-may-2025.md)
