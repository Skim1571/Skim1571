<template>
  <div class="splashscreen" id="home">
    <div>
      <img id="logo" alt="SteveKim logo" src="../assets/steve.jpg" @mouseover="hover=true" @mouseleave="hover=false"
        :class="{active: hover}" />
    </div>
    <div class="splash">
      <h1>Hello, I'm <span class="highlightedRed"> Steve </span> J Kim.</h1>
      <h1>I am a Full-Stack Developer.</h1>
      <button class="generalButton">
        <a href="https://docs.google.com/document/d/1nSnICbjNWaXKM8X7TCbTT74YCHjQDtksZwv03iDKOY4/export?format=pdf"
          target="_blank"><span class="material-icons md-48">
            picture_as_pdf
          </span></a>
        <h3>Resume</h3>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      hover: false,
    }
  }
}

</script>

<style>
.splashscreen {
  display: flex;
  width: 100%;
  height: 100vh;
  text-align: center;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  color: white;
}

.active {
  animation: beat 1s;
}

@keyframes beat {
  0% {
    transform: scale(1);
  }

  25% {
    transform: scale(0.8);
  }

  50% {
    transform: scale(0.9);
  }

  75% {
    transform: scale(0.8);
  }

  100% {
    transform: scale(1);
  }

}

.splash {
  animation: fadeIn 3s;
  -webkit-animation: fadeIn 3s;
  -moz-animation: fadeIn 3s;
  -o-animation: fadeIn 3s;
  -ms-animation: fadeIn 3s;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

.highlightedRed {
  color: red;
}

.generalButton {
  border: 2px solid black;
  border-radius: 10%;
  flex-direction: column;
  background-image: url('https://i.pinimg.com/originals/bd/38/24/bd3824d20a91a706157d9f667c8f9337.jpg');
  background-size: 150%;
  width: 10rem;
  padding: 1rem;
  margin-top: 5rem;
  align-self: center;
  color: white;
}

.generalButton>a {
  color: inherit;
}

.generalButton:hover {
  background-color: rgba(255, 255, 255, 0.8);
  color: black;
}

.generalButton>a:hover {
  color: black;
}

.material-icons.md-18 {
  font-size: 18px;
}

.material-icons.md-24 {
  font-size: 24px;
}

.material-icons.md-36 {
  font-size: 36px;
}

.material-icons.md-48 {
  font-size: 48px;
}
</style>