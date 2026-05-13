---
description: Saiba como integrar o conector do Workday com o Adobe Learning Manager
jcr-language: en_us
title: Conector do Workday
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 1%

---


# Conector do Workday no Adobe Learning Manager

## Introdução

O **Workday** é um sistema baseado em nuvem que ajuda as organizações a gerenciar funcionários e dados financeiros. É usado principalmente em tarefas de RH, como contratação, folha de pagamento e acompanhamento de desempenho. Quando conectado ao Adobe Learning Manager, permite a sincronização automática de dados do usuário e da habilidade entre as duas plataformas.

O conector do Workday permite que você integre facilmente o Adobe Learning Manager com o locatário do Workday da sua organização. Essa integração permite a sincronização automática de dados e habilidades do usuário entre os dois sistemas, melhorando a precisão dos dados e reduzindo o esforço manual.

## Principais benefícios

- Importe usuários do Workday para o Adobe Learning Manager.
- Mapeie atributos entre o Workday e o Adobe Learning Manager.
- Exportar habilidades do usuário do Adobe Learning Manager para o Workday.
- Agendar tarefas de sincronização de dados para serem executadas automaticamente.

## Pré-requisitos

Antes de configurar o conector do Workday, obtenha os seguintes detalhes do administrador do Workday:

- URL do host
- ID do locatário
- Nome de usuário
- Senha

## Configurar o conector do Workday

Você pode configurar o conector do Workday no Adobe Learning Manager para permitir que você importe dados do usuário do Workday, exporte habilidades do usuário de volta para o Workday e agende sincronizações automatizadas para manter os dois sistemas atualizados.

Para configurar o conector do Workday:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco **Workday** e selecione **Conectar**.

   ![](assets/workday-connector1.png)
   _Configurar o conector do Workday para importar e exportar os dados_

3. Digite os seguintes detalhes da conexão:
   - **Nome da conexão**: um nome de sua escolha para a conexão.
   - **Url do Host**: Fornecida pelo Administrador do Workday.
   - **Locatário**: identificador interno do administrador do Workday.
   - **Nome de usuário e senha**: o administrador do Workday cria um usuário de sistema integrado (ISU) com os privilégios de segurança necessários e o compartilha com o administrador de integração.

   ![](assets/workday-connector2.png)
   _Adicione os detalhes necessários para configurar o conector do Workday_

4. Selecione **Conectar** para concluir a instalação.

>[!NOTE]
>
>Você pode configurar várias conexões do Workday em sua conta.

## Importar usuários do Workday

### Mapear atributos

Você pode usar o conector do Workday para importar usuários ativos do seu locatário do Workday para o Adobe Learning Manager. Essa integração simplifica o gerenciamento de usuários ao manter os registros de funcionários sincronizados. Além do Workday, o Adobe Learning Manager também oferece suporte a importações de usuários de outras fontes de dados, como FTP e Salesforce.

Antes de importar usuários, você deve mapear atributos de usuário entre o Workday e o Learning Manager.

1. Navegue até a página **Visão geral** no conector do Workday.
2. Selecione **Usuários internos** na seção **Importar**.

   ![](assets/workday-connector3.png)
   _Selecione Usuários Internos para mapear os atributos do usuário_

3. Use a opção **Mapear atributos** para vincular campos entre os dois sistemas:
   - Na coluna **Adobe Learning Manager**, selecione o atributo Adobe Learning Manager correspondente.
   - Na coluna **Workday**, use o menu suspenso para selecionar o atributo Workday correspondente.

   ![](assets/workday-connector4.png)
   _Mapeando os atributos do Workday com campos do Adobe Learning Manager_

   >[!NOTE]
   >
   >No momento, o Adobe Learning Manager oferece suporte à importação de até **69 atributos de usuário** do Workday. Você pode habilitar campos adicionais usando o recurso **Campos Ativos** no Adobe Learning Manager. Para adicionar atributos personalizados do Workday, entre em contato com seu Gerente de Conta de Sucesso do Cliente (CSAM).

4. Marque a caixa de seleção **Excluir trabalhadores temporários** para evitar a importação de trabalhadores temporários.
5. Aplique filtros se necessário, por exemplo, para importar usuários sob gerenciadores específicos.

>[!IMPORTANT]
>
>Certifique-se de que a UUID, o endereço de e-mail e o nome do funcionário sejam exclusivos. Valores incorretos ou duplicados podem causar falhas de integração.

## Atributos do Workday compatíveis

Lista de atributos compatíveis do Workday:

```
wd:User_ID wd:Worker_ID manager wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Formatted_Name wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Formatted_Name wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:First_Name wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Last_Name wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:First_Name wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Last_Name wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.@wd:Formatted_Address wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Postal_Code wd:Personal_Data.wd:Contact_Data.wd:Email_Address_Data.0.wd:Email_Address wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Country_Region_Descriptor wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Formatted_Phone wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Country_ISO_Code wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:International_Phone_Code wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Phone_Number wd:Personal_Data.wd:Primary_Nationality_Reference.wd:ID.1.$ wd:Personal_Data.wd:Gender_Reference.wd:ID.1.$ wd:Personal_Data.wd:Identification_Data.wd:National_ID.0.wd:National_ID_Data.wd:ID wd:Personal_Data.wd:Identification_Data.wd:Custom_ID.0.wd:Custom_ID_Data.wd:ID wd:User_Account_Data.wd:Default_Display_Language_Reference.wd:ID.1.$ wd:Role_Data.wd:Organization_Role_Data.wd:Organization_Role.0.wd:Organization_Role_Reference.wd:ID.1.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Position_Title wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Title wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Name wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.@wd:Formatted_Address
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Classification_Reference.wd:ID.1.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Group_Reference.wd:ID.1.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Work_Space__Reference.wd:ID.1.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Family_Reference.0.wd:ID.1.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Profile_Name wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Profile_Reference.wd:ID.1.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Reference.wd:ID.2.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Worker_Type_Reference.wd:ID.1.$ wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.@wd:Formatted_Address wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Management_Level_Reference.wd:ID.1.$ wd:Employment_Data.wd:Worker_Status_Data.wd:Active wd:Employment_Data.wd:Worker_Status_Data.wd:Active_Status_Date wd:Employment_Data.wd:Worker_Status_Data.wd:Hire_Date wd:Employment_Data.wd:Worker_Status_Data.wd:Original_Hire_Date wd:Employment_Data.wd:Worker_Status_Data.wd:Retired wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date wd:Employment_Data.wd:Worker_Status_Data.wd:Terminated wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$ wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$ wd:Qualification_Data.wd:Education.0.wd:School_Name wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Company wd:Management_Chain_Data.wd:Worker_Supervisory_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID Primary Work Email wd:Organization_Type_Reference_Cost_Center_ID wd:Organization_Type_Reference_Cost_Center_Name wd:Organization_Type_Reference_Company wd:Organization_Subtype_Reference_Department
wd:Organization_Subtype_Reference_Division wd:Universal_ID wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Descriptor wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Reference.wd:ID.2.$ wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Municipality
```

## Exportar habilidades do usuário para o Workday

Você pode exportar todas as habilidades ativas do usuário do Adobe Learning Manager para o Workday. As habilidades retiradas não são exportadas.

>[!IMPORTANT]
>
>- Não tente exportar habilidades de várias contas do Adobe Learning Manager para a mesma conta do Workday simultaneamente.
>- Se várias contas da Adobe Learning Manager usarem a mesma conta da Workday, verifique se os nomes de habilidades são consistentes em todas as contas para evitar conflitos.

### Configurar uma exportação agendada

Para configurar as exportações agendadas:

1. Selecione **Habilidades do Usuário** e selecione **Configurar Agendamento** na página **Visão Geral do Workday**.

   ![](assets/workday-connector5.png)
   _Selecione Habilidades de Usuário para agendar a exportação_

2. Marque a caixa de seleção **Habilitar exportação de habilidades do usuário usando esta conexão**.
3. Selecione **Habilitar agendamento**.
4. Defina a data de início, a hora e o intervalo de recorrência.

   ![](assets/workday-connector6.png)
   _Configurar a exportação de agendamento no conector do Workday_

5. Selecione **Salvar** para aplicar o agendamento.

### Exportação sob demanda

Para criar exportações por demanda:

1. Selecione **Sob demanda** na página **Visão geral do Workday**.
2. Digite a data inicial a partir da qual o relatório deve começar.
3. Selecione **Executar** para executar o relatório.

### Exibir status da execução

1. Vá para **Status de Execução**.
2. Exiba o status de todas as tarefas e baixe relatórios de erros conforme necessário.

## Agendando tarefas de sincronização

Você pode configurar o conector para executar tarefas de sincronização de dados automaticamente:

- Agende importações diárias de usuários do Workday para o Learning Manager.
- Agende exportações periódicas de habilidades do usuário para o Workday.

>[!NOTE]
>
>O agendamento garante que os registros e os dados de habilidades do usuário estejam sempre atualizados em ambos os sistemas.

## Pontos a serem lembrados

- O campo UUID preenchido no Workday não pode ser excluído por Administradores do LMS voltados para o cliente.
- A função **Limpar Usuário** só dá suporte a até 50 usuários por execução. Tenha cuidado ao importar usuários com UUIDs.
- As habilidades são mapeadas no nível do item de habilidade no Workday, usando o nome e o nível da habilidade do Adobe Learning Manager.
