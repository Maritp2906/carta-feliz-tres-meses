# carta-feliz-tres-meses
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>¡Feliz Tres Meses!</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f0f0f0;
            margin: 0;
        }

        .card {
            width: 300px;
            height: 200px;
            background: white;
            position: relative;
            perspective: 1000px;
        }

        .card-content {
            width: 100%;
            height: 100%;
            background-color: #FFB6C1;
            position: absolute;
            top: 0;
            left: 0;
            transform-style: preserve-3d;
            transform: rotateY(0);
            transition: transform 1s;
        }

        .card.open .card-content {
            transform: rotateY(180deg);
        }

        .card-content .front, .card-content .back {
            width: 100%;
            height: 100%;
            position: absolute;
            backface-visibility: hidden;
        }

        .card-content .front {
            background-color: #FF69B4;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 24px;
            color: white;
        }

        .card-content .back {
            background-color: #FFB6C1;
            transform: rotateY(180deg);
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        .back .heart {
            font-size: 64px;
            color: red;
            margin-bottom: 20px;
        }

        .back .message {
            font-size: 20px;
            color: #333;
        }

        button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: #FF69B4;
            color: white;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #FF1493;
        }
    </style>
</head>
<body>

    <div class="card" id="card">
        <div class="card-content">
            <div class="front">
                ¡Haz clic para abrir la carta!
            </div>
            <div class="back">
                <div class="heart">❤️</div>
                <div class="message">¡Feliz tres meses!</div>
            </div>
        </div>
    </div>

    <button onclick="abrirCarta()">Abrir Carta</button>

    <script>
        function abrirCarta() {
            const card = document.getElementById('card');
            card.classList.toggle('open');
        }
    </script>

</body>
</html>
