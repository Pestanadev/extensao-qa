## Cenário 10: Contas a Receber.

**Tela:** `/contas-receber` · **Área:** Operação · **Requisito:** [RF10](../1-Analise-de-requisitos.md#rf10)

### Caso de Teste 01: Contas a Receber — Cadastro, consulta, edição e exclusão.

| ID | Descrição |
| :------- | :------- |
| C10-CT01 | Verificar cadastro, consulta, edição e exclusão em Contas a Receber. |

| **Pré-condições** |
| :------- |
| Usuário autenticado com perfil administrador no ambiente `sifitalfa.centrion.com.br`. |

| **Passos** |
| :------- |
| **DADO** que estamos autenticados no SIFIT e acessamos a tela Contas a Receber (`/matriculas`) |
| **QUANDO** cadastramos uma conta a receber (via matrícula) |
| **E** consultamos, editamos e excluímos a conta |
| **ENTÃO** cada operação deve ser concluída e refletida na listagem |

| **Critérios de aceitação** |
| :------- |
| Cada operação deve ser concluída e refletida na listagem. |

| **Data** | **Ambiente** | **Resultado** | **Evidência** | **Bug** | **Origem** |
| :---: | :---: | :---: | :---: | :---: | :---: |
| 17/11/2026 18:19 | sifitalfa | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/d77ccbff-1206-4144-9702-1fb8068bfb56) | — | Equipe (vídeos JAM) — CT-68 do repositório anterior |

**Observação da execução:** Cadastro pela matrícula; 400 = validação “Selecione o Tipo de Pagamento”; conta listada depois.

---
