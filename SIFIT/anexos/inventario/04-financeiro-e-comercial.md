# Inventário · Financeiro e Comercial

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../../Cenarios-de-testes/) conforme a [correspondência de IDs](../correspondencia-de-ids.md).

**Data do levantamento:** 21/10/2026 · **Abrangência:** telas, campos e ações observados na interface.

## RF20 · Caixas

**Rota:** `/caixas` · **Área:** Financeiro

### Consulta e filtros

Data inicial/final; status; Buscar; paginação; tamanho de página.

### Campos e informações

Visualização abre Fechamento de Caixa: usuário, datas inicial/final e Local de Contas.

### Botões e ações

Abrir Caixa; Visualizar; Imprimir; no fechamento Buscar Contas, Salvar, Cancelar e Fechar.

### O que foi observado

Indicadores de abertos, fechados, locais e registros no período. O botão Visualizar de um caixa aberto abriu formulário de fechamento. Nenhum caixa foi aberto ou fechado.

### O que falta validar

Detalhar abertura, fechamento, reabertura, conferência e ajuste após criar ambiente financeiro de teste; conciliar contas e totais. Ações adicionais constam nas permissões, mas não foram executadas.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF21 · Pagar.me

**Rota:** `/pagarme` · **Área:** Financeiro

### Consulta e filtros

Seletor Últimos 30 dias no gráfico.

### Campos e informações

Saldo disponível, processamento, recebíveis futuros, recebido no mês, gráfico, métodos de pagamento, transações, repasses, assinaturas e chargebacks.

### Botões e ações

Solicitar saque; Ver previsão; Ver recebíveis; Ver relatório completo; Ver extrato completo; Nova cobrança; Configurações; Ver todas as transações e demais Ver todas.

### O que foi observado

Havia valores -- em diversas áreas e gráfico com valores e datas apresentados. Sem ambiente de integração conhecido, não é possível afirmar quais valores são reais ou demonstrativos.

### O que falta validar

Confirmar sandbox e token com responsável; testar apenas nesse ambiente. Saques, cobranças, transferência e mudanças na integração não foram acionados.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF22 · Despesas Fixas

**Rota:** `/despesas-fixas` · **Área:** Financeiro

### Consulta e filtros

Código; nome; status; recorrência; Buscar.

### Campos e informações

Código; nome; status; valor; recorrência.

### Botões e ações

Nova Despesa; Visualizar; Deletar; Salvar Despesa; Cancelar; Fechar.

### O que foi observado

Lista exibe valor, recorrência e status; indicadores de despesas, ativas, inativas e valor listado. Cadastro aberto com recorrência 1 Dia.

### O que falta validar

Geração das contas periódicas, datas, repetição sem duplicar e efeito de inativação.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF23 · Relatórios

**Rota:** `/relatorios` · **Área:** Financeiro

### Consulta e filtros

Tipo de relatório; início/fim; filtros condicionais por tipo.

### Campos e informações

Sete tipos: Avaliações, Clientes, Colaboradores, Matrículas, Contas a Receber, Contas a Pagar e Caixas. Contas a Receber acrescenta tipo de pagamento, status e opção Detalhado. Matrículas mostra Plano e Tipo de Plano (Todos/Mensal/Trimestral/Semestral/Anual/Diária); Caixas mostra Formato Normal/Detalhado. Avaliações, Clientes, Colaboradores e Contas a Pagar apresentaram tipo e datas, sem outros filtros visíveis nesta inspeção.

### Botões e ações

Selecionar tipo por cartão ou lista; Gerar Relatório (PDF).

### O que foi observado

Gerar Relatório ficou habilitado após carregamento. A alternância para Contas a Receber revelou os filtros específicos. PDFs não foram gerados nesta sessão. Os sete tipos foram selecionados para inspeção dos filtros, sem gerar PDF.

### O que falta validar

Gerar PDFs dos sete tipos com massa conhecida e comparar linhas, totais e datas com consultas ao banco.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF24 · Prospecção

**Rota:** `/prospeccao` · **Área:** Comercial

### Consulta e filtros

Buscar lead; estágio; Limpar.

### Campos e informações

Nome; estágio do lead; e-mail; telefone; observação; código automático.

### Botões e ações

Adicionar Lead; Visualizar; Deletar; Salvar Lead; Cancelar; Fechar.

### O que foi observado

Lista com código, nome, estágio e criação. Indicadores de leads, novos contatos e interessados. Novo lead inicia em Novo Contato.

### O que falta validar

Estágios e transições permitidas, duplicidades, contato inválido, edição e exclusão.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF25 · Planos

**Rota:** `/planos` · **Área:** Comercial

### Consulta e filtros

Código; nome; status; Buscar.

### Campos e informações

Código; nome; grupo; status; cobrança Mensalidade recorrente/Diária/Período fixo; parcelas; valor mensal/diária; matrícula; Tem Personal; função dos professores; dependentes de 0 a 6; benefícios.

### Botões e ações

Novo Plano; Visualizar; Deletar; adicionar benefício; Salvar Plano; Salvar também na Pagar.me quando disponível; Cancelar.

### O que foi observado

Foram alternados os três tipos de cobrança sem salvar. Diária mostra Valor Diária e Dias na matrícula?; Período fixo mostra Quantidade e Período. Adicionar benefício criou campo local. Ranking mostra planos com mais alunos, baseado em matrículas carregadas.

### O que falta validar

Persistência de cada tipo, datas e parcelas, benefícios, dependentes, personal e conciliação do ranking. Integração Pagar.me apenas em sandbox.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF26 · Modelos de Contrato

**Rota:** `/modelos-contrato` · **Área:** Comercial

### Consulta e filtros

Não foram exibidos filtros na lista inicial.

### Campos e informações

Título; status; texto rico; preview; variáveis de aluno, plano, academia e contrato; contadores de palavras e caracteres.

### Botões e ações

Adicionar Modelo Contrato (/adicionar-modelo-contrato); estilos de parágrafo/cabeçalho; negrito, itálico, sublinhado, tachado, alinhamento, listas, link, desfazer/refazer; Atualizar preview; inserir variável; Como usar?; Ver todas as variáveis; Salvar modelo; Cancelar.

### O que foi observado

Editor e grupos de variáveis foram inspecionados. Variáveis incluem nome/CPF/RG/telefone/e-mail/nascimento do aluno, plano/valor/extenso/vencimento/duração, academia/CNPJ/endereço e datas/número/responsável do contrato.

### O que falta validar

Testar editor, substituição de variáveis e contrato gerado com dados fictícios. Ações de edição/exclusão em lista vazia não foram observadas. Nenhum contrato foi assinado.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF27 · Tipos de Pagamento

**Rota:** `/tipos-pagamento` · **Área:** Comercial

### Consulta e filtros

Código; nome; status; tipo; Buscar.

### Campos e informações

Código; nome; status; Escolher Bandeira; tipo Débito/Crédito; Pagamento Pelo Sistema.

### Botões e ações

Novo; Visualizar; Deletar; Salvar; Cancelar.

### O que foi observado

Lista com tipo, via gateway e status. Cadastro inspecionado. A contagem de ativos e disponibilidade em matrículas precisam de conciliação.

### O que falta validar

Efeito de status, seleção de bandeira e gateway nos formulários financeiros; exclusão com vínculos.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF28 · Bandeiras

**Rota:** `/bandeiras` · **Área:** Comercial

### Consulta e filtros

Código; nome; Buscar.

### Campos e informações

Código; nome; taxa adicional; taxa débito; Multiplica taxa adicional por mês; parcelas com código, número e taxa.

### Botões e ações

Nova Bandeira; Adicionar Parcela; Salvar; Cancelar.

### O que foi observado

Nenhuma bandeira encontrada. Cadastro de bandeira e tabela de parcelas inspecionados.

### O que falta validar

Criar bandeira de teste, mapear edição/exclusão após criação e validar taxas e parcelamento com massa conhecida.

[Cobertura](../matriz-de-rastreabilidade.md)

---
