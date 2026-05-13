---
description: Saiba como integrar o conector do Adobe Connect com o Adobe Learning Manager
jcr-language: en_us
title: Conector do Adobe Connect
contentowner: mmanuel
source-git-commit: 8a5212062c6b172b0e9d4f3faa2e66d26c5c2b56
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 2%

---


# Conector do Adobe Connect no Adobe Learning Manager

## Introdução

O Adobe Learning Manager integra-se ao Adobe Connect para ajudar você a oferecer e gerenciar treinamento em sala de aula virtual. Com essa integração, você pode agendar sessões, usar salas de reunião persistentes ou dinâmicas, capturar participação, importar resultados do quiz e fornecer aos alunos gravações de sessão.

## Configurar o Adobe Connect

Para configurar o Adobe Connect:

1. Faça logon no Adobe Learning Manager como administrador de integração.
2. Passe o mouse sobre o bloco **Adobe Connect** e selecione **Conectar**.

   ![](assets/adobe-connect-connector1.png)
   _Selecione Conectar para configurar o Conector do Adobe Connect_

3. Digite os seguintes detalhes:

   - **Nome da Conexão**
   - **URL do Adobe Connect**
   - **Conectar Email Do Administrador**
4. Digite a **ID de logon do administrador do Connect** (obrigatório se o logon por email do Adobe Connect não for usado).

   ![](assets/adobe-connect-connector2.png)
   _Digite os detalhes necessários para a configuração do Adobe Connect_

5. Selecione **Habilitar autenticação do Connect**.

   >[!NOTE]
   >
   >Só há suporte para contas do Connect hospedadas por Adobe. (O domínio deve terminar com .adobeconnect.com)

6. Selecione **Conectar**.

Depois de autenticar a ID de e-mail do administrador:

- O Adobe Learning Manager exibe uma mensagem de sucesso confirmando que o Connect está integrado.
- A solicitação é encaminhada à equipe de back-end do Adobe Connect para aprovação. Isso geralmente leva de um a dois dias.

>[!IMPORTANT]
>
>O administrador da conta do Adobe Connect deve aceitar os Termos e condições ao fazer logon pela primeira vez. Se isso não for feito, a autenticação do logon poderá falhar.

## Adicionar informações da sessão da sala de aula virtual

Se um autor não tiver fornecido detalhes da sessão para um curso em sala de aula virtual, o administrador poderá adicioná-los:

1. Faça logon como administrador.
2. Selecione o curso de SV.
3. Selecione **Instâncias** e selecione **Detalhes da Sessão**.
4. Selecione o ícone **Editar** para adicionar ou atualizar informações da sessão.

>[!NOTE]
>
>Sua conta do Connect deve ter salas de reunião e capacidade suficientes para que os usuários simultâneos executem salas de aula virtuais. Cada sessão de sala de aula virtual do Adobe Learning Manager cria automaticamente uma nova sala de reunião do Connect, a menos que você use uma sala de aula contínua.

## Salas de reunião persistentes

O Adobe Connect oferece suporte a salas de reunião permanentes, que permanecem disponíveis para reutilização.

- Você pode criar uma sessão de sala de aula virtual usando uma sala persistente existente no Connect.
- Em vez disso, você também pode optar por fazer com que o Adobe Learning Manager crie uma sala dinâmica para cada sessão.

Quando os alunos participam de uma sessão usando o Adobe Connect, eles entram na sala por meio do Learning Manager usando autenticação segura.

Após concluírem uma sessão, os alunos podem acessar a gravação e a senha da sessão no aplicativo Learning Manager.

## Importar pontuações do questionário do Adobe Connect

O Adobe Learning Manager pode importar dados do quiz das sessões do Adobe Connect e combiná-los com outros fluxos de trabalho de relatórios. Isso inclui pontuações do quiz, respostas do aluno e dados de conclusão, como o funcionamento dos módulos em ritmo individualizado.

### Fluxo de trabalho de importação do quiz

#### Adobe Connect (host)

- O host do Connect cria um curso e carrega conteúdo que inclui um questionário interativo.
- O host configura um treinamento em sala de aula virtual (SV) e vincula o curso ao VC ou usa a opção **Compartilhar curso** para compartilhá-lo durante a sessão.

#### Adobe Learning Manager (Autor)

- O autor cria um curso no Adobe Learning Manager com o tipo de módulo definido como **Sala de aula virtual**.
- Na lista suspensa **Sistema de Conferência**, selecione **Conectar** como provedor de sala de aula virtual.
- Escolha a **Sala de Reunião Persistente** criada pelo host no Connect.
- Atribua um professor, salve e publique o curso.

#### Adobe Learning Manager (Aluno)

- O aluno se inscreve no curso e ingressa na sessão Connect VC.
- O host do Connect permite que o aluno acesse a sessão.

### Adobe Connect (host e aluno)

- O host compartilha o questionário na sessão.
- O aluno conclui o quiz e sai da sessão.

### Adobe Learning Manager (Sincronização e administração)

- Quando a sessão terminar, o Adobe Learning Manager sincronizará automaticamente os dados do quiz.
- O fluxo de trabalho de importação do quiz é iniciado após o término da duração agendada.
- Para acompanhar o progresso, o administrador de integração pode verificar o **Status de execução** no conector do Adobe Connect.
- Após a conclusão da importação, o status é atualizado para **Concluído**.

O administrador pode revisar os resultados importados:

- **Presença e pontuação:** veja as pontuações e a participação finais no quiz.
- **Pontuação do quiz L2:**
   - **Por Usuário:** mostra pontuações individuais em pontos e percentuais.
   - **Por pergunta:** exibe os resultados do quiz em um gráfico de relatório.
