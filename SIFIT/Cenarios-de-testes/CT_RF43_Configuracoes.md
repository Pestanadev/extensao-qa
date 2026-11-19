## Cenário 43: Configurações.

**Tela:** `/configuracoes` · **Área:** Configurações · **Requisito:** [RF43](../1-Analise-de-requisitos.md#rf43)

### Caso de Teste 01: Navegar pelas sete abas sem salvar.

| ID | Descrição |
| :------- | :------- |
| C43-CT01 | Navegar pelas sete abas sem salvar. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Configurações (`/configuracoes`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Configurações do SIFIT |
| **QUANDO** abrir Home, Biometria, Avaliação, Aniversário, Pagamento, Integrações e Design; em Aniversário abrir Endpoints & Tokens |
| **ENTÃO** exibir os respectivos campos e manter alterações persistentes intactas ao sair sem salvar |

| **Critérios de aceitação** |
| :------- |
| Exibir os respectivos campos e manter alterações persistentes intactas ao sair sem salvar. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Aprovado | Registro textual | — | Exploração local — CT-RF43-01 |

**Observação da execução:** As sete abas e a subaba Endpoints & Tokens abriram; nenhuma configuração foi salva.

---

### Caso de Teste 02: Configurações — Home.

| ID | Descrição |
| :------- | :------- |
| C43-CT02 | Verificar home em Configurações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Configurações (`/configuracoes`) |
| **QUANDO** alteramos as opções da aba "Home" |
| **E** clicamos em salvar |
| **ENTÃO** as configurações devem ser salvas e mantidas ao reabrir a aba |

| **Critérios de aceitação** |
| :------- |
| As configurações devem ser salvas e mantidas ao reabrir a aba. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 15:58 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/2bea0a38-f30b-447a-9f86-4da71aa7b8c1) | — | Equipe (vídeos JAM) — CT-13 do repositório anterior |

**Observação da execução:** Aba Home salva sem erro (2xx).

---

### Caso de Teste 03: Configurações — Biometria.

| ID | Descrição |
| :------- | :------- |
| C43-CT03 | Verificar biometria em Configurações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Configurações (`/configuracoes`) |
| **QUANDO** alteramos as opções da aba "Biometria" |
| **E** clicamos em salvar |
| **ENTÃO** as configurações devem ser salvas e mantidas ao reabrir a aba |

| **Critérios de aceitação** |
| :------- |
| As configurações devem ser salvas e mantidas ao reabrir a aba. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 15:59 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/5d844b20-b8a7-4968-b8d5-7ad405d0a6d9) | — | Equipe (vídeos JAM) — CT-14 do repositório anterior |

**Observação da execução:** Aba Biometria salva sem erro (2xx).

---

### Caso de Teste 04: Configurações — Avaliação.

| ID | Descrição |
| :------- | :------- |
| C43-CT04 | Verificar avaliação em Configurações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Configurações (`/configuracoes`) |
| **QUANDO** alteramos as opções da aba "Avaliação" |
| **E** clicamos em salvar |
| **ENTÃO** as configurações devem ser salvas e mantidas ao reabrir a aba |

| **Critérios de aceitação** |
| :------- |
| As configurações devem ser salvas e mantidas ao reabrir a aba. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:00 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/70f6b2f5-fd50-4128-8514-3ae81f851599) | — | Equipe (vídeos JAM) — CT-15 do repositório anterior |

**Observação da execução:** Aba Avaliação salva sem erro (2xx).

---

### Caso de Teste 05: Configurações — Aniversário.

| ID | Descrição |
| :------- | :------- |
| C43-CT05 | Verificar aniversário em Configurações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Configurações (`/configuracoes`) |
| **QUANDO** alteramos as opções da aba "Aniversário" |
| **E** clicamos em salvar |
| **ENTÃO** as configurações devem ser salvas e mantidas ao reabrir a aba |

| **Critérios de aceitação** |
| :------- |
| As configurações devem ser salvas e mantidas ao reabrir a aba. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:01 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/a1c2c902-4443-4d48-b530-445a63aaeccb) | — | Equipe (vídeos JAM) — CT-16 do repositório anterior |

**Observação da execução:** Aba Aniversário salva sem erro (2xx).

---

### Caso de Teste 06: Configurações — Pagamento.

| ID | Descrição |
| :------- | :------- |
| C43-CT06 | Verificar pagamento em Configurações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Configurações (`/configuracoes`) |
| **QUANDO** alteramos as opções da aba "Pagamento" |
| **E** clicamos em salvar |
| **ENTÃO** as configurações devem ser salvas e mantidas ao reabrir a aba |

| **Critérios de aceitação** |
| :------- |
| As configurações devem ser salvas e mantidas ao reabrir a aba. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:02 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/7db68275-cd1a-4ce5-8d34-86b401ab1b2c) | — | Equipe (vídeos JAM) — CT-17 do repositório anterior |

**Observação da execução:** Aba Pagamento salva sem erro (2xx).

---

### Caso de Teste 07: Configurações — Integrações.

| ID | Descrição |
| :------- | :------- |
| C43-CT07 | Verificar integrações em Configurações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Configurações (`/configuracoes`) |
| **QUANDO** alteramos as opções da aba "Integrações" |
| **E** clicamos em salvar |
| **ENTÃO** as configurações devem ser salvas e mantidas ao reabrir a aba |

| **Critérios de aceitação** |
| :------- |
| As configurações devem ser salvas e mantidas ao reabrir a aba. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:05 | sifitalfa | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/99ecc77c-0ae0-4031-aaca-e26881937139) | — | Equipe (vídeos JAM) — CT-18 do repositório anterior |

**Observação da execução:** 422 ×3 com valores fictícios; validação esperada, sem teste com dados válidos.

---

### Caso de Teste 08: Configurações — Design.

| ID | Descrição |
| :------- | :------- |
| C43-CT08 | Verificar design em Configurações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Configurações (`/configuracoes`) |
| **QUANDO** alteramos as opções da aba "Design" |
| **E** clicamos em salvar |
| **ENTÃO** as configurações devem ser salvas e mantidas ao reabrir a aba |

| **Critérios de aceitação** |
| :------- |
| As configurações devem ser salvas e mantidas ao reabrir a aba. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:07 | sifitalfa | Reprovado | [Vídeo (Jam)](https://jam.dev/c/11c2253a-aa5b-40a9-8b33-717e5d13ef1c) | [BUG-008](../3-Relatorio-de-Bugs.md#bug-008) | Equipe (vídeos JAM) — CT-19 do repositório anterior |

**Observação da execução:** 400 e “Erro ao salvar configurações”.

---
