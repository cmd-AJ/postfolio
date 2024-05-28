<script>
  import Headermenu from './lib/Headermenu.svelte';
  import Loading from './lib/Loading.svelte';
  import Mainproject from './lib/Mainproject.svelte';
</script>

<header></header>

<main>
  <div >
    <Loading></Loading>
  </div>
</main>

<footer>
</footer>


<style>
  
  :root{
    background-color: black;
    
  }

  header{
    background-color: #0C1821;
    padding: 0%;
    margin: 0%;

  }

  footer{
    width: 100%;
    height: 8vh;
    margin-top: 3%;
    display: flex;
    flex-direction: row;
    background-color: #CCC9DC ;
  }



</style>