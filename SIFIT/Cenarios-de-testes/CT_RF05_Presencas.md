## Cenário 05: Presenças.

**Tela:** `/presencas` · **Área:** Principal · **Requisito:** [RF05](../1-Analise-de-requisitos.md#rf05)

### Caso de Teste 01: Consultar presenças por período.

| ID | Descrição |
| :------- | :------- |
| C05-CT01 | Consultar presenças por período. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Presenças |
| **QUANDO** consultamos o período de 12/11 a 18/11/2026 |
| **E** aplicamos o atalho "Este mês" |
| **ENTÃO** devem ser listadas as presenças do período, coerentes com os check-ins confirmados |

| **Critérios de aceitação** |
| :------- |
| Devem ser listadas as presenças do período, coerentes com os check-ins confirmados. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Inconclusivo | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF05-01 |

**Observação da execução:** 0 presenças em 12–18/11 e no mês, mas o banco tem 25 check-ins confirmados desde 20/10.

---

### Caso de Teste 02: Aplicar filtro “Este mês”.

| ID | Descrição |
| :------- | :------- |
| C05-CT02 | Aplicar filtro “Este mês”. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Presenças |
| **QUANDO** clicamos em "Este mês" |
| **ENTÃO** o período deve ir de 01/11/2026 a 18/11/2026 |

| **Critérios de aceitação** |
| :------- |
| O período deve ir de 01/11/2026 a 18/11/2026. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | Registro textual (respostas HTTP) | [BUG-021](../3-Relatorio-de-Bugs.md#bug-021) | Execução complementar — CT2-RF05-02 |

**Observação da execução:** Aplicou 20/10–18/11 (30 dias).

---
