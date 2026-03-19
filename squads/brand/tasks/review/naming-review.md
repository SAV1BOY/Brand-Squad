# Naming Review
> Revisao critica do nome selecionado para marca ou produto.

## Objetivo
Validar o nome selecionado contra todos os criterios estrategicos, linguisticos, legais e digitais — garantindo que seja a melhor escolha antes da decisao final e registro.

## Agentes
- **naming-strategist** — lidera a revisao tecnica
- **brand-chief** — aprovacao final

## Inputs
- Nome selecionado e short list
- Naming decision matrix preenchida
- Dados de disponibilidade de dominios e handles
- Resultado de screening legal
- Posicionamento e brand strategy

## Passos
1. Revisar score na naming decision matrix
2. Validar alinhamento com posicionamento
3. Testar pronunciabilidade em mercados-alvo
4. Verificar conotacoes negativas em outros idiomas
5. Confirmar disponibilidade de dominios e handles
6. Confirmar status de screening legal
7. Avaliar potencial de longevidade do nome
8. Documentar decisao final (aprovado ou alternativa)

## Frameworks Obrigatorios
- naming-systems
- naming-decision-matrix

## Checklists de Qualidade
- naming-quality
- naming/naming-legal-screening-checklist

## Output Esperado
```
## Naming Review
### Nome Avaliado: [nome]
### Score Decision Matrix: [pontuacao]
### Alinhamento Estrategico: [pass/fail]
### Pronunciabilidade: [pass/fail por mercado]
### Conotacoes: [pass/fail por idioma]
### Disponibilidade Digital: [dominios e handles]
### Status Legal: [limpo / pendencia]
### Decisao: [aprovado / alternativa recomendada]
```

## Registro
- `data/registries/naming-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: nome selecionado com scoring completo, dados de disponibilidade digital e screening legal concluidos
- Gate de saida: score GREEN (>=80%) nos checklists naming-quality e naming/naming-legal-screening-checklist
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre naming-strategist e brand-chief sobre decisao final → brand-chief decide (como orchestrator)
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (problemas legais, conotacoes negativas, baixa memorabilidade, etc.)
- Apos 3 loops → escalacao automatica nivel 2 (retorno ao naming-workshop para novas opcoes)
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: naming-shortlist-and-scoring
- Downstream: verbal-identity-development, brand-guidelines-creation, maintain-naming-registry
- Cross-squad: product squad (se naming de produto)

### Metricas
- Score final na naming decision matrix
- Status de disponibilidade digital (dominios + handles)
- Status legal (limpo/pendencia)
