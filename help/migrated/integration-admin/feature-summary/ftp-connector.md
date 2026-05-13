---
description: Saiba como integrar o conector FTP com o Adobe Learning Manager
jcr-language: en_us
title: Conector FTP
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '2008'
ht-degree: 0%

---


# Conector FTP no Adobe Learning Manager

## Introdução

O FTP (File Transfer Protocol) é um protocolo de rede padrão usado para transferir arquivos entre um cliente e um servidor pela Internet ou por uma rede local. Permite aos usuários fazer upload, baixar e gerenciar arquivos em um servidor remoto. Para transferências de arquivos seguras, variantes como SFTP (SSH File Transfer Protocol) e FTPS (FTP Secure) são comumente usadas. O FTP é amplamente adotado em ambientes corporativos para automatizar a troca de dados entre sistemas, como a sincronização de dados do usuário ou de treinamento entre plataformas Adobe Learning Manager e externas.

Este documento oferece orientação passo a passo para administradores de integração sobre a configuração e o uso do conector FTP no Adobe Learning Manager. O conector FTP permite a troca automática de dados entre o Learning Manager e os sistemas externos usando protocolos de transferência de arquivos seguros.

Você aprenderá como configurar conexões FTP, mapear campos de dados, agendar importações ou exportações automatizadas de usuários e monitorar a atividade de sincronização. Este guia oferece suporte à integração tranquila e segura com plataformas de aprendizado externas ou sistemas de RH. Você pode importar usuários internos e instruções xAPI e exportar habilidades do usuário, transcrições do aluno e dados xAPI.

Os administradores de integração devem gerar arquivos CSV para migrar usuários, dados de usuários ou conteúdo de aprendizado e carregá-los em pastas designadas na conta FTP do Adobe Learning Manager. O Adobe Learning Manager lê, mescla e importa os dados com base em um agendamento definido.

Realize essas operações sob demanda ou configurando uma programação que atenda às necessidades da sua organização.

## Benefícios da integração FTP

- Reduz o esforço manual e os erros humanos no gerenciamento de dados.
- Integra dados de várias fontes externas simultaneamente.
- Oferece suporte a operações de dados programadas e sob demanda.
- Permite o mapeamento detalhado de campos entre diferentes formatos do sistema.

## Pré-requisitos

Antes de configurar o conector FTP, verifique se o seu ambiente atende aos seguintes requisitos:

- Função de administrador de integração com permissões de conector FTP.
- Conexão estável com a Internet, com largura de banda adequada para transferências de arquivos.
- Configuração do firewall permitindo o tráfego FTP nas portas necessárias.
- Acesso de porta necessário, dependendo dos requisitos de segurança

### Permissão e acesso

Verifique se você tem o seguinte:

- Acesso para gerar e gerenciar chaves SSH (se estiver usando a autenticação SSH).
- Permissão para criar e atualizar arquivos CSV nas pastas FTP especificadas.

## Principais recursos

### Importação e exportação de dados com o conector FTP

O conector FTP no Adobe Learning Manager simplifica a troca de dados entre sistemas externos e a sua conta do Adobe Learning Manager. Ele oferece suporte a operações programadas e sob demanda de importação ou exportação, reduzindo o esforço manual e garantindo informações precisas e atualizadas.

Esse método permite a integração com vários sistemas externos. Se sistemas diferentes gerarem arquivos CSV separados, o Adobe Learning Manager mesclará os dados e os importará como um único lote.

### Importar dados para o Adobe Learning Manager

_Importação de dados do usuário_

Carregue arquivos CSV estruturados em pastas FTP designadas para importar dados internos do usuário. O Adobe Learning Manager lê e processa esses arquivos com base em seu agendamento configurado para manter as informações do usuário atualizadas.

_Integração de várias fontes_

Se você estiver usando vários sistemas externos, cada sistema pode gerar seu próprio arquivo CSV. O Adobe Learning Manager mescla os arquivos e processa os dados como um único lote, facilitando o gerenciamento de registros de usuário de diferentes fontes.

_Importação de xAPI_

O conector também oferece suporte a instruções xAPI (Experience API). Importe-os de sistemas de aprendizado de terceiros para rastrear e relatar atividades de aprendizado em várias plataformas.

### Exportar dados do Adobe Learning Manager

_Exportação de dados do aluno_

Exportar dados do usuário, como progresso de habilidade, conclusões de curso e métricas de desempenho, para um local FTP designado. Use esses dados para relatórios ou análises externos.

_Transcrições do aluno_

Gere e exporte transcrições detalhadas com conclusões de cursos, certificações e programações de aprendizado para oferecer suporte à conformidade e à verificação de credencial.

### Mapeamento de atributos

Mapeie colunas de arquivos CSV para atributos de usuário do Adobe Learning Manager. Você pode reutilizar e atualizar a configuração de mapeamento conforme necessário, facilitando a adaptação às alterações nos requisitos de dados.

### Programação e automação

Programe tarefas de importação e exportação para serem executadas em intervalos regulares, como diariamente, semanalmente ou em intervalos personalizados. Isso garante atualizações de dados consistentes sem esforço manual.

## Configurar o conector FTP

Configure o conector FTP para estabelecer a sincronização segura de dados entre o Adobe Learning Manager e sistemas externos.

Para configurar o conector FTP:

1. Faça logon como um administrador de integração.
2. Selecione **FTP do Adobe Learning Manager** e selecione **Introdução**.

   ![](assets/ftp-connector1.png)
   _Interface do conector FTP do Adobe Learning Manager mostrando o botão Introdução_

3. Selecione **Avançar** para continuar com o assistente de configuração do conector FTP.

   ![](assets/ftp-connector2.png)
   _A página Configuração exibe o botão Próximo para continuar com a configuração do conector FTP_

### Configurar a autenticação

O Adobe Learning Manager oferece suporte a três métodos de autenticação, cada um com diferentes níveis de segurança e requisitos de complexidade.

#### Autenticação básica

Este método usa credenciais tradicionais de nome de usuário e senha para acesso ao FTP. Embora mais simples de implementar, ele fornece menos segurança do que as alternativas baseadas em SSH.

1. Selecione **Criar autenticação básica usando uma senha**.
2. Digite o nome de usuário e a senha do FTP nos campos fornecidos. Verifique se as credenciais foram inseridas corretamente antes de continuar.

   ![](assets/ftp-connector3.png)
   _Formulário de autenticação por FTP com campos para nome de usuário e senha, mostrando a opção de autenticação básica selecionada_

#### Autenticação de chave SSH existente

Use este método se já tiver estabelecido pares de chaves SSH para autenticação segura.

1. Selecione **Criar autenticação usando chaves SSH existentes**.
2. Copie e cole o conteúdo da chave pública no campo de texto fornecido. Verifique se o formato da chave pública está correto (normalmente começa com ssh-rsa ou ssh-ed25519).

   ![](assets/ftp-connector4.png)
   _Interface de autenticação de chave SSH com campo de texto para entrada de chave pública_

#### Gerar uma nova chave SSH

Use esta opção para criar um novo par de chaves SSH especificamente para esta conexão FTP.

1. Selecione **Criar autenticação gerando uma nova chave SSH**.
2. Selecione **Gerar chave SSH** para criar um novo par de chaves. Baixar e armazenar com segurança a chave privada gerada. A chave pública será configurada automaticamente para a conexão FTP.

   ![](assets/ftp-connector5.png)
   _Tela de geração de chave SSH com o botão Gerar chave SSH e outras opções de configuração_

## Conectar ao FTP usando FileZilla

FileZilla é uma ferramenta opcional para o gerenciamento de conexões FTP. Ele pode ser usado quando você precisa carregar arquivos manualmente, verificar estruturas de diretório ou solucionar problemas de conexão fora dos processos automatizados do Adobe Learning Manager.

### Instalação e configuração do FileZilla

FileZilla é um cliente FTP gratuito de código aberto que fornece uma interface amigável para operações de transferência de arquivos.

Para conectar seu FTP ao FileZilla:

1. Baixe e instale o FileZilla do [site oficial](https://filezilla-project.org/).
2. Abra o **FileZilla**.
3. Selecione **Arquivo** e selecione **Gerenciador de Sites**.
4. Selecione **Novo Site**.
5. Digite os seguintes detalhes:
   - **Domínio FTP:** o endereço do servidor FTP ao qual você deseja se conectar, por exemplo, ftp.example.com. Você pode localizar seu domínio host na página do Conector FTP no Adobe Learning Manager.
   - **Porta:** a porta FTP padrão é 21. No entanto, o Adobe Learning Manager usa a Porta 22 para conexões seguras.
   - **Nome de Usuário do FTP:** O nome de logon necessário para acessar o servidor FTP.
   - **Senha de FTP:** A senha vinculada ao seu nome de usuário de FTP.
6. Selecione **Conectar**.
7. Depois de conectado, você pode transferir arquivos arrastando e soltando entre os painéis local (esquerda) e remoto (direita).

## Usar o conector FTP no Adobe Learning Manager

### Importar usuários internos usando o conector FTP

A funcionalidade de importação de usuário permite a sincronização automatizada de dados de funcionários de sistemas de RH e outras fontes externas no Adobe Learning Manager.

### Mapear atributos

O mapeamento de atributos cria a conexão entre seus dados externos e a estrutura de dados compatível do Adobe Learning Manager, garantindo que os dados sejam inseridos nos campos corretos. Essa etapa é obrigatória.

Para mapear atributos:

1. Selecione **Usuários internos** na página **Conector FTP**.
2. Selecione **Mapeamento de Colunas**.
3. Na página **Mapear atributos**:
   - O **lado esquerdo** mostra os campos obrigatórios no Adobe Learning Manager.
   - O **lado direito** mostra os nomes de colunas CSV. Inicialmente, este lado contém listas suspensas vazias.
   - Selecione **Escolher CSV** para carregar um arquivo CSV de exemplo. Isso preenche o menu suspenso do lado direito com os nomes de coluna do seu CSV. Consulte [este artigo](https://experienceleague.adobe.com/pt-br/docs/learning-manager/using/integration/migration-manual#csv).
   - Mapeie cada campo do Adobe Learning Manager com a coluna CSV correspondente.

   ![](assets/ftp-connector6.png)
   _Interface de mapeamento de atributos mostrando os campos do Adobe Learning Manager à esquerda e as listas suspensas de colunas CSV à direita_

4. Selecione **Salvar** para concluir o mapeamento.

Após salvar, a conta configurada aparece como **fonte de dados** no aplicativo do administrador. Os administradores podem agendar uma importação ou acionar uma sincronização manual.

### Importar instruções da xAPI

A importação de instruções da xAPI permite o rastreamento detalhado da atividade de aprendizado, trazendo dados de aprendizado externos para o Adobe Learning Manager.

_Configurar origem_

A configuração da origem da xAPI estabelece a conexão entre os sistemas de aprendizado externos e o controle de atividades da Adobe Learning Manager.

Para configurar uma origem:

1. Navegue até a seção de configuração da xAPI.
2. Selecione **Adicionar uma nova Configuração** na lista de configurações.

   ![](assets/ftp-connector7.png)
   _Página de gerenciamento de configuração com o botão Adicionar uma nova Configuração e a lista de configurações existente_

3. Digite o **Nome** e o **Nome do Arquivo de Origem**:
   - **Nome:** identificador descritivo para esta origem xAPI (por exemplo, Integração do LMS ou Sistema de Treinamento Externo).
   - **Nome do Arquivo de Origem:** o nome do arquivo exato que será carregado na pasta FTP (deve corresponder exatamente, incluindo a extensão do arquivo).

   ![](assets/ftp-connector8.png)
   _Formulário de configuração mostrando o campo de nome e o campo de nome do arquivo de origem_

4. Selecione **Salvar** para criar a configuração básica.

_Adicionar filtros (opcional)_

Os filtros permitem importar seletivamente instruções xAPI com base em critérios específicos.

Para adicionar um filtro para origem:

1. Selecione **Filtro** no painel esquerdo.
2. Selecione **Adicionar novo filtro**.

   ![](assets/ftp-connector9.png)
   _Página de configuração de filtro com o botão Adicionar novo filtro_

3. Configure o seguinte:
   - **Nome:** Nome descritivo para a regra de filtro.
   - **Condição:** Operador de comparação (igual, contém, maior que, etc.).

   ![](assets/ftp-connector10.png)
   _Caixa de diálogo de criação de filtro mostrando campo de nome e condições_

4. Selecione **Adicionar novo filtro** para adicionar mais filtros.
5. Selecione **Salvar** ou **Excluir** conforme necessário na coluna **Ações**.
6. Após adicionar filtros, selecione **Salvar**.

_Mapear campos_

Para mapear os campos:

1. Selecione **Mapeamento** no painel esquerdo.
2. Na página **Mapeamento**, você verá os caminhos de campos JSON à esquerda e os nomes de colunas CSV à direita.

   ![](assets/ftp-connector11.png)
   _Adicionar um mapeamento para a origem da importação_

3. Por padrão, mapeie os seguintes campos obrigatórios:
   - **ator.mbox:** representa o endereço de email do aluno (o ator que está realizando
a ação). Ele identifica exclusivamente quem fez a atividade.
   - **verb.id:** é o identificador da ação executada pelo aluno, como
concluído, tentado ou aprovado. Especifica a ação do aluno.
   - **object.id:** indica o objeto de aprendizado ou a atividade com a qual o aluno interagiu,
como um curso, módulo ou caminho de aprendizado.
4. Selecione **Adicionar um novo Mapeamento** para mapear campos adicionais.
5. Para cada campo, selecione o **tipo de dados** apropriado (cadeia de caracteres, número, booleano ou data).
6. Selecione **Salvar** para concluir o mapeamento.

## Agendar a importação

A programação automatizada garante a sincronização consistente dos dados sem intervenção manual,
manutenção dos registros da atividade de aprendizado atual.

Para agendar a importação:

1. Selecione **Configurar agendamento** no painel esquerdo.

   ![](assets/ftp-connector12.png)
   _Página de configuração de agendamento mostrando as opções de habilitação e controles de tempo_

2. Selecione **Habilitar importação de instruções xAPI usando esta conexão.**
3. Selecione **Habilitar agendamento** para configurar importações automáticas.
4. Defina os seguintes parâmetros:
   - **Data de Início:** Quando as importações agendadas devem começar.
   - **Hora:** Hora do dia da execução da importação.
   - **Repetir após:** Com que frequência as importações devem ser executadas (intervalos diários, semanais, personalizados).
5. Selecione **Salvar**.

## Executar sob demanda (opcional)

A execução sob demanda fornece importações de dados imediatas fora das operações programadas regulares.

Quando usar importações por demanda:

- Teste de novas configurações antes do agendamento
- Processamento de atualizações de dados urgentes ou com prazo apertado
- Manipular correções ou migrações de dados ocasionais. Solução de problemas de importação

Para importar manualmente instruções da xAPI:

1. Selecione **Sob Demanda** no painel esquerdo.
2. Selecione **Executar**.

   ![](assets/ftp-connector13.png)
   _Página de execução sob demanda com o botão Executar_

## Exibir status da execução

O monitoramento de status permite o gerenciamento pró-ativo de operações de importação e a rápida identificação de problemas.

Para exibir o status da execução:

1. Selecione **Status de Execução** para ver uma lista de todas as execuções de importação.
2. A página mostra:

   - **Data de Início:** quando a operação de importação começou.
   - **Duração:** tempo total necessário para o processamento.
   - **Tipo de importação:** se a importação foi agendada ou por demanda.
   - **Status Atual:** Informações de status em tempo real.
      - **Em andamento:** importação atualmente em execução
      - **Concluído:** conclusão bem-sucedida com contagens de registros
      - **Falha:** erro com informações de diagnóstico

## Solucionar problemas de importação

A seção de status de execução fornece um resumo abrangente de todas as tarefas de importação em ordem cronológica, permitindo que os administradores monitorem as operações e identifiquem problemas rapidamente.

Indicadores de status:

- **Êxito:** importação concluída sem erros.
- **Sinal de Aviso:** indica falhas ou problemas durante a execução.
- **Em andamento:** operação de importação em execução no momento.
- **Pendente:** importação agendada, mas ainda não iniciada.

Quando ocorrem falhas, o sistema exibe indicadores de aviso ao lado das execuções de importação com falha. Selecione o link Relatório de erros para baixar relatórios de erros detalhados.
