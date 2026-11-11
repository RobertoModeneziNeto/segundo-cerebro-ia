# Referências e Fontes de Conhecimento

Este documento reúne as fontes utilizadas na construção do segundo cérebro sobre Inteligência Artificial Generativa aplicada ao Desenvolvimento de Software.

Foram utilizadas documentações oficiais, cursos, tutoriais, vídeos técnicos, demonstrações e materiais sobre arquitetura e segurança.

As referências estão organizadas por categoria. Links repetidos foram consolidados.

## 1. Agentes de Inteligência Artificial

### OpenAI — documentação oficial

- [Definição e conceitos de agentes](https://developers.openai.com/api/docs/guides/agents/define-agents)
- [Visão geral de agentes e infraestrutura](https://developers.openai.com/api/docs/guides/agents)
- [Guia de seleção do modelo mais recente](https://developers.openai.com/api/docs/guides/latest-model)
- [OpenAI Agents SDK](https://developers.openai.com/api/docs/guides/agents/sdk)

### OpenAI Agents SDK — JavaScript/TypeScript

- [Documentação geral do SDK](https://openai.github.io/openai-agents-js/)
- [Sessions — gerenciamento de sessões](https://openai.github.io/openai-agents-js/guides/sessions)
- [Guardrails — validações e proteções](https://openai.github.io/openai-agents-js/guides/guardrails)
- [Running Agents — execução de agentes](https://openai.github.io/openai-agents-js/guides/running-agents)
- [Results & State — resultados e estado](https://openai.github.io/openai-agents-js/guides/results)

### Anthropic — Claude

- [Claude Prompting Best Practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)
- [Documentação oficial da plataforma Claude](https://platform.claude.com/docs/en/home)

## 2. Automação com n8n

### Documentação e integrações

- [Documentação oficial do n8n](https://docs.n8n.io/)
- [Exemplos de integração com o servidor MCP do n8n](https://docs.n8n.io/connect/connect-to-n8n-mcp-server/mcp-client-examples)
- [Site oficial do n8n](https://n8n.io/)

### Cursos da n8n Academy

- [N8N101 — Essentials: Your First Workflows](https://learn.n8n.io/courses/course-v1:n8n+N8N101+2026H2/about)
- [N8N102 — Integrations: APIs & Connected Workflows](https://learn.n8n.io/courses/course-v1:n8n+N8N102+2026H2/about)
- [N8N103 — In Practice: AI, Testing & Best Practices](https://learn.n8n.io/courses/course-v1:n8n+N8N103+2026H2/about)
- [QS101 — n8n Quickstart](https://learn.n8n.io/courses/course-v1:n8n+QS101+2026H2/about)

### Comunidade

- [Comunidade n8n no Discord](https://discord.gg/G98WXzsjky)

## 3. IA aplicada à programação

Materiais sobre programação assistida por IA, ferramentas agênticas, engenharia de prompts e desenvolvimento de software.

### GitHub e GitHub Copilot

- [GitHub Blog — Prompt Engineering Guide](https://github.blog/engineering/prompt-engineering-guide-generative-ai-llms/)
- [Inside GitHub — Working with the LLMs behind Copilot](https://github.blog/2023-05-17-inside-github-working-with-the-llms-behind-github-copilot/)
- [GitHub Copilot — Prompt Engineering](https://docs.github.com/en/copilot/concepts/prompting-and-context/prompt-engineering)
- [GitHub Copilot — Chat Cheat Sheet](https://docs.github.com/en/copilot/reference/chat-cheat-sheet)

### Anthropic — vídeos sobre Claude Code

Vídeos e demonstrações publicados no canal da Anthropic:

- Introducing Claude Code
- Projects are now a conversation with Claude
- How the Claude Code team uses Claude Code
- How Salesforce uses Claude Code
- How Factory is building autonomous software with Claude
- Building secure agents for knowledge work
- How Ramp engineers work with AI agents at every step

### OpenAI — vídeos sobre Codex e modelos abertos

Vídeos e demonstrações publicados no canal da OpenAI:

- Building with Open Models — apresentação dos modelos GPT-OSS 20B e GPT-OSS 120B.
- OpenAI Codex in your code editor
- Automatic code reviews with OpenAI Codex
- Using OpenAI Codex CLI with GPT-5-Codex
- Introducing the Codex app
- Build beautiful frontends with OpenAI Codex
- Codex in JetBrains IDEs
- Using AI in humanitarian work

### Cursor e engenharia de contexto

- [Context Engineering & Coding Agents with Cursor](https://www.youtube.com/watch?v=3KAI__5dUn0)

### Tutoriais da comunidade

- OpenAI Agents SDK Tutorial (FULL SERIES) — Kody Simpson.
- n8n Tutorial for Beginners - Build Your First Free AI Agent — Kevin Stratvert.

**Observação:** os títulos dos vídeos acima foram identificados na relação exportada pelo NotebookLM. Quando o endereço direto não foi fornecido, o título foi preservado sem criar um link presumido.

## 4. Integração com APIs de LLMs

Documentações sobre integração com modelos de linguagem, chamadas de ferramentas, estruturação de respostas e comunicação entre aplicações.

### OpenAI API

- [Function Calling](https://developers.openai.com/api/docs/guides/function-calling)
- [Using Tools — ferramentas e conectores](https://developers.openai.com/api/docs/guides/tools)
- [Model Context Protocol (MCP)](https://developers.openai.com/mcp)
- [Responses API — visão geral](https://developers.openai.com/api/reference/responses/overview)
- [Responses API vs. Chat Completions](https://platform.openai.com/docs/guides/responses-vs-chat-completions)
- [Model Selection — seleção de modelos](https://developers.openai.com/api/docs/guides/model-selection)
- [Catálogo oficial de modelos](https://developers.openai.com/api/docs/models)

### Tratamento de erros e limites de requisições

- [Error Codes — códigos de erro da API](https://developers.openai.com/api/docs/guides/error-codes)
- [Rate Limits — limites de requisições](https://developers.openai.com/api/docs/guides/rate-limits)

### Engenharia de prompts

- [OpenAI Prompt Engineering Best Practices](https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api)
- [Prompt Engineering Guide](https://platform.openai.com/docs/guides/prompt-engineering)

## 5. Segurança em IA Generativa e agentes

Fontes sobre vulnerabilidades, segurança de aplicações com LLMs e boas práticas para construção de agentes.

### OWASP

- [OWASP Gen AI Security Project](https://genai.owasp.org/)
- [OWASP Top 10 para aplicações LLM](https://genai.owasp.org/llm-top-10/)
- [LLM01 — Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/)
- [LLM03 — Supply Chain](https://genai.owasp.org/llmrisk/llm032025-supply-chain/)
- [LLM08 — Vector and Embedding Weaknesses](https://genai.owasp.org/llmrisk/llm082025-vector-and-embedding-weaknesses/)
- [OWASP Top 10 para aplicações de LLM e IA Generativa — Português](https://genai.owasp.org/resource/owasp-top-10-para-aplicacoes-de-llm-e-ia-generativa-2025/)

### AWS

- [AWS Prescriptive Guidance — Mapping to OWASP Top 10](https://docs.aws.amazon.com/prescriptive-guidance/latest/agentic-ai-security/owasp-top-ten.html)

### Google

- Google Responsible Generative AI Toolkit.

**Observação:** o endereço direto do toolkit do Google não foi disponibilizado na relação recebida.

## 6. Modelos abertos e execução local

Materiais sobre modelos open-weight e execução local de modelos de linguagem.

### GPT-OSS

- Building with Open Models — apresentação dos modelos `gpt-oss-20b` e `gpt-oss-120b`, publicada pela OpenAI.

### Tecnologias de execução abordadas

- Ollama.
- LM Studio.
- vLLM.
- Llama.cpp.

**Observação:** o endereço direto do vídeo Building with Open Models não foi disponibilizado na relação recebida.

## 7. Vídeos, demonstrações e webinars complementares

### Vimeo — demonstrações oficiais

- [Realtime Agent Demo](https://vimeo.com/1105243382)
- [Responses API — Tools & Features](https://vimeo.com/1105245596)
- [Unlock Agentic Power — Agents SDK](https://vimeo.com/1105245234)

### Webinars OpenAI

- [Build Hour — Agentic Tool Calling](https://webinar.openai.com/on-demand/d1a99ac5-8de8-43c5-b209-21903d76b5b2)
- [Build Hour — Built-in Tools](https://webinar.openai.com/on-demand/c17a0484-d32c-4359-b5ee-d318dad51586)

## 8. Desenvolvimento backend com Express.js

Materiais complementares sobre desenvolvimento de aplicações Node.js e boas práticas de implementação.

- Express.js Error Handling — tratamento de erros.
- Express.js Production Best Practices — desempenho e confiabilidade em produção.

**Observação:** os endereços dessas duas referências não estavam disponíveis na relação recebida.

---

## Organização das referências

As fontes foram agrupadas em sete áreas de conhecimento e uma seção complementar:

1. Agentes de Inteligência Artificial.
2. Automação com n8n.
3. IA aplicada à programação.
4. Integração com APIs de LLMs.
5. Segurança em IA Generativa e agentes.
6. Modelos abertos e execução local.
7. Vídeos, demonstrações e webinars.
8. Desenvolvimento backend com Express.js.

A lista foi organizada a partir das fontes apresentadas pelo NotebookLM. Referências sem URL direto foram mantidas com seus títulos, sem substituição por endereços não confirmados.
