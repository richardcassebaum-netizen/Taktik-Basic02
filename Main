<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Taktik-Basis (Demo)</title>
  <style>
    body {
      background-color: #222;
      color: #eee;
      font-family: monospace, monospace;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: flex-start;
      height: 100vh;
    }
    header {
      background: #333;
      width: 100%;
      padding: 1rem;
      text-align: center;
      font-size: 1.5rem;
      font-weight: bold;
      letter-spacing: 2px;
    }
    #game {
      margin: 2rem;
      width: 320px;
      height: 320px;
      background: #444;
      display: grid;
      grid-template-columns: repeat(8, 1fr);
      grid-template-rows: repeat(8, 1fr);
      gap: 2px;
      border: 2px solid #666;
      box-sizing: border-box;
    }
    .tile {
      background: #555;
      border-radius: 3px;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      user-select: none;
      font-size: 1.2rem;
      color: #ccc;
    }
    .tile.active {
      background: #0f0;
      color: #030;
      font-weight: bold;
    }
    #info {
      margin-top: 1rem;
      font-size: 1rem;
    }
  </style>
</head>
<body>
  <header>Taktik-Basis (Demo)</header>
  <div id="game"></div>
  <div id="info">Wähle ein Feld, um deinen Zug zu starten.</div>

  <script>
    const gridSize = 8;
    const gameEl = document.getElementById('game');
    const infoEl = document.getElementById('info');

    const tiles = [];
    let activeTile = null;

    function createGrid() {
      for (let i = 0; i < gridSize * gridSize; i++) {
        const tile = document.createElement('div');
        tile.classList.add('tile');
        tile.dataset.index = i;
        tile.textContent = '-';
        tile.addEventListener('click', () => onTileClick(i));
        gameEl.appendChild(tile);
        tiles.push(tile);
      }
    }

    function onTileClick(index) {
      if (activeTile !== null) {
        tiles[activeTile].classList.remove('active');
      }
      activeTile = index;
      tiles[index].classList.add('active');
      infoEl.textContent = `Feld ${index + 1} ausgewählt.`;
    }

    createGrid();
  </script>
</body>
</html>
