<template>
  
  <!-- Main timeline container -->
<div class="timeline-container">

  <!--  timeline point -->
  <div class="timeline-point">
<i class="fa-solid fa-graduation-cap"></i> 
   <div class="popup">
      <div class="popup-number">1</div>
      <div class="popup-details">
        <div class="popup-title">Alexander Sinton High</div>
        Lorem ipsum dolor sit amet conse adipisicing elit. Dicta vitae voluptates id hic recusandae
        omnis
        cupiditate odit quis, assumenda optio?
      </div>
    </div>
  </div>

  <!--  timeline point -->
  <div class="timeline-point">
<i class="fa-sharp fa-solid fa-dog"></i>   
    <div class="popup">
      <div class="popup-number">2</div>
      <div class="popup-details">
        <div class="popup-title">Mango5 Dotsure</div>
        Lorem ipsum dolor sit amet conse adipisicing elit. Dicta vitae voluptates
        id hic recusandae omnis cupiditate odit quis, assumenda optio?
      </div>
    </div>
  </div>

  <!-- timeline point -->
  <div class="timeline-point">
<i class="fa-sharp fa-solid fa-comments-dollar"></i>  
  <div class="popup">
      <div class="popup-number">3</div>
      <div class="popup-details">
        <div class="popup-title">Sanlam</div>
        Lorem ipsum dolor sit amet conse adipisicing elit. Dicta
        vitae voluptates
        id hic recusandae omnis cupiditate odit quis, assumenda optio?
      </div>
    </div>
  </div>

  <!--  timeline point -->
  <div class="timeline-point">
<i class="fa-solid fa-house-chimney-user"></i> 
   <div class="popup">
      <div class="popup-number">4</div>
      <div class="popup-details">
        <div class="popup-title">IHS House Sitting</div>
        Lorem ipsum dolor sit amet conse adipisicing elit. Dicta vitae voluptates id hic recusandae
        omnis
        cupiditate odit quis, assumenda optio?
      </div>
    </div>
  </div>

  <!--  timeline point -->
  <div class="timeline-point">
<i class="fa-solid fa-laptop-code"></i>
    <div class="popup">
      <div class="popup-number">5</div>
      <div class="popup-details">
        <div class="popup-title">Life Choice Academy</div>
        Lorem ipsum dolor sit amet conse adipisicing elit. Dicta
        vitae voluptates id hic recusandae omnis cupiditate odit quis, assumenda optio?
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {

}
</script>

<style scoped>

@import url("https://fonts.googleapis.com/css2?family=Nunito+Sans:ital,opsz,wght@0,6..12,200..1000;1,6..12,200..1000&display=swap");


/* Timeline container styling */
.timeline-container {
  display: flex;
  gap: 33.5px;
  width: 200%;
  height: 154px;
  justify-content: center;
  font-weight: 900;
  font-size: 3rem;
}

/* Individual timeline point styling */
.timeline-point {
  transition-duration: 0.5s;
  border-radius: 50%;
  background: linear-gradient(145deg, #1e2125, #23282c);
  box-shadow: 13.4px 13.4px 40.2px #1c1f23, -13.4px -13.4px 40.2px #262b2f;
  display: grid;
  place-items: center;
  width: 168px;
  height:154px;
  position: relative;
  color: var(--color);
}

.timeline-point::before {
  content: "";
  width: 200px;
  height: 200px;
  z-index: -1;
  border-radius: 50%;
  position: absolute;
  background: conic-gradient(
    var(--color) var(--angle),
    transparent 0deg 360deg
  );
  animation: rotateBorder 1s linear var(--delay) forwards;
}

.timeline-point:nth-child(odd)::before {
  transform: rotate(-90deg);
}

.timeline-point:nth-child(even)::before {
  transform: rotate(90deg) scaleY(-1);
}

/* Custom property for angle */
@property --angle {
  syntax: "<angle>";
  initial-value: 0deg;
  inherits: false;
}

/* Common styling for timeline points */
.timeline-point:nth-child(1) {
  --color: rgb(136, 136, 230);
  --delay: 0s;
}

.timeline-point:nth-child(2) {
  --color: #ffcc00;
  --delay: 1s;
}

.timeline-point:nth-child(3) {
  --color: rgb(136, 136, 230);
  --delay: 2s;
}

.timeline-point:nth-child(4) {
  --color: #ffcc00;
  --delay: 3s;
}

.timeline-point:nth-child(5) {
  --color: rgb(136, 136, 230);
  --delay: 4s;
}

/* Popup styling */
.popup {
  width: 321.6px;
  height: auto;
  max-height: 0;
  background-color: var(--color);
  display: grid;
  grid-template-columns: 16% 84%;
  position: absolute;
  color: white;
  border-radius: 30px;
  box-shadow: 6.7px 6.7px 21.4px #17191d, -6.7px -6.7px 21.4px #212529;

  transform-origin: bottom bottom;
  animation: expandPopup 0.5s linear calc(var(--delay) + 0.5s) forwards;
}

.timeline-point:nth-child(odd) .popup {
  bottom: 221.1px;
}

.timeline-point:nth-child(even) .popup {
  top: 221.1px;
}

/* Popup number styling */
.popup-number {
  grid-row: span 2;
  display: grid;
  font-size: 2rem;
  font-weight: bold;
  color:#fff;
  place-items: center;
  cursor: auto;
  animation: fadeIn 0.5s linear calc(var(--delay) + 0.7s) forwards;
  opacity: 0;
  height: 100%;
}

/* Popup title styling */
.popup-title {
  color: var(--color);
  padding-bottom: 6.7px;
  font-size: 1.2rem;
  font-weight: 400;
}

/* Popup details styling */
.popup-details {
  padding: 20.1px;
  background-color: #1c1f23;
  border-radius: 30px;
  opacity: 0;
  font-weight: 500;
  user-select: none;
  cursor: auto;
  overflow: hidden;
  font-size: 0.8rem;
  text-align: justify;
  background: linear-gradient(145deg, #16181b, #22262b);
  margin: 3.35px;
  animation: fadeIn 0.5s linear calc(var(--delay) + 0.7s) forwards;
}

.popup::before {
  content: "";
  width: 6.7px;
  height: 0;
  border-radius: 20px;
  background-color: var(--color);
  position: absolute;
  left: 50%;
  top: -41.9px;
  display: flex;
  animation: drawLine 0.5s linear var(--delay) forwards;
}

.timeline-point:nth-child(odd) .popup:before {
  top: calc(100% + 47px);
  transform: rotateX(180deg);
  transform-origin: top;
}

/* Hover effect for timeline points */
.timeline-point:hover {
  background: linear-gradient(145deg, var(--color), #1e2125);
  color: white;
}

/* Animation for border rotation */
@keyframes rotateBorder {
  from {
    --angle: 0deg;
  }

  to {
    --angle: 180deg;
  }
}

/* Animation for popup expansion */
@keyframes expandPopup {
  0% {
    max-height: 0;
  }

  100% {
    max-height: 200px;
  }
}

/* Animation for line drawing */
@keyframes drawLine {
  0% {
    height: 0%;
    opacity: 0;
  }

  100% {
    height: 33.5px;
    opacity: 1;
  }
}

/* Animation for fade-in effect */
@keyframes fadeIn {
  to {
    opacity: 1;
  }
}

@media (max-width: 720px) {
  body {
    height: auto;
    display: block;
  }
  .timeline-container {
    flex-direction: column;
    height: auto;
    width: 100%;
    padding: 100px 0px;
  }

  .timeline-point {
    height: 134px;
    flex-shrink: 0;
    left: calc(-321px / 2);
    margin: 0px auto;
    position: relative;
  }

  .timeline-point:nth-child(odd)::before {
    transform: rotate(0deg);
  }

  .timeline-point:nth-child(even)::before {
    transform: rotate(0deg) scaleX(-1);
  }

  .timeline-point .popup:before {
    display: none;
  }

  .timeline-point:nth-child(odd) .popup {
    bottom: auto;
    right: -370.1px;
  }

  .timeline-point:nth-child(even) .popup {
    top: auto;
    right: -370.1px;
  }
}

</style>