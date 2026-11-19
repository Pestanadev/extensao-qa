## Cenário 17: Turmas.

**Tela:** `/turmas` · **Área:** Treinamento · **Requisito:** [RF17](../1-Analise-de-requisitos.md#rf17)

### Caso de Teste 01: Turmas — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C17-CT01 | Verificar cadastro em Turmas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Turmas (`/turmas`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:53 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/6101c380-ae54-41d2-b1f2-7ac3920288ea) | — | Equipe (vídeos JAM) — CT-51 do repositório anterior |

**Observação da execução:** Turma criada (201×2).

---

### Caso de Teste 02: Turmas — Exclusão e consultas.

| ID | Descrição |
| :------- | :------- |
| C17-CT02 | Verificar exclusão e consultas em Turmas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Turmas (`/turmas`) |
| **QUANDO** pesquisamos o registro pelos filtros disponíveis |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** a listagem deve exibir os registros que atendem ao filtro |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| A listagem deve exibir os registros que atendem ao filtro. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:54 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8c18cb4d-08e6-4fbf-b82e-d07efdd1fd9b) | — | Equipe (vídeos JAM) — CT-52 do repositório anterior |

**Observação da execução:** Exclusão e consulta sem erro (2xx).

---
