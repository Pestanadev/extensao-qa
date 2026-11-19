## Cenário 31: Fornecedores.

**Tela:** `/fornecedores` · **Área:** Gestão · **Requisito:** [RF31](../1-Analise-de-requisitos.md#rf31)

### Caso de Teste 01: Fornecedores — Cadastro, edição e exclusão.

| ID | Descrição |
| :------- | :------- |
| C31-CT01 | Verificar cadastro, edição e exclusão em Fornecedores. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Fornecedores (`/fornecedores`) |
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
| 15/11/2026 13:32 | sifitalfa | Reprovado | [Vídeo (Jam)](https://jam.dev/c/f1d55cef-7804-435b-a5e0-f4b87c32bb39) | [BUG-011](../3-Relatorio-de-Bugs.md#bug-011) | Equipe (vídeos JAM) — CT-47 do repositório anterior |

**Observação da execução:** Cadastro falhou com 500 repetido; lista permaneceu com 8 registros; edição e exclusão não comprovadas.

---
