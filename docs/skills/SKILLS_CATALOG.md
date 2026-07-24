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
| reconstruir-estado-predix-licita | PRONTA_PARA_CONFIGURAR | PR #1 aprovado e mesclado |
| consultar-github-linear | PRONTA_PARA_CONFIGURAR | acessos GitHub e Linear habilitados |
| pesquisar-oportunidades-pncp | BLOQUEADA | LEA-181 e definição dos requisitos de pesquisa |
| transformar-requisitos-em-backlog | PRONTA_PARA_CONFIGURAR | governança aprovada |
| revisar-arquitetura | BLOQUEADA | LEA-176, LEA-177, LEA-178 e LEA-179 |
| validar-entrega | PRONTA_PARA_CONFIGURAR | `QUALITY_GATES.md` aprovado |
| sincronizar-documentacao-tarefas | PRONTA_PARA_CONFIGURAR | governança aprovada |

Nenhuma skill marcada como `BLOQUEADA` deve ser criada como se estivesse pronta ou usada para produzir decisões finais.

## 1. reconstruir-estado-predix-licita

### Objetivo

Reconstruir o estado oficial antes de iniciar qualquer trabalho.

### Entradas

- repositório oficial;
- projeto Linear;
- issue ou solicitação atual.

### Passos

1. ler `PROJECT_STATE.md` na `main`;
2. ler instruções e decisões vigentes;
3. verificar PRs candidatos da etapa ativa;
4. consultar o projeto e a issue ativa no Linear;
5. verificar dependências;
6. apontar divergências;
7. informar etapa, objetivo, bloqueios e próximo gate.

### Saída

Relatório curto de estado, sem modificar recursos.

### Falha

Falha quando não consegue distinguir a versão oficial da candidata ou quando os acessos necessários não estão disponíveis.

## 2. consultar-github-linear

### Objetivo

Localizar documentos, decisões, issues, dependências e evidências.

### Regra

GitHub representa o produto e sua memória; Linear representa o trabalho e o estado operacional.

### Saída

Referências verificáveis e lista de lacunas.

### Limite

Não altera arquivos, PRs, projetos ou issues sem autorização explícita.

## 3. pesquisar-oportunidades-pncp

### Objetivo

Pesquisar oportunidades atuais na fonte oficial do PNCP.

### Status

`BLOQUEADA` até a conclusão da LEA-181 e aprovação dos requisitos aplicáveis.

### Regras

- utilizar apenas endpoints e páginas oficiais aprovados;
- registrar data e hora da coleta;
- preservar número de controle e URL oficial;
- não declarar compatibilidade confirmada sem edital;
- distinguir ausência de resultado de falha de pesquisa;
- suportar paginação e deduplicação conforme especificação aprovada;
- registrar limitações de cobertura.

### Saída

Registros normalizados com proveniência.

### Falha

Falha quando a fonte está indisponível, a cobertura é desconhecida ou a paginação não foi concluída conforme a especificação.

## 4. transformar-requisitos-em-backlog

### Objetivo

Converter requisitos aprovados em trabalho executável no Linear.

### Passos

1. identificar requisito e decisão de origem;
2. confirmar que o requisito foi aprovado;
3. dividir em entregas pequenas;
4. definir critérios de aceite;
5. registrar dependências e riscos;
6. separar descoberta, implementação, teste e revisão;
7. evitar tarefas vagas como “fazer sistema”.

### Saída

Backlog rastreável, sem iniciar implementação.

### Limite

Criar ou alterar issues exige autorização explícita para o conjunto de mudanças.

## 5. revisar-arquitetura

### Objetivo

Avaliar se a arquitetura proposta atende requisitos, riscos e limites.

### Status

`BLOQUEADA` até existir arquitetura candidata baseada em requisitos, dados e riscos aprovados.

### Critérios

- simplicidade do MVP;
- modularidade;
- segurança desde o início;
- autenticação e autorização antes da persistência de dados privados;
- rastreabilidade;
- custo;
- desempenho;
- operação degradada;
- testes;
- evolução futura sem IA para IA.

### Saída

Achados, alternativas e decisão pendente.

## 6. validar-entrega

### Objetivo

Verificar uma entrega contra requisitos e critérios de aceite.

### Passos

1. identificar versão, commit e escopo;
2. confirmar independência do revisor;
3. conferir evidências;
4. executar ou revisar testes;
5. procurar regressões e riscos;
6. classificar achados conforme `QUALITY_GATES.md`;
7. emitir PASS, PASS COM RESSALVAS ou FAIL.

### Limite

Não corrigir silenciosamente durante revisão independente. O agente que remediou a entrega não pode emitir o reteste final.

## 7. sincronizar-documentacao-tarefas

### Objetivo

Garantir que GitHub e Linear descrevem o mesmo estado.

### Verificações

- versão oficial versus candidata identificada;
- decisões e status registrados;
- issue correta;
- PR vinculado;
- status coerente;
- critérios de aceite atualizados;
- bloqueios explícitos;
- estado do projeto revisado;
- próximo passo identificável.

### Saída

Confirmação de sincronização ou lista de divergências.

## Ordem de criação recomendada na interface do ChatGPT

Após o merge da governança:

1. `reconstruir-estado-predix-licita`;
2. `consultar-github-linear`;
3. `transformar-requisitos-em-backlog`;
4. `validar-entrega`;
5. `sincronizar-documentacao-tarefas`.

Somente após desbloqueio:

6. `pesquisar-oportunidades-pncp`;
7. `revisar-arquitetura`.