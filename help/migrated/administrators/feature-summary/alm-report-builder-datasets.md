---
jcr-language: en_us
title: Conjuntos de dados disponíveis no Report Builder
description: Um guia de referência para os conjuntos de dados, campos e campos derivados disponíveis no Adobe Learning Manager Report Builder.
contentowner: mmanuel
source-git-commit: b21196a3121c88bf54f33aecc0f4649eceb3ddf6
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 28%

---


# Conjuntos de dados disponíveis no Report Builder

Report Builder organiza todas as colunas disponíveis em conjuntos de dados, grupos nomeados de campos relacionados. Este artigo lista cada conjunto de dados, descreve o que ele contém e observa quais conjuntos de dados podem ser combinados em um único relatório.

**Conjuntos de dados nesta versão**

**Conjunto de dados**

**O que ele contém**

**Campos de chave**

**Usuário**

Dados de perfil do aluno para alunos ativos e excluídos

Nome, email, ID de usuário, gerente, campos ativos, status

**Transcrição**

Registros de inscrição e conclusão

Data de inscrição, data de conclusão, % de progresso, status, pontuação

**Objeto de Aprendizado**

Curso, caminho de aprendizado e metadados de certificação

nome do OA, ID do OA, tipo, catálogo, rótulo do catálogo, status

**Instância do Objeto de Aprendizado**

Detalhes no nível da instância para cursos com várias instâncias

Nome da instância, ID da instância, limite de inscrição, prazo

**Catálogo**

Pares chave-valor de metadados de catálogo e etiquetas de catálogo

Nome do catálogo, ID do catálogo, chave da etiqueta, valor da etiqueta. **As colunas de Etiqueta de Catálogo estão configuradas pelo cliente**. Elas aparecem somente se sua conta tiver etiquetas de catálogo configuradas. Os nomes e valores de rótulos exibidos refletirão sua própria configuração.

**Grupo de usuários**

Associação e hierarquia de grupos de usuários

Nome do grupo de usuários, ID do grupo de usuários, grupo pai, contagem de membros

**Sessão do módulo**

Detalhes da sessão para módulos de sala de aula, sala de aula virtual e e-learning

ID da sessão, nome da sessão, nome(s) do professor, hora de início, hora de término, local

Lista de colunas em conjuntos de dados

Catálogo

* Data de criação
* ID
* Nome

Etiqueta de catálogo

* Catálogo
* ID
* Nome
* Valor

Campo personalizado (objeto de aprendizagem)

* % de conclusão do objeto de aprendizado
* % de conformidade do objeto de aprendizado

Campo personalizado (usuário)

* % de conclusão do usuário
* % de conformidade do usuário

Objeto de aprendizado

* Nomes dos autores
* Data de desativação automática
* Contagem de Conclusões
* Data de criação
* Duração (minutos)
* Número de inscrições
* Tipo de inscrição
* Formato
* ID
* Mudança de instância ativada
* Última data de conclusão
* Data da última publicação
* Vários registros habilitados
* Nome
* Pré-requisitos obrigatórios
* Preço
* Créditos da habilidade
* Nível da habilidade
* Nome da habilidade
* Média da classificação por estrelas
* Contagem da classificação por estrelas
* Contagem iniciada
* Status
* Etiquetas
* Tipo
* ID exclusivo

Instância do objeto de aprendizado

* Prazo de conclusão
* Data de criação
* Vencimento da inscrição
* ID
* Última data de conclusão
* ID do objeto de aprendizado
* Nome
* Status
* Tipo
* Vencimento do cancelamento da inscrição

Módulo

* Acessar hora de término
* Acessar hora de início
* ID do curso
* ID da instância do curso
* Duração (minutos)
* Horário de término
* Número de inscrições
* ID
* Nomes dos instrutores
* Localização
* Informações do Local
* Região do local
* URL da localização
* ID do módulo
* Nome
* Limite de vaga
* Horário de início
* Tipo
* Limite de listas de espera

Transcrição (objeto de aprendizado)

* Data de conclusão
* Prazo de conclusão
* Origem da Conclusão
* Origem da conclusão - ID do usuário
* Origem da conclusão - nome do usuário
* Data de inscrição
* Fonte da inscrição
* Estado da inscrição
* ID do objeto de aprendizado
* Nome do objeto de aprendizado
* ID da instância do objeto de aprendizado
* Em atraso
* ID do objeto de aprendizado principal
* Data da aprovação
* Porcentagem do progresso
* ID da certificação raiz
* Data de início
* Status
* Tempo gasto (minutos)
* Maior pontuação de usuário
* ID do usuário
* Pontuação mais recente do usuário

Transcrição (módulo)

* Data de conclusão
* ID do curso
* ID do módulo
* Nome do módulo
* Data da aprovação
* Porcentagem do progresso
* Pontuação total do módulo de questionário
* Data de início
* Status
* Tempo gasto (minutos)
* E-mail do usuário
* Maior pontuação de usuário
* ID do usuário
* Pontuação mais recente do usuário
* Nome do usuário

Usuário

* Adobe ID
* Idioma do Conteúdo
* Data de criação
* Data de exclusão
* Contagem de membros da equipe direta
* E-mail
* ID
* Idioma da Interface
* É administrador
* É autor
* Tem função personalizada
* É instrutor
* É administrador de integração
* É aluno
* É gerente
* É um usuário-raiz
* Data do último acesso
* E-mail do gerente
* ID do gerente
* Nome do gerente
* ID exclusiva do gerente
* Nome
* Funções
* Origem
* Status
* Contagem de membros da equipe
* Fuso Horário
* Tipo
* ID exclusivo

Grupo de usuários

* Data de criação
* ID
* Contagem de membros
* Nome
* Status

Grupo de usuários (campo ativo)

* Data de criação
* ID
* Contagem de membros
* Nome
* Status

Grupo de usuários (personalizado)

* Data de criação
* ID
* Contagem de membros
* Nome
* Status

Grupo de usuários (equipe direta)

* Data de criação
* ID
* Contagem de membros
* Nome
* E-mail do proprietário
* ID do proprietário
* Nome do proprietário
* ID único do proprietário
* Status

Grupo de usuários (integrados)

* Data de criação
* ID
* Contagem de membros
* Nome
* Status

Grupo de usuários (equipe)

* Data de criação
* ID
* Contagem de membros
* Descrição
* Nome
* E-mail do proprietário
* ID do proprietário
* Nome do proprietário
* Status do proprietário
* ID único do proprietário
* Status

**Como os conjuntos de dados se unem**

Nem todos os pares de conjuntos de dados podem ser combinados em um único relatório. Os conjuntos de dados devem compartilhar uma relação lógica no modelo de dados da Adobe Learning Manager para poderem ser unidos. Quando você adiciona sua primeira coluna, o Report Builder filtra os conjuntos de dados restantes para mostrar apenas os compatíveis. Se um conjunto de dados aparecer esmaecido, ele não poderá ser associado diretamente às colunas que você já selecionou.

Isso significa que o conjunto de dados não pode ser unido com as colunas que você já selecionou. Essa é uma restrição rígida no modelo de dados. Os dois conjuntos de dados não compartilham um caminho de associação compatível.

Um exemplo comum é o campo derivado de **Conformidade %**. Quando a Conformidade % estiver selecionada, os conjuntos de dados **Transcrição**, **Transcrição de módulo** e **Instância do LO** estarão desabilitados. A % de conformidade é calculada no nível do usuário ou do grupo de usuários em relação aos objetos de aprendizado e catálogos. Ele deve ser usado somente com colunas e filtros do **Usuário**, do **Grupo de Usuários**, do **Objeto de Aprendizado** e do **Catálogo**.

Para usar um conjunto de dados desabilitado, desmarque as colunas que estão causando o conflito e adicione o conjunto de dados necessário.

As relações de junção abaixo são extraídas do modelo de dados Report Builder. Entendê-los ajuda a planejar quais conjuntos de dados combinar antes de criar um relatório.

**Conjuntos de dados de hub**

Dois conjuntos de dados atuam como hubs centrais. A maioria dos outros conjuntos de dados se conecta através deles:

* **Registro** (conjunto de dados de registro), a tabela de fatos primária. Ele se conecta diretamente ao **Usuário** (o aluno que se inscreveu), ao **Objeto de Aprendizado** (no qual se inscreveu) e por meio do objeto de aprendizado à **Sessão de Módulo**, ao **Catálogo**, à **Etiqueta de Catálogo** e à **Instância do OA**.
* **Transcrição do módulo** (conjunto de dados moduleTranscript) — a tabela de fatos de progresso no nível do módulo. Ele se conecta ao **Usuário** e à **Sessão de Módulo**, que por sua vez se vincula ao **Objeto de Aprendizado**.

A maioria dos relatórios que combinam dados do aluno, do curso e de conclusão é criada por meio de um desses dois hubs.

**Unir caminhos por caso de uso**

**Para combinar estes conjuntos de dados**

**O caminho de ingresso**

**Usuário** + **Registro**

Inscrição → Usuário (via ID do aluno)

**Inscrição** + **Objeto de Aprendizado**

Inscrição → Objeto de aprendizado (via ID do OA)

**Objeto de Aprendizado** + **Catálogo**

Objeto de aprendizado → Catálogo do LO → Catálogo

**Objeto de Aprendizado** + **Etiqueta de Catálogo**

Objeto de aprendizado → Etiquetas de catálogo do LO

**Objeto de Aprendizado** + **Instância do OA**

Instância do LO → Objeto de aprendizado

**Sessão de Módulo** + **Objeto de Aprendizado**

Sessão do módulo → Objeto de aprendizado (via curso da sessão)

**Sessão do Módulo** + **Usuário** (professor)

Sessão do módulo → Usuário (via alias do professor FK)

**Usuário** + **Grupo de Usuários**

Associação de grupo de usuários → Usuário + Grupo de usuários

**Objeto de Aprendizado** + **Usuário** (autor)

LO Author → User (por meio do alias FK do autor)

**Usuário** + **Campos Ativos**

Campos ativos do usuário → Usuário (via ID do usuário)

**Relações com alias**

Alguns campos no modelo de dados ingressam na entidade **Usuário** por meio de uma função nomeada em vez de uma ID de aluno direta. Estas são chaves estrangeiras com alias. Eles apontam para a mesma tabela de usuários, mas representam uma função diferente:

* **Professor**: a sessão do módulo ingressa no usuário como professor da sessão
* **Autor**: autor do OA ingressa no usuário como autor do objeto de aprendizado
* **Gerente**: o usuário se une a si mesmo para representar o gerente do aluno
* **Concluído por**: cada inscrição e transcrição de módulo contém uma referência de usuário separada para “concluído por”

É por isso que um único relatório pode mostrar o nome de um aluno e o nome do professor. Ambos vêm da entidade Usuário por caminhos de join diferentes.

**Tipos de conjuntos de dados do grupo de usuários**

A categoria **Grupo de Usuários** contém várias exibições distintas de conjunto de dados, cada uma abrangendo um tipo diferente de grupo:

**Conjunto de dados**

**Tipo de grupo**

**Grupo de Usuários** (userGroup)

Todos os grupos de usuários. Usar este conjunto de dados como o grupo de usuários principal

**Grupo de usuários de campo ativo** (ative_field_user_group)

Grupos com base em valores de campo ativos (por exemplo, região, departamento)

**Grupo de usuários da equipe** (team_user_group)

Grupos baseados em hierarquia de gerentes

**Grupo de usuários personalizado** (custom_user_group)

Grupos personalizados configurados manualmente

**Grupo de usuários interno** (inbuilt_user_group)

Grupos definidos pelo sistema

Os conjuntos de dados do grupo de usuários baseado em exibição (**Campo Ativo**, **Equipe**, **Personalizado**, **Interno**) não têm relações diretas de chave estrangeira no esquema, são exibições SQL. Isso significa que eles têm restrições de junção mais livres do que o conjunto de dados **Grupo de Usuários** principal. Use o conjunto de dados **Grupo de Usuários** principal ao ingressar dados do grupo de usuários com dados de inscrição ou transcrição para obter os resultados mais confiáveis.

**Campos derivados**

Os campos derivados são colunas pré-calculadas calculadas por Report Builder. Elas são listadas separadamente das colunas padrão no seletor de colunas.

**Campo derivado**

**O que ele calcula**

**Conjuntos de dados necessários**

**Conformidade %**

Porcentagem de alunos necessários que concluíram cursos marcados como de conformidade

Grupo de usuários, Objeto de aprendizado, Transcrição

**Conclusão %**

Conclusões divididas por inscrições × 100

Transcrição ou Objeto de aprendizado

**Contagem de Usuários Inscritos**

Total de alunos inscritos em um objeto de aprendizado

Objeto de aprendizado

**Contagem de Conclusão**

Total de conclusões de um objeto de aprendizado

Objeto de aprendizado

**Iniciar Contagem**

Alunos que iniciaram, mas não concluíram

Objeto de aprendizado

**Contagem de Membros**

Número de usuários em um grupo de usuários

Grupo de usuários
