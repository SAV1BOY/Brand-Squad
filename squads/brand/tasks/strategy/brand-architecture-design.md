# Brand Architecture Design
> Definicao da estrutura de relacionamento entre marcas do portfolio.

## Objetivo
Desenhar a arquitetura de marca que organiza as relacoes entre marca-mae, sub-marcas, endorsed brands e marcas independentes — maximizando sinergia e minimizando confusao no portfolio.

## Agentes
- **david-aaker** — lidera o design de arquitetura
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Portfolio atual de marcas e produtos
- Brand Strategy Document
- Dados de percepcao por marca
- Estrategia de crescimento do negocio

## Passos
1. Inventariar todas as marcas e produtos do portfolio
2. Mapear relacoes atuais entre marcas
3. Avaliar modelos de arquitetura (branded house, house of brands, etc.)
4. Analisar sinergia e risco de canibalizacao
5. Definir modelo ideal de arquitetura
6. Definir regras de uso e hierarquia visual
7. Documentar guidelines de co-existencia
8. Validar com stakeholders e registrar decisao

## Frameworks Obrigatorios
- aaker-brand-identity-system
- brand-architecture-models
- brand-portfolio-strategy

## Checklists de Qualidade
- aaker/aaker-architecture-audit
- brand-architecture-quality

## Output Esperado
```
## Brand Architecture
### Modelo Escolhido: [branded house / house of brands / hybrid]
### Hierarquia: [diagrama de relacoes]
### Regras de Uso: [quando usar cada marca]
### Hierarquia Visual: [tamanhos e posicoes]
### Regras de Naming: [padroes para novos produtos]
### Riscos Mitigados: [canibalizacao, confusao]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: portfolio atual inventariado, brand strategy document disponivel, estrategia de crescimento definida
- Gate de saida: score GREEN (>=80%) nos checklists aaker/aaker-architecture-audit e brand-architecture-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre modelo de arquitetura → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (canibalizacao nao avaliada, hierarquia ambigua, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-audit, stakeholder-interviews, positioning-development
- Downstream: brand-extension-strategy, brand-guidelines-creation, naming-workshop
- Cross-squad: product squad (arquitetura de naming de produtos)

### Metricas
- Numero de marcas/produtos mapeados no portfolio
- Risco de canibalizacao avaliado (alto/medio/baixo)
- Clareza das regras de co-existencia (pass/fail)
