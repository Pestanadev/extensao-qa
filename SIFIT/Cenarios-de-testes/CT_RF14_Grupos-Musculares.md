## Cenário 14: Grupos Musculares.

**Tela:** `/grupos-musculares` · **Área:** Treinamento · **Requisito:** [RF14](../1-Analise-de-requisitos.md#rf14)

### Caso de Teste 01: Grupos Musculares — Cadastro, consulta e edição.

| ID | Descrição |
| :------- | :------- |
| C14-CT01 | Verificar cadastro, consulta e edição em Grupos Musculares. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Grupos Musculares (`/grupos-musculares`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** pesquisamos o registro pelos filtros disponíveis |
| **E** alteramos dados do registro e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** a listagem deve exibir os registros que atendem ao filtro |
| **E** as alterações devem ser mantidas após salvar |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| A listagem deve exibir os registros que atendem ao filtro. |
| As alterações devem ser mantidas após salvar. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 18:07 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/6aee3782-c54d-4a79-8a42-55bd50d0c8df) | [BUG-014](../3-Relatorio-de-Bugs.md#bug-014) | Equipe (vídeos JAM) — CT-62 do repositório anterior |

**Observação da execução:** Cadastro aceito (201); edição com imagem: 400 e “Erro ao salvar grupo”.

---

### Caso de Teste 02: Grupos Musculares — Exclusão.

| ID | Descrição |
| :------- | :------- |
| C14-CT02 | Verificar exclusão em Grupos Musculares. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Grupos Musculares (`/grupos-musculares`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 18:08 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/ef33cef8-c4d8-435d-b873-01a664f2c32b) | — | Equipe (vídeos JAM) — CT-63 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---
