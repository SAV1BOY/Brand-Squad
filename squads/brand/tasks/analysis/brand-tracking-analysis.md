# Brand Tracking Analysis
> Analise periodica de metricas de rastreamento da marca.

## Objetivo
Coletar, analisar e interpretar metricas de brand tracking — awareness, consideracao, preferencia, loyalty e mental availability — gerando insights para otimizacao continua da estrategia de marca.

## Agentes
- **byron-sharp** — lidera a analise de tracking
- **kevin-keller** — complementa com metricas CBBE
- **brand-chief** — orquestracao e validacao

## Inputs
- Dados de pesquisa de tracking do periodo
- Baseline de metricas anteriores
- Dados de vendas e market share
- Dados de social listening

## Passos
1. Coletar dados de todas as fontes de tracking
2. Calcular metricas de awareness (aided e unaided)
3. Analisar evolucao de consideracao e preferencia
4. Medir mental availability e CEPs
5. Avaliar metricas de loyalty e advocacy
6. Comparar com periodos anteriores (trend)
7. Comparar com concorrentes (benchmark)
8. Gerar insights e recomendacoes de acao

## Frameworks Obrigatorios
- brand-tracking-model
- measurement-layer

## Checklists de Qualidade
- brand-tracking-quality
- sharp/mental-availability-audit

## Output Esperado
```
## Brand Tracking Report
### Periodo: [datas]
### Awareness: [aided %, unaided %, trend]
### Consideracao: [%, trend]
### Preferencia: [%, trend vs. concorrentes]
### Mental Availability: [score, CEPs cobertos]
### Loyalty: [NPS, repeat, advocacy]
### Comparativo: [vs. periodo anterior e vs. concorrentes]
### Insights: [top 5 findings]
### Recomendacoes: [acoes priorizadas]
```

## Registro
- `data/metrics/brand-equity-score-history`
