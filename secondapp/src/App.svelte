<script>
  let winner = null;
  import Square from "./square.svelte";
  let square = [null, null, null, null, null, null, null, null, null];
  let xIsNext = true;

  let chance = "X";
  function handleclick(i) {
    if (!square[i]) {
      square[i] = xIsNext ? "X" : "O";
      xIsNext = !xIsNext;
      chance = xIsNext ? "X" : "O";
      winner = calculatewinner(square);
    }
  }
  function calculatewinner(square) {
    const winningcombo = [
      [0, 1, 2],
      [3, 4, 5],
      [6, 7, 8],
      [0, 3, 6],
      [1, 4, 7],
      [2, 5, 8],
      [0, 4, 8],
      [2, 4, 6],
    ];

    for (let i = 0; i < winningcombo.length; i++) {
      const [a, b, c] = winningcombo[i];
      if (square[a] && square[a] === square[b] && square[a] === square[c])
        return `Winner: ${square[a]}`;
        
    }
    const isDraw = square.every((square) => square !== null);
    return isDraw ? "It's a draw" : null;
  }

  function restartGame(){
    square=[null, null, null, null, null, null, null, null, null];
    xIsNext = true;
    winner = null;
  }
 
</script>

<main>
  <h1>TIC-TAC-TOE</h1>

  {#if winner}
    <h3>{winner}</h3>
  {:else}
    <h3>PLAYER'S TURN: {chance}</h3>
  {/if}
  <div class="board">
    {#each square as square, i}
      <Square value={square} handleClick={() => handleclick(i)} />
    {/each}
 
  </div>

  {#if winner}
  <button on:click={restartGame}>Restart Game</button>
  {/if}
</main>

<style>
  .board {
    display: flex;
    flex-wrap: wrap;
    width: 300px;
  }
</style>
