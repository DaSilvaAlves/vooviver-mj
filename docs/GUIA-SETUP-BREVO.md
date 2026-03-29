# Guia de Configuracao do Brevo — Sair da Caixa Viagens

**Para:** Maria Jose C. Sequeira
**Marca:** Sair da Caixa Viagens
**Data:** 29/03/2026

Este guia explica passo a passo como configurar o Brevo (antigo Sendinblue) para captar emails, enviar o Guia do Viajante automaticamente e nutrir os contactos com 5 emails ao longo de 21 dias.

Nao precisas de saber programar. Segue cada passo pela ordem indicada.

---

## Indice

1. [Criar conta gratuita no Brevo](#1-criar-conta-gratuita-no-brevo)
2. [Configurar remetente e verificar dominio](#2-configurar-remetente-e-verificar-dominio)
3. [Criar lista de contactos](#3-criar-lista-de-contactos)
4. [Carregar o PDF do guia](#4-carregar-o-pdf-do-guia)
5. [Criar formulario de captacao](#5-criar-formulario-de-captacao)
6. [Criar a sequencia automatica de 5 emails](#6-criar-a-sequencia-automatica-de-5-emails)
7. [Verificar rastreio de aberturas e cliques](#7-verificar-rastreio-de-aberturas-e-cliques)
8. [Conformidade RGPD](#8-conformidade-rgpd)

---

## 1. Criar conta gratuita no Brevo

O plano gratuito do Brevo permite enviar 300 emails por dia, criar formularios e automacoes. E mais do que suficiente para comecar.

### Passos

1. Abre o browser e vai a **https://www.brevo.com/pt/**
2. Clica no botao **"Inscrever-se gratuitamente"** (canto superior direito)
3. Preenche os campos:
   - **Email:** mjcsequeira@gmail.com
   - **Password:** escolhe uma password segura (minimo 8 caracteres, com letras e numeros)
4. Clica em **"Criar a minha conta"**
5. Vai ao Gmail e abre o email de confirmacao do Brevo — clica no link para confirmar
6. Preenche o perfil da empresa:
   - **Nome da empresa:** Sair da Caixa Viagens
   - **Site:** https://vooviver-mj.vercel.app
   - **Sector:** Turismo / Viagens
   - **Numero de contactos:** 0-250 (selecciona a opcao mais baixa)
   - **Numero de colaboradores:** So eu
7. Clica em **"Concluir"**

Vais ser encaminhada para o painel principal (dashboard) do Brevo. A conta esta criada.

---

## 2. Configurar remetente e verificar dominio

Para que os emails nao caiam no spam, precisas de verificar o teu endereco de envio.

### 2.1 Verificar o email remetente

1. No menu lateral esquerdo, clica em **"Definicoes"** (icone de roda dentada, em baixo)
2. Clica em **"Remetentes e dominios"** (ou "Senders & Domains")
3. Clica em **"Adicionar um remetente"**
4. Preenche:
   - **Nome do remetente:** Maria Jose — Sair da Caixa Viagens
   - **Email do remetente:** mjcsequeira@gmail.com
5. Clica em **"Guardar"**
6. Vai ao Gmail — receberas um email de verificacao do Brevo. Clica no link para confirmar.

Apos confirmacao, vais ver um visto verde ao lado do email na lista de remetentes.

### 2.2 Verificar dominio (opcional mas recomendado)

Se no futuro tiveres um email com dominio proprio (exemplo: maria@sairdacaixaviagens.pt), podes verificar o dominio para melhorar a entregabilidade. Por agora, com o Gmail verificado, funciona perfeitamente.

Para verificar dominio no futuro:
1. Vai a **Definicoes > Remetentes e dominios > Dominios**
2. Clica em **"Adicionar dominio"**
3. Introduz o dominio (ex: sairdacaixaviagens.pt)
4. O Brevo mostra registos DNS (DKIM, SPF) que precisas de adicionar no teu gestor de dominio
5. Apos adicionar, clica em **"Verificar"**

Por agora, avanca com o Gmail. Funciona bem para comecar.

---

## 3. Criar lista de contactos

Vais criar uma lista dedicada para quem descarrega o Guia do Viajante.

### Passos

1. No menu lateral, clica em **"Contactos"**
2. Clica em **"Listas"** (no topo da pagina)
3. Clica em **"Criar uma lista"**
4. Escreve o nome: **Guia do Viajante**
5. Na pasta, selecciona a pasta por defeito ou cria uma chamada **"Leads"**
6. Clica em **"Criar"**

Pronto. A lista aparece agora na secao de listas. Vai ficar vazia ate alguem preencher o formulario.

Toma nota do **numero da lista** (aparece ao lado do nome, ex: Lista #2). Vais precisar dele mais a frente.

---

## 4. Carregar o PDF do guia

O PDF do Guia do Viajante pode ficar alojado de duas formas. Recomendo ambas para seguranca.

### Opcao A — No site (Vercel) — Recomendado para o link nos emails

O PDF sera colocado na pasta do site pelo programador, ficando acessivel em:
```
https://vooviver-mj.vercel.app/downloads/guia-viajante-sair-da-caixa.pdf
```

Nao precisas de fazer nada aqui — o programador trata disto. Guarda este link.

### Opcao B — No Brevo (backup)

1. No menu lateral, clica em **"Campanhas"** > **"Modelos de email"**
2. Quando estiveres a criar um email (no passo 6 deste guia), podes carregar o PDF directamente no editor:
   - Clica em **"Adicionar bloco"** > **"Botao"**
   - No link do botao, clica no icone de clip (anexo) e carrega o PDF
   - O Brevo gera um link publico automaticamente

### Opcao C — Google Drive (alternativa simples)

1. Abre o Google Drive (drive.google.com)
2. Carrega o ficheiro PDF
3. Clica com o botao direito > **"Partilhar"** > **"Qualquer pessoa com o link"**
4. Copia o link

Recomendacao: usa a Opcao A (link do site) como link principal nos emails.

---

## 5. Criar formulario de captacao

Este formulario vai ser embebido na pagina /guia do site. Quando alguem o preenche, e automaticamente adicionado a lista "Guia do Viajante".

### Passos

1. No menu lateral, clica em **"Contactos"**
2. Clica em **"Formularios"** (no topo)
3. Clica em **"Criar um formulario de inscricao"**
4. Selecciona **"Formulario incorporado"** (embedded)
5. Da um nome interno: **Formulario Guia do Viajante**

### Configurar os campos

6. No editor de formulario, remove todos os campos existentes (clica no X de cada um)
7. Adiciona os campos necessarios:
   - Arrasta **"Nome"** (FIRSTNAME) para o formulario
   - Arrasta **"Email"** para o formulario
8. Configura cada campo:
   - **Nome:** Placeholder = "O teu primeiro nome" | Obrigatorio = Sim
   - **Email:** Placeholder = "O teu melhor email" | Obrigatorio = Sim
9. Texto do botao: muda para **QUERO O MEU GUIA**

### Configurar a lista de destino

10. Na seccao **"Definicoes do formulario"** (ou Settings):
    - **Lista de contactos:** selecciona **"Guia do Viajante"** (a lista que criaste no passo 3)
    - **Pagina de confirmacao:** selecciona **"Redirecionar para URL"** e escreve:
      ```
      https://vooviver-mj.vercel.app/guia/obrigado
      ```
    - **Double opt-in:** Desactivado (para simplicidade; se quiseres conformidade maxima, activa — mas o utilizador recebe um email extra de confirmacao antes de receber o guia)

### Obter o codigo HTML

11. Clica em **"Guardar e publicar"**
12. Vai aparecer uma seccao **"Codigo de integracao"** com codigo HTML
13. Copia todo o codigo HTML — vai ser algo parecido com isto:

```html
<!-- Inicio do formulario Brevo -->
<div id="sib-form-container" class="sib-form-container">
  <div id="sib-container" class="sib-container--large">
    <form id="sib-form" method="POST"
      action="https://sibforms.com/serve/AQUI_VAI_O_TEU_ID_UNICO"
      data-type="subscription">

      <div>
        <div class="sib-input sib-form-block">
          <div class="form__entry entry_block">
            <div class="form__label-row">
              <label for="FIRSTNAME">Nome</label>
            </div>
            <div class="entry__field">
              <input class="input" type="text" id="FIRSTNAME" name="FIRSTNAME"
                placeholder="O teu primeiro nome" required />
            </div>
          </div>
        </div>
      </div>

      <div>
        <div class="sib-input sib-form-block">
          <div class="form__entry entry_block">
            <div class="form__label-row">
              <label for="EMAIL">Email</label>
            </div>
            <div class="entry__field">
              <input class="input" type="email" id="EMAIL" name="EMAIL"
                placeholder="O teu melhor email" required />
            </div>
          </div>
        </div>
      </div>

      <div>
        <div class="sib-form-block" style="text-align: center;">
          <button class="sib-form-block__button sib-form-block__button-with-loader"
            type="submit">
            QUERO O MEU GUIA
          </button>
        </div>
      </div>

      <input type="text" name="email_address_check" value="" class="input--hidden" />
      <input type="hidden" name="locale" value="pt" />
    </form>
  </div>
</div>
<!-- Fim do formulario Brevo -->
```

14. Envia este codigo ao programador — ele integra-o na pagina /guia do site

**Nota:** O campo `email_address_check` e o honeypot anti-spam do Brevo. E invisivel para utilizadores reais mas apanha bots.

---

## 6. Criar a sequencia automatica de 5 emails

Esta e a parte mais importante. Vais criar uma automacao que envia 5 emails automaticamente ao longo de 21 dias a cada pessoa que descarrega o guia.

### 6.1 Criar a automacao

1. No menu lateral, clica em **"Automacao"** (ou "Automation")
2. Clica em **"Criar uma automacao"**
3. Selecciona **"Criar de raiz"** (nao uses os templates pre-feitos)
4. Da um nome: **Sequencia Guia do Viajante**
5. Clica em **"Criar"**

### 6.2 Definir o trigger (gatilho)

6. No editor visual, clica em **"Adicionar ponto de entrada"**
7. Selecciona **"Um contacto e adicionado a uma lista"**
8. Escolhe a lista: **Guia do Viajante**
9. Clica em **"OK"** ou **"Guardar"**

### 6.3 Adicionar o Email 1 (D+0 — imediato)

10. Clica no **"+"** abaixo do trigger
11. Selecciona **"Enviar um email"**
12. Clica em **"Criar um modelo de email"** (ou selecciona um ja existente)
13. Escolhe um template basico/simples (fundo branco, sem muitas imagens)
14. Preenche:
    - **Assunto:** O teu Guia do Viajante esta aqui — boas viagens!
    - **Preview text:** 52 paginas para viajares melhor, mais barato e sem stress.
    - **Remetente:** Maria Jose — Sair da Caixa Viagens (mjcsequeira@gmail.com)

15. No editor de email, escreve o seguinte conteudo:

---

**CONTEUDO DO EMAIL 1 — "Aqui esta o teu guia"**

> Ola {{ contact.FIRSTNAME }},
>
> Obrigada por quereres este guia. Levei semanas a escreve-lo e meti tudo o que sei la dentro — sem guardar nada para mim.
>
> Aqui esta:
>
> **[BOTAO: DESCARREGAR O GUIA]**
> *(Link do botao: https://vooviver-mj.vercel.app/downloads/guia-viajante-sair-da-caixa.pdf)*
>
> Podes le-lo no telemovel, no computador, ou imprimir as checklists (capitulos 5 e 6 — vao ser-te muito uteis).
>
> Se tiveres alguma pergunta, responde a este email ou envia-me mensagem no WhatsApp (+351 933 096 770). Respondo pessoalmente.
>
> Boas viagens,
> Maria Jose
>
> ---
> Sair da Caixa Viagens
> @sairdacaixa.viagens
> vooviver-mj.vercel.app

---

16. Guarda o modelo de email
17. De volta a automacao, o Email 1 ja esta ligado ao trigger

### 6.4 Adicionar espera de 3 dias + Email 2

18. Clica no **"+"** abaixo do Email 1
19. Selecciona **"Adicionar um atraso"**
20. Define: **3 dias**
21. Clica no **"+"** abaixo do atraso
22. Selecciona **"Enviar um email"**
23. Cria um novo modelo com:
    - **Assunto:** Os 10 destinos que mais surpreendem os portugueses
    - **Preview text:** Sabias que podes ver gorilas na natureza por menos de 3.000 EUR?

---

**CONTEUDO DO EMAIL 2 — "Ja leste o capitulo 11?"**

> Ola {{ contact.FIRSTNAME }},
>
> Espero que estejas a gostar do guia.
>
> Se so pudesses ler uma parte, le o capitulo 11 — os 10 destinos incriveis que custam menos do que pensas.
>
> O que mais surpreende as pessoas:
>
> → **Uganda/Ruanda** (ver gorilas): 2.950 EUR com voos
> (as agencias cobram quase 10.000 EUR pelo mesmo)
>
> → **Socotra**: 1.880 EUR — o destino mais extraordinario que existe. E eu sou a unica em Portugal que o oferece.
>
> → **Marrocos completo**: 870 EUR com voos
> (a concorrencia pede 2.595 EUR)
>
> Estes sao precos reais de viagens de grupo que eu organizo. Tudo incluido. Sem letras pequenas.
>
> Queres saber mais sobre algum deles?
> Responde a este email ou fala comigo no WhatsApp.
>
> Maria Jose

---

### 6.5 Adicionar espera de 4 dias + Email 3

24. Clica no **"+"** abaixo do Email 2
25. Selecciona **"Adicionar um atraso"**
26. Define: **4 dias** (D+3 + 4 = D+7)
27. Clica no **"+"** e selecciona **"Enviar um email"**
28. Cria um novo modelo com:
    - **Assunto:** "Maria, como e que os teus precos sao tao baixos?"
    - **Preview text:** Nao e magia. E matematica. Deixa-me explicar.

---

**CONTEUDO DO EMAIL 3 — "A pergunta que toda a gente me faz"**

> Ola {{ contact.FIRSTNAME }},
>
> A pergunta que mais recebo e: "Como e possivel estes precos?"
>
> A resposta e simples:
>
> 1. **Trabalho directamente com operadores locais**
>    (sem 3 intermediarios a cobrar margem)
>
> 2. **Negocio precos de grupo** (15-25 pessoas)
>    (volume = descontos que individuais nao conseguem)
>
> 3. **Escolho destinos fora do mainstream**
>    (menos procura turistica = precos mais honestos)
>
> 4. **Nao tenho loja no shopping a pagar renda**
>    (os meus custos sao os teus precos baixos)
>
> Isto nao e low-cost. Nao e mau servico. E o preco justo sem a gordura desnecessaria.
>
> Se algum dia quiseres comparar, pede orcamento a qualquer agencia para o mesmo destino e periodo. Depois fala comigo.
>
> O choque vai ser real.
>
> Maria Jose
>
> P.S. Explico tudo isto no capitulo 1 do guia — "Como funcionam realmente os precos das viagens." Se ainda nao leste, vale muito a pena.

---

### 6.6 Adicionar espera de 7 dias + Email 4

29. Clica no **"+"** abaixo do Email 3
30. Selecciona **"Adicionar um atraso"**
31. Define: **7 dias** (D+7 + 7 = D+14)
32. Clica no **"+"** e selecciona **"Enviar um email"**
33. Cria um novo modelo com:
    - **Assunto:** O que aconteceu quando levei o primeiro grupo a Uganda
    - **Preview text:** Nao vou mentir — estava nervosa. Mas o resultado...

---

**CONTEUDO DO EMAIL 4 — "Uma historia real"**

> Ola {{ contact.FIRSTNAME }},
>
> Quero contar-te uma historia.
>
> Quando organizei o meu primeiro grupo para Uganda, estava nervosa. Eram 18 pessoas que confiaram em mim sem nunca me terem visto pessoalmente.
>
> Preparei tudo ao detalhe: voos, alojamentos, guias locais, os permits para ver os gorilas. Revisei tudo tres vezes. Mesmo assim, na vespera do voo, nao dormi.
>
> Quando chegamos ao Bwindi e vimos a primeira familia de gorilas de montanha, vi 36 olhos a brilhar. O silencio era absoluto. Ninguem queria respirar de mais. A Ana disse-me ao ouvido: "Maria, isto e o melhor dia da minha vida."
>
> Voltaram todos a perguntar: "Quando e a proxima?"
>
> E para isto que faco o que faco. Nao e pelo dinheiro. E por ver as pessoas a viver algo que nunca imaginaram ser possivel — e a um preco que nunca imaginaram pagar.
>
> Se quiseres viver algo parecido, os proximos grupos estao a formar-se. Fala comigo — mostro-te as opcoes.
>
> Maria Jose

---

### 6.7 Adicionar espera de 7 dias + Email 5

34. Clica no **"+"** abaixo do Email 4
35. Selecciona **"Adicionar um atraso"**
36. Define: **7 dias** (D+14 + 7 = D+21)
37. Clica no **"+"** e selecciona **"Enviar um email"**
38. Cria um novo modelo com:
    - **Assunto:** Os proximos destinos estao quase cheios
    - **Preview text:** Uganda a 2.950 EUR. Socotra a 1.880 EUR. Vagas limitadas.

---

**CONTEUDO DO EMAIL 5 — "Proximos grupos — queres vir?"**

> Ola {{ contact.FIRSTNAME }},
>
> Ha 3 semanas enviei-te o Guia do Viajante. Espero que te tenha sido tao util como quis que fosse.
>
> Hoje escrevo-te porque os proximos grupos estao a formar-se — e quero que tenhas a oportunidade de vir.
>
> **PROXIMAS VIAGENS:**
>
> → **Uganda/Ruanda** (ver gorilas): Outubro 2026 — desde 2.950 EUR
> 12 dias com voos, alojamento, guias e permits incluidos
>
> → **Socotra** (Iemen): Novembro 2026 — desde 1.880 EUR
> O destino mais extraordinario do mundo. Unica operadora em Portugal.
>
> → **Marrocos completo**: Setembro 2026 — desde 870 EUR
> 9 dias com voos. Deserto, medinas, Atlas — tudo incluido.
>
> Todos os precos incluem voos. Os grupos sao de 15 a 25 pessoas. As vagas preenchem-se por ordem de inscricao.
>
> Se algum destes destinos te chamou a atencao, envia-me mensagem e eu envio-te o programa completo:
>
> **[BOTAO: FALAR COM A MARIA NO WHATSAPP]**
> *(Link: https://wa.me/351933096770?text=Ola%20Maria%2C%20vi%20o%20email%20dos%20proximos%20destinos%20e%20gostava%20de%20saber%20mais.)*
>
> **[BOTAO: VER TODOS OS DESTINOS NO SITE]**
> *(Link: https://vooviver-mj.vercel.app/#destinations)*
>
> Obrigada por confiares em mim.
>
> Maria Jose
>
> ---
> Sair da Caixa Viagens
> Consultora associada VooViver — RNAVT N.12366

---

### 6.8 Activar a automacao

39. Revisa toda a sequencia no editor visual. Deve ficar assim:

```
[Contacto adicionado a lista "Guia do Viajante"]
    |
    ▼
[Enviar Email 1 — "Aqui esta o teu guia"]
    |
    ▼
[Esperar 3 dias]
    |
    ▼
[Enviar Email 2 — "Ja leste o capitulo 11?"]
    |
    ▼
[Esperar 4 dias]
    |
    ▼
[Enviar Email 3 — "A pergunta que toda a gente me faz"]
    |
    ▼
[Esperar 7 dias]
    |
    ▼
[Enviar Email 4 — "Uma historia real"]
    |
    ▼
[Esperar 7 dias]
    |
    ▼
[Enviar Email 5 — "Proximos grupos — queres vir?"]
```

40. Clica em **"Activar"** (canto superior direito)
41. Confirma a activacao

A automacao esta agora activa. Cada vez que alguem preencher o formulario e entrar na lista "Guia do Viajante", vai receber os 5 emails automaticamente.

---

## 7. Verificar rastreio de aberturas e cliques

O Brevo rastreia aberturas e cliques automaticamente. Nao precisas de configurar nada extra.

### O que e rastreado automaticamente

| Metrica | Como funciona |
|---------|---------------|
| **Aberturas** | Um pixel invisivel no email detecta quando alguem o abre |
| **Cliques** | Os links no email sao rastreados automaticamente |
| **Bounces** | Emails que nao foram entregues (endereco errado, caixa cheia) |
| **Cancelamentos** | Quem clicou em "Cancelar subscricao" |

### Onde ver as estatisticas

1. Vai a **"Automacao"** no menu lateral
2. Clica na automacao **"Sequencia Guia do Viajante"**
3. Em cada email, vais ver:
   - **Taxa de abertura** (objectivo: acima de 40%)
   - **Taxa de clique** (objectivo: acima de 8%)
   - **Bounces e cancelamentos**

### Onde ver estatisticas por contacto

1. Vai a **"Contactos"**
2. Clica no nome de um contacto
3. Vais ver o historico: que emails recebeu, quais abriu, onde clicou

### Dica importante

Se a taxa de abertura estiver abaixo de 30%, experimenta mudar o assunto do email. O Brevo permite editar os modelos a qualquer momento sem desactivar a automacao.

---

## 8. Conformidade RGPD

O RGPD (Regulamento Geral de Proteccao de Dados) e obrigatorio na Europa. Aqui esta o que precisas de garantir:

### 8.1 Link de cancelamento de subscricao (obrigatorio)

O Brevo adiciona automaticamente um link de **"Cancelar subscricao"** no rodape de todos os emails enviados. Nao o remova nunca. E obrigatorio por lei.

### 8.2 Texto de consentimento no formulario

Abaixo do botao "QUERO O MEU GUIA", adiciona este texto:

> Ao submeter este formulario, aceitas receber o Guia do Viajante e emails com dicas de viagem da Sair da Caixa Viagens. Podes cancelar a qualquer momento atraves do link em cada email. Os teus dados sao tratados com respeito e nunca partilhados com terceiros. Consulta a nossa [Politica de Privacidade].

Para adicionar isto no formulario do Brevo:
1. Edita o formulario
2. Arrasta um bloco de **"Texto"** para baixo do botao
3. Escreve o texto acima
4. Guarda

### 8.3 Politica de Privacidade

Precisas de ter uma pagina de Politica de Privacidade no site. Pode ser simples. Deve incluir:

- Que dados recolhes (nome e email)
- Para que os usas (enviar o guia e emails informativos sobre viagens)
- Onde ficam guardados (Brevo, servidores na Europa)
- Como cancelar (link em cada email ou contacto directo)
- Contacto do responsavel (mjcsequeira@gmail.com)

O programador pode criar esta pagina em `/privacidade` no site.

### 8.4 Regras de retencao

- Se um contacto cancelar a subscricao, o Brevo bloqueia-o automaticamente
- Nao envies emails a quem cancelou — o Brevo ja trata disso
- Se alguem pedir para apagar os dados, vai a Contactos, encontra a pessoa e clica em **"Apagar"**

### Checklist RGPD

| Requisito | Estado |
|-----------|--------|
| Link de cancelamento em todos os emails | Automatico (Brevo) |
| Texto de consentimento no formulario | A adicionar |
| Pagina de Politica de Privacidade | A criar |
| Possibilidade de apagar dados | Sim (manual no Brevo) |
| Dados guardados na Europa | Sim (Brevo tem servidores na UE) |

---

## Resumo — Lista de verificacao final

Depois de seguir todos os passos, confirma que tens tudo:

| Passo | Feito? |
|-------|--------|
| Conta Brevo criada e email confirmado | [ ] |
| Remetente verificado (mjcsequeira@gmail.com) | [ ] |
| Lista "Guia do Viajante" criada | [ ] |
| PDF do guia carregado/disponivel via link | [ ] |
| Formulario criado e publicado | [ ] |
| Codigo HTML do formulario enviado ao programador | [ ] |
| Email 1 (D+0) — "Aqui esta o teu guia" configurado | [ ] |
| Email 2 (D+3) — "Ja leste o capitulo 11?" configurado | [ ] |
| Email 3 (D+7) — "A pergunta que toda a gente me faz" configurado | [ ] |
| Email 4 (D+14) — "Uma historia real" configurado | [ ] |
| Email 5 (D+21) — "Proximos grupos — queres vir?" configurado | [ ] |
| Automacao activada | [ ] |
| Texto RGPD no formulario | [ ] |
| Politica de Privacidade no site | [ ] |

---

## Contactos e links uteis

| Recurso | Link / Contacto |
|---------|-----------------|
| Painel Brevo | https://app.brevo.com |
| Site | https://vooviver-mj.vercel.app |
| Pagina do guia | https://vooviver-mj.vercel.app/guia |
| WhatsApp Maria | +351 933 096 770 |
| Instagram | @sairdacaixa.viagens |
| Email Maria | mjcsequeira@gmail.com |
| Suporte Brevo | https://help.brevo.com/hc/pt |

---

## Duvidas frequentes

**P: E se alguem nao receber o email?**
R: Pede-lhe para verificar a pasta de spam/lixo. Se nao estiver la, vai a Contactos no Brevo e verifica se o email esta na lista. Se estiver, reenvia manualmente.

**P: Posso editar os emails depois de activar a automacao?**
R: Sim. Vai a Automacao, clica no email que queres editar, faz as alteracoes e guarda. As alteracoes aplicam-se apenas a quem ainda nao recebeu esse email.

**P: Quantos emails posso enviar por dia no plano gratuito?**
R: 300 por dia. Para comecar e mais do que suficiente. Se ultrapassares este limite, o Brevo tem planos pagos a partir de 7 EUR/mes.

**P: Preciso de actualizar os destinos e precos no Email 5?**
R: Sim. Cada vez que os destinos ou datas mudarem, edita o Email 5 na automacao com a informacao actualizada.

**P: Posso adicionar mais emails a sequencia?**
R: Sim. Basta abrir a automacao, clicar no "+" no final e adicionar um novo atraso + email.

---

*Guia de Configuracao Brevo v1.0 — Sair da Caixa Viagens*
*Custo: 0 EUR (plano gratuito)*
