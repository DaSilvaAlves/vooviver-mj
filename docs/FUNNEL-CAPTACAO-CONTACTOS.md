# FUNIL DE CAPTACAO DE CONTACTOS — Sair da Caixa Viagens

**Objectivo:** Captar emails em troca do eBook gratuito, nutrir leads com valor, converter em contacto directo (WhatsApp/formulario).
**Orcamento:** 50 EUR/mes
**Data:** 29/03/2026

---

## 1. Arquitectura do Funil

```
    ┌─────────────────────────────────────────────────┐
    │              FONTES DE TRAFEGO                   │
    │  Instagram (organico) + WhatsApp + Boca-a-boca  │
    │  + Landing page existente + Google (futuro)      │
    └──────────────────┬──────────────────────────────┘
                       ▼
    ┌─────────────────────────────────────────────────┐
    │          LANDING PAGE DO EBOOK                   │
    │  vooviver-mj.vercel.app/guia                    │
    │                                                  │
    │  "O Guia que a Tua Agencia Nunca Te Deu"        │
    │  52 paginas GRATIS — so precisas do teu email   │
    │                                                  │
    │  [Nome] [Email] [QUERO O GUIA]                  │
    └──────────────────┬──────────────────────────────┘
                       ▼
    ┌─────────────────────────────────────────────────┐
    │          PAGINA DE OBRIGADO                      │
    │  vooviver-mj.vercel.app/guia/obrigado           │
    │                                                  │
    │  "O guia esta no teu email!"                    │
    │  + CTA: "Enquanto esperas, ve os destinos       │
    │    que tenho disponiveis" → link para destinos   │
    │  + CTA: "Segue-me no Instagram" → link          │
    │  + CTA: "Junta-te ao WhatsApp" → link           │
    └──────────────────┬──────────────────────────────┘
                       ▼
    ┌─────────────────────────────────────────────────┐
    │          EMAIL AUTOMATICO (D+0)                  │
    │  "Aqui esta o teu guia — boas viagens!"         │
    │  + PDF em anexo ou link de download              │
    │  + Assinatura da Maria                           │
    └──────────────────┬──────────────────────────────┘
                       ▼
    ┌─────────────────────────────────────────────────┐
    │          SEQUENCIA DE NURTURING                  │
    │  5 emails ao longo de 21 dias                    │
    │  (ver seccao 4 para detalhe)                     │
    └──────────────────┬──────────────────────────────┘
                       ▼
    ┌─────────────────────────────────────────────────┐
    │          CONVERSAO                               │
    │  WhatsApp directo / Formulario na landing page   │
    │  → Maria responde pessoalmente em <4h            │
    └─────────────────────────────────────────────────┘
```

---

## 2. Landing Page do eBook — Especificacao

### 2.1 URL e Rota

- **URL:** `vooviver-mj.vercel.app/guia`
- **Implementacao:** Nova pagina Astro em `src/pages/guia.astro`
- **Pagina de obrigado:** `src/pages/guia/obrigado.astro`

### 2.2 Estrutura da Pagina

```
┌────────────────────────────────────────────┐
│ HEADER (simplificado — logo + link home)   │
├────────────────────────────────────────────┤
│                                            │
│  HERO                                      │
│  ┌──────────────────┬───────────────────┐  │
│  │                  │                   │  │
│  │  Badge: GRATIS   │  [IMAGEM/MOCKUP  │  │
│  │                  │   DO EBOOK]       │  │
│  │  H1: O Guia que  │                   │  │
│  │  a Tua Agencia   │                   │  │
│  │  Nunca Te Deu    │                   │  │
│  │                  │                   │  │
│  │  Subtitulo:      │                   │  │
│  │  52 paginas com  │                   │  │
│  │  tudo o que      │                   │  │
│  │  precisas...     │                   │  │
│  │                  │                   │  │
│  │  [FORMULARIO]    │                   │  │
│  │  Nome | Email    │                   │  │
│  │  [QUERO O GUIA]  │                   │  │
│  │                  │                   │  │
│  └──────────────────┴───────────────────┘  │
│                                            │
├────────────────────────────────────────────┤
│                                            │
│  O QUE VAIS APRENDER (bullet points)       │
│                                            │
│  ✓ Porque pagas 70% a mais sem saber       │
│  ✓ Quando reservar para poupar centenas    │
│  ✓ 10 destinos incriveis que custam        │
│    menos do que pensas                     │
│  ✓ Checklist completa para nao             │
│    esqueceres nada                         │
│  ✓ Como evitar armadilhas de cambio        │
│  ✓ Seguro de viagem: o essencial           │
│                                            │
├────────────────────────────────────────────┤
│                                            │
│  QUEM E A MARIA (mini bio + foto)          │
│                                            │
│  "Sou consultora de viagens de grupo.      │
│   Levo portugueses a destinos que 99%      │
│   das agencias nao conhecem — a precos     │
│   que nao vao acreditar. Este guia tem     │
│   tudo o que aprendi."                     │
│                                            │
├────────────────────────────────────────────┤
│                                            │
│  FORMULARIO REPETIDO (para quem scrollou)  │
│  Nome | Email | [QUERO O GUIA]             │
│                                            │
├────────────────────────────────────────────┤
│  FOOTER (minimo — logo + RNAVT)            │
└────────────────────────────────────────────┘
```

### 2.3 Copy da Landing Page

**Badge:** `GRATIS — 52 PAGINAS`

**H1:** O Guia que a Tua Agencia Nunca Te Deu

**Subtitulo:** 52 paginas com tudo o que precisas de saber para viajar melhor, mais barato e sem stress. Sem truques. Sem cartao de credito. So o teu email.

**CTA do botao:** QUERO O MEU GUIA

**Texto sob o formulario:** Recebemos o teu email com respeito. Zero spam, promessa da Maria.

**Bullet points (seccao "O que vais aprender"):**
- Como funcionam realmente os precos das viagens (e porque pagas ate 70% a mais)
- A melhor altura para reservar cada tipo de viagem
- Viagem solo vs grupo: a verdade que ninguem te conta
- 7 perguntas que deves fazer ANTES de pagar a qualquer agencia
- Checklist completa: documentos, malas, saude, dinheiro
- A armadilha do cambio no aeroporto (e como evitar)
- 10 destinos incriveis que custam menos do que pensas — com precos reais
- Modelo de orcamento de viagem (pronto a preencher)

### 2.4 Formulario — Campos

| Campo | Tipo | Obrigatorio | Placeholder |
|-------|------|-------------|-------------|
| Nome | text | Sim | O teu primeiro nome |
| Email | email | Sim | O teu melhor email |
| Honeypot | hidden | — | Anti-spam (invisivel) |

**Botao:** QUERO O MEU GUIA (gold, glow, full width no mobile)

### 2.5 Backend do Formulario

**Opcao A — Formsubmit.co (gratis, ja em uso)**

```
POST https://formsubmit.co/mjcsequeira@gmail.com
_subject: "Novo pedido do Guia do Viajante"
_next: https://vooviver-mj.vercel.app/guia/obrigado
_autoresponse: Email automatico com link para o PDF
```

Limitacao: Formsubmit.co envia autoresposta simples. Para email sequence, precisa de solucao dedicada.

**Opcao B — Brevo (ex-Sendinblue) — RECOMENDADO**

| Aspecto | Detalhe |
|---------|---------|
| Plano gratuito | 300 emails/dia, formularios, automacao basica |
| Custo | 0 EUR (dentro do orcamento) |
| Funcionalidades | Formulario embeddable, autoresposta com PDF, email sequence de 5 emails |
| Integracao | Formulario HTML embebido na pagina Astro |

**Opcao C — MailerLite (alternativa)**

| Aspecto | Detalhe |
|---------|---------|
| Plano gratuito | 1.000 subscritores, 12.000 emails/mes |
| Custo | 0 EUR (ate 1.000 subscritores) |
| Funcionalidades | Landing pages, automacao, formularios |

**Recomendacao:** Brevo — gratuito, permite automacao de emails, formularios integraveis, e tem interface em portugues.

---

## 3. Pagina de Obrigado — Especificacao

### URL: `/guia/obrigado`

**Copy:**

```
[Icone check verde]

O guia esta a caminho do teu email!

Verifica a caixa de entrada (e o spam, por precaucao).
Se nao receberes em 5 minutos, envia-me mensagem.

---

Enquanto esperas, que tal conheceres os destinos
que tenho disponiveis para os proximos meses?

[VER DESTINOS] → link para seccao destinos da landing page

Ou segue-me para novidades em primeira mao:

[Instagram] @sairdacaixa.viagens
[WhatsApp] Fala comigo directamente
```

**Objectivo triplo:**
1. Confirmar que o email foi enviado
2. Direccionar para a landing page principal (ver destinos)
3. Captar seguidor no Instagram / contacto WhatsApp

---

## 4. Sequencia de Email Nurturing (5 emails, 21 dias)

### Configuracao Tecnica

| Parametro | Valor |
|-----------|-------|
| Ferramenta | Brevo (gratuito) |
| Trigger | Submissao do formulario |
| Remetente | Maria Jose — Sair da Caixa Viagens |
| Reply-to | mjcsequeira@gmail.com |
| Unsubscribe | Automatico (obrigatorio RGPD) |

---

### EMAIL 1 — D+0 (imediato): "Aqui esta o teu guia"

**Assunto:** O teu Guia do Viajante esta aqui — boas viagens!
**Preview:** 52 paginas para viajares melhor, mais barato e sem stress.

```
Ola [NOME],

Obrigada por quereres este guia. Levei semanas a escreve-lo
e meti tudo o que sei la dentro — sem guardar nada para mim.

Aqui esta:
[BOTAO: DESCARREGAR O GUIA] → link para PDF

Podes le-lo no telemovel, no computador, ou imprimir
as checklists (capitulos 5 e 6 — vao ser-te muito uteis).

Se tiveres alguma pergunta, responde a este email
ou envia-me mensagem no WhatsApp (+351 933 096 770).
Respondo pessoalmente.

Boas viagens,
Maria Jose

—
Sair da Caixa Viagens
@sairdacaixa.viagens
vooviver-mj.vercel.app
```

---

### EMAIL 2 — D+3: "Ja leste o capitulo 11?"

**Assunto:** Os 10 destinos que mais surpreendem os portugueses
**Preview:** Sabias que podes ver gorilas na natureza por menos de 3.000 EUR?

```
Ola [NOME],

Espero que estejas a gostar do guia.

Se so pudesses ler uma parte, le o capitulo 11 — os 10
destinos incriveis que custam menos do que pensas.

O que mais surpreende as pessoas:

→ Uganda/Ruanda (ver gorilas): 2.950 EUR com voos
  (as agencias cobram quase 10.000 EUR pelo mesmo)

→ Socotra: 1.880 EUR — o destino mais extraordinario
  que existe. E eu sou a unica em Portugal que o oferece.

→ Marrocos completo: 870 EUR com voos
  (a concorrencia pede 2.595 EUR)

Estes sao precos reais de viagens de grupo que eu organizo.
Tudo incluido. Sem letras pequenas.

Queres saber mais sobre algum deles?
Responde a este email ou fala comigo no WhatsApp.

Maria Jose
```

---

### EMAIL 3 — D+7: "A pergunta que toda a gente me faz"

**Assunto:** "Maria, como e que os teus precos sao tao baixos?"
**Preview:** Nao e magia. E matematica. Deixa-me explicar.

```
Ola [NOME],

A pergunta que mais recebo e: "Como e possivel estes precos?"

A resposta e simples:

1. Trabalho directamente com operadores locais
   (sem 3 intermediarios a cobrar margem)

2. Negocio precos de grupo (15-25 pessoas)
   (volume = descontos que individuais nao conseguem)

3. Escolho destinos fora do mainstream
   (menos procura turistica = precos mais honestos)

4. Nao tenho loja no shopping a pagar renda
   (os meus custos sao os teus precos baixos)

Isto nao e low-cost. Nao e mau servico. E o preco justo
sem a gordura desnecessaria.

Se algum dia quiseres comparar, pede orcamento a qualquer
agencia para o mesmo destino e periodo. Depois fala comigo.

O choque vai ser real.

Maria Jose

P.S. Explico tudo isto no capitulo 1 do guia — "Como
funcionam realmente os precos das viagens." Se ainda nao
leste, vale muito a pena.
```

---

### EMAIL 4 — D+14: "Uma historia real"

**Assunto:** O que aconteceu quando levei o primeiro grupo a [destino]
**Preview:** Nao vou mentir — estava nervosa. Mas o resultado...

```
Ola [NOME],

Quero contar-te uma historia.

[Nota: adaptar com historia real da Maria — primeira viagem
de grupo que organizou, emocoes, o que correu bem, o que
aprendeu, como os viajantes reagiram]

Exemplo de estrutura:
- Setup: "Quando organizei o meu primeiro grupo para
  [destino], estava nervosa. Eram [X] pessoas que
  confiaram em mim."
- Momento: "Quando chegamos a [lugar], vi [X] olhos
  a brilhar. O [nome] disse: '[citacao]'. A [nome]
  nao largou a camara durante 3 dias."
- Resultado: "Voltaram todos a perguntar: quando e
  a proxima?"
- Reflexao: "E para isto que faco o que faco. Nao e
  pelo dinheiro. E por ver as pessoas a viver algo
  que nunca imaginaram."

Se quiseres viver algo parecido, os proximos grupos
estao a formar-se. Fala comigo — mostro-te as opcoes.

Maria Jose
```

---

### EMAIL 5 — D+21: "Proximos grupos — queres vir?"

**Assunto:** Os proximos destinos estao quase cheios
**Preview:** [Destino] a [preco] EUR. Vagas limitadas.

```
Ola [NOME],

Ha 3 semanas enviei-te o Guia do Viajante. Espero que
te tenha sido tao util como quis que fosse.

Hoje escrevo-te porque os proximos grupos estao a
formar-se — e quero que tenhas a oportunidade de vir.

PROXIMAS VIAGENS:

→ [Destino 1]: [data] — desde [preco] EUR
  [1 frase sobre o destino]

→ [Destino 2]: [data] — desde [preco] EUR
  [1 frase sobre o destino]

→ [Destino 3]: [data] — desde [preco] EUR
  [1 frase sobre o destino]

Todos os precos incluem voos. Os grupos sao de [X-Y]
pessoas. As vagas preenchem-se por ordem de inscricao.

Se algum destes destinos te chamou a atencao, envia-me
mensagem e eu envio-te o programa completo:

[BOTAO: FALAR COM A MARIA NO WHATSAPP]
[BOTAO: VER TODOS OS DESTINOS NO SITE]

Obrigada por confiares em mim.

Maria Jose

—
Sair da Caixa Viagens
Consultora associada VooViver — RNAVT N.12366
```

---

## 5. Hosting do PDF

| Opcao | Como | Custo |
|-------|------|-------|
| **Brevo (recomendado)** | Upload do PDF no Brevo, link no email automatico | 0 EUR |
| **Google Drive** | Upload, partilhar com link publico | 0 EUR |
| **Vercel (static)** | Colocar PDF em `/public/` do projecto Astro | 0 EUR |

**Recomendacao:** Vercel — PDF em `public/downloads/guia-viajante-sair-da-caixa.pdf`. Link directo, rapido, sem dependencia de terceiros.

---

## 6. Metricas do Funil

| Metrica | Ferramenta | Target (3 meses) |
|---------|------------|-------------------|
| Visitas a /guia | Plausible/GA | 200+/mes |
| Taxa de conversao (visita → email) | Brevo + Plausible | >25% |
| Emails captados | Brevo | 50+/mes |
| Taxa de abertura email sequence | Brevo | >40% |
| Taxa de clique nos emails | Brevo | >8% |
| Respostas ao email (replies) | Gmail | 5+/mes |
| Contactos WhatsApp gerados | Manual | 10+/mes |
| Conversoes em orcamento | Manual | 3-5/mes |

---

## 7. Implementacao Tecnica — Resumo

### Ficheiros a Criar

| Ficheiro | Descricao |
|----------|-----------|
| `src/pages/guia.astro` | Landing page do eBook |
| `src/pages/guia/obrigado.astro` | Pagina de obrigado pos-download |
| `src/components/EbookHero.astro` | Hero da pagina do eBook |
| `src/components/EbookForm.astro` | Formulario de captacao (Brevo embed) |
| `src/components/EbookBenefits.astro` | Seccao "O que vais aprender" |
| `public/downloads/guia-viajante-sair-da-caixa.pdf` | O PDF do eBook |

### Integracao com Brevo

```html
<!-- Formulario Brevo embebido -->
<form
  action="https://sibforms.com/serve/FORM_ID"
  method="POST"
  class="sib-form"
>
  <input type="text" name="FIRSTNAME" placeholder="O teu primeiro nome" required />
  <input type="email" name="EMAIL" placeholder="O teu melhor email" required />
  <input type="hidden" name="locale" value="pt" />
  <input type="hidden" name="html_type" value="simple" />
  <button type="submit" class="btn-primary w-full">QUERO O MEU GUIA</button>
</form>
```

### SEO da Pagina /guia

| Meta | Valor |
|------|-------|
| Title | Guia Gratis do Viajante — Sair da Caixa Viagens |
| Description | Descarrega gratis o guia de 52 paginas com tudo o que precisas para viajar melhor, mais barato e sem stress. Por Maria Jose Sequeira. |
| OG Image | Mockup do eBook (capa) |
| Schema | WebPage + Offer (preco: 0) |

---

## 8. Fluxo Completo — Visao de Utilizador

```
1. Sofia ve post no Instagram da Maria com destino a bom preco
2. Clica no link da bio → landing page principal
3. Fica curiosa mas nao esta pronta para pedir orcamento
4. Ve banner/link para "Guia Gratis" → clica → /guia
5. Le a pagina, ve o que vai aprender, confia na Maria
6. Preenche: "Sofia" + "sofia@email.pt" → [QUERO O MEU GUIA]
7. Redireccionada para /guia/obrigado
8. Segue a Maria no Instagram (CTA na pagina de obrigado)
9. Recebe email D+0 com o PDF → le no dia seguinte
10. Recebe email D+3 → surpreende-se com precos dos destinos
11. Recebe email D+7 → percebe porque os precos sao possiveis
12. Recebe email D+14 → conecta-se emocionalmente com a historia
13. Recebe email D+21 → ve um destino que quer, clica no WhatsApp
14. Maria responde em <4h com programa completo
15. Sofia reserva Uganda/Ruanda por 2.950 EUR
16. Volta de viagem → da testemunho → indica 3 amigas
17. O ciclo repete-se.
```

---

*Funil de Captacao v1.0 — Sair da Caixa Viagens*
*Custo total: 0 EUR (ferramentas gratuitas)*
*Tempo de implementacao estimado: 1-2 sessoes de desenvolvimento*
