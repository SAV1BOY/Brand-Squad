# Brand Voice Development
> Desenvolvimento do sistema de voz e tom da marca.

## Objetivo
Criar um guia completo de brand voice que defina como a marca fala, escreve e se comunica — incluindo principios de voz, espectro de tom, vocabulario e exemplos praticos para cada contexto.

## Agentes
- **donald-miller** — lidera com foco em clareza de messaging
- **emily-heyward** — valida autenticidade e consistencia
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand archetype selecionado
- Personalidade da marca definida
- Dados de VoC (linguagem real do cliente)
- Posicionamento e messaging house

## Passos
1. Definir principios de voz (3-4 adjetivos-guia)
2. Descrever cada principio com "Somos X, nao Y"
3. Definir espectro de tom (formal-informal, serio-divertido, etc.)
4. Criar vocabulario da marca (palavras que usamos e evitamos)
5. Desenvolver exemplos para cada contexto (site, social, email, etc.)
6. Criar guia de adaptacao de tom por canal
7. Desenvolver exercicios de calibracao de voz
8. Documentar brand voice guide completo

## Frameworks Obrigatorios
- verbal-identity-system
- brand-lexicon-framework

## Checklists de Qualidade
- brand-voice-quality
- miller/messaging-clarity-audit

## Output Esperado
```
## Brand Voice Guide
### Principios de Voz: [3-4 principios com descricao]
### Espectro de Tom: [escala por dimensao]
### Vocabulario: [palavras usamos / palavras evitamos]
### Tom por Canal: [adaptacoes por contexto]
### Exemplos Praticos: [antes/depois por canal]
### Exercicios de Calibracao: [para equipe]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand archetype selecionado, dados de VoC disponiveis, posicionamento e messaging house definidos
- Gate de saida: score GREEN (>=80%) nos checklists brand-voice-quality e miller/messaging-clarity-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre donald-miller e emily-heyward sobre principios de voz → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (principios vagos, exemplos insuficientes, vocabulario incompleto, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-archetype-selection, voice-of-customer-mining, messaging-house-development
- Downstream: verbal-identity-development, brand-guidelines-creation, brand-lexicon-development
- Cross-squad: copy squad (brand voice guide como referencia central)

### Metricas
- Numero de principios de voz definidos com descricao "Somos X, nao Y"
- Numero de exemplos praticos por canal
- Completude do vocabulario (palavras usamos/evitamos)
