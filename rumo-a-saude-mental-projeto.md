# Rumo à Saúde Mental — projeto completo (frases + dinâmica)

Documento para análise. Levantado direto do código (`index.html`) da **v4** (05/11/2026). As mudanças de cada versão estão na seção 0. Versões antigas seguem jogáveis em `/v2/` e `/v3/`.
Jogo no ar: https://hyratecnologia.github.io/rumo-ao-bem-estar/
Código: https://github.com/hyratecnologia/rumo-ao-bem-estar

---

## 0. Histórico de mudanças

### v4 (05/11/2026)

| # | O que mudou |
|---|---|
| 1 | O medidor **voltou a ser "dificuldade"** (FÁCIL, NORMAL, DIFÍCIL, MUITO DIFÍCIL, EXTREMA, EXTREMA+) |
| 2 | **Partida mais longa** (cerca de 3 min): multidão aos 25 s, chefão aos 60 s, final em até 180 s |
| 3 | A escolha de personagem **abre aleatória**. Ao clicar em "nascer", um **sorteio** ("VOCÊ NÃO ESCOLHE.") define quem nasce |
| 4 | Pessoas de máscara **mais diversas** (inclusive negras) e **variadas**: corrida, selfie no meio do caminho, patins, moto, carro de luxo, jato |
| 5 | **Chefão em foco**: os mascarados saem de cena, a multidão fica quieta, as falas dele aparecem maiores, e ele é desenhado **na frente** do cenário |
| 6 | **Tela de bônus** quando o(a) psicólogo(a) chega |
| 7 | **Final**: o chefão sai de cena e só ficam as pessoas que ajudam. **No máximo 8 cargas** no chão e **2 por ajudante**. O(a) psicólogo(a) fica **visível**, ao lado da personagem |
| 8 | **Obstáculos criativos e animados** para cada barreira comum |
| 9 | **Tela de fim**: cargas carregadas, recursos de ajuda (CVV 188 e chat, CAPS/UBS, serviço-escola) e aviso de que é um joguinho representativo |
| 10 | **Capa com várias pessoas diferentes**, cada uma com sua pilha |
| 11 | **Balões de fala acompanham quem fala**, ficam acima das plaquinhas e mostram no máximo 2 por pessoa |
| — | As crises (taquicardia etc.) continuam como estavam |

### v3 (05/11/2026)

| # | O que muda | Antes | Depois | Seções |
|---|---|---|---|---|
| 1 | Barreiras de identidade | muro roxo que dava para desviar; batendo, perdia coração | muro que **ocupa a rua inteira**; **não dá para pular nem desviar**; a personagem fica presa um instante e perde um item que ama, **sem perder coração** | 6.5, 8, 13 |
| 2 | Colapso | aparecia "NÃO DÁ MAIS" | **sem frase**: a personagem apenas para | 6.13, 8 |
| 3 | Medidor | "dificuldade" (FÁCIL … EXTREMA+) | "barreiras sociais" (POUCAS … TODAS). **Desfeito na v4**: voltou a ser "dificuldade" | 3, 5, 12, 13 |
| 4 | Opção de deficiência | não / cadeira de rodas | **não / sim** (a cadeira de rodas fica só como representação visual) | 3, 6.5, 12 |
| — | Frase do chefão | "NÃO HÁ POBREZA QUE RESISTA A 14 HORAS DE TRABALHO" | **mantida, sem alteração** | 6.10, 9 |

**Motivo das mudanças 1 a 3:**
- Se desse para desviar de RACISMO ou ASSÉDIO, o jogo diria sem querer que quem foi atingido "não desviou direito". Com o muro inevitável, o jogo cumpre o próprio aviso: "algumas barreiras não dependem de quem passa".
- "Não dá mais" é uma frase muito associada a ideação suicida, por isso saiu.
- "Dificuldade" dava a entender que o problema era a identidade. "Barreiras sociais" deixava claro que o peso vem do caminho. (Na v4 a equipe preferiu voltar para "dificuldade".)

---

## 1. Visão geral

- **O que é:** joguinho em pixel art, de navegador, feito para a **Semana da Psicologia**. Tema: saúde mental, cobranças sociais, desigualdade e cuidado.
- **Formato:** um único arquivo HTML, sem instalação. Funciona no computador, no celular (de preferência deitado) e com controle de videogame. Pode ser instalado na tela inicial do celular, onde aparece com o nome "Saúde Mental".
- **Duração:** uma partida leva cerca de 3 minutos (no máximo 180 segundos de jogo, mais o final).
- **Visual:** uma avenida noturna vista de cima em 3/4, rolando para a direita. A personagem anda com uma pilha de "cargas" na cabeça.
- **Mensagem central:** *"Saúde mental não é linha de chegada. E ninguém caminha sozinho."*
- **Descrição para compartilhar (link):** "Um joguinho sobre saúde mental e cobranças. Todo mundo parece chegar lá. Por que você não chega?"

### Fluxo de telas
1. **Capa** → 2. **Escolha de personagem** ("Quem você vai ser?") → 3. **Sorteio** ("Você não escolhe.") → 4. **Partida** (com a **tela de bônus** quando o psicólogo chega) → 5. **Final animado** → 6. **Tela de fim**, que leva a "jogar de novo" ou "trocar personagem".

---

## 2. Capa (tela inicial)

**Textos:**
- Logo: **RUMO À** / **SAÚDE MENTAL**
- Botão: **▶ começar** (piscando)
- Rodapé: **semana da psicologia**

**Cena animada:** uma avenida da cidade ao entardecer/noite, com prédios, nuvens rosadas, varal de lâmpadas, postes, um gato preto, uma bicicleta e uma plaquinha de coração em neon que pisca. **Várias pessoas diferentes** andam pela avenida, cada uma com sua pilha, para a capa não ficar enviesada numa identidade só:
- um homem branco rico: trabalho, doença, cuidar dos pais
- uma mulher negra pobre: boleto, aluguel, faculdade, dupla jornada
- mais ao fundo, um homem negro LGBT+: boleto, trabalho, provar o dobro
- uma mulher cadeirante LGBT+: dupla jornada, trabalho

Enquanto andam, cada uma **vai deixando cair, de vez em quando, as coisas que ama** (guitarra, pintura, livro, bola, videogame, música, skate, cinema).

---

## 3. Escolha de personagem

**Textos:**
- Sobretítulo: **antes de nascer**
- Título: **QUEM VOCÊ VAI SER?**
- Retrato animado com a legenda **você**
- Opções (duas escolhas por linha):

| Linha | Opção A (padrão) | Opção B |
|---|---|---|
| cor | branca | negra |
| gênero | homem | mulher |
| orientação | hétero | lgbt+ |
| classe | rica | pobre |
| deficiência | não | sim |

- Medidor: **dificuldade**, com 6 níveis: **FÁCIL, NORMAL, DIFÍCIL, MUITO DIFÍCIL, EXTREMA, EXTREMA+**
- Botão: **nascer**
- **A tela já abre com um personagem aleatório** (cada traço é sorteado), para não ter um "padrão" no começo. A pessoa pode mudar à vontade.

**Regra da dificuldade:** cada escolha da coluna B soma +1 ponto (negra, mulher, lgbt+, pobre, com deficiência). Com 0 pontos é FÁCIL e com 5 é EXTREMA+. A ideia: "o caminho não é igual para todo mundo". A dificuldade também define o ritmo do jogo: quanto maior, mais rápido caem as cargas e mais frequentes são as barreiras.

### 3.1 Sorteio: "VOCÊ NÃO ESCOLHE."
Ao clicar em **nascer**, a escolha feita **não vale**:
- Sobretítulo: **mas na vida real...**
- Título: **VOCÊ NÃO ESCOLHE.**
- O retrato e os traços giram rápido, como numa roleta (com "tic-tic"), e vão desacelerando por cerca de 3 s até parar num **personagem sorteado**. A legenda muda de "sorteando..." para **"você"**.
- Aparecem os traços sorteados (ex.: *"mulher · negra · hétero · pobre"*) e a **dificuldade** em cor.
- Frase: **"ninguém escolhe cor, gênero, classe ou corpo ao nascer."**
- Depois de cerca de 3 s (ou com um toque na tela), a partida começa com o personagem sorteado. "Jogar de novo" repete o mesmo personagem; "trocar personagem" volta à escolha (que abre aleatória de novo).

**Aparência da personagem conforme as escolhas:**
- negra → pele escura e cabelo crespo (afro, se for mulher)
- branca → pele clara (cabelo comprido, se for mulher)
- rica → camisa azul-marinho e blazer
- pobre → camisa vermelha e calça jeans
- lgbt+ → broche de arco-íris no peito
- deficiência: sim → aparece sentada numa cadeira de rodas (representação visual da deficiência)

> Existe no código uma opção **"filhos"** (com criança acompanhando, cargas e barreiras próprias), mas **ela não aparece na tela de escolha**. Hoje fica sempre desligada. Detalhes na seção 12.

---

## 4. Controles

- **Teclado:** setas ou WASD para andar; espaço (também Z/K) para pular; E (também X/J/Shift) para largar carga; M para ligar/desligar o som
- **Celular:** arrastar na tela vira um joystick para andar; toque rápido ou botão **PULAR** para pular; botão **LARGAR** para soltar uma carga; botão **SOM/MUDO** no canto
- **Controle de videogame:** analógico ou direcional para andar; A para pular; B/X para largar
- No celular, o jogo entra em tela cheia no primeiro toque e tenta travar a tela deitada. Se o celular estiver em pé, aparece a dica: **"gire o celular para jogar maior"**.
- Dica fixa abaixo do jogo (no computador): **"setas / wasd andar · espaço pular · e largar carga · m som"**

---

## 5. Interface durante a partida (HUD)

- **5 corações**, com a legenda **"saúde mental"**
- Barra de progresso **"CAMINHO DA SAÚDE MENTAL"**, que termina num marco verde **"saúde mental"**
- Canto direito: **"dificuldade"** e o nível (FÁCIL … EXTREMA+)
- **Balões de fala acompanham quem fala**: os da personagem ficam acima da plaquinha "VOCÊ", os do(a) psicólogo(a) um pouco ao lado, e cada pessoa mostra no máximo 2 balões (o mais novo embaixo)
- Plaquinha **"VOCÊ"** em cima da pilha da personagem
- Plaquinha **"PSICÓLOGO"** ou **"PSICÓLOGA"** em cima do(a) psicólogo(a), quando ele(a) chega
- Plaquinha **"MERCADO DE TRABALHO"** embaixo do chefão
- Avisos numa faixa vermelha embaixo, sempre com ⚠ (lista na seção 9)

---

## 6. Dinâmica central

### 6.1 A avenida e o portal que foge
- A personagem anda para a direita. Lá na frente há um **portal/arco verde escrito "SAÚDE MENTAL"**.
- **O portal sempre se afasta.** Quando a personagem chega a 150 px dele, ele "foge" para frente (com um som de vento). Quanto mais carga ela leva, mais longe ele vai. **Ninguém alcança o portal.** É a tradução de "saúde mental não é linha de chegada".

### 6.2 Cargas que caem do céu
Os blocos caem do alto. Se caem na pilha, grudam na cabeça. Cada carga pesa e deixa a personagem **mais lenta** e com **pulo mais baixo**. A pilha vai até 16 itens.

**Cargas que NÃO saem (fixas):**

| Carga | Texto | Quem recebe |
|---|---|---|
| boleto | BOLETO | todos (pobre recebe mais vezes e **já começa com um**) |
| trabalho | TRABALHO | todos |
| faculdade | FACULDADE | todos |
| doença | DOENÇA | todos |
| aluguel | ALUGUEL | todos |
| cuidar | CUIDAR DOS PAIS | todos |
| casa | DUPLA JORNADA | só mulher |
| dobro | PROVAR O DOBRO | só pessoa negra |
| filhos / creche | FILHOS / CRECHE | só com filhos (opção desligada) |

**Cargas que saem só com o(a) psicólogo(a) por perto:**

| Carga | Texto | Origem |
|---|---|---|
| culpa | CULPA (pesa o dobro) | jogada pelo Mercado de Trabalho |
| armário | ARMÁRIO | só LGBT+, cai a cada 10–13 s depois dos 7 s de jogo |

**Cargas que dá para largar a qualquer hora (botão LARGAR / tecla E):**

| Carga | Texto | Extra |
|---|---|---|
| curtidas | CURTIDAS | |
| padrão | PADRÃO DE BELEZA | |
| consumo | TER MAIS | |
| comparar | VIDA DOS OUTROS | |
| curso | CURSO DA FELICIDADE | ao pegar, aparece também **"SÓ 12X DE R$ 97!"** |

**Ritmo:** nos primeiros 12 segundos só caem cargas pesadas. Depois disso, 55% do que cai é largável. Quanto maior a dificuldade, mais rápido as cargas caem.

### 6.3 O que você ama (itens bons)
Itens com brilho azul que também caem e entram na pilha:

| Item | Texto |
|---|---|
| guitarra | TOCAR GUITARRA |
| paleta | PINTAR |
| livro | LER |
| bola | JOGAR BOLA |
| controle | VIDEOGAME |
| fone | OUVIR MÚSICA |
| skate | ANDAR DE SKATE |
| pipoca | IR AO CINEMA |

- Eles **aliviam**: cada um reduz a "pressão" interna (ver 6.7).
- **Não dá para largá-los de propósito.**
- **A pressão os tira de você:** sempre que cai uma carga fixa na pilha, ou quando a personagem bate numa barreira, ela **perde um item que ama**. Aparece **"VOCÊ LARGOU: [ITEM]"**. Isso não acontece com o(a) psicólogo(a) por perto.
- Caem com frequência no começo (a cada 3,6–5 s) e ficam mais raros depois dos 35 s (a cada 7–9 s).

### 6.4 Largar
- Ao apertar LARGAR, sai **a carga largável mais alta da pilha**, com um efeito verde.
- Ao largar a culpa: **"CULPA LARGADA"**. Ao largar o armário: **"ARMÁRIO LARGADO"**.
- Se nada na pilha pode sair: a pilha treme e aparece **"NÃO SAI"**.
- Com o(a) psicólogo(a) por perto, **o que pode ser largado brilha em verde**.

### 6.5 Barreiras no chão
Começam depois de 4 s. Existem dois tipos, com regras diferentes.

**Barreiras comuns**: cada uma é uma cena animada própria, a maioria em movimento:

| Barreira | Como aparece | Como passar |
|---|---|---|
| PRAZO | despertador vermelho que **rola na sua direção**, tocando "TRIIIM" | pular ou desviar |
| META | gráfico de barras vermelhas que **sobem e descem** | pular quando as barras estão baixas |
| HORA EXTRA | relógio de ponto marcando **23:47** | pular ou desviar |
| CONTA ATRASADA | envelopes de conta **voando**, subindo e descendo na pista | desviar no tempo certo |
| PROVA AMANHÃ | pilha alta de livros balançando | desviar (alta para pular) |
| SEM FÉRIAS | mala acorrentada com cadeado e guarda-sol fechado | pular ou desviar |
| FILA | três pessoas numa fila atravessada na pista | desviar |
| DESEMPREGO | porta com placa **"VAGA PREENCHIDA"** que às vezes abre ("ABERTA?") | passar quando abre |
| TRÂNSITO | carro **cruzando a avenida** de um lado ao outro, buzinando "BI-BI!" | esperar ou pular |
| PLANTÃO | maca de hospital com sirene **atravessando a rua** | esperar ou pular |

- Dá para **pular** ou **desviar**.
- Batendo, a personagem **perde 1 coração**, fica piscando por um instante, perde um item que ama e aparece o nome da barreira.

**Barreiras sociais (de identidade)**: muro roxo alto que **ocupa a rua inteira, de calçada a calçada**.

- **Não dá para pular nem desviar.** Se o jogador tenta pular, o pulo bate no muro e a personagem volta ao chão. Não existe jeito de escapar: a barreira não depende da habilidade de quem passa.
- Ao encostar no muro, a personagem **fica presa por um instante** (é empurrada levemente para trás e não avança), **perde um item que ama** e aparece o nome da barreira. Depois disso ela atravessa devagar e segue o caminho.
- **Não tira coração.** O custo é tempo e o que você ama, não uma "falha" do jogador.
- Aparecem em 60% das vezes quando a personagem tem algum desses traços:

| Traço | Barreiras |
|---|---|
| negra | RACISMO · "SEM PERFIL" · SEGUIDA NA LOJA |
| mulher | MACHISMO · ASSÉDIO · SALÁRIO MENOR |
| lgbt+ | LGBTFOBIA · "É SÓ UMA FASE" · PIADINHA |
| pobre | SEM GRANA · ÔNIBUS LOTADO · SEM INTERNET |
| com deficiência (peso dobrado) | SEM RAMPA · ESCADA · CALÇADA QUEBRADA · CAPACITISMO |
| filhos (desligado) | SEM CRECHE · REUNIÃO NA ESCOLA |

A dificuldade também deixa as barreiras mais frequentes.

### 6.6 As pessoas de máscara (quem "chega lá")
- Depois de 3 s, a cada 4,5–7 s passa alguém **mais rápido que você**. São **9 pessoas diferentes** (brancas, negras, pardas; homens e mulheres; uma com broche LGBT+), todas com a mesma **máscara branca sorridente**.
- **O jeito de passar é sorteado** a cada vez (nem todos aparecem em toda partida):

| Jeito | Chance | O que faz |
|---|---|---|
| correndo | 20% | corre até o portal |
| selfie | 18% | corre, **para no meio do caminho, levanta o celular, tira uma selfie (flash)** e segue |
| patins | 16% | desliza de patins, com rastro de velocidade |
| moto | 16% | moto vermelha com farol |
| carro de luxo | 20% | conversível chique (preto, branco, vermelho ou azul, com detalhes dourados) e brilho |
| jato particular | 10% | jato passa voando no céu, rápido |

- Quando passam pelo portal, **param, posam para uma foto (flash)** e dizem uma frase:
  - **A pé, de patins ou na selfie:** "Tô ótima!" · "#gratidão" · "Cheguei!" · "Só good vibes" · "Vida plena" · "Saúde mental 100%"
  - **De moto ou carro:** "Venci na vida" · "É só querer" · "Foco e fé" · "#abençoado" · "Trabalhe enquanto eles dormem"
  - **Na selfie:** "#partiu" · "olha eu chegando!" · "#vidaperfeita" · "bom dia, mundo!" · "#gratiluz" · "#foco". Logo depois da selfie, a máscara levanta por um instante.
  - **Do jato:** "Cheguei antes!" · "#jetlife" · "Primeira classe pra felicidade" · "Sucesso é questão de mindset"
- Pouco depois da foto, **a máscara levanta e mostra o rosto de verdade: com uma lágrima.** Com o(a) psicólogo(a) por perto, ou no final, as máscaras aparecem sempre levantadas.

### 6.7 Pressão interna: coração, crises e efeitos de tela
O jogo calcula uma **"pressão"**:
`peso da pilha (pela metade com o psi por perto) + 1,2 × corações perdidos − 1,5 × itens que você ama`

- **Pressão ≥ 3:** começa a soar um **batimento cardíaco** e a tela escurece nas bordas.
- **Pressão maior ainda:** a tela treme, fica levemente esverdeada e aparece uma imagem dupla.
- **Pressão ≥ 6: CRISES** (de tempos em tempos). Duram cerca de 4,6 s, cada uma com um título grande, uma legenda e um efeito próprio:

| Crise | Legenda | Efeito |
|---|---|---|
| TAQUICARDIA | o coração dispara | coração gigante pulsando, tela vermelha, zoom no ritmo do batimento |
| FALTA DE AR | o ar não vem | escrita "inspira..." / "...expira", a visão fecha num túnel, som de respiração |
| SONO | faz dias que você não dorme direito | "Z"s subindo, as pálpebras (tela) fecham |
| TREMOR | o corpo treme | a tela treme forte |
| TONTURA | tudo gira | a tela gira |
| ENJOO | o estômago revira | tela esverdeada, imagem ondulando |
| MEDO | e se der tudo errado? | tela escura, ruído grave |

  As mais comuns são TAQUICARDIA e FALTA DE AR, seguidas de SONO. As crises também deixam a personagem mais lenta. **Com o(a) psicólogo(a) por perto, elas ficam mais fracas e mais espaçadas.**

### 6.8 Pensamentos (autocobrança)
Com a pilha a partir de peso 2, surgem balões de pensamento (em itálico, com bolinhas) a cada 6–9 s. Durante uma crise, a cada 3 s:
"continue..." · "é pior parar" · "não tem saída" · "não posso falhar" · "depois eu descanso" · "todo mundo consegue, menos eu" · "se eu parar, perco tudo" · "não sou suficiente" · "aguenta mais um pouco" · "a culpa é minha"

### 6.9 A multidão (a partir de 25 s)
Pessoas cinzentas e sem rosto ficam paradas nas calçadas. Elas **jogam cargas largáveis** em arco na sua direção e gritam:
"Preguiça!" · "Não quer vencer na vida?" · "Quem quer dá um jeito" · "Frescura!" · "Ansiedade é moda" · "Falta força de vontade" · "Vai trabalhar!" · "Já comprou casa?" · "E o namoro?" · "Tem que ser feliz!" · "Só depende de você" · "Na sua idade eu já..." · "Cadê o carro?" · "Isso é falta do que fazer"

Enquanto o chefão está em cena, a multidão **fica quieta** e não joga nada.

### 6.10 Chefão: MERCADO DE TRABALHO (a partir de 60 s)
- **A cena abre espaço para ele:** os mascarados saem correndo e não aparecem mais; a multidão fica quieta; os outdoors param de piscar "COMPRE AGORA"; os pensamentos ficam mais espaçados. Ele é desenhado **na frente** de buracos, barreiras e figurantes, e as falas dele aparecem em **balões maiores**.
- Entra com um flash, uma faixa grande **"MERCADO DE TRABALHO"** e a legenda **"o chefão que cobra de todo mundo, e diz que a culpa é sua"**.
- O visual: um executivo de terno e gravata vermelha, com um **monitor no lugar da cabeça** mostrando um gráfico subindo e olhos vermelhos. Carrega uma maleta.
- **Ataques:**
  1. **Metas rolando** (a partir de 2 s): blocos vermelhos rolam na sua direção com os textos **META, META x2, KPI, PRAZO**. Batendo, perde coração.
  2. **Holofote da vigilância** (a partir de 5 s): um feixe de luz varre a pista. Se ficar dentro dele, ganha TRABALHO ou BOLETO e o chefão grita **"PRODUZA!"**.
  3. **Culpa do céu** (a partir de 10 s): a cada 5–7 s cai uma CULPA mirando em você, com uma **sombra vermelha** no chão, e o chefão diz **"A CULPA É SUA"**.
- **Falas aleatórias** (a cada 3–5 s): "PELO BEM DA EMPRESA" · "VOCÊ DEVERIA AGRADECER" · "NÃO HÁ POBREZA QUE RESISTA A 14 HORAS DE TRABALHO" · "VISTA A CAMISA DA EMPRESA" · "PRODUZA!" · "TEM GENTE NA FILA" · "SEJA RESILIENTE"

### 6.11 Outdoors no fundo
Ao longo da avenida aparecem outdoors. Os que vendem algo piscam **"COMPRE AGORA"** (menos durante o chefão):
"CARRO DO ANO: SEJA FELIZ" · "CURSO: FELICIDADE JÁ" · "CELULAR NOVO, VIDA NOVA" · "LIVRO: AUTOCUIDADO" · "ROUPA DE MARCA = SUCESSO" · "FELICIDADE EM 12X" · "MÉTODO MENTE SÃ 3.0" · "MENTORIA: SEJA FELIZ" · "SEJA MAIS" · "#SUCESSO"

### 6.12 O(a) psicólogo(a)
- **Quando chega:** depois de 50 s se você estiver com 2 corações ou menos; ou 35 s depois que o chefão aparece; ou quando o chefão está em cena e você fica com 1 coração. Na prática, chega em algum momento entre 50 e 95 s.
- **Aparência sorteada a cada partida:** tom de pele, cabelo (incluindo grisalho, roxo e azul), roupa, chance de ser cadeirante (15%), chance de ter broche LGBT+ (20%) e 50% de chance de ser psicóloga ou psicólogo.
- **Ao chegar:** toca um sininho, você **recupera 1 coração** e o jogo **pausa numa tela de bônus**:
  - Sobretítulo piscando: **★ bônus ★**
  - Título: **A PSICÓLOGA CHEGOU** / **O PSICÓLOGO CHEGOU**
  - Retrato grande do(a) psicólogo(a), com brilho verde e a legenda PSICÓLOGA/PSICÓLOGO
  - Lista de benefícios, que entram um por um com um som:
    - **+1 ♥** um coração de volta
    - **½** perto dela/dele, a pilha pesa a metade
    - **SOLTA** culpa e armário dá pra largar: o que brilha, sai
    - **♪** perto dela/dele, você não perde o que ama
    - **CALMA** as crises vêm mais fracas e mais espaçadas
  - Frase: **"Ela/Ele não carrega nada por você. Caminha junto."**
  - Botão: **seguir juntos** (volta ao jogo)
- **O que muda com ele(a) por perto (até 60 px de distância):**
  - a pilha pesa **metade** na pressão
  - **CULPA e ARMÁRIO podem ser largados**, e o que é largável **brilha**
  - você **não perde** o que ama
  - as crises ficam mais fracas e mais espaçadas
  - as máscaras dos outros aparecem levantadas
- **Ele(a) NUNCA carrega cargas por você.** Só caminha junto, sempre um pouco atrás e ao lado.
- **Falas:** a lista está **vazia de propósito**. O código diz: *"falas do(a) psicólogo(a): a definir com a equipe. Enquanto a lista estiver vazia, ele(a) só acompanha em silêncio."* O jogo já está preparado para ele(a) responder aos pensamentos da personagem: quando surge um pensamento perto dele(a), uma fala responderia em cerca de 1,3 s. **Esse é um ponto em aberto para a equipe definir.**

### 6.13 Como a partida termina
- **Fim normal:** 30 s depois que o(a) psicólogo(a) chega, ou aos 180 s de jogo.
- **Colapso:** quando os corações chegam a 0. **Não aparece nenhuma frase: a personagem apenas para**, e o final animado começa.

---

## 7. Final animado (igual nos dois casos)

1. Tudo para. **O chefão sai de cena**, os mascarados vão embora, e a multidão e os obstáculos somem aos poucos. **Só ficam as pessoas que ajudam.**
2. A pilha **balança** e a personagem **cai de joelhos**. As cargas se espalham pelo chão: **no máximo 8**. Se havia mais, as outras somem.
3. Se o(a) psicólogo(a) ainda não tinha chegado, ele(a) chega agora e fica **colado(a) ao lado da personagem, na frente**, com a plaquinha PSICÓLOGA/PSICÓLOGO visível. Ninguém o(a) cobre.
4. **Quatro pessoas** (diversas: uma mulher negra de cabelo afro, uma ruiva, um homem negro com broche LGBT+ e outra pessoa) vêm correndo dos dois lados. **Cada uma pega coisas do chão e carrega na própria cabeça, no máximo 2 por pessoa.**
5. O que ninguém conseguiu pegar some. A personagem **levanta livre, sem nada na cabeça**.
6. Todos **caminham juntos** para a direita: a personagem, o(a) psicólogo(a) ao lado e os quatro ajudantes carregando as cargas.
7. Uma caixa de texto digita, letra por letra:
   - **"Saúde mental não é linha de chegada."**
   - **"E ninguém caminha sozinho."** (em verde)
8. Toca um acorde, a tela escurece e aparece a tela de fim.

O psicólogo continua sem carregar nada no final. **Quem divide o peso é a rede de pessoas**, e ele(a) caminha junto.

---

## 8. Tela de fim

- Sobretítulo: **"fim do caminho (por enquanto)"**, igual nos dois casos (o sobretítulo do colapso, "a saúde mental chegou ao limite", saiu junto com a frase "NÃO DÁ MAIS")
- Título: **SAÚDE MENTAL NÃO É LINHA DE CHEGADA.**
- Subtítulo (verde): **E ninguém caminha sozinho.**
- Números da partida:
  - **[n] cargas carregadas** (todas as cargas que caíram na pilha, contando o boleto inicial)
  - **[n] cargas largadas**
  - **[n] tropeços** (barreiras comuns em que bateu)
  - **[n] coisas que você ama perdidas**
  - **[n] barreiras sociais no caminho** (muros de identidade, que não dependem do jogador; aparece só se for maior que zero)
- **"O psicólogo não carregou nada por você. Caminhou junto."** (ou "A psicóloga…")
- **Quadro de ajuda** (em verde): **"PRECISA CONVERSAR? EXISTE AJUDA GRATUITA E PERTO DE VOCÊ"**
  - **CVV 188**: ligação grátis, 24 horas · chat em **cvv.org.br** (link)
  - **CAPS e UBS**: atendimento pelo SUS, perto da sua casa
  - **serviço-escola** de psicologia da sua faculdade, se houver: atendimento gratuito ou de baixo custo
- Botões: **jogar de novo** · **trocar personagem**
- **Aviso** (em itálico, no rodapé): *"Isto é um joguinho. As situações aqui são representações simplificadas e gamificadas de experiências reais, feitas para abrir conversa na Semana da Psicologia. A intenção não é medir, comparar nem diminuir a dor de ninguém: cada história é única e bem mais complexa do que qualquer jogo consegue mostrar."*
- Em telas baixas (celular deitado, notebook), a tela se divide em duas colunas para caber sem rolar.

> Os muros de identidade saíram da contagem de "tropeços" porque são inevitáveis. Contá-los como tropeço voltaria a sugerir que a culpa foi de quem passou.

---

## 9. Todos os avisos (faixa ⚠ embaixo da tela)

Cada aviso aparece uma vez por partida, na hora indicada:

| Quando | Texto |
|---|---|
| início | siga a avenida até a saúde mental |
| primeiro item que você ama | o que você ama também está no caminho: música, arte, leitura, esporte |
| primeira vez que perde um item que ama | a pressão empurra pra fora o que você ama |
| primeira carga fixa | algumas cargas não saem: boleto, trabalho, faculdade |
| primeira carga largável | curtidas, padrão de beleza, ter mais: essas dá pra largar (tecla E) / (botão LARGAR) |
| primeira barreira comum | pule as barreiras com espaço, ou desvie / pule as barreiras: toque rápido na tela ou PULAR |
| primeira barreira social (muro) | algumas barreiras não dependem de quem passa |
| primeira foto de pessoa mascarada | todo mundo parece chegar lá. repare nas máscaras |
| 25 s | a multidão cobra o tempo todo |
| 60 s | o mercado de trabalho chegou |
| chefão +2 s | metas vêm rolando: pule ou desvie |
| chefão +5 s (holofote) | fuja da luz da vigilância |
| chefão +7 s | "não há pobreza que resista a 14 horas de trabalho", diz o mercado |
| chefão +13 s | a culpa cai do céu: saia da sombra vermelha |

**Balões especiais:**
- pobre, no início: **"JÁ VEIO COM VOCÊ"** (já começa com um boleto)
- ao pegar uma carga: o nome dela (vermelho se for fixa, dourado se for largável)
- ao pegar um item que ama: **"+ [NOME]"** (azul)

---

## 10. Linha do tempo de uma partida típica

| Tempo | O que acontece |
|---|---|
| 0 s | começa (pobre já com BOLETO) |
| 1,5 s | começam a cair itens que você ama |
| 3 s | começam as cargas (só pesadas até 12 s) e as pessoas mascaradas |
| 4 s | começam as barreiras (comuns e sociais) |
| 7 s | LGBT+: começa a cair o ARMÁRIO |
| 12 s | cargas largáveis entram na mistura |
| 25 s | chega a multidão |
| 35 s | itens que você ama ficam mais raros |
| 50 s+ | o(a) psicólogo(a) pode chegar (se você estiver com ≤ 2 corações), com a tela de bônus |
| 60 s | entra o MERCADO DE TRABALHO; os mascarados saem de cena |
| ~95 s | o(a) psicólogo(a) chega, no máximo |
| psi + 30 s | final |
| 180 s | final (limite) |

**Ambiente:** a tela vai escurecendo com o tempo e com o peso da pilha. A música (chiptune) começa em tom maior e, quando escurece, passa para **tom menor**, mais lenta e mais grave. No final, a luz volta aos poucos.

---

## 11. Sons

Pulo, aterrissagem, batida (perde coração), largar (som leve e brilhante), "não sai" (som grave), batimento cardíaco, entrada do chefão (ronco grave), apito de aviso, clique de foto, vento (portal fugindo), respiração (FALTA DE AR), sininho (psicólogo chega) e um acorde final. Cada crise tem seu som próprio.

---

## 12. Coisas no código que hoje não aparecem (para decidir)

1. **Opção "filhos" desligada.** Tudo está pronto (criança que acompanha e fala "tô com fome!", "me leva no colo?", "brinca comigo?", "olha!", "tô cansado..."; cargas FILHOS e CRECHE; barreiras SEM CRECHE e REUNIÃO NA ESCOLA; +1 na dificuldade), mas **não existe o botão** na tela de escolha.
2. **Falas do(a) psicólogo(a) vazias.** É uma decisão consciente, à espera da equipe (seção 6.12).
3. **Textos da tela de fim que não aparecem**, porque os elementos não existem no HTML (o personagem sorteado já aparece na tela de sorteio):
   - perfil jogado: *"você jogou como [mulher, negra, LGBT+, com deficiência, pobre] · dificuldade [nível]"*
   - lista do que foi perdido: *"Pelo caminho, a pressão tirou de você: [itens]."*
   - dica de controles no celular: *"arraste na tela para andar · toque rápido ou PULAR para pular · LARGAR solta uma carga · 5 corações"*
4. **Nome:** o jogo se chama "Rumo à Saúde Mental", mas o endereço ainda é `rumo-ao-bem-estar` (nome antigo).

---

## 13. Leitura simbólica (resumo do design)

| Elemento do jogo | O que representa |
|---|---|
| Portal "SAÚDE MENTAL" que sempre foge | saúde mental como processo, não como meta a "alcançar" |
| Cargas fixas (boleto, trabalho, doença…) | pressões estruturais que não se resolvem com força de vontade |
| Cargas largáveis (curtidas, padrão, ter mais…) | pressões sociais/culturais que dá para soltar |
| Culpa e armário (só com o psi) | coisas que a terapia ajuda a soltar |
| Itens que você ama que caem | a pressão faz a gente abandonar o que dá prazer; eles aliviam |
| Barreiras sociais (muros que ocupam a rua) | racismo, machismo, LGBTfobia, pobreza, capacitismo: não dá para pular nem desviar, porque não dependem da habilidade de quem passa |
| Dificuldade pelas escolhas | desigualdade de ponto de partida |
| Sorteio "você não escolhe" | ninguém escolhe cor, gênero, classe ou corpo ao nascer |
| Capa com várias pessoas | todo mundo carrega algo; não existe um único perfil "que sofre" |
| Pessoas de máscara posando | a felicidade de vitrine (redes sociais, coach); por trás, a lágrima |
| Multidão sem rosto | cobranças da sociedade e da família |
| Mercado de Trabalho | produtividade, vigilância, metas e culpabilização do indivíduo |
| Chefão saindo de cena no final | quando a rede de apoio chega, a cobrança perde o palco |
| Outdoors "compre agora" | a felicidade vendida como produto |
| Crises (taquicardia, falta de ar…) | sintomas reais de ansiedade/pânico vividos na pele |
| Colapso sem frase | a personagem simplesmente para; o jogo não narra o esgotamento como fim |
| Psicólogo(a) que não carrega | a terapia não resolve por você, mas acompanha |
| Pessoas que dividem a carga no final | rede de apoio: ninguém caminha sozinho |
| Tela de bônus do psicólogo | buscar ajuda muda as regras do jogo, sem tirar o peso por você |
| CVV 188, CAPS/UBS, serviço-escola | ajuda real, gratuita e próxima |
| Aviso "isto é um joguinho" | o jogo simplifica; não mede nem compara a dor de ninguém |
