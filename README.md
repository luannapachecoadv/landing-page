# Landing Page — Luanna Pacheco Advogada

Landing page institucional da Dra. Luanna Stéphany Gonçalves Pacheco, especialista em **Direito Médico e da Saúde** (OAB/GO 73.377).

## Stack

| Tecnologia | Versão | Função |
|---|---|---|
| [Vue 3](https://vuejs.org/) | ^3.5 | Framework de UI (Composition API + `<script setup>`) |
| [Vite](https://vite.dev/) | ^8.2 | Bundler e dev server |
| [Tailwind CSS v4](https://tailwindcss.com/) | ^4.3 | Estilização via `@theme` e utilitários |
| [Google Fonts](https://fonts.google.com/) | — | Playfair Display (display) + Inter (corpo) |
| [Material Symbols](https://fonts.google.com/icons) | — | Ícones via fonte |

## Estrutura

```
src/
├── assets/
│   ├── main.css              # Design tokens, base e utilitários globais
│   └── images/
│       ├── hero.jpg / .webp  # Imagem de fundo do hero
│       └── about-me.jpg / .webp  # Foto da advogada
├── components/
│   ├── AppHeader.vue         # Navegação fixa com logo e links
│   ├── HeroSection.vue       # Seção principal com CTA
│   ├── ServicesSection.vue   # Áreas de atuação
│   ├── AboutSection.vue      # Apresentação da advogada
│   ├── ContactSection.vue    # Formulário / links de contato
│   └── AppFooter.vue         # Rodapé
├── App.vue                   # Componente raiz
└── main.js                   # Instância Vue e montagem
```

## Desenvolvimento local

```bash
npm install
npm run dev
```

O servidor inicia em `http://localhost:5173`.

## Build

```bash
npm run build
```

O output é gerado em `dist/`. O `base` está configurado como `/landing-page/` no [`vite.config.js`](./vite.config.js) para compatibilidade com o GitHub Pages.

## Deploy

O deploy é automático via **GitHub Actions** (`.github/workflows/deploy.yml`).  
A cada push na branch `main`, o projeto é buildado e publicado no **GitHub Pages**.

## Personalização

### Número do WhatsApp
Em [`HeroSection.vue`](./src/components/HeroSection.vue) e [`ContactSection.vue`](./src/components/ContactSection.vue), localize a constante `whatsappUrl` e substitua pelo número completo com DDI:

```js
const whatsappUrl = 'https://wa.me/5562900000000'
```

### Imagens
Substitua os arquivos em `src/assets/images/` mantendo os mesmos nomes:
- `hero.jpg` + `hero.webp` — imagem de fundo do hero
- `about-me.jpg` + `about-me.webp` — foto da advogada