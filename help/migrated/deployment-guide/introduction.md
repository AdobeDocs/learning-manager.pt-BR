---
jcr-language: en_us
title: Guia de Implantação do Learning Manager
description: O Learning Manager é um sistema de gerenciamento de aprendizagem (LMS) que permite que os profissionais de treinamento forneçam materiais de aprendizado envolventes e rastreáveis que podem contribuir para as necessidades ou metas de uma organização. O Learning Manager permite que os treinadores ou gerentes atribuam cursos e outros objetos de aprendizado, em uma ordem específica, aos alunos.
contentowner: shhivkum
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '3246'
ht-degree: 72%

---



# Guia de Implantação do Learning Manager

## Introdução {#introduction}

O Learning Manager é um sistema de gerenciamento de aprendizagem (LMS) que permite que os profissionais de treinamento forneçam materiais de aprendizado envolventes e rastreáveis que podem contribuir para as necessidades ou metas de uma organização. O Learning Manager permite que os treinadores ou gerentes atribuam cursos e outros objetos de aprendizado, em uma ordem específica, aos alunos. Essa ferramenta também oferece vários recursos avançados, incluindo um fluidic player de vários formatos, gamificação, medalhas e painel do aluno fácil de usar. No entanto, para aproveitar todos esses recursos, é essencial primeiro configurar e instalar o Learning Manager.

Este guia fornece instruções passo a passo sobre como começar a usar o Learning Manager. Este documento também fornece informações detalhadas sobre configuração e instalação detalhadamente. Continue lendo para saber como começar a usar o Learning Manager.

## Para quem este guia se destina? {#whoisthisguideintendedfor}

Como usuário do Learning Manager, você pode assumir a posição de administrador, autor, professor, gerente ou aluno. Este guia destina-se aos usuários que provavelmente estarão envolvidos na configuração de um LMS para uma organização ou cliente:

* **Administrador de TI** - Como administrador de TI, você pode ativar ou integrar o Learning Manager à sua organização. Um administrador de TI também pode adicionar um ou vários usuários e pode desempenhar a função de administrador de integração ou de administrador que integra o Learning Manager a aplicativos de terceiros.
* **Autor** - Como autor do Learning Manager, você pode criar conteúdo de aprendizado necessário para os requisitos de aprendizado de uma organização. Um autor está envolvido na criação do conteúdo básico carregado no Learning Manager.

* **Administrador do Learning Manager** - Um administrador do Learning Manager executa as atividades de configuração e instalação relacionadas ao aplicativo. Em algumas empresas, um administrador de TI também pode desempenhar o papel de administrador do Learning Manager.

## Introdução à implantação do Learning Manager {#getstartedwithcaptivateprimedeployment}

Depois de adquirir o Learning Manager, ative sua conta do Learning Manager usando a chave de licença recebida. Prossiga para as seguintes configurações, conforme indicado no seguinte visual:

![](assets/getting-started-withcaptivateprime.jpg)

## Configurar seu site no Learning Manager {#configureyoursiteincaptivateprime}

Antes de começar a adicionar e implementar objetos de aprendizado no Learning Manager, há algumas configurações-chave que são necessárias. Comece configurando seu site para adequar-se à sua organização. A configuração do site compreende as seguintes etapas:

* Configurar marcas e logotipos para sua organização
* Configurações de modelos de e-mail
* Configurações básicas da conta
* Configurações de feedback
* Configurações do painel do aluno

### Configurar marca e logotipo {#setupbrandingandlogo}

Como administrador, você pode definir a marca e os temas de acordo com os requisitos de marca da sua organização. Para definir a marca e os temas do seu site, faça o seguinte:

### Definindo o logotipo e banner: {#settingthelogoandbanner}

Use as configurações de logotipo e banner para exibir o logotipo da sua empresa no Learning Manager. Configure as opções de marca para definir o domínio da empresa no URL e exibir o nome da organização e esquemas de cores que correspondam à marca da organização. Para definir as configurações de marca:

* Faça logon na sua conta do Learning Manager como administrador.
* No painel esquerdo, clique em **Marcas**.
* Na página de Marcas, você pode configurar as seguintes opções clicando em **Editar** em relação à opção que deseja modificar:

   * **Nome da Organização** : o valor especificado aqui determinará o nome que aparece no banner em cada página do site.
   * **Subdomínio**: esse valor determina a URL do site.
   * **Estilo do logotipo**: a imagem nesse campo aparece como o logotipo no canto superior direito de cada página. Aqui, você pode optar por exibir apenas o logotipo, o nome da sua organização ou o logotipo e o nome da organização.

![](assets/setting-the-themesforyoursite.png)

>[!NOTE]
>
>Você só pode configurar o nome e o logotipo usando Marcas. Não é possível alterar a posição do logotipo ou da imagem.

***O Learning Manager oferece suporte aos seguintes formatos de arquivo para imagens de logotipo: .png, .jpeg, .jpg, .gif, .bmp***

### Definir os temas do seu site {#settingthethemesforyoursite}

O Learning Manager permite que você altere a aparência do seu site usando Temas. O aplicativo fornece os seguintes temas de cores para você escolher:

* Padrão Prime
* Bolhas
* Carnaval
* Outono
* Céu de inverno

Você pode escolher um dos esquemas de cores para alinhar à sua marca corporativa.

1. No painel de navegação esquerdo do Learning Manager, clique em **[!UICONTROL Marcas]**.
1. Na seção **Temas**, clique em **[!UICONTROL Editar]**. O aplicativo permite selecionar um novo tema. Conforme você seleciona um tema, você pode ver imediatamente os esquemas de cores usados para os elementos essenciais da interface.

   ![](assets/setting-the-themesforyoursite.png)

1. Além disso, é possível editar o **Cor da Barra Superior**, **Cor de destaque** e o **Brilho da barra lateral**.  Você pode usar suas próprias cores de marca para esses elementos essencias da interface.
1. Para redefinir os valores para o esquema de cores padrão do tema, clique em **[!UICONTROL Redefinir tema]**. As cores dos elementos essencias da interface do usuário são definidas como as opções padrão para o tema escolhido.
1. Depois de escolher o tema, clique em **[!UICONTROL Mostrar dicas]** para exibir os rótulos ou dicas na visualização.

   ![](assets/setting-the-themesforyoursite-step5.png)

   Observe uma apresentação de slides com várias imagens na seção **Temas**. Esta apresentação de slides permite visualizar instantaneamente o tema ou o esquema de cores. Você pode visualizar imediatamente páginas selecionadas, como a página inicial, o painel do aluno e assim por diante.

1. Se quiser visualizar as alterações em um navegador, clique em **[!UICONTROL Visualização dinâmica]**. Uma janela pop-up Visualização dinâmica do tema é exibida, onde você pode modificar o esquema de cores ou continuar com as opções padrão. Para visualizar suas opções em um navegador, clique em **[!UICONTROL Visualizar]** nesta janela pop-up.

   ![](assets/setting-the-themesforyoursite-step6.png)

1. As opções escolhidas são aplicadas temporariamente ao seu site. Se você deseja salvar o tema e as configurações de cor selecionadas, clique em **[!UICONTROL Aplicar]**.
1. Depois de selecionar e aplicar um tema, clique em ****[!UICONTROL Salvar]**** para salvar sua escolha.

## Configurar modelos de e-mail {#configureemailtemplates}

Como administrador, sua próxima etapa seria configurar modelos de e-mail para vários eventos. Você pode ativar, desativar e modificar modelos de e-mail que serão enviados aos usuários. Há três categorias principais de modelos de e-mail:

* Modelos de e-mail gerais: esses e-mails são disparados para eventos genéricos. Por exemplo, uma notificação de boas-vindas quando um usuário faz logon pela primeira vez.
* Modelos de e-mail associados a um objeto de aprendizado ou atividade: esses e-mails são enviados para alunos, autores ou gerentes sempre que há uma atividade de aprendizado. Por exemplo, e-mails que são acionados após a inscrição no curso, participação na sala de aula, conclusão do curso e assim por diante.
* Lembretes e atualizações: esses e-mails são acionados quando os usuários precisam de atualizações ou lembretes para qualquer evento. Por exemplo, um aluno que recebe um lembrete de um curso futuro ou um administrador que recebe uma notificação por e-mail de um relatório compartilhado.

Você pode ativar e configurar qualquer uma dessas notificações por e-mail no painel Administrador. Para saber como definir modelos de e-mail, realize as seguintes etapas:

1. No painel de navegação esquerdo, clique em **[!UICONTROL ** Modelos de e-mail **.]**
1. Clique em uma das seguintes guias:**[!UICONTROL ** Geral **/** Atividade de aprendizado **/** Lembretes e atualizações **.]** Como exemplo, vamos supor que você clique em **[!UICONTROL ** Atividade de aprendizado **.]**
1. Clique no botão de alternância para qualquer atividade que você deseja acionar um e-mail. Neste exemplo, vamos supor que você clique em **[!UICONTROL ** Programa de Aprendizado - Inscrito por Administrador/Gerente **.]**

   ![](assets/configure-email-templates-step3.png)

   O sistema exibe a mensagem pop-up “Ativado com sucesso”. Agora, sempre que um gerente ou um administrador se inscreve em um curso, o aluno recebe um e-mail dessa conta do Learning Manager.

1. Você pode modificar o modelo de e-mail padrão. Para fazer isso, clique no evento. Neste exemplo, clique em **[!UICONTROL Programa de aprendizado - Inscrito por Administrador/Gerente.]**
1. No menu **[!UICONTROL Visualização do modelo]** pop-up, observe que há duas guias: [!UICONTROL Aluno] e [!UICONTROL Gerente].

   ![](assets/configure-email-templates-step5.png)

   Para cada uma dessas guias, clique no corpo do e-mail para modificar o conteúdo. Para salvar as alterações no modelo de e-mail, clique em **[!UICONTROL Salvar]**.

   Agora, sempre que um aluno é inscrito em um curso pelo gerente ou pelo administrador, o aluno e seu gerente recebem uma notificação por e-mail.

   ***Observação: as modificações são aplicáveis somente ao modelo de e-mail associado ao evento selecionado.***

1. Observe que não foi possível modificar o URL da conta ou a assinatura no modelo de e-mail. Para modificar o **[!UICONTROL URL da conta]** ou **[!UICONTROL Assinatura]**, clique na guia **[!UICONTROL Configurações]**. Nessa guia, você pode modificar o banner de e-mail, a assinatura de e-mail e o URL da conta.

   O link do URL da conta é mostrado em todos os e-mails, pouco antes da assinatura. Insira o URL de sua preferência e clique em **[!UICONTROL Salvar]**. Esse URL é visível somente para os usuários internos.

   Para o banner de email, você pode alterar a cor do banner selecionando  **[!UICONTROL ** Plano de fundo do banner **.]** Você também pode usar uma imagem personalizada como banner selecionando o **[!UICONTROL Imagem personalizada]** opção. Clique em  **[!UICONTROL Salvar]** depois de fazer as alterações.

   ***Observação: o tamanho da imagem personalizada para o banner de e-mail deve ser de 1240x200px. As imagens maiores que o tamanho recomendado são cortadas.***

   ***O Learning Manager só é compatível com os tipos de arquivo .jpg, .jpeg e .png para banners de e-mail.***

   ![](assets/configure-email-templates-step6.png)

1. Você também pode ativar os e-mails opcionais do gerente. Se você selecionar a opção **[!UICONTROL Habilitar]** caixa de seleção, sempre que um relatório direto recebe um e-mail desta conta do Prime, o gerente também é incluído na lista de distribuição.

   ***Observação: as configurações nesta guia são aplicáveis a todos os modelos globalmente.***

### Configurar modelos de e-mail para um objeto de aprendizado {#configureemailtemplatesforalearningobject}

Além de configurar modelos de e-mail em um nível global, como administrador, você também pode configurar modelos de e-mail para um objeto de aprendizado específico. Nesse caso, todas as alterações feitas no modelo de e-mail são aplicáveis somente a esse objeto de aprendizado.

Essa opção também está disponível para autores, quando eles configuram um objeto de aprendizado.

Para configurar modelos de e-mail para um objeto de aprendizado:

1. Clique no curso, programa de aprendizado ou certificação para o qual você deseja configurar o modelo de e-mail.
1. No painel esquerdo, clique em **[!UICONTROL ** Modelos de e-mail **.]** O sistema exibe uma caixa de diálogo pop-up ****[!UICONTROL Visualização do modelo]****.
1. Modifique o assunto ou o corpo do modelo de e-mail e clique em **[!UICONTROL **Salvar**]**para aplicar as alterações.
1. Para cancelar as alterações, clique em **[!UICONTROL ** Reverter para original **.]**

### Restringir usuários de receber e-mails {#restrictusersfromreceivingemails}

Como administrador, você pode selecionar quem receberá ou não e-mails do Learning Manager. Você pode fazer isso usando a guia ****[!UICONTROL Usuário restrito]**** na caixa de diálogo ****[!UICONTROL Configurações]** **guia. Os usuários podem ser adicionados a esta lista através do nome, da ID de e-mail ou da ID de usuário exclusiva. Os usuários listados nessa opção ficarão restritos ao recebimento de qualquer comunicação por e-mail do Learning Manager.

## Configurações da sua conta {#configureyouraccountsettings}

O Learning Manager permite que você defina algumas configurações de conta, como configurações básicas, configurações de feedback, configurações gerais e configurações para o painel do aluno. Os procedimentos a seguir informam como definir essas configurações:

### Definir configurações básicas {#configurebasicsettings}

1. Na página inicial do Learning Manager, clique em ****[!UICONTROL Configurações]****. Por padrão, o sistema exibe a página Informações básicas, com os campos de idioma e local padrão.
1. Clique em ****[!UICONTROL Alterar]**** no canto superior direito da página para editar as Informações básicas.
1. Configure as seguintes opções:

   * **País**: selecione o país neste campo suspenso.
   * **Fuso horário**: defina o fuso horário apropriado para o seu local.
   * **Local**: selecione o idioma de sua escolha. Se você alterar o idioma nesse campo, a alteração será aplicada a todos os usuários que usam esse aplicativo. No entanto, individualmente, cada usuário pode modificar o idioma de preferência.
   * **O exercício tem início a partir de**: selecione o mês em que o exercício financeiro da sua organização começa.



   ![](assets/configure-basic-settings-step3.png)

## Definir configurações de feedback {#configurefeedbacksettings}

O Learning Manager permite que você colete feedback de alunos para um curso. Também é possível coletar feedback sobre os alunos usando o Learning Manager. Para solicitar feedback, primeiro você deve configurar os tipos N1 e N3 de feedback.

O feedback N3 é o feedback que um gerente fornece sobre um aluno. Você pode usar esse tipo de feedback para controlar o desempenho dos alunos ao longo do tempo. O feedback N1 é o feedback que um aluno fornece sobre um curso. Esse tipo de feedback ajuda um administrador a coletar feedback direto sobre um curso.

Como administrador, você pode definir as configurações de feedback globalmente. Para isso, siga este procedimento:

1. Na página inicial do Learning Manager, clique em **[!UICONTROL Configurações]**.
1. No painel esquerdo, clique em **[!UICONTROL Geral]**.
1. Para configurar o feedback N1, clique no botão **[!UICONTROL Feedback N1]** guia. Você verá as opções para configurar uma pergunta obrigatória e várias perguntas opcionais. Estas são as perguntas que um aluno visualiza enquanto fornece feedback após concluir um curso. As perguntas são formuladas como instruções para que os alunos possam selecionar sua resposta em uma escala de 1 a 5.

   A primeira parte do feedback N1 é uma pergunta obrigatória sobre como um aluno recomenda este curso a um amigo ou colega.

   ***Observação: não é possível editar ou modificar a pergunta obrigatória.***

   ![](assets/configure-feedbacksettings-step3.png)

1. Para configurar as outras perguntas para o seu questionário de feedback, clique nas perguntas dos ****[!UICONTROL Cursos de ritmo individualizado]**** ou ****[!UICONTROL Cursos de sala de aula]****. Quando você clica em uma pergunta, o sistema permite editar as perguntas padrão.



   ![](assets/configure-feedbacksettings-step4.png)

1. Você pode ativar ou desativar as perguntas padrão ou modificar completamente as perguntas padrão para atender às suas necessidades. Por exemplo, você pode remover a pergunta padrão “A questão do treinamento foi relevante para mim.” e adicionar substituir a pergunta por “Eu achei o treinamento útil e relevante.”
1. Depois de finalizar as perguntas para os alunos, você pode definir as configurações de lembrete. Por padrão, há um lembrete existente, no qual o aplicativo envia lembretes automáticos aos alunos após a conclusão bem-sucedida de um curso. Esse lembrete também é definido para ser repetido a cada duas semanas até que o aluno responda. Você pode modificar o lembrete existente clicando nele ou adicionar um novo lembrete.

   ![](assets/configure-feedbacksettings-step6.png)

1. Defina as configurações de lembrete preenchendo as seguintes opções:

   * **Quando enviar**: especifique se deseja enviar a solicitação de feedback na conclusão do curso ou após a conclusão do curso.
   * **Dias após a conclusão**: especifique o número de dias após os quais você deseja enviar a solicitação de feedback. Este campo é visível somente se selecionado ****[!UICONTROL Após a conclusão do curso]****.

   * **Recorrência**: especifique se deseja enviar o lembrete de feedback todos os dias, todas as semanas ou todos os meses. Você também pode especificar quantas semanas deseja enviar o lembrete.

1. Clique na marca de verificação para salvar as configurações do lembrete.
1. Depois de finalizar todas as configurações de feedback, clique em **[!UICONTROL **Salvar**]**no canto superior direito da página.

## Configurar feedback N3: {#configurel3feedback}

O Feedback N3 contém as perguntas que são enviadas ao gerente do aluno após o aluno concluir um curso. O Feedback N3 permite que um administrador rastreie as alterações no comportamento ou na habilidade de um aluno ao longo do tempo. Para configurar esse feedback, na página Comentários, clique na guia ****[!UICONTROL Feedback N3]****. Você vê uma pergunta padrão. O gerente deve responder a essa pergunta usando uma escala de classificação de cinco pontos.

![](assets/configure-l3-feedback.png)

Semelhante ao Feedback N1, você pode configurar os lembretes para feedback N3. Você pode modificar o lembrete existente ou adicionar um novo lembrete de feedback.

Depois de finalizar a pergunta de feedback e as configurações do lembrete, clique em ****[!UICONTROL Salvar]**** para aplicar as configurações.

## Configurar feedback em um nível de instância {#configurefeedbackataninstancelevel}

O procedimento anterior descrevia as etapas para definir as configurações de feedback em um nível global. Ou seja, as configurações são aplicadas a todos os cursos. Além dessas perguntas globais, como administrador ou autor, você pode configurar perguntas adicionais de feedback N1 e N3 em um nível de instância.

Para definir as configurações de feedback em um nível de instância:

1. Na página inicial do Learning Manager, clique em **[!UICONTROL Cursos]**.
1. Passe o mouse sobre o curso onde deseja definir as configurações de feedback. Clique em [!UICONTROL **Exibir curso**.]

   ![](assets/configure-feedbackataninstancelevel.png)

1. Na página de detalhes do curso, clique em **[!UICONTROL Padrões de Instância]** na seção Configurar.
1. No menu [!UICONTROL **Idioma**] , selecione o idioma no qual deseja que o questionário de feedback seja exibido.
1. Ative o Feedback de reação N1 se quiser solicitar feedback dos alunos. Você pode adicionar até duas perguntas nesta seção. Os alunos podem fornecer respostas descritivas a essas perguntas.
1. Marque a caixa de seleção **[!UICONTROL Tornar obrigatório]** se quiser tornar uma ou ambas as perguntas obrigatórias.
1. Selecione **[!UICONTROL Mostrar questionário imediatamente após a conclusão do curso]** se quiser que os alunos visualizem o questionário de feedback imediatamente após a conclusão do curso.

   ![](assets/configure-feedbackataninstancelevel-step7.png)

1. Para configurar o feedback de Alteração de comportamento N3 em um nível de instância, ****[!UICONTROL Habilitar]**** o Feedback N3. O aplicativo exibe uma pergunta predefinida e obrigatória e uma pergunta em branco na qual você pode inserir uma pergunta de sua escolha.
1. Para a pergunta predefinida sobre a melhoria do aluno após realizar o curso, a resposta está no formato Escala Likert. Isto é, os gestores têm de escolher uma opção numa escala de Concordo totalmente para Descordo totalmente.
1. Especifique a segunda pergunta para o gerente. Os gerentes podem fornecer uma resposta descritiva para esta pergunta.
1. Marque a caixa de seleção ****[!UICONTROL Tornar obrigatório]**** se quiser tornar a segunda pergunta obrigatória.

   ![](assets/configure-feedbackataninstancelevel-step11.png)

1. Opcionalmente, defina as configurações do lembrete no nível da instância. Se você não definir as configurações do lembrete aqui, as configurações globais de lembrete serão atribuídas automaticamente.
1. Depois de finalizar as perguntas de feedback e as configurações de lembrete, clique em **[!UICONTROL **Salvar**]**para aplicar suas configurações.

   ***Nota: as configurações de feedback não são aplicáveis às certificações.***

## Definir configurações gerais {#configuregeneralsettings}

As configurações gerais no Learning Manager permitem que os administradores definam configurações genéricas que afetam outros recursos no aplicativo. Por exemplo, você pode usar configurações gerais para especificar se a eficácia do curso pode ficar visível para os alunos. Para definir as configurações gerais:

1. Na página inicial do Learning Manager, clique em ****[!UICONTROL Configurações]****.
1. No painel esquerdo, clique em ****[!UICONTROL Geral]****.
1. Na página Configurações gerais, você pode definir as seguintes opções:

   Para todas essas opções, o recurso que cada opção afeta é variado. Podemos fornecer links cruzados para cada um dos recursos detalhados, se necessário.

   * **Mostrar eficácia do curso**: ative essa opção se quiser que os alunos vejam a eficácia de um curso no título do curso.
   * **Opção de redefinição de módulo**: ative essa opção se deseja dar aos alunos a capacidade de redefinir um módulo. Os alunos podem redefinir os módulos caso tenham falhado ou caso tenham concluído parcialmente o módulo e queiram iniciar novamente.
   * **Moderação do curso**: ative esta opção se deseja que as alterações em um curso sejam aprovadas por um administrador antes que as alterações sejam visíveis para os alunos.
   * **Quadro de discussão**: ative essa opção se deseja que os alunos visualizem e participem de painéis de discussão para cursos. Se você ativar a caixa de seleção **Quadro de discussão**, os alunos e professores poderão postar comentários nos cursos. No entanto, se as configurações no nível do curso indicarem que este recurso não está selecionado, as configurações no nível do curso prevalecem sobre as configurações do administrador.

   * **Opção Explorar habilidades**: ative esta opção se quiser que os alunos explorem habilidades de liderança e colegas.
   * **IDs exclusivas de objetos de aprendizado**: ative essa opção se deseja fornecer aos autores a capacidade de adicionar IDs exclusivas aos objetos de aprendizado.
   * **Mostrar lista de catálogos**: ative essa opção se deseja que os alunos vejam todos os catálogos disponíveis. Essa opção ajuda os alunos a refinar suas listas de objetos de aprendizado.



   ![](assets/configure-generalsettings-step3.png)

## Definir configurações do painel do aluno {#configurelearnerdashboardsettings}

O painel do aluno no Learning Manager permite que os alunos vejam seus cursos obrigatórios e recomendados, além de suas realizações, habilidades e comunicados. Os administradores podem decidir como esse painel do aluno deve ser exibido, definindo as configurações do painel do aluno. Essas configurações permitem que os administradores definam os widgets na página do aluno. Essas configurações também especificam como e onde os widgets são colocados no painel do aluno. Como administrador, você pode visualizar o layout do painel do aluno antes de aplicar as configurações.

1. Na página inicial do Learning Manager, clique em **[!UICONTROL Configurações]**.
1. No painel de navegação esquerdo, clique em **[!UICONTROL ** Painel do aluno **.]**
1. Selecione os widgets que deseja ativar. Se você desmarcar um widget, ele será removido imediatamente da visualização. Os alunos não podem ver este widget em seu painel.
1. Clique em ****[!UICONTROL Salvar]**** para aplicar as configurações.

   ![](assets/configure-learnerdashboardsettings-step4.png)

1. Para aplicar as configurações padrão, clique em **[!UICONTROL Restaurar para padrão.]** Nesse caso, todos os widgets, exceto **[!UICONTROL Bem-vindo e Comunicados pop-up]**, estão visíveis.

   ***Mesmo depois de ativar as configurações do Painel do aluno, os alunos podem modificar e mover os widgets em seus respectivos painéis.***

