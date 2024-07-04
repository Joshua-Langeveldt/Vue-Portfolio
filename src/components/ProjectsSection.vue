<template>
    <div class="container">
      <div class="row justify-content-center">
        <Card v-for="(project, key) in projects" :key="key">
          <template #cardHeader>
            <img :src="project.img" :alt="project.title" loading="lazy" class="card-img-top">
          </template>
          <template #cardBody>
            <h5 class="card-title">{{ project.title }}</h5>
            <p class="card-text">{{ project.description }}</p>
            <a :href="project.project_url" target="_blank" class="btn btn-primary">Visit Project</a>
          </template>
        </Card>
      </div>
      <div v-if="projects && projects.length === 0" class="d-flex justify-content-center mt-4">
        <div class="spinner-border" role="status"></div>
      </div>
    </div>
  </template>
  
  <script>
  import Card from '@/components/Card.vue';
  
  export default {
    components: {
      Card
    },
    computed: {
      projects() {
        return this.$store.state.projects;
      }
    },
    mounted() {
      this.$store.dispatch('fetchProjects');
    }
  };
  </script>
  
  <style scoped>

.image-container {
display: flex;
justify-content: center;
align-items: center;
text-align: center;
margin: 1.1rem;
   width: 30%;
   transition: all .5s;

   &:hover {
    transform: scale(1.2);
    
}


}

.hover-text {
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    visibility: hidden;
    transition: visibility 0.2s;
}

.image-container:hover .hover-text {
    visibility: visible;
    font-size: large;
}

img[alt='proImg-1'] {

height: 200px;
width: 350px;
border-radius: 20px;
border: 2px solid var(--secondary);
}

.exttay{
    display: flex;
    justify-content: center;
    color: var(--secondary);
    width: 100%;
    margin-left: 5rem;
    padding-top: 1rem;
}

.heading-exttay{
    display: flex;
    justify-content: center;
    color: var(--secondary);
    width: 100%;
    margin-left: 5rem;
    padding-top: 1rem;
}

.cust-heading-exttay{

    color:black;
    margin-top: -3rem;
}

  </style>
  