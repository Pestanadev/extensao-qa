## Cenário 20: Caixas.

**Tela:** `/caixas` · **Área:** Financeiro · **Requisito:** [RF20](../1-Analise-de-requisitos.md#rf20)

### Caso de Teste 01: Caixas — Cadastro, consulta e edição.

| ID | Descrição |
| :------- | :------- |
| C20-CT01 | Verificar cadastro, consulta e edição em Caixas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Caixas (`/caixas`) |
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
| 17/11/2026 18:24 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8031915b-199c-4103-81c8-1a9dcdb5d335) | — | Equipe (vídeos JAM) — CT-70 do repositório anterior |

**Observação da execução:** 423 corresponde à regra de caixa fechado (ajuste administrativo).

---
