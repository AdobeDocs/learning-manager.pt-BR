---
title: Guia de Solução de Problemas do Live Hub
description: Mensagens de erro comuns e notificações que você pode encontrar durante uma sessão do Live Hub, suas causas e etapas para resolvê-las.
source-git-commit: 02de0cee632d34c99e1cba12cddb846f7e6cae81
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 2%

---


# Guia de solução de problemas do Live Hub

Durante uma sessão do Live Hub, os professores podem encontrar mensagens de erro ou notificações que impedem que determinadas ações sejam concluídas conforme esperado. Este artigo descreve os erros comuns enfrentados pelo professor, suas possíveis causas e as etapas para resolvê-los.

## Problemas de conexão

| Mensagem de erro | Cenário | Sugestões para superar o erro |
|---|---|---|
| Algo deu errado. Tente novamente. | Um erro geral de conectividade ou relacionado à sessão ocorre, por exemplo, quando o ingresso ou a interação com uma sessão e a solicitação falha devido à instabilidade da rede, a uma sessão ALM expirada ou a um estado de navegador conflitante, como várias guias abertas na mesma reunião. | <ul><li>Verifique sua conexão de rede e garanta uma largura de banda estável sem interferência de VPN/proxy.</li><li>Confirme se você fez logon no ALM com uma sessão válida: faça logoff e logon novamente se a sessão tiver expirado.</li><li>Evite ingressar na mesma reunião em várias guias ao mesmo tempo.</li><li>Tente uma janela anônima/privada ou limpe o cache do navegador se o problema persistir.</li><li>Atualize a página: a maioria dos erros transitórios é resolvida após uma recarga; se ocorrer novamente, entre em contato com o suporte.</li></ul> |

## Problemas na guia Quiz

As mensagens abaixo podem ser exibidas quando um professor cria ou inicia um quiz e o quiz não atende aos requisitos necessários para iniciá-lo.

| Mensagem de erro | Cenário | Sugestões para superar o erro |
|---|---|---|
| Digite uma pergunta para continuar. | Um professor tenta iniciar um quiz sem inserir o texto da pergunta. | Insira a pergunta, forneça as opções de resposta, selecione a resposta correta e inicie o quiz para os participantes. |
| As opções de resposta não podem ser deixadas em branco. | Um professor insere o texto da pergunta, mas não insere as opções de resposta ou deixa uma ou mais opções de resposta em branco. | Insira a pergunta, forneça as opções de resposta, selecione a resposta correta e inicie o quiz para os participantes. |
| Marque a resposta correta. | Um professor insere as opções de pergunta e resposta, mas não seleciona uma opção de resposta correta. | Insira a pergunta, forneça as opções de resposta, selecione a resposta correta e inicie o quiz para os participantes. |

## Problemas da guia Votação

As mensagens abaixo podem ser exibidas quando um professor duplica, exclui ou redefine uma pesquisa.

| Mensagem de erro | Cenário | Sugestões para superar o erro |
|---|---|---|
| Não foi possível duplicar a pesquisa. Tente novamente. | Um professor duplica uma pesquisa existente e a duplicata não é criada. | Feche o painel Enquetes e questionários e tente duplicar a enquete novamente. |
| Não foi possível excluir todas as pesquisas. Tente novamente. | Um professor exclui todas as pesquisas de uma vez usando Excluir tudo e a exclusão em massa falha ou é concluída apenas parcialmente. | Feche o painel Enquetes e questionários e tente excluir as enquetes novamente usando Excluir todas as enquetes. |
| Não foi possível excluir a pesquisa. Tente novamente. | Um professor exclui uma única pesquisa e a exclusão não é concluída. | Feche o painel Enquetes e questionários e tente excluir a enquete novamente. |
| Não foi possível redefinir a pesquisa. Tente novamente. | Um professor redefine uma pesquisa executada anteriormente para que possa ser reutilizada e a redefinição não seja concluída. | Feche o painel Enquetes e questionários e tente redefinir a enquete. |

## Problemas de upload de conteúdo

A mensagem abaixo pode ser exibida quando um professor carrega um arquivo de referência que o assistente do AI usa para responder a perguntas.

| Mensagem de erro | Cenário | Sugestões para superar o erro |
|---|---|---|
| Não foi possível processar o arquivo. Tente novamente. | Um professor carrega um arquivo corrompido, em branco ou protegido por senha que não pode ser processado. | Converta o arquivo em um formato compatível (PDF ou PPT) e carregue-o novamente. |

## Problemas de upload de conteúdo em caixa de informações

As mensagens abaixo aparecem como notificações do sistema quando um professor carrega um arquivo de referência que o assistente do AI usará e o arquivo falha em uma verificação de validação específica.

| Mensagem de erro | Cenário | Sugestões para superar o erro |
|---|---|---|
| O arquivo não pôde ser processado. Verifique o arquivo e tente novamente. | Um professor carrega um arquivo que está corrompido. | Verifique o formato do arquivo e converta-o em um formato compatível (PDF ou PPT) e faça upload novamente. |
| O arquivo é protegido por senha. Remova a senha e faça upload novamente. | Um professor carrega um arquivo que é protegido por senha. | Remova a proteção por senha do arquivo e faça upload novamente. |
| O arquivo não tem conteúdo para processar. Faça upload de um arquivo com conteúdo de texto. | Um professor carrega um arquivo que não tem conteúdo para o assistente do AI processar. | Faça upload de um arquivo que contenha conteúdo de texto. |
| “FileName.pdf” excede o limite de 1 MB. | Um professor carrega um arquivo PDF que excede o limite de tamanho de arquivo de 1 MB. | Compacte ou reduza o tamanho do arquivo de PDF para menos de 1 MB e faça upload novamente. |
| “FileName.pptx” excede o limite de 3 MB. | Um professor carrega um arquivo PPT que excede o limite de tamanho de arquivo de 3 MB. | Compacte ou reduza o tamanho do arquivo PPT para menos de 3 MB e faça upload novamente. |

## Problemas na sessão de grupo

As mensagens abaixo podem ser exibidas quando um professor tenta iniciar uma sessão de breakout.

| Mensagem de erro | Cenário | Sugestões para superar o erro |
|---|---|---|
| Não é possível iniciar a interrupção — a conexão foi interrompida. Tente novamente quando estiver reconectado. | Um professor tenta iniciar salas para sessão de grupo enquanto sua conexão é interrompida ou reconectada no momento. | Aguarde a conexão estabilizar (procure um indicador de reconexão) e, em seguida, inicie as salas para sessão de grupo novamente. |
| Não foi possível iniciar a sessão de grupo. Tente novamente. | Um professor inicia salas para sessão de grupo e a solicitação para iniciá-las falha. | Tente iniciar novamente as salas para sessão de grupo. Se o problema persistir, feche o painel Saída e tente novamente. |
| Não foi possível gerar o resumo. | Isso pode ocorrer nas seguintes situações: <ul><li>Nenhum usuário estava falando durante a sessão, portanto, não há nenhum conteúdo de áudio para resumir.</li><li>A discussão dura menos de 60 segundos.</li></ul> | Certifique-se de que os participantes falem ativamente por pelo menos 60 segundos durante a sessão antes de gerar o resumo. Se o problema persistir, aguarde um momento e tente novamente. |

## Problemas de geração de notificação do sistema de resposta

A mensagem abaixo pode aparecer quando um professor solicitar que o assistente de IA gere uma resposta para a pergunta de um participante no bate-papo.

| Mensagem de erro | Cenário | Sugestões para superar o erro |
|---|---|---|
| Isso não foi abordado na sessão. | Um aluno faz uma pergunta que não é coberta na referência de conteúdo carregado. Esse é um comportamento esperado, não um erro. | Responda à pergunta manualmente. |
