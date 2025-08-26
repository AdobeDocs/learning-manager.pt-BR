---
description: Para saber como criar cursos, certificações e programas de aprendizado no Learning Manager, leia este artigo.
jcr-language: en_us
title: Criar, modificar e publicar cursos
contentowner: manochan
exl-id: c5257796-0afa-4021-bd17-d3f1e9a86948
source-git-commit: 8b5343ae078f3d4774bbed713ad8db47e0cc0d86
workflow-type: tm+mt
source-wordcount: '7321'
ht-degree: 71%

---

# Criar, modificar e publicar cursos

Para saber como criar cursos, certificações e programas de aprendizado no Learning Manager, leia este artigo.

Os autores podem criar objetos de aprendizado, como cursos, certificações e planos de aprendizado. Os alunos podem consumir esses objetos de aprendizado, enquanto os administradores podem acompanhar o progresso dos alunos.

## Cursos no Learning Manager {#coursesincaptivateprime}

O Adobe Learning Manager permite que os autores criem cursos usando um ou mais módulos relacionados a treinamento virtual, treinamento em ritmo individualizado, treinamento em sala de aula e atividades. Os administradores podem usar esses cursos para criar instâncias de cursos, inscrever alunos, atribuir medalhas e habilitar o feedback de tais cursos. Também podem criar programas de aprendizado, planos de aprendizado e certificações usando estes cursos.

Os autores podem usar o conteúdo de aprendizado eletrônico criado usando qualquer ferramenta de eLearning. Outros formatos compatíveis de curso incluem arquivos de vídeo, PDF, doc, docx, PPT e PPTX.

## Criar um curso - Fluxo de trabalho básico {#createacoursebasicworkflow}

Para criar um curso, siga as etapas abaixo:

1. Faça logon no Adobe Learning Manager como autor porque somente os autores tem os direitos para criar cursos. Agora, na página de introdução, clique **[!UICONTROL Criar cursos]**.
1. Na página **Visão geral do curso**, insira o nome do curso. Agora, digite uma descrição breve para este curso, a qual é exibida no cartão do curso. Essa descrição não deve ter mais de 140 caracteres. Em seguida, insira a visão geral detalhada do curso, a qual é exibida na página de detalhes do curso. A descrição não deve exceder 1.500 caracteres.

   Como autor, você pode ver a descrição dos módulos enquanto adiciona o módulo a um curso.

1. Para tornar o curso disponível em outros idiomas, clique em Adicionar novo idioma no canto superior esquerdo da página. Selecione o idioma ou os idiomas nos quais você deseja disponibilizar o curso. Clique em **[!UICONTROL Salvar]**. Para obter mais informações, consulte [Adicionar conteúdo em diferentes idiomas](/help/migrated/authors/feature-summary/content-library.md).
1. **Modificar configurações do curso**-

   1. Na página Configurações do curso, escolha uma habilidade para o curso. Selecione a habilidade necessária na lista suspensa Habilidade. Em seguida, na lista suspensa Nível, selecione o nível necessário.
   1. Escolha as habilidades do curso, o nível e defina os créditos para a habilidade. Adicione mais habilidades, se necessário.
   1. Selecione o tipo de inscrição na lista suspensa **Tipo de inscrição**.

   Os tipos de inscrições são os seguintes:

   * **Indicado pelo gerente:** somente gerentes podem indicar esses cursos. Um aluno não poderá se inscrever nesses tipos de cursos.
   * **Aprovado pelo gerente:** os gerentes aprovam esses cursos. Os alunos podem se inscrever nesses cursos, mas não são inscritos diretamente nesses tipos de cursos sem a aprovação do gerente. Uma solicitação de notificação será enviada para os gerentes quando os alunos se inscreverem nesses tipos de cursos. Após a aprovação do gerente, esses cursos são listados como inscritos para os alunos.
   * **Autoinscrição:** os alunos podem se inscrever diretamente nesses tipos de cursos.

1. Para salvar as alterações, clique em **[!UICONTROL Salvar]**. Para publicar o curso, clique em **[!UICONTROL Publish]**.

## Criar um curso - Fluxo de trabalho avançado {#createacourseadvancedworkflow}

1. Faça logon no Adobe Learning Manager como autor porque somente os autores tem os direitos para criar cursos. Agora, na página de introdução, clique **[!UICONTROL Criar cursos]**.
1. Na página **Visão geral do curso**, insira o nome do curso. Agora, digite uma descrição breve para este curso, a qual é exibida no cartão do curso. Essa descrição não deve ter mais de 140 caracteres. Em seguida, insira a visão geral detalhada do curso, a qual é exibida na página de detalhes do curso. A descrição não deve exceder 1.500 caracteres.
1. Para tornar o curso disponível em outros idiomas, clique em Adicionar novo idioma no canto superior esquerdo da página. Selecione o idioma ou os idiomas nos quais você deseja disponibilizar o curso. Clique em **[!UICONTROL Salvar]**. Para obter mais informações, consulte [Adicionar conteúdo em diferentes idiomas](/help/migrated/authors/feature-summary/content-library.md).
1. **Modificar configurações do curso**-

   1. Na página Configurações do curso, escolha uma habilidade para o curso. Selecione a habilidade necessária na lista suspensa Habilidade. Em seguida, na lista suspensa Nível, selecione o nível necessário.
   1. Escolha as habilidades do curso, o nível e defina os créditos para a habilidade. Adicione mais habilidades, se necessário.
   1. Adicione os rótulos de conformidade personalizados ao curso, se necessário. Consulte [Adicionar rótulos de conformidade ao curso/caminho de aprendizado/certificação](/help/migrated/authors/feature-summary/courses.md#add-compliance-labels-to-courselearning-pathcertification).
   1. Selecione o tipo de inscrição na lista suspensa **Tipo de inscrição**.

   Os tipos de inscrições são os seguintes:

   * **Indicado pelo gerente:** somente gerentes podem indicar esses cursos. Um aluno não poderá se inscrever nesses tipos de cursos.
   * **Aprovado pelo gerente:** os gerentes aprovam esses cursos. Os alunos podem se inscrever nesses cursos, mas não são inscritos diretamente nesses tipos de cursos sem a aprovação do gerente. Uma solicitação de notificação será enviada para os gerentes quando os alunos se inscreverem nesses tipos de cursos. Após a aprovação do gerente, esses cursos são listados como inscritos para os alunos.
   * **Autoinscrição:** os alunos podem se inscrever diretamente nesses tipos de cursos.

1. Escolha se deseja definir um preço para o curso ou torná-lo gratuito. Se quiser tornar o curso pago, escolha a opção **[!UICONTROL Pago]** e especifique um preço. O preço então aparece no cartão do curso e na página de visão geral do curso de um aluno.

   OBSERVAÇÃO: isso é ativado somente quando o conector do Adobe Commerce está configurado.

1. Se quiser que o aluno consiga cancelar sua inscrição no curso, habilite a caixa de seleção **Os alunos podem cancelar suas inscrições**.

1. **Configuração da Instância**

   Se você ativar essa opção, os alunos que estão no estado Em andamento poderão visitar outras instâncias e se inscrever lá. Um aluno pode manter o progresso da instância anterior.

   Após publicar o curso, se você voltar à página Configurações, a opção não poderá mais ser editada.

   Você pode habilitar a opção para os seguintes tipos de curso:

   * Ritmo individualizado
   * Sala de aula
   * Atividade
   * Mesclado

   Observação: Ao duplicar um curso, se você tiver ativado a opção Configuração de instância no curso de origem, a opção permanecerá desativada no curso de destino.

   **Não há suporte para a Opção de Instância**:

   * Cursos pagos
   * Cursos do tipo inscrição indicados pelo gerente.

   A configuração da alternãncia de instância não será propagada para contas de colegas se compartilhada pelo catálogo. A opção permanece desativada no curso de destino.

1. **Várias inscrições**

   Usando isso, você pode inscrever alunos em mais de uma instância do curso em um ou diferentes períodos.

   Ative a alternância **Inscrição múltipla** para alternar entre várias inscrições de curso de um aluno. Se você habilitou a Opção de Instância, não poderá usar o recurso de Várias inscrições.

1. Selecione os cursos de pré-requisito que devem ser concluídos antes de realizar seu curso. Clique no campo Cursos e escolha na lista de cursos.
1. Habilite a caixa de seleção **Habilitar** **Pré-requisitos** se quiser que os cursos de pré-requisito se tornem obrigatórios.
1. Adicione palavras-chave como marcas relacionadas ao curso. Essas marcas ajudam os alunos a localizarem com facilidade o curso durante a pesquisa. Todas essas marcas são adicionadas automaticamente com base nos módulos que adicionamos. Se tiver outras marcas que deseja adicionar a este curso, você pode incorporá-las.
1. Adicione palavras-chave como marcas relacionadas ao curso. Essas marcas ajudam os alunos a localizarem com facilidade o curso durante a pesquisa. Todas essas marcas são adicionadas automaticamente com base nos módulos que adicionamos. Se tiver outras marcas que deseja adicionar a este curso, você pode incorporá-las.
1. No campo Desativação automática, selecione uma data em que o curso será desativado. O administrador deve habilitar a opção Retirada automática primeiro.
1. Para salvar as alterações, clique em **[!UICONTROL Salvar]**. Para publicar o curso, clique em **[!UICONTROL Publish]**.

### Adicionar rótulos de conformidade ao curso/caminho de aprendizado/certificação {#add-custom-compliance-label}

Para adicionar os rótulos de conformidade aos cursos, siga estas etapas:

1. No aplicativo do autor, vá para **[!UICONTROL Cursos]**/**[!UICONTROL Caminhos de aprendizado]**/**[!UICONTROL Certificações]** e selecione **[!UICONTROL Adicionar]**.
1. Digite o nome e outros detalhes, como descrição e habilidades.
1. Na caixa de texto **[!UICONTROL Conformidade personalizada]**, digite e selecione o rótulo de conformidade.

   ![](assets/add-compliance-label.png)
   _Adicionar conformidade personalizada_

   >[!IMPORTANT]
   >
   >Certifique-se de definir um prazo para o curso quando estiver adicionando a Conformidade personalizada.

   >[!NOTE]
   >
   >Um máximo de 50 cursos, programações de aprendizado ou certificações podem ter o mesmo valor para um rótulo de tipo de conformidade personalizado.

1. Salve e publique o curso/caminho de aprendizado/certificação.
Agora o curso/caminho de aprendizado/certificação é considerado como um tipo de conformidade. Os administradores podem adicionar este curso ao painel de conformidade e compartilhá-lo com os gerentes para monitorar o progresso

>[!NOTE]
>
>Os autores também podem adicionar os rótulos de conformidade a um curso/caminho de aprendizado/certificação existente editando-os.

## Pontos de gamificação

Você pode alocar pontos de gamificação nos níveis do curso e da instância do curso. Com isso, você pode conceder pontos a diferentes cursos ou instâncias. Os alunos são incentivados a fazer cursos específicos ou preferem uma instância específica do curso em vez de outras.

1. No nível da instância do curso, selecione **[!UICONTROL Pontos de gamificação]**.

![pontos de gamificação](assets/select-gamification-points-new.png)

*Definir pontos para gamificação*

1. Selecione **[!UICONTROL Editar]**.
1. Se você selecionar Usar configurações do nível do curso, as seguintes opções serão exibidas:

   * **[!UICONTROL Na conclusão]**: selecione essa opção se deseja que o aluno obtenha 100 pontos quando concluir um curso.
   * **Mais regras**

      * **[!UICONTROL Conclusão antecipada]**: se você selecionar isso, os primeiros 30 alunos receberão 100 pontos ao concluir um curso.
      * **[!UICONTROL Conclusão no prazo]**: se você selecionar isso, os alunos receberão 100 pontos se concluírem um curso dentro de 999 dias.

1. Se você selecionar **[!UICONTROL Usar configurações personalizadas]**, as seguintes opções são exibidas:

   * **[!UICONTROL Na conclusão]**: selecione essa opção se deseja que o aluno obtenha 100 pontos quando concluir um curso.
   * **Mais regras**

      * **[!UICONTROL Conclusão antecipada]**: se você selecionar essa opção, poderá determinar quantos alunos receberão os pontos especificados.
      * **[!UICONTROL Conclusão no prazo]**: se você selecionar essa opção, poderá determinar o número de pontos que os alunos serão premiados se concluírem um curso em um período especificado.

   ![pontos de gamificação](assets/gamification-custom-settings.png)

   *Definir conclusão antecipada e oportuna*

1. Selecione **[!UICONTROL Salvar]**.

## Agregar recursos de aprendizado

O autor pode decidir se deseja agregar os recursos de aprendizado no nível do Plano de aprendizado ou deixá-los permanecer no nível de um curso individual.

Como autor, selecione **[!UICONTROL Caminho de Aprendizado]** > **[!UICONTROL Configurações]**. Clique em **[!UICONTROL Editar]**.

Na seção **[!UICONTROL Recursos]**, a caixa de seleção Mostrar recursos constituintes do curso agregados no nível do Caminho de Aprendizado, quando ativada, exibe se os recursos presentes no nível do curso seriam exibidos no nível do Caminho de Aprendizado.

>[!NOTE]
>
>Na página Configurações de um caminho de aprendizado, um administrador também pode ativar essa opção, que exibe os recursos presentes no nível do curso que seriam exibidos no nível do caminho de aprendizado.

## Assistente de Agendamento

Gerencie conflitos no agendamento de professores e salas de aula. Se quiser saber em que hora e data qualquer professor está disponível antes de atribuí-lo ao curso, use o Assistente de programação.

Ao criar um curso, para um curso de VC ou CR, clique em Assistente de agendamento.

![Selecionar o Assistente de Agendamento](assets/scheduling-assistant.png)

*Iniciar assistente de agendamento*

A janela Assistente de programação é aberta.

![Tela do Assistente de Agendamento](assets/scheduling-assistant-window.png)

*A caixa de diálogo do Assistente de Agendamento*

No Assistente de Agendamento, você pode:

* Pesquisar professores por nome.
* Pesquisar professores por habilidades.

### Pesquisar professores por nome

No campo Professor, digite o nome do professor ou procure o nome parcial do professor. Uma lista de professores é exibida, na qual você pode escolher um professor.

![Pesquisar professores por nome](assets/search-instructor.png)

*Pesquisar professores*

Vários professores podem ser selecionados, mas somente um professor por ser atribuído por vez. A hora selecionada será destacada na janela de conflito de hora. Próximo ao professor, um ícone de cruz é exibido e você pode clicar para remover o professor.

![Selecionar vários professores](assets/busy-times.png)

*Pesquisar vários professores*

### Pesquisar professores por habilidades

Procure um professor com uma ou várias habilidades. A pesquisa usa o operador AND.

As habilidades podem ser pesquisadas apenas pelo nome parcial ou completo da habilidade, não pelo nível da habilidade.

No Assistente, insira o nome do professor, o local e o limite de vagas.

Além disso, você pode pesquisar habilidades, que seriam exibidas depois de clicar no ícone de filtro presente no lado direito da caixa de pesquisa do professor. A captura de tela abaixo exibe o botão.

![Insira habilidades para o professor](assets/scheduling-assistant-instructor-skill.png)

*Pesquisar professores por habilidades*

### Filtro de grupo de usuários

Selecione o filtro no campo Professor. Existe um filtro de **[!UICONTROL Grupo de usuários]** em que um autor ou autor personalizado pode encontrar o professor adequado usando os valores no Grupo de usuários.

Se ambos os filtros forem aplicados, uma lista de professores será exibida, pertencendo ao grupo de usuários e tendo as habilidades selecionadas.

Isso se aplica ao Assistente de agendamento na página Cursos ou instâncias.

![assistente de agendamento](assets/scheduling-assistant-2.png)

*Filtrar por grupos de usuários*

### Página Instância

Você também pode acessar o Assistente de Agendamento na página Instância, conforme mostrado abaixo.

O Assistente de agendamento também está disponível na página Instância para administradores e administrador/autor personalizado.

![Assistente de Agendamento da página Instância](assets/instances-scheduling.png)

*Programar professores da página Instâncias*

### Procurar um local

Você pode pesquisar um local especificando o nome da sala de aula e o nome da região do local no módulo e nas páginas do Assistente de programação.

## Formatação de Rich Text

Ao criar um curso, programa de aprendizado, certificação ou ajuda de tarefa, os autores podem inserir diferentes tipos de conteúdo, como texto, imagem ou aplicar várias opções de formatação de texto.

Ao criar um curso, você pode ver o Editor de Rich Text no campo Visão geral do curso. Você pode formatar o conteúdo, adicionar imagens, adicionar hiperlinks etc.

![](assets/rich-text-editor-author.png)

*Iniciar o Editor de Rich Text*

Da mesma forma, você pode usar o Editor de Rich Text para modificar a descrição ao criar um:

**Programa de aprendizado**

![](assets/lp-rte-new.png)

*Usar o Editor de Rich Text para um Programa de Aprendizado*

**Certificação**

![](assets/cert-rte-new.png)

*Usar o Editor de Rich Text para uma Certificação*

**Ajuda de tarefa**

![](assets/job-aid-rte-new.png)

*Usar o Editor de Rich Text para uma Ajuda de Trabalho*

Além disso, você pode usar o Editor de Rich Text para outros idiomas.

## Compatibilidade com a descrição de Rich Text para interface de usuário sem periféricos

### Por que a CSS é necessária?

O Rick Text é composto de marcação HTML. A renderização da marcação como está resultaria no estilo padrão aplicado pelo navegador. Isso geralmente não dá certo com as diretrizes de estilo da empresa. É necessária uma CSS para atender às diretrizes.

### Estilo padrão

A folha de estilos de CSS anexada contém o estilo aplicado pelo Learning Manager. O estilo é ajustado considerando a maioria dos casos de uso. Baixe o arquivo CSS anexado e importe-o para o seu aplicativo da Web de acordo com as suas convenções e sistema de compilação. As classes CSS definidas contêm espaços para nome na classe ql-editor e não interferem nos estilos existentes.

### Personalizar estilos

O estilo padrão pode não atender às necessidades de todos. As personalizações podem ser feitas ao substituir a CSS fornecida. Todo o estilo é delimitado sob o ql-editor como seletores descendentes. São usadas as seguintes classes:

* Recuo: **li.ql-indents-$number**. $number varia de 1 a 9
* tamanho: **ql-size-small**, **ql-size-large**, **ql-size-enorme**

* alinhamento: **ql-align-center**, **ql-align-Justi**, **ql-align-right**

* cor: **ql-color-$color**. $color = branco, vermelho, laranja, amarelo, verde, azul, roxo
* plano de fundo: **ql-bg-$color**. $color = preto, vermelho, laranja, amarelo, verde, azul, roxo
* tags html: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Arquivo CSS a ser usado para personalização.](assets/ql-headless.css)

### ALTERAÇÕES DA API PARA HABILITAR A RENDERIZAÇÃO DE VISÕES GERAIS DO RICH TEXT

Quando os clientes criam uma interface sem periféricos, eles têm a necessidade de exibir os objetos de aprendizado na interface de usuário personalizada que estão desenvolvendo. Para fazer isso, geralmente se usa a API [GET /learningObjects](https://learningmanagereu.adobe.com/docs/primeapi/v2/#!/learning_object/get_learningObjects) que está exposta. Agora que o Learning Manager oferece suporte à captura de “rich text” para o campo de visão geral, o modelo de dados dos objetos de aprendizado nas respostas da API também expõe o mesmo. Consulte o campo chamado “richTextOverview” no fragmento do modelo na resposta da API abaixo. Observe também que o campo exposto anteriormente (”visão geral”) permanece inalterado para compatibilidade com versões anteriores.

```
{ 
 "data": [ 
 { 
 "id": "string", 
 "type": "string", 
 "attributes": { 
 … 
 "localizedMetadata": [ 
 { 
 "description": "string", 
 "locale": "string", 
 "name": "string", 
 "overview": "string", 
 "richTextOverview": "string" 
 } 
 ], 
 … 
 }, 
 "relationships": { 
 … 
 } 
 } 
 } 
 ] 
} 
```

Os clientes que já estão usando o campo de visão geral não são afetados em sua interface sem periféricos e verão apenas texto sem formatação como antes. Se os clientes quiserem aproveitar a visão geral do rich text, eles precisarão criar visões gerais formatadas para seus objetos de aprendizado na interface do autor e, depois disso, o Learning Manager também começará a retornar a visão geral do rich text, além do texto sem formatação (como antes) no modelo de resposta da API.

No entanto, para renderizar esse Rich text na interface do usuário, o cliente precisará incluir um CSS. Isso é explicado detalhadamente nas seções a seguir.

## Permitir várias tentativas {#allowmultipleattempts}

Após o administrador habilitar a opção de várias tentativas, como autor, você pode configurar várias tentativas para os módulos de e-learning no nível do curso ou do módulo.

![](assets/allow-multipe-attempts.png)

*Configurar várias tentativas para um módulo de e-learning interativo*

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Opção</b></p></td>
   <td>
    <p><b>Descrição</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Definir tentativas como</p></td>
   <td>
    <p>Você pode definir o número de tentativas de um módulo como infinitas ou fornecer um limite definido. <span style="font-size: 0.8125rem;">As informações sobre a tentativa serão mostradas ao aluno depois de a opção ter sido habilitada. O aluno pode optar por tentar novamente o módulo clicando no botão 'Tentar Novamente'.</span></p></td>
  </tr>
  <tr>
   <td>
    <p>Interromper a nova tentativa quando o módulo tiver sido concluído ou aprovado</p></td>
   <td>
    <p>Para configurar quando impedir que os alunos selecionem a opção de nova tentativa, ative a caixa de seleção “Interromper nova tentativa depois que o módulo for concluído ou aprovado”. A opção “Repetir” será removida da exibição do aluno assim que ele concluir o módulo com êxito.</p></td>
  </tr>
  <tr>
   <td>
    <p>Bloquear módulo entre tentativas 0:0:1 Formato: Dias/Horas/Minutos</p></td>
   <td>
    <p>Você pode bloquear módulos por um tempo específico entre tentativas, marcando a caixa de seleção “<b>Bloquear módulo entre tentativas 0:0:1 Formato: Dias/Horas/Minutos</b>”. Quando um módulo está bloqueado, o aluno não pode visitar o módulo até que o tempo de bloqueio fornecido expire. </p>
    <p>Você pode definir os critérios de término de uma tentativa marcando as caixas de seleção '<b>Player fechado</b>' ou '<b>Conclusão</b>'.</p></td>
  </tr>
  <tr>
   <td>
    <p>Reprodutor fechado</p></td>
   <td>
    <p>Todos os módulos iniciados são tratados como uma nova tentativa se o critério selecionado for ‘<b>Reprodutor fechado</b>’. O aluno é solicitado a fornecer detalhes de bloqueio do módulo e detalhes da tentativa ao fechar o reprodutor.</p></td>
  </tr>
  <tr>
   <td>
    <p>Conclusão</p></td>
   <td>
    <p>Se o fim da tentativa estiver definido com base na <b>Conclusão</b>, então ele será calculado com base no critério de sucesso do conteúdo. Os alunos não poderão fazer novas tentativas do módulo até que o conteúdo envie as informações de conclusão. Os detalhes de bloqueio e tentativa do módulo são comunicados ao aluno depois que uma tentativa terminar.</p></td>
  </tr>
  <tr>
   <td>
    <p>Definir limite de tempo para concluir o módulo</p></td>
   <td>
    <p>Os autores podem definir um limite de tempo para concluir um módulo marcando a caixa de seleção “<b>Definir limite de tempo para concluir o módulo</b>”.</p>
    <p>Cada reprodutor iniciado é considerado uma nova tentativa e o aluno é solicitado a fornecer detalhes durante o início.</p>
    <p><b>Observação: </b><span style="font-size: 0.8125rem;">A tentativa terminará automaticamente depois que o tempo acabar. Fechar o reprodutor também finalizará a tentativa atual.</span></p></td>
  </tr>
  <tr>
   <td>
    <p>Várias tentativas no nível do módulo</p></td>
   <td>
    <p>Ao selecionar uma tentativa no ‘Nível do módulo’, na lista suspensa ‘Definir tentativa como’, será possível configurar as opções no nível de um módulo individual.</p></td>
  </tr>
 </tbody>
</table>

## Módulos do curso {#coursemodules}

### Adicionar módulos {#addmodules}

Agora você pode adicionar módulos de conteúdo, trabalho prévio e teste. Os módulos de **conteúdo** são os módulos principais que compõem o curso. Os módulos de **trabalho prévio** incluem algumas informações básicas, que pode ajudar os alunos a se preparar para o curso. Esses módulos não são obrigatórios para os alunos. Os módulos de **teste** ajudam os alunos a ignorar o conteúdo e a fazer o teste se eles já conhecem o conteúdo e querem realizar o teste para cumprirem o requisito de conformidade.

Para adicionar um módulo de conteúdo, siga as etapas abaixo:

1. Clique em **[!UICONTROL Adicionar módulos]**. Você pode ver quatro opções de adição de módulos. A primeira opção é para adicionar módulos de ritmo individualizado. Trata-se de módulos que você cria e adiciona à biblioteca do módulo no Adobe Learning Manager. Esta segunda opção serve para configurar a sala de aula virtual. A terceira opção serve para configurar um módulo de sala de aula e a quarta é o módulo de atividade.

   ![](assets/select-module-type.png)

   *Adicionar um módulo a um curso*

   **Módulo de ritmo individualizado:** nesse modo, você pode iniciar e concluir um módulo de curso em seu próprio ritmo. Você pode definir sua própria programação.

   Depois de clicar na opção, você pode visualizar a lista de módulos de ritmo individualizado que já foram adicionados à sua biblioteca de módulos. Aqui você pode percorrer a lista e selecionar os que você quer adicionar ou pode pesquisar os módulos digitando o nome do módulo no campo de pesquisa ou as marcas do módulo.

   Depois de selecionar os módulos, clique em **[!UICONTROL Adicionar]**. Esses módulos agora aparecem na seção Conteúdo.

   Você também pode reorganizar os módulos. Arraste qualquer módulo e mova-o para cima ou para baixo e organize-os em uma sequência adequada.

   **Módulo de sala de aula virtual:** nesse modo, os alunos podem participar em palestras on-line em tempo real realizadas por um professor treinado. Insira o título, a descrição e defina a duração da sessão. Você também pode especificar o URL da conferência e os professores para dirigir a sessão. Para salvar as alterações, clique em **[!UICONTROL Concluído]**.

   ![](assets/1st-image.png)

   *Adicionar um módulo VC*

   Ao criar um curso usando a caixa de diálogo de configuração de sala de aula virtual, defina o **Sistema de Conferência** para a conexão de equipes que você criou. Selecione se deseja um organizador de reunião para o evento.

   Se você selecionar **Sim** para um organizador de reunião, você deve inserir o nome do organizador. Digite o nome e selecione o organizador.

   **Ignorando lobby**

   * Se você selecionar **Sim**, qualquer aluno pode participar da reunião.
   * Se você selecionar **Não**, uma solicitação é enviada ao organizador para permitir ou impedir que o aluno participe da reunião.

   **Observação:** um aluno deve estar disponível no Microsoft Teams. No entanto, o aluno pode participar do Learning Manager como convidado.

   **Módulo de sala de aula:** nesse modo, os alunos participam pessoalmente em palestras realizadas por um professor treinado. Insira o título, a descrição e defina a duração da sessão. Você também pode especificar o local da aula e os professores que dirigem a sessão. Para salvar as alterações, clique em **[!UICONTROL Concluído]**.

   ![](assets/classroom-module.png)

   *Adicionar um módulo de sala de aula*

   Ao criar um curso, na caixa de diálogo de configuração de sala de aula virtual, defina o sistema de conferência para a conexão Microsoft Teams que você criou. Selecione se deseja um organizador de reunião para o evento.

   Se você selecionar Sim para um organizador de reunião, você deve inserir o nome do organizador. Digite o nome do organizador e selecione o organizador.

   **Ignorando lobby**

   * Se você selecionar Sim, qualquer aluno pode participar da reunião.
   * Se você selecionar Não, uma solicitação é enviada ao organizador para permitir ou impedir que o aluno participe da reunião.

   **Observação:** se um aluno quiser participar de Microsoft Teams como convidado, ele deverá inserir o e-mail. O e-mail deve estar presente no Learning Manager.

   **Módulo de atividade:** nesse modo, os alunos devem concluir um conjunto de atividades, como workshops, exercícios, questionários e outras atividades de aprendizado. Insira o título, a descrição e o URL externo para referência. Para salvar as alterações, clique em **[!UICONTROL Concluído]**.

   ![](assets/activity-module.png)

   *Adicionar um módulo de atividade*

   Você pode especificar a duração ao adicionar um módulo de atividade em um curso para o tipo de atividade Envio de arquivo e módulos baseados em xAPI.

1. Da mesma forma, adicione os módulos para modos de trabalho prévio e teste.
1. Escolha o tipo de sequenciamento dos módulos como Ordenado ou Não ordenado de acordo com as suas preferências.

   Se optar por **Ordenado**, os módulos serão exibidos na mesma sequência em que foram criados. Se optar por **Não ordenado**, os módulos não são organizados em sequência. Os alunos podem finalizar os módulos em qualquer ordem.

1. Na lista suspensa Módulos obrigatórios, escolha o número de módulos que o aluno deve realizar para concluir o curso.
1. Adicione uma imagem de capa e a imagem do banner do curso. Os catálogos são criados pelo administrador. Para obter mais informações, consulte [Catálogos](/help/migrated/administrators/feature-summary/catalogs.md).

   **Observação:** as dimensões recomendadas são:

   * **Imagem de capa:** 300 px x 300 px
   * **Imagem do banner:** 1600 px x 140 px

1. No canto superior direito da página, clique em **[!UICONTROL Salvar]**.

#### Adicionar link de HTML no módulo de atividade

Os autores podem adicionar links de HTML no módulo de atividade e definir os critérios de conclusão. Para adicionar um link de HTML e definir critérios de conclusão, siga estas etapas:

1. No aplicativo do autor, selecione **[!UICONTROL Criar Cursos]** na página inicial.
1. Selecionar **[!UICONTROL Adicionar]** da tela **[!UICONTROL Catálogo do curso]**
1. Digite o nome e a descrição do curso.
1. Na opção **[!UICONTROL Módulo]**, selecione **[!UICONTROL Adicionar Módulo]** > **[!UICONTROL Módulo de Atividade]**.
1. No prompt **[!UICONTROL Activity Module]**, digite o nome e a descrição.
1. Selecione o **[!UICONTROL Tipo]** como **[!UICONTROL URL externa]**.
1. Selecione qualquer uma das opções a seguir na opção **[!UICONTROL Critérios de conclusão]**.
   * **[!UICONTROL Marcas do aluno concluídas]**: o aluno tem a opção de marcar o curso como concluído no Fluidic Player.
   * **[!UICONTROL Ao iniciar conteúdo]**: o curso será marcado automaticamente como concluído quando o aluno o iniciar.

   ![](assets/completion-criteria-activity-module.png)
   _Critérios de conclusão_

1. Selecione **[!UICONTROL Adicionar]** e publique o curso.

## Lista de verificação {#create-checklist}

A avaliação é um aspecto importante de qualquer LMS. Avaliações on-line são uma das principais maneiras de avaliar a compreensão de um aluno de um tópico. Mas muitas vezes, é necessário avaliar a compreensão de uma pessoa enquanto ela está no trabalho, observando-a realizar as tarefas necessárias.

Considere os funcionários das lojas ou dos armazéns em avaliação das tarefas que devem desempenhar diariamente. Podem ser as etapas realizadas para consertar uma máquina de café ou as etapas envolvidas na embalagem de um produto. Os professores podem avaliar funcionários para tais tarefas com base em uma lista de verificação e avaliá-los como Aprovado ou Reprovado na atividade de avaliação.

### Criar uma lista de verificação {#createachecklist}

Somente um autor pode criar uma lista de verificação. Uma lista de verificação é um tipo de módulo Atividade. Ao configurar um módulo de Atividade, você, um Autor, pode selecionar uma Atividade como **Lista de Verificação**, conforme mostrado abaixo:

![](assets/checklist-option.png)

*Criar uma lista de verificação*

Depois de escolher a opção **Lista de verificação**, você verá algumas opções adicionais.

**Tipo de lista de verificação:** escolha qualquer opção, **Sim/Não** ou **1-5**. Se você escolher Sim/Não, a lista de verificação conterá perguntas que só podem ser respondidas com Sim ou Não. Se você escolher 1-5, poderá ver uma lista de verificação Likert, na qual você poderá classificar uma pergunta em uma escala de cinco pontos.

**Critérios de aprovação:**

<table>
 <tbody>
  <tr>
   <td>
    <p>Se você escolheu <b>Sim/Não</b>, então...</p></td>
   <td>
    <p>Se você escolheu <b>1-5</b>, então...</p></td>
  </tr>
  <tr>
   <td>
    <p>Defina os critérios de aprovação como o número de respostas como Sim. Por exemplo: se você inserir 3, o aluno passará no curso, se ele receber pelo menos três respostas <b>Sim</b>, quando avaliado por um professor.</p></td>
   <td>
    <p>Defina os critérios de aprovação como um limite de qualquer número entre 1 e 5. Por exemplo: se você inserir 2 e 4, o aluno passará no curso, se ele/ela atingir pelo menos <b>duas </b>avaliações com pontuação maior ou igual a <b>quatro</b>.</p></td>
  </tr>
 </tbody>
</table>

Escolha um professor ou professores que avaliarão o aluno.

Além disso, se você tiver algo para comentar ou uma observação, poderá adicioná-la no campo de texto **Observação para o professor**.

Agora adicione as perguntas da lista de verificação. Clique em **[!UICONTROL Adicionar]** Você só pode adicionar até 150 perguntas.

![](assets/add-checklist-questions.png)

*Adicionar perguntas da lista de verificação*

Para adicionar mais perguntas, clique em **[!UICONTROL Adicionar mais]**.

Salve as alterações, adicione o módulo e publique o curso.

### Adicionar habilidades {#addskills}

Nessa página, insira os seguintes detalhes:

1. Escolha as habilidades do curso, o nível e defina os créditos para a habilidade. Adicione mais habilidades, se necessário.

   ![](assets/course-skills.png)

   *Adicionar habilidades a um curso*

1. Escolha o tipo de inscrição. As opções são as seguintes:

   * **Indicado pelo gerente:** somente gerentes podem indicar esses cursos. Um aluno não poderá se inscrever nesses tipos de cursos.
   * **Aprovado pelo gerente:** os gerentes aprovam esses cursos. Os alunos podem se inscrever nesses cursos, mas não são inscritos diretamente nesses tipos de cursos sem a aprovação do gerente. Uma solicitação de notificação será enviada para os gerentes quando os alunos se inscreverem nesses tipos de cursos. Após a aprovação do gerente, esses cursos são listados como inscritos para os alunos.
   * **Autoinscrição:** os alunos podem se inscrever diretamente nesses tipos de cursos.

1. Se quiser que o aluno consiga cancelar sua inscrição no curso, habilite a caixa de seleção **Os alunos podem cancelar suas inscrições**.
1. Selecione os cursos de pré-requisito que devem ser concluídos antes de realizar seu curso. Clique no campo Cursos e escolha na lista de cursos.

   ![](assets/prerequisite-courses.png)

   *Adicionar cursos de pré-requisito*

1. Habilite a caixa de seleção **Pré-requisitos** se quiser que os cursos de pré-requisito sejam obrigatórios.
1. Adicione palavras-chave como marcas relacionadas ao curso. Essas marcas ajudam os alunos a localizarem com facilidade o curso durante a pesquisa. Todas essas marcas são adicionadas automaticamente com base nos módulos que adicionamos. Se tiver outras marcas que deseja adicionar a este curso, você pode incorporá-las.
1. Adicione os perfis do público-alvo desse curso clicando na área de texto e escolhendo os perfis na sugestões.
1. Adicione arquivos de recurso para o curso como material extra. Arraste os materiais como texto, vídeo ou arquivos de áudio.
1. Agora, este curso estará disponível para os alunos com esses perfis como um curso recomendado. Nesta seção, você também pode anexar recursos adicionais para os alunos. Os alunos poderão baixar estes arquivos para referência futura. Depois de fazer todas as alterações, clique em **[!UICONTROL Salvar]** no canto superior direito. Isso salva o curso como rascunho. O curso é salvo como rascunho, por padrão.

## Atribuir professores para os módulos {#assigninstructorsformodules}

1. Depois de criar os módulos para o curso, você pode atribuir professores aos módulos. No painel do autor, clique em **[!UICONTROL Catálogo de cursos]**.
1. Clique no curso cujo módulo você deseja atribuir aos professores.
1. Na seção **Adicionar Módulos**, clique no módulo ao qual deseja atribuir um professor.
1. No campo **Professor**, especifique o nome do usuário ao qual deseja atribuir a função de professor.

   ![](assets/instructor-field.png)

   *Atribuir uma função de professor a um usuário*

1. Para republicar o curso com as atualizações, clique em **[!UICONTROL Republicar]**.

### Permitir que professores marquem como bem-sucedido

O Adobe Learning Manager permite que os professores marquem o status de sucesso dos alunos em um módulo de sala de aula ou sala de aula virtual. Os autores podem conceder aos professores permissão para marcar o status de sucesso dos alunos ao criar módulos de Sala de aula ou Sala de aula virtual. Os professores podem marcar o sucesso marcando um aluno como Aprovado ou Reprovado, garantindo que o progresso seja atualizado adequadamente.

Para permitir que os professores marquem o sucesso do aluno:

1. Faça logon no Adobe Learning Manager como autor.
2. Selecione **[!UICONTROL Criar cursos]** na página inicial.
3. Selecione **[!UICONTROL Adicionar]**.
4. Digite os detalhes necessários e selecione **[!UICONTROL Adicionar Módulos]**.
5. Selecione **[!UICONTROL Módulo de Sala de Aula Virtual]** ou **[!UICONTROL Módulo de Sala de Aula]**.
6. Digite os detalhes necessários e selecione as datas.
7. Selecione a opção **[!UICONTROL Permitir que o professor marque o êxito]**.

   ![A mensagem “Permitir que o professor marque como bem-sucedido?” a caixa de seleção está realçada, permitindo que os autores registrem o status de sucesso do aluno para um módulo](/help/migrated/authors/feature-summary/assets/allow-instructor-mark-success.png)
   _Tela Detalhes da sessão com a opção Permitir que o professor marque como bem-sucedido destacada para os módulos Sala de aula ou Sala de aula virtual_

8. Selecione **[!UICONTROL Concluído]**.


## Lista de verificação da observação

Um módulo de lista de verificação agora pode ser revisado por gerentes, além de professores. Os gerentes de pessoas, bem como os gerentes não hierárquicos, como gerentes de loja ou gerentes de local, podem revisar e concluir a lista de verificação.

Os autores do curso podem adicionar gerentes de pessoas, bem como gerentes não hierárquicos (se aplicável) como revisores selecionando essas opções de função na seção “Revisores” ao configurar um módulo Lista de verificação. Isso pode ser feito no nível da instância do curso.

![Lista de verificação para gerentes](assets/manager-checklist.png)

*Adicionar revisores a um módulo de atividade*

Selecionar a opção “**[!UICONTROL +Gerentes]**” habilitará automaticamente um gerente de aluno na hierarquia da organização para revisar a lista de verificação. Você não precisa pesquisar e adicionar nomes de gerentes individualmente.

Se o administrador da conta tiver configurado funções de gerente não hierárquicas (como gerentes de local ou gerentes de site) usando a opção Campos ativos, essas funções de gerente estarão disponíveis para você selecionar e permitir que elas revisem a lista de verificação.

Você não precisa pesquisar e adicionar nomes de gerentes individualmente. Quando os alunos se inscrevem no curso da lista de verificação, ele envia automaticamente uma notificação aos gerentes/gerentes de loja para revisão junto com qualquer professor selecionado. Esse fluxo de trabalho facilita para os autores não mencionarem os nomes de gerentes individuais.

Na captura de tela de exemplo fornecida acima, selecionar a opção “**[!UICONTROL +Gerenciadores de Armazenamento]**” habilitará automaticamente o gerente não hierárquico alinhado ao aluno para revisar a lista de verificação. Observe que “store” aqui será substituído pelo campo ativo definido pelo administrador.

As atualizações no módulo de lista de verificação também incluem notificações para professores e gerentes quando um aluno está inscrito em um curso que tem um módulo de lista de verificação. O revisor recebe uma notificação no centro de notificações do Learning Manager, bem como no painel do professor/gerente, informando que a ação da lista de verificação deve ser executada.

<!--![View notification for enrollment](assets/checklist-notification.png)-->

O revisor poderá exibir informações sobre todos os itens de revisão de lista de verificação pendentes no menu Listas de verificação e no menu Notificações quando fizer logon como professor/gerente.

![Aprovações de certificado](assets/pending-task-managers.png)

*Aprovações para certificação*

Depois de clicar em Revisar lista de verificação, o revisor pode concluir a avaliação.

![Revisar itens de revisão de lista de verificação pendente](assets/evaluation-checklist.png)

*Revisar itens de revisão de lista de verificação pendente*

Os relatórios podem ser baixados em listas de verificação, que incluem informações detalhadas sobre a avaliação do aluno, nome do revisor, função e e-mail.

O csv do relatório de lista de verificação tem os campos novos e atualizados:

* Nome do revisor em vez do nome do professor
* E-mail do revisor em vez do e-mail do professor
* Função do revisor: os valores possíveis são Gerente, Gerente de Loja/Local, Professor

## Visualizar um curso {#previewacourse}

Depois que o curso é criado e salvo como rascunho, você pode visualizar o curso como aluno e depois publicá-lo para disponibilizá-lo no catálogo de cursos.

Para visualizar o curso, clique em **[!UICONTROL Visualizar como aluno]**.

![Visualizar um curso como aluno](assets/preview-as-a-learner.png)

*Visualizar um curso como aluno*

Isso abre a página **Visão geral** do curso para você, na qual você pode ver os módulos, a ordem deles e outros detalhes relacionados ao curso.

![](assets/overview-page.png)

*Exibir módulos e outros detalhes relacionados*

Para ver como é a experiência dos alunos ao realizar este curso, clique em cada um dos módulos para começar a reproduzi-los. O curso começa a ser reproduzido no Fluidic Player.

## Publicar um curso {#publishacourse}

Depois de visualizar o curso como aluno, você pode publicá-lo para que esteja disponível para os alunos. Observe que o curso ainda está no modo de rascunho.

Um ciclo de vida típico do curso é semelhante ao seguinte:

* **Rascunho** - Quando um autor termina de criar um curso e o salva. Nesse estado, o curso ainda não está disponível para os alunos.
* **Publicado** - quando um autor termina de publicar um curso. Nesse estado, o curso está disponível para os alunos se inscreverem. Você também pode editar um curso nesse estado.
* **Retirado** - após ter publicado um curso, o autor pode movê-lo para o estado Retirado se não quiser que o curso apareça no catálogo de cursos dos alunos.
* **Excluído** - Um curso no estado Excluído é aquele que foi removido completamente do aplicativo Adobe Learning Manager. Somente os autores podem excluir cursos quando estão nos estados Rascunho ou Retirado.

![](assets/typical-course-lifecycle.png)

*Fluxo de trabalho do ciclo de vida de um curso*

Para publicar o curso que você criou, clique em **[!UICONTROL Publicar]** no canto superior direito da página.

![](assets/publish-a-course.png)

*Publish um curso*

Na mensagem pop-up de confirmação exibida, clique em **[!UICONTROL OK]**.

O curso está disponível no catálogo de cursos.

## Exibir um curso {#viewacourse}

Como autor, você pode exibir uma lista de todos os cursos disponíveis. Para exibir todos os cursos na conta do Learning Manager, clique em Catálogo de cursos. Para exibir todos os cursos criados por você no Learning Manager, clique em **[!UICONTROL Meus cursos]**.

No cartão do curso, passe o mouse sobre as opções e clique em **[!UICONTROL Exibir curso]**.

![](assets/view-a-course.png)

*Exibir um curso*

É exibida a janela de informações do curso. O curso está no modo de somente leitura. Para modificar o curso, clique em **[!UICONTROL Editar]**.

## Retirar um curso {#retireacourse}

Retirar um curso o ocultará dos alunos, mesmo que eles estejam inscritos ou já o tenham concluído. Se retirar um curso, você não pode inscrever alunos novos no curso. Os alunos que já estão inscritos podem realizar o curso.

Para retirar um curso, no cartão do curso, passe o mouse sobre as opções e clique em Retirar curso.

![](assets/retiring-course.png)

*Desativar um curso*

No pop-up de confirmação exibido, clique em **[!UICONTROL Sim]**.

## Duplicar um curso {#duplicateacourse}

Você pode criar uma cópia do curso e modificá-lo. Se quiser fazer backup do curso, você pode duplicá-lo.

## Pesquisar cursos {#searchforcourses}

O Adobe Learning Manager permite encontrar de forma mais fácil os cursos da sua escolha rapidamente. Você pode pesquisar seus cursos das seguintes maneiras:

**Campo de pesquisa:** clique na barra de pesquisa no canto superior direito da **Catálogo de cursos**. Digite o nome do curso ou quaisquer palavras-chave associadas aos seus cursos. Também é possível pesquisar pelas marcas adicionadas durante a criação do curso. As marcas podem ser pesquisadas dentro do campo Pesquisar cursos, o que significa que elas são exibidas no campo de pesquisa à medida que você digita.

![](assets/search-field.png)

*Pesquisar cursos*

**Filtrar lista de cursos:** você pode filtrar os cursos por estado como Todos, Publicado, Rascunho e Retirado. Com base na sua escolha, você pode exibir a lista filtrada de cursos e fazer a escolha apropriada.

Como autor, você também pode classificar os cursos para melhor localizar o curso desejado. Clique em **[!UICONTROL Classificar por]** e escolha ordem alfabética crescente, ordem alfabética decrescente, data de criação do curso, data de atualização do curso e eficácia dos cursos.

![](assets/filter-list-of-courses.png)

*Filtrar lista de cursos*

## Inscrever alunos em um curso {#enrolllearnersinacourse}

Para inscrever os alunos nos cursos ou permitir que os gerentes indiquem alunos para os cursos, você deve alternar para o modo Administrador, pois somente os administradores têm o direito de inscrever alunos nos cursos.

Para alternar para o modo de administrador,

1. Clique em sua foto do perfil e, em seguida, selecione Administrador.
1. No modo Administrador, clique em **[!UICONTROL Cursos]** no painel esquerdo. Nesta página, você pode ver todos os cursos criados por todos os autores na sua conta do Learning Manager.
1. Para inscrever os alunos, passe o mouse sobre o cartão do curso e você poderá ver a opção **Inscrever alunos**. Clique nessa opção.

   ![](assets/enroll-learners.png)

   *Inscrever alunos em um curso*

1. Na caixa de diálogo Inscrever alunos, no canto superior direito, você verá que a opção **Instância padrão** está selecionada. Assim que um curso é criado por um autor, uma instância padrão do curso é criada.

   ![](assets/default-instance.png)

   *Exibir instância padrão de um curso*

1. Comece digitando o nome de um aluno no campo Incluir alunos e escolha um aluno. Você também pode adicionar grupos de usuários aqui. Se quiser inscrever todos os alunos na sua conta do Learning Manager, comece a digitar todos. Você também pode inscrever alunos em uma equipe.

   ![](assets/include-learners.png)

   *Adicionar alunos a um curso*

1. Se desejar excluir alunos do curso, digite o nome do aluno no campo **Excluir alunos**.
1. Depois de inscrever os alunos, clique em **[!UICONTROL Continuar]**. Na caixa de diálogo Inscrever alunos, você pode exibir o resumo da inscrição.

   ![](assets/summary-of-enrollment.png)

   *Exibir resumo de inscrição no curso*

1. Para inscrever todos os alunos no curso, clique em **[!UICONTROL Inscrever]**. Esses usuários estão agora inscritos com êxito nesse curso. Os alunos recebem uma notificação para continuar e fazer o curso. Para inscrever mais alunos, repita o procedimento de inscrição.

## Alterações na página Instância do curso dos módulos de sala de aula virtual do Connect {#connect-vc}

Ao recuperar um curso do Connect, você pode criar dois tipos de salas:

* Dinâmica
* Permanente

Um URL permanente é sempre corrigido. Mas para os usuários que não têm o Connect e sua própria sala de reuniões, eles devem usar uma sala de reuniões dinâmica no tempo de execução. As pessoas podem então participar da reunião.

![](assets/dynamic-room-options.png)

*Opções de sala de reunião dinâmica*

Agora você pode alterar o URL da sala permanente na página **Instância do curso**.

<!--| ![](assets/persistentroomdropdown.png) | ![](assets/courseinstancepage-persistentroom.png) |
|---|---|-->

## Cancelar a inscrição de alunos em um curso {#unenrolllearnersfromacourse}

Ao criar um curso, um autor pode habilitar a opção **Os alunos podem cancelar suas inscrições** para que os alunos que estão participando do curso possam cancelar suas inscrições no curso.

Um administrador pode também cancelar a inscrição de alunos no curso.

![](assets/unenroll-learners.png)

*Cancelar inscrição de alunos em um curso*

Para obter mais informações, consulte [Cancelar a inscrição de alunos](/help/migrated/administrators/feature-summary/courses.md).

## Adicionar módulos de curso no Captivate e no Presenter {#addcoursemodulesforcaptivateandpresenter}

Você também pode publicar módulos de curso no Learning Manager a partir do software Adobe Captivate e Adobe Presenter usando o menu Publicar.

1. No Captivate, clique em **[!UICONTROL Publish]** > **[!UICONTROL Publish para o Learning Manager]**.
1. Forneça o nome de subdomínio ou a ID de e-mail e clique em **[!UICONTROL Enviar]**. Se tiver várias contas, você será solicitado a escolher a conta.
1. Faça logon com as credenciais da Adobe. Se não tiver uma Adobe ID, clique em **[!UICONTROL Criar conta]**. Após a autorização, você será direcionado para a página de publicação do módulo.
1. Forneça quaisquer informações básicas sobre o módulo e clique em Publicar.

Você pode ver o módulo publicado na página de módulos do Learning Manager. Para obter mais informações, consulte [Publicar projeto no Adobe Learning Manager.](https://helpx.adobe.com/captivate/classic/publish-project-to-captivate-prime.html)

## Eficácia do curso {#courseeffectiveness}

A pontuação de eficácia do curso ajuda os autores a avaliarem os cursos que não estão dando certo segundo as necessidades dos alunos e modificá-los apropriadamente. A eficácia do curso é avaliada para compreender a utilidade de um curso para o aluno. É uma combinação dos resultados do feedback do aluno sobre o conteúdo do curso, O curso testa os resultados de um aluno e o feedback do gerente avaliando um aluno com base no aprendizado do curso.

Em **Meus cursos**, o autor pode ver a classificação da eficácia do curso nas miniaturas do curso conforme mostrado na imagem abaixo. Você pode ver a classificação desse curso como 100.

<!--![](assets/course-rating.png)-->

O valor da classificação da eficácia do curso é calculado levando-se em consideração os valores dos feedbacks N1, N2 e N3. Para ver o detalhamento de cada feedback, clique no valor da eficácia do curso. Um menu pop-up é exibido, conforme mostrado abaixo.

![](assets/how-course-effectivenessiscalculated.png)

*Cálculo da eficácia do curso*

Nessa imagem de amostra, todos os usuários receberam todos os três tipos de feedback, portanto, a pontuação é de 100/100. Com essa tabela, você pode entender como a falta de feedback pode afetar a eficácia geral. Para ver como são feitos os cálculos da eficácia do curso, clique na seta para baixo no canto inferior direito da janela pop-up.

<!--![](assets/how-course-effectivenessiscalculated1.png)-->

Conforme o gráfico circular mostrado acima, o gerente atribui mais peso ao feedback N3.

## Certificações e programas de aprendizado {#certificationsandlearningprograms}

O autor e o administrador podem criar certificados e programas de aprendizado para os alunos no aplicativo de criação. Na página inicial, clique em Certificações ou em Programas de aprendizado para criar objetos de aprendizado.

Para saber como criar e gerenciar certificações e programas de aprendizado, consulte [Certificações](/help/migrated/administrators/feature-summary/certifications.md) e [Programas de aprendizado](/help/migrated/administrators/feature-summary/learning-programs.md).

## Cursos obrigatórios para certificação externa {#mandatorycoursesforexternalcertification}

Nas versões anteriores do Learning Manager, para os alunos em uma certificação externa, não era obrigatória a conclusão do curso para completar um certificado.

Agora, é possível fazer cursos obrigatórios ativando a opção **Definir cursos necessários como obrigatórios para a conclusão do certificado** na guia Currículo.

![](assets/set-required-coursesasmandatory.png)

*Definir cursos obrigatórios para concluir um certificado*

Quando os cursos são definidos como obrigatórios:

* A página de envio do gerente lista os alunos somente depois que eles concluírem os cursos.
* O aluno pode carregar um arquivo somente depois de concluir o curso.

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como remover &quot;procurar indicação do gerente&quot; para um curso?

Execute as seguintes etapas:

1. Faça logon no Learning Manager como Autor.
1. Abrir o curso.
1. No painel esquerdo, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Editar]**.
1. Na lista suspensa **Tipo de inscrição**, altere o tipo de inscrição de **Indicado pelo gerente** para **Aprovado pelo gerente** ou **Inscrito**.

1. Depois de alterar o tipo de inscrição, republique o curso.

+++

+++Como combinar cursos?

É possível combinar cursos através de um programa de aprendizado.

1. Faça o logon no Adobe Learning Manager como Administrador.
1. No painel esquerdo, clique em **[!UICONTROL Programas de aprendizado]**.
1. Para adicionar um programa de aprendizado, clique em **[!UICONTROL Adicionar]**.
1. Forneça os detalhes do Programa de aprendizado e clique em **[!UICONTROL Salvar]** para salvar o programa.
1. Depois de criar o Programa de aprendizado, clique em **[!UICONTROL Catálogo]**.
1. Em um cartão do curso, clique em **[!UICONTROL Adicionar]**, conforme mostrado abaixo. Repita o processo para todos os cursos que deseja adicionar ao Programa de aprendizado.

![](assets/add-catalog.png)

Depois de adicionar todos os cursos exigidos no Programa de aprendizado, clique em **[!UICONTROL Publicar]**.

Em um Programa de aprendizado, você só pode adicionar cursos com inscrição, e não cursos Indicados pelo gerente ou Aprovados pelo gerente. Esse é um comportamento padrão no Learning Manager.

+++

+++Como garantir que nem todos os cursos estejam visíveis para todos os alunos?

Você pode conseguir isso através de catálogos. Um catálogo padrão contém todos os cursos adicionados ao Learning Manager por padrão.

Você deve desabilitar o catálogo padrão e criar catálogos personalizados.

1. Faça o logon no Adobe Learning Manager como Administrador.
1. No painel esquerdo, clique em **[!UICONTROL Catálogos]**.
1. Crie um catálogo clicando em **[!UICONTROL Criar]**. Insira os detalhes e clique em **[!UICONTROL Salvar]**.

1. Nas opções do catálogo recém-criado, você pode selecionar diferentes tipos de aprendizado que podem ser adicionados, por exemplo, programa de aprendizado, certificação ou curso.
1. Na seção Programa de aprendizado, clique em **[!UICONTROL Adicionar conteúdo]**.
1. No painel esquerdo, clique em **[!UICONTROL Compartilhar internamente]** ou **[!UICONTROL Compartilhar externamente]**, dependendo do público-alvo que deseja atingir.

1. Para adicionar um grupo de usuários, clique em **[!UICONTROL Adicionar grupos de usuários]**.
1. Na página Catálogos, desabilite o **D[!UICONTROL Catálogo padrão]** e habilite o catálogo que você criou.

![](assets/enable-custom-catalog.png)

+++

+++Como se reinscrever em um curso concluído?

A conclusão de um curso não pode ser revertida. Um aluno **não pode se reinscrever** em um curso concluído.

+++

+++Como os alunos podem ver um curso mesmo depois de concluí-lo?

Um aluno pode ver um curso depois de concluí-lo clicando no botão Revisar do curso.

Siga as etapas abaixo:

1. Faça o logon como aluno.
1. Abra o curso que você concluiu.
1. Clique em **[!UICONTROL Rever]**.

+++

+++Como adicionar um arquivo de recursos no curso?

Ao criar um curso, você pode adicionar arquivos de vídeo, áudio, pdf ou texto ao curso que sejam relevantes para o curso para que o aluno possa acessar material de treinamento adicional.

![](assets/add-resources.png)

+++

+++Como definir várias tentativas no módulo?

**Pré-requisito:** o administrador deve habilitar a opção **Várias Tentativas** em **Configurações > Geral** no aplicativo do administrador.

Como autor, na página de visão geral do curso, habilite a opção **Permitir várias tentativas**.

Para obter mais informações, consulte a [seção sobre várias tentativas](courses.md#Allowmultipleattempts).

+++

+++É possível baixar o conteúdo que foi carregado no Adobe Learning Manager para modificar o conteúdo?

Não, o conteúdo carregado no Learning Manager é um arquivo zip publicado e não é o arquivo de origem. Portanto, mesmo que o conteúdo seja baixado, ele não pode ser editado em uma ferramenta de criação. Você precisaria de um arquivo de origem para editar o conteúdo.

+++
