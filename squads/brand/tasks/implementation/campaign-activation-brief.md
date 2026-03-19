# Campaign Activation Brief
> Criacao de brief de ativacao de campanha alinhado a estrategia de marca.

## Objetivo
Desenvolver um briefing completo de campanha que traduza a estrategia de marca em diretrizes acionaveis para equipes criativas e de midia — garantindo que cada campanha reforce o posicionamento e os distinctive assets.

## Agentes
- **emily-heyward** — lidera o brief criativo com foco em lancamento
- **donald-miller** — valida messaging e narrativa
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Strategy Document
- Messaging House
- Brand Guidelines
- Objetivos de negocio da campanha
- Budget e canais disponiveis

## Passos
1. Definir objetivo da campanha e KPIs
2. Identificar audiencia-alvo e insight do consumidor
3. Definir mensagem central (alinhada a messaging house)
4. Especificar tom e abordagem criativa
5. Listar distinctive assets obrigatorios
6. Definir canais e formatos
7. Especificar do's & don'ts de marca
8. Documentar brief completo para equipe criativa

## Frameworks Obrigatorios
- activation-layer
- miller-storybrand-sb7
- heyward-obviousness-method

## Checklists de Qualidade
- brand-messaging-quality
- heyward/brand-launch-readiness-audit

## Output Esperado
```
## Campaign Activation Brief
### Objetivo: [meta + KPIs]
### Audiencia: [perfil + insight]
### Mensagem Central: [headline + supporting]
### Tom e Abordagem: [diretrizes criativas]
### Distinctive Assets Obrigatorios: [lista]
### Canais e Formatos: [especificacao]
### Do's & Don'ts: [regras de marca]
### Timeline: [datas-chave]
```

## Registro
- `data/registries/brand-decisions-log`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand strategy document, messaging house e brand guidelines disponiveis, objetivos de campanha definidos
- Gate de saida: score GREEN (>=80%) nos checklists brand-messaging-quality e heyward/brand-launch-readiness-audit
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre emily-heyward e donald-miller sobre abordagem criativa → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (brief incompleto, messaging desalinhada, distinctive assets ausentes, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: messaging-house-development, brand-guidelines-creation, storybrand-script
- Downstream: launch-coordination, social-media-brand-rollout
- Cross-squad: marketing squad (brief para execucao de campanha), copy squad (messaging para criacao)

### Metricas
- Completude do brief (todos os campos preenchidos)
- Alinhamento com messaging house (pass/fail)
- Numero de distinctive assets obrigatorios especificados
