<script>
// @ts-nocheck

	import Carousel from "svelte-carousel";
	const images = [
	  {
		url: './carblogs.mp4',
		description: "./react.svg",
	  },
	  {
		url: "./chat.mp4",
		description: "./javascript.svg",
	  },
	  {
		url: "./Ionic.mp4",
		description: "./ionic.svg",
	  },
	  {
		url: "./html.mp4",
		description: "./html5.svg",
	  },
	  {
		url: "./goku.mp4",
		description: "./css3.svg",
	  },
	];
	let carousel; // for calling methods of the carousel instance
	const handleNextClick = () => {
	  carousel.goToNext();
	};
  </script>
  
  <Carousel
  
	  bind:this={carousel}
	  let:loaded
	  autoplay
	  autoplayDuration={15000}
	  autoplayProgressVisible
	  
	  
  >
  
	  {#each images as src, imageIndex (src)}
		<div class="img-container">
		  {#if loaded.includes(imageIndex)}
			<!-- <img src={src.url} alt={src.description} width={'100%'} height={600} /> -->
			<div class="imagenylogo">
			<video
				width={'100%'} height={600}
				src={src.url}
				autoplay
				loop
			>
				<track kind="captions" />
			</video>
		</div>
		  {/if}
		</div>
	  {/each}
  </Carousel>


<style> 


	@keyframes grandepeq {
        0%   { transform: scale(1);}
        50% { transform: scale(1.05); }
        100%   { transform: scale(1);}

        
    }


</style>