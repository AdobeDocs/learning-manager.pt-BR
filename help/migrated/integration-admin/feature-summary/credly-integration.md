---
jcr-language: en_us
title: Credly
description: Saiba mais sobre a integração de credenciais com o ALM para gerenciar e compartilhar medalhas externas da plataforma em vários canais de redes sociais
contentowner: chandrum
source-git-commit: a27c1566678d697512a75d94804b8804b5dc9b2b
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# Credly

A [Credibilidade](https://info.credly.com/) é uma plataforma de credencial digital que permite que alunos e organizações obtenham, compartilhem e verifiquem conquistas profissionais, como medalhas ou certificações. Os alunos podem gerenciar e compartilhar medalhas por meio de seu perfil de credencial nas redes sociais e em outros lugares.

## Pré-requisito

Configure uma Conta de crédito para sua organização. Adicione alunos à Credly usando as IDs de e-mail deles no Adobe Learning Manager. Isso permitirá que os alunos vejam as medalhas na Credly e no Adobe Learning Manager.

## Adicionar o conector de crédito ao Adobe Learning Manager

Siga estas etapas para adicionar o conector de crédito ao Adobe Learning Manager:

1. Faça logon como **[!UICONTROL Administrador de Integração]**.
2. Selecione **[!UICONTROL Credível]** > **Conectar** para adicionar o conector **[!UICONTROL Credível]** ao Adobe Learning Manager.

   ![](assets/connector-credly.png)
   _Adicionar conector de Crédito_

3. Digite o **[!UICONTROL Nome da Conexão]**.
4. Digite a **[!UICONTROL ID da organização]** e o **[!UICONTROL token de autorização]**.

   >[!NOTE]
   >
   >Cada medalha na Credly vem com uma ID da organização e um token de autorização. Copie esses valores de Credly.

5. Digite o **[!UICONTROL Nome do host]** e selecione **[!UICONTROL Conectar]**.

## Migrar medalhas da credencial

O arquivo badge.csv no Adobe Learning Manager permite migrar medalhas do LMS existente ou de sistemas externos. O arquivo badge.csv foi atualizado com duas novas colunas:

* ID da medalha externa
* Provedor de medalha externo.

A ID da medalha externa se refere à ID do modelo de medalha na plataforma Credly, e o provedor de medalha externa é Credly. Adicione esses valores em badge.csv e siga as etapas mencionadas no [Manual de migração](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual#migrationprocedure) para migrar o csv.

## Criar uma habilidade - Administrador

Depois que a medalha for importada para o Adobe Learning Manager, o administrador pode criá-la como uma habilidade. Para saber como criar uma habilidade, consulte [Criar e modificar habilidades](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/skills-levels).

### Atribuir a habilidade/medalha ao objeto de aprendizado - Autor

O autor/administrador pode atribuir essas medalhas ALM importadas por crédito a um curso, caminho de aprendizado ou certificação (não apenas habilidades) e, no consumo desses objetos de aprendizado, a medalha será obtida e pode ser exibida no aplicativo Credly e ALM.

Os alunos podem fazer logon na Credly e ver as medalhas na plataforma Credly. Com a Credly, eles podem compartilhar as medalhas em plataformas externas, como o LinkedIn e outras mídias sociais.

