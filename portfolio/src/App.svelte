<script>
  import Loader from './lib/Loader.svelte';
</script>

<header></header>

<main>
  <div >
    <Loader
	this={() => import('./lib/Loading.svelte')}
>
	<div class="loader" slot="fallback">
		loading...
  </div>
</Loader>
    <!-- <Loading></Loading> -->
  </div>
</main>




<style>
  
  :root{
    background-color: black;
    
  }

  header{
    background-color: #0C1821;
    padding: 0%;
    margin: 0%;

  }
  .loader {
    margin-top: 50vh;
    margin-left: 40vw;
    display: inline-flex;
    border: 2px solid #8a3737;
    --c:no-repeat linear-gradient(#d80e0e 0 0) 50%;
    background:
      var(--c) calc(50% - 5px)/5px 5px,
      var(--c) calc(50% + 5px)/5px 5px;
  }
  .loader::before,
  .loader::after {
    content: "12 00 23 40 31 45 60 17 45 32 29 42 50 08 14 07 46 11 03 55";
    font-size: 30px;
    font-family: monospace;
    font-weight: bold;
    line-height: 1em;
    height: 1em;
    width: 2ch;
    color: #5c040400;
    text-shadow: 0 0 0 #c74242;
    overflow: hidden;
    margin: 5px 10px; 
    animation: l3 1s steps(20) infinite;
  }
  .loader::before {
    animation-duration: 1.5s;
  }
  @keyframes l3 {
    100% {text-shadow: 0 -20em 0 #4e0c0c}
  }
    



</style>