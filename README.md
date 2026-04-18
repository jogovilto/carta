[index.html.txt](https://github.com/user-attachments/files/26848500/index.html.txt)
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

/* FINAL CINEMA */
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

<div id="inicio">
    <h1>Eu fiz isso pra você ❤️</h1>
    <button onclick="entrar()">Entrar</button>
</div>

<audio id="musica" loop>
  <source src="musica.mp3" type="audio/mpeg">
</audio>

<div id="conteudo">
<div class="contador" id="contador"></div>

<div class="container">

<h1 class="fade type" data-text="Para minha pandinha, minha princesa, Gabriela Alaide ❤️"></h1>

<p class="fade type" data-text="Eu tentei escrever isso de várias formas…"></p>
<p class="fade type" data-text="mas nenhuma parece suficiente pra você."></p>
<p class="fade type" data-text="Porque você não é algo simples de explicar…"></p>
<p class="fade type" data-text="você é algo que se sente."></p>

<p class="fade type" data-text="Hoje você faz 18 anos…"></p>
<p class="fade type" data-text="e eu só consigo pensar no quanto sou sortudo por ter você."></p>
<p class="fade type" data-text="E mês que vem… 1 ano de nós."></p>

<!-- FOTO 1 -->
<p class="fade"><b>A maquiagem kkkkk</b></p>
<p class="fade">
Eu nunca vou esquecer esse dia. Era pra ser algo simples… e virou um desastre completo kkkkk.<br><br>
Mas o que ficou não foi a maquiagem dando errado… foi a gente rindo até não conseguir mais respirar.<br><br>
E é isso que eu amo na gente.<br>
Mesmo quando tudo dá errado… a gente transforma em um dos melhores momentos.<br><br>
Se for pra viver uma vida inteira assim… eu quero isso pra sempre com você.
</p>
<img src="foto1.jpg">

<!-- FOTO 2 -->
<p class="fade"><b>A viagem…</b></p>
<p class="fade">
Essa semana pode parecer só uma viagem…<br>
mas pra mim foi muito mais que isso.<br><br>
Foi ali que eu comecei a perceber o quanto você era importante.<br>
Foi ali que eu senti que não queria te perder.<br><br>
Cada momento ali construiu algo que hoje eu tenho certeza:<br>
eu quero você na minha vida.
</p>
<img src="foto2.jpg">

<!-- FOTO 3 -->
<p class="fade"><b>Seu sorriso…</b></p>
<p class="fade">
Esse sorriso… é diferente.<br><br>
É real. É leve. É você de verdade.<br><br>
E você não faz ideia do quanto isso mexe comigo.<br>
Porque quando você sorri assim… parece que tudo fica bem.<br><br>
Se eu pudesse escolher uma coisa pra ver todos os dias…<br>
seria você sorrindo assim.
</p>
<img src="foto3.jpg">

<!-- FOTO 4 -->
<p class="fade"><b>A cara de nojo KKKKK</b></p>
<p class="fade">
Eu até hoje dou risada disso.<br><br>
Mas sabe o que é mais importante?<br>
A gente é real.<br><br>
A gente não precisa fingir nada.<br>
E talvez seja exatamente isso que faz tudo ser tão especial.<br><br>
Eu amo até suas caras de nojo.
</p>
<img src="foto4.jpg">

<!-- FOTO 5 -->
<p class="fade"><b>A primeira vez que te vi…</b></p>
<p class="fade">
Essa aqui… foi o começo de tudo.<br><br>
Talvez eu não tenha percebido na hora…<br>
mas alguma coisa mudou dentro de mim.<br><br>
Minha vida começou a tomar outro rumo.<br><br>
E hoje eu sei qual era esse rumo:<br>
você.<br><br>
E foi a melhor coisa que já me aconteceu.
</p>
<img src="foto5.jpg">

<p class="fade">Pandinha… você é minha paz.</p>
<p class="fade">Minha pessoa.</p>
<p class="fade">Meu lugar favorito no mundo.</p>

<p class="fade">Eu te amo nos dias bons.</p>
<p class="fade">Nos dias difíceis.</p>
<p class="fade">Em todos os momentos.</p>

<p class="fade">E eu escolheria você… sempre.</p>

<button class="final-btn" onclick="plotTwist()">Clique aqui 💖</button>

</div>
</div>

<div id="plotFinal">
    <div id="plotTexto" class="plot-text"></div>
    <div id="nomeFinal" class="nome-final">Gabriela Alaide</div>
</div>

<script>
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

    iniciarDigitacao();
}

function escreverTexto(el, texto, velocidade=40){
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
        }
    }
    digitar();
}

function iniciarDigitacao(){
    let els = document.querySelectorAll(".type");
    els.forEach((el, i) => {
        setTimeout(() => {
            escreverTexto(el, el.getAttribute("data-text"));
        }, i * 1500);
    });
}

let inicio = new Date("2025-05-06");
let hoje = new Date();
let dias = Math.floor((hoje - inicio) / (1000 * 60 * 60 * 24));
document.getElementById("contador").innerText =
"Estamos juntos há " + dias + " dias ❤️";

setInterval(() => {
    let h = document.createElement("div");
    h.className = "heart";
    h.innerText = "❤️";
    h.style.left = Math.random() * 100 + "vw";
    document.body.appendChild(h);
    setTimeout(() => h.remove(), 6000);
}, 400);

function plotTwist(){
    document.getElementById("plotFinal").style.display = "flex";

    let texto =
`Se você chegou até aqui...

é porque sentiu tudo.

Mas tem uma coisa que eu não falei ainda.

De todas as escolhas da minha vida...

a melhor de todas
foi escolher você.

E se eu pudesse viver tudo de novo...

eu escolheria você
todas as vezes.

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
