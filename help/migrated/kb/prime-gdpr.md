---
jcr-language: en_us
title: Conformidade do Learning Manager com o GDPR
description: Conformidade do Adobe Learning Manager com o GDPR
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '581'
ht-degree: 0%

---



# Conformidade do Learning Manager com o GDPR

>[!IMPORTANT]
>
>O conteúdo deste documento não é um conselho legal e não tem a intenção de ser um substituto para o conselho legal. Consulte o departamento jurídico de sua empresa para obter o conselho relativo ao GDPR.

+++O que é o GDPR?

O GDPR é um novo regulamento da União Europeia que entra em vigor em 25 de maio de 2018. Ele fornece um forte controle para a privacidade dos dados e permite que os usuários se encarreguem de seus próprios dados pessoais.

+++

+++Como ou Por que ele se aplica à você como um cliente do Adobe Learning Manager?

Embora o GDPR seja um regulamento da UE, ele é aplicável a entidades comerciais em todo o mundo, que coleta informações pessoais de qualquer usuário que possa ser residente da UE.  Como um cliente do Learning Manager, avalie se o GDPR é aplicável à sua organização.

+++

+++Qual o papel do Adobe nisso como um fornecedor do Learning Manager?

De acordo com o GDPR, se a sua empresa fornece um produto ou serviço para residentes da UE, e se determina como e porque coleta, rastreia e monitora seus dados, você é considerado um [controlador de dados](https://gdpr-info.eu/art-24-gdpr/). Como um cliente do Adobe Learning Manager, se você executa uma dessas atividades, é considerado como um controlador de dados.

As empresas que processam dados em nome de controladores são consideradas  [processadores de dados](https://gdpr-info.eu/art-28-gdpr/). Como um fornecedor do Adobe LMS Learning Manager hospedado na nuvem, o Adobe desempenha a função de processador de dados. Veja a seguir mais detalhes sobre  [GDPR e sua empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

+++

+++Como o Learning Manager permite que você esteja em conformidade com o GDPR?

O Learning Manager tem incorporado as seguintes ferramentas e processos que o ajudarão na conformidade com o GDPR. Para suportar quaisquer processos que vão além do fato do produto estar em total conformidade com o regulamento, talvez ainda seja necessário avaliar isso com a equipe de conformidade.

**Direito de Esquecer - Alcançando o Controlador de Dados:** O GDPR requer que os controladores de dados suportem a funcionalidade Direito de Esquecer para seus usuários. Isso significa que qualquer usuário tem o direito de solicitar que o controlador de dados exclua permanentemente quaisquer Dados pessoais armazenados para esse usuário. Se você receber tal solicitação e depois avaliar que é uma solicitação válida, esta funcionalidade é agora fornecida no Learning Manager através de sua [Remover usuários](../administrators/feature-summary/purge-users.md) funcionalidade. Esse recurso permite que o administrador inicie uma exclusão permanente de quaisquer dados relacionados a um indivíduo específico, mediante solicitação do indivíduo, momento em que o Learning Manager excluirá instantaneamente os dados de seu banco de dados e uma limpeza dos registros de backup (destinados à recuperação do sistema) também seguirá automaticamente.

**Direito de Esquecer - Alcançando o Processador de Dados:** O usuário final também pode entrar em contato com o Adobe de forma independente para excluir seu PII. Nesse caso, o Learning Manager detectará automaticamente quais contas têm a propriedade do PII para esse usuário e o Adobe notificará o administrador imediatamente de tal solicitação. O administrador pode avaliar a validade da solicitação e receber uma chamada pela solicitação por meio do recurso Remover usuários.

**Direito de acesso:** O GDPR concede ao usuário final o direito de solicitar dados que um controlador pode ter armazenado para esse usuário final. Para suportar essa solicitação, o Learning Manager permite que o administrador gere sozinho a transcrição do aluno que pode ser compartilhada com o usuário.

**Privacidade por Design, Criptografia de Dados:** Processamos os dados em trânsito e estacionários usando os melhores padrões de criptografia do setor para garantir a segurança dos dados. Os algoritmos de criptografia usados são SHA-256. Isso garante que todos os dados que você armazena estejam adequadamente protegidos para que não caiam em mãos erradas.

+++

