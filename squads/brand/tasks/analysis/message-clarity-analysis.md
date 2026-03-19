# Message Clarity Analysis
> Analise de clareza e eficacia das mensagens da marca em todos os canais.

## Objetivo
Avaliar se as mensagens da marca estao sendo compreendidas, lembradas e motivando a acao desejada — testando clareza, recall e persuasao em diferentes canais e audiencias.

## Agentes
- **donald-miller** — lidera a analise de clareza
- **miller-sticky-brand** — avalia stickiness
- **brand-chief** — orquestracao e validacao

## Inputs
- Messaging House atual
- Copy de canais ativos
- Dados de performance de comunicacao (CTR, conversao)
- Feedback qualitativo de clientes

## Passos
1. Mapear mensagens-chave em cada canal
2. Aplicar teste de clareza (5 segundos) por mensagem
3. Avaliar recall das mensagens-chave
4. Medir compreensao da proposta de valor
5. Avaliar stickiness (framework SUCCESs)
6. Analisar metricas de performance (CTR, conversao)
7. Identificar mensagens confusas ou ineficazes
8. Recomendar reescrita ou ajuste

## Frameworks Obrigatorios
- miller-storybrand-sb7
- messaging-house

## Checklists de Qualidade
- miller/messaging-clarity-audit
- brand-messaging-quality

## Output Esperado
```
## Message Clarity Report
### Mensagens Avaliadas: [lista por canal]
### Teste de Clareza (5s): [pass/fail por mensagem]
### Recall: [% que lembra mensagem-chave]
### Compreensao da Proposta: [% que entende]
### Stickiness (SUCCESs): [score por mensagem]
### Performance: [CTR e conversao por canal]
### Mensagens a Reescrever: [lista priorizada]
### Recomendacoes: [ajustes especificos]
```

## Registro
- `data/registries/brand-claims-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: messaging house disponivel, copy de canais ativos coletado, dados de performance de comunicacao acessiveis
- Gate de saida: score GREEN (>=80%) nos checklists miller/messaging-clarity-audit e brand-messaging-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre donald-miller e miller-sticky-brand sobre avaliacao de stickiness → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (teste de clareza incompleto, metricas de performance ausentes, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: messaging-house-development, storybrand-script, campaign-activation-brief
- Downstream: messaging-review, brand-health-scorecard-analysis
- Cross-squad: copy squad (resultados de clareza para ajuste de copy)

### Metricas
- % de mensagens que passam no teste de 5 segundos
- Score medio de stickiness (SUCCESs) das mensagens-chave
- Correlacao entre clareza de mensagem e metricas de conversao
