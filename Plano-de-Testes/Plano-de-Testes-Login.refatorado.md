# Plano de Testes — Login (PT-001)

| Campo                   | Valor                                  |
|------------------------:|----------------------------------------|
| Projeto                 | SIM Racing Manager                     |
| Módulo                  | Autenticação / Login                   |
| Responsável             | Paulo Fernando Puppe Junior            |
| Identificador do Plano  | PT-001                                 |
| Versão                  | 1.1                                    |
| Ambiente                | UAT                                    |
| Status                  | Em andamento                           |
| Data de Criação         | 2026-07-02                             |
| Última Atualização      | 2026-07-13                             |

---

## 1. Objetivo

Definir o planejamento e os critérios para a execução dos testes da funcionalidade de autenticação (Login) do sistema SIM Racing Manager. O plano cobre fluxos de login local, login via Google (OAuth), recuperação de senha, logout, validações e controles de segurança.

---

## 2. Escopo

Inclui os seguintes fluxos e verificações:

- Login tradicional (usuário/senha)
- Login com Google (OAuth)
- Recuperação de senha (fluxo "Esqueci minha senha")
- Logout e encerramento de sessão
- Validações de campos obrigatórios e mensagens de erro
- Proteção contra ataques básicos (ex.: SQL injection)
- Bloqueio por tentativas inválidas

Fora do escopo desta versão: cadastro/alteração/exclusão de usuários e configurações administrativas.

---

## 3. Objetivos de Qualidade

Garantir que:

- Usuários válidos autentiquem com sucesso;
- Usuários inválidos não obtenham acesso;
- Mensagens e validações orientem corretamente o usuário;
- Fluxo OAuth funcione conforme esperado;
- Sessões são encerradas de forma segura;
- Não existam vulnerabilidades básicas relacionadas à autenticação.

---

## 4. Referências e Artefatos (links relativos mantidos)

- Plano: `../Plano-de-Testes/Plano-de-Testes-Login.md` (este documento)
- Levantamento Funcional: `../Documentacao/Levantamento-Funcional.md`
- Estratégia de Testes: `../Planejamento/Estrategia-de-Testes.md`
- Casos de Teste: `../Casos-de-Teste/Login-Casos-de-Teste.md`
- Massa de Testes: `../Massa-de-Testes/MT-001-Contas-Google.md`
- Execuções: `../Execucao-de-Testes/ET-002-Login-Google-Valido.md`
- Evidências: `../Evidencias/ET-002-Login-Google-Valido/`
- Bugs: `../Relatorios-de-Bugs/BUG-001-Login.md`
- Matrizes: `../Matrizes/Matriz-de-Rastreabilidade.md`, `../Matrizes/Matriz-de-Riscos.md`

---

## 5. Ambiente de Testes

| Item                  | Valor                 |
|----------------------:|-----------------------|
| Ambiente               | UAT                   |
| Sistema Operacional    | Windows 11            |
| Navegador Principal    | Google Chrome         |
| Navegador Secundário   | Microsoft Edge        |
| Conexão                | Internet banda larga  |
| Banco de Dados         | Ambiente UAT          |
| Autenticação           | Local + Google OAuth  |

---

## 6. Ferramentas

- VS Code, Git, GitHub, Markdown, Markdownlint (sugestão), Draw.io, Trello/Jira (planejamento), Postman (APIs), Playwright (automação - futuro).

---

## 7. Estratégia de Testes

Tipos de testes priorizados:

- Funcionais (fluxos críticos)
- Negativos (validações)
- Segurança básica (SQLi, bloqueio de conta)
- Regressão (fluxos críticos por release)
- Exploratórios (quando houver mudanças relevantes)

Priorização: CTs críticos com prioridade Alta (ex.: autenticação, bloqueio, OAuth) executados em primeiro lugar.

---

## 8. Critérios de Entrada e Saída

Critérios de entrada (execução inicia quando):

- Ambiente UAT disponível e estável;
- Versão da aplicação implantada;
- Casos de teste revisados e massa de testes preparada;
- Requisitos e critérios de aceite definidos.

Critérios de saída (teste concluído quando):

- Casos críticos executados e evidenciados;
- Rastreabilidade atualizada;
- Todos os bugs bloqueantes corrigidos ou sinalizados com plano de ação;
- Relatório de execução entregue.

---

## 9. Massa de Testes

| ID     | Descrição                        |
|:-------|:---------------------------------|
| MT-001 | Conta Google válida              |
| MT-002 | Usuário válido                   |
| MT-003 | Usuário inválido                 |
| MT-004 | Senha inválida                   |
| MT-005 | Payloads de segurança (ex.: SQLi)|

---

## 10. Casos de Teste (sumário)

Tabela de cobertura dos casos definidos (IDs mantidos):

| Caso   | Descrição                    | Prioridade | Referência | Execução / Evidência |
|:-------|:-----------------------------|:----------:|:----------:|:---------------------|
| CT-001 | Login válido                 | Alta       | `Login-Casos-de-Teste.md` | — |
| CT-002 | Senha incorreta              | Alta       | `Login-Casos-de-Teste.md` | `BUG-001` |
| CT-003 | Usuário inexistente          | Alta       | `Login-Casos-de-Teste.md` | — |
| CT-004 | Campos vazios                | Alta       | `Login-Casos-de-Teste.md` | — |
| CT-005 | SQL Injection                | Alta       | `Login-Casos-de-Teste.md` | — |
| CT-006 | Senha em branco              | Média      | `Login-Casos-de-Teste.md` | — |
| CT-007 | Usuário em branco            | Média      | `Login-Casos-de-Teste.md` | — |
| CT-008 | Bloqueio por tentativas      | Alta       | `Login-Casos-de-Teste.md` | — |
| CT-009 | Recuperação de senha         | Alta       | `Login-Casos-de-Teste.md` | — |
| CT-010 | Logout                       | Alta       | `Login-Casos-de-Teste.md` | — |
| CT-011 | Login com Google             | Alta       | `Login-Casos-de-Teste.md` | `ET-002` / evidências: `../Evidencias/ET-002-Login-Google-Valido/` |

---

## 11. Riscos e Mitigações

| ID    | Risco                       | Mitigação                                |
|:------|:----------------------------|:------------------------------------------|
| RK-001| Ambiente indisponível       | Validar disponibilidade antes da execução |
| RK-002| Massa de testes incorreta  | Revisar e versionar dados de teste        |
| RK-003| Bugs críticos              | Priorizar correção e regressão completa   |
| RK-004| Evidências ausentes        | Checklist obrigatório por execução        |

---

## 12. Critérios de Aprovação

- Casos críticos aprovados ou mitigados;
- Sem bugs bloqueantes sem tratamento;
- Evidências anexadas e rastreáveis;
- Matrizes e documentação atualizadas.

---

## 13. Rastreabilidade (mapeamento simplificado)

- Requisito fonte: `../Documentacao/Levantamento-Funcional.md` (autenticação / login).
- Execuções/evidências conhecidas: `../Execucao-de-Testes/ET-002-Login-Google-Valido.md` / `../Evidencias/ET-002-Login-Google-Valido/`.
- Defeito documentado: `../Relatorios-de-Bugs/BUG-001-Login.md` (relacionado a CT-002).

Observação: para auditoria/portfólio, manter Matriz de Rastreabilidade detalhada em `Matrizes/Matriz-de-Rastreabilidade.md` com vínculo requisito → CT → ET → evidência → bug.

---

## 14. Checklist de Execução (modelo)

- [ ] Validar ambiente UAT;
- [ ] Carregar e validar massa de testes (MT-001..MT-005);
- [ ] Executar CTs críticos (CT-001, CT-002, CT-008, CT-011, CT-010);
- [ ] Salvar evidências em `Evidencias/` e registrar execução em `Execucao-de-Testes/`;
- [ ] Reportar bugs com passos e evidências;
- [ ] Atualizar matrizes.

---

## 15. Próximos Passos

- Executar os casos críticos e anexar evidências;
- Preencher Matriz de Rastreabilidade com vínculos completos;
- Planejar automação dos fluxos críticos e integração CI;
- Definir métricas de qualidade (taxa de passagem, defeitos por execução).

---

## 16. Histórico de Alterações

| Versão | Data       | Autor                       | Alteração                                    |
|:------:|:----------:|:---------------------------|:---------------------------------------------|
| 1.0    | 2026-07-02 | Paulo Fernando Puppe Junior | Criação do documento                          |
| 1.1    | 2026-07-13 | Paulo Fernando Puppe Junior | Refatoração e padronização                    |

---
