## Cenário 37: Fichas de Anamnese.

**Tela:** `/anamneses` · **Área:** Saúde · **Requisito:** [RF37](../1-Analise-de-requisitos.md#rf37)

### Caso de Teste 01: Fichas de Análise — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C37-CT01 | Verificar cadastro em Fichas de Análise. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Fichas de Análise (`/anamneses`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:19 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/6ecb6761-b8df-4203-becc-7bbc1417f032) | — | Equipe (vídeos JAM) — CT-41 do repositório anterior |

**Observação da execução:** Ficha criada (201×2).

---
