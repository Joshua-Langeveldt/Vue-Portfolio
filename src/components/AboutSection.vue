<template>
<section class="row max-height" id="about">   
  <div class="row">
    <div class="d-flex justify-content-between">
      <div class="cust-about"> 
        <p class="about-page">Hi There, My name is Jamin Langeveldt and I'm on a journey to becoming a Full Stack Web Developer.
          I consider myself to be a very hardworking person that is goal orientated. 
          I believe that you should chase your dreams and have fun doing it due to the fact that we only live once. 
          My skill set allows me to adapt to any circumstance and working environment easily. 
          I have a hunger for gaining experience and remain dedicated in everything I do.</p>
      </div>

      <div class="container">
        <!-- Loop generated boxes -->
        <div class="box-container">
          <div class="box box1"></div>
          <div class="box box2"></div>
          <div class="box box3"></div>
          <div class="box box4"></div>
          <div class="box box5"></div>
          <div class="box box6"></div>
          <div class="box box7"></div>
          <div class="box box8"></div>
          <div class="box box9"></div>
          <div class="box box10"></div>
        </div>
      </div>
    </div>
  </div> 
</section>
</template>

<script>
export default {

}
</script>

<style scoped>
/* Slide in from the left */
@keyframes slideInFromLeft {
from {
opacity: 0;
transform: translateX(-100px); 
}
to {
opacity: 1;
transform: translateX(0);
}
}

/* Apply the animation */
.about-page {
animation: slideInFromLeft 8s ease both; 
}

.container {
display: flex;
align-items: flex-end;
gap: 2px;
justify-content: space-evenly;
height: 400px;
width: 565px;
/* transform: rotate3d(-1, -2, 0.2, 32deg); */
}

.box-container {
display: grid;
grid-template-columns: repeat(5, 100px); 
grid-template-rows: repeat(2, 100px); 
column-gap: 10px;
}

.box {
margin-top: -10rem;
width: 100%;
height: 100%;
background-image: url('https://joshua-langeveldt.github.io/images/images/Logo/LOGO.png');
background-size: auto auto; 
border: 2px solid white;
border-radius: 3px 3px 0 0;
box-shadow: 8px 6px 4px  #000;

/* -webkit-box-reflect:  0 linear-gradient(rgba(0,0,0,0), rgba(0,0,0,0.4)); */
animation: raise 5s ease infinite alternate;
}

.box1 { background-position: 0px 0px; }
.box2 { background-position: -100px 0px; }
.box3 { background-position: -200px 0px; }
.box4 { background-position: -300px 0px; }
.box5 { background-position: -400px 0px; }
.box6 { background-position: 0px -100px; }
.box7 { background-position: -100px -100px; }
.box8 { background-position: -200px -100px; }
.box9 { background-position: -300px -100px; }
.box10 { background-position: -400px -100px; }

.box:hover {
filter: grayscale(1);
}

@keyframes raise {
0% { height: 25%; }
50% { height: 100%; }
100% { height: 300%; }
}

@media (max-width: 720px) {
  .about-page {
    margin-left: 0;
    width: 300%;
    font-size: 1rem;
  }

  .container {
    margin-top: 0rem;
    transform: rotate3d(-1, -2, 0.2, 32deg);
    margin-left:15rem;

  }
.box-container {
  column-gap:1px;
}

}

@media (max-width: 300px) {
  .about-page {
    font-size: 2rem;
    width: 110%;
    margin-left: 10rem;
  }

  .box-container {
      display: none;
  }

}
</style>
