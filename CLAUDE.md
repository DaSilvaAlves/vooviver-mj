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

Deploy automático via Vercel a partir do branch main.

## Tech Stack

- **Astro 6.1** (SSG estático, zero JS por defeito)
- **Tailwind CSS 4** (via @tailwindcss/vite — sem tailwind.config.js, tokens definidos com @theme em `src/styles/global.css`)
- **Formsubmit.co** como backend do formulário de contacto (endpoint hardcoded em ContactForm.astro)
- **TypeScript** em modo strict (extends astro/tsconfigs/strict)
- **Node.js >=22.12.0**

## Architecture

Astro component-based com dados separados em JSON:

- `src/pages/index.astro` — página única que compõe todos os componentes
- `src/components/*.astro` — secções da landing page (Hero, Destinations, ContactForm, FAQ, etc.)
- `src/data/*.json` — dados de destinos, FAQ e testemunhos (editáveis sem tocar em componentes)
- `src/layouts/Layout.astro` — layout master com meta tags, fonts, SEO e structured data (JSON-LD)
- `src/styles/global.css` — design tokens (@theme), classes utilitárias (.glass, .glow-gold, .btn-primary, etc.) e animações
- `src/assets/` — imagens optimizadas pelo Astro (destinos em .webp, foto da Maria em .png)

## Design System

Tema dark premium com glassmorphism. Cores principais definidas em `src/styles/global.css` via `@theme`:

| Token | Hex | Uso |
|-------|-----|-----|
| --color-bg | #06060B | Fundo |
| --color-surface | #0D0D14 | Superfícies elevadas |
| --color-gold | #F5A623 | CTAs, destaques premium |
| --color-teal | #00D4AA | Sucesso, CTAs secundários |
| --color-coral | #FF6B6B | Urgência, badges |

Fonts: Inter (body/headings) + JetBrains Mono (badges/números).

## Key Implementation Details

- **ContactForm.astro** é o componente mais complexo (~23 KB): formulário multi-step (3 passos) com validação client-side, progress bar e honeypot anti-spam. Submete via POST para Formsubmit.co → mjcsequeira@gmail.com
- **Scroll animations**: Intersection Observer em Layout.astro aplica classe `.visible` a elementos `.reveal`
- **SEO**: structured data JSON-LD (TravelAgency, TouristTrip, FAQPage) embutido no Layout.astro
- **vercel.json**: headers de segurança + cache imutável de 1 ano para assets estáticos (/_astro/*)
- **Sem .env em uso** — o .env.example referencia Formspree mas a implementação actual usa Formsubmit.co directamente
