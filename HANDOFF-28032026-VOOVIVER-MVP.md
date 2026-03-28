# HANDOFF — VooViver / Sair da Caixa Viagens
**Data:** 28/03/2026
**Sessao:** MVP Landing Page + Estrategia de Funil
**Cliente:** Maria Jose Sequeira
**Projecto:** vooviver-mj
**URL Producao:** https://vooviver-mj.vercel.app

---

## 1. O que foi feito nesta sessao

### Entregaveis Completos

| Entregavel | Estado | Notas |
|------------|--------|-------|
| Auditoria de Marketing VooViver | Completa | Score 33/100, 7 accoes imediatas identificadas |
| PRD Landing Page | Completo | 10 FRs, 8 NFRs, 3 fases de entrega |
| 4 Stories de Desenvolvimento | Validadas (GO) | 1.1 Setup, 1.2 Seccoes, 1.3 Form/SEO, 1.4 Performance |
| Landing Page MVP | LIVE | https://vooviver-mj.vercel.app |
| Design System Dark Premium | Implementado | Glassmorphism, gold/teal, animacoes scroll |
| Formulario Multi-Step | Funcional | 3 passos, Formsubmit.co → mjcsequeira@gmail.com |
| SEO + Schema Markup | Implementado | TravelAgency, TouristTrip, FAQPage |
| Deploy Vercel | Producao | Build automatico, CDN global |

### Stack Tecnico

| Camada | Tecnologia |
|--------|------------|
| Framework | Astro 6.1.1 (SSG) |
| Styling | Tailwind CSS 4 (CSS-first) |
| Form Backend | Formsubmit.co (mjcsequeira@gmail.com) |
| Hosting | Vercel (producao) |
| Imagens | Unsplash (placeholder) + foto real da Maria |

### Commits

| Hash | Mensagem |
|------|----------|
| f7cf86a | feat: landing page premium dark |
| 45a776f | fix(form): configurar Formsubmit.co com email real |
| 0ebf2e6 | docs: auditoria, PRD, stories e assets |

---

## 2. Dados da Cliente

| Campo | Valor |
|-------|-------|
| Nome completo | Maria Jose Sequeira |
| Email | mjcsequeira@gmail.com |
| WhatsApp | +351 933 096 770 |
| Facebook | https://www.facebook.com/mariajose.sequeira.5 |
| Instagram | https://www.instagram.com/sairdacaixa.viagens/ |
| LinkedIn | https://www.linkedin.com/in/maria-jos%C3%A9-sequeira-58a81b48/ |
| Marca pessoal | Sair da Caixa Viagens |
| Empresa | VooViver Viagens (RNAVT N.12366) |
| Pagina VooViver | vooviver.com/pt/contact/pedido-de-orcamento-de-viagens-maria-serqueira |

---

## 3. Brandbook — Sair da Caixa Viagens / Maria Jose Sequeira

### 3.1 Posicionamento

| Elemento | Definicao |
|----------|-----------|
| Categoria | Consultora de viagens de grupo para destinos unicos |
| Tagline proposta | "Sair da Caixa — viagens de grupo para destinos que nao encontras em mais nenhuma agencia" |
| Diferenciador #1 | Destinos exclusivos que nenhum concorrente PT oferece (Socotra, Uganda/Ruanda) |
| Diferenciador #2 | Precos 35-70% abaixo da concorrencia com voos incluidos |
| Diferenciador #3 | Consultora pessoal — nao e uma agencia impessoal, e a Maria |
| Publico-alvo | Portugueses 30-55 anos, aventureiros mas que querem seguranca de grupo |
| Promessa | Destinos impossiveis a precos imbativeis, com tudo incluido |

### 3.2 Tom de Voz

| Regra | Detalhe |
|-------|---------|
| Tom | Directo, autentico, de quem ja viajou — nunca vendedora |
| Pessoa | 1a pessoa quando fala a Maria, 2a pessoa para o viajante |
| Estilo | Conversa entre amigos que partilham a paixao por viajar |
| PROIBIDO | "curso", "facil", "automatico", "revolucionario", "garantido" |
| PREFERIDO | "descobrir", "explorar", "sair da caixa", "destinos unicos", "grupo", "aventura real" |
| Heroi | O viajante e sempre o heroi — a Maria e a guia que torna possivel |

### 3.3 Identidade Visual (Design System Implementado)

**Paleta de Cores:**

| Nome | Hex | Uso |
|------|-----|-----|
| Background | #06060B | Fundo principal — dark premium |
| Surface | #0D0D14 | Seccoes alternadas |
| Card | #12121A | Cards e superficies elevadas |
| Text | #F0F0F5 | Texto principal |
| Text Secondary | #8892A4 | Texto secundario, labels |
| Text Muted | #4A5568 | Placeholders, texto desactivado |
| Gold | #F5A623 | Premium, precos, destaques, CTA primario |
| Teal | #00D4AA | Accao, sucesso, CTA secundario |
| Coral | #FF6B6B | Urgencia, badges de desconto |
| Purple | #8B5CF6 | Exclusivo, especial |

**Tipografia:**

| Uso | Fonte | Peso |
|-----|-------|------|
| Display/H1 | Inter | 900, -0.03em tracking |
| H2 | Inter | 800 |
| Body | Inter | 400, line-height 1.8 |
| Precos/Badges | JetBrains Mono | 700 |

**Componentes Visuais:**

| Componente | Estilo |
|------------|--------|
| Cards | Glassmorphism: rgba(255,255,255,0.04) + blur(16px) + border rgba(255,255,255,0.08) |
| Botoes primarios | Gold (#F5A623) com glow shadow |
| Botoes WhatsApp | Verde com pulse animation |
| Hover em cards | translateY(-4px) + gold glow shadow |
| Scroll animations | Fade-in-up com Intersection Observer |
| Gradientes | Gold → Teal para highlights |
| Badges | Glass com border colorida (teal, purple, coral) |

### 3.4 Assets Disponiveis

| Asset | Localizacao | Estado |
|-------|-------------|--------|
| Foto profissional Maria | src/assets/maria-jose-sequeira.png | Disponivel |
| Logo VooViver | A RECOLHER | Necessario em SVG |
| Videos Instagram | @sairdacaixa.viagens | Disponivel para embed |
| Imagens destinos | Unsplash (placeholder) | Substituir por fotos reais |

---

## 4. Estrategia de Funil — Captacao de Contactos

### 4.1 Funil Actual (Landing Page MVP)

```
                    TOPO DO FUNIL
    ┌─────────────────────────────────────┐
    │  Instagram / Facebook / WhatsApp    │
    │  → Link para landing page           │
    └──────────────┬──────────────────────┘
                   ▼
              MEIO DO FUNIL
    ┌─────────────────────────────────────┐
    │  Landing Page (vooviver-mj)         │
    │  → Hero + Destinos + Precos         │
    │  → Prova social (testemunhos)       │
    │  → Comparacao competitiva           │
    └──────────────┬──────────────────────┘
                   ▼
            FUNDO DO FUNIL
    ┌─────────────────────────────────────┐
    │  Formulario Multi-Step OU WhatsApp  │
    │  → Lead capturado (email)           │
    │  → Maria responde em 24h           │
    └─────────────────────────────────────┘
```

### 4.2 Funil Optimizado (Proximas Fases)

```
    ATRACCAO (novo)
    ┌─────────────────────────────────────┐
    │  1. Guias de destinos (blog/SEO)    │
    │  2. Reels Instagram com CTA         │
    │  3. Pinterest boards por destino    │
    │  4. Google Ads (destinos unicos)    │
    └──────────────┬──────────────────────┘
                   ▼
    CAPTACAO (melhorar)
    ┌─────────────────────────────────────┐
    │  5. Lead magnet: "Guia Gratuito     │
    │     dos 10 Destinos Mais Baratos"   │
    │  6. Pop-up de saida com desconto    │
    │  7. Quiz "Qual o teu destino ideal?"│
    └──────────────┬──────────────────────┘
                   ▼
    NURTURING (novo)
    ┌─────────────────────────────────────┐
    │  8. Email sequence (5 emails)       │
    │     D+0: Obrigado + destinos        │
    │     D+3: Historia de viagem real    │
    │     D+7: Comparacao de precos       │
    │     D+14: Testemunho de cliente     │
    │     D+21: Oferta limitada           │
    │  9. WhatsApp follow-up pessoal      │
    └──────────────┬──────────────────────┘
                   ▼
    CONVERSAO (melhorar)
    ┌─────────────────────────────────────┐
    │  10. Orcamento personalizado        │
    │  11. Chamada/video com a Maria      │
    │  12. Pagamento + confirmacao        │
    └──────────────┬──────────────────────┘
                   ▼
    RETENCAO (novo)
    ┌─────────────────────────────────────┐
    │  13. Email pos-viagem (testemunho)  │
    │  14. Programa de referencia         │
    │  15. Grupo WhatsApp de viajantes    │
    └─────────────────────────────────────┘
```

### 4.3 Lead Magnets Propostos

| Lead Magnet | Formato | Objectivo | Prioridade |
|-------------|---------|-----------|------------|
| "10 Destinos de Grupo Mais Baratos que Sozinho" | PDF/eBook | Captar emails | P0 |
| "Quiz: Qual o Teu Proximo Destino?" | Pagina interactiva | Segmentar leads por destino | P1 |
| "Checklist: O Que Levar para Africa" | PDF | Captar leads interessados em Africa | P2 |
| "Comparador de Precos: VooViver vs Agencias" | Pagina | Converter indecisos | P1 |

### 4.4 Email Nurture Sequence

| Email | Dia | Assunto | Objectivo |
|-------|-----|---------|-----------|
| 1 | D+0 | "Obrigado! Aqui estao os destinos mais procurados" | Welcome + destinos |
| 2 | D+3 | "Como 15 portugueses descobriram Socotra por 1.880 EUR" | Historia real + prova social |
| 3 | D+7 | "Ja comparaste precos? Vais ficar surpreso" | Tabela comparativa + diferenciacao |
| 4 | D+14 | "O que a Ana disse depois de voltar de Uganda" | Testemunho + emocao |
| 5 | D+21 | "Ultimas vagas para [destino] — [data]" | Urgencia + CTA final |

---

## 5. Estrategia de Marketing — Proximos Passos

### 5.1 Accoes Imediatas (Esta Semana)

| # | Accao | Responsavel | Impacto |
|---|-------|-------------|---------|
| 1 | Maria verifica email Formsubmit.co (1a submissao) | Maria | Formulario funcional |
| 2 | Recolher 3 testemunhos reais de clientes | Maria | +20% conversao |
| 3 | Substituir imagens Unsplash por fotos reais | Dev | Autenticidade |
| 4 | Criar destaque no Instagram com link para landing page | Maria | Trafego |
| 5 | Partilhar landing page no WhatsApp Business | Maria | Leads directos |

### 5.2 Accoes Este Mes

| # | Accao | Responsavel | Impacto |
|---|-------|-------------|---------|
| 6 | Criar lead magnet "10 Destinos Mais Baratos" | Marketing | Captacao de emails |
| 7 | Configurar email nurture (5 emails) | Marketing | Nurturing automatico |
| 8 | Criar 4 Reels Instagram com CTA para landing page | Maria | Trafego organico |
| 9 | Activar Google Business Profile | Maria | SEO local |
| 10 | Pedir reviews no Google a clientes anteriores | Maria | Prova social |
| 11 | Adicionar dominio personalizado (ex: sairdacaixa.pt) | DevOps | Marca propria |

### 5.3 Accoes Este Trimestre

| # | Accao | Responsavel | Impacto |
|---|-------|-------------|---------|
| 12 | Blog com guias de destinos (SEO) | Marketing | Trafego organico a longo prazo |
| 13 | Pinterest boards por destino | Maria | Canal visual de descoberta |
| 14 | Programa de referencia (desconto por indicacao) | Marketing | Growth loop |
| 15 | Landing pages individuais por destino | Dev | SEO + conversao especifica |
| 16 | A/B testing de headlines e CTAs | Marketing | Optimizacao continua |
| 17 | TikTok/Reels de experiencias reais | Maria | Alcance organico |

---

## 6. Melhorias Pendentes na Landing Page

| # | Melhoria | Prioridade | Notas |
|---|----------|------------|-------|
| 1 | Substituir imagens Unsplash por fotos reais dos destinos | P0 | Maria tem fotos no Instagram |
| 2 | Adicionar testemunhos reais (testimonials.json) | P0 | Recolher com a Maria |
| 3 | Embed de video Instagram real | P1 | Usar Reel da @sairdacaixa.viagens |
| 4 | Ajustar copy do hero com feedback da Maria | P1 | Tom mais pessoal |
| 5 | Adicionar mais destinos (Vietname, etc.) | P1 | Actualizar destinations.json |
| 6 | Pagina de destino individual (ex: /socotra) | P2 | SEO especifico |
| 7 | Lead magnet popup de saida | P2 | Captar quem abandona |
| 8 | Integrar Google Analytics / Plausible | P1 | Medir conversoes |
| 9 | Dominio personalizado | P1 | sairdacaixa.pt ou similar |
| 10 | Favicon personalizado (logo Maria/SdC) | P2 | Branding |
| 11 | Animacoes mais refinadas (parallax hero) | P2 | Premium feel |
| 12 | Pagina de obrigado pos-formulario | P2 | Tracking + CTA adicional |

---

## 7. Metricas a Monitorizar

| Metrica | Ferramenta | Target |
|---------|------------|--------|
| Visitantes unicos | Plausible/GA | Baseline → crescimento 20%/mes |
| Taxa de conversao formulario | Formsubmit.co logs | >15% |
| Taxa de conclusao formulario | Custom (JS events) | >50% dos que iniciam |
| Origem do trafego | Plausible/GA | Instagram > WhatsApp > Google |
| Lighthouse Performance | PageSpeed Insights | >= 95 |
| Tempo no site | Plausible/GA | > 2 minutos |
| Bounce rate | Plausible/GA | < 40% |

---

## 8. Ficheiros do Projecto

```
vooviver-mj/
├── src/
│   ├── assets/
│   │   └── maria-jose-sequeira.png     # Foto real
│   ├── components/
│   │   ├── Hero.astro                  # Hero cinematico dark
│   │   ├── TrustBar.astro              # Barra de confianca glass
│   │   ├── Destinations.astro          # Cards destinos premium
│   │   ├── PriceComparison.astro       # Comparacao de precos
│   │   ├── Testimonials.astro          # Testemunhos (aguarda dados)
│   │   ├── VideoShowcase.astro         # Seccao Instagram/video
│   │   ├── AboutMaria.astro            # Bio + foto + social
│   │   ├── ContactForm.astro           # Form 3-step + WhatsApp
│   │   ├── FAQ.astro                   # Accordion + Schema
│   │   ├── Footer.astro                # Footer dark + legal
│   │   └── FloatingWhatsApp.astro      # Botao flutuante WhatsApp
│   ├── data/
│   │   ├── destinations.json           # 4 destinos com precos
│   │   ├── testimonials.json           # Vazio (recolher)
│   │   └── faq.json                    # 6 FAQs
│   ├── layouts/
│   │   └── Layout.astro                # Meta, OG, Schema, fonts
│   ├── pages/
│   │   └── index.astro                 # Pagina principal
│   └── styles/
│       └── global.css                  # Design system dark premium
├── docs/
│   └── stories/                        # 4 stories do MVP
├── MARKETING-AUDIT-VOOVIVER.md         # Auditoria completa
├── MARKETING-AUDIT-VOOVIVER.pdf        # Versao PDF formatada
├── PRD-LANDING-PAGE-MARIA-SERQUEIRA.md # Requisitos
├── HANDOFF-28032026-VOOVIVER-MVP.md    # Este ficheiro
├── astro.config.mjs
├── vercel.json
└── package.json
```

---

## 9. Acessos e Configuracoes

| Servico | Estado | Notas |
|---------|--------|-------|
| Vercel | Conectado | euricojsalves-4744s-projects/vooviver-mj |
| Formsubmit.co | Configurado | mjcsequeira@gmail.com (verificar 1a submissao) |
| Dominio | Vercel default | vooviver-mj.vercel.app (dominio custom pendente) |
| Git | Local | 3 commits, sem remote GitHub |

---

## 10. Decisoes Tomadas

| Decisao | Escolha | Alternativa Rejeitada | Razao |
|---------|---------|----------------------|-------|
| Stack | Astro 6 SSG | Next.js / Nuxt | Overkill para landing page estatica |
| Design | Dark premium | Light theme | Cliente rejeitou light como "10% do esperado" |
| Form backend | Formsubmit.co | Formspree / API custom | Zero config, funciona com email directo |
| Hosting | Vercel | Netlify / Cloudflare | Integracao nativa Astro, deploy instantaneo |
| CSS | Tailwind 4 CSS-first | Tailwind 3 / CSS Modules | Mais moderno, sem config JS |
| Nome | Maria Jose Sequeira | Maria Serqueira (inicial) | Corrigido com dados reais do Facebook/LinkedIn |

---

## 11. Riscos e Dependencias

| Risco | Probabilidade | Impacto | Mitigacao |
|-------|---------------|---------|-----------|
| Maria nao verifica email Formsubmit.co | Media | Alto | Contactar Maria directamente |
| Imagens Unsplash removidas | Baixa | Medio | Substituir por fotos reais ASAP |
| Sem testemunhos reais | Alta | Alto | Recolher activamente com Maria |
| Sem dominio personalizado | Certa | Medio | Registar sairdacaixa.pt |
| Sem analytics instalado | Certa | Medio | Instalar Plausible na proxima sessao |

---

## 12. Proxima Sessao — Agenda Recomendada

1. **Melhorias visuais** que o Eurico identificou (refinamentos)
2. **Testemunhos reais** — integrar se a Maria ja enviou
3. **Lead magnet** — criar eBook "10 Destinos" como PDF
4. **Email nurture** — configurar sequencia de 5 emails
5. **Dominio personalizado** — registar e configurar
6. **Analytics** — instalar Plausible
7. **Fotos reais** — substituir Unsplash pelos originais
8. **Video Instagram** — embed real no VideoShowcase

---

*HANDOFF criado em 28/03/2026 por Aria (Architect) + Eurico (Product Owner)*
*Projecto VooViver — Sair da Caixa Viagens*
*URL: https://vooviver-mj.vercel.app*
