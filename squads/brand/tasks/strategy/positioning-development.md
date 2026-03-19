# Positioning Development
> Desenvolvimento do posicionamento estrategico da marca no mercado.

## Objetivo
Definir o posicionamento unico e defensavel da marca — para quem, em qual categoria, com qual diferencial e por qual razao — criando um territorio mental claro e distinto dos concorrentes.

## Agentes
- **al-ries** — lidera o posicionamento estrategico
- **marty-neumeier** — valida diferenciacao e brand gap
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Mapa competitivo (category-and-competitor-research)
- Dados de percepcao e associacoes
- Category entry points mapeados
- Customer interviews e VoC

## Passos
1. Revisar landscape competitivo e posicionamentos existentes
2. Identificar white spaces e oportunidades
3. Definir target audience especifico
4. Definir frame of reference (categoria)
5. Articular point of difference (diferencial)
6. Definir reasons to believe (RTBs)
7. Redigir positioning statement
8. Testar contra concorrentes e validar unicidade

## Frameworks Obrigatorios
- ries-positioning
- neumeier-brand-gap
- stp-segmentation-targeting-positioning

## Checklists de Qualidade
- ries/positioning-statement-audit
- neumeier/brand-gap-audit
- positioning-quality

## Output Esperado
```
## Positioning Statement
### Para: [target audience]
### Na categoria: [frame of reference]
### A marca [nome] e: [point of difference]
### Porque: [reasons to believe]
### Diferencial vs. Concorrentes: [comparativo]
### Teste de Unicidade: [pass/fail]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: mapa competitivo concluido, dados de percepcao e CEPs disponiveis, customer interviews realizadas
- Gate de saida: score GREEN (>=80%) nos checklists ries/positioning-statement-audit, neumeier/brand-gap-audit e positioning-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre al-ries e marty-neumeier sobre diferenciacao → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (posicionamento nao diferenciado, target generico, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: category-and-competitor-research, perception-study, category-entry-points-research, customer-interviews
- Downstream: define-brand-promise, messaging-house-development, brand-equity-plan, tagline-development
- Cross-squad: copy squad (positioning statement como referencia), marketing squad (posicionamento para campanhas)

### Metricas
- Score de unicidade do posicionamento vs. concorrentes
- Clareza do point of difference (teste de compreensao)
- Numero de white spaces explorados na definicao
