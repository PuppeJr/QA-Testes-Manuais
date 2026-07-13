# Plano de Testes

## Objetivo

Definir a estratégia, o escopo, os critérios e os recursos necessários para validar a funcionalidade de autenticação do sistema.

---

## Informações Gerais

| Campo              | Valor                       |
|--------------------|-----------------------------|
| Documento          | PT-001                      |
| Projeto            | QA-Testes-Manuais           |
| Funcionalidade     | Login                       |
| Versão             | 1.1                         |
| Responsável        | Paulo Fernando Puppe Junior |
| Ambiente           | UAT                         |
| Última Atualização | 13/07/2026                  |

---

## Escopo

Este plano contempla os testes relacionados ao processo de autenticação do sistema.

Serão validados:

- Login com Google
- Login por usuário e senha
- Logout
- Recuperação de senha
- Validação dos campos obrigatórios
- Segurança da autenticação

---

## Objetivos dos Testes

- Garantir autenticação correta.
- Garantir segurança do login.
- Validar mensagens de erro.
- Garantir funcionamento do logout.
- Validar recuperação de senha.

---

## Tipos de Testes

| Tipo          | Aplicação |
|---------------|-----------|
| Funcional     | ✔         |
| Regressão     | ✔         |
| Exploratórios | ✔         |
| Segurança     | ✔         |
| Usabilidade   | ✔         |

---

## Critérios de Entrada

- Ambiente disponível.
- Sistema implantado.
- Massa de testes preparada.
- Conta Google válida.
- Usuário cadastrado.

---

## Critérios de Saída

- Todos os casos críticos executados.
- Evidências registradas.
- Bugs documentados.
- Casos atualizados.
- Aprovação para homologação.

---

## Massa de Testes

| Item             | Situação |
|------------------|----------|
| Usuário válido   | ✔        |
| Usuário inválido | ✔        |
| Senha inválida   | ✔        |
| Conta Google     | ✔        |

---

## Artefatos Relacionados

### Documento de Origem

- LF-001 — Levantamento Funcional

### Casos de Teste

- CT-001 ao CT-010

### Execuções

- ET-002

### Evidências

- EV-002

### Matrizes

- Matriz de Rastreabilidade
- Matriz de Riscos

### Sprint

- Sprint 03

---

## Histórico de Alterações

| Data       | Versão | Responsável                 | Alteração            |
|------------|--------|-----------------------------|----------------------|
| 05/06/2026 | 1.0    | Paulo Fernando Puppe Junior | Criação              |
| 13/07/2026 | 1.1    | Paulo Fernando Puppe Junior | Refatoração completa |

---

## Revisão

Este plano deverá ser revisado sempre que houver alteração significativa na funcionalidade de Login.
