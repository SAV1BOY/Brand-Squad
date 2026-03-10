# Brand Tracking Model
> Sistema de monitoramento continuo que mensura saude, percepcao e desempenho da marca ao longo do tempo.

---

## Definicao

Brand Tracking e a pratica de monitorar metricas-chave de marca de forma continua ou periodica para avaliar a saude da marca, detectar mudancas na percepcao do consumidor e medir o impacto de investimentos em branding. Diferente de pesquisas pontuais, o tracking fornece uma visao longitudinal que permite identificar tendencias e agir proativamente.

Um modelo robusto de tracking combina metricas de funil de marca (awareness, consideracao, preferencia, uso) com metricas de equity (associacoes, qualidade percebida, lealdade) e metricas comportamentais (share of search, share of voice, NPS). A integracao dessas camadas oferece uma visao completa de como a marca esta performando em relacao a concorrencia e a si mesma no tempo.

## Quando Usar

- Para monitorar o impacto de campanhas e investimentos em marca
- Ao avaliar a saude competitiva da marca em relacao aos concorrentes
- Para justificar investimentos em branding com dados longitudinais
- Quando a marca passa por mudancas estrategicas (reposicionamento, expansao, crise)

## Estrutura / Modelo

```
┌─────────────────────────────────────────────┐
│         DASHBOARD DE BRAND TRACKING         │
│                                             │
│  FUNIL DE MARCA          EQUITY             │
│  ┌────────────────┐      ┌────────────────┐ │
│  │ Awareness  85% │      │ Qualidade  4.2 │ │
│  │ Considerac 62% │      │ Valor perc 3.8 │ │
│  │ Preferenc  34% │      │ Diferenc.  3.5 │ │
│  │ Uso        28% │      │ Confianca  4.0 │ │
│  │ Lealdade   18% │      │ Relevancia 3.9 │ │
│  └────────────────┘      └────────────────┘ │
│                                             │
│  COMPORTAMENTAL          EMOCIONAL          │
│  ┌────────────────┐      ┌────────────────┐ │
│  │ Share Search 8%│      │ NPS       +42  │ │
│  │ Share Voice 12%│      │ Brand Love 3.7 │ │
│  │ Mencoes/sem 2k │      │ Sentimento 78% │ │
│  └────────────────┘      └────────────────┘ │
│                                             │
│  Periodicidade: Mensal (digital) / Trimestral│
│  (pesquisa) / Anual (equity profundo)        │
└─────────────────────────────────────────────┘
```

## Como Aplicar (Passo a Passo)

1. **Selecione metricas por camada**: Escolha 3-5 metricas por camada (funil, equity, comportamental, emocional) que sejam relevantes para os objetivos da marca.
2. **Defina baseline e benchmarks**: Mensure o ponto de partida e estabeleca comparativos (concorrencia, periodo anterior, meta).
3. **Implemente coleta continua**: Combine pesquisas de tracking (mensal ou trimestral), dados digitais (search, social) e dados de CRM.
4. **Crie dashboards acionaveis**: Visualize tendencias, nao apenas snapshots. Sinalize alertas quando metricas cruzam limiares criticos.
5. **Vincule a decisoes**: Cada ciclo de tracking deve gerar 2-3 acoes concretas. Se o tracking nao muda decisoes, ele e custo, nao investimento.

## Exemplos de Aplicacao

**Ambev**: Opera tracking continuo de marcas como Brahma, Skol e Budweiser no Brasil. Mensura awareness espontaneo, top-of-mind, associacoes de marca e NPS por regiao. Os dados alimentam decisoes de midia, patrocinio e portfolio trimestralmente.

**iFood**: Combina tracking tradicional (pesquisa trimestral) com dados proprietarios (share of search, frequencia de uso, NPS transacional). Detectou queda em percepcao de "variedade" e lancou campanha especifica para restaurantes premium como resposta direta ao tracking.

## Erros Comuns

- **Medir sem agir**: Tracking que vira relatorio bonito mas nao muda decisoes e desperdicio de recurso.
- **Frequencia inadequada**: Tracking anual em mercados dinamicos perde mudancas criticas. Tracking semanal em categorias estaveis gera ruido.
- **Ignorar concorrencia**: Metricas absolutas enganam. Um awareness de 80% parece otimo ate descobrir que o concorrente esta em 90%.

## Integracao com Outros Frameworks

| Framework | Conexao |
|---|---|
| Keller CBBE Pyramid | As metricas de tracking podem ser organizadas nos quatro niveis da piramide |
| Aaker Brand Equity Model | Dimensoes de equity de Aaker (lealdade, awareness, qualidade percebida) mapeiam diretamente em metricas de tracking |
| Measurement Layer | O tracking e a ferramenta central da camada de mensuracao do brand system |

## Referencias

- Romaniuk, J. & Sharp, B. (2022). *How Brands Grow Part 2*. Oxford University Press. Cap. 9.
- Keller, K. L. (2013). *Strategic Brand Management*. Pearson. Cap. 10 — Measuring Brand Performance.
