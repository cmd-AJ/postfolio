<script>
  import Headermenu from './lib/Headermenu.svelte';
  import Counter from './lib/Counter.svelte'
</script>

<header><Headermenu></Headermenu></header>

<main>
  <div >
    <Counter />
  </div>
</main>

<footer></footer>


<style>
  
  :root{
    background-color: #F5F5F5;
  }

  header{
    background-color: #E7E5E5;
    padding: 0%;
    margin: 0%;

  }



</style>