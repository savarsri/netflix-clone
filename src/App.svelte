<script>
import Header from "./header.svelte";

var currentIndex = 1;
displaySlides(currentIndex);

function setSlidesf(num) {
    displaySlides(currentIndex += num);
}

function setSlidesb(num) {
    displaySlides(currentIndex -= num);
}

function displaySlides(num) {
    var x;
    var slides = document.getElementsByClassName("img");
    if (num > slides.length) { currentIndex = 1 }
    if (num < 1) { currentIndex = slides.length }
    for (x = 0; x < slides.length; x++) {
        slides[x].style.display = "none";
    }
    slides[currentIndex - 1].style.display = "block";
}
</script>

<main class="fullscreen">
<div class="menuribbon">
<img src="https://pbs.twimg.com/media/EUcW85oXsAAnIBP.jpg" class="logo" alt="logo">
<Header/>

</div>
<div class="slider">
  <div class="imageslide fade"><img src='https://www.indiewire.com/wp-content/uploads/2019/12/midsommar.jpg?w=800' alt="sliderimage#1"> 
  </div>
  <div class="imageslide fade"><img src='https://media.gettyimages.com/id/458467163/photo/the-first-avenger-movie-poster.jpg?s=612x612&w=gi&k=20&c=Fc9E7HSJmEiviWNqmLsoXGgwOdpN8fv3qZ0fem6__rM=' alt="sliderimage#1"> 
  </div>
  <div class="imageslide fade"><img src='https://i.pinimg.com/550x/4e/83/29/4e83294e9f7911d16f49343317c684cd.jpg' alt="sliderimage#1"> 
  </div>
  <div class="imageslide fade"><img src='https://www.designer-daily.com/wp-content/uploads/2012/12/lord-war-creative-movie-posters.jpg' alt="sliderimage#1"> 
  </div>
  <div class="imageslide fade"><img src='https://media.glamour.com/photos/56957ec78fa134644ec24e88/master/w_1600%2Cc_limit/entertainment-2014-06-the-giver-movie-poster-main.jpg' alt="sliderimage#1"> 
  </div>
  <div class="imageslide fade"><img src='https://www.indiewire.com/wp-content/uploads/2019/12/midsommar.jpg?w=800' alt="sliderimage#1"> 
  </div>
  <div class="imageslide fade"><img src='https://media.gettyimages.com/id/458467163/photo/the-first-avenger-movie-poster.jpg?s=612x612&w=gi&k=20&c=Fc9E7HSJmEiviWNqmLsoXGgwOdpN8fv3qZ0fem6__rM=' alt="sliderimage#1"> 
  </div>
  <button class="slider-btn previous" on:click={setSlidesb}>❮</button>
  <button class="slider-btn next" on:click={setSlidesf}>❯</button>
</div>
</main>


<style>

 

 
/* Our main images-slideshow container */
.slider {
  max-width: 612px;
  position: relative;
  margin: auto;
  display: flex;
  overflow:scroll;
  flex-direction: row;
}
 
/*Style for ">" next and "<" previous buttons */
.slider-btn{
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 8px 16px;
  margin-top: -22px;
  color: rgb(0, 0, 0);
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
  background-color: rgba(255, 255, 255, 0.5);
  border-radius: 50%;
}
 
/* setting the position of the previous button towards left */
.previous {
  left: 2%;
}
 /* setting the position of the next button towards right */
.next {
  right: 2%;
}
 
/* On hover, adding a background color */
.previous:hover,
.next:hover {
  color: rgb(255, 253, 253);
  background-color: rgba(0, 0, 0, 0.8);
}
  /* ------------------------------- */
/* .slider{
  display: flex;
  overflow:scroll;
  flex-direction: row;
} */
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

img{
  height: 200px;
  width: 150px;
size:50cm;
margin: 1cm 1cm;
}
</style>