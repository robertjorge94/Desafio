# Desafio de QA — Login e Cadastro

 ## Sobre o desafio

 Neste desafio, você atuará como uma pessoa **QA**, responsável por analisar, testar e avaliar uma aplicação web de **Login e Cadastro**.

 **Aplicação:**\
 https://horadoqa.github.io/login/

 A proposta é passar por diferentes etapas de um processo de qualidade de software:

 **Análise → Testes Manuais → Gherkin → Automação → Testes de API → Relatório de Bugs → Documentação**

 O objetivo não é apenas verificar se a aplicação "funciona", mas identificar possíveis comportamentos inesperados e demonstrar uma estratégia de testes bem estruturada.

---

 # 🎯 Objetivos

 Ao finalizar o desafio, você deverá demonstrar conhecimento em:

- Análise de requisitos e regras de negócio;
- Elaboração de cenários de testes;
- Testes funcionais;
- Testes positivos e negativos;
- Testes exploratórios;
- BDD/Gherkin;
- Automação de testes E2E;
- Cypress ou Playwright;
- Testes de API com Postman;
- Identificação e documentação de bugs;
- Organização de um projeto de QA;
- Versionamento e documentação no GitHub.

---

 # 1\. Análise da aplicação

 Antes de começar a testar, explore a aplicação e identifique:

- Quais funcionalidades estão disponíveis;
- Quais campos existem;
- Quais campos são obrigatórios;
- Quais validações existem;
- Quais mensagens são apresentadas;
- Como funciona a navegação;
- Quais comportamentos são esperados;
- Quais comportamentos podem representar defeitos.

 Não comece simplesmente automatizando os primeiros passos que encontrar.

 **Primeiro compreenda a aplicação.**

---

# 2\. 🧪 Testes Manuais

Crie uma suíte de testes manuais contemplando, no mínimo:

### Login

- Login com credenciais válidas;
- Login com senha inválida;
- Login com e-mail inexistente;
- Login com e-mail inválido;
- Login com campos vazios;
- Login somente com e-mail;
- Login somente com senha;
- Espaços antes/depois dos dados;
- Valores nos limites permitidos pelos campos;
- Valores acima dos limites;
- Caracteres especiais;
- Diferentes combinações de dados inválidos.

### Cadastro

- Cadastro com dados válidos;
- Cadastro com campos obrigatórios vazios;
- Cadastro com e-mail inválido;
- Cadastro com e-mail já utilizado;
- Senha inválida;
- Confirmação de senha diferente;
- Dados abaixo do tamanho mínimo;
- Dados acima do tamanho máximo;
- Caracteres especiais;
- Espaços;
- Tentativas com dados incompletos.

 ### Interface e navegação

 Avalie também:

- Navegação entre Login e Cadastro;
- Links e botões;
- Mensagens de validação;
- Feedback apresentado ao usuário;
- Comportamento dos campos;
- Layout;
- Responsividade;
- Comportamento em diferentes resoluções;
- Usabilidade.

> Os cenários acima são apenas um ponto de partida. Durante a exploração, novos casos de teste devem ser identificados.

---

# 3\. 📝 Gherkin / BDD

Transforme os principais casos de teste em cenários utilizando **Given, When, Then**.

Exemplo:

```
Feature: Login

  Scenario: Login com credenciais válidas
    Given que o usuário está na página de login
    When informar um e-mail válido
    And informar uma senha válida
    And clicar no botão de login
    Then o sistema deve permitir o acesso do usuário
```

 Crie cenários para fluxos positivos e negativos.

 Sempre que possível, organize os cenários por **Feature**.

 Exemplo:

```
features/
├── login.feature
├── cadastro.feature
└── navegacao.feature
```

---

 # 4\. 🤖 Automação de Testes

 Após executar os testes manualmente, escolha os cenários mais relevantes para automação.

 Utilize:

 - **Cypress**

 ou

 - **Playwright**

 A automação deverá contemplar, no mínimo:

 - Fluxo de login;
- Fluxo de cadastro;
- Validações importantes;
- Cenários positivos;
- Cenários negativos;
- Validação das mensagens apresentadas;
- Validação dos resultados esperados.

 ## Boas práticas esperadas

 O projeto deverá apresentar:

- Organização dos testes;
- Seletores confiáveis;
- Reutilização de código;
- Fixtures, quando fizer sentido;
- Funções auxiliares;
- Dados de teste separados do código;
- Assertions claras;
- Nomenclatura consistente;
- Tratamento adequado de evidências;
- Código legível e sustentável.

---

 # 5\. 🌐 Testes de API

 Caso sejam identificadas APIs utilizadas pela aplicação, crie uma coleção no **Postman**.

 Teste, quando aplicável:

- GET;
- POST;
- PUT/PATCH;
- DELETE;
- Status codes;
- Headers;
- Request body;
- Response body;
- Campos obrigatórios;
- Dados inválidos;
- Cenários de sucesso;
- Cenários de erro.

 Também deverão ser criados testes automatizados no Postman para validar as respostas.

 Exemplo:

```
pm.test("Status code deve ser 200", function () {
    pm.response.to.have.status(200);
});
```

 > Não é necessário inventar APIs que não façam parte da aplicação. Caso não exista uma API acessível para testes, documente essa limitação no projeto.

---

# 6\. Relatório de Bugs

 Todo defeito encontrado deverá ser documentado.

 Utilize, no mínimo, os seguintes campos:

 | Campo | Descrição |
| --- | --- |
| ID | Identificador do bug |
| Título | Resumo do problema |
| Descrição | Explicação do defeito |
| Pré-condição | Estado necessário para reproduzir |
| Passos | Passo a passo |
| Resultado esperado | O que deveria acontecer |
| Resultado atual | O que aconteceu |
| Severidade | Impacto técnico/funcional |
| Prioridade | Ordem de tratamento |
| Ambiente | Browser, SO etc. |
| Evidência | Screenshot, vídeo ou log |
| Status | Aberto, corrigido, retestado etc. |

### Exemplo

```
BUG-001

Título:
Sistema permite cadastro sem preenchimento do e-mail.

Passos:
1. Acessar a página de cadastro.
2. Preencher os demais campos.
3. Deixar o campo de e-mail vazio.
4. Clicar em "Cadastrar".

Resultado esperado:
O sistema deve informar que o campo e-mail é obrigatório.

Resultado atual:
O cadastro é processado sem apresentar a validação esperada.

Severidade:
Alta

Prioridade:
Alta
```

---

# 7\. Relatório de execução

 Ao final, apresente um resumo dos testes:

 | Tipo | Total | Passou | Falhou | Bloqueado |
| --- | --- | --- | --- | --- |
| Testes Manuais | - | - | - | - |
| Cypress/Playwright | - | - | - | - |
| API/Postman | - | - | - | - |

Também informe:

 - Quantidade de bugs encontrados;
- Bugs por severidade;
- Cenários automatizados;
- Cenários que não puderam ser automatizados;
- Limitações encontradas;
- Riscos identificados.

---

 # 8\. Estrutura sugerida do GitHub

 Organize o projeto de forma profissional.

```
qa-login-cadastro/
│
├── README.md
│
├── docs/
│   ├── plano-de-testes.md
│   ├── casos-de-teste.md
│   ├── cenarios-gherkin.md
│   └── relatorio-final.md
│
├── manual-tests/
│   └── casos-de-teste.xlsx
│
├── bugs/
│   └── bugs.md
│
├── automation/
│   ├── cypress/
│   │   └── ...
│   │
│   └── playwright/
│       └── ...
│
├── api/
│   ├── collection.json
│   └── environment.json
│
├── evidence/
│   ├── screenshots/
│   └── videos/
│
└── .gitignore
```

 Você não precisa necessariamente utilizar **Cypress e Playwright ao mesmo tempo**. Escolha uma das ferramentas para a implementação principal.

---

 # 9\. README.md

 O README deve permitir que outra pessoa consiga entender e executar o projeto.

 Inclua:

 ### Sobre o projeto

 Explique brevemente o objetivo do desafio.

 ### Aplicação testada

 Informe o endereço da aplicação.

 ### Tecnologias

 Exemplo:

```
- Gherkin
- Cypress
- JavaScript
- Postman
- Git/GitHub
```

 ou:

```
- Gherkin
- Playwright
- TypeScript
- Postman
- Git/GitHub
```

 ### Como executar

 Explique passo a passo como instalar as dependências e executar os testes.

 ### Testes

 Informe quais cenários foram automatizados.

 ### Bugs encontrados

 Apresente um resumo dos principais problemas identificados.

 ### Evidências

 Adicione screenshots, vídeos ou relatórios relevantes.

---

 # 10\. ⭐ Desafio Extra

 Para quem quiser ir além:

- Criar uma pipeline de CI/CD;
- Executar os testes automaticamente no GitHub Actions;
- Gerar relatório HTML;
- Executar testes em diferentes browsers;
- Criar testes parametrizados;
- Implementar Page Object Model;
- Criar comandos/métodos reutilizáveis;
- Configurar ambientes;
- Gerenciar dados de teste;
- Integrar resultados da automação ao CI;
- Adicionar lint e formatação ao projeto;
- Criar testes de acessibilidade;
- Realizar testes de responsividade;
- Criar uma estratégia de regressão.

---

 # 🏆 Critérios de avaliação

 O projeto será avaliado considerando:

| Critério | Avaliação |
| --- | --- |
| Análise da aplicação | Identificação dos principais fluxos e riscos |
| Testes manuais | Cobertura e qualidade dos casos |
| Gherkin | Clareza e organização dos cenários |
| Automação | Qualidade e manutenção do código |
| API | Qualidade das validações, quando aplicável |
| Bugs | Capacidade de identificar e documentar problemas |
| Evidências | Clareza das evidências apresentadas |
| Organização | Estrutura do projeto |
| Git/GitHub | Commits e organização do repositório |
| Documentação | Clareza do README e relatórios |

---

 # 📦 Entrega final

 Ao concluir o desafio, o repositório deverá conter:

- [ ] Plano de testes;
- [ ] Casos de testes manuais;
- [ ] Cenários em Gherkin;
- [ ] Evidências dos testes;
- [ ] Automação com Cypress ou Playwright;
- [ ] Testes de API com Postman, quando aplicável;
- [ ] Relatório de bugs;
- [ ] Relatório final;
- [ ] README.md;
- [ ] Instruções para execução;
- [ ] Código organizado;
- [ ] Histórico de commits.

 ## 🎯 Objetivo final

 O resultado esperado é um projeto que possa ser apresentado como **portfólio de QA**, demonstrando não apenas conhecimento de ferramentas, mas principalmente capacidade de:

 **pensar em cenários → identificar riscos → testar → encontrar problemas → automatizar → documentar → comunicar os resultados.**
