---
description: Saiba como integrar o conector de acesso a dados de treinamento com o Adobe Learning Manager
jcr-language: en_us
title: Conector de acesso a dados de treinamento
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '872'
ht-degree: 2%

---


# Conector de acesso a dados de treinamento no Adobe Learning Manager

## Introdução

O **Conector de Acesso a Dados de Treinamento** permite criar uma experiência de aprendizado sem periféricos que pode ser autônoma ou integrada a uma interface personalizada criada com os **Sites do Adobe Experience Manager (AEM)**. Esse conector ajuda a recuperar e exibir conteúdo de treinamento atualizado para os alunos, com recursos de pesquisa e filtro.

>[!IMPORTANT]
>
>- Este recurso só estará disponível se o Adobe Learning Manager for vendido como um **complemento** para a Adobe Experience Manager.
>- Os dados do curso recuperados através deste conector são atualizados a cada 24 horas
>- Esse conector não é de autoatendimento para criar uma experiência sem periféricos ou baseada em AEM não conectada. Entre em contato com a Adobe para planejar a abordagem correta para o seu caso de uso.

## Como funciona

Quando o conector é ativado, o Adobe Learning Manager expõe um conjunto de APIs públicas que fornecem metadados de treinamento, como cursos, programações de aprendizado e certificados. Você pode usar essas APIs para criar um front-end personalizado de marca que exiba o conteúdo de treinamento e ofereça suporte à funcionalidade de pesquisa e filtro.

## Configurar o conector Acesso a dados de treinamento

Você pode integrar o Adobe Learning Manager ao seu sistema de armazenamento e pesquisa de dados para enviar metadados de treinamento para a AEM Sites ou outras experiências sem periféricos.

Para configurar o conector:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco **Acesso a Dados de Treinamento** e selecione **Conectar**.

   ![](assets/training-data-access-connector1.png)
   _Selecione Conectar para configurar o conector Acesso a Dados de Treinamento_

3. Digite um **Nome da Conexão**.
4. Selecione o **Tipo de Interface**:

   - **Learning Manager nativo**: experiência padrão de logon, disponível por padrão.
   - **Interfaces sem periféricos**: opção premium que expõe APIs públicas para um front-end sem periféricos e não conectado.

   ![](assets/training-data-access-connector2.png)
   _Digite os detalhes necessários para a configuração do conector de Acesso a Dados de Treinamento_

5. Selecione **Conectar**. O Adobe Learning Manager gera a **URL Base** e a **URL CDN** automaticamente. Você usará essas URLs em seu site ou aplicativo personalizado para buscar dados de treinamento.

>[!NOTE]
>
>Os clientes do plano premium recebem um URL de API diferente dos clientes padrão.

## Exportar metadados de treinamento

Para exportar metadados de treinamento:

1. Selecione **Exportar metadados de treinamento** na página do conector.
2. Selecione **Habilitar exportação de metadados de treinamento usando esta conexão** para começar a enviar seus dados de treinamento para o sistema de pesquisa e recuperação.
3. Selecione **Habilitar agendamento** e defina a data de início, a hora e o intervalo.

   ![](assets/training-data-access-connector3.png)
   _Agendar exportação de metadados de treinamento_

4. Selecione **Salvar**.

   - Isso carrega automaticamente todas as imagens do curso, do plano de aprendizado e do certificado para a **CDN**.
   - Ele também exporta os metadados associados para o sistema de pesquisa.

### Exportações sob demanda

- **Executar exportações por demanda:** vá para **Por demanda**, defina a **Data de início** e selecione **Executar** para executar uma exportação quando necessário.
- **Verifique o status da execução:** exiba o progresso e o histórico da exportação na página **Status de Execução**.

## Criar e publicar o site em AEM

Para exibir dados de treinamento em um site sem periféricos ou baseado no AEM Sites:

1. **Instale o pacote AEM** de [Adobe do repositório GitHub](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0) (pré-requisito).
2. Use a **URL Base**, a **URL da CDN**, a **ID de Cliente**, o **Segredo de Cliente** e o **Token de Atualização de Administrador** para criar uma configuração no AEM.
3. Construir o site usando componentes AEM.
4. Publish o site para alunos.
5. Para obter detalhes completos sobre a instalação, consulte [este artigo](https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/integration/aem-sites/adobe-learning-manager-integration-aem) e [este artigo](https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/integration/aem-sites/integrate-aem-learning-manager).

### Experiência do aluno

Quando o site estiver ativo:

- O site exibe todos os **Cursos**, **Caminhos de Aprendizado** e **Certificados** recuperados do Adobe Learning Manager por meio do sistema de pesquisa.
- Os alunos que **não estão conectados** podem navegar e exibir os detalhes do curso.
- Quando um aluno clica para se inscrever em um curso, caminho de aprendizado ou certificado, ele é solicitado a **fazer logon** para concluir a inscrição e iniciar o treinamento.

## Experiência não conectada

A experiência não conectada permite criar uma experiência em tempo real para usuários não conectados. Por exemplo, uma experiência não conectada serve como uma página de aterrissagem para campanhas de marketing para incentivar inscrições.

A experiência não conectada no Adobe Learning Manager pode ser configurada usando o conector **Acesso a dados de treinamento**. O conector fornece as seguintes ofertas:

- Oferta padrão
- Oferta premium

### Oferta padrão

A oferta padrão é criar a versão nativa do Adobe Learning Manager. Os usuários podem criar uma experiência sem periféricos apenas para demonstração e não conectada. A experiência de demonstração sem periféricos é indimensionável e não deve ser usada em um ambiente de produção.

### Oferta premium

A oferta premium ajuda os usuários a criar uma interface sem periféricos, que é configurada pelo conector **Acesso a Dados de Treinamento**. Isso permite que os usuários obtenham dados em tempo real sobre o curso e os detalhes do caminho de aprendizado, como nome, descrição, autor, habilidades, duração etc. Para cenários de aprendizagem combinada, você também obtém limites de vagas em tempo real, vagas ocupadas, limites de listas de espera e contagens de listas de espera. Os clientes podem usar essas APIs para criar recursos de pesquisa e filtro e um resumo completo do curso para alunos não conectados.

Os clientes podem adquirir um plano premium para criar essa experiência não conectada altamente dimensionável.

>[!NOTE]
>
>Entre em contato com a equipe de suporte ou o CSM para adquirir o plano premium.

Depois que um usuário comprar um plano, a equipe de CSM ativará o plano premium para ele. Com o conector Acesso a dados de treinamento, os usuários podem configurar uma experiência não conectada com os recursos mencionados anteriormente.
