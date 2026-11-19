## Cenário 38: Modelos de Anamnese.

**Tela:** `/anamnese/modelos` · **Área:** Saúde · **Requisito:** [RF38](../1-Analise-de-requisitos.md#rf38)

### Caso de Teste 01: Modelos de Análise — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C38-CT01 | Verificar cadastro em Modelos de Análise. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Modelos de Análise (`/anamnese/modelos/novo`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:13 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/fe27eb69-fbd3-487d-80fd-e6f06253f99d) | — | Equipe (vídeos JAM) — CT-37 do repositório anterior |

**Observação da execução:** Modelo criado (201).

---

### Caso de Teste 02: Modelos de Análise — Exclusão.

| ID | Descrição |
| :------- | :------- |
| C38-CT02 | Verificar exclusão em Modelos de Análise. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Modelos de Análise (`/anamnese/modelos`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:14 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/468320db-cac1-4df6-89c1-eeffb6bd47e4) | — | Equipe (vídeos JAM) — CT-38 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---

### Caso de Teste 03: Modelos de Análise — Inativação.

| ID | Descrição |
| :------- | :------- |
| C38-CT03 | Verificar inativação em Modelos de Análise. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Modelos de Análise (`/anamnese/modelos`) |
| **QUANDO** inativamos o registro |
| **ENTÃO** o status do registro deve passar a Inativo |

| **Critérios de aceitação** |
| :------- |
| O status do registro deve passar a Inativo. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:14 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/e67ff75f-af66-4169-8b4d-6b20f41e5576) | — | Equipe (vídeos JAM) — CT-39 do repositório anterior |

**Observação da execução:** Inativação sem erro (2xx).

---

### Caso de Teste 04: Modelos de Análise — Consulta.

| ID | Descrição |
| :------- | :------- |
| C38-CT04 | Verificar consulta em Modelos de Análise. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Modelos de Análise (`/anamnese/modelos`) |
| **QUANDO** pesquisamos o registro pelos filtros disponíveis |
| **ENTÃO** a listagem deve exibir os registros que atendem ao filtro |

| **Critérios de aceitação** |
| :------- |
| A listagem deve exibir os registros que atendem ao filtro. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:15 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/421d76e9-1c7e-4d98-a39f-77db30f8e417) | — | Equipe (vídeos JAM) — CT-40 do repositório anterior |

**Observação da execução:** Consulta sem erro (2xx).

---
