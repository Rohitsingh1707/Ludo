<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Mini Ludo Dice Game</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f8f8f8;
    }
    h1 {
      color: #4CAF50;
    }
    .dice {
      font-size: 100px;
      margin: 20px;
    }
    button {
      padding: 10px 20px;
      font-size: 20px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    button:hover {
      background-color: #45a049;
    }
    .player-turn {
      font-size: 24px;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <h1>Mini Ludo Dice Game</h1>
  <div class="player-turn" id="turn">Player 1's Turn</div>
  <div class="dice" id="dice">🎲</div>
  <button onclick="rollDice()">Roll Dice</button>  <script>
    let currentPlayer = 1;

    function rollDice() {
      const dice = document.getElementById("dice");
      const turn = document.getElementById("turn");
      const roll = Math.floor(Math.random() * 6) + 1;

      const diceFaces = ["", "⚀", "⚁", "⚂", "⚃", "⚄", "⚅"];
      dice.innerHTML = diceFaces[roll];

      alert(`Player ${currentPlayer} rolled a ${roll}`);

      currentPlayer = currentPlayer === 1 ? 2 : 1;
      turn.innerText = `Player ${currentPlayer}'s Turn`;
    }
  </script></body>
</html>
