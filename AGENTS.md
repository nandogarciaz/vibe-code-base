# AGENTS.md — Contexto do projeto

Este arquivo é lido automaticamente pelos agentes antes de qualquer tarefa.
Mantenha atualizado sempre que a stack ou as convenções mudarem.

## Stack
- Linguagem: [ex: TypeScript / Node.js]
- Framework: [ex: Next.js, Express]
- Banco de dados: [ex: PostgreSQL]
- Testes: [ex: Vitest, Jest]

## Convenções
- Nomenclatura: camelCase para variáveis e funções, PascalCase para componentes/classes
- Commits: Conventional Commits (feat:, fix:, chore:, refactor:)
- Toda função pública tem tratamento de erro explícito
- Nenhum valor sensível hardcoded — sempre via .env

## Como rodar
- Testes: `npm test`
- Lint: `npm run lint`
- Build: `npm run build`

## Onde estão as coisas
- PRD geral: `docs/PRD.md`
- Decisões de arquitetura: `docs/adr/`
- Specs por feature: `docs/specs/{nome-da-feature}/spec.md`
- Agentes: `.agents/agents/`
- Skills: `.agents/skills/`

## Fluxo de entrega
Toda feature passa por três agentes em sequência: developer → tester → reviewer.
Nenhuma feature é considerada pronta sem aprovação do reviewer contra o spec.
