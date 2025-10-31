# otra_prueba
6:08 de la noche creo que voy por buen caminmo nose no creo
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Preguntas Casual</title>
</head>
<body>
  <h1>Preguntas casuales</h1>
  <button id="mostrarPregunta">Hazme una pregunta</button>
  <p id="pregunta"></p>

  <script>
    const preguntas = [
      "¿Qué tal tu día?",
      "¿Cómo te ha ido hoy?",
      "¿Qué cuentas de nuevo?",
      "¿Todo bien por ahí?",
      "¿Cómo te sientes ahora?"
    ];

    const boton = document.getElementById('mostrarPregunta');
    const parrafo = document.getElementById('pregunta');

    boton.addEventListener('click', () => {
      const indice = Math.floor(Math.random() * preguntas.length);
      parrafo.textContent = preguntas[indice];
    });
  </script>
</body>
</html>
