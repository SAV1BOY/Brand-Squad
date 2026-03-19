# Customer Interviews
> Entrevistas em profundidade com clientes para capturar percepcoes, necessidades e linguagem real.

## Objetivo
Coletar insights qualitativos diretamente de clientes sobre percepcao da marca, jobs-to-be-done, linguagem utilizada e expectativas — alimentando decisoes de posicionamento e messaging.

## Agentes
- **denise-yohn** — lidera o desenho e execucao das entrevistas
- **brand-chief** — orquestracao e validacao final

## Inputs
- Perfil dos clientes a serem entrevistados
- Roteiro base de perguntas
- Objetivos especificos da pesquisa
- Contexto de marca e projeto

## Passos
1. Definir perfis de entrevistados (segmentos, personas)
2. Elaborar roteiro semi-estruturado
3. Recrutar participantes (minimo 5 por segmento)
4. Conduzir entrevistas individuais em profundidade
5. Transcrever e codificar respostas
6. Identificar padroes, temas e linguagem recorrente
7. Mapear jobs-to-be-done e momentos de decisao
8. Consolidar em relatorio de insights

## Frameworks Obrigatorios
- discovery-and-research
- jobs-to-be-done-branding

## Checklists de Qualidade
- Minimo 5 entrevistas por segmento
- Roteiro validado antes da execucao
- Transcricoes completas arquivadas

## Output Esperado
```
## Relatorio de Entrevistas
### Perfil dos Entrevistados: [segmentos e quantidade]
### Percepcoes-Chave: [temas recorrentes]
### Jobs-to-be-Done: [lista priorizada]
### Linguagem do Cliente: [expressoes e termos reais]
### Insights para Marca: [recomendacoes]
```

## Registro
- `data/research/interview-notes/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: perfil de entrevistados definido, roteiro base aprovado por denise-yohn
- Gate de saida: minimo 5 entrevistas por segmento realizadas, transcricoes completas, insights codificados
- Score minimo: GREEN (>=80%) na validacao de completude e qualidade dos insights

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre interpretacao de insights → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (amostra insuficiente, codificacao incompleta, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: briefing do projeto com objetivos de pesquisa
- Downstream: define-brand-purpose, define-brand-promise, voice-of-customer-mining, positioning-development
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de entrevistas realizadas por segmento
- Numero de jobs-to-be-done identificados
- Numero de expressoes de linguagem real coletadas
