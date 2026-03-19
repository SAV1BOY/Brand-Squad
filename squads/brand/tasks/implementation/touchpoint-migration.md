# Touchpoint Migration
> Migracao de todos os pontos de contato para a nova identidade de marca.

## Objetivo
Planejar e executar a migracao de todos os touchpoints — digitais, fisicos e humanos — para a nova identidade, garantindo consistencia e minimizando disrupcao na experiencia do cliente.

## Agentes
- **alina-wheeler** — lidera o plano de migracao
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Touchpoint inventory atualizado
- Brand Guidelines novas
- Prioridades de migracao definidas
- Budget e timeline disponivel

## Passos
1. Revisar touchpoint inventory completo
2. Classificar touchpoints por prioridade (alta, media, baixa)
3. Estimar esforco e custo por touchpoint
4. Criar cronograma de migracao faseado
5. Definir responsaveis por cada touchpoint
6. Executar migracao por fase
7. Auditar cada touchpoint migrado
8. Documentar status e pendencias

## Frameworks Obrigatorios
- brand-experience-map
- brand-consistency-model

## Checklists de Qualidade
- wheeler/brand-touchpoints-audit
- brand-guidelines-quality

## Output Esperado
```
## Plano de Migracao de Touchpoints
### Fase 1 (Critica): [touchpoints + prazo + responsavel]
### Fase 2 (Importante): [touchpoints + prazo + responsavel]
### Fase 3 (Desejavel): [touchpoints + prazo + responsavel]
### Status: [migrado / em andamento / pendente]
### Budget Estimado: [por fase]
### Auditoria: [checklist de validacao]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: touchpoint inventory atualizado, brand guidelines novas finalizadas, prioridades e budget definidos
- Gate de saida: score GREEN (>=80%) nos checklists wheeler/brand-touchpoints-audit e brand-guidelines-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre priorizacao de touchpoints → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (touchpoints migrados com inconsistencia, cronograma nao cumprido, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: touchpoint-inventory, brand-guidelines-creation, visual-identity-direction
- Downstream: consistency-review, launch-coordination
- Cross-squad: design squad (execucao de migracoes visuais), marketing squad (atualizacao de materiais)

### Metricas
- % de touchpoints migrados por fase
- % de touchpoints auditados apos migracao
- Score de consistencia pos-migracao
