# Cross-Squad Brand Sync
> Sincronizacao periodica de marca entre o Brand Squad e os demais squads.

## Objetivo
Garantir que todos os squads do MMOS estejam alinhados com a estrategia, identidade e guidelines de marca mais recentes — coletando feedback, resolvendo duvidas e identificando oportunidades de melhoria na colaboracao.

## Agentes
- **brand-chief** — lidera a sincronizacao

## Inputs
- Brand Guidelines versao atual
- Atualizacoes de marca recentes
- Feedback acumulado dos squads
- Registro de duvidas e solicitacoes
- Cross-squad integration map (config.yaml)

## Passos
1. Preparar pauta com atualizacoes de marca do periodo
2. Coletar feedback pendente de cada squad
3. Verificar se assets entregues estao sendo usados corretamente
4. Identificar necessidades nao atendidas dos squads
5. Resolver duvidas sobre uso da marca
6. Alinhar proximas entregas e timeline
7. Atualizar handoff materials se necessario
8. Documentar acoes e decisoes

## Frameworks Obrigatorios
- brand-governance-model

## Checklists de Qualidade
- Todos os squads participantes representados
- Feedback documentado e endereçado
- Acoes com responsavel e prazo

## Output Esperado
```
## Cross-Squad Sync Report
### Data: [data do sync]
### Squads Participantes: [lista]
### Atualizacoes Comunicadas: [lista]
### Feedback Recebido: [por squad]
### Duvidas Resolvidas: [lista]
### Necessidades Identificadas: [novas demandas]
### Acoes: [lista com responsavel e prazo]
### Proximo Sync: [data agendada]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines versao atual disponivel, atualizacoes de marca do periodo documentadas, feedback dos squads coletado
- Gate de saida: todos os squads participantes representados, feedback documentado e enderecado, acoes com responsavel e prazo
- Score minimo: GREEN (>=80%) na validacao de completude e cobertura do sync

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief (como unico agente, escala para HRM Chief nivel 3)
- Se conflito entre squads sobre uso da marca → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (squads nao representados, feedback nao enderecado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-guidelines-creation, update-brand-guidelines, brand-governance-setup
- Downstream: update-brand-guidelines (se feedback demandar mudancas), partner-alignment
- Cross-squad: copy, marketing, product, design, people squads (sincronizacao bidirecional)

### Metricas
- Numero de squads participantes no sync
- Numero de duvidas resolvidas e acoes definidas
- % de acoes concluidas antes do proximo sync
