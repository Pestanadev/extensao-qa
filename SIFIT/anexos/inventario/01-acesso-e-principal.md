# Inventário · Acesso e Principal

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../../Cenarios-de-testes/) conforme a [correspondência de IDs](../correspondencia-de-ids.md).

**Data do levantamento:** 21/10/2026 · **Abrangência:** telas, campos e ações observados na interface.

## RF01 · Autenticação e sessão

**Rota:** `/login` · **Área:** Acesso

### Consulta e filtros

Não se aplica.

### Campos e informações

Login; Senha; Manter conectado (desmarcado durante a inspeção).

### Botões e ações

Entrar; Esqueci minha senha; Sair do sistema no menu da conta.

### O que foi observado

Credenciais fornecidas abriram /dashboard. A interface identifica a conta como Jair. Credenciais fictícias foram rejeitadas. Após sair, abrir /clientes retornou ao login. O link de recuperação permaneceu na mesma tela.

### O que falta validar

Persistência de Manter conectado após fechar e reabrir o navegador; expiração de sessão; diferentes perfis; recuperação de senha após correção.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF01_Autenticacao-e-sessao.md)

---

## RF02 · Página Inicial

**Rota:** `/dashboard` · **Área:** Principal

### Consulta e filtros

Período inicial e final; botão Buscar; seleção Hoje no gráfico por horário; buscas locais nos detalhamentos.

### Campos e informações

Indicadores de risco, valor em aberto, pico de movimento e avaliações pendentes; clientes ativos e ausentes; sem matrícula; personais; matrículas, desistências e renovações; análise de retenção; saúde da academia; motivos de risco; agenda; últimas entradas; aniversariantes.

### Botões e ações

Ver detalhes; cartões de ausentes, sem matrícula, personais, matrículas e desistências; Ver análise completa; Cobrar agora; Enviar mensagem; Ver avaliações; Ver todas as mensalidades; Cobrar todos no WhatsApp; Ver agenda; Ver todos nas entradas e aniversários.

### O que foi observado

Foram abertos os detalhamentos de ausentes, sem matrícula, personais, matrículas, desistências e financeiro. Ausentes oferece visualizar cliente e Remover da lista. Os detalhamentos possuem busca e fechamento. Financeiro mostra Exportar, faixas de atraso, paginação, cobrança e Registrar pagamento. Alguns links com destino # abrem modais.

### O que falta validar

Conciliar indicadores com o banco e regras de período. Cartão Sem Matrículas mostrou 6 e modal inicialmente mostrou 0, mas na revisão exibiu 6 registros e total 6; a divergência inicial não se repetiu; desistências mostrou total 2 e lista vazia. Confirmar critérios antes de classificar causa. Atalhos de mensagem, exportação e registro financeiro não foram concluídos.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF02_Pagina-Inicial.md)

---

## RF03 · Dashboard analítico

**Rota:** `/dash` · **Área:** Principal

### Consulta e filtros

Não foram apresentados filtros próprios na área principal.

### Campos e informações

Inteligência Sifit; risco, aniversários, avaliações vencendo e frequência em queda; gráficos de frequência, idade, sexo, matrículas por mês e plano, contas por método e mês, cancelamentos, avaliações por mês e personal.

### Botões e ações

Ver Inteligência; navegação global.

### O que foi observado

Os gráficos carregaram, mas o título principal permaneceu Despesas Fixas. O item Dashboard estava selecionado no menu.

### O que falta validar

Validar origem, período, séries e agregações dos gráficos com o banco. Título registrado em BUG-002.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF03_Dashboard-analitico.md)

---

## RF04 · Check-in

**Rota:** `/checkin` · **Área:** Principal

### Consulta e filtros

Unidade; busca de cliente; Todos; Presentes agora; Não compareceram; Check-in pendente; Filtros.

### Campos e informações

Contadores de check-ins de hoje, presentes, meta, média diária e taxa de frequência; tabela com cliente, plano, horário, entrada, saída, unidade, status e ação; código de Entrada rápida.

### Botões e ações

Check-in manual; Escanear QR Code; Realizar check-in; Registrar entrada na linha; Ver todos nos presentes; notificações.

### O que foi observado

Entrada manual abriu busca por nome, código ou CPF e abas Cliente existente, Visitante / Aula experimental e Sem biometria. Registrar entrada fica desabilitado sem seleção. O clique em Filtros não apresentou mudança perceptível na inspeção.

### O que falta validar

Executar entrada e saída em cliente de teste, duplicidade, matrícula inativa, unidade, visitante, QR e biometria. Comportamento de Filtros pendente de reprodução. Não foram registrados check-ins por esta exploração.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF05 · Presenças

**Rota:** `/presencas` · **Área:** Principal

### Consulta e filtros

Busca textual; De; Até; Buscar; Hoje; Esta semana; Este mês.

### Campos e informações

Total no período; alunos distintos; média por dia; dias no período; resultados de presença.

### Botões e ações

Consultar e alternar períodos.

### O que foi observado

O período inicialmente consultado exibiu Nenhuma presença encontrada e orientação para ajustar período ou busca.

### O que falta validar

Usar intervalo com registros e comparar contagens, unidades, horários e fronteiras de datas com o banco.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF06 · SifitBox — aulas

**Rota:** `/sifitbox/aulas` · **Área:** Principal

### Consulta e filtros

Data inicial e final; Buscar.

### Campos e informações

Lista de aulas do período.

### Botões e ações

Gerar aulas.

### O que foi observado

A consulta exibiu Nenhuma aula encontrada no período. Gerar aulas não foi acionado, pois pode criar registros.

### O que falta validar

Geração baseada em turmas recorrentes, repetição sem duplicidade, vagas, reservas e ações de aula que só aparecem com dados.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF46 · Meu perfil e controles globais

**Rota:** `/profile` · **Área:** Acesso

### Consulta e filtros

Menu da conta; notificações Tudo/Não lidas; seleção de tema claro/escuro.

### Campos e informações

Menu: Meu perfil, Segurança, Preferências, Sair. Notificações: risco, financeiro e avaliações. Perfil: conteúdo de demonstração em inglês, cabeçalhos Usuário/Documentos/Endereço/About me.

### Botões e ações

Meu perfil; Segurança; Preferências; Sair do sistema; abrir notificações; Marcar como lidas; tema; Edit profile; Show more; botão Abrir Academy Assistant em telas internas.

### O que foi observado

Meu perfil exibiu Hello Jesse e Jessica Jones. Segurança e Preferências apontam para /configuracoes. Notificações foram abertas sem marcar como lidas. O tema já estava escuro; a preferência não foi alterada. O assistente não recebeu comandos.

### O que falta validar

Corrigir perfil, confirmar destino de Segurança e Preferências, testar acessibilidade, tema e notificações com conta de teste. Não foram alteradas senhas, preferências ou permissões.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF46_Meu-perfil-e-controles-globais.md)

---
