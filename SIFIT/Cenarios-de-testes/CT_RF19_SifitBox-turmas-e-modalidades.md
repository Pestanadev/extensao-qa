## Cenário 19: SifitBox — turmas e modalidades.

**Tela:** `/sifitbox/turmas` · **Área:** Treinamento · **Requisito:** [RF19](../1-Analise-de-requisitos.md#rf19)

### Caso de Teste 01: Turmas — SifitBox - cadastro de turma.

| ID | Descrição |
| :------- | :------- |
| C19-CT01 | Verificar sifitBox - cadastro de turma em Turmas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Turmas (`/sifitbox/turmas`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 14:07 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/8016aa6c-0813-48e2-a73b-ee93378894ac) | — | Equipe (vídeos JAM) — CT-59 do repositório anterior |

**Observação da execução:** Turma SifitBox criada (201×2).

---
