---
title: Criar um curso com o Navegador do exame seguro
description: Crie um quiz com o modo Navegador de exame seguro e adicione-o a um curso como um módulo em ritmo individualizado no Adobe Learning Manager para fornecer um ambiente de avaliação restrito.
source-git-commit: 6629e193116a8c2de12606277986811b20bbdf90
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%
---

# Criar um curso com o Navegador do exame seguro

Os autores podem adicionar questionários aos cursos que exigem o Navegador de exame seguro para fornecer um ambiente de avaliação seguro e restrito. O navegador Safe Exam se aplica somente a questionários nativos individuais do Adobe Learning Manager e não restringe o acesso a outros módulos do curso.

Antes de adicionar o quiz a um curso, certifique-se de que o Navegador de exame seguro esteja ativado para o quiz. Se o curso incluir outros tipos de entrega, como módulos de sala de aula virtual, esses módulos continuam a funcionar independentemente do requisito do navegador do exame seguro.

Este artigo explica como adicionar um questionário ativado pelo navegador do Safe Exam a um curso e definir suas configurações para o curso.

## Criar um quiz com o modo Navegador de exame seguro

O modo Navegador do exame seguro determina se os alunos devem usar o Navegador do exame seguro para fazer o quiz. A opção aparece somente depois que um administrador ativa a integração do navegador do Safe Exam para a conta. Exiba **Habilitar o navegador Safe Exam** para obter mais informações.

Para criar um quiz com o modo Navegador do Safe Exam:

1. Faça logon no ALM como autor.
1. Selecione **Criar Conteúdo**.

   A página **Biblioteca de Conteúdo** é exibida.

1. Selecione **Adicionar** > **Quiz**.

   A página **Criar quiz** é aberta.

1. Insira um nome para o quiz no campo **Nome**.
1. (Opcional) Insira uma descrição para o quiz no campo Descrição.
1. Selecione **Adicionar pergunta do quiz** e adicione os **Critérios de aprovação**.
1. Habilitar **modo Navegador de Exame Seguro**. A opção **Permitir que o autor personalize enquanto cria o curso** é exibida.

   ![Configuração do modo Navegador de Exame Seguro na página Criar Quiz](assets/quiz-safe-exam-browser-mode-setting.png "configuração do modo Navegador de Exame Seguro na página Criar Quiz")

1. (Opcional) Habilitar **Permitir que o autor personalize durante a criação do curso**.

   A opção Navegador de exame seguro aparece quando você configura o código do curso.

   >[!NOTE]
   >
   > Se o administrador ativar essa opção, você poderá ativar ou desativar o requisito do Navegador de exame seguro (SEB) para um módulo de questionário do curso. Se o administrador desabilitar essa opção, o SEB se tornará obrigatório para o quiz e você não poderá alterar esse requisito.

1. Selecione **Publish**.

## Adicionar um questionário ativado pelo navegador do Safe Exam a um curso

Adicione o questionário como um módulo em ritmo individualizado para exigir o Navegador de exames seguro para essa avaliação. Antes de começar, certifique-se de que o quiz seja publicado com o Navegador de exame seguro ativado. Ver Ativar Navegador de Exame Seguro para mais informações.

Para adicionar o quiz a um curso:

1. Selecione **Criar curso** e insira o nome e a descrição do curso.
1. Selecione **Adicionar Módulos** na página **Módulos**.

   O pop-up Módulos é exibido.

1. Selecione **Aprendizado em ritmo individualizado**. A caixa de diálogo **Módulo de ritmo individualizado** é aberta.

   ![Caixa de diálogo do módulo de ritmo individualizado listando os módulos de questionário disponíveis](assets/self-paced-module-dialog-quiz-selection.png "Caixa de diálogo do módulo de ritmo individualizado listando os módulos de questionário disponíveis")

1. Marque a caixa de seleção ao lado do quiz do navegador do Safe Exam que você criou.
1. Selecione **Adicionar**. O questionário é adicionado ao curso como um módulo em ritmo individualizado.
1. (Opcional) Para adicionar outro tipo de entrega ao curso, selecione **Adicionar Mais Tipos de Entrega** e configure o módulo necessário.
1. Selecione **Salvar** > **Publish**.

   O curso agora inclui uma avaliação que exige que os alunos usem o navegador seguro do exame.
