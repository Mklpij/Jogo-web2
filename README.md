<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jogo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }

        h1 {
            margin-top: 50px;
        }

        button {
            margin: 10px;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }

        #nao-btn {
            position: relative;
            top: 0;
            left: 0;
        }
    </style>
</head>
<body>

    <h1>Vamos jogar hoje?</h1>

    <button onclick="responder('sim')">Sim</button>
    <button id="nao-btn" onclick="moverBotao()">Não</button>

    <script>
        function responder(escolha) {
            if (escolha === 'sim') {
                window.location.href = 'https://www.youtube.com/watch?v=kqKDnZtOFYk'; // https://youtu.be/kqKDnZtOFYk?si=umYJOvT9rsvjTPRR
            } else {
                alert("Você escolheu: " + escolha);
            }
        }

        function moverBotao() {
            var naoBtn = document.getElementById("nao-btn");
            var novaPosicaoTop = Math.floor(Math.random() * window.innerHeight - naoBtn.clientHeight);
            var novaPosicaoLeft = Math.floor(Math.random() * window.innerWidth - naoBtn.clientWidth);
            
            naoBtn.style.top = novaPosicaoTop + "px";
            naoBtn.style.left = novaPosicaoLeft + "px";
        }
    </script>

</body>
</html>
