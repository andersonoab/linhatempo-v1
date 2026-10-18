# Calendários Sonova — transferência de atividades entre meses

## Atualizar o projeto

Substitua o **index.html** na mesma pasta em que você usa o projeto. A aba **Calendário** mantém suas atividades anteriores. O segundo calendário, **Calendário RH · Excel**, continua separado, editável por um clique e com os ajustes preservados ao reler a planilha.

Todos os cartões do dia agora são exibidos. Não existe limite de três atividades nem botão “+ atividades”. O botão **+** no fim do dia serve somente para criar uma atividade nova.

## Levar as atividades para os meses seguintes

O **Calendário RH · Excel** agora utiliza a mesma forma de transferência do calendário original, com seu próprio mês ativo.

Exemplo: levar as atividades de outubro para novembro.

1. Abra **Calendário RH · Excel** e avance até **novembro** pelas setas.
2. Clique em **Assumir mês** e confirme. Novembro passa a ser o mês ativo do RH.
3. Volte para **outubro** pelas setas.
4. Clique em **Migrar 216 p/ ativo** (o número acompanha as atividades daquele mês) e confirme. Você será levado a novembro com as atividades transferidas.
5. Clique em qualquer cartão para ajustar data, situação ou responsável e salve, como já faz.

Repita o mesmo procedimento para dezembro e os meses seguintes. As atividades de data única são **movidas**, preservando o dia do mês e a duração. Se o dia não existir, será usado o último dia do mês de destino. Atividades concluídas voltam para **Pendente**, com a data de conclusão limpa. Os demais estados são mantidos. A competência acompanha o mês de destino; os IDs e as observações são preservados.

A migração considera todas as atividades de data única do mês de origem, inclusive ocultas e fora dos filtros, como no calendário original. As atividades que já estavam no destino permanecem. Itens sem data precisam receber uma data antes de serem transferidos.

Atividades com **Recorrente mensal** já aparecem nos meses seguintes. Ao assumir um novo mês, as recorrentes concluídas voltam a pendentes. O mês ativo também avança automaticamente ao abrir o aplicativo em um mês posterior ao salvo, como no calendário original. Os calendários possuem controles e dados separados.

A transferência não cria uma cópia no mês de origem. Se precisar guardar uma fotografia antes de transferir, use **Backup RH**. As novas datas ficam salvas no navegador e são preservadas ao reler o mesmo Excel; para levá-las à planilha, use **Exportar visão RH**. A edição no HTML não grava automaticamente no arquivo original.

O fechamento continua sinalizado no dia **22** de cada mês. As datas transferidas ainda podem ser ajustadas por clique ou arraste.

## Excel já planejado

Abra **Controle_Faturamento_RH_Planejado.xlsx** e use a aba **RH_Execucao**. As 225 atividades possuem datas propostas, mantendo os responsáveis, situações, evidências e os SLAs originais.

A equipe pode ajustar diretamente a coluna **Prazo**, escolher a **Situação** nas listas e registrar conclusão/observação conforme executar. As datas iniciais representam planejamento, não conclusão confirmada.

O ciclo da folha foi organizado assim:

| Etapa | Data-modelo de outubro/2026 |
|---|---|
| Entradas, validações e preparação | Até dia 19 |
| Integrações de ponto, benefícios e variáveis | Até dia 20 |
| Cálculo preliminar, conferências e líquido final | Dia 21 |
| Aprovações finais e marco de fechamento | **Dia 22** |
| Banco, contabilização e conciliações | Após o fechamento |
| Pagamento-modelo | Último dia útil do mês |

O dia 22 também aparece identificado no calendário RH como **Fechamento da folha**.

## Controles do planejamento na mesma aba

Os controles ficam à direita da tabela, nas colunas **N e O**:

- **O2:** mês do planejamento, inicialmente outubro/2026.
- **O3:** dia de fechamento da folha, inicialmente **22**.
- **O4:** dia-modelo de admissão, inicialmente **19**.
- **O5:** dia-modelo de desligamento, inicialmente **13**.
- **O6:** data-modelo para aprovação de férias futuras, inicialmente 23/11/2026.

As datas das 225 linhas iniciais usam fórmulas ligadas a esses controles. A coluna **Critério do planejamento** explica o racional de cada proposta, sem alterar a coluna **Prazo de referência** original. Para uma exceção, substitua a fórmula da célula Prazo pela data real.

As fórmulas antecipam datas que caiam em sábado ou domingo. Feriados, horários de corte, alçadas, vencimentos oficiais e condições de cada evento devem ser ajustados à realidade da operação. O fechamento permanece no dia numérico escolhido em O3.

## Distribuição inicial

- **216 atividades em outubro/2026**.
- **3 preparações em setembro/2026**, que precisam anteceder o início da competência.
- **3 etapas de projetos em novembro/2026**.
- **3 etapas de projetos em dezembro/2026**.

As 225 atividades são consultadas navegando entre os meses do calendário. Admissões, desligamentos, férias e chamados utilizam cenários/reservas de agenda. Ajuste as datas aos casos reais e aos SLAs aplicáveis. As fases de projeto são um cronograma-modelo, sem confirmar go-live ou conclusão de qualquer projeto real. As atividades diárias/semanais mantêm sua frequência original; a data preenchida é um ponto de controle, não uma expansão automática em várias ocorrências.

As etapas de encargos foram posicionadas como conferência e preparação internas. Essas datas não substituem a validação de competência e vencimentos oficiais. Marcos antigos permanecem no SLA original, inclusive o registro de NR-1 de julho/2026.

## Importar e editar

1. Salve o Excel atualizado.
2. No HTML, abra **Calendário RH · Excel** e clique em **Ler Excel de faturamento**.
3. Selecione o arquivo planejado. Todos os itens com data daquele mês serão exibidos integralmente nos dias correspondentes.
4. Clique no cartão para editar data, situação, responsável, observação, cor ou recorrência e salve. Também é possível arrastar para outro dia.

A releitura não apaga seus ajustes locais. Se quiser substituir a data que você já mudou no calendário pela nova proposta do Excel, abra essa atividade e use **Restaurar dados do Excel**. As demais atividades recebem as datas novas normalmente, pelo ID execução.

As edições feitas no HTML ficam no navegador e no **Backup RH**. Elas não gravam automaticamente no Excel. O botão **Exportar visão RH** gera uma planilha com a visão filtrada. Para preservar todos os campos e o histórico de ajustes, use **Backup RH**; o backup JSON das abas originais continua separado.

## Histórico e preservação

Para uma execução nova, utilize uma linha livre com ID próprio. Não substitua o registro do ciclo anterior. Se quiser manter uma fotografia do planejamento antes de mudar o mês em O2, preserve o ciclo concluído em novas linhas ou em uma cópia do arquivo.

As 18 abas originais do arquivo de faturamento foram preservadas integralmente. A edição ficou restrita à aba RH_Execucao e à ampliação de sua tabela para incluir o critério das datas. Não houve redistribuição de responsáveis nem alteração de situações para simular execução.

Foram verificadas as 225 datas calculadas, o recálculo dos controles e a leitura no navegador. Também foram conferidos a exibição integral de todos os cartões, a edição por clique, a preservação dos ajustes na releitura e o isolamento do calendário original. A validação no Excel desktop/Online da Sonova depende do ambiente corporativo e não foi executada aqui.

A transferência mensal foi validada com 216 atividades reais do planejamento, cancelamento, releitura, persistência, edição, recorrência, meses curtos, ano bissexto e preservação do calendário original.
