<script>
  // import './app.css'
  import Navbar from './components/Navbar.svelte';
  
  let name = "Diremu"
  let age = 19
  let number = 0;

  function addNumber () {
    number = number + 1
  }
</script>

<main>
  <Navbar />
</main>

<style>
</style>
