# 🧪 Automação de Testes E2E - Central de Atendimento (CAC TAT)

![Cypress](https://img.shields.io/badge/-cypress-%23E5E5E5?style=for-the-badge&logo=cypress&logoColor=058a5e)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

Este projeto consiste em uma suíte de testes automatizados End-to-End (E2E) para a aplicação **Central de Atendimento ao Cliente TAT**. O objetivo é garantir a qualidade das funcionalidades críticas de envio de formulários, validação de campos e usabilidade em diferentes viewports.

## 🚀 Funcionalidades Testadas

Os testes cobrem os principais fluxos de usuário descritos em `cypress/integration/CAC-TAT.spec.js`:

- **Formulários:** Preenchimento e envio com sucesso; validação de campos obrigatórios e formatos de email inválidos.
- **Upload de Arquivos:** Testes de anexação de arquivos via seleção direta e *Drag & Drop*.
- **API & Rede:** Validação de requisições HTTP (GET) interceptadas para garantir status 200 e integridade do corpo da resposta.
- **Responsividade:** Execução de testes simulando dispositivos móveis (viewport mobile).
- **Avançado:**
  - Uso de **Comandos Customizados** para reduzir repetição de código.
  - Manipulação do relógio do navegador (`cy.clock` e `cy.tick`) para testes de mensagens temporárias.
  - Invocação de métodos e atributos ocultos com `.invoke()`.
  - Tratamento de links que abrem em outra aba (`target="_blank"`).

## 🛠️ Tecnologias Utilizadas

- **Cypress**: Framework de automação.
- **JavaScript**: Linguagem de script.
- **GitHub Actions**: Pipeline de Integração Contínua (CI) configurado para rodar os testes a cada *push*.
- **Lodash**: Utilizado para repetição de testes (`Cypress._.times`) garantindo estabilidade.

## 📂 Estrutura do Projeto

O projeto segue o padrão de arquitetura do Cypress:

- `cypress/integration/`: Arquivos de teste (specs).
- `cypress/support/`: Comandos customizados (`commands.js`).
- `cypress/fixtures/`: Massas de dados para testes.
- `.github/workflows/`: Configuração do pipeline de CI.

## ▶️ Como Rodar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/ThiLinhares/cypress-basico-v2.git](https://github.com/ThiLinhares/cypress-basico-v2.git)
   cd cypress-basico-v2
