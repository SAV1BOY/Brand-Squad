# Employee Brand Perception
> Pesquisa de percepcao interna da marca entre colaboradores.

## Objetivo
Medir como os colaboradores percebem, vivenciam e representam a marca — identificando nivel de alinhamento entre brand promise externa e experiencia interna, e oportunidades de fortalecimento da cultura de marca.

## Agentes
- **denise-yohn** — lidera a pesquisa de percepcao interna
- **kevin-keller** — complementa com metricas de brand knowledge
- **brand-chief** — orquestracao e validacao

## Inputs
- Brand Strategy Document e brand promise
- Valores e cultura organizacional documentados
- Dados de clima organizacional (se disponiveis)
- Acesso a colaboradores para pesquisa

## Passos
1. Definir objetivos e dimensoes a medir
2. Desenhar instrumento de pesquisa (survey + entrevistas)
3. Aplicar pesquisa com amostra representativa de colaboradores
4. Medir conhecimento da marca (brand knowledge interno)
5. Avaliar alinhamento entre promessa e experiencia
6. Identificar embaixadores naturais da marca
7. Mapear gaps entre cultura desejada e vivenciada
8. Documentar findings e recomendacoes

## Frameworks Obrigatorios
- yohn-brand-as-business
- yohn-fusion

## Checklists de Qualidade
- yohn/brand-as-business-audit
- Amostra representativa de departamentos
- Anonimato garantido

## Output Esperado
```
## Relatorio de Percepcao Interna
### Metodologia: [survey/entrevistas, amostra]
### Conhecimento da Marca: [% que conhece proposito, valores]
### Alinhamento Promessa-Experiencia: [score]
### Embaixadores Identificados: [perfil e quantidade]
### Gaps Cultura-Marca: [lista priorizada]
### Recomendacoes: [acoes de alinhamento interno]
```

## Registro
- `data/research/survey-results/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand strategy document e brand promise disponiveis, acesso a colaboradores garantido
- Gate de saida: score GREEN (>=80%) no checklist yohn/brand-as-business-audit, amostra representativa de departamentos confirmada
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre denise-yohn e kevin-keller sobre metricas de brand knowledge → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (amostra nao representativa, gaps nao mapeados, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-audit, define-brand-purpose
- Downstream: internal-training, brand-ambassador-program
- Cross-squad: people squad (employer brand e alinhamento cultural)

### Metricas
- % de colaboradores que conhecem proposito e valores da marca
- Score de alinhamento promessa-experiencia interna
- Numero de embaixadores naturais identificados
