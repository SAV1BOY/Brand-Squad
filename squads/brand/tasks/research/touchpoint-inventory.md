# Touchpoint Inventory
> Inventario completo de todos os pontos de contato da marca com seus publicos.

## Objetivo
Mapear, classificar e avaliar todos os touchpoints da marca — fisicos, digitais e humanos — identificando inconsistencias e oportunidades de melhoria na experiencia de marca.

## Agentes
- **alina-wheeler** — lidera o mapeamento e avaliacao
- **brand-chief** — orquestracao e validacao

## Inputs
- Brand Guidelines atuais
- Lista de canais e plataformas da marca
- Mapa de jornada do cliente (se existir)
- Materiais de comunicacao em uso

## Passos
1. Listar todos os touchpoints conhecidos por categoria
2. Classificar: pre-compra, compra, pos-compra
3. Classificar: fisico, digital, humano
4. Avaliar consistencia visual em cada touchpoint
5. Avaliar consistencia verbal em cada touchpoint
6. Fotografar/capturar cada touchpoint para registro
7. Pontuar cada touchpoint (consistente, parcial, inconsistente)
8. Priorizar ajustes por visibilidade e impacto

## Frameworks Obrigatorios
- brand-experience-map
- wheeler-brand-identity-process

## Checklists de Qualidade
- wheeler/brand-touchpoints-audit

## Output Esperado
```
## Inventario de Touchpoints
### Touchpoints Digitais: [lista com avaliacao]
### Touchpoints Fisicos: [lista com avaliacao]
### Touchpoints Humanos: [lista com avaliacao]
### Score de Consistencia Geral: [percentual]
### Prioridades de Ajuste: [top 10 touchpoints a corrigir]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines atuais disponiveis, lista de canais e plataformas mapeada
- Gate de saida: score GREEN (>=80%) no checklist wheeler/brand-touchpoints-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre classificacao de touchpoints → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (touchpoints faltantes, avaliacao incompleta, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-audit, brand guidelines existentes
- Downstream: touchpoint-migration, consistency-review, brand-guidelines-creation
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero total de touchpoints inventariados
- Score de consistencia geral (% consistente)
- Numero de touchpoints priorizados para correcao
