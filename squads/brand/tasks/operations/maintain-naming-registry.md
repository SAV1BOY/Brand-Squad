# Maintain Naming Registry
> Manutencao do registro de nomes, dominios e handles da marca.

## Objetivo
Manter o naming registry atualizado com todos os nomes registrados, dominios adquiridos, handles reservados e status legal — servindo como fonte unica de verdade para gestao de naming.

## Agentes
- **naming-strategist** — lidera a manutencao do registro
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Naming Registry atual
- Novos nomes registrados
- Status de renovacao de dominios
- Atualizacoes de status legal/trademark

## Passos
1. Revisar registro atual de nomes
2. Atualizar status de cada nome (ativo, reservado, expirado)
3. Verificar datas de renovacao de dominios
4. Atualizar status de trademarks e registros legais
5. Registrar novos nomes e handles adquiridos
6. Identificar nomes e dominios a vencer
7. Recomendar renovacoes ou releases
8. Publicar registro atualizado

## Frameworks Obrigatorios
- naming-systems

## Checklists de Qualidade
- naming/naming-legal-screening-checklist
- Dominios com data de renovacao verificada
- Handles ativos em todas as plataformas

## Output Esperado
```
## Naming Registry (Atualizado)
### Data: [data da atualizacao]
### Nomes Ativos: [lista com status legal]
### Dominios: [lista com data de vencimento]
### Handles: [por plataforma com status]
### Trademarks: [status de registro]
### Alertas: [vencimentos proximos]
### Acoes Necessarias: [renovacoes e aquisicoes]
```

## Registro
- `data/registries/naming-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: naming registry atual disponivel, status de renovacao de dominios verificado
- Gate de saida: score GREEN (>=80%) no checklist naming/naming-legal-screening-checklist, dominios com data de renovacao verificada, handles ativos em todas as plataformas
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre renovacao vs. release de nomes → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (datas de renovacao nao verificadas, status legal desatualizado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: naming-review, naming-shortlist-and-scoring
- Downstream: update-brand-guidelines (se nomes mudam)
- Cross-squad: product squad (status de naming de produtos)

### Metricas
- Numero de nomes com status legal atualizado
- Numero de dominios com data de renovacao proxima (alerta)
- % de handles ativos e verificados por plataforma
