## Cenário 41: Inteligência e Automação.

**Tela:** `/inteligencia-automacao` · **Área:** Inteligência · **Requisito:** [RF41](../1-Analise-de-requisitos.md#rf41)

### Caso de Teste 01: Inteligência e Automação — Integração e Automatização.

| ID | Descrição |
| :------- | :------- |
| C41-CT01 | Verificar integração e Automatização em Inteligência e Automação. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Inteligência e Automação (`/inteligencia-automacao`) |
| **QUANDO** navegamos pelas opções de integração e automatização |
| **ENTÃO** as informações devem ser carregadas sem erro |

| **Critérios de aceitação** |
| :------- |
| As informações devem ser carregadas sem erro. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:10 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/e91d5a54-306f-4853-8c6d-6a9c7d506088) | — | Equipe (vídeos JAM) — CT-21 do repositório anterior |

**Observação da execução:** Configuração e listagens com respostas 2xx.

---

### Caso de Teste 02: Inteligência e Automação — Relatório de Risco de Evasão.

| ID | Descrição |
| :------- | :------- |
| C41-CT02 | Verificar relatório de Risco de Evasão em Inteligência e Automação. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Inteligência e Automação (`/inteligencia-automacao`) |
| **QUANDO** geramos o relatório de risco de evasão com os filtros disponíveis |
| **ENTÃO** o relatório deve ser exibido conforme os filtros |

| **Critérios de aceitação** |
| :------- |
| O relatório deve ser exibido conforme os filtros. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:16 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/4f6d9b31-d3aa-4085-8151-694a60234e0b) | — | Equipe (vídeos JAM) — CT-22 do repositório anterior |

**Observação da execução:** Relatório de risco gerado; respostas 2xx.

---

### Caso de Teste 03: Inteligência e Automação — Automações - Configuração.

| ID | Descrição |
| :------- | :------- |
| C41-CT03 | Verificar automações - Configuração em Inteligência e Automação. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Inteligência e Automação (`/inteligencia-automacao`) |
| **QUANDO** configuramos uma automação e salvamos |
| **ENTÃO** a configuração deve ser salva ou deve ser exibida mensagem de validação clara |

| **Critérios de aceitação** |
| :------- |
| A configuração deve ser salva ou deve ser exibida mensagem de validação clara. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 16:18 | sifitalfa | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/7b66dbf7-705c-4e42-a6ba-4fdffa29745d) | — | Equipe (vídeos JAM) — CT-23 do repositório anterior |

**Observação da execução:** 422 e “Não foi possível concluir” por destinatário inválido; validação esperada.

---
