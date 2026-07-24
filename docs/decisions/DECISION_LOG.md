# Registro de Decisões — Predix Licita

## Como interpretar este registro

Cada decisão possui dois estados distintos:

- **Aprovação de negócio:** indica se Leo aprovou a direção na conversa.
- **Estado documental:** indica se a decisão ainda está proposta em PR ou já foi oficializada por merge na `main`.

Enquanto este arquivo estiver apenas no PR #1, as decisões abaixo estão aprovadas pelo usuário, mas **pendentes de oficialização documental**.

Campos obrigatórios para novas decisões:

- identificador;
- título;
- data;
- aprovador;
- motivação;
- decisão;
- consequências;
- aprovação de negócio;
- estado documental;
- substitui ou é substituída por, quando aplicável.

---

## DEC-001 — Repositório exclusivo

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** separar o Predix Licita de projetos sem relação e preservar uma memória própria.  
**Decisão:** `leon337/predixai-licita` é a sede exclusiva do projeto.  
**Consequências:** nenhum outro repositório pode receber código ou documentação oficial do produto.  
**Aprovação de negócio:** aprovada  
**Estado documental:** candidata no PR #1; oficial após merge na `main`  
**Substituição:** não se aplica.

## DEC-002 — Separação do Predix Negócio Digital

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** desenvolver os dois objetivos em paralelo sem mistura de escopo, memória ou execução.  
**Decisão:** Predix Licita e Predix Negócio Digital serão tratados em projetos, chats, repositórios e backlogs separados.  
**Consequências:** uma integração comercial futura não permite misturar governança ou implementação.  
**Aprovação de negócio:** aprovada  
**Estado documental:** candidata no PR #1; oficial após merge na `main`  
**Substituição:** não se aplica.

## DEC-003 — Primeiro usuário

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** validar utilidade e confiabilidade internamente antes de oferecer o sistema ao mercado.  
**Decisão:** a Predix AI BR será a primeira usuária.  
**Consequências:** o produto somente será ofertado a terceiros depois de validação interna documentada.  
**Aprovação de negócio:** aprovada  
**Estado documental:** candidata no PR #1; oficial após merge na `main`  
**Substituição:** não se aplica.

## DEC-004 — MVP sem inteligência artificial

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** reduzir complexidade e validar primeiro coleta, filtros, organização e regras objetivas.  
**Decisão:** a primeira versão utilizará fontes oficiais, filtros explícitos e regras determinísticas.  
**Consequências:** IA generativa, Grok, leitura automática e agente conversacional ficam fora do MVP.  
**Aprovação de negócio:** aprovada  
**Estado documental:** candidata no PR #1; oficial após merge na `main`  
**Substituição:** não se aplica.

## DEC-005 — Planejamento antes do código

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** evitar repetição da implementação prematura ocorrida no experimento anterior.  
**Decisão:** nenhum código oficial será criado antes da aprovação dos documentos e gates da Sprint 0.  
**Consequências:** implementações prematuras devem ser interrompidas e registradas como experimentos.  
**Aprovação de negócio:** aprovada  
**Estado documental:** candidata no PR #1; oficial após merge na `main`  
**Substituição:** não se aplica.

## DEC-006 — GitHub, Linear, Supabase e Vercel

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** definir papéis claros para memória, gestão, infraestrutura e deploy sem antecipar decisão arquitetural.  
**Decisão:** GitHub será a memória oficial e Linear o gerenciamento. Supabase e Vercel são tecnologias candidatas para banco/backend e deploy, mas sua configuração depende da arquitetura aprovada.  
**Consequências:** não criar recursos, custos ou ambientes antes do gate técnico.  
**Aprovação de negócio:** parcialmente aprovada; GitHub e Linear confirmados, Supabase e Vercel condicionados  
**Estado documental:** candidata no PR #1; oficial após merge na `main`  
**Substituição:** poderá ser complementada por ADRs de arquitetura.

## DEC-007 — Equipe inicial

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** iniciar com uma equipe pequena, clara e controlável antes de ampliar os agentes.  
**Decisão:** iniciar com cinco papéis: Orquestrador; Produto e Licitações; Arquitetura e Engenharia; Segurança e Qualidade; Revisor Independente.  
**Consequências:** novos agentes exigem necessidade comprovada e decisão registrada.  
**Aprovação de negócio:** aprovada  
**Estado documental:** candidata no PR #1; oficial após merge na `main`  
**Substituição:** não se aplica.

## DEC-008 — Experimento anterior

**Data:** 24/07/2026  
**Aprovador:** Leo  
**Motivação:** o experimento interpretou o comando incorretamente, implementou antes do planejamento e utilizou repositório inadequado.  
**Decisão:** o MVP experimental criado em `predixai-operations` foi descartado como base oficial.  
**Consequências:** não copiar código, arquitetura, score, banco ou decisões técnicas daquele experimento sem nova análise e aprovação.  
**Aprovação de negócio:** encerramento aprovado  
**Estado documental:** candidata no PR #1; registro histórico oficial após merge na `main`  
**Substituição:** substitui qualquer pressuposto de continuidade do PR #16.

## DEC-009 — Segurança antes da persistência

**Data:** 24/07/2026  
**Aprovador:** pendente de confirmação final no merge do PR #1  
**Motivação:** perfil empresarial, documentos, notas e favoritos não podem ser persistidos antes de autenticação, autorização, isolamento e classificação de dados.  
**Decisão proposta:** a linha de base de segurança será definida na Sprint 0 e implementada antes de qualquer persistência privada; a Sprint 5 será de endurecimento e validação final.  
**Consequências:** funcionalidades privadas das Sprints 2 e 3 ficam bloqueadas pelo gate de segurança.  
**Aprovação de negócio:** proposta de remediação  
**Estado documental:** candidata no PR #1  
**Substituição:** corrige a interpretação anterior de segurança concentrada apenas na Sprint 5.