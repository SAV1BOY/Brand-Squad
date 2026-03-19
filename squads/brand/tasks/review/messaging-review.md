# Messaging Review
> Revisao critica da messaging e comunicacao verbal da marca.

## Objetivo
Avaliar a clareza, consistencia e eficacia de toda a comunicacao verbal da marca — messaging house, copy, tagline e comunicacoes — garantindo alinhamento com a estrategia e maximo impacto.

## Agentes
- **donald-miller** — lidera a revisao de messaging
- **brand-chief** — aprovacao final

## Inputs
- Messaging House
- StoryBrand BrandScript
- Copy de canais ativos (site, social, email, etc.)
- Brand Voice Guide
- Feedback de performance de comunicacao

## Passos
1. Revisar messaging house contra criterios de qualidade
2. Avaliar clareza da mensagem central (teste de 5 segundos)
3. Verificar consistencia da messaging entre canais
4. Testar alinhamento do copy com brand voice
5. Avaliar eficacia do StoryBrand script
6. Identificar inconsistencias e mensagens confusas
7. Testar stickiness das mensagens-chave
8. Documentar ajustes recomendados

## Frameworks Obrigatorios
- miller-storybrand-sb7
- messaging-house

## Checklists de Qualidade
- brand-messaging-quality
- miller/messaging-clarity-audit

## Output Esperado
```
## Messaging Review
### Messaging House: [aprovada / ajuste necessario]
### Clareza (teste 5s): [pass/fail]
### Consistencia entre Canais: [score]
### Brand Voice Alignment: [score]
### StoryBrand Script: [eficaz / ajuste necessario]
### Stickiness: [score SUCCESs]
### Ajustes Recomendados: [lista priorizada]
### Status Final: [aprovado / revisao necessaria]
```

## Registro
- `data/registries/brand-claims-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: messaging house concluida, StoryBrand BrandScript disponivel, copy de canais ativos coletado
- Gate de saida: score GREEN (>=80%) nos checklists brand-messaging-quality e miller/messaging-clarity-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre qualidade do messaging → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief direcionado ao agente responsavel pelo componente falho (messaging house → donald-miller, stickiness → miller-sticky-brand)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: messaging-house-development, storybrand-script, brand-voice-development
- Downstream: campaign-activation-brief, website-brand-implementation
- Cross-squad: copy squad (ajustes de messaging comunicados)

### Metricas
- Score de clareza no teste de 5 segundos
- Score de stickiness (SUCCESs) por mensagem-chave
- % de consistencia da messaging entre canais
