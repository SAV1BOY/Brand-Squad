# Category and Competitor Research
> Pesquisa aprofundada de categoria e mapeamento competitivo para fundamentar decisoes de posicionamento.

## Objetivo
Mapear o landscape competitivo completo — players, posicionamentos, claims, distinctive assets e category entry points — gerando inteligencia para diferenciacao estrategica.

## Agentes
- **al-ries** — lider da analise competitiva e posicionamento
- **byron-sharp** — mental availability e category entry points
- **brand-chief** — orquestracao e validacao

## Inputs
- Briefing do projeto com categoria definida
- Lista preliminar de concorrentes diretos e indiretos
- Dados de market share (se disponiveis)
- Canais e touchpoints da categoria

## Passos
1. Definir escopo da categoria e criterios de inclusao de concorrentes
2. Mapear todos os players relevantes (diretos, indiretos, substitutos)
3. Analisar posicionamento de cada concorrente (claim, promessa, tom)
4. Identificar category entry points da categoria (Byron Sharp)
5. Mapear distinctive assets dos concorrentes
6. Identificar white spaces e oportunidades de diferenciacao
7. Consolidar em mapa competitivo visual
8. Documentar insights e recomendacoes

## Frameworks Obrigatorios
- ries-positioning
- category-entry-points
- competitive-framing

## Checklists de Qualidade
- ries/positioning-statement-audit
- sharp/mental-availability-audit

## Output Esperado
```
## Mapa Competitivo
### Concorrentes Diretos: [lista com posicionamento de cada]
### Concorrentes Indiretos: [lista]
### Category Entry Points: [lista priorizada]
### White Spaces Identificados: [oportunidades]
### Recomendacoes: [insights para posicionamento]
```

## Registro
- `data/research/competitor-research/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: briefing com categoria definida, lista preliminar de concorrentes disponivel
- Gate de saida: score GREEN (>=80%) nos checklists ries/positioning-statement-audit e sharp/mental-availability-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre al-ries e byron-sharp sobre categorizacao → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas nos criterios de mapeamento competitivo
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: briefing inicial do projeto
- Downstream: positioning-development, competitive-repositioning, category-creation-strategy
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de concorrentes mapeados (diretos + indiretos)
- Numero de category entry points identificados
- Numero de white spaces documentados
