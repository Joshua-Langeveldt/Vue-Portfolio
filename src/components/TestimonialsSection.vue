<template>
    <div id="carouselExampleCaptions" class="carousel slide">
      <div class="carousel-indicators">
        <button v-for="(testimonial, index) in testimonials" :key="index"
                type="button" data-bs-target="#carouselExampleCaptions" :data-bs-slide-to="index"
                :class="{ 'active': index === 0 }" :aria-current="index === 0" :aria-label="`Slide ${index + 1}`"></button>
      </div>
  
      <div class="carousel-inner" v-if="testimonials?.length">
        <div v-for="(testimonial, index) in testimonials" :key="index"
             :class="['carousel-item', { 'active': index === 0 }]">
          <div class="d-flex justify-content-center align-items-center">
            <div :class="`card-deck col-sm ardcay-style${index + 1}`">
              <div class="ardcay">
                <div class="ardcay-body">
                  <img :src="testimonial.image" alt="Image1">
                  <h5 class="ardcay-title">{{ testimonial.name }}</h5>
                  <p class="ardcay-text">{{ testimonial.text }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
  
      <!-- Placeholder for loading state -->
      <div v-else>
        Loading testimonials...
      </div>
  
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </template>
  
  
  <script setup>
  
  import { computed, onMounted } from 'vue'
import { useStore } from 'vuex'
    const store = useStore()
    const testimonials = computed(() => store.state.testimonials )
    onMounted(() => {
      setTimeout(()=>{
        store.dispatch('fetchTestimonials')
      }, 1000)
    })

  </script>

<style scoped>

/*Testimonial Styling*/

.card-deck{
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 5rem;
    width: 50%;

    transition: all .5s;
    
    &:hover {
        transform: scale(1.2);
        color: white;

    }
    
}

.ardcay {
    width: 550px;
    height: 350px;
    border: 3px solid #fff;
    border-radius: 30px;
    box-shadow: .3vw .2vw .2vw silver, .1vw 0.1vw .5vw silver;


} 

.ardcay-body {
    padding: 20px;
}

.ardcay-title {
    font-size: 1.5em;
    color: var(--secondary);
    font-family: "Italiana", sans-serif;
  font-weight: 400;
  font-style: normal;
	text-align:center;
	margin-top: 0px;


}

.ardcay-text {
    color: var(--secondary);
    font-size: 1rem;
    font-family: "Italiana", sans-serif;
  font-weight: 400;
  font-style: normal;
    width:100%;
	text-align:center;
    padding-left: 0px;
    margin-left: 0%;
  
}

#ardcay-style1{

    margin-left: -18rem;
}

#ardcay-style2{

    margin-left: -18rem;
}

#ardcay-style3{

    margin-left: -18rem;
}

#ardcay-style4{

    margin-left: -18rem;
}

#ardcay-style5{

    margin-left: -18rem;
}

/*Testimonial-Image*/

img[alt='Image1'] {

    height: 70px;
    width: 70px;
    border-radius: 20px;
    border: 2px solid #FFEBB2;

    &:hover {
        transform: scale(1.2);
        height: 100px;
        width:100px;
        margin: 8px;
    }
}


@media screen and (max-width: 300px) {
.ardcay {
    width: 550px;
    height: auto; 
    border: 3px solid #fff;
    border-radius: 30px;
    box-shadow: .3vw .2vw .2vw silver, .1vw 0.1vw .5vw silver;
} 


}
</style>