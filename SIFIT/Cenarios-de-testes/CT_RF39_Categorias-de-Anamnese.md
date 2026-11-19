## Cenário 39: Categorias de Anamnese.

**Tela:** `/anamnese/categorias` · **Área:** Saúde · **Requisito:** [RF39](../1-Analise-de-requisitos.md#rf39)

### Caso de Teste 01: Categorias — Nova categoria.

| ID | Descrição |
| :------- | :------- |
| C39-CT01 | Verificar nova categoria em Categorias. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Categorias (`/anamnese/categorias`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 12:36 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/fa77ae9d-c3cf-4924-a01d-f924803708c5) | — | Equipe (vídeos JAM) — CT-34 do repositório anterior |

**Observação da execução:** Categoria criada (201×2).

---

### Caso de Teste 02: Categorias — Exclusão.

| ID | Descrição |
| :------- | :------- |
| C39-CT02 | Verificar exclusão em Categorias. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Categorias (`/anamnese/categorias`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 12:37 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8fc13646-0334-4b05-9499-3fff4e0c539a) | — | Equipe (vídeos JAM) — CT-35 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---

### Caso de Teste 03: Categorias — Consulta e edição.

| ID | Descrição |
| :------- | :------- |
| C39-CT03 | Verificar consulta e edição em Categorias. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Categorias (`/anamnese/categorias`) |
| **QUANDO** pesquisamos o registro pelos filtros disponíveis |
| **E** alteramos dados do registro e salvamos |
| **ENTÃO** a listagem deve exibir os registros que atendem ao filtro |
| **E** as alterações devem ser mantidas após salvar |

| **Critérios de aceitação** |
| :------- |
| A listagem deve exibir os registros que atendem ao filtro. |
| As alterações devem ser mantidas após salvar. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 12:37 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/6f4b42ba-8895-4375-af7e-fe3b1ce8a0cf) | — | Equipe (vídeos JAM) — CT-36 do repositório anterior |

**Observação da execução:** Consulta e edição sem erro (2xx).

---
