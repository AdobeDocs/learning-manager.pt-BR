---
description: Faça upload de documentos, políticas ou planos existentes para fundamentar a IA no conteúdo da sua organização. Escolha se deseja restringir a geração somente a esses arquivos ou deixar que o AI complemente com seu conhecimento geral.
jcr-language: en_us
title: Gerenciar arquivos de origem
source-git-commit: 229e407621281978f94783c3e9320c237c314fc3
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---


# Gerenciar arquivos de origem

**Gerenciar fontes** permite controlar o conteúdo que o Compositor de Conteúdo usa para gerar o curso. Adicione seus próprios documentos a um curso e escolha se deseja restringir a IA apenas a esse conteúdo ou deixá-la complementar o material com conhecimento próprio. Se você não adicionar documentos, o Compositor de conteúdo gera o curso usando o conhecimento existente do modelo de IA.

## Gerar um curso usando o material de origem

1. Selecione **Gerenciar Fontes** ou **Adicionar arquivos** no painel de chat ou na barra de ferramentas.
   ![](../assets/5_brief_manage_sources_prompt_updated.png)

2. Arraste um arquivo para a caixa de diálogo ou selecione **+ Adicionar arquivos de origem** para procurar. É possível adicionar vários arquivos de origem.
   ![](../assets/6_manage_sources_no_files_added_updated.png)

3. Selecione **Restringir saída ao conteúdo dos arquivos**. Isso permite que o compositor de conteúdo use apenas conteúdo de origem para gerar o curso. Se essa opção estiver desmarcada, o Compositor de conteúdo também usará a Web para criar um curso.
   ![](../assets/7_manage_sources_file_uploading_restrict_output_updated.png)

Formatos compatíveis:

| **Formato** | **Tamanho máximo** |
|-------------------------|--------------|
| PDF | 100 MB |
| Markdown (.md) | 100 MB |
| PowerPoint (.ppt/.pptx) | 100 MB |
| MS Word (.doc/.docx) | 100 MB |
| Arquivo de texto (.txt) | 100 MB |

Selecione **Continuar** para gerar a estrutura de tópicos do curso.

### Gerar sem material de origem

Execute as etapas abaixo para gerar a estrutura do curso quando não tiver um arquivo de origem como um documento de referência.

1. Selecione **Gerenciar fontes**. A caixa de diálogo **Gerenciar origens** é aberta.

2. Selecione **Não tenho nenhum material de origem - Gere o curso sem arquivos de origem** para permitir que a IA gere conteúdo de seu conhecimento geral. Quando essa opção não está selecionada e os arquivos são carregados, o AI restringe o conteúdo gerado somente aos seus documentos carregados.![](../assets/8_manage_sources_no_source_material_option_updated.png)

3. Selecione **Continuar** para gerar a estrutura de tópicos do curso.

### Atualizar um curso quando o material de origem for alterado

Os documentos de origem podem ficar desatualizados depois que um curso já foi gerado; uma política é revisada, um SOP recebe uma nova versão ou um conjunto de instruções é atualizado. Use esse fluxo de trabalho para alinhar o curso novamente com o material atual.

1. Selecione **Gerenciar Fontes** no painel de chat ou na barra de ferramentas para reabrir a caixa de diálogo.

2. Adicione os arquivos novos ou revisados usando **+ Adicionar arquivos de origem**.

3. Remova ou substitua quaisquer arquivos desatualizados para que a lista de origem reflita apenas o material atual.

4. Selecione Continuar para salvar a lista de origem atualizada.

5. Gere novamente as lições afetadas no Compositor de conteúdo, revise as alterações e publique novamente o curso. A republicação envia a atualização para o Adobe Learning Manager como uma nova versão do módulo - consulte Controle de versão do módulo no ALM.

### Confirme o upload do arquivo

    ![](../assets/9_manage_sources_file_ingested_confirmation_updated.png)

Depois que um arquivo é anexado, o ícone de arquivo na barra de ferramentas mostra uma contagem de medalhas. O assistente confirma o carregamento e oferece um atalho **Gerar estrutura de tópicos**. Selecione-o ou selecione **Gerar Estrutura de Tópicos** na barra de ferramentas superior.
