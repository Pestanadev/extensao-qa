## Cenário 07: Clientes.

**Tela:** `/clientes` · **Área:** Operação · **Requisito:** [RF07](../1-Analise-de-requisitos.md#rf07)

### Caso de Teste 01: Tratar vencimento inválido no perfil.

| ID | Descrição |
| :------- | :------- |
| C07-CT01 | Tratar vencimento inválido no perfil. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Clientes (`/clientes`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Clientes do SIFIT |
| **QUANDO** abrir o cliente de teste com conta de data inválida; aguardar o financeiro do perfil |
| **ENTÃO** apresentar data válida ou indicação de data não informada; não formatar como 30/11/-0001 |

| **Critérios de aceitação** |
| :------- |
| Apresentar data válida ou indicação de data não informada; não formatar como 30/11/-0001. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/BUG-004-cliente-data.png) | [BUG-004](../3-Relatorio-de-Bugs.md#bug-004) | Exploração local — CT-RF07-08 |

**Observação da execução:** Perfil do registro de teste exibiu vencimento e próximo vencimento 30/11/-0001. Persistência/causa não verificadas.

---

### Caso de Teste 02: Validar obrigatórios do cadastro de cliente.

| ID | Descrição |
| :------- | :------- |
| C07-CT02 | Validar obrigatórios do cadastro de cliente. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Cadastrar Cliente |
| **QUANDO** clicamos em "Cadastrar Cliente" sem preencher os campos |
| **ENTÃO** deve ser exibida mensagem de campo obrigatório |
| **E** nenhum cliente deve ser criado |

| **Critérios de aceitação** |
| :------- |
| Deve ser exibida mensagem de campo obrigatório. |
| Nenhum cliente deve ser criado. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF07-01 |

**Observação da execução:** Salvar vazio exibiu “Preencha o nome da pessoa”.

---

### Caso de Teste 03: Cadastrar cliente com campos obrigatórios.

| ID | Descrição |
| :------- | :------- |
| C07-CT03 | Cadastrar cliente com campos obrigatórios. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Cadastrar Cliente |
| **QUANDO** preenchemos Nome "QA Cliente Teste 1118", Status Ativo, Sexo e Data de Nascimento 01/01/2000 |
| **E** clicamos em "Cadastrar Cliente" |
| **ENTÃO** o cliente deve ser salvo e listado |
| **E** o total de clientes deve aumentar em um |

| **Critérios de aceitação** |
| :------- |
| O cliente deve ser salvo e listado. |
| O total de clientes deve aumentar em um. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF07-02 |

**Observação da execução:** Cliente #440 “QA Cliente Teste 1118”; `cadastrar-cliente` 201; total 145→146.

---

### Caso de Teste 04: Consultar cliente por nome.

| ID | Descrição |
| :------- | :------- |
| C07-CT04 | Consultar cliente por nome. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Clientes |
| **QUANDO** pesquisamos pelo nome "QA Cliente" |
| **ENTÃO** o cliente de teste deve ser retornado |

| **Critérios de aceitação** |
| :------- |
| O cliente de teste deve ser retornado. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF07-03 |

**Observação da execução:** Busca por “QA Cliente” retornou o #440.

---

### Caso de Teste 05: Exibir perfil de cliente novo.

| ID | Descrição |
| :------- | :------- |
| C07-CT05 | Exibir perfil de cliente novo. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Visualizar Cliente |
| **QUANDO** abrimos o perfil do cliente recém-criado |
| **ENTÃO** campos não informados devem aparecer vazios ou como não informados |
| **E** não deve haver dados de demonstração |

| **Critérios de aceitação** |
| :------- |
| Campos não informados devem aparecer vazios ou como não informados. |
| Não deve haver dados de demonstração. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/EXE2-RF07-cliente-null-contato.jpg) | [BUG-020](../3-Relatorio-de-Bugs.md#bug-020) | Execução complementar — CT2-RF07-04 |

**Observação da execução:** “null” no contato e objetivos/progresso fictícios.

---

### Caso de Teste 06: Alterar dados do cliente.

| ID | Descrição |
| :------- | :------- |
| C07-CT06 | Alterar dados do cliente. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Alterar Cliente |
| **QUANDO** alteramos o nome para "QA Cliente Teste 1118 Editado" e o tipo sanguíneo para O+ |
| **E** clicamos em "Salvar Alterações" |
| **ENTÃO** as alterações devem ser exibidas e mantidas |

| **Critérios de aceitação** |
| :------- |
| As alterações devem ser exibidas e mantidas. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF07-05 |

**Observação da execução:** `atualizar-cliente` 200; nome “... Editado” e tipo sanguíneo O+ conferidos no banco.

---

### Caso de Teste 07: Excluir cliente com matrícula cancelada.

| ID | Descrição |
| :------- | :------- |
| C07-CT07 | Excluir cliente com matrícula cancelada. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Clientes |
| **QUANDO** excluímos o cliente de teste, que possui matrícula cancelada |
| **E** confirmamos a exclusão |
| **ENTÃO** o cliente deve ser excluído ou deve ser exibida a regra que impede a exclusão, sem erro interno |

| **Critérios de aceitação** |
| :------- |
| O cliente deve ser excluído ou deve ser exibida a regra que impede a exclusão, sem erro interno. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/EXE2-RF07-erro-500-excluir-cliente.jpg) | [BUG-019](../3-Relatorio-de-Bugs.md#bug-019) | Execução complementar — CT2-RF07-06 |

**Observação da execução:** 500 “Erro interno inesperado”.

---
