<script>
    import Carousel from './Carousel.svelte'
    import Console from './Console.svelte';
    let showModal = false
    const screens = [ 'https://w.wallhaven.cc/full/3l/wallhaven-3l8vzv.jpg', 'https://w.wallhaven.cc/full/ne/wallhaven-new1ew.jpg', 'https://w.wallhaven.cc/full/ox/wallhaven-oxelvp.jpg'  ]
    $: nombre = '/Invitados: ~$'
    $: comando = ''
    $: flicker = '\u2588'

    setInterval( flick, 2001)
    setInterval( flicked, 1000)

        function flick() {
            flicker = '\u0020'
    }

    function flicked() {
            flicker =  '\u2588'
    }
    

    function handleclick({ target }) {
		const el = document.querySelector(target.getAttribute('href'));
		if (!el) return;
    el.scrollIntoView({
      behavior: 'smooth'
    });
  }


</script>


    <div class="project01"  style="background-image: url({screens[2]});" >
    </div>
    <div class="text1">
        <p><strong style="font-size: 3vh;">Andre Jo</strong>, passionate programmer currently studying at the Universidad del Valle de Guatemala. I specialize in seamlessly connecting frontend and backend technologies to create dynamic web applications. I advocate for the synergy between frontend and backend development, where seamless integration enhances a digital product's functionality and aesthetics. My expertise includes backend technologies like Python, Java, and Node.js, as well as frontend technologies such as HTML, CSS, and JavaScript. I'm driven by a constant thirst for knowledge, always seeking to expand my skill set and deepen my understanding of software development. </p>
        <button class="buttons" id="buttons" on:click={handleclick}><a href="#tecno" on:click|preventDefault={handleclick}>Get Started</a></button>
        <div class="foto" style="background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTQxHUOYmNClfAMmDMFEfn7IyQfFwPVxJVu1n3wVXmatA&s');"></div>
    </div>
    <div id=tecno class="tecnologias"><h1 style=" font-size:6vh; text-align: center;">Proyectos</h1></div>
    <div class="tec" >
        <Carousel></Carousel>
    </div>

    <div class="console">
        <button >Help with console?</button>
        {nombre}
        <span style="min-width: 30px; margin-right: 6px;" class="input" role="textbox" contenteditable>{comando}</span>
        {flicker}

        <!-- <Console bind:showModal ></Console> -->
    </div>

<style>
    
    .prueba{
        width: 100vw;
        height: 40vh;
        background-color: antiquewhite;

    }
    

    .console{
        margin-top: 5%;
        width: 50vw;
        height: 40vh;
        background-color: rgb(160, 160, 160);
        display: flex;
        flex-direction: row;
    }

    .comandline{
        min-width: 1px;
        width: 1px;
        height: 5vh;
        background-color: rgb(0, 0, 0);
        resize: none;

    }

    .tec{
            
        --s: 48px; /* control the size*/
        --c1: #000000;
        --c2: #ccc9dc;
        --c3: #324a5f;
        
        --b: calc(var(--s)/2.67); /* control the thickness of the wavy line */
        
        --_r: calc(1.28*var(--s) + var(--b)/2) at left 50%;
        --_f: calc(100% - var(--b)),var(--c1) calc(101% - var(--b)) 100%,#0000 101%;
        --g0: calc(-.8*var(--s)),var(--c2) var(--_f);
        --g1: calc(-.8*var(--s)),var(--c3) var(--_f);
        --_s: calc(1.5*var(--s) + var(--b));
        background: 
            radial-gradient(var(--_r) bottom var(--g0)) calc(2*var(--s)) calc(-1*var(--_s)),
            radial-gradient(var(--_r) bottom var(--g1)) calc(-1*var(--s)) calc(var(--_s)/-2),
            radial-gradient(var(--_r) top    var(--g1)) 0 var(--_s),
            radial-gradient(var(--_r) top    var(--g0)) var(--s) calc(var(--_s)/ 2),
            linear-gradient(var(--c2) 50%,var(--c3) 0);
        background-size: calc(4*var(--s)) var(--_s);
        padding-top: 2%;
        
        
    }

    .tecnologias{
        width: 100vw;
        margin-top: 10%;
        height: 14vh;
        
        background-color: #000000;
        color: #CCC9DC;
    }

    .foto{
        width: 20vw;
        height: 40vh;
        position: relative;
        right: 40%;
        bottom: 10%;
        background-size: cover;
    }

    .project01{
        width: 90vw;
        height: 80vh;
        display: flex;
        justify-content: center;
        margin-left: 5%;   
        margin-top: 5%;
        color: white;
        background-color: black;
        background-size: cover;
        rotate: -1deg;
        animation-name: grandepeq;
        animation-duration: 20s;
        position: relative;
        border-radius: 0px;
        
    }

    .buttons{
        background-color: #CCC9DC;
        border-radius: 20px;
        display: flex;
        margin-left: 80%;
        width: 10vw;
        height: 5vh;
        align-items: center;
        justify-content: center;
        font-size: 1.2vmax;
        

    }
    
    .buttons:hover{
        background-color: #0C1821;
        color: #CCC9DC;
        animation: borders 10s infinite;
    }

    .text1{
        width: 60vw;
        height: 35vh;
        margin: 15vh;
        margin-left: 30%;
        background-color: rgba(0, 0, 0, 0.747);
        color: white;
        padding: 2%;
        font-size: 1.2vmax;
        text-align: justify;
        font-family: sans-serif;
        word-wrap: break-word;
        position: absolute;
        top: 100px;
        right: 1%;
        border-radius: 30px;
        animation: borders 10s infinite;

    }

    @keyframes grandepeq {
        0%   { transform: scale(1);}
        50% { transform: scale(1.05); }
        100%   { transform: scale(1);}

        
    }

    @keyframes coolwaves {
        0%   { transform: scale(1);}
        50% { transform: scale(0.5); }
        100%   { transform: scale(1);}

        
    }
    

    @keyframes example {
        
        0%   {color:black; bottom: 20px;}
        25%  {color:#0C1821; bottom: 20px; }
        50%  {color:#1B2A41; bottom: 20px;}
        75%  {color:#CCC9DC; top: 100px;}
        100% {color:#324A5F }
    }

    @keyframes borders {
        0%   {border: 3px solid #CCC9DC}
        50% {border: 3px solid #324A5F }
        100%   {border: 3px solid #CCC9DC}

        
    }



    


</style>
  

<!-- https://coolors.co/000000-0c1821-1b2a41-324a5f-ccc9dc -->