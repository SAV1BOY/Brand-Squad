# Brand Association Mapping
> Mapeamento estruturado das associacoes de marca na mente do consumidor.

## Objetivo
Mapear a rede de associacoes que o consumidor faz com a marca — atributos, beneficios, emocoes, personalidade — utilizando os frameworks CBBE e Aaker para diagnosticar a forca e unicidade dessas associacoes.

## Agentes
- **kevin-keller** — lidera o mapeamento via CBBE
- **david-aaker** — complementa com brand identity system
- **brand-chief** — orquestracao e validacao

## Inputs
- Dados de pesquisa de percepcao
- Entrevistas com clientes
- Dados de social listening
- Posicionamento atual documentado

## Passos
1. Definir categorias de associacao a mapear
2. Coletar dados primarios (pesquisa) e secundarios (social)
3. Mapear associacoes por tipo (atributo, beneficio, atitude)
4. Avaliar forca de cada associacao
5. Avaliar favorabilidade de cada associacao
6. Avaliar unicidade vs. concorrentes
7. Construir mapa visual de associacoes
8. Identificar gaps entre associacoes desejadas e reais

## Frameworks Obrigatorios
- keller-cbbe-pyramid
- aaker-brand-equity-model

## Checklists de Qualidade
- keller/cbbe-pyramid-audit
- aaker/aaker-equity-audit

## Output Esperado
```
## Mapa de Associacoes de Marca
### Associacoes de Atributo: [lista com forca]
### Associacoes de Beneficio: [lista com forca]
### Associacoes de Atitude: [lista com forca]
### Unicidade vs. Concorrentes: [diferenciadores reais]
### Gaps: [associacoes desejadas nao percebidas]
### Recomendacoes: [como fortalecer/criar associacoes]
```

## Registro
- `data/research/survey-results/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: dados de pesquisa de percepcao disponiveis, entrevistas com clientes concluidas
- Gate de saida: score GREEN (>=80%) nos checklists keller/cbbe-pyramid-audit e aaker/aaker-equity-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre kevin-keller e david-aaker sobre classificacao de associacoes → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (associacoes incompletas, unicidade nao avaliada, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: perception-study, customer-interviews, social-listening-analysis
- Downstream: positioning-development, define-brand-promise, brand-equity-plan
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de associacoes mapeadas por tipo (atributo, beneficio, atitude)
- % de associacoes avaliadas quanto a forca, favorabilidade e unicidade
- Numero de gaps identificados entre associacoes desejadas e reais
