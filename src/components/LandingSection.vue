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

<style>
  h1 {
      margin: 10rem;
  }

  .changingTitle {
      margin-left: -58rem;
      margin-top: -8rem;
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
</style>
