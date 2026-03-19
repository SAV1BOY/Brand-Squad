# Brand Ambassador Program
> Criacao e gestao do programa de embaixadores da marca.

## Objetivo
Estabelecer um programa estruturado de brand ambassadors — colaboradores que representam e evangelizam a marca internamente e externamente — ampliando o alcance e a autenticidade da comunicacao de marca.

## Agentes
- **denise-yohn** — lidera o programa de ambassadors
- **emily-heyward** — garante autenticidade na expressao
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Guidelines e Brand Voice Guide
- Resultados de employee brand perception
- Criterios de selecao de ambassadors
- Objetivos do programa

## Passos
1. Definir objetivos e escopo do programa
2. Estabelecer criterios de selecao de ambassadors
3. Identificar e recrutar ambassadors potenciais
4. Criar programa de capacitacao especifico
5. Desenvolver toolkit do ambassador (conteudo, templates)
6. Definir metricas de participacao e impacto
7. Lancar programa com evento/kick-off
8. Monitorar, reconhecer e iterar

## Frameworks Obrigatorios
- yohn-brand-as-business
- activation-layer

## Checklists de Qualidade
- yohn/brand-as-business-audit
- internal-rollout-quality

## Output Esperado
```
## Brand Ambassador Program
### Objetivos: [metas do programa]
### Criterios de Selecao: [perfil ideal]
### Ambassadors Selecionados: [lista e departamentos]
### Programa de Capacitacao: [modulos e cronograma]
### Toolkit: [materiais disponibilizados]
### Metricas: [como medir impacto]
### Reconhecimento: [programa de incentivos]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines e brand voice guide disponiveis, resultados de employee brand perception concluidos, criterios de selecao definidos
- Gate de saida: score GREEN (>=80%) nos checklists yohn/brand-as-business-audit e internal-rollout-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre denise-yohn e emily-heyward sobre criterios do programa → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (criterios vagos, toolkit incompleto, metricas nao definidas, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: internal-training, employee-brand-perception, brand-guidelines-creation
- Downstream: brand-governance-enforcement, consistency-review
- Cross-squad: people squad (integracao com programas de engajamento)

### Metricas
- Numero de ambassadors recrutados e capacitados
- Score de engajamento dos ambassadors no programa
- Impacto mensuravel na adocao da marca internamente
