# ARCHITECTURE.md — Brand Squad (Mapa de Interconexao)

> Este documento e o mapa completo de dependencias, fluxos e interconexoes do Brand Squad.
> Ele mostra como cada diretorio se conecta e como os dados fluem pelo sistema.

---

## 1. Diagrama de Camadas

```
┌─────────────────────────────────────────────────────────────────┐
│                        BRAND SQUAD OS                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐   ┌──────────┐   │
│  │ RESEARCH │──▶│ STRATEGY │──▶│ IDENTITY │──▶│ACTIVATION│   │
│  └──────────┘   └──────────┘   └──────────┘   └──────────┘   │
│       │              │              │              │            │
│       ▼              ▼              ▼              ▼            │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                    GOVERNANCE                             │  │
│  └──────────────────────────────────────────────────────────┘  │
│       │              │              │              │            │
│       ▼              ▼              ▼              ▼            │
│  ┌──────────────────────────────────────────────────────────┐  │
│  │                   MEASUREMENT                             │  │
│  └──────────────────────────────────────────────────────────┘  │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

## 2. Fluxo de Dados Principal

```
Input do Projeto
       │
       ▼
┌─────────────┐     ┌──────────────┐     ┌──────────────┐
│   TASKS/    │────▶│   AGENTS/    │────▶│  FRAMEWORKS/ │
│ (o que fazer)│     │ (quem faz)   │     │ (como fazer) │
└─────────────┘     └──────────────┘     └──────────────┘
       │                   │                     │
       │                   ▼                     │
       │            ┌──────────────┐             │
       │            │  CHECKLISTS/ │◀────────────┘
       │            │(quality gate)│
       │            └──────────────┘
       │                   │
       ▼                   ▼
┌─────────────┐     ┌──────────────┐
│  TEMPLATES/ │────▶│    DATA/     │
│  (output)   │     │ (registro)   │
└─────────────┘     └──────────────┘
```

---

## 3. Mapa de Dependencias entre Diretorios

### 3.1 Dependencias Primarias
```
config.yaml
  ├── agents/          → Define quais agentes existem e seus roles
  ├── frameworks/      → Define quais frameworks cada task usa
  ├── checklists/      → Define quais checklists cada task requer
  ├── templates/       → Define quais templates cada task preenche
  └── data/registries/ → Define onde registrar resultados
```

### 3.2 Dependencias dos Agentes
```
agents/*.md
  ├── frameworks/      → Cada agente referencia seus frameworks favoritos
  ├── checklists/      → Cada agente aplica checklists especificos
  ├── reference/       → Cada agente cita livros e principios
  ├── voice/           → Agentes de messaging usam voice profiles
  └── lib/components/  → Agentes usam componentes reutilizaveis
```

### 3.3 Dependencias dos Workflows
```
workflows/*.md
  ├── tasks/           → Cada workflow orquestra multiplas tasks
  ├── agents/          → Cada workflow envolve agentes especificos
  ├── templates/       → Cada workflow gera outputs via templates
  └── checklists/      → Cada workflow passa por quality gates
```

### 3.4 Diretorios Independentes (sem dependencias de entrada)
```
reference/             → Material de consulta (livros, psicologia, industrias)
swipe/                 → Exemplos e inspiracao
archive/               → Cases historicos
authority/             → Estrategias de autoridade e confianca
phrases/               → Biblioteca de frases reutilizaveis
```

---

## 4. Agentes por Camada

### Layer 1 — Research
| Agente | Papel na Camada |
|--------|----------------|
| Brand Chief | Direciona escopo da pesquisa |
| Byron Sharp | CEPs, mental availability research |
| Kevin Keller | CBBE baseline measurement |
| Denise Yohn | Stakeholder e employee perception |

### Layer 2 — Strategy
| Agente | Papel na Camada |
|--------|----------------|
| Brand Chief | Integra e decide |
| David Aaker | Brand identity system, equity plan |
| Al Ries | Positioning, category creation |
| Marty Neumeier | Differentiation, simplicity |
| Kevin Keller | Brand resonance strategy |
| Jean-Noel Kapferer | Identity Prism |
| Byron Sharp | Distinctive assets strategy |

### Layer 3 — Identity
| Agente | Papel na Camada |
|--------|----------------|
| Brand Chief | Aprova identidade final |
| Alina Wheeler | Visual identity process, brand book |
| Emily Heyward | Creative consistency, "obviousness" |
| Donald Miller | Messaging, StoryBrand |
| Miller Sticky Brand | Stickiness e memorabilidade |
| Naming Strategist | Naming system |
| Archetype Consultant | Arquetipos e personalidade |
| Domain Scout | Dominios e handles |

### Layer 4 — Activation
| Agente | Papel na Camada |
|--------|----------------|
| Brand Chief | Coordena rollout |
| Denise Yohn | Internal alignment, training |
| Emily Heyward | Launch readiness |

### Layer 5 — Governance
| Agente | Papel na Camada |
|--------|----------------|
| Brand Chief | Enforce padres e aprovacoes |
| Alina Wheeler | Guidelines e touchpoints |
| Byron Sharp | Consistency de distinctive assets |

### Layer 6 — Measurement
| Agente | Papel na Camada |
|--------|----------------|
| Brand Chief | Decisoes baseadas em dados |
| Byron Sharp | Mental availability tracking |
| Kevin Keller | CBBE measurement |

---

## 5. Roteamento: config.yaml como Cerebro

O `config.yaml` conecta tudo. Para cada task:

```yaml
task-name:
  agents: [quem participa]
  frameworks: [quais frameworks aplicar]
  checklists: [quais quality gates passar]
  templates: [quais templates preencher]
  registry: [onde registrar resultado]
```

Consulte o `config.yaml` para o roteamento completo.

---

## 6. Cross-Squad Integration

### Brand → Copy Squad
```
brand/voice/brand-voices/         → copy/voice/brand-voices/
brand/frameworks/messaging-house  → copy/frameworks/
brand/templates/strategy/positioning-statement → copy/reference/
brand/checklists/archetypes/      → copy/voice/ (tom e personalidade)
```

### Shared Assets
```
brand/phrases/tone-words-allowed.md    ↔ copy/
brand/phrases/tone-words-forbidden.md  ↔ copy/
brand/phrases/brand-descriptors-library.md ↔ copy/
```

---

## 8. Quality Gate Cascade

O Brand Squad opera com quality gates em 5 niveis, em cascata. Nenhum output avanca sem passar pelo gate correspondente.

```
┌──────────────────────────────────────────────────────────────┐
│                    QUALITY GATE CASCADE                       │
├──────────────────────────────────────────────────────────────┤
│                                                                │
│  ┌─────────────┐                                              │
│  │ 1. AGENT    │  Cada agente valida seu proprio output       │
│  │    GATE     │  antes de entregar ao squad                  │
│  └──────┬──────┘                                              │
│         ▼                                                      │
│  ┌─────────────┐                                              │
│  │ 2. TASK     │  Checklists obrigatorios definidos no        │
│  │    GATE     │  config.yaml routing (por task)              │
│  └──────┬──────┘                                              │
│         ▼                                                      │
│  ┌─────────────┐                                              │
│  │ 3. LAYER    │  Layer transition gates que validam          │
│  │    GATE     │  completude antes de avancar de camada       │
│  └──────┬──────┘  (checklists/layer-gate-*.md)                │
│         ▼                                                      │
│  ┌─────────────┐                                              │
│  │ 4. CHIEF    │  brand-chief revisa output consolidado       │
│  │    GATE     │  e valida coerencia entre camadas            │
│  └──────┬──────┘                                              │
│         ▼                                                      │
│  ┌─────────────┐                                              │
│  │ 5. FINAL    │  Validacao antes de handoff cross-squad      │
│  │    GATE     │  ou entrega ao sistema maior                 │
│  └─────────────┘                                              │
│                                                                │
├──────────────────────────────────────────────────────────────┤
│  SCORING:  GREEN >=80%  │  YELLOW 60-79%  │  RED <60%        │
│  RED = bloqueado        │  YELLOW = chief override            │
├──────────────────────────────────────────────────────────────┤
│  Detalhes: docs/quality-gates-guide.md                        │
│  Config:   config.yaml → quality_gates                        │
└──────────────────────────────────────────────────────────────┘
```

### Layer Transition Gates
| Transicao | Checklist | Aprovadores |
|-----------|-----------|-------------|
| Research → Strategy | `checklists/layer-gate-research-to-strategy` | brand-chief, byron-sharp, kevin-keller |
| Strategy → Identity | `checklists/layer-gate-strategy-to-identity` | brand-chief, al-ries, david-aaker |
| Identity → Activation | `checklists/layer-gate-identity-to-activation` | brand-chief, alina-wheeler, emily-heyward |
| Activation → Governance | `checklists/layer-gate-activation-to-governance` | brand-chief, denise-yohn |

---

## 9. Learning & Memory System

O Brand Squad opera com um ciclo Kaizen continuo que transforma experiencia em melhoria.

```
┌──────────────────────────────────────────────────────┐
│                   KAIZEN LOOP                         │
│                                                        │
│     ┌──────────┐                                      │
│     │ EXECUTE  │  Executar task conforme routing       │
│     └────┬─────┘                                      │
│          ▼                                             │
│     ┌──────────┐                                      │
│     │ MEASURE  │  Avaliar via quality gates            │
│     └────┬─────┘                                      │
│          ▼                                             │
│     ┌──────────┐                                      │
│     │  LEARN   │  Registrar em learnings-log           │
│     └────┬─────┘                                      │
│          ▼                                             │
│     ┌──────────┐                                      │
│     │ IMPROVE  │  Alimentar improvement-backlog        │
│     └────┬─────┘                                      │
│          ▼                                             │
│     ┌──────────┐                                      │
│     │ EXECUTE  │  Proxima execucao incorpora melhoria  │
│     └──────────┘                                      │
└──────────────────────────────────────────────────────┘
```

### Registries de Memoria Operacional
| Registry | Arquivo | Captura |
|----------|---------|---------|
| Decisoes | `data/registries/brand-decisions-log` | Todas as decisoes estrategicas com racional |
| Premissas | `data/registries/assumptions-log` | Premissas feitas e seu status de validacao |
| Riscos | `data/registries/risk-log` | Riscos identificados e mitigacao |
| Aprendizados | `data/registries/learnings-log` | Licoes de sucesso e falha |
| Melhorias | `data/registries/improvement-backlog` | Oportunidades priorizadas |
| Handoffs | `data/registries/handoff-log` | Transferencias cross-squad |
| Claims | `data/registries/brand-claims-registry` | Promessas e RTBs da marca |
| Touchpoints | `data/registries/brand-touchpoints-registry` | Pontos de contato mapeados |
| Violacoes | `data/registries/brand-violations-log` | Desvios de guidelines |
| Assets | `data/registries/distinctive-assets-registry` | Ativos distintivos da marca |
| Naming | `data/registries/naming-registry` | Historico de naming |

Detalhes: `docs/learning-and-memory-guide.md`

---

## 10. Escalation & Rework

### Cadeia de Escalacao
```
┌─────────────┐     ┌──────────────┐     ┌──────────────┐
│  NIVEL 1    │────▶│   NIVEL 2    │────▶│   NIVEL 3    │
│ Agente      │     │ Brand Chief  │     │  HRM Chief   │
│ re-executa  │     │  arbitra     │     │ decisao final│
└─────────────┘     └──────────────┘     └──────────────┘
```

**Triggers de Escalacao:**
1. Quality gate RED apos 3 rework loops
2. Conflito entre 2+ agentes sem resolucao
3. Task fora do escopo do squad
4. Stakeholder override request
5. Deadline em risco

### Rework Loop
```
Output → Quality Gate → FAIL → Rework Brief → Re-execucao → Gate Retry
                                                     │
                                              Max 3 loops
                                                     │
                                          Se falhar → Escalacao
```

Detalhes: `docs/escalation-protocol.md` | `docs/rework-loops-guide.md`

---

## 11. HRM Governance Model

O Brand Squad opera dentro do modelo HRM (Hierarchical Role Modeling) com 4 niveis:

```
┌──────────────────────────────────────────────────────┐
│                  HRM GOVERNANCE                       │
├──────────────────────────────────────────────────────┤
│                                                        │
│  Nivel 4: HRM CHIEF (sistema)                         │
│  ├── Decisoes que impactam multiplos squads            │
│  ├── Arbitragem final de conflitos                     │
│  └── Aprovacao de mudancas estruturais                 │
│                                                        │
│  Nivel 3: BRAND CHIEF (squad)                          │
│  ├── Orquestra todos os agentes                        │
│  ├── Arbitra conflitos entre agentes                   │
│  ├── Override de quality gates YELLOW                   │
│  ├── Aprovacao final de outputs do squad               │
│  └── Coordena handoffs cross-squad                     │
│                                                        │
│  Nivel 2: TEAMS / SWARMS (funcional)                   │
│  ├── Strategy Team: Aaker + Keller + Ries + Neumeier  │
│  ├── Identity Team: Wheeler + Heyward + Miller         │
│  ├── Research Team: Sharp + Keller + Yohn              │
│  ├── Naming Swarm: Naming + Archetype + Domain         │
│  └── Coordenacao horizontal entre agentes              │
│                                                        │
│  Nivel 1: AGENTS (individual)                          │
│  ├── Executa tasks dentro do seu dominio               │
│  ├── Aplica frameworks e checklists                    │
│  ├── Valida output via agent gate                      │
│  ├── Sabe quando escalar                               │
│  └── Sabe quando delegar                               │
│                                                        │
├──────────────────────────────────────────────────────┤
│  Principio: cada nivel so escala quando esgota         │
│  suas opcoes de resolucao                              │
└──────────────────────────────────────────────────────┘
```

### Quando Cada Nivel Intervem
| Nivel | Intervem Quando |
|-------|-----------------|
| Agent | Task esta no seu dominio e ele tem frameworks/checklists adequados |
| Team/Swarm | Task requer coordenacao entre multiplos agentes do mesmo dominio |
| Brand Chief | Conflito entre agentes, quality gate YELLOW, output consolidado, handoff cross-squad |
| HRM Chief | Impacto cross-squad, mudanca estrutural, gate RED apos 3 loops, decisao irreversivel |

---

## 7. Glossario

| Termo | Definicao |
|-------|-----------|
| **HRM** | Hierarchical Role Modeling — metodologia de estruturacao de agentes em hierarquia |
| **CEP** | Category Entry Point — situacao em que o consumidor pensa na categoria |
| **CBBE** | Customer-Based Brand Equity — modelo de Keller (piramide) |
| **RTB** | Reason-to-Believe — prova que sustenta a promessa de marca |
| **STP** | Segmentation, Targeting, Positioning |
| **SB7** | StoryBrand 7-Part Framework de Donald Miller |
| **EVP** | Employee Value Proposition |
| **Brand Prism** | Modelo de 6 facetas de identidade de marca (Kapferer) |
| **Distinctive Assets** | Elementos sensoriais que identificam a marca sem o nome (Sharp) |
| **Brand Gap** | Distancia entre estrategia e execucao criativa (Neumeier) |
| **Zag** | Radical differentiation — ir contra quando todos vao a favor (Neumeier) |
| **Brand Mantra** | Essencia da marca em 3-5 palavras (Keller) |
| **Mental Availability** | Probabilidade de a marca ser lembrada em situacao de compra (Sharp) |
| **Physical Availability** | Facilidade de encontrar e comprar a marca (Sharp) |
