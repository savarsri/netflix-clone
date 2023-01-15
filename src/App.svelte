<script>
import Header from "./header.svelte";
</script>

<main class="fullscreen">
<div class="menuribbon">
<img src="https://pbs.twimg.com/media/EUcW85oXsAAnIBP.jpg" class="logo" alt="logo">
<Header/>
</div>

</main>


<style>

.fullscreen{
background-color: black;
}

.logo{
height:120px;
width:170px;  
}

.menuribbon{
  display: flex;
  flex-direction: row;
  width:100%;
}


</style>