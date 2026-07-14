# Massa de Testes — MT-001 — Conta Google Válida

## Informações Gerais

| Campo              | Valor                       |
|--------------------|-----------------------------|
| Identificador      | MT-001                      |
| Projeto            | SIM Racing Manager          |
| Módulo             | Login                       |
| Funcionalidade     | Login com Google            |
| Tipo               | Dados Positivos             |
| Ambiente           | UAT                         |
| Responsável        | Paulo Fernando Puppe Junior |
| Status             | Aprovado                    |
| Data de Criação    | 2026-07-02                  |
| Última Atualização | 2026-07-14                  |

---

## Objetivo

Disponibilizar os dados necessários para execução dos testes relacionados ao Login utilizando autenticação Google.

---

## Escopo

Esta massa de testes é utilizada na validação dos seguintes fluxos:

- Login utilizando Google OAuth
- Recuperação de sessão autenticada
- Validação de autenticação com conta Google válida

Não deve ser utilizada para testes de login tradicional, logout ou cenários negativos.

---

## Dados de Teste

| Campo         | Valor                        |
|---------------|------------------------------|
| Identificador | `MT-001`                     |
| Usuário       | `qa_google_001`              |
| E-mail        | `qa_google_001@example.test` |
| Perfil        | Usuário                      |
| Status        | Ativo                        |
| Ambiente      | UAT                          |

---

## Pré-condições

- Conta Google previamente cadastrada.
- Conta ativa.
- Serviço Google OAuth disponível.
- Ambiente UAT disponível.

---

## Pós-condições

- Usuário autenticado durante a execução do teste.
- Nenhuma alteração permanente na conta utilizada.

---

## Rastreabilidade

| Artefato        | Referência |
|-----------------|------------|
| Requisito       | RF-001     |
| Plano de Testes | PT-001     |
| Caso de Teste   | CT-011     |
| Execução        | ET-002     |
| Evidência       | EV-002     |
| Bug             | Nenhum     |

---

## Observações

- Esta conta deve ser utilizada exclusivamente no ambiente UAT.
- Não alterar senha, e-mail ou perfil durante a execução.
- Não excluir a conta.
- Utilizar apenas para testes relacionados ao Login Google.

---

## Histórico de Alterações

| Versão | Data       | Autor                       | Descrição            |
|--------|------------|-----------------------------|----------------------|
| 1.0    | 2026-07-14 | Paulo Fernando Puppe Junior | Criação do documento |
