# Guidelines Review
> Revisao critica do brand book e guidelines de marca.

## Objetivo
Avaliar a completude, clareza e usabilidade das brand guidelines — garantindo que qualquer pessoa consiga aplicar a marca corretamente usando o documento como referencia unica.

## Agentes
- **alina-wheeler** — lidera a revisao tecnica
- **emily-heyward** — avalia usabilidade e clareza
- **brand-chief** — aprovacao final

## Inputs
- Brand Guidelines/Brand Book
- Feedback de usuarios das guidelines
- Touchpoints atuais para comparacao
- Distinctive Assets Registry

## Passos
1. Revisar completude (todos os capitulos necessarios)
2. Avaliar clareza das instrucoes e regras
3. Testar usabilidade (alguem novo consegue aplicar?)
4. Verificar exemplos visuais suficientes
5. Validar do's & don'ts com casos reais
6. Confirmar alinhamento com distinctive assets registry
7. Verificar secao de governanca e contatos
8. Documentar aprovacao ou revisoes necessarias

## Frameworks Obrigatorios
- wheeler-brand-identity-process
- brand-consistency-model

## Checklists de Qualidade
- wheeler/brand-guidelines-audit
- brand-guidelines-quality

## Output Esperado
```
## Guidelines Review
### Completude: [capitulos presentes / faltantes]
### Clareza: [score de usabilidade]
### Exemplos Visuais: [suficientes / insuficientes]
### Do's & Don'ts: [completos / gaps]
### Governanca: [clara / ajuste necessario]
### Gaps Identificados: [lista]
### Status Final: [aprovado / revisao necessaria]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines/brand book finalizado, feedback de usuarios coletado
- Gate de saida: score GREEN (>=80%) nos checklists wheeler/brand-guidelines-audit e brand-guidelines-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre alina-wheeler e emily-heyward sobre usabilidade → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (capitulos incompletos, instrucoes confusas, exemplos insuficientes, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-guidelines-creation
- Downstream: update-brand-guidelines, touchpoint-migration, partner-alignment
- Cross-squad: todos os squads (guidelines aprovadas sao distribuidas para uso)

### Metricas
- Score de completude (capitulos presentes vs. requeridos)
- Score de usabilidade (teste com usuario novo)
- Numero de gaps identificados e corrigidos
