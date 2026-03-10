# Verificador de Disponibilidade de Handles

> Checagem sistematica de handles em redes sociais para candidatos de nome.

## Objetivo

Verificar disponibilidade de usernames/handles em todas as plataformas relevantes para cada candidato de nome.

## Inputs

- Lista de candidatos de nome
- Plataformas prioritarias
- Variacoes aceitaveis de handle

## Processo

### 1. Plataformas Prioritarias
| Plataforma | Handle Format | Prioridade |
|-----------|---------------|-----------|
| Instagram | @[nome] | Alta |
| Twitter/X | @[nome] | Alta |
| LinkedIn | /company/[nome] | Alta |
| TikTok | @[nome] | Media |
| YouTube | @[nome] | Media |
| Facebook | /[nome] | Media |
| Pinterest | /[nome] | Baixa |

### 2. Variacoes Aceitaveis
Se @[nome] nao disponivel:
- @[nome]oficial
- @[nome]br
- @use[nome]
- @get[nome]
- @[nome]_

### 3. Avaliar Handles Ocupados
- Conta esta ativa? (postou nos ultimos 6 meses?)
- Conta tem muitos seguidores? (dificil de adquirir)
- Conta parece abandonada? (possivel recuperacao via plataforma)
- E squatting obvio? (pode contestar em algumas plataformas)

## Output

Matriz de disponibilidade por candidato e plataforma.

| Nome | IG | TW | LI | TT | YT | FB | Score |
|------|----|----|----|----|----|----|----|
| [A] | ✅ | ✅ | ✅ | ❌ | ✅ | ✅ | 5/6 |

## Exemplo de Uso

```
> handle-availability-checker --names "Planto,Investi"
> Planto: 4/6 disponiveis (IG: ✅, TW: ✅, LI: ✅, TT: ✅, YT: ❌, FB: ❌)
> Investi: 3/6 disponiveis (IG: ❌, TW: ✅, LI: ✅, TT: ❌, YT: ✅, FB: ❌)
```
