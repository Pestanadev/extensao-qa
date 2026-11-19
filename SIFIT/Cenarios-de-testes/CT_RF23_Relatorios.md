## Cenário 23: Relatórios.

**Tela:** `/relatorios` · **Área:** Financeiro · **Requisito:** [RF23](../1-Analise-de-requisitos.md#rf23)

### Caso de Teste 01: Relatórios — Geração e filtro.

| ID | Descrição |
| :------- | :------- |
| C23-CT01 | Verificar geração e filtro em Relatórios. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Relatórios (`/relatorios`) |
| **QUANDO** geramos um relatório |
| **E** aplicamos os filtros disponíveis |
| **ENTÃO** o relatório deve ser exibido conforme os filtros aplicados |

| **Critérios de aceitação** |
| :------- |
| O relatório deve ser exibido conforme os filtros aplicados. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 20:06 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/91321d0b-ad8b-41d0-baf6-2fdf90e5dc87) | — | Equipe (vídeos JAM) — CT-73 do repositório anterior |

**Observação da execução:** Geração e filtro com respostas 2xx; conteúdo dos PDFs não verificado.

---
