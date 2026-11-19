# ✅ **Relatório Final de Execução de Testes - SIFIT**

**Sistema testado:** SIFIT — sistema de gestão de academias (versão web)  
**Responsável:** Arthur Soares Gardim (RA 14526), Felipe Pestana (RA 14530), Guilherme Ananias Calixto Ribeiro (RA 14652), Kaiki Teles de Andrade (RA 14518)  
**Data de execução:** 01/10/2026 a 18/11/2026  
**Ambiente:** ambientes de testes da disciplina

* Sistema operacional: Windows 11
* Navegadores: Google Chrome 157 (gravações Jam) e navegador integrado baseado em Chromium
* URLs: [https://sifit.centrion.com.br](https://sifit.centrion.com.br) e [https://sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)
* Banco de dados: MySQL, consultado em modo leitura pelo MySQL Workbench

---

## 📊 **Resumo da Execução**

| Total de Casos de Teste | Casos Passaram | Casos Falharam | Não concluídos | Bugs Registrados |
| ----------------------- | -------------- | -------------- | -------------- | ---------------- |
| 108 | 71 | 28 | 9 | 21 |

**Detalhamento dos resultados**

| Resultado | Casos | Critério |
| --- | ---: | --- |
| Aprovado | 37 | Resultado esperado atendido |
| Aprovado com ressalva | 34 | Fluxo sem erro, com efeito não totalmente visível ou não conferido no banco |
| Parcial | 8 | Ao menos uma operação do caso falhou (contado em “Falharam”) |
| Reprovado | 20 | Resultado diferente do esperado |
| Inconclusivo | 8 | Evidência ou pré-condição insuficiente (ex.: integração desconectada) |
| Bloqueado | 1 | Funcionalidade indisponível no ambiente |

Origem dos casos: 15 da exploração local (21/10/2026), 73 gravados pela equipe com Jam (01/10 a 17/11/2026) e 20 da execução complementar (18/11/2026).

---

## 🔍 **Cobertura por Módulo**

| Código RF | Módulo | Casos Testados | Casos Passaram | Bugs encontrados | Bug(s) Associado(s) |
| --------- | ------ | -------------- | -------------- | ---------------- | ------------------- |
| [RF01](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | 9 | 7 | 1 | BUG-001 |
| [RF02](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | 7 | 1 | 1 | BUG-006 |
| [RF03](Cenarios-de-testes/CT_RF03_Dashboard-analitico.md) | Dashboard analítico | 1 | 0 | 1 | BUG-002 |
| [RF04](Cenarios-de-testes/CT_RF04_Check-in.md) | Check-in | 1 | 1 | 0 | - |
| [RF05](Cenarios-de-testes/CT_RF05_Presencas.md) | Presenças | 2 | 0 | 1 | BUG-021 |
| [RF06](Cenarios-de-testes/CT_RF06_SifitBox-aulas.md) | SifitBox — aulas | 1 | 0 | 0 | - |
| [RF07](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | 7 | 4 | 3 | BUG-004, BUG-019, BUG-020 |
| [RF08](Cenarios-de-testes/CT_RF08_Matriculas.md) | Matrículas | 5 | 4 | 1 | BUG-018 |
| [RF09](Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md) | Avaliações físicas | 3 | 1 | 2 | BUG-003, BUG-015 |
| [RF10](Cenarios-de-testes/CT_RF10_Contas-a-Receber.md) | Contas a Receber | 1 | 1 | 0 | - |
| [RF11](Cenarios-de-testes/CT_RF11_Contas-a-Pagar.md) | Contas a Pagar | 1 | 1 | 0 | - |
| [RF12](Cenarios-de-testes/CT_RF12_Fichas-de-Treino.md) | Fichas de Treino | 2 | 2 | 0 | - |
| [RF13](Cenarios-de-testes/CT_RF13_Exercicios.md) | Exercícios | 2 | 1 | 1 | BUG-014 |
| [RF14](Cenarios-de-testes/CT_RF14_Grupos-Musculares.md) | Grupos Musculares | 2 | 1 | 1 | BUG-014 |
| [RF15](Cenarios-de-testes/CT_RF15_Objetivos-Treino.md) | Objetivos Treino | 1 | 1 | 0 | - |
| [RF16](Cenarios-de-testes/CT_RF16_Grupos.md) | Grupos | 3 | 1 | 1 | BUG-013 |
| [RF17](Cenarios-de-testes/CT_RF17_Turmas.md) | Turmas | 2 | 2 | 0 | - |
| [RF18](Cenarios-de-testes/CT_RF18_Categorias-Crossfit.md) | Categorias Crossfit | 1 | 1 | 0 | - |
| [RF19](Cenarios-de-testes/CT_RF19_SifitBox-turmas-e-modalidades.md) | SifitBox — turmas e modalidades | 1 | 1 | 0 | - |
| [RF20](Cenarios-de-testes/CT_RF20_Caixas.md) | Caixas | 1 | 1 | 0 | - |
| [RF21](Cenarios-de-testes/CT_RF21_Pagar-me.md) | Pagar.me | 1 | 0 | 0 | - |
| [RF22](Cenarios-de-testes/CT_RF22_Despesas-Fixas.md) | Despesas Fixas | 1 | 0 | 1 | BUG-016 |
| [RF23](Cenarios-de-testes/CT_RF23_Relatorios.md) | Relatórios | 1 | 1 | 0 | - |
| [RF24](Cenarios-de-testes/CT_RF24_Prospeccao.md) | Prospecção | 1 | 1 | 0 | - |
| [RF25](Cenarios-de-testes/CT_RF25_Planos.md) | Planos | 1 | 0 | 1 | BUG-012 |
| [RF26](Cenarios-de-testes/CT_RF26_Modelos-de-Contrato.md) | Modelos de Contrato | 1 | 1 | 0 | - |
| [RF27](Cenarios-de-testes/CT_RF27_Tipos-de-Pagamento.md) | Tipos de Pagamento | 1 | 1 | 0 | - |
| [RF28](Cenarios-de-testes/CT_RF28_Bandeiras.md) | Bandeiras | 3 | 1 | 1 | BUG-010 |
| [RF29](Cenarios-de-testes/CT_RF29_Colaboradores.md) | Colaboradores | 2 | 2 | 0 | - |
| [RF30](Cenarios-de-testes/CT_RF30_Funcoes-e-permissoes.md) | Funções e permissões | 1 | 1 | 0 | - |
| [RF31](Cenarios-de-testes/CT_RF31_Fornecedores.md) | Fornecedores | 1 | 0 | 1 | BUG-011 |
| [RF32](Cenarios-de-testes/CT_RF32_Tipos-de-Documentos.md) | Tipos de Documentos | 2 | 2 | 0 | - |
| [RF33](Cenarios-de-testes/CT_RF33_Atividades.md) | Atividades | 6 | 5 | 1 | BUG-017 |
| [RF34](Cenarios-de-testes/CT_RF34_Pontuacao.md) | Pontuação | 1 | 1 | 0 | - |
| [RF35](Cenarios-de-testes/CT_RF35_Produtos.md) | Produtos | 2 | 1 | 0 | - |
| [RF36](Cenarios-de-testes/CT_RF36_Enquetes.md) | Enquetes | 2 | 2 | 0 | - |
| [RF37](Cenarios-de-testes/CT_RF37_Fichas-de-Anamnese.md) | Fichas de Anamnese | 1 | 1 | 0 | - |
| [RF38](Cenarios-de-testes/CT_RF38_Modelos-de-Anamnese.md) | Modelos de Anamnese | 4 | 4 | 0 | - |
| [RF39](Cenarios-de-testes/CT_RF39_Categorias-de-Anamnese.md) | Categorias de Anamnese | 3 | 3 | 0 | - |
| [RF40](Cenarios-de-testes/CT_RF40_Perguntas-de-Anamnese.md) | Perguntas de Anamnese | 3 | 1 | 1 | BUG-009 |
| [RF41](Cenarios-de-testes/CT_RF41_Inteligencia-e-Automacao.md) | Inteligência e Automação | 3 | 2 | 0 | - |
| [RF42](Cenarios-de-testes/CT_RF42_Resultados-IA.md) | Resultados IA | 1 | 1 | 0 | - |
| [RF43](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | 8 | 6 | 1 | BUG-008 |
| [RF44](Cenarios-de-testes/CT_RF44_Modelos-de-Ficha.md) | Modelos de Ficha | 1 | 0 | 1 | BUG-007 |
| [RF45](Cenarios-de-testes/CT_RF45_Aplicativo.md) | Aplicativo | 2 | 2 | 0 | - |
| [RF46](Cenarios-de-testes/CT_RF46_Meu-perfil-e-controles-globais.md) | Meu perfil e controles globais | 2 | 1 | 1 | BUG-005 |

---

## 🐞 **Resumo dos Bugs Reportados**

| ID | Título | Severidade | Status |
| ------- | ------- | ---------- | ------ |
| [BUG-001](3-Relatorio-de-Bugs.md#bug-001) | Recuperação de senha não apresenta fluxo ou orientação | Média | Aberto |
| [BUG-002](3-Relatorio-de-Bugs.md#bug-002) | Dashboard exibe título Despesas Fixas | Baixa | Aberto |
| [BUG-003](3-Relatorio-de-Bugs.md#bug-003) | IMC exibe unidade kg/m³ | Baixa | Aberto |
| [BUG-004](3-Relatorio-de-Bugs.md#bug-004) | Perfil apresenta vencimento com ano negativo | Média | Aberto |
| [BUG-005](3-Relatorio-de-Bugs.md#bug-005) | Meu perfil apresenta conteúdo de demonstração | Média | Aberto |
| [BUG-006](3-Relatorio-de-Bugs.md#bug-006) | Botão ao lado do período do painel não executa ação | Baixa | Aberto |
| [BUG-007](3-Relatorio-de-Bugs.md#bug-007) | Criação de modelo de ficha retorna 400 | Média | Aberto |
| [BUG-008](3-Relatorio-de-Bugs.md#bug-008) | Salvar aba Design das configurações retorna 400 | Baixa | Aberto |
| [BUG-009](3-Relatorio-de-Bugs.md#bug-009) | Edição de pergunta de anamnese retorna 500 | Média | Aberto |
| [BUG-010](3-Relatorio-de-Bugs.md#bug-010) | Bandeiras cadastradas não aparecem na listagem | Alta | Aberto |
| [BUG-011](3-Relatorio-de-Bugs.md#bug-011) | Cadastro de fornecedor retorna 500 | Alta | Aberto |
| [BUG-012](3-Relatorio-de-Bugs.md#bug-012) | Exclusão de plano retorna 500 | Média | Aberto |
| [BUG-013](3-Relatorio-de-Bugs.md#bug-013) | Exclusão de grupo retorna 500 | Média | Aberto |
| [BUG-014](3-Relatorio-de-Bugs.md#bug-014) | Salvar grupo muscular ou exercício com imagem retorna 400 | Média | Aberto |
| [BUG-015](3-Relatorio-de-Bugs.md#bug-015) | Salvar avaliação física retorna 500 | Alta | Aberto |
| [BUG-016](3-Relatorio-de-Bugs.md#bug-016) | Cadastro de despesa fixa falha com 500 na primeira tentativa | Média | Aberto |
| [BUG-017](3-Relatorio-de-Bugs.md#bug-017) | Atividade é salva com todos os campos vazios | Média | Aberto |
| [BUG-018](3-Relatorio-de-Bugs.md#bug-018) | Desconto da matrícula não é aplicado ao valor | Alta | Aberto |
| [BUG-019](3-Relatorio-de-Bugs.md#bug-019) | Exclusão de cliente retorna erro interno 500 | Média | Aberto |
| [BUG-020](3-Relatorio-de-Bugs.md#bug-020) | Perfil de cliente sem contato exibe “null” e objetivos fictícios | Média | Aberto |
| [BUG-021](3-Relatorio-de-Bugs.md#bug-021) | Filtro “Este mês” de Presenças aplica os últimos 30 dias | Baixa | Aberto |

---

## 📈 **Gráfico de Resultado (Texto Alternativo)**

**Casos por status:**

* ✅ Passaram: 71 (aprovados 37; com ressalva 34)
* ❌ Falharam: 28 (reprovados 20; parciais 8)
* ⚠️ Não concluídos: 9 (inconclusivos 8; bloqueado 1)

**Severidade dos bugs:**

* 🟥 Alta: 4
* 🟨 Média: 12
* 🟩 Baixa: 5

---

## 📋 **Resultado por caso de teste**

| ID | Módulo | Caso | Resultado | Evidência | Bug |
| --- | --- | --- | --- | --- | --- |
| [C01-CT01](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Entrar com credenciais válidas | Aprovado | [Captura](evidencias/imagens/EXE-login-sucesso.png) | - |
| [C01-CT02](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Rejeitar credenciais inválidas | Aprovado | [Captura](evidencias/imagens/EXE-login-invalido.png) | - |
| [C01-CT03](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Impedir entrada com campos vazios | Aprovado | [Captura](evidencias/imagens/EXE-login-vazio.png) | - |
| [C01-CT04](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Abrir recuperação de senha | Reprovado | [Captura](evidencias/imagens/BUG-001-recuperacao-senha.png) | BUG-001 |
| [C01-CT05](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Encerrar sessão | Aprovado | Registro textual | - |
| [C01-CT06](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Proteger rota após logout | Aprovado | Registro textual | - |
| [C01-CT07](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Login — Login com campos em branco | Aprovado com ressalva | [Print (Jam)](https://jam.dev/c/76ae1224-ce04-4e4a-8c98-7554ea821020) | - |
| [C01-CT08](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Login — Botão "Esqueci minha senha" | Reprovado | [Print (Jam)](https://jam.dev/c/e4dded02-6f23-43cc-832a-fedf751e0c06) | BUG-001 |
| [C01-CT09](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md) | Autenticação e sessão | Login — Acesso com credenciais corretas | Aprovado | [Vídeo (Jam)](https://jam.dev/c/50d88cbd-0fc5-4602-a937-6f27e3e9a016) | - |
| [C02-CT01](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | Carregar Página Inicial | Aprovado | [Captura](evidencias/imagens/EXE-login-sucesso.png) | - |
| [C02-CT02](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | Conciliar cartão Sem Matrículas e detalhamento | Inconclusivo | Registro textual | - |
| [C02-CT03](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | Dashboard — Botão ao lado de "Competência" sem funcionalidade | Reprovado | [Print (Jam)](https://jam.dev/c/4dfcb03a-bf1b-4d35-8874-31f846f25250) | BUG-006 |
| [C02-CT04](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | Financeiro — Cobrar todos via WhatsApp | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/72e56dc7-3c8c-43e9-9c8f-13a80cad87f1) | - |
| [C02-CT05](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | Financeiro — Exportar | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/7d3f61d3-5e70-43fd-b0da-0e380956c7cb) | - |
| [C02-CT06](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | Financeiro — Desistência - tela sem registros | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/c503ecf1-549d-4e44-8c9e-90e9038765b8) | - |
| [C02-CT07](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md) | Página Inicial | Acionar botão ao lado do período no painel | Reprovado | Registro textual (respostas HTTP) | BUG-006 |
| [C03-CT01](Cenarios-de-testes/CT_RF03_Dashboard-analitico.md) | Dashboard analítico | Identificar corretamente o Dashboard | Reprovado | [Captura](evidencias/imagens/BUG-002-dashboard-titulo.png) | BUG-002 |
| [C04-CT01](Cenarios-de-testes/CT_RF04_Check-in.md) | Check-in | Dashboard — Check-in | Aprovado | [Vídeo (Jam)](https://jam.dev/c/79d6a37a-eae8-44ed-8109-ca23cb0b0460) | - |
| [C05-CT01](Cenarios-de-testes/CT_RF05_Presencas.md) | Presenças | Consultar presenças por período | Inconclusivo | Registro textual (respostas HTTP) | - |
| [C05-CT02](Cenarios-de-testes/CT_RF05_Presencas.md) | Presenças | Aplicar filtro “Este mês” | Reprovado | Registro textual (respostas HTTP) | BUG-021 |
| [C06-CT01](Cenarios-de-testes/CT_RF06_SifitBox-aulas.md) | SifitBox — aulas | Acessar aulas do SifitBox | Bloqueado | Registro textual (respostas HTTP) | - |
| [C07-CT01](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | Tratar vencimento inválido no perfil | Reprovado | [Captura](evidencias/imagens/BUG-004-cliente-data.png) | BUG-004 |
| [C07-CT02](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | Validar obrigatórios do cadastro de cliente | Aprovado | Registro textual (respostas HTTP) | - |
| [C07-CT03](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | Cadastrar cliente com campos obrigatórios | Aprovado | Registro textual (respostas HTTP) | - |
| [C07-CT04](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | Consultar cliente por nome | Aprovado | Registro textual (respostas HTTP) | - |
| [C07-CT05](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | Exibir perfil de cliente novo | Reprovado | [Captura](evidencias/imagens/EXE2-RF07-cliente-null-contato.jpg) | BUG-020 |
| [C07-CT06](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | Alterar dados do cliente | Aprovado | Registro textual (respostas HTTP) | - |
| [C07-CT07](Cenarios-de-testes/CT_RF07_Clientes.md) | Clientes | Excluir cliente com matrícula cancelada | Reprovado | [Captura](evidencias/imagens/EXE2-RF07-erro-500-excluir-cliente.jpg) | BUG-019 |
| [C08-CT01](Cenarios-de-testes/CT_RF08_Matriculas.md) | Matrículas | Preencher matrícula por diária sem salvar | Aprovado | Registro textual | - |
| [C08-CT02](Cenarios-de-testes/CT_RF08_Matriculas.md) | Matrículas | Consultar matrículas | Aprovado | Registro textual (respostas HTTP) | - |
| [C08-CT03](Cenarios-de-testes/CT_RF08_Matriculas.md) | Matrículas | Cadastrar matrícula | Aprovado com ressalva | [Captura](evidencias/imagens/EXE2-RF08-matricula-ativa-cliente-440.jpg) | - |
| [C08-CT04](Cenarios-de-testes/CT_RF08_Matriculas.md) | Matrículas | Aplicar desconto na matrícula | Reprovado | Registro textual (respostas HTTP) | BUG-018 |
| [C08-CT05](Cenarios-de-testes/CT_RF08_Matriculas.md) | Matrículas | Cancelar matrícula | Aprovado com ressalva | Registro textual (respostas HTTP) | - |
| [C09-CT01](Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md) | Avaliações físicas | Calcular IMC na interface sem salvar | Aprovado | [Captura](evidencias/imagens/BUG-003-imc-unidade.png) | - |
| [C09-CT02](Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md) | Avaliações físicas | Exibir unidade correta do IMC | Reprovado | [Captura](evidencias/imagens/BUG-003-imc-unidade.png) | BUG-003 |
| [C09-CT03](Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md) | Avaliações físicas | Avaliações — Cadastro, consulta, edição e exclusão | Parcial | [Vídeo (Jam)](https://jam.dev/c/364850dc-8240-4fee-9169-465b5a9ef048) | BUG-015 |
| [C10-CT01](Cenarios-de-testes/CT_RF10_Contas-a-Receber.md) | Contas a Receber | Contas a Receber — Cadastro, consulta, edição e exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/d77ccbff-1206-4144-9702-1fb8068bfb56) | - |
| [C11-CT01](Cenarios-de-testes/CT_RF11_Contas-a-Pagar.md) | Contas a Pagar | Contas a Pagar — Cadastro, consulta, edição e exclusão | Aprovado | [Vídeo (Jam)](https://jam.dev/c/0510745c-7eec-4a3c-8134-9059959177c1) | - |
| [C12-CT01](Cenarios-de-testes/CT_RF12_Fichas-de-Treino.md) | Fichas de Treino | Fichas de Treino — Cadastro | Aprovado | [Vídeo (Jam)](https://jam.dev/c/bdb3fe53-a12a-49a1-a545-948ff43a715b) | - |
| [C12-CT02](Cenarios-de-testes/CT_RF12_Fichas-de-Treino.md) | Fichas de Treino | Fichas de Treino — Inativação e exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/84037d7e-56f9-41cd-8dec-17f9bcb06ab1) | - |
| [C13-CT01](Cenarios-de-testes/CT_RF13_Exercicios.md) | Exercícios | Biblioteca de Exercícios — Cadastro, consulta e edição | Parcial | [Vídeo (Jam)](https://jam.dev/c/d5d88e50-ae2a-4cae-8c14-719d9b9300be) | BUG-014 |
| [C13-CT02](Cenarios-de-testes/CT_RF13_Exercicios.md) | Exercícios | Biblioteca de Exercícios — Exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/c31e86c3-e6c0-49b0-8243-d83bf909dedd) | - |
| [C14-CT01](Cenarios-de-testes/CT_RF14_Grupos-Musculares.md) | Grupos Musculares | Grupos Musculares — Cadastro, consulta e edição | Parcial | [Vídeo (Jam)](https://jam.dev/c/6aee3782-c54d-4a79-8a42-55bd50d0c8df) | BUG-014 |
| [C14-CT02](Cenarios-de-testes/CT_RF14_Grupos-Musculares.md) | Grupos Musculares | Grupos Musculares — Exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/ef33cef8-c4d8-435d-b873-01a664f2c32b) | - |
| [C15-CT01](Cenarios-de-testes/CT_RF15_Objetivos-Treino.md) | Objetivos Treino | Objetivos de Treino — Cadastro, alteração e exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/903fd7be-ddd7-4a4b-9f0d-a3bb5b9157a3) | - |
| [C16-CT01](Cenarios-de-testes/CT_RF16_Grupos.md) | Grupos | Grupos — Cadastro, consulta, inativação e exclusão | Parcial | [Vídeo (Jam)](https://jam.dev/c/484df916-a8fd-4159-9528-4334f8919d80) | BUG-013 |
| [C16-CT02](Cenarios-de-testes/CT_RF16_Grupos.md) | Grupos | Cadastrar grupo (sonda) | Aprovado | [Captura](evidencias/imagens/SONDA-04-grupo-presente-no-banco-sifit-alfa.jpg) | - |
| [C16-CT03](Cenarios-de-testes/CT_RF16_Grupos.md) | Grupos | Excluir grupo sem vínculos | Reprovado | [Captura](evidencias/imagens/SONDA-03-erro-ao-deletar-grupo.jpg) | BUG-013 |
| [C17-CT01](Cenarios-de-testes/CT_RF17_Turmas.md) | Turmas | Turmas — Cadastro | Aprovado | [Vídeo (Jam)](https://jam.dev/c/6101c380-ae54-41d2-b1f2-7ac3920288ea) | - |
| [C17-CT02](Cenarios-de-testes/CT_RF17_Turmas.md) | Turmas | Turmas — Exclusão e consultas | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8c18cb4d-08e6-4fbf-b82e-d07efdd1fd9b) | - |
| [C18-CT01](Cenarios-de-testes/CT_RF18_Categorias-Crossfit.md) | Categorias Crossfit | Categorias de Crossfit — Cadastro, edição, consulta e exclusão | Aprovado | [Vídeo (Jam)](https://jam.dev/c/1df6ae82-8043-4ed1-b6e9-89c5ddc370d4) | - |
| [C19-CT01](Cenarios-de-testes/CT_RF19_SifitBox-turmas-e-modalidades.md) | SifitBox — turmas e modalidades | Turmas — SifitBox - cadastro de turma | Aprovado | [Vídeo (Jam)](https://jam.dev/c/8016aa6c-0813-48e2-a73b-ee93378894ac) | - |
| [C20-CT01](Cenarios-de-testes/CT_RF20_Caixas.md) | Caixas | Caixas — Cadastro, consulta e edição | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8031915b-199c-4103-81c8-1a9dcdb5d335) | - |
| [C21-CT01](Cenarios-de-testes/CT_RF21_Pagar-me.md) | Pagar.me | Financeiro — Pagar.me - solicitação de saque | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/f8f35850-c834-4a33-ac10-6aebb905b4d2) | - |
| [C22-CT01](Cenarios-de-testes/CT_RF22_Despesas-Fixas.md) | Despesas Fixas | Despesas Fixas — Cadastro, edição e exclusão | Parcial | [Vídeo (Jam)](https://jam.dev/c/573bcb6b-2dae-499f-9137-e9ee7a48167d) | BUG-016 |
| [C23-CT01](Cenarios-de-testes/CT_RF23_Relatorios.md) | Relatórios | Relatórios — Geração e filtro | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/91321d0b-ad8b-41d0-baf6-2fdf90e5dc87) | - |
| [C24-CT01](Cenarios-de-testes/CT_RF24_Prospeccao.md) | Prospecção | Prospecção — Cadastro, alteração e exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/1dfb1eb4-d3af-4361-9709-31d39274ca72) | - |
| [C25-CT01](Cenarios-de-testes/CT_RF25_Planos.md) | Planos | Planos — Cadastro, inativação, alteração e exclusão | Parcial | [Vídeo (Jam)](https://jam.dev/c/6ec365fc-5fee-4ebf-a9c4-cc8c42243f41) | BUG-012 |
| [C26-CT01](Cenarios-de-testes/CT_RF26_Modelos-de-Contrato.md) | Modelos de Contrato | Modelos de Contrato — Cadastro | Aprovado | [Vídeo (Jam)](https://jam.dev/c/1b30c3cf-8100-47c6-b4f3-a42340197fbe) | - |
| [C27-CT01](Cenarios-de-testes/CT_RF27_Tipos-de-Pagamento.md) | Tipos de Pagamento | Tipos de Pagamento — Cadastro, consulta, edição e exclusão | Aprovado | [Vídeo (Jam)](https://jam.dev/c/e3b4b3f5-be92-48a3-9270-81dd0d63c80c) | - |
| [C28-CT01](Cenarios-de-testes/CT_RF28_Bandeiras.md) | Bandeiras | Bandeiras de Cartão — Cadastro | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/e25b0150-92e4-4976-bddf-23e8dca8e6b3) | BUG-010 |
| [C28-CT02](Cenarios-de-testes/CT_RF28_Bandeiras.md) | Bandeiras | Bandeiras de Cartão — Cadastro e consulta | Reprovado | [Vídeo (Jam)](https://jam.dev/c/03c675ab-9995-473c-98d6-b443636466bf) | BUG-010 |
| [C28-CT03](Cenarios-de-testes/CT_RF28_Bandeiras.md) | Bandeiras | Cadastrar bandeira e localizá-la | Reprovado | Registro textual (respostas HTTP) | BUG-010 |
| [C29-CT01](Cenarios-de-testes/CT_RF29_Colaboradores.md) | Colaboradores | Colaboradores — Cadastro | Aprovado | [Vídeo (Jam)](https://jam.dev/c/705c5e7b-2c39-4514-94d1-237ba03da5ad) | - |
| [C29-CT02](Cenarios-de-testes/CT_RF29_Colaboradores.md) | Colaboradores | Colaboradores — Edição e exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/cfbf52d0-5468-438c-b895-0c71fadde4ad) | - |
| [C30-CT01](Cenarios-de-testes/CT_RF30_Funcoes-e-permissoes.md) | Funções e permissões | Funções — Cadastro e grupo de permissões | Aprovado | [Vídeo (Jam)](https://jam.dev/c/1c619e71-bf82-469b-8061-a45acfc99019) | - |
| [C31-CT01](Cenarios-de-testes/CT_RF31_Fornecedores.md) | Fornecedores | Fornecedores — Cadastro, edição e exclusão | Reprovado | [Vídeo (Jam)](https://jam.dev/c/f1d55cef-7804-435b-a5e0-f4b87c32bb39) | BUG-011 |
| [C32-CT01](Cenarios-de-testes/CT_RF32_Tipos-de-Documentos.md) | Tipos de Documentos | Tipos de Documentos — Cadastro e alteração | Aprovado | [Vídeo (Jam)](https://jam.dev/c/24c28488-384b-4401-8963-b81d4da1b59d) | - |
| [C32-CT02](Cenarios-de-testes/CT_RF32_Tipos-de-Documentos.md) | Tipos de Documentos | Tipos de Documentos — Exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/a92d0c75-1b14-494f-9045-176bb441a869) | - |
| [C33-CT01](Cenarios-de-testes/CT_RF33_Atividades.md) | Atividades | Atividades — Nova atividade | Aprovado | [Vídeo (Jam)](https://jam.dev/c/62ff8072-1a6c-4512-9525-4489f3f4a79b) | - |
| [C33-CT02](Cenarios-de-testes/CT_RF33_Atividades.md) | Atividades | Atividades — Exclusão de atividade | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/3ed505f2-30fb-4a63-9655-beba55acf23c) | - |
| [C33-CT03](Cenarios-de-testes/CT_RF33_Atividades.md) | Atividades | Atividades — Pesquisar atividade | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/2b06f310-4c2c-42b5-ab68-1fcf64411612) | - |
| [C33-CT04](Cenarios-de-testes/CT_RF33_Atividades.md) | Atividades | Validar nome obrigatório de atividade | Reprovado | [Captura](evidencias/imagens/EXE2-RF33-atividade-sem-nome-aceita.jpg) | BUG-017 |
| [C33-CT05](Cenarios-de-testes/CT_RF33_Atividades.md) | Atividades | Alterar atividade | Aprovado | Registro textual (respostas HTTP) | - |
| [C33-CT06](Cenarios-de-testes/CT_RF33_Atividades.md) | Atividades | Excluir atividade | Aprovado | Registro textual (respostas HTTP) | - |
| [C34-CT01](Cenarios-de-testes/CT_RF34_Pontuacao.md) | Pontuação | Financeiro — Pontuação | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/c8d0473d-4441-472b-846e-bcdc02fb6695) | - |
| [C35-CT01](Cenarios-de-testes/CT_RF35_Produtos.md) | Produtos | Produtos — Novo produto | Parcial | [Vídeo (Jam)](https://jam.dev/c/1a2f5a18-65fa-4145-9072-d1cb973fdce1) | - |
| [C35-CT02](Cenarios-de-testes/CT_RF35_Produtos.md) | Produtos | Produtos — Inativação e exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/34982376-5d60-40bc-b361-6d812a5d4fdc) | - |
| [C36-CT01](Cenarios-de-testes/CT_RF36_Enquetes.md) | Enquetes | Enquetes — Cadastro | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/5d07fa69-a8d7-47fa-9814-6299d08ecbb4) | - |
| [C36-CT02](Cenarios-de-testes/CT_RF36_Enquetes.md) | Enquetes | Enquetes — Inativação e exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/24e0135a-e211-4f0a-b46f-79f3beaf3be9) | - |
| [C37-CT01](Cenarios-de-testes/CT_RF37_Fichas-de-Anamnese.md) | Fichas de Anamnese | Fichas de Análise — Cadastro | Aprovado | [Vídeo (Jam)](https://jam.dev/c/6ecb6761-b8df-4203-becc-7bbc1417f032) | - |
| [C38-CT01](Cenarios-de-testes/CT_RF38_Modelos-de-Anamnese.md) | Modelos de Anamnese | Modelos de Análise — Cadastro | Aprovado | [Vídeo (Jam)](https://jam.dev/c/fe27eb69-fbd3-487d-80fd-e6f06253f99d) | - |
| [C38-CT02](Cenarios-de-testes/CT_RF38_Modelos-de-Anamnese.md) | Modelos de Anamnese | Modelos de Análise — Exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/468320db-cac1-4df6-89c1-eeffb6bd47e4) | - |
| [C38-CT03](Cenarios-de-testes/CT_RF38_Modelos-de-Anamnese.md) | Modelos de Anamnese | Modelos de Análise — Inativação | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/e67ff75f-af66-4169-8b4d-6b20f41e5576) | - |
| [C38-CT04](Cenarios-de-testes/CT_RF38_Modelos-de-Anamnese.md) | Modelos de Anamnese | Modelos de Análise — Consulta | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/421d76e9-1c7e-4d98-a39f-77db30f8e417) | - |
| [C39-CT01](Cenarios-de-testes/CT_RF39_Categorias-de-Anamnese.md) | Categorias de Anamnese | Categorias — Nova categoria | Aprovado | [Vídeo (Jam)](https://jam.dev/c/fa77ae9d-c3cf-4924-a01d-f924803708c5) | - |
| [C39-CT02](Cenarios-de-testes/CT_RF39_Categorias-de-Anamnese.md) | Categorias de Anamnese | Categorias — Exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8fc13646-0334-4b05-9499-3fff4e0c539a) | - |
| [C39-CT03](Cenarios-de-testes/CT_RF39_Categorias-de-Anamnese.md) | Categorias de Anamnese | Categorias — Consulta e edição | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/6f4b42ba-8895-4375-af7e-fe3b1ce8a0cf) | - |
| [C40-CT01](Cenarios-de-testes/CT_RF40_Perguntas-de-Anamnese.md) | Perguntas de Anamnese | Perguntas — Nova pergunta | Parcial | [Vídeo (Jam)](https://jam.dev/c/902e3330-f85e-43b4-83c7-5d7283a39882) | BUG-009 |
| [C40-CT02](Cenarios-de-testes/CT_RF40_Perguntas-de-Anamnese.md) | Perguntas de Anamnese | Perguntas — Exclusão | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/8e5dbe98-c990-4219-b190-daf4249875c5) | - |
| [C40-CT03](Cenarios-de-testes/CT_RF40_Perguntas-de-Anamnese.md) | Perguntas de Anamnese | Perguntas — Consulta e edição | Reprovado | [Vídeo (Jam)](https://jam.dev/c/d53c5739-725c-4eae-8b83-f6b6b072bd51) | BUG-009 |
| [C41-CT01](Cenarios-de-testes/CT_RF41_Inteligencia-e-Automacao.md) | Inteligência e Automação | Inteligência e Automação — Integração e Automatização | Aprovado | [Vídeo (Jam)](https://jam.dev/c/e91d5a54-306f-4853-8c6d-6a9c7d506088) | - |
| [C41-CT02](Cenarios-de-testes/CT_RF41_Inteligencia-e-Automacao.md) | Inteligência e Automação | Inteligência e Automação — Relatório de Risco de Evasão | Aprovado | [Vídeo (Jam)](https://jam.dev/c/4f6d9b31-d3aa-4085-8151-694a60234e0b) | - |
| [C41-CT03](Cenarios-de-testes/CT_RF41_Inteligencia-e-Automacao.md) | Inteligência e Automação | Inteligência e Automação — Automações - Configuração | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/7b66dbf7-705c-4e42-a6ba-4fdffa29745d) | - |
| [C42-CT01](Cenarios-de-testes/CT_RF42_Resultados-IA.md) | Resultados IA | Inteligência e Automação — Resultados da Inteligência | Aprovado | [Vídeo (Jam)](https://jam.dev/c/5ed5598f-64f3-49af-b0d6-84cd94ff2ec6) | - |
| [C43-CT01](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Navegar pelas sete abas sem salvar | Aprovado | Registro textual | - |
| [C43-CT02](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Configurações — Home | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/2bea0a38-f30b-447a-9f86-4da71aa7b8c1) | - |
| [C43-CT03](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Configurações — Biometria | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/5d844b20-b8a7-4968-b8d5-7ad405d0a6d9) | - |
| [C43-CT04](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Configurações — Avaliação | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/70f6b2f5-fd50-4128-8514-3ae81f851599) | - |
| [C43-CT05](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Configurações — Aniversário | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/a1c2c902-4443-4d48-b530-445a63aaeccb) | - |
| [C43-CT06](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Configurações — Pagamento | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/7db68275-cd1a-4ce5-8d34-86b401ab1b2c) | - |
| [C43-CT07](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Configurações — Integrações | Inconclusivo | [Vídeo (Jam)](https://jam.dev/c/99ecc77c-0ae0-4031-aaca-e26881937139) | - |
| [C43-CT08](Cenarios-de-testes/CT_RF43_Configuracoes.md) | Configurações | Configurações — Design | Reprovado | [Vídeo (Jam)](https://jam.dev/c/11c2253a-aa5b-40a9-8b33-717e5d13ef1c) | BUG-008 |
| [C44-CT01](Cenarios-de-testes/CT_RF44_Modelos-de-Ficha.md) | Modelos de Ficha | Treinos — Cadastro de Modelo de Ficha (Novo Modelo de Ficha > Criar Modelo) | Reprovado | [Vídeo (Jam)](https://jam.dev/c/645a3706-aa9e-4724-b4bb-6b7badb33e92) | BUG-007 |
| [C45-CT01](Cenarios-de-testes/CT_RF45_Aplicativo.md) | Aplicativo | Aplicativo — Notificações | Aprovado | [Vídeo (Jam)](https://jam.dev/c/f0dcb321-e13b-492c-9cc1-386a56f2db35) | - |
| [C45-CT02](Cenarios-de-testes/CT_RF45_Aplicativo.md) | Aplicativo | Aplicativo — Exclusão de notificação | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/47886dbd-22c5-4699-ae62-71be6cc8fd32) | - |
| [C46-CT01](Cenarios-de-testes/CT_RF46_Meu-perfil-e-controles-globais.md) | Meu perfil e controles globais | Exibir perfil coerente com a conta | Reprovado | [Captura](evidencias/imagens/BUG-005-perfil-template.png) | BUG-005 |
| [C46-CT02](Cenarios-de-testes/CT_RF46_Meu-perfil-e-controles-globais.md) | Meu perfil e controles globais | Notificações — Marcar mensagens como lidas | Aprovado com ressalva | [Vídeo (Jam)](https://jam.dev/c/d9fd0191-a91f-47a4-8edf-5c9ace910b25) | - |

---

## 🗄️ **Ambientes e banco de dados**

| Ambiente | API | Banco | Casos |
| --- | --- | --- | --- |
| `sifit.centrion.com.br` | `backendsifit.centrion.com.br` | `u339572246_sifit_alfa` | Exploração local, execução complementar e 4 vídeos de login/painel |
| `sifitalfa.centrion.com.br` | `backsifitalfa.centrion.com.br` | Não identificado | 69 vídeos da equipe |

O banco `u339572246_sifit_alfa` foi confirmado como banco do `sifit` por um registro de teste criado pela interface e localizado por SELECT. Os registros dos vídeos do `sifitalfa` não foram encontrados nesse banco; por isso, a persistência desses casos não foi comprovada por consulta. Na execução complementar, a persistência foi conferida no banco para cinco operações: grupo, cadastro e alteração de cliente, matrícula com desconto e bandeira. Detalhes em [conferência do banco](anexos/conferencia-do-banco.md).

**Registros de teste remanescentes no `sifit`:** grupo #12 (SONDA-QA-1118), cliente #440 com matrícula #246 cancelada e conta #1625 pendente, e bandeira #35. As exclusões falharam por BUG-013, BUG-019 e BUG-010.

---

## 📁 **Evidências e Documentos**

* ✔️ [Análise de Requisitos](1-Analise-de-requisitos.md)
* ✔️ [Plano de Testes](2-plano-de-testes.md)
* ✔️ [Casos de Teste (Markdown)](Cenarios-de-testes/)
* 🐛 [Relatório de Bugs com Evidências](3-Relatorio-de-Bugs.md)
* 📹 Evidências em vídeo e print hospedadas no Jam.dev (links em cada caso)
* 🖼️ [Capturas da execução](evidencias/imagens/)
* 📎 Anexos: [matriz de rastreabilidade](anexos/matriz-de-rastreabilidade.md), [pendências, investigações e melhorias](anexos/pendencias-e-melhorias.md), [consolidação da equipe](anexos/consolidacao-da-equipe.md), [análise dos vídeos](anexos/analise-dos-videos.md), [conferência do banco](anexos/conferencia-do-banco.md), [correspondência de IDs](anexos/correspondencia-de-ids.md) e [inventário de telas](anexos/inventario/)

---

## ✅ **Conclusão**

A execução manual no SIFIT cobriu 45 dos 46 requisitos (RF06 bloqueado pelo módulo SifitBox desabilitado). Dos 108 casos, 71 passaram e 28 falharam total ou parcialmente. Os defeitos de maior impacto estão em **Bandeiras** (cadastros não listados), **Matrículas** (desconto não aplicado), **Avaliações** e **Fornecedores** (erro 500 ao salvar), além de **exclusões** de grupo, plano e cliente que retornam erro interno em vez de mensagens de regra.

🔍 Identificação da Causa Raiz (Root Cause Analysis)

* **Bandeiras (BUG-010):** o banco mostra status nulo em todas as bandeiras; a causa provável é a gravação sem status combinada a uma listagem filtrada por status ativo.
* **Matrículas (BUG-018):** o percentual de desconto é gravado, mas os campos calculados (valor do desconto e total com desconto) permanecem com o valor cheio; o cálculo não é executado no salvamento.
* **Exclusões com erro 500 (BUG-012, 013, 019):** o padrão indica ausência de tratamento de exceção ou de verificação de vínculos antes da exclusão; o usuário recebe erro interno em vez de uma regra explicativa.
* **Validação ausente (BUG-017, BUG-020):** campos obrigatórios não são validados no servidor, e valores vazios são exibidos como o texto “null”.
* **Envio de imagens (BUG-014):** a falha ocorre apenas com imagem anexada, o que aponta para validação de tipo/tamanho de arquivo sem mensagem ao usuário.

Essas hipóteses foram formuladas a partir da interface, das respostas HTTP e de consultas de leitura ao banco; a confirmação depende de análise do código e dos logs do servidor.
