<template>
  <div id="app">
    <TheHero />
    <ProjectsList/>
  </div>
</template>

<script>
import TheHero from "./components/TheHero.vue";
import ProjectsList from "./components/ProjectsList.vue";

export default {
  name: "App",
  components: {
    TheHero,
    ProjectsList
},
};
</script>

<style lang="scss">
@import "assets/styles/main.scss";





</style>
