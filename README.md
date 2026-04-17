<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Para minha pandinha ❤️</title>

<style>
body {
    font-family: 'Comic Sans MS', cursive;
    background: linear-gradient(#f5f5f5, #ececec);
    color: #333;
    text-align: center;
    padding: 20px;
    overflow-x: hidden;
}

.container {
    max-width: 700px;
    margin: auto;
}

h1 {
    color: #6b5b95;
}

/* animação texto */
.fade {
    opacity: 0;
    transform: translateY(20px);
    animation: aparecer 1.5s forwards;
}

@keyframes aparecer {
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

img {
    width: 100%;
    max-width: 400px;
    border-radius: 15px;
    margin: 20px 0;
}

/* botão música */
.botao-musica {
    background: #6b5b95;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 20px;
    cursor: pointer;
}

/* botão final */
button {
    background: #aa6f73;
    color: white;
    border: none;
    padding: 15px 25px;
    border-radius: 20px;
    cursor: pointer;
    margin-top: 20px;
}

.hidden {
    display: none;
}

.final {
    margin-top: 20px;
    font-size: 18px;
    color: #6b5b95;
}

/* corações */
.heart {
    position: fixed;
    bottom: -10px;
    color: #ff6b81;
    animation: subir 6s linear infinite;
    font-size: 20px;
}

@keyframes subir {
    0% { transform: translateY(0); opacity: 1; }
    100% { transform: translateY(-100vh); opacity: 0; }
}

.contador {
    margin: 15px;
    font-size: 16px;
    color: #6b5b95;
}
</style>

</head>

<body>

<!-- música -->
<audio id="musica" loop>
  <source src="musica.mp3" type="audio/mpeg">
</audio>

<button class="botao-musica" onclick="tocarMusica(this)">
Tocar música 🎵
</button>

<div class="contador" id="contador"></div>

<div class="container">

<h1 class="fade">Para minha pandinha, minha princesa, Gabriela Alaide ❤️</h1>

<p class="fade">Eu tentei escrever isso de várias formas…</p>
<p class="fade">mas nenhuma parece suficiente pra você.</p>

<p class="fade">Hoje você faz 18 anos…</p>
<p class="fade">e eu só consigo pensar no quanto sou sortudo por ter você.</p>

<p class="fade">E mês que vem… 1 ano de nós.</p>

<p class="fade"><b>A maquiagem kkkkk</b></p>
<p class="fade">Mesmo dando errado… virou uma das melhores memórias.</p>
<img src="foto1.jpg">

<p class="fade"><b>A viagem…</b></p>
<p class="fade">Ali eu percebi que você era especial de verdade.</p>
<img src="foto2.jpg">

<p class="fade"><b>Seu sorriso…</b></p>
<p class="fade">Ele muda tudo em mim.</p>
<img src="foto3.jpg">

<p class="fade"><b>A cara de nojo KKKKK</b></p>
<img src="foto4.jpg">

<p class="fade"><b>A primeira vez que te vi…</b></p>
<p class="fade">Ali… tudo começou.</p>
<img src="foto5.jpg">

<p class="fade">Pandinha… você é minha pessoa.</p>
<p class="fade">Minha paz. Meu lugar favorito.</p>

<p class="fade">Eu te amo. Hoje e sempre.</p>

<button onclick="mostrarMensagem()">Clique aqui 💖</button>

<div id="mensagemFinal" class="final hidden">
    Você foi a melhor coisa que já aconteceu na minha vida.<br><br>
    Eu escolheria você em todas as vidas.<br><br>
    Feliz aniversário, minha princesa.<br>
    Eu te amo pra sempre. ❤️
</div>

</div>

<script>
// música com fade
function tocarMusica(btn){
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

    btn.style.display = "none";
}

// contador (MUDA A DATA AQUI)
let dataInicio = new Date("2025-05-06"); // <-- COLOCA A DATA QUE VOCÊS COMEÇARAM
let hoje = new Date();
let dias = Math.floor((hoje - dataInicio) / (1000 * 60 * 60 * 24));

document.getElementById("contador").innerText =
"Estamos juntos há " + dias + " dias ❤️";

// corações
setInterval(() => {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerText = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (15 + Math.random() * 20) + "px";
    document.body.appendChild(heart);

    setTimeout(() => {
        heart.remove();
    }, 6000);
}, 500);

// botão final
function mostrarMensagem(){
    document.getElementById("mensagemFinal").classList.remove("hidden");
}
</script>

</body>
</html>
