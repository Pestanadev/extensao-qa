## Cenário 45: Aplicativo.

**Tela:** `/aplicativo` · **Área:** Configurações · **Requisito:** [RF45](../1-Analise-de-requisitos.md#rf45)

### Caso de Teste 01: Aplicativo — Notificações.

| ID | Descrição |
| :------- | :------- |
| C45-CT01 | Verificar notificações em Aplicativo. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Aplicativo (`/aplicativo`) |
| **QUANDO** executamos a ação descrita no cenário |
| **ENTÃO** o sistema deve responder conforme o esperado |

| **Critérios de aceitação** |
| :------- |
| O sistema deve responder conforme o esperado. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 15:51 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/f0dcb321-e13b-492c-9cc1-386a56f2db35) | — | Equipe (vídeos JAM) — CT-28 do repositório anterior |

**Observação da execução:** Notificação criada (201).

---

### Caso de Teste 02: Aplicativo — Exclusão de notificação.

| ID | Descrição |
| :------- | :------- |
| C45-CT02 | Verificar exclusão de notificação em Aplicativo. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Aplicativo (`/aplicativo`) |
| **QUANDO** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 15:51 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/47886dbd-22c5-4699-ae62-71be6cc8fd32) | — | Equipe (vídeos JAM) — CT-29 do repositório anterior |

**Observação da execução:** Exclusão sem erro (2xx).

---
