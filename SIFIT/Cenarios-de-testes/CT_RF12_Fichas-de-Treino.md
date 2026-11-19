## Cenário 12: Fichas de Treino.

**Tela:** `/fichas-treino` · **Área:** Treinamento · **Requisito:** [RF12](../1-Analise-de-requisitos.md#rf12)

### Caso de Teste 01: Fichas de Treino — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C12-CT01 | Verificar cadastro em Fichas de Treino. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Fichas de Treino (`/fichas-treino`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 18:13 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/bdb3fe53-a12a-49a1-a545-948ff43a715b) | — | Equipe (vídeos JAM) — CT-66 do repositório anterior |

**Observação da execução:** Ficha criada (201).

---

### Caso de Teste 02: Fichas de Treino — Inativação e exclusão.

| ID | Descrição |
| :------- | :------- |
| C12-CT02 | Verificar inativação e exclusão em Fichas de Treino. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Fichas de Treino (`/ficha-treino/alterar/4`) |
| **QUANDO** inativamos o registro |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o status do registro deve passar a Inativo |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O status do registro deve passar a Inativo. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 18:14 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/84037d7e-56f9-41cd-8dec-17f9bcb06ab1) | — | Equipe (vídeos JAM) — CT-67 do repositório anterior |

**Observação da execução:** Inativação e exclusão sem erro (2xx).

---
