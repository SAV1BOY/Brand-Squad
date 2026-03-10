# Create New Brand Agent
> Criacao e configuracao de um novo agente especialista para o Brand Squad.

## Objetivo
Adicionar um novo agente especialista ao Brand Squad — definindo seu perfil, expertise, frameworks, dominio de atuacao e integracoes com o config.yaml — expandindo as capacidades do squad.

## Agentes
- **brand-chief** — lidera a criacao e integracao

## Inputs
- Necessidade identificada (gap de expertise)
- Referencia do especialista/autor a modelar
- Frameworks e metodologias do especialista
- Obras e publicacoes de referencia

## Passos
1. Identificar gap de expertise no squad atual
2. Selecionar especialista/autor a ser modelado
3. Pesquisar frameworks, metodologias e principios-chave
4. Redigir agent file seguindo padrao dos existentes
5. Definir role, layer e domain no config.yaml
6. Mapear routing (quais tasks o agente participa)
7. Testar integracao com workflows existentes
8. Documentar e publicar novo agente

## Frameworks Obrigatorios
- HRM (Hierarchical Role Modeling)

## Checklists de Qualidade
- Agent file segue estrutura padrao
- Domain e expertise claramente definidos
- Routing configurado no config.yaml
- Nao conflita com agentes existentes

## Output Esperado
```
## Novo Agente
### Nome: [nome do agente]
### Role: [specialist/sub-specialist]
### Layer: [research/strategy/identity/etc.]
### Domain: [expertise especifica]
### Frameworks: [lista de frameworks]
### Tasks Assignadas: [lista de tasks no routing]
### Arquivo: agents/[nome].md
```

## Registro
- `data/registries/brand-decisions-log`
