<template>
  <div class="app">
    <NavBar />
    <SplashScreen />
    <AboutMe />
  </div>

</template>

<script>
import NavBar from './components/NavBar.vue'
import SplashScreen from './views/SplashScreen.vue'
import AboutMe from './views/AboutMe.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    SplashScreen,
    AboutMe,

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
  box-sizing: border-box;
}

#logo {
  border-radius: 50%;
  border: 2px solid black;
}
</style>
