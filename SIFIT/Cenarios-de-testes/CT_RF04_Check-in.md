## Cenário 04: Check-in.

**Tela:** `/checkin` · **Área:** Principal · **Requisito:** [RF04](../1-Analise-de-requisitos.md#rf04)

### Caso de Teste 01: Dashboard — Check-in.

| ID | Descrição |
| :------- | :------- |
| C04-CT01 | Verificar check-in em Dashboard. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Dashboard (`/checkin`) |
| **QUANDO** registramos o check-in de um aluno |
| **ENTÃO** o check-in deve ser salvo e exibido na lista do dia |

| **Critérios de aceitação** |
| :------- |
| O check-in deve ser salvo e exibido na lista do dia. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 17:14 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/79d6a37a-eae8-44ed-8109-ca23cb0b0460) | — | Equipe (vídeos JAM) — CT-05 do repositório anterior |

**Observação da execução:** Check-in registrado (201) e exibido na lista.

---
