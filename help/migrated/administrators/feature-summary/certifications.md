---
description: Saiba como criar certificações, inscrever alunos e editar certificações publicadas.
jcr-language: en_us
title: Certificações
contentowner: manochan
exl-id: 406d1c33-aac3-47e1-9b32-83874976ce54
source-git-commit: 69ef7d1e27fac3db49cbb4b9f9403f74e146efb5
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 67%

---

# Certificações

Saiba como criar certificações, inscrever alunos e editar certificações publicadas.

Certifique seus alunos de uma só vez ou em um intervalo de tempo periódico utilizando esse recurso. Somente os administradores podem definir as certificações dos alunos.

Como administrador, você pode criar um programa de certificação hospedado internamente ou conduzido por terceiros. No caso de certificações internas, defina os cursos que um aluno deve concluir para obter a certificação. Publique o programa e atribua-o aos alunos.

## Criar uma certificação {#createacertification}

1. Clique em **[!UICONTROL Certificação]** no painel esquerdo.\
   É exibida uma página com uma lista de certificações nos estados de rascunho e publicado.

1. Veja as certificações em vários modos:

   1. Clique em **[!UICONTROL Rascunho]** para ver todas as certificações no estado de rascunho. Você precisa terminar de criá-los.
   1. Clique em **[!UICONTROL Publicado]** para ver todas as certificações publicadas por você.
   1. Clique em **[!UICONTROL Tudo]** para exibir as certificações em todos os estados.
   1. Classifique e exiba a lista de certificações em ordem crescente ou decrescente ou com base na data em que foram atualizadas.

1. Clique em **[!UICONTROL Adicionar]**.

   A página de uma nova certificação é exibida.

![](assets/add-new-certification.png)

*Exibir a página para adicionar uma certificação*

1. Adicione nome e descrição do certificado.

<table>
 <tbody>
  <tr>
   <th>Campo</th>
   <th>Descrição</th>
  </tr>
  <tr>
   <td>Dias restantes para a conclusão</td>
   <td>O prazo para a certificação. Digite um valor numérico.</td>
  </tr>
  <tr>
   <td>Tipo</td>
   <td>
    <p>O tipo de certificação:</p>
    <ul>
     <li><b>Periódica</b>- Escolha essa opção se a certificação tiver de ser realizada anualmente ou a cada dois ou três anos.</li>
     <li><b>Permanente</b>- Escolha essa opção se for necessário realizar a certificação uma única vez.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Reatribuição</td>
   <td>Escolha se deseja que o certificado seja reatribuído com base na data de conclusão ou na data de inscrição.<br></td>
  </tr>
  <tr>
   <td>Validade (em meses) <br></td>
   <td>Especifique por quanto tempo a certificação pode permanecer válida.</td>
  </tr>
  <tr>
   <td>Sequenciamento de cursos<br></td>
   <td>Decida se os alunos devem fazer os cursos seguindo ou não uma ordem.<br></td>
  </tr>
  <tr>
   <td>Cancelamento da inscrição<br></td>
   <td>Ative ou desative a opção para permitir que os alunos cancelem suas inscrições.</td>
  </tr>
  <tr>
   <td>Emissor da certificação<br></td>
   <td>
    <p>Escolher <b>Interno</b> se pertencer à sua organização ou escolha <b>Externo</b> para certificações de fora da organização.</p>
    <p>Ao escolher <b>Certificação externa</b>, você verá mais duas opções:</p>
    <ul>
     <li>Igual à data de aprovação<br></li>
     <li>Enviado pelo aluno<br></li>
    </ul>
    <p>Os alunos podem especificar a data de conclusão correta das certificações externas. Nas versões anteriores, a data de conclusão era definida por padrão pelo Prime, com base na data de aprovação do gerente. A data de conclusão fornecida pelo aluno deve ser maior que a data de criação do certificado<span>.</span></p></td>
  </tr>
  <tr>
   <td>Duração</td>
   <td>Se escolheu a Certificação externa, então especifique a duração em minutos.</td>
  </tr>
  <tr>
   <td>Tags</td>
   <td>Insira as marcas que deseja associar ao certificado. As marcas são úteis quando você deseja procurar o certificado.</td>
  </tr>
  <tr>
   <td>Selecionar catálogos<br></td>
   <td>Escolha o catálogo do qual o certificado faz parte.</td>
  </tr>
 </tbody>
</table>

Selecione o nível de produtos, funções e funções na **[!UICONTROL Recomendar para]** para sugerir esse caminho de aprendizado aos usuários que expressaram interesse nesses produtos e funções.

![](assets/recommend-for.png)

*Recomendação*

Escolha os cursos a serem adicionados à certificação de **[!UICONTROL Cursos]** > **[!UICONTROL Catálogo]** guia.

Passe o mouse sobre cada quadro do curso, clique em + para adicioná-los à certificação. Clique em **[!UICONTROL Visualizar]** para exibir o curso como aluno antes de adicioná-lo.

1. Clique em **[!UICONTROL Currículo]** para exibir/verificar a lista de cursos adicionados.
1. Clique em **[!UICONTROL Publicar]**.

## Mapeamento de instâncias do curso para certificações {#courseinstancemappingforcertifications}

Para mapear o curso e a instância para certificações:

1. Clique em Certificações no painel esquerdo.
1. Na lista de certificações, selecione a opção Exibir certificação da certificação para a qual deseja mapear o curso e a instância.
1. No painel esquerdo, clique em Cursos. São exibidos os cursos da certificação. Clique em Editar.
1. Passe o mouse sobre o curso para o qual deseja definir o mapeamento de instância e selecione Mapeamento de instância do curso.
1. Na janela pop-up exibida, selecione a instância do curso que será fornecida para a certificação escolhida.
1. Clique em Salvar.

Um administrador pode adicionar cursos de tipo de sala de aula virtual e sala de aula a um Programa de aprendizado. Qualquer sessão dada pelo autor durante a criação do curso se torna a instância padrão. Quando o administrador adiciona cursos a um programa de aprendizado, ele é mapeado, por padrão, para a instância padrão de todos os cursos, mas o administrador pode alterar o mapeamento da instância. O número de cursos adicionados a um programa de aprendizado também é visível na página de instâncias, conforme mostrado abaixo.

## Ativar controle total do catálogo {#catalog}

Assim como concede controle total [do catálogo de aprendizados ou módulos](shared-catalog-full-control.md), você também pode ativar o controle total do catálogo dos programas de aprendizado.

## Inscrever ou cancelar a inscrição dos alunos na certificação {#enrollorunenrolllearnerstothecertification}

Para obter mais informações sobre como inscrever alunos e as etapas a seguir, consulte [Inscrição de alunos](courses.md#main-pars_header_1058138132).

## Cancelar as inscrições dos alunos {#unenrollmentforlearners}

Ao criar certificações, o administrador tem a opção de selecionar se os alunos podem cancelar a inscrição nos programas de aprendizado. Se o administrador seleciona a opção, então o aluno pode cancelar a inscrição.

![](assets/unenrollment.png)

*Escolha para cancelar a inscrição dos alunos*

## Marcar conclusão {#markcompletion}

Os administradores podem marcar uma certificação como concluída usando a opção disponível para eles. Para marcar a conclusão de uma certificação, siga estas etapas.

1. Abrir **[!UICONTROL Certificação]** > **[!UICONTROL Alunos]**.

   A página Alunos é aberta com a lista de alunos inscritos.

1. Selecione um, vários ou todos os alunos para marcar a conclusão da certificação usando a caixa de seleção disponível para cada aluno.
1. Clique em  **[!UICONTROL Ação]** > **[!UICONTROL Marcar conclusão.]**

   Observe que, se uma certificação tiver vários cursos, a conclusão será marcada para todos os cursos.

## Cursos obrigatórios para certificação externa {#mandatory}

Nas versões anteriores do Learning Manager, para os alunos em uma certificação externa, não era obrigatória a conclusão do curso para completar um certificado.

Agora, é possível fazer cursos obrigatórios ativando a opção **[!UICONTROL Definir cursos necessários como obrigatórios para a conclusão do certificado]** na guia Currículo ao editar a certificação.

## Edição de uma certificação publicada {#editingapublishedcertification}

Um administrador pode editar uma certificação no estado publicado. Nesse estado, o administrador pode editar todas as seções de uma certificação e republicá-la.

Para editar uma certificação publicada, clique no cartão de certificação e clique em **[!UICONTROL Editar]** no canto superior direito da página.

Ao editar as seções de uma certificação, se for necessário sair da página, será necessário republicar a certificação. É exibida uma caixa de diálogo de confirmação que solicitará que a certificação seja publicada novamente.

![](assets/edit-a-certificate.png)

*Editar um certificado*

## Assinatura {#subscription}

Os administradores podem obter relatórios de pontuação do questionário e de status do aluno. Eles podem definir a frequência do relatório, o assunto do e-mail e a ID de e-mail dos destinatários. Dependendo da frequência definida, o destinatário receberá um e-mail com o relatório anexado.

![](assets/report-subscription.jpeg)

*Definir a frequência do relatório e outras propriedades*
