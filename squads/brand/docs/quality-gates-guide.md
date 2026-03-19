# Guia de Quality Gates — Brand Squad

> Documento operacional que define os quality gates do Brand Squad,
> garantindo que nenhum output saia abaixo do padrao GOLD.

---

## 1. Objetivo

Quality gates sao pontos de verificacao obrigatorios no fluxo de trabalho
do Brand Squad. Eles existem para garantir que cada entrega — de um agente
individual ate o handoff cross-squad — atenda ao nivel minimo de qualidade
exigido pelo sistema HRM.

Nenhum output avanca para a proxima etapa sem passar pelo gate correspondente.
O padrao GOLD e inegociavel: se nao passou no gate, nao sai do squad.

---

## 2. Tipos de Gates

O Brand Squad opera com 5 tipos de quality gates, organizados em cascata.

### 2.1 Per-Agent Gate

Cada agente valida seu proprio output antes de entregar ao fluxo.
O agente aplica os criterios do seu framework principal e verifica
se o output atende ao minimo esperado para sua especialidade.

- **Responsavel**: o proprio agente executor
- **Criterios**: definidos no arquivo do agente (agents/*.md)
- **Momento**: antes de submeter o output para o task gate

### 2.2 Per-Task Gate

Checklists obrigatorios definidos no config.yaml para cada task.
O routing section do config.yaml especifica quais checklists sao
aplicados a cada task — sem excecao.

- **Responsavel**: sistema de routing (config.yaml)
- **Criterios**: checklists/ correspondentes (ex: aaker/aaker-equity-audit)
- **Momento**: apos agente concluir, antes de consolidacao

### 2.3 Per-Layer Gate

Gates de transicao entre camadas do sistema (Research → Strategy →
Identity → Activation). Cada transicao exige validacao especifica
definida em checklists/layer-gate-*.md.

- **Responsavel**: brand-chief + approvers definidos no config.yaml
- **Criterios**: checklists de transicao de layer (layer_transitions no config.yaml)
- **Momento**: na transicao entre camadas (ver ARCHITECTURE.md, Secao 1)

### 2.4 Chief Gate

O brand-chief revisa o output consolidado de uma task completa,
avaliando coerencia entre as contribuicoes dos diferentes agentes
e alinhamento com a estrategia geral da marca.

- **Responsavel**: brand-chief (config.yaml → chief_agent)
- **Criterios**: coerencia, completude, alinhamento estrategico
- **Momento**: apos todos os agent e task gates passarem

### 2.5 Final Gate

Validacao final antes do handoff cross-squad. Garante que o pacote
de entrega esta completo, documentado e no formato esperado pelo
squad receptor.

- **Responsavel**: brand-chief
- **Criterios**: contrato de handoff + acceptance criteria do receptor
- **Momento**: antes de qualquer transferencia para outro squad

---

## 3. Cascade Logic

Os gates seguem uma sequencia rigida. Nenhum gate posterior pode
ser executado se o anterior nao foi aprovado.

```
Agent Gate → Task Gate → Layer Gate → Chief Gate → Final Gate
```

Se qualquer gate retorna RED, o fluxo para e entra em rework loop
(ver docs/rework-loops-guide.md). Se retorna YELLOW, o brand-chief
deve decidir se aprova com override ou envia para rework.

---

## 4. Scoring Rubric Unificado

Todos os gates usam o mesmo sistema de pontuacao para consistencia.

### GREEN (>= 80%)
- **Status**: Aprovado
- **Acao**: output segue para a proxima etapa sem restricoes
- **Registro**: score registrado no registry da task

### YELLOW (60-79%)
- **Status**: Aprovado com ressalvas
- **Acao**: requer override explicito do brand-chief com justificativa documentada
- **Registro**: score + justificativa do override registrados
- **Nota**: brand-chief assume responsabilidade pelo avanco

### RED (< 60%)
- **Status**: Bloqueado
- **Acao**: rework obrigatorio, output nao avanca sob nenhuma circunstancia
- **Registro**: score + gap analysis registrados
- **Proximo passo**: inicia rework loop (ver docs/rework-loops-guide.md)

---

## 5. Enforcement Rules

1. **RED bloqueia progressao**: nenhum override possivel para RED
2. **YELLOW exige chief override**: apenas brand-chief pode aprovar YELLOW,
   e deve documentar a justificativa no brand-decisions-log
3. **Todos os scores sao registrados**: em data/registries/brand-decisions-log
4. **Gates nao podem ser pulados**: mesmo em situacoes de urgencia
5. **Rework tem limite**: maximo 3 loops antes de escalacao automatica
   (ver docs/escalation-protocol.md)

---

## 6. Conexao com config.yaml

O config.yaml e a fonte de verdade para o roteamento de quality gates.
A secao `routing` define, para cada task:

- **checklists**: quais checklists sao aplicados (Per-Task Gate)
- **agents**: quais agentes executam (Per-Agent Gate)
- **registry**: onde os resultados sao registrados

A secao `quality_gates` define:

- **layer_transitions**: checklists e approvers por transicao de camada
- **scoring**: thresholds GREEN/YELLOW/RED
- **enforcement**: regras de bloqueio e registro
- **cascade**: ordem dos 5 gates

---

## 7. Conexao com ARCHITECTURE.md

O ARCHITECTURE.md (Secao 1 — Diagrama de Camadas) define as 4 camadas
operacionais: Research, Strategy, Identity e Activation. Os Per-Layer
Gates operam exatamente nas transicoes entre essas camadas.

A camada de Governance no ARCHITECTURE.md e onde os quality gates vivem
conceitualmente — ela permeia todas as outras camadas e garante que o
padrao GOLD seja mantido em cada transicao.

---

## 8. Resumo Rapido

| Gate         | Responsavel    | Quando                    | Criterio Base           |
|--------------|----------------|---------------------------|-------------------------|
| Per-Agent    | Agente         | Antes de entregar output  | Framework do agente     |
| Per-Task     | Sistema        | Apos execucao da task     | Checklists config.yaml  |
| Per-Layer    | brand-chief    | Transicao entre camadas   | Checklist de transicao  |
| Chief        | brand-chief    | Output consolidado        | Coerencia + estrategia  |
| Final        | brand-chief    | Antes de handoff          | Contrato de handoff     |

---

> **Regra de ouro**: Na duvida, o gate bloqueia. Melhor rework do que
> entregar abaixo do padrao.
