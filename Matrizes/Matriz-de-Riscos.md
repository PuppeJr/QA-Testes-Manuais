# Matriz de Riscos

## Objetivo

Identificar, classificar e acompanhar os principais riscos relacionados às atividades de testes do projeto.

---

## Classificação

### Probabilidade

| Probabilidade | Significado                 |
|---------------|-----------------------------|
| Alta          | Pode ocorrer frequentemente |
| Média         | Pode ocorrer eventualmente  |
| Baixa         | Pouco provável              |

### Impacto

| Impacto | Significado                         |
|---------|-------------------------------------|
| Alto    | Compromete funcionalidades críticas |
| Médio   | Afeta parcialmente o sistema        |
| Baixo   | Pouco impacto para o usuário        |

---

## Tabela de Riscos

| ID     | Risco                      | Probabilidade | Impacto | Prioridade | Mitigação                                            | Status |
|--------|----------------------------|---------------|---------|------------|------------------------------------------------------|--------|
| RK-001 | Login indisponível         | Média         | Alto    | Alta       | Executar testes de autenticação antes da homologação | ?     |
| RK-002 | Ambiente UAT indisponível  | Média         | Alto    | Alta       | Validar disponibilidade antes da execução            | ?     |
| RK-003 | Casos de teste incompletos | Baixa         | Alto    | Alta       | Revisão técnica dos documentos                       | ?     |
| RK-004 | Evidências insuficientes   | Média         | Médio   | Média      | Padronizar template de evidências                    | ?     |
| RK-005 | Bugs sem rastreabilidade   | Baixa         | Alto    | Alta       | Atualizar Matriz de Rastreabilidade                  | ?     |
| RK-006 | Massa de testes incorreta  | Média         | Médio   | Média      | Validar dados antes da execução                      | ?     |
| RK-007 | Alterações sem regressão   | Média         | Alto    | Alta       | Executar suíte de regressão                          | ?     |
| RK-008 | Falta de documentação      | Baixa         | Alto    | Média      | Atualizar documentação continuamente                 | ?     |

---

## Revisão

A matriz será revisada ao término de cada sprint para inclusão de novos riscos e atualização das ações de mitigação.
