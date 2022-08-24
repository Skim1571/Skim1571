<template>
  <div class="about">
    <div>
      <img id="logo" alt="SteveKim logo" src="../assets/steve.jpg" />
      <h1>This is the about page</h1>
      <TextSphere :items_list="items_list" />

    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutMe',
  components: {},
  data: () => ({
  }),
  methods: {

  }
}
</script>

<style>
.about {
  height: 100vh;
}

#logo {
  margin-top: 3rem;
}
</style>