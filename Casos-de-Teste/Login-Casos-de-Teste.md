# Casos de Teste - Login

** CT-001 - Login com usuário e senha válidos

*** Objetivo

Validar acesso ao sistema com credenciais corretas.

*** Pré-condição

Usuário cadastrado.

*** Passos

1. Abrir tela de login.
2. Informar usuário válido.
3. Informar senha válida.
4. Clicar em Entrar.

*** Resultado Esperado

Sistema permite acesso e direciona para a página inicial.

*** Prioridade

Alta

---

** CT-002 - Login com senha incorreta

*** Objetivo

Validar mensagem de erro para senha inválida.

*** Pré-condição

Usuário cadastrado.

*** Passos

1. Informar usuário válido.
2. Informar senha incorreta.
3. Clicar em Entrar.

*** Resultado Esperado

Sistema exibe mensagem de erro.

*** Prioridade

Alta
** CT-003 - Login com usuário inexistente

*** Objetivo

Validar comportamento do sistema para usuário não cadastrado.

*** Pré-condição

Usuário não cadastrado.

*** Passos

1. Informar usuário inexistente.
2. Informar uma senha qualquer.
3. Clicar em Entrar.

*** Resultado Esperado

Sistema exibe mensagem de credenciais inválidas.

*** Prioridade

Alta

---

** CT-004 - Login com campos vazios

*** Objetivo

Validar obrigatoriedade dos campos.

*** Pré-condição

Tela de login aberta.

*** Passos

1. Deixar usuário vazio.
2. Deixar senha vazia.
3. Clicar em Entrar.

*** Resultado Esperado

Sistema solicita preenchimento dos campos obrigatórios.

*** Prioridade

Alta

---

** CT-005 - Login com SQL Injection

*** Objetivo

Validar proteção contra entradas maliciosas.

*** Passos

1. Informar:
   ' OR '1'='1
2. Clicar em Entrar.

*** Resultado Esperado

Sistema rejeita a entrada e mantém a segurança da aplicação.

*** Prioridade

Alta

---

** CT-006 - Login com senha em branco

*** Objetivo

Validar comportamento quando apenas a senha não é informada.

*** Resultado Esperado

Sistema solicita preenchimento da senha.

*** Prioridade

Média

---

** CT-007 - Login com usuário em branco

*** Objetivo

Validar comportamento quando apenas o usuário não é informado.

*** Resultado Esperado

Sistema solicita preenchimento do usuário.

*** Prioridade

Média

---

** CT-008 - Bloqueio após múltiplas tentativas inválidas

*** Objetivo

Validar mecanismo de segurança.

*** Resultado Esperado

Conta bloqueada após quantidade definida de tentativas.

*** Prioridade

Alta

---

** CT-009 - Recuperação de senha

*** Objetivo

Validar fluxo de recuperação de senha.

*** Resultado Esperado

Sistema envia instruções para redefinição.

*** Prioridade

Alta

---

** CT-010 - Logout do sistema

*** Objetivo

Validar encerramento da sessão do usuário.

*** Resultado Esperado

Usuário retorna para tela de login.

*** Prioridade

Alta
