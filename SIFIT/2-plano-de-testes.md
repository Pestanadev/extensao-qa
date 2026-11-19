## 🧪 **Plano de Testes - SIFIT**

### 📌 1. **Identificação**

* **Nome do Projeto**: SIFIT - Sistema de Gestão de Academias
* **Versão Avaliada**: versão web disponível nos ambientes da disciplina (número de versão não informado)
* **Ambiente de Testes**: [https://sifit.centrion.com.br](https://sifit.centrion.com.br) e [https://sifitalfa.centrion.com.br](https://sifitalfa.centrion.com.br)
* **Tipo de Teste**: Teste Funcional Manual
* **Data do Documento**: 18/11/2026
* **Responsável**: Arthur Soares Gardim (RA 14526), Felipe Pestana (RA 14530), Guilherme Ananias Calixto Ribeiro (RA 14652), Kaiki Teles de Andrade (RA 14518)

---

### 🎯 2. **Objetivo**

Verificar manualmente as funcionalidades do SIFIT, com foco nos fluxos de cadastro, consulta, alteração, inativação e exclusão, nas mensagens de erro e na integridade dos dados gravados, registrando evidências em vídeo e captura de tela.

---

### 🧩 3. **Escopo**

**Incluído:**

* RF01 - Autenticação e sessão
* RF02 - Página Inicial
* RF03 - Dashboard analítico
* RF04 - Check-in
* RF05 - Presenças
* RF06 - SifitBox — aulas
* RF07 - Clientes
* RF08 - Matrículas
* RF09 - Avaliações físicas
* RF10 - Contas a Receber
* RF11 - Contas a Pagar
* RF12 - Fichas de Treino
* RF13 - Exercícios
* RF14 - Grupos Musculares
* RF15 - Objetivos Treino
* RF16 - Grupos
* RF17 - Turmas
* RF18 - Categorias Crossfit
* RF19 - SifitBox — turmas e modalidades
* RF20 - Caixas
* RF21 - Pagar.me
* RF22 - Despesas Fixas
* RF23 - Relatórios
* RF24 - Prospecção
* RF25 - Planos
* RF26 - Modelos de Contrato
* RF27 - Tipos de Pagamento
* RF28 - Bandeiras
* RF29 - Colaboradores
* RF30 - Funções e permissões
* RF31 - Fornecedores
* RF32 - Tipos de Documentos
* RF33 - Atividades
* RF34 - Pontuação
* RF35 - Produtos
* RF36 - Enquetes
* RF37 - Fichas de Anamnese
* RF38 - Modelos de Anamnese
* RF39 - Categorias de Anamnese
* RF40 - Perguntas de Anamnese
* RF41 - Inteligência e Automação
* RF42 - Resultados IA
* RF43 - Configurações
* RF44 - Modelos de Ficha
* RF45 - Aplicativo
* RF46 - Meu perfil e controles globais

**Excluído:**

* Testes de carga, desempenho e segurança
* Aplicativo móvel do aluno
* Envio real de mensagens (WhatsApp, SMS, e-mail) e cobranças reais no gateway Pagar.me
* Dispositivos físicos (biometria e catraca)

---

### 🔧 4. **Ferramentas Utilizadas**

* Navegador Google Chrome e navegador integrado baseado em Chromium
* Jam (extensão do Chrome) para gravação de vídeos e prints
* Ferramentas de inspeção do navegador (DevTools) para respostas HTTP
* MySQL Workbench para consultas de leitura ao banco
* Markdown e GitHub para documentação
* Assistente de IA (Claude) como apoio na análise das evidências e na redação da documentação

---

### 🧪 5. **Técnicas de Teste**

* Particionamento de equivalência
* Análise de valor limite
* Caminho feliz (Happy Path)
* Testes negativos (campos vazios e dados inválidos)
* Testes exploratórios
* Verificação de persistência por consulta ao banco (quando disponível)

---

### 📄 6. **Critérios de Aceitação**

* O caso passa quando o sistema responde conforme o resultado esperado e os critérios de aceitação do cenário.
* Operações de cadastro, alteração e exclusão devem refletir na listagem e, quando possível, no banco.
* Mensagens de erro e validações devem ser claras e consistentes.

| Resultado | Definição |
| --- | --- |
| Aprovado | Resultado esperado atendido |
| Aprovado com ressalva | Sem erro, mas com efeito não totalmente visível ou não conferido no banco |
| Parcial | Ao menos uma operação do caso falhou |
| Reprovado | Resultado diferente do esperado |
| Inconclusivo | Evidência ou pré-condição insuficiente |
| Bloqueado | Funcionalidade indisponível no ambiente |

---

### 🚦 7. **Critérios de Saída (Exit Criteria)**

* Todos os requisitos do escopo com ao menos um caso executado ou bloqueio justificado.
* Falhas registradas no relatório de bugs com passos, evidência e caso relacionado.
* Relatório final com resultado por caso e por módulo.

---

### ⏱️ 8. **Cronograma**

| Atividade | Data Início | Data Fim |
| --- | --- | --- |
| Levantamento da interface e requisitos | 21/10/2026 | 21/10/2026 |
| Gravação dos testes (Jam) | 01/10/2026 | 17/11/2026 |
| Revisão das evidências e execução complementar | 18/11/2026 | 18/11/2026 |
| Registro de bugs e relatório final | 18/11/2026 | 18/11/2026 |

---

### 📋 9. **Módulos a Serem Testados**

| Código RF | Módulo | Prioridade |
| --------- | ------ | ---------- |
| RF01 | Autenticação e sessão | Alta |
| RF02 | Página Inicial | Média |
| RF03 | Dashboard analítico | Média |
| RF04 | Check-in | Média |
| RF05 | Presenças | Média |
| RF06 | SifitBox — aulas | Média |
| RF07 | Clientes | Alta |
| RF08 | Matrículas | Alta |
| RF09 | Avaliações físicas | Alta |
| RF10 | Contas a Receber | Alta |
| RF11 | Contas a Pagar | Alta |
| RF12 | Fichas de Treino | Média |
| RF13 | Exercícios | Média |
| RF14 | Grupos Musculares | Média |
| RF15 | Objetivos Treino | Média |
| RF16 | Grupos | Média |
| RF17 | Turmas | Média |
| RF18 | Categorias Crossfit | Baixa |
| RF19 | SifitBox — turmas e modalidades | Baixa |
| RF20 | Caixas | Alta |
| RF21 | Pagar.me | Média |
| RF22 | Despesas Fixas | Alta |
| RF23 | Relatórios | Média |
| RF24 | Prospecção | Média |
| RF25 | Planos | Alta |
| RF26 | Modelos de Contrato | Média |
| RF27 | Tipos de Pagamento | Média |
| RF28 | Bandeiras | Média |
| RF29 | Colaboradores | Média |
| RF30 | Funções e permissões | Média |
| RF31 | Fornecedores | Média |
| RF32 | Tipos de Documentos | Média |
| RF33 | Atividades | Média |
| RF34 | Pontuação | Média |
| RF35 | Produtos | Média |
| RF36 | Enquetes | Baixa |
| RF37 | Fichas de Anamnese | Média |
| RF38 | Modelos de Anamnese | Média |
| RF39 | Categorias de Anamnese | Média |
| RF40 | Perguntas de Anamnese | Média |
| RF41 | Inteligência e Automação | Média |
| RF42 | Resultados IA | Baixa |
| RF43 | Configurações | Média |
| RF44 | Modelos de Ficha | Média |
| RF45 | Aplicativo | Baixa |
| RF46 | Meu perfil e controles globais | Baixa |

---

### 🐞 10. **Gestão de Defeitos**

* Bugs documentados com:

  * Título e descrição
  * Passos para reproduzir
  * Comportamento esperado e obtido
  * Ambiente
  * Caso de teste relacionado
  * Evidência (print ou vídeo)
  * Severidade e prioridade (Alta, Média, Baixa)
* Registro em [3-Relatorio-de-Bugs.md](3-Relatorio-de-Bugs.md)

---

### 📌 11. **Riscos Identificados**

| Risco | Impacto | Mitigação |
| --- | --- | --- |
| Ambiente compartilhado com outras turmas (dados alterados por terceiros) | Médio | Usar prefixo QA nos dados de teste e registrar IDs criados |
| Dois ambientes (`sifit` e `sifitalfa`) com bancos diferentes | Alto | Registrar o ambiente de cada caso; conferir no banco apenas casos do ambiente correspondente |
| Banco do `sifitalfa` não disponibilizado | Médio | Comprovar por resposta HTTP e evidência visual; registrar a limitação |
| Integrações sem sandbox (WhatsApp, Pagar.me) | Médio | Classificar como inconclusivo e não executar envio real |
| Módulo SifitBox desabilitado | Baixo | Registrar como bloqueado |

---

### 📁 12. **Entregáveis**

* Análise de Requisitos
* Plano de Testes
* Casos de Teste (pasta `Cenarios-de-testes`)
* Evidências de Execução (vídeos Jam e capturas em `evidencias/imagens`)
* Registro de Bugs
* Registro de investigações e melhorias (anexo)
* Relatório Final de Execução
