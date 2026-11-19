## Cenário 30: Funções e permissões.

**Tela:** `/funcoes` · **Área:** Gestão · **Requisito:** [RF30](../1-Analise-de-requisitos.md#rf30)

### Caso de Teste 01: Funções — Cadastro e grupo de permissões.

| ID | Descrição |
| :------- | :------- |
| C30-CT01 | Verificar cadastro e grupo de permissões em Funções. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Funções (`/funcoes`) |
| **QUANDO** cadastramos uma nova função com dados de teste |
| **E** definimos o grupo de permissões e salvamos |
| **ENTÃO** a função deve ser salva com as permissões selecionadas |

| **Critérios de aceitação** |
| :------- |
| A função deve ser salva com as permissões selecionadas. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 15/11/2026 13:35 | sifitalfa | Aprovado | [Vídeo (Jam)](https://jam.dev/c/1c619e71-bf82-469b-8061-a45acfc99019) | — | Equipe (vídeos JAM) — CT-48 do repositório anterior |

**Observação da execução:** Função criada (201×2) com permissões.

---
