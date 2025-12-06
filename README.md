# 🧪 Automação de Testes E2E - Central de Atendimento (CAC TAT)

![Cypress](https://img.shields.io/badge/-cypress-%23E5E5E5?style=for-the-badge&logo=cypress&logoColor=058a5e)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)

Este projeto consiste em uma suíte de testes automatizados End-to-End (E2E) para a aplicação **Central de Atendimento ao Cliente TAT**. O objetivo é garantir a qualidade das funcionalidades críticas de envio de formulários, validação de campos e usabilidade em diferentes resoluções.

## 🚀 Funcionalidades Testadas

Os testes cobrem os principais fluxos de usuário identificados no arquivo principal de especificação:

- **Formulários:**
  - Preenchimento e envio com sucesso.
  - Validação de campos obrigatórios e formatos de email inválidos.
  - Teste de campos numéricos (telefone) rejeitando caracteres não-numéricos.
- **Upload de Arquivos:**
  - Testes de anexação de arquivos via seleção direta (`selectFile`).
  - Simulação de *Drag & Drop*.
  - Uso de *fixtures* e *alias* para arquivos.
- **API & Rede:**
  - Validação de requisições HTTP (GET) interceptadas para garantir status 200 e integridade do corpo da resposta.
- **Interface Avançada:**
  - Manipulação de classes CSS para exibir mensagens de sucesso e erro.
  - Verificação de links que abrem em outra aba (`target="_blank"`).
  - Interação com elementos ocultos utilizando `.invoke('show')`.
- **Responsividade:**
  - Execução de testes simulando dispositivos móveis (viewport mobile).

## 🛠️ Tecnologias Utilizadas

- **Cypress**: Framework de automação principal.
- **JavaScript**: Linguagem de script.
- **GitHub Actions**: Pipeline de Integração Contínua (CI) configurado para rodar os testes a cada *push*.
- **Lodash**: Utilizado para repetição de testes (`Cypress._.times`) garantindo estabilidade.

## 📂 Estrutura do Projeto

O projeto segue a estrutura padrão recomendada pelo Cypress:

- `cypress/integration/`: Arquivos de teste (ex: `CAC-TAT.spec.js`).
- `cypress/support/`: Comandos customizados (`commands.js`).
- `cypress/fixtures/`: Massas de dados para testes (ex: `example.json`).
- `.github/workflows/`: Configuração do pipeline de CI (`ci.yml`).

## ▶️ Como Rodar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/ThiLinhares/cypress-basico-v2.git
   cd cypress-basico-v2
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Execute os testes:**

   - **Interface Gráfica (Cypress Runner):**
     Para abrir o Cypress e ver os testes rodando interativamente:
     ```bash
     npm run cy:open
     ```

   - **Modo Headless (Terminal):**
     Para rodar todos os testes no terminal (ideal para CI):
     ```bash
     npm test
     ```

   - **Simulação Mobile (Visual):**
     Para abrir o Cypress simulando um dispositivo de 410x860:
     ```bash
     npm run cy:open:mobile
     ```
     
   - **Simulação Mobile (Headless):**
     Para rodar os testes mobile pelo terminal:
     ```bash
     npm run test:mobile
     ```

## 🤖 Integração Contínua

Este repositório possui um workflow configurado no GitHub Actions que executa toda a suíte de testes automaticamente.

- **Arquivo de configuração:** `.github/workflows/ci.yml`
- **Gatilho:** Executado a cada `push` para o repositório.
- **Passos:** Checkout do código, instalação de dependências e execução do `cypress-io/github-action`.

---
Desenvolvido por **Thiago Linhares** [LinkedIn](https://www.linkedin.com/in/thiagolinharesm/)
