---
description: Saiba como integrar o Harvard ManageMentor ao Adobe Learning Manager
jcr-language: en_us
title: Conector do Harvard ManageMentor
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---


# Conector do Harvard ManageMentor no Adobe Learning Manager

## Introdução

O **conector do Harvard ManageMentor** foi projetado para clientes corporativos que usam o Harvard ManageMentor. Ele permite que os alunos descubram e acessem os cursos do Harvard ManageMentor diretamente da Adobe Learning Manager. Depois de conectado, o sistema pode buscar dados de progresso do aluno periodicamente e criar cursos no Adobe Learning Manager com base nos metadados importados.

Este artigo explica como configurar e usar o conector do Harvard ManageMentor no Adobe Learning Manager.

Com essa integração, os administradores de integração podem conectar a conta do Harvard ManageMentor da empresa ao Adobe Learning Manager para importar cursos automaticamente e acompanhar o progresso do aluno, sem criar novos conteúdos de treinamento do zero.

## Pré-requisito

Verifique se o recurso **Migração** está habilitado para sua conta antes de configurar o conector.

## Configurar o conector

Use o conector do Harvard ManageMentor para trazer cursos do Harvard ManageMentor para o Adobe Learning Manager. Depois de conectar sua conta, você pode importar os detalhes do curso e acompanhar o progresso do aluno.

Para configurar o conector:

1. Faça logon como um administrador de integração.
2. Selecione **Harvard ManageMentor** na página inicial.
3. Selecione uma das seguintes opções no bloco do conector:
   - **Introdução**
   - **Conectar**
   - **Gerenciar Conexões**

   ![](assets/harvard-managementor-connector1.png)
   O bloco _Harvard ManageMentor mostra três opções de configuração_

## Criar uma nova conexão

Para criar uma nova conexão:

1. Selecione **Conectar** no bloco **Harvard ManageMentor**.

   ![](assets/harvard-managementor-connector2.png)
   _Selecione Conectar para criar uma nova conexão Harvard ManageMentor_

2. Digite a conexão no campo **Nome da Conexão**.
3. Selecione **Conectar** para criar a conexão.

   ![](assets/harvard-managementor-connector3.png)
   _Digite o nome no campo Nome da Conexão_

## Gerenciar a conexão

Depois de configurar o conector Harvard ManageMentor, você pode gerenciar sua conexão no Adobe Learning Manager. Você pode alterar as configurações de sincronização e executar as sincronizações manualmente ou de acordo com um agendamento.

### Ativar a conexão

Para ativar a conexão:

1. Selecione **Gerenciar Conexões** no bloco **Harvard ManageMentor**.

   ![](assets/harvard-managementor-connector4.png)
   _Gerenciar conexões para configurar e agendar a importação de dados_

2. Selecione a conexão.
3. Selecione **Configurar** no painel de navegação esquerdo.
4. Selecione **Habilitar Conexão** e selecione **Salvar**.

   ![](assets/harvard-managementor-connector5.png)
   _Habilitar o conector Harvard ManageMentor para importar os dados_

### Agendar sincronização

Para agendar a sincronização:

1. Selecione **Gerenciar Conexões** no bloco **Harvard ManageMentor**.
2. Selecione a conexão.
3. Selecione **Configurar** no painel de navegação esquerdo.
4. Selecione **Habilitar agenda** na seção **Sincronização de agenda**.

   ![](assets/harvard-managementor-connector6.png)
   _Agendar a importação de dados do Harvard ManageMentor para o Adobe Learning Manager_

5. Selecione a data e a hora de início em UTC.
6. Digite o número de dias após os quais a sincronização deve se repetir.
7. Selecione **Salvar**.

As configurações de sincronização são salvas. O conector será executado dentro do cronograma e importará dados do Harvard ManageMentor para o Adobe Learning Manager.

## Executar sincronização sob demanda

A opção **Sincronização sob demanda** permite importar manualmente dados do Harvard ManageMentor para o Adobe Learning Manager. Isso é útil quando você deseja atualizar os dados de atividade do aluno imediatamente, sem esperar pela próxima sincronização agendada.

Para executar a importação de dados sob demanda:

1. Selecione **Gerenciar Conexões** no bloco **Harvard ManageMentor**.
2. Selecione a conexão.
3. Selecione **Execução sob Demanda** no painel esquerdo.
4. Selecione **Data de Início**.

   ![](assets/harvard-managementor-connector7.png)
   _Executar a solicitação por demanda para importação imediata de dados do Harvard ManageMentor para o Adobe Learning Manager_

5. Selecione uma das seguintes opções:

   - **Desabilitar o acesso ao Adobe Learning Manager durante a execução**: recomendado se a sincronização puder causar tempo de inatividade.
   - **Habilitar o acesso ao Adobe Learning Manager durante a execução**: recomendado para evitar a interrupção do serviço.
6. Selecione **Executar** para importar todos os dados da data de início até o presente.

### Exibir histórico de execução

A página Status de execução lista todas as execuções de sincronização em ordem. Se uma execução apresentar erros, será exibido um ícone de aviso. Se necessário, você pode verificar o log de erros, corrigir o arquivo CSV e executar a sincronização mais recente novamente.

Para exibir o histórico de execução:

1. Selecione **Status de Execução** no painel esquerdo.
2. Você pode ver as seguintes colunas:
   - **Executar**
   - **Data de Início**
   - **Duração**
   - **Tipo** (Agendado ou Por Demanda)
   - **Status** (Em Andamento ou Concluído)

   ![](assets/harvard-managementor-connector8.png)
   _Exibir o status de execução das importações agendadas e por demanda_

>[!NOTE]
>
>Se você excluir e recriar uma conexão, o histórico de execução das execuções anteriores ainda ficará visível. Você só pode executar novamente a sincronização mais recente.

### Requisito para sincronização

Verifique se os seguintes arquivos estão presentes na pasta FTP do Harvard ManageMentor:

- **hmm12_metadata.csv** Este arquivo contém metadados do curso. Siga o formato de nomeação de arquivo correto.
- **client_hmm12_yyyyMMdd.csv** Este arquivo é o feed de usuário. O formato de data deve corresponder a aaaaMMdd.

**Arquivos de exemplo**

- [Arquivo de metadados do curso para o conector Harvard ManageMentor](https://experienceleague.adobe.com/docs/learning-manager/assets/hmm12-metadata.csv?lang=pt-BR)
- [Arquivo de feed de usuário para o conector Harvard ManageMentor](https://experienceleague.adobe.com/docs/learning-manager/assets/client-hmm12-20170304.csv?lang=pt-BR)
