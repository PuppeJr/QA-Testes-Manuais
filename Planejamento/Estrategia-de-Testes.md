# Estratégia de Testes

## Objetivo

Definir a abordagem utilizada para validar a qualidade do sistema, estabelecendo quais tipos de testes serão executados, suas prioridades e critérios de cobertura.

---

## Objetivos da Estratégia

- Garantir a qualidade das funcionalidades críticas.
- Identificar defeitos o mais cedo possível.
- Reduzir riscos durante a homologação.
- Assegurar a rastreabilidade entre requisitos e testes.
- Apoiar futuras atividades de automação.

---

## Tipos de Testes

| Tipo de Teste   | Objetivo                                                        | Aplicação             |
|-----------------|-----------------------------------------------------------------|-----------------------|
| Funcional       | Validar regras de negócio                                       | Todo o sistema        |
| Exploratório    | Descobrir comportamentos inesperados                            | Funcionalidades novas |
| Negativo        | Validar tratamento de erros                                     | Login, formulários    |
| Regressão       | Garantir que alterações não afetaram funcionalidades existentes | Após correções        |
| Usabilidade     | Avaliar facilidade de uso                                       | Interface             |
| Segurança       | Validar proteção contra acessos indevidos                       | Login e autenticação  |
| Compatibilidade | Verificar funcionamento em diferentes navegadores               | Interface Web         |

---

## Priorização

| Prioridade | Critério                            |
|------------|-------------------------------------|
| Alta       | Funcionalidades críticas ao negócio |
| Média      | Funcionalidades importantes         |
| Baixa      | Funcionalidades complementares      |

---

## Funcionalidades Prioritárias

- Login
- Dashboard
- Resultados
- Temporadas
- Classificação

---

## Cobertura Inicial

Nesta fase do projeto serão priorizados:

- Testes Funcionais
- Testes Exploratórios
- Testes Negativos
- Testes de Segurança
- Testes de Regressão

---

## Ferramentas Utilizadas

- Git
- GitHub
- Visual Studio Code
- Markdown
- Google Chrome
- Chrome DevTools

---

## Evolução

A estratégia será revisada ao final de cada sprint para incorporar novos tipos de testes, automação e melhorias no processo.
