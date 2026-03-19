# Trend and Cultural Context
> Analise de tendencias culturais e contexto sociocultural relevante para a marca.

## Objetivo
Mapear tendencias culturais, comportamentais e sociais que impactam a categoria e o publico da marca — gerando insights para posicionamento, messaging e expressao de marca mais relevantes e contemporaneos.

## Agentes
- **jean-noel-kapferer** — lidera analise cultural e semiotica
- **denise-yohn** — conecta tendencias com cultura organizacional
- **brand-chief** — orquestracao e validacao

## Inputs
- Categoria e publico-alvo definidos
- Dados de social listening
- Relatorios de tendencias do setor
- Contexto cultural local e global

## Passos
1. Definir escopo de analise (macro e micro tendencias)
2. Mapear tendencias culturais relevantes para a categoria
3. Identificar tensoes culturais que a marca pode enderecar
4. Analisar como concorrentes estao respondendo as tendencias
5. Avaliar fit entre tendencias e DNA da marca
6. Identificar oportunidades de posicionamento cultural
7. Recomendar territorios culturais para a marca
8. Documentar com evidencias e exemplos

## Frameworks Obrigatorios
- brand-semiotics
- kapferer-brand-identity-prism

## Checklists de Qualidade
- kapferer/identity-prism-audit
- Tendencias documentadas com evidencias
- Fit com marca validado

## Output Esperado
```
## Relatorio de Tendencias e Contexto Cultural
### Macro Tendencias: [lista com impacto na categoria]
### Micro Tendencias: [lista com relevancia local]
### Tensoes Culturais: [oportunidades para a marca]
### Resposta dos Concorrentes: [como estao se posicionando]
### Territorios Recomendados: [para a marca explorar]
### Riscos: [tendencias a evitar]
```

## Registro
- `data/research/competitor-research/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: categoria e publico-alvo definidos, dados de social listening disponiveis, relatorios de tendencias coletados
- Gate de saida: score GREEN (>=80%) no checklist kapferer/identity-prism-audit, tendencias documentadas com evidencias e fit validado
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre jean-noel-kapferer e denise-yohn sobre relevancia de tendencias → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (tendencias sem evidencia, fit nao validado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: category-and-competitor-research, social-listening-analysis
- Downstream: positioning-development, brand-archetype-selection, visual-identity-direction
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de tendencias mapeadas com evidencias concretas
- Numero de territorios culturais recomendados para a marca
- % de tendencias com fit validado contra DNA da marca
