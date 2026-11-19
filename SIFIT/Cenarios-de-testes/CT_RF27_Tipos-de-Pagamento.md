## Cenário 27: Tipos de Pagamento.

**Tela:** `/tipos-pagamento` · **Área:** Comercial · **Requisito:** [RF27](../1-Analise-de-requisitos.md#rf27)

### Caso de Teste 01: Tipos de Pagamento — Cadastro, consulta, edição e exclusão.

| ID | Descrição |
| :------- | :------- |
| C27-CT01 | Verificar cadastro, consulta, edição e exclusão em Tipos de Pagamento. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Tipos de Pagamento (`/tipos-pagamento`) |
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
| 15/11/2026 13:58 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/e3b4b3f5-be92-48a3-9270-81dd0d63c80c) | — | Equipe (vídeos JAM) — CT-54 do repositório anterior |

**Observação da execução:** Tipo criado (201×2), consultado, editado e excluído.

---
