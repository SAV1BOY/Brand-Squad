# Naming Workshop
> Workshop estruturado de geracao de nomes para marca ou produto.

## Objetivo
Conduzir um workshop criativo e estrategico para gerar uma long list robusta de opcoes de nome, utilizando tecnicas diversas de geracao e criterios claros de avaliacao.

## Agentes
- **naming-strategist** — lidera o workshop e geracao
- **al-ries** — valida potencial estrategico e de posicionamento
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Naming brief preenchido e aprovado
- Posicionamento da marca definido
- Brand archetypes e personalidade
- Criterios de avaliacao definidos
- Restricoes legais e linguisticas

## Passos
1. Revisar naming brief e criterios de avaliacao
2. Aplicar tecnicas de geracao (metaforas, neologismos, acronimos, etc.)
3. Gerar pelo menos 100 opcoes brutas
4. Fazer primeira filtragem por criterios eliminatorios
5. Agrupar por familia/abordagem
6. Selecionar 50-70 nomes para long list
7. Aplicar naming-decision-matrix preliminar
8. Documentar long list com justificativas

## Frameworks Obrigatorios
- naming-systems
- naming-spectrum
- naming-decision-matrix

## Checklists de Qualidade
- naming/naming-brief-checklist
- naming/naming-shortlist-checklist
- naming-quality

## Output Esperado
```
## Resultado do Naming Workshop
### Criterios de Avaliacao: [lista de criterios]
### Tecnicas Utilizadas: [lista]
### Total Gerado: [numero]
### Long List: [50-70 nomes com categoria]
### Familias Identificadas: [agrupamentos]
### Favoritos Preliminares: [top 15-20]
### Proximos Passos: [shortlist e scoring]
```

## Registro
- `data/registries/naming-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: naming brief preenchido e aprovado, posicionamento definido, criterios de avaliacao acordados
- Gate de saida: score GREEN (>=80%) nos checklists naming/naming-brief-checklist, naming/naming-shortlist-checklist e naming-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre naming-strategist e al-ries sobre potencial estrategico dos nomes → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (long list insuficiente, criterios nao aplicados, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: positioning-development, brand-archetype-selection, brand-architecture-design
- Downstream: naming-shortlist-and-scoring, naming-review
- Cross-squad: nenhum (task interna de identidade)

### Metricas
- Numero de nomes gerados na long list
- Numero de familias/abordagens identificadas
- % de nomes que passaram na filtragem por criterios eliminatorios
