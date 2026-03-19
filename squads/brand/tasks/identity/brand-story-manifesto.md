# Brand Story Manifesto
> Criacao da narrativa de marca e manifesto inspirador.

## Objetivo
Desenvolver a historia da marca e um manifesto que capture sua essencia emocional — conectando proposito, valores e visao em uma narrativa envolvente que inspire equipe, parceiros e clientes.

## Agentes
- **donald-miller** — lidera a estrutura narrativa (StoryBrand)
- **emily-heyward** — garante autenticidade e impacto emocional
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand purpose e posicionamento
- StoryBrand BrandScript
- Brand archetype e personalidade
- Historia da empresa/fundadores
- Valores e visao

## Passos
1. Revisar proposito, valores e StoryBrand script
2. Identificar o "por que" emocional da marca
3. Construir arco narrativo da marca (origem, desafio, visao)
4. Redigir brand story (versao longa)
5. Redigir manifesto (versao inspiradora e concisa)
6. Criar versoes para diferentes formatos (video, apresentacao, site)
7. Testar impacto emocional com equipe interna
8. Documentar versoes finais

## Frameworks Obrigatorios
- brand-storytelling-framework
- miller-storybrand-sb7

## Checklists de Qualidade
- brand-narrative-quality

## Output Esperado
```
## Brand Story & Manifesto
### Brand Story (versao longa): [narrativa completa]
### Manifesto: [versao inspiradora, 200-400 palavras]
### Versao para Video: [roteiro resumido]
### Versao para Site: [texto adaptado]
### Versao Elevator (30s): [pitch emocional]
### Citacoes-Chave: [frases de impacto]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand purpose e posicionamento definidos, StoryBrand BrandScript concluido, brand archetype selecionado
- Gate de saida: score GREEN (>=80%) no checklist brand-narrative-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre donald-miller e emily-heyward sobre narrativa → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (narrativa desconectada do proposito, manifesto sem impacto emocional, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: define-brand-purpose, storybrand-script, brand-archetype-selection
- Downstream: internal-training, campaign-activation-brief, website-brand-implementation
- Cross-squad: people squad (manifesto para alinhamento cultural), marketing squad (brand story para campanhas)

### Metricas
- Score de impacto emocional (teste com equipe interna)
- Numero de versoes adaptadas por formato (video, site, apresentacao)
- Alinhamento com proposito e BrandScript (pass/fail)
