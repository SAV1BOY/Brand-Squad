# Guia de Aprendizado e Memoria Operacional — Brand Squad

> Como o Brand Squad aprende com cada execucao e transforma experiencia em melhoria sistematica.

---

## Objetivo

Garantir que o Brand Squad nao repita erros, replique sucessos e evolua continuamente. O squad possui memoria operacional — tudo que acontece e registrado, analisado e usado para melhorar proximas execucoes.

---

## Principio

Um squad sem memoria e um squad que repete erros. O Brand Squad opera com o ciclo Kaizen: cada execucao alimenta a proxima.

---

## Ciclo Kaizen

```
Execute → Measure → Learn → Improve → Execute
   │         │         │         │         │
   │    Quality    Registrar   Priorizar  Incorporar
   │     Gates    em logs     melhorias   na proxima
   │                                      execucao
```

---

## O Que Registrar

### 1. Decisoes — `data/registries/brand-decisions-log`
Toda decisao estrategica com contexto, opcoes consideradas, escolha final e racional.
**Quando:** apos cada decisao de marca
**Quem registra:** brand-chief ou agente responsavel

### 2. Premissas — `data/registries/assumptions-log`
Premissas feitas durante decisoes que precisam ser validadas no futuro.
**Quando:** ao tomar decisao baseada em suposicao
**Quem registra:** agente que fez a premissa

### 3. Riscos — `data/registries/risk-log`
Riscos identificados que podem impactar a marca.
**Quando:** ao identificar risco durante qualquer task
**Quem registra:** agente que identificou

### 4. Aprendizados — `data/registries/learnings-log`
Licoes de sucesso, falha e insight.
**Quando:** apos task concluida ou apos rework loop
**Quem registra:** agente executante + brand-chief

### 5. Melhorias — `data/registries/improvement-backlog`
Oportunidades de melhoria priorizadas.
**Quando:** apos falha em quality gate, apos retrospectiva, apos feedback
**Quem registra:** quality gate automatico + brand-chief

### 6. Handoffs — `data/registries/handoff-log`
Transferencias de assets entre squads.
**Quando:** apos cada handoff cross-squad
**Quem registra:** brand-chief

---

## Cadencia

| Atividade | Frequencia | Responsavel | Registro |
|-----------|-----------|-------------|----------|
| Post-task review | Apos cada task | Agente + brand-chief | learnings-log |
| Quarterly retrospective | Q1/Q2/Q3/Q4 | brand-chief + todos os agentes | improvement-backlog |
| Cross-squad sync | Mensal | brand-chief | handoff-log |
| Registry cleanup | Trimestral | brand-chief | Arquivar registros antigos |
| Assumption validation | Trimestral | agentes relevantes | assumptions-log |

---

## Como Learnings Retroalimentam Execucao

### Antes de Iniciar Task
1. Consultar `learnings-log` para tasks similares — que licoes foram aprendidas?
2. Consultar `assumptions-log` — alguma premissa relevante foi invalidada?
3. Consultar `improvement-backlog` — existe melhoria pendente aplicavel?

### Durante Execucao
4. Se encontrar risco → registrar em `risk-log`
5. Se tomar decisao → registrar em `brand-decisions-log`
6. Se assumir premissa → registrar em `assumptions-log`

### Apos Execucao
7. Registrar resultado em `learnings-log` (sucesso, falha ou insight)
8. Se quality gate falhou → improvement-backlog recebe automaticamente
9. Se handoff executado → registrar em `handoff-log`

---

## Metricas de Aprendizado

| Metrica | O que mede |
|---------|-----------|
| Learnings por quarter | Volume de aprendizados capturados |
| Improvements implementados | % do backlog que virou acao |
| Reincidencia de erros | % de erros que se repetem (deve tender a zero) |
| Premissas validadas | % de premissas que foram testadas |
| First-pass rate trend | Tendencia da taxa de aprovacao na primeira tentativa |

---

## Conexoes

- **Quality Gates Guide:** `docs/quality-gates-guide.md` — gates alimentam improvement-backlog
- **Rework Loops Guide:** `docs/rework-loops-guide.md` — loops alimentam learnings-log
- **Config.yaml:** `config.yaml → memory` — lista completa de registries
- **ARCHITECTURE.md:** secao 9 — diagrama do Kaizen loop
