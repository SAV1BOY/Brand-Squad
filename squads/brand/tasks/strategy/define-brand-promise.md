# Define Brand Promise
> Definicao da promessa central da marca e suas razoes para acreditar (RTBs).

## Objetivo
Articular a promessa de valor unica da marca — o compromisso que faz com seu publico — acompanhada de razoes concretas para acreditar (RTBs) que sustentam a credibilidade da promessa.

## Agentes
- **donald-miller** — lidera a articulacao com clareza StoryBrand
- **david-aaker** — valida alinhamento com brand identity system
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Purpose definido
- Posicionamento da marca
- Dados de customer interviews e VoC
- Diferenciais competitivos identificados

## Passos
1. Revisar posicionamento e proposito definidos
2. Identificar beneficios funcionais e emocionais principais
3. Mapear reasons to believe (RTBs) concretas
4. Redigir opcoes de brand promise (3-5 versoes)
5. Testar clareza e memorabilidade de cada opcao
6. Validar que a promessa e entregavel e verificavel
7. Selecionar e refinar promessa final
8. Documentar com RTBs e prova

## Frameworks Obrigatorios
- brand-promise-and-rtb
- miller-storybrand-sb7

## Checklists de Qualidade
- brand-messaging-quality
- miller/messaging-clarity-audit

## Output Esperado
```
## Brand Promise
### Promessa: [declaracao em uma frase]
### Beneficio Funcional: [o que entrega]
### Beneficio Emocional: [como faz sentir]
### RTBs: [lista de razoes para acreditar]
### Prova: [evidencias concretas]
### Teste de Clareza: [pass/fail]
```

## Registro
- `data/registries/brand-claims-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand purpose e posicionamento definidos, dados de customer interviews e VoC disponiveis
- Gate de saida: score GREEN (>=80%) nos checklists brand-messaging-quality e miller/messaging-clarity-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre donald-miller e david-aaker sobre formulacao da promessa → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (promessa vaga, RTBs insuficientes, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: define-brand-purpose, positioning-development, customer-interviews
- Downstream: messaging-house-development, tagline-development, brand-story-manifesto
- Cross-squad: copy squad (brand promise para referencia de messaging)

### Metricas
- Score de clareza da promessa (teste de compreensao)
- Numero de RTBs concretas documentadas
- Pass/fail no teste de entregabilidade da promessa
