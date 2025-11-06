meu_site/
│
├── app.py
└── templates/
    └── index.html

from flask import Flask, render_template

app = Flask(__name__)

@app.route("/")
def home():
    return render_template("index.html")

if __name__ == "__main__":
    app.run(debug=True)

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Site Básico</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #1a1a1a; /* preto */
            color: #f0f0f0; /* texto claro */
        }

        header {
            background-color: #0057e7; /* azul */
            color: yellow; /* amarelo */
            padding: 20px;
            text-align: center;
        }

        main {
            background-color: #333333; /* cinza escuro */
            padding: 40px;
            text-align: center;
        }

        footer {
            background-color: #222; /* preto mais escuro */
            color: #cccccc; /* cinza claro */
            text-align: center;
            padding: 15px;
        }

        button {
            background-color: yellow; 
            color: #000;
            border: none;
            padding: 10px 20px;
            margin-top: 20px;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            background-color: #0057e7;
            color: #fff;
        }
    </style>
</head>
<body>
    <header>
        <h1>Bem-vindo ao Meu Site</h1>
    </header>

    <main>
        <h2>Este é um modelo básico em Flask</h2>
        <p>Feito com as cores preta, cinza, azul e amarela.</p>
        <button>Clique aqui</button>
    </main>

    <footer>
        <p>© 2025 - Meu Site Simples em Flask</p>
    </footer>
</body>
</html>
