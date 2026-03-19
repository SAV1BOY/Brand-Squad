# Brand Guidelines Creation
> Criacao do brand book completo com todas as diretrizes de uso da marca.

## Objetivo
Produzir o documento definitivo de brand guidelines — cobrindo identidade visual, verbal, aplicacoes, do's & don'ts e regras de governanca — servindo como referencia unica para todos os usuarios da marca.

## Agentes
- **alina-wheeler** — lidera a criacao das guidelines
- **emily-heyward** — valida usabilidade e clareza
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Visual identity direction aprovada
- Brand voice guide
- Messaging house
- Distinctive assets registry
- Touchpoint inventory

## Passos
1. Definir estrutura e capitulos do brand book
2. Documentar proposito, posicionamento e valores
3. Detalhar sistema visual (logo, cores, tipografia, foto, layout)
4. Documentar sistema verbal (voz, tom, vocabulario)
5. Criar secao de aplicacoes (papelaria, digital, ambiente, etc.)
6. Desenvolver do's & don'ts com exemplos visuais
7. Incluir secao de governanca e aprovacao
8. Revisar, aprovar e distribuir

## Frameworks Obrigatorios
- wheeler-brand-identity-process
- heyward-obviousness-method

## Checklists de Qualidade
- wheeler/identity-system-audit
- wheeler/brand-guidelines-audit
- brand-guidelines-quality

## Output Esperado
```
## Brand Book — Estrutura
### 1. Essencia da Marca: [proposito, visao, valores]
### 2. Posicionamento: [statement e pilares]
### 3. Identidade Visual: [logo, cores, tipo, foto, layout]
### 4. Identidade Verbal: [voz, tom, vocabulario]
### 5. Aplicacoes: [por touchpoint]
### 6. Do's & Don'ts: [exemplos visuais]
### 7. Governanca: [aprovacao e contatos]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: visual identity direction aprovada, brand voice guide concluido, messaging house e distinctive assets registry disponiveis
- Gate de saida: score GREEN (>=80%) nos checklists wheeler/identity-system-audit, wheeler/brand-guidelines-audit e brand-guidelines-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre alina-wheeler e emily-heyward sobre usabilidade do brand book → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (capitulos incompletos, exemplos insuficientes, do's & don'ts vagos, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: visual-identity-direction, brand-voice-development, messaging-house-development, define-distinctive-assets
- Downstream: touchpoint-migration, internal-training, partner-alignment, guidelines-review
- Cross-squad: marketing squad, design squad, copy squad, product squad (brand book como referencia para todos)

### Metricas
- Numero de capitulos completos com exemplos visuais
- Score de usabilidade (teste com usuario novo)
- Cobertura de touchpoints nas aplicacoes documentadas
