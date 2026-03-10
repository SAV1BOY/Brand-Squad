# Scanner de Consistencia de Marca

> Analise sistematica de consistencia de marca em todos os canais e touchpoints.

## Objetivo

Identificar inconsistencias de marca entre canais, materiais e experiencias, gerando mapa de gaps e prioridades de correcao.

## Inputs

- Lista de canais e touchpoints ativos
- Brand guidelines da marca
- Acesso aos canais para avaliacao
- Equipe/responsavel por cada canal

## Processo

### 1. Coleta de Amostras

| Canal | Amostras | Coletado |
|-------|----------|----------|
| Website (todas as paginas) | Screenshots + copy | [ ] |
| Email (5 ultimos de cada tipo) | Full email | [ ] |
| Instagram (20 ultimos posts) | Visual + caption | [ ] |
| LinkedIn (10 ultimos posts) | Visual + copy | [ ] |
| Atendimento (10 interacoes) | Transcricoes | [ ] |
| Material impresso | Fotos/scans | [ ] |
| Apresentacoes | Decks | [ ] |

### 2. Avaliacao por Dimensao

Para cada amostra, avaliar (1-10):
- **Identidade Visual**: Logo, cor, tipografia, imagens
- **Tom de Voz**: Formalidade, emocao, personalidade
- **Mensagem**: Alinhamento com posicionamento e proposta de valor
- **Experiência**: Qualidade e coerencia da interacao

### 3. Mapa de Consistencia

| Canal | Visual | Voz | Mensagem | Experiencia | Score |
|-------|--------|-----|----------|-------------|-------|
| Website | | | | | |
| Email | | | | | |
| Instagram | | | | | |
| Atendimento | | | | | |

### 4. Gap Analysis

Identificar:
- Canais com maior desvio do padrao
- Dimensoes mais inconsistentes
- Causa raiz (falta de guidelines? falta de treinamento? agencia desalinhada?)

## Output

Relatorio com: mapa de consistencia, ranking de gaps, causa raiz por gap, plano de acao priorizado.

## Exemplo de Uso

```
> brand-consistency-scanner --brand "MarcaX" --channels "website,email,instagram,cs"
> Consistencia geral: 72%
> Gap critico: Atendimento ao cliente (54%) — tom informal demais vs. guidelines
```
