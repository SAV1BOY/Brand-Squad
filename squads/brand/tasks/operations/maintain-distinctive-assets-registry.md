# Maintain Distinctive Assets Registry
> Manutencao e atualizacao do registro de distinctive assets da marca.

## Objetivo
Manter o distinctive assets registry atualizado com status, metricas de reconhecimento, regras de uso e evolucao de cada asset — servindo como fonte unica de verdade para gestao dos assets.

## Agentes
- **byron-sharp** — lidera a manutencao do registro
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Distinctive Assets Registry atual
- Resultados de recognition analysis
- Novos assets criados
- Dados de uso dos assets em touchpoints

## Passos
1. Revisar registro atual de distinctive assets
2. Atualizar metricas de reconhecimento (fame e uniqueness)
3. Registrar novos assets adicionados
4. Atualizar status de cada asset (invest, maintain, test, avoid)
5. Verificar regras de uso por asset
6. Documentar evolucao historica
7. Identificar assets que precisam de atencao
8. Publicar registro atualizado

## Frameworks Obrigatorios
- distinctive-assets-system

## Checklists de Qualidade
- sharp/distinctive-assets-audit

## Output Esperado
```
## Distinctive Assets Registry (Atualizado)
### Data: [data da atualizacao]
### Assets Ativos: [lista com status e metricas]
### Novos Assets: [adicionados no periodo]
### Assets Descontinuados: [removidos e motivo]
### Evolucao de Recognition: [trend por asset]
### Alertas: [assets que precisam de acao]
```

## Registro
- `data/registries/distinctive-assets-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: distinctive assets registry atual disponivel, resultados de recognition analysis coletados
- Gate de saida: score GREEN (>=80%) no checklist sharp/distinctive-assets-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre status de assets → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (metricas desatualizadas, assets faltantes, status inconsistente, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: distinctive-assets-recognition-analysis, define-distinctive-assets, sonic-branding-development
- Downstream: brand-guidelines-creation (atualizacao de assets), consistency-review
- Cross-squad: design squad (assets visuais atualizados), marketing squad (assets para campanhas)

### Metricas
- Numero de assets com metricas de fame e uniqueness atualizadas
- % de assets com status atualizado (invest/maintain/test/avoid)
- Numero de alertas de assets que precisam de acao
