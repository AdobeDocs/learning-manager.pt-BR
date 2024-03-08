---
jcr-language: en_us
title: Importar habilidades de fontes externas
description: Importe habilidades de provedores de conteúdo, como LinkedIn e Go1, usando os respectivos conectores.  As habilidades importadas serão adicionadas às habilidades definidas pelo administrador no Learning Manager e estarão disponíveis para os autores durante o fluxo de trabalho de criação do curso.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: 3047145d9f6940c2d941fdf2c8e878369c858b0f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 1%

---

# Importar habilidades de fontes externas

Importe habilidades de provedores de conteúdo, como LinkedIn e Go1, usando os respectivos conectores. Esse aprimoramento é uma parte da meta para a capacidade do Learning Manager de se integrar a nuvens de habilidades e sistemas de gerenciamento de talentos externos. As habilidades importadas serão adicionadas às habilidades definidas pelo administrador no Learning Manager e estarão disponíveis para os autores durante o fluxo de trabalho de criação do curso. Também foram feitos aprimoramentos na funcionalidade de pesquisa de habilidades em toda a plataforma para fornecer uma melhor experiência de pesquisa quando a conta tem um grande número de habilidades.

## Configurar importação de habilidade

Siga as etapas no procedimento para ativar a importação de habilidades na conta.

1. No aplicativo de administração, selecione **Configurações** no painel esquerdo.
1. Selecionar **Geral**.
1. No menu **Importação de habilidades** , selecione **Habilitar**. Se estiver ativado, você pode escolher uma origem externa para importar **Habilidades**. As habilidades dos recursos de aprendizado existentes serão importadas para o repositório de habilidades uma vez durante a execução inicial. Para todas as importações subsequentes de recursos de aprendizado, as habilidades serão importadas para o repositório de habilidades apenas para itens recém-importados.
1. Selecione um provedor de conteúdo na lista suspensa.

Como administrador, você só pode importar uma habilidade como origem.

### Nível de habilidade padrão

O nível de habilidade padrão é um e Crédito é 10 após a migração das habilidades. Posteriormente, o administrador pode alterar o crédito.

Não é possível editar o nome da habilidade, a descrição e adicionar níveis a habilidades externas. No entanto, você pode adicionar domínios, medalhas e editar créditos.

#### Alterações de relatórios

Adicionamos uma nova coluna **Origem** com valores - Interno, LinkedIn Learning, Go1, que indica a origem da importação da habilidade.

As habilidades recém-adicionadas estarão no topo.

Na página de configuração Curso, adicionamos uma nova coluna **Atribuído por** contendo valores, Interno e Provedor de Conteúdo.


## Fluxo de trabalho do administrador de integração

O administrador de integração carrega os CSVs (habilidade, nível de habilidade e curso) e migra os cursos para a conta. Por exemplo, depois que o administrador seleciona o LinkedIn Learning, ele pode agendar uma atividade em que as habilidades e os níveis são importados para o Adobe Learning Manager.

## Exportar as habilidades

Como administrador,

1. Selecionar **Habilidades** no painel esquerdo.
1. Selecione a origem de qualquer habilidade. Você pode ver os cursos, as ajudas de tarefa, os alunos inscritos e os professores do curso.

### Editar uma habilidade

Selecione uma habilidade. No menu **Editar uma habilidade** , não é possível editar o nome e a descrição da habilidade. No entanto, você pode adicionar domínios de habilidade e uma medalha para a habilidade.
