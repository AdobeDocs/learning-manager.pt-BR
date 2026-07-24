---
description: Tudo sobre o Gradebook da perspectiva do aluno
jcr-language: en_us
title: Gradiente para alunos
source-git-commit: 0862e0d042fac74377b44c3387a72336ec625161
workflow-type: tm+mt
source-wordcount: '1391'
ht-degree: 0%

---


# Gradiente para alunos

## Iniciar um curso com livro de notas

Quando o livro de notas está habilitado e visível para um curso no Adobe Learning Manager, uma guia **Livro de notas** aparece na página de visão geral do curso. Use-a para ver sua pontuação ponderada para cada módulo, sua pontuação agregada atual e se você passou ou ainda precisa concluir mais do curso.

![](assets/image_0008.png)

## Quando o catálogo de notas estiver disponível

A guia **Gradebook** aparece ao lado de **Módulos**, **Anotações** e **Discussões** no reprodutor do curso quando o autor ou administrador habilitou a visibilidade do gradebook para o curso. Se a guia não estiver visível, o livro de notas não foi ativado para este curso ou o administrador desativou a visibilidade do aluno. As pontuações ainda podem ser gravadas e estar visíveis para o administrador.

Você pode abrir a guia **Gradebook** a qualquer momento durante a inscrição:

![](assets/image_0009.png)

* **Antes de iniciar:** após a inscrição, você verá a lista completa de módulos pontuáveis com suas porcentagens de ponderação, as marcas máximas para cada um e os critérios de aprovação definidos pelo autor. Isso mostra exatamente como o curso é classificado antes de começar.
* **Enquanto em andamento:** à medida que você conclui os módulos e as pontuações são gravadas, o catálogo de notas é atualizado para mostrar suas pontuações até agora, juntamente com os módulos que ainda não foram tentados ou que estão aguardando a correção.
* **Após a conclusão:** o gradiente mostra todas as pontuações finais do módulo, a pontuação agregada calculada do curso e um resultado de **Aprovado** no cabeçalho.

## Exibir o catálogo de notas

* Em **Meu Aprendizado**, selecione seu curso.
* Selecione a guia **Gradebook** na página do curso.

  O cabeçalho do livro de notas mostra:

  ![](assets/image_0010a.png)

* O **Critério de aprovação:** A pontuação agregada mínima e o número de módulos necessários
* O número de módulos necessários que você concluiu do total
* Sua **Pontuação agregada** atual como uma porcentagem
* Seu status atual do curso: **Não iniciado**, **Conclusão pendente**, **Aprovado** ou **Falha**

A tabela de módulos abaixo do cabeçalho mostra as seguintes colunas para cada módulo:

| **Coluna** | **O que ele mostra** |
|------------|-------------------|
| **Módulo** | O nome e o tipo do módulo |
| **Status** | Seu status de conclusão ou pontuação para este módulo (consulte a referência de status abaixo) |
| **Peso** | A porcentagem com que este módulo contribui para sua pontuação agregada |
| **Pontuação** | Sua pontuação para este módulo (por exemplo, 40/100) |
| **Contribuição** | Os pontos percentuais reais que este módulo adicionou à sua pontuação agregada até agora |

## Exibir peso do módulo na guia Módulos

Você também pode ver o peso de cada módulo na guia **Módulos** sem abrir o gradiente.

Na página do curso, selecione a guia **Módulos**.

![](assets/image_0011.png)

A guia **Módulos** exibe a porcentagem de peso de cada módulo e o número de módulos necessários para concluir o curso.

## Pontuações do módulo com várias tentativas

Se um módulo permitir várias tentativas, a pontuação mostrada no livro de notas depende de como o autor do curso o configurou:

* **Mais alto:** a melhor pontuação de qualquer tentativa é mostrada. Uma pontuação mais baixa em uma tentativa posterior não reduz sua pontuação gravada.
* **Mais Recente:** a pontuação da sua tentativa mais recente é sempre mostrada. Uma pontuação mais baixa em uma tentativa posterior substitui a anterior.

## Entenda o status do seu módulo

Cada módulo no gradiente mostra um dos seguintes status:

![](assets/image_0012.png)

| **Status** | **O que significa** |
|------------|-------------------|
| **Concluído** | Módulo concluído e pontuação registrada |
| **Em andamento** | Módulo iniciado mas ainda não concluído |
| **Não iniciado** | Módulo ainda não aberto |
| **Falha** | O módulo marcou e a pontuação não atingiu o limite de aprovação do módulo |
| **Revisão pendente** | Módulo concluído, mas aguardando uma pontuação de um professor ou administrador |
| **Sem peso** | O tipo de módulo não oferece suporte à pontuação (PDF, vídeo e semelhante); não contribui para a agregação |

## Como a pontuação agregada é calculada

Sua pontuação agregada é a soma da contribuição ponderada de cada módulo pontuado:

(Pontuação alcançada ÷ Pontuação máxima) × % de Ponderação = Contribuição do módulo

A coluna **Contribuição** no livro de notas mostra a contribuição de cada módulo para a sua agregação atual. Os módulos marcados como **Sem ponderação** são excluídos deste cálculo.

A escala de pontuação não precisa ser a mesma em todos os módulos. Um módulo teve uma pontuação de 100 e um módulo de 10, ambos contribuem corretamente. A fórmula normaliza cada um antes de aplicar a ponderação.

## Exibir e relatar pontuações na agenda

Os administradores do Adobe Learning Manager podem visualizar as pontuações ponderadas dos livros de notas de todos os alunos inscritos em um curso, analisar o desempenho individual do aluno por módulo, baixar uma transcrição do aluno filtrada e acompanhar as alterações de configuração dos livros de notas no relatório Registro de auditoria de conteúdo.

## Exibir a agenda de um curso

Quando o gradiente está habilitado para um curso, uma nova seção **Feedback N2 - Gradebook** aparece na navegação à esquerda em **Relatórios** quando você abre o curso.

* Faça logon no Adobe Learning Manager como administrador.
* Na navegação à esquerda, selecione **Cursos** e abra o curso que deseja revisar.
* Na navegação do curso, em **Relatórios**, selecione **Feedback N2 - Gradebook**. A página **Gradebook de comentários ativos** é aberta.

![](assets/image_0013.png)

Ele mostra:

1. Os critérios de aprovação para o curso (módulos mínimos necessários e pontuação agregada mínima)
2. Uma linha de filtro para exibir alunos por nível: **Aprovado**, **Falha** ou **Conclusão pendente**
3. A fórmula de pontuação agregada: Pontuação agregada = Σ (Pontuação alcançada ÷ Pontuação máxima) × Ponderação, para cada módulo
4. Uma lista de alunos mostrando a **Pontuação agregada** de cada aluno e sua pontuação para cada módulo pontuável
5. Um menu suspenso de instâncias para alternar entre as instâncias do curso quando um curso tem várias instâncias

Os alunos que ainda não tentaram nenhum módulo pontuado mostram traços nas colunas de pontuação. Os módulos que não oferecem suporte a pontuação, PDF, vídeo, áudio e semelhantes não aparecem como colunas de pontuação.

## Exibir as pontuações de um aluno individual

No **Gradebook de Comentários Ativos**, selecione o nome de um aluno.

![](assets/image_0014.png)

A exibição individual do aluno mostra:

1. O nome, email e status do aluno (**Conclusão pendente**, **Aprovada** ou **Falha**)
2. A pontuação agregada e quantos módulos obrigatórios o aluno concluiu
3. Uma tabela de módulos mostrando: nome do módulo, tipo, se ele é necessário, status, peso, pontuação obtida e contribuição para o agregado

A tabela de módulos inclui todos os módulos pontuáveis e não pontuáveis. Os módulos pontuáveis mostram sua pontuação e contribuição. Os módulos não pontuáveis mostram traços nas colunas Pontuação e Contribuição.

## Módulos de pontuação

O comportamento da pontuação para administradores e professores não foi alterado no fluxo de trabalho atual:

* Os **módulos de questionário SCORM, AICC, xAPI e nativos** são pontuados automaticamente quando o conteúdo subjacente relata uma pontuação.
* **Sessões de sala de aula, sessões de sala de aula virtual e módulos de Atividade** são pontuadas por professores ou administradores na página **Presença e Pontuação**.

## Baixar a transcrição do aluno para um curso

Você pode baixar uma transcrição do aluno filtrada para este curso diretamente da página do livro de notas de uma das duas maneiras:

* No **Gradebook de feedback ativo**, selecione **Baixar transcrição do aluno** no canto superior direito da página.
* Na home page do administrador, selecione **Relatórios** e selecione **Relatórios Personalizados**. Selecione **Transcrições do aluno** na lista de relatórios disponíveis.

Consulte Alterações de relatórios na versão para obter mais informações.

## Eventos da Trilha de auditoria de conteúdo

A trilha de auditoria de conteúdo captura dois eventos de configuração específicos do livro de notas:

| **Evento** | **Quando ele aparecer** |
|-----------|---------------------|
| **Gradebook atualizado** | Quando um autor ativa ou desativa a grade de um curso |
| **Peso Do Módulo Atualizado** | Quando um autor altera a porcentagem de ponderação de um módulo |

Consulte Alterações de relatórios na versão para obter mais informações.

Use essas entradas para rastrear quem alterou a configuração do livro de notas e quando, particularmente em ambientes em que vários autores colaboram no mesmo curso.

## Solução de problemas

**A seção Feedback N2 - Gradebook não aparece na navegação do curso**

O Gradebook deve ser ativado pelo autor do curso ao criar o curso. Confirme se o autor ativou o catálogo de notas para a criação do curso. Se o curso foi criado antes do livro de notas estar disponível, ele não pode ser adicionado retroativamente. Uma nova versão do curso é necessária.

**A pontuação agregada de um aluno é 0 apesar dos módulos concluídos**

Confirme se o curso tem pelo menos um módulo pontuável com um valor de ponderação atribuído. Se todos os módulos concluídos pelo aluno forem não pontuáveis (PDF, vídeo, áudio), nenhuma pontuação agregada será calculada. Além disso, confirme se os módulos pontuados ainda não estão no status **Revisão pendente**. Os módulos não classificados são excluídos do agregado até que um professor insira uma pontuação.

**A coluna Peso está ausente da transcrição do aluno baixada**

Essa coluna aparece somente quando o catálogo de notas está ativado e pelo menos um módulo tem um valor de ponderação salvo. Confirme se o autor ativou o livro de notas e salvou os valores de ponderação totalizando 100%.

**Um aluno concluiu todos os módulos obrigatórios, mas mostra Conclusão pendente**

Um ou mais módulos ainda podem estar aguardando uma pontuação de um professor ou administrador (**Status de revisão pendente**). O curso não pode ser concluído até que todos os módulos obrigatórios tenham uma conclusão e uma pontuação registradas. Insira a pontuação pendente de **Presença e Pontuação** para limpar o estado pendente.
