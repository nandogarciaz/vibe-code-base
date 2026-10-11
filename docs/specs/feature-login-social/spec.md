# Spec — Login social

## Objetivo
Permitir que o usuário se autentique usando conta Google ou GitHub, sem
precisar criar senha.

## Comportamento esperado
1. Usuário clica em "Entrar com Google" ou "Entrar com GitHub".
2. É redirecionado ao provedor, autoriza o acesso, e retorna autenticado.
3. Se for o primeiro login, uma conta é criada automaticamente com os
   dados básicos do provedor (nome, e-mail, foto).
4. Se já existir uma conta com o mesmo e-mail, o login social é vinculado
   a ela, não cria conta duplicada.

## Casos de borda
- Usuário cancela a autorização no provedor → volta para tela de login
  com mensagem neutra, sem erro técnico exposto.
- E-mail do provedor já está associado a uma conta criada por senha →
  vincula automaticamente, sem pedir confirmação extra.
- Provedor não retorna e-mail (alguns permitem ocultar) → bloqueia o
  cadastro e informa que é necessário e-mail público para login social.

## Critérios de aceite
- [ ] Login via Google funciona ponta a ponta em ambiente de teste
- [ ] Login via GitHub funciona ponta a ponta em ambiente de teste
- [ ] Conta duplicada não é criada quando e-mail já existe
- [ ] Cancelamento no provedor não gera erro não tratado
- [ ] Ausência de e-mail do provedor é tratada com mensagem clara

## Fora de escopo
- Login social com outros provedores (Facebook, Apple) — feature futura
- Desvinculação de conta social pelo usuário — feature futura
