---
title: Adicionar locais de sala de aula
description: Saiba como os administradores podem definir configurações e adicionar, migrar, editar e excluir locais de sala de aula no Adobe Learning Manager, e como adicionar traduções para um local de sala de aula.
source-git-commit: 6f2b9abf305665fe0b66007411455bd2210ee248
workflow-type: tm+mt
source-wordcount: '1641'
ht-degree: 3%

---


# Adicionar locais de sala de aula

Os administradores podem criar e gerenciar uma biblioteca de locais de sala de aula para reutilizar ao configurar eventos de treinamento ministrados pelo professor no módulo Sala de aula e Salas de aula virtuais. Para cada local, você pode definir detalhes como o nome do local, o limite de vagas e informações adicionais, incluindo um URL de local. Os autores podem selecionar esses locais predefinidos ao criar um curso.

Por padrão, o Adobe Learning Manager usa um formato de local de campo único. Para organizações que gerenciam Locais de Sala de Aula em vários países e idiomas, o Learning Manager também oferece suporte a um formato estruturado de quatro campos que inclui **País**, **Estado/Província/Região**, **Cidade** e **Nome do local**. Esse formato fornece recursos adicionais, como filtragem baseada em local e suporte a idiomas para locais individuais. Os administradores podem alternar para o formato de quatro campos por meio de uma migração única.

>[!NOTE]
>
>Se o formato de local de quatro campos não estiver ativado, os autores e alunos podem continuar usando os Locais de sala de aula normalmente. O formato de local de campo único existente permanece disponível e nenhuma alteração é necessária. Exiba [Migrar para o método de quatro campos](#migrate-classroom-locations-to-the-four-field-format) para obter mais informações.

## Definir configurações do Local da Sala de Aula

Os administradores podem controlar se os autores podem criar e gerenciar locais de sala de aula. Use as configurações de **Locais de sala de aula** para definir o nível de acesso disponível para os autores.

Para definir as configurações de **Locais de Sala de Aula**:

1. Faça logon no Adobe Learning Manager como **Administrador**.
1. Selecione **Configurações** > **Locais de sala de aula**.

   Isso exibe a página **Locais de Sala de Aula**.

1. Selecione a guia **Configurações**.

   ![Guia Configurações para Locais de Sala de Aula](assets/classroom-locations-settings-tab.png)

   *Habilite os privilégios de Autor para os locais de Sala de Aula e Sala de Aula Virtual na guia **Configurações**.*

1. Selecione **Editar**.

   A alternância se torna editável, permitindo que você atualize as seguintes configurações:

   | **Configuração** | **Descrição** |
   |---|---|
   | **Permitir que autores criem locais** | Ative esta opção para permitir que os autores criem locais de módulos de sala de aula e sala de aula virtual ao criar sessões de treinamento ministradas por instrutor. |
   | **Permitir que autores modifiquem e excluam locais** | Ative esta opção para permitir que os autores editem ou excluam locais de sala de aula e sala de aula virtual. |

1. Selecione **Salvar**.

## Criar e gerenciar locais de sala de aula

Os administradores podem criar e gerenciar locais de sala de aula que os autores podem reutilizar ao criar sessões de treinamento em sala de aula e sala de aula virtual. O Adobe Learning Manager suporta dois formatos de local:

* **Formato de campo único**: cada local da sala de aula é identificado por um único campo **Nome do local**. Exiba [Adicionar um Local da Sala de Aula usando um formato de campo único](#add-a-classroom-location-using-a-single-field-format) para obter mais informações.
* **Formato de quatro campos**: cada local da sala de aula é organizado em **País**, **Estado/Província/Região**, **Cidade** e **Nome do local**, facilitando o gerenciamento de locais em várias regiões. Se sua conta atualmente usa o formato de campo único, conclua a migração única antes de alternar para o formato de quatro campos. Exiba [Migrar para o método de quatro campos](#migrate-classroom-locations-to-the-four-field-format) para obter mais informações.

### Adicionar um local da sala de aula usando um formato de campo único

Você pode adicionar um Local da sala de aula usando o formato de campo único:

1. Faça logon no Adobe Learning Manager como **Administrador**.
1. Selecione **Configurações** > **Locais de sala de aula**.
1. Selecione **Adicionar** > **Novo Local**.
1. Insira os seguintes detalhes na caixa de diálogo **Locais de Sala de Aula**:

   1. Digite o **Nome do local**. Use um nome exclusivo. Caso contrário, o Learning Manager exibirá uma mensagem de erro.
   1. Digite a descrição do local no campo **Informações do local**. Este campo é opcional.
   1. Digite o **URL do local**. Os alunos podem ver essas informações nos detalhes da sala de aula. O URL também pode ser um URL de localização de mapas, se necessário. Este é um campo opcional.
   1. Digite e selecione a **Região do Local**. Este campo é opcional.
   1. Digite o número de licenças disponíveis no campo **Limite de vagas**. Isso indica a capacidade da sala de aula. Esse valor pode ser alterado ao criar o evento real de treinamento ministrado pelo professor.
      ![Adicionar um local de sala de aula usando o formato de campo único](assets/add-classroom-location-single-field-format.jpeg)
      *Adicione um Local de Sala de Aula usando o formato de campo único.*

### Migrar locais de sala de aula para o formato de quatro campos

Se sua conta usa o formato antigo de local da sala de aula de campo único, migre seus locais da sala de aula existentes antes de ativar o formato de quatro campos. O formato de quatro campos organiza os dados de local em **País**, **Estado/Província/Região**, **Cidade** e **Nome do local**, facilitando o gerenciamento de locais em várias regiões.

Essa migração é um processo único. Depois de mudar para o formato de quatro campos, você não pode reverter a conta para o formato de campo único.

Para migrar locais existentes:

1. Navegue até **Administrador** > **Locais de sala de aula** e selecione a guia **Configurações**.
1. Selecione **Exportar** na seção **Migração de formato de local**.

   Um arquivo CSV com seus locais de sala de aula existentes é baixado. As seguintes colunas estão disponíveis:

   1. **room_id**: identificador exclusivo do local.
   1. **localidade**: a localidade para o Nome de Local e as Informações de Local traduzidos.
   1. **nome**: nome da sala de aula.
   1. **país**: país onde a sala de aula está localizada.
   1. **estado**: estado, província ou região onde a sala de aula está localizada.
   1. **cidade**: cidade onde a sala de aula está localizada.
   1. **informações**: detalhes adicionais, como nome do edifício, andar ou número da sala.
   1. **url**: URL associada ao local, como um link de mapa.
   1. **limite de vagas**: capacidade máxima da sala de aula.

   >[!NOTE]
   >
   >O CSV exportado sempre inclui as colunas de formato de local de quatro campos, mesmo quando o formato de quatro campos não está ativado.

   ![Verificar o andamento da migração](assets/location-format-migration-progress.png)

   *Verifique o andamento da migração antes de alternar para o formato de local de quatro campos.*

1. Para cada nome de coluna, atualize o arquivo CSV com as informações necessárias, como País, Estado, Cidade, juntamente com todas as outras informações necessárias.
1. Selecione **Importar** e carregue o arquivo CSV atualizado.

   O Adobe Learning Manager valida os dados e atualiza o andamento da migração.

1. Quando a barra de progresso da migração atingir 100%, selecione **Alternar para o novo formato de 4 campos**. O status de **Migração de formato de local** é atualizado para **Migração concluída**.

   ![Status de conclusão da migração de formato de local](assets/location-format-migration-complete.png)

   *A migração em formato de local atualiza o status de Migração concluída.*

## Adicionar locais de sala de aula usando um formato de quatro campos

Após concluir a migração única, os administradores podem criar locais de sala de aula no formato de quatro campos. Os autores podem reutilizar esses locais ao criar sessões de treinamento ministradas pelo professor. Os administradores podem adicionar locais de sala de aula individualmente ou importar vários locais de sala de aula de um arquivo CSV.

### Adicionar um local de sala de aula

Use os locais da sala de aula para padronizar locais de treinamento e simplificar o agendamento de sessões para autores.

Para adicionar um local da sala de aula:

1. No aplicativo de administração, selecione **Configurações** > **Locais de sala de aula**.

   ![Guia Todos os Locais](assets/all-locations-tab.png)

   *Selecione a guia **Todos os Locais**para adicionar um Local de Sala de Aula.*

1. Selecione **Adicionar** > **Novo local** no canto superior direito.

   A janela pop-up **Local da sala de aula** é exibida.

   ![Janela pop-up Local da Sala de Aula](assets/classroom-location-popup-window.png)

   *Insira os detalhes na janela pop-up Local da Sala de Aula.*

1. Na janela pop-up **Local da Sala de Aula**, insira os seguintes detalhes:

   | **Campo** | **Descrição** |
   |---|---|
   | **País** | Selecione o país onde está a sala de aula. |
   | **Estado/Província/Região** | Selecione o estado, província ou região. |
   | **Cidade** | Selecione a cidade onde fica a sala de aula. |
   | **Nome do Local** | Insira o nome da sala de aula ou sala. |
   | **Informações de Local** | Informe detalhes adicionais, como o nome do edifício, andar ou número da sala. |
   | **URL do local** | Insira um URL para o local, como um link de mapa. |
   | **Limite de vagas** | Insira a capacidade máxima de assentos da sala de aula. |

1. Selecione **Salvar**.

   O local da sala de aula é salvo e listado na guia **Todos os locais**.

### Importar locais de sala de aula em massa

Use a importação em massa para adicionar vários locais de sala de aula ou atualizar os locais existentes usando um arquivo CSV.

Para importar locais de sala de aula em massa:

1. No aplicativo de administração, selecione **Configurações** > **Locais de sala de aula**.
1. Selecione **Baixar CSV** na guia **Todos os Locais**.

   Um arquivo CSV que contém seus locais de sala de aula existentes é baixado. As seguintes colunas estão disponíveis:

   1. **room_id**: identificador exclusivo do local.
   1. **localidade**: a localidade para o Nome de Local e as Informações de Local traduzidos.
   1. **nome**: nome da sala de aula.
   1. **país**: país onde a sala de aula está localizada.
   1. **estado**: estado, província ou região onde a sala de aula está localizada.
   1. **cidade**: cidade onde a sala de aula está localizada.
   1. **informações**: detalhes adicionais, como nome do edifício, andar ou número da sala.
   1. **url**: URL associada ao local, como um link de mapa.
   1. **limite de vagas**: capacidade máxima da sala de aula.

1. Para cada nome de coluna, atualize o arquivo CSV com as informações necessárias, como País, Estado, Cidade, juntamente com todas as outras informações necessárias.
1. Selecione **Adicionar** > **Locais de importação em massa** no canto superior direito.

   A janela pop-up **Importar CSV de Locais** é exibida.

   ![Janela pop-up Importar CSV de Locais](assets/import-locations-csv-popup.png)

   *Arraste e solte o CSV com as informações atualizadas.*

1. Arraste e solte o arquivo CSV atualizado na área de upload.
1. Selecione **Importar**.

   Os Locais de sala de aula são atualizados.

## Adicionar traduções para um local da sala de aula

Adicione traduções para os campos **Nome do local** e **Informações do local** para exibir detalhes do Local da Sala de Aula nos idiomas preferidos do aluno.

Para adicionar traduções a um local da sala de aula:

1. Selecione **Todos os locais** > **Adicionar** dos **Locais de sala de aula**.
1. Selecione **Novo Local**.

   A janela pop-up **Local da sala de aula** é exibida.

1. Selecione **Adicionar Novo Idioma**.

   A janela pop-up **Adicionar Novo Idioma** é exibida.

   ![Janela pop-up Adicionar Novo Idioma](assets/add-new-language-popup.png)

   *Selecione os idiomas na janela pop-up Adicionar Novo Idioma.*

1. Selecione **Salvar**.

   As traduções são salvas e exibidas aos usuários.

>[!NOTE]
>
>Somente os campos **Nome do Local** e **Informações do Local** oferecem suporte a traduções. Detalhes do local, como **País**, **Estado/Província/Região** e **Cidade**, não foram traduzidos.

## Editar um local da sala de aula

Para editar um Local da sala de aula, siga estas etapas:

1. No aplicativo de administração, selecione **Configurações** > **Locais de sala de aula**.
1. Passe o mouse sobre o local da sala de aula desejado que deseja editar.

   ![Ícone Editar para um Local de Sala de Aula](assets/edit-classroom-location-icon.png)

   *Passe o mouse sobre o Local da Sala de Aula necessário e selecione o ícone de edição.*

1. Selecione o ícone **Editar Local da Sala de Aula**.

   A janela pop-up Local da sala de aula é exibida.

1. Modifique o Local da Sala de Aula e selecione **Salvar**.

## Excluir um local da sala de aula

Para excluir um Local da sala de aula, siga estas etapas:

1. No aplicativo de administração, selecione **Configurações** > **Locais de sala de aula**.
1. Passe o mouse sobre o local da sala de aula desejado que deseja excluir.
1. Selecione o ícone **Excluir local da sala de aula**.

   A janela pop-up Confirmação necessária é exibida.

   ![Janela pop-up de Confirmação Necessária](assets/delete-classroom-location-confirmation.png)

   *Selecione Excluir para confirmar a exclusão de um Local de Sala de Aula.*

1. Selecione **Excluir**.

## Perguntas frequentes

1. **O que acontece com os Locais de Sala de Aula existentes após a conclusão da migração?**<br>
Você pode ativar o formato de local de quatro campos somente depois que todos os locais existentes forem migrados, manualmente ou por meio de um upload de CSV. Depois que o formato de quatro campos é ativado, todos os cursos existentes que usam Locais de sala de aula exibem locais no novo formato.

1. **Preciso reestruturar manualmente o CSV exportado para corresponder ao formato de local de quatro campos?**<br>
Não. O arquivo CSV exportado sempre usa o formato de local de quatro campos, independentemente de estar ativado no momento. Você só precisa atualizar os valores ausentes antes de importar o arquivo.

1. **A migração afeta os relatórios do Adobe Learning Manager?**<br>
Sim. Após a migração, os relatórios que incluem informações do Local da sala de aula exibem os locais no seguinte formato:

   **País > Estado/Província/Região > Cidade > Nome do Local**

   Esse formato substitui o valor anterior do local de campo único.

1. **O que acontece se eu não habilitar o formato de localização de quatro campos?**<br>
Nada é alterado para autores ou alunos. Os locais de sala de aula continuam a aparecer e funcionar como hoje, usando o formato de campo único existente até que um administrador conclua a migração e ative o formato de quatro campos.
