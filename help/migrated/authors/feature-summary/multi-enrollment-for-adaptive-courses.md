---
description: Saiba como ativar a inscrição múltipla para cursos adaptáveis, gerenciar limites de vagas e listas de espera e entender as regras de inscrição em caminhos de aprendizado
jcr-language: en_us
title: Várias inscrições para cursos adaptáveis
exl-id: e2a52964-fe9d-4a71-a020-68201f75f9f0
hide: true
source-git-commit: e056f1a655efd7c999856e2b54b28e676e67afc6
workflow-type: tm+mt
source-wordcount: '1231'
ht-degree: 0%
---

# Várias inscrições para cursos adaptáveis

## Visão geral

A inscrição múltipla permite que um aluno se inscreva em mais de uma instância do mesmo curso ao mesmo tempo. No Adobe Learning Manager, agora você pode ativar a inscrição múltipla para cursos adaptáveis.

## Sobre várias inscrições em um curso adaptável

Um curso adaptável mostra a cada aluno apenas os módulos que correspondem aos seus grupos de usuários. Com a opção de várias inscrições ativada, um aluno pode realizar várias instâncias desse curso, como sessões em diferentes meses.

Os cursos adaptativos controlam as listas de espera no nível do módulo, não no nível da instância. Um aluno pode estar em andamento em alguns módulos e em lista de espera em outros ao mesmo tempo. Por exemplo, um curso tem duas instâncias e cada instância tem um limite de vaga de uma. O primeiro aluno se inscreve nas duas instâncias e ocupa as duas vagas. Um segundo aluno que se inscreve nas duas instâncias está em lista de espera em ambas.

## Ativar várias inscrições para um curso adaptável

1. Faça logon no Adobe Learning Manager como autor.
2. Na navegação à esquerda, selecione **Cursos**. Abra um curso adaptável ou crie um.
3. Adicione os módulos. Para cada módulo de conteúdo, selecione **Adicionar regras** para definir os grupos de usuários que podem vê-lo e os grupos de usuários para os quais ele é obrigatório.
4. Selecione **Salvar**. A opção de várias inscrições ficará disponível.
5. Ative a alternância **Várias inscrições**.
6. Crie as instâncias necessárias. Para sessões de sala de aula e sala de aula virtual, defina os limites de vagas.
7. Selecione **Publish**.

Os alunos agora podem se inscrever em mais de uma instância do curso.

## Limite de vagas e comportamento da lista de espera

Os cursos adaptáveis impõem limites de vagas para cada sessão de sala de aula ou sala de aula virtual. Um aluno é inscrito imediatamente e fica em lista de espera apenas nas sessões que estão cheias. O aluno pode iniciar todos os outros módulos imediatamente.

| Condição | Resultado |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| Todas as sessões visíveis têm licenças disponíveis | O aluno está inscrito com acesso total a todos os módulos. |
| Uma ou mais sessões visíveis estão cheias | O aluno está inscrito e na lista de espera apenas nas sessões completas. |
| Você adiciona uma sessão obrigatória sem vagas a um curso com alunos inscritos | O aluno está em lista de espera na nova sessão. O progresso e o acesso existentes não são afetados. |
| Uma alteração no grupo de usuários remove uma sessão dos módulos visíveis do aluno | O Adobe Learning Manager libera a vaga imediatamente. |
| Um aluno alterna para outra instância | Os módulos concluídos permanecem concluídos. As vagas são usadas apenas para módulos visíveis que o aluno não concluiu. |

## Regras de inscrição e conclusão para programações de estudo adaptáveis

Os autores agora podem adicionar cursos adaptáveis a caminhos de aprendizado adaptáveis no Adobe Learning Manager. A inscrição, a lista de espera e a conclusão seguem regras que combinam as configurações da seção e as configurações do curso definidas pelos autores.

### Como um caminho de aprendizado adaptável avalia um aluno

O Adobe Learning Manager avalia a visibilidade no nível da seção e no nível do curso. A regra de seção decide se um aluno vê uma seção e os cursos adaptáveis nela. As regras do módulo em cada curso adaptável decidem se o aluno está inscrito no curso.

Os alunos serão inscritos automaticamente sempre que houver uma alteração do UG em relação ao curso adaptável na LP adaptável. E, ao mesmo tempo, os alunos receberão notificações de inscrição automática e e-mails.

### Regras de avaliação de inscrição

Quando você inscreve um aluno em um caminho de aprendizado adaptável, o Adobe Learning Manager verifica o caminho nesta ordem:

| Ordem | Verificar | Resultado |
|-----------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 | Visibilidade da seção | O Adobe Learning Manager verifica a inscrição de um curso apenas se a sua seção estiver visível para o aluno. |
| 2 | Qualificação do curso | Se o curso não tiver um módulo obrigatório para o aluno, ele não está inscrito no curso. O curso não conta para a conclusão do caminho de aprendizado. |
| 3 | Seções sem curso qualificado | Se uma seção contiver apenas cursos adaptáveis e o aluno não estiver qualificado para nenhum deles, o Adobe Learning Manager ignorará a seção. |
| 4 | Inscrição no Caminho de Aprendizado | Se nenhuma das seções obrigatórias se aplicar ao aluno, ele não estará inscrito no caminho de aprendizado. |

Se o aluno já estiver inscrito em uma instância do curso que pertence à instância do caminho de aprendizado, o Adobe Learning Manager usará essa inscrição.

Após a inscrição, as seguintes regras se aplicam:

* Um aluno que pulou um curso inicialmente devido à visibilidade pode ser inscrito automaticamente se o curso adaptável estiver visível devido à visibilidade/alterações de regra obrigatórias posteriormente.
* Uma alteração de grupo de usuários ou uma alteração de curso pode cancelar a inscrição de um aluno em um curso adaptável. Se nenhum conteúdo obrigatório permanecer no caminho, a inscrição do aluno será cancelada no caminho.
* Para alterações na seção, o aluno não receberá nenhuma notificação de inscrição automática ou e-mail. Quando a página é recarregada, o aluno pode ver as alterações.

### Comportamento da lista de espera em caminhos de aprendizado adaptáveis

A lista de espera funciona no nível da sessão, não no nível da instância. Isso também se aplica a cursos adaptáveis em caminhos de aprendizado.

| Cenário | Comportamento |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Nenhum curso adaptável no caminho tem um módulo de sala de aula ou sala de aula virtual | Nenhuma lista de espera se aplica. |
| Um curso adaptável tem um módulo de sala de aula ou sala de aula virtual e nenhuma instância está selecionada | O curso assume **Nenhuma instância** como padrão. O aluno pode se inscrever em qualquer instância e está na lista de espera apenas em sessões que estão cheias. |
| Uma instância é selecionada antes da inscrição | O aluno está inscrito nessa instância e está na lista de espera apenas em sessões que estão cheias. |

Para gerenciar alunos na lista de espera, abra o curso adaptável e selecione a guia **Alunos** > **Lista de espera**. Para um curso adaptável em um caminho de aprendizado flexível e um caminho de aprendizado adaptável, os alunos na lista de espera aparecem somente na guia **Lista de espera** do curso e não no caminho de aprendizado.

### Atualizar o comportamento de conclusão e reversão

O Adobe Learning Manager não revoga a conclusão automaticamente quando os grupos de usuários ou as regras são alterados. Um aluno concluído permanece concluído até que você atualize a conclusão.

* Execute **Atualizar conclusão** no caminho de aprendizado. Você não pode atualizar um curso adaptável por conta própria para os alunos que o seguem pelo caminho.

* Cada curso adaptável recalcula primeiro, com base nos módulos obrigatórios atuais do aluno. O caminho de aprendizado é recalculado com base nas seções obrigatórias atuais e nos estados do curso atualizado.

* Se o curso ou o caminho não estiver mais concluído, o status do aluno mudará para em andamento. A conclusão original permanece na transcrição do aluno como um registro histórico.

* Uma reversão de conclusão localiza os cursos adaptáveis cujos módulos foram alterados por causa de uma alteração no grupo de usuários ou de uma republicação. Isso recalcula esses cursos e depois o caminho de aprendizado. O status do trabalho mostra **Êxito** quando a reversão termina.

A lista de espera é controlada no nível do módulo. Um aluno pode ser colocado em lista de espera em uma sessão completa em mais de uma instância. Por exemplo, um curso tem duas instâncias com um limite de vagas de uma para cada. O primeiro aluno se inscreve nas duas instâncias e ocupa as duas vagas. Um segundo aluno que se inscreve em ambas as instâncias aparece na guia **Lista de espera** de cada instância.

### Atribuir vagas para alunos na lista de espera

Quando um aluno cancela a inscrição, um autor aumenta um limite de vagas ou um aluno alterna instâncias, o Adobe Learning Manager limpa a lista de espera na ordem de data de inscrição. Você também pode alocar licenças manualmente.

1. Abra o curso adaptável.
2. Selecione a guia **Alunos** > **Lista de espera**.
3. Marque a caixa de seleção ao lado de cada aluno para o qual deseja alocar vagas.
4. Selecione **Alocar Licenças**.

O Adobe Learning Manager limpa cada aluno selecionado da lista de espera em todas as sessões da lista de espera de uma vez, não apenas na sessão que você está visualizando. O sistema presume que você organizou a vaga para o aluno.
