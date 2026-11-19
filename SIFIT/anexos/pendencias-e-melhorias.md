# Pendências, investigações e melhorias

> Anexo da documentação SIFIT. Os identificadores originais (CT-RFxx-yy, FP-CT-xx, CT2-RFxx-yy) correspondem aos IDs C<RF>-CT<n> dos [cenários de teste](../Cenarios-de-testes/) conforme a [correspondência de IDs](correspondencia-de-ids.md).

Investigações identificadas na exploração. Sua avaliação está relacionada aos fluxos do plano de execução e evidências, com resultados e capturas associados ao fluxo correspondente.

## Investigações abertas

| ID | Observação | Por que ainda não é conclusão | Próxima ação |
| --- | --- | --- | --- |
| INV-001 | Inicialmente Sem Matrículas 6 versus modal 0; revisão mostrou 6/6 | Divergência não se repetiu; possível estado transitório, sem causa comprovada | Conciliar origem com banco; CT-RF02-02 |
| INV-002 | Desistências: total 2, lista vazia | Pode haver diferença entre agregado e consulta | Conciliar período, status, academia e dados |
| INV-003 | Personais: ícones apontam /visualizar-cliente/{id} | Pode haver identidade compartilhada ou destino incorreto | Confirmar vínculo colaborador/cliente |
| INV-004 | Check-in: Filtros não mostrou mudança ao clique | Comportamento previsto e reprodução pendentes | Reproduzir e confirmar o comportamento do filtro |
| INV-005 | Perfil de cliente: Editar objetivos não respondeu visivelmente | Fluxo e regra não confirmados | Repetir em massa isolada e conferir implementação/banco |
| INV-006 | Check-ins no perfil e tabela de presenças divergiram | Podem ser fontes distintas | Mapear eventos, presença, entrada/saída e datas |
| INV-007 | Configurações: dias de ausência com valor negativo preexistente | Não foi testado se o formulário aceita salvar negativo | Validar limite em ambiente isolado e origem no banco |
| INV-008 | Tipos de pagamento: ativos/uso em outros formulários a conciliar | Pode haver regra legada ou filtro diferente | Conferir status e elegibilidade em matrícula/contas |
| INV-009 | Contas a Pagar: totais zerados com linha pendente | Critérios dos indicadores não conhecidos | Comparar período, status, valores e consultas |
| INV-010 | Pagar.me: valores -- e gráfico preenchido | Integração e fonte não confirmadas | Validar configuração e sandbox |
| INV-011 | Produtos/Pontuação: botões sem nome na acessibilidade | Não comprova ausência visual de dados | Inspecionar visual e teclado; corrigir nomes acessíveis se confirmado |
| INV-012 | Cadastro de pergunta não mostrou categoria | Vínculo pode ser definido em outro fluxo | Verificar edição, montador e esquema |
| INV-013 | Login fornecido identifica Jair | Não comprova erro de identidade | Confirmar login → colaborador → academia no banco |
| INV-014 | + Modalidade sem dados não mostrou retorno visível | Pode ser ação de salvar do formulário inline | Confirmar validação e semântica em ambiente de teste |
| INV-015 | Configurar Aniversariantes mostrou critérios e preview de risco de evasão | Pode haver formulário genérico ou mapeamento incorreto | Confirmar regra e efeito no banco, sem executar envio real |

### Situação em 18/11/2026

| ID | Situação | Fundamento |
| --- | --- | --- |
| INV-001 | Encerrada, não confirmada | Em 18/11 a Página Inicial e a tela de Clientes exibiram o mesmo total de Sem Matrículas (21) |
| INV-002 | Limitação declarada | FP-CT-10 mostrou a tela vazia, mas sem conciliação com o indicador; não reexecutada |
| INV-003 | Limitação declarada | Não reexecutada |
| INV-004 | Limitação declarada | Não reexecutada; FP-CT-05 cobre o registro de check-in, não o botão Filtros |
| INV-005 | Relacionada ao BUG-020 | Perfil novo exibe objetivos fictícios; a edição de objetivos não foi reexecutada |
| INV-006 | Divergência confirmada, causa aberta | Presenças mostra 0 no período, e a tabela `checkins` tem 25 registros CONFIRMADO desde 20/10 (último em 18/11). Falta saber se Presenças usa outra fonte |
| INV-007 | Limitação declarada | Não reexecutada para evitar alterar configuração compartilhada |
| INV-008 | Limitação declarada | O formulário de matrícula lista 14 tipos de pagamento, incluindo nomes de teste |
| INV-009 | Limitação declarada | Não reexecutada |
| INV-010 | Limitação declarada | FP-CT-11 inconclusivo; o gateway não pode ser validado sem sandbox |
| INV-011 | Limitação declarada | Não reexecutada |
| INV-012 | Limitação declarada | Os vídeos de perguntas não mostram vínculo com categoria |
| INV-013 | **Resolvida, não é defeito** | No banco, o login `login da conta de testes` pertence ao funcionário 11, cuja pessoa se chama Jair |
| INV-014 | Limitação declarada | O SifitBox está desabilitado para a empresa (CT2-RF06-01) |
| INV-015 | Limitação declarada | Não reexecutada |
| INV-016 | **Nova** | Matrícula #246 cancelada, mas a conta a receber #1625 (R$ 52,00) continuou pendente. A regra esperada (estornar, cancelar ou manter) não está documentada |
| INV-017 | **Nova** | Após a falha de exclusão do cliente #440, a tela de alteração passou a abrir como cadastro (botão “Cadastrar Cliente”, sexo vazio), inclusive por “Alterar dados”. O mesmo ocorreu ao abrir `/alterar-cliente/440` pela URL. Reprodução isolada pendente |

“Limitação declarada” significa que o item não foi resolvido nesta entrega e fica registrado como limite da avaliação, sem conclusão de defeito.

## Funcionalidades declaradas indisponíveis

Em 18/11/2026, o módulo SifitBox estava desabilitado para a empresa da conta de testes (“Modulo SifitBox nao habilitado para esta empresa”), o que bloqueia RF06 nesse ambiente.

Na Central de Automações, Avaliações vencendo, Frequência em queda, Financeiro diário e Cobranças automáticas estão identificadas como **Em desenvolvimento**. Essas funcionalidades estão registradas como indisponíveis na versão observada.

O WhatsApp estava desconectado e sem configuração. Conectar, Testar, Enviar e Desconectar estavam desabilitados. Isso é uma pré-condição ausente, não prova de defeito.

## Funcionalidades ainda não executadas

- Editor posterior à criação de ficha e modelo de treino, com lista inicial vazia.
- Etapas de seleção de modelo/respostas/conclusão da anamnese.
- Detalhes de aula, reservas e capacidade após geração no Box.
- PDFs dos sete relatórios; comparação de avaliações e links de resultado. Os filtros foram inspecionados.
- Execução e histórico de automações; coerência da configuração de Aniversariantes.
- Persistência do vínculo de funções do colaborador; suas quatro abas foram inspecionadas.
- Ações de linhas ausentes em bandeiras, objetivos e modelos; moderação sem posts/denúncias de teste.
- Fluxos financeiros de abertura/fechamento/reabertura, baixas e integrações.
- Todos os efeitos persistentes de cadastrar, editar, cancelar e excluir.

Esses itens descrevem a etapa histórica local. O material recebido posteriormente contém execuções relacionadas, ainda pendentes de conciliação por operação, conforme a [consolidação da equipe](consolidacao-da-equipe.md). A cobertura planejada e os bloqueios de dados ou infraestrutura estão identificados no plano de execução.

## Melhorias propostas

| ID | Proposta | Evidência ou motivação |
| --- | --- | --- |
| MEL-001 | Arredondar apresentação do IMC sem perder precisão armazenada | Exemplo exibiu muitas casas decimais |
| MEL-002 | Melhorar contraste no SifitBox em tema escuro | Cartões brancos com textos muito claros na inspeção |
| MEL-003 | Ajustar layout da situação financeira do cliente | Texto de próximo vencimento/total quebrava excessivamente no viewport inspecionado |
| MEL-004 | Diferenciar carregamento, vazio e erro | Indicadores frequentemente aparecem zerados antes dos dados |
| MEL-005 | Mensagens claras em botões sem retorno e obrigatoriedade | Investigações de Filtros/Objetivos/Modalidade e variação na validação de login vazio |
| MEL-006 | Clarificar destino de Segurança e Preferências | Ambos apontam /configuracoes; não foi encontrado fluxo próprio de segurança nesse destino |

## Informações acadêmicas pendentes

Nome do aluno e integrantes; turma; professor; título oficial do projeto; cronograma e critérios de avaliação. Instituição: UniALFA. Curso: Sistemas para Internet.
