# Brand Equity Plan
> Plano estrategico de construcao e protecao do brand equity ao longo do tempo.

## Objetivo
Desenvolver um plano estruturado para construir, mensurar e proteger o brand equity — definindo acoes por dimensao de equity, metas e metricas de acompanhamento.

## Agentes
- **david-aaker** — lidera o plano de equity (Aaker model)
- **kevin-keller** — complementa com CBBE e brand resonance
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Resultados de brand audit
- Dados de brand tracking atual
- Posicionamento e brand strategy definidos
- Metas de negocio

## Passos
1. Avaliar estado atual do equity por dimensao (Aaker)
2. Mapear nivel atual na CBBE Pyramid (Keller)
3. Definir metas de equity por dimensao
4. Desenhar acoes para cada dimensao (awareness, quality, associations, loyalty)
5. Definir metricas e KPIs de acompanhamento
6. Estabelecer timeline e milestones
7. Definir riscos e planos de mitigacao
8. Documentar plano completo

## Frameworks Obrigatorios
- aaker-brand-equity-model
- keller-cbbe-pyramid
- brand-equity-valuation

## Checklists de Qualidade
- aaker/aaker-equity-audit
- keller/cbbe-pyramid-audit

## Output Esperado
```
## Brand Equity Plan
### Estado Atual: [score por dimensao]
### Metas: [por dimensao e timeline]
### Acoes por Dimensao:
  - Awareness: [acoes]
  - Perceived Quality: [acoes]
  - Associations: [acoes]
  - Loyalty: [acoes]
### KPIs: [metricas de acompanhamento]
### Timeline: [milestones trimestrais]
### Riscos: [e mitigacoes]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand audit concluido, posicionamento e brand strategy definidos, metas de negocio claras
- Gate de saida: score GREEN (>=80%) nos checklists aaker/aaker-equity-audit e keller/cbbe-pyramid-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre david-aaker e kevin-keller sobre priorizacao de dimensoes → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (metas sem baseline, KPIs nao mensuraveis, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-audit, positioning-development, perception-study
- Downstream: brand-tracking-analysis, quarterly-brand-review, brand-equity-valuation-analysis
- Cross-squad: nenhum (plano interno de equity)

### Metricas
- Numero de dimensoes de equity com meta definida
- % de KPIs com baseline e meta quantificada
- Completude do timeline com milestones trimestrais
