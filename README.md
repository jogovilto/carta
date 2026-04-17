[index.html.txt](https://github.com/user-attachments/files/26841128/index.html.txt)
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<title>Para minha pandinha ❤️</title>

<style>
body {
    font-family: 'Comic Sans MS', cursive;
    background: #f5f5f5;
    color: #333;
    text-align: center;
    padding: 20px;
    overflow-x: hidden;
}

.container {
    max-width: 700px;
    margin: auto;
}

/* ANIMAÇÃO TEXTO */
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
    opacity: 0;
    animation: aparecer 2s forwards;
}

/* delay automático */
.delay1 { animation-delay: 1s; }
.delay2 { animation-delay: 2s; }
.delay3 { animation-delay: 3s; }
.delay4 { animation-delay: 4s; }
.delay5 { animation-delay: 5s; }

/* botão final */
button {
    background: #6b5b95;
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
</style>

</head>

<body>

<!-- MÚSICA -->
<audio autoplay loop>
  <source src="musica.mp3" type="audio/mpeg">
</audio>

<div class="container">

<h1 class="fade">Para minha pandinha, minha princesa, Gabriela Alaide ❤️</h1>

<p class="fade delay1">Eu tentei escrever isso de várias formas…</p>
<p class="fade delay1">mas nenhuma parece suficiente pra você.</p>

<p class="fade delay2">Hoje você faz 18 anos…</p>
<p class="fade delay2">e eu só consigo pensar no quanto sou sortudo por ter você.</p>

<p class="fade delay3">E mês que vem… 1 ano de nós.</p>

<!-- FOTO 1 -->
<p class="fade delay3"><b>A maquiagem kkkkk</b></p>
<p class="fade delay3">Mesmo dando errado… virou uma das melhores memórias.</p>
<img src="foto1.jpg" class="delay3">

<!-- FOTO 2 -->
<p class="fade delay4"><b>A viagem…</b></p>
<p class="fade delay4">Ali eu percebi que você era especial de verdade.</p>
<img src="foto2.jpg" class="delay4">

<!-- FOTO 3 -->
<p class="fade delay5"><b>Seu sorriso…</b></p>
<p class="fade delay5">Ele muda tudo em mim.</p>
<img src="foto3.jpg" class="delay5">

<!-- FOTO 4 -->
<p class="fade delay5"><b>A cara de nojo KKKKK</b></p>
<img src="foto4.jpg" class="delay5">

<!-- FOTO 5 -->
<p class="fade delay5"><b>A primeira vez que te vi…</b></p>
<p class="fade delay5">Ali… tudo começou.</p>
<img src="foto5.jpg" class="delay5">

<p class="fade delay5">Pandinha… você é minha pessoa.</p>
<p class="fade delay5">Minha paz. Meu lugar favorito.</p>

<p class="fade delay5">Eu te amo. Hoje e sempre.</p>

<!-- BOTÃO FINAL -->
<button onclick="mostrarMensagem()">Clique aqui 💖</button>

<div id="mensagemFinal" class="final hidden">
    Você foi a melhor coisa que já aconteceu na minha vida.<br><br>
    Feliz aniversário, minha princesa.<br>
    Eu te amo pra sempre. ❤️
</div>

</div>

<script>
function mostrarMensagem() {
    document.getElementById("mensagemFinal").classList.remove("hidden");
}
</script>

</body>
</html>
