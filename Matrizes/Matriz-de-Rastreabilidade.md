# Matriz de Rastreabilidade

## Objetivo

A Matriz de Rastreabilidade estabelece a relação entre requisitos, casos de teste, execuções, evidências e registros de defeitos.

Seu objetivo é garantir que todas as funcionalidades importantes do sistema sejam testadas e que seja possível identificar rapidamente quais testes validam cada requisito.

---

## Fluxo de Rastreabilidade

```text
Requisito
     ↓
Caso de Teste
     ↓
Execução de Teste
     ↓
Evidência
     ↓
Bug (quando existir)
```

---

## Matriz

| Requisito | Funcionalidade    | Caso de Teste | Execução | Evidência | Bug | Status  |
|-----------|-------------------|---------------|----------|-----------|-----|---------|
| RF-001    | Login com Google  | CT-001        | ET-002   | EV-002    | N/A | ✅      |
| RF-002    | Dashboard         | CT-002        | —        | —         | —   | ⏳      |
| RF-003    | Drivers           | CT-003        | —        | —         | —   | ⏳      |
| RF-004    | Teams             | CT-004        | —        | —         | —   | ⏳      |
| RF-005    | Seasons           | CT-005        | —        | —         | —   | ⏳      |
| RF-006    | Calendar          | CT-006        | —        | —         | —   | ⏳      |
| RF-007    | Results           | CT-007        | —        | —         | —   | ⏳      |
| RF-008    | Notifications     | CT-008        | —        | —         | —   | ⏳      |
| RF-009    | Perfil do Usuário | CT-009        | —        | —         | —   | ⏳      |

---

## Legenda

| Símbolo | Significado |
|---------|-------------|

| ⏳ | Não iniciado |
| 🚧 | Em andamento |
| ✅ | Validado |
| ❌ | Reprovado |

---

## Atualização

A matriz deverá ser atualizada sempre que um novo requisito, caso de teste, execução ou defeito for criado.
