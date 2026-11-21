---
description: Saiba como o Adobe Learning Manager marca os alunos como participantes quando assistem a uma gravação de sessão do Adobe Connect, sem atualizações manuais
jcr-language: en_us
title: Acompanhar a participação nas exibições de gravação do Adobe Connect
exl-id: f4cb951e-3cb1-4caf-b6b8-aec86b32f782
source-git-commit: 90b45cb128b74ecb33a89bf42ef4d6e960101ff0
workflow-type: tm+mt
source-wordcount: '1654'
ht-degree: 1%
---

# Acompanhar a participação nas exibições de gravação do Adobe Connect

## Visão geral

O Adobe Learning Manager pode monitorar a participação em sessões de sala de aula virtual do Adobe Connect por meio de exibições de gravação. Quando um aluno perde uma sessão ao vivo, mas assiste à gravação no Adobe Connect por tempo suficiente, o Learning Manager marca o aluno como tendo participado da sessão. O aluno conclui o módulo da sessão e pode avançar para a conclusão do objeto de aprendizado ao qual a sessão pertence.

Antes desse recurso, o Learning Manager não tinha como registrar a participação dos alunos que assistiam a uma gravação do Connect. Um aluno que perdeu uma sessão ao vivo não pôde concluí-la e um professor teve de entrar e marcar a participação manualmente. Este recurso remove essa etapa manual. O Adobe Connect informa quem observou qual gravação e por quanto tempo, e o Learning Manager compara o tempo de observação com os critérios de conclusão definidos para a conta.

Depois que o aluno atende aos critérios de conclusão da sessão gravada, os alunos são marcados no aplicativo do administrador.

A ID de e-mail do aluno deve ser a mesma no Adobe Learning Manager e no Adobe Connect, pois o Adobe Learning Manager redireciona o aluno para o Adobe Connect usando a mesma ID de e-mail.
A frequência de sincronização padrão e o intervalo mais curto que o administrador de integração pode definir são de uma hora.


## Quem faz o quê

| Função | O que eles fazem |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Aluno | Abre a gravação da sessão e a observa depois de perder a sessão ao vivo. |
| O professor | Inicia a gravação durante a sessão ao vivo, para que haja uma gravação e uma transcrição. |
| Administrador de Integração | Configura a conta do Adobe Connect que a sincronização de presença usa e define o agendamento de sincronização ou o ativa ou desativa. |
| Autor ou gerente de entrega | Agenda as sessões de sala de aula virtual e, para programas de vários dias, reutiliza uma sala persistente em vários dias. |
| Adobe Connect | Captura o e-mail de cada aluno e o tempo de observação de gravação e apresenta a lista de visualizadores de gravação por meio de uma API. |

Cada função tem uma parte separada em fazer com que a participação baseada em gravação funcione.

## Glossário

| Prazo | Significado |
|---------------------------------|--------------------------------------------------------------------------------------------------------|
| Sessão de sala de aula virtual | Uma sessão de sala de aula virtual hospedada no Adobe Connect. |
| Treinamento virtual ministrado por instrutor | Treinamento que um professor oferece por meio de sessões de sala de aula virtual. |
| Objeto de aprendizado | Um curso, por exemplo, que contém o módulo de sessão. |
| Sala persistente | Uma sala do Adobe Connect que pode ser reutilizada para várias sessões, por exemplo, no dia 1, dia 2 e dia 3. |
| Critérios para conclusão | A porcentagem de gravação que um aluno deve observar para ser marcada como concluída para o módulo. |

## Casos de uso

### Um aluno perde uma sessão ao vivo

Um aluno não pode ingressar na sessão de sala de aula virtual ao vivo. Posteriormente, o aluno abre a sessão no Learning Manager e observa a gravação. Quando o tempo de observação atende aos critérios de conclusão, o Learning Manager marca o aluno como participou e ele conclui o módulo sem pedir ajuda ao professor.

### Um aluno que observa apenas parcialmente

Um aluno abre a gravação, mas observa menos do que o compartilhamento necessário. Os critérios de conclusão não são atendidos, portanto o Learning Manager não marca o aluno como participou.

### Sessões de vários dias em uma sala persistente

Um autor ou gerente de entrega programa sessões para o dia 1, dia 2 e dia 3 na mesma sala persistente do Connect. Eles podem ver e reutilizar o nome da sala sem fazer logon na Adobe Connect.

## Principais recursos

| Recurso | O que ela faz |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Participação automática | Marca um aluno como participou de uma sessão de sala de aula virtual baseada no Connect quando o aluno assiste a gravação por tempo suficiente para atender ao limite prescrito. |
| Assistir o tempo a partir da conexão | Usa o e-mail do aluno e registra o tempo de observação capturado pelo Adobe Connect. |
| Limite de critérios de conclusão | Marca o aluno concluído para o módulo quando o tempo de observação atinge a porcentagem definida nos critérios de conclusão. |
| Somente tempo de observação real | Conta o tempo que um aluno realmente assistiu. Arrastar a barra de busca não adiciona tempo de observação. |
| Sincronização agendada | Executa um pipeline de back-end em um cronograma controlado pelo administrador de integração e pode ser ativado ou desativado. |
| Visibilidade persistente da sala | Mostra o nome da sala do Connect no nível da instância para que os autores possam reutilizar uma sala persistente em dias. |

## Como funciona o rastreamento de participação

*De um aluno que abriu a gravação para o Learning Manager que marcou o módulo como concluído.*

### Fluxo completo

1. O professor hospeda a sessão de sala de aula virtual ao vivo no Adobe Connect e inicia a gravação. A gravação e a transcrição ficam disponíveis após a sessão.

1. Um aluno que perdeu a sessão seleciona a gravação para visualizá-la. O Adobe Connect controla a exibição automaticamente.

1. O Adobe Connect captura o e-mail do aluno e o tempo que ele realmente passou assistindo.

1. No agendamento configurado, um pipeline SnapLogic de back-end chama a API do Adobe Connect e obtém a lista de visualizadores de gravação para um determinado quadro de tempo. O pipeline usa a conta do Adobe Connect configurada no administrador de integração.

1. O Learning Manager mapeia cada visualizador para o curso e o módulo correspondentes.

1. O Learning Manager compara o tempo total de observação do aluno com os critérios de conclusão.

1. Se o tempo de observação atender aos critérios, o Learning Manager marcará o aluno como concluído para o módulo. No back-end, o Learning Manager registra isso preenchendo o CSV do curso do usuário.

>[!NOTE]
>
>O Adobe Connect não envia dados ao Learning Manager. O Learning Manager o coloca no nível da instância do Adobe Connect; por exemplo, “esses cinco usuários assistiram a essas seis gravações nas últimas 24 horas”. Portanto, a participação é atualizada após a próxima execução do pipeline, não no momento em que o aluno termina de assistir.

### Critérios de conclusão e tempo de observação

O aluno deve observar pelo menos a porcentagem de gravação definida pelos critérios de conclusão. Lembre-se destas regras:

* A porcentagem se aplica à duração da gravação, não à duração da sessão agendada. Se uma sessão de 15 minutos for gravada por apenas 5 minutos, o tempo necessário será baseado nos 5 minutos. O Adobe Connect fornece a duração da gravação.

* A porcentagem é definida no Learning Manager. É uma configuração comum em toda a conta, não uma configuração para cada instância. O mesmo tipo de configuração já aplicado a sessões ao vivo, por exemplo, exigindo 80% de participação.

* O Adobe Connect registra quanto tempo o aluno realmente assistiu. Pular com a barra de busca não conta e o Learning Manager processa o tempo de observação que o Connect passa.

| Critérios para conclusão | Duração da gravação | Tempo de observação necessário | Resultado |
|-------------------------|------------------------------------|-----------------------|-------------------------------------------------------------|
| 50% | 5 minutos | 2,5 minutos | Marcado como concluído depois que 2,5 minutos forem observados. |
| 50% | 5 minutos (a sessão durava 15 minutos) | 2,5 minutos | Baseado na gravação de 5 minutos, não na sessão de 15 minutos. |
| 0% | Qualquer | Nenhum além da abertura | Abrir a gravação é suficiente. |

### Janela Elegibilidade

O Learning Manager aplica participação baseada em gravação somente até a data de conclusão do objeto de aprendizado. Se o objeto de aprendizado não tiver data de conclusão, o Learning Manager usará a data de conclusão do objeto de aprendizado pai.

### Agendar a sincronização

O administrador de integração controla a frequência de execução do pipeline. O agendamento pode ser de hora em hora ou semanal, entre outros intervalos, e o administrador de integração pode ativá-lo ou desativá-lo. A mesma conta da Adobe Connect é usada para cada execução.

### O que muda

* Quando um usuário adiciona a sala persistente criada para o dia 1, o Learning Manager fornece acesso a essa sala. Eles podem, então, adicionar a mesma sala às sessões em outros dias.
* O Learning Manager mostra o nome da sala do Connect no nível da instância, nos detalhes da sessão ao lado do **URL da sala de aula virtual**.
* Para a instância padrão, o Learning Manager mostra a sala configurada durante a criação do curso.

### Limitações e considerações

* A participação não é em tempo real, pois o Learning Manager extrai dados em um agendamento.
* O recurso aborda somente sessões de sala de aula virtual baseada em conexão.
* Uma gravação deve existir, portanto, o professor deve iniciá-la durante a sessão ao vivo.
* Os alunos são correspondidos pelo endereço de e-mail que o Adobe Connect captura.
* Arrastar a barra de busca não adiciona tempo de observação.
* A participação baseada em gravação é interrompida na data de conclusão do objeto de aprendizado ou do objeto de aprendizado pai.

### Pontos a serem lembrados

* O tempo de observação deve ser maior ou igual à porcentagem prescrita (por exemplo, 50% de 5 minutos é 2,5 minutos). O tempo de observação não é somado se o aluno assistir repetidamente à sessão, mas ainda estiver aquém do tempo de observação prescrito. No entanto, o tempo de observação é adicionado mesmo se o aluno observar a sessão em diferentes pontos do tempo em partes e atender aos critérios de limite. Por exemplo, se um aluno assistir a um minuto da sessão no dia 1 e, em seguida, assistir a outros 1,5 minuto da sessão no dia seguinte a partir do ponto em que ele saiu, o tempo de observação será adicionado. Isso acontece no Adobe Connect.

* Os critérios de conclusão podem ser configurados no nível do curso e da conta. O efeito é o mesmo da participação da sessão ao vivo.

* A frequência de sincronização padrão e o intervalo mais curto que o administrador de integração pode definir são de uma hora.

* A ID de e-mail do aluno deve ser a mesma no Adobe Learning Manager e no Adobe Connect, pois o Adobe Learning Manager redireciona o aluno para o Adobe Connect usando a mesma ID de e-mail.

### Perguntas frequentes

**P. O aluno precisa participar da sessão ao vivo?**
**A.** Não. Um aluno que perde a sessão ao vivo ainda pode ser marcado como frequentado assistindo à gravação por tempo suficiente.

**P. Quanto da gravação o aluno deve assistir?**
**A.** A porcentagem nos critérios de conclusão, aplicada à duração da gravação. Por exemplo, a 50%, uma gravação de 5 minutos precisa de pelo menos 2,5 minutos de tempo de observação.

**P. Ignorar na contagem de gravação?**
**A.** Não. O Adobe Connect registra o tempo que o aluno assistiu de fato, portanto, arrastar a barra de busca não conta.

**P. A participação é marcada assim que o aluno termina de assistir?**
**A.** Não. O Learning Manager extrai os dados do visualizador do Adobe Connect conforme um agendamento, portanto, a participação é atualizada após a próxima execução do pipeline.

**P. O Adobe Connect envia os dados para o Learning Manager?**
**A.** Não. O Learning Manager o extrai. É um mecanismo de pull no nível da instância do Adobe Connect, não um push.

**P. Como o Learning Manager sabe qual aluno assistiu?**
**A.** O Adobe Connect captura o email do aluno e o tempo de observação da gravação. O Learning Manager mapeia isso para o curso e o módulo.

**P. Quem controla com que frequência a sincronização é executada?**
**A.** O administrador de integração define o agendamento e pode ativá-lo ou desativá-lo.

**P. A porcentagem de conclusão é definida para cada instância?**
**A.** Não. É uma configuração comum em toda a conta.

**P. As sessões de vários dias podem compartilhar uma sala do Connect?**
**A.** Sim. Os autores podem reutilizar a sala persistente criada para o dia 1 nas sessões para outros dias, e o nome da sala aparece no nível da instância no Learning Manager.
