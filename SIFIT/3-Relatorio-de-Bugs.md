# 3 - Relatório de Bugs - SIFIT

## BUG-01 - Botão ao lado de "Competência" no Dashboard não executa nenhuma ação
| Campo | Detalhe |
|---|---|
| Módulo | Dashboard |
| Severidade (sugerida) | Baixa |
| Cenário | CT-04 |
| Data | 02/10/2026 |
| Ambiente | Chrome 154, Windows 11 |
| Evidência | [Print (Jam)](https://jam.dev/c/4dfcb03a-bf1b-4d35-8874-31f846f25250) |

**Passos para reproduzir**
1. Fazer login no sistema.
2. Acessar o Dashboard.
3. Clicar no botão localizado ao lado do campo "Competência".

**Resultado esperado:** o botão executar a função correspondente.  
**Resultado obtido:** nenhuma ação acontece.  
**Observação:** na sessão capturada, uma requisição à API retornou 403 (acesso negado). Não foi confirmado se isso tem relação com o botão.

---

## BUG-02 - Erro 400 (Bad Request) ao criar Modelo de Ficha
| Campo | Detalhe |
|---|---|
| Módulo | Treinos |
| Severidade (sugerida) | Alta (impede a criação do modelo) |
| Cenário | CT-12 |
| Data | 31/10/2026 |
| Ambiente | Chrome 156, Windows 11 |
| Evidência | [Vídeo (Jam)](https://jam.dev/c/645a3706-aa9e-4724-b4bb-6b7badb33e92) |

**Passos para reproduzir**
1. Clicar em "Cadastro de Modelo" no menu superior.
2. Abrir "Novo Modelo de Ficha" e preencher os campos obrigatórios (informar aqui os dados usados).
3. Clicar em "Criar Modelo".

**Resultado esperado:** o modelo ser criado e aparecer na listagem.  
**Resultado obtido:** a API responde 400 Bad Request e o sistema exibe um painel de erro.  
**Observação técnica:** a requisição POST ao servidor de back-end retornou 400 e nenhum erro foi registrado no console do navegador.

---

## BUG-03 - Erro 500 ao alterar uma pergunta (Perguntas de anamnese)
| Campo | Detalhe |
|---|---|
| Módulo | Perguntas |
| Severidade (sugerida) | Alta (impede alterar uma pergunta existente) |
| Cenário | CT-31 |
| Data | 15/11/2026 |
| Ambiente | Chrome 157, Windows 11 |
| Evidência | [Vídeo (Jam)](https://jam.dev/c/902e3330-f85e-43b4-83c7-5d7283a39882) |

**Passos para reproduzir**
1. Acessar o menu Perguntas e criar uma nova pergunta (o cadastro funciona e a API responde 201).
2. Na listagem, abrir a pergunta criada pelo ícone de lupa.
3. Alterar um campo (texto ou número) e clicar em "Salvar".

**Resultado esperado:** a alteração ser salva.  
**Resultado obtido:** a API de alteração responde 500 (erro interno do servidor) e o sistema exibe um painel de erro; ao tentar salvar de novo, o erro se repete.  
**Observação técnica:** nenhum erro foi registrado no console do navegador; a falha aparece nas requisições ao endpoint de alteração de pergunta.
