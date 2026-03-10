# Verificador de Disponibilidade de Dominio

> Checagem sistematica de disponibilidade de dominios para candidatos de nome.

## Objetivo

Verificar disponibilidade de dominios relevantes para cada candidato de nome e identificar alternativas viaveis.

## Inputs

- Lista de candidatos de nome
- TLDs prioritarios (.com, .com.br, .io, .co, etc.)
- Orcamento para aquisicao de dominio (se aplicavel)

## Processo

### 1. Verificacao Primaria
Para cada candidato, checar:
- [nome].com
- [nome].com.br
- [nome].io
- [nome].co

### 2. Variacoes
Se primario nao disponivel, testar:
- get[nome].com
- [nome]app.com
- [nome]hq.com
- try[nome].com
- use[nome].com
- go[nome].com

### 3. Avaliar Dominios Ocupados
- Dominio esta em uso ativo? (site funcional)
- Dominio esta estacionado? (pode ser adquirivel)
- Whois mostra proprietario contactavel?
- Plataformas como Sedo, Afternic tem o dominio listado?

### 4. Estimativa de Custo
| Dominio | Status | Custo Estimado |
|---------|--------|---------------|
| [nome].com | Disponivel/Estacionado/Ativo | $X |

## Output

Relatorio de disponibilidade por candidato com recomendacao de melhor opcao e custo estimado.

## Exemplo de Uso

```
> domain-availability-checker --names "Planto,Investi,Grana"
> Planto.com: Estacionado ($2,500 estimado)
> Planto.com.br: Disponivel ($40/ano)
> Investi.com.br: Disponivel ($40/ano)
> Grana.com: Ativo (indisponivel)
```
