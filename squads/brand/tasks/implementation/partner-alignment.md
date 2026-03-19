# Partner Alignment
> Alinhamento de parceiros e fornecedores com as diretrizes de marca.

## Objetivo
Garantir que todos os parceiros, fornecedores e agencias que utilizam a marca estejam alinhados com as guidelines, regras de uso e padroes de qualidade — protegendo a integridade da marca em interacoes de terceiros.

## Agentes
- **brand-chief** — lidera o alinhamento
- **alina-wheeler** — define padroes de uso visual

## Inputs
- Lista de parceiros e fornecedores ativos
- Brand Guidelines atuais
- Contratos de uso de marca existentes
- Partner Brand Usage Guide

## Passos
1. Mapear todos os parceiros que usam a marca
2. Classificar por nivel de uso (alto, medio, baixo)
3. Criar pacote de guidelines para parceiros
4. Desenvolver partner brand usage guide
5. Realizar sessao de alinhamento com parceiros-chave
6. Definir processo de aprovacao de materiais
7. Estabelecer auditoria periodica de parceiros
8. Documentar regras e consequencias

## Frameworks Obrigatorios
- brand-governance-model

## Checklists de Qualidade
- co-branding-quality

## Output Esperado
```
## Partner Alignment
### Parceiros Mapeados: [lista com nivel de uso]
### Pacote de Guidelines: [materiais distribuidos]
### Sessoes Realizadas: [parceiros alinhados]
### Fluxo de Aprovacao: [processo definido]
### Auditoria: [frequencia e criterios]
### Status por Parceiro: [alinhado / pendente]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines atuais disponiveis, lista de parceiros e fornecedores mapeada
- Gate de saida: score GREEN (>=80%) no checklist co-branding-quality
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre brand-chief e alina-wheeler sobre regras de uso para parceiros → brand-chief decide
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (pacote de guidelines incompleto, fluxo de aprovacao vago, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-guidelines-creation, brand-governance-setup
- Downstream: brand-governance-enforcement, consistency-review
- Cross-squad: nenhum (task de alinhamento com parceiros externos)

### Metricas
- % de parceiros alinhados e com pacote de guidelines distribuido
- Numero de sessoes de alinhamento realizadas
- % de parceiros com fluxo de aprovacao definido
