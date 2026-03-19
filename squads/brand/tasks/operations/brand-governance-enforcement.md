# Brand Governance Enforcement
> Aplicacao e monitoramento das regras de governanca de marca.

## Objetivo
Garantir que as regras de governanca de marca estejam sendo cumpridas — monitorando uso, identificando violacoes, aplicando correcoes e mantendo a integridade da marca em todas as frentes.

## Agentes
- **brand-chief** — lidera a aplicacao de governanca
- **alina-wheeler** — valida compliance visual

## Inputs
- Modelo de governanca de marca
- Brand Guidelines
- Relatorios de consistency review
- Registro de violacoes anteriores
- Feedback de parceiros e equipes

## Passos
1. Revisar registro de violacoes do periodo
2. Monitorar uso da marca em canais internos
3. Monitorar uso por parceiros e terceiros
4. Classificar violacoes por severidade
5. Notificar responsaveis sobre violacoes
6. Apoiar correcao das violacoes
7. Atualizar registro de violacoes
8. Recomendar ajustes no modelo de governanca

## Frameworks Obrigatorios
- brand-governance-model
- brand-consistency-model

## Checklists de Qualidade
- brand-guidelines-quality
- Violacoes documentadas com evidencia
- Correcoes acompanhadas ate resolucao

## Output Esperado
```
## Governance Enforcement Report
### Periodo: [datas]
### Violacoes Identificadas: [total por severidade]
### Violacoes Criticas: [detalhe com evidencia]
### Violacoes Resolvidas: [% de resolucao]
### Violacoes Pendentes: [lista com responsavel]
### Reincidencias: [areas com problemas recorrentes]
### Ajustes no Modelo: [recomendacoes]
```

## Registro
- `data/registries/brand-violations-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: modelo de governanca de marca definido, brand guidelines disponiveis, registro de violacoes anteriores acessivel
- Gate de saida: score GREEN (>=80%) no checklist brand-guidelines-quality, violacoes documentadas com evidencia, correcoes acompanhadas
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre brand-chief e alina-wheeler sobre severidade de violacoes → brand-chief decide
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (violacoes nao documentadas, correcoes nao acompanhadas, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: consistency-review, partner-alignment, brand-governance-setup
- Downstream: update-brand-guidelines (ajustes no modelo), quarterly-brand-review
- Cross-squad: todos os squads e parceiros afetados (notificacao e correcao de violacoes)

### Metricas
- Numero de violacoes identificadas por severidade
- % de violacoes resolvidas no prazo
- Taxa de reincidencia por area
