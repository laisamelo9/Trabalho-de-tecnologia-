document.addEventListener('DOMContentLoaded', function () {  
    const botaoDeAcessibilidade = document.getElementById('botao-acessibilidade')
    const opcoesDeAcessibilidade = document.getElementById('opcoes-acessibilidade')

    botaoDeAcessibilidade.addEventListener('click', function () {
        botaoDeAcessibilidade.classList.toggle('rotacao-botao');
        opcoesDeAcessibilidade.classList.toggle('apresenta-lista')

    })

    const aumentaFonteBotao = document.getElementById('aumentar-fonte');
    const diminuiFonteBotao = document.getElementById('diminuir-fonte');

    const alternaContraste = document.getElementById('alterna-contraste')

    let tamanhoAtualFonte = 1;

    aumentaFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte += 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    diminuiFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte -= 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    alternaContraste.addEventListener('click', function () {
        document.body.classList.toggle('alto-contraste')
    })


})
<button onclick="toggleDark()">🌙 Alternar modo escuro</button>

<script>
  function toggleDark() {
    document.body.classList.toggle("dark");
  }
</script>

<style>
  .dark {
    background: #121212;
    color: #eee;
  }
</style>
<button onclick="mostrarAviso()">Mostrar aviso</button>
<p id="aviso" role="alert"></p>

<script>
  function mostrarAviso() {
    const aviso = document.getElementById("aviso");
    aviso.textContent = "Sua sessão vai expirar em 2 minutos!";
    let audio = new Audio("aviso.mp3");
    audio.play();
  }
</script><a href="#conteudo" class="skip-link">Pular para o conteúdo principal</a>

<style>
  .skip-link {
    position: absolute;
    left: -999px;
    top: auto;
    background: #000;
    color: #fff;
    padding: 8px;
  }
  .skip-link:focus {
    left: 10px;
    top: 10px;
  }
</style>

<main id="conteudo">
  <h1>Bem-vindo ao site acessível</h1>
</main>
