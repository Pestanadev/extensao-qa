## Cenário 24: Prospecção.

**Tela:** `/prospeccao` · **Área:** Comercial · **Requisito:** [RF24](../1-Analise-de-requisitos.md#rf24)

### Caso de Teste 01: Prospecção — Cadastro, alteração e exclusão.

| ID | Descrição |
| :------- | :------- |
| C24-CT01 | Verificar cadastro, alteração e exclusão em Prospecção. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Prospecção (`/prospeccao`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** alteramos dados do registro e salvamos |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** as alterações devem ser mantidas após salvar |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| As alterações devem ser mantidas após salvar. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 14:05 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/1dfb1eb4-d3af-4361-9709-31d39274ca72) | — | Equipe (vídeos JAM) — CT-58 do repositório anterior |

**Observação da execução:** Cadastro, alteração e exclusão sem erro (2xx).

---
