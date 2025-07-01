---
title: Alterações futuras no Adobe Learning Manager
description: Saiba mais sobre os novos recursos, melhorias e atualizações importantes a serem feitas em breve no Adobe Learning Manager. Mantenha-se informado sobre as mudanças para que você possa planejar com antecedência e aproveitar ao máximo os aprimoramentos mais recentes.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 63462eb272fe90d58c89f2be383fc103db6d4ece
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---

# Alterações futuras no Adobe Learning Manager

Estamos animados em compartilhar várias atualizações importantes futuras para o Adobe Learning Manager com as próximas versões. Essas melhorias visam simplificar os fluxos de trabalho administrativos, melhorar a precisão dos relatórios de dados e fortalecer os controles baseados em funções.

Essas alterações foram projetadas para reduzir o esforço manual, oferecer suporte à automação e melhorar o controle em todas as operações de treinamento.

## Capturar conclusões marcadas como professor na transcrição do aluno

### Público-alvo

Administrador e proprietários de automação

### Visão geral

No Adobe Learning Manager, ao usar transcrições incrementais do aluno (LT) para fluxos de trabalho de automação, as conclusões marcadas pelo professor feitas após a data da sessão não são capturadas. O carimbo de data/hora de conclusão reflete a hora de término original da sessão (não a hora em que o professor marcou a conclusão). Como essas atualizações ficam fora da janela de alteração de um dia usada para geração de LT incremental, como resultado, os dados de participação e conclusão dos alunos são excluídos dos relatórios, levando a relatórios downstream inexatos ou incompletos e possíveis lacunas de conformidade.

### O que mudou

Os relatórios de transcrição do aluno (LT) incluem conclusões marcadas por professores após a data da sessão. Isso garante que qualquer marcação de presença atrasada seja refletida corretamente na exportação da transcrição.

Estados de participação como “Presente com aprovação/reprovação” aparecerão automaticamente nas exportações de LT incrementais.

### Novidades

* Nova coluna: Marcar Data de conclusão (Fuso horário UTC).
* A Fonte de conclusão está disponível no nível do módulo.
* Compatível com relatórios LT baseados em conector ou gerados por API de trabalho.

![](assets/capture-instructor.png)

**Ação necessária**

* Se a automação depender das posições de coluna, assegure as contas lógicas para a nova coluna.
* Se estiver usando nomes de colunas, nenhuma alteração será necessária.
* As conclusões com ajuste retroativo (importações manuais) não estão incluídas.

## Baixar links no relatório de ajudas de tarefa

### Público-alvo

Administrador, administrador personalizado e proprietários de automação

### Visão geral

O relatório de ajudas de tarefa inclui um link de download direto para cada ajuda de tarefa, permitindo acesso rápido a partir do próprio relatório.

### Novidades

Uma nova coluna, **[!UICONTROL Link de Ajuda de Trabalho]**, foi adicionada à terceira posição do relatório. Ele vincula diretamente à ajuda de tarefa se for um arquivo ou mostrar o URL externo fornecido pelo autor.

Usuários com acesso (administradores/autores e funções personalizadas) podem baixar a ajuda de tarefa usando este link.

![](assets/download-links-for-job-aid.png)

### Ação necessária

* Revise os fluxos de trabalho automatizados usando relatórios de ajudas de tarefa (usando a API de trabalhos).
* Se o script for baseado na posição da coluna, atualize os scripts de acordo.
* Nenhuma ação é necessária se forem usados nomes de coluna.

## Colunas ID de Usuário Interno e Email do Gerente adicionadas ao Relatório do Usuário

### Público-alvo

Administradores (e administradores personalizados) que usam o **[!UICONTROL Relatório do usuário]** (**[!UICONTROL Administrador]** > **[!UICONTROL Usuários]** > **[!UICONTROL Interno]** > **[!UICONTROL Exportar dados do usuário]**) baixado da Interface do Usuário do administrador.

### Visão geral

Para ajudar nos fluxos de trabalho de identificação e integração de usuários, duas colunas, **[!UICONTROL ID de Usuário Interno]** e **[!UICONTROL Email do Gerente]** foram adicionadas ao relatório do Usuário, exportado pela Interface do Usuário.

### Novidades

O relatório Usuário inclui uma ID de usuário interna do usuário e o endereço de email do gerente, para mapeá-los exclusivamente entre diferentes ferramentas ou endpoints de API.

### Ação necessária

* Se estiver usando esse relatório em fluxos automatizados, essa coluna recém-adicionada deverá ser tratada na automação.
* Nenhuma alteração é necessária se os fluxos de trabalho não forem afetados.

## Permissões de comunicado no escopo para administradores personalizados

### Público-alvo

Administradores personalizados

### Visão geral

Os administradores personalizados podem criar comunicados apenas para os grupos de usuários ou catálogos dentro de seu escopo definido.

### Novidades

* As regras de escopo permitem que os administradores personalizados criem comunicados apenas para grupos de usuários ou catálogos específicos.
* Ao definir uma função personalizada, os administradores podem atribuir permissões de comunicado com escopo nos grupos de usuários ou catálogos.
* Os administradores personalizados estão limitados à criação de comunicados dentro de seu escopo determinado.
* O relatório de anúncio de notificação para administradores personalizados exibirá os alunos apenas no escopo atribuído a eles.

### Ação necessária

* O formato do relatório permanecerá inalterado. Se os administradores personalizados o baixarem da interface de usuário, o conteúdo do relatório estará sujeito ao seu escopo.
* Nenhuma modificação é necessária se esse relatório não for utilizado em nenhum fluxo de trabalho automatizado ou downstream.
