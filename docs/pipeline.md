# Pipeline SDD — Spec-Driven Development

Fluxo sequencial de especificação orientada a entregas, com handoff entre etapas.

## Fluxo

```
00-idea  →  01-brief  →  02-prd  ──→  03-architecture  →  05-tasks  →  06-prompts
                                  └→  04-ux-ui  ──────────┘
```

| Etapa | Diretiva | Gera | Descrição |
|-------|----------|------|-----------|
| 00 | `00-idea.md` | `generated/idea.md` | Discovery estratégico — valida ideia, decide GO/NO-GO |
| 01 | `01-brief.md` | `generated/brief.md` | Product Brief — consolida visão, escopo MVP, direção técnica |
| 02 | `02-prd.md` | `generated/prd.md` | PRD operacional — requisitos, épicos, stories, critérios de aceite |
| 03 | `03-architecture.md` | `generated/architecture.md` | Arquitetura do sistema — stack, padrões, boundaries, convenções |
| 04 | `04-ux-ui.md` | `generated/ux-ui.md` | Especificação UX/UI — telas, componentes, interações, estados |
| 05 | `05-tasks.md` | `generated/tasks.md` | Task breakdown — milestones, dependências, slices verticais |
| 06 | `06-prompts.md` | `generated/prompts.md` | Prompts executáveis — prontos para coding agents |

## Como Usar

1. Cada arquivo `.md` em `docs/` é uma **diretiva de agente** com role, regras e comportamento
2. Execute cada etapa em sequência — o output de uma alimenta a próxima
3. Os artefatos gerados vão para `docs/generated/` com nomes limpos (sem número)
4. Os prompts finais em `docs/generated/prompts.md` estão prontos para execução em qualquer coding agent

## Handoff

Cada etapa produz um artefato em `docs/generated/` que serve como input para a etapa seguinte.
O handoff inclui:
- Output path do artefato gerado
- Formato esperado do output
- Próxima etapa e sua diretiva correspondente

## Agentes Compatíveis

Codex, Cursor, Windsurf, Claude Code, **OpenCode**
