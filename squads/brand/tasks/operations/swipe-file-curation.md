# Swipe File Curation
> Curadoria do swipe file de referencias e inspiracoes de marca.

## Objetivo
Manter um acervo organizado e atualizado de referencias de branding — exemplos de excelencia em posicionamento, identidade, messaging, campaigns e distinctive assets — servindo como fonte de inspiracao e benchmark.

## Agentes
- **brand-chief** — lidera a curadoria
- **emily-heyward** — contribui com referencias de lancamento e identidade

## Inputs
- Swipe file atual
- Novas referencias identificadas
- Premiacoes e cases do setor
- Tendencias de branding
- Contribuicoes dos agentes do squad

## Passos
1. Revisar swipe file atual e remover itens obsoletos
2. Coletar novas referencias de excelencia
3. Classificar por categoria (visual, verbal, campaign, etc.)
4. Anotar por que cada referencia e relevante
5. Taggar por framework/principio que exemplifica
6. Organizar em estrutura navegavel
7. Distribuir highlights para o squad
8. Atualizar swipe.config com novas fontes

## Frameworks Obrigatorios
- Conhecimento geral de todos os frameworks do squad

## Checklists de Qualidade
- Minimo 5 novas referencias por mes
- Cada referencia com anotacao de relevancia
- Classificacao por categoria consistente

## Output Esperado
```
## Swipe File Update
### Data: [data da atualizacao]
### Novas Referencias: [lista com categoria e anotacao]
### Referencias Removidas: [lista com motivo]
### Total no Acervo: [por categoria]
### Highlights do Mes: [top 3 referencias]
### Fontes Adicionadas: [novas fontes de curadoria]
```

## Registro
- `swipe/` e `swipe.config`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: swipe file atual disponivel, novas referencias coletadas
- Gate de saida: minimo 5 novas referencias por mes, cada referencia com anotacao de relevancia, classificacao por categoria consistente
- Score minimo: GREEN (>=80%) na validacao de completude e qualidade da curadoria

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre brand-chief e emily-heyward sobre relevancia de referencias → brand-chief decide
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (referencias sem anotacao, classificacao inconsistente, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: trend-and-cultural-context, competitor-brand-shifts (fontes de novas referencias)
- Downstream: nenhum (asset de referencia continuo para todo o squad)
- Cross-squad: nenhum (swipe file interno do brand squad)

### Metricas
- Numero de novas referencias adicionadas por mes
- Total de referencias no acervo por categoria
- Numero de referencias removidas por obsolescencia
