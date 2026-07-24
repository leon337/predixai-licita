# PredixAI BR Licita

Plataforma nacional de pesquisa, organização e acompanhamento de oportunidades públicas, criada inicialmente para atender às necessidades internas da Predix AI BR.

## Estado atual

**Sprint 0 — Governança e planejamento.**

Ainda não há implementação oficial do produto. O MVP será definido, revisado e aprovado antes da geração de código.

## Objetivo inicial

Permitir que a Predix AI BR encontre oportunidades publicadas em fontes oficiais, começando pelo PNCP, aplique filtros objetivos, acompanhe prazos e compare os dados disponíveis com seu perfil empresarial.

## Regra do MVP

A primeira versão não utilizará inteligência artificial. Pesquisa, filtros, classificação e bloqueadores serão baseados em regras determinísticas e dados rastreáveis.

## Fontes de verdade

- **GitHub:** documentação, decisões, arquitetura, código, testes e histórico.
- **Linear:** backlog, roadmap, responsáveis, dependências e estado das entregas.
- **Projeto ChatGPT PredixAI BR Licita:** coordenação, discussão e uso dos agentes e skills.
- **Supabase e Vercel:** somente após aprovação da arquitetura e da etapa de implementação.

## Estrutura planejada

```text
docs/
├── governance/
├── product/
├── architecture/
├── decisions/
├── state/
├── agents/
└── skills/
```

## Roadmap macro

1. Sprint 0 — Governança, planejamento e linha de base de segurança
2. Sprint 1 — Coleta e pesquisa pública no PNCP, sem persistência de dados privados
3. Sprint 2 — Controle de acesso, filtros, detalhes e oportunidades salvas, somente após o gate de persistência privada
4. Sprint 3 — Perfil empresarial e compatibilidade objetiva, com isolamento e retenção aprovados
5. Sprint 4 — Alertas e acompanhamento
6. Sprint 5 — Endurecimento, auditoria e validação final dos controles existentes
7. Futuro — Leitura e análise de editais com IA, mediante decisão específica

A Sprint 5 não inaugura segurança. Autenticação, autorização, isolamento, classificação de dados, retenção e exclusão, proteção de segredos e testes de acesso devem existir antes de qualquer funcionalidade privada.

## Histórico importante

Uma implementação experimental anterior foi descartada por ter sido criada prematuramente e em outro repositório. Nenhum código daquele experimento constitui base oficial deste projeto.
