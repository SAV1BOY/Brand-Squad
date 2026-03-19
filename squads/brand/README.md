# Brand Squad — MMOS Brand Strategy + Identity OS

> Sistema operacional completo de **Brand Strategy + Brand Identity** do MMOS.
> 15 agentes especializados | ~727 arquivos | Metodologia HRM | Gold-standard SOTA.

---

## Visao Geral

O Brand Squad e o sistema de inteligencia de marca do MMOS. Ele cobre todo o ciclo de vida de uma marca:

```
Research → Strategy → Identity → Activation → Governance → Measurement
```

Cada camada possui **agentes especializados**, **frameworks**, **checklists de qualidade**, **templates de entregaveis**, **tasks executaveis** e **workflows ponta-a-ponta**.

---

## Estrutura do Repositorio

```
squads/brand/
├── agents/          # 15 agentes (perfis HRM com prompt de ativacao)
├── archive/         # Cases historicos, rebrands, evolucao
├── authority/       # Autoridade, confianca, reputacao
├── checklists/      # 100+ quality gates por entregavel e autor
├── data/            # Pesquisa, registros operacionais, metricas
├── docs/            # Documentacao do squad
├── frameworks/      # 90+ frameworks de branding
├── lib/             # Componentes, patterns e utilities reutilizaveis
├── phrases/         # Biblioteca de frases e blocos de mensagem
├── projects/        # Templates de projeto (brand do zero, rebrand, etc.)
├── reference/       # 85+ livros, psicologia, industrias
├── scripts/         # Automacao e consistencia
├── swipe/           # Swipe files de marca (exemplos)
├── swipe-sources/   # Fontes e indices de swipe
├── tasks/           # 70+ tarefas executaveis
├── templates/       # 75+ templates de entregaveis
├── voice/           # Voz, tom, calibracao, adaptacao por canal
├── workflows/       # 20 fluxos ponta-a-ponta
├── ARCHITECTURE.md  # Mapa de interconexao do squad
├── config.yaml      # Cerebro de roteamento (task → agents → frameworks → checklists → templates)
├── README.md        # Este arquivo
└── swipe.config     # Configuracao do sistema de swipe files
```

---

## Os 15 Agentes do Brand Squad

### Estrategia, Equity & Construcao de Marca
| Agente | Dominio | Obra de Referencia |
|--------|---------|-------------------|
| **Brand Chief** | Orquestrador geral | Integra todos os frameworks |
| **David Aaker** | Brand equity, identity system, architecture | Building Strong Brands |
| **Kevin Keller** | CBBE, brand resonance | Strategic Brand Management |
| **Jean-Noel Kapferer** | Identity Prism, luxury branding | The New Strategic Brand Management |
| **Byron Sharp** | Mental/physical availability, distinctive assets | How Brands Grow |
| **Denise Yohn** | Brand as business, internal alignment | What Great Brands Do |

### Posicionamento, Categoria & Vantagem Competitiva
| Agente | Dominio | Obra de Referencia |
|--------|---------|-------------------|
| **Al Ries** | Positioning, category creation, focus | Positioning: The Battle for Your Mind |
| **Marty Neumeier** | Brand Gap, simplicity, differentiation | The Brand Gap / Zag |

### Identidade, Sistema Visual & Diretrizes
| Agente | Dominio | Obra de Referencia |
|--------|---------|-------------------|
| **Alina Wheeler** | Brand identity process, brand book | Designing Brand Identity |
| **Emily Heyward** | "Obviousness", creative consistency | Obsessed |

### Mensagem, Narrativa & Clareza
| Agente | Dominio | Obra de Referencia |
|--------|---------|-------------------|
| **Donald Miller** | StoryBrand SB7, messaging | Building a StoryBrand |
| **Miller Sticky Brand** | Mensagens que colam | StoryBrand + stickiness |

### Operacoes Especiais
| Agente | Dominio | Obra de Referencia |
|--------|---------|-------------------|
| **Naming Strategist** | Naming systems, shortlists, testes | Naming methodologies |
| **Archetype Consultant** | Arquetipos de marca, personalidade | Hero and the Outlaw |
| **Domain Scout** | Dominios, handles, disponibilidade | Domain heuristics |

---

## Como Funciona

### 1. Cerebro de Roteamento (config.yaml)
Para cada **task**, o `config.yaml` define:
- Quais **agentes** participam
- Quais **frameworks** sao obrigatorios
- Quais **checklists** devem ser passados
- Quais **templates** geram o output
- Onde **registrar** o resultado

### 2. Fluxo de Execucao
```
Task → Agentes consultam Frameworks → Executam → Passam Checklists → Preenchem Templates → Registram em Data
```

### 3. Camadas do Sistema
```
Layer 1: Research      → Pesquisa, auditoria, entrevistas, VOC
Layer 2: Strategy      → Posicionamento, promessa, CEPs, arquitetura
Layer 3: Identity      → Nome, voz, assets, guidelines
Layer 4: Activation    → Rollout, treinamento, launch
Layer 5: Governance    → Padroes, aprovacoes, guardrails
Layer 6: Measurement   → Tracking, KPIs, decisoes
```

---

## Quality Gates & Governance

O Brand Squad opera com quality gates em 5 niveis em cascata:
1. **Agent Gate** — cada agente valida seu output
2. **Task Gate** — checklists obrigatorios por task (config.yaml)
3. **Layer Gate** — validacao entre camadas (checklists/layer-gate-*.md)
4. **Chief Gate** — brand-chief revisa output consolidado
5. **Final Gate** — validacao antes de handoff cross-squad

Scoring: GREEN (>=80%) | YELLOW (60-79%, chief override) | RED (<60%, bloqueado)

Docs: `docs/quality-gates-guide.md` | `docs/escalation-protocol.md` | `docs/rework-loops-guide.md`

---

## Operational Memory

O squad registra tudo em memoria operacional via Kaizen loop:
- `data/registries/brand-decisions-log` — decisoes estrategicas
- `data/registries/assumptions-log` — premissas para validacao
- `data/registries/risk-log` — riscos identificados
- `data/registries/learnings-log` — licoes aprendidas
- `data/registries/improvement-backlog` — melhorias priorizadas
- `data/registries/handoff-log` — transferencias cross-squad

Docs: `docs/learning-and-memory-guide.md`

---

## Cross-Squad Integration

O Brand Squad alimenta 5 squads com contratos formais de handoff:

| Squad Receptor | Assets Transferidos | Quality Bar |
|---------------|---------------------|-------------|
| **Copy** | brand-voice-guide, positioning, messaging-house, archetypes | GREEN em checklists de identidade |
| **Marketing** | brand-guidelines, distinctive-assets, campaign-frameworks | GREEN em brand-guidelines-quality |
| **Product** | naming, ux-writing-principles, verbal-identity | GREEN em naming + voice quality |
| **Design** | visual-guidelines, creative-direction, brand-assets | GREEN em visual-identity-quality |
| **People** | employer-brand, EVP, brand-values | GREEN em brand-purpose-quality |

Docs: `docs/handoff-contracts-guide.md` | `docs/cross-squad-integration-guide.md`

---

## Quick Start

1. Leia o `ARCHITECTURE.md` para entender o mapa completo
2. Consulte `docs/getting-started.md` para comecar
3. Escolha uma task em `tasks/` e siga o workflow correspondente
4. Use o `config.yaml` para saber quais agentes, frameworks e checklists usar

---

## Teams & Swarms

| Agrupamento | Membros | Coordenador |
|-------------|---------|-------------|
| Strategy Team | Aaker, Keller, Ries, Neumeier | Aaker |
| Identity Team | Wheeler, Heyward, Miller, Miller Sticky | Wheeler |
| Research Team | Sharp, Keller, Yohn | Sharp |
| Naming Swarm | Naming Strategist, Archetype, Domain Scout | Naming Strategist |

Docs: `docs/agent-roles-guide.md` | `ARCHITECTURE.md` (secao 11)

---

## Versao

- **Squad:** Brand Strategy + Identity
- **Versao:** 1.1.0
- **Agentes:** 15
- **Teams/Swarms:** 3 teams + 1 swarm
- **Arquivos:** ~730+
- **Metodologia:** HRM (Hierarchical Role Modeling)
- **Ultima auditoria:** 2026-03-19
