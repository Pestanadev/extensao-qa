## Cenário 06: SifitBox — aulas.

**Tela:** `/sifitbox/aulas` · **Área:** Principal · **Requisito:** [RF06](../1-Analise-de-requisitos.md#rf06)

### Caso de Teste 01: Acessar aulas do SifitBox.

| ID | Descrição |
| :------- | :------- |
| C06-CT01 | Acessar aulas do SifitBox. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela SifitBox — Aulas |
| **QUANDO** acessamos a lista de aulas do período |
| **ENTÃO** as aulas do período devem ser listadas |

| **Critérios de aceitação** |
| :------- |
| As aulas do período devem ser listadas. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Bloqueado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF06-01 |

**Observação da execução:** “Acesso negado — Modulo SifitBox nao habilitado para esta empresa”.

---
