# Componentes de UI da Marca
> Template para documentar a aplicacao da identidade visual em componentes de interface digital.

## Instrucoes de Uso
Preencha apos a definicao de cores, tipografia e iconografia. Este documento traduz a identidade
visual da marca em componentes de interface reutilizaveis. Deve ser usado em conjunto com o
design system. Envolva o time de produto e desenvolvimento.

## Template

### 1. Principios de UI
**Filosofia de design:** [PREENCHER]
**Prioridade visual:** [PREENCHER] (conteudo / navegacao / acao)
**Densidade de informacao:** [PREENCHER] (alta / media / baixa)
**Abordagem mobile:** [PREENCHER] (mobile-first / responsive / adaptive)

### 2. Grid e Espacamento
**Grid system:** [PREENCHER] (colunas, gutter, margem)
**Unidade base de espacamento:** [PREENCHER] (ex: 8px)
**Escala de espacamento:** [PREENCHER] (ex: 4, 8, 12, 16, 24, 32, 48, 64)
**Breakpoints:** [PREENCHER]

### 3. Botoes
| Variante | Fundo | Texto | Borda | Border-radius | Padding |
|----------|-------|-------|-------|---------------|---------|
| Primario | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| Secundario | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| Terciario / Ghost | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| Destrutivo | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |

**Estados:** Default / Hover / Active / Focus / Disabled
**Tamanhos:** Small / Medium / Large
**Com icone:** [PREENCHER] (esquerda / direita / ambos)

### 4. Campos de Formulario
**Estilo:** [PREENCHER] (outlined / filled / underline)
**Border-radius:** [PREENCHER]
**Altura padrao:** [PREENCHER]
**Label:** [PREENCHER] (floating / acima / placeholder-only)
**Estados:** [PREENCHER] (default / focus / error / success / disabled)
**Mensagens de erro:** [PREENCHER] (posicao, cor, tipografia)

### 5. Cards
**Border-radius:** [PREENCHER]
**Sombra:** [PREENCHER]
**Padding interno:** [PREENCHER]
**Hover effect:** [PREENCHER]
**Variacoes:** [PREENCHER]

### 6. Navegacao
**Header / Navbar:** [PREENCHER]
**Menu mobile:** [PREENCHER] (hamburger / tab bar / drawer)
**Breadcrumbs:** [PREENCHER]
**Tabs:** [PREENCHER]
**Sidebar:** [PREENCHER]

### 7. Feedback e Status
**Toasts / Snackbars:** [PREENCHER]
**Modais:** [PREENCHER]
**Loading states:** [PREENCHER]
**Empty states:** [PREENCHER]
**Badges / Tags:** [PREENCHER]

### 8. Tokens de Design
| Token | Valor | Uso |
|-------|-------|-----|
| --color-primary | [PREENCHER] | [PREENCHER] |
| --color-secondary | [PREENCHER] | [PREENCHER] |
| --radius-sm | [PREENCHER] | [PREENCHER] |
| --radius-md | [PREENCHER] | [PREENCHER] |
| --shadow-sm | [PREENCHER] | [PREENCHER] |
| --shadow-md | [PREENCHER] | [PREENCHER] |
| --space-unit | [PREENCHER] | [PREENCHER] |

### 9. Acessibilidade
**WCAG target:** [PREENCHER] (AA / AAA)
**Focus visible:** [PREENCHER]
**Contraste minimo texto:** [PREENCHER]
**Area de toque minima:** [PREENCHER]
**Screen reader considerations:** [PREENCHER]

## Exemplo Preenchido

### 3. Botoes (Grão Urbano)
| Variante | Fundo | Texto | Borda | Radius | Padding |
|----------|-------|-------|-------|--------|---------|
| Primario | #5C6B3C | #FFFFFF | none | 8px | 12px 24px |
| Secundario | transparent | #5C6B3C | 1.5px #5C6B3C | 8px | 12px 24px |
| Terciario | transparent | #5C6B3C | none | 8px | 12px 24px |
| Destrutivo | #D94F4F | #FFFFFF | none | 8px | 12px 24px |

### 8. Tokens (parcial)
| Token | Valor | Uso |
|-------|-------|-----|
| --color-primary | #5C6B3C | Botoes, links, acentos |
| --color-accent | #C4663E | CTAs de destaque, badges |
| --radius-sm | 4px | Badges, tags |
| --radius-md | 8px | Botoes, cards, inputs |
| --shadow-sm | 0 1px 3px rgba(0,0,0,0.1) | Cards, dropdowns |
| --space-unit | 8px | Base para todo espacamento |

## Checklist de Qualidade
- [ ] Todos os componentes basicos estao documentados
- [ ] Tokens de design estao definidos e podem ser importados no codigo
- [ ] Acessibilidade WCAG AA esta garantida em todos os componentes
- [ ] Estados interativos (hover, focus, disabled) estao especificados
- [ ] Breakpoints e comportamento responsivo estao definidos
- [ ] O documento esta alinhado com o design system (Figma / Storybook)
