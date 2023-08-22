<!DOCTYPE html>
<html>
<head>
    <title>Simple HTML5 Game</title>
    <style>
        /* Your game styles go here */
        #game-board {
            width: 400px;
            height: 400px;
            background-color: #ccc;
            position: relative;
        }

        #player {
            width: 50px;
            height: 50px;
            background-color: blue;
            position: absolute;
        }
    </style>
</head>
<body>
    <div id="game-board">
        <div id="player"></div>
    </div>

    <script>
        // JavaScript code for your game goes here
        const player = document.getElementById('player');
        const gameBoard = document.getElementById('game-board');

        let playerX = 0;
        let playerY = 0;

        function movePlayer(event) {
            switch (event.key) {
                case 'ArrowUp':
                    playerY -= 10;
                    break;
                case 'ArrowDown':
                    playerY += 10;
                    break;
                case 'ArrowLeft':
                    playerX -= 10;
                    break;
                case 'ArrowRight':
                    playerX += 10;
                    break;
            }

            player.style.left = playerX + 'px';
            player.style.top = playerY + 'px';
        }

        document.addEventListener('keydown', movePlayer);
    </script>
</body>
</html>
