# Distinctive Assets Recognition Analysis
> Analise de reconhecimento e eficacia dos distinctive assets da marca.

## Objetivo
Medir o nivel de reconhecimento e atribuicao correta de cada distinctive asset da marca — avaliando quais estao funcionando, quais precisam de reforco e quais devem ser descontinuados.

## Agentes
- **byron-sharp** — lidera a analise de recognition
- **brand-chief** — orquestracao e validacao

## Inputs
- Distinctive Assets Registry
- Dados de pesquisa de reconhecimento
- Dados de eye-tracking ou attention (se disponiveis)
- Dados de uso dos assets em touchpoints

## Passos
1. Listar todos os distinctive assets em uso
2. Medir fame (% que reconhece o asset)
3. Medir uniqueness (% que atribui a marca correta)
4. Plotar na Distinctive Asset Grid (fame x uniqueness)
5. Classificar: invest, maintain, avoid, test
6. Comparar com medicao anterior (evolucao)
7. Identificar assets subutilizados ou inconsistentes
8. Recomendar acoes por asset

## Frameworks Obrigatorios
- distinctive-assets-system
- sharp-mental-availability

## Checklists de Qualidade
- sharp/distinctive-assets-audit

## Output Esperado
```
## Distinctive Assets Recognition Report
### Assets Avaliados: [lista]
### Distinctive Asset Grid:
  - Invest (alto fame, alta uniqueness): [assets]
  - Maintain (performance boa): [assets]
  - Test (potencial nao comprovado): [assets]
  - Avoid (baixo desempenho): [assets]
### Evolucao: [comparativo com periodo anterior]
### Recomendacoes por Asset: [acao especifica]
```

## Registro
- `data/registries/distinctive-assets-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: distinctive assets registry atualizado, dados de pesquisa de reconhecimento disponiveis
- Gate de saida: score GREEN (>=80%) no checklist sharp/distinctive-assets-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre classificacao de assets na grid → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (fame/uniqueness nao medidos, grid incompleta, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: define-distinctive-assets, maintain-distinctive-assets-registry
- Downstream: brand-health-scorecard-analysis, quarterly-brand-review
- Cross-squad: nenhum (analise interna de assets)

### Metricas
- Numero de assets avaliados com fame e uniqueness medidos
- % de assets classificados como invest ou maintain na grid
- Evolucao de reconhecimento vs. medicao anterior
