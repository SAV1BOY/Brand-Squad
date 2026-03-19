# Guia de Integracao Cross-Squad — Brand Squad

> Como o Brand Squad se conecta e colabora com outros squads do sistema MMOS.

---

## Principio

A marca e transversal — toca marketing, produto, vendas, cultura e design. O Brand Squad produz os fundamentos que outros squads usam para manter consistencia. Toda integracao segue contratos formais de handoff com quality gates obrigatorios.

---

## Integracoes Ativas

### Brand → Copy Squad
- **Assets entregues**: brand-voice-guide, positioning-statement, messaging-house, brand-archetypes
- **Shared assets**: phrases/tone-words-allowed, phrases/tone-words-forbidden, phrases/brand-descriptors-library
- **Quality bar**: GREEN em todos os checklists de identidade
- **Aceite**: Copy squad valida usabilidade dos assets para producao de copy
- **Recebe do Copy**: Feedback de performance de messaging, sugestoes de evolucao de tom
- **Cadencia**: Handoff a cada nova task de identidade verbal; sync mensal

### Brand → Marketing Squad
- **Assets entregues**: brand-guidelines, distinctive-assets-registry, campaign-frameworks
- **Quality bar**: GREEN em brand-guidelines-quality
- **Aceite**: Marketing squad confirma aplicabilidade para campanhas
- **Recebe do Marketing**: Dados de performance de campanha, feedback de mercado, brand tracking data
- **Cadencia**: Handoff a cada atualizacao de guidelines; sync mensal

### Brand → Product Squad
- **Assets entregues**: naming (shortlist + recomendacao final), ux-writing-principles, verbal-identity
- **Quality bar**: GREEN em naming-quality + brand-voice-quality
- **Aceite**: Product squad valida integracao com roadmap e interface
- **Recebe do Product**: Roadmap, feedback de usuarios sobre percepcao, nomenclatura proposta
- **Cadencia**: Handoff por demanda (novos features/produtos); sync mensal

### Brand → Design Squad
- **Assets entregues**: visual-guidelines, creative-direction, brand-assets, distinctive-assets-registry
- **Quality bar**: GREEN em visual-identity-quality
- **Aceite**: Design squad valida executabilidade dos guidelines
- **Recebe do Design**: Execucoes visuais, inovacoes de design, propostas de evolucao
- **Cadencia**: Handoff a cada atualizacao visual; sync mensal

### Brand → People/Culture Squad
- **Assets entregues**: employer-brand, EVP, brand-values, internal rollout playbook
- **Quality bar**: GREEN em brand-purpose-quality
- **Aceite**: People squad valida alinhamento cultural
- **Recebe do People**: Dados de eNPS, cultura real da equipe, feedback de onboarding
- **Cadencia**: Handoff a cada atualizacao de proposito/valores; sync trimestral

---

## Protocolo de Handoff

### Processo Padrao
```
1. Brand Squad conclui task com output aprovado (quality gate GREEN)
2. Brand Chief valida output consolidado (Chief Gate)
3. Final Gate verifica readiness para handoff
4. Empacotar assets conforme contrato do squad receptor
5. Entregar com documentacao de uso
6. Squad receptor valida aceite
7. Registrar em data/registries/handoff-log.md
8. Follow-up em 2 semanas para verificar adocao
```

### Quality Gates de Handoff
- Output deve ter passado TODOS os 5 niveis do quality gate cascade
- Score minimo: GREEN (>=80%) em todos os checklists do contrato
- YELLOW requer override documentado do Brand Chief
- RED bloqueia handoff — rework obrigatorio

### Rejeicao de Handoff
Se o squad receptor rejeitar os assets:
1. Documentar motivo da rejeicao
2. Registrar em handoff-log com status "rejeitado"
3. Gerar rework brief com feedback do receptor
4. Re-executar task com foco nos gaps identificados
5. Repassar pelo quality gate cascade
6. Novo handoff com verificacao especifica dos pontos rejeitados

---

## Regras de Colaboracao

1. Squads consultam Brand Squad antes de criar materiais de marca
2. Atualizacoes de marca sao comunicadas a todos os squads via cross-squad-brand-sync
3. Feedback cross-squad e coletado via sync mensal (task: cross-squad-brand-sync no config.yaml)
4. Conflitos sao escalados para Brand Chief → se nao resolver, HRM Chief
5. Brand Squad nao executa tasks fora do seu escopo — delega ao squad competente
6. Toda modificacao de assets ja entregues requer notificacao ao squad receptor

---

## Matriz de Integracao

| Squad Receptor | Assets Primarios | Quality Bar | Checklist Principal | Contrato |
|---------------|-----------------|-------------|--------------------|---------|
| Copy | voice-guide, positioning, messaging, archetypes | GREEN identidade | brand-voice-quality | brand_to_copy |
| Marketing | guidelines, distinctive-assets, campaigns | GREEN guidelines | brand-guidelines-quality | brand_to_marketing |
| Product | naming, ux-writing, verbal-identity | GREEN naming + voice | naming-quality | brand_to_product |
| Design | visual-guidelines, creative-direction, assets | GREEN visual | visual-identity-quality | brand_to_design |
| People | employer-brand, EVP, values | GREEN purpose | brand-purpose-quality | brand_to_people |

---

Referencia: `config.yaml` (handoff_contracts + cross_squad) | `docs/handoff-contracts-guide.md` | `data/registries/handoff-log.md`
