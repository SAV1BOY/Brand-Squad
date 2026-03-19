# Quarterly Brand Review
> Revisao trimestral completa do estado da marca.

## Objetivo
Conduzir uma revisao trimestral abrangente que consolide todas as metricas, analises e decisoes do periodo — gerando um panorama completo da saude da marca e definindo prioridades para o proximo trimestre.

## Agentes
- **brand-chief** — lidera a revisao trimestral
- **david-aaker** — contribui com avaliacao de equity
- **byron-sharp** — contribui com metricas de availability
- **kevin-keller** — contribui com evolucao CBBE

## Inputs
- Brand tracking analysis do trimestre
- Brand health scorecard
- Consistency review do periodo
- Registro de decisoes e mudancas
- Feedback dos squads parceiros

## Passos
1. Coletar todas as analises e metricas do trimestre
2. Consolidar brand health scorecard
3. Revisar decisoes e mudancas do periodo
4. Avaliar evolucao vs. metas definidas
5. Analisar movimentos competitivos do trimestre
6. Coletar feedback de squads parceiros
7. Definir prioridades para proximo trimestre
8. Documentar e distribuir relatorio trimestral

## Frameworks Obrigatorios
- brand-tracking-model
- aaker-brand-equity-model
- measurement-layer

## Checklists de Qualidade
- brand-tracking-quality
- brand-strategy-quality

## Output Esperado
```
## Quarterly Brand Review — Q[X] [ANO]
### Brand Health Score: [indice geral]
### Equity Evolution: [trend por dimensao]
### Key Wins: [conquistas do trimestre]
### Key Challenges: [desafios identificados]
### Competitive Landscape: [mudancas relevantes]
### Squad Feedback: [resumo]
### Prioridades Q[X+1]: [lista rankeada]
### Decisoes Tomadas: [registro]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand tracking analysis e brand health scorecard do trimestre concluidos, feedback dos squads parceiros coletado
- Gate de saida: score GREEN (>=80%) nos checklists brand-tracking-quality e brand-strategy-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para HRM Chief nivel 3 (revisao trimestral e estrategica)
- Se conflito entre david-aaker, byron-sharp e kevin-keller sobre priorizacao → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (metricas incompletas, prioridades nao fundamentadas, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-tracking-analysis, brand-health-scorecard-analysis, consistency-review, competitor-brand-shifts
- Downstream: brand-equity-plan (atualiza metas), competitive-repositioning (se necessario)
- Cross-squad: todos os squads (prioridades do proximo trimestre comunicadas)

### Metricas
- Indice geral de saude da marca vs. trimestre anterior
- Numero de prioridades definidas para proximo trimestre
- % de metas do trimestre atingidas
