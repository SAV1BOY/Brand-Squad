# Website Brand Implementation
> Implementacao da nova identidade de marca no site/website.

## Objetivo
Atualizar o website com a nova identidade visual e verbal da marca — logo, cores, tipografia, tom de voz, messaging e imagens — garantindo que o principal touchpoint digital reflita a marca atualizada.

## Agentes
- **alina-wheeler** — lidera a implementacao visual
- **donald-miller** — valida messaging e copy do site
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Guidelines atuais
- Website atual (auditoria de paginas)
- Copy deck atualizado
- Assets visuais prontos
- Messaging house e StoryBrand script

## Passos
1. Auditar todas as paginas do site atual
2. Mapear atualizacoes necessarias por pagina
3. Implementar nova identidade visual (logo, cores, fontes)
4. Atualizar copy de todas as paginas (messaging alinhada)
5. Substituir imagens e assets visuais
6. Atualizar meta descriptions e SEO elements
7. Testar consistencia em desktop e mobile
8. Publicar e monitorar metricas

## Frameworks Obrigatorios
- wheeler-brand-identity-process
- miller-storybrand-sb7

## Checklists de Qualidade
- wheeler/identity-system-audit
- miller/messaging-clarity-audit
- Consistencia mobile/desktop verificada

## Output Esperado
```
## Website Brand Implementation
### Paginas Atualizadas: [lista com status]
### Identidade Visual: [logo, cores, fontes — implementados]
### Copy: [paginas reescritas e aprovadas]
### SEO: [meta descriptions atualizadas]
### Testes: [desktop + mobile validados]
### Metricas Pre/Pos: [comparativo]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines atuais disponiveis, copy deck atualizado, assets visuais prontos, messaging house e StoryBrand script concluidos
- Gate de saida: score GREEN (>=80%) nos checklists wheeler/identity-system-audit e miller/messaging-clarity-audit, consistencia mobile/desktop verificada
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre alina-wheeler e donald-miller sobre implementacao visual vs. copy → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (paginas inconsistentes, copy desalinhado, mobile quebrado, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-guidelines-creation, storybrand-script, visual-identity-direction
- Downstream: consistency-review, brand-tracking-analysis
- Cross-squad: product squad (implementacao tecnica do site), design squad (execucao visual)

### Metricas
- % de paginas atualizadas com nova identidade
- Score de consistencia visual e verbal entre paginas
- Performance mobile/desktop pos-implementacao
