---
description: Uma visão geral sobre cada conector compatível com ALM
jcr-language: en_us
title: Visão geral dos conectores compatíveis com ALM
contentowner: mmanuel
source-git-commit: bd80ca31ff633e21ec81e717772e43989f0d9aae
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 6%

---


# Conectores do Adobe Learning Manager

## Introdução

O Adobe Learning Manager (ALM) fornece um conjunto abrangente de conectores que permitem integração perfeita com aplicativos de terceiros e sistemas empresariais. Esses conectores funcionam como pontes entre seu sistema de gerenciamento de aprendizagem e plataformas externas, facilitando a sincronização automatizada de dados, o gerenciamento de usuários, a importação de conteúdo e as exportações de registros de aprendizagem.

Este documento serve como um guia de referência completo para entender e selecionar os conectores apropriados para o ecossistema de aprendizado da sua organização. Quer você esteja procurando se integrar a sistemas de RH, plataformas de comércio eletrônico, ferramentas de reuniões virtuais ou soluções de business intelligence.

Para obter uma lista completa de conectores compatíveis com o Adobe Learning Manager, consulte os artigos de conectores aninhados logo abaixo deste artigo no Índice à esquerda.

>[!NOTE]
>
>Este recurso está parcialmente disponível em ambientes autorizados pelo FedRAMP. Consulte [Disponibilidade de recursos em ambientes FedRAMP](/help/migrated/feature-availability-in-fedramp-authorized-environment.md) para obter detalhes.

>[!NOTE]
>
>Com a versão de novembro de 2022 do Adobe Learning Manager, o Zoom descontinuou a autenticação [JWT até junho de 2023](https://developers.zoom.us/docs/internal-apps/s2s-oauth/). Da mesma forma, o conector do Zoom com JWT continuará funcionando até a data mencionada, mas recomendamos que os usuários criem um aplicativo OAuth de servidor para servidor para substituir a funcionalidade na conta dele. Toda nova conexão terá a autenticação OAuth do Zoom por padrão.

## Categorias de conector

Os conectores do Adobe Learning Manager podem ser organizados em várias categorias funcionais com base em seu objetivo principal e recursos de integração:

| Categoria | Finalidade | Exemplo de conectores |
|---------|--------|-------------------|
| Transferência de dados | Troca de dados com base em arquivos e operações em massa | FTP, FTP personalizado, Box |
| Aula virtual | Integração de treinamento e reunião ao vivo | Microsoft Teams, Zoom, Adobe Connect |
| Sistemas corporativos | Integração de sistemas de RH e de negócios | Workday, Salesforce, ADFS |
| Plataformas de conteúdo | Integração externa do conteúdo de aprendizado | LinkedIn Learning, Harvard ManageMentor, getAbstract |
| Análise e BI | Relatórios e visualização de dados | Power BI, Acesso a Dados de Treinamento |
| Autenticação | Gerenciamento de identidade e segurança | AD FS (recursos de SSO) |
| Comércio eletrônico e marketing | Integração de vendas e marketing | Adobe Commerce, Marketo Engage |

## Conectores de transferência de dados e gerenciamento de arquivos

Esses conectores facilitam a troca automatizada de dados por meio de protocolos de transferência de arquivos, permitindo operações em massa e comunicação entre sistemas.

### Conector FTP do Adobe Learning Manager

O conector FTP permite que as organizações automatizem a sincronização de dados entre o Adobe Learning Manager e sistemas externos usando o protocolo de transferência de arquivos, amplamente adotado. Esse conector oferece suporte a variantes seguras, incluindo SFTP (SSH File Transfer Protocol) e FTPS (FTP Secure) para maior segurança.

#### Principais recursos:

- Faça upload e download de arquivos entre a Adobe Learning Manager e servidores remotos.
- Intercâmbio automatizado de dados para informação dos utilizadores e registros de formação.
- Suporte para protocolos de transferência de arquivos seguros (SFTP, FTPS).
- Processamento em lote de grandes conjuntos de dados.

Para obter mais informações, consulte [Conector FTP](/help/migrated/integration-admin/feature-summary/ftp-connector.md).

### Conector FTP personalizado

O conector FTP personalizado fornece recursos de transferência de arquivos mais sofisticados, com suporte a formatos de dados estruturados e trocas de instruções xAPI. Esse conector é projetado para organizações que exigem um controle mais granular sobre seus processos de troca de dados.

#### Principais recursos:

- Importe e exporte dados do usuário por meio de arquivos CSV estruturados.
- Manipular registros de aprendizado e instruções xAPI.
- Processamento automatizado de arquivos a partir de pastas FTP designadas.
- Recursos de segurança aprimorados para transferência de dados confidenciais.

Para obter mais informações, consulte [Conector FTP personalizado](/help/migrated/integration-admin/feature-summary/custom-ftp-connector.md).

### Conector do Box

O conector do Box aproveita a plataforma de armazenamento em nuvem do Box para facilitar a sincronização perfeita de dados entre sistemas externos e o Adobe Learning Manager. Esse conector é útil principalmente para organizações que já usam o Box para gerenciamento de arquivos.

#### Principais recursos:

- Sincronização e armazenamento de arquivos com base na nuvem.
- Processamento automatizado de dados CSV.
- Integração com fluxos de trabalho existentes do Box.
- Atualizações de dados em tempo real de pastas designadas.

Para obter mais informações, consulte o [conector Box](/help/migrated/integration-admin/feature-summary/box-connector.md).

## Conectores de sala de aula virtual e de reunião

Esses conectores integram o Adobe Learning Manager a plataformas populares de videoconferência e reuniões virtuais, permitindo a realização perfeita de sessões de treinamento em tempo real.

### Conector do Microsoft Teams

O conector Microsoft Teams transforma o Adobe Learning Manager em uma solução abrangente de sala de aula virtual, integrando-se diretamente aos recursos de reunião do Teams. Esse conector é essencial para organizações que usam o ecossistema Microsoft 365.

#### Principais recursos:

- Agende sessões de sala de aula virtual diretamente do Adobe Learning Manager.
- Criação e gerenciamento automáticos de reuniões de equipes.
- Acesso contínuo do aluno sem links de reunião separados.

Para mais informações, consulte [Conector do MS Teams](/help/migrated/integration-admin/feature-summary/install-microsoft-teams-connector.md).

### Conector do Zoom

O conector do Zoom permite que as organizações aproveitem os recursos robustos de videoconferência do Zoom diretamente em seu ambiente Adobe Learning Manager, fornecendo uma experiência perfeita para professores e alunos.

#### Principais recursos:

- Agendamento de reunião do Direct Zoom do Adobe Learning Manager.
- Geração e distribuição automatizadas de links de reuniões.
- Monitoramento de participação em tempo real.
- Gerenciamento de gravação e integração de reprodução.
- Suporte a sala de sessão de grupo para sessões interativas.

Para obter mais informações, consulte [Conector de zoom](/help/migrated/integration-admin/feature-summary/zoom-connector.md).

### Conector do Adobe Connect

O conector do Adobe Connect fornece integração profunda com uma plataforma de sala de aula virtual própria, oferecendo recursos avançados para experiências de aprendizado online interativas.

#### Principais recursos:

- Recursos interativos avançados (pesquisas, questionários, breakouts).
- Ferramentas de apresentação e compartilhamento de tela de alta qualidade.
- Gravação e reprodução abrangentes de sessões.
- Experiência de sala de aula virtual otimizada para dispositivos móveis.

Para mais informações, consulte [Conector do Adobe Connect](/help/migrated/integration-admin/feature-summary/adobe-connect-connector.md).

## Conectores de integração de sistema empresarial

Esses conectores permitem que a Adobe Learning Manager se integre com os principais sistemas de negócios, facilitando o gerenciamento automatizado de usuários e a sincronização de dados organizacionais.

### Conector do Workday

O conector do Workday cria uma ponte contínua entre o sistema de RH e a plataforma de gerenciamento de aprendizagem, garantindo que os registros de funcionários, as estruturas organizacionais e as atribuições de função permaneçam sincronizados entre os dois sistemas.

#### Principais recursos:

- Provisionamento automatizado de usuários da Workday.
- Sincronização de dados de funcionários em tempo real.
- Mapeamento da hierarquia organizacional.
- Automação de atribuição de aprendizado baseada em funções.

Para mais informações, consulte [Conector do Workday](/help/migrated/integration-admin/feature-summary/workday-connector.md).

### Conector do Salesforce

O conector do Salesforce permite que as organizações integrem seu sistema de gerenciamento de relacionamento com o cliente com iniciativas de aprendizado, criando oportunidades para treinamento de vendas, treinamento de clientes e acompanhamento de desempenho.

#### Principais recursos:

- Importação automatizada de usuários do Salesforce.
- Mapeamento de campo de dados personalizado.
- Exportação do registro de aprendizado para o Salesforce.
- Correlação entre desempenho de vendas e conclusão do treinamento.
- Gerenciamento do programa de educação do cliente.

Para mais informações, consulte [Conector do Salesforce](/help/migrated/integration-admin/feature-summary/salesforce-connector.md).

### Conector ADFS (Serviços de Federação do Ative Diretory)

O conector do ADFS permite que as organizações implementem autenticação e autorização de nível corporativo, permitindo que os usuários acessem o Adobe Learning Manager usando suas credenciais existentes do Ative Diretory.

#### Principais recursos:

- Implementação de logon único (SSO)
- Conformidade de segurança corporativa
- Autenticação perfeita do usuário
- Importação automatizada de usuário
- Capacidade de agendar
- Capacidade de filtrar

Para obter mais informações, consulte [Conector ADFS](/help/migrated/integration-admin/feature-summary/adfs-connector.md).

## Conectores da plataforma de aprendizado e conteúdo

Esses conectores expandem seu catálogo de aprendizado integrando bibliotecas de conteúdo externo e plataformas de aprendizado especializadas.

### Conector do LinkedIn Learning

O conector de aprendizado do LinkedIn fornece acesso à ampla biblioteca de cursos de desenvolvimento profissional do LinkedIn, permitindo que as organizações complementem seu treinamento interno com conteúdo externo líder no setor.

#### Principais recursos:

- Acesso ao catálogo completo de cursos do LinkedIn Learning.
- Detecção e importação automatizadas de cursos.
- Rastreamento do progresso do aluno no Adobe Learning Manager.

Para mais informações, consulte [Conector do LinkedIn](/help/migrated/integration-admin/feature-summary/linkedin-learning-connector.md).

### Conector do Harvard ManageMentor

O conector Harvard ManageMentor traz conteúdo de treinamento de liderança e gerenciamento de classe mundial diretamente para o seu ambiente Adobe Learning Manager, fornecendo acesso aos renomados recursos educacionais da Harvard Business School.

#### Principais recursos:

- Acesso premium a conteúdo da Harvard Business School.
- Módulos de gerenciamento e desenvolvimento de liderança.
- Importação e organização contínuas de conteúdo.

Para mais informações, consulte [Conector Harvard ManageMentor](/help/migrated/integration-admin/feature-summary/harvard-managementor-connector.md).

### Conector getAbstract

O conector getAbstract fornece acesso a resumos concisos de livros comerciais e insights profissionais, permitindo que as organizações ofereçam aprendizado contínuo por meio de formatos de conteúdo digestíveis.

#### Principais recursos:

- Acesso a resumos e insights de livros de negócios.
- Rastreamento e relatórios de dados de uso.
- Criação automática do registro de conclusão.

Para obter mais informações, consulte [getAbstract connector](/help/migrated/integration-admin/feature-summary/getabstract-connector.md).

## Conectores de Business Intelligence e análise

Esses conectores habilitam recursos avançados de geração de relatórios, visualização de dados e business intelligence integrando dados de aprendizado a plataformas de análise externas.

### Conector do Power BI

O Power BI transforma seus dados de aprendizado em insights de negócios acionáveis sincronizando automaticamente as métricas de aprendizado com a poderosa plataforma de business intelligence da Microsoft.

#### Principais recursos:

- Sincronização de dados de aprendizado em tempo real.
- Criação e gerenciamento de painel personalizado.
- Visualização avançada de dados e relatórios.
- Integração da transcrição do aluno e do relatório de habilidades.

Para obter mais informações, consulte [Conector Powe BI](/help/migrated/integration-admin/feature-summary/power-bi-connector.md).

### Conector de acesso a dados de treinamento

O conector Acesso a dados de treinamento permite que as organizações criem interfaces de aprendizado personalizadas e experiências de aprendizado sem periféricos, fornecendo acesso à API para dados de treinamento e informações do curso.

**Principais recursos:**

- Acesso público da API aos dados do curso e do caminho de aprendizado.
- Suporte ao desenvolvimento da interface de usuário personalizada.
- Criação de experiência de aprendizado sem periféricos.
- Recursos avançados de pesquisa e filtragem.

Para mais informações, consulte [Conector de Acesso a Dados de Treinamento](/help/migrated/integration-admin/feature-summary/training-data-access-connector.md).

## Conectores de comércio eletrônico e marketing

Esses conectores permitem a monetização do conteúdo de aprendizado e a integração com plataformas de automação de marketing.

### Conector do Adobe Commerce

O conector do Adobe Commerce transforma o Adobe Learning Manager em uma plataforma abrangente de comércio de aprendizagem, permitindo que as organizações vendam cursos, certificações e programas de treinamento por meio de uma experiência de comércio eletrônico totalmente integrada.

**Principais recursos:**

- Integração perfeita da plataforma de comércio eletrônico.
- Catálogo de cursos e gerenciamento de preços.
- Processamento e inscrição automatizados de pagamentos.

Para mais informações, consulte [Conector do Adobe Commerce](/help/migrated/integration-admin/feature-summary/adobe-commerce-connector.md).

### Conector do Marketo Engage

O conector do Marketo Engage cria sinergias poderosas entre atividades de aprendizado e campanhas de marketing, permitindo que as organizações aproveitem o envolvimento educacional para incentivar o leads e o desenvolvimento do cliente.

#### Principais recursos:

- Criação e atualizações automáticas de leads.
- Rastreamento da atividade de aprendizado para insights de marketing.
- Acionadores de inscrição no curso e evento de conclusão.

Para obter mais informações, consulte [conector do Marketo Engage](/help/migrated/integration-admin/feature-summary/marketo-engage-connector.md).
