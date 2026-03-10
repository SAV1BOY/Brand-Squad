# Construtor de Teste de Distinctive Assets

> Cria testes para medir fama e unicidade dos assets distintivos de uma marca.

## Objetivo

Projetar e executar testes que medem quao reconheciveis e unicos sao os distinctive assets de uma marca, seguindo metodologia Sharp/Romaniuk.

## Inputs

- Lista de distinctive assets da marca (logo, cor, tipografia, som, etc.)
- Publico-alvo para o teste
- Concorrentes para comparacao
- Assets de concorrentes para cross-test

## Processo

### 1. Design do Teste

**Teste de Fama (Recognition)**
- Mostrar asset isolado (sem nome da marca)
- Perguntar: "Voce reconhece isso? De que marca e?"
- Medir: % que reconhece corretamente

**Teste de Unicidade (Attribution)**
- Mostrar asset junto com assets de concorrentes
- Perguntar: "Qual marca usa [cor/forma/som]?"
- Medir: % que atribui corretamente e exclusivamente

**Teste de Associacao (Speed)**
- Mostrar nome da marca por 3 segundos
- Pedir: "Que elementos visuais voce associa?"
- Medir: quais assets sao lembrados espontaneamente

### 2. Metodologia

- Amostra minima: 100 respondentes no publico-alvo
- Mix: 50% clientes + 50% nao-clientes da categoria
- Formato: Survey online com imagens/audio
- Controle: Incluir assets falsos para calibrar

### 3. Analise

Plotar cada asset no Distinctive Asset Grid:
- Eixo X: Unicidade (0-100%)
- Eixo Y: Fama (0-100%)
- Classificar: Estrela, Emergente, Generico ou Fraco

## Output

Mapa de assets no grid com recomendacoes: quais proteger, quais fortalecer, quais abandonar.

## Exemplo de Uso

```
> distinctive-assets-test --brand "MarcaX" --assets "logo,cor,tagline,mascote"
> Logo: Estrela (Fama 85%, Unicidade 90%)
> Cor: Emergente (Fama 40%, Unicidade 80%)
> Tagline: Generico (Fama 70%, Unicidade 30%)
> Mascote: Fraco (Fama 20%, Unicidade 60%)
```
