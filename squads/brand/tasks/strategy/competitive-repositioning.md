# Competitive Repositioning
> Reposicionamento estrategico da marca frente a mudancas competitivas.

## Objetivo
Redefinir o posicionamento da marca em resposta a movimentos competitivos, mudancas de mercado ou evolucao do publico — mantendo relevancia e diferenciacao sem perder o equity construido.

## Agentes
- **al-ries** — lidera o reposicionamento competitivo
- **marty-neumeier** — valida nova diferenciacao
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Posicionamento atual documentado
- Analise de movimentos competitivos recentes
- Dados de percepcao atualizados
- Mudancas no mercado ou publico identificadas

## Passos
1. Diagnosticar motivos para reposicionamento
2. Mapear novo landscape competitivo
3. Identificar novas oportunidades de diferenciacao
4. Definir novo frame of reference (se necessario)
5. Articular novo point of difference
6. Avaliar impacto no equity existente
7. Redigir novo positioning statement
8. Planejar transicao do posicionamento antigo para novo

## Frameworks Obrigatorios
- ries-positioning
- competitive-framing
- neumeier-brand-gap

## Checklists de Qualidade
- ries/positioning-statement-audit
- positioning-quality

## Output Esperado
```
## Competitive Repositioning
### Motivo: [por que reposicionar]
### Posicionamento Anterior: [statement antigo]
### Novo Posicionamento: [statement novo]
### Diferencial Atualizado: [novo PoD]
### Impacto no Equity: [o que muda, o que preserva]
### Plano de Transicao: [como migrar sem perder equity]
### Riscos: [e mitigacoes]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: posicionamento atual documentado, analise de movimentos competitivos recentes concluida, dados de percepcao atualizados
- Gate de saida: score GREEN (>=80%) nos checklists ries/positioning-statement-audit e positioning-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre al-ries e marty-neumeier sobre novo diferencial → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (novo posicionamento nao diferenciado, impacto em equity nao avaliado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: category-and-competitor-research, competitor-brand-shifts, perception-study
- Downstream: messaging-house-development, touchpoint-migration, campaign-activation-brief
- Cross-squad: marketing squad (novo posicionamento para campanhas), copy squad (atualizacao de messaging)

### Metricas
- Score de diferenciacao do novo posicionamento vs. anterior
- Nivel de impacto estimado no equity existente
- Completude do plano de transicao de posicionamento
