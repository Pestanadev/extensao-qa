## Cenário 34: Pontuação.

**Tela:** `/pontuacao` · **Área:** Gestão · **Requisito:** [RF34](../1-Analise-de-requisitos.md#rf34)

### Caso de Teste 01: Financeiro — Pontuação.

| ID | Descrição |
| :------- | :------- |
| C34-CT01 | Verificar pontuação em Financeiro. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Financeiro (`/pontuacao`) |
| **QUANDO** cadastramos uma pontuação de teste |
| **E** excluímos a pontuação cadastrada |
| **ENTÃO** a pontuação deve ser salva e listada |
| **E** após a exclusão, deve deixar de ser exibida |

| **Critérios de aceitação** |
| :------- |
| A pontuação deve ser salva e listada. |
| Após a exclusão, deve deixar de ser exibida. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 31/10/2026 17:18 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/c8d0473d-4441-472b-846e-bcdc02fb6695) | — | Equipe (vídeos JAM) — CT-09 do repositório anterior |

**Observação da execução:** Cadastro (201×2) e exclusão visíveis (3→2); uma resposta 500 sem efeito visível.

---
