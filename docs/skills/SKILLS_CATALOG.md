# Catálogo Inicial de Skills — Predix Licita

## Regra geral

Skills são procedimentos repetíveis. Elas não representam pessoas e não concedem autonomia além das instruções do projeto.

Cada skill deve declarar:

- objetivo;
- quando usar;
- entradas obrigatórias;
- fontes autorizadas;
- sequência de execução;
- saídas;
- limites;
- critérios de falha;
- registro no GitHub e Linear.

## 1. reconstruir-estado-predix-licita

### Objetivo

Reconstruir o estado oficial antes de iniciar qualquer trabalho.

### Passos

1. ler `PROJECT_STATE.md`;
2. ler instruções e decisões vigentes;
3. consultar o projeto e a issue ativa no Linear;
4. verificar PRs e dependências;
5. apontar divergências;
6. informar etapa, objetivo, bloqueios e próximo gate.

### Saída

Relatório curto de estado, sem modificar recursos.

## 2. consultar-github-linear

### Objetivo

Localizar documentos, decisões, issues, dependências e evidências.

### Regra

GitHub representa o produto e sua memória; Linear representa o trabalho e o estado operacional.

### Saída

Referências verificáveis e lista de lacunas.

## 3. pesquisar-oportunidades-pncp

### Objetivo

Pesquisar oportunidades atuais na fonte oficial do PNCP.

### Regras

- utilizar apenas endpoints e páginas oficiais;
- registrar data e hora da coleta;
- preservar número de controle e URL oficial;
- não declarar compatibilidade confirmada sem edital;
- distinguir ausência de resultado de falha de pesquisa;
- suportar paginação e deduplicação quando implementada.

### Saída

Registros normalizados com proveniência.

## 4. transformar-requisitos-em-backlog

### Objetivo

Converter requisitos aprovados em trabalho executável no Linear.

### Passos

1. identificar requisito e decisão de origem;
2. dividir em entregas pequenas;
3. definir critérios de aceite;
4. registrar dependências e riscos;
5. separar descoberta, implementação, teste e revisão;
6. evitar tarefas vagas como “fazer sistema”.

### Saída

Backlog rastreável, sem iniciar implementação.

## 5. revisar-arquitetura

### Objetivo

Avaliar se a arquitetura proposta atende requisitos, riscos e limites.

### Critérios

- simplicidade do MVP;
- modularidade;
- segurança;
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

1. identificar versão e escopo;
2. conferir evidências;
3. executar ou revisar testes;
4. procurar regressões e riscos;
5. registrar achados;
6. emitir PASS, PASS COM RESSALVAS ou FAIL.

### Limite

Não corrigir silenciosamente durante revisão independente.

## 7. sincronizar-documentacao-tarefas

### Objetivo

Garantir que GitHub e Linear descrevem o mesmo estado.

### Verificações

- decisões registradas;
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

1. `reconstruir-estado-predix-licita`;
2. `consultar-github-linear`;
3. `transformar-requisitos-em-backlog`;
4. `validar-entrega`;
5. `sincronizar-documentacao-tarefas`;
6. `pesquisar-oportunidades-pncp`;
7. `revisar-arquitetura`.

As skills de pesquisa e arquitetura devem ser refinadas após a aprovação dos requisitos e da fonte técnica do PNCP.