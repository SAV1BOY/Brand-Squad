# Social Media Brand Rollout
> Implementacao da nova marca em todos os canais de redes sociais.

## Objetivo
Executar o rollout da marca nas redes sociais — atualizando perfis, bios, templates, tom de voz e conteudo visual — garantindo consistencia e impacto em todas as plataformas.

## Agentes
- **emily-heyward** — lidera a estrategia de rollout social
- **donald-miller** — valida messaging e bios
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Brand Guidelines atuais
- Brand Voice Guide
- Templates de social media
- Lista de canais e perfis sociais
- Calendario de lancamento

## Passos
1. Inventariar todos os perfis e canais sociais
2. Atualizar fotos de perfil e capas
3. Reescrever bios e descricoes alinhadas a messaging
4. Criar templates visuais para cada plataforma
5. Definir tom de voz por plataforma (adaptacoes)
6. Publicar conteudo de lancamento/transicao
7. Atualizar links, destaques e informacoes fixas
8. Monitorar reacao e engajamento pos-rollout

## Frameworks Obrigatorios
- activation-layer
- verbal-identity-system

## Checklists de Qualidade
- brand-guidelines-quality
- Consistencia visual entre plataformas verificada
- Messaging alinhada em todos os perfis

## Output Esperado
```
## Social Media Brand Rollout
### Canais Atualizados: [lista com status]
### Perfis: [foto, capa, bio — por plataforma]
### Templates: [criados por formato e plataforma]
### Tom por Plataforma: [adaptacoes definidas]
### Conteudo de Lancamento: [posts publicados]
### Metricas: [engajamento pos-rollout]
```

## Registro
- `data/registries/brand-touchpoints-registry`

---

## Governanca da Task

### Quality Gates
- Gate de entrada: brand guidelines e brand voice guide disponiveis, templates de social media criados, calendario de lancamento definido
- Gate de saida: score GREEN (>=80%) no checklist brand-guidelines-quality, consistencia visual e messaging verificadas em todas as plataformas
- Score minimo: GREEN (>=80%) no checklist principal

### Escalacao
- Se quality gate RED apos 2 tentativas → escalar para brand-chief
- Se conflito entre emily-heyward e donald-miller sobre messaging em redes sociais → brand-chief arbitra
- Se task fora do escopo → registrar em data/registries/risk-log e redirecionar

### Rework Loop
- Max 3 loops de rework por task
- Cada loop gera rework brief com falhas especificas (perfis inconsistentes, bios desalinhadas, templates fora do padrao, etc.)
- Apos 3 loops → escalacao automatica nivel 2
- Registro: data/registries/improvement-backlog

### Handoff
- Upstream: brand-guidelines-creation, brand-voice-development, campaign-activation-brief
- Downstream: consistency-review, social-sentiment-analysis
- Cross-squad: marketing squad (coordenacao de conteudo social)

### Metricas
- Numero de canais/perfis atualizados
- Score de consistencia entre plataformas
- Engajamento pos-rollout vs. baseline
