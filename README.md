<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Lora:ital,wght@1,400&family=Parisienne&display=swap" rel="stylesheet">
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>💌</text></svg>">

    <title>Un Mensaje Especial para Ti</title>

    <style>
        /* 🎨 Los mismos estilos originales, sin cambios */
        /* --- VARIABLES --- */
        :root {
            --color-fondo-gradiente-1: #e0c3fc;
            --color-fondo-gradiente-2: #8ec5fc;
            --color-sobre-cuerpo: #ffdde1;
            --color-sobre-solapa: #eeb7c2;
            --color-sobre-solapa-superior: #fbe2e7;
            --color-carta: #fdfbfb;
            --color-sello: #cf425c;
            --color-sombra-fuerte: rgba(0, 0, 0, 0.25);
            --color-sombra-suave: rgba(0, 0, 0, 0.1);
            --color-texto: #3a3a3a;
            --color-firma: #c91515;
            --fuente-titulo: 'Great Vibes', cursive;
            --fuente-fecha: 'Lora', serif;
            --fuente-carta: 'Parisienne', cursive;
            --duracion-apertura: 1.7s;
        }

        /* --- resto de tu CSS original aquí --- */
    </style>
</head>
<body>

    <div id="loader">
        <div class="loader-icon">💌</div>
        <div class="progress-bar-container">
            <div id="progress-bar" class="progress-bar"></div>
        </div>
        <div id="progress-percentage">0%</div>
    </div>
    
    <main class="main-content">
        <h1>Un Mensaje Especial para Ti</h1>

        <div class="contenedor">
            <div class="envoltura-sobre">
                <div class="sobre"></div>
                <div class="solapa solapa-superior"></div>
                <div class="solapa solapa-derecha"></div>
                <div class="solapa solapa-izquierda"></div>
                <div class="corazon"></div>
                <div class="carta">
                    <div class="contenido">
                        <span class="fecha">Siempre presente</span>
                        <p class="saludo">Querida Damaris,</p>
                        <p class="cuerpo">La amistad es uno de los tesoros más grandes de la vida, y yo tengo la fortuna de contar con la tuya.</p>
                        <p class="cuerpo">Gracias por tu compañía, por tu apoyo sincero y por esos momentos que se quedan grabados en el corazón.</p>
                        <p class="cuerpo">Quiero que sepas que siempre podrás contar conmigo, hoy y siempre. 💖</p>
                        
                        <div class="bloque-firma">
                            <img src="https://drive.google.com/thumbnail?id=1SsZk-dSh2jGsS2kGgCqhZIgeD9ZUi_jM" alt="Foto de recuerdo" class="imagen-recuerdo">
                            <p class="firma">Con mucho cariño,<br>Tu amigo</p>
                        </div>

                    </div>
                </div>
            </div>
        </div>
    </main>
    
    <audio id="sound" src="https://dl.dropboxusercontent.com/scl/fi/esct592hxwzjyf9a2egpc/Si-supieras-lo-que-siento-con-mirarte....mp3?rlkey=xqbaohnpyd7b3mejkvvdg6dlq&st=2vagx61x&dl=1" type="audio/mpeg" preload="auto"></audio>

    <!-- Tu JavaScript original aquí -->
</body>
</html>
