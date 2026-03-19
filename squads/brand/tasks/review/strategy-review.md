# Strategy Review
> Revisao critica da estrategia de marca para validacao e refinamento.

## Objetivo
Avaliar a robustez, coerencia e eficacia da estrategia de marca — posicionamento, proposito, promessa e arquitetura — garantindo que esteja alinhada com objetivos de negocio e diferenciada no mercado.

## Agentes
- **brand-chief** — lidera a revisao
- **david-aaker** — avalia brand identity system
- **al-ries** — avalia posicionamento e foco

## Inputs
- Brand Strategy Document completo
- Positioning Statement
- Brand Purpose e Promise
- Brand Architecture
- Dados de mercado e concorrencia

## Passos
1. Revisar positioning statement contra criterios de qualidade
2. Avaliar clareza e diferenciacao do posicionamento
3. Validar alinhamento entre purpose, promise e positioning
4. Avaliar coerencia da brand architecture
5. Testar robustez contra movimentos competitivos
6. Verificar alinhamento com objetivos de negocio
7. Identificar gaps e inconsistencias
8. Documentar aprovacao ou ajustes necessarios

## Frameworks Obrigatorios
- aaker-brand-identity-system
- ries-positioning

## Checklists de Qualidade
- brand-strategy-quality
- positioning-quality

## Output Esperado
```
## Strategy Review
### Posicionamento: [aprovado / ajuste necessario]
### Purpose: [aprovado / ajuste necessario]
### Promise: [aprovado / ajuste necessario]
### Architecture: [aprovado / ajuste necessario]
### Gaps Identificados: [lista]
### Ajustes Recomendados: [lista priorizada]
### Status Final: [aprovado / revisao necessaria]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand strategy document completo, positioning statement, brand purpose e promise disponiveis
- Gate de saida: score GREEN (>=80%) nos checklists brand-strategy-quality e positioning-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief (como lider da revisao, escala para HRM Chief nivel 3)
- Se conflito entre david-aaker e al-ries sobre avaliacao da estrategia → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief direcionado ao agente responsavel pelo componente falho (positioning → al-ries, identity system → david-aaker)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: positioning-development, define-brand-purpose, define-brand-promise, brand-architecture-design
- Downstream: identity-review (layer gate strategy→identity), brand-guidelines-creation
- Cross-squad: nenhum (task de revisao interna — gate obrigatorio antes de avancar para identity layer)

### Metricas
- % de componentes estrategicos aprovados na primeira revisao
- Numero de gaps e inconsistencias identificados
- Tempo entre submissao e aprovacao final
