# Naming Shortlist and Scoring
> Selecao e pontuacao final dos melhores nomes candidatos.

## Objetivo
Reduzir a long list a uma short list de 5-10 nomes finalistas, pontuar cada um com criterios objetivos, e selecionar o nome vencedor apos verificacoes de disponibilidade legal e digital.

## Agentes
- **naming-strategist** — lidera a avaliacao e scoring
- **brand-chief** — orquestracao e decisao final

## Inputs
- Long list do naming workshop
- Naming decision matrix com criterios
- Dados de disponibilidade de dominios
- Verificacao legal preliminar

## Passos
1. Revisar long list e criterios de avaliacao
2. Aplicar scoring na naming-decision-matrix (todos os criterios)
3. Selecionar top 10 para short list
4. Verificar disponibilidade de dominios e handles
5. Realizar screening legal preliminar (INPI/USPTO)
6. Testar pronunciabilidade e memorabilidade
7. Rankear e selecionar top 3 finalistas
8. Documentar decisao final com justificativa

## Frameworks Obrigatorios
- naming-systems
- naming-decision-matrix

## Checklists de Qualidade
- naming/naming-shortlist-checklist
- naming/naming-testing-checklist
- naming/naming-legal-screening-checklist

## Output Esperado
```
## Naming Shortlist & Scoring
### Criterios e Pesos: [matriz de avaliacao]
### Short List (Top 10): [nome + score total]
### Disponibilidade Digital: [dominios e handles]
### Status Legal: [screening por nome]
### Top 3 Finalistas: [ranking com justificativa]
### Nome Recomendado: [vencedor + fundamentacao]
```

## Registro
- `data/registries/naming-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: long list do naming workshop disponivel, naming decision matrix com criterios definidos
- Gate de saida: score GREEN (>=80%) nos checklists naming/naming-shortlist-checklist, naming/naming-testing-checklist e naming/naming-legal-screening-checklist
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre ranking de nomes → brand-chief arbitra com base na decision matrix
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (scoring inconsistente, verificacao legal incompleta, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: naming-workshop
- Downstream: naming-review, verbal-identity-development, brand-guidelines-creation
- Cross-squad: product squad (naming de produto, se aplicavel)

### Metricas
- Numero de nomes na short list com scoring completo
- % de nomes com verificacao legal concluida
- Disponibilidade digital confirmada dos top 3 finalistas
