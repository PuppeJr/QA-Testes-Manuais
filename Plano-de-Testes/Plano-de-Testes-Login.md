# Plano de Testes — Login

| Documento          | PT-001                      |
| ------------------ | --------------------------- |
| Projeto            | SIM Racing Manager          |
| Módulo             | Autenticação                |
| Responsável        | Paulo Fernando Puppe Junior |
| Tipo de Documento  | Plano de Testes             |
| Versão             | 1.1                         |
| Ambiente           | UAT                         |
| Status             | Em andamento                |
| Data de Criação    | 2026-07-02                  |
| Última Atualização | 2026-07-13                  |

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

- Levantamento Funcional: ../Documentacao/Levantamento-Funcional.md
- Critérios de Entrada e Saída: ../Documentacao/Criterios-de-Entrada-e-Saida.md
- Mapa do Sistema: ../Documentacao/Mapa-do-Sistema.md

### Planejamento

- Backlog do Projeto: ../Planejamento/Backlog-do-Projeto.md
- Estratégia de Testes: ../Planejamento/Estrategia-de-Testes.md
- Cronograma: ../Planejamento/Cronograma.md

### Casos de Teste

- Login: ../Casos-de-Teste/Login-Casos-de-Teste.md

### Execuções / Evidências

- Execução: ../Execucao-de-Testes/ET-002-Login-Google-Valido.md
- Evidências: ../Evidencias/ET-002-Login-Google-Valido/

### Matrizes

- Matriz de Rastreabilidade: ../Matrizes/Matriz-de-Rastreabilidade.md
- Matriz de Riscos: ../Matrizes/Matriz-de-Riscos.md

---

## Ambiente de Testes

| Item                 | Valor                |
| -------------------- | -------------------- |
| Ambiente             | UAT                  |
| Sistema Operacional  | Windows 11           |
| Navegador Principal  | Google Chrome        |
| Navegador Secundário | Microsoft Edge       |
| Internet             | Banda Larga          |
| Banco de Dados       | Ambiente UAT         |
| Autenticação         | Local + Google OAuth |

---

## Ferramentas Utilizadas

| Ferramenta               | Finalidade          |
| ------------------------ | ------------------- |
| VS Code                  | Documentação        |
| Git                      | Versionamento       |
| GitHub                   | Repositório         |
| Markdown                 | Documentação        |
| Markdownlint             | Padronização        |
| Draw.io                  | Diagramas           |
| Trello                   | Planejamento        |
| Postman                  | API                 |
| Playwright               | Automação (planejado)|

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
- Sistema implantado na versão a ser validada.
- Casos de teste revisados e aprovados.
- Massa de testes preparada.
- Requisitos e critérios de aceite definidos.

---

## Critérios de Saída

Os testes serão considerados concluídos quando:

- Todos os casos críticos forem executados.
- Evidências das execuções estiverem anexadas.
- Bugs relevantes forem registrados com evidências.
- Rastreabilidade atualizada.
- Não existirem bugs bloqueantes abertos.

---

## Massa de Testes

| Identificador | Descrição           |
| ------------- | ------------------- |
| MT-001        | Conta Google válida |
| MT-002        | Usuário válido      |
| MT-003        | Usuário inválido    |
| MT-004        | Senha inválida      |
| MT-005        | Payloads de segurança (ex: SQLi) |

---

## Casos de Teste Cobertos

| Caso   | Descrição               |
| ------ | ----------------------- |
| CT-001 | Login válido            |
| CT-002 | Senha incorreta         |
| CT-003 | Usuário inexistente     |
| CT-004 | Campos vazios           |
| CT-005 | SQL Injection           |
| CT-006 | Senha em branco         |
| CT-007 | Usuário em branco       |
| CT-008 | Bloqueio por tentativas |
| CT-009 | Recuperação de senha    |
| CT-010 | Logout                  |
| CT-011 | Login com Google        |

---

## Riscos

| ID     | Risco                 | Mitigação                 |
| ------ | --------------------- | ------------------------- |
| RK-001 | Ambiente indisponível | Validar disponibilidade antes da execução |
| RK-002 | Massa incorreta       | Revisar e versionar dados de teste |
| RK-003 | Bugs críticos         | Definir plano de rollback e comunicação |
| RK-004 | Evidências ausentes   | Checklist obrigatório para cada execução |

---

## Critérios de Aprovação

Será considerado aprovado quando:

- Todos os testes críticos aprovados.
- Sem bugs críticos ou bloqueantes abertos.
- Evidências registradas e anexadas.
- Documentação atualizada.

---

## Rastreabilidade

| Artefato                  | Referência        |
| ------------------------- | ----------------- |
| Levantamento Funcional    | ../Documentacao/Levantamento-Funcional.md |
| Backlog                   | ../Planejamento/Backlog-do-Projeto.md |
| Casos de Teste            | ../Casos-de-Teste/Login-Casos-de-Teste.md |
| Execução                  | ../Execucao-de-Testes/ET-002-Login-Google-Valido.md |
| Evidências                | ../Evidencias/ET-002-Login-Google-Valido/ |
| Bugs                      | ../Relatorios-de-Bugs/BUG-001-Login.md |
| Matrizes                  | ../Matrizes/ |

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

- Executar CT-001 ao CT-011 prioritariamente.
- Atualizar execuções (ET-002 e demais) com evidências.
- Registrar bugs com evidências e atribuir responsáveis.
- Definir métricas (taxa de passagem, defeitos por execução).
- Planejar automação dos fluxos críticos (Playwright).

---

## Histórico de Alterações

| Versão | Data       | Autor                       | Alteração                                                                                                                |
| ------ | ---------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| 1.0    | 2026-07-02 | Paulo Fernando Puppe Junior | Criação do documento                                                                                                     |
| 1.1    | 2026-07-13 | Paulo Fernando Puppe Junior | Refatoração, padronização e links relativos corrigidos                                                                   |
