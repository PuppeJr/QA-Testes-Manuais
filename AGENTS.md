# AGENTS.md

## Objetivo

Este repositório utiliza uma esteira de QA Manual baseada em rastreabilidade completa.

Todos os agentes devem respeitar os padrões definidos neste documento.

## Regras obrigatórias

- Nunca sobrescrever arquivos automaticamente.
- Sempre apresentar uma versão para revisão.
- Mostrar as diferenças antes da substituição.
- Apenas um H1 por arquivo.
- Compatibilidade total com markdownlint.
- Preservar IDs:
  - RF
  - PT
  - CT
  - MT
  - ET
  - EV
  - BUG
  - RK

- Nunca quebrar a rastreabilidade.

Fluxo obrigatório:

RF
↓
PT
↓
CT
↓
MT
↓
ET
↓
EV
↓
BUG
↓
Matriz

Ao finalizar qualquer alteração:

- sugerir Conventional Commit
- nunca executar alterações destrutivas
- nunca criar arquivos *.refatorado.md sem autorização
