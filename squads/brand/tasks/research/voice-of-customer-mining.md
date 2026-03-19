# Voice of Customer Mining
> Mineracao de dados de voz do cliente em reviews, redes sociais e canais de suporte.

## Objetivo
Extrair padroes de linguagem, sentimentos e percepcoes do cliente a partir de fontes nao-estruturadas — reviews, redes sociais, tickets de suporte e foruns — para alimentar messaging e posicionamento.

## Agentes
- **denise-yohn** — lidera a analise de percepcao e cultura
- **donald-miller** — identifica linguagem para messaging
- **brand-chief** — orquestracao e validacao

## Inputs
- Acesso a reviews (Google, Reclame Aqui, App Store, etc.)
- Acesso a redes sociais da marca
- Dados de tickets de suporte
- Foruns e comunidades relevantes

## Passos
1. Definir fontes de dados e periodo de analise
2. Coletar reviews e mencoes relevantes
3. Categorizar por tema (produto, servico, marca, preco, etc.)
4. Identificar sentimento predominante por tema
5. Extrair linguagem real do cliente (expressoes, metaforas)
6. Mapear dores, desejos e expectativas nao atendidas
7. Identificar brand personality percebida vs. desejada
8. Consolidar em repositorio de VoC

## Frameworks Obrigatorios
- discovery-and-research
- brand-personality-scale

## Checklists de Qualidade
- Minimo 3 fontes de dados analisadas
- Categorizacao por tema consistente
- Linguagem do cliente documentada literalmente

## Output Esperado
```
## Relatorio VoC
### Fontes Analisadas: [lista com volume]
### Temas Predominantes: [ranking]
### Sentimento por Tema: [positivo/negativo/neutro]
### Linguagem Real: [expressoes extraidas]
### Gaps de Percepcao: [marca desejada vs. percebida]
### Recomendacoes: [insights para messaging]
```

## Registro
- `data/research/voc-dumps/`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: acesso a pelo menos 3 fontes de dados (reviews, social, suporte) confirmado
- Gate de saida: categorizacao por tema consistente, linguagem do cliente documentada literalmente, gaps de percepcao mapeados
- Score minimo: GREEN (>=80%) na validacao de completude e qualidade do repositorio VoC

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre denise-yohn e donald-miller sobre interpretacao de linguagem → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (fontes insuficientes, categorizacao inconsistente, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: customer-interviews, acesso a fontes de dados
- Downstream: messaging-house-development, storybrand-script, brand-voice-development
- Cross-squad: nenhum (task interna de pesquisa)

### Metricas
- Numero de fontes de dados analisadas
- Volume de mencoes classificadas por sentimento
- Numero de expressoes reais extraidas para uso em messaging
