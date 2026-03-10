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
