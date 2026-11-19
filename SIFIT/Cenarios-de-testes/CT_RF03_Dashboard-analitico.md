## Cenário 03: Dashboard analítico.

**Tela:** `/dash` · **Área:** Principal · **Requisito:** [RF03](../1-Analise-de-requisitos.md#rf03)

### Caso de Teste 01: Identificar corretamente o Dashboard.

| ID | Descrição |
| :------- | :------- |
| C03-CT01 | Identificar corretamente o Dashboard. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Dashboard analítico (`/dash`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Dashboard analítico do SIFIT |
| **QUANDO** abrir o item Dashboard (/dash); conferir título e item selecionado |
| **ENTÃO** o título deve identificar Dashboard ou o painel analítico, sem indicar Despesas Fixas |

| **Critérios de aceitação** |
| :------- |
| O título deve identificar Dashboard ou o painel analítico, sem indicar Despesas Fixas. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/BUG-002-dashboard-titulo.png) | [BUG-002](../3-Relatorio-de-Bugs.md#bug-002) | Exploração local — CT-RF03-01 |

**Observação da execução:** /dash exibiu título Despesas Fixas.

---
