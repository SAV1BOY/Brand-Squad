# Perception Study
> Estudo quantitativo e qualitativo de percepcao de marca junto ao publico-alvo.

## Objetivo
Medir como a marca e percebida pelo publico-alvo em termos de awareness, associacoes, preferencia e lealdade — utilizando a CBBE Pyramid como framework principal.

## Agentes
- **kevin-keller** — lidera o desenho e analise do estudo
- **byron-sharp** — complementa com metricas de mental availability
- **brand-chief** — orquestracao e validacao

## Inputs
- Objetivos especificos do estudo
- Definicao do publico-alvo e amostra
- Hipoteses a validar
- Dados de percepcao anteriores (se existirem)

## Passos
1. Definir objetivos e hipoteses do estudo
2. Desenhar instrumento de pesquisa (survey CBBE)
3. Definir amostra e metodo de coleta
4. Aplicar pesquisa (quantitativa e/ou qualitativa)
5. Tabular e analisar dados coletados
6. Mapear posicao na CBBE Pyramid
7. Comparar com concorrentes (se dados disponiveis)
8. Documentar findings e recomendacoes

## Frameworks Obrigatorios
- keller-cbbe-pyramid
- sharp-mental-availability
- brand-salience-heuristics

## Checklists de Qualidade
- keller/cbbe-pyramid-audit

## Output Esperado
```
## Relatorio de Percepcao
### Metodologia: [quanti/quali, amostra, periodo]
### Awareness: [aided e unaided]
### Associacoes Principais: [top 5]
### Posicao CBBE: [nivel atingido na piramide]
### Mental Availability: [score e CEPs]
### Comparativo Competitivo: [ranking]
### Recomendacoes: [acoes priorizadas]
```

## Registro
- `data/research/survey-results/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: objetivos e hipoteses definidos, publico-alvo e amostra determinados
- Gate de saida: score GREEN (>=80%) no checklist keller/cbbe-pyramid-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre kevin-keller e byron-sharp sobre metodologia → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (amostra insuficiente, analise incompleta, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: briefing do projeto, customer-interviews
- Downstream: brand-association-mapping, positioning-development, brand-equity-plan
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Tamanho da amostra vs. minimo planejado
- Nivel atingido na CBBE Pyramid
- Score de mental availability calculado
