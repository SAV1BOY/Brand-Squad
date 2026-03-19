# Update Brand Guidelines
> Atualizacao periodica do brand book e guidelines de marca.

## Objetivo
Manter as brand guidelines atualizadas com as ultimas decisoes, novos assets, ajustes de identidade e aprendizados — garantindo que o documento de referencia reflita sempre o estado atual da marca.

## Agentes
- **alina-wheeler** — lidera a atualizacao das guidelines
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Guidelines versao atual
- Registro de decisoes de marca recentes
- Novos assets criados
- Feedback de usuarios das guidelines
- Violacoes identificadas em consistency reviews

## Passos
1. Revisar registro de decisoes desde ultima atualizacao
2. Identificar mudancas que impactam as guidelines
3. Atualizar secoes afetadas (visual, verbal, aplicacoes)
4. Adicionar novos exemplos e aplicacoes
5. Atualizar do's & don'ts com casos reais
6. Revisar secao de governanca e contatos
7. Versionar e documentar changelog
8. Distribuir nova versao e comunicar mudancas

## Frameworks Obrigatorios
- wheeler-brand-identity-process

## Checklists de Qualidade
- wheeler/brand-guidelines-audit
- brand-guidelines-quality

## Output Esperado
```
## Atualizacao de Guidelines
### Versao: [nova versao]
### Changelog: [lista de mudancas]
### Secoes Atualizadas: [lista]
### Novos Assets Incluidos: [lista]
### Do's & Don'ts Adicionados: [novos casos]
### Distribuicao: [para quem e quando]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines versao atual disponivel, registro de decisoes desde ultima atualizacao coletado
- Gate de saida: score GREEN (>=80%) nos checklists wheeler/brand-guidelines-audit e brand-guidelines-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre mudancas nas guidelines → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (secoes desatualizadas, changelog incompleto, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: consistency-review, guidelines-review, brand-governance-enforcement (violacoes que demandam atualizacao)
- Downstream: partner-alignment, internal-training (comunicacao de mudancas)
- Cross-squad: todos os squads (nova versao distribuida para todos os usuarios)

### Metricas
- Numero de secoes atualizadas por versao
- Tempo entre decisao de marca e atualizacao no brand book
- % de usuarios notificados sobre mudancas
