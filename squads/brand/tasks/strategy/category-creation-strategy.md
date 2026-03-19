# Category Creation Strategy
> Estrategia de criacao de uma nova categoria de mercado para a marca.

## Objetivo
Desenvolver a estrategia para criar e dominar uma nova categoria de mercado, posicionando a marca como lider e referencia — seguindo os principios de Al Ries sobre foco e criacao de categoria.

## Agentes
- **al-ries** — lidera a estrategia de criacao de categoria
- **marty-neumeier** — valida diferenciacao radical (Zag)
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Analise de mercado e concorrencia
- Dados de customer interviews (necessidades nao atendidas)
- Tendencias e inovacoes da industria
- Capacidades e diferenciais do negocio

## Passos
1. Identificar necessidade nao atendida ou mal atendida
2. Definir a nova categoria e seus limites
3. Nomear a categoria (naming de categoria)
4. Posicionar a marca como criadora e lider da categoria
5. Definir o "inimigo" (categoria antiga ou status quo)
6. Criar narrativa de categoria (por que existe)
7. Definir criterios que a marca domina
8. Planejar evangelizacao e educacao do mercado

## Frameworks Obrigatorios
- ries-positioning
- ries-22-immutable-laws
- neumeier-zag-method

## Checklists de Qualidade
- ries/focus-and-category-audit
- neumeier/zag-audit

## Output Esperado
```
## Estrategia de Criacao de Categoria
### Nova Categoria: [nome e definicao]
### Necessidade Atendida: [problema que resolve]
### Inimigo: [o que substitui]
### Posicao de Lideranca: [por que a marca e a referencia]
### Narrativa: [historia da categoria]
### Criterios de Dominio: [onde a marca ganha]
### Plano de Evangelizacao: [como educar o mercado]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: analise de mercado e concorrencia concluida, customer interviews com necessidades nao atendidas identificadas
- Gate de saida: score GREEN (>=80%) nos checklists ries/focus-and-category-audit e neumeier/zag-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre al-ries e marty-neumeier sobre definicao da categoria → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (categoria mal delimitada, naming confuso, plano de evangelizacao ausente, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: category-and-competitor-research, customer-interviews, positioning-development
- Downstream: positioning-development, naming-workshop, campaign-activation-brief
- Cross-squad: marketing squad (evangelizacao da nova categoria)

### Metricas
- Clareza da definicao da nova categoria (teste de compreensao)
- Numero de criterios de dominio definidos
- Completude do plano de evangelizacao
