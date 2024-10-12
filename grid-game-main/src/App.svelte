<script>
  import './app.css'
  import Navbar from './components/Navbar.svelte';
  import Square from './components/Square.svelte';
  import Grid from './components/Grid.svelte';

  let name = "Diremu"
  let age = 19
  let number = 0;

  function addNumber () {
    number = number + 1
  }
</script>

<main>
  <Navbar />
  <Square/>
  <Square />
  <Grid />
</main>

<style>
</style>
