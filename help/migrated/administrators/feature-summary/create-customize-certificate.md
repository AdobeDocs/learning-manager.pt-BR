---
title: Criar e personalizar um certificado
description: Os certificados personalizados no Adobe Learning Manager (ALM) permitem que administradores e autores projetem, gerenciem e emitam certificados personalizados para alunos.
jcr-language: en-us
exl-id: 99e20f00-9f8f-477f-9416-24636ed23b87
source-git-commit: 13fbdb95129ba7612e8e42d3da88ef3c6784e729
workflow-type: tm+mt
source-wordcount: '2628'
ht-degree: 0%

---

# Certificados personalizados no Adobe Learning Manager

## Introdução

Os certificados personalizados no Adobe Learning Manager mudam a forma como os administradores projetam, gerenciam e fornecem certificados de conclusão.

Os administradores podem:

- Crie certificados em um editor visual no estilo de tela em vez de escrever código.
- Anexar certificados a cursos, programações de estudo e certificações com padrões flexíveis.
- Use planos de fundo generativos viabilizados por Adobe Firefly, mantendo as necessidades de marca e conformidade em mente.
- Migrar de modelos de HTML existentes e permanecer compatível com registros históricos do aluno.

O processo de certificação segue a medalha existente e o modelo de realização no Learning Manager, para que o comportamento do aluno se mantenha familiar, enquanto os administradores e as equipes de suporte gastam menos tempo nas operações de certificação.

>[!NOTE]
>
>Os recursos de certificado que usam IA generativa estão sujeitos à cota. O limite é de 10.000 solicitações por cliente.

## Principais recursos da certificação personalizada

### Designer de certificados (editor de estilo de tela)

Um designer de certificados de arrastar e soltar fornece uma tela WYSIWYG (what-you-see-is-what-you-get, o que você vê é o que você recebe), na qual os administradores podem criar e gerenciar designs sem habilidades em HTML ou CSS.

**Edição visual**

- Arraste, posicione, redimensione, vire e gire texto e imagens.
- Alinhar elementos (superior, inferior, esquerda, direita); enviar para trás ou trazer para a frente.
- Duplique ou clone elementos para trabalho de layout mais rápido.

**Elementos com suporte**

- Campos de texto com controles de fonte, cor, tamanho e alinhamento.
- Espaços reservados dinâmicos (por exemplo, nome do aluno, nome do curso ou certificação, data, campos da conta e campos de usuário ativos onde apenas atributos de valor único são permitidos).
- Imagens, incluindo logotipos e medalhas, com redimensionamento manual preferencial em relação ao ajuste automático para um layout previsível.

**Plano de fundo e layout**

- Orientação retrato ou paisagem (corrigida após a criação).
- Fundos como cores sólidas ou imagens com transparência ajustável.
- Galeria de imagens com imagens predefinidas e fundos compartilhados.
- Controles de zoom (50%-150%) e alinhamento de grade ou ajuste.

**Localização**

- Suporte a vários locais em que cada local tem seu próprio arquivo de layout.
- Quando você adiciona um código do idioma, seu layout é copiado do código do idioma padrão e pode ser personalizado.
- Menu suspenso Idioma com visualização por local em tempo de design.

**Ciclo de vida de rascunho e publicação**

- Salve designs como rascunhos; rascunhos não podem ser usados para emissão.
- Após a publicação, a estrutura de design é bloqueada; algumas edições podem exigir a duplicação do design.
- Visualização de PDF em tempo real para verificar o layout antes do lançamento.

### Catálogo e listagem de modelos

A página de listagem **Design do Certificado** ajuda os administradores a gerenciar modelos de certificado em escala:

- Catálogo baseado em blocos com as guias **Publicado** e **Rascunho**.
- Pesquise por título do certificado; filtre por **Orientação**.
- Ações em cada design:
   - Duplicada (para variantes).
   - Definido como padrão no nível de **Conta**, **Curso**, **Caminho de Aprendizado** ou **Certificação**.
   - Desative ou desative modelos que não estão mais em uso.
- Suporte a modelos de fornecedores terceirizados que podem ser integrados e reutilizados.

### Configuração e herança flexíveis

Os administradores podem configurar certificados em vários níveis:

**Padrões em nível de conta**

- Defina um design de certificado padrão para todos os novos objetos de aprendizado (LOs).
- O padrão atua como um ponto de partida; os LOs existentes não são alterados automaticamente quando o padrão da conta é alterado.

**Substituições em nível de instância**

- Configuração em nível de instância para cursos, certificações e programações de aprendizado, incluindo:
   - Marca por coorte (por exemplo, para regiões diferentes ou contas de parceiros).
   - Designs de certificado diferentes para ciclos de certificação recorrentes.

**Resolução e fallback de certificados**

Quando um aluno conclui o treinamento, o Learning Manager escolhe um design nesta ordem:

- Configuração da instância do LO
- Configuração do LO
- Modelo padrão do OA
- Modelo padrão da conta

### planos de fundo generativos baseados em Adobe Firefly

Para ajudar os clientes a produzir certificados consistentes com a marca em escala, o designer se integra ao Adobe Firefly:

- Os administradores geram planos de fundo a partir de prompts de palavras-chave e um esquema de cores (por exemplo, “minimalista, da área de saúde, paleta azul-petróleo”).
- Uma biblioteca de palavras-chave com curadoria é compatível com setores comuns (transporte, assistência médica e outros) de usuários que não são designers.
- As imagens geradas são adicionadas à galeria de plano de fundo e podem ser reutilizadas em todos os modelos.
- O crédito e a classificação por níveis para o uso de Firefly no Learning Manager são definidos pela política do produto.

### Migração de certificado de HTML herdado

Os modelos de certificado de HTML ou ZIP existentes são preservados, mas não podem ser editados no novo designer:

- Os modelos herdados são migrados com sinalizadores como `isLegacy` / `is_active`.
- Eles aparecem como entradas não editáveis (sem visualização WYSIWYG) e permanecem válidos para uso histórico.
- Quando as medalhas são vinculadas a modelos herdados, a migração mantém os certificados para download; onde a configuração não pode ser preservada, os padrões globais são aplicados.

### geração de PDF e pré-cozedura

Para melhorar o desempenho do tempo de execução e a experiência do aluno:

- Os certificados são pré-assados no momento da conclusão (quando o OA é concluído) e, em seguida, armazenados em cache para que os alunos possam baixá-los rapidamente.
- Os fluxos de alunos existentes para baixar certificados por meio de **Medalhas** e **Conquistas** permanecem os mesmos.

## O desafio

Atualmente, o gerenciamento de certificados no Learning Manager depende de um modelo de código pesado e de suporte pesado:

**Alta dependência de CSM e equipes de suporte**: os administradores fornecem arquivos HTML ou ZIP que os CSMs ou a engenharia carregam por meio de ferramentas internas. Cada alteração (marca, logotipos, texto normativo, assinaturas) precisa de um tíquete interno e ciclo de implantação.

**Agilidade limitada para equipes de negócios**: as equipes de marketing, conformidade ou RH geralmente precisam de atualizações de certificado frequentes e localizadas (idiomas, campanhas, regras específicas do país). O fluxo de trabalho atual torna mais lentas essas atualizações e atrasa os programas de conformidade.

**Configuração fragmentada e herança desconhecida**: modelos de HTML herdados podem ser definidos em nível de conta, objeto de aprendizado padrão e objeto de aprendizado com regras de fallback complexas. Sem uma configuração personalizada clara de vários níveis, pode ser difícil ver qual modelo se aplica onde.

**Restrições de vínculo de medalha** Os certificados estão fortemente acoplados a **medalhas**:

- Um certificado deve estar associado a uma medalha; não há emissão somente de certificado.
Esse acoplamento pode complicar as alterações de design quando os administradores desejam certificados sem elementos de gamificação.

**Criação não visual e inconsistência de marca**: os certificados baseados em HTML são flexíveis, mas precisam de habilidades de front-end que muitos administradores não têm. Alguns clientes confiam em certificados padrão genéricos, o que enfraquece a consistência da marca.

**Lacuna competitiva**: alguns sistemas de gerenciamento de aprendizado incluem designers de certificados personalizados nativos (por exemplo, Docebo). O design de certificado de autoatendimento nesta área tem sido uma lacuna conhecida para o Adobe Learning Manager.

O resultado é alteração lenta, alto custo de suporte e uma experiência de criação que não corresponde às expectativas do administrador para certificados e credenciais.

## Como as certificações personalizadas abordam esses desafios

### Fluxos de trabalho de autoatendimento e de fácil utilização pelo administrador

Veja os fluxos de trabalho:

- O designer de certificados e a lista substituem scripts de upload de HTML e provisionamento interno por uma experiência orientada pelo administrador:
- Os administradores criam, publicam e desativam designs de certificados no Learning Manager sem o envolvimento de código ou CSM.
- As atualizações de design (por exemplo, marca sazonal ou específica do parceiro) levam minutos na interface, em vez de tíquetes e ciclos de engenharia.
- Os padrões em nível de conta e de objeto de aprendizado reduzem a configuração repetitiva por objeto.

### Redução das despesas gerais de suporte e dos riscos operacionais

Ao consolidar o gerenciamento de certificados em **Conquistas** com uma experiência de usuário clara:

- Cargas de trabalho para solicitações de “upload ou alteração do meu certificado” descartadas para equipes de CSM e engenharia.
- O produto aplica restrições seguras (por exemplo, orientação bloqueada, modelos herdados não editáveis) para reduzir o risco de implantações existentes.
- Os modelos herdados migrados mantêm os certificados históricos disponíveis sem esforço de suporte extra.

### Controle, consistência e controle da marca

Os padrões, Firefly e galerias ajudam os clientes a:

- Envie modelos de marca uma vez no nível da conta e substitua somente onde for necessário.
- Use planos de fundo de Firefly dentro dos resguardos da empresa em vez de ativos externos ad hoc.
- Administre certificados por meio dos estados publicar e aposentar, com rascunhos visualizáveis antes da implantação.

### Alinhamento com fluxos de crachás e certificados existentes

O design mantém o caminho atual do aluno: os certificados ainda são baixados de **Medalhas** e **Conquistas**, o que limita o novo treinamento.

### Desempenho e escalabilidade

Certificados pré-configurados e desempenho do alvo de renderização orientado por JSON:

- Os certificados são gerados na conclusão e armazenados, portanto, o download é efetivamente uma recuperação estática.
- Os designs baseados em JSON permanecem leves para o editor e para a renderização em tempo de execução em escala.

## Casos de uso reais

### Treinamento de clientes e parceiros: credenciais de marca em escala

**Cenário:** uma empresa de software executa academias de clientes e parceiros com centenas de programas em várias regiões e marcas.

- Use modelos padrão em nível de conta com planos de fundo gerados por Firefly alinhados a cada linha de produto.
- Adicione layouts específicos de locais para títulos de certificação localizados, isenções de responsabilidade e assinaturas regulatórias.
- Para parceiros premium, duplique modelos base e adicione identidade visual de parceiro (logotipo e texto legal) no nível da instância.
- Os PDF pré-cozidos permitem que os parceiros baixem certificados logo após a conclusão das certificações de parceiros, com carga mínima no Learning Manager.

Esse padrão se encaixa em ecossistemas de franquias ou de várias marcas em que os certificados reforçam o valor da marca e do parceiro (por exemplo, grandes redes de parceiros, como a RealPage).

### Treinamento em conformidade e regulamentação: ambientes de várias localidades e de alta alteração

**Cenário:** uma empresa regulamentada deve atualizar o texto do certificado de conformidade com frequência por país e idioma.

- A **edição liderada pelo administrador** permite que as equipes legais ou de conformidade alterem as palavras e os campos dinâmicos sem tíquetes de engenharia.
- Layouts específicos de localidade oferecem suporte a **isenções de responsabilidade específicas de país ou região** e assinaturas em um backbone de design compartilhado.
- A **lógica de fallback** garante que, se um modelo de instância do LO específico estiver ausente, o sistema ainda usará padrões seguros e evitará falhas de emissão.

Isso se aplica a instituições de saúde, finanças, governo e outros setores nos quais o texto do certificado muda com frequência e é auditado.

### Certificações recorrentes com conteúdo de catálogo par ou compartilhado

**Cenário:** uma conta principal do Learning Manager compartilha conteúdo com várias **contas entre parceiros** (por exemplo, várias contas de clientes), cada uma com certificações recorrentes e seus próprios certificados.

- Contas entre parceiros podem **adicionar cursos adquiridos a certificações recorrentes** e configurar **modelos de certificados locais** no nível da instância.
- As atualizações do curso do fluxo da conta principal para as recorrências esperadas, enquanto os designs do certificado podem permanecer **por cliente**.

### Programas internos de capacitação e liderança

**Cenário:** programas internos (por exemplo, aceleradores de gerentes ou academias de produtos) desejam **certificados visualmente distintos** que os administradores possam atualizar sem trabalho de HTML.

- Os proprietários do programa podem criar **modelos de marca de programa** (por exemplo, acadêmicos internos ou visuais no estilo MAP) sem habilidades de HTML.
- As substituições no nível da instância permitem que diferentes coortes ou regiões usem variantes (por exemplo, identidade visual regional ou específica da coorte).
- fundos de Firefly dão suporte a visuais **específicos de evento ou de coorte** com menos dependência de equipes de design.

### Transição de certificados HTML herdados

**Cenário:** os clientes existentes usam certificados personalizados HTML5 gerenciados por CSMs.

- Os modelos de HTML ou ZIP herdados são migrados e marcados como herdados, o que preserva o uso e os downloads anteriores.
- Os administradores podem migrar para modelos baseados em designer ao longo do tempo, começando com programas de alta prioridade.
- Se a migração não puder preservar um mapeamento (por exemplo, medalhas desativadas no meio do caminho), o sistema volta para o modelo padrão global para que os alunos não sejam bloqueados.

## Criar um certificado personalizado

**Pré-requisito**

Para usar imagens do Firefly, sua instância do Adobe Learning Manager deve ser integrada ao Firefly.

1. Entre no Adobe Learning Manager como **Administrador**.
2. Na seção **Configurar**, selecione **Conquistas**. A página **Medalhas** é aberta.
   ![Criar um certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate1.png)
   *Navegue até Conquistas no painel de navegação esquerdo*

3. No painel de navegação esquerdo, selecione **Certificados**. A página **Certificados** é aberta.
   ![Criar um certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate2.png)
   *A página Certificado*

4. Na área superior direita da página, selecione **Novo certificado**. A caixa de diálogo **Criar um Novo Certificado** é aberta.
5. Selecione **Paisagem** ou **Retrato**, dependendo da aparência do certificado. Depois de selecionar uma orientação, você verá um modelo em branco e modelos prontos para essa orientação.
   ![Criar um certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate3.png)
   *Opção Paisagem ou Retrato*

6. Selecione o modelo em branco ou um modelo existente.
7. Insira um nome de certificado.
8. No menu suspenso, selecione um idioma padrão.
9. Selecione **Criar**. Se você tiver escolhido o modelo em branco, uma tela em branco será exibida abaixo do nome do certificado.
10. Adicione elementos: **Texto**, **Imagem**, **Valor Dinâmico** e **Fundo do Certificado**.
    ![Criar um certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate4.png)
    *Adicionar elementos ao certificado*

11. Para **Texto**, adicione conteúdo em **Texto pré-formatado** ou **Modelos de texto** ou adicione texto personalizado. O texto é exibido na tela. Quando o texto é selecionado, as opções de formatação aparecem acima da tela. Para remover o conteúdo indesejado, selecione o ícone **Excluir** no canto superior direito da tela.
12. Para adicionar imagens, selecione **Imagem** ao lado de **Adicionar elementos**. Faça upload de imagens do seu computador ou selecione imagens nas listas de categorias.
13. Selecione **Valor Dinâmico** para adicionar detalhes básicos, etiquetas de catálogo e campos ativos.
14. Selecione **Fundo do Certificado** para aplicar cores ou imagens. Para criar imagens com Adobe Firefly, selecione **Gerar Imagem**.
15. No campo de prompt, descreva o que deseja (até 100 caracteres) e selecione **Gerar**. Quatro opções de imagem são exibidas com base no seu prompt.
16. Selecione a imagem desejada. É aplicado como fundo do certificado.
    ![Criar um certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate5.png)
    *Adicionar imagem ao certificado*

17. Selecione **Visualizar** para revisar o certificado antes de publicar. Isso ajuda a entender como o certificado se parece.
    ![Criar um certificado personalizado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/create-custom-certificate6.png)
    *Visualizar o certificado*

18. Na visualização, é possível salvar no Google Drive, baixar, imprimir ou usar outras opções, como propriedades de anotação ou do documento.
19. Selecione **Salvar como Rascunho** para continuar mais tarde ou selecione **Publish** para publicar o certificado. Após a publicação, os alunos podem baixar o certificado quando cumprirem a etapa configurada.

Depois de salvar um certificado em **Publicado** ou **Rascunhos**, você pode editá-lo, cloná-lo, renomeá-lo ou excluí-lo.

## Editar um certificado personalizado

1. Na seção **Configurar**, selecione **Conquistas**. A página **Medalhas** é aberta.
2. No painel de navegação esquerdo, selecione **Certificados**. A página **Certificados** é aberta.
3. Selecione a guia **Publicado** ou **Rascunhos** para o certificado desejado.
4. Abra o menu de ações (**...**) do certificado e selecione **Editar**.
   ![Editar certificado no menu de ações](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0001.png)
   *Opção Editar no menu suspenso*

5. Faça as alterações.
6. Selecione **Publish** ou **Salvar como Rascunho**.

## Clonar um certificado personalizado

Use **Clonar** quando desejar uma cópia de um certificado para um novo nome ou um caso de uso semelhante. Após clonar, renomeie o certificado para que ele tenha um nome distinto; caso contrário, o nome poderá corresponder à origem, mesmo se você tiver alterado o design.

>[!NOTE]
>
>Não é possível definir um novo nome enquanto você salva imediatamente após o clone. Renomeie o certificado depois que ele for salvo como um rascunho ou publicado.

1. Na seção **Configurar**, selecione **Conquistas**. A página **Medalhas** é aberta.
2. No painel de navegação esquerdo, selecione **Certificados**. A página **Certificados** é aberta.
3. Selecione a guia **Publicado** ou **Rascunhos** para o certificado desejado.
4. Abra o menu de ações (**...**) para o certificado e selecione **Clonar**.
   ![Clonar certificado do menu de ações](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0002.png)
   *Opção Clonar no menu suspenso*

5. Faça as alterações.

6. Selecione **Publish** ou **Salvar como Rascunho**.

7. Renomeie o certificado clonado usando as etapas em [Renomear um certificado personalizado](#rename-a-custom-certificate).

## Renomear um certificado personalizado

É possível renomear um certificado sem cloná-lo.

1. Na seção **Configurar**, selecione **Conquistas**. A página **Medalhas** é aberta.
2. No painel de navegação esquerdo, selecione **Certificados**. A página **Certificados** é aberta.
3. Selecione a guia **Publicado** ou **Rascunhos** para o certificado desejado.

4. Abra o menu de ações (**...**) do certificado e selecione **Renomear**.
   ![Renomear certificado do menu de ações](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0003.png)
   *Opção Renomear no menu suspenso*

5. Na caixa de diálogo **Renomear certificado**, insira o novo nome.
   ![Caixa de diálogo Renomear certificado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0004.png)
   *Insira um novo nome*

6. Selecione **Salvar**. O Learning Manager mostra uma mensagem de confirmação.

## Como excluir um certificado personalizado

A exclusão de um certificado não pode ser desfeita. Continue apenas se tiver certeza.

>[!NOTE]
>
>Não é possível excluir um certificado anexado a um objeto de aprendizado ou instância.

1. Na seção **Configurar**, selecione **Conquistas**. A página **Medalhas** é aberta.
2. No painel de navegação esquerdo, selecione **Certificados**. A página **Certificados** é aberta.
3. Selecione a guia **Publicado** ou **Rascunhos** para o certificado desejado.
4. Abra o menu de ações (**...**) do certificado e selecione **Excluir**. O Adobe Learning Manager mostra uma mensagem de confirmação.
   ![Excluir certificado do menu de ações](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0005.png)
   *Opção Excluir no menu suspenso*
   ![Excluir confirmação do certificado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0006.png)
   *Mensagem de confirmação*

5. Selecione **Sim**. Se o certificado não estiver anexado a um objeto de aprendizado ou instância, o Learning Manager concluirá a exclusão e poderá mostrar outra confirmação.

## Definir um certificado personalizado como o certificado padrão

É possível definir um certificado como padrão para:

- Treinamentos
- Caminhos de aprendizado
- Certificações
- Todos

![Opções de certificado padrão](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0007.png)
*Definir como certificado padrão*

1. Na seção **Configurar**, selecione **Conquistas**. A página **Medalhas** é aberta.
2. No painel de navegação esquerdo, selecione **Certificados**. A página **Certificados** é aberta.
3. Selecione a guia **Publicado** ou **Rascunhos** para o certificado desejado.
4. Abra o menu de ações (**...**) para o certificado, selecione **Definir como padrão** e selecione uma das quatro opções. O Learning Manager mostra uma mensagem de confirmação.
5. Selecione **Sim**. O Learning Manager mostra outra confirmação. O certificado mostra um rótulo **Padrão para** com a categoria selecionada (por exemplo, **Padrão para treinamentos**).
   ![Padrão para rótulo de categoria no certificado](/help/migrated/administrators/feature-summary/assets/custom-cert-alm_images/image_0008.png)
   *Depois de se tornar o certificado padrão*
