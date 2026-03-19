# Gate de Transicao: Identity → Activation
> Valida que todos os elementos de identidade estao finalizados e aprovados antes de iniciar ativacao. Ativar uma marca com identidade incompleta gera inconsistencia irreversivel no mercado.

---

## Pre-condicoes

Os seguintes artefatos devem existir antes de aplicar este gate:

- [ ] Naming finalizado, validado legalmente e registrado em `data/registries/naming-registry`
- [ ] Brand voice desenvolvida e documentada conforme `verbal-identity-system`
- [ ] Direcao de identidade visual aprovada conforme `wheeler-brand-identity-process`
- [ ] Brand guidelines criadas e validadas pelo checklist `brand-guidelines-quality`
- [ ] Brand story e manifesto escritos conforme `brand-storytelling-framework`
- [ ] Identidade verbal completa (tagline, tom de voz, lexicon) registrada
- [ ] Dominio principal e handles assegurados conforme `domain-heuristics`

---

## Criterios de Aprovacao

### Identidade Visual
- [ ] Logo finalizado em todos os formatos necessarios (RGB, CMYK, positivo, negativo, monocromatico)
- [ ] Paleta de cores definida com codigos exatos (HEX, RGB, CMYK, Pantone)
- [ ] Tipografia primaria e secundaria selecionadas com licencas garantidas
- [ ] Sistema de imagistica e iconografia documentado
- [ ] Aplicacoes minimas testadas (cartao de visita, assinatura de email, redes sociais)

### Identidade Verbal
- [ ] Naming aprovado nos checklists `naming-quality` e screening legal
- [ ] Tagline finalizada e validada pelo checklist `tagline-quality`
- [ ] Tom de voz documentado com exemplos de DO e DON'T
- [ ] Messaging house traduzida em copy real para touchpoints prioritarios
- [ ] Brand lexicon (vocabulario permitido e proibido) compilado

### Consistencia e Governanca
- [ ] Brand book completo e distribuivel conforme `brand-guidelines/brand-book-template`
- [ ] Distinctive assets catalogados no `data/registries/distinctive-assets-registry`
- [ ] Teste de obviousness realizado conforme `heyward-obviousness-method`
- [ ] Coerencia entre identidade visual e verbal validada
- [ ] Arquivos finais organizados e acessiveis para equipe de ativacao

---

## Quem Aprova

| Papel | Agente | Obrigatorio |
|-------|--------|-------------|
| Orquestrador | brand-chief | Sim |
| Especialista Identity/Systems | alina-wheeler | Sim |
| Especialista Identity/Launch | emily-heyward | Sim |

Aprovacao requer consenso dos 3 agentes. Em caso de divergencia, brand-chief tem voto de minerva.

---

## Scoring

| Bloco | Itens OK | Total | % |
|-------|----------|-------|---|
| Pre-condicoes | ___ | 7 | ___% |
| Identidade Visual | ___ | 5 | ___% |
| Identidade Verbal | ___ | 5 | ___% |
| Consistencia e Governanca | ___ | 5 | ___% |
| **TOTAL** | ___ | **22** | ___% |

### Classificacao

- **Verde (>=80%):** Gate aprovado — iniciar tasks de Activation
- **Amarelo (60-79%):** Gate condicional — requer override explicito do brand-chief com justificativa registrada
- **Vermelho (<60%):** Gate BLOQUEADO — retornar para Identity obrigatoriamente

---

## Se Falhar

1. Rework brief gerado automaticamente com itens reprovados e feedback especifico
2. Tasks re-atribuidas aos agentes de Identity responsaveis (alina-wheeler, emily-heyward, donald-miller, naming-strategist)
3. Maximo de 3 loops de rework permitidos
4. Apos 3 loops sem aprovacao, escalar para revisao manual com stakeholders do projeto
5. Cada loop de rework deve ser registrado em `data/registries/brand-decisions-log`

---

## Registro

- Resultado do gate registrado em: `data/registries/brand-decisions-log`
- Formato: data | gate | resultado | score | aprovadores | observacoes

---

## Frameworks Relacionados

- `wheeler-brand-identity-process`
- `heyward-obviousness-method`
- `verbal-identity-system`
- `brand-storytelling-framework`
- `naming-systems`
- `domain-heuristics`
- `distinctive-assets-system`

---

## Conexao

Apos aprovacao, iniciar tasks de Activation conforme `config.yaml` routing (internal-training, touchpoint-migration, launch-coordination, partner-alignment).
