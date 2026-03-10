# Calculadora de Brand Equity

> Calculo do valor composto de brand equity baseado no modelo de cinco dimensoes de Aaker.

## Objetivo

Produzir score unico de brand equity que integra multiplas dimensoes e permite comparacao ao longo do tempo e contra concorrentes.

## Inputs

- Dados de pesquisa de awareness (recall, recognition)
- Dados de pesquisa de associacoes (forca, favorabilidade, unicidade)
- Dados de qualidade percebida (vs. categoria e concorrentes)
- Dados de lealdade (NPS, retention, share of wallet, recompra)
- Dados de distinctive assets (fama e unicidade)

## Processo

### 1. Score por Dimensao (0-100)

**Awareness Score**
= (Top of Mind × 3 + Recall Espontaneo × 2 + Recognition × 1) / 6 × 100

**Associacoes Score**
= (Forca + Favorabilidade + Unicidade) / 3 × 100

**Qualidade Percebida Score**
= Score de qualidade vs. media da categoria × 100

**Lealdade Score**
= (NPS normalizado × 0.3 + Retention × 0.3 + Recompra × 0.2 + Share of Wallet × 0.2) × 100

**Assets Score**
= Media de (Fama × Unicidade) de todos os assets principais × 100

### 2. Score Composto

Brand Equity Score = (Awareness × 0.20) + (Associacoes × 0.25) + (Qualidade × 0.20) + (Lealdade × 0.20) + (Assets × 0.15)

### 3. Interpretacao

| Score | Classificacao | Significado |
|-------|--------------|-------------|
| 80-100 | Excepcional | Top 10% da categoria |
| 60-79 | Forte | Acima da media |
| 40-59 | Medio | Na media da categoria |
| 20-39 | Fraco | Abaixo da media |
| 0-19 | Critico | Necessita acao imediata |

## Output

Score composto + breakdown por dimensão + comparativo com periodos anteriores + gap analysis + recomendações priorizadas.

## Exemplo de Uso

```
> brand-equity-calculator --brand "MarcaX"
> Equity Score: 68/100 (Forte)
> Breakdown: Awareness 75, Associacoes 72, Qualidade 70, Lealdade 60, Assets 55
> Gap principal: Assets (55) — distinctive assets precisam de investimento
```
