# SDD Pipeline — Spec-Driven Development

Uma metodologia sequencial que transforma ideias em prompts executáveis através de especificações estruturadas com handoff entre etapas.

## O Problema

Sessões avulsas com coding agents (ChatGPT, Claude, Codex, etc.) geram resultados inconsistentes. Cada nova sessão perde contexto, decisões se perdem, e o agente reinventa soluções a cada interação.

## A Solução

**SDD (Spec-Driven Development)** organiza o desenvolvimento em um **pipeline de 7 etapas**, cada uma com:
- Um **papel** específico (PM, Arquiteto, UX Designer, etc.)
- **Regras claras** de comportamento e escopo
- **Handoff explícito** — o output de uma etapa é o input da próxima
- **Anti-overengineering** embutido em cada diretiva

## Pipeline

```
00-idea  →  01-brief  →  02-prd  ──→  03-architecture  →  05-tasks  →  06-prompts
                                  └→  04-ux-ui  ──────────┘
```

| Etapa | Diretiva | Role | Gera |
|-------|----------|------|------|
| 00 | `docs/00-idea.md` | Strategic Product Discovery Partner | `docs/generated/idea.md` |
| 01 | `docs/01-brief.md` | Senior Product Manager | `docs/generated/brief.md` |
| 02 | `docs/02-prd.md` | Senior Product Requirements Engineer | `docs/generated/prd.md` |
| 03 | `docs/03-architecture.md` | Senior Software Architect | `docs/generated/architecture.md` |
| 04 | `docs/04-ux-ui.md` | Senior UX Strategist | `docs/generated/ux-ui.md` |
| 05 | `docs/05-tasks.md` | Senior Tech Lead | `docs/generated/tasks.md` |
| 06 | `docs/06-prompts.md` | AI Implementation Orchestrator | `docs/generated/prompts.md` |

## Como Usar

1. Clone o repositório
2. Abra com qualquer coding agent (OpenCode, Codex, Cursor, Windsurf, Claude Code, Gemini CLI)
3. Execute `docs/00-idea.md` — o agente assume o papel e conduz a conversa
4. Salve o artefato gerado em `docs/generated/idea.md`
5. Avance para `docs/01-brief.md` com o artefato como contexto
6. Repita até `docs/06-prompts.md`
7. Execute os prompts gerados — cada um é autocontido e implementável

## Guia Visual

Abra `docs/sdd-guide.html` no navegador para um guia interativo com explicações detalhadas, fluxo visual e dicas práticas.

## Compatibilidade

Codex, Cursor, Windsurf, Claude Code, OpenCode, Gemini CLI e qualquer agente compatível com markdown.

## Licença

MIT
