## Cenário 15: Objetivos Treino.

**Tela:** `/objetivos-treino` · **Área:** Treinamento · **Requisito:** [RF15](../1-Analise-de-requisitos.md#rf15)

### Caso de Teste 01: Objetivos de Treino — Cadastro, alteração e exclusão.

| ID | Descrição |
| :------- | :------- |
| C15-CT01 | Verificar cadastro, alteração e exclusão em Objetivos de Treino. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Objetivos de Treino (`/objetivos-treino`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** alteramos dados do registro e salvamos |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** as alterações devem ser mantidas após salvar |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| As alterações devem ser mantidas após salvar. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 14:19 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/903fd7be-ddd7-4a4b-9f0d-a3bb5b9157a3) | — | Equipe (vídeos JAM) — CT-61 do repositório anterior |

**Observação da execução:** Cadastro (201) e exclusão visíveis (7→6); 400 sem mensagem visível.

---
