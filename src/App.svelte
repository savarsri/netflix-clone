<script>
import Header from './header.svelte'

// Get the video
var video = document.getElementById("myVideo");

// Get the button
var btn = document.getElementById("myBtn");
</script>
  
<main class="fullscreen">
  <h1 style="font-family:Centaur"><h1 style="font-size:50px">CHILLFLIX</h1></h1>
  <Header/>
  <video autoplay muted loop id="myVideo">
    <source src="https://assets.codepen.io/6093409/river.mp4" type="video/mp4">
  </video>
  <div class="content">
  
    <!-- Use a button to pause/play the video with JavaScript -->
    <!-- <button id="myBtn" on:click={myFunction}>Pause</button> -->
  </div>
</main>

<style>

#myVideo {
  position: relative;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 400px;
  /* overflow:visible; */
}

.fullscreen{
  top:0;
  right:0;
  left:0;
  bottom:0;
  overflow:auto;
  /* background-color: indigo; */
}

h1{
  overflow:auto;
  padding:20px;
  text-align: center;
  color:yellow;
  width:auto;
  height:20%;
  margin:0%;
  border: 2px solid red;
  background-color: black;
}    
:root{
      background-color: #181818;
    }

    /* Add some content at the bottom of the video/page */
.content {
  position: fixed;
  bottom: 0;
  background: rgba(0, 0, 0, 0.5);
  color: #f1f1f1;
  width: 100%;
  padding: 20px;
}

/* Style the button used to pause/play the video */
#myBtn {
  width: 200px;
  font-size: 18px;
  padding: 10px;
  border: none;
  background: #000;
  color: #fff;
  cursor: pointer;
}

#myBtn:hover {
  background: #ddd;
  color: black;
}
</style>
