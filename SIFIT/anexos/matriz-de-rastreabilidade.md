# Matriz de rastreabilidade

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../Cenarios-de-testes/) conforme a [correspondência de IDs](correspondencia-de-ids.md).

A matriz relaciona as 46 áreas funcionais às 15 verificações locais de 21/10, aos 73 casos da equipe (vídeos JAM, com veredito no [registro da equipe](casos-originais-da-equipe.md)), aos 20 casos da execução complementar de 18/11 e às ocorrências consolidadas (BUG-001 a BUG-021; INV abertas). Com isso, 45 dos 46 requisitos têm ao menos um caso executado; RF06 está bloqueado no ambiente. Os 44 destinos do menu correspondem a RF02–RF45; autenticação e controles globais completam o levantamento.

A execução futura está organizada em fluxos com comprovação de CRUD no banco e capturas para consultas e relatórios. A coluna Planejamento remete ao plano de execução e evidências; não representa execução concluída.

| RF | Área e inventário | Casos locais (21/10) | Casos da equipe (FP-CT) | Execução 18/11 | Planejamento | Ocorrências |
| --- | --- | --- | --- | --- | --- | --- |
| RF01 | [Autenticação e sessão](inventario/01-acesso-e-principal.md) | [6](../Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | 01–03 | — | PF01 | BUG-001 |
| RF02 | [Página Inicial](inventario/01-acesso-e-principal.md) | [2](../Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | 04, 07, 08, 10 | CT2-RF02-01 | PF02, PF03 | BUG-006; INV-001 |
| RF03 | [Dashboard analítico](inventario/01-acesso-e-principal.md) | [1](../Cenarios-de-testes/CT_RF03_Dashboard-analitico.md) | 04 | — | PF04 | BUG-002 |
| RF04 | [Check-in](inventario/01-acesso-e-principal.md) | — | 05 | — | FL04 | — |
| RF05 | [Presenças](inventario/01-acesso-e-principal.md) | — | — | CT2-RF05-01, 02 | FL04 | BUG-021; INV-006 |
| RF06 | [SifitBox — aulas](inventario/01-acesso-e-principal.md) | — | — | CT2-RF06-01 (bloqueado) | FL09 | — |
| RF07 | [Clientes](inventario/02-operacao.md) | [1](../Cenarios-de-testes/CT_RF07_Clientes.md) | — | CT2-RF07-01 a 06 | FL02 | BUG-004, BUG-019, BUG-020; INV-017 |
| RF08 | [Matrículas](inventario/02-operacao.md) | [1](../Cenarios-de-testes/CT_RF08_Matriculas.md) | — | CT2-RF08-01 a 04 | FL03 | BUG-018; INV-016 |
| RF09 | [Avaliações físicas](inventario/02-operacao.md) | [2](../Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md) | 71 | — | FL05 | BUG-003, BUG-015 |
| RF10 | [Contas a Receber](inventario/02-operacao.md) | — | 68 | — | FL11 | — |
| RF11 | [Contas a Pagar](inventario/02-operacao.md) | — | 69 | — | FL12 | — |
| RF12 | [Fichas de Treino](inventario/03-treinamento.md) | — | 66, 67 | — | FL07 | — |
| RF13 | [Exercícios](inventario/03-treinamento.md) | — | 64, 65 | — | FL06 | BUG-014 |
| RF14 | [Grupos Musculares](inventario/03-treinamento.md) | — | 62, 63 | — | FL06 | BUG-014 |
| RF15 | [Objetivos Treino](inventario/03-treinamento.md) | — | 61 | — | FL07 | — |
| RF16 | [Grupos](inventario/03-treinamento.md) | — | 57 | CT2-RF16-01, 02 | FL01 | BUG-013 |
| RF17 | [Turmas](inventario/03-treinamento.md) | — | 51, 52 | — | FL08 | — |
| RF18 | [Categorias Crossfit](inventario/03-treinamento.md) | — | 60 | — | FL09 | — |
| RF19 | [SifitBox — turmas e modalidades](inventario/03-treinamento.md) | — | 59 | — | FL09 | — |
| RF20 | [Caixas](inventario/04-financeiro-e-comercial.md) | — | 70 | — | FL13 | — |
| RF21 | [Pagar.me](inventario/04-financeiro-e-comercial.md) | — | 11 | — | Bloqueado: sandbox Pagar.me | — |
| RF22 | [Despesas Fixas](inventario/04-financeiro-e-comercial.md) | — | 72 | — | FL12 | BUG-016 |
| RF23 | [Relatórios](inventario/04-financeiro-e-comercial.md) | — | 73 | — | PF05, PF06, PF07, PF08, PF09, PF10, PF11 | — |
| RF24 | [Prospecção](inventario/04-financeiro-e-comercial.md) | — | 58 | — | FL16 | — |
| RF25 | [Planos](inventario/04-financeiro-e-comercial.md) | — | 56 | — | FL01 | BUG-012 |
| RF26 | [Modelos de Contrato](inventario/04-financeiro-e-comercial.md) | — | 55 | — | FL17 | — |
| RF27 | [Tipos de Pagamento](inventario/04-financeiro-e-comercial.md) | — | 54 | — | FL14 | — |
| RF28 | [Bandeiras](inventario/04-financeiro-e-comercial.md) | — | 30, 53 | CT2-RF28-01 | FL14 | BUG-010 |
| RF29 | [Colaboradores](inventario/05-gestao.md) | — | 49, 50 | — | FL15 | — |
| RF30 | [Funções e permissões](inventario/05-gestao.md) | — | 48 | — | FL15 | — |
| RF31 | [Fornecedores](inventario/05-gestao.md) | — | 47 | — | FL10 | BUG-011 |
| RF32 | [Tipos de Documentos](inventario/05-gestao.md) | — | 45, 46 | — | FL10 | — |
| RF33 | [Atividades](inventario/05-gestao.md) | — | 24–26 | CT2-RF33-01 a 03 | FL18 | BUG-017 |
| RF34 | [Pontuação](inventario/05-gestao.md) | — | 09 | — | FL18 | — |
| RF35 | [Produtos](inventario/05-gestao.md) | — | 27, 44 | — | FL18 | — |
| RF36 | [Enquetes](inventario/05-gestao.md) | — | 42, 43 | — | FL19 | — |
| RF37 | [Fichas de Anamnese](inventario/06-saude-inteligencia-configuracoes.md) | — | 41 | — | FL20 | — |
| RF38 | [Modelos de Anamnese](inventario/06-saude-inteligencia-configuracoes.md) | — | 37–40 | — | FL20 | — |
| RF39 | [Categorias de Anamnese](inventario/06-saude-inteligencia-configuracoes.md) | — | 34–36 | — | FL20 | — |
| RF40 | [Perguntas de Anamnese](inventario/06-saude-inteligencia-configuracoes.md) | — | 31–33 | — | FL20 | BUG-009 |
| RF41 | [Inteligência e Automação](inventario/06-saude-inteligencia-configuracoes.md) | — | 21–23 | — | FL22 | — |
| RF42 | [Resultados IA](inventario/06-saude-inteligencia-configuracoes.md) | — | 20 | — | FL22 | — |
| RF43 | [Configurações](inventario/06-saude-inteligencia-configuracoes.md) | [1](../Cenarios-de-testes/CT_RF43_Configuracoes.md) | 13–19 | — | FL21 | BUG-008 |
| RF44 | [Modelos de Ficha](inventario/06-saude-inteligencia-configuracoes.md) | — | 12 | — | FL07 | BUG-007 |
| RF45 | [Aplicativo](inventario/06-saude-inteligencia-configuracoes.md) | — | 28, 29 | — | Bloqueado: ambiente do aplicativo | — |
| RF46 | [Meu perfil e controles globais](inventario/01-acesso-e-principal.md) | [1](../Cenarios-de-testes/CT_RF46_Meu-perfil-e-controles-globais.md) | 06 | — | PF12 | BUG-005 |
