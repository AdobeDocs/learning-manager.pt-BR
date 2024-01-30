---
jcr-language: en_us
title: Descontinuações de API no Adobe Learning Manager
description: À medida que as APIs no Adobe Learning Manager evoluem, elas são periodicamente reorganizadas ou atualizadas. Quando as APIs evoluem, a API antiga é descontinuada e eventualmente removida. Esta página contém informações que você precisa saber ao migrar de versões de API obsoletas para versões de API mais novas e estáveis.
contentowner: saghosh
source-git-commit: 83fdd06aed823a50458d50c8ac240d56af873a6d
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 19%

---


# Descontinuações de API no Adobe Learning Manager

## Descontinuações de API na versão de março de 2024 do Adobe Learning Manager

### Alterações nos Limites de Taxa

Na próxima versão do Adobe Learning Manager, estamos reestruturando os limites da taxa da API para novas contas. Para contas existentes, somente as APIs do administrador terão taxa limitada. Após 90 dias (cerca de 3 meses), reestruturaremos os limites de taxa para todas as APIs, mas as contas existentes serão incluídas na lista de permissões de acordo com o uso atual. As contas existentes precisam revisar o uso da API do aluno.

Para novas contas, se elas quiserem aumentar os limites da taxa, deverão entrar em contato com a equipe de Sucesso do cliente do ALM.

#### Quais APIs terão taxa limitada

Para novas contas, todas as APIs de administrador, aluno e pesquisa terão limites de taxa e serão ativadas.

A taxa de intermitência de API ou o limite de intermitência se refere ao número máximo de solicitações permitidas a serem feitas a uma API em uma intermitência curta dentro de um período limitado.

A tabela a seguir lista os limites de taxa e intermitência para as APIs.

<table>
    <tr>
        <th>API</th>
        <th>Número de solicitações-RPM</th>
        <th>Número de solicitações-Intermitência</th>
    </tr>
    <tr>
        <td>Administrador</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Aluno</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Pesquisa</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>

### Alterações nos limites de deslocamento

Devido ao alto número de registros recuperados pelo valor de deslocamento e à redução do desempenho geral, estamos aplicando um limite de **500** registros. Na próxima versão, para Administrador e Aluno, o **Usuários do GET** A API retornará um máximo de **500** registros.

Se precisar buscar mais registros, use o **GET** API.

A alteração nos limites de compensação se aplica a todos os novos clientes. Para clientes existentes, a regra de 90 dias se aplica.

### Excluir caminhos

No momento, as APIs do Learning Manager seguem uma estrutura de dados de gráfico, que permite buscar dados atravessando o modelo de API por meio de inclusões. Mesmo que você pudesse atravessar uma API de até sete níveis, buscar os dados usando uma única chamada de API é computacionalmente caro.

Recomendamos que todos os clientes novos e existentes façam chamadas pequenas várias vezes em vez de uma chamada grande. Essa abordagem evitará que dados indesejados sejam carregados na chamada.

Queremos aplicar essas restrições em novas contas e manter uma lista branca das contas existentes.

#### Quais caminhos estão obsoletos

Os caminhos a seguir estão obsoletos:

* /learningObjects
   * Caminhos obsoletos:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Novos caminhos:
      * enrollment.loInstance.loResources
      * instances.loResources

* /learningObjects/{id}
   * Caminho preterido:
      * enrollment.instances.subLoInstances.learningObject
   * Novo caminho:
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

### Alterações na contagem resumida de instâncias

Atualmente, no ponto de extremidade de resumo do OA, você busca o número de todas as instâncias possíveis. Por exemplo, para um curso, você pode exibir o número de inscrições e listas de espera na resposta para **GET /learningObjects/{loId}/instâncias/{loInstanceId}/summary**. Você pode, então, visualizar completionCount e enrollmentCount na resposta. Se o curso for uma sala de aula virtual ou sala de aula, você também pode ver o limite de vagas e o limite da lista de espera.

O processo de recuperação das contagens de conclusão e inscrição é computacionalmente caro, portanto, o cálculo é feito com base em solicitação. Se os dados não estiverem presentes no cache, eles serão recarregados, o que exige muitos cálculos. Se houver muitos usuários se inscrevendo em um curso, a contagem será grande e afetará efetivamente o desempenho da CPU.

Na próxima versão do Adobe Learning Manager, no ponto de extremidade de resumo da Instância do LO, completionCount, enrollmentCount, seatLimit e waitlistCount são armazenados em cache. As informações armazenadas em cache persistem até que haja alterações nas inscrições ou cancelamentos de inscrição. Para contagens superiores a 1000 inscrições, assumiremos as contagens estimadas e invalidaremos os resultados de todas as contas novas e existentes.

>[!NOTE]
>
>Para contagens, como completionCount, enrollmentCount, seatLimit e waitlistCount excedendo 1000, é recomendável interpretá-las como estimativas em vez de números precisos, pois elas serão recuperadas do cache.

### Classificar por nome

Na próxima versão do Adobe Learning Manager, nome e -name são descontinuados no campo de classificação das seguintes APIs:

* GET /userGroups/{userGroupId}/users
* GET /users

>[!NOTE]
>
>Para todas as contas novas e existentes, a classificação por nome e -name será descontinuada.


## Descontinuações da API na versão de novembro de 2023 do Adobe Learning Manager

### Sinalizador de substituição

Na versão de novembro de 2023 do Adobe Learning Manager, descontinuamos o sinalizador de substituição das APIs. O sinalizador de substituição não faz parte da especificação da API pública e destina-se a testes de back-end. O sinalizador foi descontinuado para APIs do aluno. No entanto, o sinalizador ainda é válido para APIs de administrador.

O motivo pelo qual estamos descontinuando o sinalizador para as APIs do aluno é porque o sinalizador de substituição estava buscando uma grande quantidade de dados por meio das APIs do aluno.

No futuro, a seguinte API do aluno deixará de funcionar porque tem o sinalizador de substituição.

<code>https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&amp;página[limite]=10&amp;sort=id&amp;override=TRUE</code>

### Alterações de API para novas recomendações baseadas em habilidade

O Adobe Learning Manager aprimora as recomendações para contas habilitadas para clientes e parceiros. Essa melhoria no algoritmo de recomendação com a alteração no algoritmo de classificação para curso, caminho de aprendizado e certificação fornece uma melhor experiência do usuário na detecção de conteúdo.

O algoritmo não permitirá mais recomendações baseadas em pares. A alteração não afetará os usuários existentes, mas a opção Alinhado ao setor continuará existindo. Para a opção Personalizada, o Adobe Learning Manager não permitirá mais a seleção personalizada baseada em pares.

O grupo de colegas agora se torna uma conta e os alunos verão uma sequência de caracteres que mostra os tópicos em tendência no grupo. Todas as recomendações são explicáveis. Por exemplo, se você estiver visualizando algo em um assunto, o cartão na faixa exibirá o motivo do curso.

### Alterações No Relatório De Anúncio De Notificações

Nas versões anteriores do Adobe Learning Manager, o relatório de Aviso de Notificação não tinha nenhum filtro. O Adobe Learning Manager baixou todas as notificações na conta.

Na versão de novembro de 2023, adicionamos um filtro de data, com o qual você pode baixar as notificações dentro de um período especificado.  No entanto, você só pode baixar o relatório nos últimos seis meses.