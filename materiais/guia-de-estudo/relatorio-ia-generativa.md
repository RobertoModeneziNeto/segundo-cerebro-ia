# IA Generativa aplicada ao Desenvolvimento de Software
## Engenharia de contexto, agentes inteligentes e desenvolvimento assistido por IA

## 1. Introdução

A Inteligência Artificial Generativa vem transformando a maneira como softwares são desenvolvidos, permitindo automatizar tarefas, acelerar a produção de código, integrar sistemas e criar aplicações capazes de interpretar informações e executar ações.

Grande parte dessas soluções utiliza os **Modelos de Linguagem de Grande Porte (LLMs — Large Language Models)**, que conseguem interpretar e gerar conteúdo a partir de instruções e contextos fornecidos pelo usuário ou pela aplicação.

Entretanto, para utilizar esses modelos em sistemas reais, não basta enviar uma pergunta e receber uma resposta. É necessário estruturar o contexto, definir instruções, disponibilizar ferramentas, controlar permissões e validar os resultados produzidos.

Nesse cenário, conceitos como engenharia de prompts, engenharia de contexto, RAG, agentes de IA e integração com APIs tornam-se fundamentais para o desenvolvimento de aplicações inteligentes.

Este material explora esses conceitos e apresenta como ferramentas como GitHub Copilot, OpenAI Codex, Claude Code, Cursor e OpenAI Agents SDK podem ser utilizadas no desenvolvimento de software.

### Objetivos de aprendizagem

Ao longo deste conteúdo, serão explorados os seguintes objetivos:

- Compreender os fundamentos dos modelos de linguagem e suas limitações.
- Entender a importância da engenharia de prompts e da engenharia de contexto.
- Conhecer técnicas de recuperação de informações, como RAG.
- Compreender a arquitetura e o funcionamento de agentes de IA.
- Explorar ferramentas de desenvolvimento assistido por inteligência artificial.
- Conhecer mecanismos de validação, execução de ferramentas e verificação automatizada de código.

---

## 2. Fundamentos dos LLMs e engenharia de contexto

### 2.1 O que são modelos de linguagem?

Um LLM é um modelo de inteligência artificial treinado para reconhecer padrões em grandes conjuntos de dados e gerar respostas a partir do contexto recebido.

Seu funcionamento envolve a previsão de tokens, que são unidades de texto e podem representar palavras, partes de palavras ou outros elementos. O modelo calcula quais tokens são mais prováveis em determinado contexto e os gera sequencialmente para construir uma resposta.

Embora essa explicação ajude a compreender seu funcionamento básico, os LLMs não devem ser considerados bancos de dados ou mecanismos de consulta com acesso garantido a todas as informações utilizadas durante o treinamento.

Suas respostas dependem de fatores como:

- Dados utilizados no treinamento.
- Instruções fornecidas.
- Contexto disponível na conversa.
- Recursos e ferramentas disponibilizados pela aplicação.
- Limites e capacidades do modelo utilizado.

Por isso, mesmo modelos avançados podem produzir informações incorretas, incompletas ou desatualizadas.

### 2.2 Engenharia de prompts

A engenharia de prompts consiste na elaboração de instruções que orientam o comportamento do modelo e ajudam a obter respostas mais relevantes.

Um prompt bem estruturado pode definir:

- **Objetivo:** o que precisa ser realizado.
- **Contexto:** informações necessárias para executar a tarefa.
- **Papel ou especialidade:** perspectiva que o modelo deve adotar.
- **Restrições:** o que deve ou não ser feito.
- **Formato de saída:** como a resposta deve ser apresentada.
- **Exemplos:** referências de resultados esperados.

Por exemplo, em vez de enviar apenas a mensagem de um cliente relatando um problema de conexão, uma aplicação de suporte pode fornecer o histórico do atendimento, informações técnicas disponíveis e instruções para que o modelo produza uma orientação adequada.

Essa estrutura reduz ambiguidades e aproxima a resposta da necessidade real do usuário.

### 2.3 Engenharia de contexto

A engenharia de contexto amplia a ideia de engenharia de prompts. Seu objetivo é selecionar, organizar e fornecer ao modelo as informações necessárias para executar uma tarefa.

Em aplicações de desenvolvimento de software, esse contexto pode incluir:

- Código-fonte do projeto.
- Estrutura de diretórios.
- Documentação técnica.
- Histórico de conversas.
- Regras de negócio.
- Resultados de testes.
- Informações recuperadas de bancos de dados.

O desafio está em fornecer informações relevantes sem ultrapassar os limites de contexto do modelo ou incluir dados desnecessários.

### 2.4 RAG — Retrieval-Augmented Generation

O RAG, ou Geração Aumentada por Recuperação, combina modelos de linguagem com mecanismos de busca e recuperação de informações.

Em vez de depender exclusivamente do conhecimento adquirido durante o treinamento, a aplicação pode consultar uma base de documentos e fornecer os trechos relevantes ao modelo durante a geração da resposta.

Um fluxo simplificado funciona assim:

1. O usuário envia uma pergunta.
2. A aplicação pesquisa informações em uma base de conhecimento.
3. Os documentos ou trechos relevantes são recuperados.
4. O conteúdo recuperado é enviado ao modelo junto com a pergunta.
5. O modelo utiliza o contexto para elaborar uma resposta.

Essa abordagem pode ser aplicada a assistentes de documentação, sistemas de suporte, consultas empresariais e ferramentas de análise de informações.

É importante destacar que o RAG não garante respostas corretas. A qualidade depende da base consultada, da recuperação dos documentos e da capacidade do modelo de interpretar as informações.

---

## 3. Pipeline de contexto em ferramentas de desenvolvimento

Ferramentas como o GitHub Copilot utilizam informações do ambiente de desenvolvimento para produzir sugestões mais relacionadas ao código que está sendo escrito.

Esse processo envolve a coleta e a seleção de informações relevantes antes de encaminhá-las ao modelo.

Entre os elementos que podem compor o contexto estão:

- Linguagem de programação utilizada.
- Arquivo atualmente aberto.
- Código próximo ao cursor.
- Arquivos relacionados ao desenvolvimento.
- Instruções e documentação do projeto.
- Histórico e informações adicionais disponibilizadas pela ferramenta.

### 3.1 Etapas de construção do contexto

De maneira conceitual, esse processo pode ser dividido em cinco etapas:

**1. Coleta de contexto (Gathering Context)**

A ferramenta identifica informações relevantes do ambiente, como arquivos, código atual, linguagem utilizada e instruções disponíveis.

**2. Seleção de trechos (Snippeting)**

Arquivos extensos podem ser divididos em trechos menores. Isso permite selecionar apenas as partes relevantes para a tarefa, reduzindo a quantidade de informações encaminhadas ao modelo.

**3. Organização e formatação**

Os trechos selecionados são organizados de maneira que o modelo consiga compreender sua origem e finalidade. Caminhos de arquivos, comentários e estruturas específicas podem ajudar nessa identificação.

**4. Priorização**

As informações são organizadas conforme sua relevância. O código próximo ao cursor, por exemplo, pode ser mais importante para uma sugestão imediata do que arquivos não relacionados.

**5. Geração e validação**

O contexto é enviado ao modelo, que produz uma sugestão. O desenvolvedor pode então revisar, aceitar, modificar ou testar o código gerado.

O objetivo desse pipeline é equilibrar relevância, qualidade da resposta, quantidade de contexto e velocidade de execução.

---

## 4. Construção de agentes autônomos com OpenAI Agents SDK

À medida que as aplicações evoluem, surge a necessidade de ir além de interações simples com modelos de linguagem.

Os **agentes de IA** são sistemas que combinam modelos, instruções, ferramentas e mecanismos de controle para executar tarefas de maneira orientada a objetivos.

Um agente pode interpretar uma solicitação, decidir qual ferramenta utilizar, executar uma ação, analisar o resultado e continuar o processo até alcançar o objetivo definido.

### 4.1 Componentes de um agente

Uma arquitetura de agente pode envolver:

- **Modelo:** responsável por interpretar informações e orientar as decisões.
- **Instruções:** definem o comportamento e os objetivos do agente.
- **Ferramentas:** permitem consultar APIs, acessar dados ou executar operações.
- **Contexto:** fornece informações necessárias durante a execução.
- **Guardrails:** ajudam a validar entradas, saídas e operações.
- **Orquestração:** controla a sequência de execução e a interação entre agentes.

### 4.2 Contexto do modelo e contexto local

No desenvolvimento de agentes, é importante diferenciar duas categorias de contexto.

**Contexto do modelo (Model Context)**

Representa as informações disponibilizadas ao modelo para que ele consiga interpretar a solicitação e tomar decisões. Pode incluir instruções, mensagens anteriores, resultados de ferramentas e documentos relevantes.

**Contexto local (Local Context / Run Context)**

Representa os dados e recursos mantidos pela aplicação durante a execução. Pode incluir informações de autenticação, clientes de banco de dados, serviços internos e registradores de eventos.

Essa separação ajuda a evitar o envio desnecessário de informações internas ao modelo e permite que o backend mantenha o controle sobre operações sensíveis.

### 4.3 Saídas estruturadas

Em aplicações reais, nem sempre é interessante receber uma resposta em texto livre.

É possível definir estruturas de saída para que o modelo produza dados em formatos específicos, que posteriormente podem ser validados pela aplicação.

Entre as ferramentas utilizadas estão:

- **Zod:** biblioteca de validação de esquemas para TypeScript.
- **Pydantic:** biblioteca de validação e modelagem de dados para Python.
- **Structured Outputs:** recurso que permite orientar a geração de respostas conforme um formato estruturado.

Esses mecanismos facilitam a integração entre modelos de linguagem e sistemas tradicionais.

### 4.4 Sistemas multiagentes e handoffs

Quando uma tarefa envolve diferentes especialidades, pode ser interessante distribuir o trabalho entre agentes.

Um agente principal pode receber a solicitação e encaminhá-la para agentes especializados, utilizando mecanismos de transferência conhecidos como **handoffs**.

Exemplo de organização:

- Agente principal: interpreta a solicitação.
- Agente de pesquisa: consulta informações.
- Agente de análise: interpreta os resultados.
- Agente executor: realiza uma operação autorizada.
- Agente avaliador: verifica o resultado.

Essa arquitetura pode melhorar a organização de tarefas complexas, mas também aumenta a necessidade de controlar comunicação, permissões, custos e possíveis falhas entre agentes.

---

## 5. Desenvolvimento assistido por inteligência artificial

Ferramentas de programação assistida por IA estão evoluindo de simples mecanismos de autocompletar código para ambientes capazes de analisar repositórios e executar tarefas de desenvolvimento.

Entre as principais ferramentas estudadas estão:

- **GitHub Copilot:** oferece sugestões de código e assistência durante o desenvolvimento.
- **OpenAI Codex:** auxilia na execução de tarefas de programação por meio de agentes de código.
- **Claude Code:** permite trabalhar com código e executar tarefas de desenvolvimento em um ambiente de terminal.
- **Cursor:** editor de código com recursos de inteligência artificial integrados.

### 5.1 Principais aplicações

Essas ferramentas podem auxiliar em diferentes etapas do desenvolvimento:

**Geração de código:** criação de funções, componentes, estruturas e arquivos.

**Refatoração:** reorganização de código para melhorar legibilidade e manutenção.

**Depuração:** análise de erros, interpretação de mensagens e sugestão de correções.

**Testes:** criação e execução de testes automatizados.

**Análise de repositórios:** compreensão da estrutura e identificação de dependências entre arquivos.

**Revisão de código:** análise de alterações e identificação de possíveis problemas.

### 5.2 Ciclo de execução e autoavaliação

Ferramentas mais avançadas podem executar um ciclo de trabalho que envolve:

1. Receber uma tarefa.
2. Analisar o projeto e identificar os arquivos relevantes.
3. Planejar as alterações.
4. Implementar o código.
5. Executar comandos e testes disponíveis.
6. Analisar os resultados.
7. Corrigir problemas identificados.
8. Apresentar as alterações para revisão.

Esse processo é conhecido como ciclo de autoavaliação ou auto-verificação.

Apesar dessas capacidades, a revisão humana continua sendo necessária. Um teste aprovado não garante que o código esteja livre de vulnerabilidades, erros de negócio ou problemas de arquitetura.

### 5.3 Recursos multimodais

Algumas ferramentas também conseguem trabalhar com imagens, capturas de tela e referências visuais.

Em um fluxo de desenvolvimento de interfaces, por exemplo, o agente pode receber uma imagem de referência, produzir uma implementação inicial e utilizar ferramentas de navegador, como Playwright, para verificar visualmente o resultado.

Essa abordagem aproxima o desenvolvimento assistido por IA de processos de prototipagem e validação visual.

---

## 6. Integração de aplicações com APIs de LLMs

Para incorporar inteligência artificial a um software, é necessário integrar o modelo à aplicação por meio de APIs ou SDKs.

Uma arquitetura comum utiliza React no frontend, Node.js com TypeScript no backend e um serviço de modelo de linguagem para processar as solicitações.

### 6.1 Arquitetura básica

**Frontend — React**

Responsável pela interface, captura das mensagens do usuário e apresentação das respostas.

**Backend — Node.js e TypeScript**

Responsável por autenticação, regras de negócio, comunicação com o modelo, validação de dados e execução de ferramentas.

**Modelo de linguagem — LLM**

Responsável por interpretar as solicitações e gerar respostas ou indicar a necessidade de utilizar ferramentas.

**Banco de dados**

Armazena informações da aplicação, usuários, histórico de conversas e outros dados necessários.

**APIs externas**

Disponibilizam funcionalidades adicionais, como consulta de informações, serviços de terceiros e integrações empresariais.

### 6.2 Function Calling

O Function Calling permite que um modelo solicite a execução de funções disponibilizadas pela aplicação.

O modelo não executa diretamente o código do backend. Ele identifica uma ferramenta disponível e retorna uma solicitação estruturada, que deve ser interpretada e executada pela aplicação.

O fluxo básico é:

1. A aplicação envia uma solicitação ao modelo junto com a definição das ferramentas disponíveis.
2. O modelo identifica se precisa utilizar alguma ferramenta.
3. A aplicação recebe a solicitação de execução.
4. O backend valida os argumentos e executa a função.
5. O resultado é enviado novamente ao modelo.
6. O modelo utiliza o resultado para continuar a execução ou elaborar a resposta final.

Esse mecanismo permite conectar modelos de linguagem a bancos de dados, APIs externas e funcionalidades internas.

### 6.3 Responses API e gerenciamento de contexto

A Responses API permite desenvolver interações com modelos de linguagem e utilizar recursos como ferramentas e respostas estruturadas.

Em fluxos com Function Calling, a aplicação precisa preservar corretamente os itens de resposta e os resultados das ferramentas para que o modelo tenha acesso ao histórico necessário durante a execução.

Também é importante definir limites de execução, tratar erros e validar os dados recebidos.

### 6.4 Model Context Protocol (MCP)

O MCP é um protocolo que padroniza a comunicação entre aplicações de IA e fontes externas de contexto e ferramentas.

Ele pode facilitar a integração com serviços, arquivos, bancos de dados e outros recursos, reduzindo a necessidade de desenvolver integrações específicas para cada combinação de aplicação e ferramenta.

---

## 7. Segurança e confiabilidade

A utilização de IA em aplicações reais exige atenção especial à segurança, principalmente quando os agentes podem acessar dados ou executar operações.

### 7.1 Proteção de credenciais

Chaves de API e outras credenciais devem permanecer no backend, armazenadas em variáveis de ambiente ou mecanismos apropriados de gerenciamento de segredos.

Elas não devem ser expostas no código enviado ao navegador, em repositórios públicos ou em registros de execução.

### 7.2 Princípio do menor privilégio

Cada agente e ferramenta deve receber somente as permissões necessárias para realizar sua tarefa.

Por exemplo, um agente responsável por consultar produtos não precisa necessariamente ter permissão para excluir registros do banco de dados.

### 7.3 Validação de entradas e saídas

Dados recebidos do usuário e argumentos retornados pelo modelo devem ser validados antes de serem utilizados.

Bibliotecas como Zod e Pydantic podem ajudar a definir estruturas e verificar os dados.

### 7.4 Prompt injection

Prompt injection é uma categoria de ataque na qual instruções maliciosas são introduzidas no conteúdo recebido pelo modelo, tentando alterar seu comportamento ou induzir ações indevidas.

Algumas medidas de proteção incluem:

- Separação entre instruções confiáveis e conteúdo externo.
- Validação das operações solicitadas.
- Controle de permissões das ferramentas.
- Revisão humana para ações sensíveis.
- Isolamento de ambientes de execução.
- Monitoramento das atividades dos agentes.

Guardrails podem contribuir para a validação de entradas, saídas e operações, mas não substituem uma arquitetura de segurança adequada.

### 7.5 Tratamento de erros e confiabilidade

Aplicações integradas a LLMs também precisam considerar falhas de rede, limites de requisições, indisponibilidade de serviços e respostas inválidas.

Entre as boas práticas estão:

- Tratamento centralizado de erros.
- Logs e monitoramento.
- Limites de tentativas.
- Estratégias de retry com backoff.
- Respeito às orientações de espera, como Retry-After, quando aplicáveis.
- Controle de operações repetidas e idempotência.
- Validação dos resultados antes de persistir informações.

---

## 8. Aplicações práticas

A combinação dessas tecnologias permite construir diferentes tipos de soluções.

| Aplicação | Tecnologias envolvidas | Finalidade |
|---|---|---|
| Assistente de documentação | LLM, RAG e banco de dados vetorial | Consultar documentação e responder perguntas |
| Agente de atendimento | LLM, APIs e n8n | Interpretar solicitações e automatizar etapas do atendimento |
| Assistente de desenvolvimento | Codex, Claude Code ou Cursor | Auxiliar na escrita, análise e manutenção de código |
| Automação empresarial | n8n, APIs REST e LLM | Integrar serviços e automatizar processos |
| Assistente financeiro | LLM, banco de dados e ferramentas | Consultar e organizar informações financeiras |
| Agente de análise de dados | LLM, PostgreSQL e APIs | Consultar informações e produzir análises |

Esses exemplos demonstram como a IA pode atuar como uma camada inteligente conectada a sistemas e serviços já existentes.

A escolha das tecnologias depende dos requisitos, da complexidade, dos custos, da segurança e da infraestrutura disponível.

---

## 9. Limitações e desafios

Apesar dos avanços, a utilização de IA generativa apresenta desafios técnicos e operacionais.

**Alucinações:** os modelos podem gerar informações incorretas ou referências inexistentes.

**Limites de contexto:** grandes volumes de informação podem exigir estratégias de seleção, resumo e recuperação de conteúdo.

**Custos:** o uso de APIs, ferramentas externas e múltiplos agentes pode aumentar o custo de execução.

**Latência:** chamadas a modelos e serviços externos podem tornar as aplicações mais lentas.

**Segurança:** agentes com permissões excessivas podem executar operações inadequadas ou acessar informações indevidas.

**Manutenção:** modelos, APIs e ferramentas podem sofrer alterações, exigindo atualização e validação contínuas.

**Dependência de validação humana:** resultados importantes devem passar por revisão e testes, principalmente em operações sensíveis.

Portanto, a IA deve ser tratada como um recurso de apoio à engenharia de software, e não como substituta automática dos processos de desenvolvimento, revisão e qualidade.

---

## 10. Resultados do projeto Second Brain

O projeto utilizou o Google NotebookLM como ambiente de organização e consulta de conhecimento.

Foram reunidas documentações oficiais, tutoriais, materiais técnicos e referências relacionadas às principais áreas de estudo.

Durante a construção da base de conhecimento, foram realizadas consultas para avaliar a capacidade do NotebookLM de:

- Explicar conceitos e relacionar diferentes tecnologias.
- Propor arquiteturas de agentes utilizando React, Node.js e TypeScript.
- Elaborar exemplos de integração com bancos de dados e APIs externas.
- Analisar implementações e identificar problemas técnicos.
- Revisar respostas e corrigir informações inconsistentes.

Os testes demonstraram que o NotebookLM consegue organizar conteúdos e produzir explicações úteis, mas também pode apresentar erros em exemplos de código, identificadores de modelos e detalhes de implementação.

Em algumas situações, mesmo após solicitações de correção, determinadas inconsistências permaneceram nas respostas.

Por esse motivo, a validação com documentação oficial e testes práticos foi considerada uma etapa essencial do projeto.

---

## 11. Conclusão

A Inteligência Artificial Generativa está ampliando as possibilidades do desenvolvimento de software, permitindo construir aplicações capazes de interpretar informações, utilizar ferramentas e automatizar tarefas.

O estudo dos LLMs, da engenharia de contexto, dos agentes de IA, do n8n e das APIs demonstra que a criação de soluções inteligentes exige muito mais do que a integração com um modelo de linguagem.

É necessário compreender a arquitetura da aplicação, controlar permissões, estruturar dados, validar resultados e implementar mecanismos de segurança e confiabilidade.

As ferramentas de desenvolvimento assistido por IA também representam uma mudança importante no trabalho dos desenvolvedores, oferecendo suporte desde a escrita de código até a execução de testes e análise de projetos.

Como principal aprendizado, destaca-se que a IA pode aumentar a produtividade e ampliar as possibilidades de desenvolvimento, desde que seja utilizada com planejamento, conhecimento técnico e validação humana.

**A construção de aplicações inteligentes depende não apenas da capacidade dos modelos, mas também da qualidade da engenharia utilizada para integrá-los ao software.**
