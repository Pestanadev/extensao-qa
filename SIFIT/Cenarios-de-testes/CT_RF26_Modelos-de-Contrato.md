## Cenário 26: Modelos de Contrato.

**Tela:** `/modelos-contrato` · **Área:** Comercial · **Requisito:** [RF26](../1-Analise-de-requisitos.md#rf26)

### Caso de Teste 01: Modelos de Contrato — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C26-CT01 | Verificar cadastro em Modelos de Contrato. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Modelos de Contrato (`/modelos-contrato`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:59 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/1b30c3cf-8100-47c6-b4f3-a42340197fbe) | — | Equipe (vídeos JAM) — CT-55 do repositório anterior |

**Observação da execução:** Modelo criado (201).

---
