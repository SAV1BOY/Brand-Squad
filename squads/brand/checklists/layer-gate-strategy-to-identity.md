# Gate de Transicao: Strategy → Identity
> Valida que todas as entregas de Strategy estao completas e coerentes antes de iniciar o trabalho de Identity. Construir identidade sem estrategia solida e construir sobre areia.

---

## Pre-condicoes

Os seguintes artefatos devem existir antes de aplicar este gate:

- [ ] Posicionamento definido e aprovado conforme `ries-positioning` e `neumeier-brand-gap`
- [ ] Proposito de marca documentado conforme `brand-purpose-framework`
- [ ] Brand promise e RTBs registrados em `data/registries/brand-claims-registry`
- [ ] Messaging house construida conforme `messaging-house` e `miller-storybrand-sb7`
- [ ] Arquitetura de marca desenhada conforme `brand-architecture-models`
- [ ] Distinctive assets definidos conforme `distinctive-assets-system`
- [ ] Plano de brand equity criado conforme `aaker-brand-equity-model` e `keller-cbbe-pyramid`

---

## Criterios de Aprovacao

### Solidez Estrategica
- [ ] Positioning statement finalizado e validado pelo checklist `positioning-quality`
- [ ] Proposito de marca e diferenciador central claramente articulados
- [ ] Brand promise testada quanto a credibilidade e relevancia
- [ ] RTBs (Reasons to Believe) documentados com evidencias concretas
- [ ] Onlyness statement definido conforme framework `neumeier-zag-method`

### Arquitetura e Estrutura
- [ ] Modelo de arquitetura de marca selecionado e justificado (monolitica, endorsed, independente)
- [ ] Hierarquia de mensagens definida no messaging house com 3+ niveis
- [ ] Category entry points priorizados para ativacao de mental availability
- [ ] Segmentacao de publico-alvo refinada com personas estrategicas
- [ ] StoryBrand script (SB7) validado pelo checklist `brand-messaging-quality`

### Planejamento de Equity
- [ ] KPIs de brand equity definidos com baseline e metas
- [ ] Piramide CBBE projetada com associacoes desejadas por nivel
- [ ] Distinctive assets planejados (quais criar, quais fortalecer, quais abandonar)
- [ ] Estrategia de mental e physical availability documentada
- [ ] Todas as decisoes estrategicas registradas em `data/registries/brand-decisions-log`

---

## Quem Aprova

| Papel | Agente | Obrigatorio |
|-------|--------|-------------|
| Orquestrador | brand-chief | Sim |
| Especialista Positioning | al-ries | Sim |
| Especialista Equity/Identity | david-aaker | Sim |

Aprovacao requer consenso dos 3 agentes. Em caso de divergencia, brand-chief tem voto de minerva.

---

## Scoring

| Bloco | Itens OK | Total | % |
|-------|----------|-------|---|
| Pre-condicoes | ___ | 7 | ___% |
| Solidez Estrategica | ___ | 5 | ___% |
| Arquitetura e Estrutura | ___ | 5 | ___% |
| Planejamento de Equity | ___ | 5 | ___% |
| **TOTAL** | ___ | **22** | ___% |

### Classificacao

- **Verde (>=80%):** Gate aprovado — iniciar tasks de Identity
- **Amarelo (60-79%):** Gate condicional — requer override explicito do brand-chief com justificativa registrada
- **Vermelho (<60%):** Gate BLOQUEADO — retornar para Strategy obrigatoriamente

---

## Se Falhar

1. Rework brief gerado automaticamente com itens reprovados e feedback especifico
2. Tasks re-atribuidas aos agentes de Strategy responsaveis (al-ries, david-aaker, donald-miller, marty-neumeier)
3. Maximo de 3 loops de rework permitidos
4. Apos 3 loops sem aprovacao, escalar para revisao manual com stakeholders do projeto
5. Cada loop de rework deve ser registrado em `data/registries/brand-decisions-log`

---

## Registro

- Resultado do gate registrado em: `data/registries/brand-decisions-log`
- Formato: data | gate | resultado | score | aprovadores | observacoes

---

## Frameworks Relacionados

- `ries-positioning`
- `neumeier-brand-gap`
- `brand-purpose-framework`
- `miller-storybrand-sb7`
- `brand-architecture-models`
- `aaker-brand-equity-model`
- `keller-cbbe-pyramid`

---

## Conexao

Apos aprovacao, iniciar tasks de Identity conforme `config.yaml` routing (naming-workshop, brand-voice-development, visual-identity-direction, brand-guidelines-creation, brand-story-manifesto, verbal-identity-development, domain-scouting).
