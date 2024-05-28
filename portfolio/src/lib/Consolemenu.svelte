<script>
	export let answer;
    $:dirs = answer

    import Tecnologies from './Tecnologies.svelte'
    import Backend from './Backend.svelte';
    import Osystem from './Osystem.svelte'

    const array = [ { carpeta:'frontend', url:"/Invitados: ~$ cd frontend"},
     {carpeta:'experience', url:"/Invitados: ~$ cd experience"}, 
     {carpeta:'backend', url:"/Invitados: ~$ cd backend"},
     {carpeta:'tools', url:"/Invitados: ~$ cd tools"}
      ]

    function cambiarroute(dir){
        dirs = dir
    }

</script>

<p>{dirs}</p>


{#if dirs.trim() === ("/Invitados: ~$ ls")}
    <div>
        {#each array as { carpeta, url }}
                    <button on:click={() => cambiarroute(url)} ><u>{carpeta}</u></button>
        {/each}
    </div>
{/if}

{#if dirs.trim() === ("/Invitados: ~$ cd frontend")}
    <div>
        <Tecnologies></Tecnologies>
    </div>
{/if}

{#if dirs.trim() === ("/Invitados: ~$ cd backend")}
    <div>
        <Backend></Backend>
    </div>
{/if}

{#if dirs.trim() === ("/Invitados: ~$ cd experience")}
    <div>
        <li > <strong>Auxiliar de Programación Basica </strong>: 2024 </li>
    </div>
{/if}

{#if dirs.trim() === ("/Invitados: ~$ cd tools")}
    <div>
        <Osystem></Osystem>
    </div>
{/if}

{#if dirs.trim() === ("/Invitados: ~$ cd") || dirs.trim() === ("/Invitados: ~$ cd ..") }
    <div class="loader">
        
    </div>
{/if}




<style>

        /* HTML: <div class="loader"></div> */
    .loader {
    width: 50px;
    height: 20px;
    scale: 1.5;
    left: 45vw;
    top: 10vh;
    --c:no-repeat radial-gradient(farthest-side,#CCC9DC 93%,#0000);
    background:
        var(--c) 0    0,
        var(--c) 50%  0,
        var(--c) 100% 0;
    background-size: 8px 8px;
    position: relative;
    animation: l4-0 1s linear infinite alternate;
    }
    .loader:before {
    content: "";
    position: absolute;
    width: 8px;
    height: 12px;
    background: #324A5F;
    left: 0;
    top: 0;
    animation: 
        l4-1 1s  linear infinite alternate,
        l4-2 0.5s cubic-bezier(0,200,.8,200) infinite;
    }
    @keyframes l4-0 {
    0%      {background-position: 0  100%,50% 0   ,100% 0}
    8%,42%  {background-position: 0  0   ,50% 0   ,100% 0}
    50%     {background-position: 0  0   ,50% 100%,100% 0}
    58%,92% {background-position: 0  0   ,50% 0   ,100% 0}
    100%    {background-position: 0  0   ,50% 0   ,100% 100%}
    }
    @keyframes l4-1 {
    100% {left:calc(100% - 8px)}
    }
    @keyframes l4-2 {
    100% {top:-0.1px}
    }

    li{
        font-size: 4vh;
        margin-left: 7%;
    }

    button{
        background-color: #0C1821;
        color: #CCC9DC;
        border: 0px;
        font-size: 4vh;
        margin-left: 2%;
    }

    button:hover{
        color: white;

    }

</style>
