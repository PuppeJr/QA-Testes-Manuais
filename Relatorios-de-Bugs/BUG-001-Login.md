# BUG-001 - Mensagem de erro não exibida após senha inválida

## Identificação

- **ID:** BUG-001
- **Título:** Sistema não exibe mensagem de erro para senha incorreta.
- **Módulo:** Login
- **Severidade:** Média
- **Prioridade:** Alta
- **Status:** Aberto

---

## Ambiente

- **Navegador:** Google Chrome
- **Sistema Operacional:** Windows 11
- **Versão da Aplicação:** 1.0

---

## Pré-condições

- Usuário previamente cadastrado.
- Sistema disponível para autenticação.

---

## Passos para Reproduzir

1. Acessar a tela de login.
2. Informar um usuário válido.
3. Informar uma senha incorreta.
4. Clicar no botão **Entrar**.

---

## Resultado Atual

O sistema permanece na tela de login sem exibir nenhuma mensagem de erro ao usuário.

---

## Resultado Esperado

O sistema deve impedir a autenticação e exibir uma mensagem informando que o usuário ou a senha são inválidos.

---

## Impacto

A ausência da mensagem de erro dificulta o entendimento do problema pelo usuário, podendo gerar tentativas repetidas de login e aumento no volume de chamados ao suporte.

---

## Evidências

- Captura de tela da execução (quando disponível).
- Vídeo da reprodução do defeito (opcional).

---

## Observações

O comportamento foi identificado durante a execução do caso de teste **CT-002 – Login com senha incorreta**.

---

## Responsável pela Identificação

Paulo Fernando Puppe Junior

---

## Data da Identificação

05/06/2026
