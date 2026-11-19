## Cenário 46: Meu perfil e controles globais.

**Tela:** `/profile` · **Área:** Acesso · **Requisito:** [RF46](../1-Analise-de-requisitos.md#rf46)

### Caso de Teste 01: Exibir perfil coerente com a conta.

| ID | Descrição |
| :------- | :------- |
| C46-CT01 | Exibir perfil coerente com a conta. |

| **Pré-condições** |
| :------- |
| Usuário com acesso ao ambiente `sifit.centrion.com.br`; tela Meu perfil e controles globais (`/profile`). |

| **Passos** |
| :------- |
| **DADO** que estamos na tela Meu perfil e controles globais do SIFIT |
| **QUANDO** abrir menu da conta; clicar Meu perfil; aguardar |
| **ENTÃO** exibir informações do usuário autenticado ou estado vazio apropriado; não apresentar Jesse/Jessica Jones demonstrativos |

| **Critérios de aceitação** |
| :------- |
| Exibir informações do usuário autenticado ou estado vazio apropriado; não apresentar Jesse/Jessica Jones demonstrativos. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 21/10/2026 | sifit | Reprovado | [Captura](../evidencias/imagens/BUG-005-perfil-template.png) | [BUG-005](../3-Relatorio-de-Bugs.md#bug-005) | Exploração local — CT-RF46-01 |

**Observação da execução:** Meu perfil abriu conteúdo de demonstração Hello Jesse/Jessica Jones.

---

### Caso de Teste 02: Notificações — Marcar mensagens como lidas.

| ID | Descrição |
| :------- | :------- |
| C46-CT02 | Verificar marcar mensagens como lidas em Notificações. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Notificações (`/dashboard`) |
| **QUANDO** abrimos o painel de notificações |
| **E** marcamos as mensagens como lidas |
| **ENTÃO** as mensagens devem passar a lidas e o contador deve ser atualizado |

| **Critérios de aceitação** |
| :------- |
| As mensagens devem passar a lidas e o contador deve ser atualizado. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 22/10/2026 19:41 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/d9fd0191-a91f-47a4-8edf-5c9ace910b25) | — | Equipe (vídeos JAM) — CT-06 do repositório anterior |

**Observação da execução:** Painel aberto e ações concluídas sem erro; mudança de estado pouco legível no vídeo.

---
