---
description: Saiba como integrar o conector Marketo Engage com o Adobe Learning Manager
jcr-language: en_us
title: Conector do Marketo Engage
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 3%

---


# conector do Marketo Engage no Adobe Learning Manager

## Introdução

O conector do Marketo Engage permite que o Adobe Learning Manager se integre perfeitamente com o Marketo Engage, uma plataforma de automação de marketing. Essa integração ajuda os profissionais de marketing a rastrear e agir nos dados de comportamento do aluno do Adobe Learning Manager sincronizando-os com o banco de dados do Marketo.

O conector Marketo Engage permite a sincronização perfeita de dados entre os dois sistemas e que os profissionais de marketing usem os dados da atividade de aprendizado para criar campanhas de marketing direcionadas.

O conector do Marketo Engage permite:

- Adicionar ou atualizar leads automaticamente no banco de dados do Marketo Engage quando os usuários são adicionados ao Adobe Learning Manager.
- Sincronize os comportamentos de aprendizado do usuário, como inscrições no curso, conclusões, atribuições de habilidades e conclusões de habilidades, como objetos personalizados no Marketo.
- Crie campanhas dinâmicas no Marketo usando esses dados, aproveitando recursos como **Smart Lists**.

Essa integração ajuda os profissionais de marketing a atingir públicos com base em sua jornada de aprendizado no Adobe Learning Manager.

## Principais recursos

- Criação automática de leads e atualizações com base nos usuários do Adobe Learning Manager.
- Exportar a atividade de aprendizado (inscrições, conclusões, conquistas de habilidades) como objetos personalizados para o Marketo.
- Programe ou acione exportações sob demanda.
- Suporte a relatórios unificados, incluindo:
   - Relatório do usuário
   - Transcrição de aprendizado
   - Relatório de habilidades do usuário

## Pré-requisitos

Antes da integração, certifique-se de que sua conta do Marketo oferece suporte à criação de esquemas por meio de APIs.

Você precisará dos seguintes detalhes para criar a conexão:

- **Nome da Conexão**
- **ID do cliente**
- **Segredo do cliente**
- **Domínio Marketo Engage**

>[!NOTE]
>
>Você pode obter a ID do cliente e o segredo do cliente no aplicativo Marketo Engage em **LaunchPoint** e o domínio da seção **Serviços Web**.

## Configurar o conector

Para configurar o conector do Marketo Engage:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco **Marketo Engage** e selecione **Conectar**.

   ![](assets/marketo-engage-connector1.png)
   _Selecione Conectar para configurar o conector de Marketo Engage_

3. Digite as credenciais necessárias

   - Nome da conexão
   - ID do cliente
   - Segredo do cliente
   - Domínio do Marketo Engage

   ![](assets/marketo-engage-connector2.png)
   _Digite os detalhes necessários para o conector de Marketo Engage_

4. Selecione **Conectar** para estabelecer a conexão.

## Eventos e acionadores de campanhas

Você pode acionar exportações de dados para o Marketo Engage com base nos seguintes eventos:

- Um novo usuário foi adicionado ao Adobe Learning Manager.
- Um usuário está inscrito em um curso.
- Um usuário conclui um curso.
- Um usuário está inscrito em uma habilidade.
- Um usuário completa uma habilidade.

Estes eventos podem ser exportados **sob demanda** ou **de forma agendada**.

## Mapeamento de colunas

O Marketo usa dois bancos de dados:

- **Banco de Dados de Clientes Potenciais** - para registros de usuário (clientes potenciais)
- **Banco de Dados de Objeto Personalizado** - para registros de atividade e eventos personalizados

Para mapear campos entre Adobe Learning Manager e Marketo:

1. Os campos do **Relatório do Usuário** do Adobe Learning Manager são exibidos em uma coluna.
2. Os **campos Marketo** correspondentes são listados na coluna adjacente.
3. Mapeie os campos apropriados do Learning Manager para o Marketo para criar e atualizar leads.
4. Após o mapeamento, todos os usuários exportados aparecem como clientes potenciais no Banco de Dados de Clientes Potenciais do Marketo.

Os relatórios exportados na seção **Objetos personalizados do Marketo** são prefixados com “cp_”.

## Eventos de exportação suportados

Você pode exportar os seguintes eventos relacionados ao usuário para sua instância do Marketo Engage:

- Novo usuário adicionado
- Metadados do usuário atualizados
- Atividade do usuário atualizada
- Inscrição no treinamento
- Autoinscrição
- Conclusão de habilidade

Essas exportações ajudam a impulsionar o envolvimento e personalizar campanhas de divulgação usando os dados da atividade de aprendizado.
