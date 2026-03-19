# Brand Archetype Selection
> Selecao e ativacao do arquetipo de marca para guiar personalidade e comunicacao.

## Objetivo
Identificar e selecionar o arquetipo primario (e secundario) da marca, traduzindo-o em diretrizes concretas de personalidade, tom de voz e comportamento que orientem toda a comunicacao.

## Agentes
- **archetype-consultant** — lidera a selecao e ativacao
- **jean-noel-kapferer** — valida coerencia com identity prism
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Strategy Document
- Dados de percepcao de marca
- Customer interviews (como clientes descrevem a marca)
- Valores e cultura organizacional

## Passos
1. Apresentar os 12 arquetipos e suas caracteristicas
2. Avaliar fit de cada arquetipo com a marca
3. Selecionar arquetipo primario (dominante)
4. Selecionar arquetipo secundario (complementar)
5. Definir blend e proporcao (ex: 70/30)
6. Traduzir em tracos de personalidade especificos
7. Definir implicacoes para tom de voz e comunicacao
8. Validar coerencia com Kapferer Identity Prism

## Frameworks Obrigatorios
- brand-archetypes-system
- archetype-activation
- kapferer-brand-identity-prism

## Checklists de Qualidade
- archetypes/archetype-selection-checklist
- archetypes/archetype-consistency-checklist

## Output Esperado
```
## Brand Archetype Guide
### Arquetipo Primario: [nome + justificativa]
### Arquetipo Secundario: [nome + justificativa]
### Blend: [proporcao e como se manifesta]
### Tracos de Personalidade: [lista]
### Tom de Voz: [implicacoes concretas]
### Exemplos de Comportamento: [como a marca age]
### O Que a Marca NAO E: [anti-arquetipos]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand strategy document disponivel, dados de percepcao de marca coletados, valores e cultura organizacional documentados
- Gate de saida: score GREEN (>=80%) nos checklists archetypes/archetype-selection-checklist e archetypes/archetype-consistency-checklist
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre archetype-consultant e jean-noel-kapferer sobre coerencia com identity prism → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (arquetipo nao coerente, blend confuso, implicacoes vagas, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: define-brand-purpose, perception-study, stakeholder-interviews
- Downstream: brand-voice-development, visual-identity-direction, brand-story-manifesto
- Cross-squad: copy squad (arquetipos para guiar tom de voz no copy)

### Metricas
- Clareza do blend primario/secundario (proporcao definida)
- Numero de tracos de personalidade traduzidos em diretrizes concretas
- Coerencia com Kapferer Identity Prism (pass/fail)
