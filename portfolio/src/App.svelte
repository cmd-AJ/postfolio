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
<button></button>
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
    margin-top: 100%;
    display: flex;
    flex-direction: row;
    background-color: #0C1821 ;
  }

  button{
        display: flex;
        width: vw;
        height: 8vh;
        background-size:cover;
        background-repeat: no-repeat;
        border: 0px;
        margin-bottom: 1vh;
    }

</style>