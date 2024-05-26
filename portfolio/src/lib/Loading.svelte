<script>

    const screens = [ 'https://w.wallhaven.cc/full/3l/wallhaven-3l8vzv.jpg', 'https://w.wallhaven.cc/full/ne/wallhaven-new1ew.jpg', 'https://w.wallhaven.cc/full/ox/wallhaven-oxelvp.jpg'  ]
    

</script>


    <div class="project01"  style="background-image: url({screens[0]});" >
    </div>
    <div class="text1">
        <p>I'm Andre Jo, a passionate programmer currently studying at the Universidad del Valle de Guatemala. I specialize in seamlessly connecting frontend and backend technologies to create dynamic web applications. I advocate for the synergy between frontend and backend development, where seamless integration enhances a digital product's functionality and aesthetics. My expertise includes backend technologies like Python, Java, and Node.js, as well as frontend technologies such as HTML, CSS, and JavaScript. I'm driven by a constant thirst for knowledge, always seeking to expand my skill set and deepen my understanding of software development. Let's connect, collaborate, and code the future together.</p>
        <button>Get Started</button>
        <div class="foto" style="background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTQxHUOYmNClfAMmDMFEfn7IyQfFwPVxJVu1n3wVXmatA&s');"></div>
    </div>
    

<style>

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
        animation-duration: 10s;
        position: relative;
        transform-style: preserve-3d;
        border-radius: 0px;
        
    }

    .project01::before {
    content: "";
    position: absolute; 
    inset: 0px;
    background: conic-gradient(from 90deg at 40% -25%, #1B2A41, #1B2A41, #1B2A41, #1B2A41, #324A5F, #324A5F, #CCC9DC, #CCC9DC, #CCC9DC, #CCC9DC, #CCC9DC, #CCC9DC, #CCC9DC, #CCC9DC, #CCC9DC, #CCC9DC);
    filter: blur(10px);
    transform: translate3d(25px,27px,-1px);
    border-radius: inherit;
    pointer-events: none;
    rotate: 1deg;
    }

    button{
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
    
    button:hover{
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
        0%   { height: 80vh; width: 90vw;}
        50% {height: 70vh; width: 88vw; }
        100%   {height: 80vh; width: 90vw;}

        
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