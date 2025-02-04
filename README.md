<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>San Valentín ❤️</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffe6e6;
        }
        .container {
            margin-top: 100px;
        }
        h1 {
            color: #d63384;
        }
        #message {
            font-size: 20px;
            color: #ff1493;
            display: none;
            margin-top: 20px;
        }
        button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        #yes {
            background-color: #ff4d88;
            color: white;
        }
        #no {
            background-color: #999;
            color: white;
            position: absolute;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>¿Quieres ser mi San Valentín? 💖</h1>
        <button id="yes" onclick="sayYes()">Sí</button>
        <button id="no" onmouseover="moveNo()">No</button>
        <p id="message"></p>
    </div>

    <script>
        function sayYes() {
            let messages = [
                "¡Sabía que dirías que sí! 💕",
                "Eres lo mejor que me ha pasado 😍",
                "Te amo con todo mi corazón 💖",
                "Juntos somos imparables 💑",
                "Eres mi persona favorita ❤️"
            ];
            let message = document.getElementById("message");
            message.innerText = messages[Math.floor(Math.random() * messages.length)];
            message.style.display = "block";
        }

        function moveNo() {
            let button = document.getElementById("no");
            let x = Math.random() * (window.innerWidth - 100);
            let y = Math.random() * (window.innerHeight - 100);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
    </script>

</body>
</html>
