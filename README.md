<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Blog</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

<header>
    <h1>Meu Blog</h1>
    <p>Notícias e informações</p>
</header>

<main>

    <article>
        <img src="img/imagem1.jpg" alt="Imagem da postagem">
        <h2>Minha primeira postagem</h2>
        <p>
            Conteúdo do artigo do blog.
        </p>
        <p>
            Autor:
            <a href="https://www.exemplo.com" target="_blank" rel="noopener noreferrer">
                João Silva
            </a>
        </p>
    </article>

    <article>
        <img src="img/imagem2.jpg" alt="Imagem da postagem">
        <h2>Segunda postagem</h2>
        <p>
            Outro conteúdo para o blog.
        </p>
        <p>
            Autor:
            <a href="https://www.exemplo.com" target="_blank" rel="noopener noreferrer">
                Maria Souza
            </a>
        </p>
    </article>


    <button class="btn-tema-escuro">🌙</button>
    <button class="btn-voltar-topo">⬆️</button>

</main>


<script src="script.js"></script>

</body>
</html>
:root {
    --cor-primaria: #183C63;
    --cor-secundaria: #3782d2;
    --cor-fundo: #ffffff;
    --cor-texto: #151428;
    --cor-contraste: #f3eef7;
    --cor-botao: #f9f9f9;
    --cor-destaque: #ff6b00;
    --fonte-texto: 'Segoe UI', sans-serif;
}


/* Transição suave */
* {
    transition: background-color 0.3s ease, 
                transform 0.3s ease,
                box-shadow 0.3s ease;
}


body {
    max-width: 100vw;
    margin: 0;
    background-color: var(--cor-fundo);
    color: var(--cor-texto);
    font-family: var(--fonte-texto);
}


header {
    background-color: var(--cor-primaria);
    color: white;
    padding: 20px;
}


main {
    padding: 20px;
}


article {
    display: flex;
    flex-direction: column;
    gap: 10px;
    padding: 20px;
    margin-bottom: 20px;

    border-radius: 10px;
    background-color: var(--cor-fundo);

    box-shadow: 0 2px 6px rgba(0,0,0,0.3);
}


/* Efeito ao passar o mouse */
article:hover {

    transform: scale(1.02);

    box-shadow:
    0 6px 15px rgba(55,130,210,0.5);
}


img {
    max-width: 100%;
    border-radius: 8px;
}


a {
    color: var(--cor-secundaria);
}


/* Tema escuro */

.tema-escuro {

    --cor-primaria: #c9e3ff;
    --cor-secundaria: #70b7ff;
    --cor-fundo: #151428;
    --cor-texto: #ffffff;
    --cor-contraste: #f3eef7;
    --cor-botao: #222222;
    --cor-destaque: #ffd60a;

}


/* Ajustes no modo escuro */

.tema-escuro a {
    color: var(--cor-secundaria);
}


.tema-escuro p {
    color: var(--cor-texto);
}


.tema-escuro header p {
    color: var(--cor-contraste);
}


/* Sombra dos cards no modo escuro */

.tema-escuro article {

    box-shadow:
    0 2px 8px rgba(120,180,255,0.4);

}


.tema-escuro article:hover {

    box-shadow:
    0 8px 20px rgba(120,200,255,0.7);

}



/* Botão tema */

.btn-tema-escuro {

    position: fixed;

    bottom: 16px;

    right: 16px;

    font-size: 32px;

    padding: 12px;

    background-color: var(--cor-primaria);

    border-radius: 50%;

    border: none;

    cursor: pointer;

}


/* Botão voltar ao topo */

.btn-voltar-topo {

    position: fixed;

    bottom: 80px;

    right: 16px;

    font-size: 24px;

    padding: 12px;

    background-color: var(--cor-secundaria);

    border-radius: 50%;

    border: none;

    cursor: pointer;

}
const btnTemaEscuro = document.querySelector(".btn-tema-escuro");

btnTemaEscuro.addEventListener("click", mudaTema);


function mudaTema() {

    const corpoPagina = document.body;


    if (corpoPagina.classList.contains("tema-escuro")) {

        corpoPagina.classList.remove("tema-escuro");

    } else {

        corpoPagina.classList.add("tema-escuro");

    }

}



const btnVoltarTopo = document.querySelector(".btn-voltar-topo");


btnVoltarTopo.addEventListener("click", function () {

    window.scrollTo(0,0);

});
meu-blog/
│
├── index.html
├── style.css
├── script.js
│
└── img/
    ├── imagem1.jpg
    └── imagem2.jpg
