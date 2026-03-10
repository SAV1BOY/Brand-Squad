# Brand Health Scorecard Analysis
> Analise consolidada da saude da marca em formato de scorecard executivo.

## Objetivo
Consolidar todas as metricas de marca em um scorecard unico e visual — combinando equity, tracking, distinctive assets, consistencia e performance — para comunicacao executiva e tomada de decisao.

## Agentes
- **brand-chief** — lidera a consolidacao
- **byron-sharp** — contribui com metricas de availability
- **kevin-keller** — contribui com metricas de equity

## Inputs
- Brand tracking analysis
- Distinctive assets recognition analysis
- Brand equity valuation
- Consistency review
- Dados de performance de negocio

## Passos
1. Definir dimensoes do scorecard (equity, awareness, consistency, etc.)
2. Coletar scores de cada dimensao
3. Normalizar escalas para comparabilidade
4. Calcular indice geral de saude da marca
5. Identificar semaforo por dimensao (verde, amarelo, vermelho)
6. Comparar com scorecard do periodo anterior
7. Destacar alertas e celebracoes
8. Documentar scorecard e distribuir

## Frameworks Obrigatorios
- brand-tracking-model
- measurement-layer

## Checklists de Qualidade
- brand-tracking-quality
- Todas as dimensoes com dados atualizados
- Comparativo temporal incluido

## Output Esperado
```
## Brand Health Scorecard
### Indice Geral: [score 0-100]
### Dimensoes:
  - Brand Equity: [score + semaforo]
  - Awareness: [score + semaforo]
  - Mental Availability: [score + semaforo]
  - Distinctive Assets: [score + semaforo]
  - Consistencia: [score + semaforo]
  - Brand Sentiment: [score + semaforo]
### Evolucao: [vs. periodo anterior]
### Alertas: [dimensoes em vermelho]
### Destaques: [dimensoes em verde]
### Acoes Recomendadas: [top 3 prioridades]
```

## Registro
- `data/metrics/brand-equity-score-history`
