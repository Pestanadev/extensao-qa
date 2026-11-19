## Cenário 32: Tipos de Documentos.

**Tela:** `/tipos-documento` · **Área:** Gestão · **Requisito:** [RF32](../1-Analise-de-requisitos.md#rf32)

### Caso de Teste 01: Tipos de Documentos — Cadastro e alteração.

| ID | Descrição |
| :------- | :------- |
| C32-CT01 | Verificar cadastro e alteração em Tipos de Documentos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Tipos de Documentos (`/tipos-documento`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** alteramos dados do registro e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** as alterações devem ser mantidas após salvar |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| As alterações devem ser mantidas após salvar. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:26 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/24c28488-384b-4401-8963-b81d4da1b59d) | — | Equipe (vídeos JAM) — CT-45 do repositório anterior |

**Observação da execução:** Tipo criado (201×2) e alterado.

---

### Caso de Teste 02: Tipos de Documentos — Exclusão.

| ID | Descrição |
| :------- | :------- |
| C32-CT02 | Verificar exclusão em Tipos de Documentos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Tipos de Documentos (`/tipos-documento`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:27 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/a92d0c75-1b14-494f-9045-176bb441a869) | — | Equipe (vídeos JAM) — CT-46 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---
