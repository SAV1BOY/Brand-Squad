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
