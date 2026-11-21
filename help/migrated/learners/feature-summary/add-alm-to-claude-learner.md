---
description: Adicione o servidor Adobe Learning Manager à sua própria conta do Claude como um conector personalizado, faça logon e pergunte sobre seu aprendizado
jcr-language: en_us
title: Adicionar o Adobe Learning Manager a Claude como aluno
exl-id: 31c00b29-4919-48b7-9993-ed3ac358ba5e
source-git-commit: 05691364449234a4782e2de5d4752c7b277f5fd4
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---

# Adicionar o Adobe Learning Manager a Claude como aluno

Use essas etapas somente se sua organização ainda não adicionou o conector para você. Se você vir um conector do Adobe Learning Manager em Claude, selecione **Conectar**.

## Adicionar o conector no Claude

1. No Claude, vá para **Personalizar** \> **Conectores**.
2. Selecione **Adicionar** (**+**) e depois **Adicionar conector personalizado**.
3. Insira um **Nome**, como Adobe Learning Manager.
4. Insira a URL do ponto de extremidade MCP em **URL do servidor MCP remoto**.
5. Selecione **Continuar**.
6. Em **Autenticação**, mantenha **entrar agora**.
7. Em **Cliente OAuth**, selecione **Usar seu próprio cliente OAuth**.
8. Insira a ID do cliente em **ID do cliente**.
9. Insira a chave secreta no **Segredo do Cliente**.
10. Selecione **Adicionar**.
11. Faça logon no Adobe Learning Manager quando a página de logon for aberta.

Depois que você faz logon, o conector é exibido como conectado. Faça uma pergunta sobre seu aprendizado. Para ideias, veja **exemplos de prompts para alunos**.

>[!IMPORTANT]
>
>Claude rotula o campo Segredo do cliente como opcional, mas o Adobe Learning Manager o exige. Se você deixá-lo vazio ou inserir um valor incorreto, o logon falhará com a mensagem “Falha na autorização”.

>[!NOTE]
>
>Suas solicitações são executadas com suas próprias permissões. Claude só consegue ver o que está no Adobe Learning Manager.

## Usar uma conta da Adobe Learning Manager diferente

Se o navegador já tiver uma sessão ativa do Adobe Learning Manager, Claude se conecta à conta sem solicitar credenciais. Para se conectar como um usuário diferente, faça logoff do Adobe Learning Manager primeiro ou use uma janela privada do navegador.

## Outros clientes de IA

Para o ChatGPT ou outro cliente, as etapas são diferentes. Consulte a documentação do cliente AI para adicionar um conector personalizado e use os mesmos três valores do administrador.

## Solução de problemas

**O logon mostra uma mensagem de redirecionamento não registrada.** O administrador deve adicionar o domínio Claude a **Domínios de redirecionamento** para o servidor. Peça ao administrador para adicionar <https://claude.ai> e tente novamente.

**Claude diz que a autorização falhou.** Verifique se há espaços extras ou um valor incorreto na chave secreta. Copie-o novamente do administrador, remova o conector e adicione-o novamente.

**Você se conectou como o usuário errado.** Desconecte o conector, faça logoff do Adobe Learning Manager e conecte-se novamente em uma janela privada do navegador.

**Claude pede para você entrar novamente.** Sua sessão expirou ou seu acesso foi revogado. Selecione **Conectar** para entrar novamente.
