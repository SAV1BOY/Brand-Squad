# Social Sentiment Analysis
> Analise aprofundada de sentimento da marca em canais digitais.

## Objetivo
Analisar o sentimento do publico em relacao a marca em redes sociais e plataformas digitais — identificando drivers de sentimento positivo e negativo, tendencias e alertas para gestao proativa da reputacao.

## Agentes
- **byron-sharp** — lidera a analise de salience e sentimento
- **donald-miller** — interpreta narrativas e messaging
- **brand-chief** — orquestracao e validacao

## Inputs
- Dados de social listening
- Mencoes e reviews coletadas
- Historico de sentimento (baseline)
- Eventos e campanhas do periodo

## Passos
1. Coletar dados de sentimento de todas as plataformas
2. Classificar por sentimento (positivo, negativo, neutro)
3. Identificar drivers de sentimento positivo (o que gera elogios)
4. Identificar drivers de sentimento negativo (o que gera criticas)
5. Correlacionar sentimento com eventos e campanhas
6. Analisar evolucao temporal (trend)
7. Identificar alertas e riscos reputacionais
8. Recomendar acoes de gestao de sentimento

## Frameworks Obrigatorios
- brand-salience-heuristics
- brand-tracking-model

## Checklists de Qualidade
- Dados de multiplas plataformas incluidos
- Classificacao consistente de sentimento
- Correlacao com eventos documentada

## Output Esperado
```
## Social Sentiment Report
### Periodo: [datas]
### Sentimento Geral: [% positivo / negativo / neutro]
### Drivers Positivos: [top 5 temas]
### Drivers Negativos: [top 5 temas]
### Trend: [evolucao no periodo]
### Correlacao com Eventos: [campanhas e impacto]
### Alertas: [riscos reputacionais]
### Recomendacoes: [acoes de gestao]
```

## Registro
- `data/research/social-listening/`
