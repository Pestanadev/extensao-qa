## Cenário 21: Pagar.me.

**Tela:** `/pagarme` · **Área:** Financeiro · **Requisito:** [RF21](../1-Analise-de-requisitos.md#rf21)

### Caso de Teste 01: Financeiro — Pagar.me - solicitação de saque.

| ID | Descrição |
| :------- | :------- |
| C21-CT01 | Verificar pagar.me - solicitação de saque em Financeiro. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Financeiro (`/pagarme`) |
| **QUANDO** solicitamos um saque com valor de teste |
| **ENTÃO** deve ser exibida a confirmação ou a resposta do gateway Pagar.me |

| **Critérios de aceitação** |
| :------- |
| Deve ser exibida a confirmação ou a resposta do gateway Pagar.me. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 15:57 | sifitalfa | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/f8f35850-c834-4a33-ac10-6aebb905b4d2) | — | Equipe (vídeos JAM) — CT-11 do repositório anterior |

**Observação da execução:** Solicitação de saque com respostas 2xx; efeito no gateway não verificável.

---
