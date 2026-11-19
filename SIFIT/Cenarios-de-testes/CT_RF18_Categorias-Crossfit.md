## Cenário 18: Categorias Crossfit.

**Tela:** `/categorias-exercicios-crossfit` · **Área:** Treinamento · **Requisito:** [RF18](../1-Analise-de-requisitos.md#rf18)

### Caso de Teste 01: Categorias de Crossfit — Cadastro, edição, consulta e exclusão.

| ID | Descrição |
| :------- | :------- |
| C18-CT01 | Verificar cadastro, edição, consulta e exclusão em Categorias de Crossfit. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Categorias de Crossfit (`/categorias-exercicios-crossfit`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** pesquisamos o registro pelos filtros disponíveis |
| **E** alteramos dados do registro e salvamos |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** a listagem deve exibir os registros que atendem ao filtro |
| **E** as alterações devem ser mantidas após salvar |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| A listagem deve exibir os registros que atendem ao filtro. |
| As alterações devem ser mantidas após salvar. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 14:15 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/1df6ae82-8043-4ed1-b6e9-89c5ddc370d4) | — | Equipe (vídeos JAM) — CT-60 do repositório anterior |

**Observação da execução:** Categoria criada (201×2), editada e excluída.

---
