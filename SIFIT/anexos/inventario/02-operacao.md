# Inventário · Operação da academia

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../../Cenarios-de-testes/) conforme a [correspondência de IDs](../correspondencia-de-ids.md).

**Data do levantamento:** 21/10/2026 · **Abrangência:** telas, campos e ações observados na interface.

## RF07 · Clientes

**Rota:** `/clientes` · **Área:** Operação

### Consulta e filtros

Código; Nome; Status; Situação; Plano; Personal; Buscar; paginação e tamanho 20/50/100.

### Campos e informações

Identificação: código, nome, status, sexo e nascimento; tipo sanguíneo; CPF e RG; foto JPG/PNG/GIF; telefone, celular/WhatsApp, emergência, e-mail; CEP, país, estado, cidade, logradouro, número, bairro, complemento; código do leitor, Sempre Liberado; usuário e senha do aplicativo; nome, telefone, profissão e CPF do responsável; estado civil, profissão e observação.

### Botões e ações

Novo Cliente; visualizar; Deletar; no formulário, Cancelar e Cadastrar Cliente. Perfil: Alterar imagem, Alterar dados, Editar objetivos, Aplicar Anamnese, Enviar mensagem, Agendar avaliação, Registrar pagamento, Ver todas as presenças e Ver histórico completo.

### O que foi observado

Novo cadastro /adicionar-cliente e edição /alterar-cliente/{id} foram abertos. Nome, status, sexo e nascimento têm marca de obrigatoriedade no cadastro. Perfil /visualizar-cliente/{id} exibe situação, desempenho de quatro semanas, metas, check-ins, objetivos, matrícula e financeiro. O registro de teste inspecionado mostrou vencimento 30/11/-0001. Editar objetivos não produziu mudança visível.

### O que falta validar

Criar, alterar e excluir apenas massa isolada; verificar obrigatórios, documentos, foto, responsável, duplicidade e vínculos. Explicar divergências entre histórico de check-ins e presenças. Confirmar identidade da conta no banco. Não registrar senhas na documentação.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF07_Clientes.md)

---

## RF08 · Matrículas

**Rota:** `/matriculas` · **Área:** Operação

### Consulta e filtros

Código; Nome; Buscar; Buscar por data; paginação; tamanho de página.

### Campos e informações

Funcionário cadastrante; data; status; Renovada; moeda; aluno por pesquisa; Modalidade (plano); data inicial e final; Pag. Via Sistema; tipo de pagamento; taxa de matrícula; dia de vencimento; valor da parcela; desconto; total; observação.

### Botões e ações

Cadastrar Matrícula (/adicionar-matricula); Visualizar; Cancelar matrícula; Deletar; Editar dentro da visualização; Salvar/Cancelar formulário.

### O que foi observado

Pesquisa de aluno por nome retornou o registro de teste e preencheu seu código e nome. A seleção de Plano Diário calculou parcela e total 20,00, término no mesmo dia e retirou Dia Vencimento. Nenhuma matrícula foi salva. Detalhes exibem funcionário, status, plano, datas, pagamento e valores.

### O que falta validar

Conferir geração de contas, datas, desconto, diária variável, período fixo, recorrência, renovação, personal/dependentes e anamnese após conclusão. Cancelamento e exclusão são operações diferentes.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF08_Matriculas.md)

---

## RF09 · Avaliações físicas

**Rota:** `/avaliacoes` · **Área:** Operação

### Consulta e filtros

Código; Nome; Status Todos/Pendente/Realizado; Buscar.

### Campos e informações

Agendamento: cadastrante, aluno por código/nome e busca, personal, data e hora. Realização: IMC (idade, altura, peso e resultado); circunferências (pescoço, ombro, tórax, braços, antebraços, abdômen, cintura, quadril, coxas, panturrilhas, relação cintura/quadril e resultado); subcutâneas (bíceps, tricipital, subescapular, axila, supra ilíaca, tórax, abdominal, coxa e panturrilha); composição corporal (% gordura, peso gordura, densidade, % e peso de massa magra, peso ideal e excesso).

### Botões e ações

Cadastrar Avaliação; Alterar e Fazer Avaliação nas pendentes; Imprimir, Relatório completo (PDF), Visualizar, Link e Comparação nas realizadas; Deletar; Salvar/Cancelar nos formulários.

### O que foi observado

As quatro abas de realização foram inspecionadas. Com valores fictícios 1,75 m e 70 kg, o campo calculou 22.857142857142858 sem salvar. O rótulo mostrou kg/m³. Não foram persistidas medidas nem concluída uma avaliação.

### O que falta validar

Validar agendamento, edição, realização, fórmulas aprovadas pelo responsável, unidades, arredondamento, formatos decimais, PDF, comparação e vínculos financeiros. Fórmulas corporais e interpretações clínicas não foram homologadas.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF09_Avaliacoes-fisicas.md)

---

## RF10 · Contas a Receber

**Rota:** `/contas-receber` · **Área:** Operação

### Consulta e filtros

Código; Nome; tipo de data; datas inicial/final; status; Buscar; Hoje; Ontem; Últimos 7 dias; Este mês.

### Campos e informações

Cadastrante, data, status, Resíduo; cliente por pesquisa; código e título; Criar cópias; valor a receber; moeda; vencimento; funcionário recebedor; valor e data de recebimento; tipo de pagamento; local de recebimento; observação.

### Botões e ações

Nova Conta; Visualizar; Deletar; Pesquisar cliente; Cancelar; Salvar.

### O que foi observado

Foram inspecionados listagem, indicadores e formulário. O cadastro abriu com status Recebido e seção Dados do Recebimento. Nenhum lançamento foi salvo.

### O que falta validar

Confirmar estados Pendente/Recebido, resíduos, cópias, descontos/multas/juros, baixa parcial, conciliação com caixa e exclusão vinculada. Recebimentos serão avaliados com lançamentos de teste no fluxo FL11, sem transação financeira real.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF11 · Contas a Pagar

**Rota:** `/contas-pagar` · **Área:** Operação

### Consulta e filtros

Código; Nome; tipo de data; datas inicial/final; status; Buscar; paginação; tamanho de página.

### Campos e informações

Cadastrante; data; status; tipo de despesa fixa/variável; tipo da conta; título; fornecedor por pesquisa; tipo de documento; documento do fornecedor; emissão; categoria; valor; vencimento; local de pagamento; observação.

### Botões e ações

Nova Conta; Visualizar; Deletar; Pesquisar fornecedor; Salvar; Cancelar.

### O que foi observado

O formulário abriu como Pendente, Variável e Contas e Despesas. A tela apresenta total a pagar, valor restante, contas listadas e atrasadas. Nenhum pagamento foi efetuado.

### O que falta validar

Conferir fornecedor/colaborador, categoria, documento, baixa parcial/total, vencimento, despesas fixas e caixa. Investigar totais zerados diante de conta pendente, respeitando os filtros.

[Cobertura](../matriz-de-rastreabilidade.md)

---
