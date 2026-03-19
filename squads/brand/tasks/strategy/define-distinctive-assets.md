# Define Distinctive Assets
> Definicao e priorizacao dos distinctive assets da marca.

## Objetivo
Identificar, criar e priorizar os distinctive assets da marca — elementos visuais, sonoros e verbais que geram reconhecimento instantaneo — maximizando mental availability conforme os principios de Byron Sharp.

## Agentes
- **byron-sharp** — lidera a definicao de distinctive assets
- **alina-wheeler** — valida viabilidade de implementacao visual
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand identity atual (logo, cores, tipografia)
- Dados de reconhecimento de marca
- Distinctive assets dos concorrentes
- Brand Guidelines existentes

## Passos
1. Inventariar assets atuais da marca
2. Avaliar nivel de reconhecimento de cada asset
3. Classificar por tipo (cor, forma, som, personagem, etc.)
4. Identificar gaps — assets que faltam
5. Priorizar assets para investimento
6. Definir regras de uso consistente para cada asset
7. Criar metricas de reconhecimento para tracking
8. Documentar no distinctive assets registry

## Frameworks Obrigatorios
- sharp-mental-availability
- distinctive-assets-system

## Checklists de Qualidade
- sharp/distinctive-assets-audit
- distinctive-assets-quality

## Output Esperado
```
## Distinctive Assets Registry
### Assets Existentes:
  - [Asset]: [tipo, reconhecimento atual, prioridade]
### Assets a Criar: [lista com justificativa]
### Regras de Uso: [por asset]
### Metricas de Tracking: [como medir reconhecimento]
### Plano de Investimento: [prioridades]
```

## Registro
- `data/registries/distinctive-assets-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand identity atual inventariada, dados de reconhecimento disponiveis, distinctive assets dos concorrentes mapeados
- Gate de saida: score GREEN (>=80%) nos checklists sharp/distinctive-assets-audit e distinctive-assets-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre byron-sharp e alina-wheeler sobre viabilidade de assets → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (assets sem metrica de reconhecimento, regras de uso vagas, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-audit, category-entry-points-research, visual-identity-direction
- Downstream: maintain-distinctive-assets-registry, brand-guidelines-creation, sonic-branding-development
- Cross-squad: marketing squad (distinctive assets para campanhas), design squad (assets visuais para execucao)

### Metricas
- Numero de distinctive assets inventariados e classificados
- % de assets com metrica de reconhecimento definida
- Numero de gaps de assets identificados e priorizados
