# Análise dos 73 registros JAM da equipe

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../Cenarios-de-testes/) conforme a [correspondência de IDs](correspondencia-de-ids.md).

**Data:** 18/11/2026 · **Método:** leitura automatizada, no navegador integrado do Claude, das abas Info, Actions, Network e da linha do tempo de cada link JAM. Os vídeos não foram assistidos quadro a quadro.

## O que foi extraído

- **Info:** título, duração, data e hora, e URL do site gravado.
- **Actions:** quantidade de ações e textos digitados, que servem como identificadores dos registros de teste. O JAM já mascara campos de senha (`***`). Nomes de pessoas usados em buscas foram omitidos.
- **Network e linha do tempo:** método e status HTTP das requisições ao backend. O JAM não exibe o caminho da API nessa extração, então a operação de cada status é inferida pela ordem das ações.

**Limite:** a tabela de rede do JAM só desenha as linhas visíveis, então em gravações longas a contagem pode ficar incompleta. Por isso os erros abaixo juntam a tabela de rede e os marcadores da linha do tempo. Um status 2xx indica que o backend aceitou a requisição, mas não prova o resultado correto da operação nem a persistência. Status 201 (Created) indica criação aceita pelo backend.

## Resultado geral

| Indicador | Quantidade |
| --- | ---: |
| Links lidos | 73 de 73 |
| Gravados em `sifit.centrion.com.br` (01/10/2026) | 4: FP-CT-01 a FP-CT-04 |
| Gravados em `sifitalfa.centrion.com.br` (22/10 a 17/11/2026) | 69: FP-CT-05 a FP-CT-73 |
| Com resposta de erro do backend (4xx/5xx) | 19 |
| Com erro 500 (falha interna do servidor) | 9 |
| Sem requisição ao backend capturada | 4: FP-CT-02, 08, 10, 26 |

FP-CT-01, 02 e 04 não têm duração (são capturas de tela), embora o JAM tenha registrado ações e rede. Em todos os registros do `sifitalfa`, as requisições vão para `backsifitalfa.centrion.com.br`. Nos do `sifit`, vão para `backendsifit.centrion.com.br`.

## Registros com erro do backend

| Caso | Tela | Erros HTTP | Leitura |
| --- | --- | --- | --- |
| FP-CT-09 | Pontuação | 500 ×1 | Falha interna em uma das gravações; houve também 201 ×2 |
| FP-CT-12 | Modelos de Ficha | 400 ×1 | Título do JAM: “Creating workout model returns 400 Bad Request” (FP-BUG-02) |
| FP-CT-18 | Configurações › Integrações | 422 ×3 | Validação rejeitada três vezes |
| FP-CT-19 | Configurações › Design | 400 ×1 | Requisição rejeitada |
| FP-CT-23 | Automações | 422 ×1 | Validação rejeitada |
| FP-CT-27 | Produtos › Novo | 400 ×2 | Rejeições antes de 201 ×2 |
| FP-CT-31 | Perguntas › Nova | 500 ×4 | Quatro falhas internas; coerente com “Erro ao salvar pergunta” a 0:32 (FP-BUG-03) |
| FP-CT-33 | Perguntas › Edição | 500 ×1 | Falha interna na edição |
| FP-CT-47 | Fornecedores | 500 ×5 a ×7 | Falhas internas repetidas no cadastro/edição |
| FP-CT-53 | Bandeiras | 500 ×2 | Falhas internas; houve um 201 |
| FP-CT-56 | Planos | 500 ×2 | Coerente com “Erro ao deletar Plano” a 0:57 |
| FP-CT-57 | Grupos | 500 ×2 | Falhas internas; houve 201 ×2 |
| FP-CT-61 | Objetivos de Treino | 400 ×2 | Rejeições |
| FP-CT-62 | Grupos Musculares | 400 ×1 a ×2 | Rejeição |
| FP-CT-64 | Exercícios | 400 ×3 | Rejeições; houve 201 ×3 |
| FP-CT-68 | Contas a Receber | 400 ×1 | Gravado na rota `/matriculas` |
| FP-CT-70 | Caixas | 423 ×2 | Recurso bloqueado (423 Locked) |
| FP-CT-71 | Avaliações | 500 ×1 a ×2 | Falha interna |
| FP-CT-72 | Despesas Fixas | 500 ×2 | Falhas internas; houve um 201 |

Os casos marcados como “A confirmar” na fonte e que contêm erro 4xx/5xx não podem ser aprovados sem análise do momento do erro. Os erros 500 são candidatos a novos defeitos (FP-CT-33, 47, 53, 57, 71, 72 e 09) e precisam de confirmação visual no vídeo antes de virar relatório de bug.

## Tabela completa

Legenda: **F** = `sifit`, **A** = `sifitalfa`. Nos identificadores digitados, `⌫` indica correção feita durante a digitação. Os textos aparecem como capturados.

| Caso | Site | Data/hora (BRT) | Duração | Rota | Ações | HTTP do backend (resumo) | Identificadores digitados |
| --- | --- | --- | --- | --- | ---: | --- | --- |
| FP-CT-01 | F | 01/10 21:25 | print | /login | 15 | POST 200 | campos mascarados |
| FP-CT-02 | F | 01/10 21:31 | print | /login | 5 | — | — |
| FP-CT-03 | F | 01/10 21:34 | 0:05 | /login | 3 | 2xx | — |
| FP-CT-04 | F | 01/10 21:36 | print | /dashboard | 24 | 2xx | — |
| FP-CT-05 | A | 31/10 17:14 | 0:24 | /checkin | 17 | 2xx; 201 ×1 | busca por nome de cliente (omitido) |
| FP-CT-06 | A | 22/10 19:41 | 0:17 | /dashboard | 26 | 2xx | — |
| FP-CT-07 | A | 22/10 19:43 | 0:43 | /dashboard | 29 | 2xx | texto colado |
| FP-CT-08 | A | 22/10 19:45 | 0:04 | /dashboard | 0 | — | — |
| FP-CT-09 | A | 31/10 17:18 | 0:49 | /pontuacao | 31 | 201 ×2; **500 ×1** | “Teste” |
| FP-CT-10 | A | 22/10 19:46 | 0:11 | /dashboard | 6 | — | — |
| FP-CT-11 | A | 31/10 15:57 | 0:29 | /pagarme | 22 | 2xx | valor “100” |
| FP-CT-12 | A | 31/10 15:53 | 0:09 | /fichas-treino-modelo | 9 | **400 ×1** | texto colado |
| FP-CT-13 | A | 31/10 15:58 | 0:40 | /configuracoes | 41 | 2xx | “120” |
| FP-CT-14 | A | 31/10 15:59 | 0:11 | /configuracoes | 7 | 2xx | — |
| FP-CT-15 | A | 31/10 16:00 | 0:16 | /configuracoes | 14 | 2xx | “1” |
| FP-CT-16 | A | 31/10 16:01 | 0:27 | /configuracoes | 27 | 2xx | texto colado |
| FP-CT-17 | A | 31/10 16:02 | 0:14 | /configuracoes | 16 | 2xx | “a” |
| FP-CT-18 | A | 31/10 16:05 | 0:41 | /configuracoes | 17 | **422 ×3** | campos mascarados; “aaaaaaaaaa” |
| FP-CT-19 | A | 31/10 16:07 | 0:03 | /configuracoes | 2 | **400 ×1** | — |
| FP-CT-20 | A | 31/10 16:08 | 0:11 | /inteligencia/resultados | 6 | 2xx | — |
| FP-CT-21 | A | 31/10 16:10 | 0:30 | /inteligencia-automacao | 22 | 2xx | — |
| FP-CT-22 | A | 31/10 16:16 | 0:37 | /inteligencia-automacao | 17 | 2xx | “4”, “aaa2” |
| FP-CT-23 | A | 31/10 16:18 | 0:56 | /inteligencia-automacao | 41 | 2xx; **422 ×1** | “32”, “40” |
| FP-CT-24 | A | 31/10 16:21 | 0:30 | /atividades | 23 | 201 ×3 | “Treino de Pernas”; segundo cadastro iniciado por “Treino de P…” |
| FP-CT-25 | A | 31/10 16:22 | 0:11 | /atividades | 6 | 2xx | — |
| FP-CT-26 | A | 31/10 16:23 | 0:10 | /atividades | 1 | — | busca “Treino” |
| FP-CT-27 | A | 31/10 17:28 | 0:20 | /produtos | 14 | 201 ×2; **400 ×2** | “test” |
| FP-CT-28 | A | 31/10 15:51 | 0:11 | /aplicativo | 9 | 201 ×1 | “aaaaa” |
| FP-CT-29 | A | 31/10 15:51 | 0:07 | /aplicativo | 5 | 2xx | — |
| FP-CT-30 | A | 15/11 12:24 | 0:28 | /bandeiras | 29 | 201 ×2 | “master”, “aaaa1”, “qqq222” |
| FP-CT-31 | A | 15/11 12:30 | 0:52 | /perguntas-anamnese | 36 | 201 ×2; **500 ×4** | “Como treinar pernas corretamente?”, categoria “Pernas” |
| FP-CT-32 | A | 15/11 12:33 | 0:05 | /perguntas-anamnese | 2 | 2xx | — |
| FP-CT-33 | A | 15/11 12:34 | 0:10 | /perguntas-anamnese | 6 | **500 ×1** | “quais ti…” |
| FP-CT-34 | A | 15/11 12:36 | 0:20 | /anamnese/categorias | 7 | 201 ×2 | “Alimentação2” |
| FP-CT-35 | A | 15/11 12:37 | 0:10 | /anamnese/categorias | 7 | 2xx | — |
| FP-CT-36 | A | 15/11 12:37 | 0:08 | /anamnese/categorias | 6 | 2xx | “Energia” |
| FP-CT-37 | A | 15/11 13:13 | 0:19 | /anamnese/modelos/novo | 22 | 201 ×1 | “aaaaaaaa” |
| FP-CT-38 | A | 15/11 13:14 | 0:11 | /anamnese/modelos | 6 | 2xx | — |
| FP-CT-39 | A | 15/11 13:14 | 0:13 | /anamnese/modelos | 22 | 2xx | — |
| FP-CT-40 | A | 15/11 13:15 | 0:10 | /anamnese/modelos | 7 | 2xx | busca “Iniciante” |
| FP-CT-41 | A | 15/11 13:19 | 0:21 | /anamneses | 11 | 201 ×2 | texto colado |
| FP-CT-42 | A | 15/11 13:21 | 0:30 | /enquetes | 19 | 2xx | “teste####”, “Enquete test @@@@@” |
| FP-CT-43 | A | 15/11 13:23 | 0:14 | /enquetes | 9 | 2xx | — |
| FP-CT-44 | A | 15/11 13:24 | 0:10 | /produtos | 7 | 2xx | — |
| FP-CT-45 | A | 15/11 13:26 | 0:12 | /tipos-documento | 10 | 201 ×2 | texto colado |
| FP-CT-46 | A | 15/11 13:27 | 0:05 | /tipos-documento | 2 | 2xx | — |
| FP-CT-47 | A | 15/11 13:32 | 1:16 | /fornecedores | 68 | **500 ×5–7** | “test”, sequências de zeros |
| FP-CT-48 | A | 15/11 13:35 | 1:07 | /funcoes | 105 | 201 ×2 | “aaaaaaaaa”, “eeeaae” |
| FP-CT-49 | A | 15/11 13:38 | 1:09 | /colaboradores | 65 | 201 ×2 | “test”, data 01/06/2026, campos mascarados |
| FP-CT-50 | A | 15/11 13:39 | 0:18 | /colaboradores | 17 | 2xx | campo mascarado |
| FP-CT-51 | A | 15/11 13:53 | 0:33 | /turmas | 24 | 201 ×2 | “turma test” |
| FP-CT-52 | A | 15/11 13:54 | 0:10 | /turmas | 5 | 2xx | busca “testeeeeeeee” |
| FP-CT-53 | A | 15/11 13:55 | 0:37 | /bandeiras | 34 | 201 ×1; **500 ×2** | “master” |
| FP-CT-54 | A | 15/11 13:58 | 0:26 | /tipos-pagamento | 20 | 201 ×2 | “master”, “test”, “eere” |
| FP-CT-55 | A | 15/11 13:59 | 0:14 | /modelos-contrato | 30 | 201 ×1 | “aaaa…” |
| FP-CT-56 | A | 15/11 14:01 | 0:59 | /planos | 40 | 2xx; **500 ×2** (linha do tempo) | “aaa”, “111” |
| FP-CT-57 | A | 15/11 14:03 | 0:38 | /grupos | 40 | 201 ×2; **500 ×2** | “test”, “testeeeeeeeee” |
| FP-CT-58 | A | 15/11 14:05 | 0:40 | /prospeccao | 33 | 2xx | “aaaaaaaaa”, “aa@” |
| FP-CT-59 | A | 15/11 14:07 | 0:59 | /sifitbox/turmas | 93 | 201 ×2 | “aaaaaaaaaaaaa” |
| FP-CT-60 | A | 15/11 14:15 | 0:26 | /categorias-exercicios-crossfit | 21 | 201 ×2 | “test”, “8” |
| FP-CT-61 | A | 15/11 14:19 | 0:35 | /objetivos-treino | 40 | 201 ×2; **400 ×2** | “aaaaaa”, “8” |
| FP-CT-62 | A | 17/11 18:07 | 0:53 | /grupos-musculares | 36 | 201 ×1; **400 ×1–2** | “aaaaaaaaaaa”, busca “pernas” |
| FP-CT-63 | A | 17/11 18:08 | 0:14 | /grupos-musculares | 8 | 2xx | busca “pernas” |
| FP-CT-64 | A | 17/11 18:10 | 0:51 | /exercicios | 36 | 201 ×3; **400 ×3** | “aaaaaaaaa”, “testes_01” |
| FP-CT-65 | A | 17/11 18:11 | 0:13 | /exercicios | 4 | 2xx | — |
| FP-CT-66 | A | 17/11 18:13 | 0:47 | /fichas-treino | 22 | 201 ×1 | — |
| FP-CT-67 | A | 17/11 18:14 | 0:23 | /ficha-treino/alterar/4 | 23 | 2xx | ficha de ID 4 |
| FP-CT-68 | A | 17/11 18:19 | 1:26 | /matriculas | 56 | **400 ×1** | “a”, “1” |
| FP-CT-69 | A | 17/11 18:21 | 0:59 | /contas-pagar | 41 | 201 ×2 | “aaaaaa”, “aaaaaa1111” |
| FP-CT-70 | A | 17/11 18:24 | 1:32 | /caixas | 0 | **423 ×2** | — |
| FP-CT-71 | A | 17/11 18:27 | 2:01 | /avaliacoes | 130 | 201 ×2; **500 ×1–2** | busca por nome (omitido), “test”, altura “1,87” |
| FP-CT-72 | A | 17/11 20:05 | 0:31 | /despesas-fixas | 22 | 201 ×1; **500 ×2** | “aaaaaaaaa” |
| FP-CT-73 | A | 17/11 20:06 | 0:43 | /relatorios | 0 | 2xx | — |

## Veredito por caso (revisão de 18/11/2026)

**Critério.** Os 19 registros com erro do backend foram assistidos nos pontos de erro e no quadro final, com captura do quadro do vídeo. Os demais receberam veredito pela evidência automatizada: ações concluídas, ausência de erro HTTP e resposta 201 nos cadastros. “Aprovado com ressalva” indica fluxo sem erro, mas efeito não totalmente visível ou não conferido no banco. “Parcial” indica que ao menos uma operação do caso falhou. A conferência no banco não foi possível porque o `sifitalfa` grava em outro banco (ver [conferência do banco](conferencia-do-banco.md)).

| Resultado | Casos |
| --- | ---: |
| Aprovado | 20 |
| Aprovado com ressalva | 32 |
| Parcial | 8 |
| Reprovado | 7 |
| Inconclusivo | 6 |
| **Total** | **73** |

| Caso | Resultado | Fundamento | Ocorrência |
| --- | --- | --- | --- |
| FP-CT-01 | Aprovado com ressalva | Acesso bloqueado com campos vazios; a mensagem informa usuário e senha incorretos em vez de campos obrigatórios | — |
| FP-CT-02 | Reprovado | O print marca o link, mas não mostra o resultado; a reprodução local confirma que o link permanece em /login# | BUG-001 |
| FP-CT-03 | Aprovado | Login abriu o painel inicial; respostas 2xx | — |
| FP-CT-04 | Reprovado | Botão ao lado do período sem ação; reproduzido no sifit em 18/11 (sem mudança na tela e sem requisição) | BUG-006 |
| FP-CT-05 | Aprovado | Check-in registrado (201) e exibido na lista | — |
| FP-CT-06 | Aprovado com ressalva | Painel aberto e ações concluídas sem erro; mudança de estado pouco legível no vídeo | — |
| FP-CT-07 | Inconclusivo | Depende do WhatsApp, desconectado no ambiente; envio não verificável | — |
| FP-CT-08 | Inconclusivo | Gravação de 4 s sem ações; arquivo exportado não aparece | — |
| FP-CT-09 | Aprovado com ressalva | Cadastro (201×2) e exclusão visíveis (3→2); uma resposta 500 sem efeito visível | — |
| FP-CT-10 | Inconclusivo | Tela vazia exibida; relação com o indicador de desistências não verificada | INV-002 |
| FP-CT-11 | Inconclusivo | Solicitação de saque com respostas 2xx; efeito no gateway não verificável | — |
| FP-CT-12 | Reprovado | 400 e “Erro ao salvar modelo” | BUG-007 |
| FP-CT-13 | Aprovado com ressalva | Aba Home salva sem erro (2xx) | — |
| FP-CT-14 | Aprovado com ressalva | Aba Biometria salva sem erro (2xx) | — |
| FP-CT-15 | Aprovado com ressalva | Aba Avaliação salva sem erro (2xx) | — |
| FP-CT-16 | Aprovado com ressalva | Aba Aniversário salva sem erro (2xx) | — |
| FP-CT-17 | Aprovado com ressalva | Aba Pagamento salva sem erro (2xx) | — |
| FP-CT-18 | Inconclusivo | 422 ×3 com valores fictícios; validação esperada, sem teste com dados válidos | — |
| FP-CT-19 | Reprovado | 400 e “Erro ao salvar configurações” | BUG-008 |
| FP-CT-20 | Aprovado | Resultados exibidos; respostas 2xx | — |
| FP-CT-21 | Aprovado | Configuração e listagens com respostas 2xx | — |
| FP-CT-22 | Aprovado | Relatório de risco gerado; respostas 2xx | — |
| FP-CT-23 | Inconclusivo | 422 e “Não foi possível concluir” por destinatário inválido; validação esperada | — |
| FP-CT-24 | Aprovado | Atividades criadas (201×3) | — |
| FP-CT-25 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-26 | Aprovado com ressalva | Pesquisa feita na própria tela, sem requisição | — |
| FP-CT-27 | Parcial | 1ª tentativa: 400 e “Erro ao salvar produto” (mensagem genérica); cadastro concluído depois (201×2) | — |
| FP-CT-28 | Aprovado | Notificação criada (201) | — |
| FP-CT-29 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-30 | Aprovado com ressalva | Cadastro com 201×2; a listagem de bandeiras não exibe registros (reproduzido em 18/11) | BUG-010 |
| FP-CT-31 | Parcial | Cadastro aceito (201×2); edição falhou: 500 e “Erro ao salvar pergunta” a 0:32 | BUG-009 |
| FP-CT-32 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-33 | Reprovado | Edição falhou com 500 (formulário em salvamento a 0:09) | BUG-009 |
| FP-CT-34 | Aprovado | Categoria criada (201×2) | — |
| FP-CT-35 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-36 | Aprovado com ressalva | Consulta e edição sem erro (2xx) | — |
| FP-CT-37 | Aprovado | Modelo criado (201) | — |
| FP-CT-38 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-39 | Aprovado com ressalva | Inativação sem erro (2xx) | — |
| FP-CT-40 | Aprovado com ressalva | Consulta sem erro (2xx) | — |
| FP-CT-41 | Aprovado | Ficha criada (201×2) | — |
| FP-CT-42 | Aprovado com ressalva | Enquete salva sem erro (2xx) | — |
| FP-CT-43 | Aprovado com ressalva | Inativação e exclusão sem erro (2xx) | — |
| FP-CT-44 | Aprovado com ressalva | Inativação e exclusão sem erro (2xx) | — |
| FP-CT-45 | Aprovado | Tipo criado (201×2) e alterado | — |
| FP-CT-46 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-47 | Reprovado | Cadastro falhou com 500 repetido; lista permaneceu com 8 registros; edição e exclusão não comprovadas | BUG-011 |
| FP-CT-48 | Aprovado | Função criada (201×2) com permissões | — |
| FP-CT-49 | Aprovado | Colaborador criado (201×2) | — |
| FP-CT-50 | Aprovado com ressalva | Edição e exclusão sem erro (2xx) | — |
| FP-CT-51 | Aprovado | Turma criada (201×2) | — |
| FP-CT-52 | Aprovado com ressalva | Exclusão e consulta sem erro (2xx) | — |
| FP-CT-53 | Reprovado | 500 ao salvar “master”; consulta posterior: “Nenhuma bandeira encontrada” | BUG-010 |
| FP-CT-54 | Aprovado | Tipo criado (201×2), consultado, editado e excluído | — |
| FP-CT-55 | Aprovado | Modelo criado (201) | — |
| FP-CT-56 | Parcial | Cadastro, inativação e alteração sem erro; exclusão: 500 e “Erro ao deletar Plano” a 0:57 | BUG-012 |
| FP-CT-57 | Parcial | Cadastro concluído (12→13); exclusão: 500 e “Erro ao deletar Grupo” (reproduzido em 18/11) | BUG-013 |
| FP-CT-58 | Aprovado com ressalva | Cadastro, alteração e exclusão sem erro (2xx) | — |
| FP-CT-59 | Aprovado | Turma SifitBox criada (201×2) | — |
| FP-CT-60 | Aprovado | Categoria criada (201×2), editada e excluída | — |
| FP-CT-61 | Aprovado com ressalva | Cadastro (201) e exclusão visíveis (7→6); 400 sem mensagem visível | — |
| FP-CT-62 | Parcial | Cadastro aceito (201); edição com imagem: 400 e “Erro ao salvar grupo” | BUG-014 |
| FP-CT-63 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-64 | Parcial | Cadastro aceito (201×3); salvamento com imagem: 400 ×3 e “Erro ao salvar exercício” | BUG-014 |
| FP-CT-65 | Aprovado com ressalva | Exclusão sem erro (2xx) | — |
| FP-CT-66 | Aprovado | Ficha criada (201) | — |
| FP-CT-67 | Aprovado com ressalva | Inativação e exclusão sem erro (2xx) | — |
| FP-CT-68 | Aprovado com ressalva | Cadastro pela matrícula; 400 = validação “Selecione o Tipo de Pagamento”; conta listada depois | — |
| FP-CT-69 | Aprovado | Conta criada (201×2), editada e excluída | — |
| FP-CT-70 | Aprovado com ressalva | 423 corresponde à regra de caixa fechado (ajuste administrativo) | — |
| FP-CT-71 | Parcial | Avaliação criada (201×2); salvamento posterior: 500 (“Salvando...” a 0:45) | BUG-015 |
| FP-CT-72 | Parcial | 1º salvamento: 500 com “Salvando...” travado; cadastro concluído depois (201) | BUG-016 |
| FP-CT-73 | Aprovado com ressalva | Geração e filtro com respostas 2xx; conteúdo dos PDFs não verificado | — |

## Comparação com o banco do Workbench

Os valores digitados mais distintivos foram procurados nas 207 colunas de texto do esquema `u339572246_alfa1` (somente leitura): “treinar pernas”, “Treino de Pernas”, “Pernas”, “Alimentação2”, “Energia”, “Iniciante”, “master”, “Enquete test”, “turma test”, “testeeee”, “testes_01”, “eeeaae”, “qqq222” e “aaaa1”. **Nenhuma ocorrência foi encontrada** ([DB-05](../evidencias/imagens/DB-05-valores-dos-videos-nao-encontrados.jpg)).

O resultado é coerente com o restante da conferência. Os vídeos gravam no backend `backsifitalfa.centrion.com.br`, e o banco acessível pelo Workbench não contém nenhum registro criado neles.

## Pendências

1. Conferir a persistência no banco usado por `backsifitalfa`, por exemplo procurando “Como treinar pernas corretamente?”, “Treino de Pernas”, “turma test” e “testes_01”.
