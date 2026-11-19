# Consolidação das evidências da equipe

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../Cenarios-de-testes/) conforme a [correspondência de IDs](correspondencia-de-ids.md).

**Data:** 18/11/2026 · **Situação:** 73 casos da equipe com veredito; trabalho local e da equipe conciliados; banco do `sifit` identificado; persistência dos vídeos do `sifitalfa` não verificável.

## Fonte e dimensão

Material de Felipe Pestana, [Pestanadev/extensao-qa — SIFIT](https://github.com/Pestanadev/extensao-qa/tree/82b552089584394795036768a169cfb24206cc51/SIFIT), revisão `82b552089584394795036768a169cfb24206cc51`. Foram lidos o README, os quatro documentos principais e os 37 arquivos de cenários SIFIT. O conteúdo OrangeHRM herdado do exemplo não integra esta contagem.

| Indicador da fonte | Quantidade |
| --- | ---: |
| Arquivos de cenários | 37 |
| Casos identificados | 73 |
| Links JAM distintos | 73 |
| Links classificados como vídeo | 70 |
| Links classificados como print | 3 |
| Resultados “A confirmar” | 70 |
| Resultados “FALHOU” | 2 |
| Resultado “PARCIAL” | 1 |
| Bugs descritos pelo autor | 3 |

Os 73 casos não equivalem a 73 testes aprovados. Vários deles agrupam operações de CRUD, e o veredito local separa as operações quando uma delas falha.

## Revisão das evidências

Os 73 links foram lidos em 18/11/2026 (abas Info, Actions e Network do JAM). Os 19 registros com erro do backend foram assistidos nos pontos de erro. Fundamentos e critérios estão na [análise dos vídeos](analise-dos-videos.md).

| Resultado local | Casos |
| --- | ---: |
| Aprovado | 20 |
| Aprovado com ressalva | 32 |
| Parcial | 8 |
| Reprovado | 7 |
| Inconclusivo | 6 |

Os três bugs da fonte foram incorporados à numeração única: FP-BUG-01 virou BUG-006, FP-BUG-02 virou BUG-007 e FP-BUG-03 virou BUG-009. Os vídeos revelaram mais oito defeitos (BUG-008 e BUG-010 a BUG-016), entre eles as falhas de exclusão de plano e de grupo. O FP-CT-02 confirma o BUG-001, já registrado localmente.

## Ambientes e banco

| Ambiente | API | Banco | Uso |
| --- | --- | --- | --- |
| `sifit.centrion.com.br` | `backendsifit.centrion.com.br` | `u339572246_sifit_alfa` (comprovado por grupo-sonda) | Exploração local, FP-CT-01 a 04 e execução complementar |
| `sifitalfa.centrion.com.br` | `backsifitalfa.centrion.com.br` | Não identificado | FP-CT-05 a 73 |

O slide 6 da disciplina indica, em texto, o esquema `u339572246_alfa1`, que pertence a uma loja virtual de outro projeto. Os prints dos slides 7 e 8 usam `u339572246_sifit_alfa`, que é o banco do `sifit`. Nesse banco não há nenhum rastro dos vídeos do `sifitalfa`: nem os valores digitados, nem gravações nas janelas de horário, nem as exclusões de contas de 17/11 na tabela `logs`. A investigação completa está na [conferência do banco](conferencia-do-banco.md).

Consequência: a persistência dos 69 casos do `sifitalfa` não pode ser comprovada por SELECT nesta entrega. A execução complementar no `sifit` comprovou persistência no banco para cinco operações: grupo-sonda, cadastro e alteração de cliente, matrícula com desconto e bandeira.

## Conciliação entre trabalho local e da equipe

| Área | Exploração local (21/10) | Casos da equipe | Execução complementar (18/11) | Conciliação |
| --- | --- | --- | --- | --- |
| RF01 Login | CT-RF01-01 a 06 | FP-CT-01 a 03 | — | FP-CT-03 = CT-RF01-01; FP-CT-01 = CT-RF01-03; FP-CT-02 = CT-RF01-04 (BUG-001). A senha inválida já está coberta pelo CT-RF01-02 |
| RF02/03 Painéis | CT-RF02-01, 02-02, 03-01 | FP-CT-04 | CT2-RF02-01 | Botão do período: FP-BUG-01, reproduzido como BUG-006 |
| RF05 Presenças | — | — | CT2-RF05-01, 02 | Lacuna coberta; BUG-021 e INV-006 |
| RF06 SifitBox aulas | — | — | CT2-RF06-01 | Bloqueado: módulo desabilitado para a empresa |
| RF07 Clientes | CT-RF07-08 (BUG-004) | — | CT2-RF07-01 a 06 | Lacuna coberta; BUG-019 e BUG-020 |
| RF08 Matrículas | CT-RF08-08 | FP-CT-68 (matrícula via contas) | CT2-RF08-01 a 04 | Lacuna coberta; BUG-018 e INV-016 |
| RF09 Avaliações | CT-RF09-08, 09 (BUG-003) | FP-CT-71 | — | Ocorrências distintas: BUG-003 (unidade) e BUG-015 (500 ao salvar) |
| RF16 Grupos | — | FP-CT-57 | CT2-RF16-01, 02 | Exclusão reproduzida no `sifit` (BUG-013) |
| RF28 Bandeiras | — | FP-CT-30, 53 | CT2-RF28-01 | Reproduzido no `sifit`; causa provável identificada no banco (BUG-010) |
| RF33 Atividades | — | FP-CT-24 a 26 | CT2-RF33-01 a 03 | Edição de atividade, pendência apontada pelo colega, coberta; BUG-017 |
| RF43 Configurações | CT-RF43-01 (navegação) | FP-CT-13 a 19 | — | Complementares: o local navegou sem salvar; a equipe salvou cada aba (BUG-008 em Design) |
| RF46 Perfil | CT-RF46-01 (BUG-005) | FP-CT-06 | — | Complementares (perfil × notificações) |

Com a execução complementar, 45 dos 46 requisitos têm ao menos um caso executado. RF06 está bloqueado pelo ambiente. Os números consolidados (108 verificações e 21 bugs) estão no [relatório de execução](../4-Relatorio-dos-testes.md).

## Módulos da fonte e requisitos

| Módulo da fonte | Casos recebidos | RF relacionado |
| --- | --- | --- |
| Login | FP-CT-01, FP-CT-02, FP-CT-03 | RF01 |
| Dashboard | FP-CT-04, FP-CT-05 | RF02, RF03, RF04 |
| Notificações | FP-CT-06 | RF46 |
| Financeiro | FP-CT-07, FP-CT-08, FP-CT-09, FP-CT-10, FP-CT-11 | RF02, RF34, RF21 |
| Treinos | FP-CT-12 | RF44 |
| Configurações | FP-CT-13 a FP-CT-19 | RF43 |
| Inteligência e Automação | FP-CT-20 a FP-CT-23 | RF42, RF41 |
| Atividades | FP-CT-24, FP-CT-25, FP-CT-26 | RF33 |
| Produtos | FP-CT-27, FP-CT-44 | RF35 |
| Aplicativo | FP-CT-28, FP-CT-29 | RF45 |
| Bandeiras de Cartão | FP-CT-30, FP-CT-53 | RF28 |
| Perguntas | FP-CT-31, FP-CT-32, FP-CT-33 | RF40 |
| Categorias | FP-CT-34, FP-CT-35, FP-CT-36 | RF39 |
| Modelos de Análise | FP-CT-37 a FP-CT-40 | RF38 |
| Fichas de Análise | FP-CT-41 | RF37 |
| Enquetes | FP-CT-42, FP-CT-43 | RF36 |
| Tipos de Documentos | FP-CT-45, FP-CT-46 | RF32 |
| Fornecedores | FP-CT-47 | RF31 |
| Funções | FP-CT-48 | RF30 |
| Colaboradores | FP-CT-49, FP-CT-50 | RF29 |
| Turmas | FP-CT-51, FP-CT-52, FP-CT-59 | RF17, RF19 |
| Tipos de Pagamento | FP-CT-54 | RF27 |
| Modelos de Contrato | FP-CT-55 | RF26 |
| Planos | FP-CT-56 | RF25 |
| Grupos | FP-CT-57 | RF16 |
| Prospecção | FP-CT-58 | RF24 |
| Categorias de Crossfit | FP-CT-60 | RF18 |
| Objetivos de Treino | FP-CT-61 | RF15 |
| Grupos Musculares | FP-CT-62, FP-CT-63 | RF14 |
| Biblioteca de Exercícios | FP-CT-64, FP-CT-65 | RF13 |
| Fichas de Treino | FP-CT-66, FP-CT-67 | RF12 |
| Contas a Receber | FP-CT-68 | RF10 |
| Contas a Pagar | FP-CT-69 | RF11 |
| Caixas | FP-CT-70 | RF20 |
| Avaliações | FP-CT-71 | RF09 |
| Despesas Fixas | FP-CT-72 | RF22 |
| Relatórios | FP-CT-73 | RF23 |

“Modelos/Fichas de Análise” correspondem às telas de anamnese (`/anamnese/modelos` e `/anamneses`), conforme as URLs registradas nos vídeos.

## Pendências de consolidação

| Pendência | Estado |
| --- | --- |
| Revisão das 73 mídias e classificação por operação | Concluída (veredito por caso) |
| Conciliação com os 15 resultados históricos locais | Concluída (tabela acima) |
| Identificação do banco do `sifit` | Concluída: `u339572246_sifit_alfa` |
| Identificação do banco do `sifitalfa` | Pendente: depende do professor ou do responsável pelo ambiente |
| Persistência dos 69 casos do `sifitalfa` | Não verificável sem esse banco |
| Usuário do Workbench com privilégios de escrita | Ambiente de teste; recomendação registrada |
| Dados usados no bug de modelo de ficha | Campo incompleto no relato da fonte |
| Conclusão do relatório recebido | Ainda contém campo a preencher na fonte |
| Dados acadêmicos (integrantes, turma, professor, título) | Pendente: informação a ser preenchida pela equipe |

## Materiais acadêmicos consultados

Os seis PDFs fornecidos foram examinados. Os materiais sobre princípios, processo e erro/defeito/falha sustentam priorização, rastreabilidade e comparação entre resultado esperado e observado. A apresentação da Aula 7 forneceu os acessos ao sistema e ao banco.

Na apresentação do segundo bimestre, a página 4 descreve a documentação SIFIT individual, e a página 5 descreve separadamente o trabalho em grupo do TCC (manual, sistema/banco e vídeo). Essas duas atividades não foram tratadas como uma única exigência. A organização atual em grupo e a aceitação de prints seguem a orientação posterior relatada pelo integrante.

Revisão e execução complementar realizadas com Claude em 18/11/2026. O banco foi consultado apenas com leitura; as alterações de dados ocorreram somente pela interface do `sifit`, com registros de teste identificados pelo prefixo QA/SONDA.
