---
description: Saiba como o Relatório de registro de auditoria do administrador rastreia alterações de configuração, mostrando quem as fez, quando e os valores antes e depois.
jcr-language: en_us
title: Relatório de registro de auditoria do administrador
exl-id: 71b2ee42-ef1c-47fb-95ad-c339562e227d
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: c061ccbefe8d40154220587796062d335e35de77
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 0%
---

# Relatório de registro de auditoria do administrador {#adminaudittrailreport}

Gere um relatório das alterações de configuração feitas nas configurações Básico, Avançado e de Integração da sua conta, incluindo quem fez cada alteração, quando e o valor antes e depois.

## O que o relatório captura

O Relatório de registro de auditoria do administrador fornece um registro histórico das alterações de configuração para que você possa determinar:

- Quem fez a alteração
- Quando a alteração foi feita
- A configuração anterior à alteração
- Qual é a configuração após a alteração

O relatório abrange as alterações feitas em:

- Configurações de **Noções básicas**
- Configurações **avançadas**
- Configurações de **integrações**

O relatório é somente aditivo: os novos registros de alteração são adicionados ao longo do tempo e as entradas registradas anteriormente nunca são removidas. Isso permite que você revise o histórico completo de uma configuração em várias alterações, não apenas no valor atual.

O relatório está disponível para qualquer usuário com privilégios de Relatório e acesso total ao grupo de usuários. Isso inclui administradores completos e administradores personalizados que receberam acesso ao relatório.

>[!NOTE]
>
>Os registros estarão disponíveis a partir da atualização 112 de setembro de 2026. As alterações feitas antes desta atualização não são incluídas no relatório. Consulte [notas de versão](/help/migrated/release-note/release-notes.md), atualização 112.

## Por que este relatório é importante para a conformidade

As empresas que operam em setores regulamentados geralmente precisam demonstrar que as alterações de configuração nos sistemas que lidam com registros eletrônicos são rastreadas, atribuíveis e retidas. O Relatório de registro de auditoria do administrador suporta esses requisitos, identificando a pessoa, a configuração, o tempo e os valores de antes e depois de cada alteração.

>[!NOTE]
>
>Este relatório dá suporte às atividades de conformidade da sua organização. Não certifica, por si só, a conformidade com qualquer regulamentação ou norma específica.

## Gerar um relatório de registro de auditoria do administrador

1. Faça logon no Adobe Learning Manager como administrador.
2. Na navegação à esquerda, selecione **Gerenciar** > **Relatórios** > **Relatórios personalizados**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report1.png)

3. Role para baixo e selecione **Trilha de auditoria do administrador**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report2.png)

4. **Selecionar Intervalo**: escolha o período para o relatório — **Última semana**, **Último mês** ou **Escolha datas**. Se você selecionar **Escolher datas**, insira uma data **De** e uma data **Até**.
5. **Selecionar tipo de configuração**: escolha **Selecionar Tudo**, **Básico**, **Integrações** ou **Avançado**.

   Para ver a lista completa de configurações rastreadas por este relatório em Básico, Integrações e Avançado, selecione **Baixar Lista de configurações**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report6.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report3.png)

6. Selecione **Gerar**.

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report4.png)

   ![](/help/migrated/administrators/feature-summary/assets/audit-trail-report5.png)

Um arquivo `.csv` contendo as alterações é baixado para a pasta Downloads do seu navegador. A geração de relatórios pode demorar um pouco. Você pode continuar usando o Adobe Learning Manager enquanto ele processa. Se você fechar a janela do navegador antes que o relatório esteja pronto, o download começará da próxima vez que você fizer logon.

## Usos comuns deste relatório

- **Investigue uma alteração de configuração inesperada** — confirme o que mudou, quando e quem fez a alteração, em vez de confiar em pressupostos.
- **Revise as alterações feitas por vários administradores** — gere uma exibição consolidada de todas as atividades de configuração que estão no escopo do relatório para um determinado período, em vez de contatar cada administrador individualmente.
- **Confirme uma alteração de configuração aprovada** — verifique se o administrador esperado fez a alteração dentro do período de tempo esperado e se o novo valor corresponde ao que foi aprovado.
- **Comparar o histórico de uma configuração em várias alterações** — use a coluna **Revisão** para ver quantas vezes uma configuração específica foi alterada e revise cada valor registrado em sequência, incluindo se uma alteração posterior restaurou uma anterior.
- **Dar suporte a uma revisão de conformidade** — gere o relatório para o período em análise como parte de seus registros administrativos e de conformidade.
- **Revise as configurações após uma alteração de política** — confirme se as atualizações de configuração pretendidas foram aplicadas de forma consistente e identifique as alterações que ocorreram inesperadamente.
- **Manter um registro administrativo histórico** — baixe e retenha relatórios de acordo com as práticas de gerenciamento de registros da sua organização.

## Referência de coluna de relatório

O arquivo `.csv` baixado inclui as seguintes colunas.

| Coluna | Descrição |
|---|---|
| **ID do evento** | Um identificador exclusivo para esse registro de alteração específico. |
| **Carimbo de data/hora (UTC)** | A data e a hora em que a alteração foi feita, em Tempo Universal Coordenado. |
| **E-mail** | O endereço de email do administrador que fez a alteração. |
| **UUID** | Um identificador exclusivo para o administrador que fez a alteração. Preenchido somente se a UUID estiver ativada no nível da conta. |
| **Nome do administrador** | O nome para exibição do administrador que fez a alteração. |
| **Tipo de Evento** | A categoria do evento registrado — por exemplo, `Modify`, `Create` ou `Delete`. |
| **Tipo de Ação** | O tipo de ação executada na configuração — por exemplo, `CREATE_SETTING`, `UPDATE_SETTING` ou `DELETE_SETTING`. |
| **Tipo de objeto** | O objeto de configuração que foi alterado. |
| **ID do objeto** | O identificador exclusivo da configuração específica ou do objeto de configuração que foi alterado. |
| **Valor Anterior** | O valor da configuração antes da alteração. (Para uma configuração excluída, isso mostra o valor que existia antes da exclusão.) |
| **Novo Valor** | O valor da configuração após a alteração. (Para uma configuração excluída, essa opção fica em branco.) |
| **Revisão** | O número de vezes que essa ID de Objeto específica foi alterada quando o evento foi gravado. A primeira alteração registrada para um objeto começa em 1. |

>[!TIP]
>
>Para localizar todas as configurações que foram excluídas durante um período, filtre o arquivo baixado em que **Tipo de Ação** é `DELETE_SETTING`.

## Acessar este relatório programaticamente

Você pode recuperar o Relatório de registro de auditoria do administrador programaticamente usando a API Trabalhos, em vez de gerá-lo manualmente pelo aplicativo do administrador. Isso é útil se você deseja programar exportações regulares ou alimentar o relatório em um sistema de monitoramento ou alerta downstream. Consulte [Relatório de registro de auditoria do administrador da API de trabalhos](/help/migrated/api-changes-sep-2026.md#job-api-for-admin-audit-trail-report).

## Limitações

- **Localização**: o conteúdo do relatório não está localizado. O relatório é gerado no idioma padrão da conta, independentemente das configurações de localidade definidas para sua conta.
- **Motivo da alteração**: o relatório não captura o motivo pelo qual uma alteração foi feita. Manter separadamente qualquer solicitação de alteração, aprovação ou justificativa de negócios relacionada.

## Práticas recomendadas

- Selecione um intervalo de datas que abranja a alteração suspeita ou planejada.
- Selecione **Selecionar Tudo** quando a área de configurações afetada não for conhecida.
- Compare as colunas **Valor Anterior** e **Novo Valor** para cada entrada.
- Use as colunas **Nome do Administrador** e **Carimbo de data/hora** para correlacionar uma alteração com registros internos ou de trabalho aprovados.
- Mantenha a solicitação de alteração, aprovação ou justificativa de negócios relacionada separadamente quando sua organização exigir uma explicação documentada para uma alteração.

## Solução de problemas

**Não vejo nenhum registro antes de uma determinada data**
Os registros estão disponíveis somente a partir da atualização 112 (setembro de 2026). As alterações feitas antes dessa atualização não são incluídas no relatório. Consulte [notas de versão](/help/migrated/release-note/release-notes.md)

**A coluna UUID está vazia para alguns ou todos os registros**
A coluna UUID será preenchida somente se a UUID estiver ativada no nível da conta. Se não estiver habilitada, essa coluna não estará presente.

**Tenho uma função de Administrador personalizada, mas não consigo encontrar este relatório**
Confirme se sua função personalizada recebeu privilégios de Relatório e acesso total ao grupo de usuários. Entre em contato com o proprietário da conta ou com um administrador completo para solicitar esse acesso, se necessário.
