---
description: Saiba como integrar o conector do Power BI ao Adobe Learning Manager
jcr-language: en_us
title: Conector do Power BI
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 4%

---


# Power BI no Adobe Learning Manager

## Introdução

O Power BI permite integrar o Adobe Learning Manager ao Microsoft Power BI (licença comercial) para que você possa analisar, visualizar e compartilhar seus dados de aprendizado.

Com essa integração, o administrador de integração pode exportar automaticamente conjuntos de dados em tempo real, como transcrições do aluno, habilidades do usuário e relatórios de atividades xAPI, diretamente para um espaço de trabalho do Power BI selecionado.

Depois de conectado, você pode usar todos os recursos do Power BI para criar painéis e relatórios personalizados. Isso ajuda sua organização a obter insights mais profundos sobre o progresso do aluno, as conquistas de habilidades e a eficácia do treinamento e a tomar decisões informadas com base em dados de aprendizado em tempo real.

>[!NOTE]
>
>O Adobe Learning Manager oferece suporte à integração somente com a versão comercial do Microsoft Power BI. A integração com a versão da Government Cloud não é compatível.

## Pré-requisitos

- Somente há suporte para o Microsoft Power BI com uma **licença comercial**.
- Verifique se você tem permissão para criar aplicativos e espaços de trabalho do Power BI.
- Obtenha seu **Nome do Locatário**, **ID do Cliente de Aplicativos**, **Segredo do Cliente de Aplicativos** e **ID do Espaço de Trabalho** (opcional).

## Configurar o conector do Power BI

Para conectar o ALM ao Power BI:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco do conector **Power BI** e selecione **Conectar**.

   ![](assets/power-bi-connector1.png)
   _Selecione Conectar para configurar o conector do Power BI_

3. Digite os seguintes detalhes:

   - ID do cliente
   - Segredo do cliente
   - Nome do locatário
   - ID do Espaço de Trabalho (opcional)

   ![](assets/power-bi-connector2.png)
   _Digite os detalhes necessários para configurar o Power BI_

4. Selecione **Conectar**.

## Registrar o aplicativo Power BI

Para registrar o aplicativo Power BI:

1. Vá para [Registrar o Power BI](https://app.powerbi.com/embedded setup).
2. Selecione **Incorporar à sua organização** e faça logon na sua conta da Microsoft.
3. Digite um nome para o aplicativo.
4. Selecione **Aplicativo Web do servidor** em **Tipo de aplicativo**.
5. Na seção **Redirecionar URL**, selecione **Usar uma URL personalizada** e digite [esta URL](https://learningmanager.adobe.com/ctr/app/azure/_callback): (Substitua o domínio, se necessário, para o seu ambiente.)
6. No campo **URL Inicial**, digite [esta URL](https://learningmanager.adobe.com/).
7. Na seção **Permissões**, selecione **Ler todos os conjuntos de dados** e **Ler e gravar todos os conjuntos de dados**.
8. Contate o administrador do Power BI para obter o **Nome do Locatário**.
9. Se você não tiver uma ID de espaço de trabalho, crie um espaço de trabalho no Power BI (requer o Power BI Pro) e copie a ID do URL.
10. Selecione **Registrar aplicativo** e salve a **ID de Cliente** e o **Segredo de Cliente** para uso posterior.

>[!NOTE]
>
>Se precisar reautorizar a conexão mais tarde, crie um novo aplicativo Power BI e use o URL de redirecionamento correto para o seu ambiente.

## Exportar relatórios para o Power BI

Depois de configurar a conexão, você pode exportar estes relatórios:

- **Transcrições do aluno**
- **Habilidades do usuário**
- **Relatórios de Atividades da xAPI**
- **Relatórios unificados** (uma combinação de vários relatórios)

### Transcrição do aluno

#### Agendar exportações

1. Selecione **Transcrições do aluno** no painel esquerdo.
2. Selecione **Habilitar Agendamento** na página Exportar.
3. Selecione a **data de início** e a **hora**.
4. Defina o **intervalo** para a frequência de repetição da exportação (diária, semanal etc.).

   ![](assets/power-bi-connector3.png)
   _Habilitar a exportação de agendamento para transcrição do aluno_

5. Selecione **Salvar**.

#### Exportação sob demanda

- Você pode gerar relatórios manualmente especificando a **data de início** e executando uma exportação por demanda.
- O relatório incluirá dados da data especificada até o presente.

### Habilidades do usuário

#### Agendar exportações

1. Selecione **Habilidades do usuário** no painel esquerdo.
2. Selecione **Habilitar Agendamento** na página Exportar.
3. Selecione a **data de início** e a **hora**.
4. Defina o **intervalo** para a frequência de repetição da exportação (diária, semanal etc.).

   ![](assets/power-bi-connector4.png)
   _Habilitar a exportação agendada do relatório de habilidades do usuário_

5. Selecione **Salvar**.

#### Exportação sob demanda

- Você pode gerar relatórios manualmente especificando a **data de início** e executando uma exportação por demanda.
- O relatório incluirá dados da data especificada até o presente.

### Gerenciar relatórios de atividades da xAPI

**Instruções xAPI** também podem ser exportadas para o Power BI.

#### Configurar exportações xAPI

1. Selecione **Exportar relatório de atividades da xAPI**.
2. Selecione **Configuração** no painel esquerdo.

   - Preencha os campos de caminho JSON para corresponder às colunas CSV.
   - Selecione **Adicionar** para incluir mais caminhos.
   - Use **Editar** para atualizar campos.
3. Selecione **Salvar**.

#### Agendar exportações

1. Selecione **Configurar Agenda**.
2. Selecione **Habilitar exportação de instruções xAPI usando esta conexão**.
3. Defina a **data de início**, a **hora** e o **intervalo**.
4. Selecione **Salvar**.

#### Exportação sob demanda

1. Selecione **Sob Demanda**.
2. Especifique a **data de início**.
3. Selecione **Executar**.

>[!NOTE]
>
>Se algumas instruções xAPI no Armazenamento de registros de aprendizado (LRS) não tiverem caminhos JSON configurados, seus valores aparecerão como N/A no Power BI.

#### Exibir status da execução

- Use **Status de Execução** para exibir o histórico de exportações, incluindo hora de início, duração e status.
- Um ícone de aviso indica execuções com falha. Clique no link para baixar relatórios de erros como .CSV.

### Relatórios unificados

**Relatórios unificados** combinam dados de:

- Transcrição do aluno
- Gamificação
- Relatório de feedback
- Logon/Acesso
- Habilidade do usuário
- Relatório do usuário
- Relatório de treinamento

Isso ajuda a criar painéis de controle mais avançados mesclando dados no Power BI.

#### Criar configuração de relatório unificada

1. Selecione **Relatórios Unificados** e depois selecione **Configuração**.
2. Digite um nome exclusivo no campo **Nome do Conjunto de Dados**.
3. Selecione um ou mais relatórios que deseja incluir neste conjunto de dados em **Selecionar Relatórios para Exportação de Dados**.

   - Transcrição do aluno
   - Logon/Acesso
   - Relatório de treinamento
   - Gamificação
   - Habilidade do usuário
   - Relatório de feedback
   - Relatório do usuário
4. Use o campo **Adicionar filtros de grupo de usuários** para selecionar quais dados de grupos de usuários você deseja exportar. Por padrão, **Todos os Usuários** está selecionado.
5. Use o campo **Adicionar Filtros do Catálogo de Conteúdo** para filtrar relatórios por catálogo de conteúdo.
6. A tabela de filtros mostra quais relatórios dão suporte aos filtros de **Grupo de usuários**, **Catálogo** ou **Tempo**.

   ![](assets/power-bi-connector5.png)
   _Criar uma configuração para relatórios unificados_

7. Depois de selecionar relatórios e filtros, selecione **Salvar** no canto superior direito.

#### Filtrar transcrições do aluno por status

- **Todos:** todos os registros no intervalo de datas
- **Concluído:** apenas atividades de aprendizado concluídas
- **Em andamento:** apenas atividades em andamento
- **Não iniciado:** exclui registros ainda não iniciados
- **Não inscrito:** Inclui registros não inscritos

## Baixar Modelos do Power BI

O Adobe fornece modelos de Power BI prontos para ajudar você a começar rapidamente.

- Baixe modelos, importe seus relatórios e personalize conforme necessário.
- Use modelos para criar painéis atraentes sem começar do zero.

## Configurações relacionadas ao Caminho de aprendizado

A forma como os **Caminhos de Aprendizado** aparecem em seus relatórios depende das suas configurações de administrador:

- **Conexões Existentes:**

   - Se o **Caminho de Aprendizado** estiver desabilitado, nenhuma linha ou coluna relacionada será incluída.
   - Se ativado, o relatório inclui o Caminho de Aprendizado (Nível superior) para alunos inscritos.

- **Novas Conexões:**

   - Se o Caminho de aprendizado estiver desativado, as colunas mostrarão:

      - **Caminho Incorporado:** Nome do Programa de Aprendizado.
      - **ID do Caminho Inserido:** ID do Programa de Aprendizado.
      - **ID do curso incorporado:** IDs de cursos no Caminho de Aprendizado.
   - Se ativada, a coluna **Tipo** usa o Caminho de Aprendizado (Nível Superior) onde relevante.
   - Para novas conexões, as alterações se aplicam após 30 dias.

### Onde ver seus dados**

Todos os dados exportados aparecem como conjuntos de dados em sua conta Power BI. Use-os para criar painéis e visualizações personalizados.
