## Cenário 29: Colaboradores.

**Tela:** `/colaboradores` · **Área:** Gestão · **Requisito:** [RF29](../1-Analise-de-requisitos.md#rf29)

### Caso de Teste 01: Colaboradores — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C29-CT01 | Verificar cadastro em Colaboradores. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Colaboradores (`/colaboradores`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:38 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/705c5e7b-2c39-4514-94d1-237ba03da5ad) | — | Equipe (vídeos JAM) — CT-49 do repositório anterior |

**Observação da execução:** Colaborador criado (201×2).

---

### Caso de Teste 02: Colaboradores — Edição e exclusão.

| ID | Descrição |
| :------- | :------- |
| C29-CT02 | Verificar edição e exclusão em Colaboradores. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Colaboradores (`/colaboradores`) |
| **QUANDO** alteramos dados do registro e salvamos |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** as alterações devem ser mantidas após salvar |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| As alterações devem ser mantidas após salvar. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:39 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/cfbf52d0-5468-438c-b895-0c71fadde4ad) | — | Equipe (vídeos JAM) — CT-50 do repositório anterior |

**Observação da execução:** Edição e exclusão sem erro (2xx).

---
