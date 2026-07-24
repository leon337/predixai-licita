# Catálogo Inicial de Skills — Predix Licita

## Regra geral

Skills são procedimentos repetíveis. Elas não representam pessoas e não concedem autonomia além das instruções do projeto.

Cada skill deve declarar:

- objetivo;
- status;
- quando usar;
- entradas obrigatórias;
- fontes autorizadas;
- dependências;
- sequência de execução;
- saídas;
- limites;
- critérios de falha;
- registro no GitHub e Linear.

A configuração ou execução de uma skill não concede permissão adicional. Escritas no GitHub, Linear, Supabase, Vercel ou em qualquer recurso externo continuam sujeitas à issue autorizada, às ferramentas realmente disponíveis e à aprovação exigida pelas instruções do projeto.

## Estados permitidos

- `ESPECIFICADA`: conceito documentado, ainda não criado na interface;
- `BLOQUEADA`: depende de requisitos, fonte ou decisão ainda pendente;
- `PRONTA_PARA_CONFIGURAR`: pode ser criada manualmente no ChatGPT;
- `CONFIGURADA`: criada na interface e testada;
- `VALIDADA`: executada com evidência e revisão;
- `SUSPENSA`: não deve ser utilizada.

## Matriz de status e dependências

| Skill | Status atual | Dependências principais |
|---|---|---|
| reconstruir-estado-predix-licita | ESPECIFICADA | PR #1 aprovado e mesclado |
| consultar-github-linear | ESPECIFICADA | PR #1 aprovado e mesclado; acessos GitHub e Linear habilitados |
| pesquisar-oportunidades-pncp | BLOQUEADA | LEA-181 concluída; requisitos de pesquisa aprovados |
| transformar-requisitos-em-backlog | ESPECIFICADA | governança e requisitos aprovados |
| revisar-arquitetura | BLOQUEADA | LEA-176, LEA-177, LEA-178 e LEA-179 concluídas com documentos candidatos disponíveis |
| validar-entrega | ESPECIFICADA | `QUALITY_GATES.md` oficializado; critérios de aceite e versão identificados |
| sincronizar-documentacao-tarefas | ESPECIFICADA | governança aprovada e mesclada |

Nenhuma skill marcada como `BLOQUEADA` deve ser criada como se estivesse pronta ou usada para produzir decisões finais. As skills `ESPECIFICADA` somente passam a `PRONTA_PARA_CONFIGURAR` quando todas as dependências estiverem satisfeitas e o estado for atualizado no GitHub e no Linear.

## 1. reconstruir-estado-predix-licita

### Objetivo

Reconstruir o estado oficial e candidato antes de iniciar qualquer trabalho.

### Status

`ESPECIFICADA` até o PR #1 ser aprovado e mesclado.

### Quando usar

- no início de uma nova conversa ou etapa;
- antes de responder sobre estado, próximo item, bloqueios ou autorização;
- quando houver suspeita de divergência entre GitHub, Linear e conversa.

### Entradas obrigatórias

- repositório oficial;
- projeto Linear;
- issue ou solicitação atual;
- PR candidato vinculado, quando existir.

### Fontes autorizadas

- documentos vigentes na `main`;
- PRs candidatos da etapa ativa;
- projeto, issues, relações e comentários no Linear;
- decisões aprovadas pelo usuário ainda pendentes de oficialização, quando explicitamente registradas.

### Dependências

- acesso de leitura ao GitHub e Linear;
- ordem de consulta oficial disponível;
- identificação da issue atual.

### Sequência de execução

1. ler `PROJECT_STATE.md` na `main`;
2. ler instruções e decisões vigentes;
3. identificar documentos candidatos e declarar que ainda não são oficiais;
4. verificar PRs candidatos da etapa ativa;
5. consultar o projeto, a issue atual e suas dependências no Linear;
6. comparar estado, versões, bloqueios e próximo gate;
7. apontar divergências sem corrigi-las silenciosamente;
8. informar etapa, objetivo, bloqueios e próximo passo.

### Saída

Relatório de estado com versão oficial, versão candidata, issue ativa, bloqueios, divergências e próximo gate.

### Limites

- não modifica recursos por padrão;
- não promove candidato à condição de oficial;
- não presume que uma autorização antiga abrange uma nova etapa.

### Critérios de falha

Falha quando não consegue distinguir a versão oficial da candidata, identificar a issue autorizada, acessar uma fonte obrigatória ou reconciliar uma divergência material.

### Registro no GitHub e Linear

Registrar divergências materiais na issue correspondente e, quando aplicável, no PR candidato. Atualizações de arquivos, estados ou relações exigem autorização explícita.

## 2. consultar-github-linear

### Objetivo

Localizar documentos, decisões, issues, dependências, comentários e evidências verificáveis.

### Status

`ESPECIFICADA` até a governança ser oficializada e os acessos serem confirmados.

### Quando usar

- quando uma resposta depender do conteúdo real do repositório ou backlog;
- para reconstruir histórico e dependências;
- para verificar sincronização e evidências.

### Entradas obrigatórias

- repositório, arquivo, PR, commit ou termo pesquisado;
- projeto, issue ou intervalo de issues no Linear;
- objetivo da consulta.

### Fontes autorizadas

- repositório oficial e seus PRs;
- projeto oficial no Linear;
- anexos e links explicitamente vinculados às issues consultadas.

### Dependências

- ferramentas GitHub e Linear habilitadas;
- permissão de leitura;
- identificadores suficientes para localizar as fontes.

### Sequência de execução

1. delimitar a pergunta e as entidades necessárias;
2. consultar primeiro a fonte oficial aplicável;
3. abrir documentos, PRs, commits, issues e relações relevantes;
4. diferenciar conteúdo vigente, candidato e histórico;
5. cruzar as evidências;
6. retornar referências verificáveis e lacunas.

### Saída

Referências verificáveis, síntese baseada nas fontes e lista de lacunas ou divergências.

### Limites

- não altera arquivos, PRs, projetos ou issues sem autorização explícita;
- não usa resumo anterior como substituto da consulta direta;
- não inventa conteúdo ausente.

### Critérios de falha

Falha quando a fonte obrigatória não está acessível, o identificador é insuficiente, a versão não pode ser confirmada ou as evidências são contraditórias sem regra de resolução.

### Registro no GitHub e Linear

Citar arquivos, commits, PRs e issues consultados na entrega. Lacunas materiais devem ser registradas na issue ativa ou no PR quando houver autorização para comentar.

## 3. pesquisar-oportunidades-pncp

### Objetivo

Pesquisar oportunidades atuais na fonte oficial do PNCP com proveniência e cobertura verificáveis.

### Status

`BLOQUEADA` até a conclusão da LEA-181 e aprovação dos requisitos aplicáveis.

### Quando usar

Somente depois do desbloqueio formal, para pesquisas previstas em issue autorizada e baseadas na especificação aprovada da fonte.

### Entradas obrigatórias

- termos incluídos e excluídos;
- filtros autorizados;
- intervalo temporal;
- critérios de paginação e cobertura;
- issue de execução.

### Fontes autorizadas

- documentação oficial do PNCP aprovada na LEA-181;
- endpoints e páginas oficiais aprovados;
- requisitos de pesquisa oficializados no repositório.

### Dependências

- LEA-181 concluída;
- requisitos de pesquisa aprovados;
- endpoints, paginação, limites e comportamento de erro documentados;
- acesso à fonte oficial.

### Sequência de execução

1. validar entradas e filtros;
2. confirmar endpoints e limites aprovados;
3. executar consulta somente leitura;
4. completar paginação e deduplicação conforme especificação;
5. registrar data e hora da coleta;
6. preservar número de controle e URL oficial;
7. distinguir ausência de resultado de falha da fonte;
8. registrar limitações de cobertura.

### Saída

Registros normalizados com proveniência, horário de coleta, cobertura, filtros usados, URLs oficiais e limitações.

### Limites

- não declarar compatibilidade confirmada sem requisitos documentados;
- não interpretar edital como parecer jurídico;
- não persistir dados privados;
- não enviar proposta nem executar ação de participação;
- não usar endpoints não aprovados.

### Critérios de falha

Falha quando a fonte está indisponível, a cobertura é desconhecida, a paginação não é concluída, a deduplicação não é verificável ou os requisitos de pesquisa permanecem bloqueados.

### Registro no GitHub e Linear

Registrar parâmetros, evidências, limitações e resultado na issue de pesquisa. Artefatos permanentes somente podem ser adicionados ao GitHub em branch e PR autorizados.

## 4. transformar-requisitos-em-backlog

### Objetivo

Converter requisitos aprovados em trabalho pequeno, testável e rastreável no Linear.

### Status

`ESPECIFICADA` até a governança e os requisitos aplicáveis serem aprovados.

### Quando usar

Depois que requisitos numerados e decisões de origem estiverem aprovados e houver autorização para criar ou alterar um conjunto delimitado de issues.

### Entradas obrigatórias

- requisitos aprovados;
- decisões de origem;
- escopo da etapa;
- critérios de aceite;
- riscos e dependências conhecidos;
- autorização de escrita no Linear.

### Fontes autorizadas

- documentos oficializados na `main`;
- PR candidato expressamente aprovado para planejamento;
- decisões registradas no `DECISION_LOG.md`;
- projeto e backlog oficial no Linear.

### Dependências

- governança aprovada;
- requisitos aplicáveis aprovados;
- escopo e autorização de escrita definidos.

### Sequência de execução

1. identificar requisito e decisão de origem;
2. confirmar aprovação e estado documental;
3. dividir em entregas pequenas;
4. definir critérios de aceite verificáveis;
5. registrar dependências e riscos;
6. separar descoberta, implementação, teste, segurança e revisão;
7. excluir trabalho fora do MVP;
8. criar ou propor issues rastreáveis.

### Saída

Backlog priorizado e rastreável, sem iniciar implementação.

### Limites

- criar ou alterar issues exige autorização explícita para o conjunto de mudanças;
- não muda escopo aprovado;
- não inclui IA no MVP;
- não transforma hipótese em requisito aprovado.

### Critérios de falha

Falha quando o requisito não está aprovado, não possui origem, não pode ser testado, depende de decisão ausente ou a autorização de escrita não cobre a alteração.

### Registro no GitHub e Linear

Cada issue deve vincular requisito, decisão, dependências e critérios de aceite. Mudanças estruturais devem ser refletidas no estado candidato do GitHub em fluxo autorizado.

## 5. revisar-arquitetura

### Objetivo

Avaliar se uma arquitetura candidata atende requisitos, dados, riscos, segurança, testes e limites do MVP.

### Status

`BLOQUEADA` até existir arquitetura candidata baseada em requisitos, dados e riscos aprovados.

### Quando usar

Após a produção da arquitetura candidata na LEA-178 e somente quando as dependências documentais necessárias estiverem disponíveis.

### Entradas obrigatórias

- arquitetura candidata e versão revisada;
- requisitos funcionais e não funcionais;
- modelo de dados;
- registro de riscos;
- decisões tecnológicas propostas;
- critérios de aceite e custos conhecidos.

### Fontes autorizadas

- documentos das LEA-176, LEA-177, LEA-178 e LEA-179;
- `QUALITY_GATES.md`;
- ADRs e PR candidato correspondente;
- documentação técnica oficial dos fornecedores avaliados.

### Dependências

- LEA-176 concluída;
- LEA-177 concluída;
- arquitetura candidata da LEA-178 disponível;
- LEA-179 concluída;
- versão e critérios de aceite identificados.

### Sequência de execução

1. confirmar versão, escopo e independência aplicável;
2. mapear requisitos para componentes e decisões;
3. revisar fronteiras, dados, integrações e operação degradada;
4. verificar autenticação e autorização antes da persistência privada;
5. avaliar segurança, rastreabilidade, custo, desempenho e testes;
6. identificar lacunas, alternativas e riscos;
7. classificar achados conforme os gates aplicáveis;
8. registrar decisão pendente de aprovação humana.

### Saída

Achados classificados, alternativas, riscos residuais e recomendação pendente de decisão humana.

### Limites

- não implementa código;
- não configura banco, Supabase, Vercel ou produção;
- não seleciona tecnologia apenas por preferência;
- não aprova a própria arquitetura quando participou de sua produção.

### Critérios de falha

Falha quando faltam requisitos, modelo de dados, riscos, versão identificável, evidências de custo/segurança ou independência exigida.

### Registro no GitHub e Linear

Publicar revisão no PR da arquitetura e registrar resultado, achados, bloqueios e reteste na issue correspondente.

## 6. validar-entrega

### Objetivo

Verificar uma entrega contra requisitos, critérios de aceite e gates de qualidade.

### Status

`ESPECIFICADA` até `QUALITY_GATES.md` ser oficializado e existir entrega identificável.

### Quando usar

Em revisões preliminares, revisões independentes e retestes autorizados de documentos, código, infraestrutura ou operação.

### Entradas obrigatórias

- repositório, PR, branch e commit;
- issue correspondente;
- requisitos e critérios de aceite;
- evidências e testes;
- declaração de independência do revisor.

### Fontes autorizadas

- documentos e código da versão revisada;
- requisitos e decisões vigentes;
- GitHub e Linear oficiais;
- evidências e testes vinculados à entrega;
- fontes externas oficiais exigidas pelo escopo.

### Dependências

- versão identificável;
- critérios de aceite definidos;
- evidências acessíveis;
- independência válida quando a revisão for final.

### Sequência de execução

1. identificar versão, commit e escopo;
2. confirmar independência do revisor;
3. reconstruir o estado e consultar requisitos;
4. conferir evidências e testes;
5. procurar contradições, regressões, riscos e lacunas;
6. classificar achados conforme `QUALITY_GATES.md`;
7. emitir PASS, PASS COM RESSALVAS ou FAIL;
8. registrar bloqueios, correção necessária e reteste.

### Saída

Relatório de revisão com versão, verificações, achados, severidades, resultado, bloqueios e próximo passo.

### Limites

- não corrigir silenciosamente durante revisão independente;
- o agente que produziu ou remediou a entrega não pode emitir o reteste final;
- não aprovar sem evidências;
- não reduzir severidade para liberar prazo.

### Critérios de falha

Falha quando a versão não é identificável, faltam evidências essenciais, a independência exigida não existe, há divergência material não resolvida ou os critérios de aceite não podem ser verificados.

### Registro no GitHub e Linear

Publicar revisão ou comentário no PR e registrar resultado e achados na issue. O status da issue deve refletir a execução da revisão sem concluir automaticamente a entrega revisada.

## 7. sincronizar-documentacao-tarefas

### Objetivo

Garantir que GitHub e Linear descrevem o mesmo estado, versões, decisões, bloqueios e próximo gate.

### Status

`ESPECIFICADA` até a governança ser aprovada e mesclada.

### Quando usar

- após mudança relevante em PR, issue, decisão ou gate;
- antes de solicitar revisão;
- após revisão, remediação, reteste, aprovação ou merge;
- antes de informar o estado do projeto ao usuário.

### Entradas obrigatórias

- `PROJECT_STATE.md` vigente e candidato;
- PR, branch e commit ativos;
- projeto e issues correspondentes no Linear;
- decisões e resultado de revisão aplicáveis.

### Fontes autorizadas

- repositório oficial e PRs candidatos;
- projeto oficial no Linear;
- `DECISION_LOG.md` e `QUALITY_GATES.md`;
- comentários e evidências vinculados à etapa.

### Dependências

- acesso ao GitHub e Linear;
- entidades e versões identificadas;
- autorização explícita para qualquer escrita necessária.

### Sequência de execução

1. identificar versão oficial e candidata;
2. comparar fase, status, issue ativa e dependências;
3. verificar PR, commit, resultado de revisão e bloqueios;
4. conferir decisões e próximo gate;
5. listar divergências antes de alterar recursos;
6. aplicar somente as atualizações autorizadas;
7. reler GitHub e Linear após a escrita;
8. registrar confirmação ou divergências remanescentes.

### Saída

Confirmação de sincronização ou lista de divergências com localização, impacto e correção necessária.

### Limites

- não altera recursos sem autorização explícita;
- não promove PR candidato à memória oficial;
- não conclui issue estrutural, marca PR como pronto ou faz merge sem autorização específica;
- não oculta divergência não resolvida.

### Critérios de falha

Falha quando uma das fontes não pode ser consultada, a versão não é identificável, a escrita autorizada não é suficiente ou permanece divergência material entre GitHub e Linear.

### Registro no GitHub e Linear

Registrar o resultado da sincronização na issue ativa e, quando aplicável, no PR. Informar exatamente quais arquivos, metadados, issues ou estados foram alterados.

## Ordem de criação recomendada na interface do ChatGPT

Após o merge da governança e atualização dos estados para `PRONTA_PARA_CONFIGURAR`:

1. `reconstruir-estado-predix-licita`;
2. `consultar-github-linear`;
3. `transformar-requisitos-em-backlog`;
4. `validar-entrega`;
5. `sincronizar-documentacao-tarefas`.

Somente após desbloqueio formal:

6. `pesquisar-oportunidades-pncp`;
7. `revisar-arquitetura`.
