# ET-002 - Login Google Válido

## Objetivo

Validar que um usuário autorizado consegue acessar o sistema utilizando autenticação Google.

---

## Ambiente

| Item | Valor |
| ---- | ----- |
| Sistema | SIM Racing Manager |
| Ambiente | UAT |
| URL | [SIM Racing Manager UAT](https://app-uat.simracingmanager.online/signIn) |
| Navegador | Google Chrome |
| Sistema Operacional | Windows 11 |

---

## Caso de Teste Relacionado

CT-SRM-001

---

## Pré-condições

- Conta Google cadastrada.
- Internet disponível.
- Navegador atualizado.

---

## Passos Executados

1. Acessar a página de Login.
2. Verificar carregamento da tela.
3. Clicar em **Entrar com Google**.
4. Selecionar conta Google autorizada.
5. Confirmar autenticação.

---

## Resultado Obtido

O usuário foi autenticado com sucesso utilizando uma conta Google previamente autorizada e foi redirecionado para o Dashboard do sistema.

---

## Status

☑ Executado com Sucesso

---

## Evidências

- Captura da tela de Login.
- Captura da tela do Dashboard após autenticação.
- Evidências armazenadas na pasta `Evidencias/ET-002/`.

---

## Observações

Durante a inspeção e execução inicial da tela de autenticação foram observados os seguintes comportamentos:

- O botão **Entrar com Google** altera levemente sua tonalidade quando o cursor do mouse é posicionado sobre ele (efeito hover).
- O cursor é alterado para o formato de mão, indicando corretamente um elemento clicável.
- O botão pode ser acessado utilizando apenas o teclado (TAB + ENTER), demonstrando suporte básico à navegação por teclado.
- Ao clicar em **Entrar com Google**, há apenas um breve piscar da interface antes da abertura da janela de autenticação do Google. Não existe indicador visual de carregamento (spinner ou barra de progresso).
- Foi possível realizar múltiplos cliques rápidos antes da abertura da janela de autenticação, indicando ausência de bloqueio contra múltiplas interações.
- Em resolução reduzida, o botão permaneceu visível e funcional, não sendo identificados problemas de responsividade durante a inspeção inicial.
