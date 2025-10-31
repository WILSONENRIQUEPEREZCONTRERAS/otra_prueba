# otra_prueba

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Preguntas y Respuestas</title>
</head>
<body>
  <h1>Preguntas casuales</h1>
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

    // Mostrar pregunta aleatoria
    botonPregunta.addEventListener('click', () => {
      const indice = Math.floor(Math.random() * preguntas.length);
      preguntaActual = preguntas[indice];
      parrafoPregunta.textContent = preguntaActual;
      parrafoRespuesta.textContent = ""; // Limpiar respuesta anterior
      inputRespuesta.value = ""; // Limpiar input
    });

    // Responder y dar feedback
    botonEnviar.addEventListener('click', () => {
      const userResp = inputRespuesta.value.trim();
      if(userResp === "") {
        parrafoRespuesta.textContent = "Por favor escribe algo antes de enviar.";
      } else {
        parrafoRespuesta.textContent = `¡Gracias por responder! Dijiste: "${userResp}"`;
      }
    });
  </script>
</body>
</html>
