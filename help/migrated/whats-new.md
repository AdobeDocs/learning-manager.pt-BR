---
description: Saiba mais sobre os novos recursos da versão de dezembro de 2026 do Adobe Learning Manager, incluindo gráficos de Report Builder e Virtual Coach.
jcr-language: en_us
title: Novidades na versão de dezembro de 2026 do Adobe Learning Manager
exl-id: da46f186-3ff3-422a-af49-31c7405fd584
product_v2:
  - id: ed12e5b7-96e3-45e7-a17f-de222065ebcb
    internal-label: Learning Manager
source-git-commit: 054b295163bb0312f07aa82b2a21c7e55b5fbc1d
workflow-type: tm+mt
source-wordcount: '4684'
ht-degree: 0%
---

# Novidades na versão de dezembro de 2026 do Adobe Learning Manager

Esta versão do Adobe Learning Manager apresenta uma variedade de novos recursos e aprimoramentos destinados a simplificar a plataforma e expandir seus recursos. Essas atualizações simplificam os fluxos de trabalho diários, melhoram a forma como o conteúdo de aprendizagem é organizado e fornecido e tornam a experiência geral mais consistente e intuitiva.

## Report Builder gráficos e dashboards

O Adobe Learning Manager agora oferece suporte a gráficos e dashboards no Report Builder, permitindo que os administradores visualizem os dados do relatório diretamente na plataforma. Os administradores podem criar gráficos a partir de colunas de relatórios, com agregação e filtragem disponíveis em cada gráfico.

O Report Builder suporta os seguintes tipos de gráfico:

* Número grande
* Gráfico de linhas
* Gráfico de barras
* Gráfico de pizza
* Tabela dinâmica

Um painel de relatório contém gráficos criados a partir de um relatório. Um painel de controle personalizado combina gráficos de vários relatórios, como registro e dados do usuário, e suporta até 20 widgets. Os gráficos que pertencem a um relatório são compartilhados quando você compartilha o relatório. Isso ajuda os administradores a manter os dados de relatório atuais em uma exibição em vez de executar os relatórios novamente. Os gráficos exibem até 10.000 pontos de dados, e as tabelas dinâmicas mostram até 100 linhas e 100 colunas. Se um gráfico exceder um limite, aplique filtros para restringir os resultados. Ainda não é possível exportar painéis.

## Relatórios do Agente do Insights no Report Builder

Os administradores agora podem continuar trabalhando com respostas do Agente do Insights no Report Builder. Quando o Agente do Insights responde a uma pergunta, o Report Builder mapeia a mesma consulta para seus próprios campos em uma etapa paralela. Os administradores podem abrir, revisar, editar e salvar o relatório. A partir daí, você pode usar os mesmos recursos de Report Builder que qualquer outro relatório, como assinaturas.

Se parte de uma pergunta não puder ser expressa com campos Report Builder, o relatório lista essa parte como uma lacuna. Se a parte que falta é central para a questão, o relatório não é oferecido. Consultas complexas podem produzir resultados reduzidos, portanto, revise cada relatório antes de confiar nele.

## Integração com o Adobe Experience Manager Assets

O Adobe Learning Manager agora se integra ao Adobe Experience Manager Assets, permitindo que os autores acessem e usem conteúdo de aprendizado aprovado e ativos de imagem diretamente de um repositório centralizado. Isso remove a etapa manual de download e upload entre a equipe que gerencia ativos no DAM (Digital Asset Manager, gerenciador de ativos digitais) e a equipe que cria cursos no Adobe Learning Manager.

O que muda:

* **Acessar ativos aprovados:** os autores navegam e selecionam ativos do Experience Manager Assets sem sair do Adobe Learning Manager, portanto os cursos usam arquivos aprovados atuais em vez de cópias locais que podem ficar desatualizadas.
* **Manter os ativos do curso atualizados:** quando um ativo é alterado no DAM, a atualização pode fluir para os cursos usando-o automaticamente, mantendo o conteúdo consistente à medida que os ativos são revisados.
* **O acesso segue as permissões existentes:** os autores veem apenas os ativos aos quais já têm acesso no Experience Manager Assets, portanto, navegar no Adobe Learning Manager respeita as mesmas permissões que o próprio DAM.

O resultado é um caminho único e controlado de ativo para aluno, com menos trabalho manual e menos incompatibilidades de versão.

## Aprimoramentos no envio de arquivos

Os módulos de envio de arquivos agora oferecem suporte a envios de equipe e avaliação baseada em rubrica. Uma nova configuração também controla se a aprovação do professor é necessária para envios.

### Envios para a equipe

Os professores agora podem criar equipes para envios de arquivos. Cada equipe envia um arquivo para toda a equipe. O professor avalia o envio uma vez e o resultado se aplica a cada membro. Equipes são formadas de duas maneiras: os professores as criam manualmente ou um processo agendado as cria antes da data de início da instância, com base nos membros por equipe ou número de equipes.

Os professores gerenciam equipes em uma nova página de **gerenciamento de equipes** e revisam o trabalho em uma página de envios de equipe. Os professores também podem cancelar o envio de um envio aprovado para desbloquear a equipe quando alterações forem necessárias, como quando um membro da equipe sai. Uma equipe comporta até 100 membros. Os alunos podem exibir sua equipe, seus membros e o resultado da avaliação. Os módulos de equipe não podem ser adicionados ou excluídos depois que um curso é publicado.

### Avaliações com base em rubricas

Os autores agora podem definir uma rubrica, chamada de plano de avaliação, para os módulos de envio de arquivos. Uma rubrica suporta perguntas objetivas com opções pontuadas e perguntas subjetivas com revisão escrita.

Os autores também podem definir as seguintes configurações:

* Se os alunos visualizam as perguntas de avaliação baseadas na rubrica antes de enviarem
* Se a pontuação é uma pontuação geral ou uma pontuação para cada critério

Cada pergunta pode ser marcada como obrigatória e configurada para permitir comentários do revisor. Uma avaliação baseada em rubrica comporta até 100 perguntas, e os autores inserem perguntas separadamente para cada local. Depois que um curso é publicado, somente o texto da pergunta pode ser alterado.

### Aprovação do instrutor ou conclusão automática

Os autores agora podem escolher se os envios de arquivos exigem a aprovação do professor ou são concluídos automaticamente. Esta configuração é independente do plano de avaliação.

## Servidor do Protocolo de Contexto de Modelo para o Assistente de Aluno

O ALM permite que os alunos acessem o aprendizado nas ferramentas que já usam por meio de um servidor MCP (Model Context Protocol). Os alunos podem acessar o Learning Manager de qualquer lugar, incluindo ChatGPT, Claude e agentes personalizados. Configure o servidor no aplicativo do administrador de integração para dar aos administradores acesso a seis ferramentas principais para os alunos. Isso inclui duas ferramentas do Assistente do aluno: Agente de resposta e Caminho de aprendizado personalizado.

O servidor fornece os seguintes recursos:

* Pesquisa
* Listar inscrições
* Obter objeto de aprendizado
* Obter perfil de usuário
* Responder à pergunta sobre conteúdo de aprendizado
* Obter caminho de aprendizado personalizado

Os administradores podem editar cada descrição de ferramenta para adicionar exemplos específicos da organização. Os clientes leem os detalhes de autorização dos metadados do servidor, portanto a instalação precisa apenas de uma ID de cliente e um segredo do cliente.

## Faixas personalizadas de edição e identidade visual do Caminho de Aprendizado

Os alunos agora podem remover tópicos ou cursos sugeridos em uma única etapa, além da opção existente para refinar as listas de tópicos e cursos por meio do bate-papo.

Os administradores agora podem reposicionar a faixa Caminhos de aprendizado personalizados na página inicial do aluno por meio da página Marcas.

## Pratique habilidades com role-play em Virtual Coach

O Adobe Learning Manager agora oferece o Virtual Coach (Treinador virtual), uma solução de treinamento e interpretação baseada em IA que permite que os alunos pratiquem conversas realistas no local de trabalho antes de enfrentá-los no trabalho. Os exemplos incluem objeções de vendas, escalonamento de clientes e análises de desempenho.

Autores criam cenários com base em seus próprios materiais de referência usando modelos ou um assistente de IA, e os alunos falam com uma personalidade da IA que se adapta às suas respostas em tempo real. Após cada sessão, os alunos recebem feedback instantâneo de pontuação e orientação sobre o conhecimento e o estilo de comunicação, medido em relação aos critérios definidos pelo autor.

O Virtual Coach oferece suporte a nove idiomas e pode ser usado como uma ajuda de tarefa independente ou incorporado em um curso.

## Citações do caminho de aprendizado no Assistente do aluno

As respostas do Assistente do aluno agora citam o caminho de aprendizado que contém um curso de origem, juntamente com o próprio curso. Os alunos abrem a página de visão geral do curso ou a página do caminho de aprendizado na citação. As respostas retiradas de uma ajuda de tarefa incluem um link para download. Isso ajuda os alunos a encontrar o treinamento que responde às suas perguntas.

## Configurações do Assistente do AI

O Assistente do administrador oferece dois agentes: Agente do Insights e Agente do conhecimento. Eles podem ser configurados individualmente. O Assistente de aluno oferece três agentes: Agente de conhecimento, Agente de resposta e Agente de caminho de aprendizado. Eles podem ser configurados junto com a configuração do catálogo.

## Webhooks para edições do professor em instâncias do objeto de aprendizado

O webhook de modificação de instância de objeto de aprendizado agora é acionado quando um professor edita uma sessão de sala de aula virtual, além das alterações de administrador e autor. Alterações como o tempo da sessão, o local e o limite de inscrição o acionam. Os clientes sem periféricos podem recuperar os detalhes da sessão por meio da API pública e transmitir as atualizações aos alunos.

## Cursos com várias inscrições no widget de conformidade

O widget de conformidade agora lista cada instância de um curso de várias inscrições que um aluno deve concluir. Cada entrada exibe o nome da instância. Se uma instância tiver um prazo, qualquer instância sem prazo ficará oculta. O ponto de extremidade de inscrições da API pública oferece suporte ao mesmo comportamento por meio de um parâmetro opcional.

## Reenviar convites de sessão de sala de aula virtual

Os administradores com permissão de edição de curso agora podem reenviar um convite de sessão da página de instância. Selecione **Reenviar**, procure o aluno e envie. A opção está disponível para sessões atuais e futuras de sala de aula virtual. Para alunos em várias instâncias, o convite vai apenas para a instância selecionada. Os alunos que não estão inscritos na sessão são ignorados com um aviso.

## Participação automática nas exibições de gravação do Adobe Connect

O Adobe Learning Manager agora marca a presença quando um aluno reproduz a gravação de uma sessão de sala de aula virtual perdida. Uma integração agendada extrai dados do visualizador do Adobe Connect e compara o tempo de reprodução com os critérios de conclusão definidos para a conta. Os administradores definem o agendamento no aplicativo do administrador de integração. O Adobe Learning Manager considera apenas o tempo de exibição real ao determinar a participação, portanto, ignorar uma gravação não conta para os critérios de conclusão.

## E-mail Builder para cursos e instâncias

O E-mail Builder no Adobe Learning Manager permite que administradores e autores criem modelos de comunicação com a marca do aluno. Na versão de dezembro de 2026 do Learning Manager, a experiência completa do E-mail Builder está disponível para e-mails no nível do curso e da instância. Os autores podem personalizar esses emails enquanto herdam os layouts e a formatação definidos pelos administradores.

Com o Email Builder, você pode:

* Criar layouts de email reutilizáveis
* Aplicar identidade visual da organização
* Personalizar banners e assinaturas
* Definir fontes e cores padrão
* Padronize a comunicação entre cursos e programas de aprendizado

Os administradores criam layouts e modelos de email para toda a conta. Os autores personalizam e-mails nos níveis de curso e instância sem recriar modelos do zero.

As configurações de banner e assinatura foram movidas. Antes, essas configurações apareciam em uma guia separada do **Configurações**. Essa guia foi removida e o **Banner** e a **Assinatura** agora aparecem no **Layout global**.

### Hierarquia do Construtor de email

O Email Builder usa uma hierarquia. Cada nível herda de seu nível pai e permite a personalização local.

| **Nível** | **O que ele oferece** | **Quem o personaliza** |
|-------------------|---------------------------------------------------------------------------------------------------------------------|-----------------------|
| Layout da conta | Identidade visual, fontes, cores e estrutura de cabeçalho e rodapé | Administradores |
| Modelo de conta | Estilo de email global, componentes de mensagens comuns e identidade visual compartilhada | Administradores |
| Modelo do curso | E-mails específicos do curso, como mensagens de inscrição, lembretes do curso, e-mails de conclusão e notificações de sessão | Autores |
| Modelo de instância | O nível mais alto de personalização, como mensagens específicas de coorte, específicas de sessão ou regionais | Autores |

Todos os cursos podem ser herdados dos modelos de conta. Os e-mails do curso herdam o layout da organização e permitem a personalização do conteúdo.

### Herança de layout

Um modelo é vinculado ao layout mais próximo disponível. Um modelo em nível de instância é vinculado a um layout em nível de instância, se houver. Se não houver nenhum, o modelo será vinculado ao layout principal mais próximo. Você pode ver de qual nível vem um layout.

Quando um modelo é vinculado a um layout:

* A identidade visual flui para o modelo automaticamente.
* Os autores atualizam apenas o conteúdo.
* O layout reduz a duplicação entre mensagens.

Você pode desvincular um modelo de seu layout. Depois de desvincular um modelo:

* O modelo mantém seu design existente.
* Futuras atualizações de layout não afetam o modelo.
* O modelo torna-se editável de forma independente.

A herança do layout depende dos layouts pai disponíveis. Quando ambos os níveis existem, os e-mails de nível de instância substituem os modelos de nível de curso.

### Fluxo de trabalho do administrador e do autor

Os administradores usam modelos em nível de conta para manter as mensagens consistentes em toda a conta, que eles gerenciam criando um layout e um modelo e, em seguida, publicando a marca.

Os autores usam modelos em nível de instância quando as coortes precisam de mensagens diferentes, que gerenciam por meio de instâncias do curso.

### Disponibilidade do E-mail Builder para e-mails de curso e instância

Se o E-mail Builder já estiver ativado para sua conta, você receberá as novas alterações automaticamente e não precisará fazer nada. A funcionalidade de e-mail existente continua a operar independentemente das atividades de migração do Email Builder.

## Atributos personalizados do aluno na interoperabilidade das ferramentas de aprendizado

O Adobe Learning Manager agora lê atributos personalizados do aluno por meio do ponto de extremidade opcional Nomes e serviços de provisionamento de funções da Interoperabilidade das ferramentas de aprendizado. Ele também os lê a partir da solicitação de inicialização. Atributos como país ou cidade são armazenados em campos de perfil agrupáveis. Os parâmetros de inicialização exigem um prefixo para que o Adobe Learning Manager os reconheça. Alguns sistemas de aprendizado, como o Moodle, não oferecem suporte a esse ponto de extremidade.

## Notificações do professor no quadro de discussão

Os clientes sem periféricos agora podem enviar aos professores e gerentes de coorte um resumo da atividade do quadro de discussão. Ao usar a API, você adiciona assinantes a um painel. Eles receberão novas postagens, comentários e respostas em um único email, no intervalo definido por você. Curtidas e não curtidas não são incluídas. Você ativa o recurso por meio da API.

## Classificação de relevância na pesquisa de catálogo do administrador

A pesquisa do catálogo na exibição do administrador agora classifica os resultados por relevância, usando o mesmo serviço de pesquisa que o aluno e a pesquisa do administrador em outro lugar. Uma correspondência exata, como um nome de catálogo com uma data específica, aparece primeiro, seguida de correspondências parciais. A lista de sugestões durante a digitação segue a mesma ordem.

## Sincronização de cancelamento de sessão do Adobe Workfront

As sessões canceladas no Adobe Workfront são transferidas para o Adobe Learning Manager durante o processo de migração, sem etapas manuais. A migração adiciona uma coluna **Estado** opcional que aceita **Ativo** ou **Cancelado**. Um valor em branco deixa a sessão inalterada. Um cancelamento feito por meio da migração se comporta como o feito na interface do Learning Manager. Alunos, professores, administradores, autores e gerentes recebem os mesmos e-mails de cancelamento.

Dois comportamentos se aplicam a sessões canceladas:

* A migração não aplica alterações de detalhes a uma sessão cancelada e retorna um erro de validação para essas linhas.
* Definir o estado como Ativo reativa a sessão e, em seguida, você pode atualizar seus detalhes ou cancelá-lo novamente.

As atualizações de sessão continuam funcionando como antes.

## Limite de caracteres para nomes

O Adobe Learning Manager agora aceita nomes de até 255 caracteres, contra 63. Isso se aplica aos usuários adicionados na interface, por meio da importação de CSV e no autorregistro, para que as sincronizações de usuário de outros sistemas não falhem mais em nomes longos.

Isso é especialmente útil ao migrar usuários de um sistema externo ou automatizar a criação de usuários.

A partir da versão de dezembro de 2026, o campo do nome aceita até 255 caracteres. As versões anteriores aceitavam no máximo 63 caracteres.

>[!NOTE]
>
>O limite se aplica a todos os usuários na conta, independentemente da função. Os usuários existentes e seus nomes não são afetados por essa alteração.

É possível digitar nomes longos ao adicionar ou editar usuários das seguintes maneiras:

* Adicionar um único usuário na interface do administrador
* Editar um usuário existente
* Importar usuários com um arquivo CSV
* Registrar usuários por meio do autorregistro
* Adicionar usuários externos

Nomes longos podem ser mais largos do que o espaço disponível em algumas partes da interface. Para manter o layout legível, o Adobe Learning Manager encurta os nomes longos nas seguintes áreas compactas:

* Células da tabela
* Itens de lista suspensa
* Resultados da pesquisa

Para exibir o nome completo, passe o mouse sobre o nome abreviado.

## Informações de medalha para cursos e programações de aprendizado

Quando os autores adicionam um curso ou caminho de aprendizado, uma janela lista cursos existentes e caminhos de aprendizado com informações da medalha. A janela mostra o nome, o tipo (curso ou caminho de aprendizado), o status da publicação e o formato do curso, como ritmo individualizado, virtual, sala de aula ou misto.

## Aprimoramentos não conectados

O Learning Manager agora permite o acesso controlado ao conteúdo de aprendizado sem exigir que os usuários façam logon. Os administradores podem especificar quais catálogos são públicos, enquanto os autores podem determinar quais cursos e módulos estão disponíveis sem uma conta. O conteúdo público é publicado como páginas rastreáveis e legíveis por IA, tornando a academia detectável por meio de mecanismos de pesquisa e assistentes de IA, como Claude e ChatGPT. O uso anônimo é rastreado por visitante e relatado separadamente do uso conectado.

### Consumo de conteúdo sem fazer logon

Os visitantes da sua academia pública agora podem reproduzir o conteúdo selecionado diretamente da página de visão geral do curso, sem precisar ter uma conta, um email ou um formulário.

* **Ativar ou desativar o acesso não conectado:** os administradores podem ativar ou desativar o consumo de conteúdo não conectado para toda a conta.
* **Disponibilizar cursos ou módulos sem fazer logon:** os autores podem disponibilizar um curso inteiro sem fazer logon ou abrir apenas módulos específicos, como um módulo introdutório gratuito antes do conteúdo avançado controlado.
* **Herdar configurações dos cursos:** os caminhos de aprendizado e as certificações seguem as configurações dos cursos dentro deles, sem nenhuma configuração extra.
* **Exibir conteúdo sem fazer logon:** alunos não autenticados podem exibir conteúdo não conectado disponível sem fazer logon na conta.
* **Somente conteúdo de ritmo individualizado:** conteúdo de terceiros licenciado e conteúdo de catálogo adquirido não podem ser disponibilizados sem logon.
* **Relatórios sobre consumo anônimo:** Um relatório sobre consumo mensal não conectado pode ser gerado.
* **Habilitar o aprendizado não conectado entre plataformas:** o consumo de conteúdo não conectado é compatível com Adobe Learning Manager nativo na Web e em dispositivos móveis, em implantações sem periféricos e em academias baseadas em widget do Adobe Experience Manager Sites.

### Escolher quais catálogos são públicos

Os administradores agora podem escolher os catálogos específicos que aparecem na academia pública. Somente esses catálogos podem ser pesquisados por visitantes anônimos e indexados por mecanismos de pesquisa e assistentes de IA, portanto, os cursos de teste ou conteúdo interno permanecem privados.
 

### Encontre em mecanismos de pesquisa e assistentes de IA (beta)

O Adobe Learning Manager agora pode tornar sua academia pública detectável por mecanismos de pesquisa como Google e por assistentes de IA como ChatGPT, Claude e Gemini. Seus cursos podem então aparecer em resultados de pesquisa e respostas geradas por IA, atribuídas à sua academia.

* Os controles em nível de conta permitem que os administradores decidam se os rastreadores podem acessar a academia pública e se seu conteúdo pode ser indexado.
* Cada academia recebe seu próprio mapa do site e o robots.txt, gerado automaticamente a partir dos catálogos que você tornou públicos.
* As páginas são renderizadas previamente para rastreadores, de modo que os assistentes de IA que não executam o JavaScript ainda podem lê-las.
* Os rastreadores só veem o que um visitante poderia acessar. O conteúdo controlado nunca é exposto.
* Metatítulo, descrição e dados estruturados: o Adobe Learning Manager os gera automaticamente para cada curso, caminho de aprendizado e certificação, com base nos metadados de aprendizado.

>[!NOTE]
>
>A descoberta de IA e pesquisa no Adobe Learning Manager nativo requer um domínio personalizado. As implantações sem periféricos precisarão implementar partes da configuração em seu próprio ambiente.

## Remover um curso sem tornar um caminho de aprendizado inacessível

Um curso inativo ou uma programação de aprendizado aninhada é removido do objeto de aprendizado de nível superior, que permanece aberto para novas inscrições. Retirar um curso não torna mais o caminho de aprendizado inacessível.

## URL de página não conectada para perfis de autorregistro

Os perfis de autorregistro permitem que usuários externos, como parceiros ou membros de várias organizações, criem suas próprias contas da Adobe Learning Manager. Cada perfil agora pode ter seu próprio URL de menu compartilhável e não conectado, incorporado ao Experience Builder.

Quando os usuários selecionam **Inscrever-se** em uma página acessada por meio dessa URL, eles são adicionados ao perfil ao qual a URL pertence. Isso mantém os usuários de diferentes organizações, como agências ou empresas parceiras separadas, em perfis separados.

## Armazenar datas do último acesso para inscrições no Caminho de Aprendizado

O Adobe Learning Manager agora permite anexar metadados personalizados, como uma data de último acesso, a uma inscrição no Caminho de aprendizado. Você o define e lê por meio da API, que ajuda a controlar o acesso limitado no tempo aos caminhos de aprendizado atribuídos.

As inscrições no curso já são compatíveis com uma última data de acesso por meio da API, que controla por quanto tempo um aluno pode acessar o curso. As inscrições no Caminho de aprendizado agora oferecem um campo de metadados genérico, para que você possa armazenar uma data de último acesso ou qualquer outro valor que queira controlar.

## Exportar relatórios de Report Builder com a API de trabalho

Esta versão do Adobe Learning Manager adiciona um novo tipo de trabalho de API de trabalho, `generateCustomReport`. Transmita uma ID de relatório para exportar automaticamente qualquer relatório criado no Report Builder.

Combinado com o novo conjunto de dados do questionário L2 em Report Builder, agora você pode:

* Exporte dados do questionário em nível de pergunta (N2) em vários cursos e módulos em um único relatório, em vez de executar `generateQuizReport` uma vez por curso.
* Automatize exportações recorrentes, como uma exportação incremental diária para o data warehouse ou para a ferramenta de business intelligence.

Os tipos de trabalho existentes, incluindo `generateQuizReport`, não foram alterados.

## Alterações no cabeçalho da coluna em relatórios baixados

O Report Builder agora inclui o nome do conjunto de dados nos cabeçalhos de coluna padrão de relatórios baixados. Portanto, o Nome do conjunto de dados do Objeto de Aprendizado aparece como **Objeto de Aprendizado - Nome** em vez de **Nome**. Para colunas agregadas, o título também inclui a função, como **Contagem de Objeto de Aprendizado - ID**. Se você inserir um nome personalizado no campo **Alias** de uma coluna, esse alias será usado como o cabeçalho e permanecerá inalterado.

Após a atualização, os relatórios existentes sem aliases personalizados mostram os cabeçalhos atualizados, enquanto os dados, filtros e agendamentos dos relatórios não são afetados. Se os seus scripts, planilhas, painéis de inteligência comercial ou integrações fizerem referência a colunas por cabeçalho, atualize-os para os novos nomes ou defina um alias personalizado para manter um cabeçalho específico.

## Hub ao vivo

O Live Hub agora está disponível para clientes do Ultimate e permanece na versão beta para clientes do Prime.

## Suporte multilíngue para legendas ocultas no Live Hub

As legendas ocultas no Live Hub foram aprimoradas para oferecer suporte a idiomas adicionais. Os professores agora podem selecionar o idioma da legenda em **Configurações da sala** com base no idioma falado durante a sessão.

As legendas são geradas automaticamente no idioma selecionado e exibidas em um painel dedicado que é atualizado continuamente conforme o professor fala. Todos os participantes exibem legendas no idioma selecionado pelo professor.

Esse aprimoramento melhora a acessibilidade para os participantes em diferentes idiomas e os ajuda a seguir as sessões ao vivo de maneira mais eficaz.

## Interface do Live Hub localizada e reprodutor de gravação

A interface do Live Hub agora aparece no idioma selecionado para a interface do usuário do Learning Manager. Os rótulos e títulos durante toda a sessão, incluindo bate-papo, participantes, pesquisas, salas de grupo e configurações, aparecem no idioma escolhido pelo usuário. O Live Hub oferece suporte aos mesmos 18 idiomas de interface do Learning Manager, incluindo inglês. O reprodutor de gravação também é localizado, portanto, elementos como pesquisas aparecem no idioma do curso. Por exemplo, uma gravação de um curso de alemão exibe a interface do reprodutor em alemão.

Isso proporciona aos participantes globais uma experiência consistente em toda a plataforma e em gravações de sessão.

## Sessões do Live Hub de até 5.000 participantes

O Live Hub agora oferece suporte a sessões em grande escala com até 5.000 participantes, permitindo que as organizações conduzam grandes sessões de treinamento. Os autores podem escolher uma capacidade de 5.000 participantes ao adicionar um módulo de sala de aula virtual a um curso. O Live Hub configura automaticamente a sala com base no tamanho da audiência e aplica restrições específicas de interação.

Em sessões grandes, os seguintes recursos e comportamentos se aplicam:

* O acesso à câmera, o compartilhamento de tela e a funcionalidade do quadro de comunicações são limitados a professores.
* As salas para sessão de grupo estão indisponíveis.
* Grandes volumes de mensagens de chat simultâneas, reações e perguntas são entregues em lotes escalonados.
* Outras interações e recursos, incluindo pesquisas, questionários, gravação e acompanhamento de participação, funcionam como em sessões regulares.

Isso permite que as organizações executem grandes sessões de treinamento na mesma plataforma, com uma sala que pode ser definida para o tamanho esperado do público.

## Canais

Os canais agora estão disponíveis para todos os clientes.

## Reserva de inscrição de grupo e gerenciamento de lista de espera

A reserva de inscrição em grupo e o gerenciamento de listas de espera fornecem aos autores um controle mais preciso sobre quem pode se inscrever nos cursos de Sala de aula e Sala de aula virtual. Os autores podem alocar vagas para grupos de usuários específicos e definir datas de abertura de inscrições separadas para esses grupos e todos os outros alunos. Eles também podem ativar a promoção automática da lista de espera com uma data de corte, portanto, uma vaga disponível vai para o próximo aluno qualificado. Reservar todas as vagas restringe um curso aos grupos selecionados.

## Suporte para várias conexões do Zoom

O Adobe Learning Manager agora oferece suporte a várias conexões do Zoom em uma única conta, permitindo que as organizações gerenciem sessões de sala de aula virtual em diferentes contas do Zoom.

Os administradores de integração podem configurar várias conexões do Zoom e atribuí-las a funções ou grupos de usuários específicos. Ao criar ou editar uma sessão do curso, os autores podem selecionar entre as conexões do Zoom disponíveis para eles, com cada sessão usando uma conexão.

Esse aprimoramento fornece maior flexibilidade para organizações que usam várias contas do Zoom, especialmente nos seguintes casos:

* **Treinamento específico do departamento**: gerencie contas separadas do Zoom para departamentos ou equipes diferentes na mesma conta do Learning Manager.
* **Treinamento externo e de parceiros**: atribua conexões dedicadas do Zoom a parceiros ou grupos de usuários específicos para dar suporte às suas sessões de treinamento.
* **Acesso controlado**: restringe a disponibilidade de conexões do Zoom com base em funções ou grupos de usuários, garantindo que os Autores possam selecionar apenas as conexões atribuídas a eles.
* **Gerenciamento simplificado de conexões**: permitir que os administradores de integração gerenciem centralmente várias conexões do Zoom sem afetar as sessões existentes.

## Integração do Navegador de Exame Seguro para questionários

O Adobe Learning Manager agora se integra ao navegador Safe Exam para questionários nativos, fornecendo um ambiente seguro e controlado para realizar avaliações. Os administradores podem ativar a integração no nível da conta e carregar um arquivo de configuração do Navegador de exame seguro (.seb) para definir as restrições de avaliação. Os autores podem escolher quais questionários individuais requerem o navegador Safe Exam.

Quando os alunos tentarem fazer um quiz que requer o Navegador de exame seguro, serão solicitados a iniciar o navegador. Isso bloqueia o acesso a outros navegadores e aplicativos durante a avaliação, de acordo com as restrições definidas pelo administrador. Os alunos que não o têm instalado são solicitados a baixá-lo.

**Onde ele ajuda:**

* **Avaliações de certificação:** realize questionários nos quais é importante restringir o acesso a recursos externos.
* **Treinamento de conformidade:** dê suporte a avaliações controladas para treinamento obrigatório e requisitos normativos.
* **Avaliações de alta complexidade:** reduza as oportunidades de acesso a aplicativos ou recursos não autorizados durante avaliações importantes.
* **Gerenciamento de avaliação flexível:** permita que os autores exijam o Navegador de Exame Seguro apenas para questionários que precisem de restrições adicionais.

## Correções de acessibilidade no Live Hub

Correções de acessibilidade no Live Hub aprimoram a experiência para usuários de tecnologias de assistência e navegação por teclado.

* **Leitores de tela**: os controles e o conteúdo agora são anunciados corretamente com NVDA, JAWS, VoiceOver e TalkBack.
* **Navegação no teclado**: cada elemento interativo pode ser acessado em uma ordem de tabulação lógica com um indicador de foco visível, o foco não fica mais preso e um link de navegação para ignorar está disponível.
* **Legendas ocultas**: as sessões ao vivo mostram legendas em tempo real, as gravações suportam carregamento e alternância de legenda, e a alternância de legenda pode ser operada pelo teclado.
* **Contraste de cores**: os componentes de texto e interface agora atendem às taxas de contraste necessárias, e um tema de alto contraste está disponível.
* **Zoom e refluxo**: o conteúdo e a funcionalidade são preservados com zoom de 200% no navegador, e o Live Hub funciona com ampliadores de tela.

## Alterações na API da versão de dezembro de 2026 do Adobe Learning Manager

### Pedidos de API de marcador e manipulação de conteúdo desativado

Os alunos podem marcar treinamentos para revisitá-los posteriormente. Anteriormente, as APIs de marcador retornavam treinamentos salvos em uma ordem específica, impedindo que as integrações sem periféricos exibissem primeiro os treinamentos salvos mais recentemente. Os marcadores dos objetos de aprendizado retirados também permaneciam na lista e levavam a erros de “Página não encontrada”.

Esta atualização corrige ambos:

* Os marcadores agora são retornados como os mais recentes primeiro.
* Os marcadores dos objetos de aprendizado retirados não são mais retornados.

Nenhum novo ponto de extremidade, parâmetro ou atributo de resposta é adicionado, portanto as integrações existentes continuam funcionando sem alterações.

### APIs para notificações do professor do quadro de discussão

Esta versão inclui novas APIs que oferecem suporte a notificações do professor do quadro de discussão. Use-os para inscrever professores e gerentes de coorte em painéis de discussão e controlar qual atividade aparece em seus emails de resumo.

### Suporte de API para instâncias com várias inscrições no aplicativo do aluno

A API de inscrições agora oferece suporte a instâncias de várias inscrições no aplicativo do aluno. Adicione o parâmetro `includeMultiInstanceEnrollments=true` opcional a `GET /enrollments` para incluí-los. O padrão é `false`, portanto as integrações existentes, incluindo implementações sem periféricos, continuam trabalhando inalteradas.

### Data do último acesso para inscrição nos Caminhos de aprendizado

Agora você pode armazenar metadados personalizados, como uma data de último acesso, em uma inscrição no Caminho de aprendizado e defini-la e lê-la por meio da API. Isso ajuda a controlar o acesso limitado no tempo aos caminhos de aprendizado atribuídos.

* Defina os metadados em uma inscrição existente ou ao inscrever um aluno usando um token de administrador.
* Leia-o com um token de administrador ou aluno.

Os metadados são para seu próprio rastreamento. Ele não controla o acesso e não é aplicado aos cursos no caminho.

### Tipo de trabalho da API de trabalho para exportações de Report Builder

A API de Trabalho tem um novo tipo de trabalho, `generateCustomReport`, que exporta qualquer relatório de Report Builder salvo quando você passa sua ID de relatório. Com o novo conjunto de dados do questionário L2, você pode exportar dados do questionário em nível de pergunta em vários cursos em um relatório e automatizar exportações recorrentes.

Os tipos de trabalho existentes, incluindo `generateQuizReport`, não foram alterados.

### APIs para o conector do Zoom

Use essas APIs para exibir e gerenciar conectores do Zoom no Adobe Learning Manager. Use-os para recuperar conexões existentes do Zoom, salvar credenciais do Zoom, criar ou atualizar conexões e gerenciar permissões de acesso para grupos de usuários e funções personalizadas.

**Sequência de API**

Usar as APIs nesta sequência:

| **Etapa** | **API** | **Finalidade** | **Autenticação** |
|------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------|-----------------------------------------------------|
| 1 | `POST /ctr/authcred/uuid/20012    ` | Salve as credenciais do Zoom. | Sessão do administrador de integração |
| 2 | `POST /ctr/app/esconnect  ` | Crie uma conexão com o Zoom ou atualize uma existente. | Sessão do administrador de integração |
| 3 | `PUT /ctr/xtsa/{connectionId}/access` | Defina os grupos de usuários e funções personalizadas que podem usar a conexão. | Sessão do administrador de integração |

**Autenticação e permissões**

Essas APIs usam autenticação baseada em sessão e exigem que o usuário faça logon como administrador de integração no Adobe Learning Manager.
