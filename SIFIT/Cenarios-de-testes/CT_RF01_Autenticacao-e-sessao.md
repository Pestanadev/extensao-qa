## Cenário 01: Autenticação e sessão.

**Tela:** `/login` · **Área:** Acesso · **Requisito:** [RF01](../1-Analise-de-requisitos.md#rf01)

### Caso de Teste 01: Entrar com credenciais válidas.

| ID | Descrição |
| :------- | :------- |
| C01-CT01 | Entrar com credenciais válidas. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Autenticação e sessão (`/login`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Autenticação e sessão do SIFIT |
| **QUANDO** abrir /login; preencher as credenciais fornecidas por canal privado; clicar Entrar |
| **ENTÃO** abrir /dashboard com sessão autenticada. Não exibir nem publicar a senha |

| **Critérios de aceitação** |
| :------- |
| Abrir /dashboard com sessão autenticada. Não exibir nem publicar a senha. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | [Captura](../evidencias/imagens/EXE-login-sucesso.png) | — | Exploração local — CT-RF01-01 |

**Observação da execução:** Redirecionou para /dashboard; interface mostrou Jair.

---

### Caso de Teste 02: Rejeitar credenciais inválidas.

| ID | Descrição |
| :------- | :------- |
| C01-CT02 | Rejeitar credenciais inválidas. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Autenticação e sessão (`/login`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Autenticação e sessão do SIFIT |
| **QUANDO** usar login fictício qa_documentacao_inexistente_20261021 e senha fictícia; clicar Entrar |
| **ENTÃO** permanecer fora da área autenticada e informar falha de autenticação |

| **Critérios de aceitação** |
| :------- |
| Permanecer fora da área autenticada e informar falha de autenticação. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | [Captura](../evidencias/imagens/EXE-login-invalido.png) | — | Exploração local — CT-RF01-02 |

**Observação da execução:** Credenciais fictícias rejeitadas com O nome de usuário e senha não correspondem.

---

### Caso de Teste 03: Impedir entrada com campos vazios.

| ID | Descrição |
| :------- | :------- |
| C01-CT03 | Impedir entrada com campos vazios. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Autenticação e sessão (`/login`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Autenticação e sessão do SIFIT |
| **QUANDO** deixar Login e Senha vazios; clicar Entrar |
| **ENTÃO** não criar sessão autenticada. Avaliar separadamente a clareza da mensagem de obrigatoriedade |

| **Critérios de aceitação** |
| :------- |
| Não criar sessão autenticada. Avaliar separadamente a clareza da mensagem de obrigatoriedade. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | [Captura](../evidencias/imagens/EXE-login-vazio.png) | — | Exploração local — CT-RF01-03 |

**Observação da execução:** Não entrou com campos vazios. Na primeira tentativa apareceu mensagem genérica; em uma repetição não houve mensagem inline perceptível. Aprovação restrita ao bloqueio de acesso.

---

### Caso de Teste 04: Abrir recuperação de senha.

| ID | Descrição |
| :------- | :------- |
| C01-CT04 | Abrir recuperação de senha. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Autenticação e sessão (`/login`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Autenticação e sessão do SIFIT |
| **QUANDO** na tela sem sessão, clicar Esqueci minha senha |
| **ENTÃO** abrir recuperação ou orientação acionável; não permanecer sem resposta |

| **Critérios de aceitação** |
| :------- |
| Abrir recuperação ou orientação acionável; não permanecer sem resposta. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/BUG-001-recuperacao-senha.png) | [BUG-001](../3-Relatorio-de-Bugs.md#bug-001) | Exploração local — CT-RF01-04 |

**Observação da execução:** Link não abriu recuperação nem orientação; permaneceu na tela de login.

---

### Caso de Teste 05: Encerrar sessão.

| ID | Descrição |
| :------- | :------- |
| C01-CT05 | Encerrar sessão. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Autenticação e sessão (`/login`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Autenticação e sessão do SIFIT |
| **QUANDO** entrar; abrir o menu da conta; clicar Sair do sistema |
| **ENTÃO** retornar ao login e invalidar o acesso autenticado |

| **Critérios de aceitação** |
| :------- |
| Retornar ao login e invalidar o acesso autenticado. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | Registro textual | — | Exploração local — CT-RF01-05 |

**Observação da execução:** Sair do sistema retornou para /login.

---

### Caso de Teste 06: Proteger rota após logout.

| ID | Descrição |
| :------- | :------- |
| C01-CT06 | Proteger rota após logout. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Autenticação e sessão (`/login`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Autenticação e sessão do SIFIT |
| **QUANDO** após sair, abrir /clientes diretamente |
| **ENTÃO** redirecionar para /login sem exibir dados de clientes |

| **Critérios de aceitação** |
| :------- |
| Redirecionar para /login sem exibir dados de clientes. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | Registro textual | — | Exploração local — CT-RF01-06 |

**Observação da execução:** Abrir /clientes após logout redirecionou para /login.

---

### Caso de Teste 07: Login — Login com campos em branco.

| ID | Descrição |
| :------- | :------- |
| C01-CT07 | Verificar login com campos em branco em Login. |

| **Pré-condições** |
| :------- |
| Estar na página de login, sem sessão ativa. |

| **Passos** |
| :------- |
| **DADO** que estamos na página de login do SIFIT |
| **QUANDO** deixamos os campos login e senha vazios |
| **E** clicamos em "Entrar" |
| **ENTÃO** devemos permanecer na página de login |
| **E** deve ser exibida mensagem indicando os campos obrigatórios |

| **Critérios de aceitação** |
| :------- |
| Devemos permanecer na página de login. |
| Deve ser exibida mensagem indicando os campos obrigatórios. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 01/10/2026 21:25 | sifit | Aprovado com ressalva | [Print (Jam)](https://jam.dev/c/76ae1224-ce04-4e4a-8c98-7554ea821020) | — | Equipe (vídeos JAM) — CT-01 do repositório anterior |

**Observação da execução:** Acesso bloqueado com campos vazios; a mensagem informa usuário e senha incorretos em vez de campos obrigatórios.

---

### Caso de Teste 08: Login — Botão "Esqueci minha senha".

| ID | Descrição |
| :------- | :------- |
| C01-CT08 | Verificar botão "Esqueci minha senha" em Login. |

| **Pré-condições** |
| :------- |
| Estar na página de login, sem sessão ativa. |

| **Passos** |
| :------- |
| **DADO** que estamos na página de login do SIFIT |
| **QUANDO** clicamos em "Esqueci minha senha" |
| **ENTÃO** deve ser aberto o fluxo de recuperação de senha ou uma orientação de suporte |

| **Critérios de aceitação** |
| :------- |
| Deve ser aberto o fluxo de recuperação de senha ou uma orientação de suporte. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 01/10/2026 21:31 | sifit | Reprovado | [Print (Jam)](https://jam.dev/c/e4dded02-6f23-43cc-832a-fedf751e0c06) | [BUG-001](../3-Relatorio-de-Bugs.md#bug-001) | Equipe (vídeos JAM) — CT-02 do repositório anterior |

**Observação da execução:** O print marca o link, mas não mostra o resultado; a reprodução local confirma que o link permanece em /login#.

---

### Caso de Teste 09: Login — Acesso com credenciais corretas.

| ID | Descrição |
| :------- | :------- |
| C01-CT09 | Verificar acesso com credenciais corretas em Login. |

| **Pré-condições** |
| :------- |
| Estar na página de login, sem sessão ativa; conta de testes fornecida pelo professor. |

| **Passos** |
| :------- |
| **DADO** que estamos na página de login do SIFIT |
| **QUANDO** preenchemos login e senha válidos da conta de testes |
| **E** clicamos em "Entrar" |
| **ENTÃO** devemos ser redirecionados para a Página Inicial |

| **Critérios de aceitação** |
| :------- |
| Devemos ser redirecionados para a Página Inicial. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 01/10/2026 21:34 | sifit | Aprovado | [Vídeo (Jam)](https://jam.dev/c/50d88cbd-0fc5-4602-a937-6f27e3e9a016) | — | Equipe (vídeos JAM) — CT-03 do repositório anterior |

**Observação da execução:** Login abriu o painel inicial; respostas 2xx.

---
