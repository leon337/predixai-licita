# Estado Oficial do Projeto — Predix Licita

**Data-base:** 24/07/2026  
**Fase:** Sprint 0 — Governança e planejamento  
**Status geral:** remediação da governança em andamento  
**Implementação:** não autorizada  
**Versão documental vigente na main:** inicialização mínima do repositório  
**Versão candidata:** PR #1 — governança e escopo da Sprint 0

## Objetivo da etapa atual

Corrigir os achados da revisão crítica preliminar do PR #1, obter revisão independente final e oficializar a base de governança antes de iniciar a definição detalhada do produto.

## Concluído nesta etapa

- repositório exclusivo criado e inicializado;
- separação oficial do Predix Negócio Digital aprovada pelo usuário;
- experimento anterior encerrado;
- projeto Linear atualizado para o repositório correto;
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
- remediação dos oito achados iniciada.

## Backlog ativo da Sprint 0

- LEA-173 — governança e aprovação do PR #1;
- LEA-174 — configuração manual dos agentes e skills;
- LEA-175 — usuários e jornadas;
- LEA-176 — requisitos funcionais e não funcionais;
- LEA-177 — modelo de dados;
- LEA-178 — arquitetura;
- LEA-179 — riscos, segurança e privacidade;
- LEA-180 — critérios objetivos de compatibilidade;
- LEA-181 — estudo oficial da API e dados do PNCP;
- LEA-182 — estratégia de testes;
- LEA-183 — consolidação do planejamento e gate de implementação.

## Em elaboração

- remediação e reteste independente do PR #1;
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

- o PR #1 não pode ser mesclado antes da revisão independente final;
- nenhuma implementação deve começar antes da aprovação integral da Sprint 0;
- Supabase e Vercel ainda não estão autorizados para este repositório;
- nenhuma persistência privada pode existir antes do gate de autenticação, autorização e isolamento;
- regras técnicas e limites reais da API do PNCP ainda precisam ser estudados na LEA-181;
- o perfil empresarial oficial da Predix ainda precisa ser documentado e auditado;
- skills de PNCP e arquitetura permanecem bloqueadas por dependências.

## Gate atual

1. concluir a remediação dos achados da revisão preliminar;
2. solicitar revisão independente a outro agente/chat;
3. obter PASS ou PASS COM RESSALVAS sem achados críticos ou altos abertos;
4. obter aprovação humana;
5. mesclar o PR #1 na `main`;
6. sincronizar LEA-173 e LEA-165.

## Próximo item após o gate

Configurar os agentes e skills liberados pela LEA-174 e iniciar a LEA-175 — usuários e jornadas do MVP.

## Fontes oficiais e candidatas

- GitHub oficial: `leon337/predixai-licita` na `main`;
- candidato atual: PR #1, branch `docs/sprint-0-governanca`;
- Linear: projeto `Predix Licita — Radar e Análise`;
- tarefa-mãe: LEA-165;
- governança: LEA-173.