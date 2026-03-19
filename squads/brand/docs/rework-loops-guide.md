# Guia de Rework Loops — Brand Squad

> Processo padrao quando um output falha no quality gate. Garante melhoria continua sem loops infinitos.

---

## Objetivo

Definir o que acontece quando uma entrega do Brand Squad nao atinge o padrao minimo de qualidade (GREEN >= 80%). O rework loop e o mecanismo que transforma falhas em melhorias sem bloquear o sistema.

---

## Trigger

Um rework loop e acionado quando:
- Quality gate score < GREEN threshold (80%)
- Criterios especificos de um checklist nao foram atendidos
- brand-chief identifica inconsistencia entre entregas

---

## Processo

### Passo 1 — Identificacao de Falhas
O quality gate identifica quais criterios especificos falharam. Nao basta dizer "falhou" — e necessario listar exatamente quais itens do checklist nao passaram e por que.

### Passo 2 — Geracao do Rework Brief
Documento gerado automaticamente com:
- Task original e seu objetivo
- Checklist aplicado e score obtido
- Lista de criterios que falharam
- Evidencias do que esta faltando
- Sugestoes de melhoria (baseadas em frameworks relacionados)
- Prazo para re-entrega

### Passo 3 — Re-atribuicao
O rework brief e atribuido ao agente responsavel pelo output original. Se o agente original nao puder resolver (ex: falha em area fora do seu dominio), o brand-chief pode re-atribuir a outro agente.

### Passo 4 — Re-execucao Focada
O agente re-executa APENAS os pontos que falharam. Nao e necessario refazer o output inteiro — apenas os criterios nao atendidos.

### Passo 5 — Re-validacao
O output revisado passa pelo MESMO quality gate. Se GREEN, segue para a proxima etapa. Se ainda YELLOW ou RED, novo loop.

---

## Limites

| Regra | Valor |
|-------|-------|
| Max loops por output | 3 |
| Escalacao apos max loops | Automatica para brand-chief (Nivel 2) |
| Se brand-chief nao resolver | Escalacao para HRM Chief (Nivel 3) |

---

## Rework Brief Template

```
## Rework Brief — [Task] — Loop [N]

**Data:** YYYY-MM-DD
**Task:** [nome da task]
**Agente responsavel:** [nome]
**Checklist aplicado:** [nome do checklist]
**Score obtido:** [X%]

### Criterios que Falharam
- [ ] [criterio 1] — [evidencia do que falta]
- [ ] [criterio 2] — [evidencia do que falta]

### Sugestoes de Melhoria
- [sugestao baseada no framework relevante]

### Prazo
- Re-entrega ate: YYYY-MM-DD
```

---

## Registro

Cada rework loop e registrado em `data/registries/improvement-backlog` com:
- Task afetada
- Numero do loop
- Criterios que falharam
- Resultado apos rework

---

## Anti-patterns

- **Nao aceitar "quase bom"** — se o score e YELLOW, o gate nao foi passado
- **Nao pular o gate** — mesmo sob pressao de prazo
- **Nao fazer mais de 3 loops** — se 3 tentativas nao resolveram, o problema e estrutural e precisa de escalacao
- **Nao refazer tudo** — foco nos criterios que falharam, nao no output inteiro
- **Nao ignorar patterns** — se o mesmo criterio falha repetidamente, registrar em learnings-log

---

## Metricas

| Metrica | O que mede |
|---------|-----------|
| First-pass rate | % de outputs que passam no gate na primeira tentativa |
| Loops medios por task type | Quantos loops cada tipo de task precisa em media |
| Tempo medio de rework | Quanto tempo leva cada loop |
| Criterios mais falhados | Quais criterios falham com mais frequencia (feed improvement-backlog) |

---

## Conexoes

- **Quality Gates Guide:** `docs/quality-gates-guide.md` — define os gates que acionam rework
- **Escalation Protocol:** `docs/escalation-protocol.md` — o que acontece apos 3 loops
- **Improvement Backlog:** `data/registries/improvement-backlog` — onde registrar cada loop
- **Learnings Log:** `data/registries/learnings-log` — onde registrar patterns recorrentes
- **Config.yaml:** `config.yaml → rework` — configuracao do sistema de rework
