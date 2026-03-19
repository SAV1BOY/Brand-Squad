# Social Listening Analysis
> Analise de mencoes e conversas sobre a marca nas redes sociais e plataformas digitais.

## Objetivo
Monitorar e analisar o que esta sendo dito sobre a marca em canais digitais — volume, sentimento, temas e influenciadores — gerando insights para ajustes de estrategia e comunicacao.

## Agentes
- **byron-sharp** — lidera a analise de salience e mental availability
- **brand-chief** — orquestracao e validacao

## Inputs
- Palavras-chave e termos de busca definidos
- Acesso a ferramentas de social listening
- Periodo de analise definido
- Benchmark de concorrentes

## Passos
1. Definir termos de busca (marca, produtos, concorrentes)
2. Configurar monitoramento nas plataformas relevantes
3. Coletar dados de mencoes no periodo definido
4. Classificar mencoes por sentimento (positivo, negativo, neutro)
5. Identificar temas e topicos mais recorrentes
6. Mapear influenciadores e advogados da marca
7. Comparar share of voice com concorrentes
8. Documentar insights e alertas

## Frameworks Obrigatorios
- brand-salience-heuristics
- category-entry-points

## Checklists de Qualidade
- Minimo 3 plataformas monitoradas
- Classificacao de sentimento consistente
- Comparativo competitivo incluido

## Output Esperado
```
## Relatorio de Social Listening
### Periodo: [datas]
### Volume de Mencoes: [total e por plataforma]
### Sentimento: [% positivo/negativo/neutro]
### Temas Recorrentes: [top 10]
### Share of Voice: [vs. concorrentes]
### Influenciadores: [top advogados e criticos]
### Alertas: [temas criticos]
### Recomendacoes: [acoes sugeridas]
```

## Registro
- `data/research/social-listening/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: palavras-chave definidas, acesso a ferramentas de social listening confirmado, periodo de analise definido
- Gate de saida: minimo 3 plataformas monitoradas, classificacao de sentimento consistente, comparativo competitivo incluido
- Score minimo: GREEN (>=80%) na validacao de completude e consistencia da analise

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre classificacao de sentimento → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (plataformas faltantes, classificacao inconsistente, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: briefing do projeto, category-and-competitor-research
- Downstream: voice-of-customer-mining, social-sentiment-analysis, trend-and-cultural-context
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de plataformas monitoradas
- Volume total de mencoes classificadas
- Share of voice vs. concorrentes
