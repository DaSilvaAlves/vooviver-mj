# PRD: Landing Page Maria Serqueira — VooViver Viagens

**Projecto:** vooviver-mj
**Cliente:** Maria Serqueira, Consultora VooViver
**Data:** 28/03/2026
**Autor:** Aria (Architect) + Eurico (Product Owner)
**Status:** Draft — aguarda validacao de assets

---

## 1. Contexto e Problema

A Maria Serqueira e consultora da VooViver Viagens — agencia portuguesa de viagens de grupo com destinos unicos (Socotra, Uganda/Ruanda, Marrocos) a precos 35-70% abaixo da concorrencia.

**Problema actual:**
- A pagina de orcamento da Maria no site VooViver mostra dados de outra consultora (bug critico)
- Formulario com 15+ campos — taxa de abandono estimada >80%
- Zero prova social no funil de vendas
- Headline generico que nao comunica nenhum diferenciador
- Score de marketing global: 33/100 (Grau F)

**Oportunidade:** O produto e forte, a comunicacao e fraca. Uma landing page profissional dedicada pode multiplicar conversoes por 3x a 5x.

---

## 2. Objectivos

| Objectivo | Metrica | Target |
|-----------|---------|--------|
| Aumentar taxa de conversao do formulario | Submissoes / visitantes | >15% (vs ~3% estimado actual) |
| Reduzir abandono do formulario | Taxa de conclusao multi-step | >50% |
| Tempo de carregamento | Lighthouse Performance | 95+ |
| Mobile first | Mobile usability score | 100 |
| SEO local | Schema markup + meta tags | Implementado |

---

## 3. Publico-Alvo

### Persona Primaria: Viajante de Grupo

| Atributo | Detalhe |
|----------|---------|
| Idade | 30-55 anos |
| Localizacao | Portugal (maioria Norte/Centro) |
| Motivacao | Viajar para destinos diferentes, em grupo, com lider/guia |
| Dores | Precos altos em agencias tradicionais, medo de viajar sozinho para destinos exoticos |
| Device | 65% mobile, 35% desktop (estimativa sector turismo PT) |
| Canais | Instagram, Facebook, WhatsApp, Google Search |

### Persona Secundaria: Lead Referido

Amigo/familiar de cliente anterior que recebeu o link da Maria por WhatsApp ou redes sociais.

---

## 4. Requisitos Funcionais

### FR-01: Hero Section

- Foto profissional da Maria (placeholder ate receber asset)
- Headline diferenciador: comunicar destinos unicos + precos imbativeis
- Sub-headline com proposta de valor clara
- 2 CTAs: "Pedir Orcamento Gratuito" (scroll to form) + "Falar por WhatsApp" (link directo)
- Background com imagem de destino (Socotra ou Marrocos)

### FR-02: Trust Bar

- Barra horizontal com indicadores de confianca
- Elementos: selo RNAVT N.12366, "X viagens organizadas", "Resposta em 24h", metodos de pagamento
- Visivel imediatamente abaixo do hero (above the fold em desktop)

### FR-03: Destinos em Destaque

- 4 cards de destinos: Socotra, Uganda/Ruanda, Marrocos, Tailandia
- Cada card: imagem, nome do destino, "desde X EUR/pessoa", badge "Voos incluidos"
- CTA em cada card: "Saber Mais" (scroll to form com destino pre-seleccionado)
- Layout: grid 2x2 em desktop, stack vertical em mobile

### FR-04: Comparacao de Precos

- Tabela comparativa VooViver vs concorrencia (Pinto Lopes, Leva-Me)
- Destaque visual na diferenca percentual (-70%, -67%, -56%)
- Nota: "Todos os pacotes incluem voo, alojamento e guia"
- Fonte dos dados: auditoria de marketing 28/03/2026

### FR-05: Testemunhos

- 3 slots para testemunhos de clientes reais da Maria
- Cada testemunho: texto, nome, destino visitado, data, foto (opcional)
- Placeholder ate receber testemunhos reais
- Fallback: se zero testemunhos disponiveis, secao oculta no lancamento

### FR-06: Sobre a Maria

- Bio curta (3-4 frases)
- Foto profissional
- Especialidades/destinos favoritos
- "Porque escolhi ser consultora VooViver"
- Link para redes sociais da Maria (se existirem)

### FR-07: Formulario Multi-Step (Progressive Disclosure)

- **Passo 1 (captura):** Nome, email, telefone — 3 campos apenas
- **Passo 2 (qualificacao):** Destino (dropdown), datas aproximadas, numero de pessoas
- **Passo 3 (opcional):** Observacoes livres, como conheceu a Maria
- Barra de progresso visual (3 pontos)
- Submissao parcial no passo 1 (lead capturado mesmo com abandono)
- Alternativa WhatsApp sempre visivel ao lado do formulario
- Validacao inline (sem reload)
- Confirmacao visual apos envio + mensagem "A Maria responde em 24h"

### FR-08: FAQ com Schema

- 5-6 perguntas frequentes:
  1. "Os voos estao incluidos no preco?"
  2. "Posso pagar em prestacoes?"
  3. "Qual o tamanho dos grupos?"
  4. "Preciso de visto para estes destinos?"
  5. "E seguro viajar para Socotra/Uganda?"
  6. "Como funciona o pedido de orcamento?"
- Schema markup FAQPage para rich snippets no Google
- Accordion/collapse nativo (sem JS externo)

### FR-09: Footer

- RNAVT N.12366
- Link RGPD / Politica de Privacidade
- Metodos de pagamento aceites
- Livro de reclamacoes
- Link discreto "Queres ser consultor VooViver?" (separacao de funis)
- Copyright

### FR-10: SEO e Meta Tags

- Title: "Maria Serqueira — Viagens de Grupo desde 870 EUR | VooViver"
- Meta description optimizada com CTA
- Open Graph tags com imagem de destino
- Twitter Cards
- Schema markup: TravelAgency + TouristTrip + FAQPage
- Canonical URL unico
- Sitemap.xml
- robots.txt

---

## 5. Requisitos Nao-Funcionais

| NFR | Requisito | Target |
|-----|-----------|--------|
| NFR-01 | Performance | Lighthouse Performance >= 95 |
| NFR-02 | Mobile First | 100% responsivo, formulario usavel em telemovel |
| NFR-03 | Acessibilidade | WCAG 2.1 AA minimo |
| NFR-04 | Velocidade | LCP < 1.5s, CLS < 0.1, FID < 100ms |
| NFR-05 | Compatibilidade | Chrome, Safari, Firefox, Edge (ultimas 2 versoes) |
| NFR-06 | RGPD | Sem cookies de tracking sem consentimento, formulario com checkbox RGPD |
| NFR-07 | Seguranca | HTTPS obrigatorio, sanitizacao de inputs do formulario |
| NFR-08 | Uptime | 99.9% (garantido por Vercel) |

---

## 6. Stack Tecnico

| Camada | Tecnologia | Versao | Justificacao |
|--------|------------|--------|--------------|
| Framework | Astro | 5.x | SSG, zero JS por defeito, performance maxima |
| Styling | Tailwind CSS | 4.x | Utility-first, responsivo, design system rapido |
| Formulario backend | Formspree ou Resend | - | Sem backend proprio, RGPD compliant |
| Hosting | Vercel | - | Deploy instantaneo, CDN, dominio custom |
| Analytics | Plausible | - | RGPD compliant, sem cookies, leve |
| Imagens | Astro Image (sharp) | - | Optimizacao automatica, WebP/AVIF, lazy loading |
| Icons | Astro Icon (Lucide) | - | SVG inline, zero overhead |

### Decisoes Arquitecturais

| Decisao | Escolha | Alternativa Rejeitada | Razao |
|---------|---------|----------------------|-------|
| SSG vs SSR | SSG (build time) | SSR | Landing page estatica, nao precisa de dados dinamicos |
| Framework | Astro | Next.js / Nuxt | Overkill para single landing page, Astro e mais leve |
| Form backend | Formspree/Resend | API custom | Sem necessidade de backend, reduz complexidade |
| CSS | Tailwind | CSS Modules | Velocidade de desenvolvimento, design system integrado |
| Hosting | Vercel | Netlify / Cloudflare Pages | Integracao nativa com Astro, preview deploys |

---

## 7. Estrutura de Ficheiros

```
vooviver-mj/
├── src/
│   ├── layouts/
│   │   └── Layout.astro            # Layout base (head, meta, fonts)
│   ├── pages/
│   │   └── index.astro             # Landing page unica
│   ├── components/
│   │   ├── Hero.astro              # FR-01
│   │   ├── TrustBar.astro          # FR-02
│   │   ├── Destinations.astro      # FR-03
│   │   ├── PriceComparison.astro   # FR-04
│   │   ├── Testimonials.astro      # FR-05
│   │   ├── AboutMaria.astro        # FR-06
│   │   ├── ContactForm.astro       # FR-07 (multi-step island)
│   │   ├── FAQ.astro               # FR-08
│   │   └── Footer.astro            # FR-09
│   ├── data/
│   │   ├── destinations.json       # Dados dos destinos + precos
│   │   ├── testimonials.json       # Testemunhos (editavel pela Maria)
│   │   └── faq.json                # Perguntas frequentes
│   ├── styles/
│   │   └── global.css              # Tailwind base + custom fonts
│   └── assets/
│       ├── maria-serqueira.webp    # Foto profissional
│       ├── destinations/           # Imagens dos destinos
│       └── vooviver-logo.svg       # Logo VooViver
├── public/
│   ├── favicon.ico
│   ├── robots.txt
│   └── sitemap.xml
├── astro.config.mjs
├── tailwind.config.mjs
├── package.json
├── tsconfig.json
├── .gitignore
├── MARKETING-AUDIT-VOOVIVER.md     # Referencia (auditoria original)
├── MARKETING-AUDIT-VOOVIVER.pdf    # Referencia (versao PDF)
└── PRD-LANDING-PAGE-MARIA-SERQUEIRA.md  # Este documento
```

---

## 8. Design Direction

### Paleta de Cores (proposta)

| Uso | Cor | Hex | Nota |
|-----|-----|-----|------|
| Primaria | Azul oceano profundo | #1B4965 | Confianca, viagem, profissionalismo |
| Secundaria | Coral quente | #E07A5F | Energia, aventura, CTAs |
| Accent | Dourado suave | #D4A574 | Premium, destaque de precos |
| Background | Branco quente | #FAFAF8 | Limpo, leve |
| Texto | Cinzento escuro | #2D3436 | Legibilidade maxima |
| Texto secundario | Cinzento medio | #636E72 | Labels, metadata |

> **Nota:** Paleta a validar com a Maria e com a identidade VooViver existente. Se a VooViver tiver brand guidelines, prevalecem.

### Tipografia

| Uso | Fonte | Peso |
|-----|-------|------|
| Headlines | Inter | 700-900 |
| Body | Inter | 400 |
| Precos/badges | JetBrains Mono | 700 |

### Principios de Design

1. **Mobile first** — 65% do trafego vem de telemovel
2. **Whitespace generoso** — respiracao entre seccoes
3. **Imagens grandes** — destinos vendem-se pelo visual
4. **CTAs contrastantes** — coral sobre fundo claro, impossiveis de ignorar
5. **Formulario nao-intimidante** — 3 campos visiveis, resto progressivo

---

## 9. Assets Necessarios (Recolher com a Maria)

| Asset | Status | Prioridade | Notas |
|-------|--------|------------|-------|
| Foto profissional da Maria | A RECOLHER | P0 | Fundo neutro, sorriso, profissional |
| 2-3 testemunhos de clientes | A RECOLHER | P0 | Nome, destino, texto curto |
| Bio da Maria (3-4 frases) | A RECOLHER | P0 | Experiencia, motivacao, especialidades |
| Imagens dos destinos | A RECOLHER | P1 | Socotra, Uganda, Marrocos, Tailandia |
| Logo VooViver (SVG) | A RECOLHER | P1 | Formato vectorial se disponivel |
| Numero de viagens organizadas | A RECOLHER | P1 | Para trust bar |
| Link WhatsApp Business | A RECOLHER | P0 | Numero activo da Maria |
| Redes sociais da Maria | A RECOLHER | P2 | Instagram, Facebook (se existirem) |
| Dominio/URL final | A DECIDIR | P0 | Subdominio vs path vs dominio proprio |

---

## 10. Entrega por Fases

### Fase 1: MVP (Lancamento)

Todas as seccoes funcionais com dados reais onde disponivel, placeholders onde nao.

| Seccao | Depende de asset? | Fallback |
|--------|-------------------|----------|
| Hero | Foto Maria | Imagem destino como background, sem foto |
| Trust Bar | N. viagens | "Centenas de viagens" (generico) |
| Destinos | Imagens destinos | Stock photos de alta qualidade |
| Precos | Nao | Dados da auditoria ja disponiveis |
| Testemunhos | Testemunhos reais | Seccao oculta ate ter dados |
| Sobre Maria | Bio + foto | Texto generico + sem foto |
| Formulario | WhatsApp link | Formulario + email como fallback |
| FAQ | Nao | Dados da auditoria ja disponiveis |

### Fase 2: Optimizacao (Semana 2-3)

- Integrar todos os assets reais recebidos da Maria
- A/B testing de headlines (se trafego suficiente)
- Ajustar copy com base em feedback da Maria
- Adicionar Plausible Analytics
- Submeter sitemap ao Google Search Console

### Fase 3: Crescimento (Mes 2+)

- Programa de recolha de testemunhos (email automatico pos-viagem)
- Blog/guias de destinos (se aprovado)
- Integrar Google Business Profile reviews
- Considerar paginas individuais por destino (SEO)

---

## 11. Restricoes e Dependencias

| Restricao | Impacto |
|-----------|---------|
| Sem acesso ao backend VooViver (PrestaShop) | Formulario usa servico externo (Formspree/Resend) |
| Assets da Maria podem demorar | MVP lanca com fallbacks, actualiza depois |
| Dominio a decidir | Pode ser dominio proprio ou subdominio VooViver |
| RGPD obrigatorio | Checkbox de consentimento no formulario, politica de privacidade |

---

## 12. Criterios de Aceitacao

- [ ] Landing page carrega em <1.5s (LCP)
- [ ] Lighthouse Performance >= 95
- [ ] Formulario funcional em 3 passos com submissao parcial
- [ ] Responsivo e usavel em iPhone SE (menor viewport comum)
- [ ] Schema markup valido (teste com Google Rich Results Test)
- [ ] Meta tags Open Graph correctas (teste com Facebook Debugger)
- [ ] WhatsApp link funcional
- [ ] RGPD: checkbox de consentimento presente
- [ ] Zero erros na consola do browser
- [ ] Deployed e acessivel via URL publico

---

*PRD criado por Aria (Architect) — 28/03/2026*
*Baseado na Auditoria de Marketing VooViver (AI Marketing Suite)*
