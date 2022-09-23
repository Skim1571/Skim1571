<template>
  <div class="about" id="about">
    <h1>My Technical Knowledge</h1>
    <div class="skills" id="rotator">
      <div class="frontend" id="frontend" @mouseover="hover = true">
        <h2>FrontEnd</h2>
        <div class="container">
          <div class="leftColumn">
            <i class="fa-brands fa-html5 fa-2x"></i><span>HTML5</span>
            <i class="fa-brands fa-css3-alt fa-2x"></i><span>CSS</span>
            <i class="fa-brands fa-square-js fa-2x"></i><span>JavaScript</span>
          </div>
          <div class="rightColumn">
            <i class="fa-brands fa-react fa-2x"></i><span>React</span>
            <i class="fa-brands fa-vuejs fa-2x"></i><span>Vue</span>
          </div>
        </div>
      </div>
      <div class="backend" id="backend">
        <h2>BackEnd</h2>
        <div class="container">
          <div class="leftColumn">
            <img src="../assets/mongodb.png" class="icon" id="mongoDB"><span>MongoDB</span>
            <img src="../assets/postgresql.png" class="icon"><span>Postgresql</span>
            <img src="../assets/django.png" class="icon"><span>Django</span>
          </div>
          <div class="rightColumn">
            <i class="fa-brands fa-node-js fa-2x"></i><span>Node.js</span>
            <img src="../assets/python.png" class="icon"><span>Python</span>
            <img src="../assets/express.png" class="icon"><span>Express.js</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutMe',
  components: {},
  data: () => ({
    // return {
    //   hover: false
    // }
  }),
  methods: {
    // handleHover(e) {

    // }
    // classChanger() {
    //   let element = document.querySelector.getElementByClassName("frontend")


    //   document.querySelector.getElementById("frontend").hover(function () {
    //     (this).addClass("spin");
    //   })
    // }

  }
}
</script>

<style>
.about {
  height: 100vh;
  color: white;
}

#logo {
  margin-top: 3rem;
}

/* credit: https://stackoverflow.com/questions/58382716/two-divs-orbiting-around-a-center-css-animation */
#rotator {
  position: relative;
  width: 45rem;
  height: 20rem;
  animation: rotations 30s linear infinite;
  border-radius: 50%;
  margin: 0 auto;
  margin-top: 20rem;
}

#frontend,
#backend {
  position: absolute;
  animation: inherit;
  animation-direction: reverse;
}

#frontend {
  background-image: url('https://i.pinimg.com/originals/bd/38/24/bd3824d20a91a706157d9f667c8f9337.jpg');
  background-size: 150%;
  background-repeat: no-repeat;
  border: 5px solid black;
  width: 40%;
  height: auto;
  color: white;
  border-radius: 3rem;
}

.container {
  display: grid;
  grid-template-columns: 10rem 10rem;
  margin-bottom: 1rem;
}

.leftColumn {
  display: flex;
  margin-left: -2rem;
  align-items: center;
  flex-direction: column;
}

.rightColumn {
  display: flex;
  margin-left: -2rem;
  align-items: center;
  flex-direction: column;
}

#spin {
  animation: spin 5s;
}

#backend {
  background-image: url('https://i.pinimg.com/originals/bd/38/24/bd3824d20a91a706157d9f667c8f9337.jpg');
  background-size: 160%;
  background-repeat: no-repeat;
  border: 5px solid black;
  border-radius: 3rem;
  bottom: -.25rem;
  right: -.25rem;
  width: 40%;
  height: auto;
  color: white;
}

.icon {
  width: 15%;
  height: 45%;
  filter: grayscale(1);
  margin-bottom: 2px;
}

#mongoDB {
  width: 15%;
}

span {
  margin-bottom: 5px;
}

@keyframes rotations {
  to {
    transform: rotate(360deg)
  }
}

@keyframes spin {
  0% {
    transform: rotateY(0deg);
  }

  50% {
    transform: rotateY(180deg);
  }

  100% {
    transform: rotateY(360deg);
  }
}
</style>

