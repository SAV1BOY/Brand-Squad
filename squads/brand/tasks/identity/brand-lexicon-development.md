# Brand Lexicon Development
> Desenvolvimento do lexicon proprietario da marca.

## Objetivo
Criar um vocabulario unico e proprietario da marca — termos, expressoes e nomenclaturas exclusivas — que reforce a identidade verbal, diferencie a comunicacao e crie senso de pertencimento.

## Agentes
- **naming-strategist** — lidera a criacao do lexicon
- **donald-miller** — valida clareza e usabilidade
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Verbal identity system
- Brand voice guide
- Dados de VoC (linguagem do cliente)
- Terminologia do setor
- Brand personality e archetype

## Passos
1. Mapear terminologia atual do setor e da marca
2. Identificar oportunidades de nomenclatura proprietaria
3. Criar termos para produtos, features e experiencias
4. Desenvolver expressoes e giros de linguagem da marca
5. Definir lista de palavras proibidas e substituicoes
6. Testar compreensao com publico-alvo
7. Criar guia de uso com exemplos
8. Documentar brand lexicon completo

## Frameworks Obrigatorios
- brand-lexicon-framework
- verbal-identity-system

## Checklists de Qualidade
- brand-voice-quality
- Termos testados quanto a compreensao
- Consistencia com brand voice validada

## Output Esperado
```
## Brand Lexicon
### Termos Proprietarios: [lista com definicao e uso]
### Nomenclatura de Produtos: [padroes]
### Expressoes da Marca: [frases e giros de linguagem]
### Palavras Proibidas: [lista com substituicoes]
### Guia de Uso: [quando e como usar cada termo]
### Exemplos em Contexto: [aplicacoes reais]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: verbal identity system disponivel, brand voice guide concluido, dados de VoC coletados
- Gate de saida: score GREEN (>=80%) no checklist brand-voice-quality, termos testados quanto a compreensao
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre naming-strategist e donald-miller sobre clareza dos termos → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (termos incompreensiveis, lista de proibidos incompleta, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: verbal-identity-development, brand-voice-development, voice-of-customer-mining
- Downstream: brand-guidelines-creation, update-brand-guidelines
- Cross-squad: copy squad (lexicon como referencia de vocabulario), product squad (nomenclatura para produtos e features)

### Metricas
- Numero de termos proprietarios criados e testados
- % de termos que passaram no teste de compreensao
- Completude do guia de uso com exemplos em contexto
