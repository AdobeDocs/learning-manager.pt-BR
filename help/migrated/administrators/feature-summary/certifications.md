---
description: Saiba como criar certificações, inscrever alunos e editar certificações publicadas.
jcr-language: en_us
title: Certificações
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 0%

---



# Certificações

Saiba como criar certificações, inscrever alunos e editar certificações publicadas.

Certifique os alunos apenas uma vez ou em um intervalo de tempo recorrente usando esse recurso. Somente os administradores podem definir as certificações para os alunos.

Como administrador, você pode criar um programa de certificação hospedado internamente ou conduzido por terceiros. No caso da certificação interna, defina os cursos que um aluno deve concluir para obter a certificação. Publique o programa e atribua-o aos alunos.

## Criar uma certificação {#createacertification}

1. Clique em **[!UICONTROL Certificação]** no painel esquerdo.\
   É exibida uma página com uma lista de certificações nos estados de rascunho e publicado.

1. Veja as certificações em vários modos:

   1. Clique em **[!UICONTROL Rascunho]** para ver todas as certificações no estado de rascunho. Você precisa concluir a criação deles.
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
   <td>Dias para concluir</td>
   <td>O prazo para a certificação. Insira um valor numérico.</td>
  </tr>
  <tr>
   <td>Tipo</td>
   <td>
    <p>O tipo de certificação:</p>
    <ul>
     <li><b>Recorrente</b>- Escolha essa opção se a certificação tiver de ser realizada anualmente ou a cada dois ou três anos.</li>
     <li><b>Perpétuo</b>- Escolha essa opção se for necessário realizar a certificação uma única vez.</li>
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
   <td>Cancelar inscrição<br></td>
   <td>Ative ou desative a opção para permitir que os alunos cancelem suas inscrições.</td>
  </tr>
  <tr>
   <td>Emissor da certificação<br></td>
   <td>
    <p>Escolher <b>Interno</b> se pertencer à sua organização ou escolha <b>Externo</b> para certificações de fora da organização.</p>
    <p>Ao escolher <b>Certificação externa</b>, você verá mais duas opções-</p>
    <ul>
     <li>Igual à Data Aprovada<br></li>
     <li>Enviado pelo aluno<br></li>
    </ul>
    <p>Os alunos podem especificar a data de conclusão correta para certificações externas. Nas versões anteriores, a data de conclusão era definida por padrão pelo Prime, com base na data de aprovação do gerente. A data de conclusão fornecida pelo aluno deve ser maior que a data de criação do certificado<span>.</span></p></td>
  </tr>
  <tr>
   <td>Duração</td>
   <td>Se escolheu a Certificação externa, então especifique a duração em minutos.</td>
  </tr>
  <tr>
   <td>Tags</td>
   <td>Insira as tags que deseja associar ao certificado. As marcas são úteis quando você deseja procurar o certificado.</td>
  </tr>
  <tr>
   <td>Selecionar catálogos<br></td>
   <td>Escolha o catálogo do qual o certificado faz parte.</td>
  </tr>
 </tbody>
</table>

Escolha os cursos a serem adicionados à certificação de **[!UICONTROL Cursos]** > **[!UICONTROL Catálogo]** guia.

Passe o mouse sobre cada quadro do curso, clique em + para adicioná-los à certificação. Clique em **[!UICONTROL Visualizar]** para exibir o curso como aluno antes de adicioná-lo.

1. Clique em **[!UICONTROL Currículo]** para exibir/verificar a lista de cursos adicionados.
1. Clique em **[!UICONTROL Publicar]**.

## Mapeamento de instância de curso para certificações {#courseinstancemappingforcertifications}

Para mapear o curso e a instância para certificações:

1. Clique em Certificações no painel esquerdo.
1. Na lista de certificações, selecione Exibir certificação da certificação em que você deseja mapear o curso e a instância.
1. No painel esquerdo, clique em Cursos. Os cursos para a certificação são exibidos. Clique em Editar.
1. Passe o mouse sobre o curso onde deseja definir o mapeamento de instância, selecione Mapeamento de instância de curso.
1. Na janela pop-up exibida, selecione a instância do curso que deve ser entregue para a certificação escolhida.
1. Clique em Salvar.

Um administrador pode adicionar cursos de tipo de sala de aula virtual e sala de aula a um Programa de aprendizado. Qualquer sessão que o autor tenha dado durante a criação do curso se torna a instância padrão. Quando o administrador adiciona cursos a um programa de aprendizado, por padrão, ele é mapeado para a instância padrão de todos os cursos, mas o administrador pode alterar o mapeamento de instância. O número de cursos adicionados a um programa de aprendizado também é visível na página de instâncias, conforme mostrado abaixo.

## Ativar controle total do catálogo {#catalog}

Como conceder acesso total [controle do catálogo de aprendizados ou módulos](shared-catalog-full-control.md), você também pode ativar o controle total do catálogo para certificações.

## Inscrever ou cancelar a inscrição dos alunos na certificação {#enrollorunenrolllearnerstothecertification}

Para obter mais informações sobre como inscrever alunos e as etapas a seguir, consulte [Inscrição de alunos](courses.md#main-pars_header_1058138132).

## Cancelar inscrição dos alunos {#unenrollmentforlearners}

Ao criar certificações, o administrador tem a opção de selecionar se os alunos podem cancelar suas inscrições na certificação. Se o administrador selecionar a opção, o aluno poderá cancelar a inscrição.

![](assets/unenrollment.png)

*Escolha para cancelar a inscrição dos alunos*

## Marcar conclusão {#markcompletion}

Os administradores podem marcar uma certificação como concluída usando a opção disponível para eles. Para marcar a conclusão de uma certificação, use as etapas a seguir.

1. Abrir **[!UICONTROL Certificação]** > **[!UICONTROL Alunos]**.

   A página Alunos é aberta com a lista de alunos inscritos.

1. Selecione um, vários ou todos os alunos para marcar a conclusão da certificação usando a caixa de seleção disponível para cada aluno.
1. Clique em  **[!UICONTROL Ação]** > **[!UICONTROL Marcar conclusão.]**

   Observe que, se uma certificação tiver vários cursos, a conclusão será marcada para todos os cursos.

## Cursos obrigatórios para certificação externa {#mandatory}

Nas versões anteriores do Learning Manager, para que um certificado fosse concluído, não era obrigatória a conclusão do curso do aluno na certificação externa.

Agora, é possível fazer cursos obrigatórios ativando a opção **[!UICONTROL Definir cursos necessários como obrigatórios para a conclusão do certificado]** na guia Currículo ao editar a certificação.

## Editar uma certificação publicada {#editingapublishedcertification}

Uma certificação pode ser editada por um administrador em um estado publicado. Nesse estado, o administrador pode editar todas as seções de uma certificação e publicá-las novamente.

Para editar uma certificação publicada, clique no cartão de certificação e clique em **[!UICONTROL Editar]** no canto superior direito da página.

Ao editar as seções de uma certificação, se for necessário sair da página, você precisará republicar a certificação. Você obtém uma caixa de diálogo de confirmação solicitando que você republique a certificação.

## Assinatura {#subscription}

Um administrador pode obter a pontuação do questionário e os relatórios de status do aluno. Eles podem definir a frequência do relatório, o assunto do e-mail e a ID de e-mail dos destinatários. Dependendo da frequência definida, o destinatário receberá um email com o relatório anexado.

![](assets/report-subscription.jpeg)

*Definir a frequência do relatório e outras propriedades*
