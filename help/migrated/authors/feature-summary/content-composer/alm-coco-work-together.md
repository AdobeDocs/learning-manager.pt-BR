---
description: Saiba como o Compositor de conteúdo lida com a criação e o Adobe Learning Manager lida com a entrega, o rastreamento e a geração de relatórios após a publicação.
jcr-language: en_us
title: Como o Compositor de conteúdo e o Adobe Learning Manager trabalham juntos
source-git-commit: 68d15fa96588b2569c9b1cdb480e2ba9f31a1cf6
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---


# Como o Adobe Learning Manager Content Composer e o Adobe Learning Manager funcionam juntos

O compositor de conteúdo controla a criação. O Adobe Learning Manager lida com entrega, inscrição, rastreamento e emissão de relatórios. Os dois produtos se conectam por meio de uma etapa de publicação. Depois de publicar a partir do Compositor de conteúdo, o curso se torna um módulo na Biblioteca de conteúdo do ALM, onde pode ser montado em um curso e atribuído aos alunos.

## O que o Compositor de conteúdo controla

- Lição e estrutura de tópicos

- Conteúdo do curso - texto, imagens, vídeos, componentes e verificações de conhecimento

- Questionários de fim de aula, incluindo tipos de pergunta e opções de resposta

- Tema visual

- Critérios de conclusão e de êxito

- Versão do SCORM usada para relatórios

## O que o Adobe Learning Manager controla

- Inscrição e acesso do aluno

- Metadados do módulo - duração, tags, IDs exclusivas, expiração

- Montagem do curso - combinação de módulos do Compositor de conteúdo com outros conteúdos de aprendizado

- Acompanhamento, relatórios e transcrições do aluno

- Controle de versão do curso

- Notificações e lembretes

## Da criação do curso à conclusão do aluno

1. **Criar o curso no Compositor de Conteúdo**: crie seu curso no Compositor de Conteúdo, incluindo lições, tópicos, temas, questionários e configurações de conclusão. Defina as configurações do curso - critérios de conclusão, critérios de sucesso e pontuação do questionário - antes de publicar.
Para mais informações, consulte [Definir configurações do curso](#settings).

2. **Publish para Adobe Learning Manager:** quando a criação estiver concluída, conecte o Compositor de Conteúdo à sua conta do ALM por meio das configurações de **Exportar** e publique o curso. O compositor de conteúdo envia o curso para a Biblioteca de conteúdo do ALM como um módulo compatível com SCORM.
   ![Um curso publicado com um cabeçalho, logotipo e tema de fonte personalizados aplicados](../assets/49_published_course_custom_branding_header_updated.png)

3. **Configure o módulo no ALM:** depois de publicado, o curso aparece como um módulo na Biblioteca de Conteúdo do ALM. Um autor do ALM configura os metadados do módulo - incluindo duração, tags, IDs exclusivas e configurações de expiração - e adiciona o módulo a um curso do ALM juntamente com outros conteúdos de aprendizado.
   ![Metadados do módulo e campos de critérios de conclusão](../assets/50_alm_add_content_composer_module_metadata_updated.png)

>[!NOTE]
>
>Se você definir critérios de conclusão e êxito no Adobe Learning Manager (ALM), essas configurações terão precedência sobre as definidas no Compositor de conteúdo.

4.**Publish o curso ALM:** um autor do ALM monta o módulo em um curso ALM, adiciona imagens e configurações do curso e o publica. Somente após essa etapa é possível inscrever os alunos.

Para obter mais informações, consulte o [Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-author).
![&#x200B; A Biblioteca de Conteúdo no Adobe Learning Manager, mostrando os módulos publicados e de processamento](../assets/51_alm_content_library_list_view_updated.png)

Para obter mais informações, consulte [Criação do curso como autor no ALM](https://experienceleague.adobe.com/en/docs/learning-manager/using/authors/courses).

5.**Os alunos concluem o curso:** acessam o curso por meio do Adobe Learning Manager, iniciam o módulo Compositor de Conteúdo, concluem lições e questionários e recebem pontuações com base nos critérios de conclusão e sucesso configurados na Etapa 1.

Para mais informações, consulte [Acessar curso como aluno](https://experienceleague.adobe.com/en/docs/learning-manager/using/get-started/getting-started-learner).

&#x200B;6. O ALM registra o progresso do aluno: o status de conclusão, as pontuações do quiz e os dados do aluno são registrados no ALM e disponibilizados por meio de transcrições do aluno e relatórios administrativos.

7.**Atualize o curso usando o controle de versão**: quando você atualiza o conteúdo no Compositor de Conteúdo e republica, o ALM cria uma nova versão do módulo. Os autores do ALM podem atualizar cursos existentes para usar a versão mais recente.
