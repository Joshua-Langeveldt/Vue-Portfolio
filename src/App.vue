<template>
  <div class="wrapper">
    <NavComp />
    <main class="container-fluid">
      <router-view />
    </main>
    <FooterComp />
  </div>

</template>

<script>
import NavComp from '@/components/Navbar.vue' 
import FooterComp from '@/components/Footer.vue'

export default {
  components: {
    NavComp,
    FooterComp
  },
  computed: {
    jobTitle(){
      return this.$store.state.jobTitle
    }
  },

}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
