# Consistency Review
> Revisao de consistencia da marca em todos os pontos de contato.

## Objetivo
Auditar a consistencia de aplicacao da marca em todos os touchpoints — identificando desvios, violacoes e oportunidades de melhoria — garantindo que a experiencia de marca seja uniforme.

## Agentes
- **brand-chief** — lidera a revisao de consistencia
- **byron-sharp** — avalia distinctive assets
- **alina-wheeler** — avalia consistencia visual

## Inputs
- Brand Guidelines atuais
- Touchpoint inventory
- Distinctive Assets Registry
- Amostras de materiais atuais por touchpoint

## Passos
1. Coletar amostras de todos os touchpoints ativos
2. Comparar cada amostra com brand guidelines
3. Avaliar uso correto dos distinctive assets
4. Classificar desvios por severidade (critico, moderado, leve)
5. Identificar touchpoints consistentes (benchmarks)
6. Calcular score de consistencia geral
7. Priorizar correcoes por impacto
8. Documentar violacoes e plano de correcao

## Frameworks Obrigatorios
- brand-consistency-model
- distinctive-assets-system

## Checklists de Qualidade
- distinctive-assets-quality
- brand-guidelines-quality

## Output Esperado
```
## Consistency Review
### Score Geral: [percentual de consistencia]
### Touchpoints Consistentes: [lista]
### Desvios Criticos: [lista com evidencia]
### Desvios Moderados: [lista]
### Desvios Leves: [lista]
### Violacoes de Distinctive Assets: [detalhe]
### Plano de Correcao: [prioridades e responsaveis]
```

## Registro
- `data/registries/brand-violations-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines atuais disponiveis, touchpoint inventory concluido, amostras de materiais coletadas
- Gate de saida: score GREEN (>=80%) nos checklists distinctive-assets-quality e brand-guidelines-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre byron-sharp e alina-wheeler sobre classificacao de desvios → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (amostras insuficientes, classificacao inconsistente, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: touchpoint-migration, brand-guidelines-creation, launch-coordination
- Downstream: brand-governance-enforcement, update-brand-guidelines
- Cross-squad: todos os squads afetados por violacoes (notificacao de correcao)

### Metricas
- Score de consistencia geral (% de touchpoints consistentes)
- Numero de desvios criticos vs. moderados vs. leves
- % de violacoes corrigidas no prazo
