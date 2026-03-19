# Identity Review
> Revisao critica da identidade visual e verbal da marca.

## Objetivo
Avaliar a qualidade, coerencia e eficacia do sistema de identidade da marca — visual e verbal — garantindo que traduza corretamente a estrategia e funcione em todos os touchpoints.

## Agentes
- **brand-chief** — lidera a revisao
- **alina-wheeler** — avalia sistema visual
- **emily-heyward** — avalia impacto e obviedade

## Inputs
- Visual Identity Direction
- Brand Voice Guide
- Brand Guidelines
- Aplicacoes em touchpoints
- Distinctive Assets Registry

## Passos
1. Revisar sistema visual contra Wheeler identity audit
2. Avaliar consistencia entre touchpoints
3. Validar obviedade e impacto (Heyward method)
4. Verificar aderencia a brand guidelines
5. Testar reconhecibilidade dos distinctive assets
6. Avaliar sistema verbal (voz, tom, vocabulario)
7. Identificar inconsistencias e gaps
8. Documentar aprovacao ou ajustes

## Frameworks Obrigatorios
- wheeler-brand-identity-process
- heyward-obviousness-method

## Checklists de Qualidade
- visual-identity-quality
- brand-guidelines-quality

## Output Esperado
```
## Identity Review
### Sistema Visual: [aprovado / ajuste necessario]
### Sistema Verbal: [aprovado / ajuste necessario]
### Consistencia: [score por touchpoint]
### Distinctive Assets: [status de cada]
### Gaps: [lista de inconsistencias]
### Ajustes: [lista priorizada]
### Status Final: [aprovado / revisao necessaria]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: visual identity direction, brand voice guide, brand guidelines e distinctive assets registry disponiveis
- Gate de saida: score GREEN (>=80%) nos checklists visual-identity-quality e brand-guidelines-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief (como lider da revisao, escala para HRM Chief nivel 3)
- Se conflito entre alina-wheeler e emily-heyward sobre avaliacao visual → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief direcionado ao agente responsavel (visual → alina-wheeler, impacto → emily-heyward)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: visual-identity-direction, brand-voice-development, brand-guidelines-creation, define-distinctive-assets
- Downstream: touchpoint-migration, launch-coordination (layer gate identity→activation)
- Cross-squad: nenhum (task de revisao interna — gate obrigatorio antes de avancar para activation layer)

### Metricas
- Score de consistencia entre touchpoints avaliados
- % de distinctive assets com reconhecibilidade validada
- Numero de inconsistencias visuais/verbais identificadas
