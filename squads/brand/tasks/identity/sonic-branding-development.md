# Sonic Branding Development
> Desenvolvimento da identidade sonora da marca.

## Objetivo
Criar os elementos sonoros da marca — audio logo, soundscape, voz institucional e diretrizes sonoras — adicionando uma dimensao sensorial que reforce reconhecimento e memorabilidade.

## Agentes
- **byron-sharp** — valida potencial como distinctive asset
- **alina-wheeler** — garante coerencia com identidade visual
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand personality e archetype
- Visual identity direction
- Distinctive assets definidos
- Referencias sonoras da categoria
- Budget disponivel para producao

## Passos
1. Definir territorios sonoros alinhados a personalidade
2. Pesquisar sonic branding dos concorrentes
3. Criar briefing para audio logo (mnemonic)
4. Desenvolver soundscape da marca (ambiencia sonora)
5. Definir diretrizes para voz institucional
6. Definir musica de holding e jingles (se aplicavel)
7. Testar reconhecimento e associacao com a marca
8. Documentar sonic branding guidelines

## Frameworks Obrigatorios
- distinctive-assets-system
- brand-experience-map

## Checklists de Qualidade
- sharp/distinctive-assets-audit
- Coerencia com personalidade da marca validada
- Teste de reconhecimento realizado

## Output Esperado
```
## Sonic Branding Guide
### Audio Logo: [descricao e arquivo]
### Soundscape: [ambiencia e aplicacoes]
### Voz Institucional: [caracteristicas]
### Musica de Holding: [diretrizes]
### Aplicacoes: [onde e como usar cada elemento]
### Teste de Reconhecimento: [resultados]
### Regras de Uso: [do's & don'ts sonoros]
```

## Registro
- `data/registries/distinctive-assets-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand personality e archetype definidos, visual identity direction concluida, distinctive assets definidos
- Gate de saida: score GREEN (>=80%) no checklist distinctive-assets-quality, teste de reconhecimento realizado
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre byron-sharp e alina-wheeler sobre coerencia sonora-visual → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (audio logo sem reconhecimento, soundscape desalinhado com personalidade, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-archetype-selection, visual-identity-direction, define-distinctive-assets
- Downstream: brand-guidelines-creation, maintain-distinctive-assets-registry
- Cross-squad: marketing squad (elementos sonoros para campanhas)

### Metricas
- Numero de elementos sonoros criados (audio logo, soundscape, voz)
- Score de reconhecimento no teste de associacao com a marca
- Coerencia com personalidade da marca (pass/fail)
