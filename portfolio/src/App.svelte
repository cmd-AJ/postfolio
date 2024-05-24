<script>
  import Headermenu from './lib/Headermenu.svelte';
  import Counter from './lib/Counter.svelte'
  import Mainproject from './lib/Mainproject.svelte';
</script>

<header><Headermenu></Headermenu></header>

<main>
  <div >
    <Mainproject></Mainproject>

  </div>
</main>

<footer>
  <button style=" background-image: url('https://i.pinimg.com/736x/b5/1b/78/b51b78ecc9e5711274931774e433b5e6.jpg')  " ></button>
  <button style=" background-image: url('https://static1.srcdn.com/wordpress/wp-content/uploads/2021/12/Gmail-Dark-Mode.jpg')" ></button>
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
    margin-top: 51vh;
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