# StoryBrand Script
> Desenvolvimento do script StoryBrand SB7 completo da marca.

## Objetivo
Criar o script StoryBrand seguindo o framework SB7 de Donald Miller — posicionando o cliente como heroi e a marca como guia — resultando em uma narrativa clara que gera engajamento e conversao.

## Agentes
- **donald-miller** — lidera a criacao do script SB7
- **miller-sticky-brand** — refina para stickiness
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Dados de customer interviews (linguagem do cliente)
- Brand promise e posicionamento
- Dores e desejos do publico-alvo
- Messaging house (se ja existir)

## Passos
1. Definir o Heroi (cliente) e seu desejo
2. Identificar o Problema (externo, interno, filosofico)
3. Posicionar a Marca como Guia (empatia + autoridade)
4. Apresentar o Plano (3 passos simples)
5. Chamar para Acao (CTA direto e transicional)
6. Mostrar o Sucesso (transformacao positiva)
7. Mostrar o Fracasso (o que acontece sem agir)
8. Criar one-liner e BrandScript completo

## Frameworks Obrigatorios
- miller-storybrand-sb7
- miller-one-liner

## Checklists de Qualidade
- miller/storybrand-sb7-audit
- miller/one-liner-audit

## Output Esperado
```
## StoryBrand BrandScript
### Heroi: [quem e o cliente]
### Problema Externo: [dor tangivel]
### Problema Interno: [frustracao emocional]
### Problema Filosofico: [injustica maior]
### Guia (Empatia): [como a marca entende]
### Guia (Autoridade): [credenciais e provas]
### Plano: [3 passos]
### CTA Direto: [acao principal]
### CTA Transicional: [acao secundaria]
### Sucesso: [vida transformada]
### Fracasso: [consequencia da inacao]
### One-Liner: [frase unica]
```

## Registro
- `data/registries/brand-claims-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: dados de customer interviews disponiveis, brand promise e posicionamento definidos
- Gate de saida: score GREEN (>=80%) nos checklists miller/storybrand-sb7-audit e miller/one-liner-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre donald-miller e miller-sticky-brand sobre narrativa → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (heroi mal definido, plano confuso, CTA fraco, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: messaging-house-development, customer-interviews, define-brand-promise
- Downstream: brand-story-manifesto, campaign-activation-brief, website-brand-implementation
- Cross-squad: copy squad (BrandScript como referencia para copy), marketing squad (narrativa para campanhas)

### Metricas
- Completude dos 7 elementos SB7 (todos preenchidos)
- Score de clareza do one-liner (teste de compreensao)
- Alinhamento do script com dados reais do cliente (pass/fail)
