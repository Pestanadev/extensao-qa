## Cenário 44: Modelos de Ficha.

**Tela:** `/fichas-treino-modelo` · **Área:** Configurações · **Requisito:** [RF44](../1-Analise-de-requisitos.md#rf44)

### Caso de Teste 01: Treinos — Cadastro de Modelo de Ficha (Novo Modelo de Ficha > Criar Modelo).

| ID | Descrição |
| :------- | :------- |
| C44-CT01 | Verificar cadastro de Modelo de Ficha (Novo Modelo de Ficha > Criar Modelo) em Treinos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Treinos (`/fichas-treino-modelo`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 15:53 | sifitalfa | Reprovado | [Vídeo (Jam)](https://jam.dev/c/645a3706-aa9e-4724-b4bb-6b7badb33e92) | [BUG-007](../3-Relatorio-de-Bugs.md#bug-007) | Equipe (vídeos JAM) — CT-12 do repositório anterior |

**Observação da execução:** 400 e “Erro ao salvar modelo”.

---
