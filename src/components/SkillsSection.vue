<template>
    <div class="cust-container">
      <div class="animation-container" :class="{ 'animation-reverse': isAnimationReverse }" ref="animationContainer">
        <div class="ball glowing" style="width: 100px; height: 100px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/DOM.jpg" />
        </div>
        
        <div class="ball glowing" style="width: 100px; height: 100px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/html.png" />
        </div>
        
        <div class="ball glowing" style="width: 100px; height: 100px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/css.webp" />
        </div>
        
        <div class="ball glowing" style="width: 80px; height: 80px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/bootstrap.jpg" />
        </div>
        
        <div class="ball glowing" style="width: 80px; height: 80px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/javascript.webp" />
        </div>
        
        <div class="ball glowing" style="width: 80px; height: 80px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/cli.png" />
        </div>
        
        <div class="ball glowing" style="width: 60px; height: 60px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/api.jpg" />
        </div>
        
        <div class="ball glowing" style="width: 60px; height: 60px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/database.jpg" />
        </div>
        
        <div class="ball glowing" style="width: 60px; height: 60px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/github.png" />
        </div>
        
        <div class="ball glowing" style="width: 60px; height: 60px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/mongoDB.png" />
        </div>
        
        <div class="ball glowing" style="width: 50px; height: 50px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/node.png" />
        </div>
        
        <div class="ball glowing" style="width: 50px; height: 50px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/sql.png" />
        </div>
        
        <div class="ball glowing" style="width: 50px; height: 50px;">
          <img class="skill-img" src="https://joshua-langeveldt.github.io/images/images/Skills/ui&ux.png" />
        </div>
      </div>
      
      <div class="button-container">
        <i class="toggle-icon fas fa-sync-alt" @click="toggleOrbitDirection"></i>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isAnimationReverse: false
      };
    },
    methods: {
      toggleOrbitDirection() {
        this.isAnimationReverse = !this.isAnimationReverse;
      }
    }
  };
  </script>
  
  <style scoped>


  .cust-container {
    background-size: cover;
    background-position: center;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    color: #fff;
  }
  
  .animation-container {
    position: relative;
    width: 850px;
    height: 500px;
    margin: auto;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
    top: 35%;
    transform: translateY(-55%);
  }
  
  .ball {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 600px; 
    height: 300px; 
    border-radius: 50%;
    box-shadow: 0 0 10px 5px #ffcc00;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: white;
  }
  
  .ball.glowing {
    animation: orbit 5s linear infinite, glow 1s ease-in-out infinite alternate;
  }
  
  .ball:nth-child(1) {
    width: 80px;
    height: 80px;
    top: 50%;
    left: 50%;
    margin-top: -15px;
    margin-left: -15px;
    animation-duration: 45s;
  }
  
  .ball:nth-child(2) {
    width: 90px;
    height: 90px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 35s;
  }
  
  .ball:nth-child(3) {
    width: 40px;
    height: 40px;
    top: 50%;
    left: 50%;
    margin-top: -20px;
    margin-left: -20px;
    animation-duration: 30s;
  }
  
  .ball:nth-child(4) {
    width: 45px;
    height: 45px;
    top: 50%;
    left: 50%;
    margin-top: -22.5px;
    margin-left: -22.5px;
    animation-duration: 25s;
  }
  
  .ball:nth-child(5) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 20s;
  }
  
  .ball:nth-child(6) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 15s;
  }
  
  .ball:nth-child(7) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 10s;
  }
  
  .ball:nth-child(8) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 10.5s;
  }
  
  .ball:nth-child(9) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 9.5s;
  }
  
  .ball:nth-child(10) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 8s;
  }
  
  .ball:nth-child(11) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 7.5s;
  }
  
  .ball:nth-child(12) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 6s;
  }
  
  .ball:nth-child(13) {
    width: 50px;
    height: 50px;
    top: 50%;
    left: 50%;
    margin-top: -25px;
    margin-left: -25px;
    animation-duration: 5.5s;
  }
  
  @keyframes orbit {
    0% {
      transform: rotate(0deg) translateY(210px) rotate(0deg);
    }
  
    100% {
      transform: rotate(360deg) translateY(210px) rotate(-360deg);
    }
  }
  
  @keyframes glow {
    0% {
      box-shadow: 0 0 15px 5px #d00303;
    }

    50% {
        box-shadow: 0 0 15px 5px rgb(61, 61, 231);

    }
  
    100% {
      box-shadow: 0 0 25px 10px #ffcc00 ;
    }
  }
  
  .animation-reverse .ball.glowing {
    animation-direction: reverse;
  }
  
  .button-container {
    position: absolute;
    top: 340%;
    left: 50.5%;
    transform: translate(-50%, -50%);
    z-index: 1;
    background-color: rgba(0, 0, 0, 0.7);
    padding: 20px;
    border-radius: 50%;
    transition: background-color 0.3s ease;
  }
  
  .button-container:hover {
    background-color: rgba(0, 0, 0, 0.5);
  }
  
  .toggle-icon {
    color: #ffcc00;
    font-size: 24px;
    cursor: pointer;
    transition: all 0.3s ease;
  }
  
  .toggle-icon:hover {
    color: #ffffff;
  }
  
  .skill-img {
    width: 100%;
    height: 100%;
    border-radius: 50%;
  }

/* Additional styles for responsiveness */
@media screen and (max-width: 720px) {


  .animation-container {
    width: 100%;
    height: 50%;   
    top: 15%; 
  }

  .button-container{

    top: 180rem !important;
    left:29rem;
  }

  .button-container:hover {
    background-color: rgba(0, 0, 0, 0.5);
  }

  .toggle-icon {
    color: #ffcc00;
    font-size: 24px;
    cursor: pointer;
    transition: all 0.3s ease;
  }
  
  .toggle-icon:hover {
    color: #ffffff;
  }

}

@media screen and (max-width: 300px) {
  .animation-container {
    width: 100%;
    height: 250px; 
    top: 20%;
  }

  .button-container{
top: 237rem !important;
left:37rem;
}

.button-container:hover {
background-color: rgba(0, 0, 0, 0.5);
}

.toggle-icon {
color: #ffcc00;
font-size: 24px;
cursor: pointer;
transition: all 0.3s ease;
}

.toggle-icon:hover {
color: #ffffff;
}

}

  </style>
  