# Tagline Development
> Criacao de tagline memoravel e estrategicamente alinhada a marca.

## Objetivo
Desenvolver uma tagline que sintetize a essencia da marca em poucas palavras — memoravel, diferenciadora e alinhada ao posicionamento — servindo como elemento distintivo verbal.

## Agentes
- **donald-miller** — lidera com foco em clareza e simplicidade
- **emily-heyward** — valida obviedade e impacto
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Posicionamento e brand promise definidos
- Messaging house (se existir)
- Brand voice e personalidade
- Taglines dos concorrentes

## Passos
1. Revisar posicionamento, promessa e pilares de mensagem
2. Definir tipo de tagline (descritiva, provocativa, imperativa, etc.)
3. Gerar 20-30 opcoes de tagline
4. Filtrar por clareza, memorabilidade e diferenciacao
5. Selecionar top 5 para avaliacao detalhada
6. Testar compreensao e recall com publico
7. Validar alinhamento com brand voice
8. Selecionar e documentar tagline final

## Frameworks Obrigatorios
- tagline-architecture
- verbal-identity-system

## Checklists de Qualidade
- tagline-quality

## Output Esperado
```
## Tagline
### Tagline Selecionada: [frase]
### Tipo: [descritiva/provocativa/imperativa]
### Alinhamento com Posicionamento: [como conecta]
### Teste de Clareza: [resultado]
### Teste de Recall: [resultado]
### Versoes Alternativas: [para contextos especificos]
### Regras de Uso: [quando e como usar]
```

## Registro
- `data/registries/brand-claims-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: posicionamento e brand promise definidos, brand voice e personalidade disponveis
- Gate de saida: score GREEN (>=80%) no checklist tagline-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre donald-miller e emily-heyward sobre abordagem criativa → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (tagline generica, sem recall, desalinhada com posicionamento, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: positioning-development, define-brand-promise, messaging-house-development
- Downstream: verbal-identity-development, brand-guidelines-creation, campaign-activation-brief
- Cross-squad: copy squad (tagline como referencia verbal), marketing squad (tagline para campanhas)

### Metricas
- Numero de opcoes geradas e avaliadas
- Score de clareza e recall da tagline selecionada
- Alinhamento com posicionamento (pass/fail)
