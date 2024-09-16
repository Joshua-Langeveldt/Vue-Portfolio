<template>
    <div class="row bg-img container-fluid" id="landing-content">
        <div class="d-flex justify-content-end align-items-end">
            <h1 class="landing-title">Hey, My Name Is <span><br>Jamin Joshua<br>Langeveldt</span></h1>
            <div id="details">
                <p v-if="title" class="changingTitle">
                    I Am A
                    <span>{{ title }}</span>
                </p>
                <Spinner v-else/>
            </div>
            <a href="https://drive.google.com/uc?export=download&id=1eR4opf_Mh8h2LNUNjNpJUVlSUcLiiFge" id="download-link"><button class="btn cv-btn">Download CV</button></a>
        </div>
        <div class="rotating-div image-box border-animation container-fluid">
            <img src="https://joshua-langeveldt.github.io/images/images/Logo/king2.webp" alt="Crown" class="crown-image">
            <div class="card">
                <img src="https://joshua-langeveldt.github.io/images/images/People/Jam-Inside.jpg" alt="landing-img">
            </div>
        </div>
        <div class="col"></div>
    </div>
  </template>
  
  <script setup>
    import Spinner from './Spinner.vue'
    import { computed, onMounted, ref } from 'vue'
    import { useStore } from 'vuex'
    const store = useStore()
    const jobTitle = computed(() => store.state.jobTitle)
  
    const title = ref('a software developer')
    const cnt = ref(-1)
  
    function repeat() {
        try {
            if (cnt.value == jobTitle.value?.length) cnt.value = 0;
            title.value = jobTitle.value?.at(cnt.value);
            setTimeout(repeat, 2000)
            cnt.value++
        } catch (e) {
            //
        }
    }
  
    onMounted(() => {
        store.dispatch('fetchJobTitle')
        repeat()
    })
  </script>
  
  <style scoped>

.cv-btn{
  background-color: #0A0D12;
    color: white;
    border-radius: 1rem;
    padding: 0.3rem;
    border: 0;
    width: 9rem;
    margin-top:15rem;
    height: 3.5rem;
    margin-left: -47rem;

}

.cv-btn:hover{
  background-color: gold;
    color: #000;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.7);
    transition: 0.2s;
    transform: scale(1.1);
}
    h1 {
        margin: 10rem;
    }
  
    .changingTitle {
        margin-left: -48rem;
        margin-top: -7rem;
        color: white;
        font-size: 1.9rem;
        font-family: "Italiana", sans-serif;
        font-weight: 700;
        font-style: normal;
    }
  
    /*CrownStyling*/
    .crown-image {
        position: absolute;
        top: -185%;
        left: 55%;
        transform: translateX(-50%);
        width: 140px; 
        z-index: 1; 
        }
  
        /* Media queries for responsiveness */
        @media (max-width: 720px) {
          .cv-btn{
  background-color: #0A0D12;
    color: white;
    border-radius: 1rem;
    padding: 0.3rem;
    border: 0;
    width: 9rem;
    margin-top:5rem;
    height: 3.5rem;
    margin-left: -55rem;

}

.cv-btn:hover{
  background-color: gold;
    color: #84A7A1;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.7);
    transition: 0.2s;
    transform: scale(1.1);
}
  
  .d-flex {
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.changingTitle {
  margin-top: -4rem;
  margin-left:-54rem;
  font-size: 2rem;
}

.landing-title {
  font-size: 5rem;
  margin-top: 6rem;
}

.rotating-div{

   width:30%;
   margin-top: 37rem;
   margin-left: 8rem;
   margin-bottom: -10rem;
}
}

@media (max-width: 300px) {
  .cv-btn{
  background-color: #0A0D12;
    color: white;
    border-radius: 1rem;
    padding: 0.3rem;
    border: 0;
    width: 9rem;
    margin-top:10rem;
    height: 3.5rem;
    margin-left: -70rem;

}

.cv-btn:hover{
  background-color: gold;
    color: #84A7A1;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.7);
    transition: 0.2s;
    transform: scale(1.1);
}

.d-flex {
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.landing-text {
  margin-top: 1rem;
  margin-right: 0;
}

.landing-title {
  margin-top: 10rem;
  font-size: 8rem;
  margin-bottom: 2rem;
}

.changingTitle {
  margin-right:14.5rem !important;
  font-size: 3.5rem;
  margin-top: 1rem;
}

.rotating-div{

width:40%;
height: 30%;
margin-top: 70rem;
margin-left: 8rem;
margin-bottom: 10rem;
}

.crown-image {
    position: absolute;
    top: -155%;
    left: 51%;
    transform: translateX(-50%);
    width: 150px; 
    z-index: 1; 
    }
}
  </style>
  
