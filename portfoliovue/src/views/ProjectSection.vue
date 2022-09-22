<template>
  <div class="projects" id="projects">
    <div>
      <h1>My Recent Projects</h1>
    </div>
    <div class="projectsCards">
      <ProjectCards :key="project.title" :project="project" v-for="project in projects" />
    </div>
  </div>
</template>

<script>
import ProjectCards from '../components/ProjectCards.vue';
export default {
  name: "ProjectSection",
  data: () => ({
    projects: [{
      "title": "PetMe",
      "url": "https://petme.herokuapp.com",
      "image": "https://i.imgur.com/BchhYg9.png",
      "date": "9/14/22",
      "description": "PostGresql, Django, Python, React"
    },
    {
      "title": "LFG",
      "url": "https://group-finder-pro.herokuapp.com/",
      "image": "https://i.imgur.com/sl9EQxl.png",
      "date": "8/30/22",
      "description": "PostGresql, Express, React, Node.js"
    },
    {
      "title": "StrokeCaddy",
      "url": "https://strokecaddy.herokuapp.com/",
      "image": "https://i.imgur.com/ZZrQdSe.png",
      "date": "8/11/22",
      "description": "Mongoose, Express, React, Node.js"
    },
    ]
  }),
  mounted() {

  },
  components: {
    ProjectCards
  }
}
</script>

<style>
.projects {
  height: 150vh;
  color: white;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.projectCards {
  display: grid;
  grid-template-columns: repeat(2, 100px);
  grid-template-rows: repeat(2, 100px);
}
</style>