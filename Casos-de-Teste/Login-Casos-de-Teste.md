# Casos de Teste — Login

## Informações Gerais

| Campo               | Valor                            |
| ------------------- | -------------------------------- |
| Projeto             | SIM Racing Manager               |
| Módulo              | Autenticação / Login             |
| Responsável         | Paulo Fernando Puppe Junior      |
| Identificador do Plano | PT-001                        |
| Ambiente            | UAT                              |
| Última Atualização  | 2026-07-13                       |

---

## Objetivo

Consolidar e executar os casos de teste relacionados ao processo de autenticação: login com credenciais locais, login via Google, fluxos de recuperação e segurança. Manter rastreabilidade, IDs e links para permitir auditoria e automação futura.

---

## Referências

- Plano de Testes: `../Plano-de-Testes/Plano-de-Testes-Login.md`
- Massa de Testes: `../Massa-de-Testes/MT-001-Contas-Google.md`
- Evidências: `../Evidencias/ET-002-Login-Google-Valido/`
- Relatórios de Bug: `../Relatorios-de-Bugs/BUG-001-Login.md`

---

## Convenções

- Status: `Não Executado` / `Executado (Passou)` / `Executado (Falhou)` / `Bloqueado`
- Evidência: caminho relativo para arquivos na pasta `Evidencias/`
- IDs: manter o identificador único `CT-###` em cada caso para rastreabilidade.

---

## Casos de Teste

### CT-001 — Login com usuário e senha válidos
**Tipo:** Funcional  
**Prioridade:** Alta  
**Pré-condições:** Usuário cadastrado; sistema disponível.  
**Massa:** `usuario.teste` / `Senha@123`  
**Passos:**
1. Acessar a tela de Login.
2. Informar usuário e senha válidos.
3. Clicar em **Entrar**.
**Resultado esperado:** Autenticação bem-sucedida e redirecionamento ao Dashboard.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-002 — Login com senha incorreta
**Tipo:** Negativo  
**Prioridade:** Alta  
**Pré-condições:** Usuário cadastrado.  
**Massa:** `usuario.teste` / `senhaErrada123`  
**Passos:**
1. Informar usuário válido.
2. Informar senha incorreta.
3. Clicar em **Entrar**.
**Resultado esperado:** Mensagem de credenciais inválidas.  
**Status:** Executado (Falhou)  
**Observação:** defeito registrado como `BUG-001` (não exibe mensagem de erro).  
**Evidência:** `../Relatorios-de-Bugs/BUG-001-Login.md`

---

### CT-003 — Login com usuário inexistente
**Tipo:** Negativo  
**Prioridade:** Alta  
**Pré-condições:** Nenhuma.  
**Massa:** `usuario.inexistente` / `Senha@123`  
**Passos:**
1. Informar usuário inexistente.
2. Informar qualquer senha.
3. Clicar em **Entrar**.
**Resultado esperado:** Sistema informa que credenciais são inválidas.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-004 — Login com campos vazios
**Tipo:** Validação  
**Prioridade:** Alta  
**Pré-condições:** Tela de Login aberta.  
**Passos:**
1. Deixar usuário e/ou senha vazios.
2. Clicar em **Entrar**.
**Resultado esperado:** Validação e mensagens indicando campos obrigatórios.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-005 — Proteção contra SQL Injection
**Tipo:** Segurança  
**Prioridade:** Alta  
**Massa:**
```
' OR '1'='1
```
**Passos:**
1. Informar payload no campo usuário.
2. Informar qualquer senha.
3. Clicar em **Entrar**.
**Resultado esperado:** Rejeição sem execução de comandos SQL.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-006 — Login com senha em branco
**Tipo:** Validação  
**Prioridade:** Média  
**Pré-condições:** Usuário cadastrado.  
**Passos:**
1. Informar usuário.
2. Deixar senha em branco.
3. Clicar em **Entrar**.
**Resultado esperado:** Sistema solicita preenchimento da senha.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-007 — Login com usuário em branco
**Tipo:** Validação  
**Prioridade:** Média  
**Pré-condições:** Tela de Login aberta.  
**Passos:**
1. Deixar usuário em branco.
2. Informar senha válida.
3. Clicar em **Entrar**.
**Resultado esperado:** Sistema solicita preenchimento do usuário.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-008 — Bloqueio após múltiplas tentativas inválidas
**Tipo:** Segurança  
**Prioridade:** Alta  
**Pré-condições:** Usuário cadastrado.  
**Passos:**
1. Errar a senha 5 vezes consecutivas.
2. Tentar login novamente.
**Resultado esperado:** Conta bloqueada conforme regra de negócio.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-009 — Recuperação de senha
**Tipo:** Funcional  
**Prioridade:** Alta  
**Pré-condições:** Usuário cadastrado.  
**Passos:**
1. Clicar em "Esqueci minha senha".
2. Informar e-mail cadastrado.
3. Confirmar solicitação.
**Resultado esperado:** Envio de instruções para redefinição por e-mail.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-010 — Logout
**Tipo:** Funcional  
**Prioridade:** Alta  
**Pré-condições:** Usuário autenticado.  
**Passos:**
1. Clicar em **Logout**.
**Resultado esperado:** Sessão encerrada e redirecionamento para Login.  
**Status:** Não Executado  
**Evidência:** —

---

### CT-011 — Login com Google (conta válida)
**Tipo:** Funcional  
**Prioridade:** Alta  
**Pré-condições:** Conta Google válida disponível (ver `../Massa-de-Testes/MT-001-Contas-Google.md`).  
**Passos:**
1. Na tela de Login, clicar em "Entrar com Google".
2. Selecionar conta Google válida.
3. Concluir autenticação e verificar redirecionamento ao Dashboard.
**Resultado esperado:** Autenticação via Google concluída e Dashboard exibido com usuário autenticado.  
**Status:** Executado (Passou)  
**Evidências:**
- `../Evidencias/ET-002-Login-Google-Valido/ET-002-01-Tela-Login.png`
- `../Evidencias/ET-002-Login-Google-Valido/ET-002-02-Selecao-Conta-Google.png`
- `../Evidencias/ET-002-Login-Google-Valido/ET-002-03-Dashboard.png`
- `../Evidencias/ET-002-Login-Google-Valido/ET-002-04-Perfil-Usuario.png`

---

## Rastreabilidade (simples)

| Caso   | Fonte de Requisito / Referência |
| ------ | ------------------------------ |
| CT-001 | `../Documentacao/Levantamento-Funcional.md` (Login) |
| CT-002 | `../Documentacao/Levantamento-Funcional.md` (Login) |
| CT-003 | `../Documentacao/Levantamento-Funcional.md` (Login) |
| CT-004 | `../Documentacao/Levantamento-Funcional.md` (Validações) |
| CT-005 | `../Documentacao/Levantamento-Funcional.md` (Segurança) |
| CT-006 | `../Documentacao/Levantamento-Funcional.md` (Validações) |
| CT-007 | `../Documentacao/Levantamento-Funcional.md` (Validações) |
| CT-008 | `../Documentacao/Levantamento-Funcional.md` (Segurança) |
| CT-009 | `../Documentacao/Levantamento-Funcional.md` (Recuperação de senha) |
| CT-010 | `../Documentacao/Levantamento-Funcional.md` (Logout) |
| CT-011 | `../Documentacao/Levantamento-Funcional.md` (OAuth / Google) |

---

## Observações e próximos passos

- Atualizar status e anexar evidências após cada execução.
- Vincular cada execução a uma entrada de Execução (`ET-xxx`) com evidências e capturas.  
- Criar checklist de regressão mínima: CT-001, CT-002, CT-008, CT-011, CT-010.
- Priorizar automação dos fluxos críticos e integrar com CI.

---

## Histórico de alterações

- 2026-07-13 — Refatorado e completado por Paulo Fernando Puppe Junior
