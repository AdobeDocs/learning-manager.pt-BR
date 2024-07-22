---
title: Transição do Gerenciador de FTP do Adobe
description: O Adobe Learning Manager suporta um novo conector usando o protocolo SFTP da família AWS Transfer. Você pode substituir qualquer cliente FTP de código aberto pelo gerenciador de FTP do Adobe.
exl-id: c5674e61-9e3d-45e5-9f3c-e0aa15ec2dac
source-git-commit: 566716404c1cff34108e39014e14416d65088a80
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 68%

---

# Transição do Gerenciador de FTP do Adobe

O Adobe Learning Manager dá suporte a um novo conector usando o protocolo SFTP da família AWS Transfer.

Você pode substituir qualquer cliente FTP de código aberto pelo gerenciador de FTP do Adobe.

Alguns clientes FTP recomendados pelo AWS estão listados [aqui](https://docs.aws.amazon.com/transfer/latest/userguide/transfer-file.html):

* FileZilla (Windows, macOS e Linux)
* OpenSSH (macOS e Linux) – Observação: esse cliente só funciona com servidores habilitados para o protocolo de transferência de arquivos (SFTP) do Secure Shell (SSH).
* WinSCP (somente Microsoft Windows)
* Cyberduck (Windows, macOS e Linux)

## Configurar o conector FTP baseado no AWS

Você deve configurar o novo conector FTP baseado no AWS no administrador de integração.

![imagem de conectores](assets/alm-ftp.png)
*Selecione a opção de FTP*

Depois de se conectar, você pode ver a página Detalhes da conexão.

![página de detalhes da conexão](assets/connection-name.png)
*Exibir a página de detalhes da conexão*

Há três opções de autenticação:

### Criar autenticação gerando novas chaves SSH

Você pode gerar a chave SSH no seu próprio sistema se desejar. Clique em Gerar chave SSH.

A chave privada é baixada no computador e a chave pública é salva em nossos serviços. Depois que você clica em Conectar, o usuário do FTP é criado usando as chaves pública e privada como autenticação.

Você criou uma conexão FTP.

### Criar autenticação usando chaves SSH existentes

Se você já tiver uma chave SSH, cole a chave pública no campo **[!UICONTROL Chave Pública do FTP]** e clique em Conectar.

![Chaves SSH](assets/ssh-keys.png)
*Colar as chaves*

### Criar autenticação básica usando uma senha

Esse é o mecanismo básico de autenticação. Selecione a primeira opção, **[!UICONTROL Criar autenticação básica usando uma senha]**. Insira a senha e clique em **[!UICONTROL Conectar]**.

Isso cria uma conexão.

## O que vem a seguir

### Configurar o cliente FTP

Configure a conexão em um cliente FTP (recomendado na seção anterior) com as chaves baixadas ou chaves ou senha existentes.

### Exportação de teste de amostra

* No cliente FTP, altere o local do FTP do ExaVault para o novo local do FTP. O novo domínio é `http://almftp.adobelearningmanager.com/`.
* Você também deve incluir na lista de permissões o IP `18.195.107.67`.
* Após a autenticação, você deve carregar e baixar alguns arquivos de amostra para e do novo local do FTP usando clientes FTP externos ou scripts de automação.
* Você deve transferir dados do local antigo para o novo.
* A política de retenção de dados para o conector permanece a mesma. O ExaVault também deu suporte a algumas políticas de retenção de dados além da política oficial. Essas políticas de retenção de dados não estarão disponíveis para o novo conector. Verifique se o conector usa qualquer retenção de dados além das políticas que oficialmente têm suporte.

### O que acontece com os projetos de migração

| Status | Recomendação |
|---|---|
| Nova migração | Não é possível iniciar novas migrações do FTP antigo. Você deve usar o novo FTP para as novas migrações. Para obter mais suporte sobre isso, entre em contato com a Equipe de sucesso do cliente. |
| Migração em andamento | Criar um sprint: você pode continuar usando o FTP antigo, mas recomendamos usar o novo FTP. Entre em contato com a equipe de Sucesso do cliente para verificar se há algum sprint que não possa ser deslocado. |
| Migração fechada | Nenhuma ação. |

## Conectar-se ao Adobe Learning Manager usando o cliente Filezilla FTP

1. Conecte-se ao novo Conector FTP do ALM. Clique em Conectar.

   ![conectar imagem](assets/connect-client.png)
   *Conectar ao novo Conector FTP do ALM*

1. Para conectar-se por meio da autenticação básica por senha, insira o nome do domínio, o nome do usuário do FTP e configure uma senha que corresponda aos critérios de validação de senha. Clique em Conectar. A nova conexão FTP será criada e poderá ser acessada por meio de qualquer cliente SFTP.

   ![configurações de ftp](assets/connect-settings.png)
   *via autenticação básica via senha*

1. Instale qualquer cliente SFTP, por exemplo, File Zilla. Inicie o File Zilla e clique em Open Site Manager no canto superior esquerdo.

   ![Cliente SFTP](assets/sftp-client-install.png)
   *Conectar via cliente SFTP*

1. Clique em **[!UICONTROL Novo site]** para criar um novo site. Renomeie o site conforme necessário.

   ![novo site](assets/new-site.png)
   *Criar um site*

1. Mapeie os detalhes da página de credenciais do conector.

   * Selecionar protocolo como &#39;SFTP - SSH File Transfer Protocol&#39;
   * Hospedar como domínio FTP
   * Tipo de logon como &#39;Solicitar senha&#39;
   * Usuário como nome de usuário do FTP

1. Clique em Conectar.

   ![credenciais](assets/connector-credentials.png)
   *Insira as credenciais*

   >[!NOTE]
   >
   >Execute esta etapa no cliente File Zilla.

1. Insira a senha.

   (Opcional) Marque a caixa de seleção Lembrar senha para lembrar a senha.

   ![senha](assets/password.png)
   *Insira a senha*

   (Opcional) Marque a caixa de seleção **[!UICONTROL Sempre confiar neste host]** para confiar no host.

1. Clique em OK.

   ![chave de host desconhecida](assets/unknown-host-key.png)
   *Chave do host*

1. Verifique o status e o progresso da conexão no topo.

   A metade esquerda é o site local e a metade direita é o site remoto.

   Para mover arquivos de local para remoto e vice-versa:

   * Você pode arrastar e soltar arquivos.
   * Clique duas vezes no arquivo.

   ![status da conexão](assets/connection-status-progress.png)
   *Verifique o status da conexão*

Você pode alterar e atualizar o tipo de autenticação a qualquer momento.

Outras formas de autenticação são através de chaves SSH:

Cole sua chave pública na caixa de texto para usar as chaves SSH existentes. Clique em Conectar/Salvar.

Para gerar novas chaves SSH, clique no botão &#39;**[!UICONTROL Gerar chave SSH]**&#39;. A chave privada será baixada. Clique em **[!UICONTROL Conectar/Salvar]**.

![gerar chave ssh](assets/ssh-key.png)
*Gerar chave SSH*

Mapeie os detalhes. Selecione o tipo de logon como arquivo de chave. Selecione o arquivo de chave privada.

Clique em **[!UICONTROL Conectar]**.

## O que acontece depois que o ExaVault é descontinuado

Depois que o ExaVault for descontinuado, todos os projetos de migração existentes, que estiverem em andamento, passarão para o novo FTP como local de origem. Em seguida, você deve configurar o novo conector FTP e continuar o processo de migração.

## Recomendações para migrar sprints

Ao criar um projeto de migração, a Adobe recomenda que você o crie usando o novo conector SFTP do AWS para evitar a migração do sprint do Exavault para o AWS em um estágio posterior.

Se uma migração estiver em andamento, feche o sprint atual que usa o Exavault como uma fonte de dados. Crie a conexão SFTP do AWS, teste a configuração e entre em contato com a equipe de Sucesso do Cliente para mudar para a nova fonte de dados SFTP do AWS. Depois de mudar, crie um novo sprint no mesmo projeto de migração. As pastas do sprint são criadas no novo local, e você pode carregar os CSVs de migração para continuar a atividade.

**Casos em que um projeto de migração não pode ser fechado**

* O mapeamento da ID do curso é feito no projeto atual para cursos que são migrados de sistemas externos herdados para o Adobe Learning Manager. Você só pode fazer isso se quiser atualizar os mesmos cursos no mesmo projeto. Depois de fechar o projeto, você não pode modificar seus detalhes.
* Para projetos de migração baseados em API, em que você não deve fechar um projeto.