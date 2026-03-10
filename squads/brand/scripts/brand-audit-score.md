# Brand Audit Score

> Avaliacao estruturada e quantificavel da saude geral de uma marca.

## Objetivo

Produzir um score numerico de 0-100 que avalia a saude da marca em multiplas dimensoes, identificando pontos fortes e gaps criticos para acao.

## Inputs

- Nome da marca e categoria
- Website, redes sociais e materiais de comunicacao
- Brand guidelines (se existentes)
- Dados de pesquisa de mercado (se disponiveis)
- Informacoes sobre concorrentes principais

## Processo

### 1. Avaliacao por Dimensao (cada uma de 0-10)

**Identidade (Aaker/Kapferer)**
- Clareza de proposito e valores
- Consistencia de identidade visual
- Personalidade de marca definida e coerente
- Prisma de identidade completo

**Posicionamento (Ries/Trout)**
- Diferenciacao clara vs. concorrentes
- Onliness statement articulavel
- Categoria bem definida
- Proposta de valor unica

**Saliencia (Sharp)**
- Distinctive assets fortes e reconheciveis
- Category entry points mapeados
- Disponibilidade mental e fisica
- Penetracao de mercado

**Voz (Wheeler)**
- Tom de voz definido e documentado
- Consistencia entre canais
- Diferenciacao verbal
- Adequação ao publico

**Experiencia (Keller)**
- Consistencia de touchpoints
- Momentos de peak-end projetados
- Alinhamento cultura-marca
- NPS e satisfacao

### 2. Calculo do Score

Score = Media ponderada das 5 dimensoes (cada uma peso 20%)

### 3. Classificacao

- 80-100: Marca Forte — manter e otimizar
- 60-79: Marca Saudavel — gaps especificos a corrigir
- 40-59: Marca em Risco — acao urgente necessaria
- 0-39: Marca Critica — revisao estrategica completa

## Output

Relatorio com: score total, score por dimensao, top 3 forcas, top 3 gaps, recomendacoes priorizadas com timeline.

## Exemplo de Uso

```
> brand-audit-score --brand "MarcaX" --category "SaaS B2B"
> Resultado: 67/100 (Saudavel)
> Gap critico: Saliencia (4/10) — distinctive assets fracos
> Recomendacao #1: Investir em cor e audio logo proprietarios
```
