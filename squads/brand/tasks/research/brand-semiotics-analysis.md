# Brand Semiotics Analysis
> Analise semiotica dos signos, simbolos e codigos culturais da marca e da categoria.

## Objetivo
Decodificar os signos e simbolos utilizados pela marca e pela categoria — cores, formas, linguagem, rituais — identificando codigos culturais dominantes e oportunidades de diferenciacao semiotica.

## Agentes
- **jean-noel-kapferer** — lidera a analise semiotica
- **brand-chief** — orquestracao e validacao

## Inputs
- Materiais visuais e verbais da marca
- Materiais dos principais concorrentes
- Codigos visuais da categoria
- Contexto cultural do mercado-alvo

## Passos
1. Coletar corpus de analise (marca + concorrentes + categoria)
2. Identificar codigos visuais dominantes na categoria
3. Analisar signos da marca (denotacao e conotacao)
4. Mapear codigos verbais (tom, vocabulario, metaforas)
5. Identificar codigos culturais associados a categoria
6. Avaliar coerencia semiotica da marca
7. Identificar oportunidades de ruptura semiotica
8. Documentar recomendacoes para identidade

## Frameworks Obrigatorios
- brand-semiotics
- kapferer-brand-identity-prism

## Checklists de Qualidade
- kapferer/identity-prism-audit

## Output Esperado
```
## Relatorio de Analise Semiotica
### Codigos Visuais da Categoria: [dominantes e emergentes]
### Signos da Marca: [denotacao e conotacao]
### Codigos Verbais: [tom, vocabulario, metaforas]
### Coerencia Semiotica: [avaliacao]
### Oportunidades de Diferenciacao: [rupturas possiveis]
### Recomendacoes: [direcao semiotica para identidade]
```

## Registro
- `data/research/competitor-research/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: materiais visuais e verbais da marca e concorrentes coletados, contexto cultural do mercado-alvo documentado
- Gate de saida: score GREEN (>=80%) no checklist kapferer/identity-prism-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre interpretacao semiotica → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (codigos nao fundamentados, coerencia nao avaliada, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: category-and-competitor-research, brand-audit
- Downstream: visual-identity-direction, brand-archetype-selection, trend-and-cultural-context
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de codigos visuais e verbais identificados na categoria
- Numero de oportunidades de diferenciacao semiotica documentadas
- Score de coerencia semiotica da marca
