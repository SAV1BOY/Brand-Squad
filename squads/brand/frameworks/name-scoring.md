# Name Scoring Framework
> Framework quantitativo para avaliar e comparar candidatos a nome de marca com scoring padronizado e ponderado.

---

## Definicao

O Name Scoring Framework e um sistema de avaliacao quantitativa que atribui pontuacoes objetivas a candidatos de nome de marca em multiplas dimensoes, permitindo comparacao rigorosa e decisao informada. O framework transforma julgamentos subjetivos ("eu gosto mais desse") em avaliacoes estruturadas com criterios explicitos e pesos definidos.

O sistema avalia cada nome em 8 dimensoes: Distinctiveness (unicidade), Memorability (facilidade de lembranca), Pronounceability (facilidade de pronuncia), Spellability (facilidade de grafia), Meaningfulness (significado/sugestao), Protectability (registrabilidade legal), Scalability (capacidade de crescer com a marca) e Likeability (atratividade geral). Cada dimensao recebe um peso de acordo com as prioridades do projeto.

O framework nao substitui julgamento estrategico, mas disciplina a conversacao e reduz vies pessoal na decisao.

---

## Quando Usar

- Fase final de selecao de naming (comparar 3-10 finalistas)
- Apresentacao de recomendacao de naming para stakeholders
- Resolucao de impasse quando a equipe nao converge
- Documentacao de raciocinio para escolha de nome
- Validacao pos-pesquisa de nomes com consumidores

---

## Estrutura / Modelo

```
┌──────────────────────────────────────────────────────┐
│              NAME SCORING MATRIX                     │
├──────────────┬──────┬────────┬────────┬────────┬─────┤
│ CRITERIO     │ PESO │Nome A  │Nome B  │Nome C  │Meta │
├──────────────┼──────┼────────┼────────┼────────┼─────┤
│Distinctiveness│ 15% │  /5    │  /5    │  /5    │ 4+  │
│Memorability  │ 15%  │  /5    │  /5    │  /5    │ 4+  │
│Pronounceabil.│ 15%  │  /5    │  /5    │  /5    │ 4+  │
│Spellability  │ 10%  │  /5    │  /5    │  /5    │ 3+  │
│Meaningfulness│ 15%  │  /5    │  /5    │  /5    │ 3+  │
│Protectability│ 10%  │  /5    │  /5    │  /5    │ 4+  │
│Scalability   │ 10%  │  /5    │  /5    │  /5    │ 3+  │
│Likeability   │ 10%  │  /5    │  /5    │  /5    │ 3+  │
├──────────────┼──────┼────────┼────────┼────────┼─────┤
│SCORE PONDERADO│100% │ ___    │ ___    │ ___    │3.5+ │
├──────────────┼──────┼────────┼────────┼────────┼─────┤
│VETO (algum <2)│     │ S/N   │ S/N    │ S/N    │ N   │
└──────────────┴──────┴────────┴────────┴────────┴─────┘
```

### Escala de Pontuacao

```
5 = Excepcional  │ Top 10% dos nomes que ja vimos
4 = Forte        │ Acima da media, atende bem
3 = Adequado     │ Aceitavel, sem destaque
2 = Fraco        │ Abaixo do desejavel, risco
1 = Inaceitavel  │ Eliminatorio, nao seguir
```

---

## Como Aplicar (Passo a Passo)

### Passo 1: Calibrar Pesos
Ajuste os pesos das 8 dimensoes conforme prioridades do projeto. Marca internacional? Aumente Pronounceability. Mercado saturado? Aumente Distinctiveness.

### Passo 2: Definir o Painel de Avaliadores
Reuna 3-5 avaliadores com perfis diversos: estrategista, criativo, linguista, representante do target, stakeholder de negocio. Cada um pontua independentemente.

### Passo 3: Pontuar Independentemente
Cada avaliador pontua cada nome em cada dimensao ANTES de discutir com os demais. Isso evita groupthink.

### Passo 4: Compilar e Analisar
Calcule media ponderada por nome. Identifique: (a) vencedor geral, (b) nomes com veto (<2 em qualquer dimensao critica), (c) divergencias grandes entre avaliadores.

### Passo 5: Discutir Divergencias
Para dimensoes onde avaliadores divergem mais de 2 pontos, abra discussao para entender perspectivas e recalibrar se necessario.

### Passo 6: Decidir com Dados + Julgamento
O score informa mas nao decide sozinho. Use como base para discussao final, complementando com gut feeling estrategico e pesquisa com consumidores.

---

## Exemplos de Aplicacao

### Exemplo 1: Startup de health tech
- **Candidatos:** Vitaly (4.2), MedFlow (3.8), Cureva (4.0), HealthBridge (3.1)
- **Veto:** HealthBridge vetado por Distinctiveness = 1 (generico demais)
- **Vencedor:** Vitaly — forte em todas as dimensoes, especialmente memorabilidade e sonoridade

### Exemplo 2: Marca de cosmeticos
- **Candidatos:** Lumière (3.9), Dermasense (3.4), Veluria (4.3)
- **Divergencia:** Lumière — equipe criativa deu 5 em likeability; equipe legal deu 2 em protectability (muito proximo de marcas existentes)
- **Decisao:** Veluria avancou por equilibrio entre todas as dimensoes

### Exemplo 3: Rebranding corporativo
- **Pesos ajustados:** Scalability (20%), Protectability (15%), Distinctiveness (20%) — priorizando longevidade
- **Candidatos avaliados com novos pesos revelaram vencedor diferente do "favorito" da diretoria**

---

## Erros Comuns

1. **Avaliar em grupo desde o inicio:** Groupthink domina. Sempre pontuar individualmente ANTES de discutir.
2. **Pesos iguais para tudo:** Nem toda dimensao importa igualmente para todo projeto. Calibre pesos antes de pontuar.
3. **Ignorar vetos:** Um score 1 em protectability elimina o nome independente do score geral. Vetos sao absolutos.
4. **Confiar so no score:** O framework e ferramenta de pensamento, nao oraculo. Use-o para estruturar, nao substituir julgamento.
5. **Nao incluir o target:** Avaliacao apenas interna ignora percepcao real. Inclua dados de pesquisa com consumidores quando possivel.

---

## Integracao com Outros Frameworks

| Framework | Relacao | Como Conectam |
|-----------|---------|---------------|
| SMILE & SCRATCH | Complementar | SMILE/SCRATCH e qualitativo-estrategico; Name Scoring e quantitativo-comparativo |
| Linguistic Stress Test | Input | Resultados do Stress Test alimentam dimensoes de Pronounceability e Spellability |
| Shortlist Methodology | Sequencial | Shortlist filtra candidatos; Scoring compara os finalistas |
| Name Taxonomy | Informativo | Nomes de diferentes tipos taxonomicos devem ser pontuados separadamente |
| Morpheme Builder | Sequencial | Builder gera candidatos; Scoring avalia os melhores |

---

## Referencias

- Kohli, C. & LaBahn, D. (1997). "Creating Effective Brand Names." *Journal of Advertising Research*, 37(1), 67-75.
- Robertson, K. (1989). "Strategically Desirable Brand Name Characteristics." *Journal of Consumer Marketing*, 6(4), 61-71.
