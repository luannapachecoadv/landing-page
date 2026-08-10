# ADR-001: Framework — Vue.js 3 com Vite

| Campo      | Valor                  |
|------------|------------------------|
| Data       | 2026-08-09             |
| Status     | Aceito                 |
| Decisores  | Equipe de desenvolvimento |

## Contexto

A landing page existente era um único arquivo `index.html` gerado pelo Google Stitch, sem componentização ou processo de build. A manutenção e evolução do código exigem uma estrutura mais organizada.

## Decisão

Adotar **Vue.js 3** como framework de UI com **Vite** como bundler.

## Justificativa

- Vue 3 com Composition API oferece componentes reutilizáveis e escalabilidade sem overhead de SSR desnecessário para um site estático.
- Vite proporciona HMR instantâneo em desenvolvimento e build de produção otimizado.
- O output do Vite é HTML/CSS/JS estático puro, compatível com GitHub Pages sem nenhuma infraestrutura de servidor.
- Ecossistema maduro com excelente suporte a TypeScript (caso necessário no futuro).

## Consequências

- O projeto passa a ter um passo de build (`npm run build`) antes do deploy.
- O arquivo `index.html` original é substituído pelo entry point do Vite.
- Cada seção da página vira um componente `.vue` isolado.
