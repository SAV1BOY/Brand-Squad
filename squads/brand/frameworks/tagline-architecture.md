# Tagline Architecture
> Framework para criar, classificar e gerenciar taglines e slogans em diferentes niveis do portfolio de marca.

---

## Definicao

Tagline Architecture e o sistema que organiza as frases de efeito de uma marca em uma hierarquia logica — da tagline corporativa (perene e estrategica) ate slogans de campanha (temporarios e taticos). Cada nivel tem uma funcao diferente, e a gestao integrada garante que todas as frases reforcem o posicionamento sem se contradizerem.

Uma tagline corporativa sintetiza a essencia da marca em poucas palavras e dura anos ou decadas. Um slogan de campanha traduz a tagline para um momento ou publico especifico e muda periodicamente. Linhas descritivas explicam o que a marca faz (uteis para marcas com nomes abstratos). A confusao entre esses niveis e uma das causas mais comuns de inconsistencia verbal.

## Quando Usar

- Ao criar ou revisar a tagline principal da marca
- Para organizar a hierarquia de frases quando ha multiplas linhas em uso
- Ao briefar campanhas que precisam de slogans alinhados a tagline master
- Para decidir se a marca precisa de tagline, descriptor, slogan — ou todos

## Estrutura / Modelo

```
┌─────────────────────────────────────────────┐
│          TAGLINE ARCHITECTURE               │
│                                             │
│  NIVEL 1: TAGLINE CORPORATIVA (Perene)      │
│  Sintetiza a essencia da marca.             │
│  Duracac: 5-20+ anos                       │
│  Ex: Nike "Just Do It" | Apple "Think      │
│      Different" | Itau "Feito para voce"   │
│                                             │
│  NIVEL 2: DESCRIPTOR (Funcional)            │
│  Explica o que a marca faz.                │
│  Usado quando o nome e abstrato.            │
│  Ex: Salesforce "The CRM Company"           │
│                                             │
│  NIVEL 3: SLOGAN DE CAMPANHA (Temporario)   │
│  Traduz a tagline para um momento.          │
│  Duracao: 3-12 meses                        │
│  Ex: Coca-Cola "Taste the Feeling"          │
│                                             │
│  NIVEL 4: LINHA DE PRODUTO (Especifico)     │
│  Diferencia produto dentro do portfolio.    │
│  Ex: iPhone "The best iPhone yet"           │
│                                             │
│  ┌─────────────────────────────────────┐    │
│  │ Tagline Master                       │   │
│  │   └── Descriptor (se necessario)     │   │
│  │       └── Slogan Campanha 2024       │   │
│  │           └── Linha Produto A        │   │
│  │           └── Linha Produto B        │   │
│  └─────────────────────────────────────┘    │
└─────────────────────────────────────────────┘
```

## Como Aplicar (Passo a Passo)

1. **Audite as frases existentes**: Liste todas as taglines, slogans e descriptors em uso. Identifique sobreposicoes, contradicoes e redundancias.
2. **Defina a tagline master**: Ela deve sintetizar o posicionamento em 3-7 palavras. Teste: funciona sem o logo? E memoravel? Diferencia?
3. **Avalie a necessidade de descriptor**: Se o nome da marca nao comunica o que ela faz (ex: "Nubank" sem "banco digital"), um descriptor funcional e necessario.
4. **Crie framework para slogans de campanha**: Estabeleca regras — todo slogan deve derivar da tagline master e nao contradize-la.
5. **Documente a hierarquia**: Crie um guia visual que mostre como cada nivel funciona, onde aparece e quais sao os limites de criacao.

## Exemplos de Aplicacao

**Nike**: Tagline master = "Just Do It" (desde 1988, perene). Slogans de campanha = "You Can't Stop Us", "Dream Crazy" (temporarios, mas sempre derivados do espirito de superacao de "Just Do It"). Nao usa descriptor porque o nome e o swoosh sao suficientes.

**Bradesco**: Tagline master = "Presenca" ou variantes como "E so comecar". Descriptor implicito via contexto (banco). Slogans de campanha mudam por temporada mas mantem o tom de proximidade e encorajamento que a tagline master define.

## Erros Comuns

- **Confundir slogan de campanha com tagline master**: Trocar a tagline corporativa a cada campanha gera inconsistencia e impede a construcao de associacao de longo prazo.
- **Tagline que descreve em vez de inspirar**: "Lider em solucoes de TI" e descriptor, nao tagline. A tagline deve evocar emocao ou atitude.
- **Muitas frases sem hierarquia**: Se a marca tem tagline, descriptor, slogan, lema interno e frase de campanha sem organizacao, o consumidor recebe mensagens fragmentadas.

## Integracao com Outros Frameworks

| Framework | Conexao |
|---|---|
| Verbal Identity System | Taglines sao um componente do sistema verbal mais amplo |
| Messaging House | A tagline master funciona como o "telhado" da casa de mensagens |
| Brand Positioning Statement | A tagline e a expressao publica e condensada do posicionamento |

## Referencias

- Wheeler, A. (2017). *Designing Brand Identity*. Wiley. Cap. 3 — Brand Language.
- Ries, A. & Ries, L. (2002). *The 22 Immutable Laws of Branding*. Harper Business. Cap. 10 — Law of the Word.
