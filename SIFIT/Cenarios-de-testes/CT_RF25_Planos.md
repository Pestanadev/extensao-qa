## Cenário 25: Planos.

**Tela:** `/planos` · **Área:** Comercial · **Requisito:** [RF25](../1-Analise-de-requisitos.md#rf25)

### Caso de Teste 01: Planos — Cadastro, inativação, alteração e exclusão.

| ID | Descrição |
| :------- | :------- |
| C25-CT01 | Verificar cadastro, inativação, alteração e exclusão em Planos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Planos (`/planos`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** alteramos dados do registro e salvamos |
| **E** inativamos o registro |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** as alterações devem ser mantidas após salvar |
| **E** o status do registro deve passar a Inativo |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| As alterações devem ser mantidas após salvar. |
| O status do registro deve passar a Inativo. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 14:01 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/6ec365fc-5fee-4ebf-a9c4-cc8c42243f41) | [BUG-012](../3-Relatorio-de-Bugs.md#bug-012) | Equipe (vídeos JAM) — CT-56 do repositório anterior |

**Observação da execução:** Cadastro, inativação e alteração sem erro; exclusão: 500 e “Erro ao deletar Plano” a 0:57.

---
