# 2 - Plano de Testes - SIFIT

## Objetivo
Validar manualmente as principais funcionalidades do SIFIT, registrando evidências em vídeo e print.

## Escopo
**Dentro do escopo:** login, dashboard, notificações, financeiro, treinos (modelo de ficha), configurações, inteligência e automação, atividades, produtos, aplicativo e cadastros auxiliares (perguntas, categorias, modelos e fichas de análise, enquetes, tipos de documentos, fornecedores, funções, colaboradores, turmas, bandeiras de cartão, tipos de pagamento, modelos de contrato, planos, grupos, prospecção, categorias de crossfit, objetivos de treino, grupos musculares, biblioteca de exercícios, fichas de treino, contas a receber, contas a pagar, caixas, avaliações, despesas fixas e relatórios).  
**Fora do escopo:** testes de carga, segurança e automação.

## Tipos de teste
- Positivo (fluxo esperado)
- Negativo (dados vazios ou inválidos)
- Exploratório / funcional (navegação e comportamento das telas, incluindo cadastro, edição, consulta, inativação e exclusão)

> Observação: por causa do limite de gravações do Jam, em vários vídeos os testes positivo e negativo foram gravados juntos.

## Ambiente
| Item | Detalhe |
|---|---|
| Sistema | SIFIT - versão web (e aplicativo) |
| Navegador | Google Chrome |
| Sistema operacional | Windows 11 |
| Banco de dados | MySQL (consulta via MySQL Workbench) |

## Ferramentas
- **Jam** (extensão do Chrome) - gravação de vídeos e prints como evidência
- **MySQL Workbench** - conferência dos dados no banco
- **Markdown / GitHub** - documentação

## Critérios
- **Passou:** o sistema respondeu conforme o esperado.
- **Falhou:** comportamento diferente do esperado; abrir registro em `3-Relatorio-de-Bugs.md`.

## Entregáveis
`1-Analise-de-requisitos.md`, `2-plano-de-testes.md`, `3-Relatorio-de-Bugs.md`, `4-Relatorio-dos-testes.md` e a pasta `Cenarios-de-testes`.
