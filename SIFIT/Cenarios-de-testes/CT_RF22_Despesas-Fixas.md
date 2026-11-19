## Cenário 22: Despesas Fixas.

**Tela:** `/despesas-fixas` · **Área:** Financeiro · **Requisito:** [RF22](../1-Analise-de-requisitos.md#rf22)

### Caso de Teste 01: Despesas Fixas — Cadastro, edição e exclusão.

| ID | Descrição |
| :------- | :------- |
| C22-CT01 | Verificar cadastro, edição e exclusão em Despesas Fixas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Despesas Fixas (`/despesas-fixas`) |
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
| 17/11/2026 20:05 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/573bcb6b-2dae-499f-9137-e9ee7a48167d) | [BUG-016](../3-Relatorio-de-Bugs.md#bug-016) | Equipe (vídeos JAM) — CT-72 do repositório anterior |

**Observação da execução:** 1º salvamento: 500 com “Salvando...” travado; cadastro concluído depois (201).

---
