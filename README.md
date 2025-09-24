<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Un Mensaje Especial para ti Damaris</title>

  <!-- Fuentes -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Lora:ital,wght@1,400&family=Parisienne&display=swap" rel="stylesheet">

  <!-- Favicon emoji -->
  <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>💌</text></svg>">

  <style>
    :root {
      --color-fondo-gradiente-1: #e0c3fc;
      --color-fondo-gradiente-2: #8ec5fc;
      --color-sobre-cuerpo: #ffdde1;
      --color-sobre-solapa: #eeb7c2;
      --color-carta: #fff;
      --color-sello: #cf425c;
      --color-sombra-fuerte: rgba(0, 0, 0, 0.25);
      --color-texto: #3a3a3a;
      --fuente-titulo: 'Great Vibes', cursive;
      --fuente-carta: 'Parisienne', cursive;
    }

    body {
      margin: 0;
      padding: 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      background: linear-gradient(135deg, var(--color-fondo-gradiente-1), var(--color-fondo-gradiente-2));
      font-family: var(--fuente-carta);
    }

    h1 {
      font-family: var(--fuente-titulo);
      font-size: clamp(2.5rem, 8vw, 4rem);
      color: #f63afd93;
      text-shadow: 2px 2px 10px var(--color-sombra-fuerte);
      text-align: center;
      margin-bottom: 30px;
    }

    .contenedor {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .envoltura-sobre {
      position: relative;
      width: 320px;
      height: 220px;
      cursor: pointer;
      perspective: 1000px;
    }

    .sobre {
      width: 100%;
      height: 100%;
      background: var(--color-sobre-cuerpo);
      border-radius: 10px;
      box-shadow: 0px 10px 20px var(--color-sombra-fuerte);
      position: relative;
      overflow: hidden;
    }

    .solapa {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 50%;
      background: var(--color-sobre-solapa);
      clip-path: polygon(0 0, 100% 0, 50% 100%);
      transform-origin: top;
      transition: transform 1s ease;
      z-index: 2;
    }

    .sobre.abierto .solapa {
      transform: rotateX(180deg);
    }

    .carta {
      position: absolute;
      top: 0;
      left: 50%;
      transform: translateX(-50%) translateY(100%);
      width: 280px;
      height: 180px;
      background: var(--color-carta);
      border-radius: 5px;
      padding: 20px;
      box-shadow: 0px 10px 20px var(--color-sombra-fuerte);
      text-align: center;
      opacity: 0;
      transition: all 1s ease;
      z-index: 1;
    }

    .sobre.abierto .carta {
      transform: translateX(-50%) translateY(-20%);
      opacity: 1;
    }

    .carta p {
      margin: 0;
      color: var(--color-texto);
    }

    .carta .saludo {
      font-size: 1.5rem;
      margin-bottom: 10px;
    }

    .carta .cuerpo {
      font-size: 1.1rem;
      margin-bottom: 15px;
    }

    .carta .firma {
      font-size: 1.3rem;
      color: var(--color-sello);
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="contenedor">
    <h1>Un Mensaje Especial para ti, Damaris</h1>
    <div class="envoltura-sobre" id="sobre">
      <div class="sobre">
        <div class="solapa"></div>
        <div class="carta">
          <p class="saludo">Querida Damaris,</p>
          <p class="cuerpo">Quiero que sepas lo mucho que significas para mí. Tu sonrisa ilumina mis días y tu amistad es un regalo invaluable.</p>
          <p class="firma">Con todo mi cariño 💌</p>
        </div>
      </div>
    </div>
  </div>

  <script>
    const sobre = document.getElementById("sobre");
    sobre.addEventListener("click", () => {
      sobre.querySelector(".sobre").classList.toggle("abierto");
    });
  </script>
</body>
</html>
