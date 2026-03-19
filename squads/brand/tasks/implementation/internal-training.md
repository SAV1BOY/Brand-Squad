# Internal Training
> Treinamento interno de marca para garantir alinhamento e adocao por toda a organizacao.

## Objetivo
Capacitar colaboradores de todos os niveis a compreender, viver e representar a marca corretamente — garantindo que a experiencia interna seja coerente com a promessa externa.

## Agentes
- **denise-yohn** — lidera o programa de treinamento
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Guidelines completas
- Brand Voice Guide
- Brand Story e Manifesto
- Messaging House
- Materiais de onboarding existentes

## Passos
1. Definir publico-alvo do treinamento (niveis e departamentos)
2. Criar conteudo modular (proposito, posicionamento, voz, visual)
3. Desenvolver exercicios praticos de aplicacao
4. Criar quiz de validacao de conhecimento
5. Realizar sessoes de treinamento (presencial/virtual)
6. Distribuir brand pocket guide (resumo rapido)
7. Estabelecer programa de brand ambassadors
8. Medir adocao e compreensao pos-treinamento

## Frameworks Obrigatorios
- yohn-brand-as-business
- yohn-fusion
- activation-layer

## Checklists de Qualidade
- yohn/brand-as-business-audit
- internal-rollout-quality

## Output Esperado
```
## Programa de Treinamento Interno
### Modulos: [lista com duracao]
### Publico: [departamentos e niveis]
### Materiais: [apresentacoes, pocket guide, quiz]
### Cronograma: [datas e sessoes]
### Metricas de Adocao: [como medir]
### Brand Ambassadors: [criterios e selecionados]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines completas, brand voice guide e brand story disponiveis, materiais de onboarding existentes revisados
- Gate de saida: score GREEN (>=80%) nos checklists yohn/brand-as-business-audit e internal-rollout-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre conteudo do treinamento → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (modulos incompletos, quiz inadequado, adocao baixa, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-guidelines-creation, brand-voice-development, brand-story-manifesto
- Downstream: launch-coordination, brand-ambassador-program
- Cross-squad: people squad (integracao com programas de treinamento corporativo)

### Metricas
- % de colaboradores treinados por departamento
- Score medio no quiz de validacao de conhecimento
- % de adocao pos-treinamento (uso correto da marca)
