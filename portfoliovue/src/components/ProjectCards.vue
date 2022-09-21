<template>
  <div class="projectCard">
    <div class="cardImage">
      <img :src="project.image" />
    </div>
    <div class="info-wrapper">
      <h1>{{project.title}}</h1>
      <h3>{{project.date}}</h3>
      <h3>{{project.description}}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "projectCards",
  props: {
    project: {
      title: String,
      url: String,
      image: String,
      date: String,
      description: String
    }
  }
}
</script>

<style scoped>
.projectCard {
  max-width: 300px;
  max-height: 380px;
  border-radius: 4px;
  background-image: url('https://taikotile.com/wp-content/uploads/2018/07/1602942699-White-marble-finish-tiles-2.jpg');
  cursor: pointer;
  transition: all 0.2s;
  border-radius: 10%;
  color: black;
  opacity: .8;
  margin: 4rem;
  grid-column: 1/3;
  grid-row: 1/3;
}

.projectCard:hover {
  opacity: 1;
  box-shadow: 2px 5px 5px white;
}

.projectCard .image-wrapper {
  width: auto;
}

.projectCard img {
  width: 100%;
  height: 200px;
  border-top-left-radius: 10%;
  border-top-right-radius: 10%;
}

.projectCard .info-wrapper {
  padding: 1em;
}
</style>