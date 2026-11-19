# Conferência do banco pelo MySQL Workbench

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../Cenarios-de-testes/) conforme a [correspondência de IDs](correspondencia-de-ids.md).

**Data:** 18/11/2026, 01:31–01:35 (horário local; o servidor registrou `NOW()` = 2026-11-18 04:31:49) · **Execução:** Claude, pela sessão do MySQL Workbench já aberta e conectada pelo Arthur · **Natureza:** somente leitura (`SELECT` em tabelas e em `information_schema`). Nenhuma senha foi digitada ou extraída; nenhum dado, estrutura ou permissão foi alterado.

## Resultado

**O esquema acessível pela conexão “SIFIT” do Workbench não corresponde ao SIFIT gravado nos vídeos.** A conclusão se apoia na estrutura e nas datas, não na quantidade de produtos:

1. **Nenhuma entidade de academia.** Das 43 tabelas, nenhuma corresponde a planos, turmas, anamnese, matrículas, alunos, exercícios, fichas, treinos, caixas, fornecedores, colaboradores, enquetes, avaliações ou despesas. Não há colunas com esses termos ([DB-01](../evidencias/imagens/DB-01-esquema-sem-tabelas-academia.jpg)).
2. **Estrutura de loja virtual.** Existem `produtos` (com `ncm`, `ean`, `peso_embalado`, `preco_pix`), `pedidos` (com `codigo_rastreio`, `valor_frete`, `pix_qr_code`), `cupons`, `marcas`, `banners`, `combos`, `melhor_envio`, `instagram_posts` e `newsletter`.
3. **Migrations de e-commerce.** As 24 migrations registradas tratam de marcas, artigos, parceiros/cupons, banners, Instagram, “mais vendidos” e autenticação social. Nenhuma cria entidade de academia.
4. **Catálogo de informática.** Os 12 grupos são categorias de hardware (Memórias RAM, Monitores, Placas de Vídeo, Notebooks etc.) e o único produto é “Computador Alfa Gamer X1” ([DB-03](../evidencias/imagens/DB-03-grupos-catalogo-informatica.jpg)).
5. **Datas incompatíveis com as gravações.** Os vídeos FP-CT-31 e FP-CT-56 são de 15/11/2026. A última gravação em tabelas de conteúdo é de 06/08/2026 (`produtos`, `users`) e a última em `personal_access_tokens` é de 28/08/2026. O único `update_time` recente do servidor é em `clientes` (11/11/2026 17:54), anterior às gravações e fora dos módulos testados ([DB-02](../evidencias/imagens/DB-02-contagens-e-ultimas-gravacoes.jpg)).

A tabela `perguntas` existe, mas tem estrutura de FAQ (`pergunta`, `resposta`, `status`), está vazia e não possui vínculo com anamnese. Por isso, não serve para conferir FP-CT-31 (`/perguntas-anamnese`).

A semelhança entre o nome `alfa1` e o subdomínio `sifitalfa` não demonstra correspondência. O esquema aparenta pertencer a outro projeto, uma loja de informática, hospedada na mesma conta.

## Varredura completa (18/11/2026, 10:49–10:53)

O integrante informou que o banco nunca mudou. Então a conferência foi refeita cobrindo o esquema inteiro, e não apenas a estrutura. Foram usadas as consultas de varredura-completa.sql, todas somente leitura.

| Verificação | Resultado |
| --- | --- |
| Permissões (`SHOW GRANTS`) | `ALL PRIVILEGES` apenas em `u339572246_alfa1`; nenhum outro banco concedido |
| Bancos visíveis | `information_schema` e `u339572246_alfa1` |
| Objetos no esquema | 43 tabelas e 432 colunas; 0 views, 0 rotinas, 0 triggers e 0 eventos |
| Contagem exata de todas as tabelas | Total pequeno. Maiores: `cidades` 5.585, `personal_access_tokens` 402, `atributos` 170, `categorias` 29, `estados` 27, `migrations` 24, `artigos` 15, `grupos` 12. As demais têm entre 0 e 9 linhas |
| Busca de termos de academia no **conteúdo** de 207 colunas de texto ([DB-04](../evidencias/imagens/DB-04-busca-termos-academia-207-colunas.jpg)) | 4 ocorrências em 3 colunas, todas sem relação com academia (detalhe abaixo) |

A busca usou os termos plano, turma, anamnese, matrícula, treino, academia, aluno, exercício, crossfit, musculação, sifit, centrion, modalidade, mensalidade e personal. Ela cobriu todas as colunas de texto e JSON, exceto cidades, estados, tokens e sessões. Só foram contadas ocorrências; nenhum dado pessoal foi listado.

- `artigos.conteudo` (2): falsos positivos. A palavra encontrada é “personalização”, em artigos sobre cooktop e fogão.
- `users.nome` e `users.email` (1 registro): o único usuário administrativo usa o identificador “centrion”, nome da empresa desenvolvedora do SIFIT. Ele foi criado em 06/08/2026. O e-mail não foi registrado.

Contagem exata de cada tabela: artigos 15, atributos 170, authentication_methods 0, banners 9, cartoes 0, categoria_artigos 4, categorias 29, cidades 5585, clientes 1, combos 3, configuracoes 2, contatos 0, cupons 3, empresa 1, enderecos 0, estados 27, estoques 1, failed_jobs 0, grupos 12, identity_link_intents 0, imagens_produtos 0, instagram_accounts 0, instagram_posts 0, marcas 7, melhor_envio 0, migrations 24, newsletter 0, paginas 0, parceiros 4, parcelamento 1, password_reset_tokens 0, pedidos 0, perguntas 0, personal_access_tokens 402, produtos 1, produtos_3d 0, produtos_pedidos 0, security_events 1, sessions 0, social_accounts 0, social_auth_codes 0, users 1, valores_variacoes 1.

**Conclusão da varredura:** os dados do SIFIT (academia) não estão em nenhuma tabela, coluna ou conteúdo deste esquema. Os dados de teste mostrados nos vídeos de 15/11/2026 também não aparecem. O esquema pertence à mesma conta de hospedagem e tem um usuário “centrion”. A explicação compatível com os fatos é um outro projeto da Centrion (loja virtual “alfa”), hospedado na mesma conta. O banco do SIFIT deve estar em outro esquema, ao qual o usuário `u339572246_alfa1` não tem acesso. A confirmação depende do valor de `DB_DATABASE` configurado no servidor do `sifitalfa`.

## Comparação com o inventário de telas

O [inventário](inventario/01-acesso-e-principal.md) de 21/10/2026, levantado no navegador do Codex, registra 46 telas do SIFIT. Elas foram comparadas com as 43 tabelas do esquema.

| Tela do SIFIT (inventário) | Campos observados na interface | Tabela de mesmo nome em `alfa1` | Compatível? |
| --- | --- | --- | --- |
| RF07 Clientes | sexo, tipo sanguíneo, RG, código do leitor, Sempre Liberado, responsável, plano, personal | `clientes`: cpf, cnpj, tipo_pessoa, pagarme_id, parceiro_id, avatar | Não |
| RF16 Grupos | Mostrar Home, tipo de caixa Interno/Externo, descrição | `grupos`: urn, destaque1/2, imagem, ordem; dados “Placas de Vídeo”, “Notebooks” | Não |
| RF35 Produtos | tipo Venda/Pontuação, pontuação | `produtos`: ncm, ean, peso/medidas de embalagem, preco_pix, marca_id | Não |
| RF39 Categorias de Anamnese | ícone Bootstrap Icons, cor hexadecimal | `categorias`: grupo_id, urn, imagem | Não |
| RF40 Perguntas de Anamnese | número/ordem, tipo de resposta Sim/Não/Não Sei/Se Sim | `perguntas`: pergunta, resposta (FAQ) | Não |
| RF43 Configurações | abas Biometria, Avaliação, Aniversário, Integrações, Design | `configuracoes`: chave/valor com `ordenacao_padrao`, `parcelamento_minimo` | Não |
| RF25 Planos | cobrança, parcelas, Tem Personal, dependentes, benefícios | inexistente | Não |

Das 46 telas, 40 não têm nenhuma tabela de nome correspondente. Entre elas estão matrículas, presenças, check-in, avaliações, contas a pagar e a receber, fichas, exercícios, turmas, caixas, planos, contratos, colaboradores, fornecedores e anamnese. As 6 coincidências de nome da tabela acima (todas, exceto Planos, incluída como exemplo de tela sem tabela) não coincidem nos campos. A loja também tem entidades que nenhuma tela do SIFIT apresenta: pedidos com rastreio e frete, cupons, marcas, banners, Melhor Envio, Instagram e newsletter.

## Comparação com o site em funcionamento (18/11/2026)

O integrante fez login no navegador integrado do Claude. As telas foram apenas consultadas, sem criar, editar ou excluir nada.

| Tela em `sifit.centrion.com.br` | O que o site exibe | O que o esquema `alfa1` contém |
| --- | --- | --- |
| `/grupos` | 10 grupos de academia (#1 Treino Livre, #2 Treino Personal, #7 Grupo dos Marombas, #9 Grupo Manual SIFIT 2026…), com tipo de caixa Interno/Externo | 12 grupos de hardware (#7 Memórias RAM, #8 Monitores…) |
| `/produtos` | 7 produtos de Venda/Pontuação (#5 Notebook Gamer, #6 Nintendo Switch 2, #9 Garrafa…) | 1 produto (“Computador Alfa Gamer X1”) |
| `/perguntas-anamnese` | 6 perguntas ativas (#5 a #10, ex.: “Possui alguma lesao?”) | `perguntas` com 0 registros |
| `/planos` | 41 planos (31 ativos), com 9 alunos em planos | Nenhuma tabela de planos |

Os IDs, nomes e quantidades não coincidem em nenhuma das telas comparadas. **O site lê outro banco.**

### Backends identificados

O endereço do backend está embutido no JavaScript publicado por cada front-end:

| Front-end | Backend (API) | Build do app |
| --- | --- | --- |
| `sifit.centrion.com.br` (usado no login acima e na exploração histórica) | `backendsifit.centrion.com.br` | `app.b5fff9dc.js` |
| `sifitalfa.centrion.com.br` (domínio dos vídeos FP-CT-31 e FP-CT-56) | `backsifitalfa.centrion.com.br` | `app.b94f53e2.js` |

Os dois domínios usam **APIs e builds diferentes**. Por isso, os dados vistos em `sifit` não comprovam o que foi gravado em `sifitalfa`, e o contrário também vale. Para conferir os vídeos, é preciso o banco usado por `backsifitalfa`. Para conferir a exploração local, é preciso o banco usado por `backendsifit`. Nenhum dos dois é o esquema `u339572246_alfa1`, ou o banco de `sifitalfa` também teria entidades de academia.

## Teste de ligação site → banco (18/11/2026)

Teste ativo, autorizado pelo integrante em ambiente de teste. Foi criado um registro com nome único no site e, logo depois, procurado no banco.

| Passo | Horário local | Resultado |
| --- | --- | --- |
| 1. Criar grupo no site `sifit.centrion.com.br/grupos` | ~11:54 | Grupo **#12 `SONDA-QA-1118`** salvo; o total no site passou de 10 para 11 ([SONDA-01](../evidencias/imagens/SONDA-01-grupo-criado-no-site.jpg)) |
| 2. Consultar `grupos` e todas as colunas de texto de `u339572246_alfa1` | 11:55:36 | `grupos` com **12** registros (sem alteração) e maior `id` **43**; “SONDA” com **0** ocorrências ([SONDA-02](../evidencias/imagens/SONDA-02-grupo-ausente-no-banco.jpg)) |

**Conclusão:** o cadastro feito pelo site não chegou ao banco acessível pelo Workbench, e a numeração dos dois não coincide (#12 no site contra `id` máximo 43 no banco). A gravação do site `sifit` (API `backendsifit`) ocorre em outro banco. ### Tentativa de limpeza: exclusão falhou

Ao excluir o grupo #12 (lixeira → “Confirmar”), o site exibiu **“Erro ao deletar Grupo”** ([SONDA-03](../evidencias/imagens/SONDA-03-erro-ao-deletar-grupo.jpg)). A API respondeu **HTTP 500** em `POST https://backendsifit.centrion.com.br/api/deleta/grupo/1`. O cadastro, em `POST /api/adiciona/grupo/1`, havia respondido 201.

A falha ocorreu com um grupo recém-criado, sem planos ou outros vínculos, e reproduz o erro 500 registrado no FP-CT-57 (Grupos, `sifitalfa`, 15/11/2026). É um defeito reproduzível de exclusão de grupo nos dois domínios. Ele deve ser avaliado para o relatório de bugs. A exclusão não foi repetida, e o grupo **#12 `SONDA-QA-1118` continua no site `sifit`**.

O teste não foi repetido no `sifitalfa`, porque falta login nesse domínio. Pelas evidências anteriores, esperam-se o mesmo resultado: nenhum dos 14 valores digitados nos vídeos do `sifitalfa` existe no esquema.

## Banco correto: `u339572246_sifit_alfa` (18/11/2026, 12:06)

A conexão foi refeita com os dados dos slides 7 e 8: host `servidor MySQL da disciplina`, usuário e esquema `u339572246_sifit_alfa`. A senha foi digitada pelo integrante. A conexão antiga, para `alfa1`, foi removida do Workbench. Todas as consultas foram de leitura.

| Verificação | Resultado |
| --- | --- |
| Esquema | `u339572246_sifit_alfa`, com 129 tabelas de academia (`planos`, `turmas`, `perguntas_anamnese`, `pessoas`, `checkins` etc.) |
| Grupo-sonda criado no site `sifit` | **Encontrado:** `grupos.id = 12`, `SONDA-QA-1118`, `created_at` 2026-11-18 14:54:10 (servidor em UTC; 11:54 BRT). A tabela tem 11 grupos com `id` máximo 12, igual ao site ([SONDA-04](../evidencias/imagens/SONDA-04-grupo-presente-no-banco-sifit-alfa.jpg)) |
| 14 valores digitados nos vídeos do `sifitalfa` | Só valores genéricos aparecem: `enquetes` “teste”, de 2024 e 23/10/2026; `grupo_muscular` #2 “Pernas”, de 2021; `bandeiras` #33 e #34 “master”, de 16/11/2026 04:55 UTC. Os valores distintivos (“Como treinar pernas corretamente?”, “Treino de Pernas”, “turma test”, “testes_01”, “Alimentação2”, “qqq222”, “aaaa1”, “eeeaae”) **não existem** |
| Registros criados desde 01/10/2026 | 46 tabelas com registros recentes. Os horários não coincidem com as janelas dos vídeos de 15/11 (15:24–17:19 UTC) e 17/11 (21:07–23:06 UTC) |

**Conclusão:** `u339572246_sifit_alfa` é o banco do site `sifit.centrion.com.br`, e isso está provado pelo grupo-sonda. Os registros dos vídeos gravados no `sifitalfa` (API `backsifitalfa`) não foram encontrados nele. Há duas explicações: o `sifitalfa` usa outro banco, ou os registros foram excluídos ou alterados nos próprios vídeos (vários casos terminam em exclusão). Para decidir, falta uma sonda no `sifitalfa`, que requer login nesse domínio. Os “master” de 16/11 e os demais registros recentes podem ser de outros alunos testando o `sifit`.

### Investigação de rastros dos vídeos do `sifitalfa`

Hipótese avaliada: o banco é compartilhado por todos os alunos, e os registros dos vídeos podem ter sido excluídos ou alterados pelo próprio colega.

| Verificação | Resultado |
| --- | --- |
| Exclusão lógica (`deleted_at` ou similar) | Não existe em nenhuma tabela: exclusões removem o registro |
| Tabelas de rastro | `logs` (ação, tabela, id alterado), `auditoria_financeira`, `automacao_logs`, `log_login` e `perguntas_anamnese_old` |
| Qualquer `created_at`/`updated_at`/`executado_em` nas janelas dos vídeos: 22/10, 31/10, 15/11 e 17/11, em UTC e em BRT | **Nenhum registro.** Controle: a mesma consulta, com a janela de 18/11 14:50–14:58, encontra o grupo-sonda, então o método funciona |
| Tabelas que gravam só a data (`planos`, `logs`, `funcoes`) | Nenhum plano criado em 15/11 (FP-CT-56 cadastrou plano nesse dia). Em `logs`, as exclusões de contas são de 21/10, 24/10, 14/11 e 16/11, e **nenhuma é de 17/11**, quando FP-CT-68 e FP-CT-69 excluíram contas a receber e a pagar |
| `log_login` | Último registro em 2023; não é usada pelo sistema atual |

**Conclusão:** as operações gravadas nos vídeos do `sifitalfa` (cadastros com resposta 201, edições e exclusões de contas) não deixaram nenhum rastro em `u339572246_sifit_alfa`, nem em registros remanescentes, nem em datas de alteração, nem no log de exclusões. Uma exclusão posterior não explica a ausência: a tabela `logs` registraria as exclusões de contas, e as edições e inativações sem exclusão posterior deixariam `updated_at`. **O `sifitalfa` (API `backsifitalfa`) grava em outro banco.** Para conferir os 69 vídeos, é preciso o acesso a esse banco ou a confirmação do professor.

## Origem dos dados de acesso

A apresentação da disciplina (“AULA 7 - Apresentação Sistemas CentriumWeb”) informa o sistema `sifit.centrion.com.br` e o banco no host `servidor MySQL da disciplina`, usuário e esquema padrão `u339572246_alfa1`. A conexão conferida corresponde, portanto, ao banco indicado pelo professor. As evidências desta conferência mostram que esse esquema não recebe as gravações do site: estrutura de loja virtual, grupos e planos ausentes, valores dos vídeos ausentes e o grupo-sonda #12 ausente. **Causa identificada:** os slides 7 e 8 da mesma apresentação são prints do Workbench do professor. Neles, a conexão “CONEXAO SIFIT” usa usuário e esquema padrão **`u339572246_sifit_alfa`**, no mesmo host, e o navegador exibe tabelas de academia (`planos`, `plano_clientes`, `plano_sifit`, `perguntas_anamnese`, `pessoas`, `pontuacao`, `aulas_experimental` etc.). O slide 6, em texto, traz `u339572246_alfa1`, que é o esquema de loja virtual conferido aqui. A conexão do Workbench foi criada a partir do texto do slide 6; o banco do SIFIT é provavelmente `u339572246_sifit_alfa`. A conferência dos casos deve ser refeita com uma conexão para esse usuário e esquema, cuja senha deve ser informada pelo próprio integrante.

## Ambiente consultado

| Item | Valor observado |
| --- | --- |
| Conexão no Workbench | “SIFIT” (rótulo local) |
| Servidor | MariaDB 11.8.9 em hospedagem compartilhada (`servidor MySQL da disciplina`) |
| Esquema em uso | `u339572246_alfa1` |
| Esquemas visíveis ao usuário | `information_schema` e `u339572246_alfa1` (apenas) |
| Tabelas | 43 |
| Privilégios do usuário no esquema | Leitura e escrita completas, incluindo `ALTER`, `DROP`, `DELETE` e `UPDATE` |

Como o usuário enxerga um único esquema, o banco do SIFIT (`sifitalfa` ou `sifit`) não pode ser localizado por esta conexão. Ele pode estar em outro esquema, outro usuário ou outro servidor.

**Risco de segurança:** a conexão usada para conferência tem privilégios de alteração e exclusão. Para as próximas consultas, recomenda-se um usuário somente leitura.

## Tabelas e contagens

Contagem exata por `COUNT(*)` nas tabelas relevantes:

| Tabela | Registros | Última alteração (`updated_at`) |
| --- | ---: | --- |
| grupos | 12 | 2026-06-16 16:55:40 |
| categorias | 29 | 2026-08-04 18:51:41 |
| produtos | 1 | 2026-08-06 23:18:15 |
| perguntas | 0 | — |
| pedidos | 0 | — |
| artigos | 15 | 2026-07-27 20:57:08 |
| users | 1 | 2026-08-06 22:25:56 |
| personal_access_tokens | 402 | 2026-08-28 01:10:22 |

Tabelas do esquema: artigos, atributos, authentication_methods, banners, cartoes, categorias, categoria_artigos, cidades, clientes, combos, configuracoes, contatos, cupons, empresa, enderecos, estados, estoques, failed_jobs, grupos, identity_link_intents, imagens_produtos, instagram_accounts, instagram_posts, marcas, melhor_envio, migrations, newsletter, paginas, parceiros, parcelamento, password_reset_tokens, pedidos, perguntas, personal_access_tokens, produtos, produtos_3d, produtos_pedidos, security_events, sessions, social_accounts, social_auth_codes, users, valores_variacoes.

Não foram consultados nem registrados dados pessoais de `clientes`, `users` ou `contatos`, nem valores de `configuracoes` ou tokens.

## Casos conferidos

| Caso | Situação no esquema `alfa1` |
| --- | --- |
| FP-CT-31 — Perguntas (anamnese) | Não correlacionável: `perguntas` é FAQ de loja, vazia e sem vínculo com anamnese |
| FP-CT-56 — Planos | Não correlacionável: não existe tabela de planos |
| FP-CT-27 / FP-CT-44 — Produtos | Não correlacionável: `produtos` é catálogo de hardware com 1 registro de 06/08/2026, anterior aos testes |
| Demais 69 casos | Não correlacionáveis: as entidades testadas não existem no esquema |

**Nenhum dos 73 casos teve persistência comprovada ou refutada por esta conexão.** Os identificadores dos vídeos não foram extraídos para comparação: como o esquema não contém nenhuma entidade de academia, qualquer `SELECT` por esses identificadores voltaria vazio sem provar nada sobre o SIFIT.

## Consultas executadas

Todas as consultas foram de leitura. Os resultados acima foram copiados diretamente da grade do Workbench.

```sql
-- 1. Identificação do ambiente
SELECT DATABASE(), CURRENT_USER(), @@version, @@hostname, NOW(),
  (SELECT GROUP_CONCAT(schema_name) FROM information_schema.schemata),
  (SELECT COUNT(*) FROM information_schema.tables WHERE table_schema = DATABASE());

-- 2. Tabelas e estimativa de linhas
SELECT GROUP_CONCAT(CONCAT(table_name, ':', table_rows) ORDER BY table_name SEPARATOR ' | ')
FROM information_schema.tables WHERE table_schema = DATABASE();

-- 3. Migrations e busca por estrutura de academia
SELECT (SELECT GROUP_CONCAT(migration ORDER BY id SEPARATOR ' | ') FROM migrations),
  (SELECT GROUP_CONCAT(DISTINCT CONCAT(table_name, '.', column_name))
     FROM information_schema.columns WHERE table_schema = DATABASE()
     AND column_name REGEXP 'academ|plano|turma|anamn|matric|aluno|exerc|ficha|treino|caixa|fornec|colabor|empresa_id|tenant'),
  (SELECT GROUP_CONCAT(table_name) FROM information_schema.tables WHERE table_schema = DATABASE()
     AND table_name REGEXP 'plano|turma|anamn|matric|aluno|exerc|ficha|treino|caixa|fornec|colabor|enquete|avalia|despesa|conta');
-- Resultado: colunas apenas instagram_*.empresa_id e social_accounts.tenant_id; tabela apenas "contatos" (formulário de contato)

-- 4. Colunas das tabelas com nomes ambíguos
SELECT table_name, GROUP_CONCAT(column_name ORDER BY ordinal_position)
FROM information_schema.columns WHERE table_schema = DATABASE()
  AND table_name IN ('perguntas','grupos','categorias','produtos','clientes','users','empresa','configuracoes','contatos','pedidos')
GROUP BY table_name;

-- 5. Contagens e últimas gravações (DB-02)
SELECT 'grupos' tabela, COUNT(*) n, MAX(updated_at) ultima FROM grupos
UNION ALL SELECT 'categorias', COUNT(*), MAX(updated_at) FROM categorias
UNION ALL SELECT 'produtos',   COUNT(*), MAX(updated_at) FROM produtos
UNION ALL SELECT 'perguntas',  COUNT(*), MAX(updated_at) FROM perguntas
UNION ALL SELECT 'pedidos',    COUNT(*), MAX(updated_at) FROM pedidos
UNION ALL SELECT 'artigos',    COUNT(*), MAX(updated_at) FROM artigos;

-- 6. Última atualização registrada pelo servidor
SELECT GROUP_CONCAT(CONCAT(table_name, '=', update_time))
FROM information_schema.tables WHERE table_schema = DATABASE() AND update_time IS NOT NULL;
-- Resultado: clientes = 2026-11-11 17:54:04

-- 7. Resumo estrutural (DB-01)
SELECT DATABASE() esquema, COUNT(*) tabelas,
  SUM(table_name REGEXP 'plano|turma|anamn|matric|aluno|exerc|ficha|treino|caixa|fornec|colabor|enquete|avalia|despesa') academia,
  SUM(table_name IN ('produtos','pedidos','cupons','marcas','banners','combos','melhor_envio')) ecommerce
FROM information_schema.tables WHERE table_schema = DATABASE();
-- Resultado: u339572246_alfa1 | 43 | 0 | 7

-- 8. Catálogo (DB-03)
SELECT id, nome, status FROM grupos ORDER BY id;
```

## Capturas

| Arquivo | Conteúdo |
| --- | --- |
| [DB-01-esquema-sem-tabelas-academia.jpg](../evidencias/imagens/DB-01-esquema-sem-tabelas-academia.jpg) | Navegador do esquema e resumo: 43 tabelas, 0 de academia, 7 de e-commerce |
| [DB-02-contagens-e-ultimas-gravacoes.jpg](../evidencias/imagens/DB-02-contagens-e-ultimas-gravacoes.jpg) | Contagens e datas de última alteração, todas anteriores a 15/11/2026 |
| [DB-03-grupos-catalogo-informatica.jpg](../evidencias/imagens/DB-03-grupos-catalogo-informatica.jpg) | Grupos de catálogo de hardware |
| [DB-05-valores-dos-videos-nao-encontrados.jpg](../evidencias/imagens/DB-05-valores-dos-videos-nao-encontrados.jpg) | Busca de 14 valores digitados nos vídeos JAM: 0 ocorrências em 207 colunas |
| [DB-04-busca-termos-academia-207-colunas.jpg](../evidencias/imagens/DB-04-busca-termos-academia-207-colunas.jpg) | Busca de termos de academia no conteúdo: 207 colunas, 3 com ocorrência, todas sem relação com academia |

## Pendências

1. Obter acesso de leitura ao banco efetivamente usado por `sifitalfa.centrion.com.br`, confirmando esquema e servidor com o colega ou o responsável pelo ambiente.
2. Com o banco correto, extrair dos vídeos os identificadores dos registros (nomes cadastrados, datas e horários) e compará-los por `SELECT`, começando por FP-CT-31 e FP-CT-56.
3. Verificar se `sifitalfa` e `sifit` usam bancos distintos.
4. Registrar o relato do colega sobre “tabelas de comércio eletrônico” como explicado: a conexão aponta para um esquema de loja. A divergência não decorre da quantidade de produtos.
