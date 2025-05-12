---
description: Saiba como configurar o idioma da interface com SAML
jcr-language: en_us
title: Configurar o idioma da interface por meio do SAML
contentowner: chandrum
exl-id: 726cb45e-1c37-42b1-924a-565c84c82852
source-git-commit: 7b84a4565ccf109ed4789f4963d6e250f5d0a852
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Configurar o idioma da interface por meio do SAML

O Adobe Learning Manager (ALM) agora aceita um atributo SAML para o idioma. Esse atributo é mapeado para a interface do usuário e as configurações de idioma do conteúdo, garantindo uma interação tranquila com o LMS no idioma de sua preferência. A configuração dessas configurações de idioma é gerenciada por meio da plataforma IAM (Identity and Access Management), que utiliza SAML para logon único (SSO). Isso oferece suporte tanto a logons iniciados por provedor de serviços (SP) quanto a logons iniciados por provedor de identidade (IdP), permitindo que os usuários vejam a interface e o conteúdo em seu idioma escolhido. O fluxo de trabalho é o seguinte:

1. Criar aplicativo no Okta
2. Adicionar um usuário na Okta
3. Configurar SSO no ALM

## Criar aplicativo no Okta

Para criar um aplicativo no Okta, siga estas etapas:

1. Crie uma conta de desenvolvedor na Okta usando o email da sua empresa e faça logon na sua conta.
2. Selecione **[!UICONTROL Aplicativos]** > **[!UICONTROL Criar Integração de Aplicativos]**.
3. Selecione **[!UICONTROL SAML 2.0]** e **[!UICONTROL Próximo]**.
4. Digite um nome para o aplicativo e selecione Próximo.
5. Configure os seguintes campos:

   * **[!UICONTROL URL de Logon Único]**: digite a URL de domínio específica à qual deseja vincular o aplicativo (por exemplo, [https://learningmanagerstage.adobe.com/saml/SSO](https://learningmanagerstage.adobe.com/saml/SSO)). Altere o URL do ambiente, se necessário.
   * **[!UICONTROL URI do público-alvo (ID da entidade da controladora de armazenamento)]**: use a mesma URL de ambiente acima.
   * **[!UICONTROL Formato de ID de Nome]**: selecione o endereço de email.
   * **[!UICONTROL Nome de Usuário do Aplicativo]**: selecione o nome de usuário do Okta.

6. Em Instruções de Atributo, adicione o seguinte (ou campos adicionais conforme necessário):
   * **Nome**: localidade
   * **Formato de Nome**: Indefinido
   * **Valor**: user.locale

7. Selecione Próximo e selecione Concluir.
8. Depois de concluído, role até Certificados de assinatura SAML:

   * Localize a linha onde o status é **[!UICONTROL Ativo]**.
   * Selecione **[!UICONTROL Ações]** > **[!UICONTROL Exibir Metadados de IdP]**.
   * Isso abrirá um arquivo XML em uma nova guia. Copie o código XML e salve-o como um arquivo .xml localmente.

## Adicionar um usuário na Okta

Para criar um usuário na Okta, siga estas etapas:

1. Selecione **[!UICONTROL Diretório]** > **[!UICONTROL Pessoas]** e selecione **[!UICONTROL Adicionar Pessoa]**.
2. Digite os detalhes necessários para o usuário e selecione **[!UICONTROL Salvar]**.
3. Pesquise e selecione o novo nome de usuário.
4. Selecione **[!UICONTROL Atribuir Aplicativo]**.
5. Selecione o aplicativo criado anteriormente e selecione **[!UICONTROL Salvar]**.
6. Navegue até o perfil do usuário e selecione **[!UICONTROL Editar]**.
7. No campo de localidade, digite o valor necessário (por exemplo, fr_FR, en_US) e selecione **[!UICONTROL Salvar]**.

## Configurar SSO no ALM

Para configurar o SSO no ALM, siga estas etapas:

1. Faça logon como administrador.
2. Selecione **[!UICONTROL Configurações]** > **[!UICONTROL Métodos de Logon]**.
3. Vá para a guia Configuração de **[!UICONTROL Logon Único (SSO)]**.
4. Selecione **[!UICONTROL Adicionar nova configuração de SSO]**.

   ![](assets/sso-add.PNG)
   _Adicionar sso no ALM_

5. Configure os seguintes detalhes e selecione Salvar.
   * Digite um nome para a configuração.
   * Selecione **[!UICONTROL IDP iniciado]** no menu suspenso **[!UICONTROL Configurações de logon único (SSO)]**.
   * Para **[!UICONTROL URL de Autenticação Iniciada por IDP]**:

      * Abra o arquivo XML de metadados baixado anteriormente.
      * Procure o valor do local e copie-o.
      * Cole esse valor no campo URL de autenticação iniciada pelo IDP.

   * Para **[!UICONTROL Arquivo XML de Metadados]**: faça upload do arquivo .xml que você baixou anteriormente.

6. Volte para a guia **[!UICONTROL Configuração]**.
7. Na lista suspensa, selecione **[!UICONTROL Configuração de Logon Único]**.
8. No menu suspenso **[!UICONTROL Configuração de SSO]**, selecione o nome de configuração criado anteriormente.
9. Selecione **[!UICONTROL Salvar]**.

## Configuração de logon e idioma do usuário

Quando um usuário faz logon usando as credenciais por meio de SSO, o atributo de idioma passado do IDP é mapeado para a interface do usuário e os campos de idioma de conteúdo no ALM. As configurações de idioma são refletidas imediatamente na interface do usuário e no conteúdo, sem nenhum tempo de armazenamento em cache.

Os usuários podem atualizar manualmente suas configurações de idioma na seção perfil de usuário. Essas preferências de idioma atualizadas manualmente permanecerão em vigor e não serão substituídas pelas configurações do IDP durante logons futuros.

Se um usuário for excluído por software do ALM, as configurações de idioma serão mantidas no banco de dados. Quando o mesmo usuário for adicionado novamente, o idioma definido anteriormente será restaurado.

Os administradores podem verificar os relatórios de Atividade do usuário, Resumo do aprendizado e Painel de conformidade para obter detalhes específicos do idioma.

## Atualização da preferência de idioma do usuário ao fazer logon por SAML

O Adobe Learning Manager é uma plataforma multilíngue que oferece suporte às preferências de idioma dos alunos de várias maneiras, por meio da interface, do conteúdo e dos módulos do curso, todos disponíveis em vários idiomas.

Com esse aprimoramento, o Adobe Learning Manager aprimora o provisionamento de usuários just-in-time para usuários de plataforma nativa. Quando novos usuários criam contas e fazem logon pela primeira vez, suas preferências de idioma são capturadas com precisão e aplicadas automaticamente.

### Principais benefícios

* Atualiza automaticamente as preferências de idioma dos usuários durante o logon.
* Fornece uma experiência personalizada ao exibir a interface e o conteúdo no idioma preferido do usuário.
* Integra-se perfeitamente ao processo de autenticação SAML.

Quando os usuários fazem logon por SAML, sua preferência de idioma (idioma da interface e do conteúdo) é verificada e atualizada com base nas informações fornecidas durante o processo de logon.

O recurso se integra ao processo de logon por SAML para capturar e atualizar a preferência de idioma do usuário sem problemas.
