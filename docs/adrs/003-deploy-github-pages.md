# ADR-003: Deploy — GitHub Pages via GitHub Actions

| Campo      | Valor                  |
|------------|------------------------|
| Data       | 2026-08-09             |
| Status     | Aceito                 |
| Decisores  | Equipe de desenvolvimento |

## Contexto

O site precisa ser hospedado de forma gratuita e confiável, com deploy automático a cada push na branch principal.

## Decisão

Usar **GitHub Pages** como plataforma de hospedagem, com deploy automatizado via **GitHub Actions** usando `actions/deploy-pages`.

## Justificativa

- GitHub Pages é gratuito para repositórios públicos, sem custos de infraestrutura.
- A integração com GitHub Actions permite CI/CD nativo sem ferramentas externas.
- `actions/deploy-pages` é a solução oficial e mantida pelo GitHub para deploy de sites estáticos.
- O output do Vite (`dist/`) é compatível diretamente com GitHub Pages.
- Suporte a domínio customizado caso necessário no futuro.

## Consequências

- O repositório precisa ter GitHub Pages habilitado com source configurado como **GitHub Actions**.
- A `base` do Vite é configurada como `/landing-page/` (nome do repositório).
- A branch `gh-pages` não é utilizada; o deploy é feito diretamente pelo workflow para o ambiente `github-pages`.
- Todo push para `main` dispara um build e deploy automático.
