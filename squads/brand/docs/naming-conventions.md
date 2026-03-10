# Convenções de Nomenclatura

> Padrões de nomes para arquivos, diretórios e elementos do Brand Squad.

## Arquivos

### Regra Geral
- Lowercase (minúsculas)
- Hifens para separar palavras (kebab-case)
- Extensão `.md` para todos os documentos
- Sem espaços, acentos ou caracteres especiais

### Exemplos
- `brand-strategy-framework.md` (correto)
- `Brand Strategy Framework.md` (incorreto)
- `brandStrategyFramework.md` (incorreto)

### Padrões por Tipo
- Frameworks: `[autor]-[nome-framework].md`
- Checklists: `[tema]-checklist.md`
- Templates: `[tipo]-template.md`
- Componentes: `[nome]-component.md`
- Padrões: `[nome]-pattern.md`
- Projetos: `[tipo]-project.md`
- Cases: `[marca]-[tema].md`

## Diretórios

### Regra Geral
- Lowercase com hifens (kebab-case)
- Nomes curtos e descritivos
- Máximo 2 palavras quando possível
- Sem abreviações obscuras

### Estrutura
```
squads/brand/
  agents/
  archive/
    iconic-brands/
    iconic-rebrands/
    brand-failures/
    category-creation/
    evolution/
  authority/
  checklists/
  docs/
  frameworks/
  lib/
    components/
    patterns/
    utilities/
  phrases/
  projects/
  templates/
  voice/
  workflows/
```

## Elementos Internos

### Títulos de Documentos
- Em português, com acentuação
- Capitalização de título (primeira letra maiúscula das palavras principais)
- Consistente com o propósito do arquivo

### Seções
- `##` para seções principais
- Nomes curtos e diretos
- Consistentes entre documentos do mesmo tipo

## Quando Criar Novo Arquivo vs Editar Existente

- Novo tema ou conceito: criar novo arquivo
- Atualização de conteúdo: editar existente
- Expansão significativa de tópico: pode justificar split
- Sempre prefira arquivos focados a arquivos extensos
