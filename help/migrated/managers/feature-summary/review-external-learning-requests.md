---
jcr-language: en_us
title: Enviar aprendizado externo no Adobe Learning Manager
description: Os gerentes podem revisar as solicitações externas de aprendizado enviadas pelos membros de sua equipe, verificar os detalhes e qualquer prova de conclusão, bem como aprovar ou rejeitar cada solicitação com um comentário opcional. Os envios aprovados são adicionados à transcrição do aluno.
contentowner: saghosh
source-git-commit: 2495d33fc1595bd962ba07988123e3563d4c69a0
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 1%

---


# Revisar solicitações externas de aprendizado como gerente

Quando um aluno da sua equipe envia uma solicitação de aprendizado externa no Adobe Learning Manager, você recebe uma notificação na plataforma. Você pode revisar os detalhes de envio, aprovar ou rejeitar a solicitação e adicionar um comentário para o aluno.

## Como funciona o fluxo de trabalho de revisão do gerente

Quando um aluno envia uma solicitação de aprendizado externa, ocorre o seguinte:

1. Você receberá uma **notificação no aplicativo** solicitando que você revise o envio. O envio aparece na guia **Aprendizado Externo** do painel do seu gerente.
2. Abra um envio, revise todos os campos e qualquer documento carregado como prova e selecione **Aprovar** ou **Rejeitar**.
3. Você pode adicionar um **comentário de revisão** que o aluno verá quando receber sua notificação.
4. O aluno recebe uma **notificação na plataforma** com sua decisão.

Se você aprovar um envio, a atividade de aprendizado externa será adicionada à **Transcrição do aluno administrador** e aparecerá no registro de transcrição do aluno.

<!--You can also change a previously **Rejected** submission to **Approved** if the circumstances change.-->

## Revisar e aprovar ou rejeitar um envio

1. Faça logon no Adobe Learning Manager como gerente.

2. Selecione **Aprendizado Externo** no painel de navegação esquerdo.

3. Na lista de submissão, selecione a solicitação que deseja revisar. Os envios são classificados por data de envio, com a mais recente na parte superior.

4. Revise o envio completo:

   - Título, descrição, datas, duração e pontuação

   - Qualquer campo personalizado configurado pelo administrador

   - O documento comprovativo em anexo, se fornecido. Selecione o anexo para exibir ou baixá-lo

5. Selecione **Aprovar** ou **Rejeitar**.

6. No campo **Comentário da Revisão**, insira as observações do aluno. Isso é opcional, mas recomendado ao rejeitar uma solicitação, para que o aluno saiba o que corrigir.

7. Selecione **Enviar**.

O aluno recebe uma notificação no aplicativo de sua decisão. Se você aprovou o envio, ele agora aparece na transcrição do aluno.

## Gerenciar sua fila de envio

Sua fila de aprendizado externo mostra todos os envios pendentes e anteriores de seus subordinados diretos.

**Filtrar por status**

Use o filtro **Status** para restringir a lista:

- **Todos**- mostra cada envio independentemente do status

- **Aguardando revisão-** mostra apenas os envios que estão pendentes da sua revisão

- **Aprovado-** mostra os envios que você já aprovou

- **Rejeitado-** mostra os envios que você rejeitou

**Pesquisar e classificar**

- Use o campo **Pesquisar** para localizar envios por nome de aluno.

- Os envios são classificados por data de envio por padrão, com a mais recente na parte superior.

### Regras de roteiro de aprovação

Por padrão, os envios de aprendizado externos são encaminhados para o gerente direto de um aluno. As regras a seguir se aplicam quando um aluno não tem um gerente direto atribuído:

| **O aluno tem um gerente** | **O aluno é ele mesmo um gerente** | **Envio roteado para** |
|---------------------------|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Sim | Não | Gerente direto (caso padrão) |
| Sim | Sim | Gerente direto (caso padrão) |
| Não | Não | Usuário da conta raiz, se o usuário da conta raiz tiver uma função de gerente; caso contrário, o envio será aprovado automaticamente. |
| Não | Sim | Usuário da conta raiz, se o usuário da conta raiz tiver uma função de gerente; caso contrário, a submissão é encaminhada ao aluno. |

Se tiver dúvidas sobre a atribuição do gerente para um aluno específico, entre em contato com o administrador da sua conta.

## Alterações externas de transcrição e relatório de aprendizado

Quando o envio de aprendizado externo de um aluno é aprovado no Adobe Learning Manager, a atividade é adicionada ao sistema de relatórios e aparece na transcrição do aluno administrador e na transcrição do aluno.

### Como o aprendizado externo aparece nas transcrições do aluno

**Observação:** a habilitação do Aprendizado Externo adiciona as seguintes novas colunas à Transcrição do Aluno Administrador: **Nome do Aprendizado Externo**, **Comentário de Conclusão** e uma coluna dinâmica para cada campo personalizado. As colunas de campo personalizado sempre aparecem no final da exportação. Se os dados da transcrição do aluno forem alimentados em relatórios automatizados ou ferramentas de BI, certifique-se de que esses pipelines estejam atualizados para manipular as colunas adicionais.

Somente envios de aprendizado externos **aprovados** aparecem nas transcrições. Os envios no status **Aguardando Aprovação** ou **Rejeitado** não são incluídos nas exportações de transcrição.

A transcrição do aluno administrador e a transcrição do aluno tratam o título de aprendizado externo de maneira diferente:

- Na **Transcrição do aluno administrador**, o título de aprendizado externo é colocado na coluna **LP/Certificação/Curso** existente, mantendo a estrutura da coluna consistente com outros tipos de atividade de aprendizado.

- Na **Transcrição do aluno** (gerada pelo aluno), uma nova coluna chamada **Nome do aprendizado externo** é adicionada imediatamente após a coluna **Módulo**.

Os campos personalizados configurados pelo administrador aparecem como colunas dinâmicas no final de ambas as exportações de transcrição depois que um envio é aprovado.

A filtragem baseada em data na transcrição do aluno administrador para linhas de aprendizado externas se baseia na **data de conclusão**, que corresponde à data de aprovação.