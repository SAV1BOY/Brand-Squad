# Scraper de Sentimento Social

> Coleta e analise de sentimento sobre a marca em redes sociais e plataformas online.

## Objetivo

Monitorar e analisar o que consumidores dizem sobre a marca em canais sociais, identificando tendencias de sentimento e temas emergentes.

## Inputs

- Nome da marca e variacoes (abreviacoes, erros comuns de grafia)
- Plataformas a monitorar
- Palavras-chave associadas
- Periodo de analise
- Benchmark de sentimento anterior

## Processo

### 1. Coleta

**Plataformas**
| Plataforma | Tipo de Mencao | Ferramenta |
|-----------|---------------|-----------|
| Twitter/X | Mencoes, hashtags, threads | API / Brandwatch |
| Instagram | Comentarios, stories, tags | API / Sprout |
| LinkedIn | Posts, comentarios, artigos | Manual / Hootsuite |
| Reddit | Posts, comentarios em subreddits | API / Reddit Search |
| Google Reviews | Avaliacoes e resenhas | API |
| Reclame Aqui | Reclamacoes e resolucoes | Manual / API |

### 2. Classificacao

| Categoria | Definicao | Acao |
|-----------|-----------|------|
| Positivo | Elogio, recomendacao, defesa | Amplificar e agradecer |
| Neutro | Mencao informativa sem emocao | Monitorar |
| Negativo | Critica, reclamacao, frustração | Responder e resolver |
| Crise | Volume alto de negativo concentrado | Ativar protocolo de crise |

### 3. Analise de Temas

Agrupar mencoes por tema para identificar padroes:
- Produto/servico (qualidade, features, bugs)
- Atendimento (positivo, negativo)
- Preco/valor
- Marca/comunicacao
- Concorrentes (comparacoes)

## Output

Dashboard com: sentimento geral (%), tendencia, temas mais frequentes, alertas de crise, mencoes destacadas.

## Exemplo de Uso

```
> social-sentiment-scraper --brand "MarcaX" --period "30d"
> Sentimento: 72% positivo, 18% neutro, 10% negativo
> Tendencia: +5% vs. periodo anterior
> Tema emergente: "atendimento lento" cresceu 200% — investigar
```
