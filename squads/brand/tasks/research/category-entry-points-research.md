# Category Entry Points Research
> Pesquisa de category entry points para maximizar mental availability da marca.

## Objetivo
Identificar, mapear e priorizar os category entry points (CEPs) — situacoes, necessidades e momentos em que o consumidor pensa na categoria — para orientar estrategias de mental availability.

## Agentes
- **byron-sharp** — lidera a pesquisa de CEPs
- **brand-chief** — orquestracao e validacao

## Inputs
- Definicao da categoria e subcategorias
- Dados de comportamento do consumidor
- Pesquisas de mercado existentes
- Dados de concorrencia

## Passos
1. Definir a categoria e limites de analise
2. Listar potenciais CEPs (situacoes, motivos, momentos)
3. Pesquisar quais CEPs sao mais frequentes
4. Pesquisar quais CEPs a marca ja esta associada
5. Mapear CEPs dominados por concorrentes
6. Priorizar CEPs por frequencia e oportunidade
7. Recomendar CEPs-alvo para a marca
8. Documentar resultados e plano de ativacao

## Frameworks Obrigatorios
- category-entry-points
- sharp-mental-availability

## Checklists de Qualidade
- sharp/mental-availability-audit

## Output Esperado
```
## Mapa de Category Entry Points
### CEPs Identificados: [lista completa]
### CEPs por Frequencia: [ranking]
### CEPs da Marca: [quais ja esta associada]
### CEPs dos Concorrentes: [mapeamento]
### CEPs-Alvo Recomendados: [priorizacao]
### Plano de Ativacao: [como associar marca aos CEPs]
```

## Registro
- `data/research/competitor-research/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: categoria definida, dados de comportamento do consumidor disponiveis
- Gate de saida: score GREEN (>=80%) no checklist sharp/mental-availability-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre priorizacao de CEPs → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (CEPs incompletos, priorizacao sem dados, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: category-and-competitor-research, dados de mercado
- Downstream: positioning-development, define-distinctive-assets, brand-tracking-analysis
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de CEPs identificados e priorizados
- % de CEPs ja associados a marca vs. concorrentes
- Numero de CEPs-alvo recomendados para ativacao
