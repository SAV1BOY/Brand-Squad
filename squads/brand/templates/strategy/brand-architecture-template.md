# Arquitetura de Marca
> Template para definir a estrutura e relacao entre marcas, submarcas, produtos e servicos.

## Instrucoes de Uso
Use quando a empresa possui ou planeja ter mais de uma marca, produto ou linha. A arquitetura
define como as marcas se relacionam entre si e com a marca-mae. Preencha apos a definicao da
estrategia da marca principal. Fundamental para empresas em crescimento ou diversificacao.

## Template

### 1. Contexto
**Empresa:** [PREENCHER]
**Numero de marcas/produtos atuais:** [PREENCHER]
**Marcas/produtos planejados (proximo 1-2 anos):** [PREENCHER]
**Desafio de arquitetura:** [PREENCHER]

### 2. Modelo de Arquitetura Escolhido
**Modelo:** [PREENCHER]
- Monolitica (Branded House) — uma marca para tudo
- Endossada (Endorsed) — submarcas com endosso da mae
- Independente (House of Brands) — marcas independentes
- Hibrida — combinacao de modelos

**Justificativa:** [PREENCHER]

### 3. Hierarquia de Marcas
**Marca corporativa:** [PREENCHER]
**Marca principal (master brand):** [PREENCHER]

#### Nivel 1 — Submarcas / Linhas
| Submarca | Relacao com a mae | Publico | Posicionamento |
|----------|-------------------|---------|----------------|
| [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |

#### Nivel 2 — Produtos / Servicos
| Produto | Vinculado a | Naming convention |
|---------|-------------|-------------------|
| [PREENCHER] | [PREENCHER] | [PREENCHER] |
| [PREENCHER] | [PREENCHER] | [PREENCHER] |
| [PREENCHER] | [PREENCHER] | [PREENCHER] |

### 4. Regras de Arquitetura
**Quando criar uma nova submarca:** [PREENCHER]
**Quando usar a marca-mae diretamente:** [PREENCHER]
**Quando criar marca independente:** [PREENCHER]
**Convencao de naming:** [PREENCHER]
**Relacao visual entre niveis:** [PREENCHER]

### 5. Diagrama de Arquitetura
```
[PREENCHER — representacao visual da hierarquia]
Exemplo:
MARCA CORPORATIVA
├── Master Brand
│   ├── Submarca A
│   │   ├── Produto A1
│   │   └── Produto A2
│   ├── Submarca B
│   └── Servico C
└── Marca Independente X
```

### 6. Implicacoes de Identidade
| Nivel | Logo | Cores | Tipografia | Tom de voz |
|-------|------|-------|------------|------------|
| Master brand | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| Submarcas | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| Produtos | [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |

### 7. Governanca
**Quem aprova novas marcas:** [PREENCHER]
**Processo de aprovacao:** [PREENCHER]
**Revisao periodica da arquitetura:** [PREENCHER]

## Exemplo Preenchido

### 3. Hierarquia de Marcas
**Marca corporativa:** Grão Urbano Alimentos Ltda.
**Marca principal (master brand):** Grão Urbano

#### Nivel 1 — Submarcas / Linhas
| Submarca | Relacao com a mae | Publico | Posicionamento |
|----------|-------------------|---------|----------------|
| Grão Urbano Cafe | Endossada | Amantes de cafe especial | Cafes de torra artesanal |
| Grão Urbano Kitchen | Endossada | Almoco executivo | Refeicoes completas plant-based |
| Sprouta (app delivery) | Independente com endosso | Digital-first, delivery | Delivery plant-based rapido |

### 5. Diagrama
```
GRÃO URBANO ALIMENTOS (corporativa)
├── Grão Urbano (master brand)
│   ├── Grão Urbano Café (cafes especiais)
│   ├── Grão Urbano Kitchen (refeicoes)
│   └── Grão Urbano Market (varejo embalados)
└── Sprouta (app delivery — "por Grão Urbano")
```

## Checklist de Qualidade
- [ ] O modelo de arquitetura esta justificado estrategicamente
- [ ] Todos os niveis da hierarquia estao mapeados
- [ ] Regras claras para criacao de novas marcas existem
- [ ] Implicacoes de identidade por nivel estao definidas
- [ ] O diagrama visual e claro e compreensivel
- [ ] Governanca de aprovacao esta formalizada
