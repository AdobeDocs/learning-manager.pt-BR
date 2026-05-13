---
description: Saiba como integrar o conector do Adobe Commerce
jcr-language: en_us
title: Conector do Adobe Commerce
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 4%

---


# Conector do Adobe Commerce no Adobe Learning Manager

## Conector do Adobe Commerce

>[!NOTE]
>
>Este recurso só estará disponível se o Adobe Learning Manager for vendido como um **complemento** para a Adobe Experience Manager. O conector também pode ser habilitado para contas de **avaliação**.

O Adobe Learning Manager integra-se ao Adobe Commerce, uma solução de comércio eletrônico extensível e dimensionável que permite fornecer experiências de comércio multicanal para clientes B2B e B2C. Use o conector do Adobe Commerce para conectar o Adobe Learning Manager ao Adobe Commerce e ativar recursos de treinamento pago e comércio eletrônico na sua plataforma de aprendizado.

Quando o conector é ativado, o Learning Manager envia dados de treinamento para a Adobe Commerce, para que os alunos possam comprar cursos, programações de aprendizado ou certificações. O conector também coleta informações de compra para validar transações e conceder aos alunos acesso ao seu treinamento.

## Pré-requisitos

Antes de configurar o conector do Adobe Commerce, verifique o seguinte:

- Habilite o [RabbitMQ](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/start/overview) ou qualquer outro agente de mensagens.
- Habilitar trabalhos [CRON](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/start/overview#cron_consumers_runner).

Para ativá-los, edite os seguintes arquivos:

- .magento.app.yaml
- .magento/services.yaml
- .magento.env.yaml

Outros requisitos de configuração:

- Substitua o limite de opções usando um módulo personalizado. Esta etapa é opcional, mas recomendada para grandes conjuntos de dados.
- Habilite todas as **APIs assíncronas**. Grandes conjuntos de dados de treinamento são exportados de forma assíncrona. Quando o Learning Manager chama as APIs do Adobe Commerce, as solicitações são enfileiradas e processadas por um consumidor que cria produtos no lado do comércio. O processamento assíncrono deve estar habilitado porque não está disponível por padrão no Adobe Commerce.
- Adicione um **link de retorno** ao Learning Manager na página de sucesso do pagamento no Adobe Commerce.
   - Usar esta [URL de retorno](https://learningmanager.adobe.com/app/learner#/postPayment):
- Altere a **indexação** de **Ao Salvar** para **Agendada**. Consulte a [Base de Dados de Conhecimento](https://experienceleague.adobe.com/pt-br/support?support-tab=home#home) para obter mais informações.
- Aplique os **patches** necessários. Consulte [Aplicar documentação de patches](https://experienceleague.adobe.com/pt-br/docs/commerce-cloud-service/start/overview) para obter instruções.
- Configure o **Fastly** para o Adobe Commerce na infraestrutura de nuvem (preparo e produção). Consulte [Configurar o Fastly](https://devdocs.magento.com/cloud/cdn/configure-fastly.html) para obter mais informações.

## Configurar o conector

Para configurar o conector do Adobe Commerce:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco do conector do **Adobe Commerce** e selecione **Conectar**.

   ![](assets/adobe-commerce-connector1.png)
   _Selecione Conectar para configurar o conector do Adobe Commerce_

3. Digite os seguintes detalhes:

   - Nome da conexão
   - Token de acesso
   - URL do Adobe Commerce
   - Código da loja
4. Selecione o Tipo de interface entre as seguintes opções:

   - Learning Manager nativo
   - Personalizado usando o AEM Sites

   ![](assets/adobe-commerce-connector2.png)
   _Digite os detalhes necessários para a configuração do Adobe Commerce_

5. Selecione **Conectar**.

## Definir preços para treinamento

Quando a conexão estiver ativada:

- Os autores podem definir preços para cursos, programações de aprendizado ou certificações.
- Após a publicação, os alunos podem comprar treinamento por meio do Adobe Learning Manager ou de um site personalizado de AEM.

## Fluxo de compra

### Adobe Learning Manager nativo

- Os alunos fazem logon no Adobe Learning Manager para comprar um curso, caminho de aprendizado ou certificado.
- Quando os alunos clicam em Comprar agora, eles são redirecionados para a Adobe Commerce para concluir o pagamento.
- Após o pagamento, os alunos são solicitados a retornar ao Adobe Learning Manager para iniciar o treinamento.
- Os alunos devem fazer logon separadamente na Adobe Commerce para concluir a compra.
- Os alunos recebem e-mails de confirmação de compra do Learning Manager e do Adobe Commerce. Os emails da Adobe Commerce podem ser ativados ou desativados conforme necessário.

### AEM Sites personalizado

Ao usar sites AEM personalizados:

- Os alunos podem navegar e comprar cursos pelo site do AEM.
- O site AEM usa metadados sincronizados do Adobe Learning Manager para pesquisa e exibição.
- Usuários conectados e convidados podem navegar. No entanto, somente os usuários conectados podem comprar.
- Após o logon, os alunos podem adicionar cursos ao carrinho, visualizar detalhes e concluir a compra.

## Exportar cursos para o Adobe Commerce

### Agendar exportação

Para agendar a exportação:

1. Selecione **Exportar metadados de treinamento** e selecione **Configurar agendamento**.
2. Selecione **Habilitar exportação de metadados de treinamento usando esta conexão**.
3. Selecione **Habilitar agendamento** e defina **data de início**, **hora** e **intervalo**.

   ![](assets/adobe-commerce-connector3.png)
   _Habilitar a exportação agendada_

4. Selecione **Salvar**.

### Exportação sob demanda

Depois que os autores definem os preços para o treinamento, o administrador de integração deve exportar os dados do treinamento:

1. Selecione **Exportar metadados de treinamento** e selecione **Sob demanda**.
2. Selecione o intervalo de datas.
3. Selecione **Executar** para exportar.

   ![](assets/adobe-commerce-connector4.png)
   _Criar exportação sob demanda_

4. Após o sucesso, os cursos e caminhos de aprendizado com preço fixo são movidos para o Adobe Commerce para compra.
