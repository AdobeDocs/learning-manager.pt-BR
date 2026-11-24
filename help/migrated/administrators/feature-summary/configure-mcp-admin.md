---
description: Crie, gerencie e desative servidores do Protocolo de contexto de modelo no Adobe Learning Manager para que os clientes de IA possam acessar com segurança o treinamento dos alunos.
jcr-language: en_us
title: Configurar um servidor de Protocolo de Contexto de Modelo
exl-id: 3130c36d-e63e-4cd6-b0ed-561371b9b261
source-git-commit: 89aa1b5ab02eed8a61507ab162fcbbd384e6c5fc
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 1%
---

# Configurar um servidor de Protocolo de Contexto de Modelo

## Visão geral

Cada servidor MCP registra um aplicativo cliente OAuth 2.0 que autoriza os clientes de IA a agir em nome dos alunos. Como administrador, você cria o servidor e copia suas credenciais e, em seguida, as fornece ao administrador do cliente AI, que conclui a conexão. Você pode revisitar um servidor a qualquer momento para editá-lo, refinar suas descrições de ferramentas, copiar suas credenciais ou excluí-lo.

>[!NOTE]
>
>O servidor fornece acesso de leitura somente aos usuários com a função de aluno.

## Criar o servidor MCP

1. Faça logon no Adobe Learning Manager como administrador.
2. Navegue até **IA no aprendizado** > **Servidores MCP**.
3. Selecione **Novo Servidor MCP**.
4. Insira os detalhes do servidor, incluindo uma descrição.

   * **Nome do servidor:** insira um nome de até 50 caracteres.
   * **Descrição:** insira uma breve descrição de até 150 caracteres.
   * **URL:** insira a URL da empresa ou do aplicativo.
   * **Domínios de redirecionamento:** insira o domínio de cada cliente AI que se conectará, como [http://\*.chatgpt.com](https://encoded-592c9deb-987b-4562-aa3c-9fa3d37d83e9.uri/http%3a%2f%2f*.chatgpt.com) ou [http://\*.claude.ai](https://encoded-592c9deb-987b-4562-aa3c-9fa3d37d83e9.uri/http%3a%2f%2f*.claude.ai). Esse campo é obrigatório.

   ![](assets/2_Administrator--Configure-MCP-image1.png)

5. Selecione **Próximo**.
6. Na página **Ferramentas disponíveis**, revise as ferramentas do aluno que o servidor expõe. Forneça descrições detalhadas, contextuais e orientadas por finalidade para ferramentas MCP.Forneça descrições contextuais detalhadas de cada ferramenta. Uma descrição precisa ajuda os clientes compatíveis com MCP a selecionar e chamar a ferramenta apropriada. Inclua a finalidade da ferramenta, as tarefas compatíveis, as entradas esperadas e os casos de uso típicos.

   ![](assets/2_Administrator--Configure-MCP-image2.png)

   Selecione **Exibir** para cada ferramenta para exibir as instruções para determinar quando a ferramenta está selecionada e como a ferramenta responde.

   ![](assets/2_Administrator--Configure-MCP-image3.png)

7. Selecione **Credenciais de cliente** no painel de navegação esquerdo.
8. Copie a **URL do Ponto de Extremidade do MCP**, a **ID do Cliente** e a **Chave Secreta**. Selecione **Copiar** ao lado de cada valor.

   ![](assets/2_Administrator--Configure-MCP-image4.png)

9. Selecione **Fechar**.

>[!NOTE]
>
>O servidor fornece acesso de leitura somente aos usuários com a função de aluno.

Forneça o URL do ponto de extremidade, a ID do cliente e a chave secreta ao administrador do cliente do AI.

## Editar uma descrição de ferramenta

A descrição da ferramenta informa ao cliente do AI quando selecionar a ferramenta e como ela responde. Você também pode adicionar prompts de exemplo. Descrições bem escritas de ferramentas ajudam os clientes compatíveis com MCP a descobrir e acionar as ferramentas apropriadas com mais precisão. Inclua a finalidade da ferramenta, as tarefas compatíveis, as entradas esperadas e os casos de uso típicos.

1. Na página **Ferramentas disponíveis**, selecione o menu **Ações** de uma ferramenta.
2. Selecione **Configuração da ferramenta MCP** \> **Editar**.

   ![](assets/2_Administrator--Configure-MCP-image5.png)

3. Na caixa de diálogo **Editar ferramenta**, atualize **Instruções/Descrição**.

   ![](assets/2_Administrator--Configure-MCP-image6.png)

4. Em **Exemplos de prompts**, edite os prompts. Para adicionar um prompt, selecione **Adicionar outro exemplo**.
5. Selecione **Salvar**.

Para retornar uma ferramenta ao seu texto original, selecione o menu **Ações** da ferramenta e selecione **Configuração da ferramenta MCP** \> **Redefinir**.

## Editar um servidor MCP

1. Selecione **IA no aprendizado** > **Servidores MCP**.
2. Selecione o nome do servidor.
3. Selecione **Editar**.
4. Atualize os campos na página **Detalhes do aplicativo** e salve as alterações.

## Excluir um servidor MCP

1. Selecione **IA no aprendizado** > **Servidores MCP**.
2. Na linha do servidor, selecione o menu **Ações**.
3. Selecione **Excluir**.
4. No diálogo de confirmação, selecione **Excluir**.

>[!WARNING]
>
>A exclusão de um servidor remove o acesso a todas as suas ferramentas para aplicativos de IA conectados. As sessões ativas podem parar de funcionar imediatamente e não é possível desfazer a exclusão.

## Solução de problemas

**As alterações na ferramenta não aparecem imediatamente.**
As edições nas descrições de ferramentas levam algum tempo para entrar em vigor. Aguarde e tente novamente.

**Um cliente AI parou de funcionar depois que um servidor foi excluído.**
Crie um novo servidor e forneça as novas credenciais ao administrador do cliente do AI.

**O cliente de IA usa a ferramenta errada.**
Revise as descrições de ferramentas alteradas. Selecione **Redefinir** para restaurar o texto original.

## Práticas recomendadas

* Mantenha as descrições originais da ferramenta, a menos que tenha um motivo específico para alterá-las.
* Escreva descrições de ferramentas e exemplos de prompts específicos e inequívocos ao editá-los.
* Armazene a chave secreta com segurança e compartilhe-a somente com o administrador do cliente do AI.
* Crie um servidor separado para cada aplicativo de IA, para que você possa revogar um sem afetar os outros.
* Confirme se nenhum aplicativo de IA depende de um servidor antes de excluí-lo.
