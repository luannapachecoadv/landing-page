# ADR-002: Estilização — Tailwind CSS v4

| Campo      | Valor                  |
|------------|------------------------|
| Data       | 2026-08-09             |
| Status     | Aceito                 |
| Decisores  | Equipe de desenvolvimento |

## Contexto

A versão anterior carregava o Tailwind via CDN com configuração inline no `<script>`, o que é inadequado para produção (sem tree-shaking, sem otimização de bundle).

## Decisão

Adotar **Tailwind CSS v4** instalado via npm com o plugin oficial `@tailwindcss/vite`.

## Justificativa

- Tailwind v4 introduz configuração de design tokens diretamente em CSS com a diretiva `@theme {}`, eliminando o arquivo `tailwind.config.js` para tokens.
- O plugin `@tailwindcss/vite` integra o Tailwind diretamente no pipeline de build do Vite, sem necessidade de PostCSS separado.
- O processo de build elimina classes CSS não utilizadas (PurgeCSS integrado), reduzindo drasticamente o tamanho do CSS final.
- O design system do projeto (`DESIGN.md`) mapeia diretamente para variáveis CSS no bloco `@theme`.

## Consequências

- O arquivo principal de estilos (`src/assets/main.css`) define todos os tokens de design via `@theme {}`.
- Não há `tailwind.config.js` para tokens — toda a configuração de design reside em CSS.
- Classes do Tailwind são usadas diretamente nos templates `.vue`.
