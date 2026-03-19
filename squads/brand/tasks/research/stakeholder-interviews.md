# Stakeholder Interviews
> Entrevistas com stakeholders internos para capturar visao, expectativas e alinhamento sobre a marca.

## Objetivo
Coletar perspectivas de lideranca e stakeholders-chave sobre a marca — visao, valores, diferenciais percebidos e expectativas — identificando alinhamentos e desalinhamentos para fundamentar decisoes estrategicas.

## Agentes
- **denise-yohn** — lidera o desenho e conducao das entrevistas
- **brand-chief** — orquestracao e validacao

## Inputs
- Lista de stakeholders a entrevistar
- Contexto do projeto e objetivos
- Materiais de marca existentes
- Roteiro base de entrevista

## Passos
1. Mapear stakeholders-chave (C-level, diretores, fundadores)
2. Elaborar roteiro com perguntas sobre visao, valores e marca
3. Agendar e conduzir entrevistas individuais
4. Documentar respostas e citacoes-chave
5. Identificar temas convergentes e divergentes
6. Mapear gaps de alinhamento entre stakeholders
7. Sintetizar visao consolidada vs. visoes individuais
8. Documentar recomendacoes de alinhamento

## Frameworks Obrigatorios
- discovery-and-research
- yohn-brand-as-business

## Checklists de Qualidade
- Minimo de entrevistas com todos os stakeholders-chave
- Divergencias documentadas e sinalizadas
- Citacoes literais registradas

## Output Esperado
```
## Relatorio de Stakeholder Interviews
### Stakeholders Entrevistados: [lista e cargos]
### Visao Convergente: [temas em que todos concordam]
### Visao Divergente: [temas com desalinhamento]
### Percepcao da Marca: [como cada stakeholder ve]
### Expectativas: [o que esperam da marca]
### Recomendacoes de Alinhamento: [acoes]
```

## Registro
- `data/research/interview-notes/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: lista de stakeholders aprovada, roteiro base de entrevista validado por denise-yohn
- Gate de saida: todos os stakeholders-chave entrevistados, divergencias documentadas e sinalizadas, citacoes literais registradas
- Score minimo: GREEN (>=80%) na validacao de completude e qualidade das entrevistas

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre interpretacao de divergencias → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (stakeholders faltantes, divergencias nao documentadas, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: briefing inicial do projeto
- Downstream: define-brand-purpose, define-brand-promise, brand-architecture-design
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de stakeholders entrevistados vs. planejado
- Numero de temas convergentes vs. divergentes identificados
- Numero de citacoes literais registradas
