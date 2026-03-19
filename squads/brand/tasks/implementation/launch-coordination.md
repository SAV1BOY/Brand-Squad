# Launch Coordination
> Coordenacao do lancamento da marca nova ou atualizada.

## Objetivo
Planejar e coordenar o lancamento da marca — interno e externo — garantindo um rollout sincronizado, impactante e livre de falhas em todos os canais e touchpoints.

## Agentes
- **brand-chief** — lidera a coordenacao geral
- **emily-heyward** — garante impacto e consistencia do lancamento

## Inputs
- Brand Guidelines finalizadas
- Plano de migracao de touchpoints
- Programa de treinamento interno concluido
- Materiais de lancamento prontos
- Calendario de canais definido

## Passos
1. Definir data e estrategia de lancamento (big bang vs. gradual)
2. Criar timeline detalhado com milestones
3. Coordenar lancamento interno (antes do externo)
4. Preparar materiais de imprensa e PR
5. Sincronizar atualizacao de todos os canais digitais
6. Coordenar atualizacao de materiais fisicos
7. Monitorar lancamento em tempo real
8. Documentar resultados e aprendizados

## Frameworks Obrigatorios
- activation-layer

## Checklists de Qualidade
- heyward/brand-launch-readiness-audit
- internal-rollout-quality

## Output Esperado
```
## Plano de Lancamento
### Estrategia: [big bang / gradual / hibrido]
### Timeline: [datas-chave e milestones]
### Lancamento Interno: [data e acoes]
### Lancamento Externo: [data e acoes por canal]
### Materiais de PR: [press release, kit]
### Monitoramento: [metricas em tempo real]
### Contingencia: [plano B para problemas]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines finalizadas, treinamento interno concluido, plano de migracao em andamento, materiais de lancamento prontos
- Gate de saida: score GREEN (>=80%) nos checklists heyward/brand-launch-readiness-audit e internal-rollout-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre brand-chief e emily-heyward sobre estrategia de lancamento → brand-chief decide
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (timeline desalinhado, canais nao sincronizados, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: internal-training, touchpoint-migration, campaign-activation-brief, brand-guidelines-creation
- Downstream: consistency-review, brand-tracking-analysis
- Cross-squad: marketing squad (coordenacao de lancamento externo), people squad (lancamento interno)

### Metricas
- % de canais atualizados no dia do lancamento
- % de milestones cumpridos no prazo
- Score de monitoramento em tempo real (incidentes vs. zero)
