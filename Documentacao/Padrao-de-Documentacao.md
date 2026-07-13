# Padrão de Documentação

## Objetivo

Este documento define os padrões adotados no projeto **QA-Testes-Manuais** para garantir organização, padronização, rastreabilidade e facilidade de manutenção da documentação.

---

## Estrutura dos Documentos

Todos os documentos deverão seguir, sempre que aplicável, a seguinte estrutura:

1. Título
2. Objetivo
3. Informações Gerais
4. Artefatos Relacionados
5. Conteúdo Principal
6. Histórico de Alterações
7. Revisão

---

## Convenção de Identificadores

| Artefato                | Prefixo | Exemplo |
|-------------------------|---------|---------|
| Requisito Funcional     | RF      | RF-001  |
| Requisito Não Funcional | RNF     | RNF-001 |
| Plano de Testes         | PT      | PT-001  |
| Caso de Teste           | CT      | CT-001  |
| Execução de Teste       | ET      | ET-001  |
| Evidência               | EV      | EV-001  |
| Bug                     | BUG     | BUG-001 |
| Sprint                  | SPR     | SPR-001 |
| Release                 | REL     | REL-001 |
| Risco                   | RK      | RK-001  |
| Backlog                 | QA      | QA-001  |
| Documento               | DOC     | DOC-001 |

---

## Versionamento

Cada documento deverá possuir versão.

Exemplo:

| Versão | Alteração   |
|--------|-------------|
| 1.0    | Criação     |
| 1.1    | Correções   |
| 2.0    | Refatoração |

---

## Histórico de Alterações

Sempre que um documento sofrer alterações relevantes deverá possuir um histórico.

Exemplo:

| Data       | Versão | Responsável                 | Descrição            |
|------------|--------|-----------------------------|----------------------|
| 12/07/2026 | 1.0    | Paulo Fernando Puppe Junior | Criação do documento |

---

## Artefatos Relacionados

Sempre que possível, os documentos deverão referenciar outros artefatos do projeto.

Exemplo:

- Plano de Testes
- Casos de Teste
- Execuções
- Evidências
- Bugs
- Matrizes
- Sprints

---

## Convenção dos Arquivos

Os nomes dos arquivos deverão utilizar:

- Letras
- Hífen (-)
- Sem espaços
- Sem caracteres especiais

Exemplo:

Plano-de-Testes-Login.md

---

## Markdown

Todos os documentos deverão seguir:

- Apenas um título H1 (#)
- Hierarquia correta de títulos
- Tabelas padronizadas
- Listas consistentes
- Sem erros do markdownlint

---

## Objetivo Final

Toda documentação deverá permitir que qualquer pessoa consiga compreender o projeto, localizar rapidamente as informações e reproduzir os testes realizados.
