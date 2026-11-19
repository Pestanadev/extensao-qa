## Cenário 16: Grupos.

**Tela:** `/grupos` · **Área:** Treinamento · **Requisito:** [RF16](../1-Analise-de-requisitos.md#rf16)

### Caso de Teste 01: Grupos — Cadastro, consulta, inativação e exclusão.

| ID | Descrição |
| :------- | :------- |
| C16-CT01 | Verificar cadastro, consulta, inativação e exclusão em Grupos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Grupos (`/grupos`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** pesquisamos o registro pelos filtros disponíveis |
| **E** inativamos o registro |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** a listagem deve exibir os registros que atendem ao filtro |
| **E** o status do registro deve passar a Inativo |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| A listagem deve exibir os registros que atendem ao filtro. |
| O status do registro deve passar a Inativo. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 14:03 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/484df916-a8fd-4159-9528-4334f8919d80) | [BUG-013](../3-Relatorio-de-Bugs.md#bug-013) | Equipe (vídeos JAM) — CT-57 do repositório anterior |

**Observação da execução:** Cadastro concluído (12→13); exclusão: 500 e “Erro ao deletar Grupo” (reproduzido em 18/11).

---

### Caso de Teste 02: Cadastrar grupo (sonda).

| ID | Descrição |
| :------- | :------- |
| C16-CT02 | Cadastrar grupo (sonda). |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Grupos |
| **QUANDO** cadastramos o grupo "SONDA-QA-1118" |
| **ENTÃO** o grupo deve ser listado e gravado no banco |

| **Critérios de aceitação** |
| :------- |
| O grupo deve ser listado e gravado no banco. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | [Captura](../evidencias/imagens/SONDA-04-grupo-presente-no-banco-sifit-alfa.jpg) | — | Execução complementar — CT2-RF16-01 |

**Observação da execução:** Grupo #12 “SONDA-QA-1118”; 201; presente no banco.

---

### Caso de Teste 03: Excluir grupo sem vínculos.

| ID | Descrição |
| :------- | :------- |
| C16-CT03 | Excluir grupo sem vínculos. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Grupos |
| **QUANDO** excluímos o grupo de teste, sem vínculos |
| **E** confirmamos a exclusão |
| **ENTÃO** o grupo deve ser removido |

| **Critérios de aceitação** |
| :------- |
| O grupo deve ser removido. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/SONDA-03-erro-ao-deletar-grupo.jpg) | [BUG-013](../3-Relatorio-de-Bugs.md#bug-013) | Execução complementar — CT2-RF16-02 |

**Observação da execução:** 500 “Erro ao deletar Grupo”.

---
