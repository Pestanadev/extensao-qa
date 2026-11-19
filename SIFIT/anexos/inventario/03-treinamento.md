# Inventário · Treinamento

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../../Cenarios-de-testes/) conforme a [correspondência de IDs](../correspondencia-de-ids.md).

**Data do levantamento:** 21/10/2026 · **Abrangência:** telas, campos e ações observados na interface.

## RF12 · Fichas de Treino

**Rota:** `/fichas-treino` · **Área:** Treinamento

### Consulta e filtros

Código; nome do aluno; status; Buscar; Limpar filtros; paginação e tamanho.

### Campos e informações

Funcionário cadastrante; lançamento; aluno por pesquisa; personal; datas inicial/final; objetivo; observação.

### Botões e ações

Cadastrar Ficha; Pesquisar aluno; Criar Nova Ficha; Usar Modelo de Ficha; Cancelar.

### O que foi observado

Lista vazia após carregamento, com indicadores de cadastradas, ativas, vencendo em sete dias e inativas/canceladas. Formulário inicial inspecionado. O editor posterior à criação não foi acessado porque depende de gravar uma ficha.

### O que falta validar

Editor de exercícios, séries, repetições, impressão e ações de linha pendentes de levantamento após a criação de uma ficha de teste.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF13 · Exercícios

**Rota:** `/exercicios` · **Área:** Treinamento

### Consulta e filtros

Organização por grupo muscular; não foi exibido campo global de busca.

### Campos e informações

Código; nome obrigatório; imagem JPG/PNG até 5 MB; vídeo MP4/MOV até 50 MB.

### Botões e ações

Adicionar por grupo; Visualizar; Deletar; Procurar imagem/vídeo; Salvar; Cancelar; Fechar.

### O que foi observado

Biblioteca carregou exercícios e grupos vazios. O formulário é aberto dentro do grupo escolhido. Total global e totais por grupo são exibidos.

### O que falta validar

Persistir mídia de teste, limites e extensões; alteração de nome/mídia; integridade com ficha e grupo; tratamento de exclusão vinculada.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF14 · Grupos Musculares

**Rota:** `/grupos-musculares` · **Área:** Treinamento

### Consulta e filtros

Código; nome; tipo de membro; Buscar; Limpar filtros; paginação e tamanho.

### Campos e informações

Código; nome; tipo de membro; imagem por arquivo.

### Botões e ações

Cadastrar grupo; Visualizar; Deletar; Escolher arquivo; Salvar; Cancelar.

### O que foi observado

Indicadores de grupos cadastrados, superiores, inferiores e aeróbio. O formulário foi aberto e cancelado.

### O que falta validar

Tipos permitidos, imagem, nomes repetidos e exclusão quando há exercícios vinculados.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF15 · Objetivos Treino

**Rota:** `/objetivos-treino` · **Área:** Treinamento

### Consulta e filtros

Código; nome; Buscar.

### Campos e informações

Código; nome; descrição.

### Botões e ações

Novo Objetivo; Salvar; Cancelar.

### O que foi observado

Lista vazia, com indicadores de objetivos, exibidos e com descrição. Formulário inspecionado; ações de registros existentes não foram observadas.

### O que falta validar

Cadastrar objetivo de teste e descobrir edição/exclusão disponíveis; vincular à ficha. Não assumir CRUD completo por analogia.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF16 · Grupos

**Rota:** `/grupos` · **Área:** Treinamento

### Consulta e filtros

Código; nome; status; tipo de caixa; Buscar.

### Campos e informações

Código; nome; status; Mostrar Home; tipo de caixa Interno/Externo; descrição.

### Botões e ações

Novo Grupo; Visualizar; Deletar; Salvar Grupo; Cancelar; Fechar.

### O que foi observado

Mostra grupos, ativos, exibição na home e caixa externo. Novo formulário inspecionado.

### O que falta validar

Verificar impacto do grupo nos planos, home e caixa; exclusão com vínculos.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF17 · Turmas

**Rota:** `/turmas` · **Área:** Treinamento

### Consulta e filtros

Código; nome da turma; status; Buscar; Limpar filtros.

### Campos e informações

Código; nome; status; plano; Aula Experimental; tempo em meses; horas inicial/final; Tem Personal; dias da semana, de segunda a domingo.

### Botões e ações

Cadastrar Turma; Editar; Deletar; selecionar dias; Salvar; Cancelar.

### O que foi observado

Lista apresenta plano, horário, dias e status. Indicadores de cadastradas, ativas, com personal e aula experimental. Formulário inspecionado.

### O que falta validar

Horários iguais/invertidos, dias vazios, personal condicional, sobreposição e vínculos com plano.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF18 · Categorias Crossfit

**Rota:** `/categorias-exercicios-crossfit` · **Área:** Treinamento

### Consulta e filtros

Código; nome da categoria; Buscar; Limpar filtros.

### Campos e informações

Código; nome.

### Botões e ações

Nova Categoria; Editar; Deletar; Salvar; Cancelar.

### O que foi observado

Lista exibe datas de criação e atualização e indicadores de categorias, exibidas e atualizadas.

### O que falta validar

Atualização das datas, unicidade e exclusão com vínculos de exercícios.

[Cobertura](../matriz-de-rastreabilidade.md)

---

## RF19 · SifitBox — turmas e modalidades

**Rota:** `/sifitbox/turmas` · **Área:** Treinamento

### Consulta e filtros

Não distinguir os campos de entrada como filtros sem testar: a tela apresenta formulários junto às listas.

### Campos e informações

Modalidade: nome, descrição e status. Turma recorrente: nome, modalidade, hora inicial/final, dias Dom–Sáb, vagas e status.

### Botões e ações

Botões + Modalidade e + Turma; ícones de editar e excluir nas duas listas.

### O que foi observado

Formulários ficam na própria tela. Um clique em + Modalidade com campos vazios não apresentou confirmação visível. O tema escuro exibiu cartões brancos com texto muito claro, dificultando a leitura.

### O que falta validar

Validar significado dos botões e mensagens de obrigatoriedade com massa isolada; edição, exclusão, limite de vagas e geração de aulas. Operações de persistência não executadas.

[Cobertura](../matriz-de-rastreabilidade.md)

---
