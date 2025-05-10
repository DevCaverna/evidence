# Projeto Disciplina: Requisitos de Software

Olá! Este repositório faz parte do projeto da disciplina de Requisitos de Software da UTFPR - Campus Cornélio Procópio.

Link do Padlet: [Evidence](https://padlet.com/kawanharshe/evidence-i6j1q27zigdgo0ue)

## 1. Introdução

***1.1. Nome do Grupo***

**DevCaverna**

**Integrantes:**
- [@KawanKakubo](https://github.com/KawanKakubo) — Kawan Harshe Kakubo
- [@OtavioGonzaga](https://github.com/OtavioGonzaga) — Otavio Luiz Gonzaga
- [@reimuh](https://github.com/reimuh) — André Born
- [@tavinhoo](https://github.com/tavinhoo) — Otávio
- [@Vinicius-Antonio](https://github.com/Vinicius-Antonio) — Vinicius Antonio

***1.2. Nome do Sistema***

Evidence

***1.3. Propósito do Sistema***

Este documento apresenta os requisitos dos usuários a serem desenvolvidos pela Evidence, fornecendo aos desenvolvedores as informações necessárias para o projeto e implementação, assim como para a realização dos testes e homologação do sistema.

O objetivo do sistema Evidence é auxiliar advogados e peritos judiciais por meio do cadastro de informações sobre processos jurídicos e do upload de documentos, possibilitando que uma inteligência artificial gere relatórios e insights sobre os casos. O sistema ajudará a otimizar o tempo dos profissionais, aumentar a precisão das análises e garantir melhores resultados em processos judiciais.

***1.4. Público-Alvo***

Este documento se destina aos arquitetos de software, engenheiros de software, testadores, clientes e demais profissionais envolvidos no desenvolvimento do sistema Evidence.

***1.5. Descrição dos Usuários***

O sistema Evidence será utilizado por advogados, peritos judiciais e demais profissionais da área jurídica.

***Personas:***
[Personas](https://www.canva.com/design/DAGmocIOSE4/01dDA-jb2goppFgMoq1PmA/edit?utm_content=DAGmocIOSE4&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

***Análise da situação atual: antes da introdução de sua solução***

- **O que as pessoas fazem?**  
  Analisam manualmente documentos e dados jurídicos, o que pode ser demorado e sujeito a erros.

- **Quais os artefatos envolvidos?**  
  Papéis físicos, documentos digitais não organizados, processos judiciais diversos.

- **O que elas precisam saber?**  
  Entender o andamento de processos, identificar padrões, reunir informações relevantes.

***Análise das tarefas depois: como serão executadas as suas tarefas com sua solução***

- **O que as pessoas fazem?**  
  Cadastram casos e documentos no sistema e analisam relatórios automáticos gerados pela IA.

- **Quais os artefatos envolvidos?**  
  Sistema Evidence, documentos digitais organizados e processados.

- **O que elas precisam saber?**  
  Como interpretar os insights e relatórios gerados automaticamente pelo sistema.

***Cenário: Antes***

Os profissionais jurídicos gastam horas analisando documentos e processos, frequentemente lidando com informações dispersas e sem auxílio de tecnologias inteligentes.

***Cenário: Depois***

Com o Evidence, os profissionais cadastram os dados no sistema e, em poucos minutos, recebem relatórios e insights baseados em IA, otimizando tempo e aumentando a precisão de suas decisões jurídicas.

## 2. Documentos gerais no repositório

***2.1. Requisitos Funcionais***

| Identificador | Descrição |
|---------------|-----------|
| **RF01** | O sistema deve permitir que o advogado cadastre informações básicas de um processo jurídico, incluindo número do processo, partes envolvidas e data de abertura. |
| **RF02** | O sistema deve permitir que o perito judicial faça upload de documentos relacionados a um processo em formatos como PDF, DOCX e JPEG. |
| **RF03** | O sistema deve permitir que o advogado consulte todos os processos cadastrados, filtrando por status ativo, arquivado e concluído. |
| **RF04** | O sistema deve gerar relatórios automáticos sobre padrões em processos jurídicos, como tempo médio de resolução e tendências de decisões. |
| **RF05** | O sistema deve enviar notificações para o advogado quando prazos processuais estiverem próximos de vencer. |
| **RF06** | O sistema deve permitir que o advogado adicione anotações personalizadas a um processo, como observações sobre estratégias ou contatos relevantes. |
| **RF07** | O sistema deve permitir que o perito judicial compartilhe documentos específicos com outros profissionais vinculados ao mesmo processo. |
| **RF08** | O sistema deve garantir que a inteligência artificial analise documentos jurídicos e destaque trechos relevantes. |
| **RF09** | O sistema deve permitir que o administrador gerencie permissões de acesso. |
| **RF10** | O sistema deve exportar relatórios em formatos como PDF para uso em apresentações ou arquivamento. |

***2.2. Requisitos Não Funcionais***

 Identificador | Descrição | Depende de |
|---------------|-----------|------------|
| **RNF01** | O sistema deve integrar-se com APIs governamentais para validação e atualização automática de dados processuais. | RF01, RF03 |
| **RNF02** | O sistema deve utilizar um banco de dados não relacional (NoSQL) para armazenar documentos, anotações e metadados de forma escalável. | RF02, RF06, RF08 |
| **RNF03** | O sistema deve ser implementado com suporte à concorrência e alta performance, utilizando a linguagem Go para otimizar tarefas paralelas, como geração de relatórios e processamento de documentos. | RF02, RF04, RF05, RF08 |
| **RNF04** | O sistema deve garantir alta disponibilidade (99,9%) para que os usuários possam acessá-lo a qualquer momento, especialmente em prazos críticos. | RF05, RF03 |
| **RNF05** | As notificações de prazos devem ser entregues com latência inferior a 5 minutos, via e-mail e/ou push notification. | RF05 |
| **RNF06** | O sistema deve permitir anotações com suporte a rich text (negrito, listas, links) e salvamento automático a cada 30 segundos. | RF06 |
| **RNF07** | O compartilhamento de documentos entre profissionais deve respeitar permissões e criptografia ponta a ponta. | RF07, RF09 |
| **RNF08** | A análise com inteligência artificial deve processar documentos com tempo de resposta inferior a 10 segundos por arquivo e exibir trechos destacados com precisão baseada em NLP jurídico. | RF08 |
| **RNF09** | O sistema deve oferecer um painel de controle para o administrador gerenciar permissões de forma granular, com logs de acesso e histórico de alterações. | RF09 |
| **RNF10** | Os relatórios exportados devem seguir padrões visuais consistentes (layout, cores, logotipo) e estar disponíveis nos formatos PDF e DOCX. | RF04, RF10 |

***2.3. Perguntas***

*<Arquivo com as perguntas realizadas na entrevista .>*

***2.4. Entrevista***

*<Arquivo com as respostas do indivíduo entrevistado e link do drive com upload da gravação.>*

***2.5. Histórias do Usuário***

*<Imagem, arquivo (PDF), link com as Histórias de Usuário.>*

***2.6. Diagramas de Caso de Uso e Especificações***

*<Imagem, arquivo (PDF), link com Diagrama de Caso de Uso.>*

***2.7. Diagramas de Atividades***

*<Imagem, arquivo (PDF), link com Diagrama de Atividades.>*

***2.8. Matrizes de Rastreabilidade***

*<Imagem, arquivo (PDF), link com Matriz de Rastreabilidade.>*

***2.9. Protótipos***

*<Imagem, arquivo (PDF), link com Protótipo.>*

## Estudo de Viabilidade

**Viabilidade Operacional:**  
O projeto é viável considerando a disponibilidade de tecnologias de inteligência artificial para análise de texto jurídico e plataformas de desenvolvimento de sistemas. Há também uma necessidade real de otimização de processos jurídicos, o que garante adesão do público-alvo.

**Viabilidade Técnica:** 
Quanto a viabilidade técnica, todos os aspectos são simples, com exceção da IA e do algoritmo de censura de dados sensíveis.
Para a IA, será utilizado um serviço de terceiros (OpenAI, Cloude, etc.), e o algoritmo pode ser importado de bibliotecas abertas para garantir viabilidade e segurança.

**Cronograma:**
- Levantamento de Requisitos: 2 semanas
- Análise e Modelagem: 2 semanas
- Desenvolvimento Inicial: 4 semanas
- Testes e Validações: 2 semanas
- Ajustes Finais e Deploy: 2 semanas

Total: Aproximadamente 3 meses.

## Objetivos de Desenvolvimento Sustentável (ODS)

Este projeto atende ao ODS 16 da ONU: Paz, Justiça e Instituições Eficazes, promovendo igualdade de acesso à justiça por meio de um sistema que gera decisões mais rápidas e justas com auxílio da tecnologia.

## Referências
