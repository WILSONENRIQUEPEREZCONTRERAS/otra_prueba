# otra_prueba

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Hola Mundo Creativo</title>
  <style>
    /* Fondo degradado animado */
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(-45deg, #ff9a9e, #fad0c4, #a1c4fd, #c2e9fb);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
    }

    @keyframes gradientBG {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    /* Estilo del texto */
    h1 {
      font-size: 4rem;
      color: white;
      text-shadow: 2px 2px 8px rgba(0,0,0,0.3);
      animation: bounce 2s infinite;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }

    /* Botón interactivo */
    button {
      margin-top: 20px;
      padding: 10px 25px;
      font-size: 1.2rem;
      border: none;
      border-radius: 12px;
      cursor: pointer;
      background-color: #ff6f91;
      color: white;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: #ff4757;
      transform: scale(1.1);
    }
  </style>
</head>
<body>
  <div style="text-align:center;">
    <h1 id="holaMundo">Hola Mundo 🌎</h1>
    <button id="cambiarTexto">Hazme saludar</button>
  </div>

  <script>
    const texto = document.getElementById('holaMundo');
    const boton = document.getElementById('cambiarTexto');

    const saludos = [
      "¡Hola Mundo! 😄",
      "¡Hola Universo! ✨",
      "¡Hey tú! 👋",
      "¡Saludos desde GitHub! 🖤",
      "¡Hola, programador/a! 💻"
    ];

    boton.addEventListener('click', () => {
      const indice = Math.floor(Math.random() * saludos.length);
      texto.textContent = saludos[indice];
    });
  </script>
</body>
</html>



   
