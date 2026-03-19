# Messaging House Development
> Desenvolvimento da messaging house completa da marca.

## Objetivo
Construir a messaging house — estrutura hierarquica de mensagens da marca — que organiza proposito, promessa, pilares de mensagem, proof points e key messages para cada audiencia.

## Agentes
- **donald-miller** — lidera o desenvolvimento com foco em clareza
- **miller-sticky-brand** — garante stickiness das mensagens
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Posicionamento definido
- Brand promise e RTBs
- Dados de customer interviews e VoC
- Perfis de audiencia/personas

## Passos
1. Revisar posicionamento, promessa e RTBs
2. Definir pilares de mensagem (3-4 pilares)
3. Desenvolver proof points para cada pilar
4. Criar key messages por audiencia
5. Testar clareza e memorabilidade
6. Aplicar filtro de stickiness (SUCCESs)
7. Validar consistencia com brand voice
8. Documentar messaging house completa

## Frameworks Obrigatorios
- miller-storybrand-sb7
- messaging-house
- brand-promise-and-rtb

## Checklists de Qualidade
- miller/storybrand-sb7-audit
- miller/messaging-clarity-audit
- brand-messaging-quality

## Output Esperado
```
## Messaging House
### Brand Purpose: [topo da casa]
### Brand Promise: [compromisso central]
### Pilares de Mensagem:
  - Pilar 1: [tema + proof points]
  - Pilar 2: [tema + proof points]
  - Pilar 3: [tema + proof points]
### Key Messages por Audiencia: [adaptacoes]
### Elevator Pitch: [versao 30 segundos]
### Teste de Stickiness: [score SUCCESs]
```

## Registro
- `data/registries/brand-claims-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: posicionamento definido, brand promise e RTBs aprovados, perfis de audiencia disponveis
- Gate de saida: score GREEN (>=80%) nos checklists miller/storybrand-sb7-audit, miller/messaging-clarity-audit e brand-messaging-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre donald-miller e miller-sticky-brand sobre pilares de mensagem → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (pilares sobrepostos, proof points genericos, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: positioning-development, define-brand-promise, voice-of-customer-mining
- Downstream: storybrand-script, tagline-development, brand-voice-development, campaign-activation-brief
- Cross-squad: copy squad (messaging house como referencia central), marketing squad (messaging para campanhas)

### Metricas
- Numero de pilares de mensagem com proof points concretos
- Score de stickiness (framework SUCCESs) das mensagens-chave
- Numero de key messages adaptadas por audiencia
