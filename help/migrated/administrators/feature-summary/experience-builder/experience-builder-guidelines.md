---
title: Diretrizes e limitações do Experience Builder no Adobe Learning Manager
description: As diretrizes e limitações do Experience Builder oferecem sugestões personalizadas de cursos e conteúdo aos alunos usando algoritmos acionados por IA.
jcr-language: en-us
source-git-commit: b3124c47d56a50437cb284fe809828bcd4c4008d
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---


# Diretrizes e limitações do Experience Builder

O Experience Builder é uma ferramenta poderosa projetada para ajudar os usuários a criar páginas da Web dinâmicas e atrativas com facilidade. Para garantir o desempenho, a usabilidade e a segurança ideais, é essencial seguir determinadas diretrizes e recomendações ao configurar páginas, usar widgets e personalizar layouts. Este documento fornece uma visão geral detalhada de notas e pontos importantes que os usuários devem considerar ao trabalhar com o Experience Builder.

As informações descritas aqui abordam aspectos importantes, como configurações de páginas e widgets, opções de personalização, manipulação de código personalizado e considerações de segurança. Ao seguir essas recomendações, os usuários podem maximizar a eficiência de seus projetos do Experience Builder, evitar armadilhas comuns e se adaptar perfeitamente a atualizações e alterações.

## Configuração de página e widget

### Máximo de páginas

É possível criar até 1.000 páginas no Experience Builder. Esse é o limite máximo, mas é recomendável planejar as páginas estrategicamente para evitar a complexidade desnecessária.

### Widgets por página

* **Limite rígido**: no máximo 25 widgets podem ser adicionados a uma única página.
* **Limite recomendado**: para melhor desempenho, é aconselhável usar no máximo 10 widgets por página.
* **Widgets baseados em API**: os widgets dependentes de APIs do ALM (por exemplo, Cursos e caminhos, Categoria, Meu Aprendizado, Aprendizado Social, Calendário, Conformidade, Quadro de classificação) devem ser limitados a 10 por página.
* **Widgets independentes**: widgets como HTML e caixa de conteúdo, que não dependem de APIs do ALM, podem ser usados até o limite rígido de 25 widgets.

### Widgets de uso único

Determinados widgets, como Calendário, Aprendizado social, Conformidade e Quadro de classificação, devem ser usados apenas uma vez por página. Usá-los várias vezes pode levar a problemas de desempenho, especialmente para widgets como o calendário, que exigem recursos significativos para carregar sessões.

### Diretrizes de dimensionamento do widget

Widgets como Calendário, Quadro de classificação, Social e Conformidade devem ser colocados em layouts com uma largura mínima de um terço da página. Os widgets de placa única são mais adequados para essa largura a fim de garantir uma exibição ideal. Widgets como Calendário e Conformidade (exibição expandida) são projetados para layouts de semilargura para oferecer uma melhor experiência ao usuário. Para outros tamanhos de layout, os widgets ajustarão responsivamente para se ajustar ao espaço disponível e manter a usabilidade.

O uso de widgets com essas diretrizes de tamanho recomendadas aprimora a interação geral do usuário.

## Diretrizes de personalização

### Distâncias padrão de pixels

**Distância vertical**: a distância vertical padrão entre os widgets é de 80 pixels.
**Distância horizontal**: a distância horizontal padrão entre os widgets é de 20 pixels.

### CSS personalizado

Os usuários podem substituir distâncias padrão e outras propriedades visuais usando CSS personalizado.

Etapas para a personalização:

* Inspect os elementos de página para identificar classes CSS.
* Aplique alterações no nível global, no nível do widget ou no nível da página.

Por exemplo, para reduzir a distância vertical entre os widgets, modifique a propriedade CSS para a classe relevante.

## Posicionamento do menu

Os menus podem ser posicionados na parte superior ou esquerda da página. Mais ajustes podem ser feitos usando CSS personalizado.

## Recomendações específicas ao recurso

### Widgets Aprendizado social e Gamificação

* Se esses recursos estiverem desativados, os administradores deverão remover manualmente os widgets correspondentes das páginas.
* As páginas devem ser recriadas para garantir que permaneçam funcionais e visualmente intactas após a desativação desses recursos.

## Manuseando código personalizado

### Impacto das atualizações

* O código personalizado existente (HTML, CSS, JS) injetado no back-end pode não funcionar conforme o esperado após as atualizações do Experience Builder.
* Os usuários devem reescrever seu código para alinhá-lo às novas alterações da interface, como nomes de classe atualizados.

### Suporte de front-end

* Adicione código personalizado diretamente no portal do administrador usando widgets de HTML ou blocos CSS/JS no nível de conta.

### Isenção de responsabilidade

* O código personalizado pode não funcionar como esperado em versões futuras, exigindo ajustes. Esteja preparado para atualizar o código após cada versão.

## Recomendações gerais

### Considerações sobre desempenho

* Evite exceder os limites de widget recomendados para evitar a degradação do desempenho.
* O uso de widgets com uso intensivo de recursos (por exemplo, um calendário) várias vezes em uma página pode afetar significativamente os tempos de carregamento da página.

### Considerações de segurança

* **widgets HTML**: você deve garantir que o código trate de problemas de segurança, como ataques de scripts entre sites (XSS), pois eles estão fora do escopo do controle do Experience Builder.
* **Rodapé personalizado**: ao personalizar o rodapé usando HTML ou CSS, verifique se o código segue as práticas recomendadas de segurança.

### Alterações de quebra

As atualizações do Experience Builder podem introduzir mudanças radicais nas personalizações. Você deve:

* Ajuste o código para corresponder aos novos elementos de interface.
* Teste as personalizações após cada atualização.

## Notas adicionais

### Implementação de CSS personalizada

* Você pode inspecionar elementos de página, copiar classes CSS e aplicar as propriedades desejadas para personalizar layouts globalmente, no nível do widget ou no nível da página.

### IDs de widget e IDs de página

Cada widget e página tem IDs exclusivas que podem ser usadas para alterações de CSS direcionadas. Isso permite a personalização em diferentes níveis:

* Nível global: aplique alterações de CSS em todas as páginas.
* Nível do widget: aplica alterações de CSS a widgets específicos.
* Nível da página: aplica alterações de CSS a todos os widgets em uma página específica.










