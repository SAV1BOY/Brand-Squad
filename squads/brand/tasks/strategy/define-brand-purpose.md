# Define Brand Purpose
> Definicao do proposito da marca — a razao de existir alem do lucro.

## Objetivo
Articular um proposito de marca claro, autentico e inspirador que conecte a missao do negocio a um impacto positivo maior, servindo como norte estrategico para todas as decisoes de marca.

## Agentes
- **denise-yohn** — lidera a definicao do proposito
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Resultados de stakeholder interviews
- Missao, visao e valores existentes
- Dados de customer interviews e VoC
- Contexto de mercado e tendencias

## Passos
1. Revisar missao, visao e valores atuais
2. Analisar insights de stakeholders e clientes
3. Identificar intersecao entre competencia, paixao e necessidade do mundo
4. Redigir opcoes de proposito (3-5 versoes)
5. Testar cada opcao contra criterios de autenticidade
6. Validar alinhamento com estrategia de negocio
7. Selecionar e refinar proposito final
8. Documentar com narrativa de suporte

## Frameworks Obrigatorios
- brand-purpose-framework
- yohn-brand-as-business

## Checklists de Qualidade
- brand-purpose-quality
- yohn/brand-as-business-audit

## Output Esperado
```
## Brand Purpose
### Proposito: [declaracao em uma frase]
### Narrativa de Suporte: [contexto e fundamentacao]
### Conexao com Negocio: [como guia decisoes]
### Criterios de Autenticidade: [evidencias]
### Implicacoes para Marca: [como se manifesta]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: resultados de stakeholder interviews e customer interviews disponiveis, missao/visao/valores existentes revisados
- Gate de saida: score GREEN (>=80%) nos checklists brand-purpose-quality e yohn/brand-as-business-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre agentes sobre autenticidade do proposito → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (proposito generico, sem conexao com negocio, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: stakeholder-interviews, customer-interviews, brand-audit
- Downstream: define-brand-promise, messaging-house-development, brand-story-manifesto
- Cross-squad: people squad (brand values e cultura)

### Metricas
- Score de autenticidade do proposito (criterios de validacao)
- Alinhamento entre proposito e estrategia de negocio (pass/fail)
- Numero de versoes avaliadas antes da selecao final
