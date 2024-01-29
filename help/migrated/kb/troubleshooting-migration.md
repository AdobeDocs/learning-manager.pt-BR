---
description: Este documento contém dicas básicas de solução de problemas para solucionar alguns dos problemas típicos que podem ser encontrados ao migrar dados e conteúdo do LMS existente do Learning Manager.
jcr-language: en_us
title: Solução de problemas de migração
contentowner: jayakarr
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---



# Solução de problemas de migração

Este documento contém dicas básicas de solução de problemas para solucionar alguns dos problemas típicos que podem ser encontrados ao migrar dados e conteúdo do LMS existente do Learning Manager.

## Problemas genéricos de migração {#genericmigrationissues}

### Não é possível fazer logon na pasta FTP ou na pasta de conteúdo {#unabletologintoftpfolderorcontentfolder}

Verifique se suas contas foram criadas nos serviços FTP e Box. Ao criar um projeto de migração, você solicita a configuração desses dois serviços. Assim que você cria os serviços, você recebe e-mails do Exavault e do Box para redefinir ou configurar as senhas. Se você não se lembrar das senhas, poderá redefini-las acessando os sites do Exavault e do Box.

### As tarefas não são refletidas mesmo depois de clicar no botão Atualizar {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Certifique-se de que os arquivos CSV sejam carregados na pasta correta no Exavault FTP. A estrutura do caminho deve ser a seguinte:

`code Account>Project>Sprint location`

* Certifique-se de que os nomes de arquivo dos arquivos CSV estejam de acordo com os nomes de especificação do CSV:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### As falhas são mostradas para tarefas com registros de erro {#failuresareshownforjobswitherrorrecords}

1. Baixe os registros de erro clicando em **Baixar registros de erros** link
1. Corrija os CSVs originais com base nos erros relatados e
1. Execute novamente o sprint com os CSVs modificados.

A prática recomendada é executar CSVs modificados em um novo sprint quando o número de alterações for menor em comparação ao número total de registros.

### Não é possível fazer logon no aplicativo Learning Manager mesmo depois de interromper a migração do sprint {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Pode levar de 10 a 15 minutos para desbloquear uma conta quando uma execução do sprint for interrompida ou concluída. Tente acessar o aplicativo após 15 minutos.

### Alguns dos trabalhos de migração exibem o status &#39;Em andamento&#39; mesmo depois que &#39;Parar&#39; é acionado. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Pode levar de 10 a 15 minutos para parar a execução de todas as tarefas quando estiverem no estado &#39;Em andamento&#39;. Verifique novamente o status após 10 minutos.

### Não é possível criar um sprint porque o botão está desativado {#unabletocreateasprintasthebuttonisdisabled}

Verifique se o sprint atual está marcado como concluído antes de criar um sprint. Clique em **[!UICONTROL Marcar sprint como concluído]** na parte superior da página para concluir uma migração do sprint.

### Não é possível marcar um projeto de migração como concluído porque o botão está desativado {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Verifique se o sprint atual está marcado como concluído antes de marcar a conclusão do projeto de migração. Clique em **[!UICONTROL Marcar sprint como concluído]** na parte superior da página para concluir uma migração do sprint.

## Problemas de CSV {#csvissues}

### A migração do arquivo module_version.csv está falhando e o conteúdo ainda não foi migrado {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Verifique se o conteúdo está disponível na pasta Conteúdo (conta do Box no projeto de migração especificado, caminho do sprint). Verifique também se você selecionou a opção **Sim** para **Você migrará o conteúdo deste sprint?** pergunta na página de criação do sprint.

Caso se esqueça de selecionar **Sim** e continue neste sprint, aguarde até concluir o sprint. Crie outro sprint e clique nele **[!UICONTROL Sim]**.

### Os registros enrollment.csv ou user_course_grade.csv falham com uma mensagem de erro &#39;Não é uma ID válida do Learning Manager&#39; {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Verifique se a ID de e-mail fornecida como parte dos campos userId e assignedByUserID pertence a usuários válidos do Learning Manager. Caso contrário, adicione o usuário, crie um novo sprint com **Sincronizar usuários** opção selecionada. Caso o usuário não faça parte da organização, adicione-o como um usuário excluído no Learning Manager usando Adicionar especificação do CSV dos usuários. Um exemplo de especificação de CSV para adicionar usuários excluídos é fornecido abaixo como referência.

[Users.csv](assets/users.zip) Consulte **Especificações do CSV e CSVs de amostra** seção em [Manual de migração](../integration-admin/feature-summary/migration-manual.md) para baixar um conjunto completo de especificações do CSV e arquivos CSV de amostra.

### Os cursos aparecem em branco ou módulos incorretos são reproduzidos em um curso migrado {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Assegurar que o **moduleOrderInCourse** o valor principal de um curso começa com **0** e está em ordem contínua. A ordem em termos de courseModuleType deve ser PRETEST, TESTOUT, CONTENT

Além disso, verifique se duas versões de Atividade, Sala de aula e Sala de aula virtual não estão vinculadas ao curso existente.

### Receber uma mensagem como &#39;O módulo já está vinculado a um curso existente&#39; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

O Learning Manager não permite vincular o módulo Atividade/Sala de aula virtual/Sala de aula a mais de um curso. Certifique-se de que o módulo não esteja vinculado a nenhum outro curso.

### Todos os cursos mostram a versão mais recente dos módulos Atividade/Sala de aula virtual/Sala de aula, mesmo que os cursos estejam vinculados a versões de módulos diferentes {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

O controle de versão dos módulos Atividade, Sala de aula e Sala de aula virtual não é suportado no Learning Manager. Se você fornecer versões por meio do arquivo moduleVersion.csv, ele atualizará o arquivo existente em vez de criar uma nova versão.

### A duração desejada não é exibida para um módulo de Atividade/Sala de aula virtual/Sala de aula migrado {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

A duração desejada não é uma entrada válida para o módulo Atividade/Sala de aula virtual/Sala de aula.

### O URL do hiperlink não abre no Learning Manager {#hyperlinkurldoesntopenupincaptivateprime}

Verifique se os links fornecidos são prefixados com &#39;http://&#39; ou &#39;https://&#39;

### A migração de moduleVersion falha com erros “Arquivo não encontrado” {#moduleversionmigrationfailswithfilenotfounderrors}

Verifique se o arquivo referido está presente na pasta de conteúdo e se foi migrado com êxito.

### A migração de moduleVersion falha com uma mensagem de erro “Ocorreu um erro interno - para o módulo : x e moduleVersion : y” {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Execute novamente o sprint para resolver o problema.
