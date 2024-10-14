<script>
  export let value = 0;
</script>

<div class="square {value === 2 ? 'bg-green-400' : ''}">
  {#if value !== 0}
    {value}
  {/if}
</div>

<style>
  .square {
    background-color: rgb(223, 223, 177);
    width: 60px;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    font-weight: bold;
    border-radius: 5px;
    transition: background-color 0.3s;
  }

  .green {
    background-color: rgb(16, 238, 16);
  }
</style>
