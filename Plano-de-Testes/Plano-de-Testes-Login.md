# Plano de Testes — Login

| Documento | PT-001 |
| ---------- | ------ |
| Projeto | SIM Racing Manager |
| Módulo | Autenticação |
| Responsável | Paulo Fernando Puppe Junior |
| Tipo de Documento | Plano de Testes |
| Versão | 1.1 |
| Ambiente | UAT |
| Status | Em andamento |
| Data de Criação | 2026-07-02 |
| Última Atualização | 2026-07-13 |

---

## Objetivo

Definir o planejamento, estratégia, escopo, critérios, riscos e abordagem para validação da funcionalidade de autenticação do sistema SIM Racing Manager.

Este documento serve como referência para toda a execução dos testes relacionados ao Login.

---

## Escopo

Este plano contempla os seguintes fluxos:

- Login tradicional
- Login utilizando Google OAuth
- Recuperação de senha
- Logout
- Validação de campos obrigatórios
- Mensagens de erro
- Segurança do processo de autenticação
- Bloqueio por tentativas inválidas

---

## Fora do Escopo

Não fazem parte desta versão:

- Cadastro de usuários
- Administração de contas
- Alteração de perfil
- Exclusão de usuários
- Configurações administrativas

---

## Objetivos da Qualidade

Garantir que:

- O usuário consiga autenticar-se corretamente.
- Não seja possível acessar o sistema sem autenticação.
- O sistema valide corretamente entradas inválidas.
- O fluxo Google OAuth funcione.
- O logout encerre completamente a sessão.
- Não existam vulnerabilidades básicas na autenticação.

---

## Referências

### Documentação

- LF-001 — Levantamento Funcional
- Backlog do Projeto
- Estratégia de Testes
- Critérios de Entrada e Saída

### Casos de Teste

- CT-001 ao CT-010

### Execuções

- ET-002

### Evidências

- EV-002

### Matrizes

- Matriz de Rastreabilidade
- Matriz de Riscos

---

## Ambiente de Testes

| Item | Valor |
| ---- | ----- |
| Ambiente | UAT |
| Sistema Operacional | Windows 10 |
| Navegador Principal | Google Chrome |
| Navegador Secundário | Microsoft Edge |
| Internet | Banda Larga |
| Banco de Dados | Ambiente UAT |
| Autenticação | Local + Google OAuth |

---

## Ferramentas Utilizadas

| Ferramenta | Finalidade |
| ---------- | ---------- |
| VS Code | Documentação |
| Git | Versionamento |
| GitHub | Repositório |
| Markdown | Documentação |
| Markdownlint | Padronização |
| Markdown Table Formatter | Formatação |
| Markdown All in One | Produtividade |
| Git Graph | Histórico Git |
| Draw.io | Diagramas |
| Trello | Planejamento |
| Jira | Simulação de gestão |
| Postman | API |
| Playwright | Automação (futuro) |

---

## Estratégia de Testes

Serão executados:

- Testes Funcionais
- Testes Negativos
- Testes Exploratórios
- Testes de Validação
- Testes de Segurança
- Testes de Regressão

---

## Critérios de Entrada

A execução somente poderá iniciar quando:

- Ambiente disponível.
- Sistema implantado.
- Casos de teste aprovados.
- Massa de testes preparada.
- Requisitos definidos.

---

## Critérios de Saída

Os testes serão considerados concluídos quando:

- Todos os casos críticos forem executados.
- Evidências anexadas.
- Bugs registrados.
- Rastreabilidade atualizada.
- Não existirem bugs bloqueantes.

---

## Massa de Testes

| Identificador | Descrição |
| ------------- | --------- |
| MT-001 | Conta Google válida |
| MT-002 | Usuário válido |
| MT-003 | Usuário inválido |
| MT-004 | Senha inválida |
| MT-005 | SQL Injection |

---

## Casos de Teste Cobertos

| Caso | Descrição |
| ---- | --------- |
| CT-001 | Login válido |
| CT-002 | Senha incorreta |
| CT-003 | Usuário inexistente |
| CT-004 | Campos vazios |
| CT-005 | SQL Injection |
| CT-006 | Senha em branco |
| CT-007 | Usuário em branco |
| CT-008 | Bloqueio por tentativas |
| CT-009 | Recuperação de senha |
| CT-010 | Logout |

---

## Riscos

| ID | Risco | Mitigação |
| -- | ------ | --------- |
| RK-001 | Ambiente indisponível | Validar antes da execução |
| RK-002 | Massa incorreta | Revisar dados |
| RK-003 | Bugs críticos | Regressão completa |
| RK-004 | Evidências ausentes | Checklist obrigatório |

---

## Critérios de Aprovação

Será considerado aprovado quando:

- 100% dos testes críticos aprovados.
- Sem bugs críticos.
- Sem bugs bloqueantes.
- Evidências registradas.
- Documentação atualizada.

---

## Rastreabilidade

| Artefato | Referência |
| --------- | ---------- |
| Levantamento Funcional | LF-001 |
| Backlog | QA-001 até QA-030 |
| Casos de Teste | CT-001 ao CT-010 |
| Execução | ET-002 |
| Evidências | EV-002 |
| Bugs | BUG-001 |
| Matriz de Rastreabilidade | Atualizada |
| Matriz de Riscos | Atualizada |

---

## Checklist do Plano

- [x] Objetivo definido
- [x] Escopo definido
- [x] Ambiente definido
- [x] Ferramentas definidas
- [x] Estratégia definida
- [x] Critérios definidos
- [x] Massa de testes definida
- [x] Casos vinculados
- [x] Riscos identificados
- [x] Rastreabilidade criada

---

## Próximos Passos

- Executar CT-001 ao CT-010.
- Atualizar ET-002.
- Registrar evidências.
- Abrir bugs quando necessário.
- Atualizar métricas.
- Preparar automação com Playwright.

---

## Histórico de Alterações

| Versão | Data | Autor | Alteração |
| ------- | ---- | ----- | --------- |
| 1.0 | 2026-07-02 | Paulo Fernando Puppe Junior | Criação do documento |
| 1.1 | 2026-07-13 | Paulo Fernando Puppe Junior | Refatoração completa, padronização corporativa, inclusão de rastreabilidade, critérios, checklist e estratégia de testes |
