---
title: Novidades desta versão
description: Saiba mais sobre os novos recursos e aprimoramentos na versão de novembro de 2023 do Adobe Learning Manager.
exl-id: d670dc47-d57f-464a-bee8-064cc16e59f9
source-git-commit: a655c86ab14f23fc9954229244d94a79d3188642
workflow-type: tm+mt
source-wordcount: '2370'
ht-degree: 70%

---

# Novidades desta versão

## Interface do usuário reformulada

A interface de usuário do Adobe Learning Manager passou por algumas atualizações para oferecer uma experiência mais limpa e moderna. As páginas de destino para as funções de administrador e autor foram renovadas e as atualizações de tema da interface do usuário foram feitas para todas as funções. No entanto, não foram feitas alterações no local de menus, botões ou links, e você poderá encontrá-los exatamente onde estavam localizados antes.

As atualizações do tema serão aplicadas automaticamente a contas que usam o tema padrão. As atualizações do tema da interface do usuário não afetarão as contas que fizeram modificações para usar um tema personalizado. Essas contas precisam voltar para o tema padrão para obter as atualizações do novo tema.

![Imagem da interface do usuário](assets/refreshed-ui.png)

### Sobre esta alteração

**O que muda nesta versão?**

Há um novo modelo no cabeçalho que redimensiona automaticamente o logotipo para um tamanho e posição fixos, mantendo a proporção do logotipo. A alteração pretende melhorar o apelo visual da experiência do aluno.

O nome da organização no cabeçalho também é redimensionado automaticamente para 336 (mínimo) x 680 (máximo) px para os alunos.

**Qual é o tamanho recomendado do logotipo?**

A largura máxima do logotipo é 210 px. Os logotipos com largura superior a 210 px ou altura superior a 42 px são redimensionados para 42 x 210 px.

Se o tamanho do logotipo for menor que o recomendado, ele será carregado sem qualquer alteração e terá o alinhamento centralizado.

**Qual é o impacto?**

Nomes de empresas que forem mais longos serão cortados, e um reticências preencherá o espaço.

**O que recomendamos?**

* Redimensione a imagem mantendo a proporção intacta. O tamanho máximo recomendado do logotipo é 42 px (vertical) x 210 px (horizontal).
* Para muitas contas, isso seria aplicado automaticamente; nenhuma alteração é necessária.

## Extensibilidade nativa

Configure experiências personalizadas dentro da versão nativa do Adobe Learning Manager, permitindo que você não use headless para casos menos complicados. Você também pode criar aplicativos personalizados e colocá-los em vários pontos na versão nativa dos fluxos de trabalho do aluno, gerente, administrador, autor ou professor.

Um aluno pode usar um aplicativo personalizado ou uma extensão que um administrador criou.

Consulte [Extensão nativa](/help/migrated/administrators/feature-summary/native-extensibility.md) para saber mais.

## Ferramenta de criação de quiz

Agora você pode criar avaliações no Learning Manager com a nova ferramenta de criação de quiz na página Biblioteca de conteúdo. As avaliações criadas se tornam parte da biblioteca de conteúdo e podem ser adicionadas a uma pasta “pública” para fins de reutilização do curso.

Exiba [Criar um quiz](/help/migrated/authors/feature-summary/content-library.md) para saber mais.

## Alterações de relatórios nesta versão

### Alterações no relatório de inscrição de ajuda de tarefa

Nas versões anteriores do Adobe Learning Manager, o relatório de inscrição de ajuda de tarefa não tinha filtros. O Adobe Learning Manager baixou todos os dados de uma conta.

Nesta versão, adicionamos um menu suspenso na caixa de diálogo Relatório de ajudas de tarefa.

### Alterações no relatório de anúncio de notificações

Em versões anteriores do Adobe Learning Manager, o relatório de Aviso de Notificação não tinha nenhum filtro. O Adobe Learning Manager baixou todas as notificações na conta.

Nesta versão, adicionamos um filtro de data, com o qual você pode baixar as notificações em um período especificado.  No entanto, você só pode baixar o relatório nos últimos seis meses.

### Alterações nos dados de revisão do curso no relatório de inscrição

Nesta versão, você pode baixar as informações de revisão do curso em um relatório de inscrição especificando um horário. O período de download será limitado a seis meses para contas com mais de cinco milhões de inscrições. Para todas as outras contas, o período será de 15 meses.

Você pode baixar o relatório de **[!UICONTROL Relatórios]** > **[!UICONTROL Relatórios personalizados]** > **[!UICONTROL Relatórios de histórico]** > **[!UICONTROL Relatório de acesso ao curso]**.

### Alterações na transcrição do aluno

Nas versões anteriores do Adobe Learning Manager, se um administrador personalizado tivesse o escopo de usuário, a transcrição do aprendizado continha os usuários excluídos. Nesta versão, a transcrição do aprendizado conterá os usuários excluídos se o administrador personalizado tiver o escopo do usuário ou acesso a todos os grupos de usuários.

### Relatório de alterações na presença

O Relatório de participação na página de participação dos cursos no aplicativo do administrador e na página Alunos da sessão do aplicativo do professor costumavam ser baixados de forma síncrona. Nesta versão, o download desse relatório será feito de forma assíncrona por meio de uma notificação.

Para obter mais informações sobre relatórios, consulte [Relatórios](/help/migrated/administrators/feature-summary/reports.md) no Adobe Learning Manager.

## Desativação do Marketplace de Conteúdo

Os cursos que expiraram no catálogo do marketplace de conteúdo importado (treinamento corporativo) serão excluídos automaticamente assim que expirarem. Os cursos serão definidos para serem desativados quando o conteúdo for marcado para desativação. Os alunos inscritos existentes podem consumi-los em um período limitado, após o qual serão excluídos. Isso manterá o catálogo limpo e não mostrará aos usuários nenhum curso expirado.

## Novas recomendações com base em habilidades

O Adobe Learning Manager aprimora as recomendações para contas habilitadas para clientes e parceiros. Essa melhoria no algoritmo de recomendação com a alteração no algoritmo de classificação para curso, caminho de aprendizado e certificação fornece uma melhor experiência do usuário na detecção de conteúdo.

O algoritmo não permitirá mais recomendações baseadas em pares. A alteração não afetará os usuários existentes, mas a opção Alinhado ao setor continuará existindo. Para a opção Personalizada, o Adobe Learning Manager não permitirá mais a seleção personalizada baseada em pares.

O grupo de colegas agora se torna uma conta e os alunos verão uma sequência de caracteres que mostra os tópicos em tendência no grupo. Todas as recomendações são explicáveis. Por exemplo, se você estiver visualizando algo em um assunto, o cartão na faixa exibirá o motivo do curso.

## Aprimoramentos no fluxo de trabalho do administrador personalizado

Os administradores personalizados agora terão mais paridade com as funções de administrador em relação ao acesso aos relatórios. Os administradores poderão configurar o acesso aos relatórios com melhor controle.

No Adobe Learning Manager, somente a transcrição de aprendizado e a transcrição de gamificação estão disponíveis para um administrador personalizado. Nesta versão, um administrador personalizado pode acessar todos os relatórios personalizados, exceto relatórios de xAPI e de e-mail, que ainda estão disponíveis somente para o administrador. O acesso a todos os relatórios está sujeito ao catálogo e ao escopo do usuário que o administrador personalizado tem. Há poucos relatórios que estão disponíveis apenas com escopo completo. São eles:

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Relatório</b></p></td>
   <td>
    <p style="text-align: left;"><b>Disponível</b></p></td>
   <td>
    <p style="text-align: left;"><b>Escopo</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Registro de auditoria do conteúdo</p></td>
   <td>
    <p>Sim</p></td>
   <td>
    <p>Catálogo completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Registro de auditoria do usuário</p></td>
   <td>
    <p>Sim</p></td>
   <td>
    <p>Usuário completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Acesso de login</p></td>
   <td>
    <p>Sim</p></td>
   <td>
    <p>Usuário completo</p></td>
  </tr>
    </tbody>
</table>

**Novos controles somente leitura**

Na página Funções personalizadas, adicionamos as seguintes opções Somente leitura para permitir que os administradores forneçam opções mais flexíveis ao Administrador personalizado: O administrador personalizado agora terá permissão Somente leitura adicional para Usuários, Modelos de email e Planos de aprendizado.

**Usuários**:

Se você selecionar Somente leitura, o administrador personalizado poderá exibir todos os usuários, mas não poderá editar os dados do usuário, e criar um portal de autoinscrição para os usuários.

**Planos de aprendizado**:

Se você selecionar Somente leitura, um administrador personalizado não poderá adicionar ou editar um plano de aprendizado. Eles podem baixar um relatório do plano de aprendizado e visualizar seus detalhes. Mas eles não podem alterar os detalhes do curso.

>[!NOTE]
>
>Os planos de aprendizado serão adicionais somente leitura junto com controle total.

**Modelos de Email**

Se você selecionar Somente leitura, um administrador personalizado poderá exibir os modelos de e-mail. Eles não podem ativar ou desativar as configurações de modelo de e-mail, mas podem baixar relatórios de acesso a e-mail.

### Transcrições do aluno

Se a permissão Usuário ou Todo o grupo de usuários estiver selecionada, e o administrador personalizado tentar baixar as transcrições do aluno, a opção Incluir aluno excluído retornará todos os alunos excluídos no relatório.

### Relatórios

Um administrador personalizado pode acessar os seguintes relatórios de acordo com o escopo definido:

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Relatório</b></p></td>
   <td>
    <p style="text-align: left;"><b>Disponível</b></p></td>
   <td>
    <p style="text-align: left;"><b>Escopo</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Registro de auditoria do conteúdo</p></td>
   <td>
    <p>Sim</p></td>
   <td>
    <p>Catálogo completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Registro de auditoria do usuário</p></td>
   <td>
    <p>Sim</p></td>
   <td>
    <p>Usuário completo</p></td>
  </tr>
  <tr>
   <td>
    <p>Acesso de login</p></td>
   <td>
    <p>Sim</p></td>
   <td>
    <p>Usuário completo</p></td>
  </tr>
    </tbody>
</table>

<!--| Report | Available | Scope |
|--- |--- |
| Content Audit Trail | Yes | Full Catalog |
| User Audit Trail | Yes | Full User |
|Login Access | Yes | Full User |-->

## Integração de conexão aprimorada

Os professores podem personalizar sua experiência de sessão selecionando salas específicas do professor. Nesta versão, fizemos os seguintes aprimoramentos:

### Importar transcrições

Você poderá importar transcrições de sessão do Connect e analisar as transcrições. Os alunos receberão a transcrição após a gravação, que pode ser baixada posteriormente.

### Editar vídeos

Os professores podem editar o vídeo e aprimorar a experiência de visualização dos alunos. Os professores verão um link na página de visão geral da sessão para levá-los à página de logon da Adobe Connect. Depois de fazer logon, o professor verá o link de gravação. Clicar no link os redirecionará para o vídeo, que pode ser cortado.

## Restringir relatórios do painel a usuários com função de gerente

Os administradores só podem pesquisar gerentes em relatórios do Painel.

## Limitar processamento de relatório do painel legado

Quando um administrador tenta plotar um relatório do painel de controle e o relatório leva muito tempo para plotar (mais de 2,5 min), o Adobe Learning Manager exibe a seguinte mensagem:

![imagem de relatório herdada](assets/error-message.png)
*Mensagem de erro quando o relatório demora muito*

Relatórios dessa magnitude não podem ser exibidos na interface do usuário, mas o administrador pode baixá-los.

## Suporte de migração para etiquetas de catálogo

O fluxo de trabalho de migração agora oferece suporte a etiquetas de catálogo. Os CSVs de migração podem ser usados para importar chaves de etiqueta de catálogo e valores de etiqueta de catálogo e anexá-las a cursos, programações de aprendizado, certificações e ajudas de tarefa. O fluxo de trabalho também pode ser usado para excluir valores e chaves incorretos, se necessário.

## Aprimoramentos da API para filtragem de curso complexo

A filtragem avançada de cursos por tags e etiquetas de catálogo (usando uma combinação das condições “AND” e “OR”) agora será possível por meio das APIs do Learning Manager.

## Alterações da API nesta versão

### Validação na API de trabalho

Nesta versão, se o relatório de ajuda de tarefa exceder 10 milhões gerados usando a API de tarefa, a resposta terá a mensagem: “O relatório solicitado tem muitos dados para ser gerado; considere aplicar filtros de ajuda de tarefa!”.

### Notificação de uma publicação excluída

Nas versões anteriores do Adobe Learning Manager, se qualquer curso, certificação ou plano de aprendizado fosse excluído e sua notificação estivesse presente, você ainda podia acessar o curso, certificação ou plano de aprendizado visitando sua notificação.

Nesta versão, garantiremos que uma postagem excluída não esteja mais acessível. Se você especificar a ID na API /posts/{id} e a ID da publicação não estiver mais disponível, a API exibirá a mensagem “Publicação não encontrada para o recurso especificado”.

### Prazo de conclusão da API do aluno

Nas versões anteriores, o Adobe Learning Manager buscava o prazo na tabela de inscrição. Nesta versão, o Adobe Learning Manager calculará o prazo a partir da tabela de instâncias do curso. Se o prazo não estiver disponível, ele retornará à tabela de inscrição.

### Sinalizador de substituição

Na versão de novembro de 2023 do Adobe Learning Manager, estamos descontinuando o sinalizador de substituição das APIs. O sinalizador de substituição não faz parte da especificação da API pública e destina-se a testes de back-end. O sinalizador foi descontinuado para APIs do aluno. No entanto, o sinalizador ainda é válido para APIs de administrador.

O motivo pelo qual estamos descontinuando o sinalizador para as APIs do aluno é porque o sinalizador de substituição estava buscando uma grande quantidade de dados por meio das APIs do aluno.

No futuro, a seguinte API do aluno deixará de funcionar porque tem o sinalizador de substituição.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Destacar resultados

Na próxima versão do Adobe Learning Manager, por exemplo, na API /search, estamos alterando o padrão de highlightResults para false.

Além disso, alteraremos o padrão de snippetTypes para courseName. Isso destacará apenas os nomes dos cursos na pesquisa se highlightResults for True.

### Novo tipo de recurso para o quiz

O ponto de extremidade `instances.loResources.resources` retornará `ResourceContentType` com o Quiz.

## Aviso de descontinuação

Em 30 de novembro de 2023, o LinkedIn Learning descontinuará o uso do método HTTP GET para obter um token OAuth. Após a substituição, você só poderá gerar um token OAuth usando o método POST HTTP.
O Adobe Learning Manager descontinuará o BlueJeans em fevereiro de 2024. Todas as novas contas após fevereiro de 2024 não incluirão o conector do BlueJeans.

## Notas de versão

Para obter informações sobre as versões atuais e anteriores do aplicativo Web e do aplicativo de dispositivo do Learning Manager, consulte as [Notas da versão](release-note/release-notes.md).

## Erros corrigidos nesta versão

* Uma miniatura de um curso, que é um pré-requisito para um caminho de aprendizado ou outro curso, não é exibida quando um aluno abre a página de visualização do caminho de aprendizado ou do curso.
* Se as opções Calendário, Gamificação e Aprendizado social não estiverem selecionadas, a configuração do painel do aluno não manterá a próxima configuração. As opções Recomendado nas áreas de interesse e Procurar por catálogo não são exibidas conforme selecionadas, mas aparecem na visualização.
* Mesmo depois que um aluno conclui um curso de sala de aula virtual, ele recebe um e-mail de lembrete para concluir o curso.
* Para contas entre parceiros, você não pode baixar relatórios do painel.
* Excluir e adicionar um módulo de lista de verificação em um curso produz um erro interno.
* No caso dos modelos de Convite de sessão, a ID de e-mail do remetente tem o texto captivatePrime em vez de AdobeLearningManager.
* Quando você usa a eficácia do curso como eixo Y secundário, o download do relatório falha com uma exceção de ponteiro nulo.
* Se um aluno tiver uma função de administrador personalizada atribuída, ele navegará para o perfil de administrador personalizado por padrão. No entanto, quando um URL de redirecionamento do aluno é definido na conta, o administrador personalizado é direcionado para um destino diferente, não para o perfil de Função de administrador personalizada.
* O escopo de gamificação não funcionará conforme o esperado se disabled_sub_groups for definido como um número grande.
* Em alguns casos, os usuários excluídos acionam uma migração.
* Um aluno não pode reproduzir cursos do LinkedIn no aplicativo MS Teams.
* A API de inscrição não retorna as inscrições em um plano de aprendizado do Flex ou plano de aprendizado incorporado como esperado.
* No aplicativo para dispositivos móveis, os nomes de um curso, certificação ou plano de aprendizado aparecem em minúsculas.
* Nas versões anteriores do Adobe Learning Manager, se qualquer curso, certificação ou plano de aprendizado fosse excluído e sua notificação estivesse presente, você ainda podia acessar o curso, certificação ou plano de aprendizado visitando sua notificação. Nesta versão, garantiremos que uma postagem excluída não esteja mais acessível. Se você especificar a ID na API /posts/{id} e a ID da publicação não estiver mais disponível, a API exibirá a mensagem “Publicação não encontrada para o recurso especificado”.
* Na API do aluno, o campo de prazo de conclusão não é exibido na resposta da API de inscrição.
* Na API Obter inscrição para alunos, os detalhes da inscrição aparecem mesmo depois que você especifica uma ID de instância incorreta.

## Problemas conhecidos nesta versão

* Uma nova inscrição ou atualização de uma inscrição falha quando um plano de aprendizado do Flex está em outro plano de aprendizado do Flex.
* O URL de transcrição não exibe as gravações de sessão nas sessões do Adobe Connect.
* Um aluno pode fazer um quiz offline no aplicativo móvel mesmo que ele falhe.

## Requisitos do sistema

[Requisitos de sistema do Learning Manager](system-requirements.md)

## Versões anteriores do Adobe Learning Manager

* [Versão de julho de 2023](whats-new-2023-july.md)
* [Versão de abril de 2023](whats-new-2023-april.md)
