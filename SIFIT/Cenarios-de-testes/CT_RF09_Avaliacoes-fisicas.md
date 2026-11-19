## Cenário 09: Avaliações físicas.

**Tela:** `/avaliacoes` · **Área:** Operação · **Requisito:** [RF09](../1-Analise-de-requisitos.md#rf09)

### Caso de Teste 01: Calcular IMC na interface sem salvar.

| ID | Descrição |
| :------- | :------- |
| C09-CT01 | Calcular IMC na interface sem salvar. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Avaliações físicas (`/avaliacoes`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Avaliações físicas do SIFIT |
| **QUANDO** abrir Fazer Avaliação de registro de teste; na aba IMC informar altura 1,75 e peso 70; sair do campo e observar; cancelar |
| **ENTÃO** calcular 70 / (1,75 × 1,75), aproximadamente 22,857142857. Não persistir as medidas |

| **Critérios de aceitação** |
| :------- |
| Calcular 70 / (1,75 × 1,75), aproximadamente 22,857142857. Não persistir as medidas. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | [Captura](../evidencias/imagens/BUG-003-imc-unidade.png) | — | Exploração local — CT-RF09-08 |

**Observação da execução:** 1,75 m e 70 kg resultaram em 22.857142857142858 na interface; operação cancelada.

---

### Caso de Teste 02: Exibir unidade correta do IMC.

| ID | Descrição |
| :------- | :------- |
| C09-CT02 | Exibir unidade correta do IMC. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Avaliações físicas (`/avaliacoes`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Avaliações físicas do SIFIT |
| **QUANDO** abrir Fazer Avaliação e conferir o rótulo de IMC |
| **ENTÃO** identificar kg/m², compatível com peso dividido pelo quadrado da altura |

| **Critérios de aceitação** |
| :------- |
| Identificar kg/m², compatível com peso dividido pelo quadrado da altura. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/BUG-003-imc-unidade.png) | [BUG-003](../3-Relatorio-de-Bugs.md#bug-003) | Exploração local — CT-RF09-09 |

**Observação da execução:** Rótulo apresentou IMC kg/m³.

---

### Caso de Teste 03: Avaliações — Cadastro, consulta, edição e exclusão.

| ID | Descrição |
| :------- | :------- |
| C09-CT03 | Verificar cadastro, consulta, edição e exclusão em Avaliações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Avaliações (`/avaliacoes`) |
| **QUANDO** cadastramos um novo registro com dados de teste e salvamos |
| **E** pesquisamos o registro pelos filtros disponíveis |
| **E** alteramos dados do registro e salvamos |
| **E** excluímos o registro e confirmamos a exclusão |
| **ENTÃO** o registro deve ser salvo e exibido na listagem |
| **E** a listagem deve exibir os registros que atendem ao filtro |
| **E** as alterações devem ser mantidas após salvar |
| **E** o registro deve deixar de ser exibido na listagem |

| **Critérios de aceitação** |
| :------- |
| O registro deve ser salvo e exibido na listagem. |
| A listagem deve exibir os registros que atendem ao filtro. |
| As alterações devem ser mantidas após salvar. |
| O registro deve deixar de ser exibido na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 18:27 | sifitalfa | Parcial | [Vídeo (Jam)](https://jam.dev/c/364850dc-8240-4fee-9169-465b5a9ef048) | [BUG-015](../3-Relatorio-de-Bugs.md#bug-015) | Equipe (vídeos JAM) — CT-71 do repositório anterior |

**Observação da execução:** Avaliação criada (201×2); salvamento posterior: 500 (“Salvando...” a 0:45).

---
