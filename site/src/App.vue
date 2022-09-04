<template>
  <div id="app-main-container">
    <HeaderBar />
    <Landing />
    <Services />
    <Formation />
    <FooterBar />
  </div>
</template>

<script>
import HeaderBar from './components/HeaderBar.vue'
import FooterBar from './components/FooterBar.vue';
import Services from './components/Services.vue'
import Formation from './components/Formation.vue'
import Landing from './components/Landing.vue'

export default {
  name: 'App',
  components: {
    HeaderBar, 
    FooterBar, 
    Services, 
    Formation, 
    Landing
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
