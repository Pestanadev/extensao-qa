## Cenário 40: Perguntas de Anamnese.

**Tela:** `/perguntas-anamnese` · **Área:** Saúde · **Requisito:** [RF40](../1-Analise-de-requisitos.md#rf40)

### Caso de Teste 01: Perguntas — Nova pergunta.

| ID | Descrição |
| :------- | :------- |
| C40-CT01 | Verificar nova pergunta em Perguntas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Perguntas (`/perguntas-anamnese`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 12:30 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/902e3330-f85e-43b4-83c7-5d7283a39882) | [BUG-009](../3-Relatorio-de-Bugs.md#bug-009) | Equipe (vídeos JAM) — CT-31 do repositório anterior |

**Observação da execução:** Cadastro aceito (201×2); edição falhou: 500 e “Erro ao salvar pergunta” a 0:32.

---

### Caso de Teste 02: Perguntas — Exclusão.

| ID | Descrição |
| :------- | :------- |
| C40-CT02 | Verificar exclusão em Perguntas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Perguntas (`/perguntas-anamnese`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 12:33 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8e5dbe98-c990-4219-b190-daf4249875c5) | — | Equipe (vídeos JAM) — CT-32 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---

### Caso de Teste 03: Perguntas — Consulta e edição.

| ID | Descrição |
| :------- | :------- |
| C40-CT03 | Verificar consulta e edição em Perguntas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Perguntas (`/perguntas-anamnese`) |
| **QUANDO** pesquisamos o registro pelos filtros disponíveis |
| **E** alteramos dados do registro e salvamos |
| **ENTÃO** a listagem deve exibir os registros que atendem ao filtro |
| **E** as alterações devem ser mantidas após salvar |

| **Critérios de aceitação** |
| :------- |
| A listagem deve exibir os registros que atendem ao filtro. |
| As alterações devem ser mantidas após salvar. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 12:34 | sifitalfa | Reprovado | [Vídeo (Jam)](https://jam.dev/c/d53c5739-725c-4eae-8b83-f6b6b072bd51) | [BUG-009](../3-Relatorio-de-Bugs.md#bug-009) | Equipe (vídeos JAM) — CT-33 do repositório anterior |

**Observação da execução:** Edição falhou com 500 (formulário em salvamento a 0:09).

---
