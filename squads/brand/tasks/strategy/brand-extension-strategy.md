# Brand Extension Strategy
> Estrategia de extensao da marca para novos territorios, categorias ou segmentos.

## Objetivo
Avaliar e planejar a extensao da marca para novos territorios — analisando fit perceptual, risco de diluicao e modelo de arquitetura — garantindo que o equity da marca-mae seja preservado e potencializado.

## Agentes
- **david-aaker** — lidera a analise de portfolio e arquitetura
- **kevin-keller** — avalia transferencia de equity e fit
- **al-ries** — valida foco e risco de diluicao
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Architecture atual
- Dados de brand equity e percepcao
- Business case da extensao
- Dados da nova categoria/segmento

## Passos
1. Avaliar forca do equity da marca-mae
2. Analisar fit perceptual entre marca e nova categoria
3. Avaliar risco de diluicao do equity
4. Analisar concorrencia na nova categoria
5. Definir modelo de extensao (line, category, brand stretch)
6. Definir papel na brand architecture
7. Testar conceito com publico-alvo
8. Documentar estrategia e decisao go/no-go

## Frameworks Obrigatorios
- aaker-brand-identity-system
- keller-cbbe-pyramid
- brand-portfolio-strategy

## Checklists de Qualidade
- aaker/aaker-architecture-audit
- keller/cbbe-pyramid-audit

## Output Esperado
```
## Estrategia de Extensao
### Oportunidade: [nova categoria/segmento]
### Fit Perceptual: [score e analise]
### Risco de Diluicao: [alto/medio/baixo + mitigacao]
### Modelo de Extensao: [line/category/stretch]
### Arquitetura: [relacao com marca-mae]
### Decisao: [go/no-go com fundamentacao]
### Proximos Passos: [se go]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand architecture definida, dados de brand equity e percepcao disponiveis, business case documentado
- Gate de saida: score GREEN (>=80%) nos checklists aaker/aaker-architecture-audit e keller/cbbe-pyramid-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre david-aaker, kevin-keller e al-ries sobre risco de diluicao → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (fit perceptual nao comprovado, risco de diluicao subestimado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-architecture-design, brand-equity-plan, positioning-development
- Downstream: naming-workshop, brand-guidelines-creation (atualizacao de arquitetura)
- Cross-squad: product squad (extensao para novos produtos)

### Metricas
- Score de fit perceptual entre marca e nova categoria
- Nivel de risco de diluicao avaliado (alto/medio/baixo)
- Decisao go/no-go documentada com fundamentacao
