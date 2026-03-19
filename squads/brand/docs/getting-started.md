# Primeiros Passos com o Brand Squad

> Guia operacional para comecar a usar o Brand Squad em projetos de marca.

---

## O Que E o Brand Squad

O Brand Squad e o sistema operacional de marca do MMOS. Ele opera com 15 agentes especializados, organizados em 6 camadas (Research → Strategy → Identity → Activation → Governance → Measurement), coordenados por um Brand Chief e governados por quality gates em cascata.

**Antes de qualquer coisa, leia:**
- `ARCHITECTURE.md` — mapa completo de interconexao do squad
- `config.yaml` — cerebro de roteamento (task → agents → frameworks → checklists → templates)

---

## Passo 1: Identifique o Tipo de Projeto

| Projeto | Template | Workflow |
|---------|----------|---------|
| Marca do zero | `projects/new-brand-project.md` | `workflows/brand-discovery-workflow.md` |
| Rebrand completo | `projects/rebrand-project.md` | `workflows/rebrand-workflow.md` |
| Refresh de marca | `projects/brand-refresh-project.md` | `workflows/brand-refresh-workflow.md` |
| Naming | `projects/naming-project.md` | `workflows/naming-workflow.md` |
| Auditoria de marca | `projects/brand-audit-project.md` | `workflows/brand-audit-workflow.md` |
| Guidelines | `projects/brand-guidelines-project.md` | `workflows/brand-guidelines-workflow.md` |
| Brand tracking | `projects/brand-tracking-project.md` | `workflows/brand-tracking-workflow.md` |
| Extension de marca | `projects/brand-extension-project.md` | `workflows/brand-extension-workflow.md` |
| Employer brand | `projects/employer-brand-project.md` | `workflows/employer-brand-workflow.md` |
| Rollout | `projects/brand-rollout-project.md` | `workflows/rollout-workflow.md` |
| Crise de marca | `projects/brand-crisis-response-project.md` | `workflows/brand-crisis-workflow.md` |

---

## Passo 2: Consulte o Roteamento

Abra o `config.yaml` e localize a task correspondente na secao `routing`. La voce encontra:
- **agents**: quem participa
- **frameworks**: quais metodologias aplicar
- **checklists**: quais quality gates passar
- **templates**: quais entregaveis gerar
- **registry**: onde registrar o resultado

Exemplo para `brand-audit`:
```yaml
brand-audit:
  agents: [brand-chief, byron-sharp, kevin-keller]
  frameworks: [aaker-brand-equity-model, keller-cbbe-pyramid, distinctive-assets-system]
  checklists: [aaker/aaker-equity-audit, sharp/distinctive-assets-audit]
  templates: [analysis/brand-audit-report-template]
  registry: data/registries/brand-decisions-log
```

---

## Passo 3: Ative os Agentes

Consulte `docs/agent-roles-guide.md` para entender qual agente faz o que. Regras:
- Cada agente so executa dentro do seu dominio
- O Brand Chief coordena e resolve conflitos
- Se a task envolver multiplos agentes, siga a ordem definida no workflow

Para perfis completos dos agentes: `agents/*.md`

---

## Passo 4: Execute a Task

1. Leia a task em `tasks/[categoria]/[task-name].md`
2. Siga os passos de execucao na ordem
3. Aplique os frameworks obrigatorios de `frameworks/`
4. Preencha os templates de `templates/`
5. Passe pelos checklists de qualidade de `checklists/`

---

## Passo 5: Passe pelos Quality Gates

O squad opera com 5 niveis de quality gates em cascata:

```
1. Agent Gate → cada agente valida seu output
2. Task Gate → checklists obrigatorios do config.yaml
3. Layer Gate → transicao entre camadas (checklists/layer-gate-*.md)
4. Chief Gate → brand-chief revisa output consolidado
5. Final Gate → validacao antes de handoff cross-squad
```

Scoring: GREEN (>=80%) | YELLOW (60-79%, chief override) | RED (<60%, bloqueado)

Detalhes: `docs/quality-gates-guide.md`

---

## Passo 6: Registre o Resultado

Apos aprovacao, registre em `data/registries/`:
- Decisoes → `brand-decisions-log.md`
- Premissas → `assumptions-log.md`
- Riscos → `risk-log.md`
- Aprendizados → `learnings-log.md`
- Melhorias → `improvement-backlog.md`

---

## Passo 7: Handoff (se aplicavel)

Se o output precisa ir para outro squad:
1. Passe pelo Final Gate (gate 5)
2. Empacote os assets conforme `docs/handoff-contracts-guide.md`
3. Registre em `data/registries/handoff-log.md`
4. Faca follow-up com o squad receptor

Contratos ativos: Brand → Copy, Marketing, Product, Design, People

---

## Guias de Referencia

| Guia | Conteudo |
|------|----------|
| `docs/agent-roles-guide.md` | Papeis e decisao de qual agente usar |
| `docs/framework-selection-guide.md` | Como escolher o framework certo |
| `docs/template-usage-guide.md` | Como usar e customizar templates |
| `docs/checklist-usage-guide.md` | Como aplicar checklists de qualidade |
| `docs/quality-gates-guide.md` | Sistema de quality gates em cascata |
| `docs/escalation-protocol.md` | Quando e como escalar |
| `docs/rework-loops-guide.md` | Processo de rework quando gate falha |
| `docs/cross-squad-integration-guide.md` | Integracao com outros squads |
| `docs/handoff-contracts-guide.md` | Contratos de handoff formais |
| `docs/learning-and-memory-guide.md` | Ciclo Kaizen de aprendizado |
| `docs/brand-governance-policy.md` | Politica de governanca |
| `docs/naming-and-domain-policy.md` | Regras de naming |

---

Referencia: `config.yaml` | `ARCHITECTURE.md` | `README.md`
