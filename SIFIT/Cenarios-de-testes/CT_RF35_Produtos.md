## Cenário 35: Produtos.

**Tela:** `/produtos` · **Área:** Gestão · **Requisito:** [RF35](../1-Analise-de-requisitos.md#rf35)

### Caso de Teste 01: Produtos — Novo produto.

| ID | Descrição |
| :------- | :------- |
| C35-CT01 | Verificar novo produto em Produtos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Produtos (`/produtos`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 17:28 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/1a2f5a18-65fa-4145-9072-d1cb973fdce1) | — | Equipe (vídeos JAM) — CT-27 do repositório anterior |

**Observação da execução:** 1ª tentativa: 400 e “Erro ao salvar produto” (mensagem genérica); cadastro concluído depois (201×2).

---

### Caso de Teste 02: Produtos — Inativação e exclusão.

| ID | Descrição |
| :------- | :------- |
| C35-CT02 | Verificar inativação e exclusão em Produtos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Produtos (`/produtos`) |
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
| 15/11/2026 13:24 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/34982376-5d60-40bc-b361-6d812a5d4fdc) | — | Equipe (vídeos JAM) — CT-44 do repositório anterior |

**Observação da execução:** Inativação e exclusão sem erro (2xx).

---
