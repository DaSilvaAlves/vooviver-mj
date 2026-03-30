# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Landing page para Maria José Sequeira — consultora de viagens "Sair da Caixa Viagens" / VooViver. Site estático em produção: https://vooviver-mj.vercel.app

## Commands

```bash
npm run dev      # Dev server com hot reload
npm run build    # Build estático para /dist/
npm run preview  # Preview do build local
```

Deploy automático via Vercel a partir do branch main. Sem lint nem testes configurados.

## Tech Stack

- **Astro 6.1** (SSG estático, zero JS por defeito)
- **Tailwind CSS 4** (via @tailwindcss/vite — sem tailwind.config.js, tokens definidos com @theme em `src/styles/global.css`)
- **@astrojs/sitemap** — gera sitemap.xml automaticamente a partir de `site` no astro.config.mjs
- **Formsubmit.co** como backend do formulário de contacto (endpoint hardcoded em ContactForm.astro)
- **TypeScript** em modo strict (extends astro/tsconfigs/strict)
- **Node.js >=22.12.0**

## Architecture

Astro component-based com dados separados em JSON. Duas páginas:

- `src/pages/index.astro` — landing page principal, compõe todos os componentes seccionais
- `src/pages/guia.astro` — página standalone do lead magnet (eBook "Guia do Viajante"), com formulário Formsubmit.co inline e thank-you page em `src/pages/guia/obrigado.astro`
- `src/components/*.astro` — secções da landing page (Hero, Destinations, ContactForm, FAQ, EbookBanner, etc.)
- `src/data/*.json` — dados de destinos, FAQ e testemunhos (editáveis sem tocar em componentes)
- `src/layouts/Layout.astro` — layout master com meta tags, fonts, SEO e structured data (JSON-LD)
- `src/styles/global.css` — design tokens (@theme), classes utilitárias (.glass, .glow-gold, .btn-primary, etc.) e animações
- `src/assets/` — imagens optimizadas pelo Astro (destinos em .webp, foto da Maria em .png)

### Data flow

Os componentes `Destinations.astro`, `FAQ.astro` e `Testimonials.astro` importam directamente os JSON de `src/data/`. Para adicionar/editar destinos, FAQs ou testemunhos, editar apenas os JSON — os componentes iteram automaticamente.

## Design System

Tema dark premium com glassmorphism. Cores principais definidas em `src/styles/global.css` via `@theme`:

| Token | Hex | Uso |
|-------|-----|-----|
| --color-bg | #06060B | Fundo |
| --color-surface | #0D0D14 | Superfícies elevadas |
| --color-gold | #F5A623 | CTAs, destaques premium |
| --color-teal | #00D4AA | Sucesso, CTAs secundários |
| --color-coral | #FF6B6B | Urgência, badges |

Classes utilitárias glassmorphism: `.glass`, `.glass-strong`, `.glass-card` (definidas em global.css, não em Tailwind).

Fonts: Inter (body/headings) + JetBrains Mono (badges/números).

## Key Implementation Details

- **ContactForm.astro** é o componente mais complexo (~23 KB): formulário multi-step (3 passos) com validação client-side, progress bar e honeypot anti-spam. Submete via POST para Formsubmit.co → mjcsequeira@gmail.com
- **guia.astro** tem o seu próprio formulário Formsubmit.co (lead magnet), independente do ContactForm. Redirige para `/guia/obrigado` após submissão.
- **Scroll animations**: Intersection Observer em Layout.astro aplica classe `.visible` a elementos `.reveal`
- **SEO**: structured data JSON-LD (TravelAgency, TouristTrip, FAQPage) embutido no index.astro. Sitemap gerado pelo plugin @astrojs/sitemap.
- **vercel.json**: headers de segurança (X-Frame-Options, CSP-like) + cache imutável de 1 ano para assets estáticos (/_astro/*)
- **Sem .env em uso** — o .env.example referencia Formspree mas a implementação actual usa Formsubmit.co directamente
