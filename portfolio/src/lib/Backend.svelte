<script>

    const tecnologias = [
        { id:"python", imagen:"../src/assets/python.svg" },
        { id:"java", imagen:"../src/assets/java.svg" },
        { id:"javascript", imagen:"../src/assets/javascript.svg" },
        { id:"C++", imagen:"../src/assets/cplus.svg" }
    ]

</script>

<div style="display: flex;">

    <div><img class="svelte"  src={tecnologias[0].imagen} alt="">
    </div>

    <div><img class="svelte" src={tecnologias[1].imagen} alt="">
        </div>
    
    <div><img class="ionic" style="height: 18vh;" src={tecnologias[2].imagen} alt="">
    </div>

    <div style="display: flex;">
        <img class="htmls" style="height: 18vh;" src={tecnologias[3].imagen} alt="">
    </div>



</div>



<style>

    .htmls{
        position: relative; 
        right: 0%;
        top: 20%;
        animation: ziims 10s infinite;
        margin-left: 20%;
    }

    img{
        width: 20vw;
        height: 25vh;
    }
    .ionic{
        animation: ziim 20s infinite;
        display: flex;
        justify-content: center;
        margin-top: 15%;
        margin-left: 20%;

    }
    .svelte{
        animation: ziim 20s infinite;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-left: 20%;

    }
    
    @keyframes rotation {
    from { rotate: 360deg;}
    to {background-color: 0deg;}
    }

    @keyframes ziim {
        from {
			transform: scale(0.75);
		}
		to {
			transform: scale(0.9);
		}
    }

    @keyframes ziims {
        from {
			transform: scale(0.75);
		}
		to {
			transform: scale(1);
		}
    }

</style>