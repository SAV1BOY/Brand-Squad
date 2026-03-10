# Linter de Brand Guidelines

> Verificacao automatizada de consistencia entre materiais de comunicacao e guidelines de marca.

## Objetivo

Analisar materiais de comunicacao e identificar desvios das brand guidelines documentadas, gerando relatorio de conformidade.

## Inputs

- Brand guidelines da marca (visual + verbal)
- Materiais a serem avaliados (URLs, imagens, textos)
- Nivel de rigor (strict / standard / relaxed)

## Processo

### 1. Verificacao Visual
- [ ] Cores utilizadas estao na paleta aprovada?
- [ ] Logo esta na versao correta para o contexto?
- [ ] Area de protecao do logo esta respeitada?
- [ ] Tipografia e a aprovada (familia, peso, tamanho)?
- [ ] Imagens seguem o estilo definido?
- [ ] Proporcoes e grid estao corretos?

### 2. Verificacao Verbal
- [ ] Tom de voz esta alinhado com o perfil definido?
- [ ] Vocabulario usa palavras aprovadas e evita proibidas?
- [ ] Nivel de formalidade esta no range aceitavel?
- [ ] Claims feitos tem suporte documentado?
- [ ] Mensagem central esta alinhada com posicionamento?

### 3. Verificacao de Consistencia
- [ ] Material e consistente com outros materiais recentes?
- [ ] Canal de publicacao esta adequado ao tom?
- [ ] CTA segue padrao definido?

### 4. Classificacao de Issues

| Severidade | Definicao | Acao |
|-----------|-----------|------|
| Critica | Violacao que pode causar dano legal ou reputacional | Bloquear publicacao |
| Alta | Desvio significativo das guidelines | Corrigir antes de publicar |
| Media | Desvio menor mas visivel | Corrigir no proximo ciclo |
| Baixa | Sugestao de melhoria | Nice to have |

## Output

Relatorio com: score de conformidade (%), lista de issues por severidade, recomendacoes de correcao.

## Exemplo de Uso

```
> guidelines-linter --url "website.com/landing" --guidelines "brand-guidelines.md"
> Score: 82% conformidade
> Issues: 1 alta (cor secundaria errada), 3 medias (tom inconsistente)
```
