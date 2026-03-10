# Aftermarket Acquisition Framework
> Framework para avaliar e adquirir dominios no mercado secundario para marcas.

---

## Definicao

O Aftermarket Acquisition Framework e um modelo estruturado para avaliar, negociar e adquirir dominios que ja estao registrados por terceiros. No contexto de branding, dominios premium sao ativos estrategicos — o endereco digital define a primeira impressao, a memorabilidade e a autoridade percebida de uma marca. Este framework sistematiza o processo desde a identificacao da necessidade ate o fechamento da aquisicao, minimizando riscos legais e financeiros.

Dominios aftermarket incluem: dominios estacionados (parked), dominios em leilao, dominios expirados e dominios em uso por terceiros. Cada categoria exige abordagem diferente de negociacao e avaliacao de risco.

---

## Quando Usar

- Lancamento de marca nova que precisa de dominio .com premium
- Rebranding onde o dominio desejado ja esta registrado
- Consolidacao de portfolio de dominios para protecao de marca
- Expansao internacional exigindo ccTLDs especificos
- Upgrade de dominio para versao mais curta ou mais memoravel

---

## Estrutura / Modelo

```
┌─────────────────────────────────────────────┐
│        AFTERMARKET ACQUISITION FLOW         │
├─────────────────────────────────────────────┤
│                                             │
│  1. DISCOVERY & ASSESSMENT                  │
│     ├── Identificar dominio-alvo            │
│     ├── Verificar status (WHOIS)            │
│     ├── Classificar tipo de holder          │
│     └── Avaliar alternativas                │
│                                             │
│  2. VALUATION                               │
│     ├── Comparables (vendas similares)      │
│     ├── Trafego organico existente          │
│     ├── Extensao e TLD                      │
│     ├── Comprimento e memorabilidade        │
│     └── Valor estrategico para a marca      │
│                                             │
│  3. APPROACH STRATEGY                       │
│     ├── Contato direto vs broker            │
│     ├── Uso de shell company (anonimato)    │
│     ├── Timing (expiracao, renovacao)       │
│     └── Oferta inicial vs teto             │
│                                             │
│  4. NEGOTIATION & CLOSING                   │
│     ├── Escrow service (Escrow.com)         │
│     ├── Contrato de transferencia           │
│     ├── Verificacao tecnica (DNS)           │
│     └── Registro e protecao pos-compra      │
│                                             │
└─────────────────────────────────────────────┘
```

### Matriz de Tipo de Holder

```
  Holder Type      │ Dificuldade │ Custo Tipico  │ Estrategia
  ─────────────────┼─────────────┼───────────────┼──────────────
  Domainer (invest)│ Media       │ 5x-50x reg    │ Negociacao direta
  Empresa ativa    │ Alta        │ Variavel      │ Broker + paciencia
  Estacionado      │ Baixa-Media │ 2x-20x reg    │ Oferta direta
  Expirado         │ Baixa       │ 1x-5x reg     │ Backorder service
  Cybersquatter    │ Alta        │ UDRP/legal    │ Acao juridica
```

---

## Como Aplicar (Passo a Passo)

### Passo 1: Mapeamento de Necessidade
Defina o dominio ideal (marca.com) e liste 3-5 alternativas aceitaveis. Verifique disponibilidade em WHOIS e historico em archive.org.

### Passo 2: Due Diligence do Dominio
Analise: historico de uso (spam, conteudo adulto afeta SEO), backlinks existentes (Ahrefs/Moz), trafego estimado (SimilarWeb), e status legal (trademarks conflitantes).

### Passo 3: Avaliacao Financeira
Use NameBio, GoDaddy Aftermarket e DN Journal para comparar vendas de dominios similares. Defina um piso (fair market value) e um teto (valor estrategico maximo para a marca).

### Passo 4: Estrategia de Abordagem
Para dominios de alto valor, use um broker ou shell company para nao revelar a identidade da marca compradora (evita inflacao de preco). Para dominios de baixo valor, contato direto via WHOIS ou formulario do site.

### Passo 5: Negociacao
Comece com oferta em 20-30% do teto. Negocie em rodadas. Nunca revele urgencia. Tenha BATNA (melhor alternativa) clara.

### Passo 6: Fechamento Seguro
Use servico de escrow. Verifique transferencia completa (registrar, DNS, auth code). Atualize WHOIS com dados da empresa. Ative renovacao automatica.

---

## Exemplos de Aplicacao

### Exemplo 1: Startup de Fintech
Marca "Nuvem Pay" precisava de nuvempay.com (registrado por domainer). Avaliacao via comparables: R$ 15.000-25.000. Abordagem via broker. Fechamento em R$ 18.000 com escrow. Tempo total: 45 dias.

### Exemplo 2: E-commerce em Rebranding
Empresa mudou de "SuperOfertas" para "Pronto". pronto.com.br estava com empresa inativa. Contato direto via WHOIS. Negociacao de 3 meses. Fechamento em R$ 8.000 + transferencia via Registro.br.

### Exemplo 3: Marca Global Entrando no Brasil
Marca internacional precisava do .com.br. Dominio em uso por pequena empresa local. Estrategia: oferta generosa + assessoria juridica. Contrato incluiu periodo de transicao de 90 dias para o vendedor migrar.

---

## Erros Comuns

1. **Revelar identidade da marca:** Se o vendedor sabe que uma grande empresa quer o dominio, o preco pode multiplicar 10x ou mais.
2. **Nao fazer due diligence de historico:** Dominios com passado de spam podem ter penalidades de SEO que levam meses para recuperar.
3. **Pular o escrow:** Transferencias diretas sem intermediario seguro resultam em fraudes frequentes no mercado de dominios.
4. **Ignorar ccTLDs:** Focar apenas no .com e esquecer .com.br, .pt e outros relevantes para o mercado-alvo.
5. **Nao ter BATNA:** Entrar em negociacao sem alternativa viavel gera dependencia e precos inflados.

---

## Integracao com Outros Frameworks

| Framework | Relacao | Como Conectam |
|-----------|---------|---------------|
| Domain Scoring Matrix | Dependente | Scoring Matrix avalia opcoes; Aftermarket Acquisition executa a compra |
| Digital Namespace | Complementar | Namespace mapeia toda presenca digital; Aftermarket resolve gaps de dominio |
| Defensive Registration | Sequencial | Apos adquirir dominio principal, Defensive Registration protege variacoes |
| Domain Risk Assessment | Pre-requisito | Risk Assessment identifica riscos antes de iniciar aquisicao |

---

## Referencias

- Schwartz, M. (2016). *The Domain Game*. Page Publishing.
- ICANN Domain Name Dispute Resolution Policies (UDRP).
- NameBio.com — Base de dados de vendas historicas de dominios.
- Registro.br — Politicas de transferencia de dominios .br.
