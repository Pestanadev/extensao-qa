# Inventário · Saúde, Inteligência e Configurações

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../../Cenarios-de-testes/) conforme a [correspondência de IDs](../correspondencia-de-ids.md).

**Data do levantamento:** 21/10/2026 · **Abrangência:** telas, campos e ações observados na interface.

## RF37 · Fichas de Anamnese

**Rota:** `/anamneses` · **Área:** Saúde

### Consulta e filtros

Busca textual; status.

### Campos e informações

Total, concluídas, pendentes e clientes avaliados. Aplicação inicia com seleção do aluno por busca.

### Botões e ações

Nova Anamnese; buscar aluno; Próxima; Fechar.

### O que foi observado

Lista vazia. O assistente Aplicar Anamnese abriu etapa Selecionar Aluno. As etapas seguintes não foram concluídas. A pesquisa retornou aluno de teste e sua seleção abriu Selecionar Modelo, com modelo disponível e Iniciar desabilitado enquanto nenhum modelo estava selecionado. Iniciar não foi acionado porque pode criar uma ficha.

### O que falta validar

Selecionar modelo e iniciar em massa fictícia, responder perguntas condicionais, salvar pendente/concluída, reabrir e conferir histórico. Criação efetiva da ficha ainda não verificada.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF38 · Modelos de Anamnese

**Rota:** `/anamnese/modelos` · **Área:** Saúde

### Consulta e filtros

Busca; status; no montador, busca de pergunta e categoria.

### Campos e informações

Nome obrigatório; status; descrição; perguntas disponíveis e selecionadas; obrigatoriedade por pergunta; ordem; resumo de perguntas obrigatórias/opcionais; preview.

### Botões e ações

Novo Modelo (/anamnese/modelos/novo); Editar; Preview; excluir; Adicionar ao modelo; Remover; Limpar tudo; reordenar por arraste; Mostrar preview; Salvar Modelo; Cancelar.

### O que foi observado

Adicionar pergunta alterou a contagem de 0 para 1 e exibiu opção Obrigatória, Remover e preview. Salvar permaneceu desabilitado sem nome. Alteração local descartada sem salvar.

### O que falta validar

Persistir ordem e obrigatoriedade; preview versus aplicação real; edição/exclusão de modelo já aplicado.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF39 · Categorias de Anamnese

**Rota:** `/anamnese/categorias` · **Área:** Saúde

### Consulta e filtros

Busca; status.

### Campos e informações

Nome obrigatório; status; ícone Bootstrap Icons; atalhos de ícone; cor por seletor e hexadecimal; pré-visualização.

### Botões e ações

Nova Categoria; Editar; Excluir; Criar Categoria; Cancelar.

### O que foi observado

Cadastro inspecionado, com Criar Categoria desabilitado enquanto nome vazio. Há cartões de categorias ativas e inativas.

### O que falta validar

Validar ícones/cor, vínculo com perguntas e exclusão referenciada.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF40 · Perguntas de Anamnese

**Rota:** `/perguntas-anamnese` · **Área:** Saúde

### Consulta e filtros

Código; nome; status; Buscar.

### Campos e informações

Código; nome; status; pergunta; número/ordem; tipo de resposta Sim e Não, Sim/Não/Não Sei ou Se Sim, qual?.

### Botões e ações

Nova Pergunta; Visualizar; Deletar; Salvar; Cancelar.

### O que foi observado

Cadastro e tipos de resposta inspecionados. O formulário legado não mostrou seleção de categoria, embora montador e gestão de categorias existam.

### O que falta validar

Verificar como pergunta se vincula à categoria, comportamento condicional e impacto em modelos e respostas anteriores.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF41 · Inteligência e Automação

**Rota:** `/inteligencia-automacao` · **Área:** Inteligência

### Consulta e filtros

Atualizar dados da central.

### Campos e informações

Automações Risco de Evasão e Aniversariantes; estado ativo; frequência; canal; última execução/resultado; atividade recente. Risco: Diário/Semanal/Personalizado, horário, canais WhatsApp/E-mail/Apenas painel, destinatários, critérios, sensibilidade e preview.

### Botões e ações

Executar agora; Configurar; Ver resultados do risco; liga/desliga; Salvar configuração; Cancelar.

### O que foi observado

Configurar risco abriu frequência, canais, destinatários Dono/Financeiro/Recepção/Professor, critérios Ausência/Inadimplência/Baixa frequência/Treino abandonado/Queda de check-ins, sensibilidade e preview. Avaliações vencendo, Frequência em queda, Financeiro diário e Cobranças automáticas estão explicitamente Em desenvolvimento. Configurar Aniversariantes também foi aberto e apresentou os mesmos grupos de critérios de risco e preview de alunos em risco; coerência com aniversários ficou como INV-015.

### O que falta validar

Executar em ambiente isolado, conferir logs e destinatários, origem dos critérios e dados enviados. Nenhuma automação foi executada, ativada ou desativada. Confirmar se a configuração de Aniversariantes deveria usar critérios e preview próprios de aniversário.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF42 · Resultados IA

**Rota:** `/inteligencia/resultados` · **Área:** Inteligência

### Consulta e filtros

Hoje; Últimos 7, 30 e 90 dias.

### Campos e informações

Automações executadas; relatórios enviados; risco; frequência em queda; aniversariantes; avaliações vencendo; inadimplentes; frequência média; achados; automações eficientes; resumo Inteligência Sifit.

### Botões e ações

Alternar período; consultar resultados.

### O que foi observado

A tela carregou métricas e mensagens de ausência de execução/achados no período inicial.

### O que falta validar

Conferir janela temporal, cálculo e consistência entre central, resultados e home; executar automação isolada para observar resultados adicionais.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF43 · Configurações

**Rota:** `/configuracoes` · **Área:** Configurações

### Consulta e filtros

Abas Home, Biometria, Avaliação, Aniversário, Pagamento, Integrações e Design.

### Campos e informações

Home: plano do Sifit (desabilitado), acesso desktop, presença, Box, turmas, dias de ausência, multa, juros, comprovante desktop e anamnese ao concluir matrícula. Biometria: possui, marca/modelo, código, porta, IP, login/senha, dias para travar e aparelho separado. Avaliação: cobrar, tipo e teste físico. Aniversário: envio automático, canais, mensagem, variáveis, origem SMS/e-mail. Pagamento: habilitar e token. Integrações: provider, API URL/key, instância e ativo. Design: cores, logo e capa.

### Botões e ações

Cancelar; Salvar Configurações; em Aniversário alternar Mensagens/Endpoints & Tokens; inserir variáveis. WhatsApp: Salvar Configuração, Conectar por QR, Testar, Enviar Teste, Desconectar e Atualizar Status.

### O que foi observado

Todas as sete abas e a subaba Endpoints & Tokens foram abertas. WhatsApp estava desconectado, inativo e sem configuração, com Conectar/Testar/Enviar/Desconectar desabilitados. Nenhuma configuração foi salva. Valor negativo de dias de ausência foi observado no ambiente, mas não foi criado nesta sessão.

### O que falta validar

Validar limites e efeitos em ambiente isolado; obter autorização e infraestrutura para catraca, WhatsApp e gateway. Valores de senhas, IPs, tokens e chaves não integram esta documentação.

[Cenários deste módulo](../../Cenarios-de-testes/CT_RF43_Configuracoes.md)

---

## RF44 · Modelos de Ficha

**Rota:** `/fichas-treino-modelo` · **Área:** Configurações

### Consulta e filtros

Código; título; criador; Buscar.

### Campos e informações

Cadastro inicial: nome do modelo e personal.

### Botões e ações

Nova Ficha; Criar Modelo; Cancelar.

### O que foi observado

Lista vazia; indicadores de modelos, criadores, listados e sem criador. Formulário inicial inspecionado.

### O que falta validar

Criar modelo de teste para acessar o editor posterior e conferir aplicação em ficha. Ações de edição/exclusão não foram observadas em lista vazia.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF45 · Aplicativo

**Rota:** `/aplicativo` · **Área:** Configurações

### Consulta e filtros

Só pendentes para postagens; Ver todas para notificações, postagens e denúncias.

### Campos e informações

Usuários ativos do app e novos posts; notificações com código, mensagem e data; postagens com status/data; denúncias com motivo, autor, data e status. Aviso: destinatário fixo Todos os alunos, mensagem até 180 caracteres e prévia no celular.

### Botões e ações

Criar Notificação; Visualizar/Deletar aviso existente; Ver todas as notificações; Só pendentes; Ver todas as postagens; Ver todas denúncias; Enviar aviso; Cancelar.

### O que foi observado

Criar Notificação foi aberto, com Enviar aviso desabilitado sem texto. Destinatário Todos os alunos está desabilitado para alteração. Não foram publicados avisos nem moderados conteúdos.

### O que falta validar

Limites 179/180/181, edição de texto, entrega no app e moderação devem ser testados com grupo de teste isolado. Ações internas de posts/denúncias dependem de massa.

[Cobertura](../matriz-de-rastreabilidade.md)

---
