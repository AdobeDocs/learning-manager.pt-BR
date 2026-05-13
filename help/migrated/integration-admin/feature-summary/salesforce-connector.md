---
description: Saiba como integrar o conector do Salesforce com o Adobe Learning Manager
jcr-language: en_us
title: Conector do Salesforce
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '2251'
ht-degree: 5%

---


# Conector do Salesforce para Adobe Learning Manager

## Introdução

O conector do Salesforce integra suas contas do Salesforce e do Adobe Learning Manager (ALM), permitindo a importação automatizada de usuários, a sincronização de dados e as exportações de registros de aprendizado. Este guia explica como configurar o conector, gerenciar dados do usuário e integrar insights de aprendizado no Salesforce.

O conector do Salesforce para Adobe Learning Manager permite uma integração tranquila, importando automaticamente usuários, oferecendo suporte ao mapeamento de dados personalizado e exportando registros de aprendizado para o Salesforce.

Ao seguir este guia, você aprenderá como:

- Estabeleça conexões seguras entre o Salesforce e o Adobe Learning Manager.
- Configurar processos automatizados de importação de usuários do Salesforce.
- Mapeie campos do Salesforce para atributos do Adobe Learning Manager de maneira eficaz.
- Exporte registros de aprendizado de volta para o Salesforce para obter relatórios abrangentes.
- Configure a filtragem e o agendamento para sincronização de dados direcionados.

## O que é o conector do Salesforce?

O conector do Salesforce é uma ferramenta de integração eficiente que cria uma ponte perfeita entre o CRM do Salesforce e o Adobe Learning Manager. Esse conector elimina a entrada manual de dados, sincronizando automaticamente as informações do usuário, os dados de contato e os registros de aprendizado entre as duas plataformas.

## Principais recursos

### Mapeamento de atributos

Isso ajuda a criar links flexíveis entre os campos do Salesforce e os atributos de usuário do Adobe Learning Manager. Você pode mapear campos padrão como Nome, E-mail e Gerente para atributos correspondentes no Learning Manager. O conector também é compatível com campos personalizados em ambas as plataformas, inclui validação de campo obrigatória para manter a precisão dos dados e permite salvar configurações de mapeamento para reutilização em importações futuras.

### Importação automatizada de usuário

Ele simplifica a integração e a manutenção de usuários por meio de processos automatizados de importação que eliminam o gerenciamento manual de arquivos CSV.

- Importação direta de objetos de usuário do Salesforce sem formatos de arquivo intermediários.
- Sincronização em tempo real das alterações do perfil do usuário.
- Suporte para usuários padrão e contatos externos.

### Agendamento automático de importações

Configurar agendas de sincronização automatizadas que mantêm a moeda dos dados sem intervenção manual. Selecione entre as opções de agendamento de intervalo diário, semanal ou personalizado.

- Configuração de fuso horário para organizações globais.
- Programação de pico/fora de pico para otimizar o desempenho do sistema.

### Filtro de usuário

- Aplique critérios de filtragem para direcionar populações específicas de usuários e otimizar a eficiência da sincronização de dados.
- Filtragem baseada em funções para programas de treinamento direcionados.
- Filtragem geográfica ou baseada em local para implementações regionais
- Filtragem de campo personalizado usando critérios e fórmulas do Salesforce.

## Pré-requisitos

Antes de configurar o conector do Salesforce, verifique se o seu ambiente atende aos seguintes requisitos:

- [URL da organização do Salesforce](https://myorg.salesforce.com)
- Credenciais de logon de administrador para o Salesforce e o Adobe Learning Manager.
- Administrador do sistema ou permissões equivalentes no Salesforce.
- Conta ativa do Adobe Learning Manager com licenciamento apropriado

## Configurar o conector do Salesforce

O conector do Salesforce no Adobe Learning Manager permite que os administradores de integração automatizem a sincronização dos dados do usuário e dos registros de aprendizado entre o Salesforce e o Adobe Learning Manager.

Para criar um conector do Salesforce:

1. Faça logon como um administrador de integração.
2. Selecione **Salesforce** e selecione **Conectar**.

   ![](assets/salesforce-connector1.png)
   _Página de conectores do Adobe Learning Manager mostrando o conector do Salesforce com o botão Conectar realçado_

3. Digite a URL da sua organização do Salesforce e selecione **Conectar**. Isso levará você à página de logon do Salesforce.

   ![](assets/salesforce-connector2.png)
   _Formulário de logon do Salesforce exibindo campos de entrada de nome de usuário e senha_

4. Faça logon com seu nome de usuário e senha. Conclua quaisquer etapas de autenticação adicionais, como verificação de dois fatores ou respostas a perguntas de segurança.

   Após a autenticação bem-sucedida, a página de visão geral do conector é exibida, confirmando a conexão estabelecida entre os sistemas.

   ![](assets/salesforce-connector3.png)
   _Página de visão geral do conector do Salesforce mostrando o status da conexão bem-sucedida_

### Mapear atributos

Entender o mapeamento de atributos O mapeamento de atributos cria a conexão essencial entre os campos de dados do Salesforce e os atributos do usuário do Adobe Learning Manager, garantindo que as informações do usuário sejam transferidas com precisão entre os sistemas.

#### Requisitos de Mapeamento

- Todos os campos obrigatórios do Adobe Learning Manager devem ser mapeados para os campos correspondentes do Salesforce
- As configurações de mapeamento são reutilizáveis e persistentes em várias importações

Para mapear os atributos:

1. Navegue até a página de visão geral do conector do Salesforce.
2. Selecione **Usuários Internos** e selecione **Configurar Mapeamento**.
3. Selecione uma das seguintes opções:

   - **Usuários:** contas padrão do Salesforce usadas por funcionários ou membros internos da equipe
   - **Contatos:** indivíduos externos, como clientes, parceiros ou fornecedores.

4. Corresponda os campos ativos do Adobe Learning Manager com as colunas do Salesforce na página de mapeamento. O campo **Gerente** deve ser mapeado para um campo de email de gerente de usuário.

   ![](assets/salesforce-connector4.png)
   _Interface de mapeamento de campos exibindo atributos de usuário do Adobe Learning Manager à esquerda e seleções do menu suspenso de campos do Salesforce à direita_

5. Selecione **Salvar** para concluir o mapeamento.

## Importar usuários e contatos

O conector do Salesforce permite que o Adobe Learning Manager se conecte com a sua conta do Salesforce e importe automaticamente os usuários com base na sua configuração.

- **Usuários internos**: funcionários e funcionários com contas de usuário do Salesforce.
- **Contatos Externos**: clientes, parceiros, fornecedores e outras partes interessadas externas.
- **Importações Mistas**: combinação de usuários e contatos em um único processo de sincronização.
- **Importações Filtradas**: sincronização direcionada com base em critérios específicos.

O conector do Salesforce permite que o Adobe Learning Manager se conecte com a sua conta do Salesforce e importe automaticamente os usuários com base na sua configuração.

O conector oferece suporte à importação de contatos, além de usuários padrão do Salesforce. Isso ajuda a estender os programas de treinamento a colaboradores externos, como clientes ou parceiros.

Para importar contatos:

1. Selecione **Salesforce** na página **Conectores**.
2. Selecione **Importar usuários internos** na página de conexão.

   ![](assets/salesforce-connector5.png)
   _Página do conector do Salesforce com a opção Importar usuários internos realçada_

3. Selecione **Contatos** na página **Importar usuários**.
4. Selecione **Sim** para a opção **Filtrar Contatos antes de importar**. **
5. Configure as seguintes opções:

   - **Escolha a coluna Contatos:** selecione o campo que deseja importar para o Adobe Learning Manager.
   - **Especificar valores:** selecione os valores que representam o campo selecionado.
   - Mapear os atributos do Salesforce com os campos do Adobe Learning Manager

   ![](assets/salesforce-connector6.png)
   _Configuração de importação de contato mostrando opções de filtragem e mapeamento de campo_

6. Selecione **Salvar**.
7. Se você selecionar **Não. Importe todos os Contatos**; você pode mapear os campos diretamente sem filtrar os contatos.

## Exportar registros de aprendizado

A funcionalidade de exportação de registros de aprendizado permite compartilhar dados do Adobe Learning Manager com o Salesforce, criando recursos abrangentes de relatório e análise que combinam os resultados do aprendizado com os dados do CRM.

### Objetos personalizados no Salesforce

Antes de exportar registros de aprendizado do Adobe Learning Manager, crie objetos personalizados no Salesforce. Objetos personalizados permitem armazenar dados específicos para as necessidades da sua organização ou do setor. Para obter mais informações, exiba [objetos personalizados do Salesforce](https://trailhead.salesforce.com/en/content/learn/modules/data_modeling/objects_intro).

### Instalar pacotes da Adobe Learning Manager

O Adobe fornece pacotes pré-criados que criam os objetos personalizados necessários:

- [Pacote 1](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPJ): objetos e campos de aprendizado principais
- [Pacote 2](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPT): objetos de análise de aprendizado estendidos
- [Pacote 3](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPi): objetos adicionais de relatório e integração

>[!IMPORTANT]
>
>Substitua [test.salesforce.com](https://acrobat.adobe.com/home/test.salesforce.com) nas URLs do pacote pelo domínio real da sua organização do Salesforce.

### Processo de instalação do pacote

Para instalar os pacotes:

1. Faça logon no Salesforce como administrador.
2. Navegue até cada URL do pacote no navegador.
3. Siga o assistente de instalação para cada pacote e conceda as permissões apropriadas aos usuários que acessarão os dados de aprendizado.
4. Renomeie os nomes dos objetos personalizados no Salesforce.
5. Selecione os eventos e clique em **Salvar**.

>[!NOTE]
>
>Verifique se o acesso do administrador do sistema foi concedido a todos os campos ativos adicionados após a instalação do pacote.

### Exportar registros

Para exportar os registros para o Salesforce:

1. Selecione **Exportar registros unificados** na página de conectores do **Salesforce**.
2. Selecione os eventos dentre os seguintes:

   - Adição de novo usuário
   - Inscrição no treinamento
   - Conclusão do treinamento
   - Inscrição de habilidade
   - Conclusão de habilidade

3. Selecione **Objeto de contato** na opção **Evento de vínculos com**. Isso garante que os usuários existentes no Adobe Learning Manager, mas não no Salesforce, sejam criados no Salesforce.

   ![](assets/salesforce-connector7.png)
   _Configuração de exportação de registro de aprendizado mostrando a seleção de eventos e as opções de vinculação_

>[!NOTE]
>
>Você pode criar várias conexões em uma única conta. Cada conexão pode oferecer suporte a até três objetos personalizados no Salesforce. Para criar várias conexões para a mesma conta do Salesforce, até três pacotes podem ser instalados. O número de pacotes instalados deve corresponder ao número de conexões desejadas.

## Configuração do aplicativo Salesforce

O Adobe Learning Manager fornece um pacote do aplicativo Salesforce. Depois de instalados e configurados na instância do Salesforce, os usuários de vendas podem acessar e concluir o treinamento diretamente no portal do Salesforce. O aplicativo permite que os usuários descubram novos cursos, visualizem recomendações personalizadas e consumam conteúdo sem sair do Salesforce.

### Acessar o aplicativo Salesforce

Para configurar o aplicativo Salesforce:

1. Faça logon como um administrador de integração.
2. Selecione **Aplicativos** e selecione **Aplicativos em destaque**.
3. Selecione **Salesforce**.

   ![](assets/salesforce-connector8.png)
   _Página de aplicativos da Adobe Learning Manager mostrando a seção Aplicativos em destaque com o bloco de aplicativo do Salesforce realçado_

4. Observe a **ID do Aplicativo** e o **Segredo do Cliente** mostrados na caixa de texto de descrição.

   ![](assets/salesforce-connector9.png)
   _Página de detalhes do aplicativo Salesforce no Adobe Learning Manager mostrando a ID do aplicativo e o Segredo do cliente na caixa de descrição_

5. Selecione **Aprovar** para habilitar o aplicativo.

### Gerar tokens de acesso

Para gerar tokens de acesso:

1. Navegue até **Recursos do desenvolvedor** no Adobe Learning Manager.
2. Selecione **Tokens de acesso para teste e desenvolvimento**.
3. Na seção **Obter código OAuth**, digite a ID do cliente (ID do aplicativo) e o escopo deve ser definido como **admin:read,admin:write**.
4. Selecione **Enviar**.
5. Na seção **Obter Token de Atualização**, digite a **ID de Cliente** e o **segredo do Cliente**.
6. Selecione **Enviar** e anote o token de atualização e o token de acesso.

>[!IMPORTANT]
>
>Anote o token de atualização e o token de acesso gerados.

### Criar uma conta do Salesforce

Se você não tiver uma conta do Salesforce, siga estas etapas para criar uma usando o mesmo endereço de email da conta da Adobe Learning Manager. Você pode usar a edição Developer ou Enterprise. É importante se inscrever usando a mesma ID de email associada à sua conta da Adobe Learning Manager.

1. Vá para a [página de inscrição do Salesforce Developer](https://developer.salesforce.com/signup).
2. Digite os detalhes necessários usando o mesmo endereço de email usado para sua conta da Adobe Learning Manager.
3. Verifique sua caixa de entrada e sua conta por meio do email enviado pelo Salesforce.
4. Defina sua senha e faça logon no Salesforce.
5. Após fazer logon, anote o URL do Salesforce (por exemplo, https://yourorg.lightning.force.com) para uso durante a configuração.

### Instalar o pacote do Adobe Learning Manager

Esta seção aborda a instalação do pacote Adobe Learning Manager em seu ambiente do Salesforce.

>[!IMPORTANT]
>
>O aplicativo Adobe Learning Manager é compatível somente com a exibição Lightning do Salesforce. Verifique se a experiência Lightning está ativada antes de continuar.

#### Instalar o pacote

Para instalar o pacote:

1. Abra a [URL do pacote do Adobe Learning Manager](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WOQ).
2. Digite seu nome de usuário e senha na página de logon.
3. Selecione **Instalar**. Na página de instalação, mantenha a opção Instalar somente para administradores selecionada. Não a altere.
4. Selecione **Concluído**. Você será guiado até a página **Pacotes Instalados**, na qual poderá ver o pacote instalado pela Adobe Learning Manager.

Você será redirecionado para a página Pacotes instalados, onde é possível verificar a instalação do pacote da Adobe Learning Manager

#### Configurar o aplicativo

Para configurar o aplicativo:

1. Selecione **Inicializador de Aplicativos** (ícone de grade de 9 pontos ao lado da Instalação)
2. Procure por Adobe Learning Manager.
3. Para configurar o aplicativo, selecione **Configurar**.
4. Selecione **Novo** e adicione os seguintes detalhes:

   - **Config:** insira um nome de sua escolha.
   - **ClientID**: insira o valor obtido na primeira seção.
   - **ClientSecret:** insira o valor obtido na primeira seção.
   - **RefreshToken:** insira o valor obtido na primeira seção.
   - **LearningManagerBaseURL:** a URL do site onde o Adobe Learning Manager está hospedado.

### Configuração de site remoto

O Salesforce requer configurações de site remoto para permitir a comunicação com serviços externos, como o Adobe Learning Manager.

#### Adicionando configurações de site remoto

Para adicionar configurações de site remoto:

1. No Salesforce, selecione **Configurar** no canto superior direito.
2. Selecione **Configuração** no canto superior direito da página.
3. Pesquise **Configurações de Site Remoto** em **Localização Rápida**.
4. Selecione **Novo Site Remoto**.
5. Insira os detalhes:

   - **Nome do Site Remoto:** digite um nome de sua escolha (por exemplo, Adobe Learning Manager).
   - **URL do Site Remoto:** Digite a URL onde o Adobe Learning Manager está hospedado.
6. Selecione **Salvar**.

### Configurar notificações

Configure notificações para manter os usuários informados sobre atividades de aprendizado e atualizações.

#### Criar notificações personalizadas

Para ativar as notificações:

1. Selecione **Configuração** no canto superior direito.
2. Pesquise **Notificações personalizadas** e selecione **Novas**.
3. Digite os seguintes detalhes:

   - **Nome da Notificação Personalizada:** LearningManagerNotification
   - **Nome da API:** LearningManagerNotification

4. Selecione **Desktop** e **Dispositivos móveis** como canais suportados.
5. Selecione **Salvar**.

#### Ativar notificações por push em dispositivos móveis (opcional)

Para usuários que desejam receber notificações em dispositivos móveis:

Para ativar as notificações push para dispositivos móveis, siga as etapas abaixo:

1. Instale o aplicativo Salesforce para dispositivos móveis em seu celular.
2. Faça logon no aplicativo usando suas credenciais.
3. Vá para **Configuração** e selecione **Configurações de Entrega de Notificação**.
4. Adicione o Salesforce para iOS e Android.

### Configuração e permissões do usuário

Esta seção aborda a configuração de acesso e permissões de usuário para o aplicativo Adobe Learning Manager no Salesforce.

#### Noções básicas sobre perfis de usuário

O aplicativo Adobe Learning Manager é compatível com vários perfis de usuário que correspondem às funções no Adobe Learning Manager:

- Administrador
- Administrador de Integração
- O professor
- Aluno
- Perfis personalizados (conforme necessário)

#### Atribuir ou criar perfis de usuário

Você pode usar perfis existentes ou criar perfis personalizados para usuários do Adobe Learning Manager:

**Usar perfis existentes**

1. Navegue até a **Instalação** e selecione **Usuários**.
2. Selecione **Perfis**.
3. Selecione um perfil que se alinhe com as funções dos seus usuários
4. Atribua esse perfil aos usuários durante a instalação do pacote.

**Criar perfis personalizados**

1. Navegue até **Configuração** e selecione **&#x200B; usuários. &#x200B;**
2. Selecione **Perfis**.
3. Clique em **Novo Perfil**.
4. Crie um perfil personalizado com base em um existente, personalizado para os usuários do Adobe Learning Manager.

#### Configurar o perfil

Para configurar um perfil:

1. Após instalar o pacote, selecione **Configurar** e selecione **Novo**.
2. Digite os seguintes detalhes:

   - **Nome de Configuração**
   - **ClientID**
   - **ClientSecret**
   - **URLBaseDoLearningManager**
   - **Desabilitar Redirecionamento**

>[!NOTE]
>
>Verifique se o aplicativo Adobe Learning Manager está ativado para que todos os alunos o visualizem.

#### Definir permissões de usuário

Selecione os usuários e atribua as permissões necessárias para acessar o aplicativo Adobe Learning Manager.

#### Atualizar configurações do perfil

1. Selecione um perfil (por exemplo, Perfil Padrão) e selecione **Editar**.
2. Na seção **Configurações do Aplicativo Personalizado**, marque a caixa para o **Adobe Learning Manager** para tornar o aplicativo acessível.
3. Na seção **Configurações da guia personalizada**, defina a **Página inicial do aluno** como **Padrão em**.
4. Selecione **Salvar** para aplicar as alterações.

Os alunos com os perfis atribuídos agora podem acessar o aplicativo Adobe Learning Manager no Salesforce.

Você configurou com êxito o conector do Salesforce para Adobe Learning Manager. Agora, os usuários podem acessar seu conteúdo de aprendizado diretamente no Salesforce, melhorando a adoção e o envolvimento com os programas de treinamento da sua organização.
