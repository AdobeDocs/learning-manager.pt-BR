---
title: Novidades na versão de abril de 2026 do Adobe Learning Manager
description: Saiba mais sobre os novos recursos, melhorias e atualizações importantes na versão de abril de 2026 do Adobe Learning Manager.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 78b345adf3fb39cdfa728ff4a788be1b36fff906
workflow-type: tm+mt
source-wordcount: '20211'
ht-degree: 0%

---

# Atualizações no Adobe Learning Manager

>[!IMPORTANT]
>
>Os recursos desta versão estão disponíveis na versão beta. A funcionalidade e o comportamento podem mudar antes do lançamento. Compartilhe feedback por meio de seus canais de suporte Adobe comuns.


Este documento resume os novos recursos, melhorias e atualizações na versão de abril de 2026 do Adobe Learning Manager. Use-a para planejar alterações para sua organização e entender o que está disponível para alunos, administradores e autores.

**Para alunos:** o Fluidic Player agora mostra o nome do próximo módulo e um botão Limpar saída. O idioma do reprodutor pode ser definido por meio de LTI para uma experiência consistente em todas as plataformas. o conteúdo do Captivate inclui um sumário unificado, marcas de conclusão no nível do slide e exportações de notas confiáveis. O suporte a vários idiomas está disponível para ajudas de tarefa, perguntas de lista de verificação e faixas de texto de vídeo (VTT). O Assistente de IA ajuda os alunos a obter respostas dentro da experiência de aprendizado.

**Para administradores e autores:** o conector do Zoom oferece suporte a várias sessões VILT simultâneas. Os cursos compartilhados em contas entre parceiros exibem o autor real em vez de “Autor externo”. Os administradores podem restringir quando os módulos podem ser iniciados. As datas de expiração do objeto de aprendizado são expostas nas APIs do aluno. Os módulos de lista de verificação oferecem suporte à pontuação ponderada, ao texto da pergunta multilíngue e aos comentários opcionais do revisor. Os certificados personalizados oferecem um editor de arrastar e soltar com campos dinâmicos e planos de fundo gerados por IA. O Experience Builder não conectado permite criar páginas de aprendizado público sem exigir logon.

**Para professores:** gere códigos QR para registro de instância e presença de sessão. Adicione comentários ou feedback durante a avaliação da lista de verificação.

**Relatórios e análises:** o conteúdo do SCORM agora pode relatar várias tentativas de questionário nos relatórios L2. O tempo de aprendizado gasto no cálculo foi aprimorado nas transcrições do aluno. Os relatórios de transcrição de aprendizado dos administradores são atualizados. Os aprimoramentos de pesquisa avançada estão disponíveis.

## Navegação do Fluidic Player: mostrar o nome do próximo módulo

### Visão geral

Esse aprimoramento já foi incluído na versão de novembro de 2025 do Adobe Learning Manager.

A ação &quot;Próximo&quot; no reprodutor indica o que acontecerá quando clicado ao exibir o nome do próximo módulo ou curso e sinalizar explicitamente quando o aluno estiver prestes a sair do reprodutor.

### Novidades

**&quot;Próximo Módulo: {ModuleName}&quot; rótulo no reprodutor**

O ícone Próximo no Fluidic Player agora mostra o nome do próximo módulo no curso. Por exemplo, Próximo módulo: Lição 2 - Introdução.

Isso se aplica onde quer que o aluno esteja mudando de um módulo para o próximo no mesmo curso.

**Limpar ação de saída no último módulo**

Quando o aluno estiver no último módulo de um curso, um novo botão de ação Sair será exibido, indicando que clicar nele fechará o reprodutor e o retornará ao contexto do curso.

**Comportamento responsivo para conteúdo móvel e PDF**

Em janelas de visualização menores (por exemplo, ~largura de 320 px), o rótulo Próximo pode ser encurtado ou oculto, mostrando somente o ícone, para evitar sobreposições com controles PDF.

Para módulos do PDF, o reprodutor ajusta os controles para uma linha separada, de modo que os rótulos de navegação e os controles do PDF não interfiram entre si.

**Atualização de Administrador > Marcas > Visualização do player**

A visualização do reprodutor em Admin > Marca agora reflete o novo rótulo, por exemplo, Próximo módulo: Lição 2. Isso permite que os administradores vejam o comportamento de navegação atualizado.

### Principais benefícios

**Navegação mais clara para alunos**

Os alunos não precisam mais adivinhar o que acontecerá quando selecionarem &quot;Próximo&quot;. O rótulo especifica claramente o que vem a seguir, seja um módulo ou um curso. Essa redução na ambiguidade ajuda a aliviar a hesitação e a confusão, especialmente em públicos-alvo de grande porte do setor de educação do cliente, onde muitos alunos podem não estar familiarizados com as interfaces LMS.

**Taxas mais altas de conclusão do curso**

Indicar claramente a próxima etapa (Próximo Módulo: {ModuleName}) e adicionar uma ação Sair distinta para o módulo final reduz a probabilidade de os alunos abandonarem o curso ou ignorarem a última etapa de conclusão.

**Experiência do usuário mais previsível em todos os dispositivos**

Os rótulos atualizados se alinham com o comportamento Próximo ou Anterior e os ícones no desktop, tablet e dispositivo móvel. As restrições de layout são respeitadas em todos os dispositivos e fluxos de PDF para que os controles permaneçam utilizáveis e acessíveis.

Isso é particularmente importante para implementações sem periféricos nas quais o Fluidic Player é incorporado em uma experiência de aprendizado personalizada.

### Casos de uso

**Portais educacionais de clientes e parceiros (sem periféricos ou integrados ao AEM)**

Contas que utilizam o Adobe Learning Manager em uma configuração totalmente sem periféricos, direcionando os alunos de canais de marketing externos. Estes alunos:

* Geralmente consomem conteúdo de vídeo em sequências longas.

* Espere uma experiência no estilo de currículo, em que o sistema indique claramente o próximo episódio/módulo.

Nesses ambientes, o rótulo **Próximo Módulo:{ModuleName}**:

* Reforça a natureza guiada da jornada.

* Minimiza a queda entre os módulos.

**Cursos de conformidade e certificação com módulos solicitados**

Em cenários regulamentados ou de conformidade pesada:

* Os alunos devem concluir uma sequência estrita de módulos.

* Os autores geralmente desabilitam o sumário para evitar ignorar.

Aqui, mostrando o **Próximo Módulo:{ModuleName}**:

* Confirma aos alunos que estão seguindo a sequência correta.

* Torna menos provável que interpretem incorretamente a ação Próximo e saiam cedo.

**Caminhos de aprendizado em que os cursos se seguem**

Onde os Caminhos de aprendizado ou equivalentes agrupam vários cursos. Isso é útil ao criar sequências no estilo de currículo para grandes públicos.

**Consumo em dispositivos móveis**

Para alunos que usam principalmente telefones ou tablets:

* Os rótulos atualizados e o comportamento responsivo garantem que a navegação permaneça compreensível sem depender de ícones de fechamento minúsculos ou controles ocultos.

* Isso é importante para a educação do cliente, funcionários de shows ou alunos da linha de frente que podem acessar o conteúdo em sessões curtas em dispositivos móveis.

## Conector do Zoom - criar várias sessões simultâneas de Zoom

### Visão geral

A atualização do conector do Zoom melhora a forma como o Adobe Learning Manager gerencia o VILT (Virtual Instructor-Led Training, treinamento virtual ministrado por instrutor). Antes, os usuários só podiam criar uma sessão de zoom por vez. Com a nova atualização, os administradores e autores podem agendar várias sessões do Zoom ao mesmo tempo usando a integração padrão.

### Novidades

#### Suporte para várias sessões simultâneas do Zoom por meio do conector

* O conector do Zoom agora permite que mais de uma sessão do VILT na mesma data/hora seja criada no ALM.

* A lógica de agendamento não impõe mais uma restrição “uma reunião do Zoom por vez” no nível de conta/conector.

* Os administradores e autores podem configurar sessões VILT sobrepostas (por exemplo, salas de aula regionais, controles paralelos ou sessões repetidas para diferentes grupos de parceiros) sem soluções alternativas.

#### As reuniões são criadas usando a identidade do professor no Zoom (não o superadministrador do Zoom)

Para suportar reuniões simultâneas com segurança, o conector foi atualizado para que:

* As reuniões do Zoom agora são criadas usando o endereço de email do professor, em vez do email do superadministrador do Zoom.

* A conta do Zoom de cada professor pode hospedar suas próprias reuniões em paralelo com outros professores, sujeito aos limites do plano de Zoom existente.

**Observação**:

* Ainda há suporte para apenas um professor por reunião.

* Se o e-mail de um professor for atualizado posteriormente no Adobe Learning Manager, as reuniões existentes permanecerão associadas ao e-mail original usado na criação.

#### Chega de colar manualmente o URL do Zoom em sessões simultâneas

Anteriormente, quando uma segunda ou terceira sessão do Zoom tinha que ser executada ao mesmo tempo:

* Os autores precisavam criar manualmente reuniões do Zoom fora do ALM e colar o URL de ingresso do Zoom na configuração da instância do curso.

* Isso era propenso a erros e não se beneficiava de recursos de conector como controle de participação.

Com o conector atualizado:

* Todas as sessões podem ser criadas diretamente na interface do usuário do ALM usando o conector do Zoom, mesmo que se sobreponham no tempo.

* O ciclo de vida da sessão (criação/cancelamento) continua a ser gerenciado centralmente por meio de integração.

### Principais benefícios

#### Melhor programação do VILT em escala

Agora, as organizações podem:

* Executar várias salas de aula virtuais baseadas em zoom ao mesmo tempo (por exemplo, trilhas paralelas em um cume virtual, coortes regionais ou sessões separadas de treinamento de parceiros).

* Evite gargalos que antes forçavam os administradores a serializar sessões ou confiar no gerenciamento manual do Zoom.

#### Redução da sobrecarga do administrador e do autor

O aprimoramento elimina:

* Criação manual de reuniões do Zoom fora do Adobe Learning Manager.

* Copie e cole os URLs do Zoom em cada instância do curso para sobrepor sessões.

* Risco de links configurados incorretamente, reuniões incorretas serem anexadas ou acompanhamento de participação perdida.

Administradores e autores podem gerenciar todas as sessões do Zoom no Adobe Learning Manager usando fluxos de trabalho familiares.

#### Melhor alinhamento com o provisionamento do Zoom e as funções de professor

Vinculando reuniões a contas individuais do Zoom do professor:

* Cada professor pode operar dentro de seus próprios limites de licença do Zoom.

* As organizações podem usar o modelo de provisionamento existente do Zoom (uma conta por treinador, por unidade de negócios etc.) ao mesmo tempo em que se integra totalmente ao Adobe Learning Manager.

* Isso evita o gargalo de ponto único de usar um usuário compartilhado do Zoom superadministrador para todas as sessões.

### Casos de uso

#### Eventos virtuais de múltiplas faixas e cumes

As equipes de treinamento do cliente que realizam grandes eventos (por exemplo, campos de inicialização de produtos, cúpulas de parceiros ou semanas de certificação) podem:

* Configure várias sessões baseadas no Zoom no mesmo intervalo de tempo (para faixas ou tópicos diferentes).

* Gerencie todos eles como módulos VILT nos cursos e caminhos de aprendizado do Adobe Learning Manager.

* Forneça aos alunos uma experiência unificada enquanto o conector lida com toda a criação de reuniões subjacentes no Zoom.

#### Treinamento global para parceiros e clientes

As organizações que treinam clientes e parceiros em todas as regiões podem:

* Execute sessões separadas do Zoom para EMEA, APAC e Américas em horários de sobreposição para corresponder ao horário de trabalho local.

* Evite forçar um único intervalo de tempo global ou configuração manual do Zoom para coortes adicionais.

#### Ativação interna

As equipes internas de capacitação (vendas, suporte etc.) podem:

* Agende sessões de integração paralelas ou breakouts baseados em funções (por exemplo, salas de zoom separadas para desenvolvedores, administradores e colaboradores do setor) no ALM.

* Manter todas as sessões no modelo VILT do ALM para fins de relatório e conformidade, em vez de fazer a transição parcialmente para reuniões não gerenciadas do Zoom.

## Mostrar o autor original dos cursos compartilhados em contas entre parceiros

### Visão geral

Quando um curso é compartilhado pelo catálogo para uma conta entre parceiros, o Adobe Learning Manager atualmente rotula o autor como “Autor externo” nas exibições do aluno, administrador e autor da conta de recebimento. Isso pode criar desafios para alunos e administradores, especialmente em grandes empresas, pois torna-se difícil identificar e entrar em contato com o proprietário de conteúdo apropriado quando surgem problemas ou dúvidas.

O aprimoramento garante que as informações do autor sejam preservadas e apresentadas em cursos compartilhados em contas entre parceiros, em vez de serem substituídas por um espaço reservado genérico.

### Novidades

Mostrar nome do autor real dos cursos compartilhados em contas entre parceiros

Para cursos compartilhados por meio de catálogos externos ou de mesmo nível, o nome do autor original da conta de origem agora é exibido na conta de recebimento em vez de “Autor externo”.

Aplica-se a:

* Aplicativo do aluno (cartão do curso ou detalhes do curso).

* Visualizações do administrador e do autor ao visualizar como aluno.

### Principais benefícios

#### Visibilidade direta do proprietário para conteúdo compartilhado

Os alunos e administradores em contas entre parceiros agora podem:

* Veja quem é o autor do curso, mesmo quando adquirido por meio de um catálogo compartilhado.

* Evite o rótulo genérico e inútil de “Autor externo”.

#### Experiência mais consistente com vários locatários e contas entre parceiros

Para clientes que executam cenários multilocatário ou corporativos estendidos:

* O mesmo curso aparece com identidade visual consistente do autor nas contas.

* A experiência do aluno está alinhada com as expectativas da conta principal (por exemplo, ver o nome do autor da conta de origem em vez de “Autor externo”).

### Casos de uso

#### Grande empresa com contas entre parceiros

A empresa usa o ALM com:

* Uma conta principal que possui os cursos canônicos, e

* Contas de mesmo nível que adquirem conteúdo por meio de catálogos compartilhados.

Os alunos em contas entre parceiros precisam saber qual equipe corporativa criou um curso para direcionar as perguntas ou sugestões de melhoria corretamente.

Com esse aprimoramento:

* Os cursos compartilhados agora exibem o nome correto do autor corporativo em contas entre parceiros.

* A carga de suporte interno da empresa é reduzida porque os alunos e os administradores locais sabem com quem entrar em contato.

#### Compartilhamento interno de várias unidades de negócios

Onde uma unidade de negócios organiza o aprendizado para outras:

* A unidade de negócios proprietária pode ser identificada no campo do autor em todas as contas de consumo.

* Os administradores locais de L&amp;D podem ver rapidamente se um curso é mantido localmente ou por outra unidade de negócios e colaborar de acordo.

## Expor a data de expiração (desativação automática) do objeto de aprendizado nas APIs do aluno

### Visão geral

Esse aprimoramento disponibiliza a data de desativação automática de um objeto de aprendizado (LO) diretamente pelas APIs do aluno da Adobe Learning Manager. Quando um curso, caminho de aprendizado ou certificação é configurado com uma data de expiração ou de aposentadoria automática, essas informações agora fazem parte dos dados do aprendizado retornados pelos principais pontos de acesso do aluno.

### Novidades

#### Novo campo de expiração/desativação automática nas APIs do objeto de aprendizado do aluno

* As APIs do objeto de aprendizado do aluno (por exemplo, os endpoints que retornam objetos de aprendizado à experiência do aluno e às plataformas externas) agora incluem a data de expiração do objeto de aprendizado (a data de desativação automática configurada para esse objeto de aprendizado).

* Esse campo é retornado como parte da entidade de LO em respostas como:

   * Obter objeto de aprendizado (detalhes do LO).

   * Dados de LO usados para preencher a página inicial, o catálogo e os resultados da pesquisa do aluno.

* O campo complementa o completionDeadline existente que já existe no nível da instância; o novo campo é especificamente a data de baixa automática de nível baixo.

#### Disponibilidade em experiências de aluno com suporte de pesquisa

Como a data de expiração é exposta como parte da representação do objeto de aprendizado com suporte de pesquisa, ela agora está disponível em qualquer lugar que o ALM ou uma plataforma externa use:

* APIs de pesquisa ou

* catálogos orientados por pesquisa e sugestões para criar visualizações do aluno.

**Escopo e exclusões**

O aprimoramento se aplica somente às APIs do aluno.

### Principais benefícios

#### Experiência do aluno com reconhecimento de expiração em LXPs personalizados

Para grandes e médias empresas, seu LXP personalizado agora pode obter informações de expiração do LO diretamente do ALM, permitindo:

* Mostre os rótulos &quot;Expirando em {date}&quot; ou &quot;Expirando em breve&quot; nos cartões de curso e nas páginas de detalhes.

* Comunique-se com urgência com mais clareza, para que os alunos priorizem o treinamento que está prestes a se aposentar.

Isso é particularmente importante para conformidade ou treinamento de produto com limite de tempo, em que os objetos de aprendizado são atualizados regularmente e as versões mais antigas são removidas.

#### Melhores orientações para os alunos sobre os treinamentos a serem realizados agora

Ao expor a expiração do objeto de aprendizado, a experiência do aluno pode:

* Destaque os cursos que ainda são válidos, mas que estão prestes a serem retirados.

* Ajude os alunos a evitar se inscrever em treinamentos que não estarão mais disponíveis ou serão válidos em um futuro próximo.

#### Coerência com os dados existentes do prazo de conclusão

Anteriormente, as APIs de aluno já apresentavam o prazo de conclusão no nível da instância, mas não a data de baixa automática no nível de aprendizado. Com esta alteração:

Os seguintes aspectos de um treinamento estão disponíveis:

* &quot;Quando devo concluir essa instância?&quot; (prazo de conclusão).

* &quot;Até quando esse treinamento é oferecido?&quot; (desativação automática/data de expiração).

### Casos de uso

#### Uma empresa global com gerenciamento rigoroso do ciclo de vida do curso

As empresas que regularmente removem e substituem cursos (por exemplo, atualizações de normas, produtos ou metodologias) podem:

* Evite a confusão do aluno sobre a descontinuação de um treinamento.

* Direcione os alunos para as ofertas mais atuais e duradouras.

Seus portais personalizados e ferramentas internas agora podem ler a data de expiração diretamente do ALM por meio das APIs do aluno.

#### Academias externas de clientes ou parceiros

Para treinamento de clientes e parceiros, as páginas e portais de marketing geralmente enfatizam o treinamento atualizado.

Ter datas de expiração na API do LO permite que os criadores de experiência:

* Oculte ou retire o foco do conteúdo que está próximo da aposentadoria.

* Crie campanhas da “Última chance de concluir”.

## Suporte a vários idiomas para ajudas de tarefa

### Visão geral

O aprimoramento estende o modelo de localização do Adobe Learning Manager às ajudas de tarefa, permitindo que os autores anexem diferentes arquivos de conteúdo por idioma a uma única ajuda de tarefa. Em vez de criar ajudas de tarefa separadas para cada idioma, os autores agora podem gerenciar todas as versões localizadas como uma ajuda de tarefa lógica.

### Novidades

#### Upload de conteúdo específico do idioma para ajudas de tarefa

Os autores podem anexar arquivos diferentes por idioma suportado a uma única ajuda de tarefa, como cursos e outros OAs.

A experiência de criação/edição de ajuda de tarefa agora oferece suporte a:

* Selecionando um idioma.

* Fazer upload do arquivo específico de idioma para esse idioma na mesma entidade de ajuda de tarefa.

#### Manuseio consistente de idioma na interface do usuário do reprodutor e do aluno

O Fluidic Player foi atualizado para que, quando um aluno abrir uma ajuda de tarefa, a variante de conteúdo correspondente ao idioma do aluno seja exibida (quando disponível).

Administradores e autores podem visualizar ajudas de tarefa como objetos únicos com variantes de idioma, em vez de itens separados por idioma.

### Principais benefícios

#### Ajuda de tarefa única para todos os idiomas

Os autores podem evitar a criação de ajudas de tarefa separadas por idioma.

Todas as variantes de idioma da mesma ajuda de tarefa (por exemplo, um procedimento, SOP, PDF de lista de verificação ou guia de referência) podem ser gerenciadas em um só lugar.

#### Melhor experiência para alunos globais

Os alunos veem automaticamente a ajuda de tarefa em seu idioma preferido, o que significa que há:

* Menos confusão sobre qual versão abrir.

* Menos risco de acessar cópias fora do local ou desatualizadas.

Isso é particularmente útil em organizações multilíngues, onde o mesmo processo ou documentação do produto deve estar disponível em vários idiomas.

### Casos de uso

#### Implantação global do conteúdo de referência

Uma empresa precisa fornecer ajudas de tarefa em vários idiomas aos alunos em todo o mundo, como:

* Fichas de referência do produto.

* Listas de verificação do processo.

* Livros de reprodução de suporte

Em vez de criar ajudas de tarefa separadas, como “Início rápido do produto - EN”, “Início rápido do produto - DE”, “Início rápido do produto - JP”, etc., eles podem criar uma ajuda de tarefa, anexar arquivos localizados para cada idioma e permitir que o ALM forneça a versão correta para cada aluno com base nas configurações de idioma.

#### Documentação voltada para o cliente ou parceiro em vários mercados

Para academias de clientes e parceiros, as ajudas de tarefa podem incluir:

* Folhas de produto

* Guias de integração

* Suporte a fluxos de trabalho

Com ajudas de tarefa em vários idiomas:

* Cada parceiro vê a versão localizada sem ser forçado a escolher entre as entradas específicas do idioma.

* As equipes de marketing e capacitação podem gerenciar uma ajuda de tarefa por tópico em todos os locais.

## Definir restrição na hora de início do módulo

### Visão geral

O aprimoramento permite que autores e administradores no Adobe Learning Manager definam uma janela de tempo durante a qual os alunos têm permissão para iniciar um módulo. Fora da janela inicial/final configurada, o módulo permanece visível na estrutura do curso, mas os alunos não podem iniciá-lo.

Esse recurso é essencial para usuários que precisam ter um controle mais rígido sobre quando determinado conteúdo se torna disponível ou deve deixar de ser iniciado, por exemplo, em programas cronometrados, treinamento baseado em coorte ou exercícios com prazo apertado.

### Novidades

Os autores agora podem configurar, no nível do módulo em um curso, uma data/hora de início e uma data/hora de término que controlam quando os alunos têm permissão para iniciar esse módulo. Dentro dessa janela, o módulo se comporta como de costume; antes da hora de início ou após a hora de término, o aluno vê o módulo no resumo do curso, mas não pode iniciá-lo.

A configuração aparece na interface de usuário de criação do curso como controles de agendamento adicionais para tipos de módulo específicos, como conteúdo em ritmo individualizado, questionários ou atividades. Os administradores podem usar esses controles para criar módulos que abrem em fases ou para evitar inícios tardios em programas em que o conteúdo deve ser consumido em um período definido.

#### Principais benefícios

A principal vantagem é a capacidade de controlar quando os módulos estão acessíveis. As equipes de treinamento podem sincronizar a disponibilidade do módulo com eventos do mundo real, como lançamentos de novos produtos, prazos normativos e programas internos. Isso garante que os alunos concluam o conteúdo de pré-requisito antes que possam acessar os módulos posteriores.

Por exemplo, a coorte 1 pode acessar o módulo 2 somente na semana 2, enquanto o módulo 3 permanecerá bloqueado até a semana 3, eliminando a necessidade de ocultar e reexibir conteúdo manualmente ou criar versões separadas do curso.

Isso aprimora a experiência do aluno: em vez de enfrentar módulos que podem ser tecnicamente acessados, mas não devem estar nesse momento (ou já devem estar concluídos), os alunos veem uma estrutura do curso na qual os módulos que têm permissão para iniciar estão claramente alinhados com a programação pretendida.

#### Casos de uso

* **Programa de habilitação baseado em coorte**: neste programa, a cada semana abre um novo módulo. O conteúdo da Semana 1 está disponível imediatamente, enquanto a Semana 2 está visível, mas não pode ser iniciada até uma data especificada. A semana 3 segue o mesmo processo de gating. Os alunos podem ver todo o caminho de aprendizado, mas o sistema controla quando eles podem realmente iniciar cada etapa.

* **Treinamento de produto ou campanha associado ao tempo**: as equipes de marketing ou de produto podem criar um módulo de treinamento que só deve ser acessado enquanto uma campanha estiver ativa ou quando uma versão específica de um produto ainda estiver disponível. Essa janela de início designada garante que os alunos não iniciem um módulo sobre uma versão de produto descontinuada após a hora de término especificada.

* **Ambientes de avaliação ou exame**: as organizações podem abrir um módulo (como um teste) para uma janela curta e bem definida (por exemplo, “você pode iniciar o exame a qualquer momento entre 9:00 e 12:00 em uma determinada data”). Os alunos não podem iniciar o exame fora dessa janela, que oferece suporte ao agendamento justo em fusos horários e coortes.

## Controle o idioma do player por meio de um parâmetro de LTI personalizado

### Visão geral

O aprimoramento permite que plataformas externas que usam a LTI (Learning Tools Interoperability, Interoperabilidade das ferramentas de aprendizado) especifiquem o idioma do conteúdo do Adobe Learning Manager no momento da inicialização. Em vez de depender do aluno para alterar o idioma no Fluidic Player, o consumidor de LTI pode enviar um código de idioma por meio de um parâmetro de LTI personalizado. O Adobe Learning Manager usará esse código para selecionar a variante de idioma apropriada.

### Novidades

As plataformas externas que atuam como consumidores de LTI agora podem passar um parâmetro de idioma personalizado (e configurações do player relacionadas) ao iniciar o conteúdo do ALM. O ALM lê esse parâmetro e:

* Define o idioma do reprodutor de acordo.

* Inicia a variante de idioma correspondente do módulo quando o conteúdo multilíngue está configurado.

Isso significa que um aluno pela primeira vez, que seleciona francês na plataforma externa, verá o reprodutor e o módulo do ALM serem lançados diretamente em francês, sem precisar ajustar nada dentro do ALM.

O aprimoramento também acomoda cenários em que a plataforma externa trata o ALM como um reprodutor de conteúdo independente. Por exemplo, ele permite ocultar elementos de navegação e o sumário, enviando parâmetros personalizados adicionais para ajustar determinadas configurações de interface do usuário. Essas configurações funcionam em conjunto com o parâmetro de idioma, permitindo que a plataforma externa forneça uma experiência de marca tranquila e, ao mesmo tempo, use o ALM para reprodução e rastreamento.

### Principais benefícios

* **Experiência de idioma consistente entre sistemas**: quando um aluno seleciona um idioma no portal externo, essa escolha é refletida imediatamente no ALM. Isso garante que os alunos não enfrentem nenhuma incompatibilidade entre o idioma do portal e do curso. Como resultado, eles não terão que procurar por uma mudança de idioma dentro do reprodutor.

* **Relatórios específicos de idioma**: em sua plataforma, a seleção de idioma é consistente com o ALM, o que melhora a precisão de suas análises e do rastreamento de aluno. Esse alinhamento também oferece suporte a configurações em que os próprios controles de idioma do ALM são desativados intencionalmente ou ocultados no Fluidic Player para cursos específicos. Nesses casos, a plataforma externa serve como uma única fonte de verdade para a linguagem.

### Casos de uso

* Um caso de uso significativo envolve grandes empresas que utilizam integrações baseadas em LTI. Os alunos se inscrevem primeiro e selecionam um idioma na plataforma. Em seguida, eles lançam sessões de treinamento do ALM por meio da LTI. Com esse aprimoramento, quando um aluno seleciona espanhol, o módulo ALM abre automaticamente em espanhol. Isso significa que os alunos não precisam ajustar as configurações de idioma no ALM. Além disso, os relatórios baseados em idioma permanecem consistentes com o que os alunos veem e experimentam no ALM.

* Outro aplicativo é o fornecimento de experiências de curso sem periféricos em um portal do cliente ou parceiro. Nesta configuração, o portal pode incorporar conteúdo do ALM usando um iframe, enquanto toda a navegação e experiência de usuário de idioma (UX) são gerenciadas fora do ALM. Utilizando parâmetros de LTI personalizados, o portal pode garantir que o player do ALM seja exibido no idioma correto e que quaisquer elementos desnecessários da interface do usuário (como o sumário e os botões de navegação) estejam ocultos. Isso permite que os alunos percebam uma única aplicação coesa em vez de uma coleção desarticulada de ferramentas.

* Isso é benéfico para organizações que fazem treinamento em grande escala em vários idiomas usando outro LMS ou plataforma de aprendizado. Eles podem padronizar o uso dessa plataforma para gerenciar perfis do aluno, selecionar localidades e apresentar catálogos. Enquanto isso, o ALM funciona como um mecanismo confiável de rastreamento e conteúdo, respeitando as preferências de idioma e as interações do usuário especificadas pelo sistema externo durante cada lançamento de LTI.

## Ponderação de pergunta da lista de verificação para avaliações do professor

### Visão geral

O aprimoramento introduz listas de verificação ponderadas, permitindo que professores e gerentes avaliem os alunos usando escalas graduais e pontuações totais, em vez de tratar cada pergunta da lista de verificação como igual. O objetivo é facilitar a criação de listas de verificação através da implementação de avaliações ponderadas de perguntas, o que permite refletir a importância relativa de diferentes ações ou habilidades em uma única lista de verificação.

### Novidades

As listas de verificação suportarão os seguintes tipos:

1. Sim/Não
O comportamento permanece o mesmo de hoje: cada pergunta é Sim/Não e os critérios de aprovação são baseados no número de respostas “Sim”.

2. Perguntas do mesmo peso

   * As perguntas são pontuadas em uma escala numérica (0-10 por padrão), onde:

      * Os valores máx./mín. na escala são personalizáveis no nível da lista de verificação.

      * A escala agora pode começar em 0 (a pontuação mínima anterior era 1).

   * Todas as perguntas compartilham a mesma pontuação máxima, portanto a lista de verificação se comporta como uma escala graduada uniforme para cada pergunta.

3. Perguntas de peso diferente

   * Cada pergunta tem sua própria pontuação máxima (peso).

   * Os critérios de aprovação dependem da porcentagem da pontuação total possível que o aluno obtém na lista de verificação (por exemplo, “aprovação se o aluno obtém ≥ 70% da pontuação total disponível”).

Para todos os tipos de lista de verificação:

* O **Revisor** (professor ou gerente) avalia o aluno de acordo com o tipo de lista de verificação configurado:

   * Selecionando Sim/Não.

   * Selecione pontuações na escala definida.

* O relatório **Lista de verificação** foi atualizado para incluir, para perguntas com peso diferente:

   * A pontuação máxima para cada pergunta.

   * A pontuação obtida por cada aluno para essa pergunta.

Isso permite a análise do desempenho geral e do desempenho específico de perguntas com base nos pesos desejados.

### Principais benefícios

* **Avaliações mais avançadas e mais realistas**: os professores podem refletir as prioridades do mundo real dando mais pontos para os comportamentos críticos e menos para os menores, enquanto ainda usam um fluxo de trabalho de lista de verificação adequado para tarefas observadas ou práticas.

* **Aprovação/reprovação total baseada em pontuação**: as avaliações podem ser baseadas na pontuação percentual geral, não apenas na quantidade de perguntas que ultrapassam um limite, alinhando-se mais estreitamente com esquemas típicos de competência ou classificação.

* **Relatórios mais eficientes**: os relatórios atualizados da lista de verificação expõem a pontuação máxima e a pontuação obtida por pergunta, permitindo que os proprietários do programa e as equipes de qualidade identifiquem pontos fracos específicos e refinem o treinamento ou a orientação de avaliação.

### Casos de uso

* **Avaliações de habilidades corporativas**: os engenheiros são avaliados por meio de listas de verificação práticas e baseadas em cenários, nas quais determinadas etapas de diagnóstico ou comunicação devem ter mais peso do que etapas cosméticas ou de baixo risco. Perguntas ponderadas e critérios de aprovação de pontuação total tornam essas avaliações mais confiáveis e preditivas do desempenho real.

* **Observações de segurança e conformidade**: no setor de saúde, manufatura ou serviço de campo, as etapas críticas de segurança podem receber pontuações máximas mais altas, garantindo que a ausência de uma ação crítica de segurança tenha um impacto maior na pontuação total do que a ausência de uma etapa processual menor.

* **Treinamento e calibração**: com o máximo de pontuações alcançadas por pergunta no relatório, os gerentes podem ver exatamente onde os alunos têm um desempenho inferior e calibrar os professores sobre como pontuar de forma consistente.

## Suporte a vários idiomas para perguntas da lista de verificação

### Visão geral

O aprimoramento introduz suporte multilíngue para perguntas de listas de verificação, permitindo que os revisores avaliem e pontuem listas de verificação em seu idioma preferido. Esse recurso é particularmente útil em regiões multilíngues e implantações globais, pois permite que os autores criem perguntas de listas de verificação localizadas para cada idioma de conteúdo compatível, mantendo um único módulo de lista de verificação e um processo de avaliação consistente.

No Adobe Learning Manager hoje:

* Todos os módulos voltados para o aluno (SCORM, PDF, HTML etc.) podem ser fornecidos em vários idiomas de conteúdo, permitindo que os alunos escolham o idioma de sua preferência.

* Em um módulo de lista de verificação, os revisores (professores/gerentes) avaliam os alunos com base nas perguntas definidas nessa lista de verificação.

### Novidades

**Criação**

* Os autores agora podem adicionar perguntas da lista de verificação em todos os idiomas selecionados no nível do curso.

* Para cada lista de verificação:

   * Espera-se que o autor forneça um texto de pergunta equivalente em cada idioma de conteúdo no qual o curso existe.

   * Os autores são responsáveis por garantir que o significado de cada pergunta seja consistente em todos os idiomas.

**Experiência de revisão**

* Os revisores verão as perguntas da lista de verificação e a interface de avaliação em seu idioma de conteúdo selecionado.

* Quando uma pergunta é avaliada em um idioma:

   * A avaliação (pontuação, Sim/Não, status) é logicamente a mesma em todos os idiomas. É uma lista de verificação única com várias visualizações de idioma, não listas de verificação separadas por idioma.

**Relatórios**

O relatório Lista de verificação exibirá o texto da pergunta no idioma do conteúdo do usuário:

* Um administrador ou revisor que executa o relatório em cada idioma vê os nomes das perguntas localizadas para esse idioma.

* As respostas e pontuações subjacentes permanecem as mesmas; apenas os rótulos de pergunta são traduzidos.

### Principais benefícios

* **Melhor experiência do revisor**: os revisores podem trabalhar inteiramente em seu próprio idioma, lendo perguntas e gravando avaliações sem barreiras linguísticas.

* **Alinhamento regulamentar e de políticas**: em regiões com requisitos de igualdade de idioma (por exemplo, holandês/francês na Bélgica), as listas de verificação agora podem atender aos mesmos padrões de outros materiais de aprendizado, reduzindo o risco de conformidade.

* **Lógica de avaliação consistente**: enquanto o texto está localizado, a avaliação e a pontuação são compartilhadas em todos os idiomas, garantindo que os resultados sejam comparáveis e gerenciados centralmente.

### Casos de uso

* As franquias de vários países que operam em vários idiomas podem implantar um único curso e uma lista de verificação, fornecendo ao mesmo tempo experiências de revisor localizadas em cada território.

* Qualquer empresa global com professores locais (por exemplo, EMEA, LATAM, APAC) pode fazer com que os revisores trabalhem no idioma local enquanto compartilham o mesmo design e a mesma emissão de relatórios de lista de verificação global.

## Lista de verificação com recurso de comentários para revisor

### Visão geral

O aprimoramento introduz um recurso de comentários para avaliações de listas de verificação, permitindo que os revisores, como professores e gerentes, forneçam feedback qualitativo juntamente com as pontuações numéricas. Esse feedback pode ser exibido aos alunos quando necessário.

O objetivo é apoiar avaliações baseadas em listas de verificação, em que o feedback do mentor é tão crucial quanto o resultado numérico. Isso inclui destacar pontos fortes específicos, áreas para melhoria ou fornecer contexto para a pontuação fornecida.

Atualmente, os revisores podem:

* Avalie uma lista de verificação para cada aluno, pergunta por pergunta.

* Visualize os resultados e reavalie os alunos que falharam.

Em cenários do mundo real, como aviação, treinadores de campo avaliam agentes de chão de fábrica e funcionários do aeroporto. Da mesma forma, os instrutores e mentores em pequenas e médias empresas (PME) frequentemente usam listas de verificação para avaliar o desempenho do trabalho. No entanto, essas listas de verificação geralmente não incluem uma seção estruturada para capturar feedback narrativo relacionado à avaliação.

### Novidades

#### Opções de criação

Os autores podem configurar cada lista de verificação para:

* Ative ou desative a capacidade de comentários dos revisores.

* Decida se o nome do revisor deve ser exibido aos alunos junto com os comentários.

Isso permite que as organizações adaptem a visibilidade dos comentários aos seus requisitos de cultura e privacidade.

#### Experiência do revisor

Quando os comentários estiverem ativados:

* Os revisores (professores/gerentes) podem adicionar comentários opcionais ao avaliar uma lista de verificação.

* Com base nas configurações da lista de verificação, eles podem escolher se os comentários serão visíveis para os alunos.

Se reavaliarem um aluno, eles poderão atualizar ou alterar comentários para refletir a avaliação mais recente.

#### Relatórios e notificações

* O relatório Lista de verificação ganha uma nova coluna para comentários do revisor, capturando o comentário fornecido durante a avaliação.

* Os alunos recebem notificações (na plataforma e por e-mail) sempre que ocorre uma avaliação da lista de verificação. Essas notificações incluem:

   * O comentário e a

   * O nome do revisor, se estiverem configurados para serem visíveis.

Isso garante que o feedback não seja apenas armazenado, mas também exibido ativamente aos alunos.

### Principais benefícios

* **Comentários mais detalhados, semelhantes aos de treinadores**: as pontuações numéricas são complementadas com comentários contextuais, tornando as listas de verificação uma ferramenta mais eficaz para o treinamento, não apenas para a conformidade.

* **Rastreabilidade e auditabilidade**: as organizações obtêm um registro persistente de quem avaliou quem, quando e o que disseram, o que é importante em ambientes regulamentados e funções de alto risco.

* **Melhor envolvimento do aluno**: os alunos recebem orientações claras vinculadas a avaliações específicas, o que melhora sua compreensão das expectativas e etapas subsequentes.

### Casos de uso

* As organizações com ambientes regulamentados podem usar comentários para documentar o julgamento clínico ou feedback de procedimentos para a equipe que está sendo observada em campo.

* As organizações de aviação e de assistência em escala podem anexar notas detalhadas sobre o desempenho operacional, as práticas de segurança e o comportamento voltado para o cliente, transformando uma lista de verificação em uma ferramenta estruturada de apontamento.

* Em mentoreamento e avaliação do SME, os professores podem capturar observações sutis que não se encaixam somente em uma pontuação, por exemplo, “lidaram bem com o escalonamento, mas precisam melhorar o gerenciamento de tempo” ou “fluxo de solução de problemas excelente; perdeu uma etapa de documentação”.

## Várias tentativas em nível de conteúdo e relatórios de questionário

### Visão geral

>[!IMPORTANT]
>
>Observe que o recurso só estará disponível após ser ativado na conta. Entre em contato com o suporte do ALM.


Atualmente, o ALM oferece suporte a várias tentativas no nível do LMS por meio do recurso MQA (Multiple Quiz Attempt):

* Os autores podem configurar tentativas no nível do curso (aplicadas a todos os módulos participantes do curso) ou no nível do módulo (por módulo do questionário).

* As tentativas podem ser:

   * Um número específico (por exemplo, 3 tentativas) ou

   * Tentativas infinitas, controladas no nível do LMS.

* Quando um aluno consome um módulo por meio do Fluidic Player e, em seguida, fecha o player ou conclui o módulo, essa sessão é tratada como uma única tentativa de LMS.

* Cada tentativa de LMS é capturada no relatório do questionário L2 como uma nova linha.

No entanto, se o próprio arquivo de conteúdo (por exemplo, um quiz Articular SCORM) implementar sua própria lógica de várias tentativas, o relatório do quiz L2 do ALM não distingue ou acompanha atualmente essas tentativas internas corretamente.

Esse aprimoramento apresenta o controle de várias tentativas em nível de conteúdo para questionários, permitindo que o Adobe Learning Manager capture com precisão cada tentativa dentro do próprio conteúdo no relatório do questionário L2. Ele foi projetado para situações em que a ferramenta de criação de conteúdo (como Articular SCORM) gerencia as tentativas de questionário de maneira independente. Com esse recurso, as tentativas são refletidas corretamente no relatório do ALM, sem depender das configurações de MQA (Multiple Quiz Attempt) no nível do LMS.

### Novidades

#### Sinalizador de autor para tentativas no nível de conteúdo

* Ao carregar conteúdo na Biblioteca de conteúdo, os autores agora podem indicar que um arquivo de conteúdo específico tem várias tentativas incorporadas.

* Esta é uma configuração por conteúdo que informa ao ALM para tratar as tentativas definidas dentro do conteúdo como a fonte da verdade.

#### Comportamento do curso/módulo

Quando esse conteúdo é usado em um curso:

* O módulo derivará suas tentativas do conteúdo, não do MQA do LMS.

* Os alunos verão apenas uma tentativa de nível LMS:

   * A visão geral do curso e a visualização do módulo não expõem um botão de “nova tentativa” do LMS para esse módulo.

   * A manipulação de tentativas (por exemplo, tentativas repetidas dentro do quiz) é regida pelo próprio conteúdo.

#### Relatórios

O relatório do quiz L2 trata cada tentativa de nível de conteúdo como uma linha de tentativa separada:

* Cada tentativa de quiz interna configurada no conteúdo aparece como sua própria linha no relatório de quiz L2, da mesma forma que as tentativas de nível LMS são representadas hoje.

* O formato de cada linha permanece o mesmo das linhas de várias tentativas existentes no relatório L2 (mesmas colunas, estrutura e semântica).

* Isso proporciona uma experiência consistente de emissão de relatórios:

   * Independentemente de as tentativas serem controladas por MQA do LMS ou pelo conteúdo, o relatório do quiz L2 mostra uma linha por tentativa.

#### Principais benefícios

* Histórico preciso de tentativas para questionários SCORM nos quais as tentativas são controladas internamente por ferramentas como Articular, sem forçar a configuração de MQA no nível do LMS pela parte superior.

* Experiência do aluno mais limpa: para tentativas controladas por conteúdo, os alunos veem um único slot no nível do LMS e não precisam interagir com os controles de nova tentativa do LMS. Todas as novas tentativas são tratadas na interface do questionário que já conhecem.

* Arquitetura flexível: os usuários podem escolher se o ALM MQA ou as tentativas no nível do conteúdo devem determinar o comportamento por módulo, dependendo de como o conteúdo foi criado e de como preferem gerenciar as tentativas.

* Modelo de relatório consistente: os consumidores downstream do relatório do quiz L2 podem tratar cada linha como “uma tentativa”, independentemente de onde a lógica da tentativa se origina.

#### Casos de uso

* As organizações que usam o recurso Articular SCORM podem manter uma lógica de questionário independente no pacote SCORM e, ao mesmo tempo, obter relatórios precisos em nível de tentativa no ALM sem a configuração adicional do LMS.

* As organizações que usam conteúdo SCORM fornecido pelo fornecedor podem evitar a necessidade de modificar ou implementar lógica adicional de tentativa e repetição com MQA no nível do LMS.

## Códigos QR do professor para inscrição de instância e participação na sessão

### Visão geral

Esse aprimoramento adiciona a capacidade de os professores gerarem eles mesmos códigos QR para:

* Inscrição na instância do curso,

* Participação na sessão ou

* Inscrição + participação conjunta

no nível da sessão. Ele foi projetado para situações em que os alunos entram em uma sala de aula física ou híbrida e exigem uma opção rápida de autoatendimento para se inscrever e registrar sua participação usando um código QR.

### Novidades

#### Códigos QR gerados pelo professor

* Os professores podem gerar códigos QR no nível da sessão para:

   * Inscrever-se na instância: os alunos digitalizam para se inscrever na instância que inclui a sessão atual.

   * Marcar participação na sessão: os alunos verificam durante/após a sessão para registrar a participação nessa sessão específica.

   * Inscrever-se na instância + marcar presença na sessão : um QR combinado para entradas que ainda não estão inscritas e precisam que sua participação seja marcada em uma etapa.

* Os professores podem exportar os códigos QR de que precisam com base no cenário (inscrição, participação ou ambos).

#### Empacotamento do código QR

O PDF de QR Code exportado inclui:

* Nome do curso

* Nome da instância

* Nome da sessão

Isso facilita para professores e coordenadores identificarem e imprimirem o código QR correto para cada sessão.

### Principais benefícios

* **Autonomia do professor**: os professores não precisam mais esperar que os administradores criem códigos QR. Eles podem gerá-los diretamente para cada sessão, melhorando a agilidade e reduzindo a sobrecarga de coordenação.

* **Logística de sala de aula aprimorada**: para públicos visitantes ou participantes do local (como funcionários de campo, funcionários de chão-de-fábrica ou participantes externos), os professores podem gerenciar a inscrição e a participação no local usando códigos QR.

* **Carga de trabalho de administrador reduzida**: as equipes de administração podem se concentrar na configuração e governança em vez de lidar com solicitações de geração de código QR de rotina para cada sessão.

### Casos de uso

* As organizações que executam grandes volumes de sessões no local (por exemplo, treinamento de produtos para profissionais) podem permitir que os professores imprimam códigos QR específicos da sessão que se inscrevem e marcam presença com uma digitalização.

* No varejo, na fabricação e no treinamento de saúde, onde os alunos frequentemente participam das sessões diretamente do piso ou sem pré-inscrição, um código QR “Inscrever-se + Participar” pode ser colocado na porta. Isso permite que os alunos façam o autoatendimento da sua inscrição e da presença por meio de seus telefones.

* Os eventos de treinamento para parceiros ou clientes permitem que o instrutor no local se adapte facilmente a alterações na sala, sessões adicionais ou participantes extras sem precisar consultar o administrador para obter novos códigos QR.

## Melhorias no reprodutor de Captivate e ALM

### Visão geral

Esse aprimoramento melhora a experiência de reproduzir conteúdo do Adobe Captivate no reprodutor Adobe Learning Manager (ALM), especialmente após as recentes alterações na arquitetura Captivate. O objetivo é permitir que os alunos se envolvam com módulos de Captivate de forma nativa no ALM, garantindo que a navegação, o rastreamento da conclusão e a anotação sejam claras, consistentes e confiáveis.

### Novidades

#### Experiência de sumário unificado

* Somente o sumário do ALM é exibido no lado esquerdo do reprodutor.

* O sumário de Captivate own fica oculto quando o módulo é reproduzido no ALM.

* Isso elimina a duplicação, garante uma única fonte confiável para a navegação e libera espaço na tela.

#### Feedback de conclusão visual

* O sumário do ALM mostra marcas de escala verdes (ou dicas visuais equivalentes) indicando conclusão no nível do slide.

* À medida que os alunos avançam pelos slides de Captivate, o sumário do ALM reflete quais slides foram concluídos, alinhando-se às expectativas do aluno para os participantes modernos do curso.

#### Controles de progresso contextuais

* Os controles do reprodutor se adaptarão com base no tipo de slide:

   * Para slides de vídeo:

      * Mostrar uma barra de progresso de tempo, refletindo a reprodução do vídeo.

* Para slides que não são de vídeo:

   * Exibir controles de navegação do slide (próximo slide/slide anterior etc.) em vez de uma barra de tempo não funcional.

      * Isso evita mostrar controles irrelevantes ou que não funcionem em determinados tipos de slide.

#### Navegação simplificada

* A barra de navegação separada do módulo (ALM) e a barra de navegação do curso são mescladas em uma única barra intuitiva.

* Esta navegação unificada:

   * Distingue claramente a movimentação pelo módulo do Captivate em comparação à movimentação de volta para o nível do curso/módulo.

   * Reduz a confusão causada por várias barras com fins de sobreposição.

#### Vinculação de notas confiáveis

* As anotações são vinculadas aos números dos slides em vez de carimbos de data e hora.

* Esta alteração:

   * Corrige falhas de exportação causadas por carimbos de data/hora ausentes ou incorretos.

   * Garante que as anotações possam ser exportadas consistentemente como PDF, com um mapeamento confiável entre as anotações e o contexto do slide ao qual pertencem.

### Principais benefícios

* Experiência mais limpa e com um único reprodutor: os alunos interagem com um sumário e um modelo de navegação, reduzindo a confusão e a carga cognitiva.

* Indicações precisas de conclusão e progresso: os tiques no nível do slide e os controles contextuais ajudam os alunos a entender onde estão e o que resta.

* Anotações e exportações mais confiáveis: ao vincular anotações aos slides em vez de carimbos de data e hora frágeis, os usuários recuperam um fluxo de trabalho confiável de anotações para PDF, mesmo com conteúdo de Captivate baseado em slides.

* Fluxo de trabalho de autor preservado: os autores mantêm a simplicidade da publicação direta de Captivate no ALM, enquanto os alunos obtêm uma experiência de reprodução moderna e integrada sem ônus de criação adicionais.

### Casos de uso

* Os programas de ativação que dependem do Captivate para simulações interativas podem implantar conteúdo no ALM, garantindo que a navegação, o rastreamento da conclusão e as notas funcionem de forma consistente para os alunos.

* As organizações que usam o Captivate como ferramenta de criação de conteúdo principal podem manter a publicação em um clique e evitar a confusão de sumários duplos e controles não funcionais para os alunos.

* As organizações que dependem de notas exportadas do conteúdo de Captivate no ALM (para treinamento, conformidade ou registros) podem acessar o seguinte:

   * As observações são vinculadas corretamente aos slides.

   * Os PDF são gerados conforme esperado.

## Melhoria no cálculo do tempo de aprendizado gasto nas transcrições do aluno

### Visão geral

A Adobe Learning Manager revisou como calcula o tempo de aprendizado nas transcrições do aluno com sua versão de abril de 2026. Anteriormente, a lógica do relatório poderia levar a tempos imprecisos se os alunos deixassem o reprodutor aberto sem se envolver com o conteúdo, causando discrepâncias. O novo método agora controla o tempo ativo com base no envolvimento do usuário, especificamente quando a guia está em foco e quando há atividade do usuário. Essa alteração resulta em dados mais precisos.

Essa atualização aprimora relatórios e painéis, ajudando os administradores a garantir melhor conformidade e acompanhar o progresso do aluno. Após o lançamento, revise suas transcrições do aluno para ver esses aprimoramentos.

O método de cálculo atualizado se concentra no envolvimento real, como foco de guia ativo e interações recentes do usuário, melhorando assim a precisão dos relatórios de tempo nas seguintes áreas:

* Transcrições do aluno (UI)
* Métricas do Painel de Administração
* Relatórios de inscrição no curso
* APIs e conectores

### O que mudou

A coluna **Tempo gasto no aprendizado** em transcrições do aluno agora usa lógica aprimorada para calcular o tempo com mais precisão. Em vez de simplesmente rastrear os tempos de abertura/fechamento do player, o sistema agora distingue entre os períodos ativos e ociosos com base no engajamento do usuário.

* **Tempo ativo**: o tempo quando o aluno está ativamente envolvido (por exemplo, na guia correta, executando ações como rolagem ou exibição de vídeo).
* **Tempo ocioso**: tempo quando o aluno não está envolvido (por exemplo, alternado por tabulação, nenhuma atividade por mais de 10 minutos), que é excluído do total.

Isso se aplica à maioria dos tipos de módulo, com exceções para módulos SCORM, Captivate e XAPI, que retêm a lógica original.

### Como funciona

O novo cálculo varia de acordo com o tipo de módulo:

* **Módulos de vídeo e áudio**: ativos quando o conteúdo está sendo reproduzido, mesmo que o aluno alterne para outra guia. O foco da guia não é necessário para controlar o tempo de reprodução.
* **Módulos estáticos (PDF, PPT, Excel etc.)**: ativos se estiverem na guia e executando atividades (movimento do mouse, rolagem, clique, entrada do teclado) nos últimos 10 minutos. Se não houver atividade por 10 minutos, ele alternará para ocioso.
* **SCORM e Captivate** mantêm a lógica de abertura/fechamento original.
* A **xAPI** agora usa a detecção de tempo ativo baseada em tabulação, em que o tempo é contado apenas quando a tabulação está ativa. Observe que o conteúdo AICC **não é** suportado.
* **HTML, LTI e outro conteúdo**: pode variar; verifique as transcrições do aluno para obter precisão.

O tempo ocioso é subtraído, garantindo que apenas o tempo de envolvimento real seja relatado.

>[!NOTE]
>
>Se o notebook entrar no modo de hibernação, o tempo de aprendizado pode não ser rastreado corretamente. Isso ocorre porque o controle de atividades pausa enquanto o sistema está suspenso e reinicia somente quando o laptop é ativado.


### Tabela de resumo

| **Tipo de módulo** | **Tempo ativo (contado)** | **Tempo ocioso (excluído)** |
| --- | --- | --- |
| **Vídeo/Áudio** | Tempo de reprodução | Não iniciado; finalizado; pausado **\>10 min** |
| **Estático (PDF/PPT/DOC)** | Atividade **e** ativa da guia nos últimos **10 min** | Nenhuma atividade **\>10 min**; guia inativa |
| **SCORM** | Tempo relatado pelo tempo de execução do conteúdo | Ocioso não pode ser detectado |
| **Captivate** | Temporização baseada em slide | Ocioso não pode ser detectado |
| **instrução** | Guia ativa | Guia inativa |
| **HTML** | Tempo de abertura do reprodutor com a guia ativa | Guia inativa |
| **Produtor/consumidor de LTI** | Se o conteúdo de LTI for reproduzido no player do ALM (ou seja, o ALM está consumindo conteúdo de LTI hospedado em outro LMS que atua como o Produtor), essa lógica de tempo gasto será aplicada.<br><br>No entanto, se o conteúdo for reproduzido fora do LMS (ou seja, o conteúdo estiver hospedado no ALM, o ALM será o Produtor, mas a reprodução acontecerá em um player externo), essa parte da lógica de cálculo de tempo não será aplicada.  <br>**Observação**: o consumidor de LTI não é compatível com o Adobe Learning Manager. | Guia inativa |

**Observação**:

* **Revisitas e sessões paralelas**: conte como ativo quando as condições acima forem atendidas.
* **Todos os dispositivos, navegadores e idiomas**: incluído; o uso de dispositivos móveis offline é adicionado após a sincronização.

### Benefícios do novo cálculo

* **Relatórios precisos**: elimina os tempos excessivos de jogadores autônomos, fornecendo durações de aprendizado realistas.
* **Melhor conformidade**: oferece suporte a controle preciso para treinamento obrigatório (por exemplo, requisito mensal de 5 horas de uma empresa).
* **Painéis aprimorados**: os gráficos de atividade do usuário e os relatórios de tempo gasto agora refletem o engajamento real.
* **Insights do aluno**: ajuda os administradores a identificarem o progresso genuíno e abordarem alunos desconectados.

### Impacto dos relatórios e das análises

* **Transcrições do aluno:** o “Tempo gasto no aprendizado” agora reflete o **envolvimento real**.
* **Painel de Administração:** as métricas que incluem tempo (por exemplo, blocos de “tempo gasto”, tendências) mostrarão valores **mais baixos, mas mais realistas** em cenários em que o tempo ocioso anteriormente inflacionou os resultados.
* **Relatórios de inscrição do curso:** os campos relacionados ao tempo adotam o **novo cálculo** após o lançamento.
* **Observação de comparabilidade:** como os dados históricos não são recalculados, as análises de séries de tempo que abrangem a data de lançamento podem mostrar uma **alteração de etapa**. Considere anotação ou segmentação por data nas ferramentas de análise.

### API e conectores

* **Não há alterações de esquema** em pontos de extremidade/campos existentes que relatam o tempo gasto.
* **A semântica do campo** foi atualizada para refletir o _cálculo de tempo ativo_ para as sessões **após** a inicialização do recurso.
* **Conectores e exportações** que consomem campos gastos com tempo receberão automaticamente os valores atualizados daqui para frente.

### Compatibilidade retroativa e migração de dados

* **Sessões históricas:** não recalculadas.
* **Novas sessões:** use o **novo** cálculo de tempo ativo.
* **Períodos mistos:** para auditorias ou relatórios longitudinais, segmente por **pré/pós-lançamento** para evitar interpretações incorretas.

### Limitações conhecidas

* O **Conteúdo interativo** (SCORM/Captivate) continua a depender do tempo fornecido pelo conteúdo; a detecção de ociosidade no conteúdo não está disponível.
* O **conteúdo baseado em Iframe** (HTML/xAPI) limita a detecção de interações de granulação fina; o foco de tabulação é usado em seu lugar.

### Perguntas frequentes

**Esta atualização altera registros históricos?**

Não. A alteração se aplica somente a sessões após a inicialização do recurso.

**Como verifico as alterações?**

Verifique as transcrições do aluno para módulos recentes; compare os tempos com as durações esperadas.

**Isso afeta todas as contas?**

Sim, é uma atualização global para todas as contas da Adobe Learning Manager.

**Os alunos precisam realizar uma ação?**

Não. A alteração é automática e transparente para os alunos.

**E se os alunos deixarem o conteúdo aberto?**

O tempo ocioso agora está excluído, evitando a geração de relatórios em excesso.

**As sessões de vídeo/áudio são pausadas automaticamente quando a guia está inativa?**

Não. O comportamento de reprodução não foi alterado. O tempo é excluído quando pausado > 10 minutos ou quando não estiver jogando ativamente.

**A atividade móvel offline será refletida?**

Sim O uso offline é incluído quando o dispositivo é sincronizado.

**O que devo fazer se meus painéis agora mostrarem médias mais baixas?**

Isso é esperado onde o tempo ocioso teve resultados anteriormente inflados. Anote os painéis e ajuste os destinos conforme necessário.

**Existem pré-requisitos?**

Nenhuma; a alteração é automática.

## Atualização dos relatórios de transcrição de aprendizado para administradores

Estamos atualizando os relatórios de Transcrição de aprendizado (LT) para que os administradores ofereçam melhor suporte às avaliações baseadas em lista de verificação e ao feedback do revisor.

## O que está mudando?

### &#x200B;1. Renomear coluna na transcrição do aprendizado do administrador

A coluna **Envio de comentário** existente no Aprendizado do Administrador
A transcrição é:

1. **Renomeado para:** `Reviewer's remarks`

### Dados mostrados nesta coluna:

* **Para módulos de envio:**
A coluna continua a exibir o comentário de envio (sem alteração de comportamento).

* **Para módulos de lista de verificação:**
A coluna agora exibe o comentário de avaliação (as observações do revisor da lista de verificação).

Essa alteração se aplica a todas as origens de LT de administrador:

* LT baixado da interface do administrador
* LT obtido por meio da API de trabalho
* LT gerado através de conectores

Após essa alteração, a mesma coluna contém: - Comentários de envio para módulos de envio

* Comentários de avaliação para módulos de lista de verificação

Sob o novo nome de cabeçalho **Comentários do revisor**.

### &#x200B;2. Nova coluna nas exportações de transcrição de aprendizado baseado em conector

Para transcrições de aprendizado exportadas pelo conector:

* Uma nova coluna chamada **Comentários do revisor** é adicionada ao final do relatório.
* Essa coluna contém os comentários do revisor, alinhados com o comportamento descrito acima:
   * Comentários de envio para módulos de envio
   * Comentários de avaliação para módulos de lista de verificação

## Impacto nas integrações e automações existentes

Se você estiver usando relatórios de transcrição de aprendizado em integrações personalizadas, automações ou ferramentas de relatórios externos, analise os seguintes cenários:

| Cenário | Impacto | Ação necessária |
|----------|--------|----------------|
| É possível identificar campos no LT do administrador pelo nome da coluna (por exemplo, “Comentário de envio”) | O cabeçalho da coluna é alterado para Comentários do revisor. | Sim Atualize qualquer mapeamento ou lógica que faça referência ao comentário de Envio para usar as observações do Revisor. |
| Os campos no LT de administração são identificados apenas pela posição da coluna (com base no índice) | A posição desta coluna permanece a mesma no Admin LT. | Normalmente, nenhuma ação. Se a sua lógica não depender do texto do cabeçalho, nenhuma alteração será necessária para o LT do administrador, basta alterar o nome da coluna se atualmente a coluna “Comentários de envio” for usada. |
| Use o LT exportado pelo conector e use uma contagem de colunas fixa ou uma posição específica na última coluna | Uma nova coluna é anexada ao final do relatório. | Sim Ajuste a lógica de análise ou validação para considerar uma coluna extra no final do arquivo. |
| Use o LT exportado pelo conector e mapeie por nome de coluna | Uma nova coluna Comentários do revisor está disponível. | Opcional. Nenhuma alteração é necessária, a menos que você queira consumir os novos dados de comentários do revisor/lista de verificação. |

**O que você deve fazer**

* Revise todos os scripts, trabalhos de ETL, painéis ou integrações que consomem relatórios de Transcrição de aprendizado do administrador.
* Se você fizer referência ao antigo nome da coluna _Comentário de envio_, atualize sua configuração ou código para usar os comentários do Revisor sobre o novo nome da coluna.
* Se você usar exportações de LT baseadas em conector e assumir um número fixo de colunas ou uma última coluna fixa, atualize sua lógica para manipular uma coluna adicional no final da exportação.

Se a sua implementação atual depende exclusivamente das posições da coluna no Admin LT e não valida ou depende do texto do cabeçalho da coluna, nenhuma alteração é necessária para o próprio Admin LT. Somente exportações de conectores precisam de atenção quando você depende de um layout fixo.


## Experiência não conectada no Experience Builder

A experiência não conectada no Experience Builder permite que as organizações exibam o conteúdo de aprendizado e as páginas do portal para todos os visitantes, incluindo aqueles que não fizeram logon. Esse recurso foi desenvolvido para atrair, informar e envolver alunos potenciais, oferecendo uma visualização suave e com marca de suas ofertas de treinamento antes de exigir que eles façam logon ou se inscrevam.

Esse recurso permite criar e personalizar páginas voltadas para o público usando a mesma interface de arrastar e soltar amigável encontrada no Experience Builder padrão. Você pode exibir catálogos, categorias, caminhos e conteúdo estático avançado do curso, incluindo imagens, texto, HTML e iframes incorporados, para qualquer pessoa que visitar seu portal. Isso simplifica a tarefa de destacar seus programas de aprendizado, promover novos cursos e fornecer informações essenciais a um público mais amplo.

Os visitantes podem navegar no catálogo, visualizar detalhes sobre cursos e instâncias e utilizar a pesquisa global para explorar as oportunidades de treinamento disponíveis. No entanto, ações que exigem a identidade de um usuário, como se inscrever em um curso, acessar recursos personalizados (como Calendário, Conformidade, Quadro de classificação ou Aprendizado social) ou realizar treinamento exigirão que o visitante faça logon. Essa abordagem garante que informações confidenciais e personalizadas permaneçam seguras, ao mesmo tempo em que permite uma experiência de visualização abrangente.

Os administradores têm a capacidade de configurar quais páginas e widgets ficam visíveis para usuários que não estão conectados, garantindo que apenas o conteúdo adequado seja exibido. As páginas podem ser configuradas para serem acessíveis a usuários conectados e não conectados ou exclusivamente para um desses grupos. O Experience Builder oferece um modo de visualização, permitindo que você veja exatamente como as páginas serão exibidas aos visitantes antes que sejam publicadas.

Para ativar esse recurso, o administrador de integração do ALM deve ativar o Conector de Acesso a Dados de Treinamento. Esse conector garante que os metadados do curso estejam acessíveis publicamente.

A identidade visual e a localização são totalmente compatíveis, permitindo que você personalize títulos de página, favicons e configurações de idioma para alinhar com a identidade da sua organização e atender às necessidades do seu público. Como parte da transição para essa experiência aprimorada, o recurso de página inicial herdada para usuários não conectados será descontinuado. Portanto, todo conteúdo público novo deve ser criado usando o Experience Builder.

### Finalidade do recurso

A experiência não conectada no Experience Builder permite que as organizações exibam publicamente seu conteúdo de aprendizado e páginas do portal para qualquer pessoa, sem exigir que os usuários façam logon. Isso ajuda a atrair, informar e envolver alunos potenciais, fornecendo uma visualização do treinamento e dos recursos disponíveis antes que a inscrição ou a autenticação seja necessária.

### Casos de uso reais em experiência não conectada

* **Marketing e extensão**: as organizações podem promover seus programas de treinamento para públicos externos, como clientes potenciais, parceiros ou candidatos a emprego, tornando catálogos de cursos e detalhes do programa acessíveis publicamente.
* **Exploração de pré-inscrição**: os alunos podem procurar cursos disponíveis, visualizar visões gerais e explorar categorias antes de decidir se inscrever ou fazer logon, ajudando-os a tomar decisões de inscrição informadas.
* **Portais de treinamento corporativo**: as empresas podem fornecer um portal público para informações de conformidade ou integração, permitindo que novos contratados ou prestadores de serviço vejam qual treinamento está disponível antes de receberem credenciais.
* **Páginas de aterrissagem de evento ou campanha**: as organizações que executam campanhas de aprendizado ou eventos podem criar páginas públicas dedicadas para destacar cursos, agendas ou recursos em destaque, aumentando a visibilidade e o envolvimento.
* **SEO e capacidade de descoberta**: ao tornar públicas páginas e catálogos selecionados, as organizações melhoram a visibilidade de seus mecanismos de pesquisa, ajudando as pessoas a descobrir suas ofertas de aprendizado online.

### Principais conceitos de experiência não conectada

A experiência não conectada do Experience Builder permite exibir publicamente conteúdo de aprendizado e páginas do portal, permitindo que os visitantes naveguem sem fazer logon.

* **Criar páginas e menus públicos**: você configura páginas e um único menu que todos podem acessar, independentemente do status de logon.
* **Adicionar apenas widgets com suporte**: você inclui widgets que não precisam de contexto de usuário (categorias, cursos e caminhos de aprendizado, caixa de conteúdo, HTML, iframe), enquanto o sistema oculta widgets específicos do usuário.
* **Configurar comportamento de página adaptável**: você decide se uma página é exibida para usuários conectados e não conectados, e o sistema adapta widgets visíveis e conteúdo com base no estado de logon.
* **Visualize as duas experiências**: use opções de visualização para ver como as páginas são exibidas para usuários conectados e não conectados, com diferenças na visibilidade e no conteúdo do widget.
* **Habilitar pesquisa global**: os visitantes pesquisam cursos e conteúdo, mas só obtêm recursos de pesquisa básicos sem integração avançada com IA.
* **Permitir que os visitantes pesquisem o catálogo e as visões gerais do curso**: os visitantes exploram páginas do catálogo, detalhes do curso e instâncias, mas devem fazer logon para se inscrever ou acessar recursos personalizados.
* **Personalizar identidade visual e localização**: defina favicons e configurações de idioma para atender às necessidades de identidade visual e acessibilidade da sua organização.
* **Habilitar o Conector de Acesso a Dados de Treinamento**: ative este conector para exportar metadados do curso para exibição pública, mantendo atualizadas as páginas não conectadas.
* **Tratar alto tráfego com infraestrutura compartilhada**: o sistema gerencia grandes volumes de visitantes anônimos usando recursos compartilhados e limitação de taxa.
* **Otimizar para SEO**: a plataforma prepara páginas públicas para indexação do mecanismo de pesquisa, tornando mais simples de localizar o conteúdo de aprendizado.

### Pré-requisitos para experiência não conectada

* Você deve ativar o Conector de acesso a dados de treinamento no administrador de integração antes de usar a experiência não conectada.
* O conector exporta os metadados do curso para um repositório público, que mantém as páginas não conectadas atualizadas.

#### Inicialização do conector de acesso a dados de treinamento

O conector TDA (Training Data Access, acesso a dados de treinamento) é um pré-requisito crítico para ativar o novo recurso criador de experiências não conectado no ALM. Esse conector facilita a exportação de metadados de treinamento, permitindo que seu portal exiba as informações do curso para os usuários que não estão conectados.

* **Ativação do conector**: você deve habilitar o conector TDA no painel do administrador de integração. Essa etapa ativa a funcionalidade do criador de experiências não conectado e torna visíveis as opções de interface relevantes na interface do administrador.
* **Exportação de metadados**: depois de ativado, o conector exporta metadados de treinamento essenciais (como nome do curso, descrição, visão geral, classificação, duração e habilidades) do ALM para um repositório público. Esses dados são usados para preencher páginas e widgets que não estão conectados.
* **Agendamento e sincronização**: o processo de exportação pode ser agendado (por exemplo, diariamente) para garantir que seu portal reflita as atualizações mais recentes do curso. As alterações feitas no ALM aparecerão em suas páginas não conectadas após o próximo ciclo de exportação, sujeitas ao armazenamento em cache e à frequência de exportação.
* **Disponibilidade de recursos**: os recursos do Experience Builder não conectados, incluindo criação de menus, suporte a widgets e visibilidade de catálogo, só são acessíveis depois que o conector TDA é inicializado. Se o conector não estiver ativado, o Experience Builder permanecerá limitado a cenários de usuário conectado.
* **Migração e suporte**: para contas que estão migrando de recursos de home page não conectados, inicializar o conector TDA é a primeira etapa para a migração. Isso garante que você possa usar a flexibilidade e os recursos aprimorados do novo criador de experiências.


### O que os visitantes podem fazer sem fazer logon

Em um site não conectado do Experience Builder, os visitantes podem navegar pelo catálogo de treinamento abrindo a página do catálogo de catálogos públicos. Eles podem usar filtros como catálogo, produto, função, tipo, habilidades e tags, dependendo de como você configurou o site. Os visitantes também podem pesquisar treinamentos usando a barra de pesquisa global no cabeçalho (se ativada) e exibir os resultados da pesquisa diretamente na página do catálogo.

Os visitantes podem exibir detalhes do treinamento abrindo páginas de visão geral para cursos, programações de aprendizado e certificações. Essas páginas exibem os principais metadados, incluindo título, descrição, autor, duração, formato, tags e habilidades.

Além disso, os visitantes podem explorar conteúdo estático e promocional. Eles podem ler blocos de texto e conteúdo avançado, exibir banners e blocos de imagens e interagir com iframes incorporados, como microsites externos, vídeos ou ferramentas.

Se um visitante clicar em Inscrever-se ou tentar iniciar o treinamento, o sistema solicitará que faça logon ou se inscreva. Após o login bem-sucedido, o visitante é redirecionado para a página apropriada, seja ela a página inicial, uma página personalizada ou o treinamento específico selecionado.

### O que não está disponível sem efetuar login

Em um site não conectado do Experience Builder, os visitantes não podem acessar recursos ou conteúdo que exigem autenticação do usuário. Eles não podem se inscrever em treinamentos, iniciar ou consumir cursos ou acessar widgets personalizados, como Meu aprendizado, Calendário, Conformidade, Quadro de classificação ou Aprendizado social. Esses widgets dependem de dados específicos do usuário e só ficam disponíveis após o login.

Os visitantes também não podem executar ações como se inscrever em um curso ou acessar qualquer conteúdo que exija acompanhamento do progresso ou do contexto do usuário. A tentativa de se inscrever ou iniciar um treinamento solicita que o visitante faça logon ou se inscreva antes de continuar.

### Widgets compatíveis em modo não conectado

No modo não conectado, somente os widgets que não exigem dados específicos do usuário são compatíveis. São eles:

* O widget Categorias, que exibe as categorias de treinamento disponíveis.
* Widget Cursos e caminhos, que mostra cursos e caminhos de aprendizado do catálogo público.
* Caixa Conteúdo, para adicionar texto estático, imagens ou conteúdo promocional.
* widget HTML, para incorporar o conteúdo de HTML personalizado.
* Widget Iframe, para exibir sites, vídeos ou ferramentas externas na página.
* Os widgets que exigem contexto de usuário, como Meu aprendizado, Calendário, Conformidade, Quadro de classificação e Aprendizado social, não estão disponíveis no modo não conectado.

### Páginas e menus na experiência não conectada

* Somente um menu não conectado é suportado, visível para todos os visitantes sem autenticação.
* As páginas podem ser adicionadas a menus conectados e não conectados; se uma página estiver em ambos, ela adapta seus widgets e conteúdo com base no estado de logon do usuário.
* Menus não conectados não têm direcionamento de público ou personalização. Todos veem o mesmo conjunto de páginas.
* Os widgets não compatíveis com o modo não conectado são ocultados automaticamente; o layout da página se ajusta para preencher as lacunas.
* O gerenciamento de menus e páginas (adição, visualização, exclusão) é semelhante ao modo conectado, mas com adaptações para restrições não conectadas.

### Comportamento de pesquisa e catálogo

No modo não conectado, os usuários podem acessar a página do catálogo e usar a pesquisa para procurar cursos e programações de aprendizado disponíveis. A página do catálogo exibe todos os cursos públicos, juntamente com os filtros e a funcionalidade de pesquisa, seguindo as mesmas configurações de conta que no modo conectado. Quando um usuário pesquisa, os resultados aparecem na página do catálogo e os usuários podem visualizar as páginas de visão geral do curso e da instância sem fazer logon. No entanto, ações como inscrição exigem logon.

Se um usuário tentar se inscrever, o sistema exigirá que ele faça logon primeiro. A pesquisa por usuários não conectados é mais simples do que a pesquisa por usuários conectados e não inclui recursos avançados, como a integração do Assistente do AI.

### Implementação técnica

#### Configuração do conector de acesso a dados de treinamento

Você deve ativar o conector de acesso a dados de treinamento no painel do administrador de integração antes de usar o recurso criador de experiências não conectado. Esse conector exporta metadados de treinamento do ALM para um repositório público, tornando-o acessível por meio de APIs para páginas não conectadas. A configuração do conector é um pré-requisito para ativar o recurso e garante que seu portal exiba informações de treinamento atualizadas.

#### Exportação e sincronização de metadados

O conector exporta os principais campos de metadados, como nome do curso, visão geral, descrição, classificação, duração e habilidades. Você pode agendar exportações (por exemplo, diariamente) para manter seu portal sincronizado com o ALM. Nem todos os campos de metadados podem ser incluídos; consulte a equipe de engenharia para obter uma lista completa. Os dados exportados são usados para preencher páginas não conectadas e as alterações no ALM aparecerão após o próximo ciclo de exportação.

#### Frequência de cache e exportação

O sistema usa a frequência de exportação de back-end e o cache de front-end para gerenciar as atualizações de dados. As alterações feitas no ALM são refletidas em seu portal após a exportação agendada e a atualização do cache. Algumas atualizações podem não aparecer imediatamente devido a esses mecanismos. Se precisar de atualizações mais rápidas, ajuste o agendamento de exportação ou limpe o cache conforme necessário.

#### Suporte à personalização de CSS/JS

Você pode aplicar CSS personalizado e JavaScript a páginas conectadas e não conectadas usando a guia Personalização. Isso permite manter a consistência de marca, adicionar elementos personalizados de interface e aprimorar a experiência do usuário em todo o portal. Todas as personalizações são aplicadas globalmente, garantindo uma aparência unificada.

#### Diferenças de URL e marcas (favicon, título da página)

Páginas não conectadas e conectadas podem ter URLs diferentes para distinguir os estados de usuário. Você pode personalizar o favicon e o título da página do seu portal, ajudando a reforçar a identidade da sua marca. Esses recursos estão disponíveis no Experience Builder. Consulte o departamento de engenharia para obter o status mais recente no suporte não conectado.

### Desempenho e escalabilidade

#### Pilha compartilhada vs. pilha premium

A pilha compartilhada permite que vários clientes usem o criador de experiências não conectado em uma infraestrutura comum, oferecendo suporte a níveis de tráfego padrão. A pilha premium é uma opção paga que fornece recursos dedicados, recursos em tempo real e limites de vagas mais altos para clientes com necessidades avançadas. Selecione a pilha com base no tráfego esperado e nas necessidades dos negócios.

#### Limites de tráfego e limitação da taxa

A pilha compartilhada impõe limites de tráfego para garantir o uso justo entre os clientes. A engenharia implementará a limitação de taxa para evitar que um único cliente consuma todos os recursos. Se você planeja campanhas de marketing ou espera alto tráfego, coordene-se com a engenharia para entender seus limites e evitar interrupções no serviço. A limitação de taxa ajuda a manter a estabilidade e o desempenho do sistema para todos os usuários.

#### Considerações sobre multilocação e SEO

A plataforma oferece suporte a multilocação, permitindo que vários clientes hospedem seus portais em uma infraestrutura compartilhada. As páginas não conectadas são compatíveis com SEO, juntamente com sitemap.xml e robots.txt para otimizar a visibilidade do mecanismo de pesquisa. Isso garante que seu portal seja detectável e indexado adequadamente pelos mecanismos de pesquisa.

### Migração e obsolescência

#### Transição da página inicial não conectada existente

Você deve recriar sua página inicial usando o novo Experience Builder para flexibilidade aprimorada, suporte a widgets e experiência do usuário aprimorada. O plano de transição garante interrupção mínima e suporte contínuo.

#### Plano de comunicação

Os clientes que usam a página inicial herdada receberão uma comunicação clara sobre o cronograma de descontinuação e as etapas de migração. Será fornecido suporte para ajudá-lo a mover sua página inicial para a nova plataforma do Experience Builder, garantindo que você se beneficie de novos recursos e atualizações contínuas.

### Suporte a localização e login

#### Lógica de fallback de localidade

O sistema exibe as páginas no local em que foram criadas. Se a localidade de um usuário não estiver disponível, o sistema usará uma lógica de fallback para selecionar a próxima melhor localidade disponível. Isso garante que os usuários sempre vejam o conteúdo em um idioma compatível, melhorando a acessibilidade e a satisfação do usuário.

#### Tipos de logon compatíveis

A experiência não conectada é compatível com todos os tipos de logon disponíveis no ALM, incluindo logon único e logon padrão. Os usuários podem navegar pelo conteúdo sem fazer logon e serão solicitados a fazer logon quando necessário, como se inscrever em um curso ou acessar recursos personalizados. Isso fornece uma transição tranquila da navegação para o engajamento.


### APIs não conectadas

#### API do objeto de aprendizado do administrador

As páginas do Experience Builder e os portais sem periféricos não conectados geralmente organizam ou filtram cursos com base no produto e na função. A API do Admin LO foi aprimorada para garantir que essas associações sejam acessíveis consistentemente para integrações back-end e sem periféricos, bem como para o conector TDA.

**Ponto de extremidade e comportamento**

Você continua a usar o ponto de extremidade do OA do administrador existente:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Onde:

* loId é a ID do objeto de aprendizado (por exemplo, curso:12345).
* enforcedFields[learningObject] instrui a API a incluir explicitamente produtos e funções para esse LO.

Isso é feito garantindo que as associações de produto e função do OA estejam presentes na resposta quando solicitadas por meio de enforcedFields. A resposta contém, em atributos, os metadados de produto e função necessários para calcular ou expor os produtos (rec\_products) e funções (rec\_roles) recomendados para o Experience Builder e outros consumidores.

Uma chamada típica de um administrador ou integração se parece com:

```
url -X GET \
 "https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json
```

O JSON do LO retornado tem a mesma estrutura básica de antes, mas agora você pode confiar na presença dos campos de produto/função ao solicitá-los por meio de enforcedFields. As integrações que não usam enforcedFields continuam se comportando como antes.

#### Listagem de objetos de aprendizado - Suporte a JobAid no filtro effectiveModifiedDate

**Finalidade**

O conector TDA (Acesso a dados de treinamento) e as implementações sem periféricos geralmente precisam executar uma sincronização incremental, com base na **data de modificação efetiva** dos objetos de aprendizado. Até esta versão, as ajudas de tarefa (do tipo OA, ajuda de tarefa) não eram tratadas corretamente quando combinadas com os filtros effectiveModifiedDate. Esta versão corrige isso para que as ajudas de tarefa possam ser sincronizadas incrementalmente, como cursos e programações de aprendizado.

**Ponto de extremidade e comportamento**

Você usa o ponto de extremidade da listagem do LO existente com filtros de data e tipo de LO:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z
 &filter.loTypes=jobAid
```

Anteriormente, quando filter.loTypes=jobAid era combinado com um intervalo effectiveModifiedDate, o filtro excluía efetivamente JobAids e a chamada se comportava como se JobAids não fosse suportado.

A partir dessa atualização, a chamada retorna apenas objetos de aprendizado JobAid cuja effectiveModifiedDate esteja dentro da janela especificada.

```
{
 "links": {
 "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"
 },
 "data": [
 {
 "id": "jobAid:144968",
 "type": "learningObject",
 "attributes": {
 "authorNames": ["Author"],
 "dateCreated": "2026-01-20T08:48:55.000Z",
 "datePublished": "2026-01-20T08:48:55.000Z",
 "dateUpdated": "2026-01-20T08:48:55.000Z",
 "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",
 "loType": "jobAid",
 "loFormat": "Content",
 "loResourceType": "Content",
 "localizedMetadata": [
 {
 "description": "Link jobAid new",
 "locale": "en-US",
 "name": "Link jobAid new"
 },
 {
 "description": "Link jobAid new fre",
 "locale": "fr-FR",
 "name": "Link jobAid new fre"
 }
 ],
 "relationships": {
 "authors": {
 "data": [
 { "id": "13385176", "type": "user" }
 ]
 },
 "instances": {
 "data": [
 { "id": "jobAid:144891\_-1", "type": "learningObjectInstance" }
 ]
 }
 }
 }
 }
 ]
}
```

Isso significa que agora você pode implementar com segurança sincronizações incrementais de JobAid com base em effectiveModifiedDate, da mesma maneira que você já faz para outros tipos.

Se você omitir filter.loTypes=jobAid, o comportamento de outros tipos de LO não será alterado; a alteração afetará apenas a combinação de JobAid com esse filtro.

#### **API de menu: filtro de menu não conectado**

**Finalidade**

O Experience Builder e os front-ends sem periféricos precisam de uma maneira direta de recuperar o **menu não conectado**, aquele que define a navegação para visitantes públicos. Antes desta versão, você tinha que buscar todos os menus e, em seguida, aplicar a lógica personalizada para identificar qual representava a navegação não conectada. Esta versão adiciona um filtro simples do lado do servidor.

**Ponto de extremidade e comportamento**

Use o ponto de extremidade da listagem de menus existente com um novo parâmetro de consulta:

```
GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true
```

Os pontos principais:

* include=pages,subMenus.pages é opcional, mas recomendável quando precisar dos detalhes da página e da página do submenu na mesma resposta.
* isNonLoggedIn=true é novo nesta versão e instrui o servidor a retornar somente menus sinalizados como menus não conectados.

Sem o parâmetro isNonLoggedIn, o ponto de extremidade se comporta exatamente como antes e retorna menus de acordo com o comportamento padrão existente. Com isNonLoggedIn=true, ele normalmente retorna o menu único usado pela experiência não conectada para sua conta (já que normalmente há um menu não conectado por conta).

Na prática, um cliente agora pode emitir:

```
curl -X GET \
 "https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json"
```

e obtenha de volta a estrutura de navegação não conectada em uma chamada, com todas as páginas que devem estar visíveis para visitantes anônimos.

Isso é particularmente útil ao criar um site independente não conectado e desejar espelhar a mesma navegação que o Experience Builder usa ou ao depurar se o menu não conectado foi configurado corretamente.

### Permitir listagem de domínios personalizados

A pilha não conectada consiste em:

* Um domínio CDN público (por exemplo, cpcontents.adobe.com ou yourdomain.example.com) que fornece layouts, config JSON e ativos estáticos.
* Um ponto de extremidade de Elasticsearch público (ES) que fornece dados de catálogo e pesquisa, mas somente se a solicitação vier de um **domínio com lista de permissões** para essa conta do ALM.

Quando você introduz um domínio personalizado, ele funciona perfeitamente sem nenhum esforço adicional após o processo existente para adicionar um domínio personalizado.

#### Pré-requisitos

Antes de incluir na lista de permissões um domínio personalizado para usuários não conectados:

1. O domínio personalizado é configurado para sua conta ALM (por exemplo, DNS para academy.yourcompany.com aponta para Adobe / Akamai e certificados são provisionados).
2. O **conector TDA (Acesso a Dados de Treinamento)** está habilitado para a conta.
3. O recurso **Experience Builder** não conectado está habilitado (lado Adobe).

Essas etapas garantem que:

* Sua conta tem um JSON **de conta não conectado (geralmente referenciado como accountConfig / experienceBuilderConfig), que inclui campos como cpDomain, almDomain, almCdnBaseUrl, esBaseUrl e domínios com permissão listada.**
* A pilha não conectada sabe onde fornecer dados e de que domínios deve aceitar solicitações.

#### Como funciona a listagem de permissões

A lista de permissões é armazenada na configuração que o TDA exporta e a pilha não conectada lê. Essa configuração inclui:

* Os domínios do ALM (cpDomain, almDomain).
* A **URL base da CDN** para conteúdo não conectado (almCdnBaseUrl).
* A **URL de base de pesquisa pública** (esBaseUrl).
* A lista de domínios que podem fazer chamadas públicas não conectadas para essa conta.

Para que o Experience Builder não conectado funcione em um domínio personalizado:

* O navegador deve carregar o HTML não conectado desse domínio personalizado (ou do domínio CDN não conectado ao ALM, dependendo da sua configuração).
* Chamadas desse domínio para os endpoints públicos ES e CDN devem ser aceitas. Isso só acontece se o domínio estiver presente na lista de permissões.

Esta versão adiciona um novo domínio CDN não conectado, cpcontents.adobe.com, e especifica que ele deve ser colocado nos **domínios listados de permissão** no conector TDA. Para usuários nativos não conectados, isso requer uma atualização.

#### Permitir listagem de um domínio personalizado

**Configurar o domínio personalizado no ALM**

Trabalhe com o Adobe para registrar seu domínio, por exemplo, academy.yourcompany.com, como o domínio personalizado para sua conta do ALM. Você atualiza o DNS para apontar para o Adobe Akamai, conforme instruído, e aguarda a conclusão do SSL e do roteamento.

Nesse ponto, o tráfego conectado e não conectado pode acessar o ALM por meio desse domínio, mas chamadas de pesquisa e catálogo não conectadas ainda poderão ser bloqueadas se o domínio não estiver na lista de permissões.

**Habilitar TDA e Experience Builder não conectado**

Verifique se:

* O **Conector de Acesso a Dados de Treinamento** está habilitado.
* O recurso **Experience Builder não conectado** está ativado para a conta.

A ativação do TDA cria ou atualiza o JSON da conta não conectada. Para novas contas, o processo também permite a pré-listagem do novo domínio CDN não conectado (cpcontent.adobe.com) por padrão, de modo que o ponto de extremidade ES público espera chamadas desse domínio.

Para contas que já estavam usando a pilha não conectada mais antiga, os conectores existentes devem ser excluídos e recriados para selecionar o novo domínio.

**Adicionar o domínio personalizado à lista de permissões**

A parte crítica é informar à pilha ES não conectada que academy.yourcompany.com é uma origem aprovada. Há dois caminhos comuns.

1. **Reabilite o conector TDA (simples, amigável ao autoatendimento)**

Os usuários nativos não conectados precisarão excluir e reativar a conexão TDA para que o novo domínio seja automaticamente incluído na lista de permissões. Isso permite duas coisas:

1. A conta não conectada JSON é gerada novamente.
2. Os domínios listados de permissão são atualizados para incluir o novo domínio CDN não conectado e seu domínio personalizado.

Isso é recomendado quando você tem um pequeno número de contas e pode tolerar a desativação e reativação temporárias do conector.

1. **Verifique se o domínio está na lista de permissões**

Após a listagem de permissões, abra o site não conectado no domínio personalizado e inspecione as chamadas de rede do navegador.

Você deseja ver:

* Solicitações para almCdnBaseUrl (por exemplo, <https://cpcontent.adobe.com/>...) 200/304.
* Solicitações para esBaseUrl (API de pesquisa pública, por exemplo <https://primeapps.adobe.com/almsearch/api/v1/>...) êxito ao retornar JSON com dados de pesquisa/catálogo.

Se essas chamadas retornarem 4xx ou erros explícitos sugerindo “domínio não confiável” ou “origem não permitida”, a lista de permissões estará incompleta ou configurada incorretamente e o suporte precisará ajustá-la.

O LLD não conectado também observa que a configuração da conta pode conter um valor de domínio esperado. No tempo de execução, o site verifica se o domínio no URL corresponde ao que está definido na configuração; se não corresponder, o usuário poderá ser redirecionado para uma página de erro. Isso protege contra o acesso da configuração de um cliente por meio do domínio de outro cliente.

### Usar recomendações no Experience Builder não conectado

O Experience Builder não conectado permite criar páginas de aprendizado públicas nas quais os visitantes podem navegar no catálogo e ver o conteúdo destacado antes de fazer logon. Mesmo que esses visitantes sejam anônimos, você ainda pode apresentar treinamentos recomendados usando metadados e widgets.

No aplicativo do aluno conectado, as recomendações podem ser personalizadas: elas podem depender do perfil, do histórico, das habilidades e do progresso do aluno. Na experiência **não conectada**, ainda não há nenhuma identidade do aluno, portanto, a plataforma não pode personalizar por usuário.

O Recommendations no modo não conectado é:

* **Com curadoria ou baseado em regras**: baseado em catálogo, produto, função, rótulos, marcas e outros metadados.
* **Orientado a segmentos**: “recomendado para desenvolvedores”, “recomendado para parceiros”, “apresentado para iniciantes”.
* **Foco em marketing**: usado para atrair e orientar os visitantes a se inscreverem assim que fizerem logon.

### Metadados e APIs que oferecem suporte a recomendações

Em segundo plano, as páginas não conectadas usam:

* O **conector TDA** para exportar metadados de objetos de aprendizado (cursos, caminhos, certificações, ajudas de tarefa) para um índice de pesquisa público.
* A **pilha de pesquisa pública** para responder a consultas de widgets não conectados (catálogo, pesquisa, cursos e caminhos, categorias).
* A **API de Objetos de Aprendizado de Administrador** para expor metadados de produto e função que podem ser usados para regras de recomendação.

Nesta versão, a API do Admin LO foi estendida para que as associações de produto e função estivessem disponíveis de forma confiável:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Isso permite que widgets e integrações sem periféricos criem recomendações baseadas em regras usando produtos, funções, etiquetas de catálogo, tags e outros campos de forma consistente.

### Criar seções de recomendação com os widgets do Experience Builder

Crie seções de recomendação em páginas não conectadas ao combinar **widgets do Experience Builder** com filtros de metadados.

#### **Widget Cursos e caminhos**

Use o widget **Cursos e caminhos** quando quiser mostrar uma linha ou grade de itens recomendados. Em sua configuração, você pode escolher:

* De quais catálogos extrair.
* Quais rótulos de catálogo, produtos, funções ou tags usar como filtros.
* Se deve mostrar cursos, caminhos, certificações, ajudas de tarefa ou uma combinação.
* Classificação e número máximo de itens.

Por exemplo, você pode criar:

* “Recomendado para desenvolvedores”: filtre por produto ou função usada para conteúdo de desenvolvedor.
* “Iniciar aqui”: filtre por um rótulo, como “Inicial” ou “Integração”.
* “Este trimestre em destaque”: filtre por um rótulo com limite de tempo, como destaque-q3-2026.

O widget não está aprendendo com o comportamento. Ele mostra tudo o que corresponde às regras de metadados que você definir. Do ponto de vista de um visitante, no entanto, parece uma faixa de recomendação.

#### **Widget de categorias**

Use o widget **Categorias** para ajudar os visitantes a navegar nos conjuntos de conteúdo “recomendados”, mesmo que eles não saibam os nomes dos seus produtos.

É possível configurar ladrilhos que representem um segmento, como:

* “Para administradores”
* “Para equipes de vendas”
* “Para parceiros”
* “Por linha de produto”

Cada bloco pode ser vinculado a:

* Uma página de catálogo filtrada (por exemplo, o catálogo filtrado por determinados produtos ou rótulos).
* Uma página dedicada não conectada que usa cursos e caminhos pré-configurados para esse segmento.

Isso proporciona uma experiência de “caminhos recomendados por segmento” sem personalização.

### Criação de recomendações baseadas em segmentos

Como os visitantes não conectados ainda não têm um perfil ALM, é útil criar recomendações **por segmento** e permitir que os visitantes selecionem por conta própria.

1. Use uma **página inicial não conectada** que explique brevemente para quem é a sua academia e mostre um pequeno número de pontos de entrada de segmento (por exemplo, “Desenvolvedores”, “Profissionais de marketing”, “Parceiros”, “Novos funcionários”). Isso pode ser feito com um widget Categorias ou uma caixa de Conteúdo ou seção HTML simples com botões.
2. Para cada segmento, crie uma **página dedicada não conectada** no Experience Builder. Nessa página, use um ou mais widgets Cursos e caminhos configurados com filtros que representem o que é “recomendado” para esse grupo. Por exemplo, para “Desenvolvedores” você pode filtrar em:
   1. Catalog = “Treinamento público”
   2. Produto = &quot;Adobe Experience Manager&quot;
   3. Tags = “Fundamentos do desenvolvedor”
3. Use essas páginas de segmento como destino de suas campanhas de marketing e como destino dos blocos na home page não conectada.

Os visitantes percebem que estão vendo recomendações personalizadas para sua situação, mesmo que a lógica seja definida em tempo de design através de metadados.

### Transição de recomendações não conectadas para personalizadas

As recomendações não conectadas são principalmente sobre **capacidade de descoberta** e **conversão**. Depois que os visitantes decidirem se inscrever ou iniciar o treinamento, eles farão logon e se tornarão alunos completos com um perfil e um histórico.

O fluxo normal é:

1. Um visitante descobre conteúdo por meio de seções de recomendação não conectadas (recomendações iniciais, páginas iniciais de segmentos, linhas em destaque).
2. Eles clicam em uma visão geral do curso ou caminho e escolhem se inscrever ou começar.
3. O ALM solicita que se inscrevam ou façam logon.
4. Depois de fazer logon, a experiência padrão do aluno conectado assume o controle, incluindo:
   1. “Meu aprendizado”
   2. Catálogo conectado com progresso pessoal
   3. Qualquer sistema de recomendação interno usado para os alunos existentes.

Em outras palavras, as recomendações conectadas os ajudam a decidir o que fazer em seguida e a continuar.

### Como as ajudas de tarefa podem ser usadas no novo Experience Builder não conectado

Na **Interface de Usuário**, as ajudas de tarefa participam de experiências não conectadas principalmente por meio de widgets que podem mostrar objetos de aprendizado:

1. **Widget de cursos e caminhos**
Este widget pode mostrar vários tipos de objeto de aprendizado, incluindo ajudas de tarefa. Em páginas não conectadas, você pode configurá-las para:
   1. Incluir ou excluir ajudas de tarefa explicitamente.
   2. Filtre ajudas de tarefa por catálogo, produto, função, rótulos, marcas e outros metadados.
   3. Apresente-os ao lado de cursos e caminhos ou como uma faixa separada de “Recursos”.

Por exemplo, em uma página de aterrissagem pública, você pode configurar uma faixa intitulada “Recursos úteis”, que mostra apenas ajudas de tarefa, e outra faixa intitulada “Cursos recomendados”, que mostra cursos e caminhos.

1. **Página e pesquisa do catálogo**
As superfícies do **catálogo** e da **pesquisa** não conectadas usam o índice de pesquisa público (alimentado pelo conector de Acesso a Dados de Treinamento). Esse índice agora suporta ajudas de tarefa corretamente, portanto:
   1. Os resultados de pesquisa não conectados podem incluir ajudas de tarefa.
   2. Filtros de catálogo não conectados (por tipo, produto, marcas etc.) pode incluir ajudas de tarefa, desde que a configuração da sua conta e os widgets estejam configurados para exibi-los.
2. **Páginas de visão geral do LO**
Quando um visitante clica em uma ajuda de tarefa de qualquer widget ou do catálogo, ele vai para uma **página de visão geral do OA** dessa ajuda de tarefa no modo não conectado. A partir daí, eles podem ler a descrição e os metadados. O download ou o consumo real normalmente ainda requer logon, mas a presença e a capacidade de descoberta da ajuda de tarefa em si são tratadas pela experiência não conectada.

### Como as ajudas de tarefa são expostas por meio de APIs não conectadas

No **lado da API**, as ajudas de tarefa são suportadas por:

1. O **Conector de Acesso a Dados de Treinamento e a pesquisa pública**
O TDA exporta metadados de ajuda de tarefa junto com outros tipos de objeto de aprendizado para o índice de pesquisa pública que atende a consultas de pesquisa e catálogo não conectadas. É nisso que o Experience Builder e as frontends sem periféricos dependem.
2. A listagem de **Objetos de Aprendizado com effectiveModifiedDate**
Nesta versão, o ponto de extremidade da lista de OAs foi corrigido para que as ajudas de tarefa funcionem corretamente com o filtro effectiveModifiedDate. Agora você pode ligar para:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z
 &filter.loTypes=jobAid
```

Antes dessa alteração, a combinação de effectiveModifiedDate com loTypes=jobAid não retornou ajudas de tarefa de forma confiável. Ou seja:

1. Seus trabalhos TDA ou ETL podem **sincronizar incrementalmente ajudas de tarefa** para experiências não conectadas, da mesma forma que fazem para cursos e caminhos.
2. Qualquer implementação sem periféricos que compila um diretório público de ajuda de tarefa pode consultar alterações com base em effectiveModifiedDate e loType=jobAid.

**Observação**:

No estado não conectado:

* As ajudas de tarefa são principalmente **detectáveis**: os visitantes podem ver que elas existem, ler descrições e entender como elas oferecem suporte a tópicos ou cursos.
* O **consumo** real (baixar ou abrir o conteúdo de ajuda de tarefa) normalmente ainda requer logon, especialmente se as ajudas de tarefa forem consideradas parte de conteúdo licenciado ou interno.

### Alterações na breve descrição na pesquisa do LO (não conectado)

Na pilha não conectada, a pesquisa e a listagem de objetos de aprendizado (LOs) são acionadas pelo conector Acesso a dados de treinamento (TDA) e por um índice de Elasticsearch público. Historicamente, essa pilha usava um único campo de visão geral/descrição para cada LO. Os clientes que criam portais sem periféricos não conectados queriam mostrar a mesma descrição curta em blocos do OA que a interface do aluno conectada mostra, em vez de apenas a visão geral longa.

A alteração introduz suporte para o OA **breve descrição** em APIs de pesquisa e listagem não conectadas:

* Para **cursos**, a semântica da interface do usuário existente é:
* Cartões conectados mostram uma breve descrição (campo de 140 caracteres), se houver; caso contrário, eles retornarão à visão geral detalhada por muito tempo.
* Para **caminhos de aprendizado**, a interface de usuário conectada usa o campo Benefícios como a descrição curta, se definida, e retorna para a visão geral caso contrário.
* Para **certificações**, é usada uma Descrição curta, com uma visão geral de Certificação mais longa como fallback.
* Para **ajudas de tarefa**, o campo de descrição principal é usado.

### Outras alterações

#### Restrição de que duas contas não podem compartilhar o mesmo domínio personalizado

Nas arquiteturas não conectadas e conectadas do Adobe Learning Manager, um **domínio personalizado** (por exemplo, academy.example.com) é tratado como uma chave globalmente exclusiva que deve ser mapeada para exatamente uma conta do ALM, para que a plataforma aplique uma restrição rígida de que **nenhuma conta pode compartilhar o mesmo domínio personalizado**. Isso é necessário para segurança, roteamento e SEO: a camada de roteamento e a pilha não conectada usam o domínio para pesquisar a configuração correta da conta (incluindo sua conta não conectada JSON, menus do Experience Builder, identidade visual e pontos de extremidade TDA/pesquisa),

Permitir o mesmo domínio personalizado em duas contas tornaria impossível garantir que os dados da conta sejam retornados, poderia causar vazamento entre locatários e também corromperia artefatos gerados, como sitemap.xml e robots.txt, que são produzidos por conta, mas descobertos por mecanismos de pesquisa por host. Operacionalmente, isso significa que, ao atribuir ou mover um domínio personalizado, primeiro você deve garantir que ele não esteja anexado a nenhuma outra conta (ou cancelar o registro dele), e as ferramentas internas do Adobe rejeitarão as tentativas de vincular o mesmo domínio a várias contas.

#### Cache de navegador de recursos na experiência não conectada

Na experiência não conectada do Adobe Learning Manager, o cache de recursos do navegador é uma parte central da estratégia de desempenho e escala, porque as páginas públicas devem lidar com tráfego de marketing grande, às vezes pontiagudo, com baixa latência e carga mínima de origem. Ativos estáticos e semiestáticos, como o shell de HTML não conectado (por exemplo, index.html/guest.html), a configuração no nível de conta JSON (account.json ou config.json), o layout de página do Experience Builder JSON (menus, layouts de widget, configurações de cartão), CSS, JS, imagens e favicons são fornecidos de um CDN do Akamai (cpcontents.adobe.com / cpcontent.adobe.com) com cabeçalhos de cache que incentivam a reutilização no lado do CDN e no lado do navegador, para que, após o primeiro carregamento de página, o navegador possa renderizar páginas não conectadas subsequentes em grande parte de seu cache, revalidando apenas quando necessário via ETag ou Última modificação.

## Ajudas de tarefa em vários idiomas

### Introdução

As ajudas de tarefa multilíngues no Adobe Learning Manager (ALM) permitem que autores e administradores forneçam documentos complementares, guias ou recursos em vários idiomas em uma única entrada de ajuda de tarefa. Os alunos em diferentes regiões podem acessar materiais relevantes em seu idioma de preferência, o que melhora a compreensão, a conformidade e a experiência do usuário.

### Comportamento anterior

Anteriormente, as ajudas de tarefa no ALM aceitavam apenas um único arquivo de conteúdo por ajuda de tarefa, mesmo quando o nome e a descrição podiam ser localizados. Para fornecer o mesmo recurso em vários idiomas, os autores tiveram que criar ajudas de tarefa separadas para cada idioma. Isso levou à duplicação, confusão e aumento da sobrecarga administrativa. Não havia uma maneira unificada de gerenciar recursos multilíngues, o que dificultava garantir a consistência e controlar o uso.

### Casos de uso

* **Habilitação global da força de trabalho**: fornecer manuais de segurança, guias de processo ou documentos de referência em vários idiomas para uma força de trabalho diversificada.
* **Conformidade regulamentar**: garanta que todos os funcionários recebam a mesma documentação de conformidade em seu idioma nativo.
* **Integração consistente**: forneça listas de verificação de integração ou perguntas frequentes em idiomas locais para novas contratações em todo o mundo.
* **Duplicação reduzida**: gerenciar todas as versões de idioma de uma ajuda de tarefa em uma única entrada, o que simplifica as atualizações e os relatórios.

### Principais recursos

* **Suporte a vários idiomas**: anexe um arquivo ou URL exclusivo para cada idioma com suporte em uma única ajuda de tarefa.
* **Nome e descrição localizados**: insira o nome e a descrição da ajuda de tarefa em cada idioma.
* **Gerenciamento unificado**: edite, atualize e relate todas as versões de idioma em um só lugar.
* **Compatibilidade com versões anteriores**: as ajudas de tarefa de idioma único existentes são replicadas automaticamente em todos os idiomas adicionados até que novos arquivos sejam carregados.

### Criar uma ajuda de tarefa multilíngue

1. Vá para a função Autor e selecione **Ajudas de tarefa**.
2. Selecione **Criar Ajuda de Trabalho**.
3. Insira o nome e a descrição da ajuda de tarefa no idioma padrão.
4. Adicione o arquivo de conteúdo primário ou URL para o idioma padrão.
5. Salve a ajuda da tarefa.

### Adicionar idiomas adicionais

1. No editor de ajuda de tarefa, selecione **Adicionar Idioma**.
2. Selecione o(s) idioma(s) desejado(s) na lista.
3. Para cada idioma adicionado:
   * Insira o nome e a descrição localizados.
   * Faça upload do arquivo de conteúdo correspondente ou forneça um URL específico de idioma.
4. Repita o procedimento para todos os idiomas necessários.

### Editar e gerenciar idiomas

1. Para atualizar um arquivo ou uma descrição para um idioma específico, selecione a guia de idioma e faça as alterações necessárias.
2. Se um idioma for adicionado após a publicação da ajuda de tarefa, o arquivo original será atribuído automaticamente ao novo idioma até que um arquivo exclusivo seja carregado.
3. Remova ou substitua arquivos para qualquer idioma conforme necessário.

### Publish e experiência do aluno

1. Depois que todos os idiomas e arquivos forem adicionados, publique a ajuda de tarefa.
2. Os alunos veem a ajuda de tarefa em seu idioma de conteúdo selecionado, com o arquivo ou URL apropriado.
3. Se o idioma de um aluno não estiver disponível, o arquivo de idioma padrão será exibido.

### Relatórios

1. Baixe relatórios de ajuda de tarefa para exibir detalhes de todos os arquivos e idiomas associados a cada ajuda de tarefa.
2. Os relatórios incluem idioma, nome de arquivo e dados de uso para controle.

### Práticas recomendadas

* Forneça traduções precisas para nomes, descrições e arquivos de conteúdo.
* Revise e atualize arquivos regularmente para garantir a consistência entre os idiomas.
* Use convenções de nomenclatura claras para distinguir os arquivos em diferentes idiomas.
* Teste a experiência do aluno alternando os idiomas do conteúdo para verificar a entrega correta do arquivo.

### Solução de problemas

* **Arquivo ausente para um idioma**: o arquivo padrão é mostrado. Verifique se todos os idiomas têm o arquivo correto carregado.
* **Ajudas de trabalho herdadas**: adicione novos arquivos de idioma para substituir originais replicados automaticamente.
* **Idioma incorreto mostrado**: verifique as configurações de idioma do conteúdo do aluno e a configuração de idioma da ajuda de tarefa.

As ajudas de tarefa multilíngues permitem fornecer recursos de suporte a um público global em uma única entrada, reduzir a duplicação e garantir que cada aluno receba as informações certas em seu idioma preferido. Este recurso melhora a acessibilidade, a conformidade e a eficiência administrativa no Adobe Learning Manager.

## Obtenha respostas com o Assistente de IA para alunos

O Assistente de IA para alunos é um assistente conversacional orientado por IA no Adobe Learning Manager projetado para orientá-lo com as informações de que você precisa com mais rapidez. Ao fazer perguntas em linguagem natural, você pode obter explicações contextuais, revelar cursos relevantes e recuperar informações do conteúdo de aprendizado, sem navegar manualmente pelos catálogos.

### Capacidades

* **Resposta inteligente de perguntas:** lida com conversas de uma vez e de várias vezes, permitindo que você faça perguntas naturalmente. As respostas são derivadas de cursos, programações de aprendizado, certificações e ajudas de tarefa.
* **Respostas baseadas em conteúdo com citações:** extrai informações diretamente de materiais de aprendizado e inclui citações que apontam de volta para o curso, módulo ou recurso original.
* **Compatibilidade ampla de conteúdo:** oferece suporte a uma ampla variedade de formatos, incluindo documentos, apresentações, vídeos, arquivos de áudio, conteúdo de HTML e módulos SCORM (Sharable Content Object Reference Model).
* **Experiência perfeita do usuário:** disponível como um painel lateral nas páginas do aluno, mantendo o histórico de bate-papo baseado em sessão para continuidade.
* **Controles de administrador robustos:** os administradores podem habilitar ou desabilitar o assistente, limitar o acesso por grupos de usuários e escolher quais catálogos internos são usados como origem para respostas geradas por IA.

### Benefícios

* **Acesso mais rápido ao conhecimento:** você recebe respostas instantâneas às suas perguntas, eliminando a necessidade de navegar por vários cursos ou documentos.
* **Envolvimento mais alto:** as interações de conversa tornam a experiência de aprendizado mais natural, intuitiva e acessível.
* **Melhor entendimento:** você pode fazer perguntas de acompanhamento para esclarecer conceitos e explorar tópicos mais detalhadamente.
* **Suporte de aprendizado escalável:** respostas automatizadas e baseadas em IA minimizam a dependência de especialistas no assunto e equipes de suporte.

Saiba mais sobre o [Assistente de IA para alunos](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

## Suporte a faixas de texto de vídeo (VTT) multilíngues

O suporte a Faixas de texto de vídeo (VTT) multilíngues no Adobe Learning Manager permite que os autores forneçam legendas para conteúdo de áudio e vídeo em vários idiomas. Esse recurso simplifica a localização, tornando o treinamento acessível a um público global e garantindo a conformidade com os padrões de acessibilidade. Os autores podem gerar, traduzir, revisar e editar automaticamente arquivos VTT diretamente na plataforma.

### Casos de uso

* **Treinamento global:** forneça conteúdo em vídeo com legendas em vários idiomas para alcançar os alunos internacionais.
* **Conformidade de acessibilidade:** forneça legendas para usuários portadores de deficiência auditiva em seu idioma preferido.
* **Localização mais rápida:** reduza o esforço manual e acelere a implantação de conteúdo com a geração e tradução automáticas de arquivos VTT.
* **Experiência consistente:** verifique se todos os alunos recebem as mesmas informações, independentemente do idioma.

### Principais recursos

* **Tradução em vários idiomas:** traduza legendas para qualquer um dos 39 idiomas diferentes do inglês com suporte.
* **Revisão e edição no aplicativo:** revise, edite e baixe arquivos VTT antes de publicar.
* **Notificações:** receba notificações no aplicativo quando a geração e tradução de VTT estiverem concluídas.
* **Publicação sem problemas:** legendas finalizadas do Publish para que os alunos acessem em seu idioma escolhido.

### Fazer upload de conteúdo e gerar VTT

1. Vá para a Biblioteca de Conteúdo e selecione **Adicionar > Conteúdo**.
2. Carregue o arquivo MP3 ou MP4.
3. Na caixa de diálogo de carregamento, selecione a opção para **Gerar Traduções**.
4. Selecione o idioma do conteúdo original (o padrão é o idioma do arquivo).
5. Selecione idiomas de destino adicionais para tradução (até 39 compatíveis).
6. Selecione **Salvar**. O sistema começa a gerar e traduzir arquivos VTT.

### Monitorar progresso

1. Após salvar, a nova entrada de conteúdo aparece na Biblioteca de conteúdo.
2. Um indicador de progresso mostra o status da geração e tradução de VTT.
3. Você receberá uma notificação no aplicativo quando o processo for concluído.

### Revisar e editar arquivos VTT

1. Na Biblioteca de Conteúdo, abra o conteúdo no modo **Editar**.
2. Para cada idioma, selecione o link **Revisão** ao lado do arquivo VTT.
3. Uma janela pop-up exibe as legendas para esse idioma.
4. Edite as legendas diretamente no pop-up ou baixe o arquivo VTT para edição offline.
5. Após fazer alterações, faça upload ou cole as legendas revisadas de volta no pop-up.
6. Salve suas edições.

### Legendas do Publish

1. Quando estiver satisfeito com todas as legendas de idioma, publique o conteúdo.
2. Os alunos veem as opções de legenda em todos os idiomas publicados ao visualizar o vídeo.

### Informações adicionais

* **Idiomas com suporte:** todos os 39 idiomas diferentes do inglês com suporte do Adobe Learning Manager.
* **Notificações:** os autores são notificados quando a geração e a tradução do VTT são concluídas.
* **Flexibilidade de edição:** as legendas podem ser editadas no aplicativo ou offline e recarregadas.
* **Escalabilidade:** criada para necessidades de acessibilidade e localização em escala empresarial.
* **Não é necessário o carregamento manual de VTT:** o sistema pode gerar arquivos VTT do zero usando o vídeo/áudio carregado.

### Práticas recomendadas

* Sempre verifique a precisão das legendas geradas automaticamente antes de publicá-las.
* Forneça traduções para todos os principais grupos de alunos para maximizar a acessibilidade.
* Use o sistema de notificação para se manter atualizado sobre o status do processamento.
* Atualizar legendas regularmente se o conteúdo de vídeo mudar.

### Solução de problemas

* Se a geração de VTT falhar, verifique se o arquivo está em um formato compatível (MP3/MP4).
* Para idiomas ausentes, verifique se eles são compatíveis e selecionados durante o upload.
* Se as legendas estiverem fora de sincronia, use o editor do aplicativo para ajustar o tempo.

O suporte a VTT multilíngue permite que você ofereça experiências de aprendizado de vídeo acessíveis e localizadas de maneira eficiente. Ao usar geração automática, tradução e edição no aplicativo, você pode garantir que seu conteúdo alcance e ofereça suporte a todos os alunos, independentemente do idioma.

## Criar certificados personalizados

Os certificados personalizados no Adobe Learning Manager (ALM) permitem que administradores e autores projetem, gerenciem e emitam certificados personalizados para alunos. O recurso inclui um editor de arrastar e soltar, campos dinâmicos, suporte a vários idiomas e planos de fundo gerados por IA, para que as organizações possam criar certificados de marca sem conhecimento técnico.

### Comportamento anterior

Anteriormente, a criação de certificados no ALM era limitada pela rigidez do modelo, falta de personalização e barreiras técnicas (como a edição de HTML). Os clientes solicitavam maneiras mais simples de criar certificados, adicionar campos dinâmicos (como nome do aluno ou professor) e oferecer suporte a vários idiomas, tudo isso mantendo a consistência da marca e o apelo visual.

### Casos de uso

* **Reconhecimento de marca**: emita certificados com logotipos, cores e fontes corporativos para fins de conformidade, treinamento ou realização.
* **Personalização dinâmica**: preencha automaticamente nomes de alunos, nomes de professores e outros campos ativos.
* **Entrega multilíngue**: forneça certificados em vários idiomas para alunos globais.
* **Design flexível**: crie certificados de paisagem ou retrato, use planos de fundo gerados por IA e visualize antes de publicar.

### Acessar certificados personalizados

1. Vá para a seção **Conquistas** na página inicial do administrador (anteriormente chamadas de **Medalhas**).
2. Selecione **Certificados** para exibir, criar ou gerenciar modelos de certificado.

### Criar um certificado

1. Selecione **Criar Certificado**.
2. Selecione a orientação retrato ou paisagem.
3. Selecione um modelo existente ou comece com uma tela em branco.
4. Insira um nome de certificado e o idioma padrão.
5. Use o editor de arrastar e soltar para adicionar:
   * Campos de texto (com opções de fonte, cor e posicionamento)
   * Imagens (logotipos, ícones etc.)
   * Campos dinâmicos (nome do aluno, nome do professor etc.)
   * Fundos de certificado (cor sólida, imagem carregada ou imagem gerada por IA)
6. Para planos de fundo gerados por IA: insira um prompt (por exemplo, “alunos em uma sala de aula”) para gerar planos de fundo usando IA.

### Adicionar campos dinâmicos

Os campos dinâmicos nos certificados personalizados do Adobe Learning Manager são espaços reservados que são preenchidos automaticamente com informações relevantes, como nome do aluno, nome do professor ou outros dados específicos da conta — quando o certificado é gerado, permitindo certificados personalizados e sensíveis ao contexto sem edição manual.

1. Insira variáveis dinâmicas, como nome do aluno, nome do professor ou outros campos ativos.
2. Os campos são preenchidos automaticamente quando o certificado é emitido.

### Suporte multilíngue

1. Adicione novos idiomas (por exemplo, francês, alemão) ao certificado.
2. Insira o texto traduzido para cada idioma.
3. Gerencie traduções e visualize certificados em cada idioma.

### Visualizar e publicar

1. Use o recurso de visualização para ver como o certificado é exibido aos alunos.
2. Baixe ou imprima a visualização para revisão.
3. Salve como rascunho para continuar editando mais tarde ou publique quando estiver pronto.

### Aplicar certificados

1. Os administradores podem definir certificados padrão para a conta.
2. Os autores podem anexar certificados a instâncias específicas de objetos de aprendizado (cursos, caminhos etc.).
3. Selecione certificados diferentes no nível da instância, conforme necessário.

### Gerenciar certificados

1. Exibir certificados publicados e de rascunho na biblioteca.
2. Edite, atualize ou exclua modelos conforme necessário.
3. Os certificados podem ser reutilizados em várias instâncias.

Os certificados personalizados no ALM fornecem uma maneira flexível de criar e emitir certificados personalizados, com marca e multilíngues. O recurso simplifica o gerenciamento de certificados, melhora o reconhecimento do aluno e suporta a conformidade global e as necessidades de marca.

## Ajudas de tarefa em vários idiomas

As ajudas de tarefa multilíngues no Adobe Learning Manager (ALM) permitem que autores e administradores forneçam documentos complementares, guias ou recursos em vários idiomas em uma única entrada de ajuda de tarefa. Os alunos de diferentes regiões podem acessar materiais relevantes em seu idioma de preferência, o que melhora a acessibilidade, a conformidade e a experiência do usuário.

### Comportamento anterior

Anteriormente, o ALM permitia apenas um arquivo de conteúdo por ajuda de tarefa, mesmo que o nome e a descrição pudessem ser localizados. Para fornecer o mesmo recurso em vários idiomas, os autores tiveram que criar ajudas de tarefa separadas para cada idioma. Isso levou à duplicação, confusão e aumento do esforço administrativo. Não havia uma maneira unificada de gerenciar recursos multilíngues, o que dificultava garantir a consistência e controlar o uso.

### Casos de uso

* **Habilitação global da força de trabalho**: fornecer manuais de segurança, guias de processo ou documentos de referência em vários idiomas para uma força de trabalho diversificada.
* **Conformidade regulamentar**: garanta que todos os funcionários recebam a mesma documentação de conformidade em seu idioma nativo.
* **Integração consistente**: forneça listas de verificação de integração ou perguntas frequentes em idiomas locais para novas contratações em todo o mundo.
* **Duplicação reduzida**: gerenciar todas as versões de idioma de uma ajuda de tarefa em uma única entrada, o que simplifica as atualizações e os relatórios.

### Criar uma ajuda de tarefa multilíngue

1. Vá para a função Autor e selecione **Ajudas de tarefa**.
2. Selecione **Criar Ajuda de Trabalho**.
3. Insira o nome e a descrição da ajuda de tarefa no idioma padrão.
4. Faça upload do arquivo de conteúdo principal ou forneça um URL para o idioma padrão.
5. Salve a ajuda da tarefa.

### Adicionar idiomas adicionais

1. No editor de ajuda de tarefa, selecione **Adicionar Idioma**.
2. Selecione o(s) idioma(s) desejado(s) na lista.
3. Para cada idioma adicionado:
   * Insira o nome e a descrição localizados.
   * Faça upload do arquivo de conteúdo correspondente ou forneça um URL específico de idioma.
4. Repita o procedimento para todos os idiomas necessários.

### Editar e gerenciar idiomas

1. Para atualizar um arquivo ou uma descrição para um idioma específico, selecione a guia de idioma e faça as alterações necessárias.
2. Se um idioma for adicionado após a publicação da ajuda de tarefa, o arquivo original será atribuído automaticamente ao novo idioma até que um arquivo exclusivo seja carregado.
3. Remova ou substitua arquivos para qualquer idioma conforme necessário.

### Publish e experiência do aluno

1. Depois que todos os idiomas e arquivos forem adicionados, publique a ajuda de tarefa.
2. Os alunos veem a ajuda de tarefa em seu idioma de conteúdo selecionado, com o arquivo ou URL apropriado.
3. Se o idioma de um aluno não estiver disponível, o arquivo de idioma padrão será exibido.

### Relatórios

1. Baixe relatórios de ajuda de tarefa para exibir detalhes de todos os arquivos e idiomas associados a cada ajuda de tarefa.
2. Os relatórios incluem idioma, nome de arquivo e dados de uso para controle.

As ajudas de tarefa multilíngues no ALM permitem fornecer recursos de suporte a um público global em uma única entrada, reduzir a duplicação e garantir que cada aluno receba as informações corretas em seu idioma preferido. Este recurso melhora a acessibilidade, a conformidade e a eficiência administrativa no Adobe Learning Manager.

## Melhorias de reprodução para cursos gerados por Captivate

A atualização melhora significativamente a experiência de reprodução de conteúdo do Adobe Captivate no ALM, introduzindo uma interface unificada e simplificada.

O reprodutor do ALM agora exibe um único sumário consolidado, ocultando o sumário do Captivate, e fornece indicadores claros de conclusão no nível do slide, incluindo marcas de escala verdes para controle visual do progresso.

O sistema simplifica a navegação mesclando os controles do módulo e do curso em uma barra intuitiva, reduzindo a confusão do aluno.

Os controles de progresso sensíveis a contexto melhoram a usabilidade exibindo barras de progresso de vídeo somente em slides de vídeo e controles de navegação de slides somente em slides que não sejam de vídeo.

Além disso, o sistema agora vincula notas aos números dos slides em vez de carimbos de data e hora, garantindo exportações de PDF confiáveis e resolvendo inconsistências de formatos anteriores.

## Aprimoramentos na lista de verificação

### Suporte a vários idiomas para lista de verificação

Este recurso permite criar e gerenciar módulos de lista de verificação em vários idiomas. Cada pergunta, instrução e critério de avaliação da lista de verificação pode ser traduzida para que os revisores e alunos interajam com a lista de verificação em seu idioma preferido. O sistema exibe a lista de verificação no idioma de conteúdo selecionado do usuário, o que melhora a acessibilidade e a conformidade para equipes globais.

1. Adicione ou edite um módulo de lista de verificação em seu curso.
2. Selecione todos os idiomas que você deseja suportar nas opções de idioma.
3. Para cada idioma, insira traduções para cada pergunta da lista de verificação, instrução e critério de avaliação.
4. Salve suas alterações. A lista de verificação é exibida no idioma do conteúdo selecionado do revisor ou do aluno.
5. Se você adicionar um novo idioma posteriormente, forneça traduções para todas as perguntas e critérios antes de publicar.
6. Ao baixar relatórios de listas de verificação, selecione seu idioma preferido para exibir o relatório nesse idioma.

### Ponderação de pergunta da lista de verificação para avaliações do professor

Esse recurso permite atribuir pontuações máximas diferentes (ponderação) a cada pergunta da lista de verificação. Você pode refletir a importância ou dificuldade variável de cada pergunta, o que permite avaliações mais precisas e significativas. O sistema calcula a pontuação total com base na sua entrada e determina se o aluno é aprovado ou reprovado de acordo com os critérios definidos.

1. Ao adicionar um módulo de lista de verificação, selecione **Pontuação personalizada**.
2. Para cada pergunta da lista de verificação, defina uma pontuação máxima exclusiva que reflita sua importância.
3. Defina a pontuação geral de aprovação para a lista de verificação.
4. Salve e publique a lista de verificação.
5. Como professor ou revisor, avalie cada aluno atribuindo uma pontuação para cada pergunta (até o máximo definido).
6. O sistema calcula a pontuação total e determina o status de aprovação/reprovação.
7. Baixe os relatórios de lista de verificação para visualizar as pontuações alcançadas e máximas para cada pergunta e a pontuação total.

### Lista de verificação com recurso de comentários para revisor

Esse recurso permite que os revisores adicionem comentários ou feedback durante a avaliação da lista de verificação. Você pode fornecer feedback personalizado e acionável para cada aluno. Você também pode optar por exibir seu nome com seus comentários para transparência. Todos os comentários são salvos na transcrição do aluno e incluídos nos relatórios da lista de verificação.

1. Ao configurar a lista de verificação, habilite **Comentários do revisor**.
2. Opcionalmente, habilite **Mostrar o nome do revisor ao aluno** se quiser que o seu nome apareça com os comentários.
3. Durante a avaliação, insira comentários ou feedback para o aluno no campo de comentários fornecidos.
4. Selecione se os comentários devem estar visíveis para o aluno.
5. Envie sua avaliação. Se ativado, o aluno verá seus comentários e seu nome junto com os resultados.
6. Todos os comentários são salvos na transcrição do aluno e incluídos nos relatórios de lista de verificação para referência futura.

## Aprimoramentos de pesquisa avançada

Os resultados da pesquisa em Pesquisa avançada agora são mais precisos e relevantes. As correspondências de palavras-chave exatas são classificadas mais alto na pesquisa de conteúdo e nos metadados, facilitando para os alunos encontrar exatamente o que estão procurando.

Os alunos agora também podem ver os objetos de aprendizado inscritos nos resultados de pesquisa, mesmo que não façam parte de um catálogo acessível, garantindo que nenhum conteúdo relevante seja perdido. Além disso, a classificação da ajuda de tarefa foi aprimorada tanto na pesquisa avançada quanto na pesquisa de conteúdo, trazendo à tona os recursos mais relevantes mais rapidamente.


## Equivalentes e suplentes

### Visão geral

Em muitas organizações, os alunos encontram situações de treinamento em que diferentes cursos podem atender legitimamente ao mesmo requisito?por exemplo, quando um novo curso substitui um mais antigo, quando um curso mais abrangente pode substituir um mais curto ou quando um curso substituto especial precisa ser oferecido.

O recurso Cursos alternativos ou Caminho de aprendizado fornece ao ALM uma maneira formal de dizer:

“Se o aluno concluiu este treinamento, trate-o como tendo atendido a esse requisito de treinamento relacionado.”

O recurso funciona em cursos e caminhos de aprendizado, garante que os requisitos de downstream, como pré-requisitos e regras de conformidade, sejam atendidos e faz isso sem forçar os alunos a passar por conteúdo redundante. Ele também mantém a precisão dos relatórios ao gravar o que foi concluído diretamente em comparação com o que foi satisfeito por meio de uma alternativa.

No núcleo, o recurso introduz o conceito de uma conclusão alternativa: um estado de conclusão especial criado automaticamente quando um aluno conclui um treinamento de origem configurado que conta para outro treinamento de destino.

### Equivalência vs. alternativas

Alguns relacionamentos de treinamento são bidirecionais, o que significa que cada curso pode satisfazer os requisitos do outro. Este é efetivamente um cenário em que dois treinamentos são tratados como substituíveis entre si. Em contraste, as relações unidirecionais permitem que um treinamento satisfaça a exigência de outro, mas não vice-versa. O ALM modela ambos os cenários usando o mesmo mecanismo subjacente de conclusão alternativa.

* **Relação bidirecional:** a conclusão de um dos treinamentos satisfaz o requisito do outro.
* **Relacionamento unidirecional:** concluir o Treinamento A satisfaz o Treinamento B, mas concluir B não satisfaz A. Isso é comum quando uma versão mais recente ou mais abrangente deve contar para um requisito mais antigo, mas não o contrário.

As alternativas são usadas com mais frequência em cenários **unidirecionais**?por exemplo, quando um curso de superconjunto mais abrangente abrange tudo em um curso de subconjunto mais simples. Completar o superconjunto deve satisfazer o requisito para o subconjunto, mas não necessariamente o contrário.

* Um curso mais recente e expandido que deve contar para um requisito mais antigo.
* Um curso criado para um público específico (por exemplo, uma variante regional ou adaptada à acessibilidade) que ainda atende ao mesmo requisito do curso principal.
* Uma nova versão aprimorada de um curso que a organização deseja contar para um requisito mais antigo, mas a versão mais antiga não deve contar para o novo requisito.

Em Alternativas, a relação normalmente é **one*way**. Se o Curso A for uma alternativa para o Curso B, concluir A pode satisfazer a exigência de B, mas concluir B não necessariamente satisfaz A.

A equivalência e a alternativa compartilham o mesmo mecanismo subjacente no ALM: quando um treinamento de origem configurado é concluído, o ALM produz automaticamente uma conclusão alternativa para um ou mais treinamentos de destino.

### Que problemas isso resolve?

Sem alternativas e equivalência, os administradores e alunos enfrentam vários problemas recorrentes:

* Os alunos são frequentemente solicitados a repetir cursos que abrangem conteúdo que já concluíram em uma versão ou formato diferente.
* A atualização de programas de conformidade é mais simples porque os administradores podem substituir ou reestruturar treinamentos sem forçar os alunos que concluíram versões mais antigas a retomar conteúdo equivalente ou substituído.
* A lógica de pré-requisito é rígida. Se um caminho exigir um curso específico como pré-requisito, não há uma maneira clara de reconhecer que outro treinamento é bom o suficiente.
* Relatórios e auditorias são mais difíceis. Não há nenhum sinal formal que mostre que um requisito foi atendido através de uma conclusão alternativa e nenhuma maneira direta de rastrear a origem do crédito.

O recurso Alternativas e Equivalência resolve esses problemas:

* Impedir esforços duplicados para alunos quando as alternativas são válidas.
* Permitir que os administradores modifiquem as estruturas de treinamento (por exemplo, troquem um curso dentro de um caminho) sem interromper as conclusões dos alunos que fizeram a versão anterior.
* Permitir que os pré-requisitos e as verificações de conformidade respeitem tanto as conclusões diretas quanto as conclusões alternativas ou equivalentes.
* Registrar claramente, em transcrições e relatórios, se um treinamento foi concluído diretamente ou satisfeito por meio de um relacionamento alternativo, junto com o qual o treinamento serviu como fonte.

### Como o recurso funciona conceitualmente

O recurso é construído em três ideias principais: **relações**, **conclusão alternativa** e **comportamento downstream**.

#### Relacionamentos entre treinamentos

Os administradores definem as relações entre cursos e caminhos de aprendizado. Para cada relação, eles escolhem uma **origem** e um ou mais **destinos**. Um único curso pode ter até 30 metas, dependendo de quantos treinamentos anteriores ou relacionados ele deve atender.

Para a Equivalência, os administradores podem tornar a relação **bidirecional** se quiserem que os dois treinamentos satisfaçam uns aos outros. Para alternativas, os administradores normalmente mantêm a direção em uma*maneira para refletir que apenas algumas substituições são permitidas.

Esses relacionamentos são armazenados no nível do treinamento, não no nível do aluno. Uma vez configurados e ativados, eles se aplicam a todas as conclusões atuais e futuras do treinamento de origem, sujeito às configurações no nível de conta, como se a conclusão retroativa estiver ativada.

### Conclusão alternativa

Quando um aluno conclui um treinamento de origem, o ALM examina todas as relações alternativas ou equivalentes configuradas e, para cada treinamento de destino relevante, cria um **registro de conclusão alternativa**. Esse registro é diferente de uma conclusão normal:

* Ele marca o treinamento de destino do aluno, mas acompanha que ele foi concluído via alternativa ou equivalência em vez de diretamente.
* Ele registra qual treinamento de origem foi usado para satisfazer o alvo.
* Ele é armazenado em uma estrutura dedicada para que a emissão de relatórios possa distinguir entre conclusões diretas e alternativas.

Os alunos verão uma conclusão alternativa mesmo se não estiverem inscritos. O relatório Transcrição do aluno (LT) inclui apenas registros de treinamentos nos quais o aluno se inscreveu.

### Experiência do aplicativo do aluno para conclusões alternativas e equivalentes

Conclusões alternativas e equivalentes são apresentadas de forma distinta no aplicativo do aluno para que os alunos possam entender claramente como um requisito de treinamento foi atendido, mantendo a consistência com transcrições e relatórios.

#### Comportamento da placa LO

#### Status de conclusão alternativo

Quando um aluno conclui um treinamento por meio de uma relação alternativa ou equivalente, o cartão do Objeto de Aprendizado (LO) exibe um status distinto, como **Concluído via Alternativo**.\
Essa distinção visual ajuda os alunos a diferenciar entre conclusões diretas e conclusões concedidas por meio de relacionamentos configurados.

#### Indicador do método de conclusão

O cartão do OA inclui um indicador do método de conclusão (por exemplo, um rótulo ou ícone) para mostrar que a conclusão foi obtida por meio de um **Alternativo**.\
Se uma conclusão alternativa for revogada posteriormente devido a alterações como inconclusão retroativa ou exclusão do treinamento de origem, o cartão do OA será atualizado para refletir **Alternativo (revogado)**.

#### Transparência e detalhes de auditoria

Os alunos podem abrir o cartão do OA para exibir detalhes adicionais, incluindo:

* O curso ou a programação de aprendizado de origem que concedeu a conclusão alternativa
* A data de conclusão associada ao treinamento de origem

Isso garante a transparência e dá suporte a auditorias e revisões de conformidade.

#### Filtragem e exibições

#### Filtro de método de conclusão

O aplicativo do aluno fornece um filtro que permite aos alunos distinguir entre:

* Conclusões **diretas**
* Conclusões **alternativas**
* **Todas** conclusões

Isso permite que os alunos entendam rapidamente como seus requisitos de aprendizado foram atendidos.

#### Exibições de transcrição e progresso

O filtro do método de conclusão está disponível nas exibições voltadas para o aluno*, como:

* Transcrições de aprendizado
* Seções de acompanhamento de progresso e conclusão

Essas exibições indicam claramente quais treinamentos foram concluídos diretamente e quais foram satisfeitos por meio de alternativas ou equivalência.

#### Alinhamento de relatórios

A lógica de filtragem no aplicativo do aluno se alinha à coluna **Método de conclusão** usada nos relatórios.\
Isso garante a consistência entre o que os alunos veem na interface e o que os administradores veem nas exportações e nos relatórios de conformidade.

#### Encerrar *a* encerrar fluxo

#### Para alunos

1. Navegue até **Meu aprendizado** ou **Cursos concluídos** no aplicativo do aluno.
2. Revise os cartões do OA para identificar treinamentos marcados como **Concluídos via Alternativo**.
3. Abra um cartão do OA para ver detalhes sobre o treinamento de origem e a data de conclusão.
4. Use o menu de filtro nas exibições de transcrição ou lista de cursos para selecionar **Direto**, **Alternativo** ou **Todos**.
5. Revise a lista atualizada com base no método de conclusão selecionado.

#### Para administradores e autores

1. Configure relacionamentos equivalentes ou alternativos entre cursos ou programações de aprendizado na interface do administrador.
2. Verifique se as conclusões alternativas são corretamente refletidas nas placas de OA e nos filtros voltados para o aluno.
3. Use as exibições e os relatórios do aluno para confirmar a consistência entre a interface do usuário e os dados exportados.
4. Se um treinamento de origem for desativado ou excluído, valide se os cartões de OA afetados foram atualizados de acordo (por exemplo, mostrando **Alternativo (revogado)** quando aplicável).

## Conclusão retroativa e comportamento incompleto

O ALM oferece suporte à conclusão retroativa e à inconclusão retroativa para garantir que os relacionamentos alternativos e equivalentes permaneçam precisos ao longo do tempo, mesmo quando os relacionamentos são criados, modificados ou removidos depois que os alunos já concluíram o treinamento.

### Conclusão retroativa

#### Definição

Quando a conclusão retroativa está ativada, os alunos que concluíram um curso de origem no passado recebem automaticamente uma conclusão alternativa para o curso de destino se um relacionamento equivalente ou alternativo for criado posteriormente.\
Isso garante que o aprendizado histórico seja respeitado sem exigir que os alunos façam o treinamento novamente.

#### Como funciona

1. Um administrador ativa a conclusão retroativa no nível da conta.
2. O administrador define uma relação equivalente ou alternativa entre um treinamento de origem e de destino.
3. O sistema verifica os registros históricos de conclusão do treinamento de origem.
4. Os alunos qualificados recebem a conclusão alternativa para o treinamento de destino.
5. Esses registros aparecem como **Concluídos via Alternativo** em transcrições e relatórios do aluno.

### Inconclusão retroativa

#### Definição

Quando a inconclusão retroativa estiver ativada, as conclusões alternativas serão revogadas se o relacionamento equivalente ou alternativo subjacente for removido ou se o treinamento de origem for excluído.\
Isso garante que o sistema reflita os relacionamentos de treinamento atuais e válidos.

#### Como funciona

1. Um administrador ativa a inconclusão retroativa no nível da conta.
2. O administrador remove uma relação alternativa ou equivalente ou exclui o treinamento de origem.
3. O sistema identifica os alunos que receberam a conclusão alternativa por meio do relacionamento afetado.
4. Os registros de conclusão alternativos correspondentes são revogados.
5. Os registros revogados são marcados como **Alternativo (revogado)** em transcrições e relatórios para visibilidade de auditoria.

### Impacto nos pré-requisitos

As conclusões alternativas—incluindo aquelas concedidas retroativamente—são tratadas como conclusões válidas ao avaliar pré-requisitos.\
Se um aluno tiver **Concluído via Alternativo**, ele poderá continuar com os cursos que exigem o treinamento de destino.

Se uma conclusão alternativa for revogada posteriormente por meio de inconclusão retroativa, o aluno pode perder a qualificação para cursos que dependiam desse pré-requisito.

### Impacto nos caminhos de aprendizado e certificações

Conclusões alternativas contribuem para o progresso e a conclusão de caminhos de aprendizado e certificações.\
Os alunos podem avançar ou concluir esses programas quando os treinamentos necessários forem atendidos por meio de relacionamentos alternativos ou equivalentes.

Se uma conclusão alternativa for revogada, as programações de aprendizado ou certificações afetadas podem perder o progresso ou o status de conclusão até que o requisito seja atendido por meio de uma conclusão válida.

### Finalizar *a* finalizar fluxo de trabalho

#### Habilitando conclusão retroativa ou inconclusão

1. Os administradores navegam até as configurações da conta e ativam a conclusão retroativa e/ou a conclusão retroativa.
2. Os administradores criam, modificam ou removem relacionamentos equivalentes ou alternativos entre treinamentos.

#### Ações do sistema

* **Para conclusão retroativa:**\
  O sistema concede conclusões alternativas com base nas conclusões de origem histórica.
* **Para inconclusão retroativa:**\
  O sistema revoga conclusões alternativas quando os relacionamentos são removidos ou os treinamentos de origem são excluídos.

#### Experiência do aluno

Os alunos veem os status de conclusão atualizados em cartões LO e em transcrições, como:

* **Concluído via Alternativo**
* **Alternativa (Revogada)**

Verificações de pré-requisitos, progresso do caminho de aprendizado e atualização do status da certificação são atualizados dinamicamente com base no estado de conclusão atual.

#### Relatórios e auditoria

Todas as alterações retroativas são refletidas no relatório Transcrição de aprendizado (LT).\
Os relatórios distinguem claramente entre conclusões diretas, conclusões alternativas e conclusões alternativas revogadas para dar suporte à conformidade, dar suporte a investigações e auditorias.

### Conclusão retroativa e comportamento incompleto

O ALM oferece suporte à conclusão retroativa e à inconclusão retroativa para garantir que os relacionamentos alternativos e equivalentes permaneçam precisos ao longo do tempo, mesmo quando os relacionamentos são criados, modificados ou removidos depois que os alunos já concluíram o treinamento.

#### Conclusão retroativa

#### Definição

Quando a conclusão retroativa está ativada, os alunos que concluíram um curso de origem no passado recebem automaticamente uma conclusão alternativa para o curso de destino se um relacionamento equivalente ou alternativo for criado posteriormente.\
Isso garante que o aprendizado histórico seja respeitado sem exigir que os alunos façam o treinamento novamente.

#### Como funciona

1. Um administrador ativa a conclusão retroativa no nível da conta.
2. O administrador define uma relação equivalente ou alternativa entre um treinamento de origem e de destino.
3. O sistema verifica os registros históricos de conclusão do treinamento de origem.
4. Os alunos qualificados recebem a conclusão alternativa para o treinamento de destino.
5. Esses registros aparecem como **Concluídos via Alternativo** em transcrições e relatórios do aluno.

#### Inconclusão retroativa

#### Definição

Quando a inconclusão retroativa estiver ativada, as conclusões alternativas serão revogadas se o relacionamento equivalente ou alternativo subjacente for removido ou se o treinamento de origem for excluído.\
Isso garante que o sistema reflita os relacionamentos de treinamento atuais e válidos.

#### Como funciona

1. Um administrador ativa a inconclusão retroativa no nível da conta.
2. O administrador remove uma relação alternativa ou equivalente ou exclui o treinamento de origem.
3. O sistema identifica os alunos que receberam a conclusão alternativa por meio do relacionamento afetado.
4. Os registros de conclusão alternativos correspondentes são revogados.
5. Os registros revogados são marcados como **Alternativo (revogado)** em transcrições e relatórios para visibilidade de auditoria.

#### Impacto nos pré-requisitos

As conclusões alternativas—incluindo aquelas concedidas retroativamente—são tratadas como conclusões válidas ao avaliar pré-requisitos.\
Se um aluno tiver **Concluído via Alternativo**, ele poderá continuar com os cursos que exigem o treinamento de destino.

Se uma conclusão alternativa for revogada posteriormente por meio de inconclusão retroativa, o aluno pode perder a qualificação para cursos que dependiam desse pré-requisito.

#### Impacto nos caminhos de aprendizado e certificações

Conclusões alternativas contribuem para o progresso e a conclusão de caminhos de aprendizado e certificações.\
Os alunos podem avançar ou concluir esses programas quando os treinamentos necessários forem atendidos por meio de relacionamentos alternativos ou equivalentes.

Se uma conclusão alternativa for revogada, as programações de aprendizado ou certificações afetadas podem perder o progresso ou o status de conclusão até que o requisito seja atendido por meio de uma conclusão válida.

#### Finalizar *a* finalizar fluxo de trabalho

#### Habilitando conclusão retroativa ou inconclusão

1. Os administradores navegam até as configurações da conta e ativam a conclusão retroativa e/ou a conclusão retroativa.
2. Os administradores criam, modificam ou removem relacionamentos equivalentes ou alternativos entre treinamentos.

#### Ações do sistema

* **Para conclusão retroativa:**\
  O sistema concede conclusões alternativas com base nas conclusões de origem histórica.
* **Para inconclusão retroativa:**\
  O sistema revoga conclusões alternativas quando os relacionamentos são removidos ou os treinamentos de origem são excluídos.

#### Experiência do aluno

Os alunos veem os status de conclusão atualizados em cartões LO e em transcrições, como:

* **Concluído via Alternativo**
* **Alternativa (Revogada)**

Verificações de pré-requisitos, progresso do caminho de aprendizado e atualização do status da certificação são atualizados dinamicamente com base no estado de conclusão atual.

#### Relatórios e auditoria

Todas as alterações retroativas são refletidas no relatório Transcrição de aprendizado (LT).\
Os relatórios distinguem claramente entre conclusões diretas, conclusões alternativas e conclusões alternativas revogadas para dar suporte à conformidade, dar suporte a investigações e auditorias.

### Webhooks para equivalentes e alternativas

O ALM fornece eventos de webhook dedicados para conclusões equivalentes e alternativas a fim de oferecer suporte à automação, integrações e sincronização com sistemas externos.

Esses eventos permitem que os consumidores externos façam uma distinção confiável entre términos diretos e términos concedidos por meio de relacionamentos alternativos ou equivalentes.

#### Visão geral

Quando um aluno conclui um curso por meio de uma relação alternativa ou equivalente, o ALM aciona um evento de webhook separado do webhook de conclusão de curso padrão.\
Isso garante que as integrações possam responder de forma diferente a conclusões alternativas, quando necessário.

Os eventos do webhook também são acionados quando ocorre conclusão retroativa ou inconclusão retroativa, abrangendo atualizações históricas, bem como alterações de relacionamento.

#### Comportamento do evento do Webhook

* Um evento distinto de webhook é acionado quando um aluno recebe o status **Concluído via Alternativo** para um curso de destino.
* O evento é gerado quando o aluno conclui um curso de origem configurado que satisfaz o destino por meio de um relacionamento equivalente ou alternativo.
* Este webhook não é acionado para conclusões diretas de curso.
* Quando a conclusão retroativa ou a inconclusão retroativa estão ativadas, os eventos do webhook são emitidos para cada aluno e curso de destino afetados.

#### Detalhes da carga do Webhook

A carga do webhook de conclusão alternativa inclui os seguintes atributos de chave:

* **ID do aluno**\
  Identifica o aluno que recebeu a conclusão alternativa.

* **Curso de origem**\
  O curso ou caminho de aprendizado que o aluno concluiu diretamente.

* **Curso de destino**\
  O curso marcado como concluído por meio do relacionamento alternativo ou equivalente.

* **Método de conclusão**\
  Indica que o método de conclusão é **alternativo**.

* **Data de conclusão**\
  Derivado da data de conclusão do curso de origem.

* **Tipo de relação**\
  Especifica se a relação é **equivalente** ou **alternativa**.

Para cenários de inconclusão retroativa, os eventos do webhook indicam que uma conclusão alternativa existente foi revogada.

#### Considerações de integração

Os sistemas externos podem usar esses eventos de webhook para:

* Atualizar registros do aluno
* Sincronizar status de conclusão
* Acionar notificações ou fluxos de trabalho downstream
* Manter trilhas de auditoria para fins de conformidade

Os consumidores do webhook devem diferenciar explicitamente entre conclusões **diretas** e **alternativas**.\
As conclusões alternativas não concedem recompensas de habilidades, medalhas ou gamificação e devem ser tratadas adequadamente nos sistemas downstream.

### Impacto da retirada e exclusão de treinamento de origem em equivalentes e suplentes

O estado do ciclo de vida de um treinamento de origem (retirado ou excluído) afeta diretamente como as conclusões alternativas e equivalentes são mantidas para os alunos. O ALM lida com esses cenários de forma diferente para preservar a precisão histórica, garantindo que os relacionamentos atuais permaneçam válidos.

#### Desativação do treinamento de origem

##### Definição

Retirar um curso o torna indisponível para novas inscrições, ao mesmo tempo em que o mantém no sistema para fins de referência histórica, relatórios e auditoria.

##### Impacto

* As conclusões alternativas existentes concedidas por meio do curso de origem retirado permanecem válidas.
* Os alunos que concluíram anteriormente o curso de origem continuam a manter a conclusão alternativa para o curso de destino.
* Nenhuma nova conclusão alternativa é gerada a partir do curso inativo, pois ele não pode ser concluído por novos alunos.
* As transcrições e os relatórios do aluno continuam a exibir **Concluído via Alternativo** para os alunos afetados.

#### Excluindo treinamento de origem

#### Definição

Excluir um curso o remove totalmente do sistema, incluindo seus registros de conclusão e relacionamentos configurados.

#### Impacto

* Se a inconclusão retroativa estiver ativada, todas as conclusões alternativas concedidas por meio do curso de origem excluído serão revogadas.
* As transcrições e os relatórios do aluno são atualizados para mostrar a **Alternativa (Revogada)** para visibilidade de auditoria e conformidade.
* Os alunos podem perder o progresso ou o status de conclusão em programações de aprendizado, certificações ou pré-requisitos que dependem da conclusão alternativa revogada.
* Nenhuma conclusão alternativa adicional pode ser concedida a partir do curso excluído.

#### Fluxo de trabalho (WRK)

1. Um administrador desativa ou exclui o curso de origem usando a interface do administrador.
2. O sistema avalia todas as conclusões alternativas e equivalentes derivadas do curso de origem.
3. O status de conclusão é atualizado com base no estado do curso:
   * **Retirado:** as conclusões alternativas existentes permanecem inalteradas.
   * **Excluído:** conclusões alternativas são revogadas se a inconclusão retroativa estiver habilitada.
4. As transcrições e os relatórios do aluno refletem o status atualizado para suportar os requisitos de conformidade e auditoria.

### Sem encadeamento de relacionamentos

O ALM não oferece suporte ao encadeamento de relações alternativas ou equivalentes. Conclusões alternativas são concedidas apenas para relacionamentos configurados diretamente e não estão em cascata entre vários níveis de cursos.

#### Conceito: sem encadeamento de relacionamentos

#### Definição

Encadeamento refere-se a permitir que relacionamentos alternativos ou equivalentes se propaguem por vários cursos.\
Por exemplo, se o Curso A for uma alternativa para o Curso B e o Curso B for uma alternativa para o Curso C, o encadeamento implicaria que a conclusão do Curso A concederia a conclusão do Curso C.

#### Política

Não há suporte para encadeamento.\
Relacionamentos alternativos e equivalentes são avaliados somente em um único nível. Concluir um curso de origem concede a conclusão alternativa apenas ao seu curso ou cursos de destino imediato, não a alvos downstream.

#### Fluxo de trabalho (WRK)

#### Configuração de relacionamento

Um administrador define relações alternativas ou equivalentes entre os cursos, como:

* Curso A → Curso B
* Curso B → Curso C

#### Evento de conclusão

Um aluno conclui o curso A diretamente.

#### Ação do sistema

* O sistema concede a conclusão alternativa para o Curso B, se a relação A → B for definida.
* O sistema não concede conclusão alternativa para o Curso C, mesmo se existir uma relação B → C.

#### Requisito de conclusão direta

Para receber a conclusão alternativa do curso C, o aluno deve:

* Completar diretamente o curso B, ou
* Conclua um curso explicitamente configurado como uma alternativa direta ou equivalente para o Curso C.

### Implicações

#### Nenhum benefício indireto

Os alunos não podem receber crédito de conclusão para cursos mais abaixo em uma cadeia de relacionamento, a menos que cada curso (ou sua alternativa direta) seja concluído.\
Isso garante que os requisitos de aprendizado sejam atendidos de forma explícita e previsível.

#### Auditoria e relatórios simplificados

Relatórios e transcrições do aluno exibem conclusões alternativas somente para relacionamentos diretos.\
Isso evita trilhas de auditoria complexas e de vários saltos e garante clareza ao revisar como uma conclusão foi concedida.

### Compartilhamento de catálogo com contas entre parceiros: relacionamentos não compartilhados

O compartilhamento de catálogo permite que os objetos de aprendizado (LOs) sejam compartilhados entre contas entre parceiros, mas os relacionamentos alternativos e equivalentes são gerenciados de forma independente em cada conta e não são compartilhados.

#### Conceito: compartilhamento e relacionamentos do catálogo

#### Compartilhamento de catálogo

As contas podem compartilhar catálogos com contas entre parceiros para fornecer acesso a cursos, caminhos de aprendizado e outros objetos de aprendizado entre contas.

#### Relações não compartilhadas

Relações alternativas, equivalentes e de conclusão alternativa configuradas na conta de origem não são compartilhadas ou replicadas quando um catálogo é compartilhado.\
Cada conta mantém e avalia seus próprios relacionamentos de maneira independente.

### Fluxo de trabalho (WRK)

#### Compartilhamento de catálogo

Um administrador na **Conta A** compartilha um catálogo contendo objetos de aprendizado com a **Conta B**.

#### Configuração de relacionamento

A conta A pode ter relacionamentos alternativos ou equivalentes definidos entre os objetos de aprendizado no catálogo compartilhado.

#### Acesso à conta entre parceiros

A conta B recebe acesso aos objetos de aprendizado compartilhados, mas não herda nenhum relacionamento alternativo ou equivalente configurado na conta A.

#### Gerenciamento independente

Se a Conta B exigir um comportamento alternativo ou equivalente semelhante, um administrador da Conta B deverá configurar manualmente os relacionamentos nessa conta.

#### Implicações

#### Sem propagação automática de relacionamento

Relacionamentos alternativos e equivalentes não estão automaticamente disponíveis em contas entre parceiros por meio do compartilhamento de catálogo.

#### Configuração manual necessária

Cada conta entre parceiros é responsável por definir e gerenciar seus próprios relacionamentos para objetos de aprendizado compartilhados.

#### Considerações de consistência

O comportamento de conclusão, a satisfação de pré-requisitos e a emissão de relatórios podem diferir entre as contas, a menos que os relacionamentos sejam intencionalmente alinhados por meio da configuração manual.


### Comportamento downstream

Quando houver uma conclusão alternativa para um treinamento de destino, o ALM a usará nas verificações de downstream:

* Se o treinamento de destino for um **pré-requisito** para outros treinamentos, o aluno se tornará qualificado para esses treinamentos como se tivesse concluído o destino.
* Se o destino for um curso **obrigatório em um caminho de aprendizado**, a lógica de conclusão do caminho poderá tratar o aluno como tendo concluído essa parte e prosseguir para marcar o caminho como concluído quando outras condições forem atendidas.
* Conformidade e outros painéis, como o Painel de Controle de Sucesso do Grupo, que dependem do cumprimento de um requisito de treinamento podem incluir alunos que têm apenas conclusões alternativas.

O sistema distingue entre conclusão real e conclusão alternativa de modo que:

* Se o aluno realizar o treinamento de destino diretamente e concluí-lo posteriormente, essa conclusão direta pode anular a necessidade da conclusão alternativa.
* Se o relacionamento entre a origem e o destino for removido ou alterado, o ALM poderá remover ou ajustar as conclusões alternativas sem tocar nas conclusões originais, desde que as conclusões retroativas estejam habilitadas para a conta.

As conclusões alternativas são projetadas para não interferir na atividade real do aluno no treinamento de destino. Eles atuam como uma sobreposição que pode ser revisada se os relacionamentos mudarem.

