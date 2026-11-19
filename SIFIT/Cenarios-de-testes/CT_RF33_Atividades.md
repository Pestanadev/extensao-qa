## Cenário 33: Atividades.

**Tela:** `/atividades` · **Área:** Gestão · **Requisito:** [RF33](../1-Analise-de-requisitos.md#rf33)

### Caso de Teste 01: Atividades — Nova atividade.

| ID | Descrição |
| :------- | :------- |
| C33-CT01 | Verificar nova atividade em Atividades. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Atividades (`/atividades`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:21 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/62ff8072-1a6c-4512-9525-4489f3f4a79b) | — | Equipe (vídeos JAM) — CT-24 do repositório anterior |

**Observação da execução:** Atividades criadas (201×3).

---

### Caso de Teste 02: Atividades — Exclusão de atividade.

| ID | Descrição |
| :------- | :------- |
| C33-CT02 | Verificar exclusão de atividade em Atividades. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Atividades (`/atividades`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:22 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/3ed505f2-30fb-4a63-9655-beba55acf23c) | — | Equipe (vídeos JAM) — CT-25 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---

### Caso de Teste 03: Atividades — Pesquisar atividade.

| ID | Descrição |
| :------- | :------- |
| C33-CT03 | Verificar pesquisar atividade em Atividades. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Atividades (`/atividades`) |
| **QUANDO** pesquisamos o registro pelos filtros disponíveis |
| **ENTÃO** a listagem deve exibir os registros que atendem ao filtro |

| **Critérios de aceitação** |
| :------- |
| A listagem deve exibir os registros que atendem ao filtro. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:23 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/2b06f310-4c2c-42b5-ab68-1fcf64411612) | — | Equipe (vídeos JAM) — CT-26 do repositório anterior |

**Observação da execução:** Pesquisa feita na própria tela, sem requisição.

---

### Caso de Teste 04: Validar nome obrigatório de atividade.

| ID | Descrição |
| :------- | :------- |
| C33-CT04 | Validar nome obrigatório de atividade. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Atividades |
| **QUANDO** abrimos "Nova Atividade" e salvamos sem preencher |
| **ENTÃO** o sistema deve exigir o nome da atividade |

| **Critérios de aceitação** |
| :------- |
| O sistema deve exigir o nome da atividade. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/EXE2-RF33-atividade-sem-nome-aceita.jpg) | [BUG-017](../3-Relatorio-de-Bugs.md#bug-017) | Execução complementar — CT2-RF33-01 |

**Observação da execução:** Atividade #10 salva sem nome (201).

---

### Caso de Teste 05: Alterar atividade.

| ID | Descrição |
| :------- | :------- |
| C33-CT05 | Alterar atividade. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Atividades |
| **QUANDO** alteramos a atividade de teste para "QA Atividade 1118" com pontuação 15 |
| **E** salvamos |
| **ENTÃO** a alteração deve ser exibida na listagem |

| **Critérios de aceitação** |
| :------- |
| A alteração deve ser exibida na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF33-02 |

**Observação da execução:** #10 alterada para “QA Atividade 1118”, pontuação 15; 200.

---

### Caso de Teste 06: Excluir atividade.

| ID | Descrição |
| :------- | :------- |
| C33-CT06 | Excluir atividade. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Atividades |
| **QUANDO** excluímos a atividade de teste e confirmamos |
| **ENTÃO** a atividade deve ser removida e o total atualizado |

| **Critérios de aceitação** |
| :------- |
| A atividade deve ser removida e o total atualizado. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF33-03 |

**Observação da execução:** `deletar-atividade` 200; total voltou a 8.

---
