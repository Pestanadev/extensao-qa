## Cenário 02: Página Inicial.

**Tela:** `/dashboard` · **Área:** Principal · **Requisito:** [RF02](../1-Analise-de-requisitos.md#rf02)

### Caso de Teste 01: Carregar Página Inicial.

| ID | Descrição |
| :------- | :------- |
| C02-CT01 | Carregar Página Inicial. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Página Inicial (`/dashboard`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Página Inicial do SIFIT |
| **QUANDO** entrar e aguardar carregamento da página inicial |
| **ENTÃO** exibir resumo, indicadores e navegação; números exatos dependem do ambiente |

| **Critérios de aceitação** |
| :------- |
| Exibir resumo, indicadores e navegação; números exatos dependem do ambiente. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | [Captura](../evidencias/imagens/EXE-login-sucesso.png) | — | Exploração local — CT-RF02-01 |

**Observação da execução:** Resumo, indicadores e menus carregaram. Aprovação de apresentação, sem homologar totais.

---

### Caso de Teste 02: Conciliar cartão Sem Matrículas e detalhamento.

| ID | Descrição |
| :------- | :------- |
| C02-CT02 | Conciliar cartão Sem Matrículas e detalhamento. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Página Inicial (`/dashboard`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Página Inicial do SIFIT |
| **QUANDO** anotar período e quantidade do cartão; abrir Sem Matrículas; anotar total, linhas e critérios do modal |
| **ENTÃO** totais coerentes para o mesmo conjunto ou explicação explícita de critérios diferentes |

| **Critérios de aceitação** |
| :------- |
| Totais coerentes para o mesmo conjunto ou explicação explícita de critérios diferentes. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Inconclusivo | Registro textual | — | Exploração local — CT-RF02-02 |

**Observação da execução:** Inicialmente cartão mostrou 6 e modal 0. Na revisão, modal mostrou 6 registros e total 6, compatíveis com o cartão. A divergência inicial não se repetiu; conciliação completa ainda depende do banco.

---

### Caso de Teste 03: Dashboard — Botão ao lado de "Competência" sem funcionalidade.

| ID | Descrição |
| :------- | :------- |
| C02-CT03 | Verificar botão ao lado de "Competência" sem funcionalidade em Dashboard. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Dashboard (`/dashboard`) |
| **QUANDO** clicamos no botão localizado ao lado do campo de período ("Competência") |
| **ENTÃO** deve ser aberta a seleção de período ou aplicado o filtro correspondente |

| **Critérios de aceitação** |
| :------- |
| Deve ser aberta a seleção de período ou aplicado o filtro correspondente. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 01/10/2026 21:36 | sifit | Reprovado | [Print (Jam)](https://jam.dev/c/4dfcb03a-bf1b-4d35-8874-31f846f25250) | [BUG-006](../3-Relatorio-de-Bugs.md#bug-006) | Equipe (vídeos JAM) — CT-04 do repositório anterior |

**Observação da execução:** Botão ao lado do período sem ação; reproduzido no sifit em 18/11 (sem mudança na tela e sem requisição).

---

### Caso de Teste 04: Financeiro — Cobrar todos via WhatsApp.

| ID | Descrição |
| :------- | :------- |
| C02-CT04 | Verificar cobrar todos via WhatsApp em Financeiro. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Financeiro (`/dashboard`) |
| **QUANDO** clicamos em "Cobrar todos no WhatsApp" |
| **ENTÃO** as cobranças devem ser enviadas ou deve ser informada a indisponibilidade da integração |

| **Critérios de aceitação** |
| :------- |
| As cobranças devem ser enviadas ou deve ser informada a indisponibilidade da integração. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 22/10/2026 19:43 | sifitalfa | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/72e56dc7-3c8c-43e9-9c8f-13a80cad87f1) | — | Equipe (vídeos JAM) — CT-07 do repositório anterior |

**Observação da execução:** Depende do WhatsApp, desconectado no ambiente; envio não verificável.

---

### Caso de Teste 05: Financeiro — Exportar.

| ID | Descrição |
| :------- | :------- |
| C02-CT05 | Verificar exportar em Financeiro. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Financeiro (`/dashboard`) |
| **QUANDO** clicamos em "Exportar" |
| **ENTÃO** deve ser gerado o arquivo com os dados exibidos |

| **Critérios de aceitação** |
| :------- |
| Deve ser gerado o arquivo com os dados exibidos. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 22/10/2026 19:45 | sifitalfa | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/7d3f61d3-5e70-43fd-b0da-0e380956c7cb) | — | Equipe (vídeos JAM) — CT-08 do repositório anterior |

**Observação da execução:** Gravação de 4 s sem ações; arquivo exportado não aparece.

---

### Caso de Teste 06: Financeiro — Desistência - tela sem registros.

| ID | Descrição |
| :------- | :------- |
| C02-CT06 | Verificar desistência - tela sem registros em Financeiro. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Financeiro (`/dashboard`) |
| **QUANDO** abrimos o detalhamento de desistências |
| **ENTÃO** a lista deve ser coerente com o indicador exibido no painel |

| **Critérios de aceitação** |
| :------- |
| A lista deve ser coerente com o indicador exibido no painel. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 22/10/2026 19:46 | sifitalfa | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/c503ecf1-549d-4e44-8c9e-90e9038765b8) | — | Equipe (vídeos JAM) — CT-10 do repositório anterior |

**Observação da execução:** Tela vazia exibida; relação com o indicador de desistências não verificada.

---

### Caso de Teste 07: Acionar botão ao lado do período no painel.

| ID | Descrição |
| :------- | :------- |
| C02-CT07 | Acionar botão ao lado do período no painel. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Página Inicial |
| **QUANDO** clicamos no botão de seta ao lado do intervalo de datas |
| **ENTÃO** deve ser aberta a seleção de período ou aplicado o filtro |

| **Critérios de aceitação** |
| :------- |
| Deve ser aberta a seleção de período ou aplicado o filtro. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | Registro textual (respostas HTTP) | [BUG-006](../3-Relatorio-de-Bugs.md#bug-006) | Execução complementar — CT2-RF02-01 |

**Observação da execução:** Sem mudança na tela e sem requisição.

---
