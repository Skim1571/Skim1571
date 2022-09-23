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
      "description": "PostgreSQL, Django, Python, React"
    },
    {
      "title": "LFG",
      "url": "https://group-finder-pro.herokuapp.com/",
      "image": "https://i.imgur.com/sl9EQxl.png",
      "date": "8/30/22",
      "description": "PostgreSQL, Express, React, Node.js"
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
  components: {
    ProjectCards
  }
}
</script>

<style>
.projects {
  height: 100vh;
  color: white;
  display: flex;
  align-items: center;
  flex-direction: column;
}

.projectsCards {
  width: 100vw;
  display: grid;
  grid-template-columns: repeat(2, auto);
  grid-template-rows: repeat(3, auto);
  justify-content: center;
}
</style>