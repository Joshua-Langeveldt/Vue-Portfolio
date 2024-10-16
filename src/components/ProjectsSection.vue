<template>
    <section id="projects" class="projects">
      <div class="container">
        <div class="row row-cols-1 row-cols-sm-2 row-cols-lg-3">
          <div
            class="col g-4 mb-4"
            v-for="project in projects"
            :key="project.title"
            data-aos="fade-up"
          >
            <div class="carding" v-if="projects.length > 0">
              <div class="image mb-2">
                <img
                  :src="project.img"
                  class="card-img-top"
                  :alt="project.title"
                  loading="lazy"
                />
              </div>
              <div class="line"></div>
              <div class="card-body">
                <h5 class="card-title text-center">{{ project.title }}</h5>
                <p class="card-text">
                  {{ project.description }}
                </p>
                <div class="links">
                  <a :href="project.github_url || '#'" class="card-link" target="_blank">
                    <button v-if="project.github_url">GitHub</button>
                  </a>
                  <a :href="project.project_url" class="card-link" target="_blank">
                    <button>Live Server</button>
                  </a>
                </div>
              </div>
            </div>
            <div v-else>
              <Spinner/>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  

  <script>
    import Spinner from "./Spinner.vue"
  export default {
    components:{
      Spinner
    },
    computed: {
      projects() {
        return this.$store.state.projects;
      },
    },
    mounted() {
      this.$store.dispatch("fetchProjects");
    },
  };
  </script>



  <style scoped>

  .container{
     margin-top: -25rem;
     
  }

  .projects {
    min-height: 100vh;
    display: flex;
    justify-content: center;
  }

  .col {
    display: flex;
    justify-content: center;
    align-content: center;
  }

  .carding {
    background: linear-gradient(to bottom,#7B3F00,  #d1691d, #ff5349);
    color: white;
    width: 23rem;
    height: 27rem;
    border-radius: 1.5rem;
    text-align: center;
    margin: 2rem;
    border: 2px solid white;
    box-shadow: .3vw .2vw .2vw silver, .1vw 0.1vw .5vw silver;
    font-family: "Italiana", sans-serif;
  font-weight: 400;
  font-style: normal;
  }
  .carding:hover {
    transform: scale(1.05);
    transition: ease-in 0.2s;
  }

  .card-title {
    height: 50px;
    margin: 2rem 3.5rem;
    border-bottom: 1px solid #000;
  }
  .image {
    display: flex;
    justify-content: center;
    background-size: contain;
    margin-top: 1rem;
  }
  img {
    display: flex;
    justify-content: center;
    height: 140px;
    width: 250px;
    border-radius: 1rem;
  }
  .card-text {
    height: 72px;
    margin: 1rem 3.7rem;
    font-size: 1.2rem;
    display: flex;
    text-align: center !important;
  }
  .links {
    text-align: center;
    display: flex;
    justify-content: center;
  }
  a {
    text-decoration: none;
  }
  button {
    background-color: #0A0D12;
    color: white;
    border-radius: 0.5rem;
    padding: 0.3rem;
    border: 0;
    width: 7rem;
    margin:2rem;
  }
  button:hover {
    background-color: #141C27;
    color: #84A7A1;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.7);
    transition: 0.2s;
    transform: scale(1.1);
  }
  ::-webkit-scrollbar {
    width: 1px;
    height: 10px;
  }
  ::-webkit-scrollbar-thumb {
    background: #84A7A1;
  }
  ::-webkit-scrollbar-track {
    background: rgba(0, 0, 0, 0.2);
  }
  @media (max-width: 1500px) {
    .projects {
      height: max-content;
    }
  }
  @media (max-width: 720px) {
   img {
    width: 200px;
    margin:1rem;
   }
   .carding{
width:110%;
height: 90%;
  }
  button{
  width: 50%;
  height:30%;
  font-size:10px;
  }

  }


  @media (max-width: 568px) {
    button:hover {
      transition: none;
      transform: none;
    }
    .card:hover {
      transform: none;
      transition: none;
    }
    img {
      width: 250px;
    }
  }
  </style>