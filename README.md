<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Candado Seguro</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #2c3e50;
            font-family: Arial, sans-serif;
            color: white;
            text-align: center;
        }
        .candado {
            background-color: #f1c40f;
            width: 120px;
            height: 160px;
            border-radius: 15px;
            position: relative;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.3);
        }
        .candado::before {
            content: "";
            width: 60px;
            height: 60px;
            background-color: transparent;
            border: 8px solid #f1c40f;
            border-radius: 50%;
            position: absolute;
            top: -40px;
            left: 50%;
            transform: translateX(-50%);
        }
        input {
            margin-top: 10px;
            padding: 8px;
            font-size: 16px;
            text-align: center;
            border: 2px solid #333;
            border-radius: 5px;
        }
        button {
            margin-top: 10px;
            padding: 8px;
            font-size: 16px;
            background-color: #27ae60;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
        }
        button:hover {
            background-color: #219150;
        }
    </style>
</head>
<body>
    <div class="candado">
        <input type="password" id="codigo" placeholder="Ingrese código">
        <button onclick="verificarCodigo()">Desbloquear</button>
    </div>
    
    <script>
        function verificarCodigo() {
            const codigoCorrecto = "6648"; // Cambia esto a la combinación que desees
            const inputCodigo = document.getElementById("codigo").value.trim(); // Elimina espacios adicionales
            console.log("Código ingresado:", inputCodigo); // Muestra el código en la consola para depuración
            if (inputCodigo === codigoCorrecto) {
                alert("¡Candau desbloquejat! Ara haureu de sortir de l'habitació i buscar a algú de la CO.");
            } else {
                alert("Codi incorrecte. Fixeu-vos en tooots els detalls.");
            }
        }
    </script>
</body>
</html>
