## Cenário 13: Exercícios.

**Tela:** `/exercicios` · **Área:** Treinamento · **Requisito:** [RF13](../1-Analise-de-requisitos.md#rf13)

### Caso de Teste 01: Biblioteca de Exercícios — Cadastro, consulta e edição.

| ID | Descrição |
| :------- | :------- |
| C13-CT01 | Verificar cadastro, consulta e edição em Biblioteca de Exercícios. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Biblioteca de Exercícios (`/exercicios`) |
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
| 17/11/2026 18:10 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/d5d88e50-ae2a-4cae-8c14-719d9b9300be) | [BUG-014](../3-Relatorio-de-Bugs.md#bug-014) | Equipe (vídeos JAM) — CT-64 do repositório anterior |

**Observação da execução:** Cadastro aceito (201×3); salvamento com imagem: 400 ×3 e “Erro ao salvar exercício”.

---

### Caso de Teste 02: Biblioteca de Exercícios — Exclusão.

| ID | Descrição |
| :------- | :------- |
| C13-CT02 | Verificar exclusão em Biblioteca de Exercícios. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Biblioteca de Exercícios (`/exercicios`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 18:11 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/c31e86c3-e6c0-49b0-8243-d83bf909dedd) | — | Equipe (vídeos JAM) — CT-65 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---
