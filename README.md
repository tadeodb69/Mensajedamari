<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Lora:ital,wght@1,400&family=Parisienne&display=swap" rel="stylesheet">
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>💌</text></svg>">

    <title>Un Mensaje Especial</title>

    <style>
        :root {
            --color-fondo-gradiente-1: #e0c3fc;
            --color-fondo-gradiente-2: #8ec5fc;
            --color-sobre-cuerpo: #ffdde1;
            --color-sobre-solapa: #eeb7c2;
            --color-carta: #fdfbfb;
            --color-firma: #c91515;
            --color-texto: #3a3a3a;
            --color-sombra-fuerte: rgba(0, 0, 0, 0.25);
            --fuente-titulo: 'Great Vibes', cursive;
            --fuente-carta: 'Parisienne', cursive;
            --fuente-fecha: 'Lora', serif;
        }
        body {
            margin: 0; padding: 20px; box-sizing: border-box;
            display: flex; flex-direction: column; justify-content: center; align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, var(--color-fondo-gradiente-1) 0%, var(--color-fondo-gradiente-2) 100%);
            font-family: var(--fuente-carta);
        }
        h1 {
            font-family: var(--fuente-titulo); font-size: clamp(2.5rem, 10vw, 5rem);
            color: #f63afd93; text-shadow: 3px 3px 10px var(--color-sombra-fuerte);
            text-align: center; margin-bottom: 40px; line-height: 1.1;
        }
        .contenedor { perspective: 1500px; }
        .envoltura-sobre {
            position: relative; width: 320px; height: 220px;
            cursor: pointer;
            filter: drop-shadow(0px 20px 25px var(--color-sombra-fuerte));
            animation: latido 2.5s infinite;
        }
        .envoltura-sobre.abierto { animation: none; }
        @keyframes latido {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.07); }
        }
        .sobre {
            position: absolute; width: 100%; height: 100%;
            background-color: var(--color-sobre-cuerpo);
            border-radius: 15px; box-shadow: inset 0 0 30px rgba(0,0,0,0.1);
        }
        .carta {
            position: fixed; top: 50%; left: 50%;
            width: 320px; height: auto;
            transform: translate(-50%, -40%) scale(1);
            opacity: 0; z-index: 1; pointer-events: none;
            background: var(--color-carta);
            border-radius: 10px; padding: 25px; box-sizing: border-box;
            background-image: url('assets/papel.jpg');
            background-size: cover; background-position: center;
        }
        .envoltura-sobre.abierto .carta {
            opacity: 1;
            transform: translate(-50%, -50%) scale(1.05);
            pointer-events: auto;
        }
        .contenido { color: var(--color-texto); font-family: var(--fuente-carta); width: 100%; height: 100%; overflow: auto; }
        .contenido .fecha { display: block; text-align: right; font-size: 1.1rem; font-family: var(--fuente-fecha); font-style: italic; color: #666; margin-bottom: 20px; }
        .contenido .saludo { font-size: 2rem; margin-bottom: 15px; }
        .contenido .cuerpo { font-size: 1.2rem; line-height: 1.5; margin-bottom: 20px; }
        .contenido .firma { font-size: 2rem; text-align: right; color: var(--color-firma); margin: 0; }
        .contenido img { display: block; margin: 20px auto; max-width: 200px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.2); }
    </style>
</head>
<body>
    <main class="main-content">
        <h1>Un Mensaje Especial</h1>
        <div class="contenedor">
            <div class="envoltura-sobre" id="sobre">
                <div class="sobre"></div>
                <div class="carta">
                    <div class="contenido">
                        <span class="fecha">Siempre en mi corazón</span>
                        <p class="saludo">Querida Damaris,</p>
                        <p class="cuerpo">Hay personas que llegan a nuestra vida para marcarla para siempre, y tú eres una de ellas. No solo fuiste una amiga, sino alguien que se convirtió en una parte muy especial de mi historia.</p>
                        <img src="assets/amistad.jpg" alt="Recuerdo especial">
                        <p class="cuerpo">Cada recuerdo contigo me trae alegría, y aunque las palabras a veces se quedan cortas, quiero que sepas lo agradecido que estoy por todo lo que compartimos.</p>
                        <p class="cuerpo">Eres alguien invaluable para mí, y siempre tendrás un lugar único en mi vida. 🌹</p>
                        <p class="firma">Con mucho cariño,<br>Un niño que te quiere mucho</p>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <audio id="musica" src="assets/musica.mp3" autoplay loop></audio>

    <script>
        const sobre = document.getElementById("sobre");
        const musica = document.getElementById("musica");
        sobre.addEventListener("click", () => {
            sobre.classList.toggle("abierto");
            if(sobre.classList.contains("abierto")){
                musica.play().catch(e => console.log("Autoplay bloqueado, inicia manualmente."));
            } else {
                musica.pause();
                musica.currentTime = 0;
            }
        });
    </script>
</body>
</html>
