# Competitor Brand Shifts
> Analise de mudancas e movimentos de marca dos concorrentes.

## Objetivo
Monitorar e analisar mudancas significativas nas marcas dos concorrentes — reposicionamentos, rebrands, novos launches, mudancas de messaging — avaliando impacto potencial na marca e recomendando respostas.

## Agentes
- **al-ries** — lidera a analise competitiva
- **byron-sharp** — avalia impacto em mental availability
- **brand-chief** — orquestracao e validacao

## Inputs
- Mapa competitivo atual
- Monitoramento de canais dos concorrentes
- Dados de social listening competitivo
- Dados de market share

## Passos
1. Identificar mudancas de marca dos concorrentes no periodo
2. Classificar por tipo (rebrand, reposicionamento, extensao, etc.)
3. Avaliar significancia estrategica de cada mudanca
4. Analisar impacto nos CEPs da categoria
5. Avaliar ameaca ao posicionamento da marca
6. Comparar distinctive assets pre e pos mudanca
7. Projetar impacto de medio prazo
8. Recomendar resposta (se necessaria)

## Frameworks Obrigatorios
- competitive-framing
- ries-positioning

## Checklists de Qualidade
- Mudancas documentadas com evidencias
- Impacto avaliado com dados

## Output Esperado
```
## Competitor Brand Shifts Report
### Periodo: [datas]
### Mudancas Identificadas:
  - [Concorrente A]: [tipo de mudanca + detalhes]
  - [Concorrente B]: [tipo de mudanca + detalhes]
### Impacto em CEPs: [quais afetados]
### Ameaca ao Posicionamento: [nivel]
### Impacto em Market Share: [projecao]
### Resposta Recomendada: [acao ou watch]
```

## Registro
- `data/research/competitor-research/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: mapa competitivo atual disponivel, monitoramento de canais dos concorrentes ativo, dados de social listening competitivo coletados
- Gate de saida: mudancas documentadas com evidencias, impacto avaliado com dados
- Score minimo: GREEN (>=80%) na validacao de completude e fundamentacao da analise

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre al-ries e byron-sharp sobre significancia de mudancas → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (mudancas sem evidencia, impacto nao quantificado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: category-and-competitor-research, social-listening-analysis
- Downstream: competitor-response-review, competitive-repositioning, quarterly-brand-review
- Cross-squad: marketing squad (alertas sobre movimentos competitivos relevantes)

### Metricas
- Numero de mudancas competitivas identificadas no periodo
- Nivel de ameaca ao posicionamento da marca (alto/medio/baixo)
- Tempo entre deteccao e documentacao da mudanca
