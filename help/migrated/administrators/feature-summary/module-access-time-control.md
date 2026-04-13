---
description: Defina uma janela de tempo durante a qual os alunos têm permissão para iniciar um módulo.
jcr-language: en_us
title: Controle de tempo de acesso do módulo
contentowner: mmanuel
source-git-commit: 6423fd5c0853705a28c6c67b6936d93e68cbca20
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 1%

---

# Controle de tempo de acesso do módulo

## Visão geral

O aprimoramento permite que autores e administradores no Adobe Learning Manager definam uma janela de tempo durante a qual os alunos têm permissão para iniciar um módulo. Fora da janela inicial/final configurada, o módulo permanece visível na estrutura do curso, mas os alunos não podem iniciá-lo.

Esse recurso é essencial para usuários que precisam de um controle mais rígido sobre quando determinado conteúdo se torna disponível ou deve deixar de ser iniciado, por exemplo, em programas cronometrados, treinamento baseado em coortes ou exercícios com detecção de tempo.

## Novidades

Os autores agora podem configurar, no nível do módulo em um curso, uma data/hora de início e uma data/hora de término que controlam quando os alunos têm permissão para iniciar esse módulo. Dentro dessa janela, o módulo se comporta como de costume; antes da hora de início ou após a hora de término, o aluno vê o módulo no resumo do curso, mas não pode iniciá-lo.
A configuração aparece na interface de usuário de criação do curso como controles de agendamento adicionais para tipos de módulo específicos, como conteúdo em ritmo individualizado, questionários ou atividades. Os administradores podem usar esses controles para criar módulos que abrem em fases ou para evitar inícios tardios em programas em que o conteúdo deve ser consumido em um período definido.

## Principais benefícios

A principal vantagem é a capacidade de controlar quando os módulos estão acessíveis. As equipes de treinamento podem sincronizar a disponibilidade do módulo com eventos do mundo real, como lançamentos de novos produtos, prazos normativos e programas internos. Isso garante que os alunos concluam o conteúdo de pré-requisito antes que possam acessar os módulos posteriores.
Por exemplo, a coorte 1 pode acessar o módulo 2 somente na semana 2, enquanto o módulo 3 permanecerá bloqueado até a semana 3, eliminando a necessidade de ocultar e reexibir conteúdo manualmente ou criar versões separadas do curso.
Isso melhora a experiência do aluno: em vez de enfrentar módulos que podem ser tecnicamente acessados, mas não devem estar nesse momento (ou já devem estar concluídos), os alunos veem uma estrutura do curso na qual os módulos a que têm permissão para iniciar estão claramente alinhados com o cronograma pretendido.

## Casos de uso

**Programa de habilitação baseado em coorte**: neste programa, a cada semana abre um novo módulo. O conteúdo da Semana 1 está disponível imediatamente, enquanto a Semana 2 está visível, mas não pode ser iniciada até uma data especificada. A semana 3 segue o mesmo processo de gating. Os alunos podem ver todo o caminho de aprendizado, mas o sistema controla quando eles podem realmente iniciar cada etapa.
**Produto ou treinamento de campanha associado ao tempo**: as equipes de marketing ou de produto podem criar um módulo de treinamento que só deve ser acessado enquanto uma campanha estiver ativa ou quando uma versão específica de um produto ainda estiver disponível. Essa janela de início designada garante que os alunos não iniciem um módulo sobre uma versão de produto descontinuada após a hora de término especificada.
**Ambientes de avaliação ou exame**: as organizações podem abrir um módulo (como um teste) para uma janela curta e bem definida (por exemplo, “você pode iniciar o exame a qualquer momento entre 9:00 e 12:00 em uma determinada data”). Os alunos não podem iniciar o exame fora dessa janela, que oferece suporte ao agendamento justo em fusos horários e coortes.

## Definindo tempo de acesso ao módulo

1. Faça logon no Adobe Learning Manager como autor.
2. Vá para a seção **Aprendizado** > **Cursos**. O ALM exibe uma lista de cursos.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time1.png)
3. Selecione o curso para o qual deseja definir a restrição.
4. Selecione **Instâncias**. O ALM exibe uma lista de instâncias.
5. Selecione **Módulos** na seção de instância para a qual você deseja definir o limite de acesso. O botão **Editar** é exibido.![alt-texto](/help/migrated/administrators/feature-summary/assets/module-access-time2.png) ![alt-texto](/help/migrated/administrators/feature-summary/assets/module-access-time3.png)
6. Selecione **Editar**. As seções relevantes relacionadas ao módulo são abertas na parte inferior da página.![alt-text](/help/migrated/administrators/feature-summary/assets/module-access-time4.png)
7. Para cada seção, selecione uma data inicial, uma data inicial, uma data final e uma data final.
8. Selecione **Salvar**. O ALM exibe a seguinte mensagem: “Mapeamento salvo com sucesso”.










