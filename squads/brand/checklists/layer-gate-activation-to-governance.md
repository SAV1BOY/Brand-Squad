# Gate de Transicao: Activation → Governance & Measurement
> Valida que a ativacao da marca foi executada com sucesso antes de transicionar para modo de governanca e medicao continua. Este gate marca a passagem de "construcao" para "manutencao e crescimento".

---

## Pre-condicoes

Os seguintes artefatos devem existir antes de aplicar este gate:

- [ ] Treinamento interno realizado conforme `yohn-brand-as-business` e `internal-rollout-quality`
- [ ] Migracao de touchpoints completa conforme `brand-experience-map`
- [ ] Coordenacao de lancamento executada conforme `activation-layer`
- [ ] Alinhamento com parceiros concluido e registrado
- [ ] Handoffs cross-squad executados conforme `config.yaml` cross_squad

---

## Criterios de Aprovacao

### Ativacao Interna
- [ ] Colaboradores treinados na nova marca com taxa de conclusao >= 90%
- [ ] Brand ambassadors internos identificados e ativados
- [ ] Cultura interna alinhada com promessa externa conforme `yohn-fusion`
- [ ] Materiais de onboarding atualizados com nova identidade

### Ativacao Externa
- [ ] Todos os touchpoints prioritarios migrados para nova identidade
- [ ] Website, redes sociais e canais digitais atualizados e ao vivo
- [ ] Materiais de comunicacao (templates, assinaturas, apresentacoes) distribuidos
- [ ] Lancamento executado conforme plano aprovado no checklist `criterios-lancamento`

### Handoffs e Integracao
- [ ] Brand voice guide entregue ao Copy Squad conforme `cross_squad.copy.handoff_from_brand`
- [ ] Fornecedores e parceiros receberam brand guidelines atualizadas
- [ ] Processos de aprovacao de uso de marca estabelecidos conforme `brand-governance-model`
- [ ] Baseline de metricas coletada para brand tracking futuro

---

## Quem Aprova

| Papel | Agente | Obrigatorio |
|-------|--------|-------------|
| Orquestrador | brand-chief | Sim |
| Especialista Activation/Culture | denise-yohn | Sim |

Aprovacao requer consenso dos 2 agentes. Brand-chief tem voto de minerva.

---

## Scoring

| Bloco | Itens OK | Total | % |
|-------|----------|-------|---|
| Pre-condicoes | ___ | 5 | ___% |
| Ativacao Interna | ___ | 4 | ___% |
| Ativacao Externa | ___ | 4 | ___% |
| Handoffs e Integracao | ___ | 4 | ___% |
| **TOTAL** | ___ | **17** | ___% |

### Classificacao

- **Verde (>=80%):** Gate aprovado — transicionar para modo Governance & Measurement
- **Amarelo (60-79%):** Gate condicional — requer override explicito do brand-chief com justificativa registrada
- **Vermelho (<60%):** Gate BLOQUEADO — retornar para Activation obrigatoriamente

---

## Se Falhar

1. Rework brief gerado automaticamente com itens reprovados e feedback especifico
2. Tasks re-atribuidas aos agentes de Activation responsaveis (denise-yohn, alina-wheeler, emily-heyward)
3. Maximo de 3 loops de rework permitidos
4. Apos 3 loops sem aprovacao, escalar para revisao manual com stakeholders do projeto
5. Cada loop de rework deve ser registrado em `data/registries/brand-decisions-log`

---

## Registro

- Resultado do gate registrado em: `data/registries/brand-decisions-log`
- Formato: data | gate | resultado | score | aprovadores | observacoes

---

## Frameworks Relacionados

- `yohn-brand-as-business`
- `yohn-fusion`
- `activation-layer`
- `brand-experience-map`
- `brand-governance-model`
- `brand-consistency-model`

---

## Conexao

Apos aprovacao, iniciar modo de operacao continua conforme `config.yaml` routing: tasks de Governance (brand-governance-setup, update-brand-guidelines, maintain-distinctive-assets-registry) e Measurement (brand-tracking-analysis, quarterly-brand-review, brand-equity-valuation-analysis).
