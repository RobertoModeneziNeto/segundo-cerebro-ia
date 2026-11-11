# 🧠 Segundo Cérebro — IA Generativa aplicada ao Desenvolvimento de Software

Este repositório documenta a criação e utilização de um segundo cérebro utilizando o **Google NotebookLM**, com foco em Inteligência Artificial Generativa aplicada ao desenvolvimento de software.

O objetivo é reunir, organizar e conectar conhecimentos de diferentes fontes, utilizando a IA como ferramenta de apoio para estudar conceitos, compreender tecnologias, explorar aplicações práticas e desenvolver soluções.

## 🎯 Objetivo

Construir uma base de conhecimento que permita consultar informações técnicas, entender conceitos e explorar exemplos práticos relacionados ao uso de IA no desenvolvimento de software.

O projeto também busca avaliar a qualidade das respostas geradas pela IA, verificando se as informações estão fundamentadas nas fontes e identificando possíveis erros técnicos.

## 📚 Temas estudados

O conteúdo foi organizado em quatro áreas principais:

### 1. Agentes de Inteligência Artificial
- Fundamentos e funcionamento dos agentes de IA.
- Uso de ferramentas e chamadas de funções.
- Arquiteturas multiagentes.
- Orquestração, memória e contexto.
- Guardrails e segurança na execução de agentes.
- OpenAI Agents SDK e Claude.

### 2. Automação com n8n
- Fundamentos da plataforma n8n.
- Criação de fluxos automatizados.
- Integração com APIs e serviços externos.
- Utilização de agentes de IA nos workflows.
- Integração com modelos como OpenAI, Gemini e Claude.
- Webhooks, triggers e processamento de dados.
- Execução local e infraestrutura com Docker.

### 3. IA aplicada à programação
- Desenvolvimento assistido por Inteligência Artificial.
- Ferramentas como Claude Code, OpenAI Codex, Cursor e GitHub Copilot.
- Geração, revisão e manutenção de código.
- Desenvolvimento de aplicações com múltiplos arquivos.
- Testes automatizados e análise de código.
- Segurança e boas práticas no desenvolvimento com IA.

### 4. Integração com APIs de LLMs
- Funcionamento de APIs de modelos de linguagem.
- Function Calling e Tool Calling.
- Responses API e Chat Completions API.
- Structured Outputs e validação com Zod.
- Integração com aplicações JavaScript e TypeScript.
- Model Context Protocol (MCP).
- Tratamento de erros, limites de requisições e segurança.

## 🔎 Fontes de conhecimento

Foram reunidas mais de 50 fontes de estudo, incluindo:

- Documentações oficiais.
- Tutoriais técnicos.
- Vídeos demonstrativos.
- Exemplos de implementação.
- Materiais sobre arquitetura e boas práticas.
- Referências sobre segurança e infraestrutura.

A prioridade foi utilizar fontes oficiais e materiais técnicos que apresentassem aplicações práticas das tecnologias estudadas.

A relação das referências está disponível em [`fontes/referencias.md`](fontes/referencias.md).

## 🤖 Ferramenta utilizada

**Google NotebookLM**

O NotebookLM foi utilizado como ambiente central para organizar as fontes, consultar informações, fazer perguntas técnicas, analisar arquiteturas e gerar materiais de estudo.

A proposta é utilizar as fontes adicionadas como base para as respostas, reduzindo a dependência de informações externas e permitindo verificar a origem do conhecimento.

**Acesse o notebook:** [INSERIR LINK PÚBLICO DO NOTEBOOK]

## 🧪 Testes e validação

Durante o desenvolvimento, foram realizadas consultas para avaliar a capacidade do NotebookLM de:

- Explicar conceitos técnicos.
- Comparar tecnologias e ferramentas.
- Propor arquiteturas de software.
- Desenvolver exemplos em TypeScript.
- Explicar integrações entre aplicações e APIs.
- Identificar problemas em implementações.
- Corrigir códigos com base na documentação disponível.

Um dos testes envolveu a implementação de Function Calling utilizando a Chat Completions API.

Durante as revisões, foi identificado um erro recorrente no acesso ao array `choices`. Mesmo após diversas solicitações de correção e explicações sobre a estrutura da resposta, o NotebookLM continuou apresentando a sintaxe incorreta em alguns trechos.

O acesso correto é:

```typescript
response.choices[0].message
```

Esse teste demonstrou a importância de revisar e validar tecnicamente os resultados produzidos por ferramentas de Inteligência Artificial, mesmo quando elas utilizam documentação como referência.

Os testes e suas respectivas evidências serão documentados em [`evidencias/perguntas-e-respostas.md`](evidencias/perguntas-e-respostas.md).

## 📖 Materiais de estudo

O projeto também contempla a geração de materiais para facilitar a revisão e a compreensão dos conteúdos:

- Guia de estudos.
- Mapa mental.
- Apresentação.
- Questionário de revisão.

Os materiais serão organizados na pasta [`materiais-gerados/`](materiais-gerados/).

## 💡 Principais aprendizados

Durante o desenvolvimento deste projeto, foram explorados conceitos importantes sobre a utilização de IA no desenvolvimento de software.

Entre os principais aprendizados estão:

- Como agentes de IA podem utilizar ferramentas para executar tarefas.
- Como automatizar processos integrando diferentes serviços pelo n8n.
- Como utilizar LLMs em aplicações desenvolvidas com JavaScript e TypeScript.
- Como estruturar chamadas de ferramentas e validar seus argumentos.
- Como considerar segurança, memória, contexto e tratamento de erros na arquitetura.
- Por que a validação humana continua sendo importante ao utilizar IA para desenvolver software.

## 👨‍💻 Autor

**Roberto Modenezi Neto**

Estudante de Sistemas de Informação, interessado em desenvolvimento de software, Inteligência Artificial, automações e novas tecnologias.

---

*Projeto desenvolvido como atividade prática de construção de um segundo cérebro utilizando Inteligência Artificial.*
