# Referências e Fontes de Conhecimento

Este documento reúne as fontes utilizadas na construção do segundo cérebro sobre Inteligência Artificial Generativa aplicada ao Desenvolvimento de Software.

Foram priorizadas documentações oficiais, guias técnicos, cursos, tutoriais e materiais práticos.

As referências estão organizadas por assunto para facilitar a consulta e o aprofundamento dos estudos.

## 1. Agentes de Inteligência Artificial

Materiais sobre conceitos, arquitetura, funcionamento, orquestração e desenvolvimento de agentes.

### OpenAI

- [Definição e conceitos de agentes](https://developers.openai.com/api/docs/guides/agents/define-agents)
- [Visão geral de agentes](https://developers.openai.com/api/docs/guides/agents)
- [Guia de seleção do modelo mais recente](https://developers.openai.com/api/docs/guides/latest-model)
- [OpenAI Agents SDK](https://developers.openai.com/api/docs/guides/agents/sdk)
- [Documentação do OpenAI Agents SDK para JavaScript/TypeScript](https://openai.github.io/openai-agents-js/)
- [Referência TypeScript — withTranscriptionSpan](https://openai.github.io/openai-agents-js/openai/agents/variables/withtranscriptionspan/)

### Anthropic

- [Claude — boas práticas de engenharia de prompts](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)
- [Documentação oficial da plataforma Claude](https://platform.claude.com/docs/en/home)

## 2. Automação com n8n

Documentações, cursos e materiais relacionados à criação de workflows, integrações, automações e agentes de IA.

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

Referências sobre programação assistida por IA, engenharia de prompts, ferramentas de desenvolvimento e utilização de agentes na criação e manutenção de software.

### GitHub e GitHub Copilot

- [Guia de engenharia de prompts para LLMs](https://github.blog/engineering/prompt-engineering-guide-generative-ai-llms/)
- [Como funcionam os modelos por trás do GitHub Copilot](https://github.blog/2023-05-17-inside-github-working-with-the-llms-behind-github-copilot/)
- [Engenharia de prompts no GitHub Copilot](https://docs.github.com/en/copilot/concepts/prompting-and-context/prompt-engineering)
- [GitHub Copilot Chat — Cheat Sheet](https://docs.github.com/en/copilot/reference/chat-cheat-sheet)

### Claude Code e ferramentas de programação agêntica

Foram utilizados materiais demonstrativos sobre:

- Claude Code.
- OpenAI Codex CLI.
- Codex App.
- Integrações com IDEs JetBrains.
- Cursor.
- Estudos de caso de utilização do Claude Code em empresas como Factory, Ramp e Salesforce.

**Observação:** os títulos desses vídeos e estudos de caso foram fornecidos na relação de fontes do NotebookLM, mas alguns links originais não estavam disponíveis no material recebido. Os endereços serão adicionados quando forem recuperados.

## 4. Integração com APIs de LLMs

Documentações sobre comunicação com modelos de linguagem, chamadas de ferramentas, estruturação de respostas e integração com aplicações.

### OpenAI API

- [Function Calling](https://developers.openai.com/api/docs/guides/function-calling)
- [Using Tools — ferramentas e conectores](https://developers.openai.com/api/docs/guides/tools)
- [Model Context Protocol (MCP)](https://developers.openai.com/mcp)
- [Responses API — visão geral](https://developers.openai.com/api/reference/responses/overview)
- [Responses API vs. Chat Completions](https://platform.openai.com/docs/guides/responses-vs-chat-completions)
- [Seleção de modelos](https://developers.openai.com/api/docs/guides/model-selection)
- [Catálogo de modelos](https://developers.openai.com/api/docs/models)

### Tratamento de erros e limites de requisições

- [Códigos de erro da API](https://developers.openai.com/api/docs/guides/error-codes)
- [Rate Limits](https://developers.openai.com/api/docs/guides/rate-limits)

### Engenharia de prompts

- [Boas práticas de engenharia de prompts — OpenAI Help Center](https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-the-openai-api)
- [Guia de Prompt Engineering da OpenAI](https://platform.openai.com/docs/guides/prompt-engineering)

## 5. Segurança em IA Generativa e agentes

Fontes sobre vulnerabilidades, proteção de aplicações com LLMs, segurança de agentes e boas práticas de arquitetura.

### OWASP

- [OWASP Gen AI Security Project](https://genai.owasp.org/)
- [OWASP Top 10 para aplicações LLM](https://genai.owasp.org/llm-top-10/)
- [LLM01 — Prompt Injection](https://genai.owasp.org/llmrisk/llm01-prompt-injection/)
- [LLM03 — Supply Chain](https://genai.owasp.org/llmrisk/llm032025-supply-chain/)
- [LLM08 — Vector and Embedding Weaknesses](https://genai.owasp.org/llmrisk/llm082025-vector-and-embedding-weaknesses/)
- [OWASP Top 10 para aplicações de LLM e IA Generativa — Português](https://genai.owasp.org/resource/owasp-top-10-para-aplicacoes-de-llm-e-ia-generativa-2025/)

### AWS

- [Guia de arquitetura de segurança para agentes de IA](https://docs.aws.amazon.com/prescriptive-guidance/latest/agentic-ai-security/owasp-top-ten.html)

## 6. Modelos abertos e execução local

Materiais sobre modelos open-weight e alternativas para execução de modelos de linguagem em infraestrutura própria.

- GPT-OSS 20B e GPT-OSS 120B.
- Execução local com Ollama.
- Utilização de LM Studio.
- Infraestrutura com vLLM.
- Execução utilizando Llama.cpp.

**Observação:** a apresentação em vídeo sobre os modelos GPT-OSS foi utilizada como referência, mas o link original não estava disponível no material recebido.

## 7. Outras fontes e materiais complementares

Também foram identificados materiais sobre:

- Tratamento de erros assíncronos no Express.js.
- Boas práticas de desempenho e confiabilidade em aplicações Express.
- Toolkit de IA Responsável do Google.
- Tutoriais de automação com Docker e Google Gemini.
- Construção de agentes utilizando o OpenAI Agents SDK.

Os links originais desses materiais ainda precisam ser recuperados para inclusão nesta lista.

---

## Observações sobre as referências

- Links repetidos foram consolidados para evitar duplicação.
- As referências foram agrupadas de acordo com seus assuntos principais.
- Documentações oficiais foram priorizadas sempre que disponíveis.
- Vídeos e tutoriais sem endereço original identificado não foram substituídos por links presumidos.

**Total:** a relação contempla as referências com endereços identificáveis na lista recebida, além dos materiais complementares que aguardam recuperação dos links originais.
