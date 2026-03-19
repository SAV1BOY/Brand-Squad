# Brand ROI Analysis
> Analise de retorno sobre investimento das iniciativas de marca.

## Objetivo
Medir e demonstrar o retorno sobre investimento (ROI) das iniciativas de branding — conectando investimentos em marca a resultados de negocio como price premium, market share, customer acquisition e lifetime value.

## Agentes
- **david-aaker** — lidera a conexao equity-resultado financeiro
- **byron-sharp** — valida impacto em penetracao e mental availability
- **brand-chief** — orquestracao e validacao

## Inputs
- Investimentos em marca no periodo (budget)
- Metricas de brand tracking (pre e pos)
- Dados financeiros (receita, margem, market share)
- Dados de aquisicao e retencao de clientes
- Price premium data

## Passos
1. Inventariar investimentos em marca no periodo
2. Mapear metricas de marca pre e pos investimento
3. Calcular evolucao de awareness, equity e loyalty
4. Correlacionar com metricas de negocio (receita, share)
5. Calcular price premium atribuivel a marca
6. Estimar impacto em customer acquisition cost
7. Calcular ROI geral e por iniciativa
8. Documentar caso de negocio para proximos investimentos

## Frameworks Obrigatorios
- brand-equity-valuation
- measurement-layer

## Checklists de Qualidade
- Dados financeiros validados
- Correlacoes com controle de variaveis externas
- ROI calculado com metodologia transparente

## Output Esperado
```
## Brand ROI Report
### Periodo: [datas]
### Investimento Total: [valor]
### Retorno de Marca:
  - Awareness: [delta]
  - Equity Score: [delta]
  - Price Premium: [%]
  - Market Share: [delta]
### ROI Geral: [% ou multiplo]
### ROI por Iniciativa: [ranking]
### Caso de Negocio: [justificativa para proximo ciclo]
### Limitacoes: [variaveis nao controladas]
```

## Registro
- `data/metrics/brand-equity-score-history`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: investimentos em marca inventariados, metricas de tracking pre e pos disponiveis, dados financeiros validados
- Gate de saida: dados financeiros validados, correlacoes com controle de variaveis externas, ROI calculado com metodologia transparente
- Score minimo: GREEN (>=80%) na validacao de completude e rigor metodologico

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre david-aaker e byron-sharp sobre atribuicao de resultados → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (correlacoes sem controle, dados financeiros incompletos, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-tracking-analysis, brand-equity-valuation-analysis
- Downstream: quarterly-brand-review, brand-equity-plan (informa proximo ciclo de investimento)
- Cross-squad: nenhum (analise interna de ROI)

### Metricas
- ROI geral das iniciativas de marca (% ou multiplo)
- Price premium atribuivel a marca (%)
- Ranking de ROI por iniciativa individual
