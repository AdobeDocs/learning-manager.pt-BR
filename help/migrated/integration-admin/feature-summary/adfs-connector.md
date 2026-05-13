---
description: Saiba como integrar o conector do ADFS com o Adobe Learning Manager
jcr-language: en_us
title: Conector ADFS
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 3%

---


# Conector ADFS no Adobe Learning Manager

## Introdução

O Conector do ADFS no Adobe Learning Manager permite que você se integre com o Microsoft Azure Ative Diretory usando os Serviços de Federação do Ative Diretory (ADFS). Essa integração permite a sincronização automática dos dados do usuário do Azure AD para o Learning Manager. Com recursos como mapeamento de atributos, filtragem de usuários e importações agendadas, o conector ajuda a simplificar o gerenciamento de usuários e garante que os dados do aluno permaneçam precisos e atualizados. É especialmente útil para organizações que dependem do AD FS para o gerenciamento centralizado de identidade e acesso.

## Pré-requisitos

Antes de configurar o conector do ADFS no Adobe Learning Manager, conclua as seguintes etapas no Portal do Azure:

- Registrar um aplicativo
- Gerar um segredo do cliente
- Definir permissões de API

### Registrar um aplicativo no Azure

Para registrar um aplicativo no Azure:

1. Faça logon no [Portal do Azure](https://portal.azure.com/).
2. Navegue até o **Azure Ative Diretory**.
3. Selecione **Adicionar** e selecione **Registro de aplicativo**.
4. Digite um nome para o aplicativo e selecione **Registrar**.

### Gerar um segredo do cliente

Para criar um segredo do cliente:

1. No aplicativo recém-registrado, vá para **Certificados e Segredos**.
2. Selecione **Novo segredo do cliente**.
3. Adicione uma descrição e defina a expiração para **24 meses**.
4. Salve o **valor do segredo do cliente** em um local seguro.

### Definir permissões de API

Para adicionar permissão de API:

1. Selecione **Permissões de API** e selecione **Adicionar uma permissão**.
2. Selecione **Microsoft Graph** e selecione **Permissões do aplicativo**.
3. Pesquise e selecione as seguintes permissões:

   - **Diretory.Read.All** - Ler dados do diretório
   - **User.Read.All** - Ler os perfis completos de todos os usuários
4. Selecione **Adicionar permissões**.
5. Conceda **consentimento do administrador** para as permissões.

## Configurar o conector do ADFS no Learning Manager

Você pode configurar o conector do ADFS no Adobe Learning Manager para importar dados do usuário do ADFS, exportar habilidades do usuário de volta para o ADFS e agendar sincronizações automatizadas para manter os dois sistemas atualizados.

Para configurar o conector do ADFS:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco do conector do **AD FS**.
3. Selecione **Conectar**.

   ![](assets/adfs-connector1.png)
   _Selecione Conectar para configurar o conector ADFS_

### Inserir detalhes da conexão

Na página de configuração do ADFS:

1. Digite os seguintes detalhes:

   - Nome da conexão
   - ID do cliente
   - Segredo do cliente

   ![](assets/adfs-connector2.png)
   _Digite os detalhes da configuração para conectar o ADFS_

2. Selecione **Conectar**.
3. O Adobe Learning Manager buscará e preencherá automaticamente a **ID do locatário** e o **Domínio primário** do seu portal do Azure.

## Importando usuários do AD FS

### Mapear atributos

- Os administradores de integração podem mapear atributos do ADFS para atributos agrupáveis correspondentes no Adobe Learning Manager.
- Este mapeamento é uma configuração única e é reutilizado para todas as importações subsequentes do usuário.
- É possível modificar o mapeamento de atributos a qualquer momento, se necessário.

### Importação automatizada de usuário

- O Adobe Learning Manager extrai automaticamente dados do usuário do ADFS em intervalos programados.
- Isso ajuda a manter os registros do usuário sincronizados entre os sistemas.

### Como filtrar usuários

- Os administradores podem aplicar filtros para limitar usuários importados.
- Por exemplo, importe somente usuários sob gerentes ou departamentos específicos.
