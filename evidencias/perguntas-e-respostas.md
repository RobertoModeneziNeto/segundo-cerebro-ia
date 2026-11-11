# Evidências de Testes e Consultas

Este documento registra algumas das consultas realizadas no Google NotebookLM durante a avaliação do segundo cérebro.

## Teste 1 — Análise da base de conhecimento

**Objetivo:** avaliar se o NotebookLM conseguia organizar as informações das fontes adicionadas.

**Resultado:** o NotebookLM organizou o conteúdo em quatro áreas principais:

- Agentes de Inteligência Artificial.
- Automação com n8n.
- IA aplicada à programação.
- Integração com APIs de LLMs.

Também identificou aplicações práticas, tecnologias e pontos que precisavam de aprofundamento.

## Teste 2 — Arquitetura de um agente de IA

**Objetivo:** solicitar uma arquitetura utilizando React, Node.js, TypeScript e uma API de LLM.

**Resultado:** a ferramenta apresentou uma arquitetura dividida entre frontend, backend e integração com o modelo de linguagem. Também abordou segurança, ferramentas, contexto e validação de dados.

**Observação:** alguns exemplos de código apresentaram problemas de implementação e precisaram de revisão.

## Teste 3 — Desenvolvimento de uma solução prática

**Objetivo:** solicitar uma implementação de agente de IA com banco de dados, APIs externas e contexto de conversação.

**Resultado:** foram apresentados estrutura de pastas, dependências, exemplos de integração e recomendações de segurança.

**Limitações identificadas:** partes da implementação estavam incompletas, incluindo rotas da aplicação e interface frontend.

## Teste 4 — Auditoria e correção de código

**Objetivo:** avaliar se o NotebookLM conseguia identificar e corrigir problemas técnicos nos exemplos apresentados anteriormente.

**Resultado:** a ferramenta identificou alguns problemas, como o tratamento do histórico de conversação e a preservação das respostas das ferramentas.

Entretanto, algumas correções sugeridas também apresentaram inconsistências.

## Teste 5 — Validação do Function Calling

**Objetivo:** verificar a estrutura de acesso às respostas da Chat Completions API.

Foi identificado um erro recorrente no acesso à propriedade `choices`.

**Código incorreto:**

```typescript
response.choices.message
```

**Código correto:**

```typescript
response.choices[0].message
```

Mesmo após várias solicitações de correção, o NotebookLM continuou reproduzindo a sintaxe incorreta em suas respostas.

### Conclusão dos testes

Os testes demonstraram que o NotebookLM consegue organizar grandes volumes de informações, explicar conceitos e auxiliar na elaboração de arquiteturas e exemplos de código.

Por outro lado, também foram identificadas limitações na geração e revisão de código.

A principal conclusão é que as respostas produzidas por Inteligência Artificial precisam ser verificadas, especialmente quando envolvem implementação técnica, APIs e decisões de arquitetura.

A validação humana continua sendo uma etapa importante do desenvolvimento de software com IA.
