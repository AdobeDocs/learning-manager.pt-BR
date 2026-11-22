---
title: Navegador de Exame Seguro
description: Ative a integração do Navegador de exame seguro no nível da conta do Adobe Learning Manager para que os autores possam exigir um ambiente de navegador seguro para questionários nativos.
source-git-commit: 8f23f95cd81e5b64932281c990d27be0c390850b
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%
---

# Navegador de Exame Seguro

O Navegador de exame seguro fornece um ambiente seguro para que os alunos realizem questionários nativos do Adobe Learning Manager, restringindo o acesso a outros navegadores e aplicativos durante uma avaliação.

Os administradores podem ativar a integração do Navegador de exame seguro no nível da conta e carregar um arquivo de configuração (.seb) para definir as restrições do quiz. Depois que a integração estiver ativada, os autores podem configurar questionários individuais para exigir o uso do navegador Safe Exam.

Este artigo explica como ativar a integração do Navegador de exame seguro para sua conta.

## Ativar integração do Navegador do Safe Exam

Configure a integração do Navegador do Safe Exam para disponibilizar a opção para os Autores ao configurar os questionários. Antes de começar, certifique-se de ter o arquivo Safe Exam Browser para sua conta.

Para ativar a integração do navegador Safe Exam:

1. Faça logon no ALM como **Administrador**.
1. Selecione **Configurações** > **Geral**.
1. Navegue até a **integração do Navegador de Exame Seguro**.
1. Selecione **Editar**.

   Isso expande a **integração do Navegador de Exame Seguro**.

1. Selecione **Habilitar**.
1. Selecione **Procurar** e carregue o arquivo do Navegador de Exame Seguro do sistema. Exiba a configuração [Configurar o arquivo do navegador do exame seguro](#configure-the-seb-file-for-macos) para obter mais informações.

   ![Configurações de integração do Navegador de Exame Seguro nas Configurações gerais](assets/safe-exam-browser-integration-settings.png "Configurações de integração do Navegador de Exame Seguro nas Configurações gerais")

1. Selecione **Salvar**.

   O Navegador do Safe Exam agora está disponível para que os Autores ativem ao configurar questionários compatíveis.

Exiba [Criar um curso com o SEB](../../authors/feature-summary/create-a-course-with-safe-exam-browser.md) para obter mais informações sobre como configurar o Navegador de Exame Seguro como **Autor**.

### Configure o arquivo .seb para o macOS {#configure-the-seb-file-for-macos}

Crie um arquivo .seb usando a Ferramenta de configuração SEB para definir as restrições do quiz, as configurações de segurança e os aplicativos permitidos. Antes de usar o Navegador de exame seguro (SEB), certifique-se de que o arquivo .seb atende aos seguintes requisitos:

1. Defina o parâmetro browserWindowWebView como 3 (Inteiro) para habilitar o SEB.
1. Defina startURL para o URL que corresponde ao ambiente de destino.
1. Certifique-se de que o arquivo .seb inclua as informações obrigatórias do quitURL.
