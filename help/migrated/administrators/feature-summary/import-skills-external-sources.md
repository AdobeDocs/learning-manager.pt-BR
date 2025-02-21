---
jcr-language: en_us
title: Importar habilidades de fontes externas
description: Importe habilidades de provedores de conteúdo, como LinkedIn e Go1, usando os respectivos conectores.  As habilidades importadas serão adicionadas às habilidades definidas pelo administrador no Learning Manager e estarão disponíveis para os autores durante o fluxo de trabalho de criação do curso.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: d96b25245daadaa0f5a330bcf8a7ab5bba995876
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Importar habilidades de fontes externas

Importe habilidades de provedores de conteúdo, como LinkedIn e Go1, usando os respectivos conectores. Esse aprimoramento é uma parte da meta para a capacidade do Learning Manager de se integrar a nuvens de habilidades e sistemas de gerenciamento de talentos externos. As habilidades importadas serão adicionadas às habilidades definidas pelo administrador no Learning Manager e estarão disponíveis para os autores durante o fluxo de trabalho de criação do curso. Também foram feitos aprimoramentos na funcionalidade de pesquisa de habilidades em toda a plataforma para fornecer uma melhor experiência de pesquisa quando a conta tem um grande número de habilidades.

## Configurar importação de habilidade

Siga as etapas no procedimento para ativar a importação de habilidades na conta.

1. No aplicativo de administração, selecione **Configurações** no painel esquerdo.
1. Selecione **Geral**.
1. Na seção **Importação de habilidades**, selecione **Habilitar**. Se ativado, você pode escolher uma origem externa para importar habilidades. Uma vez ativado, para todas as importações subsequentes de recursos de aprendizado, as habilidades serão importadas para o repositório de habilidades para itens recém-importados. As habilidades dos recursos de aprendizado existentes podem ser importadas para o repositório de habilidades uma vez e, para executar esta execução inicial, entre em contato com seu CSM.
1. Selecione um provedor de conteúdo na lista suspensa.

Como administrador, você só pode importar habilidades de uma origem de habilidade.

### Nível de habilidade padrão

O nível de habilidade padrão é um e Crédito é 10 após a migração das habilidades.

Não é possível editar o nome da habilidade, a descrição e adicionar níveis a habilidades externas. No entanto, você pode adicionar domínios, medalhas e editar créditos.

### Habilidades e créditos padrão do curso

Depois de importar habilidades, elas são adicionadas aos recursos de aprendizado importados da origem selecionada como origem da habilidade. Por exemplo, se a sua fonte de habilidades foi o LinkedIn Learning, todos os recursos de aprendizado importados do LinkedIn Learning terão as habilidades fornecidas por ele. Quando importado para recursos de aprendizado, cada recurso de aprendizado fornece um padrão de 10 créditos.

#### Relatórios

A coluna **Origem** com valores - Interno, LinkedIn Learning, Go1, que indica a origem da importação da habilidade.

As habilidades recém-adicionadas estarão no topo.

Na página de configuração Curso, a coluna **Atribuído por** contém valores, Interno e Provedor de conteúdo.


## Fluxo de trabalho do administrador de integração

O administrador de integração carrega os CSVs (habilidade, nível de habilidade e curso) e migra os cursos para a conta. Por exemplo, depois que o administrador seleciona o LinkedIn Learning, ele pode agendar uma atividade em que as habilidades e os níveis são importados para o Adobe Learning Manager.

## Exportar as habilidades

Como administrador,

1. Selecione **Habilidades** no painel esquerdo.
1. Selecione a origem de qualquer habilidade. Você pode ver os cursos, as ajudas de tarefa, os alunos inscritos e os professores do curso.

### Editar uma habilidade

Selecione uma habilidade. No pop-up **Editar uma habilidade**, não é possível editar o nome e a descrição da habilidade. No entanto, você pode adicionar domínios de habilidade e uma medalha para a habilidade.
