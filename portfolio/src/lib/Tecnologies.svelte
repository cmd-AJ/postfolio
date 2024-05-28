<script>

    const tecnologias = [
        { id:"React", imagen:"/react.svg" },
        { id:"Svelte", imagen:"/svelte.svg" },
        { id:"Ioinic", imagen:"/ionic.svg" },
        { id:"javascript", imagen:"/javascript.svg" },
        { id:"html", imagen:"/html5.svg" },
        { id:"css", imagen:"/css3.svg" },

    ]

</script>

<div style="display: flex;">

    <div><img class="react"  src={tecnologias[0].imagen} alt="">
    </div>

    <div><img class="svelte" src={tecnologias[1].imagen} alt="">
        </div>
    
    <div><img class="ionic" style="height: 18vh;" src={tecnologias[2].imagen} alt="">
    </div>

    <div style="display: flex;">
        <img class="htmls" style="height: 18vh;" src={tecnologias[4].imagen} alt="">
        <img class="css3" style="height: 18vh;" src={tecnologias[5].imagen} alt="">
    </div>



</div>



<style>

    .jss{
        position: relative;   
        top: 5px;
    }
    .htmls{
        position: relative; 
        right: 0%;
        top: 20%;
        animation: ziims 10s infinite;
    }

    .css3{
        position: relative; 
        right: 25%;
        top: 20%;
        animation: ziims 10s infinite;
    }

    img{
        width: 20vw;
        height: 25vh;
    }
    

    .react{
        animation: rotation 20s infinite;
        display: flex;
        justify-content: center;
        align-items: center;

    }
    .ionic{
        animation: rotation 20s infinite;
        display: flex;
        justify-content: center;
        margin-top: 15%;

    }
    .svelte{
        animation: ziim 20s infinite;
        display: flex;
        justify-content: center;
        align-items: center;

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