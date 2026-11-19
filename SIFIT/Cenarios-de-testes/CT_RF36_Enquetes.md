## Cenário 36: Enquetes.

**Tela:** `/enquetes` · **Área:** Gestão · **Requisito:** [RF36](../1-Analise-de-requisitos.md#rf36)

### Caso de Teste 01: Enquetes — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C36-CT01 | Verificar cadastro em Enquetes. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Enquetes (`/enquetes`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:21 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/5d07fa69-a8d7-47fa-9814-6299d08ecbb4) | — | Equipe (vídeos JAM) — CT-42 do repositório anterior |

**Observação da execução:** Enquete salva sem erro (2xx).

---

### Caso de Teste 02: Enquetes — Inativação e exclusão.

| ID | Descrição |
| :------- | :------- |
| C36-CT02 | Verificar inativação e exclusão em Enquetes. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Enquetes (`/enquetes`) |
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
| 15/11/2026 13:23 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/24e0135a-e211-4f0a-b46f-79f3beaf3be9) | — | Equipe (vídeos JAM) — CT-43 do repositório anterior |

**Observação da execução:** Inativação e exclusão sem erro (2xx).

---
