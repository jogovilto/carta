[index.html.txt](https://github.com/user-attachments/files/26841798/index.html.txt)
<!DOCTYPE html>
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

/* tela inicial */
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

/* conteúdo escondido */
#conteudo {
    display: none;
    padding: 20px;
}

.container {
    max-width: 700px;
    margin: auto;
}

/* animação texto */
.fade {
    opacity: 0;
    transform: translateY(20px);
    animation: aparecer 2s forwards;
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

/* botão final */
.final-btn {
    background: #aa6f73;
    border: none;
    padding: 15px 25px;
    border-radius: 20px;
    cursor: pointer;
    margin-top: 20px;
    color: white;
}

.hidden {
    display: none;
}

.final-msg {
    margin-top: 20px;
    color: #ffcad4;
    font-size: 18px;
}
</style>

</head>

<body>

<!-- TELA INICIAL -->
<div id="inicio">
    <h1>Eu fiz isso pra você ❤️</h1>
    <button onclick="entrar()">Entrar</button>
</div>

<!-- MÚSICA -->
<audio id="musica" loop>
  <source src="musica.mp3" type="audio/mpeg">
</audio>

<!-- CONTEÚDO -->
<div id="conteudo">

<div class="contador" id="contador"></div>

<div class="container">

<h1 class="fade">Para minha pandinha, minha princesa, Gabriela Alaide ❤️</h1>

<p class="fade">Antes de você… eu não sabia como era amar alguém assim.</p>
<p class="fade">Você chegou… e mudou tudo.</p>

<p class="fade">Hoje você faz 18 anos…</p>
<p class="fade">e eu só consigo agradecer por você existir.</p>

<p class="fade">E mês que vem… 1 ano de nós.</p>

<p class="fade"><b>A maquiagem kkkkk</b></p>
<img src="foto1.jpg">

<p class="fade"><b>A viagem…</b></p>
<img src="foto2.jpg">

<p class="fade"><b>Seu sorriso…</b></p>
<img src="foto3.jpg">

<p class="fade"><b>A cara de nojo KKKKK</b></p>
<img src="foto4.jpg">

<p class="fade"><b>A primeira vez que te vi…</b></p>
<img src="foto5.jpg">

<p class="fade">Você virou minha paz.</p>
<p class="fade">Meu lugar favorito.</p>

<p class="fade">E eu te escolheria… em todas as vidas.</p>

<button class="final-btn" onclick="mostrarMensagem()">Clique aqui 💖</button>

<div id="final" class="final-msg hidden">
    Você foi, é, e sempre será<br>
    a melhor coisa da minha vida.<br><br>
    Feliz aniversário, minha princesa.<br>
    Eu te amo pra sempre. ❤️
</div>

</div>
</div>

<script>
// entrar no site
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
}

// contador
let inicio = new Date("2025-05-06"); // ALTERA AQUI
let hoje = new Date();
let dias = Math.floor((hoje - inicio) / (1000 * 60 * 60 * 24));
document.getElementById("contador").innerText =
"Estamos juntos há " + dias + " dias ❤️";

// corações
setInterval(() => {
    let heart = document.createElement("div");
    heart.className = "heart";
    heart.innerText = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 6000);
}, 400);

// mensagem final
function mostrarMensagem(){
    document.getElementById("final").classList.remove("hidden");
}
</script>

</body>
</html>
