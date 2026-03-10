# Gerador de Candidatos de Nome

> Processo estruturado para gerar lista ampla de candidatos de nome para marca ou produto.

## Objetivo

Gerar 50-100 candidatos de nome que serao filtrados e avaliados pelo naming-scoring-matrix.

## Inputs

- Brief de naming (categoria, publico, posicionamento, tom)
- Palavras-chave e conceitos associados
- Nomes de concorrentes (para evitar similaridade)
- Mercados-alvo (idiomas a considerar)
- Restricoes (dominios obrigatorios, tamanho maximo)

## Processo

### 1. Brainstorm por Categoria (10 nomes cada)
- **Descritivos**: O que faz / o que e
- **Metaforicos**: Analogias e associacoes indiretas
- **Inventados**: Palavras novas criadas
- **Compostos**: Combinacao de duas palavras existentes
- **Acronimos**: Letras iniciais de frase significativa

### 2. Brainstorm por Tecnica (10 nomes cada)
- **Raiz latina/grega**: Radices classicas combinadas
- **Onomatopeia**: Sons que evocam o conceito
- **Truncamento**: Palavras existentes cortadas/modificadas
- **Portmanteau**: Fusao de duas palavras
- **Foreign words**: Palavras de outros idiomas que soam bem

### 3. Filtragem Inicial
Remover candidatos que:
- Sao impossiveis de pronunciar
- Tem conotacao negativa obvia
- Sao identicos a marcas existentes na categoria
- Tem mais de 4 silabas

### 4. Verificacao Rapida
Para os 20-30 sobreviventes:
- Dominio .com ou .com.br disponivel?
- Handles de social livres?
- Busca rapida no INPI por conflitos

## Output

Lista ordenada de 15-20 candidatos viáveis com: nome, tipo, significado pretendido, dominios disponiveis.

## Exemplo de Uso

```
> naming-candidate-generator --brief "fintech de investimentos, jovens, acessivel"
> Top 5: Investi, Planto, Grana, NovaMoeda, Quorum
```
