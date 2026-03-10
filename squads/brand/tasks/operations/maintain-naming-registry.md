# Maintain Naming Registry
> Manutencao do registro de nomes, dominios e handles da marca.

## Objetivo
Manter o naming registry atualizado com todos os nomes registrados, dominios adquiridos, handles reservados e status legal — servindo como fonte unica de verdade para gestao de naming.

## Agentes
- **naming-strategist** — lidera a manutencao do registro
- **brand-chief** — orquestracao e aprovacao

## Inputs
- Naming Registry atual
- Novos nomes registrados
- Status de renovacao de dominios
- Atualizacoes de status legal/trademark

## Passos
1. Revisar registro atual de nomes
2. Atualizar status de cada nome (ativo, reservado, expirado)
3. Verificar datas de renovacao de dominios
4. Atualizar status de trademarks e registros legais
5. Registrar novos nomes e handles adquiridos
6. Identificar nomes e dominios a vencer
7. Recomendar renovacoes ou releases
8. Publicar registro atualizado

## Frameworks Obrigatorios
- naming-systems

## Checklists de Qualidade
- naming/naming-legal-screening-checklist
- Dominios com data de renovacao verificada
- Handles ativos em todas as plataformas

## Output Esperado
```
## Naming Registry (Atualizado)
### Data: [data da atualizacao]
### Nomes Ativos: [lista com status legal]
### Dominios: [lista com data de vencimento]
### Handles: [por plataforma com status]
### Trademarks: [status de registro]
### Alertas: [vencimentos proximos]
### Acoes Necessarias: [renovacoes e aquisicoes]
```

## Registro
- `data/registries/naming-registry`
