<template>
  <div class="app">
    <NavBar />
    <SplashScreen />
    <AboutMe />
    <ProjectSection />
  </div>

</template>

<script>
import NavBar from './components/NavBar.vue'
import SplashScreen from './views/SplashScreen.vue'
import AboutMe from './views/AboutMe.vue'
import ProjectSection from './views/ProjectSection.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    SplashScreen,
    AboutMe,
    ProjectSection
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
  background-image: url('https://wallpapertag.com/wallpaper/full/e/a/e/118475-neutral-background-1920x1080-samsung.jpg');
  height: auto;
  width: 100%;
  background-attachment: fixed;
  background-repeat: repeat;
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