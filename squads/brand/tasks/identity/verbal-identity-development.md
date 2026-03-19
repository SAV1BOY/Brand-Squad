# Verbal Identity Development
> Desenvolvimento do sistema completo de identidade verbal da marca.

## Objetivo
Criar o sistema integrado de identidade verbal — nome, tagline, tom de voz, vocabulario, lexicon e padroes de escrita — garantindo coerencia e reconhecibilidade em toda comunicacao textual da marca.

## Agentes
- **naming-strategist** — lidera o sistema verbal
- **donald-miller** — valida clareza e messaging
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Nome da marca definido
- Tagline aprovada
- Brand voice guide
- Messaging house
- Brand personality e archetype

## Passos
1. Consolidar todos os elementos verbais ja definidos
2. Desenvolver brand lexicon (vocabulario proprietario)
3. Criar padroes de escrita por canal
4. Definir hierarquia verbal (headlines, body, CTAs)
5. Desenvolver templates de copy por formato
6. Criar glossario de termos da marca
7. Testar consistencia entre canais
8. Documentar verbal identity system completo

## Frameworks Obrigatorios
- verbal-identity-system
- brand-lexicon-framework
- tagline-architecture

## Checklists de Qualidade
- brand-voice-quality
- naming-quality

## Output Esperado
```
## Verbal Identity System
### Nome: [e regras de uso]
### Tagline: [e variacoes]
### Principios de Voz: [resumo]
### Brand Lexicon: [vocabulario proprietario]
### Padroes por Canal: [regras por formato]
### Hierarquia Verbal: [headline > body > CTA]
### Glossario: [termos da marca]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: nome da marca definido, tagline aprovada, brand voice guide concluido, messaging house disponivel
- Gate de saida: score GREEN (>=80%) nos checklists brand-voice-quality e naming-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre naming-strategist e donald-miller sobre padroes verbais → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (lexicon inconsistente, hierarquia verbal confusa, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: naming-shortlist-and-scoring, tagline-development, brand-voice-development
- Downstream: brand-guidelines-creation, brand-lexicon-development
- Cross-squad: copy squad (verbal identity como referencia), product squad (verbal identity para UX writing)

### Metricas
- Numero de elementos verbais consolidados no sistema
- Completude do brand lexicon (termos proprietarios definidos)
- Consistencia entre canais testada (pass/fail)
