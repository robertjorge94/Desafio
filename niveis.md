# 🚀 Desafio de QA — Login e Cadastro

 ## 🎯 Objetivo

 Neste desafio, você deverá analisar, testar e automatizar uma aplicação web de **Login e Cadastro**.

 **Aplicação:**\
 https://horadoqa.github.io/login/

 O desafio foi dividido em três níveis:

- 🟢 **Nível 1 — Júnior:** fundamentos de QA e testes manuais;
- 🔵 **Nível 2 — Pleno:** automação, API e maior profundidade na estratégia de testes;
- 🟣 **Nível 3 — Desafio Extra:** práticas avançadas e características de um projeto de QA mais completo.

 Você pode realizar apenas o nível correspondente ao seu objetivo ou evoluir progressivamente até o Desafio Extra.

---

 # 🟢 Nível 1 — QA Júnior

 ## 🎯 Objetivo

 Demonstrar que você consegue **explorar uma aplicação, identificar cenários, executar testes e documentar problemas**.

 Neste nível, o foco principal é **teste manual e raciocínio de QA**.

 ## ✅ Obrigatório

 ### 1\. Exploração da aplicação

 Explore a aplicação e identifique:

- Fluxo de Login;
- Fluxo de Cadastro;
- Campos disponíveis;
- Campos obrigatórios;
- Validações;
- Mensagens apresentadas;
- Navegação;
- Comportamentos esperados.

 Não fique limitado aos fluxos "felizes".

 Pense:

 > "O que pode acontecer se o usuário fizer algo diferente do esperado?"

---

 ### 2\. Casos de teste

 Crie pelo menos **15 casos de teste**, contemplando:

 - Casos positivos;
- Casos negativos;
- Campos obrigatórios;
- Dados inválidos;
- Validação de e-mail;
- Validação de senha;
- Cadastro;
- Login;
- Navegação.

 Exemplo:

 | ID | Cenário | Resultado esperado |
| --- | --- | --- |
| CT-001 | Login com dados válidos | Usuário consegue acessar |
| CT-002 | Login com senha inválida | Sistema apresenta mensagem de erro |
| CT-003 | Login sem e-mail | Sistema valida campo obrigatório |

---

 ### 3\. Gherkin

 Transforme pelo menos **5 casos de teste** em cenários Gherkin.

 Exemplo:

```
Feature: Login

Scenario: Login com credenciais válidas
  Given que estou na página de login
  When informo um e-mail válido
  And informo uma senha válida
  And clico no botão de login
  Then devo acessar a área autenticada
```

---

 ### 4\. Execução manual

 Execute os casos de teste e registre:

 - Passou;
- Falhou;
- Bloqueado;
- Não aplicável.

 Apresente as evidências dos testes que falharam.

---

 ### 5\. Relatório de bugs

 Documente os problemas encontrados.

 Cada bug deverá conter:

 - ID;
- Título;
- Passos para reprodução;
- Resultado esperado;
- Resultado atual;
- Severidade;
- Evidência.

---

 ## 📦 Entrega mínima — Júnior

 O projeto deverá conter:

 - [ ] 15+ casos de teste;
- [ ] 5+ cenários Gherkin;
- [ ] Execução dos testes;
- [ ] Evidências;
- [ ] Bugs encontrados;
- [ ] README básico;
- [ ] Repositório GitHub organizado.

 ### 🏁 O que caracteriza um bom projeto Júnior?

 Não é a quantidade de testes.

 É demonstrar que você consegue:

 **entender → pensar em cenários → testar → identificar problemas → documentar.**

---

 # 🔵 Nível 2 — QA Pleno

 ## 🎯 Objetivo

 Neste nível, além dos testes manuais, você deverá demonstrar capacidade de **planejar uma estratégia de testes e automatizar os principais fluxos**.

 O foco passa de:

 > "Consigo testar?"

 para:

 > "Consigo definir o que deve ser testado, por quê e como manter esses testes?"

---

 # 1\. 📋 Estratégia de testes

 Crie um documento de estratégia contendo:

 - Objetivo;
- Escopo;
- Fora de escopo;
- Tipos de teste;
- Riscos;
- Premissas;
- Ambiente;
- Critérios de entrada;
- Critérios de saída;
- Estratégia de regressão.

---

 # 2\. 🧪 Testes manuais

 Amplie os testes do nível Júnior.

 Crie pelo menos **30 casos de teste**, incluindo:

 ### Login

 - Credenciais válidas;
- Credenciais inválidas;
- E-mail inválido;
- Senha inválida;
- Campos vazios;
- Combinações inválidas;
- Limites dos campos;
- Caracteres especiais;
- Espaços;
- Mensagens de erro.

 ### Cadastro

 - Cadastro válido;
- Campos obrigatórios;
- E-mail inválido;
- Senhas diferentes;
- Dados inválidos;
- Limites;
- Dados duplicados, caso aplicável;
- Mensagens de validação.

 ### Interface

 - Navegação;
- Botões;
- Links;
- Responsividade;
- Feedback visual;
- Usabilidade.

---

 # 3\. 🤖 Automação

 Escolha **Cypress ou Playwright**.

 Automatize pelo menos:

 - Login;
- Cadastro;
- Um cenário positivo;
- Dois cenários negativos;
- Validação de mensagens;
- Navegação.

 ### Requisitos

 O projeto deve possuir:

 - Estrutura organizada;
- Assertions;
- Seletores adequados;
- Reutilização de código;
- Dados de teste organizados;
- Relatórios;
- Evidências em caso de falha.

---

 # 4\. 🌐 Testes de API

 Caso existam APIs acessíveis relacionadas à aplicação, utilize **Postman**.

 Crie uma collection contendo os endpoints encontrados e teste:

 - Status code;
- Response body;
- Headers;
- Dados válidos;
- Dados inválidos;
- Campos obrigatórios;
- Cenários de erro.

 Crie também testes automatizados no Postman.

 > Se não houver uma API acessível para o fluxo, documente essa limitação em vez de criar endpoints fictícios e apresentá-los como parte da aplicação.

---

 # 5\. 🐞 Gestão de bugs

 Além dos requisitos do nível Júnior, acrescente:

 - Severidade;
- Prioridade;
- Ambiente;
- Evidências;
- Impacto;
- Status;
- Relação com caso de teste.

---

 # 6\. 📊 Relatório

 Apresente métricas como:

 - Total de testes;
- Passou;
- Falhou;
- Bloqueado;
- Taxa de sucesso;
- Quantidade de bugs;
- Bugs por severidade;
- Testes automatizados.

 Exemplo:

 | Indicador | Resultado |
| --- | --- |
| Casos executados | 35 |
| Passaram | 28 |
| Falharam | 7 |
| Bloqueados | 0 |
| Bugs encontrados | 5 |
| Cenários automatizados | 12 |

---

 ## 📦 Entrega mínima — Pleno

 - [ ] Estratégia de testes;
- [ ] 30+ casos de teste;
- [ ] Gherkin;
- [ ] Testes manuais;
- [ ] Automação com Cypress **ou** Playwright;
- [ ] Testes de API com Postman, quando aplicável;
- [ ] Relatório de bugs;
- [ ] Evidências;
- [ ] Relatório de execução;
- [ ] README profissional;
- [ ] GitHub organizado.

 ### 🏁 O que diferencia o Pleno do Júnior?

 O Júnior demonstra que sabe **executar testes**.

 O Pleno demonstra que consegue **pensar estrategicamente sobre os testes**, escolher o que automatizar, estruturar uma suíte sustentável e comunicar os resultados.

---

 # 🟣 Nível 3 — Desafio Extra

 ## 🚀 Objetivo

 Aqui não existe uma quantidade fixa de testes.

 O objetivo é construir um projeto que se aproxime de uma **estrutura profissional de QA**.

 Você deverá tomar decisões e justificar suas escolhas.

---

 # 1\. 🏗️ Arquitetura de automação

 Estruture a automação utilizando boas práticas.

 Por exemplo:

```
automation/
│
├── tests/
├── pages/
├── fixtures/
├── helpers/
├── data/
├── config/
└── reports/
```

 Considere utilizar:

 - Page Object Model;
- Fixtures;
- Massa de dados;
- Funções reutilizáveis;
- Configuração por ambiente;
- Tags;
- Testes parametrizados.

---

 # 2\. 🔄 CI/CD

 Configure uma pipeline utilizando **GitHub Actions** ou ferramenta equivalente.

 A pipeline deverá:

 1. Instalar dependências;
2. Executar os testes;
3. Gerar relatório;
4. Armazenar evidências;
5. Informar o resultado da execução.

 Exemplo:

```
Push
  ↓
GitHub Actions
  ↓
Instala dependências
  ↓
Executa testes
  ↓
Gera relatório
  ↓
Publica resultado
```

---

 # 3\. 🌐 Cross-browser

 Execute os testes automatizados em diferentes navegadores, quando suportado pela ferramenta escolhida.

 Por exemplo:

 - Chromium;
- Firefox;
- WebKit.

 Documente eventuais diferenças encontradas.

---

 # 4\. 📱 Responsividade

 Teste diferentes tamanhos de tela.

 Por exemplo:

 - Desktop;
- Tablet;
- Mobile.

 Identifique problemas de:

 - Layout;
- Campos;
- Botões;
- Textos;
- Navegação;
- Sobreposição de elementos.

---

 # 5\. ♿ Acessibilidade

 Realize uma avaliação básica de acessibilidade.

 Verifique, quando aplicável:

 - Labels;
- Navegação por teclado;
- Foco;
- Contraste;
- Textos alternativos;
- Estrutura semântica;
- Mensagens de erro;
- Uso sem mouse.

 Ferramentas como **axe**, Lighthouse ou outras podem ser utilizadas.

---

 # 6\. 🔐 Segurança — abordagem básica

 Faça apenas verificações seguras e apropriadas ao ambiente disponibilizado.

 Por exemplo:

 - Validação de entrada;
- Campos que aceitam valores inesperados;
- Exposição indevida de informações;
- Comportamentos inadequados de autenticação;
- Mensagens de erro excessivamente detalhadas.

 Não realize ataques destrutivos, tentativas de exploração invasiva ou testes contra sistemas que não estejam explicitamente autorizados para isso.

---

 # 7\. 📈 Dashboard de qualidade

 Crie uma visão consolidada dos resultados.

 Exemplo:

```
QUALITY REPORT

Testes manuais ........ 45
Testes automatizados .. 20
API ................... 10

Passaram .............. 62
Falharam .............. 13
Bloqueados ............ 0

Bugs encontrados ...... 8

Críticos .............. 0
Altos ................. 2
Médios ................ 4
Baixos ................ 2
```

 O formato pode ser:

 - Markdown;
- HTML;
- Dashboard;
- Ferramenta de reporting.

---

 # 8\. 🧠 Testes exploratórios

 Além dos casos previamente definidos, realize uma sessão de **teste exploratório**.

 Documente:

 - O que foi explorado;
- Tempo da sessão;
- Áreas investigadas;
- Hipóteses;
- Problemas encontrados;
- Observações.

 Exemplo:

```
Sessão: Login Explorer
Duração: 45 minutos

Objetivo:
Investigar validações e comportamentos inesperados
no fluxo de login.

Áreas exploradas:
- Campos
- Validações
- Navegação
- Mensagens
- Responsividade

Resultado:
3 problemas identificados.
```

---

 # 9\. 📚 Documentação profissional

 O README deverá permitir que outra pessoa clone o projeto e execute os testes sem precisar perguntar como fazer.

 Inclua:

 - Objetivo;
- Arquitetura;
- Tecnologias;
- Pré-requisitos;
- Instalação;
- Configuração;
- Execução;
- Testes manuais;
- Automação;
- API;
- CI/CD;
- Relatórios;
- Bugs;
- Limitações;
- Melhorias futuras.

---

 # 🏆 O que diferencia o Desafio Extra?

 Não é simplesmente "ter mais testes".

 Um projeto avançado demonstra:

 **pensamento crítico + estratégia + automação + arquitetura + documentação + CI/CD + análise de resultados.**

 A pessoa demonstra que consegue pensar no processo de qualidade como um todo, e não apenas executar scripts.

---

 # 📊 Comparação dos níveis

 | Requisito | 🟢 Júnior | 🔵 Pleno | 🟣 Extra |
| --- | --- | --- | --- |
| Exploração da aplicação | ✅ | ✅ | ✅ |
| Testes manuais | ✅ | ✅ | ✅ |
| Casos de teste | 15+ | 30+ | Livre |
| Gherkin | 5+ | ✅ | ✅ |
| Bugs documentados | ✅ | ✅ | ✅ |
| Estratégia de testes | Básica | ✅ | Avançada |
| Cypress/Playwright | — | ✅ | ✅ |
| Postman/API | — | Quando aplicável | ✅ |
| Page Object | — | Recomendado | ✅ |
| Testes parametrizados | — | Recomendado | ✅ |
| Cross-browser | — | — | ✅ |
| Responsividade | Básica | ✅ | ✅ |
| Acessibilidade | — | — | ✅ |
| Testes exploratórios | Básico | ✅ | ✅ |
| CI/CD | — | — | ✅ |
| Relatórios | Básico | ✅ | Avançado |
| Dashboard | — | — | ✅ |
| README | Básico | Profissional | Completo |
| Git/GitHub | Básico | Organizado | Profissional |

---

 # 🎓 O que esperamos de cada nível?

 ## 🟢 Júnior

 > "Consigo testar uma aplicação e encontrar problemas."

 Deve demonstrar fundamentos de QA, atenção aos detalhes e capacidade de documentar os resultados.

 ## 🔵 Pleno

 > "Consigo definir uma estratégia de testes e automatizar os principais cenários."

 Deve demonstrar autonomia, organização, capacidade de análise e conhecimento de automação.

 ## 🟣 Desafio Extra

 > "Consigo estruturar um processo de qualidade completo."

 Deve demonstrar visão sistêmica, arquitetura de automação, integração contínua, análise de riscos, qualidade de código e comunicação dos resultados.

---

 # 📌 Regra principal do desafio

 **Não tente preencher requisitos apenas para marcar um checkbox.**

 Se você decidir não implementar determinada técnica, explique o motivo.

 Por exemplo:

 > "A aplicação não disponibiliza uma API acessível para o fluxo de cadastro. Por esse motivo, os testes de API não foram implementados. A limitação foi registrada no relatório."

 Essa justificativa faz parte da avaliação.

---

 # 🏁 Entrega final

 Ao finalizar, disponibilize o link do seu **repositório GitHub** contendo todo o material produzido.

 O projeto deve ser compreensível para outra pessoa sem que seja necessário explicar pessoalmente como ele funciona.

 ## ⭐ Pergunta final

 Ao terminar o projeto, responda no README:

 > **Se você tivesse apenas duas horas para executar uma regressão antes de uma nova versão ser publicada, quais testes escolheria e por quê?**

 A resposta deve considerar **risco, impacto no usuário, criticidade da funcionalidade e custo de execução**, e não simplesmente escolher os testes mais fáceis de automatizar.

 Uma melhoria importante nessa versão é que **não transformamos o nível em uma competição de quantidade**. O salto de Júnior → Pleno → Extra acontece principalmente pela **profundidade do raciocínio de QA**: primeiro testar bem, depois estruturar e automatizar, e finalmente criar um processo de qualidade reproduzível e integrado.