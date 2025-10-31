# otra_prueba


<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mini Chat de Preguntas</title>
</head>
<body>
  <h1>Mini Chat de Preguntas</h1>

  <button id="mostrarPregunta">Hazme una pregunta</button>
  <p id="pregunta"></p>

  <input type="text" id="respuestaUsuario" placeholder="Escribe tu respuesta aquí">
  <button id="enviarRespuesta">Enviar respuesta</button>
  <p id="respuesta"></p>

  <script>
    const preguntas = [
      "¿Qué tal tu día?",
      "¿Cómo te ha ido hoy?",
      "¿Qué cuentas de nuevo?",
      "¿Todo bien por ahí?",
      "¿Cómo te sientes ahora?"
    ];

    const botonPregunta = document.getElementById('mostrarPregunta');
    const parrafoPregunta = document.getElementById('pregunta');
    const inputRespuesta = document.getElementById('respuestaUsuario');
    const botonEnviar = document.getElementById('enviarRespuesta');
    const parrafoRespuesta = document.getElementById('respuesta');

    let preguntaActual = "";

    // Función para mostrar pregunta aleatoria
    botonPregunta.addEventListener('click', () => {
      const indice = Math.floor(Math.random() * preguntas.length);
      preguntaActual = preguntas[indice];
      parrafoPregunta.textContent = preguntaActual;
      parrafoRespuesta.textContent = "";
      inputRespuesta.value = "";
    });

    // Función para analizar respuesta
    botonEnviar.addEventListener('click', () => {
      const userResp = inputRespuesta.value.trim().toLowerCase();

      if(userResp === "") {
        parrafoRespuesta.textContent = "Por favor escribe algo antes de enviar.";
        return;
      }

      let mensaje = "";

      // Respuestas básicas según palabras clave
      if(userResp.includes("bien") || userResp.includes("genial") || userResp.includes("ok")) {
        mensaje = "¡Qué bueno! Me alegra saberlo 😊";
      } else if(userResp.includes("mal") || userResp.includes("cansado") || userResp.includes("triste")) {
        mensaje = "Vaya, espero que mañana sea un mejor día 💛";
      } else if(userResp.includes("nada") || userResp.includes("normal")) {
        mensaje = "Entiendo, a veces los días son tranquilos 😌";
      } else {
        mensaje = "Gracias por compartir, es interesante lo que me dices 🤔";
      }

      parrafoRespuesta.textContent = mensaje;
    });
  </script>
</body>
</html>


