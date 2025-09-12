<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Site Acessível</title>
  <style>
    /* ======== ESTILOS GERAIS ======== */
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 0;
      background: #f8f9fa;
      color: #222;
    }

    header, nav, main, footer {
      max-width: 900px;
      margin: auto;
      padding: 1rem;
    }

    /* ======== MENU ======== */
    nav ul {
      display: flex;
      gap: 1rem;
      list-style: none;
      padding: 0;
    }

    nav a {
      text-decoration: none;
      color: #0056b3;
      font-weight: bold;
    }

    nav a:focus, nav a:hover {
      outline: 3px solid #007BFF;
      outline-offset: 2px;
    }

    /* ======== CONTEÚDO ======== */
    img {
      max-width: 100%;
      height: auto;
    }

    /* ======== FORMULÁRIO ======== */
    form {
      display: grid;
      gap: 0.5rem;
      max-width: 400px;
    }

    label {
      font-weight: bold;
    }

    input, textarea, button {
      padding: 0.5rem;
      font-size: 1rem;
    }

    button {
      background: #007BFF;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 4px;
    }

    button:focus {
      outline: 3px solid #222;
    }

    /* ======== FOCO VISÍVEL ======== */
    .user-is-tabbing :focus {
      outline: 3px solid #007BFF;
    }
  </style>
</head>
<body>
  <header>
    <h1>Meu Site Acessível</h1>
    <nav aria-label="Menu principal">
      <ul>
        <li><a href="#conteudo">Ir para o conteúdo</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>

  <main id="conteudo">
    <section id="sobre">
      <h2>Sobre</h2>
      <p>Este site foi construído com foco em acessibilidade. Você pode navegar usando <kbd>Tab</kbd> no teclado.</p>
      <img src="https://placekitten.com/600/300" alt="Um gatinho fofo deitado">
    </section>

    <section id="contato">
      <h2>Fale Conosco</h2>
      <form aria-label="Formulário de contato">
        <label for="nome">Nome:</label>
        <input type="text" id="nome" name="nome" required>

        <label for="mensagem">Mensagem:</label>
        <textarea id="mensagem" name="mensagem" rows="4" required></textarea>

        <button type="submit">Enviar</button>
      </form>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 - Meu Site Acessível</p>
  </footer>

  <script>
    // Script para habilitar foco visível ao usar TAB
    document.addEventListener("keydown", function (e) {
      if (e.key === "Tab") {
        document.body.classList.add("user-is-tabbing");
      }
    });
  </script>
</body>
</html>
