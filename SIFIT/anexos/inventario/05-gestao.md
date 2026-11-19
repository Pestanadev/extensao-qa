# Inventário · Gestão

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../../Cenarios-de-testes/) conforme a [correspondência de IDs](../correspondencia-de-ids.md).

**Data do levantamento:** 21/10/2026 · **Abrangência:** telas, campos e ações observados na interface.

## RF29 · Colaboradores

**Rota:** `/colaboradores` · **Área:** Gestão

### Consulta e filtros

Código; nome; Buscar; paginação e tamanho.

### Campos e informações

Tipo de login Admin/Normal/Sem login; Avaliador Sim/Não; código, nome, status, nascimento, sexo, tipo sanguíneo; CPF, RG e CREF; login e senha; telefones, emergência e e-mail; país/estado/cidade/endereço/número/bairro/complemento/CEP; biometria; observação.

### Botões e ações

Novo Colaborador (/adicionar-colaborador); Funções; Visualizar (/visualizar-colaborador/{id}); Deletar; Salvar; Cancelar. Perfil do colaborador: Editar; abas Resumo, Funções, Alunos e Recebimentos; selecionar e Adicionar função; Remover função.

### O que foi observado

Cadastro inspecionado com Normal e Não avaliador selecionados. Permissões de função são uma dimensão distinta do tipo de login. Não foram criadas contas nem alteradas credenciais. O perfil individual foi aberto: Resumo mostra dados pessoais, contato e endereço; Funções mostra cargo/status e permite adicionar/remover; Alunos e Recebimentos exibiram estados vazios no registro consultado.

### O que falta validar

Vincular função e conferir acesso com contas de teste dedicadas; testar Sem login e restrições sem conceder acesso real. Validar persistência das associações e o preenchimento das abas com massa conhecida.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF30 · Funções e permissões

**Rota:** `/funcoes` · **Área:** Gestão

### Consulta e filtros

Código; nome; tipo; Buscar.

### Campos e informações

Código; nome; tipo de funcionário Interno/Externo; Personal; Avaliador. Matriz de permissões por área.

### Botões e ações

Nova Função; Permissões; Visualizar; Salvar Função; Salvar permissões; Cancelar.

### O que foi observado

Foram abertos cadastro e matriz de permissões. Ela inclui administrativo, clientes, colaboradores, avaliações, fichas, financeiro, contas e caixas, entre outras áreas. Existem permissões específicas para visualizar IDs, cadastrar biometria, receber/pagar, alterar valores/datas, reabrir caixa e gerenciar funções. Nenhuma permissão foi alterada.

### O que falta validar

Testar autorização no servidor e na interface com perfis isolados, incluindo acesso direto às rotas. Exclusão de função não foi observada.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF31 · Fornecedores

**Rota:** `/fornecedores` · **Área:** Gestão

### Consulta e filtros

Código; nome; Buscar.

### Campos e informações

Pessoa Física/Jurídica; nome obrigatório; status; CNPJ para Jurídica; telefone principal/alternativo/celular; e-mail; estado/cidade/CEP/endereço/número/bairro/complemento; observação. Ao selecionar Pessoa Física aparecem nascimento, sexo, CPF e RG; em Jurídica aparece CNPJ.

### Botões e ações

Novo Fornecedor; Visualizar; Deletar; Salvar; Cancelar.

### O que foi observado

Cadastro aberto em Pessoa Jurídica. Indicadores de cadastrados e ativos. Alternância para Física foi inspecionada sem salvar e revelou nascimento, sexo, CPF e RG.

### O que falta validar

Testar documentos por tipo de pessoa, estado/cidade, duplicidade e exclusão com contas vinculadas.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF32 · Tipos de Documentos

**Rota:** `/tipos-documento` · **Área:** Gestão

### Consulta e filtros

Código; nome; aplicação; Buscar.

### Campos e informações

Código; nome; aplicação Conta/Fornecedor ou Colaborador.

### Botões e ações

Novo Tipo; Visualizar; Deletar; Salvar; Cancelar.

### O que foi observado

Indicadores de total e aplicações por fornecedor/colaborador. Formulário inspecionado.

### O que falta validar

Verificar disponibilidade por aplicação nas contas e exclusão com referências.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF33 · Atividades

**Rota:** `/atividades` · **Área:** Gestão

### Consulta e filtros

Código; nome; Buscar.

### Campos e informações

Código; nome; pontuação; descrição.

### Botões e ações

Nova Atividade; Visualizar; Deletar; Salvar; Cancelar.

### O que foi observado

Indicadores de total, com/sem pontuação e descrição. O cadastro foi inspecionado.

### O que falta validar

Validade de pontuação negativa/zero, vínculo com campanhas e efeitos de alteração/exclusão.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF34 · Pontuação

**Rota:** `/pontuacao` · **Área:** Gestão

### Consulta e filtros

Código; nome; status; Buscar.

### Campos e informações

Código; nome; início/fim; tipo Mensal/Por período; status; produtos de resgate.

### Botões e ações

Nova Pontuação; selecionar produto; Adicionar; Salvar; Cancelar; ações nas linhas sem nome acessível.

### O que foi observado

Cadastro inspecionado. Na árvore de acessibilidade as linhas apareceram como botões sem nome; isso não comprova que os textos estão ausentes visualmente.

### O que falta validar

Campanhas, produtos de resgate, pontos necessários, datas, crédito/resgate e ações de linha devem ser verificadas com massa isolada. Auditar nomes acessíveis dos botões.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF35 · Produtos

**Rota:** `/produtos` · **Área:** Gestão

### Consulta e filtros

Código; nome; status; tipo; Buscar.

### Campos e informações

Código; nome; status; descrição; tipo Venda/Pontuação; preço no modo Venda e pontuação no modo Pontuação; imagens por seleção de arquivos.

### Botões e ações

Novo; Salvar; Cancelar; escolher imagens; ações de linha sem nome acessível.

### O que foi observado

Formulário de Venda inspecionado. O tipo Pontuação foi selecionado sem salvar e substituiu Preço pelo campo Pontuação. Botões sem nome foram observados na acessibilidade da lista.

### O que falta validar

Validar persistência de produto por pontuação, edição, exclusão, mídia e vínculos com campanhas. Não inferir controle de estoque: campo de estoque não foi observado.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF36 · Enquetes

**Rota:** `/enquetes` · **Área:** Gestão

### Consulta e filtros

Código; nome; status; Buscar.

### Campos e informações

Código; nome; status; pergunta; lista de respostas, inicialmente Resposta 1.

### Botões e ações

Nova Enquete; Visualizar; Deletar; Adicionar resposta; Salvar; Cancelar.

### O que foi observado

Lista com código, nome, pergunta e status. Alguns registros exibem Sem pergunta cadastrada. Formulário inspecionado.

### O que falta validar

Pergunta/respostas obrigatórias, múltiplas alternativas, votação no app, contagem e alterações após votos.

[Cobertura](../matriz-de-rastreabilidade.md)

---
