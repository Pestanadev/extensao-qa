## Cenário 08: Matrículas.

**Tela:** `/matriculas` · **Área:** Operação · **Requisito:** [RF08](../1-Analise-de-requisitos.md#rf08)

### Caso de Teste 01: Preencher matrícula por diária sem salvar.

| ID | Descrição |
| :------- | :------- |
| C08-CT01 | Preencher matrícula por diária sem salvar. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Matrículas (`/matriculas`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Matrículas do SIFIT |
| **QUANDO** abrir /adicionar-matricula; pesquisar e selecionar aluno de teste; escolher Plano Diário existente com valor 20,00; observar datas e valores; descartar sem salvar |
| **ENTÃO** parcela e total 20,00, término no mesmo dia para essa configuração; não exigir vencimento mensal. A persistência não faz parte deste caso |

| **Critérios de aceitação** |
| :------- |
| Parcela e total 20,00, término no mesmo dia para essa configuração; não exigir vencimento mensal. A persistência não faz parte deste caso. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | Registro textual | — | Exploração local — CT-RF08-08 |

**Observação da execução:** Plano Diário preencheu parcela e total 20,00, término no mesmo dia e ocultou Dia Vencimento; formulário descartado sem salvar.

---

### Caso de Teste 02: Consultar matrículas.

| ID | Descrição |
| :------- | :------- |
| C08-CT02 | Consultar matrículas. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Matrículas |
| **QUANDO** abrimos a tela de matrículas |
| **ENTÃO** indicadores e lista devem ser carregados |

| **Critérios de aceitação** |
| :------- |
| Indicadores e lista devem ser carregados. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF08-01 |

**Observação da execução:** Indicadores e lista carregados (9 ativas, 61 não renovadas).

---

### Caso de Teste 03: Cadastrar matrícula.

| ID | Descrição |
| :------- | :------- |
| C08-CT03 | Cadastrar matrícula. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Cadastrar Matrícula |
| **QUANDO** selecionamos o cliente de teste, o plano "Treino Livre", pagamento em dinheiro e dia de vencimento 10 |
| **E** salvamos e confirmamos uma parcela |
| **ENTÃO** a matrícula deve ficar ativa |
| **E** a conta a receber deve ser gerada |

| **Critérios de aceitação** |
| :------- |
| A matrícula deve ficar ativa. |
| A conta a receber deve ser gerada. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado com ressalva | [Captura](../evidencias/imagens/EXE2-RF08-matricula-ativa-cliente-440.jpg) | — | Execução complementar — CT2-RF08-02 |

**Observação da execução:** Matrícula #246, plano Treino Livre; ativas 9→10; conta #1625 gerada.

---

### Caso de Teste 04: Aplicar desconto na matrícula.

| ID | Descrição |
| :------- | :------- |
| C08-CT04 | Aplicar desconto na matrícula. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Cadastrar Matrícula |
| **QUANDO** informamos desconto 10 no cadastro da matrícula |
| **ENTÃO** o valor total e a parcela devem refletir o desconto |

| **Critérios de aceitação** |
| :------- |
| O valor total e a parcela devem refletir o desconto. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Reprovado | Registro textual (respostas HTTP) | [BUG-018](../3-Relatorio-de-Bugs.md#bug-018) | Execução complementar — CT2-RF08-03 |

**Observação da execução:** Desconto 10 gravado, mas valor e parcela mantidos em 52,00.

---

### Caso de Teste 05: Cancelar matrícula.

| ID | Descrição |
| :------- | :------- |
| C08-CT05 | Cancelar matrícula. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifit.centrion.com.br`; dados de teste fictícios com prefixo QA. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Matrículas |
| **QUANDO** cancelamos a matrícula de teste informando o motivo |
| **E** confirmamos o cancelamento |
| **ENTÃO** o status deve passar a Cancelado e o indicador de ativas deve ser atualizado |
| **E** as contas pendentes devem ser tratadas conforme a regra do sistema |

| **Critérios de aceitação** |
| :------- |
| O status deve passar a Cancelado e o indicador de ativas deve ser atualizado. |
| As contas pendentes devem ser tratadas conforme a regra do sistema. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 18/11/2026 | sifit | Aprovado com ressalva | Registro textual (respostas HTTP) | — | Execução complementar — CT2-RF08-04 |

**Observação da execução:** Status CANCELADO e ativas 10→9 após recarregar; conta #1625 continua pendente.

---
