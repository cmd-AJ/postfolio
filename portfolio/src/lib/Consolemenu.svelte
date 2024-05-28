<script>
	export let answer;
    $:dirs = answer

    import Tecnologies from './Tecnologies.svelte'

    const array = [ { carpeta:'Tecnologies', url:"/Invitados: ~$ cd Tecnologies"}, {carpeta:'Experience'},   ]

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

{#if dirs.trim() === ("/Invitados: ~$ cd Tecnologies")}
    <div>
        <Tecnologies></Tecnologies>
    </div>
{/if}

{#if dirs.trim() === ("/Invitados: ~$ cd ..") || dirs.trim() === ("/Invitados: ~$ cd ..") }
    <div>
        sakpda
    </div>
{/if}


<style>

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
