<template>
  <div>
    <section class="row" id="landing">
      <LandingSection /> 
    </section>

    <section class="row max-height" id="about">
      <h2 class="main-heading">About</h2>
      <div class="row">
        <div class="d-flex justify-content-between">

<div class="cust-about"> 

  <p class="about-page">Hi There, My name is Jamin Langeveldt and I'm on a journey to becoming a Full Stack Web Developer.
    I consider myself to be a very hardworking person that is goal orientated. 
    I believe that you should chase your dreams and have fun doing it due to the fact that we only live once. 
    My skill set allows me to adapt to any circumstance and working environment easily. 
    I have a hunger for gaining experience and remain dedicated in everything I do.</p>
</div>

<!--FlipCard-->
<div class="flip-card">
  <div class="flip-card-inner">
    <div class="flip-card-front">
      <img src="https://joshua-langeveldt.github.io/images/images/Logo/LOGO.png" alt="flipCard" >
    </div>
    <div class="flip-card-back">
       <img src="https://joshua-langeveldt.github.io/images/images/People/jam.png" alt="flipCard" >

    </div>
  </div>
</div>

</div>
      </div>
    </section>

    <section class="row max-height" id="education">
      <h2 class="main-heading">Education</h2>
    </section>

    <section class="row max-height" id="skills">
      <h2 class="main-heading">Skills</h2>
    </section>

    <section class="row max-height" id="testimonials">
      <h2 class="main-heading">Testimonials</h2>
    </section>

    <section class="row max-height" id="projects">
      <h2 class="main-heading">Projects</h2>
    </section>

    <section class="row max-height" id="contact">
      <h2 class="main-heading">Contact</h2>
    </section>

  </div>
</template>

<script>
import LandingSection from '@/components/LandingSection.vue'
export default {
  name: 'HomeView',
  components: {
    LandingSection
  }
}
</script>