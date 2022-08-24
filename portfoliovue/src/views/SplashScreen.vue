<template>
  <div class="splashscreen">
    <div class="splash">
      <h1>Hello, I'm <span class="highlightedRed"> Steve </span> J Kim</h1>
      <h1>Welcome to my portfolio</h1>
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

</script>

<style>
.splashscreen {
  display: flex;
  background-color: aquamarine;
  width: 100%;
  height: 100vh;
  text-align: center;
  align-items: center;
  justify-content: center;
  flex-direction: column;
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
  background-color: rgb(81, 206, 206, .4);
  width: 10rem;
  padding: 1rem;
  margin-top: 5rem;

}

.generalButton:hover {
  background-color: rgb(81, 206, 206, .8);
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