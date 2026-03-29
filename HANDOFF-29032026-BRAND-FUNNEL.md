# HANDOFF — Sessao 29/03/2026
## Brandbook + Logo + eBook + Funil de Captacao + Campanha

**Data:** 29/03/2026
**Projecto:** vooviver-mj — Sair da Caixa Viagens
**Cliente:** Maria Jose C. Sequeira
**URL Producao:** https://vooviver-mj.vercel.app
**GitHub:** https://github.com/DaSilvaAlves/vooviver-mj (publico)
**Objectivo da sessao:** Criar um funil completo para captar contactos — do brandbook ao lancamento

---

## 1. Contexto e Objectivo Original

O pedido foi claro: **pensar GRANDE e encurtar o percurso para o sucesso.**

A sequencia logica definida:
1. Brandbook profissional e detalhado (bases solidas)
2. Logo/marca (identidade visual)
3. eBook de 45-55 paginas (isco/lead magnet irrecusavel)
4. Funil de captacao de contactos
5. Campanha de lancamento

Tudo isto para um unico objectivo: **captar contactos para a Maria atraves de um eBook tao valioso que as pessoas se sintam estupidas por nao o adquirir.**

---

## 2. Quem e a Maria Jose — Perfil Completo

| Campo | Informacao |
|-------|-----------|
| Nome completo | Maria Jose C. Sequeira |
| Nascimento | 26/12/1971 |
| Naturalidade | Vila Nova de Cacela, Algarve |
| Background | Familia humilde e trabalhadora, QI acima da media |
| Lingua | Portugues nativo + Ingles fluente |
| Personalidade | Excelente comunicadora, relacoes publicas nata, perfeccionista, sabe colocar as palavras |
| Email | mjcsequeira@gmail.com |
| WhatsApp | +351 933 096 770 |
| Instagram pessoal | @sequeira7780 (212 seguidores) |
| Instagram marca | @sairdacaixa.viagens (29 seguidores) |
| Facebook | facebook.com/mariajose.sequeira.5 |
| LinkedIn | linkedin.com/in/maria-jose-sequeira-58a81b48 |

### Percurso Profissional

| Fase | Funcao | O que trouxe para as viagens |
|------|--------|------------------------------|
| 1a | Recepcionista de 1a classe nos melhores hoteis do Algarve | Padrao de excelencia, carteira profissional de recepcionista |
| 2a | Chefe de loja em campos de golfe | Gestao de clientes premium, atencao ao detalhe |
| 3a | Consultora imobiliaria (venda de imoveis) | Negociacao, construcao de confianca, fecho |
| 4a | Consultora de viagens — Sair da Caixa Viagens | Tudo acima + paixao por viajar e conhecer o mundo |

### Relacao com VooViver

| Aspecto | Detalhe |
|---------|---------|
| Estatuto | Associada, independente com marca propria |
| Licenca | Opera sob RNAVT N.12366 da VooViver |
| Marca propria | "Sair da Caixa Viagens" (nome definitivo) |
| Autonomia | Escolhe destinos, define precos, gere clientes |
| Tempo na area | 12 meses (mais a serio) |
| Experiencia | Vasta — varios destinos organizados |

### Situacao Actual

| Aspecto | Estado |
|---------|--------|
| Clientes/leads por mes | Poucos — fase de captacao |
| Ticket medio | 500-1.500 EUR/pessoa |
| Orcamento marketing | 50 EUR/mes |
| Canais activos | Instagram (organico), WhatsApp Business, boca-a-boca |
| Conhecimentos digitais | Tem conhecimentos de marketing digital, precisa de ajuda para estruturar |

### Visao a 1 Ano

Mais grupos, mais destinos, equipa propria, **independencia total da VooViver.**

---

## 3. O que foi Feito nesta Sessao

### 3.1 Entregaveis — Documentacao (7 documentos)

| # | Documento | Ficheiro | Descricao |
|---|-----------|----------|-----------|
| 1 | **Brandbook Profissional** | `docs/BRANDBOOK-SAIR-DA-CAIXA-VIAGENS.md` | 16 seccoes: posicionamento, personas (Sofia/Carlos+Rita/Ana), tom de voz com formulas de copy, paleta de 10 cores com WCAG, tipografia (Inter + JetBrains Mono), iconografia, aplicacoes (site, Instagram, WhatsApp, cartao, email), do's/don'ts, glossario |
| 2 | **Briefing Criativo de Logo** | `docs/LOGO-BRIEF-SAIR-DA-CAIXA.md` | 3 direcoes criativas (Caixa que se Abre, Bussola, Horizonte), 6 variacoes de logo, specs dark/light/mono, opcoes de execucao por orcamento |
| 3 | **Estrutura do eBook** | `docs/EBOOK-STRUCTURE-GUIA-VIAJANTE.md` | Indice dos 12 capitulos, copy de cada seccao (resumido), specs de design do PDF (tipografia, cores, layout, caixas de destaque) |
| 4 | **Conteudo Completo do eBook** | `docs/EBOOK-CONTENT-FULL.md` | **Manuscrito integral de 52 paginas.** 12 capitulos com texto corrido, tabelas, checklists, dicas. Voz da Maria em 1a pessoa. Pronto para formatar em PDF. |
| 5 | **Funil de Captacao** | `docs/FUNNEL-CAPTACAO-CONTACTOS.md` | Arquitectura completa: landing page /guia → formulario → autoresposta → 5 emails de nurturing (D+0 a D+21) → conversao WhatsApp. Copy dos 5 emails incluido. Backend: Brevo (gratis). |
| 6 | **Playbook de Lancamento** | `docs/LAUNCH-PLAYBOOK-SAIR-DA-CAIXA.md` | 6 semanas dia-a-dia: semana 1 setup, semana 2 antecipacao, semana 3 LANCAMENTO (posts prontos para Instagram/WhatsApp/Facebook), semanas 4-6 amplificacao. Orcamento 25-42 EUR/mes. ROI projectado. |
| 7 | **Guia Setup Brevo** | `docs/GUIA-SETUP-BREVO.md` | Passo-a-passo para a Maria criar conta Brevo, configurar formulario, programar os 5 emails automaticos, RGPD. Escrito para nao-tecnicos. |

### 3.2 Entregaveis — Codigo (4 ficheiros)

| # | Ficheiro | Descricao |
|---|----------|-----------|
| 1 | `src/pages/guia.astro` | Landing page do eBook. Hero com mockup do livro, formulario (nome + email), seccao "O que vais aprender" (8 bullet points), mini bio da Maria, comparacao de precos que choca (Uganda -70%, Marrocos -67%), CTA final repetido. Dark premium, glassmorphism. |
| 2 | `src/pages/guia/obrigado.astro` | Pagina pos-submissao. Icone de sucesso, mensagem "O guia esta a caminho", 3 CTAs: ver destinos, seguir Instagram, falar WhatsApp. |
| 3 | `src/components/EbookBanner.astro` | Banner glass card na pagina principal (entre AboutMaria e ContactForm) que linka para /guia. Icone de livro, badge "GRATIS — 52 PAGINAS", seta animada no hover. |
| 4 | `src/pages/index.astro` | Modificado — import e inclusao do EbookBanner. |

### 3.3 Entregaveis — Assets Visuais

| # | Asset | Localizacao | Descricao |
|---|-------|-------------|-----------|
| 1 | Logo transparente 512px | `public/assets/logo/sair-da-caixa-transparent-512.png` | Cubo isometrico com face aberta + aviao dourado a sair + estrelas + "Sair da Caixa" + "VIAGENS". Fundo transparente. |
| 2 | Logo dark 1024px | `public/assets/logo/sair-da-caixa-dark-1024.png` | Mesma logo sobre fundo escuro. Para redes sociais e materiais. |
| 3 | Logo editavel no Canva | `https://www.canva.com/design/DAHFWz2xlfs/edit` | Design original editavel — a Maria pode modificar no Canva. |

### 3.4 Entregaveis — Canva (links editaveis)

| Asset | Links Canva (4 opcoes cada) |
|-------|----------------------------|
| **Logo** (escolhida) | [Editavel](https://www.canva.com/design/DAHFWz2xlfs/edit) |
| **Brandbook apresentacao** (4 opcoes — 20 slides cada) | [Op1](https://www.canva.com/d/aBrhZz6aODCJRkP) / [Op2](https://www.canva.com/d/xAvDYIcufrTbEFS) / [Op3](https://www.canva.com/d/SwkhHh6zozCLogP) / [Op4](https://www.canva.com/d/5wuJoagG9mllcPB) |
| **eBook documento** (4 opcoes) | [Op1](https://www.canva.com/d/qsNNxaVrWbBS-o4) / [Op2](https://www.canva.com/d/pWuWToX_n3LsgBA) / [Op3](https://www.canva.com/d/QQrHiU4KIoBbP_p) / [Op4](https://www.canva.com/d/iEJTFKDuLvlMR8e) |
| **Post Instagram lancamento** (4 opcoes) | [Op1](https://www.canva.com/d/gcIrIUTY6baPyZZ) / [Op2](https://www.canva.com/d/L4BTFgNmS9dTx1p) / [Op3](https://www.canva.com/d/4UFta4dRmghagLa) / [Op4](https://www.canva.com/d/xbLObp0F4LKIzdm) |
| **Cartao de visita** (escolhido: op4) | [Op4](https://www.canva.com/d/JhuURln4dwMumyh) |

### 3.5 Infraestrutura

| Accao | Estado |
|-------|--------|
| Repositorio GitHub criado | `github.com/DaSilvaAlves/vooviver-mj` (publico) |
| GitHub ligado ao Vercel | Conectado — deploy automatico a cada push |
| Deploy de producao | Feito — `vooviver-mj.vercel.app` ao vivo |
| Branch | `main` (default) |
| Build | Astro 6.1 SSG — 3 paginas, 1.79s build |

---

## 4. URLs ao Vivo

| Pagina | URL |
|--------|-----|
| Landing page principal | https://vooviver-mj.vercel.app |
| **Pagina do eBook (nova)** | **https://vooviver-mj.vercel.app/guia** |
| Pagina de obrigado | https://vooviver-mj.vercel.app/guia/obrigado |
| GitHub | https://github.com/DaSilvaAlves/vooviver-mj |

---

## 5. Commits desta Sessao

| Hash | Mensagem |
|------|----------|
| 4fcd160 | feat: brandbook, logo, eBook lead magnet, funil de captacao e pagina /guia |

---

## 6. Destinos e Precos (dados actuais)

| Destino | Preco Sair da Caixa | Concorrencia | Diferenca |
|---------|---------------------|-------------|-----------|
| Socotra | 1.880 EUR | EXCLUSIVO em PT | — |
| Uganda/Ruanda | 2.950 EUR | Pinto Lopes: 9.995 EUR | -70% |
| Marrocos | 870 EUR | Pinto Lopes: 2.595 EUR | -67% |
| Tailandia | 1.750 EUR | Media: ~2.800 EUR | -38% |

Todos os precos incluem voos.

---

## 7. Design System (referencia rapida)

| Token | Valor | Uso |
|-------|-------|-----|
| Background | #06060B | Fundo principal |
| Surface | #0D0D14 | Seccoes alternadas |
| Card | #12121A | Cards, superficies elevadas |
| Text | #F0F0F5 | Texto principal |
| Text Secondary | #8892A4 | Subtitulos, labels |
| Gold | #F5A623 | CTAs, precos, premium |
| Teal | #00D4AA | Sucesso, CTA secundario |
| Coral | #FF6B6B | Urgencia, badges desconto |
| Purple | #8B5CF6 | Exclusivo |
| Fonts | Inter + JetBrains Mono | Body/headings + precos/badges |

---

## 8. Ficheiros do Projecto (estado actual)

```
vooviver-mj/
├── src/
│   ├── assets/
│   │   └── maria-jose-sequeira.png
│   ├── components/
│   │   ├── Hero.astro
│   │   ├── TrustBar.astro
│   │   ├── Destinations.astro
│   │   ├── PriceComparison.astro
│   │   ├── Testimonials.astro
│   │   ├── VideoShowcase.astro
│   │   ├── AboutMaria.astro
│   │   ├── EbookBanner.astro          ★ NOVO
│   │   ├── ContactForm.astro
│   │   ├── FAQ.astro
│   │   ├── Footer.astro
│   │   └── FloatingWhatsApp.astro
│   ├── data/
│   │   ├── destinations.json
│   │   ├── testimonials.json
│   │   └── faq.json
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   ├── index.astro                ★ MODIFICADO (+ EbookBanner)
│   │   ├── guia.astro                 ★ NOVO
│   │   └── guia/
│   │       └── obrigado.astro         ★ NOVO
│   └── styles/
│       └── global.css
├── public/
│   └── assets/
│       └── logo/
│           ├── sair-da-caixa-transparent-512.png  ★ NOVO
│           └── sair-da-caixa-dark-1024.png        ★ NOVO
├── docs/
│   ├── stories/                        (4 stories MVP — sessao anterior)
│   ├── BRANDBOOK-SAIR-DA-CAIXA-VIAGENS.md    ★ NOVO
│   ├── LOGO-BRIEF-SAIR-DA-CAIXA.md           ★ NOVO
│   ├── EBOOK-STRUCTURE-GUIA-VIAJANTE.md       ★ NOVO
│   ├── EBOOK-CONTENT-FULL.md                  ★ NOVO (manuscrito 52 pag)
│   ├── FUNNEL-CAPTACAO-CONTACTOS.md           ★ NOVO
│   ├── LAUNCH-PLAYBOOK-SAIR-DA-CAIXA.md      ★ NOVO
│   └── GUIA-SETUP-BREVO.md                   ★ NOVO
├── CLAUDE.md
├── MARKETING-AUDIT-VOOVIVER.md         (sessao anterior)
├── PRD-LANDING-PAGE-MARIA-SERQUEIRA.md (sessao anterior)
├── HANDOFF-28032026-VOOVIVER-MVP.md    (sessao anterior)
├── HANDOFF-29032026-BRAND-FUNNEL.md    ★ ESTE FICHEIRO
├── astro.config.mjs
├── vercel.json
└── package.json
```

---

## 9. O que Falta — Accoes Pendentes

### Prioridade 1 — Para o funil funcionar

| # | Accao | Quem | Tempo | Notas |
|---|-------|------|-------|-------|
| 1 | **Formatar eBook em PDF** | Maria/Design | 2-3h | Copiar conteudo de `EBOOK-CONTENT-FULL.md` para Canva Doc (ja ha 4 templates), formatar, exportar PDF |
| 2 | **Upload PDF para o site** | Dev | 5 min | Colocar em `public/downloads/guia-viajante.pdf` |
| 3 | **Criar conta Brevo** | Maria | 30 min | Seguir `GUIA-SETUP-BREVO.md` passo a passo |
| 4 | **Trocar formulario por Brevo** | Dev | 15 min | Substituir Formsubmit pelo embed Brevo na pagina /guia |
| 5 | **Programar 5 emails no Brevo** | Maria/Dev | 1h | Copy esta pronto no doc do funil |
| 6 | **Testar funil end-to-end** | QA | 30 min | Submeter formulario → receber email → verificar PDF → todos os links |

### Prioridade 2 — Para escalar

| # | Accao | Quem | Notas |
|---|-------|------|-------|
| 7 | Escolher brandbook preferido no Canva | Eurico/Maria | 4 opcoes de apresentacao disponíveis |
| 8 | Escolher post Instagram no Canva | Eurico/Maria | 4 opcoes disponiveis |
| 9 | Recolher 3 testemunhos reais | Maria | Critico para prova social |
| 10 | Substituir imagens Unsplash por fotos reais | Dev | Maria tem fotos no Instagram |
| 11 | Registar dominio sairdacaixa.pt | DevOps | ~10 EUR/ano |
| 12 | Instalar analytics (Plausible) | Dev | Medir conversoes |
| 13 | Executar playbook de lancamento | Maria | 6 semanas — `LAUNCH-PLAYBOOK-SAIR-DA-CAIXA.md` |

---

## 10. Decisoes Tomadas nesta Sessao

| Decisao | Escolha | Alternativa Rejeitada | Razao |
|---------|---------|----------------------|-------|
| Titulo do eBook | "O Guia que a Tua Agencia Nunca Te Deu" | "Manual do Viajante" / "52 Paginas..." | Provocador, cria curiosidade, posiciona contra concorrencia |
| Voz do eBook | 1a pessoa (Maria) | Voz institucional | Cria proximidade e confianca |
| Backend email | Brevo (gratis) | Formsubmit / MailerLite | 0 EUR, automacao, formularios, 300 emails/dia |
| Logo | Cubo isometrico + aviao dourado | Bussola / Horizonte abstracto | Mais narrativo, comunica "sair da caixa" visualmente |
| Hosting | Vercel + GitHub | Apenas Vercel | Deploy automatico, repositorio publico para mostrar a Maria |
| Numero de emails nurturing | 5 emails em 21 dias | 3 ou 7 | Equilibrio entre valor e nao saturar |
| Orcamento | 25-42 EUR/mes | Sem limite | Realista para 50 EUR/mes total |

---

## 11. Metricas-Alvo (90 dias pos-lancamento)

| Metrica | Target | Ferramenta |
|---------|--------|------------|
| Emails captados | 150+ | Brevo |
| Visitas a /guia | 600+ | Plausible |
| Taxa conversao /guia | >25% | Plausible + Brevo |
| Seguidores Instagram | 29 → 200+ | Instagram Insights |
| Contactos WhatsApp | 30+ | Manual |
| Orcamentos pedidos | 5-10 | Manual |
| Viagens confirmadas | 2-3 | Manual |

### ROI Projectado

| Cenario | Emails | Orcamentos | Vendas | Receita |
|---------|--------|-----------|--------|---------|
| Pessimista | 100 | 3 | 1 | 1.000 EUR |
| Realista | 150 | 7-8 | 3 | 3.000 EUR |
| Optimista | 250 | 17 | 8-9 | 8.500 EUR |

**Mesmo no cenario pessimista, 1 venda paga o investimento de 1 ano inteiro (50 EUR x 12 = 600 EUR).**

---

## 12. Tom de Voz — Resumo Rapido

Para qualquer trabalho futuro com esta marca:

| Regra | Detalhe |
|-------|---------|
| Voz | Maria fala em 1a pessoa — directa, calorosa, honesta |
| CTA universal | "Fala comigo" (nunca "contacte-nos") |
| Precos | Sempre mencionar "voos incluidos" |
| Proibido | "comprar", "oferta imperdivel", "garantido", "facil", "curso" |
| Preferido | "descobrir", "explorar", "sair da caixa", "precos reais" |
| Lingua | PT-PT sempre (nunca PT-BR) |
| O viajante | E sempre o heroi. A Maria e a guia. |

---

## 13. Acessos e Configuracoes

| Servico | Estado | Notas |
|---------|--------|-------|
| Vercel | Producao | vooviver-mj.vercel.app — deploy automatico via GitHub |
| GitHub | Publico | github.com/DaSilvaAlves/vooviver-mj |
| Formsubmit.co | Activo | mjcsequeira@gmail.com (pagina /guia e formulario principal) |
| Brevo | **A CRIAR** | Maria precisa de criar conta (guia disponivel) |
| Canva | Activo | Logo + templates editaveis na conta do Eurico |
| Dominio custom | **PENDENTE** | sairdacaixa.pt ou similar |
| Analytics | **PENDENTE** | Plausible recomendado |

---

*HANDOFF criado em 29/03/2026*
*Sessao: Brandbook + Logo + eBook + Funil de Captacao + Campanha*
*Projecto VooViver — Sair da Caixa Viagens*
*URL: https://vooviver-mj.vercel.app*
