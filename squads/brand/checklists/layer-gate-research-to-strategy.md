# Gate de Transicao: Research → Strategy
> Valida que todas as entregas de Research estao completas e com qualidade suficiente antes de iniciar o trabalho de Strategy. Nenhuma task de Strategy deve comecar sem aprovacao neste gate.

---

## Pre-condicoes

Os seguintes artefatos devem existir antes de aplicar este gate:

- [ ] Brand audit completo e registrado em `data/registries/brand-decisions-log`
- [ ] Pesquisa de concorrentes e categoria documentada em `data/research/competitor-research`
- [ ] Entrevistas com clientes conduzidas e registradas em `data/research/interview-notes`
- [ ] Estudo de percepcao de marca (perception study) finalizado em `data/research/survey-results`
- [ ] Category entry points mapeados conforme framework `category-entry-points`
- [ ] Inventario de touchpoints existente em `data/registries/brand-touchpoints-registry`

---

## Criterios de Aprovacao

### Completude de Pesquisa
- [ ] Relatorio de brand audit entregue com base nos frameworks `aaker-brand-equity-model` e `keller-cbbe-pyramid`
- [ ] Mapeamento competitivo inclui no minimo 5 concorrentes diretos com analise de posicionamento
- [ ] Analise de distinctive assets existentes documentada conforme `distinctive-assets-system`
- [ ] Category entry points identificados com evidencia de dados (nao apenas opiniao)
- [ ] Resultados de social listening ou VoC mining registrados em `data/research/voc-dumps`

### Profundidade de Insights
- [ ] Percepcao atual da marca documentada com piramide CBBE preenchida
- [ ] Gaps entre identidade desejada e imagem percebida identificados
- [ ] Jobs-to-be-done do publico-alvo mapeados com base em entrevistas reais
- [ ] Semiotica da categoria analisada (codigos visuais e verbais dominantes)
- [ ] Brand salience atual mensurada conforme `brand-salience-heuristics`

### Qualidade e Registro
- [ ] Todos os dados brutos organizados nas pastas de registry correspondentes
- [ ] Resumo executivo de Research produzido com insights priorizados
- [ ] Premissas e limitacoes da pesquisa declaradas explicitamente
- [ ] Fontes e metodologias documentadas para cada insight
- [ ] Brief de transicao para Strategy redigido com base nos achados

---

## Quem Aprova

| Papel | Agente | Obrigatorio |
|-------|--------|-------------|
| Orquestrador | brand-chief | Sim |
| Especialista Research/Growth | byron-sharp | Sim |
| Especialista Research/Equity | kevin-keller | Sim |

Aprovacao requer consenso dos 3 agentes. Em caso de divergencia, brand-chief tem voto de minerva.

---

## Scoring

| Bloco | Itens OK | Total | % |
|-------|----------|-------|---|
| Pre-condicoes | ___ | 6 | ___% |
| Completude de Pesquisa | ___ | 5 | ___% |
| Profundidade de Insights | ___ | 5 | ___% |
| Qualidade e Registro | ___ | 5 | ___% |
| **TOTAL** | ___ | **21** | ___% |

### Classificacao

- **Verde (>=80%):** Gate aprovado — iniciar tasks de Strategy
- **Amarelo (60-79%):** Gate condicional — requer override explicito do brand-chief com justificativa registrada
- **Vermelho (<60%):** Gate BLOQUEADO — retornar para Research obrigatoriamente

---

## Se Falhar

1. Rework brief gerado automaticamente com itens reprovados e feedback especifico
2. Tasks re-atribuidas aos agentes de Research responsaveis (byron-sharp, kevin-keller, denise-yohn)
3. Maximo de 3 loops de rework permitidos
4. Apos 3 loops sem aprovacao, escalar para revisao manual com stakeholders do projeto
5. Cada loop de rework deve ser registrado em `data/registries/brand-decisions-log`

---

## Registro

- Resultado do gate registrado em: `data/registries/brand-decisions-log`
- Formato: data | gate | resultado | score | aprovadores | observacoes

---

## Frameworks Relacionados

- `discovery-and-research`
- `brand-salience-heuristics`
- `keller-cbbe-pyramid`
- `category-entry-points`
- `distinctive-assets-system`

---

## Conexao

Apos aprovacao, iniciar tasks de Strategy conforme `config.yaml` routing (positioning-development, define-brand-purpose, define-brand-promise, messaging-house-development, brand-architecture-design, define-distinctive-assets, brand-equity-plan).
