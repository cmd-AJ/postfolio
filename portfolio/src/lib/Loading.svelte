<script>
    import Carousel from './Carousel.svelte'
    import Modal from './Modal.svelte';
    import Consolemenu from './Consolemenu.svelte';
    let showModal = false
    const screens = [ 'https://w.wallhaven.cc/full/3l/wallhaven-3l8vzv.jpg', 'https://w.wallhaven.cc/full/ne/wallhaven-new1ew.jpg', 'https://w.wallhaven.cc/full/ox/wallhaven-oxelvp.jpg'  ]
    $: nombre = '/Invitados: ~$ '
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

    function keypress(event){
        if( event.key == 'Enter'){
            event.preventDefault()
            console.log( "Le dio enter" )
            const dato = document.getElementById('spans')
            comando = '/Invitados: ~$ ' + dato.innerText
            dato.innerText = ''
        }
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
        <div class="foto" style="background-image: url('./yo.png');"></div>
    </div>
    <div id=tecno class="tecnologias"><h1 style=" font-size:6vh; text-align: center;">Proyectos</h1></div>
    <div class="tec" >
        <Carousel></Carousel>
    </div>

    <button on:click={() => (showModal = true)} class="tooltip" ><u>Help with console? </u></button>

    

    <Modal bind:showModal>
        <h2 slot="header">
            Terminal use!
        </h2>

        <p>To use this terminal to search for my technologies, projects, or works I've done, we will start with the simple commands.</p>

        <p>Command: <strong>ls</strong>   -- Shows mostly all my folder directory</p>
        <p>Command: <strong>cd</strong>   -- To enter into a directory</p>

        <p> <i> Note:</i> this a simple terminal with only these two commands.</p>
    

    </Modal>

    <div class="console">
        {nombre}
        <span  on:keydown={keypress} tabindex="0" style="min-width: 30px; margin-right: 6px; white-space: nowrap; height:20px" class="input" role="textbox" id="spans" contenteditable></span>
        {flicker}
        <!-- <Console bind:showModal ></Console> -->
    </div>

    <div class="consolemenu"><Consolemenu answer={comando}></Consolemenu></div>


    <footer>
        <div class="footer">
          <button on:click={() => window.location.href = 'https://www.linkedin.com/in/andre-jo-6a6b2422b/'}  style="margin-left: 1vw;" class="butto"><img class="" src="./linkedin.svg" alt="d"></button>
          <button on:click={() => window.location.href = 'https://github.com/cmd-AJ'} class="butto"> <img src="./github.svg" alt="d"></button>
        </div>
    </footer>

<style>

.footer{
    display: flex;
  }

.butto{
    background-color: #0C1821;
    border: 0px;
  }
  .butto:hover{
    background-color: #324A5F;
    border: 0px;
  }

  footer{
    width: 100%;
    height: 8vh;
    margin-top: 6%;
    display: flex;
    flex-direction: row;
    background-color: #0C1821 ;
  }

  img{
    width: 46px;
  }
    
    .consolemenu{
        width: 90vw;
        height: 40vh;
        background-color: #0C1821;
        margin-top: 9% ;
        color: #CCC9DC;
        margin-right: 4%;
        margin-left: 3%;
        border: 2px solid #CCC9DC;
        border-radius: 20px;
        padding: 2%;


    }

    .input{
        color: #CCC9DC;
        outline: none;
        border: 0px;

    }

    .input::placeholder{
        color:#CCC9DC
    }
    

    .console{
        margin-top: 5%;
        margin-left: 2%;
        width: 68vw;
        height: 4vh;
        background-color: rgb(0, 0, 0);
        display: flex;
        flex-direction: row;
        color: #CCC9DC;
        border-top: 5px solid white;
        border-right: 5px solid white;
        padding-top: 1%;
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

        /* HTML: <div class="tooltip">This is a Speech Bubble with a gradient coloration and with border radius </div> */
    .tooltip {
    color: #CCC9DC;
    font-size: 2vh;
    max-width: 23vw;
    text-align: center;
    position: relative;
    left: 75vw;
    top: 20vh;
    border: 0px;
    }
    .tooltip {
    /* triangle dimension */
    --b: 2em; /* base */
    --h: 1em; /* height */

    --p: 0%; /* triangle position (0%:top 100%:bottom) */
    --r: 1.2em; /* the radius */

    padding: 1em;
    border-radius: var(--r)/min(var(--r),var(--p) - var(--b)/2) var(--r) var(--r) min(var(--r),100% - var(--p) - var(--b)/2);
    background: 100%/calc(100% + var(--h)) 100% 
        linear-gradient(-45deg,#1B2A41,#324A5F); /* the gradient */
    position: relative;
    z-index: 0;
    }
    .tooltip:before {
    content: "";
    position: absolute;
    z-index: -1;
    inset: 0 0 0 calc(-1*var(--h));
    background-image: inherit;
    clip-path: polygon(var(--h) max(0%,var(--p) - var(--b)/2),0 var(--p),var(--h) min(100%,var(--p) + var(--b)/2),50% 50%);
    }

    .tooltip:hover {
    transform: scale(1.2);
    }

    .tecnologias{
        width: 100vw;
        margin-top: 10%;
        height: 14vh;
        
        background-color: #000000;
        color: #CCC9DC;
    }

    .foto{
        max-width: 19vw;
        height: 72vh;
        position: relative;
        right: 25vw;
        bottom: 44vh;
        animation: grandepeqs 20s;
        padding: 2%;
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

    a{
        color: #CCC9DC;
    }

    .buttons{
        background-color: #ccc9dc00;
        color: #CCC9DC;
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
        padding: 2vw;
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

    @keyframes grandepeqs {
    0%   { transform: scale(1) translate(0, 0); }
    50%  { transform: scale(1.05) translate(10px, -10px); }
    100% { transform: scale(1) translate(0, 0); }
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