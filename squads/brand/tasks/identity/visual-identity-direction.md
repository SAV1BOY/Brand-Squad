# Visual Identity Direction
> Definicao da direcao criativa para a identidade visual da marca.

## Objetivo
Estabelecer a direcao criativa da identidade visual — moodboard, paleta de cores, tipografia, estilo fotografico e sistema de layout — criando uma linguagem visual unica e consistente.

## Agentes
- **alina-wheeler** — lidera o processo de identidade visual
- **emily-heyward** — valida obviedade e impacto visual
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Strategy Document
- Brand archetype e personalidade
- Analise semiotica da categoria
- Distinctive assets definidos
- Referencias visuais de concorrentes

## Passos
1. Traduzir estrategia e personalidade em conceitos visuais
2. Criar moodboard de direcao criativa
3. Definir paleta de cores (primaria e secundaria)
4. Selecionar sistema tipografico (fontes)
5. Definir estilo fotografico e de ilustracao
6. Criar principios de layout e grid
7. Desenvolver sistema de icones e grafismos
8. Consolidar em identity design brief

## Frameworks Obrigatorios
- wheeler-brand-identity-process
- heyward-obviousness-method
- identity-layer

## Checklists de Qualidade
- wheeler/identity-system-audit
- visual-identity-quality

## Output Esperado
```
## Visual Identity Direction
### Conceito Criativo: [narrativa visual]
### Moodboard: [referencias visuais]
### Paleta de Cores: [primaria + secundaria + regras]
### Tipografia: [fontes + hierarquia]
### Estilo Fotografico: [diretrizes]
### Iconografia: [estilo e principios]
### Layout: [grid e principios de composicao]
### Proximo Passo: [design brief para execucao]
```

## Registro
- `data/registries/distinctive-assets-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand strategy document aprovado, brand archetype definido, analise semiotica concluida, distinctive assets definidos
- Gate de saida: score GREEN (>=80%) nos checklists wheeler/identity-system-audit e visual-identity-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre alina-wheeler e emily-heyward sobre direcao criativa → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (paleta nao diferenciada, tipografia generica, moodboard desalinhado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-archetype-selection, brand-semiotics-analysis, define-distinctive-assets
- Downstream: brand-guidelines-creation, sonic-branding-development, website-brand-implementation
- Cross-squad: design squad (visual direction como briefing para execucao)

### Metricas
- Numero de elementos visuais definidos (cores, tipo, foto, icones, layout)
- Alinhamento do conceito criativo com estrategia (pass/fail)
- Diferenciacao visual vs. codigos da categoria (avaliacao semiotica)
