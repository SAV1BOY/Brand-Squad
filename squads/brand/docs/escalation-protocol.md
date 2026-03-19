# Protocolo de Escalacao — Brand Squad

> Documento operacional que define quando e como escalar decisoes
> acima do nivel do agente dentro do Brand Squad.

---

## 1. Objetivo

Nem toda situacao pode ser resolvida no nivel do agente executor.
Este protocolo define os triggers que iniciam uma escalacao, a cadeia
de responsabilidade, as evidencias necessarias e os tempos maximos
para cada nivel.

O objetivo e garantir que problemas sejam resolvidos no nivel mais
baixo possivel, mas que escalem rapidamente quando necessario.

---

## 2. Triggers de Escalacao

Uma escalacao e disparada quando qualquer uma das seguintes condicoes
ocorre:

### 2.1 Quality Gate RED apos 3 Rework Loops
O agente tentou corrigir o output 3 vezes e o quality gate continua
retornando RED. O rework loop esgotou (ver docs/rework-loops-guide.md).

### 2.2 Conflito entre 2+ Agentes sem Resolucao
Dois ou mais agentes chegaram a conclusoes conflitantes sobre a mesma
decisao de marca e nao conseguem convergir autonomamente.

### 2.3 Task fora do Escopo do Squad
A task requer competencias ou decisoes que estao fora do dominio do
Brand Squad (ex: decisoes de pricing, tecnologia, operacoes).

### 2.4 Stakeholder Override Request
Um stakeholder externo solicita mudanca que contradiz uma decisao
ja tomada e validada pelo squad.

### 2.5 Deadline em Risco
O prazo de entrega esta comprometido e a task nao pode ser concluida
dentro do SLA acordado sem sacrificar qualidade.

### 2.6 Decisao com Impacto Cross-Squad
A decisao afeta outros squads (Copy, Marketing, Product, Design, People)
e requer alinhamento antes de ser implementada.

---

## 3. Cadeia de Escalacao

### Nivel 1 — Re-execucao pelo Agente

O agente re-executa a task com um rework brief detalhado.

- **Responsavel**: agente executor original
- **Acao**: re-executar com foco nas falhas identificadas pelo gate
- **Tempo maximo**: definido pelo SLA da task (geralmente 1 ciclo)
- **Saida**: output revisado submetido ao mesmo quality gate

### Nivel 2 — Arbitragem pelo brand-chief

O brand-chief assume a decisao, analisando as posicoes conflitantes
e aplicando o Protocolo de Arbitragem.

- **Responsavel**: brand-chief (config.yaml → chief_agent)
- **Acao**: revisar evidencias, arbitrar entre posicoes, decidir
- **Tempo maximo**: 1 ciclo apos receber evidencias completas
- **Saida**: decisao documentada no brand-decisions-log com justificativa

### Nivel 3 — HRM Chief Review

Decisao final do sistema. O HRM Chief (nivel acima do squad) revisa
o caso completo e emite decisao definitiva.

- **Responsavel**: HRM Chief (nivel sistema)
- **Acao**: revisar historico completo, decidir com autoridade final
- **Tempo maximo**: 2 ciclos apos receber pacote de escalacao
- **Saida**: decisao irrecorrivel registrada no brand-decisions-log

---

## 4. Evidencias Requeridas por Nivel

Cada nivel de escalacao exige evidencias cumulativas. O nivel superior
recebe tudo que o nivel anterior ja produziu, mais evidencias adicionais.

### Nivel 1 — Evidencias
- Output original do agente
- Score do quality gate (com detalhamento por criterio)
- Gap analysis: quais criterios falharam e por que

### Nivel 2 — Evidencias (N1 + adicionais)
- Tudo de N1
- Posicoes conflitantes documentadas (se aplicavel)
- Trade-offs identificados entre as opcoes
- Recomendacao do agente sobre caminho preferido

### Nivel 3 — Evidencias (N2 + adicionais)
- Tudo de N2
- Historico completo de tentativas (todos os rework loops)
- Impacto estimado em outros squads e timelines
- Cenarios de resolucao com pros e contras

---

## 5. Template de Escalation Request

```markdown
# Escalation Request

## Metadata
- **Data**: [YYYY-MM-DD]
- **Task**: [nome da task]
- **Agente Solicitante**: [nome do agente]
- **Nivel de Escalacao**: [N1 / N2 / N3]
- **Trigger**: [qual dos 6 triggers se aplica]

## Contexto
[Descricao breve do que aconteceu e por que a escalacao e necessaria]

## Evidencias
[Anexar ou referenciar todos os artefatos exigidos pelo nivel]

## Tentativas Anteriores
[Lista de tentativas ja realizadas e seus resultados]

## Impacto
- **No squad**: [como afeta o Brand Squad]
- **Cross-squad**: [como afeta outros squads, se aplicavel]
- **Timeline**: [impacto no cronograma]

## Recomendacao
[Posicao do solicitante sobre a melhor resolucao]
```

---

## 6. Registro

Todas as escalacoes sao registradas em:
- **Local**: data/registries/brand-decisions-log
- **Campos obrigatorios**: data, trigger, nivel, decisao, justificativa
- **Retencao**: permanente — escalacoes sao parte do historico de aprendizado

Escalacoes alimentam o improvement-backlog automaticamente
(ver docs/learning-and-memory-guide.md).

---

## 7. Tempos Maximos por Nivel

| Nivel | Responsavel   | Tempo Maximo           | Se Exceder              |
|-------|---------------|------------------------|-------------------------|
| N1    | Agente        | 1 ciclo (SLA da task)  | Escala para N2          |
| N2    | brand-chief   | 1 ciclo apos evidencias| Escala para N3          |
| N3    | HRM Chief     | 2 ciclos apos pacote   | Decisao por prioridade  |

---

## 8. Regras Gerais

1. **Escalar cedo, nao tarde**: se o trigger existe, escalar imediatamente
2. **Evidencias sao obrigatorias**: escalacao sem evidencias e rejeitada
3. **Cada nivel tenta resolver**: nao pular niveis salvo emergencia critica
4. **Decisoes sao finais no nivel em que foram tomadas**: N2 nao revisita N1
5. **Tudo e registrado**: nenhuma escalacao pode acontecer sem registro
6. **Aprendizado**: toda escalacao gera entry no improvement-backlog

---

> **Principio**: Escalar nao e falha — e o sistema funcionando como projetado.
> A falha e nao escalar quando os triggers estao presentes.
