# Brand Equity Valuation Analysis
> Analise de valoracao do brand equity em multiplas dimensoes.

## Objetivo
Quantificar e qualificar o valor do brand equity — combinando modelos Aaker (equity dimensions) e Keller (CBBE) — gerando um score comparavel ao longo do tempo e entre concorrentes.

## Agentes
- **david-aaker** — lidera a avaliacao de equity (Aaker model)
- **kevin-keller** — complementa com CBBE pyramid
- **brand-chief** — orquestracao e validacao

## Inputs
- Dados de brand tracking
- Dados de pesquisa de percepcao
- Metricas financeiras (receita, market share, price premium)
- Historico de equity scores anteriores

## Passos
1. Calcular equity por dimensao Aaker (awareness, quality, associations, loyalty)
2. Mapear posicao na CBBE Pyramid (Keller)
3. Avaliar brand resonance e brand mantra
4. Calcular price premium atribuivel a marca
5. Comparar com scores anteriores (evolucao)
6. Benchmarkar com concorrentes
7. Identificar dimensoes mais fortes e mais fracas
8. Recomendar investimentos prioritarios

## Frameworks Obrigatorios
- brand-equity-valuation
- aaker-brand-equity-model
- keller-cbbe-pyramid

## Checklists de Qualidade
- aaker/aaker-equity-audit
- keller/cbbe-pyramid-audit

## Output Esperado
```
## Brand Equity Valuation
### Score Geral: [indice composto]
### Aaker Dimensions:
  - Awareness: [score + trend]
  - Perceived Quality: [score + trend]
  - Associations: [score + trend]
  - Loyalty: [score + trend]
### CBBE Level: [nivel na piramide]
### Price Premium: [% vs. generico]
### Benchmark: [vs. concorrentes]
### Investimento Prioritario: [dimensao + acao]
```

## Registro
- `data/metrics/brand-equity-score-history`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: dados de brand tracking disponiveis, dados de percepcao coletados, metricas financeiras acessiveis
- Gate de saida: score GREEN (>=80%) nos checklists aaker/aaker-equity-audit e keller/cbbe-pyramid-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre david-aaker e kevin-keller sobre metodologia de valoracao → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (dimensoes sem dados, benchmark ausente, price premium nao calculado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-tracking-analysis, perception-study, brand-audit
- Downstream: brand-health-scorecard-analysis, quarterly-brand-review, brand-equity-plan
- Cross-squad: nenhum (analise interna de equity)

### Metricas
- Score geral de equity (indice composto)
- Evolucao por dimensao Aaker vs. periodo anterior
- Price premium calculado vs. generico
