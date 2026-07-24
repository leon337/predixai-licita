# Gates de Qualidade e Revisão — Predix Licita

## Objetivo

Definir como entregas são avaliadas, como achados são classificados e quando um item pode avançar.

## Severidade dos achados

### CRITICAL

Falha que:

- permite ação não autorizada, exposição grave de dados ou comprometimento do ambiente;
- viola regra legal ou contratual evidente;
- permite uso de informação falsa como oficial;
- pode causar submissão, contratação, custo ou decisão irreversível sem autorização;
- compromete a integridade da fonte de verdade.

**Efeito:** bloqueia imediatamente merge, conclusão e deploy. Exige correção e reteste independente.

### HIGH

Falha que:

- contradiz requisito ou decisão central;
- permite iniciar implementação sem gate;
- produz classificação enganosa ou perda relevante de rastreabilidade;
- deixa dados privados sem autenticação, autorização ou isolamento adequado;
- torna o estado oficial inconsistente com o trabalho real;
- impede operação confiável de uma função essencial.

**Efeito:** bloqueia merge, conclusão da issue e avanço de fase. Exige correção e reteste independente.

### MEDIUM

Falha que:

- reduz clareza, manutenibilidade, explicabilidade ou cobertura;
- deixa dependência, exceção ou responsabilidade ambígua;
- causa comportamento inadequado sem comprometer imediatamente o objetivo central;
- aumenta risco operacional controlável.

**Efeito:** deve ser corrigida antes do encerramento da sprint, salvo aceitação explícita e registrada como ressalva com responsável e prazo.

### LOW

Falha de baixo impacto, como:

- inconsistência editorial;
- melhoria de nomenclatura;
- documentação complementar não essencial;
- ajuste de experiência sem perda funcional relevante.

**Efeito:** pode ser tratada posteriormente se registrada no backlog.

## Resultados de revisão

### PASS

- critérios de aceite atendidos;
- nenhuma divergência material;
- nenhum achado Critical, High ou Medium aberto;
- evidências suficientes;
- independência do revisor confirmada.

### PASS COM RESSALVAS

- nenhum achado Critical ou High aberto;
- apenas achados Medium aceitos explicitamente ou Low registrados;
- as ressalvas possuem responsável, prazo e issue;
- a entrega continua segura e utilizável dentro do escopo.

### FAIL

Ocorre quando:

- existe achado Critical ou High aberto;
- faltam evidências essenciais;
- critérios de aceite não foram atendidos;
- a versão revisada não é identificável;
- a independência exigida não existe e a revisão foi apresentada como final;
- o estado entre GitHub e Linear é materialmente incompatível.

## Independência

A revisão final deve ser feita por agente ou chat que não tenha:

- produzido a entrega;
- modificado os arquivos revisados;
- realizado a remediação;
- decidido sozinho o critério de aceite durante a execução.

Quando o mesmo agente fizer a análise, o resultado deve ser chamado de **revisão preliminar**, sem autoridade para aprovação final.

## Evidências mínimas

Toda revisão deve registrar:

- repositório e PR;
- branch e commit revisado;
- issue correspondente;
- documentos e arquivos consultados;
- critérios de aceite;
- testes ou verificações executadas;
- achados com localização e reprodução;
- resultado;
- bloqueios e próximo passo.

## Gate documental

Um PR documental pode ser mesclado somente quando:

1. seu escopo estiver claramente descrito;
2. o estado candidato estiver sincronizado com o Linear;
3. achados Critical e High estiverem resolvidos;
4. reteste independente tiver sido executado;
5. houver PASS ou PASS COM RESSALVAS válido;
6. o usuário autorizar o merge.

## Gate de implementação

Código pode começar somente quando:

1. a Sprint 0 estiver concluída;
2. requisitos e arquitetura estiverem oficializados na `main`;
3. riscos e estratégia de testes estiverem aprovados;
4. a issue de implementação tiver escopo e critérios de aceite;
5. o usuário autorizar o início.

## Gate de persistência privada

Nenhum dado privado pode ser persistido antes de:

1. autenticação definida;
2. autorização definida;
3. isolamento validado;
4. dados classificados;
5. retenção e exclusão definidas;
6. segredos protegidos;
7. testes de acesso aprovados.

## Gate de deploy

Deploy de preview ou produção exige:

- issue autorizada;
- ambiente e custos aprovados;
- controles de acesso adequados;
- testes verdes;
- evidências de build e runtime;
- revisão de segurança proporcional ao ambiente;
- aprovação humana.