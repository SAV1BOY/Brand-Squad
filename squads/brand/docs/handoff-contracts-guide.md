# Guia de Handoff Contracts — Brand Squad

> Contratos formais de transferencia de assets entre o Brand Squad e outros squads do sistema.

---

## Objetivo

Garantir que toda transferencia de assets de marca entre squads seja formal, rastreavel e com qualidade assegurada. Nenhum asset sai do Brand Squad sem validacao, e nenhum squad receptor aceita assets sem verificacao.

---

## Principio

Um handoff nao e "enviar arquivos". E uma transferencia formal com:
- Assets definidos
- Qualidade validada
- Responsaveis identificados
- Aceitacao confirmada
- Feedback coletado

---

## Template de Contrato

```
## Handoff Contract — Brand → [Squad Receptor]

**Data:** YYYY-MM-DD
**Sender:** Brand Squad / [agente responsavel]
**Receiver:** [Squad] / [agente receptor]

### Assets Transferidos
- [ ] [asset 1] — [descricao + localizacao]
- [ ] [asset 2] — [descricao + localizacao]

### Quality Bar
- Score minimo: GREEN (>=80%) em [checklist especifico]
- Revisado por: brand-chief

### SLA
- Prazo de preparacao: [X dias]
- Sessao de alinhamento: [data]
- Follow-up: [data]

### Acceptance Criteria (Receptor)
- [ ] Assets estao completos e utilizaveis
- [ ] Linguagem e formato sao adequados ao squad receptor
- [ ] Duvidas foram esclarecidas na sessao de alinhamento
- [ ] Squad receptor consegue aplicar os assets sem suporte adicional

### Escalation
- Se rejeitado: brand-chief revisa e ajusta em [X dias]
- Se impasse: HRM Chief arbitra

### Feedback Loop
- Receptor envia feedback em ate [X dias] apos adocao
- Brand Squad ajusta se necessario
```

---

## Contratos Ativos

### Brand → Copy Squad
| Item | Detalhe |
|------|---------|
| Assets | Brand Voice Guide, Positioning Statement, Messaging House, Brand Archetypes |
| Quality Bar | GREEN em brand-voice-quality + positioning-quality + brand-messaging-quality |
| Shared Assets | phrases/tone-words-allowed, phrases/tone-words-forbidden, phrases/brand-descriptors-library |
| SLA | 5 dias uteis apos finalizacao da identidade |
| Acceptance | Copy Squad valida usabilidade e aplicabilidade dos assets |

### Brand → Marketing Squad
| Item | Detalhe |
|------|---------|
| Assets | Brand Guidelines, Distinctive Assets Registry, Campaign Frameworks |
| Quality Bar | GREEN em brand-guidelines-quality + distinctive-assets-quality |
| SLA | 5 dias uteis apos aprovacao de guidelines |
| Acceptance | Marketing Squad confirma aplicabilidade em campanhas |

### Brand → Product Squad
| Item | Detalhe |
|------|---------|
| Assets | Naming (produtos/features), UX Writing Principles, Verbal Identity |
| Quality Bar | GREEN em naming-quality + brand-voice-quality |
| SLA | 3 dias uteis apos naming aprovado |
| Acceptance | Product Squad valida integracao com produto |

### Brand → Design Squad
| Item | Detalhe |
|------|---------|
| Assets | Visual Guidelines, Creative Direction, Brand Assets |
| Quality Bar | GREEN em visual-identity-quality |
| SLA | 5 dias uteis apos identidade visual aprovada |
| Acceptance | Design Squad valida executabilidade dos guidelines |

### Brand → People/Culture Squad
| Item | Detalhe |
|------|---------|
| Assets | Employer Brand Framework, EVP, Brand Values |
| Quality Bar | GREEN em brand-purpose-quality |
| SLA | 10 dias uteis apos estrategia aprovada |
| Acceptance | People Squad valida alinhamento cultural |

---

## Processo de Handoff

1. **Preparacao** — brand-chief identifica assets e squad receptor
2. **Validacao** — assets passam por quality gate pre-handoff (Final Gate)
3. **Empacotamento** — agentes preparam pacote personalizado por squad
4. **Sessao de Alinhamento** — apresentacao ao squad receptor com Q&A
5. **Entrega Formal** — assets transferidos, contrato assinado
6. **Follow-up** — monitoramento de adocao (2 semanas)
7. **Feedback** — receptor envia feedback, Brand Squad ajusta se necessario

---

## Registro

Todos os handoffs sao registrados em `data/registries/handoff-log` com:
- Data, sender, receiver
- Assets transferidos
- Quality score
- Aceito sim/nao
- Feedback recebido

---

## Conexoes

- **Cross-Squad Integration Guide:** `docs/cross-squad-integration-guide.md`
- **Cross-Squad Handoff Workflow:** `workflows/cross-squad-handoff-workflow.md`
- **Config.yaml:** `config.yaml → handoff_contracts`
- **Handoff Log:** `data/registries/handoff-log`
