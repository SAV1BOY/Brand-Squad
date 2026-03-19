# Log de Aprendizados

> Captura de licoes aprendidas para evitar repeticao de erros e replicar sucessos.

## Por que Documentar Aprendizados

- Transformar experiencias em conhecimento reutilizavel
- Evitar que a mesma falha aconteca duas vezes
- Identificar padroes de sucesso para replicacao
- Acelerar a curva de aprendizado da equipe

## Formato do Registro

| Data | Aprendizado | Contexto | Tipo | Acao Resultante | Aplicavel a |
|------|-------------|----------|------|-----------------|-------------|
| YYYY-MM-DD | [aprendizado] | [task/projeto] | sucesso/falha/insight | [acao] | tasks/frameworks/processos |

## Categorias de Aprendizados

### Aprendizados de Estrategia
- O que funcionou ou nao em posicionamento
- Insights sobre mercado e consumidor
- Decisoes estrategicas e seus resultados

### Aprendizados de Identidade
- Aplicacoes visuais que geraram impacto
- Erros de consistencia e como corrigir
- Evolucao de guidelines com base em uso real

### Aprendizados de Processo
- Fluxos que aceleraram ou travaram entregas
- Quality gates que pegaram problemas cedo
- Estimativas de tempo vs. tempo real

### Aprendizados de Colaboracao
- Handoffs que funcionaram bem e por que
- Comunicacao entre squads que gerou atrito
- Alinhamentos que preveniram retrabalho

## Template de Registro

```
## [Aprendizado] — YYYY-MM-DD

**Contexto**: [Em qual task ou projeto aconteceu]
**Tipo**: sucesso | falha | insight
**O que aconteceu**: [Descricao objetiva]
**Por que aconteceu**: [Analise de causa raiz]
**Acao Resultante**: [O que mudou a partir disso]
**Aplicavel a**: [Onde mais esse aprendizado se aplica]
```

---

## Aprendizados Registrados

### [SEED] Quality gates em cascata detectam problemas mais cedo — 2026-03-01

**Contexto**: Definicao do sistema de quality gates durante setup do squad
**Tipo**: insight
**O que aconteceu**: Ao projetar o sistema, ficou claro que um unico gate final criaria bottleneck no brand-chief e permitiria que erros se acumulassem ate o fim
**Por que aconteceu**: Tasks passam por multiplos agentes e camadas — sem validacao intermediaria, o custo de rework no final e exponencialmente maior
**Acao Resultante**: Implementar cascade de 5 niveis (Agent → Task → Layer → Chief → Final) com scoring GREEN/YELLOW/RED
**Aplicavel a**: Todos os squads do MMOS — o padrao de quality gate cascade deve ser replicado

### [SEED] Config.yaml como cerebro evita ambiguidade de roteamento — 2026-03-01

**Contexto**: Decisao de centralizar roteamento no config.yaml vs distribuir nos workflows
**Tipo**: sucesso
**O que aconteceu**: Centralizar o mapping task → agents → frameworks → checklists → templates → registry num unico arquivo elimina duplicacao e garante single source of truth
**Por que aconteceu**: Quando o roteamento estava distribuido nos workflows, cada workflow definia agentes e frameworks de forma inconsistente
**Acao Resultante**: Config.yaml se tornou o cerebro de roteamento; workflows referenciam tasks mas nao redefinem o roteamento
**Aplicavel a**: Todos os squads — config.yaml como padrao de cerebro de roteamento
