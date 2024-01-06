<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>¿Me perdonas?</title>
  <style>
    body {
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background-color: #f0f0f0;
    }

    #pregunta {
      font-size: 20px;
      margin-bottom: 20px;
    }

    #opciones {
      display: flex;
    }

    .opcion {
      cursor: pointer;
      padding: 10px;
      margin: 0 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      background-color: #fff;
    }

    .opcion:hover {
      background-color: #e0e0e0;
    }

    .opcion-no {
      pointer-events: none; /* Deshabilitar clics en la opción "No" */
      color: #888; /* Cambiar el color para indicar visualmente que está deshabilitada */
      position: fixed; /* Fijar posición */
      top: 50px; /* Ajustar la posición superior según sea necesario */
      left: 50px; /* Ajustar la posición izquierda según sea necesario */
    }
  </style>
</head>
<body>

<div id="pregunta">¿Me perdonas?</div>

<div id="opciones">
  <div class="opcion" onclick="responder('si')">Sí</div>
  <div class="opcion opcion-no" onclick="responder('no')">No</div>
</div>

<script>
  function responder(respuesta) {
    if (respuesta === 'si') {
      alert('Yo también te amo.');
    } else {
      alert('Respuesta: ' + respuesta);
    }

    // Deshabilitar las opciones después de la respuesta
    document.querySelectorAll('.opcion').forEach(function(opcion) {
      opcion.style.pointerEvents = 'none';
    });
  }
</script>

</body>
</html>
                  
