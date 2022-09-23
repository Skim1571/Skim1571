<template>
  <div class="app">
    <NavBar />
    <SplashScreen />
    <AboutMe />
    <ProjectSection />
    <ContactMe />
  </div>

</template>

<script>
import NavBar from './components/NavBar.vue'
import SplashScreen from './views/SplashScreen.vue'
import AboutMe from './views/AboutMe.vue'
import ProjectSection from './views/ProjectSection.vue'
import ContactMe from './views/ContactMe.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    SplashScreen,
    AboutMe,
    ProjectSection,
    ContactMe
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

body {
  margin: 0;
}

/* credit: https://dev.to/gmeben/animating-gradients-with-pure-css-3bi8 */
.app {
  /* animation: animateBg 10s linear infinite; */
  /* background-image: linear-gradient(45deg, #42eca6, #64b3d9, #208ea2, #498ada, #5b73df, #897ed3, #5b73df, #498ada, #208ea2, #64b3d9, #42eca6); */
  background-image: url('https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.shopify.com%2Fs%2Ffiles%2F1%2F0761%2F8649%2Ffiles%2FHexagon_Wood_Nut_1.jpg%3F6559309705414561036&f=1&nofb=1');
  background-size: cover;
  min-height: max-content;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
}

/* @keyframes animateBg {
  0% {
    background-position: 0% 0%;
  }

  100% {
    background-position: 0% 100%;
  }
} */
</style>