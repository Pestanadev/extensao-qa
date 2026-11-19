# Relatório de Bugs

**Software:** SIFIT — sistema de gestão de academias

**QA responsável:** Arthur Soares Gardim (RA 14526), Felipe Pestana (RA 14530), Guilherme Ananias Calixto Ribeiro (RA 14652), Kaiki Teles de Andrade (RA 14518)

**Data:** 21/10/2026 a 18/11/2026

---

| ID | Título | Severidade | Prioridade | Status |
| ------- | ------- | ------- | ------- | ------- |
| [BUG-001](#bug-001) | Recuperação de senha não apresenta fluxo ou orientação | Média | Alta | Aberto |
| [BUG-002](#bug-002) | Dashboard exibe título Despesas Fixas | Baixa | Média | Aberto |
| [BUG-003](#bug-003) | IMC exibe unidade kg/m³ | Baixa | Média | Aberto |
| [BUG-004](#bug-004) | Perfil apresenta vencimento com ano negativo | Média | Alta | Aberto |
| [BUG-005](#bug-005) | Meu perfil apresenta conteúdo de demonstração | Média | Média | Aberto |
| [BUG-006](#bug-006) | Botão ao lado do período do painel não executa ação | Baixa | Média | Aberto |
| [BUG-007](#bug-007) | Criação de modelo de ficha retorna 400 | Média | Alta | Aberto |
| [BUG-008](#bug-008) | Salvar aba Design das configurações retorna 400 | Baixa | Média | Aberto |
| [BUG-009](#bug-009) | Edição de pergunta de anamnese retorna 500 | Média | Alta | Aberto |
| [BUG-010](#bug-010) | Bandeiras cadastradas não aparecem na listagem | Alta | Alta | Aberto |
| [BUG-011](#bug-011) | Cadastro de fornecedor retorna 500 | Alta | Alta | Aberto |
| [BUG-012](#bug-012) | Exclusão de plano retorna 500 | Média | Média | Aberto |
| [BUG-013](#bug-013) | Exclusão de grupo retorna 500 | Média | Média | Aberto |
| [BUG-014](#bug-014) | Salvar grupo muscular ou exercício com imagem retorna 400 | Média | Média | Aberto |
| [BUG-015](#bug-015) | Salvar avaliação física retorna 500 | Alta | Alta | Aberto |
| [BUG-016](#bug-016) | Cadastro de despesa fixa falha com 500 na primeira tentativa | Média | Média | Aberto |
| [BUG-017](#bug-017) | Atividade é salva com todos os campos vazios | Média | Média | Aberto |
| [BUG-018](#bug-018) | Desconto da matrícula não é aplicado ao valor | Alta | Alta | Aberto |
| [BUG-019](#bug-019) | Exclusão de cliente retorna erro interno 500 | Média | Média | Aberto |
| [BUG-020](#bug-020) | Perfil de cliente sem contato exibe “null” e objetivos fictícios | Média | Média | Aberto |
| [BUG-021](#bug-021) | Filtro “Este mês” de Presenças aplica os últimos 30 dias | Baixa | Baixa | Aberto |

> Os bugs BUG-01, BUG-02 e BUG-03 da versão anterior deste repositório correspondem a BUG-006, BUG-007 e BUG-009. A numeração foi unificada com os registros da exploração local (BUG-001 a BUG-005) e com os encontrados na revisão de 18/11/2026.

---

<a id="bug-001"></a>

### 🐞 **Bug 01: Recuperação de senha não apresenta fluxo ou orientação**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-001 | O link “Esqueci minha senha” não abre recuperação de acesso nem orientação; a tela permanece no login (/login#). |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar a página de login sem sessão ativa |
| 2. Clicar em "Esqueci minha senha" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Abrir a recuperação de acesso ou informar um procedimento de suporte. | A tela permanece no login, sem formulário ou mensagem. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows. |
| Navegador integrado (exploração de 21/10/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Login | [C01-CT04](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md): Abrir recuperação de senha<br>[C01-CT08](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md): Login — Botão "Esqueci minha senha" |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/BUG-001-recuperacao-senha.png)<br>[Print FP-CT-02 (Jam)](https://jam.dev/c/e4dded02-6f23-43cc-832a-fedf751e0c06) |

---

<a id="bug-002"></a>

### 🐞 **Bug 02: Dashboard exibe título Despesas Fixas**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-002 | Ao abrir o item Dashboard (/dash), o cabeçalho mostra “Despesas Fixas”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Fazer login |
| 2. Abrir o item Dashboard no menu |
| 3. Conferir o título da página |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Título compatível com Dashboard/painel analítico. | Cabeçalho “Despesas Fixas” com Dashboard selecionado. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows. |
| Navegador integrado (exploração de 21/10/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Dashboard analítico | [C03-CT01](Cenarios-de-testes/CT_RF03_Dashboard-analitico.md): Identificar corretamente o Dashboard |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/BUG-002-dashboard-titulo.png) |

---

<a id="bug-003"></a>

### 🐞 **Bug 03: IMC exibe unidade kg/m³**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-003 | Na avaliação física, o rótulo do IMC usa kg/m³ e o valor é exibido com muitas casas decimais. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Abrir Avaliações e iniciar uma avaliação de teste |
| 2. Selecionar IMC |
| 3. Informar altura 1,75 e peso 70 sem salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Unidade kg/m² e valor arredondado. | Rótulo “IMC kg/m³” e valor 22.857142857142858. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows. |
| Navegador integrado (exploração de 21/10/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Avaliações físicas | [C09-CT02](Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md): Exibir unidade correta do IMC |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/BUG-003-imc-unidade.png) |

---

<a id="bug-004"></a>

### 🐞 **Bug 04: Perfil apresenta vencimento com ano negativo**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-004 | A situação financeira do perfil de um cliente de teste exibiu vencimento 30/11/-0001. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Abrir o perfil do cliente de teste com conta de data inválida |
| 2. Aguardar a situação financeira |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Data válida ou tratamento explícito de data ausente/inválida. | Vencimento e próximo vencimento 30/11/-0001. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows. |
| Navegador integrado (exploração de 21/10/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Clientes | [C07-CT01](Cenarios-de-testes/CT_RF07_Clientes.md): Tratar vencimento inválido no perfil |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/BUG-004-cliente-data.png) |

---

<a id="bug-005"></a>

### 🐞 **Bug 05: Meu perfil apresenta conteúdo de demonstração**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-005 | A página Meu perfil exibe conteúdo de modelo (“Hello Jesse”, “Jessica Jones”) em inglês. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Fazer login |
| 2. Abrir o menu da conta |
| 3. Clicar em "Meu perfil" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Perfil coerente com a conta ou estado vazio apropriado. | Conteúdo demonstrativo de outro usuário. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows. |
| Navegador integrado (exploração de 21/10/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Meu perfil | [C46-CT01](Cenarios-de-testes/CT_RF46_Meu-perfil-e-controles-globais.md): Exibir perfil coerente com a conta |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/BUG-005-perfil-template.png) |

---

<a id="bug-006"></a>

### 🐞 **Bug 06: Botão ao lado do período do painel não executa ação**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-006 | O botão de seta ao lado do intervalo de datas (“Competência”) na Página Inicial não executa nenhuma ação. Registrado originalmente como BUG-01 no repositório. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Fazer login |
| 2. Na Página Inicial, clicar no botão ao lado do campo de período |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Abrir a seleção de período ou aplicar o filtro. | Nenhuma mudança na tela e nenhuma requisição ao servidor. |

| **Ambiente** |
| ---------- |
| Ambientes de testes `sifitalfa.centrion.com.br` (vídeo) e `sifit.centrion.com.br` (reprodução em 18/11/2026). |
| Desktop com Windows 11. |
| Google Chrome 157 e navegador integrado baseado em Chromium. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Página Inicial | [C02-CT03](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md): Dashboard — Botão ao lado de "Competência" sem funcionalidade<br>[C02-CT07](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md): Acionar botão ao lado do período no painel |

| **Evidência(s)** |
| :---: |
| [Print FP-CT-04 (Jam)](https://jam.dev/c/4dfcb03a-bf1b-4d35-8874-31f846f25250) |

---

<a id="bug-007"></a>

### 🐞 **Bug 07: Criação de modelo de ficha retorna 400**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-007 | Ao criar um modelo de ficha, o servidor responde 400 e a tela exibe “Erro ao salvar modelo”. Registrado originalmente como BUG-02 no repositório. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Configurações > Modelo Ficha |
| 2. Clicar em "Novo Modelo de Ficha" |
| 3. Preencher os dados e clicar em "Criar Modelo" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Modelo salvo e listado, ou mensagem indicando o campo inválido. | Resposta 400 e “Erro ao salvar modelo”. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Modelos de Ficha | [C44-CT01](Cenarios-de-testes/CT_RF44_Modelos-de-Ficha.md): Treinos — Cadastro de Modelo de Ficha (Novo Modelo de Ficha > Criar Modelo) |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-12 (Jam)](https://jam.dev/c/645a3706-aa9e-4724-b4bb-6b7badb33e92) |

---

<a id="bug-008"></a>

### 🐞 **Bug 08: Salvar aba Design das configurações retorna 400**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-008 | Ao salvar a aba Design, o servidor responde 400 e a tela exibe “Erro ao salvar configurações”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Configurações |
| 2. Abrir a aba Design |
| 3. Clicar em salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Configurações salvas. | Resposta 400 e “Erro ao salvar configurações”. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Configurações | [C43-CT08](Cenarios-de-testes/CT_RF43_Configuracoes.md): Configurações — Design |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-19 (Jam)](https://jam.dev/c/11c2253a-aa5b-40a9-8b33-717e5d13ef1c) |

---

<a id="bug-009"></a>

### 🐞 **Bug 09: Edição de pergunta de anamnese retorna 500**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-009 | Ao editar uma pergunta de anamnese existente, o servidor responde 500 e a tela exibe “Erro ao salvar pergunta”. O cadastro de nova pergunta funciona. Registrado originalmente como BUG-03 no repositório. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Saúde > Perguntas |
| 2. Abrir uma pergunta existente |
| 3. Alterar o enunciado e salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Alteração salva. | Resposta 500 e “Erro ao salvar pergunta” (FP-CT-31 a 0:32; FP-CT-33 a 0:09). |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Perguntas de Anamnese | [C40-CT01](Cenarios-de-testes/CT_RF40_Perguntas-de-Anamnese.md): Perguntas — Nova pergunta<br>[C40-CT03](Cenarios-de-testes/CT_RF40_Perguntas-de-Anamnese.md): Perguntas — Consulta e edição |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-31 (Jam)](https://jam.dev/c/902e3330-f85e-43b4-83c7-5d7283a39882)<br>[Vídeo FP-CT-33 (Jam)](https://jam.dev/c/d53c5739-725c-4eae-8b83-f6b6b072bd51) |

---

<a id="bug-010"></a>

### 🐞 **Bug 10: Bandeiras cadastradas não aparecem na listagem**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-010 | O cadastro de bandeira é aceito (201), mas a listagem continua vazia. No banco, todas as bandeiras têm status nulo, o que indica gravação sem status e listagem filtrada por status. O horário de criação foi gravado em formato de 12 horas. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Comercial > Bandeiras |
| 2. Clicar em "Nova Bandeira" |
| 3. Informar o nome "QA Bandeira 1118" e salvar |
| 4. Conferir a listagem |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Bandeira listada após salvar. | Resposta 201, mas “Nenhuma bandeira encontrada. 0 registro(s)”. No vídeo FP-CT-53 houve também 500 com “Salvando...” travado. |

| **Ambiente** |
| ---------- |
| Ambientes de testes `sifitalfa.centrion.com.br` (vídeo) e `sifit.centrion.com.br` (reprodução em 18/11/2026). |
| Desktop com Windows 11. |
| Google Chrome 157 e navegador integrado baseado em Chromium. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Bandeiras | [C28-CT02](Cenarios-de-testes/CT_RF28_Bandeiras.md): Bandeiras de Cartão — Cadastro e consulta<br>[C28-CT01](Cenarios-de-testes/CT_RF28_Bandeiras.md): Bandeiras de Cartão — Cadastro<br>[C28-CT03](Cenarios-de-testes/CT_RF28_Bandeiras.md): Cadastrar bandeira e localizá-la |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-53 (Jam)](https://jam.dev/c/03c675ab-9995-473c-98d6-b443636466bf)<br>[Vídeo FP-CT-30 (Jam)](https://jam.dev/c/e25b0150-92e4-4976-bddf-23e8dca8e6b3) |

---

<a id="bug-011"></a>

### 🐞 **Bug 11: Cadastro de fornecedor retorna 500**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-011 | O salvamento de fornecedor falha repetidamente com 500; a lista permanece com os mesmos registros. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Gestão > Fornecedores |
| 2. Clicar em "Novo Fornecedor" |
| 3. Preencher os dados e salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Fornecedor salvo e listado. | Respostas 500 repetidas; formulário travado em “Salvar” (0:47); lista com 8 registros ao final. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Fornecedores | [C31-CT01](Cenarios-de-testes/CT_RF31_Fornecedores.md): Fornecedores — Cadastro, edição e exclusão |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-47 (Jam)](https://jam.dev/c/f1d55cef-7804-435b-a5e0-f4b87c32bb39) |

---

<a id="bug-012"></a>

### 🐞 **Bug 12: Exclusão de plano retorna 500**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-012 | Após confirmar a exclusão de um plano, o servidor responde 500 e a tela exibe “Erro ao deletar Plano”. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Comercial > Planos |
| 2. Clicar em excluir em um plano de teste |
| 3. Confirmar a exclusão |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Plano excluído, ou mensagem explicando o vínculo que impede a exclusão. | Resposta 500 e “Erro ao deletar Plano” (0:57). |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Planos | [C25-CT01](Cenarios-de-testes/CT_RF25_Planos.md): Planos — Cadastro, inativação, alteração e exclusão |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-56 (Jam)](https://jam.dev/c/6ec365fc-5fee-4ebf-a9c4-cc8c42243f41) |

---

<a id="bug-013"></a>

### 🐞 **Bug 13: Exclusão de grupo retorna 500**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-013 | A exclusão de grupo falha com 500 mesmo para um grupo recém-criado e sem vínculos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Treinamento > Grupos |
| 2. Cadastrar o grupo "SONDA-QA-1118" |
| 3. Clicar na lixeira do grupo e confirmar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Grupo excluído. | Resposta 500 e “Erro ao deletar Grupo”; o grupo permanece. |

| **Ambiente** |
| ---------- |
| Ambientes de testes `sifitalfa.centrion.com.br` (vídeo) e `sifit.centrion.com.br` (reprodução em 18/11/2026). |
| Desktop com Windows 11. |
| Google Chrome 157 e navegador integrado baseado em Chromium. |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Grupos | [C16-CT01](Cenarios-de-testes/CT_RF16_Grupos.md): Grupos — Cadastro, consulta, inativação e exclusão<br>[C16-CT03](Cenarios-de-testes/CT_RF16_Grupos.md): Excluir grupo sem vínculos |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-57 (Jam)](https://jam.dev/c/484df916-a8fd-4159-9528-4334f8919d80)<br>[Captura (18/11)](evidencias/imagens/SONDA-03-erro-ao-deletar-grupo.jpg) |

---

<a id="bug-014"></a>

### 🐞 **Bug 14: Salvar grupo muscular ou exercício com imagem retorna 400**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-014 | Ao salvar grupo muscular ou exercício com imagem anexada, o servidor responde 400; cadastros sem a mesma condição são aceitos. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Grupos Musculares ou Exercícios |
| 2. Editar um registro e anexar uma imagem |
| 3. Salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Registro salvo com a imagem, ou mensagem sobre o formato/tamanho aceito. | Resposta 400 e “Erro ao salvar grupo” / “Erro ao salvar exercício”. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Grupos Musculares e Exercícios | [C14-CT01](Cenarios-de-testes/CT_RF14_Grupos-Musculares.md): Grupos Musculares — Cadastro, consulta e edição<br>[C13-CT01](Cenarios-de-testes/CT_RF13_Exercicios.md): Biblioteca de Exercícios — Cadastro, consulta e edição |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-62 (Jam)](https://jam.dev/c/6aee3782-c54d-4a79-8a42-55bd50d0c8df)<br>[Vídeo FP-CT-64 (Jam)](https://jam.dev/c/d5d88e50-ae2a-4cae-8c14-719d9b9300be) |

---

<a id="bug-015"></a>

### 🐞 **Bug 15: Salvar avaliação física retorna 500**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-015 | O salvamento da avaliação física fica em “Salvando...” e o servidor responde 500. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Avaliações |
| 2. Abrir uma avaliação de teste |
| 3. Preencher as medidas e salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Avaliação salva. | “Salvando...” (0:45) e resposta 500. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Avaliações físicas | [C09-CT03](Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md): Avaliações — Cadastro, consulta, edição e exclusão |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-71 (Jam)](https://jam.dev/c/364850dc-8240-4fee-9169-465b5a9ef048) |

---

<a id="bug-016"></a>

### 🐞 **Bug 16: Cadastro de despesa fixa falha com 500 na primeira tentativa**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-016 | O primeiro salvamento de uma nova despesa fixa trava em “Salvando...” com 500; a tentativa seguinte é aceita. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Financeiro > Despesas Fixas |
| 2. Clicar em "Nova Despesa" |
| 3. Preencher e salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Despesa salva na primeira tentativa. | 500 com “Salvando...” travado; sucesso (201) apenas ao repetir. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifitalfa.centrion.com.br`. |
| Desktop com Windows 11. |
| Google Chrome 157 (gravação Jam). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Despesas Fixas | [C22-CT01](Cenarios-de-testes/CT_RF22_Despesas-Fixas.md): Despesas Fixas — Cadastro, edição e exclusão |

| **Evidência(s)** |
| :---: |
| [Vídeo FP-CT-72 (Jam)](https://jam.dev/c/573bcb6b-2dae-499f-9137-e9ee7a48167d) |

---

<a id="bug-017"></a>

### 🐞 **Bug 17: Atividade é salva com todos os campos vazios**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-017 | O formulário de atividade aceita salvar sem nome; há atividades sem nome no sistema. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Gestão > Atividades |
| 2. Clicar em "Nova Atividade" |
| 3. Clicar em "Salvar" sem preencher |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Validação de nome obrigatório. | Resposta 201 e atividade criada sem nome (total 8 → 9). |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows 11. |
| Navegador integrado baseado em Chromium (18/11/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Atividades | [C33-CT04](Cenarios-de-testes/CT_RF33_Atividades.md): Validar nome obrigatório de atividade |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/EXE2-RF33-atividade-sem-nome-aceita.jpg) |

---

<a id="bug-018"></a>

### 🐞 **Bug 18: Desconto da matrícula não é aplicado ao valor**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-018 | O desconto informado na matrícula é gravado, mas não altera o valor total, a parcela nem a conta a receber. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Alta | Alta | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Operação > Matrículas > Cadastrar Matrícula |
| 2. Selecionar o cliente de teste e o plano Treino Livre (R$ 52,00) |
| 3. Informar Desconto 10 e salvar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Valor total e parcela com o desconto aplicado. | Valor total 52,00, parcela 52,00 e conta a receber de 52,00; no banco, percentual_desconto = 10 e valor_total_com_desconto = 52,00. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows 11. |
| Navegador integrado baseado em Chromium (18/11/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Matrículas | [C08-CT04](Cenarios-de-testes/CT_RF08_Matriculas.md): Aplicar desconto na matrícula |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/EXE2-RF08-matricula-ativa-cliente-440.jpg) |

---

<a id="bug-019"></a>

### 🐞 **Bug 19: Exclusão de cliente retorna erro interno 500**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-019 | A exclusão de um cliente com matrícula cancelada retorna erro interno, sem mensagem de regra. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Operação > Clientes |
| 2. Clicar em excluir no cliente de teste (com matrícula cancelada) |
| 3. Confirmar |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Cliente excluído ou mensagem explicando o impedimento. | Resposta 500 e “Erro no servidor — Erro interno inesperado”. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows 11. |
| Navegador integrado baseado em Chromium (18/11/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Clientes | [C07-CT07](Cenarios-de-testes/CT_RF07_Clientes.md): Excluir cliente com matrícula cancelada |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/EXE2-RF07-erro-500-excluir-cliente.jpg) |

---

<a id="bug-020"></a>

### 🐞 **Bug 20: Perfil de cliente sem contato exibe “null” e objetivos fictícios**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-020 | Cliente cadastrado só com os campos obrigatórios exibe “null” no contato e no tipo sanguíneo, e o bloco Objetivos mostra dados de demonstração. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Média | Média | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Cadastrar cliente apenas com Nome, Status, Sexo e Data de Nascimento |
| 2. Abrir o perfil do cliente |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Campos vazios exibidos como não informados; sem dados fictícios. | “null” no telefone e no tipo sanguíneo; “Perda de peso e ganho de resistência”, “Progresso geral 60%” e “Evolução positiva”. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows 11. |
| Navegador integrado baseado em Chromium (18/11/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Clientes | [C07-CT05](Cenarios-de-testes/CT_RF07_Clientes.md): Exibir perfil de cliente novo |

| **Evidência(s)** |
| :---: |
| [Captura](evidencias/imagens/EXE2-RF07-cliente-null-contato.jpg) |

---

<a id="bug-021"></a>

### 🐞 **Bug 21: Filtro “Este mês” de Presenças aplica os últimos 30 dias**

| **ID** | **Descrição** |
| ---------- | ---------- |
| BUG-021 | O atalho “Este mês” preenche os últimos 30 dias em vez do mês corrente. |

| **Severidade do Bug** | **Prioridade de Correção** | **Status** |
| :---: | :---: | :---: |
| Baixa | Baixa | Aberto |

| **Passo a passo para simular o bug** |
| ---------- |
| 1. Acessar Principal > Presenças |
| 2. Clicar em "Este mês" |

| **Comportamento Esperado** | **Comportamento Obtido** |
| :---: | :---: |
| Período de 01/11/2026 a 18/11/2026. | Período de 20/10/2026 a 18/11/2026. |

| **Ambiente** |
| ---------- |
| Ambiente de testes `sifit.centrion.com.br`. |
| Desktop com Windows 11. |
| Navegador integrado baseado em Chromium (18/11/2026). |

| **Funcionalidade Afetada** | **Caso de Teste Relacionado** |
| :---: | :---: |
| Presenças | [C05-CT02](Cenarios-de-testes/CT_RF05_Presencas.md): Aplicar filtro “Este mês” |

| **Evidência(s)** |
| :---: |
| Registro textual (passos e resposta do servidor) |

---
