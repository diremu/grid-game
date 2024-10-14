<script>
  import Square from './Square.svelte';

  // Initialize a 4x4 grid filled with 0s
  let gridArray = Array(4).fill().map(() => Array(4).fill(0));

  // Add a random 2 to the grid at the start
  function spawnRandom() {
    let emptyCells = [];
    gridArray.forEach((row, rowIndex) =>
      row.forEach((cell, colIndex) => {
        if (cell === 0) emptyCells.push({ rowIndex, colIndex });
      })
    );

    if (emptyCells.length > 0) {
      let randomCell = emptyCells[Math.floor(Math.random() * emptyCells.length)];
      gridArray[randomCell.rowIndex][randomCell.colIndex] = 2;
    }
  }

  // Handle keydown events for tile movement (basic setup)
  function handleKeydown(event) {
    if (event.key === 'ArrowLeft') {
      console.log('Move Left');
      // TODO: Implement tile shifting logic
    } else if (event.key === 'ArrowRight') {
      console.log('Move Right');
    } else if (event.key === 'ArrowUp') {
      console.log('Move Up');
    } else if (event.key === 'ArrowDown') {
      console.log('Move Down');
    }
    spawnRandom(); // Add a new tile after each move
  }

  // Add the first tile when the app starts
  spawnRandom();

  // Listen for key presses
  window.addEventListener('keydown', handleKeydown);
</script>

<!-- Render the grid -->
<div class="grid">
  {#each gridArray as row, rowIndex}
    <div class="row">
      {#each row as cell, colIndex}
        <Square value={cell} />
      {/each}
    </div>
  {/each}
</div>

<style>
  .grid {
    display: grid;
    gap: 10px;
    margin: 20px;
  }

  .row {
    display: flex;
    gap: 10px;
  }
</style>
