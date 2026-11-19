## Cenário 28: Bandeiras.

**Tela:** `/bandeiras` · **Área:** Comercial · **Requisito:** [RF28](../1-Analise-de-requisitos.md#rf28)

### Caso de Teste 01: Bandeiras de Cartão — Cadastro.

| ID | Descrição |
| :------- | :------- |
| C28-CT01 | Verificar cadastro em Bandeiras de Cartão. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Bandeiras de Cartão (`/bandeiras`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 12:24 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/e25b0150-92e4-4976-bddf-23e8dca8e6b3) | [BUG-010](../3-Relatorio-de-Bugs.md#bug-010) | Equipe (vídeos JAM) — CT-30 do repositório anterior |

**Observação da execução:** Cadastro com 201×2; a listagem de bandeiras não exibe registros (reproduzido em 18/11).

---

### Caso de Teste 02: Bandeiras de Cartão — Cadastro e consulta.

| ID | Descrição |
| :------- | :------- |
| C28-CT02 | Verificar cadastro e consulta em Bandeiras de Cartão. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Bandeiras de Cartão (`/bandeiras`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** pesquisamos o registro pelos filtros disponíveis |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** a listagem deve exibir os registros que atendem ao filtro |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| A listagem deve exibir os registros que atendem ao filtro. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:55 | sifitalfa | Reprovado | [Vídeo (Jam)](https://jam.dev/c/03c675ab-9995-473c-98d6-b443636466bf) | [BUG-010](../3-Relatorio-de-Bugs.md#bug-010) | Equipe (vídeos JAM) — CT-53 do repositório anterior |

**Observação da execução:** 500 ao salvar “master”; consulta posterior: “Nenhuma bandeira encontrada”.

---

### Caso de Teste 03: Cadastrar bandeira e localizá-la.

| ID | Descrição |
| :------- | :------- |
| C28-CT03 | Cadastrar bandeira e localizá-la. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Bandeiras de Cartão |
| **QUANDO** cadastramos a bandeira "QA Bandeira 1118" |
| **ENTÃO** a bandeira deve ser listada |

| **Critérios de aceitação** |
| :------- |
| A bandeira deve ser listada. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | Registro textual (respostas HTTP) | [BUG-010](../3-Relatorio-de-Bugs.md#bug-010) | Execução complementar — CT2-RF28-01 |

**Observação da execução:** 201, mas lista vazia; status nulo no banco.

---
