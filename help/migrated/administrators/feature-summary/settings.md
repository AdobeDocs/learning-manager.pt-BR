---
description: Saiba mais sobre as configurações da conta do Learning Manager que você pode configurar como administrador.
jcr-language: en_us
title: Configurações
contentowner: manochan
exl-id: a563d955-f67e-4218-88df-625cde673601
source-git-commit: fbab332b92dd6d017c2517d7df09a4c37ce3f6bf
workflow-type: tm+mt
source-wordcount: '3985'
ht-degree: 65%

---

# Configurações

Saiba mais sobre as configurações da conta do Learning Manager que você pode configurar como administrador.

Você pode alterar as configurações do seu perfil de administrador e atualizar as configurações da conta. Veja as informações do seu perfil, adicione/altere a foto do perfil e modifique **[!UICONTROL Sobre mim]** conteúdo. Atualize as informações da empresa, defina os métodos de logon dos usuários e configure a integração da conexão nas configurações da conta.

## Configurar o Adobe Learning Manager

Este treinamento captura as noções básicas das configurações no nível da conta.

[![botão](assets/launch-training-button.png)](https://learningmanager.adobe.com/app/learner?accountId=98632&amp;sdid=PYPVPSZY&amp;mv=display&amp;mv2=display#/course/7476018)


Se você não conseguir iniciar o treinamento, escreva para <almacademy@adobe.com>.

## Configurações da conta {#accountsettings}

Para atualizar as configurações da conta da sua organização, clique em **[!UICONTROL Configurações]** no painel esquerdo.

**Informações básicas (informações da empresa)**

Clique em **[!UICONTROL Alterar]** na página e edite as configurações de país, fuso horário, localidade e exercício financeiro.

**Configurar administrador de contato**

Se deseja adicionar ou alterar os endereços de e-mail dos administradores de suporte da empresa, você pode configurar clicando em **[!UICONTROL Geral]** no painel esquerdo. Clique em **[!UICONTROL Alterar]** adjacente a **[!UICONTROL ID do email de suporte]** e adicione as ids de e-mail. O e-mail é enviado a esses administradores quando o aluno clica **[!UICONTROL Contatar administrador]** no rodapé da página

Adicione mais IDs de e-mail com ponto-e-vírgula como separador.

**Métodos de logon** - Os administradores podem escolher o modo através do qual os usuários internos ou externos podem acessar a conta.

* **Usuários internos:** Para usuários internos, você pode definir a Adobe ID ou logon único (SSO) como modos de logon.
* **Usuários externos:** Para usuários externos, você pode definir a Adobe ID, o logon único ou a Learning Manager ID.

Se optar pela Learning Manager ID, os usuários externos podem fazer logon nessa conta depois de criarem seus nomes de usuário e senhas do Learning Manager.

>[!NOTE]
>
>Se houver vários perfis externos definidos, todos os perfis poderão ter qualquer tipo de logon. Por exemplo, se o tipo de logon for Adobe ID, todos os perfis precisam fazer logon usando apenas a Adobe ID. Cada perfil não pode ter seu tipo de logon individual.

Você pode acessar o aplicativo Learning Manager usando a Adobe ID ou usando o logon único. O logon único é um mecanismo que permite que um usuário se autentique uma vez e obtenha acesso a vários aplicativos várias vezes. Esta configuração não é obrigatória para a empresa. Se sua empresa tiver um provedor de SSO com base no SAML 2.0, você pode usá-lo para configurar o aplicativo Learning Manager. A configuração é necessária na âmbito da empresa e no aplicativo Learning Manager. Se optar por usar o SSO, entre em contato com o suporte da Adobe para receber as instruções de configuração.

**Feedback**

Clique em **[!UICONTROL Feedback]** no painel esquerdo a fim de configurar o questionário para obter feedback dos alunos após a conclusão de um curso. Consulte [conteúdo de ajuda do recurso cursos](courses.md) sobre a criação de feedback N1 e N3.

**Várias tentativas**

Selecionar **[!UICONTROL Configurações]** > **[!UICONTROL Geral]** > **[!UICONTROL Várias tentativas]**.

Se você ativar a caixa de seleção “Várias tentativas”, os autores poderão definir “Várias tentativas” para cursos ou módulos de e-learning interativos. Ao marcar a segunda caixa de seleção, os administradores podem definir “Tentativas infinitas” por padrão para qualquer curso de e-learning interativo recém-criado.

![](assets/admin-config.png)

*Marque a caixa de seleção Várias tentativas*

**Moderação do curso**

Clique em **[!UICONTROL Geral]** no painel esquerdo, e selecione a opção Moderação do curso para ativar a funcionalidade Moderação do curso. Para saber mais sobre esse recurso, consulte [Moderação do curso](courses.md#main-pars_header_1879001177).

**Quadro de discussão**

Se ativar a caixa de seleção Quadro de discussão, os alunos e professores podem publicar comentários dos cursos usando a guia Discussão na página Cursos do aplicativo dos alunos. No entanto, se as configurações no nível do curso indicarem que este recurso não está selecionado, as configurações no nível do curso prevalecem sobre as configurações do administrador.

**Painel do aluno**

No painel esquerdo, clique em Painel do aluno. Esta página permite que você selecione os widgets que deseja exibir na página Alunos. Selecione os widgets que deseja habilitar na página Alunos. Os widgets que não forem selecionados não serão exibidos na página Alunos.

**Adobe Connect**

Clique em **[!UICONTROL Adobe Connect]** no painel esquerdo para configurar a conta do Adobe Connect para hospedar sessões de sala de aula virtual. Para obter mais informações, consulte  [Adobe Connect](adobeconnect-integration.md) ajuda do recurso.

## Configurações gerais {#general}

Habilite ou desabilite as configurações a seguir:

<table>
 <tbody>
  <tr>
   <th>
    <p><b>Nome</b></p>
    </th>
   <th>
    <p><b>Descrição</b></p>
   </th>
  </tr>
  <tr>
   <td>Mostrar eficácia do curso</td>
   <td>Se ativado, os alunos podem ver a eficácia do curso atual no quadro Curso. Este recurso está disponível apenas para cursos. A classificação por estrelas não é suportada em Programas de aprendizado ou Certificados. Está disponível para cursos e programas de aprendizado, mas não para certificações.</td>
  </tr>
  <tr>
   <td>Moderação do curso</td>
   <td>Se habilitada, todas as alterações nos Cursos precisarão da aprovação do Administrador para ficarem visíveis aos alunos.</td>
  </tr>
  <tr>
   <td>Painel de discussão</td>
   <td>Se habilitar a caixa de seleção Quadro de discussão, os alunos e professores podem publicar comentários dos cursos usando a guia Discussão na página Cursos do aplicativo dos alunos. No entanto, se as configurações no nível do curso indicarem que este recurso não está selecionado, as configurações no nível do curso prevalecem sobre as configurações do administrador.</td>
  </tr>
  <tr>
   <td>Várias tentativas</td>
   <td>Se habilitada, o Autor pode configurar várias tentativas nos módulos de curso.</td>
  </tr>
  <tr>
   <td>Opção Explorar habilidades</td>
   <td>Se habilitada, os Alunos podem explorar habilidades de Pares e de Liderança e assinar as Habilidades de sua escolha.</td>
  </tr>
  <tr>
   <td>Visibilidade de habilidades ou tags</td>
   <td>Exibir todas as habilidades e tags para os alunos. Exiba todas as habilidades e rótulos, apenas as atribuídas ou aquelas que fazem parte dos Catálogos visíveis ao Aluno.</td>
  </tr>
  <tr>
   <td>IDs exclusivas do objeto de aprendizado</td>
   <td>Se habilitada, um Administrador ou um Autor pode adicionar uma ID exclusiva para cada Objeto de aprendizado.</td>
  </tr>
  <tr>
   <td>Mostrar painéis de filtro</td>
   <td>
    <p><a id="filter-panels"></a>Controle quais painéis de filtro estão disponíveis para os usuários no aplicativo do aluno para refinar os resultados da pesquisa. As opções são as seguintes:</p>
    <ul>
     <li>Catálogos</li>
     <li>Tipo</li>
     <li>Formato</li>
     <li>Duração</li>
     <li>Habilidades</li>
     <li>Níveis de habilidade</li>
     <li>Tags</li>
    </ul>
    <p>Quando o estudante inicia o aplicativo do aluno, nas seções Meu aprendizado e Catálogo, o aluno pode ver os filtros em seus respectivos painéis.</p>
    <p><b>Nota: </b>os formatos <b>e </b>a duração <b>dos filtros </b>são desativados por padrão e não aparecem para os alunos imediatamente após a liberação. O administrador deve habilitá-los. <br></p></td>
  </tr>
  <tr>
   <td>Mostrar lista de catálogos</td>
   <td>Se habilitada, os Alunos podem ver uma lista de todos os Catálogos disponíveis para eles. Alunos podem usar isso para ajustar os Objetos de aprendizado exibidos.</td>
  </tr>
  <tr>
   <td>Terminologia do produto</td>
   <td>O Learning Manager tem uma terminologia padrão usada em todo o produto. Modifique a terminologia para atender às necessidades da sua organização.</td>
  </tr>
  <tr>
   <td>Atualização da versão do módulo</td>
   <td>Configure a configuração padrão para atualizar o conteúdo. As configurações podem ser modificadas para cada conteúdo da página do curso.</td>
  </tr>
  <tr>
   <td>Registrar usuários automaticamente</td>
   <td>Se habilitada, usuários recém-importados serão registrados automaticamente. Por padrão, os usuários devem ser inscritos manualmente para começar a usar o Learning Manager.</td>
  </tr>
  <tr>
   <td><a id="autodelete"></a>Excluir usuários internos automaticamente</td>
   <td>Se habilitada, os usuários internos serão excluídos automaticamente se não acessarem o sistema por um determinado número de dias. Esse recurso é aplicável a usuários com a função <b>Aluno</b>. Para restaurar o acesso, os usuários devem entrar em contato com o Administrador.<br></td>
  </tr>
  <tr>
   <td>Mostrar rótulos de catálogo</td>
   <td>Se habilitada, Administradores e Autores podem definir rótulos de catálogo e seus valores, e vinculá-los a Objetos de aprendizado.</td>
  </tr>
  <tr>
   <td>Alunos podem visualizar suas pontuações</td>
   <td>Se habilitada, os alunos podem exibir suas pontuações na transcrição do aluno.</td>
  </tr>
  <tr>
   <td>E-mail do resumo</td>
   <td>
    <p>Um administrador pode habilitar ou desabilitar o envio de um e-mail aos alunos. O administrador também poderá controlar a frequência dos e-mails enviados.</p>
    <ul>
     <li>Para <b>contas ativas</b>, os e-mails de resumo serão desativados por padrão e administrador pode ativá-los manualmente.</li>
     <li>Para <b>contas de avaliação</b>, a opção para e-mails de resumo permanecerá desativada e o administrador não poderá ativar a opção.</li>
    </ul>
    <p>Se o recurso estiver desativado, então:</p>
    <ul>
     <li>A opção <b>E-mail de resumo</b> será desativada.</li>
     <li>Um aluno não pode ver a configuração do usuário para a assinatura de e-mail de resumo.</li>
    </ul>
    <p> Se o recurso estiver ativado:</p>
    <ul>
     <li>O administrador pode ativar e modificar a opção E-mail de resumo.</li>
     <li>Em <b>Configuraçõe do perfil </b>no aplicativo do aluno, um aluno (não na lista DND) pode optar por assinar/cancelar a assinatura do e-mail de resumo.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Habilitar ícones do Cartão de treinamento<br></td>
   <td>Se habilitada, os ícones serão exibidos nos Cartões de treinamento no aplicativo do aluno.<br></td>
  </tr>
  <tr>
   <td>Links de rodapé</td>
   <td>
    <p>Adicione links ou IDs de e-mail que aparecem como rodapés. É possível adicionar até três links de rodapé.</p>
    <p>Para personalizar os links no rodapé, execute as seguintes etapas:</p>
    <ol>
     <li>Clique em <b>Adicionar mais</b>, insira o nome e o URL ou ID de e-mail nos campos especificados. Prefixe o URL com http:// ou https://.</li>
     <li>Para propagar a mudança em todas as localidades, clique em <b>Replicar</b>. Isso garante que o nome e o URL seja aplicado em todos os idiomas.</li>
     <li>Para salvar as alterações, clique em <b>Salvar</b>. Você verá uma mensagem pop-up confirmando a alteração. Depois de clicar em OK, o rodapé será preenchido com os novos links.</li>
    </ol>
    <p>Além disso, você pode:</p>
    <ul>
     <li>Clique no botão <b>Redefinir</b> para redefinir os valores padrão na caixa de diálogo <b>Ajuda</b> e <b>Contatar administrador</b> campos.</li>
     <li>Personalize o link no rodapé em todos os idiomas. Clique na lista suspensa <b>Idioma</b>, selecione o idioma e adicione o <b>Nome</b> e o <b>URL</b> nos campos especificados. Depois de salvar as alterações, os links atualizados aparecerão no rodapé.<br></li>
    </ul></td>
  </tr>
  <tr>
   <td>Fuso horário do relatório<br></td>
   <td>
    <p>Defina uma preferência em nível de conta para exportar a transcrição de aprendizado nos seguintes fusos horários:</p>
    <ul>
     <li>UTC (comportamento padrão)</li>
     <li>Preferência de fuso horário no nível da conta</li>
    </ul>
    <p>A transcrição do aluno baixada usando a API Trabalhos também baixa os dados no fuso horário selecionado.</p>
    <p><b>Observação: </b>Não há alterações esperadas na transcrição do aluno por padrão imediatamente após a liberação. Os administradores podem configurar essa configuração em Admin &gt; Configurações &gt; Geral &gt; Fuso horário do relatório.</p></td>
  </tr>
 </tbody>
</table>

<table border="0" cellpadding="0" cellspacing="0" width="1709">
 <tbody>
  <tr>
   <td height="20" width="147">Nome</td>
   <td>Descrição</td>
  </tr>
  <tr>
   <td height="20">Mostrar eficácia do curso</td>
   <td>Se habilitada, os Alunos podem ver a Eficácia do curso atual no quadro do Curso.</td>
  </tr>
  <tr>
   <td height="20">Moderação do curso</td>
   <td>Se habilitada, todas as alterações nos Cursos precisarão da aprovação do Administrador para ficarem visíveis aos alunos.</td>
  </tr>
  <tr>
   <td height="20">Painel de discussão</td>
   <td>Se habilitar a caixa de seleção Quadro de discussão, os alunos e professores podem publicar comentários dos cursos usando a guia Discussão na página Cursos do aplicativo dos alunos. No entanto, se as configurações no nível do curso indicarem que este recurso não está selecionado, as configurações no nível do curso prevalecem sobre as configurações do administrador.</td>
  </tr>
  <tr>
   <td height="20">Várias tentativas</td>
   <td>Se habilitada, o Autor pode configurar várias tentativas nos módulos de curso.</td>
  </tr>
  <tr>
   <td height="20">Opção Explorar habilidades</td>
   <td>Se habilitada, os Alunos podem explorar habilidades de Pares e de Liderança e assinar as Habilidades de sua escolha.</td>
  </tr>
  <tr>
   <td height="20">Visibilidade de habilidades ou tags</td>
   <td>Exibir todas as habilidades e tags para os alunos. Exiba todas as habilidades e rótulos, apenas as atribuídas ou aquelas que fazem parte dos Catálogos visíveis ao Aluno.</td>
  </tr>
  <tr>
   <td height="20">IDs exclusivas do objeto de aprendizado</td>
   <td>Se habilitada, um Administrador ou um Autor pode adicionar uma ID exclusiva para cada Objeto de aprendizado.</td>
  </tr>
  <tr>
   <td rowspan="10" height="191">Mostrar painéis de filtro</td>
   <td>Controle quais painéis de filtro estão disponíveis para os usuários no aplicativo do aluno para refinar os resultados da pesquisa. As opções são as seguintes:</td>
  </tr>
  <tr>
   <td height="19">Catálogos</td>
  </tr>
  <tr>
   <td height="19">Tipo</td>
  </tr>
  <tr>
   <td height="19">Formato</td>
  </tr>
  <tr>
   <td height="19">Duração</td>
  </tr>
  <tr>
   <td height="19">Habilidades</td>
  </tr>
  <tr>
   <td height="19">Níveis de habilidade</td>
  </tr>
  <tr>
   <td height="19">Tags</td>
  </tr>
  <tr>
   <td height="19">Quando o estudante inicia o aplicativo do aluno, nas seções Meu aprendizado e Catálogo, o aluno pode ver os filtros em seus respectivos painéis.</td>
  </tr>
  <tr>
   <td height="20">Nota: os formatos e a duração dos filtros são desativados por padrão e não aparecem para os alunos imediatamente após a liberação. O administrador deve habilitá-los. </td>
  </tr>
  <tr>
   <td height="20">Mostrar lista de catálogos</td>
   <td>Se habilitada, os Alunos podem ver uma lista de todos os Catálogos disponíveis para eles. Alunos podem usar isso para ajustar os Objetos de aprendizado exibidos.</td>
  </tr>
  <tr>
   <td height="20">Terminologia do produto</td>
   <td>O Learning Manager tem uma terminologia padrão usada em todo o produto. Modifique a terminologia para atender às necessidades da sua organização.</td>
  </tr>
  <tr>
   <td height="20">Atualização da versão do módulo</td>
   <td>Configure a configuração padrão para atualizar o conteúdo. As configurações podem ser modificadas para cada conteúdo da página do curso.</td>
  </tr>
  <tr>
   <td height="20">Registrar usuários automaticamente</td>
   <td>Se habilitada, usuários recém-importados serão registrados automaticamente. Por padrão, os usuários devem ser inscritos manualmente para começar a usar o Learning Manager.</td>
  </tr>
  <tr>
   <td height="20">Excluir usuários internos automaticamente</td>
   <td>Se habilitada, os usuários internos serão excluídos automaticamente se não acessarem o sistema por um determinado número de dias. Esse recurso é aplicável a usuários com a função Aluno. Para restaurar o acesso, os usuários devem entrar em contato com o Administrador.</td>
  </tr>
  <tr>
   <td height="20">Mostrar rótulos de catálogo</td>
   <td>Se habilitada, Administradores e Autores podem definir rótulos de catálogo e seus valores, e vinculá-los a Objetos de aprendizado.</td>
  </tr>
  <tr>
   <td height="20">Alunos podem visualizar suas pontuações</td>
   <td>Se habilitada, os alunos podem exibir suas pontuações na transcrição do aluno.</td>
  </tr>
  <tr>
   <td rowspan="9" height="172">E-mail do resumo</td>
   <td>Um administrador pode habilitar ou desabilitar o envio de um e-mail aos alunos. O administrador também poderá controlar a frequência dos e-mails enviados.</td>
  </tr>
  <tr>
   <td height="19">Para contas ativas, os e-mails de resumo serão desativados por padrão e administrador pode ativá-los manualmente.</td>
  </tr>
  <tr>
   <td height="19">Para contas de avaliação, a opção para e-mails de resumo permanecerá desativada e o administrador não poderá ativar a opção.</td>
  </tr>
  <tr>
   <td height="19">Se o recurso estiver desabilitado, então:</td>
  </tr>
  <tr>
   <td height="19">A opção E-mail de resumo será desativada.</td>
  </tr>
  <tr>
   <td height="19">Um aluno não pode ver a configuração do usuário para a assinatura de e-mail de resumo.</td>
  </tr>
  <tr>
   <td height="19"> Se o recurso estiver ativado:</td>
  </tr>
  <tr>
   <td height="19">O administrador pode habilitar e modificar a opção E-mail de resumo.</td>
  </tr>
  <tr>
   <td height="20">Nas Configurações do perfil no aplicativo do aluno, um aluno (não na lista DND) pode optar por assinar/cancelar a assinatura do e-mail de resumo.</td>
  </tr>
  <tr>
   <td height="20">Habilitar ícones do Cartão de treinamento</td>
   <td>Se habilitada, os ícones serão exibidos nos Cartões de treinamento no aplicativo do aluno.</td>
  </tr>
  <tr>
   <td rowspan="8" height="153">Links de rodapé</td>
   <td>Adicione links ou IDs de e-mail que aparecem como rodapés. É possível adicionar até três links de rodapé.</td>
  </tr>
  <tr>
   <td height="19">Para personalizar os links no rodapé, execute as seguintes etapas:</td>
  </tr>
  <tr>
   <td height="19">1. Clique em Adicionar mais, insira o nome e o URL ou ID de e-mail nos campos especificados. Prefixe o URL com http:// ou https://.</td>
  </tr>
  <tr>
   <td height="19">2. Para propagar a alteração em todas as localidades, clique em Replicar. Isso garante que o nome e o URL seja aplicado em todos os idiomas.</td>
  </tr>
  <tr>
   <td height="19">3. Para salvar as alterações, clique em Salvar. Você verá uma mensagem pop-up confirmando a alteração. Depois de clicar em OK, o rodapé será preenchido com os novos links.</td>
  </tr>
  <tr>
   <td height="19">Além disso, você pode:</td>
  </tr>
  <tr>
   <td height="19">Clique no ícone Redefinir para redefinir os valores padrão nos campos Ajuda e Contatar administrador.</td>
  </tr>
  <tr>
   <td height="20">Personalize o link no rodapé em todos os idiomas. Clique na lista suspensa Idioma, selecione o idioma e adicione o Nome e o URL nos campos especificados. Depois de salvar as alterações, os links atualizados aparecerão no rodapé.</td>
  </tr>
  <tr>
   <td rowspan="5" height="96">Fuso horário do relatório</td>
   <td> Defina uma preferência em nível de conta para exportar a transcrição de aprendizado nos seguintes fusos horários:</td>
  </tr>
  <tr>
   <td height="19">UTC (comportamento padrão)</td>
  </tr>
  <tr>
   <td height="19">Preferência de fuso horário no nível da conta</td>
  </tr>
  <tr>
   <td height="19">A transcrição do aluno baixada usando a API Trabalhos também baixa os dados no fuso horário selecionado.</td>
  </tr>
  <tr>
   <td height="20">Observação: não há alterações esperadas na transcrição do aluno por padrão imediatamente após a liberação. Os administradores podem configurar essa configuração em Admin &gt; Configurações &gt; Geral &gt; Fuso horário do relatório.</td>
  </tr>
  <tr>
   <td height="19">Integração do Badgr</td>
   <td>Se habilitada, os alunos poderão carregar as suas medalhas no site do Badgr. Em cenários de educação de clientes, as organizações querem ser capazes de "certificar" os seus clientes e dar-lhes a oportunidade de exibir essas credenciais nas redes sociais. Isso motiva o aluno a fazer um treinamento e compartilhar as suas conquistas com outras pessoas. </td>
  </tr>
  <tr>
   <td height="135">
    <p>Mostrar classificação</p></td>
   <td>
    <ul>
     <li>Se a opção <b>Eficácia do curso</b> estiver habilitada, os alunos poderão ver apenas o valor da eficácia do curso.</li>
     <li>Se a opção <b>Classificação por estrelas</b> estiver ativada, os alunos poderão ver apenas a classificação por estrelas média e o número de alunos que classificaram o curso.<br></li>
    </ul>
    <p>Este recurso está disponível apenas para cursos. A classificação por estrelas não é compatível com Programas de aprendizado ou Certificados.<br><br><b>Observação: </b>Essa alteração afeta apenas o aplicativo do aluno. </p>
    <p>Em todos os outros aplicativos (administrador, autor, gerente, administrador personalizado, autor personalizado), as alterações nas configurações (classificação por estrelas ou eficácia do curso ou desabilitação da exibição da classificação) não terão nenhum efeito. </p>
    <p>Para novas contas, o <b>Mostrar classificações</b> terá a opção de <b>Classificação por estrelas</b> ativado por padrão.</p>
    <p>Para contas existentes, se a conta tinha a opção anteriormente <b>Eficácia do curso</b> ativado, depois o <b>Mostrar classificações</b> será ativada com a opção Eficácia do curso selecionada. Se a opção <b>Eficácia do curso</b>s estiver desativado, a caixa de diálogo <b>Mostrar classificações</b> também será desativada. Quando a <b>Mostrar classificações</b> estiver ativada, a opção <b>Classificação por estrelas</b> será ativada por padrão.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <tbody>
  <tr>
   <td>
    <p>Caminhos de aprendizado</p></td>
   <td>
    <p>Se a opção <b>Ativar recursos estendidos do Caminho de aprendizado</b> estiver ativada, os administradores poderão incluir os Caminhos de aprendizado nos Caminhos de aprendizado e combinar esses Caminhos de aprendizado com Cursos. A opção é irreversível.<br></p></td>
  </tr>
  <tr>
   <td>
    <p>Gerenciamento de professores<br></p></td>
   <td>
    <p>Habilite essa configuração para restringir a lista de professores que podem ser selecionados ao criar sessões de sala de aula ou sala de aula virtual. Todos os usuários com privilégios de professor só podem ser atribuídos como professor para qualquer sessão. Essa restrição não se aplica a fluxos de trabalho de migração.<br></p>
  </td>
  <tr>
    <td>
      <p>Importação de habilidades</p>
    </td>
    <td>
      <p>Se ativado, você pode escolher uma origem externa para importar Habilidades. As habilidades dos recursos de aprendizado existentes serão importadas para o repositório de habilidades uma vez durante a execução inicial. Para todas as importações subsequentes de recursos de aprendizado, as habilidades serão importadas para o repositório de habilidades apenas para itens recém-importados.
      Quando a opção é ativada, a ação é irreversível. Você não pode desativar ou mudar para outra fonte mais tarde.
      </p>
    </td>
  </tr>
  </tr>
 </tbody>
</table>

>[!NOTE]
>
>Quando a configuração de importação de habilidades estiver ativada, o layout da conta não poderá ser alternado para a exibição Clássica, ou seja, a alternância para a conta Clássica será desativada após a **Importação de habilidade** opção está ativada.


## Recomendação baseada em IA

O Learning Manager inclui uma nova página inicial do aluno, que é moderna, orientada por conteúdo e personalizada de acordo com as preferências do aluno. As recomendações de aprendizado baseadas em IA têm como objetivo aprimorar o envolvimento do aluno e identificar e corrigir as lacunas de aprendizado.

O algoritmo de recomendação foi projetado para receber várias fontes de entrada, incluindo dados do setor sobre funções, cargos e descrições que a Adobe tem originado de seus parceiros. Esses dados são então usados para treinar algoritmos de IA de Adobe para que o Learning Manager possa criar um mapa que conecte habilidades alinhadas pela indústria a cargos e/ou designações. Isso se torna uma entrada para o algoritmo de recomendação

O Learning Manager usa algoritmos de modelagem de tópicos para analisar o conteúdo de treinamento em uma conta e mapeá-los para as habilidades.

O Learning Manager usa dados de atividade de mesmo nível como outro sinal para orientar o algoritmo de recomendação de forma personalizada. Atividades como inscrição, conclusão e feedback explícito fornecido pelos alunos são usadas aqui.

Além disso, o Learning Manager usa informações explícitas e implícitas coletadas de alunos individuais para personalizar ainda mais as recomendações. Um aluno poderá indicar as suas áreas de interesse explicitamente por meio de inscrições e o Learning Manager receberá essas informações implicitamente com base em como o aluno realiza os treinamentos.

Finalmente, o administrador também poderá influenciar o algoritmo de recomendação usando os atributos do aluno que o Learning Manager deve observar ao definir grupos de pares e, também, destacando os treinamentos para grupos de usuários específicos.

## Renomeação de objetos de aprendizado {#renaminglearningobjects}

Este recurso está disponível apenas em inglês.

Agora, os administradores podem renomear objetos de aprendizado no Learning Manager. Os itens a seguir são terminologias que podem ser renomeadas.

Módulo\
Curso\
Programa de aprendizado\
Certificação\
Plano de aprendizado\
Ajuda de tarefa\
Catálogo\
Habilidade\
Medalha\
Anúncio\
Meu aprendizado\
Quadro de classificação\
Eficácia\
Pré-requisito\
Trabalho prévio\
Conteúdo principal\
Teste\
Ritmo do aluno\
Mesclado\
Sala de aula\
Aula virtual\
Atividade

Para renomear as terminologias, siga estas etapas.

1. Como administrador, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Geral]** > **[!UICONTROL Terminologia do produto]**. A opção de terminologia do produto é aberta.

   ![](assets/product-terminology.png)

   *Renomear terminologia do produto*

1. As alterações podem ser feitas por meio do upload de um modelo de terminologia do produto modificado por meio do download do arquivo CSV de amostra. Para baixar o arquivo CSV de amostra, clique no botão **[!UICONTROL Baixe aqui]** opção.
1. O arquivo CSV baixado contém o nome dos objetos na coluna A. Na coluna B, escolha o nome que você deseja atribuir ao respectivo objeto. Observe que é necessário atualizar as formas singular e plural do nome separadas por uma barra vertical (|).
1. É possível modificar uma ou mais linhas. Você pode manter as linhas inalteradas ou removê-las do arquivo CSV antes de carregá-las.
1. Faça upload do arquivo CSV modificado e clique em **[!UICONTROL Salvar]**. As atualizações do Learning Manager refletem suas alterações.
1. Para redefinir as terminologias padrão, clique em **[!UICONTROL Redefinir Terminologia do Produto]**.

   ![](assets/with-reset-option.png)

   *Redefinir as terminologias do produto*

## Configurações do perfil {#profilesettings}

1. Clique na seta suspensa no canto superior direito, ao lado de sua foto/conta, e escolha **[!UICONTROL Configurações do perfil]**.
1. Na caixa de diálogo suspensa, você pode adicionar/alterar uma foto passando o mouse sobre ela e clicando em **[!UICONTROL Editar]** na área de foto do perfil.
1. Adicionar/modificar **[!UICONTROL Sobre]** conteúdo clicando em **[!UICONTROL Editar]** adjacentes.
1. Clique em **[!UICONTROL Salvar].**

## Pasta de conteúdo {#content-folder}

O Learning Manager oferece suporte a pastas de conteúdo privado. Um administrador pode configurar pastas de conteúdo privadas e fornecer seu acesso a autores personalizados específicos usando Funções personalizadas. Observe que os autores padrão (também chamados de autores completos) continuam a ter acesso a todo o conteúdo da conta. Portanto, os autores completos têm acesso a todas as pastas e conteúdo.

As pastas de conteúdo podem ser configuradas pelos administradores. Uma vez configuradas, as pastas de conteúdo ficam visíveis para os autores, que já poderão colocar o conteúdo em uma ou várias pastas.

Para adicionar uma pasta de conteúdo, no aplicativo do administrador, clique em **[!UICONTROL Configurações]** > **[!UICONTROL Pasta de conteúdo]**.

![](assets/manage-content-folders.png)

*Alterar configurações da Pasta de conteúdo*

### Pasta

Uma pasta é um repositório de conteúdo, que é um subconjunto de toda a biblioteca de conteúdo disponível em uma conta com as seguintes propriedades:

* Somente um administrador pode criar, editar ou excluir uma pasta.
* Um administrador pode controlar o acesso a pastas como parte da definição de funções somente para administradores personalizados.
* O conteúdo **deve sempre estar associado a pelo menos uma pasta**. Para começar, todo o conteúdo será associado à pasta pública, que poderá ser alterada posteriormente.
* O conteúdo pode ser associado a várias pastas no momento da criação, o que também será possível através de operações de cópia.
* Todos os nomes de pastas devem ser exclusivos dentro da conta, caso contrário, ocorrerá um erro ao nomear uma pasta.

As pastas controlam apenas a visibilidade do conteúdo e não criam cópias do conteúdo. Portanto, a edição de conteúdo refletirá em todas as pastas associadas.

### Pasta pública

Uma pasta pública está sempre presente em uma conta e, inicialmente, todo o conteúdo será parte dessa pasta. Mais tarde, os autores podem mover o conteúdo dessa pasta para outras pastas. Uma pasta pública tem as seguintes propriedades:

* Por padrão, todo o conteúdo associado a essa pasta estará acessível a todos os tipos de autores.
* Qualquer conteúdo que faça parte de uma pasta pública não pode fazer parte de nenhuma outra pasta. O inverso também é verdadeiro.

Esta pasta não pode fazer parte da definição de função configurável. Consequentemente, não ter uma pasta pública na definição de função configurável não restringe o acesso a uma pasta pública.

### Pasta privada

* Qualquer pasta criada por um administrador é uma pasta privada.

### Operações de pasta

**Adicionar uma pasta**

Para adicionar uma pasta, clique em **[!UICONTROL Adicionar]** no canto superior direito da janela.

**Excluir uma pasta**

Você também pode excluir uma pasta. Selecione a pasta a ser excluída, clique no menu Ações e, em seguida, clique em **[!UICONTROL Excluir pasta]**.

>[!NOTE]
>
>As pastas podem ser excluídas quando todo o seu conteúdo associado também estiver associado a outras pastas. Se houver conteúdo vinculado somente à pasta que está sendo excluída, primeiro mova o conteúdo para outra pasta e, em seguida, exclua a pasta.

## Locais de sala de aula

Os administradores podem usar essa configuração para criar e configurar uma biblioteca de locais de sala de aula. Os autores podem selecionar um local pré-configurado para configurar o evento de sala de aula. Selecione um local da biblioteca para preencher automaticamente as informações do local, o URL e o limite de vagas.

Como administrador, você pode:

### Importar CSV de locais

Adicionar locais à sua conta importando um arquivo CSV de locais. O arquivo CSV deve conter a coluna Cidade.

### Adicionar um local

Adicione o seguinte:

1. Nome do local: insira o nome da sala de aula.
2. Informações de local: insira as informações sobre o local.
3. Região do Local: O valor informado aparece como filtro Locais de Treinamento para alunos.
4. URL do local: insira o URL do local.
5. Limite de vagas: insira a capacidade de vagas da sala.

![local da sala de aula](assets/location-alm.gif)

*Adicionar locais de sala de aula*

Você também pode adicionar o local com a ajuda de um CSV. O CSV deve conter os campos:

* name
* informações
* url
* limite de vagas
* região

<!--![Add classroom locations](assets/add-classroom-csv.png)-->

### Configurações {#admin-classroom-settings}

Selecionar **Editar** para alterar o seguinte:

* **Permitir que autores criem locais**: Uma vez ativado, todos os locais criados pelos autores serão listados na guia “Todos os locais”. Os alunos também verão esses locais nos filtros Catálogo e calendário.
* **Permitir que autores modifiquem e excluam locais**: uma vez ativado, os autores poderão modificar e excluir todos os locais da sala de aula. As modificações feitas pelos autores serão refletidas em toda a plataforma, incluindo relatórios.

## Perguntas frequentes {#frequentlyaskedquestions}

+++Como criar pastas diferentes para a biblioteca de conteúdo?

Clique em **[!UICONTROL Configurações]** > **[!UICONTROL Pasta de conteúdo]**. Para adicionar uma pasta, clique em **[!UICONTROL Adicionar]** no canto superior direito, e na caixa de diálogo, insira o nome e a descrição da pasta.

As pastas de conteúdo podem ser configuradas pelos administradores. Uma vez configuradas, as pastas de conteúdo ficam visíveis para os autores, que já poderão colocar o conteúdo em uma ou várias pastas.

Para obter mais informações, consulte a seção em [Pasta de conteúdo](settings.md#content-folder).
+++

+++Como adicionar exercício financeiro para a conta?

Entrada **[!UICONTROL Configurações]** > **[!UICONTROL Informações básicas]**, clique em **[!UICONTROL Alterar]**. Na guia **[!UICONTROL O exercício tem início em]** selecione o mês.
+++
