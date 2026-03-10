# Matriz de Scoring de Naming

> Avaliacao objetiva e comparativa de candidatos de nome.

## Objetivo

Avaliar e ranquear candidatos de nome usando criterios ponderados para decisao informada.

## Inputs

- Lista de 10-20 candidatos (output do naming-candidate-generator)
- Brief de naming com criterios prioritarios
- Feedback de stakeholders

## Processo

### Criterios de Avaliacao

| Criterio | Peso | Definicao |
|----------|------|-----------|
| Pronunciabilidade | 15% | Facil de falar em PT-BR (e EN se global) |
| Memorabilidade | 15% | Gruda na mente apos 1 exposicao |
| Significado | 15% | Evoca associacoes positivas e relevantes |
| Diferenciacao | 15% | Unico na categoria e no mercado |
| Disponibilidade | 15% | Dominio, handles e registro de marca |
| Escalabilidade | 10% | Funciona em diferentes mercados e contextos |
| Visual Potential | 10% | Funciona bem em logo e materiais |
| Sound | 5% | Som agradavel quando falado em voz alta |

### Escala

- 1-2: Fraco — problema serio nesse criterio
- 3-4: Abaixo da media — funciona mas nao impressiona
- 5-6: Adequado — atende requisitos basicos
- 7-8: Forte — destaque nesse criterio
- 9-10: Excepcional — referencia

### Matriz de Comparacao

| Nome | Pronunc. | Memor. | Signif. | Difer. | Disp. | Escala. | Visual | Som | TOTAL |
|------|---------|--------|---------|--------|-------|---------|--------|-----|-------|
| [A] | | | | | | | | | |
| [B] | | | | | | | | | |

## Output

Ranking de candidatos com score total, pontos fortes e fracos de cada, e recomendacao de top 3 para avaliacao final.

## Exemplo de Uso

```
> naming-scoring-matrix --candidates "Investi,Planto,Grana"
> #1 Planto (78/100) — forte em memorabilidade e significado
> #2 Investi (72/100) — forte em pronunciabilidade
> #3 Grana (65/100) — forte em sound, fraco em diferenciacao
```
