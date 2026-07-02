# Casos de Teste - Login

Este documento contém os casos de teste funcionais para validação da funcionalidade de autenticação do sistema.

---

## CT-001 - Login com usuário e senha válidos

- **Objetivo:** Validar que um usuário cadastrado consegue acessar o sistema utilizando credenciais válidas.

- **Tipo de Teste:** Funcional

- **Prioridade:** Alta

- **Pré-condições:**
  - Usuário previamente cadastrado.
  - Sistema disponível.

- **Massa de Teste:**
  - Usuário: `usuario.teste`
  - Senha: `Senha@123`

- **Passos:**
  1. Acessar a tela de Login.
  2. Informar usuário válido.
  3. Informar senha válida.
  4. Clicar em **Entrar**.

- **Resultado Esperado:**
  O sistema autentica o usuário e redireciona para a página inicial.

- **Status:** Não Executado

---

## CT-002 - Login com senha incorreta

- **Objetivo:** Validar que o sistema impede login utilizando senha incorreta.

- **Tipo de Teste:** Negativo

- **Prioridade:** Alta

- **Pré-condições:**
  - Usuário cadastrado.

- **Massa de Teste:**
  - Usuário: `usuario.teste`
  - Senha: `senhaErrada123`

- **Passos:**
  1. Informar usuário válido.
  2. Informar senha incorreta.
  3. Clicar em Entrar.

- **Resultado Esperado:**
  O sistema apresenta mensagem de credenciais inválidas.

- **Status:** Não Executado

---

## CT-003 - Login com usuário inexistente

- **Objetivo:** Validar comportamento para usuário não cadastrado.

- **Tipo de Teste:** Negativo

- **Prioridade:** Alta

- **Pré-condições:**
  - Usuário inexistente.

- **Massa de Teste:**
  - Usuário: `usuario.inexistente`
  - Senha: `Senha@123`

- **Passos:**
  1. Informar usuário inexistente.
  2. Informar uma senha qualquer.
  3. Clicar em Entrar.

- **Resultado Esperado:**
  O sistema informa que as credenciais são inválidas.

- **Status:** Não Executado

---

## CT-004 - Login com campos vazios

- **Objetivo:** Validar obrigatoriedade do preenchimento dos campos.

- **Tipo de Teste:** Validação

- **Prioridade:** Alta

- **Pré-condições:**
  - Tela de Login aberta.

- **Passos:**
  1. Deixar o campo usuário vazio.
  2. Deixar o campo senha vazio.
  3. Clicar em Entrar.

- **Resultado Esperado:**
  O sistema solicita o preenchimento dos campos obrigatórios.

- **Status:** Não Executado

---

## CT-005 - Login com SQL Injection

- **Objetivo:** Validar proteção contra SQL Injection.

- **Tipo de Teste:** Segurança

- **Prioridade:** Alta

- **Massa de Teste:**

```text
' OR '1'='1
```

- **Passos:**
  1. Informar a expressão acima no campo usuário.
  2. Informar qualquer senha.
  3. Clicar em Entrar.

- **Resultado Esperado:**
  O sistema rejeita a tentativa de autenticação sem executar comandos SQL indevidos.

- **Status:** Não Executado

---

## CT-006 - Login com senha em branco

- **Objetivo:** Validar comportamento quando apenas a senha não é informada.

- **Tipo de Teste:** Validação

- **Prioridade:** Média

- **Pré-condições:**
  - Usuário cadastrado.

- **Passos:**
  1. Informar usuário válido.
  2. Deixar a senha em branco.
  3. Clicar em Entrar.

- **Resultado Esperado:**
  O sistema solicita o preenchimento da senha.

- **Status:** Não Executado

---

## CT-007 - Login com usuário em branco

- **Objetivo:** Validar comportamento quando apenas o usuário não é informado.

- **Tipo de Teste:** Validação

- **Prioridade:** Média

- **Pré-condições:**
  - Tela de Login aberta.

- **Passos:**
  1. Deixar o campo usuário vazio.
  2. Informar uma senha válida.
  3. Clicar em Entrar.

- **Resultado Esperado:**
  O sistema solicita o preenchimento do usuário.

- **Status:** Não Executado

---

## CT-008 - Bloqueio após múltiplas tentativas inválidas

- **Objetivo:** Validar o bloqueio da conta após sucessivas tentativas inválidas.

- **Tipo de Teste:** Segurança

- **Prioridade:** Alta

- **Pré-condições:**
  - Usuário cadastrado.

- **Passos:**
  1. Informar senha incorreta cinco vezes consecutivas.
  2. Tentar novo login.

- **Resultado Esperado:**
  A conta é bloqueada conforme a regra de negócio.

- **Status:** Não Executado

---

## CT-009 - Recuperação de senha

- **Objetivo:** Validar o fluxo de recuperação de senha.

- **Tipo de Teste:** Funcional

- **Prioridade:** Alta

- **Pré-condições:**
  - Usuário cadastrado.

- **Passos:**
  1. Clicar em **Esqueci minha senha**.
  2. Informar o e-mail cadastrado.
  3. Confirmar a solicitação.

- **Resultado Esperado:**
  O sistema envia as instruções para redefinição da senha.

- **Status:** Não Executado

---

## CT-010 - Logout

- **Objetivo:** Validar o encerramento seguro da sessão.

- **Tipo de Teste:** Funcional

- **Prioridade:** Alta

- **Pré-condições:**
  - Usuário autenticado no sistema.

- **Passos:**
  1. Estar autenticado.
  2. Clicar em **Logout**.

- **Resultado Esperado:**
  O sistema encerra a sessão e retorna para a tela de Login.

- **Status:** Não Executado
