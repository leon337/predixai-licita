# Estado Oficial do Projeto — Predix Licita

**Data-base:** 24/07/2026  
**Fase:** Sprint 0 — Governança e planejamento  
**Status geral:** LEA-186 concluída com FAIL; achados HIGH remediados na LEA-187; aguardando novo reteste independente na LEA-188  
**Implementação:** não autorizada  
**Versão documental vigente na main:** inicialização mínima do repositório  
**Versão candidata:** PR #1 — governança e escopo da Sprint 0, branch `docs/sprint-0-governanca`

## Objetivo da etapa atual

Submeter a versão candidata remediada na LEA-187 a um novo reteste independente na LEA-188 antes de qualquer aprovação humana ou merge.

## Concluído nesta etapa

- repositório exclusivo criado e inicializado;
- separação oficial do Predix Negócio Digital aprovada pelo usuário;
- experimento anterior encerrado e mantido somente como histórico descartado;
- projeto Linear vinculado ao repositório correto;
- LEA-165 definida como tarefa-mãe da Sprint 0;
- backlog detalhado LEA-173 a LEA-183 criado;
- PR #1 aberto como candidato documental;
- instruções permanentes propostas;
- equipe virtual inicial proposta;
- catálogo inicial de skills proposto;
- visão do produto proposta;
- escopo do MVP sem IA proposto;
- roadmap macro proposto;
- decisões iniciais registradas como candidatas;
- revisão crítica preliminar executada com resultado FAIL;
- remediação dos oito achados preliminares executada;
- LEA-184 executada como primeiro reteste independente, com resultado FAIL;
- LEA-185 concluída como remediação separada de GOV-RI-001, GOV-RI-002 e GOV-RI-003;
- LEA-186 executada como segundo reteste independente, com resultado FAIL;
- GOV-RI-002 e GOV-RI-003 confirmados como fechados na LEA-186;
- GOV-RI-001 reaberto como HIGH por referências residuais ao gate anterior;
- GOV-RI-004 registrado como HIGH por divergência entre o README oficial e o roadmap de segurança;
- LEA-187 criada para remediação separada de GOV-RI-001 e GOV-RI-004;
- referências residuais à LEA-185 removidas do estado e do gate atual;
- `README.md` sincronizado com segurança desde a Sprint 0, controle de acesso antes da persistência privada e Sprint 5 como endurecimento;
- descrição do projeto Linear sincronizada com o resultado da LEA-186 e o novo gate;
- LEA-188 criada para novo reteste independente por agente/chat que não participou da LEA-186 nem da LEA-187.

## Backlog ativo da Sprint 0

- LEA-173 — governança e aprovação do PR #1 — em andamento;
- LEA-174 — configuração manual dos agentes e skills — bloqueada pela governança;
- LEA-175 — usuários e jornadas — bloqueada pela governança;
- LEA-176 — requisitos funcionais e não funcionais — backlog;
- LEA-177 — modelo de dados — backlog;
- LEA-178 — arquitetura — backlog;
- LEA-179 — riscos, segurança e privacidade — backlog;
- LEA-180 — critérios objetivos de compatibilidade — backlog;
- LEA-181 — estudo oficial da API e dados do PNCP — bloqueada pela governança;
- LEA-182 — estratégia de testes — backlog;
- LEA-183 — consolidação do planejamento e gate de implementação — bloqueada pelas demais entregas da Sprint 0;
- LEA-184 — primeiro reteste independente do PR #1 — concluída com FAIL;
- LEA-185 — primeira remediação dos achados de reteste — concluída;
- LEA-186 — segundo reteste independente do PR #1 — concluída com FAIL;
- LEA-187 — remediação de GOV-RI-001 e GOV-RI-004 — concluída;
- LEA-188 — novo reteste independente do PR #1 — próxima atividade de gate.

## Em elaboração

- novo reteste independente da versão remediada do PR #1 na LEA-188;
- configuração manual dos GPTs e skills após o merge da governança;
- usuários e jornadas;
- requisitos funcionais;
- requisitos não funcionais;
- modelo de dados;
- arquitetura;
- riscos;
- critérios detalhados de compatibilidade;
- estudo técnico oficial do PNCP;
- estratégia de testes;
- backlog de implementação das Sprints 1 a 5.

## Bloqueios

- o PR #1 deve permanecer Draft até o novo reteste independente;
- o PR #1 não pode ser mesclado antes de PASS ou PASS COM RESSALVAS válido e aprovação humana;
- LEA-173 não pode ser concluída antes do gate documental;
- nenhuma implementação deve começar antes da aprovação integral da Sprint 0;
- Supabase e Vercel ainda não estão autorizados para este repositório;
- nenhuma persistência privada pode existir antes de autenticação, autorização, isolamento, classificação de dados, retenção e exclusão, proteção de segredos e testes de acesso aprovados;
- regras técnicas e limites reais da API do PNCP ainda precisam ser estudados na LEA-181;
- o perfil empresarial oficial da Predix ainda precisa ser documentado e auditado;
- as skills de PNCP e arquitetura permanecem bloqueadas por dependências;
- o agente/chat que executou a LEA-186 e a remediação da LEA-187 não pode emitir o resultado independente da LEA-188.

## Gate atual

1. confirmar a conclusão e as evidências da LEA-187;
2. confirmar o novo HEAD do PR #1;
3. executar a LEA-188 em outro agente/chat independente;
4. obter PASS ou PASS COM RESSALVAS sem achados Critical ou High abertos;
5. obter aprovação humana;
6. mesclar o PR #1 na `main` somente após autorização explícita;
7. sincronizar LEA-173, LEA-165, GitHub e Linear após o merge.

## Próximo item após o gate

Configurar os agentes e skills liberados pela LEA-174 e iniciar a LEA-175 — usuários e jornadas do MVP.

## Fontes oficiais e candidatas

- GitHub oficial: `leon337/predixai-licita` na `main`;
- candidato atual: PR #1, branch `docs/sprint-0-governanca`;
- Linear: projeto `Predix Licita — Radar e Análise`;
- tarefa-mãe: LEA-165;
- governança: LEA-173;
- primeiro reteste independente: LEA-184 — concluído com FAIL;
- primeira remediação: LEA-185 — concluída;
- segundo reteste independente: LEA-186 — concluído com FAIL;
- remediação dos achados HIGH: LEA-187 — concluída;
- próximo reteste independente: LEA-188.
