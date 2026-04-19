# 🧪 QA Manual — SwagLabs Shopping

Projeto prático do bootcamp DIO: **"O dia a dia de um QA: A prática de testes manuais funcionais"**, ministrado por Carolina Santana Louzada (Analista QA — Venturus).

O objetivo é revisar conceitos de testes manuais no contexto ágil e praticar as atividades do dia a dia de um QA, com foco em testes funcionais caixa-preta.

Aqui está o material de apoio e [especificacao.pdf](especificacao.pdf) do projeto.


---

## 📋 Sobre o projeto

| Item | Detalhe |
|---|---|
| Aplicação testada | [SwagLabs Shopping](https://www.saucedemo.com) |
| Metodologia | Scrum |
| Gerenciamento | JIRA + Confluence |
| Execução dos testes | Manual |
| Nível | Sistema e Aceite |
| Tipo | Funcional caixa-preta |

---

## 📁 Estrutura dos arquivos

```
.
├── README.md
├── 01_fluxo_trabalho_e_bug.pdf
├── 02_user_stories.pdf
└── 03_casos_de_teste.pdf
```

---

## 📄 Descrição dos documentos

### [01_fluxo_trabalho_e_bug.pdf](01_fluxo_trabalho_e_bug.pdf)

Define o fluxo de trabalho do projeto e o ciclo de vida de bugs.

**Conteúdo:**
- Visão geral do projeto e ferramentas utilizadas
- Tabela de status do workflow no JIRA: `TO DO → IN PROGRESS → READY FOR QA → IN REVIEW (QA) → DONE`, com desvios para `BLOCKED` e `REOPENED`
- Transições permitidas entre os status
- Ciclo de vida do bug: `NEW → ASSIGNED → OPEN → IN PROGRESS → FIXED → PENDING RETEST → RETEST → VERIFIED → CLOSED`, com os desvios `REOPENED`, `REJECTED` e `DEFERRED`
- Campos obrigatórios para abertura de bug (ID, título, severidade, prioridade, evidências etc.)
- Regras gerais do processo de QA na sprint

---

### [02_user_stories.pdf](02_user_stories.pdf)

Contém duas User Stories elaboradas a partir da análise do SwagLabs, seguindo o critério INVEST e o princípio 3C.

**US-01 — Login de usuário** (Épico: Autenticação)
> "Como cliente cadastrado, desejo fazer login na plataforma para que eu possa acessar minha conta e realizar compras de forma personalizada."

- Atores, interfaces e fluxo de navegação
- Tabela de dados de entrada (username, password)
- Regras de negócio (usuário bloqueado, credenciais inválidas, persistência de sessão)
- 3 critérios de aceite em Gherkin (login válido, senha incorreta, usuário bloqueado)

**US-02 — Adicionar produto ao carrinho** (Épico: Carrinho de Compras)
> "Como cliente autenticado, desejo adicionar produtos ao carrinho para que eu possa selecioná-los antes de finalizar a compra."

- Atores, interfaces e fluxo de navegação
- Tabela de dados exibidos no carrinho
- Regras de negócio (contador, persistência, sem duplicatas)
- 3 critérios de aceite em Gherkin (adicionar, remover, visualizar itens)

---

### [03_casos_de_teste.pdf](03_casos_de_teste.pdf)

Reúne o plano de testes, os casos step-by-step, os cenários BDD e o ciclo de testes da Sprint 1.

**Plano de Testes**
- Ambiente: Chrome 124 / Windows 11 / Staging
- Escopo: Módulos de Autenticação e Carrinho
- Critérios de entrada e saída da sprint

**Casos de Teste — Step-by-Step (CT-01 a CT-04)**

| ID | Título | US | Tipo |
|---|---|---|---|
| CT-01 | Login com credenciais válidas | US-01 | Positivo |
| CT-02 | Login com senha incorreta | US-01 | Negativo |
| CT-03 | Adicionar produto ao carrinho | US-02 | Positivo |
| CT-04 | Remover produto a partir da listagem | US-02 | Negativo |

Cada caso inclui pré-condição, passos numerados com dados de entrada e resultado esperado, e pós-condição.

**Cenários BDD — Gherkin (BDD-01 a BDD-04)**

| ID | Cenário | US |
|---|---|---|
| BDD-01 | Login bem-sucedido com credenciais válidas | US-01 |
| BDD-02 | Login falha com usuário bloqueado | US-01 |
| BDD-03 | Adicionar produto ao carrinho com sucesso | US-02 |
| BDD-04 | Checkout não pode ser iniciado com carrinho vazio | US-02 |

**Ciclo de Testes Sprint 1**
- Consolidação dos 8 casos com rastreabilidade para as User Stories e status de execução

---

## 🛠️ Ferramentas sugeridas pelo projeto

- **Gerenciamento:** JIRA Software
- **Documentação:** Confluence
- **Casos de teste:** Zephyr Scale (plugin JIRA)
- **Mind maps:** XMind / MindMup / Miro

---

## 🔗 Referências

- [SwagLabs Shopping — aplicação alvo](https://www.saucedemo.com)
- [DIO — Digital Innovation One](https://www.dio.me)
