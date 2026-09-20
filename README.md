<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ingresse</title>
    <style>
       body {
            background-color: var(--primary-color)      ;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            color: var(--secondary-color);
            transition: background-color 0.3s, color 0.3s;
        }
        :root{
            --primary-color: #c0c0c0;
            --secondary-color: #222;
        }
        body.dark-mode {
            background-color: #222;
            color: #f3f3f3;
            transition: background-color 0.3s, color 0.3s;
        }
        body.dark-mode #escuro {
            background-color: #f3f3f3;
            color: #222;
            transition: background-color 0.3s, color 0.3s;
        }
        #escuro {
            background-color: #222;
            color: #f3f3f3;
            border: 1px solid #ccc;
            padding: 5px 10px;
            cursor: pointer;
            margin-left: 5px;
            margin-top: 5px;
            transition: background-color 0.3s, color 0.3s;
            border-radius: 12px;
        }
        h1 {
            text-align: center;
            margin-top: 20px;
            font-family: 'Arial Black', sans-serif, monospace;
        }
        h3 {
            text-align: center;
            margin-top: 5px;
            font-family: 'Fira Sans', sans-serif, monospace;
        }
        footer {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            font-size: 14px;
        }
        p {
            font-family: 'Martel', serif;
            margin: 5px 5px 5px 5px;
        }
        main {
            padding: 20px;
        }
        .filmes-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            max-width: 1100px;
            margin: 30px auto;
        }
        .filme-card {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 18px;
            padding: 12px;
            text-align: center;
            box-shadow: 0 6px 18px rgba(0, 0, 0, 0.12);
        }
        .filme-card img {
            display: block;
            width: 100%;
            height: 260px;
            object-fit: cover;
            border-radius: 14px;
        }
        .filme-card p {
            margin: 10px 0 0;
            font-weight: bold;
            text-align: center;
        }
        body.dark-mode .filme-card {
            background: rgba(255, 255, 255, 0.04);
            box-shadow: 0 6px 18px rgba(0, 0, 0, 0.3);
        }
        .barra-lateral {
            position: fixed;
            z-index: 10;
            inset: 0 auto 0 0;
            width: 220px;
            box-sizing: border-box;
            padding: 90px 18px 24px;
            background: rgba(255, 255, 255, 0.18);
            border-right: 1px solid rgba(34, 34, 34, 0.18);
        }
        .marca-fixa {
            position: fixed;
            z-index: 11;
            top: 24px;
            left: 24px;
            color: var(--secondary-color);
            font-family: 'Arial Black', sans-serif;
            font-size: 22px;
            text-decoration: none;
        }
        .navegacao {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        .navegacao a,
        .navegacao button {
            display: block;
            width: 100%;
            box-sizing: border-box;
            padding: 10px 12px;
            border: 1px solid rgba(34, 34, 34, 0.28);
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.22);
            color: var(--secondary-color);
            font: inherit;
            text-align: left;
            text-decoration: none;
            cursor: pointer;
        }
        .navegacao a:hover,
        .navegacao button:hover {
            background: rgba(255, 255, 255, 0.48);
        }
        body.dark-mode .barra-lateral { background: rgba(0, 0, 0, 0.2); border-color: rgba(255, 255, 255, 0.2); }
        body.dark-mode .marca-fixa,
        body.dark-mode .navegacao a,
        body.dark-mode .navegacao button { color: #f3f3f3; }
        body.dark-mode .navegacao a,
        body.dark-mode .navegacao button { background: rgba(255, 255, 255, 0.08); border-color: rgba(255, 255, 255, 0.28); }
        header, main, footer { margin-left: 220px; }
        @media (max-width: 700px) {
            .barra-lateral { position: static; width: 100%; min-height: auto; padding: 70px 16px 16px; border-right: 0; border-bottom: 1px solid rgba(34, 34, 34, 0.18); }
            .marca-fixa { position: absolute; top: 20px; left: 20px; }
            .navegacao { flex-direction: row; flex-wrap: wrap; }
            .navegacao a, .navegacao button { width: auto; flex: 1 1 130px; text-align: center; }
            header, main, footer { margin-left: 0; }
        }
    </style>
    <script>
        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
        }
        
    </script>
    <link rel="icon" href="favicon.ico" type="image/x-icon">

</head>
<body>
    <a class="marca-fixa" href="Index.html">Ingresse</a>
    <aside class="barra-lateral">
        <nav class="navegacao" aria-label="Navegação principal">
            <button id="escuro" onclick="toggleDarkMode()">Mudar tema</button>
            <a href="Index.html">Filmes em cartaz</a>
            <a href="contato.html">Fale conosco</a>
            <a href="sobre.html">Sobre o Ingresse</a>
        </nav>
    </aside>
    <header>
        <h1>Ingresse</h1>
        <h3>Bem-vindo ao Ingresse!</h3>
    </header>
    <main>
        <div class="filmes-grid">
            <div class="filme-card">
                <a href="AO.html"><img src="AO.jfif" alt="Cartaz do filme A Odisseia"></a>
                <p>A Odisseia</p>
            </div>
            <div class="filme-card">
                <a href="HAUND.html"><img src="HAUND.jfif" alt="Cartaz do filme Homem-Aranha: Um Novo Dia"></a>
                <p>Homem-Aranha: Um Novo Dia</p>
            </div>
            <div class="filme-card">
                <a href="JOGOS.html"><img src="images.jfif" alt="Cartaz do filme Jogos Vorazes: Amanhecer na Colheita"></a>
                <p>Jogos Vorazes: Amanhecer na Colheita</p>
            </div>
            <div class="filme-card">
                <a href="PCUAD.html"><img src="PCUAD.jfif" alt="Cartaz do filme Patrulha Canina: Uma Aventura Dino"></a>
                <p>Patrulha Canina: Uma Aventura Dino</p>
            </div>
            <div class="filme-card">
                <a href="RE.html"><img src="RE.jfif" alt="Cartaz do filme Resident Evil"></a>
                <p>Resident Evil</p>
            </div>
            <div class="filme-card">
                <a href="TS5.html"><img src="TS5.jfif" alt="Cartaz do filme Toy Story 5"></a>
                <p>Toy Story 5</p>
            </div>
            <div class="filme-card">
                <img src="" alt="Sem mais filmes em cartaz :P" href="">
                <p>Sem mais filmes em cartaz :P</p>
            </div>
        </div>
    </main>
    <footer>
        <p>&copy; 2026 Ingresse. Todos os direitos reservados.</p>
        <p style="font-size: 12px;">Desenvolvido por Guilherme Adorno Rodrigues</p>
        <p style="color: var(--primary-color); font-size: 12px;">Parabéns por encontrar meu segredo: [SEGREDO]</p>
    </footer>
</body>
</html>
