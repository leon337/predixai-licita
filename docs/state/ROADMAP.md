# Roadmap — Predix Licita

## Sprint 0 — Governança e planejamento

### Objetivo

Criar a base oficial do projeto e aprovar o que será construído.

### Entregas

- instruções do projeto ChatGPT;
- modelo operacional;
- registro de agentes;
- catálogo de skills;
- visão do produto;
- usuários e jornadas;
- requisitos funcionais;
- requisitos não funcionais;
- escopo do MVP;
- modelo de dados inicial;
- arquitetura proposta;
- riscos;
- critérios de compatibilidade;
- estratégia de testes;
- classificação dos dados;
- decisão sobre autenticação, autorização e isolamento;
- requisitos mínimos de logs, retenção e segredos;
- backlog priorizado;
- roadmap aprovado.

### Gate

Nenhum código oficial antes da aprovação integral da Sprint 0.

Nenhuma persistência de dados privados antes da aprovação da linha de base de segurança.

## Sprint 1 — Coleta e pesquisa pública no PNCP

### Objetivo

Criar uma integração confiável, paginada e rastreável com a fonte oficial, inicialmente sem persistir dados empresariais privados.

### Entregas previstas

- cliente PNCP;
- normalização;
- paginação;
- tratamento de erros;
- pesquisa textual;
- proveniência;
- cache público somente se aprovado;
- testes da integração;
- interface inicial de resultados públicos;
- observabilidade mínima da coleta;
- limites e comportamento degradado documentados.

### Gate

- cobertura e paginação verificadas;
- falha da fonte distinguida de ausência de resultado;
- nenhuma informação privada persistida;
- revisão de segurança da integração aprovada.

## Sprint 2 — Controle de acesso, filtros, detalhes e oportunidades salvas

### Objetivo

Permitir triagem e organização privada das oportunidades encontradas com isolamento de dados aprovado.

### Pré-condições obrigatórias

- autenticação implementada e testada;
- autorização definida;
- isolamento por usuário ou organização validado;
- segredos protegidos;
- logs mínimos ativos;
- política de retenção aprovada.

### Entregas previstas

- autenticação e sessão;
- autorização e isolamento;
- filtros;
- página de detalhes;
- favoritos;
- estados de acompanhamento;
- notas;
- ordenação por prazo;
- histórico mínimo;
- testes de acesso e isolamento.

## Sprint 3 — Perfil empresarial e compatibilidade objetiva

### Objetivo

Comparar dados disponíveis com informações reais cadastradas pela empresa.

### Pré-condições obrigatórias

- modelo de dados privado aprovado;
- classificação de dados empresariais;
- controle de acesso validado;
- regras de retenção e exclusão definidas.

### Entregas previstas

- perfil empresarial;
- documentos e validade;
- capacidades;
- regras determinísticas;
- bloqueadores;
- informações ausentes;
- explicação da classificação;
- auditoria das alterações relevantes;
- testes das regras e permissões.

## Sprint 4 — Alertas e acompanhamento

### Objetivo

Reduzir perda de prazos e organizar o fluxo de decisão.

### Entregas previstas

- alertas internos;
- painel de prazos;
- histórico de mudanças;
- checklist por oportunidade;
- visão de preparação;
- preferências e limites de alertas;
- testes de confiabilidade temporal.

## Sprint 5 — Endurecimento, auditoria e validação

### Objetivo

Endurecer a segurança já existente e preparar o MVP para uso interno confiável.

### Entregas previstas

- revisão aprofundada de autenticação e autorização;
- revisão da proteção dos dados empresariais;
- logs e auditoria completos para o escopo;
- testes de segurança;
- testes de regressão;
- testes de recuperação e comportamento degradado;
- revisão independente;
- validação interna;
- documentação operacional;
- decisão de prontidão para uso interno.

A Sprint 5 não inaugura segurança. Ela valida e endurece controles implementados desde as etapas anteriores.

## Futuro — IA assistiva

Somente após validação do MVP determinístico:

- leitura assistida de editais;
- extração de requisitos com citações;
- resumo documental;
- comparação assistida;
- agente conversacional;
- novas fontes oficiais.

A IA não poderá substituir fonte oficial, regra objetiva ou revisão humana.