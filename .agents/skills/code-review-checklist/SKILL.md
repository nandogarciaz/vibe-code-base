---
name: code-review-checklist
description: Checklist de revisão de código do time — use sempre que revisar
  um PR ou validar código antes de aprovar. Cobre nomenclatura, tratamento
  de erro, cobertura de testes e aderência ao spec.
---

# Checklist de revisão de código

Ao revisar qualquer código, verifique nesta ordem:

1. **Nomenclatura** — segue o padrão do projeto descrito em AGENTS.md
   (camelCase para variáveis/funções, PascalCase para componentes/classes).
2. **Tratamento de erro** — toda função que pode falhar (chamada de API,
   leitura de arquivo, parsing) tem tratamento explícito, nunca falha
   silenciosa.
3. **Configuração** — não há valores hardcoded que deveriam vir de
   variável de ambiente ou arquivo de config.
4. **Testes** — existe teste cobrindo o caso feliz e pelo menos um caso de
   borda relevante para a lógica alterada.
5. **Aderência ao spec** — o código entrega exatamente o que está descrito
   em `docs/specs/{feature}/spec.md`, nem mais, nem menos.

## Como reportar problemas
Se algum item falhar, liste especificamente:
- arquivo e linha (ou trecho) onde o problema está
- qual item do checklist foi violado
- o que precisa mudar para resolver

Nunca aprove com pendência sem justificar por escrito por que a pendência
é aceitável.
