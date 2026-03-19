# Log de Decisoes de Marca

> Registro de todas as decisoes estrategicas de marca para historico e aprendizado.

## Por que Documentar Decisoes

- Evitar re-litigar decisoes ja tomadas
- Entender o raciocinio por tras de escolhas passadas
- Onboarding mais rapido de novos membros da equipe
- Aprender com decisoes que funcionaram e que nao funcionaram

## Formato do Registro

| Data | Decisao | Contexto | Opcoes Consideradas | Decisao Final | Responsavel | Resultado |
|------|---------|----------|--------------------|--------------|-----------| ---------|
| YYYY-MM-DD | [titulo] | [por que] | [opcoes] | [escolha] | [quem] | [outcome] |

## Categorias de Decisoes

### Estrategicas
- Mudanca de posicionamento
- Expansao ou contracao de portfolio
- Entrada em novo mercado
- Mudanca de proposito ou valores

### Identidade
- Mudanca de logo, cor ou tipografia
- Evolucao de guidelines
- Novo distinctive asset

### Comunicacao
- Mudanca de tom de voz
- Nova campanha de posicionamento
- Mudanca de canais prioritarios

### Naming
- Novo nome de produto ou feature
- Mudanca de nome existente
- Decisao de arquitetura de marca

---

## Decisoes Registradas

### [SEED] Estabelecimento do Brand Squad — 2026-03-01

**Contexto**: Necessidade de criar um sistema operacional completo de marca com metodologia HRM
**Opcoes**: (1) Sistema simplificado com 3-5 agentes; (2) Sistema completo com 15 agentes especializados; (3) Sistema modular incremental
**Decisao**: Opcao 2 — Sistema completo com 15 agentes
**Raciocinio**: O escopo de brand strategy + identity requer cobertura de todas as camadas (research → measurement). Cada agente representa uma escola de pensamento distinta e complementar. O overhead de coordenacao e mitigado pelo config.yaml como cerebro de roteamento.
**Responsavel**: Brand Chief
**Resultado**: Squad operacional com ~728 arquivos, 18 diretorios MMOS, 5 handoff contracts cross-squad

### [SEED] Definicao de Quality Gate Cascade — 2026-03-01

**Contexto**: Necessidade de garantir qualidade em multiplas camadas sem criar bottleneck
**Opcoes**: (1) Gate unico final; (2) Gates por task; (3) Cascade de 5 niveis
**Decisao**: Opcao 3 — Cascade de 5 niveis (Agent → Task → Layer → Chief → Final)
**Raciocinio**: Gates em cascade detectam problemas mais cedo, reduzem rework no final, e permitem que cada camada valide dentro do seu dominio antes de passar adiante
**Responsavel**: Brand Chief
**Resultado**: Sistema de scoring GREEN/YELLOW/RED implementado com enforcement rules no config.yaml

### [SEED] Auditoria v3 — Routing e Cross-Squad Completo — 2026-03-19

**Contexto**: Auditoria v3 revelou 19 tasks sem routing no config.yaml, 2 arquivos referenciados mas inexistentes, e cross-squad limitado a 5 dos 12 squads MMOS
**Opcoes**: (1) Corrigir apenas os gaps criticos; (2) Corrigir tudo e expandir cross-squad; (3) Manter como esta
**Decisao**: Opcao 2 — Corrigir tudo e expandir cross-squad para 12 squads
**Raciocinio**: 19 tasks sem routing significava 28% das tasks invisiveis ao sistema de roteamento. Cross-squad limitado isolava o squad do ecossistema MMOS. Ambos sao gaps CRITICOS que impedem operacao real.
**Responsavel**: HRM Systems Architect (Auditoria v3)
**Resultado**: 19 routing entries adicionadas (100% coverage), 2 arquivos criados (zero refs quebradas), 7 squads adicionados (12/12 coverage), config.yaml v1.2.0

---

## Template de Registro

```
## [Titulo da Decisao] — YYYY-MM-DD

**Contexto**: [Por que essa decisao foi necessaria]
**Opcoes**: [O que foi considerado]
**Decisao**: [O que foi decidido]
**Raciocinio**: [Por que essa opcao foi escolhida]
**Responsavel**: [Quem tomou a decisao]
**Resultado** (preencher depois): [O que aconteceu]
```
