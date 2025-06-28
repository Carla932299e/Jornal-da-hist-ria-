<!DOCTYPE html><html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vila Rica Notícias</title>
  <style>
    * {
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background: #f2f2f2;
    }
    header {
      background-color: #004d40;
      color: white;
      padding: 20px;
      text-align: center;
    }
    nav {
      background: #00695c;
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 10px;
    }
    nav a {
      color: white;
      text-decoration: none;
      margin: 5px 10px;
      font-weight: bold;
    }
    .search-box {
      text-align: center;
      margin: 20px auto;
    }
    .search-box input {
      padding: 10px;
      width: 80%;
      max-width: 500px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
    .container {
      padding: 20px;
      max-width: 1000px;
      margin: auto;
    }
    .noticia {
      background: white;
      padding: 15px;
      margin-bottom: 20px;
      border-radius: 5px;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    .noticia h2 {
      margin-top: 0;
      color: #004d40;
    }
    .noticia img {
      width: 100%;
      border-radius: 5px;
      margin-top: 10px;
    }
    footer {
      text-align: center;
      padding: 15px;
      background: #004d40;
      color: white;
      margin-top: 20px;
    }
    @media (max-width: 600px) {
      nav {
        flex-direction: column;
        align-items: center;
      }
      .search-box input {
        width: 95%;
      }
    }
  </style>
</head>
<body><header>
  <h1>📰 Vila Rica Notícias</h1>
  <p>As últimas notícias da nossa querida Vila Rica</p>
</header><nav>
  <a href="#">Início</a>
  <a href="#">Política</a>
  <a href="#">Cultura</a>
  <a href="#">Esporte</a>
  <a href="#">Contato</a>
</nav><div class="search-box">
  <input type="text" placeholder="Pesquisar notícias..." onkeyup="pesquisarNoticias(this.value)" />
</div><div class="container" id="noticias">
  <div class="noticia">
    <h2>Feira Cultural movimenta o centro de Vila Rica</h2>
    <p><strong>27 de junho de 2025</strong> — A tradicional feira reuniu artistas locais, comidas típicas e muito artesanato.</p>
    <img src="https://via.placeholder.com/800x400?text=Feira+Cultural" alt="Feira Cultural">
  </div>  <div class="noticia">
    <h2>Projeto de arborização começa nas escolas municipais</h2>
    <p>Estudantes de diversas idades participam do plantio de mudas e oficinas sobre meio ambiente.</p>
    <img src="https://via.placeholder.com/800x400?text=Arboriza%C3%A7%C3%A3o+nas+escolas" alt="Projeto nas escolas">
  </div>  <div class="noticia">
    <h2>Vila Rica Esporte Clube vence campeonato regional</h2>
    <p>Com gols no segundo tempo, o time da cidade garantiu o título contra a equipe de São Miguel.</p>
    <img src="https://via.placeholder.com/800x400?text=Time+campe%C3%A3o" alt="Campeonato regional">
  </div>
</div><footer>
  <p>&copy; 2025 Vila Rica Notícias — Todos os direitos reservados.</p>
</footer><script>
  function pesquisarNoticias(texto) {
    const noticias = document.querySelectorAll('.noticia');
    noticias.forEach(noticia => {
      const titulo = noticia.querySelector('h2').innerText.toLowerCase();
      const paragrafo = noticia.querySelector('p').innerText.toLowerCase();
      const termo = texto.toLowerCase();
      noticia.style.display = titulo.includes(termo) || paragrafo.includes(termo) ? 'block' : 'none';
    });
  }
</script></body>
</html>
