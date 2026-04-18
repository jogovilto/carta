[index.html.txt](https://github.com/user-attachments/files/26848583/index.html.txt)

<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para minha pandinha ❤️</title>

<style>
body {
    margin: 0;
    font-family: 'Comic Sans MS', cursive;
    background: linear-gradient(#1a1a1a, #2c2c2c);
    color: #f5f5f5;
    text-align: center;
    overflow-x: hidden;
}

#inicio {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

#inicio button {
    padding: 15px 30px;
    border: none;
    border-radius: 30px;
    background: #6b5b95;
    color: white;
    font-size: 18px;
    cursor: pointer;
}

#conteudo {
    display: none;
    padding: 20px;
}

.container {
    max-width: 700px;
    margin: auto;
}

/* DIGITAÇÃO */
.typewriter {
    border-right: 2px solid #fff;
    white-space: nowrap;
    overflow: hidden;
    display: inline-block;
    animation: blink 0.7s infinite;
}

@keyframes blink {
    50% { border-color: transparent; }
}

img {
    width: 100%;
    max-width: 400px;
    border-radius: 15px;
    margin: 20px 0;
}

/* corações */
.heart {
    position: fixed;
    bottom: -10px;
    color: #ff6b81;
    animation: subir 6s linear infinite;
}

@keyframes subir {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-100vh); opacity: 0; }
}

.contador {
    margin: 15px;
    color: #cdb4db;
}

.final-btn {
    background: #aa6f73;
    border: none;
    padding: 15px 25px;
    border-radius: 20px;
    cursor: pointer;
    margin-top: 20px;
    color: white;
}

/* PLOT FINAL */
#plotFinal {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #000;
    color: #fff;
    display: none;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    padding: 30px;
    text-align: center;
    z-index: 999;
}

.plot-text {
    font-size: 20px;
    max-width: 600px;
    line-height: 1.6;
}

.nome-final {
    margin-top: 40px;
    font-size: 30px;
    opacity: 0;
    transition: opacity 2s ease;
    color: #ffcad4;
}
</style>
</head>

<body>

<!-- TELA INICIAL -->
<div id="inicio">
    <h1>Eu fiz isso pra você ❤️</h1>
    <button onclick="entrar()">Entrar</button>
</div>

<!-- MUSICA -->
<audio id="musica" loop>
  <source src="musica.mp3" type="audio/mpeg">
</audio>

<div id="conteudo">

<div class="contador" id="contador"></div>

<div class="container">

<!-- TEXTOS INICIAIS -->
<h1 class="type" data-text="Para minha pandinha, minha princesa, Gabriela Alaide ❤️"></h1>

<p class="type" data-text="Eu tentei escrever isso de várias formas…"></p>
<p class="type" data-text="mas nenhuma parece suficiente pra você."></p>
<p class="type" data-text="Porque você não é algo simples de explicar…"></p>
<p class="type" data-text="você é algo que se sente."></p>

<p class="type" data-text="Hoje você faz 18 anos…"></p>
<p class="type" data-text="e eu só consigo pensar no quanto sou sortudo por ter você."></p>
<p class="type" data-text="E mês que vem… 1 ano de nós."></p>

<!-- BLOCO 1 -->
<div class="bloco" style="display:none;">
<p><b>A maquiagem kkkkk</b></p>
<p>
Eu nunca vou esquecer esse dia...<br><br>
Era pra ser algo simples… e virou um desastre completo kkkkk.<br><br>
Mas o que ficou foi a gente rindo sem parar.<br><br>
E é isso que eu amo na gente.
</p>
<img src="foto1.jpg">
</div>

<!-- BLOCO 2 -->
<div class="bloco" style="display:none;">
<p><b>A viagem…</b></p>
<p>
Foi ali que eu percebi que você era especial de verdade.<br><br>
Que eu queria você na minha vida.
</p>
<img src="foto2.jpg">
</div>

<!-- BLOCO 3 -->
<div class="bloco" style="display:none;">
<p><b>Seu sorriso…</b></p>
<p>
Esse sorriso muda tudo em mim.<br><br>
Me acalma e me faz bem.
</p>
<img src="foto3.jpg">
</div>

<!-- BLOCO 4 -->
<div class="bloco" style="display:none;">
<p><b>A cara de nojo KKKKK</b></p>
<p>
Até isso eu amo em você.<br><br>
Porque é você sendo você.
</p>
<img src="foto4.jpg">
</div>

<!-- BLOCO 5 -->
<div class="bloco" style="display:none;">
<p><b>A primeira vez que te vi…</b></p>
<p>
Ali tudo começou.<br><br>
E foi a melhor coisa que me aconteceu.
</p>
<img src="foto5.jpg">
</div>

<p>Você virou minha paz.</p>
<p>Meu lugar favorito.</p>
<p>Eu te amo. Sempre.</p>

<button class="final-btn" onclick="plotTwist()">Clique aqui 💖</button>

</div>
</div>

<!-- FINAL -->
<div id="plotFinal">
    <div id="plotTexto" class="plot-text"></div>
    <div id="nomeFinal" class="nome-final">Gabriela Alaide</div>
</div>

<script>
// ENTRAR
function entrar(){
    document.getElementById("inicio").style.display = "none";
    document.getElementById("conteudo").style.display = "block";

    let musica = document.getElementById("musica");
    musica.volume = 0;
    musica.play();

    let vol = 0;
    let fade = setInterval(() => {
        if(vol < 1){
            vol += 0.05;
            musica.volume = vol;
        } else {
            clearInterval(fade);
        }
    }, 200);

    iniciarHistoria();
}

// DIGITAÇÃO
function escrever(el, texto, velocidade=35){
    return new Promise(resolve => {
        let i = 0;
        el.innerHTML = "";
        el.classList.add("typewriter");

        function digitar(){
            if(i < texto.length){
                el.innerHTML += texto.charAt(i);
                i++;
                setTimeout(digitar, velocidade);
            } else {
                el.classList.remove("typewriter");
                resolve();
            }
        }
        digitar();
    });
}

// PAUSA
function esperar(ms){
    return new Promise(r => setTimeout(r, ms));
}

// HISTÓRIA
async function iniciarHistoria(){
    let textos = document.querySelectorAll(".type");

    for(let el of textos){
        await escrever(el, el.getAttribute("data-text"));
        await esperar(600);
    }

    await esperar(1000);

    let blocos = document.querySelectorAll(".bloco");

    for(let bloco of blocos){
        bloco.style.display = "block";
        bloco.style.opacity = 0;
        bloco.style.transition = "opacity 1.5s";
        setTimeout(() => bloco.style.opacity = 1, 50);

        await esperar(2500);
    }
}

// CONTADOR
let inicio = new Date("2025-05-06");
let hoje = new Date();
let dias = Math.floor((hoje - inicio) / (1000 * 60 * 60 * 24));
document.getElementById("contador").innerText =
"Estamos juntos há " + dias + " dias ❤️";

// CORAÇÕES
setInterval(() => {
    let h = document.createElement("div");
    h.className = "heart";
    h.innerText = "❤️";
    h.style.left = Math.random() * 100 + "vw";
    document.body.appendChild(h);
    setTimeout(() => h.remove(), 6000);
}, 400);

// FINAL
function plotTwist(){
    document.getElementById("plotFinal").style.display = "flex";

    let texto =
`Se você chegou até aqui...

é porque sentiu tudo.

Mas tem algo que eu ainda não falei.

A melhor escolha da minha vida
foi escolher você.

E eu escolheria você
em todas as vidas.

Feliz aniversário, minha princesa.

Eu te amo. Pra sempre. ❤️`;

    escreverPlot(texto);
}

function escreverPlot(texto){
    let el = document.getElementById("plotTexto");
    let nome = document.getElementById("nomeFinal");
    let i = 0;

    el.innerHTML = "";
    nome.style.opacity = 0;

    function digitar(){
        if(i < texto.length){
            el.innerHTML += texto.charAt(i);
            i++;
            setTimeout(digitar, 40);
        } else {
            setTimeout(() => {
                nome.style.opacity = 1;
            }, 1500);
        }
    }
    digitar();
}
</script>

</body>
</html>
