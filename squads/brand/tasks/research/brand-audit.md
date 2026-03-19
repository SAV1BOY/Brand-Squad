# Brand Audit
> Auditoria completa dos elementos de marca usando frameworks de equity e identidade.

## Objetivo
Avaliar o estado atual da marca em todas as dimensoes — equity, identidade, consistencia, percepcao e posicionamento — gerando um diagnostico fundamentado com gaps e oportunidades.

## Agentes
- **brand-chief** — orquestra a auditoria
- **byron-sharp** — distinctive assets e mental availability
- **kevin-keller** — CBBE pyramid e brand knowledge

## Inputs
- Materiais atuais da marca (logo, guidelines, colateral)
- Dados de brand tracking (se existirem)
- Comunicacoes recentes (campanhas, social, PR)
- Feedback de stakeholders

## Passos
1. Coletar todos os materiais e manifestacoes da marca
2. Avaliar brand equity via Aaker Brand Equity Model
3. Mapear brand knowledge via CBBE Pyramid (Keller)
4. Auditar distinctive assets e nivel de reconhecimento
5. Avaliar consistencia entre touchpoints
6. Identificar gaps entre identidade desejada e percebida
7. Priorizar findings por impacto
8. Documentar em relatorio de auditoria

## Frameworks Obrigatorios
- aaker-brand-equity-model
- keller-cbbe-pyramid
- distinctive-assets-system

## Checklists de Qualidade
- aaker/aaker-equity-audit
- sharp/distinctive-assets-audit

## Output Esperado
```
## Relatorio de Brand Audit
### Score de Equity (Aaker): [pontuacao por dimensao]
### CBBE Pyramid (Keller): [nivel atingido]
### Distinctive Assets: [status de cada asset]
### Gaps Identificados: [lista priorizada]
### Recomendacoes: [acoes priorizadas por impacto]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: briefing do projeto aprovado, materiais da marca coletados, dados de tracking disponiveis
- Gate de saida: score GREEN (>=80%) nos checklists aaker/aaker-equity-audit e sharp/distinctive-assets-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre byron-sharp e kevin-keller sobre diagnostico → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas identificadas nos checklists
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: briefing inicial do projeto (entrada do squad)
- Downstream: positioning-development, define-brand-purpose, brand-equity-plan
- Cross-squad: nenhum (task interna de diagnostico)

### Metricas
- Numero de dimensoes de equity avaliadas (Aaker + Keller)
- % de gaps identificados com recomendacao acionavel
- Tempo entre coleta de materiais e entrega do relatorio
