## 📦 **Requisitos Funcionais Detalhados para Testes Manuais - SIFIT**

Levantamento das funcionalidades do SIFIT (sistema de gestão de academias) a partir da interface web. Os 44 destinos do menu correspondem a RF02–RF45; autenticação (RF01) e perfil/controles globais (RF46) completam o levantamento. O detalhamento de campos e ações de cada tela está no [inventário de telas](anexos/inventario/).

<a id="rf01"></a>

### 🔐 **RF01 - Autenticação e sessão**

**Descrição**: tela `/login` da área Acesso. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Entrar.
  * Esqueci minha senha.
  * Sair do sistema no menu da conta.

* **Pontos de atenção para teste**: Persistência de Manter conectado após fechar e reabrir o navegador; expiração de sessão; diferentes perfis; recuperação de senha após correção.

* **Cenários**: [CT_RF01](Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md)

---

<a id="rf02"></a>

### 🏠 **RF02 - Página Inicial**

**Descrição**: tela `/dashboard` da área Principal. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Ver detalhes.
  * Cartões de ausentes, sem matrícula, personais, matrículas e desistências.
  * Ver análise completa.
  * Cobrar agora.
  * Enviar mensagem.
  * Ver avaliações.
  * Ver todas as mensalidades.
  * Cobrar todos no WhatsApp.
  * Ver agenda.
  * Ver todos nas entradas e aniversários.

* **Pontos de atenção para teste**: Conciliar indicadores com o banco e regras de período. Cartão Sem Matrículas mostrou 6 e modal inicialmente mostrou 0, mas na revisão exibiu 6 registros e total 6; a divergência inicial não se repetiu; desistências mostrou total 2 e lista vazia. Confirmar critérios antes de classificar causa. Atalhos de mensagem, exportação e registro financeiro não foram concluídos.

* **Cenários**: [CT_RF02](Cenarios-de-testes/CT_RF02_Pagina-Inicial.md)

---

<a id="rf03"></a>

### 🏠 **RF03 - Dashboard analítico**

**Descrição**: tela `/dash` da área Principal. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Ver Inteligência.
  * Navegação global.

* **Pontos de atenção para teste**: Validar origem, período, séries e agregações dos gráficos com o banco. Título registrado em BUG-002.

* **Cenários**: [CT_RF03](Cenarios-de-testes/CT_RF03_Dashboard-analitico.md)

---

<a id="rf04"></a>

### 🏠 **RF04 - Check-in**

**Descrição**: tela `/checkin` da área Principal. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Check-in manual.
  * Escanear QR Code.
  * Realizar check-in.
  * Registrar entrada na linha.
  * Ver todos nos presentes.
  * Notificações.

* **Pontos de atenção para teste**: Executar entrada e saída em cliente de teste, duplicidade, matrícula inativa, unidade, visitante, QR e biometria. Comportamento de Filtros pendente de reprodução. Não foram registrados check-ins por esta exploração.

* **Cenários**: [CT_RF04](Cenarios-de-testes/CT_RF04_Check-in.md)

---

<a id="rf05"></a>

### 🏠 **RF05 - Presenças**

**Descrição**: tela `/presencas` da área Principal. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Consultar e alternar períodos.

* **Pontos de atenção para teste**: Usar intervalo com registros e comparar contagens, unidades, horários e fronteiras de datas com o banco.

* **Cenários**: [CT_RF05](Cenarios-de-testes/CT_RF05_Presencas.md)

---

<a id="rf06"></a>

### 🏠 **RF06 - SifitBox — aulas**

**Descrição**: tela `/sifitbox/aulas` da área Principal. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Gerar aulas.

* **Pontos de atenção para teste**: Geração baseada em turmas recorrentes, repetição sem duplicidade, vagas, reservas e ações de aula que só aparecem com dados.

* **Cenários**: [CT_RF06](Cenarios-de-testes/CT_RF06_SifitBox-aulas.md)

---

<a id="rf07"></a>

### 👥 **RF07 - Clientes**

**Descrição**: tela `/clientes` da área Operação. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Cliente.
  * Visualizar.
  * Deletar.
  * No formulário, Cancelar e Cadastrar Cliente. Perfil: Alterar imagem, Alterar dados, Editar objetivos, Aplicar Anamnese, Enviar mensagem, Agendar avaliação, Registrar pagamento, Ver todas as presenças e Ver histórico completo.

* **Pontos de atenção para teste**: Criar, alterar e excluir apenas massa isolada; verificar obrigatórios, documentos, foto, responsável, duplicidade e vínculos. Explicar divergências entre histórico de check-ins e presenças. Confirmar identidade da conta no banco. Não registrar senhas na documentação.

* **Cenários**: [CT_RF07](Cenarios-de-testes/CT_RF07_Clientes.md)

---

<a id="rf08"></a>

### 👥 **RF08 - Matrículas**

**Descrição**: tela `/matriculas` da área Operação. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Cadastrar Matrícula (/adicionar-matricula).
  * Visualizar.
  * Cancelar matrícula.
  * Deletar.
  * Editar dentro da visualização.
  * Salvar/Cancelar formulário.

* **Pontos de atenção para teste**: Conferir geração de contas, datas, desconto, diária variável, período fixo, recorrência, renovação, personal/dependentes e anamnese após conclusão. Cancelamento e exclusão são operações diferentes.

* **Cenários**: [CT_RF08](Cenarios-de-testes/CT_RF08_Matriculas.md)

---

<a id="rf09"></a>

### 👥 **RF09 - Avaliações físicas**

**Descrição**: tela `/avaliacoes` da área Operação. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Cadastrar Avaliação.
  * Alterar e Fazer Avaliação nas pendentes.
  * Imprimir, Relatório completo (PDF), Visualizar, Link e Comparação nas realizadas.
  * Deletar.
  * Salvar/Cancelar nos formulários.

* **Pontos de atenção para teste**: Validar agendamento, edição, realização, fórmulas aprovadas pelo responsável, unidades, arredondamento, formatos decimais, PDF, comparação e vínculos financeiros. Fórmulas corporais e interpretações clínicas não foram homologadas.

* **Cenários**: [CT_RF09](Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md)

---

<a id="rf10"></a>

### 👥 **RF10 - Contas a Receber**

**Descrição**: tela `/contas-receber` da área Operação. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Conta.
  * Visualizar.
  * Deletar.
  * Pesquisar cliente.
  * Cancelar.
  * Salvar.

* **Pontos de atenção para teste**: Confirmar estados Pendente/Recebido, resíduos, cópias, descontos/multas/juros, baixa parcial, conciliação com caixa e exclusão vinculada. Operações reais de recebimento ficam fora da execução atual.

* **Cenários**: [CT_RF10](Cenarios-de-testes/CT_RF10_Contas-a-Receber.md)

---

<a id="rf11"></a>

### 👥 **RF11 - Contas a Pagar**

**Descrição**: tela `/contas-pagar` da área Operação. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Conta.
  * Visualizar.
  * Deletar.
  * Pesquisar fornecedor.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Conferir fornecedor/colaborador, categoria, documento, baixa parcial/total, vencimento, despesas fixas e caixa. Investigar totais zerados diante de conta pendente, respeitando os filtros.

* **Cenários**: [CT_RF11](Cenarios-de-testes/CT_RF11_Contas-a-Pagar.md)

---

<a id="rf12"></a>

### 🏋️ **RF12 - Fichas de Treino**

**Descrição**: tela `/fichas-treino` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Cadastrar Ficha.
  * Pesquisar aluno.
  * Criar Nova Ficha.
  * Usar Modelo de Ficha.
  * Cancelar.

* **Pontos de atenção para teste**: Editor de exercícios, séries, repetições, impressão e ações de linha pendentes de levantamento após a criação de uma ficha de teste.

* **Cenários**: [CT_RF12](Cenarios-de-testes/CT_RF12_Fichas-de-Treino.md)

---

<a id="rf13"></a>

### 🏋️ **RF13 - Exercícios**

**Descrição**: tela `/exercicios` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Adicionar por grupo.
  * Visualizar.
  * Deletar.
  * Procurar imagem/vídeo.
  * Salvar.
  * Cancelar.
  * Fechar.

* **Pontos de atenção para teste**: Persistir mídia de teste, limites e extensões; alteração de nome/mídia; integridade com ficha e grupo; tratamento de exclusão vinculada.

* **Cenários**: [CT_RF13](Cenarios-de-testes/CT_RF13_Exercicios.md)

---

<a id="rf14"></a>

### 🏋️ **RF14 - Grupos Musculares**

**Descrição**: tela `/grupos-musculares` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Cadastrar grupo.
  * Visualizar.
  * Deletar.
  * Escolher arquivo.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Tipos permitidos, imagem, nomes repetidos e exclusão quando há exercícios vinculados.

* **Cenários**: [CT_RF14](Cenarios-de-testes/CT_RF14_Grupos-Musculares.md)

---

<a id="rf15"></a>

### 🏋️ **RF15 - Objetivos Treino**

**Descrição**: tela `/objetivos-treino` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Objetivo.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Cadastrar objetivo de teste e descobrir edição/exclusão disponíveis; vincular à ficha. Não assumir CRUD completo por analogia.

* **Cenários**: [CT_RF15](Cenarios-de-testes/CT_RF15_Objetivos-Treino.md)

---

<a id="rf16"></a>

### 🏋️ **RF16 - Grupos**

**Descrição**: tela `/grupos` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Grupo.
  * Visualizar.
  * Deletar.
  * Salvar Grupo.
  * Cancelar.
  * Fechar.

* **Pontos de atenção para teste**: Verificar impacto do grupo nos planos, home e caixa; exclusão com vínculos.

* **Cenários**: [CT_RF16](Cenarios-de-testes/CT_RF16_Grupos.md)

---

<a id="rf17"></a>

### 🏋️ **RF17 - Turmas**

**Descrição**: tela `/turmas` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Cadastrar Turma.
  * Editar.
  * Deletar.
  * Selecionar dias.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Horários iguais/invertidos, dias vazios, personal condicional, sobreposição e vínculos com plano.

* **Cenários**: [CT_RF17](Cenarios-de-testes/CT_RF17_Turmas.md)

---

<a id="rf18"></a>

### 🏋️ **RF18 - Categorias Crossfit**

**Descrição**: tela `/categorias-exercicios-crossfit` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Categoria.
  * Editar.
  * Deletar.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Atualização das datas, unicidade e exclusão com vínculos de exercícios.

* **Cenários**: [CT_RF18](Cenarios-de-testes/CT_RF18_Categorias-Crossfit.md)

---

<a id="rf19"></a>

### 🏋️ **RF19 - SifitBox — turmas e modalidades**

**Descrição**: tela `/sifitbox/turmas` da área Treinamento. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Botões + Modalidade e + Turma.
  * Ícones de editar e excluir nas duas listas.

* **Pontos de atenção para teste**: Validar significado dos botões e mensagens de obrigatoriedade com massa isolada; edição, exclusão, limite de vagas e geração de aulas. Operações de persistência não executadas.

* **Cenários**: [CT_RF19](Cenarios-de-testes/CT_RF19_SifitBox-turmas-e-modalidades.md)

---

<a id="rf20"></a>

### 💰 **RF20 - Caixas**

**Descrição**: tela `/caixas` da área Financeiro. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Abrir Caixa.
  * Visualizar.
  * Imprimir.
  * No fechamento Buscar Contas, Salvar, Cancelar e Fechar.

* **Pontos de atenção para teste**: Detalhar abertura, fechamento, reabertura, conferência e ajuste após criar ambiente financeiro de teste; conciliar contas e totais. Ações adicionais constam nas permissões, mas não foram executadas.

* **Cenários**: [CT_RF20](Cenarios-de-testes/CT_RF20_Caixas.md)

---

<a id="rf21"></a>

### 💰 **RF21 - Pagar.me**

**Descrição**: tela `/pagarme` da área Financeiro. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Solicitar saque.
  * Ver previsão.
  * Ver recebíveis.
  * Ver relatório completo.
  * Ver extrato completo.
  * Nova cobrança.
  * Configurações.
  * Ver todas as transações e demais Ver todas.

* **Pontos de atenção para teste**: Confirmar sandbox e token com responsável; testar apenas nesse ambiente. Saques, cobranças, transferência e mudanças na integração não foram acionados.

* **Cenários**: [CT_RF21](Cenarios-de-testes/CT_RF21_Pagar-me.md)

---

<a id="rf22"></a>

### 💰 **RF22 - Despesas Fixas**

**Descrição**: tela `/despesas-fixas` da área Financeiro. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Despesa.
  * Visualizar.
  * Deletar.
  * Salvar Despesa.
  * Cancelar.
  * Fechar.

* **Pontos de atenção para teste**: Geração das contas periódicas, datas, repetição sem duplicar e efeito de inativação.

* **Cenários**: [CT_RF22](Cenarios-de-testes/CT_RF22_Despesas-Fixas.md)

---

<a id="rf23"></a>

### 💰 **RF23 - Relatórios**

**Descrição**: tela `/relatorios` da área Financeiro. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Selecionar tipo por cartão ou lista.
  * Gerar Relatório (PDF).

* **Pontos de atenção para teste**: Gerar PDFs dos sete tipos com massa conhecida e comparar linhas, totais e datas com consultas ao banco.

* **Cenários**: [CT_RF23](Cenarios-de-testes/CT_RF23_Relatorios.md)

---

<a id="rf24"></a>

### 🧾 **RF24 - Prospecção**

**Descrição**: tela `/prospeccao` da área Comercial. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Adicionar Lead.
  * Visualizar.
  * Deletar.
  * Salvar Lead.
  * Cancelar.
  * Fechar.

* **Pontos de atenção para teste**: Estágios e transições permitidas, duplicidades, contato inválido, edição e exclusão.

* **Cenários**: [CT_RF24](Cenarios-de-testes/CT_RF24_Prospeccao.md)

---

<a id="rf25"></a>

### 🧾 **RF25 - Planos**

**Descrição**: tela `/planos` da área Comercial. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Plano.
  * Visualizar.
  * Deletar.
  * Adicionar benefício.
  * Salvar Plano.
  * Salvar também na Pagar.me quando disponível.
  * Cancelar.

* **Pontos de atenção para teste**: Persistência de cada tipo, datas e parcelas, benefícios, dependentes, personal e conciliação do ranking. Integração Pagar.me apenas em sandbox.

* **Cenários**: [CT_RF25](Cenarios-de-testes/CT_RF25_Planos.md)

---

<a id="rf26"></a>

### 🧾 **RF26 - Modelos de Contrato**

**Descrição**: tela `/modelos-contrato` da área Comercial. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Adicionar Modelo Contrato (/adicionar-modelo-contrato).
  * Estilos de parágrafo/cabeçalho.
  * Negrito, itálico, sublinhado, tachado, alinhamento, listas, link, desfazer/refazer.
  * Atualizar preview.
  * Inserir variável.
  * Como usar?.
  * Ver todas as variáveis.
  * Salvar modelo.
  * Cancelar.

* **Pontos de atenção para teste**: Testar editor, substituição de variáveis e contrato gerado com dados fictícios. Ações de edição/exclusão em lista vazia não foram observadas. Nenhum contrato foi assinado.

* **Cenários**: [CT_RF26](Cenarios-de-testes/CT_RF26_Modelos-de-Contrato.md)

---

<a id="rf27"></a>

### 🧾 **RF27 - Tipos de Pagamento**

**Descrição**: tela `/tipos-pagamento` da área Comercial. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo.
  * Visualizar.
  * Deletar.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Efeito de status, seleção de bandeira e gateway nos formulários financeiros; exclusão com vínculos.

* **Cenários**: [CT_RF27](Cenarios-de-testes/CT_RF27_Tipos-de-Pagamento.md)

---

<a id="rf28"></a>

### 🧾 **RF28 - Bandeiras**

**Descrição**: tela `/bandeiras` da área Comercial. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Bandeira.
  * Adicionar Parcela.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Criar bandeira de teste, mapear edição/exclusão após criação e validar taxas e parcelamento com massa conhecida.

* **Cenários**: [CT_RF28](Cenarios-de-testes/CT_RF28_Bandeiras.md)

---

<a id="rf29"></a>

### 🗂️ **RF29 - Colaboradores**

**Descrição**: tela `/colaboradores` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Colaborador (/adicionar-colaborador).
  * Funções.
  * Visualizar (/visualizar-colaborador/{id}).
  * Deletar.
  * Salvar.
  * Cancelar. Perfil do colaborador: Editar.
  * Abas Resumo, Funções, Alunos e Recebimentos.
  * Selecionar e Adicionar função.
  * Remover função.

* **Pontos de atenção para teste**: Vincular função e conferir acesso com contas de teste dedicadas; testar Sem login e restrições sem conceder acesso real. Validar persistência das associações e o preenchimento das abas com massa conhecida.

* **Cenários**: [CT_RF29](Cenarios-de-testes/CT_RF29_Colaboradores.md)

---

<a id="rf30"></a>

### 🗂️ **RF30 - Funções e permissões**

**Descrição**: tela `/funcoes` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Função.
  * Permissões.
  * Visualizar.
  * Salvar Função.
  * Salvar permissões.
  * Cancelar.

* **Pontos de atenção para teste**: Testar autorização no servidor e na interface com perfis isolados, incluindo acesso direto às rotas. Exclusão de função não foi observada.

* **Cenários**: [CT_RF30](Cenarios-de-testes/CT_RF30_Funcoes-e-permissoes.md)

---

<a id="rf31"></a>

### 🗂️ **RF31 - Fornecedores**

**Descrição**: tela `/fornecedores` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Fornecedor.
  * Visualizar.
  * Deletar.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Testar documentos por tipo de pessoa, estado/cidade, duplicidade e exclusão com contas vinculadas.

* **Cenários**: [CT_RF31](Cenarios-de-testes/CT_RF31_Fornecedores.md)

---

<a id="rf32"></a>

### 🗂️ **RF32 - Tipos de Documentos**

**Descrição**: tela `/tipos-documento` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Tipo.
  * Visualizar.
  * Deletar.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Verificar disponibilidade por aplicação nas contas e exclusão com referências.

* **Cenários**: [CT_RF32](Cenarios-de-testes/CT_RF32_Tipos-de-Documentos.md)

---

<a id="rf33"></a>

### 🗂️ **RF33 - Atividades**

**Descrição**: tela `/atividades` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Atividade.
  * Visualizar.
  * Deletar.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Validade de pontuação negativa/zero, vínculo com campanhas e efeitos de alteração/exclusão.

* **Cenários**: [CT_RF33](Cenarios-de-testes/CT_RF33_Atividades.md)

---

<a id="rf34"></a>

### 🗂️ **RF34 - Pontuação**

**Descrição**: tela `/pontuacao` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Pontuação.
  * Selecionar produto.
  * Adicionar.
  * Salvar.
  * Cancelar.
  * Ações nas linhas sem nome acessível.

* **Pontos de atenção para teste**: Campanhas, produtos de resgate, pontos necessários, datas, crédito/resgate e ações de linha devem ser verificadas com massa isolada. Auditar nomes acessíveis dos botões.

* **Cenários**: [CT_RF34](Cenarios-de-testes/CT_RF34_Pontuacao.md)

---

<a id="rf35"></a>

### 🗂️ **RF35 - Produtos**

**Descrição**: tela `/produtos` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo.
  * Salvar.
  * Cancelar.
  * Escolher imagens.
  * Ações de linha sem nome acessível.

* **Pontos de atenção para teste**: Validar persistência de produto por pontuação, edição, exclusão, mídia e vínculos com campanhas. Não inferir controle de estoque: campo de estoque não foi observado.

* **Cenários**: [CT_RF35](Cenarios-de-testes/CT_RF35_Produtos.md)

---

<a id="rf36"></a>

### 🗂️ **RF36 - Enquetes**

**Descrição**: tela `/enquetes` da área Gestão. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Enquete.
  * Visualizar.
  * Deletar.
  * Adicionar resposta.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Pergunta/respostas obrigatórias, múltiplas alternativas, votação no app, contagem e alterações após votos.

* **Cenários**: [CT_RF36](Cenarios-de-testes/CT_RF36_Enquetes.md)

---

<a id="rf37"></a>

### 🩺 **RF37 - Fichas de Anamnese**

**Descrição**: tela `/anamneses` da área Saúde. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Anamnese.
  * Buscar aluno.
  * Próxima.
  * Fechar.

* **Pontos de atenção para teste**: Selecionar modelo e iniciar em massa fictícia, responder perguntas condicionais, salvar pendente/concluída, reabrir e conferir histórico. Criação efetiva da ficha ainda não verificada.

* **Cenários**: [CT_RF37](Cenarios-de-testes/CT_RF37_Fichas-de-Anamnese.md)

---

<a id="rf38"></a>

### 🩺 **RF38 - Modelos de Anamnese**

**Descrição**: tela `/anamnese/modelos` da área Saúde. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Novo Modelo (/anamnese/modelos/novo).
  * Editar.
  * Preview.
  * Excluir.
  * Adicionar ao modelo.
  * Remover.
  * Limpar tudo.
  * Reordenar por arraste.
  * Mostrar preview.
  * Salvar Modelo.
  * Cancelar.

* **Pontos de atenção para teste**: Persistir ordem e obrigatoriedade; preview versus aplicação real; edição/exclusão de modelo já aplicado.

* **Cenários**: [CT_RF38](Cenarios-de-testes/CT_RF38_Modelos-de-Anamnese.md)

---

<a id="rf39"></a>

### 🩺 **RF39 - Categorias de Anamnese**

**Descrição**: tela `/anamnese/categorias` da área Saúde. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Categoria.
  * Editar.
  * Excluir.
  * Criar Categoria.
  * Cancelar.

* **Pontos de atenção para teste**: Validar ícones/cor, vínculo com perguntas e exclusão referenciada.

* **Cenários**: [CT_RF39](Cenarios-de-testes/CT_RF39_Categorias-de-Anamnese.md)

---

<a id="rf40"></a>

### 🩺 **RF40 - Perguntas de Anamnese**

**Descrição**: tela `/perguntas-anamnese` da área Saúde. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Pergunta.
  * Visualizar.
  * Deletar.
  * Salvar.
  * Cancelar.

* **Pontos de atenção para teste**: Verificar como pergunta se vincula à categoria, comportamento condicional e impacto em modelos e respostas anteriores.

* **Cenários**: [CT_RF40](Cenarios-de-testes/CT_RF40_Perguntas-de-Anamnese.md)

---

<a id="rf41"></a>

### 🤖 **RF41 - Inteligência e Automação**

**Descrição**: tela `/inteligencia-automacao` da área Inteligência. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Executar agora.
  * Configurar.
  * Ver resultados do risco.
  * Liga/desliga.
  * Salvar configuração.
  * Cancelar.

* **Pontos de atenção para teste**: Executar em ambiente isolado, conferir logs e destinatários, origem dos critérios e dados enviados. Nenhuma automação foi executada, ativada ou desativada. Confirmar se a configuração de Aniversariantes deveria usar critérios e preview próprios de aniversário.

* **Cenários**: [CT_RF41](Cenarios-de-testes/CT_RF41_Inteligencia-e-Automacao.md)

---

<a id="rf42"></a>

### 🤖 **RF42 - Resultados IA**

**Descrição**: tela `/inteligencia/resultados` da área Inteligência. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Alternar período.
  * Consultar resultados.

* **Pontos de atenção para teste**: Conferir janela temporal, cálculo e consistência entre central, resultados e home; executar automação isolada para observar resultados adicionais.

* **Cenários**: [CT_RF42](Cenarios-de-testes/CT_RF42_Resultados-IA.md)

---

<a id="rf43"></a>

### ⚙️ **RF43 - Configurações**

**Descrição**: tela `/configuracoes` da área Configurações. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Cancelar.
  * Salvar Configurações.
  * Em Aniversário alternar Mensagens/Endpoints & Tokens.
  * Inserir variáveis. WhatsApp: Salvar Configuração, Conectar por QR, Testar, Enviar Teste, Desconectar e Atualizar Status.

* **Pontos de atenção para teste**: Validar limites e efeitos em ambiente isolado; obter autorização e infraestrutura para catraca, WhatsApp e gateway. Valores de senhas, IPs, tokens e chaves não integram esta documentação.

* **Cenários**: [CT_RF43](Cenarios-de-testes/CT_RF43_Configuracoes.md)

---

<a id="rf44"></a>

### ⚙️ **RF44 - Modelos de Ficha**

**Descrição**: tela `/fichas-treino-modelo` da área Configurações. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Nova Ficha.
  * Criar Modelo.
  * Cancelar.

* **Pontos de atenção para teste**: Criar modelo de teste para acessar o editor posterior e conferir aplicação em ficha. Ações de edição/exclusão não foram observadas em lista vazia.

* **Cenários**: [CT_RF44](Cenarios-de-testes/CT_RF44_Modelos-de-Ficha.md)

---

<a id="rf45"></a>

### ⚙️ **RF45 - Aplicativo**

**Descrição**: tela `/aplicativo` da área Configurações. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Criar Notificação.
  * Visualizar/Deletar aviso existente.
  * Ver todas as notificações.
  * Só pendentes.
  * Ver todas as postagens.
  * Ver todas denúncias.
  * Enviar aviso.
  * Cancelar.

* **Pontos de atenção para teste**: Limites 179/180/181, edição de texto, entrega no app e moderação devem ser testados com grupo de teste isolado. Ações internas de posts/denúncias dependem de massa.

* **Cenários**: [CT_RF45](Cenarios-de-testes/CT_RF45_Aplicativo.md)

---

<a id="rf46"></a>

### 🔐 **RF46 - Meu perfil e controles globais**

**Descrição**: tela `/profile` da área Acesso. O sistema deve disponibilizar a consulta e as ações abaixo, respeitando os dados e permissões do usuário.

* **Funcionalidades esperadas**:

  * Meu perfil.
  * Segurança.
  * Preferências.
  * Sair do sistema.
  * Abrir notificações.
  * Marcar como lidas.
  * Tema.
  * Edit profile.
  * Show more.
  * Botão Abrir Academy Assistant em telas internas.

* **Pontos de atenção para teste**: Corrigir perfil, confirmar destino de Segurança e Preferências, testar acessibilidade, tema e notificações com conta de teste. Não foram alteradas senhas, preferências ou permissões.

* **Cenários**: [CT_RF46](Cenarios-de-testes/CT_RF46_Meu-perfil-e-controles-globais.md)

---

## 🧩 **Requisitos não funcionais observados**

* Mensagens de erro devem indicar a causa (campo inválido, vínculo impeditivo) em vez de erro interno.
* Campos sem valor devem ser exibidos como vazios ou “não informado”, sem o texto “null”.
* Indicadores e listas devem ser atualizados após cada operação, sem necessidade de recarregar a página.
* Datas e horários devem ser gravados em formato de 24 horas e exibidos no padrão brasileiro.

## 📝 **Observações**

* Este documento descreve o que foi observado na interface; não substitui a documentação oficial do SIFIT.
* Regras de negócio não documentadas (por exemplo, tratamento de contas ao cancelar matrícula) estão registradas como investigações em [pendências](anexos/pendencias-e-melhorias.md).
